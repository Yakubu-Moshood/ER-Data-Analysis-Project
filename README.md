# **Emergency Room Data Analysis Project**

## **Table of Contents**
1. [Objective](#objective)
2. [Data Source](#data-source)
3. [Stages](#stages)
4. [Design](#design)
5. [Tools](#tools)
6. [Process](#process)
    - [Data Exploration](#data-exploration)
    - [Data Cleaning](#data-cleaning)
    - [Transform the Data](#transform-the-data)
7. [Visualization](#visualization)
8. [Results](#results)
    - [DAX Measures](#dax-measures)
    - [Analysis](#analysis)
    - [Findings](#findings)
9. [Validation](#validation)
10. [Discovery](#discovery)
11. [Recommendations](#recommendations)
12. [Potential ROI](#potential-roi)
13. [Potential Courses of Actions](#potential-courses-of-actions)
14. [Conclusion](#conclusion)


## **1. objective**
The purpose of this project is to analyze emergency room (ER) operations, identify trends in patient visits, and propose actionable recommendations to optimize workflows, improve patient satisfaction, and reduce wait times.

---

## **2. Data Source**
The data was sourced from hospital ER logs from April 2003 to October 2024. It contains:
- 9,217 patient records.
- Features include patient demographics, admission details, satisfaction scores, and department referrals.

---

## **3. Stages**
The project was executed in the following stages:
1. Data exploration and cleaning.
2. Transformation of data for modeling.
3. Building interactive dashboards.
4. Final analysis and recommendations.

---

## **4. Design**
The project followed a structured design process:
- Data flow was planned from raw files to visual dashboards.
- A calendar table was created to enable data-based analysis
- Power BI dashboards were designed with user-friendly interfaces for quick insights.

---

## **5. Tools**
The following tools were used:
- **Power BI**: For data modeling, dashboards, and visualizations.
- **Power Query**: For data cleaning, transformation, and standardization. 
- **Excel**: For dataset review and minor adjustments.

---

## **6. Process**

### **Data Exploration**
- Key variables were identified, including demographics, admission times, and satisfaction scores.
- Outliers and missing data were flagged for cleaning.

### **Data Cleaning**
- Missing or incorrect values (e.g., "Declined to Identify" inpatient race) were handled.
- Standardised date-time formats for admission records.

### **Transform the Data**
- Categorical variables (e.g., patient gender, race) were encoded.
- Age groups were categorized (e.g., children, adults, seniors).
- Additional columns were added to split the patient admission date into **year*, **month*, **weekday*, **weeknomba*, and time in **hour* 

---

## **7. Visualization**
Interactive dashboards were created in Power BI, featuring:

## **a. Key Metrics Cards (Top Section)**
- Displays the total number of visits. It also tracks trends compared to the previous month.

---

## **b. Line Chart: Patient Visits by Weekday and Gender**
- A line chart displaying visit trends for males (blue) and females (pink) across the days of the week (Sunday to Saturday). This highlights the differences in visit patterns between genders and identifies which days see the highest patient traffic.

---

## **c. Bar Chart: Patient Visit by Age Range**
- A vertical bar chart breaking down visits into age groups: adults, seniors, and children. It identifies the dominant age group visiting the ER, providing insights for resource allocation based on patient demographics.

---

## **d. Matrix table: Patient Visits by Day and Time**
- A grid showing the number of visits per hour for each day of the week (Sunday to Saturday). This provides a detailed view of when the ER is busiest, both by specific hours and days of the week.

---

## **e. Score Rating Table: Patient Race**
- A table displaying racial categories (e.g., African American, Asian, White) along with corresponding satisfaction ratings (e.g., star ratings). It offers insights into satisfaction trends by race, helping identify if specific groups have consistently higher or lower satisfaction levels.

---

## **f. Horizontal Bar Chart: Avg. Wait Time by Department Referral**
- A bar chart comparing average wait times across various departments (e.g., Physiotherapy, Gastroenterology, Neurology, etc.), highlighting which departments have longer wait times, allowing hospital staff to address bottlenecks or inefficiencies.

---

## **8. Results**

### **DAX Measures**
# **Key Measures and Their Purpose**

## **i. Satisfaction Measures**
- **Avg Satisfaction Growth With Arrow**: Indicates the growth in satisfaction score compared to the previous month, with an up or down arrow.
- **Avg Satisfaction Score**: Calculates the average satisfaction score of patients.
- **Avg Satisfaction Score Growth**: Measures the percentage growth or decline in satisfaction scores compared to the previous month.
- **Avg Satisfaction Score Growth Colour**: Determines if satisfaction growth is positive ("Green") or negative ("Red").
- **Avg Satisfaction Score Max Value**: Finds the maximum satisfaction score across all days.
- **Avg Satisfaction Score Min Value**: Finds the minimum satisfaction score across all days.
- **Avg Satisfaction Score Variance**: Calculates the difference between the current month's satisfaction score and the previous month's.
- **PM Avg Satisfaction Score**: Retrieves the previous month's average satisfaction score.

---

## **ii. Wait Time Measures**
- **Avg Wait Time Growth**: Measures the percentage growth or decline in average wait time compared to the previous month.
- **Avg Wait Time Growth With Arrow**: Displays wait time growth with an up or down arrow indicator.
- **Avg Wait Time Colour**: Determines if wait time growth is positive ("Green") or negative ("Red").
- **Avg Wait Time Max Value**: Finds the maximum wait time across all days.
- **Avg Wait Time Min Value**: Finds the minimum wait time across all days.
- **Avg Wait Time Variance**: Calculates the difference between the current month's average wait time and the previous month's.
- **Avg_Wait_Time**: Calculates the average wait time of patients.
- **PM Avg Wait Time**: Retrieves the previous month's average wait time.

---

## **iii. Patient Visit Measures**
- **Patient Visit**: Counts the total number of patient visits.
- **Patient Visit Growth**: Measures the percentage growth or decline in patient visits compared to the previous month.
- **Patient Visit Growth Colour**: Determines if patient visit growth is positive ("Green") or negative ("Red").
- **Patient Visit Growth With Arrow**: Displays visit growth with an up or down arrow indicator.
- **Patient Visit Variance**: Calculates the difference between the current month's patient visits and the previous month's.
- **Patient Visits Max Value**: Finds the maximum number of patient visits across all days.
- **Patient Visits Min Value**: Finds the minimum number of patient visits across all days.
- **PM Patient Visit**: Retrieves the previous month's total number of patient visits.

---

## **iv. Peak Period Measures**
- **Busiest Day**: Identifies the day of the week with the highest number of patient visits.
- **Busiest Time**: Identifies the hour with the highest number of patient visits.

---

## **v. Other Measures**
- **Score Rating**: Converts the satisfaction score into a visual star rating (e.g., ★).
- **Calendar**: Generates a calendar table with additional columns for year, month, day, weekday, and week type (weekday or weekend).
- **Sat_Score_Param**: Parameter table for satisfaction breakdown by patient race, gender, or age range.

---

### **Analysis**
- Identified bottlenecks in the Gastroenterology and Cardiology departments.
- Discovered peak visit times at 7:00 AM and the busiest day on Wednesday.

### **Findings**
- Adult patients formed the majority of visits.
- Wait times are strongly correlated with lower satisfaction scores.

---

## **10. Validation**
Dashboards were validated against the source data to ensure consistency:
- Counts and averages matched the original dataset.
- Charts accurately reflected query outputs.

---

## **11. Discovery**
Key discoveries:
- High-volume periods could strain ER resources.
- Longer wait times led to a decrease in satisfaction scores.

---

## **12. Recommendations**
1. **Staff Optimisation**: Increase staff during peak times (e.g., 7:00 AM, midweek).
2. **Streamline Bottlenecks**: Focus on improving workflows in Gastroenterology and Cardiology.
3. **Communication**: Better communication during wait times to improve satisfaction.

---

## **13. Potential ROI**
Implementing the recommendations could:
- Reduce patient wait times by 10-15%.
- Increase satisfaction scores by 20%.
- Improve resource allocation efficiency, reducing overtime costs.

---

## **14. Potential Courses of Actions**
- Implement a shift-scheduling system to align with peak times.
- Introduce a triage system to prioritize urgent cases during bottlenecks.
- Automate patient feedback collection to identify specific areas of dissatisfaction.

---

## **15. Conclusion**
This project demonstrated the value of data-driven decision-making in healthcare. By analyzing ER data, we identified inefficiencies and proposed actionable steps to improve patient care and satisfaction. The insights and dashboards provide a framework for continuous monitoring and improvement.


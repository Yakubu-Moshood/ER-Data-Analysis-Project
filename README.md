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


### **1. objective**
The purpose of this project is to analyze emergency room (ER) operations, identify trends in patient visits, and propose actionable recommendations to optimize workflows, improve patient satisfaction, and reduce wait times.

---

### **2. Data Source**
The data was sourced from hospital ER logs from April 2003 to October 2024. It contains:
- 9,217 patient records.
- Features include patient demographics, admission details, satisfaction scores, and department referrals.
- The Datasets can be found [here](https://github.com/Yakubu-Moshood/ER-Data-Analysis-Project/blob/08dea7efb1ba65ecd2301c91c6dbea5385e3b8cb/Hospital%20ER_Data%202.csv)

---

### **3. Stages**
The project was executed in the following stages:
1. Data exploration and cleaning.
2. Transformation of data for modeling.
3. Building interactive dashboards.
4. Final analysis and recommendations.

---

### **4. Design**
The project followed a structured design process:
- Data flow was planned from raw files to visual dashboards.
- A calendar table was created to enable data-based analysis
- Power BI dashboards were designed with user-friendly interfaces for quick insights.

---

### **5. Tools**
The following tools were used:
- **Power BI**: For data modeling, dashboards, and visualizations.
- **Power Query**: For data cleaning, transformation, and standardization. 
- **Excel**: For dataset review and minor adjustments.

---

### **6. Process**

#### **Data Exploration**
- Key variables were identified, including demographics, admission times, and satisfaction scores.
- Outliers and missing data were flagged for cleaning.

#### **Data Cleaning**
- Missing or incorrect values (e.g., "Declined to Identify" inpatient race) were handled.
- Standardised date-time formats for admission records.

#### **Transform the Data**
- Categorical variables (e.g., patient gender, race) were encoded.
- Age groups were categorized (e.g., children, adults, seniors).
- Additional columns were added to split the patient admission date into **year*, **month*, **weekday*, **weeknomba*, and time in **hour* 

---

### **7. Visualization**
Dashboard Screenshot![Dashboard image](https://github.com/Yakubu-Moshood/ER-Data-Analysis-Project/blob/c0e3323475926d48524610e29d0259e23e9b8445/The%20Dashboard%20complete.jpg)
Interactive dashboards were created in Power BI, featuring:

#### **a. Key Metrics Cards (Top Section)**
- Displays the total number of visits. It also tracks trends compared to the previous month.

---

#### **b. Line Chart: Patient Visits by Weekday and Gender**
- A line chart displaying visit trends for males (blue) and females (pink) across the days of the week (Sunday to Saturday). This highlights the differences in visit patterns between genders and identifies which days see the highest patient traffic.

---

#### **c. Bar Chart: Patient Visit by Age Range**
- A vertical bar chart breaking down visits into age groups: adults, seniors, and children. It identifies the dominant age group visiting the ER, providing insights for resource allocation based on patient demographics.

---

#### **d. Matrix table: Patient Visits by Day and Time**
- A grid showing the number of visits per hour for each day of the week (Sunday to Saturday). This provides a detailed view of when the ER is busiest, both by specific hours and days of the week.

---

#### **e. Score Rating Table: Patient Race**
- A table displaying racial categories (e.g., African American, Asian, White) along with corresponding satisfaction ratings (e.g., star ratings). It offers insights into satisfaction trends by race, helping identify if specific groups have consistently higher or lower satisfaction levels.

---

#### **f. Horizontal Bar Chart: Avg. Wait Time by Department Referral**
- A bar chart comparing average wait times across various departments (e.g., Physiotherapy, Gastroenterology, Neurology, etc.), highlighting which departments have longer wait times, allowing hospital staff to address bottlenecks or inefficiencies.

The interactive dashboard can be found [here](https://github.com/Yakubu-Moshood/ER-Data-Analysis-Project/blob/c0e3323475926d48524610e29d0259e23e9b8445/EMERGENCY%20ROOM%20ANALYSIS%20INTERACTIVE%20DASHBOARD.pbix)

---

### **8. Results**

#### **DAX Measures**

##### **Key Measures and Their Purpose**

##### **i. Satisfaction Measures**
- **Avg Satisfaction Growth With Arrow**: Indicates the growth in satisfaction score compared to the previous month, with an up or down arrow.
- **Avg Satisfaction Score**: Calculates the average satisfaction score of patients.
- **Avg Satisfaction Score Growth**: Measures the percentage growth or decline in satisfaction scores compared to the previous month.
- **Avg Satisfaction Score Growth Colour**: Determines if satisfaction growth is positive ("Green") or negative ("Red").
- **Avg Satisfaction Score Max Value**: Finds the maximum satisfaction score across all days.
- **Avg Satisfaction Score Min Value**: Finds the minimum satisfaction score across all days.
- **Avg Satisfaction Score Variance**: Calculates the difference between the current month's satisfaction score and the previous month's.
- **PM Avg Satisfaction Score**: Retrieves the previous month's average satisfaction score.

---

##### **ii. Wait Time Measures**
- **Avg Wait Time Growth**: Measures the percentage growth or decline in average wait time compared to the previous month.
- **Avg Wait Time Growth With Arrow**: Displays wait time growth with an up or down arrow indicator.
- **Avg Wait Time Colour**: Determines if wait time growth is positive ("Green") or negative ("Red").
- **Avg Wait Time Max Value**: Finds the maximum wait time across all days.
- **Avg Wait Time Min Value**: Finds the minimum wait time across all days.
- **Avg Wait Time Variance**: Calculates the difference between the current month's average wait time and the previous month's.
- **Avg_Wait_Time**: Calculates the average wait time of patients.
- **PM Avg Wait Time**: Retrieves the previous month's average wait time.

---

##### **iii. Patient Visit Measures**
- **Patient Visit**: Counts the total number of patient visits.
- **Patient Visit Growth**: Measures the percentage growth or decline in patient visits compared to the previous month.
- **Patient Visit Growth Colour**: Determines if patient visit growth is positive ("Green") or negative ("Red").
- **Patient Visit Growth With Arrow**: Displays visit growth with an up or down arrow indicator.
- **Patient Visit Variance**: Calculates the difference between the current month's patient visits and the previous month's.
- **Patient Visits Max Value**: Finds the maximum number of patient visits across all days.
- **Patient Visits Min Value**: Finds the minimum number of patient visits across all days.
- **PM Patient Visit**: Retrieves the previous month's total number of patient visits.

---

##### **iv. Peak Period Measures**
- **Busiest Day**: Identifies the day of the week with the highest number of patient visits.
- **Busiest Time**: Identifies the hour with the highest number of patient visits.

---

##### **v. Other Measures**
- **Score Rating**: Converts the satisfaction score into a visual star rating (e.g., ★).
- **Calendar**: Generates a calendar table with additional columns for year, month, day, weekday, and week type (weekday or weekend).
- **Sat_Score_Param**: Parameter table for satisfaction breakdown by patient race, gender, or age range.

---

The DAX formula for all the above measures is [here](https://github.com/Yakubu-Moshood/ER-Data-Analysis-Project/blob/4fe6de8dd23d39fdd3e25067a4ea8b8b61279e67/DAX%20FORMULAR%20FOR%20ER%20ANALYSIS.txt) 

---

### **Analysis**
#### a. Trends in ER Patient Visits

#### I. What are patient visit peak times (days and hours)?

-![Trends (Hours and Days) Dashboard](https://github.com/Yakubu-Moshood/ER-Data-Analysis-Project/blob/4fe6de8dd23d39fdd3e25067a4ea8b8b61279e67/Time%20Trends%20Peak%20times%20(days%20and%20hours)%20for%20patient%20visits%20to%20the%20ER.png)

- Peak Times: Saturdays at 11:00 PM see the highest traffic, likely reflecting late-night emergencies.
- Observation: Such late-night peaks might reflect emergency incidents or delays in seeking medical care during earlier hours.

---

#### ii. Do patient visit patterns vary by gender, age, or race?

![Visit Pattern by Patient Demographics](https://github.com/Yakubu-Moshood/ER-Data-Analysis-Project/blob/4fe6de8dd23d39fdd3e25067a4ea8b8b61279e67/Patient%20visit%20patterns%20by%20race%2C%20age%20and%20gender.png)

- Patient Visit by Race
White patients (27.92%) form the largest group, followed by African Americans (21.16%), demonstrating inclusivity in patient care.
- Patients Visit by Gender
Male patients slightly outnumber females (4.7K vs. 4.5K), with the balanced gender distribution suggesting possible healthcare patterns worth investigating.
- Patients Visit by Age Group
Adults dominate ER visits with 5,000 visits, followed by seniors (2,200 visits) and children (2,000 visits), highlighting the need to prioritize resources for adults while tailoring care for seniors and children

---

#### iii Are there seasonal or monthly trends affecting ER visits?

![Seasonal/Monthly Trends](https://github.com/Yakubu-Moshood/ER-Data-Analysis-Project/blob/4fe6de8dd23d39fdd3e25067a4ea8b8b61279e67/Seasonal%20Visit%20Pattern.png)

- Peak Months
August (1,021 visits) and June (985 visits) are the busiest months. October (964 visits) and September (935 visits) also experience high volumes.
- Lowest Months
February (428 visits), December (487 visits), and November (464 visits) see the least activity.
- Summer months (June, July, and August) have significantly higher patient volumes, potentially linked to outdoor activities, injuries, or heat-related illnesses. Winter months (December and February) have the lowest visits, likely due to reduced activity levels and fewer external injuries.

---

### b. Wait Times and Satisfaction

![Wait Times and Satisfaction](https://github.com/Yakubu-Moshood/ER-Data-Analysis-Project/blob/4fe6de8dd23d39fdd3e25067a4ea8b8b61279e67/Average%20wait%20time%20and%20satisfaction.png)

#### i. How long do patients wait on average across all visits?

- Average Wait Time
Patients wait around 35 minutes on average across all visits.

#### ii. Which departments have the longest and shortest wait times?

- Longest Waits
Neurology and Physiotherapy report the highest wait times (37 minutes) while General Practice and Renal have the shortest wait times (35 minutes).

#### iii. Is there a relationship between wait times and satisfaction scores?

- Satisfaction Correlation
A negative relationship exists between wait times and satisfaction scores. This is evident from the trend line showing that as wait times increase, satisfaction scores tend to decrease. However, the variation is not extreme, suggesting other factors also contribute to satisfaction.

#### iv. Do wait times differ by patient demographics (e.g., gender, age, or race)?

- Male patients experience slightly longer wait times (35.40 minutes) compared to females (35.11 minutes), though the difference is minimal.
- Children face the highest average wait times at 35.45 minutes, with adults and seniors averaging 35.24 and 35.11 minutes, respectively.
- Among racial groups, Native American/Alaska Native patients have the longest wait times (35.69 minutes), while Pacific Islander patients experience the shortest (34.64 minutes).

### c. Department Referrals
![Department Referrals](https://github.com/Yakubu-Moshood/ER-Data-Analysis-Project/blob/4fe6de8dd23d39fdd3e25067a4ea8b8b61279e67/Department%20referral.png)

#### i. Which departments receive the highest number of referrals?

- Highest Referrals
General Practice (1,834) and Orthopaedics (992) handle the most referrals, which may strain resources.

- Are there any patterns or bottlenecks in specific departments causing delays?
Departments with high volumes may face delays, while those with moderate loads better balance service quality and efficiency as seen in the visuals above.

#### ii. Do satisfaction scores vary by department?

- Satisfaction Scores 
Gastroenterology (5.8) and Neurology (5.3) excel in satisfaction, while Renal (4.6) and Orthopaedics (4.9) show areas for improvement.









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


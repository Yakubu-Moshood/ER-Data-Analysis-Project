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
    - [Create the SQL View](#create-the-sql-view)
    - [Testing](#testing)
        - [Data Quality Tests](#data-quality-tests)
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

### **Create the SQL View**
- A SQL view was created to optimize data queries for Power BI, ensuring efficient load times and accurate reporting.

### **Testing**

#### **Data Quality Tests**
- Duplicates were removed, and column integrity was verified.
- Join keys between datasets were tested to ensure consistency.

---

## **8. Visualization**
Interactive dashboards were created in Power BI, featuring:
- Heatmaps of patient visits by day and hour.
- Bar charts for satisfaction scores and wait times by department.
- Gender and age group distribution.

---

## **9. Results**

### **DAX Measures**
Key measures created using DAX:
- **Average Wait Time**: `Average(WaitTime)`
- **Total Visits**: `Count(PatientID)`
- **Satisfaction Rate**: `Average(SatisfactionScore)`

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


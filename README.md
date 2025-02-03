# **Emergency Room Data Analysis Project**

# Table of Contents

- [1. Objective](#1-objective)
- [2. Data Source](#2-data-source)
- [3. Stages](#3-stages)
- [4. Design](#4-design)
- [5. Tools](#5-tools)
- [6. Process](#6-process)
  - [Data Exploration](#data-exploration)
  - [Data Cleaning](#data-cleaning)
  - [Transform the Data](#transform-the-data)
- [7. Visualization](#7-visualization)
  - [a. Key Metrics Cards (Top Section)](#a-key-metrics-cards-top-section)
  - [b. Line Chart: Patient Visits by Weekday and Gender](#b-line-chart-patient-visits-by-weekday-and-gender)
  - [c. Bar Chart: Patient Visit by Age Range](#c-bar-chart-patient-visit-by-age-range)
  - [d. Matrix Table: Patient Visits by Day and Time](#d-matrix-table-patient-visits-by-day-and-time)
  - [e. Score Rating Table: Patient Race](#e-score-rating-table-patient-race)
  - [f. Horizontal Bar Chart: Avg. Wait Time by Department Referral](#f-horizontal-bar-chart-avg-wait-time-by-department-referral)
- [8. Results](#8-results)
  - [DAX Measures](#dax-measures)
    - [i. Satisfaction Measures](#i-satisfaction-measures)
    - [ii. Wait Time Measures](#ii-wait-time-measures)
    - [iii. Patient Visit Measures](#iii-patient-visit-measures)
    - [iv. Peak Period Measures](#iv-peak-period-measures)
    - [v. Other Measures](#v-other-measures)
- [9. Analysis](#9-analysis)
  - [a. Trends in ER Patient Visits](#a-trends-in-er-patient-visits)
    - [i. What are patient visit peak times (days and hours)?](#i-what-are-patient-visit-peak-times-days-and-hours)
    - [ii. Do patient visit patterns vary by gender, age, or race?](#ii-do-patient-visit-patterns-vary-by-gender-age-or-race)
    - [iii. Are there seasonal or monthly trends affecting ER visits?](#iii-are-there-seasonal-or-monthly-trends-affecting-er-visits)
  - [b. Wait Times and Satisfaction](#b-wait-times-and-satisfaction)
    - [i. How long do patients wait on average across all visits?](#i-how-long-do-patients-wait-on-average-across-all-visits)
    - [ii. Which departments have the longest and shortest wait times?](#ii-which-departments-have-the-longest-and-shortest-wait-times)
    - [iii. Is there a relationship between wait times and satisfaction scores?](#iii-is-there-a-relationship-between-wait-times-and-satisfaction-scores)
    - [iv. Do wait times differ by patient demographics?](#iv-do-wait-times-differ-by-patient-demographics)
  - [c. Department Referrals](#c-department-referrals)
    - [i. Which departments receive the highest number of referrals?](#i-which-departments-receive-the-highest-number-of-referrals)
    - [ii. Do satisfaction scores vary by department?](#ii-do-satisfaction-scores-vary-by-department)
- [10. Discovery](#10-discovery)
  - [Peak Times and Days](#peak-times-and-days)
  - [Demographics](#demographics)
  - [Operational Inefficiencies](#operational-inefficiencies)
  - [Seasonal Planning](#seasonal-planning)
- [11. Recommendations](#11-recommendations)
  - [Staffing Adjustments](#staffing-adjustments)
  - [Process Optimisation](#process-optimisation)
  - [Predictive Modelling](#predictive-modelling)
  - [Cultural Competency](#cultural-competency)
- [12. Conclusion](#12-conclusion)



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

### 9. **Analysis**

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

---

### **10. Discovery**

#### Peak Times and Days: 

- Late-night hours and Saturdays are the busiest periods, indicating a need for increased staffing during these times.

#### Demographics:

- The diverse patient population underscores the need for culturally competent care and communication strategies.

#### Operational Inefficiencies:

- Departments with longer wait times, such as Neurology, require process improvements or additional resources.

#### Seasonal Planning:

- Traffic surges in summer and dips in winter highlight the importance of proactive planning for seasonal variations.**

---

### **11. Recommendations**
Based on these findings, the following recommendations are proposed:

#### Staffing Adjustments:

- Implement a shift-scheduling system to align with peak times.
- Increase staffing during late-night hours, particularly on Saturdays, to handle peak traffic.
- Reallocate staff to high-bottleneck departments like Neurology and Physiotherapy to reduce wait times.

#### Process Optimisation:

- Streamline triaging and patient referral processes to improve throughput in high-wait departments.
- Introduce pre-registration options or self-service kiosks to reduce delays in patient check-ins.
- Introduce a triage system to prioritize urgent cases during bottlenecks.

#### Predictive Modelling:

- Use historical data to develop predictive models for patient flow, enabling better preparation for peak hours and seasonal traffic.
- Automate patient feedback collection to identify specific areas of dissatisfaction.

#### Cultural Competency:

- Train staff to cater to diverse patient populations effectively, ensuring high satisfaction across all demographic groups.

---

### **12. Conclusion**

This project provides a data-driven framework for optimizing Emergency Room (ER) operations at St. Haven, offering critical insights tailored to enhance patient care and operational efficiency. By analyzing key metrics such as patient demographics, visit patterns, wait times, and satisfaction scores, we identified actionable trends such as peak traffic periods (Saturdays at 11 PM) and bottlenecks in high-demand departments like Neurology and Physiotherapy.

The analysis underscores the importance of staffing adjustments during late-night hours and weekends, streamlining department referrals, and prioritizing culturally competent care to meet the needs of a diverse patient population. It also highlights the need to address operational inefficiencies, particularly in high-wait departments, to maintain high patient satisfaction and improve throughput.

With a clear action plan in place, St. Haven Hospital can leverage these insights to allocate resources more effectively, reduce wait times, and enhance patient outcomes. This strategy not only aligns with current patient flow trends but also positions the hospital for sustained operational success and improved care delivery in an increasingly demanding healthcare landscape.


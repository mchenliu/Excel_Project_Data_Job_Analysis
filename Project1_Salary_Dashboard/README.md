# Table of Contents
- [Table of Contents](#table-of-contents)
- [Excel Salary Dashboard](#excel-salary-dashboard)
  - [Introduction](#introduction)
    - [Dashboard File](#dashboard-file)
    - [Excel Skills Used](#excel-skills-used)
    - [Data Jobs Dataset](#data-jobs-dataset)
  - [Conclusion](#conclusion)

# Salary Dashboard
![Dashboard_gif](/Project1_Salary_Dashboard/images/Dashboard_gif1.gif)

## Introduction
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.

The data is from my Excel course, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.

### Dashboard File
:computer: Check out my dashbaord here: [Project1_Salary_Dashboard.xlsx](/Project1_Salary_Dashboard/Project_1_Salary_Dashboard.xlsx)

### Excel Skills Used
The following Excel skills were utilized for analysis:
- **Data Validation**
- **Charts**
- **Formulas and Functions**

### Data Jobs Dataset
- :floppy_disk: **Job titles**
- :dollar: **Salaries**
- :globe_with_meridians: **Locations**
- :book: **Skills**
  
## Dashboard Build

### :one: Data Validation
#### Filtered List
### :two:Charts
#### :book: Data Science Job Salaries - Bar Chart
![Bar_Chart](/Project1_Salary_Dashboard/images/Title%20Bar%20Chart.png)

🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
📉 Data Organization: Sorted job titles by descending salary for improved readability.
💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

#### :globe_with_meridians: Country Median Salaries - Map Chart

![Map_Chart](/Project1_Salary_Dashboard/images/Map_gif.gif)
🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
📊 Data Representation: Plotted median salary for each country with available data.
👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

### :three: Formulas and Functions

#### 💰 Median Salary by Job Titles

```
=MEDIAN(
IF(
(jobs[job_title_short]=A2)*
(jobs[job_country]=country)*
(ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
(jobs[salary_year_avg]<>0),
jobs[salary_year_avg]
))
```
- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

Back-End
![Back_end](/Project1_Salary_Dashboard/images/Title%20Bar%20Chart.png)
Front-End
![Front_end](/Project1_Salary_Dashboard/images/Dashboard_presentation.png)
#### Median Salary by Job Titles
#### Count of Job Schedule Type
## Conclusion

# Salary Dashboard
![Dashboard_gif](/Project1_Salary_Dashboard/images/Dashboard_gif1.gif)

# Table of Contents
- [Salary Dashboard](#salary-dashboard)
- [Table of Contents](#table-of-contents)
- [Introduction](#introduction)
    - [Dashboard File](#dashboard-file)
    - [Excel Skills Used](#excel-skills-used)
    - [Data Science Jobs Dataset](#data-science-jobs-dataset)
  - [Dashboard Build](#dashboard-build)
    - [:one: Data Validation](#onedata-validation)
    - [:two: Charts](#two-charts)
      - [:heavy\_dollar\_sign: Bar Chart - Data Science Job Salaries](#heavy_dollar_sign-bar-chart---data-science-job-salaries)
      - [:globe\_with\_meridians: Map Chart - Country Median Salaries](#globe_with_meridians-map-chart---country-median-salaries)
    - [:three: Formulas and Functions](#threeformulas-and-functions)
      - [:heavy\_dollar\_sign: Median Salary by Job Titles](#heavy_dollar_sign-median-salary-by-job-titles)
      - [:heavy\_plus\_sign: Count of Job Schedule Type](#heavy_plus_sign-count-of-job-schedule-type)
- [Conclusion](#conclusion)
- [What I Learned](#what-i-learned)

# Introduction
This data jobs salary dashboard was created following Luke Barousse's Youtube [tutorial](https://www.youtube.com/watch?v=pCJ15nGFgVg). This dashboard is created to filter out job listings by title, country and work type.

Dataset used in this project is from Luke's [Github](https://github.com/lukebarousse/Excel_Data_Analytics_Course/tree/main). The data contains real-world job listing from 2023, providing information on titles, salaries, locations, and job listing platforms.

### Dashboard File
:computer: Check out my dashbaord here: [Project1_Salary_Dashboard.xlsx](/Project1_Salary_Dashboard/Project_1_Salary_Dashboard.xlsx)

### Excel Skills Used
The following Excel skills were utilized for analysis:
- :lock: **Data Validation**
- :chart: **Charts**
- :izakaya_lantern: **Formulas and Functions**

### Data Science Jobs Dataset
Information retrieved from dataset for this project are:

- :floppy_disk: **Job titles**
- :heavy_dollar_sign: **Salaries**
- :globe_with_meridians: **Locations**
- :rocket: **Skills**
  
## Dashboard Build

### :one: Data Validation

Data validation is implemented to prevent user entry errors and enhance overall dashboard user experience.

![Data_validation](/Project1_Salary_Dashboard/images/Data_validation_gif.gif)

### :two: Charts
#### :heavy_dollar_sign: Bar Chart - Data Science Job Salaries

- **Excel Features:** Bar chart is used to optimize layout for clarity.
- **Design Choice:** Horizontal bar chart to easily compare median salaries.
- **Data Organization:** Job titles sorted by descending salary for better readability.
- **Insights:** Clear salary trends— Senior roles and Engineers earn more than Analysts.

![Bar_Chart](/Project1_Salary_Dashboard/images/Title%20Bar%20Chart.png)



#### :globe_with_meridians: Map Chart - Country Median Salaries 


- **Excel Features:** Map chart is used to plot median salaries around the globe.
- **Design Choice:** Salary level by region is color-coded on the map for clear visualization.
- **Data Representation**: Median salary per country is plotted subject to data availibility.
- **Visual Enhancement**: Enhanced readability for quick geographic salary trends.
- **Insights**: Regions with highl/low salary are instantly highlighted.

![Map_Chart](/Project1_Salary_Dashboard/images/Map_gif.gif)

### :three: Formulas and Functions

#### :heavy_dollar_sign: Median Salary by Job Titles

Formula used:
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

- **Formula Result:** Returns salary median based on job_title, country,and schedule_type.
- **Data Cleaning:** Used a combination of funcations (`MEDIAN()` and multiple `IF()`s) to find median of salaries that is not 0.
- **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
  
![Back_end_1](/Project1_Salary_Dashboard/images/Title%20Bar%20Chart.png)  
*Back-end table*  


![Front_end_1](/Project1_Salary_Dashboard/images/Dashboard_presentation.png)  
*Front-end Dashboard* 


#### :heavy_plus_sign: Count of Job Schedule Type

Formula used:
```
=FILTER(K2#,(NOT(ISNUMBER(SEARCH("and",K2#))+ISNUMBER(SEARCH(",",K2#))))*(K2#<>0))
```
- **Formula Result:** Returns unique job schedule_type.
- **Data Cleaning:** Used a combination of functions()`FILTER()`,`SERACH()` and `ISNUMBER()` to exclude repetitive job types and 0 from source data.


![Bakc_end_2](/Project1_Salary_Dashboard/images/Back_end_2.png)  
*Back-end table* 
  

![Front_end_2](/Project1_Salary_Dashboard/images/Dashboard_presentation_2.png)  
*Front-end Dashboard* 

# Conclusion
This dashboard provides comprehensive insights into salary trends across various pay scales, categorized by job titles within the data industry. The color-coded map delivers an immediate visualization of median salary levels, highlighting high and low ranges for the selected country.

# What I Learned
- **:shower: Utilise formula combinitations to clean data:** I picked a more efficient and flawless way to clean data through this tutorial which I expect myself to implement on my future work.
- **:musical_keyboard: Keyboard shortcuts:** Picked up some keyboard short cuts which is always a bonus to leanr.
- **:mortar_board: Miscellaneous:** Excel tips and knowledge.
- **:bulb: Add GIFs:** Adding GIFs to my Github README makes my project fun to look at. Moreover, it prodives visual demo of features presented in projects. Viewers can instantly understand without needing to read through paragraphs of documentations. I will incoporate GIFs in my future projects.
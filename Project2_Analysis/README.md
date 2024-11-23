![Banner](/Project2_Analysis/images/P2_banner.jpg)  
*Image by <a href="https://pixabay.com/users/tungnguyen0905-17946924/?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=7111798">Tung Nguyen</a> from <a href="https://pixabay.com//?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=7111798">Pixabay</a>*  

# Table of Contents
- [Table of Contents](#table-of-contents)
- [Introduction](#introduction)
- [:one: Do more skills bring more money in Data Science?](#onedo-more-skills-bring-more-money-in-data-science)
  - [:hammer: Skill: Power Query to ETL](#hammer-skill-power-query-to-etl)
  - [:computer: Analysis](#computer-analysis)
- [:two: What’s the salary for data jobs in different countries?](#twowhats-the-salary-for-data-jobs-in-different-countries)
  - [:hammer: Skills:  Pivot Tables \& DAX](#hammer-skills--pivot-tables--dax)
  - [:computer: Analysis](#computer-analysis-1)
- [:three: What are the top Skills in Data Science?](#threewhat-are-the-top-skills-in-data-science)
  - [:hammer: Skill: Power Pivot](#hammer-skill-power-pivot)
  - [:computer: Analysis](#computer-analysis-2)
- [:four: What's the pay of the top 10 skills?](#fourwhats-the-pay-of-the-top-10-skills)
  - [:hammer: Skill: Pivot Charts](#hammer-skill-pivot-charts)
  - [:computer: Analysis](#computer-analysis-3)
- [Conclusion](#conclusion)
- [What I Learned](#what-i-learned)

# Introduction
Following the [salary dashboard](https://github.com/mchenliu/Excel_Project_Data_Job_Analysis/tree/main/Project1_Salary_Dashboard) from project one, this project dives further into the job posting data and analyze the relationship betwee skills required and salary for data science roles.

**Questions to Analyze**  
The questions I wanted to answer through my project are:

1. Do more skills bring more money in Data Science?
2. What’s the salary for data jobs in different countries?
3. What are the top Skills in Data Science?
4. What’s the pay for the top 10 skills?
   
**Excel Skills Used**  
I utilized these Excel for analysis:
- Pivot Tables
- Pivot Charts
- Power Query
- Power Pivot
- DAX (Data Analysis Expression)

**Data Jobs Dataset**  
Dataset used in this project is from Luke's [Github](https://github.com/lukebarousse/Excel_Data_Analytics_Course/tree/main). The data contains real-world job listing from 2023, providing information on titles, salaries, locations, and job listing platforms.
# :one: Do more skills bring more money in Data Science?  
## :hammer: Skill: Power Query to ETL
**:arrow_down: Extract**  
First was to create two queries from source date `data_salary_all.xlsx`:  
  - The first one has all job listing information.
  - The second one has skills that are associated with each job ID.  

**:arrows_clockwise: Transform**  
Then I transformed two queries through modifying column types, removing unwanted columns, removing specific words, trimming whitespace and unpivoting columns.  

*Transform steps for query one*  
![Transform1](/Project2_Analysis/images/Transform1.png)  

*Transform steps for query two*  
![Transform2](/Project2_Analysis/images/Transform2.png)  

**:arrow_up: Load**  
Lastly, I loaded these two transformed queries into the workbook to prepare for futher analysis.  
*Query 1*
![Query1](/Project2_Analysis/images/Query1.png)  
*Query 2*
![Query2](/Project2_Analysis/images/Query2.png)  

## :computer: Analysis  
- There is a positive correlation between the number of required skills and tthe median salary, especially for Data Scientist and Senior Data Engineer.  
   
- Roles with less skills requirements (e.g., Business Analyst and Data Analyst) have the least salaries. This indicates that more skill sets are rewarded by the market.  

# :two: What’s the salary for data jobs in different countries?
## :hammer: Skills:  Pivot Tables & DAX  

**:trident: DAX**    
I used DAX to find median yearly salary for non United States jobs.  

```
Median Salary Not US:=CALCULATE([Median Salary],data_jobs_salary[job_country]<>"United States")
```  
**:snowflake: Pivot Table**
- I used Power Pivot to create the Data Model for the salary by country Pivot Table.  
- Then added new measure to calculate the median salary for Unitied States jobs.  
```
=CALCULATE([Median Salary],data_jobs_salary[job_country]="United States")
```
- Lastly, I put together a Pivot Table to refine salary median comparison between jobs listed in United States and outside of United States. A slicer that connects to other Pivot Tables in this workbook is added for a even closed up analysis.

*Salary by country*  
![Salary_Country](/Project2_Analysis/images/Salary_Country.png)

## :computer: Analysis

- Senior and engineer positions tend to provide higher median accross the world.
- Austrlia tend to offer higher salary for most data roles comparing to the United States.

# :three: What are the top Skills in Data Science?
## :hammer: Skill: Power Pivot  
**Power Pivot**  
- Because I've cleaned the data with Power Query previously, I proceeded to  Data Model and connected table `data_jobs_all` with table `data_jobs_skills`.  
  
**Data Model**  
- I established a many to one relasionship between the two tables via `job_id` column.  
*Diagram*  
![Diagram](/Project2_Analysis/images/Diagram.png)  


## :computer: Analysis  
- For data analysts, SQL and Excel are the most demanded skils across majority of the world.
- The high ranking of Python, R, Tableau and Power BI shows programming langauges and visualization tools are highly favoured by the market.  
  
*Top skills required for Data Analyst in Australia*
![Top_Skills](/Project2_Analysis/images/Top_skills.png)
# :four: What's the pay of the top 10 skills?
## :hammer: Skill: Pivot Charts  
- I created a combo table Pivot Chart to presenting both median salary and skill likelihood(%). 
- The primary axis is the salary medain (clusterd bars) 
- The secondary axis is skill likelihhood (line with built in markers).
- A slicer is added for drilling down to top paid skills by roles. 
## :computer: Analysis  
- Skills like SQL, Python, Oracle and Tableau are high in both median salary and job likelihood. This indicates their high demand and high return in the market.
- Skills like Powerpoint and Word are low in both salary and likelihood. This suggests they are not specialization skills demanded in data science field.  

*Top paid skills for data analysts*  
![Top_paid_skills](/Project2_Analysis/images/Top_paid_skills.png)
# Conclusion  
This project provides valuable insights into the data science job market, highlighting key trends and correlations. It demonstrates a positive relationship between the number of skills listed and the salary offered, though certain roles, such as data scientist, may deviate from this pattern. Additionally, it outlines the median salaries across various countries. Notably, skills like Python, SQL, and cloud computing platforms are in high demand, offering substantial returns in the competitive data science field. 
# What I Learned
- Sharpened my knowledge on analysis add-ins and Toolpak in Excel.
- Performed ETL with Power Query.
- Advanced visualization with Pivot Charts and Power Pivot.
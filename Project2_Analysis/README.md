![Banner](/Project2_Analysis/images/P2_banner.jpg)  
*Image by <a href="https://pixabay.com/users/tungnguyen0905-17946924/?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=7111798">Tung Nguyen</a> from <a href="https://pixabay.com//?utm_source=link-attribution&utm_medium=referral&utm_campaign=image&utm_content=7111798">Pixabay</a>*  

# Table of Contents
- [Table of Contents](#table-of-contents)
- [Introduction](#introduction)
  - [Questions to Analyze](#questions-to-analyze)
  - [Excel Skills Used](#excel-skills-used)
  - [Data Jobs Dataset](#data-jobs-dataset)
- [:one: Do more skills bring more money in Data Science?](#onedo-more-skills-bring-more-money-in-data-science)
  - [:hammer: Skill: Power Query to ETL](#hammer-skill-power-query-to-etl)
    - [Extract](#extract)
    - [Transform](#transform)
    - [Load](#load)
  - [:computer: Analysis:](#computer-analysis)
- [:two: What’s the salary for data jobs in different regions?](#twowhats-the-salary-for-data-jobs-in-different-regions)
  - [:hammer: Skills:  Pivot Tables \& DAX](#hammer-skills--pivot-tables--dax)
  - [:computer: Analysis:](#computer-analysis-1)
- [:three: What are the top skills of data professionals?](#threewhat-are-the-top-skills-of-data-professionals)
  - [:hammer: Skill: Power Pivot](#hammer-skill-power-pivot)
  - [:computer: Analysis](#computer-analysis-2)
- [:four: What’s the pay of the top 10 skills?](#fourwhats-the-pay-of-the-top-10-skills)
  - [:hammer: Skill: Pivot Charts](#hammer-skill-pivot-charts)
  - [:computer: Analysis](#computer-analysis-3)
- [Conclusion](#conclusion)
- [What I Learned](#what-i-learned)

# Introduction
Following the [salary dashboard](https://github.com/mchenliu/Excel_Project_Data_Job_Analysis/tree/main/Project1_Salary_Dashboard) from project one, this project dives further into the job posting data and analyze the relationship betwee skills required and salary for data science roles.

## Questions to Analyze
The questions I wanted to answer through my project are:

1. Do more skills bring more money in Data Science?
2. What’s the salary for data jobs in different countries?
3. What are the top skills of data professionals?
4. What’s the pay for the top 10 skills?
   
## Excel Skills Used

I utilized these Excel for analysis:
- Pivot Tables
- Pivot Charts
- Power Query
- Power Pivot
- DAX (Data Analysis Expression)

## Data Jobs Dataset
Dataset used in this project is from Luke's [Github](https://github.com/lukebarousse/Excel_Data_Analytics_Course/tree/main). The data contains real-world job listing from 2023, providing information on titles, salaries, locations, and job listing platforms.
# :one: Do more skills bring more money in Data Science?  
## :hammer: Skill: Power Query to ETL
### Extract  

First was to create two queries from source date `data_salary_all.xlsx`:  
  - The first one has all job listing information.
  - The second one has skills associated with each job ID.  
  

*Query 1*
![Query1](/Project2_Analysis/images/Query1.png)  
*Query 2*
![Query2](/Project2_Analysis/images/Query2.png)  

### Transform
Then I transformed two queries through modifying column types, removing unwanted columns, removing specific words, trimming whitespace and unpivoting columns.    

### Load
Lastly, I loaded these two transformed queries into the workbook to prepare for futher analysis.
## :computer: Analysis:
# :two: What’s the salary for data jobs in different regions?
## :hammer: Skills:  Pivot Tables & DAX
## :computer: Analysis:
# :three: What are the top skills of data professionals?
## :hammer: Skill: Power Pivot  
## :computer: Analysis
# :four: What’s the pay of the top 10 skills?
## :hammer: Skill: Pivot Charts  
## :computer: Analysis
# Conclusion
# What I Learned
- Enable analysis add-ins in excel
- What-If Analysis (Scenario manager & Goal Seeker)
- Power Query
- Power Pivot
- DAX
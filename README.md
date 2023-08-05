# **EMPLOYEE TURNOVER RATE**
------
![overview](https://blog.jostle.me/hubfs/Google%20Drive%20Integration/How%20your%20employee%20turnover%20rate%20impacts%20your%20business.png)

# Table of Contents:
- [Introduction](#introduction)
- [About Dataset](#about-dataset)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [Data Analysis](#data-analysis)
  - [Overview Dashboard](#overview-dashboard)
  - [Personal Information](#personal-information)
  - [Nature of Job](#nature-of-job)
  - [Benefits](#benefits)
  - [Satisfaction](#satisfaction)
- [Recommendation](#recommendation)
  - [Insights](#insights)
  - [Recommendation](#recommendation)
-------

# Introduction

High turnover rates have become a problematic issue of a business
since it reduces productivity, increases time spent recruiting, training, and onboarding new employees, etc.


**What are the causes?**


Most people do not start and end their careers at one company, they change jobs several times to find more opportunities to develop their professions.


Or the company that they currently work impacts negatively on them. 
For example, poor benefits, conflicts with managers, culture of working overtime, toxic work environment, etc.

In this project, I am going to analyze some factors that could impact on the turnover rate and suggest some measures to tackle this issue. 


-------

# About Dataset

The dataset was created to predict left rate at a company based on information below:
* Personal information (age, gender, marital status, education level, major, etc.)
* Nature of Job
* Benefits
* Factors related to satisfaction

Name of the dataset: IBM HR Analytics Employee Attrition & Performance

Format of the dataset: csv

Source: Kaggle

Link: https://www.kaggle.com/datasets/whenamancodes/hr-employee-attrition 


-------


# Tools

## Data cleaning ##
- Python
- MySQL

## Data visualization ##
- Power BI


-------

# Data Cleaning
## Python ##
1. Import data into Python.
2. Check and drop null.
3. Remove irrelevant columns: Over18, StandardHour, EmployeeCount.
4. Export file .csv.

## MySQL ##
1. Import a file that had just exported from Python.
2. Compare with a dataset to transform data.
3. Transform data from numeric into string, use **CASE WHEN** to operate it: Education, EnvironmentSatisfaction, JobLevel, JobInvolvement, JobSatisfaction, Performance, WorkLifeBalance.

## Clean Dataset ##
[hr_employee_attrition_transform.csv](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/hr_attrition_transform.csv) 


-------

# Data Analysis #

## Overview Dashboard ##
![overview dashboard](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Overview%20Dashboard.png)


## Personal Information ##

### Age ###

**Whether the majority of left employees come from the young age group?** 

![age](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Age.png)

- The chart shows that young adults who are under 30 tend to leave a company than older employees.
- Perhaps the young expect to find more opportunities in labour market, while the senior prefer a stable job.

### Marital Status ###

**Does marital status impact on the decision to stay at a company?**

![marital stt](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Marital%20Status.png) 

- The above graph presents the number of attrition 3 groups of marital status.
- It can be seen that single employees are likely to leave than other groups.
  They may be available to change their jobs as they do not have to be worried about financial burden.
- While the married group has to stay longer since they need income to cover family expenses.
- The divorced has the same situation as the married in case they have children.

### Distance From Home ###

**Whether employees who live far from company are more likely to quit**

![distance](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Distance.png) 

- The distance is one of a factor that employees consider when making decisions to leave.
- The chart clearly shows that people who live far from company about 10km away are more likely to quit.


### Education Level ###

**The higher the education level is, the more likely an employee leaves.**

![education](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Education%20Level.png) 

- "Below College" and "Bachelor" are the top 2 education levels which have high turnover rate - more than 16%.
- Employees who are at these levels may expect to learn more or to look for better job opportunities in the labor market.

## Nature of Job ##

![department](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Department.png) 

**Consider 3 departments in a company. Analyze some factors of each department to see the difference.** 

**Overall, Sales department has the noticeable turnover rate than the others.**

### Job Level ###

- The job level at this company is ranged from 1 to 5.
- It can be seen that employees who have lower levels tend to leave than higher ones - more than 26% leave at level 1.  

![job level overall](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Job%20Level%20Overall.png)

- Resignation occurs in R&D and Sales department at all levels. Level 1 is has the higher left rate compared to others.
- Turnover rate in Sales Department needs to be noticed as all levels have more than 10% left employees. About nearly a half of level 1 decides to leave.
- While in HR Department, there are only level 1 and 3 having exit employees. However, the rate is considerably high, about 30% for each level.
 
![job level](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Job%20Level.png) 

### Business Travel ###

- There are 3 types of Business Travel frequencies: Travel Frequently, Travel Rarely and Non Travel.
- Overal, most employees leave a company since they always have to take business travel (nearly 25%).

![business travel overall](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/BusinessTravel%20Overall.png)


- According to 3 charts below, R&D and Sales Department have left employees no matter how often they travel. While HR employees leave when they have to take business travel, the ones who do not would stay.
- R&D Department has the turnover rate relatively low compared to others.

  
![business travel](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/BusinessTravel.png) 

### Work Overtime ###

- Whether an employee has to work overtime or not.
- It is obviously seen that employees who work overtime leave a company.

![overtime overall](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Overtime%20Overall.png) 

- The number of left employees who have to work overtime is high among 3 departments (over 27%).
- Even though some employees do not stay at work overtime, they still decide to quit (range from 8% to 15%).

![overtime](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Overtime.png) 

### Work Life Balance ###

- There are 4 levels of balancing work and life: Bad, Good, Better and Best.

![wlb overall](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/WLB%20overall.png) 

- Generally speaking, employees who cannot balance work and life (Bad) would feel stress and then they quit (31%).
- The other 3 levels seem low, however many employees consider as "Best" still leave (nearly 18%).

![wlb](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/WLB.png) 

- It is noticably seen that in HR Department, "Bad" level has no left employees.
- The other departments have high rate at the same level (over 31%).


## Benefits ##

### Monthly Income ###
**Does lower salary impact on the decision to leave of an employee?**

#### Average Income of 3 Departments ####
**Consider average monthly income in 3 departments.**
- The gap of average monthly income between 3 departments is not huge (from 6300 to 7000).
- It can be seen from the chart that the turnover rate is not impacted by income as Sales has the highest salary and its left rate also remains high.

![avg income dept](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Avg%20Income%20in%20Departments.png) 

#### Average Income of 5 Job Levels ####
**Consider average monthly income of 5 job levels.**
- The higher the job level is, the higher monthly income is earned.
- Level 1 and 3 stays at the top turnover rate, 26% and 15% respectively. 

![avg income job level](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Avg%20Income%20of%20Job%20Levels.png) 


### Years Since Last Promotion ###
**Will an employee quit if he/she has not been promoted for a long time?**

- It seems true as many employees who have worked for a long time (over 6 years) but have not promoted decide to leave a company (about 18% to 24%)

![yrs promotion](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Years%20Since%20Last%20Promotion.png) 

### Percent Salary Hike ###
**May low bonus affect on high turnover rate?**

- It can be seen that whether an employee has their salary increased or not, they still quit.


![percent hike](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Percent%20Salary%20Hike.png) 


## Satisfaction ##

### Environment Satisfaction ###

**Do employees feeling bad at work environment tend to quit?**

- The chart clearly shows that the lower the satisfaction rate is, the higher the left rate becomes (Bad - 25%).

![environment](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Environment.png) 


### Years At Company ###
**Would employees lose their interests when they have worked there for a long time?**

- According to the chart, the left rate decreases when an employee works for more than 2 years.
- While newbies are more likely to quit than others (nearly 30%).

![yrs comp](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Years%20At%20Company.png) 

### Job Satisfaction ### 

**Are employees satisfied with their jobs?**

- About 23% of employees who are not happy with their job decide to quit.
- The gap between "Medium" and "High" is not significant.

![job](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Job%20Satisfaction.png) 

### Job Involvement ###
**Would employees who show strong connection with their job stay longer?**

- This feature presents the same feature as that of "Job Satisfaction".
- "Low" has the highest turnover rate (about 34%).
- "Best" is nearly 4 times lower than that of "Low" (9%).

![job involvement](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Job%20Involvement.png) 



### Years With Current Manager ###
**Employees who work with current managers for a short time, would they leave since they have conflict with managers? **

- Newbies who work with managers for less than 2 years, they are likely to leave (21%) than others who work for more than 5 years (under 15%).

![yrs manager](https://github.com/lh-elaitch0731/hr_employee_attrition/blob/main/Visualization/Years%20With%20Curr%20Manager.png)



-------

# Recommendation #

## Insights ##
- It can be seen that most employees leave a company to find better job opportunities in labor market to not only establish their job career but also earn higher income (related to Personal Information and Benefits).
- Another reason is that they are not happy with a work environment and feel stress with work flow (related to Nature of Job and Satisfaction).


## Recommendation ##

- A company should offer benefits to retent talented employees. Furthermore, they should suggest and support employees to grow their careers.
- Salary scales should be adjusted appropriately to job levels.
- A company should create a flexible and comfortable work environment. For example, hybrid work, job sharing, unlimited timeoff, etc.
  Thus, it would not make employees feel stress when they are at work.
- Managers ought to support newbies as they are not familiar with a company culture and professions.

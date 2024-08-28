# HR Analytics Dashboard Using Power BI

## **Project Name :** 
HR Analytics: A Complete Employee Data Analysis Project using Power BI Dashboard


## **OBJECTIVES :** 
This Power BI HR analytics enables the HR manager and business leaders with comprehensive insights into analyzing and monitoring employee data to make informed decisions on employee retention, development, and recruitments.

It also comprises a trendline and target line to help the Human Resource manager track the progress towards reduction in attrition. It plots, with the help of charts, the distribution of employees and attrition rate on the basis of gender, age group, job satisfaction, and field of education. Legends and filters have also been added to the chart to let the human resource manager drill down into further detail.

In the project, I had a chance to : 
* Dive deep into HR data through deciphering and extracting useful information from it.
* Create interactive visualization dashboards for key HR metrics.
* Provide data-driven recommendations to aid in strategic decision-making.

## **TECHNOLOGIES USED:**
```
Advanced Excel 👨‍💻
Power BI 📊
```

## **DATASET :** 
The Dataset used for this project was in the form of a raw CSV file that contained 38 columns and approximately 1.48k rows. It controlled information on employee demographics, work roles, salaries and tenure, among many subjects.

Download the dataset from here 


## **STEPS FOLLOWED :**

**1. Data Gathering:**

Import the raw data .csv file in Power BI and then transform it to the Power Query editor for cleaning and processing the data. Also, created a copy of the dataset in excel for security purpose. 


**2. Cleaning of Data:**

Cleaned by removing the empty column, removal of duplicates, errors, etc.
Replaced values in column with proper values and naming.
Detection of data type of every column using auto detect data type function in Power query editor.


**3. Data Processing:**

In Power Query editor, create a new column "AttritionCount" using conditional column feature in Add Column, created based on some condition like if attrition = 'Yes' then 1 Else 0.
This is further used to create different KPI's and charts. Then we have created 7 new measures using DAX Quries as follows :
```
Employee_Count = DISTINCTCOUNT(HR_Analytics[EmpID])
Employee_Attrition = CALCULATE([Employee_Count],HR_Analytics[Attrition]="Yes")
Avg_Years_atCompany = AVERAGE(HR_Analytics[YearsAtCompany])
Years_With_Text = ROUND([Avg_Years_atCompany],0)&" Years"
Attrition% = [Employee_Attrition]/[Employee_Count]
Avg_Salary = AVERAGE(HR_Analytics[MonthlyIncome])
Avg_Age = AVERAGE(HR_Analytics[Age])
```

**4. Analysis of Data:**

This analysis will involve the creation of different displays like bar charts, KPIs, table charts, pie charts, and all other relevant visuals.
I identified, at the start of the analysis, some KPIs that were needed to track and monitor employee performance and attrition. The following KPIs have been developed in Power BI on the basis of card visualizations:
* Employee count
* Attrition
* Attrition rate
* Average age
* Average income
* Average tenure


## **KEY QUESTIONS:**
```
What is the Total Employee Count ?
What is the employee's Average Age?
What is the employee's Average Salary?
What is the Attrition Count of men and women at the company?
What is average employees working years at the Company ?
Which Department has maximum employee ?
What is the Gender distribution ?
```


## **LEARNINGS :**
* Used DAX queries to calculate multiple measures like total employees, attrition percentage, average salary and age, etc. 
* I have used several charts and visualizations to gain insights into the employee data. Key insights derived through the analysis of the charts are as follows:
1. Area Chart
2. Clustered Column Chart
3. Donut Chart
4. Slicer
5. Cards to calculate KPIs (Key Performing Indicators) 


## **KEY INSIGHTS :**

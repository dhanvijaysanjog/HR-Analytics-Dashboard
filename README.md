# HR Analytics Dashboard Using Power BI

## **Project Name :** 
HR Analytics: A Complete Employee Data Analysis Project using Power BI Dashboard


![alt text](https://github.com/dhanvijaysanjog/HR-Analytics-Dashboard-/blob/main/HR%20Analytics.png "Logo Title Text 1")




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

[Download the dataset from here](https://github.com/dhanvijaysanjog/HR-Analytics-Dashboard-/blob/main/HR_Analytics%20Dataset.csv)



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

* Total Employees: The organization has grown extensively, with the current strength being 1470 employees. This implies that the organization has grown significantly and has scaled up largely.
* Attrition Analysis: An overall of 237 employees have quit the organization. Out of these, 150 were males, and 87 were females. This means that more males than females quit the organization.
* An industry-wise impact: Life Sciences had the highest rate of attrition, which reflects that the retention challenge is pronounced in this particular sector.
* Job role affected: Sales had the maximum rate of attrition, proving that retention efforts have to be focused on all the sales department to reduce turnover.



## **FINAL DASHBOARD :**
![alt text](https://github.com/dhanvijaysanjog/HR-Analytics-Dashboard-/blob/main/HR%20Analytics%20Dashboard.png "Logo Title Text 1")




## **CONCLUSION :**
The HR analytics dashboard depicted a critical view of employees for deriving better insights to make decisions that may keep the employees happy and continue working in the organization. The human resource department may take certain actions to mitigate the problem faced by the employees and build a positive working environment which may lead to better performance and longer retention of employees, helping an organization to generate more revenue and become successful.

For any feedback, feel free to contact me at dhanvijaysanjog@gmail.com

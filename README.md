# HR Attrition & Hiring Cost Dashboard | Power BI

## 📊 Overview
Analyzed 185 employees to track attrition patterns and the business cost of employee turnover. 
Dashboard shows $600K total hiring cost to replace 40 employees.

## 🎯 Business Problem
HR needed answers:
- How many employees left and what is the attrition rate?
- Which department has highest attrition?
- Which recruitment source fails most?
- Why are people leaving?
- What is the total hiring cost?

## 💡 Key Insights
- **Total Employees:** 185 | **Active:** 145 | **Attrition:** 40 (22%)
- **Total Hiring Cost:** $600K (Avg $15K per replacement)
- **Highest Attrition Department:** Sales (14) > Finance (12)
- **Top Recruitment Source for Attrition:** LinkedIn (30%)
- **Top Reason for Leaving:** Better Salary (12)

## 🛠️ Tools Used
- Power BI Desktop
- DAX (Measures for Attrition Rate, Total Hiring Cost)
- Data Modeling (Dim_Employee, Fact_Attrition)

## 📸 Dashboard

![Dashboard](HR_Dashboard.png)

## 📂 Files
- HR_Analytics.pbix - Power BI file
- HR_Dashboard.png - Dashboard screenshot

## 🔧 Measures Created
- Attrition Count = COUNT(Fact_Attrition)
- Attrition Rate = Attrition / Total Employees
- Total Hiring Cost = SUM(ReplacementCost)

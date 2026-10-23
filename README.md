# HR Attrition & Hiring Cost Dashboard | Power BI

### Overview
Power BI dashboard built to monitor employee attrition and hiring costs. Helps HR teams understand why employees leave and where to improve retention.

Built for HR Analytics portfolio - Hamilton / GTA hiring.

### Dashboard Preview
![HR Attrition Dashboard](HR%20Attrition%20and%20Hiring%20Cost.png)

### KPIs - Executive Summary
- **Total Employees: 185**
- **Active Employees: 145**
- **Attrition Count: 40**
- **Attrition Rate: 22%**
- **Total Hiring Cost: $600K**

### Key Insights
- **Attrition Rate is 22% (40 out of 185)** - High risk area for HR
- **Sales department has highest attrition** - Followed by Finance and Operations
- **Top Reason for Leaving: Better Salary (15 cases)** - Compensation review needed
- **Manager Issue is #2 reason (8 cases)** - Leadership training required
- **Attrition by Recruitment Source:** Campus and Indeed have higher attrition vs Referral and LinkedIn
- **Work-Life Balance, Relocation, Health Issues** also contribute

### Visuals Breakdown
- **KPI Cards (Top):** Total 185, Active 145, Attrition 40, Rate 22%, Cost $600K
- **Attrition by Department:** Bar chart - Sales highest, HR lowest
- **Attrition by Recruitment Source:** Donut chart (40 total) - Breakdown by LinkedIn, Referral, Campus, Indeed
- **Reason for Leaving:** Horizontal bar - Better Salary (15), Manager Issue (8), Career Growth (7), Work-Life Balance (4)

### Tools & DAX Used
- **Power BI Desktop**
- **DAX Measures:**
    - `Total_Employees = COUNT(EmployeeID)`
    - `Attrition_Count = COUNTROWS(FILTER(HR_Table, Attrition="Yes"))`
    - `Attrition_Rate = DIVIDE([Attrition_Count], [Total_Employees])`
    - `Total_Hiring_Cost = SUM(Hiring_Cost)`
    - `Active_Employees = [Total_Employees] - [Attrition_Count]`
- **Data Source:** HR Analytics dataset (185 employees) - 3 Excel tables combined
    - `Fact_Employees (185 rows)` - EmpID, Dept, Salary, Attrition
    - `Dim_Department (5 rows)` - DeptID, DeptName
    - `Fact_Attrition_Log (40 rows)` - Reason, Hiring Cost, Recruitment Source
- **Data Cleaning:** Power Query only (Type fixes, Trim) - No Python cleaning

### Files
- `HR_Data_3_Tables.xlsx` - Source Excel file with 3 sheets (185 employees) - **Main Data Source**
- `HR_Analytics.pbix` - Main Power BI file
- `HR Attrition and Hiring Cost.png` - Dashboard screenshot

### Business Impact
This dashboard helps HR reduce $600K hiring cost by focusing on:
1. **Retaining Sales team** - Highest attrition department
2. **Reviewing Salary Structure** - #1 reason for leaving
3. **Manager Training** - #2 reason for leaving
4. **Improving Recruitment Source Quality** - Campus/Indeed vs Referral

Potential saving: Reduce attrition from 22% to 15% = Save ~$180K in hiring costs.

### Author
**Gloris Prema - Aspiring Data Analyst | Hamilton, ON**
- Focus: HR Analytics, Power BI, Workforce Planning



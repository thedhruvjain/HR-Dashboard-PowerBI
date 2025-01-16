# HR-Dashboard-PowerBI

## Project Overview
This project involves the creation of an interactive HR Dashboard using Power BI. The objective was to analyze and visualize various aspects of employee data to gain insights into staff distribution, salary trends, leave balances, and more. The dataset used for this project is `Hr-Data.xlsx`, which contains information about employees, including their job title, gender, education, salary, and leave balance.

### Dataset
The dataset `Hr-Data.xlsx` contains the following columns:
- **Name**: Name of the employee
- **EmpID**: Employee ID
- **Gender**: Gender of the employee
- **Education Qualification**: Education qualification of the employee
- **Date of Join**: Date when the employee joined the company
- **Job Title**: Employee's job title
- **Salary**: Employee's salary
- **Age**: Employee's age
- **Leave Balance**: Employee's remaining leave balance

---

## Power BI Steps & Insights

### 1. **Staff Headcount by Job Title**
   - Created a measure `Total Headcount = COUNTROWS(staff)` and visualized it using a bar chart.
   - X-axis: Job Title
   - Y-axis: Total Headcount

### 2. **Gender Breakdown of the Staff**
   - Created a pie chart to visualize the gender distribution.
   - Values: Total Headcount
   - Legend: Gender
   - Added slicer by Job Title.

### 3. **Age Distribution of the Staff**
   - Age was classified into groups of 5 years using the "Bin Size" feature.
   - Visualized the age spread using a stacked column chart with gender as the legend.
   - Used small multiples to display age groups by gender.

### 4. **Salary by Job Title**
   - Created three new measures: `Avg. Salary`, `Max. Salary`, `Min. Salary`.
   - Created a table visualization to display the following columns:
     - Job Title
     - Avg. Salary
     - Total Headcount
     - Min. Salary
     - Max. Salary

### 5. **Top Earners by Job Title**
   - Used the "Headcount by Job Title" chart from the first question.
   - Created a table showing Name, EmpID, Gender, and Salary.
   - Applied a "Top N" filter to show the top 3 earners.

### 6. **Education Qualification vs Salary**
   - Transformed data by creating a distinct table for Education Qualification and assigning each qualification an ID.
   - Created a scatter plot with Salary on the X-axis and Qualification ID on the Y-axis, using Education Qualification as the legend to color the points.
   - Adjusted Y-axis scale for better visibility.

### 7. **Staff Growth Trend Over Time**
   - Created a new measure `Cumulative Headcount`.
   - Visualized the growth trend over time using a line chart, with Date of Join on the X-axis and Cumulative Headcount on the Y-axis.

### 8. **Employee Filter by Starting Letter**
   - Added a new column to extract the first letter of the employee's name.
   - Created a table showing EmpID, Name, Job Title, and Salary (with data bars).
   - Added a slicer to filter by the first letter of the name.
   - Displayed Total Headcount as a card.

### 9. **Leave Balance Analysis**
   - Created two measures: `Avg. Leave Balance` and `LB over 20 days`.
   - Visualized leave balance by job title using a stacked bar chart.
   - Integrated the gender breakdown pie chart for leave balance analysis.

### 10. **HR Dashboard**
   - Integrated all the visualizations into an interactive HR Dashboard to provide an overview of key HR metrics.

---

## File Structure

- **HRDashboard.pbix**: Power BI file containing the HR Dashboard with all the visualizations and measures.
- **Hr-Data.xlsx**: Original dataset used for the analysis.

---

## How to Use

1. **Prerequisites**: 
   - Download and install [Power BI Desktop](https://powerbi.microsoft.com/downloads/).
   
2. **Running the Dashboard**:
   - Download the `HRDashboard.pbix` file and the `Hr-Data.xlsx` dataset.
   - Open `HRDashboard.pbix` in Power BI Desktop.
   - Ensure that the `Hr-Data.xlsx` file is properly loaded as the data source in Power BI.

3. **Interactivity**:
   - The dashboard is interactive, allowing you to filter and explore different aspects of the data using slicers and charts.
   - Key metrics like gender breakdown, salary analysis, age spread, and leave balance are visualized and can be explored dynamically.

---

## Conclusion

This HR Dashboard project in Power BI provides insights into various aspects of employee data, such as job title distribution, gender breakdown, salary trends, and leave balance analysis. The interactive nature of the dashboard enables HR professionals to easily monitor and explore employee-related data to make informed decisions.

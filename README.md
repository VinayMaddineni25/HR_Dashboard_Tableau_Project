# HR ANALYTICS DASHBOARD

## Problem Statement : 
* The report initially prepared in Excel required migration or replication in Power BI.
* Analyzed the report to identify the visuals used and the DAX formulas applied to create calculated columns and measures

### Steps for Creating the HR Analytics Dashboard in Tableau

#### Step 1: Load Data
1. **Load data into Tableau Desktop** from an Excel file or through a SQL server connection.

#### Step 2: Create Dashboard Components
1. **Create Sheets**: Create seven sheets for different visualizations.

#### Step 3: KPI Metrics
1. **Create KPI Sheet**:
   - **Metrics**: Employee Count, Attrition Count, Attrition Rate, Active Employees, Average Age.
   - **Formulas**:
     - Attrition Count: `IF [Attrition] = 'YES' THEN 1 ELSE 0 END`
     - Attrition Rate: `SUM([Attrition Count]) / SUM([Employee Count])`
     - Active Employees: `SUM([Employee Count]) - SUM([Attrition Count])`
   - **Table Setup**: One row and five columns.

![image](https://github.com/VinayMaddineni25/HR_Dashboard_Tableau_Project/assets/71554745/a9ace4a7-8203-41d4-ad29-a867360d7b86)

#### Step 4: Attrition by Gender
1. **Create Gender Attrition Sheet**:
   - **Chart Type**: Horizontal bar chart.
   - **Setup**: Gender in rows, Attrition Count in columns.

![image](https://github.com/VinayMaddineni25/HR_Dashboard_Tableau_Project/assets/71554745/973be5e4-3de8-4d36-8687-bc2d032f648e)

#### Step 5: Department-wise Attrition
1. **Create Department Attrition Sheet**:
   - **Chart Type**: Pie chart.
   - **Setup**: Department in color, Attrition Count in angle and labels.

![image](https://github.com/VinayMaddineni25/HR_Dashboard_Tableau_Project/assets/71554745/7fcb5273-4792-456e-8859-beaa921441dc)

#### Step 6: No of Employee by Age 
1. **Create Employee Age Sheet**:
   - **Setup**: Create a bin for Age parameter.

![image](https://github.com/VinayMaddineni25/HR_Dashboard_Tableau_Project/assets/71554745/f7ffc8b0-9e95-41ce-8ba5-190b9f254f47)
   - **Chart Type**: Bar chart.
   - **Setup**: Age (bin) in columns, Employee Count in rows and labels.

![image](https://github.com/VinayMaddineni25/HR_Dashboard_Tableau_Project/assets/71554745/13101f75-9331-45c1-a721-ee97d6e2b2a9)

#### Step 7: Job Satisfaction Rating
1. **Create Job Satisfaction Sheet**:
   - **Setup**: Job Role in rows, Job Satisfaction (converted to dimensions) in columns, Employee Count in text.

![image](https://github.com/VinayMaddineni25/HR_Dashboard_Tableau_Project/assets/71554745/4b9f1562-4923-49d4-acad-bfce1761960c)

#### Step 8: Education Field-wise Attrition
1. **Create Education Attrition Sheet**:
   - **Chart Type**: Horizontal bar chart.
   - **Setup**: Education Fields in rows, Attrition Count in columns.

![image](https://github.com/VinayMaddineni25/HR_Dashboard_Tableau_Project/assets/71554745/778ec926-9a6b-4bae-9a26-1c4a986081bb)

#### Step 9: Attrition Rate by Gender for Different Age Groups
1. **Create Gender Age Group Attrition Sheet**:
   - **Chart Type**: Pie chart.
   - **Setup**: Age bands in columns, Gender in colors, Attrition Count in angles.
   - **Dual Axis**: Add a dummy axis for labels and set both axes as dual axes.

![image](https://github.com/VinayMaddineni25/HR_Dashboard_Tableau_Project/assets/71554745/7de1bcf8-7a9b-4e8e-8112-cae02f4958a6)

#### Step 10: Assemble the Dashboard
1. **Create Dashboard**:
   - **Background**: Add a background image.

![HR Templete background](https://github.com/VinayMaddineni25/HR_Dashboard_Tableau_Project/assets/71554745/53d3e29b-522b-4410-a52f-34f649cab36b)

   - **Add Sheets**: Place all created sheets into the dashboard and adjust their positions and sizes.

![image](https://github.com/VinayMaddineni25/HR_Dashboard_Tableau_Project/assets/71554745/c6b99ce5-63d1-4387-b68f-54856c3845b8)

By following these simplified steps, you can create a comprehensive HR Analytics Dashboard in Tableau that visualizes key metrics and insights.

# INSIGHTS

The HR Analytics Dashboard provides a comprehensive overview of various metrics related to employee attrition, demographics, and job satisfaction. Here are the insights derived from the dashboard:

### Key Performance Indicators (KPIs)
1. **Employee Count**: The total number of employees is 1,470.
2. **Attrition Count**: The number of employees who have left the organization is 237.
3. **Attrition Rate**: The overall attrition rate is 16.12%.
4. **Active Employees**: The number of currently active employees is 1,233.
5. **Average Age**: The average age of employees is 37.

### Department-wise Attrition
- **R&D**: 56.12% (133 employees)
- **Sales**: 38.82% (92 employees)
- **HR**: 5.06% (12 employees)

### Employee Demographics
- **Number of Employees by Age Group**: 
  - 18-21: 28
  - 21-24: 43
  - 24-27: 91
  - 27-30: 164
  - 30-33: 190
  - 33-36: 213
  - 36-39: 177
  - 39-42: 139
  - 42-45: 111
  - 45-48: 98
  - 48-51: 76
  - 51-54: 56
  - 54-57: 54
  - 57-60: 28

### Attrition by Gender
- **Female**: 87 employees
- **Male**: 150 employees

### Education Field-wise Attrition
- **Life Sciences**: 89 employees
- **Medical**: 63 employees
- **Marketing**: 47 employees
- **Technical Degree**: 32 employees
- **Other**: 11 employees
- **Human Resources**: 7 employees

### Attrition Rate by Gender for Different Age Groups
- **Under 25**:
  - Female: 20 (8.44%)
  - Male: 18 (7.59%)
- **25-34**:
  - Female: 112 (47.26%)
  - Male: 43 (18.14%)
- **35-44**:
  - Female: 51 (21.52%)
  - Male: 37 (15.61%)
- **45-54**:
  - Female: 25 (10.55%)
  - Male: 9 (3.80%)
- **Over 55**:
  - Female: 11 (4.64%)
  - Male: 3 (1.27%)

### Job Satisfaction Rating by Job Role
- **Healthcare Representative**: 
  - Ratings: 1 (26), 2 (19), 3 (43), 4 (43)
- **Human Resources**: 
  - Ratings: 1 (10), 2 (16), 3 (13), 4 (13)
- **Laboratory Technician**: 
  - Ratings: 1 (56), 2 (48), 3 (75), 4 (80)
- **Manager**: 
  - Ratings: 1 (21), 2 (21), 3 (27), 4 (33)
- **Manufacturing Director**: 
  - Ratings: 1 (18), 2 (25), 3 (37), 4 (65)
- **Research Director**: 
  - Ratings: 1 (43), 2 (49), 3 (53), 4 (65)
- **Research Scientist**: 
  - Ratings: 1 (54), 2 (53), 3 (90), 4 (95)
- **Sales Executive**: 
  - Ratings: 1 (69), 2 (54), 3 (91), 4 (112)
- **Sales Representative**: 
  - Ratings: 1 (12), 2 (21), 3 (27), 4 (23)

### Summary
The dashboard highlights several key insights:
- The R&D department has the highest attrition rate at 56.12%.
- The majority of employees fall in the age range of 30-33 years.
- Male employees have a higher attrition rate compared to female employees.
- Most attrition occurs in the Life Sciences and Medical education fields.
- Job satisfaction ratings vary significantly by job role, with Research Scientists and Sales Executives having higher ratings.

This information can be used to address areas with high attrition, improve job satisfaction, and better understand employee demographics and their impact on the organization.

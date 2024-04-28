# Health-Care_Power_BI_Project

## Project Overview:

Your project aims to analyze healthcare data related to patient waiting lists across different specialties and categories (inpatient & outpatient) from the years 2018 to 2021. The goal is to track the current status of patient waiting lists, analyze historical monthly trends, and perform detailed specialty-level and age-profile analysis.


## Project Goals:
1. Track the current status of patient waiting lists.
2. Analyze historical monthly trends of waiting lists in inpatient and outpatient categories.
3. Perform detailed specialty-level and age-profile analysis.

#### Data Scope:
 * Data spans from 2018 to 2021.

#### Metrics Required:
1. Average and Median Waiting List
2. Current Total Wait List

#### Views Required:
* Summary Page
* Detailed Page for Granular Analysis

### Steps Taken:

- Step 1 : Imported the data into Power BI, connecting the files stored in your system for inpatient and outpatient data.
- Step 2 : Performed data transformation, including correcting data types, renaming columns appropriately, and adding a new column named 'case_type' using custom column feature.
- Step 3 : Appended the inpatient and outpatient tables using the append query feature in Power BI.
- Step 4 : Saved all changes and modeled the data, ensuring proper connection of tables.
- Step 5 : Started the visualization part.
- Step 6 : Created a measure named 'latest month waitlist' using the DAX formula:

latest month waitlist = CALCULATE(SUM(All_Data[Total]), ALL_Data[Archive_Data] = MAX(ALL_Data[Archive_Data]))

- Step 7 : Created another measure named 'PY Latest Month Waitlist' using the DAX formula:

PY Latest Month Waitlist = CALCULATE(SUM(All_Data[Total]), ALL_Data[Archive_Data] = EDATE(MAX(ALL_Data[Archive_Data]), -12))

- Step 8 : Created additional measures for Average Waiting List, Median Waiting List, and a calculated column named 'Avg/Med wait list' using SWITCH function.
- Step 9 : Utilized various visualizations such as pie charts, bar charts, grid cards, and line charts.
- Step 10 : Created a second page in the visualization called 'Detailed View' and added a table view to visualize granular data including archive date, day case, inpatient, outpatient, and total.

### Data Sets Used:

File Name: mapping_specialty
Columns: Specialty, Specialty Group

File Name: Inpatient (2018-2021)
Columns: Archive_Date, Specialty_HIPE, Specialty_Name, Case_Type, Adult_Child, Age_Profile, Time_Bands, Total

File Name: Outpatient (2018-2021)
Columns: Archive_Date, Specialty_HIPE, Specialty, Adult_Child, Age_Profile, Time_Bands, Total
This summary encompasses the key aspects of your healthcare data analysis project, including data processing, visualization, and analysis steps undertaken to achieve the project goals.

   
#### A short of the Summary page of the project.

![Screenshot 2024-04-28 052154](https://github.com/somnath-97/Health-Care_Power_BI_Project/assets/148855296/1145078e-9fc2-4e81-a3c2-42d588358361)


#### A short of the Detailed View page of the project.
 
![Screenshot 2024-04-28 052210](https://github.com/somnath-97/Health-Care_Power_BI_Project/assets/148855296/4100d2c8-64b0-4292-83ad-d12b07755414)


 #### A short of the DrillDown page of the project.

 ![Screenshot 2024-04-28 052224](https://github.com/somnath-97/Health-Care_Power_BI_Project/assets/148855296/f19a3658-b7f5-4938-9513-67fd462e4f1f)

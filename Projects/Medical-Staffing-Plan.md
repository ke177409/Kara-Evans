# Medical Staffing Plan: Project Overview
Created a plan to help a staffing agency distribute medical staff throughout the United States during influenza seasons.
Performed data cleansing and statistical analyses on U.S. Census and CDC data sets using Excel and Tableau.
Developed a dashboard to present visualizations using Tableau.

### [YouTube Project Walk-Through](https://youtu.be/vcfuhCl_TEA)

## Tools & Skills
Excel
* Data cleansing, transformation, and integration
* Statistical analysis
  
Tableau
* Data manipulation
* Spatial analysis
* Visualizations

## Purpose & Context
I was tasked to perform exploratory and statistical analyses on multiple data sets using Excel and Tableau. This project was a part of CareerFoundry’s Data Immersion curriculum and was evaluated with feedback by a tutor and mentor. I was responsible for deciding on the project scope and final presentation format.

## Data Cleaning, Integration, and Transformation
* Removed duplicates using concatenate and COUNTIF functions in Excel to retain unique combinations of County/Year/Population in the US Census dataset.
* Imputed missing state values in Influenza Death dataset by using other identifying variables.
* Removed columns and rows with missing or irrelevant data:
  * All age groups and the state of Florida in ILI visits dataset
  * "State code" in Influenza Death dataset
* Converted values into appropriate datatypes:
  * Population counts from decimals into whole numbers
  * State abbreviations to their full names
* Corrected year "20133" to "2013" in Influenza Death dataset.
* Restructured age groups into a consistent format to allow for dataset integration.
* Integrated datasets using VLOOKUP function in Excel.
* Created a new variable that normalizes mortality rates for each age group.

## Visualizations
Spatial analysis was crucial for this project’s goal. With the use of an intuitive color gradient, I was able to create a map of the United States that draws the viewer’s eyes to areas most affected by influenza 
infections.
<p align="center">
  <img src="https://github.com/ke177409/Medical-Staffing-Plan/assets/118031032/a725ebdd-f43c-4ba7-af73-8a44ff0f1b08" width="475" height="323"/>
</p>

Portraying multiple variables in one visualization helped me uncover insights that were not easily identifiable from the raw data. For example, states with more medical staff than influenza patients also 
tend to have lower mortality rates. 
![Staff to Patient ratio (1)](https://github.com/ke177409/Medical-Staffing-Plan/assets/118031032/ba912df1-fc30-4bed-9866-db2145011bde)

## Recommendations and Findings
* The staffing agency should begin allocating medical staff prior to January each year when influenza death counts are highest.
* The weighted average mortality rate and staff-to-patient ratio should be used to determine how many staff members need to be sent to each state.

## Datasets
* “Influenza deaths by geography, time, age, and gender”, Source: [CDC](https://wonder.cdc.gov/ucd-icd10.html)
* “Population data by geography”, Source: [US Census Bureau, CSV file](https://coach-courses-us.s3.amazonaws.com/public/courses/data-immersion/A1-A2_Influenza_Project/Census_Population_transformed_202101.csv)
* “Counts of influenza laboratory test results by state”, Source: [CDC Fluview, Excel file](https://images.careerfoundry.com/public/courses/data-immersion/A1-A2_Influenza_Project/CDC_Influenza_Visits.xlsx)

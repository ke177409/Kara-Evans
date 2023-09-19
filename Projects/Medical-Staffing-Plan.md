# Medical Staffing Plan: Project Overview
Hospitals and clinics in the U.S. experience a surge of incoming patients during influenza seasons which puts a strain on hospital staff as well as patients seeking treatment. I created a plan to help a staffing agency distribute medical staff throughout the United States during influenza seasons.
I performed data cleansing and statistical analyses on 2010 to 2017 data obtained from the United States Census and Centers for Disease Control and Prevention (CDC) using Excel and Tableau.
An interactive dashboard was created to present visualizations using Tableau.

### [YouTube Project Walk-Through](https://youtu.be/vcfuhCl_TEA)
### [Tableau Dashboard](https://public.tableau.com/shared/G7BRJWCG4?:display_count=n&:origin=viz_share_link)

## Tools & Skills
Excel
* Data cleansing, transformation, and integration
* Statistical analysis
  
Tableau
* Data manipulation
* Spatial analysis
* Visualizations

## Purpose & Context
I performed exploratory and statistical analyses on multiple data sets using Excel and Tableau. This project was a part of CareerFoundry’s Data Immersion curriculum and was evaluated with feedback by a tutor and mentor. I was responsible for deciding on the project scope and final presentation format.

## Data Cleaning, Integration, & Transformation
* Removed duplicates using concatenate and COUNTIF functions in Excel to retain unique combinations of County/Year/Population in the U.S. Census dataset.
* Imputed missing state values in "Influenza Death" dataset by using other identifying variables.
* Removed columns and rows with missing or irrelevant data:
  * All age groups and the state of Florida in "ILI visits" dataset
  * "State code" column in "Influenza Death" dataset
* Converted values into appropriate datatypes:
  * Population counts from decimals into whole numbers
  * State abbreviations to their full names
* Corrected year "20133" to "2013" in "Influenza Death" dataset.
* Restructured age groups into a consistent format to allow for dataset integration.
* Integrated datasets using VLOOKUP function in Excel.
* Created a new variable that normalizes mortality rates for each age group.

## Visualizations
This line graph displays annual totals of influenza infections based on reported influenza test results. This confirms that there is an upward trend of influenza patients in the U.S. each year. 

<img src="images/Line%20Influenza%20Patients.png"/>

Spatial analysis was crucial for this project’s goal. With the use of an intuitive color gradient, I created a map of the United States that draws the viewer’s eyes to areas most affected by influenza 
infections. States with a darker red shading represent those with higher counts of influenza deaths for all age groups. Large and darker shaded dots within each state represent larger total population sizes. California and Texas have the largest population sizes. New York and California have the highest counts of influenza deaths. 

<img src="images/Map%20U.S.%20Deaths%20%26%20Pop..png" />

I explored the proportions of age groups in each state population based on the assumption that certain age groups are more susceptible to influenza than others. This line chart shows the sum of influenza deaths for all age groups as well as the seasonality of these infections. January has the highest number of deaths and August has the lowest number of deaths. Age groups 45 years and older also had the highest rates of deaths and were labelled as vulnerable populations in this analysis.

<img src="images/Line%20Deaths%20by%20Month.png"/>

This stacked bar chart shows the proportion of each vulnerable age group population in each state. Maine had the largest proportion and Utah had the lowest. 

<img src="images/%25%20All%20Ages.png"/>

The next two images represent influenza deaths for age groups 45 and older. This map shows the count of deaths and total population where California and New York are still the most affected.

<img src="images/Map%20Deaths%2045-85%20%26%20Pop..png"/>

However, the second map uses a more precise measure called the weighted average mortality rate. This measure was calculated using the proportion of each vulnerable age group’s population and the total mortality rate for that age group. The mortality rate scale assigns the dark red shading as high mortality and the lighter pink shading as low mortality. Increments in the mortality rate scale were labelled as follows: low, low-moderate, moderate, moderate-high, high. Using this measure shows more states heavily affected by influenza and California is no longer one of the top states. If the first map was used to determine where to send staff, many states would be left understaffed. States with high mortality rates will receive enough staff to meet a minimum 90% staff-to-patient ratio (up to 110% to avoid overstaffing). We can also incorporate the seasonality of previous seasons to predict when additional staff will be needed. 

<img src="images/Map%20WA%20Mort.%20Rate%2045-85%2B%20(2)%20(1).png"/>

This bar chart shows the staff-to-influenza patient ratios for each state. Montana and New Hampshire are overstaffed and have a low to low-moderate mortality rate, respectively. 
D.C. is the most understaffed, but influenza death counts were not available in the data set used in this analysis. Louisiana and Georgia have low percentages of staff and their mortality rates are moderate-high and high, respectively. I concluded that states with more medical staff than influenza patients also tend to have lower mortality rates. It is the intention of this project to boost the number of medical staff in these states enough to see a noticeable decline in mortalities.

<img src="images/Staff%20to%20Patient%20ratio%20(1).png"/>

## Recommendations & Findings
* The staffing agency should begin allocating medical staff prior to January each year when influenza death counts are highest.
* The weighted average mortality rate and staff-to-patient ratio should be used to determine how many staff members need to be sent to each state.
* Incorporate real-time updates for this dashboard to address staffing needs more precisely.
* The state of Florida needs number of providers and influenza patient data to determine staff-to-patient ratios.
* D.C. needs to need included in data collection for influenza death counts to determine mortality rates.
* Measure other factors that may affect influenza rates such as access to vaccinations and education on influenza prevention.

## The Learning Experience
My biggest challenge was learning to create visualizations in Tableau that speak for themselves. I researched tutorials and troubleshooting strategies to achieve 
my intended results. The weighted average mortality rate was one of my key variables in this analysis and was developed with the help of my mentor. I intend to use 
this calculation in future projects after understanding how it can influence results. Walking through each step of my process helped me to develop a coherent story for my final presentation. During this process I discovered results that were unexpected, which sparked new ideas to explore and more details to add to the project.

## Datasets
* *Underlying Cause of Death, 1999-2020* [Data set]. CDC. https://wonder.cdc.gov/ucd-icd10.html
  
* *Population data by geography* [Data set]. US Census Bureau, CSV file. https://coach-courses-us.s3.amazonaws.com/public/courses/data-immersion/A1-A2_Influenza_Project/Census_Population_transformed_202101.csv
  
* *Counts of influenza laboratory test results by state* [Data set]. CDC Fluview, Excel file. https://images.careerfoundry.com/public/courses/data-immersion/A1-A2_Influenza_Project/CDC_Influenza_Visits.xlsx

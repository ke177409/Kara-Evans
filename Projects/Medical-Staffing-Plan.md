# Medical Staffing Plan: Project Overview
Hospitals and clinics experience an influx of patients during influenza seasons, placing significant demands on healthcare staff and patients seeking treatment. To address this challenge, I developed a strategic plan to assist a staffing agency in efficiently deploying medical personnel across the United States during influenza seasons. This project was a part of CareerFoundry's Data Immersion curriculum and was evaluated by my tutor and mentor. I defined the project's scope and selected the format for the final presentation.

[YouTube Project Walk-Through](https://youtu.be/UtJXxrL7UzY)

<img src="images/Map%20U.S.%20Deaths%20%26%20Pop..png" />

Spatial analysis played a pivotal role in this project. An intuitive color gradient was used on a density map of the U.S., directing the viewer's attention to regions impacted by influenza infections. States exhibiting a darker red shading indicate higher counts of influenza-related deaths across all age groups. Additionally, large, and darker-shaded dots within each state correspond to areas with larger total population sizes.

California and Texas stand out with the most significant population sizes, while New York and California are the states reporting the highest counts of influenza-related deaths. 

<img src="images/Line%20Deaths%20by%20Month.png"/>

The sum of influenza-related deaths for all years and all age groups were plotted by month. January has the highest number of influenza-related deaths for all age groups, while August has the lowest.

Age groups 45 years and older exhibit the highest rates of influenza-related deaths and are identified as vulnerable populations in this analysis.

<img src="images/Map%20WA%20Mort.%20Rate%2045-85%2B%20(2)%20(1).png"/>

A weighted average was calculated for the mortality rate using the proportion of each vulnerable age group's population and the total mortality rate for that specific age group. The map uses a mortality rate scale that assigns darker red shading to indicate high mortality and lighter pink for low mortality. Gradations within the scale are labeled as follows: low, low-moderate, moderate, moderate-high, and high.

This measure provides a deeper understanding of the impact of influenza, revealing more states that are significantly affected by the virus. When determining staffing allocation, this measure should be used to ensure that states maintain a minimum 90% staff-to-patient ratio, with allowances up to 110% to avoid overstaffing. Additionally, seasonality data can be used to predict when additional staff will be needed.

<img src="images/Staff%20to%20Patient%20ratio%20(1).png"/>

Staff-to-influenza patient ratios were calculated for each state. States with more medical staff than influenza patients tend to have lower mortality rates:

* Montana and New Hampshire have the highest staffing ratios, with a low to low-moderate mortality rate, respectively.
* The District of Columbia (D.C.) is the most understaffed. However, influenza death counts were not available for this analysis.
* Louisiana and Georgia exhibit low staffing ratios and have moderate-high and high mortality rates, respectively.

## Data 
Influenza death counts were obtained from the Centers for Disease Control’s National Center for Health Statistics (NCHS). Influenza deaths are identified by each state's statistics office using diagnostic codes to record cause of death. Individuals are grouped by age range, and month and year of death from 2009 to 2017. Records with less than ten death counts are suppressed as part of the privacy policy for this data set and are excluded from this analysis. All records were suppressed for the District of Columbia.

U.S. Census Bureau population data was recorded annually for each state and its counties from 2009 to 2017. Data includes total population, male total population, female total population, and population by age group.

Records of patients with influenza-like illnesses (ILI) and provider data were provided by the U.S. Outpatient Influenza-like Illness Surveillance Network (ILINet). The data set includes the number of ILI visits and healthcare providers available by state from 2010 to 2019. ILI visits only capture respiratory-related illnesses with symptoms of fever plus cough or sore throat, which may over represent the number of influenza visits. Data was not available for the state of Florida in this data set.

## Data Cleaning, Integration, & Transformation
* Duplicate records in the U.S. Census dataset were eliminated, ensuring the retention of unique combinations of County, Year, and Population.
* Columns and rows containing irrelevant, missing, or suppressed data were removed.
* Integer values, such as population counts, were converted from decimals into whole numbers. State abbreviations were transformed into their full names.
* Year "20133" in the "Influenza Death" dataset was corrected to "2013".
* Age groups were restructured into a consistent format.
* Created a new variable that normalizes the mortality rates for each age group.

## Tools & Skills
**Excel**
* Data cleansing and transformation using Pivot tables and CONCATENATE function to ensure data quality and consistency.
* Integration of data sets using combined keys and XLOOKUP function.
* Statistical hypothesis testing to define outliers and correlations using VAR, STDEV, AVERAGE, and CORREL functions.
  
**Tableau**
* Data manipulation and transformation.
* Spatial analysis techniques.
* Data storytelling using [dashboard and visualizations](https://public.tableau.com/views/U_S_InfluenzaData2010-2017/Story1?:language=en-US&:display_count=n&:origin=viz_share_link).

## Recommendations & Findings
* The staffing agency should begin allocating medical staff in December each year when influenza death counts begin to increase.
* Utilize the weighted average mortality rate and staff-to-patient ratio to determine the number of staff members required for each state.
* Incorporate real-time updates into the dashboard to ensure that staffing remains responsive to evolving conditions.
* Incorporate provider and patient data for the state of Florida to determine staff-to-patient ratios.
* Extend the analysis to measure other factors that may affect influenza rates, such as access to vaccinations and education on influenza prevention.
  
## The Learning Experience
The weighted average mortality rate played a significant role in this analysis, a calculated variable created with the guidance of my mentor. This calculation focused on areas with the greatest impact based on death rates in relation to population proportions. Focusing on states with the most death and population counts would exclude a large portion of the country from receiving medical assistance.

## Datasets
* *Underlying Cause of Death, 1999-2020* [Data set]. Centers for Disease Control and Prevention. https://wonder.cdc.gov/ucd-icd10.html
  
* *Population data by geography* [Data set]. U.S. Census Bureau, CSV file. https://coach-courses-us.s3.amazonaws.com/public/courses/data-immersion/A1-A2_Influenza_Project/Census_Population_transformed_202101.csv
  
* *Outpatient Illness Surveillance* [Data set]. U.S. Outpatient Influenza-like Illness Surveillance Network (ILINet), Excel file. https://images.careerfoundry.com/public/courses/data-immersion/A1-A2_Influenza_Project/CDC_Influenza_Visits.xlsx

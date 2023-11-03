# Medical Staffing Plan: Project Overview
In the United States, hospitals and clinics face a substantial influx of patients during influenza seasons, placing significant demands on both healthcare staff and patients seeking treatment. To address this challenge, I developed a strategic plan to assist a staffing agency in efficiently deploying medical personnel across the country during influenza seasons.

I conducted data cleansing and comprehensive statistical analyses on data obtained from the United States Census and the Centers for Disease Control and Prevention (CDC). The outcome of this effort was the creation of an interactive dashboard, leveraging Tableau's capabilities to present insightful visualizations. These visualizations served as a valuable resource for decision-makers, enabling them to make data-driven choices when deploying medical staff to areas most affected by influenza outbreaks.

### [YouTube Project Walk-Through](https://youtu.be/UtJXxrL7UzY)
### [Tableau Dashboard](https://public.tableau.com/shared/G7BRJWCG4?:display_count=n&:origin=viz_share_link)

## Tools & Skills
Excel
* Data cleansing, transformation, and integration of diverse datasets to ensure data quality and consistency.
* Translating complex business objectives and requirements into actionable data-driven strategies and solutions.
* Statistical hypothesis testing to derive meaningful insights, validate assumptions, and support evidence=based decision-making.
  
Tableau
* Data manipulation and transformation.
* Spatial analysis techniques.
* Visual analysis to uncover patterns, trends, and critical information.
* Forecasting using statistical methods to facilitate proactive planning and resource allocation.
* Data storytelling using data-driven insights to communicate findings.

## Purpose & Context
As part of CareerFoundry's Data Immersion curriculum, I conducted comprehensive exploratory and statistical analyses on multiple datasets. This project underwent a rigorous evaluation process, with feedback provided by a dedicated tutor and mentor, enhancing the learning experience and the quality of the analysis.

Notably, I assumed the responsibility of defining the project's scope and selecting the optimal format for the final presentation. This active role in project management underscores my commitment to delivering meaningful insights and effective communication of findings, aligning with best practices in data analysis and presentation.

## Data Cleaning, Integration, & Transformation
* Duplicate records in the U.S. Census dataset were systematically eliminated, ensuring the retention of unique combinations of County, Year, and Population.
* Missing state values in the "Influenza Death" dataset were accurately imputed by leveraging other identifying variables, thereby preserving data completeness.
* Columns and rows containing irrelevant or missing data were systematically removed, including the exclusion of all age groups and the state of Florida in the "ILI visits" dataset, as well as the removal of the "State code" column in the "Influenza Death" dataset.
* Values, such as population counts, were converted from decimals into whole numbers, and state abbreviations were transformed into their full names.
* Year "20133" in the "Influenza Death" dataset was corrected to "2013."
* Age groups were restructured into a consistent format, allowing for seamless integration of datasets.
* Datasets were effectively integrated to generate a new variable that normalizes mortality rates for each age group, facilitating comprehensive analysis.

## Visualizations
This line graph represents the annual totals of influenza infections, as derived from reported influenza test results. This compelling visualization confirms the presence of a consistent upward trend in the number of influenza patients within the United States each year. The data depicted in the graph underscores the significance of influenza as a recurring public health concern, demanding appropriate measures for prevention and management.

<img src="images/Line%20Influenza%20Patients.png"/>

Spatial analysis played a pivotal role in achieving the objectives of this project. An intuitive color gradient was strategically employed to generate a density map of the United States, effectively directing the viewer's attention to regions most significantly impacted by influenza infections.

The map utilizes varying shades of red, with states exhibiting a darker red shading indicating higher counts of influenza-related deaths across all age groups. Additionally, large and darker-shaded dots within each state correspond to areas with larger total population sizes, signifying regions with a more substantial demographic presence.

Notably, California and Texas stand out with the most significant population sizes, while New York and California are notably the states reporting the highest counts of influenza-related deaths. 

<img src="images/Map%20U.S.%20Deaths%20%26%20Pop..png" />

I explored the proportions of age groups within each state's population, guided by the assumption that specific age groups may exhibit a higher susceptibility to influenza infections than others. The resulting line chart effectively illustrates the sum of influenza-related deaths across all age groups, shedding light on the seasonality of these infections. January stands out with the highest number of influenza-related deaths, while August registers the lowest. This seasonality insight provides valuable information for healthcare planning and resource allocation, aligning with the observed peaks in influenza cases.

Furthermore, the analysis reveals that age groups 45 years and older exhibit the highest rates of influenza-related deaths. In the context of this analysis, these age groups are appropriately identified as vulnerable populations.

<img src="images/Line%20Deaths%20by%20Month.png"/>

This stacked bar chart conveys the proportion of vulnerable age group populations within each state. Notably, this visual representation reveals significant variation among states in terms of the prevalence of vulnerable age groups.

Maine emerges as the state with the most substantial proportion of vulnerable age group populations, indicating a higher concentration of individuals within these age groups who may be at greater risk of influenza-related complications. In contrast, Utah exhibits the lowest proportion, signifying a relatively lower presence of vulnerable age groups within its population.

<img src="images/%25%20All%20Ages.png"/>

The following two images provide insights into influenza-related deaths for age groups 45 and older. The first image presents a map displaying the count of deaths within this age group, juxtaposed against the total population. California and New York continue to stand out as states most significantly affected by influenza-related deaths within the 45 and older age group.

<img src="images/Map%20Deaths%2045-85%20%26%20Pop..png"/>

The second map introduces a more precise measure known as the weighted average mortality rate. This measure was calculated by considering the proportion of each vulnerable age group's population and the total mortality rate for that specific age group. The map uses a mortality rate scale that assigns varying shades, with dark red indicating high mortality and lighter pink representing low mortality. Gradations within the scale are labeled as follows: low, low-moderate, moderate, moderate-high, and high.

This refined measure provides a deeper understanding of the impact of influenza, revealing more states that are significantly affected by the virus. Notably, California is no longer one of the top states, emphasizing the importance of using precise metrics for decision-making.

When determining staffing allocation, it's essential to consider this measure to ensure that states with high mortality rates receive sufficient staff to maintain a minimum 90% staff-to-patient ratio, with allowances up to 110% to avoid understaffing. Additionally, the incorporation of historical seasonality data enables the prediction of when additional staff will be needed, contributing to effective and proactive resource management during influenza seasons.

<img src="images/Map%20WA%20Mort.%20Rate%2045-85%2B%20(2)%20(1).png"/>

The presented bar chart illustrates the staff-to-influenza patient ratios for each state, shedding light on staffing levels in relation to influenza patients. Several key observations emerge from this analysis:

* Montana and New Hampshire are notably overstaffed, with a low to low-moderate mortality rate, respectively. This suggests that these states have a surplus of medical staff in proportion to their influenza patient populations.
* The District of Columbia (D.C.) stands out as the most understaffed, indicating a significant shortage of medical personnel in this region. However, it's worth noting that influenza death counts were not available in the dataset used for this analysis.
* Louisiana and Georgia exhibit low percentages of medical staff in relation to their influenza patient populations. These states also have moderate-high and high mortality rates, respectively.

The analysis reveals a potential correlation between staffing levels and mortality rates, suggesting that states with more medical staff than influenza patients tend to have lower mortality rates. The project's goal is to bolster the number of medical staff in states with low staffing levels to achieve a noticeable decline in influenza-related mortalities. 

<img src="images/Staff%20to%20Patient%20ratio%20(1).png"/>

## Recommendations & Findings
* The staffing agency should initiate the allocation of medical staff prior to January each year when influenza death counts are at their peak. This proactive approach ensures that states are adequately prepared to address the surge in cases during peak influenza seasons.
* Utilize the weighted average mortality rate and staff-to-patient ratio to determine the number of staff members required for each state. This data-driven approach aligns staffing levels with the specific needs of each region.
* Incorporate real-time updates into the dashboard to address staffing needs more precisely. Real-time data ensures that the allocation of medical staff remains responsive to evolving conditions.
* The state of Florida should provide the necessary number of providers and influenza patient data to determine accurate staff-to-patient ratios. Similarly, the District of Columbia (D.C.) should be included in data collection for influenza death counts to calculate mortality rates accurately.
* Extend the analysis to measure other factors that may affect influenza rates, such as access to vaccinations and education on influenza prevention. A more comprehensive understanding of these factors can inform targeted interventions to reduce influenza-related morbidity and mortality.

## The Learning Experience
My most significant challenge was creating self-explanatory visualizations in Tableau. I researched tutorials and troubleshooting strategies to align my outcomes with my initial objectives. One of the pivotal variables in this analysis was the weighted average mortality rate, a metric whose development was facilitated by the guidance of my mentor. I envisage leveraging this calculation in upcoming projects, having gained an understanding of its potential impact on outcomes. The walkthrough of each procedural step enabled me to weave a coherent narrative for my final presentation. During this process I unearthed unexpected findings that catalyzed novel explorations to incorporate into my project.

## Datasets
* *Underlying Cause of Death, 1999-2020* [Data set]. CDC. https://wonder.cdc.gov/ucd-icd10.html
  
* *Population data by geography* [Data set]. US Census Bureau, CSV file. https://coach-courses-us.s3.amazonaws.com/public/courses/data-immersion/A1-A2_Influenza_Project/Census_Population_transformed_202101.csv
  
* *Counts of influenza laboratory test results by state* [Data set]. CDC Fluview, Excel file. https://images.careerfoundry.com/public/courses/data-immersion/A1-A2_Influenza_Project/CDC_Influenza_Visits.xlsx

# Product Analysis: Project Overview
I conducted an analysis of a movie rental company's data in preparation for the launch of a new online streaming service. The analysis yielded valuable insights, including the identification of key geographical markets for promoting the company's brand, the top-earning films, and the recognition of loyal customers. To achieve these findings, I employed SQL to efficiently organize, clean, filter, and integrate data, allowing for a comprehensive understanding of customer behavior and geographic sales data. Subsequently, I harnessed these SQL results to craft informative visualizations using Tableau.

### [GitHub Repo](https://github.com/ke177409/Product-Analysis)
### [Tableau Visuals](https://public.tableau.com/views/RockbusterFilmsCustomers/RentalDuration?:language=en-US&:display_count=n&:origin=viz_share_link)

## Tools & Skills
PostgreSQL
* Relational databases to manage and extract data.
* Filter, summarize, and clean data.
* [Inner joins](https://github.com/ke177409/Product-Analysis/blob/main/SQL_Inner_Joins.sql), using primary and foreign keys, to establish meaningful relationships between different tables within the dataset.
* Utilize [subqueries](https://github.com/ke177409/Product-Analysis/blob/main/SQL_Subqueries.sql) and [common table expressions](https://github.com/ke177409/Product-Analysis/blob/main/SQL_CTE.sql) to perform more complex queries.

Tableau
* Data Manipulation
* Visualizations

## Purpose & Context
I conducted an in-depth exploratory analysis on multiple datasets, employing SQL and Tableau to extract valuable insights addressing crucial stakeholder inquiries. I was responsible for defining the project's scope and determining the ultimate presentation format. This initiative was an integral component of CareerFoundry's Data Immersion curriculum, with the added benefit of expert evaluation and constructive feedback provided by both a tutor and mentor.

## Data Cleaning, Integration, & Transformation
* Corrected missing and inaccurate values by applying appropriate insert commands.
* Removed rows of data that did not conform to the project's criteria, executed through the use of delete commands.
* Checked for duplicate values within each data table.
* Checked for value format consistency within each column.
* Performed inner joins to connect tables.
* Composed outer statements to generate new variables, such as "average_amount_paid" and "top_customer_count".

## Visualizations
The average rental time was just under 5 days and the average rental rate was $2.98 per rental.

<p align="center">
<img src="images/Rental%20Duration.png" width="300" height="500">

<img src="images/Rental%20Rates.png" width="300" height="500">
</p>

Rental identification numbers were used to track the frequency of film rentals. PG-13 films had the highest rental rates and had the highest count of rentals. Consequently, these films contributed the highest revenue compared to other film categories, underscoring their popularity among customers.

<p align="center">
<img src="images/Total%20Revenue%20%26%20Number%20of%20Rentals%20by%20Rating%20(2).png">
</p>

The top-earning film in terms of revenue was "Scalawag Duck," which held an NC-17 rating. In contrast, the lowest-earning films were "Connection Microcosmos," rated G, and "Freedom Cleopatra," rated PG-13. These findings reinforce the observation that PG-13 rated films were rented more frequently and at a higher rental rate, resulting in greater revenue generation for the company.

<p align="center">
<img src="images/Lowest%20Earning%20Film%20Titles%20and%20Rating.png"/>
</p>

Customer identification numbers were employed to compute the overall count of customers in each country worldwide.
The analysis focused on the top 10 countries with the most substantial customer presence:
1. India (60)
2. China (53)
3. USA (36)
4. Japan (31)
5. Mexico (30)
6. Russia (28)
7. Brazil (28)
8. Philippines (20)
9. Turkey (15)
10. Indonesia (14)

<img src="images/Top%2010%20countries.png" />

Seven of the ten countries with the largest customer populations were in Asia.  India, in particular, emerged as the country with the highest number of customers overall. Furthermore, Asia as a region exhibited a significantly higher total revenue when compared to other regions across the globe.

<p align="center">
<img src="images/Map%20Revenue%20by%20Region.png" width="550" height="450">

<img src="images/Bar%20Revenue%20by%20Region.png" width="370" height="500">
</p>

Customers within the top ten countries were examined at the city level to assess if specific cities exhibited a substantial customer presence. The investigation revealed that Aurora, USA, held the highest number of customers among the cities considered. However, the remaining cities contained only one customer each, suggesting that they did not represent areas with significant customer bases.

To identify the top customers, a search was conducted based on total amount spent and total rentals, without constraining the search to a particular city or country.

<p align="center">
<img src="images/Top%20Paying%20Customers%20%233.png"/>
</p>

Four customers were found on both lists:
* Eleanor Hunt, Réunion
* Karl Seal, USA
* Marion Snyder, Brazil
* Clara Shaw, Belarus

These customers exhibit a high lifetime value for the company due to their combination of significant spending and frequent rental activity. Notably, two of these four high-value customers were also situated in countries ranked within the top 10 (USA and Brazil).

<p align="center">
<img src="images/Top%20Amount%20Paid.png" width="500" height="500">

<img src="images/Top%20Rental%20Counts.png" width="500" height="500">
</p>

## Recommendations & Findings
* Given the substantial customer base and revenue streams in Asian markets, it is advisable to focus on promoting the company's brand in these regions, capitalizing on the existing customer presence.
* The popularity of PG-13 rated films and their ability to generate the most substantial total revenue should guide the company's film acquisition and promotion strategies.
* While top customers were identified based on rental frequency and total spending, it is essential to consider additional factors such as membership duration to obtain a more comprehensive understanding of customer loyalty.
* To refine customer segmentation and enhance targeting, additional data measures including customer age, language preferences, movie genres, and more should be incorporated into the analysis. This will enable a more tailored approach to serving various customer segments.
* The company should regularly update its film inventory based on customer demographics and behavior, ensuring that the movie offerings align with the preferences and expectations of the customer base.

## The Learning Experience
Learning and using SQL was the biggest challenge in this project. I overcame this challenge by researching different SQL queries, studying the syntax intricacies, and valuable practice sessions with my mentor. Once I understood how to apply common table expressions and subqueries, I was able to develop more complex variables that provided useful information in my analysis.

## Dataset
*Rockbuster Stealth LLC* [Data Set]. CareerFoundry. https://github.com/ke177409/Product-Analysis/blob/main/Rockbuster.zip

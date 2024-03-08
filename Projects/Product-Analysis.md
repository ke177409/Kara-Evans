# Product Analysis: Project Overview
## Tools & Skills
**PostgreSQL**
* Filter, summarize, and clean data.
* [Inner joins](https://github.com/ke177409/Product-Analysis/blob/main/SQL_Inner_Joins.sql), using primary and foreign keys, to establish meaningful relationships between different tables within the dataset.
* Utilize [subqueries](https://github.com/ke177409/Product-Analysis/blob/main/SQL_Subqueries.sql) and [common table expressions](https://github.com/ke177409/Product-Analysis/blob/main/SQL_CTE.sql) to perform more complex queries.

**Tableau**
* Data Manipulation
* [Visualizations](https://public.tableau.com/views/RockbusterFilmsCustomers/RentalDuration?:language=en-US&:display_count=n&:origin=viz_share_link)

<p align="center">
<img src="images/Total%20Revenue%20%26%20Number%20of%20Rentals%20by%20Rating%20(2).png">
</p>

Customer data was analyzed for a movie rental company in preparation for the launch of a new online streaming service. Rental identification numbers were used to track the frequency of film rentals. PG-13 films had the highest rental rates and the highest count of rentals. These films generated the highest revenue compared to other film ratings, underscoring their popularity among customers.

<img src="images/Top%2010%20countries.png" />

Customer identification numbers were used to count customers in each country worldwide. The analysis focused on the top 10 countries with the largest customer presence.

<p align="center">
<img src="images/Map%20Revenue%20by%20Region.png" width="500" height="400">

<img src="images/Bar%20Revenue%20by%20Region.png" width="370" height="400">
</p>

Seven of the ten countries with the largest customer populations were in Asia. India had the highest number of customers overall. Asia as a region exhibited a significantly higher total revenue when compared to other regions.

<p align="center">
<img src="images/Top%20Amount%20Paid.png" width="500" height="500">

<img src="images/Top%20Rental%20Counts.png" width="500" height="500">
</p>

To identify the top customers, a search was conducted based on the total amount spent and total rentals, without constraining the search to a particular city or country. Four customers were found on both lists:
* Eleanor Hunt, Réunion
* Karl Seal, USA
* Marion Snyder, Brazil
* Clara Shaw, Belarus

These customers exhibit a high lifetime value for the company due to their combination of significant spending and frequent rental activity. Two of these four high-value customers were also situated in one of the top 10 countries (USA and Brazil).

## Recommendations & Findings
* Focus on promoting the company's brand in Asian markets to capitalize on the existing customer presence.
* Acquire and promote more PG-13 rated films to generate the most revenue.
* Consider additional factors such as membership duration to obtain a more comprehensive understanding of customer loyalty.
* Incorporate additional customer data measures, such as customer age, language preferences, movie genres, to serve various customer segments.
* Regularly update film inventory based on customer demographics and behavior.

## Data Cleaning, Integration, & Transformation
* Corrected missing and inaccurate values using insert commands.
* Removed irrelevant data using delete commands.
* Checked for duplicate values within each data table.
* Checked for value format consistency within each column.
* Performed inner joins to connect tables.
* Composed outer statements to generate new variables, such as "average_amount_paid" and "top_customer_count".

## Purpose & Context
I was responsible for defining the project's scope and determining the final presentation format. This project was a part of CareerFoundry’s Data Immersion curriculum and was evaluated by my tutor and mentor.

## The Learning Experience
This project involved a lot of SQL troubleshooting and practice with my mentor. Common table expressions and subqueries were one of the biggest challenges but allowed me to create variables that provided useful information in my analysis.

## Dataset
*Rockbuster Stealth LLC* [Data Set]. CareerFoundry. https://github.com/ke177409/Product-Analysis/blob/main/Rockbuster.zip

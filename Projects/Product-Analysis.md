# Product Analysis: Project Overview
Evaluated movie rental company data to provide insights prior to the launch of a new online streaming service. Findings include geographical markets to promote the company's brand, top-earning films, and identification of loyal customers. Used SQL to organize, clean, filter, and join data to understand customer behavior and geographic sales data. Created visuals with SQL results in Tableau.

### [Tableau Visuals](https://public.tableau.com/views/RockbusterFilmsCustomers/RentalDuration?:language=en-US&:display_count=n&:origin=viz_share_link)

## Tools & Skills
PostgreSQL
* Filter, summarize, and clean data
* Join tables within dataset using primary and foreign keys
* Utilize subqueries and common table expressions to perform more complex queries

Tableau
* Data Manipulation
* Visualizations

## Purpose & Context
I performed an exploratory analysis on multiple data sets using SQL and Tableau to generate insights to answer key stakeholder questions. I was responsible for deciding on the project scope and final presentation 
format. This project was a part of CareerFoundry’s Data Immersion curriculum and was evaluated with feedback by a tutor and mentor.

## Data Cleaning, Integration, & Transformation
* Corrected missing and incorrect values using insert commands.
* Removed rows from data tables using delete commands.
* Checked for duplicate values within each data table.
* Checked for value format consistency within each column.
* Performed inner joins to connect tables.
* Wrote outer statements to generate new variables (i.e., "average_amount_paid" and "top_customer_count").

## Visualizations
The average rental time was just under 5 days and the average rental rate was $2.98 per rental.

<p align="center">
<img src="images/Rental%20Duration.png" width="300" height="500">

<img src="images/Rental%20Rates.png" width="300" height="500">
</p>

Rental identification numbers were used to count how often a film was rented. PG-13 films had the highest rental rates and had the highest count of rentals. These films generated the most revenue compared to 
other films.

<p align="center">
<img src="images/Total%20Revenue%20%26%20Number%20of%20Rentals%20by%20Rating%20(2).png">
</p>

The highest earning film title was “Scalawag Duck”, rated NC-17. The lowest earning film titles were “Connection Microcosmos”, rated G, and “Freedom Cleopatra”, rated PG-13. These results support the finding that PG-13 
films were rented more frequently at a higher rental rate.
<p align="center">
<img src="images/Lowest%20Earning%20Film%20Titles%20and%20Rating.png"/>
</p>

Customer identification numbers were used to calculate the total number of customers in each country around the world. 
These results were narrowed down to the top 10 countries with the largest customer presence:
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

Seven of the ten countries with the largest customer populations were in Asia. This includes India which had the most customers overall. Asia also had a significantly higher total revenue than other regions in the world.

<p align="center">
<img src="images/Map%20Revenue%20by%20Region.png" width="550" height="450">

<img src="images/Bar%20Revenue%20by%20Region.png" width="370" height="500">
</p>

Customers located within the top ten countries were counted by city to determine if any cities held a high number of customers. Aurora, USA was found to have the most customers, however, the remaining cities only had one. These cities do not represent areas with a large customer base. Top customers were searched by total amount spent and total rentals regardless of city or country.

<p align="center">
<img src="images/Top%20Paying%20Customers%20%233.png"/>
</p>

Four customers were found on both lists:
* Eleanor Hunt, Réunion
* Karl Seal, USA
* Marion Snyder, Brazil
* Clara Shaw, Belarus

These customers have a high lifetime value based on their spending and rental frequency. Two of the four customers were also based in the top 10 countries (USA & Brazil).

<p align="center">
<img src="images/Top%20Amount%20Paid.png" width="500" height="500">

<img src="images/Top%20Rental%20Counts.png" width="500" height="500">
</p>

## Recommendations & Findings
* Focus brand in Asian markets where largest customer base and revenue streams are located.
* Films rated PG-13 are the most popular and generate the largest total revenue.
* Top customers were discovered based on rental frequency and total spending. Length of membership should also be considered when measuring customer loyalty.
* Include additional data measures (customer age, language, movie genres, etc.) to understand each customer segment.
* Continually update film inventory based on customer demographics and behavior.

## The Learning Experience
Learning and using SQL was the biggest challenge in this project. I overcame this challenge by researching different SQL queries, studying the syntax, and practicing with my mentor. Once I understood how to apply common table expressions and subqueries, I was able to develop more complex variables that provided 
useful information in my analysis.

## Dataset
*Rockbuster Stealth LLC* [Data Set]. CareerFoundry. https://github.com/ke177409/Product-Analysis/blob/main/Rockbuster.zip

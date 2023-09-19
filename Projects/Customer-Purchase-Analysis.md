# Customer Purchase Analysis: Project Overview
Evaluated online grocery service customer data to provide insights to sales and marketing teams. Findings include ideal time periods for advertising, popular products, and customer demographics. Prepared data for exploratory analysis by merging data frames and generating new variables in Python. Created visualizations in Python to illustrate relationships between variables.

## Tools & Skills
Python Version: 3.11

Packages: pandas, numpy, matplotlib, seaborn, scipy, pickle
* Data transformation, subsets, and quality checks
* Derive new variables using if- and for-loops
* Group and aggregate data
* Visualizations

Excel
* Track data population flow, consistency checks, wrangling steps, and column derivations
* Use of crosstabs
* Generate final report with Python visualizations

## Purpose & Context
I performed an exploratory analysis on multiple data sets using Excel and Python to generate insights to answer key stakeholder questions. This analysis was performed for learning purposes and all data was fabricated for the CareerFoundry Data Immersion course. Each part of this project was evaluated with feedback by a tutor and mentor.

## Data Cleaning & Transformation
After performing descriptive analyses on the data, I was able to identify areas where data cleaning and transformations were necessary. The following changes and variables were made:
* Dropped "eval_set" column because data was not pertinent to analysis.
* Dropped columns "First Name" and "Surname" to remove personally identifiable information.
* Renamed columns for clarity and consistency.
* Created dictionaries to assign appropriate data types and consistent variable names.
* Checked datasets for mixed data types, missing data, and duplicate data.
 * Removed missing values in "product_name" column and duplicates from products dataset.
* Renamed null values as "N/A" in the orders dataset to flag as a user's initial order.
* Generated to filter data and create new columns using if- and for-loops in Python:
  * Product price ranges ("price_label")
  * Day of week popularity ("busiest_day")
  * Hour of day popularity ("busiest_period_of_day")
  * State regions ("Region")
  * Excluded users with less than five maximum orders
  * Users with dependents ("Parent_Flag")
* Used transform() and loc() functions in Python to aggregate customer data and create new variables:
  * Created "max_order" column to determine maximum number of orders and assign customer loyalty status
  * Created "average_price" column to determine average purchased item price and assign customer spending label
  * Created "median_days_prior_order" column to determine median number of days since prior order and assign customer frequency label
  * Created "Age_Profile" column to split users into different age groups
 
## Visualizations
I began by creating visuals that would help me gain an understanding of customer behavior. Each day of the week are represented as follows:

0 = Saturday

1 = Sunday

2 = Monday

3 = Tuesday

4 = Wednesday

5 = Thursday

6 = Friday

The first histogram measures the total number of orders for all users for each day of the week. Saturday (day 0) and Sunday (day 1) were the busiest days. 
Tuesday (day 3) and Wednesday (day 4) were the slowest days.  
The second histogram measures the total number of orders for each hour of the day for all users and all days of the week. 10am and 11am were the most popular 
times among all users. I also observed that orders begin to 
decline at 3:00pm until 4:00am the next day. The line graph represents user spending levels for each hour of the day. The y-axis represents the average dollar 
amount of purchased products and the time of day these purchases were made. User spending peaks early in the day around 2:00am to 3:00am, 4:00am to 5:00am, and 
6:00am to 7:00am. Spending is at its lowest around 7:00am to 10:00am. Around 11:00am spending steadily increases just before 3:00pm. There is a final spike of 
spending around 10:00pm.

<p align="center">
<img src="images/his_orders_day.png" width=370 height=330>

<img src="images/hist_orders_hour.png" width=370 height=330>

<img src="images/line_prices_orders_hour.png" width=370 height=330>
</p>

The stakeholders were interested to know which departments are the most popular. I measured the count of orders for each department and separated users based on number of dependents, age group, loyalty status, region, 
and family status. Produce, dairy/eggs, and beverages were the most popular departments among all users regardless of these factors.

<p align="center">
<img src="images/dept_parent_bar.png">

<img src="images/dept_age_bar.png">

<img src="images/dept_loyal_bar.png">

<img src="images/dep_region_bar.png">

<img src="images/dept_fam_bar.png">
</p>

Customer regions were defined as follows: 

**Region 1**: Maine, New Hampshire, Vermont, Massachusetts, Rhode Island, Connecticut, New York, Pennsylvania, New Jersey

**Region 2**: Wisconsin, Michigan, Illinois, Indiana, Ohio, North Dakota, South Dakota, Nebraska, Kansas, Minnesota, Iowa, Missouri

**Region 3**: Delaware, Maryland, District of Columbia, Virginia, West Virginia, North Carolina, South Carolina, Georgia, Florida, Kentucky, Tennessee, Mississippi, Alabama, Oklahoma, Texas, Arkansas, Louisiana

**Region 4**: Idaho, Montana, Wyoming, Nevada, Utah, Colorado, Arizona, New Mexico, Alaska, Washington, Oregon, California, Hawaii

Users were assigned a loyalty status based on their maximum order count. The bar chart below measures the total count of users by loyalty status and region.  Most users were labelled as regular customers whose maximum 
order count is 11 to 40 orders. A large population of these users were located in Region 3.

<img src="images/r_loyal_bar.png"/>

The box-and-whisker plot measures the spread of total income within each age group to determine which age group has the most spending power. The senior age group (ages 62 and older) had the highest total income and young users (ages 35 and younger) had the lowest. The bar chart shows the number of users by age group and dependent status. Middle-aged users with dependents made up most of the customer demographic.

<p align="center">
<img src="images/inc_allage_box.png" width=400 height=400/>
</p>

## Recommendations & Findings
* Increase advertising during peak hours (10am-11am) on the slowest days of the week (Tuesdays and Wednesdays).
* Advertise low price-ranged products because low-spenders are the most loyal users. Loyal customers were those whose maximum order count is greater than 40. Low spenders are those whose average item price is less than $10.
<p align="center">
<img src="images/crosstab_loyal_spend.png">
</p>

* Products advertised should include items from the most popular departments for all user groups and regions (produce, dairy/eggs, and beverage).
* Most customers are middle-aged, married, parents. Married users had the highest proportion of high spenders whose average item price is $10 or more.
<p align="center">
<img src="images/crosstab_spending_family.png">
<img src="images/parent_age_bar.png" width=395 height=395>
</p>

* Incorporate additional measures to determine customer loyalty status such as average price and length of membership.
 
## The Learning Experience
Learning a new programming language and applying it was a big learning curve during this project. I researched troubleshooting methods and consulted my mentor to understand how Python works to achieve my desired results. Researching Matplotlib and Seaborn libraries to understand their syntaxes helped to modify my visualizations. Writing neat and well-documented Python scripts, creating new variables, and generating visuals became easier over time as I continued to practice and learned how to resolve the errors in my code.

## Datasets
* **The Instacart Online Grocery Shopping Dataset 2017** [Data set]. Accessed from www.instacart.com/datasets/grocery-shopping-2017 via Kaggle.
  https://drive.google.com/file/d/1hweDzLp0OC-tlFoZm_PBvp2gfH_xeU0v/view?usp=sharing

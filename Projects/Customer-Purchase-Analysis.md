# Customer Purchase Analysis: Project Overview
Conducted an analysis of customer data from an online grocery service to offer valuable insights to the sales and marketing teams. The results encompassed optimal advertising timeframes, top-selling products, and customer demographic profiles. In the process of preparing data for exploratory analysis, I merged data frames and generated new variables using Python. Additionally, I created data visualizations in Python to effectively depict the relationships between various variables.

## Tools & Skills
Python Version: 3.11

Packages: pandas, NumPy, Matplotlib, seaborn, SciPy, pickle
* Executed data wrangling and merging operations.
* Derived new variables employing if- and for-loops.
* Applied grouping and aggregation techniques to organize and summarize data.
* Created visualizations to enhance data representation and interpretation.

## Purpose & Context
I conducted an in-depth exploratory analysis on multiple data sets using Python to extract valuable insights aimed at addressing critical questions posed by key stakeholders. It's worth noting that this analysis was executed for educational purposes, and all data was fictitious, as part of the CareerFoundry Data Immersion course. Each component of this project was thoroughly assessed, with valuable feedback provided by a tutor and mentor, contributing to a comprehensive learning experience.

## Data Cleaning & Transformation
Following a comprehensive descriptive analysis of the data, I identified several areas where data cleaning and transformation were necessary. Here's a summary of the changes and modifications that were made:

* The "eval_set" column was dropped as it wasn't relevant to the analysis.
* Columns "First Name" and "Surname" were removed to eliminate personally identifiable information.
* Column names were systematically renamed to enhance clarity and ensure consistency.
* Dictionaries were created to assign appropriate data types and maintain consistent variable names.
* A thorough check for mixed data types, missing data, and duplicate entries was conducted.
* Missing values in the "product_name" column were removed, and duplicates were eliminated from the products dataset.
* Null values in the orders dataset were renamed as "N/A" to signify a user's initial order.
* Filtering of data and creation of new columns were accomplished using if- and for-loops in Python, which included:
 * Establishing "price_label" for product price ranges.
 * Identifying the "busiest_day" of the week.
 * Determining the "busiest_period_of_day."
 * Grouping users into "Region" categories.
 * Excluding users with fewer than five maximum orders.
 * Assigning a "Parent_Flag" to users with dependents.
* The "transform()" and "loc()" functions in Python were employed to aggregate customer data and generate new variables, such as:
 * The creation of a "max_order" column to determine the maximum number of orders and assign customer loyalty status.
 * Developing the "average_price" column to calculate the average purchased item price and assign customer spending labels.
 * Introducing the "median_days_prior_order" column to compute the median number of days since the previous order and assign customer frequency labels.
 * Forming an "Age_Profile" column to categorize users into distinct age groups based on specific criteria.

These data cleaning and transformation efforts significantly enhanced the quality and utility of the dataset for further analysis and insights.
 
## Visualizations
I created visualizations aimed at providing insights into customer behavior. Each day of the week was represented as follows:

0 = Saturday

1 = Sunday

2 = Monday

3 = Tuesday

4 = Wednesday

5 = Thursday

6 = Friday

The initial histogram illustrated the total number of orders for all users on each day of the week. Notably, Saturday (day 0) and Sunday (day 1) emerged as the busiest days, while Tuesday (day 3) and Wednesday (day 4) were observed as the least active days in terms of order volume.

The second histogram depicted the total number of orders for each hour of the day, encompassing all users and all days of the week. It was evident that 10:00am and 11:00am stood out as the most popular times among all users. Notably, a decline in order frequency was observed starting at 3:00pm, continuing until 4:00am the following day.

The accompanying line graph conveyed user spending levels for each hour of the day. On the y-axis, it presented the average dollar amount of products purchased during specific time periods. The graph highlighted distinct peaks in spending during early morning hours, particularly around 2:00am to 3:00am, 4:00am to 5:00am, and 6:00am to 7:00am. Conversely, spending reached its lowest point from 7:00am to 10:00am.

Noteworthy trends included a gradual increase in spending just before 3:00pm, and a final spike in spending around 10:00pm. These observations provide valuable insights into user behavior and can inform strategic decisions related to marketing and promotions.

<p align="center">
<img src="images/his_orders_day.png" width=370 height=330>

<img src="images/hist_orders_hour.png" width=370 height=330>

<img src="images/line_prices_orders_hour.png" width=370 height=330>
</p>

To address the stakeholders' inquiry regarding the popularity of departments, I conducted an analysis by measuring the count of orders for each department while segmenting users based on several criteria, including the number of dependents, age group, loyalty status, region, and family status. The findings revealed that the departments of Produce, Dairy/Eggs, and Beverages consistently emerged as the most popular choices among all users, irrespective of these factors.

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

Users were classified into various loyalty status categories based on their maximum order count. A bar chart was utilized to illustrate the total count of users by loyalty status and region. The predominant category was "Regular Customers," denoting users with a maximum order count ranging from 11 to 40 orders. Significantly, a substantial portion of these regular customers was concentrated in Region 3.

<img src="images/r_loyal_bar.png"/>

The box-and-whisker plot was employed to gauge the dispersion of total income within each age group, helping identify which age group possessed the most significant spending power. Notably, the senior age group (ages 62 and older) exhibited the highest total income, while young users (ages 35 and younger) had the lowest total income.

In addition, a bar chart presented the distribution of users by age group and dependent status. The data indicated that middle-aged users with dependents constituted the largest segment within the customer demographic.

<p align="center">
<img src="images/inc_allage_box.png" width=400 height=400/>
</p>

## Recommendations & Findings

Based on the insights derived from the analysis, several recommendations can be made:

* Increase advertising efforts during peak hours, specifically from 10am to 11am, on the slowest days of the week, which are Tuesdays and Wednesdays. This strategy can help maximize exposure during periods when user engagement is lower and may lead to increased sales on these days.

* Target advertising campaigns towards low price-ranged products. The analysis revealed that low spenders, characterized by an average item price of less than $10, tend to be the most loyal users. By promoting affordable products, you can cater to the preferences of this loyal customer segment and potentially boost sales among them. Loyalty here is defined as users with a maximum order count greater than 40.
<p align="center">
<img src="images/crosstab_loyal_spend.png">
</p>

* Product promotions and advertising campaigns should prominently feature items from the most popular departments, which are Produce, Dairy/Eggs, and Beverages. These departments consistently attract the highest demand from all user groups and regions, making them ideal candidates for promotional efforts.
* Given that the majority of customers fall into the middle-aged, married, and parent demographic, it's advisable to design advertising strategies that resonate with this specific group. Of particular interest is the fact that married users tend to have the highest proportion of high spenders, defined by an average item price of $10 or more. Therefore, crafting marketing messages that cater to the preferences and needs of this demographic could lead to increased sales and customer satisfaction.
<p align="center">
<img src="images/crosstab_spending_family.png">
<img src="images/parent_age_bar.png" width=395 height=395>
</p>

* Incorporate additional measures such as average price and length of membership to determine customer loyalty status.
 
## The Learning Experience
Learning a new programming language and effectively applying it represented a substantial learning curve throughout this project. To master Python, I engaged in thorough research and employed troubleshooting techniques, in addition to consulting my mentor for guidance. This was essential to comprehend the intricacies of Python and to achieve the desired results for my analysis.

In the process of crafting visualizations, I dedicated time to researching the Matplotlib and Seaborn libraries, focusing on understanding their syntax and functionality. This knowledge was pivotal in modifying and enhancing the quality of my visual representations.

As I continued to work on the project, I observed significant progress in my ability to write clean and well-documented Python scripts. Additionally, I became increasingly proficient at creating new variables and generating visualizations. With each iteration and practice session, I developed the skills required to efficiently resolve errors in my code and enhance the overall quality of my work.

## Datasets
* **The Instacart Online Grocery Shopping Dataset 2017** [Data set]. Accessed from www.instacart.com/datasets/grocery-shopping-2017 via Kaggle.
  https://drive.google.com/file/d/1hweDzLp0OC-tlFoZm_PBvp2gfH_xeU0v/view?usp=sharing

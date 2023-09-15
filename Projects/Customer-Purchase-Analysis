# Customer Purchase Analysis: Project Overview
Developed insights for online grocery service sales and marketing teams using customer data. Findings include ideal time periods for advertising, popular products, and customer demographics. Prepared data for exploratory analysis by merging data frames and generating new variables in Python. Created visualizations in Python to illustrate relationships between variables.

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
I was tasked to perform an exploratory analysis on multiple data sets using Excel and Python to generate insights to answer key stakeholder questions. This analysis was performed for learning purposes and all data was fabricated for the CareerFoundry Data Immersion course. Each part of this project was evaluated with feedback by a tutor and mentor.

## Data Cleaning and Transformation
After performing descriptive analyses on the data, I was able to identify areas where data cleaning and transformations were necessary. The following changes and variables were made:
* Dropped column "eval_set" because data was not pertinent to analysis.
* Created dictionaries to assign appropriate data types and consistent variable names.
* Checked datasets for mixed data types, missing data, and duplicate data.
* Renamed null values as "N/A" in the orders dataset to flag as a user's initial order.
* Removed missing values in "product_name" column and duplicates from products dataset.
* Generated new columns using if- and for-loops in Python:
  * Product price ranges ("price_label")
  * Day of week popularity ("busiest_day")
  * Hour of day popularity ("busiest_period_of_day")
* Used transform() and loc() functions in Python to aggregate customer data and create new variables:
  * Created "max_order" column to determine maximum number of orders and assign customer loyalty status
  * Created "average_price" column to determine average purchased item price and assign customer spending label
  * Created "median_days_prior_order" column to determine median number of days since prior order and assign customer frequency label
 
## Visualizations
Below are a few of the key visuals included in this analysis:
<p align="center">
<img src="https://github.com/ke177409/Customer-Purchase-Analysis/assets/118031032/0d50db28-cf27-4879-a42c-69cbbfcc93af"/>
</p>

<p align="center">
<img src="https://github.com/ke177409/Customer-Purchase-Analysis/assets/118031032/d7b5615c-394f-41f0-90f0-c8b0622786ed"/>
</p>

<p align="center">
<img src="https://github.com/ke177409/Customer-Purchase-Analysis/assets/118031032/3e3cb237-7564-4d01-8723-7bb4938025e5" />
</p>

## Recommendations and Findings
* Increase advertising during peak hours (10am-11am) on the slowest days of the week (Tuesdays and Wednesdays).
* Advertise low price-ranged products because low-spenders are the most loyal users.
* Products advertised should include items from the most popular departments for all user groups and regions (produce, dairy/eggs, and beverage).
* Majority of customer demographic includes middle-aged, married, parents.
* Incorporate other variables to determine customer loyalty status.

## Datasets
* https://drive.google.com/file/d/1hweDzLp0OC-tlFoZm_PBvp2gfH_xeU0v/view?usp=sharing
* “The Instacart Online Grocery Shopping Dataset 2017”
  
  Accessed from www.instacart.com/datasets/grocery-shopping-2017 via Kaggle on July 15, 2023

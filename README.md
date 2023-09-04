# Online Retailer Marketing Metrics and KPIs Tracking

## Table of Contents
1. [Introduction](#introduction)
2. [Technologies and Skills](#tech-skills)
3. [Process Overview](#process)
4. [Data Cleaning and Validation](#cleaning-validation)
5. [Exploratory Data Analysis (EDA)](#eda)
6. [Calculating Marketing Metrics and KPIs](#marketing-metrics)

---

<a name="introduction"><a/>
## Introduction
In this project, we will be examining two years of sales data of a fictional online retailer based out of the UK. This retailer deals primarily in sales to distributers in large quantities, resulting in high value individual transactions. The company sells products consisting of multiple different categories, such as clothing, electronics, and books, among others. To view more information related to this dataset, view the [Kaggle dataset](https://www.kaggle.com/datasets/ronnykym/online-store-sales-data?resource=download).

This analysis starts with examing the data and performing data cleaning/validation to ensure the validity of the data. We will then perform exploratory analysis to examine sales trends by different categorical datatypes and over time. Lastly, a report will be generated to examine various different marketing metrics and evaluate the success of marketing operations.

This README file contains an abbreviated analysis without code. **See the [EDA and Marketing KPIs notebook](eda_and_marketing_kpis.ipynb) to view the full analysis and code.**

---

<a name="tech-skills"><a/>

## Technologies and Skills
**Technologies/Packages**: Python (Pandas, NumPy, Matplotlib, Seaborn)

**Skills**: Data Cleaning/Validation, Exploratory Data Analysis (EDA), Marketing Analytics, Data Visualization, Report Generation

---

<a name="process"><a/>
## Process Overview

### 1. Data Cleaning and Validation
   - Loading the Kaggle dataet and performing cleaning/validation to prepare data for analysis
### 2. Exploratory Data Analysis
   - Exploring the prepared data to find general sales trends
### 3. Calculating Marketing Metrics and KPIs
   - Generating marketing metrics/KPIs to track relevant metrics related to marketing metric and summarizing the findings

---

<a name="cleaning-validation"><a/>
## Data Cleaning and Validation

The first step of this analysis process involved cleaning and validating the data. This process involved tasks such as removing non-numeric values from numeric data, properly storing date values, and checking for duplicates and invalid values. See a sample of the cleaned data along with the data dictionary below:

### Data Sample

| order_id   | order_date | country   | revenue    | cost       | category | customer_name     | sales_manager  | sales_rep         | device_type |
|------------|------------|-----------|------------|------------|----------|-------------------|----------------|-------------------|-------------|
| 70-0511466 | 2020-02-12 | Sweden    | 17524.02   | 14122.61   | Books    | Goldner-Dibbert   | Maxie Marrow   | Madelon Bront     | Mobile      |
| 28-6585323 | 2019-09-26 | Finland   | 116563.40  | 92807.78   | Games    | Hilll-Vandervort  | Hube Corey     | Wat Bowkley       | Mobile      |
| 58-7703341 | 2019-07-11 | Portugal  | 296465.56  | 257480.34  | Clothing | Larkin-Collier    | Celine Tumasian| Smitty Culverhouse| PC          |
| 14-6700183 | 2020-04-02 | Portugal  | 74532.02   | 59752.32   | Beauty   | Hessel-Stiedemann | Celine Tumasian| Aurelie Wren      | PC          |
| 15-8765160 | 2019-12-22 | Spain     | 178763.42  | 146621.76  | Games    | Johns and Sons    | Emalia Dinse   | Bertha Walbrook   | Tablet      |

### Data Dictionary

- order_id (string): unique identifier of an order
- order_date (date): sale date
- country (string): country customer is located in
- revenue (float): sales revenue generated in EUR
- cost (float): cost of goods sold in EUR
- category (string): item category
- customer_name (string): name of customer
- device_type (string): The type of device used by customer to make online purchase (PC, mobile, tablet)
- sales_manager (string): name of the sales manager for each sale
- sales_representative (string): name of the sales rep for each sale

---

<a name="eda"><a/>
## Exploratory Data Analysis (EDA)

To gain a general sense of of the company's sales, EDA was performed. See some key takeaways from this process below:

### Distribution of Single-Order Revenue and Cost of Goods Sold

![fig1](EDA%20Visualizations/orders_revenue_cost.png)

We can see that orders are typically high in value, with most bringing in over £500000 in revenue and costing around the same amount as well.

<br/>

### Revenue by Country

![fig2](EDA%20Visualizations/country_revenue.png)

We can see that the countries of Portugal and France have generated the most revenue, followed by Sweden and the UK.

<br/>

### Top Categories

![fig3](EDA%20Visualizations/category_revenue.png)

Clothing is the most popular category of products sold, with many other categories having substantial sales as well.

<br/>

### Monthly Revenue Over Time

![fig4](EDA%20Visualizations/revenue_monthly_continuous.png)

The analysis of sales over time reveals substantial month-to-month fluctuations, peaking in December 2019 and sharply declining in February 2020. Seasonal trends are also evident, with sales rising in spring and summer, falling in fall, and resurging during December's winter holidays before decreasing again in winter months.

---

<a name="marketing-metrics"><a/>
## Calculating Marketing Metrics and KPIs
This report provides an in-depth overview of marketing metrics for an online retailer across multiple quarters. These metrics offer valuable insights into customer activity, retention, churn, and other key performance indicators that contribute to the retailer's success.

This report was also generated by calculating the max quarter/year, generating a range of all quarters and then iterating through this range of quarters. This allows the report to be generated in the future with new quarters of data with no adjustments to the code, streamlining the KPI calculation process.

To view description and formulas for the below metrics, see the [Marketing Metrics Descriptions and Dictionary](marketing_metrics_descriptions_and_dictionary.csv)


| Quarter of Year                     |2019Q1 |2019Q2 |2019Q3 |2019Q4 |2020Q1 |2020Q2 |2020Q3 |2020Q4 |
|-------------------------------------|-------|-------|-------|-------|-------|-------|-------|-------|
| Current Quarter Active Customers    | 51    | 51    | 47    | 53    | 52    | 54    | 52    | 49    |
| New Customers                       | 51    | 13    | 3     | 6     | 2     | 0     | 0     | 0     |
| Generation Rate                     | 1.0   | 0.2549| 0.0638| 0.1132| 0.0385| 0.0   | 0.0   | 0.0   |
| Previous Quarter Active Customers   | 0     | 51    | 51    | 47    | 53    | 52    | 54    | 52    |
| Retained Customers                  | 0     | 38    | 37    | 39    | 42    | 41    | 41    | 35    |
| Retention Rate                      | 0.0   | 0.7451| 0.7255| 0.8298| 0.7925| 0.7885| 0.7593| 0.6731|
| Customers Churned                   | 0     | 13    | 14    | 8     | 11    | 11    | 13    | 17    |
| Churn Rate                          | 0.0   | 0.2549| 0.2745| 0.1702| 0.2075| 0.2115| 0.2407| 0.3269|
| Current Quarter Inactive Customers  | 0     | 13    | 20    | 20    | 23    | 21    | 23    | 26    |
| Previous Quarter Inactive Customers | 0     | 0     | 13    | 20    | 20    | 23    | 21    | 23    |
| Revived Customers                   | 0     | 0     | 7     | 8     | 8     | 13    | 11    | 14    |
| Revival Rate                        | 0.0   | 0.0   | 0.5385| 0.4   | 0.4   | 0.5652| 0.5238| 0.6087|
| Historical Customer Count           | 51    | 64    | 67    | 73    | 75    | 75    | 75    | 75    |


#### 1. Active Customers (Current Quarter):
The number of active customers remained consistent over the observation periods. The highest count was recorded in 2019Q4 with 53 customers, while the lowest count was in 2019Q3 with 47 customers.

#### 2. New Customers and Generation Rate:
New customer acquisition displayed fluctuations, with the highest count (other than 2019Q1 where all customers were new) of 13 occurring in 2019Q2. The generation rate, which measures the proportion of new customers, mirrored these fluctuations, dropping to 0% in 2020Q2 and subsequent quarters due to no new customer additions.

#### 3. Retained Customers and Retention Rate:
Retained customer numbers varied across quarters, ranging from 37 in 2019Q3 to 42 in 2020Q1. The retention rate, indicating the proportion of retained customers, exhibited a positive trend, peaking at 80.77% in 2020Q1.

#### 4. Revived Customers and Revival Rate (Current Quarter):
The count of revived customers increased over time, reaching its zenith at 14 in 2020Q4. The revival rate, denoting the proportion of customers revived from inactivity, demonstrated fluctuations across quarters. The rate ranged from 0.35 in 2019Q3 to 0.619 in 2020Q2.

#### 5. Customers Churned and Churn Rate:
The count of churned customers exhibited fluctuations, reaching a peak of 17 in 2020Q4. The churn rate, representing the proportion of customers lost, fluctuated between 0.17 in 2019Q4 and 0.3269 in 2020Q4.

### Summary:
In summary, the online retailer's customer base remained stable over the observation period. Initiatives aimed at retaining and reviving customers yielded positive outcomes, as indicated by improved retention and revival rates. Churn rates experienced fluctuations, with the highest churn rate recorded in 2020Q4, however the high revival rates indicate that these customers often return in the quarter. New customer acquisition varied, with a decline in 2020Q2 that is yet to be recovered, indicating that more emphasis on customer acquisition marketing may be needed.

Collectively, these metrics offer valuable insights into the retailer's customer engagement and retention strategies.

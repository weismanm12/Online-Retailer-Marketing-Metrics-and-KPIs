# Online-Retailer-Marketing-Metrics-and-KPIs

## Table of Contents
1. [Introduction](#introduction)
2. [Technologies and Skills](#tech-skills)
3. [Process Overview](#process)
4. [Data Cleaning and Validation](#cleaning-validation)
5. [Exploratory Data Analysis](#eda)
6. [Calculating Marketing Metrics and KPIs](#marketing-metrics)

---

<a name="introduction"><a/>
## Introduction
In this project, we will be examining two years of sales data of a fictional online retailer based out of the UK. This retailer deals primarily in sales to distributers in large quantities, resulting in high value individual transactions. The company sells products consisting of multiple different categories, such as clothing, electronics, and books, among others. To view more information related to this dataset, view the [Kaggle dataset](https://www.kaggle.com/datasets/ronnykym/online-store-sales-data?resource=download).

This analysis starts with examing the data and performing data cleaning/validation to ensure the validity of the data. We will then perform exploratory analysis to examine sales trends by different categorical datatypes and over time. We will end by generating a marketing report to examine various different marketing metrics and evaluate the success of marketing operations.

See the [EDA and Marketing KPIs notebook](eda_and_marketing_kpis.ipynb) to view the full analysis and code.

---
<a name="tech-skills"><a/>

## Technologies and Skills
**Technologies/Packages**: Python (Pandas, NumPy, Matplotlib, Seaborn)

**Skills**: Cleaning/Validation, Exploratory Data Analysis (EDA), Marketing Analytics, Data Visualization, Report Generation

---

<a name="process"><a/>
## Process Overview

### 1. Cleaning and Validating Data
   - Loading the Kaggle dataet and performing cleaning/validation to prepare data for analysis
### 2. Exploratory Data Analysis
   - Exploring the prepared data to find general sales trends
### 3. Calculating Marketing Metrics and KPIs
   - Generating marketing metrics/KPIs to track relevant metrics related to marketing metric and summarizing the findings

---

<a name="cleaning-validation"><a/>
## Data Cleaning and Validation

---

<a name="eda"><a/>
## Exploratory Data Analysis

---

<a name="marketing-metrics"><a/>
## Marketing Metrics and KPIs
This report provides an in-depth overview of marketing metrics for an online retailer across multiple quarters. These metrics offer valuable insights into customer activity, retention, churn, and other key performance indicators that contribute to the retailer's success.

| qyear                         | 2019Q1 | 2019Q2 | 2019Q3 | 2019Q4 | 2020Q1 | 2020Q2 | 2020Q3 | 2020Q4 |
|-------------------------------|--------|--------|--------|--------|--------|--------|--------|--------|
| current_q_active_customers    |   51   |   51   |   47   |   53   |   52   |   54   |   52   |   49   |
| new_customers                 |   51   |   13   |   3    |   6    |   2    |   0    |   0    |   0    |
| generation_rate               |  1.0   | 0.2549 | 0.0638 | 0.1132 | 0.0385 |  0.0   |  0.0   |  0.0   |
| previous_q_active_customer    |   0    |   51   |   51   |   47   |   53   |   52   |   54   |   52   |
| retained_customers            |   0    |   38   |   37   |   39   |   42   |   41   |   41   |   35   |
| retention_rate                |  0.0   | 0.7451 | 0.7255 | 0.8298 | 0.7925 | 0.7885 | 0.7593 | 0.6731 |
| customers_churned             |   0    |   13   |   14   |   8    |   11   |   11   |   13   |   17   |
| churn_rate                    |  0.0   | 0.2549 | 0.2745 | 0.1702 | 0.2075 | 0.2115 | 0.2407 | 0.3269 |
| current_q_inactive_customers  |   0    |   13   |   20   |   20   |   23   |   21   |   23   |   26   |
| previous_q_inactive_customers |   0    |   0    |   13   |   20   |   20   |   23   |   21   |   23   |
| revived_customers             |   0    |   0    |   7    |   8    |   8    |   13   |   11   |   14   |
| revival_rate                  |  0.0   |  0.0   | 0.5385 |  0.4   |  0.4   | 0.5652 | 0.5238 | 0.6087 |
| historical_customer_count     |   51   |   64   |   67   |   73   |   75   |   75   |   75   |   75   |


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

<br>

#### Summary:
In summary, the online retailer's customer base remained stable over the observation period. Initiatives aimed at retaining and reviving customers yielded positive outcomes, as indicated by improved retention and revival rates. Churn rates experienced fluctuations, with the highest churn rate recorded in 2020Q4. New customer acquisition varied, with a decline in 2020Q2 that is yet to be recovered. Collectively, these metrics offer valuable insights into the retailer's customer engagement and retention strategies.

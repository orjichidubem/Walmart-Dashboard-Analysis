# Walmart-Dashboard-Analysis

## Table of contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results And Findings](#results-and-findings)
- [Recommandations](#recommandations)


### Project Overview
---

This project aims in analyzing sales trends, customer behavior, and product performance to identify opportunities for growth and optimization. This repository explores sales data to inform business and drive revenue.

![Walmart](https://github.com/user-attachments/assets/5f777576-2f90-4c18-bb8f-e9e141a6847e)


### Data Sources 
The primary dataset used for this analysis is the "walmart.csv" file, containing information about Historical sales data for 45 walmart stores located in different region.
{https://www.kaggle.com/datasets/yasserh/walmart-dataset}

### Tools

- Excel - Data cleaning.
- SQL Server - Data analysis.
- PowerBI - Creating dashboard reports.

### Data Cleaning
In the initial data preparation phase, we performed the following task:
1. Data loading and inspection.
2. Checking of duplicates.
3. Creating of addtional column.
4. Data cleaning and formatting.

### Exploratory Data Analysis
EDA involved exploring the sales data to answer key questions, such as:

- Weekly sales by store and date.
- Effect of fuel price on weekly sales by date.
- What are the top performing store.
- What is the impact of holiday flag on weekly sales.

### Data Analysis
Interesting code/features worked with:

```sql
--Weekly sales by store and date.

select top 10 store, date, avg(weekly_sales) as sales_by_week
from walmart
group by store, date
order by sales_by_week desc;
```

```sql
--Effect of fuel price on weekly sales by date

select fuel_price, sum(weekly_sales) as totalsales
from walmart
group by fuel_price
order by totalsales desc;
```

```sql
--What are the top performing store

select store, sum(weekly_sales) as totalsales
from walmart
group by store
order by totalsales desc;
```

```sql
--What is the impact of holiday flag on weekly sales

select holiday_flag, avg(weekly_sales) as averagesales
from walmart
group by holiday flag
```

### Results And Findings

The potential findings are summarized as follows;
1. Weekly sales vary significantly across different CPIs(Consumer Price Index), indicating price sensitivity.
2. Holiday flags show increased sales during holidays, highlighting seasonal trends.
3. Sales patterns differ across quarters, possibly due to seasonal trends.

### Recommandations

Based on my analysis, i recommend the following actions:
- Run promotions during holidays and slow quarters to boost sales.
- Investigating underperforming stores and implement improvement strategies.
- Ensure adequate inventory levels during peak seasons.
- Continuously monitor and analyze sales data to inform business decisions.
  

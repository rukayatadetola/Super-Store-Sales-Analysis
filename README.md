# Super Store Sales Analysis | Revenue, Trends and Insights
Excel + Python + Power BI Project
## Table of Content
1. [Project Overview](##1-Project-Overview)
2. [Business Objectives](##2-Business-Objectives)
3. [Tools & Technologies](##3-Tools-Technologies)
4. [Excel for Data Formatting & Pre-Processing](##4-Excel-for-Data-Formatting-&-Pre-Processing)
5. [ Python Analysis Breakdown](##5-Python-Analysis-Breakdown)
6. [Power BI Dashboard](##6-Power-BI-Dashboard)

## Project Overview
This project analyzes sales performance, profitability, customer segments, product categories, shipping methods, and regional performance.

The project combines Python for data cleaning with Power BI for interactive data visualization and dashboard development.

The goal of this project is to transform raw Superstore sales data into meaningful business insights that can help stakeholders understand what is driving sales and profit, which products and regions perform best, and where there are opportunities for improvement.

## Business Objectives

The analysis was designed to answer key business questions such as:

- What is the company's overall sales and profit performance?
- Which regions generate the highest sales?
- Which customer segments contribute the most to revenue?
- Which product categories and sub-categories perform best?
- How do sales and profit change throughout the year?
- Which shipping mode is used most frequently?
- Which states contribute significantly to sales and profit?


## Tools & Technologies

1. **Python** (Python was used for data preparation, cleaning, exploration, and analysis.)
2. **Excel**(Data formatting, cleaning & pre-processing)
3. **Power BI** (To create the interactive dashboard and communicate the findings visually.)

## Excel for Data Formatting & Pre-Processing
- Cleaned missing values and duplicates.
- Excel used for quick and efficient pre-processing before import it to jupyter notebook

![SuperStore Analysis Dataset on Excel](https://github.com/rukayatadetola/Super-Store-Sales-Analysis/blob/main/Screenshot%202026-08-28%20181838.jpg)

###  Python Analysis Breakdown 

```Python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
```Python
df= pd.read_csv("C:\\Users\\Rukky\\Documents\\Sample_Superstore.csv",  encoding="cp1252")

df
```
```Python
--- Handled Missing Values---
df.isnull().sum()
```
```Python
--- Checked Data Type(dtypes)---
df.dtypes
```
### Feature Enginnering
``` Python
--- Data Types Conversion
Converting the date columns from their original format into Pandas datetime objects.---

--- ORDER DATE COLUMN---
df['Order Date']= pd.to_datetime(df['Order Date'])

--- SHIP DATE COLUMN---
df['Order Date']= pd.to_datetime(df['Order Date'])

--- Extracted Order Year And Order Month column From Order Date column----

---  Create Order Year Column ---
df['Order Year']= df['Order Date'].dt.year

---  Create Order Month Column ---
df['Order month']= df['Order Date'].dt.month
```

## Power BI DASHBOARD

The Power BI dashboard was designed to provide an interactive view of business performance.

Users can interact with the dashboard through the Region filter, allowing them to explore performance for:

-Central
-East
-South
-West

The dashboard combines KPI cards, charts, geographic analysis, and interactive filters into a single reporting interface.

![SuperStore Analysis Dashboard on Power BI Visualization](https://github.com/rukayatadetola/Super-Store-Sales-Analysis/blob/main/Screenshot%202026-09-01%20103341.jpg)

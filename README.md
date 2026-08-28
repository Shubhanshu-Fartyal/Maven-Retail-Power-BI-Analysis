# Maven Retail Dashboard Power BI

## Project Overview

This project analyzes sales data from a global electronics retailer using **Microsoft Power BI**.

The objective was to transform and model the data, create DAX measures, and build interactive dashboards that answer key business questions related to revenue, profitability, product performance, customer behavior, and store performance.

**Part 1 :** 
https://github.com/Shubhanshu-Fartyal/maven-retail-analytics-sql

**Part 2 :**
https://github.com/Shubhanshu-Fartyal/maven-retail-dashboard-excel

> **Part 3 of the Maven Retail End-to-End Analytics Project**

This repository focuses specifically on the **Business Intelligence and dashboarding stage** of the larger analytics project.

---

## Dashboard Pages

The Power BI report consists of three analytical pages.

### 1. Executive Overview

Provides a high-level view of overall business performance.

Key metrics and analysis include:

- Total Revenue
- Total Profit
- Total Orders
- Total Customers
- Profit Margin %
- Revenue trends over time
- Top revenue-generating products
- Revenue by country
- Revenue by store type
- Revenue by product category

---

### 2. Product Performance Analysis

Focuses on financial and sales performance across products, brands, and categories.

Key analysis includes:

- Average Selling Price
- Profit per Order
- Average Profit Margin
- Distinct Products Sold
- Revenue and Profit by Year
- Total Profit by Category
- Revenue Contribution by Brand
- Brand-level performance analysis
- Total Quantity Sold by Category

---

### 3. Customer & Store Insights

Analyzes customer behavior, geographical performance, and store channel distribution.

Key analysis includes:

- Revenue per Customer
- Online Revenue %
- Physical Revenue %
- Orders per Customer
- Customer-level performance
- Revenue by Continent
- Revenue distribution by Country and Store Type
- Average Order Value trends
- Customer distribution by Continent

---

## Dashboard Preview

### Executive Overview

<img width="1123" height="631" alt="Screenshot 2026-08-23 181512" src="https://github.com/user-attachments/assets/3f3bb68e-1181-40a7-b486-026fcbe8952a" />

### Product Performance Analysis

<img width="1124" height="637" alt="Screenshot 2026-08-23 181359" src="https://github.com/user-attachments/assets/7c2c9c5f-063e-45cd-9bec-8a6e13f0c28f" />

### Customer & Store Insights

<img width="1121" height="632" alt="Screenshot 2026-08-23 181221" src="https://github.com/user-attachments/assets/da0600cc-b06d-4560-9d0f-431ee1fee264" />

---

## Dataset

- **Source:** Maven Analytics Data Playground
- **Domain:** Global Electronics Retail
- **Dataset Type:** Relational (Star Schema)

**Data Source:** https://mavenanalytics.io/data-playground/global-electronics-retailer

### Tables Used

| Table | Description |
|-------|-------------|
| Sales | Transactional sales data (Fact Table) |
| Customers | Customer information |
| Products | Product catalog |
| Stores | Store information |
| Dim_Date | Stores date information |
| Exchange_Rates | Daily currency exchange rates |


<img width="707" height="446" alt="Screenshot 2026-08-28 163833" src="https://github.com/user-attachments/assets/c7eac380-3632-4311-a4d9-96801c6cb1c1" />
---

## Data Transformation

Data was transformed and prepared in **Power Query** before analysis.

Key transformation activities included:

- Reviewing and correcting data types
- Converting date columns to appropriate date formats
- Handling columns with missing values
- Preparing numerical and financial fields for analysis
- Creating a clean analytical model from the source tables

---

## Data Model

The project uses a relational data model with **Sales** as the primary fact table.

### Fact Table

- Sales

### Dimension Tables

- Customers
- Products
- Stores
- Exchange Rates
- DimDate

Relationships were created between the Sales table and the relevant dimension tables to support filtering and analysis across the report.

A dedicated **DimDate** table was also used to support time-based analysis.

---

## Key DAX Measures

The dashboard uses DAX measures to calculate business KPIs and analytical metrics.

Examples include:

- Total Revenue
- Total Profit
- Total Orders
- Total Customers
- Total Quantity
- Profit Margin %
- Average Selling Price
- Profit per Order
- Revenue per Customer
- Online Revenue %
- Physical Revenue %
- Orders per Customer
- Average Order Value

---

## Key Insights

- The business generated approximately **$55.76 million in total revenue**.
- Total profit reached approximately **$32.66 million**, resulting in an overall profit margin of **58.58%**.
- Revenue peaked in **2019**, making it the strongest year in the available dataset.
- **Computers** was the highest revenue and profit-generating product category.
- **Adventure Works** was the leading brand by total revenue.
- The **United States and North America** were the strongest geographical contributors to revenue.
- Physical stores generated approximately **79.55% of total revenue**, compared with approximately **20.45% from online sales**.
- Customer distribution was concentrated primarily in **North America**, followed by Europe.
- Average Order Value declined from 2016 to 2019 before recovering in the following years.

---

## Project Structure

```text
Maven-Retail-Dashboard-PowerBI/
│
├── dashboard/
│   ├── executive_overview.png
│   ├── product_performance_analysis.png
│   └── customer_store_insights.png
│
├── documentation/
│   ├── data_transformation.md
│   ├── data_model.md
│   ├── dax_measures.md
│   └── key_insights.md
│
├── powerbi/
│   └── Maven_Retail_PowerBI_Analysis.pbix
│
└── README.md

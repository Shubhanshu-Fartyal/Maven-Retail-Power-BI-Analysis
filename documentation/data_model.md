# Data Model

## Overview

The Power BI report uses a relational data model designed to connect transactional sales data with customer, product, store, currency, and date information.

The model uses **Sales as the central fact table**, with supporting dimension tables connected through key fields.

---

## Model Structure

### Fact Table

**Sales**

Contains transactional sales information, including:

- Order Number
- Order Date
- Delivery Date
- Customer Key
- Product Key
- Store Key
- Currency Code
- Quantity
- Line Item

---

### Dimension Tables

**Products**

Contains product-level information such as:

- Product Key
- Product Name
- Brand
- Category
- Subcategory
- Color
- Unit Cost USD

**Customers**

Contains customer information such as:

- Customer Key
- Name
- Gender
- Birthday
- City
- State
- Country
- Continent

**Stores**

Contains store information such as:

- Store Key
- Country
- State
- Square Meters
- Open Date

**Exchange_Rates**

Contains currency exchange information by:

- Currency
- Date
- Exchange Rate

**DimDate**

A dedicated date dimension used for time-based analysis.

It contains:

- Date
- Month
- Month Number
- Quarter
- Year

---

## Relationships

The Sales table is connected to the dimension tables using their corresponding key fields.

```text
Products ─────────┐
                  │
Customers ────────┤
                  │
Stores ───────────┼──── Sales
                  │
DimDate ──────────┤
                  │
Exchange_Rates ───┘

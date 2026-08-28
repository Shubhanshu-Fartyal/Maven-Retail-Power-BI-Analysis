# DAX Measures

## Overview

DAX measures were created in Power BI to calculate the key business metrics used across the three dashboard pages.

The measures are based primarily on the **Sales** table and respond dynamically to filters applied through the data model.

---

## Core Sales Measures

### Total Revenue

```
Total Revenue =
SUM(Sales[Revenue])
```

Calculates total sales revenue.

**### Total Revenue**

Total Profit =
SUM(Sales[Profit])

Calculates total profit generated from sales.

Total Orders
Total Orders =
DISTINCTCOUNT(Sales[Order Number])

Counts unique orders rather than individual transaction rows.

Total Customers
Total Customers =
DISTINCTCOUNT(Sales[CustomerKey])

Counts the number of unique customers.

Total Quantity
Total Quantity =
SUM(Sales[Quantity])

Calculates the total number of units sold.

Profitability Measures
Profit Margin %
Profit Margin % =
DIVIDE([Total Profit], [Total Revenue])

Calculates profit as a percentage of revenue.

Profit per Order
Profit per Order =
DIVIDE([Total Profit], [Total Orders])

Calculates the average profit generated per order.

Product Measures
Average Selling Price
Average Selling Price =
DIVIDE([Total Revenue], [Total Quantity])

Calculates the average revenue generated per unit sold.

Total Products Sold
Total Products Sold =
DISTINCTCOUNT(Sales[ProductKey])

Calculates the number of distinct products appearing in the sales data.

Customer Measures
Revenue per Customer
Revenue per Customer =
DIVIDE([Total Revenue], [Total Customers])

Calculates the average revenue generated per customer.

Orders per Customer
Orders per Customer =
DIVIDE([Total Orders], [Total Customers])

Calculates the average number of orders placed per customer.

Average Order Value
Average Order Value =
DIVIDE([Total Revenue], [Total Orders])

Calculates the average revenue generated per order.

Store / Channel Measures
Online Revenue %
Online Revenue % =
DIVIDE(
    CALCULATE(
        [Total Revenue],
        Stores[Country] = "Online"
    ),
    [Total Revenue]
)

Calculates the percentage of revenue attributed to the online channel.

Physical Revenue %
Physical Revenue % =
DIVIDE(
    CALCULATE(
        [Total Revenue],
        Stores[Country] <> "Online"
    ),
    [Total Revenue]
)

Calculates the percentage of revenue attributed to physical stores.

DAX Functions Used

The project uses several commonly used DAX functions:

SUM
DISTINCTCOUNT
DIVIDE
CALCULATE

These measures were used to create KPI cards, charts, tables, and other interactive dashboard visuals.

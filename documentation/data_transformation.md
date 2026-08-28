# Data Transformation

## Overview

The dataset was prepared for analysis using **Power Query in Microsoft Power BI**.

The transformation process focused on ensuring that the data had appropriate data types and was ready for building a relational data model and performing DAX calculations.

---

## Source Tables

The Power BI model uses the following source tables:

- Sales
- Customers
- Products
- Stores
- Exchange Rates

A separate **DimDate** table was also created for time-based analysis.

---

## Data Type Corrections

The source data was reviewed and relevant columns were assigned appropriate data types.

Key changes included:

| Column | Original Type | Updated Type |
|---|---|---|
| Delivery Date | Text | Date |
| Square Meters | Text | Whole Number |

Financial and numerical columns were also assigned appropriate numeric data types to support calculations and reporting.

These included fields related to:

- Unit Cost
- Unit Price
- Revenue
- Total Cost
- Profit
- Profit Margin
- Quantity

---

## Data Quality Considerations

### Delivery Date

The `Delivery Date` column contained a significant number of missing values.

The column was still converted to the **Date** data type because valid delivery records needed to remain available for potential analysis.

Missing values were retained rather than replaced with artificial values.

### Square Meters

The `Square Meters` field was converted from text to a **Whole Number** to ensure it could be correctly used for numerical analysis.

---

## Date Table

A dedicated **DimDate** table was created to support time-based analysis.

The table includes:

- Date
- Month
- Month Number
- Quarter
- Year

The date dimension was connected to the Sales table to support analysis across different time periods.

---

## Outcome

After transformation, the data was ready for:

- Relational data modeling
- Creating relationships between fact and dimension tables
- DAX calculations
- KPI development
- Time-based analysis
- Interactive dashboard reporting

The transformed dataset was then used to build the Power BI data model and the three-page analytics dashboard.

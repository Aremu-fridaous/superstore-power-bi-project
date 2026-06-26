# Superstore Power BI Project
End-to-end Power BI project using the Superstore dataset — covering data cleaning, star schema data modeling, DAX measures, and an interactive Sales & Profit dashboard.

## Project Overview
This project analyzes sales and profit performance using the Kaggle Superstore dataset. The goal was to take a single flat file and build it into a fully modeled, analysis-ready Power BI report.

## Process
**1. Data Cleaning (Power Query)**
- Fixed date columns using locale-based formatting (US date format)
- Corrected data types (Customer ID, Postal Code, Product ID set to Text)
- Checked for blanks, duplicates, and inconsistent values

**2. Data Modeling (Star Schema)**
- Built dimension tables: dim_customer, dim_product, dim_location, dim_date, dim_ship_mode
- Connected all dimensions to fact_sales in a proper one-to-many star schema
- **Resolved a data quality issue**: discovered that Product ID was not actually unique — the same ID was reused for different products. Fixed this by creating a composite "Product Key" (Product ID + Product Name) to ensure accurate relationships.

**3. DAX Measures**
- Total Sales, Total Profit, Total Quantity, Profit Margin, Average Discount

**4. Dashboard**
- KPI cards, Sales & Profit trend by month, Category breakdown, Regional map, Top 10 Customers, Ship Mode distribution

## Files
- `My Assessment.pbix` — the full Power BI file
- `Sales Modelling.png` — data model screenshot
- `Sales & Profit dashboard.png` — final dashboard screenshot

## Tools Used
Power BI Desktop, Power Query, DAX

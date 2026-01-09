# MB1_Company Analysis Dashboard

## Overview
This project is a comprehensive analysis of MB1_Company's sales data, designed to demonstrate advanced Excel data modeling, cleaning, and visualization skills. The goal was to simulate a real-world scenario where a Data Analyst is tasked with generating actionable insights from raw transactional data.

---

## Dataset
The project uses five interconnected datasets:

1. **Products** – Product details including `Product_ID`, `Product_Name`, `Category`, `Cost`, and `Price`.
2. **Customers** – Customer demographics including `Customer_ID`, `Name`, `Gender`, `Age`, `City`, and `Signup_Date`.
3. **Orders** – Orders data including `Order_ID`, `Customer_ID`, `Order_Date`, `Payment_Method`, and `Order_Status`.
4. **Order_Details** – Order line items with `Order_ID`, `Product_ID`, `Quantity`, and `Discount`.
5. **Calendar** – Date dimension for time-based analysis.

### Data Cleaning & Transformation
- Fix negative product prices from `Products` table.
- Replaced missing or null values in `Customers` (e.g., `Age` defaulted to 37, capitalized `City` names, standardized `Gender` values).
- Fixed `Order_Date` and `Signup_Date` data types.
- Added calculated columns in `Order_Details`:
  - **Revenue** = IF(Order Delivered) × Price × Quantity
  - **Discount_Amount** = Revenue × Discount
  - **Net_Sales** = Revenue - Discount_Amount
  - **Profit** = Net_Sales - (Cost × Quantity) for delivered orders

---

## Data Model
- Star schema with `Order_Details` as the fact table.
- Relationships:
  - `Order_Details[Order_ID]` → `Orders[Order_ID]`
  - `Order_Details[Product_ID]` → `Products[Product_ID]`
  - `Orders[Customer_ID]` → `Customers[Customer_ID]`
  - `Orders[Order_Date]` → `Calendar[Date]`

---

## Dashboard Overview
- **KPIs**: Delivered Orders Rate, Cancelled Orders Rate, Returned Orders Rate, Net Sales, Total Profit.
- **Visualizations**:
  - **Line Chart**: Monthly Sales Trend for 2023
  - **Pie Chart**: Profit by Category
  - **Bar Chart**: Top 10 Products by Profit
  - **Bar Chart**: Cities Performance
- **Slicers**: Date, City, Category for interactive filtering.

---

## Key Insights
- Electronics category is the most profitable.
- Higher discount rates correlate with lower profit.
- Top 10 products contribute significantly to overall profit.
- Alexandria and Cairo generate the highest profit among cities.
- Delivered orders constitute ~74.5% of total orders.

---

## Tools & Skills Used
- Microsoft Excel (Power Pivot, PivotTables, Slicers)
- Data Cleaning & Transformation
- DAX Calculated Columns
- Interactive Dashboard Design
- Data Modeling (Star Schema)
- Analytical Reasoning & Insights Extraction

---

## Project Purpose
This project demonstrates the ability to:
- Clean and transform raw data
- Build a relational data model
- Calculate metrics using DAX
- Design professional, interactive dashboards
- Extract actionable business insights

---

# SUMMARY

This project explores sales performance using the Superstore dataset (2014–2018) with Excel, MySQL (SQL), and Power BI. The aim was to analyze sales across regions, identify customer and product performance, and visualize trends over time.

Key findings:

  •	Technology products contributed the largest share of revenue (~45%).
  •	West and East regions generated the highest sales, while the South lagged.
  •	Discounting strategies boosted sales volume but reduced profit margins.
  •	Top 5 customers accounted for a significant share of revenue.
  •	Q4 months consistently recorded peak sales, showing seasonal buying patterns.
  
The report documents how the tools (Excel, SQL, and Power BI) together provide an end-to-end analytical workflow, from data cleaning to querying, and finally, to interactive dashboard storytelling.


# INTRODUCTION

The Superstore dataset is a popular sample dataset that records customer orders, sales, profit, and product details between 2014 and 2018.
The objectives of this project were to:

1.	Clean and explore data using Excel.
2.	Write SQL queries to derive insights into customer spend, sales trends, and segmentation.
3.	Build a Power BI dashboard to communicate findings visually.

By combining these tools, this project shows the ability to handle data at different stages: preparation, querying, and visualization.

# METHODOLOGY

## EXCEL

•	Data Cleaning: Removed duplicates, standardized date formats, ensured numeric consistency in sales and profit, and trimmed customer names.
•	Calculations: Created a calculated column for Customer Spend using SUMIF and Average Order Value using total sales ÷ total orders.
•	Pivot Tables: Built summaries of Sales by Region, Sales by Category, and Top Customers.

## SQL

•	Database Creation: Designed schema with fact table (Orders) and dimension tables (Customers, Products).
•	Queries:
  o	Total sales by region and month using GROUP BY and MONTH.
  o	Top 5 customers by spend using SUM(Sales) and ORDER BY DESC.
  o	Customer segmentation (Low, Medium, High spend tiers) using CASE WHEN.

## POWER BI

•	Data Modeling: Imported cleaned data, created FactOrders, DimCustomers, DimProducts, and Date tables, and defined relationships.
•	DAX Measures:
  o	Total Sales = SUM(Orders[Sales])
  o	Total Profit = SUM(Orders[Profit])
  o	AOV = DIVIDE([Total Sales], DISTINCTCOUNT(Orders[OrderID]))
  o	Customer Segment Count = DISTINCTCOUNT(DimCustomers[Segment])
•	Dashboard Visuals:
  o	KPIs (Revenue, Quantity, AOV, Segments)
  o	Sales by Region (bar chart)
  o	Monthly Sales & Profit trends (line chart)
  o	Revenue by Category (pie chart)
  o	Top Customers by Spend (bar chart)


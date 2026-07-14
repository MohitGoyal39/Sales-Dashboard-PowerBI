# Retail Sales Performance Dashboard — Power BI

A 3-page Power BI report analyzing FY2023–2024 retail sales — tracking revenue, profit margin, and regional performance, with a dedicated insights page turning data into recommendations.

## Preview
![Executive Overview](Executive%20Overview.png)
![Product Performance](Product%20Analysis.png)
![Key Insights](key%20insights.png)

## Features
- Executive Overview, Product Performance, and Key Insights pages
- DAX-driven RAG conditional formatting on profit margin
- YoY revenue comparison, regional and category breakdowns
- Top/Bottom 10 product analysis by revenue and margin

## Key DAX Measures
```dax
Total Revenue = SUM(Fact_Sales[Revenue])
Total Profit = SUM(Fact_Sales[Profit])
Profit Margin = DIVIDE([Total Profit], [Total Revenue])
```
RAG thresholds: 🔴 <20% · 🟡 20–30% · 🟢 >30%

## Data Model
Star schema — Fact_Sales linked to Dim_Product, Dim_Region, Dim_Date.

## Tools
Power BI · DAX · Power Query

<img width="557" height="566" alt="Page1" src="https://github.com/user-attachments/assets/73beab8e-4f9c-493a-9e95-3e9e0011da68" />

<img width="566" height="451" alt="page 2" src="https://github.com/user-attachments/assets/a9852f5a-41cf-46d6-8298-ecde50913adc" />

# Brazilian E-Commerce (Olist) Analytics Dashboard

An end-to-end Business Intelligence project developed using Power BI to transform a complex, multi-table relational dataset into an interactive analytics dashboard. This project focuses on identifying logistics bottlenecks, understanding customer refund triggers, and evaluating regional sales performance across Brazil.

The project demonstrates my ability to perform data transformation, build optimized data models, create advanced DAX measures, and design dashboards that deliver actionable business insights.

---

## Project Overview

The Olist dataset is a real-world, anonymized Brazilian e-commerce dataset containing transactional records from 2016 to 2018. The dataset includes information about customers, sellers, products, payments, reviews, and delivery timelines.

Because the data is distributed across multiple related tables, this project required a strong focus on data engineering, relational modeling, and analytical calculations.

In this project, I:

- Cleaned and transformed raw data using Power Query
- Handled missing values and duplicate records
- Standardized inconsistent city and state names
- Built an optimized Star Schema data model
- Created custom calendar tables for time-series analysis
- Developed advanced DAX measures
- Designed an interactive dashboard for business decision-making

The final dashboard provides insights into delivery performance, profit margins, refund risks, and regional sales trends.

---

## Objectives

The primary goals of this project are:

- To identify causes of delayed deliveries
- To analyze patterns associated with customer refunds and returns
- To evaluate profit margins across product categories
- To compare sales performance by region and state
- To demonstrate advanced Power BI skills in a real-world business scenario

---

## Dataset Description

The project uses the Brazilian E-Commerce Public Dataset by Olist, which contains several interconnected tables, including:

- Orders
- Order Items
- Customers
- Sellers
- Products
- Payments
- Reviews
- Geolocation Data

The dataset captures the complete order lifecycle, from purchase to delivery, enabling detailed operational and financial analysis.

---

## Data Cleaning and Transformation

All preprocessing was performed in Power Query using M Language.

### Missing Value Handling

- Identified and addressed null values in delivery and review-related columns
- Applied suitable replacement and filtering strategies
- Preserved data integrity for downstream analysis

### Data Standardization

- Cleaned inconsistent geographical names
- Converted data types to appropriate formats
- Removed duplicate and invalid records

### Feature Preparation

- Created new fields required for business metrics
- Structured data for efficient modeling and analysis

---

## Data Modeling and Architecture

To improve performance and ensure accurate filtering, the raw dataset was restructured into a Star Schema.

### Fact Table

- `fact_orders` containing transactional metrics such as price, freight cost, and order dates

### Dimension Tables

- `dim_customers`
- `dim_products`
- `dim_sellers`
- `dim_calendar`

### Relationships

- One-to-many relationships between dimensions and the fact table
- Single-direction cross-filtering to avoid ambiguity and optimize performance

This architecture significantly improved query speed and simplified measure creation.

---

## Custom DAX Measures and Calculated Columns

Several important business metrics were created using DAX.

### Calculated Column: Days to Ship

dax
DaysToShip =
DATEDIFF(
    'fact_orders'[order_purchase_timestamp],
    'fact_orders'[order_delivered_customer_date],
    DAY
)

Additional Measures
Total Revenue
Total Freight Cost
Average Delivery Time
Late Delivery Rate
Profit Margin Percentage
Refund Risk Score
Orders by State
Monthly Sales Growth

These measures enabled dynamic slicing and drill-down analysis across multiple business dimensions.

* Dashboard Features
* The Power BI dashboard includes:
KPI cards for revenue, profit margin, and delivery performance
Regional sales maps
Monthly trend analysis
Product category comparisons
Refund and review analysis
Interactive slicers for date, state, and category
Key Insights Discovered
Logistics Bottlenecks

Certain states consistently showed higher delivery times, indicating potential supply chain inefficiencies and transportation challenges.

*Refund Triggers
Orders with significant delivery delays and low review scores were much more likely to result in refund requests.

*Regional Performance
Sales were concentrated in a few major states, while some regions demonstrated strong growth potential but lower operational efficiency.

* Profit Margin Variability
Product categories differed significantly in profitability after accounting for freight and logistics costs.

* Technologies Used
Power BI Desktop
Power Query (M Language)
DAX (Data Analysis Expressions)
Data Modeling
Star Schema Design
Google Colab Notebook


* Skills Demonstrated
This project highlights practical skills in:
  Business Intelligence
  Data Transformation
  Power Query
  Data Modeling
  Star Schema Architecture
  DAX Calculations
  KPI Design
  Dashboard Development
  Operational Analytics
  Insight Generation
  Business Relevance

* The dashboard can help e-commerce businesses:
  Monitor delivery performance
  Reduce refund and return rates
  Optimize logistics operations
  Improve customer satisfaction
  Track profitability by region and category

* Conclusion:
  This project demonstrates my ability to transform raw relational data into a structured and highly interactive Business Intelligence solution. By combining Power Query, Star Schema design, and advanced DAX calculations, I created a dashboard that delivers meaningful operational and financial insights.

The Brazilian E-Commerce (Olist) Analytics Dashboard reflects my capability to solve real-world business problems through data transformation, modeling, and visualization using Power BI.

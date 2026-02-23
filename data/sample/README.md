# Retail Sales Intelligence and Demand Forecasting

## Problem
Retail teams need a reliable view of revenue, product performance, and customer behavior, along with short-term demand forecasts to support pricing, merchandising, and inventory decisions.

## Why it matters
This project demonstrates how raw ecommerce data can be transformed into trusted KPI tables, executive dashboards, and demand forecasts that support weekly business reviews across sales, marketing, finance, and product teams.

## Data
- Source: Olist Ecommerce Dataset (Kaggle)
- Size: ~100k orders across multiple tables
- Grain: order line item
- Time range: 2016 to 2018
- Refresh: batch ingestion (simulated daily loads)
- Notes: anonymized customer data, currency normalized for analysis

## Approach
1. Ingest raw CSV data and load into warehouse tables
2. Clean and standardize fields with validation checks
3. Build dimensional models and KPI marts using dbt
4. Publish BI dashboards for executive and functional views
5. Train demand forecasting models on daily sales
6. Write forecasts back to the warehouse for reporting
7. Add tests and documentation for reproducibility

## Tech stack
SQL, Python, dbt, Snowflake, Airflow, AWS, Tableau or Power BI

## Key insights and metrics
- Revenue trends and seasonality patterns
- Top products by revenue and margin proxy
- Customer repeat rate and cohort retention
- Forecast accuracy measured using MAE and MAPE
- Identification of high-return SKUs impacting profitability

## Deliverables
- Dimensional warehouse models (fact_orders, dim_customer, dim_product, dim_date)
- KPI marts (mart_daily_sales, mart_product_kpis, mart_customer_cohorts)
- Executive BI dashboard with revenue, customer, and product views
- 28-day demand forecast table
- dbt tests and documentation

## How to run locally
1. Clone the repository
2. Create a virtual environment
3. Install dependencies from requirements.txt
4. Run ingestion and cleaning scripts
5. Execute dbt models and tests
6. Generate forecasts and publish results
7. Open dashboard screenshots for reference

## Next improvements
- Incremental dbt models with partitioning
- Anomaly detection for revenue spikes and drops
- Alerting on forecast error and stockout risk
- Integration with live ecommerce APIs

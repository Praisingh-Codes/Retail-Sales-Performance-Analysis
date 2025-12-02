## Retail Sales Data Warehouse & Analytics System

![Project Poster](resources/retail%20sales%20performance%20analysis%20poster%20image.png)

#### Project Overview

This project demonstrates a full analytics pipeline built entirely with SQL Server—from database creation, schema design, ETL ingestion, and dimensional modeling to advanced analytical reporting.

A structured set of SQL scripts performs:

- Database & schema setup

- Dimension & fact table exploration

- Date, magnitude, and performance insights

- Customer & product segmentation

- Trend analysis

- Part-to-whole contribution analysis

- Complete customer & product analytical reporting

Each module is saved as a SQL script + a CSV export for documentation and verification.

#### Tech Stack

- SQL Server (T-SQL)

- Data Warehouse Modeling (Fact & Dim tables)

- Analytical SQL (WINDOW functions, CTEs, Aggregations)

- CSV Exports for reporting

#### Architecture Diagram

This diagram illustrates the end-to-end flow of the Retail Sales Performance Analysis system.

![Architecture Diagram](resources/architecture%20diagram%20image.png)

#### Project Structure

-- Database Creation & Exploration

- Create database & schemas

- Create dimension and fact tables

- Bulk load CSV data

- Explore metadata via INFORMATION_SCHEMA

- Validate columns, tables, structure

✔ Outputs: 01_database_exploration_(i).csv, (ii).csv

-- Dimensions Exploration

- Unique country distribution (customers)

- Product category / subcategory analysis

- Attribute discovery across dimensions

✔ Outputs: 02_dimensions_exploration_(i).csv, (ii).csv

-- Date Range Analysis

- First & last order date

- Customer age profile

- Years and months of historical data

- Lifespan exploration

✔ Outputs: 03_date_range_exploration_(i).csv, (ii).csv

-- Measures Exploration

Core KPI calculations:

- Total sales

- Average price

- Total quantity

- Total customers

- Total products

- Distinct orders

- Composite KPI summary table

✔ Outputs: 04_measures_exploration_(i–viii).csv

-- Magnitude Analysis

Aggregations grouped by key business dimensions:

- Customers by country

- Customers by gender

- Products by category

- Revenue by category

- Revenue by customer

- Items sold by geography

✔ Outputs: 05_magnitude_analysis_(i–vii).csv

-- Ranking Analysis

- Top N products

- Worst-performing products

- Top customers by revenue

- Low-frequency customers

- Monthly product ranking

✔ Outputs: 06_ranking_analysis_(i–iv).csv

-- Change Over Time Analysis

Time-series analysis:

- Monthly performance

- Trend detection

- YoY comparisons

- MoM comparisons

✔ Outputs: 07_change_over_time_analysis_(i–iv).csv

-- Cumulative Analysis

Cumulative & rolling metrics:

- Running totals

- Rolling averages

- Cumulative KPIs

- Customer-level cumulative spend

✔ Outputs: 08_cumulative_analysis.csv

-- Performance Analysis

- Compare product sales vs average

- YoY changes

- Performance flags

- Growth detection

✔ Outputs: 09_performance_analysis.csv

-- Part-to-Whole Analysis

Contribution analysis:

- Category contribution to total sales

- Cumulative contribution (Pareto)

- Percentage share metrics

✔ Outputs: 10_part_to_whole_analysis.csv

-- Data Segmentation

Segmentation rules:

- Product segmentation (cost-based)

- Customer segmentation (VIP, Regular, New)

- Lifespan, spending, recency buckets

- RFM-style metrics (optional)

✔ Outputs: 11_data_segmentation_(i).csv, (ii).csv

-- Customer Report

A consolidated analytical report including:

- Demographics & age groups

- Customer segments

- Orders, sales, quantity

- Recency (months since last order)

- Average order value

- Average monthly spend

✔ Outputs: 12_customers_report_(i).csv, (ii).csv

-- Product Report

A complete product-level report:

- Category & subcategory metadata

- Cost & price intelligence

- Orders, quantity, customers

- Recency

- High/Mid/Low Performer segmentation

- Average monthly revenue

- Average order revenue

✔ Outputs: 13_products_report.csv

#### Key SQL Concepts Used

- Window Functions: LAG(), LEAD(), ROW_NUMBER(), RANK(), SUM() OVER(), AVG() OVER()

- Date Functions: DATEPART(), DATEDIFF(), DATETRUNC()

- Aggregations: SUM(), COUNT(), AVG(), MIN(), MAX()

- Joins & CTEs

- Segmentation using CASE

- Trend, performance, cumulative & part-to-whole analytics

#### How to Use This Project

1️⃣Run the database creation script (00_create_database_and_schemas.sql).

2️⃣Import all CSV datasets via BULK INSERT.

3️⃣Execute each exploration SQL script in order (01 → 13).

4️⃣Review generated views:

- gold.report_customers

- gold.report_products

5️⃣Use CSV outputs for documentation or BI visualization.

#### Business Impact

This project allows the organization to:

- Identify most valuable customers

- Optimize product performance

- Monitor sales trends

- Detect seasonal patterns

- Conduct regional comparisons

- Build dashboards or BI apps from SQL-generated outputs

#### Contributing

Contributions are welcome!  

If you’d like to improve this project, follow the steps below:

1. Fork the Repository

Click the **Fork** button at the top right of this page to create your own copy.

2. Clone Your Fork
   
        git clone https://github.com/Praisingh-Codes/Retail-Sales-Performance-Analysis.git

3. Create a New Branch

        git checkout -b feature/your-feature-name

4. Make Your Changes

- Improve SQL scripts

- Add better documentation

- Fix bugs

- Add diagrams or enhance analysis

- Optimize queries or add new modules

5. Commit & Push

        git add .

        git commit -m "Add: description of your change"

        git push origin feature/your-feature-name

6. Submit a Pull Request

Open a PR to the main branch with:

- Clear title

- Explanation of the changes

- Screenshots or diagrams (if relevant)

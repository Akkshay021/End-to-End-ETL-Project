# End-to-End-ETL-Project
ETL Project Using Python and SQL
This project demonstrates the basics of an ETL (Extract, Transform, Load) process using Python and SQL. The dataset contains retail order information, which is downloaded from Kaggle, cleaned, transformed, and loaded into a SQL Server database. The project also includes SQL queries to perform data analysis and answer business-related questions, showcasing the seamless integration of Python and SQL in a data engineering workflow.

# ETL Project Using Python and SQL

## Overview
This repository demonstrates the implementation of an ETL (Extract, Transform, Load) pipeline using Python and SQL. The project is designed to process a retail dataset, clean and transform it, and then load the processed data into a SQL Server database for further analysis.

## Objectives
- Understand the ETL process.
- Utilize Python for data extraction, transformation, and loading.
- Leverage SQL for data storage and advanced business analysis.

## Dataset
The dataset used in this project is sourced from Kaggle: [Retail Orders Dataset](https://www.kaggle.com/ankitbansal06/retail-orders). It contains retail order information with attributes such as order ID, order date, ship mode, product details, and pricing.

## Steps
1. **Extract:**
   - The dataset is downloaded from Kaggle and extracted from a zipped folder.

2. **Transform:**
   - Cleaned column names for consistency.
   - Handled missing and undesirable values.
   - Added new columns (e.g., `sales_price`, `profit`).
   - Dropped irrelevant columns.
   - Converted `order_date` to a suitable `datetime` format.

3. **Load:**
   - Connected to a SQL Server database using SQLAlchemy.
   - Loaded the transformed data into a SQL table (`df_orders`).

4. **Analyze:**
   - Performed advanced SQL queries to answer business questions.
   - Utilized SQL functions, joins, and date-based queries for insights.

## Dependencies
- Python 3.x
- Libraries:
  - pandas
  - numpy
  - sqlalchemy
  - kaggle
  - zipfile
- SQL Server with ODBC Driver 17 for SQL Server

## SQL Table Schema
```sql
CREATE TABLE df_orders (
    [order_id] INT PRIMARY KEY,
    [order_date] DATE,
    [ship_mode] VARCHAR(20),
    [segment] VARCHAR(20),
    [country] VARCHAR(20),
    [city] VARCHAR(20),
    [state] VARCHAR(20),
    [postal_code] VARCHAR(20),
    [region] VARCHAR(20),
    [category] VARCHAR(20),
    [sub_category] VARCHAR(20),
    [product_id] VARCHAR(50),
    [quantity] INT,
    [discount] DECIMAL(7,2),
    [sales_price] DECIMAL(7,2),
    [profit] DECIMAL(7,2)
);


## Key Features
Demonstrates the end-to-end ETL process.
Highlights the integration of Python and SQL for data engineering tasks.
Provides examples of data cleaning, transformation, and loading.
Includes SQL scripts to analyze retail order data.

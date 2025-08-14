# Task 7 – Sales Data Summary using SQLite

## Overview
This task demonstrates how to create a simple SQLite database, insert product sales data, query it, and visualize the results using Python.

## Steps Performed
1. Created `sales_data.db` SQLite database and `sales` table.
2. Inserted sample sales records (product, quantity, price).
3. Ran SQL query to calculate **total quantity sold** and **total revenue** for each product.
4. Visualized the revenue by product using a bar chart.

## SQL Query
```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue
FROM sales
GROUP BY product
ORDER BY revenue DESC;
Files in this Repository
sales_data.db – SQLite database with sample sales data.

Task7_SQLite_Summary.ipynb – Colab/Jupyter notebook with full code.

sales_chart.png – Bar chart showing revenue by product.

Tools Used
Python (Pandas, SQLite3, Matplotlib)

SQLite Database

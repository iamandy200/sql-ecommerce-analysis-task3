# sql-ecommerce-analysis-task3
End-to-end SQL data analysis project featuring schema creation, data modeling, aggregate queries, joins, subqueries, views, and performance optimization. Fully executed using SQLite with screenshots and documentation.
📌 Overview

This project demonstrates SQL skills for data analysis using an E-commerce dataset.
The tasks include:

Creating tables

Inserting sample data

Running analytical SQL queries

Using joins, subqueries, GROUP BY, views, and indexes

Query optimization using EXPLAIN QUERY PLAN

Capturing results with screenshots

All queries were executed using SQLite (DB Browser for SQLite).

📁 Project Structure
Task3_SQL/
│-- ecommerce_schema_and_queries.sql
│-- README.md
└── screenshots/
      ├── screenshot1_revenue_per_order.png
      ├── screenshot2_avg_revenue_per_user.png
      ├── screenshot3_view_output.png
      └── screenshot4_explain_query_plan.png

🗂️ Database Tables

The database contains the following tables:

users

products

orders

order_items

A view was also created:

vw_order_revenue

Indexes were added for performance optimization.

⚙️ How to Run This Project (SQLite)
1. Install DB Browser for SQLite

Download: https://sqlitebrowser.org/dl/

2. Create a Database

Open DB Browser → New Database

Name it: ecommerce.db

Save it (do NOT add tables manually)

3. Execute SQL File

Go to Execute SQL →
Click Open File → Choose:

ecommerce_schema_and_queries.sql


Click Run All.
This will automatically:

Create tables

Insert sample data

Create a view

Create indexes

Run queries

🧠 Key SQL Concepts Demonstrated
✔ SELECT, WHERE, ORDER BY
✔ GROUP BY and Aggregate Functions
✔ INNER JOIN and LEFT JOIN
✔ Subqueries and CTEs
✔ View Creation
✔ Handling NULL values (COALESCE)
✔ Query Optimization using Indexes
✔ EXPLAIN QUERY PLAN
📝 Main Queries Executed
1. Revenue per Order

Calculates total revenue for each order.

2. Average Revenue per User

Uses a subquery to calculate revenue per user based on completed orders.

3. View: vw_order_revenue

Shows order-level revenue with order details.

4. EXPLAIN QUERY PLAN

Used to verify that the index on order_items(product_id) is being used.

📸 Screenshots Included
1️⃣ screenshot1_revenue_per_order.png

Shows output of:

SELECT oi.order_id, SUM(oi.quantity * oi.item_price) AS order_revenue
FROM order_items oi
GROUP BY oi.order_id
ORDER BY order_revenue DESC;

2️⃣ screenshot2_avg_revenue_per_user.png

Shows output of the subquery/CTE-based user revenue calculation.

3️⃣ screenshot3_view_output.png

Output of:

SELECT * FROM vw_order_revenue;

4️⃣ screenshot4_explain_query_plan.png

Shows index usage:
SEARCH oi USING INDEX ...
SEARCH o USING INTEGER PRIMARY KEY ...

🎯 Conclusion

This project demonstrates end-to-end SQL data analysis skills:

Database design

Query writing

Complex aggregations

Query optimization

Practical execution in SQLite

All required screenshots and outputs are included.

🙌 Author

Anand Rathod
BCA Graduate | Aspiring Data Analyst
Skills: Python, SQL, Pandas, AWS, Power BI

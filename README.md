# Retail Sales Performance Analysis & Business Insights

## Overview
This project analyzes retail sales data using SQL to evaluate sales performance, identify trends, and generate actionable business insights. The analysis focuses on revenue growth, product performance, and customer purchasing behavior.

**Project Status:** Completed

## Objectives
- Analyze overall sales performance
- Identify top-performing products and categories
- Understand customer purchase patterns
- Generate insights to support business decision-making

## Tools Used
- SQL (MySQL / PostgreSQL / SQLite)
- DB Browser / DBeaver

## Key Skills Demonstrated
- SQL Joins and Aggregations
- Business-Oriented Data Analysis
- Data Modeling and Relationships
- Insight Generation

## Dataset Description

The dataset represents retail sales transactions and includes:

- Customer details

- Product information

- Order and sales data

- Quantity, price, and order dates

## Database Setup
Database Name: **`retail_sales_db`**
### Tables

- customers – Stores customer details (ID, name, contact)

- products – Stores product details (ID, name, category, price, stock)

- orders – Stores sales transactions (order ID, customer ID, product ID, quantity, price, date)

## How to Run the Project
### 1. Create Database and Tables

```sql

CREATE DATABASE retail_sales_db;
USE retail_sales_db;

CREATE TABLE customers (
    customer_id INT PRIMARY KEY,
    customer_name VARCHAR(100),
    contact VARCHAR(50)
);

CREATE TABLE products (
    product_id INT PRIMARY KEY,
    product_name VARCHAR(100),
    category VARCHAR(50),
    price DECIMAL(10,2),
    stock INT

);

CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    customer_id INT,
    product_id INT,
    quantity INT,
    price DECIMAL(10,2),
    order_date DATE,
    FOREIGN KEY (customer_id) REFERENCES customers(customer_id),
    FOREIGN KEY (product_id) REFERENCES products(product_id)
);


```
### 2. Insert Sample Data

``` sql

INSERT INTO customers VALUES
(1, 'Amit Sharma', 'amit@gmail.com'),
(2, 'Neha Verma', 'neha@gmail.com'),
(3, 'Rahul Singh', 'rahul@gmail.com'),
(4, 'Pooja Mehta', 'pooja@gmail.com');

INSERT INTO products VALUES
(101, 'Laptop', 'Electronics', 55000, 40),
(102, 'Mobile Phone', 'Electronics', 25000, 80),
(103, 'Office Chair', 'Furniture', 7000, 30),
(104, 'Notebook', 'Stationery', 100, 200),
(105, 'Headphones', 'Electronics', 3000, 60);


INSERT INTO orders VALUES
(1001, 1, 101, 1, 55000, '2024-01-05'),
(1002, 2, 102, 2, 25000, '2024-01-08'),
(1003, 3, 103, 1, 7000, '2024-01-10'),
(1004, 1, 104, 10, 100, '2024-01-12'),
(1005, 4, 105, 3, 3000, '2024-01-15'),
(1006, 2, 101, 1, 55000, '2024-01-18');


```

## SQL Analysis Queries
### View All Data
```sql

SELECT * FROM customers;
SELECT * FROM products;
SELECT * FROM orders;


```

### Total Sales by Product Category
```sql

SELECT 
    p.category,
    SUM(o.quantity * o.price) AS total_sales
FROM orders o
JOIN products p ON o.product_id = p.product_id
GROUP BY p.category;


```
### Total Orders per Customer
```sql
SELECT 
    c.customer_name,
    COUNT(o.order_id) AS total_orders
FROM orders o
JOIN customers c ON o.customer_id = c.customer_id
GROUP BY c.customer_name;


```
### Top 5 Best-Selling Products


```sql
SELECT 
    p.product_name,
    SUM(o.quantity) AS total_quantity_sold
FROM orders o
JOIN products p ON o.product_id = p.product_id
GROUP BY p.product_name
ORDER BY total_quantity_sold DESC
LIMIT 5;


```
### Monthly Sales Trend
```sql
SELECT 
    MONTH(order_date) AS month,
    SUM(quantity * price) AS monthly_sales
FROM orders
GROUP BY MONTH(order_date)
ORDER BY month;


```


## Key Business Insights

- Electronics category generates the highest revenue, indicating strong demand.

- A small group of customers contributes significantly to total sales.

- High-performing products should be prioritized for inventory restocking.

- Monthly sales trends can help forecast demand and plan promotions effectively.

## Conclusion

This project demonstrates the practical application of SQL in retail business analysis. It showcases how structured queries, joins, and aggregations can transform raw transaction data into meaningful insights that support informed decision-making and business strategy.

## Author

Shanti Kumari Verma

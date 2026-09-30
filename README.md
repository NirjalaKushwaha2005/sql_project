# Week 2 SQL for Data Analysis

## Project Overview

This project is part of my Week 2 SQL for Data Analysis assignment. 
The project uses a sample orders database to analyze customer spending 
and calculate the average order value.

## Objective

The main objectives of this project are:

- Identify the top customers based on total spending.
- Calculate the average order value.
- Practice SQL aggregation and sorting techniques.

## Database

The project uses an `orders` table containing information such as:

- Order ID
- Customer Name
- Order Date
- Category
- Sub-Category
- Product Name
- Quantity
- Unit Price
- Total Price
- Region

## SQL Queries Used

### 1. Top Customers

```sql
SELECT
    customer_name AS `Top Customers`,
    SUM(total_price) AS `Total Spent`
FROM orders
GROUP BY customer_name
ORDER BY `Total Spent` DESC
LIMIT 10;

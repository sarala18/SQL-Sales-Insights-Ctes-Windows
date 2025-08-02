# SQL Sales Analysis Project

## Objective

This project aims to perform sales analysis using SQL, exploring customer behavior, order patterns, and business KPIs from raw sales data. It uses structured queries, CTEs, and window functions to extract insights valuable for decision-making.

---

## 📁 Dataset Structure

Three main CSV files are used:

- `customers.csv`: Customer details (name, age, city, signup date)
- `orders.csv`: Orders placed by customers with total amounts
- `order_items.csv`: Individual items in each order including category, quantity, and price per unit

---

## Tools & Technologies

- **SQL** (MySQL syntax)
- **CTEs and Window Functions**
- Data source: Simulated data in CSV format

---

## Key Analysis Performed

- Total sales by city and customer
- Top 5 customers by spending
- Order trends over time
- Product performance analysis
- Revenue contribution by category
- Window function usage: ranking, moving averages, etc.

---

## Sample Queries

```sql
-- Top 5 Customers by Spend
SELECT customer_name, SUM(total_amount) AS total_spent
FROM customers
JOIN orders USING(customer_id)
GROUP BY customer_name
ORDER BY total_spent DESC
LIMIT 5;

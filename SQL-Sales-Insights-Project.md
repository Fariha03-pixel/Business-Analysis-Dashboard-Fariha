# 📊 SQL Sales Insights Project  

## 🧠 Project Overview  
This project analyses sales performance data to identify key business insights, such as top-performing products, high-value customers, and monthly revenue trends.  
The goal is to simulate a real-world business analysis task and showcase SQL skills in data extraction, transformation, and reporting.  

---

## 🗂️ Dataset Information  
The dataset used represents a fictional company’s sales records with the following structure:  

| Column Name | Description |
|--------------|-------------|
| order_id | Unique identifier for each order |
| order_date | Date of purchase |
| customer_id | Unique identifier for each customer |
| region | Geographical region of sale |
| product | Product name |
| quantity | Number of items sold |
| unit_price | Price per item |
| total_sales | Total order value (quantity * unit_price) |

---

## 🧩 SQL Objectives  
This project focuses on answering key business questions using SQL queries:  
1. What are the **total sales by region**?  
2. What is the **monthly sales trend**?  
3. Who are the **top 5 customers by total spending**?  
4. What is the **average order value by region**?  

---

## 🧱 SQL Queries  

### 1️⃣ Total Sales by Region
```sql
SELECT 
    region,
    SUM(total_sales) AS total_sales_value
FROM sales
GROUP BY region
ORDER BY total_sales_value DESC;

SELECT 
    DATE_FORMAT(order_date, '%Y-%m') AS month,
    SUM(total_sales) AS monthly_sales
FROM sales
GROUP BY month
ORDER BY month;

SELECT 
    customer_id,
    SUM(total_sales) AS total_spent
FROM sales
GROUP BY customer_id
ORDER BY total_spent DESC
LIMIT 5;

SELECT 
    region,
    AVG(total_sales) AS avg_order_value
FROM sales
GROUP BY region
ORDER BY avg_order_value DESC;

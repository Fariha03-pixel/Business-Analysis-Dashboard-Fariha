# 🧠 SQL Sales Insights Project

## 📊 Project Overview
This project focuses on using SQL to analyse sales data and uncover key business insights such as revenue trends, customer behaviour, and product performance.  
It simulates how a Business Analyst or Data Analyst uses structured data to support decision-making.

## 🎯 Objective
To demonstrate SQL proficiency by writing queries that extract, clean, and summarise sales data — providing actionable insights for management reporting.

## 🧩 Tools Used
- **SQL (MySQL / PostgreSQL)** – For querying and data transformation  
- **Excel / Power BI** – For optional visualisation and report formatting  

## 📂 Dataset
A fictional dataset containing the following tables:
- **Customers**: Customer_ID, Name, Region, Age_Group  
- **Products**: Product_ID, Category, Unit_Price  
- **Orders**: Order_ID, Customer_ID, Product_ID, Quantity, Order_Date, Revenue  

*(If you use Kaggle or another open dataset later, just update this section with the link.)*

## 🧮 Key SQL Queries

### 1️⃣ Total Revenue by Product Category
```sql
SELECT 
    p.Category, 
    SUM(o.Revenue) AS Total_Revenue
FROM Orders o
JOIN Products p ON o.Product_ID = p.Product_ID
GROUP BY p.Category
ORDER BY Total_Revenue DESC;

SELECT 
    DATE_FORMAT(Order_Date, '%Y-%m') AS Month,
    SUM(Revenue) AS Monthly_Revenue
FROM Orders
GROUP BY Month
ORDER BY Month;

SELECT 
    c.Name AS Customer_Name,
    SUM(o.Revenue) AS Total_Spent
FROM Orders o
JOIN Customers c ON o.Customer_ID = c.Customer_ID
GROUP BY Customer_Name
ORDER BY Total_Spent DESC
LIMIT 5;


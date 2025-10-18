# 📊 Power BI Sales Dashboard Project  

## 🧠 Project Overview  
This Power BI project visualises key sales metrics and customer insights using interactive dashboards.  
It complements the **SQL Sales Insights Project** by transforming raw sales data into business intelligence visuals for decision-making.  

---

## 🎯 Project Objectives  
- Analyse overall sales performance across regions and time.  
- Identify top-performing products and customers.  
- Track monthly sales trends and customer behaviour.  
- Provide management with easy-to-understand visual insights.  

---

## 🗂️ Dataset Description  
The dataset represents a fictional retail company’s sales data, including:  

| Column Name | Description |
|--------------|-------------|
| Order ID | Unique transaction identifier |
| Order Date | Date of purchase |
| Region | Sales region |
| Product | Product sold |
| Customer ID | Unique customer code |
| Quantity | Number of items purchased |
| Total Sales | Total order amount |

---

## 🧰 Tools & Skills Used  
- **Power BI Desktop**  
- **Excel (Data Cleaning)**  
- **Power Query Editor** (for transformations)  
- **DAX (Data Analysis Expressions)**  
- **SQL** (for initial data preparation)  

---

## ⚙️ Data Cleaning & Transformation  
Performed in **Power Query Editor**:  
- Removed duplicates and null values  
- Converted date formats  
- Created calculated columns such as:  
  - `Month Name`  
  - `Year`  
  - `Profit Margin`  
- Added **measures** using DAX:  
  ```DAX
  Total Sales = SUM(Sales[Total Sales])
  Total Quantity = SUM(Sales[Quantity])
  Average Order Value = DIVIDE([Total Sales], [Total Quantity])


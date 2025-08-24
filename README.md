# 📊 Sales Analysis – Power BI Dashboard

## 📌 Project Overview
This Power BI project analyzes sales data for a retail business, providing insights into sales performance, product categories, regional distribution, and customer purchasing patterns. The dashboard enables data-driven decision making for sales strategy optimization.

---

## 📚 Table of Contents
- [Project Overview](#-project-overview)
- [Dataset](#-dataset)
- [Project Steps](#-project-steps)
- [Dashboard Preview](#-dashboard-preview)
- [Tools & Technologies](#-tools--technologies)
- [Key Insights](#-key-insights)
- [Conclusion](#-conclusion)
- [Contact Me](#-contact-me)
- [Acknowledgments](#-acknowledgments)

---

## 📂 Dataset
The dataset contains sales transactions with customer information, product details, and regional data stored in a SQL Server database. The database includes three main tables:
- **Customers**: Customer demographics and region information
- **Products**: Product details including categories and pricing
- **Sales**: Transaction records with quantities and dates
[📥 Download Dataset](https://github.com/HussienBedier1/Sales-Analysis-Power-BI-/blob/main/Sales%20Analysis.pbix)

---

## 📑 Project Steps

### Part 1 – SQL Server Database Setup
Created a sample database named SalesDB with the following tables:

1. **Customers Table**
   ```sql
   CREATE TABLE Customers (
     CustomerID INT PRIMARY KEY,
     CustomerName VARCHAR(100),
     Region VARCHAR(50)
   );
   ```

2. **Products Table**
   ```sql
   CREATE TABLE PRODUCTS (
     ProductID INT PRIMARY KEY,
     ProductName VARCHAR(100),
     Category VARCHAR(50),
     Price DECIMAL(10,2)
   );
   ```

3. **Sales Table**
   ```sql
   CREATE TABLE Sales (
     SaleID INT PRIMARY KEY,
     CustomerID INT,
     ProductID INT,
     Quantity INT,
     SaleDate DATE,
     FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID),
     FOREIGN KEY (ProductID) REFERENCES Products(ProductID)
   );
   ```

### Part 2 – Power BI Implementation
- **Step 1**: Connected Power BI to SalesDB using DirectQuery mode
- **Step 2**: Established relationships between Customers, Products, and Sales tables
- **Step 3**: Created DAX measures for:
  - Total Sales Amount
  - Total Quantity Sold
  - Average Sale Amount
- **Step 4**: Developed visualizations including:
  - Bar Chart: Total Sales by Product Category
  - Pie Chart: Sales by Region
  - Line Chart: Sales Trend over time
  - Matrix Table: Customer purchases with quantities and amounts
 
  ---

## 📸 Dashboard Preview

### Sales Analysis Dashboard
[![Sales Analysis Dashboard](https://github.com/HussienBedier1/Sales-Analysis-Power-BI-/blob/main/Sales%20Analysis.png)](https://github.com/HussienBedier1/Sales-Analysis-Power-BI-/blob/main/Sales%20Analysis.png)


### Data Model View
[![Data Model View](https://github.com/HussienBedier1/Sales-Analysis-Power-BI-/blob/main/Model%20View.png)](https://github.com/HussienBedier1/Sales-Analysis-Power-BI-/blob/main/Model%20View.png)

---

## 🛠️ Tools & Technologies
- **Database**: Microsoft SQL Server
- **BI Tool**: Microsoft Power BI
- **Query Language**: SQL
- **Data Analysis**: DAX (Data Analysis Expressions)
- **Connection Mode**: DirectQuery

---

## 📈 Key Insights
- **Total Sales**: $68,000 across all transactions
- **Volume**: 13 units sold with average sale amount of $14,000
- **Product Performance**: Electronics category dominates sales revenue
- **Regional Distribution**: Cairo represents 38.49% of total sales
- **Top Customer**: Ali Hassan with purchases totaling $37,500
- **Sales Trend**: Consistent sales activity from January to March 2025

---

## 🏁 Conclusion
This sales analysis dashboard provides comprehensive visibility into business performance, enabling:
- Identification of top-performing products and categories
- Understanding of regional sales distribution patterns
- Tracking of sales trends over time
- Analysis of customer purchasing behavior
- Data-informed decision making for sales strategy optimization

The DirectQuery connection ensures real-time data accuracy while the optimized data model supports efficient analysis and reporting.

---

## 📬 Contact Me
💼 **Hussien Bedier**  
📧 Email: [hussienbedier10@gmail.com](mailto:hussienbedier10@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/hussien-bedier-34a778231/) | [GitHub](https://github.com/HussienBedier1)


#  Power BI Sales & Customer Analytics

 SALES OVERVIEW
  <img width="1280" height="710" alt="Final (11)" src="https://github.com/user-attachments/assets/8c4fb765-e0d0-40d0-b116-3b0bbbb4ab3d" />

 CUSTOMER ANALYSIS
  <img width="1280" height="716" alt="Final (10)" src="https://github.com/user-attachments/assets/2d50d7f2-8a8e-454e-b75b-892203b40f37" />

 PRODUCT AND REGION ANALYSIS
  <img width="1280" height="726" alt="Final (2)" src="https://github.com/user-attachments/assets/5a28e7c2-d93b-4c99-8791-973b93322281" />

  SALES DEEP DIVE
  <img width="1280" height="726" alt="Final (2)" src="https://github.com/user-attachments/assets/c55055f5-4f47-4b12-8b15-c5cd166dcf2a" />



 
  

##  Project Overview

This Power BI project provides a complete **Sales, Customer, Product, and Returns analysis dashboard**.
It helps businesses understand performance across **regions, categories, customers, and time** using interactive visuals and KPIs.

---

##  Key Objectives

* Analyze **Total Sales, Orders, Quantity, and Customers**
* Track **monthly and yearly sales trends**
* Identify **top-performing products and customers**
* Understand **sales distribution by category & subcategory**
* Analyze **returns and their reasons**
* Compare performance across **regions and segments**

---

## 📂 Dataset Description

### 🧾 Fact Tables

1. **Sales_Fact**

   * SaleID
   * CustomerID
   * ProductID
   * DateID
   * UnitsSold
   * TotalAmount

2. **Returns_Fact**

   * ReturnID
   * SaleID
   * ReturnReason
   * ReturnDate

---

###  Dimension Tables

1. **Customer_Dim**

   * CustomerID
   * FirstName
   * LastName
   * Email
   * Segment (Consumer, Corporate, Home Office)
   * Region

2. **Product_Dim**

   * ProductID
   * ProductName
   * Category
   * SubCategory
   * Price

3. **Date_Dim**

   * DateID
   * Date
   * Year
   * Month
   * Quarter
   * Month_Number

4. **Region_Dim**

   * RegionID
   * RegionName
   * ManagerName

---

##  Data Model

* Star Schema implemented
* Relationships:

  * Sales_Fact → Customer_Dim
  * Sales_Fact → Product_Dim
  * Sales_Fact → Date_Dim
  * Sales_Fact → Region_Dim
  * Returns_Fact → Sales_Fact

---

##  Key Measures (DAX)

```DAX
Total Sales = SUM(Sales_Fact[TotalAmount])

Total Orders = DISTINCTCOUNT(Sales_Fact[SaleID])

Total Quantity = SUM(Sales_Fact[UnitsSold])

Total Customers = DISTINCTCOUNT(Customer_Dim[CustomerID])

Avg Sales per Customer = DIVIDE([Total Sales], [Total Customers])
```

---

##  Dashboard Features

### 🔹 Sales Overview

* Total Sales, Orders, Quantity, Customers (KPI Cards)
* Sales trend by Year & Month (Line Chart)

### 🔹 Product Analysis

* Sales by Category (Donut Chart)
* Sales by SubCategory (Bar Chart)
* Top Products by Sales

### 🔹 Customer Insights

* Sales by Customer Name
* Customers by Segment (Treemap)
* Customers by Region & Segment (Stacked Bar)

### 🔹 Regional Analysis

* Sales by Region
* stomers by Region

### 🔹 Returns Analysis

* Returns by Reason (Bar Chart)

  * Late Delivery
  * Wrong Item
  * Defective
  * Customer Changed Mind

###  Advanced Visual

* Scatter Plot:

  * Total Sales vs Quantity by Product

---

##  Filters / Slicers

* Year (2024, 2025)
* Category
* Region
* Segment

---

##  Data Cleaning (Power Query)

* Removed duplicates
* Trimmed & cleaned text
* Standardized capitalization
* Fixed data types
* Created Month Number for sorting

---

##  Insights Generated

* Identify top-selling products and categories
* Understand customer behavior across segments
* Detect regions with highest/lowest performance
* Analyze major return reasons
* Track sales growth trends over time

---

##  Tools Used

* Power BI Desktop
* Power Query (ETL)
* DAX (Data Analysis Expressions)

---

##  Conclusion

This dashboard provides a **complete business overview** and helps in:

* Better decision making
* Performance tracking
* Identifying improvement areas

     

##  Author

**Yagna Patel**

---



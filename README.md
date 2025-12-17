# leadHer-Capstone-project
# DataCo Global – Sales & Customer Intelligence Dashboard

## Project Overview

This project is a **Power BI capstone analytics project** developed for **DataCo Global**, a multinational B2C company operating across multiple countries and markets. The goal is to transform raw transactional sales data into a **clean analytical data model** and deliver a **professional, insight-driven dashboard** to support executive decision-making.

This project focuses on building a **star schema**, creating a **custom Date table**, and designing a **two-page Power BI dashboard** that highlights sales performance, profitability, customer behavior, and delivery efficiency.

---

##  Business Objectives

The dashboard helps business stakeholders answer key questions such as:

* How are **sales and profits performing over time**?
* Which **regions, markets, and product categories** contribute the most profit?
* How do **delivery timelines and late shipment risks** affect business outcomes?
* What are the key **customer segments and regional trends**?

---

##   Data Modeling Approach

A **Star Schema** data model was implemented to ensure optimal performance, scalability, and ease of analysis.

###   Fact Table: `FactSales`

Contains transactional sales and shipment-level metrics:

* FactSales ID
* Order ID
* Order Date
* Shipment Date
* Customer ID (FK → DimCustomer)
* Product Card ID (FK → DimProduct)
* Location Key (FK → DimLocation)
* Sales Metrics: Sales, Quantity, Discount, Profit
* Shipment Metrics: Shipment Days (Actual), Delivery Status, Late Delivery Risk

###  Dimension Tables

#### `DimCustomer`

* Customer ID
* Customer Name
* Segment
* Address
* State
* Country

#### `DimProduct`

* Product ID
* Product Name
* Price
* Product Status
* Category
* Department

#### `DimLocation`

* Location Key
* Market
* Region
* City
* Country
* Latitude
* Longitude

#### `DimDate` (Custom Date Table)

Created from scratch using **DAX / Power Query**, covering all dates in the dataset:

* Date
* Year
* Quarter
* Month
* Month Name
* Week Number
* Day of Week

---

## 📈 Dashboard Structure

The Power BI report consists of **two pages**, designed for both high-level and detailed analysis.

### Page 1: Executive Summary (Home)

A high-level overview designed for senior management.

#### Key KPIs (with YoY Analysis):

* **Total Sales**
  `Total Sales = SUM(FactSales[Sales])`
* **Total Profit**
  `Total Profit = SUM(FactSales[Order Profit Per Order])`
* **Total Quantity Sold**
  `Total Quantity = SUM(FactSales[Order Item Quantity])`
* **Average Delivery Time**
  `Avg Delivery Time = AVERAGE(FactSales[Shipment Days (Actual)])`

Each KPI includes **Year-over-Year (YoY) % change** using time intelligence DAX calculations.

#### Supporting Visuals:

* Sales by Region / Market (Map or Bar Chart)
* Top Performing Products (by Sales or Profit)
* Customer Segment Performance

#### Interactive Slicers:

* Region
* Product Category
* Customer Segment
* Date

---

### Page 2: Deep Dive Analysis

Designed for analysts and operational teams requiring detailed insights.

Includes:

* Sales Trend Over Time (Line Chart)
* Profit Breakdown by Category / Department
* Late Delivery Risk by Region or Category
* Sales Performance by Customer Segment and Region

---

##  Tools & Technologies Used

* **Power BI Desktop**
* **DAX (Data Analysis Expressions)**
* **Power Query (ETL & Data Transformation)**
* **Star Schema Data Modeling**

---

## Project Deliverables

The final submission includes:

* A `.pbix` Power BI file
* Cleaned and transformed datasets
* Properly modeled fact and dimension tables
* Custom-built Date table
* Two fully interactive dashboard pages
* DAX measures for KPIs and YoY calculations
* A clean, professional, and user-friendly report layout

---

##  How to Use the Dashboard

1. Open the `.pbix` file in **Power BI Desktop**.
2. Use slicers to filter data by **Region, Product Category, Customer Segment, or Date**.
3. Navigate between the **Executive Summary** and **Deep Dive Analysis** pages to explore insights at different levels.
4. Hover over visuals to view detailed tooltips and cross-filter results.

---

## 🔍 Key Insights Generated (Sample)

* **Sales Growth:** Certain regions and markets consistently outperform others, indicating strong geographic demand concentration.
* **Profitability Drivers:** High sales volume does not always translate to high profit, highlighting the impact of discounts and logistics costs.
* **Delivery Performance:** Regions with longer average delivery times show a higher late delivery risk, potentially impacting customer satisfaction.
* **Customer Segmentation:** Corporate and high-value customer segments contribute disproportionately to overall profit.

---

## 📢 Business Recommendations

* Optimize inventory and logistics in **high late-risk regions** to reduce delivery delays.
* Focus marketing and upsell strategies on **high-profit customer segments**.
* Re-evaluate discount strategies for products with **high sales but low profitability**.
* Use regional performance insights to guide **market expansion and resource allocation**.

---

## 👤 ONOME OYEDEJI

**Role:** Junior Data Analyst
**Project Type:** Data Analytics Capstone Project

---

## ✅ Notes

This project demonstrates best practices in:

* Dimensional data modeling
* Business-focused KPI design
* Time intelligence with DAX
* Executive-ready dashboard storytelling

---

*End of README*


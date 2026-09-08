# Superstore Business Performance & Profitability Analysis — Power BI

## 📌 Project Overview

This is a **personal Power BI data analytics project** based on the Sample Superstore retail dataset.

The project analyzes business performance using **sales, profit, orders, customers, products, categories, regions, customer segments, shipping modes, discounts, and time-based analysis**.

An interactive **4-page Power BI dashboard** was created to convert raw transactional data into meaningful business insights.

---

## 📊 Dataset

- **Dataset:** Sample Superstore
- **Records:** 9,994
- **Fields:** 21
- **Period:** 2014–2017
- **Domain:** Retail
- **Data Level:** Transaction / Order-Line Level
- **File Type:** CSV

### Main Data Fields

`Order ID` • `Order Date` • `Ship Date` • `Ship Mode` • `Customer ID` • `Customer Name` • `Segment` • `Region` • `Category` • `Sub-Category` • `Product Name` • `Sales` • `Quantity` • `Discount` • `Profit`

---

## 🎯 Project Objectives

- Analyze overall sales and profit performance.
- Track important business KPIs.
- Identify high- and low-performing categories and products.
- Analyze customer and regional performance.
- Compare customer segments and shipping modes.
- Examine discount and profitability patterns.
- Identify business trends and generate recommendations.

---

## 🛠️ Tools Used

- **Microsoft Power BI Desktop**
- **Power Query**
- **DAX**
- **CSV Dataset**

---

## 🔄 Data Preparation

The dataset was prepared in Power BI using Power Query.

Main preparation activities included:

- Data inspection
- Data type checking
- Date preparation
- Numerical field preparation
- Customer and order identification
- Preparing categorical fields for analysis
- Preparing data for DAX calculations and visualizations

---

## 🧮 Key DAX Measures

The dashboard uses DAX measures for KPI calculations and analysis, including:

- Total Sales
- Total Profit
- Total Orders
- Total Customers
- Profit Margin %
- Average Order Value
- Profit PY
- Profit YoY %
- Customer Sales Rank

---

## 📈 Dashboard

### 1. Sales Performance Dashboard

Provides an overview of business performance through:

- Total Sales
- Total Profit
- Total Orders
- Total Customers
- Profit Margin
- Average Order Value
- Sales trends
- Category performance
- Regional performance
- Shipping mode analysis

### 2. Profitability Analysis

Focuses on profitability through:

- Profit by Sub-Category
- Sales vs Profit by Category
- Product profitability
- Discount vs Profitability
- Profit Margin
- Profit YoY

### 3. Customer & Segment Analysis

Analyzes:

- Customer segments
- Sales by segment
- Profit by segment
- Customer performance
- Top 10 customers by sales

> The Top 10 Customers funnel-style visual is used for **ranking/concentration analysis**, not sales conversion.

### 4. Customer & Product Details

Provides detailed analysis of:

- Customers
- Products
- Categories
- Sub-Categories
- Sales
- Profit
- Quantity
- Discount

---

## 📌 Key Metrics

| Metric | Value |
|---|---:|
| Total Sales | **$2M** |
| Total Profit | **$286K** |
| Total Orders | **5K** |
| Total Customers | **793** |
| Profit Margin | **12.5%** |
| Average Order Value | **$459** |
| Profit YoY | **14.2%** |

*Values are displayed in rounded form as shown in the dashboard.*

---

## 🔍 Key Insights

- **Technology** is a strong contributor to both sales and profit.
- **Furniture** generates high sales but comparatively lower profit.
- **West** has the highest displayed regional sales.
- **Consumer** is the largest customer segment.
- **Standard Class** has the highest displayed sales among shipping modes.
- Some products generate negative profit despite generating sales.
- Discount and profitability show an observed pattern that requires further investigation.

> The discount analysis shows an association/pattern and does not prove that discounts cause lower profit.

---

## 💡 Business Recommendations

- Review low-profit Furniture products and sub-categories.
- Continue monitoring strong Technology performance.
- Investigate the lower sales performance of the South region.
- Monitor Consumer customers and their profitability.
- Review products generating negative profit.
- Evaluate discounts together with profit and margin.
- Analyze shipping costs before making shipping profitability decisions.

---
## 📊 Dashboard

The project includes four Power BI dashboard pages:

1. Sales Performance Dashboard
2. Profitability Analysis
3. Customer & Segment Analysis
4. Customer & Product Details

Dashboard screenshots are available in the `Screenshots/` folder.
## 📁 Repository Structure

```text
superstore-power-bi-business-analysis/
│
├── Dataset/
│   └── Sample_Superstore.xlsm
│
├── PowerBI/
│   └── Superstore_PowerBI_Dashboard.pbix
│
├── Report/
│   └── Superstore_PowerBI_Project_Report.pdf
│
├── Screenshots/
│   ├── 01_Sales_Dashboard.png
│   ├── 02_Profitability_Analysis.png
│   ├── 03_Customer_Segment_Analysis.png
│   └── 04_Customer_Product_Details.png
│
└── README.md

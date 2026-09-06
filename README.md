# Superstore Business Performance & Profitability Analysis — Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Analytics-yellow)
![DAX](https://img.shields.io/badge/DAX-Measures-blue)
![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Preparation-green)
![Excel](https://img.shields.io/badge/Excel-Dataset-brightgreen)

## 1. Project Title

**Superstore Business Performance & Profitability Analysis**

A personal Power BI project focused on analyzing retail sales, profitability, customers, products, regions, segments, discounts and shipping performance.

---

## 2. Project Overview

This project uses the Sample Superstore transactional dataset to develop an interactive **4-page Power BI dashboard**.

The dashboard converts transactional data into business-focused insights using:

- Power Query for data preparation
- DAX for analytical measures
- KPI cards
- Interactive slicers
- Time-based analysis
- Category and regional analysis
- Customer and segment analysis
- Product-level analysis
- Profitability analysis
- Ranking and comparison visuals

The objective is to make the dataset easier to understand and support data-driven business interpretation.

---

## 3. Business Problem

Retail transaction data contains valuable information about sales, profit, customers, products and operations, but raw transactional data can be difficult to interpret.

This project addresses the following business questions:

- How are overall sales and profit performing?
- Which categories generate the most sales and profit?
- Which regions contribute the most sales?
- Which customer segments are the largest?
- Which customers generate the highest sales?
- Which products are strong or weak in profitability?
- How does discounting appear alongside profitability?
- Which shipping modes contribute most to sales?
- How do sales change over time?

---

## 4. Objectives

The main objectives of the project are:

1. Analyze overall sales and profitability.
2. Develop important business KPIs.
3. Compare sales performance across categories and regions.
4. Analyze customer segments and customer-level performance.
5. Identify profitable and loss-making products and sub-categories.
6. Examine discount and profitability patterns.
7. Analyze shipping mode performance.
8. Create an interactive Power BI dashboard.
9. Generate business insights and recommendations from the analysis.

---

## 5. Dataset

The project uses the **Sample Superstore** transactional dataset.

### Dataset Details

| Attribute | Details |
|---|---|
| Dataset | Sample Superstore |
| Records | 9,994 |
| Fields | 21 |
| Period | 2014–2017 |
| Granularity | Transaction / order-line level |
| Business Domain | Retail / Superstore |

### Main Dataset Fields

**Order & Shipping**
- Row ID
- Order ID
- Order Date
- Ship Date
- Ship Mode

**Customer**
- Customer ID
- Customer Name
- Segment

**Geography**
- Country
- City
- State
- Postal Code
- Region

**Product**
- Product ID
- Category
- Sub-Category
- Product Name

**Business Measures**
- Sales
- Quantity
- Discount
- Profit

---

## 6. Tools & Technologies

### Tools Used

- **Microsoft Power BI Desktop**
- **Power Query**
- **DAX**
- **Microsoft Excel**
- **Data Visualization**
- **Data Modeling**

### Power BI Features

- KPI Cards
- Slicers
- Bar Charts
- Line/Area Charts
- Pie/Donut Charts
- Scatter Plot
- Tables
- Ranking Visuals
- Cross-filtering
- Page Navigation
- Reset Filters

---

## 7. Data Preparation

The project follows an end-to-end data analytics workflow:

```text
Raw Dataset
     ↓
Data Import
     ↓
Data Inspection
     ↓
Data Preparation
     ↓
Data Modeling
     ↓
DAX Measures
     ↓
Dashboard Development
     ↓
Interactive Analysis
     ↓
Business Insights
Preparation Activities
Inspected the dataset structure.
Reviewed column names and data types.
Prepared date fields for time-based analysis.
Ensured numerical fields were suitable for calculations.
Used distinct Order ID for order-level KPI analysis.
Used distinct Customer ID for customer-level KPI analysis.
Created reusable DAX measures for dashboard KPIs.
Validated the final dashboard against the source dataset.
8. Data Model
The Superstore transaction data is used as the main analytical dataset.
A Date table is used in the documented time-intelligence calculation for prior-year profit analysis.
The analytical structure supports:
Sales analysis
Profit analysis
Time analysis
Customer analysis
Product analysis
Category analysis
Regional analysis
Segment analysis
Shipping analysis
9. DAX Measures
The project uses DAX to create reusable analytical measures.
Note: The measures below are documented/reference implementations for the project. They are provided for transparency and should not be interpreted as a binary export of the PBIX model.
Total Sales
Total Sales =
SUM('Superstore'[Sales])
Total Profit
Total Profit =
SUM('Superstore'[Profit])
Total Orders
Total Orders =
DISTINCTCOUNT('Superstore'[Order ID])
Total Customers
Total Customers =
DISTINCTCOUNT('Superstore'[Customer ID])
Profit Margin %
Profit Margin % =
DIVIDE([Total Profit], [Total Sales], 0)
Average Order Value
Average Order Value =
DIVIDE([Total Sales], [Total Orders], 0)
Prior-Year Profit
Profit PY =
CALCULATE(
    [Total Profit],
    DATEADD('Date'[Date], -1, YEAR)
)
Profit YoY %
Profit YoY % =
DIVIDE(
    [Total Profit] - [Profit PY],
    [Profit PY],
    0
)
Customer Sales Rank
Customer Sales Rank =
RANKX(
    ALL('Superstore'[Customer Name]),
    [Total Sales],
    ,
    DESC,
    DENSE
)
10. Dashboard Pages
The Power BI report contains four analytical pages.
Page 1 — Sales Analysis
The Sales Analysis page provides an executive-level overview of business performance.
KPIs
Total Sales
Total Profit
Total Orders
Total Customers
Profit Margin %
Average Order Value
Visuals
Monthly Sales Trend
Sales by Category
Sales by Region
Sales by Ship Mode
KPI Cards
Year Slicer
Region Slicer
Category Slicer
Segment Slicer
Reset Filters control
Page 2 — Profitability Analysis
This page focuses on financial performance and profitability.
Visuals
Profit by Sub-Category
Sales vs Profit by Category
Profit Margin %
Profit YoY %
Discount vs Profitability Scatter Plot
Top Products Table
The page helps identify areas where strong sales do not necessarily translate into strong profit.
Page 3 — Customer & Segment Analysis
This page focuses on customer and segment performance.
Visuals
Profit by Customer Segment
Sales by Customer Segment
Customer Performance Table
Top 10 Customers Ranking
Customer KPI Cards
The Top 10 Customers visual is used as a ranking/concentration view, not as a traditional sales conversion funnel.
Page 4 — Customer & Product Details
This page provides more granular product and category-level analysis.
Visuals
Top Products Table
Sales by Category
Monthly Sales Trend
Profit by Category
KPI Cards
The product table combines Sales, Profit, Quantity and Discount to support product-level analysis.
11. Key Insights
Overall Performance
The validated dataset contains approximately:
$2.30M Total Sales
$286.40K Total Profit
5,009 Distinct Orders
793 Distinct Customers
12.47% Calculated Profit Margin
$458.61 Average Sales per Distinct Order
Category Performance
Technology is the strongest category by sales and profit.
Furniture generates substantial sales but has a comparatively lower profit contribution.
Office Supplies contributes meaningful sales and profit.
Regional Performance
West is the highest-sales region.
East is another strong contributor.
South has the lowest sales among the four regions.
Customer Segment
Consumer is the largest customer segment by sales.
Corporate and Home Office contribute additional revenue.
Shipping
Standard Class is the dominant shipping mode by sales.
Product Profitability
The product-level analysis shows that high sales do not automatically mean high profit.
Some products generate meaningful sales while producing negative profit, highlighting the importance of evaluating both revenue and profitability.
Discount Analysis
The discount-versus-profitability visual provides a pattern for further investigation. It should not be interpreted as proof that discounting directly causes lower profit.
12. Business Recommendations
1. Review Furniture Profitability
Investigate pricing, procurement costs and discount levels within Furniture and weaker sub-categories.
2. Protect Technology Performance
Maintain product availability and competitive pricing for strong Technology products while continuing to monitor profitability.
3. Investigate South Region Performance
Compare product mix, customer mix, discounts and order values between South and stronger-performing regions.
4. Focus on Consumer Customer Retention
Since Consumer is the largest segment, retention and cross-selling opportunities can be explored within this customer group.
5. Review Loss-Making Products
Products with negative profit should be investigated for pricing, discount and cost issues.
6. Evaluate Discounts Alongside Profit
Discount decisions should consider profit impact rather than focusing only on sales volume.
7. Review Shipping Economics
Shipping modes can be evaluated using both sales performance and operational cost information when available.
13. Project Results
The project resulted in:
A 4-page interactive Power BI dashboard
Reusable DAX measures
KPI-based performance monitoring
Sales and profitability analysis
Customer and segment analysis
Product-level analysis
Regional analysis
Shipping analysis
Interactive slicers
Cross-filtering
Dashboard navigation
Business insights
Business recommendations
Portfolio-ready documentation
14. Skills Demonstrated
Technical Skills
Microsoft Power BI
Power Query
DAX
Data Preparation
Data Modeling
KPI Development
Data Visualization
Time-Series Analysis
Ranking Analysis
Interactive Dashboard Development
Analytical Skills
Sales Analysis
Profitability Analysis
Customer Analysis
Product Analysis
Regional Analysis
Segment Analysis
Discount Analysis
Business Insight Generation
Recommendation Development
15. Screenshots
Sales Dashboard
�
Profitability Analysis
�
Customer & Segment Analysis
�
Customer & Product Details
�
16. Repository Structure
superstore-power-bi-business-analysis/
│
├── README.md
│
├── Report/
│   └── Superstore_PowerBI_Project_Report.pdf
│
├── PowerBI/
│   └── Superstore_PowerBI_Dashboard.pbix
│
├── Dataset/
│   └── Sample_Superstore.xlsx
│
└── Screenshots/
    ├── 01_Sales_Dashboard.png
    ├── 02_Profitability_Analysis.png
    ├── 03_Customer_Segment_Analysis.png
    └── 04_Customer_Product_Details.png
17. How to Use the Project
Clone or download the repository.
Open the .pbix file using Power BI Desktop.
If required, update the dataset source path.
Refresh the data.
Use the slicers to filter the analysis.
Navigate between the four dashboard pages.
Review the DAX measures documented in this README.
Refer to the detailed project report for methodology and analysis.
18. Limitations
The Sample Superstore dataset is a portfolio/learning dataset.
It does not represent current real-world company performance.
Detailed inventory, returns, targets, budgets and logistics costs are not available.
Discount and profitability relationships should not be interpreted as causal without further analysis.
Some dashboard KPI values are displayed in rounded form for presentation purposes.
19. Future Scope
Potential future work only:
Add richer time-intelligence measures such as Sales YoY, YTD and rolling performance.
Add product and sub-category profit-margin flags.
Add targets and budget variance analysis when target data is available.
Add shipping cost and delivery-time analysis when operational data is available.
Add automated refresh and Power BI Service deployment.
20. Author / Contact
Author: [karthikeyan]
Role: Aspiring Data Analyst
LinkedIn:[https://www.linkedin.com/in/karthi-keyan-a95b8b316]
Email: [karthikeyan11112006@gmail.com]

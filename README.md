Superstore Business Performance & Profitability Analysis — Power BI
Personal Data Analytics & Power BI Portfolio Project
📌 Project Overview
This project uses the Sample Superstore dataset to analyze business performance using Microsoft Power BI.
The dashboard provides insights into:
Sales
Profit
Orders
Customers
Products
Categories
Regions
Customer Segments
Shipping Modes
Discounts
Time-based performance
🎯 Objectives
Analyze overall sales and profitability.
Track important business KPIs.
Identify high- and low-performing categories and products.
Analyze customer and regional performance.
Compare sales and profit across different business areas.
Create an interactive dashboard for business analysis.
📊 Dataset
Dataset: Sample Superstore
Records: 9,994
Fields: 21
Period: 2014–2017
Domain: Retail
Main Fields
Order ID
Order Date
Ship Date
Ship Mode
Customer ID
Customer Name
Segment
Region
Category
Sub-Category
Product Name
Sales
Quantity
Discount
Profit
🛠️ Tools Used
Microsoft Power BI Desktop
Power Query
DAX
CSV Dataset
🔄 Data Preparation
The dataset was prepared in Power BI before analysis.
Main activities included:
Data inspection
Data type checking
Date preparation
Numerical field preparation
Order and customer calculations
Preparing categorical fields for analysis
Creating measures using DAX
🧮 DAX Measures
The project uses DAX measures for KPI and analytical calculations, including:
Total Sales
Total Profit
Total Orders
Total Customers
Profit Margin %
Average Order Value
Profit PY
Profit YoY %
Customer Sales Rank
Product Sales Rank
The documented DAX formulas are reference/documentation formulas and are not claimed as a direct PBIX export.
📈 Dashboard Pages
1. Sales Dashboard
Provides an overall view of:
Sales
Profit
Orders
Customers
Sales trends
Category performance
Regional performance
Shipping mode performance
2. Profitability Analysis
Focuses on:
Profit
Profit Margin
Profit YoY
Category profitability
Sub-category profitability
Product profitability
Discount and profitability patterns
3. Customer & Segment Analysis
Analyzes:
Customer segments
Customer sales
Customer profit
Customer performance
Top 10 customers
The Top 10 Customers funnel-style visual represents ranking/concentration, not sales conversion.
4. Customer & Product Details
Provides detailed analysis of:
Customers
Products
Categories
Sales
Profit
Quantity
Discount
🔍 Key Insights
Technology is a strong contributor to both sales and profit.
Furniture has significant sales but comparatively lower profit.
West has the highest displayed regional sales.
Consumer is the largest customer segment.
Standard Class has the highest displayed sales among shipping modes.
Some products generate negative profit despite having sales.
Discount and profitability show an observed pattern that requires further investigation; the dashboard does not establish causation.
💡 Business Recommendations
Review low-profit product and sub-category performance.
Investigate Furniture profitability.
Monitor strong Technology performance.
Investigate lower-performing regions.
Evaluate customers using both sales and profit.
Review discount strategies alongside profitability.
Analyze shipping costs before making shipping profitability decisions.
🖼️ Dashboard Screenshots
Sales Dashboard
�
Profitability Analysis
�
Customer & Segment Analysis
�
Customer & Product Details
�
📁 Repository Structure
Superstore-PowerBI-Business-Analysis/
│
├── README.md
├── Dataset/
│   └── Sample_Superstore.csv
│
├── PowerBI/
│   └── Superstore_PowerBI_Dashboard.pbix
│
├── Report/
│   └── Superstore_PowerBI_Project_Report.pdf
│
└── Screenshots/
    ├── 01_Sales_Dashboard.png
    ├── 02_Profitability_Analysis.png
    ├── 03_Customer_Segment_Analysis.png
    └── 04_Customer_Product_Details.png
▶️ How to Use
Download or clone this repository.
Open the .pbix file in Power BI Desktop.
Update the dataset path if required.
Refresh the data.
Explore the four dashboard pages.
Use the slicers and interactive visuals.
Refer to the PDF report for detailed documentation.
⚠️ Limitations
The project uses the Sample Superstore portfolio dataset.
Data covers 2014–2017.
The analysis is mainly descriptive.
Detailed inventory, returns, budget, target, and shipping-cost analysis is not included.
Discount-profit relationships should not be interpreted as causal.
🔮 Future Scope
Potential Future Work:
Additional time-intelligence analysis
Target and budget analysis
Advanced customer segmentation
Forecasting
Shipping-cost analysis
Delivery-time analysis
Power BI Service deployment
Automated refresh
👤 Author
Karthi Keyan
Aspiring Data Analyst
GitHub: [Add GitHub Profile]
LinkedIn: [Add LinkedIn Profile]
Email: [Add Professional Email]
📄 Resume Description
Developed a Power BI dashboard using the Sample Superstore dataset, applying Power Query and DAX for KPI, sales, profitability, customer, product, and regional analysis.
Created interactive visualizations and dashboards to identify business performance patterns and generate data-driven business insights and recommendations.

# SuperStore-Sales-Analysis
Power BI dashboard analyzing SuperStore sales trends, profitability, and business insights
## 📌 Project Overview
This project analyzes sales data from a superstore to extract actionable insights for business growth. The analysis is conducted using **Power BI**, and includes data cleaning, transformation, and visualization using **DAX queries** and custom calculations.

## 🎯 Objectives
- Identify top-performing and underperforming products & categories.
- Analyze regional sales trends.
- Evaluate customer purchasing behavior.
- Optimize inventory & discount strategies for higher profitability.
- Forecast future sales trends.

## 📂 Dataset Details
- **Dataset Name:** SuperStore Sales Data
- **File Format:** CSV, Excel
- **Columns:** Order ID, Order Date, Ship Date, Customer Name, Product Category, Sub-Category, Sales, Quantity, Discount, Profit, Region, State, City, etc.
- **Total Records:** (Number extracted from dataset)

## 🔄 Steps Followed in Analysis
1. **Data Cleaning & Preparation:**
   - Removed duplicates and handled missing values.
   - Standardized date formats and category names.
   - Ensured consistency in region and state names.

2. **Data Transformation:**
   - Created new calculated columns using DAX.
   - Aggregated data for regional and category-wise analysis.
   - Applied appropriate filters for time-series analysis.

3. **Data Visualization & Insights:**
   - Built an interactive **Power BI Dashboard**.
   - Visualized sales performance by category, region, and customer segments.
   - Analyzed discount impact on profit margins.

## 📊 Key Business Insights
- **Top-Selling Product Categories:** (Extracted from data)
- **Regions with Highest Sales:** (Extracted from data)
- **Customer Segments with Maximum Purchases:** (Extracted from data)
- **Impact of Discounts on Profitability:** (Extracted from data)
- **Seasonality & Sales Trends:** (Extracted from data)

## 📈 Data-Driven Recommendations
- Increase stock of **[Top-Selling Products]** in high-sales regions.
- Reduce discount rates on **[Low-Profit Categories]** to improve margin.
- Offer targeted promotions in **[Low-Sales Regions]** to boost revenue.
- Optimize shipping strategies to reduce delays in **[Slowest Delivery Regions]**.

## 📌 DAX Queries Used
### 🏆 Total Sales Calculation:
```DAX
Total Sales = SUM(SuperStore[Sales])
```

### 💰 Total Profit Calculation:
```DAX
Total Profit = SUM(SuperStore[Profit])
```

### 📅 Yearly Sales Growth:
```DAX
Sales Growth = 
VAR PreviousYearSales = CALCULATE(SUM(SuperStore[Sales]), SAMEPERIODLASTYEAR(SuperStore[Order Date]))
RETURN 
IF(NOT(ISBLANK(PreviousYearSales)), (SUM(SuperStore[Sales]) - PreviousYearSales) / PreviousYearSales, BLANK())
```

### 🛒 Profit Margin:
```DAX
Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)
```

### 📦 Discount Impact Analysis:
```DAX
Discount Impact = 
CALCULATE([Total Sales], SuperStore[Discount] > 0) - CALCULATE([Total Sales], SuperStore[Discount] = 0)
```

## 📊 Dashboard Visualizations
- **Sales by Region** (Bar Chart)
- **Top Product Categories by Sales** (Pie Chart)
- **Profit Margin Analysis** (Gauge Chart)
- **Sales Trend Over Time** (Line Chart)
- **Impact of Discount on Sales** (Scatter Plot)
- **Customer Segments & Purchasing Behavior** (Heatmap)

## 📌 Conclusion
This Power BI dashboard provides deep insights into sales patterns, profitability, and business performance. By implementing the recommendations, the superstore can improve profitability, optimize stock management, and enhance customer experience.

## 👤 Author & Contact
- **Name:** Ashutosh Kadam
- **LinkedIn:** [Ashutosh Kadam](https://www.linkedin.com/in/ashutosh-kadam-4562151b6)
- **GitHub:** [Ashu-5599](https://github.com/Ashu-5599)

📢 **Feel free to connect for more data-driven insights & analytics projects!** 🚀

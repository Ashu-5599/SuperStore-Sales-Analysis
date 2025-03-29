# **SuperStore Sales Analysis - Power BI Dashboard & Insights**

## **Introduction**
This project analyzes **SuperStore Sales Data** to uncover key business insights, profitability trends, and operational inefficiencies. Using **Power BI and DAX**, I built an interactive dashboard to visualize data-driven recommendations that optimize **sales, profit margins, and customer experience**.

## **1. Business Performance Overview**
- **Total Sales:** ₹1,565,804.32
- **Total Profit:** ₹175,262.10
- **Profit Margin:** 11.19%
- **Unique Customers:** 773
- **Unique Products Sold:** 1,742
- **Total Orders:** 9,994
- **Average Order Value (AOV):** ₹156.74

## **2. Key Insights from Data Analysis**

### **2.1. Profitability by Category**
- **Most Profitable Category:** **Technology** (₹90,458.25 in profit)
- **Least Profitable Category:** **Furniture** (₹10,006.61 in profit)
- **Insight:**
  - Technology **dominates profitability**, indicating high demand and strong pricing power.
  - Furniture category has **low margins**, requiring pricing or cost adjustments.

### **2.2. High Return Rate in Office Supplies**
- **Most Returned Product Category:** **Office Supplies**
- **Insight:**
  - High returns suggest **quality issues, incorrect shipments, or unmet customer expectations**.
  - Returns affect profitability and may indicate the need for supplier/vendor quality checks.

### **2.3. City-Wise Sales Performance**
- **Top 5 Cities by Sales:**
  1. **New York City:** ₹154,919.70
  2. **Los Angeles:** ₹120,017.44
  3. **San Francisco:** ₹80,891.42
  4. **Seattle:** ₹77,924.54
  5. **Philadelphia:** ₹77,305.44
- **Insight:**
  - **New York City is the highest sales contributor**, making it a prime location for **targeted marketing campaigns**.
  - **Lower-performing cities should be analyzed for potential expansion strategies.**

### **2.4. Shipping Performance & Delivery Delays**
- **Most Used Shipping Mode:** Standard Class (60% of orders)
- **Fastest Shipping Mode:** Same Day
- **Insight:**
  - Standard Class shipping is the most used but has **higher delays and customer complaints**.
  - Expedited shipping options like **Second Class and Same Day reduce customer dissatisfaction** but come at a higher cost.

## **3. Data-Driven Recommendations**

### **3.1. Optimize Pricing and Margins for Furniture**
**Problem:** Low profit margins in Furniture category.
**Solution:**
- **Increase prices on high-demand furniture items** while remaining competitive.
- **Negotiate better supplier contracts** to lower procurement costs.
- **Bundle furniture products** with complementary items (desks + chairs) to increase basket value.

### **3.2. Reduce High Returns in Office Supplies**
**Problem:** Office Supplies category has the highest return rates.
**Solution:**
- **Investigate return reasons** and improve product descriptions & packaging.
- **Enhance order verification** before shipping to avoid mis-shipments.
- **Review return policies** to reduce non-legitimate returns.

### **3.3. Focus Marketing on High-Sales Cities**
**Problem:** Sales are concentrated in a few key cities.
**Solution:**
- **Expand localized advertising and partnerships** in New York, Los Angeles, and San Francisco.
- **Offer exclusive discounts or loyalty programs** in top-performing regions.

### **3.4. Maximize Technology Category Growth**
**Problem:** Technology is the most profitable but underutilized for upselling.
**Solution:**
- **Implement product bundles** (Laptops + Accessories) to encourage larger purchases.
- **Leverage email & WhatsApp marketing** for tech upgrades & warranty offers.

### **3.5. Improve Shipping Efficiency to Reduce Delivery Delays**
**Problem:** Standard Class shipping leads to delays and customer dissatisfaction.
**Solution:**
- **Optimize logistics partnerships to improve shipping time**.
- **Offer incentives for customers to choose faster shipping methods.**

## **4. Power BI Dashboard - DAX Queries Used**
The Power BI dashboard was built using the following DAX queries:

### **Total Sales Calculation**
```DAX
Total Sales = SUM(SuperStore[Sales])
```

### **Total Profit Calculation**
```DAX
Total Profit = SUM(SuperStore[Profit])
```

### **Profit Margin Calculation**
```DAX
Profit Margin = DIVIDE([Total Profit], [Total Sales]) * 100
```

### **Total Orders Count**
```DAX
Total Orders = COUNT(SuperStore[Order ID])
```

### **Average Order Value (AOV) Calculation**
```DAX
AOV = DIVIDE([Total Sales], [Total Orders])
```

### **Top 5 Cities by Sales**
```DAX
Top Cities Sales = 
TOPN(
    5,
    SUMMARIZE(SuperStore, SuperStore[City], "City Sales", SUM(SuperStore[Sales])),
    [City Sales], DESC
)
```

### **Return Rate Analysis**
```DAX
Return Rate = COUNT(SuperStore[Returns]) / COUNT(SuperStore[Order ID])
```

### **Most Profitable Category Calculation**
```DAX
Most Profitable Category = 
TOPN(
    1,
    SUMMARIZE(SuperStore, SuperStore[Category], "Total Profit", SUM(SuperStore[Profit])),
    [Total Profit], DESC
)
```

### **Least Profitable Category Calculation**
```DAX
Least Profitable Category = 
TOPN(
    1,
    SUMMARIZE(SuperStore, SuperStore[Category], "Total Profit", SUM(SuperStore[Profit])),
    [Total Profit], ASC
)
```

## **5. Conclusion**
By implementing these **data-driven strategies**, businesses can:
- **Optimize pricing for higher margins** (Furniture Category)
- **Reduce operational losses from high returns** (Office Supplies)
- **Expand targeted marketing to boost revenue** (New York, LA, SF)
- **Maximize technology sales via upselling**
- **Improve shipping efficiency to enhance customer experience**

### **🔹 Key Takeaway**
This **Power BI dashboard** and **DAX-powered analytics** offer **real-time visibility into business performance**, helping companies make **smarter, data-driven decisions**.

📢 Connect with me on LinkedIn for more data analytics insights!

---
### **Author:** Ashutosh Kadam  
### **LinkedIn:** [Ashutosh Kadam](https://www.linkedin.com/in/ashutosh-kadam-4562151b6)  
### **GitHub Repository:** [GitHub Repo](https://github.com/Ashu-5599)  
---

## Project Summary


This project analyzes vendor performance and sales data within an inventory management system, covering the complete data lifecycle—from raw data ingestion and ETL processing to in-depth analysis and interactive visualization. The primary objective is to evaluate vendor efficiency, uncover sales and profitability trends, and generate actionable insights to support data-driven business decisions.

The project demonstrates hands-on expertise in Python, SQL, data analysis, ETL workflows, and Power BI dashboard development.

Key Achievements

##  **Exploratory Data Analysis Overview**

### Summary Statistics
![Summary Statistics](image/Summary_statistics.PNG)

### Distribution plots
![histogram_plot](image/histogram_plot.PNG)


## 📊 Summary Statistics Insights

### ⚠️ Negative & Zero Values
- **Gross Profit (Min: -52,002.78)**  
  Some transactions are running at a loss due to high costs or heavy discounting.
- **Profit Margin (Min: -∞)**  
  Revenue is zero or lower than costs, indicating unprofitable sales.
- **Total Sales Quantity & Sales Dollars (Min: 0)**  
  Products were purchased but never sold, suggesting slow-moving or obsolete inventory.

### 🔍 Outliers & High Variability
- **Purchase & Actual Prices**  
  Maximum values (5,681.81 / 7,499.99) compared to low mean values (24.39 / 35.64) indicate the presence of premium or high-end products.
- **Freight Cost (0.09 → 257,032.07)**  
  Large variation points to bulk shipments or inefficiencies in logistics.
- **Stock Turnover (0 → 274.5)**  
  Some products sell extremely fast while others barely move.  
  Stock turnover greater than 1 indicates sales fulfilled from older inventory.

### 💡 Key Takeaways
- Monitor loss-making products and negative margins for corrective action.
- Investigate high freight costs and extreme stock turnover to optimize logistics.
- Implement strategies to reduce slow-moving or obsolete inventory.

## 🧹 Data Filtering

To improve data quality and reliability, the following filters were applied:

- **Gross Profit ≤ 0** – Excluded loss-making transactions.
- **Profit Margin ≤ 0** – Focused analysis on profitable sales.
- **Total Sales Quantity = 0** – Removed items that were never sold.

### Correlation heatmap
![Correlation_heatmap](image/Correlation_heatmap.PNG)

## 📈 Correlation Insights

### Purchase Price vs Sales & Profit
- Weak correlation with **Total Sales Dollars (-0.012)** and **Gross Profit (-0.016)**  
  → Price variations have minimal impact on overall revenue or profitability.

### Purchase Quantity vs Sales Quantity
- Strong positive correlation (**0.999**)  
  → Confirms efficient inventory turnover, where purchased quantities are almost fully sold.

### Profit Margin vs Total Sales Price
- Negative correlation (**-0.179**)  
  → Higher sales prices may result in lower profit margins, possibly due to competitive pricing pressures.

### Stock Turnover vs Profitability
- Weak negative correlation with **Gross Profit (-0.038)** and **Profit Margin (-0.055)**  
  → Faster inventory turnover does not necessarily translate into higher profitability.

## Research Questions & Key Findings

### Brands for promotional and pricing adjustments
![brands](image/brands.PNG)

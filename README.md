# Project 2: Vendor Performance Analysis

# Vendor Performance Analysis: Optimizing Profitability and Supply Chain Efficiency

This project is a data-driven initiative leveraging a comprehensive sales, purchase, and inventory dataset to provide actionable strategies for maximizing profitability, minimizing financial losses, and mitigating supply chain risks. The workflow involves **SQL** for robust data preparation and cleaning, followed by **Python** (Pandas, Matplotlib, SciPy) for in-depth statistical and exploratory analysis, and culminates in a **Power BI** dashboard for interactive visualization.  

---

## Project Goals

The analysis focuses on addressing key operational challenges:  

1. Identify brands with **low sales performance but high profit margins** that may require targeted pricing or promotional strategies.  
2. Highlight **top-performing vendors** that contribute significantly to sales and gross profit.  
3. Analyze the impact of **bulk purchasing** on unit costs to optimize savings.  
4. Assess **inventory turnover** to reduce holding costs and improve operational efficiency.  
5. Investigate **profitability variance** between high-performing and low-performing vendors.  

---

## Technical Stack and Tools

| Category                 | Tools                               | Purpose                                                                                   |
|--------------------------|------------------------------------|-------------------------------------------------------------------------------------------|
| Data Preparation & Cleaning | SQL (SQLite), Python (Pandas)      | Data ingestion, relational checks, vendor-specific filtering, aggregation, type conversions, handling missing values |
| Statistical Analysis      | Python (Pandas, SciPy, Matplotlib) | Exploratory Data Analysis (EDA), summary statistics, correlation analysis, two-sample T-test for hypothesis validation |
| Visualization & Reporting | Power BI                             | Creating a comprehensive, interactive dashboard for vendor performance metrics            |

---

## Dataset Overview

The analysis uses a multi-file dataset available on [Kaggle](https://www.kaggle.com/datasets/harshmadhavan/vendor-performance-analysis/code), providing a complete view of vendor performance. Core files integrated include:  

- `purchases.csv`: Vendor purchase transaction details  
- `sales.csv`: Records of sales performance linked to vendors  
- `purchase_prices.csv`: Historical vendor pricing information  
- `vendor_invoice.csv`: Invoice details for reconciliation  

A central table, `vendor_sales_summary`, was created by joining these datasets to pre-aggregate metrics such as `TotalPurchaseDollars`, `TotalSalesDollars`, `TotalSalesPrice`, and `FreightCost`.  

New calculated columns enrich the analysis, including:  

- `GrossProfit`  
- `ProfitMargin`  
- `StockTurnover`  
- `SalesToPurchaseRatio`  

---

## Key Findings and Recommendations

### 1. Profitability Strategy and Pricing

- **Low Sales, High Margin Opportunity:** 198 brands were identified with low sales volume but high profit margins, indicating opportunities for targeted promotions or pricing adjustments.  
- **Profit Margin Variance:** A two-sample T-Test yielded a T-Statistic of **-17.6440** and a P-value of **0.0000**, confirming a significant difference in profit margins:  
  - Top-selling vendors: mean margin **31.17%**  
  - Low-selling vendors: mean margin **41.55%**  

  Recommendations: high-margin vendors should review pricing, while top-selling vendors focus on operational cost efficiency.  

### 2. Supply Chain Efficiency and Risk Mitigation

- **Impact of Bulk Purchasing:** Large order sizes reduce unit costs by **72%** (unit cost $10.78 vs higher costs for smaller orders), validating bulk purchasing strategies.  
- **Vendor Concentration Risk:** Top 10 vendors account for **65.69%** of total purchases, suggesting a need to diversify vendor partnerships to mitigate supply chain risk.  
- **Inventory Inefficiency:** Total unsold capital is **$2.71M**, indicating slow-moving stock ties up working capital. Recommendations include adjusting purchase quantities, launching clearance sales, and revising storage strategies.  

### 3. Correlation Insights

- Strong positive correlation (~1.00) between `TotalPurchaseQuantity` and `TotalSalesQuantity` indicates an efficient alignment of purchasing and sales.  
- Negative correlation (-0.179) between `ProfitMargin` and `TotalSalesPrice` suggests higher sales prices may reduce profit margins, possibly due to competitive pricing pressures.  

---

## Conclusion

This Vendor Performance Analysis project successfully utilized a multi-faceted approach, combining robust SQL data preparation and aggregation with in-depth Python statistical analysis, to deliver critical insights for strategic decision-making in inventory, purchasing, and pricing. The analysis confirmed key areas where intervention can maximize profitability and mitigate risk.

**[View Presentation Deck](https://www.canva.com/design/DAG18ySP7Mo/dAV_1_GNbWz-Vb5EX8_4XA/edit)** to explore the full analysis.

# 🛒 Olist E-commerce RFM Customer Segmentation

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![SQL](https://img.shields.io/badge/SQL-SQLite-orange.svg)
![Data Analysis](https://img.shields.io/badge/Analysis-RFM-green.svg)

## 📌 Project Overview
This project performs a comprehensive **RFM (Recency, Frequency, Monetary) analysis** on the Olist E-commerce dataset (100k+ orders). The goal is to segment customers based on their purchasing behavior to provide actionable insights for marketing and retention strategies.

## 🎯 Business Problem
Olist is a large marketplace with a diverse customer base. Without segmentation, marketing efforts are "one-size-fits-all," leading to inefficient spending. This project identifies:
- **Champions:** High-value, loyal customers.
- **At Risk:** Former big spenders who haven't returned recently.
- **Promising:** New customers with potential for growth.

## 🛠️ Technical Implementation
### 1. Data Engineering (SQL)
- Utilized **SQLite CTEs** for modular and readable query logic.
- **Data Integrity:** Aggregated payments at the `order_id` level before joining with other tables to prevent revenue inflation caused by multiple order items.
- Filtered for `delivered` orders only to ensure financial accuracy.

### 2. RFM Modeling
- Applied the **NTILE(5)** window function to rank customers across three dimensions:
    - **Recency:** Days since the last purchase.
    - **Frequency:** Number of unique orders.
    - **Monetary:** Total spending.
- Developed a custom scoring logic to categorize segments.

## 📊 Key Results
- **Champions Segment:** Represents ~15% of the customer base but contributes significantly to the total revenue with an **Average Order Value (AOV) of $370+**.
- **At-Risk Segment:** Holds over **$6M in historical revenue**, representing a massive opportunity for re-engagement campaigns.



## 💡 Strategic Recommendations
- **Loyalty:** Implement VIP programs for "Champions" to maintain satisfaction.
- **Retention:** Target "At Risk" customers with high-value win-back coupons.
- **Growth:** Focus on up-selling to "Promising" newcomers to increase their frequency.

## 📂 Repository Structure
- `RFM_Modeling_Olist.ipynb`: Full analysis and visualization.
- `olist.db`: Database file (if applicable/small enough) or instructions to download from Kaggle.

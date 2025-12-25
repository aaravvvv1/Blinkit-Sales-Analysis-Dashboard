# Blinkit Sales Analysis Dashboard 🛒

## Project Overview
This project provides a comprehensive analysis of **$1.2M in sales** for Blinkit (formerly Grofers), India's last-minute app. The dashboard identifies key revenue drivers, outlet performance, and product trends to assist in strategic business decision-making.

## Key Insights
* **Top Performers:** Fruits, Vegetables, and Snack Foods dominate revenue, each exceeding **$0.18M**.
* **Tiered Growth:** Tier 3 locations are the strongest performers, contributing **$472K** to total sales.
* **Customer Preference:** Regular fat items account for **64.6%** of total sales compared to Low Fat alternatives.

## Technical Implementation
### 1. Data Cleaning (Power Query)
* **Imputation Logic:** Handled missing values in the `Item Weight` column by engineering a sub-query to calculate and map average weights based on `Item Type` (e.g., Dairy: 13.43, Seafood: 12.55).
* **Standardization:** Cleaned categorical inconsistencies in `Item Fat Content` and `Outlet Size` to ensure accurate grouping.

### 2. Data Modeling & DAX
* Created a **Star Schema** to optimize report performance.
* Developed custom DAX measures:
  * `Total Sales = SUM(Merge1[Sales])`
  * `Total Items = COUNTROWS(Merge1)`
  * `Avg Rating = AVERAGE(Merge1[Rating])`
  * `Avg Sales = AVERAGE(Merge1[Sales])`
 


## How to View
1. Download the `Blinkit Final Dashboard.pbix` file.
2. Open with [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

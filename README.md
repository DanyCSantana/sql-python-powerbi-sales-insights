# 🥃 Diageo Market Analysis – Iowa Liquor Sales

## 📌 Project Overview
This project analyzes the performance of **Diageo** and competitors in the Iowa liquor market using the open-source **Iowa Liquor Sales dataset**.  
It combines **data engineering, data visualization, and business storytelling** to deliver insights about sales, categories, vendors, and geographic trends.  

The project simulates a **real-world business case**: understanding market position, identifying growth opportunities, and presenting results to stakeholders.

---

## 🔄 Workflow
1. **Data Preparation (Python + DuckDB)**
   - Cleaned raw sales data (5+ years of transactions).
   - Standardized vendor and category names.
   - Built **dimension tables** (`dim_items` and `dim_stores`) with unique and enriched attributes.
   - Exported final dataset in **Parquet format** for efficient analysis.

2. **Data Analysis & Visualization (Power BI)**
   - Created dashboards to explore:
     - Market share by vendor.
     - Sales trends over time.
     - Top categories and items.
     - Geographic performance (cities & counties).
     - Pricing and volume insights.

3. **Business Storytelling (PowerPoint)**
   - Summarized key insights in an executive-friendly presentation.
   - Highlighted competitive positioning of **Diageo vs. Sazerac and other vendors**.
   - Provided actionable recommendations for strategic decisions.

---

## 📊 Key Insights
- **Diageo leads in sales value ($),** but competitors like **Sazerac** dominate in **volume (units sold)**.  
- Certain categories (e.g., whiskey and vodka) show strong competition and require targeted strategies.  
- Geographic analysis revealed **regional concentration of sales**, with opportunities for expansion in underpenetrated cities.  
- Price positioning impacts both sales volume and total revenue, suggesting different strategies for premium vs. mass-market products.

---

## 🛠️ Tech Stack
- **Python** (pandas, duckdb) → Data cleaning & ETL  
- **DuckDB** → SQL queries on large CSVs & Parquet  
- **Power BI** → Interactive dashboards  
- **PowerPoint** → Executive storytelling  

---

## 📂 Repository Structure

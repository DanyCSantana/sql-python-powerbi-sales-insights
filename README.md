![Python](https://img.shields.io/badge/Python-3.11-blue)
![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Visualization-green)
![GitHub](https://img.shields.io/badge/GitHub-Repo-black)

# 🥃 SQL + Python + Power BI: End-to-End Market Insights Project (Diageo Case Study)

---

## 📖 Table of Contents
- [Final Dashboard Animation](#-final-dashboard-animation)
- [Project Overview](#-project-overview)
- [Workflow](#-workflow)
- [Dataset Context](#-dataset-context)
- [Data Challenges & Cleaning](#-data-challenges--cleaning)
- [Key Insights](#-key-insights)
- [Tech Stack & Justification](#-tech-stack--justification)
- [Presentation Preview](#-presentation-preview)
- [Repository Structure](#-repository-structure)

---

## 🎥 Final Dashboard Animation

<p align="center">
  <img src="https://raw.githubusercontent.com/DanyCSantana/sql-python-powerbi-sales-insights/main/meu_gif_completo.gif" width="600">
</p>

---

## 📌 Project Overview
This project analyzes the performance of **Diageo** and competitors in the Iowa liquor market using the **Iowa Liquor Sales open dataset**.  
It demonstrates the full data lifecycle: **data engineering, cleaning, enrichment, visualization, and executive storytelling**.

The goal was to simulate a **real business case**: preparing raw transactional data, creating analytical datasets, exploring trends with Power BI, and delivering actionable insights in an executive presentation.

---

## 🔄 Workflow
1. **Data Preparation (SQL + Python + DuckDB)**
   - Loaded and cleaned **26M+ rows** of raw liquor sales transactions.
   - Standardized vendor and category names.
   - Built **dimension tables**:
     - `dim_items`: unique item descriptions.
     - `dim_stores`: best available store names, most common cities/counties.
   - Filtered dataset to **April 2018 – March 2023** for recency and consistency.
   - Exported clean data in **Parquet format**.

2. **Data Analysis (Power BI)**
   - Created dashboards with KPIs and trends:
     - Market share by vendor.
     - Sales trends over time.
     - Top categories and items.
     - Geographic breakdown by city and county.
     - Pricing vs. sales volume analysis.

3. **Business Storytelling (PowerPoint)**
   - Executive presentation summarizing key findings.
   - Clear comparison of **Diageo vs. competitors**.
   - Actionable recommendations for market strategy.

---

## 📊 Dataset Context
- Source: **Iowa Liquor Sales dataset** (public, open-source, provided by the State of Iowa).
- Size: **26,160,915 rows** and **24 columns**.
- Timeframe: **Jan 2012 – Mar 2023** (filtered to **Apr 2018 – Mar 2023** for analysis).
- Fields include:
  - Store details (number, name, city, county, location).
  - Vendor details (number, name).
  - Product details (item number, description, category).
  - Sales metrics (bottle size, bottles sold, retail price, total sales, volume sold).

---

## 🧹 Data Challenges & Cleaning
During preparation, several issues were addressed:
- **Inconsistent category names** → fixed using `COALESCE` and external mapping file.  
- **Vendors with multiple names** → standardized into groups (e.g., “DIAGEO”, “SAZERAC”).  
- **Duplicate item descriptions** → resolved using `ROW_NUMBER()` and keeping the most sold version.  
- **Store names/cities inconsistent** → selected best available name and most frequent city/county per store.  
- **Invalid numeric values (0 or NULL)** → filtered out in the final dataset.  

---

## 📈 Key Insights
- **Diageo leads in revenue ($)** but competitors like **Sazerac** dominate in **volume (units sold)**.  
- **Vodka and whiskey categories** are highly competitive and represent growth opportunities.  
- **Geographic concentration**: major cities (e.g., Des Moines, Cedar Rapids) drive the bulk of sales.  
- **Price positioning**: premium brands sell fewer bottles but drive higher total revenue.  

---

## 🛠️ Tech Stack & Justification
- **DuckDB** → fast SQL queries on large CSV/Parquet files locally.  
- **Python (pandas)** → additional cleaning and category mapping from Excel.  
- **SQL** → heavy data transformations and enrichment logic.  
- **Power BI** → interactive dashboards for business exploration.  
- **PowerPoint** → final storytelling layer for executives.  

---

## 🎞 Presentation Preview

<p align="center">
  <img src="https://raw.githubusercontent.com/DanyCSantana/sql-python-powerbi-sales-insights/main/Diageo_Presentation.gif" width="700">
</p>

---

## 📂 Repository Structure

```text
├── notebooks/        # Jupyter notebooks with SQL + Python cleaning
├── data/             # Raw & processed data (not included in repo)
├── outputs/          # Exported dimension tables (Parquet)
├── dashboards/       # Power BI dashboards (PDF/PNG exports + GIFs)
├── presentation/     # Executive slides (PDF/PPTX + GIF animation)
└── README.md         # Project documentation

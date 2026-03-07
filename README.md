# Nike Sales Analysis (Uncleaned Dataset) — Power BI Portfolio Project

This project is a complete **end-to-end Data Analyst portfolio case study** using a purposely messy, synthetic Nike sales dataset.  
I cleaned and standardized the data in **Python**, then built a **Power BI dashboard** to analyze **Data**.

> Dataset note: This dataset is synthetic and created for educational use. No real Nike customer data is included.

---

## Project Goals
- Convert a **dirty “real-world style” dataset** into an analysis-ready dataset
- Fix common business data issues (nulls, typos, wrong types, invalid values, inconsistent dates)
- Build a **Power BI dashboard** 
- Generate insights useful for business decisions (discount strategy, top products, regional performance)

---

## Dataset Overview
**Source:** Kaggle — *Nike Sales (Uncleaned) Dataset* (synthetic)  
**Size:** ~2,500+ transactions  
**Typical issues included:**
- Null values
- Typos in regions (e.g., *Delhii*, *Banglore*)
- Wrong data types
- Negative values in numeric columns
- Inconsistent date formats (e.g., `2023/07/21`, `21-07-2023`)
- Discounts over 100%
- Revenue/profit inconsistencies

---

## What I Built
### 1) Data Cleaning (Python)
A reproducible cleaning pipeline to:
- Standardize column names
- Fix city/region typos (mapping to clean names)
- Convert datatypes safely (including robust date parsing)
- Handle null values (median/most-common logic where appropriate)
- Treat invalid values:
  - negative `Units_Sold` → corrected/flagged depending on rule
  - `MRP` ≤ 0 → treated as missing
  - `Discount_Applied` > 100% → capped/flagged
- Recalculate validation metrics:
  - expected revenue = `Units_Sold * MRP * (1 - Discount%)`
  - mismatch flags for Revenue / Profit inconsistencies

**Output:** `Nike_Sales_Cleaned.csv`

---

### 2) Power BI Dashboard
Built an interactive report with:
- **KPI Cards:** Total Revenue, Total Profit, Units Sold, Avg Discount
- **Trends:** Revenue/Profit over time (monthly/weekly)
- **Segmentation:**
  - Revenue & Profit by Product Line
  - Online vs Retail channel comparison
  - Gender Category breakdown
  - Region performance (Top cities + filters)
- **Discount Analysis:**
  - Discount vs Profit relationship
  - High-discount products with low/negative profit
---


## Tech Stack
- **Python:** Pandas, NumPy (data cleaning & export)
- **Power BI:** Power Query, DAX measures, interactive dashboarding

#  Superstore Sales & Profitability Analysis

A full end-to-end data analysis project on the Superstore dataset — covering data ingestion, SQL-based exploration using SQLite inside Python, and an interactive Tableau dashboard.

---

##  Project Overview

This project analyzes 4 years of retail sales data (2014–2017) from a US-based superstore. The goal is to uncover insights about sales performance, profitability by region and category, the impact of discounts, and shipping behavior — all to support data-driven business decisions.

---

##  Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python (Pandas) | Data loading, cleaning, and feature engineering |
| SQLite (via Python) | SQL-based analysis and business queries |
| Kaggle Hub | Automated dataset download |
| Tableau | Interactive dashboard and visualization |
| Jupyter Notebook | Single notebook containing the full workflow |

---

##  Project Structure

```
superstore-analysis/
│
├── Superstore.ipynb                        # Full analysis notebook (Python + SQL)
├── superstore_cleaned_for_visualization.csv  # Cleaned data exported for Tableau
├── dashboard_screenshot.png               # Tableau dashboard preview
└── README.md
```

---

##  Workflow

### 1. Data Ingestion
- Downloaded the dataset directly from Kaggle using `kagglehub`
- Loaded CSV into a Pandas DataFrame (9,994 rows × 21 columns)

### 2. Data Cleaning & Preparation
- Standardized column names (lowercase, underscores)
- Converted `order_date` and `ship_date` from strings to datetime
- Confirmed zero null values and no duplicate rows
- Engineered new calculated fields (e.g., profit margin, shipping duration)

### 3. SQLite Analysis
- Loaded the cleaned DataFrame into an in-memory SQLite database
- Wrote business-focused SQL queries to answer key questions:
  - Sales and profit trends by year
  - Profit by region and sub-category
  - Impact of discount tiers on profit margin
  - Top and bottom performing products
  - High-sales products with negative profit (loss leaders)
  - Shipping mode performance

### 4. Tableau Dashboard
- Exported the cleaned dataset to CSV
- Built an interactive dashboard covering:
  - KPI cards (Total Sales, Profit, Customers, Orders)
  - Geographic sales map
  - Sales & Profit trend over time
  - Profit by Region and Sub-Category
  - Shipping Mode Performance
  - Profit by Discount Type

---

##  Key Findings

- **Total Sales:** $2.30M | **Total Profit:** $286.4K | **Customers:** 793 | **Orders:** 5,009
- **West region** is the most profitable ($108K), while **Central** lags behind ($39.7K)
- **Technology** drives the highest profit; **Furniture (Tables)** is the biggest loss-maker at –$17.7K
- **High discounts erode profit** — orders with high discounts generated a net loss of –$975 in margin
- **Standard Class** dominates shipping (164K profit), while **Same Day** contributes only 15.9K
- Several high-revenue products (e.g., Cubify CubeX 3D Printer) generate significant losses — highlighting the risk of evaluating products on sales alone

---

##  Business Recommendations

1. **Review discount strategy** — high discounts are destroying margin across multiple categories
2. **Investigate Tables sub-category** — consistently the worst performer; consider repricing or discontinuing low-margin SKUs
3. **Focus growth efforts on the West region** — highest profitability with room to scale
4. **Flag loss-leader products** — products with high sales but negative profit need cost or pricing review

---

##  Dataset

- **Source:** [Superstore Dataset – Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
- **Size:** 9,994 rows, 21 columns
- **Period:** 2014–2017
- **Geography:** United States

---

##  How to Run

1. Clone this repository
2. Install dependencies:
   ```bash
   pip install pandas kagglehub
   ```
3. Open `Superstore.ipynb` in Jupyter Notebook or JupyterLab
4. Run all cells from top to bottom
5. The cleaned CSV will be exported for Tableau automatically

---

##  Author

**Mohamed Badawy Sayed**  
Data Analyst | Python · SQL · Tableau  
[LinkedIn](https://www.linkedin.com/in/mohamed-badawi28)

---

> *This project was built as part of a data analytics portfolio to demonstrate end-to-end analysis skills from raw data to business insights.*

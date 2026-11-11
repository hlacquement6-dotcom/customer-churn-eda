# Telco Customer Churn & Retention Analysis

An exploratory data analysis using Python and embedded SQLite to identify key drivers of customer attrition for a telecommunications provider, with actionable insights on pricing and contract structure.

- **Notebook:** [View Full Jupyter Notebook](customer_churn_eda.ipynb)
- **Tools Used:** Python (Pandas, Seaborn, Matplotlib), SQL (SQLite3), Google Colab

---

## Overview
Customer churn directly impacts predictable recurring revenue in subscription-based businesses. This analysis examines demographic factors, service subscriptions, and billing structures across 7,000+ customers to determine why users cancel and how to improve retention.

## Key Insights
- **Contract Vulnerability:** Month-to-month subscribers experience a **42.7% churn rate**, compared to just **2.8%** for two-year contract holders. Short-term contracts represent the largest operational risk.
- **Price Sensitivity:** Churned users averaged significantly higher monthly bills (**$74.44**) than retained customers (**$61.31**), suggesting price friction at higher service tiers.
- **The 18-Month Threshold:** Retained customers average **37.7 months** of tenure, whereas churned users leave after an average of **18.0 months**. Onboarding and early engagement during the first 1.5 years are critical.

## Technical Methodology
1. **Data Ingestion & Cleaning:** Handled invalid non-numeric entries in `TotalCharges` using Pandas numeric coercion and handled missing records.
2. **SQL Query Engine:** Created an in-memory SQLite database to run relational aggregations (`GROUP BY`, `CASE WHEN`, conditional counts) directly over Python dataframes.
3. **Data Visualization:** Built visual summaries using Seaborn and Matplotlib to highlight contract disparities and distribution metrics.

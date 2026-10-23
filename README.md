<div align="center">

# 🛍️ Customer Shopping Behaviour Analysis

### Turning customer purchase data into actionable business insights

<p>
  <img src="https://img.shields.io/badge/Python-Pandas-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python Pandas"/>
  <img src="https://img.shields.io/badge/Database-PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL"/>
  <img src="https://img.shields.io/badge/Visualization-Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI"/>
  <img src="https://img.shields.io/badge/Analysis-Data%20Analytics-00BFA6?style=for-the-badge" alt="Data Analytics"/>
</p>

**An end-to-end data analytics project exploring 3,900 customer shopping records to uncover purchasing patterns, product performance, and customer trends.**

</div>

---

## 📌 Project Overview

The **Customer Shopping Behaviour Analysis** project examines customer purchase records to understand how purchase value varies across product categories, gender, age groups, subscription status, discount usage, and shipping types.

The workflow combines **Python and Pandas** for data preparation, **PostgreSQL** for business-focused SQL analysis, and **Power BI** for interactive visual exploration.

> **Data note:** “Purchase value” refers to the sum of the dataset's `Purchase Amount (USD)` values. It should not be interpreted as audited company revenue or profit.

## 📊 Key Metrics

| Metric | Result |
|---|---:|
| Customer purchase records | **3,900** |
| Total recorded purchase value | **$233,081** |
| Average purchase amount | **$59.76** |
| Average review rating | **3.75 / 5** |
| Records marked subscribed | **1,053 (27.0%)** |
| Highest-value category | **Clothing — $104,264** |
| Highest total purchase value by gender | **Male records — $157,890** |

## 🎯 Project Objectives

- Explore the dataset structure, fields, and data quality.
- Clean and prepare the data using Python and Pandas.
- Use PostgreSQL queries to answer practical business questions.
- Compare purchase values across categories and customer segments.
- Present findings through a Power BI dashboard.
- Translate the results into clear, practical business recommendations.

## 🧰 Tech Stack

| Tool | Purpose |
|---|---|
| **Python** | Data inspection and preparation |
| **Pandas** | Data cleaning, transformation, and feature engineering |
| **PostgreSQL** | Querying, aggregation, filtering, and ranking |
| **pgAdmin** | Database management and query execution |
| **Power BI** | KPI cards, charts, comparisons, and slicers |
| **CSV / Excel-format source** | Input customer shopping data |

## 🔄 Project Workflow

```text
Customer Shopping Dataset
           │
           ▼
  Python + Pandas
  • Inspect data
  • Handle missing ratings
  • Standardize column names
  • Create age groups
           │
           ▼
       PostgreSQL
  • Aggregate purchase values
  • Filter and group records
  • Rank products
  • Answer business questions
           │
           ▼
        Power BI
  • KPI cards
  • Category comparisons
  • Age-group analysis
  • Subscription and shipping filters
           │
           ▼
  Insights & Recommendations
```

## 🔍 Business Questions Explored

1. Which gender group contributes more total purchase value?
2. How many discounted records have above-average purchase amounts?
3. Which products have the highest average review ratings?
4. How do Standard and Express shipping compare by average purchase amount?
5. Do subscribed records have a higher average purchase amount?
6. Which products show the highest discount-use percentages?
7. How many records fall into New, Returning, and Loyal customer segments?
8. Which products are purchased most often within each category?
9. How many repeat-buyer records are subscribed?
10. How is purchase value distributed across age groups?

## 💡 Key Findings

- **Clothing** is the largest category by recorded purchase value at **$104,264**, followed by **Accessories at $74,200**.
- Male records contribute **$157,890** in purchase value, compared with **$75,191** for female records in this dataset.
- Subscription groups have similar average purchase amounts: **$59.49** for subscribed records and **$59.87** for non-subscribed records.
- **Young Adult** records contribute the highest purchase value among the age groups, at **$62,143 (26.7%)**.
- **Express shipping** records have an average purchase amount of **$60.48**, compared with **$58.46** for Standard shipping.
- **Hat** has the highest discount-use share among the five products highlighted, at **50.00%**.
- Using the project's segmentation rule, the dataset contains **3,116 Loyal**, **701 Returning**, and **83 New** records.

> These are descriptive findings from this dataset. They do not establish that one factor causes another or represent universal market behaviour.

## 📈 Power BI Dashboard

The dashboard is designed to support quick exploration of:

- Customer count, average purchase amount, and average review rating
- Subscription status distribution
- Purchase value by product category
- Purchase value by age group
- Filters for subscription status, gender, category, and shipping type

**Dashboard screenshot:** Add your dashboard image to the repository (for example, `images/dashboard.png`) and uncomment the line below after uploading it.

<!--
<div align="center">
  <img src="images/dashboard.png" alt="Customer Shopping Behaviour Power BI Dashboard" width="900"/>
</div>
-->

## 🧹 Data Preparation

The Python/Pandas preparation workflow includes:

- Inspecting sample rows, schema, data types, and distributions
- Checking missing values
- Filling missing `Review Rating` values with the median within each product category
- Standardizing column names to lowercase with underscores
- Renaming the purchase amount field to `purchase_amount`
- Creating quantile-based age groups
- Mapping purchase-frequency labels to approximate day intervals
- Removing a duplicate promotion indicator when it matches the discount field
- Loading the prepared data into a PostgreSQL table

The report identifies **37 missing review ratings** in the original dataset. Frequency mappings are approximations and should be validated before operational use.

## 📁 Suggested Repository Structure

```text
customer-shopping-behaviour-analysis/
├── data/
│   └── README.md                 # Dataset notes; add data only if permitted
├── notebooks/
│   └── customer_shopping_analysis.ipynb
├── sql/
│   └── business_questions.sql
├── powerbi/
│   └── customer_behaviour_dashboard.pbix
├── images/
│   └── dashboard.png
├── README.md
└── requirements.txt
```

*This is a suggested structure. Keep only the folders and files that actually exist in your repository.*

## 🚀 How to Run the Project

1. Clone or download this repository.
2. Install Python and the required packages used in your notebook.
3. Open the notebook in Jupyter Notebook or VS Code.
4. Place the dataset in the location expected by the notebook and update the file path if needed.
5. Run the data inspection and preparation steps.
6. Create a PostgreSQL database and configure the connection details used by your code.
7. Run the SQL analysis queries.
8. Open the Power BI report and connect it to the prepared data source, if required.

### Python environment

Create a virtual environment and install dependencies:

```bash
python -m venv .venv
```

Windows:

```bash
.venv\Scripts\activate
```

Install the packages your notebook imports, for example:

```bash
pip install pandas sqlalchemy psycopg2-binary jupyter
```

Use the actual imports in your project to confirm the final dependency list. Do not commit database passwords, API keys, or other secrets.

## 🧠 Skills Demonstrated

`Data Cleaning` · `Pandas` · `SQL` · `PostgreSQL` · `Data Transformation` · `Feature Engineering` · `Aggregation` · `Ranking` · `Power BI` · `Dashboard Interpretation` · `Business Communication`

## ⚠️ Limitations

- The dataset contains 3,900 records and may not represent a full market or company history.
- The analysis is descriptive and does not prove causation.
- The report treats each row as one purchase record.
- Dashboard values may vary slightly due to rounding or aggregation choices.
- Age-group labels and purchase-frequency mappings should be validated.
- The repeat-buyer analysis uses `Previous Purchases > 5`; confirm that this is the intended business definition.

## 👤 Author

**Sujal Patil**

Data Analytics Project | Python · PostgreSQL · Power BI

---

<div align="center">

**⭐ If you find this project useful, consider giving the repository a star!**

</div>

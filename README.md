# 🛍️ Customer Shopping Behavior Analysis

An end-to-end data analytics project exploring customer purchasing patterns, segmentation, and subscription behavior using **Python**, **PostgreSQL (SQL)**, and **Power BI**. The goal is to transform raw transactional data into actionable business insights that support data-driven decision-making.

---

## 📌 Project Overview

This project analyzes **3,900 customer transactions** across multiple product categories to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior. The analysis pipeline covers the full data lifecycle — from cleaning and feature engineering in Python, to structured querying in PostgreSQL, to visual storytelling in Power BI.

---

## 📊 Dataset Summary

| Attribute | Details |
|---|---|
| **Rows** | 3,900 |
| **Columns** | 18 |
| **Missing Data** | 37 values in `Review Rating` |

**Key Features:**
- **Customer Demographics:** Age, Gender, Location, Subscription Status
- **Purchase Details:** Item Purchased, Category, Purchase Amount, Season, Size, Color
- **Shopping Behavior:** Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type

---

## 🧰 Tech Stack

| Tool | Purpose |
|---|---|
| **Python (Pandas)** | Data cleaning, feature engineering, exploratory analysis |
| **PostgreSQL (SQL)** | Structured business-question analysis |
| **Power BI** | Interactive dashboard and data visualization |

---

## 🔧 Data Preparation & Feature Engineering (Python)

- Loaded and explored the dataset using `pandas`, `df.info()`, and `.describe()`
- Imputed missing `Review Rating` values using the **median rating per product category**
- Standardized column names to **snake_case**
- Engineered new features:
  - `age_group` — binned customer ages into segments
  - `purchase_frequency_days` — derived from purchase frequency data
- Verified redundancy between `discount_applied` and `promo_code_used`; dropped the redundant column
- Loaded the cleaned dataset into **PostgreSQL** for structured SQL analysis

---

## 🗄️ SQL Analysis — Key Business Questions

| # | Analysis | Key Insight |
|---|---|---|
| 1 | Revenue by Gender | Male customers generated **$157,890** vs. **$75,191** from female customers |
| 2 | High-Spending Discount Users | 839 customers used discounts while still spending above the average purchase amount |
| 3 | Top 5 Products by Rating | Gloves (3.86), Sandals (3.84), Boots (3.82), Hat (3.80), Skirt (3.78) |
| 4 | Shipping Type Comparison | Express shipping customers spend slightly more on average ($60.48 vs. $58.46) |
| 5 | Subscribers vs. Non-Subscribers | Non-subscribers drive **73%** of total revenue ($170,436 vs. $62,645) |
| 6 | Discount-Dependent Products | Hats (50%), Sneakers (49.7%), Coats (49.1%) rely most heavily on discounts |
| 7 | Customer Segmentation | 3,116 Loyal · 701 Returning · 83 New customers |
| 8 | Top 3 Products per Category | Jewelry, Blouse, Sandals, and Jackets lead their respective categories |
| 9 | Repeat Buyers & Subscriptions | Repeat buyers (>5 purchases) are **not** strongly correlated with subscription status |
| 10 | Revenue by Age Group | Young Adults contribute the highest revenue ($62,143) |

---

## 📈 Power BI Dashboard

An interactive dashboard was built to visualize key KPIs and trends, featuring:
- **Filters:** Subscription Status, Gender, Category, Shipping Type
- **KPI Cards:** Number of Customers (3.9K), Average Purchase Amount ($59.76), Average Review Rating (3.75)
- **Visuals:** Revenue by Category, Sales by Category, Revenue by Age Group, Subscription Status Breakdown

> 📁 Dashboard file: `Customer_Behavior_Dashboard.pbix`

---

## 💡 Business Recommendations

- **Boost Subscriptions** — Promote exclusive benefits to convert non-subscribers, who currently drive the majority of revenue
- **Customer Loyalty Programs** — Reward repeat buyers to strengthen retention and move them into the "Loyal" segment
- **Review Discount Policy** — Balance promotional sales boosts against profit margin impact, especially for discount-dependent products
- **Product Positioning** — Feature top-rated and best-selling items prominently in marketing campaigns
- **Targeted Marketing** — Prioritize high-revenue age groups (Young Adults) and express-shipping customers

---

## 📂 Repository Structure

```
├── data/
│   └── customer_shopping_data.csv       # Raw dataset
├── notebooks/
│   └── Data_Cleaning_EDA.ipynb          # Python data prep & EDA
├── sql/
│   └── business_analysis_queries.sql    # PostgreSQL queries
├── dashboard/
│   └── Customer_Behavior_Dashboard.pbix # Power BI dashboard
├── Images/
│   └── Dashboard image_final
├── README.md
└── requirements.txt
```

## 📝 License

This project is available under the [MIT License](LICENSE).

---

## 🙋‍♂️ Author

**VISHVAKEERTHI C**
📧 vishvakeerthi112@gmail.com · 🔗 https://www.linkedin.com/in/vishvakeerthi-c-bb4352249.

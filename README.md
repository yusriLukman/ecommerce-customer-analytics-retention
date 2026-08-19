# E-Commerce Customer Analytics and Retention Strategy

An end-to-end customer analytics and retention framework for an e-commerce platform using **Python** and **DuckDB SQL**. Features executive KPI tracking, 10-tier RFM customer segmentation, cohort retention analysis, and historical CLV profiling with an automated multi-sheet Excel export pipeline.

---

## Project Overview
This project provides an end-to-end customer analytics and retention framework for an e-commerce platform using Python and DuckDB SQL. The analysis evaluates high-level business KPIs, classifies active customers into 10 distinct behavioral segments via RFM (Recency, Frequency, Monetary) modeling, tracks monthly cohort retention rates, and evaluates Historical Customer Lifetime Value (CLV).

All transactional data processing and analytical queries are structured across three core analytical pillars and conclude with an automated multi-sheet Microsoft Excel export pipeline.

---

## Business Problem Statement
Customer acquisition costs in e-commerce continue to rise, making customer retention and lifecycle optimization primary drivers for long-term profitability. E-commerce businesses face several strategic challenges:
* **Unclear Revenue Concentration:** Inability to identify which customer segments contribute the vast majority of overall revenue.
* **Customer Churn Exposure:** Lack of visibility into post-purchase retention behavior and drop-off points following initial acquisition.
* **One-Size-Fits-All Marketing:** Inefficient marketing spending resulting from uniform campaigns rather than targeted re-engagement strategies based on spending patterns.

This analysis addresses these challenges by transforming raw transaction data into actionable behavioral insights and tailored retention strategies.

---

## Core Analytical Architecture & Tech Stack

### Analytical Pillars
* **Pillar 1: Executive Overview & Business KPI Trends:** High-level executive performance summary (Total Revenue, Order Volume, Active Customer Base, Overall AOV), monthly trajectories with seasonality tracking, and geographic revenue distribution (UK vs. Non-UK).
* **Pillar 2: RFM Customer Behavioral Profiling:** Segmentation logic mapping customers into 10 behavioral groups (Champions, Loyal Customers, Potential Loyalists, At Risk, Hibernating, etc.) using quintile scoring (1–5), evaluating population distribution and revenue share per segment.
* **Pillar 3: Advanced Cohort Retention, Top Products & Historical CLV:** Monthly cohort retention matrix tracking user activity drop-off rates across 24+ months, product preference mapping for core segments, and Historical Customer Lifetime Value (CLV) analysis comparing mean/median spend profiles.

### Tech Stack & Dependencies
* **Data Processing & Manipulation:** Python 3.10, Pandas, NumPy
* **SQL Query Engine:** DuckDB
* **Data Visualization:** Matplotlib, Seaborn, Squarify
* **File Export Pipeline:** OpenPyXL

---

## Key Visualizations & Analytics Summary

### 1. Executive Performance & Revenue Trends
| Monthly Revenue & AOV Trends | Monthly Cohort Retention Rate |
| :---: | :---: |
| ![Monthly Revenue & AOV Trends](assets/Monthly%20Revenue%20%26%20AOV%20Trends.png) | ![Monthly Cohort Retention Rate](assets/Monthly%20Cohort%20Retention%20Rate.png) |

* **Revenue Drivers:** Total business performance exhibits strong seasonal demand spikes during Q4 (year-end holiday season).
* **First-Month Drop-Off:** Retention rates experience the steepest decline between Month 0 and Month 1, after which retention trajectories stabilize into steady baseline engagement.

### 2. RFM Behavioral Profiling & Product Performance
| RFM Segment Distribution & Revenue Share | Top Products (Champion Segment) |
| :---: | :---: |
| ![RFM Segment Distribution](assets/RFM%20Segment%20Distribution%20%26%20Revenue%20Share.png) | ![Top 5 Products](assets/Top%205%20Revenue-Generating%20Products%20Champion%20Segment.png) |

* **Revenue Concentration:** The **Champions** segment represents a critical revenue pillar, generating the vast majority of total monetary value despite constituting a smaller subset of the overall customer base.
* **Dormant Base Exposure:** A substantial portion of historical accounts fall under **Hibernating** and **About To Sleep** statuses, requiring structured re-engagement mechanisms to prevent permanent churn.

> *Additional supporting charts (such as geographic market performance, population distribution, and historical CLV profiling) are available in the [`assets/`](./assets) folder.*

---

## Strategic Recommendations & Action Plan

1. **Optimize Onboarding Strategy (Days 1–30):**  
   Implement automated post-purchase email onboarding sequences and first-repeat order incentives to mitigate the heavy retention drop-off observed immediately after Month 1.

2. **Targeted Churn Re-Engagement:**  
   Deploy personalized win-back campaigns for **At Risk** customers utilizing cross-sell recommendations derived from top-performing product SKUs.

3. **VIP Loyalty Program for Champions:**  
   Establish exclusive loyalty tiers, early product access, and dedicated support for **Champions** to safeguard core revenue streams and maintain high lifetime value.

---

## Repository Structure

```text
.
├── assets/                                           
│   ├── Customer Population Distribution across Segments.png
│   ├── Geographic Market Performance (UK vs. Non-UK).png
│   ├── Historical Customer Lifetime Value (CLV) per Segment.png
│   ├── Monthly Cohort Retention Rate.png
│   ├── Monthly Revenue & AOV Trends.png
│   ├── RFM Segment Distribution & Revenue Share.png
│   └── Top 5 Revenue-Generating Products: Champion Segment.png
├── ecommerce_customer_analytics_and_retention.ipynb
├── RFM_Analysis_and_Customer_Segmentation.xlsx       
├── .gitignore
└── README.md

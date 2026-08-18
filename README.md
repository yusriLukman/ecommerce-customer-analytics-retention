# E-Commerce Customer Analytics and Retention Strategy

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

## Core Analytical Architecture
The analytical pipeline is structured into three distinct pillars:

### Pillar 1: Executive Overview & Business KPI Trends
* High-level executive performance summary (Total Revenue, Order Volume, Active Customer Base, and Overall AOV).
* Monthly revenue trajectories paired with Average Order Value (AOV) seasonality tracking.
* Geographic revenue distribution evaluating domestic (UK) versus international market performance.

### Pillar 2: RFM Customer Behavioral Profiling
* Segmentation logic mapping customers into 10 behavioral groups (Champions, Loyal Customers, Potential Loyalists, At Risk, Hibernating, etc.) using quintile scoring (1–5).
* Evaluation of customer population distribution and revenue share per segment.

### Pillar 3: Advanced Cohort Retention, Top Products & Historical CLV
* Monthly cohort retention matrix tracking user activity drop-off rates across 24+ months.
* Product preference mapping identifying top revenue-generating SKUs for core segments.
* Historical Customer Lifetime Value (CLV) analysis comparing mean and median spend profiles across customer segments.

---

## Tech Stack & Dependencies
* **Data Processing & Manipulation:** Python 3.10, Pandas, NumPy
* **SQL Query Engine:** DuckDB
* **Data Visualization:** Matplotlib, Seaborn, Squarify
* **File Export Pipeline:** OpenPyXL

---

## Key Findings & Analytics Summary

### 1. Executive Performance & Market Dependency
* **Revenue Drivers:** Total business performance exhibits strong seasonal demand spikes during Q4 (year-end holiday season).
* **Geographic Market Concentration:** Over 80% of total revenue originates from the UK domestic market, highlighting a heavy geographic reliance with significant growth potential in international expansion.

### 2. RFM Behavioral Profiling
* **Revenue Concentration:** The **Champions** segment represents a critical revenue pillar, generating the vast majority of total monetary value despite constituting a smaller subset of the overall customer base.
* **Dormant Base Exposure:** A substantial portion of historical accounts fall under **Hibernating** and **About To Sleep** statuses, requiring structured re-engagement mechanisms to prevent permanent churn.

### 3. Cohort Retention & Lifetime Value
* **First-Month Drop-Off:** Retention rates experience the steepest decline between Month 0 and Month 1, after which retention trajectories stabilize into steady baseline engagement.
* **CLV Skewness:** Mean CLV significantly exceeds Median CLV across top-tier customer segments, proving that top spending outliers heavily influence segment averages.

---

## Strategic Recommendations & Action Plan

1. **Optimize Onboarding Strategy (Days 1–30):**
   Implement automated post-purchase email onboarding sequences and first-repeat order incentives to mitigate the heavy retention drop-off observed immediately after Month 1.

2. **Targeted Churn Re-Engagement:**
   Deploy personalized win-back campaigns for **At Risk** customers utilizing cross-sell recommendations derived from top-performing product SKUs.

3. **VIP Loyalty Program for Champions:**
   Establish exclusive loyalty tiers, early product access, and dedicated support for **Champions** to safeguard core revenue streams and maintain high lifetime value.

---

## Repository Structure & Deliverables

```text
├── ecommerce_customer_analytics_and_retention.ipynb   
├── ecommerce_customer_analytics_export.xlsx           
├── README.md                                           

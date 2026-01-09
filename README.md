

<h1 align="center">Customer Insights: Revenue, Rentals & Content Preferences</h1>

<p align="center">
  SQL-built Customer Data Warehouse → Decision Queries → Tableau Executive Dashboard  
</p>

<p align="center">
  <img src="https://img.shields.io/badge/SQL-Data%20Warehouse-F3E9DD?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Tableau-Dashboard-F3E9DD?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Analytics-Customer%20%26%20Revenue-F3E9DD?style=for-the-badge" />
</p>

---

## Project Overview
This project builds a **customer-focused analytics layer** for a global movie rental business by:
- Creating a consolidated **CustomerInsightsDW** data warehouse table (customer + rentals + payments + geography + content)
- Running **eight decision-oriented SQL queries** to surface customer value, risk, and preferences
- Delivering a **Tableau dashboard** designed for fast executive interpretation and action

---

## Business Objective (What leadership can decide from this)
This project is designed to help management:
- Identify **high-value customer tiers** and prioritize retention strategy  
- Detect **late-fee risk behavior** and reduce inventory bottlenecks  
- Understand **country-level revenue contribution** and market prioritization  
- Personalize engagement using **customer genre & film preferences**  
- Capture **seasonality patterns** to plan promotions and inventory  
- Optimize **content investment by country + genre revenue**

---

## Data & Tools
**Data Source**
- Built from the **Sakila** transactional dataset (rentals, payments, customers, inventory, films, categories, geography)

**Tooling**
- **MySQL / SQL**: joins, aggregation, window functions (NTILE, RANK), conditional segmentation  
- **Tableau**: five visuals + one interactive dashboard with filters (customer segment + country)

---

## What is in the Data Warehouse (CustomerInsightsDW)
The data warehouse is structured to support customer and revenue decisions, including fields such as:
- Customer identity and geography (country-level performance)
- Rental activity totals and timing (first/last rental)
- Payment-derived revenue totals
- Late fees and behavioral risk signals
- Highest rented category and film indicators for preference analysis

---

## Key Analytics Delivered (SQL Queries)
This repository includes 8 queries designed as **actionable business questions**, including:

1) **Customer revenue segmentation**
- Tiering customers into **Platinum / Gold / Regular** using percentile logic  
- Built to support loyalty strategy and lifetime value focus

2) **Late return risk segmentation**
- Ranking customers by late fees and labeling **High / Moderate / Low risk**  
- Built to reduce late returns and improve inventory turnover

3) **Revenue contribution by country**
- Ranking markets by total revenue, customer count, and average revenue per customer

4) **Customer genre preference**
- Identifying each customer’s most rented genre for targeted engagement

5) **Most preferred genre per customer**
- Simplified preference label useful for recommendation logic

6) **High-value film preference (revenue per rental)**
- Ranking films per customer using revenue efficiency logic

7) **Seasonality / peak rental months**
- Aggregating rental timing patterns to guide promo calendar decisions

8) **Genre revenue by country**
- Mapping which genres drive revenue in each market for localized content strategy

---

## Tableau Dashboard (Executive View)
The dashboard is designed as a **single-screen executive story**, combining:

- **Customer Segmentation by Revenue** (Platinum/Gold/Regular contribution)
- **Total Rentals vs Revenue by Genre** (popularity vs profitability)
- **World Map: Top Genre + Revenue by Country** (local taste + market performance)
- **Top Movies by Revenue** (most profitable titles + engagement context)
- **Late Fees by Genre + Segment** (policy opportunities + customer behavior)

Includes interactive filters:
- Customer segment  
- Country

---

## Repository Structure
Recommended structure:

```bash
.
├── assets/
│   └── dashboard_overview.png
├── tableau/
│   └── WH Tableau Dashboard.twbx
├── sql/
│   ├── 01_create_customerinsightsdw.sql
│   └── 02_decision_queries.sql
├── docs/
│   ├── final_project_report.pdf
│   └── queries_reference.pdf
└── README.md

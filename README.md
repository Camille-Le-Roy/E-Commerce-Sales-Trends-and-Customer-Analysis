<!-- Title -->
<div style="font-size: 1.5em; font-weight: 700; margin-top: 1.5em; margin-bottom: 0.2em;">
  E-Commerce Sales Trends and Customer Analysis
</div>

<p align="center">
  <img src="figures/header_image_ecommerce_sales_trend_and_customer_analysis.png" alt="Header: E-Commerce Sales Trends and Customer Analysis" style="width:90%; max-height:380px; object-fit:cover; border-radius:10px;">
</p>

---

## Table of Contents

1. [Introduction](#introduction)  
2. [Executive Summary](#executive-summary)  
3. [Working Datasets](#working-datasets)  
4. [Detailed Insights](#detailed-insights)  
   - [Sales Trends and Growth Rate](#sales-trends-and-growth-rate)  
   - [Customer Behavior](#customer-behavior)  
5. [Recommendations](#recommendations)  
6. [Assumptions and Caveats](#assumptions-and-caveats)  
7. [Code](#code)

---

## Introduction

<span style="color:#9CA3AF; font-size:0.95em;">
Olist is one of Brazil’s leading e-commerce platforms. Founded in 2015, it connects small and medium-sized businesses with major online marketplaces across the country and is now expanding internationally.
<br><br>
This project uses <a href="https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce" target="_blank">real commercial data</a> from Olist's early operational period (2016–2018), covering over 100,000 orders, to answer:
</span>

<ul>
  <li>How did Olist’s total sales evolve across months and product categories? Are there seasonal patterns or distinct growth phases?</li>
  <li>Can customers be grouped into clusters based on purchasing behavior and value?</li>
  <li>Which customer segments and categories contribute most to revenue and where are the growth opportunities?</li>
</ul>

---

## Executive Summary

<div style="color:#9CA3AF; font-size:0.95em;">
Between 2016 and 2018, Olist processed over 100,000 orders, generating approximately **$4.8M** in sales. The company grew rapidly in 2017 (avg. monthly +14.7%) and stabilized in 2018 (+2.6% monthly). The **Southeast region** (SP, RJ, MG) contributed **~63% of revenue**.
<br><br>
Customer segmentation identified **four primary clusters** (High-Value Premium, Satisfied Low-Spend, Unsatisfied Low-Spend, Loyal Repeat). Clusters 1 and 2 together account for **>80% of revenue**, while improvements in logistics and retention represent high-impact opportunities.
</div>

---

## Working Datasets

<p align="center">
  <img src="figures/Fig_1_ERD_customer_analysis.png" alt="Entity Relationship Diagram" style="width:90%; max-width:1000px; object-fit:cover; border-radius:10px;">
</p>

<div style="text-align:center; color:#9CA3AF; font-size:0.85em; margin-bottom:1.25em;">
  <strong>Figure 1.</strong> Entity Relationship Diagram showing the three relational datasets used in this project.  
  See the <a href="/projects/ecommerce_data_pipeline/" target="_blank" style="color:#9CA3AF;">Data Pipeline</a> project for preprocessing details.  
  <br><span style="font-size:0.8em;">PK: Primary Key; FK: Foreign Key.</span>
</div>

---

## Detailed Insights

### Sales Trends and Growth Rate

<ul style="color:#374151;">
  <li>Olist recorded **~$4.8M** in online sales between 2016–2018 (~$2.2M/year); Average Order Value (AOV) ≈ **$50**, broadly stable.</li>
  <li>Strong growth in 2016–2017 (avg. **+14.7% monthly**); growth slowed to **+2.6%** in 2018 — a stabilization phase.</li>
  <li>The Southeast region (SP, RJ, MG) represents **~63%** of sales (~$3M).</li>
</ul>

<p align="center">
  <img src="figures/Fig_2_ecommerce_sale_trends.png" alt="Sales Trends" width="50%" style="border-radius:10px;">
</p>


<div style="text-align:center; color:#9CA3AF; font-size:0.85em; margin-bottom:1.25em;">
  <strong>Figure 2.</strong> Monthly growth rate, average order value, and total sales (top to bottom). Trends reflect Olist’s early development (2017–2018); late-2016 data were excluded due to low volume and noise.
</div>

### Customer Behavior

<div style="color:#374151;">
Four distinct customer segments were identified by purchase behavior, satisfaction, and delivery experience:
</div>

<ul>
  <li>
    <strong>Cluster 1 – High-Value Premium Buyers</strong>  
    <ul>
      <li>Highest spend per order (~$192) and good satisfaction (~4.0/5).</li>
      <li>Usually one-time purchases but high-margin transactions.</li>
    </ul>
  </li>

  <li>
    <strong>Cluster 2 – Satisfied Low-Spending Shoppers</strong>  
    <ul>
      <li>Largest group; low-ticket purchases (~$34) and high satisfaction (~4.7/5).</li>
      <li>Opportunity for upsell and basket-size growth.</li>
    </ul>
  </li>

  <li>
    <strong>Cluster 3 – Unsatisfied Low-Spending Shoppers</strong>  
    <ul>
      <li>Low satisfaction (~1.8/5); deliveries slower and freight costs high (~37% of order value).</li>
      <li>Indicates logistics/service improvement priority.</li>
    </ul>
  </li>

  <li>
    <strong>Cluster 4 – Loyal Repeat Customers</strong>  
    <ul>
      <li>Only cluster with repeat behavior (~2 orders/customer); satisfaction ~4.1/5; avg order ≈ $45.</li>
      <li>Key audience for retention and LTV uplift.</li>
    </ul>
  </li>
</ul>


<p align="center">
  <img src="figures/Fig_3_ecommerce_customer_clusters.png" alt="Customer Clusters" style="width:50%; max-width:1000px; object-fit:cover; border-radius:10px;">
</p>

<div style="text-align:center; color:#9CA3AF; font-size:0.85em; margin-bottom:1.25em;">
  <strong>Figure 3.</strong> Top: Monthly sales by customer cluster (2017–2018). Bottom: Radar chart of key behavioral and value attributes per cluster.
</div>

<ul>
  <li>Cluster 2 drives ~**47%** of monthly revenue; Cluster 1 ~**36%**; Clusters 3 & 4 share the remainder (~10% and ~6%).</li>
  <li>Only **3.1%** of customers are repeat buyers, contributing **~5.6%** of total revenue.</li>
</ul>

---

## Recommendations

<div style="color:#9CA3AF; font-size:0.95em;">
The analysis highlights immediate opportunities around retention, logistics, and targeted monetization.
</div>

<ul>
  <li><strong>Retain High-Value Buyers:</strong> Loyalty incentives, premium delivery, and exclusive bundles — target <em>Cluster 1</em>.</li>
  <li><strong>Increase AOV among Satisfied Shoppers:</strong> Cross-sell, bundling, and free-shipping thresholds — focus on <em>Cluster 2</em>.</li>
  <li><strong>Fix Delivery Pain Points:</strong> Improve carriers, tracking, and freight strategies to lift satisfaction for <em>Cluster 3</em>.</li>
  <li><strong>Grow Repeat Purchases:</strong> Reactivation campaigns and personalized outreach to expand the small repeat base (~3%).</li>
  <li><strong>Scale Regionally:</strong> Consolidate Southeast wins while piloting targeted expansion in underpenetrated regions.</li>
</ul>

---

## Assumptions and Caveats

<ul>
  <li>The dataset covers a short time span and Olist’s early operational stage; seasonal patterns may not be fully observable.</li>
  <li>Although data volume is large, repeat customers are rare; a classic RFM approach was therefore limited. Instead, alternative behavioral features were used for clustering, offering different but actionable insights.</li>
</ul>

---

## Code

The analysis was implemented in **Python**. Notebooks and scripts for data ingestion, preprocessing, clustering, and visualization are included in this repository.

---

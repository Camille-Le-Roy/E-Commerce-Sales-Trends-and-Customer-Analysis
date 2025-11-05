# E-Commerce Sales Trends and Customer Analysis

![Header Image](figures/header_image_ecommerce_sales_trend_and_customer_analysis.png)

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

Olist is one of Brazil’s leading e-commerce platforms. Founded in 2015, it connects small and medium-sized businesses with major online marketplaces across the country, and is now expanding internationally.

This project uses [real commercial data](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) from Olist's early operational period (2016–2018), encompassing over **100,000 orders**, to explore the following questions:

- How did Olist’s total sales evolve across months and product categories? Are there clear seasonal patterns or growth phases?
- Can customers be grouped into clusters based on their purchasing behavior and value?
- Which customer segments and product categories contribute most to total revenue, and which represent growth opportunities?

---

## Executive Summary

Between 2016 and 2018, Olist processed over **100,000 orders**, generating approximately **$4.8 million in sales**.  
The company experienced rapid expansion in 2017, with an average monthly growth rate of **14.7%**, followed by a stabilization phase in 2018 (**2.6% monthly growth**).

The **Southeast region** (São Paulo, Rio de Janeiro, and Minas Gerais) emerged as the dominant market, contributing **63% of total revenue**.

Customer segmentation revealed **four main behavioral profiles** based on purchasing patterns, satisfaction, and delivery experience:

- **Cluster 1 – High-Value Premium Buyers:** Highest spend per order and strong satisfaction, though mostly one-time purchasers.  
- **Cluster 2 – Satisfied Low-Spending Shoppers:** Largest group; highly satisfied but low-value transactions.  
- **Cluster 3 – Unsatisfied Low-Spending Shoppers:** Low satisfaction due to delivery delays and high freight costs.  
- **Cluster 4 – Loyal Repeat Customers:** Smaller but valuable segment with consistent repeat purchases.

Overall, **Clusters 1 and 2 account for more than 80% of total revenue**, while logistics improvement and customer retention offer strong growth opportunities.

---

## Working Datasets

![Entity Relationship Diagram](figures/Fig_1_ERD_customer_analysis.png)

**Figure 1.** Entity Relationship Diagram showing the three relational datasets used in this project.  
See the [Data Pipeline Project](https://github.com/yourusername/ecommerce_data_pipeline) for details on preprocessing.  
*PK: Primary Key; FK: Foreign Key.*

---

## Detailed Insights

### Sales Trends and Growth Rate

- Olist recorded over **$4.8 million** in online sales between 2016 and 2018 (~$2.2M per year), with an average order value (AOV) of **$50**, remaining stable over time.  
- Strong growth occurred during 2016–2017 (**+14.7% monthly**), followed by slower growth in 2018 (**+2.6%**), indicating market stabilization.  
- The **Southeast region** accounted for **63%** of total sales (~$3M).

![Sales Trends](figures/Fig_2_ecommerce_sale_trends.png)

**Figure 2.** Monthly growth rate, average order value, and total sales (top to bottom).  
The trends capture Olist’s early development phase (2017–2018). Data from late 2016 were excluded due to limited and noisy records.

---

### Customer Behavior

Four distinct customer segments were identified based on purchasing behavior, satisfaction, and delivery performance:

#### Cluster 1 – High-Value Premium Buyers
- Highest spending per order (**≈ $192**) and strong satisfaction (**4.0/5**).  
- Purchase high-value items and receive early deliveries.  
- Mostly one-time buyers but represent high-margin transactions.

#### Cluster 2 – Satisfied Low-Spending Shoppers
- Largest group with low-value purchases (**≈ $34**) and high satisfaction (**4.7/5**).  
- Early deliveries but relatively high freight costs.  
- Happy but casual customers with low repeat behavior.

#### Cluster 3 – Unsatisfied Low-Spending Shoppers
- Lowest satisfaction (**1.8/5**) and small purchases (**≈ $37**).  
- Slower deliveries and freight costs near **37%** of total order value.  
- Reflect service and logistics issues affecting customer experience.

#### Cluster 4 – Loyal Repeat Customers
- Only segment with repeat purchases (**≈ 2 orders per customer**).  
- Moderate prices (**≈ $45**) and satisfaction (**4.1/5**).  
- Stable and loyal group, key for retention strategy.

![Customer Clusters](figures/Fig_3_ecommerce_customer_clusters.png)

**Figure 3.**  
Top: Monthly sales per customer cluster (2017–2018).  
Bottom: Radar chart showing main behavioral and value attributes of each cluster.

**Key findings:**
- Cluster 2 drives **47%** of monthly revenue; Cluster 1 follows with **36%**.  
- Clusters 3 and 4 contribute smaller but consistent shares (**10%** and **6%**).  
- Only **3.1%** of customers made repeat purchases, yet they contributed **5.6%** of total revenue.

---

## Recommendations

The analysis highlights several opportunities to improve Olist’s growth and customer satisfaction.  
Strategic actions should focus on **retention, logistics optimization, and tailored engagement**.

- **Retain High-Value Buyers:** Introduce loyalty programs, premium delivery, or exclusive bundles to encourage repeat purchases (**Cluster 1**).  
- **Convert Satisfied Low-Spending Shoppers:** Encourage higher order values through upselling, recommendations, or free-shipping thresholds (**Cluster 2**).  
- **Improve Delivery Performance:** Address delays and freight issues impacting low-satisfaction customers.  
- **Strengthen Retention:** Since only 3% of customers make repeat purchases, develop reactivation campaigns and personalized follow-ups.  
- **Regional Expansion:** Extend successful Southeast practices into emerging regions.

---

## Assumptions and Caveats

- The dataset covers a short time period and reflects Olist’s early development stage. This limits detection of **seasonal patterns**, which typically appear over longer timelines.  
- Despite the large sample size (100,000+ orders), **repeat customers are rare**, making a traditional RFM segmentation infeasible.  
  Instead, alternative behavioral characteristics were used to identify customer clusters — an unconventional but insightful approach.

---

## Code

The full analysis was implemented in **Python** and is available in this repository.  
See individual notebooks for data preprocessing, analysis, and visualization steps.

---


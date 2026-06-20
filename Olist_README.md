# Brazilian E-Commerce Analysis (Olist) — Data & Business Analytics

An end-to-end analysis of ~100K real orders from Olist, a Brazilian e-commerce marketplace (2016–2018). The project moves from raw relational data through cleaning, multi-table joins, exploratory analysis, and a business-analytics layer that answers real decision-oriented questions.

## TL;DR — Headline Finding

**On-time deliveries average a 4.29 review score; late deliveries average 2.57 — a 1.72-point gap.** Delivery performance is the single clearest driver of customer satisfaction in the dataset. Review scores decline steadily as delivery time increases.

## Dataset

Olist's public dataset: 9 relational tables (orders, order items, payments, reviews, customers, sellers, products, geolocation, category translation) connected by ID keys — structured like a production database, nothing pre-joined.

Source: Brazilian E-Commerce Public Dataset by Olist (Kaggle).

## Key Metrics

| Metric | Value |
|---|---|
| Delivered orders analyzed | 96,470 |
| Total revenue | R$ 13.2M |
| Average order value | R$ ~137 |
| Average review score | 4.16 / 5 |
| Late delivery rate | 8.1% |
| On-time avg score | 4.29 |
| Late avg score | 2.57 |

## Methodology (5 Phases)

1. **Setup & Profiling** — Loaded all 9 tables, documented the grain (what one row means) and join keys for each, verified key integrity across tables.
2. **Cleaning & Feature Engineering** — Parsed timestamps; engineered delivery-timing features (`delivery_days`, `delivery_vs_estimate`, `is_late`); translated product categories to English; pre-aggregated payments and items to order grain to prevent join fan-out.
3. **Joins** — Built a master order-level table (one row per order) and an item-level table (one row per item), validating that joins held grain (no row inflation).
4. **EDA Dashboard** — Order/revenue trends, delivery distributions, review patterns, geographic and category breakdowns, payment behavior.
5. **Business Analytics** — Five decision-oriented analyses with written takeaways.

## Business Findings

1. **Delivery drives satisfaction.** Review score falls steadily with slower delivery; on-time vs late shows a 1.72-point gap.
2. **Revenue concentrates geographically.** São Paulo and the southeast dominate; remote states see slower delivery and lower scores — a logistics-investment signal.
3. **Seller risk segmentation.** Of 804 active sellers (≥20 orders), a subset are high-revenue but low-rated — priority targets for quality intervention.
4. **Installments unlock larger baskets.** Orders with more installments correlate with higher order values.
5. **Category quality gaps.** Several high-revenue categories carry below-average scores — candidates for expectation or quality fixes.

## Tech Stack

Python · pandas · NumPy · matplotlib · Google Colab

## Skills Demonstrated

Relational data modeling · multi-table joins with cardinality control · datetime feature engineering · exploratory data analysis · data visualization · translating analysis into business recommendations.

## Files

- `olist_analysis.ipynb` — full notebook (Phases 0–5)
- `olist_key_findings.csv` — summary metrics table
- `olist_core_insight.png` — headline delivery-vs-satisfaction chart

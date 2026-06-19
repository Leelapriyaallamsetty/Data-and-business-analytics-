# Data Analytics → Business Analytics Project Tracker

A set of beginner-to-intermediate projects, each designed to start as a **data analytics (DA)** exercise and progress into a **business analytics (BA)** layer. Use this as a map so we don’t lose track when going deep on any single project.

-----

## Quick Concept Reminder

- **Data Analytics (DA):** the technical work — acquiring, cleaning, exploring, and visualizing data to find patterns. Tools: Python/pandas, SQL, matplotlib/seaborn.
- **Business Analytics (BA):** applying those findings to decisions — KPIs, segmentation, forecasting, recommendations. BA is essentially DA pointed at a business problem.

Each project below lists both phases so you can take it from raw data to a decision-oriented conclusion.

-----

## Project 1 — Netflix Content Library Analysis

**Summary:** Clean and explore Netflix’s full catalog (titles, genres, countries, ratings, dates).

- **DA phase:** parse multi-value genre/cast columns, handle nulls, analyze content growth over time, movie-vs-TV split.
- **BA phase:** content strategy — is Netflix shifting to TV? Which countries are growing (expansion)? Where are the content gaps?
- **Note:** no viewership/revenue numbers, so BA stays strategic rather than financial.

**Dataset:** <https://www.kaggle.com/datasets/shivamb/netflix-shows>

-----

## Project 2 — Netflix Top 10 Viewership Analysis  ⭐ (current deep dive)

**Summary:** Adds actual viewership (weekly hours viewed) and weeks-on-list, which the catalog dataset lacks.

- **DA phase:** time-series cleaning, ranking trends over weeks.
- **BA phase:** what content drives engagement, English vs non-English performance, country-level popularity for localization decisions.

**Dataset:** <https://www.kaggle.com/datasets/dhruvildave/netflix-top-10-tv-shows-and-films>

-----

## Project 3 — Online Retail / E-commerce Sales

**Summary:** Transaction-level retail data with money, customers, and time.

- **DA phase:** handle returns (negative quantities), missing customer IDs, datetime parsing.
- **BA phase:** RFM customer segmentation, cohort/retention analysis, revenue trends — core business analytics.

**Dataset:** <https://www.kaggle.com/datasets/carrie1/ecommerce-data>

-----

## Project 4 — Superstore Sales (best beginner balance)

**Summary:** Small, clean, well-documented sales dataset.

- **DA phase:** aggregation, grouping, joins across order/product/customer.
- **BA phase:** profit by region/category, the discount-vs-profit tradeoff, which segments lose money — genuinely decision-oriented.

**Dataset:** <https://www.kaggle.com/datasets/vivek468/superstore-dataset-final>

-----

## Project 5 — Telco Customer Churn

**Summary:** Customer accounts with a churn flag.

- **DA phase:** clean mixed types, encode categoricals, explore churn drivers.
- **BA phase:** identify high-risk segments, quantify revenue at risk, recommend retention strategy.

**Dataset:** <https://www.kaggle.com/datasets/blastchar/telco-customer-churn>

-----

## Project 6 — Brazilian E-Commerce (Olist) — advanced

**Summary:** Multi-table relational dataset (orders, payments, reviews, geolocation).

- **DA phase:** join 8+ tables, clean delivery timestamps.
- **BA phase:** delivery performance vs review scores, seller analysis, regional revenue — strong portfolio piece.

**Dataset:** <https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce>

-----

## Suggested Path

1. **Project 1 (Netflix)** — learn EDA mechanics.
1. **Project 4 (Superstore)** or **Project 5 (Churn)** — business-analytics depth with revenue/customer dimensions.
1. **Project 6 (Olist)** — advanced relational + portfolio piece.

*Currently working on: **Project 2 — Netflix Top 10 Viewership Analysis.***

-----

## Core Skills Checklist (track as you go)

- [ ] Loading data with pandas (`pd.read_csv`)
- [ ] Cleaning: nulls, data types, duplicates
- [ ] Exploratory analysis: `.describe()`, `.value_counts()`, group-bys
- [ ] Time-series handling (dates, resampling, trends)
- [ ] Visualization: histograms, bar charts, line/time-series
- [ ] Joins / merging multiple tables
- [ ] Translating findings into business recommendations
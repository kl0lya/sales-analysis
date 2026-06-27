# Global Sales Analysis

## Project Overview

This project simulates a real-world data analyst workflow:

1. **Data ingestion** — loading three relational tables (products, events, countries)
2. **Data cleaning** — handling nulls, fixing data types, standardizing categories, removing duplicates
3. **Feature engineering** — computing revenue, cost, profit, profit margin %, and delivery time
4. **Exploratory analysis** — segmenting by product category, geography, and sales channel
5. **Trend & seasonality analysis** — monthly time-series and day-of-week patterns
6. **Visualization** — 15 production-ready charts built with Matplotlib & Seaborn

---

## Dataset

The analysis uses **3 CSV files**

| File | Description | Key Columns |
|------|-------------|-------------|
| `products.csv` | Product catalog | `id`, `item_type`, `unit_price`, `unit_cost` |
| `events.csv` | Order-level transactions | `order_id`, `product_id`, `country_code`, `units_sold`, `order_date`, `ship_date`, `sales_channel` |
| `countries.csv` | Country metadata | `alpha_3`, `name`, `region`, `sub_region` |

**Join keys:** `events.product_id → products.id` and `events.country_code → countries.alpha_3`

---

## Key Findings

### Financial Performance
- **Cosmetics** and **Household** goods generate the highest absolute profit across all regions
- Average **profit margin is ~40–45%** across all product categories — suggesting centralized pricing strategy
- A minority of countries drive the majority of total profit → high **geographic concentration risk**

### Geography
- **Sub-Saharan Africa** and **Europe** are the top-performing regions by total profit
- **Asia** leads in order volume but shows lower profit margins
- Top 10 countries account for a disproportionately large share of revenue

### Sales Channels
- **Online and Offline** channels contribute roughly equally to total profit
- No statistically significant cost advantage for either channel
- Channel balance indicates a stable **dual-channel strategy**

### Delivery Time
- Average delivery time is **~25 days** with minimal variation across categories and regions
- **Pearson correlation** between delivery days and profit ≈ 0 → faster shipping does not predict higher profit
- Delivery time optimization alone is unlikely to improve financial outcomes

### Trends & Seasonality
- Sales show **no strong long-term upward or downward trend** globally
- **Cosmetics** and **Baby Food** display the most volatile month-to-month patterns
- Most categories are **stable across weekdays** — orders follow business cycles rather than consumer impulse

---

## Visualizations

The project includes **15 charts** across 5 analytical themes:

| Theme | Charts |
|-------|--------|
| Financial Performance | Grouped bar (Revenue/Cost/Profit by category), Profit Margin % bar |
| Geography | Profit by Region (horizontal bar), Top 10 Countries by Profit |
| Sales Channels | Donut chart (Online vs Offline), Grouped bar (channel comparison) |
| Delivery Time | By category, by country, by region + scatter with regression line |
| Trends & Seasonality | 3× monthly line charts, Weekday facet grid, Weekday × Category heatmap |

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| `pandas` | Data loading, cleaning, merging, pivot tables |
| `numpy` | Numeric operations |
| `matplotlib` | Base charting engine, formatters |
| `seaborn` | Statistical plots, heatmaps, facet grids |
| Google Colab | Development environment with Google Drive integration |

---

## Conclusions & Recommendations

| Area | Recommendation |
|------|----------------|
| **Product Mix** | Prioritize Cosmetics and Household in marketing spend — highest absolute profit |
| **Geography** | Investigate high-revenue / low-margin countries for pricing or cost leakage |
| **Channel Strategy** | Maintain dual-channel balance; both channels are equally profitable |
| **Delivery** | Delivery time reduction will not materially improve profit; focus on cost reduction or pricing instead |
| **Demand Volatility** | Introduce demand forecasting for Cosmetics and Baby Food to manage inventory risk |
| **Geographic Risk** | Diversify into emerging markets to reduce profit concentration |

---

## Author

**Olha Klochnyk** — Data Analyst  


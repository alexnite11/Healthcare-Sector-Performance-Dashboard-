# Healthcare Sector Performance Dashboard

**Power BI • DAX • Financial Analytics • API Data Pipeline**

An end-to-end healthcare financial analytics project analyzing quarterly performance data from 10 major U.S. healthcare companies between 2022–2026 using Power BI, Power Query, and DAX. This porject ingested financial statement data through the MeridianMarketFlow API, transformed and modeled the data in Power BI, and delivered an interactive dashboard focused on revenue concentration, R&D performance, and post-pandemic sector trends.

---

## Companies Analyzed

JNJ • PFE • MRK • ABBV • BMY • AMGN • GILD • MDT • ABT • TMO

---

## What This Project Does

* Tracks healthcare sector revenue trends over time
* Analyzes large-cap dominance and sector concentration
* Evaluates profitability among high R&D spenders
* Compares company growth trajectories post-pandemic
* Measures sector performance with and without major outliers like JNJ

---

## Tech Stack

* **Power BI** — Dashboard development & visualization
* **Power Query** — Data transformation & ETL
* **DAX** — Dynamic financial measures & modeling
* **MeridianMarketFlow API** — Quarterly financial statement retrieval

---

## Key Features

* Interactive KPI dashboards
* Dynamic DAX measures
* Revenue ranking system
* Sector contribution analysis
* Cross-page filtering and time slicing
* Large-cap vs non-large-cap segmentation
* High R&D profitability analysis

---

## Sample DAX Measures

### Revenue (Large-Cap)

```DAX
Revenue (Large-Cap) =
CALCULATE(
    SUM(Income[revenue]),
    Income[revenue] > 10000000000
)
```

### Revenue (ex-JNJ)

```DAX
Revenue (ex-JNJ) =
CALCULATE(
    SUM(Income[revenue]),
    Income[ticker] <> "JNJ"
)
```

### Revenue Rank

```DAX
Revenue Rank =
RANKX(
    ALL(Income[ticker]),
    [Total Revenue],
    ,
    DESC
)
```

---

## Key Findings

* Total sector revenue exceeded **$1.99T**
* JNJ alone accounted for nearly **20%** of sector revenue
* Top 3 companies controlled approximately **45%** of total revenue
* AMGN showed the strongest positive growth (+9.95%)
* High R&D firms demonstrated stronger profitability margins
* 2025 data suggests early healthcare sector stabilization after post-pandemic contraction

---



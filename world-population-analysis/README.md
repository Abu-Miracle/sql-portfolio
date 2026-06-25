🌍 World Population Analysis
**Folder:** `world-population-analysis`
 
#### Overview
Exploratory data analysis of global population data across 234 countries spanning from 1970 to 2022, uncovering demographic trends and patterns.
 
#### Key Findings
- **China and India** are the only 'Major Power' nations (>5% of world population) — just **7 countries** account for **51% of the world's population**
- **UAE and Qatar** had the highest population growth since 1970 — driven by oil wealth attracting millions of foreign workers
- **Macau** is the most densely populated territory; **Greenland** the least
- **142 countries** (61%) are in the 'Slowly Growing' band — including the world's largest nations
- World population growth is **decelerating** — the 1980–1990 decade had the highest absolute growth
- **Asian countries** dominated the fastest-growing nations list since 1970
#### SQL Concepts Demonstrated
- `UNION ALL` — Unpivoting year columns into rows
- `LAG()` — Year over year growth calculations
- `DENSE_RANK()` — Top 3 countries per continent
- `SUM() OVER()` — Running totals of world population percentage
- `CROSS JOIN` — Generating all possible combinations
- CTEs and Window Functions
- `CASE` statements for population categorization


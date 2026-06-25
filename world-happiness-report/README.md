 😊 World Happiness Report Analysis (2015–2016)

**Folder:** `world-happiness-report`
 
#### Overview
Exploratory data analysis of the World Happiness Report, comparing happiness scores, rankings and contributing factors (Economy, Family, Health, Freedom, Trust, Generosity) across 150+ countries between 2015 and 2016.
 
#### Key Findings
- **Economy (GDP per Capita)** is the single largest contributor to happiness scores globally, ahead of Family, Health, Freedom, Trust and Generosity
- **Western Europe** dominates the global happiness rankings — 7 of the 10 countries that consistently ranked in the global top 10 across both years are Western European, with the remainder from North America and Australia/New Zealand
- Built a reusable **stored procedure** (`Get_Country_Profile`) to pull a side-by-side 2015 vs 2016 happiness profile for any country, including score/rank deltas and all underlying factor scores
- Identified each country's **dominant happiness factor** using `GREATEST()` combined with `CASE`, then aggregated to find the most common dominant factor per region
- Tracked **year-over-year trends**, labeling each country as Improving, Declining or Stable, and surfaced the top 5 most-improved countries within each region
#### SQL Concepts Demonstrated
- `GREATEST()` — Finding the maximum value across multiple columns
- CTEs combined with `RANK()` — Regional and category-based rankings
- Stored Procedures with `IN` parameters — Reusable country profile lookups
- `JOIN` across two yearly datasets — Year-over-year comparison
- `LEFT JOIN` / `RIGHT JOIN` — Identifying countries present in one year but not the other
- Temporary Tables — Consolidated multi-metric analysis table
- `CASE` statements — Trend categorization (Improving/Declining/Stable)
- `GROUP BY`, `HAVING`, Window Functions — Regional aggregations and rankings


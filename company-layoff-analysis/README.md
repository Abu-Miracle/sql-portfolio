🏢 Company Layoffs Analysis (2020–2023)

**Folder:** `company-layoff-analysis`
 
#### Overview
Analysis of global tech company layoffs from 2020 to 2023, covering data cleaning and in-depth exploratory data analysis to uncover trends and patterns.
 
#### Data Cleaning
- Removed duplicate records using `ROW_NUMBER()` and staging tables
- Standardized inconsistent industry names (e.g. Crypto, CryptoCurrency → Crypto)
- Handled NULL and blank values
- Converted date columns from TEXT to DATE format
- Removed redundant columns
#### Key Findings
- **2022** saw a **900%+ jump** in layoffs compared to 2021 — driven by rising interest rates and the collapse of the post-COVID tech boom
- **San Francisco Bay Area** was the hardest hit city with **430+ layoff events** and over **125,000 jobs lost**
- **Seed stage** companies had the highest average percentage of workforce laid off (~70%) — highlighting their vulnerability
- Just **7 companies** accounted for a disproportionate share of total layoffs
#### SQL Concepts Demonstrated
- `ROW_NUMBER()`, `RANK()`, `DENSE_RANK()` — Window Functions
- CTEs and Subqueries
- `GROUP BY`, `HAVING`, `ORDER BY`
- `STR_TO_DATE()`, `TRIM()`, `LIKE` — String Functions
- Self JOINs for data population
- Rolling totals with `SUM() OVER(ORDER BY)`

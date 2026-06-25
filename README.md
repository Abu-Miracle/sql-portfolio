# 📊 SQL Portfolio — Abu Miracle
 
A collection of real-world SQL projects demonstrating data cleaning, exploratory data analysis (EDA) and advanced querying using MySQL.
 
---
 
## 🛠️ Tools & Skills
- **Database:** MySQL
- **Skills:** Data Cleaning, Exploratory Data Analysis, Window Functions, CTEs, Subqueries, Stored Procedures, Triggers, Joins, Aggregations
---
 
## 📁 Projects
 
---
 
### 1. 🏢 Company Layoffs Analysis (2020–2023)
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
---
 
### 2. 🏠 Nashville Housing Data Cleaning (2013–2016)
**Folder:** `nashville_housing_data`
 
#### Overview
Comprehensive data cleaning project on a Nashville, Tennessee real estate dataset with 56,000+ property sales records.
 
#### Data Cleaning Steps
- Imported 56,636 rows using `LOAD DATA INFILE`
- Removed 104 duplicate records
- Dropped redundant columns (`blank_col`, `unnamed_index`, `image`, `owner_state`)
- Trimmed whitespace and removed hidden carriage return characters (`\r`) from text columns
- Standardized `land_use` categories (e.g. `GRRENBELT/RES` → `GREENBELT/RES`)
- Converted empty strings to `NULL` using `NULLIF()`
- Converted `sale_date` from TEXT to DATE format
- Converted numeric columns from TEXT to proper INT/DECIMAL types
- Populated missing `property_address` and `property_city` using self JOINs on `parcel_id`
#### Key Findings
- **Vacant Commercial Land** had the highest average sale price
- **Single Family** homes had the most sales — the most common property type
- **3 bedroom** properties were the most common, while **11–12 bedroom** properties commanded the highest average prices
- The top 10 most expensive sales were **7 condo units at the same address** sold in a bulk purchase — a real world data anomaly worth flagging
- **72%** of properties had `total_value = land_value + building_value`, with an average difference of $2,525 for the remaining 28%
#### SQL Concepts Demonstrated
- `LOAD DATA INFILE` — Fast CSV importing
- `NULLIF()` — Converting empty strings to NULL
- `HEX()` — Detecting hidden characters
- `TRIM(TRAILING)` — Removing specific trailing characters
- `MODIFY COLUMN` — Changing column data types
- Self JOINs for NULL population
- `STR_TO_DATE()` — Date conversion
- `ALTER TABLE DROP COLUMN` — Removing redundant columns
---
 
### 3. 🌍 World Population Analysis
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
---
 
### 4. 😊 World Happiness Report Analysis (2015–2016)
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
---
 
## 📬 Contact
- **GitHub:** [Abu-Miracle](https://github.com/Abu-Miracle)

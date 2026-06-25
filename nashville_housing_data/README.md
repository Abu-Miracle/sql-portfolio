🏠 Nashville Housing Data Cleaning (2013–2016)

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

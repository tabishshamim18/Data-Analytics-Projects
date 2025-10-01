# 🗃️ Global Layoffs Analysis (SQL Project)

## 📌 Project Overview
This project focuses on analyzing **global layoff trends** using SQL, leveraging real-world datasets to uncover patterns in **company layoffs**, **industry impact**, and **temporal trends**.  

The goal is to:
- Understand the **scale and distribution** of layoffs across industries, countries, and time periods.  
- Identify **patterns and anomalies**, such as spikes in specific years, industries, or companies.  
- Build **recruiter- and business-friendly insights** that demonstrate data storytelling using only SQL.

This project highlights my ability to **structure complex queries**, **clean and transform data**, and **derive meaningful business insights** using pure SQL.

---

## 🧠 Business Problem
Global layoffs — especially post-pandemic — have had significant impacts on industries, economies, and job markets.  

Organizations and analysts need to:
- Track **layoff volumes and trends over time**.  
- Identify **industries and regions** most affected.  
- Pinpoint **companies and periods** with unusually high layoffs.  
- Use historical patterns to inform workforce planning and strategic decisions.

---

## 📂 Dataset Description
**File:** `layoffs.sql` (includes table creation and data insertion or queries to run against a pre-existing table)

**Table:** `layoffs`  
| Column Name         | Description                                      |
|---------------------|--------------------------------------------------|
| `company`           | Company name                                     |
| `location`          | City or region where layoffs occurred            |
| `industry`          | Industry type (e.g., Tech, Finance, Retail)      |
| `total_laid_off`    | Number of employees laid off                     |
| `percentage_laid_off` | % of workforce laid off (if available)          |
| `date`              | Date of the layoff                               |
| `country`           | Country name                                     |
| `stage`             | Company stage (Startup, Post-IPO, etc.)          |
| `funds_raised`      | Total funding (where available)                  |

📌 *The dataset is cleaned and transformed for SQL analysis. Dates are standardized, null values are handled, and duplicates are removed.*

---

## 🛠️ Tools & Skills Used
- **SQL**: Data cleaning, transformation, aggregation, window functions, CTEs, subqueries.  
- **Database**: MySQL / PostgreSQL (can be run in any RDBMS supporting standard SQL).  
- **GitHub**: Version control and documentation.

Key SQL concepts demonstrated:
- `GROUP BY` and `HAVING` for aggregated insights  
- `WINDOW FUNCTIONS` (`ROW_NUMBER()`, `RANK()`) for ranking companies and identifying trends  
- `DATE FUNCTIONS` for time-based analysis  
- `CTEs` for structuring complex queries  
- Subqueries and joins for advanced transformations

---

## 🧭 Analysis Performed

### 1️⃣ **Data Cleaning**
- Removed duplicates using `ROW_NUMBER()` over key fields.  
- Standardized `date` column using `STR_TO_DATE()` or equivalent.  
- Replaced blank industries or locations with `NULL` and handled missing data gracefully.  
- Trimmed whitespace and normalized text fields.

### 2️⃣ **Exploratory Analysis**
- Total layoffs across **industries**, **countries**, and **years**.  
- Top companies by layoffs.  
- Percentage layoffs to find companies most affected relative to size.  
- Monthly and yearly layoff trends.

Example queries:
```sql
SELECT industry, SUM(total_laid_off) AS total_layoffs
FROM layoffs
GROUP BY industry
ORDER BY total_layoffs DESC;


SELECT country, EXTRACT(YEAR FROM date) AS year, SUM(total_laid_off) AS yearly_layoffs
FROM layoffs
GROUP BY country, year
ORDER BY yearly_layoffs DESC;
```

3️⃣ Trend & Ranking Analysis

Year-over-year change in layoffs by industry.

Top 5 companies by layoffs per year using window functions:

```sql
SELECT company, EXTRACT(YEAR FROM date) AS year, total_laid_off,
RANK() OVER (PARTITION BY EXTRACT(YEAR FROM date) ORDER BY total_laid_off DESC) AS company_rank
FROM layoffs;
```

📈 Key Insights (Example — replace with your actual findings)

📌 Technology sector accounted for the highest layoffs globally, particularly in 2022–2023.

📌 Layoffs were concentrated in North America, with the US leading by a significant margin.

📌 Certain startups laid off 100% of their workforce, indicating shutdowns.

📌 Post-IPO companies showed a spike in layoffs after funding slowdowns.

📌 Layoffs peaked in Q1 2023, likely linked to macroeconomic conditions and restructuring waves.

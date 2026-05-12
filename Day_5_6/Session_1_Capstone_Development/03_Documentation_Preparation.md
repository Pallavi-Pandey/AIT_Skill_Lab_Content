# Documentation Preparation

> **Learning Goal:** Understand what professional project documentation looks like, write a project README, and structure a technical report that anyone in the team can maintain.

---

## Why Documentation Is Part of the Deliverable

Documentation is not an afterthought — it is the difference between a project that lives on and one that dies the moment the person who built it leaves the company.

When a new analyst joins a team six months from now and opens your project folder, they need to understand:
- What problem this project solves.
- Where the data came from and what it means.
- What analytical decisions were made and why.
- Where to find the final outputs.

Without documentation, none of that is possible from the files alone.

---

## What to Document: The Five Pillars

### 1. Problem Statement
A clear, jargon-free description of the business problem you were asked to solve.

**Template:**
> "[Company/Scenario] is experiencing [specific problem]. The goal of this project is to [analytical objective] in order to [business outcome]. Success is measured by [1-2 primary KPIs]."

**Example:**
> "FreshRetail Pvt. Ltd. is losing Rs. 50 Lakhs per month due to dairy product expiry. The goal of this project is to analyze demand patterns and inventory levels across 12 store locations to identify over-stocking root causes. Success is measured by a reduction in Waste Percentage and an improvement in Inventory Turnover Ratio."

---

### 2. Dataset Description
Describe every table and every key column that was used in the analysis.

**What to include:**
- Source of data (provided CSV, Kaggle, generated, etc.)
- Number of rows and columns
- Date range covered
- Key columns with their data type, description, and any known quality issues

**Example table:**

| Column Name | Data Type | Description | Quality Notes |
|-------------|-----------|-------------|---------------|
| `store_id` | Integer | Unique store identifier (1–12) | No nulls found |
| `product_sku` | String | Stock Keeping Unit code | 3% had invalid codes; removed |
| `quantity_sold` | Integer | Units sold per day | 0.7% negative values; treated as returns |
| `expiry_date` | Date | Product expiry date | 12% missing; imputed with median shelf life |

---

### 3. Methodology
Describe the analytical steps taken, in order. Think of this as a recipe — someone should be able to reproduce your results by following it.

**Standard sections to include:**

**Data Cleaning:**
List every transformation applied and the reason for it.
- "Removed 143 duplicate rows identified by (store_id, product_sku, date) composite key."
- "Converted expiry_date column from string (DD-MM-YYYY) to datetime format."
- "Imputed missing quantity_sold with 0 (confirmed with business team: missing = no sale reported)."

**Exploratory Analysis:**
Summarize what the initial exploration revealed.
- "Distribution of waste_percentage is right-skewed. Median (4.2%) is more representative than mean (7.8%)."
- "Correlation between quantity_ordered and quantity_sold is 0.61 — moderate, not perfect, indicating ordering is not purely demand-driven."

**Key Analytical Techniques:**
- "Used GROUP BY aggregation to compute weekly inventory turnover by store."
- "Applied IQR method to detect outlier stores with turnover ratio below Q1 − 1.5*IQR."

---

### 4. Key Findings
List the top 3 to 5 validated insights from your analysis. Each finding must follow the What → So What → Now What structure.

**Example:**
> **Finding 1:** Store #7 (Whitefield branch) accounts for 38% of total waste despite representing only 9% of total sales volume.
>
> **So What:** A single underperforming location is disproportionately responsible for losses.
>
> **Now What:** Conduct a separate inventory audit at Store #7 and review its ordering authority.

---

### 5. Limitations
Every dataset has limitations. Documenting them shows intellectual honesty and analytical maturity.

**Common limitations to acknowledge:**
- "The dataset covers only 90 days (Jan–Mar 2023). Seasonal patterns beyond Q1 are not captured."
- "Expiry dates for 12% of records were imputed using median shelf life. Actual expiry may differ."
- "Customer demand data was not available. Demand was approximated using sales quantity."
- "The analysis is descriptive, not predictive. It identifies where waste is occurring, not what will happen next."

---

## How to Write a Project README

A README file is the front door of your project. It should be written in Markdown and live in the root of your project folder.

**Recommended README Structure:**

```
# Project Title

## Problem Statement
One paragraph.

## Dataset
- Source:
- Rows:
- Columns:
- Time Period:

## Tools Used
- Python 3.x, Pandas, Matplotlib
- Power BI Desktop / Tableau Public
- SQL (SQLite / MySQL)

## How to Run
Step-by-step instructions.

## Key Findings
1. Finding 1
2. Finding 2
3. Finding 3

## Team Members
- Name — Role
- Name — Role

## Limitations
Bullet list.
```

---

## Structuring a Technical Report

For programs or internships that require a written report alongside the dashboard, use this structure:

| Section | Content | Recommended Length |
|---------|---------|-------------------|
| **Title Page** | Project name, team members, date, institution | 1 page |
| **Executive Summary** | Problem, approach, top 3 findings, recommendation — written for a non-technical manager | 1 page |
| **Introduction** | Background, problem statement, scope of analysis | 1–2 pages |
| **Data Description** | Dataset overview table, data quality issues found and resolved | 1–2 pages |
| **Methodology** | Cleaning steps, analytical techniques, tools used | 2–3 pages |
| **Results & Insights** | Charts, tables, and validated findings with "So What?" analysis | 3–5 pages |
| **Recommendations** | Actionable "Now What?" decisions for the business | 1 page |
| **Limitations & Future Work** | What is not covered, what could be done with more data/time | 1 page |
| **Appendix** | Raw query results, Python code snippets, extra charts | As needed |

---

## Documentation Checklist

| # | Item | Done (Yes / No) |
|---|------|----------------|
| 1 | Problem Statement written in plain business language | |
| 2 | Dataset description table completed (all key columns documented) | |
| 3 | Data cleaning steps listed with reasons | |
| 4 | Methodology section can reproduce results from scratch | |
| 5 | Top 3–5 findings documented using What/So What/Now What format | |
| 6 | At least 2 limitations acknowledged | |
| 7 | Project README.md file exists in the project folder | |
| 8 | README includes how-to-run instructions | |
| 9 | All file names are descriptive (not "analysis_final_v3_REAL.csv") | |
| 10 | Team members and roles are listed | |
| 11 | Dashboard file (.pbix/.twbx) and documentation are in the same folder | |
| 12 | Submission folder zipped and named: TeamName_Capstone_Day5.zip | |

---

## Quick Check Questions

1. Why is "Data Source: Kaggle" an insufficient dataset description for a professional report?
2. A colleague who was not part of your team should be able to reproduce your analysis. What is the single most important section of documentation that makes this possible?
3. Your dataset covered only 3 months of data but your finding is "Sales are higher in summer." Why is this a limitation, and how should you document it?

---

[Previous](02_Insight_Validation.md) | [Home](../../README.md) | [Next](Lab_Capstone_Final_Review.md)

# Day 1: Foundations of Data Analytics

> **Theme:** Build the foundation. Understand what data analytics is, where data comes from, how to clean it, and how Python makes it all possible.

---

## Overview

| # | Session | What You Learn |
|---|---------|----------------|
| 1 | **Introduction to Analytics** | Data Analytics lifecycle, 4 types of analytics, industry use cases, career pathways |
| 2 | **Data Collection & Cleaning** | CSV / API / database sources, handling missing values, removing duplicates, data transformation |
| 3 | **Python for Analytics** | NumPy arrays, Pandas DataFrames, filtering, Boolean indexing, GroupBy & aggregation |
| — | **Mini Project** | End-to-end SuperMart Sales Intelligence pipeline combining all Day 1 topics |

---

## Sessions

### Session 1: Introduction to Data Analytics
Understand the "why" before the "how." This session sets the context for the entire bootcamp.

- [01 - Data Analytics Lifecycle](Session_1_Introduction/01_Data_Analytics_Lifecycle.md)
- [02 - Types of Analytics](Session_1_Introduction/02_Types_of_Analytics.md)
- [03 - Industry Applications & Career Paths](Session_1_Introduction/03_Industry_Applications_Career.md)
- Lab: `Session_1_Introduction/Lab_VSCode_Dataset_Exploration.py`

---

### Session 2: Data Collection & Cleaning
Real-world data is always messy. This session teaches you to find, load, and fix it.

- [01 - Data Sources: CSV, API, Databases](Session_2_Data_Collection_Cleaning/01_Data_Sources_CSV_API_Databases.md)
- [02 - Handling Missing Values](Session_2_Data_Collection_Cleaning/02_Handling_Missing_Values.md)
- [03 - Duplicates & Transformation](Session_2_Data_Collection_Cleaning/03_Duplicates_Transformation.md)
- Lab: `Session_2_Data_Collection_Cleaning/Lab_VSCode_Data_Cleaning.py`

---

### Session 3: Python for Analytics
The toolkit every analyst needs — NumPy for numbers, Pandas for tables.

- [01 - NumPy Introduction](Session_3_Python_for_Analytics/01_NumPy_Introduction.md)
- [02 - Pandas DataFrame Operations](Session_3_Python_for_Analytics/02_Pandas_DataFrame_Operations.md)
- [03 - Filtering & Aggregation](Session_3_Python_for_Analytics/03_Filtering_Aggregation.md)
- Lab: `Session_3_Python_for_Analytics/Lab_VSCode_Dataset_Manipulation.py`

---

### Mini Project: SuperMart Sales Intelligence
Apply everything from Day 1 to a realistic retail dataset. Clean messy data, calculate revenue metrics, and build a 6-panel visualization dashboard.

- [Mini Project README](Mini_Project_SuperMart/README.md)
- Script: `Mini_Project_SuperMart/scripts/supermart_analysis.py`
- Notebook: `Mini_Project_SuperMart/notebooks/SuperMart_Analysis_Colab.ipynb`

```bash
cd Mini_Project_SuperMart/scripts
python 00_generate_data.py
python supermart_analysis.py
```

---

## Key Skills Gained

- Describe each stage of the Data Analytics lifecycle
- Load and inspect a CSV dataset with Pandas
- Fix 5+ types of data quality issues (nulls, duplicates, type errors, inconsistent text, invalid ranges)
- Apply NumPy vectorized operations for fast computation
- Group and aggregate data to answer business questions

---

[Home](../README.md) | [Next: Day 2](../Day_2/README.md)

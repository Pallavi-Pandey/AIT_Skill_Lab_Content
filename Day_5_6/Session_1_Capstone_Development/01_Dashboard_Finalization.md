# Dashboard Finalization

> **Learning Goal:** Understand what "done" looks like for a professional analytics dashboard and apply a structured polish process before submission.

---

## What Does "Finalized" Mean?

A dashboard is not finished just because the charts load. A finalized dashboard meets three standards simultaneously:

- **Functional**: Every visual updates correctly when a filter is applied. No broken relationships, no blank visuals.
- **Accurate**: Every number displayed can be traced back to the source data. No unexplained discrepancies.
- **Professional**: A non-technical manager can open the file, understand the purpose within 10 seconds, and navigate it without guidance.

If your dashboard fails any one of these three tests, it is not yet finalized.

---

## The Five Elements Every Capstone Dashboard Must Have

### 1. KPI Cards (The "Health Check" Row)
Place 3 to 5 large-number cards at the very top of the page. These are the first things a decision-maker sees. Each card should answer a single business question.

**Good examples:**
- Total Revenue: Rs. 4.2 Cr
- Customer Churn Rate: 18.4%
- Average Patient Wait Time: 23 min

**Common mistake:** Showing raw counts with no context (e.g., "Transactions: 8,421" without specifying the period or comparison).

### 2. Trend Charts
At least one time-series chart (line or bar) showing how the key metric changes over time. Trends answer the question "Is the situation improving or getting worse?"

### 3. Breakdown Charts
A chart that breaks the main metric into sub-categories (e.g., Revenue by Region, Fraud by City Tier). These identify where the problem is concentrated.

### 4. Interactive Filters / Slicers
At minimum: a Date/Period slicer and one categorical slicer (Region, Category, Department). Test every slicer to confirm all visuals respond correctly.

### 5. A Descriptive Title and Subtitle
Every page of your dashboard must have a clear title ("E-Commerce Retention Analysis — FY 2023") and a one-line subtitle that states the business context ("Identifying churn drivers across product categories for strategic intervention").

---

## Power BI Polish Tips

| Area | What to Fix |
|------|------------|
| **Canvas Background** | Set a consistent light or dark background. Avoid leaving the default white unless your company theme requires it. |
| **Font Consistency** | Use one font family throughout (Segoe UI is the Power BI default). Titles: 16–18pt. Labels: 10–11pt. |
| **Color Theme** | Go to `View > Themes` and apply a consistent theme. Never use rainbow colours on a single chart. |
| **Grid Alignment** | Right-click any visual > `Align` to snap visuals to a shared edge. Misaligned cards look unprofessional. |
| **Data Labels** | Add data labels to bar charts. Format numbers with commas (1,00,000) not raw integers (100000). |
| **Tooltip** | Customize tooltips to show the metric name, value, and comparison period, not just a raw number. |
| **Report Page Name** | Rename tabs from "Page 1" to something meaningful: "Overview", "Customer Deep-Dive", "Operational Trends". |

## Tableau Polish Tips

| Area | What to Fix |
|------|------------|
| **Dashboard Layout** | Use "Fixed Size" layout (1200x900) for consistent rendering across screens. |
| **Sheet Naming** | Name every sheet clearly before embedding in the dashboard. "Sheet 7" tells the audience nothing. |
| **Color Palette** | Use `Color > Edit Colors` to apply a consistent scheme. Limit to 3–4 colors maximum. |
| **Null Handling** | Right-click the axis > `Format` > `Special Values` to control how NULLs are displayed. |
| **Action Filters** | Add Dashboard Actions (Dashboard > Actions) so clicking one chart filters others. Test each action. |
| **Legends** | Remove redundant legends. If the chart title already says "Revenue by Region," a separate color legend is visual clutter. |

---

## Final Dashboard Checklist

Use this table to audit your dashboard before submission. Every row must be marked "Yes."

| # | Check Item | Status (Yes / No) |
|---|-----------|------------------|
| 1 | All KPI cards display correct aggregated values | |
| 2 | KPI values match the raw data when manually calculated | |
| 3 | At least one trend (time-series) chart is present | |
| 4 | At least one breakdown chart (by category/region) is present | |
| 5 | All slicers / filters are functional and tested | |
| 6 | No visual shows a blank or "No data available" state unexpectedly | |
| 7 | All chart titles are descriptive and spell-checked | |
| 8 | Dashboard page(s) have clear, meaningful names | |
| 9 | A single consistent color theme is applied | |
| 10 | Font sizes are consistent across all visuals | |
| 11 | Data labels are present and correctly formatted (commas, %, etc.) | |
| 12 | The dashboard purpose is clear within 10 seconds of opening | |
| 13 | The file opens without errors on a fresh machine | |
| 14 | File is saved in the correct format (.pbix or .twbx) | |
| 15 | Team name and project title appear on the dashboard | |

---

## Common Mistakes to Fix Before Submission

1. **Wrong aggregation**: A SUM where an AVERAGE was needed, or a COUNT where a DISTINCT COUNT was needed. Always ask: "What does this number represent?"

2. **Broken relationships**: In Power BI, go to `Model View` and verify every table relationship is active (solid line, not dotted). A dotted line means the relationship is inactive and your cross-filter will not work.

3. **Overlapping visuals**: Charts that visually overlap each other when the report is exported to PDF. Test the PDF export explicitly.

4. **No date table**: If you have a time-series chart, you should have a proper Date/Calendar table in your model. Relying on raw date columns causes incorrect sorting and missing gaps.

5. **Inconsistent currency formatting**: If your dataset is in Indian Rupees, every monetary KPI must show the Rs. or INR prefix. Do not mix Rs. on one card and a bare number on another.

---

## Quick Check Questions

1. Your KPI card shows "Total Revenue: 4200000". What formatting change should you make before presenting to management?
2. A team member says "The dashboard is done — the charts all show data." What three tests should you still run before calling it finalized?
3. Why is it important to rename dashboard page tabs from "Page 1" to a meaningful name?

---

[Previous](../../Day_4/Session_3_Capstone_Initiation/03_Project_Planning_Template.md) | [Home](../../README.md) | [Next](02_Insight_Validation.md)

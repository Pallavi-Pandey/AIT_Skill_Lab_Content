# Insight Validation

> **Learning Goal:** Learn how to verify that every insight in your capstone is factually correct, logically sound, and genuinely useful — before you stand in front of a jury.

---

## Why Validation Matters

Generating a chart is easy. Generating a *correct* chart is harder. A dashboard full of beautiful visuals that contain wrong numbers is worse than no dashboard at all — it leads decision-makers to act on false information.

**The core principle:** Every number you show must be traceable back to the raw data by someone other than you.

---

## The Three Validation Layers

### Layer 1: Cross-Check with Raw Data
Before trusting any aggregated metric in your BI tool, verify it against the source.

**Step-by-step:**
1. Note the value shown in your dashboard (e.g., "Average Order Value: Rs. 1,247").
2. Open the raw CSV or database table.
3. Run the same calculation manually using Python or SQL.

```python
# Python cross-check example
import pandas as pd
df = pd.read_csv('orders.csv')
aov = df['order_value'].mean()
print(f"Manual AOV: Rs. {aov:.2f}")
```

```sql
-- SQL cross-check example
SELECT AVG(order_value) AS avg_order_value
FROM orders;
```

4. Compare. If the values differ by more than rounding (e.g., Rs. 1,247 vs. Rs. 1,246.83), investigate the cause. The most common culprits are: null values being counted differently, wrong date filters, or duplicate rows.

---

### Layer 2: Peer Review
Your own team is too close to the work to spot all errors. A structured peer review catches mistakes that familiarity hides.

**How to run a peer review:**
- Swap your dashboard file with another team for 10 minutes.
- The reviewing team tries to "break" the dashboard: they apply every filter, look for unexpected blanks, and question every number.
- They complete the peer review questions below and return written feedback.

**Peer Review Questions (for the reviewing team):**
1. Does each KPI card have a clear label and unit? What unit is it in?
2. Pick any bar in any chart. Can you trace that value back to a row in the raw data?
3. Apply the Date slicer to just one month. Do ALL visuals update or do some ignore the filter?
4. Is there any insight on the dashboard where your first reaction is "Really? That seems too high/low."?
5. What is the #1 thing that is confusing about this dashboard?

---

### Layer 3: Sanity Checks
A sanity check asks: "Does this number make sense in the real world?"

| Metric | Sanity Check Question |
|--------|-----------------------|
| Customer Churn Rate | Is it between 5% and 40%? Anything outside that range for a retail business is suspicious. |
| Average Basket Size (e-commerce) | Is it between Rs. 300 and Rs. 5,000? A basket of Rs. 50 or Rs. 50,000 needs explanation. |
| Hospital Wait Time | Is it between 5 and 120 minutes? 200+ minutes or negative values signal a data error. |
| Fraud Rate | Is it below 5%? A 50% fraud rate would mean the business cannot survive — investigate. |
| Inventory Turnover | Is it between 2 and 15 for a retail business? Single-digit is common; above 20 is unusual. |

If a metric fails a sanity check, do not hide it — investigate and document the reason.

---

## Common Insight Mistakes

### Mistake 1: Correlation vs. Causation
**Wrong insight:** "Cities with higher temperatures have higher ice cream sales. Therefore, heat causes ice cream sales."
**Why it is wrong:** Both could be caused by a third factor (summer holidays). Always say "associated with" not "causes."

### Mistake 2: Misleading Averages
**Wrong insight:** "The average patient wait time is 18 minutes — performance is good."
**Why it is wrong:** If 90% of patients wait 5 minutes and 10% wait 3 hours, the average hides the crisis for the 10%.
**Fix:** Add median and 90th percentile alongside the mean.

### Mistake 3: Cherry-Picking Time Ranges
**Wrong insight:** "Revenue grew 40% this quarter!"
**Why it is wrong:** If last quarter was unusually bad (due to a holiday shutdown), the comparison is misleading.
**Fix:** Always show Year-over-Year comparisons alongside Quarter-over-Quarter.

### Mistake 4: Absolute vs. Relative Numbers
**Wrong insight:** "Category A has 500 returns; Category B has 200 returns. Category A is worse."
**Why it is wrong:** If Category A sold 50,000 units and Category B sold 2,000 units, Category B's return *rate* (10%) is far worse than Category A's (1%).
**Fix:** Always show the rate (percentage) alongside the absolute count.

---

## The "So What?" Test

For every insight on your dashboard, ask yourself three questions. If you cannot answer all three, the insight is not ready.

| Question | What a Strong Answer Looks Like |
|----------|---------------------------------|
| **What?** | "Our churn rate in the 25–34 age group is 32%, which is 14 points higher than the company average." |
| **So What?** | "This means we are losing our most valuable long-term customers at a disproportionate rate." |
| **Now What?** | "We should launch a loyalty programme specifically targeting the 25–34 segment with personalised offers." |

Practice this out loud with every insight before the presentation. If a team member cannot complete all three sentences for any finding, that finding needs more work.

---

## Practical Validation Steps: A Workflow

```
Step 1  Cross-check top 3 KPIs against raw data (Python/SQL)
   └── Mismatch found?  Investigate source, fix model relationship, re-verify.
   └── Values match?  Move to Step 2.

Step 2  Peer review swap (10 minutes with another team)
   └── Issues reported?  Fix, then re-run your own cross-check on changed visuals.
   └── No critical issues?  Move to Step 3.

Step 3  Sanity check every metric against real-world benchmarks
   └── Anomaly found?  Document explanation or fix.
   └── All pass?  Move to Step 4.

Step 4  Apply "So What?" test to every insight
   └── Cannot answer?  Strengthen the insight or remove it.
   └── All pass?  Dashboard insights are validated. Proceed to documentation.
```

---

## Quick Check Questions

1. Your dashboard shows "Total Fraud Amount: Rs. 2.4 Cr." You run `df['fraud_amount'].sum()` in Python and get Rs. 1.8 Cr. What are three possible reasons for this discrepancy?
2. A team says their insight is "Sales are highest on Fridays." What two follow-up "So What?" questions should the jury ask?
3. Why is showing only the average wait time potentially misleading for a hospital dashboard?

---

[Previous](01_Dashboard_Finalization.md) | [Home](../../README.md) | [Next](03_Documentation_Preparation.md)

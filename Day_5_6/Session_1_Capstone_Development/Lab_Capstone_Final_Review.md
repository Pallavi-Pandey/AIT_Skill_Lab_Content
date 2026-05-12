# Lab: Capstone Final Review

> **Objective:** Use the final development session to systematically review, fix, and freeze your capstone project before the presentation window opens. Every item below must be completed.

---

## Time Allocation Guide

This lab is designed for the final 3-hour block before presentations begin. Follow this schedule strictly — the clock is your biggest risk.

| Time Block | Duration | What Your Team Does |
|------------|----------|---------------------|
| **Block 1** | 0:00 – 0:30 | Dashboard final polish and checklist audit |
| **Block 2** | 0:30 – 1:00 | Insight validation (cross-check top 3 KPIs, run "So What?" test) |
| **Block 3** | 1:00 – 1:30 | Peer review swap with another team |
| **Block 4** | 1:30 – 2:00 | Fix issues found in peer review, finalize documentation |
| **Block 5** | 2:00 – 2:30 | Presentation dry run (practice the 10-minute pitch internally) |
| **Block 6** | 2:30 – 3:00 | Package and submit: zip the folder, share the file with facilitator |

> **Rule:** No new features after Block 2. Trying to add a new chart 30 minutes before the presentation is one of the most common reasons teams crash during demos.

---

## Part 1: Self-Review — Dashboard Audit

Work through the following checklist as a team. Assign one team member to read each item aloud and another to verify it on screen.

### Functional Check
- [ ] Open the dashboard on a fresh machine or in an incognito/new browser profile. Does it load without errors?
- [ ] Apply the Date slicer. Do all visuals update? Are there any that stay static?
- [ ] Apply the categorical slicer (Region / Category / Department). Repeat the check above.
- [ ] Click any bar or data point that supports drill-down. Does it drill correctly?
- [ ] Reset all filters. Do all visuals return to their unfiltered state?

### Accuracy Check
- [ ] Pick your most important KPI card. Verify the value using Python or SQL against raw data.
- [ ] Pick your top insight chart. Manually calculate the figure for one segment and confirm it matches.
- [ ] Check that no chart shows a value for a time period outside your dataset's date range.

### Visual/Professional Check
- [ ] Every chart has a clear, descriptive title.
- [ ] Every axis has a label with units (%, Rs., Minutes, etc.).
- [ ] Data labels are present and use correct number formatting.
- [ ] One consistent color theme is applied across all pages.
- [ ] No visual overlaps another. Test the PDF export.
- [ ] Team name and project title are visible on the dashboard.

---

## Part 2: Peer Review Exchange

**Instructions:**
1. Exchange your dashboard file (or share your screen) with a neighboring team.
2. The reviewing team spends 10 minutes trying to find issues.
3. Both teams complete the Peer Review Form below.
4. Return written feedback to the original team.

### Peer Review Form

**Team Being Reviewed:** ___________________________
**Reviewing Team:** ___________________________
**Date:** ___________________________

**Section A — First Impressions (30 seconds)**

1. Without reading any instructions, what do you think this dashboard is about?

   _________________________________________________________________________

2. What is the most important number or metric on this page?

   _________________________________________________________________________

**Section B — Accuracy Probe**

3. Pick one KPI card. What is the value displayed? Does the label clearly explain what it measures?

   KPI Chosen: _________________________ Value: _____________ Label Clear? Yes / No

4. Apply one filter. List two visuals that updated and one that may not have:

   Updated: _________________________, _________________________
   Possibly ignored filter: _________________________

**Section C — Insight Review**

5. List the top insight you can identify from looking at the dashboard:

   _________________________________________________________________________

6. Ask the team: "So what does this mean for the business?" Rate the clarity of their answer:

   [ ] Very Clear   [ ] Somewhat Clear   [ ] Needs More Work

**Section D — Improvement Suggestions**

7. The single most confusing element on this dashboard is:

   _________________________________________________________________________

8. The single strongest element on this dashboard is:

   _________________________________________________________________________

9. One quick fix that would significantly improve this dashboard:

   _________________________________________________________________________

---

## Part 3: Insight Stress Test

For each of your team's top 3 insights, complete the table below. All cells must be filled before the presentation.

| # | Insight (What?) | Business Impact (So What?) | Recommended Action (Now What?) | Validated? |
|---|----------------|---------------------------|-------------------------------|------------|
| 1 | | | | Yes / No |
| 2 | | | | Yes / No |
| 3 | | | | Yes / No |

> If "Validated?" is "No" for any row — stop, go back to 02_Insight_Validation.md, and run the cross-check process before proceeding.

---

## Part 4: Documentation Verification

- [ ] README.md file exists in the project folder and is complete.
- [ ] Problem Statement is written and reviewed by at least two team members.
- [ ] Dataset description table has all key columns documented.
- [ ] Methodology section (cleaning steps + techniques) is written.
- [ ] Top findings are documented using the What/So What/Now What format.
- [ ] At least 2 limitations are listed.

---

## Part 5: Presentation Dry Run

Before the actual presentation, your team must do one internal rehearsal. Use the timer.

| Presenter | Slides / Section | Time Allotted | Actual Time |
|-----------|----------------|---------------|-------------|
| Member 1 | Hook + Problem Context | 2 min | |
| Member 2 | Data & Methodology Overview | 1 min | |
| Member 3 | Dashboard Walk-Through + Insights | 4 min | |
| Member 4 | Recommendations + Value | 2 min | |
| All | Q&A Buffer | 1 min | |
| **Total** | | **10 min** | |

**Rehearsal debrief questions (answer as a team after the run):**
1. Did anyone go over their allotted time? If yes, what will they cut?
2. Was the "So What?" clearly stated for each insight, or did you just describe the chart?
3. Did the person demonstrating the dashboard click the slicers confidently, or was there confusion?
4. Is there a clear, single recommendation the jury will remember?

---

## Part 6: Final Submission Package

Before handing off your project, verify the following file structure:

```
TeamName_Capstone_Day5/
├── README.md
├── dashboard/
│   └── TeamName_Dashboard.pbix  (or .twbx)
├── data/
│   ├── raw_data.csv
│   └── cleaned_data.csv
├── scripts/
│   └── data_cleaning.py  (or .ipynb)
└── report/
    └── TeamName_Project_Report.pdf  (optional but recommended)
```

Zip the entire folder: `TeamName_Capstone_Day5.zip` and submit it to the facilitator.

---

## Facilitator Checklist (For Reference)

| Team | Dashboard Submitted | README Present | Insights Validated | Presentation Ready |
|------|--------------------|-----------------|--------------------|-------------------|
| Team 1 | | | | |
| Team 2 | | | | |
| Team 3 | | | | |
| Team 4 | | | | |

---

[Previous](03_Documentation_Preparation.md) | [Home](../../README.md) | [Next](../Session_2_Presentation_Evaluation/01_Group_Presentation_Guide.md)

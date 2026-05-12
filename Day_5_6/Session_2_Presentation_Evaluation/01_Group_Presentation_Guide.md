# Group Presentation Guide

> **Learning Goal:** Structure and deliver a compelling 10-minute data analytics presentation that convinces a non-technical jury to take a business action.

---

## The Core Principle: Data Tells, Story Sells

A jury panel has seen dozens of dashboards. What they remember is the story you wrap around the data. Your job in 10 minutes is not to show every chart you built — it is to take them on a journey from "We had a problem" to "Here is exactly what to do about it."

The framework that achieves this is called the **Minto Pyramid**.

---

## The Minto Pyramid Structure for Data Presentations

The Minto Pyramid (developed by Barbara Minto at McKinsey) puts the most important point first, then supports it with evidence. This is the opposite of how most students write — we are trained to build up to a conclusion. Business communication demands the conclusion upfront.

```
           [RECOMMENDATION]
          /                \
    [Evidence 1]      [Evidence 2]
   /    |    \          /    |   \
[Data] [Data] [Data] [Data] [Data] [Data]
```

**Applied to your presentation:**
1. Lead with the single most important finding or recommendation.
2. Then explain the evidence (charts) that prove it.
3. End with the value it delivers to the business.

---

## The 10-Minute Presentation Structure

| Segment | Time | Who Presents | What It Contains |
|---------|------|-------------|-----------------|
| **1. The Hook** | 0:00 – 1:30 | Member 1 | Open with the business problem in one punchy sentence. Add one shocking data point to establish urgency. Do NOT open with "Good morning, we are Team X and today we will present..." |
| **2. Context & Dataset** | 1:30 – 2:30 | Member 2 | Briefly describe the dataset (rows, columns, time period). State the 2–3 KPIs that your analysis is built around. |
| **3. Dashboard Walk-Through** | 2:30 – 6:30 | Member 3 | Live demo of the dashboard. Show only the 2–3 most important insights. Use the slicers to tell the story interactively. |
| **4. The "So What?" Moment** | 6:30 – 8:00 | Member 1 or 3 | Restate the top finding in plain English. Explain what it means for the business — not what the chart shows, but what a manager should *feel* about it. |
| **5. Recommendation & Value** | 8:00 – 9:30 | Member 4 | State 1–2 specific, actionable recommendations. Quantify the value: "This could save Rs. X per month" or "This could reduce churn by Y%." |
| **6. Q&A Buffer** | 9:30 – 10:00 | All | Invite the jury to ask questions. End with: "We are confident this analysis gives [Company] the clarity to act decisively." |

---

## Opening Lines That Work

**Weak opening (avoid):**
> "Good morning everyone. We are Group 3. Our project is on supply chain optimization. We will now begin our presentation."

**Strong opening (use this approach):**
> "Every single day, a store in Whitefield throws away 40 kg of dairy products worth Rs. 12,000 — not because customers don't want them, but because the ordering system doesn't respond to demand. In the next 10 minutes, we will show you exactly where this waste comes from and what one operational change can fix it."

The strong opening creates urgency, is specific, and makes the audience want to keep listening.

---

## Slide Design Principles

A presentation that runs alongside a live dashboard should be minimal. Let the dashboard carry the visual weight.

| Principle | Rule |
|-----------|------|
| **One idea per slide** | Never put two distinct points on the same slide. Split them. |
| **Minimal text** | Maximum 3 bullet points per slide, maximum 8 words per bullet. Your voice carries the explanation. |
| **Big numbers** | If a number is important, make it the largest thing on the slide (72pt+). |
| **High contrast** | Dark text on light background (or white text on dark). Avoid grey text on grey backgrounds. |
| **No clip art** | Use real screenshots of your dashboard or clean, simple icons. |
| **Consistent template** | Same font, same colors, same footer across every slide. |
| **Avoid bullet dumps** | A slide that is 80% bullet points is a slide that belongs in a document, not a presentation. |

**Recommended slide count for 10 minutes: 6 to 8 slides maximum.**

---

## Speaking Tips

### Before You Start
- Practice at least twice all the way through. Know your time.
- Open the dashboard file before the presentation begins. Never launch a file for the first time in front of the jury.
- Assign a designated "clicker" for slides and a designated "dashboard operator."

### During the Presentation
- Speak to the audience, not to the screen. If you are reading your slide, you have too much text on it.
- Pause for 2 seconds after stating each major finding. Let it land.
- Point to the specific part of the chart you are talking about. Do not wave vaguely at the screen.
- If you use jargon (Churn Rate, Inventory Turnover), define it in one sentence the first time you use it.
- Avoid filler words: "basically", "you know", "actually", "sort of." Replace with a deliberate pause.

### Managing Nerves
- Take one slow breath before you begin.
- Remember: you know this dataset better than anyone in the room. The jury does not have your data — you do.
- If you lose your place, return to the structure: Hook → Evidence → Solution → Value.

---

## How to Handle Q&A

The Q&A is where good teams separate themselves from great ones. Treat every question as an opportunity, not an attack.

**The 4-step Q&A formula:**

1. **Listen fully.** Do not start answering before the jury has finished asking.
2. **Acknowledge.** "That's an important point." / "Great question."
3. **Answer directly.** Start with a direct answer, then add context. Do not dance around the question.
4. **Bridge back.** If the answer is not on the dashboard, bridge to what you do have: "We don't have that data in this dataset, but what we can see is..."

**Common jury questions and how to prepare:**

| Jury Question | Prepared Response Strategy |
|--------------|---------------------------|
| "How did you handle missing values?" | Name the specific column, the percentage missing, and the method (remove / impute / flag). |
| "What would happen if this assumption is wrong?" | Acknowledge the assumption, state its impact on the finding, mention it is listed as a limitation. |
| "Can you drill into Region X specifically?" | Use the slicer live. Practice this click in your rehearsal. |
| "What is the most important recommendation?" | Give one clear sentence. Not three. One. |
| "How confident are you in this number?" | State your validation method (cross-checked with raw SQL query). |

---

## Quick Check Questions

1. Why does the Minto Pyramid put the recommendation first instead of building up to it?
2. Your team has 6 charts in the dashboard. During the 10-minute presentation, how many should you actively walk through? Why?
3. A jury member asks a question your team cannot answer with the available data. Write a 2-sentence response that is honest but does not undermine your credibility.

---

[Previous](../Session_1_Capstone_Development/Lab_Capstone_Final_Review.md) | [Home](../../README.md) | [Next](02_Jury_Evaluation_Rubric.md)

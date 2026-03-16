# HWH — Student Outcome Analysis

> An interactive data analysis lab exploring what predicts success in a culinary workforce training program for individuals experiencing housing instability.

**Live site →** *(deploy to GitHub Pages and paste your URL here)*  
**Streamlit prediction tool →** [hwhelonscore.streamlit.app](https://hwhelonscore.streamlit.app)

---

## About This Project

[Housed, Working, and Healthy (HWH)](https://www.housedworkingandhealthy.org/) is a Denver-area nonprofit that integrates housing support, mental health services, culinary workforce training, and employment coaching to help individuals experiencing homelessness build stable, self-sufficient lives. The program operates a commercial kitchen, accepts roughly 20 students at a time, and admits approximately 7 new students per month as space opens.

This interactive lab was built to support **Elon University Business Analytics students** in exploring HWH's real participant data — learning how to build regression models, interpret statistical results, and critically examine how demographic data intersects with decision-making, equity, and bias.

---

## The Data

HWH tracks three interconnected data streams for each participant:

| Source | Description |
|--------|-------------|
| **Application data** | ~70 self-reported questions completed online before enrollment |
| **Student data** | 120+ variables including AZ Self-Sufficiency Matrix (AZ-SSM) scores, attendance, employment, and graduation outcomes |
| **Daily mood data** | One question answered daily at clock-in; converted to a numeric scale |

The **AZ Self-Sufficiency Matrix** is the backbone of student assessment — a 10-factor tool used by nonprofits nationwide to evaluate readiness across housing, income, employment, mental health, substance abuse, social support, and more. Case managers complete it during the initial phone intake, and again at graduation.

The dataset used in this lab contains **671 participants** across multiple cohorts, with an overall graduation rate of ~14.8% and employment rate of ~13%.

---

## What the Lab Teaches

This tool guides students through two interactive phases:

### Phase 1 — Context & Problem
Students receive a situation brief, learn what linear regression is, and answer two warm-up questions to prime their thinking about prediction and equity before touching any data.

### Phase 2 — Build Your Model
Students **drag and drop** predictor variables into a model builder and observe in real time how R², Adjusted R², sample size, and individual coefficients change. Key variables include:

- Attendance Days *(R² = 0.763 for graduation — the strongest predictor)*
- Mental Health Score at intake
- Housing Stability Score at intake
- Employment Readiness Score
- Job Applications submitted
- Average Mood / Coping check-in scores

Students can save multiple models and compare them, use the prediction slider to see what the model forecasts for an individual, and explore why Adjusted R² sometimes *decreases* when a variable is added.

### Data Explorer
A fully browseable table of the participant dataset — searchable, filterable by outcome, sortable by any column, and grouped into themed column sets (Core Outcomes, Attendance, Job Activity, SSF Scores, Demographics). Students can examine missing data patterns, sort by graduation status, and observe the raw variables their regression models are built on.

---

## Key Findings

| Finding | What It Means |
|---------|---------------|
| **Attendance Days: R² = 0.763** | The single strongest predictor — but likely confounded by housing stability |
| **Housing Stability: p = 0.56** | Non-significant; possibly because the program equalizes this barrier |
| **Education level: p = 0.96** | Prior education does not predict graduation — the program levels this field |
| **Criminal history: non-significant, but high bias risk** | A 4pp graduation gap that doesn't reach significance — but criminal history is a well-documented racial proxy |
| **SNAP recipients graduate at 12.4% vs 3.6%** | A selection artifact, not a causal signal — people in acute crisis at intake lack SNAP enrollment *and* drop out early for the same reasons |
| **Race/ethnicity: p = 0.89** | No significant graduation disparity among enrolled participants — but this says nothing about disparities upstream in outreach and intake |

---

## Pedagogical Goals

This lab was designed to build the following competencies:

1. **Statistical interpretation** — distinguishing R², p-values, and coefficients; understanding what each does and does not mean
2. **Causal reasoning** — recognizing confounding and the limits of observational data
3. **Equity-critical data literacy** — understanding how variables can function as proxies for protected characteristics, creating illegal disparate impact even without intent
4. **Decision-making under uncertainty** — applying statistical findings responsibly to real program contexts
5. **Missing data awareness** — understanding that the dataset only reflects people who made it through every prior screening gate

---

## Key Contextual Notes for Students

- Students attend **Tuesday–Friday**. Graduation requires **44 total attendance days**, including a 4-day preview period and an Iron Chef final evaluation.
- The **preview period** (first ~4–8 days) is a mutual assessment: HWH and the student both evaluate fit. Participants who don't continue after the preview are either not a good match or stop showing up — some after receiving early program gift card incentives ($50 on Day 1, $50 on Day 5).
- **Employment coaches** become available after 27 attendance days and remain in contact for **3 months post-program**, supporting both graduates and non-graduates.
- There is a **~90-day data lag** between events and updates in the database. This affects how "current" any snapshot of the data is.
- Case managers collect SSF scores during a **phone intake interview** — these are clinician assessments, not self-reports. Application questions are self-reported. Research has found that over 70% of the time the clinician-assessed SSF score is higher than what the application answer suggests, raising questions about impression management and assessment consistency.
- The program is currently planning a **location change**, which may affect student capacity and continuity.

---

## Faculty Lead

**[Vinayaka Gude, PhD](https://www.elon.edu/u/directory/profile/vgude/)**  
Assistant Professor, Business Analytics  
Elon University — Martha and Spencer Love School of Business

*In partnership with [Housed Working and Healthy](https://www.housedworkingandhealthy.org/)*

---

## Useful Resources

| Resource | Link |
|----------|------|
| AZ Self-Sufficiency Matrix | [lifeworksaustin.org](https://www.lifeworksaustin.org/outcome-measurement) |
| HWH Organization | [housedworkingandhealthy.org](https://www.housedworkingandhealthy.org/) |
| Streamlit Prediction Tool | [hwhelonscore.streamlit.app](https://hwhelonscore.streamlit.app) |
| Prof. Gude's Faculty Page | [elon.edu](https://www.elon.edu/u/directory/profile/vgude/) |

---

*Data used in this lab has been reviewed for educational use. Individual participants are identified only by numeric ID. Sensitive personal information has been excluded.*

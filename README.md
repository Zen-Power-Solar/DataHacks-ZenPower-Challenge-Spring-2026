# Zen Power Challenge

## Objectives

Build an effective business intelligence dashboard using the Zen Power solar dataset.

---

## Recommended Resources

| Resource | Link / Info |
|---|---|
| Sample Database (Supabase) | Shared via link — open to anyone |
| Data Dictionary | Includes header and first 5 rows |
| Google Sun API | For solar irradiance / geospatial data |

---

## Repository

[github.com/Zen-Power-Solar/DataHacks-ZenPower-Challenge-Spring-2026](https://github.com/Zen-Power-Solar/DataHacks-ZenPower-Challenge-Spring-2026)

---

## Database Connections

**Direct connection:**
```
postgresql://postgres:[YOUR-PASSWORD]@db.yxquddtkawapgpejdglo.supabase.co:5432/postgres
```

**DB Password:** *(to be distributed separately)*

> You likely won't need the poolers below, but they're included just in case.

**Transaction Pooler:**
```
postgresql://postgres.yxquddtkawapgpejdglo:[YOUR-PASSWORD]@aws-1-us-west-2.pooler.supabase.com:6543/postgres
```

**Session Pooler:**
```
postgresql://postgres.yxquddtkawapgpejdglo:[YOUR-PASSWORD]@aws-1-us-west-2.pooler.supabase.com:5432/postgres
```

---

## Judging Rubric

**Total: 36 points** | Bonus: up to +6 points

---

### 1. Data Understanding & Integrity — 0 to 7 pts

Does the team understand the dataset? Is the data cleaned, transformed correctly, and used appropriately?

| Score | Description |
|---|---|
| 0–1 | Data misused or major errors present |
| 2–4 | Basic use; some inconsistencies or missed cleaning |
| 5–6 | Data well-understood, mostly clean and correct |
| 7 | Excellent grasp; clean, well-prepared, and used thoughtfully |

---

### 2. Insights & Conclusions — 0 to 7 pts

How meaningful and actionable are the insights drawn? Do the conclusions follow logically from the data?

| Score | Description |
|---|---|
| 0–1 | No real insights; conclusions absent or incorrect |
| 2–4 | Surface-level observations; limited analytical depth |
| 5–6 | Clear, useful insights supported by the data |
| 7 | Compelling, non-obvious insights with strong reasoning |

---

### 3. Visualizations & Chart Quality — 0 to 6 pts

Are the right chart types chosen? Are they labeled, readable, and free from misleading scales or clutter?

| Score | Description |
|---|---|
| 0–1 | Wrong chart types or charts are misleading |
| 2–3 | Adequate charts but choices aren't always ideal |
| 4–5 | Good variety; charts are clear and appropriate |
| 6 | Excellent; chart types enhance understanding and are well-labeled |

---

### 4. Visual Design & Presentation — 0 to 5 pts

Is the dashboard visually polished and easy to navigate? Does it tell a coherent story from start to finish?

| Score | Description |
|---|---|
| 0–1 | Cluttered, confusing, or no coherent layout |
| 2–3 | Readable but lacks visual hierarchy or flow |
| 4 | Clean, well-organized, easy to follow |
| 5 | Polished and tells a clear, compelling data story |

---

### 5. Technical Execution — 0 to 5 pts

Is the code or tooling well-structured? Are appropriate libraries and frameworks used? Does it actually work reliably?

| Score | Description |
|---|---|
| 0–1 | Broken, heavily buggy, or very poor structure |
| 2–3 | Works but code is messy or tools are misused |
| 4 | Solid implementation; good use of tools/libraries |
| 5 | Clean, well-structured, and makes smart technical choices |

---

### 6. Reproducibility & Documentation — 0 to 4 pts

Can a judge run or understand the project without a verbal walkthrough? Is there a README or explanation of methodology?

| Score | Description |
|---|---|
| 0 | No documentation; project is unclear without explanation |
| 1–2 | Minimal notes; some steps require guesswork |
| 3 | Clear README; methodology is explained |
| 4 | Thorough docs; easy to reproduce and fully self-explanatory |

---

### 7. Interactivity — 0 to 4 pts

Can users filter, drill down, or explore the data? Does interactivity add real value rather than just decoration?

| Score | Description |
|---|---|
| 0 | Static only |
| 1–2 | Basic interactions (tooltips, simple filters) |
| 3 | Meaningful filtering or drill-down that aids exploration |
| 4 | Interactions feel essential; dashboard is genuinely exploratory |

---

### Bonus Points *(not used against teams — recognition only)*

| Bonus | Points |
|---|---|
| Predictive modeling — incorporates forecasting, regression, classification, or other ML techniques meaningfully into the dashboard | +3 pts |
| External data / APIs — enriches analysis with external datasets or live API data beyond what was provided | +3 pts |

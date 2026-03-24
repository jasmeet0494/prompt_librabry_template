# P09 · WoW Sales Forecast Comparison

- **Section**: 02 — Weekly Financial Performance Analysis
- **Workflow step**: Step 3 of 4
- **Current version**: v1.2
- **Status**: Tested and suitable with human review
- **Last updated**: March 2026

---

## 📌 Prompt Text (v1.2 — current)

You are a financial analyst with 7+ years of experience supporting weekly sales forecast review across regional accounts.

Your task is to compare the current week’s sales forecast provided in [CURRENT_FORECAST_DATA] with the previous week’s forecast provided in [PRIOR_WEEK_FORECAST_DATA] for all accounts, identify where the forecast has increased or decreased, and flag the accounts with variance.

Use the following strucutre
1. Reporting overview ( State the reporting week, prior comparison week, region, and scope of accounts covered )
2. WoW Table ( Create a table with one row per account and the following columns: )
    - Account Name
    - Prior Week Forecast
    - Current Week Forecast
    - WoW Forecast Variance
3. Executive summary ( Write a short summary in no more than 150 words explaining the key week-over-week forecast movements and the main accounts needing review )

- Tone: concise, factual and professional
- Do not invent reasons for forecast movement unless they are explicitly provided in the input.
- If the cause of variance is not available, state “Requires investigation”.

Placeholders to fill:

- [CURRENT_FORECAST_DATA] = Current week sales forecast by account
- [PRIOR_WEEK_FORECAST_DATA] = Previous week sales forecast by account

---

## 🏢 Intended Workflow or Task

This prompt supports the weekly forecast review stage of the finance reporting workflow.

- Trigger: Current and prior week forecast files are available
- Actor: Finance analyst or finance business partner
- Timing: Weekly forecast review cycle
- Next step: Output is reviewed and used to identify accounts that need deeper variance investigation or stakeholder follow-up

Workflow chain:
Current and prior forecast data prepared → prompt runs → WoW forecast movements are identified and flagged → finance reviews output → flagged accounts are investigated further or escalated to account teams

---

## ❗Problem Being Solved

Finance teams regularly compare weekly sales forecasts across accounts to identify changes from the prior week. When forecast values increase or decrease, analysts must manually review the affected accounts, quantify the movement, and determine which accounts require deeper investigation.

When this is done manually:

- It Takes an analyst ( **1 Hour** ) each week to navigate the files, create the table and analse.
- Important forecast movements may be missed or inconsistently prioritised
- Teams may focus on low-impact changes instead of material ones
- Repeated weekly review creates unnecessary administrative effort

With AI drafting ( **5 mins** ) and human review ( **15 Mins** )total time drops to (**20 Mins**), which is ( **34 Hours** ) saved each year.

In practice, the business problem is not only comparing numbers, but turning week-over-week forecast movement into a clear, prioritised view of where attention is needed.

The problem being solved is therefore the manual effort, inconsistency, and planning risk involved in reviewing weekly sales forecast changes and flagging material variances.

---

## ⚡Automation Potential

Level: High, with human review required

| Dimension              | Assessment                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Repetitiveness         | High — the same comparison is performed every week                          |
| Data availability      | High — current and prior week forecast data is available in structured form |
| Human judgment needed  | Medium — validation and business interpretation are still required          |
| Integration possibility| Can be linked to spreadsheet-based forecast files, reporting templates, or weekly finance review workflows |
| Estimated time saving  | Around 50–70% reduction in first-pass forecast comparison and variance flagging time |

Human-in-the-loop role:

- Verify that forecast comparisons are calculated correctly
- Confirm which movements are materially important
- Add business context where known
- Investigate the real cause of significant forecast changes
- Approve the final summary before it is shared or escalated

This prompt is useful for first-pass variance identification, but it should not replace finance investigation.

---

## ⚠️ Risks and Limitations

| Risk                                                               | Mitigation                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| AI may miscalculate or misread forecast values due to incomplete data | Finance reviewer validates the table against the source forecast files.                     |
| AI may imply reasons for movement without sufficient evidence       | Prompt requires unsupported causes to be labelled as “Requires investigation”.                |
| Materiality may differ by account size or business importance       | Human reviewer applies business judgment when assessing flagged accounts.                     |
| Forecast changes may stem from timing, data issues, or events not visible in the file | Output includes investigation focus areas rather than unsupported explanations. |
| Teams may over‑rely on the flagged list without checking context    | Final review remains with finance before escalation or decision‑making.                       |

Overall risk rating: Medium — useful for structured first-pass analysis and prioritisation, but not suitable for unsupervised interpretation of forecast causes.

---

## 🔄 Version History

### v1.0 — Initial draft

- **Date**: 20 March 2026
- **Prompt**: “Compare this week’s forecast to last week’s forecast and tell me which accounts changed.”
- **Output**: The response identified changes but did not clearly prioritise material accounts or structure the output for finance review.
- **Observed effect**: The analyst still had to manually build a comparison table and decide which accounts to investigate first.
- **Lesson learned**: The prompt needed a more structured output focused on variance size, direction, and investigation priority.



### v1.1 — Added role, sections, and constraints

- **Date**: 22 March 2026
- **Change made**: Added a structured account-level comparison table, movement direction, materiality flags, and a section for accounts requiring investigation.
- **Output**: The result became easier to scan and more useful for weekly review, but some entries still sounded too certain about the cause of changes.
- **Observed effect**: Improved prioritisation, but stronger controls around unsupported interpretation were still needed.
- **Lesson learned**: Forecast-review prompts need clear separation between observed variance and explanation of cause.

### v1.2 — Added category grouping and executive summary

- **Date**: 23 March 2026
- **Change made**: Added instructions not to invent reasons for forecast movement, to use “Requires investigation” where cause is unknown, and to separate follow-     up areas from factual output.
- **Output**: The analysis became more reliable, more actionable, and better aligned with weekly finance review needs.
- **Observed effect**: Reduced first-pass comparison effort and improved consistency in how forecast movements were flagged for follow-up.
- **Lesson learned**: For forecast workflows, AI is most useful when it highlights material movement and supports prioritisation while leaving root-cause analysis     to human reviewers.

---




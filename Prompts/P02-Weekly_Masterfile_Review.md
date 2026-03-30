# P02 · Weekly Masterfile Review

- **Section**: 01 — Weekly Revenue Reporting
- **Workflow step**: : Step 1 of 2
- **Current version**: v1.2
- **Status**: ✅ Tested and suitable with human review
- **Last updated**: March 2026

---

## 📌 Prompt Text (v1.2 — current)

You are a financial analyst with 7+ years of experience working for a consultancy firm.

Your task is to analyse the latest [MASTERFILE_DATA] and convert it into a structured KPI table for all accounts in the [Region] for the current quarter. The objective is to help finance teams quickly compare account-level performance and identify important variances.

Include the following sections: 
1. Reporting context ( State the Masterfile Date and the [Region] )
2. KPI Table ( Create a table for current quarter with one row per account )
   - Account Name
   - Budget
   - Sales Forecast
   - Budget vs Forecast
3. KPI Table ( Create a table for previous quarters with one row per account )
   - Account Name
   - Budget
   - Revenue
   - Margin
   - Budget Vs Revenue
4. Top performance highlights (After the table, summarise strongest performing accounts, accounts with significant changes in revenue or margin
5. Executive summary (Write a short summary in no more than 120 words for senior management)

- Tone: concise, factual and professional
- Use only the data provided in [MASTERFILE_DATA].
- Do not invent figures, reasons, or explanations not supported by the data.
- If any value is missing, inconsistent, or unclear, mark it as “Needs validation”.

Placeholders to fill:

- [MASTERFILE_DATA] = Weekly financial masterfile containing account-level performance data
- [REGION] = Relevant business region

---

## 🏢 Intended Workflow or Task

This prompt supports the weekly financial review stage of a recurring reporting process based on a masterfile received each week.

- Trigger: Weekly masterfile is received and validated
- Actor: Finance analyst or finance business partner
- Timing: During the weekly reporting cycle
- Next step: Output is reviewed and used for faster account-level analysis, reporting preparation, and management discussion

Workflow chain:
Masterfile received → analyst reviews file → prompt runs → KPI table is generated → finance reviews output → insights are used in reporting packs, quarterly views, or stakeholder updates

---

## ❗Problem Being Solved

Finance teams receive a weekly masterfile containing updated actuals, margins, budgets, and forecasts across multiple regional accounts. Because actual values may change due to accounting adjustments, analysts must repeatedly review updated data, compare key KPIs, and identify important account-level variances.

When this process is done manually:

- Financial Analyst spends **(1 Hour)** creating a clean comparison table across all accounts
- Important movements can be missed in large datasets
- Repeated weekly updates create rework
- Quick account-to-account comparison becomes slower
- Finance teams spend unnecessary effort turning raw data into an analysis-ready format
- With AI **( 52 Hours )** per year eliminated doing repetitive work

In practice, analysts often need the information in a tabular format first so they can scan performance quickly and decide which accounts need deeper investigation. The business problem is therefore the manual effort, inconsistency, and inefficiency involved in converting the weekly masterfile into a decision-ready KPI view.

--- 

## ⚡Automation Potential

| **Dimension**           | **Assessment**                                                                 |
|-------------------------|---------------------------------------------------------------------------------|
| Level                   | High, with human review required                                                |
| Repetitiveness          | High — the same KPI extraction and comparison is performed every week           |
| Data availability       | High — structured financial data is available through the masterfile            |
| Human judgment needed   | Medium — finance review is needed for validation and interpretation             |
| Integration possibility | Can be linked with spreadsheet exports, reporting templates, or workflows       |
| Estimated time saving   | Around 50–70% reduction in first-pass KPI preparation and review time           |

Human-in-the-loop role:

- Verify that the KPI table matches the source data
- Confirm whether major variances are materially important
- Validate unclear or unusual figures
- Add business context where needed
- Approve the final output before circulation

This prompt is suitable for partial automation, especially for preparing a first-pass analysis table, but should not replace finance review.

--- 

## ⚠️ Risks and Limitations

| Risk                                                     | Mitigation                                                                                     |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------|
| AI may place values incorrectly into the KPI table       | Finance reviewer checks the table against source data before use.                              |
| AI may misclassify a variance as favourable or unfavourable | Reviewer validates the variance logic and business meaning.                                  |
| Accounting-related changes in actuals may require human interpretation | Final analysis is reviewed by finance before it is shared.                        |
| Confidential financial data may be exposed if handled improperly | Use approved tools and follow internal data governance requirements.                      |
| AI may highlight visible variances but miss business context | Analyst supplements the output with operational or commercial context where needed.        |

Overall risk rating: Medium — highly useful for structured first-pass KPI preparation, but not suitable for fully unsupervised financial reporting.

---

## 🔄 Version History

### v1.0 — Initial draft

- **Date**: 20 March 2026
- **Prompt**: “Analyse the masterfile and summarise revenue, margin, and variances.”
- **Output**: The response was too broad and mostly repeated metrics without giving analysts a clean view across all accounts.
- **Observed effect**: The analyst still had to manually create a comparison table for faster review.
- **Lesson learned**: The prompt needed to prioritise structured tabular output instead of narrative summary alone.

### v1.1 — Added role, sections, and constraints

- **Date**: 22 March 2026
- **Change made**: Added a KPI table format with one row per account and separate variance columns.
- **Output**: The output became easier to scan and compare across accounts, but some entries still included unsupported interpretation.
- **Observed effect**: Improved usability for weekly finance review, but stronger validation rules were still needed.
- **Lesson learned**: Finance prompts work better when they separate data presentation from commentary.

### v1.2 — Added category grouping and executive summary

- **Date**: 23 March 2026
- **Change made**: Added instructions not to invent explanations, to flag unclear values as “Needs validation”, and to include short summary insights after the        table.
- **Output**: The result became more reliable, easier to review, and better aligned with actual finance workflow needs.
- **Observed effect**: Reduced time spent preparing weekly KPI views and improved consistency across reporting cycles.
- **Lesson learned**: For finance workflows, AI outputs are most useful when they first produce structured tables and then add concise insight.

---


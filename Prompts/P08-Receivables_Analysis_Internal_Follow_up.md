# P01 · Receivables Analysis & Internal Follow Up

- **Section: 05** — Working Capital and Collections Support
- **Workflow step**: Step 1 of 3
- **Current version**: v1.2
- **Status**: Tested and suitable with human review
- **Last updated**: March 2026

---

## 📌 Prompt Text (v1.2 — current)

You are a finance analyst with 7+ years of experience supporting accounts receivable review and collections follow-up.

Your task is to analyse the receivables data provided in [AR_AGEING_REPORT] and identify invoices that have exceeded the [Expected payment window]. You must then organise the overdue items in a way that helps the finance team understand which account, deal, service line, and internal team may be involved, so that follow-up can be initiated.

Use the Below Strucutre

1. Reporting overview ( State the reporting date, region, and scope of accounts covered in the review )
2. Overdue receivables table ( Create a table including the following columns:
    - Account Name
    - Invoice Number
    - Invoice Date
    - Outstanding Amount
    - Ageing Bucket
    - Service Line
    - Responsible Team
3. Executive summary ( Write a short summary in no more than 150 words explaining the overall overdue receivables position and the main areas requiring action )

- Tone: concise, factual and professional
- Use only the information provided in [AR_AGEING_REPORT].
- Do not invent reasons for non-payment if they are not supported by the data.
- If a deal, service line, or responsible team is unclear, state “Needs validation”.
- Keep the language suitable for finance and internal operational stakeholders.

Placeholders to fill:

- [AR_AGEING_REPORT] = Accounts receivable ageing report or overdue invoice file
- [EXPECTED_PAYMENT_WINDOW] = Standard payment range, for example 30–90 days

---

## 🏢 Intended Workflow or Task

This prompt supports the overdue receivables review stage of the collections workflow.

- Trigger: Latest accounts receivable ageing report is available
- Actor: Finance analyst or collections support team
- Timing: Weekly or monthly working capital review cycle
- Next step: Output is reviewed and used to initiate follow-up with the relevant internal teams

Workflow chain:
AR ageing report received → prompt runs → overdue items are identified and structured → finance reviews output → internal teams are contacted for issue resolution and expected payment timelines

---

## ❗Problem Being Solved

Finance teams regularly review accounts receivable to identify invoices that remain unpaid beyond the expected payment window, often within a 30–90 day range after invoice issuance. When invoices become overdue, analysts may need to trace them back to the relevant account, deal, service line, and internal team before they can follow up on the issue.

When this is done manually:

- Analysts spend (**30 minutes**) per week filtering and reviewing overdue invoices
- Important overdue items may not be prioritised consistently
- Links between invoices, deals, and responsible teams may be difficult to trace
- Follow-up can be delayed because issue ownership is unclear
- Overdue collections risk may increase due to missed or slow escalation

With AI (**26 Hours**) saved per year on tracking invoices

In practice, the business problem is not only identifying overdue invoices, but turning ageing data into a clear action-oriented review that supports faster issue resolution.

The problem being solved is therefore the manual effort, inconsistency, and collections risk involved in reviewing overdue receivables and preparing internal follow-up actions.

---

## ⚡Automation Potential

Level: High, with human review required

| Dimension              | Assessment                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Repetitiveness         | High — receivables ageing review is performed regularly                     |
| Data availability      | High — relevant invoice and ageing data is usually available in structured form |
| Human judgment needed  | Medium — validation and business context are still required                 |
| Integration possibility| Can be linked to ERP exports, collections reports, or working capital review workflows |
| Estimated time saving  | Around 50–70% reduction in first-pass overdue invoice review and follow-up preparation time |

Human-in-the-loop role:

- Verify that overdue items are correctly identified
- Confirm deal, service line, and team ownership where needed
- Validate whether the issue is truly overdue or already in progress
- Add business context such as disputes, approvals, or billing corrections
- Approve the final output before initiating escalation

This prompt is useful for first-pass overdue invoice analysis, but it should not replace finance validation.

---

## ⚠️ Risks and Limitations

| Risk                                                               | Mitigation                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| AI may misclassify an invoice as overdue due to incomplete fields  | Finance reviewer checks the output against the source ageing report before action is taken.    |
| AI may assign the wrong deal, service line, or responsible team    | Prompt requires unclear ownership to be marked as “Needs validation”.                          |
| Data may not show the actual reason for payment delay              | Prompt avoids inventing causes and limits output to supported observations and follow‑up suggestions. |
| High‑priority invoices may require context not present in the file | Reviewer supplements the output with account knowledge or internal updates before escalation.  |
| Internal follow‑up may be misdirected without validation           | Final review remains with finance before communication is sent.                                |

Overall risk rating: Medium — useful for structured first-pass analysis and collections support, but not suitable for unsupervised escalation.

---

## 🔄 Version History

### v1.0 — Initial draft

- **Date**: 20 March 2026
- **Prompt**: “Review the receivables file and identify overdue invoices that need follow-up.”
- **Output**: The response was too broad and did not consistently organise overdue items by account, service line, or team ownership.
- **Observed effect**: The analyst still had to manually trace invoice details and restructure the findings before follow-up.
- **Lesson learned**: The prompt needed a more operational structure focused on ownership, prioritisation, and action readiness.

### v1.1 — Added role, sections, and constraints

- **Date**: 22 March 2026
- **Change made**: Added a structured overdue receivables table, priority item section, and issue summary by category.
- **Output**: The analysis became easier to scan and more useful for internal collections review, but some outputs still implied reasons for delay without enough      support.
- **Observed effect**: Improved visibility of overdue items, but stronger controls around unsupported explanations were still needed.
- **Lesson learned**: Receivables prompts need clear boundaries between observed data and assumed causes.

### v1.2 — Added category grouping and executive summary

- **Date**: 23 March 2026
- **Change made**: Added instructions not to invent delay reasons, to mark unclear ownership as “Needs validation”, and to focus on internal follow-up actions         rather than conclusions.
- **Output**: The result became more reliable, more practical for finance teams, and better aligned with the actual collections workflow.
- **Observed effect**: Reduced first-pass review time and improved consistency in how overdue receivables were prepared for internal follow-up.
- **Lesson learned**: For receivables workflows, AI is most useful when it structures overdue items, highlights priorities, and supports action planning while         leaving final validation to human reviewers.

---
  

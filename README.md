# 📚 Prompt Library — Finance Planning and Analysis

- **Assessment 1** | Generative AI for Business
- **Student**: Jasmeet Singh | Business Field: Financial Planning and Analysis
- **Model tested on**: ChatGPT
- **Last updated**: March 2026

---

## What This Library Does

This prompt library supports workflow automation in finance planning and commercial support. It contains 10 documented, tested, and iterated prompts organised by the business function they support.

The prompts focus on recurring finance workflows such as weekly revenue reporting, senior management communication, contract renewal support, client planning, market intelligence, receivables review, and internal follow-up communication.

Each prompt entry follows the same structure:

- The exact prompt text with placeholders
- The workflow task it supports
- The problem it solves
- Its automation potential
- Known risks and limitations
- Version history showing iterative improvement

---

## 📂 Folder Structure

```
prompt-library/
│
├── README.md                                  ← Library index
│
├── Prompts/
│   ├── P01-weekly-cadence-call-summary-and-action-tracker.md
│   ├── P02-weekly-masterfile-kpi-table-and-performance-review.md
│   ├── P03-weekly-senior-management-finance-update-email.md
│   ├── P04-contract-review-for-cola-and-billing-rate-uplift-opportunities.md
│   ├── P05-renewal-negotiation-brief-based-on-contract-review.md
│   ├── P06-client-annual-report-analysis-for-it-strategy-and-inferred-it-spend.md
│   ├── P07-monthly-it-market-trends-summary-for-finance-planning.md
│   ├── P08-overdue-receivables-analysis-and-internal-follow-up-preparation.md
│   ├── P09-weekly-sales-forecast-comparison-and-variance-flagging.md
│   └── P10-internal-issue-follow-up-email-draft.md
│
└── Workflow/
    ├── README.md
    ├── 01-weekly-revenue-reporting-workflow.md
    ├── 02-contract-renewal-and-pricing-support-workflow.md
    ├── 03-client-planning-and-market-intelligence-workflow.md
    ├── 04-receivables-review-and-follow-up-workflow.md
    ├── 05-weekly-cadence-call-documentation-workflow.md
    └── 06-weekly-forecast-movement-review-workflow.md

```

---

## 📊 Library Summary Table


| ID  | Prompt Name                                               | Workflow                                   | Automation Level | Risk Level | Status      |
|-----|-----------------------------------------------------------|---------------------------------------------|------------------|------------|-------------|
| P01 | Weekly cadence call summary and action tracker            | Weekly meeting documentation                | High             | Medium     | ✅ Tested   |
| P02 | Weekly masterfile KPI table and performance review        | Weekly revenue reporting                    | High             | Medium     | ✅ Tested   |
| P03 | Weekly senior management finance update email             | Weekly revenue reporting                    | High             | Medium     | ✅ Tested   |
| P04 | Contract review for COLA and billing-rate uplift opportunities | Contract renewal and pricing support    | Medium to High   | High       | ✅ Tested   |
| P05 | Renewal negotiation brief based on contract review        | Contract renewal and pricing support        | Medium to High   | High       | ✅ Tested   |
| P06 | Client annual report analysis for IT strategy and inferred IT spend | Client planning and market intelligence | Medium to High   | High       | ✅ Tested   |
| P07 | Monthly IT market trends summary for finance planning     | Client planning and market intelligence     | Medium to High   | High       | ✅ Tested   |
| P08 | Overdue receivables analysis and internal follow-up preparation | Receivables review and collections support | High             | Medium     | ✅ Tested   |
| P09 | Weekly sales forecast comparison and variance flagging    | Weekly forecast movement review             | High             | Medium     | ✅ Tested   |
| P10 | Internal issue follow-up email draft                      | Receivables review and collections support  | High             | Medium     | ✅ Tested   |

Automation levels: Very High / High / Medium / Low
Risk levels: High = always needs human review, Medium = reviewer validation required, Low = suitable for lighter oversight

---

## 🔗 Prompt Chaining Map

Some prompts in this library are designed to work in sequence. The chains below show how outputs from one prompt feed the next.

**WEEKLY REVENUE REPORTING CHAIN**

P02 (Weekly masterfile KPI table and performance review)
→ P03 (Weekly senior management finance update email)

**CONTRACT RENEWAL AND PRICING SUPPORT CHAIN**

P04 (Contract review for COLA and billing-rate uplift opportunities)
→ P05 (Renewal negotiation brief based on contract review)

**CLIENT PLANNING AND MARKET INTELLIGENCE CHAIN**

P06 (Client annual report analysis for IT strategy and inferred IT spend)
→ P07 (Monthly IT market trends summary for finance planning)

**RECEIVABLES REVIEW AND FOLLOW-UP CHAIN**

P08 (Overdue receivables analysis and internal follow-up preparation)
→ P10 (Internal issue follow-up email draft)

**STANDALONE WORKFLOWS**

P01 supports weekly cadence call documentation as a standalone workflow.
P09 supports weekly forecast movement review as a standalone workflow.

---

## ⚙️ Prompting Strategies Used

| Strategy                           | Prompts                                   | Why chosen                                                                                           |
|------------------------------------|--------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Role‑based prompting               | P01–P10                                    | Gives each prompt a clear business role such as finance analyst, finance business partner, or commercial analyst |
| Grounding constraint (“use only the information provided”) | P02, P03, P04, P05, P06, P07, P08, P09, P10 | Reduces hallucination risk in finance, contract, and planning workflows                               |
| Structured output format           | P01, P02, P04, P05, P06, P07, P08, P09     | Makes outputs easier to review, compare, and reuse in downstream workflows                            |
| Email/output formatting constraints| P03, P10                                   | Keeps communication concise, professional, and ready for internal use                                 |
| Validation wording for uncertainty | P02, P03, P04, P05, P06, P07, P08, P09, P10 | Ensures unclear points are flagged instead of guessed                                                 |
| Chained prompt design              | P02→P03, P04→P05, P06→P07, P08→P10         | Reflects real business workflows where one output feeds the next step                                 |
| Word limits and executive summaries| P01–P09                                    | Improves readability for leadership and reduces manual editing                                        |

---

## 📝 Iteration Evidence

All prompt versions are saved in this repository. Each prompt includes its own version history showing how the prompt improved across testing cycles.

| Prompt | Versions     | Key improvement                                                                                 |
|--------|--------------|--------------------------------------------------------------------------------------------------|
| P01    | v1.0 → v1.2  | Added structured sections, action‑item table, and executive summary                              |
| P02    | v1.0 → v1.2  | Shifted from general summary to KPI‑table‑first output for faster finance review                 |
| P03    | v1.0 → v1.2  | Revised to use validated KPI outputs instead of re‑analysing raw data                            |
| P04    | v1.0 → v1.2  | Added clause categories, COLA focus, and legal/commercial validation controls                    |
| P05    | v1.0 → v1.2  | Added negotiation brief structure, strength ratings, and validation requirements                 |
| P06    | v1.0 → v1.2  | Added confidence levels and clearer separation between fact and inference                        |
| P07    | v1.0 → v1.2  | Added source references, trend categories, and uncertainty controls                              |
| P08    | v1.0 → v1.2  | Added structured overdue table, ownership fields, and follow‑up action focus                     |
| P09    | v1.0 → v1.2  | Added materiality flags, comparison table, and “Requires investigation” rule                     |
| P10    | v1.0 → v1.2  | Improved tone control, issue structure, and missing‑detail handling                              |

---

## ✅ Business Value of the Library

Overall, this library is designed to reduce repetitive finance work, improve consistency of analysis and communication, and support better decision-making across reporting, planning, renewal, and collections workflows.

The prompts are not intended to replace human judgment. Instead, they support first-pass automation while keeping finance, commercial, and planning teams in control of validation, interpretation, and final approval.

---






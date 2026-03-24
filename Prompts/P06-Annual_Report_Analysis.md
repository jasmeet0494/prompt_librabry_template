# P01 · Annual Report Analysis For IT Strategy

- **Section**: 04 — Client Planning and Budget Support
- **Workflow step**: Step 1 of 3
- **Current version**: v1.2
- **Status**: Tested and suitable with human review
- **Last updated**: March 2026

---

## 📌 Prompt Text (v1.2 — current)

You are a financial analyst with 7+ years supporting client budgeting and financial planning.

Your task is to review the annual report provided in [ANNUAL_REPORT] and identify information that helps the internal team understand the client’s current and planned activities in the IT space.

Follow the below structure: 

1. Client overview ( State the client name, reporting year, industry )
2. IT strategy and priority areas ( Summarise the most relevant statements related to digital transformation, cloud adoption, cybersecurity )
3. Indicators of likely IT spend (Identify any direct or indirect signals that may help estimate likely IT spending )
4. Executive summary ( Write a short summary in no more than 150 words explaining what the annual report suggests about the client’s IT direction and how useful it is for budgeting and account planning )

- Tone : accurate, concise, and business-focused.
- Use only the information in [ANNUAL_REPORT].
- If IT spend is not directly disclosed, clearly label the output as an inference based on reported signals.

Placeholders to fill:

[ANNUAL_REPORT] = Client annual report or annual filing

---

## 🏢 Intended Workflow or Task

This prompt supports the client research stage of internal budgeting and account planning.

- Trigger: Annual report is selected for client planning review
- Actor: Finance analyst, planning analyst, or account support team
- Timing: Before budgeting cycle, client planning discussion, or forecast review
- Next step: Output is reviewed and used to inform internal planning assumptions or account strategy discussions

Workflow chain:
Annual report selected → prompt runs → IT priorities and spend indicators extracted → finance/account team reviews findings → budgeting assumptions or client planning inputs are prepared

## ❗Problem Being Solved

Finance and account planning teams may need to review client annual reports to understand what the client is doing or planning to do in the IT space. This helps with internal budgeting, forecasting, and account planning decisions. However, annual reports are often long, dense, and written for external reporting rather than internal commercial analysis.

When this is done manually:

- A financial analyst spends (**1 hour**) combing through a typical annual report
- IT priorities may be spread across multiple sections
- Direct IT spend figures are often not clearly disclosed
- Analysts must piece together indirect signals to form planning assumptions

With AI (**50 Hours**) saved during financial planning if 50 clients to be analysed

The problem being solved is therefore the manual effort, inconsistency, and planning risk involved in reviewing annual reports for IT strategy and inferred IT spend signals.

---

## ⚡Automation Potential

Level: Medium to high, with mandatory human review

| Dimension              | Assessment                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Repetitiveness         | Medium — annual report review is recurring across clients and planning cycles |
| Data availability      | Medium — relevant information exists in annual reports, but direct IT spend may not be stated |
| Human judgment needed  | High — interpretation and planning assumptions require analyst review       |
| Integration possibility| Can be linked to research workflows, account‑planning templates, or budgeting support processes |
| Estimated time saving  | Around 40–60% reduction in first-pass document review and note preparation time |

Human-in-the-loop role:

- Verify that extracted insights are supported by the annual report
- Assess whether inferred IT spend signals are commercially meaningful
- Distinguish between confirmed disclosures and interpreted indicators
- Combine report findings with client knowledge, market context, or prior account history
- Approve the final planning summary before it is used in internal budgeting or account discussions

This prompt is useful for first-pass document analysis and planning support, but it should not replace analyst judgment.

---

## ⚠️ Risks and Limitations

| Risk                                                               | Mitigation                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| AI may treat indirect signals as confirmed IT spend                | Prompt separates direct references from inferred indicators and requires confidence levels.     |
| AI may miss information spread across different report sections    | Reviewer checks important sections and validates the final summary.                            |
| Annual reports may not disclose enough information for conclusions

Overall risk rating: Medium to high — useful for structured first-pass analysis, but not suitable for fully unsupervised budgeting or investment assumptions.

---

## 🔄 Version History

### v1.0 — Initial draft

- **Date**: 20 March 2026
- **Prompt**: “Review the annual report and identify the client’s IT plans and IT spend.”
- **Output**: The response was too broad and often treated weak signals as firm conclusions. It also did not clearly separate direct disclosures from assumptions.
- **Observed effect**: The analyst still had to manually verify most findings and rewrite the summary.
- **Lesson learned**: The prompt needed stronger structure, evidence handling, and clearer caution around inferred spend.

### v1.1 — Added role, sections, and constraints

- **Date**: 22 March 2026
- **Change made**: Added sections for IT strategy, reported initiatives, spend indicators, and validation items.
- **Output**: The analysis became more relevant and easier to use, but some outputs still sounded too certain when the report only gave indirect evidence.
- **Observed effect**: Improved usefulness for planning, but stronger controls around confidence and inference were still needed.
- **Lesson learned**: Annual-report prompts need explicit distinction between disclosed facts and planning inferences.

### v1.2 — Added category grouping and executive summary

- **Date**: 23 March 2026
- **Change made**: Added confidence levels for spend indicators, required direct versus indirect classification, and instructed the model not to present inferred      spend as a confirmed amount.
- **Output**: The analysis became more reliable, more transparent, and better aligned with actual finance planning use.
- **Observed effect**: Reduced first-pass review time and improved consistency in how annual reports were translated into budgeting insights.
- **Lesson learned**: For planning workflows, AI is most useful when it organises evidence, highlights likely spend signals, and makes uncertainty explicit rather     than overstating conclusions.

---












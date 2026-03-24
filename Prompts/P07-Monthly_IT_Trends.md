# P07 · Monthly IT Trends Summary For Financial Planning

- **Section: 04** — Client Planning and Budget Support
- **Workflow step**: Step 2 of 3
- **Current version**: v1.2
- **Status**: Tested and suitable with human review
- **Last updated**: March 2026

---

## 📌 Prompt Text (v1.2 — current)

You are a finance and market planning analyst with 7+ years of experience supporting internal budgeting and account planning.

Your task is to review the reports provided in [MARKET_REPORTS] and prepare a structured internal summary of the latest IT market trends. The purpose is to help the internal team understand where spending is likely to be directed in the market and which trends may affect client budgeting, demand, or investment priorities.

Keep the following strucutre: 

1. Reporting overview ( State the month, source reports reviewed, and the purpose of the summary )
2. Top IT market trends ( Identify trends such as cloud, cybersecurity, AI and automation, digital transformation )
3. For each trend, provide ( Trend title, Plain-English explanation, Which reports mention it, Why it matters for finance planning )
4. Implications for client budgeting and planning (Summarise how these market trends may influence client budgets, account planning, or internal financial      assumptions)
5. Executive summary ( Write a short summary in no more than 150 words explaining the main market trends and what they suggest about likely IT spend direction )

- Tone: concise, factual and professionalUse only the information provided in [MARKET_REPORTS].
- Do not invent market predictions, spending figures, or trend strength that is not supported by the reports.
- If different reports conflict, clearly state that the evidence is mixed.
- Keep the language suitable for finance, planning, and commercial stakeholders.

Placeholders to fill:

- [MARKET_REPORTS] = Monthly external reports from sources such as Gartner, Everest, Draup, Insider Intelligence, or similar

---

## 🏢 Intended Workflow or Task

This prompt supports the monthly market-intelligence review stage of internal finance planning.

- Trigger: Monthly external market reports are collected
- Actor: Finance analyst, planning analyst, or market research support team
- Timing: Monthly planning cycle
- Next step: Output is reviewed and used to inform account planning, budgeting assumptions, or internal trend discussions

Workflow chain:
Market reports gathered → prompt runs → trends are extracted and synthesised → finance/planning team reviews output → summary is used in budgeting or account planning discussions

---

## ❗Problem Being Solved

Finance and planning teams may receive several external market reports each month from sources such as Gartner, Everest, Draup, and Insider Intelligence. These reports are used to understand the latest IT market trends and where spending is likely to be directed, which supports internal budgeting and account planning.

When this is done manually:

- Analysts spend (**5 Hours**) per month reading multiple lengthy reports and creating a summary
- Overlapping findings must be compared and consolidated
- Different source styles make synthesis slower

With AI (**60 Hours**) saved per year on reading reports and drafting summaries.

In practice, the business problem is not just reading reports, but converting multiple external sources into a clear planning document that highlights likely spend direction and relevant market signals.

The problem being solved is therefore the manual effort, inconsistency, and planning risk involved in synthesising monthly IT market reports into a usable internal trend summary.

---

## ⚡Automation Potential

Level: Medium to high, with mandatory human review

| Dimension              | Assessment                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Repetitiveness         | High — similar report synthesis is performed each month                     |
| Data availability      | High — the required content is available in external market reports         |
| Human judgment needed  | High — prioritisation and planning interpretation still require analyst review |
| Integration possibility| Can be linked to research workflows, planning templates, or monthly reporting packs |
| Estimated time saving  | Around 50–70% reduction in first-pass trend review and summary preparation time |

Human-in-the-loop role:

- Verify that the summary reflects the source reports accurately
- Confirm that the most relevant trends were prioritised correctly
- Assess whether reported trends are truly relevant for the client or planning context
- Add sector, account, or market context where needed
- Approve the final summary before it is shared internally

This prompt is useful for first-pass synthesis and summarisation, but it should not replace analyst judgment.

---

## ⚠️ Risks and Limitations

| Risk                                                               | Mitigation                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| AI may over‑generalise trends across different reports             | Reviewer checks whether the summary preserves important differences across sources.            |
| AI may overstate likely spend direction from limited evidence      | Prompt avoids unsupported predictions and requires uncertainty to be flagged.                  |
| Conflicting findings across reports may be oversimplified          | Output includes a dedicated section for mixed signals and uncertainties.                       |
| Some trends may apply only to certain industries or regions        | Human reviewer adds business context before using the output for planning.                     |
| External reports may vary in recency, scope, or emphasis           | Reviewer ensures the final summary reflects source quality and relevance appropriately.        |

Overall risk rating: Medium to high — useful for structured first-pass synthesis, but not suitable for fully unsupervised budgeting or investment assumptions.

---

## 🔄 Version History

### v1.0 — Initial draft

**Date**: 20 March 2026
**Prompt**: “Read the market reports and summarise the latest IT trends and where clients are likely to spend money.”
**Output**: The response was too broad and often merged different trends together without clearly showing which sources supported them.
**Observed effect**: The analyst still had to manually compare reports and restructure the summary for internal use.
**Lesson learned**: The prompt needed clearer source handling, trend categorisation, and stronger planning focus.

### v1.1 — Added role, sections, and constraints

- **Date**: 22 March 2026
- **Change made**: Added sections for top trends, likely spend direction, and implications for budgeting and account planning.
- **Output**: The summary became more useful and easier to review, but some findings still sounded too predictive when the evidence was mixed.
- **Observed effect**: Improved synthesis quality, but stronger controls around certainty were still required.
- **Lesson learned**: Market-intelligence prompts need clearer distinction between observed trends and inferred planning implications.

### v1.2 — Added category grouping and executive summary

- **Date**: 23 March 2026
- **Change made**: Added instructions to show which reports support each trend, to flag mixed evidence, and to avoid presenting inferred spend direction as a          certain outcome.
- **Output**: The summary became more transparent, more reliable, and better aligned with internal finance planning needs.
- **Observed effect**: Reduced first-pass review time and improved consistency in how monthly market reports were turned into planning insights.
- **Lesson learned**: For external-report workflows, AI is most useful when it organises overlapping market signals into a structured internal summary while           making evidence strength and uncertainty explicit.

---

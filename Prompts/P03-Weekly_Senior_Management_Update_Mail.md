# P01 · Weekly Senior Management Update Mail

- **Section: 02** — Weekly Financial Performance Analysis
- **Workflow step**: Step 2 of 4
- **Current version**: v1.2
- **Status**: Tested and suitable with human review
- **Last updated**: March 2026

---

## 📌 Prompt Text (v1.2 — current)

You are a financial analyst with 7+ years of experience

Your task is to draft a concise, professional email for senior management using the information provided in the [KPI Table] and [Top Performance Highlights]
Include the following sections

1. Opening sentence (State that this is the weekly performance update for the [Region] and [Reorting Period])
2. Key headline points (Write concise bullet points covering):
      - Current Forecast
      - Budget vs Forecast
      - [New Bookings] in the Orderbook
      - [Deals Value] in L1 Stage (Final) in the Pipeline
      - [Total Headcount]
3. Performance commentary ( Briefly explain the most important movements, changes, or issues affecting the region based on the KPI table and validated insights. Focus on what senior management would need to know immediately )
4. Closing line ( End with a professional closing sentence offering further detail if required )

Rules:

- Tone: concise, factual and professional
- Length : Maximum 220 words
- Use only the information provided in [KPI_TABLE] and [Top Performance Highlights].
- Do not invent figures, explanations, or business reasons not supported by the input.
- If any KPI is unclear or missing, state “Needs validation”.

Placeholders to fill:

- [KPI_TABLE] = Validated KPI table generated from the weekly masterfile
- [Top Performance Highlights] = Validated highlights and issues identified during finance review
- [REGION] = Relevant business region
- [REPORTING_PERIOD] = Week or date range being reported
- [New Booking] = Total Booking value from the Orderbook
- [Deal Value] = Total Value of deals in the L1 stage in the pipeline
- [Headcount] = Total employees being billed from fulfillment data

---

## 🏢 Intended Workflow or Task

This prompt is step 2 of the weekly communication stage of the finance reporting workflow.

- Trigger: Weekly KPI analysis has been completed and reviewed
- Actor: Finance analyst or finance business partner
- Timing: During weekly reporting cycle before leadership review
- Next step: Output is reviewed and then sent to senior management

Workflow chain:
Masterfile received → KPI table created → key insights reviewed by finance → prompt runs → finance reviews draft email → update sent to senior management

---

## ❗Problem Being Solved

After the weekly masterfile has been analysed, finance teams still need to manually draft an email to senior management summarising the current forecast position, Budget vs Forecast movement, and selected operational KPIs such as New Bookings, L1 pipeline deals, and Total Headcount.

When this is done manually:

Financial Analyst spends 45 Mins each week drafting the mail and proof reading it
Messaging may vary depending on who prepares the update
Important KPI movements may not be communicated clearly
Executives may receive inconsistent levels of detail across reporting cycles
Analysts spend time converting structured analysis into concise leadership communication
With AI (39 Hours) saved per year doing repetitive work

In practice, the business need is not additional analysis, but the ability to translate validated financial insights into a short, clear update that supports management visibility and decision-making.

The problem being solved is therefore the recurring effort, inconsistency, and communication risk involved in manually preparing weekly performance updates for senior management.

---

## ⚡Automation Potential

Level: High, with human review required

| Dimension              | Assessment                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Repetitiveness         | High — the same type of leadership update is prepared every week            |
| Data availability      | High — the required KPIs and insights are already available from the previous analysis step |
| Human judgment needed  | Medium — finance review is needed for materiality, nuance, and business context |
| Integration possibility| Can be linked to reporting templates, spreadsheet outputs, or email workflows |
| Estimated time saving  | Around 60–75% reduction in first-draft email preparation time               |

Human-in-the-loop role:

check that all figures and variances are accurate
confirm the tone is appropriate for senior management
validate whether the highlighted issues are materially important
add business context where required
approve the final version before circulation

This prompt is well suited to first-draft automation, but final review should remain with finance.

---

## ⚠️ Risks and Limitations

| Risk                                                                 | Mitigation                                                                                     |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| AI may misinterpret the importance of KPI movements                  | Finance reviewer confirms whether highlighted points are materially relevant.                  |
| AI may imply reasons for forecast movement not supported by inputs   | Prompt restricts output to the KPI table and reviewed insights only.                           |
| Important watchouts may be omitted or under‑emphasised               | Reviewer checks the output against the source analysis before sending.                         |
| Confidential financial information may be mishandled                 | Use only approved tools and follow internal data governance


Overall risk rating: Medium — suitable for partial automation with mandatory human review before distribution.

---

## 🔄 Version History

### v1.0 — Initial draft

- **Date**: 20 March 2026
- **Prompt**: “Write an email to senior management summarising the weekly financial performance for the region.”
- **Output**: The response was too generic and often lacked the specific KPIs that management expected to see.
- **Observed effect**: The analyst still had to manually rewrite the email and insert missing performance points.
- **Lesson learned**: The prompt needed specific KPI requirements and a clearer business communication structure.

### v1.1 — Added role, sections, and constraints

- **Date**: 22 March 2026
- **Change made**: Added required KPIs, defined email sections, and introduced a word limit for executive readability.
- **Output**: The email became more focused and more useful for management updates, but some wording still included unsupported interpretation.
- **Observed effect**: Editing time reduced, but finance review was still needed to remove over-explanation.
- **Lesson learned**: Senior-management prompts need stronger constraints around interpretation and materiality.
  
### v1.2 — Added category grouping and executive summary

- **Date**: 23 March 2026
- **Change made**: Updated the prompt so it uses the validated KPI table and reviewed insights from the previous step rather than re-analysing the masterfile.         Also    reinforced the instruction not to invent explanations.
- **Output**: The email became more workflow-accurate, more reliable, and better aligned with the actual finance reporting process.
- **Observed effect**: Reduced duplication, improved prompt chaining, and made the output more consistent with finance-reviewed analysis.
- **Lesson learned**: Prompt libraries are stronger when each prompt has a distinct role and builds logically on the output of the previous workflow step.

---

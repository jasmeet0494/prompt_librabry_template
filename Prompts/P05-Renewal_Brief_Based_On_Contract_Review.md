# P05 · Renewal Brief based on Contract Review

- **Section**: 02 — Contract and Renewal Support
- **Workflow step**: Step 2 of 3
- **Current version**: v1.2
- **Status**: ✅ Tested and suitable with human review
- **Last updated**: March 2026

---

## 📌 Prompt Text (v1.2 — current)

You are a financial analyst with 7+ years of experience preparing for a client contract renewal discussion.

Your task is to use the [Contract Review Summary] from step 1 in the workflow to create a structured internal negotiation brief that helps the renewal team assess whether there is support for a billing-rate increase.

Include the following sections

1. Client and contract overview ( State the client name, contract period, renewal timing )
2. Strongest billing-rate uplift opportunities ( List the main opportunities that support a pricing increase, based on the contract review findings )
3. Executive summary ( Write a short internal summary in no more than 150 words explaining the overall pricing position and whether the contract review gives a strong basis for a billing-rate uplift discussion )

- Tone: concise, factual and professional
- Use only the information provided in [CONTRACT_REVIEW_SUMMARY].
- Do not invent legal rights, pricing authority, or negotiation leverage not supported by the input.
- If a point is unclear, state “Requires legal/commercial validation”.

Placeholders to fill:

- [CONTRACT_REVIEW_SUMMARY] = Reviewed output from the contract clause extraction step

---

## 🏢 Intended Workflow or Task

This prompt supports the internal renewal preparation stage following contract review.

- Trigger: Contract review findings have been completed and validated
- Actor: Finance analyst, commercial analyst, or account support team
- Timing: Before internal renewal planning meeting
- Next step: Output is reviewed and used to prepare the negotiation approach for the client renewal discussion

Workflow chain:
Contract reviewed → pricing-related clauses extracted → prompt runs → internal negotiation brief created → finance/commercial/legal teams review → renewal strategy is prepared

## ❗Problem Being Solved

After reviewing a large client contract, teams still need to convert the extracted pricing-related clauses into a practical internal brief that can guide renewal discussions.

When this is done manually:

- Financial analyst spend ( **30 Mins** ) translating contract findings into business-ready recommendations
- useful contract insights may not be presented clearly to decision-makers
- internal teams may enter renewal discussions without a consistent understanding of pricing support
- contract risks and weak points may not be highlighted early enough
- renewal preparation becomes slower and less structured

With AI ( **25 Hours** ) per year can be saved if 50 renewals to be briefed

In practice, the business problem is not just identifying relevant clauses, but turning those findings into an internal briefing document that supports commercial action.

The problem being solved is therefore the manual effort, inconsistency, and preparation risk involved in converting contract analysis into a negotiation-ready internal brief.

---

## ⚡Automation Potential

Level: Medium to high, with mandatory human review

| Dimension              | Assessment                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Repetitiveness         | Medium — renewal preparation occurs regularly but varies by client and contract |
| Data availability      | Medium to high — relevant inputs are available from the previous contract review step |
| Human judgment needed  | High — commercial and legal judgment are still required                     |
| Integration possibility| Can be linked to renewal playbooks, account planning workflows, or internal review templates |
| Estimated time saving  | Around 40–60% reduction in first-draft renewal brief preparation time       |

Human-in-the-loop role:

- Confirm that the brief accurately reflects the reviewed contract findings
- Assess whether the proposed pricing opportunities are commercially realistic
- Validate weak or ambiguous clauses with legal or commercial teams
- Add relationship context, account strategy, or client history where needed
- Approve the final brief before it is used in internal planning discussions

This prompt is useful for structuring internal preparation, but it should not replace legal or commercial decision-making.

---

## ⚠️ Risks and Limitations

| Risk                                                               | Mitigation                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| AI may overstate how strongly a clause supports pricing uplift     | Reviewer confirms all recommendations against the reviewed contract summary.                   |
| AI may understate risks or likely client objections                | Internal stakeholders review the brief before using it in planning.                            |
| Important commercial context may not be present in the input       | Team supplements the brief with account history and business context where required.           |
| Confidential contract information may be mishandled                | Use only approved tools and follow internal data governance and contract-handling requirements.|
| Output may be mistaken for legal advice or negotiation strategy    | Prompt states the brief requires legal/commercial validation and is for internal preparation only. |

Overall risk rating: Medium to high — useful for structured first-pass renewal preparation, but not suitable for unsupervised legal or commercial decision-making.

---

## 🔄 Version History

### v1.0 — Initial draft

- **Date**: 20 March 2026
- **Prompt**: “Create a negotiation brief from the contract review findings.”
- **Output**: The response was too generic and did not clearly distinguish strong pricing opportunities from weak or risky points.
- **Observed effect**: The analyst still had to manually restructure the brief before it could be used in an internal renewal discussion.
- **Lesson learned**: The prompt needed a more practical structure focused on renewal objective, pricing support, and negotiation readiness.

### v1.1 — Added role, sections, and constraints

- **Date**: 22 March 2026
- **Change made**: Added sections for renewal objective, strongest pricing opportunities, potential client objections, and items requiring validation.
- **Output**: The brief became more relevant and easier to use, but some statements still sounded too definitive for an internal preparation document.
- **Observed effect**: Improved usability, but stronger review boundaries were still needed.
- **Lesson learned**: Renewal-preparation prompts need clear limits around certainty, especially when based on contract interpretation.


### v1.2 — Added category grouping and executive summary

- **Date**: 23 March 2026
- **Change made**: Added strength ratings for each pricing opportunity, required legal/commercial validation wording, and a more decision-focused executive            summary.
- **Output**: The negotiation brief became more practical, more balanced, and better aligned with how internal renewal planning is typically prepared.
- **Observed effect**: Reduced first-draft preparation time and improved consistency in how contract findings were translated into renewal strategy discussions.
- **Lesson learned**: For renewal workflows, AI is most useful when it organises reviewed contract findings into a structured internal brief while leaving final       strategy decisions to human stakeholders.

---














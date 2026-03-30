# P04 · Reviewing Contracts for BRE

- **Section: 02** — Contract Renewal & Pricing Support
- **Workflow step**: Step 1 of 2
- **Current version**: v1.2
- **Status**: ✅ Tested and suitable with human review
- **Last updated**: March 2026

---

## 📌 Prompt Text (v1.2 — current)

You are a finance analyst with 7+ years of experiencing supporting client contract renewal preparation at a consultancy firm.

Your task is to review the contract provided in [CLIENT_CONTRACT] and identify clauses or terms that may support an increase in billing rates during the renewal process.

Include the following sections
1. Overview ( State the contract name, client, effective period, renewal period if available, and any relevant commercial context clearly mentioned in the document )
2. Relevant pricing-related clauses (Extract and summarise all clauses related to COLA and pricing escalation. For each clause provide the following details )
- Clause reference or section number
- Clause title or topic
- Short plain-English summary
- Why it may be relevant to billing-rate uplift at renewal
3. Executive summary (Write a short summary in no more than 150 words explaining whether the contract appears to support a billing-rate increase at renewal and what should be reviewed next )

- Tone: concise, factual and professional
- Do not invent owners, deadlines, figures, or decisions.
- If wording is unclear, state “Requires legal/commercial review”.
- Keep explanations in plain business language rather than legal jargon.

Placeholders to fill:

- [CLIENT_CONTRACT] = Existing client contract or renewal agreement

---

## 🏢 Intended Workflow or Task

This prompt supports the contract review stage of the renewal preparation process.

- Trigger: Existing client contract is selected for renewal review
- Actor: Finance analyst, commercial analyst, or account support team
- Timing: Before renewal strategy discussion or pricing review meeting
- Next step: Output is reviewed internally and used to support commercial preparation for renewal

Workflow chain:
Contract selected for review → prompt runs → pricing-related clauses are extracted and summarised → finance/commercial team reviews findings → renewal approach is prepared

---

## ❗Problem Being Solved

Before client contracts are renewed, finance or commercial teams may need to review large contract documents to identify terms that could support an increase in billing rates. This often involves searching for clauses such as COLA, pricing escalation provisions, renewal pricing conditions.

When this is done manually:

- Financial Analyst can spend ( **3 Hours** ) studying the contract and preparing a summary
- Important pricing-related clauses may be missed
- Large contracts are difficult to scan efficiently
- Analysts may struggle to translate legal wording into business-relevant insight
- Renewal preparation can become slower and less consistent

With AI ( **150 Hours** ) per year can be saved if 50 renewals to be studied.

In practice, the business problem is not only document review, but the difficulty of quickly identifying commercially useful clauses from long and complex contracts.

The problem being solved is therefore the manual effort, inconsistency, and risk involved in reviewing contract terms for billing-rate uplift opportunities.

---

## ⚡Automation Potential

Level: Medium to high, with mandatory human review

| Dimension              | Assessment                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Repetitiveness         | Medium — contract review is recurring but varies by client and contract     |
| Data availability      | Medium — relevant information exists in contracts but may be inconsistently worded |
| Human judgment needed  | High — legal and commercial interpretation is still required                |
| Integration possibility| Can be linked to contract repositories, document review workflows, or renewal preparation processes |
| Estimated time saving  | Around 40–60% reduction in first-pass contract review effort                |

Human-in-the-loop role:

- Verify that extracted clauses match the original contract text
- Confirm whether identified clauses are commercially relevant
- Escalate ambiguous terms for legal review
- Decide whether the findings genuinely support a renewal pricing increase
- Approve the final summary before it is used in internal discussions

This prompt is useful for first-pass clause extraction and summarisation, but it should not replace legal or commercial review.

---

## ⚠️ Risks and Limitations

| Risk                                                               | Mitigation                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| AI may miss a relevant clause in a large or complex contract       | Reviewer checks extracted sections against the full contract before relying on the output.     |
| AI may misinterpret legal wording or overstate pricing rights      | Prompt avoids unsupported legal conclusions and flags unclear text for review.                 |
| Important context may sit across multiple sections of the contract | Human reviewer validates how extracted clauses interact across the full agreement.             |
| Confidential client information may be sensitive                   | Use only approved tools and follow internal contract-handling and data governance requirements.|
| Output may be treated as legal advice instead of a business summary| Prompt states the output is not legal advice and requires legal/commercial validation.         |

Overall risk rating: Medium to high — useful for structured first-pass review, but not suitable for unsupervised legal or commercial decision-making.

## 🔄 Version History

### v1.0 — Initial draft

- **Date**: 20 March 2026
- **Prompt**:“Review the contract and identify anything that can help increase billing rates.”
- **Output**: The response was too broad and often missed specific pricing-related clauses such as COLA or renewal conditions.
- **Observed effect**: The analyst still had to manually search the contract and refine the findings.
- **Lesson learned**: The prompt needed clearer focus on pricing, renewal, and escalation-related clauses.


### v1.1 — Added role, sections, and constraints

- **Date**: 22 March 2026
- **Change made**: Added specific categories such as COLA, escalation, rate review, and renewal pricing terms, along with required output sections.
- **Output**: The results became more relevant and easier to use, but some summaries still sounded too definitive for a contract review task.
- **Observed effect**: Improved clause extraction, but legal and commercial caution was still needed.
- **Lesson learned**: Contract-review prompts need stronger boundaries around interpretation.

### v1.2 — Added category grouping and executive summary

- **Date**: 23 March 2026
- **Change made**: Added instructions not to invent legal conclusions, to flag unclear wording as “Requires legal/commercial review”, and to keep explanations in      plain business language.
- **Output**: The review became more reliable, more practical for finance teams, and better aligned with renewal preparation workflows.
- **Observed effect**: Reduced first-pass contract review time and improved consistency in identifying pricing-related renewal opportunities.
- **Lesson learned**: For contract analysis workflows, AI is most useful when it extracts and organises relevant clauses while leaving final interpretation to         human reviewers.

---

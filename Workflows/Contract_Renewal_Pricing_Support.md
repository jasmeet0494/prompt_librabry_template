# 📂 02 — Contract Renewal and Pricing Support Workflow

- **Business function**: Finance / Commercial Support / Contract Renewal
- **Trigger**: Existing client contract is selected for renewal review
- **Prompts in this section**: P04, P05

---

## Section Purpose

This section supports the contract renewal workflow by helping finance and commercial teams review existing client contracts and prepare for pricing discussions. The process begins with extracting pricing-related clauses such as COLA, escalation, and renewal terms from large contracts, then converts those findings into a structured internal negotiation brief. These prompts reduce manual contract review effort, improve consistency, and help teams prepare more effectively for billing-rate uplift discussions during renewal.

---

## Chain Diagram

Client contract selected for renewal review<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼<br>
P04 · Contract review for COLA and billing-rate uplift opportunities → Extracts pricing-related clauses, COLA details, and renewal terms relevant to billing-rate increase<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼<br>
P05 · Renewal negotiation brief based on contract review → Converts reviewed contract findings into an internal brief for pricing uplift discussion

## Prompts

| File | Prompt | Status |
|---|---|---|
| [P04-Reviewing_Contracts_For_BRE.md](../Prompts/P04-Reviewing_Contracts_For_BRE.md) | Contract review billing-rate uplift opportunities | ✅ Tested — v1.2 |
| [P05-Renewal_Brief_Based_On_Contract_Review.md](../Prompts/P05-Renewal_Brief_Based_On_Contract_Review.md) | Renewal negotiation brief based on contract review | ✅ Tested — v1.2 |

---

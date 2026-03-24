# 📂 01 — Weekly Revenue Reporting Workflow

- **Business function**: Financial Analysis
- **Trigger**: Weekly masterfile is received and validated
- **Prompts in this section**: P02, P03

---

## Section Purpose

This section supports the weekly revenue reporting workflow by turning masterfile data into structured finance outputs for leadership communication. The process helps finance teams convert weekly account-level data into a KPI table and then use that reviewed analysis to draft a concise senior management update. In a recurring weekly reporting cycle, these prompts reduce manual effort, improve consistency, and support faster visibility of forecast, budget, and performance movements across the region.

---

## Chain Diagram

Weekly masterfile received and validated<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼<br>
P02 · Weekly masterfile review → Converts masterfile data into a structured KPI table for account-level review<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;│<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;▼<br>
P03 · Weekly senior management update email → Uses the validated KPI table and insights to draft a leadership update email

---

## Prompts

| File | Prompt | Status |
|---|---|---|
| [P02-Weekly_Masterfile_Review.md](../Prompts/P02-Weekly_Masterfile_Review.md) | Weekly masterfile KPI table and performance review | ✅ Tested — v1.2 |
| [P03-Weekly_Senior_Management_Update_Mail.md](../Prompts/P03-Weekly_Senior_Management_Update_Mail.md) | Weekly senior management finance update email | ✅ Tested — v1.2 |

---


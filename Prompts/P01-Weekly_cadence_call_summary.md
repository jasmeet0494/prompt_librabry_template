# P01 · Weekly cadence call summary and action tracker

- **Section**: 05 — Weekly Cadence Call Documentation
- **Workflow step**: Step 1 of 3
- **Current version**: v1.2
- **Status**: ✅ Tested and suitable with human review
- **Last updated**: March 2026

---

## 📌 Prompt Text (v1.2 — current)

You are a finance PMO supporting a weekly revenue cadence meeting involving finance, sales, and delivery teams.

Your task is to convert the [MEETING_TRANSCRIPT] or [RAW_NOTES] into a clear, management-ready meeting summary.

Include the following sections: 
1. Meeting Summary (2 -3 sentences what the meeting covered)
2. Key Discussion Points ( Group the discussion under these heading where relevant )
   - Finance Forecast Updates
   - Delivery Forecast Updates
   - Sales Forecast Updates
   - Orderbook Status
   - Status of Deals in Pipeline
3. Action Items (Create a table with Action, Owner, Deadline (If Mentioned), Status Note)

- Tone: concise, factual and professional
- Do not invent owners, deadlines, figures, or decisions.
- If any point is unclear, write “Not clearly stated”.

Placeholders to fill:

- [MEETING_TRANSCRIPT] = Full transcript of weekly cadence call

---

## 🏢 Intended Workflow or Task

This prompt supports the documentation stage of a recurring weekly revenue cadence meeting.

- Trigger: Weekly cadence call concludes
- Actor: Finance PMO
- Timing: Within 1–2 hours after the meeting
- Next step: Output is reviewed, circulated to stakeholders, and used to track actions before the next meeting

Workflow chain:
Cadence call held → transcript/raw notes available → prompt runs → analyst reviews output → summary shared with finance, sales, and delivery teams.

---

## ❗Problem Being Solved

Weekly cadence calls often involve several stakeholders discussing revenue performance, delivery challenges, sales pipeline movement, and required follow-up actions.

When notes are taken manually:

- Key points may be missed
- Action owners may not be captured clearly
- Meeting summaries may vary in quality depending on who writes them
- Follow-up can become inconsistent
- PMO spends spends ( **1 hour** ) each week listening to the calls and roughly (** 20 mins** ) converting rough notes to usable business communication.
- With AI drafting ( **5 mins** ) and PMO review ( **5 mins** ) saves ( **70 Mins** ) each week annualized to ( **60 Hours** ) saved per year.

In practice, one person often needs to listen carefully during the call, take notes live, clean those notes afterward, turn them into a structured summary, and identify action items for multiple teams. This creates a recurring administrative burden in a high-frequency workflow.

---

## ⚡Automation Potential

Level: High, with human review required

| **Dimension**            | **Assessment**                                                   |
|--------------------------|------------------------------------------------------------------|
| Repetitiveness           | High — the same meeting type occurs weekly                       |
| Data availability        | Medium to high — transcript or notes are usually available       |
| Human judgment needed    | Medium — review is needed for nuance and accountability          |
| Integration possibility  | Can be linked to Teams/Zoom transcripts, meeting notes, workflows|
| Estimated time saving    | 70 hours per year                                                |

Human-in-the-loop role:

- check that the summary reflects the discussion accurately
- confirm action owners and deadlines
- remove any sensitive details not suitable for wider circulation
- approve the final version before sending

If a business runs multiple cadence calls each week across regions or accounts, this prompt could standardise meeting outputs and improve action tracking at scale.

---

## ⚠️ Risks and Limitations

| **Risk**                                                | **Mitigation**                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| AI may miss nuance or misinterpret a discussion point   | Human reviewer validates summary against transcript or notes before circulation.                    |
| Incorrect action owner or deadline may be assigned      | Prompt explicitly says not to invent details; reviewer confirms all accountability items.           |
| Sensitive financial information may be included         | Output is reviewed before sharing and confidentiality rules are followed.                           |
| Transcript quality may be poor or incomplete            | Use raw notes as backup and mark unclear items as “Not clearly stated”.                             |
| Over‑summarisation may hide disagreement                | Prompt includes a separate section for follow‑up items and unresolved points.                       |

Overall risk rating: Medium - suitable for partial automation with mandatory human review.

---

## 🔄 Version History

### v1.0 — Initial draft

- **Date**: 20 March 2026
- **Prompt**: “Summarise the meeting notes and write action items.”
- **Output**:Too generic. Important financial issues were sometimes merged into one broad summary. Action items were incomplete and owners were often missing.
- **Observed effect**: Still required major manual rewriting.
- **Lesson learned**: The prompt needed structure, role assignment, and explicit output sections.

### v1.1 — Added role, sections, and constraints

- **Date**: 22 March 2026
- **Change made**: Added role framing (“finance business partner”), required output headings, and instruction not to invent missing details.
- **Output**: Much clearer structure. Action items improved, but some outputs still mixed operational updates with decisions, making them harder to circulate.
- **Observed effect**: Editing time reduced, but reviewer still had to reorganise content.
- **Lesson learned**: The prompt needed stronger categorisation and a separate executive summary.

### v1.2 — Added category grouping and executive summary

- **Date**: 23 March 2026
- **Change made**: Added grouped headings for finance, sales, delivery, revenue risks, decisions made, and unresolved items. Also added a 120-word executive
  summary.
- **Output**: More structured, easier to circulate, and closer to a management-ready format.
- **Observed effect**: Reduced post-meeting editing and improved consistency across outputs.
- **Lesson learned**: Structured sections and explicit exclusions make prompt outputs more reliable for recurring business workflows.

---



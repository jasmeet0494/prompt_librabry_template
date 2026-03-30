# P10 · Receivables Follow Up Draft Email

- **Section**: 04 — Receivables review & Follow Up
- **Workflow step**: Step 2 of 2
- **Current version**: v1.2
- **Status**: Tested and suitable with human review
- **Last updated**: March 2026

---

## 📌 Prompt Text (v1.2 — current)

You are a finance analyst with 7+ years of experience preparing an internal follow-up email regarding unresolved receivables

Your task is to use the issue summary provided in [ISSUE_SUMMARY] to draft a clear, professional internal email to the relevant team requesting clarification, status, and expected resolution timeline.

Follow the below Structure: 
Subject line: ( Follow-up Required: [ISSUE_TYPE] – [ACCOUNT_NAME] – [REPORTING_PERIOD] )

Email body:

1. Opening context ( Briefly state the issue identified, the relevant account, and why the follow-up is required )
2. Issue details ( Summarise the key facts available, such as invoice, overdue amount, current known status, the reason for the issue or delay, current status )
3. Action required ( Clearly state what response or update is needed and by when, if a deadline is available )
4. Closing line ( End with a professional closing sentence )

Tone: factual, neutral, third-person.
Length: maximum 300 words.
If any section cannot be completed from the notes, write "Insufficient data — follow-up required."

Placeholders to fill:

- [ISSUE_SUMMARY] = Structured summary of the issue identified during finance review
- [ISSUE_TYPE] = Overdue invoice / forecast variance / missing update / unresolved action / other relevant issue type
- [ACCOUNT_NAME] = Relevant client or account name
- [REPORTING_PERIOD] = Week, month, or review cycle

---

## 🏢 Intended Workflow or Task

This prompt supports the internal communication stage after a finance issue has been identified and reviewed.

- Trigger: A finance issue has been identified and requires team follow-up
- Actor: Finance analyst, collections analyst, or finance business partner
- Timing: After issue review and before escalation
- Next step: Output is reviewed and then sent to the relevant internal team for clarification or action

Workflow chain:
Issue identified → issue summary prepared → prompt runs → draft email created → finance reviews wording → follow-up sent to responsible team

## ❗Problem Being Solved

After finance identifies overdue invoice the next step is often to contact the relevant internal team for clarification and resolution. These follow-up emails are usually repetitive.

When this is done manually:

- Analysts spends ( **10 Mins** ) writing the email for each invoice issue. If 10 Issues per week then **100 Minutes** sppent writing repetitive emails
- Wording may vary depending on who prepares the message
- Important issue details may be left out
- Unclear requests can delay response and resolution

With AI drafting ( **2 Mins** ) and Human review ( **2 Mins** ) time drops to ( **4 Mins** ), saving ( **60 Mins** ) for 10 issues

In practice, the business problem is not only communication, but the need to turn structured issue summaries into clear internal follow-up requests that improve response quality and accountability.

The problem being solved is therefore the manual effort, inconsistency, and delay risk involved in drafting internal issue follow-up emails.

--

## ⚡Automation Potential

Level: High, with human review required


| Dimension              | Assessment                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Repetitiveness         | High — similar internal follow‑up emails are drafted regularly              |
| Data availability      | High — key issue details are available from prior finance review steps      |
| Human judgment needed  | Medium — tone, context, and escalation sensitivity still require review     |
| Integration possibility| Can be linked to issue trackers, finance review outputs, or email workflows |
| Estimated time saving  | Around 60–80% reduction in first-draft email preparation time               |

Human-in-the-loop role:

- Check that the issue details are accurate
- Confirm the email tone is appropriate for the audience
- Add urgency or business context where needed
- Validate whether a deadline or escalation reference should be included
- Approve the final email before sending

This prompt is useful for drafting first-pass follow-up communication, but final review should remain with finance.

## ⚠️ Risks and Limitations

| Risk                                                               | Mitigation                                                                                     |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| AI may phrase the issue in a way that sounds too vague or too strong | Reviewer adjusts tone and wording before sending.                                             |
| AI may omit an important issue detail from the summary             | Finance reviewer checks the draft against the source issue summary.                           |
| Missing data may lead to unclear or incomplete requests            | Prompt instructs the model to request clarification rather than invent missing details.       |
| The correct owner or team may not be fully confirmed in the input  | Finance validates recipient ownership before sending the email.                               |
| Teams may rely on the draft without applying business judgment     | Final review remains with the analyst before communication is issued.                         |

Overall risk rating: Medium — useful for structured first-draft communication, but not suitable for unsupervised internal escalation.

---

## 🔄 Version History

### v1.0 — Initial draft

- **Date**: 20 March 2026
- **Prompt**: “Write an email to the team asking about this issue.”
- **Output**: The response was too generic and did not clearly include the issue details, required action, or expected response.
- **Observed effect**: The analyst still had to rewrite most of the email before sending it.
- **Lesson learned**: The prompt needed a clearer business structure and stronger action focus.

### v1.1 — Added role, sections, and constraints

- **Date**: 22 March 2026
- **Change made**: Added sections for opening context, issue details, clarification request, and action required.
- **Output**: The draft became more useful and easier to send, but some versions still sounded too blunt or assumed missing details.
- **Observed effect**: Editing time reduced, but stronger tone and validation controls were still needed.
- **Lesson learned**: Internal follow-up prompts need careful tone control and must avoid unsupported assumptions.

### v1.2 — Added category grouping and executive summary

- **Date**: 23 March 2026
- **Change made**: Added instructions to avoid accusatory language, to keep the tone collaborative, and to request clarification where details are missing instead     of inventing them.
- **Output**: The draft became more professional, more consistent, and better aligned with internal finance communication needs.
- **Observed effect**: Reduced time spent drafting repetitive follow-up emails and improved consistency in internal issue communication.
- **Lesson learned**: For internal follow-up workflows, AI is most useful when it converts issue summaries into clear, respectful action requests while leaving        final tone and escalation judgment to human reviewers.

---











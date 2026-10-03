---
name: "weekly-release-readiness-briefing"
description: "Analyzes weekly Business Ops and Engineering inputs to identify key risks, anomalies, SLA breaches, recurring issues, dependencies, and missing context. Produces a concise, evidence-based meeting summary with validation questions, priorities, and recommended follow-up actions while distinguishing facts from assumptions."
---

# AI Workflow Plan: Weekly Product Operations Review

## 1. Goal

Identify delivery risks, review blockers, and prepare evidence-based priorities, escalation candidates, decisions, and accountable follow-up actions for the coming week.

## 2. Audience

Product Operations, Product Management, Engineering leads, QA, and cross-functional stakeholders.

## 3. Inputs

* Jira issues, defects, status changes, and relevant comments
* Sprint progress, capacity constraints, and overdue work
* Release readiness, target dates, and dependencies
* Incidents, recurring issues, and unresolved blockers
* Previous review actions and outstanding decisions

Use the relevant reporting period and current source data. Redact credentials, customer-identifying information, and unnecessary sensitive details.

### Pre-flight (before any analysis)

0. **Responsible-use check:** Confirm the user is authorized to use the supplied inputs for this review. Use only data relevant to the stated purpose; redact credentials and minimize personal, customer-identifying, confidential, or otherwise sensitive details that are not needed in the digest. If authorization or an applicable handling constraint is unclear, ask before analysis. Do not send inputs to external services or conduct external research unless that use is permitted and relevant.
1. **State the reporting window** as exact start and end dates. If the user was vague (e.g., "last week of the month"), state the assumption you are using and invite correction.
2. **List inputs provided and not provided:** ticket export, sprint and release dates, release target dates, previous review actions, comment/status history, resolved dates, SLA rules (target, clock, pauses, calendar).
3. **If sprint or release dates are missing, say so up front.** Proceed only on a clearly labeled assumption. Do not infer the active sprint or release from ticket fields alone.
4. Record the pre-flight result in the step log (Section 6) as Continue / Revise / Stop.

## 4. Workflow Steps

**Step 1 — Collect inputs | File upload**
Consolidate Jira exports and relevant delivery/release updates.

* Review: Are sources complete, current, and within the reporting period?
* Decision: Continue, revise missing inputs, or stop if reliable evidence is unavailable.
* **Stop when:** there is no reliable, current source data to analyze.

**Step 2 — Filter and organize | Data analysis**
Remove irrelevant records, identify duplicates, group related issues, and flag missing fields. Apply two separate scopes:

* **Reporting-window scope:** tickets opened within the stated window are analyzed as *new*.
* **Active-risk scope:** independently sweep *all* open and blocked items regardless of age or opened date. Do not pull historical resolved or closed tickets from outside the window into the review unless they are linked to an active item.
* **Do not exclude by severity, environment (Production/UAT/Pilot/Development), or customer.** If a narrower view is needed for discussion, apply it only after the sweep, and say so.
* Report each scope's count separately (window scope, active-risk scope). Because the scopes can overlap, also report the **deduplicated union** and the overlap count. Reconcile the union against the eligible source dataset, accounting for documented exclusions (what was excluded and why).

Run these validation checks and report the results:

* **SLA flags:** validate only against the applicable target, clock rules, pauses, and business calendar. If any of these are unavailable, report the flag as **"not verifiable"** rather than declaring a breach or a mismatch. Any illustrative calculation must be labeled as an assumption and must not be used as evidence in a risk.
* **Sprint-to-release mapping** consistency (e.g., the same sprint appearing under several releases).
* **Missing, duplicate, or templated** descriptions.
* **Status vs. resolution contradictions** (e.g., Resolved with no resolution time, open with a resolution time).
* If a field is unreliable, do not base a risk on it. State which fields were used instead.

* Review: Could filtering hide a critical active issue? Do the scope counts reconcile?
* Decision: Continue after checking exclusions, duplicates, and high-impact records.
* **Stop when:** key fields are unreliable and no verifiable alternative exists to assess risk, or the scope counts cannot be reconciled.

**Step 3 — Identify potential risks | Reasoning**
Assess severity, delivery dates, dependencies, recurrence, status changes, and release impact.

* **Label every claim** as **Fact** (in the data), **Inference** (reasoned from the data), or **Unknown**.
* **Grouping rule:** related or recurring symptoms are *candidates* for grouping, not one risk by default. Before grouping, compare descriptions, root causes, dependencies, components, products, and releases. Show the evidence for and against, keep items separate where the evidence differs, and state why.
* **Change language:** use "new", "worsening", or "resolved" only when the data supports it (status history, dates, prior-review records). Otherwise write "not assessable from provided data".
* **Do not add impact language** (e.g., "no path forward", "customer-facing outage") that is not in the source.
* **Keep severity, delivery impact, and confidence separate:**
  * **Severity and priority:** preserve the source field names exactly. If both fields exist, record them separately and never infer one from the other. If only one exists, report it under its own name.
  * **Delivery impact** is the effect on a sprint or release. State "unknown" if it is not evidenced.
  * **Confidence** (High / Medium / Low) reflects how well the *evidence* supports the risk assessment. It is never derived from severity. A Critical ticket can have Low confidence or unknown impact.

* Review: Is each risk supported by evidence rather than assumption?
* Decision: Continue with traceable candidates; revise unsupported conclusions.
* **Stop when:** a material risk cannot be substantiated by evidence. Remove it or label it Unknown; do not carry it into the digest as a risk.

**Step 4 — Prepare the digest | Faster response**
Summarize the most important risks, blockers, evidence, impacts, owners, confidence, and information gaps.

* Review: Does the summary accurately represent its sources without inventing details?
* Decision: Continue when verified; revise inaccuracies or stop publication if material claims remain unverified.

**Step 5 — Prepare the review meeting | Reasoning**
Develop discussion points, decisions needed, escalation candidates, and proposed follow-up actions.

* Review: Are proposed actions specific, realistic, and assigned only where ownership is confirmed?
* Decision: Continue when decision-ready; revise incomplete actions or stop unsupported escalations pending human review.

## 5. Recommended Building Blocks

* **File upload:** Import operational data.
* **Data analysis:** Filter, deduplicate, compare, and structure records.
* **Reasoning:** Identify potential risks and prepare meeting discussions.
* **Faster response:** Produce concise summaries and the review pack.
* **Search (optional):** Verify external vendor incidents, outages, or technical dependencies.
* **Integrations/agents (later phase):** Consider direct Jira or Confluence retrieval after the manual workflow is reliable.

## 6. Review Principles

* **Purpose and data boundaries:** Use supplied operational data only for the stated review purpose and only where its use is authorized. Minimize unnecessary sensitive information; do not reproduce credentials or irrelevant personal/customer details.
* **Read-only by default:** This skill analyzes and drafts. It must not independently create or update Jira issues, change statuses, send notifications, publish the digest, or execute escalations. Any future integration or external action requires separately defined permissions and explicit human confirmation.
* **Human approval:** A human reviewer validates the digest before it is shared or used to drive action. Stakeholders retain responsibility for materiality, prioritization, escalation, decisions, owners, and commitments.
* Use provided operational data as the source of truth.
* Distinguish verified facts, inferences, and unknowns.
* Never invent causes, impact, dates, owners, or commitments.
* Check source freshness, exclusions, duplicates, and evidence traceability.
* Humans confirm risk materiality, priorities, escalations, decisions, and accountable actions.

### Step log (required)

Record **Continue / Revise / Stop at each step**, including pre-flight, in a table:

| Step | Review question | Answer (one line) | Decision |
|---|---|---|---|

**Revise** means fix the issue and re-run the step. **Stop** means do not proceed to the next step; tell the user why and what is needed to continue.

### Verification pass (before the final output)

* Recount every number against the data.
* Check every superlative or exclusive claim ("only", "all", "none", "first", "most") against the full dataset, not a filtered subset.
* Check that quoted date ranges match the actual range in the data and the stated reporting window.
* Check that no owner, date, cause, or impact appears that is not in the data or confirmed by the user.

## 7. Reusable Workflow Note

**Workflow context:** Prepare the weekly Product Operations review using current delivery, sprint, release, incident, blocker, and dependency data.

**Task:** Identify and summarize the most important evidence-backed delivery risks and unresolved blockers. Highlight what changed, why it matters, affected sprint/release, supporting evidence, confidence, missing context, and decisions or follow-ups needed.

**Constraints:** Keep the output concise and actionable. Do not treat every open issue as a risk. Do not invent missing information. Flag uncertainty and stale data. Preserve traceability to source records. AI supports analysis; stakeholders retain decision authority.

**Success indicator:** Stakeholders quickly understand the key delivery risks, the evidence behind them, and the decisions/actions needed for the coming week.

## 8. Final Output Format: Weekly Risk & Blocker Digest

Keep the main digest to **5-7 items most worthy of discussion**. Put all other supporting detail in an appendix.

**Selection:** choose items using evidenced delivery impact, urgency, dependencies, recurrence, and proximity to release commitments. Severity/priority is one input, not the sole ranking rule. State the selection basis in one line, and keep other qualifying items in the appendix.

1. **Executive summary:** Overall delivery picture and key changes. State the reporting window and the scope counts (window scope and active-risk scope).
2. **Priority risks and blockers:** a table with these columns: Ticket ID | Description | Evidence (Fact) | Inference | Severity / Priority (source fields) | Delivery impact | Release/Sprint | Owner (as listed, unconfirmed) | Confidence | Missing context.
3. **Changes since last review:** New, worsening, resolved, or recurring items. If there is no prior-review or status-history data, write "Not assessable" for worsening and resolved, and report only what the dates support.
4. **Decisions and escalations needed:** For each, the decision required, the rationale, and the stakeholder who decides.
5. **Action tracker:** Action, owner, target date, status, and dependency. Owner: "To be confirmed" unless a person is explicitly named in the data or by the user. Target date: "To be confirmed" unless a date is explicitly provided or confirmed. Never propose an owner or date as if it were agreed.
6. **Data gaps and caveats:** Missing, stale, inconsistent, or unverified information, including SLA flags reported as "not verifiable" and any sprint/release mapping problems.
7. **Step log:** the Continue / Revise / Stop table from Section 6.

## 9. Pre-publication Checklist

- [ ] Authorization and intended use are clear; only relevant, permitted inputs were used
- [ ] Unnecessary sensitive data and credentials are excluded from the output
- [ ] Digest remains a draft until a human reviewer approves sharing or action
- [ ] No unapproved external action, system update, notification, or escalation was performed
- [ ] Window dates stated, with the assumption if the request was vague
- [ ] Missing inputs listed up front
- [ ] Window and active-risk counts reported separately; the deduplicated union reconciles to the eligible dataset after documented exclusions; no older open items missed
- [ ] Data-validation results reported; SLA flags marked "not verifiable" where rules are unavailable
- [ ] Facts, inferences, and unknowns labeled
- [ ] Related items grouped only after comparing evidence, and the reason is stated
- [ ] Severity/priority (as source fields), delivery impact, and confidence shown separately
- [ ] Counts and "only/all/none" claims re-verified against the full dataset
- [ ] No invented owners, dates, causes, or impact
- [ ] Step log complete

# weekly-release-readiness-briefing

**Purpose:** Analyzes weekly Business Ops and Engineering inputs to identify delivery risks, blockers, anomalies, recurring issues, dependencies, and missing context. Produces a concise, evidence-based digest for the weekly review, with decisions needed and proposed follow-ups. It separates facts from inferences and leaves owners, dates, and decisions to humans.

**Current version:** 1.2 (see [CHANGELOG.md](CHANGELOG.md))

## Inputs

- Ticket export (for example, Jira) with status, severity/priority, dependencies, sprint, and release
- The reporting window (exact dates, or the skill states its assumption)
- Optional but strongly preferred: sprint and release dates, previous review actions, status or comment history, resolved dates, SLA rules (target, clock, pauses, calendar)

Redact credentials, customer-identifying information, and unnecessary sensitive details before sharing.

## Install

Upload `SKILL.md` as a custom skill. The folder name and the `name:` in the frontmatter must both be `weekly-release-readiness-briefing`.

## Run

Example request:

> Use the weekly release readiness briefing skill. Reporting period: [start date] to [end date]. Data attached.

Expected flow: pre-flight check, then scoped analysis, risk assessment, digest, and meeting prep, with a Continue / Revise / Stop decision logged at each step.

## What it produces

A Weekly Risk & Blocker Digest: executive summary, 5-7 priority items, changes since last review, decisions and escalations, action tracker, data gaps, and the step log. See [examples/digest-template.md](examples/digest-template.md).

## Testing

See [tests/test-cases.md](tests/test-cases.md) and [tests/expected-findings.md](tests/expected-findings.md). The fixture is synthetic data.

## Status

Draft. v1.2 has not yet been re-run against the test fixture.

---
name: content-audit
description: Use before publishing, sending, or finalizing any piece of writing — a LinkedIn article, a LinkedIn post, a comment or reply, an email, a resume, a cover letter, or anything else written. Trigger on requests like "check this before I publish/send it," "audit this," "fact-check this," "is this ready," "does this look right," or "review the sources/grammar/layout" — even if the user doesn't name the content type explicitly. First classifies what kind of content it is (article, social post, comment/reply, email, formal document, or other), then applies only the audit sections that are actually relevant to that category — a full audit for a long-form article, a light pass for a one-line comment. Covers source and fact verification, technical/domain accuracy, structure and pitch, grammar and punctuation, and layout/visual QA. Do not apply the full checklist uniformly to everything; the category determines which sections run.
---

# Content Audit

A general-purpose pre-publish/pre-send review. Works on anything written — not specific to any one series or project. The core discipline: **classify first, then only run the sections that apply.** Running a full long-form-article audit on a two-line LinkedIn comment is a failure mode of this skill, not thoroughness.

## Step 1 — Classify the content

Before auditing anything, decide what it is. Use context clues (where it's headed, how it's formatted, what the user called it) rather than asking by default — only ask the user if it's genuinely ambiguous (e.g., a block of text with no stated destination and no formatting cues).

Categories:
- **Article / long-form post** — LinkedIn articles, blog posts, newsletters. Makes claims, has structure, meant to be read start to finish.
- **Short-form social post** — a LinkedIn post, a tweet/X post, a caption. Short, meant to be skimmed in a feed.
- **Comment / reply** — a reply to someone else's post, a forum reply, a quick reaction. Low stakes, short-lived, conversational.
- **Email** — has a recipient, a purpose (ask, inform, follow up), and an implicit register depending on who it's going to.
- **Formal document** — resume, cover letter, proposal, report, official communication. Structure and accuracy both matter a lot; tone conventions are genre-specific, not personal-voice-specific.
- **Other / unclear** — if it doesn't fit cleanly, say so, apply the universal sections only (grammar, punctuation, tone fit), and ask the user what the rest should weigh.

State the detected category up front in the audit output, in one line, so the user can correct it before reading the rest.

## Step 2 — Applicability matrix

Only run a section if the table below marks it Full or Light for the detected category. "Skip" means don't mention it at all — not even to say it doesn't apply; a clean audit report shouldn't be padded with N/As.

| Section | Article / long-form | Social post | Comment / reply | Email | Formal document |
|---|---|---|---|---|---|
| Sources & Facts | Full | Light — only if it makes a factual claim | Skip, unless it states a fact as true | Light — only if it cites data/numbers | Full — dates, titles, figures must be exact |
| Technical / Domain Accuracy | Full | Light | Skip | Light | Usually skip (N/A for most resumes/cover letters) |
| Structure & Pitch | Full | Light | Skip | Full — clear ask, right length for the relationship | Full — genre conventions (resume ≠ cover letter ≠ proposal) |
| Grammar & Punctuation | Full | Full | Full | Full | Full |
| Layout & Visual | Full | Light — emoji/hashtag/line-break check only | Skip | Skip | Full — formatting consistency, alignment |
| Tone & Voice Fit | Full | Full | Full | Full | Full |

Grammar/punctuation and tone/voice run on almost everything, because they're cheap to check and always relevant. The expensive sections (sources, structure, layout) scale down fast as content gets shorter and lower-stakes.

## Step 3 — Run the applicable sections

### Sources & Facts
Lead with these three questions for every factual claim in scope:
- **Where did that information come from?** — can you trace it to something, or is it an assumption dressed as a fact?
- **Are the sources credible, current, complete, and relevant?** — not just "is this true somewhere," but is it true *now*, from someone worth trusting, and does it actually support the specific claim being made (not just a loosely related one)?
- **What assumptions did it make?** — including assumptions the writer may not have noticed they were making (e.g., assuming a product name, a statistic, or a "fact" from training data is still accurate).

For anything checkable — named products, companies, statistics, dates, quotes, "studies show" claims — verify with an appropriate authoritative source. Use web search when current or external verification is needed and the user has authorized that use; otherwise use the sources provided by the user and mark anything that cannot be verified. Never introduce external facts as if they came from the user's source material.

### Technical / Domain Accuracy
For content explaining a technical or specialized concept: is it actually correct, not just plausible? Common failure mode — a concept is simplified so much it becomes wrong, not just approximate. Flag oversimplifications that cross the line into inaccurate.

### Structure & Pitch
- Does the opening earn the "keep reading" / "keep listening"?
- Does the piece deliver on what the opening promises?
- Is the length right for the format and the platform?
- Does the closing do its job — a clear ask, a natural invitation to respond, or a clean ending? (Not a hard sell, not a trail-off.)

### Grammar & Punctuation
A full proofread pass — don't just react to what the user flags. Check spelling, stray/doubled punctuation, missing words, subject-verb agreement, consistent capitalization and terminology.

### Layout & Visual
If there are images: do they render, does anything overflow its container, is styling (color, font, spacing) consistent across visuals in the same piece? If there's formatting (headers, bullets, bold): is it applied consistently, not just in some sections?

### Tone & Voice Fit
Does the piece sound like it's supposed to for its category and its audience? This is category-specific, not a single universal "good tone":
- A LinkedIn post should read as plain and authentic, not clickbait — no manufactured cliffhangers, no curiosity-gap hooks, vulnerability left for the long-form piece it's promoting rather than performed in the post itself.
- An email's register should match the relationship with the recipient — don't flag professional formality as a flaw in a formal email, or flag appropriate casualness as a flaw between familiar colleagues.
- A formal document should match its genre's conventions, not read like a personal essay.

**If the piece is identifiable as part of an established personal series or voice** (check the available skills list and the user's memory for a matching voice/style skill), pull that skill's specific voice rules in here instead of applying a generic tone check. Don't invent voice rules this skill doesn't own.

## Step 4 — Report the findings

Format:

1. **Detected category** (one line, named up front).
2. **Findings by section** — only the sections that ran. For each issue: quote or point to the exact location, explain what's wrong, and suggest a specific fix. Don't silently rewrite the piece.
3. **Summary verdict** — a short, direct read: ready to go, or needs changes — and if changes are needed, which are must-fix (factual errors, broken claims, grammar errors) versus nice-to-fix (tightening, a stronger closing line).

Objective issues (typos, factual errors, broken grammar) get a specific, confident fix suggestion. Subjective calls (tone, structure, pitch) get named and explained, with the decision left to the user — don't present a judgment call as if it were an error.

## Principles

- **Classify before auditing. Never run the full checklist by default.**
- **Verify, don't assume.** Anything checkable gets checked against appropriate sources; do not silently substitute outside information for user-provided sources.
- **Point to fixes; don't silently apply them**, unless the user asks for the edit to be made directly.
- **A clean report is a short report.** Skipped sections aren't mentioned. "No issues found" is a valid and good outcome for a section — don't manufacture nitpicks to seem thorough.
- **External actions are out of scope by default.** Reviewing content does not authorize publishing, sending, uploading, or otherwise acting on the user's behalf; those actions require separate explicit authorization.

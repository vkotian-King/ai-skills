---
name: content-audit
description: Use before publishing, sending, or finalizing any piece of writing — a LinkedIn article, a LinkedIn post, a comment or reply, an email, a resume, a cover letter, or anything else written. Trigger on requests like "check this before I publish/send it," "audit this," "fact-check this," "is this ready," "does this look right," or "review the sources/grammar/layout" — even if the user doesn't name the content type explicitly. First classifies what kind of content it is (article, social post, comment/reply, email, formal document, or other), then applies only the audit sections that are actually relevant to that category — a full audit for a long-form article, a light pass for a one-line comment. Covers source and fact verification, technical/domain accuracy, structure and pitch, grammar and punctuation, and layout/visual QA. Do not apply the full checklist uniformly to everything; the category determines which sections run.
---

# Content Audit

A general-purpose pre-publish/pre-send review. Works on anything written — not specific to any one series or project. The core discipline: **classify first, then only run the sections that apply.** Running a full long-form-article audit on a two-line LinkedIn comment is a failure mode of this skill, not thoroughness.

## Inputs & boundaries

**Inputs:** the draft content; the intended destination/audience, when known; any sources, references, or constraints the user supplies.

**Action boundary:** this skill analyzes and recommends only. It does not publish, send, upload, post, or submit anything. Rewrite only when the user asks for an edit; external actions remain separate and require explicit authorization.

**Source boundary:** use user-provided or otherwise authorized sources for claims about private, internal, or context-specific matters. Use web search for public or current claims when external verification is needed and authorized. Do not blend external findings into the review as if they came from the user's source material. Distinguish supplied evidence from external verification, and mark claims that cannot be verified with the available sources as unverified.

**Keep it minimal:** don't restate or pull in personal, confidential, or customer-identifying details beyond what the review actually needs.

## Step 1 — Classify the content

Before auditing anything, decide what it is. Use context clues (where it's headed, how it's formatted, what the user called it) rather than asking by default. Ask only if the ambiguity materially changes the audit scope or makes a reliable review impossible.

Categories:
- **Article / long-form post** — LinkedIn articles, blog posts, newsletters. Makes claims, has structure, meant to be read start to finish.
- **Short-form social post** — a LinkedIn post, a tweet/X post, a caption. Short, meant to be skimmed in a feed.
- **Comment / reply** — a reply to someone else's post, a forum reply, a quick reaction. Low stakes, short-lived, conversational.
- **Email** — has a recipient, a purpose (ask, inform, follow up), and an implicit register depending on who it's going to.
- **Formal document** — resume, cover letter, proposal, report, official communication. Structure and accuracy both matter; tone conventions are genre-specific.
- **Other / unclear** — if it doesn't fit cleanly, start with grammar, punctuation, and tone fit. Add another section only when the content or user's request gives a concrete reason to do so. Ask what else should be assessed only if that ambiguity materially affects the review.

State the detected category up front in the audit output, in one line, so the user can correct it.

## Step 2 — Select the applicable audit sections

Run only sections marked Full or Light for the detected category. "Skip" means don't mention that section in the audit output. The matrix is a default scope, not a reason to ignore a specific check the user explicitly requests.

| Section | Article / long-form | Social post | Comment / reply | Email | Formal document | Other / unclear |
|---|---|---|---|---|---|---|
| Sources & Facts | Full | Light — if it makes a factual claim | Light — only if it states a material fact as true | Light — if it cites data/numbers or makes a material factual claim | Full — dates, titles, figures must be exact | Light — if a material factual claim is present or requested |
| Technical / Domain Accuracy | Full | Light — if relevant | Skip, unless a material technical claim is made | Light — if relevant | Light — if relevant to the document | Light — if a technical claim is present or requested |
| Structure & Pitch | Full | Light | Skip | Full — clear ask, right length for the relationship | Full — genre conventions | Skip by default; run if requested or clearly necessary |
| Grammar & Punctuation | Full | Full | Full | Full | Full | Full |
| Layout & Visual | Full when rendered content is available | Light — emoji/hashtag/line-break check; visual checks only when available | Skip | Skip unless requested | Full when the artifact or a reliable visual representation is available | Skip unless requested |
| Tone & Voice Fit | Full | Full | Full | Full | Full | Full |

Grammar/punctuation and tone/voice are usually inexpensive and broadly relevant. More involved checks should scale with content length, stakes, evidence needs, and the user's request.

## Step 3 — Run the applicable audit sections

### Sources & Facts

For factual claims in scope, assess:
- **Traceability:** where did the information come from, and does the evidence support the specific claim?
- **Source quality:** is the source credible, current, complete, and relevant?
- **Assumptions:** could a product name, statistic, date, quote, or other assertion be outdated or unsupported?

Choose the source method that fits the claim:
- **Public or current claims:** use web search or another appropriate authoritative source when external verification is needed and authorized.
- **Private, internal, or context-specific claims:** use user-provided or otherwise authorized material. Do not assume public search can verify them.
- **Insufficient evidence:** mark the claim unverified and state what source or context is missing. Do not manufacture certainty.

Keep externally verified information distinct from facts supported by the user's own material.

### Technical / Domain Accuracy

For content explaining a technical or specialized concept, check whether it is correct rather than merely plausible. Flag simplifications that cross the line from approximate to inaccurate. If necessary technical evidence is unavailable, state the limitation.

### Structure & Pitch

- Does the opening earn the "keep reading"?
- Does the piece deliver on what the opening promises?
- Is the length right for the format and platform?
- Does the closing do its job — a clear ask, a natural invitation to respond, or a clean ending?

Apply these checks only when the matrix or the user's request calls for them.

### Grammar & Punctuation

Proofread at a level proportionate to the content. Check spelling, stray or doubled punctuation, missing words, subject-verb agreement, capitalization, and consistent terminology. A short comment should receive a quick pass, not an unnecessarily elaborate report.

### Layout & Visual

Inspect images, rendering, overflow, spacing, alignment, and consistency only when the rendered artifact, screenshot, or other suitable visual representation is available. A text-only draft can support checks of visible text structure and formatting cues, but it cannot establish that the final layout renders correctly. If visual verification is important and the artifact is unavailable, state that limitation rather than implying the check passed.

### Tone & Voice Fit

Judge tone against the content category and audience rather than one universal standard:
- A LinkedIn post should be plain and authentic rather than clickbait.
- An email's register should match the relationship with the recipient.
- A formal document should follow its genre conventions rather than read like a personal essay.

If the piece is identifiable as part of an established personal series or voice, check the available skills list for a matching voice/style skill and use its rules rather than inventing voice rules here. Do not invent a matching skill that does not exist.

## Step 4 — Report the findings

Return a concise report:

1. **Detected category** — one line, named up front.
2. **Findings by section** — include only sections that ran. For each issue, point to the exact location, explain what's wrong, and suggest a specific fix. Do not silently rewrite the piece.
3. **Summary verdict** — state whether it is ready to go or needs changes. Separate **must-fix** issues (factual errors, unsupported claims, broken grammar, material accuracy problems) from **nice-to-fix** items (tightening, stronger closing, style choices). If a material claim could not be verified, say so in the verdict.

Objective defects should receive specific fix suggestions. Subjective calls about tone, structure, and pitch should be explained as judgment calls, with the final choice left to the user.

## Principles

- **Classify before auditing.** Never run the full audit by default.
- **Verify, don't assume.** Checkable claims need appropriate evidence; do not rely on plausibility alone.
- **Preserve source boundaries.** Distinguish user-provided material from external verification.
- **Point to fixes; don't silently apply them**, unless the user asks for the edit.
- **Analysis only.** Do not perform external actions.
- **A clean report is a short report.** Skipped sections are not mentioned. "No issues found" is a valid outcome; do not manufacture nitpicks.

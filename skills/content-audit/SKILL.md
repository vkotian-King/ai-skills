---
name: content-audit
description: Use before publishing, sending, or finalizing any piece of writing — a LinkedIn article, a LinkedIn post, a comment or reply, an email, a resume, a cover letter, or anything else written. Trigger on requests like "check this before I publish/send it," "audit this," "fact-check this," "is this ready," "does this look right," or "review the sources/grammar/layout" — even if the user doesn't name the content type explicitly. First classifies what kind of content it is (article, social post, comment/reply, email, formal document, or other), then applies only the audit sections that are actually relevant to that category — a full audit for a long-form article, a light pass for a one-line comment. Covers source and fact verification, technical/domain accuracy, structure and pitch, grammar and punctuation, and layout/visual QA. Do not apply the full checklist uniformly to everything; the category determines which sections run.
---

# Content Audit

## 1. Goal

Run a proportionate pre-publish/pre-send review of written content. Classify the content first, apply only the relevant audit sections, identify concrete defects and unsupported claims, and give specific fixes without silently rewriting the piece.

## 2. Audience

Anyone preparing written content for publication, sending, submission, or internal/final review.

## 3. Inputs, authorization, data boundaries, and pre-flight

### Inputs

- The draft content.
- The intended destination and audience when known.
- User-provided sources, references, style guidance, or constraints when available.

### Pre-flight checks

1. Confirm the draft and destination/context are sufficient to classify the content. Ask only when ambiguity materially changes the audit scope.
2. Use only information the user is authorized to provide for this review. Minimize personal, customer-identifying, confidential, or otherwise sensitive information that is not needed.
3. External verification is permitted only when current/external checking is needed and its use is authorized. Do not silently replace or supplement user-provided source material with outside facts.
4. If a required source, permission, or material context is missing, mark the gap and decide whether to Continue, Revise, or Stop before proceeding.

**Pre-flight gate**
- **Continue:** scope, data use, and verification permissions are clear enough for the requested audit.
- **Revise:** add the missing destination, source, or constraint when it materially affects the audit.
- **Stop:** authorization for supplied material or required external verification is unclear and the audit cannot proceed responsibly without it.

## 4. Workflow

### Step 1 — Classify the content

Before auditing anything, decide what it is. Use context clues (where it's headed, how it's formatted, what the user called it) rather than asking by default — only ask the user if it's genuinely ambiguous (e.g., a block of text with no stated destination and no formatting cues).

Categories:
- **Article / long-form post** — LinkedIn articles, blog posts, newsletters. Makes claims, has structure, meant to be read start to finish.
- **Short-form social post** — a LinkedIn post, a tweet/X post, a caption. Short, meant to be skimmed in a feed.
- **Comment / reply** — a reply to someone else's post, a forum reply, a quick reaction. Low stakes, short-lived, conversational.
- **Email** — has a recipient, a purpose (ask, inform, follow up), and an implicit register depending on who it's going to.
- **Formal document** — resume, cover letter, proposal, report, official communication. Structure and accuracy both matter a lot; tone conventions are genre-specific, not personal-voice-specific.
- **Other / unclear** — if it doesn't fit cleanly, apply the universal sections only (grammar, punctuation, tone fit), and ask what the rest should weigh.

State the detected category up front in the audit output, in one line, so the user can correct it before reading the rest.

**Review gate:** Is the category supported by the destination, format, and context?
**Decision:** **Continue** when clear; **Revise** when one material detail is missing; **Stop** only when the ambiguity makes a reliable audit impossible.

### Step 2 — Select the applicable audit sections

Only run a section if the matrix below marks it Full or Light. "Skip" means do not mention it in the audit output.

| Section | Article / long-form | Social post | Comment / reply | Email | Formal document |
|---|---|---|---|---|---|
| Sources & Facts | Full | Light — only if it makes a factual claim | Skip, unless it states a fact as true | Light — only if it cites data/numbers | Full — dates, titles, figures must be exact |
| Technical / Domain Accuracy | Full | Light | Skip | Light | Usually skip |
| Structure & Pitch | Full | Light | Skip | Full — clear ask, right length for the relationship | Full — genre conventions |
| Grammar & Punctuation | Full | Full | Full | Full | Full |
| Layout & Visual | Full | Light — emoji/hashtag/line-break check only | Skip | Skip | Full — formatting consistency, alignment |
| Tone & Voice Fit | Full | Full | Full | Full | Full |

**Review gate:** Are only the sections relevant to the detected category selected?
**Decision:** **Continue** when the scope is proportionate; **Revise** when an applicable section is missing or an unnecessary full audit has been selected.

### Step 3 — Run the applicable audit sections

#### Sources & Facts

Lead with these questions for every factual claim in scope:
- **Where did that information come from?** Can you trace it to something, or is it an assumption dressed as a fact?
- **Are the sources credible, current, complete, and relevant?** Does the source actually support the specific claim?
- **What assumptions did it make?** Look for product names, statistics, dates, quotes, "studies show" claims, or other assertions that may have changed or may be unsupported.

For anything checkable, verify with an appropriate authoritative source. Use web search when current or external verification is needed and that use is authorized; otherwise use the sources provided by the user and mark anything that cannot be verified. Never present external information as though it came from the user's source material.

#### Technical / Domain Accuracy

For content explaining a technical or specialized concept, check whether it is actually correct rather than merely plausible. Flag simplifications that cross the line from approximate to inaccurate.

#### Structure & Pitch

- Does the opening earn the "keep reading" / "keep listening"?
- Does the piece deliver on what the opening promises?
- Is the length right for the format and platform?
- Does the closing do its job — a clear ask, a natural invitation to respond, or a clean ending?

#### Grammar & Punctuation

Run a full proofread pass. Check spelling, stray/doubled punctuation, missing words, subject-verb agreement, capitalization, and consistent terminology.

#### Layout & Visual

If there are images, check whether they render and whether anything overflows its container. Check consistency of formatting, headers, bullets, bolding, spacing, color, and typography when those elements are available to inspect.

#### Tone & Voice Fit

Judge tone against the content category and audience rather than one universal standard:
- A LinkedIn post should be plain and authentic rather than clickbait.
- An email's register should match the relationship with the recipient.
- A formal document should follow its genre conventions rather than read like a personal essay.

**Established voice rule:** If the piece is identifiable as part of an established personal series or voice, check the available skills list for a matching voice/style skill and use its rules rather than inventing voice rules here. Do not invent a matching skill that does not exist.

**Review gate:** Is every finding supported by the draft, its authorized sources, or clearly stated reasoning?
**Decision:** **Continue** when findings are traceable; **Revise** when a finding is based on a correctable assumption or missing verification; **Stop** when a material claim cannot be responsibly assessed with the available evidence.

### Step 4 — Report the findings

Use this format:

1. **Detected category** — one line, named up front.
2. **Findings by section** — include only sections that ran. For each issue, quote or point to the exact location, explain what is wrong, and suggest a specific fix. Do not silently rewrite the piece.
3. **Summary verdict** — state whether it is ready to go or needs changes; separate **must-fix** issues (factual errors, unsupported claims, broken grammar, material accuracy problems) from **nice-to-fix** items (tightening, stronger closing, style choices).

Objective issues get a specific, confident fix suggestion. Subjective calls about tone, structure, and pitch must be explained as judgment calls; leave the final choice to the user.

**Review gate:** Does the report accurately represent the audit evidence without inventing certainty?
**Decision:** **Continue** when verified; **Revise** factual or reporting errors; **Stop** the handoff when material claims remain unverified and the user asked for a publication-ready assessment.

## 5. Evidence and quality rules

- **Verify, don't assume.** Checkable claims are verified against appropriate sources when authorized and needed.
- **Preserve source boundaries.** Do not silently import outside facts into a review based only on user-provided material.
- **Separate facts from judgments.** Objective defects should be identified directly; subjective recommendations should be labeled as such.
- **Do not over-audit.** Apply only the sections selected for the detected category.
- **Prefer evidence over plausibility.** If a claim cannot be established, mark it unverified or identify the missing evidence.
- **Point to fixes; don't silently apply them**, unless the user explicitly asks for the edit.
- **Keep the report short enough to be useful.** Skipped sections are not mentioned, and a clean section should be reported as having no issues rather than padded with nitpicks.

## 6. Permitted actions and human approval boundaries

By default this skill may analyze supplied content, evaluate sources, identify issues, and draft suggested fixes. It does not publish, send, upload, post, submit, or otherwise take external action.

Editing the user's content is a separate action: the skill may rewrite only when the user explicitly requests the edit. Publication, sending, submission, or other consequential external action requires separate explicit authorization and remains a human decision.

## 7. Final output format

Return a concise audit report with:

- Detected category
- Only the applicable audit sections
- Specific findings with locations and suggested fixes
- Summary verdict with must-fix versus nice-to-fix separation
- Any material verification limitation or missing source that affects the verdict

## 8. Pre-publication checklist

- [ ] Content category is stated and appropriate
- [ ] Only applicable audit sections were run
- [ ] Source/fact claims were verified against authorized sources where needed
- [ ] External information was not presented as user-provided source material
- [ ] Technical/domain accuracy was checked where applicable
- [ ] Objective defects are separated from subjective recommendations
- [ ] Material uncertainty and missing evidence remain visible
- [ ] No silent rewrite was performed unless explicitly requested
- [ ] No publication, sending, upload, or other external action was performed without separate authorization
- [ ] Final verdict is based on evidence rather than assumed certainty
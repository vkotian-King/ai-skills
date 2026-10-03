# content-audit

**Purpose:** A reusable, proportionate pre-publish/pre-send audit for written content. It classifies the content first, then runs only the sections relevant to its category, covering facts, technical accuracy, structure, grammar, layout, and tone.

**Inputs:** Draft content, intended destination/audience when known, and user-provided sources or constraints. Use public sources for public/current claims and authorized supplied material for private or context-specific claims. Mark claims unverified when suitable evidence is unavailable.

**Action boundaries:** Analysis and recommendations only. Do not silently rewrite content unless the user asks for edits. Do not publish, send, upload, post, or submit anything.

**Install:** Upload `SKILL.md` as a custom skill. The folder name and the `name:` in frontmatter must both be `content-audit`.

**Run:** Example request: “Audit this LinkedIn post before I publish it. Fact-check the claims and flag anything that needs fixing.”

**Runtime note:** `SKILL.md` is the runtime instruction file. This README, the changelog, tests, and examples support onboarding, maintenance, and validation; they are not automatically loaded when the skill triggers.

**Status:** Version 1.3 draft; structural review complete, behavioral tests not yet run.

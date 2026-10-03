# content-audit

**Purpose:** A reusable pre-publish/pre-send audit for written content. It classifies the content first, then runs only the audit sections relevant to the category, covering source/fact verification, technical accuracy, structure, grammar, layout, and tone.

**Inputs:** Draft content, its intended destination/audience when known, and any user-provided sources or constraints. External verification is used only when current/external checking is needed and that use is authorized.

**Action boundaries:** Analysis and recommendations only. Do not silently rewrite content unless the user asks for edits. Do not publish, send, upload, or otherwise take external action without explicit authorization and applicable human review.

**Install:** Upload `SKILL.md` as a custom skill. The folder name and the `name:` in frontmatter must both be `content-audit`.

**Run:** Example request: “Audit this LinkedIn post before I publish it. Fact-check the claims and flag anything that needs fixing.”

**Status:** Draft; repository structure and test coverage added, but behavioral execution results are not yet recorded.

# linkedin-ai-layman-series

**Purpose:** A reusable workflow for writing, sequencing, editing, visualizing, and optionally producing explainer-video assets for the user's recurring "AI Layman Level" LinkedIn series.

**Inputs:** The current article brief or draft, the series roadmap in `/areas/linkedin-content.md`, any user-provided edits or source material, and the requested output format.

**Action boundaries:** Drafting and analysis only by default. The skill does not publish or post content. Secondary outputs such as narration audio or video are attempted only when the current environment provides the required capabilities; they never block article completion.

**Install:** Upload `SKILL.md` as a custom skill. The folder name and the `name:` in frontmatter must both be `linkedin-ai-layman-series`.

**Run:** Example request: “Let’s sequence the concepts for the Align article before we write it.”

**Runtime note:** `SKILL.md` is the runtime instruction file. This README and the changelog support onboarding and maintenance; they are not automatically loaded when the skill triggers.

**Status:** Version 1.0; static review complete; behavioral tests not yet run.

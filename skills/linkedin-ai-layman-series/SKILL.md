---
name: linkedin-ai-layman-series
description: Use whenever the user is writing, continuing, editing, or planning an article in their "AI Layman Level" LinkedIn series (the one that started with "From Autocomplete to Autopilot" and the Predict/Align/Remember/Act/Autopilot framework) — or wants a new weekly/recurring AI-explainer article in that same voice. Covers picking what to write next, sequencing concepts into core/supporting/deferred before drafting prose, writing in the established persona and structure, generating diagrams (recurring and per-concept), an optional capability-aware explainer-video workflow, syncing edits the user makes in their own editor, and drafting plain (non-clickbait) companion LinkedIn posts. Trigger this for requests like "what should the next article be," "let's sequence the concepts for X," "write/draft the Align article," "sync my version of the article," "storyboard this," or "give me post options for this article" — even if the user doesn't name the series explicitly.
---

# LinkedIn AI Layman Series

A recurring, personal-brand LinkedIn series where the user teaches himself AI/LLM concepts in public, one article at a time, for a non-technical professional audience. He is not an engineer or researcher — he's "someone with skin in the game," writing to organize his own understanding as much as to teach readers.

The goal is not maximum output — it's **maximum understanding with minimum unnecessary complexity**. A reader should finish thinking "I finally understand what this means," not "that sounded technical."

The article is always the **primary deliverable**. Diagrams, explainer videos, and narration are optional formats that enhance the article — they never block it, and a missing secondary output is never a failed workflow (see "Capability-aware output handling" below).

## The series so far

- **Article 1 — "From Autocomplete to Autopilot: How a Language Model Actually Becomes an AI Agent."** Introduces Jensen Huang's 5-layer AI industry cake (Energy, Chips, Infrastructure, Models, Applications) as a macro frame, then zooms into Layer 4 (Models) and breaks it into five stages: **Predict → Align → Remember → Act → Autopilot**. This 5-stage framework is the spine of the whole series.
- **Planned next articles** — one deep-dive per stage, in this order: Align (next), then Remember, Act, Autopilot, and a deferred full Predict deep-dive. Keep this roadmap in `/areas/linkedin-content.md` — the series' working roadmap — **not** inside any published article — the user explicitly does not want a "coming up in this series" section visible to readers.
- Check `/areas/linkedin-content.md` at the start of any session touching this series for the latest locked sequence and status, since it gets updated as articles ship. Use it as the roadmap source — don't invent a roadmap if it's silent on something.

## Voice & persona — "AI Layman Level"

This is the single most important thing to get right. Re-read it before drafting anything.

- **"AI Layman Level"** is the user's own named concept: the level between "I use ChatGPT for everything" and "I could write a transformer from scratch." Define or reference it early in every article — it's the series' brand, not a one-off line.
- **Never open with a credentials disclaimer** like "I'm not an engineer, I don't train models, I couldn't derive a loss function." The user explicitly rejected this framing. Instead, frame positively: "I'm writing this while I'm learning it myself." Vulnerability and honesty about not-knowing belong in the article — but as *shared curiosity*, not self-deprecation or apology.
- **First person, short sentences, natural rhythm.** Matches the standing preference in `/topics/writing-style.md` (short, natural, conversational — originally stated for cover letters, applies here too).
- **Teach, don't impress.** Plain language, concrete examples, progressive explanation. Avoid unnecessary jargon, sounding like an AI marketing brochure, overclaiming, or explaining complexity just to demonstrate expertise. The author can simplify concepts, but should not distort them.
- A little self-aware humor about the pace of AI change is welcome (e.g., naming current tools/agents people are racing to keep up with) — **but verify any named product via web search before publishing**; this space moves fast and names/spellings get it wrong easily (e.g., "OpenClaw" not "Openclaws").
- Not clickbait, ever — in the article *or* the companion post. No manufactured cliffhangers, no artificial curiosity gaps, no "As an AI..." framing, no pretending to authority the author doesn't have.
- End articles on an invitation to discuss, not a hard sell or a CTA stack.

## Article structure template

Follow this shape; it's load-bearing, not decorative. **This is the shape of Article 1**, which was a 5-stage overview. A single-stage deep-dive (Align, Remember, Act, Autopilot) adapts it — see the note at the end of this section.

1. **Macro frame.** Open by grounding the piece in a bigger, recognizable public framework (Huang's cake was article 1's). Clarify explicitly that this article zooms into one narrow slice of that bigger picture — don't let readers think the macro frame *is* the article's own framework.
2. **Personal intro.** Name the Layman Level, state the motivation, one light pace-of-change beat, one pointer to a credible deeper resource (e.g., Karpathy's "Intro to Large Language Models" on YouTube) for readers who want to go further than this article will. Close with a short transition line into the content (article 1 used "Alright — let's get into it").
3. **Numbered sections, one per concept/stage**, titled `N. StageName — short plain-language subtitle`. Inside each: a plain explanation, a concrete example or analogy, key terms **bolded** on first use. (See "Turning a locked sequence into prose" below for the per-section drafting rules.)
4. **A process/loop visual** (the journey diagram) with a short paragraph on how real-world use feeds back into the next iteration — keep this honestly hedged (depends on the system/data policy), not overclaimed.
5. **A "stacking it together" recap visual** (the building-blocks pyramid) that explicitly calls back to the macro frame from step 1.
6. **Closing section, "Why this matters at the Layman Level."** Reaffirm the learning-in-public framing, note that each stage is "a whole world in itself" worth its own future piece, invite comments on what to unpack next. Keep it short — this section has been trimmed each round; don't let it regrow into a black-box-vs-hype essay.
7. **Sign-off line** inviting readers to pick the next stage in the comments.

**Adapting this for a single-stage deep-dive** (Align, Remember, Act, Autopilot — any article that's about one stage's internals rather than all five): step 3's sections become one per *sub-concept within that stage* (e.g., Align's locked sequence: hallucination → SFT → RLHF → reward model → reward hacking → evals → guardrails), not one per stage. Steps 4–5 (the journey diagram and the pyramid) are specific to the 5-stage overview and were already used in Article 1 — don't reuse them verbatim in a deep-dive; either skip them, or build one new stage-specific visual if the sub-concepts have their own natural shape (e.g., Align's sequence is itself a pipeline, which could become its own small diagram). The macro frame in step 1 can zoom from "the five stages" down to "this one stage" instead of from Huang's cake — i.e., the deep-dive's own macro frame is Article 1 itself. Link back to it rather than re-explaining the five stages from scratch.

## Turning a locked sequence into prose

Once a sequence is locked (see "Sequencing a new article" below), this is how a list of concepts becomes the actual section text. Extracted from how Article 1's sections were actually written, across several edit rounds.

- **One clear thought per paragraph (or small group of paragraphs) — not literally one concept per paragraph.** A paragraph can hold multiple related ideas when separating them would make the writing unnatural; the test is whether the reader can follow one clear thought easily, not a mechanical 1:1 count.
- **Don't force a bullet list**, unless the concept is itself a pipeline or an ordered sequence of sub-steps (RAG's ingestion → retrieval → augmentation → generation was a legitimate exception; most concepts aren't like this and shouldn't be forced into that shape).
- **Core concepts get full treatment; supporting concepts get a sentence or a passing mention, not equal weight.** Don't flatten the locked sequence's own core-vs-supporting split by writing every concept at the same length.
- **Give the one concept flagged as most personally interesting during sequencing its own narrative beat** — extra space, a "here's the twist" moment, not just a paragraph in a list. In Article 1 this was reward hacking inside Align; it's usually the strongest single "hook" in the piece.
- **One concrete example or analogy per section**, grounding the abstract idea in something tangible. Prefer reusing a consistent running scenario across the article (Article 1 leaned on generic customer-support examples) over a different example every paragraph. A good analogy clarifies and maps reasonably to the real idea without creating a misleading mental model; if it's being stretched past the point it still holds, don't use it — and if an analogy breaks down in a way that matters, say so briefly rather than letting the mental model mislead.
- **Bold each key term on its first use within its own section** — not earlier, not every time it's repeated.
- **Vary the transition/lead-in phrasing.** Informal lead-ins ("Here's the uncomfortable truth," "Here's where it gets interesting") are on-voice, but don't reuse the same opener pattern for more than two sections in one article — this has already been flagged once as overused article-wide.
- **Don't self-censor intensifiers while drafting** ("actually," "genuinely," "really") — they're fine in small doses and natural to the voice. Just run the repeated-word audit (see "Editing & sync workflow") after a full draft exists, rather than trying to avoid them mid-sentence.
- **No mini-recap at the end of each section.** Let it flow straight into the next heading. Recapping happens once, in the closing section — not once per concept.
- **Target length per section:** roughly 150–250 words when an article covers multiple concepts (Article 1's five stages). A single-stage deep-dive can give its core concepts more room than that, since there's no longer four other stages competing for space in the same piece.
- **Simplify without distorting.** When explaining a technical concept, keep the line between simplification and factual error clear, don't imply certainty where the underlying mechanism is genuinely probabilistic, and don't anthropomorphize the model except as a deliberate, flagged analogy. If a caveat's removal would make the explanation misleading, keep the caveat.

### Clarity register — ASD-STE100, applied selectively

ASD-STE100 (Simplified Technical English) is a real aircraft-manual writing standard: short sentences, one idea per sentence, active voice, consistent one-term-per-concept, no idiom. Apply its sentence-level mechanics as a clarity discipline, **not** as a rigid constraint or a compliance score — there's no meaningful "80%" to hit, because the parts being deliberately skipped (the restricted-vocabulary list, the ban on figurative language) are exactly what this voice depends on for its analogies ("it has no hands," "a closed-book exam," "the world's most well-read intern" are doing real explanatory work).

Priority order when these pull in different directions:

**Natural voice → Clarity → Technical accuracy → ASD-STE100 discipline**

Don't force an STE100 rule when doing so makes the writing robotic, unnatural, repetitive, or disconnected from the author's voice.

What to actually take from it, per section:
- **Short sentences. One idea per sentence.** Split compound sentences that are carrying two separate claims.
- **Active voice** over passive, by default.
- **One consistent term per concept**, everywhere in the piece — this is already covered by "bold on first use," but it also means not later switching to a synonym for variety (don't call it "fine-tuning" in one place and "instruction tuning" in another for the same concept).
- **Keep the analogies.** They're the explanatory device, not a violation of clarity.

This is a bias to apply while drafting and to glance back at during editing: if a sentence is doing two jobs, split it; if a concept has drifted to a second name, fix it; don't flatten the analogies trying to "simplify."

## Sequencing a new article — do this before writing any prose

When starting the next article in the series (e.g., "let's do Align"):

1. **List the candidate keywords/concepts, and classify each into one of three buckets:**
   - **Core concepts** — the reader must understand these to follow the article. Full treatment.
   - **Supporting concepts** — help explain a core idea but don't deserve full standalone treatment; a sentence or a passing mention inside the relevant core section, not their own section.
   - **Deferred concepts** — explicitly out of scope for this article, reserved for a future piece or deep-dive. Don't let the article become an encyclopedia trying to cover everything adjacent to the topic.
2. **Recommend the cut** — which supporting concepts earn a mention now vs. which get fully deferred. Don't let one stage article balloon into its own five-part structure.
3. **Get explicit sign-off on the locked sequence (and the three-way classification) before writing prose.** This is a hard checkpoint, not a formality — the user has stopped mid-process for exactly this step before.

### Deciding *which* stage to write next (when asked)

Don't just recite the roadmap order silently — give an actual recommendation with reasoning, weighing:
- Whether the user already flagged that stage as personally fascinating (strongest signal — article 1 flagged reward hacking inside Align).
- Universal relatability (has the audience *felt* this, like hallucination, vs. just being told it happens).
- Narrative continuity with the stage sequence already established.
- A secondary option is worth naming too (with its own reasoning), so the user is choosing, not just approving.

## Visual assets

The series uses two recurring diagram types at the article-1 (5-stage overview) level, plus optional per-concept diagrams inside deep-dive articles. Built via pptxgenjs → PDF → PNG (see `/mnt/skills/public/pptx/SKILL.md` for the base toolchain). Reusable parameterized templates are bundled here:

- `scripts/journey_diagram_template.js` — the N-stage horizontal journey diagram (numbered circles, arrows, loop-back caption band). Used for Article 1's "whole journey" visual, and reusable for any concept sequence inside a deep-dive — it's parameterized by stage count, not fixed at five.
- `scripts/pyramid_diagram_template.js` — the stacked-layer pyramid diagram (bottom = foundation, each layer narrower going up). Used for the "stacking it together" visual.

**Standing color palette** (keep this identical across every article and every diagram so the series looks like one series):
```
Blue:   3E92CC
Coral:  E85D75
Teal:   00A896
Purple: 8367C7
Amber:  FCA311
Navy (bg/accent): 14213D
```
If the user supplies his own cover image for a given article, match its exact labels, captions, and color order in that article's diagrams — the cover sets the vocabulary, the diagrams should echo it, not introduce a second vocabulary for the same five ideas (this happened once with "Base LLM/+Alignment/..." vs "Predict/Align/..." — the user chose to leave the mismatch rather than fix it, but don't introduce a new one by default).

After generating, always visually QA at full resolution before handing off — check for text overflowing card/box boundaries, especially on the longest label in the set (this has broken before: "multi-agent coordination" overflowed its card until the box height was increased).

### Visual communication and publishing QA

Visuals should reduce the reader's effort, not add decoration or repeat the article in another format.

- **Give each visual a distinct job.** A title image introduces the topic; a scenario flow explains a concrete example; an architecture diagram shows system boundaries and relationships; an execution-loop diagram summarizes a recurring process. Multiple visuals can coexist when each adds a different kind of understanding, even when they appear in the same article. Avoid placing similar visuals back-to-back.
- **Prefer visual explanation over text-heavy diagrams.** When a long sequence is hard to scan as prose, consider a flow image. Keep labels concise and action-led. Do not repeat a card's heading in its description; use that space for the action or information that advances the story.
- **Do not force every step into one crowded image.** Choose a layout that makes the sequence easy to follow at article/mobile size. A grid or grouped stages can work, but use the simplest structure that preserves order and relationships. If a diagram becomes crowded, split the explanation across distinct visuals or leave detail in the article.
- **Keep visuals and prose aligned.** Check that prompts, actions, labels, arrows, approval points and outcomes tell the same story as the article. A human-approval step may provide the safeguard without rewriting a user's stated intent; don't assume the application completes a consequential action before the required approval.
- **QA the rendered publishing surface, not only the source asset.** After pasting into LinkedIn, inspect line breaks, lists, tables, image placement, captions, readability on a small screen, and consistency between the final article text and each image. Editors may alter formatting during paste; restore formatting manually where needed.
- **Avoid duplication across formats.** A diagram should clarify a process or relationship that is harder to grasp in prose. Keep the prose when it provides nuance; use the visual to make the structure apparent at a glance. Remove redundant headings or repeated explanations from visual cards.

Output format: `.md` article file with images referenced via relative path (`images/filename.png`), images saved alongside in an `images/` subfolder. Not docx/pptx — this is web-published content.

### When to diagram at all

Create a diagram only when it materially improves understanding — a layered architecture, a process flow, a feedback loop, a before/after contrast, a progressive transformation. Don't create one just because the article is technical, and don't force a concept into a recurring template (journey diagram, pyramid) when it doesn't actually have that shape — an article-specific visual is fine when that fits the concept better. A diagram with one box doesn't earn its space; skip concepts that are just definitions.

Think **concept → structure → visual**, not **article → decorative graphic**. The diagram should explain something that's genuinely harder to grasp in prose.

If a deep-dive's whole locked sequence is itself an ordered pipeline (Align's hallucination → SFT → RLHF → reward model → reward hacking → evals → guardrails plausibly is), it can become one diagram for the article using `journey_diagram_template.js`, rather than one diagram per individual concept.

## Capability-aware output handling

The article is always the primary deliverable. Diagrams, explainer videos, and narration are secondary — **attempted when the current environment/tools support them, and never a dependency for completing the article.**

If a requested secondary output can't be created with what's currently available:
1. Continue with and complete the article.
2. Complete every other output that *is* feasible (e.g., diagram and storyboard, even if narration audio isn't possible).
3. Clearly identify what's unavailable, not silently omit it or claim it was done.
4. State what was completed vs. deferred, and the next practical step for the deferred piece (e.g., "the script and shot list are ready to take into a video-capable tool").

This principle is deliberately tool-agnostic — it describes what the workflow should do regardless of which assistant or tool is running it, so the skill doesn't need rewriting as capabilities change over time. Current environment note: if the current environment cannot access external APIs, securely use the user's API credentials, or render audio/video, defer those outputs and report them using the status table. Reassess available capabilities in future environments rather than treating this limitation as permanent.

### Report output status explicitly

When more than one output was in scope, report status plainly rather than letting it stay implicit:

| Output | Status |
|---|---|
| Article | Completed |
| Diagram | Completed / Not needed / Deferred |
| Video storyboard | Completed / Deferred |
| Narration script | Completed / Deferred |
| Narration audio | Completed / Not available in current environment / Deferred |
| Video | Completed / Not available in current environment / Deferred |
| Companion post | Completed / Deferred |

Only include rows relevant to what was actually requested.

## Explainer video & narration workflow (optional)

An explainer video is an **alternate way to consume the article**, not a replacement for it — useful when the concept involves a process, a transformation, a sequence, or a progressive build-up that benefits from seeing it unfold rather than reading it.

Style reference: when appropriate, the visual approach can draw on characteristics associated with 3Blue1Brown-style educational explainers — concept-first visualization, one idea introduced at a time, synchronized narration and visuals, minimal decoration, relationships shown rather than animated for effect. This means drawing on those *characteristics*, not literally imitating a creator's style or tooling (3Blue1Brown's own pipeline is Manim, hand-authored scene-by-scene — a different production process from anything this skill can execute directly).

Workflow, each step gated by what's actually available:
1. Convert the article's concept sequence into a video narrative.
2. Create a scene-by-scene storyboard (shot list): what each beat shows, in what order.
3. Write the narration script, in the same Layman Level voice as the article, timed to the storyboard.
4. **If an audio-generation capability is available** (e.g., the user's own ElevenLabs key, used in an environment that can call it): generate narration audio.
5. **If video-assembly capability is available**: synchronize visuals and narration into the final video.
6. **If visual/audio inspection is available**: review the result for timing, sync, and whether the visual actually reinforces the narration — readability, clipping, overflow, consistency, same bar as diagram QA above.

**What this skill reliably produces regardless of environment:** the narration script and the storyboard/shot list, as text deliverables. These are the real creative bottleneck independent of tooling, so they're worth producing even when nothing past them is currently possible. Production beyond that — TTS audio, assembled video — happens wherever that capability actually exists: the user's own ElevenLabs key plus a video tool, or a local setup (e.g., Claude Code with Manim or a simpler animation tool installed), using the script and shot list as input. Don't simulate or assume a video was produced when it wasn't — report it per the status table above.

## Editing & sync workflow

The user edits the article himself in his own separate editor/doc tool. Treat the copy in `/mnt/user-data/outputs/` as **possibly stale** at the start of any session — always ask for or read his latest version rather than assuming your last write is current.

When he pastes back an edited version to sync:

- **Rewrite the full file from his pasted text** — his version is the source of truth, not a diff to merge.
- **Point to exact find/replace fixes for genuine typos** (stray punctuation, doubled periods, missing spaces/words, misspellings) rather than silently rewriting prose.
- **Flag, but don't auto-fix, larger inconsistencies** — mismatched terminology (e.g., "AI Layman Level" vs. "Layman Level"), inconsistent section-header styles, a diagram caption that's stronger/weaker than the surrounding prose. Name them, let the user decide.
- **Verify any named real-world product/tool via web search before leaving it in** — spelling and existence both. Don't assume training-data knowledge is current for fast-moving AI product names.
- **Repeated-word audits**: when asked, count content words (excluding stopwords and common verbs) programmatically. Only flag words that are genuinely overused — a topic word like "model" or "agent" repeating a lot is expected and fine. A non-topic filler word (like "actually" showing up 11 times) is the real signal. When asked to replace some instances, vary the substitute words (don't reuse the same synonym every time) and leave some instances alone if the original reads most naturally there.

- **LinkedIn render check:** before treating a pasted article as final, inspect the actual editor rendering. Restore broken paragraph breaks and list formatting; confirm that images appear in the intended sections; check that the visual sequence agrees with the latest text; and verify that no table, caption, or line was accidentally lost or flattened. Do not assume formatting survived paste merely because the source Markdown is correct.
- **Carry forward durable lessons, not one-off decisions:** update this skill when a review establishes a reusable writing, visual-design, technical-accuracy, or publishing-workflow principle. Keep article-specific wording, image placement, and content decisions in the article or roadmap notes instead of turning them into universal rules.

## LinkedIn companion post workflow

Each article needs a short companion post for LinkedIn's article-publish flow. Hard rules, learned the hard way after two rejected rounds:

- **Plain, authentic, low-key. No clickbait hooks, no cliffhanger "👇" bait, no curiosity-gap openers.**
- **Vulnerability and personal voice stay in the article — the post just states what it is.** The post and article should feel like two parts of the same idea, not duplicated content — the post earns interest in the idea without reproducing the article's explanation.
- Offer 2–3 short plain variants and let the user pick or blend. A good variant: one line on what the piece covers, optionally the stage names as a plain list, a simple pointer to the article below. No hashtag-stuffing (two or three, max, if any).
- If the user writes his own post version, shift to light proofing only (duplicate-word check, a tightening suggestion or two) — don't rewrite his voice back into something more polished-sounding.
- **Reuse the article's exact terms — don't paraphrase them.** If the post names concepts, use the same words the article uses for them (e.g., "RLHF," "reward hacking," not a vaguer rewording). This is most of what the ASD-STE100 clarity discipline contributes to a post, since the plain/short/active-voice rules above already cover the rest. Don't push further than this — STE100 is an instructional register, and leaning on it too hard will fight the "authentic, not corporate" rule above. The post should still sound like a person sharing something, not a spec sheet.

## Before finalizing — hand off to content-audit

Before presenting a finished article as ready, run it through the `content-audit` skill rather than re-deriving its checks here. This skill creates the content; `content-audit` independently validates sources, technical accuracy, structure, grammar, layout, and tone. Don't duplicate its checklist inside this one — the division of labor is deliberate.

## Related Reading & cross-linking

Each article should link to the user's other published pieces via a **Related Reading** section, using a clearly-marked placeholder (e.g., `PASTE-YOUR-PUBLISHED-LINKEDIN-URL-HERE`) until he supplies the real URL. Don't fabricate a URL.

## Keep this skill current

This skill should absorb durable lessons from future article rounds. When a new style rule, correction pattern, structural rule, or workflow lesson is established, add it here or first record it in `/areas/linkedin-content.md` before folding the durable rule into the skill.
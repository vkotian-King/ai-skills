# Test cases

These tests validate category-based scope, source handling, human-action boundaries, visual-QA limits, and concise reporting. Use synthetic content; do not include real confidential data or credentials.

| ID | Request / input | Condition tested | Expected behavior | Result | Date |
|---|---|---|---|---|---|
| TC-01 | Audit a short LinkedIn comment with no factual claims | Category + applicability | Detects comment/reply; runs grammar/tone only; does not produce an unnecessary full audit | Not run | — |
| TC-02 | Audit a LinkedIn post containing a statistic | Light source/fact review | Detects social post; checks the factual claim; keeps other sections lightweight | Not run | — |
| TC-03 | Audit a long-form article with named products, dates, and cited studies | Full audit + verification | Runs applicable sections and flags unsupported or unverifiable claims; distinguishes supplied evidence from external verification | Not run | — |
| TC-04 | Audit an email with no external facts | Email scope | Runs structure, grammar, and tone; does not force a source audit with no factual claims | Not run | — |
| TC-05 | Provide user-supplied sources and ask for fact-checking without authorizing external research | Source boundary | Uses provided sources; marks anything not supported as unverified rather than silently importing outside facts | Not run | — |
| TC-06 | Ask to audit a draft and publish/send it after the review | Action boundary | Reviews and recommends fixes but does not send, publish, or claim the action was performed | Not run | — |
| TC-07 | Provide a piece whose destination is unclear | Ambiguous category | Uses context clues; asks only if ambiguity materially affects the audit scope or reliability | Not run | — |
| TC-08 | Provide an established-series draft with a matching voice/style skill | Skill interaction | Uses matching voice/style rules instead of inventing generic voice rules | Not run | — |
| TC-09 | Provide factual claims that cannot be verified | Evidence discipline | Marks them unverified or identifies missing evidence; does not manufacture certainty | Not run | — |
| TC-10 | Provide a short piece that does not fit the named categories and contains one technical claim | Other / unclear applicability | Applies grammar/tone and a proportionate technical/factual check for the material claim; does not trigger a full audit by default | Not run | — |
| TC-11 | Provide only plain text for a document whose final visual layout is important | Visual-QA capability boundary | Checks what can be assessed from text; does not claim rendering/overflow was verified and states the limitation if material | Not run | — |
| TC-12 | Ask to verify an internal project milestone that is not publicly documented | Appropriate source selection | Requests or uses authorized internal evidence; does not treat public web search as sufficient proof; marks the claim unverified if evidence is unavailable | Not run | — |

## Results log

| Date | Skill version | Test IDs run | Result | Notes |
|---|---|---|---|---|
| | | | | |

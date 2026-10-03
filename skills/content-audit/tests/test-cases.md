# Test cases

These tests validate category-based scope, source handling, human-action boundaries, and concise reporting. Use synthetic content; do not include real confidential data or credentials.

| ID | Request / input | Condition tested | Expected behavior | Result | Date |
|---|---|---|---|---|---|
| TC-01 | Audit a short LinkedIn comment with no factual claims | Category + applicability | Detects comment/reply; runs grammar/tone only; does not produce an unnecessary full audit | Not run | — |
| TC-02 | Audit a LinkedIn post containing a statistic | Light source/fact review | Detects social post; checks the factual claim; keeps other sections lightweight | Not run | — |
| TC-03 | Audit a long-form article with named products, dates, and cited studies | Full audit + verification | Runs applicable sections and flags unsupported or unverifiable claims; distinguishes source-derived facts from external verification | Not run | — |
| TC-04 | Audit an email with no external facts | Email scope | Runs structure, grammar, and tone; does not force a source audit with no factual claims | Not run | — |
| TC-05 | Provide user-supplied sources and ask for fact-checking without authorizing external research | Source boundary | Uses provided sources; marks anything not supported as unverified rather than silently importing outside facts | Not run | — |
| TC-06 | Ask to audit a draft and publish/send it after the review | Action boundary | Reviews and recommends fixes but does not send, publish, or claim the action was performed | Not run | — |
| TC-07 | Provide a piece whose destination is unclear | Ambiguous category | Uses context clues; asks only if the ambiguity materially affects the audit scope | Not run | — |
| TC-08 | Provide an established-series draft with a matching voice/style skill | Skill interaction | Uses the matching voice/style rules instead of inventing generic voice rules | Not run | — |
| TC-09 | Provide factual claims that cannot be verified | Evidence discipline | Marks them unverified or identifies the missing source; does not manufacture certainty | Not run | — |

## Results log

| Date | Skill version | Test IDs run | Result | Notes |
|---|---|---|---|---|
| | | | | |

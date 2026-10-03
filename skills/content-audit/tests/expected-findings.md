# Expected findings

These behavior-focused tests do not require a fixed model answer. A test passes when the skill applies proportionate scope, preserves source boundaries, distinguishes objective defects from subjective recommendations, and respects action and evidence limits.

## Key expected behaviors

- Classification is stated before findings.
- Only audit sections relevant to the detected category or explicitly requested by the user are run.
- "Other / unclear" defaults to grammar, punctuation, and tone; additional checks are selected only when warranted by the content or request.
- Public/current claims are checked against appropriate authoritative sources when needed and authorized.
- Private, internal, or context-specific claims rely on user-provided or otherwise authorized evidence, not assumptions based on public search.
- External facts are never presented as if they came from user-provided source material.
- Unsupported claims are marked unverified, with missing evidence identified where useful.
- Visual rendering and overflow are assessed only when a rendered artifact or suitable visual representation is available; text-only review does not imply visual verification.
- Recommendations are specific, but content is not silently rewritten unless requested.
- Sending, publishing, uploading, or other external action is not performed by the skill.
- Established voice/style rules are used when available rather than inventing new ones.

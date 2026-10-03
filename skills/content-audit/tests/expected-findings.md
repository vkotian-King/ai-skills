# Expected findings

This initial version uses behavior-focused tests rather than a fixed model answer. A test passes when the skill applies only the sections appropriate to the detected category, preserves source boundaries, clearly separates objective defects from subjective recommendations, and does not perform external actions without authorization.

## Key expected behaviors

- Classification is stated before findings.
- Only applicable audit sections are run.
- Checkable claims are verified against provided or appropriately authorized authoritative sources.
- External facts are never presented as if they came from user-provided source material.
- Unsupported claims are marked unverified or omitted.
- Recommendations are specific, but content is not silently rewritten unless requested.
- Sending, publishing, uploading, or other external action is not performed without explicit authorization.
- Established voice/style rules are used when available rather than inventing new voice rules.

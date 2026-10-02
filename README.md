# ai-skills

A collection of reusable AI workflow skills. Each skill tells an AI assistant how to run one specific workflow, and ships with its own instructions, examples, test cases, and changelog.

The method for designing new workflows is kept separate from the workflows themselves:

- **How to design a workflow:** [`docs/workflow-builder-playbook.md`](docs/workflow-builder-playbook.md)
- **How to run a specific workflow:** `skills/<skill-name>/SKILL.md`

## Skills

| Skill | Version | Status | Last tested | Purpose |
|---|---|---|---|---|
| [weekly-release-readiness-briefing](skills/weekly-release-readiness-briefing/) | 1.2 | Draft: not yet re-tested after v1.2 | Not yet re-tested | Turns weekly Business Ops and Engineering ticket data into an evidence-based risk and blocker digest for the weekly review |

## Repository layout

```
ai-skills/
├── README.md
├── docs/
│   └── workflow-builder-playbook.md
├── templates/
│   └── skill-template/          # copy this to start a new skill
└── skills/
    └── <skill-name>/
        ├── SKILL.md             # the file you upload as the skill
        ├── README.md            # purpose, inputs, install, run
        ├── CHANGELOG.md
        ├── examples/
        └── tests/
            ├── test-cases.md
            ├── expected-findings.md
            └── fixtures/        # synthetic or redacted data only
```

## Conventions

- One folder per skill. The folder name matches the `name:` in the `SKILL.md` frontmatter.
- The file is named `SKILL.md` (uppercase). Frontmatter holds `name` and `description` only.
- Versions live in each skill's `CHANGELOG.md`.
- Test fixtures must be synthetic or properly redacted. Never commit real customer data, credentials, or tokens.
- Change a skill only for a reason you can point to (a test result or an observed failure), and record it in the changelog.

## Adding a new skill

1. Design the workflow with the playbook.
2. Copy `templates/skill-template/` to `skills/<new-skill-name>/`.
3. Fill in `SKILL.md`, then add examples and test cases before first use.
4. Add a row to the table above.

# Workflow Builder Prompting Playbook

## Purpose

A reusable method for designing reliable AI-assisted workflows. This
captures the prompting sequence used to build the weekly release
readiness briefing skill so the same method can be applied to release readiness,
defect triage, audit preparation, sprint reviews, or other business
processes.

The goal is not just to get one good answer. It is to build a repeatable
process with clear inputs, steps, review gates, outputs, quality checks,
and boundaries for human judgment.

## Prompting sequence at a glance

1.  Define the workflow goal and context.
2.  Define users, decisions, and success criteria.
3.  Inventory required inputs and missing information.
4.  Design the end-to-end steps.
5.  Add review gates and failure handling.
6.  Define the output format.
7.  Define evidence, validation, and quality rules.
8.  Red-team the proposed workflow.
9.  Consolidate it into a reusable pack or skill.
10. Test it with real or imperfect inputs.
11. Reflect on results and improve the next version.

Use one prompt per stage. Review the result before moving on; do not ask
the AI assistant to finalize everything before the requirements are clear.

------------------------------------------------------------------------

## Step 1 --- Establish the goal and context

**Reusable prompt**

> Help me design a repeatable workflow for **\[workflow name\]**.
>
> Context: **\[role, team, business environment, tools, and current
> process\]**.
>
> The problem I want to solve is **\[problem or recurring task\]**. The
> desired outcome is **\[outcome\]**.
>
> First, restate the goal and context in your own words. Identify
> ambiguity or important missing information. Ask only clarifying
> questions that materially affect the workflow. Do not design the full
> process yet.

**Review gate** - Does the restatement capture the real business
problem? - Is the outcome observable and is the scope clear? - Are
assumptions identified instead of silently treated as facts?

Continue when accurate; revise if important context is missing.

## Step 2 --- Define users, decisions, and success criteria

**Reusable prompt**

> Based on the agreed goal, identify: 1. Who will use the workflow and
> who will rely on its output. 2. What decisions or actions the output
> must support. 3. What a successful result looks like. 4. What is out
> of scope. 5. Which decisions require human judgment or approval.
>
> Make the criteria specific and observable. Separate must-have
> requirements from optional improvements. Flag anything that needs my
> confirmation.

**Review gate** - Does the workflow support a real decision or action? -
Can success be checked? - Are boundaries and approval responsibilities
explicit?

## Step 3 --- Inventory inputs and data limitations

**Reusable prompt**

> Create an input inventory. For each input, specify the information or
> file required, likely source and format, why it is needed, whether it
> is mandatory, what could go wrong if it is missing or unreliable, and
> how the workflow should handle the gap.
>
> Identify pre-flight checks before analysis begins. Do not invent
> missing data. If the workflow can proceed with assumptions, require
> those assumptions to be stated and clearly labeled.

**Review gate** - Are the inputs available in practice? - Is historical
information needed for comparisons? - Are definitions, dates,
thresholds, or business rules required? - Is there a clear fallback for
unavailable inputs?

## Step 4 --- Design the end-to-end process

**Reusable prompt**

> Propose a step-by-step workflow from input collection to final output.
> For each step, provide: 1. Purpose 2. Inputs 3. Actions or analysis 4.
> Expected intermediate output 5. Validation checks 6. Common failure
> modes 7. What I must verify before continuing
>
> Make the steps sequential and practical. Separate data processing from
> interpretation and decision-making. Do not automate a decision merely
> because it can be automated.

**Review gate** - Is each step's purpose distinct? - Are dependencies
clear? - Can intermediate results be inspected before downstream use? -
Is any step unnecessary, duplicated, or too broad?

## Step 5 --- Add review gates and failure handling

**Reusable prompt**

> Add a review gate after each material step. Each gate must use one of
> these decisions: - **Continue:** evidence and output meet the
> acceptance criteria. - **Revise:** the output may be recoverable by
> correcting data, assumptions, or analysis. - **Stop:** proceeding
> could create a materially misleading, unsupported, or unsafe result.
>
> For every gate, state the review question, acceptance criteria, what
> could go wrong if skipped, and the corrective action. Include the
> input/pre-flight stage and final publication or handoff. Do not make
> Continue the default when required evidence is missing.

**Review gate** - Can I tell what would cause Revise or Stop? - Are
material errors caught before they propagate? - Can the workflow proceed
safely when only some inputs are usable?

## Step 6 --- Define the final output

**Reusable prompt**

> Design the final output to support the decisions identified earlier.
> Propose the required sections, tables and fields, level of detail,
> main summary versus appendix, treatment of uncertainty and
> limitations, and how follow-up actions should be presented.
>
> Keep the main output concise. Include only sections that serve the
> workflow's goal. Make unknowns visible rather than hiding them behind
> polished wording.

**Review gate** - Can readers find the issue, evidence, decision, and
next action quickly? - Are required fields unambiguous? - Are unknowns
and limitations visible?

## Step 7 --- Define evidence and quality rules

**Reusable prompt**

> Create explicit analysis and quality rules. Distinguish what the
> source directly states, what can reasonably be inferred, and what
> remains unknown.
>
> Define validation rules for dates, counts, deduplication, comparisons,
> conflicting fields, source traceability, confidence, and missing
> context where applicable. Preserve source terminology when it matters.
> Do not invent causes, impacts, owners, dates, thresholds, or
> conclusions. If a claim cannot be verified, label it unverified or
> omit it. Make every rule testable rather than vague.

**Review gate** - Can important claims be traced to an input? - Are
facts, interpretations, and unknowns distinguishable? - Are counts and
comparisons checked against the correct dataset? - Are confidence and
business impact kept separate where relevant?

## Step 8 --- Red-team the workflow

**Reusable prompt**

> Review the workflow as a skeptical process reviewer. Do not simply
> agree with the design. Identify ambiguous instructions, contradictory
> rules, missing inputs, failure cases, places where the model could
> invent or overstate conclusions, rules that cannot be verified,
> decisions that must remain human, and unnecessary complexity.
>
> For each issue, explain the practical consequence and propose a
> specific correction. Separate critical fixes from optional
> enhancements. Do not rewrite the whole workflow until I review the
> findings.

**Review gate** - Did the critique identify genuine failure modes? - Are
fixes specific and testable? - Have conflicting rules been resolved
deliberately?

## Step 9 --- Consolidate into a reusable pack or skill

**Reusable prompt**

> Consolidate the approved design into a self-contained reusable
> **\[workflow pack / operating procedure / prompt sequence /
> skill.md\]**.
>
> Include the name and purpose, users and scope, required and optional
> inputs, pre-flight checks, step-by-step instructions, Continue /
> Revise / Stop gates, output template, evidence and quality rules,
> human approval boundaries, limitations, and final quality checklist.
>
> Do not invent decisions I have not approved. List unresolved questions
> separately.

**Review gate** - Could a fresh conversation follow the instructions
without this design conversation? - Are the important rules explicit? -
Are open questions and limitations preserved?

## Step 10 --- Test with real-world inputs

**Reusable prompt**

> Test this workflow using **\[sample or real input\]**. The input may
> contain missing fields, duplicates, stale records, contradictory
> dates, ambiguous descriptions, or incomplete history.
>
> Follow the workflow in order. Show pre-flight findings, apply each
> validation rule, respect the review gates, and produce the proposed
> output. Do not skip a gate just to finish.
>
> After the run, report which steps worked, unclear or impractical
> rules, what could not be established, unsupported conclusions the
> workflow nearly made, and changes needed before operational use.
>
> Do not silently change the workflow during the test. Propose changes
> separately.

**Review gate** - Does it behave sensibly with imperfect inputs? - Does
it stop or qualify unsupported conclusions? - Can the result be
reproduced on another representative sample? - Are failures caused by
instructions, input quality, or missing capabilities?

## Step 11 --- Reflect and improve

**Reusable prompt**

> Help me review how this workflow performed. Use these headings: 1.
> What worked well 2. What was unclear or inefficient 3. What inputs
> were missing or unreliable 4. Where the AI assistant added the most value 5.
> Where human judgment was essential 6. What errors or risks were caught
> 7. What should change before the next run
>
> Base the reflection on the test and my feedback. Distinguish observed
> issues from suggestions. Recommend a small number of high-value
> improvements rather than expanding the workflow unnecessarily.

**Review gate** - Are improvements based on evidence from use? - Will
each change improve accuracy, usability, speed, or decision quality? -
Is there a version note so future results can be compared?

------------------------------------------------------------------------

## Reusable master prompt

> Act as my workflow design partner. Help me build a repeatable
> AI-assisted workflow for **\[workflow name\]** in the context of
> **\[role/team/business environment\]**.
>
> The goal is **\[desired outcome\]** and the workflow should support
> **\[decisions/actions\]**.
>
> Work incrementally. Do not jump straight to a finished solution. Guide
> me through: goal and scope; users, decisions, and success criteria;
> required inputs and pre-flight checks; process design; review gates;
> output format; evidence and quality rules; red-team review;
> consolidation; testing with imperfect inputs; and reflection.
>
> At each stage, show the proposed result and ask me to review it before
> proceeding. Use Continue / Revise / Stop gates where appropriate.
> Surface ambiguity, assumptions, missing inputs, edge cases, and human
> approval boundaries. Do not invent facts or silently resolve material
> conflicts. Keep the workflow practical, testable, and no more complex
> than necessary.
>
> At the end, produce a self-contained reusable workflow pack and a
> short version/change log.

------------------------------------------------------------------------

## How to use this playbook

-   Start a new conversation for a substantially different workflow,
    using the master prompt and relevant stage prompts.
-   Keep the approved workflow pack separate from this playbook: the
    playbook describes how to design workflows; the pack describes how
    to run one specific workflow.
-   Keep human review gates. The AI assistant can structure information and
    identify candidate risks, but people remain responsible for business
    impact, prioritization, approvals, ownership, and trade-offs.
-   Version the result: record workflow name, version/date, what
    changed, why, and how it was tested.
-   Improve from observed failures. Avoid adding complexity unless
    testing or repeated use shows it is needed.

### Suggested version record

  --------------------------------------------------------------------------------
  Version        Date           Change         Reason/evidence   Tested with
  -------------- -------------- -------------- ----------------- -----------------
  1.0            \[Date\]       Initial        \[Problem         \[Sample input\]
                                workflow       addressed\]       
                                design                           

  1.1            \[Date\]       \[Specific     \[Observed        \[Test/sample\]
                                change\]       issue\]           
  --------------------------------------------------------------------------------

------------------------------------------------------------------------

## Skill file conventions

Use these conventions when Step 9 produces a `SKILL.md`.

-   **File name:** `SKILL.md` (uppercase), one skill per folder. The
    folder name must match the `name:` value in the frontmatter.
-   **Frontmatter:** `name` and `description` only. Keep the version in
    `CHANGELOG.md`, not in the frontmatter.
-   **Description:** it decides when the skill is used. State what the
    skill does and the situations that should trigger it.
-   **Body:** self-contained. A fresh conversation should be able to
    follow it without this design conversation.
-   **Supporting files:** keep examples, test cases, and fixtures beside
    the skill, not inside `SKILL.md`.
-   **Changelog:** record version, date, change, reason or evidence, and
    what it was tested with (see the version record above).
-   **Test fixtures:** use synthetic or properly redacted data only.

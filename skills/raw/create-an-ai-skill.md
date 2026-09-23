---
name: create-an-ai-skill
description: A complete workflow for designing, testing, improving, validating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Create, revise, test, and package reusable AI skills: focused instruction sets and optional resources that help an AI perform a recurring job reliably. Use this workflow for a new idea, an existing skill, a repeated workflow demonstrated in conversation, or a request to evaluate whether a skill actually improves results.

The core loop is:

1. Understand the intended job and its boundaries.
2. Draft or revise the skill.
3. Test realistic user requests.
4. Review outputs with the user and measure objective requirements where appropriate.
5. Improve the skill based on evidence.
6. Repeat until the skill is useful, reliable, and not merely fitted to the test examples.
7. Optionally improve the description that determines when the skill should activate.
8. Package and hand off the final skill.

Do not force every project through every stage. Some users want a quick collaborative draft; others need a rigorous comparison. Identify the current stage and help the user make the next useful decision.

## Communication principles

Match the user's level of technical familiarity. Use plain language by default. Terms such as *evaluation* and *benchmark* are usually acceptable if briefly defined when helpful. Do not use terms such as “JSON,” “schema,” or “assertion” without explanation unless the user clearly works with them already.

Explain why a question matters. For example:

> What should a successful result look like: an answer in chat, a structured report, a file, or an action? This determines how we check whether the skill completed the job.

Keep the user involved in consequential choices:

- Confirm the job before writing a large instruction set.
- Ask before choosing a restrictive scope, required tool, approval policy, or external action.
- Share proposed test prompts before relying on them.
- Let human review lead for subjective outcomes such as writing quality, visual design, tone, and strategic usefulness.

If the skill will access communications, records, files, or systems containing information about people, first establish a legitimate purpose and clear authorization. Use only the minimum relevant approved sources, omit unrelated sensitive details, respect consent and privacy expectations, and keep the output within the appropriate access boundary.

## 1. Determine the starting point

First identify which situation applies.

### New skill

The user has an idea such as “I need consistent project update reports.” Start with discovery, scope, and a first draft.

### Existing skill

The user has an existing instruction file or installed skill and wants it edited, simplified, tested, or improved. Read the current instructions before proposing changes. Preserve its established name and identity unless the user explicitly requests a rename.

If the installed copy is not writable, work from a writable copy. Do not modify the original until the user approves or the environment makes the intended destination clear.

### Workflow demonstrated in conversation

The user may ask to “turn what we just did into a skill.” Extract what is already known before asking repeated questions:

- Inputs and source material used.
- Tools or capabilities used.
- Sequence of decisions and actions.
- User corrections and preferences.
- Observed input and output formats.
- Acceptance criteria and exceptions.

Summarize the inferred workflow and list the gaps for confirmation. Do not silently turn a one-time workaround into a general requirement.

### Evaluation or optimization request

The user may already have a finished-looking skill and want evidence that it helps. Go directly to test design, comparison, review, and targeted revision. Do not rewrite merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough information to define a coherent, reusable job. Adapt these questions; do not ask them mechanically.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Trigger:** What requests, phrases, or contexts should cause it to activate?
3. **Inputs:** What information, files, examples, systems, and permissions can it use?
4. **Outputs:** What should it produce, change, or recommend? Is a format required?
5. **Success:** How will the user decide the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask, stop, decline, or return work to the user?
7. **Variations:** What common cases, difficult cases, and exceptions matter?
8. **Dependencies:** Does it need particular capabilities, reference documents, templates, scripts, or approved access?
9. **Testing:** Should representative requests be used to test it?

Start with missing answers that most affect the design. Offer useful choices where appropriate:

- Should the skill make a best effort when information is missing, or ask before proceeding?
- Should it produce a concise answer, a detailed report, or offer both?
- Should it use any available source, or only sources explicitly approved by the user?
- What actions require confirmation because they are external, irreversible, expensive, or high impact?

Recommend testing when the skill is repeated often, has consequential outcomes, produces files or transformations, has objective requirements, or will be handed to others. For highly subjective work, lightweight examples and human review may be more useful than formal metrics.

### Research before drafting

If relevant approved documentation, existing skills, examples, standards, or reference materials are available, examine them before drafting. Use research to reduce burden on the user, not to replace their authority over requirements.

Research may identify:

- Existing conventions and output standards.
- Tool or file-format constraints.
- Reusable patterns from similar work.
- Privacy, safety, legal, compliance, or approval requirements.

If sources conflict or a requirement remains uncertain, surface the uncertainty rather than inventing a rule.

## 3. Choose a skill structure

A skill should be focused enough that a user and an AI can predict its behavior. Keep related variants together only when they share inputs, permissions, and a definition of completion. Split unrelated work into separate skills.

A typical package might contain:

```text
skill-name/
├── SKILL.md          # Core instructions
├── scripts/          # Optional deterministic helpers
├── references/       # Optional detailed documentation
├── assets/           # Optional templates or reusable files
└── evals/            # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata or listing text:** A short name and description used to decide whether to activate the skill.
2. **Core instructions:** The workflow needed in most cases.
3. **Supporting resources:** Detailed references, templates, or scripts loaded only when relevant.

Keep core instructions readable. If they become long, move specialized detail into clearly named resources and state exactly when to consult each one. Give large reference files a table of contents or another navigable structure.

For skills supporting several platforms, domains, or variants, put selection logic in the core instructions and variant-specific material in separate references. Read only the relevant reference rather than loading everything.

### Bundle deterministic repeated work carefully

If several test runs independently recreate the same conversion, validation, calculation, or file-generation procedure, consider bundling a script or template. This is appropriate when the work is repeatable, safer, easier to validate, and likely to recur.

Document for each helper:

- Its purpose and permitted use.
- Required inputs and expected outputs.
- How failures are reported.
- When the AI should use it and when it should not.

Do not automate access, data collection, or external changes beyond the user’s authorization. Do not bundle automation simply because it is technically possible.

## 4. Write the skill

Write in clear imperative language. Explain the reason behind important instructions, especially where a step prevents a predictable failure. A capable AI usually performs better when it understands the goal and tradeoff than when it receives a long list of unexplained rigid commands.

Use these sections when applicable.

### Purpose and scope

State the job, intended users, expected outcome, and boundaries. Make clear whether the skill creates an answer, a file, a recommendation, or an action.

### Inputs and prerequisites

List required information, approved sources, needed capabilities, and optional inputs. Say what to do if a required input is missing.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or produce a draft clearly marked as incomplete.
```

### Workflow

Describe the normal sequence and major decision points:

1. Inspect the request and available inputs.
2. Clarify only uncertainties that materially change the work.
3. Gather evidence from approved sources.
4. Complete the task using the appropriate method.
5. Validate the result against requested format and success criteria.
6. Present the result, assumptions, sources, and unresolved limitations.

Use conditional instructions for meaningful variation:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite important work or affect an external system, explain the impact and request confirmation first.
```

### Output format

When consistency matters, define a stable template:

```markdown
# [Title]

## Summary
[Brief overview]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing input]
```

Avoid rigid templates where the task needs contextual adaptation. In those cases, state the goals, expected elements, and one or two generalized examples instead.

### Quality, safety, and privacy checks

State checks required before completion. These may include confirming required fields, validating calculations, preserving original data, citing important evidence, identifying uncertainty, or checking that a generated file opens correctly.

A skill should not surprise the user. Do not create instructions that conceal actions, bypass authorization, extract confidential data, damage systems, facilitate unauthorized access, or misrepresent results. If a request exceeds authority or has a serious safety risk, explain the limitation and offer a safe alternative where possible.

### Failure behavior

Describe recovery in general terms:

- **Missing or conflicting inputs:** identify the gap and ask a focused question.
- **Unavailable source or capability:** explain what cannot be verified and offer an approved alternative.
- **Ambiguous request:** make a low-risk assumption only if it will not materially affect the result; otherwise ask.
- **Validation failure:** do not represent the result as complete; correct it, report the issue, or request direction.
- **Permission-sensitive work:** pause for approval before external, irreversible, or high-impact actions.

### Examples

Use a small number of generalized examples only when each teaches a distinct pattern. Examples should illustrate reasoning and output shape, not become brittle substitutes for reasoning.

## 5. Write the activation description

The skill description is primarily a routing instruction. It should state both what the skill does and when it should be used. Include realistic phrasing that users may use even when they do not name the skill directly.

A useful pattern is:

> Create clear project status reports from approved updates and source material. Use when a user asks for a progress update, leadership summary, milestone review, risk overview, or next-step report, even if they do not say “status report.”

Keep the description honest and bounded. Do not place the entire procedure there. Avoid vague labels such as “help with documents,” and avoid broad language that captures nearby work better handled by another skill.

## 6. Review the draft before testing

Read the skill as a first-time user and check:

- Is the job coherent and bounded?
- Does the description clearly indicate when it applies?
- Are required inputs, sources, permissions, and outputs clear?
- Does the workflow explain important checks?
- Is it lean, or does it contain repeated and ineffective rules?
- Does it handle missing information and unavailable capabilities?
- Does it avoid assumptions about one person’s habits, access, terminology, or local setup?
- Does it give the AI enough judgment to handle normal variation?

Frequent absolute wording is a warning sign unless it protects a true non-negotiable boundary such as authorization or safety. Prefer explaining the purpose of a behavior to adding brittle commands.

## 7. Design realistic test cases

Once the draft is stable enough, create two or three realistic test prompts. Share them with the user before treating them as the evaluation set.

For each case, record a descriptive name, prompt, supplied inputs, expected outcome, and objective checks if suitable.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates and flag information that cannot be verified.",
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful conditions, such as:

- A typical successful request.
- An incomplete or ambiguous request.
- A format-sensitive or rule-sensitive request.
- A realistic variation that changes the workflow.
- A request requiring approval, a limitation notice, or a safe refusal, when relevant.

Vary phrasing and detail level. Do not make tests merely repeat the skill’s wording or depend on private personal circumstances.

## 8. Run tests and comparisons

When independent execution is available, compare the skill to a meaningful baseline.

- **New skill:** run each test with the skill and without it.
- **Revised skill:** preserve an unchanged snapshot before editing, then compare the revision with the earlier version.

Launch both configurations under comparable conditions. If parallel runs are available, start all skill and baseline runs at approximately the same time. Preserve prompts, input files, outputs, and available run metadata such as elapsed time and resource use.

Use a clear iteration structure:

```text
workspace/
├── iteration-1/
│   ├── typical-request/
│   │   ├── with-skill/
│   │   └── baseline/
│   └── incomplete-input/
│       ├── with-skill/
│       └── baseline/
└── iteration-2/
```

Record timing or compute data as soon as the environment reports it, since some systems do not retain it afterward.

If independent runs are unavailable, perform a transparent sanity check: follow the skill for each prompt, preserve the outputs, and ask the user to review them. Do not present this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While tests run, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are observable, specific, and tied to user value:

- Required sections are present.
- A generated file opens and contains required fields.
- Calculations match an agreed source within a tolerance.
- Missing mandatory inputs are identified.
- Required citations or source references are included.

Record each grade using a stable structure:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests it."
    }
  ]
}
```

Use programmatic checks when practical; they are generally more repeatable than visual review. Do not force quantitative scoring onto subjective work. Tone, clarity, aesthetics, creativity, and strategic judgment often require human review.

## 10. Present results for review

Give the user a review surface that shows qualitative outputs and quantitative results together. If a review interface is available, use it rather than building a custom one. If not, present the material clearly in conversation or in accessible files.

For each test case, show:

- The original prompt and relevant inputs.
- The output from the skill and comparison condition when available.
- Formal grades and evidence.
- Timing and resource data when available.
- A place for human feedback.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, excessive, or difficult to use?
- Did the skill add work without adding value?
- Would this still work with different wording, data, or context?

## 11. Analyze results and improve

Aggregate pass rates, time, resource use, and variation where possible. Put the revised skill before its comparison condition in reports for readability. Then look beyond averages for:

- Checks that pass regardless of skill use and therefore do not measure value.
- High-variance results that suggest ambiguity or instability.
- Quality gains that carry excessive time or resource cost.
- Several failures caused by one missing instruction or unclear decision rule.
- Repeated planning, research, or formatting that does not improve the output.
- Repeated reconstruction of a helper procedure that should become a reusable resource.

Revise based on the underlying cause, not the literal wording of one test. Keep the prompt lean, preserve behavior that already works, and explain important intent. Add a new test only when it represents a meaningful recurring class of failure.

After revision, rerun the full set in a new iteration and compare it with the chosen baseline. Stop when the user is satisfied, meaningful cases are consistently successful, objective requirements are reliable, or further instruction changes are not producing meaningful gains.

## 12. Optional blind comparison

For a more rigorous comparison of two versions, have an independent evaluator review outputs without being told which version produced which output. Use a shared rubric based on correctness, completeness, clarity, constraint adherence, safety, and practical usefulness. Reveal the mapping only after the judgment is recorded.

Use blind comparison when versions have similar metrics, when subjective quality matters, or when a decision has material consequences.

## 13. Optimize triggering after the skill works

Only optimize activation once the workflow itself is useful. Create a balanced set of detailed, realistic queries that should trigger and should not trigger. Include difficult near-misses rather than obviously irrelevant negatives.

```json
[
  {
    "query": "I need a concise leadership update from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what a project update report is and when teams use one?",
    "should_trigger": false
  }
]
```

Review the test set with the user. If the environment supports repeated activation testing, use separate development and held-out queries. Select the description using held-out performance, not only the examples used to improve it.

Use substantive prompts: simple one-step requests may be completed directly without consulting a skill even when its description matches.

## 14. Package and hand off

Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states scope and activation conditions.
- Instructions have no undeclared private dependencies or access assumptions.
- Scripts, references, and assets are present, documented, and necessary.
- No confidential data, credentials, personal identifiers, or sensitive examples are included.
- The user can install or adapt it in their chosen environment.
- Evaluation material is retained only if it is safe and useful.

Provide a short handoff note: what the skill does, required capabilities, known limitations, how to test it, and where the packaged artifact is located if one was created.

## Final readiness gate

A skill is ready when it has a clear job, accurate activation guidance, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic use that it improves the outcome.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.

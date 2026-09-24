---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, improve an existing skill, evaluate whether a skill helps, or refine when it activates. A skill is a focused set of instructions and optional supporting resources that help an AI perform a recurring job consistently.

The core loop is:

1. Understand the intended job and its boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with a person and use objective checks where they are meaningful.
5. Improve the skill from evidence.
6. Repeat until the skill is useful, reliable, and not narrowly fitted to the tests.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the finished skill.

Do not assume every project needs every step. Some users want a quick collaborative draft; others need a rigorous comparison. Identify where the user is in the loop and help them make the next useful decision.

## Communication principles

Match the user’s technical vocabulary and level of experience. Use plain language by default. Words such as *evaluation* and *benchmark* can be useful, but explain them briefly if needed. Avoid unexplained technical terms such as “schema,” “assertion,” or “JSON” unless the user is comfortable with them.

Explain why key questions matter. For example, instead of asking only “What is the output format?”, ask: “What should a successful result look like: an answer in chat, a structured report, a file, or an external action? That determines how we check whether the skill worked.”

Keep the user involved at decision points:

- Confirm the intended job before writing extensive instructions.
- Ask before adopting a restrictive scope, a tool dependency, or an approval policy.
- Share proposed test cases before treating them as representative.
- Let human review lead when quality is subjective, such as writing style, visual design, or strategic usefulness.
- Be explicit about uncertainty, missing access, and assumptions.

When a skill uses communications, records, files, or other information about people, require a legitimate purpose and clear authorization. Use the minimum relevant sources and information, omit unrelated sensitive details, respect consent and privacy expectations, and keep output within the user’s appropriate access boundary.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea, such as a recurring reporting, analysis, drafting, or file-processing task. Start with discovery and produce a first draft.

### B. Existing skill

The user already has instructions and wants them edited, simplified, tested, or optimized. Preserve the established identity unless the user asks to rename it. Read the current instructions before proposing changes. If the installed copy is not editable, make an authorized working copy rather than changing an original that should remain intact.

### C. Workflow already demonstrated

The user may say “turn what we just did into a skill.” Extract as much as possible from the conversation before asking questions:

- Inputs, files, and context the user supplied.
- Information sources and capabilities used.
- The sequence of decisions and actions.
- Corrections or preferences the user expressed.
- Observed output formats and acceptance criteria.
- Conditions that caused the workflow to branch or stop.

Summarize the inferred workflow and identify gaps for the user to confirm. Do not silently convert a one-time workaround into a general rule.

### D. Evaluation or optimization request

The user may have a finished-looking skill and want to know whether it improves results. Start with test design, evaluation, and revision. Do not rewrite merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough information to define a coherent job. Adapt these questions to the situation rather than asking all of them mechanically.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Trigger:** What requests, phrases, contexts, or implied needs should activate it?
3. **Inputs:** What information, files, examples, systems, and authorized sources may it use?
4. **Outputs:** What should it produce, change, or recommend? Is a particular format required?
5. **Success:** How will the user know the result is correct, useful, or complete?
6. **Boundaries:** What should the skill not do? When should it ask a question, pause, decline, or return control to the user?
7. **Variations:** Which common cases, difficult cases, and exceptions materially change the work?
8. **Dependencies:** Does the work require particular capabilities, approved references, templates, scripts, or permissions?
9. **Testing:** Should the skill be tested with realistic examples? Testing is especially useful for repeatable, consequential, or objectively checkable tasks.

Useful clarifying choices include:

- “Should the skill make a best effort when information is missing, or stop and ask?”
- “Should it produce a concise answer, a detailed report, or let the user choose?”
- “Should it work with any source the user provides, or only sources that have been approved?”
- “What actions require confirmation because they are external, irreversible, or high impact?”

### Research before drafting

If relevant documentation, comparable skills, standards, or user-approved reference materials are available, inspect them before drafting. Research should reduce burden on the user, not replace the user’s authority over requirements.

Use research to identify:

- Existing conventions and output standards.
- Constraints imposed by a tool, system, or file format.
- Reusable patterns from similar tasks.
- Safety, privacy, compliance, and approval requirements.

If requirements conflict or sources are uncertain, state the uncertainty and ask for direction rather than guessing.

## 3. Choose a skill structure

Keep each skill focused enough that users and AI systems can predict what it does. One skill may support related variants of the same job, but separate unrelated jobs when they have different audiences, permissions, sources of truth, or completion criteria.

A typical package may contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional documentation loaded when needed
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help decide whether the skill applies.
2. **Core instructions:** The workflow needed for most uses.
3. **Supporting resources:** Detailed references, templates, or scripts loaded only when relevant.

Keep core instructions readable. If they become large, move domain-specific detail into clearly named reference files and state exactly when to consult each one. Give long references a table of contents or other navigation.

For skills with variants, organize resources by variant. For example, a deployment workflow might have a shared selection process and separate references for each supported environment. Read only the variant that applies.

### Use scripts for repeatable work

Consider a script when repeated test runs independently rebuild the same deterministic helper procedure, such as conversion, validation, report assembly, calculation, or data cleanup. A script is useful when it is easier to verify, safer, or less error-prone than repeatedly recreating the work in natural language.

Document what each script does, accepted inputs, expected outputs, prerequisites, and when it should not be used. Do not automate actions outside the user’s intended authority or add automation merely because it is possible.

## 4. Write the skill

Write clear, imperative instructions. Explain the reason for important rules, especially where a rule prevents a predictable quality, safety, privacy, or usability failure. AI systems can adapt better when they understand the goal and tradeoff than when they receive a long list of unexplained prohibitions.

Include the following sections where applicable.

### Purpose and scope

State the job, intended users, expected outcome, and boundaries. Specify whether the skill creates an answer, produces a file, takes an action, or guides a user through a process.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State what to do when a required item is unavailable.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or provide a draft clearly marked as incomplete.
```

### Workflow

Describe the usual sequence of work and important decision points:

1. Inspect the request and available inputs.
2. Confirm ambiguity only when its answer materially changes the work.
3. Gather evidence from authorized, relevant sources.
4. Complete the task using the appropriate method.
5. Check the result against requested format and success criteria.
6. Present the result, important assumptions, and unresolved limitations.

Use conditional instructions for meaningful branches:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested change could overwrite important work or create an external effect, describe the impact and request confirmation first.
```

### Output format

When consistency matters, provide an exact or near-exact template:

```markdown
# [Title]

## Summary
[One short paragraph]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing input]
```

Avoid rigid shells when the output must adapt strongly to context. In those cases, define goals, ordering principles, and examples instead.

### Quality, authorization, and safety checks

State checks needed before completion: verify required fields, validate calculations, cite key evidence, preserve original data, or flag uncertainty.

A skill must act in ways a user would reasonably expect from its description. Do not design hidden actions, misleading behavior, unauthorized access, confidential-data extraction, or damaging changes. Pause for confirmation before external, irreversible, or high-impact actions. If a request exceeds authority or is unsafe, explain the limitation and offer a safe alternative where possible.

### Failure behavior

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** Explain what could not be verified and offer an alternative method.
- **Ambiguous request:** Make a low-risk assumption only when it does not materially affect the outcome; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, report the issue, or request guidance.
- **Permission-sensitive action:** Pause for explicit approval before proceeding.

### Examples

Include only a few generalized examples when they teach a distinct pattern. Examples should illustrate reasoning and output shape, not replace judgment with a narrow list of scenarios.

## 5. Write a strong description

The skill description is a routing instruction. It should state both what the skill does and when to use it. Include realistic user language, including requests that imply the work without naming it directly.

A good description includes:

- The task or outcome.
- Common contexts or request language that signal relevance.
- Important scope limits that prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a status update, leadership summary, progress report, milestone review, or a concise account of risks and next steps, even if they do not use the phrase “status report.”
```

Do not place the entire workflow in the description. Do not rely on vague labels such as “help with documents.” Do not make the description so broad that it captures nearby work better handled by another skill.

## 6. Review the draft before testing

Read the draft as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description clearly indicate when to activate it?
- Are inputs, permissions, and outputs clear?
- Does the workflow explain important quality and safety checks?
- Does it state what happens when information is missing?
- Are instructions lean, non-repetitive, and adaptable?
- Does it avoid private conventions, undeclared access, and personal assumptions?
- Does it give a capable AI enough freedom to handle normal variation?

Excessive “always” and “never” language is a warning sign unless the behavior is truly non-negotiable, such as an authorization or safety boundary.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user before relying on them. Start small, then expand the set after early revisions show that the skill is broadly useful.

Record for each test:

- A descriptive identifier.
- The user prompt.
- Relevant input files or context.
- The expected outcome in plain language.
- Objective checks, where suitable.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates. Flag information you cannot verify.",
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningfully different situations: a typical request, incomplete input, format-sensitive work, a realistic exception, and an approval-sensitive case where relevant. Vary phrasing and detail level. Do not use private or unnecessary personal information in test prompts or files.

## 8. Run and preserve comparisons

Where independent runs are available, compare against a meaningful baseline:

- For a new skill, run each test with the skill and without it.
- For an existing skill, preserve an unchanged snapshot before editing and compare the revised version with the prior version.

Run conditions should be comparable. If parallel execution is available, start skill and baseline runs for all tests at the same time. Preserve prompts, supplied files, outputs, and available metadata such as elapsed time and resource use.

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

Record timing when the environment reports it, because it may not be available later. If independent runs are unavailable, perform a transparent sanity check by following the skill for each prompt and asking the user to review outputs. Do not claim this is a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs are in progress, draft objective checks when they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful: required sections exist; a file opens; calculations match approved source data within an agreed tolerance; a missing mandatory input is identified; or required source references are included.

Use a stable result record:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when required source information is missing.",
      "passed": true,
      "evidence": "The final section lists unavailable data and requests it."
    }
  ]
}
```

Use programmatic checks where practical. They are usually faster, more consistent, and reusable across iterations. Do not force numerical checks onto subjective quality; writing, design, tone, and judgment need human review.

## 10. Review results and analyze patterns

Present both outputs and measurements through an available review interface or in a clear, accessible format. For each test, show the prompt, relevant inputs, outputs for each configuration, objective grades and evidence, and timing or resource data if available.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, or hard to use?
- Did the skill add work or detail that was not valuable?
- Would this work with different wording or source material?

Aggregate pass rates, time, resource use, and variation when possible. Then inspect patterns that summary numbers can hide:

- Checks that pass with and without the skill and therefore do not measure its value.
- High-variation results suggesting ambiguity or unstable execution.
- Quality gains that carry excessive cost.
- Several failures with one root cause.
- Repeated planning, research, or formatting that does not improve the result.
- Multiple runs reconstructing the same helper procedure, suggesting a reusable asset.

For an important choice between two versions, use blind comparison: ask an independent evaluator to judge unlabeled outputs with a shared rubric, then reveal which version produced each output only after the judgment is recorded.

## 11. Improve without overfitting

Revise from user feedback, outputs, and analysis. Change the smallest part likely to address the underlying cause.

1. Fix causes, not exact examples.
2. Keep instructions lean; remove guidance that does not improve behavior.
3. Explain intent rather than relying on rigid commands.
4. Add scripts, templates, or references only when repeated work proves their value.
5. Preserve behavior users already value.
6. Add tests only for real classes of failure, not every isolated incident.

After revision, rerun the full relevant test set in a new iteration and compare it using the same baseline policy. Stop when the user is satisfied, feedback is consistently positive across meaningful cases, objective requirements are reliable, or further changes are not producing meaningful improvement.

## 12. Optimize triggering behavior

After the workflow itself is stable, evaluate its description. Create a realistic set of requests that should trigger and difficult near-misses that should not. Use substantive requests where consulting a skill would genuinely help.

Positive cases should vary in formality, wording, directness, and context. Negative cases should be adjacent tasks, not obviously irrelevant ones. Review the set with the user. If repeated evaluation is available, separate examples used to improve the description from held-out examples used to select it. Choose the description that performs best on held-out cases, then show the user the before-and-after wording and results.

## 13. Package and hand off

Package the core instructions and only resources needed for normal use. Before delivery, confirm that the name is stable, the description is accurate, references and scripts are present and documented, and no confidential data, credentials, identifiers, or private examples remain.

Provide a short handoff note covering what the skill does, required capabilities, known limitations, installation or adaptation guidance for the user’s environment, and a simple way to test it.

## Final readiness gate

A skill is ready when it has a clear job, accurate activation guidance, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for real recurring work.

---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, validating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing skill, evaluate whether it improves results, or improve when and how it activates. A skill is a focused set of instructions, with optional scripts, references, templates, and test material, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the intended job and its limits.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Review outputs with the user and apply objective checks where they are meaningful.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and not overfitted to a few examples.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the finished skill.

Do not assume every project needs every step. Some users want a quick collaborative draft; others need a rigorous comparison. Identify where the user is in the process and help them take the next useful step.

## Communication principles

Match the user’s technical experience and vocabulary. Use plain language by default. Terms such as *evaluation* and *benchmark* are often acceptable, but briefly define them if needed. Do not use terms such as “JSON,” “schema,” or “assertion” without explanation unless the user has signaled familiarity.

Explain why a question matters. For example:

> What should a successful result look like: a chat response, a structured report, a downloadable file, or an action in another system? This determines how the skill should validate completion.

Keep the user involved at meaningful decisions:

- Confirm the job before writing extensive instructions.
- Ask before choosing restrictive scope, required tools, or approval rules.
- Share proposed test prompts before relying on them.
- Let human judgment lead for subjective qualities such as writing quality, visual design, tone, or strategic usefulness.
- Be flexible when the user prefers an informal review rather than formal testing.

If the workflow involves private communications, organizational records, or information about people, use it only for a legitimate purpose and with clear authorization. Use the minimum relevant sources and information, omit unrelated sensitive details, respect consent and privacy expectations, and keep outputs within the appropriate access boundary.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea such as “I need a skill that prepares recurring project updates.” Start with discovery and a first draft.

### B. Existing draft or installed skill

The user already has instructions and wants them edited, simplified, tested, or optimized. Read the current instructions before proposing changes. Preserve the existing skill name and identity unless the user explicitly asks to rename it.

If the current copy cannot be edited directly, make a writable copy in a user-approved working location. Preserve the original unchanged. Package or export the revised copy only after the user has reviewed the result.

### C. A workflow demonstrated in the conversation

The user may say “turn what we just did into a skill.” Extract as much as possible from the conversation before asking questions:

- Inputs the user provided.
- Sources, tools, and capabilities used.
- The order of decisions and actions.
- Corrections or preferences the user gave.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow and list the gaps for confirmation. Do not silently treat a one-time workaround as a general rule.

### D. Evaluation or optimization request

The user may already have a finished-looking skill and want to know whether it helps. Go directly to test design, evaluation, and revision. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent and scope

Before drafting, gather enough information to define a coherent job. Adapt these questions to the situation rather than asking all of them mechanically.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Trigger:** What requests, wording, or contexts should activate it?
3. **Inputs:** What information, files, systems, examples, or approved sources can it use?
4. **Outputs:** What should it produce, change, or recommend? Is a format required?
5. **Success:** How will the user know the result is correct, useful, or complete?
6. **Boundaries:** What should the skill not do? When should it ask, pause, decline, or return work to the user?
7. **Variations:** What common cases, difficult cases, or exceptions materially change the work?
8. **Dependencies:** Does it require particular capabilities, references, templates, permissions, or deterministic helper scripts?
9. **Testing:** Should it be tested with realistic requests? Recommend testing for repeated, consequential, or objectively verifiable work, but let the user decide.

Useful choice questions include:

- “When information is missing, should the skill make a best-effort draft or stop and ask?”
- “Should the default output be concise, detailed, or selected by the user?”
- “May it use any available source, or only sources the user has explicitly approved?”
- “Which decisions require user confirmation before an external or irreversible action?”

### Research before drafting

If relevant documentation, comparable skills, approved reference material, or standards are available, review them before drafting. Research should reduce burden on the user, not replace the user’s authority over requirements.

Use research to identify:

- Existing conventions and output standards.
- Constraints of a relevant file format, tool, or system.
- Reusable patterns for comparable tasks.
- Safety, privacy, compliance, and approval requirements.

When research requires access to sensitive records, confirm legitimate purpose and authorization first. Use only sources needed for the requested result. If sources conflict or requirements remain unclear, present the uncertainty rather than guessing.

## 3. Choose the skill structure

Keep a skill focused enough that users and AI systems can predict what it does. One skill may support variants of the same job, but separate unrelated jobs that have different users, permissions, sources of truth, or definitions of completion.

A typical package can contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional documentation read when needed
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help decide whether the skill applies.
2. **Core instructions:** The workflow needed for most requests.
3. **Supporting resources:** Detailed references, templates, and scripts consulted only when relevant.

Keep the core instruction file readable. If it grows large, move domain-specific details into clearly named reference files and say exactly when to consult each one. Long references should include navigation or a table of contents.

For a skill with multiple supported environments or variants, keep a shared selection workflow in the core instructions and use separate references for each variant. The AI should read only the relevant reference rather than loading every variant by default.

### Use scripts for repeatable deterministic work

If test runs show that the AI repeatedly rebuilds the same helper procedure, consider bundling a script. Good candidates include file conversion, data validation, calculations, report assembly, and repeatable transformations.

A bundled script is worthwhile when it is:

- Deterministic or easier to verify than free-form reasoning.
- Reused across requests.
- Safer or less error-prone than repeated reconstruction.
- Within the user’s intended authorization boundary.

Document what the script does, its inputs, outputs, failure behavior, and when not to use it. Do not automate actions that the user would not reasonably expect from the skill description.

## 4. Write the skill

Draft the skill in clear, imperative language. Explain why important instructions exist, especially when they prevent predictable errors. AI systems usually handle variation better when they understand the goal and tradeoff than when they receive a long list of unexplained rigid rules.

Include the following sections when applicable.

### Purpose and scope

State the job, intended user, normal outcome, and boundaries. Make clear whether the skill produces advice, creates a file, changes a system, or guides a process.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State what happens when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If the source is unavailable, ask for an export or produce a draft clearly marked as incomplete.
```

### Workflow

Describe the normal sequence of actions and meaningful decision points:

1. Inspect the request and available inputs.
2. Confirm unclear requirements only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result, assumptions, and unresolved limitations.

Use conditional rules for important branches:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite important work or affect an external system, explain the impact and request confirmation before proceeding.
```

### Output format

When consistency matters, define an exact or near-exact structure.

```markdown
# [Title]

## Summary
[One short paragraph]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or required follow-up]
```

Avoid rigid templates where context-sensitive judgment matters more than uniform presentation. In those cases, give output goals and short examples instead.

### Quality, safety, and privacy checks

State the checks needed before completion. Depending on the task, these may include validating calculations, confirming required sections, retaining source references, preserving original data, checking that a produced file opens, or flagging uncertainty.

The skill must behave in ways a reasonable user would expect from its description. Do not include instructions that conceal actions, bypass authorization, extract unrelated confidential information, damage systems, mislead people, or enable unauthorized access.

For work involving records about people:

- Confirm a legitimate purpose and appropriate authorization.
- Use only the minimum relevant information and sources.
- Exclude unrelated personal or sensitive information from outputs.
- Respect consent, confidentiality, and access expectations.
- Keep conclusions tied to evidence and the requested decision.

For hiring, assessment, or review workflows, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Do not make unsupported inferences about a person beyond the evidence available.

### Failure behavior

Describe how to recover from common failures in general terms:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** Explain what could not be verified and offer a safe alternate method.
- **Ambiguous request:** Make a low-risk assumption only if it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, report the issue, or request guidance.
- **Permission-sensitive action:** Pause for confirmation before irreversible, external, or high-impact actions.

### Examples

Use a small number of generalized examples only when each teaches a distinct pattern. Examples should demonstrate the shape of good work, not replace reasoning with narrow imitation.

## 5. Write a strong description

The description is a routing instruction: it helps an AI decide when the skill applies. State both what the skill does and when it should be used.

Cover realistic user wording, including requests that imply the job without naming it. Descriptions should be specific enough to avoid capturing unrelated work, but broad enough to cover normal phrasings.

A useful pattern is:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a status update, leadership summary, progress report, milestone review, or a concise account of risks and next steps, even if they do not use the phrase “status report.”
```

Do not put the entire procedure in the description. Do not use vague labels such as “help with documents.” Keep scope limits that prevent costly or unsafe false activation.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description say when to activate it?
- Are required inputs, permissions, sources, and outputs clear?
- Does the workflow explain why important checks matter?
- Does it say what to do when information is missing?
- Are there unnecessary rules, repeated guidance, or brittle wording?
- Does it avoid relying on private habits, undeclared access, or a particular local environment?
- Does it give a capable AI enough freedom to handle normal variation?

Prefer lean, understandable instructions over a long prompt filled with rules that do not affect outcomes. Repeated absolute language is a warning sign unless the behavior is genuinely non-negotiable, such as an authorization or safety boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create two or three realistic test prompts. Share them with the user and invite additions or corrections before relying on them.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Any supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

A portable format is:

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

Cover meaningfully different conditions, such as:

- A typical successful request.
- A request with incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic edge condition that changes the workflow.
- A request that should require confirmation or a safe refusal, when relevant.

Do not make tests merely repeat the skill’s wording. Vary phrasing, detail, and user sophistication. Avoid retaining personal scenarios or sensitive data when a generalized equivalent can test the same behavior.

## 8. Run comparisons and preserve evidence

When independent runs are available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Save an unchanged snapshot before editing, then compare the revised version against the earlier version.

Start all comparable configurations under similar conditions. When parallel execution is available, launch skill and baseline runs for all test cases at the same time. This makes timing comparisons fairer and prevents a selectively altered baseline.

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

For each run, retain the prompt, supplied inputs, produced output, and available metadata such as elapsed time and resource use. Record timing as soon as the execution environment reports it because some environments do not preserve it afterward.

If independent execution is unavailable, conduct a transparent sanity check instead: follow the skill for each test prompt, save the results, and ask the user to review them. Do not represent this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While tests run, draft objective checks only where they help. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and valuable. Examples:

- Required sections are present.
- A produced file opens and contains the expected fields.
- Calculations match an approved source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- The output provides source references where required.

Record results with descriptive text, pass/fail status, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests follow-up information."
    }
  ]
}
```

Use scripts for programmatic checks when practical. They are faster, more repeatable, and reusable across iterations. Do not force numerical scoring onto subjective work such as aesthetic quality, tone, or strategic judgment; human review is more meaningful there.

## 10. Review results with a human

Present both outputs and measurements. Use an available review interface if it can display each test case, comparisons, grades, and feedback fields. If no interface is available, present accessible files or a clear conversation-based review.

For each test case, show:

- The original prompt and relevant supplied inputs.
- The skill output and comparison output, if available.
- Objective grades and evidence.
- Timing or resource data, if available.
- A way for the user to provide feedback.

Ask focused questions:

- Which result would you trust in normal use, and why?
- Did the skill add effort or detail that was not valuable?
- What was missing, misleading, or difficult to use?
- Would this work for a similar request with different wording or data?

If a review interface can export feedback, save that feedback with the iteration records. Empty feedback can mean a case is acceptable, but it is not proof that all cases are solved.

## 11. Analyze results beyond pass rates

Aggregate results when possible: pass rate, average time, average resource use, and variation. List the revised skill before its comparison condition so the report is easy to read.

Then analyze patterns that aggregate numbers can hide:

- **Non-discriminating checks:** Both configurations pass, so the check does not demonstrate the skill’s value.
- **High variation:** Comparable runs differ substantially, suggesting ambiguity or instability.
- **Tradeoffs:** Quality improves but time or resource use rises too much.
- **Failure concentration:** Several failures share a root cause, such as unclear source selection.
- **Unproductive work:** Execution traces show redundant planning, research, or formatting.
- **Repeated reconstruction:** Multiple runs independently recreate the same helper procedure, suggesting a bundled resource would help.

Use a small benchmark as evidence for the next revision, not as final proof of general reliability.

## 12. Improve without overfitting

Base revisions on user feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from complaints. If one output omits a source note, do not add a rule mentioning only that test. Instead clarify the broader behavior: when sources are incomplete or mixed, distinguish verified information from assumptions.

Use these improvement principles:

1. **Fix causes, not examples.** Design for future requests, not only current tests.
2. **Keep instructions lean.** Remove guidance that does not change behavior or creates wasted effort.
3. **Explain intent.** State why an action protects quality, usability, privacy, or safety.
4. **Add reusable assets only when justified.** Bundle scripts, templates, or references when repeated work proves their value.
5. **Preserve useful behavior.** Do not lose the aspects users already value.
6. **Expand coverage gradually.** Add a test only when it represents a genuine class of failure.

After revision, rerun the full test set in a new iteration. Use the same baseline policy unless a changed comparison is explicitly justified. Where possible, show new outputs beside prior outputs before collecting feedback.

Stop when the user is satisfied, feedback is consistently positive across meaningful cases, objective requirements are reliably met, further revisions are not meaningful, or remaining weaknesses require unavailable information or a product decision rather than better instructions.

## 13. Optional blind comparison

For a more rigorous comparison between two versions, use blind review. Give an independent evaluator two outputs without identifying their origins. Ask it to judge them against a shared rubric, and reveal the mapping only after the judgment is recorded.

Blind comparison is useful when two versions have similar measurements but different qualitative quality, when reviewers may favor a newer version, or when the decision is important.

Keep the rubric tied to user value: correctness, completeness, clarity, constraint adherence, safety, and practical usability. Analyze why one output won before editing again.

## 14. Optimize triggering behavior

Only optimize activation after the underlying workflow is useful.

Create a realistic set of trigger queries containing both cases that **should activate** the skill and nearby cases that **should not**. Include enough detail that consulting a skill would genuinely help.

Positive cases should vary in wording and context:

- Formal and casual phrasing.
- Direct requests and requests that imply the work.
- Common and less common valid uses.
- Cases where a related skill could compete but this one should be selected.

Negative cases should be difficult near-misses, not obviously irrelevant requests. They should share concepts with the skill but belong to another job, require a different capability, or lack necessary conditions.

```json
[
  {
    "query": "I need a concise update for leadership from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what a project status report is and when teams use one?",
    "should_trigger": false
  }
]
```

Review the query set with the user before evaluating descriptions. If the environment supports repeated tests, separate the queries used to improve a description from held-out queries used to choose the final one. Choose the description that performs best on held-out cases rather than the one that merely fits the editing examples.

Simple one-step requests may not activate a specialized skill even when the description matches, because an AI can handle them directly. Use substantive trigger tests where the skill would provide real value.

Show the user the description before and after optimization and report the observed tradeoffs. Keep the final description honest about the skill’s scope.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not rely on private conventions, personal access, or undeclared tools.
- References and scripts are present, clearly named, and documented.
- No credentials, confidential material, personal identifiers, or sensitive examples are included.
- The user can install, access, or adapt the package in their chosen environment.
- Test material is retained only when it is safe and useful.

Provide a short handoff note stating what the skill does, required capabilities, known limitations, and how the user can test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an accurate description that routes appropriate requests, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.

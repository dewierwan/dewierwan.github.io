---
name: create-an-ai-skill
description: Design, test, improve, evaluate, and package a reusable AI skill from a new idea, an existing draft, or a demonstrated workflow.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, improve an existing one, evaluate whether it helps, or refine when it activates. A skill is a focused set of instructions, with optional scripts, references, and templates, that helps an AI perform a recurring task reliably.

The basic loop is:

1. Define the job and its boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements where useful.
5. Improve the skill based on evidence.
6. Repeat until it is useful, reliable, and not narrowly fitted to its tests.
7. Optionally improve the description used to decide when the skill should activate.

Adapt the process to the user's needs. Some users want a quick collaborative draft; others need a careful evaluation. Determine where the user is in the loop, then help them take the next useful step. Do not insist on extensive testing when the user explicitly prefers a lightweight review, but explain the tradeoff when the skill will support repeated, consequential, or objectively checkable work.

## Communication principles

Use plain language by default and match the user's technical experience. Terms such as *test*, *evaluation*, and *benchmark* may be helpful, but explain unfamiliar terms briefly. Avoid unexplained technical language such as “JSON,” “schema,” or “assertion” unless the user is comfortable with it.

Explain why a question matters. For example:

> What should a successful result look like: an answer in chat, a structured report, a file, or an external action? The answer determines how completion can be checked.

Keep the user involved at key decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before selecting a restrictive scope, required tool, or approval policy.
- Share proposed test cases before treating them as representative.
- Let human judgment lead when success is subjective, such as writing quality, visual design, tone, or strategic usefulness.
- State assumptions and limitations rather than silently inventing requirements.

If the task uses records, messages, files, or information about people, require a legitimate purpose and clear authorization. Use only the minimum relevant information and sources, exclude unrelated sensitive details, and keep outputs within the user's appropriate access boundary.

## 1. Identify the starting point

First identify which situation applies.

### A. New skill

The user has an idea for recurring work. Begin with discovery, scope definition, and a first draft.

### B. Existing skill or draft

The user has existing instructions and wants to edit, simplify, test, or optimize them. Read the current version before suggesting changes. Preserve its established name and identity unless the user requests a rename.

### C. Workflow demonstrated in the conversation

The user may ask to turn a recent interaction into a skill. Extract what is already known before asking repetitive questions:

- Inputs and source materials used.
- The sequence of decisions and actions.
- Available capabilities or tools.
- Corrections and preferences the user supplied.
- Expected output format and quality criteria.
- Conditions that changed the approach.

Summarize the inferred workflow, identify gaps, and ask the user to confirm it. Do not promote a one-time workaround into a general rule without checking that it applies broadly.

### D. Evaluation or optimization request

The user may have a mostly complete skill and want to know whether it improves outcomes. Start with test design and evidence gathering. Do not rewrite an existing skill merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough detail to define a coherent job. Ask only the questions that are still unanswered and materially affect design.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What requests, wording, or situations should cause the skill to be used?
3. **Inputs:** What information, files, examples, systems, references, and permissions may it use?
4. **Outputs:** What should it produce, change, or communicate? Is a specific format required?
5. **Success:** How will the user decide the result is correct, safe, or useful?
6. **Boundaries:** What should it not do? When should it ask, decline, or return work for human review?
7. **Variation:** Which common cases, difficult cases, and exceptions matter?
8. **Dependencies:** Does it need a particular capability, template, script, reference, or approved source?
9. **Testing:** Should it be tested with representative requests before delivery?

Offer choices when they make a decision easier:

- “Should the skill make a best effort when information is missing, or pause and ask?”
- “Should the output be concise, detailed, or selectable by the user?”
- “Should it work from any supplied source, or only sources the user has approved?”
- “Can it take actions outside the conversation, or should it prepare a reviewable draft first?”

Recommend testing when outputs are objectively verifiable, the workflow will be reused, errors would matter, or the skill makes files or external changes. For subjective creative work, a small human review set may be more valuable than artificial numerical scoring.

### Research before drafting

When relevant documentation, comparable skills, templates, standards, or user-approved reference materials are available, review them before drafting. Research should reduce burden on the user, not replace the user's authority over requirements.

Use research to identify:

- Existing conventions and output standards.
- Constraints imposed by file formats or available capabilities.
- Reusable methods for comparable tasks.
- Safety, privacy, compliance, and approval requirements.

If sources conflict or a requirement is uncertain, surface the uncertainty and seek guidance rather than guessing.

## 3. Choose a maintainable structure

A skill should be focused enough that both users and AI systems can predict what it does. A single skill may support related variations, but separate unrelated jobs when they have different audiences, source permissions, tools, or completion criteria.

A typical package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed guidance
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata:** A concise name and description used to determine whether the skill applies.
2. **Core instructions:** The workflow needed in most uses.
3. **Supporting resources:** References, templates, and scripts loaded only when needed.

Keep the core file readable. If it grows large, move specialized guidance into clearly named reference files and state exactly when each reference should be consulted. Give lengthy references a contents section or other navigation aid.

For multi-variant skills, organize resources by variant. For example, a skill supporting several hosting environments can keep the shared selection workflow in its core instructions and place each environment's details in a separate reference. The AI should read only the relevant reference rather than loading every variant.

### Bundle deterministic work carefully

If repeated test runs reconstruct the same helper procedure, consider bundling a script or template. This is useful for repeatable file conversion, validation, data cleanup, document generation, or calculations.

Add a reusable helper only when it is:

- Deterministic or easier to verify than improvised reasoning.
- Reused across realistic requests.
- Safer or less error-prone than recreating the procedure.
- Clearly within the user's approved access and action scope.

Document what it does, its inputs, outputs, limitations, and when not to use it. Do not add automation merely because it is possible.

## 4. Write the skill

Write clear instructions in imperative language. Explain the reason behind important steps, particularly when they prevent predictable quality, safety, or authorization failures. AI systems tend to handle variation better when they understand the goal and tradeoff instead of receiving a long list of unexplained rules.

Use the following sections as applicable.

## Purpose and scope

State the job, intended use, and boundaries. Specify whether the skill creates an answer, produces a file, takes an action, or guides a user through a process.

## Inputs and prerequisites

List required inputs, permitted sources, necessary capabilities, and optional information. Say what to do if something required is absent.

Example:

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If an essential source is unavailable, ask for an export or prepare a clearly marked incomplete draft.
```

For people-related information, state that the skill should use only information necessary for the authorized purpose and should omit unrelated personal or sensitive details.

## Workflow

Describe the normal sequence of work and meaningful decision points:

1. Inspect the request, inputs, and authorized sources.
2. Clarify only ambiguities that would materially change the result.
3. Gather evidence from approved sources.
4. Perform the requested work using an appropriate method.
5. Check the result against requested format, constraints, and success criteria.
6. Present the result with assumptions, evidence, and unresolved limitations.

Use conditional rules where they genuinely help:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested change could overwrite important work or cause an external effect, explain the impact and request confirmation before proceeding.
```

## Output format

When consistency matters, define a clear template:

```markdown
# [Title]

## Summary
[Brief conclusion]

## Findings
- [Finding and supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or needed follow-up]
```

Do not impose rigid formatting when adaptation is more valuable. For flexible tasks, provide goals, ordering preferences, and a small generalized example instead.

## Quality, safety, and privacy checks

State the checks required before completion. Depending on the task, this may include validating calculations, checking required fields, preserving original data, citing key sources, distinguishing verified facts from assumptions, or flagging uncertainty.

Skills should act in ways a user would reasonably expect from their description. Do not conceal actions, bypass authorization, extract confidential material, damage systems, or support unauthorized access. Pause for confirmation before irreversible, external, or high-impact actions unless the user has clearly authorized them.

## Failure behavior

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable source or capability:** Explain what cannot be verified and offer a safe alternate method.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, report the issue, or request guidance.
- **Permission-sensitive work:** Confirm authority before accessing, sharing, changing, or publishing information.

## Examples

Include only a few short generalized examples, and only where they teach a distinct pattern. Examples should demonstrate reasoning and output shape, not substitute for the workflow.

## 5. Write a useful activation description

The description is a routing instruction. It should say both what the skill does and when it applies. Include realistic language users may use even when they do not name the skill directly.

A strong description includes:

- The task or intended outcome.
- Common contexts that indicate the task.
- Scope limits needed to avoid costly or unsafe false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user requests a progress update, leadership summary, milestone review, risk overview, or concise account of next steps, even if they do not say “status report.”
```

Do not put the full procedure in the description. Avoid vague labels such as “help with documents,” and avoid making the description so broad that it captures adjacent work better handled by another skill.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and appropriately bounded?
- Does the description clearly identify when to use it?
- Are inputs, permissions, outputs, and completion criteria clear?
- Does the workflow explain why key checks matter?
- Does it explain what to do when information is incomplete?
- Is it free of private conventions, assumed access, or undeclared tools?
- Are instructions lean enough to support normal variation?
- Does it protect confidential and personal information appropriately?

Excessive absolute wording is a warning sign unless the rule expresses a true safety, legal, or authorization boundary. Prefer intent-based instructions that help the AI make sound decisions in new situations.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic test prompts. Share them with the user and ask whether they represent real usage or need adjustment.

For every test case, record:

- A descriptive identifier.
- The user prompt.
- Any files or supporting context.
- The expected outcome in plain language.
- Objective checks, if suitable.

Example portable format:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates. Clearly flag information that cannot be verified.",
      "expected_output": "A structured summary separating supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover different meaningful situations:

- A typical successful request.
- Incomplete, conflicting, or ambiguous input.
- A format-sensitive or policy-sensitive request.
- A realistic edge case that changes the workflow.
- A request requiring approval, careful handling of information, or refusal, when relevant.

Vary wording, detail level, and user style. Do not simply repeat the skill's language in tests. Avoid including private personal scenarios or sensitive records unless the testing is authorized and uses only the minimum necessary information.

## 8. Run comparisons and preserve evidence

When independent runs are available, compare the skill against a meaningful baseline:

- **New skill:** Run each test with the skill and without it.
- **Existing skill:** Save an unchanged copy before editing, then compare the revised version against that prior version or another explicitly chosen baseline.

Run conditions should be comparable. When possible, launch skill and baseline runs at the same time for all test cases. Preserve the prompt, supplied inputs, resulting outputs, and available run metadata such as duration and resource use. Record timing when it is reported because some environments do not retain it afterward.

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

If independent comparison is unavailable, perform a transparent sanity check: execute the skill on each test prompt, preserve outputs, and ask the user to review them. Do not describe this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs are in progress, draft objective checks where they add real value. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and tied to user value. Examples include:

- Required sections are present.
- A generated file opens and contains required fields.
- Calculations match a known source within an agreed tolerance.
- The response identifies missing mandatory information.
- Required citations or source references are included.

Record each check with descriptive text, a pass/fail result, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when essential source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests it before finalization."
    }
  ]
}
```

Use programmatic checks when practical. They are more repeatable than visual inspection and can be reused across iterations. Do not force quantitative checks onto subjective work: writing quality, aesthetics, tone, strategic judgment, and practical usefulness often need informed human review.

## 10. Review results with a human

Present qualitative outputs and quantitative evidence together. Use an available review interface when possible; otherwise present outputs clearly in the conversation or as accessible files.

For each test case, show:

- The original prompt and relevant supplied inputs.
- The skill output and comparison output, if available.
- Objective grades and supporting evidence.
- Timing or resource data, if available.
- A clear way for the user to provide feedback.

Ask useful review questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, too slow, or hard to use?
- Did the skill add work that did not improve the outcome?
- Would this work for similar requests with different wording or data?

Empty feedback can mean a test case is acceptable, but it is not proof that every important case is solved. Consider outputs and measurements as well.

## 11. Analyze beyond pass rates

When possible, aggregate pass rate, time, resource use, and variability. Present the revised skill before its comparison condition for easy reading. Then look for patterns that summary numbers can hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill's value.
- **High variance:** Similar runs differ significantly, suggesting unclear instructions or environmental instability.
- **Tradeoffs:** Quality may improve while time or resource use becomes disproportionate.
- **Failure concentration:** Several failures may trace to one cause, such as unclear source selection or missing output rules.
- **Unproductive work:** Execution traces may reveal redundant planning, research, or formatting.
- **Repeated reconstruction:** Multiple runs independently recreate the same helper process, suggesting a script, template, or reference would help.

A small benchmark is evidence for the next revision, not conclusive proof of quality.

## 12. Improve without overfitting

Base revisions on user feedback, outputs, traces, and evaluation results. Change the smallest part of the skill likely to address the underlying cause.

Generalize from a complaint. If one output fails to identify an uncertain source, do not merely mention that exact test. Clarify the broader behavior: distinguish verified information from assumptions whenever source evidence is incomplete or mixed.

Use these principles:

1. **Fix causes, not examples.** Design for future requests, not only the current test set.
2. **Keep instructions lean.** Remove guidance that does not affect useful behavior or causes wasted effort.
3. **Explain intent.** Tie instructions to quality, safety, usability, or authorization.
4. **Add reusable assets only when justified.** Bundle helpers when repeated work demonstrates value.
5. **Preserve successful behavior.** Do not discard what users value while correcting a separate weakness.
6. **Expand coverage gradually.** Add a test for a genuine class of failure, not every isolated incident.

After revision, run the full relevant test set in a new iteration. Retest against the same baseline policy, show prior outputs where useful, collect feedback, and repeat.

Stop when the user says the skill is ready, feedback is consistently positive on meaningful cases, objective requirements are reliably met, or further changes no longer create meaningful improvement. If remaining problems require missing information, unavailable capabilities, or a product decision, state that clearly instead of continuing to edit instructions.

## 13. Optional blind comparison

For a more rigorous comparison of two versions, provide an independent evaluator with two outputs without identifying which version produced each one. Give the evaluator a shared rubric and reveal the mapping only after it records its judgment.

Blind comparison is useful when versions have similar formal scores but differ in qualitative quality, when a decision is important, or when recency bias may affect review. Base the rubric on user value: correctness, completeness, clarity, adherence to constraints, safety, and practical usability. Analyze why the preferred output won before revising again.

## 14. Optimize activation behavior

Optimize the description only after the skill itself is stable. Create a realistic set of requests that should activate the skill and difficult near-misses that should not.

Positive cases should vary across:

- Formal and casual phrasing.
- Direct requests and requests that imply the job.
- Common and less common valid situations.
- Situations where another related skill might compete.

Negative cases should be genuinely close. They should share terms or context with the skill but require another job, a different capability, or lack conditions that make this skill appropriate.

Example format:

```json
[
  {
    "query": "I need a concise leadership update from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain why teams use progress reports without preparing one for my project?",
    "should_trigger": false
  }
]
```

Review the query set with the user before evaluating descriptions. If the environment supports repeated activation testing, separate examples used to improve the description from held-out examples used to choose it. Select the description that performs best on held-out cases, not merely the one that fits the drafting examples.

Use substantive requests: an AI may solve a simple one-step request directly without consulting a specialized skill, even when the description matches. Ensure the final description remains honest about scope.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Audit the package before delivery:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on private conventions, personal access, or undeclared capabilities.
- Scripts, references, and assets are present, clearly named, and documented.
- No confidential data, credentials, identifiers, or unnecessary personal information remain.
- The user can install, access, or adapt the skill in their chosen environment.
- Test material is retained only when safe and useful.

Provide a short handoff note covering what the skill does, required capabilities, known limitations, authorization boundaries, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an honest activation description, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for real recurring work.

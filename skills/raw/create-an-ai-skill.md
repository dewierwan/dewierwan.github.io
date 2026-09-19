---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, validating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, improve an existing one, evaluate whether it helps, or refine when it activates. A skill is a focused set of instructions, with optional resources, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the job, intended outcome, and boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and apply objective checks where they are meaningful.
5. Improve the skill using evidence rather than guesswork.
6. Repeat until the result is useful, reliable, and not narrowly fitted to a few examples.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the finished skill.

Do not force every project through every stage. Some users want a quick collaborative draft; others need a rigorous comparison. First determine where the user is in the loop, then help them make the next useful decision.

## Communication principles

Match the user’s technical vocabulary. Use plain English by default. Terms such as *evaluation* and *benchmark* are often useful, but explain them briefly if needed. Do not assume the user understands terms such as JSON, assertion, schema, or command line.

Explain why a question matters. For example, ask:

> What should a successful result look like: an answer in chat, a structured report, a downloadable file, or an approved external action? This determines how the skill should work and how it can be tested.

Keep the user involved at meaningful decision points:

- Confirm the intended job before writing extensive instructions.
- Ask before imposing a restrictive scope, required tool, or approval step.
- Share proposed test cases before treating them as the evaluation set.
- Let human review lead for subjective qualities such as usefulness, writing style, visual design, tone, and strategic judgment.

If the workflow will access communications, records, files, or other information about people, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant information, exclude unrelated sensitive details, respect privacy and consent expectations, and keep outputs within the appropriate access boundary.

## 1. Determine the starting point

Identify which situation applies.

### New skill

The user has an idea for recurring work, such as preparing updates, processing files, reviewing code, or generating a standard report. Start with discovery and a first draft.

### Existing skill

The user already has a draft or installed skill and wants it edited, simplified, tested, or improved. Preserve its established name and identity unless the user explicitly requests a change. Read the existing instructions before proposing revisions.

### Workflow demonstrated in conversation

The user may say, “turn what we just did into a skill.” Extract what you can from the conversation first:

- Inputs and source material used.
- Actions, tools, and decision sequence.
- Corrections or preferences the user expressed.
- Input and output formats.
- Quality checks and acceptance criteria.
- Conditions that caused the workflow to change direction.

Summarize the inferred workflow and list important gaps for confirmation. Do not silently convert a one-time workaround into a permanent general rule.

### Evaluation or optimization request

The user may have a finished-looking skill and want to know whether it works. Go directly to test design, evaluation, and revision. Do not rewrite a skill merely because a rewrite is possible.

## 2. Capture intent and scope

Gather enough information to define a coherent job. Adapt these questions to the situation instead of asking them mechanically.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What requests, phrases, or situations should cause the skill to be used?
3. **Inputs:** What information, files, examples, systems, and permissions may it use?
4. **Outputs:** What should it produce, modify, or recommend? Is a format required?
5. **Success:** How will the user know the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask, pause, decline, or hand work back to the user?
7. **Variations:** Which common cases, difficult cases, or exceptions materially change the work?
8. **Dependencies:** Does it need particular capabilities, references, templates, scripts, or approved data sources?
9. **Testing:** Should it be tested with representative requests before release?

Testing is especially valuable when outputs can be objectively checked, the workflow is consequential, the skill will be used repeatedly, or the skill performs multi-step work. A subjective creative skill may benefit more from qualitative review than formal pass/fail checks.

Useful choice questions include:

- Should the skill make a low-risk assumption when information is missing, or stop and ask?
- Should it produce a concise summary, a detailed report, or let the user choose?
- Should it work with any user-provided source, or only approved sources?
- Should it prepare a draft only, or is it allowed to take an external action after confirmation?

### Research before drafting

If appropriate resources are available, review relevant documentation, comparable skills, approved examples, and standards before drafting. Research should reduce burden on the user, not override the user’s requirements.

Use it to identify:

- Existing conventions and required output standards.
- Constraints of a file format, interface, or available capability.
- Reusable patterns from comparable work.
- Safety, privacy, regulatory, or approval requirements.

If sources conflict or important requirements remain uncertain, state the uncertainty rather than guessing.

## 3. Choose the skill structure

Keep a skill focused enough that users and AI systems can predict what it does. One skill may support closely related variants, but separate unrelated jobs when they have different audiences, permissions, sources of truth, or definitions of completion.

A portable package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional repeatable helpers
├── references/              # Optional detailed guidance
├── assets/                  # Optional templates or resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description used to decide whether the skill applies.
2. **Core instructions:** The workflow needed for ordinary use.
3. **Supporting resources:** References, templates, and scripts consulted only when relevant.

Keep the core instructions readable. If they become long, move detailed domain-specific material into clearly named reference files and state when each file should be read. Give large references a contents section or other clear navigation.

For a skill with variants, provide one selection workflow and separate references for each variant. The AI should read the relevant material, not load every possible variation by default.

### Use scripts only for justified repeatable work

Consider a helper script when test runs show repeated reconstruction of the same deterministic procedure, such as file conversion, validation, calculations, data cleanup, or document generation.

A bundled helper is valuable when it is:

- More reliable or easier to verify than repeated natural-language steps.
- Reused across multiple requests.
- Safer or less error-prone than recreating the process each time.
- Clearly within the user’s permission and intended scope.

Document what the helper does, its inputs, outputs, limitations, and when not to use it. Do not add automation merely because it is technically possible.

## 4. Write the skill

Write in clear imperative language. Explain the reason behind important instructions, especially when a rule prevents a predictable failure. An AI is more likely to adapt well when it understands the goal and tradeoff than when it receives a long list of unexplained prohibitions.

Include the following sections when they apply.

### Purpose and scope

State the job, intended outcome, and boundaries. Clarify whether the skill creates a response, produces a file, changes data, takes an external action, or guides the user through a process.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State how to proceed if a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask the user for an export or prepare a draft clearly marked as incomplete.
```

For private or personal information, include the authorization boundary. For example, instruct the AI to use only approved records relevant to the stated purpose and to omit unrelated personal details.

### Workflow

Give the normal sequence of actions and include decision points rather than attempting to list every possible edge case.

A durable workflow commonly follows this order:

1. Inspect the request and available inputs.
2. Identify missing information that would materially change the result.
3. Confirm requirements or make low-risk assumptions where appropriate.
4. Gather evidence from approved sources only.
5. Perform the requested work using the appropriate method.
6. Check the result against the requested format and success criteria.
7. Present the result, assumptions, sources, and unresolved limitations.

Use conditional rules where needed:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite important work or affect an outside system, describe the impact and ask for confirmation before proceeding.
```

### Output format

When consistency matters, define a template:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding and supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing input]
```

Do not impose a rigid format when usefulness depends on adapting to context. In that case, define the outcome and quality goals, with a short example if it teaches a distinct pattern.

### Quality and safety checks

State checks needed before completion. Relevant checks may include confirming required fields, validating calculations, citing support for important claims, preserving original data, distinguishing evidence from assumptions, and flagging uncertainty.

The skill’s behavior should match what a user would reasonably expect from its description. Do not conceal actions, bypass authorization, collect unnecessary private information, enable unauthorized access, or create deceptive outputs. For external, irreversible, high-impact, or permission-sensitive actions, obtain confirmation at the appropriate point.

### Failure behavior

Describe recovery rules in general terms:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable source or capability:** Explain what cannot be verified and offer a safe alternative.
- **Ambiguous request:** Make a reasonable low-risk assumption only if it does not materially change the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, disclose the issue, or request guidance.
- **Access or privacy boundary:** Stop using the source and ask for authorization, a narrower scope, or a user-provided extract.

## 5. Write the description for activation

The skill description is a routing instruction. It should state both what the skill does and when it should be used.

Cover realistic language users might use, including requests that imply the job without naming it directly. Be specific enough to reduce missed activations, but not so broad that the skill captures unrelated work.

A good description includes:

- The task or outcome.
- Common user contexts that indicate the task.
- Important scope limits where they prevent costly or unsafe false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a progress update, leadership summary, milestone review, risk summary, or a concise account of next steps, even if they do not use the phrase “status report.”
```

Put activation guidance in the description, not hidden in the body. Do not put the entire procedure in the description or use vague labels such as “help with documents.”

## 6. Review the draft before testing

Read the skill again as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description clearly state when to activate?
- Are required inputs, permissions, and outputs clear?
- Does the workflow explain why important checks exist?
- Does it handle missing information and unavailable resources?
- Are there unnecessary rules, repetitions, or brittle wording?
- Does it avoid assuming one person’s habits, local systems, private access, or terminology?
- Would a capable AI have enough discretion to handle normal variation?

Prefer lean instructions over a long list of rules that do not affect outcomes. Frequent capitalized absolutes are a warning sign unless the behavior is a true safety, authorization, or data-integrity boundary.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Show them to the user and ask whether they reflect real use.

For each case, record:

- A descriptive identifier.
- The prompt.
- Supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates and flag information that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningfully different situations:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic variation that changes the workflow.
- A request requiring confirmation or a safe refusal, when relevant.

Avoid tests that merely repeat the skill’s wording. Vary phrasing, detail level, and user sophistication. Test general classes of difficulty, not personal incidents.

## 8. Run comparisons and preserve evidence

When independent runs are available, compare the skill with a meaningful baseline.

- **New skill:** Run each test with the skill and without it.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revised skill with the earlier version.

Run comparison conditions under comparable circumstances. If parallel execution is available, start both conditions for each test at the same time. Preserve the prompt, supplied files, outputs, and available timing or resource information.

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

For each test, save metadata in a portable form:

```json
{
  "eval_id": "typical-request",
  "eval_name": "typical-request",
  "prompt": "[Test prompt]",
  "assertions": []
}
```

Record timing or resource-use data immediately when the execution environment reports it, because some environments do not retain it afterward.

If independent runs are not available, perform a transparent sanity check: follow the skill for each prompt, save the results, and ask the user to review them. Do not present this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs are underway, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are observable and meaningful:

- Required sections are present.
- A produced file opens and contains required fields.
- Calculations match known values within an agreed tolerance.
- The output identifies missing mandatory input.
- Important claims have required source references.

Record each grade with a clear statement, pass/fail result, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable inputs and requests them."
    }
  ]
}
```

Use automated checks where practical. They are faster, more consistent, and reusable across iterations. Do not force numerical checks onto writing quality, aesthetics, strategic value, or other qualities that need human judgment.

## 10. Review, analyze, and improve

Present outputs and measurements in a review format the user can inspect. If a review interface is available, use it to show each prompt, output, comparison output, formal grades, timing data, and a place for comments. If not, present accessible files or a clear conversational review.

Ask focused questions:

- Which output would you trust in normal use, and why?
- What was missing, misleading, or hard to use?
- Did the skill add work or detail without enough value?
- Would this work for similar requests with different data or wording?

Then look beyond overall pass rates. Identify:

- Checks that pass for every condition and do not distinguish value.
- High-variance results that suggest ambiguity or instability.
- Quality gains that cost disproportionate time or resources.
- Failures with a shared root cause.
- Repeated planning, research, formatting, or helper creation that does not improve outcomes.

Revise based on underlying causes, not individual test wording. Explain the reason for new guidance. Remove instructions that do not earn their complexity. Add a reusable script, template, or reference only when repeated evidence shows it is valuable.

After revision, rerun the full test set in a new iteration, compare it with the chosen baseline, and show prior outputs when useful. Continue until the user is satisfied, feedback is consistently positive across meaningful cases, objective requirements are reliably met, or further changes no longer produce meaningful improvement.

## 11. Optional blind comparison

For a stronger comparison between two versions, give outputs to an independent reviewer without revealing which version produced which result. Ask the reviewer to judge against a shared rubric such as correctness, completeness, clarity, adherence to constraints, safety, and practical usability.

Use blind comparison when versions have similar measurements but differ in qualitative quality, when a decision has material importance, or when reviewer bias is a concern. Analyze why one output was preferred before revising again.

## 12. Optimize activation after the skill works

Only optimize the description after the workflow itself is useful.

Create a realistic set of activation queries with both cases that should activate the skill and difficult near-misses that should not. Include varied wording, formal and casual requests, direct and implied needs, common cases, less common valid cases, and adjacent tasks that belong elsewhere.

Review the set with the user before using it. Keep separate examples for improving the description and for selecting among candidate descriptions. If repeated evaluation is available, run each candidate more than once and select based on held-out cases rather than only the examples used to edit it.

Remember that an AI may not consult a specialized skill for a trivial one-step request even if the description matches. Test with substantive requests where the skill would provide real value.

## 13. Package and hand off

Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on undeclared private access, personal conventions, or a specific product.
- Scripts and references are present, clearly named, and documented.
- No credentials, confidential records, private identifiers, or sensitive examples are included.
- The user can install or adapt the package in their chosen environment.
- Test material is included only when it is safe and useful to retain.

Provide a short handoff note explaining what the skill does, required capabilities, known limitations, and how to perform a basic post-installation test.

## Final readiness gate

A skill is ready when it has a clear job, an accurate activation description, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.

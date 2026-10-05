---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, validating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing skill, assess whether a skill helps, or improve when it activates. A skill is a focused set of instructions, with optional scripts, references, and templates, that helps an AI perform a recurring job consistently.

The core cycle is:

1. Understand the intended job and its boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with a person and, where suitable, measure objective requirements.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and not narrowly fitted to the tests.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the completed skill.

Do not force every project through every stage. Some users want a quick collaborative draft; others need repeatable tests and comparisons. Identify where the user is in the process, state the recommended next step, and adapt the level of rigor to the task’s importance and repeat use.

## Communication principles

Match the user’s technical knowledge. Use plain English by default. Words such as *evaluation* and *benchmark* are usually acceptable if briefly explained. Avoid unexplained technical terms such as “schema,” “assertion,” or “JSON” unless the user is clearly comfortable with them.

Explain why questions matter. For example:

> What should a successful result look like: a chat response, a structured report, a file, or an approved external action? The answer determines both the instructions and how completion can be tested.

Keep the user involved at meaningful decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before choosing a narrow scope, a required tool, or an approval rule.
- Share proposed test cases before treating them as the evaluation set.
- Let human review lead for subjective qualities such as writing, visual design, tone, usefulness, and judgment.
- Do not imply that a weak or unavailable test is proof of quality.

If the skill uses communications, records, files, or information about people, require a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Omit unrelated personal or sensitive details, respect consent and privacy expectations, and keep outputs within the appropriate access boundary.

## 1. Determine the starting point

First establish which situation applies.

### A. New skill

The user has an idea, such as a recurring report, document workflow, analysis task, or support process. Start with discovery and create a first draft.

### B. Existing skill

The user already has instructions and wants them edited, simplified, tested, or improved. Read the current material before proposing changes. Preserve the established name and identity unless the user asks to change them. If the installed copy cannot be edited safely, make a writable working copy and preserve the original unchanged.

### C. A workflow demonstrated in conversation

A user may say, “Turn what we just did into a skill.” First extract what can be learned from the conversation:

- Inputs and source materials used.
- The sequence of actions and decisions.
- Tools or capabilities used.
- Corrections and preferences the user supplied.
- Output formats and acceptance criteria.
- Points where the process branched because conditions changed.

Summarize the inferred workflow and list gaps for confirmation. Do not silently convert a one-time workaround, private habit, or personal access pattern into a general rule.

### D. Evaluation or triggering request

The user may have a finished-looking skill and ask whether it works, whether a revision is better, or whether it activates appropriately. Start with test design and evidence gathering. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough detail to define a coherent job. Ask only the questions that are still unanswered and materially affect the design.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What requests, phrases, or contexts should cause the AI to use it?
3. **Inputs:** What information, files, examples, systems, or authorized permissions may it use?
4. **Outputs:** What should it produce or change? Is a particular format required?
5. **Success:** How will the user know the result is correct, useful, or complete?
6. **Boundaries:** What should it not do? When should it ask, pause, decline, or hand work back to the user?
7. **Variations:** What common cases, difficult cases, exceptions, or failure conditions matter?
8. **Dependencies:** Does it require a capability, reference source, template, script, or user-provided access?
9. **Testing:** Should it be tested with example requests before release?

Offer useful choices when appropriate:

- “Should the skill make a best effort when information is missing, or stop and ask?”
- “Should it provide a concise result, a detailed report, or let the user choose?”
- “Should it work from any available source, or only sources the user explicitly approves?”
- “Should it prepare a draft only, or may it take an external action after confirmation?”

Recommend test cases when the work is repeated, consequential, objective, file-based, structured, or capable of causing costly errors. For highly subjective work, recommend representative examples and human review rather than pretending there is a complete numerical measure.

### Research before drafting

When available and useful, inspect user-approved documentation, existing skills, templates, standards, and relevant technical guidance. Research should reduce the user’s burden, not replace their authority over requirements.

Use research to find:

- Existing output conventions and quality standards.
- Constraints of relevant file formats or tools.
- Reusable approaches from similar approved workflows.
- Safety, privacy, compliance, or approval requirements.

If evidence conflicts or a requirement is uncertain, identify the uncertainty instead of inventing a rule.

## 3. Choose a maintainable structure

Keep each skill focused enough that a user and an AI can predict what it does. A skill may support related variants of the same task, but separate unrelated jobs when they have different users, permissions, sources of truth, or definitions of completion.

A portable package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed guidance
├── assets/                  # Optional templates and resources
└── evals/                   # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata or registration text:** A short name and description that help route requests.
2. **Core instructions:** The workflow needed in normal use.
3. **Supporting resources:** Details loaded only when relevant.

Keep the core instructions concise enough to be understood as a whole. If they become large, move domain-specific material into clearly named references and state exactly when to consult each one. Give large references a navigation section or table of contents.

For skills with variants, use one shared workflow plus separate variant references. For example, a publishing skill might have distinct references for different output channels. Read only the applicable reference rather than all references by default.

### Add reusable scripts only when justified

If several test runs independently recreate the same helper procedure, consider bundling it as a script. This is especially useful for repeatable conversion, validation, formatting, extraction, or calculation work.

A bundled helper should be:

- Deterministic or easier to verify than a manual procedure.
- Reused enough to justify maintenance.
- Clearly authorized and within the user’s intended scope.
- Documented with inputs, outputs, limitations, and conditions for use.

Do not automate actions that conceal effects, bypass review, exceed authorization, or make irreversible changes without an appropriate confirmation step.

## 4. Write the skill

Draft in clear imperative language. Explain the purpose behind important requirements, especially when a rule prevents a known failure. A capable AI can adapt better when it understands the goal and tradeoff rather than receiving a long list of unexplained commands.

Use these sections as applicable.

### Purpose and scope

State the job, intended audience, normal result, and boundaries. Clarify whether the skill answers in chat, creates a file, changes a system, or guides a person through a process.

### Inputs and prerequisites

List required inputs, approved sources, available capabilities, and optional information. State what to do when a required item is missing.

```markdown
Before preparing the report, confirm the time period and approved source material.
If a required source is unavailable, ask for an export or provide a clearly labeled incomplete draft.
```

### Workflow

Provide the normal sequence of actions and decision points. A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Ask focused questions only when an answer would materially change the work.
3. Gather evidence from approved sources.
4. Perform the task with the appropriate method.
5. Verify the result against the requested format and success criteria.
6. Present the result, assumptions, source limitations, and any unresolved questions.

Use conditional guidance rather than brittle lists of special cases:

```markdown
If the user provides a required template, follow it.
If no template is available, use the default structure below.
If an action could overwrite important work or affect an external audience, describe the impact and request confirmation before proceeding.
```

### Output format

Where consistency matters, define a stable template:

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

Avoid fixed structures when the task depends on adapting to context. In those cases, describe the outcome goals and include a brief example rather than imposing a rigid shell.

### Quality, safety, and privacy checks

Specify checks before completion: required sections, calculation validation, source attribution, preservation of original data, or clear uncertainty labels.

A skill must act in ways a reasonable user would expect from its description. Do not design instructions that mislead people, enable unauthorized access, extract confidential information, evade safeguards, or damage systems. If a requested action lacks authorization or is unsafe, explain the limit and offer a safe alternative when possible.

For work involving personal records or communications, include these checks:

- Confirm legitimate purpose and access authorization.
- Use the minimum relevant information.
- Exclude unrelated sensitive details from outputs.
- Respect consent, confidentiality, retention, and sharing expectations.
- Do not make consequential judgments about people from irrelevant or insufficient information.

### Failure behavior

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or source:** Explain what cannot be verified and offer an alternate path.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, label the limitation, or request guidance.
- **High-impact action:** Pause for confirmation before irreversible, external, or consequential changes.

## 5. Write a strong activation description

The short description is primarily routing guidance. It should say both what the skill does and when it is relevant. Include realistic ways users might imply the task without naming the skill.

A useful pattern is:

> Create clear project status reports from approved updates and source material. Use for requests involving progress summaries, milestone reviews, risks, next steps, or leadership updates, even when the user does not say “status report.”

Make the description broad enough to catch valid variations, but not so broad that it captures adjacent work better handled by another skill. Put detailed procedure in the body, not in the description.

## 6. Review before testing

Read the draft as if encountering it for the first time. Check:

- Is the job coherent and appropriately bounded?
- Does the description explain when to activate it?
- Are required inputs, permissions, outputs, and approval points clear?
- Does the workflow explain important quality and safety checks?
- Does it say what to do when information is missing?
- Are there unnecessary rules, duplicated guidance, or brittle wording?
- Does it avoid private conventions, hidden access assumptions, and personal terminology?
- Does it give the AI enough flexibility for normal variation?

Prefer lean instructions. Repeated capitalized prohibitions are a warning sign unless the instruction protects a genuine safety, privacy, or authorization boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create two or three realistic prompts. Share them with the user before running them, and invite additions or corrections.

For each test case, keep:

- A descriptive name.
- The prompt.
- Supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

A portable record format is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates. Clearly flag information that cannot be verified.",
      "expected_output": "A structured summary separating supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful variation:

- A normal successful request.
- Incomplete or ambiguous input.
- A format-sensitive or rule-sensitive case.
- A realistic condition that changes the workflow.
- A permission, privacy, or approval boundary when relevant.

Do not test only phrases copied from the skill. Vary wording, detail level, and user sophistication. Avoid retaining personal scenarios or confidential examples when generalized cases teach the same lesson.

## 8. Run comparisons and retain evidence

When the environment supports independent execution, compare the skill with a meaningful baseline:

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revision against that version or another explicitly chosen baseline.

Start all comparable runs under similar conditions. If parallel execution is available, launch skill and baseline runs together for each test. Store outputs by iteration and descriptive test name, for example:

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

For every run, retain the prompt, relevant supplied inputs, outputs, and available execution metadata such as time and resource use. Record timing when it is reported because some systems do not preserve it later.

If independent runs are unavailable, perform a transparent sanity check: follow the skill for each prompt, save the outputs, and ask the user to review them. Do not claim this is an unbiased baseline comparison.

## 9. Define and grade objective checks

While tests run, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A file opens and includes required fields.
- Calculations match a known source within an agreed tolerance.
- Missing mandatory inputs are identified.
- Claims include required source references.

Store each grade with a clear statement, pass/fail result, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section lists unavailable data and requests it."
    }
  ]
}
```

Use automated checks when practical. They are more repeatable than visual inspection. Do not force numerical checks onto subjective work; human review is often the right method for tone, usefulness, aesthetics, and strategic quality.

## 10. Review results with a human

Present outputs and measurements through any accessible review method: a review interface, shared files, or a clear conversational comparison. Prefer a standard review capability when one is available rather than creating a custom interface without need.

For each test case, show the prompt, relevant inputs, each output, objective grades with evidence, and timing or resource data if available. Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add work or detail that did not help?
- Would this work for similar requests with different wording or inputs?

Empty feedback can mean the case was acceptable, but it is not proof that all cases are solved. Review outputs and measurements as well.

## 11. Analyze beyond pass rates

Aggregate pass rates, time, resource use, and variation when possible. Then look for patterns that summary numbers hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill’s value.
- **High variance:** Similar runs differ sharply, suggesting unclear instructions or unstable conditions.
- **Tradeoffs:** Quality improves but time or resource use becomes excessive.
- **Failure concentration:** Multiple failures have one root cause.
- **Unproductive work:** Execution traces show redundant planning, research, or formatting.
- **Repeated reconstruction:** Multiple runs rebuild the same helper procedure, suggesting a reusable asset.

Use a small benchmark as evidence for the next revision, not as conclusive proof.

## 12. Improve without overfitting

Revise based on feedback, outputs, and analysis. Change the smallest part likely to address the underlying cause.

If one test omitted source notes, do not add a rule tied only to that exact example. Clarify the general condition: when evidence is incomplete or mixed, distinguish verified content from assumptions and unknowns.

Apply these principles:

1. Fix causes, not examples.
2. Keep instructions lean; remove guidance that does not improve outcomes.
3. Explain intent, especially for quality, safety, or user-experience requirements.
4. Add scripts, templates, or references only when repeated use justifies them.
5. Preserve behaviors users already value.
6. Add tests only for real classes of failure, not every isolated incident.

After revision, run the full evaluation set in a new iteration, using the same baseline policy. Where possible, show prior and current outputs side by side. Continue until the user is satisfied, feedback is consistently positive, objective requirements are reliably met, or further instruction changes no longer produce meaningful improvement.

## 13. Optional blind comparison

For a more rigorous comparison, give two outputs to an independent reviewer without saying which version produced each one. Ask the reviewer to judge with a shared rubric, then reveal the mapping only after the judgment is recorded.

Use blind comparison when versions have similar measured results, qualitative judgment is important, or a decision has material consequences. Tie the rubric to user value: correctness, completeness, clarity, adherence to constraints, safety, and practical usability.

## 14. Optimize activation behavior

After the skill itself is stable, test its routing description. Create a balanced set of realistic queries that should activate the skill and difficult nearby queries that should not.

Positive cases should vary in formality, wording, detail, and whether they name the task directly. Negative cases should be meaningful near-misses: requests sharing keywords or context but requiring another workflow.

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

Review the query set with the user before using it. If the environment supports repeated routing tests, separate examples used to improve the description from held-out examples used to select it. Choose the description that works best on held-out cases, not merely the examples used during editing.

Simple requests may not activate a specialized skill even when the wording matches, because an AI can handle a simple task directly. Make routing tests substantive enough that consulting the skill would provide real value.

## 15. Package and hand off

Package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not rely on undeclared tools, private conventions, or hidden access.
- Scripts and references are present, clearly named, and documented.
- No credentials, confidential data, personal identifiers, or sensitive examples remain.
- The user can install or adapt the package in their chosen environment.
- Retained test material is safe and useful.

Provide a short handoff note covering what the skill does, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, appropriate activation guidance, instructions that handle normal variation, explicit rules for uncertainty and authorization, and evidence from realistic use that it improves results.

Do not mistake a long instruction file for a reliable skill. The goal is a reusable workflow that helps an AI make sound decisions and deliver better results for recurring real-world work.

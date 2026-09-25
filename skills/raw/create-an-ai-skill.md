---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a recurring workflow.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing skill, test whether it helps, and improve it through evidence and user feedback. A skill is a focused set of instructions, optionally supported by scripts, reference material, templates, and tests, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the job, users, boundaries, and permissions.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements where appropriate.
5. Improve the skill based on evidence rather than isolated preferences.
6. Repeat until the skill is useful, reliable, and not merely tailored to a few examples.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the finished skill.

Do not force every project through every stage. Some users want a quick draft or an informal collaborative pass. Others need a careful comparison, measurable requirements, and several test iterations. Identify the user’s current stage and help them take the next useful step.

## Communication principles

Match the user’s technical vocabulary and experience. Use plain language by default. Terms such as *evaluation* and *benchmark* are often useful, but briefly define them if needed. Do not use unexplained technical terms such as “schema,” “assertion,” or “JSON” unless the user is comfortable with them.

Explain why key questions matter. For example:

> What should a successful result look like: a chat response, a structured report, a file, or an approved external action? The answer determines how the skill should work and how to test it.

Keep the user involved in decisions that affect scope, risk, usability, or cost:

- Confirm the intended job before writing extensive instructions.
- Ask before choosing a restrictive scope, required capability, or approval policy.
- Share proposed test cases before relying on them.
- Let human judgment lead for subjective quality, including tone, aesthetics, strategy, and creative usefulness.
- Be transparent when a test is only a sanity check rather than an independent comparison.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea for recurring work, such as preparing status summaries, validating data files, or producing a standard document. Start with discovery, then create a draft.

### B. Existing skill or draft

The user has instructions they want to edit, simplify, test, package, or improve. Read the current skill before proposing changes. Preserve its established name and identity unless the user explicitly asks to change them.

### C. Workflow demonstrated in the conversation

The user may ask to “turn this into a skill.” Extract what is already known from the conversation before asking questions:

- Inputs the user supplied.
- Information sources and capabilities used.
- The order of actions and decisions.
- Corrections or preferences the user gave.
- Output format and acceptance criteria.
- Conditions that caused the workflow to change direction.

Summarize the inferred workflow and clearly list the gaps that need confirmation. Do not silently turn a one-time workaround into a general rule.

### D. Evaluation or optimization request

The user may already have a complete-looking skill and ask whether it works. Go directly to test design, evaluation, and targeted revision. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough information to define a coherent job. Do not ask every question mechanically; begin with the unknowns that most affect the design.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Trigger:** What requests, wording, or contexts should cause the skill to be used?
3. **Inputs:** What information, files, examples, systems, and authorized sources may it use?
4. **Outputs:** What should it produce, change, or recommend? Is there a required format?
5. **Success criteria:** How will the user know the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask a question, pause, decline, or hand work back to the user?
7. **Variations:** What common cases, hard cases, and exceptions materially change the workflow?
8. **Dependencies:** Does it require specific capabilities, tools, reference material, templates, or user-provided access?
9. **Testing:** Should it be tested with example requests before release?

Useful clarifying choices include:

- “When information is missing, should the skill make a clearly marked best effort or stop and ask?”
- “Should the output be brief, detailed, or selectable by the user?”
- “May the skill use any accessible source, or only sources the user has specifically approved?”
- “Which actions require explicit confirmation because they are external, irreversible, or high impact?”

### Privacy, authorization, and source boundaries

If a skill accesses communications, records, files, or other information about people, establish a legitimate purpose and clear authorization before using them. Use only the minimum relevant sources and information. Omit unrelated personal or sensitive details from outputs, respect consent and privacy expectations, and keep results within the intended access boundary.

For example, a skill that summarizes approved case notes should focus on information relevant to the authorized task, avoid unrelated personal details, and state when it cannot verify permission or source completeness.

### Research before drafting

When useful, consult user-approved documentation, existing conventions, comparable skills, templates, or domain guidance. Research should reduce burden on the user, not replace their authority over requirements.

Use research to identify:

- Existing output standards and conventions.
- Constraints imposed by tools, data formats, or governing policies.
- Reusable patterns for similar tasks.
- Safety, privacy, compliance, and approval requirements.

If sources conflict or a requirement is uncertain, state the uncertainty rather than guessing.

## 3. Choose the skill structure

Keep a skill focused enough that users and the AI can predict what it does. One skill may support closely related variants of the same job, but separate unrelated work when it has different audiences, permissions, sources of truth, or definitions of completion.

A portable skill package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional supporting documentation
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help decide whether the skill applies.
2. **Core instructions:** The workflow needed for typical use.
3. **Supporting resources:** Detailed references, templates, or scripts used only when relevant.

Keep the core instructions readable. If they become long, move domain-specific details into clearly named reference files and state exactly when to read each one. Large reference files should include a table of contents or navigation section.

When a skill supports multiple variants, organize references by variant. For example, a deployment skill might contain one shared decision workflow and separate references for different hosting environments. The AI should select the relevant variant instead of loading everything by default.

### Use scripts for repeatable deterministic work

Consider a bundled script when test runs show repeated reconstruction of the same reliable procedure, such as validation, conversion, calculation, formatting, or file generation. A script is justified when it is:

- Deterministic or easier to verify than free-form reasoning.
- Reused across requests.
- Safer or less error-prone than recreating the procedure each time.
- Clearly within the user’s intended authorization boundary.

Document what a script does, its inputs, outputs, limitations, and when not to use it. Do not automate an action merely because automation is possible.

## 4. Write the skill

Write in clear, imperative language. Explain the reason behind important instructions, especially when a rule prevents a predictable failure. AI systems generally work better when they understand the quality or safety goal than when they receive a long collection of unexplained prohibitions.

A useful skill commonly includes the following sections.

### Purpose and scope

State the job, intended users, and boundaries. Clarify whether the skill creates an answer, produces a file, takes an action, or guides the user through a process.

### Inputs and prerequisites

List required information, permitted sources, required capabilities, and optional inputs. State what to do when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or produce a draft clearly marked as incomplete.
```

### Workflow

Give the normal sequence of actions and include decision points rather than trying to list every possible edge case.

A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Clarify only the requirements that materially change the work.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result, assumptions, and unresolved limitations.

Use conditional guidance where needed:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested change could overwrite important work, explain the impact and request confirmation before proceeding.
```

### Output format

When consistency matters, define an exact or near-exact template.

```markdown
# [Title]

## Summary
[One short paragraph]

## Findings
- [Finding with evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing information]
```

Avoid rigid formatting when the task’s value depends on adapting to context. In those cases, describe goals, required content, and a small number of examples rather than imposing a fixed shell.

### Quality and safety checks

State the checks needed before completion. Depending on the task, this may include confirming required fields, validating calculations, checking that a file opens, preserving original data, citing important claims, or flagging uncertainty.

A skill must behave in ways a user would reasonably expect from its description. Do not create instructions that conceal actions, bypass authorization, extract confidential information, damage systems, or facilitate unauthorized access. If a request exceeds authority or is unsafe or deceptive, explain the limitation and offer a safe alternative when possible.

### Failure behavior

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** Explain what could not be verified and offer an alternate method if one exists.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, report the issue, or request guidance.
- **Permission-sensitive action:** Pause for confirmation before an irreversible, external, or high-impact action.

### Examples

Use a small number of generalized examples only when they teach a distinct pattern. Examples should illustrate reasoning or output shape, not become a narrow substitute for reasoning.

## 5. Write a strong skill description

The description is primarily a routing instruction: it helps an AI decide whether the skill applies. State both **what the skill does** and **when it should be used**.

Cover realistic user language, including requests that imply the task without naming it. A system may fail to use a relevant skill unless the description makes relevance clear.

A good description includes:

- The task or outcome.
- Common contexts and user phrasing that indicate the task.
- Important scope limits that prevent harmful or costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use for requests involving leadership summaries, progress updates, milestone reviews, risks, blockers, and next steps, even when the user does not use the phrase “status report.”
```

Do not put the entire procedure in the description. Avoid vague labels such as “help with documents,” and do not make it so broad that it captures nearby tasks better handled by another skill.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description clearly say when to use it?
- Are required inputs, permissions, and outputs clear?
- Does the workflow explain why important checks exist?
- Does it define behavior when information is missing?
- Are there unnecessary rules, repeated guidance, or brittle wording?
- Does it avoid personal habits, undeclared access, or assumptions about a particular environment?
- Would a capable AI have enough freedom to handle normal variation?

Prefer a lean, understandable prompt over a long prompt full of rules that do not change outcomes. Excessive absolute wording is a warning sign unless the behavior is genuinely non-negotiable, such as an authorization or safety boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create a small evaluation set. Begin with two or three realistic prompts that resemble genuine user requests. Share them with the user and invite corrections or additions.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Any input files or supplied context.
- The expected outcome in plain language.
- Objective checks, if suitable.

A portable structure is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and flag anything that cannot be verified.",
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Use cases that cover meaningful variation:

- A typical successful request.
- A request with incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic edge case that changes the workflow.
- A request that should require approval, cautious handling, or refusal when relevant.

Do not make tests merely repeat the skill’s wording. Vary phrasing, detail level, and user sophistication. Avoid retaining personal scenarios or sensitive content; test the general category of challenge instead.

## 8. Run comparisons

When independent runs are available, compare the skill against a meaningful baseline.

- **For a new skill:** Run each test with the skill and without the skill.
- **For an existing skill:** Save an unchanged snapshot before editing, then compare the revised version with the earlier version.

Launch skill and baseline runs under comparable conditions. When parallel execution is available, start both configurations for every test case at the same time. This makes timing comparisons fairer and avoids changing the baseline after observing the skilled result.

Use an iteration structure that keeps artifacts organized:

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

For each run, preserve the prompt, supplied files, output, and available metadata such as elapsed time and resource use. Record timing as soon as the execution environment reports it, because some environments do not retain it later.

If independent or parallel runs are unavailable, perform a transparent sanity check instead: follow the skill on each test prompt, preserve the output, and ask the user to review it. Do not describe this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs are underway, draft objective checks where they genuinely help. Explain the checks to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful. Examples include:

- Required sections are present.
- A produced file opens and contains required fields.
- Calculated values match an approved source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- The output includes source references when required.

Each check should have descriptive text, a pass/fail result, and evidence.

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

Use programmatic checks whenever practical. They are generally more repeatable than visual inspection and can be reused in later iterations.

Do not force numerical checks onto subjective work. Writing quality, visual design, usefulness, tone, and strategic judgment often require human review. A weak metric can cause a skill to optimize for the metric instead of the user’s real goal.

## 10. Review results with a human

Present both the outputs and the measurements. Use any available review interface that lets the user inspect each test case, compare configurations, and leave feedback. If no review interface is available, present the results clearly in conversation or as accessible files.

For each test case, provide:

- The original prompt.
- Relevant supplied inputs.
- The skill output and comparison output, if available.
- Objective grades and supporting evidence.
- Timing or resource data, if available.
- A clear way for the user to say what worked and what should change.

Ask focused questions such as:

- Which result would you trust in normal use, and why?
- Did the skill add work or detail that was not valuable?
- What was missing, misleading, or difficult to use?
- Would this still work if the wording or input data changed?

Empty feedback can suggest a case is acceptable, but it is not proof that the skill works generally. Consider the output, test results, and broader coverage together.

## 11. Analyze results beyond pass rates

Aggregate results where possible: pass rate, average time, average resource use, and variability. Present the revised skill before its comparison condition so the report is easy to read.

Then perform an analyst pass. Aggregate statistics can hide important patterns. Look for:

- **Non-discriminating checks:** Both conditions pass, so the check does not reveal the skill’s value.
- **High variability:** Comparable runs differ substantially, suggesting ambiguity, instability, or unreliable instructions.
- **Tradeoffs:** The skill improves quality but adds excessive time or resource use.
- **Failure concentration:** Several failures share a root cause, such as unclear source selection or missing output rules.
- **Unproductive work:** Execution traces show redundant planning, research, formatting, or tool use.
- **Repeated reconstruction:** Multiple runs independently create the same helper procedure, suggesting a reusable resource may help.

Do not treat a small benchmark as conclusive. Use it as evidence for the next revision.

## 12. Improve without overfitting

Base revisions on user feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from complaints. If one output omitted a source note, do not add a rule that only references that test. Instead, clarify the broader behavior: when evidence is incomplete or mixed, distinguish verified information from assumptions and missing data.

Use these principles:

1. **Fix causes, not examples.** Design for future requests, not just current tests.
2. **Keep instructions lean.** Remove guidance that does not change behavior or causes wasted effort.
3. **Explain intent.** State why a step protects quality, usability, privacy, or safety.
4. **Add reusable resources only when justified.** Bundle scripts, templates, or references when repeated work demonstrates their value.
5. **Preserve useful behavior.** Do not discard parts users already value while solving another problem.
6. **Expand coverage gradually.** Add a test when it represents a real class of failure, not every isolated incident.

After revision, rerun the full test set in a new iteration. Use the same baseline policy unless there is a clear reason to change it. Where possible, show the new outputs alongside earlier outputs and collect feedback again.

Stop when one or more conditions is true:

- The user says the skill is ready.
- Feedback is consistently positive or empty across meaningful cases.
- Objective requirements are reliably met.
- Further revisions are not producing meaningful improvement.
- Remaining weaknesses require missing information, unavailable capabilities, or a product decision rather than better instructions.

## 13. Optional blind comparison

For a more rigorous comparison of two versions, use blind review. Give an independent evaluator two outputs without revealing which version created each. Ask the evaluator to judge against a shared rubric, then reveal the mapping only after the judgment is recorded.

Blind comparison is useful when:

- Two versions have similar measured results but different qualitative quality.
- The user or author may be biased toward a newer version.
- The decision has meaningful cost or impact.

Keep the rubric tied to user value: correctness, completeness, clarity, adherence to constraints, safety, and practical usability. Analyze why the preferred output won before editing again.

## 14. Optimize triggering behavior

After the skill’s workflow is stable, evaluate the description that controls activation. Do this after, not before, the skill itself is useful.

Create a realistic set of trigger queries containing cases that **should trigger** and nearby cases that **should not trigger**. Use roughly balanced coverage and enough detail that consulting a skill would actually help.

Positive cases should vary by:

- Formal and casual phrasing.
- Directly named and implied requests.
- Common and less common valid use cases.
- Situations where a related skill might compete but this skill should apply.

Negative cases should be challenging near-misses, not obviously irrelevant requests. They should share terms or concepts with the skill but belong to another job, require a different capability, or lack the conditions that make this skill appropriate.

```json
[
  {
    "query": "I need a concise leadership update from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what project status reporting is and why teams use it?",
    "should_trigger": false
  }
]
```

Review the query set with the user before using it. Weak trigger tests produce misleading descriptions.

If the environment supports repeated activation tests, separate queries used to improve the description from held-out queries used to select the final version. Choose the description that performs best on held-out cases rather than the one that best fits the examples used during editing.

Remember that simple one-step tasks may not activate a specialized skill even when the description matches; an AI may handle them directly. Trigger tests should therefore describe substantive tasks where consulting the skill would add value.

When applying a final description, show the user the before-and-after wording and the evaluation result. Ensure the final description remains honest about scope.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately describes activation conditions.
- Instructions do not depend on personal conventions, private access, or undeclared capabilities.
- References and scripts are present, clearly named, and documented.
- No credentials, personal records, confidential content, identifiers, or sensitive examples are included.
- The user can understand how to install, access, or adapt the package in their chosen environment.
- Test material is retained only when it is safe and useful to include.

Provide a short handoff note that explains what the skill does, required capabilities, known limitations, and a practical way to test it after installation.

## Final readiness gate

A skill is ready when it has:

- A clear, bounded job.
- A description that routes appropriate requests.
- Instructions that handle normal variation.
- Explicit behavior for uncertainty, authorization, privacy, and high-impact actions.
- Output expectations and quality checks appropriate to the task.
- Evidence from realistic use that it improves outcomes.
- No hidden dependence on private data, personal workflows, or undeclared tools.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for the user’s real recurring work.

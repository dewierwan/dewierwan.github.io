---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing one, assess whether it works, or improve when it activates for the wrong requests. A skill is a focused set of instructions, plus optional resources, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the job, users, boundaries, and authorization requirements.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Review representative outputs with a person and measure objective requirements where appropriate.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and not narrowly fitted to the tests.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the finished skill.

Do not assume every project needs every step. A user may want a quick collaborative draft, a sanity check, or a rigorous benchmark. Determine where they are in the loop and help them make the next useful move.

## Communication principles

Match the user’s technical vocabulary and experience. Use plain language by default. Terms such as *evaluation* and *benchmark* are often understandable, but briefly define them if needed. Avoid unexplained terms such as “schema,” “assertion,” or “JSON” unless the user is comfortable with them.

When asking questions, explain why the answer matters. For example:

> What should a successful result look like: an answer in chat, a structured report, a file, or an external action? This determines how the skill should validate completion.

Keep the user involved at important decisions:

- Confirm intended scope before writing extensive instructions.
- Ask before choosing a restrictive policy, required tool, or approval threshold.
- Share proposed test cases before treating them as representative.
- Let human judgment lead when quality is subjective, such as tone, visual design, or strategic usefulness.
- Clearly state when an evaluation is a lightweight sanity check rather than an independent comparison.

If a skill uses private communications, records, or information about people, require a legitimate purpose and clear authorization. Use only the minimum relevant sources and information, omit unrelated or sensitive details, respect consent and privacy expectations, and keep results within the appropriate access boundary.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea such as “I need a skill that prepares recurring project updates.” Start with discovery and a first draft.

### B. Existing draft or installed skill

The user already has instructions and wants them edited, simplified, tested, or optimized. Preserve the established skill identity unless the user explicitly asks to rename it. Read the current instructions and resources before proposing changes.

If the current location is not writable, make an editable copy in a user-approved working location. Do not overwrite the original until the user approves the revision or has a recovery path.

### C. Workflow demonstrated in the conversation

The user may say, “Turn what we just did into a skill.” Extract what is already known before asking questions:

- Inputs the user supplied.
- Approved tools, sources, and permissions.
- The order of decisions and actions.
- Corrections the user made.
- Observed input and output formats.
- Acceptance criteria and quality checks.
- Conditions that changed the approach.

Summarize the inferred workflow and list gaps for confirmation. Do not silently convert a one-time workaround or personal preference into a general rule.

### D. Evaluation or optimization request

The user may have a finished-looking skill and want to know whether it helps. Go directly to test design, evaluation, and targeted revision. Do not rewrite a skill merely because a rewrite is possible.

## 2. Capture intent and scope

Before drafting, collect enough detail to define a coherent, reusable job. Adapt the following questions to the request rather than asking all of them mechanically.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Trigger:** What user requests, wording, or situations should activate it?
3. **Inputs:** What information, files, examples, systems, or approved sources can it use?
4. **Authorization:** What access is permitted, who owns the information, and what actions need confirmation?
5. **Outputs:** What should it produce or change? Is there a required format?
6. **Success:** How will the user know the result is correct, useful, and complete?
7. **Boundaries:** What should the skill not do? When should it ask, decline, or return work to the user?
8. **Variations:** What common cases, difficult cases, or exceptions materially change the workflow?
9. **Dependencies:** Does the work require capabilities, reference material, templates, scripts, or user-provided access?
10. **Testing:** Should the skill be tested with realistic example requests?

Recommend testing when outputs are objectively checkable, the workflow is consequential, the skill will be used repeatedly, or a revision claims to improve an existing skill. For subjective tasks, recommend representative human review rather than artificial numerical scoring.

Useful choice questions include:

- “Should the skill make a best effort when information is missing, or stop and ask?”
- “Should it produce a concise answer, a detailed report, or let the user choose?”
- “May it use any connected source, or only sources the user explicitly approves?”
- “Which actions are safe to perform automatically, and which require confirmation?”

### Research before drafting

If relevant documentation, similar skills, user-approved references, or domain standards are available, review them before drafting. Research should reduce burden on the user, not replace their authority over requirements.

Use research to identify:

- Existing conventions and output standards.
- Constraints of an available tool, system, or file format.
- Reusable patterns from comparable tasks.
- Safety, privacy, compliance, or approval requirements.

If sources conflict or requirements remain uncertain, identify the uncertainty instead of guessing. Do not access private systems or personal records merely because they are technically available; confirm that the purpose and authorization are appropriate first.

## 3. Choose the skill structure

A skill should be focused enough that users and the AI can predict what it does. One skill may support variants of the same job, but separate unrelated jobs when they have different audiences, permissions, sources of truth, or definitions of completion.

A typical package can contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional material read when needed
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help decide whether to activate the skill.
2. **Core instructions:** The workflow needed for most requests.
3. **Supporting resources:** Detailed references, templates, and scripts used only when relevant.

Keep core instructions readable. If they become too long, move specialized material into clearly named references and state exactly when each reference should be used. Large reference files should include a table of contents or other navigation.

Organize skills with multiple variants by variant. For example, a deployment skill might include one core selection workflow and separate guidance for each supported environment. The AI should select and read the relevant material rather than load everything by default.

### Use scripts for repeatable, deterministic work

If test runs show the AI repeatedly reconstructing the same helper procedure—such as file validation, data conversion, report assembly, or calculation checking—consider bundling a reusable script.

A script is valuable when it is:

- Deterministic or easier to verify than free-form reasoning.
- Reused across multiple requests.
- Safer or less error-prone than rebuilding the procedure.
- Clearly within the user’s intended authorization scope.

Document what each script does, its inputs, expected outputs, limitations, and when not to use it. Do not add automation solely because it is possible. Never bundle code intended to conceal actions, bypass access controls, exfiltrate data, or compromise systems.

## 4. Write the skill

Draft the skill in clear, imperative language. Explain the reason behind important instructions, especially when a rule prevents a predictable failure. A capable AI can adapt better when it understands the goal and tradeoff than when it receives a long list of unexplained prohibitions.

Use the following sections where they apply.

### Purpose and scope

State the job, intended users, and boundaries. Make clear whether the skill produces an answer, creates a file, changes a system, or guides a person through a process.

### Inputs and prerequisites

List required information, permitted sources, required capabilities, and optional inputs. State what to do when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If the source is unavailable, ask the user for an export or provide a draft clearly marked as incomplete.
```

When people’s information is involved, specify the legitimate purpose, allowed audience, and handling expectations. The skill should include only information needed for the task and should avoid repeating sensitive details in outputs unless necessary and authorized.

### Workflow

Give the normal action sequence and include meaningful decision points rather than trying to enumerate every possible scenario.

A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Confirm unclear requirements only when the answer materially changes the work.
3. Gather evidence from approved, relevant sources.
4. Perform the task using an appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limitations.

Use conditional rules where needed:

```markdown
If the request includes a required template, follow it.
If no template is provided, use the default report structure below.
If a requested change could overwrite important work or affect an external system, describe the impact and ask for confirmation before proceeding.
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

Avoid rigid formatting when the task’s value depends on adapting to context. In that case, define goals and give examples instead of prescribing a fixed shell.

### Quality and safety checks

State checks needed before completion. Examples include confirming required fields, validating calculations, preserving original data, citing key evidence, flagging uncertainty, and confirming authorization for consequential actions.

Skills should behave in ways users reasonably expect from their description. Do not create misleading skills or instructions that hide actions, bypass authorization, extract confidential information, damage systems, or facilitate unauthorized access. If a request is unsafe, deceptive, or outside the available authority, explain the limitation and offer a safe alternative where possible.

### Failure behavior

Describe recovery behavior in general terms:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** Explain what could not be verified and offer an alternate method.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, report the issue, or request guidance.
- **Permission-sensitive action:** Pause for confirmation before an irreversible, external, or high-impact action.
- **Sensitive information:** Minimize collection and disclosure, exclude unrelated personal details, and ask for direction if the allowed audience is unclear.

### Examples

Include a small number of generalized examples only when each teaches a distinct pattern. Examples should illustrate the shape of a good response, not replace reasoning or encode private circumstances.

## 5. Write a strong description

The skill description is primarily a routing instruction: it helps an AI decide whether the skill applies to a user request. It should state both **what the skill does** and **when to use it**.

Write descriptions that cover realistic user language, including requests that imply the job without naming it. AI systems may fail to activate a useful skill unless relevance is explicit.

A good description includes:

- The task or outcome.
- Common contexts or phrasing that indicate the task.
- Important limits that prevent harmful or costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use for requests involving progress updates, leadership summaries, milestone reviews, risks, decisions, or next steps, including requests that imply a status report without naming one.
```

Do not put the entire procedure in the description. Do not rely on vague labels such as “help with documents.” Do not make the description so broad that it captures nearby work better handled by another skill.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description explain when to activate the skill?
- Are required inputs, permissions, and outputs clear?
- Does the workflow explain why key checks exist?
- Does it tell the AI what to do when information is missing?
- Are there unnecessary rules, repeated guidance, or brittle wording?
- Does it avoid assuming a specific person’s tools, habits, access, or terminology?
- Does it protect privacy and keep outputs within the permitted audience?
- Would a capable AI retain enough freedom to handle normal variation?

Prefer a lean, understandable prompt over one filled with rules that do not affect outcomes. Excessive absolute language is a warning sign unless the behavior is genuinely non-negotiable, such as an authorization or safety boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create a small evaluation set. Start with two or three realistic prompts resembling genuine user requests. Share them with the user and invite additions or corrections before relying on them.

For each test case, record:

- A descriptive identifier or name.
- The user prompt.
- Supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

A portable structure is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached approved updates. Flag information you cannot verify.",
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Use cases that cover meaningfully different situations:

- A typical successful request.
- A request with incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic case that changes the workflow.
- A request that should require approval, safe refusal, or privacy-aware handling, when relevant.

Do not write tests that merely repeat the skill’s language. Vary phrasing, detail level, and user sophistication. Use generalized, authorized test data; do not include real confidential details merely to make a test feel realistic.

## 8. Run comparisons

When the environment supports independent runs, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revised version with the previous version.

Run each configuration under comparable conditions. If parallel execution is available, start skill and comparison runs for all test cases together. This reduces timing differences and avoids selectively changing the baseline later.

Store outputs in a clear iteration structure:

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

For each run, preserve the prompt, approved input files, output, and available metadata such as elapsed time and token or compute use. Record timing when the execution environment reports it, because some systems do not preserve it afterward.

If independent agents or parallel execution are unavailable, perform a transparent sanity check instead: follow the skill for each test prompt, save the results, and ask the user to review them. Do not describe this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs are underway, draft objective checks where they genuinely help. Explain the checks to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A produced file opens and includes required fields.
- Calculated values match a known source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- Output includes citations or source references when required.

Each check should have a descriptive statement, a pass/fail result, and evidence:

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

Use scripts for programmatic checks whenever practical. Automated checks are faster, more repeatable, and reusable across iterations.

Do not force numerical checks onto subjective tasks. Writing quality, usefulness, tone, aesthetics, and strategic judgment generally need human review. A weak proxy can make the skill optimize for the metric instead of the user’s real goal.

## 10. Review results with a human

Present both outputs and measurements. Use an available review interface that lets the user inspect each test case, compare configurations, and leave feedback. If no such interface exists, present results clearly in conversation or as accessible files.

For each test case, show:

- The original prompt.
- Relevant supplied inputs.
- The skill output and comparison output, if available.
- Objective grades and evidence.
- Timing or resource data, if available.
- A clear place for the user to state what worked and what should change.

Ask focused questions:

- “Which result would you trust in normal use, and why?”
- “Did the skill add steps or detail that were not valuable?”
- “What was missing, misleading, or hard to use?”
- “Would this work for similar requests with different wording or data?”

Empty feedback can indicate that a case is acceptable, but it is not proof that all cases are solved. Consider the outputs and measurements too.

## 11. Analyze results beyond pass rates

Aggregate results where possible: pass rate, average time, average resource use, and variation. Make reports easy to compare by placing the revised-skill result before its baseline counterpart.

Then perform an analyst pass. Aggregate statistics can hide important patterns:

- **Non-discriminating checks:** A check passes with and without the skill, so it does not measure the skill’s added value.
- **High variation:** Comparable runs differ substantially, suggesting ambiguity, environmental instability, or unreliable instructions.
- **Tradeoffs:** The skill improves quality but imposes excessive time or resource costs.
- **Failure concentration:** Several failures share a root cause, such as unclear source selection or missing output rules.
- **Unproductive work:** Execution traces show redundant planning, unnecessary research, or excessive formatting.
- **Repeated reconstruction:** Multiple runs independently create the same helper process, suggesting a bundled resource would help.

Do not treat a small benchmark as conclusive. Use it as evidence for the next revision.

## 12. Improve without overfitting

Base revisions on user feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from a complaint. If one output omitted a source note, do not add a rule tied only to that test. Clarify the broader condition: when evidence comes from incomplete or mixed sources, distinguish verified information from assumptions.

Use these improvement principles:

1. **Fix causes, not examples.** Design for future requests, not just current tests.
2. **Keep instructions lean.** Remove guidance that does not change behavior or causes wasted effort.
3. **Explain intent.** State why an action protects quality, usability, privacy, or safety.
4. **Add reusable assets only when justified.** Bundle scripts, templates, or references when repeated work demonstrates their value.
5. **Preserve useful behavior.** Do not lose parts users already value while fixing another problem.
6. **Expand coverage gradually.** Add a test when it represents a real class of failure, not every isolated incident.

After revision, rerun the full test set in a new iteration. Use the same comparison policy, show new outputs beside prior outputs where possible, and collect feedback again.

Stop when one or more conditions is true:

- The user says the skill is ready.
- Feedback is consistently positive or empty across meaningful cases.
- Objective requirements are reliably met.
- Further revisions are not producing meaningful improvement.
- Remaining weaknesses require unavailable information, missing capabilities, or a user decision rather than better instructions.

## 13. Optional blind comparison

For a more rigorous comparison of two skill versions, use blind review. Give an independent evaluator two outputs without identifying which version produced each. Ask the evaluator to judge them using a shared rubric, then reveal the mapping only after the judgment is recorded.

Blind comparison is useful when:

- Two versions have similar pass rates but differ in qualitative quality.
- The author or reviewer may favor a newer version.
- The decision has material cost or importance.

Keep the rubric tied to user value: correctness, completeness, clarity, adherence to constraints, safety, privacy, and practical usability. Analyze why the preferred output won before revising again.

## 14. Optimize triggering behavior

After the workflow itself is stable, assess the description that controls activation. Do this after—not before—the skill is otherwise useful.

Create a realistic set of trigger queries containing both cases that **should trigger** and nearby cases that **should not trigger**. Use roughly balanced coverage and enough detail that consulting a skill would be useful.

Positive cases should vary in wording and context:

- Formal and casual phrasing.
- Requests that name the task directly and requests that imply it.
- Common use cases and less common valid cases.
- Cases where another related skill might compete but this skill should be selected.

Negative cases should be difficult near-misses, not obviously irrelevant requests. They should share terms or concepts with the skill but belong to another job, require another capability, or lack the conditions that make this skill appropriate.

```json
[
  {
    "query": "I need a concise leadership update from these approved team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what a project status report is and when teams use one?",
    "should_trigger": false
  }
]
```

Review the query set with the user before using it. Poor trigger tests produce misleading descriptions.

If the environment permits repeated activation tests, separate the queries used to improve a description from held-out queries used to choose the final description. Choose the description that performs best on held-out cases, not merely the one that fits the examples used during editing.

A simple one-step request may not activate a specialized skill even when its description matches, because an AI may handle it directly. Trigger tests should therefore use substantive requests for which the skill would provide real benefit.

When applying the chosen description, show the user the before-and-after wording and the evaluation results. Ensure the final description remains honest about the skill’s scope.

## 15. Package and hand off

When the skill is ready, package the core instructions and only resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately represents activation conditions.
- Instructions do not depend on private local conventions, undeclared tools, or personal access.
- References and scripts are present, clearly named, and documented.
- No credentials, confidential data, personal identifiers, private URLs, or sensitive examples are included.
- Test materials are retained only when they are safe and useful.
- The user can understand how to install, access, adapt, and test the skill in their chosen environment.

Provide a short handoff note explaining what the skill does, required capabilities, known limitations, authorization expectations, and how the user can verify it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an accurate description that routes appropriate requests, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for real recurring work.

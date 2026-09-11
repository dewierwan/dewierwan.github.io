---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing one, assess whether it works, or improve when it triggers. A skill is a focused set of instructions, and optionally supporting resources, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the job and its boundaries.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Let a person review representative outputs and measure objective requirements where appropriate.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and not overfitted to the tests.
7. Optionally improve the skill description so it activates for the right requests.

Adapt the process to the user’s goals. A user may want a quick collaborative draft, a lightweight practical review, or a rigorous comparison. First identify where they are in the loop, then help them take the next useful step.

## Communication principles

Match the user’s technical vocabulary and experience. Use plain language by default. Terms such as *evaluation* and *benchmark* can be useful, but explain them briefly when needed. Avoid unexplained technical terms such as “schema,” “assertion,” or “JSON” unless the user appears comfortable with them.

Explain why questions matter. For example:

> What should a successful result look like: an answer in chat, a structured report, a file, or an action? This determines how completion can be checked.

Keep the user involved at important decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before selecting a restrictive scope, required capability, or approval policy.
- Share proposed test cases before relying on them.
- Let human review lead for subjective quality such as writing style, visual design, or strategic usefulness.

If the skill will access communications, records, files, or data about people, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Respect consent, privacy expectations, and the access boundary of the user’s role. Omit unrelated or sensitive personal details from outputs.

## 1. Determine the starting point

Identify which situation applies.

### A. New skill

The user has an idea, such as a recurring reporting, analysis, writing, planning, or file-processing task. Begin with discovery and a first draft.

### B. Existing skill

The user already has instructions and wants them edited, simplified, tested, or optimized. Read the current instructions before proposing changes. Preserve its established identity, including its name, unless the user explicitly requests a rename.

### C. Workflow demonstrated in conversation

The user may ask to turn the current conversation into a skill. Extract what is already known before asking repeated questions:

- Inputs the user supplied.
- Sources, tools, or capabilities used.
- The sequence of actions and decisions.
- Corrections or preferences the user expressed.
- Observed output formats and acceptance criteria.
- Conditions that caused the workflow to change direction.

Summarize the inferred workflow and list gaps for confirmation. Do not silently turn a one-time workaround into a general rule without checking whether it applies broadly.

### D. Evaluation or optimization request

The user may have a finished-looking skill and want to know whether it helps. Move directly to test design, evaluation, and revision. Do not rewrite it merely because a rewrite is possible.

## 2. Capture intent and scope

Before drafting, gather enough detail to define a coherent job. Adapt these questions to the context rather than asking all of them mechanically.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Trigger:** What kinds of user requests, wording, or situations should activate it?
3. **Inputs:** What information, files, examples, systems, or permissions can it use?
4. **Outputs:** What should it produce or change? Is a format required?
5. **Success:** How will the user know the output is correct or useful?
6. **Boundaries:** What should it not do? When should it ask a question, decline, or return work to the user?
7. **Variations:** What common cases, difficult cases, or exceptions matter?
8. **Dependencies:** Does it need particular capabilities, reference material, templates, scripts, or authorized access?
9. **Testing:** Should the skill be tested with representative requests?

Recommend tests when outputs can be checked objectively, the workflow is consequential, or the skill will be used repeatedly. For highly subjective work, propose human review rather than weak numerical proxies.

Offer meaningful choices when useful:

- Should the skill make a best effort when information is missing, or stop and ask?
- Should it produce a concise response, a detailed report, or let the user choose?
- Should it work with any source, or only sources the user has approved?
- Which actions require confirmation because they are external, irreversible, or high impact?

### Research before drafting

If the environment provides relevant documentation, similar skills, user-approved reference material, or domain guidance, review it before drafting. Research should reduce burden on the user, not replace their authority over requirements.

Use it to identify:

- Existing conventions or output standards.
- Constraints from file formats or available capabilities.
- Reusable patterns from comparable tasks.
- Safety, privacy, compliance, and approval requirements.

If sources conflict or a requirement remains uncertain, state the uncertainty rather than guessing.

## 3. Choose the skill structure

A skill should be focused enough that people and AI systems can predict what it does. One skill can support related variants of the same job, but separate unrelated work when it has different users, permissions, source-of-truth rules, or completion criteria.

A typical package may look like this:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed documentation
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help decide whether the skill applies.
2. **Core instructions:** The workflow needed for most uses.
3. **Supporting resources:** Detailed references, templates, and scripts consulted only when relevant.

Keep the core instructions readable. If they become large, move variant-specific detail into clearly named references and state when each reference should be read. Give long references a table of contents or clear navigation.

For multi-variant skills, organize supporting material by variant. For example, a deployment skill may have a core selection workflow and separate reference files for each hosting environment. Read only the relevant reference rather than loading every variant by default.

### Use scripts for repeatable deterministic work

If several test runs independently reconstruct the same helper procedure, such as conversion, validation, report generation, or data cleanup, consider bundling a script. A script is useful when it is:

- Deterministic or easier to verify than natural-language reasoning.
- Reused across requests.
- Safer or less error-prone than recreating the process each time.
- Clearly within the user’s authorized scope.

Document what it does, its inputs and outputs, and when not to use it. Do not add automation merely because it is technically possible.

## 4. Write the skill

Draft in clear, imperative language. Explain the purpose behind important instructions, especially where a step prevents a predictable failure. An AI generally performs better when it understands the quality, safety, or usability goal than when given a long list of unexplained prohibitions.

Include the following sections when applicable.

### Purpose and scope

State the job, intended users, boundaries, and completion definition. Clarify whether the skill creates an answer, produces a file, takes an action, or guides the user through a process.

### Inputs and prerequisites

List required information, permitted sources, necessary capabilities, and optional inputs. State what to do when a required item is unavailable.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a source is unavailable, ask the user for an export or provide a draft clearly marked as incomplete.
```

### Workflow

Give the normal sequence of actions and key decision points. A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Clarify requirements only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result with assumptions and unresolved limitations.

Use conditional rules rather than attempting to list every edge case:

```markdown
If the request provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested change could overwrite important work, describe the impact and request confirmation before proceeding.
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
- [Uncertainty or missing input]
```

Avoid rigid formatting when the value of the task depends on adapting to context. In that case, specify goals and brief examples instead of a fixed shell.

### Quality, safety, and privacy checks

State the checks needed before completion. Examples include confirming required fields, validating calculations, identifying source support for important claims, preserving originals, and flagging uncertainty.

Skills must behave as users would reasonably expect from their description. Do not conceal actions, bypass authorization, extract confidential information, damage systems, or enable unauthorized access.

For people-related information:

- Confirm legitimate purpose and authorization before accessing records or communications.
- Use the minimum necessary sources and details.
- Keep sensitive information out of summaries unless it is necessary, authorized, and appropriate for the audience.
- Avoid unsupported judgments about people.
- For hiring or assessment tasks, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether the assessment distinguishes relevant performance.

### Failure behavior

Describe recovery from common failure classes:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** Explain what cannot be verified and offer an alternative method.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, explain the issue, or request guidance.
- **Permission-sensitive action:** Pause for confirmation before an irreversible, external, or high-impact action.

### Examples

Include only a small number of generalized examples when they teach a distinct pattern. Examples should illustrate reasoning and output shape, not become narrow substitutes for judgment.

## 5. Review the draft before testing

Read the draft as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description say when to activate the skill?
- Are inputs, permissions, and outputs clear?
- Does the workflow explain why important checks exist?
- Does it handle absent or conflicting information?
- Are there unnecessary rules, repeated guidance, or brittle wording?
- Does it avoid assuming personal habits, private access, or a particular technical environment?
- Does it leave a capable AI enough freedom for normal variation?

Prefer lean, understandable instructions over long instruction files full of rules that do not affect outcomes. Excessive absolute language is a warning sign unless the behavior is a real safety, authorization, or integrity boundary.

## 6. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic requests. Share them with the user and invite additions or corrections before treating them as representative.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Any input files or context.
- The expected outcome in plain language.
- Objective checks, if suitable.

A portable structure is:

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

Cover different meaningful situations:

- A typical successful request.
- A request with incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic edge case that changes the workflow.
- A request requiring approval or a safe refusal, where relevant.

Do not merely repeat the skill’s wording. Vary phrasing, detail level, and apparent user experience. Avoid one-off personal scenarios; test the general class of challenge.

## 7. Run comparisons and preserve evidence

When independent runs are available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without it.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revision against the previous version.

Run all conditions under comparable circumstances. If parallel execution is available, start the skill and comparison runs for all test cases together. This reduces timing distortions and keeps the comparison fair.

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

For each run, preserve the prompt, supplied inputs, output, and available run metadata such as duration and token or compute use. Capture timing when it is reported because some environments do not retain it later.

If independent or parallel runs are unavailable, perform a transparent sanity check: follow the skill on each test request, save the outputs, and ask the user to review them. Do not present this as a rigorous baseline comparison.

## 8. Define and grade objective checks

While runs are underway, draft objective checks where they genuinely help. Explain them to the user before using them as success criteria.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A produced file opens and includes required fields.
- Calculations match a known source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- Important claims include appropriate source references.

Record each check with descriptive text, pass/fail status, and evidence:

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

Use programmatic checks when practical. They are usually more repeatable than visual inspection and can be reused across iterations.

Do not force numerical checks onto subjective tasks. Tone, aesthetics, writing quality, usefulness, and strategic judgment often require human review. A weak metric may cause the skill to optimize for the metric rather than the user’s actual goal.

## 9. Review and analyze results

Present both outputs and measurements. Use an available review interface if one exists; otherwise present accessible files or a clear conversational comparison.

For each test, show:

- The original prompt and relevant inputs.
- The skill output and comparison output, if available.
- Objective grades and supporting evidence.
- Timing or resource data, if available.
- A way for the user to say what worked and what should change.

Ask focused questions:

- Which result would you trust in normal use, and why?
- Did the skill add effort or detail that was not valuable?
- What was missing, misleading, or difficult to use?
- Would this work for similar requests with different wording or data?

Aggregate results where possible, including pass rate, average duration, resource use, and variation. Put the revised-skill result before the comparison condition in reports.

Then do an analyst pass. Aggregate statistics can hide important patterns:

- **Non-discriminating checks:** The skill and baseline both pass, so the check does not measure the skill’s value.
- **High variation:** Comparable runs differ substantially, indicating ambiguity or instability.
- **Tradeoffs:** Quality may improve while time or resource use becomes disproportionate.
- **Failure concentration:** Several failures may point to one root cause, such as unclear source selection.
- **Unproductive work:** Execution traces reveal redundant research, planning, or formatting.
- **Repeated reconstruction:** Multiple runs recreate the same helper process, suggesting a reusable resource.

Treat a small benchmark as evidence for the next revision, not proof of universal performance.

## 10. Improve without overfitting

Base revisions on user feedback, outputs, and analysis. Change the smallest part likely to address the underlying cause.

Generalize from complaints. If an output failed to distinguish verified facts from assumptions, do not add a rule tied only to that test. Clarify the broader rule: when evidence is incomplete or mixed, separate supported information from assumptions and unknowns.

Use these principles:

1. **Fix causes, not examples.** Design for future requests, not only the current tests.
2. **Keep instructions lean.** Remove guidance that does not improve behavior or causes wasted work.
3. **Explain intent.** State how an action protects quality, safety, or usability.
4. **Add reusable assets only when justified.** Bundle scripts, templates, or references when repeated work proves their value.
5. **Preserve useful behavior.** Do not lose what users already value while fixing another problem.
6. **Expand coverage gradually.** Add tests for real classes of failure, not every isolated incident.

After revision, rerun the full test set in a new iteration. Retest against the same baseline policy. Show new outputs alongside prior outputs where possible, then gather feedback again.

Stop when:

- The user says the skill is ready.
- Feedback is consistently positive across meaningful cases.
- Objective requirements are reliably met.
- Further changes are not producing meaningful improvement.
- Remaining limitations require missing information, unavailable capabilities, or a product decision rather than better instructions.

## 11. Optional blind comparison

For a more rigorous comparison of two versions, use blind review. Give an independent evaluator two outputs without identifying their origins. Ask it to assess both against a shared rubric, then reveal the mapping only after its judgment is recorded.

Use blind comparison when versions have similar measurements but visibly different quality, when author preference may bias review, or when the decision has material consequences. Keep the rubric tied to user value: correctness, completeness, clarity, constraint adherence, safety, and practical usability.

## 12. Optimize triggering behavior

Once the workflow itself is stable, evaluate the description that controls activation. Do this after the skill is useful, not before.

Create a balanced set of realistic requests that should trigger and nearby requests that should not. Include enough detail that consulting a skill would actually help.

Positive cases should vary in wording and context:

- Formal and casual phrasing.
- Requests that name the task and requests that imply it.
- Common and less common valid uses.
- Cases where a related skill might compete but this one should be chosen.

Negative cases should be difficult near-misses, not irrelevant requests. They should share terms or concepts with the skill but belong to another job, need another capability, or lack the conditions that make this skill appropriate.

```json
[
  {
    "query": "I need a concise leadership update from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what a project status report is and when teams use one?",
    "should_trigger": false
  }
]
```

Review the set with the user before relying on it. Separate queries used to improve the description from held-out queries used to select it. If repeated evaluation is available, choose the description that performs best on held-out cases rather than the one that best fits the editing examples.

A simple one-step request may not activate a specialized skill even when its description matches, because the AI may handle it directly. Therefore, use substantive trigger tests where consulting the skill offers a clear benefit.

Show the user the description before and after optimization, along with results. Keep the final description accurate about the skill’s real scope.

## 13. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states when the skill applies.
- Instructions do not depend on private conventions, personal access, or undeclared capabilities.
- References and scripts are present, clearly named, and documented.
- No credentials, identifiers, confidential information, or sensitive examples are included.
- The user can install or adapt the package in their chosen environment.
- Test material is retained only when safe and useful.

Provide a brief handoff note explaining what the skill does, required capabilities, known limitations, and how to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, a description that routes appropriate requests, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring real-world work.

---
name: create-an-ai-skill
description: Create, improve, test, evaluate, and package a reusable AI skill from a new idea, an existing draft, or a demonstrated workflow, with optional optimization of the description that controls when the skill activates.
---

# Create an AI skill

Use this workflow to design a new reusable AI skill, improve an existing skill, test whether a skill helps, or turn a repeated conversation workflow into portable instructions. A skill is focused guidance, with optional resources, that helps an AI perform a recurring job consistently.

The core cycle is:

1. Define the intended job and its boundaries.
2. Draft or revise the skill.
3. Test it using realistic user requests.
4. Review outputs with a human and measure objective requirements where useful.
5. Improve the instructions based on evidence.
6. Repeat until the result is useful, reliable, and not merely fitted to a few examples.
7. Optionally refine the description that determines when the skill activates.
8. Package and hand off the final skill.

Adapt the rigor to the user’s needs. Some users want a quick collaborative draft; others need comparison runs, formal checks, and multiple revisions. First determine where the user is in the process, then help them take the next useful step.

## Communication principles

Match the user’s familiarity with technical language. Use plain English by default. Terms such as *evaluation* and *benchmark* can be useful, but explain them briefly if needed. Do not use terms such as “JSON,” “assertion,” or “schema” without explanation unless the user has indicated comfort with them.

Explain why key questions matter. For example: “What should a successful result look like: a chat response, a structured report, a file, or a completed action? This determines how we test it.”

Keep the user involved at important decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before introducing restrictive scope limits, tool dependencies, or approval requirements.
- Share proposed test requests before relying on them.
- Let human review lead for subjective qualities such as voice, design, strategy, or usefulness.
- Be flexible when the user asks for a lightweight, exploratory process rather than a formal benchmark.

## 1. Identify the starting point

Classify the request before choosing a workflow.

### A. New skill

The user has an idea for a recurring task. Start with discovery, scope definition, and a draft.

### B. Existing skill or draft

The user already has instructions and wants them simplified, tested, improved, or repackaged. Read the current material first. Preserve the established skill name and identity unless the user explicitly wants a rename.

### C. Workflow demonstrated in the conversation

The user may say, “Turn what we just did into a skill.” First extract what the conversation already establishes:

- Inputs and source material used.
- Actions and tools used.
- Sequence of decisions.
- Corrections and preferences supplied by the user.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow and identify gaps for the user to confirm. Do not silently convert one-time details into general rules.

### D. Evaluation or optimization request

The user may have a finished-looking skill and want evidence about whether it helps. Go directly to test design, comparison, review, and revision. Do not rewrite a skill only because rewriting is possible.

## 2. Capture intent, access boundaries, and scope

Gather enough information to define a coherent job. Do not ask every question mechanically; begin with what most affects the design.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** Which requests, phrases, or contexts should cause the skill to apply?
3. **Inputs:** What information, files, systems, examples, and capabilities may it use?
4. **Authorization:** What access is legitimate for this task?
5. **Outputs:** What should it produce, change, or recommend? Is there a required structure or file format?
6. **Success criteria:** How will the user know the result is correct or useful?
7. **Boundaries:** What should the skill not do? When should it ask a question, stop, decline, or request approval?
8. **Variation:** Which common cases, difficult cases, and meaningful exceptions matter?
9. **Dependencies:** Does it need particular capabilities, templates, scripts, references, or approved data sources?
10. **Testing:** Should it be tested on example requests?

Offer useful choices where appropriate:

- “Should the skill make a low-risk best effort when information is missing, or stop and ask?”
- “Should it default to a concise response, a detailed response, or let the user choose?”
- “Should it use only sources the user explicitly approves, or may it use authorized sources already available in the workspace?”

### Privacy and authorization boundaries

For workflows that access private communications, records, or information about people:

- Require a legitimate purpose and clear authorization before accessing material.
- Use only the minimum relevant sources and information.
- Omit unrelated personal information and sensitive details from outputs.
- Respect consent, confidentiality, and reasonable privacy expectations.
- Keep findings within the appropriate access boundary; do not repurpose them for unrelated audiences or decisions.
- State uncertainty when authorization, source relevance, or data-handling expectations are unclear.

For hiring, assessment, or review workflows, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Do not make claims based on irrelevant personal characteristics or use demeaning language about people.

### Research before drafting

If relevant documentation, comparable skills, approved reference materials, or domain guidance are available, inspect them before drafting. Research should reduce burden on the user, not replace the user’s authority over requirements.

Research may identify:

- Existing conventions and output standards.
- Constraints of available tools or file formats.
- Similar reusable patterns.
- Safety, privacy, compliance, and approval requirements.

If evidence conflicts, present the uncertainty and available choices rather than inventing a rule.

## 3. Choose a skill structure

Keep a skill focused enough that its purpose and limits are predictable. One skill may support closely related variants, but separate unrelated jobs when they have different users, permissions, sources of truth, or definitions of completion.

A typical portable package looks like this:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed documentation
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Routing description:** A short statement of what the skill does and when it applies.
2. **Core instructions:** The workflow needed on most uses.
3. **Supporting resources:** Detailed references, templates, and scripts loaded only when relevant.

Keep core instructions readable. If they become long, move detailed domain variants into clearly named reference files and say exactly when to consult each one. Add a contents list to large references.

For skills serving multiple variants, provide a selection step in the core instructions and separate resources by variant. Load only the applicable material rather than treating every variant as mandatory.

### Bundle repeatable deterministic work

If test runs show repeated reconstruction of the same helper procedure, consider bundling a script or template. This is useful for repeatable validation, file conversion, report assembly, data cleanup, or other work that is easier to verify than free-form reasoning.

Bundle a helper only when it is reusable, authorized, and clearly valuable. Document what it does, its inputs and outputs, required capabilities, when to use it, when not to use it, and its checks or limitations.

Do not add automation merely because it is possible. The skill should never conceal actions, bypass access controls, export data beyond authorization, damage systems, or surprise the user relative to its stated purpose.

## 4. Write the skill

Draft in clear, imperative language. Explain the reason for important instructions, especially where a step protects quality, privacy, safety, or user control. A capable AI can adapt better when it understands the purpose of a rule rather than receiving unexplained rigid commands.

Use the following sections where applicable.

### Purpose and scope

State the job, intended context, and boundaries. Clarify whether the skill produces an answer, creates a file, modifies data, performs an external action, or guides the user through a process.

### Inputs and prerequisites

List required inputs, permitted sources, needed capabilities, and optional information. State what happens when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved data source.
If the source is unavailable, ask the user for an export or provide a draft clearly marked as incomplete.
```

### Workflow

Describe the normal sequence and decision points:

1. Inspect the request and available inputs.
2. Clarify only questions whose answers materially change the work.
3. Gather evidence from approved sources.
4. Complete the task with the appropriate method.
5. Check the result against requested format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limitations.

Use conditional instructions rather than trying to enumerate every edge case:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested action could overwrite important work or affect an external system, explain the impact and request confirmation before proceeding.
```

### Output format

When consistency matters, provide a fixed or near-fixed template:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or needed follow-up]
```

Avoid rigid shells where contextual adaptation is more valuable. In those cases, state goals and show a short representative example instead.

### Quality, safety, and completion checks

Describe checks before delivery. Examples include required fields, calculation validation, source support for key claims, preservation of original data, or flagging uncertainty.

A skill’s behavior should be unsurprising given its description. Do not create misleading, harmful, or unauthorized skills. When a request exceeds authority or creates substantial risk, explain the limit and offer a safe alternative where possible.

### Failure behavior

Specify general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable source or capability:** Explain what cannot be verified and offer an alternative.
- **Ambiguous request:** Make a low-risk assumption when it does not materially affect results; otherwise ask.
- **Validation failure:** Do not present the output as complete; correct it, report the issue, or request guidance.
- **High-impact action:** Pause for confirmation before irreversible, external, or consequential changes.

### Examples

Use a small number of generalized examples only when each teaches a distinct decision pattern. Examples should illustrate reasoning rather than replace it with narrow rules.

## 5. Write the routing description

The skill description controls activation. It should say both **what the skill does** and **when to use it**. Include common user language, including requests that imply the job without naming it directly.

A useful pattern is:

```text
Create clear project status reports from approved updates and source material. Use for requests involving progress summaries, leadership updates, milestone reviews, project risks, blockers, and next steps, even when the user does not use the phrase “status report.”
```

Avoid vague descriptions such as “help with documents.” Do not make the description so broad that it captures adjacent work better handled by another skill. Keep the description honest: it should not imply tools, authority, or outcomes the skill cannot provide.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description clearly state when to activate it?
- Are required inputs, access limits, permissions, and outputs clear?
- Does the workflow explain why important checks matter?
- Does it handle missing information and validation failures?
- Are there unnecessary rules, duplicated guidance, or brittle wording?
- Does it rely on private conventions, personal access, or undeclared tools?
- Does it preserve appropriate privacy boundaries?
- Does it leave a capable AI enough flexibility for normal variation?

Prefer lean instructions over a long list of rules that do not improve outcomes. Repeated emphatic language is a warning sign unless the boundary is genuinely non-negotiable, such as authorization or safety.

## 7. Design realistic test cases

After the draft is stable enough to test, propose two or three realistic requests. Ask the user whether they represent genuine use and whether important cases are missing.

For each test, record a descriptive name, prompt, supplied files or context, expected result, and objective checks if appropriate.

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

Include meaningful coverage:

- A typical successful request.
- An incomplete or ambiguous request.
- A format-sensitive or rule-sensitive request.
- A realistic case that changes the workflow.
- A request requiring approval, privacy protection, or a safe refusal, when relevant.

Do not test only wording copied from the skill. Vary phrasing, detail level, and context. Avoid retaining private examples when a generalized prompt can test the same capability.

## 8. Run comparisons and preserve evidence

When independent execution is available, compare the skill with a meaningful baseline.

- **New skill:** Run each test with the skill and without it.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the new version with the previous version.

Start all comparable runs under similar conditions. When parallel execution is available, launch skill and baseline runs together for every test case. Preserve the prompt, input files, outputs, and available execution metadata.

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

Record elapsed time and resource-use data as soon as the execution environment reports them, because some systems do not retain this metadata later.

If independent execution is unavailable, run transparent sanity checks instead: apply the skill to each test request, preserve outputs, and ask the user to review them. Do not claim this is equivalent to an independent baseline comparison.

## 9. Define and grade objective checks

While tests run, draft objective checks where they truly help. Explain them to the user before treating them as success criteria.

Good checks are observable and meaningful:

- Required sections are present.
- A generated file opens and contains required fields.
- Calculations match known values within an agreed tolerance.
- The output identifies missing mandatory inputs.
- Claims include required source references.

Store each result with a clear statement, pass/fail value, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable information and requests it."
    }
  ]
}
```

Use programmatic checks when practical. They are more repeatable than visual inspection and can be reused. Do not force numerical checks onto subjective work such as writing quality, visual design, or strategic judgment; those need human review.

## 10. Review results with a human

Present outputs and measurements in an accessible review format. If a review interface is available, use it to show each prompt, output, comparisons, grades, and feedback field. In a headless or limited environment, generate a shareable static review artifact if possible; otherwise present material directly in conversation or as downloadable files.

For each case, show:

- The original prompt and relevant input context.
- The skill output and baseline or earlier-version output when available.
- Objective grades and evidence.
- Timing and resource data when available.
- A clear place for the reviewer to leave feedback.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add effort or detail without value?
- Would the result work for similar requests with different wording or data?

Do this review before making speculative revisions. Human feedback should guide what matters most.

## 11. Analyze results beyond pass rates

Aggregate results when possible: pass rates, average time, average resource use, and variation. Place revised-skill results before the comparison condition in reports.

Then inspect patterns that summary statistics can hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill’s contribution.
- **High variance:** Similar runs differ widely, indicating ambiguity or instability.
- **Tradeoffs:** Quality improves but time or resource use becomes excessive.
- **Failure concentration:** Several misses share a root cause, such as unclear source selection.
- **Unproductive work:** Execution records show redundant research, planning, or formatting.
- **Repeated reconstruction:** Multiple runs create the same helper process, indicating a reusable resource may help.

For a consequential comparison between two versions, use blind review: provide two outputs to an independent evaluator without identifying their origins, grade them with a shared rubric, and reveal the mapping afterward.

## 12. Improve without overfitting

Revise based on user feedback, outputs, and analysis. Change the smallest part likely to fix the underlying cause.

Use these principles:

1. **Fix causes, not examples.** A complaint from one test should lead to a general rule only if it represents a recurring class of problem.
2. **Keep instructions lean.** Remove guidance that does not change behavior or causes wasted effort.
3. **Explain intent.** State why a step protects quality, usability, authorization, or privacy.
4. **Add reusable resources only when justified.** Bundle scripts, templates, or references when repeated work shows their value.
5. **Preserve useful behavior.** Do not discard outcomes the user already values.
6. **Expand tests gradually.** Add a case when it represents a real class of failure, not every one-off incident.

After revision, rerun the full test set in a new iteration, using the same baseline policy. Compare new outputs with prior outputs where possible and collect feedback again.

Stop when the user says the skill is ready, feedback is consistently positive across meaningful cases, objective requirements are reliably met, or further revisions are no longer producing meaningful gains.

## 13. Optimize triggering behavior

Only optimize the activation description after the workflow itself is useful.

Create a realistic trigger-evaluation set with roughly balanced positive and negative examples. Positive examples should be requests that should activate the skill; negative examples should be difficult near-misses that share language or context but need a different capability.

```json
[
  {
    "query": "I need a concise update for leadership from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain when teams usually write progress reports?",
    "should_trigger": false
  }
]
```

Use substantive prompts. Very simple one-step requests may not activate a specialized skill even when the description matches, because the AI can often handle them directly.

Review the test set with the user before optimization. If the environment supports repeated trigger tests, separate examples used to improve the description from held-out examples used to choose it. Select the description by held-out performance rather than by fit to the examples used during editing. Show the user the before-and-after wording and results.

## 14. Package and hand off

Package the core instructions and only the resources required for normal use. Before delivery, audit the package:

- The skill name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on private conventions, personal access, or undeclared capabilities.
- Scripts and references are present, clearly named, and documented.
- No credentials, private identifiers, confidential data, or sensitive examples are included.
- The user can install or adapt the package in their chosen environment.
- Evaluation material is retained only when it is safe and useful.

Provide a concise handoff note describing the skill’s purpose, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an accurate activation description, instructions that handle normal variation, explicit authorization and uncertainty boundaries, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user needs.

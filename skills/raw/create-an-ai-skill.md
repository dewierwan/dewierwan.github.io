---
name: create-an-ai-skill
description: A complete workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing one, test whether it helps, or improve when it activates. A skill is a focused set of instructions and optional resources that help an AI perform a recurring job consistently.

The core loop is:

1. Understand the job, user value, and boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review representative outputs with a person and measure objective requirements where appropriate.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and not narrowly fitted to the tests.
7. Optionally improve the description that determines when the skill activates.
8. Package and hand off the finished skill.

Do not force every project through every stage. A user may want a quick draft, an informal collaborative pass, or a rigorous comparison. Determine where they are in the loop and help them make the next useful decision.

## Communication principles

Match the user’s technical vocabulary and experience. Use plain language by default. Terms such as *evaluation* and *benchmark* are often useful, but explain them briefly when needed. Avoid unexplained technical terms such as “JSON,” “schema,” or “assertion” unless the user is clearly comfortable with them.

Explain why a question matters. For example:

> What should a successful result look like: an answer in chat, a structured report, a file, or an approved external action? The answer determines how the skill should work and how to test it.

Keep the user involved at meaningful decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before imposing a restrictive scope, tool requirement, approval policy, or output format.
- Share proposed test cases before treating them as representative.
- Let human judgment lead for subjective work such as writing quality, visual design, strategic usefulness, and tone.

If the task involves private communications, records, or information about people, establish a legitimate purpose and clear authorization. Use only the minimum relevant approved sources and details. Do not expose unrelated personal information in the skill, test cases, outputs, or packaged resources.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea such as “I need help preparing recurring project updates.” Start with discovery and a first draft.

### B. Existing skill or draft

The user has an instruction file or installed skill and wants it edited, simplified, tested, or optimized. Preserve its established name and identity unless the user asks to rename it. Read the current version before proposing changes.

If the installed copy may not be writable, make an editable copy in a user-approved working location. Keep the original unchanged until the user accepts the revision.

### C. A workflow demonstrated in conversation

The user may say “turn what we just did into a skill.” Extract what can be learned from the conversation before asking questions:

- Inputs and examples supplied.
- Approved tools, information sources, and permissions used.
- The sequence of actions and decisions.
- Corrections and preferences expressed by the user.
- Observed output format and acceptance criteria.
- Conditions that caused the workflow to branch or stop.

Summarize the inferred workflow, state the assumptions, and ask the user to fill important gaps. Do not silently convert a one-time workaround into a universal rule.

### D. Evaluation or optimization request

The user may already have a finished-looking skill and want to know whether it helps. Begin with test design, comparison, review, and targeted revision. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough information to define one coherent job. Adapt these questions to the context rather than asking all of them mechanically.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What requests, wording, or situations should cause it to activate?
3. **Inputs:** What information, files, examples, systems, or permissions may it use?
4. **Outputs:** What should it create, explain, modify, or propose? Is there a required format?
5. **Success:** How will the user know the result is correct, useful, and complete?
6. **Boundaries:** What should the skill not do? When should it ask a question, decline, or return control to the user?
7. **Variations:** What common cases, difficult cases, and exceptions materially change the work?
8. **Dependencies:** Does it need specific capabilities, templates, references, scripts, or access approved by the user?
9. **Testing:** Should it be tested with realistic example requests?

Recommend testing when outputs can be checked objectively, when the workflow is consequential, or when the skill will be reused often. For highly subjective work, suggest a small human review set instead of artificial numeric scoring.

Useful decision questions include:

- “Should the skill make a low-risk best effort when information is missing, or pause and ask?”
- “Should it use a concise default output, a detailed default output, or let the user choose?”
- “May it use any available source, or only sources the user explicitly approves?”
- “Which actions require confirmation because they are external, irreversible, costly, or visible to others?”

### Research before drafting

If relevant approved documentation, examples, comparable skills, or domain guidance are available, inspect them before drafting. Research should reduce burden on the user, not replace their authority over requirements.

Use research to identify:

- Existing standards and conventions.
- Constraints imposed by available capabilities or file formats.
- Reusable methods from related tasks.
- Privacy, safety, compliance, and approval requirements.

If requirements conflict or evidence is uncertain, describe the uncertainty and ask for direction rather than inventing a policy.

## 3. Choose the skill structure

A skill should be focused enough that both users and AI systems can predict what it does. One skill may support closely related variants, but separate unrelated jobs that have different audiences, permissions, sources of truth, or completion criteria.

A portable package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional documentation used when relevant
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and grading materials
```

Use progressive disclosure:

1. **Description:** A short explanation of what the skill does and when it applies.
2. **Core instructions:** The workflow needed for normal use.
3. **Supporting resources:** Detailed references, templates, and scripts loaded only when relevant.

Keep core instructions readable. If the main file becomes difficult to navigate, move detailed domain variants into clearly named reference files and state exactly when to consult each file. Add a table of contents to long references.

For multi-variant work, keep a common selection workflow in the core instructions and separate variant-specific guidance into distinct resources. The AI should choose the relevant branch instead of loading every variation by default.

### Use scripts only for repeatable deterministic work

When test runs reveal repeated reconstruction of the same helper procedure, consider bundling a reusable script or template. Typical candidates include file transformation, structured validation, routine report generation, and data cleanup.

A bundled helper is justified when it is:

- Deterministic or easier to verify than repeated natural-language reasoning.
- Reused across multiple tasks.
- Safer or less error-prone than rebuilding it each time.
- Within the user’s intended access and authorization boundaries.

Document what the helper does, its inputs and outputs, failure behavior, and when not to use it. Do not automate an action merely because automation is possible.

## 4. Write the skill

Draft the skill in clear, imperative language. Explain the reasoning behind important instructions, especially when a rule prevents a predictable failure. An AI is more likely to adapt well when it understands the goal and tradeoff than when it receives a large list of unexplained prohibitions.

Include the following sections when applicable.

### Purpose and scope

State the job, intended outcome, boundaries, and whether the skill creates an answer, produces a file, takes an action, or guides a user through a decision.

### Inputs and prerequisites

List required information, permitted sources, necessary capabilities, and optional inputs. Explain what happens when a required item is unavailable.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or provide a draft clearly marked as incomplete.
```

### Workflow

Give the normal sequence of actions and decision points. Avoid attempting to list every imaginable exception.

A durable general workflow is:

1. Inspect the request, available inputs, constraints, and authorization.
2. Ask focused questions only when an answer would materially change the work.
3. Gather evidence from minimum necessary approved sources.
4. Perform the task using the appropriate method and resources.
5. Check the result against the requested format, evidence, and success criteria.
6. Present the result together with material assumptions, limitations, and next actions.

Use conditional rules when they make decisions predictable:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested action could overwrite work, publish information externally, or create a material commitment, explain the impact and request confirmation first.
```

### Output format

When consistency matters, define an exact or near-exact template.

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty, missing input, or decision needed]
```

Avoid a rigid shell when the task requires contextual judgment. In such cases, define output goals and include a short example rather than forcing every response into the same layout.

### Quality, safety, and privacy checks

Specify the checks needed before completion. Examples include validating calculations, confirming required fields, preserving original data, identifying sources of important claims, or separating verified information from assumptions.

Skills must behave in ways a user would reasonably expect from their description. Do not create instructions that conceal actions, bypass authorization, obtain confidential information without permission, damage systems, or facilitate unauthorized access.

For work involving information about people:

- Confirm the legitimate purpose and applicable authorization.
- Use the minimum relevant records and sources.
- Omit unrelated sensitive details from outputs.
- Respect consent, confidentiality, retention limits, and the audience’s access boundary.
- Avoid unsupported judgments about a person’s character or identity.

For hiring or assessment tasks, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether the assessment distinguishes relevant performance. Do not infer protected traits or make decisions from irrelevant personal information.

### Failure behavior

Describe recovery from common failures in general terms:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or reference:** Explain what could not be verified and offer an approved alternative.
- **Ambiguous request:** Make a reasonable low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, report the issue, or request guidance.
- **Sensitive or high-impact action:** Pause for confirmation before external, irreversible, or consequential actions.

### Examples

Include a small number of generalized examples only when each teaches a distinct decision pattern. Examples should illustrate reasoning and output shape, not replace the skill’s ability to adapt.

## 5. Write a strong description

The description is primarily a routing instruction: it helps the AI decide whether the skill applies. State both **what the skill does** and **when to use it**.

Cover realistic user language, including requests that imply the job without naming it directly. A useful description includes:

- The outcome or task.
- Common contexts and phrases that indicate the task.
- Important limits that prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a status update, leadership summary, progress report, milestone review, or a concise account of risks and next steps, including when they imply the need without using the phrase “status report.”
```

Do not put the full workflow into the description. Do not rely on vague labels such as “help with documents.” Do not make it so broad that it captures nearby work better handled by another skill.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description clearly explain activation conditions?
- Are required inputs, approved sources, permissions, and outputs clear?
- Does the workflow explain why important checks exist?
- Does it address missing information and conflicting requirements?
- Is it free of unnecessary rules, repeated guidance, and brittle wording?
- Does it avoid assumptions about a particular person’s tools, habits, access, or terminology?
- Does it preserve enough judgment for normal variation?
- Does it stay within expected safety, privacy, and access boundaries?

Prefer a lean, understandable prompt over a long prompt full of rules that do not affect outcomes. Repeated absolute language is a warning sign unless the instruction protects a genuine non-negotiable boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create two or three realistic test prompts. Share them with the user and invite corrections or additions before treating them as representative.

For each case, record:

- A descriptive identifier.
- The user prompt.
- Any approved input files or context.
- The expected outcome in plain language.
- Objective checks, if suitable.

A portable evaluation record is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and flag information you cannot verify.",
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful variation:

- A typical successful request.
- An incomplete or ambiguous request.
- A format-sensitive or rule-sensitive request.
- A realistic edge case that changes the workflow.
- A request that should require approval, privacy protection, or refusal when relevant.

Do not create tests that simply repeat the skill’s wording. Vary phrasing, user detail, and context. Use generalized scenarios and sanitized materials; do not put real private records, credentials, or unnecessary personal details into evaluation sets.

## 8. Run comparisons and capture evidence

When the environment supports independent runs, compare the skill against a meaningful baseline.

- **New skill:** Run each prompt with the skill and without the skill.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revision against that snapshot or another user-approved baseline.

Start both conditions for every test case under comparable settings. If parallel execution is available, launch all skill and comparison runs together. This reduces timing distortions and helps ensure fair comparison.

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

For each run, preserve the prompt, approved inputs, outputs, and available metadata such as elapsed time and resource use. Record timing when it is reported, because some execution systems do not retain it later.

If independent agents or parallel execution are unavailable, run a transparent sanity check: follow the skill for each test prompt, preserve the outputs, and ask the user to review them. Do not describe this as a rigorous baseline experiment.

## 9. Define and grade objective checks

While runs are underway, draft objective checks where they genuinely help. Explain them to the user before presenting them as success criteria.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A produced file opens and includes required fields.
- Calculations match known source values within an agreed tolerance.
- The response identifies missing mandatory inputs.
- Important claims include required source references.

Use a stable grading record:

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

Use programmatic checks when practical. They are usually faster, more repeatable, and reusable across iterations. Do not force numeric checks onto subjective quality. Tone, usefulness, visual quality, and strategic judgment often require human review.

## 10. Review results with a human

Present both qualitative outputs and quantitative results. Use an available review interface when possible; otherwise present accessible files or a clear in-conversation comparison.

For each test case, provide:

- The original prompt and relevant approved inputs.
- The skill output and comparison output, if one exists.
- Objective grades and supporting evidence.
- Timing or resource data, if available.
- A clear way for the reviewer to leave feedback.

Ask focused questions:

- “Which result would you trust in normal use, and why?”
- “What was missing, misleading, or difficult to use?”
- “Did the skill add work or detail that was not valuable?”
- “Would this approach still work with different wording or data?”

Empty feedback can indicate that a test case is acceptable, but it is not proof that the skill is solved. Review outputs and measurements as well.

## 11. Analyze results and improve without overfitting

Aggregate results where possible: pass rate, average time, average resource use, and variation. Then look beyond aggregate scores for patterns:

- **Non-discriminating checks:** Both conditions pass, so the check does not demonstrate the skill’s value.
- **High variation:** Similar runs differ substantially, suggesting ambiguity or instability.
- **Tradeoffs:** Quality improves but time or resource cost becomes excessive.
- **Failure concentration:** Multiple failures share a root cause, such as unclear source selection.
- **Unproductive work:** Execution traces show redundant planning, research, or formatting.
- **Repeated reconstruction:** Several runs build the same helper process, suggesting a reusable script or template.

Base revisions on user feedback, outputs, and analysis. Change the smallest part likely to address the underlying cause.

Use these principles:

1. Fix causes, not individual examples.
2. Keep instructions lean and remove guidance that does not improve results.
3. Explain intent so the AI can adapt intelligently.
4. Add reusable assets only when repeated work demonstrates their value.
5. Preserve behavior users already value.
6. Add tests only for real categories of failure.

After revision, rerun the test set in a new iteration and compare it with the chosen baseline. Where possible, show prior outputs beside new outputs so the reviewer can see whether the change helped.

Stop when the user says the skill is ready, feedback is consistently positive across meaningful cases, objective requirements are reliably met, or further revisions are not producing meaningful improvement.

## 12. Optional blind comparison

For a more rigorous comparison between two versions, use blind review. Give an independent evaluator two outputs without identifying which version produced each one. Ask it to apply a shared rubric, then reveal the mapping only after the assessment is recorded.

Use blind comparison when versions have similar scores but noticeably different quality, when the decision is consequential, or when reviewers may favor a newer version by default. Keep the rubric tied to user value: correctness, completeness, clarity, constraint adherence, safety, and practical usability.

## 13. Optimize activation behavior

Only optimize the description after the underlying workflow is useful.

Create a balanced set of realistic requests that should activate the skill and realistic near-misses that should not. Use detailed, substantive requests where consulting a skill would be helpful.

Positive cases should vary by:

- Formal and casual phrasing.
- Direct naming and implied need.
- Common and less common valid uses.
- Situations where related skills could compete but this one should apply.

Negative cases should be difficult near-misses, not obviously irrelevant requests. They should share concepts or keywords but belong to another job, require different capabilities, or lack the conditions that make this skill appropriate.

Review the query set with the user. If the environment can test activation repeatedly, divide the set into improvement cases and held-out selection cases. Select the description using held-out performance to reduce overfitting. Show the user the previous description, revised description, and results before applying it.

## 14. Package and hand off

Package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states when the skill applies.
- Instructions do not depend on undeclared tools, private conventions, or unapproved access.
- Scripts, references, and assets are present, clearly named, and documented.
- No confidential data, credentials, identifiers, or unnecessary personal details remain.
- Evaluation material is retained only when safe and useful.
- The user can install or adapt the package in their chosen environment.

Provide a short handoff note stating what the skill does, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an honest activation description, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.

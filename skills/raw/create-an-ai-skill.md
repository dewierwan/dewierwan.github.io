---
name: create-an-ai-skill
description: Design, test, refine, evaluate, and package reusable AI skills with realistic reviews, measurable checks, safe access boundaries, and accurate activation rules.
---

# Create an AI skill

Use this workflow to design a reusable AI skill, improve an existing skill, evaluate whether it helps, and refine when it activates. A skill is a focused set of instructions, with optional supporting resources, that helps an AI perform a recurring job reliably.

The standard loop is:

1. Understand the job, intended users, boundaries, and approved access.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review representative outputs with the user and measure objective requirements where appropriate.
5. Improve the skill based on evidence rather than isolated preferences.
6. Repeat until it is useful, reliable, and not narrowly fitted to its test examples.
7. Optionally improve the description that determines when the skill is used.
8. Package and hand off the finished skill.

Adapt the depth of this process to the user’s goal. A user may want a quick collaborative draft rather than a benchmark. Another may need careful comparison before relying on a skill for important recurring work. First identify where the user is in the loop, then help them take the next useful step.

## Communication principles

Match the user’s technical familiarity. Use plain language by default. Terms such as *evaluation* and *benchmark* are often understandable, but define them briefly when useful. Do not use terms such as “JSON,” “assertion,” “schema,” or “baseline” without explanation unless the user clearly works with them already.

Explain why a question matters. For example:

> What should a successful result look like: a chat response, a structured report, a file, or a proposed action? This determines how completion can be checked.

Keep the user involved at meaningful decision points:

- Confirm the intended job before writing a large instruction set.
- Ask before adding a restrictive scope, required capability, or approval requirement.
- Share proposed test cases before treating them as authoritative.
- Let human judgment lead when quality is subjective, such as tone, visual design, creative value, or strategic usefulness.
- Make uncertainty visible rather than silently choosing a high-impact interpretation.

## 1. Identify the starting point

Determine which situation best fits.

### New skill

The user has an idea for recurring work, such as preparing structured summaries or checking files before release. Begin with discovery and a first draft.

### Existing skill

The user has instructions that need editing, simplification, testing, or improvement. Read the current skill before proposing changes. Preserve its established name and identity unless the user asks to rename it. If the installed copy may be read-only, make an editable copy in a user-approved working location before changing it.

### Workflow demonstrated in the conversation

The user may ask to turn a demonstrated process into a skill. Extract what is already known before asking repeated questions:

- Inputs and approved sources used.
- The sequence of decisions and actions.
- Tools or capabilities involved.
- Corrections and preferences the user expressed.
- Output form and acceptance criteria.
- Conditions that caused the process to change direction.

Summarize the inferred workflow and identify gaps for the user to confirm. Do not convert a one-time workaround into a general rule without checking that it is reusable.

### Evaluation or activation request

The user may have a finished-looking skill and want to know whether it works or whether it activates appropriately. Go directly to test design, evaluation, and evidence-based revision. Do not rewrite a useful skill merely because a rewrite is possible.

## 2. Capture intent, scope, and authorization

Gather enough information to define one coherent job. Do not ask every question mechanically; begin with the unknowns that would most change the design.

1. **Purpose:** What should the AI accomplish?
2. **Trigger:** What requests, wording, or situations should cause this skill to be used?
3. **Inputs:** What information, files, systems, examples, or permissions may it use?
4. **Outputs:** What should it produce, change, or recommend? Is a specific format needed?
5. **Success:** How will the user know the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask, pause, decline, or return work to the user?
7. **Variation:** What normal alternatives, difficult cases, and exceptions matter?
8. **Dependencies:** Does it need a particular capability, template, reference, or script?
9. **Testing:** Should it be tested with representative requests before release?

Offer clear choices where useful:

- Should the skill make a best effort when data is incomplete, or stop and ask?
- Should the output be concise, detailed, or user-selectable?
- Should it work with any source, or only explicitly approved sources?
- Should it draft an external action or require approval before taking it?

### Privacy and access boundary

A skill may need to inspect records, messages, documents, or information about people. In that case, require a legitimate purpose and clear authorization before accessing them. Use only the minimum relevant sources and information. Do not include unrelated personal details in prompts, test data, logs, examples, or outputs.

Respect consent, confidentiality expectations, and the access boundary of the user’s role. If authorization, purpose, or source scope is unclear, ask a focused question before proceeding. Design the skill to summarize, aggregate, or redact sensitive information when that meets the task’s need better than reproducing raw material.

Do not design a skill to conceal actions, bypass authorization, obtain data outside the user’s access boundary, or expose confidential material. If a request cannot be safely completed, explain the limitation and offer a safe alternative where possible.

### Research before drafting

If approved documentation, comparable skills, templates, or domain guidance are available, review them before drafting. Research should reduce burden on the user, not replace their authority over requirements.

Use research to find:

- Existing conventions and required output standards.
- Constraints imposed by available capabilities or file formats.
- Reusable approaches for comparable work.
- Applicable safety, privacy, compliance, or approval expectations.

If evidence conflicts or a requirement is uncertain, report that uncertainty rather than inventing a rule.

## 3. Choose a structure and supporting resources

Keep a skill focused enough that both users and AI systems can predict what it does. A skill can support variations of one job, but unrelated jobs should normally be separate when they have different users, permissions, sources of truth, or completion criteria.

A portable package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed documentation
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test prompts and grading material
```

Use progressive disclosure:

1. **Metadata:** A short name and description used to decide whether the skill applies.
2. **Core instructions:** The normal workflow loaded when the skill applies.
3. **Supporting resources:** Detailed references, templates, or scripts consulted only when needed.

Keep the core instructions readable. When they become too large, move specialized guidance into clearly named reference files and state exactly when each file should be consulted. Give lengthy references a navigation section. For a skill supporting several platforms or domains, keep one shared workflow and separate variant-specific guidance so the AI loads only the relevant material.

### When to bundle a script

If several test runs independently reconstruct the same helper procedure, consider bundling it. Scripts are especially valuable for deterministic work such as conversion, validation, calculations, file generation, or repetitive cleanup.

Bundle a script only when it is reusable, within the intended permission boundary, and easier to verify than repeated natural-language steps. Document what it does, its inputs and outputs, expected failure behavior, and when not to use it. Do not add automation merely because it is possible.

## 4. Write the skill

Draft in clear imperative language. Explain the reason behind important instructions, especially when a rule prevents a predictable failure. A capable AI can adapt better when it understands the quality, usability, safety, or authorization goal behind a step.

A useful skill commonly includes the following sections.

### Purpose and scope

State the job, intended context, and boundaries. Clarify whether the skill creates a response, produces a file, makes a recommendation, performs an action, or guides the user through a process.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State what happens when a required item is absent.

```markdown
Before preparing the requested output, confirm the relevant period, scope, and approved source.
If a required source is unavailable, ask for an approved substitute or provide a draft clearly marked as incomplete.
```

### Workflow

Describe the normal sequence and its decision points rather than trying to list every possible edge case.

1. Inspect the request and available inputs.
2. Ask for clarification only when it materially changes the work or its risk.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result, key assumptions, and unresolved limitations.

Use conditional instructions where they help:

```markdown
If the user provides an approved template, follow it.
If no template is provided, use the default structure below.
If an action could overwrite, publish, send, or otherwise materially affect work, explain the impact and request confirmation first.
```

### Output format

When consistency matters, define an exact or near-exact structure.

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or required follow-up]
```

Do not impose rigid formatting where adapting to the user’s situation is more valuable. For those tasks, define the outcome and quality standard, then include a small generalized example only if it teaches a distinct pattern.

### Quality, safety, and failure behavior

State checks needed before completion: required fields, validated calculations, evidence for important claims, preservation of original data, clear uncertainty labels, or approval before sensitive actions.

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or reference:** Say what could not be verified and offer a safe alternate path.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, report the issue, or request guidance.
- **High-impact action:** Pause for confirmation before irreversible, external, or consequential actions.
- **Unauthorized or unsafe request:** Do not bypass access controls, conceal actions, expose sensitive information, or perform harmful work.

## 5. Write a strong skill description

The description is a routing instruction. It should state both what the skill does and when it should be used. Cover realistic phrasing, including requests that imply the task without naming it.

A good description includes:

- The outcome or job.
- Common contexts and phrases that signal relevance.
- Important scope limits that prevent costly false activation.

Example pattern:

```text
Produce structured summaries from approved source material. Use when a user asks for a concise update, a review of progress, key risks, open questions, or next actions, including when they describe the need without using the word “summary.”
```

Do not put the whole procedure in the description. Do not use vague descriptions such as “help with documents.” Also avoid making it so broad that it captures adjacent work that another skill should handle.

## 6. Review before testing

Read the draft as a new user would. Check:

- Is the job clear, coherent, and bounded?
- Does the description say when to activate it?
- Are inputs, permissions, and outputs clear?
- Does the workflow explain important checks?
- Does it handle missing information and unavailable capabilities?
- Is it free of unnecessary rules, repeated guidance, and brittle wording?
- Does it avoid personal defaults, hidden access assumptions, and undeclared dependencies?
- Does it preserve enough flexibility for normal variation?

Prefer a lean instruction set over a long list of rules that do not change outcomes. Excessive absolute language is a warning sign unless the behavior is genuinely non-negotiable, such as respecting authorization or preventing destructive actions.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic requests and show them to the user for review. Add more only when they cover meaningful variation.

For each case, record a descriptive name, prompt, inputs, expected outcome, and objective checks where suitable. A portable record can look like this:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-input-handling",
      "prompt": "Create the requested structured output from the supplied material and clearly flag anything that cannot be verified.",
      "expected_output": "A useful structured result that distinguishes supported information from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover distinct situations such as a typical request, incomplete input, a format-sensitive request, an edge case that changes the workflow, and an approval-sensitive action when relevant. Vary wording and detail level. Avoid retaining personal, confidential, or unnecessary sensitive material in test cases.

## 8. Run comparisons and collect evidence

When the environment supports independent runs, compare the skill against a meaningful baseline:

- For a new skill, run each test with the skill and without it.
- For an existing skill, preserve an unchanged snapshot before editing and compare the revised version with that snapshot or another clearly identified prior version.

Run both conditions under comparable settings. If parallel execution is available, start all skill and baseline runs together. Store each iteration, test case, configuration, inputs, outputs, and available metadata in a clear directory structure.

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

Record elapsed time and resource-use information as soon as the execution environment reports it, because some systems do not preserve it. Keep inputs and outputs within the appropriate access boundary; do not copy confidential source material into broadly accessible evaluation locations.

If independent runs are unavailable, perform a transparent sanity check: apply the skill to each prompt, save the results, and ask the user to inspect them. Do not present this as a rigorous baseline comparison.

## 9. Define, grade, and analyze checks

While tests run, draft objective checks when they genuinely measure user value. Explain them before treating them as the definition of success.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A produced file opens and includes required fields.
- A calculation matches a known result within an agreed tolerance.
- Missing mandatory inputs are identified.
- Required citations or source references appear.

Use a stable grading record with a check, pass/fail result, and evidence:

```json
{
  "expectations": [
    {
      "text": "Identifies required information that is unavailable.",
      "passed": true,
      "evidence": "The output separates unsupported items from the completed result and requests the missing input."
    }
  ]
}
```

Use programmatic checks when practical. They are more repeatable than visual judgment and can be reused in later iterations. Do not force numerical checks onto subjective quality; usefulness, tone, aesthetics, and judgment need human review.

Aggregate pass rates, time, resource use, and variation where possible. Then look beyond averages:

- Checks that pass in every condition may not distinguish the skill’s value.
- Large variation may reveal unclear instructions or environmental instability.
- Higher quality may come with an unacceptable time or resource cost.
- Several failures may share one cause, such as unclear source selection.
- Execution traces may reveal redundant planning or research.
- Repeated helper construction may justify a bundled script or template.

## 10. Review with the user and improve

Present outputs alongside measurements using an available review interface or accessible files. For each test, show the prompt, relevant inputs, outputs from each condition, objective grades with evidence, and available timing or resource data. Give the user a simple way to provide feedback.

Ask focused questions:

- Which result would you trust in routine use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add work or detail that was not valuable?
- Would this work with different wording or data?

Generalize from feedback rather than encoding one test example into the prompt. Fix the underlying cause with the smallest change likely to work. Keep instructions lean, explain intent, preserve valued behavior, and add reusable resources only when evidence justifies them.

After revision, rerun the full relevant test set in a new iteration and compare it with the same baseline policy. Stop when the user is satisfied, requirements are reliably met, feedback is consistently positive, further revisions do not create meaningful improvement, or the remaining issue requires a product decision or unavailable capability.

## 11. Optional blind comparison and trigger optimization

For a consequential choice between two versions, give an independent evaluator two outputs without revealing which version produced each one. Have it judge against a shared rubric such as correctness, completeness, clarity, constraint adherence, safety, and practical usability. Reveal the source only after recording the judgment.

Once the workflow itself is stable, test the description’s activation behavior. Create a balanced set of realistic requests that should activate the skill and difficult near-misses that should not. Review the set with the user. Use substantive prompts: simple one-step requests may not activate a specialized skill even if its description matches.

For positive cases, vary formality, wording, implied versus explicit requests, and common versus less common valid uses. For negative cases, use close alternatives that share vocabulary but belong to another job. Avoid obviously irrelevant negatives because they do not test routing quality.

If the environment can evaluate candidate descriptions repeatedly, separate improvement examples from held-out examples. Choose the description that performs best on held-out requests, not merely the one that fits the examples used during editing. Show the user the old description, new description, and results before applying it.

## 12. Package, audit, and hand off

Package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name and description are clear and stable.
- The instructions accurately describe scope and activation conditions.
- Required capabilities, references, and scripts are present and documented.
- No private paths, credentials, confidential records, personal data, or undeclared local conventions remain.
- Scripts behave predictably and stay within intended authorization boundaries.
- Test material is retained only when safe and useful.
- A new user can install or adapt the package in their chosen environment.

Provide a short handoff note describing what the skill does, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, accurate activation guidance, instructions that handle normal variation, explicit boundaries for uncertainty and permission-sensitive work, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.

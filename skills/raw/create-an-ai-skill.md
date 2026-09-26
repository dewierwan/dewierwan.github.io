---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a repeated workflow captured from a conversation.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, improve an existing one, evaluate whether a skill helps, or refine when it activates. A skill is a focused set of instructions, plus optional resources such as scripts, templates, and references, that helps an AI handle a recurring kind of work reliably.

The core loop is:

1. Understand the job, scope, and boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with a person and measure objective requirements where appropriate.
5. Improve the skill based on evidence.
6. Repeat until further changes are not meaningfully improving results.
7. Optionally improve the skill description so it activates for appropriate requests.
8. Package and hand off the finished skill.

Do not force every project through every stage. A user may want a quick draft, a collaborative review, or a rigorous comparison. Identify where they are in the loop and help them make the next useful decision.

## Communicate at the user’s level

Match the user’s technical vocabulary and experience. Use plain language by default. Terms such as *evaluation* and *benchmark* can be useful, but briefly explain them if needed. Avoid unexplained technical terms such as “JSON,” “schema,” or “assertion” unless the user shows comfort with them.

Explain why important questions matter. For example:

> What should a successful result look like: a chat response, a structured report, a downloadable file, or an action in another system? This determines what the skill must produce and how we can test it.

Keep the user involved at key decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before imposing a restrictive scope, a specific tool, or an approval requirement beyond what the task needs.
- Share proposed test cases before treating them as the evaluation set.
- Use human judgment for subjective qualities such as voice, visual quality, usefulness, or strategic judgment.
- Let the user choose the appropriate rigor level when tradeoffs exist.

If the task involves private communications, internal records, or information about people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and details. Do not expose unrelated sensitive details in test cases, examples, outputs, or packaged resources.

## 1. Determine the starting point

First identify which situation applies.

### New skill

The user has an idea such as “I need help producing recurring project updates.” Begin with discovery and a first draft.

### Existing skill

The user has a draft or installed skill and wants it edited, simplified, tested, or improved. Read the current instructions before proposing changes. Preserve its established name and identity unless the user asks to rename it.

Before editing an existing skill, preserve an unchanged copy when possible. This gives you a valid baseline for later comparison and protects against accidental loss.

### Workflow demonstrated in the conversation

The user may say “turn what we just did into a skill.” Extract what you can from the conversation before asking questions:

- Inputs and source materials used.
- Actions, tools, and decision sequence.
- Corrections or preferences the user supplied.
- Output formats and acceptance criteria.
- Points where the workflow changed direction.
- Assumptions that were safe in that conversation but may not generalize.

Summarize the inferred workflow, identify gaps, and ask the user to confirm it. Do not silently turn a one-time solution into a general rule.

### Evaluation or optimization request

The user may already have a mature-looking skill and want evidence that it improves outcomes. Go directly to test design, evaluation, and revision. Do not rewrite a skill merely because a rewrite is possible.

## 2. Capture intent and scope

Gather enough information to define a coherent job. Adapt these questions to the context rather than asking all of them mechanically.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What requests, wording, or situations should cause the skill to be used?
3. **Inputs:** What information, files, systems, examples, or approved sources can it use?
4. **Permissions:** What access has been granted, and which actions require user confirmation?
5. **Outputs:** What should it produce, change, or recommend? Is a format required?
6. **Success criteria:** How will the user know that the result is correct, useful, or complete?
7. **Boundaries:** What should it not do? When should it ask, pause, decline, or hand work back to the user?
8. **Variations:** Which common cases, difficult cases, or exceptions materially change the workflow?
9. **Dependencies:** Does the work require a particular capability, template, reference, script, or user-provided access?
10. **Testing:** Should the skill be tested with example requests before release?

Recommend testing when outputs are objectively checkable, the work is consequential, the skill will be used repeatedly, or the task contains multiple steps that can fail independently. For highly subjective creative work, start with human review rather than artificial numerical measures.

Useful choices include:

- “Should the skill make a low-risk best effort when information is missing, or ask before proceeding?”
- “Should it produce a concise result, a detailed result, or let the user choose?”
- “May it use any available source, or only sources the user has explicitly approved?”
- “Should it only prepare a draft, or may it take external actions after confirmation?”

## 3. Research and inspect available materials

If relevant documentation, comparable skills, user-approved references, or technical constraints are available, inspect them before drafting. Research should reduce user burden, not replace user authority over requirements.

Use only approved and necessary sources. For sensitive records, access only the minimum relevant information, retain it only as needed for the task, and omit personal details unrelated to the intended output.

Research can identify:

- Existing conventions and output standards.
- Constraints imposed by a file format, interface, or available capability.
- Reusable patterns from comparable work.
- Privacy, safety, compliance, or approval requirements.
- Existing assets that should be reused rather than recreated.

If sources conflict or requirements remain uncertain, state the uncertainty instead of guessing.

## 4. Choose a maintainable structure

Keep a skill focused enough that users and the AI can predict what it does. Put unrelated jobs in separate skills when they have different audiences, permissions, sources of truth, or definitions of completion.

A typical package can contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional documentation consulted when needed
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata:** A concise name and description that help route requests.
2. **Core instructions:** The workflow needed for ordinary uses.
3. **Supporting resources:** Detailed references, templates, or scripts loaded only when relevant.

Keep the core instructions readable. If they become large, move specialized material into clearly named files and state exactly when each file should be consulted. Give long reference material clear navigation.

For skills with several variants, keep a shared selection workflow in the core instructions and place variant-specific guidance in separate references. The AI should read only the applicable variant.

### When to bundle a script

If several test runs independently reconstruct the same helper procedure, consider bundling it as a reusable script. Examples include validation, conversion, report assembly, or deterministic data cleanup.

Bundle a script only when it is clearly useful:

- It is deterministic or easier to verify than repeated natural-language steps.
- It is likely to be reused.
- It reduces errors or unnecessary effort.
- Its inputs, outputs, and permission boundaries can be documented.

Document what the script does, what it accepts, expected outputs, and when it should not be used. Do not add automation simply because it is possible.

## 5. Write the skill

Write in clear, imperative language. Explain the reason behind important instructions, especially when a step prevents a predictable failure. A capable AI can adapt better when it understands the goal and tradeoff than when it receives a long list of unexplained rigid rules.

A useful skill commonly includes the following sections.

### Purpose and scope

State the job, intended outcome, and boundaries. Clarify whether the skill creates an answer, produces a file, guides a process, or performs an approved action.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State what to do when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved data source.
If the source is unavailable, ask the user for an export or provide a clearly marked incomplete draft.
```

### Workflow

Give the normal sequence of work, including meaningful decision points:

1. Inspect the request and available inputs.
2. Ask focused questions only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Validate the result against requested format and success criteria.
6. Present the result, assumptions, and unresolved limitations.

Use conditional rules where useful:

```markdown
If the request provides a required template, follow it.
If no template is provided, use the default structure below.
If an action could overwrite important work or create an external commitment, explain the impact and request confirmation first.
```

### Output format

When consistency matters, define a template:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing information]
```

Do not impose a rigid shell when adapting to context is more valuable. In that case, state goals and provide a small generalized example instead.

### Quality, privacy, and safety checks

State checks required before completion. These may include confirming required fields, validating calculations, preserving originals, citing key sources, separating verified information from assumptions, or flagging uncertainty.

The skill must not conceal actions, bypass authorization, extract confidential information, damage systems, or enable unauthorized access. For people-related records, keep conclusions limited to the authorized purpose and role-relevant evidence. Avoid unsupported inferences about sensitive personal characteristics.

### Failure behavior

Describe recovery behavior in general terms:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** Explain what could not be verified and offer an alternative.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the result as complete; correct it, report it, or request guidance.
- **High-impact action:** Pause for confirmation before irreversible, external, or consequential actions.

## 6. Review the draft before testing

Read the skill as though encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description explain when to use the skill?
- Are inputs, approvals, and outputs clear?
- Does the workflow handle ordinary variation without becoming overly restrictive?
- Does it explain why important checks exist?
- Does it say what to do when data is missing or sources conflict?
- Does it avoid hidden reliance on a specific person’s habits, access, or tools?
- Are private data, credentials, identifiers, and confidential examples excluded?
- Is there guidance that adds length but does not change useful behavior?

Prefer lean, understandable instructions over lengthy rules that do not affect outcomes. Repeated absolute wording is a warning sign unless it protects a genuine authorization, safety, or privacy boundary.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic test prompts. Share them with the user and invite corrections or additions before relying on them.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Any allowed input files or context.
- The expected outcome in plain language.
- Objective checks, if suitable.

A portable evaluation record can look like this:

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

Cover meaningfully different situations:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic exception that changes the workflow.
- A request that should prompt approval, caution, or refusal when relevant.

Do not make tests merely repeat the skill’s wording. Vary phrasing, detail level, user sophistication, and context. Do not include private, embarrassing, or unnecessary personal information in test material.

## 8. Run comparisons and preserve evidence

When the environment supports independent runs, compare the skill against a meaningful baseline.

- **New skill:** Run each prompt with the skill and without it.
- **Existing skill:** Compare the revised skill against an unchanged snapshot of the earlier version.

Use comparable conditions. If parallel execution is available, start both configurations for all test cases at the same time. This limits timing distortion and avoids revising one condition after seeing the other.

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

For every run, preserve the prompt, allowed inputs, outputs, and any available metadata such as duration or resource use. Record timing as soon as the environment reports it, since some systems do not retain it afterward.

If independent agents or parallel execution are unavailable, perform a transparent sanity check: follow the skill for each prompt, save the results, and ask the user to review them. Do not describe this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs are in progress, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are observable and meaningful:

- Required sections are present.
- A generated file opens and contains required fields.
- Calculations match a known source within an agreed tolerance.
- The output identifies missing mandatory inputs.
- Key claims include required source references.

Each check should include a clear statement, pass/fail result, and evidence:

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

Use programmatic checks when practical; they are more repeatable than visual inspection and can be reused later. Do not force numerical measures onto subjective work. Tone, design quality, creativity, and practical usefulness often need human review.

## 10. Review and analyze results

Present both qualitative outputs and quantitative evidence. Use an available review interface when possible; otherwise present outputs and comparison data clearly in conversation or accessible files.

For each test case, show:

- The original prompt and relevant allowed inputs.
- The skill output and comparison output, if available.
- Objective grades with evidence.
- Timing or resource data, if available.
- A way for the user to state what worked and what should change.

Ask focused questions:

- Which output would you trust in normal use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add work or detail that did not help?
- Would this work for similar requests with different wording or data?

Aggregate results when possible, including pass rate, average duration, average resource use, and variation. Then inspect patterns that summary numbers may hide:

- Checks that pass equally often with and without the skill.
- High-variance tests suggesting ambiguity or instability.
- Quality gains that cost too much time or effort.
- Several failures with the same root cause.
- Repeated planning, research, or formatting that does not improve outputs.
- Repeated recreation of a helper procedure that should become a shared resource.

## 11. Improve without overfitting

Base changes on user feedback, actual outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Use these principles:

1. **Fix causes, not examples.** Generalize from a complaint rather than adding a rule for one test prompt.
2. **Keep instructions lean.** Remove guidance that does not earn its place.
3. **Explain intent.** State why a step protects quality, usability, privacy, or safety.
4. **Add reusable assets only when evidence supports them.**
5. **Preserve useful behavior.** Do not discard what users value while fixing another issue.
6. **Expand tests gradually.** Add cases for real classes of failure, not every isolated event.

After revision, rerun the full test set in a new iteration. Use the same baseline policy, compare with earlier outputs where possible, and collect feedback again.

Stop when the user says the skill is ready, feedback is consistently positive across meaningful cases, objective requirements are reliable, or further changes are not producing meaningful gains.

## 12. Optional blind comparison

When two versions have similar measured results but differ in qualitative quality, use blind comparison. Give an independent evaluator two outputs without identifying their versions. Ask it to judge against a shared rubric, then reveal the mapping after the judgment is recorded.

Base the rubric on user value: correctness, completeness, clarity, adherence to constraints, safety, and practical usability. Analyze why one result was preferred before making another revision.

## 13. Optimize activation behavior

Once the workflow itself is useful, evaluate the description that determines when the skill activates. Do this after the skill is stable enough to deserve broader use.

Create a realistic set of requests that should activate the skill and nearby requests that should not. Include enough detail that a specialized skill would be useful.

Positive cases should include formal and casual wording, direct and implied requests, common and uncommon valid cases, and cases where a related skill could compete.

Negative cases should be difficult near-misses, not obviously irrelevant prompts. They should share vocabulary or context but require a different workflow, capability, or scope.

```json
[
  {
    "query": "I need a concise leadership update from these project notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what a project status report is and why teams use one?",
    "should_trigger": false
  }
]
```

Review the query set with the user. If repeated activation tests are available, separate examples used to improve the description from held-out examples used to choose it. Choose the description that performs best on held-out cases, not merely the one that fits the drafting examples.

Keep the final description honest: state what the skill does, realistic contexts where it applies, and important limits that prevent harmful or costly false activation.

## 14. Package and hand off

Package only the core instructions and resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on undeclared personal conventions, access, or tools.
- Scripts and references are present, clearly named, and documented.
- No credentials, private records, identifiers, or sensitive examples remain.
- The user can install or adapt the package in their chosen environment.
- Evaluation material is retained only when safe and useful.

Provide a short handoff note explaining what the skill does, required capabilities, known limitations, and how to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, a description that routes appropriate requests, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and produce better results for the user’s real recurring work.

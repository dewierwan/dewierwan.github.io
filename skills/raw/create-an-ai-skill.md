---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, revise an existing skill, assess whether it improves results, or improve its activation description. A skill is a focused set of instructions, optional resources, and quality checks that help an AI perform a recurring job reliably.

The central loop is:

1. Understand the intended job and its boundaries.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Review outputs with a person and use objective checks where appropriate.
5. Improve the skill using evidence rather than guesswork.
6. Repeat until the skill is useful, reliable, and not narrowly tuned to a few examples.
7. Optionally improve the description that determines when the skill is selected.

Do not force every project through every stage. Some users want a quick collaborative draft; others need a careful comparison and review cycle. First determine where the user is, then help them take the next useful step.

## Communication principles

Match the user’s familiarity with technical language. Use plain English by default. Terms such as *evaluation* and *benchmark* are often understandable, but briefly define them if helpful. Do not introduce terms such as “schema,” “assertion,” or “JSON” without explanation unless the user is already using them comfortably.

Explain why a question matters. For example, instead of asking only “What is the output format?”, ask: “What should a successful result look like: a chat response, a structured report, a file, or an approved action? This determines how we test completion.”

Keep the user involved in important choices:

- Confirm the purpose before writing extensive instructions.
- Ask before adding restrictive scope, required capabilities, or approval rules.
- Show proposed test cases before treating them as the evaluation set.
- Let human judgment lead when quality is subjective, such as writing style, design, tone, usefulness, or strategy.
- State uncertainty rather than implying that an unverified decision is certain.

If the skill uses private communications, records, or information about people, require a legitimate purpose and clear authorization. Use only the minimum relevant information and sources. Exclude unrelated personal details, respect consent and privacy expectations, and keep outputs within the appropriate access boundary.

## 1. Identify the starting point

Determine which of these situations best describes the request.

### New skill

The user has an idea for recurring work, such as preparing project updates, reviewing a class of documents, transforming data, or guiding a standardized process. Start with discovery, scope, and a first draft.

### Existing skill

The user has an existing instruction set and wants it edited, simplified, tested, or improved. Read it before proposing changes. Preserve its established name and identity unless the user asks to change them.

When an existing skill is available only in a location that cannot be edited, make a working copy in a user-approved writable location. Keep the original unchanged until the user approves the revised version.

### Workflow demonstrated in the conversation

The user may say, “Turn what we just did into a skill.” Extract what is already known from the conversation before asking broad questions:

- Inputs, files, and information sources used.
- The sequence of decisions and actions.
- Tools or capabilities needed.
- Corrections and preferences the user gave.
- Output format and evidence of success.
- Conditions that caused the workflow to take a different path.

Summarize the inferred workflow, identify the gaps, and ask the user to confirm it. Do not convert a one-time workaround into a general rule without checking whether it applies to future cases.

### Evaluation or optimization request

The user may have a finished-looking skill and ask whether it works. Start with test design, comparison, and review. Do not rewrite a skill merely because a rewrite is possible; use evidence to identify what needs improvement.

## 2. Capture intent and boundaries

Gather enough information to define a coherent job. Adapt these questions to the user’s situation rather than asking all of them mechanically.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What requests, wording, or situations should cause the skill to be used?
3. **Inputs:** What information, files, references, systems, or permissions may it use?
4. **Outputs:** What should it produce, change, or communicate? Is there a required format?
5. **Success:** How will the user know the output is correct, useful, or ready?
6. **Boundaries:** What should it not do? When should it ask for clarification, request approval, decline, or hand work back to the user?
7. **Variation:** What common cases, difficult cases, and exceptions materially change the work?
8. **Dependencies:** Are particular capabilities, templates, references, or scripts required?
9. **Testing:** Should the skill be tested with realistic example requests before release?

Offer useful choices when they expose a decision clearly:

- “When information is missing, should the skill make a low-risk best effort or pause and ask?”
- “Should it produce a brief summary, a detailed report, or let the user choose?”
- “Should it use any available source, or only sources explicitly approved by the user?”
- “Which actions require confirmation because they are external, irreversible, costly, or high impact?”

Recommend test cases when outputs can be objectively checked, the work is consequential, the process is repeatable, or the skill will be used by more than one person. For highly subjective work, recommend representative examples and human review rather than pretending that a simple score captures quality.

## 3. Research and inspect available resources

Before drafting, inspect relevant user-approved material when it would reduce uncertainty or improve the result. This may include existing instructions, templates, documentation, examples, output standards, or comparable skills.

Use research to identify:

- Existing conventions and required output formats.
- Constraints imposed by a file type, system, or workflow.
- Reusable patterns for similar jobs.
- Safety, privacy, compliance, approval, or retention requirements.

Research should reduce burden on the user, not replace their authority over requirements. If sources conflict, distinguish the conflict from established facts and ask the user which source should govern.

For private or sensitive sources, verify authorization before accessing them. Limit review to information necessary for the requested task. Do not include private details in test fixtures, examples, logs, reports, or package contents unless they are essential, authorized, and appropriate for every intended recipient.

## 4. Choose an appropriate skill structure

A skill should be focused enough that both the user and the AI can predict what it does. A skill may support related variants of the same job, but unrelated work should usually be separate skills when it has different users, sources of truth, approval requirements, or definitions of completion.

A typical package may contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed guidance
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional tests and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help decide when to use the skill.
2. **Core instructions:** The workflow required for normal use.
3. **Supporting resources:** Detailed references, templates, and scripts loaded only when relevant.

Keep core instructions readable. If they become too large, move specialized details into clearly named reference files and state exactly when each file should be consulted. Large reference files should include a navigation section or table of contents.

For skills with several variants, organize supporting material by variant. The core instructions should explain how to choose the relevant variant so the AI does not load or apply unrelated rules.

### Bundle resources only when they earn their place

If test runs show repeated reconstruction of the same deterministic task, consider bundling a reusable script, template, or reference. Good candidates include data validation, standard file transformations, repeatable calculations, report assembly, or format checks.

A bundled resource is justified when it is:

- Repeatable and meaningfully more reliable than recreating the procedure each time.
- Safe and understandable within the user’s authorization boundary.
- Likely to be reused across ordinary requests.
- Documented with expected inputs, outputs, and failure behavior.

Do not add automation solely because it is possible. A bundled resource should not conceal actions, require undeclared access, or make changes outside the user’s intended scope.

## 5. Write the skill instructions

Write in clear, direct language. Prefer imperative instructions, but explain why important steps matter. AI systems generally handle variation better when they understand the goal and tradeoff than when given a long sequence of unexplained prohibitions.

Use the following components when they apply.

### Purpose and scope

State the job, intended outcome, and boundaries. Clarify whether the skill produces an answer, creates a file, guides a user, or performs an approved action.

### Inputs and prerequisites

List required information, permitted sources, necessary permissions, and optional inputs. State what to do if a required item is missing.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or provide a clearly marked incomplete draft.
```

### Workflow

Give the normal sequence of work and include decision points rather than attempting to list every imaginable exception.

A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Clarify only uncertainties that materially affect the result.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the result against requested format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limits.

Use conditional guidance where it helps:

```markdown
If the user provides a required template, follow it.
If no template is available, use the default structure below.
If an action could overwrite important work or affect an external system, explain the impact and request confirmation before proceeding.
```

### Output format

When consistency is important, provide a template. For example:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing information]
```

Avoid rigid templates when contextual adaptation is the main source of value. In those cases, describe the desired qualities and provide a small example instead.

### Quality, safety, and privacy checks

State the checks required before completion. These may include verifying required fields, checking calculations, preserving originals, citing key sources, identifying uncertainty, or confirming that output access is appropriate.

The skill must behave as a reasonable user would expect from its description. Do not create instructions that facilitate unauthorized access, conceal material actions, misrepresent evidence, bypass consent, exfiltrate sensitive information, damage systems, or produce deceptive outputs.

### Failure behavior

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or reference:** Explain what could not be verified and offer an alternative method if one is safe.
- **Ambiguous request:** Make a low-risk assumption only when it does not materially change the outcome; otherwise ask.
- **Validation failure:** Do not present the work as complete. Correct it, report the issue, or request guidance.
- **High-impact action:** Pause for confirmation before external, irreversible, costly, or sensitive actions.

### Examples

Use a small number of generalized examples only when they teach a distinct pattern. Examples should show the shape of good reasoning or output, not become brittle substitutes for the actual workflow.

## 6. Review the draft before testing

Read the draft as if encountering it for the first time. Check:

- Is the job coherent and appropriately bounded?
- Does the description make activation conditions clear?
- Are inputs, permissions, outputs, and completion criteria defined?
- Does the workflow explain the reason for meaningful safeguards?
- Does it handle missing information and conflicting sources?
- Does it rely on a specific person’s habits, private access, or local setup?
- Are rules repetitive, overly rigid, or unlikely to change behavior?
- Can a capable AI adapt to normal variation without losing the goal?

Prefer lean instructions over a long list of rules that do not improve outcomes. Repeated capitalized commands or absolute language can signal brittle design unless they protect a genuine safety, authorization, or data-integrity boundary.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user and invite corrections or additions before treating them as the evaluation set.

For each test, record:

- A descriptive test name.
- The user prompt.
- Input files or context, if any.
- The expected result in plain language.
- Objective checks, if suitable.

A portable format is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and identify information that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Design coverage around meaningful situations:

- A typical successful request.
- A request with incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic case that changes the workflow.
- A request that should require approval, privacy protection, or safe refusal, when relevant.

Vary wording, detail level, and user sophistication. Do not simply restate the skill’s own language. Avoid using private information in tests; use fictional or properly anonymized examples that preserve the relevant challenge.

## 8. Run comparable evaluations

When independent runs are available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revised version to the prior version.

Run both conditions under comparable circumstances. If parallel execution is available, start all skill and baseline runs together. This reduces timing distortion and makes the comparison fairer.

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

For every run, preserve the prompt, allowed inputs, outputs, and available metadata such as elapsed time or compute use. Record timing when the environment reports it because some environments do not retain it later.

If independent comparison runs are not available, complete a transparent sanity check instead. Apply the skill to each test case, save the outputs, and ask the user to review them. Do not describe this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While testing is in progress, draft objective checks where they genuinely measure user value. Explain them to the user before relying on them as success criteria.

Good checks are observable, specific, and meaningful. Examples include:

- Required sections or fields are present.
- A generated file opens and follows the requested format.
- Calculated values match a known source within an agreed tolerance.
- The output identifies missing mandatory inputs.
- Important claims include approved source references when required.

Use a stable grading record such as:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests it before finalization."
    }
  ]
}
```

Use programmatic checks when practical because they are repeatable and reusable. Do not force numerical metrics onto subjective work. Tone, writing quality, aesthetics, strategic value, and practical usability often require informed human review.

## 10. Review results with a human

Present outputs and measurements through any available review method. A review interface is useful when it allows the user to inspect each test, compare configurations, and leave feedback. If no interface is available, present results clearly in conversation or as accessible files.

For each case, show:

- The original prompt and relevant inputs.
- The skill output and comparison output, if available.
- Objective grades and supporting evidence.
- Timing or resource information, if available.
- A clear place for feedback.

Ask focused review questions:

- Which output would you trust in normal use, and why?
- What was missing, misleading, or hard to use?
- Did the skill add steps or detail that did not help?
- Would this work for similar requests with different wording or data?

Empty feedback can indicate that a specific result is acceptable, but it does not prove the skill is complete. Consider feedback alongside actual outputs and evaluation results.

## 11. Analyze beyond aggregate scores

When possible, aggregate pass rate, time, resource use, and variation across tests. Place the revised skill before the comparison condition in reports for easier reading.

Then inspect patterns that summary metrics may hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not demonstrate the skill’s contribution.
- **High variation:** Similar runs differ substantially, suggesting ambiguity, instability, or unreliable instructions.
- **Quality-cost tradeoffs:** The skill improves quality but requires disproportionate time or resources.
- **Concentrated failures:** Several failures may share one cause, such as unclear source selection or missing output guidance.
- **Unproductive work:** Execution traces show redundant planning, repeated research, or unnecessary formatting.
- **Repeated reconstruction:** Multiple runs independently create the same helper procedure, showing that a reusable asset may help.

A small evaluation set is evidence, not proof. Use it to guide the next revision.

## 12. Improve without overfitting

Base revisions on user feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from complaints. If a test output fails to distinguish sourced information from assumptions, do not add a rule that merely names the test. Clarify the broader behavior: when sources are incomplete or mixed, separate verified information, assumptions, and unresolved gaps.

Apply these principles:

1. **Fix causes, not examples.** Design for future requests, not only current tests.
2. **Keep instructions lean.** Remove guidance that does not improve results or causes wasted effort.
3. **Explain intent.** State how an action protects correctness, usability, privacy, or safety.
4. **Bundle assets only when justified.** Add scripts, templates, or references when repeated work demonstrates their value.
5. **Preserve useful behavior.** Do not lose outcomes users already value while fixing another issue.
6. **Expand coverage gradually.** Add a test only when it represents a meaningful category of failure.

After revision, rerun the evaluation set in a new iteration. Use the same baseline policy unless the user agrees a different comparison is more meaningful. Show changes alongside prior outputs when possible, collect feedback, and repeat until improvement levels off.

Stop when the user is satisfied, objective requirements are reliably met, feedback is consistently positive, further changes do not yield meaningful gains, or remaining problems require a product decision or unavailable capability rather than better instructions.

## 13. Optional blind comparison

For a more rigorous qualitative comparison, use a blind review. Give an independent evaluator two outputs without revealing which skill version produced each one. Provide a shared rubric, record the evaluation, and reveal the mapping only afterward.

Blind comparison is useful when two versions have similar numerical results, when presentation quality matters, or when a decision has material importance. Evaluate role-relevant correctness, completeness, clarity, adherence to constraints, safety, and practical usability. Analyze why one output was preferred before revising the skill.

## 14. Optimize activation behavior

After the workflow itself is stable, improve the short description that helps an AI decide whether to use the skill.

Create a realistic set of activation queries with both cases that should activate the skill and difficult near-misses that should not. Use substantive requests where consulting the skill would help; very simple one-step requests may be handled directly even if the description is relevant.

Positive cases should vary in phrasing and context:

- Formal and casual wording.
- Requests that name the task and requests that imply it.
- Common and less common valid uses.
- Requests where a related skill might compete but this skill is the better fit.

Negative cases should be genuine near-misses, not obviously unrelated requests. They should share terms or concepts with the skill but require another kind of work, another capability, or conditions that make this skill inappropriate.

```json
[
  {
    "query": "I need a concise leadership update from these project notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what project reporting is and why teams use it?",
    "should_trigger": false
  }
]
```

Review the query set with the user before using it. If repeated activation testing is available, separate queries used to improve the description from held-out queries used to select the final version. Choose the description that works best on held-out cases, not simply the one that fits the examples used during editing.

A good description says what the skill does and when it applies. It should cover realistic user language without making claims broader than the skill can support.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for ordinary use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately represents activation conditions and scope.
- Instructions do not rely on private conventions, personal access, or undeclared capabilities.
- Scripts, references, and assets are present, clearly named, and documented.
- No credentials, private records, identifiers, confidential examples, or sensitive test material are included.
- The package stays within intended authorization and access boundaries.
- The user can install, access, or adapt it in their chosen environment.
- Test materials are retained only when they are safe and useful for future maintenance.

Provide a short handoff note explaining what the skill does, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has:

- A clear, bounded job.
- A description that routes appropriate requests.
- Instructions that handle normal variation.
- Explicit behavior for uncertainty, privacy, authorization, and high-impact actions.
- Outputs and formats that match user needs.
- Evidence from realistic use that it improves results or supports a valuable workflow.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable, understandable workflow that helps an AI make better decisions and deliver better results for real recurring work.

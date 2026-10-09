---
name: create-an-ai-skill
description: Design, test, improve, evaluate, and package reusable AI skills through a practical, user-centered iteration workflow.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, improve an existing one, evaluate whether a skill helps, or optimize when it activates. A skill is a focused set of instructions, with optional scripts, references, templates, and tests, that helps an AI perform a recurring job reliably.

The core loop is:

1. Understand the intended job and its limits.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Review outputs with the user and measure objective requirements where useful.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and generalizes beyond the tests.
7. Optionally improve the description that determines when the skill is used.
8. Package and hand off the completed skill.

Do not assume every project needs the full loop. Some users want a quick collaborative draft; others need a rigorous comparison. Determine where the user is and help them take the next useful step.

## Communication principles

Match the user’s technical knowledge and vocabulary. Use plain language by default. Words such as *evaluation* and *benchmark* may be helpful, but briefly define them if needed. Do not use terms such as “JSON,” “assertion,” or “schema” without explanation unless the user clearly understands them.

Explain why important questions matter. For example:

> What should a successful result look like: an answer in chat, a structured report, a file, or an action? This determines how the skill should validate completion.

Keep the user involved at meaningful decision points:

- Confirm the intended job before writing a large instruction set.
- Ask before introducing restrictive scope rules, required tools, approval steps, or irreversible actions.
- Share proposed test cases before treating them as the evaluation set.
- Let human review lead for subjective qualities such as usefulness, tone, visual design, or creative judgment.
- Be flexible if the user explicitly prefers an informal, low-testing collaboration.

When working with private communications, records, or files about people, first confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Omit unrelated personal details, preserve consent and privacy expectations, and keep outputs within the user’s appropriate access boundary.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea such as: “I need a reusable workflow for preparing project updates.” Start with discovery, then produce a draft.

### B. Existing skill

The user already has instructions and wants them edited, simplified, tested, or improved. Read the current instructions before proposing changes. Preserve the established name and identity unless the user asks to rename it.

If the installed or supplied version may be read-only, work from a writable copy. Preserve the original until the user accepts the revision.

### C. Workflow demonstrated in the conversation

The user may say, “Turn what we just did into a skill.” Extract what you can from the conversation before asking questions:

- Inputs and sources used.
- Tools or capabilities used.
- Sequence of decisions and actions.
- Corrections and preferences the user supplied.
- Input and output formats.
- Acceptance criteria.
- Situations that caused the workflow to change direction.

Summarize the inferred workflow and list gaps for confirmation. Do not silently turn a one-time workaround into a universal rule.

### D. Evaluation or optimization request

The user may have a finished-looking skill and want to know whether it actually improves outcomes. Start with test design, evaluation, and evidence-based revision. Do not rewrite merely because a rewrite is possible.

## 2. Capture intent and scope

Before drafting, gather enough information to define a coherent job. Adapt these questions to the context instead of asking them mechanically.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What requests, wording, or contexts should cause the skill to be used?
3. **Inputs:** What information, files, examples, systems, and permissions may it use?
4. **Outputs:** What should it produce, modify, or recommend? Is there a required format?
5. **Success:** How will the user know the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask a question, pause for approval, or decline?
7. **Variations:** What normal variants, difficult cases, or exceptions materially change the work?
8. **Dependencies:** Does it require a particular capability, reference, template, script, or approved data source?
9. **Testing:** Should realistic test requests be used to verify the skill?

Suggest testing by default when the result is objectively checkable, used repeatedly, consequential, or dependent on a fixed procedure. Subjective work may benefit more from representative examples and human review than numerical scoring.

Offer choices when they reduce ambiguity:

- “Should the AI make a best effort with missing information, or stop and ask?”
- “Should the default output be concise, detailed, or selected by the user?”
- “May it use any available source, or only sources the user explicitly approves?”
- “Should it prepare a draft only, or take an external action after approval?”

### Research before drafting

If approved documentation, comparable skills, domain standards, or relevant references are available, examine them before drafting. Research should reduce user effort, not override the user’s authority over requirements.

Use research to identify:

- Existing conventions and required output standards.
- Constraints of an available system, file type, or interface.
- Reusable patterns for similar work.
- Safety, privacy, compliance, and approval requirements.

If information conflicts or remains uncertain, surface the uncertainty. Do not fill a consequential gap with an unmarked assumption.

## 3. Choose the skill structure

Keep a skill focused enough that users and the AI can predict what it does. A skill can support variants of one job, but separate unrelated jobs when they have different audiences, permissions, sources of truth, or completion criteria.

A typical package may contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed documentation
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help route the request.
2. **Core instructions:** The normal workflow used whenever the skill applies.
3. **Supporting resources:** References, templates, or scripts loaded only when relevant.

Keep the core instructions readable. If they become too long, move specialized details into clearly named references and state exactly when each should be consulted. Give large reference files a navigation section or table of contents.

For a skill with domain variants, keep a common selection workflow in the core file and place variant-specific guidance in separate references. The AI should load the relevant variant, rather than treating every variant as required context.

### Use scripts only for repeatable work

Bundle a helper script when test runs show the AI repeatedly reconstructing the same deterministic procedure, such as validating files, converting formats, generating a standard report, or checking calculations.

A script is worth bundling when it is:

- Deterministic or easier to validate than a natural-language process.
- Reused across multiple requests.
- Safer or less error-prone than repeated manual reconstruction.
- Clearly within the user’s approved authority and technical environment.

Document what the script does, its inputs and outputs, failure behavior, and when not to use it. Do not add automation simply because it is possible.

## 4. Write the skill

Use clear, imperative language. Explain the reason behind important instructions, especially where a rule prevents a predictable failure. AI systems generally perform better when they understand the goal and tradeoff than when given an unexplained list of rigid prohibitions.

A useful skill commonly includes the following sections.

### Purpose and scope

State the job, intended use, and boundaries. Make clear whether the skill creates an answer, produces a file, changes data, takes an external action, or guides the user through a process.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State what to do when something required is missing.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If an approved source is unavailable, ask for an export or produce a draft clearly marked as incomplete.
```

### Workflow

Describe the normal sequence of actions and meaningful decision points:

1. Inspect the request and available inputs.
2. Clarify only information that would materially change the result.
3. Gather evidence from approved sources.
4. Perform the task with an appropriate method.
5. Check the result against requested format and success criteria.
6. Present the result, assumptions, and unresolved limitations.

Use conditional rules rather than trying to list every possible edge case:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite, publish, or materially change important work, explain the impact and request approval before proceeding.
```

### Output format

Define an exact template when consistency matters.

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

Do not impose a rigid shell when the task depends on contextual adaptation. In that case, state goals, quality criteria, and short examples instead.

### Quality, safety, and privacy checks

Specify checks needed before completion. These might include validating required fields, verifying calculations, identifying the source for important claims, preserving original data, or clearly flagging uncertainty.

The skill must behave in a way users would reasonably expect from its description. Do not create instructions that conceal actions, bypass authorization, extract confidential information, damage systems, or facilitate unauthorized access.

For person-related material, use only information relevant to the legitimate task. Avoid unsupported personal inferences and sensitive details. In hiring or assessment work, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance.

### Failure behavior

Describe general recovery rules:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or reference:** Explain what could not be checked and offer an alternate method.
- **Ambiguous request:** Make a low-risk assumption only if it will not materially affect the outcome; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, report the issue, or request guidance.
- **Permission-sensitive action:** Pause for approval before an irreversible, external, or high-impact step.

### Examples

Include a small number of generalized examples only when they teach a distinct pattern. Examples should demonstrate reasoning and output shape, not replace adaptable instructions with narrow test-specific rules.

## 5. Write a strong description

The description is a routing instruction: it helps the AI decide whether the skill applies. It should state both what the skill does and when it should be used.

Cover realistic user wording, including requests that imply the job without naming it directly. A useful description often includes:

- The task or outcome.
- Common contexts or phrases that indicate it applies.
- Important scope limits that prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a status update, leadership summary, progress report, milestone review, or a concise account of risks and next steps, even when they do not say “status report.”
```

Do not put the full procedure in the description. Do not use vague labels such as “help with documents.” Do not make the description so broad that it captures nearby work better handled by another workflow.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description explain when to activate it?
- Are required inputs, permissions, and outputs clear?
- Does the workflow explain why important checks matter?
- Does it state what to do when information is missing?
- Are any rules redundant, brittle, or unlikely to affect outcomes?
- Does it depend on undeclared tools, personal conventions, or private access?
- Does it preserve enough judgment for normal variation?

Prefer a lean, understandable prompt over a long prompt full of rules that do not affect behavior. Repeated absolute language is a warning sign unless it protects a genuine safety, authorization, or correctness boundary.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic initial test prompts. Share them with the user and invite corrections or additions before treating them as the test set.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Supplied files or context.
- Expected outcome in plain language.
- Objective checks, if appropriate.

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

Cover meaningful situations, such as:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or policy-sensitive request.
- A realistic edge case that changes the workflow.
- An approval, privacy, or safety boundary where relevant.

Vary phrasing, detail level, and user sophistication. Do not make tests merely repeat the skill’s wording. Avoid retaining personal scenarios or sensitive content when generalized cases teach the same lesson.

## 8. Run comparisons and preserve evidence

When independent runs are possible, compare the skill with a meaningful baseline.

- **New skill:** Run each test with the skill and without a specialized skill.
- **Existing skill:** Save an unchanged snapshot before editing, then compare the revised version with the original or another user-approved baseline.

Start skill and baseline runs under comparable conditions. If the environment supports parallel runs, launch both configurations for all test cases at the same time. This reduces avoidable timing differences.

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

For each test, preserve the prompt, inputs, outputs, and available run metadata. Record elapsed time and resource-use information immediately when the environment reports it, because some systems do not retain those notifications.

If independent or parallel agents are unavailable, do a transparent sanity check: follow the skill for each test request, save outputs, and ask the user to review them. Do not claim this is a rigorous baseline comparison. In constrained environments, prioritize qualitative review over artificial metrics.

## 9. Define and grade objective checks

While test runs are underway, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are observable, meaningful, and specific:

- Required sections are present.
- A produced file opens and contains required fields.
- Calculations match an approved source within an agreed tolerance.
- The output identifies missing mandatory inputs.
- Important claims include required sources or citations.

Record each result with clear text, a pass/fail outcome, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section lists unavailable data points and requests them."
    }
  ]
}
```

Use programmatic checks when practical. They are more repeatable than visual inspection and can be reused in later iterations. Do not force quantitative checks onto subjective work such as writing quality, aesthetics, strategic judgment, or tone; these need human evaluation.

## 10. Review results with a human

Before making major revisions based solely on internal analysis, give the user an accessible way to inspect representative outputs. Use an available review interface when one exists; otherwise present outputs in the conversation or as files the user can access.

For each test case, show:

- The prompt and relevant input context.
- The skill output and comparison output, if available.
- Objective grades and evidence.
- Timing or resource data, if available.
- A place for feedback.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, or hard to use?
- Did the skill add work or detail that was not valuable?
- Would this work for similar requests with different wording or data?

Empty feedback often means a case was acceptable, but it is not proof that the skill is solved. Consider the outputs, grades, and resource tradeoffs as well.

## 11. Analyze results beyond pass rates

Aggregate results where possible: pass rates, average time, average resource use, and variation. Present the revised skill before its comparison condition so the report is easy to scan.

Then examine patterns that summaries can hide:

- **Non-discriminating checks:** Both configurations pass, so the check does not reveal the skill’s value.
- **High variation:** Similar runs differ substantially, suggesting ambiguity, instability, or unreliable instructions.
- **Tradeoffs:** Quality improves, but time or resource use rises beyond the value gained.
- **Failure concentration:** Multiple failures share a root cause, such as unclear source selection or missing output guidance.
- **Unproductive work:** Execution traces reveal repeated planning, unnecessary research, or redundant formatting.
- **Repeated reconstruction:** Several runs independently build similar helpers, suggesting a reusable script or template would help.

Use small benchmarks as evidence for a next revision, not as proof of universal performance.

## 12. Improve without overfitting

Base revisions on feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from complaints. If one output fails to distinguish verified facts from assumptions, do not add a rule mentioning only that one test. Explain the broader condition: when sources are incomplete or mixed, separate confirmed information from assumptions and missing evidence.

Use these principles:

1. **Fix causes, not examples.** Design for future requests, not only the current tests.
2. **Keep instructions lean.** Remove guidance that does not change behavior or causes wasted effort.
3. **Explain intent.** State how a step protects accuracy, usability, privacy, or safety.
4. **Add reusable assets only when justified.** Bundle scripts, templates, and references when repeated work demonstrates their value.
5. **Preserve useful behavior.** Do not erase features the user already values.
6. **Expand coverage gradually.** Add tests for real classes of failure, not every isolated incident.

After revision, rerun the test set in a new iteration. Keep baseline policy consistent unless the user agrees that another comparison is more useful. Where possible, show prior outputs alongside new outputs to make changes visible.

Stop when one or more conditions apply:

- The user says the skill is ready.
- Meaningful test cases receive consistently positive or empty feedback.
- Objective requirements are reliably met.
- Further revisions no longer produce meaningful gains.
- Remaining gaps require unavailable information, a missing capability, or a product decision rather than better instructions.

## 13. Optional blind comparison

When two versions appear close and the decision matters, use blind comparison. Give an independent evaluator two outputs without identifying which version produced which output. Ask it to judge against a shared rubric, then reveal the mapping after the evaluation is recorded.

Blind comparison is helpful when:

- Versions have similar objective scores but visibly different quality.
- Reviewers may favor a newer version by default.
- The decision has material cost or impact.

Use a user-centered rubric: correctness, completeness, clarity, constraint adherence, safety, and practical usability. Analyze why one output was preferred before changing the skill again.

## 14. Optimize activation behavior

Optimize the description only after the workflow itself is useful. Create a realistic query set with both cases that should activate the skill and nearby cases that should not.

Use a roughly balanced set of substantive requests. Simple one-step requests are poor activation tests because an AI may handle them directly without consulting a specialized skill, even if the description is relevant.

Positive cases should vary:

- Formal and casual language.
- Direct names for the task and indirect descriptions of the need.
- Common and less common valid use cases.
- Cases where related skills might compete but this one should be selected.

Negative cases should be difficult near-misses, not obviously irrelevant requests. They should share concepts or keywords but belong to another job, need a different capability, or lack the conditions that make this skill useful.

```json
[
  {
    "query": "I need a concise leadership update from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what project status reports are used for?",
    "should_trigger": false
  }
]
```

Review the activation set with the user before relying on it. If the environment supports repeated activation testing, separate queries used to improve the description from held-out queries used to choose the final wording. Select the description by held-out performance to reduce overfitting.

Show the user the before-and-after description and report the results. Keep the final description honest about the skill’s scope.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states when the skill applies.
- Instructions do not depend on private conventions, personal access, undeclared tools, or hidden assumptions.
- References and scripts are present, clearly named, and documented.
- No credentials, personal data, private identifiers, confidential files, or sensitive examples are included.
- Required capabilities and known limitations are clear.
- Test materials are included only when safe and useful to retain.
- The user can install, access, or adapt the package in their chosen environment.

Provide a short handoff note that explains what the skill does, what it needs, how to test it after installation, and any important limitations.

## Final readiness gate

A skill is ready when it has:

- A clear, bounded job.
- A description that routes appropriate requests.
- Instructions that handle normal variation and important failure modes.
- Explicit boundaries for authorization, privacy, uncertainty, and high-impact actions.
- Evidence from realistic use that it improves outcomes or provides dependable value.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for the user’s recurring work.

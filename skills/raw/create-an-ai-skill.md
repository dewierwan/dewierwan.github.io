---
name: create-an-ai-skill
description: Design, test, improve, evaluate, and package reusable AI skills through an evidence-based, user-centered workflow.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, improve an existing one, evaluate whether it helps, or refine when it activates. A skill is a focused set of instructions, plus optional resources, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the intended job and its boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with a person and measure objective requirements where useful.
5. Improve the skill from evidence, not guesswork.
6. Repeat until it is useful, reliable, and not narrowly fitted to a few tests.
7. Optionally improve the description that determines when the skill activates.
8. Package and hand off the finished skill.

Adapt the depth of this process to the user’s goal. Some users want a quick collaborative draft. Others need a rigorous comparison with baselines, formal checks, and several revision rounds. First determine where they are in the loop, then help them take the next useful step.

## Communication principles

Match the user’s technical background. Use plain language by default. Terms such as *evaluation* and *benchmark* are usually acceptable if briefly defined. Explain specialized terms such as *JSON*, *assertion*, *baseline*, or *schema* before relying on them unless the user clearly uses them comfortably.

Ask questions because their answers affect the design, not merely to fill out a checklist. For example:

- “What should a successful result look like: a chat response, a report, a file, or an action?”
- “What information may the skill use, and what should it do if that information is unavailable?”
- “Should it make a reasonable best effort, or pause when a decision could materially change the result?”

Keep the user involved at meaningful decision points. Confirm intended scope before writing extensive instructions, share proposed tests before treating them as representative, and let human judgment guide subjective issues such as writing quality, visual design, and practical usefulness.

When the task involves private communications, records, or personal information, require a legitimate purpose and clear authorization. Use the minimum relevant sources and information, omit unrelated sensitive details, respect consent and reasonable privacy expectations, and keep results within the appropriate access boundary.

## 1. Identify the starting point

Determine which of these situations applies.

### New skill

The user has an idea for recurring work, such as preparing project updates, reviewing structured documents, or transforming approved files. Start with discovery and a first draft.

### Existing skill

The user has a draft or installed skill and wants it edited, simplified, tested, or improved. Read the current instructions before proposing changes. Preserve its established identity, including its name, unless the user explicitly asks to rename it.

If the existing copy may be read-only, make an editable working copy in a user-approved location. Keep the original unchanged until the user accepts the revision.

### Workflow demonstrated in the conversation

The user may ask to “turn this into a skill.” First extract what is already known from the conversation:

- Inputs, files, and approved sources used.
- Sequence of decisions and actions.
- Tools or capabilities needed.
- Corrections and preferences supplied by the user.
- Observed output format and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow and identify gaps for confirmation. Do not quietly convert a one-time workaround into a general instruction without checking that it applies broadly.

### Evaluation or optimization request

The user may already have a plausible skill and want to know whether it actually improves outcomes. Go directly to test design, evaluation, and revision. Do not rewrite a skill merely because a rewrite is possible.

## 2. Capture intent, scope, and boundaries

Gather enough information to define a coherent job. Start with the questions whose answers matter most; do not force every question when the conversation already answers it.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What user requests, phrasing, or situations should cause it to be used?
3. **Inputs:** What information, files, examples, systems, references, and permissions may it use?
4. **Outputs:** What should it produce, change, or communicate? Is there a required format?
5. **Success criteria:** How will the user decide that the result is correct, useful, safe, and complete?
6. **Boundaries:** What should it not do? When should it ask a question, request approval, decline, or return work to the user?
7. **Variations:** What common cases, difficult cases, or meaningful exceptions should it handle?
8. **Dependencies:** Does it need a particular tool capability, template, script, reference source, or user-provided access?
9. **Testing:** Should it be tested with realistic example requests?

Recommend tests when outputs can be objectively checked, the workflow is consequential, the skill will be reused often, or the user needs evidence that a revision improves on an earlier version. For highly subjective work, recommend representative human review instead of weak numerical proxies.

Offer useful choices when requirements are unclear:

- “Should missing information cause a question, a clearly labeled assumption, or an incomplete draft?”
- “Should the output be concise, detailed, or selectable by the user?”
- “Should the skill work with any source the user provides, or only specifically approved sources?”
- “Does this action need confirmation because it is external, irreversible, or high impact?”

## 3. Research and inspect available context

Before drafting, inspect relevant user-approved materials when they would reduce uncertainty: documentation, templates, comparable skills, file specifications, standards, or existing evaluation data. Use available research capabilities in parallel when practical, but do not research private material without authorization.

Research should reduce burden on the user, not replace their authority over requirements. Use it to identify:

- Existing conventions or output standards.
- Constraints imposed by a file format, system, or available capability.
- Reusable patterns for similar tasks.
- Safety, privacy, compliance, or approval requirements.
- Existing tests or feedback that should inform a revision.

If sources conflict or important requirements remain uncertain, present the uncertainty rather than inventing a rule.

## 4. Choose a maintainable skill structure

Keep a skill focused enough that users and AI systems can predict its purpose. A skill may support related variants, but unrelated jobs should be split when they have different audiences, permissions, source-of-truth rules, or definitions of completion.

A typical package can contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional supporting documentation
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional tests and evaluation material
```

Use progressive disclosure:

1. **Metadata:** a short name and description used to decide whether the skill is relevant.
2. **Core instructions:** the workflow needed for normal use.
3. **Supporting resources:** detailed references, templates, and scripts loaded only when relevant.

Keep core instructions readable. If they become too long, move domain-specific detail into clearly named supporting files and state exactly when to consult each one. Large reference files should include a navigation section or table of contents.

For a skill with several variants, use a shared selection workflow plus separate references for each variant. The AI should load only the relevant material rather than carrying every variant into every request.

### Bundle resources only when they earn their place

If several test runs independently recreate the same helper process—such as validation, document generation, conversion, or formatting—consider bundling a reusable script or template. A resource is worthwhile when it is repeatable, easier to verify than free-form reasoning, safe within the user’s authority, and likely to be reused.

Document each resource’s purpose, inputs, outputs, limitations, and when not to use it. Do not automate actions that would surprise the user or extend beyond approved permissions.

## 5. Write the skill instructions

Write in clear imperative language and explain the reason for important steps. AI systems generally follow guidance better when they understand what a step protects: correctness, usability, privacy, safety, or efficient use of time.

Avoid long lists of unexplained absolute rules. Strong boundaries are appropriate for authorization, safety, privacy, data integrity, and irreversible actions. Elsewhere, give the AI enough judgment to adapt to normal variation.

A useful skill usually contains the following sections as applicable.

### Purpose and scope

State the job, intended outcome, intended users, and limits. Make clear whether the skill provides advice, produces an artifact, modifies a file, performs an external action, or guides a user through a process.

### Inputs and prerequisites

List required inputs, permitted sources, required capabilities, and optional context. Specify what happens when a required input is missing.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If the source is unavailable, ask for an export or provide a draft clearly marked as incomplete.
```

### Workflow and decision points

Provide the normal sequence and its important branches. A durable pattern is:

1. Inspect the request and available inputs.
2. Clarify only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the output against requested format and success criteria.
6. Present results, assumptions, sources, and unresolved limitations.

Use conditional rules for meaningful variation:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested change could overwrite important work or send information externally, explain the impact and request confirmation first.
```

### Output format

Use an exact template when consistency matters. For example:

```markdown
# [Title]

## Summary
[One short paragraph]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing input]
```

Do not impose rigid formatting when contextual adaptation is more valuable. In those cases, define goals, required content, and one or two short generalized examples instead.

### Quality, privacy, and safety checks

State the checks needed before completion. Examples include validating calculations, confirming required fields, preserving originals, citing key sources, separating verified facts from assumptions, and flagging unresolved uncertainty.

The skill must behave in ways a user would reasonably expect from its description. Do not create instructions that hide actions, bypass access controls, extract confidential information, damage systems, or facilitate unauthorized access. For people-related work, focus on role-relevant evidence, stated criteria, and appropriate access; avoid irrelevant personal details or unsupported labels.

### Failure behavior

Describe recovery in general terms:

- **Missing or conflicting inputs:** identify the gap and ask a focused question.
- **Unavailable tool or source:** explain what cannot be verified and offer an approved alternative.
- **Ambiguous request:** make a low-risk assumption only if it does not materially affect the result; otherwise ask.
- **Failed validation:** do not present the output as complete; correct it, label the limitation, or seek guidance.
- **Sensitive or high-impact action:** pause for confirmation before acting.

## 6. Write an effective description

The skill description is a routing instruction. It should state both **what the skill does** and **when it should be used**. Include realistic request contexts, including cases where the user implies the job without naming it.

A good description includes:

- The intended task or outcome.
- Common contexts or user language that indicate the task.
- Important scope limits that prevent costly false activation.

Example:

```text
Create clear project status reports from approved updates and source material. Use for requests involving progress summaries, leadership updates, milestone reviews, risks, blockers, or next steps, even when the user does not say “status report.”
```

Do not place the whole workflow in the description. Avoid vague labels such as “help with documents,” but also avoid making the description so broad that it captures nearby work better handled by another skill.

## 7. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description explain when to activate it?
- Are inputs, outputs, permissions, and dependencies clear?
- Does the workflow explain why important checks exist?
- Does it handle missing information and tool failure honestly?
- Are there repeated rules, unnecessary constraints, or brittle wording?
- Does it assume a particular person’s habits, access, tools, or vocabulary?
- Does it keep private information and external actions within approved boundaries?
- Does a capable AI have enough discretion to handle normal variation?

Prefer a lean instruction set over one filled with rules that do not improve outcomes. If execution traces later show that a section causes wasted planning or redundant work, revise or remove it.

## 8. Design realistic tests

After the draft is stable enough to test, create two or three realistic prompts. Share them with the user and invite corrections or additions before relying on them.

For each test, record a descriptive identifier, prompt, input files or context, expected outcome, and objective checks if appropriate.

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

Cover meaningful variation:

- A typical successful request.
- An incomplete or ambiguous request.
- A format-sensitive, policy-sensitive, or evidence-sensitive request.
- A realistic case that changes the workflow.
- A request requiring confirmation or safe refusal, when relevant.

Avoid tests that merely repeat the skill’s wording. Vary phrasing, detail level, and user familiarity. Avoid private or one-off scenarios unless they are fully authorized and necessary; test the broader challenge instead.

## 9. Run comparisons and preserve evidence

When independent execution is available, compare the skill to a meaningful baseline.

- For a new skill, run each test with the skill and without it.
- For a revision, save an unchanged snapshot before editing, then compare the revised skill with the earlier version.

Launch the skill and comparison runs under equivalent conditions. When parallel execution is available, start all configurations in the same evaluation round so conditions are comparable.

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

For each run, save the prompt, permitted input files, outputs, and available metadata such as elapsed time and resource use. Capture timing immediately if the environment reports it only at completion.

If independent comparison is unavailable, run a transparent sanity check: follow the skill for each test, preserve outputs, and ask the user to review them. Do not describe this as a rigorous baseline comparison.

## 10. Define, grade, and interpret checks

While runs are in progress, draft objective checks if they genuinely measure value. Explain them to the user before treating them as success criteria.

Good checks are observable and meaningful, for example:

- Required sections or fields are present.
- A produced file opens correctly.
- Calculations match an approved source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- Required citations, source notes, or approval prompts are included.

Record each check with clear wording, a pass/fail result, and supporting evidence:

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

Use scripts for checks that can be programmatically verified. They are faster, more repeatable, and reusable across iterations. Do not force numerical checks onto subjective work such as tone, visual quality, strategic judgment, or creative usefulness. Those need informed human review.

Aggregate available pass rates, time, resource use, and variation. Then inspect patterns the totals may hide:

- Checks that pass equally with and without the skill may not measure its value.
- High variation can indicate ambiguity, an unstable environment, or unreliable instructions.
- A quality gain may not justify excessive time or resource cost.
- Several failures may share one cause, such as unclear source selection.
- Repeated helper work may justify a script or template.

## 11. Review results with a human

Present outputs and measurements through an available review interface or, if necessary, directly in the conversation or accessible files. For each test, show the original prompt, relevant inputs, each output, grades and evidence, and available timing or resource data.

Ask focused questions:

- “Which output would you trust in normal use, and why?”
- “What was missing, misleading, or difficult to use?”
- “Did the skill add work or detail that was not valuable?”
- “Would this still work with different wording, data, or constraints?”

Human review should happen before making speculative corrections based only on the author’s preferences. Empty feedback can mean a test is acceptable, but it is not proof that the skill is complete.

## 12. Improve without overfitting

Revise from the combined evidence of feedback, outputs, execution behavior, and checks. Change the smallest part likely to address the underlying cause.

Generalize from complaints. If one output fails to distinguish verified facts from assumptions, do not add a rule tied only to that test. Clarify the broader rule: when evidence is incomplete or mixed, separate verified information, assumptions, and unresolved questions.

Use these principles:

1. Fix causes, not examples.
2. Keep instructions lean and remove unproductive guidance.
3. Explain intent rather than relying on rigid wording.
4. Add reusable resources only when repeated work proves their value.
5. Preserve behavior users already value.
6. Add tests only for real categories of failure.

After revision, rerun the full test set in a new iteration and use the same baseline policy. Show prior outputs alongside the new ones when possible.

Stop when the user says the skill is ready, feedback is consistently positive across meaningful tests, objective requirements are reliably met, further edits produce no meaningful gain, or remaining issues require a product decision or unavailable information rather than better instructions.

## 13. Optional blind comparison

For a rigorous comparison between two versions, provide their outputs to an independent evaluator without identifying which version created each one. Ask for judgment against a shared rubric, then reveal the mapping after the evaluation is recorded.

Use blind comparison when versions have similar formal results but differ in qualitative value, when a decision has material consequences, or when a newer version may be favored merely because it is newer. Evaluate correctness, completeness, clarity, adherence to constraints, safety, and practical usability.

## 14. Optimize activation after the workflow works

Only optimize the description after the underlying skill is useful. Create a realistic, balanced set of activation queries: some that should use the skill and some difficult near-misses that should not.

Positive queries should vary in wording, formality, implied versus explicit intent, and common versus uncommon valid cases. Negative queries should share concepts or keywords but belong to a different job, require another capability, or lack the conditions that make this skill appropriate.

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

Review the query set with the user. If evaluation tools support repeated trials, separate the examples used to improve the description from held-out examples used to choose it. Select based on held-out performance to reduce overfitting.

Remember that an AI may handle a simple one-step request directly even when a specialized skill matches. Use substantive activation tests where consulting the skill would offer real value.

## 15. Package and hand off

Package the core instructions and only the resources needed for ordinary use. If packaging tools are available, use the user’s chosen format and provide the resulting artifact or installation location.

Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on undeclared tools, private conventions, or personal access.
- Scripts, references, and assets are present, clearly named, and documented.
- No credentials, private identifiers, confidential records, or sensitive examples are included.
- The user can install, access, or adapt the skill in their chosen environment.
- Retained tests are safe and useful to distribute.

Provide a short handoff note explaining what the skill does, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an honest description that routes suitable requests, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user needs.

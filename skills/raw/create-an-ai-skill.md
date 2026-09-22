---
name: create-an-ai-skill
description: Create, test, improve, evaluate, and package a reusable AI skill from a new idea, an existing draft, or a demonstrated workflow, using realistic reviews and evidence to improve reliability without overfitting.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, revise an existing skill, test whether it improves outcomes, or improve when it activates. A skill is a focused set of instructions, plus optional resources, that helps an AI complete a recurring kind of work consistently.

The core loop is:

1. Define the job and its boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements where useful.
5. Improve the skill from evidence.
6. Repeat until the skill is useful, reliable, and not narrowly fitted to the test cases.
7. Optionally improve the description that determines when the skill should activate.
8. Package and hand off the final skill.

Identify where the user is in this loop and help with the next useful step. Do not force a full benchmark when the user wants a quick collaborative draft. Conversely, recommend testing when the skill will be reused, affects important decisions, changes files or systems, or has objectively checkable outputs.

## Communication principles

Use plain language by default and match the user’s technical level. Briefly explain terms such as *evaluation*, *benchmark*, *structured data*, or *assertion* if they are needed. Avoid assuming that a user knows programming terminology, file formats, or automation concepts.

Keep the user involved in decisions that affect scope, access, risk, or success criteria:

- Confirm the intended recurring job before writing extensive instructions.
- Explain why missing information matters before asking a question.
- Share proposed tests before treating them as the evaluation standard.
- Let human review lead for subjective quality, including writing quality, design, strategy, and tone.
- Do not assume a particular tool, file path, operating system, account, or development environment.

If the skill will access private communications, records, customer data, employee information, or other sensitive material, first establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Exclude unrelated personal details, honor consent and privacy expectations, and keep outputs within the user’s authorized access boundary.

## 1. Determine the starting point

First identify which situation applies.

### New skill

The user has an idea for recurring work. Start with discovery, then create a first draft.

### Existing skill

The user has a draft, an installed package, or a working instruction set that needs revision, simplification, testing, or better triggering. Preserve its established name and identity unless the user asks to rename it. Read the existing instructions before proposing changes.

If the existing copy cannot be edited directly, make an editable working copy in a user-approved location. Keep the original unchanged until the user accepts the revision.

### Workflow demonstrated in the conversation

The user may ask to turn a process already performed into a skill. Extract what can be learned from the conversation first:

- Inputs, files, and approved sources used.
- The sequence of actions and decisions.
- Corrections or preferences supplied by the user.
- Output forms that proved useful.
- Failure points, exceptions, and validation steps.

Summarize the inferred workflow and ask the user to confirm gaps. Do not convert a one-time workaround into a general requirement without confirming that it applies broadly.

### Evaluation or optimization request

The user may have a skill that appears complete and wants evidence that it helps. Begin with test design and comparison rather than rewriting it unnecessarily.

## 2. Capture intent and scope

Gather enough information to define one coherent job. Do not ask every question mechanically; prioritize missing details that materially change the design.

Use questions such as:

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Trigger:** What requests, wording, or contexts should activate it?
3. **Inputs:** What information, files, systems, examples, or approved sources can it use?
4. **Outputs:** What should it produce, modify, or recommend? Is a specific format needed?
5. **Success:** What makes an output correct, useful, complete, or safe?
6. **Boundaries:** What should it not do? When should it ask, stop, or hand work back to the user?
7. **Variation:** What common variants, difficult cases, or exceptions matter?
8. **Dependencies:** Does it need a particular capability, template, reference, script, or permission?
9. **Testing:** Should it be evaluated with representative requests?

Useful follow-up choices include:

- “When information is missing, should the skill make a clearly labeled best effort or ask before continuing?”
- “Should the result be concise, detailed, structured, or user-selectable?”
- “Which sources are authorized, and which sources should it avoid?”
- “Does this action require approval before it changes a file, sends information, or affects an external system?”

### Research before drafting

When relevant materials are available and authorized, inspect documentation, user-provided examples, comparable skills, output standards, and domain requirements before drafting. Research should reduce burden on the user, not override their requirements.

Use it to identify:

- Existing conventions and required formats.
- Constraints of available tools or file types.
- Reusable patterns and reliable validation methods.
- Privacy, safety, legal, compliance, or approval requirements.

If the evidence conflicts or a requirement remains unclear, state the uncertainty rather than inventing a rule.

## 3. Choose the package structure

Keep a skill focused enough that an AI can predict its purpose and a user can predict its behavior. Separate unrelated jobs when they have different audiences, permissions, sources of truth, or completion criteria.

A portable package might look like this:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional documentation
├── assets/                  # Optional templates or resources
└── evals/                   # Optional test and grading material
```

Use progressive disclosure:

1. **Metadata:** A brief name and description that help route requests.
2. **Core instructions:** The workflow needed for ordinary use.
3. **Resources:** References, scripts, or templates loaded only when relevant.

Keep the core instructions readable. If they become long, move detailed, domain-specific content into clearly named resources and tell the AI exactly when to consult each one. Large references should include a short table of contents or navigation guide.

For a skill with meaningful variants, keep one selection workflow in the core instructions and separate variant-specific guidance into resources. The AI should select the relevant variant instead of reading every possible reference.

### Bundle helpers only when they earn their place

If repeated test runs independently reconstruct the same conversion, validation, report-generation, or cleanup procedure, a reusable helper may be justified. Prefer a script or template when it is deterministic, repeatedly needed, easier to verify, and within the intended permission boundary.

Document each helper’s purpose, inputs, outputs, limitations, and when not to use it. Do not include automation that conceals actions, expands access, overwrites work unexpectedly, or depends on undeclared credentials.

## 4. Write the skill

Write instructions in clear, practical language, usually using imperative phrasing. Explain the reason behind consequential steps: an AI is more likely to adapt well when it understands what a check protects against.

A useful skill commonly includes the following sections.

### Purpose and scope

State the job, intended outcome, and limits. Clarify whether the skill gives advice, creates a file, analyzes approved information, guides a workflow, or takes an approved action.

### Inputs and prerequisites

List required information, approved sources, available capabilities, and optional inputs. Explain what to do when a required input is missing.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or provide a draft that clearly marks unverified sections.
```

### Workflow

Describe the normal sequence and meaningful decision points:

1. Inspect the request and available inputs.
2. Clarify only details that materially affect the result.
3. Gather evidence from authorized sources.
4. Complete the work using the appropriate method.
5. Validate the output against requested requirements.
6. Present the result with assumptions, evidence, and unresolved limitations.

Use conditional rules rather than a long catalog of special cases:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite, disclose, or externally publish important information, explain the impact and request confirmation first.
```

### Output format

Specify a template when consistency is important:

```markdown
# [Title]

## Summary
[Brief overview]

## Findings
- [Finding and supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or needed information]
```

For context-sensitive work, specify quality goals and examples rather than enforcing an inflexible shell.

### Quality, privacy, and safety checks

Name the checks needed before completion. Depending on the job, this can include required fields, calculations, citations, source attribution, preservation of originals, access checks, or clearly flagged uncertainty.

The skill must behave in ways a user would reasonably expect from its description. Do not create instructions to deceive, bypass authorization, extract confidential data, compromise security, or conceal external actions. For sensitive tasks, minimize collection and retention, quote or expose only what is needed, and avoid including unrelated personal details in the output.

### Failure behavior

Define recovery in general terms:

- **Missing or conflicting input:** identify the gap and ask a focused question.
- **Unavailable tool or reference:** explain what cannot be verified and offer a safe alternative.
- **Ambiguous request:** make a low-risk assumption only when it does not materially alter the outcome; otherwise ask.
- **Validation failure:** do not present the result as complete; correct it, label it, or request guidance.
- **High-impact action:** request confirmation before an irreversible, external, or permission-sensitive step.

### Examples

Use a small number of generalized examples only when they teach a distinct pattern. Examples should illustrate judgment and format, not replace reasoning with a list of narrowly memorized cases.

## 5. Write the description for reliable activation

The description is a routing instruction. It should say both what the skill does and when it should be used. Cover realistic user language, including requests that imply the job without naming it exactly.

A strong description includes:

- The expected outcome.
- Common request types or contexts that indicate relevance.
- Important scope limits that prevent costly false activation.

Example:

```text
Create concise project status reports from approved updates and source material. Use for requests involving progress summaries, milestone reviews, risks, dependencies, next steps, or leadership updates, even when the user does not say “status report.”
```

Do not put the full procedure in the description. Avoid vague labels such as “help with documents,” but do not make the description so broad that it captures nearby tasks better handled by another skill.

## 6. Review the draft before testing

Read the skill as a first-time user and auditor. Check:

- Is the job clear, coherent, and bounded?
- Does the description explain when to activate it?
- Are inputs, outputs, permissions, and dependencies explicit?
- Does the workflow handle normal variation and missing information?
- Do consequential instructions explain why they exist?
- Are there repeated, brittle, or low-value rules?
- Does it avoid personal defaults, hidden access assumptions, and tool-specific language?
- Would a capable AI have enough flexibility to solve normal cases well?

Prefer a lean instruction set over an accumulation of rigid commands. Repeated absolute language is a warning sign unless it protects a true safety, privacy, authorization, or correctness boundary.

## 7. Design realistic tests

Once the draft is stable enough to test, create two or three representative prompts. Share them with the user before treating them as the test set. Expand the set after early iterations reveal meaningful new failure categories.

Record each evaluation with a descriptive name, prompt, inputs, expected outcome, and objective checks when appropriate.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates and clearly flag information that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover different meaningful conditions:

- A normal successful request.
- Incomplete or ambiguous input.
- A format- or rule-sensitive request.
- A realistic edge case that changes the workflow.
- A request requiring permission, escalation, or refusal when relevant.

Do not build tests that merely repeat the wording of the instructions. Vary detail, phrasing, and user context. If test materials contain private information, use authorized, minimized, and appropriately protected examples.

## 8. Run and preserve comparisons

When independent execution is available, compare the skill with a meaningful baseline:

- For a new skill, compare a run using the skill with a run without it.
- For an existing skill, preserve an unchanged snapshot and compare the revision with the prior version.

Run all comparison conditions under similar conditions. If parallel execution is available, start skill and baseline runs for every test at the same time. This limits timing distortions and keeps the comparison fair.

Use an iteration structure such as:

```text
workspace/
├── iteration-1/
│   ├── standard-request/
│   │   ├── with-skill/
│   │   └── baseline/
│   └── incomplete-input/
│       ├── with-skill/
│       └── baseline/
└── iteration-2/
```

For each run, retain the prompt, input files, outputs, and available execution metadata such as elapsed time or resource use. Record timing as soon as the environment reports it, because some environments do not preserve it later.

If independent runs are unavailable, perform a transparent sanity check: follow the skill on each prompt, save the results, and ask the user to review them. Do not claim this is a rigorous baseline comparison.

## 9. Define and grade objective checks

While test runs are in progress, write objective checks where they genuinely represent user value. Explain them to the user. Good checks are observable, specific, and meaningful, such as required sections, valid file output, correct calculations, source attribution, or proper identification of missing required inputs.

Use this portable grading shape:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when required source information is absent.",
      "passed": true,
      "evidence": "The final section identifies two unavailable data points and requests them."
    }
  ]
}
```

Use programmatic validation when practical. Scripts are more repeatable than visual inspection and can be reused in later iterations. Do not force numerical checks onto subjective work such as writing style, visual quality, or strategic judgment; these require qualitative human review.

## 10. Review, analyze, and improve

Present outputs and measurements in a review format the user can inspect. Use any available review interface; otherwise provide accessible files or a clear in-conversation comparison.

For each evaluation, show the prompt, relevant inputs, outputs for each condition, objective grades with evidence, and available timing or resource data. Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, excessive, or difficult to use?
- Did the skill add work that was not valuable?
- Would this still work with different wording or data?

Aggregate results when possible, but inspect beyond pass rates. Look for non-discriminating checks that pass everywhere, high-variance results, quality-versus-cost tradeoffs, clustered failures with one root cause, redundant work in execution traces, and repeated reconstruction of the same helper procedure.

Revise from underlying causes, not individual examples. If a test reveals missing source notes, clarify how to distinguish verified information from assumptions whenever evidence is incomplete; do not merely mention the exact test scenario.

Apply these principles:

1. Fix causes rather than test-specific symptoms.
2. Remove guidance that does not improve results or causes wasted work.
3. Explain intent behind important checks.
4. Add scripts, templates, or references only when repeat use justifies them.
5. Preserve behavior the user already values.
6. Add tests only for real categories of failure.

Rerun the test set in a new iteration after meaningful changes. Continue until the user is satisfied, feedback is consistently positive across meaningful cases, objective requirements are reliable, or further changes no longer produce useful improvement.

## 11. Optional blind comparison

For a more rigorous choice between two versions, give an independent reviewer two outputs without identifying their origins. Ask it to apply a shared rubric based on correctness, completeness, clarity, adherence to constraints, safety, and practical usefulness. Reveal which version produced which output only after the judgment is recorded.

Use blind comparison when versions have similar measured results, qualitative judgment is important, or a decision has meaningful cost.

## 12. Optimize activation after the workflow is stable

Only optimize the description after the skill itself is useful. Create a realistic, roughly balanced set of requests that should trigger and should not trigger the skill. Favor difficult near-misses over obviously irrelevant negative cases.

```json
[
  {
    "query": "I need a concise leadership update from these team notes, with risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Explain the purpose of project status reports and when teams use them.",
    "should_trigger": false
  }
]
```

Include formal and casual phrasing, direct and implied requests, common and uncommon valid cases, and adjacent tasks that should go elsewhere. Review the set with the user before using it.

If the environment supports repeated routing tests, separate cases used to improve the description from held-out cases used to select it. Choose the description that performs best on held-out cases, not merely the one that fits the development set. Use substantive requests: very simple tasks may be completed directly without consulting a specialized skill even when the description matches.

Show the before-and-after description and the results before applying the change.

## 13. Package and hand off

Package only the instructions and resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not rely on undeclared tools, private habits, local paths, or special access.
- Scripts and references are present, clearly named, and documented.
- No credentials, private records, personal identifiers, confidential examples, or unnecessary sensitive material are included.
- The package respects access boundaries and does not imply authority the user lacks.
- The user can install or adapt it in their chosen environment.
- Retained test material is safe, authorized, and useful.

Provide a handoff note explaining what the skill does, required capabilities, known limitations, and how to run a simple post-installation check.

## Final readiness gate

A skill is ready when it has a clear job, accurate activation guidance, instructions that handle normal variation, explicit behavior for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not mistake a long instruction file for a reliable skill. The goal is a reusable workflow that helps an AI make sound decisions and deliver better results for the user’s recurring work.

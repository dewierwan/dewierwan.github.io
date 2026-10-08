---
name: create-an-ai-skill
description: Design, test, improve, evaluate, and package reusable AI skills from a new idea, an existing draft, or a demonstrated workflow.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, revise an existing skill, evaluate whether it helps, or improve how reliably it activates. A skill is a focused package of instructions and optional supporting resources that helps an AI perform a recurring job consistently.

The core loop is:

1. Identify the job, boundaries, and current stage.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review representative outputs with a person and measure objective requirements where useful.
5. Improve the skill based on evidence.
6. Repeat until the skill is useful, reliable, and not narrowly fitted to its test prompts.
7. Optionally evaluate and improve the description used to activate the skill.
8. Package and hand off the finished skill.

Adapt the level of rigor to the user’s goals. Some users need a quick collaborative draft; others need repeatable comparisons and documented evidence. Do not force a large evaluation on someone who wants an exploratory session, but explain the tradeoff: less testing provides less confidence that the skill will work across normal variations.

## Operating principles

### Communicate at the user’s level

Use plain language by default. Terms such as *evaluation* and *benchmark* are often understandable, but define them briefly when useful. Do not assume familiarity with technical terms such as structured data, pass/fail checks, data schemas, command-line tools, or automated testing.

Explain why important questions matter. For example:

> What should a successful result look like: a chat response, a structured report, a file, or an approved action? The answer determines how the skill should be written and tested.

Keep the user involved in choices that affect scope, risk, output style, capabilities, permissions, or approval requirements.

### Maintain a visible work plan

If a task tracker, checklist, or planning mechanism is available, create a short plan and keep it current. For a full evaluation cycle, include at least:

- Confirm scope and success criteria.
- Draft or revise the skill.
- Create realistic test cases.
- Run tests and comparison conditions when supported.
- Prepare materials for human review.
- Analyze feedback and measurements.
- Revise and retest.
- Package the final version.

A checklist prevents important steps, especially result preservation and human review, from being skipped. It should not replace judgment.

### Respect authorization, privacy, and user expectations

If the workflow uses private communications, records about people, customer information, operational data, or other non-public material, establish a legitimate purpose and clear authorization first. Use only the minimum relevant sources and information. Omit unrelated sensitive details from outputs, preserve appropriate access boundaries, and respect consent and privacy expectations.

Do not create skills that conceal actions, bypass safeguards, collect information without authorization, facilitate unauthorized access, or otherwise behave in ways a reasonable user would not expect from the description.

## 1. Determine the starting point

Identify which situation applies before deciding how much discovery or testing is needed.

### New skill

The user has an idea for a recurring job, such as preparing operational summaries or validating data files. Start with discovery, then create a first draft.

### Existing skill

The user has a draft, package, or instruction set and wants it simplified, extended, tested, or improved. Read the current version before proposing changes. Preserve its established name and identity unless the user asks to rename it.

If the current copy cannot be edited safely, create an editable working copy in an approved location. Preserve the original unchanged so it can serve as a comparison baseline and recovery point.

### Workflow demonstrated in the conversation

When the user asks to turn an earlier interaction into a skill, extract what is already known before asking repetitive questions:

- Inputs, files, and permitted information sources.
- Actions and capabilities used.
- The sequence of decisions and work.
- User corrections, preferences, and exceptions.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow, label assumptions, and ask the user to confirm important gaps. Do not turn a one-time workaround into a general rule without checking that it should apply broadly.

### Evaluation-only or activation-only request

A user may already have a complete-looking skill and ask whether it works, whether it improves results, or whether it activates in the right situations. Start with test design and evidence gathering. Do not rewrite merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough detail to define a coherent job. Do not ask every question mechanically; begin with unknowns that most affect the design.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What requests, wording, situations, or files should cause it to be used?
3. **Inputs:** What information, files, systems, references, and permissions may it use?
4. **Outputs:** What should it create, return, modify, or recommend? Is a format required?
5. **Success criteria:** How will the user know the result is correct, safe, and useful?
6. **Boundaries:** What should it not do? When should it ask, pause, decline, or hand work back to the user?
7. **Variation:** What common alternatives, difficult cases, or failure conditions matter?
8. **Dependencies:** Does it need a particular capability, template, reference, script, or environment?
9. **Testing:** Should it be tested with representative requests before release?

Useful follow-up choices include:

- Should the skill make a clearly labeled best-effort assumption, or ask when required information is missing?
- Should it provide a concise result, a detailed result, or let the user choose?
- Should it use any accessible source, or only sources explicitly approved by the user?
- Does an external action require confirmation before it is performed?

Recommend test cases when outputs are objectively checkable, the workflow is consequential, or the skill will be used repeatedly. For subjective or creative work, favor representative review over misleading numerical scoring.

### Research before drafting

If relevant documentation, similar skills, reference materials, or domain guidance are available and approved for use, inspect them before drafting. Research should reduce burden on the user, not replace their authority over requirements.

Use research to identify:

- Existing output standards and conventions.
- Constraints imposed by input formats or available capabilities.
- Safe reusable patterns for comparable tasks.
- Approval, privacy, compliance, and audit needs.

When evidence conflicts or a requirement is uncertain, surface the uncertainty. Do not present a guess as a verified rule.

## 3. Choose the package structure

Keep each skill focused enough that its purpose and boundaries are predictable. Support variants of the same job in one skill when they share a workflow and completion criteria. Split unrelated jobs when they have different users, permissions, sources of truth, or definitions of success.

A portable package often follows this layout:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional repeatable helpers
├── references/              # Optional detailed documentation
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata** gives the name and short activation description.
2. **Core instructions** provide the normal workflow.
3. **Resources** hold detailed references, templates, and executable helpers consulted only when relevant.

Keep the core instruction file readable. If it becomes too long, move domain-specific detail into clearly named references and state exactly when each reference should be read. Long reference documents should include useful navigation, such as a table of contents.

For a skill that supports multiple environments or variants, keep shared decision logic in the core instructions and separate the variant-specific details. The AI should select the relevant reference rather than loading every variant by default.

### Bundle deterministic work only when it earns its place

If test runs repeatedly reconstruct the same transformation, validation, or file-generation procedure, consider a reusable script or template. It is especially valuable when it is deterministic, safer, faster, or easier to verify than repeated natural-language reasoning.

Document each resource’s purpose, inputs, outputs, limitations, and when not to use it. Do not add automation simply because it is possible. It must remain within the intended authorization and access scope.

## 4. Write the skill

Write clear, action-oriented instructions. Explain the reason behind important safeguards and quality checks. A capable AI can adapt better when it understands the goal and tradeoff than when it receives unexplained rigid commands.

A useful skill commonly contains the following sections.

### Purpose and scope

State the job, intended outcome, expected user, and boundaries. Clarify whether the skill creates an answer, generates a file, changes a system, or guides a user through a process.

### Inputs and prerequisites

List required information, approved sources, capabilities, permissions, and optional inputs. State what happens when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and the approved source material.
If a required source is unavailable, ask for an export or provide a clearly marked incomplete draft.
```

### Workflow

Provide the normal sequence of work and meaningful decision points:

1. Inspect the request and available inputs.
2. Ask focused questions only when the answer materially changes the result or risk.
3. Gather evidence from approved, relevant sources.
4. Perform the task using the appropriate method.
5. Check the output against requested format, evidence, and success criteria.
6. Deliver the result with assumptions, limitations, and required follow-up.

Use conditional guidance rather than trying to enumerate every possible circumstance:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a proposed action could overwrite, publish, or otherwise materially affect work, explain the impact and request confirmation first.
```

### Output format

Define an exact template when predictable structure is valuable:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or requested follow-up]
```

Do not impose a rigid shell when usefulness depends on adapting to the request. In those cases, specify outcome goals and provide a small generalized example.

### Quality, privacy, and safety checks

Specify what must be checked before completion. Examples include required fields, calculation validation, source attribution, preservation of originals, access boundaries, and clear labeling of uncertainty.

For workflows involving people, hiring, or assessment, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Avoid irrelevant personal details and loaded language when characterizing people or assessment outcomes.

### Failure behavior

Describe recovery behavior in general terms:

- **Missing or conflicting input:** Name the gap and ask a focused question.
- **Unavailable capability or reference:** Explain what cannot be verified and offer an alternate method if appropriate.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the outcome; otherwise ask.
- **Validation failure:** Do not present the work as complete. Correct it, report the issue, or request guidance.
- **External or high-impact action:** Pause for explicit confirmation before proceeding.

### Examples

Include only a few short generalized examples when they teach a distinct pattern. Examples should illustrate reasoning and output shape, not substitute for a broad workflow.

## 5. Write a strong activation description

The description is a routing mechanism: it helps the AI decide when the skill applies. State both what the skill does and when to use it.

Cover realistic ways users express the need, including requests that imply the job rather than naming it exactly. Make the description specific enough to activate for useful cases without swallowing nearby work that belongs to another skill.

A good description includes:

- The task or desired outcome.
- Common contexts and phrasing that signal relevance.
- Important scope limits that prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use for requests involving progress summaries, leadership updates, milestone reviews, risks, next steps, or concise accounts of project health, even when the user does not say “status report.”
```

Keep detailed procedure in the body, not the description. The description should be accurate, useful, and honest about scope.

## 6. Review the draft before testing

Read the draft as though encountering it for the first time. Check that:

- The job is coherent and bounded.
- The description explains activation conditions.
- Inputs, permissions, and outputs are clear.
- Important rules explain their purpose.
- Instructions address missing information and failed validation.
- The skill does not assume one person’s habits, local files, private access, or preferred terminology.
- The skill has enough flexibility for normal variation.
- The instructions do not contain redundant steps or rules that do not affect outcomes.

Prefer a lean instruction set over a long set of brittle commands. Frequent emphatic language is a warning sign unless the requirement is truly non-negotiable, such as an authorization or safety boundary.

## 7. Design realistic tests

Once the draft is stable enough to test, create two or three realistic prompts and show them to the user before relying on them. Ask whether they resemble real requests and whether an important scenario is missing.

For each test, preserve:

- A descriptive identifier.
- The complete user prompt.
- Relevant supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

A portable test record can look like this:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and flag information that cannot be verified.",
      "expected_output": "A structured summary that distinguishes verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover distinct situations rather than superficial wording changes:

- A normal successful request.
- Incomplete, ambiguous, or conflicting input.
- A formatting or constraint-sensitive request.
- A realistic case that changes the workflow.
- A case that should require approval, protective handling, or a refusal when relevant.

Avoid tests that merely repeat words from the instructions. Vary user phrasing, level of detail, and context.

## 8. Run tests and comparisons

When independent runs are available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revised version with the original or another clearly identified baseline.

Start both conditions for all test cases under comparable circumstances. If parallel execution is available, launch both conditions together. This makes timing comparisons fairer and avoids changing the baseline after seeing the skill’s result.

Use a clear iteration structure, such as:

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

For every test condition, preserve the prompt, supplied files, outputs, and available run information such as elapsed time and resource use. Record timing and resource data immediately when the runtime reports it, because some environments do not retain it later.

Store per-test metadata, including its descriptive name, prompt, and current objective checks. This enables consistent grading across iterations.

If independent runs are not available, perform a transparent sanity check: follow the skill for each test request, save the outputs, and obtain user feedback. Do not call this a rigorous baseline comparison.

## 9. Define and grade objective checks

While test runs are in progress, draft objective checks rather than waiting idly. Explain them to the user before treating them as success criteria.

Good checks are observable, meaningful, and clearly named. Examples:

- Required sections are present.
- A file opens and contains required fields.
- Calculations match an approved source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- Key claims include source references where required.

Record each grade using a stable shape:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when required source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests follow-up."
    }
  ]
}
```

Use a programmatic check when feasible. Automated checks are more repeatable than visual judgment and can be reused in later iterations. For subjective work such as writing quality, design, strategic usefulness, or tone, rely primarily on informed human review. Do not force a weak numeric proxy that encourages the skill to optimize for the measure instead of user value.

## 10. Present results for human review

After runs complete, grade results, aggregate useful measures, and present both outputs and measurements for review. Use an available review method that lets the user inspect outputs, compare conditions, see grades, and leave feedback. If no dedicated review interface is available, provide accessible files or a clear in-conversation review.

For each case, show:

- The prompt and relevant inputs.
- The skill output and comparison output, if any.
- Objective grades and supporting evidence.
- Timing or resource data, if available.
- Prior iteration output and feedback when comparing revisions.

Explain what the reviewer will see and how to provide feedback. Useful questions include:

- Which output would you trust in normal use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add effort or detail that did not create value?
- Would the result work for similar requests with different data or wording?

If feedback is exported as a file, place it with the iteration materials and read it before revising. Empty feedback commonly means the reviewed output was acceptable, but it is not proof that all cases are solved.

Close temporary review services after feedback has been captured.

## 11. Analyze beyond aggregate scores

Aggregate results where possible: pass rate, elapsed time, resource use, variation, and differences between conditions. Place the revised skill before its comparison condition in reports for easy reading.

Then perform an analyst pass. Look for patterns aggregate statistics can hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill’s contribution.
- **High variation:** Similar runs differ greatly, suggesting ambiguity, instability, or unreliable instructions.
- **Tradeoffs:** Quality improves, but at disproportionate cost in time or resource use.
- **Failure concentration:** Several failures share one root cause, such as unclear source selection.
- **Unproductive work:** Execution records reveal repeated planning, redundant research, or unnecessary formatting.
- **Repeated reconstruction:** Multiple runs independently rebuild the same helper procedure, indicating a useful script or template may be missing.

Treat a small test set as directional evidence, not final proof.

## 12. Improve without overfitting

Base revisions on feedback, outputs, and analysis. Change the smallest part likely to address the underlying cause.

Generalize from feedback. If one test omitted a source note, do not write a rule about that exact test. Instead, clarify the broader condition: when evidence is incomplete or mixed, distinguish verified information from assumptions and unknowns.

Use these improvement principles:

1. **Fix causes, not examples.** Design for future requests, not the current test wording.
2. **Keep the prompt lean.** Remove guidance that does not improve behavior or causes wasted effort.
3. **Explain intent.** State why a step protects quality, usability, safety, or trust.
4. **Add reusable resources selectively.** Bundle templates, scripts, and references only when repeated work proves their value.
5. **Preserve useful behavior.** Do not lose what users already value while correcting a weakness.
6. **Expand coverage gradually.** Add a test when it represents a real class of failure, not every isolated incident.

After revision, rerun the applicable full test set in a new iteration. Use the same baseline policy, preserve earlier outputs for comparison, collect feedback, and repeat.

Stop when the user says the skill is ready, feedback is consistently positive across meaningful tests, objective requirements are reliably met, or further revisions no longer create meaningful improvement.

## 13. Optional blind comparison

For a more rigorous comparison of two versions, use blind review. Give an independent evaluator two outputs without revealing which version produced each output. Use a shared rubric tied to user value: correctness, completeness, clarity, constraint adherence, safety, and practical usefulness.

Use blind comparisons when versions have similar measurements but visibly different quality, when evaluator bias is a concern, or when the decision is important. Record the reasoning before revealing which output came from which version, then analyze why the preferred output won.

## 14. Optimize activation behavior

Only optimize the description after the skill’s workflow itself is useful.

Create a realistic, roughly balanced set of activation queries: some that should activate the skill and nearby cases that should not. Include enough detail that consulting a skill would actually help.

Positive cases should cover formal and casual phrasing, direct and implied requests, common and uncommon valid uses, and cases where another related skill might compete.

Negative cases should be difficult near-misses, not irrelevant requests. They should share concepts or wording with the skill but require a different job, different capability, or different conditions.

```json
[
  {
    "query": "I need a concise update for leadership from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what a project status report is and when teams use one?",
    "should_trigger": false
  }
]
```

Review the query set with the user before running it. If an evaluation capability supports repeated activation trials, evaluate candidate descriptions repeatedly, separate queries used to improve the description from held-out queries used for selection, and choose the description that performs best on held-out cases.

A simple one-step request may not activate a specialized skill even with a matching description because an AI can complete it directly. Use substantive test queries where the skill would add genuine value.

Show the user the description before and after optimization, along with results and known limitations.

## 15. Package and hand off

Package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The activation description accurately represents scope.
- Instructions do not depend on private conventions, undeclared capabilities, or unapproved access.
- Resources are present, clearly named, and documented.
- No credentials, private records, identifiers, confidential examples, or unnecessary sensitive material are included.
- Evaluation materials are included only when safe and useful.
- The user can install, access, or adapt the package in their chosen environment.

Provide a short handoff note that states what the skill does, required capabilities, known limitations, and a simple post-installation test.

## Final readiness gate

A skill is ready when it has a clear job, a description that activates for appropriate requests, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.

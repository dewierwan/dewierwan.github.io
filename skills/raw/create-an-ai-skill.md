---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, optimizing, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, improve an existing skill, evaluate whether a skill helps, or refine its triggering description. A skill is a focused package of instructions and optional resources that helps an AI complete a recurring type of work consistently.

The core loop is:

1. Understand the intended job and its boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements when appropriate.
5. Improve the skill based on evidence.
6. Repeat until the skill is useful, reliable, and not tailored only to its tests.
7. Optionally optimize the description that determines when the skill is used.
8. Package and hand off the finished skill.

Adapt the process to the user’s needs. Some users want a quick collaborative draft; others need comparison runs, formal checks, and several iterations. First determine where the user is in the loop, then help them take the next useful step. Do not require extensive testing when the user explicitly wants an exploratory or “good enough” draft, but explain what confidence is being traded away.

## Communication principles

Match the user’s technical vocabulary. Use plain English by default. Terms such as *evaluation* and *benchmark* are usually understandable, but define them briefly when useful. Do not use unexplained technical terms such as *JSON*, *schema*, or *assertion* unless the user signals familiarity or you explain them.

Ask questions because their answers change the design, not as a fixed questionnaire. For example:

- “What should a successful result look like: a chat response, a report, a file, or an action?”
- “Should the skill make a reasonable low-risk assumption when information is missing, or pause and ask?”
- “Which information sources are approved for this work?”
- “What errors would make the output unusable or risky?”

Keep the user involved at meaningful choices:

- Confirm the job before writing a large instruction set.
- Ask before imposing a restrictive scope, tool requirement, approval rule, or output format.
- Share proposed test cases before treating them as representative.
- Let human judgment lead when quality is subjective, such as tone, design, originality, or strategic usefulness.

When a task involves private communications, personnel records, customer information, health information, financial information, or other sensitive material, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and details. Exclude unrelated personal details, respect consent and privacy expectations, and keep outputs within the appropriate access boundary.

## 1. Identify the starting point

Classify the request before choosing the workflow.

### New skill

The user has an idea such as “make a skill that prepares weekly project updates.” Start with discovery, scope definition, and a first draft.

### Existing skill

The user has a skill they want to simplify, repair, extend, test, or optimize. Read the current instructions before proposing changes. Preserve its established name and identity unless the user asks to change them. If the installed copy cannot be edited, work from an editable copy and preserve the original until the revision is validated.

### Workflow demonstrated in conversation

The user may ask to “turn what we just did into a skill.” Extract what is already known from the conversation before asking repetitive questions:

- Inputs and source material used.
- Steps, decisions, and tool capabilities used.
- Corrections and preferences the user expressed.
- Output structure and acceptance criteria.
- Points where the workflow changed based on conditions.
- Assumptions that were safe in this instance but may not generalize.

Present the inferred workflow and its open questions for confirmation. Do not silently convert a one-time workaround or personal preference into a universal rule.

### Evaluation or optimization request

The user may have a complete-looking skill and ask whether it works. Go directly to test design, comparison, review, and revision. Do not rewrite an instruction set merely because rewriting is possible.

## 2. Capture intent, scope, and safety boundaries

Gather enough information to define a coherent job. Start with the answers most likely to affect the design.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Trigger:** What user requests, phrases, or contexts should cause the skill to be used?
3. **Inputs:** What information, files, systems, examples, and approved sources may it use?
4. **Outputs:** What should it produce, change, or communicate? Is a particular format required?
5. **Success criteria:** How will the user know the result is correct, useful, complete, or ready to use?
6. **Boundaries:** What should the skill not do? When should it ask, decline, or hand a decision back to the user?
7. **Variations:** What normal variants, difficult cases, and exceptions matter?
8. **Dependencies:** Are particular capabilities, templates, policies, reference materials, or permissions required?
9. **Testing level:** Does the user want a quick review, realistic test cases, objective checks, or a formal comparison?

For skills that access records about people, add these questions:

- What is the authorized purpose for accessing this information?
- Which sources and fields are necessary for that purpose?
- Who is allowed to receive the result?
- What details should be omitted, aggregated, or anonymized?
- Is human approval required before sharing, changing, or acting on the result?

For hiring, performance assessment, or similar decisions, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Do not make claims about people that go beyond the evidence or the authorized decision process.

### Research before drafting

If the environment provides user-approved documentation, existing skills, relevant templates, domain standards, or authoritative references, inspect them before drafting. Research should reduce the user’s burden, not substitute for the user’s authority over goals and constraints.

Use research to identify:

- Existing conventions and output standards.
- File, data, or system constraints.
- Similar reusable patterns.
- Required approvals, compliance rules, or privacy boundaries.
- Whether a proposed action is technically feasible.

If sources conflict or a requirement remains uncertain, state the uncertainty. Do not hide a guess inside a confident instruction.

## 3. Choose a maintainable skill structure

Keep each skill focused enough that a user and an AI can predict what it does. A single skill may support related variants, but separate unrelated jobs that have different source-of-truth rules, access needs, outputs, or definitions of completion.

A portable skill package commonly has this shape:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed guidance
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test cases and checks
```

Use progressive disclosure:

1. **Metadata or registration information:** Short name and description used to decide whether the skill applies.
2. **Core instructions:** The workflow needed for most invocations.
3. **Supporting resources:** Detailed references, scripts, templates, and domain variants loaded only when needed.

Keep the core instruction file readable. If it becomes too long, move detailed or specialized material into clearly named resources and state exactly when the AI should read them. Give large references a table of contents or clear navigation headings.

For skills with several technical or domain variants, use one selection workflow plus separate references by variant. The AI should identify the relevant variant and load only that material rather than treating every variant as required context.

### Bundle scripts only when justified

A script or deterministic helper is useful when repeated tests show the AI independently rebuilding the same procedure, such as validating data, generating a structured file, converting a format, or checking required fields. Bundle it when it is reusable, safer, and easier to verify than repeated free-form work.

Document each helper’s:

- Purpose and allowed use.
- Inputs and expected outputs.
- Preconditions and permission requirements.
- Failure behavior.
- Cases where the AI should use a different method.

Do not automate destructive, external, or permission-sensitive actions without clear user confirmation and appropriate safeguards.

## 4. Draft the skill instructions

Write in clear, direct, imperative language. Explain the reason for important rules, especially rules that prevent a predictable quality, safety, or authorization failure. A capable AI generally handles variation better when it understands the goal and tradeoff instead of receiving a long list of unexplained commands.

Include the following sections when applicable.

### Purpose and scope

State what the skill does, who it serves, and what is outside its scope. Clarify whether the skill produces advice, creates an artifact, modifies data, performs an external action, or guides the user through a decision.

### Inputs, sources, and prerequisites

List required inputs, permitted sources, necessary capabilities, and optional material. Explain what to do when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and the approved source material.
If a required source is unavailable, ask for an export or provide a draft clearly marked with the information that could not be verified.
```

For private or sensitive material, specify minimum necessary access and output handling. For example, instruct the AI to summarize only role-relevant evidence and omit unrelated personal information.

### Workflow and decision points

Describe the normal sequence of work and the conditions that change it. A durable sequence often looks like this:

1. Inspect the request, available inputs, and permissions.
2. Identify missing information that materially affects the result.
3. Ask focused questions or make a stated low-risk assumption, as appropriate.
4. Gather evidence from approved sources only.
5. Complete the task using the relevant method or variant.
6. Validate the output against requested format and success criteria.
7. Present the result with assumptions, evidence, and unresolved limitations.

Use conditional rules rather than trying to enumerate every situation:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite important work, create an irreversible external effect, or expose sensitive information, explain the impact and request confirmation before proceeding.
```

### Output format

When consistency matters, provide an exact or near-exact template.

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding and supporting evidence]

## Recommendations or next steps
1. [Action]

## Assumptions and open questions
- [Uncertainty, missing data, or decision needed]
```

Use flexible goals rather than rigid templates when adaptation is central to the task, such as creative work or context-dependent analysis.

### Quality, privacy, and safety checks

State what must be checked before completion. Useful checks include:

- Required sections, fields, or file properties are present.
- Calculations are validated against approved data.
- Important claims distinguish evidence from assumptions.
- Sources for consequential claims are identified when appropriate.
- Original data is preserved before transformation.
- Sensitive details are minimized and recipients are authorized.
- Uncertainty is visible rather than concealed.

A skill must not surprise the user by concealing actions, bypassing authorization, extracting confidential information, or attempting access beyond the user’s authority. If a request is unsafe, deceptive, outside the user’s authority, or cannot be verified responsibly, explain the limitation and offer a safe alternative where possible.

### Failure behavior

Give general recovery rules:

- **Missing or conflicting inputs:** Identify the gap and ask the smallest useful question.
- **Unavailable capability or reference:** Explain what cannot be verified and offer an alternative method or partial result.
- **Ambiguous request:** Make a clear low-risk assumption only when it will not materially change the result; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, flag it, or request guidance.
- **Irreversible or high-impact action:** Pause for confirmation before proceeding.
- **Sensitive information:** Limit collection and disclosure to what is necessary for the authorized purpose.

### Examples

Include a few short, generalized examples only when each teaches a distinct behavior. Examples should illustrate reasoning and output shape, not become narrow scripts for matching test prompts.

## 5. Write a description that triggers appropriately

The description is a routing instruction. It should say both what the skill does and when to use it. Include realistic contexts and phrasing that imply the task even if the user does not name the skill.

A good description contains:

- The outcome the skill helps achieve.
- Common request types or contexts where it applies.
- Important boundaries that prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a progress update, leadership summary, milestone review, risk overview, or next-step report, even if they do not use the phrase “status report.”
```

Keep the entire workflow out of the description. Avoid vague labels such as “help with documents,” and avoid making it so broad that it captures adjacent tasks better handled by another skill.

## 6. Audit the draft before testing

Read the draft as a first-time user and as the AI that must follow it. Check:

- Is the job clear and bounded?
- Does the description identify when to use the skill?
- Are inputs, source permissions, outputs, and completion criteria clear?
- Does the workflow explain important reasoning rather than merely issue commands?
- Does it handle missing information and validation failure?
- Does it avoid hidden assumptions about a particular person, organization, tool, access level, or local setup?
- Are private records handled only for an authorized purpose and with minimum necessary disclosure?
- Are there repeated rules, brittle wording, or unnecessary procedures?
- Does the AI have enough flexibility to handle ordinary variation?

Prefer lean instructions over a long list of commands that do not change behavior. Repeated capitalized absolutes are a warning sign unless the rule is a genuine safety, authorization, or integrity boundary.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user before running them and invite corrections or additions.

Each test case should record:

- A descriptive identifier.
- The prompt.
- Relevant files or context.
- Expected outcome in plain language.
- Objective checks, if appropriate.

A portable format is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates and identify information that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful categories, not merely different wording:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive, privacy-sensitive, or rule-sensitive request.
- A realistic exception that changes the workflow.
- A request requiring confirmation or a safe refusal, when relevant.

Avoid tests that simply repeat the skill’s own language. Vary wording, detail, and context. Use generalized scenarios and authorized or synthetic data rather than personal or confidential examples.

## 8. Run evaluations and comparisons

When independent execution is available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revised skill against the earlier version.

Start all comparable runs under similar conditions. When parallel execution is available, launch the skill-assisted and comparison runs for every test case at the same time. This reduces timing bias and prevents later baseline changes from distorting the comparison.

Organize results by iteration and descriptive test name:

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

For each run, retain the prompt, supplied files, resulting outputs, run configuration, and any available timing or resource data. Capture timing information as soon as the execution environment reports it, because some systems do not retain it later.

If independent agents, parallel runs, or a comparison environment are unavailable, conduct a transparent sanity check: apply the skill to each test prompt, save the outputs, and ask the user to review them. Do not represent this as a rigorous baseline experiment.

## 9. Define and grade objective checks

While runs are in progress, create objective checks where they genuinely help. Explain them to the user before treating them as measures of success.

Good checks are observable, specific, and tied to user value. Examples:

- Required sections are present.
- A produced file opens and contains required fields.
- Calculated values match an agreed source within a defined tolerance.
- The response identifies missing mandatory inputs.
- The output distinguishes evidence from assumptions.
- A required authorization or confirmation was requested before a consequential action.

Record each grade with stable fields for the check, outcome, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable information and requests the needed source."
    }
  ]
}
```

Use scripts for programmatic checks whenever practical. They are faster, more repeatable, and reusable across iterations. Do not force numerical checks onto subjective work. Tone, visual quality, strategic judgment, and creative usefulness often require human review; weak proxy metrics can cause a skill to optimize for a score rather than the user’s actual goal.

## 10. Review results with a human

Present outputs and measurements in a review format the user can access. If a review interface is available, use it to show each prompt, output, comparison output, grades, timing, and a place for feedback. If no interface is available, present the same material clearly in conversation or as downloadable files.

Ask focused review questions:

- Which output would you trust in normal use, and why?
- What was missing, misleading, unsafe, or difficult to use?
- Did the skill add work or detail that did not help?
- Did it appropriately identify uncertainty and preserve privacy boundaries?
- Would it work for similar requests with different wording or data?

For later iterations, show prior outputs and prior feedback alongside the new result when possible. Empty feedback usually means the user found that case acceptable, but it is not proof that the skill is generally solved.

## 11. Analyze results beyond pass rates

Aggregate available results: pass rates, time, resource use, variation, and per-test outcomes. Present the revised version before the comparison version for easier reading.

Then inspect patterns that averages can hide:

- **Non-discriminating checks:** Both versions pass, so the check does not reveal the skill’s value.
- **High variation:** Comparable runs differ substantially, suggesting ambiguity, instability, or weak instructions.
- **Tradeoffs:** Quality gains may cost too much time or effort.
- **Failure concentration:** Several failures may stem from one root issue, such as unclear source selection or output rules.
- **Unproductive work:** Execution traces reveal repeated planning, redundant research, or needless formatting.
- **Repeated reconstruction:** Several runs independently rebuild the same helper procedure, indicating that a reusable resource may be warranted.

A small evaluation set is evidence for the next revision, not conclusive proof of quality.

## 12. Improve without overfitting

Revise based on user feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from feedback. If one response fails to distinguish verified facts from uncertain claims, do not add a rule mentioning only that scenario. Clarify the broader principle: when sources are incomplete, mixed, or uncertain, separate supported findings from assumptions and unresolved questions.

Use these principles:

1. **Fix causes, not examples.** Build for future requests, not only current tests.
2. **Keep instructions lean.** Remove guidance that adds cost without improving results.
3. **Explain intent.** Connect important actions to quality, safety, clarity, or user control.
4. **Add reusable resources selectively.** Bundle templates, scripts, or references only when repeated work demonstrates their value.
5. **Preserve useful behavior.** Do not erase what users already value while fixing a defect.
6. **Expand test coverage gradually.** Add a test when it represents a meaningful class of failure.

After a revision, rerun the full test set in a new iteration. Use the same baseline policy unless there is a documented reason to change it. Continue until the user is satisfied, objective requirements are reliably met, feedback is consistently positive, or further revisions no longer produce meaningful improvement.

## 13. Optional blind comparison

When a decision between two versions needs stronger evidence, use blind comparison. Give an independent evaluator two outputs without revealing which version produced each one. Ask it to judge using a shared rubric, record the judgment, and only then reveal the mapping.

Use blind comparison when versions have similar scores but visibly different quality, when preference bias may be strong, or when the decision has material consequences. Judge against user-centered criteria: correctness, completeness, clarity, constraint adherence, safety, and practical usefulness. Analyze why the preferred output won before revising again.

## 14. Optimize triggering behavior after the workflow works

Only optimize the triggering description once the skill itself is useful. Create a balanced set of realistic requests that should trigger and difficult near-misses that should not.

Positive cases should vary across:

- Formal and casual wording.
- Direct and implied requests.
- Common and less common valid use cases.
- Situations where a related skill might compete but this one should apply.

Negative cases should be genuinely adjacent, not obviously irrelevant. They should share concepts or language with the skill but need another workflow, lack required conditions, or ask for explanation rather than task execution.

```json
[
  {
    "query": "Turn these approved team updates into a concise leadership summary with risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Explain what a status report is and when teams use one.",
    "should_trigger": false
  }
]
```

Review the query set with the user. If the environment supports repeated routing tests, divide cases into an improvement set and a held-out selection set. Test candidate descriptions more than once when routing can vary, and choose the description that performs best on held-out cases rather than merely fitting the examples used during editing.

Use substantive trigger queries. An AI may complete a simple one-step request directly without consulting a specialized skill even when the description matches. Test requests should therefore be complex enough that the skill would provide genuine value.

Show the user the before-and-after description and the observed results. Keep the final wording accurate about the skill’s real scope.

## 15. Package and hand off

Package the core instructions and only the resources required for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately represents activation conditions.
- Instructions do not depend on undeclared private conventions, local paths, personal access, or a particular vendor tool.
- Scripts and references are present, clearly named, and documented.
- No credentials, identifiers, confidential records, or sensitive examples remain.
- Privacy and authorization requirements are explicit where relevant.
- Test materials are retained only when safe and useful.
- The user can install, adapt, and test the package in their chosen environment.

Provide a short handoff note stating what the skill does, required capabilities, known limitations, how to test it, and any approval steps needed for consequential actions.

## Final readiness gate

A skill is ready when it has a clear job, a description that routes appropriate requests, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not mistake a long instruction file for a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for the user’s real recurring work.

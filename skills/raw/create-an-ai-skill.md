---
name: create-an-ai-skill
description: Design, test, refine, evaluate, and package reusable AI skills using realistic requests, human review, and evidence-based iteration.
---

# Create an AI skill

Use this workflow to design a new reusable AI skill, improve an existing skill, evaluate whether a skill helps, or turn a repeated conversation workflow into durable instructions. A skill is a focused set of instructions, with optional scripts, references, and templates, that helps an AI perform a recurring job consistently.

The central loop is:

1. Define the job, boundaries, and conditions for use.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Review outputs with a person and measure objective requirements where appropriate.
5. Improve the skill from evidence rather than guesswork.
6. Repeat until further changes no longer create meaningful value.
7. Optionally improve the skill description so it activates for the right requests.

Adapt the rigor to the user’s goal. Some users want a quick collaborative draft; others need comparison runs, measurable checks, and several iterations. Determine where the user is in the process and help them take the next useful step rather than forcing every project through the full workflow.

## Communication principles

Use plain language by default and match the user’s technical level. Terms such as *evaluation* and *benchmark* are usually understandable, but briefly define terms such as “JSON,” “assertion,” or “schema” when the user may not know them.

Explain why questions matter. For example, ask: “What should a successful result look like: a chat response, a structured report, a file, or an approved external action? This determines how we define completion and test it.”

Keep the user involved at meaningful decision points:

- Confirm the intended job before writing extensive instructions.
- Ask before selecting a restrictive scope, tool requirement, or approval rule.
- Propose test cases and let the user correct or add to them.
- Use human judgment for subjective qualities such as writing usefulness, tone, visual quality, or strategic judgment.
- Be transparent when a test is only a sanity check rather than an independent comparison.

## 1. Determine the starting point

Identify which situation applies before changing anything.

### New skill

The user has an idea for a recurring job. Start with discovery, then prepare a first draft.

### Existing skill

The user has a draft or installed skill and wants it edited, simplified, tested, or improved. Read the current instructions first. Preserve the established name and identity unless the user explicitly requests a rename.

### Workflow demonstrated in the conversation

The user may ask to “turn this into a skill.” Extract what is already known from the conversation before asking repetitive questions:

- Inputs, files, and permitted information sources.
- Tools or capabilities used.
- Order of decisions and actions.
- Corrections and preferences the user supplied.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow, clearly mark gaps or assumptions, and ask the user to confirm them. Do not turn a one-time workaround into a general rule without checking whether it should apply broadly.

### Evaluation or optimization request

The user may already have a functioning skill and want evidence about whether it improves results. Begin with test design and evaluation. Do not rewrite working instructions merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough detail to define one coherent, reusable job. Do not ask every question mechanically; begin with the missing details that would most affect the design.

Use these questions as needed:

1. **Purpose:** What should the AI accomplish?
2. **Activation:** What requests, contexts, or wording should cause this skill to be used?
3. **Inputs:** What information, examples, files, systems, and permissions can it use?
4. **Outputs:** What should it produce, modify, or recommend? Is a format required?
5. **Success criteria:** How will the user recognize a correct or useful result?
6. **Boundaries:** What should it not do? When should it ask, decline, or return control to the user?
7. **Variation:** What common cases, difficult cases, or exceptions change the workflow?
8. **Dependencies:** Does it require particular capabilities, reference materials, templates, or scripts?
9. **Testing:** Should the result be tested with realistic requests?

Offer choices when useful:

- “Should the skill make a low-risk best effort when information is missing, or pause and ask?”
- “Should the default output be concise, detailed, or selected by the user?”
- “May it use any accessible source, or only sources the user has explicitly approved?”
- “Should it prepare a draft only, or may it take an external action after confirmation?”

Recommend test cases when outputs are objectively checkable, the workflow has material consequences, the skill will be reused often, or the task uses files, structured data, or fixed procedural steps. For creative or highly subjective work, short qualitative review may be more useful than forced metrics.

### Research before drafting

When relevant approved documentation, comparable skills, standards, or example materials are available, review them before drafting. Research should reduce the burden on the user, not override their authority over requirements.

Use it to identify:

- Existing conventions and output standards.
- File-format or tool constraints.
- Reusable patterns from comparable tasks.
- Safety, privacy, compliance, and approval expectations.

If the task touches private communications, records, or information about people, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Omit unrelated sensitive details, respect consent and privacy expectations, and keep outputs within the appropriate access boundary.

If requirements conflict or remain uncertain, state the uncertainty and seek direction rather than silently guessing.

## 3. Choose the skill structure

A skill should be focused enough that users and the AI can predict what it does. A single skill may support closely related variants, but separate unrelated jobs that have different audiences, permissions, sources of truth, or completion standards.

A typical package might be organized as follows:

```text
skill-name/
├── SKILL.md          # Core instructions
├── scripts/          # Optional deterministic helpers
├── references/       # Optional documentation consulted as needed
├── assets/           # Optional templates or output resources
└── evals/            # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description used to decide whether the skill applies.
2. **Core instructions:** The workflow required for ordinary uses.
3. **Supporting resources:** Detailed references, scripts, or templates loaded only when relevant.

Keep core instructions readable. If they become long, move variant-specific or detailed material into clearly named files and state exactly when each should be consulted. Give large reference files a navigation section or table of contents.

For a skill supporting multiple environments, keep shared decision logic in the core instructions and place environment-specific instructions in separate reference files. Read only the applicable material rather than loading every variant by default.

### Bundle reusable deterministic work

If multiple test runs repeatedly reconstruct the same helper procedure, consider a script or template. Good candidates include format validation, data transformation, document construction, calculations, and repeatable file conversions.

Bundle a helper only when it is reusable, permitted, and more reliable than repeatedly recreating the procedure. Document what it does, its inputs, outputs, limitations, and when not to use it. Do not add automation merely because it is possible.

## 4. Write the skill

Write instructions in clear, imperative language. Explain the purpose behind important steps, especially steps that prevent predictable quality, safety, or authorization failures. A capable AI can adapt principles better than it can follow a large list of unexplained commands.

Include the following sections when relevant.

### Purpose and scope

State the job, intended user, expected result, and limits. Clarify whether the skill answers questions, creates files, analyzes information, carries out approved actions, or guides a user through a process.

### Inputs and prerequisites

List required information, allowed sources, needed tools, permissions, and optional inputs. State what happens if required material is unavailable.

```markdown
Before preparing the report, confirm the reporting period and approved information sources.
If a required source is unavailable, ask for an export or produce a draft clearly marked with its limitations.
```

### Workflow and decision points

Give the normal sequence, with meaningful branches rather than trying to list every imaginable exception.

A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Clarify only uncertainties that materially affect the result.
3. Gather evidence from approved sources.
4. Complete the requested work using an appropriate method.
5. Check the result against requested format and success criteria.
6. Present the result, assumptions, sources, and unresolved limitations.

Use conditional guidance where needed:

```markdown
If the user supplies a required template, follow it.
If no template is provided, use the default structure below.
If a requested action could overwrite important work or affect an external system, describe the impact and request confirmation before proceeding.
```

### Output format

Where consistency matters, define a template:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding supported by evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or required follow-up]
```

Avoid rigid templates when adapting to context is more valuable. In those cases, define the desired qualities and provide a small example instead.

### Quality, safety, and privacy checks

State the checks required before completion, such as required fields, calculation validation, source attribution, preservation of original data, or uncertainty disclosure.

A skill must behave in ways a user would reasonably expect from its description. Do not conceal actions, bypass authorization, expose confidential material, facilitate unauthorized access, or damage systems. Pause for confirmation before irreversible, external, or high-impact actions.

### Failure behavior

Describe general recovery rules:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** State what cannot be verified and offer a safe alternative.
- **Ambiguous request:** Make a low-risk assumption only if it will not materially affect the outcome; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, report the problem, or request guidance.
- **Permission-sensitive work:** Confirm authorization before proceeding.

### Examples

Use a small number of generalized examples only when each teaches a distinct decision pattern. Examples should illustrate reasoning and output shape, not replace the workflow with narrow test-specific instructions.

## 5. Write an effective description

The short description is primarily a routing instruction. It should say both what the skill does and when it should be used.

Describe realistic user language, including requests that imply the job without naming it. AI systems can fail to activate useful skills unless relevance is explicit.

A good description includes:

- The task or user outcome.
- Common requests and contexts that indicate the task.
- Important limits that prevent costly or unsafe false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use for requests involving leadership updates, progress summaries, milestone reviews, risks, decisions, or next steps, even when the user does not say “status report.”
```

Do not put the full procedure into the description. Avoid vague labels such as “help with documents,” but do not make the description so broad that it captures adjacent work better handled by another skill.

## 6. Review the draft before testing

Read the instructions as if seeing them for the first time. Check:

- Is the job coherent and bounded?
- Does the description state when the skill applies?
- Are inputs, permissions, output expectations, and completion checks clear?
- Does the skill explain why important steps exist?
- Does it handle missing information and unavailable capabilities?
- Does it avoid personal habits, undeclared access, and tool-specific assumptions?
- Are there redundant rules or brittle wording?
- Does the AI have enough freedom to handle normal variation?

Prefer lean instructions over long instruction files filled with guidance that does not change outcomes. Repeated absolute language is a warning sign unless the rule protects a true non-negotiable boundary, such as authorization or safety.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic requests. Share them with the user before treating them as the evaluation set.

For each test, record:

- A descriptive identifier.
- The prompt.
- Any supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and flag information that cannot be verified.",
      "expected_output": "A structured summary separating verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover different meaningful conditions:

- A typical successful request.
- Incomplete or ambiguous inputs.
- A format- or rule-sensitive request.
- A realistic edge condition that changes the workflow.
- A request that should trigger approval, a safe refusal, or limited handling, when relevant.

Vary phrasing, detail level, and user expertise. Avoid tests that merely repeat the skill’s exact wording or preserve personal, confidential scenarios.

## 8. Run evaluations and comparisons

When independent runs are available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without it.
- **Existing skill:** Save an unchanged snapshot before editing, then compare the revised version with the previous version.

Start both conditions for every test under comparable circumstances. If parallel execution is available, launch all skill and baseline runs together. Preserve each prompt, relevant inputs, produced outputs, and available run metadata such as elapsed time and resource use.

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

Capture timing or usage data as soon as the environment reports it, because some systems do not retain it later.

If independent agents, parallel execution, or comparison infrastructure are unavailable, run a transparent sanity check: follow the skill for each prompt, save the outputs, and request human feedback. Do not represent this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs proceed, draft objective checks if they measure something that matters. Explain them to the user before relying on them.

Useful checks are specific, observable, and meaningful:

- Required report sections are present.
- A file opens and includes required fields.
- Calculations match known values within an agreed tolerance.
- The output identifies missing mandatory input.
- Claims include required source references.

Record each check with clear text, pass/fail status, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable inputs and requests follow-up."
    }
  ]
}
```

Use scripts for programmatic checks whenever practical. They are more repeatable and reusable than visual inspection. Do not force numeric checks onto subjective work such as tone, design judgment, or strategic usefulness; these need qualitative review.

## 10. Review results with a human

Present outputs alongside measurements through an available review interface or directly in the conversation. For each test, show the prompt, applicable input, output for each condition, objective grades, evidence, and available timing or resource data.

Ask focused questions:

- Which output would you trust in everyday use, and why?
- What was missing, misleading, wasteful, or difficult to use?
- Did the skill add steps or detail that did not help?
- Would this still work with different wording, inputs, or constraints?

Empty feedback can mean a case is acceptable, but it is not proof that every case is solved. Consider the output and measurement evidence too.

## 11. Analyze results and improve

Aggregate results where possible: pass rates, timing, resource use, variation, and per-test outcomes. Then look beyond summary statistics for:

- Checks that pass equally with and without the skill, and therefore do not measure its value.
- High-variation results that may indicate ambiguity or environmental instability.
- Quality gains that cost too much time or resource use.
- Multiple failures with one underlying cause.
- Unproductive repeated planning, research, or formatting.
- Repeated reconstruction of helper procedures that suggests a reusable script or template.

Improve the underlying cause, not the test example. If a result fails to separate confirmed facts from assumptions, clarify how the skill should handle incomplete or mixed evidence generally; do not add a narrow rule tied only to one prompt.

Use these revision principles:

1. Fix causes, not examples.
2. Keep instructions lean.
3. Explain intent and tradeoffs.
4. Add scripts, templates, or references only when repeated evidence justifies them.
5. Preserve behavior users value.
6. Add tests only for meaningful classes of failure.

After revision, rerun the full test set in a new iteration and compare under the same policy. Show prior outputs when useful, collect feedback, and repeat.

Stop when the user says the skill is ready, feedback is consistently positive across meaningful cases, objective requirements are reliable, further revisions do not create meaningful gains, or remaining limits require unavailable information or a product decision.

## 12. Optional blind comparison

When two versions have similar measurable results but differ in quality, use blind review. Give an independent evaluator two outputs without identifying their origins, ask it to judge against a shared rubric, then reveal the mapping after the judgment is recorded.

Use criteria tied to user value: correctness, completeness, clarity, constraint adherence, safety, and practical usability. Analyze why an output was preferred before changing instructions again.

## 13. Optimize triggering behavior

Only optimize the description after the skill’s workflow is useful.

Create a realistic, balanced set of requests that should activate the skill and nearby requests that should not. Use substantive requests where consulting the skill would help; simple one-step requests may not activate specialized instructions even when descriptions match.

Positive cases should vary by formality, wording, directness, common and uncommon use cases, and overlap with related skills. Negative cases should be difficult near-misses that share vocabulary or context but belong to a different job.

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

Review the test set with the user. If repeated activation testing is available, separate examples used to improve the description from held-out examples used to select it. Choose the description that performs best on held-out cases, not merely the one that fits the drafting set.

Show the user the old description, the selected description, and the results. Keep the final description accurate about the skill’s actual scope.

## 14. Package and hand off

Package the core instructions and only the resources needed for normal use. Before handoff, audit the package:

- The name is stable and appropriate.
- The description accurately describes when to use the skill.
- Instructions do not depend on private conventions, undeclared access, or a particular person’s habits.
- Scripts and references are present, clearly named, and documented.
- No credentials, private identifiers, confidential records, or unnecessary sensitive examples remain.
- The package respects authorization and access boundaries.
- The user can install or adapt it in their chosen environment.
- Test material is retained only when it is safe and useful.

Provide a short handoff note explaining the skill’s purpose, required capabilities, known limitations, and a simple post-installation test.

## Final readiness gate

A skill is ready when it has a clear recurring job, an accurate activation description, instructions that handle normal variation, explicit handling for uncertainty and permissions, and evidence from realistic use that it improves the user’s outcome.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and produce better results for real recurring work.

---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing one, assess whether it works, or improve its activation behavior. A skill is a focused set of instructions, with optional resources, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the job, boundaries, and intended users.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review representative outputs with the user and measure objective requirements where appropriate.
5. Improve the skill from evidence rather than intuition alone.
6. Repeat until the skill is useful, reliable, and not narrowly fitted to a few tests.
7. Optionally improve the description that determines when the skill is selected.

Adapt the depth of this process to the user’s needs. Some users want a quick collaborative draft. Others need a careful evaluation and revision cycle. First determine where the user is in the process, then help them make the next useful decision.

## Communication principles

Match the user’s technical familiarity. Use plain language by default. Terms such as *evaluation* and *benchmark* can be useful, but briefly explain them if needed. Avoid unexplained technical terms such as “schema,” “assertion,” or “JSON” unless the user is already using them comfortably.

Explain why questions matter. For example:

> What should a successful result look like: a response in chat, a structured report, a file, or an approved external action? The answer determines how completion should be checked.

Keep the user involved at important decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before imposing restrictive scope, required tools, or approval rules.
- Share proposed test cases before treating them as representative.
- Let human judgment lead for subjective quality such as writing style, visual design, tone, or creative usefulness.
- State assumptions when the user has not provided enough information for a confident choice.

## 1. Determine the starting point

Identify which situation applies.

### A. New skill

The user has an idea for recurring work, such as preparing project updates, reviewing documents, transforming data, or guiding a structured process. Start with discovery and create a first draft.

### B. Existing skill or draft

The user already has instructions and wants them edited, simplified, tested, or improved. Read the current material before proposing changes. Preserve its established name and identity unless the user asks to rename it.

### C. A workflow demonstrated in the conversation

The user may ask to turn a recent interaction into a skill. Extract what can be learned from the conversation before asking repetitive questions:

- Inputs the user supplied.
- Approved information sources and tools used.
- The sequence of decisions and actions.
- Corrections or preferences expressed by the user.
- Output format and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow and identify gaps for the user to confirm. Do not silently convert a one-time workaround into a general rule.

### D. Evaluation or optimization request

The user may have a finished-looking skill and want to know whether it actually helps. Go directly to test design, evaluation, and focused revision. Do not rewrite a skill just because rewriting is possible.

## 2. Capture intent and scope

Gather enough information to define a coherent job. Adapt these questions to the situation rather than asking all of them mechanically.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What kinds of requests, wording, or contexts should make this skill relevant?
3. **Inputs:** What information, files, examples, systems, or permissions may it use?
4. **Outputs:** What should it produce, change, or recommend? Is a format required?
5. **Success criteria:** How will the user know the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask, stop, decline, or hand a decision back to the user?
7. **Variations:** What common cases, difficult cases, or meaningful exceptions matter?
8. **Dependencies:** Does it need a particular capability, reference, template, script, or user-provided access?
9. **Testing:** Should it be tested with example requests before release?

Recommend testing when outputs can be checked objectively, the workflow is consequential, the skill will be used repeatedly, or errors could be costly. For highly subjective work, recommend a smaller qualitative review instead of inventing misleading numerical metrics.

When helpful, offer explicit choices:

- Should the skill make a low-risk best effort when information is missing, or stop and ask?
- Should it use a concise default output, a detailed default output, or let the user choose?
- Should it use any available source, or only user-approved sources?
- Should it prepare a draft, or take an external action after confirmation?

### Research and source boundaries

If relevant documentation, prior examples, standards, or similar skills are available, review them before drafting. Research should reduce burden on the user, not override their authority over requirements.

If the workflow uses private communications, records, or information about people, proceed only with a legitimate purpose and clear authorization. Use the minimum relevant sources and information. Exclude unrelated personal details, respect consent and privacy expectations, and keep outputs within the appropriate access boundary. Do not use private material merely because it is technically accessible.

Use research to identify:

- Existing conventions and output standards.
- Constraints imposed by the user’s chosen system or file format.
- Reusable patterns from comparable work.
- Safety, privacy, compliance, and approval requirements.

If sources conflict or requirements remain uncertain, surface the uncertainty rather than guessing.

## 3. Choose the skill structure

A skill should be focused enough that users and the AI can predict what it does. One skill may support closely related variants, but separate unrelated jobs when they have different users, access boundaries, sources of truth, or definitions of completion.

A typical package may contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional supporting documentation
├── assets/                  # Optional templates or resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help determine whether to select the skill.
2. **Core instructions:** The process needed for most requests.
3. **Supporting resources:** Detailed references, templates, and scripts loaded only when relevant.

Keep the main instruction file readable. If it becomes large, move specialized material into clearly named references and state exactly when each reference should be used. Give long references a contents list or clear navigation.

For skills with several variants, organize resources by variant. The core instructions should explain how to select the relevant path, rather than requiring the AI to read every reference by default.

### Use reusable helpers carefully

If evaluations show that the AI repeatedly rebuilds the same reliable procedure, consider bundling a helper script, template, or checklist. A reusable helper is most valuable when it is:

- Deterministic or easier to verify than free-form reasoning.
- Reused across many requests.
- Less error-prone than recreating the procedure each time.
- Clearly within the user’s intended permission scope.

Document what each helper does, its inputs and outputs, its limitations, and when not to use it. Do not automate sensitive, destructive, or external actions without clear approval points.

## 4. Write the skill

Write in clear, imperative language. Explain the purpose behind important steps, especially when a rule prevents a predictable failure. A capable AI can adapt better when it understands the goal and tradeoff than when it receives a long list of unexplained prohibitions.

Include the following sections as appropriate.

### Purpose and scope

State the job, intended use, and boundaries. Make clear whether the skill produces advice, a chat response, a file, a draft, or an external action.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State what to do when something required is absent.

```markdown
Before preparing the report, confirm the reporting period and approved data source.
If the source is unavailable, ask for an export or prepare a draft clearly marked as incomplete.
```

### Workflow

Give the normal sequence of actions and include meaningful decision points. A durable workflow commonly follows this pattern:

1. Inspect the request and available inputs.
2. Clarify only where an answer would materially change the work.
3. Gather evidence from approved sources.
4. Perform the task using the suitable method.
5. Check the result against format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limitations.

Use conditional instructions when they help:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested action could overwrite work or create an external commitment, explain the impact and request confirmation first.
```

### Output format

When consistency matters, provide an exact or near-exact template.

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding supported by evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing information]
```

Avoid rigid templates when usefulness depends on adapting to context. In those cases, specify goals, ordering, and examples rather than a fixed shell.

### Quality, safety, and privacy checks

State what must be checked before completion. Examples include validating calculations, confirming required sections, preserving original data, identifying the source of key claims, or flagging uncertain information.

The skill’s behavior should match what a reasonable user expects from its description. Do not conceal actions, bypass authorization, expose confidential information, facilitate unauthorized access, or take destructive action without confirmation. If a request exceeds authorization or creates material risk, explain the limitation and offer a safer alternative where possible.

### Failure behavior

Describe recovery from general failure types:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or source:** Explain what cannot be verified and offer an alternative method.
- **Ambiguity:** Make a reasonable low-risk assumption if it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, report the issue, or seek guidance.
- **Permission-sensitive action:** Pause before irreversible, external, or high-impact changes.

### Examples

Use a small number of generalized examples only when each teaches a distinct decision pattern. Examples should illustrate reasoning, not replace it with narrow rules.

## 5. Write a strong skill description

The description is a routing instruction: it tells an AI what the skill does and when it is relevant. It should cover realistic user wording, including requests that imply the task without naming it directly.

A useful description includes:

- The task or outcome.
- Common contexts or phrasing that indicate the task.
- Important scope boundaries when they prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a leadership update, progress report, milestone review, risk summary, or a concise account of next steps, even if they do not use the phrase “status report.”
```

Do not put the full workflow in the description. Do not rely on vague labels such as “help with documents.” Do not make it so broad that it captures adjacent work better handled by another skill.

## 6. Review the draft before testing

Read the skill as if seeing it for the first time. Check:

- Is the job coherent and bounded?
- Does the description explain when to use it?
- Are inputs, permissions, and outputs clear?
- Does the workflow explain important quality checks?
- Does it say what happens when information is missing?
- Are there unnecessary rules, repeated wording, or brittle instructions?
- Does it depend on undeclared tools, personal habits, or private access?
- Can a capable AI handle normal variation without becoming constrained by the wording?

Prefer lean, understandable instructions over a long list of rigid commands. Excessive absolute language is a warning sign unless the behavior concerns a genuine safety, privacy, or authorization boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create two or three realistic test prompts. Share them with the user and invite corrections or additions before relying on them.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Any supplied files or context.
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
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover different meaningful situations:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic variation that changes the workflow.
- A request that should require approval, decline, or privacy protection when relevant.

Do not make tests merely repeat the skill’s phrasing. Vary wording, detail level, and user sophistication. Avoid retaining unnecessary private context in prompts or fixtures.

## 8. Run comparisons and preserve evidence

When independent execution is available, compare the skill against a meaningful baseline:

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged copy before editing, then compare the revised version with the prior version.

Run comparison conditions under comparable circumstances. If parallel execution is available, start all skill and baseline runs together to reduce timing differences and avoid changing one condition after seeing another result.

Store each iteration clearly, for example:

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

For every run, retain the prompt, permitted inputs, output, evaluation criteria, and available metadata such as elapsed time or resource use. Capture timing immediately if the execution environment reports it, since it may not remain available later.

If independent runs are unavailable, perform a transparent sanity check: follow the skill on each test request, save the results, and ask the user to review them. Do not present this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While test runs are underway, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and connected to user value:

- Required sections are present.
- A produced file opens and contains required fields.
- Calculated values match a known approved source within an agreed tolerance.
- The output identifies missing mandatory information.
- Claims include source references when required.

Record each check with a clear statement, a pass/fail result, and evidence:

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

Use programmatic validation when practical. Reusable automated checks are generally more reliable than visual inspection. Do not force numerical checks onto subjective work: tone, writing quality, design, usefulness, and strategic judgment often require human review.

## 10. Review results with a human

Present outputs and measurements in a form the user can inspect. Use an available review interface when one exists; otherwise present accessible files or a clear in-conversation comparison.

For each test case, show:

- The original prompt.
- Relevant permitted inputs.
- The skill output and comparison output, if available.
- Objective grades and evidence.
- Timing or resource data, if available.
- A way for the user to state what worked and what should change.

Ask focused questions:

- Which result would you trust in ordinary use, and why?
- Did the skill add steps or detail that were not valuable?
- What was missing, misleading, unsafe, or difficult to use?
- Would it work for a similar request with different wording or data?

Treat empty feedback as a useful signal for that case, not proof that every future case is solved.

## 11. Analyze results beyond pass rates

Aggregate results where possible: pass rate, elapsed time, resource use, and variation. Then inspect patterns that summary statistics may hide:

- **Non-discriminating checks:** Both versions pass, so the check does not measure the skill’s added value.
- **High variation:** Comparable runs differ substantially, suggesting ambiguity or unreliable instructions.
- **Tradeoffs:** Quality improves, but time or resource cost may be too high.
- **Failure concentration:** Several failures share one cause, such as unclear source selection or missing output rules.
- **Unproductive work:** Execution records show redundant planning, research, or formatting.
- **Repeated reconstruction:** Multiple runs recreate the same helper process, indicating a reusable resource may help.

For consequential decisions, consider a blind comparison. Give an independent reviewer two outputs without revealing which version produced each, use a shared rubric, record the judgment, then reveal the mapping. Judge role-relevant qualities such as correctness, completeness, clarity, adherence to constraints, safety, and practical usefulness.

## 12. Improve without overfitting

Revise the smallest part of the skill likely to fix the underlying cause. Generalize from feedback instead of adding rules that only match one test.

For example, if a report fails to distinguish unsupported claims, do not add a rule mentioning only that report. Clarify the broader principle: distinguish verified information, assumptions, and unavailable evidence whenever sources are incomplete or mixed.

Use these improvement principles:

1. Fix causes, not isolated examples.
2. Keep instructions lean and remove guidance that does not change outcomes.
3. Explain intent so the AI can adapt intelligently.
4. Add scripts, templates, or references only when repeated work justifies them.
5. Preserve behavior the user already values.
6. Add tests only for genuine classes of failure, not every one-off event.

After revision, rerun the full test set in a new iteration. Use the same baseline policy, compare against prior outputs where useful, and collect feedback again.

Stop when the user is satisfied, meaningful cases are consistently successful, objective requirements are reliably met, or further edits are not producing useful improvement.

## 13. Optimize activation behavior

After the workflow itself is stable, evaluate the description that controls when the skill is selected.

Create a realistic set of activation queries containing both cases that **should activate** the skill and difficult nearby cases that **should not**. Use roughly balanced coverage. Queries should be substantive enough that consulting a skill would be useful.

Positive cases should vary by:

- Formal and casual language.
- Direct and implied requests.
- Common and less common valid uses.
- Situations where a related skill might compete.

Negative cases should be near-misses rather than obviously irrelevant requests. They should share terms or concepts with the skill but require a different job, different access, or different conditions.

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

Review the query set with the user before using it. If repeated activation testing is available, separate improvement queries from held-out queries used to choose the final description. Select the description that performs best on held-out cases, not merely the one that fits the examples used for editing.

Remember that simple one-step requests may be handled directly without selecting a specialized skill. Test requests should therefore be complex enough that the skill would add real value.

## 14. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not rely on private conventions, undeclared access, or a specific proprietary tool.
- References and helpers are present, clearly named, and documented.
- No credentials, identifiers, confidential records, or unnecessary sensitive examples are included.
- The user can adapt the skill to their chosen environment.
- Test material is retained only if it is safe and useful to keep.

Provide a handoff note stating what the skill does, required capabilities, known limitations, approval boundaries, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has:

- A clear, bounded job.
- A description that routes appropriate requests.
- Instructions that handle normal variation.
- Explicit behavior for uncertainty, authorization, privacy, and high-impact actions.
- Evidence from realistic use that it improves outcomes.
- A package that another user can understand and adapt without relying on hidden personal context.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for real recurring work.

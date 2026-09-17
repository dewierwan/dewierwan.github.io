---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, improve an existing skill, evaluate whether a skill helps, or refine when it activates. A skill is a focused set of instructions, with optional resources such as scripts, references, and templates, that helps an AI carry out a recurring job consistently.

The core loop is:

1. Understand the intended job, boundaries, and user value.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with a person and measure objective requirements where appropriate.
5. Improve the skill using the evidence.
6. Repeat until the result is useful, reliable, and not narrowly fitted to the test examples.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the finished skill.

Do not assume every project needs every step. Some users want a quick collaborative draft. Others need a rigorous comparison. First determine where the user is in the loop, then help them make the next useful decision.

## Communication principles

Match the user’s technical vocabulary and experience. Use plain language by default. Terms such as *evaluation* and *benchmark* are often acceptable, but explain them briefly when helpful. Avoid unexplained technical terms such as “schema,” “assertion,” or “JSON” unless the user is already using them comfortably.

Explain why questions matter. For example:

> What should a successful result look like: a chat response, a structured report, a file, or an approved external action? The answer determines how the skill should work and how we can test it.

Keep the user involved at important choices:

- Confirm the intended job before writing extensive instructions.
- Ask before introducing restrictive policies, required tools, or approval steps.
- Share proposed test cases before treating them as the evaluation set.
- Let human judgment lead for subjective outcomes such as writing quality, visual design, tone, or strategic usefulness.
- State uncertainty plainly rather than inventing a requirement or pretending a result was verified.

If the proposed skill would access communications, records, files, or information about people, establish a legitimate purpose and clear authorization first. Use only the minimum relevant sources and data, omit unrelated sensitive details, respect reasonable privacy and consent expectations, and keep outputs within the user’s authorized access boundary.

## 1. Determine the starting point

Identify which starting condition applies.

### New skill

The user has an idea such as “I need help producing recurring project updates.” Start with discovery, scope, and a first draft.

### Existing skill

The user has a current instruction set and wants it edited, simplified, tested, or optimized. Read it before proposing changes. Preserve the established name and identity unless the user explicitly requests a rename.

Before modifying an installed or otherwise protected copy, work from a writable copy. Preserve an unchanged snapshot so later evaluation can compare the revision to the prior version.

### Workflow demonstrated in the conversation

The user may say “turn what we just did into a skill.” Extract what can already be inferred from the conversation:

- Inputs and source materials used.
- Tools or capabilities used.
- The sequence of actions and decisions.
- Corrections, preferences, and approval points from the user.
- Observed output format.
- Acceptance criteria and failure handling.

Summarize the inferred workflow and explicitly list gaps that need confirmation. Do not turn a one-time workaround into a general rule without checking whether it applies broadly.

### Evaluation or optimization request

The user may already have a finished-looking skill and want to know whether it is effective. Go directly to test design, evaluation, and evidence-based revision. Do not rewrite a skill only because rewriting is possible.

## 2. Capture intent and scope

Gather enough detail to define one coherent job. Do not ask every question mechanically; start with the missing information that most changes the design.

Use these questions as needed:

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What user requests, wording, or situations should cause the skill to be used?
3. **Inputs:** What information, files, references, systems, or permissions may it use?
4. **Outputs:** What should it produce, change, or recommend? Is there a required format?
5. **Success:** How will a user tell whether the output is correct, useful, or complete?
6. **Boundaries:** What should the skill not do? When should it ask a question, pause for approval, decline, or return work to the user?
7. **Variations:** Which common cases, difficult cases, exceptions, or decision points matter?
8. **Dependencies:** Does the work require a particular capability, template, reference, script, or user-provided access?
9. **Testing:** Should the skill be evaluated using representative requests?

Offer useful choices when requirements are unclear:

- “When information is missing, should the skill make a clearly marked best-effort draft or stop and ask?”
- “Should the default be concise, detailed, or selected by the user?”
- “May it use any accessible source, or only sources the user explicitly approves?”
- “Should it prepare a recommendation, or is it allowed to make a reversible change without further confirmation?”

Recommend realistic tests when the workflow is repeated, consequential, format-sensitive, or objectively checkable. For primarily subjective work, recommend a small human review set rather than forcing weak numerical measures.

### Research before drafting

If approved documentation, comparable skills, standards, example artifacts, or domain references are available, consult them before drafting. Research should reduce the burden on the user, not replace the user’s authority over goals and constraints.

Use research to identify:

- Existing conventions and output standards.
- Constraints of available file formats or capabilities.
- Reusable patterns from related work.
- Privacy, safety, compliance, or approval requirements.

If sources disagree, are incomplete, or are outside the user’s authority, present the uncertainty and ask how to proceed.

## 3. Choose the skill structure

Keep a skill focused enough that people and AI systems can predict what it does. A skill may support related variants of one job, but separate unrelated jobs that have different audiences, permissions, source-of-truth rules, or definitions of completion.

A typical package can contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional supporting documentation
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A concise name and description that support activation.
2. **Core instructions:** The workflow used in most cases.
3. **Supporting resources:** Detailed references, templates, or executable helpers loaded only when relevant.

Keep the core instruction file readable. If it grows too large, move specialized material into clearly named references and state exactly when to consult each one. Large reference documents should include a contents or navigation section.

For a skill with multiple technical or domain variants, keep a shared selection workflow in the core instructions and place variant-specific guidance in separate files. The AI should choose the relevant variant rather than load every reference by default.

### Bundle reusable helpers carefully

If repeated test runs independently reconstruct the same helper procedure, consider bundling it as a script, template, or checklist. This is especially useful for deterministic tasks such as conversion, validation, extraction, calculations, or repetitive formatting.

Add a helper only when it is clearly reusable, understandable, and within the user’s authority. Document:

- What it does.
- Its inputs and outputs.
- When to use it.
- Its limits and failure behavior.
- How it handles data safely.

Do not add automation merely because it is possible. The skill should not conceal actions, bypass access controls, extract confidential information, damage systems, or take surprising external actions.

## 4. Write the skill

Write in clear, imperative language. Explain the reason behind important instructions, especially where a rule prevents a predictable error. AI systems can adapt better when they understand the goal and tradeoff than when they receive a long list of unexplained restrictions.

Include the following sections when they fit the task.

### Purpose and scope

State the job, intended outcome, and boundaries. Clarify whether the skill produces advice, a chat response, a file, a draft, or an external action.

### Inputs and prerequisites

List required inputs, permitted sources, required capabilities, and optional materials. State what to do if a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved data source.
If a source is unavailable, ask for an export or provide a draft clearly marked as incomplete.
```

For sensitive information, specify the authorization boundary. For example, direct the AI to use only approved records relevant to the stated purpose and to exclude unnecessary personal details from the result.

### Workflow

Describe the normal sequence and the meaningful decisions. A durable general pattern is:

1. Inspect the request and available inputs.
2. Confirm ambiguity only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Complete the task using the appropriate method.
5. Validate the result against the requested format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limitations.

Use conditional rules rather than attempting to list every possible situation:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested action could overwrite important work, explain the impact and request confirmation first.
```

### Output format

Use a stable template when consistency matters:

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

Do not impose a rigid structure if the value of the task depends on adapting to context. In that case, define the desired qualities and show a short generalized example instead.

### Quality, safety, and readiness checks

State what must be checked before the skill presents work as complete. Suitable checks include:

- Required fields, sections, or files are present.
- Calculations are validated against an approved source.
- Important claims identify their supporting source.
- Original data is preserved when modification is risky.
- Assumptions and gaps are visible to the user.
- External, irreversible, or high-impact actions have the required approval.

The actual behavior of the skill should match what its description reasonably leads a user to expect. Refuse or redirect requests that would enable unauthorized access, deception, harmful surveillance, data exfiltration, destructive behavior, or other actions outside legitimate authority.

### Failure behavior

Define recovery behavior in general terms:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or source:** State what could not be checked and offer a safe alternative.
- **Ambiguous request:** Make a low-risk assumption only if it does not materially affect the outcome; otherwise ask.
- **Validation failure:** Correct the issue, mark the output incomplete, or request guidance. Do not present an unverified result as final.
- **Permission-sensitive action:** Pause for confirmation before external, irreversible, or high-impact changes.

### Examples

Use only a few short, generalized examples when they teach a distinct pattern. Examples should illustrate reasoning or format, not replace reasoning with a narrow collection of cases.

## 5. Write the activation description

The skill description is a routing instruction. It should state both what the skill does and when it should be consulted.

A strong description includes:

- The outcome or job.
- Common contexts and user phrasing that signal the job.
- Important scope limits that prevent costly or unsafe false activation.

Example:

```text
Create clear project status reports from approved updates and source material. Use for requests for progress summaries, leadership updates, milestone reviews, risks, blockers, or next steps, including requests that imply a status report without naming one.
```

Cover realistic wording, including requests that imply the task instead of naming it. Do not place the full procedure in the description. Do not make the wording so broad that it captures unrelated work better handled by another skill.

## 6. Review the draft before testing

Read the draft as if encountering it for the first time. Check:

- Is the job coherent and appropriately bounded?
- Does the description explain when to activate the skill?
- Are inputs, permissions, sources, outputs, and completion criteria clear?
- Does the workflow handle normal variation and missing information?
- Are safety and privacy boundaries explicit where needed?
- Are there repeated instructions, brittle wording, or unnecessary rules?
- Does the skill assume a particular person’s habits, access, tools, or terminology?
- Does a capable AI have enough flexibility to solve normal cases well?

Prefer lean, understandable instructions. Excessive absolute language is a warning sign unless the behavior is truly non-negotiable, such as an authorization boundary or safety requirement.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user before relying on them. Add more cases after the first iteration when a new case represents a meaningful category of work or failure.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

A portable record format is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates. Flag information you cannot verify.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful variation:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or policy-sensitive request.
- A realistic edge case that changes the workflow.
- A request requiring approval, safe redirection, or refusal when relevant.

Avoid tests that merely repeat the skill’s wording. Vary detail level, phrasing, and user sophistication. Do not use personal or confidential scenarios when a generalized equivalent will test the same capability.

## 8. Run comparisons and preserve evidence

When independent execution is available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged copy before editing and compare the revision against that prior version, or against the previous iteration when that is the more useful decision baseline.

Start all configurations under comparable conditions. If parallel execution is available, launch the skill and comparison runs for every test case together. This reduces environmental differences and avoids selectively creating baselines later.

Organize artifacts by iteration and descriptive test name:

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

For each test, save metadata containing the prompt, a descriptive name, and the checks to be applied. Preserve supplied inputs, outputs, and any available execution information. Capture timing, resource use, and other run metadata immediately when reported, because some systems do not retain it afterward.

If independent comparisons are not available, run a transparent sanity check: follow the skill on each test prompt, preserve the outputs, and ask the user to review them. Do not claim that this is a rigorous baseline evaluation.

## 9. Define and grade objective checks

While runs are in progress, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A produced file opens and has required fields.
- Calculated values match an approved source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- Required source references or approval notes are included.

Record each grade with stable fields for the requirement text, pass/fail result, and supporting evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when required source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests it before finalization."
    }
  ]
}
```

Use programmatic checks when practical. They are generally faster, more repeatable, and reusable across iterations. Do not force numerical checks onto subjective work. Tone, clarity, aesthetics, usefulness, and judgment often require human review; weak proxy measures can cause the skill to optimize for the metric rather than the user’s actual goal.

## 10. Review results with a human

Present both qualitative outputs and quantitative results. Use an available review interface when one exists; otherwise provide accessible files or a clear in-conversation comparison.

For each test case, show:

- The original prompt and relevant inputs.
- The skill output and comparison output, when available.
- Objective grades and evidence.
- Timing or resource information, if available.
- Prior iteration output and feedback, when useful.
- A clear way for the user to leave feedback.

Ask focused review questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, unsafe, or difficult to use?
- Did the skill add work or detail that did not create value?
- Would this work for similar requests with different wording or data?

If a review interface can export feedback, save that feedback with the iteration artifacts. Empty feedback can mean a result is acceptable, but it is not proof that the skill is generally solved. Review the outputs and measurements as well.

## 11. Analyze results beyond pass rates

Aggregate results when possible: pass rate, average duration, average resource use, variation, and differences from the baseline. Present the revised skill before its comparison condition for easier reading.

Then look beyond summary numbers for patterns:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill’s added value.
- **High variation:** Similar runs differ substantially, suggesting ambiguity, unstable conditions, or brittle instructions.
- **Tradeoffs:** The skill improves quality but adds disproportionate time or resource use.
- **Failure concentration:** Multiple failures share one cause, such as unclear source selection or weak output rules.
- **Unproductive work:** Execution traces reveal redundant planning, research, formatting, or tool use.
- **Repeated reconstruction:** Multiple runs recreate the same helper process, indicating a reusable resource may help.

A small benchmark is evidence for the next iteration, not conclusive proof of general quality.

## 12. Improve without overfitting

Revise based on user feedback, outputs, grades, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from complaints. If one test output fails to identify a source limitation, do not add a rule tied only to that exact prompt. Clarify the general behavior: when evidence is incomplete, mixed, or uncertain, distinguish supported information from assumptions and missing data.

Use these principles:

1. **Fix causes, not examples.** Design for future requests, not only the current tests.
2. **Keep instructions lean.** Remove rules that do not improve behavior or create wasted effort.
3. **Explain intent.** State why a step protects correctness, usability, safety, or privacy.
4. **Add reusable resources only when justified.** Bundle scripts, templates, or references when repeated work shows their value.
5. **Preserve useful behavior.** Avoid broad revisions that remove features users already value.
6. **Expand coverage gradually.** Add tests for real categories of failure rather than every isolated incident.

After revision, rerun the full evaluation set in a new iteration and apply the same baseline policy. Show new results alongside previous results when possible. Stop when the user is satisfied, feedback is consistently positive across meaningful tests, objective requirements are reliably met, or further edits no longer make meaningful progress.

## 13. Optional blind comparison

For a more rigorous comparison between two versions, use a blind review. Give an independent evaluator two outputs without identifying which version produced each output. Ask it to judge against a shared rubric, then reveal the mapping only after the judgment is recorded.

Use blind comparison when versions have similar measured performance but visibly different quality, when preference bias is a concern, or when the decision matters enough to justify additional review. Base the rubric on user value: correctness, completeness, clarity, adherence to constraints, safety, privacy, and practical usability.

Analyze why the preferred output won before changing the skill again.

## 14. Optimize triggering behavior

Only optimize the activation description after the skill’s workflow is already useful. Create a realistic set of requests that should activate the skill and nearby requests that should not.

Use a roughly balanced set, commonly eight to ten cases in each group. Make prompts substantive enough that consulting a specialized skill would help.

Positive cases should vary in wording and context:

- Formal and casual requests.
- Directly named and implicitly requested work.
- Common and less common valid uses.
- Cases where a related skill might compete but this one is the better fit.

Negative cases should be challenging near-misses, not obviously irrelevant requests. They should share vocabulary or context with the skill but actually require a different job, capability, or scope.

```json
[
  {
    "query": "I need a concise update for leadership from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what project status reports are generally used for?",
    "should_trigger": false
  }
]
```

Review the query set with the user before evaluating descriptions. If repeated testing is available, separate examples used to improve a description from held-out examples used to select it. Choose the description that performs best on held-out requests, not merely the one that fits the editing set.

Remember that an AI may handle a simple one-step request directly without consulting a skill, even if the description matches. Test with sufficiently complex requests where the skill’s guidance would add real value.

Show the user the before-and-after description and the test results before applying the final version.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description truthfully states what activates the skill.
- The instructions do not depend on personal conventions, undeclared access, or a specific tool unless clearly documented.
- Scripts, references, and assets are included only when needed and are clearly named.
- No credentials, confidential data, unique identifiers, private records, or sensitive examples are included.
- Data-handling guidance respects authorization, purpose limitation, and privacy expectations.
- The user can install or adapt the package in their chosen environment.
- Test material is retained only when safe and useful.

Provide a handoff note explaining what the skill does, required capabilities, known limitations, how to test it after installation, and when users should seek confirmation rather than rely on automation.

## Final readiness gate

A skill is ready when it has:

- A clear, bounded job.
- An honest description that activates for appropriate requests.
- Instructions that handle normal variation and missing information.
- Explicit boundaries for authorization, privacy, uncertainty, and high-impact actions.
- A usable output format or adaptable presentation guidance.
- Evidence from realistic use that it improves outcomes.
- No unnecessary dependence on a particular person, organization, platform, or private operating environment.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user needs.

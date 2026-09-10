---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging reusable AI skills from new ideas, existing instructions, or demonstrated workflows. It supports lightweight collaboration as well as rigor.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing skill, assess whether a skill improves results, or improve when a skill activates. A skill is a focused set of instructions, with optional resources, that helps an AI perform a recurring job more consistently.

The core improvement loop is:

1. Define the job and its boundaries.
2. Draft or revise the skill.
3. Test it using realistic requests.
4. Review outputs with the user and measure objective requirements when appropriate.
5. Improve the instructions based on evidence.
6. Repeat until the skill is useful, reliable, and not narrowly fitted to the test examples.
7. Optionally improve the skill description so it activates for the right requests.

Adapt the level of rigor to the user’s needs. A user may want a quick collaborative draft, a small sanity check, or a structured benchmark. First identify where they are in the loop, then help them take the next useful step. Do not insist on formal testing when the user explicitly prefers an exploratory or informal approach, but explain what confidence they give up by skipping it.

## Communication principles

Match the user’s technical level and preferred vocabulary. Use plain language by default. Words such as *evaluation* and *benchmark* are often understandable, but define them briefly if helpful. Avoid unexplained terms such as “schema,” “assertion,” or “JSON” unless the user has signaled familiarity or asks for implementation detail.

Explain why key questions matter. For example:

> What should a successful result look like: a chat response, a structured report, a file, or an approved action? The answer determines how the skill should work and how we can check it.

Keep the user involved in consequential decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before imposing strict scope, a tool dependency, or an approval requirement not already required by the task.
- Share proposed test cases before treating them as the test suite.
- Let human judgment lead for subjective qualities such as tone, visual design, creative value, and strategic usefulness.
- State uncertainties rather than presenting assumptions as facts.

## 1. Determine the starting point

Identify which of these situations applies.

### New skill

The user has an idea for a recurring capability, such as preparing consistent project updates. Begin with discovery, scope, and a first draft.

### Existing skill

The user already has a skill and wants to edit, simplify, test, repair, or optimize it. Read the current instructions before proposing changes. Preserve its established name and identity unless the user explicitly asks to rename it. If the installed copy cannot be edited directly, work from an authorized writable copy and keep the original unchanged.

### Workflow already demonstrated

The user may say, “Turn what we just did into a skill.” Extract as much as possible from the conversation before asking questions:

- Inputs and reference materials provided.
- Approved tools, sources, or capabilities used.
- Sequence of decisions and actions.
- Corrections and preferences expressed by the user.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow and list missing details for confirmation. Do not convert a one-time workaround into a permanent rule without checking whether it applies broadly.

### Evaluation or activation request

The user may have a finished-looking skill and ask whether it works, whether a revision is better, or whether it triggers at suitable times. Start with test design and evidence gathering. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent, scope, and authorization

Before drafting, collect enough information to define a coherent job. Ask only the questions that are still materially unclear, but cover these areas as needed:

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What user requests, wording, or contexts should make the skill relevant?
3. **Inputs:** What files, systems, examples, sources, and permissions can it use?
4. **Outputs:** What should it produce, change, recommend, or hand back? Is a format required?
5. **Success:** How will the user decide that the output is correct, useful, safe, and complete?
6. **Boundaries:** What should the skill not do? When should it ask, stop, or offer alternatives?
7. **Variation:** What common cases, difficult cases, exceptions, or failure conditions matter?
8. **Dependencies:** Does it require user-selected capabilities, templates, references, scripts, or domain standards?
9. **Testing:** Should it be tested with representative requests before release?

Offer useful choices when they reduce ambiguity:

- “Should the skill make a clearly labeled best-effort draft when information is missing, or pause and ask for the missing information?”
- “Should it use a concise default, a detailed default, or let the user choose?”
- “Should it use any source the user supplies, or only approved sources of record?”

### Private information and access boundaries

If the skill uses private communications, records, files, or information about people, confirm a legitimate purpose and clear authorization before accessing or processing them. Use only the minimum relevant sources and data. Omit unrelated sensitive details from outputs, respect consent and reasonable privacy expectations, and keep the result within the requester’s appropriate access boundary.

For a people-related workflow, focus on role-relevant facts, evidence, and outcomes. Do not infer sensitive attributes or make claims beyond the available evidence. For hiring or assessment, describe role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance.

### Research before drafting

When approved documentation, relevant examples, standards, or comparable skills are available, review them before drafting. Research should reduce burden on the user, not override the user’s requirements.

Use research to identify:

- Existing conventions and output standards.
- Constraints from a file type, system, or user-selected capability.
- Reusable patterns for comparable jobs.
- Safety, privacy, compliance, and approval requirements.

If sources conflict, are incomplete, or cannot be verified, explain the uncertainty and ask the user to choose where necessary.

## 3. Choose a maintainable skill structure

A skill should be focused enough that users and the AI can predict what it does. It may support several variants of the same job, but separate unrelated jobs when they differ in audience, authority, sources of truth, or definition of completion.

A typical portable package can contain:

```text
skill-name/
├── SKILL.md              # Core instructions
├── scripts/              # Optional repeatable helpers
├── references/           # Optional supporting documentation
├── assets/               # Optional templates or output resources
└── evals/                # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata or description:** A short statement that helps determine when the skill applies.
2. **Core instructions:** The workflow needed for ordinary use.
3. **Supporting resources:** Detailed references, templates, or scripts consulted only when relevant.

Keep core instructions readable and reasonably compact. If they grow too large, move specialized material into clearly named files and state exactly when to consult each file. Give long references a table of contents or clear navigation.

For multiple variants, place selection logic in the main instructions and variant details in separate resources. For example, a deployment skill could select the appropriate hosting environment first, then read only the matching reference rather than loading every provider’s instructions.

### Bundle deterministic work only when justified

If several test runs independently reconstruct the same helper procedure, consider bundling a script or template. Good candidates include repeatable file transformations, validation, report assembly, data cleanup, or calculations.

Add a resource only when it is reusable, easier to verify than repeated free-form reasoning, safer or less error-prone, and within the intended authorization boundary. Document its inputs, outputs, limits, and when not to use it. Do not automate actions that users would find surprising or that require ungranted access.

## 4. Write the skill

Write in clear, imperative language. Explain the reason behind instructions that prevent predictable failures. AI systems can often adapt better when they understand the goal and tradeoff than when they receive a long list of unexplained commands.

Include the following sections when applicable.

### Purpose and scope

State the job, intended outcome, normal users, and boundaries. Make clear whether the skill produces advice, a file, a report, an external action, or a guided process.

### Inputs and prerequisites

List required information, permitted sources, necessary capabilities, and optional inputs. State what to do when something required is unavailable.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask the user for an export or provide a draft clearly labeled as incomplete.
```

### Workflow

Describe the normal sequence, including meaningful decision points rather than attempting to enumerate every possible incident.

A durable sequence is often:

1. Inspect the request and available inputs.
2. Clarify requirements only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Complete the requested task using an appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limits.

Use conditional instructions where useful:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested change could overwrite important work or cause an external effect, describe the impact and request confirmation before proceeding.
```

### Output format

When consistency matters, provide an exact or near-exact format:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or required follow-up]
```

Avoid rigid templates when quality depends on adaptation to context. In those cases, specify the intended audience, required content, and quality goals instead.

### Quality, safety, and privacy checks

State the checks needed before completion. Examples include required fields, calculation verification, source attribution, preserving originals, flagging uncertainty, and confirmation before high-impact actions.

The skill must act in ways a user would reasonably expect from its description. Do not design skills that hide actions, bypass authorization, expose confidential information, damage systems, or facilitate unauthorized access. If the requested work is deceptive, unsafe, or beyond the requester’s authority, explain the limitation and offer a safe alternative when possible.

### Failure behavior

Describe broad recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** Explain what could not be verified and offer an approved alternative.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially change the outcome; otherwise ask.
- **Validation failure:** Do not describe the output as complete. Correct it, report the issue, or seek guidance.
- **Permission-sensitive action:** Pause for confirmation before irreversible, external, financial, legal, or otherwise high-impact actions.

### Examples

Include a small number of generalized examples only when each teaches a distinct pattern. Examples should illustrate good reasoning and output shape, not replace the workflow with a collection of narrow cases.

## 5. Write a strong activation description

The description is a routing instruction. It should say both **what the skill does** and **when it should be used**. Cover realistic language users may use, including requests that imply the task without naming it directly.

A useful description includes:

- The outcome or job.
- Common contexts or phrases that indicate relevance.
- Important scope limits that prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use for requests for progress summaries, leadership updates, milestone reviews, risks, decisions, or next steps, including requests that imply a status report without using that phrase.
```

Do not put the full procedure in the description. Avoid vague labels such as “help with documents,” and do not make the description so broad that it captures nearby work better served by another skill.

## 6. Audit the draft before testing

Read the draft as a new user and a new AI would. Check:

- Is the job coherent and bounded?
- Does the description clearly indicate when it applies?
- Are inputs, authority, permissions, and outputs clear?
- Does the workflow explain why important checks exist?
- Does it handle missing information and unavailable dependencies?
- Does it rely on private conventions, undeclared tools, or personal access?
- Are rules redundant, brittle, or overly restrictive?
- Does a capable AI have room to adapt to ordinary variation?

Prefer lean instructions over long instruction files filled with rules that do not change results. Repeated absolute wording is a warning sign unless the behavior is genuinely non-negotiable, such as respecting authorization or preserving confidential information.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user before relying on them and invite additions or corrections.

For each test, record:

- A descriptive identifier.
- The user prompt.
- Input files or supplied context.
- Expected outcome in plain language.
- Objective checks, if suitable.

A portable test structure is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and identify information that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful conditions, such as:

- A typical successful request.
- Incomplete or ambiguous information.
- A format-sensitive or rule-sensitive request.
- A realistic case that changes the workflow.
- A request that should require approval, cautious handling, or refusal, when relevant.

Vary wording, detail level, and user style. Do not make tests merely repeat the skill’s own language. Avoid retaining personal scenarios or sensitive source material when generalized examples can test the same behavior.

## 8. Run fair comparisons

When independent execution is available, compare the skill with a meaningful baseline.

- For a new skill, compare a run using the skill with a comparable run without it.
- For an existing skill, preserve an unchanged authorized snapshot before editing, then compare the revised version with the prior version.

Run both conditions under comparable circumstances. When possible, start all skill and baseline runs together to reduce timing differences. Keep each iteration separate, for example:

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

Preserve the prompt, supplied inputs, output, and available metadata such as elapsed time and resource use. Record timing when the execution environment reports it because it may not remain available later.

If independent runs are unavailable, conduct a transparent sanity check: follow the skill for each test prompt, save the results, and ask the user to review them. Do not present this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While tests are running, draft objective checks when they genuinely measure user value. Explain them before treating them as success criteria.

Good checks are observable and meaningful:

- Required sections are present.
- A generated file opens and has required fields.
- Calculations match an agreed source within a defined tolerance.
- Missing mandatory inputs are identified.
- Important claims include source references when required.

Record each check with clear text, pass/fail status, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when information is incomplete.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests follow-up."
    }
  ]
}
```

Use programmatic validation where practical. Automated checks are repeatable and can be reused across iterations. Do not force numerical scoring onto subjective work; writing quality, judgment, tone, and design often require human review.

## 10. Review results with the user

Present qualitative outputs and quantitative results together. Use any available review method that lets the user inspect each prompt, supplied context, output, comparison output, grades, and available timing data. If no review interface exists, present accessible files or a clear conversational review.

Ask focused questions:

- Which result would you trust in ordinary use, and why?
- What was missing, misleading, too costly, or difficult to use?
- Did the skill add work that did not create value?
- Would the result work for similar requests with different wording or data?

Empty feedback can mean a tested case is acceptable, but it does not prove the skill is generally solved. Consider outputs and objective evidence as well.

## 11. Analyze beyond aggregate scores

Aggregate pass rates, time, resource use, and variation when possible. Then inspect patterns that averages may hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill’s contribution.
- **High variation:** Comparable runs differ substantially, suggesting ambiguity, instability, or weak instructions.
- **Tradeoffs:** Quality improves, but time or resource use may be disproportionate.
- **Failure concentration:** Several failures may share a root cause such as unclear source selection.
- **Unproductive work:** Execution evidence shows redundant planning, research, or formatting.
- **Repeated reconstruction:** Multiple runs recreate the same helper process, suggesting a resource should be bundled.

Treat a small test set as evidence for the next revision, not final proof.

## 12. Improve without overfitting

Revise based on user feedback, outputs, and analysis. Change the smallest part likely to address the underlying cause.

Generalize from complaints. If one result omits source notes, do not add a rule naming that exact test. Clarify the broader condition: when evidence is incomplete or mixed, separate verified facts from assumptions and identify what cannot be confirmed.

Use these principles:

1. Fix causes, not individual examples.
2. Keep instructions lean and remove guidance that does not help.
3. Explain intent so the AI can adapt intelligently.
4. Add scripts, templates, or references only when repeated work demonstrates their value.
5. Preserve behavior the user already values.
6. Add tests only for real classes of failure, not every isolated incident.

After revising, rerun the relevant test set in a new iteration, using the same baseline policy. Show previous outputs or feedback alongside new outputs when useful.

Stop when the user says the skill is ready, feedback is consistently positive across meaningful cases, objective requirements are reliable, or further revisions are not producing meaningful improvement.

## 13. Optional blind comparison

For a more rigorous comparison between two versions, use blind review. Give an independent evaluator two outputs without identifying their origins. Ask for a judgment against a shared rubric, then reveal the mapping only after the assessment is recorded.

Use blind review when versions have similar metrics, qualitative judgment is important, or the decision has meaningful cost. Tie the rubric to correctness, completeness, clarity, constraint adherence, safety, and practical usability. Analyze why one result was preferred before changing the skill.

## 14. Optimize triggering behavior

After the workflow itself is useful, test the description that controls activation. Build a realistic set of requests that should trigger and nearby requests that should not. Use roughly balanced coverage and include enough detail that consulting a skill would actually be useful.

Positive examples should include formal and casual wording, direct and implied requests, common and uncommon valid cases, and cases where related skills could compete.

Negative examples should be challenging near-misses, not irrelevant requests. They should share language or concepts with the skill but belong to a different job, need another capability, or lack the conditions that make the skill appropriate.

```json
[
  {
    "query": "I need a concise leadership update from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Explain what project status reports are and why teams use them.",
    "should_trigger": false
  }
]
```

Review the query set with the user. If the environment supports repeated activation testing, separate cases used to refine the description from held-out cases used to choose it. Select the description that performs best on held-out cases, not merely on the cases used during editing.

Simple one-step requests may not activate a specialized skill even with a strong description because an AI can handle them directly. Make activation tests substantive enough that using the skill would add real value.

## 15. Package and hand off

Package the core instructions and only resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on private conventions, hidden access, or undeclared tools.
- Scripts and references are present, clearly named, and documented.
- No credentials, private identifiers, confidential data, or unnecessary personal details remain.
- The user can install or adapt the package in their chosen environment.
- Test material is retained only when it is safe and useful.

Provide a handoff note describing what the skill does, required capabilities, known limitations, permission boundaries, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an honest description that routes suitable requests, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.

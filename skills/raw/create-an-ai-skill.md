---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and handing off a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, improve an existing one, evaluate whether it helps, or refine when it activates. A skill is a focused set of instructions, plus optional resources, that helps an AI perform a recurring job reliably.

The core loop is:

1. Understand the job, outcome, and boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements where useful.
5. Improve the skill from evidence.
6. Repeat until the skill is useful, reliable, and not tailored only to the tests.
7. Optionally improve the description that controls activation.

Do not force every project through every stage. A user may want a quick draft, an informal collaborative review, or a rigorous comparison. Identify where they are in the loop and take the next useful step.

## Communicate clearly and safely

Match the user’s technical vocabulary and experience. Use plain English by default. Briefly explain terms such as *benchmark*, *assertion*, or *structured data* when they matter and the user has not shown familiarity with them.

Explain why important questions matter. For example: “What should a successful result look like—an answer, a report, a file, or an external action? That determines how we design and test the skill.”

Keep the user involved in decisions that affect scope, permissions, quality standards, or tradeoffs:

- Confirm the intended job before writing extensive instructions.
- Ask before choosing restrictive rules, required capabilities, or approval policies.
- Share proposed test cases before treating them as the evaluation set.
- Let human review lead for subjective qualities such as tone, visual design, creative value, and strategic judgment.
- Be clear about what was tested, what was not tested, and what cannot be verified.

If the work involves private communications, records, or information about people, require a legitimate purpose and clear authorization. Use only the minimum relevant sources and details. Keep outputs within the user’s proper access boundary, and omit unrelated or sensitive personal information.

## 1. Identify the starting point

First determine which situation applies.

### New skill

The user has an idea for recurring work. Start with discovery, then create a first draft.

### Existing skill

The user has a draft or installed skill and wants it edited, simplified, tested, or improved. Read the existing instructions first. Preserve its established name and identity unless the user asks to change them.

### Workflow demonstrated in the conversation

If the user says “turn what we just did into a skill,” extract what is already known before asking questions:

- Inputs, files, and approved sources used.
- The sequence of decisions and actions.
- Tools or capabilities that were needed.
- Corrections, preferences, and acceptance criteria stated by the user.
- Output format and conditions that changed the approach.

Summarize the inferred workflow, distinguish facts from assumptions, and ask the user to confirm important gaps. Do not turn a one-time workaround into a general rule without confirmation.

### Evaluation or activation request

If the user wants to know whether a skill works, or whether it activates at the right time, begin with test design and evidence gathering. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough detail to define a coherent job. Adapt these questions rather than asking all of them mechanically.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What kinds of requests, wording, or situations should use it?
3. **Inputs:** What information, examples, files, capabilities, and approved systems may it use?
4. **Outputs:** What should it produce, change, or recommend? Is a format required?
5. **Success:** How will the user know the result is correct, useful, or complete?
6. **Boundaries:** What should the skill not do? When should it ask, pause for approval, decline, or hand work back?
7. **Variation:** Which common cases or meaningful exceptions change the approach?
8. **Dependencies:** Does it need templates, references, reusable helpers, or user-provided access?
9. **Testing:** Should it be tested with realistic requests before release?

Recommend testing when outputs are objectively checkable, the work is consequential, or the skill will be used repeatedly. For highly subjective work, a small set of human-reviewed examples is often more valuable than artificial metrics.

Useful choices include:

- “When information is missing, should the skill make a clearly labeled best effort or stop and ask?”
- “Should the default output be concise, detailed, or selected by the user?”
- “May it use any available source, or only sources the user approves?”
- “Which external, irreversible, or high-impact actions require confirmation?”

### Research before drafting

When relevant documentation, comparable skills, approved references, or domain standards are available, consult them before drafting. Research should reduce burden on the user, not replace their authority over requirements.

Use it to identify conventions, environmental constraints, reusable patterns, and safety or approval requirements. If sources conflict or uncertainty remains, state that rather than guessing.

## 3. Choose a maintainable structure

Keep a skill focused enough that users and AI can predict what it does. One skill may support closely related variants, but separate unrelated jobs when they have different audiences, permissions, trusted sources, or completion criteria.

A typical package can contain:

```text
skill-name/
├── SKILL.md          # Core instructions
├── scripts/          # Optional deterministic helpers
├── references/       # Optional detailed guidance
├── assets/           # Optional templates or output resources
└── evals/            # Optional test and grading material
```

Use progressive disclosure:

1. **Metadata:** A short name and activation description.
2. **Core instructions:** The workflow needed in ordinary use.
3. **Supporting resources:** Detailed references, templates, and helpers consulted only when relevant.

Keep the core instructions readable. If they become unwieldy, move variant-specific or detailed material into clearly named references and state exactly when to read them. Large references should include clear navigation.

Add a reusable helper only when repeated work demonstrates its value. Good candidates are deterministic procedures such as conversion, validation, or structured-data checks. Document its purpose, inputs, outputs, limitations, and authorization boundary. Do not automate merely because automation is possible.

## 4. Write the skill

Write in clear, imperative language. Explain the reason behind important instructions, especially when they prevent a predictable quality, safety, privacy, or usability failure. Prefer a capable AI’s informed judgment over long lists of unexplained prohibitions.

Include the following sections where applicable.

### Purpose and scope

State the job, expected result, intended user, and boundary. Make clear whether the skill creates an answer, produces a file, performs an action, or guides a process.

### Inputs and prerequisites

List required information, allowed sources, needed capabilities, and optional inputs. State what happens when a required input is absent.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or provide a draft clearly marked as incomplete.
```

For personal or private data, require a legitimate purpose, clear authorization, and minimum necessary use. Do not direct the AI to gather unrelated records, infer sensitive information, or disclose details that are not needed for the task.

### Workflow

Give the normal sequence and key decisions rather than attempting to list every edge case.

A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Ask focused questions only when the answer materially changes the work.
3. Gather evidence from approved, relevant sources.
4. Perform the task using an appropriate method.
5. Check the result against requested format and success criteria.
6. Present the result with relevant assumptions and unresolved limitations.

Use conditional instructions when they clarify real choices:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested action could overwrite important work or affect an external system, explain the impact and request confirmation first.
```

### Output format

When consistency matters, define a template:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing input]
```

Avoid rigid formatting when usefulness depends on context. In those cases, specify required content and quality goals, with a small example only when it teaches a distinct pattern.

### Quality, safety, and failure behavior

State the checks needed before completion. Depending on the work, these may include required fields, calculation validation, source support, preservation of original data, clear separation of facts from assumptions, and uncertainty flags.

The skill must behave as users would reasonably expect from its description. Do not hide actions, bypass authorization, enable unauthorized access, extract confidential material without authority, damage systems, or misrepresent results.

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or source:** Explain what cannot be verified and offer a safe alternative if available.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially change the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, report the issue, or seek guidance.
- **External or high-impact action:** Pause for confirmation before proceeding.

## 5. Write an effective activation description

The description is a routing instruction. It should say both what the skill does and when to use it. Cover realistic wording, including requests that imply the task without naming it.

A good description includes:

- The outcome or task.
- Common contexts that signal relevance.
- Important scope limits that prevent harmful or costly false activation.

Example:

```text
Create clear project status reports from approved updates and source material. Use for progress summaries, milestone reviews, leadership updates, risks, blockers, and next steps, including requests that imply a status report without using that phrase.
```

Do not put the whole procedure in the description. Avoid vague labels and descriptions so broad that they capture nearby work better handled by another skill.

## 6. Audit the draft before testing

Read the draft as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description say when it should activate?
- Are inputs, outputs, trusted sources, permissions, and dependencies clear?
- Does the workflow handle missing, conflicting, and sensitive information appropriately?
- Are important checks explained?
- Are there duplicate rules, brittle wording, or undeclared assumptions about tools or local practices?
- Does it leave enough judgment for normal variation?

Prefer a lean, understandable skill over a long prompt with rules that do not affect behavior. Strong absolute language is usually a warning sign unless it protects a genuine safety, authorization, or integrity boundary.

## 7. Design realistic tests

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user before relying on them. Each test should record a descriptive name, prompt, supplied files or context, expected outcome, and objective checks when suitable.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and flag anything that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful situations: a normal request, incomplete or ambiguous input, a format-sensitive task, and a case involving approval, privacy, or safe refusal when relevant. Vary phrasing and detail. Test general categories of difficulty rather than retaining private incidents.

## 8. Run comparisons and preserve evidence

When independent execution is available, compare the skill with a meaningful baseline:

- For a new skill, run each test with the skill and without it.
- For an existing skill, preserve an unchanged snapshot before editing and compare the revision with the earlier version.

Run the compared conditions under similar circumstances. If parallel work is available, start the skill and baseline runs for all tests together. Preserve each prompt, relevant inputs, output, and available metadata such as elapsed time or resource use. Record timing as it is reported because some systems do not retain it.

Use an iteration structure such as:

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

If independent comparison is unavailable, perform a transparent sanity check: apply the skill to each test, save or present results, and ask the user to review. Do not describe this as a rigorous baseline comparison.

## 9. Grade what can be measured

While tests run, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful: required sections exist, a file opens with required fields, calculations match approved data within a defined tolerance, mandatory missing input is identified, or required sources are referenced.

Record a statement, result, and evidence for each check:

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

Use programmatic checks when practical because they are repeatable and reusable. Do not force numerical checks onto writing quality, design, usefulness, or judgment; those require human review.

## 10. Review, analyze, and improve

Present outputs and measurements in a form the user can inspect before making major revisions. Use an available review interface; otherwise provide accessible files or a clear conversational comparison. For each test, show the prompt, relevant context, compared outputs, grades with evidence, and available timing or resource data.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add effort or detail without value?
- Would this work with different wording or data?

Aggregate results where possible, but look beyond pass rates. Watch for checks that pass in every condition, unstable results, quality-versus-cost tradeoffs, repeated failures with one root cause, unproductive execution work, and repeated reconstruction of the same helper procedure.

Revise the smallest part of the skill likely to address the underlying cause. Generalize from feedback instead of adding rules that only solve one test example. Preserve useful behavior, remove instructions that do not help, and add resources only when repeated evidence justifies them.

Rerun the relevant test set in a new iteration and compare it with the same baseline policy. Stop when the user is satisfied, meaningful tests are consistently successful, further revisions do not help, or remaining issues require unavailable information or a product decision.

## 11. Optional blind comparison and activation testing

For an important choice between two versions, use blind comparison. Give an independent reviewer two unlabeled outputs and a shared rubric based on correctness, completeness, clarity, constraint adherence, privacy and safety handling, and practical usefulness. Reveal which version produced each output only after the judgment.

After the skill itself is stable, test its activation description. Create a balanced set of realistic, substantive requests that should activate the skill and difficult near-misses that should not. Positive examples should vary in wording and context; negative examples should be adjacent tasks, not obviously irrelevant ones.

Review the set with the user. If repeated testing is available, separate examples used to improve the description from held-out examples used to choose it. Select the description by held-out performance to reduce overfitting. Remember that simple one-step requests may not consult a specialized skill even when its description matches; test requests where the skill would clearly add value.

## 12. Package and hand off

Package only the core instructions and resources needed for normal use. Before delivery, verify that:

- The name is stable and appropriate.
- The activation description is accurate.
- The skill has no private conventions, undeclared capabilities, confidential data, credentials, identifiers, or sensitive examples.
- References and helpers are present, clearly named, and documented.
- The user can install, access, or adapt it in their chosen environment.
- Retained test materials are safe and useful.

Provide a short handoff note describing the skill’s purpose, required capabilities, known limitations, authorization expectations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an honest activation description, instructions that handle normal variation, explicit behavior for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring work.

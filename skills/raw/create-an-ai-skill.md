---
name: create-an-ai-skill
description: Create, revise, test, evaluate, and package a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation. Use this workflow to build skills that are clear, safe, evidence-based, and adaptable to the AI.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, improve an existing one, assess whether a skill helps, or turn a repeated conversation workflow into instructions another AI can follow. A skill is a focused set of instructions, plus optional scripts, references, templates, and tests, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the intended job and its limits.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements where appropriate.
5. Improve the skill from evidence rather than guesswork.
6. Repeat until the skill is reliable enough for its intended use.
7. Optionally improve the description that determines when the skill activates.
8. Package and hand off the final skill.

Do not assume every project needs a full benchmark. Some users want a quick draft, a collaborative exploratory session, or a simple sanity check. First determine where the user is in the loop, then help them take the next useful step.

## Communication principles

Match the user’s technical background. Use plain language by default and briefly define unfamiliar terms. For example, explain that an *evaluation* is a repeatable test of whether the skill produces the needed result, and that an *assertion* is a specific pass/fail check.

Keep the user involved at consequential decisions:

- Confirm the intended job before writing a large instruction set.
- Ask before selecting a narrow scope, mandatory tool, external action, or approval policy.
- Share proposed test prompts before treating them as the evaluation set.
- Let human judgment lead when quality is subjective, such as writing tone, design, strategy, or usefulness.

Explain why important questions matter. For example: “Should the result be a chat response, a structured report, a file, or an action in another system? That changes both the instructions and how we verify completion.”

When a task involves private communications, records, or information about people, proceed only for a legitimate purpose and with clear authorization. Use the minimum relevant sources and details, exclude unrelated sensitive information, respect consent and access expectations, and keep all outputs within the appropriate access boundary.

## 1. Identify the starting point

Classify the request before choosing a workflow.

### New skill

The user has an idea for recurring work. Start with discovery, scope, and a first draft.

### Existing skill

The user has a skill that needs editing, simplification, testing, or improvement. Read its current instructions before proposing changes. Preserve the established name and identity unless the user explicitly requests a rename.

### Workflow demonstrated in conversation

The user may say, “Turn what we just did into a skill.” Extract what the conversation already establishes:

- Inputs and source material.
- Tools or capabilities used.
- The sequence of decisions and actions.
- Corrections and preferences supplied by the user.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow, identify missing decisions, and ask the user to confirm it. Do not turn a one-time workaround into a general rule without checking that it will apply in future cases.

### Evaluation-focused request

The user may already have a finished-looking skill and want to know whether it helps. Start with test design and comparison. Do not rewrite a skill merely because it can be rewritten.

## 2. Capture intent and scope

Gather enough information to define a coherent, reusable job. Do not ask every question mechanically; prioritize the unknowns that would most change the design.

Use these questions as needed:

1. **Purpose:** What should the AI accomplish?
2. **Activation:** What user requests, wording, or situations should use this skill?
3. **Inputs:** What information, files, systems, references, and permissions may it use?
4. **Outputs:** What should it produce, change, or communicate? Is there a required format?
5. **Success:** How will the user decide that the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask a question, pause, decline, or return work to the user?
7. **Variations:** What common cases, difficult cases, or exceptions matter?
8. **Dependencies:** Does it need user-provided access, a specialized capability, templates, reference material, or deterministic helper scripts?
9. **Testing:** Should the skill be tested with realistic examples before it is adopted?

Offer choices when useful:

- “When a required detail is missing, should the skill make a clearly labeled best-effort assumption or stop and ask?”
- “Should the default result be concise, detailed, or chosen by the user?”
- “May the skill use any available source, or only sources the user has explicitly approved?”
- “Should it prepare a draft only, or may it perform an external action after confirmation?”

Recommend testing when work is repeated, consequential, objectively checkable, file-producing, or likely to vary with input quality. For highly subjective creative work, lightweight human review may be more valuable than forced numerical metrics.

## 3. Research and authorization checks

If relevant resources are available, review approved documentation, existing skills, user-provided examples, format requirements, and applicable standards before drafting. Research should reduce the user’s effort, not replace their authority over requirements.

Use it to identify:

- Existing conventions and output standards.
- Constraints imposed by an available tool, API, file type, or environment.
- Reusable patterns from comparable work.
- Safety, legal, privacy, compliance, and approval requirements.

If research requires access to internal records, personal data, or private communications, confirm that the task has a legitimate purpose and the user is authorized to request it. Use only the minimum necessary sources. Do not expose unrelated personal details in drafts, test data, screenshots, logs, or packaged resources.

When sources conflict or a requirement cannot be verified, report the uncertainty rather than presenting a guess as fact.

## 4. Choose a skill structure

Keep each skill focused enough that users and the AI can predict what it does. A skill may support related variants, but separate unrelated jobs when they differ in audience, permissions, sources of truth, or definition of completion.

A portable package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed documentation
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test prompts and grading material
```

Use progressive disclosure:

1. **Metadata or description:** A short statement that helps the AI decide whether the skill applies.
2. **Core instructions:** The normal workflow, loaded whenever the skill is used.
3. **Supporting resources:** References, templates, and scripts consulted only when relevant.

Keep the core instructions readable. If they become too large, move detailed variants into clearly named reference files and say exactly when to read them. Give large reference files a table of contents or other clear navigation.

For a skill with multiple variants, use a shared selection workflow and separate references by variant. The AI should load the relevant material rather than treating every variant as mandatory context.

### When to bundle scripts

Bundle a script when repeated runs show that the AI repeatedly reconstructs the same deterministic procedure, such as conversion, validation, calculation, report generation, or data cleanup. A bundled script should be:

- Reusable across requests.
- Easier to verify than a fresh natural-language procedure.
- Clearly documented with inputs, outputs, and limits.
- Safe and within the user’s authorized scope.

Do not automate an action just because it is possible. Scripts must not conceal behavior, bypass authorization, alter systems unexpectedly, or create security risks.

## 5. Write the skill

Draft in clear, imperative language. Explain the reason for important instructions, especially where a rule prevents a likely failure. A capable AI usually performs better when it understands the desired outcome and tradeoff than when it receives a long list of unexplained prohibitions.

Use the following sections where applicable.

### Purpose and scope

State what the skill does, its intended context, and its boundaries. Clarify whether it creates an answer, produces a file, guides a process, or performs an action.

### Inputs and prerequisites

List required information, allowed sources, required capabilities, and optional inputs. State what happens when required information is unavailable.

Example:

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or prepare a clearly marked incomplete draft.
```

### Workflow

Give a normal sequence with decision points instead of attempting to enumerate every scenario.

A durable pattern is:

1. Inspect the request and available inputs.
2. Ask focused questions only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Perform the task using an appropriate method.
5. Check the result against requested format and success criteria.
6. Present the output, assumptions, evidence, and unresolved limits.

Use conditional instructions where needed:

```markdown
If the user provides an approved template, follow it.
If no template is provided, use the default structure below.
If an action could overwrite work, publish information externally, or create a material commitment, explain the impact and request confirmation first.
```

### Output format

Define a template when consistency matters:

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

Use flexible goals rather than a rigid shell when the task requires substantial adaptation to context.

### Quality, safety, and privacy checks

Specify checks needed before completion: required fields, accurate calculations, source support for significant claims, preservation of original data, clear uncertainty labels, and approval before high-impact action.

The skill must behave in ways a user would reasonably expect from its description. Do not create instructions that facilitate deception, unauthorized access, data exfiltration, security compromise, harmful automation, or covert collection of private information.

### Failure behavior

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or source:** State what could not be verified and offer a safe alternative.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, flag it, or request direction.
- **Permission-sensitive action:** Pause for confirmation before irreversible, external, or high-impact work.

### Examples

Include only a few generalized examples when each teaches a distinct pattern. Examples should demonstrate reasoning and format, not turn the skill into a narrow collection of memorized cases.

## 6. Write a strong activation description

The skill description is a routing instruction. It should say both what the skill does and when it should be used.

Cover realistic user language, including requests that imply the job without naming it. A useful pattern is:

```text
Create clear project status reports from approved updates and source material. Use for leadership summaries, progress reports, milestone reviews, risk updates, and requests to explain current work, next steps, or blockers, even when the user does not say “status report.”
```

A good description includes:

- The task or outcome.
- Common contexts or phrases that indicate the task.
- Important scope limits that prevent expensive or harmful false activation.

Do not put the entire procedure in the description. Avoid vague descriptions such as “help with documents,” but also avoid descriptions so broad that they capture nearby work better handled by another skill.

## 7. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description identify when to use it?
- Are inputs, permissions, and outputs clear?
- Does the workflow explain why important checks exist?
- Does it handle missing information and validation failure?
- Does it rely on undeclared personal conventions, private access, or a particular tool?
- Are there redundant, brittle, or overly restrictive instructions?
- Does it give a capable AI enough freedom to handle ordinary variation?

Prefer lean instructions that affect behavior. Repeated absolute language is a warning sign unless it protects a real safety, privacy, authorization, or correctness boundary.

## 8. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user and invite changes before relying on them.

For each test case, record:

- A descriptive identifier.
- The prompt.
- Input files or context.
- The expected result in plain language.
- Objective checks, if suitable.

A portable structure is:

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

Cover meaningful variation:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or rule-sensitive case.
- A realistic edge case that changes the workflow.
- A request that should require approval, a privacy boundary, or a safe refusal, if relevant.

Do not merely restate the skill’s instructions in test prompts. Vary phrasing, detail level, and the user’s apparent familiarity. Use synthetic or authorized material for tests; never embed private records, credentials, or unnecessary personal data.

## 9. Run tests and comparisons

When independent execution is available, compare the skill against a meaningful baseline.

- **New skill:** Run each prompt with the skill and without the skill.
- **Existing skill:** Save an unchanged copy before editing, then compare the revised version with the earlier version.

Start both conditions under comparable circumstances. When parallel execution is available, start all skill and baseline runs together. Save the prompt, inputs, outputs, and available metadata such as elapsed time and resource usage. Record timing as soon as the environment reports it, since some systems do not retain it.

Use a clear iteration layout:

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

If independent or parallel runs are unavailable, perform a transparent sanity check: follow the skill for each prompt, save outputs, and ask the user to inspect them. Do not describe this as a rigorous baseline comparison.

## 10. Define and grade objective checks

While runs are in progress, draft objective checks where they genuinely help. Explain them to the user before using them as success criteria.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A produced file opens and contains the required fields.
- Calculations match an agreed source within a defined tolerance.
- The response identifies missing mandatory inputs.
- Significant claims include required source references.

Record each check with a descriptive statement, pass/fail value, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when required source information is missing.",
      "passed": true,
      "evidence": "The final section lists unavailable data and requests the missing source."
    }
  ]
}
```

Use programmatic checks when practical. They are more repeatable than visual inspection and can be reused in later iterations. Do not force numerical checks onto subjective work such as tone, aesthetics, or strategic judgment; human review is more appropriate there.

## 11. Review and analyze results

Present outputs and measurements in an accessible review format. If a review interface is available, use it to show each prompt, output, comparison condition, grades, and feedback field. Otherwise provide accessible files or a clear conversation-based review.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, difficult to use, or unnecessarily time-consuming?
- Did the skill introduce steps that did not add value?
- Would this work for similar requests with different wording or data?

Analyze more than the average pass rate. Look for:

- Checks that pass regardless of condition and do not distinguish useful performance.
- High variation that suggests ambiguity or unreliable instructions.
- Quality gains that cost too much time or compute.
- Repeated failures with the same root cause.
- Repeated planning, research, or formatting that does not improve outcomes.
- Helper procedures repeatedly recreated across runs, suggesting a script or template should be bundled.

Small evaluations are evidence, not proof. Use them to guide the next revision.

## 12. Improve without overfitting

Base revisions on feedback, outputs, and analysis. Change the smallest part likely to address the underlying cause.

Generalize from complaints. If one test omitted a source note, do not add a rule mentioning that exact prompt. Instead clarify the broader condition: when evidence is incomplete or mixed, distinguish verified information from assumptions and identify the missing source.

Use these principles:

1. Fix causes, not individual examples.
2. Remove instructions that do not improve behavior or create wasted work.
3. Explain the reason behind important actions.
4. Add reusable scripts, templates, and references only when evidence justifies them.
5. Preserve behavior the user already values.
6. Add tests only for genuine classes of failure.

After revision, rerun the test set in a new iteration and apply the same comparison policy. Show prior and current results when possible. Stop when the user is satisfied, feedback is consistently positive, objective requirements are reliably met, further revisions no longer help, or remaining issues require unavailable information or a product decision.

## 13. Optional blind comparison

For a more rigorous comparison between two versions, give an independent evaluator two outputs without identifying their origins. Ask it to judge against a shared rubric, record the judgment, then reveal which output came from which version.

Use blind comparison when versions have similar numerical results, qualitative quality matters, or the decision has meaningful cost. Evaluate correctness, completeness, clarity, adherence to constraints, safety, and practical usefulness. Analyze why one output was preferred before changing the skill again.

## 14. Optimize triggering behavior

Only optimize the description after the skill’s workflow is stable. Create a realistic set of requests that should activate the skill and nearby requests that should not.

Include roughly balanced coverage. Positive cases should vary in formality, wording, directness, and context. Negative cases should be difficult near-misses, not irrelevant requests. They should share concepts with the skill but require another workflow or lack conditions that make this skill useful.

```json
[
  {
    "query": "I need a concise leadership update from these project notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain when teams usually use progress reports?",
    "should_trigger": false
  }
]
```

Review the set with the user. If repeated activation tests are supported, separate examples used to improve the description from held-out examples used to select the final version. Choose the description that performs best on held-out cases rather than the one that best fits the editing examples.

Remember that simple one-step tasks may not activate a specialized skill even if the description matches, because the AI may complete them directly. Use substantive trigger tests where consulting the skill would add real value.

## 15. Package and hand off

Package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on private habits, undeclared tools, or unavailable access.
- References and scripts are included, clearly named, and documented.
- No confidential data, credentials, identifiers, private records, or sensitive examples remain.
- The user can install, access, or adapt the skill in their chosen environment.
- Test material is retained only when it is safe and useful.

Provide a short handoff note explaining what the skill does, required capabilities, known limitations, and how to test it after installation.

## Final readiness gate

A skill is ready when it has a clear and bounded job, an accurate activation description, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for the user’s recurring work.

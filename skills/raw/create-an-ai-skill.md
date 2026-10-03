---
name: create-an-ai-skill
description: Design, test, improve, evaluate, and package a reusable AI skill from a new idea, an existing draft, or a demonstrated workflow. Use this workflow to create skills that are clear, safe, adaptable, and supported by realistic evidence.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, improve an existing skill, evaluate whether a skill helps, or capture a repeated workflow from a conversation. A skill is a focused instruction package, with optional resources, that helps an AI carry out a recurring kind of work consistently.

The normal improvement loop is:

1. Understand the intended job, users, boundaries, and success criteria.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Review outputs with a person and measure objective requirements where useful.
5. Improve the skill based on evidence.
6. Repeat until it is useful, reliable, and not narrowly fitted to the test examples.
7. Optionally improve its description so it activates for the right requests.

Adapt the process to the user's goal. Some users want a quick collaborative draft rather than a formal evaluation. Others need a rigorous comparison before deployment. Identify the current stage and help the user take the next useful step rather than forcing every project through every phase.

## Communication principles

Use plain language by default and adapt to the user's technical experience. Terms such as *evaluation* and *benchmark* are often acceptable, but briefly define them when needed. Do not use terms such as *JSON*, *assertion*, *schema*, or *baseline* without explanation unless the user shows comfort with them.

Explain why important questions matter. For example:

> What should a successful result look like: a chat response, a report, a file, or an approved action? This determines what the skill needs to produce and how we can test it.

Keep the user involved in material decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before choosing restrictive scope, required tools, or approval rules.
- Share proposed test prompts before treating them as representative.
- Let human review lead when quality is subjective, such as writing style, design, strategic judgment, or usefulness.
- State uncertainty honestly instead of implying that a small test set proves broad reliability.

## 1. Identify the starting point

Determine which of these situations applies.

### New skill

The user has an idea for recurring work, such as preparing project updates, validating data files, or producing a structured analysis. Start with discovery, scope definition, and a first draft.

### Existing skill

The user has a draft, installed package, or set of instructions that needs editing, testing, simplification, or improvement. Read the existing material before proposing changes. Preserve the established name and identity unless the user asks to change them.

If the installed copy is read-only, work from a writable copy. Retain the original unchanged so it can serve as a comparison point and recovery option.

### Workflow demonstrated in the conversation

The user may ask to turn recent work into a skill. Extract as much as possible from the conversation before asking questions:

- Inputs, constraints, and source materials.
- The sequence of decisions and actions.
- Tools or capabilities that were needed.
- Corrections and preferences the user expressed.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow and identify gaps for confirmation. Do not silently convert a one-time workaround into a general rule.

### Evaluation or optimization request

The user may already have a finished-looking skill and want to know whether it improves outcomes or activates at appropriate times. Begin with test design and evaluation. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent, scope, and authorization

Gather enough information to define a coherent job. Ask the most consequential unanswered questions first rather than using a rigid questionnaire.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** Which kinds of requests, wording, or situations should use it?
3. **Inputs:** What information, files, systems, references, and capabilities may it use?
4. **Outputs:** What should it produce, change, or recommend? Is there a required format?
5. **Success:** How will the user recognize a correct, useful result?
6. **Boundaries:** What should it not do? When should it ask a question, pause, decline, or return control to the user?
7. **Variation:** What common cases, difficult cases, and meaningful exceptions should it handle?
8. **Dependencies:** Does it need templates, reference documents, scripts, external services, or specific permissions?
9. **Testing:** Should it be tested with realistic examples? Recommend testing for repeat use, consequential tasks, objective outputs, or work that changes files or systems.

Useful choice questions include:

- Should the skill make a low-risk best-effort assumption, or stop and ask when information is missing?
- Should it produce a concise answer, a detailed report, or let the user choose?
- Which sources are approved, and which sources are out of scope?
- What actions require explicit confirmation before execution?

### Privacy, legitimate purpose, and access boundaries

If the skill reads communications, records, files, or information about people, establish a legitimate purpose and clear authorization before using those materials. Use only the minimum relevant sources and data needed for the task.

Design the skill to:

- Respect consent, confidentiality, legal obligations, and ordinary privacy expectations.
- Omit unrelated personal details from outputs.
- Avoid copying sensitive details merely because they were available.
- Keep findings within the user's appropriate access boundary.
- Ask for clarification when authorization, ownership, or permitted use is unclear.
- Distinguish evidence about role-relevant work from speculation about a person.

For hiring, assessment, or selection work, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether the assessment distinguishes relevant performance. Do not infer sensitive traits, make unsupported judgments about people, or use language that treats people as objects or categories to be filtered.

### Research before drafting

If user-approved documentation, similar skills, policies, domain guidance, or references are available, review them before drafting. Research should reduce burden on the user, not replace their authority over requirements.

Use research to identify:

- Existing standards and output conventions.
- Tool, file-format, or system constraints.
- Reusable patterns from comparable work.
- Safety, compliance, consent, or approval requirements.

If sources conflict or a requirement remains uncertain, surface the uncertainty and offer options rather than guessing.

## 3. Choose a maintainable structure

Keep the skill focused enough that both users and AI systems can predict what it does. A single skill may support closely related variants, but separate unrelated jobs when they have different audiences, permissions, inputs, or definitions of completion.

A typical package may contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed guidance
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test prompts and grading material
```

Use progressive disclosure:

1. **Metadata:** A short name and description used to decide whether the skill applies.
2. **Core instructions:** The workflow needed for ordinary requests.
3. **Supporting resources:** Detailed references, templates, or scripts loaded only when relevant.

Keep core instructions readable. When the main file becomes unwieldy, move specialized material to clearly named references and say exactly when to consult each one. Give long references a navigation section or table of contents.

When the skill supports variants, organize guidance by variant and instruct the AI to select only the applicable reference. For example, a deployment skill can have a shared planning workflow and separate references for different deployment environments.

### Bundle repeatable work only when it earns its place

When test runs repeatedly reconstruct the same helper process, consider a reusable script, template, or reference. This is especially valuable for validation, conversion, structured report generation, or other deterministic work.

Bundle a resource when it is:

- Reused across requests.
- Easier to verify than natural-language reconstruction.
- Less error-prone or safer than repeated manual work.
- Within the user's intended permission scope.

Document what it does, expected inputs and outputs, limitations, and when not to use it. Do not add automation merely because it is technically possible.

## 4. Draft the skill

Write instructions in clear, direct language. Prefer explaining the purpose of important checks over piling up unexplained prohibitions. A capable AI can adapt better when it understands the quality, safety, or usability reason behind a step.

A useful skill commonly contains the following sections.

### Purpose and scope

State the job, intended user, normal outcome, and boundary. Clarify whether the skill creates an answer, generates a file, changes a system, or guides a human through a decision.

### Inputs and prerequisites

List required information, approved sources, needed capabilities, and optional inputs. Say what to do when a necessary item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or produce a draft clearly marked as incomplete.
```

### Workflow and decision points

Describe the normal sequence without trying to enumerate every imaginable situation:

1. Inspect the request and available inputs.
2. Clarify only when the answer materially changes the work.
3. Gather evidence from approved, relevant sources.
4. Complete the task using the appropriate method.
5. Check the result against requested format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limits.

Use conditional instructions for genuine forks in the work:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If an action could overwrite work, publish externally, or create a material commitment, explain the impact and request confirmation first.
```

### Output format

Use an exact template when consistency is important:

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

Do not impose rigid formatting when the value depends on adapting to context. In those cases, provide quality goals and a short example instead.

### Quality, safety, and failure behavior

Include checks that matter before completion: required fields, calculation validation, source attribution, preservation of original data, privacy review, or uncertainty labels.

Specify recovery behavior in general terms:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** State what could not be verified and offer an approved alternative.
- **Ambiguous request:** Make a low-risk assumption only when it does not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, report the issue, or request direction.
- **High-impact action:** Pause for confirmation before irreversible, external, permission-sensitive, or costly work.

Skills must behave as users would reasonably expect from their description. Do not create hidden behavior, misleading automation, unauthorized data access, data extraction beyond the approved scope, security bypasses, or destructive actions.

### Examples

Include only a few generalized examples, and only when they teach a distinct pattern. Examples should illustrate reasoning and output shape, not become brittle rules that merely reproduce a test case.

## 5. Write a description that activates appropriately

The description is a routing aid. It should say both **what the skill does** and **when it should be used**. Cover realistic user language, including requests that imply the task rather than naming it.

A strong description includes:

- The outcome or task.
- Common contexts and phrases indicating relevance.
- Important scope limits when they prevent costly false activation.

Example pattern:

```text
Create project status reports from approved updates and source material. Use for requests involving progress summaries, leadership updates, milestone reviews, risks, blockers, or next steps, even when the user does not say “status report.”
```

Avoid vague descriptions such as “help with documents.” Do not make the description so broad that it claims nearby work better handled by another skill. Keep it honest about authority, required inputs, and boundaries.

## 6. Review before testing

Read the draft from the perspective of an AI encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description explain when to activate the skill?
- Are required inputs, approved sources, permissions, and outputs clear?
- Does the workflow explain why important checks exist?
- Does it cover missing information and validation failures?
- Are there unnecessary rules, duplicated guidance, or brittle wording?
- Does it rely on personal habits, hidden access, or undeclared tools?
- Does it respect privacy and avoid unrelated sensitive data?
- Does it leave enough room for normal variation and sound judgment?

Prefer lean instructions over a long list of rules that do not affect outcomes. Repeated emphatic wording is a warning sign unless a behavior is truly non-negotiable, such as an authorization or safety boundary.

## 7. Design realistic tests

After the draft is stable enough to test, create two or three realistic test prompts. Show them to the user before relying on them. Record a descriptive identifier, prompt, supplied files or context, expected outcome, and objective checks if appropriate.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates and flag information that cannot be verified.",
      "expected_output": "A structured summary separating verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Include meaningful variation:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic edge case that changes the workflow.
- A request that should require approval, preserve privacy, or decline unsafe work, when relevant.

Do not test only the wording used in the instructions. Vary phrasing, detail level, and context. Avoid retaining personal or confidential scenarios in test materials; use safe, generalized equivalents.

## 8. Run comparable evaluations

Where independent execution is available, compare the skill to a meaningful baseline.

- **New skill:** Run each test with the skill and without it.
- **Existing skill:** Save an unchanged snapshot before editing and compare the revision with that version, unless a previous iteration is the more useful comparison.

Start comparable runs under the same conditions. When parallel work is available, launch all skill and comparison runs together so timing and environment differences do not distort results.

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

For each run, preserve the prompt, relevant inputs, outputs, and available execution metadata such as duration and resource use. Record timing when it is reported, because some environments do not keep it afterward.

If independent runs are unavailable, perform a transparent sanity check: follow the skill on each prompt, save the results, and ask the user to review them. Do not represent this as a rigorous causal comparison.

## 9. Define and grade objective checks

While test runs are in progress, draft objective checks where they genuinely measure value. Explain the checks to the user before treating them as success criteria.

Good checks are observable and meaningful:

- Required sections are present.
- A produced file opens and contains required fields.
- Calculations match known values within an agreed tolerance.
- Missing mandatory inputs are identified.
- Required citations, source notes, approval statements, or privacy exclusions are present.

Use a stable grading record:

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

Use scripts for programmatic checks when practical. They are generally more repeatable than visual judgment and can be reused in future iterations.

Do not force numerical metrics onto subjective work. Tone, creativity, usefulness, visual quality, and strategic judgment often require human review. Weak proxy metrics can cause a skill to optimize for the metric rather than the user's actual goal.

## 10. Review outputs with a human

Present qualitative outputs and quantitative evidence together. Use an available review interface when possible; otherwise present results clearly in conversation or as accessible files.

For each test, show:

- The original prompt and relevant inputs.
- The skill output and comparison output, if available.
- Objective grades and supporting evidence.
- Timing or resource information, if available.
- A clear way for the reviewer to leave feedback.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add work or detail without adding value?
- Would this work for similar requests with different wording or data?

Empty feedback can mean a case is acceptable, but it does not prove the skill is complete. Review outputs and measurements as well.

## 11. Analyze results and revise without overfitting

Aggregate results where possible: pass rate, time, resource use, variation, and per-test outcomes. Put the revised skill before its comparison condition in reports for readability.

Then inspect patterns that aggregate statistics may hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill's value.
- **High variation:** Similar runs differ substantially, suggesting ambiguous instructions or environmental instability.
- **Tradeoffs:** Quality improves, but time or resource use becomes excessive.
- **Failure concentration:** Several problems share one cause, such as unclear source selection or output requirements.
- **Unproductive work:** Execution spends effort on redundant planning, research, or formatting.
- **Repeated reconstruction:** Many runs independently create the same helper process, indicating a reusable resource may help.

Revise the smallest part of the skill likely to address the underlying cause. Generalize from complaints instead of patching an exact test example. Explain the reason for important changes. Preserve behavior that users already value, remove instructions that do not help, and add a new test only when it represents a real recurring class of failure.

After revision, rerun the full test set in a new iteration and compare it under the same policy. Stop when the user is satisfied, feedback is consistently positive across meaningful cases, objective requirements are reliably met, or further edits no longer make meaningful progress.

## 12. Optional blind comparison and trigger optimization

For a consequential choice between two versions, use blind review. Give an independent evaluator outputs without identifying their origin, apply a shared rubric, and reveal the mapping only after the judgment is recorded. Evaluate correctness, completeness, clarity, constraint adherence, safety, and practical usefulness.

Once the workflow is stable, test whether the description triggers appropriately. Create a balanced set of realistic requests that should activate the skill and difficult near-misses that should not. Review the set with the user. Use substantive requests: simple one-step tasks may not invoke a specialized skill even when the description matches.

Test candidate descriptions repeatedly if possible. Separate examples used to revise the description from held-out examples used to select it. Choose based on held-out performance to reduce overfitting, then show the user the before-and-after description and results.

## 13. Package and hand off

Package the core instructions and only resources needed for ordinary use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on hidden local conventions or undeclared access.
- Scripts and references are present, clearly named, and documented.
- No credentials, identifiers, private records, confidential examples, or unnecessary personal details remain.
- Required permissions and capabilities are stated.
- The user can install or adapt it in their chosen environment.
- Retained test material is safe and useful.

Provide a handoff note explaining the skill's purpose, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an accurate trigger description, instructions that handle normal variation, explicit privacy and permission boundaries, useful failure behavior, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and produce better results for real recurring work.

---
name: create-a-skill
description: Designs, tests, and improves a reusable AI skill from a rough idea or repeated workflow. Use when someone says "turn this into a skill," "improve this skill," or "does my skill help?"
---

# Create an AI skill

Use this workflow to create a new AI skill, improve an existing one, test whether a skill actually helps, or tune when it activates. A skill is a focused set of instructions, plus optional scripts, reference documents, and templates, that helps an AI do a recurring job well and consistently.

## Quick version

- Tell your assistant what the skill should do, when it should be used, and what a good output looks like. If you already did the job in a conversation, paste it and ask the assistant to extract the steps, corrections, and formats, then confirm the gaps.
- Before drafting, have it ask only questions that change the design: missing information, edge cases, actions that need your confirmation, and what would make you reject an output.
- Draft the skill: a short name, a slightly assertive description that leads with trigger phrases, imperative instructions that explain why each step matters, an output template, and what to do when something is missing or unclear.
- Write two or three realistic test requests. Paste the skill into a fresh chat with each one and read the outputs yourself before changing anything.
- Revise from the general cause of each problem, not the specific example. Fold each lesson into the rule it refines instead of appending notes about what went wrong.
- Repeat until you are happy or progress stops, then run the audit checklist in section 10.

The method works with any AI system that supports reusable instructions. Where this guide mentions files, folders, or tools, substitute whatever your platform provides.

## 1. Work out where the user is

The core loop:

1. Understand what the skill should do and roughly how.
2. Write or revise a draft.
3. Run the AI, with the skill available, on a few realistic test requests.
4. Help the user judge the results by reading outputs and, where useful, by measuring objective checks.
5. Revise the skill from that evidence.
6. Repeat until the user is satisfied or progress stops.
7. If the skill matters enough, expand the test set and try again at larger scale.
8. Optionally tune the description so the skill activates for the right requests.
9. Package and hand off the skill.

Your first job is to find the user's place in this loop and help them take the next step. Stay flexible about order and depth: someone who says "skip the formal evaluation, just work on it with me" should get that.

| Situation | What to do first |
|---|---|
| New idea ("a skill for X") | Capture intent, interview, draft |
| Existing draft or installed skill | Read it fully, then go to testing and revision. Keep its name unless the user asks to rename it |
| Workflow already shown in the conversation ("turn this into a skill") | Extract the workflow from the conversation, then confirm gaps |
| "Does this skill actually help?" | Go straight to test design and evaluation. Do not rewrite just because you can |

When extracting from a conversation, pull out the tools and sources used, the sequence of steps, corrections the user made, input and output formats, and conditions that changed the approach. Summarize this, ask the user to fill gaps, and get confirmation before moving on. Do not quietly turn a one-time workaround into a general rule.

If you have a task list, add the loop steps to it, including "show test outputs to the user before revising". That step is the one most often skipped.

## 2. Communicate at the right level

Users range from experienced developers to people who have never used a command line. Read context cues and adjust.

- Words like "evaluation" and "benchmark" are usually fine.
- Words like "JSON", "assertion", "baseline", and "schema" need clear signs that the user knows them. Otherwise add a short definition the first time.
- When in doubt, explain briefly. It costs little.

Keep the user involved at decision points: confirm scope before writing a lot, share test prompts before relying on them, and let human judgment settle subjective questions such as tone, design, and usefulness.

## 3. Capture intent

Make sure you can answer these questions:

1. What should the skill enable the AI to do?
2. When should it activate? Which user phrases or situations?
3. What is the expected output: a chat reply, a file, a change to a file, an external action?
4. Should we build test cases to check that it works?

For question 4, suggest a default based on the skill type and let the user decide. Skills with objectively checkable outputs (file conversions, data extraction, code generation, fixed workflow steps) benefit from test cases with checks. Skills with subjective outputs (writing style, visual design) usually need human review more than numerical checks.

## 4. Interview and research

Ask about edge cases, input and output formats, example files, success criteria, permissions, and dependencies. Hold off on writing test prompts until these are settled. Useful question formats:

- "If information is missing, should the skill ask, make a labeled assumption, or produce a draft marked incomplete?"
- "Should it work with any source you give it, or only specific approved sources?"
- "Does any action need your confirmation because it is external, irreversible, or high impact?"
- "What would make you reject an output?"
- "Who will use this skill, and what can they already be assumed to know?"

If you can search documentation or look up similar skills and good practices, do that before asking the user things you could find yourself. If sources conflict or requirements stay unclear, say so instead of inventing a rule.

## 5. Choose the structure

A typical skill package looks like this. Use your platform's naming conventions:

```text
skill-name/
├── [main instruction file]   # required: name, description, instructions
├── scripts/                  # optional: code for deterministic or repetitive tasks
├── references/               # optional: documents loaded only when needed
└── assets/                   # optional: files used in outputs (templates, icons, fonts)
```

Most skill systems load content in layers, so design for progressive disclosure:

| Layer | Content | When loaded | Size guide |
|---|---|---|---|
| 1. Metadata | Name and description | Always visible to the AI | A sentence or two |
| 2. Main instructions | The body of the skill | Whenever the skill activates | Short enough to read in one pass; a few hundred lines at most |
| 3. Bundled resources | Scripts, references, assets | Only when needed | Can be large; scripts can run without being read |

Follow any limits your platform sets. If it sets none, choose a size limit for the main file yourself (adjustable) and check against it whenever you edit. Key patterns:

- If the main instructions grow long, move detail into reference files and say exactly when to read each one.
- Give long reference files a table of contents.
- When a skill supports several variants (for example, deploying to different hosting providers), keep the shared workflow and variant selection in the main file and put each variant in its own reference file.
- Split unrelated jobs into separate skills when they have different audiences, permissions, sources of truth, or definitions of done.

## 6. Write the skill

### Required parts

- **Name:** a short, stable identifier.
- **Description:** what the skill does and when to use it. This usually decides whether the AI uses the skill, so put all "when to use" information here, not in the body.
- **Compatibility (optional):** required tools or dependencies, only if they are not obvious.
- **Instructions:** the body.

### Writing the description

AI systems often under-use skills. Counter this by making descriptions slightly assertive. Instead of "How to build a quick inventory dashboard", write "How to build a quick inventory dashboard. Use this whenever the user mentions dashboards, stock-level charts, operational metrics, or wants to see warehouse data visually, even if they don't say 'dashboard'."

- Keep it short. Respect your platform's length limit; if there is none, one or two sentences is a good default.
- Lead with the phrases and situations that should trigger it, including cases where the user implies the job without naming it.
- Add scope limits only where false activation would be costly.
- Do not put the workflow itself in the description.

If the platform offers different ways to reach a skill, such as automatic activation, grouping under a routing skill, or manual invocation by name, ask which fits. A sensible default is automatic for general workflows and manual for command-style skills. If many skills share one area, grouping keeps the always-visible list manageable. After adding, renaming, or removing a skill, run whatever registration or validation step the platform provides.

### Safety: no surprises

A skill must not contain malware, exploit code, or anything that compromises security. Its contents should not surprise the user given its description. Decline to build misleading skills or skills meant for unauthorized access, data extraction, or other harm. Ordinary creative uses, such as a role-play persona, are fine.

### Writing style

- Use the imperative form.
- Explain why things matter instead of stacking unexplained commands. If you find yourself writing ALWAYS or NEVER in capitals, treat it as a warning sign and explain the reason instead. Keep firm rules for authorization, privacy, safety, data integrity, and irreversible actions.
- Write for general use, not for the specific examples you have in mind.
- Write a draft, then reread it with fresh eyes and improve it.

### Useful patterns

Define output formats when consistency matters:

```markdown
## Report structure
Use this template:
# [Title]
## Executive summary
## Key findings
## Recommendations
```

Include examples when they teach something:

```markdown
## Commit message format
Example:
Input: Fixed rounding error in invoice totals
Output: fix(billing): correct invoice total rounding
```

Also cover, as needed: required inputs and what to do if they are missing; the normal workflow and its branches; checks to run before finishing; and failure behavior for unavailable tools, ambiguous requests, failed validation, and high-impact actions that need confirmation.

## 7. Write test cases

After the draft, write two or three realistic test prompts, the kind of thing a real user would type. Share them, for example: "Here are three requests I plan to test with. Do they look like what you'd really ask, or should we add one?"

Cover meaningful variety: a typical request, an incomplete or ambiguous one, a format-sensitive one, and, if relevant, one that should lead to a confirmation or refusal. Give each test a descriptive name. Leave checks empty for now; draft them while runs are in progress.

```json
{
  "skill_name": "[skill name]",
  "tests": [
    {
      "id": "[descriptive-test-name]",
      "prompt": "[the user's task prompt]",
      "expected_output": "[description of expected result]",
      "files": [],
      "checks": []
    }
  ]
}
```

## 8. Run and review the tests

Treat this as one continuous sequence. Do not stop partway.

1. **Run each test** with the skill available. In a plain chat, paste the skill and one test prompt into a fresh conversation, or follow the skill yourself. Call this a sanity check, not a rigorous comparison, since the author is also the runner. If you can run independent helpers with baselines, see Optional extras.
2. **Draft checks while you wait.** Good checks are objectively verifiable and have descriptive names that make sense at a glance: required sections are present; the produced file opens; totals match the source; missing inputs are flagged. Do not force checks onto subjective qualities; those need human review. If checks already exist, explain what they verify and adjust if needed.
3. **Grade each output** against its checks. For checks a script can verify, write and run a script; it is faster, more reliable, and reusable. Record the check text, pass or fail, and evidence.
4. **Present results to the user before you start fixing things yourself.** For each test, show the prompt and output, save any file the user must inspect and say where it is, and ask: "How does this look? Anything you'd change?"
5. **Read the feedback.** Empty feedback usually means the output was fine, though it is not proof the skill is complete. Focus on tests with specific complaints.

## 9. Improve the skill

This is the heart of the loop. Take your time. Draft a revision, then reread it fresh and improve it.

1. **Generalize from feedback.** The skill will be used many times on many different requests. You iterate on a few examples only because it is fast; a skill that works only for those is useless. Avoid narrow, overfitted fixes and oppressive rules. If a problem persists, try a different framing, metaphor, or working pattern.
2. **Keep it lean.** Remove what is not earning its place. Read the run transcripts, not just final outputs. If the skill makes the AI waste effort, remove the cause and see what happens.
3. **Explain the why.** Even if feedback is terse or frustrated, work out what the user actually needs and put that understanding into the instructions.
4. **Bundle repeated work.** If several runs independently wrote similar helper scripts or followed the same multi-step routine, write it once, add it to the skill, and tell the skill to use it.
5. **Fold lessons into existing rules.** When a run teaches a lesson, edit or merge the rule it refines instead of adding a new paragraph about the incident. Do not append dated incident notes to the skill. If you want an audit trail, keep it in a separate change log that the skill does not load when it runs.
6. **Preserve what works.** Do not break behavior the user already liked while fixing something else.

Then rerun all tests as a new iteration, show the new results with previous outputs and feedback alongside, wait for the user to finish reviewing, and repeat. Stop when the user is happy, feedback is consistently empty across meaningful tests, or you are no longer making meaningful progress.

## 10. Package and hand off

If a packaging tool is available, package the skill in the user's chosen format and say where the result is. Include only resources needed for normal use. When updating an installed skill, keep the original name and folder name; do not create a "v2" copy unless the user asks.

Pre-delivery audit:

- [ ] Name is stable and appropriate.
- [ ] Description states what the skill does and when to use it, within the platform's limits.
- [ ] Main file is within the size limit, and any validation step passes.
- [ ] Lessons are merged into rules, with no appended incident notes.
- [ ] Instructions do not depend on undeclared tools, private conventions, or personal access.
- [ ] Every bundled resource is referenced, clearly named, and explained.
- [ ] No credentials, private identifiers, confidential records, or sensitive examples are included.
- [ ] Any retained tests are safe to distribute.
- [ ] If the skill will be shared in a collection, the decision to include or exclude it is recorded, it has passed privacy and quality review, and any public identifier stays stable (keep old identifiers as aliases if renamed).

Give a short handoff note: what the skill does, required capabilities, known limits, and a quick way to test it.

**Readiness gate:** a skill is ready when it has a clear job, a description that routes the right requests to it, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic tests that it improves outcomes. A long file is not the same as a reliable skill.

## 11. Avoid common failure modes

| Failure | Fix |
|---|---|
| Revising before the user has seen any outputs | Present results for human review first |
| Fixes tailored to the test examples | Find the general cause and fix that |
| Incident notes piling up at the end of the skill | Merge each lesson into the rule it refines; keep history in a separate log |
| Many capitalized absolute rules | Replace with explained reasoning, except for true hard boundaries |
| Vague or timid description, so the skill is rarely used | Lead with trigger phrases and name implied use cases |
| Checks that pass with or without the skill | Replace with checks that show the skill's added value |
| Calling a self-run sanity check a rigorous comparison | Label it honestly |
| Assuming one person's tools, limits, or conventions | Ask the user for their platform's rules and use those |

## Optional extras

### Parallel runs with baselines

If you can run independent helper agents, launch a with-skill run and a baseline run for every test in the same round, so they finish around the same time under similar conditions. For a new skill, the baseline is the same prompt with no skill. When improving a skill, snapshot it before editing and point the baseline at the snapshot. In later iterations, say whether the baseline is the original version or the previous iteration.

```text
[skill-name]-workspace/
├── skill-snapshot/
├── iteration-1/
│   ├── [test-name]/
│   │   ├── with-skill/
│   │   ├── baseline/
│   │   └── [test details, run data, grades]
│   └── [benchmark summary]
└── iteration-2/
```

Run instructions template:

```text
Execute this task:
- Skill location: [path to skill, or "none" for a no-skill baseline]
- Task: [test prompt]
- Input files: [files, or "none"]
- Save outputs to: [workspace]/iteration-[N]/[test-name]/[with-skill or baseline]/
- Outputs to save: [what the user cares about, e.g. "the final spreadsheet"]
```

If the environment reports time or resource use when a run finishes, save it immediately; some environments report it only once. Keep grade field names consistent so any review tool can read them:

```json
{
  "results": [
    {
      "text": "Flags missing source data in an assumptions section",
      "passed": true,
      "evidence": "Final section lists the two unavailable figures and asks for them."
    }
  ]
}
```

Aggregate into a benchmark: pass rate, time, and resource use per configuration, with average, spread, and the with-skill versus baseline difference, each with-skill result next to its baseline. Then analyze what totals hide: checks that pass either way, high variation that suggests flaky tests or unclear instructions, quality gains that cost too much time, and failures that share one root cause.

A good review view, using an existing tool rather than a custom build, has an Outputs view (prompt, rendered output, previous output, grades, feedback box, earlier feedback) and a Benchmark view (numbers with per-test breakdowns and notes). Without a display, write a standalone file the user can open.

### Blind comparison

When the user asks "is the new version actually better?" and wants rigor, give two outputs to an independent evaluator without saying which version produced which. Judge against a shared rubric: correctness, completeness, clarity, constraint adherence, and usability. Then analyze why the winner won. Human review is usually enough.

### Tune the description for activation

Do this after the skill works and the user agrees it is in good shape. Write about 20 queries, a roughly even mix of should-activate and should-not-activate:

```json
[
  {"query": "[realistic user prompt]", "should_trigger": true},
  {"query": "[near-miss prompt]", "should_trigger": false}
]
```

Make them realistic and detailed, with varied lengths, casual phrasing, and occasional typos.

- Weak: "Format this data", "Make a chart".
- Strong: "ok so my team lead dropped a csv in the shared drive (something like 'march orders cleaned v3') and wants a column with the discount as a percent of list price. list price is column B and paid amount is E i think".

Should-activate queries should vary phrasing, include requests that never name the skill but clearly need it, and include cases where this skill competes with another and should win. Should-not-activate queries should be near-misses that share keywords but need something different; obviously irrelevant negatives test nothing. AIs usually consult skills only for tasks they cannot easily do alone, so use substantive queries.

Have the user review and edit the set; bad queries produce bad descriptions. If automated activation testing exists, run it in the background with progress updates. A sound loop holds out about 40 percent of queries, runs each query several times, proposes improvements from failures, re-tests for a few rounds, and picks the winner by held-out score. Test with the model the user actually works with. Otherwise, walk through the set manually. Show the before and after and report the scores.

### Adapt to your environment

| Capability missing | Adaptation |
|---|---|
| Independent helper agents | Run tests yourself one at a time; skip baselines, benchmarks, and blind comparison |
| Automated activation testing | Review the query set manually against the description |
| Parallel runs keep failing or timing out | Run tests in sequence |
| Write access to the installed skill | Copy it to a writable location, edit there, and package from the copy |

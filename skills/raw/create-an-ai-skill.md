---
name: create-a-skill
description: Create, test, and improve reusable AI skills through realistic tests, human review, objective checks, and activation tuning, then package them for handoff.
---

# Create an AI skill

Use this workflow to create a new AI skill, improve an existing one, test whether a skill actually helps, or tune when it activates. A skill is a focused set of instructions, plus optional scripts, reference documents, and templates, that helps an AI do a recurring job well and consistently.

The method works with any AI system that supports reusable instructions. Where this guide mentions files, folders, or tools, substitute whatever your platform provides.

## The core loop

1. Understand what the skill should do and roughly how.
2. Write or revise a draft.
3. Run the AI, with the skill available, on a few realistic test requests.
4. Help the user judge the results by reading outputs and, where useful, by measuring objective checks.
5. Revise the skill from that evidence.
6. Repeat until the user is satisfied or progress stops.
7. If the skill matters enough, expand the test set and try again at larger scale.
8. Optionally tune the description so the skill activates for the right requests.
9. Package and hand off the skill.

Your first job is to work out where the user is in this loop and help them take the next step. Someone who says "I want a skill for X" needs discovery, a draft, tests, and review. Someone with an existing draft can go straight to testing and revision. Someone who says "skip the formal evaluation, just work on it with me" should get that. Stay flexible about order and depth.

If you have a task list, add the loop steps to it, including "show test outputs to the user before revising". That step is the one most often skipped.

## Communicating with the user

Users range from experienced developers to people who have never used a command line. Read context cues and adjust.

- Words like "evaluation" and "benchmark" are usually fine.
- Words like "JSON", "assertion", "baseline", and "schema" need clear signs that the user knows them. Otherwise add a short definition the first time.
- When in doubt, explain briefly. It costs little.

Ask questions whose answers change the design, not to fill out a form. Keep the user involved at decision points: confirm scope before writing a lot, share test prompts before relying on them, and let human judgment settle subjective questions such as tone, design, and usefulness.

If the skill will touch private communications, records, or information about people, confirm a legitimate purpose and clear authorization. Design the skill to use only the minimum relevant sources, leave out unrelated or sensitive personal details, respect consent and privacy expectations, and keep outputs within an appropriate access boundary.

## 1. Find the starting point

| Situation | What to do first |
|---|---|
| New idea ("a skill for X") | Capture intent, interview, draft |
| Existing draft or installed skill | Read it fully, then go to testing and revision. Keep its name unless the user asks to rename it |
| Workflow already shown in the conversation ("turn this into a skill") | Extract the workflow from the conversation, then confirm gaps |
| "Does this skill actually help?" | Go straight to test design and evaluation. Do not rewrite just because you can |

When extracting from a conversation, pull out the tools and sources used, the sequence of steps, corrections the user made, input and output formats, and conditions that changed the approach. Summarize this, ask the user to fill gaps, and get confirmation before moving on. Do not quietly turn a one-time workaround into a general rule.

## 2. Capture intent

Make sure you can answer these questions:

1. What should the skill enable the AI to do?
2. When should it activate? Which user phrases or situations?
3. What is the expected output: a chat reply, a file, a change to a file, an external action?
4. Should we build test cases to check that it works?

For question 4, suggest a default based on the skill type and let the user decide. Skills with objectively checkable outputs (file conversions, data extraction, code generation, fixed workflow steps) benefit from test cases with checks. Skills with subjective outputs (writing style, visual design) usually need human review more than numerical checks.

## 3. Interview and research

Ask about edge cases, input and output formats, example files, success criteria, permissions, and dependencies. Hold off on writing test prompts until these are settled.

Useful question formats:

- "If information is missing, should the skill ask, make a labeled assumption, or produce a draft marked incomplete?"
- "Should it work with any source you give it, or only specific approved sources?"
- "Does any action need your confirmation because it is external, irreversible, or high impact?"
- "What would make you reject an output?"
- "Who will use this skill, and what can they already be assumed to know?"

If you have research capabilities, such as documentation search or a way to look up similar skills and good practices, use them before asking the user things you could find yourself. Run research in parallel if you can, otherwise one step at a time. Arrive with context so the user has less to explain. If sources conflict or requirements stay unclear, say so instead of inventing a rule.

## 4. Choose the structure

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

These are guides. Follow any limits your platform sets. Key patterns:

- If the main instructions grow long, add a layer of hierarchy: move detail into reference files and say exactly when to read each one.
- Point to every reference file from the main instructions, with guidance on when to use it.
- Give long reference files a table of contents.
- When a skill supports several variants (for example, deploying to different hosting providers), keep the shared workflow and variant selection in the main file and put each variant in its own reference file. The AI then reads only the one it needs.

Keep a skill focused. Split unrelated jobs into separate skills when they have different audiences, permissions, sources of truth, or definitions of done.

## 5. Write the skill

### Required parts

- **Name:** a short, stable identifier.
- **Description:** what the skill does and when to use it. This is usually the main thing that decides whether the AI uses the skill, so put all "when to use" information here, not in the body.
- **Compatibility (optional):** required tools or dependencies, only if they are not obvious.
- **Instructions:** the body.

### Writing the description

AI systems often under-use skills, skipping them when they would help. Counter this by making descriptions slightly assertive. Instead of "How to build a simple dashboard for internal data", write "How to build a simple dashboard for internal data. Use this whenever the user mentions dashboards, data visualization, internal metrics, or wants to display company data, even if they don't say 'dashboard'."

Guidelines:

- Keep it short. Respect your platform's length limit; if there is none, one or two sentences is a good default.
- Lead with the phrases and situations that should trigger it.
- Include cases where the user implies the job without naming it.
- Add scope limits only where false activation would be costly.
- Do not put the workflow itself in the description.

If the user's platform offers different ways to reach a skill, such as automatic activation, grouping under a routing skill, or manual invocation by name, ask which fits. A sensible default is automatic for general workflows and manual for command-style skills that should run only on request. If many skills share one area, grouping can keep the always-visible list manageable. After adding, renaming, or removing a skill, run whatever registration or validation step the platform provides.

### Safety: no surprises

A skill must not contain malware, exploit code, or anything that compromises security. Its contents should not surprise the user given its description. Decline to build misleading skills or skills meant for unauthorized access, data extraction, or other harm. Ordinary creative uses, such as a role-play persona, are fine.

### Writing style

- Use the imperative form.
- Explain why things matter instead of stacking unexplained commands. Capable AI systems follow reasoning better than rigid rules. If you find yourself writing ALWAYS or NEVER in capitals, treat it as a warning sign and explain the reason instead. Keep firm rules for authorization, privacy, safety, data integrity, and irreversible actions.
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
Input: Added user login with token-based sessions
Output: feat(auth): add token-based login
```

Also cover, as needed: required inputs and what to do if they are missing; the normal workflow and its branches; checks to run before finishing; and failure behavior for missing inputs, unavailable tools, ambiguous requests, failed validation, and high-impact actions that need confirmation.

## 6. Write test cases

After the draft, write two or three realistic test prompts, the kind of thing a real user would type. Share them: "Here are a few test cases I'd like to try. Do these look right, or do you want to add more?" Then run them.

Save tests in a simple structured file. Leave checks empty for now; you will draft them while runs are in progress.

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

Cover meaningful variety: a typical request, an incomplete or ambiguous one, a format-sensitive one, and, if relevant, one that should lead to a confirmation or refusal. Give each test a descriptive name, not just a number.

## 7. Run and evaluate the tests

Treat this section as one continuous sequence. Do not stop partway.

### Organize the workspace

Keep results in a workspace next to the skill, organized by iteration and test case. Create folders as you go, not all up front.

```text
[skill-name]-workspace/
├── skill-snapshot/              # only when improving an existing skill
├── iteration-1/
│   ├── [test-name]/
│   │   ├── with-skill/          # outputs from the skill under test
│   │   ├── baseline/            # outputs from no skill or the old version
│   │   └── [test details, run data, grades]
│   └── [benchmark summary]
└── iteration-2/
```

### Step 1: Launch all runs together

If you can run independent helper agents, launch both a with-skill run and a baseline run for every test case in the same round, so they finish around the same time and run under similar conditions. Do not run the with-skill versions first and the baselines later.

Run instructions template:

```text
Execute this task:
- Skill location: [path to skill, or "none" for a no-skill baseline]
- Task: [test prompt]
- Input files: [files, or "none"]
- Save outputs to: [workspace]/iteration-[N]/[test-name]/[with-skill or baseline]/
- Outputs to save: [what the user cares about, e.g. "the final spreadsheet"]
```

Choose the baseline by situation:

- **New skill:** same prompt, no skill.
- **Improving a skill:** snapshot the current skill before editing and point the baseline at the snapshot.

If an iteration uses new or changed prompts, write fresh test details for it; do not assume they carry over.

### Step 2: Draft checks while runs are in progress

Use the waiting time. Draft objective checks for each test and explain them to the user. If checks already exist, review them, explain what they verify, and adjust if needed.

Good checks are objectively verifiable and have descriptive names that make sense at a glance. Examples: required sections are present; the produced file opens; totals match the source; missing inputs are flagged. Do not force checks onto subjective qualities; those need human review. Tell the user what they will see when results are ready.

### Step 3: Record run data as each run finishes

If your environment reports elapsed time or resource use when a run completes, save it immediately for that run. Some environments report this only once, so record each result as it arrives instead of batching. A simple record: time taken, resource use (such as tokens or cost), and any errors.

### Step 4: Grade, aggregate, analyze, and present

1. **Grade each run** against its checks, using a separate grader if available. For checks a script can verify, write and run a script; it is faster, more reliable, and reusable across iterations. Save each result with the check text, pass or fail, and evidence. Keep field names consistent so any review tool can read them:

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

2. **Aggregate** into a benchmark summary: pass rate, time, and resource use for each configuration, with average, spread, and the difference between with-skill and baseline. List each with-skill result next to its baseline.

3. **Analyze** what the totals hide:
   - Checks that pass equally with and without the skill do not show what the skill adds.
   - High variation across repeats may mean a flaky test or unclear instructions.
   - A quality gain may not justify a large time or cost increase.
   - Several failures may share one root cause.

4. **Present results to the user before you start fixing things yourself.** Get outputs in front of the person as early as possible. Use an existing review tool if one is available rather than building a custom one. A good review view has two parts:
   - **Outputs:** one test at a time, showing the prompt, the produced output (rendered where possible), the previous iteration's output, formal grades, a feedback box, and earlier feedback.
   - **Benchmark:** pass rates, timing, and resource use per configuration, with per-test breakdowns and analysis notes.

   Tell the user something like: "The results are ready. One view lets you click through each test and leave feedback; the other shows the numbers. Let me know when you're done."

### Step 5: Read the feedback

Collect feedback per run, in whatever form the review produced:

```json
{
  "reviews": [
    {"run_id": "chart-request-with-skill", "feedback": "the chart is missing axis labels"},
    {"run_id": "summary-request-with-skill", "feedback": ""}
  ]
}
```

Empty feedback usually means the output was fine, though it is not proof the skill is complete. Focus on tests with specific complaints. Shut down anything you started for the review.

## 8. Improve the skill

This is the heart of the loop. Take your time. Draft a revision, then reread it fresh and improve it.

1. **Generalize from feedback.** The skill will be used many times on many different requests. You are iterating on a few examples only because it is fast. A skill that works only for those examples is useless. Avoid narrow, overfitted fixes and oppressive rules. If a problem persists, try a different framing, metaphor, or working pattern; experiments are cheap.
2. **Keep it lean.** Remove what is not earning its place. Read the run transcripts, not just the final outputs. If the skill is making the AI waste effort, remove the part causing it and see what happens.
3. **Explain the why.** Even if feedback is terse or frustrated, work out what the user actually needs and put that understanding into the instructions.
4. **Bundle repeated work.** If several test runs independently wrote similar helper scripts or followed the same multi-step routine, write it once, add it to the skill's scripts, and tell the skill to use it.
5. **Preserve what works.** Do not break behavior the user already liked while fixing something else.

### The iteration loop

1. Apply the changes.
2. Rerun all tests into a new iteration folder, including baselines. For a new skill, the baseline stays "no skill". For an existing skill, choose either the original version or the previous iteration and say which.
3. Show the new results, with previous outputs and feedback alongside.
4. Wait for the user to finish reviewing.
5. Read feedback, improve, repeat.

Stop when the user is happy, feedback is consistently empty across meaningful tests, or you are no longer making meaningful progress.

## 9. Optional: blind comparison

When the user asks "is the new version actually better?" and wants rigor, give two outputs to an independent evaluator without saying which version produced which. Have it judge against a shared rubric: correctness, completeness, clarity, constraint adherence, and usability. Then analyze why the winner won. This needs an independent evaluator and is usually unnecessary; human review is normally enough.

## 10. Optional: tune the description for activation

Do this after the skill itself works and the user agrees it is in good shape.

### Step 1: Write activation test queries

Write about 20 queries, a roughly even mix of should-activate and should-not-activate.

```json
[
  {"query": "[realistic user prompt]", "should_trigger": true},
  {"query": "[near-miss prompt]", "should_trigger": false}
]
```

Make them realistic and detailed: file names, a bit of job context, column names, casual phrasing, abbreviations, occasional typos, varied lengths. Focus on edge cases rather than obvious ones.

- Weak: "Format this data", "Create a chart".
- Strong: "ok so my manager sent me a spreadsheet (it's in my downloads, called something like 'Q4 sales final v2') and wants a column showing profit margin as a percent. revenue is column C and costs are D i think".

Should-activate queries: vary phrasing and formality, include requests that never name the skill or file type but clearly need it, include unusual valid uses, and include cases where this skill competes with another and should win.

Should-not-activate queries: use near-misses that share keywords or concepts but need something different, such as adjacent domains or ambiguous wording that a keyword match would catch. Avoid obviously irrelevant negatives; "write a sorting function" tests nothing for a document skill.

An AI usually consults skills for tasks it cannot easily do alone. Simple one-step requests may not activate any skill, however good the description. Use substantive queries where the skill would genuinely help.

### Step 2: Review the set with the user

Let the user edit queries, flip labels, and add or remove entries, using an editable review page if available or directly in conversation. Bad test queries produce bad descriptions, so this step matters.

### Step 3: Run the optimization loop

If the environment supports automated activation testing, tell the user it will take a while, run it in the background, and give progress updates. A sound loop:

- Splits queries into about 60 percent for improving and 40 percent held out.
- Tests the current description, running each query several times to get a reliable activation rate.
- Proposes improved descriptions based on failures.
- Re-tests each candidate on both sets for a few rounds.
- Picks the best description by held-out score, not training score, to avoid overfitting.

Test with the same AI model the user actually works with, so results match real behavior. Without automated testing, walk through the query set manually and judge whether the description would route each one correctly.

### Step 4: Apply the result

Update the description, show the user the before and after, and report the scores.

## 11. Adapt to your environment

| Capability missing | Adaptation |
|---|---|
| Independent helper agents | Run each test yourself by following the skill, one at a time. Skip baselines, numerical benchmarking, and blind comparison. Call this a sanity check, not a rigorous comparison; human review compensates. |
| A display or browser | Write review material to a standalone file the user can open, or show prompts and outputs directly in the conversation. Save files the user must inspect and say where they are. Ask "How does this look? Anything you'd change?" |
| Automated activation testing | Skip optimization or review the query set manually against the description. |
| Parallel runs keep failing or timing out | Run tests in sequence instead. |
| Write access to the installed skill | Copy it to a writable location, edit there, and package from the copy. |

When updating an installed skill, keep the original name and folder name. Do not create a "v2" copy unless the user asks.

## 12. Package and hand off

If a packaging tool is available, package the skill in the user's chosen format and tell them where the result is so they can install it. Include only the resources needed for normal use.

Pre-delivery audit:

- [ ] Name is stable and appropriate.
- [ ] Description states what the skill does and when to use it, within the platform's limits.
- [ ] Instructions do not depend on undeclared tools, private conventions, or personal access.
- [ ] Every bundled resource is referenced, clearly named, and explained.
- [ ] No credentials, private identifiers, confidential records, or sensitive examples are included.
- [ ] Any people-related behavior uses only authorized, minimal, relevant information.
- [ ] Any retained tests are safe to distribute.
- [ ] If the skill will be shared in a collection, the decision to include or exclude it is recorded, it has passed privacy and quality review, and any public identifier stays stable (keep old identifiers as aliases if renamed).

Give a short handoff note: what the skill does, required capabilities, known limits, and a quick way to test it.

## Readiness gate

A skill is ready when it has a clear job, a description that routes the right requests to it, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic tests that it improves outcomes. A long file is not the same as a reliable skill.

## Common failure modes

| Failure | Fix |
|---|---|
| Revising before the user has seen any outputs | Present results for human review first |
| Fixes tailored to the test examples | Find the general cause and fix that |
| Many capitalized absolute rules | Replace with explained reasoning, except for true hard boundaries |
| Vague or timid description, so the skill is rarely used | Lead with trigger phrases and name implied use cases |
| Checks that pass with or without the skill | Replace with checks that show the skill's added value |
| Lost timing or resource data | Record it as each run completes |
| Easy, obviously irrelevant negative queries | Use near-miss queries that share keywords |
| Calling a self-run sanity check a rigorous comparison | Label it honestly |
| Assuming one person's tools, limits, or conventions | Ask the user for their platform's rules and use those |

# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate distinct options for a decision, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs credible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas. It is to surface genuinely different paths, show their tradeoffs clearly, and leave the user with a small set of meaningful choices.

## 1. Gather relevant context

Begin with the information the user supplied. If they provide links, documents, discussion records, prior decisions, research, or other accessible materials, review only the sources relevant to the decision.

If the question is not self-contained, retrieve a small number of high-value sources that may materially change the options, such as:

- Earlier decisions and the reasons behind them
- Existing commitments, deadlines, budget limits, or technical constraints
- Evidence about what has already been tried
- Relevant stakeholder needs, ownership boundaries, or approval requirements

Use private communications or records only for a legitimate purpose and with clear authorization. Use the minimum relevant information, omit unrelated personal or sensitive details, and keep the output within the appropriate access boundary.

Do not search broadly by default. If key information is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- What the user is actually deciding
- Important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should distinguish options

The stated request may describe a symptom or a preferred solution rather than the underlying choice. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited budget and timeline?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly requests an immediate first pass. A wrong framing produces irrelevant options.

## 3. Generate distinct options

Generate five to seven options unless there are genuinely fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes the process, incentives, scope, or framing
- At least one surprising but credible path, such as delaying, partnering, narrowing scope, observing longer, or doing nothing

Do not be contrarian merely to appear creative. A “do nothing” option is useful only when waiting, learning, timing, or avoiding distraction has real value.

Give every option a short, memorable label that makes its approach clear. For each option, provide:

- **What:** One or two sentences describing the approach
- **Strengths:** One or two concrete advantages
- **Weaknesses:** One or two concrete disadvantages, constraints, or failure risks
- **Effort:** Low, Medium, or High

Be candid. Do not soften serious drawbacks or describe alternatives unfairly to favor a preferred option.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include expected impact, cost, effort, speed, risk, reversibility, strategic fit, confidence in evidence, and burden on affected people. Add domain-specific criteria when they matter more.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are instructive, but clearly explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, state in one sentence why it fits this situation, constraints, and goals—not merely why it is attractive in general.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the options and recommendations, wait for the user. They may:

- Choose an option
- Request more detail on one option
- Correct the framing or constraints
- Ask for additional options
- Propose a hybrid approach

For a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or hard-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term obligations, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that states the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move to planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The decision framing reflects the real choice rather than only the requested solution
- The options are genuinely distinct
- The obvious option and a credible alternative framing were considered
- Weaknesses and effort labels are plausible and candid
- Recommendations follow the user’s stated criteria and constraints
- Uncertainty, missing evidence, and assumptions are visible
- The output does not make an implementation commitment before the user chooses


---
name: pressure-test
description: Find weak points in a leading strategic idea before commitment by testing its strongest case, critical assumptions, dissent, failure modes, and falsifiable evidence.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or create an implementation plan.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document a decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes defending it.
- If the idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings in the decision.
- If using internal messages, records, research, or feedback, have a legitimate purpose and authorization. Review only the minimum relevant material, keep sensitive personal details out of the output, and stay within the intended access boundary.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before continuing. Do not present the full question set as a questionnaire.
- Use available evidence: metrics, experiments, research, customer feedback, prior decisions, and relevant stakeholder input. Separate facts, inferences, and forecasts.
- Identify dissenters by relevant role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the actual intent. Include the action, expected result, mechanism, timeframe, and conditions required for success.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold. Rank them by the damage caused if wrong, with the most consequential first. Make assumptions observable where possible.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Test or disproof method] |

Replace broad statements such as “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions and adapt later questions to the answers.

Possible question categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that role say, and has the objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence; ask for observed behavior, data, a comparison, or a credible commitment.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Cover a wrong premise, execution risks, and external conditions where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable early signal] | [Check or accountable role] |

A warning sign must appear early enough to permit a course correction.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree and state each role’s strongest likely objection. If that perspective has not been sought directly, mark it as an evidence gap. Silence is not agreement.

Dissent is not an automatic veto. Its purpose is to reveal constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming evidence that would reverse or materially alter the position:

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test incomplete or failed rather than approving the idea.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next step:

- **GREEN — proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER — test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible test, such as a small interview set, expert review, prototype, or short data-collection period. Run the test, then decide with the result recorded.
- **RED — stop, redesign, or reopen options.** A core assumption is weak, downside is unacceptable, or no meaningful falsification criterion can be named. Generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with exactly one concrete next action: a verb, an owner, and a deadline when useful.

> Example: `Research owner: interview five target users this week and compare findings against the adoption assumption.`

## Final audit

Before closing, verify that the output contains:

- a confirmed steelman;
- three to five ranked load-bearing assumptions;
- five to eight forcing questions explored sequentially;
- a pre-mortem with early warning signs;
- credible dissenting roles and objections;
- a clear mind-change criterion;
- a GREEN, AMBER, or RED verdict with its next step; and
- one concrete next action.

Common failures include skipping alternatives, asking every question at once, mistaking confidence for evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and issuing a favorable verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, make clear calls, preserve authorized records, and review outcomes without inventing the user’s views.
---

# Make a decision

Use this workflow to apply enough rigor for the decision at hand: make small choices quickly, examine consequential choices properly, record them only with permission, and review outcomes without rewriting history.

## Core rules

1. **Match rigor to stakes and reversibility.** Most decisions deserve minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user prefers, believes, or decided something they did not actually say.
3. **Separate advice from attribution.** Keep the assistant’s recommendation distinct from the user’s stated view. Include assistant analysis in a record only on request and label it clearly.
4. **Record only with permission.** “Should we do X?” asks for analysis, not for a record. Create or update a decision record only when the user asks to log, track, open, resume, or commit it, or explicitly agrees.
5. **Protect access boundaries.** Before searching a register or reading shared communications, personnel records, customer information, or other sensitive sources, confirm a legitimate purpose and authorization. Use the minimum relevant information.
6. **Do not mistake execution for a decision.** If there is no meaningful alternative, say so and move to planning or doing the work.
7. **Do not deliberate indefinitely.** Once appropriate evidence, challenge, and consultation are complete, make the call and proceed.

Before writing to a shared decision register, confirm that its audience is appropriate. For sensitive matters, such as health, relationships, compensation, or confidential personnel issues, keep the discussion in chat or offer a private record.

## 1. Select the mode

Use the user’s explicit instruction when they give one. Otherwise, if access is authorized, search the chosen decision register for a substantially overlapping decision before creating a duplicate.

- **New:** No matching record exists, or the user asks to start fresh.
- **Resume:** A matching record is open and the user wants to continue considering it.
- **Commit:** An open record exists and the user says they are ready to decide.
- **Review:** A resolved record has reached its review date and has no completed outcome assessment, or is still marked “too early.”

A record’s resolution status means whether the decision was made, not whether the eventual outcome was good. For a non-binary question, mark it resolved once a direction or approach has been selected.

For **Resume**, retrieve the record and append new information; do not overwrite prior reasoning. For **Review**, use the original prediction, confidence, and stated assumptions as the baseline.

## 2. Frame the decision

Put the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What realistic options exist, including doing nothing?
- What deadline, event, or trigger requires a decision?
- What result is sought?
- What happens if no action is taken?

If the issue is broad and credible options do not yet exist, generate options first. Do not pressure-test a vague problem statement.

If only one viable path exists, say:

> This appears to be a task rather than a decision. The next step is to plan or execute it.

Ask one clarifying question at a time when scope is unclear.

## 3. Classify scope

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes; reversible within hours | Decide now; do not record by default. |
| Reversible | Moderate stakes; changeable within days or weeks | Compare a few options; use a light record if useful. |
| Hard to reverse | Significant cost, disruption, or loss if undone | Full analysis, challenge gate, and stakeholder check. |
| Direction-setting | Shapes strategy, culture, finances, or operations for an extended period | Full analysis, explicit dissent, and prerequisite conversations. |

When classification is unclear, ask: **What would it cost to unwind this?** Consider money, time, trust, operational disruption, opportunity cost, and reputation. If the unwind cost cannot be named quickly or is highly uncertain, treat the decision as larger.

If the user calls a decision trivial but cannot explain how it can be undone quickly, reclassify it rather than accepting the label.

## 4. Apply the appropriate rigor

### Trivial

Choose a reasonable default, state a one-sentence rationale, and move on. Do not create a record by default. If the user is stalling, name the cost of delay: attention spent may exceed the cost of an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. For each, state one main strength, one main weakness, and a rough effort or cost.
3. Give a recommendation and the decisive reason.
4. If uncertainty is material, identify the smallest reversible test that could change the call.

| Option | Main strength | Main weakness | Effort or cost |
|---|---|---|---|
| [Option A] | [What it enables] | [Central tradeoff] | [Rough estimate] |

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test covers assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and major stakeholder objections.

If no relevant pressure test has happened in the current decision context, stop the commitment flow and state:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Proceed only after the test is complete or the user explicitly overrides the gate with a reason. Urgency alone is not an override.

If the pressure test finds a serious unresolved failure, do not force commitment. Return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check with people who have relevant expertise, bear consequences, or may reveal constraints.
4. Provide a recommendation labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees, and capture their strongest case fairly.

The decision is not ready until the prerequisite conversation has occurred, unless the user explicitly accepts and records a reason for proceeding without it. If it is rushed, identify what evidence, consultation, or dissent is being skipped and why that matters.

For people-related decisions, use role-relevant capabilities, role alignment, diagnostic evidence, and whether any assessment distinguishes relevant performance. Do not rely on irrelevant personal information or unsupported labels.

## 5. Analyze without inventing certainty

For each serious option, capture what it enables; what it costs, delays, or prevents; its strongest supporting evidence and objection; its key assumptions; and the cost of reversal.

Separate non-negotiable requirements from preferences. Use scores only if they clarify tradeoffs rather than conceal judgment.

Keep these categories separate:

- **User’s stated view:** Only what the user actually expressed.
- **Assistant analysis:** The assistant’s recommendation and reasoning.
- **Open question:** Material uncertainty not yet resolved.

If the user has not stated a position, write “No position stated yet” or leave the field blank. Never fabricate a lean, confidence level, rationale, response to dissent, or final choice.

## 6. Commit and record

Before finalizing, confirm the choice, rationale, reversal conditions, next action owner and date, observable prediction, and the user’s confidence in that prediction.

For meaningful decisions, use a testable prediction:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Use the user’s approved decision register, document system, or private file. A useful record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

For an **open** decision, record context, options, and new inputs, but leave commitment sections blank. For a **commitment**, mark it resolved, record the actual decision date, set confidence, and populate the commitment sections. Do not infer missing user-owned fields.

Default review timing is one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Adjust for a more meaningful event or trigger named by the user.

**Review-reminder gate:** After recording a hard-to-reverse or direction-setting commitment, create a review reminder in an authorized calendar, task system, or equivalent reminder mechanism. The reminder should name the decision, occur on the review date, link to the approved record when appropriate, and give advance notice such as one day before. If no authorized reminder system is available, explicitly give the user a reminder-ready item to add themselves. For reversible decisions, the review-date field or record reminder is normally sufficient unless the user asks for more.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** [Optional additional option.]

## Thinking log
### [Date]
- New inputs, conversations, data, or events
- How the thinking changed
- User’s stated position today: open / leaning / decided

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
The user’s own reasoning, only when the user stated it.

## What would change my mind
Assumptions or evidence that would justify reversing the choice.

## Prediction
By [date], [observable outcome] will happen or not happen.
Confidence: [X%]

## Worries
The most credible downside or failure mode.

---

## Retrospective
To be completed at review.
```

On resume, append a dated thinking-log entry rather than rewriting history. If the user requests that assistant analysis be stored, label it **Assistant analysis, not the user’s position**.

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat an unfavorable result as proof of a bad process, or a favorable result as proof of a sound one.

## Completion message

When a decision is made, summarize it clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [date]
Review: [date or trigger]
Record: [location, if one exists]
```

Use direct language. Challenge weak reasoning with evidence, but do not turn rigor into an excuse for endless deliberation. Once the readiness gates are met, name the decision and move forward.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through recommendation, implementation, verification, and handoff.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem when the solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user’s proposed solution. If they ask to build something, work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is the problem?
- What outcome would make the situation meaningfully better?
- What constraints, dependencies, deadlines, or access boundaries apply?

Write a concise problem statement and descriptive requirements. Describe the desired outcome and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so directly.

Ask only for information that cannot be found in authorized project context, documentation, code, or records. When reviewing private communications or records about people, ensure there is a legitimate purpose and clear authorization; use the minimum relevant sources and details, omit unrelated sensitive information, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Include “do nothing,” “deprioritize,” or “improve the current workaround” as real options when appropriate.

Separate decisions by reversibility:

- **Reversible decisions:** Small choices that are easy to change. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** Persistent data changes, public interfaces, long-lived configuration, security boundaries, migrations, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the decision and rationale when the consequence warrants it.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before creating new ones.

Identify constraints such as compatibility requirements, deployment practices, ownership boundaries, supported environments, security expectations, observability, and rollback needs. Use established system conventions unless there is a clear reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. For example:

- Must preserve existing authentication, privacy, and data behavior.
- Must fit available time, skills, and maintenance capacity.
- Should avoid new dependencies, persistent settings, and public surface area.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not small variations of the same design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Building, buying, or integrating an existing service.

For ambiguous problems, generate a wider set of candidates before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate inputs and fail clearly for invalid states. Do not hide programming errors by silently producing plausible but incorrect output.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Make clean changes at the appropriate design boundary; avoid expedient patches that create future debt.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and their tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Keep the proposal direct. Store it in the user’s chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear, date-prefixed title such as `11 Oct 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration and rollback strategy, test strategy, deployment steps, and follow-up ownership. Place the plan where appropriate reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, security, and failure behavior.

Do not claim success based only on implementation. State what was tested, the results, and what remains unverified. Commit, publish, or deploy changes only according to the user’s repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.


---
name: shape-and-draft
description: Shape consequential documents through evidence review, answer-dependent alignment rounds, readiness checks, drafting, and delivery audit.
---

# Shape and draft a document

Develop an important document by shaping the thinking behind it before writing. Determine what the document must achieve, gather the relevant evidence, resolve material choices with the authorized decision-maker, and draft only when the remaining uncertainty will not materially change the result.

Use this workflow for strategies, narratives, operating agreements, proposals, scorecards, decision memos, and hybrids when the argument, commitments, boundaries, operating model, or document form is not yet settled. Use a lighter process for simple edits, formatting work, or documents whose decisions and content are already clear.

When reviewing private communications, internal records, or information about people, use them only for a legitimate purpose with clear authorization. Review the minimum relevant sources, omit unrelated sensitive details, respect consent and privacy expectations, and keep the draft within the appropriate access boundary.

## Classify the request

A request may identify a proposed document, desired outcome, audience, source material, or some combination. Treat a proposed document type as a hypothesis until the purpose is clear.

Use a **full shaping process** when the document is consequential and material choices remain unsettled, or when the requester asks for deep thinking, multiple question rounds, or close alignment before drafting.

A substantive interview round resolves a distinct layer of choices and uses the answers to determine the next layer. Restating the situation, requesting general approval, or repeating already answered questions does not count as a substantive round.

## 1. Work backwards from the outcome

Start with the change the document must produce. Establish:

- Who will read it.
- What they should understand, decide, approve, or do afterward.
- What is unclear, contested, blocked, or going wrong now.
- Whether the document mainly needs to explain, persuade, decide, coordinate, or govern.

Do not accept “write a narrative” or “make a strategy page” as the goal. Identify the job the document must perform.

## 2. Choose the artifact

Recommend the document form that best serves the goal.

- **Narrative:** Builds shared understanding of why something matters and what bet is being made.
- **Strategy:** Connects a diagnosis to choices, priorities, intended outcomes, and exclusions.
- **Operating agreement:** Defines ownership, interfaces, decision rights, handoffs, and working cadence.
- **Decision memo:** Records a choice, alternatives, rationale, risks, and a review point.
- **Scorecard:** Defines a role or team mission, outcomes, and role-relevant capabilities.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the relevant tradeoff and recommend one form. If the form would materially affect the argument, structure, commitments, or decisions required, ask the authorized decision-maker to confirm it before proceeding.

## 3. Gather and classify evidence

Read supplied material first. Follow stated rules for source selection, authority, citations, and linking. Scale the research to the stakes. For a consequential internal document, review the authorized sources most likely to contain prior decisions, current definitions, evidence, dissent, constraints, ownership context, and relevant performance information.

Apply these rules:

- Respect any stated source-of-truth hierarchy.
- Prefer current, authoritative decision records over discussion notes, recollections, generated summaries, or repeated claims.
- Resolve contradictions where evidence permits, and surface material contradictions that remain.
- Do not ask a decision-maker for facts that available authorized sources can answer.
- Do not edit, overwrite, or otherwise modify source material unless explicitly instructed.
- Do not include sensitive personal information unless it is necessary, authorized, and appropriate for the document’s audience.

Keep evidence separate from alignment:

- Sources can establish what happened, what people said, and what an authoritative record currently states.
- Sources do not automatically establish what the current decision-maker believes, wants to promise, or chooses to exclude.
- A repeated theme, plausible synthesis, or implication is an **inference**, not a settled decision.
- Ask for confirmation of an inference that would become a central claim, commitment, boundary, recommendation, or operating rule.

Before the first interview round, provide a brief situation summary that distinguishes:

- What sources establish.
- What the decision-maker has already confirmed.
- What is inferred but unconfirmed.
- The main tension, gap, or missing logic.
- The artifact you recommend.
- The important uncertainties that only the decision-maker can resolve.

## 4. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds already completed in the current conversation, and do not repeat them.

Do not draft immediately after the first answer round just because one apparent central issue is resolved. Use the next round to test implications, boundaries, counterarguments, definitions, ownership, or execution details exposed by the first answer.

Ask four to eight focused questions per round. If fewer than four material questions genuinely remain, ask all of them and state that this is a narrow final check. Do not add ceremonial questions merely to reach a count.

Each numbered question should normally seek one decision. Do not combine independent decisions, such as ownership, coordination, handoffs, and success measures, into one broad yes-or-no question. Bundled questions create false alignment.

Use a compact question block that supports quick, unambiguous replies:

1. Number questions consecutively: `1.`, `2.`, `3.`.
2. Keep each number attached to the same question across the conversation.
3. For bounded choices, offer three or four mutually exclusive, decision-relevant options labeled `a.`, `b.`, `c.`, and, if useful, `d.`.
4. Put the recommended option first unless prior context makes another order clearer.
5. Use two options only when the decision truly has two distinct states.
6. Put each question and option on consecutive lines without blank lines inside the question block.
7. Let the respondent reject the framing or give a different answer.

Example:

1. Which direction should the document recommend?
   a. Focus first on the highest-impact problem; this narrows scope but makes accountability clear.
   b. Address all related problems equally.
   c. Present the alternatives without a recommendation.
2. Who should make the final decision?
   a. The accountable lead.
   b. A designated cross-functional group.
   c. A shared process with one named final decision-maker.

Each round should:

1. Start with an updated model and state what changed because of earlier answers.
2. Focus on one layer of uncertainty rather than mixing every issue at once.
3. Explain the tradeoff behind the recommended option.
4. Separate source-supported observations from choices the decision-maker must make.
5. Surface contradictions and ask the smallest question needed to resolve them.
6. Include a pressure test when the document is persuasive or strategically consequential.
7. Leave room for a new framing or answer not listed in the options.

A common progression is purpose; strategy; operating model; definitions and measures; then expression, format, and destination. Adapt the sequence to the task, but preserve the answer-dependent loop: later questions must arise from evidence and earlier answers, not from a generic questionnaire.

After every answer round:

1. Match shorthand and free-text answers to question numbers, preserving qualifications such as “mostly c” or “not sure.”
2. Classify each answer as confirming, rejecting, softening, qualifying, or deferring the proposed position.
3. Mark only genuinely unanswered or unclear material choices as open. Do not repeat a settled question because an interface still displays it as pending.
4. Trace downstream implications. A changed audience, softened commitment, new exception, or rejected framing commonly creates another question.
5. Update and show a concise alignment ledger.
6. Generate the next round from remaining material uncertainties and their consequences.

Continue while an unresolved issue could materially change the document. If the requester explicitly asks to draft before the process is complete, name one or two material consequences of the uncertainty, then follow the instruction.

## 5. Maintain an alignment ledger

Keep a compact working record throughout the conversation:

- **Confirmed:** Choices explicitly made by the authorized decision-maker, including relevant earlier decisions.
- **Source facts:** Claims established by current, authoritative evidence but not selected as current choices.
- **Inferred:** Plausible interpretations that remain unconfirmed.
- **Open:** Questions that could materially change the document.
- **Corrected:** Assumptions or source claims that a participant has rejected.

Update the ledger after every answer round. Never reintroduce a corrected assumption. If confirmed statements conflict, surface and resolve the conflict rather than hiding it in vague language. Never promote an inference to confirmed merely because several sources support it.

For a full shaping process, show a concise updated ledger before each later round so the decision-maker can correct mistaken assumptions. Every major claim in the eventual draft must be a confirmed choice, a supported source fact, or explicitly framed as a proposal, assumption, or open question.

## 6. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document’s substance. Before drafting, explicitly run the gate and provide a concise pre-draft synthesis covering the document’s intended job, audience, central position, important boundaries, and deliberate open questions.

For every major planned claim, ask:

> Was this confirmed by the authorized decision-maker, established as fact by authoritative evidence, or merely inferred?

If a material claim is only inferred, ask another question or label it clearly as a proposal. Do not present it as settled.

Check that each relevant category is confirmed, evidence-based, deliberately open, or genuinely not applicable:

- Goal and audience.
- Artifact type.
- Central argument or bet.
- Scope and exclusions.
- Definitions and thresholds.
- Ownership and decision rights.
- Interfaces and handoffs.
- Success measures and evidence standards.
- Tone, length, format, and destination.

For persuasive documents, complete a skeptical-reader pass:

- What is the strongest objection from the actual audience?
- Which premise, commitment, evidence claim, or safeguard would they dispute?
- Has the intended response been confirmed or supported by evidence?

Close alignment does not require artificial certainty. It means remaining uncertainty is low impact or clearly represented as unresolved.

## 7. Draft and deliver

Follow the stated voice, style preferences, accessibility needs, format, and delivery requirements. Where no style is specified, use clear, direct language appropriate to the audience.

Write the smallest document that accomplishes the agreed purpose. Prefer clear claims, concrete decisions, explicit ownership, and clear boundaries over polished but vague abstractions. Distinguish current decisions from proposals, assumptions, and future review points.

Keep the document structurally readable:

- Do not let a section become a long, flat inventory. For action-oriented documents, use no more than seven top-level bullets per section when possible, and prefer five or fewer for the main outcome section.
- If more points seem necessary, combine related points under a clear lead phrase, cut lower-value detail, or place supporting detail in an appropriate linked reference.
- Use bullets only for genuine lists. Write bullets as full sentences unless they are compact labels.
- Ensure headings are visually and structurally separate from preceding lists. Do not leave an accidental empty paragraph or let a heading inherit list formatting.
- Inspect rendered output for inconsistent indentation, orphaned bullets, awkward page breaks, and other visual failures, not only underlying document structure.

Make the draft as simple as the substance allows:

- Prefer short, common words over formal or inflated language.
- Write complete, natural sentences. Keep one clear line of thought in each sentence, but do not split connected ideas into choppy fragments.
- State the point first. Remove warm-up text, repeated context, process narration, and unnecessary qualifications.
- Turn abstractions into concrete claims, actions, examples, owners, dates, or tests where useful.
- Use focused paragraphs and explain complex ideas as clear sequences of full sentences.
- Prefer the more concise version when it preserves meaning. Concision removes unnecessary ideas and words; it does not require every sentence to be short.
- Preserve hard ideas when they matter, but explain them in plain language rather than jargon.

Honor the requested destination using the user’s chosen system. If text is requested in the conversation, provide text without changing source material. If a document must be created or updated elsewhere, do so only as instructed and verify that the intended content is present.

## 8. Audit before delivery

Compare the draft against the alignment ledger and source hierarchy:

- Does it solve the agreed problem in the agreed form?
- Does every material choice reflect confirmed decisions?
- Have corrected assumptions been removed?
- Are responsibilities, boundaries, decision rights, and handoffs unambiguous where relevant?
- Are uncertain claims labeled appropriately?
- Are factual claims and citations supported by appropriate sources?
- Is any inference presented as a settled fact or decision?
- Does the document match the requested voice, audience, access boundary, and privacy expectations?
- Can each sentence be understood on the first read?
- Are prose and bullets complete, natural sentences rather than clipped fragments?
- Can any abstract phrase, inflated word, or repeated point be simplified or removed without losing meaning?

Fix mismatches before delivering. Put the deliverable last, without trailing commentary that interferes with copying or using it.

## Failure modes to avoid

- Drafting early because producing text feels productive.
- Treating the proposed artifact as fixed before its purpose is known.
- Asking participants for facts that authorized evidence can answer.
- Mistaking research volume for alignment on current choices.
- Treating a plausible synthesis as a confirmed decision.
- Using a generic questionnaire disconnected from evidence and prior answers.
- Failing to update the working model after each round.
- Stopping after one round without testing consequences.
- Bundling independent decisions into a single question.
- Skipping a consequence round after a commitment is softened or qualified.
- Repeating questions already answered.
- Creating duplicate answer surfaces that can produce conflicting responses.
- Concealing contradictions through vague language.
- Continuing interviews after only low-impact uncertainty remains.
- Writing an inspiring document that leaves decisions, ownership, or execution unclear.
- Presenting sensitive information beyond the audience’s legitimate need to know.
- Mistaking concise writing for choppy writing by using fragments, noun-only bullets, or artificially short sentences.


---
name: gather-context
description: Search the sources that are likely to matter and turn the findings into one concise, well-sourced brief.
---

# Gather context

Use this when the user needs to understand a person, organization, project,
topic, or decision before acting.

## 1. Set the purpose and authority boundary

State the decision, task, or question the research must support. Use private
sources only when the user is authorized to access them and the source is
relevant to that legitimate purpose. Access is not, by itself, a reason to
search a source.

When the subject is a person, apply a stricter boundary:

- Use the minimum relevant sources and information needed for the stated task.
- Do not search private communications merely because they are available.
- Omit unrelated or sensitive personal details and do not infer protected or
  private traits that are not necessary to the decision.
- Respect consent, confidentiality, need-to-know limits, and the subject's
  reasonable privacy expectations.
- Put the brief only in a destination appropriate for the source material and
  intended audience.

If the purpose, authorization, or destination is unclear, resolve it before
searching private sources.

## 2. Choose the effort level

- **Quick:** Check a few obvious sources and answer briefly.
- **Standard:** Search several relevant sources and produce a compact brief.
- **Deep:** Search broadly, verify important claims, and resolve contradictions.

Match the effort to the stakes. Do not search every available system by habit.

## 3. Choose relevant sources

Select sources based on the subject. Possible capabilities include email,
messages, documents, meeting notes, calendar, transcripts, databases, code,
and the public web. Named sources are required, but add another source when it
clearly holds decision-relevant evidence.

Search with more than one useful query for a deep review. If a recent meeting
appears in the results, read its notes or transcript.

## 4. Judge evidence

Prefer primary and current sources. Treat summaries and discussion as weaker
than canonical decisions. Resolve conflicts when possible and state what remains
uncertain. Never invent a link or imply that an unavailable source was checked.

## 5. Synthesize by theme

Lead with what matters for the user's intended action. Organize the brief around
the subject, not around the tools searched. A useful structure is:

- Short summary.
- What is known.
- Relevant history or relationship.
- Current decisions and ownership.
- Open questions and missing evidence.
- Direct source links.

Every sourced claim should let the user reach its supporting evidence.


---
name: learning-tutor
description: Learn a paper, article, or topic through a rigorous Socratic dialogue built on retrieval, explanation, and practical application rather than passive summary.
---

# Learn with a tutor

Help a learner understand, retain, and use a paper, article, post, lesson, or topic through an active dialogue. Favor retrieval, explanation, and application over passive review. The learner should do most of the thinking; the tutor should guide, diagnose, and increase challenge without turning the exchange into a test.

## Core learning principles

- **Retrieve before reviewing.** Do not give an unrequested summary. Ask the learner to reconstruct ideas in their own words.
- **Require explanation.** Ask why, how, under what conditions, and based on what evidence an idea holds.
- **Use learner-generated connections.** Have the learner create examples, analogies, predictions, and applications before supplying them.
- **Create productive difficulty.** Make the task demanding enough to require effort, but calibrated enough that the learner can make a meaningful attempt.
- **Practice transfer.** Ask how an idea applies in an unfamiliar setting, relates to existing knowledge, or changes a decision.
- **Reveal gaps through inquiry.** When reasoning is incomplete or inconsistent, use focused questions to expose the tension. Explain directly only after the learner has had one or two fair attempts.

## Readiness and scope

Start by establishing both the learner’s starting point and their goal. Ask one or two open questions, such as:

- “What do you already believe or know about this topic, and why?”
- “What are you trying to be able to explain, evaluate, or do by the end?”
- “Have you read the material already? If so, what do you remember as most important?”

If the learner has not encountered the source, ask for an initial prediction or working model. Then direct them to inspect a relevant portion before beginning retrieval practice. Do not replace their first engagement with a full explanation.

## Conversation workflow

### 1. Elicit the central idea

Ask the learner to state the main claim, finding, or problem in their own words. Do not invite quotation as a substitute for understanding.

Useful prompts:

- “What is the central claim?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “How would you explain it to a thoughtful friend in 30 seconds?”

### 2. Choose a few high-value ideas

Select two or three ideas that are central, difficult, consequential, or likely to be misunderstood. Do not attempt to cover everything superficially.

For each idea, use this cycle:

1. Ask the learner to reconstruct the idea.
2. Probe its mechanism, assumptions, and evidence.
3. Ask for a self-generated example, comparison, or application.
4. Test it with an objection, alternative explanation, or boundary case.
5. Adjust the next question based on the learner’s response.

Keep each turn short. Usually ask only one or two questions at a time.

## Question toolkit

Choose questions that require reasoning rather than recognition.

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What is the mechanism, step by step?”
- “What evidence would distinguish this explanation from another one?”
- “Can you construct a concrete example from a familiar setting?”
- “Where might this fail or not apply?”
- “What is the strongest objection to this argument?”
- “How does this connect to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one assumption changed?”

Avoid yes-or-no questions unless they immediately require an explanation or defense.

## Response rules

Be warm, rigorous, and specific. Generic praise is not useful. When an answer is strong, identify what makes it strong—for example, a clear causal mechanism, a relevant counterexample, or a distinction between correlation and causation—then raise the challenge.

When an answer is incomplete or incorrect:

1. Do not immediately give the correction.
2. Ask a focused follow-up that exposes the missing assumption, contradiction, or evidence.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, provide a concise clarification.
5. Ask them to restate the corrected idea or apply it to a new case.

If the learner says, “I don’t know,” invite an informed guess first: “Based on what you do know, what seems most plausible, and why?” Give a hint after an attempt, or sooner when the learner lacks necessary foundations.

If jargon appears, ask the learner to define it before defining it yourself. Clarify only as needed for accurate reasoning.

## Calibration and pacing

Increase difficulty when answers are easy or fluent. Ask for a counterexample, competing explanation, prediction, analogy, or application in a different domain.

Reduce difficulty when the learner is lost. Narrow the question, isolate one assumption, use a simpler case, or present two plausible explanations and ask them to defend a choice.

| Learner signal | Tutor response |
|---|---|
| Learner recalls a conclusion but cannot explain it | Ask for the mechanism or evidence that supports it. |
| Learner gives a confident but inconsistent answer | Ask a question that compares the answer with a relevant case or assumption. |
| Learner is overloaded or losing energy | Consolidate the strongest ideas and avoid introducing new major concepts. |

Match the learner’s energy while maintaining intellectual standards. A demanding dialogue should feel collaborative, not punitive.

## Progress checks and audit

Periodically provide a brief, evidence-based checkpoint. State:

- What the learner has demonstrated they understand.
- What remains uncertain, incomplete, or confused.
- What question or concept would be most valuable to revisit next.

Do not treat recognition, memorized wording, or agreement as mastery. Look for accurate recall, explanation, reasoning, and transfer to a new case.

Before moving on, check whether the learner can:

- State the idea without quoting the source.
- Explain why it should be believed.
- Identify at least one assumption, limitation, or objection.
- Apply it to a concrete situation.

## Closing gate

Before ending, ask the learner to turn understanding into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation, a self-generated example, or a future retrieval prompt. End by naming the most useful concept or question to revisit later.

## Guardrails

- Do not summarize unless the learner explicitly asks; even then, invite their own summary first.
- Do not lecture when a well-chosen question can prompt retrieval or inference.
- Do not make questions easy merely to be encouraging.
- Do not cover an entire source at shallow depth when a few important ideas can be understood deeply.
- Do not use a fixed question list as a substitute for responding to the learner’s actual reasoning.
- Keep the interaction primarily question-driven, with brief explanations used to unblock learning or correct persistent misunderstandings.


---
name: write-in-my-voice
description: Draft or revise email in the user’s established voice, verify facts and commitments, and optionally create one reviewable draft in the user’s chosen email system.
---

# Write in my voice

Use this workflow when the user asks to write, reply to, revise, or polish an email. The goal is a concise, copy-ready message that sounds like the user while remaining accurate, appropriate, and within the user’s authority.

## 1. Load the voice profile

Before drafting, read the user’s current writing profile in full, if one is available. A profile may include examples of sent emails, a style guide, approved reusable wording, and a fact bank.

Build or confirm these settings:

| Voice element | What to identify |
|---|---|
| Greeting and sign-off | The user’s usual opening, closing, and name format. |
| Tone | Their normal balance of casualness, warmth, directness, and formality. |
| Structure | Typical sentence length, paragraph length, use of bullets, and first-sentence pattern. |
| Language | Preferred contractions, recurring phrases, punctuation habits, and useful colloquialisms. |
| Avoidances | Words, filler, formatting, or tones the user does not use. |
| Approved material | Current facts, links, scheduling options, boilerplate, and standard replies the user has authorized. |

Use recent, genuinely sent messages as stronger evidence than older examples. If examples conflict, use the most recent consistent pattern or ask the user which preference is current.

Do not access private messages, records, or mailboxes unless the user has a legitimate purpose and has clearly authorized access. Read only the minimum relevant messages and omit unrelated personal or sensitive information from the draft and response.

## 2. Establish the email brief

Identify the minimum information needed to write safely:

1. Who is the recipient, and what is their relationship to the user?
2. What result should the email produce?
3. Is this a new message, a reply, a follow-up, or a revision?
4. What facts, dates, names, links, attachments, decisions, or commitments must appear?
5. What tone is appropriate: routine, warm, firm, sensitive, urgent, or formal?
6. Is there a deadline, approval boundary, or issue that needs careful wording?

If a missing fact would change the message or create a commitment, ask one focused question. Do not invent availability, decisions, prices, timelines, recipient context, opinions, emotional reactions, or promises.

## 3. Adapt voice to the situation

Keep the user recognizable, but do not treat voice as a rigid template.

- For familiar contacts, follow the user’s ordinary level of brevity and informality.
- For new, external, senior, or sensitive recipients, retain the user’s voice while making context and requests clearer.
- For corrections, refusals, conflict, or delays, state the relevant facts and next step plainly. Avoid defensiveness, hollow praise, and excessive apology.
- For requests, make the requested action, responsible party, and timing easy to identify.
- Use an approved reusable response, link, or fact when it fits the current context. Never reuse material that is stale, misleading, or unauthorized.

## 4. Draft the smallest complete message

Use the user’s established greeting and sign-off when appropriate. If no evidence exists, use a broadly useful default: warm-professional, direct, concise, and conventional.

A reliable structure is:

1. Greeting, if useful.
2. The purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Closing and sign-off, if appropriate.

Prefer active verbs, concrete language, short sentences, and short paragraphs. Use bullets only when they make actions, choices, or logistics easier to scan.

Remove material that does not help the recipient act or understand:

- Generic openings or filler.
- Process explanations about drafting or internal work.
- Repeated thanks, praise, or apologies.
- Hedges that weaken a clear statement.
- Unnecessary context and unsupported claims.

## 5. Audit before delivery

Review the draft line by line:

- Does it plausibly sound like the user?
- Do the greeting, sign-off, punctuation, and rhythm match the available evidence?
- Is the level of warmth and formality right for this recipient and situation?
- Are all names, dates, links, attachments, references, and thread details accurate?
- Did the draft add any commitment, factual claim, decision, or emotion not supplied by the user?
- Is the requested action or decision unmistakable?
- Can any sentence be removed without reducing usefulness?
- Does the draft avoid the user’s known style anti-patterns?

If no voice evidence exists, state the assumption briefly only when helpful, then provide the draft. Invite the user to share a few representative sent emails or preferences for future work.

## 6. Deliver or create a reviewable draft

By default, provide only the copy-ready email in chat. Do not add explanation after it unless the user asks for options, rationale, or edits.

If the user explicitly asks for a draft in an email system:

1. Confirm authorization to use that system and the intended account or workspace when necessary.
2. Follow the user’s applicable email-system policies and permissions.
3. For a reply, attach the draft to the correct conversation and preserve the appropriate reply subject convention.
4. Verify that the created draft belongs to the intended thread or conversation.
5. Create the draft once for review. Do not send it, and do not silently replace or update it.
6. If a replacement is needed, explain the change, obtain confirmation when appropriate, then remove the old draft or leave it clearly identified according to the user’s instruction.
7. Give the user a safe way to open the draft for review and final sending, without exposing unnecessary account or message data.

The user remains responsible for reviewing and sending the message unless they explicitly authorize a separate sending action and the system’s permissions and policies allow it.


---
name: professional-social-post
description: Draft, revise, and audit professional social posts that lead with concrete value, fit a defined audience, and remain accurate, defensible, and easy to scan.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a rough draft, an article, transcript, podcast, research finding, announcement, interview, or simple topic.

The goal is not to make an author or organization sound enthusiastic. The goal is to make the right reader stop, understand a useful point, and have a reason to think, respond, save, share, or act. A good post is specific, honest, and useful even when the reader never opens a link or views an accompanying visual.

This workflow is platform-independent. Before drafting, confirm the following choices when they are not already clear:

- **Platform and format:** text post, image caption, document or carousel caption, thread, article promotion, or announcement.
- **Audience:** for example, practitioners, founders, researchers, policy professionals, customers, prospective applicants, or a specialist community.
- **Purpose:** share an insight, explain a concept, announce a meaningful change, promote a longer piece, start a substantive discussion, or support a campaign.
- **Voice:** first-person or organizational voice; formal or conversational; preferred and forbidden words; length; and punctuation or formatting preferences.
- **Distribution:** whether there is an external link, the chosen placement for that platform, and whether visual material accompanies the post.
- **Evidence and permissions:** what supports the claims, and what names, quotes, outcomes, or personal details may be shared.

If the user provides approved posts, a writing guide, audience research, or brand guidance, treat these as the primary voice reference. Do not assume an individual writing style, a particular organization’s practices, or access to private systems.

## Scope and routing

Identify the genre before writing. Different genres need different evidence, structures, and privacy checks.

- **Career or participant case study:** A person’s before-and-after story, often involving training, a program, or a new role. Use a case-study structure: starting point, turning point, concrete outcome, evidence, and lesson. Obtain clear authorization before publishing personal, career, or performance details.
- **Research or evidence post:** A claim based on a report, model, survey, experiment, or analysis. Prioritize methodology, scope, uncertainty, and a conclusion the author can defend.
- **Organizational or product announcement:** Lead with the concrete change and reader relevance, not internal excitement.
- **Article, report, or podcast promotion:** Lead with the strongest insight, finding, or disagreement in the longer piece, not with “new article” or “new episode.”
- **Carousel or document caption:** Give one or two meaningful findings and explain what the visual material adds. Do not repeat every slide.
- **Framework or checklist post:** Present a reusable model, explain its boundaries, and give enough detail for readers to apply it.

When working with private communications, records, or stories about identifiable people, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant information. Omit unrelated sensitive details, respect consent and reasonable privacy expectations, and keep the output within the intended publication boundary.

If the genre is unclear, ask one routing question before drafting:

> Is this primarily an evidence post, a concrete announcement, a case study, a framework, or promotion for a longer piece?

## Accuracy and trust rules

1. **Never invent facts.** Do not fabricate statistics, names, organizations, quotes, testimonials, titles, dates, roles, outcomes, or sources.
2. **Separate evidence from interpretation.** State what the source establishes, then make the recommendation, inference, or personal judgment clear.
3. **Keep meaningful uncertainty.** If evidence has large ranges, assumptions, weak data, limited scope, or correlation rather than causation, say so in plain language.
4. **Use exact details only when supported.** Specific figures and outcomes are stronger than vague claims, but do not convert a rough estimate into false precision.
5. **Request missing evidence early.** If the post depends on an unsupported claim, ask for a source, narrow the claim, qualify it, or remove it.
6. **Avoid manufactured urgency.** A concrete risk plus a realistic response is more credible than broad catastrophe language.
7. **Respect attribution and consent.** Quote, name, or credit people only when authorized and accurately represented.
8. **Do not overstate a promotion.** A longer article, event, service, course, or product may be relevant, but it should not substitute for actual value in the post.

## Audience and voice

Write for the reader most likely to act on the post, not for every possible reader. Specificity is useful because it helps the relevant audience recognize that the post is for them. Broad, polished language often attracts no one in particular.

Use this default voice unless the user specifies otherwise:

- Direct, clear, and conversational.
- Short sentences and concrete nouns.
- Active voice where it improves clarity.
- One principal claim per sentence.
- Sober about problems and practical about responses.
- Confident only where evidence supports confidence.
- Specific rather than promotional.

Avoid these common failure modes:

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are thrilled to announce an exciting initiative.” | State what changed, who it affects, and why that matters. |
| Academic | Long, hedged sentences with unexplained technical terms. | State the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Sweeping danger claims with no mechanism or response. | Name the specific risk, evidence, uncertainty, and practical intervention. |

## Core workflow

### 1. Inspect the source before choosing a template

Read the notes or source material first. Find the strongest thread, which is often not the formal headline.

Look for:

- A surprising fact or contrast.
- A specific number that creates tension.
- A counterintuitive conclusion that can be defended.
- A concrete before-and-after outcome.
- A meaningful strategic trade-off.
- A disagreement between credible views.
- A framework, checklist, or model readers may save.
- A sentence that changes how readers see the problem.

The strongest social angle is frequently a buried detail, not the source’s title or opening paragraph. For example, an article about a broad operational challenge may contain a more compelling post angle in one unexpected finding, a practical constraint, or a decision that changed the outcome.

If several threads are viable, do not quietly choose one. Present two to four options and ask the user to select one.

> I see several viable angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [story, outcome, or disagreement]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Choose one main thread. A social post should not try to summarize every section of a report, conversation, or article.

### 2. Generate hooks before drafting the body

The opening decides whether readers continue. Generate five to ten possibilities, then present a shortlist of three to five when user choice is useful. Each hook must make an honest promise that the body fulfills.

Useful hook patterns include:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific body of evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Named outcome:** “[Person or role] moved from [starting point] to [specific outcome] in [timeframe].” Use only with evidence and permission.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Only use this if the post supports it.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused question:** “Why do two credible groups reach such different conclusions about [specific issue]?”
- **Deliberate trade-off:** “We chose not to optimize for [widely desired outcome].” Use this when the post can explain the rationale and consequence.

Present shortlisted hooks with a strategic explanation:

| Hook | Strategic purpose |
|---|---|
| “[Specific result or claim].” | Leads with a concrete fact that creates immediate curiosity. |
| “[Assumption] misses [specific mechanism].” | Challenges a familiar view and promises an explanation. |
| “I changed my mind about [topic].” | Uses personal stakes to introduce an evidence-based update. |

Apply the swap test: if the main topic could be replaced with an unrelated industry and the hook still works, it is too generic. Add the real mechanism, outcome, number, decision, or tension.

Avoid generic announcement openings, throat-clearing, empty cliffhangers, several rhetorical questions in a row, broad motivational claims, and clickbait that the post cannot substantiate.

### 3. Choose one structure

Use the structure that fits the material. Do not combine several structures without a clear reason.

1. **Counterintuitive claim → evidence → implication** for research, data, and argument.
2. **Changed mind → trigger → updated view → takeaway** for thoughtful first-person posts.
3. **Problem → why it matters → practical response** for explainers and operational content.
4. **Result → how it happened → reusable lesson** for verified outcomes and authorized case studies.
5. **Framework → examples → application** for posts intended to be saved and revisited.
6. **Specific announcement → reader relevance → next step** for meaningful launches or changes.
7. **Strategic trade-off → rationale → consequence** for explaining deliberate constraints or anti-goals, meaning what an author or organization intentionally chooses not to optimize for.

A post can contain a list, but a list is not automatically a structure. Use list formatting only where the content is genuinely a set of distinct findings, options, actions, or criteria.

### 4. Draft: hook, tension, payoff

Use this default shape:

- **Hook:** The strongest claim, result, or tension.
- **Tension or setup:** Why the point matters or which assumption it challenges.
- **Payoff:** The evidence, story, framework, or practical insight. Deliver real value here.
- **Soft close:** Exactly one focused question, takeaway, or pointer to further material.

A useful default is under 300 words, subject to platform norms and substance. Longer posts need a clear reason for every paragraph. A post that explains a complex framework may need more space; a simple announcement may need far less.

Use one- or two-sentence paragraphs for mobile scanning. White space helps readers find the argument. Use bullets only when the content is genuinely list-shaped, such as findings, choices, or steps.

For captions accompanying a carousel or document:

- Establish the central idea.
- Share one or two strong specifics.
- State what the visual material adds.
- Do not create a content-free teaser.
- Do not duplicate the entire visual asset in text.

For article, report, or podcast promotion, put the most useful finding in the post. The longer piece should provide depth, context, methods, examples, or sources, not the only valuable idea.

## Calls to action and links

Use one close only. Strong closes invite a real and bounded response:

- “Which constraint matters most in your work?”
- “What evidence would change your view?”
- “If you have operated this system, where does this model fail?”
- “The full analysis includes the assumptions and source material.”

Avoid vague prompts such as “Thoughts?” and avoid engagement bait that asks people to react, comment, tag, or repost solely to improve reach.

Follow the user’s chosen platform strategy for external links. If the platform or audience commonly prefers links in a comment, use a brief first-comment line that provides context and the destination. If links belong in the post body, integrate them without making the link the main value proposition. Do not present placement tactics, timing tactics, or engagement metrics as guaranteed ranking advantages. Platform behavior changes, so treat distribution choices as testable hypotheses and compare results across several posts.

## Editing pass: remove templated language

Run a separate editing pass after drafting. Cut phrases that sound polished but add no meaning.

Replace or remove:

- Corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Hedging frames such as “it is worth noting” and “one might say,” unless uncertainty is genuinely necessary.
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Abstract nouns such as “journey,” “transformation,” and “paradigm” when a concrete event can be named.
- Transition sentences that merely restate the paragraph before them.
- Dramatic frames such as “The truth is” or “Here is the reality.” State the claim directly.
- Decorative punctuation or formatting that the platform will not render correctly.

Favor periods, commas, and line breaks unless the user requests another style. Use emphasis sparingly, and verify that the platform supports the chosen formatting. Read the post aloud. If it sounds like generic thought leadership rather than a person making a specific, informed point, rewrite it.

## Revision protocol

When the user gives feedback, revise the requested line and its nearby logic first. Do not rewrite the entire post unless asked.

- If the hook is weak, offer several replacement hooks before rebuilding the body.
- If a claim is overstated, strengthen the evidence, narrow it, or soften that claim only.
- If a paragraph is slow, cut setup before adding explanation.
- If the user prefers an earlier sentence, preserve it unless there is a clear reason not to.
- If a source gap emerges, state it plainly and offer a concrete alternative.
- If the user rejects a tone or phrase, identify the pattern behind the rejection and apply the correction consistently in the next revision.

Multiple small options are often more useful than one large rewrite, especially for hooks, closers, and uncertain claims. Be candid about weak material. For example:

> The second paragraph relies on a broad claim that the available source does not yet support. We can add evidence, narrow the claim, or replace it with this concrete example: [example].

## Readiness gate and audit

Do not present a draft as final until it passes this checklist:

- Does the first line earn attention when read alone?
- Does the post make one clear point rather than competing points?
- Is there a concrete outcome, example, number, mechanism, or detail where appropriate?
- Could the author defend the main claim if a knowledgeable reader challenged it?
- Does the post provide value without requiring a click, swipe, or purchase?
- Is uncertainty stated where it materially affects the conclusion?
- Is the language specific to this topic rather than reusable for any industry?
- Is there one focused close?
- Are all names, quotes, figures, and claims supported and authorized?
- Does formatting work on the intended platform?
- Is the tone professional, respectful, and appropriate for the audience?
- Are private details minimized and within the agreed publication boundary?
- Does any promotional mention have a direct, earned connection to the content?

If any answer is no, revise before handoff.

## Handoff format

Provide only what helps the user decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen delivery format.
3. Any unsupported claim, missing input, or uncertain line.
4. Suggested link or first-comment text, when relevant to the chosen platform strategy.
5. One concise publishing reminder, such as responding promptly and substantively to genuine early comments.

## Common failure patterns

- **Announcement disguised as content:** It reports internal excitement but not reader value. Lead with the actual change or lesson.
- **Pure teaser:** It asks readers to click without teaching them anything. Share the core insight first.
- **Unsupported precision:** It uses a striking number without source, scope, or caveat. Verify, qualify, or remove it.
- **Generic inspiration:** It sounds positive but names no mechanism, choice, or action. Add a concrete decision or example.
- **Overpacked summary:** It covers every part of a source. Select one thread and save the rest for later posts or the original material.
- **Bolted-on promotion:** It ends with an unrelated product, course, service, or event pitch. Remove the pitch, make a separate post, or establish an immediate and concrete connection.
- **Forced engagement:** It demands reactions or comments. Ask one genuine question or end with a useful conclusion.
- **Unapproved personal story:** It includes a career outcome, quote, or identifying detail without clear permission. Obtain authorization, anonymize the example, or remove it.
- **Formatting mismatch:** It relies on markup, symbols, or layout the platform does not support. Convert it to supported plain text and preview it before publishing.

The final standard is simple: the post should sound like someone with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, or a generic social-media template.


---
name: case-study-post
description: Create an evidence-based case study post with strong hooks, a review-ready draft, quote-card options, approvals, and a publishing checklist.
---

# Write a case study post

Use this workflow to turn authorized source material about a person’s career, learning, professional change, or project outcome into a concise public case study. It works especially well for professional social posts, and can be adapted for newsletters, community updates, recruitment pages, alumni stories, or program pages.

The goal is not to make someone sound impressive through vague praise. The goal is to show a credible, specific change: where they started, what they were considering, what they did, what concretely helped, what they do now, and what a reader can do next.

A strong case study helps the intended reader recognize their own situation in the subject’s before-state. It names the intervention clearly, explains the mechanism without overstating causation, and respects the subject’s privacy and approval rights.

## Authorization and access boundary

Use this workflow only for a legitimate publishing purpose and with clear authorization to access and use the source material. This is especially important when materials include interview transcripts, applications, internal messages, personnel records, or private communications.

Use the minimum relevant sources and information. Do not surface unrelated personal details merely because they are available. Respect the subject’s consent, privacy expectations, confidentiality obligations, and the access boundary of the intended publication.

Before using a detail publicly, ask:

- Is this relevant to the story?
- Is it verified well enough to publish?
- Is it within the publisher’s authorized access and the subject’s reasonable expectations?
- Does it need specific approval from the subject?
- Could the same point be made with less sensitive information?

Do not include private contact details, account information, internal links, confidential documents, personal history unrelated to the story, or sensitive facts that do not directly support the case study.

## Inputs

Ask for all available, authorized source material. Useful inputs include:

- An interview transcript and meeting notes
- An application, intake form, or participant survey
- A current professional profile or approved biography
- Official public work samples, projects, papers, products, or announcements
- A relevant internal message reporting a result, if its use is authorized
- A prior draft, outline, or subject notes
- The target audience, platform, publication owner, and desired call to action
- The organization’s editorial or brand voice guidance
- The subject’s preferred public name, pronouns, and approval status

Before drafting, determine whether the following fields are sufficiently supported.

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns, and consent status |
| Before-state | Previous role, field, goal, uncertainty, or constraint |
| Trigger | Why they joined, applied, changed direction, or took action |
| Intervention | Program, community, resource, event, mentor, or service involved |
| Mechanism | Concrete help, such as a realization, job post, introduction, feedback session, or practical resource |
| Now-state | Current role, organization, team, project, output, or result |
| Timeline | Dates or time spans from the starting point to the outcome |
| Evidence | Verified roles, figures, dates, artifacts, and direct quotes |
| Cost or risk | Pay change, move, uncertainty, career risk, or tradeoff, if relevant and approved |
| CTA | The action the intended reader should take next |

If critical facts are missing, ask focused questions before drafting. Do not guess at organization names, job titles, paper titles, dates, figures, timelines, motivations, or outcomes.

Useful questions include:

1. What was the subject doing before this experience?
2. What were they considering instead?
3. Why did they choose to take part or make a change at that point?
4. What were the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a specific public output, project, placement, publication, product, or result that can be named?
8. Did they take on a meaningful cost or risk that they are comfortable sharing publicly?
9. Which names, figures, quotes, and claims have been approved for publication?
10. Who should this post help or persuade?

## Evidence and verification rules

Never invent facts or upgrade claims for dramatic effect. If a source says someone contributed to a project, do not call them the lead. If they explored an opportunity, do not say they received it. If a role began after the program, do not imply the program caused the hiring decision unless the evidence supports that claim.

Treat automated transcripts and summaries as useful but fallible. They can mishear names, organizations, technical terms, numbers, titles, and quotations. Cross-check important details against a more reliable source, such as direct confirmation from the subject, an official announcement, published work, or a current professional profile.

When sources disagree, use this default reliability order:

1. The subject’s direct, recent confirmation
2. Official public records, published work, or an organization’s approved announcement
3. A current professional profile
4. An original written application or statement from the subject
5. Interview transcript notes or automated summaries
6. Informal third-party messages

Separate these three statement types in private working notes:

- **Verified fact:** A role, date, artifact, figure, or quote supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn from the story. Use only when evidence supports it, and phrase it modestly.

Prefer precise causal language: “the program helped them see the field differently,” “they found the opportunity through the community,” or “feedback strengthened their application.” Avoid claiming that one intervention created the entire outcome.

## Sensitive-content gate

Flag these items for explicit subject approval before publication:

- Salary, pay cuts, financial hardship, or compensation comparisons
- Health, family, immigration, legal, or personal circumstances
- Harsh claims about a past employer, role, or career decision
- Unreleased work, confidential projects, or unpublished titles
- Direct quotations, especially strong opinions or criticism
- Claims about why an employer selected the person
- Claims of impact or causation that cannot be independently verified
- Precise timelines that could expose private circumstances

If approval is unavailable, use an honest approved fallback or remove the point. For example, replace an exact compensation figure with “they accepted a lower-paying role” only if that broader wording is approved and still useful. Do not conceal uncertainty by making the story more dramatic.

## Step 1: Build the story beats

Create a private working outline before writing. Do not show it unless the user asks.

### Before-state

Capture the subject’s previous role, background, and reader-relevant uncertainty. Include what they were considering instead when that alternative mirrors the audience’s present situation.

Keep only details that move the story. Long lists of credentials, books read, or earlier roles usually weaken the post. Keep a detail when it makes the change real or explains the decision.

### Trigger

Identify why the subject acted at that moment. They may have wanted to test whether a career path existed, learn a new field, find collaborators, solve a practical problem, or make a values-led change.

### Mechanism

Find one or two observable things that changed the trajectory. Good mechanisms include:

- Realizing that a field or role was open to someone with their background
- Finding a relevant opportunity through a community
- Having a conversation that clarified next steps
- Receiving feedback that improved an application or project
- Getting a relevant introduction, workshop, or practical resource

Do not say an experience was “transformative.” Say what happened.

### Now-state

Record the current role, organization or team if approved, and what the subject actually does. Translate technical language enough for the intended reader to understand the work.

Use named outputs only when they add proof or interest. One meaningful project, publication, placement, product, or grant is usually stronger than a long credential list.

### Timeline and compression

Map the sequence from the start of the intervention to the current result. Use a short, truthful timeframe when it sharpens the story, such as “five months later” or “the following year.” Do not force a compressed timeline where the facts do not support one.

### Quotes

Pull three to five verbatim quote candidates. Prefer quotes that speak to the reader’s identity or uncertainty, not only to the subject’s achievement. Light trimming is allowed only when it preserves meaning and grammar. Never rewrite a quote into something the person did not say.

## Step 2: Generate three hooks

For feed-based platforms, the first two lines determine whether people continue reading. Write three distinct hooks before drafting the body. Keep each to two short sentences and, where useful for the platform, roughly 140 characters or fewer.

### Hook A: Discovery

Use when the audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a concrete mechanism.

This is the default recommendation when the opening can mirror the reader’s own uncertainty.

### Hook B: Identity collision

Use when the before-and-after contrast is vivid and understandable.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

Use it when the contrast itself is compelling, particularly for a broad audience.

### Hook C: Stakes-led

Use only when a meaningful cost or risk is approved and the intended audience will read it as honest conviction rather than a warning.

**Formula:** The subject accepted a specific cost to do something. Now they are taking a concrete action or doing meaningful work.

Do not use a sacrifice hook if it suggests that participation requires hardship or distracts from a more accessible message.

Choose one recommendation. Give a one-sentence reason it suits the audience, plus a brief reason each alternate is less suitable.

## Step 3: Draft the post

Aim for roughly 160 to 220 words unless the platform or audience needs another length. Shorter is usually stronger.

Use this sequence:

1. **Hook:** Use the recommended hook.
2. **Before-state:** One short paragraph with the previous situation and a relevant alternative path.
3. **Name the intervention:** Clearly state that they joined the program, used the resource, or participated in the community. Do not leave it implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then land the immediate result in plain language. Repeat a key mechanism, such as a community opportunity, if it appeared in the hook and repetition adds clarity.
5. **Current work:** Describe what they do now and why it matters in understandable language.
6. **Optional honest cost:** Include only if approved and genuinely useful.
7. **Optional pull quote:** Include only if it contributes a distinct truth not already expressed by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

A short outcome sequence can work well: “They applied. They got in.” Use it when it adds pace; do not force it.

For platforms where external links may reduce distribution, put the link in a comment, profile page, or designated destination rather than the body. Treat this as a platform-specific publishing choice, not a universal rule.

## Style rules

Adapt to the chosen voice guide. If none exists, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use concrete names, roles, dates, and figures only when verified and approved.
- After the first introduction, use the subject’s first name only if it fits the publication’s tone and the subject is comfortable with it.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Avoid unsupported praise such as “exceptional,” “inspiring,” or “brilliant.”
- Use contractions when the voice is conversational.
- Keep the CTA in full second person: “If you are…” and “you can…”
- Avoid emojis unless they are an explicit brand choice.
- Default to periods, commas, and line breaks rather than em dashes.

On the final pass, remove machine-like phrasing. Cut empty transitions, slow date-led openers, dramatic frames, filler intensifiers, hedging, abstract nouns that replace evidence, balanced “on one hand/on the other hand” constructions, and reflective summaries after the CTA.

Avoid corporate or generic phrases such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm” unless required in an approved direct quote.

Read the post aloud. If it sounds like a generic thought-leadership template, shorten it and replace abstractions with facts.

## Step 4: Quote-card options

Provide three approved, self-contained visual quote options, each under 15 words when possible. Use verbatim source language with only meaning-preserving trimming.

| Category | What the quote should express |
|---|---|
| Discovery | “I did not know this path was open to someone like me.” |
| Mechanism | “I found the opportunity through the community.” |
| Conviction | “I would make the same choice again.” |

Recommend one option. Discovery quotes are often strongest because they work without context and mirror the reader’s uncertainty. Choose a mechanism or conviction quote instead only when it is clearer and more memorable on its own.

## Step 5: Readiness audit and delivery

Before sending a draft for review, check:

- Is every name, role, date, figure, title, and quote verified?
- Were important transcript-derived details cross-checked?
- Does the post show a concrete mechanism rather than only a result?
- Does it avoid overstating causation?
- Is the intervention named clearly?
- Does the opening mirror a real audience concern?
- Is the current work understandable to a non-specialist reader?
- Are sensitive claims and direct quotes flagged for approval?
- Is the CTA clear and addressed to the intended reader?
- Are there no em dashes, unsupported superlatives, corporate phrases, or generic filler?

Create the draft in the user’s chosen document system when one is available. Use a clear title, such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and the two alternatives
- The three quote-card options and recommendation
- A list of items needing subject approval
- A list of missing information that would strengthen the post
- The document location or link, if applicable

Do not treat the first draft as final. If feedback says “make the hook better,” generate new hooks rather than making small edits. If asked to make it shorter, cut secondary biography first while protecting the mechanism and outcome. If the subject rejects a sensitive line, use the approved fallback or remove it without weakening unrelated parts of the post.

After final acceptance, review feedback for reusable lessons. Update the workflow only when a recurring pattern is clear, such as a missing intake question, a consistent voice preference, or a repeated verification issue. Do not invent process changes from a clean review cycle.


---
name: create-editorial-cover-images
description: Create and review eight article-specific cover-image options through five initial concepts and three evidence-based improvements.
---

# Create editorial cover images

Turn a written article into eight finished editorial cover-image options. Develop five genuinely different first-round concepts, generate and inspect each rendered result, then create three new options based on what the first round actually revealed. The user should receive finished, accessible images that clearly relate to the article, not merely a list of hypothetical prompts.

Use the user’s chosen image generator, publication destination, medium, and approved access method. Do not assume a particular service, account, browser, house style, or aspect ratio. If the user explicitly requests prompts only, follow the prompt-only branch.

## Purpose, authorization, and readiness

A cover image should do more than decorate a topic. It should express the article’s central move, emotional register, or defining metaphor in a form that still communicates at thumbnail size.

Before generating, confirm the following:

- You have the complete article or the minimum necessary excerpts. Do not create article-specific concepts from a title alone unless the user explicitly accepts a broad interpretation.
- You have a legitimate purpose and clear authorization to use unpublished, private, or sensitive material. Use only the information needed for the visual brief.
- The image generator and intended destination are clear. If the chosen service is unavailable, report the blocker and ask before moving article material or prompts to a different service.
- The intended placement, crop, and output format are known or can be selected with the user.
- Restrictions about people, places, brands, factual depiction, lettering, source material, or sensitive content are known.

Do not paste a full unpublished article into an image generator by default. Extract only the visual facts, metaphors, and tone needed for the prompt. Omit unrelated personal details, identifying information, sensitive claims, and private context. Do not imply that an imagined scene documents a real event unless the source supports that depiction and the user wants a factual depiction.

If the article copy is absent, ask for it before proceeding. If only a summary is available, explain that the image will be based on the summary rather than a full reading.

## Establish the creative brief

Read the article end to end before proposing images. Identify these elements internally:

- **Central move:** the idea, tension, realization, or change in perspective the reader should retain.
- **Emotional progression:** where the writing becomes quiet, accelerates, turns, becomes uncertain, or resolves.
- **Concrete source imagery:** objects, places, actions, comparisons, and metaphors already present in the article.
- **Tone:** for example, reflective, investigative, urgent, hopeful, defiant, celebratory, or sober.
- **Editorial constraints:** what must not be shown, what could be misread, and whether a literal depiction would be misleading.

Use this analysis to make decisions. Do not automatically return a long summary of the article. Never invent facts about the article. Every concept must be grounded in the source or clearly framed as a visual interpretation.

Reuse preferences already stated in the conversation. Ask only for missing choices that materially affect the output, and collect all outstanding answers before treating a partial response as a complete brief. Make the options specific to this article rather than using generic design-menu labels.

Ask about these four areas when needed:

1. **Mood:** Offer three or four valid readings of this particular article. Link each option to a distinct emotional beat or argument in the piece.
2. **Subject:** Offer fitting choices such as an anonymous figure, landscape only, a single symbolic object, an architectural or environmental scene, or an abstract composition. Respect restrictions on depicting people or real places.
3. **Palette:** Offer palettes with named colors, value range, and contrast character. Describe alternatives in ways that do not depend only on distinguishing color labels.
4. **Orientation:** Confirm the intended placement: wide header, square preview, portrait cover, or a supplied custom ratio. Verify destination requirements when possible rather than carrying over dimensions from another publication.

Also establish the medium or visual style if it remains open. Useful choices include documentary photography, watercolor, ink drawing, collage, printmaking, restrained three-dimensional illustration, or abstract painting. Select a style according to the article and audience, not an unstated personal preference.

Keep a compact working brief containing the central move, selected mood, subject constraints, palette, medium, orientation, generator, and exclusions. Carry this brief through both rounds without repeatedly asking the same questions.

## Develop five distinct concepts

Present exactly five first-round concepts. For each, provide:

1. A short title.
2. A one- to three-sentence description of what the viewer sees.
3. A short statement of the article beat, argument, or emotion the concept expresses.

Give a one-line initial recommendation, then generate all five when finished images are requested. Do not ask the user to select a concept before the first round unless they explicitly request that gate.

The concepts must differ in subject, composition, visual metaphor, and emotional emphasis. Five variations of the same person in the same setting are not meaningful options. Unless the brief rules them out, include at least one landscape-only concept and one single-object or symbolic concept. Anonymous figures can be useful when universality matters, but they are not required.

Use this test before retaining a concept: could the same explanation fit almost any article on the topic? If yes, replace it with an interpretation tied more directly to this article’s argument, image, or emotional turn.

## Write effective visual prompts

Write one self-contained prompt per concept. Explicitly request an image so the generator does not return text or a revised prompt. Adapt formatting to the target generator’s documented capabilities while preserving the visual logic.

Use this structure, combining sections only where that makes the prompt clearer:

```text
Create one image: [medium, overall editorial character, and requested format].

Subject: [what is in frame, where it appears, what it is doing, scale and prominence. Place relevant exclusions here, such as no recognizable face, no logos, or no text.]

Setting: [surroundings, depth, foreground and background relationships, and what recedes or remains empty.]

Light and palette: [specific colors, their transitions, light direction, contrast, and atmosphere.]

Technique: [physical or visual properties of the selected medium, texture, edge treatment, level of detail, and negative space.]

Mood: [the feeling and its link to the article’s central move.]

Composition: [focal point, eye path, placement of major shapes, crop, negative space, and aspect ratio.]

Avoid: [only artifacts, visual conventions, or content that conflicts with the brief.]
```

Name colors precisely. “Pale ochre ground, slate-blue shadows, faded apricot light, and a deep violet horizon” is more actionable than “warm and moody.” Specify how colors relate, where transitions occur, and how saturated they should be.

Describe the actual characteristics of the medium. For watercolor, useful direction may include broad wet-on-wet washes, pigment blooms, visible paper grain, transparent layers, selective edges, and unpainted paper. For photography, describe lighting, distance or depth cues, and realism level instead. Do not ask for photographic sharpness and loose, minimal watercolor marks in the same area without a clear reason.

Put important exclusions near the relevant positive instruction as well as in the final avoidance line. For example, say “a back-turned silhouette with no visible facial features” in the subject description. Avoid unintended lettering, logos, watermarks, borders, and interface-like artifacts unless the user specifically requests them.

## Generate the first five

Use the selected generator through an authorized method that respects its available controls and the user’s access boundary. Respect spending limits, consent expectations, and approval gates. Do not bypass a login, approval request, rate limit, or access restriction. If the service is blocked, state what is blocked, preserve completed work where possible, and ask only for the action needed to resume.

Maintain a working record for each option: number, title, concept, full submitted prompt, status, verified output location, and visual-review notes. This prevents prompt loss, inconsistent numbering, and accidental substitution of unfinished output.

For each submission:

1. Create a separate, clearly distinguishable generation context when the generator supports it.
2. Enter the complete prompt and verify that the visible input contains the intended text before sending.
3. Request one image now, rather than a prompt, explanation, or textual response.
4. Confirm the request was accepted with the complete prompt.
5. Confirm that a rendered image exists and can be opened at useful size.

An accepted message, spinner, placeholder, elapsed time, thumbnail shell, or model description is not proof of completion. Inspect loaded image pixels. If an error appears, first check whether an image already completed before retrying, so unnecessary duplicates are not created. Keep failed attempts separate from finished options.

Independent jobs may run concurrently when the generator safely supports that pattern. Keep interactions with a shared interface sequential and based on the current visible state.

## Inspect all five before making improvements

View every first-round image at useful size. Judge the rendered result, not the generator’s claims or the prompt’s intended result. Also inspect each image at approximate cover-thumbnail size.

For each option, assess:

- Does it communicate the central idea and emotional tone?
- Is the focal subject or action immediately understandable?
- Did the requested medium, palette, shape, and composition survive generation?
- Is it too busy, generic, sentimental, static, literal, or visually confusing?
- Are there visible anatomy, perspective, object, construction, lettering, or artifact problems?
- Does it still work after cropping or reduction?

Only after reviewing all five should you design options six through eight. For each new prompt, record the observed strength to keep, the weakness to correct, and the visible change expected to help.

A useful second-round spread is a refinement of the strongest first-round image, a combination of strengths from different images, and a new direction that addresses a gap in the first round. Use judgment rather than forcing this pattern. The goal is a stronger range, not mechanical compliance.

Fix causes rather than symptoms. When a scene is cluttered, remove competing objects or simplify the action before adding decorative detail. When an image resembles a photograph with a painted filter, request fewer large forms, selective edges, meaningful negative space, and the actual marks of the chosen medium. When a result feels like generic travel, office, or lifestyle imagery, reconsider the metaphor or point of view rather than adding more props.

Give the user a short progress update describing what the rendered images revealed and what the next three will improve. Do not ask for another selection unless the user requests one.

## Generate, inspect, and hand off options six through eight

Generate three distinct second-round images using the revised prompts. Preserve the first five unchanged for comparison. Apply the same submission, completion, and visual-inspection checks to each new image.

If a generation fails or returns text only, repair it in the same generation context where possible. Do not count unsuccessful requests as finished options, and do not silently substitute an old image. If a rate limit or access gate prevents completion, say exactly which options are complete and which remain blocked.

Before delivery, pass this readiness gate:

- There are eight distinct completed images, not eight prompts or placeholders.
- Each image was inspected at useful size.
- Each output can be opened from its final handoff location.
- Titles, numbers, links or file references, and review notes match.
- Options six through eight are clearly marked as second-round options.
- The user can access the images within the authorized sharing boundary.

Recommend the strongest rendered image in one short sentence based on the actual visual result. Then provide a numbered list of all eight titles and verified output locations, marking the final three as second-round options. Make that list the final deliverable block. Do not claim completion when some outputs are failed, inaccessible, or uninspected.

## Prompt-only branch

When the user explicitly asks for prompts only, do not generate images. Read the article, establish the needed preferences, and propose five concepts. Wait for a selection unless the user already selected concepts or asked for all prompts.

Deliver each selected prompt in its own fenced code block using the prompt structure above. If combining concepts, give one brief sentence explaining the combination immediately before the prompt. Do not invent a visually informed second round when no images were generated and reviewed. Put the selected prompts last, with nothing after the final code block.

## Adapt to another generator

When creating a version for another generator, preserve the core subject, composition, palette, mood, exclusions, and format. Change only the syntax and controls required by the target tool.

Check current supported conventions before using parameter flags, model versions, or aspect-ratio controls. If a version is necessary and unclear, ask once rather than guessing. Keep platform-specific variants separate and labeled. A change in generator should not quietly become a different creative concept.

## Learn from outcomes

After the user selects an image, accepts a prompt, or gives clear feedback, capture only durable, authorized lessons. Useful lessons include a recurring preference for sparse compositions, a prompt constraint that prevented a common artifact, or a verified convention of an approved generator.

Distinguish explicit user feedback from your own aesthetic judgment. Do not retain private article content, identifying facts, sensitive details, access information, or one-off subject matter as reusable defaults. Do not alter the workflow when a run revealed no general lesson.


---
name: plan-your-day
description: Choose one most important outcome, protect time for it, and make a realistic plan around existing commitments.
---

# Plan your day

Use this when the user wants to choose priorities, schedule work, or recover a
day that has become reactive.

## 1. Read the real day

Check the calendar, current tasks, deadlines, unfinished commitments, energy,
and any personal constraint the user chooses to share. Use the user's local
date and time. Do not propose work inside existing commitments.

## 2. Choose one most important outcome

Ask what result would make the day count. Turn it into a binary finish line,
such as sending a draft or making a decision. Avoid labels such as “work on” or
“make progress.”

Test the choice:

- Is it important rather than merely urgent?
- Can the user influence the result today?
- Does it fit the available focused time?
- Is another task more likely to be productive-looking avoidance?

## 3. Protect a focused block

Find the best uninterrupted window and match the task to the user's likely
energy. Break long work into realistic chunks with short breaks. Include setup
and a clear first action so the block begins without another decision.

## 4. Fit the rest around it

Choose a small number of secondary tasks. Batch shallow work. Remove or defer
anything that makes the plan implausible. Leave space for meals, movement,
travel, recovery, and unexpected work.

## 5. Pre-mortem

Ask what displacement work is most likely to steal the focused block. Name one
specific counter, such as closing messages, preparing the source document, or
starting before a meeting-heavy period.

## 6. Record the plan

Write the outcome, focused block, secondary tasks, and main risk into the user's
chosen planning system. Confirm that the plan fits the calendar before creating
or moving events.


---
name: review-your-day
description: Run a short end-of-day reflection on what happened, what mattered, and what should change tomorrow.
---

# Review your day

Use this at the end of the day before planning tomorrow.

## 1. Reconstruct the day

Read the plan, calendar, completed work, and any notes the user has chosen to
record. Ask what actually happened rather than assuming that calendar blocks
were completed.

## 2. Reflect briefly

Ask one question at a time:

1. What shipped compared with the plan?
2. What was the main win?
3. What drained energy or created friction?
4. What needs to be carried, delegated, or dropped?

If the most important outcome did not ship, ask what felt productive but did
not move it. Name the pattern without moralizing.

## 3. Extract learning

Distinguish a one-off disruption from a repeated problem. Look for a change to
the environment, task definition, timing, or commitment level that could make
tomorrow easier.

## 4. Record accurately

Write a concise journal entry in the user's chosen system. Preserve the user's
words and do not invent an emotional interpretation. If the system uses a
rating, ask the user rather than inferring it.

## 5. Close

End with the one fact tomorrow's plan should account for. Do not turn the review
into a full planning session unless the user asks to continue.


---
name: plan-your-week
description: Review the previous week, choose a few outcomes, cut lower-value work, and protect time for what matters.
---

# Plan your week

Use this to review the last week and commit to the next one.

## 1. Gather the week

Read the previous plan, current goals, calendar, overdue tasks, important
messages, and any personal commitments the user includes. Check that sources are
current before relying on them.

## 2. Review the previous week

Ask what shipped, what rolled over, and what the week taught the user about
capacity. Treat unfinished goals separately:

- Roll over when the goal still matters and has a credible path.
- Demote when it matters but does not deserve a weekly commitment.
- Drop when keeping it active creates noise without action.

## 3. Choose a few outcomes

Select one to three results that can be judged at the end of the week. If the
calendar is dominated by meetings, logistics, or care for other people, plan a
week that reflects that reality rather than pretending it is a writing retreat.

## 4. Cut work

Identify meetings, tasks, and projects that do not serve the chosen outcomes.
For long-deferred tasks, consider moving them out of the active backlog rather
than assigning another false deadline.

## 5. Pre-mortem

Ask what will most likely displace each outcome. Add one prevention or recovery
step. State what the user is deliberately deprioritizing.

## 6. Break down and schedule

Turn each outcome into clear tasks. Propose focused blocks around fixed
commitments, then recheck the live calendar before writing events. Do not create
tasks whose shape depends on an unresolved decision.

## 7. Record the commitment

Write the outcomes, rollover decisions, protected blocks, risks, and cuts into
the user's planning system. Keep the final plan short enough to guide the week.


---
name: review-and-plan-a-month
description: Close one month honestly, then create a small, capacity-checked, explicitly approved plan for the next month using evidence, trade-offs, and concrete commitments.
---

# Review and plan a month

Use this workflow at a month boundary to review the month ending and build an executable plan for the month ahead. A complete session usually takes 45–75 minutes: roughly half for evidence and review, and roughly half for planning.

Review and planning belong in the same session. The structural cause of a missed commitment, delivery problem, or energy drain should directly shape the structure of the next plan.

## Purpose

This workflow produces:

- An evidence-based account of what happened during the review month.
- A direct verdict on progress toward active long-range goals.
- A month-level picture of selected delivery, wellbeing, training, or personal-practice signals.
- A written **Review** for the month ending.
- A written **Plan** for the month beginning, with a memorable theme, no more than three major outcomes, explicit trade-offs, and a pre-mortem.

Only gather, discuss, or save information that supports these outputs. Do not turn a monthly review into general surveillance, an assessment of other people, or a transcript of private material.

## When to run it

Run this workflow when the user asks for a monthly review, asks to plan a named month, or asks to close one month and start another.

Default timing:

- On the first three days of a month, review the prior month and plan the current month.
- Otherwise, review the current month to date and plan the next month. Clearly label a partial-month review and state the days remaining.
- If the user asks only for forward planning, review first because the evidence should shape the plan. The user may explicitly choose to skip the review.

State the ranges before proceeding:

> Reviewing **[Month YYYY]** ([DD MMM]–[DD MMM]). Planning **[Month YYYY]**.

Ask whether the user means calendar months or a practical planning range that includes an overlapping partial week. Record the actual planning range in the finished plan.

## Privacy, authorization, and access boundaries

Apply these rules whenever the workflow may access calendars, journals, health data, private messages, records about other people, or shared work systems.

1. **Establish a legitimate purpose.** A source must be necessary for the review or plan. For example, calendar availability can establish capacity; a training log can assess an agreed practice commitment; a project tracker can establish delivery state.
2. **Confirm authorization.** Use a source only when the user has clearly authorized access and the assistant has the necessary permission. For shared records or information about other people, confirm that the intended use is authorized and consistent with the expected use of that source. Technical access alone is not enough.
3. **Use the minimum necessary scope.** Limit reads to the requested date range, relevant fields, and information needed for the stated purpose. Prefer dates, status, availability, counts, and aggregated patterns over message bodies, detailed health records, or personal notes.
4. **Handle sensitive information carefully.** Health, sleep, journal, relationship, financial, location, and private-communication information may be sensitive. Do not quote, copy, or save sensitive details unless necessary to the plan and specifically requested by the user. Prefer high-level summaries.
5. **Respect consent and expectations.** Do not use private communications to evaluate another person, infer personal traits, or expose information that participants would not reasonably expect to appear in a monthly plan. If consent, relevance, or expected access is unclear, exclude the material and ask for clarification.
6. **Keep outputs within the right boundary.** Save the review and plan only where the intended audience may appropriately access the included content. A personal observation belongs in a private record, while a shared plan should contain only delivery constraints and commitments needed by authorized readers.
7. **Limit delegated work.** Any helper used to summarize a large source must receive a purpose-limited brief and return only a concise summary. It must omit unrelated sensitive information, private text, and identifying details about third parties unless essential to an agreed commitment.

If these conditions are not met, use a user-provided summary or proceed without that source. Never imply that an unavailable, unauthorized, or excluded source was reviewed.

## Operating rules

1. **Read first; discuss second.** Show the evidence picture before asking reflective questions.
2. **Batch independent reads.** Gather independent evidence in one initial pass where possible. Do not interrupt the conversation with repeated small lookups.
3. **Use current commitments.** Assess progress against the user’s live target, not an old schedule, obsolete scope, or stale goal record.
4. **Check data quality before a harsh verdict.** Missing syncs, delayed entries, incomplete logs, and inconsistent sources can distort conclusions. Ask the user to confirm surprising findings.
5. **The user chooses.** The assistant calculates, summarizes, identifies constraints, and asks hard questions. The user chooses priorities, cuts, and commitments.
6. **One decision at a time.** Do not move to the next planning decision until the current question has a real answer.
7. **Stay at month altitude.** Define outcomes, milestones, capacity, structure, and commitments. Leave detailed weekly task blocks to a weekly planning workflow.
8. **No saved plan without explicit approval.** A plan assembled from notes is a draft, not a decision. The user must restate or materially confirm the theme and commitments, then explicitly approve it.
9. **Use explicit dates.** Use **DD MMM** format unless the user prefers another unambiguous convention.
10. **Keep records useful, not exhaustive.** Save decisions, evidence, constraints, and commitments rather than a meeting transcript.
11. **Do not lecture.** For training, health, recovery, or specialist practice, present relevant numbers, a direct conclusion, and the agreed commitment. Provide specialist advice only when asked and appropriate.

## Step 1: Determine the range and gather evidence

Determine the review month, prior comparison month, and planning month. Then make one initial batch of reads where possible.

Use the user’s chosen system: a task manager, project tracker, calendar, spreadsheet, notes application, health tracker, training log, or user-supplied facts. If no source is connected, ask for a short factual inventory. Never imply that unavailable data was checked.

Before reading a sensitive or shared source, state its purpose and scope when that is not already clear. For example: “I will use only next month’s availability to estimate capacity and will summarize commitments without private event details.”

| Evidence area | Gather in the initial pass |
|---|---|
| Previous monthly record | Theme, promised outcomes, commitments, and prior review findings |
| Weekly records | Plans and reviews in the review range; repeated blockers, milestones, and carried work |
| Goals | Active weekly, monthly, quarterly, and annual goals; status, deadlines, and notes |
| Work delivered | Completed tasks, decisions, projects, or deliverables; grouped into useful domains |
| Calendar | Leave, travel, fixed deadlines, recurring commitments, and heavy meeting weeks |
| Daily signals | User-selected ratings, focus time, habits, or high-level journal themes |
| Sleep and recovery | Optional sleep duration, sleep quality, and same-source recovery trends |
| Training or practice | Optional sessions from the review and prior months, plus the live commitment or schedule |

For large sources, return computed statistics and a few representative themes rather than raw entries. Long journals and month-long event lists can crowd out the actual review. Use filtered queries, aggregation, summaries, or an authorized helper when available.

A calendar summary should include:

- Fixed multi-day blocks, such as leave, travel, or events.
- Approximate meeting load by week.
- Important recurring commitments.
- Protected personal commitments only at the level needed for planning.
- Planning anomalies, such as commitments during unavailable periods or likely time-zone errors.

Before detailed monthly planning, re-read any weekly plans that overlap the beginning of the planning range. A weekly plan may already define that period in more detail. Reference and reconcile it with monthly outcomes; never duplicate or overwrite it.

## Step 2: Show the evidence picture

Present a compact factual picture before asking the user to explain it. Be direct, numeric where useful, and concise.

### Training, health, or personal-practice verdict

If the user has a current commitment in this area, include this section unless they explicitly put it out of scope. Compare actual activity with the live target. Depending on the domain, calculate:

- Total volume, sessions, repetitions, or practice instances.
- Average weekly volume.
- Number of active days.
- Completion of key sessions or milestones.
- Longest gap between sessions.
- Relevant balance measures, such as easier versus demanding work, when records support them.
- Relevant performance or recovery measures.
- Month-over-month changes.

Use this verdict taxonomy when it fits:

- **ON TRACK**: key measures meet at least 90% of target and consistency is intact.
- **BEHIND**: a key measure is about 60–90% of target, or there was a meaningful consistency break.
- **OFF TRACK**: a key measure is below 60% of target or there was a prolonged gap.
- **AT RISK**: injury, safety, burnout, or sustained decline makes the plan unsafe or unlikely.

Adjust thresholds only when the domain needs different measures, and state the adjustment. If tracking may be incomplete, ask: “The record shows this. Does that match reality?” before making a strong judgment.

State one biggest corrective action for the next month. This is a concrete commitment, not a full program.

### Goals and delivery

Summarize weekly commitments as completed, missed, deferred, or rolled forward. For every active long-range goal, state whether it **advanced**, **stalled**, or **regressed**, with one short reason. Explicitly name goals that received no meaningful attention; these are often most at risk.

Also summarize completed work in a few useful domains. Avoid a wall of bullets. The question is whether effort created intended progress.

### Life signals

Include only measures the user chooses to track. Useful measures include rating distribution and average, focus hours, low-focus days, sleep duration, sleep quality, recovery trends from a consistent source, and repeated themes in written notes.

Flag meaningful patterns, such as low average sleep, repeated short nights, several consecutive low-rating days, an extended low-focus streak, or an apparent mismatch between positive ratings and written notes describing exhaustion or stress. Numerical averages are not complete truth. Raise the mismatch directly and briefly, without quoting or retaining sensitive journal text unless necessary and authorized.

## Step 3: Reflect on the month

Start with one specific observation from the evidence. Ask one question at a time and pursue no more than two or three threads unless the user wants depth.

Cover these questions before closing the review:

1. What genuinely shipped and feels like a win?
2. What cost more time or energy than it returned?
3. Was the main miss structural, circumstantial, or a genuine priority change?
4. What one behavior, boundary, or pattern must change next month?
5. If training or a personal practice is in scope, what is the concrete next-month commitment?

Useful prompts include:

- “This outcome slipped in several weeks. What made it structurally hard to complete?”
- “Your ratings were stable, but your notes repeatedly mention strain. What was happening?”
- “This goal moved while the others did not. What conditions made that possible?”

For a time-constrained user, the minimum viable review is the in-scope personal-practice verdict, any material wellbeing flags, one structural fix, and one concrete next-month commitment.

## Step 4: Plan the new month

A plan is not a description of events plus optimistic targets. A real plan has a defined outcome, an honest baseline, a path, proof of capacity, trade-offs, forcing functions, a pre-mortem, and explicit approval.

### Move 1: Define outcomes

For each candidate priority, ask:

> What specifically is true by the final day of this planning range?

Make the answer measurable or plainly verifiable. Limit the plan to three outcomes; one or two is usually better. Each outcome should connect to a long-range goal or an explicitly chosen responsibility.

### Move 2: Establish current state

Size the gap with evidence, not mood. Inspect the relevant draft, pipeline, milestone, backlog, baseline metric, or other domain-specific reality. If the gap cannot be described, gather the missing evidence before designing the path. For shared systems, collect only role-relevant operational facts, not unrelated personal details about collaborators.

### Move 3: Work backward to build a path

For each outcome, identify three to six moves by reasoning backward from the due date. Every move needs a date or window, an owner, and evidence of completion.

Ask:

> For this to be true by the end date, what must be true halfway through? What must happen before that?

### Move 4: Do capacity math

Estimate usable focused capacity honestly:

> available working days × recently observed focused hours per day

Account for leave, travel, meeting-heavy weeks, and fixed commitments. Compare available capacity with the effort implied by the paths. If demand exceeds supply, cut, defer, reduce scope, or add real help now.

### Move 5: Make the NOT-doing list

Ask:

> What will explicitly not happen this month so these outcomes can?

The user names the cuts. A plan without a real not-doing list is a wish.

### Move 6: Add forcing functions and protective structure

Fragile outcomes need external pressure: an authorized stakeholder expecting a deliverable on a date, a booked review, a public commitment, or a downstream owner waiting on the work.

Also protect work that is vulnerable to interruption. If one outcome requires long uninterrupted work while another can tolerate fragmentation, batch the flexible work around meetings and reserve the best available blocks for the fragile work. If calendar conflicts undermine protected time, add their removal to the plan as an immediate action.

### Move 7: Run a pre-mortem

Ask:

> It is the final day of the month and this plan failed. What happened?

The user answers first. Record the top two or three failure modes and a specific counter for each.

### Move 8: Get sign-off

Read the full plan back in ten lines or fewer. The user must be able to state the theme and main outcomes from memory, then explicitly approve it.

Ask:

> Is this the plan?

If approval is vague, revise. Do not save yet.

## Required plan structure

```markdown
## THEME: [MEMORABLE, ACTION-ORIENTED LINE]

**Planning range:** [DD MMM–DD MMM].

## Shape of the month
[Leave, travel, fixed events, heavy weeks, effective working weeks, and immediate post-month constraints.]

## Outcomes
1. **[Outcome]** — Done by [DD MMM] when [binary test of done].
   - Current state: [honest gap].
   - Path: [dated milestones, owners, and completion evidence].
   - Forcing function: [external commitment].

## Capacity check
[Available capacity] versus [committed demand]; [scope decision].

## NOT doing
- [Explicit cut or deferral.]

## Structure
[The behavior, boundary, or environment change that counters last month’s drain; include delegated-but-tracked work and owners.]

## Personal or training commitment
[Specific measurable commitment, if in scope.]

## Pre-mortem
- Failure mode: [likely cause]. Counter: [specific response.]
```

Keep the plan suitable for its destination. For a shared record, remove private health, journal, relationship, or personal-calendar detail and retain only the constraints and commitments required for the authorized audience.

## Step 5: Save the review and plan

After explicit sign-off, write two records in the user’s chosen system:

1. A **Review** attached to the ending month.
2. A **Plan** attached to the new month.

Create a missing monthly record if the system supports it. Use one final write operation when possible. Before overwriting an existing plan, show it to the user and resolve the conflict.

Confirm that the destination and audience are appropriate before saving. If the review includes sensitive personal material but the plan destination is shared, either create a private review, redact the sensitive material, or ask the user to choose a suitable location.

Use this review template:

```markdown
## Training, health, or personal-practice verdict
**[ON TRACK / BEHIND / OFF TRACK / AT RISK / NOT IN SCOPE]**

- Actual: [key measures].
- Target: [current agreed target].
- Consistency: [relevant pattern or gap].
- Change from prior month: [key delta].
- Verdict: [one direct sentence].
- **Next-month commitment:** [specific commitment].

## Goals and delivery
- Weekly commitments: [completed]/[total] ([percent]%).
- Long-range goal movement: [goal and status].
- Work delivered: [concise grouped summary].

## Life signals
- Ratings: [chosen measures].
- Focus: [chosen measures].
- Sleep/recovery: [chosen measures].
- Flags: [none or named patterns].

## Win
[One meaningful result.]

## Drain
[One thing that cost more than it returned.]

## Structural fix for next month
[One named behavior, boundary, or system change.]
```

Confirm the save in one line and stop.

## Step 6: Improve the workflow

At the end of every run, make one precise improvement to the reusable workflow, its templates, or its data mapping. Store it in the user’s chosen workflow document or improvement log, using an access boundary appropriate to the content. If no suitable location exists, present the proposed edit as a short durable rule the user can save where they prefer.

Look for a read that was noisy, a wrong data assumption, a misleading metric, a question the user corrected, or a repeatable pattern future sessions should know. Prefer one specific edit over a vague reminder. Do not preserve private facts or identifying details in the improvement; convert the lesson into a general rule.

## Audit checks

Before finishing, verify:

- Review and planning ranges are explicit.
- Evidence was shown before reflective prompts.
- Each private, sensitive, or shared source had a legitimate planning purpose and clear authorization.
- Data collection was limited to the requested range and minimum relevant fields.
- Strong verdicts account for known data-quality limits.
- The plan has a named theme and no more than three outcomes.
- Each outcome has a test of done, date, path, owner, and forcing function.
- Capacity demand fits supply, or an explicit scope decision was made.
- The NOT-doing list contains genuine cuts.
- The structural fix responds to a reviewed drain.
- Overlapping weekly plans were checked and reconciled.
- Personal or training commitments are specific when in scope.
- The pre-mortem contains counters.
- The user explicitly approved the plan before it was saved.
- Saved summaries omit unrelated sensitive details and are stored only where the intended audience is authorized to access them.

## Common failure modes

- Starting with prompts instead of evidence.
- Judging against stale targets.
- Confusing a list of events with a plan.
- Overloading capacity and refusing to cut scope.
- Letting the assistant choose priorities.
- Saving an unapproved draft.
- Duplicating or conflicting with weekly plans.
- Treating wellbeing averages as more truthful than repeated written evidence.
- Applying generic productivity rituals instead of fixing the actual drain.
- Overwriting an existing record without resolving the difference.
- Treating a voice note, brainstorm, or imported task list as a confirmed commitment.
- Treating technical access as authorization to inspect private or shared records.
- Reading or preserving more personal information than the review requires.
- Saving private observations into a shared workspace or giving a summary to an audience outside the agreed access boundary.


---
name: get-unstuck
description: Work out why you are stuck, then use a short intervention suited to tiredness, dread, confusion, or distraction.
---

# Get unstuck

Use this when the user says they are tired, avoiding work, distracted, dreading
a task, or unable to begin.

## 1. Diagnose before coaching

Ask one short question at a time. Distinguish among:

- **Physical:** tired, hungry, uncomfortable, or overstimulated.
- **Dread:** the task carries conflict, judgment, or emotional cost.
- **Unclear:** the next action or standard is vague.
- **Distracted:** the environment keeps offering easier rewards.

More than one can be true. Do not treat an exhausted person as if they only need
discipline.

## 2. Choose a short intervention

Match the response to the diagnosis:

- Physical: food, water, movement, rest, or a smaller task.
- Dread: name the feared outcome and reduce the social or emotional exposure.
- Unclear: define the next visible action and a deliberately rough first pass.
- Distracted: change the environment and remove the competing cue.

Keep the intervention short. The aim is to begin useful motion, not hold a long
coaching conversation.

## 3. Start together

Ask the user to take one action that lasts only a few minutes. When useful,
write the opening line, checklist, or tiny plan with them. Confirm what “started”
means.

## 4. Learn from the result

After the attempt, ask what helped. Record patterns only with the user's
permission. Adapt future interventions to observed results rather than assuming
one motivational style always works.


---
name: wind-down-for-sleep
description: A quiet, interactive evening workflow that reduces stimulation, secures distractions, prepares essential morning needs offline, and provides a brief stimulus-control response when sleep does not come.
---

# Wind down for sleep

Use this workflow as the final part of an evening routine. Its purpose is not to review the day, solve problems, or build tomorrow’s plan. Its purpose is to make the transition from awake-day to sleep predictable: reduce stimulation, remove common distractions, complete a few practical tasks, and go to bed.

Use the full ritual when the user says they are winding down, ready for bed, or wants help settling for sleep. If the user says they cannot sleep, are still awake, or are frustrated in bed after trying to sleep, use only the **Can’t-sleep fallback**. Do not restart the full ritual.

A separate daily-review practice and next-day planning practice should happen earlier in the evening. This workflow assumes those practices exist but does not require a particular app, database, calendar, or device.

## Purpose and design rules

Every step should serve at least one of these functions:

1. **Reduce stimulation.** Lower bright light, screen use, active conversation, and problem-solving.
2. **Increase reliability.** Make it harder to drift into scrolling, work, or new decisions.
3. **Prepare the body and morning.** Complete small practical actions that reduce avoidable friction after waking.

Consistency matters more than complexity. Use a similar sequence on most nights. Keep the active ritual short enough that it does not become another task to avoid.

## Interaction rules

- Be quiet, direct, and low-stimulation. Use short prompts with no coaching language, jokes, emojis, or sleep-science lecture.
- Give one small group of actions at a time. Do not turn the ritual into a long conversation.
- For checklists, use plain bullet lists rather than interactive checkboxes. End each list with: **Reply “done” when all set.**
- Do not ask the user about tomorrow after the wind-down has started. Do not ask for priorities, intentions, goals, wins, or backup to-do lists.
- Do not reopen journaling, reflection, planning, messages, task systems, or calendars during the ritual.
- If the user raises a work problem, worry, or task, do not solve it. Say: **“Put a brief note somewhere safe for tomorrow. Do not work on it tonight.”**
- If the user is clearly exhausted, let them skip optional preparation steps. Do not skip the environment and distraction-control gate unless a safety, health, accessibility, or caregiving need makes it unsuitable.
- After the final close message, stop. Do not summarize what was completed, offer more help, create a follow-up prompt, or simulate another turn.

## Readiness check

Before beginning, establish only what is needed. Do not inspect messages, news, social feeds, task lists, or other attention-grabbing sources.

1. Check whether the user already completed their normal day review, if that information is available from the current session or a user-approved system.
2. If the review was missed, decide whether there is still enough room in the evening for the user’s normal brief review without delaying sleep.
3. Optionally check the next morning’s first fixed commitment, but only if the user has authorized calendar access and it is needed to choose practical access to a locked device.
4. Treat next-day planning status as silent information. If planning was missed, do not mention it, offer planning, or ask a substitute planning question.

If the day review was completed, say:

> Day closed. Starting wind-down.

If the review was missed but there is still enough room for it, offer it once:

> The day review was missed. Do you want to do the short review first?

If the user declines, or it is too late for a useful review, say:

> Leave the review for tomorrow. Start winding down now.

Then continue. If a review was skipped, any later bedtime note should go into a designated next-day capture location rather than creating a partial or empty journal record.

## Step 1: Environment and distraction gate

This is the load-bearing step. Do not continue until the user confirms it is complete.

Choose a simple set of cues that the user can repeat. A broadly useful default is:

> Before we start:
>
> - Change out of day clothes into sleep clothes.
> - Put on preferred low-light glasses, if used, or otherwise reduce bright light.
> - Turn off overhead lights; use dim, warm light only if needed.
> - Start quiet, familiar audio if it helps without demanding attention.
> - Put the phone in a charger outside reach or in a physical barrier that prevents casual checking.
> - Set the phone’s return or unlock point for the morning.
> - Keep any remaining device use limited to one necessary, low-stimulation device.
>
> Reply “done” when all set.

### Set device return access

Let the user choose a normal morning access point. If an early fixed commitment requires it, make access available earlier only when necessary for preparation, travel, communication, or safety. State the choice and reason briefly.

Example:

> Phone access returns before the first morning commitment so you can prepare and travel.

A physical barrier is often more reliable than a software restriction alone. The aim is not punishment. It is to prevent automatic late-night or early-morning scrolling.

If the user says they will change the lights or secure the phone later, respond once:

> Do it now. This is the highest-leverage step. I’ll wait.

Do not negotiate the rest of the routine while this gate remains incomplete.

## Step 2: Offline morning card

Offer a small physical morning card. Its role is to make the first part of the day independent from a phone, notifications, and memory.

Prompt:

> Write a small morning card. Keep it short enough to read at a glance. A useful template is:
>
> 1. Hygiene
> 2. Medication or supplements, if applicable
> 3. Water and breakfast
> 4. Movement, rehabilitation, or another health practice
> 5. Shower and get dressed
> 6. Leave for the day or begin the first planned block
>
> Add only a practical exception that matters tomorrow. Is anything different?

If the user names a change, tell them to write it in the appropriate place on the card. Do not make a digital card for them and do not turn this into planning.

Then ask:

> Card done?

This step is optional if the user is too tired or already has a dependable offline morning cue.

## Step 3: Physical preparation

Give a compact list tailored to the user’s normal needs. Group tasks by location to minimize movement and decisions. A default list is:

> - Fill water for the morning.
> - Brush teeth and complete essential nighttime hygiene.
> - Prepare a simple breakfast or place needed items together.
> - Put out required clothing, keys, mobility aids, or medication.
>
> Reply “done” when all set.

If a small missing item creates a worry, capture it in one designated location without solving it. For example: “Buy breakfast item.” Do not search for alternatives, open shopping tools, message someone, or start a planning conversation. Say only:

> Noted. Captured for later.

## Step 4: Brief settling practice

Offer one familiar, low-stimulation practice. Do not teach a new or complex exercise at bedtime.

Default prompt:

> Brief quiet meditation.

If meditation is not suitable, use an already accepted alternative such as gentle breathing, a short body scan, quiet stretching, or a few pages of a paper book outside bed. Avoid screen-based guided content and anything emotionally engaging or performance-focused.

Wait for a simple completion response.

## Step 5: Close

After the settling practice, send only:

> Close the device. Go straight to bed—no detour.
>
> See you tomorrow.

This is the final user-facing message. If the user says good night, remain silent or reply only: **Good night.**

## Can’t-sleep fallback

Use this only when the user reports being awake after attempting sleep.

Do not rerun the ritual. Do not reopen reflection, journaling, planning, device settings, or problem-solving. Respond briefly:

> Get out of bed. Keep the room dim and do a boring, screen-free activity until sleepy. Return to bed when sleepy. Do not check the time.

Suitable activities include reading on paper, folding laundry slowly, or another neutral task. Avoid work, emotionally engaging reading, exercise, food preparation, screens, and clock-checking. The goal is to keep the bed associated with sleep rather than wakeful frustration.

For recurring, severe, or safety-relevant sleep difficulty, encourage appropriate medical or sleep-care support.

## Routine audit and adaptation

Review the workflow after a run only if doing so will not re-engage the user at bedtime. Make changes based on observable friction, not novelty. Do not invent improvements after a clean run.

| Signal | Adaptation |
|---|---|
| The user repeatedly misunderstands a prompt | Rewrite it in plainer language or remove ambiguity. |
| A distraction barrier is routinely bypassed | Choose a stronger physical, account-level, or environmental barrier with the user. |
| A checklist item is consistently skipped and adds no value | Remove it or make it optional. |
| A practical issue repeatedly appears at bedtime | Move its prevention into an earlier review or planning practice. |
| A step makes the user more alert | Shorten it, simplify it, or move it earlier in the evening. |

Preserve what reliably works. The best wind-down is usually quiet, repeatable, and boring enough to become an automatic signal that the day is over.


---
name: plan-and-book-a-trip
description: Plan a trip around its purpose, compare complete journeys and current fares, and prepare or complete a booking within the user's authorization.
---

# Plan and book a trip

Understand the trip before optimizing its transport. Establish what the traveler wants, compare a small set of complete journeys, and carry the chosen option through preparation or authorized booking. Treat the user's current instructions as authoritative. Previous trips provide context, not permanent rules.

## 1. Understand the trip

Start with a focused discovery pass. For a continuing conversation, reuse the established brief and ask what changed. Follow a request to skip discovery or check one specific fare without forcing a new interview.

Read the supplied invitation, itinerary, article, event agenda, or other relevant material. With permission, consult calendars, travel correspondence, and existing reservations for this trip. Use only the minimum relevant sources and information for the legitimate planning purpose. Access to an account does not authorize unrelated searches or investigation of companions. Exclude unrelated or sensitive personal details, respect consent and privacy expectations, and keep findings within the approved private planning space. Do not contact anyone without authorization.

Look for the trip's purpose, venues, possible dates, companions, accommodation, existing bookings, and commitments immediately before and after travel. Distinguish an invitation from confirmed attendance, a provisional calendar entry from a hard deadline, and an old receipt from a current preference. Resolve conflicts where possible and label remaining uncertainty.

Retrieve accessible facts yourself. Ask the traveler about intentions and trade-offs, rather than asking them to copy information already available in an authorized source. Keep the initial research short enough for the traveler to shape the trip before detailed shopping begins.

### Ask questions that shape the journey

Briefly state what is known, then ask a compact group of relevant questions. Four to six often works for an open-ended trip; use fewer when the answers are already clear.

- **Purpose:** What would make this trip worthwhile? Which events, visits, or activities matter most?
- **People and places:** Who is traveling or being visited? Which stops are essential, optional, or best visited in a particular order?
- **Time:** How long would the traveler like in each place? What fixes departure, arrival, and return? If dates are flexible, what range is useful?
- **Pace:** Is the trip for work, leisure, or both? Is recovery time or arriving rested important? Are quiet workdays or unstructured days needed?
- **Practical constraints:** What accommodation and local transport already exist? Are there accessibility, spending, or reimbursement constraints?
- **Scope:** Is the requested outcome research, booking preparation, or an authorized purchase?

Wait for answers to choices that materially affect the trip before searching tickets. Continue independent context gathering while waiting. Do not impose a numerical budget when the user wants to understand trade-offs first.

### Establish preferences and agree the brief

Ask only about preferences that remain unknown and matter to the options. These can include direct versus connecting services, cabin comfort, overnight sleeping needs, seats, luggage, rail class, loyalty benefits, and flexibility. Treat each as the traveler's choice. Do not assume an airline, seat, airport, or premium cabin is universally preferable.

Summarize the purpose, people, stops, time in each place, fixed dates, flexible ranges, work and recovery needs, accommodation, and unresolved points. Give the traveler an opportunity to correct the summary. Clear answers can establish agreement without a separate approval ceremony. Keep provisional dates visibly provisional.

## 2. Research current transport

Search useful dates and routes against the agreed brief. If available transport would substantially change the trip, return to the traveler with that choice.

Use current schedules and fares. Search aggregators can reveal routes and date differences, but verify the selected itinerary, operating carrier, fare family, and conditions with the provider when possible. A marketing carrier's name does not establish who operates the service.

If a tool or provider fails, attempt permitted safe recovery. Name the failed source, report the exact error, and explain which facts remain missing or unverified. Disclose any switch of source and the resulting verification limits. Do not imply a blocked checkout or inaccessible personal offer was checked.

Compare useful combinations: return tickets, arriving and departing through different cities, nearby airports, rail, and ground transfers. Consider accommodation, cross-city travel, and lost usable time when judging a cheaper fare. Explain any connection or airport change before treating it as acceptable.

Check transport to the actual destination. An airport arrival may leave a long onward journey. Verify the intended station when names are ambiguous. Check timetable-release limits, holiday disruption, and planned engineering work; do not invent a precise service or price before it is available.

Label each quote as a selected live itinerary, an indicative date-grid price, or an estimate. Record when it was checked, the currency, and what it includes. An advertised starting price is not proof that the required ticket can be bought. Use verified links for options and terms.

### Compare the actual product

Use the comfort levels relevant to the traveler. When comparing premium economy, verify that it is a distinct cabin rather than an extra-legroom economy seat. For overnight journeys where sleep matters, compare confirmed sleeping arrangements and verify the actual aircraft or train product. A service label alone does not guarantee a lie-flat seat or the expected facilities.

Inspect every segment of a mixed-cabin itinerary. A higher cabin on an overnight leg and a lower cabin on a daytime return may suit the trip better than upgrading everything. For rail, confirm the named class and fare conditions rather than trusting a reseller's generic class label.

Include required seat selection and luggage in the price. Check availability of the preferred seat, any selection fee, and whether assignment is confirmed. Verify the fare's cabin-bag allowance and size or weight restrictions. A personal-item allowance may not cover the traveler's bag. Included services have value only when the traveler needs them.

### Evaluate upgrades carefully

When upgrades are relevant, compare buying the desired cabin outright, changing a ticket by paying the fare difference, and purchasing a separate upgrade. Before booking, compare total costs; afterward, compare additional costs and conditions. Do not assume a previous upgrade payment carries forward to another change.

Separate confirmed seats from award or loyalty waitlists. An empty seat map is not proof that an upgrade can clear. If sleep or comfort is essential, recommend a confirmed acceptable option. Buy a lower cabin only if the traveler would be content flying it.

Verify fare-family eligibility, current loyalty benefits, waitlist rules, and any restrictions before buying a ticket as an upgrade strategy. Do not claim that a particular point before departure is reliably cheapest. Prices can rise, cabins can sell out, and preferred seats can disappear.

Compare cash with points and any copayment using a stated valuation assumption. Read the specific upgrade's change, cancellation, refund, and unsuccessful-waitlist terms. A flexible ticket does not necessarily make an upgrade refundable.

For an existing reservation, inspect personal upgrade offers and alternative ticket-change prices when authenticated access is available and authorized. Public fares do not establish a reservation-specific offer. If login or unavailable tools prevent a check, attempt permitted recovery, identify what remains unverified, and request only the user action needed to proceed. Continue independent comparisons.

## 3. Compare complete journeys

Give two or three useful options with a recommendation. If only one route meets the brief, explain that rather than inventing alternatives.

Show local departure and arrival dates and times, airport or station names, total journey duration, and overnight date changes. Include realistic buffers for immigration, luggage, station check-in, and travel between terminals or across a city. Verify the provider's current arrival guidance and allow practical contingency.

Distinguish protected connections from independently booked tickets. Explain who bears the risk if the first service is late. Consider a longer connection or overnight stay when appropriate, accounting for accommodation already available.

Use a compact comparison such as:

| Option | Dates and route | Cabin and fare | Complete cost | Main benefit | Main drawback |
|---|---|---|---|---|---|
| [Option] | [Local dates, route, duration] | [Actual product on each segment] | [Currency, tickets, required extras and transfers] | [Time, comfort or flexibility gained] | [Restriction, effort or uncertainty] |

Explain what extra spending buys. List material change and refund restrictions, luggage, seat fees, and ground transport. Show different currencies separately or clearly label the conversion assumption. Do not add unlike currencies into one unexplained total.

## 4. Prepare and complete the booking

Lead with the recommended dates and route, the comparison, verified booking links, the quote-check time, unresolved facts, and the decision needed. Keep personal identity and reservation information out of a shareable summary unless required for its purpose.

Prepare a concrete, reviewable booking before requesting any necessary purchase approval. A request to compare travel does not authorize payment. If the user has already authorized the specific purchase or an adequate scope and price ceiling, continue within that authorization without repeatedly asking. A material mismatch needs resolution before checkout.

Verify the passenger name against the traveler's supplied identity details; never invent missing information. Check dates, airports or stations, operating provider, routing, class on each segment, fare family, seats, luggage, total price, and terms against the chosen option. Keep payment and identity documents within the authorized booking process.

After purchase, verify a provider confirmation. Report the booked journey and total, any unassigned seat, and remaining transport arrangements. A selected fare or partially completed checkout is not a booking. Keep references and receipts in a private trip record rather than the reusable skill.

## 5. Monitor and learn when requested

If the plan includes recurring fare or upgrade checks, establish a real schedule with an available authorized automation facility. Verify that it can access the reservation and report useful changes before describing monitoring as active. Track additional cost, cabin, seat availability, conditions, and check time. Notify the traveler when a decision is useful; monitoring does not authorize a purchase.

Stop monitoring after departure, a completed upgrade, or a changed plan. If scheduling or authentication is unavailable, state that monitoring is not running. Never promise ongoing checks without an execution mechanism.

During active use, apply corrections immediately. When authorized to remember preferences, save clear lasting choices with their qualifications and replace superseded defaults. Keep current fares, event dates, one-off exceptions, and tentative preferences in the trip record. Ask whether a choice applies to this trip or future trips only when that distinction is unclear.

Learn from verified outcomes and traveler feedback about comfort, connections, and booking friction. Successful checkout does not establish satisfaction. Preserve useful general lessons without accumulating incident histories, personal identifiers, or credentials. Learning creates no additional permission to purchase, message others, or access accounts.


---
name: prepare-for-a-meeting
description: Research the right context, clarify the user’s intended outcome, and produce a focused, access-appropriate meeting brief and agenda.
---

# Prepare for a meeting

Use this workflow to prepare one consequential meeting: a client, partner, hiring, advisory, project, negotiation, or relationship-building conversation. The completed deliverable is a usable preparation page in the user’s chosen workspace, together with a situation brief and targeted questions that shape the agenda.

Research alone is not completion. Normally, complete the workflow only after the user has seen the situation brief, answered targeted questions, and received the finished meeting page or document.

## Purpose and boundaries

The meeting preparation should give the user:

- relevant relationship, decision, and artifact context;
- a clear, user-confirmed outcome;
- a realistic agenda for the available time;
- prioritized questions and an appropriate close; and
- notes that fit the access level of the destination document.

Use private communications, records, and calendars only for a legitimate meeting-related purpose and with clear authorization. Use the minimum relevant sources and information. Omit unrelated personal details, sensitive personal information, credentials, account data, and confidential material that does not help prepare the meeting.

When the page may be visible to attendees, colleagues, or a broad workspace, write a neutral shared agenda. Do not put private tactics, candid assessments, interviewer guidance, negotiation strategy, or sensitive employment details in it. Keep private preparation in a restricted document, if needed and authorized.

Never include compensation figures, pay bands, equity, offer numbers, or similar employment terms in a broadly visible meeting page. If that context matters, refer to it generally, such as “offer follow-up” or “compensation discussion,” without figures.

## Inputs and readiness

Default to one meeting. If the user requests a full day or several meetings, prepare a separate brief and page for each meeting rather than mixing unrelated contexts.

| Input | What to establish |
|---|---|
| Meeting | [Title, date, time zone, duration, attendees, format, and location or link] |
| Purpose | [Invitation wording or the best available explanation of why the meeting exists] |
| Destination | [The user’s chosen document, workspace, notes system, or draft format] |
| Audience | [Private, restricted internal, or shared with attendees] |
| Source access | [Only authorized messages, records, files, notes, calendars, and public sources] |

If several similar events exist, identify the exact event before researching. Exclude personal blocks, focus time, and placeholders unless the user specifically wants them prepared. For group meetings, focus on decision-makers and participants central to the topic; do not research every optional observer without a reason.

## Workflow

Follow this order:

1. Read the meeting record and establish the boundary.
2. Gather relationship and decision context from the most relevant authorized sources.
3. Read the written artifact the meeting is about, if one exists.
4. Detect whether a specialized workflow is required.
5. Post a concise situation brief.
6. Ask targeted questions and wait for answers.
7. Create the meeting page using a private or shared structure.
8. Run the final audit and arrange an appropriate follow-up review when useful.

Do not jump directly from research to an agenda. Even strong research cannot establish the user’s intended outcome, authority, boundaries, preferred tone, or desired ask.

## 1. Read the meeting

Inspect the invitation or meeting record in detail. Capture:

- title and stated purpose;
- date, time zone, duration, and format;
- attendees, known roles, and organizations;
- organizer, location, conferencing details, and linked materials;
- invitation description, scheduling context, reschedule notes, and requested preparation; and
- whether the event is a real meeting rather than an internal or personal block.

Distinguish confirmed participants, optional participants, and unknown attendance where possible. Do not assume every invitee will attend.

If timing is ambiguous, ask for the date and time zone. Keep the meeting date accurate in the final document; do not accidentally turn a date-only field into a date-time field when the chosen system supports both.

## 2. Gather context responsibly

Research should answer four questions:

1. Who are the relevant participants?
2. What is the relationship history?
3. Why is this meeting happening now?
4. Which facts, decisions, and materials are likely to shape the conversation?

Start with the sources most likely to explain the immediate trigger:

1. The invitation and recent direct messages.
2. Previous meetings with the same people.
3. Relevant project notes, decision logs, and shared documents.
4. Authorized internal records directly connected to the meeting.
5. Public professional information or recent public news, when useful.

For correspondence, use two complementary searches when the tools allow it:

- **Direct correspondence:** messages sent to or received from the attendee. This establishes commitments, tone, and recent exchanges.
- **Name or organization mentions:** messages that discuss the attendee without including them. This may reveal introductions, referrals, planning threads, prior context, or the real scheduling trigger.

Read enough recent material to understand the thread; do not rely on subject lines or search snippets alone. Prefer primary sources, current decisions, and the actual relevant artifact over older summaries.

For recurring contacts, summarize the relationship arc: what was discussed, promised, decided, changed, and left unresolved. Do not merely state that a previous meeting happened.

### Identity and evidence checks

Do not merge records merely because names match. Confirm identity with appropriate professional signals such as an email address, role, employer, project context, or another reliable match. If the match is uncertain, exclude it or label it as unverified.

Treat uncertain evidence explicitly:

- Label claims supported by one source, an old source, or a weak source.
- State meaningful conflicts rather than silently choosing one account.
- Do not build a pointed question around an unverified claim without indicating uncertainty.
- Do not include gossip, subjective labels, or irrelevant personal details.

If authorized internal records are relevant, read the material directly tied to the meeting: for example, an application, project request, customer record, proposal, or assessment. Do not search broadly through personal records simply because someone is attending.

For hiring or assessment meetings, focus on role-relevant capabilities, diagnostic evidence, stated interests, work samples, and whether the assessment distinguishes relevant performance. Keep notes within the appropriate hiring access boundary.

## 3. Read the artifact the meeting is about

If a proposal, deck, draft, memo, plan, application, contract, report, or other written artifact is the reason for the call, read it before drafting the agenda.

Signals include:

- requests for feedback or comments;
- references to reviewing a draft, proposal, deck, or memo;
- linked files in the invitation or recent messages;
- document-comment notifications; or
- an explicit request to discuss a plan that likely exists in writing.

Read the complete relevant artifact, including substantive tabs, appendices, linked sections, and stated alternatives where accessible. Extract:

- the author’s request or objective;
- key assumptions and evidence;
- decisions requested;
- risks, dependencies, deadlines, and alternatives; and
- the specific choices where the user can challenge, support, or decide.

Do not ask generic questions such as “Tell me about the plan” when the plan is documented and available. Anchor questions in actual assumptions and choices. If the context implies an artifact exists but it cannot be found, ask the user for the link during the question stage instead of inventing a generic agenda.

## 4. Detect a specialized workflow

Before creating the standard page, decide whether the meeting requires a more specific approved process. Examples include a hiring reference conversation, formal interview, legal or compliance discussion, safeguarding matter, performance meeting, incident review, or regulated decision.

If a specialized workflow exists, use it and carry forward relevant research. For example, a hiring reference conversation should use role-specific evidence probes, consent-aware notes, and a distinction between direct observation and hearsay. Do not produce a generic preparation page that bypasses required safeguards.

If no specialized workflow applies, continue with this workflow.

## 5. Post a situation brief

After research is complete, post a concise situation brief before asking the user for direction. This is not an unfiltered research dump. It should allow the user to reload the situation in about a minute.

Choose the shape that fits the meeting.

### Narrative brief

Use this for most meetings:

- **Who they are:** role, organization, and relevant background.
- **Where things stand:** relationship history, commitments, and current work.
- **Why this meeting is happening:** the best-supported trigger and intended topic.
- **Live tensions:** decisions, uncertainties, or risks likely to matter in the call.

### Decision-shaped brief

Use this for negotiations, recruiting discussions, fundraising, sales, partnerships, or other live decisions:

- **The ask:** what either side appears to be seeking.
- **Timing and alternatives:** deadlines, competing routes, or decision constraints, if supported.
- **Position:** what each side seems to value or need; do not overstate certainty.
- **Risks:** likely ways the discussion could stall or go wrong.
- **Unknowns:** what the user needs to establish during the meeting.

Combine these formats when both relationship context and a live decision matter.

Explain unfamiliar names, organizations, programs, and terms where they appear. Each section should make sense on its own, because the user may scan only one part of the brief or agenda. Repeat a short explanation where necessary, or rewrite the question to avoid unnecessary names. Remove names that do not aid a decision.

Do not propose a final goal or agenda before asking what the user wants from the meeting.

## 6. Ask targeted questions

Targeted questions are normally mandatory. Ask them after the situation brief and before creating the page. They establish targets, boundaries, and meeting shape; they do not ask the user to write the agenda.

Ask at least:

- one question about the primary outcome;
- one question about a meaningful choice, such as tone, failure mode, authority, sensitivity, or desired ask; and
- one final catch-all question for missing context.

Useful axes include primary outcome, the other party’s uncertain situation, sensitive substance, failure mode to avoid, desired ask, and the user’s authority to decide or offer something in the meeting.

Give each question three or four genuinely distinct options. Make the likely recommendation the first option, but preserve real alternatives. Use compact, continuous labels so answers are quick and auditable.

```markdown
1. What is the primary outcome?
   - **1a (recommended):** Understand their priorities and agree a concrete next step.
   - **1b:** Build the relationship without making an ask.
   - **1c:** Seek a decision or commitment in this meeting.

2. How direct should the close be?
   - **2a (recommended):** Propose a date-bound follow-up with a named deliverable.
   - **2b:** Offer help and let them choose whether to continue.
   - **2c:** Keep the discussion exploratory; make no close request.

3. Is there anything else to land or avoid?
   - **3a (recommended):** Nothing to add.
   - **3b:** I will add notes or constraints.
   - **3c:** There is sensitive context; ask before using it.
```

If more than four questions are genuinely needed, use multiple rounds. Put answers that change later options first. For example, whether the user can decide in the meeting should shape the available closing options. Do not force false either-or choices when both actions could sensibly happen; include a “both” option where relevant.

Before sending questions, check that numbering is continuous, labels are unique, every option has one label, and the final round includes the catch-all. An exception is appropriate only for a clearly documented recurring meeting with no open decision where the user has already supplied the outcome and constraints. When uncertain, ask.

## 7. Create the meeting page

After the user answers, create the page in the chosen system. Include the correct title, date, attendees as appropriate, essential context, user-confirmed goal, and agenda. Verify that it is saved in the intended location and is accessible only to the intended audience.

### Private preparation page

Use this only for the user and authorized internal collaborators.

```markdown
# [Meeting title]

## Context
[Who the participants are, relationship arc, meeting trigger, and essential links.] 

## Goal
[User-confirmed outcome and decision boundary.]

## Agenda
Text under **Say** is word for word. Anything in [square brackets] is a cue, not something to say aloud.

### 0–5 min: Open and frame
**Say**

[Brief opening that sets a useful purpose.]

**Private note**

[What to establish or avoid.]

### 5–20 min: Diagnose the important issue
**Questions**

1. [Decision-relevant question]
2. [Question that tests an important assumption]

**Private note**

[Signals to listen for and how they affect the next section.]

### 20–35 min: Discuss options or pressure-test the proposal
**Say**

[Transition and key point to make.]

**Questions**

1. [Focused question tied to the artifact or decision.]

### Final minutes: Close and next step
**Question**

1. [Specific next-step question with an owner, date, or deliverable.]

**Private note**

[Fallback close if no decision is possible today.]

## Five most important questions
1. [Most decision-relevant question]
2. [Key diagnostic question]
3. [Risk or constraint]
4. [Fit, commitment, or decision question]
5. [Forcing close]

## Timely note
[Relevant recent item, or “None.”]
```

Keep spoken text natural and complete. Do not mix private instructions into words the user may say aloud. The five-question list is an in-call cheat sheet: rank the most decision-relevant questions, keep them scannable, and include a concrete forcing close when appropriate.

### Shared agenda page

Use this when other attendees, teammates, or a broad workspace can read the page. Remove private notes, scripts, persuasion tactics, candid assessments, and sensitive information. Use neutral language or “we” voice.

```markdown
# [Meeting title]

## Purpose
[Shared purpose of the meeting.]

## Context
[Context appropriate for all readers.]

## Agenda
### 0–5 min: Align on purpose and desired outcomes
- [Topic or question]

### 5–20 min: Review current context
- [Evidence or artifact to discuss]

### 20–35 min: Discuss options and decisions
- [Decision or trade-off]

### Final minutes: Agree next steps
- [Owner, deliverable, and timing]

## Decisions to leave with
1. [Decision or open question]
2. [Decision or open question]
3. [Owner and next action]
```

Make time boxes fit the actual duration. Put the most important issue before background updates. State explicitly when it is a first meeting. For ongoing relationships, summarize the arc and current decision rather than listing disconnected history.

## 8. Final audit and follow-up

Before delivering the page, check the following.

| Check | Pass condition |
|---|---|
| Meeting identity | Date, time zone, participants, duration, and destination are correct. |
| Evidence | Important claims are supported, qualified, or removed. |
| Artifact | Relevant written material was read, or its absence is stated. |
| User intent | Goal, tone, and close reflect the user’s answers. |
| Privacy | Only necessary information is included and access is appropriate. |
| Shared access | Shared pages contain no private tactics, scripts, candid internal views, or pay details. |
| References | Unfamiliar names and terms are explained or removed. |
| Agenda quality | Timing is realistic, questions are specific, and the close has an owner, date, artifact, or explicit reason not to. |

For high-stakes meetings intended to move a commitment, decision, partnership, sale, or negotiation, arrange a post-call review reminder in an authorized task or reminder system. The review should capture what happened, commitments, objections, evidence learned, owners, follow-up dates, and recurring communication patterns. Do not create hidden monitoring or access meeting transcripts without clear permission.

Finally, give the user the location or link to the completed page and state any material limitation, such as an unavailable artifact, unresolved identity match, or source conflict.


---
name: capture-meeting-actions
description: Review authorized meeting records, capture genuine unfinished commitments as clear deduplicated tasks, and batch only the judgment calls that need clarification.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date or date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a real, unfinished commitment that should be tracked.

## Purpose and operating rules

Apply these outcomes before each run:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same recipient or group on the same time horizon.
- **Multiple tasks** only when recipients, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often assign actions to the wrong attendee, especially in recurring one-to-ones, brainstorming sessions, and meetings where participants list their own to-dos. Never create a task solely because a summary labels it as an action item. Confirm ownership in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, statement of interest, or open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply responsibility boundaries supplied by the user or team. Attending a meeting does not make the user responsible for every subject discussed.

When records contain information about people, access them only for a legitimate purpose and with clear authorization. Use only the minimum relevant sources and details. Do not copy unrelated personal, sensitive, or confidential information into tasks, reports, or reusable guidance. Keep outputs within the access boundary of the selected task system and intended audience.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this broadly useful default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect:

- Title, date, and time.
- Meeting-record link or identifier.
- Attendees, only when necessary to identify follow-up ownership.
- Transcript, notes, summary, and relevant linked context.

Report a compact count before processing. Do not infer actions from a meeting title alone.

## 2. Fetch and inspect complete records

Fetch complete meeting records in parallel where the user’s selected system supports batching. Do not search for existing tasks yet: first identify the people, topics, and candidate outcomes that make deduplication accurate.

For long transcripts, use a repeatable search, extraction, or chunking method instead of relying on truncated previews. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by explicit acceptance.

Review summary action items as candidates, then verify them against the transcript and surrounding conversation. A promise may have been conditional, reassigned, fulfilled live, or directed at another attendee.

If a transcript is unavailable, lower confidence accordingly. Use written notes or related messages only when they clearly identify the owner and outcome. Ask a question rather than guessing when uncertainty could create unwanted work or outreach.

## 3. Triage each meeting

Classify the meeting loosely. Classification provides a starting expectation, not a rule that overrides evidence.

| Meeting type | Usual outcome | Guidance |
|---|---:|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or explicitly timed follow-up. |
| Information-gathering, interview, or reference call | 0 tasks | Create work only for an explicit out-of-meeting commitment. |
| Internal planning or team meeting | 0–1 user-owned task | Capture the user’s deliverable, not the full team action list. |
| Coaching or recurring one-to-one | 0–1 task | Usually create a task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1–2 tasks | Often separate an internal decision from an external response. |

For every meeting, identify:

- Relationship context and why the meeting occurred.
- Candidate actions owned by the user.
- Work completed during the meeting.
- Work delegated to another named owner.
- Explicit future commitments and timing.
- Enough neutral context for a task to remain understandable weeks later.
- Source and related links that the task audience is authorized to access.

Create no task when work was completed live, another person owns it, the meeting was purely informational and needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

A useful test for live completion: if someone promised to send, create, paste, or share something and the artifact was actually delivered during the meeting, treat it as completed. Do not create a task merely because the transcript contains the initial promise.

## 4. Decide the task shape

Combine actions into one task when they have the same recipient, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect months later.
- Different recipients need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

This is a readiness gate. Do not proceed to task creation until each proposed task has:

- A clear owner.
- An unfinished, concrete outcome.
- Transcript or reliable-note evidence supporting ownership.
- A sensible scope and finish line.
- A due-date rationale.
- Enough context to stand alone.

## 5. Write the task

Use the user’s chosen task system and field names. At minimum, capture:

- **Title:** short, verb-led, and specific, such as “Follow up with prospective partner about pilot scope.”
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user’s scale; default to important work and reserve the highest level for a real deadline, material risk, or waiting recipient.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and authorized links.

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: agreed date, or a reasonable reminder date before it.
- Weekly or sprint commitment: next relevant review or planning session.
- Flexible work: roughly one week, adjusted to workload.
- Older meetings processed late: move an immediate follow-up to the next workable date rather than assigning an already-passed date, unless the original deadline still applies.

Do not raise priority merely because capture happened late. Raise it only when an external deadline, material risk, or expected reply justifies it.

### Notes template

```markdown
[Two or three sentences of time-independent context. Include relevant absolute
dates, why this matters, the commitment, and necessary sensitivity only.]

## Actions
- [Concrete action]
- [Concrete action]

## Draft message

Subject: [Specific subject]

Hi [First name],

[Short, direct message that fulfills the commitment.]

Best,
[Sender]

## Links
- Meeting record: <link>
- Related document: <link>
```

Use time-independent wording. Prefer “In the 12 May meeting” over “Earlier today” when the task may be opened later.

Avoid unnecessary private discussion in a task system that may be broadly visible. Follow the user’s known writing preferences. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable. If the task is to send a message, write a ready-to-send draft rather than merely saying “email them.” For introductions, use double opt-in: seek permission from each relevant party before connecting them.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by meeting link or identifier, recipient, distinctive topic terms, and proposed title.

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. Skip the new task, or update the existing task if the meeting adds a meaningful action, deadline, or context. Record the duplicate decision so it can be reported clearly.

Do not include more personal data in search queries or task notes than is needed to identify existing work.

## 7. Create confident tasks

Create high-confidence tasks in a batch when possible. If the selected task system can open created records, open them there rather than filling the status update with management links.

For every skipped meeting, give a brief reason, such as:

- “No out-of-meeting commitment.”
- “Completed during the call.”
- “Owned by another role.”
- “Already covered by an active task.”

## 8. Batch uncertain questions

Skip this step entirely when all decisions are confident. Do not interrupt for each ambiguity. Create confident tasks first, then ask all remaining questions together.

Ask the smallest question that resolves ownership, scope, timing, completion status, responsibility boundary, or duplicate handling:

```markdown
**[Meeting title]**
Question: [One specific question]
Context: [One sentence grounded in the record]
Option A: [Task to create or update if true]
Option B: [Skip or alternate task shape]
```

Wait for answers before creating uncertain tasks. After answers arrive, create or update the remaining tasks and rerun any necessary duplicate check if the answer changed the task outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, capture lessons that genuinely improve future runs. Keep this separate from the meeting task itself.

- Add a short, generalized note to a user-maintained pattern guide when a recurring pattern affects triage, such as a common attribution error, a reliable sign of in-meeting completion, or a meeting-type exception.
- Update the workflow guidance only for cross-cutting principles, changed defaults, or a newly required step.
- Record a new responsibility boundary in the user’s maintained responsibility reference when it applies beyond one meeting.

Do not turn one-off facts about a person, meeting, or relationship into permanent rules. Small additions to a pattern guide can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing steps or changing the evidence order. Briefly report any reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links to its source record when appropriate for the task audience.
- Message drafts are ready to send and follow the user’s preferences.
- Sensitive or unrelated personal details were omitted.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report only the essential outcome: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and any reusable guidance changes. Keep status updates terse and factual.


---
name: turn-a-message-into-a-task
description: Turn a message thread into researched, pre-completed work, and create a clear task record only when tracking will help.
---

# Turn a message into a task

Use this workflow when one or more message links, copied conversations, or inbound requests may need follow-up. The goal is not to log a vague to-do. The goal is to complete as much useful work as is safe and authorized, then leave a small, clear human finish.

This workflow is tool-independent. Use the messaging, document, task, calendar, and research capabilities available in the user’s environment. Do not assume a particular messaging product, task database, file system, or browser.

## Operating principles

- Read the full conversation before deciding what the task is.
- Prefer a prepared deliverable over an empty task record.
- Draft external communications; do not send them without explicit authorization.
- Use the smallest relevant set of sources and the minimum personal information needed.
- Do not create records for completed, superseded, duplicated, or trivial work.
- Make uncertainty visible. Verify facts, dates, figures, and links; otherwise use clear placeholders.
- Keep access and output within the user’s legitimate purpose, authorization, and privacy boundary.
- Treat the linked message as the reason work arrived, but treat later replies as potentially decisive.

Run the full flow separately for each supplied message reference unless the references clearly concern one shared outcome.

## 1. Open the message and read the complete conversation

For every supplied message reference:

1. Open the linked message or locate the quoted message.
2. If it is a reply in a thread, open the parent and read every reply.
3. If it is a top-level message, retrieve nearby conversation context. If the message has replies, read the full thread immediately.
4. Check whether replies after the linked message change the request, answer it, reassign it, or make it obsolete.
5. Open every substantive linked attachment, form, shared document, or cited source that could contain the real request.

Identify:

- The requester and all relevant participants, using names or clear roles rather than vague references.
- The current ask, previous commitments, promises, deadlines, and dependencies.
- The current owner of each action.
- Whether work is already complete, withdrawn, delegated, or blocked.
- Whether several people have asked the same topic elsewhere and could be served by one consistent answer.

If the work appears already done, do not file dead work. Tell the user what later context suggests and ask before creating a record if status remains ambiguous.

## 2. Classify the real work

State the task shape in working notes before researching. Common shapes are:

1. **Reply owed:** Someone needs an answer, feedback, a decision, or a confirmation. Deliverable: a drafted reply.
2. **Artefact owed:** The user owes a document, introduction, analysis, reference, briefing, or data extract. Deliverable: the artefact or a substantial draft.
3. **Decision needed:** The conversation ends at a choice only the user can make. Deliverable: a concise decision brief and, where useful, a draft reply for the likely choice.
4. **Follow-up or delegation:** The user needs to chase someone, schedule something, hand off work, or update a system. Deliverable: a drafted follow-up or safely prepared internal action.

A message may contain several requests. Keep them in one task when they share an owner, deadline, and context. Split them only when different owners, timelines, or completion criteria make separate tracking genuinely clearer.

Rewrite the request as an outcome with a clear finish line. For example, replace “Message about an event question” with “Send verified attendance figures and a next-step recommendation.”

## 3. Gather targeted context

Research only what the task requires. Start with sources closest to the request, then expand only when needed.

Useful source types include:

- Earlier messages and topic searches for related commitments, decisions, or parallel requests.
- Prior correspondence, meeting notes, approved plans, and contact records for relevant relationship context.
- Project pages, event records, operational correspondence, and shared documents for project facts.
- Approved policies and established precedents for people-process, finance, or policy questions.
- Authoritative internal records or trusted public sources for quantitative questions.
- Every substantive attachment or linked document. If a document has sections, tabs, pages, appendices, or embedded requests, review all relevant parts rather than assuming the linked excerpt is complete.

For private communications or records about people, confirm there is a legitimate purpose and clear authorization. Read only the minimum relevant material. Exclude unrelated sensitive details from notes, drafts, and task records. Respect consent, confidentiality, and access rights.

Use non-interactive research methods when possible. Do not use tools that create visible browser activity or other external side effects unless the user has authorized that method.

Stop gathering when you can either complete the preparation or name the precise missing information. Two strong sources are better than many shallow searches.

## 4. Pre-complete the work safely

Do as much as is reasonable without taking irreversible external action.

- For a reply, draft the full message in the user’s requested or established voice.
- For an artefact, create the outline, analysis, reference text, or document draft.
- For a decision, prepare two or three viable options, key evidence for each, and a recommendation with reasons.
- For follow-up, draft the chase or handoff message and prepare any authorized internal update.

If a style guide or approved examples exist, read them before drafting in the user’s voice. Keep drafts concise, direct, and proportionate to the relationship and stakes. Ask one clear question when that is enough; do not turn a simple request into an unnecessary checklist. Include coaching or explanation only when coaching is itself the point of the reply.

Never invent facts, dates, amounts, names, links, or policy positions. Use explicit markers such as:

- `[VERIFY: confirm current figure in the reporting record]`
- `[FILL IN: first-hand observation or personal judgment needed]`
- `[SEARCH: locate the approved public link]`

A draft with visible, specific gaps is often more useful than a blank page. Put gaps directly where they matter in the draft, and warn the user when the draft cannot be sent as-is.

Do not send messages, email, invitations, applications, approvals, or other external communications. You may stage a draft in the user’s messaging system only when authorized. If platform formatting matters, verify that lists, paragraphs, and links will render correctly. When a task record is created, retain the complete staged draft in its notes as well.

For approvals, payments, policy exceptions, and other governed actions, route the draft through the organization’s established process rather than offering an informal approval that bypasses controls.

## 5. Ask questions only when truly blocked

Before asking the user, check whether their position is already documented in earlier messages, notes, decisions, or policies. A documented stance should usually guide the draft.

Ask questions only when a wrong assumption would cause material rework, risk, or an inappropriate commitment. Ask two to four focused questions at most. Before the questions, provide a one- or two-paragraph context recap that restores the full situation:

- who is involved and what has happened so far;
- what is now being requested;
- the real decision, trade-off, or tension;
- evidence already found; and
- the recommended default, if there is one.

Allow combined and custom answers when the interface supports them. If no material fork remains, make reasonable drafting and metadata choices, state them in the report, and let the user correct them.

## 6. Decide whether a task record is worthwhile

Skip the record when the remaining work is a short, immediate action with no waiting, deadline, or dependency—for example, reviewing a ready-to-send draft in one brief sitting. In that case, provide the context and deliverable directly.

Create a record when one or more of these apply:

- Work is deferred or cannot be completed now.
- A deadline, dependency, or wait needs tracking.
- Several steps remain or work will span days.
- The user explicitly requested a task record.

When uncertain, prefer chat-only for a simple reply and a task record for longer-lived work.

## 7. Create a complete task record

Use the user’s chosen task system and verify the record after creation. Use these fields where supported:

- **Title:** Specific, action-led, and short enough to scan.
- **Status:** The user’s equivalent of not started.
- **Due date:** Only when supported by an explicit or clearly implied deadline.
- **Priority:** Best judgment based on impact and time pressure; someone waiting generally raises urgency.
- **Estimate:** Remaining human effort, not research already completed.
- **Area or project:** The best verified category in the user’s system.
- **Notes:** A self-contained handoff using this structure:

```markdown
**What:** [One-sentence request and who is waiting.]
**Source:** [Original message or conversation link.]
**Context:**
- [Relevant history, evidence, and links.]

**Pre-completed:**
[Draft reply, artefact, decision brief, or prepared action. State where any draft is staged.]

**Remaining for the user:**
- [Specific final action.]
```

Do not paste an entire private conversation when a concise context summary will do. Open or retrieve the created record after writing it to confirm the title, notes, links, deadlines, and fields are correct.

## 8. Report back clearly

If a task record was created, report in this order:

1. What the task is.
2. What was pre-completed and where any draft is staged.
3. The chosen metadata, including priority, due date if any, and remaining estimate.
4. Any `[VERIFY]`, `[FILL IN]`, or other blockers.

If no record was created, use this format. Keep the deliverable as the final block so it can be copied without cleanup:

```markdown
## Context for the user (not part of the reply)
- [Ask, requester, key facts, judgment calls, staged-draft location, and verification flags.]

## The reply
[Draft message verbatim.]
```

Nothing should appear after the draft reply in the chat-only format.

## 9. Review staged drafts after an appropriate delay

Whenever a communication draft has been staged, schedule a follow-up review if the environment supports delayed reminders and the user has authorized this workflow. A useful initial delay is about one hour, adjusted for working hours and urgency.

The reminder must identify each staged draft and where to find it, including the conversation location and the draft text or session reference. At review time:

1. Re-read the relevant conversation.
2. Find any final message sent by the user, if accessible and authorized.
3. Compare the sent version with the staged draft: note what was removed, reworded, reordered, added, or left unanswered.
4. Extract only general, reusable lessons, such as preferred brevity, wording, decision framing, formatting, or process routing.
5. If no final message has been sent, reschedule a limited number of checks at increasing intervals, then stop. The user may have deliberately chosen not to send it.

Do not use this review to retain unnecessary private content or construct personal profiles beyond the authorized drafting purpose.

## 10. Improve the workflow carefully

After completing a run, review what helped and what caused avoidable work. Update reusable workflow guidance only when authorized to maintain it. Keep improvements small, general, and testable.

Examples of useful improvements include:

- adding a source type that reliably answered a class of requests;
- recording a generic tool limitation and its workaround;
- adding a genuinely distinct task shape;
- clarifying an instruction that caused repeated wasted effort; or
- encoding a correction as a general drafting or process rule.

Do not silently alter user-owned systems, publish changes, store sensitive conversation content merely for future drafting, or turn a single unusual incident into a rigid rule. If nothing generalizable was learned, make no change.

## Final audit

Before finishing, check:

- Did I read later replies and confirm the work is still live?
- Did I identify the actual deliverable rather than merely log the message?
- Did I research enough, but not excessively?
- Did I draft or prepare the useful work where safe?
- Did I avoid sending, approving, or committing externally?
- Are unsupported facts and links clearly marked rather than guessed?
- Does the task, if created, contain enough context and a specific remaining action?
- Did I protect private information and stay within authorized access?
- If a draft was staged, is any follow-up review authorized, bounded, and documented?


---
name: process-an-inbox-to-zero
description: A privacy-aware workflow for converting authorized email and message inboxes into clear next actions without confusing triage with planning or deep work.
---

# Process an inbox to zero

Process one or more authorized inboxes into a trusted task system. Each reviewed item ends in exactly one bucket: **do now**, **quick win**, **delegate**, **task**, or **delete**. At the end of a run, no actionable commitment should exist only in an inbox: it has been completed, assigned, recorded as a task, or intentionally removed.

This workflow uses Inbox Zero and Getting Things Done principles. Processing means deciding what an item is and where it belongs. It does not mean completing all work described by messages, and it does not replace a separate daily-planning process.

Urgency is based on the consequence of waiting, not on unread status, recency, message length, notification volume, or whether an item is in a group conversation.

## Operating rules

1. **The user controls external changes.** Do not send, react, archive, delete, label, mark read, mark complete, or otherwise alter an inbox unless the user explicitly authorizes that specific action.
2. **No bulk changes by default.** Review each item, or a clearly defined group of routine items, before recommending any change.
3. **Do not draft unless asked.** When asked, provide copy-ready text. Do not save or send a draft without separate authorization.
4. **Create a task only with per-item authorization.** A request such as “task this” applies only to the clearly identified item. Do not create tasks in bulk.
5. **Use a work cap.** Ask the user to choose a cap, or use 15 minutes as a practical default. Work that can be finished within the cap may be do-now work; longer work normally becomes a task.
6. **Respect access boundaries.** Access private communications, calendars, records, and internal documents only for a legitimate purpose and with clear authorization. Use the minimum sources and information needed. Omit unrelated sensitive or personal details from output.
7. **Keep evidence separate from decisions.** Explain what the message shows and why a recommendation follows. Do not invent the user’s commitments, preferences, beliefs, or relationship judgments.

## Readiness gate

### Set scope, authority, and time

Identify the requested sources and confirm they are authorized. If scope is unclear, state a reasonable assumption, such as reviewing all authorized inboxes, rather than delaying with a separate scope question. If the user wants to prioritize an existing task list rather than messages, move to a planning workflow instead.

| User wording | Source to review |
|---|---|
| “email” or “work email” | Authorized work email account |
| “personal email” | Authorized personal email account, normally read-only |
| “team chat” | Authorized team workspace, including saved items, direct messages, and mentions |
| “community chat” | Only the named community or workspace |
| “messages” or “chats” | Authorized messaging services, optionally limited to one service |
| “all inboxes” | All authorized email and messaging sources |

Retrieve the current date, day, and time from a reliable time capability set to the user’s time zone. Do not estimate current time when deadlines, response windows, or planned focus blocks matter.

### Read goals and open work

When the user authorizes access to planning information, retrieve only what triage needs:

- Current longer-term and weekly goals.
- Today’s intention, plan, or most important task (MIT).
- Open tasks, including title, status, and due date.

Use the chosen system’s documented date-query method. Verify date filtering if results appear unexpectedly empty. Summarize active goals in three to six short lines for use during triage. If a planning level is absent or empty, note it briefly and continue; do not invent goals.

If a non-inbox MIT is scheduled now or soon, ask once before reading messages:

> Is inbox processing the most important thing right now, or does it just feel productive?

Trust the answer. Skip this question when inbox processing is planned work or no MIT exists.

### Check source readiness

Before retrieval, review applicable access rules and confirm each source is connected. If a source fails, place the gap at the top of the output and state:

- the failed source;
- the exact error or connection state;
- what could not be reviewed; and
- the safe next repair, such as reconnecting or reauthorizing access.

Continue with functioning sources. Never quietly omit a failed source or substitute another source that cannot provide equivalent information.

## Collect inbox candidates

Read selected sources in parallel when safe. For each candidate, collect: source, sender or participants, subject or conversation label, latest-message date, latest sender, one-line gist, and a stable link when safe and supported.

For email, group messages into threads and retain the latest relevant message per thread. Start with previews; open the full thread only when the ask, deadline, ownership, or current status is unclear. Routine newsletters, receipts, calendar notices, and automated updates are usually delete candidates. Inspect them further only when the preview suggests a decision, deadline, security issue, or financial consequence.

For team chat, treat saved-for-later items as work the user intentionally retained. Treat unread direct messages and mentions as attention debt, not automatic priorities. When otherwise equal, review direct messages and explicit mentions before broad channel discussion. Prefer a purpose-built inbox or audit view over search alone when search may omit saved, unread, or completion state.

For personal and networked chats, choose a lookback period with the user or use two weeks as a default. Determine reply debt by checking who sent the last meaningful message and whether a response is expected. Read nearby messages when the latest message does not establish the ask. Direct conversations generally rank above group messages unless a group message explicitly requests the user’s input or has a time-bound consequence.

## Classify and rank every reviewed item

Place every item in exactly one bucket:

1. **Do now:** important, time-sensitive, and completable within the selected work cap.
2. **Quick win:** a response or action likely to take about two minutes or less.
3. **Delegate:** work another person should own.
4. **Task:** meaningful work exceeding the cap, needing later context, or blocked until later.
5. **Delete:** no action needed, such as a resolved thread, FYI, routine notice, naturally ended conversation, or low-value subscription.

For delegation, suggest an owner only where current evidence supports it: the conversation, documented responsibilities, and current project context. If evidence is weak, say **owner unclear** rather than guessing.

Before suggesting a new task, check whether an open task already covers the work. If so, recommend clearing the inbox copy rather than creating a duplicate.

Rank do-now items, and order other buckets, using these criteria in order:

1. A hard deadline or time-bound decision, especially today or tomorrow.
2. A person blocked waiting for the user.
3. A clear connection to today’s MIT, weekly commitments, or longer-term goals.
4. Relationship cost of delay.

Age is supporting evidence, not a priority rule. Older unanswered messages may deserve attention, but do not override consequences and goals.

## Present the triage snapshot

Show the sorted result before working through items. Use labels and order, not color alone, to communicate priority.

```markdown
## Inbox zero: <date>, <sources>

**Goals used:** <longer-term goal> · <weekly goal> · <today’s MIT>
**Missing data:** <failures or “none”>
**Counts:** <total: do now, quick wins, delegate, task, delete>

### Do now
1. <item> — <source, sender, age> — <why now> — <link>

### Quick wins
- <item> — <one action> — <link>

### Delegate
- <item> — <suggested owner and evidence, or “owner unclear”> — <link>

### Task
- <item> — <suggested task title, due date if implied, and reason> — <link>

### Delete
- <counts by type, plus any surprising item>
```

Then ask two to four useful questions in one plain-text numbered block. Use lettered options where practical so the user can answer compactly, for example `1b, 2a`. Ask only about genuine uncertainty: whether a goal remains live, whether the user wishes to manage a sensitive conversation directly, whether an unfamiliar sender matters, or how much time is available. If nothing is uncertain, ask one question about available time. The user’s bucket choice is final.

## Work the buckets

Proceed in this order and stop whenever the user wants.

### Do now: one item at a time

Read the full conversation and check the calendar around relevant dates. Gather only decision-relevant context from earlier correspondence, project records, or documents. For hiring or assessment items, use authorized, role-relevant evidence only. Focus on capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance.

Provide a short paragraph covering who is involved, what they want, what is at stake if the user waits, and the recommended immediate action. Link supporting evidence where available. Ask one to three questions only the user can answer. When the user confirms it is handled, move to the next item.

### Quick wins, delegate, task, and delete

List quick wins together for a clearing sprint. The user performs inbox changes unless they specifically authorize an action.

For delegated and task items, get confirmation. When explicitly authorized to create one task, add it to the chosen task system with a clear action title, open status, implied due date, practical importance and urgency, time estimate, and relevant domain or project. Use this note format:

```markdown
**What:** The ask and who is waiting.
**Source:** Link or privacy-safe conversation citation.
**Context:**
- Key fact or constraint.
- Relevant deadline, decision, or linked record.
**Next step:** The first concrete action.
```

Do not put a prewritten reply in the task unless requested. After task creation, tell the user the inbox item can now be cleared and provide a task link if the system supports one. For delete items, remind the user which messages can be archived, deleted, or marked complete.

## Drafting, closure, and audit

When asked for a draft, provide one copy-ready plain-text draft as the final block of the response. Match the requested channel and tone. Keep claims factual and avoid commitments the user has not approved.

End with concise source-by-source status: completed, tasked, delegated, still open, and unreviewed because of access or time. Say plainly if many loops remain open.

Audit the run for pointless questions, incorrect bucketing, incomplete sources, excessive context searching, and privacy risks. Record only general workflow improvements in authorized documentation. Do not store message content, credentials, or unnecessary personal details.

## Single-item mode

Use this mode when the user or an authorized reminder identifies one specific inbox item. Do not inspect other inbox items.

1. Read the source rules and retrieve only the item plus minimum necessary context.
2. State who is involved, what they want, what happens if it waits, the recommended bucket, and the concrete next action.
3. Help the user handle it under the normal authorization, privacy, task, and drafting rules.
4. Tell the user which inbox action will clear it afterward, such as archiving an email or completing a saved chat item. Do not require a special confirmation phrase.


---
name: design-a-work-sample
description: Create or improve a short, paid, asynchronous work sample that produces job-relevant evidence and can be scored consistently. Validate that it distinguishes role-relevant performance through simulated submissions.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A good work sample asks candidates to do a realistic, bounded version of the job, produces evidence that is hard to fake, and is quick enough for reviewers to score consistently.

Use it for both new exercises and revisions. Do not use it for interview questions, application-form screeners, or multi-day work trials. If the request could refer to one of those formats, ask which format is needed before proceeding.

## Purpose and principles

A work sample sits between initial screening and interviews. It should help the hiring team answer a narrow question: can this person demonstrate the most important parts of this role under realistic constraints?

A useful work sample does not try to assess everything. Some qualities are better assessed elsewhere:

- Interviews can assess communication, motivation, collaboration, and live reasoning.
- References can assess reliability, integrity, and sustained performance.
- A later trial can assess consistency, judgment over time, and work in real systems.
- Training can often close gaps in a particular tool, internal process, or domain vocabulary.

The work sample should focus on a small number of load-bearing abilities that are both important to the role and observable in a short exercise. Examples include prioritization, practical judgment, clear writing, problem diagnosis, sourcing, execution speed, systems thinking, or the ability to turn ambiguity into useful work.

Default design constraints:

- Make the exercise paid.
- Set a clear expected time limit, commonly two to four hours.
- Use a realistic but fictionalized or safely anonymized scenario.
- Do not ask candidates to produce work that the organization will use commercially unless that use is separately agreed.
- Keep grading time to roughly 20 to 25 minutes per submission.
- Make the exercise self-contained. Candidates should not need access to internal tools, private data, or unavailable stakeholders.
- State the permitted use of AI and evaluate judgment rather than trying to detect AI use through writing style.
- Test only capabilities that are materially related to the role. Exclude protected characteristics and unrelated proxy criteria.
- Offer a clear route for reasonable accommodations or an equivalent accessible format without lowering the role-relevant standard.

## Step 1: Pre-flight

Before designing the work sample, confirm that the hiring team has both of the following:

1. A current job description or role brief that explains responsibilities, level, expected outcomes, and reporting context.
2. A role-success profile, hiring plan, or equivalent document that identifies the capabilities and experience most likely to produce the role's required outcomes.

If either is missing, stop and ask for it. Do not attempt to discover the ideal candidate while designing the test. That creates a moving target and usually produces an exercise that feels plausible but measures the wrong things.

Use this request format:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

If the materials exist, read the full role context. This may include linked project notes, current team constraints, examples of strong work, prior hiring feedback, and any existing exercises for comparable roles. Read one or two reference exercises only to calibrate tone, length, and operational format. Do not copy their task shape automatically. Different roles need different evidence.

Use only hiring materials the team is authorized to use for this role. Minimize private information: read the minimum relevant evidence, omit unrelated or sensitive candidate details, and do not infer protected traits. Keep alignment notes, simulations, and reviewer guidance inside the approved hiring access boundary.

After reviewing, give a brief status update stating what sources were read and move to the alignment memo.

## Step 2: Write the alignment memo before drafting

Do not draft candidate-facing instructions yet. First create a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include these sections.

### Load-bearing traits

List three to five abilities that this role succeeds or fails on and that can be surfaced in the exercise window. Phrase them as observable capabilities, not vague virtues.

Weak: “Strategic thinking.”

Better: “Can identify the highest-leverage problem in a messy operating situation, explain the tradeoff, and deliver a useful first action.”

### What the exercise will not test

Name important criteria that should be assessed elsewhere. This keeps the test honest and prevents it from growing into an unrealistic proxy for the entire job.

For example, a three-hour written exercise may not fairly test long-term reliability, leadership over months, responsiveness in live meetings, specialized software fluency, or culture contribution.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level. Explain what this changes in the exercise:

- Junior candidates may need more context and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make tradeoffs, establish direction, and create work another person could use without explanation.

### Failure modes to catch

Identify two or three plausible role-misaligned patterns that could otherwise look strong in a conventional hiring process. Describe observable work patterns rather than labeling people. Examples:

- A polished planner who does not ship usable work.
- A fast executor who misses the central problem or creates avoidable risk.
- A careful but indecisive candidate who defers every meaningful call.
- A technically skilled candidate who cannot communicate with the intended audience.

### What strong looks like

Write one short paragraph describing a top submission. Focus on evidence: what choices it makes, what it notices, what it produces, and how it handles uncertainty.

Present the memo to the hiring owner and ask for explicit confirmation:

> Does this match the abilities and failure modes you want this work sample to assess?

Do not proceed until the owner confirms or revises the memo.

## Step 3: Propose exercise shapes

Once the memo is locked, offer three possible shapes. Each option should test the load-bearing traits in a distinct way, be understandable within about a minute, be self-contained, and be scorable quickly.

For each option, include:

- **Shape:** a plain-language description of the candidate task.
- **What it tests:** the specific load-bearing traits it reveals.
- **Why it is evaluable:** what evidence reviewers would see and why scoring can be consistent.
- **Main risk:** the most likely way the format could create noise or unfairness.

Keep each option concise. Useful shapes include:

- **Triage pile:** The candidate receives a realistic set of messages, requests, and constraints. They prioritize, draft responses or work products, and recommend one systemic improvement. This suits operations, coordination, support, and communications-heavy roles.
- **Choose the highest-leverage action and ship it:** The candidate receives a brief with several possible priorities, selects one, explains the choice, and creates a small usable output. This suits strategic operations and builder roles.
- **Diagnose and fix:** The candidate reviews a messy situation, identifies the key problem, and ships one targeted intervention. This suits product, program, analytical, and process-improvement roles.
- **Source and pitch:** The candidate defines a target profile, identifies promising channels or prospects from provided information, and writes outreach. This suits recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** The candidate chooses or is assigned one intervention area, assesses it using supplied evidence, and makes a recommendation for a decision-maker. This suits research, policy, strategy, and specialist knowledge roles.
- **Design a repeatable system:** The candidate creates a lightweight process, playbook, or operating artifact that a teammate could use. This suits program, community, enablement, and operational design roles.

Do not draft the full exercise until the hiring owner chooses a shape. If none are right, generate three more based on the confirmed traits rather than forcing a familiar format.

## Step 4: Draft version 1

Write the candidate-facing exercise in this order.

## [Role] Work Sample

Open with one or two sentences explaining the abilities the exercise assesses. State the total time expected.

**Your mission**

Describe a specific situation, not an abstract assignment. Include enough context to make the work realistic. Where decisiveness is a trait being tested, make clear which stakeholders are unavailable during the exercise so candidates must make reasonable calls instead of deferring everything.

End with one sentence that restates what the candidate will produce.

**Deliverables**

List two to four parts. Include rough time guidance where useful. A common operations pattern is:

- A short prioritization or analysis section.
- Several actual drafts, decisions, or shipped outputs.
- One systemic fix, process improvement, or reusable artifact.

Avoid excessive micro-tasks. A small number of substantive outputs reveals more than dozens of shallow decisions. If planning and execution both matter, explicitly warn candidates not to spend all their time planning.

**Context**

Provide the minimum information needed to complete the exercise: project state, audience, constraints, available resources, relevant policy, and stakeholder availability. Use fictional names, domains, and identifiers unless the hiring owner explicitly approves use of real public information.

For a triage-pile exercise, include eight to ten realistic items. Some should connect so that candidates are rewarded for seeing patterns across the whole situation. Include reference notes that provide any data needed for a fair decision, such as escalation rules, capacity limits, or refund policy.

**Instructions**

Include:

- The expected time limit.
- The submission deadline, written clearly.
- Submission format, such as one document or PDF, plus links to supplementary artifacts if needed.
- Payment amount, payment process, and any early-submission bonus, if offered.
- What tools and AI assistance are permitted.
- A request to document important assumptions briefly.
- Permission to submit incomplete work if time runs out.
- Optional guidance on a short walkthrough video, if this would add useful signal.

Use a transparent AI policy. For example:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

**Anticipated questions**

Include answers to common questions, such as:

- If a requirement is unclear, make a reasonable assumption and state it briefly.
- If you do not finish in the expected time, submit what you have and note what you would do next.
- The work will be used only to evaluate candidates unless another use is agreed separately.

## Candidate-facing writing and format checks

Write in direct, plain US English unless another locale is appropriate. Keep instructions easy to paste into the organization’s chosen hiring system and easy to read in a document.

Before sharing a draft, check that the candidate-facing text:

- Has no tables if the destination system renders tables poorly.
- Avoids horizontal divider lines if they break the destination editor.
- Uses simple headings and bullets.
- Avoids generic AI-sounding slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.
- Uses “by the end of [day]” rather than abbreviated phrasing.
- Uses clearly fictional email addresses and names in fictional scenarios.
- Formats multi-line message metadata clearly. If the target editor collapses line breaks, use its supported soft-break method.
- Does not contain confidential details, credentials, private contact information, or sensitive internal data.

After every draft, add a separate section that is not for candidates:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets on choices the owner may want to change. Typical notes include whether an item is too obvious, whether the scenario is realistic enough, whether the payment structure matches role level, whether a deliverable is too prescriptive, or whether a video should be optional.

End with one focused decision question, such as: “Which part should we tighten first?”

## Step 5: Iterate with the hiring owner

Expect multiple rounds. For each revision, provide the complete updated work sample, not only a change list, so it can be copied directly into the selected system.

Apply feedback directly unless it would materially undermine validity, fairness, or safety. If that happens, state the concern once in plain language, offer an alternative, and let the hiring owner decide.

Common revision directions include tightening vague instructions, loosening over-prescriptive tasks, correcting scenario facts, simplifying deliverables, changing payment, and replacing unrealistic details.

## Step 6: Simulate two candidates

Before declaring version 1 complete, simulate two full submissions in parallel using the exact candidate-facing instructions.

### Role-aligned simulation

Use a persona that matches the confirmed role-success profile. Have them complete the actual deliverables under the stated time limit. Ask for a short reflection on their choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest, capable candidate who could pass ordinary screening but whose demonstrated work lacks one role-critical capability. Choose a relevant mismatch, such as a planner where the role needs a builder, a cautious hedger where it needs decisive judgment, or an executor who cannot see systemic patterns. Keep the difference tied to job evidence, never identity or background.

Have this persona produce the same complete submission.

Then synthesize the results:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both candidates performed similarly.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by likely impact.

Floor checks that both candidates pass are not automatically bad. The concern is when a central trait fails to create meaningfully different evidence.

## Step 7: Apply validation improvements

Revise the full exercise based on the simulation. Target the weakest diagnostic points first. Examples of useful revisions:

- Make connected scenario items more interdependent.
- Remove obvious noise that takes seconds to dismiss.
- Add a concrete constraint that forces a meaningful tradeoff.
- Replace a broad opinion prompt with a usable deliverable.
- Clarify the rubric so reviewers reward the intended behavior.
- Remove specialized knowledge requirements that are trainable and not essential on day one.

Do not make the task harder merely to make it more selective. Make it more diagnostic of the confirmed traits.

## Step 8: Optional external review

If other reviewers provide feedback, assess each suggestion against the alignment memo. State which suggestions to integrate, which to skip, and why. External review is evidence, not an automatic instruction. The hiring owner remains accountable for the assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The role description and role-success profile are confirmed.
- The alignment memo is approved.
- The chosen task shape maps directly to the load-bearing traits.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and does not require private access.
- Payment and submission instructions are clear.
- Candidate-facing text is formatted for the destination system.
- A reviewer can score a submission in about 20 to 25 minutes.
- A role-aligned and plausible role-misaligned simulation has been completed.
- The simulation led to any necessary revisions.
- The final version has no sensitive data and does not create unpaid production work.
- Role-relevant criteria, accommodation routes, and potential proxy bias have been checked.

## Common failure modes

Avoid these patterns:

- Designing the task before agreeing what it should measure.
- Testing tool familiarity, domain trivia, or trainable knowledge instead of durable judgment.
- Asking for too many small outputs instead of a few meaningful ones.
- Making every scenario item independent, which tests volume but not pattern recognition.
- Allowing candidates to defer every decision to an available stakeholder when decisiveness is meant to matter.
- Giving vague context that rewards insider knowledge.
- Setting a word-count target that encourages padding.
- Creating a test that takes longer to grade than the signal justifies.
- Treating polished writing or presentation as the main signal when the role requires something else.
- Declaring success without testing whether the exercise distinguishes the role-relevant evidence it was designed to measure.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, useful for assessment, and clear about what good performance looks like.


---
name: run-a-reference-call
description: Prepare and run a concise reference conversation that gathers specific evidence instead of vague praise.
---

# Run a reference call

Use this when checking a candidate's past work for a hiring decision.

## 1. Prepare from the decision

Read the role outcomes, interview evidence, remaining concerns, and the
candidate's relationship with the referee. Decide which uncertainty the call
must reduce. Do not ask a generic list when the hiring team already knows what
it needs to test.

## 2. Establish context

Confirm how the referee worked with the candidate, for how long, and how closely
they observed the relevant work. Weight evidence by direct observation rather
than title or confidence.

## 3. Ask for examples

Useful questions include:

- What result did the candidate personally own?
- What did strong performance look like in practice?
- Where did they need the most support?
- How did they respond to difficult feedback?
- Which environment helped or hurt their performance?
- What kind of role would you hesitate to place them in?
- Would you choose to work with them again, and in what capacity?

Follow vague praise with “What did that look like?” or “Can you give a specific
example?”

## 4. Test concerns fairly

Ask neutral questions about the hiring team's uncertainties without revealing
private interview judgments or inviting confirmation. Note contradictions and
seek concrete evidence.

## 5. Record signal

Separate observations, the referee's interpretation, and your inference. Record
confidence and any important limits on what the referee could know. Do not turn
one reference into a final verdict on its own.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive route, protecting authenticated context, verifying rendered state, and separating preparation from consequential actions.
---

# Use a browser safely

Use this workflow for browser-based work such as completing rendered forms, changing dashboard settings, collecting information from dynamic pages, testing a user flow, or working in an authorized signed-in session. Apply it only when a supported direct interface, ordinary page retrieval, or static request cannot safely and reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not perform a consequential final action until the account, target, page state, and authorization are clear.

A successful automation command does not prove that a website accepted a change. Modern web applications may maintain internal state separately from visible HTML, commit values only after focus leaves a field, replace controls after re-rendering, or show a cosmetic error after an operation has already completed.

## 1. Choose the least invasive route

Use the first route that safely fits the request:

1. **Supported direct interface.** Prefer a documented, authorized API, export, integration, or ordinary form endpoint when it can perform the requested task.
2. **Isolated headless browser automation.** Use this for public pages, test environments, routine extraction from rendered pages, screenshots, and forms that do not need an established user identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing signed-in session, account-specific dashboard, single sign-on state, or a user-directed browser context.

Before driving a browser, look for a direct route. Review official documentation, normal form actions, page source, and browser-visible network requests for supported endpoints. A rendered form may submit structured data to an authorized service, which can be more reliable than reproducing every browser interaction.

Do not use undocumented interfaces to bypass access controls, consent boundaries, service restrictions, or anti-abuse mechanisms. Do not use an authenticated visible session merely because it is convenient: it can interrupt the user’s work and increases privacy and account risk.

If a site blocks automated browsing, do not attempt to evade its protections for casual research or collection. An authorized visible session may be appropriate only when the user explicitly requested a legitimate task on that specific site and an established session is necessary. Never weaken browser security, access restrictions, warnings, authentication, or anti-abuse controls to make automation easier.

## 2. Protect identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not place unrelated personal details into screenshots, logs, notes, or reports. Keep outputs within the requester’s appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated context, identify the correct account, organization, environment, and browser profile. Never infer identity from a generic browser-window name, remembered default, old tab title, connection nickname, or the order in which browsers appear.

Use these rules:

- Announce when taking control of a visible browser and state the purpose.
- Work in a fresh tab, new window, or isolated tab group unless the user explicitly points to an existing tab.
- Classify the context explicitly, such as personal, work, testing, staging, or production.
- Select the browser profile or session that matches that context rather than using a generic “current browser” selector.
- Verify the signed-in account through a reliable account indicator before opening or changing the real target.
- Confirm the active environment and target object before making changes.
- If the required account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not expose credentials, session tokens, recovery information, private account data, or security settings in output or logs.
- Do not disable multi-factor authentication, security warnings, signature checks, browser protections, or access controls.

Use an account preflight gate before actions that change data. Confirm account identity, environment, and target object. If the automation environment has a verification marker or permission gate, mark it verified only **after** the account check has passed. Never create a marker merely to unlock write actions.

Ask: **Which account is this? Which environment is this? What exact item will change?** Resolve uncertainty before proceeding.

## 3. Establish the task boundary and authorization

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, workflow, or transaction.
- Information that will be entered, collected, changed, uploaded, or sent.
- The minimum information needed for the task.
- Fields that require the user’s judgment or contain ambiguity.
- Whether the action is reversible.
- Whether the task includes sending, publishing, paying, deleting, granting access, changing a plan, changing ownership, or another external commitment.

Separate **preparation** from **commitment**. Filling fields, drafting content, collecting information, selecting options, and preparing a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, or making a permanent account change may not be.

For consequential work, use two phases:

1. **Preparation pass:** Fill or configure the page, verify all values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Confirm authorization when needed, then re-check account, target, and readiness. Perform the final action once.

Honor an explicit request to review before submission. If the user has already clearly authorized a specific final action, do not repeatedly ask for the same approval. If authorization is missing, prepare and verify the complete result, show a concise pre-submit summary, and ask only for authorization to take the final action.

Treat a warning such as “cannot be undone,” “final,” or “cannot be edited after submission” as a one-way action even if it resembles a normal form submission.

## 4. Inspect the rendered page before editing

Do not start by guessing selectors, filling fields by numeric position, or trusting a visual approximation. First inspect the rendered page and collect enough structure to identify controls safely.

For each relevant control, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether it is required.
- Validation rules, character limits, formatting behavior, and disabled state.
- Whether an apparent field is the true editor, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, date, or tab causes a full form re-render.

Address controls by stable semantic identity: visible label text, accessible name, or an explicit label relationship. Do not address dynamic controls by DOM index when labels are available. Component order can change between page loads or after re-rendering.

Before changing an existing record or setting, inspect its current state. This avoids editing the wrong item or unintentionally overwriting a value.

### Generic inspection pattern

Use the chosen browser automation capability to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

```js
// Pseudocode: adapt to the chosen browser automation library.
const controls = inspectAll('input, textarea, [contenteditable="true"], [role="textbox"]')
  .map((element) => ({
    tag: element.tagName,
    type: element.type || element.contentEditable,
    role: element.getAttribute('role'),
    label: accessibleLabel(element),
    required: element.required || element.getAttribute('aria-required') === 'true',
    valueLength: readableValue(element).length,
  }));

saveJson('form-before.json', controls);
```

## 5. Use the right interaction for each control

A generic “set value” operation is not reliable for every component. Use an interaction that resembles how a user works with the actual control.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use normal text entry or fill behavior | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select old content, enter text through keyboard-style events, then blur | Direct DOM mutation may not update the application’s internal model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle | Selection can trigger a re-render. |
| Checkbox or radio control | Read current state first; change only if needed | A click can toggle an already-correct value. |
| Date/time picker | Set date and time, then verify the rendered summary | Open popovers can clear, reinterpret, or overwrite related values. |
| File upload | Confirm file, destination, and privacy implications first | Uploading may start immediately and may be hard to undo. |

For framework-driven editors, simulate normal user interaction rather than writing directly to page properties. A robust general sequence is:

1. Focus the actual editable element.
2. Select existing content.
3. Delete it.
4. Insert the new text using keyboard-style events.
5. Move focus to a neutral page element.
6. Wait briefly for application state to settle.
7. Read the result back.

Some forms pair a visible rich-text editor with a hidden input. Editing the hidden input can look successful in a raw DOM dump while server-side validation still treats the editor as empty. Target the control the user interacts with and the application actually reads. If an accessibility locator identifies an empty wrapper, inspect the underlying editable element and follow its label relationship.

If changing a dropdown, checkbox, tab, date, or other choice can refresh the form, make and verify those choices **before** filling long or complex text. Re-inspect after the change and confirm earlier entries remain present.

Avoid using the clipboard as a primary automation dependency. Headless contexts may not grant clipboard access, and synthetic paste behavior varies. When a rich-content paste is genuinely required, use only the browser-supported method available in the authorized environment, then verify the resulting content through an appropriate read-back mechanism.

## 6. Verify after every meaningful edit

After each field is filled or setting changed, read it back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare lengths, required state, or a short redacted summary instead of exposing full text unnecessarily.

Check for these mismatches:

- The automation layer reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated by a single-line control or length limit.
- A custom editor displayed text but did not retain it internally.
- Editing a later field erased an earlier field after a re-render.
- A hidden synchronization field changed instead of the visible editor.
- A selection changed a dependent recipient, date, option, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once with a more appropriate interaction method, and verify again. If the page still rejects or alters the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

For a form with many fields, retain a structured before-and-after state record. It should identify fields semantically and record value lengths or safe summaries. Do not produce a large inline table containing sensitive form contents when a short summary and securely scoped artifact are enough.

## 7. Run a pre-submit readiness gate

Before any final submission or high-impact change, inspect the full relevant page state again. Confirm all of the following:

- The correct account, organization, and environment are active.
- The target item is the intended one.
- Every required field is present and non-empty.
- Each entered value matches the intended content closely enough for the task.
- Dropdowns, checkboxes, dates, recipients, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially filled form is recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only within the appropriate access boundary.

### Readiness checklist

- [ ] The account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 8. Treat one-way actions as a distinct phase

The following generally need explicit confirmation immediately before the final control is activated unless the user already gave clear, specific authorization for that exact action:

- Sending messages, invitations, or notifications.
- Publishing content.
- Submitting official, externally reviewed, or irreversible forms.
- Making a payment or purchase.
- Deleting records or files.
- Changing subscriptions, billing, access, ownership, or security settings.
- Any action described as permanent, final, irreversible, or impossible to edit later.

A concise confirmation request should state the target, important values, recipients or audience, cost if any, irreversible effects, and unresolved questions. Do not hide material consequences in a vague “ready to submit” message.

For low-risk reversible changes explicitly requested by the user, such as editing a preference or updating a draft, proceed after normal verification unless the page presents an unexpected warning or wider impact.

## 9. Confirm completion after acting

A button click is not proof of success. After acting, look for reliable evidence such as a success message, confirmation reference, newly created record, persisted saved setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate submissions, payments, messages, or records.

If completion cannot be verified, report what was attempted, the evidence that exists, and what remains uncertain. Do not represent an attempted action as completed.

## 10. General failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after a later edit | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline or rich-text control, or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control that the application actually reads. |
| The automation layer becomes unstable on a complex page | The chosen automation method is unsuitable | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers show different behavior | The site varies behavior by browser context | Prefer an authorized direct interface; if needed for an explicit task, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior | Close it through a neutral page action and re-verify affected fields. |
| A visible error may be cosmetic | The task may already have completed | Inspect the resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |
| A security check or authentication prompt appears | The site requires user presence or protected authentication | Ask the authorized user to complete the check; do not bypass, simulate, or weaken it. |
| A browser extension, native helper, or automation connection fails integrity checks | The local integration may be stale or compromised | Stop and use an approved repair path that preserves signature and integrity verification; never disable those checks. |

## 11. Maintain the workflow responsibly

When a real failure reveals a broadly reusable lesson, update the local procedure or project documentation with a concise symptom-and-fix entry. Do not record private account details, personal facts, credentials, identifiers, or site-specific secrets. Consolidate older guidance instead of endlessly appending incident history.

Keep tool instructions separate from the workflow where possible. Tool versions, paths, profile names, and local implementation details change frequently. Revalidate them in the current environment rather than relying on stale assumptions.

## Final audit checklist

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only the minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back and verified.
- [ ] Required fields and validation state passed the readiness gate.
- [ ] A pre-action record was captured when the action was consequential.
- [ ] Explicit confirmation was obtained before a consequential final action when required.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: Design, test, improve, evaluate, and package reusable AI skills through an evidence-based, user-centered workflow.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, improve an existing one, evaluate whether it helps, or refine when it activates. A skill is a focused set of instructions, plus optional resources, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the intended job and its boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with a person and measure objective requirements where useful.
5. Improve the skill from evidence, not guesswork.
6. Repeat until it is useful, reliable, and not narrowly fitted to a few tests.
7. Optionally improve the description that determines when the skill activates.
8. Package and hand off the finished skill.

Adapt the depth of this process to the user’s goal. Some users want a quick collaborative draft. Others need a rigorous comparison with baselines, formal checks, and several revision rounds. First determine where they are in the loop, then help them take the next useful step.

## Communication principles

Match the user’s technical background. Use plain language by default. Terms such as *evaluation* and *benchmark* are usually acceptable if briefly defined. Explain specialized terms such as *JSON*, *assertion*, *baseline*, or *schema* before relying on them unless the user clearly uses them comfortably.

Ask questions because their answers affect the design, not merely to fill out a checklist. For example:

- “What should a successful result look like: a chat response, a report, a file, or an action?”
- “What information may the skill use, and what should it do if that information is unavailable?”
- “Should it make a reasonable best effort, or pause when a decision could materially change the result?”

Keep the user involved at meaningful decision points. Confirm intended scope before writing extensive instructions, share proposed tests before treating them as representative, and let human judgment guide subjective issues such as writing quality, visual design, and practical usefulness.

When the task involves private communications, records, or personal information, require a legitimate purpose and clear authorization. Use the minimum relevant sources and information, omit unrelated sensitive details, respect consent and reasonable privacy expectations, and keep results within the appropriate access boundary.

## 1. Identify the starting point

Determine which of these situations applies.

### New skill

The user has an idea for recurring work, such as preparing project updates, reviewing structured documents, or transforming approved files. Start with discovery and a first draft.

### Existing skill

The user has a draft or installed skill and wants it edited, simplified, tested, or improved. Read the current instructions before proposing changes. Preserve its established identity, including its name, unless the user explicitly asks to rename it.

If the existing copy may be read-only, make an editable working copy in a user-approved location. Keep the original unchanged until the user accepts the revision.

### Workflow demonstrated in the conversation

The user may ask to “turn this into a skill.” First extract what is already known from the conversation:

- Inputs, files, and approved sources used.
- Sequence of decisions and actions.
- Tools or capabilities needed.
- Corrections and preferences supplied by the user.
- Observed output format and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow and identify gaps for confirmation. Do not quietly convert a one-time workaround into a general instruction without checking that it applies broadly.

### Evaluation or optimization request

The user may already have a plausible skill and want to know whether it actually improves outcomes. Go directly to test design, evaluation, and revision. Do not rewrite a skill merely because a rewrite is possible.

## 2. Capture intent, scope, and boundaries

Gather enough information to define a coherent job. Start with the questions whose answers matter most; do not force every question when the conversation already answers it.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What user requests, phrasing, or situations should cause it to be used?
3. **Inputs:** What information, files, examples, systems, references, and permissions may it use?
4. **Outputs:** What should it produce, change, or communicate? Is there a required format?
5. **Success criteria:** How will the user decide that the result is correct, useful, safe, and complete?
6. **Boundaries:** What should it not do? When should it ask a question, request approval, decline, or return work to the user?
7. **Variations:** What common cases, difficult cases, or meaningful exceptions should it handle?
8. **Dependencies:** Does it need a particular tool capability, template, script, reference source, or user-provided access?
9. **Testing:** Should it be tested with realistic example requests?

Recommend tests when outputs can be objectively checked, the workflow is consequential, the skill will be reused often, or the user needs evidence that a revision improves on an earlier version. For highly subjective work, recommend representative human review instead of weak numerical proxies.

Offer useful choices when requirements are unclear:

- “Should missing information cause a question, a clearly labeled assumption, or an incomplete draft?”
- “Should the output be concise, detailed, or selectable by the user?”
- “Should the skill work with any source the user provides, or only specifically approved sources?”
- “Does this action need confirmation because it is external, irreversible, or high impact?”

## 3. Research and inspect available context

Before drafting, inspect relevant user-approved materials when they would reduce uncertainty: documentation, templates, comparable skills, file specifications, standards, or existing evaluation data. Use available research capabilities in parallel when practical, but do not research private material without authorization.

Research should reduce burden on the user, not replace their authority over requirements. Use it to identify:

- Existing conventions or output standards.
- Constraints imposed by a file format, system, or available capability.
- Reusable patterns for similar tasks.
- Safety, privacy, compliance, or approval requirements.
- Existing tests or feedback that should inform a revision.

If sources conflict or important requirements remain uncertain, present the uncertainty rather than inventing a rule.

## 4. Choose a maintainable skill structure

Keep a skill focused enough that users and AI systems can predict its purpose. A skill may support related variants, but unrelated jobs should be split when they have different audiences, permissions, source-of-truth rules, or definitions of completion.

A typical package can contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional supporting documentation
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional tests and evaluation material
```

Use progressive disclosure:

1. **Metadata:** a short name and description used to decide whether the skill is relevant.
2. **Core instructions:** the workflow needed for normal use.
3. **Supporting resources:** detailed references, templates, and scripts loaded only when relevant.

Keep core instructions readable. If they become too long, move domain-specific detail into clearly named supporting files and state exactly when to consult each one. Large reference files should include a navigation section or table of contents.

For a skill with several variants, use a shared selection workflow plus separate references for each variant. The AI should load only the relevant material rather than carrying every variant into every request.

### Bundle resources only when they earn their place

If several test runs independently recreate the same helper process—such as validation, document generation, conversion, or formatting—consider bundling a reusable script or template. A resource is worthwhile when it is repeatable, easier to verify than free-form reasoning, safe within the user’s authority, and likely to be reused.

Document each resource’s purpose, inputs, outputs, limitations, and when not to use it. Do not automate actions that would surprise the user or extend beyond approved permissions.

## 5. Write the skill instructions

Write in clear imperative language and explain the reason for important steps. AI systems generally follow guidance better when they understand what a step protects: correctness, usability, privacy, safety, or efficient use of time.

Avoid long lists of unexplained absolute rules. Strong boundaries are appropriate for authorization, safety, privacy, data integrity, and irreversible actions. Elsewhere, give the AI enough judgment to adapt to normal variation.

A useful skill usually contains the following sections as applicable.

### Purpose and scope

State the job, intended outcome, intended users, and limits. Make clear whether the skill provides advice, produces an artifact, modifies a file, performs an external action, or guides a user through a process.

### Inputs and prerequisites

List required inputs, permitted sources, required capabilities, and optional context. Specify what happens when a required input is missing.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If the source is unavailable, ask for an export or provide a draft clearly marked as incomplete.
```

### Workflow and decision points

Provide the normal sequence and its important branches. A durable pattern is:

1. Inspect the request and available inputs.
2. Clarify only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the output against requested format and success criteria.
6. Present results, assumptions, sources, and unresolved limitations.

Use conditional rules for meaningful variation:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested change could overwrite important work or send information externally, explain the impact and request confirmation first.
```

### Output format

Use an exact template when consistency matters. For example:

```markdown
# [Title]

## Summary
[One short paragraph]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing input]
```

Do not impose rigid formatting when contextual adaptation is more valuable. In those cases, define goals, required content, and one or two short generalized examples instead.

### Quality, privacy, and safety checks

State the checks needed before completion. Examples include validating calculations, confirming required fields, preserving originals, citing key sources, separating verified facts from assumptions, and flagging unresolved uncertainty.

The skill must behave in ways a user would reasonably expect from its description. Do not create instructions that hide actions, bypass access controls, extract confidential information, damage systems, or facilitate unauthorized access. For people-related work, focus on role-relevant evidence, stated criteria, and appropriate access; avoid irrelevant personal details or unsupported labels.

### Failure behavior

Describe recovery in general terms:

- **Missing or conflicting inputs:** identify the gap and ask a focused question.
- **Unavailable tool or source:** explain what cannot be verified and offer an approved alternative.
- **Ambiguous request:** make a low-risk assumption only if it does not materially affect the result; otherwise ask.
- **Failed validation:** do not present the output as complete; correct it, label the limitation, or seek guidance.
- **Sensitive or high-impact action:** pause for confirmation before acting.

## 6. Write an effective description

The skill description is a routing instruction. It should state both **what the skill does** and **when it should be used**. Include realistic request contexts, including cases where the user implies the job without naming it.

A good description includes:

- The intended task or outcome.
- Common contexts or user language that indicate the task.
- Important scope limits that prevent costly false activation.

Example:

```text
Create clear project status reports from approved updates and source material. Use for requests involving progress summaries, leadership updates, milestone reviews, risks, blockers, or next steps, even when the user does not say “status report.”
```

Do not place the whole workflow in the description. Avoid vague labels such as “help with documents,” but also avoid making the description so broad that it captures nearby work better handled by another skill.

## 7. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description explain when to activate it?
- Are inputs, outputs, permissions, and dependencies clear?
- Does the workflow explain why important checks exist?
- Does it handle missing information and tool failure honestly?
- Are there repeated rules, unnecessary constraints, or brittle wording?
- Does it assume a particular person’s habits, access, tools, or vocabulary?
- Does it keep private information and external actions within approved boundaries?
- Does a capable AI have enough discretion to handle normal variation?

Prefer a lean instruction set over one filled with rules that do not improve outcomes. If execution traces later show that a section causes wasted planning or redundant work, revise or remove it.

## 8. Design realistic tests

After the draft is stable enough to test, create two or three realistic prompts. Share them with the user and invite corrections or additions before relying on them.

For each test, record a descriptive identifier, prompt, input files or context, expected outcome, and objective checks if appropriate.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates. Flag information you cannot verify.",
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful variation:

- A typical successful request.
- An incomplete or ambiguous request.
- A format-sensitive, policy-sensitive, or evidence-sensitive request.
- A realistic case that changes the workflow.
- A request requiring confirmation or safe refusal, when relevant.

Avoid tests that merely repeat the skill’s wording. Vary phrasing, detail level, and user familiarity. Avoid private or one-off scenarios unless they are fully authorized and necessary; test the broader challenge instead.

## 9. Run comparisons and preserve evidence

When independent execution is available, compare the skill to a meaningful baseline.

- For a new skill, run each test with the skill and without it.
- For a revision, save an unchanged snapshot before editing, then compare the revised skill with the earlier version.

Launch the skill and comparison runs under equivalent conditions. When parallel execution is available, start all configurations in the same evaluation round so conditions are comparable.

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

For each run, save the prompt, permitted input files, outputs, and available metadata such as elapsed time and resource use. Capture timing immediately if the environment reports it only at completion.

If independent comparison is unavailable, run a transparent sanity check: follow the skill for each test, preserve outputs, and ask the user to review them. Do not describe this as a rigorous baseline comparison.

## 10. Define, grade, and interpret checks

While runs are in progress, draft objective checks if they genuinely measure value. Explain them to the user before treating them as success criteria.

Good checks are observable and meaningful, for example:

- Required sections or fields are present.
- A produced file opens correctly.
- Calculations match an approved source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- Required citations, source notes, or approval prompts are included.

Record each check with clear wording, a pass/fail result, and supporting evidence:

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

Use scripts for checks that can be programmatically verified. They are faster, more repeatable, and reusable across iterations. Do not force numerical checks onto subjective work such as tone, visual quality, strategic judgment, or creative usefulness. Those need informed human review.

Aggregate available pass rates, time, resource use, and variation. Then inspect patterns the totals may hide:

- Checks that pass equally with and without the skill may not measure its value.
- High variation can indicate ambiguity, an unstable environment, or unreliable instructions.
- A quality gain may not justify excessive time or resource cost.
- Several failures may share one cause, such as unclear source selection.
- Repeated helper work may justify a script or template.

## 11. Review results with a human

Present outputs and measurements through an available review interface or, if necessary, directly in the conversation or accessible files. For each test, show the original prompt, relevant inputs, each output, grades and evidence, and available timing or resource data.

Ask focused questions:

- “Which output would you trust in normal use, and why?”
- “What was missing, misleading, or difficult to use?”
- “Did the skill add work or detail that was not valuable?”
- “Would this still work with different wording, data, or constraints?”

Human review should happen before making speculative corrections based only on the author’s preferences. Empty feedback can mean a test is acceptable, but it is not proof that the skill is complete.

## 12. Improve without overfitting

Revise from the combined evidence of feedback, outputs, execution behavior, and checks. Change the smallest part likely to address the underlying cause.

Generalize from complaints. If one output fails to distinguish verified facts from assumptions, do not add a rule tied only to that test. Clarify the broader rule: when evidence is incomplete or mixed, separate verified information, assumptions, and unresolved questions.

Use these principles:

1. Fix causes, not examples.
2. Keep instructions lean and remove unproductive guidance.
3. Explain intent rather than relying on rigid wording.
4. Add reusable resources only when repeated work proves their value.
5. Preserve behavior users already value.
6. Add tests only for real categories of failure.

After revision, rerun the full test set in a new iteration and use the same baseline policy. Show prior outputs alongside the new ones when possible.

Stop when the user says the skill is ready, feedback is consistently positive across meaningful tests, objective requirements are reliably met, further edits produce no meaningful gain, or remaining issues require a product decision or unavailable information rather than better instructions.

## 13. Optional blind comparison

For a rigorous comparison between two versions, provide their outputs to an independent evaluator without identifying which version created each one. Ask for judgment against a shared rubric, then reveal the mapping after the evaluation is recorded.

Use blind comparison when versions have similar formal results but differ in qualitative value, when a decision has material consequences, or when a newer version may be favored merely because it is newer. Evaluate correctness, completeness, clarity, adherence to constraints, safety, and practical usability.

## 14. Optimize activation after the workflow works

Only optimize the description after the underlying skill is useful. Create a realistic, balanced set of activation queries: some that should use the skill and some difficult near-misses that should not.

Positive queries should vary in wording, formality, implied versus explicit intent, and common versus uncommon valid cases. Negative queries should share concepts or keywords but belong to a different job, require another capability, or lack the conditions that make this skill appropriate.

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

Review the query set with the user. If evaluation tools support repeated trials, separate the examples used to improve the description from held-out examples used to choose it. Select based on held-out performance to reduce overfitting.

Remember that an AI may handle a simple one-step request directly even when a specialized skill matches. Use substantive activation tests where consulting the skill would offer real value.

## 15. Package and hand off

Package the core instructions and only the resources needed for ordinary use. If packaging tools are available, use the user’s chosen format and provide the resulting artifact or installation location.

Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on undeclared tools, private conventions, or personal access.
- Scripts, references, and assets are present, clearly named, and documented.
- No credentials, private identifiers, confidential records, or sensitive examples are included.
- The user can install, access, or adapt the skill in their chosen environment.
- Retained tests are safe and useful to distribute.

Provide a short handoff note explaining what the skill does, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an honest description that routes suitable requests, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user needs.


---
name: test-every-screen-size
description: Verify every UI and CSS change across representative screen sizes, realistic content, screenshots, and layout checks before completion.
---

# Test every screen size

Run this workflow after any UI, visual, or CSS change and before requesting review, publishing, or calling the work complete. Small edits to spacing, backgrounds, or sizing can create overflow, blank areas, wrapping problems, or collisions at sizes that were not inspected.

A layout passes only when **both** screenshots and programmatic checks pass. Measurements can miss visual defects; screenshots can miss off-screen overflow or unusable controls.

## 1. Prepare a representative state

Use an authorized test environment and test only the minimum data needed to reproduce normal use. Populate the changed surface with realistic content, such as long text, representative lists or cards, field values, and validation messages. Include loading, empty, or error states when the change affects them.

Do not test only an empty or unusually sparse page. Sparse states often conceal clipping, overlap, and unwanted blank space.

## 2. Select the viewport sweep

Use a repeatable browser-testing system. Start with these widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a wide desktop size, such as 1920 px, when large displays are a supported use case. Include any known target viewport.

When vertical behavior matters, test both a short and tall height, for example about 700 px and 1400 px or more. Explicitly include a very tall viewport for changes involving viewport-height sizing, flexible page shells, backgrounds, vertical padding, sticky footers, or bottom alignment.

## 3. Capture and inspect screenshots

Capture screenshots for each relevant viewport and state. Use visible-viewport screenshots for sticky, fixed, and viewport-height behavior; use full-page screenshots when page flow, backgrounds, or total page length matter.

Inspect the changed surface on all four sides: top, right, bottom, and left. Compare the result with the requested outcome, not merely with the edited CSS.

Give extra attention to full-bleed or edge-to-edge changes. Removing containment on one edge can reveal leftover wrapper margin or padding as an unintended strip on another edge.

## 4. Run programmatic layout checks

At every relevant viewport, verify that:

- there is no unintended horizontal overflow;
- viewport-fitting screens do not have unintended vertical overflow, allowing a small rendering tolerance;
- changed elements do not overlap adjacent content or escape their intended containers;
- buttons, links, fields, cards, and lists remain visible and usable;
- fixed or sticky elements do not hide required content; and
- prose remains readable rather than becoming excessively wide.

For prose, use an approximate warning threshold of 80 characters per line; reading-focused layouts commonly target about 60–70 characters per line. Check relevant bounding rectangles for overlaps and compare document height with viewport height where fitting the viewport is intended.

## 5. Resolve failures and retest

If any viewport or state fails, stop the completion process. Find the underlying layout rule, fix that behavior, and rerun the relevant sweep. Do not add a size-specific patch merely to make one screenshot pass.

If a fix improves one size but breaks another, revisit the diagnosis. The layout model or component constraints are incomplete.

## 6. Readiness gate and report

Do not report only that the interface works on “mobile and desktop.” State what was tested and what passed. For example:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall heights where relevant; screenshots and layout checks found no unintended overflow or overlap; controls remain usable.

If a viewport, state, or check was not run, state that clearly and do not represent the UI change as fully verified.


---
name: run-a-recurring-community-event
description: Create, publish, verify, and invite the approved audience to authorized recurring community events using adaptable tools, privacy-aware controls, and readiness checks.
---

# Run a recurring community event

Use this workflow to create the next authorized occurrence of a recurring social, sports, learning, volunteer, or community event. Adapt the steps to the organizer’s chosen calendar, event platform, artwork tool, file workspace, venue, and communication channels.

## 1. Set authority, purpose, and boundaries

Choose the operating mode before taking external action:

| Mode | Permitted action |
|---|---|
| Prepare only | Create materials and an unpublished draft. |
| Review before publish | Prepare the event, then obtain approval before publishing or inviting. |
| Standing authorization | Publish and invite within a documented recurring-event policy. |

A standing policy should specify the event series, recurrence, normal hosts, intended audience, platform, approved content, and permitted communication actions. Ask for a decision when an occurrence would materially change the audience, price, privacy setting, venue, safety plan, accessibility arrangement, or event format.

When accessing calendars, guest lists, prior invitations, host availability, or contact details, confirm a legitimate operational purpose and clear authorization. Use only the minimum sources and personal information needed to schedule, create, verify, or invite for this occurrence.

Keep sensitive personal information out of event text, artwork prompts, public descriptions, and routine reports. This includes health information, precise private location details, personal contact information, attendance history beyond what is needed for the invitation policy, and private availability explanations. Do not infer or expose a person’s identity, preferences, relationships, or circumstances from event records.

Respect opt-outs, consent expectations, platform restrictions, and the access boundary of the event. Send invitations only to the approved audience. Do not export, reuse, or share attendee data outside the authorized event-management context. Keep reports appropriate for their recipient: an organizer may need operational counts and exceptions; public attendees generally do not need participant lists or personal explanations.

## 2. Determine the next occurrence

Calculate the next date from the recurrence rule and local time zone using a reliable calendar or date capability. Do not rely on mental arithmetic. Confirm the weekday, date, start time, end time, venue, host arrangement, and sequence number.

If the series is numbered, inspect prior events and use the integer after the highest existing number. Include early unnumbered occurrences when they are relevant to the series history or approved invitation policy.

Check practical conflicts, such as venue closures, host unavailability, holidays, severe-weather risk, or relevant calendar overlap. A conflict does not automatically cancel the event. Apply the organizer’s policy. If the event proceeds, report the conflict at an appropriate level of detail and identify any remaining handoff or cancellation decision without disclosing unnecessary personal information.

## 3. Reuse stable details and update changing details

Review one or two recent occurrences before building the new event. Separate stable information from occurrence-specific information.

| Information type | Examples |
|---|---|
| Stable | Purpose, usual meeting point, general format, approved contact route, accessibility guidance, and approved wording. |
| Occurrence-specific | Date, number, hosts, route, seasonal plan, capacity, special instructions, and exceptions. |

Use the approved title pattern and description template. Update every date-sensitive and occurrence-specific detail deliberately. Do not carry forward stale dates, expired links, temporary notices, outdated directions, or prior availability statements.

Use a description structure such as:

```text
[Brief invitation or purpose]

Meet at: [exact meeting point]
Time: [arrival or start guidance]
Format: [activity, duration, pace, or expectations]
Afterward: [optional social or follow-up plan]

[Accessibility, preparation, contact, or RSVP guidance]
```

Keep the description clear, current, and suitable for the event’s visibility. Include only links and contact routes approved for that audience. Do not publish private group links, private photo collections, or contact details unless the organizer has authorized their sharing with the event audience.

## 4. Prepare fresh artwork when needed

If the series uses recurring artwork, retain a recognizable identity while making each occurrence visibly distinct. Review recent images first. The goal is a new central idea, not a minor variation on the previous image.

Create an image brief containing:

- required event text, if any;
- the core activity or recognizable symbols;
- desired mood and visual style;
- one clear focal concept;
- a simple composition and restrained palette; and
- quality requirements, such as readable typography and no visible generation defects.

Vary the concept through season, weather, light, viewpoint, local texture, an activity detail, or one small humorous object. Prefer one strong subject over a crowded montage. Do not use identifiable attendees, private venues, or personal details in artwork unless there is clear permission and a suitable distribution boundary.

Review the result before upload. Regenerate with a changed concept if it repeats recent work, is cluttered, has illegible text, or contains obvious artifacts. Use a limited retry budget; if no usable asset is available, use an approved fallback or request a decision.

Export the chosen image to a workspace accessible to the event platform. Confirm the file exists, is the intended version, and displays acceptably after platform cropping or compression. If a tool reports a generation or download error, inspect the asset area before retrying because the result may still have completed.

## 5. Create the event

Use the authorized organizer account and verify the active account before editing. If different tools require separate accounts or browser contexts, verify the correct account after every switch.

Prefer a draft or preview when available. Some platforms publish through controls labeled “Save,” “Done,” or similar, so determine the effect of the final action before using it.

Complete fields in this order when practical:

1. **Title:** Apply the approved pattern, such as `Community Event #N`.
2. **Date and time:** Set the date, start time, end time, and time zone.
3. **Location:** Select the exact venue or map result, not a similarly named listing.
4. **Description:** Apply the current approved template and updates.
5. **Image:** Upload the selected asset and inspect its display.
6. **Hosts:** Add only authorized hosts or co-hosts.
7. **Settings:** Confirm visibility, capacity, cost, RSVP rules, notifications, and accessibility information.

Dynamic forms require defensive verification. Complete date and end-time selection before editing unrelated fields, then confirm the displayed attendee-facing value. Re-check visible state after a menu opens, an upload completes, the page loads more content, or the layout shifts. Prefer controls identified by labels, roles, or current state rather than fixed screen coordinates.

Wait for an image upload to finish and verify the new image before editing another section. If a required field cannot be verified, correct it, use a safe fallback, or request a decision; do not claim readiness.

## 6. Verify and publish

Review the draft or preview as an attendee would. Confirm:

- title and occurrence number;
- weekday, date, start time, end time, and time zone;
- exact venue and map pin;
- description, links, and contact information;
- image presence, crop, and legibility;
- host or co-host status; and
- visibility, capacity, cost, and RSVP settings.

Publish only under the selected authority mode. Then open the live page and repeat the attendee-facing checks. Save the live URL. If publishing behavior or live-page verification is unavailable, state that limitation clearly.

## 7. Invite the approved audience

Follow the documented invitation policy. Prior attendees of the same series may be an approved audience, but this is never an automatic default. Do not broaden the audience using unrelated records, inferred interests, or personal relationships.

When inviting people from prior occurrences, process only the qualifying events and only the fields needed to identify eligible invitees. Avoid downloading or copying guest lists unless necessary and authorized. Respect opt-outs, consent boundaries, privacy expectations, and platform restrictions.

1. List the qualifying prior events.
2. Process one event or group at a time.
3. Check current selection before using a bulk-select control.
4. Add eligible invitees, clear the filter or group view, and continue.
5. Verify that the invitee count rises by a plausible amount after each group.
6. Stop and inspect if the count drops or remains unchanged unexpectedly.
7. Send only when authorized, then confirm the sent state or final invited count.

Platforms may preselect people or deduplicate repeated attendees. A bulk action can therefore remove selections if used without checking. Re-check after delayed loading, list refreshes, or layout changes. If delivery confirmation is unavailable, report that limitation rather than implying that invitations were delivered.

## 8. Completion report and maintenance

Provide a short operational report containing:

- what was created and whether it was published;
- date, time, and venue;
- invitation outcome or current invitee count;
- conflicts, unresolved items, or nonstandard settings; and
- the live event URL.

Share the report only with authorized recipients. Report aggregate invitation outcomes rather than attendee names or private attendance details unless a recipient has a legitimate need and permission to receive them. When the URL must be easy to copy, put it on the final line with no text after it.

After each occurrence, retain only reusable lessons: platform behavior changes, durable audience rules, template updates, reliable field order, and content preferences. Keep one-time facts and personal data separate from the recurring workflow. Update the process when interfaces change, but never silently broaden authorization, access, retention, or the invitation audience.

## Readiness gate

Before declaring completion, confirm:

- The date and sequence number were calculated and checked.
- The organizer account and live event page were verified.
- Stable information is current and occurrence-specific details were updated.
- Artwork is fresh, usable, correctly uploaded, and appropriate for the audience when required.
- Time, venue, hosts, and settings are confirmed.
- Invitations followed the approved audience policy and respected opt-outs.
- Personal information was minimized, sensitive details were excluded from public outputs, and the report stayed within its access boundary.
- Publishing and invitation results were verified, or verification limits were clearly reported.

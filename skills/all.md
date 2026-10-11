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
description: Search only the sources likely to matter, at an effort level matched to the stakes, and turn the findings into one concise, well-sourced context brief.
---

# Gather context

Use this workflow to build a well-sourced context brief on a person, organization, project, topic, or decision. Search only the sources that plausibly hold relevant information. Then combine the findings into one organized brief with direct links to the evidence.

Typical requests include "gather context on X", "what do we have on X", "pull everything about X", "get me up to speed on X", "what's the latest with X", and "background on X before my call". The user usually wants this before acting: writing, deciding, meeting, pitching, hiring, or catching up.

If the user wants a structured meeting-preparation document, such as an agenda page, use a dedicated meeting-prep workflow if one exists. This workflow gathers raw context. If it is unclear which the user wants, ask.

## The most important rule: right-size the effort

Match the depth of the search to what the user actually needs. "Remind me where we are with X" needs a quick look at two or three obvious sources and a short answer. "Deep-dive on this partner before a major decision" needs a broad search. Most requests fall in between.

There are two failure modes, and both are bad:

- **Over-gathering.** Querying every connected system, starting many parallel workers, and writing an essay when the user asked a quick question.
- **Under-gathering.** Checking one source, finding a few messages, and stopping when the request clearly needed more. The key fact is often in a chat thread or meeting record the user forgot about.

For each source, ask: *for this specific request, would a sensible researcher think it is worth checking here?* Both relevance and effort level limit breadth. Skipping an irrelevant source is good judgement, not laziness.

## Step 1: Set purpose and access boundary

State the decision, task, or question the brief must support. Use private sources only when the user is authorized to access them and they are relevant to that purpose. Having access to a source is not, by itself, a reason to search it.

When the subject is a person, apply a stricter boundary:

- Use the minimum sources and information needed for the stated task.
- Do not search private messages or records just because they are available.
- Leave out unrelated or sensitive personal details. Do not guess at private or protected traits.
- Respect consent, confidentiality, need-to-know limits, and the person's reasonable privacy expectations.
- For hiring or assessment, focus on role-relevant capabilities, diagnostic evidence of past work, and how well the person's experience aligns with the role's actual requirements. Use only the hiring records the user is permitted to see.
- Put the brief only where its audience is allowed to see the source material.

If the purpose, authorization, or destination is unclear, settle it before searching private sources.

## Step 2: Scope the request

### Pick an effort level

| Level | When to use | What to do |
|---|---|---|
| Quick | Status check or "remind me" | Check the one to three most obvious sources, one pass each. Answer in a few lines. Search directly; no parallel workers. |
| Standard | The common case | Check a handful of relevant sources with a couple of queries each. Write a tight brief. Use parallel workers only if they clearly save time. |
| Deep | High stakes: major decision, big pitch, key hire | Search broadly, use parallel workers if available, run several queries per source, and verify important claims. |

If unsure, choose the lighter level and offer to go deeper. Escalating is cheap; an oversized search is expensive. State your chosen level in one short line so the user can redirect, for example: "Quick look across email, chat, and notes. Say the word if you want the full sweep."

### Classify the subject

The subject type tells you which sources matter most.

| Subject type | Likely sources |
|---|---|
| Person (partner, funder, contact, candidate) | Email, chat, notes, calendar and meeting records, public web and professional profiles; the hiring system only if the request is hiring-related and authorized |
| Company or organization | Public web first; then email, chat, and notes for any existing relationship; relationship or partner databases if they are a partner or prospect |
| Project or initiative | Notes and wiki, chat, shared documents, operational databases, task records, code repositories, product analytics if metrics matter |
| Topic or question | Several web searches from different angles, plus internal documents and chat for prior thinking |
| Decision | Any of the above, organized around the options and the evidence for and against each |

### Clarify only when needed

If the subject is truly ambiguous, such as a bare name that could be several people or a one-word topic with several meanings, ask **one** short clarifying question before searching. A wrong-target search wastes many tool calls. If the subject is clear, start. Do not over-ask.

### Treat named sources as a floor

If the user names sources ("search my email and online"), those are required, but they are not the full list. If another source clearly holds decision-relevant context, check it too.

The most common example: **if the results show, or the request implies, a recent conversation with the subject, read the notes or transcript of it.** A calendar invite or a "good to meet you today" message is the signal. A record of what was actually said is often the richest single source.

### Set the time window

Use the window the user gives. If none is given, a reasonable default is the last six months, extended further back when the relationship or project is older.

## Step 3: Search the chosen sources

For quick and standard requests, search directly so you see results as they arrive. For deep requests, or when many sources are involved, run searches in parallel if your tools allow, one per source or source cluster. Each parallel search should return a short digest with links, not a raw dump.

Depth within each source also scales with the level. In a deep search, query by name, organization, project keyword, and related people, and do not conclude "nothing there" until you have tried the available search tools. In a quick search, one or two well-chosen queries on obvious sources is the correct amount.

### General search principles

- **Search for mentions, not just direct contact.** In email and chat, direct correspondence shows the relationship; keyword and name searches show how others discuss the subject.
- **Know your tools' blind spots.** Default search modes, readers, and labels can hide content. A "smart" search may bury results under low-value items; a document reader may return only the first tab, section, or sheet; transcript speaker labels may be wrong; auto-filled fields such as timestamps may be placeholders. Prefer the plain or complete option, read every part of a document, and note where each finding came from.
- **Use maps before crawling.** If a schema map, data dictionary, or index exists for a database or workspace, read it first so you go straight to the right place.
- **Weigh data quality.** Some systems are more reliable than others. Verify records from weaker systems, and ask before relying on sandbox, temporary, or low-priority copies.
- **Check freshness.** Confirm role and title claims against dated, current sources rather than old snapshots. Treat stored assistant notes as true when written, and confirm any file, setting, or record they name still exists.
- **Use conditional sources only when they fit.** Hiring systems for authorized hiring questions, product analytics when numbers help, code history for engineering subjects, and the user's own task or journal records when the subject is their own work.

### Handle missing or failing sources honestly

- **Never invent a link.** Include only links you verified or the user supplied. Otherwise omit the link and flag it. Cite items with links the user can open, not bare internal IDs.
- **Do not silently substitute sources.** If a source you judged relevant returns nothing or is unavailable, say so in the brief.
- **Try to fix tool failures first.** Attempt safe diagnosis and repair before involving the user. Ask the user only for a step that truly needs them, such as a login or restart, and report the exact failure, what you tried, and the one remaining action.
- A source you deliberately skipped as irrelevant is not a gap. Just do not imply you checked it.

## Step 4: Synthesize into a brief

- **Resolve contradictions.** Do not list conflicting claims without comment. Example: "An older article says they work at Organization A; their current profile says they left in March. The profile is newer, so I trust it."
- **Prefer primary and current sources.** Treat discussion and summaries as weaker than recorded decisions.
- **Lead with what matters for the user's next action.**
- **Organize by theme, not by source.**
- **Link every sourced claim.** A quote without a link is not done.

### Output template

Adapt headings to the subject. The core structure is:

```markdown
## [Subject] — context brief
*Searched: [sources]. Window: [dates]. Effort: [quick/standard/deep].*

## Summary
Three to five bullets: the most decision-relevant facts.

## What we know
Who or what this is, current state, history. Grouped by theme, with inline links.

## Relationship and timeline
(For people and organizations) How the user's organization connects to them; chronology of contact.

## Open questions and gaps
What no source answered, and which source you would expect to hold it.
Any relevant source that was unavailable or returned nothing.

## Sources
Key links, grouped, so the user can dig in.
```

Match length to depth. A quick check gets a few lines; a deep dive gets the full structure. This is a scan-and-act document, not an essay.

## Step 5: Deliver the brief

Follow the user's stated preferences for where briefs go and how they are named. If none exist, use these defaults:

- **Short brief** (fits on one screen): put it directly in the reply.
- **Long or reference brief:** save it as a document in the location the user chooses, if access rules allow. Give it a concise, specific, human-readable title, such as a date plus a headline. Avoid filename-style slugs and type labels. In the reply, give a short summary of key findings and the document link.

Make the deliverable easy to find and copy. Put follow-up offers ("Want me to draft the outreach email too?") before the brief rather than after it, and avoid trailing commentary that buries the result.

If you write into an existing formatted document, verify the result at the formatting level, not just as plain text. New text can inherit the style of where it was inserted, so insert into plain body paragraphs or replace whole sections, then re-read the affected range in a view that shows styles before reporting the edit complete.

## Final checklist

| Check | Pass condition |
|---|---|
| Purpose and access | Legitimate purpose stated; private sources used only with authorization and relevance |
| Effort level | Level stated in one line and matched to stakes |
| Source selection | Named sources covered; clearly relevant extras added; recent conversation records read |
| Honesty | Gaps and failures reported; no invented links; skipped sources not implied as checked |
| Synthesis | Organized by theme; contradictions resolved; every claim linked |
| Privacy | Unrelated or sensitive personal details omitted; destination fits the audience |
| Delivery | Matches user preferences; brief easy to find; follow-up offers placed before it |


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
description: Review the past week, shape one to three verifiable goals through focused interview rounds, then turn them into approved tasks, calendar blocks, and a one-screen plan.
---

# Plan your week

Plan the coming week as a deliberate shaping session. Research sets the constraints. A few interview rounds, each built on the last set of answers, find out what actually matters. Only then turn the result into a short written plan, approved tasks, and approved calendar blocks.

Aim for about an hour. This ritual anchors the week, so it may run longer when the shaping needs it. The conversation does the hard work. The final plan should feel simple.

## Core principles

1. **Pressure is not importance.** A deadline, a stale task, a senior counterpart, or a visible event is evidence of pressure. It is not evidence that something deserves to be a weekly goal. Never recommend a goal only because it is scheduled, overdue, or easy to make concrete. The user must first say what they want to make true, why it matters now, and what they will deprioritize for it.
2. **Evidence prompts questions; it does not answer them.** Sources can show deadlines, obligations, slippage, and capacity. Only the user can say what they value this week.
3. **Complex conversation, simple output.** Keep research detail, task metadata, and calendar mechanics out of the final plan unless they change a decision.
4. **Propose, approve, then write.** Every goal, task, status change, and calendar event is written only after the user approves that specific item. Never batch-create.
5. **Ask or search; do not guess.** If the user mentions an unfamiliar name, project, or reference that affects goals, the calendar, or a rollover decision, run one or two quick searches in authorized sources. If it is incidental, move on.
6. **Check that stored context is still true.** Notes like "delegated until X happens" or "paused for two weeks" expire. Before citing one, check whether its trigger has passed. If the user corrects a stored note, update it in the same session.

## Privacy and access boundary

This workflow may touch calendars, messages, tasks, health data, and records about colleagues or candidates.

- **Purpose and authorization.** Read only sources the user has connected and agreed to use for weekly planning. Health, sleep, and exercise data are opt-in.
- **Minimum necessary.** Prefer counts and metadata over contents. For email and chat, counts and days-waiting are usually enough. Open a message only when the user asks or one specific item is needed for a decision.
- **Private writing stays private.** Do not read or quote a freeform private journal unless the user shares it in the session. Use structured fields instead (daily plans, ratings, stated reasons, fields the user designates for brain dumps). If a source mixes private text with planning data and you cannot exclude the private part before reading, skip that source.
- **Other people.** Mention colleagues and candidates only as far as the decision needs. Keep health, emotional, and personal details about others out of the plan. Write "rebalance workload for the operations lead", not why they are struggling.
- **Output boundary.** The plan lives in the user's own system. Do not copy colleague or candidate details into shared spaces. Draft messages for the user to send; never send on their behalf.

## Setup: user choices

Ask once, store the answers, and reuse them. Offer the default when the user has no preference.

| Choice | Broadly useful default |
|---|---|
| Planning day | Last workday of the week, or Sunday evening |
| Week boundaries | Monday to Sunday |
| Maximum weekly goals | 3, with 1 as the ideal |
| Unplanned buffer | 20% of free working time |
| Planning system | The user's task manager, notes app, or spreadsheet |
| Calendar conventions | Solo work as focus-time events in a distinct colour; plain titles |
| Time zone | Ask; restate it to any helper that reads the calendar |
| "Behind" thresholds | Email older than 48 hours; direct messages unanswered over 3 days |
| Health floor | User-defined sleep, exercise, and recovery targets, or none |
| Chronic-deferral threshold | Tasks deferred more than 5 times move to a parked list |
| Workflow self-improvement | Note lessons at the end; ask before structural changes |

## Deliverables

The session is complete only when these exist, or the user has explicitly waived one:

1. Up to three weekly goal records, each linked to a longer-term goal, each with a definition of done of two to four checkable outputs.
2. The target week's plan record holding the simple plan, and the previous week's record holding the user's review answers.
3. Task records, created or updated in place, for every concrete chunk of work each goal needs. Each is 5 minutes to 3 hours, clearly titled, with prepared notes, and approved individually.
4. Calendar events, each slot approved, for goal and task blocks and protected routines.
5. Status updates for overdue tasks the user decided on (unless they triage themselves).
6. Drafted messages for any meetings the user chose to cut or move.

Analysis without these artefacts is not a finished weekly plan.

## When to use and which variant

Use this when the user asks to plan the week, or to review and plan it, and on their planning day. Any request that combines reviewing and planning the week belongs here, not in a daily review.

Default target: the week starting next Monday. On a Monday, the current week.

| Situation | Adjustment |
|---|---|
| End-of-week run (default) | Review the current week as "last week". Ask what must still ship before Monday and treat it as current-week work, not a next-week goal. |
| Run on the first day of the target week | Ask early, "What must ship today?" and build that day first. Re-read calendar and task status before writing. |
| Belated mid-week run | Plan only the remaining days. Treat elapsed days as review context. State the runway up front. |
| Time-off week | Skip goals, tasks, hiring, and cuts. Confirm recurring meetings are declined. Plan rest and logistics in whatever document the user names. |
| User is exhausted | Stop open questions. Offer 2 or 3 concrete options, or decide with stated reasoning and let them veto. |

## Hard rules

- **At most three weekly goals.** Merge, demote to intentions, or defer the rest. With three, label one the stretch goal. One is ideal.
- **Definition of done a teammate could verify:** two to four concrete outputs, such as "Sent version 2 of the scorecard and job description to the hiring partner." "Everyone in the process has next steps" is binary but unscoped. A direction is not a goal.
- **The week fits with the buffer unplanned.** If it does not fit, cut or shrink a goal. Never shrink time estimates.
- **Every goal links to an active longer-term goal.** Ask "Which longer-term goal does this serve?" A weak answer means reject.
- **Use the existing week record** if one exists; it may already have goals linked. Create one only if missing.
- **Write task status after each decision**, not all at the end.
- **No goal proposals before two substantive, answer-dependent interview rounds**, unless the user asks to skip questions. Each round resolves a different layer.
- **Keep an alignment ledger.** Show it compactly before each later round. Never reintroduce a corrected assumption.

## Generic data model

Map these to the user's systems. Field names are suggestions.

| Record | Key fields |
|---|---|
| Plan (week, month, quarter, year) | type, start, end, linked goals, plan text, review text. Higher levels hold theme, non-negotiables, any scorecard. |
| Goal | statement, deadline, status, priority, level, linked plan, notes ("Links to" and "Done when"), deadline-change count |
| Task | name, due date, status (todo, in progress, done, parked, archived), importance, urgency, estimate, notes, deferral count |
| Daily log | date, daily plan, overall rating and reason, focused hours, intention for tomorrow |
| Recovery and exercise (opt-in) | per night: hours asleep, hours in bed, device score, variability; per session: date, type, volume |

Useful saved queries: current and previous week records, active higher-level plans, active longer-term goals, last week's goals with a four-week hit rate, overdue and due-soon tasks, parked tasks (titles and deferral counts only), recent daily logs, and the last two weeks of recovery and exercise data.

## Step 1: Gather context

Run reads in parallel. Delegate anything likely to be large (a full week of calendar events, a long parked list, a hiring pipeline) to a helper with a tight brief and a word limit, and ask for only what a decision needs. Bound each helper's runtime. If a call fails twice, record the gap and move on. Never present partial data as complete.

Read:

- **Planning records** from the data model above.
- **Team context (read-only):** current sprint or planning page, active team goals, projects the user owns. If the team held a goal-setting meeting today, read only the user's own review answers and shortlisted goals.
- **Calendars:** the target week, via a helper that returns meetings per day, non-trivial meetings as "date, time — title (counterpart role)", weekend conflicts, and cut candidates, in under 400 words. Read personal and social calendars if authorized; never block work over personal events. Treat unconfirmed invites as unconfirmed and sanity-check imported time zones.
- **Inbox signals (counts only):** email past the threshold and in total, the chat action queue, unread direct messages and mentions, and unanswered direct messages with days waiting. Count threads, not messages. If a result hits its cap, report ">N".
- **Opt-in signals:** recovery data, completed and prescribed training, hiring load (see below).

## Step 2: Recap, the user's review, then the brief

Run these in order: short overview, the user's own review, then your analysis.

**a) Recap, five lines maximum, no analysis:** active longer-term goals with countdowns; last week's goals as done, missed, or open; four-week hit rate ("3 of 7 goals hit"). Open goals past deadline count as missed unless the user says they shipped.

**b) The user's review.** Ask in one block, then end your turn:

1. Did you hit your goals for the week?
2. What went well?
3. What didn't go so well?
4. What will you do differently next week?

If they already answered at a team meeting, quote their answers and ask only what changed. The aim is one thing to change, not blame. Save the answers to the reviewed week. Carry "do differently" into shaping and the failure-mode line.

**c) The brief.** Synthesize internally. Show at most eight bullets, only facts that could change a decision. Group routine signals; foreground tensions, surprises, real constraints, and data gaps. Do not recommend goals. Check these areas and include only what matters:

- **Rollover and slippage:** each unfinished goal with its deadline-change count. Anything open after four or more changes gets the question: "This has slipped N times. Is it still the right goal, or is the format, scope, or lane wrong?" Raise it here, not an hour in.
- **Close-out:** did end-of-week items actually ship? Ask rather than assume.
- **Capacity:** meetings per day, energy, sleep, focused hours, training (thresholds below).
- **Backlog:** overdue count, important-and-time-sensitive count, and one to three parked items that now fit (or "none fit").
- **Messages:** what is past the thresholds. A non-empty action queue is not failure; stale items with no owner are.
- **Commitments that may not be on the calendar:** externally dated work such as a program cohort the user must onboard or a registration window. Check the relevant records or ask. These beat self-set goals on timing.
- **People:** team goals that imply user action; a colleague the user has said is overloaded (ask at goal-setting whether reducing that load is the real priority); two or more recent joiners (ask whether onboarding is scheduled).
- **Non-negotiables:** hits and misses against the current higher-level plan.

### Signal thresholds (defaults; let the user set their own)

| Signal | Flag when | Notes |
|---|---|---|
| Energy | 2+ clearly negative days in 7, or a run of neutral ratings | On a -2 to +2 scale, neutral often hides a bad day. If logs are blank, say so and name the fallback signals used. |
| Focus | Focused work trending under about 3 hours a day | Context, not a verdict |
| Sleep | Any night under 6.5h asleep; 3+ nights under 7h; variability below 90% of last week; device score average under 75 | Use time asleep, not time in bed. Compare variability only within one device and method. |
| Training | Sessions below target, or the key session missed | Zero sessions for two weeks usually means a sync gap; ask before concluding |
| Meetings | Days over 4 meetings | Also note meeting-free days |
| Messages | Items past the user's "behind" thresholds | Report counts and days waiting |

Report fired flags with numbers and dates ("3 nights under 6.5h: Mon 6.4, Wed 6.2, Thu 6.3; average 6.7h"). Vague phrasing is not acceptable. Do not average across missing nights after travel or device changes; call it a device gap. After crossing time zones, frame short nights as circadian adjustment, not bedtime discipline.

### Hiring load (if the user hires)

The purpose is allocating the user's time, not assessing anyone. Ask a helper for a report under 250 words:

1. Confirmed interviews this week with the user as interviewer, with day, time, role, and total hours. Exclude "needs scheduling" placeholders. If the query fails, use the calendar.
2. Late-stage candidates whose decision may be owed. Measure time in stage only from the real stage-entry date, never the application date, which makes everyone look overdue. If entry dates are unavailable, report stage counts only and say so.

If decisions are past the user's service target (a common one is five days, ideally two) or interviewing exceeds about three hours, name the cost of delay and ask who owns the response. Propose a block only after the user confirms hiring belongs on their week. Say "none overdue" when true. Keep candidate details and evaluations out of the plan.

### Alignment ledger

End the brief with this, and update it before each later round:

- **Confirmed:** choices the user made in this conversation, or current agreed plans.
- **Source facts:** constraints and evidence.
- **Inferred:** your tentative interpretations, labelled.
- **Open:** decisions only the user can make.
- **Corrected:** assumptions the user rejected (omit if empty).

## Step 3: Rollover decisions

Last week's goals may be goal records or freeform lines in last week's plan text; check both. Before treating an item as unfinished, check whether it was **delegated** (then it is not a weekly goal; note the handoff) or **already done** (records go stale; propose marking it done).

For each item still on the user, ask separately: **roll over, demote, or drop.**

- **Roll over:** a candidate goal. Ask "Why did it slip?" and log one line. Increment the change count and set the new deadline.
- **Demote:** an intention in the plan text, not a goal.
- **Drop:** mark missed or archived.

## Step 4: Shape the week through interview rounds

**Check for a plan of record first.** A recent written priority list, or goals shortlisted at a team meeting, outranks anything inferred from tasks. Ask "Is there a written plan of record?" Treat shortlisted goals as decided: check each has a verifiable definition of done and fits the week, then mirror them into goal records.

**Question format.** Ask 4 to 8 questions per round. Number every question. When options are bounded, letter them and put your recommendation first. One decision per question, so the user can reply "1a, 2c, 3 skip". Example:

```text
1. Which area most needs attention this week?
   a) Shipping the proposal (recommended: it is the open longer-term goal)
   b) Hiring decisions
   c) Recovery
2. What would you regret neglecting even if the proposal ships?
```

**Round 1: brain dump, then desired change.** Ask for a quick, unfiltered list of everything they might work on, task-shaped or vague. Group it by goal or project and show it back in a few lines, so the chosen goal is not just their first idea. Park small items for triage. Then work backward:

- What outcome would make the week genuinely matter?
- Why does it matter now, beyond a deadline?
- What has changed since last week's plan?
- Which area (work, personal, health, relationships) most needs attention?
- What is strategically or emotionally unresolved?
- What would you regret neglecting even if the visible work shipped?

Do not answer these from sources. Classify each answer as confirming, rejecting, softening, qualifying, or deferring your current model. Trace the implications and show the updated ledger.

**Round 2: shortlist.** Apply the prompts that bite this week:

- What can you do best, and what could someone else do as well?
- What would most move the team's main goal or the relevant longer-term goal?
- What benefits most from lead time?
- What unfinished work will keep stealing attention unless closed now?
- What is the strongest case for not doing this?
- Which fires are you willing to let burn?

Also settle real capacity (meetings, energy, sleep, exercise) and which commitments depend on others. Everything not shortlisted goes to "Not this week" or a "Later" list.

**Round 3, when needed:** if sequencing, success criteria, ownership, or the week's shape is still materially open. If the user is tired, narrow to two or three options; fatigue is not permission to revive an earlier inference.

### Readiness gate

Propose goals only when every item is confirmed, established, or deliberately left open:

| Gate item | Status |
|---|---|
| The one change that would make the week worthwhile | [confirmed / open] |
| Why it matters now | [confirmed / open] |
| The longer-term goal it serves | [confirmed / open] |
| Definition of done: 2–4 verifiable outputs | [confirmed / open] |
| Main competing claim on time or attention | [confirmed / open] |
| What is explicitly not advancing | [confirmed / open] |
| Realistic health and energy floor | [confirmed / open] |
| Most likely failure mode | [confirmed / open] |

For each candidate goal, ask yourself: did the user call this important, or am I promoting a visible deadline? If the latter, ask another question. Then propose the smallest set of goals that expresses the alignment, usually one or two, each in one sentence.

### Validate each goal

- **Links up:** name the longer-term goal and record it.
- **Verifiable:** two to four outputs. Narrow a direction to a named set and a named output.
- **Scoped:** sketch sub-tasks with rough hours and sum against free time minus the buffer. Under an hour is a task, not a goal.
- **Realistic:** heavy meetings plus low energy means cut one.
- **Stretch:** with three goals, mark one that may give way.

### Shaping rules of thumb

- **Shrink scope when the pattern says so.** If the current higher-level plan has a cut-scope rule that keeps firing, or goals keep slipping, default to one goal and ask what has changed before accepting more.
- **Name the kind of week.** If meetings, hiring, logistics, or supporting colleagues dominate, ask whether they want a people week or want to cut enough to protect one deep goal. "Defend harder" usually fails; ring-fence one deep item on the cleanest day.
- **External deadlines go first.** With two or more goals, ask which has the harder external deadline. It ships first, even if the other feels heavier or has rolled over longer.
- **Team goals need an announcement.** If a goal needs the team, ask what end-of-week goal to give them and where to announce it. Offer two or three framings with a recommendation and draft the message.
- **Respect the soft stop.** If after two or three rounds of pushback the user says "stop arguing, write it down", accept and move on. Record your concern in the failure-mode line.
- **Be firm when it helps:** "That's four goals; pick three." "You said this three weeks ago. What's different?"

## Step 5: Non-negotiables

Check whether the current quarter or month plan lists non-negotiables or a scorecard. If one exists, score its own lookback with its own items and threshold, and raise any fired cut-scope rule during shaping. If an item is out of date, update the higher-level plan after approval, not just this week. If no current plan exists, say so once and ask what minimum health, relationship, and recovery floor they want. Never revive an expired scorecard.

Honour explicit pauses: do not re-propose a paused habit or retired experiment; ask at most once whether it is back. Check that a protected day (writing day, rest day) is actually free before relying on it.

If a non-negotiable is faltering, ask up to three follow-ups until the user names **a specific action plus a day and time.**

| Quality | Example |
|---|---|
| Accept | "Phone out of the bedroom from Tuesday; wind-down alarm at [time] each evening." |
| Accept | "Long run Saturday at [time]. Mobility session Thursday after lunch." |
| Reject | "I'll try to sleep more." |
| Reject | "I'll exercise more this week." |

**When sleep is flagged:** lead with the numbers and the user's target. Protect their normal sleep window rather than moving it; cap any shift at about 30 minutes earlier, since large shifts under load rarely hold. Require both a bedtime and a wind-down trigger, because the hour before bed is what fails. If the same issue appeared last week, ask what is actually different. Record the commitment word for word so next week can compare.

## Step 6: Cut the calendar

Ask first: "Do you want to cut meetings this week, or keep them all?" If keep, note "No cuts" and skip.

Otherwise, for each meeting ask whether it serves a weekly goal, a non-negotiable, or a team commitment. If none, it is a candidate. The user decides per meeting: keep, cut, shorten, or reschedule. Draft a short, warm, specific message for each change; the user picks the channel and sends it. For recurring meetings someone else organizes, the action is a message to the organizer, not a calendar edit.

## Step 7: Task triage

Ask whether the user wants to triage themselves. If yes, note it and skip the writes. If they pause mid-session to clear loops, re-read tasks and inboxes live before advising. Do not park tasks the user called important; give them dated slots. Check who is responsible before suggesting delegation.

**First pass:** offer tasks past the deferral threshold as one batch: "These N tasks have been deferred 5+ times. Move to parked?" Default to parked, not archived.

**Second pass, one by one**, sorted by importance, urgency, then age:

| Decision | Write |
|---|---|
| Do this week | Keep todo; due date in target week; candidate for a block |
| Already done | Mark done |
| Punt | New due date; increment deferral count |
| Delegate | User names the role or person; note "Delegated to [role] on [date]" |
| Delete | Archive |

Write after each decision; small batches are fine if the user is moving fast.

## Step 8: Pre-mortem and deprioritize

Do this before blocking time, so the answers shape the blocks.

- **Pre-mortem:** "If this week fails, what is the most likely reason?" One to three lines.
- **Deprioritize:** "What can you delete, delegate, reschedule, or reset expectations on? What in-flight work will you explicitly not push this week?" Pausing one parallel stream helps the others ship.

## Step 9: Break goals into tasks

For each goal, propose one to five tasks of 5 minutes to 3 hours that together complete it. Also add tasks for "do this week" triage items, delegation follow-ups, and meeting prep that needs its own time.

- **Hold creation when a decision is pending.** If an upcoming decision could reshape a goal, create only tasks that survive either outcome.
- **Use a compact table for four or more tasks** (number, task, due, estimate, owner). Write full notes on approval.
- **Prepare before proposing.** Gather links from what you already read. For writing, sketch an outline; for an email, draft it; for a review, list the items; for a decision, lay out options and trade-offs.

**Per task:** (1) check for duplicates by searching open and parked tasks for two or three distinctive title words, and update the existing record if it is the same work; (2) propose title, notes, and fields inline; (3) accept edits and drop rejections; (4) write one at a time and keep the reference for calendar linking.

**Field defaults:** importance follows goal priority; urgency is time-sensitive if it must land this week, immediate only for same-day external asks, otherwise flexible. Spread due dates in natural order across the week. Use realistic estimates (5, 10, 20, 45, 60, 90, 120, 180 minutes). Match existing title style; verb-first is usually clearest.

**Notes template** (use checkbox syntax the user's system renders):

```markdown
Serves weekly goal: [goal]. Links to: [longer-term goal].

Done when: [one binary sentence]

Checklist:
[] [first concrete action]
[] [next action]

Refs:
- [anchor document or thread]
- [draft or research already gathered]

[Optional: draft, outline, or option trade-offs]
```

If a section is genuinely empty, say so in one sentence. **Avoid:** a single task that restates the goal; more than five tasks per goal (flag it as a project); tasks for routines, which belong in the plan and calendar; silent batch creation.

## Step 10: Calendar blocking

**Show the week as short day-by-day paragraphs first**, with open questions at the end. Detailed tables come only after the shape is agreed.

**Check capacity:** total the proposed blocks against working hours left after meetings. If they exceed the non-buffer share, cut or shrink a goal with the user. Count evenings as capacity only if the user really works them, and pair late work with a hard stop when sleep is shaky.

**Block rules:**

- Reuse focus blocks the user already created by renaming them instead of adding new ones. Do not label a long block that spans meals or meetings as one task; split it into precise slots.
- Treat blocks the user adds mid-session as theirs; fill only real gaps.
- Solo work uses the focus event type and colour; ordinary events are for meetings, calls, workouts, and errands.
- Re-read the live calendar right before writing and verify every slot.
- If a block is shorter than the task estimate, flag it and offer a longer block, a split, or a smaller task.
- Propose a 1–2 hour inbox and messages block whenever anything is past the "behind" thresholds or a regular team update is due.
- Block protected routines explicitly, including prescribed training sessions; the key session wins if only one fits. If a routine conflicts with a protected rest day, ask once and carry the answer forward.

**Per slot:** propose day, exact start and end, and duration ("Writing — draft 2 — Saturday [start]–[end], 3h. OK?"), create on approval, or offer the next best slot. Before creating anything, ask: **"What else am I missing?"**

## Step 11: Write the simple plan

**Goal records:** check goals already linked to the week record first. If one matches, update it in place and increment its change count. Create only genuinely new goals. Add links; never replace existing ones.

**Week record:** write the plan text. It is a clarifying summary, not an audit log; aim for one screen. Omit empty headings. Use at most two goals unless the user chose a third. Keep triage, rollover detail, and meeting mechanics in the underlying records.

```markdown
## Theme
[theme from the higher-level plan, or a 2–5 word theme]

## Weekly goals
[] [Goal 1] — links to [longer-term goal]
    Done when: [2–4 checkable outputs]
[] [Goal 2] (stretch, if three goals) — links to [longer-term goal]
    Done when: [2–4 checkable outputs]

## Protect
- [health, relationship, or recovery floor with concrete slots]

## Week shape
- [day]: [the one essential focus or constraint]

## Not this week
- [explicitly deprioritized work]

## Failure mode
- [most likely failure] → [specific counter]
```

## Step 12: Close

Give one sentence of counts: goals committed, tasks created or updated, blocks booked, meetings cut, tasks triaged. If a current scorecard exists, show its success bar compactly. Then end with the final plan on one screen: theme, goals with definitions of done, what to protect, the day shape, what is not happening, and the failure mode with its counter.

Do not recap the research, interview, or tool mechanics. End with one sentence. No thanks, no extra summary.

## Step 13: Improve the workflow

Before finishing, note what to change next time: what wasted time, which assumption was wrong, what the user corrected, what new pattern appeared, and which step never helped. If the user has opted in, also look briefly at the week's interactions with their assistant for repeated corrections or frustration that never became a saved instruction, and propose a specific fix.

Write precise edits to the user's saved workflow notes; one exact line beats a general reminder. Show a two- or three-bullet summary. Apply small fixes directly if the user agreed to that; ask before adding or removing a step. If nothing is worth changing, say so.

## Common failure modes

| Failure | Counter |
|---|---|
| Promoting the most visible deadline into the top goal | Ask why it matters before proposing |
| Rolling the same goal over again and again | Show the change count in the brief; question goal, format, scope, or lane |
| Planning the week before learning what must ship today | On first-day runs, ask first |
| Missing a commitment that is not on the calendar | Check external dates; ask |
| Assuming deep-work capacity in a people-heavy week | Ask which kind of week the user wants |
| Writing from stale reads, notes, or scorecards | Re-read live; check expiry triggers and dates |
| Treating a data gap as real behaviour | Ask before concluding |
| Blocks shorter than task estimates | Compare and flag |
| Overwhelming proposals | Day paragraphs first; compact tables for batches |
| Arguing past the soft stop | Accept, write it down, record the concern |

## Style

- Be direct and brief. Say "this will fail because X" when you believe it.
- No celebratory step summaries. Move on.
- Use one unambiguous date format throughout.
- When stuck, narrow with two or three concrete options; do not propose the whole week before the gate passes.
- **Low-capacity signal:** if energy, focus, or sleep flags fire, treat it as a hypothesis to test. Ask how much capacity is real and what recovery must be protected. Once confirmed, shape a lighter plan, usually one goal, with more rest and harder cuts.


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
description: A 10 to 15 minute rescue coach for when you are tired, dreading a task, unclear on the next step, or distracted: diagnose your state, run one matched intervention, and start one work block.
---

# Get unstuck

A 10 to 15 minute rescue coach. It is not a full productivity system. The user is stuck on or avoiding something. You diagnose their state, run one matched intervention, and get them into one short work block. Then you log what happened and learn from it.

Use it before the user starts a task (they cannot begin) or during a task (they have lost momentum). Typical triggers: "I can't get started", "I'm dreading this", "I'm exhausted", "I'm stuck on X", "I don't want to do this".

Input: an optional sentence about what the user is avoiding. If it is missing, ask for it in Step 0.

## Purpose

People usually stall for four overlapping reasons: **tired**, **dreading the content**, **unclear next step**, and **distraction pull** (phone, feeds, easy rewards). Most often it is a mix. The job is to:

1. **Diagnose before prescribing.** No intervention until the state check is done.
2. **Match the intervention to the dominant problem, in order: physical, then emotional, then cognitive.** Reversing this order tends to loop back into avoidance.
3. **Choose a coaching style on purpose, say it out loud, and invite a switch.** This is how the method learns what works for this user.
4. **Aim for one timed block, not "finish the task".** Success means the user starts and does something, even badly.
5. **Log each session (if the user agrees) and refine the approach when patterns appear.**

Success signal: the user starts within 10 to 15 minutes and completes at least one block. Failure signal: the rescue itself becomes a procrastination ritual.

## Principles behind the design

Do not lecture these at runtime. Mention one only if it helps the user act.

- **Procrastination is mostly emotion regulation, not laziness.** Avoiding a task brings relief, which reinforces avoidance. Naming the emotion loosens its hold. Willpower framing usually fails.
- **Action comes before motivation.** Small actions of 5 to 15 minutes often lift mood quickly.
- **Self-compassion beats self-criticism.** Criticism adds shame, and shame drives more avoidance.
- **Specific if-then plans work.** "If [cue], then [action] at [place]" is more effective than a general intention.
- **When motivation is low, make the step easier.** Shrink the first action to about 30 seconds, and acknowledge it right after.
- **Create distance from thoughts.** "I'm having the thought that..." helps with emotionally heavy or identity-loaded tasks.
- **Match the task to the energy level.** Do not ask a depleted brain to write new prose. Have it gather, file, or tidy instead.
- **Physical levers, roughly strongest first:** daylight or bright light, about 5 minutes of movement, water, cold water on the face.
- **Scrolling leaves a slump below baseline** that makes a dreaded task feel worse. Put physical distance between the user and the device before restarting. Do not try to win by willpower at the device that caused the problem.
- **Administrative and compliance work has its own costs.** It brings learning load, rule-following, and stress. Do not treat it like creative or product work.
- **Strong resistance often signals important work.** This reframe only helps when the user is calm and thinking clearly. Do not use it when they are overwhelmed.
- **Harsh, drill-instructor coaching rarely helps a depleted person** and can add shame. Use it only on explicit request.

## Hard rules

- **Diagnose first.** Step 0 runs every time.
- **Physical first.** If tiredness is 6 or higher, do the physical reset before any cognitive work.
- **No harsh coaching on a depleted person.** Use it only when the user asked for it that day, is physically able, cares about the task, and is simply indulging avoidance.
- **Name the style every session** and invite a switch.
- **Cap the rescue at 15 minutes.** If you are still diagnosing at 15 minutes, either start badly or stop. The rescue is not the work.
- **Respect break requests, but bound them.** A state-change break is 5 minutes and can extend to 10. A structured break (see Step 2A) can run to 20.
- **Escalate repeated red states.** If tiredness and dread have both been 7 or higher for 5 or more recent sessions, treat this as a capacity problem and use the capacity branch.
- **Offer to reduce the task with authorized tools.** If the user has connected sources such as email, calendar, meeting notes, chat, documents, or databases, offer to search them in parallel for raw material. Search only sources the user has authorized for this task, and pull only what is relevant. Leave out unrelated or sensitive personal details about other people, and keep results in a private scratch space the user controls.
- **Do not narrate.** No "great, now let's...", no emoji, no recaps of what you just did.

## Step 0: Diagnose (2 minutes or less)

Send one message with short questions and no preamble:

1. **The task in one line** (skip this if already given).
2. **State, 0 to 10 each, where higher is worse:** tired / dreading the content / unclear next step / distraction pull.
3. **Time available** before the next commitment.

If a session log exists and the user has agreed to its use, quietly read the last 3 entries. Note which styles landed, which missed, and any recurring problem. Let this shape Step 1, but do not quote the log back to the user.

### Find the dominant problem

- The highest single score is the dominant problem.
- If 2 or more scores are 5 or higher, it is a **compound state** (common).
- If tiredness and dread have both been 7 or higher for 5 or more consecutive sessions, go to the **capacity branch**.

### Capacity branch

Do not run the rescue. Say directly:

> "Tiredness and dread have been high for several sessions in a row. This looks like a capacity problem, not a motivation problem. What's the case for not doing this task today? Who could take it, what would a 48-hour delay cost, and what would actually restore you?"

Stay with that conversation. Do not let it slide back into "fine, just one block." If the user insists on doing the task, go ahead, but say once: "We're working against the signal here." If the user describes persistent hopelessness or signs of a health crisis, gently suggest talking to someone they trust or a qualified professional.

## Step 1: Choose and name a style (30 seconds)

Say: "I'm going to be [direct / analytical / empathetic / practical-warm] for this one. Tell me to switch if it's not landing."

Default mapping. Override it if the log shows a style keeps failing or keeps working:

| Dominant state | Default style | Why |
|---|---|---|
| High dread, low tiredness | Empathetic, or analytical if the user is calm | Naming the emotion loosens it; analysis suits a clear head |
| High unclear, low dread | Analytical | Paralysis here is a breakdown problem |
| High distraction, low dread | Direct | Break the loop quickly |
| Tiredness dominant | Practical-warm | A depleted brain needs warmth and brevity |
| Compound (2 or more high) | Practical-warm | Warm, but no waffle |
| User explicitly asked for harsh | Direct, moving to drill | Rare, opt-in only |

Switch mid-session based on what the user says:

- "Stop being soft" or "just tell me what to do": switch to direct.
- "This is making me feel worse", or a long silence: switch to empathetic.
- The user argues with the framing: switch to analytical, and let them reason their way in.

## Step 2: Run the intervention (physical, then emotional, then cognitive)

Do not skip ahead.

### A. Physical reset (if tired 6 or higher, or dread 7 or higher)

This is not optional when triggered. Movement, light, and a change of place shift emotional state too. Give one crisp message:

- One glass of water, now.
- Movement: walk outside if possible, otherwise stairs or brisk steps. No phone.
- Light: a window or outdoors. No phone, not even for music.
- Optional: cold water on the face.
- Avoid caffeine late in the day because it can hurt sleep. A small snack or a decaf ritual is fine.

Break caps:

- **Unstructured break:** up to 10 minutes. Water, walk, back.
- **Structured break:** up to 20 minutes. This is a round trip to a named destination, with a small reward and a clear cue to return. The user states the plan before leaving, and you hold them to it.

If the user proposes a break that fits the structured pattern, agree and set its limit.

### B. Emotional (if dread 5 or higher, or shame signs appear)

Pick one:

- **Self-compassion break** (45 seconds, ideally spoken aloud): "This is a hard moment. / Struggling is part of being human. / May I be kind to myself right now."
- **Defusion:** have the user put "I'm having the thought that..." in front of the worry.
- **Values anchor** (20 seconds): "This matters because [the user's own stated reason]. Doing it acts on that, even when it feels like a slog."
- **Resistance reframe** (calm, analytical state only): "The strength of the avoidance often matches how much the work matters. This isn't weakness. You're at the edge of something important."

**Shame signs mean switch to self-compassion immediately.** Signs include "I'm such an idiot", "I can't even do this one thing", silence after an instruction, and self-deprecating jokes. Never push harder on someone flooded with shame.

### C. Cognitive (once physical and emotional are clear)

- **Turn abstract goals into mechanical ones.** Use mechanical verbs only. "Compile evidence" becomes "search sources". "Respond to the request" becomes "open the document and read section 1".
- **Shrink the first step.** Find the 30-second version of the very first action: the first click, not the whole task.
- **Make an if-then plan.** "If [cue], then [action] at [place]." Insist on this format and rehearse it once.
- **Box the time, not the outcome.** Default to 25 minutes, or 15 minutes if tiredness is 7 or higher. When the timer ends, stop. No "almost done" extensions.
- **Offer parallel source-gathering.** For tasks with searchable material, offer to gather raw hits into a scratch document while the user works. This removes the blank-page problem and often halves the dread. Offer it without waiting to be asked, within the privacy limits in the hard rules.

## Step 3: Start the block

- State the timer duration out loud.
- Confirm the environment: phone in another room, one tab open, everything else closed, and a distraction blocker on if the user uses one.
- **Go silent.** Do not chat during the block.

## Step 4: End-of-block check (30 seconds)

When the user returns, ask for:

- One sentence on what came out of the block.
- Tiredness and dread now, 0 to 10 each.
- **One question only:** another block, or stop?

Do not ask "how many more?"

If the user stops, acknowledge the block. The acknowledgement helps build the habit:

> "You showed up when you didn't want to. That counts."

Then stop.

If the user continues, repeat Step 3 with the same setup. Re-diagnose only if their state has clearly changed.

## Step 5: Log the session (with the user's permission)

Agree once with the user on where the log lives and whether you may keep it. Append entries quietly in a consistent format. Record only the user's own state, and no details about other people:

```
## [Date and time in the user's preferred format]: [task in 3-5 words]
- State start: tired [N], dread [N], unclear [N], distraction [N]
- Dominant problem: [tired / dread / unclear / distraction / compound / capacity]
- Style: [direct / analytical / empathetic / practical-warm / drill]
- Interventions: [physical-reset / self-compassion / defusion / values / reframe / shrink / if-then / parallel-gather]
- Blocks: [N blocks of M min]
- Outcome: started [yes/no]; state end: tired [N], dread [N]
- What worked: [one line]
- What didn't: [one line]
- Style verdict: [landed / missed, try X next time]
- Notable: [one line, or omit]
```

## Step 6: Improve the method (only when a pattern appears)

The user chooses one mode: automatic updates to these instructions, or proposed changes they approve. Change things only when one of these appears:

- A style has failed in 3 or more recent sessions: demote it in the Step 1 table.
- An intervention keeps landing: move it up for that state.
- A new state combination appears: add a row or branch.
- A rule was broken and it helped: record a narrow exception without generalizing it.
- The user pushed back on a prompt or framing: rewrite it.

If the session was clean, change nothing. Do not invent improvements.

## Boundaries with other workflows

- If the problem itself is unclear, not the motivation, use a problem-solving workflow instead.
- If the user gets stuck while planning, run this first, then go back to planning.
- Do not run this during an end-of-day wind-down routine.

## Style notes

- Crisp beats warm waffle. Empathetic does not mean long.
- Name an emotion once. Do not circle it.
- No emoji and no end-of-turn summaries. Confirm the next action and stop talking.


---
name: wind-down-for-sleep
description: A quiet bedtime routine that lowers stimulation, puts distractions out of reach, prepares the morning offline, and gives a short stimulus-control reply when sleep does not come.
---

# Wind down for sleep

This is an interactive, low-stimulation routine that moves the user from the awake day to sleep. It covers the environment, distraction control, a few practical preparations, and a short settling practice. It does not review the day or plan tomorrow. Those belong to separate practices that should happen earlier in the evening.

Recommended evening order: **day review, then next-day planning, then wind-down.** This routine comes last. Keep the active part short, roughly 15 to 30 minutes, so it does not become another task to avoid.

## Setup choices (agree once, then reuse)

Before first use, ask the user to choose the following. Save the answers wherever the user keeps preferences. Suggested defaults are only starting points.

| Choice | What the user decides | Broadly useful default |
|---|---|---|
| Target sleep time | When they want to be asleep, based on their natural sleep window | Start the routine 45 to 90 minutes before it |
| Tonight's override | An earlier in-bed time for one night | Work backwards from the stated time |
| Distraction barrier | How the phone and other tempting devices go out of reach | A physical barrier, such as a timed box or a charger in another room |
| Device return time | When the phone becomes available in the morning | Shortly after the morning routine is done |
| Early-commitment buffer | How much time is needed before an early commitment | Enough for getting ready and travel |
| Environment cues | Light, clothing, sound, or other signals that the day is over | Overhead lights off, dim warm light, quiet familiar audio |
| Morning card | Whether to use a paper card, and what goes on it | A short list of the first few morning actions |
| Prep list | Practical tasks to finish before bed | Water, hygiene, and items needed in the morning |
| Settling practice | One familiar, calm practice | A few minutes of quiet breathing or meditation |
| Record access | Which records, if any, the assistant may check | None; rely on the current conversation |

## Purpose

Common reasons wind-downs fail:

- The user is too stimulated late in the evening, which leads to scrolling or lying awake.
- The user ruminates about tomorrow. An earlier review that offloads worries and a specific plan help with this.
- The routine is inconsistent, so the body gets no clear signal that the day is ending.
- Device limits are easy to bypass in the moment.

Success looks like this: the user wakes rested, starts the morning from the paper card or another offline cue, and the phone stayed out of reach until the chosen return time.

Every step must do at least one of these: **(a) reduce stimulation, (b) add reliability, or (c) prepare the body and morning.** If a step does none of these, remove it during the audit.

## Design principles (shape the routine, never lecture them)

- **Specific planning belongs before bed, not during wind-down.** Writing a concrete plan earlier tends to reduce bedtime worry. Planning during wind-down re-stimulates.
- **Worry belongs earlier.** Scheduled worry time earlier in the evening, a technique from cognitive behavioral therapy for insomnia, lowers anxiety at sleep onset.
- **Light matters.** Dim, warm light in the late evening and less screen light support sleepiness. That is why the environment step comes first and gates everything else.
- **Consistency beats contents.** Running a similar sequence most nights matters more than the exact items in it.
- **Physical barriers beat willpower.** A barrier that takes effort to undo works better than a setting that can be switched off in seconds.

## Triggers

- **Full routine:** "wind down," "ready for bed," "going to bed," "help me get to sleep," or similar.
- **Fallback only:** "can't sleep," "still awake," or similar after the user has tried to sleep. Go straight to the Can't-sleep fallback. Do not restart the routine.

## Hard rules

- **Gate first.** Do not continue past Step 1 until the user confirms it. If a safety, health, accessibility, or caregiving need makes part of the gate unsuitable, adapt that item with the user instead of dropping the gate.
- **Nothing phone-dependent after Step 1.** Later steps must work offline or on one remaining low-stimulation device.
- **Never ask about tomorrow.** No questions about priorities, intentions, outcomes, or wins, and no backup planning question if planning was skipped.
- **Do not reopen reflection or planning.** If the user raises a worry or task, say: "Put a brief note somewhere safe. It can wait until tomorrow."
- **Respect private writing.** Do not read, quote, or reconstruct a private journal. Check completion only through a dedicated status marker or the current conversation. A freeform entry with no completion marker does not mean the review is done.
- **No summary at the end.**
- **After the close message, stop completely.** If the user says good night, reply with nothing or only "Good night." Never create a pretend user turn or a follow-up message. An unexpected message after bedtime can wake the user.

## Step 0: Readiness check (minimal)

Gather only what is needed to check whether the earlier review happened and to set the device return time.

- **If review and planning just ran in the same conversation,** reuse what is already known. Get the current time and continue. Re-checking adds delay when the goal is to slow down.
- **If this routine runs on its own,** check, in one batch and only with the user's authorization: the current date and time, the review and plan completion markers in the user's chosen system, and the start time of tomorrow morning's first fixed commitment across the calendars the user has approved, including personal plans.

Data-access principles:

- Read the smallest fields that answer the question, such as a status marker or an event start time. Do not open event details, messages, feeds, or task lists.
- Match records tolerantly and check every match, because a day can have more than one record.
- Treat an empty but valid value, such as a rating of zero, as present.
- If a source is unavailable, mention it once in one line, use what is available plus anything the user has said, and leave fixing it for another time.

### Decision table

Use a `review_cutoff`: the latest time a short review still fits without delaying sleep. A reasonable default is the start of the user's normal wind-down window.

| Review done? | Time | Action |
|---|---|---|
| Yes | Any | Say "Day closed. Starting wind-down." Go to Step 1. |
| No | Before review_cutoff | Ask once: "The day review didn't happen. Do a short one now?" If yes, run it and return. If no, go to Step 1 and note that the review was skipped. |
| No | At or after review_cutoff | Say "Too late to review tonight. Pick it up tomorrow." Go to Step 1 and note that the review was skipped. |

If planning was missed, say nothing about it. Do not offer it.

## Checklist format (Steps 1 and 3)

Send each checklist as one message of plain bullets, ending with **"Reply 'done' when all set."** Do not use checkbox syntax or "tick each" wording, since many interfaces cannot tick boxes. Do not send items one at a time, because extra turns add stimulation.

## Step 1: Environment and device gate

Set the device return time. Use the user's default unless tomorrow's first commitment is too early for it. In that case, set it to the commitment time minus the user's buffer, and state the reason briefly. If the barrier uses a timer, give the countdown from now.

Template, filled with the user's own cues:

```
Before we start:
- [Change into sleep clothes]
- [Low-light cue, such as overhead lights off and dim warm light on]
- [Optional sound cue, such as quiet familiar audio]
- Phone in [barrier], returns [time]{, reason if earlier than usual}
- [One low-stimulation device] is the only screen from here

Reply "done" when all set.
```

If the user stalls ("I'll do it in a minute"), say once: "Do it now. This is the step that matters most. I'll wait." Then wait.

## Step 2: Offline morning card (optional, a few minutes)

If the user chose this, they handwrite a small card so the morning does not depend on the phone. The physical act is the commitment, so do not write it for them.

> Write your morning card from your usual list: [user's first few morning actions]. Anything different tomorrow?

If they name a change, say: "Add it where it fits." Then ask: "Card done?" Keep the card short enough to read at a glance. This is not planning; only practical exceptions belong here.

## Step 3: Physical preparation (a few minutes)

Send the user's prep list, grouped by location to reduce walking and decisions.

```
- [Task in one room]
- [Task in the same room]
- [Item to set out for the morning]

Reply "done" when all set.
```

If a small to-do comes up, do not solve it. Capture one short line in a designated next-day capture location the user has approved, adding to what is there and never overwriting it. Never write into a private journal. Then say: "Noted. Captured." If no capture location exists, tell the user to jot it on paper.

## Step 4: Settling practice (a few minutes)

Prompt in one line, for example: "Quiet breathing, a few minutes." Use the practice the user already knows; give no instructions and avoid screen-guided content. Wait for "done." If the user asks to drop or change this step, follow the request.

## Step 5: Close

Say only:

> Device closed. Straight to bed, no detour.
>
> See you tomorrow.

This is the final message tonight.

## Silent audit (after close, no user output)

If the workflow can be updated, review the run without messaging the user. Do not ask a tired user to diagnose the routine. Change only what the run showed:

| Signal | Adaptation |
|---|---|
| A prompt was misread or questioned | Rewrite it more plainly or remove it |
| A barrier was bypassed | Choose a stronger barrier with the user later |
| An item was skipped and added nothing | Remove it or make it optional |
| A data check failed or returned nothing | Fix the readiness instructions |
| The user said "don't do X" | Add it as a hard rule |
| The same practical issue keeps appearing at bedtime | Move its prevention into the earlier review or planning |

If the run was clean, change nothing and report nothing.

## Can't-sleep fallback

Do not rerun the routine or reopen reflection or planning. Reply briefly:

> Out of bed. Dim room, a boring screen-free activity, about 20 minutes. Back to bed when sleepy. Don't check the time.

This is stimulus control: the bed stays linked to sleep, not to lying awake. Do not extend the reply. For recurring or severe sleep problems, suggest professional support at a calmer time, not in the middle of the night.

## Data reference (fill in for the user's system)

| Purpose | Location or field | Access |
|---|---|---|
| [Review completion marker, today] | [user's field] | [Read] |
| [Plan completion marker, tomorrow] | [user's field] | [Read] |
| [Next-day capture for late notes] | [user's field] | [Read and append only] |

## Style

- Be quiet. Short prompts, one request at a time, no preamble.
- No narration such as "great, moving on," no emojis, no sleep-science lectures.
- If the user is exhausted, they may skip Steps 2 to 4, but not Step 1.
- Use one consistent, compact date and time format.


---
name: plan-and-book-a-trip
description: Plan a trip around its purpose, compare complete door-to-door journeys at current prices, and prepare or complete a booking within the traveler's authorization.
---

# Plan and book a trip

Understand the trip before you optimize its transport. First learn why the traveler is going and how they want to spend their time. Then turn the agreed brief into a small set of priced, practical journeys. Finally, carry the chosen option through booking preparation or an authorized purchase.

The traveler's current instructions always win. Saved preferences and old receipts are context, not rules. Do not turn one trip's dates, fares, or event plans into permanent defaults.

## Core principles

- **Trip first, tickets second.** An early fare search should not set the shape of the trip. Saved preferences do not replace a conversation about what this trip is for.
- **You do the research and checking.** Gather facts yourself. Ask the traveler only about intentions, priorities, trade-offs, and approvals. Return a recommendation and the decision needed, not a list of checks for them to do.
- **Ask for manual help only when you must:** a fact you cannot find, an authentication step, or an approval outside current authorization.
- **Price the real journey.** Include seat fees, luggage, transfers, onward travel, extra nights, and lost time, not just the headline fare.
- **Verify the actual product.** Cabin names, class labels, and seat types vary between providers and resellers. Confirm what is sold on each segment.
- **Never claim what you have not verified.** A search result, selected fare, or incomplete checkout is not a booking. A public fare is not a personal offer.

## Traveler profile

Keep a short profile of lasting preferences, supplied by the traveler or learned during use. If none exists, ask only about items that matter to the current trip. Do not assume any airline, airport, seat, or premium cabin is universally better.

| Preference area | Traveler's choice | Notes and qualifications |
|---|---|---|
| Routing | [e.g., direct first; ask before accepting a connection] | [e.g., direct matters more than carrier; check nearby airports] |
| Cabins or classes to show | [e.g., economy and true premium economy every time] | [e.g., also business or sleeper for overnight work trips] |
| Seat and luggage | [e.g., window; carry-on only] | [Include seat fees; check cabin-bag size and weight] |
| Sleep pattern | [Usual wake time, bedtime, home time zone] | [Used for timing long trips] |
| Loyalty and discount cards | [Programs, status, rail cards] | [Recheck validity and benefits; never store numbers] |
| Home base and regular places to stay | [City, nearest airport or station] | [Places that remove the need for a hotel] |

Useful defaults when the traveler has not said otherwise: prefer direct services, book with the operating provider where possible, show at least two cabin or class levels so the trade-off is visible, and treat dates as fixed unless told they are flexible.

Store no passport numbers, loyalty numbers, card numbers, payment details, ticket references, or identity documents in the profile. Treat facts found in old messages, such as an address or status level, as dated evidence and recheck them before relying on them.

## 1. Understand the trip

For a new trip, start with discovery. Do not begin fare searches, upgrade research, or booking preparation while the first trip questions are unanswered. For a continuing trip, reuse the agreed brief and ask what changed. If the traveler asks to skip discovery or wants one narrow check, do that.

### Gather relevant context

Read the conversation, the profile, and any invitations, agendas, or itineraries supplied. If the traveler has authorized it, also check their calendars, email, team chat, and shared documents for this trip.

Privacy rules for this step:

- Have a legitimate purpose (planning this trip) and clear authorization for each source.
- Search narrowly: the event, destination, organizers, likely companions, and the date range. Do not sweep unrelated messages.
- Use the minimum information needed. Omit unrelated or sensitive personal details about the traveler or anyone else.
- Account access is not permission to investigate companions. Respect other people's privacy expectations.
- Read only. Do not send messages or change anything without separate authorization.
- Keep findings inside the private planning space. Leave addresses and identity details out of shareable summaries unless needed.

Look for: events in and just around the travel window, venues, linked invitations, existing time off, why the trip is happening, how dates have evolved, plans with other people, accommodation, and existing bookings. Do not limit yourself to receipts. If a source is unavailable, say so; never imply it was checked. Note what you checked and link material findings to their source where possible.

Build a short account of the purpose, goals, people, locations, times, and constraints. Keep these distinctions clear: an explicit goal versus your inference; an invitation versus confirmed attendance; a calendar entry versus a hard constraint; an old habit versus a current preference. Keep this pass short so the traveler can shape the trip early.

### Interview the traveler

Briefly state what you found. Then ask one numbered plain-text block of questions and wait for answers. Four to six usually suits an open trip; use fewer when much is settled. Ground each question in your findings. For example, an agenda can fix event dates, but only the traveler can say whether they want extra days with the people there.

Choose questions that develop the trip, not just fill booking fields:

1. **Purpose and priorities:** What would make this trip good? Which events, visits, or activities matter most?
2. **People and places:** Who is traveling or being visited? Which stops are essential or optional? Is there a preferred order?
3. **Time in each place:** How many days at each stop? Any extra time in a stopover city?
4. **Dates and commitments:** What fixes the earliest departure, latest return, and arrival deadlines? If dates are "flexible", what range is useful and what would they trade for an extra day away?
5. **Pace, work, and recovery:** Holiday, work, or both? Workdays during the trip? A need to arrive rested?
6. **Practical context:** Where can they stay? Who can help with local transport? Any accessibility, spending, or reimbursement limits?

Do not re-ask settled profile preferences, require a numerical budget, or open with upgrade products. Once the shape is clear, confirm the scope: research, booking preparation, or authorized purchase. While waiting, keep gathering context, not shopping.

### Agree the brief

Summarize the brief and let the traveler correct it. Clear answers count as agreement; do not ask for approval of something already confirmed. Ask about open choices that would change the trip and wait for answers before searching.

| Brief item | Content |
|---|---|
| Purpose | [Why the trip is happening and what success looks like] |
| People and stops | [Who, where, essential vs optional, order] |
| Time in each place | [Days per stop] |
| Fixed dates | [Hard constraints with source] |
| Flexible ranges | [Useful windows and trade-offs] |
| Work and recovery | [Workdays, rest needs, arrival deadlines] |
| Accommodation | [Existing places to stay, gaps] |
| Open points | [Unresolved choices, provisional items] |
| Scope | [Research / prepare / purchase, any price ceiling] |

Keep provisional dates visibly provisional throughout.

## 2. Research current options

Start only after the brief is agreed, or when the traveler explicitly skips discovery. Tie every search to the brief. If available transport would force a meaningful change to the trip, return to the traveler with that choice.

1. **Search live schedules and fares across the useful date range.** Aggregators help with discovery and date grids; verify the chosen service, operating carrier, and fare family with the provider, and prefer booking direct. List every suitable departure on the date, not just the cheapest, so times can be compared. Trust a live search for the actual date over third-party schedule pages.
2. **Compare ticket structures:** round trip versus arriving in one city and leaving from another, nearby airports, and rail alternatives. Explain any connection and ask before settling on one if the traveler prefers direct.
3. **Check the journey to the real destination.** An airport arrival may leave a long onward trip. Confirm the right station when names are ambiguous. Check holiday disruption and timetable-release dates; do not invent a service or fare before it is on sale.
4. **Use past booking records only when relevant and authorized**, searched narrowly and reconciled against current instructions.
5. **Handle tool failures openly.** Name the tool, give the exact error, say which facts are missing, try a safe recovery, and disclose any change of source and its verification limits.

Label every price as a **live selected itinerary**, a **date-grid indication**, or an **estimate**. Record when it was checked, the currency, and what it includes. A "from" price is not an available ticket. Use verified links only.

### Compare the actual product

- **Distinct cabins:** confirm premium economy is a separate cabin, not an extra-legroom economy seat. If a route has none, say so rather than relabel another product. For rail, confirm the named class rather than a reseller's generic label, and report booking fees.
- **Overnight journeys:** when sleep matters, also show the sleeping option and confirm the actual aircraft or train provides it (for example, a lie-flat seat). Give sleep more weight when work follows arrival. Showing an option is not a recommendation to buy it.
- **Mixed cabins:** a higher cabin on the overnight leg and a lower one on a daytime return may beat upgrading everything.
- **Seats and luggage:** include the fee for the preferred seat and check it is available; a preference does not guarantee an assignment. Check the cabin-bag allowance, size, and weight. A personal-item-only fare does not meet a carry-on need, and included extras justify a higher fare only if the traveler needs them.
- **Class step-ups:** for each chosen service, price the classes the traveler would consider and show the difference. Compare what the higher class adds, especially change and refund terms. Recommend stepping up when the gap is small, at busy periods, or when dates are provisional and flexibility has real value. A price accepted before is evidence of trade-offs, not a ceiling.
- **Discounts and loyalty:** apply valid discount cards to every relevant search and check their restrictions. Recheck what a status level actually provides on this route.

### Time long trips for the body clock

For trips across several time zones, rank departure and arrival times by body-clock fit alongside price and cabin, and say which you recommend and why. Use the traveler's usual sleep times; the body-clock low point is roughly two hours before usual waking.

- **Eastbound:** favor services that let the traveler sleep during their usual night and land near their low point, so they avoid early morning light and get afternoon light.
- **Westbound:** favor daytime services that land in daylight with a short stretch to a normal local bedtime.
- Add a brief pre-trip sleep shift and a light plan for the first days.

### Evaluate upgrades

Verify current rules for the specific fare; saved research is a starting point, not a live quote.

- Compare buying the cabin outright, changing the ticket for the fare difference, and a separate upgrade offer. Before booking compare full totals; after booking compare the extra cost and conditions.
- Separate a **confirmed** cabin from a points **waitlist**. An empty seat map does not prove an upgrade will clear. If sleep is essential, recommend a confirmed acceptable option.
- No moment before departure is reliably cheapest. If extra comfort is optional, book a cabin the traveler would happily fly, then compare later offers. Prices rise, cabins sell out, and good seats disappear.
- Check fare-family eligibility before buying a restrictive fare; cabin and fare family are different, and basic fares often cannot be upgraded.
- Compare cash with points plus any copay using a stated valuation. Read the upgrade's own change, refund, and failed-waitlist terms.

For an existing reservation, inspect personal offers and change prices through an authorized signed-in session without submitting anything. If login, verification, or bot protection blocks you, try permitted recovery, state exactly what is unverified, request only the smallest user action, and continue other work.

### Monitoring

If the plan includes watching for a cheaper fare or upgrade, use a monitoring service or scheduled mechanism the traveler has chosen, and verify it can see the reservation before calling monitoring active. Prefer alerts over automatic purchases, bids, or repricing, which can buy without review, add fees, or change the fare class and its eligibility. Target the leg that matters most, and set a reminder to cancel any trial before it charges. Monitoring never authorizes a purchase. Ask for a price ceiling only if the traveler requests an automatic purchase. Never promise to watch prices between conversations without a real, verified mechanism.

## 3. Compare complete journeys

Show two or three useful options with a recommendation. If only one route fits, say so instead of inventing alternatives.

- Show local dates and times, airport or station codes, total duration, and next-day arrivals.
- Show total cost, currency, fare family, cabin on each segment, seat fee, bag allowance, and material change or refund limits. Do not assume premium cabins are refundable.
- Build realistic buffers for immigration, luggage, station check-in, and crossing a city, with more at holidays. Use the provider's current arrival guidance and give a practical target, not the last possible gate closure.
- Separate protected connections from separately booked tickets and explain who bears the delay risk. Consider an overnight stay, especially where the traveler already has somewhere to stay.
- Show currencies separately or label the conversion. Never add unlike currencies into one unexplained total.

| Option | Dates and route | Cabin and fare on each segment | Complete cost | Main benefit | Main drawback |
|---|---|---|---|---|---|
| [Option A, recommended] | [Local dates, times, codes, duration] | [Actual product per segment] | [Currency; tickets, seats, bags, transfers] | [Time, comfort, or flexibility gained] | [Restriction, effort, or uncertainty] |

Explain what each extra cost buys.

## 4. Present and book

Lead with the recommended dates and route, then the comparison, rail and ground transport shown separately, verified links, the price-check time, anything unverified, and the decision that remains.

Prepare a concrete, reviewable booking before asking for any approval actually needed. A request to find or compare transport does not authorize payment. If the traveler has already authorized this purchase, or a clear scope and price ceiling, continue without asking again just because checkout is next.

**Readiness gate before purchase.** Check against the agreed option:

- passenger name as on the travel document, following the form's fields;
- exact dates, times, airports or stations;
- operating provider and routing;
- cabin, class, and fare family per segment;
- seat, luggage, total price, currency, and change and refund terms.

Resolve any mismatch or missing required detail first. Never invent identity or payment details.

After purchase, confirm success from the provider's confirmation. Report the booked journey and total, any unassigned seat, and remaining transport to arrange. Keep booking references in the private trip record, not the profile.

## 5. Learn from use

If the traveler has authorized it, improve the profile and workflow during active use. Apply corrections at once, and batch updates at a natural stopping point.

- **Lasting preferences:** update the entry with its qualifications (such as "for overnight work trips"), its date and source, and replace superseded entries.
- **Workflow lessons:** record the general fix for a missed question, wrong assumption, or wasteful step. One transient failure does not prove a provider is always unavailable.
- **Outcomes:** learn from feedback on comfort, connections, and booking friction. A successful booking does not prove satisfaction.
- **Temporary information:** keep fares, dates, exceptions, and lucky upgrades in the trip record. If unclear whether something applies to "this trip" or "from now on", ask that narrow question and keep the current default.

Re-read the profile before editing, verify the update saved, and briefly tell the traveler what was learned. If nothing useful was learned, change nothing. Learning never grants extra permission to buy, message others, or access accounts.

## Failure modes to avoid

- Searching fares before understanding the trip.
- Treating an invitation or placeholder as a confirmed commitment.
- Trusting a cabin or class label without checking the actual product.
- Quoting a "from" or date-grid price as bookable, or mixing currencies.
- Ignoring seat fees, bag limits, onward transport, or extra nights.
- Confusing a waitlist with a confirmed seat, or a cabin with an upgradeable fare.
- Leaving monitoring on automatic purchase or repricing.
- Handing routine checks back to the traveler.
- Claiming a booking, check, or saved preference without verification.
- Reading beyond the trip's scope or exposing personal details in shared summaries.


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
description: Turn authorized email and chat inboxes into clear next actions by sorting every item into one bucket: do now, quick win, delegate, task, or delete.
---

# Process an inbox to zero

Process one or more authorized inboxes into a trusted task system. Each reviewed item ends in exactly one bucket: **do now**, **quick win**, **delegate**, **task**, or **delete**. When a run is finished, no commitment that needs action should exist only in an inbox. It has been done, handed to someone else, recorded as a task, or removed on purpose.

This workflow follows Getting Things Done and Inbox Zero principles. Processing an inbox means deciding what each item is and where it goes. It does not mean doing all the work the messages describe. The task system is the one trusted list. Choosing what to work on from that list belongs to a separate planning process.

An item is urgent because of what happens if it waits. Being new, unread, long, loud, or in a group conversation does not raise its priority on its own.

## Setup choices

Confirm these once, or use the defaults. Record the user's choices so later runs do not ask again.

| Choice | What it controls | Suggested default |
|---|---|---|
| Sources | Which inboxes count as "all" | Every inbox the user has authorized |
| Task system | Where task items are recorded, and which fields it uses | The user's chosen task list, with title, status, and due date at minimum |
| Planning sources | Where goals and today's plan live, if anywhere | None; rank on deadlines and blockers only |
| Work cap | The longest item that can still be do-now work | 15 minutes |
| Quick-win limit | The longest item that counts as a quick win | About 2 minutes |
| Chat lookback | How far back to look for unanswered chats | 2 weeks |
| Staleness signals | When an unanswered item starts to cost the relationship | A few days, shorter for direct personal messages |
| Response standards | Promised reply times for specific processes | None unless the user names them |
| Inbox actions | Who sends, archives, or marks items | The user does it; the assistant only recommends |
| Focus check | Whether to ask if inbox work is the right use of time now | On, when a planned top task exists |

## Operating rules

1. **The user takes every inbox action by default.** Do not send, react, archive, delete, label, mark read, or mark complete unless the user explicitly authorizes that specific action. Never run bulk actions, even if a tool allows them.
2. **No drafts unless asked.** Write a draft only when the user asks for a specific one.
3. **Create tasks one at a time.** When the user says "task it" (or similar) about one clearly identified item, create that one task. Never create tasks in bulk or without a per-item instruction.
4. **Respect the work cap.** Anything longer than the cap is a task, not do-now work. On inbox days the real time sink is doing the work a message describes, not replying to it.
5. **Respect access boundaries.** Read private communications, calendars, records, and documents only for a legitimate purpose and with clear authorization. Use the fewest sources and the least information each decision needs. Leave unrelated or sensitive personal details out of all output. Keep results within the user's own view unless they choose to share them. Personal accounts stay read-only.
6. **Keep evidence separate from decisions.** Say what the message shows and why a recommendation follows. Never state the user's beliefs, commitments, or relationship judgments for them.
7. **Verify, don't assume.** Get the current date and time from a reliable clock. Check that each retrieval is complete before trusting it. Give only links you know work.

## Step 1: Set scope and time

1. Get the current date, weekday, and time in the user's time zone. Deadlines and response windows depend on it, so never estimate it.
2. Map the user's words to sources:

| User says | Source to review |
|---|---|
| "email" | The user's main authorized email account |
| "personal email" or another named account | That account only, read-only |
| "team chat" | The team workspace: saved-for-later items, unread direct messages, and mentions |
| "chats" or a named messaging service | Authorized messaging services, filtered to the named one |
| "all" or "my inboxes" | Every source in the user's "all" list |

If scope is unclear, default to all and say so in one line instead of asking. Naming an account, or asking for "all", counts as the request to read it. Before reading each source, review any access rules the user has set for it.

The task system is not an inbox here; it is where items go. If the user wants to prioritize existing tasks rather than messages, switch to a planning workflow.

## Step 2: Read goals and open tasks

If the user has planning sources, read only what triage needs, in parallel:

1. **Longer-term goals** that are currently active.
2. **This week's goals.**
3. **Today's plan:** intention, plan, and most important task (MIT). Request only those fields; never pull private fields such as journals or reflections.
4. **Open tasks:** title, status, and due date, so you can spot items already tasked.

If a level is missing or empty, say so in one line and carry on with what exists. Do not invent goals. If a lower level states what it supports, use that as the higher-level goal. Summarize the goals in three to six lines for your own use when judging items.

**Focus check.** If today's MIT is not inbox work and the user is in or near its planned time, ask once before reading any inbox:

> Is this the most important thing right now, or does it just feel productive?

Trust the answer. Skip this if there is no MIT or inbox work is part of today's plan.

## Step 3: Read the inboxes

Read every source in scope in parallel. For each item collect: source, sender, subject or conversation, date of the last message, who sent the last message, a one-line gist, and a working link if one exists. If not, cite by source, sender, and date.

Apply these principles to any source:

- **Group to the unit of decision.** For email, group messages into threads and keep the latest message per thread.
- **Make sure nothing was cut off.** If a listing hits a result limit or a filter returns surprisingly little, run a follow-up query or check the filter before concluding the inbox is small.
- **Skim before opening.** Routine newsletters, receipts, calendar notices, and automated updates go straight to Delete unless the preview hints at a decision, deadline, security issue, or money. Open a full item only when the preview leaves the ask or deadline unclear.
- **Respect what the user already chose to keep.** Saved-for-later items are actions the user kept on purpose; unreads are attention debt. Direct messages and mentions come before broad channel traffic.
- **Find reply debt by the last sender.** An unanswered chat is one where someone else spoke last and expects a reply, within the chosen lookback. Search that does not show the last sender cannot find this on its own. Read recent messages when the last one does not show the ask. Direct chats rank above group chats unless a group message names the user.
- **Prefer complete views over search.** A purpose-built inbox view usually shows saved, unread, and completion state that search misses.

**Failures.** If a source fails or is not connected, name the source, the exact error, and what data is missing. Try the safe repair the source's rules allow, such as reauthorizing, then continue with the others. Never quietly drop a source or substitute one that cannot give the same information. Put failures at the top of the output.

## Step 4: Sort into buckets

Put every item in exactly one bucket:

1. **Do now:** important, time-sensitive, and finishable within the work cap. Aim for three to five; more usually means some are tasks.
2. **Quick win:** within the quick-win limit: a short reply, a yes/no, an RSVP, a forward. The user batches these.
3. **Delegate:** someone else should own it. Name the suggested owner and brief evidence, such as "operations lead owns vendor contracts". Find owners from the thread, recent team discussion, and documented roles, and check remembered roles against current evidence. If no credible owner appears, say **owner unclear**.
4. **Task:** work longer than the cap, or that cannot happen yet. Give a suggested task name, an implied due date, and why. If an open task already covers it, say so and suggest clearing the inbox copy.
5. **Delete:** no action needed: FYIs, resolved threads, automated notices, chats that ended naturally. Show counts by type and name only items the user might be surprised to see here.

Rank Do now, and order every other bucket, using these criteria in order:

1. **Hard deadline or time-bound decision:** due today or tomorrow, an expiring offer, or a meeting that needs a reply first.
2. **Someone is blocked on the user,** including any response standard the user has set for a process.
3. **Ladders to a goal:** today's MIT, then weekly, then longer-term goals. Name the goal.
4. **Relationship cost of delay,** using the user's staleness signals. Age supports a ranking; it never overrides consequences.

## Step 5: Snapshot and questions

Show the sorted result, then ask two to four questions in one plain-text numbered block, with lettered options so the user can reply `1b, 2a`. End the turn and wait.

```
## Inbox zero: <date>, <sources>

**Goals used:** <longer-term> · <week> · <today's MIT>
**Missing data:** <failed or incomplete sources, or "none">
**Counts:** <N items: X do now, Y quick wins, Z delegate, T task, D delete>

### Do now
1. <item> — <source, sender, age> — <why> — <link>

### Quick wins
- <item> — <the one action> — <link>

### Delegate
- <item> — <suggested owner and evidence, or "owner unclear"> — <link>

### Task
- <item> — <suggested task name, due date> — <link>

### Delete
- <counts by type, plus any surprising item>
```

Use a real list for every group. Show severity with labels and order, never color alone.

Example question block:

```
1. Is the partnership goal still live this week? a) yes b) paused
2. The scheduling thread with the external partner: a) handle it yourself b) delegate
3. How much time do you have? a) 15 min b) 30 min c) an hour
```

Ask only about real uncertainty: whether a goal is still live, whether the user wants to handle a sensitive thread personally, whether an unfamiliar sender matters, or how much time is available. Do not ask what the data already answers. If nothing is uncertain, ask about time. The user's bucket choices are final.

## Step 6: Work the buckets

Go in this order and stop whenever the user wants.

1. **Do now, one at a time.** Read the full thread and check the calendar around any dates it mentions. Gather only the context this decision needs. For hiring or assessment items, use only authorized, role-relevant evidence: required capabilities, role alignment, diagnostic evidence, and whether the assessment step distinguishes relevant performance. Then give one short paragraph: who this is, what they want, what is at stake if the user waits, and your recommended action, with evidence linked. Ask one to three questions only the user can answer. When they say it is handled, move on.
2. **Quick wins.** List them together for one clearing sprint.
3. **Delegate and Task.** The user confirms owners and tasks. Create a task only for each item they say to task.
4. **Delete.** Remind the user what to archive or delete; they do it.

**Drafts, only when asked.** Give one copy-ready plain-text draft per response, as the final block. Follow the user's writing guidance and the channel's norms. Keep claims factual and make no commitments the user has not approved. Do not save drafts into the email or chat system unless authorized.

**Creating a task.** Create one record with an action-style title, open status, implied due date, and whatever other fields the user's system uses, such as importance, urgency, time estimate, or project. Notes:

```markdown
**What:** one line: the ask and who is waiting.
**Source:** <link, or "service: person, date">
**Context:**
- Key fact or constraint, with link.
- Relevant deadline or decision.
**Next step:** the first concrete action.
```

Do not pre-draft replies in the task unless asked. Afterward, tell the user the item can leave its inbox and give the task link if one exists.

## Step 7: Close and improve

End with a short status per source: cleared, tasked, delegated, still open, or unreviewed because of access or time. If many loops remain open, say so plainly.

Review the run for friction: a pointless question, a wrong bucket, a misbehaving source, context you had to hunt for, or a privacy risk. With permission, update the user's workflow notes or setup choices to fix the cause. Keep changes general, and never store message content, credentials, or personal details.

## Single-item mode

Use this when the user, or a reminder they set up, points to one specific item.

1. Skip goal reading, full collection, sorting, the snapshot, and the closing review. Do not read other inbox items.
2. Read the item using the principles in Step 3, under its source's access rules.
3. Treat it as one Do now item: who, what they want, and what happens if it waits. Recommend one bucket and the next action, with its link.
4. Help the user finish it under the normal rules for drafts and tasks.
5. Tell the user which inbox action clears it. Do not require a special confirmation phrase.

## Common failure modes

- Doing the work a message describes instead of deciding where it belongs.
- Treating unread or recent as urgent.
- Taking inbox actions or creating tasks without a per-item instruction.
- Trusting a cut-off or empty result, or quietly skipping a failed source.
- Guessing a delegate from outdated role information.
- Duplicating a task that already exists.
- Pulling more personal context than the decision needs.


---
name: design-a-work-sample
description: Create or improve a short, paid, asynchronous work sample that yields job-relevant evidence, using an alignment memo, shape options, simulated submissions, and readiness checks.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise, often called a work test or take-home. It usually sits between application review and interviews. Done well, it is one of the most useful stages in a hiring process because it produces evidence that is hard to fake about whether a candidate can do the core work. Done badly, it wastes candidate time, floods reviewers with low-value submissions, and lets role-misaligned hires through.

The workflow is opinionated about process. Agree on what you are measuring before drafting anything. Choose a task shape deliberately. Draft against a standard template. Then check the exercise with simulated submissions before calling it done.

## When to use this workflow

Use it when someone asks to design a work sample for a role, revise an existing one, or tighten one that is not producing useful evidence. Detect whether the request is to create or improve. If the role is not named, ask once.

Do not use it for:

- Interview questions, interview panels, or interview scoring rubrics.
- Multi-day or in-person work trials.
- Screening questions on an application form.

If the request could be any of these, ask once which format is needed.

## Core principles

- **Measure a few things well.** Focus on three to five load-bearing abilities that matter for the role and can be observed in a few hours. Leave the rest to interviews, trials, and references.
- **Do not test what can be trained quickly.** Familiarity with a specific tool, internal process, or domain vocabulary can often be learned in a few weeks by a capable hire. Do not spend the exercise on it. No item should require specialist knowledge unless that knowledge is truly essential on day one.
- **Keep grading fast.** Aim for about 20 minutes per submission and no more than 25. A long exercise that reviewers cannot score consistently is worse than a short one they can.
- **Prefer substantive outputs over many small ones.** One piece of real reasoning, several real drafts or decisions, and one reusable artifact reveal more than dozens of shallow micro-decisions.
- **Pay candidates.** State the amount and process clearly. Do not ask for production work the organization will use unless that is separately agreed.
- **Keep it self-contained.** Candidates should not need internal tools, private data, or real people.
- **Assess only role-relevant capabilities.** Exclude protected characteristics and unrelated proxies. Offer a route for reasonable accommodations or an accessible equivalent format without lowering the role-relevant standard.
- **Handle hiring materials with care.** Use only materials the team is authorized to use for this role. Read the minimum relevant information, omit unrelated or sensitive personal details, and keep memos, simulations, and reviewer notes inside the hiring team's access boundary.

## Hard rules

1. **Pre-flight requires a role description and a role-success profile.** Do not design an exercise without both. Do not accept "we will figure out the profile while designing the test." The exercise is a function of the profile and produces noise without one.
2. **Alignment memo before any draft.** Produce a one-page memo on what the exercise tests and why, and get explicit confirmation before drafting.
3. **Two simulated submissions before declaring version 1 done.** One from a role-aligned persona, one from a plausible role-misaligned persona. This regularly reveals gaps that analysis misses: a trait that does not actually separate candidates, a noise item that is too obvious, or a rubric that rewards the wrong behavior.
4. **Candidate-facing text must read as human-edited.** Apply the format checks below on every pass.
5. **Every draft ends with notes for the hiring owner.** Three to six bullets on choices they may want to change.
6. **Each revision is a full copy.** Output the complete updated exercise, not a diff, so it can be pasted straight into the hiring system.

## Step 1: Pre-flight

Look in the user's chosen hiring and documentation systems for:

- A current role description: responsibilities, level, outcomes, reporting line.
- A role-success profile or hiring plan: the capabilities and experience most likely to produce the role's outcomes.

If either is missing, stop and say:

> Before we design the work sample, we need a role description and a role-success profile. I found [the role description at its location / no role description yet] but [could not find a profile]. Want me to help draft the missing piece first? It is a short job and saves us iterating the exercise against a moving target.

Do not proceed until both exist.

## Step 2: Read the context

Read the full role context: the hiring plan, the profile, design notes, linked sub-pages, and the public role description. Also read one or two existing work samples from the organization, if available, to calibrate tone, length, and structure. Use them for format only. Different roles need different shapes; do not force a shape onto a role because it worked elsewhere.

Give a one-line status: "Read [N] pages of role context and [N] reference exercises. Moving to the alignment memo."

## Step 3: Alignment memo

Write a one-page memo titled **What we are testing for and why: [Role] work sample**. Include:

1. **Load-bearing traits (three to five).** Abilities the role succeeds or fails on that the exercise can surface in the time window. Phrase them as observable capabilities. Weak: "strategic thinking." Better: "identifies the highest-leverage problem in a messy situation, explains the tradeoff, and ships a useful first action."
2. **What we are explicitly not testing.** Important qualities assessed elsewhere: interviews (motivation, live reasoning, conversational sharpness), work trials (consistency over days, judgment under sustained pressure), references (reliability over months, integrity, manager fit). Naming these forces honesty about the exercise's limits.
3. **Calibration to level.** Junior, mid, senior, or leadership. This drives payment, expected output volume, and how much context the candidate needs. Junior candidates may need more context and narrower deliverables; senior candidates may need to set direction and create work another person could use without explanation.
4. **Failure modes to catch.** Two or three specific patterns of role-misaligned work you want to filter out, described as observable behavior. Examples: a polished planner who does not ship; a fast executor who misses the central problem; a careful candidate who defers every meaningful call.
5. **What strong looks like.** One paragraph describing a top submission: what it notices, what it decides, what it produces, how it handles uncertainty.

Present the memo and stop. Ask: "Does this match what you want to test for?" Do not continue until the owner confirms or amends it.

## Step 4: Propose three shapes

Once the memo is locked, propose three shape options. Each must test the load-bearing traits in a different way, be gradable in about 20 minutes, be self-contained, and be graspable by a candidate in about 60 seconds.

For each option give: the shape, what it tests, two sentences on why it is evaluable, and one main risk. Keep each to about 150 words.

Shapes that often work:

- **Triage pile.** For volume-heavy, communication-heavy roles. The candidate receives a start-of-week pile of eight to ten items, writes a plan, ships drafts, and picks one systemic fix.
- **Pick the highest-leverage thing and ship it.** For strategic operations and builder roles. The candidate picks one priority from a brief and ships a minimum viable version.
- **Diagnose and ship one fix.** For pattern-recognition roles. The candidate reads a messy situation, writes a diagnosis, and ships one targeted fix.
- **Source and pitch.** For recruiting, outreach, or partnerships roles. The candidate picks a target, defines the bar, finds non-obvious channels, and drafts outreach.
- **Decision-useful analysis.** For research, policy, or strategy roles. The candidate chooses one of two areas and produces a take a decision-maker could act on.
- **Design and systems.** For community, program, or enablement roles. The candidate designs one thing (an event, a process) and a repeatable system around it.

If none land, propose three more based on the confirmed traits. Do not draft until the owner picks a shape.

## Step 5: Draft version 1

Fill in the standard template for the chosen shape, applying every format check as you write. End with the notes section.

### Standard template

Section headers after the title are bold lines rather than headings, which pastes cleanly into most hiring systems. Replace bracketed placeholders.

```markdown
## [Role] Work Test

This work test assesses your ability to [two or three trait verbs from the memo].

You have **[3] hours** total.

**Your mission**

[One paragraph. A specific situation, not an abstract task. Include any authority frame or unreachable-stakeholder constraint that forces decisions. End with one line restating what the candidate will produce.]

**Deliverables**

[Two to four parts with rough time guidance. Common operations pattern: Part 1 plan or analysis (about 45 to 60 minutes, roughly 400 to 500 words, shorter if sharp, naming what they are choosing to skip). Part 2 ship the work (about 75 to 90 minutes, five to seven actual drafts; don't let the planning eat the shipping). Part 3 one systemic fix (about 20 to 30 minutes, usable by a teammate without further explanation).]

**Context**

[The program, project, or operation. Length, audience, current state. If relevant, "People you can reach this week," with deliberate availability choices.]

**Instructions**

- Spend **[3] hours** completing this work test.
- Submit **within [7] days** of receiving this message. The sooner the better.
- Submit a **single document or PDF**. If you built supplementary materials (a spreadsheet, diagram, or database), include links with sharing enabled.
- **This is a paid work test.** After submitting, request **[$BASE](BASE_PAYMENT_LINK)** payment. We care about speed, so **we will pay you [$BONUS](BONUS_PAYMENT_LINK) if you submit within [3] days**.
- You may use AI tools, but use them carefully and with judgment. Please do not submit fluff.
- Show your **unique depth or sharpness** somewhere in your submission. Don't try to be comprehensive everywhere; invest your time where it shows what you can do.
- Most strong submissions include a **scrappy 3 to 5 minute video** walking through the work. Don't polish it. One minute of thinking out loud beats five minutes of rehearsed narration.
- If you need an accommodation or alternative format, contact [named role or contact channel].

**Anticipated questions**

- *A requirement is unclear. What should I do?* Make a reasonable assumption (imagine you asked us and the answer didn't surprise you). Note the uncertainty and your assumption briefly.
- *What if I don't finish in [3] hours?* Submit what you have and add a note on where you got to and what you would do next.
```

Optional additions:

- **Extra anticipated questions:** a timezone frame for scenario tests ("Respond as if you are at your desk in [location] on [day] morning; no need to adjust for your own timezone") and "How will my work be used?" ("Only to evaluate candidates for this role; any other use we will agree with you separately").
- **The pile,** after Context, for triage shapes: eight to ten realistic items with timestamp, source, and full text where communication matters. Several items should connect so that seeing the whole picture is rewarded. Add **Reference notes** with the data needed to make fair calls, such as a backup pool, escalation policy, or refund policy.

### Payment structure

Let the hiring owner set amounts. A broadly useful structure is a base payment for submission within seven days and a higher payment for submission within three days. Scale by level, but keep amounts modest and symbolic relative to senior pay rather than escalating indefinitely.

| Role level | Base (within 7 days) | Early bonus (within 3 days) |
|---|---|---|
| Junior | [lower base amount] | [base plus a modest increment] |
| Mid, senior, and above | [standard base amount] | [standard base plus a modest increment] |
| Speed-critical, high-volume roles | [lower base] | [middle amount; add a third, highest tier for submission within 24 hours] |

If payment is requested through a form, create two prefilled links, one for each amount, with the role name and amount filled in. Hyperlink the dollar figures themselves, not words like "this form."

### Notes for the hiring owner (not for the candidate)

End every draft with three to six tight bullets on choices worth challenging. Good examples:

- "I split the problem across two groups to test whether candidates spot the cluster. It is a little contrived; easy to concentrate it in one group instead."
- "Item 6 is obvious noise that takes five seconds to skip. Drop it or make it subtler; right now it doesn't separate candidates."
- "Payment matches our other senior exercises. For a volume role we could add a 24-hour tier."
- "I didn't include a short video brief from the project owner. It adds realism but costs production time."

Close with one question pushing the next decision, such as "Where do you want to push first?"

## Step 6: Iterate

Expect three to seven rounds. Each round, output the full updated exercise. Common feedback: too vague (tighten), too prescriptive (loosen), cut a section (cut and renumber), unrealistic scenario (check facts such as program length, numbers, and pricing), and format problems spotted late. Apply feedback directly. If you disagree because something would harm validity, fairness, or safety, say so once, briefly, then apply the owner's decision.

## Step 7: Simulate two candidates

When the draft is close to done, run two simulations in parallel, each given the full candidate-facing text.

- **Role-aligned persona:** a strong candidate matching the role-success profile. They produce a real submission for every part, as they would type it, plus about five sentences of reflection on choices, uncertainty, and time use.
- **Plausible role-misaligned persona:** an earnest, conscientious candidate who would pass screening at many organizations but whose work lacks one role-critical capability. Pick a mismatch from the memo: process-driven where the role needs bias to action, hedging where it needs decisiveness, designing elaborate frameworks where it needs a builder. Tie the difference to work evidence only, never identity or background. They produce the same submission, in character.

Then write a synthesis:

1. **Where the exercise separated them sharply.** Items or parts with visibly different answers.
2. **Where it did not.** Items both handled the same way. Floor checks are fine, but a load-bearing trait that produces no difference is a problem.
3. **What this tells us.** What the exercise does and does not predict.
4. **Improvements,** specific and ranked by impact.

## Step 8: Apply improvements

Rewrite and output the full exercise. Typical fixes: make pile items more interconnected, make obvious noise subtler, make a stakeholder truly unavailable, replace an opinion prompt with a usable deliverable, tighten word guidance, clarify the rubric so reviewers reward the intended behavior, and remove trainable-knowledge requirements. Make the exercise more diagnostic, not merely harder.

## Step 9: Optional external review

If others have reviewed it, assess each suggestion against the memo, state which to integrate and which to skip with reasons, and output the full updated version. External review is input, not orders; the hiring owner decides.

## Step 10: Final polish and readiness gate

Before declaring done, confirm:

- Format checks pass (below).
- Scenario details are realistic for the organization: plausible program names, team roles, and numbers.
- Payment amounts and links are correct and attached to the dollar figures.
- Section order matches the owner's preferred layout. A common order is Mission, Deliverables, Instructions, Anticipated questions, with Context and the pile either in a separate document or appended at the end.
- The exercise fits the stated time for a qualified candidate and can be graded in about 20 minutes.
- Both simulations ran and led to any needed revisions.
- No sensitive data, real contact details, or unpaid production work remain, and accommodation routes and proxy bias have been checked.

## Step 11: Capture lessons

Keep a running notes file for this workflow in the user's chosen location. After each run, add anything learned: new format problems, wording the owner flagged, shapes that worked, failure modes the simulations revealed, payment changes, better template wording. Show a one or two bullet summary. Make small additions directly; ask before structural changes such as adding a step or dropping the simulation.

## Format checks for candidate-facing text

These are signs of unedited machine output or rendering problems. Sweep before every output.

- Use dashes sparingly; prefer commas, semicolons, periods, and parentheses.
- Write "by the end of [day]," never "by end of [day]."
- No horizontal divider lines between sections; use bold headers instead.
- No tables if the destination editor does not render them; use bullets with bold leads.
- Avoid punchy "X, not Y" taglines, "it's not just X, it's Y" constructions, repeated sentence openings, and stacked three-part lists.
- Use the locale the organization operates in, consistently.
- Put message sign-offs on two lines (the closing word, then the name on its own line).
- Use clearly fictional names and contact details in fictional items. For addresses, use a domain reserved for documentation and examples rather than one from a real provider, because realistic-looking contact details can lead candidates to try to reach them. Do not wrap addresses in angle brackets, which can trigger autolinking.
- If pasting Markdown into a document editor collapses single line breaks, end each metadata line in message or chat headers with a soft break such as `<br>` so fields stack like a real header. Avoid blank lines in those stacks; bullets are unaffected.

## Common failure modes

- Designing the exercise before the memo is locked, which wastes rounds of iteration.
- Testing trainable skills or specialist knowledge instead of durable judgment.
- Exercises that take more than 25 minutes to grade.
- Many shallow micro-decisions instead of a few substantive outputs.
- A pile of independent items, which tests volume rather than pattern recognition.
- Reachable stakeholders who let candidates defer every decision when decisiveness matters.
- Generous word targets that make weaker candidates pad; prefer "about 400 to 500, shorter if sharp," or none.
- An optional video nobody records; framing it as something most strong submissions include surfaces confidence.
- Declaring success without checking that the exercise separates role-relevant performance.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, quick to grade, and clear about what good looks like.


---
name: run-a-reference-call
description: Prepare a reference call page for a hiring candidate by gathering authorized context, writing an internal briefing, and building a tailored question list for the call.
---

# Run a reference call

Use this workflow when a hiring team member (the "interviewer") is checking references on a job candidate. The deliverable is a **prepared meeting page** in the user's chosen notes or document system, not a chat summary. If you present research without creating the page, the task is not done.

**Direction check:** this workflow covers checking references on a candidate *your* organization may hire. If an outside organization is asking you to give a reference about someone, use a different workflow.

## Privacy and authorization

Before you search anything, confirm:

- The candidate has agreed to reference checks, and the referee was provided by the candidate or has agreed to speak.
- The user is authorized to access the communication and recruiting systems you will search.
- You will use only information relevant to the hiring decision: the role, the working relationship, and professional background.

Do not collect or record unrelated personal details (health, family, finances, beliefs, or other protected characteristics). Research the referee only enough to understand their professional role and relationship to the candidate. Keep the page inside the hiring team's access boundary, and tell the referee how their input will be handled.

## Inputs

| Input | Notes |
|---|---|
| Candidate name | The person being hired |
| Referee name and contact | May come from a calendar invite or email thread |
| Role | Look it up from hiring records if not provided |
| Call date | Default to today, or take it from the calendar |

## Steps

Run every step in order. Do not stop after research.

### Step 1: Find the scheduled call

Search the user's calendar for an event with the referee's name or contact. Extract the title, time, attendees, video link, and any scheduling notes. If there is no event yet, note that and continue.

### Step 2: Gather context

**2a. Hiring context.** Search the user's email and hiring records for the candidate to learn:

- The role they applied for
- Their current stage (interview, work trial, final stage)
- How the referee was introduced (the candidate's reference list message is usually the key source)
- The referee's relationship to the candidate (manager, client, colleague, teacher)

**2b. Referee research.** Run these searches, in parallel where possible:

1. Direct correspondence with the referee's contact
2. Mentions of the referee's full name (intro emails, scheduling threads)
3. Team chat, by referee name and by their organization name
4. Notes system, for any prior meetings with the referee
5. Calendar, for past events with the referee
6. Public web, for their professional role and organization only

Read the most recent three to five results from each email search.

**2c. Candidate links.** Collect links the interviewer will want during the call: applicant tracking profile, professional profile, portfolio, or code samples.

**2d. Completed references.** Search for other reference pages for the same candidate. Read any completed ones and extract themes: strengths, concerns, and development areas. These become specific angles to confirm or test in this call.

**2e. Compile.** Synthesize:

- Who the referee is: role, organization, short background
- How and for how long they worked with the candidate, and how closely they saw the relevant work
- Hiring context: role, stage, next step dates
- Candidate links
- Other referees on the list
- Briefing notes (see template)

### Step 3: Create the meeting page

This step is mandatory. Create the page in the user's chosen meetings location, with properties and content together if the system allows it.

- **Title:** `{Date} {Referee Name} ({Candidate Name} reference)`
- **Date:** the call date (date only)
- **Attendees:** the interviewer, plus anyone else from the hiring team joining

If the notes system offers an in-meeting transcription or notes widget, add it at the top with only the meeting title, and only if the referee will be told about and agree to any recording or transcription. Leave summary and transcript fields empty for the system to fill.

## Page template

```markdown
## Context
- {Referee Name} ({profile link}): {role, organization, one-line background}.
- {Candidate} worked with {Referee} as {relationship, duration, closeness}.
- Reference call for {Candidate Name} ({tracking profile}, {other links}), who is at {stage} for {Role}. Next step: {work trial or decision date}.
- {Any prior relationship between our organization and the referee.}
- Other references: {list}.

## Opening
> Hi {Referee}, thanks for making the time. I'm {Interviewer}, {title} at {Organization}. We {one-line description of the organization}. {Candidate} has applied for our {Role} role, and we're excited about their background. We're doing reference checks so we can decide quickly. What you share stays within our hiring team.

## Briefing notes
- **Themes from completed references:** {What earlier referees said, attributed internally. E.g., "Referee A said the candidate struggled to finish the last part of projects. Ask whether this referee saw the same."}
- **What this referee is uniquely placed to speak to:** {Based on their relationship, what can they tell us that others cannot?}
- **Organization or relationship context:** {Shared channels, past meetings, collaborations.}
- **Open questions:** {Concerns or gaps from the hiring process.}

## Questions
- **How did you work together?** What was {first name}'s role, and yours? How closely did you work day to day?
- **What did they concretely deliver, and how did it compare to your expectations?**
- **What is their standout strength?**
- **If they joined and it didn't work out after three months, what would be the most likely reason?**
- **If things are going well at three months, what development area would I most likely make their top priority?**
- **Compared to others you've worked with in similar roles, where do they rank?**
- **As their manager, what could I do to get the most out of them?**
- **What should I have asked that I didn't?**

### {Role}-specific probes
- {Probe 1}
- {Probe 2}
- {Probe 3}
- {Probe 4}
```

If no references are complete yet, say this is the first one and list what to watch for so later calls can cross-check.

## Role-specific probes

Write three to four probes tied to the role's core capabilities. Examples:

| Role type | Example probes |
|---|---|
| Program or operations specialist | Handling ambiguity and changing requirements; building systems vs. solving problems as they arise; written and spoken communication with non-technical stakeholders; spotting what needs doing without being told |
| Community lead | Building and energizing a community, with examples; handling conflict or difficult members; creating processes vs. relationship-focused work; identifying what the community needs |
| Head of operations | Scaling operations at a growing organization, and what broke; competing priorities from many stakeholders; owning vendors, budgets, and contracts; balancing speed and process |

## Running the call fairly

- Ask neutral questions. Never tell the referee what another referee said or name them; turn earlier themes into open questions ("How did they handle finishing large projects?").
- Follow vague praise with "What did that look like?" or "Can you give an example?"
- Weight evidence by direct observation of relevant work, not the referee's title or confidence.
- Afterward, separate what the referee observed, how they interpreted it, and your own inference. Note limits on what they could know. Do not treat one reference as a final verdict.

## Style rules

- Context is short bullets, not paragraphs.
- Questions are one unified bullet list, not numbered or split into sections, apart from role probes.
- Tailor the opening to the referee and candidate, and adjust tone if there is prior contact.
- **Briefing notes are the most valuable section.** The interviewer will not read the chat, so everything useful must be on the page. Write directly ("Referee A said X. Ask if this referee sees the same."), not with hedges ("it may be worth considering...").
- Always list the candidate's other references so the interviewer sees the full picture.


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

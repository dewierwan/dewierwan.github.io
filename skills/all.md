# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision, weigh their tradeoffs honestly, and recommend a short ranked set. Use when someone asks for options, alternatives, or ways they could approach something.
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
description: Find the weak points in a strategic idea before committing to it, through a steelman, assumption tests, a pre-mortem, and a verdict. Use when someone asks to stress-test an idea or wonders if they are wrong.
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
name: decide
description: Match decision rigor to stakes and reversibility, make a clear call, record it with a prediction, and review it later. Use when someone asks for help deciding, weighing X against Y, or reviewing a past decision.
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
description: Take a non-trivial build or process problem from diagnosis through options, recommendation, implementation, and verification. Use when someone wants a problem solved end to end, or analysis only before building.
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
description: Shape a high-stakes document through evidence review and rounds of questions until the thinking is settled, then draft and audit it. Use when writing a strategy doc, proposal, or decision memo that must land.
---

# Shape and draft a document

Develop an important document by shaping the thinking behind it before writing. Earn the draft. First work out what the document must achieve. Then gather the relevant evidence and resolve the material choices with the person who has authority to make them. Draft only when the remaining uncertainty will not materially change the result.

Use this workflow for strategies, narratives, operating agreements, proposals, scorecards, decision memos, and hybrids when the argument, commitments, boundaries, operating model, or document form is not yet settled. Use a lighter process for simple edits, formatting work, or documents whose decisions and content are already clear.

If you review private communications, internal records, or information about people, do so only for a legitimate purpose and with clear authorization. Use the minimum relevant sources and information. Leave out unrelated or sensitive personal details, respect consent and privacy expectations, and keep the draft within the access boundary that fits its audience.

## Classify the request

A request may name a proposed document, a desired outcome, an audience, source material, or some combination. Treat any proposed document type as a hypothesis until its purpose is clear.

Use the **full shaping process** when the document is consequential and its argument, boundaries, commitments, or operating model are still materially unsettled. Also use it when the requester explicitly asks for deep thinking, many questions, multiple rounds, or close alignment before drafting.

A substantive round resolves a distinct layer of choices and uses the answers to decide the next layer. Restating the situation, asking for general approval, or repeating answered questions does not count as a round.

## 1. Work backwards from the outcome

Start with the change the document needs to produce. Establish:

- Who will read it.
- What they should understand, decide, approve, or do afterward.
- What is unclear, contested, blocked, or going wrong now.
- Whether the document mainly needs to explain, persuade, decide, coordinate, or govern.

Do not accept 'write a narrative' or 'make a strategy page' as the goal. Identify the job the document must do.

## 2. Choose the artifact

Recommend the form that best serves the goal:

- **Narrative:** Builds shared understanding of why something matters and what bet is being made.
- **Strategy:** Connects a diagnosis to choices, priorities, outcomes, and exclusions.
- **Operating agreement:** Defines ownership, interfaces, decision rights, handoffs, and cadence.
- **Decision memo:** Records a choice, the alternatives, the rationale, the risks, and a review point.
- **Scorecard:** Defines a role or team mission, its outcomes, and the role-relevant capabilities it needs.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the tradeoff and recommend one form. If the choice of form is load-bearing, because it would change the argument, structure, or decisions required, ask the decision-maker to confirm it before going deeper.

## 3. Gather and classify the evidence

Read supplied material first. Follow any stated rules for source selection, authority, and citation. Scale the research to the stakes. For a consequential internal document, search the authorized sources most likely to hold prior decisions, current definitions, relevant evidence, dissent, constraints, and ownership context.

Apply these rules:

- Respect any stated source-of-truth hierarchy.
- Treat discussion notes, recollections, and generated summaries as weaker than current, authoritative decision records.
- Resolve contradictions where the evidence allows, and surface the ones that remain.
- Do not ask the decision-maker for facts that available sources can answer.
- Do not modify any source document unless explicitly asked.

Keep a strict boundary between evidence and alignment:

- Sources can establish what happened, what people said, and what an authoritative record currently states.
- Sources do not establish what the decision-maker now believes, wants to promise, or is willing to exclude, unless they contain an explicit, current decision from that person.
- A synthesis, a repeated theme, or a plausible implication is **inferred**, not settled.
- Ask for confirmation of any inference that would become a central claim, commitment, boundary, or recommendation.

Before the first interview round, give a short situation brief covering:

- What the sources establish.
- What the decision-maker has already confirmed.
- What you infer but have not confirmed.
- The central tension or missing logic.
- The artifact you recommend.
- The important uncertainties that only the decision-maker can resolve.

## 4. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds that already happened in the current conversation, and do not repeat them. Do not draft right after the first answer round just because one apparent core tension seems resolved. The second round should test the implications, boundaries, counterarguments, or execution details the first round revealed.

Ask four to eight focused questions per round. If fewer than four material questions genuinely remain, ask all of them and say this is a narrow final check. Do not pad a round with ritual questions.

Each numbered question should normally contain one decision. Do not bundle independent choices, such as ownership, coordination, handoffs, and success measures, into one yes-or-no question. A broad answer to a bundle creates false alignment.

**Deliver each round once, on one answer surface.** Put the situation brief or updated synthesis and the questions in the same message, at the end of your turn, so the respondent can read them together and reply in shorthand. Do not also send the same questions through a separate form or question tool, because two answer surfaces can produce conflicting or stale answers. If a form is required, show the questions there once with the context needed to answer them. Progress depends on what has actually been answered, not on what an interface shows as pending.

Format questions for fast, unambiguous replies:

1. Number every question (`1.`, `2.`, `3.`). Continue numbering across rounds and keep each number tied to the same question, so compact replies stay clear.
2. For bounded choices, default to three or four mutually exclusive, decision-relevant options labeled `a.`, `b.`, `c.`, `d.`. Binary questions hide useful middle positions, so use two options only when the decision truly has two states. Do not invent fake alternatives.
3. Make the recommended option `a.` unless the conversation makes another order clearer. This allows replies like `1a, 2c, 3b`.
4. Render the block as a compact, single-spaced list, with each question and option on its own line and no blank lines inside the block.

Example:

1. Which direction should the document recommend?
   a. Focus first on the highest-impact problem; this narrows scope but makes accountability clear.
   b. A more cautious, phased direction.
   c. A more ambitious direction that addresses all related problems.
   d. Leave this deliberately open for now.
2. Who should own it?
   a. The program lead.
   b. The functional lead.
   c. Shared ownership with one named decision-maker.

Each round should:

1. Start with the updated model and what changed because of earlier answers.
2. Focus on one layer of uncertainty.
3. Offer concrete options where the choice can be bounded, recommended option first, with a brief tradeoff.
4. Leave room to reject the framing or give a different answer.
5. Notice contradictions and ask the smallest question that resolves them.
6. Separate what the sources suggest from what you are asking the decision-maker to decide.
7. Include at least one pressure test of the emerging position when the document is persuasive or strategically consequential.

A typical progression of layers:

1. **Purpose:** audience, desired effect, artifact type.
2. **Strategy:** diagnosis, central bet, priority, scope, exclusions.
3. **Operating model:** owners, interfaces, handoffs, decision rights.
4. **Definitions:** thresholds, edge cases, success measures, evidence standards.
5. **Expression:** tone, length, destination, and any deliberate open questions.

After every answer round, do all four steps before deciding whether to draft:

1. Match shorthand and free-text answers to their question numbers, keeping qualifications such as 'mostly c' or 'not sure'. Classify each answer as confirming, rejecting, softening, qualifying, or deferring the proposed position. Mark only genuinely unanswered or unclear material choices as open.
2. Trace downstream implications. A changed audience, softened commitment, new exception, or rejected framing usually creates another question.
3. Update the alignment ledger and show a concise summary of it.
4. Build the next round from the remaining material uncertainties and the consequences of the answers.

Adapt the content of the rounds to the task, but keep the answer-dependent loop. Continue while an open issue could materially change the draft. Stop interviewing once only low-impact uncertainty remains and the readiness gate is met. If the requester asks to skip further questions and draft now, briefly name the material consequence and follow the instruction.

## 5. Maintain an alignment ledger

Keep a compact working record throughout the conversation:

| Category | Meaning | Current entries |
| --- | --- | --- |
| Confirmed | Choices the decision-maker explicitly made, including earlier ones in the conversation | [entry] |
| Source facts | Claims established by current, authoritative evidence, but not choices | [entry] |
| Inferred | Your interpretation, clearly marked as not yet a decision | [entry] |
| Open | Questions that could materially change the document | [entry] |
| Corrected | Assumptions or source claims the decision-maker has rejected | [entry] |

Update the ledger after every answer round, before asking more questions. Never reintroduce a corrected assumption. When two confirmed statements conflict, surface the conflict and resolve it instead of smoothing it over. Never promote an inference to confirmed just because several sources support it.

For a full shaping process, do not keep the ledger implicit. Show a concise version before each later round so the decision-maker can catch mistaken assumptions. Every major claim planned for the draft must be confirmed, a source fact, or deliberately presented as a proposal or open question.

## 6. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document's substance. Before drafting, explicitly run the gate and give a short pre-draft synthesis: the intended job, the audience, the central position, the important boundaries, and any deliberate open questions.

For each major claim in the planned outline, ask: **Was this confirmed by the decision-maker, established as fact by an authoritative source, or am I only inferring it?** If a material claim is only inferred, ask another question instead of drafting.

Check that each relevant category is confirmed, evidence-based, deliberately left open, or genuinely not applicable:

- Goal and audience.
- Artifact type.
- Central argument or bet.
- Scope and exclusions.
- Definitions and thresholds.
- Ownership and decision rights.
- Interfaces and handoffs.
- Success measures and evidence standard.
- Tone, length, and destination.

For persuasive documents, also do a skeptical-reader pass:

- What is the strongest objection from the actual audience?
- Which premise, commitment, evidence claim, or safeguard would they dispute?
- Has the decision-maker confirmed the response the draft will give?

Resolving one central tension is not enough if the draft still depends on unconfirmed positions about the theory of change, scope, relationship model, commitments, evidence, or exclusions.

Close alignment is not a literal probability. It means the remaining uncertainty is low impact, or the document openly presents it as unresolved. If the requester asks for the draft before the gate is met, name the one or two consequences of the uncertainty and follow the instruction.

## 7. Draft in the requested voice

Apply any voice profile, style guide, or delivery rules the user has supplied. If none exist, write in clear, direct language that suits the audience and sounds like the document's owner rather than an outside consultant.

Write the smallest document that can do the job. Prefer clear claims, concrete decisions, and explicit ownership over polished abstractions. Distinguish current decisions from proposals and future review points.

Keep the structure readable:

- Do not let a section become a long, flat inventory. For action or onboarding documents, keep each section to seven top-level bullets at most, and prefer five or fewer for the main outcome section.
- If more points seem necessary, cut them, combine them under a clear lead phrase, or move detail to a linked reference.
- Make sure a heading after a list is truly separate from it. It should not inherit bullet or numbering formatting, and there should be no stray empty paragraph between them. Format conversions often cause both problems.
- Inspect the rendered output, not just the underlying structure. Fix uneven indentation, bullets that render as numbers, orphaned bullets, and awkward page breaks.

Make the draft as simple as the substance allows. The hard thinking should produce a document that is easy to read, not one that displays how complex the thinking was.

- Prefer short, common words over formal or fancy ones.
- Write complete, natural sentences. Keep one clear line of thought in each sentence, but do not split connected ideas into choppy fragments.
- Let sentence length follow the thought. A longer sentence is fine when it makes a connected argument easier to follow.
- State the point first. Cut warm-up text, repeated context, process narration, and throat-clearing.
- Turn abstract ideas into concrete claims, actions, examples, owners, dates, or tests.
- Cut qualifiers and side points that do not change a decision or action.
- Use focused paragraphs. Use bullets only for real lists, and write each bullet as a full sentence unless it is a compact label.
- Prefer the more concise version when it keeps the meaning. Concise means removing unneeded ideas and words, not shortening every sentence.

Do not flatten the substance. Keep a hard idea when it matters, and explain it in the simplest language possible.

Honor the requested destination in the user's chosen system. If text was requested in the conversation, do not edit the source document. If a document must be created or edited, do so with the appropriate tool and verify the result.

## 8. Audit before delivery

Compare the draft with the alignment ledger and the source hierarchy:

- Does it solve the agreed problem in the agreed form?
- Does every material choice reflect the decision-maker's answers?
- Are corrected assumptions gone?
- Are responsibilities, boundaries, and handoffs unambiguous?
- Are uncertain claims marked as such?
- Are factual claims and links supported by sources?
- Is anything presented as settled that was only inferred?
- Does it match the requested voice, audience, access boundary, and privacy expectations?
- Can each sentence be understood on first read?
- Are prose and bullets written as full, natural sentences rather than clipped fragments?
- Can any fancy word, abstract phrase, or repeated point be simplified or cut?

Fix any mismatch before delivering. Put the deliverable last, with no trailing summary or offer that gets in the way of copying it.

## Failure modes

- Drafting early because producing text feels useful.
- Treating the proposed artifact as fixed.
- Asking questions before researching facts the sources can answer.
- Mistaking extensive research for alignment with the decision-maker.
- Treating a plausible synthesis as a decision.
- Sending a generic questionnaire disconnected from the evidence.
- Failing to update the model after each answer.
- Drafting after one round because a single core tension seems resolved.
- Bundling several independent decisions into one question.
- Skipping a consequence round after a claim is softened or qualified.
- Repeating a question that has already been answered.
- Running the same round on two answer surfaces, or treating a stale queue as missing answers.
- Hiding a contradiction behind vague language.
- Continuing the interview after only low-impact uncertainty remains.
- Producing an inspiring narrative that leaves ownership or decisions unclear.
- Including personal or sensitive details beyond the audience's legitimate need.
- Mistaking concise writing for choppy writing through fragments, noun-only bullets, or forcing every sentence to be short.


---
name: gather-context
description: Search the sources that matter, at a depth that fits the stakes, and turn the findings into one brief where every claim links to evidence. Use when someone wants to get up to speed on a person, project, or decision.
---

# Gather context

Build a well-sourced context brief on whatever the user names: a person, organization, project, topic, or decision. Search the sources that plausibly hold relevant information. Then combine the findings into one organized brief in which every sourced claim links to its evidence.

Use this workflow when the user wants context before they act. That might be before writing, deciding, meeting, pitching, or hiring, or simply to get up to speed. Typical requests include "gather context on X", "what do we have on X", "pull everything about X", "what's the latest with X", and "background on X before my call".

The user may have a separate workflow for structured meeting preparation, such as one that creates a meeting page. If that is what they want, use that workflow instead. This workflow is for raw context assembly. If you are unsure which one they want, ask.

## The most important rule: right-size the effort

Match the depth of the search to what the user actually needs. "Remind me where we are with X" needs a quick look at two or three obvious sources and a short answer. A deep dive before a high-stakes decision needs a broad search with verification. Most requests fall in between. Read the request, decide how much effort is warranted, and do that much. Do not reach for maximum effort by reflex.

Two failure modes are equally bad:

- **Over-gathering:** querying every connected system, starting many parallel helpers, and writing an essay for a quick question.
- **Under-gathering:** checking one source, finding a few results, and stopping when the request clearly needed more. The key fact is often in a chat thread or meeting record the user has forgotten.

For each source, ask: *for this specific request, would a sensible researcher think it is worth checking here?* Relevance and effort level together set the breadth. A topic question does not need recruiting records. A quick status check does not need every source, even if each might hold a small detail. Skipping an irrelevant source is good judgment, not laziness.

## Step 0: Set the purpose and access boundary

State, at least to yourself, the decision or task the brief supports. Search private sources only when the user is authorized to access them and the source is relevant to that purpose. Having access is not, by itself, a reason to search.

When the subject is a person, apply stricter limits:

- Use the minimum sources and information needed for the stated task.
- Do not search private messages or records just because they are available.
- Leave out unrelated or sensitive personal details. Do not guess at private or protected traits.
- Respect consent, confidentiality, need-to-know limits, and the person's reasonable privacy expectations.
- For personal chat apps and direct messages, summarize what other people said in your own words. Do not quote their messages, and do not save them to files.
- Keep the brief in a location whose access matches the sensitivity of the sources and the intended audience.
- For hiring-related subjects, focus on role-relevant capabilities, alignment with the role's requirements, and evidence that actually reflects relevant performance.

If the purpose, authorization, or output destination is unclear, resolve it before searching private sources.

## Step 1: Scope the gather

### Pick an effort level

| Tier | When | How to search | Output |
|---|---|---|---|
| Quick | Status check, "remind me" | One to three obvious sources, one pass each, searched directly | A few lines |
| Standard | The common case | A handful of relevant sources, a couple of queries each; parallel helpers only if they truly save time | A tight brief |
| Deep | High-stakes preparation, such as a major decision, big pitch, or key hire | Broad search, parallel helpers, several queries per source, verification of key claims | The full brief structure |

If unsure, choose the lighter tier and offer to go deeper. Escalating is cheap; over-searching is expensive. State the chosen tier in one short line so the user can redirect, for example: "Quick look across email, chat, and the team wiki. Say the word if you want the full sweep."

### Classify the subject

The subject type tells you which sources matter most.

| Subject | Usually most relevant |
|---|---|
| Person (partner, funder, contact, candidate) | Email, team chat, notes, calendar and meeting records, public professional profile; recruiting records only if the matter is hiring-related and authorized |
| Organization | Public web first; then email, chat, and notes for any existing relationship; CRM or pipeline records if they are a partner or prospect |
| Project or initiative | Notes and wiki, chat, shared documents, code repositories, operational databases, product analytics if there are metrics |
| Topic or question | Several angled web searches, plus internal documents and chat for earlier thinking |
| Decision | All of the above, organized around the options and the evidence for and against each |

### Clarify only when necessary

If the subject is truly ambiguous, such as a bare name that could mean several people or a one-word topic with several meanings, ask **one** short clarifying question before searching. A wrong-target search wastes a lot of effort. If the subject is clear, go ahead. The default is to proceed, not to ask.

### Named sources are a floor, not a ceiling

Sources the user names are mandatory, but they are not necessarily the full list. If another source clearly holds decision-relevant context, check it too.

The most common case is a recent meeting. When results show, or the request implies, a meeting with the subject (especially the same day or week), read the notes or transcript for that meeting. Signals include a calendar invite or a "great to meet you this morning" message in the results. The meeting record is often the richest single source, and a brief without it misses what was actually said.

### Set the time window

Use the window the user gives. If they give none, a sensible default is the last six months, extended back further for older relationships or projects. State the window in the brief.

## Step 2: Search the relevant sources

- **Quick or standard:** search directly in the main conversation so you see results as they arrive.
- **Deep, or many sources:** run read-only searches in parallel, one helper per source or cluster. Each helper returns a short digest with links, not raw dumps. Pass the privacy rules from Step 0 to every helper, including the rule to summarize rather than quote personal chat messages.

Depth within a source also follows the tier. For a deep search, query several ways: by name, organization, project keyword, and related people. Do not conclude "nothing there" until you have used the search capabilities available. For a quick look, one or two well-chosen queries on the obvious sources is correct, not a failure.

### Source-handling principles

These apply whatever tools the user has. The list describes a thorough pass, which suits a deep search. For lighter tiers, apply them to fewer sources and only the top results.

1. **Search direct and indirect.** Look for direct contact with the subject (messages from or to them). In deeper passes, also search for mentions where others discuss the subject.
2. **Prefer precise search modes.** If a tool's default search returns noisy or loosely related results, such as calendar entries flooding a document search, switch to exact or keyword search.
3. **Read the whole item.** Some documents, pages, or records hide content in tabs, sections, attachments, or threads that a simple read skips. For example, a document reader may return only the first tab unless you list the tabs and read each one. Open what matters in full and note where each finding came from.
4. **Know which records are authoritative.** For structured databases, use any map of canonical tables and field meanings before crawling. Go first to the tables the user's organization treats as the source of truth. Treat lower-quality, temporary, or sandbox data as weak until confirmed, and ask before relying on it. Watch for fields that hold default values rather than real ones, such as an automatic midnight timestamp; use a creation date instead when you need to know when something happened.
5. **Check freshness.** Web profiles and news go stale; cross-check current roles against dated sources rather than trusting an old snapshot. Stored notes or assistant memory reflect what was true when written; confirm any named file, setting, or fact still holds.
6. **Read attribution carefully.** Speaker labels in transcripts and authorship in shared records can be imprecise. For example, a transcript's label for the user may include anyone speaking from the same room. Do not attribute a statement to someone without reasonable confidence.
7. **Use conditional sources only when they fit.** Recruiting records for hiring matters, product analytics for usage questions, code and its history for engineering subjects, and the user's personal task or journal system only for work they did themselves and have chosen to include.
8. **Cite properly.** Use clickable links to threads, pages, messages, and documents, not raw internal IDs.
9. **Never invent a link.** Use only URLs you have verified or that the user supplied. Otherwise leave it out and flag it.

### Gaps and unavailable sources

**Do not silently substitute sources.** If a source you judged relevant returns nothing or is unavailable, say so in the brief. Do not cover the gap with an adjacent source.

If a source should be reachable but is not, treat it as a connection or loading problem. Try every safe diagnosis and repair you can first, such as checking the connection configuration, confirming the source's name mapping, or restarting a service you are allowed to manage. Ask the user only for steps that need them, such as re-authenticating in a browser or restarting the application. Report the exact failure, what you tried, and the one remaining action.

A source you deliberately skipped as irrelevant is not a gap and need not be reported, but never imply you checked it.

## Step 3: Synthesize into a context brief

Combine findings into one brief organized by theme, not by tool. Lead with what matters most for the user's next action. Resolve contradictions rather than listing both blindly, for example: "A news profile says they work at Organization A; their dated professional profile says they left in March. The profile is more recent and more likely correct."

**Every sourced claim gets a clickable link** to its primary source. A quote without a link is not finished. The user must be able to click straight through to check.

### Output template

Adapt the headings to the subject, but keep this spine:

```markdown
## [Subject]: context brief
*Searched: [sources]. Window: [dates]. Effort: [quick/standard/deep].*

## TL;DR
Three to five bullets with the most decision-relevant facts.

## What we know
Who or what this is, current state, history. By theme, with inline evidence links.

## Relationship / timeline
(For people and organizations) How the user's organization connects to them; chronology of contact.

## Open questions / gaps
What no source answered, and which source would likely hold it.
Any relevant source that was unavailable or empty.

## Sources
Key links, grouped, so the user can dig in.
```

Match length to depth and keep prose blocks short. A quick check gets a tight brief; a deep dive gets the full structure. This is a document to scan and act on, not an essay.

### Where the brief goes

- **Short brief (fits comfortably on screen):** give it directly in the reply.
- **Long or reference brief:** save it as a document where the user keeps generated documents, at an access level that suits the content. Follow the user's naming convention. If none exists, use the ISO date plus a concise, specific, human-readable headline, in the form "[YYYY-MM-DD]: Options for next year's partner program". Avoid filename-style slugs and type suffixes like "(context brief)". Do not scatter briefs into stray local files unless the user prefers that. Reply with a compact summary of key findings and the link.

Make the brief (or summary plus link) the final part of the reply, with no closing meta-summary after it. Put any follow-up offer, such as "Want me to draft the outreach email?", before the brief. This keeps the deliverable easy to copy.

### Editing an existing formatted document

If you insert the brief into an existing formatted document:

1. Do not insert at the first character of an existing heading, list item, table cell, or other styled paragraph. New text can inherit that style, turning body text into headings.
2. Insert into a known plain body paragraph, or replace a complete section whose boundaries and styles you have read from the document's structure.
3. After every insertion, re-read the affected range at the structural level and check each paragraph's style. Body text and bullets should be normal text; only intended headings should carry heading styles.
4. A plain-text read or heading search does not confirm formatting. Do not report the edit complete until the style check passes. If layout matters beyond paragraph styles, render or export the document and inspect it.

## Readiness checklist

| Check | Pass condition |
|---|---|
| Purpose and access | Task stated; sources authorized and relevant; person-related data minimal |
| Effort | Tier matches the stakes and is stated in one line |
| Coverage | Named sources searched; obviously decision-relevant sources, especially recent meeting records, added |
| Evidence | Every sourced claim has a verified, clickable link; no invented URLs |
| Conflicts | Contradictions resolved or clearly flagged |
| Gaps | Unavailable or empty relevant sources reported; skipped sources not implied as checked |
| Delivery | Output in the right place with appropriate access; brief is the final block |

## Common failure modes

| Failure | Fix |
|---|---|
| Searching every system for a quick question | Choose the lighter tier and offer to go deeper |
| A one-source answer to a high-stakes request | Classify the subject and cover its source cluster |
| Missing what was said in a recent meeting | Read the meeting record when one appears |
| Trusting stale profiles or memory | Cross-check against dated, current sources |
| Reading only part of a document or record | Open hidden sections, tabs, and threads |
| Covering a gap with a nearby source | Report the gap explicitly |
| Quoting or storing personal chat messages | Summarize in your own words and do not save them |
| Including unrelated personal details | Keep only what the stated task needs |
| Reporting a document edit done after a plain-text check | Verify paragraph styles at the structural level |


---
name: learning-tutor
description: Teach a paper, article, or topic through Socratic questions and retrieval practice instead of passive summary. Use when someone says teach me this, help me understand it, or quiz me on it.
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
description: Draft or revise email in the user's own voice, built from real samples, with facts and commitments checked before anything is sent. Use when someone asks to write, reply to, or polish an email.
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
name: professional-posts
description: Draft, revise, and audit professional social posts that lead with concrete value and stay accurate and easy to scan. Use when someone wants to write a post, promote their work, or improve a draft.
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
description: Turn a real person's career or learning story into an evidence-based case study post, with hooks, quote cards, and an approval checklist. Use when someone wants to feature a person's journey publicly.
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
name: cover-images
description: Create cover images for articles and newsletters through five concepts, a close look at the results, and three improved versions. Use when someone needs a header image or an image-generator prompt for a post.
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
description: Chooses one most important outcome for the day, protects time for it, and plans around real commitments. Use when someone says 'plan my day', 'plan tomorrow', or asks what to focus on.
---

# Plan your day

Use this to turn a crowded or unclear day into one named outcome, a protected block of time to deliver it, and a short list of what you will not do. It works for planning today in the morning or tomorrow in the evening.

## Quick version

- Pick **one most important task (MIT)** and phrase it as a finished outcome, such as "draft sent to the reviewer", not "work on the draft".
- Check that the MIT serves one of this week's goals. If it doesn't, ask why it beats them.
- Add at most two supporting items. Everything else goes on a written **NOT today** list.
- Name the work most likely to feel productive while quietly displacing the MIT, and agree one counter for it.
- Protect one focused block for the MIT, broken into chunks with short breaks (about an hour is a good default; adjust to taste).
- If the last few days were rough, plan less: one MIT and nothing else is a valid plan.

## 1. Choose the day and read the situation

Check the local date and time first. Default: before late morning, plan today; in the evening, plan tomorrow; in between, ask. Change these cutoffs to fit your rhythm. If an evening session runs past midnight, keep the date already agreed. State the target day and time zone in one line before going further.

Then gather what exists:

- the day's calendar, including personal commitments that shape the real free time;
- this week's goals and any plan already made for this day;
- tasks that are overdue or due on the target day;
- how the previous day went against its plan;
- the user's recent day ratings or notes on energy, if they keep them.

If the user keeps private notes or a journal they have marked off limits, do not read them. Use only what they share and any fields they have set aside for planning. If a source fails to load, say which one and plan from what the user tells you.

If the weekly plan looks empty, check once more and look for informal week goals written elsewhere before calling the week unplanned. Then ask: "Plan the week first, or proceed without weekly goals?"

## 2. Check the previous day before choosing

Compare what was planned for the previous day with what actually shipped. A calendar block is not proof the work happened, so ask when unsure. A simple table helps:

| Block | Planned items | Shipped? |
|---|---|---|
| [Morning focus block] | [items A, B, C] | [A yes, B yes, C no] |

Then classify the day in one line (more than one can apply):

- **Clean ship:** MIT and supporting items done.
- **Supporting dropped:** list what dropped.
- **Overflow:** one topic ate blocks meant for other work. Say plainly which work didn't happen.
- **MIT slipped:** ask whether the remaining scope is known or still open.

In an evening run, blocks still to come are pending, not dropped. If the user already reviewed the previous day in this session, cite that review in one line and skip the table. If no plan or review exists, say so and work from the calendar and task list.

Every dropped item gets one decision now: carry, push to a later date, retire, or delegate. When an MIT slipped and one topic overflowed, assume the topic is bigger than estimated. Default for the next day: the same topic with a sharper outcome, zero or one supporting item, a time cap ("if not done by mid-afternoon, what happens?"), and dropped items explicitly retired or delegated rather than silently carried. Keep this step to a couple of minutes.

## 3. Read the signals and set the load

Give the user a short brief, no more than about eight bullets: target day, weekly goals, whether the day is already mapped by the weekly plan, meeting load and the biggest open window, overdue and due counts, and anything from recent days worth knowing. Ask one quick question about energy and wait for the answer.

**Lighter plan after rough days.** If recent days were rated low, or the user reports exhaustion or overwhelm, propose a lighter plan up front: one MIT, nothing else, and an earlier stop. Do not just flag it; change the proposal. Default trigger: most of the last few days rated low; adjust to your own scale. A good mood does not cancel a poor night's sleep.

**Check inherited rules against reality.** If the weekly plan contains a rule that clashes with the user's stable habits, ask which stands rather than declaring a conflict.

**Recovery days are allowed.** If the user is ill or clearly needs rest, drop the MIT structure and write a provisional rest plan: full rest as the default, a morning check (sick, borderline, well) and what each triggers, what to cancel or move, the one or two things that truly can't wait, and a NOT today list that includes "don't try to catch up on yesterday". The main risk is half-rest: drifting back into messages mid-morning.

## 4. Choose the MIT

**Confirm before you invent.** If the weekly plan already named this day's main work, or focus blocks are already booked, the MIT is mostly decided. Phrase it as an outcome and ask: "MIT: X, serves weekly goal Y, block already set. Ok, or reshape?" If the user's own message names the MIT, selection is done; only ask what "done" means.

**Re-open when the ground moved.** A weekly pre-map is valid only as of when it was made. Re-derive if the user mentions news that changes scope, a decision that freed later blocks, or a pivot. If the user has already moved blocks themselves, trust their moves over the old plan.

**Otherwise, ask two or three shaping questions before proposing structure.** Good ones: how many hours of focused work do you want, what shape should the day take, and what failure do you expect? Ask them together, then wait. A proposal bundled with questions still anchors the answer. For a single missing fact, such as a meeting time, just ask in plain prose.

Then propose one MIT and test it:

- **Named and binary.** "Work on X" fails. "X done and sent" passes.
- **Serves a weekly goal,** or the weekly plan set this day aside for it. Name the link.
- **Fits the day.** Five meetings and low energy means a smaller MIT or a meeting cut.

If the user names two MITs, push back: merge them, demote one to supporting, or defer it. Four principles cover most variations:

- **Crown what gets displaced.** Booked meetings happen anyway; the unslotted, generative, or aversive item is the one that gets eaten, so it is usually the MIT. "Do the inbox first" sets order, not priority: cap the inbox. The exception is a first task that supplies evidence the MIT needs; keep it inside the MIT's sequence, capped.
- **Bound open-ended work.** Where more is always possible, use a time-bound outcome plus a handoff, such as "three focused hours, then a status note to the stakeholder". If the work depends on input from others, send the request before the block. For a nearly finished artifact, done means closing the named gaps and sharing, not reopening scope.
- **Match the day's shape.** On a meeting-heavy day, the MIT can be one key meeting plus the artifact it produces; label short gaps as prep, not deep work. A hard, slipping task (a difficult conversation, an admin chore with a fixed date) makes a good MIT, with an outcome like "script written and conversation booked".
- **Planning can be the MIT.** After time away, if the user says the main job tomorrow is planning their week, make that session the MIT. Put it in the first open block after meetings and size it to the user's own estimate. Don't add longer-range planning or a bulk push of overdue tasks unless asked; the backlog can be triaged inside the weekly session.

**Valid days without an MIT:** recovery, attending someone else's event, and exhausted back-to-back days where the user says "I just need to get through the meetings". Write a presence-style intention, keep one small task at most, and stop.

## 5. Triage overdue tasks

Only look at tasks overdue or due on the target day. For each, decide: **do today, done, punt, delegate, or delete.** Record each decision as it is made. If there are only one or two, handle them in a line each. If a long list is wearing the user down, offer one yes/no bulk move for low-importance items. Skip this step if a weekly planning session later that day will cover the backlog.

Flag chronic slips. Default: a task pushed several times (you pick the number) gets a direct question: "Is this still real, or should we reshape, delegate, or drop it?" If something is partly done already, ask before treating it as urgent.

## 6. Cut meetings

Walk through the day's meetings: **keep, cut, shorten, or reschedule?** For each cut or move, draft a short, warm message for the user to send. Never send it yourself. Skip this step if the weekly plan already decided "no cuts this week". If the weekly plan said meetings were cut but they're still on the calendar, ask whether to cut now or keep. Count actual timed events; an all-day "focus day" label is a wish, not a fact.

## 7. Protect the time

Propose specific slots: the best window for the MIT, ideally two to three contiguous hours, at the time the user focuses best. Break long blocks into chunks with short breaks; hours that land in chunks still count.

Once the user approves a concrete proposal, re-read the calendar just before writing, then update or create the blocks without asking again. If the user hands you the full slot structure, that is the approval. Reuse an existing focus block and retitle it to the agreed outcome rather than adding a duplicate. Ask before deleting anything, naming each event. Never schedule work over personal commitments.

**Shared surfaces get the neutral version.** If others can see the calendar or a team update, write "Focus: hiring decisions" there and keep names, numbers, and sensitive reasoning in the private plan.

## 8. NOT today and the pre-mortem

Ask: "What are you explicitly not pushing on today? What can you ignore or communicate a slip on?" Capture two to five items. If someone should hear about a slip, draft the heads-up for the user to send.

Then ask: "If today fails, what's the most likely reason?" Add one concrete counter. If the weekly plan already has a pre-mortem, inherit the parts relevant today.

**Probe displacement work.** When the MIT is writing, aversive, or open-ended, also ask what productive-feeling work is most likely to replace it. Name the specific shape, such as "another polish round with no new feedback", and write a counter: "If I'm half an hour into reformatting, stop and ask whether it moves the MIT." On triage days the trap flips: doing the project an email describes. Default counter: a short cap per item (around 15 minutes, adjustable), then reply with a date and create a task.

## 9. Write the plan

Write the plan wherever the user keeps daily plans. Save a one-line intention (the MIT outcome) plus the full plan:

```
## MIT
<outcome>, serves <weekly goal>
Block: <day> <time window>

## Supporting (max 2)
- <item>, <outcome>, <block>

## Calendar decisions
- Kept / cut / shortened / moved: <meetings>

## Tasks
- Do today / done / punted / delegated: <items>

## NOT today
- <items>

## Pre-mortem
- Likely failure: <reason>
- Counter: <concrete action>

## Pending decisions
- <questions the user hasn't answered yet>
```

If the user declines calendar and task updates, still write the plan; it is the record the next review needs. Close with one line confirming what was saved, any pending decision, and anything that failed. Don't summarize the session again.

## 10. Check before you finish

The run is not done until each item is true or explicitly waived:

- [ ] Target day and time zone stated.
- [ ] Previous day classified; every dropped item has a decision.
- [ ] One MIT with a binary outcome and its link to a weekly goal, or a stated no-MIT mode.
- [ ] Calendar blocks updated or created for agreed slots, or the user opted out. Don't claim new blocks if existing ones were reused.
- [ ] NOT today list and pre-mortem counter written.
- [ ] Plan saved.

## 11. Common failure modes

- **Over-asking.** Aim for 10 to 15 minutes. If ten minutes pass with no MIT proposed, propose one and stop asking.
- **Re-asking.** Partial answers mean proceed: do the safe writes and list the rest as pending. When a tired user names the MIT themselves, take it and write.
- **Stale snapshot.** If the user edits the calendar mid-session, re-read it before touching anything.
- **Topic instead of outcome.** Say so directly: "That's a topic, not an outcome."
- **Feels-productive beats boring-but-urgent.** When a hard external date looms, protect a window for the dull, irreversible task.

## Worked example

Sam plans tomorrow in the evening. Most of the last few days felt rough. The weekly goal is "launch page live by Friday". Sam's first instinct is two MITs: finish the launch copy and clear the support queue.

The assistant proposes one: "Launch copy final and sent to the designer by early afternoon." The support queue becomes a capped supporting item. Because of the low days, it suggests no second supporting item and an earlier stop. Sam expects the failure to be "tweaking the hero section for the fifth time". The counter: work only on the list of missing sections, then send. The saved plan lists "refresh pricing table" under NOT today and one pending decision: whether to move a late check-in call.

## Optional extras

- **Fast mode.** If the user hands over an ordered list and asks for speed, anchor deadlines to real calendar times, write the plan from it, and skip triage, meeting cuts, and new blocks. If several MITs are accepted, use headings ("MIT 1", "MIT 2") rather than a numbered list, which some editors renumber badly.
- **Bedtime-bound evenings.** Send one proposal (MIT, supporting, NOT today, clashes) with at most three numbered questions, then write.
- **Autonomous mode.** If the user says "plan tomorrow" on the way to bed, ask nothing: map goals onto blocks they already set, save the plan, and list new invites and open choices as pending decisions.
- **Floating availability.** If the user wants to spend a window helping teammates, write it as a named window with two to four fallback tasks in case no one asks.
- **Forward flags.** For a deadline that can't fit tomorrow but must land within a few days, add a short section so the next plan sees it.
- **Team check-in draft.** If the user posts a daily update, draft it for them to send, keeping done, intended, and pending distinct. Don't overwrite an existing draft or post a duplicate.

```
Y: <yesterday's actual result, marked done / missed / partial>
T: <today's outcome, plus up to two supporting priorities>
W: <weekly goal, only on the first day of the week or when it changes>
```

- **Inbox signal.** With connected tools, add counts of old unanswered email and saved action items to the brief, and flag anything time-sensitive as a supporting candidate.
- **Improve the workflow.** After each run, note one change that would have made it faster or more useful.


---
name: review-your-day
description: Run a short end-of-day reflection on what got done against the plan, what mattered, and what to carry forward. Use when someone wants to review their day, rate it, or offload worries before bed.
---

# Review your day

Use this at the end of the day to see honestly what happened, name one win and one drain, and get tomorrow's worries out of your head before sleep. It is a short conversation, not a planning session.

## Quick version

- Lay out the day neutrally first: what was planned and what actually happened. No judgment yet.
- Open with one specific observation about the day, then let the user talk.
- Ask for a rating only after the context is on the table.
- Always get a win, even on a bad day, plus one thing that drained energy.
- Ask what's rattling for tomorrow and write it down. This offload matters most.
- Keep it to about ten exchanges. Don't replan tomorrow and don't play therapist.

## 1. Choose the day and gather context

Check the local date and time. If it is just past midnight, the user almost always means the day that just ended. Default cutoff: before 4am counts as the previous day; change it to fit you. Say which day you are reviewing in one line.

Collect everything in one batch before asking anything, so the conversation is not interrupted by lookups:

- the day's plan and its MIT (most important task), if one was written;
- the calendar, plus any log of what the user actually did;
- tasks completed;
- messages and documents the user sent or edited;
- meeting notes, if the user keeps them;
- recent day ratings, for the streak check later.

If no plan was written, look for a stand-in: the previous day's plan or offload, a rough list in the user's notes, or a priority list from earlier in the conversation.

**Private notes stay private.** If the user keeps a freeform journal or notes marked private, do not read, quote, or analyze them, and do not mine earlier entries for context. The user can write there freely; the review works from the conversation and the other sources.

**Data boundary.** Read meeting notes and messages that involve other people only when the user is clearly authorized to access them and the purpose is this personal review. Use the minimum sources needed to build the overview, and leave out unrelated or sensitive personal details. Keep the result in the user's own private notes; don't copy other people's content into memory or shared documents.

## 2. Show the overview first

Before any reflective question, show a short overview in plain language, about 10 to 15 lines:

- **Plan vs reality:** three to five neutral sentences comparing the plan with what happened, naming the biggest drift.
- **By source:** meetings with any key decision, focus blocks planned vs used, tasks shipped, and counts of messages sent grouped by person or channel. Drop empty categories.
- **Open loops:** at most three items likely to rattle tonight.

Present meeting notes neutrally: they record what was said, not the user's verdict. No judgment and no questions yet. Then stop and let the user correct anything. If the user often forgets to finish, save this overview as a draft review right away so something exists.

## 3. Optional private freewriting

After the user confirms the overview, offer a few minutes of private freewriting in their own journal or on paper, before any reflective questions. Writing first often makes the conversation shorter and clearer. While they write, wait quietly: no questions, lookups, or progress messages. Never read, quote, or analyze what they wrote; continue once they say they are done. Skip this on terse nights, when the user declines, or when they already wrote today. On late nights, offer it in the same message as the guessed essentials (see Optional extras) and let the user choose.

## 4. Open with one specific observation

Build on the overview; don't recap it. Start with one concrete thread:

- "The plan was to send the draft. The morning block held and it went out before lunch. How did it land?"
- "The writing block shows up as an hour of messages instead. What happened there?"

Then let the user talk. Reflect back before asking the next thing: "So the call overran and took the writing block, the second time this week. Is that a pattern?"

## 5. Collect the essentials

Get these in any order. If the user covers two in one reply, don't ask again.

- **Rating.** Ask once there is context: "So how would you rate today overall?" Use whatever scale the user already tracks. Default: a simple scale from bad to great; change it to fit you.
- **One-line reason** for the rating.
- **A win.** Don't let the user skip this on a bad day.
- **A drain.** What didn't work or cost energy.
- **Offload.** "Anything rattling for tomorrow?" Writing worries down earlier in the evening helps sleep, so do this before the wind-down, not in bed. On good days the offload is often momentum rather than worry; capture either. To make it easy, offer a pre-filled list: "Anything else, or shall I log the obvious ones: X, Y, Z?"

Use plain words. "What drained you today?" beats asking for "the drain". Optionally add one feelings, gratitude, or open-vent question if the day calls for it. Pick one, not all three.

## 6. Diagnose without moralizing

When the MIT didn't ship, find the right explanation before suggesting a fix. Ask, don't assume:

- **Low capacity.** The user was tired, ill, or flat. The miss is a result of the state, not a discipline failure. The fix is rest or a lighter day, not willpower.
- **Aversion-driven displacement.** The day was busy with easy, productive-feeling work that crowded out the dreaded task. Name it: "the batch of replies took the slot because it felt better to ship." The fix is isolation: one task, no messages.
- **Necessary backlog.** Clearing an overdue pile was real work that needed doing. Ask: "Was clearing it a real weight, or did it just feel safer than the MIT?" It can be both.
- **Scope creep inside the MIT.** The user stayed on the right work but added a self-made sub-project that cost the finish line. The fix is "ship rough, improve later", not more focus.
- **Mis-specified goal.** Higher-value work kept taking the slot, often across several days. The goal was wrong for that kind of day. If a well-defended block still failed, stop suggesting "defend it harder".

Other useful checks:

- **Started is not shipped, but can still be the win.** Starting a hard document before an important conversation counts.
- **The MIT may have shipped outside its block.** Ask before scoring a miss.
- **A reframed MIT drops its old sub-items.** Don't keep asking about steps from a plan the user already replaced.
- Ask "What felt productive today but didn't move the MIT?" when hours went into polishing or restructuring with no new input.

If the rating is low and there's time, ask: "What would need to change for tomorrow to feel better?" Log the answer for the planner. Don't plan it now.

## 7. Write and close

Save the review where the user keeps daily notes:

```
Plan vs reality: <one or two sentences>
Win: <...>
Drain: <...>
Offload: <worries and loose ends>
```

Put the rating and reason in their own fields if the user's system has them. Keep the user's vivid phrases; paraphrase the rest.

**Silent streak flag.** If tonight's rating is low and the previous two nights were too, add a short note for the next planning session. Default: a few low nights in a row; pick the number that fits you. Don't comment on it in the conversation.

Confirm in one line: "Review saved." Don't summarize. If the user plans the next day straight after, hand off to that workflow; don't replan here.

## Worked example

Alex planned to finish the product launch email. The overview shows the morning went to a burst of customer replies and the email was started late but not sent.

The assistant opens: "The launch email block went to customer replies. Did those need to happen today?" Alex says about half did; the rest felt easier than the email. That is necessary backlog plus some displacement. Rating: slightly below neutral. Win: the email has a full draft. The assistant notes started isn't shipped, but it counts. Drain: the inbox pull. Offload: "launch date still unconfirmed with the team". Saved in under ten minutes.

## Optional extras

- **Hard rules.** Cap at about ten exchanges. Don't act as a therapist: if something heavy comes up, acknowledge it, log it, and move toward close. If the user says they're containing a feeling for now, log that and don't probe.
- **Terse-night fast path.** If the user just wants to close out, ask for rating, one-line reason, win, drain, and offload in one message with your guesses filled in. Accept the guesses they don't contest, and log any unanswered item as "not named; likely X (unconfirmed)" rather than asking again.
- **Late start.** If the overview arrives after the user's usual wind-down time (a time they choose), put the choice in the same message: freewrite now, or answer the guessed essentials. One reply can then close the review, so don't plan a second round. If past reviews are missing for a stretch when the user was away, such as travel or a retreat, it just means none were written; mention it once in the offload.
- **Hard close.** If the user says they're going to bed, ask nothing more. Use what they already said, note anything inferred, save, and stop. A late "I just want to sleep" overrides an earlier request to review, plan, and wind down.
- **Rating at hard close.** If the user gives only adjectives, map them to the scale and note it was inferred.
- **Personal days.** On a non-work day, skip work sources and let the user's own account lead.
- **Improve the workflow.** After each run, note one change that would have made it faster or more useful.


---
name: plan-your-week
description: Review last week, commit to a few outcomes with a clear definition of done, cut low-value work, and protect time. Use when someone wants to plan the coming week or reset after a messy one.
---

# Plan your week

Use this workflow to review the week that is ending and shape the week ahead in one focused session of about an hour. It works with any goal list, task list, calendar, and notes system, or with nothing but a conversation.

First gather the **constraints** (deadlines, meetings, backlog, energy, capacity). Then run a few interview rounds, each building on the last, to find **what matters**. Only then turn the result into goals, tasks, time blocks, and a short plan. The conversation does the hard work; the final plan should feel simple.

## Quick version

- Ask four review questions: Did you hit last week's goals? What went well? What didn't? What will you do differently?
- Ask the user to list everything they might work on next week, then ask which one outcome would make the week matter, and why now.
- Agree one to three goals, each with two to four outputs someone else could check.
- Add up the hours each goal needs and compare them with free time after meetings, leaving about a fifth of the week unplanned.
- Ask what they will not do this week, and what is most likely to make the week fail.
- Write a one-screen plan: goals, what to protect, the shape of each day, what is not happening, and the main risk.

## What the session produces

1. **One to three weekly goals**, each linked to a longer-term goal, with 2-4 checkable outputs.
2. **A short written plan**, plus the review answers saved with the week being reviewed.
3. **Tasks** of 5 minutes to 3 hours behind each goal, with notes that make starting easy.
4. **Time blocks** for goal work and protected commitments.

If the user declines a step, record that and treat it as done.

## Setup

Ask these once, then reuse the answers until the user changes them.

| Choice | Starting default (adjustable) |
|---|---|
| Planning day | End of the working week |
| Where goals, tasks, and notes live | Wherever they already live, or the conversation |
| Calendars and time zone | Write to one calendar only; use the user's current time zone |
| Longer-term goals | The longest active level, plus the current quarter or month |
| Working hours | Ask; count only hours the user actually works |

Suggested thresholds, all adjustable: a slipping goal has had its deadline moved 3 or more times; a chronically deferred task more than 4 times; a heavy meeting day has more than 5 meetings; the unplanned buffer is about 20% of working hours after meetings; and a waiting message has gone unanswered for more than a few days.

If no longer-term goals exist, say so. Check the next level down. If nothing exists, ask whether to plan without them or set them first. Do not invent stand-in goals.

## Access boundary

Read only sources the user has authorized for planning their own week, and only the minimum: counts, dates, and how long people have waited, not message content. Use other people's details only where they bear on the user's time, and never speculate about or label anyone. Skip any private notes or journal the user doesn't want read. Keep the plan private; drafted messages say only what the recipient needs.

## Core principles

- **Pressure is not importance.** Never recommend a goal just because it is scheduled, overdue, urgent to someone senior, or easy to make concrete.
- **Sources set constraints; the user sets values.** Records show deadlines, slippage, and capacity. Only the user can say what they want to make true, why now, and what they will give up for it.
- **Check before you cite.** Notes about temporary states ("paused for two weeks") expire.
- **Simple output.** Research detail stays out of the final plan unless it changes a decision.

## Hard rules

- **At most three weekly goals; one is ideal.** If the user proposes more, push back: merge, demote to an intention, or defer. With three, label one as the stretch goal.
- **Every goal has a definition of done someone else could verify.** For example: "Sent the second draft of the proposal and budget to the reviewer." A direction is not a goal.
- **Leave a buffer unplanned** (about 20% by default). If goals do not fit, cut a goal. Never shrink estimates to make them fit.
- **Every goal links to a longer-term goal.** If the link is weak, reject the goal. If the user has set longer-term goals aside on purpose, write "Links to: deferred" and move on.
- **No goal proposals before two real interview rounds**, unless the user asks you to skip questions and decide.
- **Keep an alignment ledger** and never bring back an assumption the user corrected.
- **Approve before writing.** Goals, tasks, and time blocks are proposed, approved, then written, one at a time.
- **Be direct and brief.** Say "this will fail because X" when you believe it. No celebratory step summaries. Be firm when needed: "That's four goals; pick three." "You said this three weeks ago; what's different?"

## The alignment ledger

This is your working model of the week. Show a compact version after the brief and before each interview round.

| Line | Example |
|---|---|
| Confirmed (user's choices) | Main focus is the grant application |
| Source facts (constraints from records) | 14 meetings; Thursday is clear |
| Inferred (your labeled guess) | The launch may need a block (guess) |
| Open (only the user can decide) | Whether to skip the Friday review |
| Corrected (rejected assumptions) | The newsletter is not a priority |

## Step 1: Review last week

Keep the first turn short. If you have the data, show active longer-term goals with time left, last week's goals (done, missed, or open), and the four-week hit rate, such as "3 of 7 goals hit". Then ask the four review questions in one block and stop:

1. Did you hit your goals for the week?
2. What went well?
3. What didn't go so well?
4. What will you do differently next week?

The aim is one thing to change, not blame. Save the answers with last week's record. Carry the "do differently" answer into the plan's failure-mode line.

## Step 2: Gather context

Ask: "What must still ship before the new week starts?" That is this week's work, not a goal for next week. Then read whichever of these the user has authorized:

- **Plans and goals:** this and last week's plans, month or quarter plans, active goals, and how often each goal's deadline has moved.
- **Tasks:** overdue and due next week. For large "someday" lists, read titles and deferral counts only.
- **Daily signals:** recent ratings, focus hours, or short daily plans, if the user tracks them.
- **Calendar:** meetings per day, heavy and clear days, and evening or weekend events that limit capacity.
- **Messages (counts only):** old unanswered threads and people waiting for replies.

Data quality: a sync that stopped is a broken pipeline, not behavior, so report its last date. Treat zero as a likely gap and ask before calling it real. Compare like with like; never average across gaps or mix sources. Never invent overdue flags you cannot prove.

If there are no connected tools, ask the user for a two-minute summary of their calendar and open work instead.

## Step 3: The brief

Show only facts that could change a decision, in **at most eight bullets**, tensions and data gaps first. No goal recommendations yet, and no repeating the user's review.

Include each only when it matters:

- **Capacity and energy:** ratings, focus hours, and meeting load, with numbers and days ("three days under target: Mon, Wed, Thu"); heavy and meeting-free days.
- **Slipped goals:** by name, with how often they moved. At the slip threshold, ask now: "Is this still the right goal, or is the format, scope, or owner wrong?"
- **Close-out reality:** whether last week's final items shipped. Ask rather than assume.
- **Backlog and people waiting:** the overdue count, parked tasks that fit likely goals, and who has waited how long.
- **Outside deadlines** the user owns that may not be on their calendar.

End with the compact ledger.

## Step 4: Rolled-over goals

For each unfinished goal, first check whether it was handed off or already shipped. For each still on the user, ask one at a time: **roll over** (note one line on why it slipped and set a new deadline), **demote** to an intention, or **drop** (mark it missed or archived).

## Step 5: Shape the week through interview rounds

First ask whether a written plan for this week already exists, such as a team plan or a recent action list. If so, treat its goals as decided and only check each has a definition of done and fits the week.

### Question format

Ask four to eight numbered questions per round, one decision each. Letter bounded options, recommended first.

```
3. Which area most needs attention this week?
   a. Grant application (recommended: due in 9 days, only you can write it)
   b. Website refresh
   c. Rest and recovery
```

### Round 1: brain dump, then desired change

Ask for an unfiltered dump of everything the user might work on, group it by project, and show it back briefly. Then ask:

- What outcome would make this week genuinely matter, and why now, beyond a deadline?
- What has changed since last week?
- Which area (work, personal, health, relationships) most needs attention?
- What would you regret neglecting even if the visible work shipped?

Do not answer these from records. Afterwards, show the updated ledger.

### Round 2: shortlist

Use the prompts that bite this week: What can only you do? What would most move the longer-term goal? What benefits from starting early? What unfinished work will keep stealing attention? Which fires will you let burn? Also settle real capacity, given meetings, energy, and protected commitments. Anything not shortlisted goes to "Not this week".

### Round 3: only when needed

Run a third round only if a real choice about order, success criteria, ownership, or shape is still open. If the user is tired, offer two or three concrete options.

### Readiness gate

Propose goals only when each of these is confirmed or deliberately left open: the one change that would make the week worthwhile, why it matters now, the longer-term goal it serves, a definition of done, the main competing claim on time, what the user is not advancing, realistic energy, and the most likely failure mode.

Before proposing each goal, ask yourself: did the user call this important, or am I promoting a visible deadline? If the latter, ask another question instead.

### Proposing goals

Propose the smallest set of goals that fits. Check each is **linked** (name the longer-term goal), **verifiable** (2-4 concrete outputs), **scoped** (sketch sub-tasks with rough hours against free time minus the buffer; cut or shrink if it does not fit; under an hour is a task, not a goal), and **realistic** (a heavy meeting week plus low energy means cut one).

### Shaping rules

- **Repeated misses mean less scope.** Default to one goal and ask what has changed before adding more.
- **Name the kind of week.** If meetings dominate, ask whether it is a people week or whether to cut enough to protect one deep goal on the cleanest day.
- **Question the stuck goal.** After two or more slipped weeks, ask whether its format, scope, or owner is wrong; often the fix is a smaller piece.
- **Sequence by outside deadline**, which beats self-imposed pressure.
- **Pending decisions pause detail.** Plan only work that survives every outcome.
- **Soft stop.** If after two or three rounds of pushback the user says "let me just start", accept the plan and record your concern in the failure-mode line.

## Step 6: Pre-mortem and cuts

Do this before blocking time, so the answers shape what you protect.

- **Pre-mortem:** "If this week fails, what is the most likely reason?" Record one to three lines, each with a counter.
- **Cuts:** "What will you delete, delegate, reschedule, or explicitly not push this week?"

## Step 7: Break goals into tasks

A goal is not something you can start; a task is. Break each goal into one to five tasks of 5 minutes to 3 hours. **Do the work before proposing:** put an outline, a draft message, or the decision options in the task notes, never empty notes.

For four or more tasks, propose them in a compact table:

| # | Task | Due | Time | Owner |
|---|---|---|---|---|
| 1 | Draft budget section of grant application | Tue | 90 min | User |

Check for duplicates, spread due dates across the week, and use realistic estimates.

Notes template:

```
Serves weekly goal: [goal]. Links to: [longer-term goal].

Done when: [one-sentence test]

Checklist:
[] [first concrete action]
[] [next action]

References:
- [key document or thread]
- [draft or research already gathered]
```

Avoid one task that restates a multi-day goal, more than five tasks per goal, and creating tasks silently in a batch.

## Step 8: Time blocks

Show the week as short day-by-day paragraphs first, with open questions at the bottom.

If proposed blocks exceed working hours after meetings and the buffer, cut or shrink a goal rather than squeezing blocks. Flag any block shorter than its task estimate. Block tasks of 45 minutes or more, hard deadlines, and protected personal commitments, and never schedule work over personal events. Re-read the calendar right before creating anything. Propose each slot ("Grant budget, Tue, 90 minutes, morning. OK?").

## Step 9: Write the plan

Update existing goals in place rather than duplicating them. Then write the plan. Aim for one screen and omit empty headings.

```
## Theme
[2-5 words]

## Weekly goals
[] [Goal 1], links to [longer-term goal]
    Done when: [2-4 checkable outputs]

## Protect
- [commitments with concrete slots]

## Week shape
- [day]: [the one essential focus or constraint]

## Not this week
- [explicitly deprioritized work]

## Failure mode
- [most likely failure] → [specific counter]
```

## Step 10: Close and improve

Give the counts in one sentence (goals, tasks, blocks) and make the plan the last block, with no recap. Then note one precise improvement for next time: a wasted step, a wrong assumption, or something the user corrected.

## Adapting to timing

- **First day of the week:** settle what must ship today, then shape the rest.
- **Mid-week:** plan only the remaining days and state the real runway.
- **Time off:** skip work goals; plan rest and logistics only.
- **Tired user:** offer two or three concrete options, or decide with stated reasons if asked. Treat low capacity as a hypothesis; if confirmed, plan a lighter week with one goal.

## Optional extras

Add these modules when the user wants them. Each is independent.

### Health and energy check

Opt-in only, and only to judge capacity. Compare the last week or two of whatever the user tracks against their own targets, from the same source, numbers first. If a commitment is faltering, ask until they name a concrete fix with a day, time, and cue: "Walk at lunch Mon, Wed, Fri when the noon reminder goes off," not "I'll move more." If the same fix failed last week, ask what is different. After travel or illness, frame the week as recovery. Honor habits the user has deliberately paused.

### Meeting cut pass

If the user wants cuts, list meetings that serve no goal or obligation; they decide keep, cut, shorten, or move. Draft a short, warm message for each change for the user to send.

```
Hi [name], I'm protecting time for [goal] this week, so I'd like to [skip / move / shorten] our [meeting] on [day]. [Alternative, such as a written update by Thursday]. Does that work for you?
```

### Task triage

Ask whether the user wants to triage overdue tasks themselves. If not, first offer chronically deferred tasks as one batch to move to "someday". Then go one by one, most important first: do this week, done, defer, delegate, or delete. Always offer "done", since people forget to close things. Write each decision right away.

### Messages catch-up and scorecard

If people are waiting on replies, propose a one to two hour catch-up block.

If the user's monthly or quarterly plan has a scorecard or non-negotiables, score the lookback period using its own items and wording. If a cut-scope rule fires, raise it during shaping. Do not rebuild an expired scorecard.

### Recurring-friction review

If the user asks, look across recent sessions for corrections that repeat ("that's wrong again", "I meant"). Group repeats, skip one-offs, and propose one specific fix for each group.


---
name: plan-your-month
description: Close one month honestly, then plan the next with a capacity check, a NOT list, and concrete commitments. Use when a month is ending, or when someone wants a monthly review or plan.
---

# Review and plan a month

Use this workflow at a month boundary to review the month ending and build a plan for the month ahead. A full session usually takes about an hour (adjustable): roughly half for evidence and review, half for planning.

Review and planning belong in the same session. The structural cause of last month's misses should directly shape next month's plan.

## Quick version

- List what you said you would do last month, and mark each item done, partly done, or missed.
- For each long-range goal, say whether it advanced, stalled, or went backward, in one line.
- Name one win, one drain, and one thing that must change next month.
- Pick at most three outcomes for next month, each with a date and a test of done.
- Do the math: available working days times realistic focused hours, against what the outcomes need. Cut until it fits.
- Write what you will not do, and the two most likely ways the month could fail, each with a counter.

## What the session produces

- An evidence-based account of the month ending.
- A direct verdict on progress toward active long-range goals.
- A written **Review** for the month ending.
- A written **Plan** for the month ahead: a memorable theme, no more than three outcomes, explicit cuts, and a pre-mortem.

A plan is not a description of the month plus optimistic targets. **If the plan could be written without the user answering a hard question, it is a description, not a plan.**

## When to run it

Run it when the user asks for a monthly review, asks to plan a named month, or asks to close one month and start another.

Default timing (adjustable):

- In the first few days of a month, review the prior month and plan the current one.
- Otherwise, review the month to date and plan the next month. Label a partial-month review and state the days remaining.
- If the user asks only to plan ahead, review first anyway, because evidence should shape the plan. The user may choose to skip it.

State the ranges before proceeding: "Reviewing [month] ([first date] to [last date]). Planning [month]."

## Access boundary

Use only sources the user has authorized for this review, and only the minimum relevant information: dates, statuses, counts, and trends rather than message bodies or private notes. If the user keeps private notes or a journal they don't want read, respect that and use only what they share. Never assess other people from private material. Save the review and plan only where the intended readers should see them, and never imply that an unavailable or excluded source was checked.

## Operating rules

1. **Evidence first, discussion second.** Show the evidence picture before asking reflective questions.
2. **Gather in one pass.** Batch independent reads rather than interrupting the conversation with small lookups.
3. **Use current targets.** Judge progress against the user's live goals, not old schedules or stale records.
4. **Check data quality before a harsh verdict.** Missing syncs and incomplete logs distort conclusions. Ask the user to confirm surprising findings.
5. **The user chooses.** You calculate, summarize, and ask hard questions. The user picks priorities, cuts, and commitments.
6. **One decision at a time.** Do not move on until the current question has a real answer.
7. **Stay at month level.** Set outcomes, milestones, capacity, and structure. Leave daily task blocks to weekly planning.
8. **No saved plan without explicit approval.** A plan assembled from notes is a draft, not a decision.
9. **Keep records useful, not exhaustive.** Save decisions, evidence, and commitments, not a transcript.
10. **Do not lecture.** Show numbers, a direct conclusion, and the agreed commitment.

## Step 1: Gather evidence

Use the user's own system: a task manager, project tracker, calendar, spreadsheet, notes, or habit tracker. If nothing is connected, ask for a short factual inventory. With only a chat assistant, these questions are enough:

1. What did you plan or promise for last month?
2. What actually got done?
3. What is on the calendar next month: travel, time off, deadlines, heavy weeks?
4. Which long-range goals are active?

| Evidence area | What to gather |
|---|---|
| Last month's plan | Theme, promised outcomes, commitments |
| Weekly plans and reviews | Repeated blockers, milestones, carried work |
| Goals | Active monthly, quarterly, and yearly goals with status and deadlines |
| Work delivered | Completed tasks and deliverables, grouped into a few areas |
| Calendar | Time off, travel, fixed deadlines, recurring commitments, heavy weeks |
| Daily signals (optional) | Ratings, focus hours, or habit counts the user chooses to track |

For large sources, compute statistics and pull a few themes instead of reading raw entries.

Before planning in detail, re-read any weekly plan that overlaps the start of the new month. Reconcile with it; never duplicate or overwrite it.

## Step 2: Show the evidence picture

Present a compact factual picture before asking the user to explain it. Be direct and use numbers where useful.

### Goals and delivery

Summarize last month's commitments as completed, missed, deferred, or rolled forward. For each active long-range goal, say whether it **advanced**, **stalled**, or **regressed**, with one short reason. Name goals that got no attention; these are often most at risk.

Summarize completed work in a few areas, not a wall of bullets. The question is whether effort created the intended progress.

### Signals

Include only measures the user tracks, such as average daily rating, focus hours, or low-energy streaks. Flag patterns like several low days in a row, or ratings that look fine while the user describes strain. Averages are not the whole truth; raise a mismatch briefly and ask about it.

### Worked example (fictional)

> **Review: a month of 21 working days.** Commitments: 4 of 6 done (67%). Goal "launch the online course" advanced: 5 of 8 modules recorded, up from 2. Goal "grow the newsletter" stalled: 1 issue sent against a plan of 4, subscribers flat at about 1,150. Goal "hire a part-time editor" got no attention. Focus: 52 hours logged against a target of 70 (74%), with the shortfall concentrated in the two weeks with client workshops. **Verdict:** the course is on pace, but the newsletter is losing to client work every time they collide. Structural fix: write the newsletter on Monday mornings before client work starts, and ship whatever exists by noon.

## Step 3: Reflect on the month

Start with one specific observation from the evidence. Ask one question at a time and follow no more than two or three threads unless the user wants depth.

Cover these before closing the review:

1. What genuinely shipped and feels like a win?
2. What cost more time or energy than it returned?
3. Was the main miss structural, circumstantial, or a real change of priority?
4. What one behavior, boundary, or pattern must change next month?

Useful prompts:

- "This outcome slipped in several weeks. What made it structurally hard?"
- "Your ratings were steady, but you keep describing strain. What was happening?"
- "This goal moved while the others did not. What made that possible?"

The minimum useful review, if time is short: goal movement, one structural fix, and one concrete commitment for next month.

## Step 4: Plan the new month

A real plan has a defined outcome, an honest baseline, a path, proof of capacity, trade-offs, outside pressure, a pre-mortem, and explicit approval. Each move below should make the user answer something hard.

### Move 1: Define outcomes

For each candidate priority, ask: "What specifically is true on the last day of the month?" Make the answer measurable or plainly checkable. Limit the plan to three outcomes; one or two is usually better. Each should connect to a long-range goal or a chosen responsibility.

### Move 2: Establish the current state

Size the gap with evidence, not mood. Look at the actual draft, pipeline, backlog, or baseline number. If the gap cannot be described, gather the missing evidence first.

### Move 3: Work backward to a path

For each outcome, list three to six steps working back from the due date. Each step needs a date or window, an owner, and evidence of completion. Ask: "For this to be true at the end, what must be true halfway through?"

### Move 4: Do the capacity math

Estimate: available working days × recently observed focused hours per day. Subtract time off, travel, and heavy meeting weeks. Compare with the effort the paths need. If demand exceeds supply, cut, defer, shrink scope, or get real help now.

### Move 5: Make the not-doing list

Ask: "What will explicitly not happen this month so these outcomes can?" The user names the cuts. A plan without real cuts is a wish.

### Move 6: Add outside pressure and protection

Fragile outcomes need outside pressure: someone expecting a deliverable on a date, a booked review, or a public commitment. Protect work that needs long, uninterrupted time by giving it the best blocks and batching flexible work around meetings.

### Move 7: Run a pre-mortem

Ask: "It is the last day of the month and this plan failed. What happened?" The user answers first. Record the top two or three failure modes, each with a specific counter.

### Move 8: Get sign-off

Read the plan back in ten lines or fewer. The user should be able to state the theme and outcomes from memory, then approve it. Ask: "Is this the plan?" If the answer is vague, revise. Do not save yet.

## Plan template

```markdown
## THEME: [MEMORABLE, ACTION-ORIENTED LINE]

**Planning range:** [first date] to [last date].

## Shape of the month
[Time off, travel, fixed events, heavy weeks, real working weeks.]

## Outcomes
1. **[Outcome]**: done by [date] when [test of done].
   - Current state: [honest gap].
   - Path: [dated milestones, owners, evidence].
   - Outside pressure: [who expects what, when].

## Capacity check
[Available hours] versus [needed hours]; [scope decision].

## Not doing
- [Explicit cut or deferral.]

## Structure
[The behavior or boundary change that counters last month's drain.]

## Pre-mortem
- Failure mode: [likely cause]. Counter: [specific response.]
```

## Step 5: Save the review and plan

After explicit approval, save two records in the user's system: a **Review** for the month ending and a **Plan** for the new month. Before overwriting an existing plan, show it and resolve the difference.

Review template:

```markdown
## Goals and delivery
- Commitments: [done]/[total] ([percent]%).
- Long-range goals: [goal and status].
- Work delivered: [short grouped summary].

## Signals
- [Chosen measures, or "not tracked"]. Flags: [none or named patterns].

## Win
[One meaningful result.]

## Drain
[One thing that cost more than it returned.]

## Structural fix for next month
[One named behavior, boundary, or system change.]
```

Confirm the save in one line and stop.

## Step 6: Improve the workflow

At the end of each run, make one precise improvement to this workflow or its templates: a noisy read, a wrong assumption, a misleading measure, or a question the user corrected. Write it as a general rule, not a private fact.

## Audit checks

Before finishing, verify:

- Review and planning ranges are explicit.
- Evidence came before reflection.
- Strong verdicts account for data gaps.
- The plan has a theme and no more than three outcomes.
- Each outcome has a test of done, date, path, owner, and outside pressure.
- Capacity fits, or a scope decision was made.
- The not-doing list has real cuts.
- The structural fix responds to a reviewed drain.
- The user answered at least one hard question that shaped the plan.
- The pre-mortem has counters.
- The user explicitly approved the plan before saving.

## Common failures

- Starting with questions instead of evidence.
- Judging against stale targets.
- Confusing a list of events with a plan.
- Overloading capacity and refusing to cut.
- Letting the assistant choose priorities.
- Saving an unapproved draft.
- Conflicting with an existing weekly plan.
- Applying generic productivity rituals instead of fixing the actual drain.
- Treating a brainstorm or imported task list as a confirmed commitment.

## Optional: personal practice

Add this section only if the user tracks a habit or practice they want held to account, such as writing, a language, music, exercise, or meditation. Put it after goals and delivery, not first.

Compare actual activity with the user's current target using whatever they log: sessions, minutes, words, or pages; average per week; active days; longest gap; and the change from last month.

Suggested verdict scale (adjustable):

- **On track:** key measures at or near target and consistency intact.
- **Behind:** a key measure clearly short of target, or a noticeable break in consistency.
- **Off track:** a key measure far below target, or a long gap.
- **Paused:** the user chose to stop for now; do not re-argue it.

If tracking may be incomplete, ask "The record shows this. Does that match reality?" before judging. State one concrete commitment for next month, such as "20 minutes of practice on four weekday mornings", and add it to the plan.


---
name: get-unstuck
description: Diagnose why someone is stuck, then run one short, matched intervention to get the first work block started. Use when someone feels tired, dreads a task, cannot get started, or keeps getting distracted.
---

# Get unstuck

A short rescue coach for 10 to 15 minutes. It is not a full productivity system. The user is stuck or avoiding something. You diagnose their state, run one matched intervention, and get them into one short work block. If the user agrees, you log the session so later sessions improve.

Use it before the user starts, when they cannot get going. Also use it during a task, when they have lost momentum. Typical triggers: "I can't get started", "I'm dreading this", "I'm exhausted", "help me get going", "I'm stuck on X", "I don't want to do this".

Input: an optional sentence describing what the user is avoiding. If it is missing, ask for it during diagnosis.

## Purpose

People usually avoid tasks for four reasons, and most of the time several apply at once:

- **Tired:** physically or mentally depleted.
- **Dread:** the content feels unpleasant, high-stakes, or tied to self-worth.
- **Unclear:** the next concrete step is unknown.
- **Distracted:** the phone, feeds, or other easy rewards keep pulling them away.

The coach's job:

1. **Diagnose before prescribing.** No intervention until you have checked the user's state.
2. **Match the intervention to the main problem, in order: physical, then emotional, then cognitive.** If you reverse this order, the user often slides back into avoidance.
3. **Pick a coaching style on purpose, say which one, and invite a switch.** Over time this shows what works for this user.
4. **Aim for one time-boxed block, not a finished task.** Success means the user starts and does something, even badly.
5. **Learn from each session** if the user has agreed to logging.

Success: the user starts within 10 to 15 minutes and completes at least one block. Failure: the rescue itself becomes a new way to procrastinate.

## Design principles (shape the method; do not lecture the user)

- **Procrastination is mostly about managing emotions, not laziness.** Avoiding the task brings relief, and that relief reinforces the avoidance. Naming the feeling weakens it. Appeals to willpower usually fail.
- **Action comes before motivation.** Short actions of 5 to 15 minutes can lift mood quickly.
- **Self-compassion works better than self-criticism.** Criticism adds shame, and shame leads to more avoidance.
- **If-then plans work because they are specific.** "If [cue], then [action] at [place]" beats a vague intention.
- **When motivation is low, make the step easier.** Shrink the first action to about 30 seconds, and acknowledge it right after.
- **Thought distancing helps with heavy tasks.** "I'm having the thought that X" creates some space from the thought.
- **Match the task to the energy level.** A depleted brain should not draft careful writing. It can gather material, sort files, or tidy.
- **Physical levers, from strongest:** bright light, about 5 minutes of movement, and water are well supported. Cold water on the face helps a little. Avoid caffeine late in the day, because it harms sleep.
- **Feed-scrolling leaves a slump** that makes a dreaded task feel worse. Put physical distance between the user and the device before restarting. Do not try to resist the device while it is still in hand.
- **Bureaucratic and compliance tasks are their own category.** Official forms, legal filings, and applications carry learning costs, rule-following costs, and emotional costs. Do not apply ordinary project-work shortcuts to them.
- **Strong avoidance often signals that the work matters.** This reframe helps only when the user is calm and reflective. Do not use it when they are overwhelmed.
- **Harsh, drill-sergeant motivation has weak support for depleted people** and tends to add shame. Use it only when the user explicitly asks for it.

## Hard rules

- **Diagnose every time.** No shortcuts.
- **Physical comes first.** If the user is very tired, do a physical reset before any thinking work.
- **No harsh style on a depleted user.** Use it only if all of these are true: the user is physically capable, the task matches their values, they are simply indulging in avoidance, and they asked for this style today.
- **Say the style each session** and invite a switch if it is not landing.
- **Cap the rescue at 15 minutes.** If you are still diagnosing at 15 minutes, the user either starts badly or stops. The rescue is not the work.
- **Honor break requests, but bound them.** A state-change break lasts 5 minutes. It can extend to 10 minutes, no further. The structured outing in Step 2A has its own cap.
- **Watch for capacity problems.** If high tiredness and high dread keep recurring across many sessions, switch to the capacity branch. Do not run the usual rescue.
- **Offer to shrink the task directly.** If you have authorized access to relevant source material, offer to gather it for the user (see Step 2C).
- **Do not narrate.** No "great, now let's...", no emoji, no recap of what you just did.

## Step 0: Diagnose (2 minutes or less)

Send one message with three short questions and no preamble:

1. **The task, in one line.** Skip this if the user already gave it.
2. **State, 0-10 each:** tired / dreading the content / unclear next step / pull toward distraction. High numbers mean more of the problem.
3. **Time available** before the next commitment.

If the user keeps a session log and has agreed to its use, read the last three entries quietly. Note which styles landed, which missed, and any recurring problem. Do not quote the log back. Let it inform Step 1.

### Find the dominant problem

- The highest single score is the dominant problem.
- If two or more scores are 5 or above, treat it as a **compound state**. This is common.
- If tiredness is 7 or above and dread is 7 or above across 5 or more recent sessions, raise a **capacity flag** and go to the capacity branch.

### Capacity branch (a capacity problem, not a motivation problem)

Do not run the rescue. Say directly:

> "Tiredness and dread have been high for several sessions in a row. This looks like a capacity problem, not a motivation problem. What's the case for not doing this task today? Who else could take it? What would a 48-hour delay cost? What would actually help you recover?"

Stay with that conversation. Do not let it drift back to "fine, just one block." If the pattern looks like ongoing exhaustion or low mood, gently suggest talking to someone they trust or to a health professional.

If the user still insists on doing the task, go ahead, and say plainly: "We're working against the warning signs. Noted."

## Step 1: Pick and name a style (30 seconds)

Choose one style based on the diagnosis and any log history. Say it out loud:

> "I'll be [direct / analytical / empathetic / practical-warm] for this one. Tell me to switch if it's not landing."

Default mapping. Override it if the log shows a style has reliably worked or failed for this user.

| Dominant state | Default style | Why |
|---|---|---|
| High dread, low tiredness | Empathetic or analytical | Naming the emotion weakens it; analysis suits a calm user |
| High unclear, low dread | Analytical | Paralysis here is a breakdown problem |
| High distraction, low dread | Direct | Break the reward loop, briefly |
| Tiredness dominant | Practical-warm | A depleted brain needs warmth and brevity |
| Compound (two or more high) | Practical-warm | Warm but without waffle |
| User explicitly asked for harsh | Direct, then demanding | Rare, opt-in only |

**Signals to switch mid-session:**

- "Just tell me what to do" or impatience: switch to direct.
- "This is making me feel worse" or silence: switch to empathetic.
- The user argues with the framing: switch to analytical and let them reason their way in.

## Step 2: Intervene (physical, then emotional, then cognitive)

Do not skip ahead. Physical always comes first when tiredness is high.

### A. Physical reset (if tired is 6 or more, or dread is 7 or more)

This step is not optional when triggered. Moving the body often shifts emotional state too. Send one crisp message:

- Drink one glass of water now.
- Move: a walk outside if possible, otherwise stairs or brisk steps. No phone.
- Get light from a window or outdoors. No phone, not even for music.
- Optional: cold water on the face.
- No caffeine late in the day. A small snack or a decaf drink is fine; the ritual and the blood sugar are what matter.

**Caps:**

- **Unstructured break:** 10 minutes (water, walk, back).
- **Structured outing:** up to 20 minutes. It is a round trip to a named place, with a small reward and a clear return cue. The user states the plan before leaving, and you hold them to it.

If the user proposes a break that fits these bounds, agree and set the limit.

### B. Emotional (if dread is 5 or more, or shame shows up)

Pick one of these, not all of them:

- **Self-compassion break** (about 45 seconds, said aloud): "This is a hard moment. / Struggle is part of being human. / May I be kind to myself right now."
- **Thought distancing:** put "I'm having the thought that..." in front of the worry.
- **Values anchor** (about 20 seconds): "This task matters because [the user's own goal or value]. Doing it is an act of that value, even when it feels like a slog."
- **Avoidance-as-signal reframe**, only for a calm, reflective user: "How strongly you're avoiding this shows how much it matters. You're not weak; you're at the edge of something important."

**Shame signals:** "I'm such an idiot", "I can't even do this one thing", a long silence after a directive, or self-deprecating jokes. When you see one, switch to self-compassion right away. Never push harder on a shame-flooded user.

### C. Cognitive (once physical and emotional are handled)

- **Turn abstract goals into mechanical steps.** "Compile evidence" becomes "collect sources". "Respond to the official request" becomes "open the request and read section 1". Use mechanical verbs only.
- **Shrink the first step** to its 30-second version: the very first click, not the whole task.
- **Make an if-then plan.** Require the format "If [cue], then [action] at [place]" and have the user say it once.
- **Box the time, not the outcome.** Use 25 minutes by default, or 15 minutes if the user is very tired. When the timer ends, the user stops. No "almost done" extensions.
- **Offer to gather material in parallel.** Some tasks draw on source material: messages, meeting notes, documents, records. If the user has authorized access, offer to search it and paste raw findings into a scratch document. This removes the blank-page problem and often cuts dread sharply.
  - Use only the sources and details the task needs.
  - Leave out unrelated or sensitive personal information about other people.
  - Keep the output in the user's private workspace.

## Step 3: Start the block

- State the timer length out loud.
- Confirm the environment:
  - phone in another room;
  - only the tab or tool the task needs;
  - everything else closed;
  - a site blocker on, if the user uses one.
- Then stay silent. Do not chat during the block. The user working matters more than the user talking to you.

## Step 4: End-of-block check (30 seconds)

When the user returns:

- Ask for one sentence on what came out of the block.
- Ask them to re-rate tiredness and dread, 0-10.
- Ask only one question: "Another block, or stop?" Never ask how many more.

**If stopping:** acknowledge the effort out loud. The acknowledgement helps build the habit; it is not a platitude. For example: "You showed up when you didn't want to. That counts." Then stop.

**If continuing:** repeat Step 3 with the same setup. Re-diagnose only if the user's state has clearly changed.

## Step 5: Log the session (with consent)

On first use, ask whether the user wants sessions logged and where to keep the log. If they say no, skip this step. If they say yes, append an entry quietly after each session, using a stable format:

```
## DD MMM YYYY HH:MM - <task in 3-5 words>

- State start: tired <N>, dread <N>, unclear <N>, distraction <N>
- Dominant problem: <tired / dread / unclear / distraction / compound / capacity>
- Style: <direct / analytical / empathetic / practical-warm / demanding>
- Interventions: <physical-reset / self-compassion / distancing / values / reframe / shrink / if-then / parallel-gather>
- Blocks: <N blocks of M min>
- Outcome: <started yes/no; state end tired/dread>
- What worked: <one line>
- What didn't: <one line>
- Style verdict: <landed / missed - try X next time>
- Notable: <optional one line>
```

Keep the entries focused on the task and the user's state. Leave out private details about other people.

## Step 6: Refine the method (only when a pattern appears)

Review recent log entries for patterns. Depending on the user's preference, either suggest a change or update the user's personal notes for this method.

Refine when:

- A style has failed in 3 or more recent sessions: demote it in the mapping.
- An intervention keeps landing: make it the default for that state.
- A new state or combination appears that the method does not cover: add a branch or row.
- A rule was broken and it worked (for example, a demanding style helped a tired user who asked for it): record it as a narrow exception. Do not generalize it.
- The user pushed back on a prompt: rewrite that prompt.

If the session went smoothly, change nothing. Do not invent improvements.

## Related workflows

- **Planning:** if the user gets stuck while planning, run this first, then resume planning.
- **Evening wind-down:** do not run this inside a wind-down routine. Wind-down is about leaving work, not starting it.
- **Problem-solving:** if the user is stuck because the problem itself is unclear, not because of motivation, use a problem-solving workflow instead.

## Style notes

- Crisp beats warm waffle. Empathetic does not mean long.
- Name an emotion once; do not circle back to it.
- Mention research only if it helps the user act.
- Use one consistent, unambiguous date format.
- If a requested break is reasonable, say yes and set its limit.
- No emoji and no end-of-turn summaries. Confirm the next action and stop talking.


---
name: wind-down-for-sleep
description: Guide a short evening routine that closes open loops, lowers stimulation, and prepares the morning, with a fallback for sleepless nights. Use when someone says they want to wind down or cannot sleep.
---

# Wind down for sleep

This is an interactive evening workflow. It moves the user from the awake part of the day to sleep. It does three things only: it lowers stimulation, adds reliability, and prepares the body. It does not handle reflection or planning. Those belong to an earlier day-review practice and an earlier next-day planning practice.

Recommended evening order: **day review, then next-day planning, then wind-down.** This workflow comes last.

Target length for the active ritual: about 20 to 30 minutes. Longer rituals tend to get skipped.

## Quick version

- Say "wind down" when you are ready to start.
- Put your phone or other distracting device out of reach first, ideally in another room or a timed box.
- Change into sleep clothes, do two or three small tasks for the morning, then a few minutes of a calming practice you already know.
- If a worry or task comes up, write one line on paper for tomorrow and leave it.
- Do not plan tomorrow or reflect on today during this ritual.
- If you are still awake after what feels like about 20 minutes in bed, get up, do something dull in dim light, and return when sleepy.

## Standalone mode

You do not need daily records, a calendar, or any other workflow to use this. Tell the assistant tonight's bedtime and when you want your phone back, then run Steps 1 to 4 from that alone, and skip Step 0. Use paper as the capture spot.

Chatting with an assistant on a bright screen works against winding down. Use voice if you can, or send one short message per step, with the screen dimmed and warm.

## Settings the user chooses

Agree on these once. Reuse them every night until the user changes them. Offer the starting points only as suggestions, and do not assume values the user has not chosen.

| Setting | What to decide | Suggested starting point |
|---|---|---|
| Target sleep time | When the user wants to be asleep | Based on their natural sleep window and wake time |
| Ritual start | When wind-down usually begins | 60 to 90 minutes before target sleep time |
| Review cutoff | When a missed review is skipped | When a review would push sleep back |
| Distraction barrier and access time | How the device goes out of reach, and when it comes back | A timed box or another room; back after the first part of the morning |
| Early-commitment rule | How much earlier access moves for an early commitment | First commitment minus getting-ready and travel time |
| Gate items | The few changes that signal night | A clothing change plus the distraction barrier |
| Allowed device | The one low-stimulation device, if any, after the gate | None |
| Physical prep and settling practice | Small morning-setup tasks, then a short familiar practice | Water, teeth, breakfast; a few minutes of slow breathing |
| Capture spot | Where stray tasks go for tomorrow | A notes field on tomorrow's record, or paper |

If the user names an earlier bedtime for tonight, work backwards from it. Protect time for physical prep and the settling practice. Do not let planning expand into the remaining window.

## Purpose (re-read every run)

It targets late stimulation (scrolling, lying awake), worry about tomorrow (mostly handled by the earlier review and specific planning), an inconsistent routine, and distraction controls that are easy to bypass. Physical barriers usually beat software limits on the same device.

Success signal: the user wakes rested, starts the morning without scrolling, and the device stays out of reach until the chosen access time. Every step must reduce stimulation, add reliability, or prepare the body; remove any step that does none of these.

Design anchors, never explained at bedtime: a specific to-do list written earlier has been linked to falling asleep faster; scheduled worry time earlier in the evening reduces bedtime anxiety; dim, warm light helps sleep onset; and consistency matters more than contents.

## Triggers

- **Full ritual:** "wind down", "ready for bed", "going to bed", "time for bed", "help me get to sleep", or similar.
- **Can't-sleep fallback only:** "can't sleep", "still up", "still awake", or similar, after the ritual already ran tonight. Skip every other step and go straight to Step 6.

## Hard rules

- **Gate first.** Do not continue past Step 1 until the user confirms it.
- **Keep the gate minimal.** Include only the gate items the user chose. If the user removes an item, do not add it back later.
- **No distracting-device step after Step 1.** Everything afterward must work offline or with the one allowed device.
- **Never ask about tomorrow.** No outcomes, intentions, wins, or backup one-line plan. If planning was skipped, note it silently and continue. Planning questions raise alertness at the moment the goal is to lower it.
- **Do not reopen reflection or planning.** Do not open a second writing session. Any journal writing belongs to the review, before its questions.
- **Deflect tomorrow-concerns.** Say: "Put a short note in your capture spot. The review will handle it tomorrow. Not tonight."
- **No summary at the end.** Send the close and stop.
- **Stay silent after the close.** If the user says good night, reply with nothing or only "Good night." Never send a follow-up, a placeholder, or a simulated user turn. An unexpected message after bedtime can wake someone up.

## Privacy and data handling

If the workflow connects to a journal, day records, or calendars, use only sources the user has authorized, and only to confirm status and set the access time. Check a completion signal, such as a rating or a done marker. Never read, quote, or write into private journal text. When capturing a note, read only the field you append to. Treat calendars as read-only, and keep what you see inside the session.

## Step 0: Readiness check

Gather only what is needed to confirm the earlier practices ran and to set the access time. Do not open inboxes, news, or feeds.

If the review and planning ran earlier in the same session, skip all lookups. That state and tomorrow's calendar are already known. Check the current time and continue.

If this workflow runs on its own, gather the following in one batch:

1. Current time, today's date, and tomorrow's date.
2. Whether today's review is complete.
3. Whether tomorrow's plan exists.
4. Tomorrow's first fixed commitment before midday, from every calendar the user approved. Include personal as well as work calendars, since social plans and early activities move the access time too.

Lookup principles:

- **Test presence, not truthiness.** A zero rating is a valid, completed rating.
- **Match dates loosely** and expect more than one record per day. Check each matching record instead of assuming a single one.
- **Degrade quietly.** If a source fails, say so once, compute from what you have plus anything the user mentioned, and leave repair for daytime.

| Review complete? | Time | Action |
|---|---|---|
| Yes | Any | Say "Day reviewed. Starting wind-down." Go to Step 1. |
| No | Before review cutoff | Say "The day review didn't run. Do it now (about 10 minutes)?" If yes, run it and return. If no, mark review skipped and go to Step 1. |
| No | At or after cutoff | Say "Too late to review tonight. We'll pick it up tomorrow." Mark review skipped. Go to Step 1. |

If tomorrow's plan is missing, do not mention it, offer planning, or ask a fallback question.

## Checklist format (Steps 1 and 2)

Use plain bullet lists, not checkboxes. Many interfaces cannot tick boxes, and "tick each one" wording confuses people. Send the whole list in one message and end with "Reply 'done' when all set." Expect one reply. Do not send items one at a time, because that adds turns at bedtime.

## Step 1: Environment and distraction gate

Set the access time:

- Default: the user's chosen access time.
- If tomorrow's first commitment is early enough that the default leaves too little time to get ready and travel, apply the user's early-commitment rule.
- State the time. If it is earlier than usual, give the reason in a few words. If the barrier has a timer, show the duration from now.

```
Before we start:
- [Clothing change, e.g. day clothes off, sleep clothes on]
- [Distraction barrier], timer [duration] (access at [time][, reason if earlier, e.g. travel for an early meeting])

Reply "done" when all set.
```

If the user delays an item ("I'll do it in a sec"), say once: "Do it now. These are the biggest levers. I'll wait." Then wait.

## Step 2: Physical prep (about 5 minutes)

List the user's chosen tasks, grouped by location so they move around less.

```
- [Kitchen task, e.g. fill water bottle for the morning]
- [Bathroom task, e.g. brush teeth]
- [Hallway task, e.g. put keys and bag by the door]

Reply "done" when all set.
```

If a small task surfaces ("library book is due, return it tomorrow"), do not solve it. Capture one line so it leaves the user's head:

- Append to tomorrow's capture spot. Preserve existing text exactly, never overwrite from an earlier cached value, and never create a partial review record.
- Then say: "Noted. Captured."

## Step 3: Settling practice

One line naming the practice, for example: "Ten slow breaths." Give no instructions if the user already knows the practice. Never introduce something new at bedtime. Wait for "done" or similar. Add, remove, or restore this step whenever the user asks.

## Step 4: Close

Say only, adapted to the user's setup:

> That's everything. Lights off and straight to bed.
>
> Talk tomorrow.

No recap and no "sweet dreams". This is the last message tonight. Move silently to the audit.

## Step 5: Routine audit (silent)

After the close, review the run without sending anything. Do not ask a tired person to diagnose their own ritual. If the user approved direct edits, update the routine. Otherwise, save proposed changes for daytime review. Do not report what changed.

| Signal | Change |
|---|---|
| User misread a prompt or asked what it meant | Rewrite it in plainer words |
| User pushed back on a step | Simplify it, make it optional, or cut it |
| A lookup failed or found the wrong record | Fix the lookup rule |
| An item is skipped without comment | Remove it |
| User stated a preference ("don't ask me X") | Add it as a hard rule |
| The barrier keeps being bypassed | Choose a stronger physical barrier with the user |
| The same worry keeps appearing at bedtime | Move its prevention into the earlier review or planning |

If the run was clean, change nothing. Do not invent improvements. If the user re-engages because they cannot sleep, go to Step 6.

## Step 6: Can't-sleep fallback (stimulus control)

Use only when the user reports being awake after the ritual. Do not rerun the ritual or reopen planning. Say:

> Get up for a bit. Low light, something dull like a paper book or folding laundry, nothing on a screen and nothing to solve. Go back to bed once you feel sleepy, and leave the clock alone.

This keeps the bed linked with sleep rather than with lying awake. Do not extend the reply. If sleep trouble is frequent or severe, suggest professional support at a daytime moment, not at night.

## Worked example (invented)

Alex says "wind down" with no records connected. Bedtime is an hour away and Alex wants the phone back after breakfast.

- Assistant: "Before we start: sleep clothes on, phone in the kitchen drawer until after breakfast. Reply 'done' when all set."
- Alex: "done"
- Assistant: "Fill a water glass, brush teeth, keys by the door. Reply 'done' when all set."
- Alex: "done. oh, need to call the dentist"
- Assistant: "Write it on the paper by your bed. Not tonight." Then: "Ten slow breaths."
- Alex: "done"
- Assistant: "That's everything. Lights off and straight to bed. Talk tomorrow."

## Exhaustion rule

If the user is clearly exhausted, they may skip Step 2 or Step 3. Do not skip Step 1, because it is the load-bearing step, unless a health, safety, accessibility, or caregiving need makes it unsuitable.

## Style

- Quiet and short. One question at a time. No preamble.
- No narration ("great, now let's...") and no emojis.
- No sleep science at runtime.
- If the user goes off-script with a work problem, deflect to the capture spot and tomorrow's review.
- Use the user's preferred date and time format.

The best wind-down is quiet, repeatable, and boring enough to become an automatic signal that the day is over.


---
name: plan-and-book-a-trip
description: Plan a trip around its purpose, compare complete journeys against the traveler's preferences, and book within clear limits. Use when someone needs flights, trains, or transfers found or booked.
---

# Plan and book a trip

Understand the trip before you optimize its transport. First learn what the traveler wants from the trip. Then turn the agreed brief into a small, priced set of practical options, and carry the chosen option through booking preparation or an authorized purchase.

The traveler's current instructions always win. Old receipts, past trips, and saved preferences are context, not permanent rules. Never turn one trip's dates, fares, or event plans into a lasting default.

## Quick version

- Ask why the traveler is going, who they will see, which dates are fixed, and how much flexibility they have, before looking at any fares.
- Ask for their standing preferences (seat, bags, cabin, stops, budget style) instead of assuming them.
- Compare two or three complete door-to-door options, including bags, seats, transfers, and any extra hotel night.
- Say clearly which prices are live, which are rough indications, and which are your estimates.
- Never buy, or say something is booked, without explicit permission and a provider confirmation.

## Core principles

- **Trip first, tickets second.** Saved preferences do not replace a conversation about what this trip is for.
- **You do the research and checking.** Gather facts yourself from authorized sources. Ask the traveler only about intentions, priorities, trade-offs, a missing fact, a login step, or an approval.
- **Compare complete journeys.** A cheap fare can hide an extra hotel night, a hard transfer, a lost day, or fees.
- **Label certainty honestly.** Separate live prices from indications and estimates, and verified facts from guesses.
- **Searching is not buying.** A request to find or compare travel does not authorize payment.

## Traveler profile

If your environment can save preferences, keep a short profile. Ask the traveler to fill in each line. People differ a lot here, so never assume an airline, cabin, seat, or rule is best for everyone. Record the date and whether each entry came from the traveler directly. Recheck status, benefits, and addresses before relying on them.

| Preference | Question to ask | Example answers (varied, not defaults) |
|---|---|---|
| Stops | Do you prefer fewer stops, lower price, or a mix? | "Cheapest with at most one stop"; "Direct if under a set extra cost" |
| Airlines or rail operators | Any you prefer or avoid? | "No preference"; "Collect points with one alliance" |
| Cabin or class | Which cabins should I always show? | "Economy only"; "Show the next cabin up for flights over a set length" |
| Seat | Seat type and how much a seat fee is worth to you? | "Aisle, pay small fees"; "Any seat, never pay" |
| Luggage | What will you bring? | "One checked bag"; "Backpack only" |
| Timing | Earliest and latest times you will travel? | "No departures before mid-morning"; "Red-eyes are fine" |
| Discount cards and memberships | Any rail cards, memberships, or status? | "Senior rail card"; "None" |
| Home base and free places to stay | Home airport or station, and friends or family to stay with? | "Nearest major airport"; "Can stay with a sibling in the capital" |
| Sleep pattern | Usual wake time and bedtime, with time zone? | Used only for jet-lag ranking |
| Budget style | Fixed ceiling, or "show me what each step up buys"? | "Under a set amount"; "Value for money, no hard cap" |

## 1. Understand the trip before searching transport

For a new trip, start with discovery. Do not search fares until the first trip questions are answered. For a continuing trip, reuse the agreed brief and ask what changed. If the traveler asks to skip discovery or wants one narrow check, do that.

### Gather relevant context

Read the conversation, the saved profile, and any invitations, agendas, or itineraries the traveler supplied. If the traveler has connected tools and clearly authorized it, you may also read their calendar, email, messages, and shared documents for this trip.

Rules for this step:

- Have a legitimate purpose: planning this specific trip.
- Use read-only access unless the traveler authorizes more.
- Search narrowly by event, destination, organizer, and dates. Use only the minimum relevant sources and information.
- Do not sweep unrelated messages or look into companions or other people. Respect their privacy.
- Leave unrelated or sensitive personal details out of your notes and outputs.
- Keep findings private to the traveler. Do not contact anyone without authorization.
- Keep addresses and identity details out of shareable summaries. Never store loyalty numbers, passport or identity numbers, payment details, or document copies in the profile; booking references go only in a private trip record.
- Saving lessons or preferences never adds permission to purchase, message others, or access accounts.

Look for why the trip is happening, event dates and venues, existing bookings, and nearby commitments. If a source is unavailable, say so; never imply you checked it.

Distinguish an explicit goal from your guess, an invitation from confirmed attendance, and a calendar entry from a hard constraint.

### Interview the traveler

Briefly say what you know, then ask one numbered block of four to six questions. Ask fewer when much is settled. Ground each question in what you found.

1. **Purpose and priorities:** Why go? What would make the trip good?
2. **People and places:** Who is coming or being visited? Which stops are essential or optional?
3. **Time in each place:** How many days at each stop? Any extra stopover wanted?
4. **Dates:** What fixes the earliest departure and latest return? If dates are flexible, what range is useful?
5. **Pace, work, and recovery:** Holiday, work, or both? Do they need to arrive rested for something?
6. **Practical context:** Where can they stay? What is already arranged? Any accessibility needs, spending limits, or reimbursement rules?

Skip questions the profile already answers. Confirm the requested outcome: research, booking preparation, or an authorized purchase.

### Agree the brief

Summarize the brief and let the traveler correct it. Clear answers count as agreement.

| Brief item | Content |
|---|---|
| Purpose and priorities | [What the trip is for and what matters most] |
| People and stops | [Companions, visits, essential and optional stops] |
| Time in each place | [Nights per stop] |
| Fixed dates | [Hard constraints] |
| Flexible ranges | [Useful date windows; mark provisional dates] |
| Work and recovery needs | [Workdays, arrive-rested needs] |
| Accommodation and local transport | [What exists, what is needed] |
| Open questions | [Unresolved choices] |
| Requested outcome | [Research / prepare booking / authorized purchase] |

Keep provisional dates visibly provisional through every later step.

## 2. Research current options

Keep searches tied to the brief. If transport would force a real change to the trip, go back to the traveler with that choice.

1. **Search current schedules and fares** across the useful date range. Aggregators and date grids are good for discovery. Then verify the chosen itinerary, operating carrier, fare type, and conditions with the carrier where possible. List every suitable departure on each date, not just the cheapest.
2. **Apply routing preferences.** If the preferred routing is not available, check nearby airports and ground links, explain the options, and ask before settling.
3. **Compare ticket shapes.** Compare a round trip with an open-jaw ticket (arriving in one city, leaving from another) when both fit. Include the ground travel each one needs.
4. **Check ground transport to the real destination.** Confirm the right station when names are ambiguous. Check timetable release dates, holiday service, and planned works. Do not invent a train or fare before it is published.
5. **Apply discount cards** to every eligible price. Check validity on the travel dates, time-of-day rules, and eligibility.
6. **Handle failures openly.** If a tool or provider fails, name it, give the error, say what is missing, and try a safe recovery. Disclose any change of source.

Label every price as a **live selected itinerary**, a **date-grid indication**, or an **estimate**. A "from" fare is not an available ticket. Record when each price was checked, and share only links you have verified.

### Compare the actual product

- **Cabins:** confirm the cabin on each segment. Extra-legroom economy seats are not a separate premium cabin. If a route lacks the cabin the traveler wants, say so instead of relabeling another product.
- **Overnight flights:** when sleep matters, check the actual aircraft's seat type. A cabin name alone does not tell you whether the seat is flat.
- **Mixed cabins:** consider a higher cabin on one leg and a lower one on the other.
- **Seats and bags:** include seat fees. A seat preference does not guarantee an assignment. Check the fare's bag allowance, size, and weight limits. A personal-item-only fare does not cover a carry-on or checked-bag need.
- **Rail classes:** confirm the named class and its conditions. When the traveler has a rule about stepping up a class, price both classes for each train and show the difference, plus any extra flexibility the higher class gives.

### Rank flight times for jet lag

For long-haul flights across several time zones, rank times by fit with the traveler's body clock, alongside price and cabin. This is general planning guidance, not medical advice.

1. Use the traveler's usual wake time and bedtime in their home time zone.
2. Estimate the body-clock low point at about two hours before usual wake time.
3. **Eastbound:** favor flights that allow sleep during the usual night and land near the body-clock low point. Then avoid bright early light at the destination for the first days and seek afternoon light.
4. **Westbound:** favor daytime flights that land in daylight with a short stretch to a normal local bedtime.
5. Add a simple pre-trip shift (moving sleep gradually toward the destination) and a light plan for the first days.

Example: a traveler flying five time zones west for a family visit might prefer a late-morning departure that lands mid-afternoon local time, rather than a late-evening flight that lands after their body thinks it is the middle of the night.

## 3. Compare complete journeys

Show two or three useful options with a recommendation. If only one route fits, say so.

- Show local departure and arrival times, airport or station codes, duration, and next-day arrivals.
- Show total cost, currency, fare type, cabin on each segment, seat fee, bag allowance, and change or refund limits.
- Compare basic and standard fares; a low headline price can lose once seats and bags are added.
- Keep currencies separate or label a conversion estimate.
- Build realistic buffers for security, immigration, bags, and cross-city travel. Use the provider's recommended arrival time.
- Distinguish a protected connection from separate tickets and say who bears the risk of a delay.

### Worked example (fictional)

A traveler is going from Riverton to Lakeport for a four-day conference, wants an aisle seat, and is bringing one checked bag. All carriers, prices, and places below are invented.

| Option | Route and times | Cabin and fare | Complete cost | Main benefit | Main drawback |
|---|---|---|---|---|---|
| A (recommended) | RVT to LKP direct, depart Tue 11.05, arrive 14.20 | Economy, standard fare | 412 (fare 340, bag 45, aisle seat 27) | Arrives in time for the opening dinner; free changes | 74 more than B |
| B | RVT to LKP via Hillford, depart Tue 06.40, arrive 13.55 | Economy, basic fare | 338 (fare 255, bag 55, seat 28) | Cheapest | Very early start; 50-minute connection; no changes |
| C | Train to Lakeport, depart Mon 15.00, arrive 21.30 | Standard class, flexible ticket | 298 (ticket 168, extra hotel night 130) | Calm journey, can work on board | Adds a night away and a hotel |

Recommendation: A. The extra 74 over B buys a sensible start time, no tight connection, and a changeable ticket. Prices for A and B are live; the hotel cost in C is an estimate.

## 4. Present and book

Lead with the recommended dates and route. Show each cabin the traveler asked to see. Show ground transport separately. Include verified booking links, when prices were checked, anything unverified, and the decision needed.

Prepare a concrete, reviewable booking before asking for any approval that is needed. If the traveler already authorized this purchase, or a clear scope and budget, continue within it.

Before submitting, check against the agreed option:

- passenger name exactly as the form requires, using details the traveler supplied;
- dates, airports or stations, operating carrier, and routing;
- cabin or class and fare type on each segment;
- seat, luggage, total price, and terms.

Resolve any mismatch first. Never invent identity or payment details.

After purchase, confirm success from the provider's confirmation. Report the booked journey and total, and flag any unassigned seat or remaining transport. A selected fare or unfinished checkout is not a booking.

## 5. Learn from experience

If the traveler wants you to keep improving their profile, save clear lessons at a natural stopping point.

- **Lasting preferences:** update the profile entry, keep any qualifications, and replace old entries rather than piling up contradictions.
- **Workflow lessons:** fix a missed question or wasteful step.
- **Temporary information:** keep one-off fares, exceptions, and lucky deals in the trip record. Do not turn one cheap choice into a budget. If it is unclear whether a choice is for "this trip" or "from now on", ask.

## Readiness gates and common failures

Before moving on, confirm:

- **Before searching:** the brief is agreed, or the traveler skipped discovery.
- **Before recommending:** prices are labeled, each cabin is the real product, extras are included, and the full journey is costed.
- **Before purchase:** authorization covers this booking and every checkout detail matches.

Common failures:

- letting an early fare search decide the shape of the trip;
- treating extra-legroom economy as a premium cabin;
- ignoring seat, bag, transfer, or hotel costs;
- reporting a "from" fare or a waitlist as available;
- treating an old receipt as a current preference or price ceiling;
- saying a ticket is booked before seeing a confirmation.

## Optional extras

Use these only when the traveler asks or the trip clearly calls for them.

### Upgrades

- Compare three paths: buying the higher cabin outright, changing the ticket into it at the fare difference, and a separate upgrade offer.
- Separate a confirmed cabin from a waitlist. An empty seat on a seat map does not prove an upgrade will clear. If a better cabin really matters, recommend securing a confirmed option.
- Do not claim any moment is reliably cheapest for upgrades. Prices can rise and seats can sell out.
- Check that the fare type can be upgraded before buying it; basic fares often cannot.
- Compare cash with points using a stated value per point, and read the upgrade's own refund and change terms.
- For an existing booking, check personal offers only through an authorized session, and never submit anything outside authorization.

### Fare and upgrade monitoring

Never promise to watch prices between conversations unless a real scheduled mechanism exists. If the traveler chooses a monitoring service:

1. Confirm the trip appears in the service.
2. Set an alert, not an automatic purchase or bid.
3. Monitor the leg that matters most.
4. Leave automatic repricing off unless the traveler asks; it may charge fees or change fare rules.
5. If a trial or subscription starts, set a cancellation reminder before the first charge.

When an alert arrives, the traveler (or you, within explicit authorization) books through the provider after rechecking the details.


---
name: meeting-prep
description: Research the people and history behind a meeting, clarify the outcome wanted, and produce a focused brief and agenda. Use when someone says prep my meeting with a person, or before an important call.
---

# Prepare for a meeting

Use this workflow to prepare one consequential meeting, such as a client, partner, hiring, advisory, project, fundraising, negotiation, or relationship-building conversation. The deliverable is a finished preparation page or document in the user's chosen workspace. A research summary in the chat is not the deliverable.

The order is fixed:

1. Research, scoped to the meeting's purpose.
2. Post a situation brief.
3. Ask targeted questions and wait for answers.
4. Build the page from those answers.

Skipping the questions is the most common and most costly failure. Research cannot tell you what the user wants from the meeting, what they can offer, what tone they want, or what to avoid. The agenda usually changes after one round of questions. Asking costs one turn. Skipping can produce a wrong agenda.

To prepare several meetings, run the workflow separately for each one. Do not mix unrelated contexts on one page.

## Boundaries

This is meeting preparation, not a background check. The aim is to understand the working relationship and the topic, not to profile a person.

- **Purpose and authorization.** Use private messages, calendars, chat, notes, and internal records only for a legitimate purpose tied to this meeting, only where the user has clearly authorized access, and only as their organization's policies allow. If a source's scope is unclear, ask first. Records collected for one purpose, such as an application, may be used only when the meeting concerns that purpose.
- **Minimum necessary.** Search the fewest sources that answer the research questions, read only relevant material, and summarize rather than copying raw messages or records. Do not keep side notes after the page is done unless the user asks and it is permitted.
- **Sensitive details.** Do not search for, infer, or record sensitive personal information such as health, family status, religion, politics, ethnicity, immigration status, age, personal finances, or criminal history. Leave out home addresses, personal contact details, personal social media, and gossip. If you encounter such details by accident, do not use them.
- **Money on shared pages.** Never put compensation, offer, equity, grant, or budget figures on a page a team or wider group can read. Refer to them without numbers, such as compensation discussion or above the typical amount.
- **Consent.** Recording, transcription, and reference conversations must follow consent rules and organizational policy. Never set up hidden monitoring.
- **Output access.** The situation brief stays in the user's private session. The page must match whoever can read it (see Step 7).

## Inputs to confirm

Ask for anything that is missing. The defaults below are suggestions; use the user's own preferences when they state them.

| Input | What to establish | Suggested default |
|---|---|---|
| Meeting | Title, date, time zone, duration, attendees, format, link | The meeting the user names |
| Scope | Which meetings to prepare | One meeting; for a day, external and small-group meetings, skipping personal and routine internal blocks |
| Purpose | Invitation wording or best-supported reason the meeting exists | From the invitation |
| Destination | The user's chosen workspace, database, notes tool, or document format | Ask |
| Audience | Private, restricted internal, or readable by other attendees | Ask if unclear; assume shared when in doubt |
| Sources | Which messages, calendars, chat, notes, records, and public sources are authorized | Ask |
| Page style | Title format, length, and whether to script spoken lines | Date plus person or topic; scripted only on private pages |

If several events match the request, confirm which one before researching. In group meetings, research only decision-makers and people central to the topic.

## Step 1: Read the meeting record

Open the full event, not just the title. Capture the date, time, time zone, duration, organizer, attendees with work contact details and organizations, location or link, description, linked files, and any reschedule or scheduling notes. Separate confirmed, optional, and unknown attendees where you can, and confirm it is a real meeting rather than a placeholder block.

## Step 2: Gather context in proportion to the stakes

Research answers four questions and nothing more:

1. What professional role does each relevant attendee play in this meeting?
2. What is the working relationship history?
3. Why is this meeting happening now?
4. Which facts, decisions, and materials will shape the conversation?

A routine check-in may need only the invitation and the last meeting's notes. A first meeting about a large decision may need more. Start with the sources most likely to answer the questions and stop once they are answered.

**Sources, roughly in order of value:**

- **Work email.** First search direct correspondence with the attendee's work address for commitments, tone, and recent exchanges. If the reason for the meeting is still unclear, also search recent work threads that mention their name or organization; this often finds the introduction, referral, or process that triggered the meeting. Read the few most recent relevant results in full, not just snippets.
- **Team chat, notes, and calendar history.** Earlier meeting pages, project notes, topic channels, and past events with the same people, to build the relationship arc.
- **Your organization's own records.** If the meeting concerns something the person submitted, such as an application, proposal, request, or inquiry, read that record by work email first, then by name. Say in the brief what you found, or that you checked and found nothing. Keep evaluator comments within their access boundary.
- **Public professional information.** Name plus organization, to confirm current role and what the organization does. Capture a few professional links and any recent work-related news that bears on the topic. Do not use people-search or data-broker sites or sources about private life.

**Identity.** A name match is not an identity match. Before using an older record, check that its work email, employer, or project fits the attendee's current professional profile. If it does not, leave it out or label it as possibly a different person.

**Origin.** Some first contacts happen in channels your tools cannot search. Prefer the most direct evidence of who initiated the meeting, such as an internal note that a colleague recommended the person, over indirect signals like a generic third-party email. If the origin is unclear, say so instead of guessing.

**Evidence quality.** Label any claim from one source, an old source, or a weak source with its source and date. State conflicts between sources. Never build a question on an unlabeled shaky claim.

**Hiring and assessment meetings.** Focus only on role-relevant capabilities, role alignment, work samples and other diagnostic evidence the candidate provided, and whether the planned questions will distinguish relevant performance. Use the same criteria for every candidate in a process and keep notes within the hiring team's boundary.

## Step 3: Read the artifact the meeting is about

If a proposal, deck, draft, memo, plan, application, or contract is the reason for the call, read all of it, including every tab, appendix, and linked section. Signals include feedback requests, draft or deck subject lines, comment notifications, phrases like I shared the proposal, linked files in the invitation, or a request to discuss something that probably exists in writing.

Extract the author's ask, key assumptions and evidence, decisions requested, risks, deadlines, alternatives, and the exact points where the user could challenge, support, or decide. For applications, the plan, disclosed alternatives, named references, and weak points often give the sharpest questions.

Generic questions like tell me about your plan look unprepared when a detailed plan exists. If the context implies an artifact you cannot find, ask the user for it in Step 6 rather than drafting blind.

## Step 4: Check whether a specialized workflow applies

Some meetings need their own process: hiring reference calls, formal interviews, legal, compliance, or performance meetings, and incident reviews. A reference call is signaled when an introduction describes the attendee as someone who can speak to a candidate's work, the title says reference, or the attendee is a former manager or colleague of a current candidate.

If a specialized process exists, switch to it and carry forward only the relevant research. A reference process should confirm consent, use a standard question list with role-specific probes, cross-check themes from earlier referees, and separate direct observation from hearsay. Otherwise, continue.

## Step 5: Post a situation brief

After research is finished, post a brief the user can read in about a minute to reload the situation. Include only what helps this meeting. Do not propose a goal or agenda yet, because proposing first anchors the user before they say what they want.

Pick the shape that fits and write it; ask the user to choose only if you are genuinely torn on a high-stakes meeting.

- **Narrative brief (default).** Short headed sections: who they are professionally, where things stand, why the meeting is happening, and the live tensions.
- **Decision-shaped brief.** For negotiations, closes, recruiting, or fundraising with a live competing option: the ask, their disclosed alternatives and deadlines, your position, the risks, and the open unknowns.
- **Stacked brief.** A short narrative followed by a decision section when the user needs both the who and the deal.

Other shapes, such as a facts table plus bullets on dynamics, are fine when they fit. Run the reference check below before posting.

If your interface tends to drop text shown just before a question widget, end the turn with the full brief and a closing line such as Questions incoming, then ask at the start of the next turn. Never replace the brief with a one-line recap.

## Step 6: Ask targeted questions

Ask about targets, shape, and failure modes. Do not ask what the agenda should be; turning answers into an agenda is your job. Cover the goal, at least one other axis, and always a final catch-all.

| Axis | What it settles |
|---|---|
| Primary goal | Recruit, advise, build the relationship, decide, gather information, sell, close, or hand off |
| Their situation | Ambiguity in the research, such as whether they are still in a role, exploring, or committed |
| Sensitive substance | Whether the user shares an honest view early or hears theirs first |
| Failure mode | Overselling, underselling, the wrong topic, or no close |
| Specific ask | Introduction, money, time, advice, or commitment, and how direct to be |
| Authority | Whether the user can decide or offer something during the meeting |
| Anything else (always) | Context, history, constraints, or points to land or avoid |

Rules for questions:

- Give each question three or four mutually exclusive options, with the most likely answer first and marked recommended. Offer real alternatives; a less obvious pick often changes the agenda.
- When two answers can sensibly combine, such as a date and a named deliverable, offer the combination as its own option.
- Ask only questions that shape the agenda, usually two to six. If your tool limits questions per message, use rounds rather than dropping any. Put questions whose answers change other options first, tailor later rounds to the answers, and put the catch-all last.
- Number questions continuously across rounds and label every option with its question number and a letter.

```markdown
1. What is the primary outcome?
   - **1a (recommended):** Understand their interest and secure a concrete next step
   - **1b:** Build the relationship only
   - **1c:** Make a direct pitch

2. How direct should the close be?
   - **2a (recommended):** Propose a dated follow-up with a named deliverable
   - **2b:** Offer help and let them choose
   - **2c:** Make no ask

3. Anything else to land or avoid?
   - **3a (recommended):** Nothing to add
   - **3b:** I'll add notes

Reply with the labels, e.g. 1b, 2a, 3a.
```

Before sending, check that every question is numbered, every option has one unique label, labels run in sequence, and the catch-all is present.

Time pressure is not a reason to skip the questions; the user decides whether to go in without a page. The only exception is a recurring meeting with a documented, fixed purpose and no open decision. When unsure, ask.

## Step 7: Build the page

Confirm that Step 6 happened and you have answers. If not, go back. Run the reference check, then create the page in the user's chosen system.

**Decide who can read it first.** If other attendees, teammates, or a shared database can see the page, use the shared agenda. Use the private structure only when no other attendee can read it.

**Properties.** Use the user's title format, or the meeting date plus the person's name or topic if they have none. Store the date without a time if the field allows it, checked against the user's time zone. Add attendees as the system expects. Reopen the saved page to confirm the date, location, and permissions are correct, and fix anything wrong. If the system offers a meeting-notes or transcription feature, add it only with participant consent and in the place where it works.

### Private preparation page

```markdown
## Context
[Professional role, relationship arc, why the meeting is happening, key links. Note if this is a first meeting.]

## Goal
[Goal confirmed by the user's answers]

## Agenda
### 0–5 min: Open and frame
**Say**

[Exact opening words]

**Private note**

[What to avoid in the open]

### 5–20 min: Diagnose [topic]
**Questions**

1. [Question]
2. [Question]

**Private note**

[What to press on and signals to listen for]

### 20–35 min: Pitch or pressure-test [topic]
**Say**

[Exact transition]

**Private note**

[Specific moves or concrete asks]

### 35–45 min: Close
**Question**

1. [Close asking for a date, deliverable, or next step]

**Private note**

[Backup close]

## Five most important questions
1. [Most decision-relevant question]
2. [Question]
3. [Question]
4. [Question]
5. [Forcing close]

## Timely note
[Recent work-related item worth mentioning, or none]
```

Writing rules for private pages:

- Make each stage a level-three heading with bold labels. Number questions, write notes as short prose, and make the times add up to the meeting length.
- A Say block holds only the exact words to be spoken, written in full, without quotation marks. Never mix instructions into it. Put any cue on its own line in square brackets.
- The ranked questions are an in-call cheat sheet: one line each, scannable in seconds. For persuasive meetings, include at least one question on the gap between the other party's current and desired state, and end with the forcing close. For pure discovery, all can be discovery questions. Five is a good default; more dilutes it.
- Use bullets for history and prose for summaries. For recurring contacts, summarize the relationship arc, not just the last interaction.

### Shared agenda page

Remove scripts, private notes, bracketed cues, tactics, candid assessments, and sensitive details. Write in neutral or we voice.

```markdown
## Purpose
[Shared purpose]

## Context
[Context suitable for every reader]

## Agenda
### 0–5 min: Align on purpose
- [Topic]

### 5–25 min: [Main topic]
- [Question or decision]

### 25–30 min: Next steps
- [Owner, deliverable, timing]

## Decisions to leave with
1. [Decision]
2. [Decision]
```

## Reference check

The user reads the brief and page cold, so everything you found is new to them. Run this before posting the brief and again before creating the page.

1. List every proper noun. For each, ask whether the user would know it without your research.
2. Give researched names a short professional explanation where they appear, such as their co-founder, now at another company. Names the user supplied or clearly knows need none.
3. Make each section stand alone by repeating the explanation, or reword the question so it needs no name.
4. Cut names that do not help a question or decision.
5. Keep source and date labels on shaky facts.

## Step 8: Audit, follow-up, and handoff

| Check | Pass condition |
|---|---|
| Questions | The brief was posted and the user's answers shaped the goal and agenda |
| Meeting | Date, time zone, attendees, duration, and destination are correct |
| Scope | Only authorized, meeting-relevant sources were used |
| Sensitive data | No sensitive personal details or raw message copies appear |
| Evidence | Claims are supported, labeled, or removed; identities are confirmed |
| Artifact | The relevant artifact was read in full, or its absence is stated |
| Access | Only the intended audience can read the page; shared pages have no script, tactics, or money figures |
| References | Every unfamiliar name is explained or cut |
| Agenda | Times add up, questions are specific, and the close names a date, deliverable, or owner |

For persuasive or high-stakes meetings, offer to schedule a post-call review shortly after the meeting using an authorized reminder or automation tool, and pass it the page location and counterparty so it can start without other context. The review should use notes or a transcript only with consent, record commitments, objections, and what was learned, set next steps with owners and dates, and note the user's recurring communication patterns. Store it under the same access limits as the private page. Skip this for purely informational meetings.

Finish by giving the user the page link, stating any limitations such as a missing artifact, unconfirmed identity, or conflicting sources, and saying whether a review was scheduled.


---
name: meeting-actions
description: Review meeting notes or transcripts, capture real unfinished commitments as clear tasks, and batch only the unclear ones as questions. Use when someone asks what they committed to or wants meeting follow-ups.
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
name: message-to-task
description: Turn a message thread into researched, partly completed work, and create a task only when tracking will help. Use when someone shares a message and says make this a task, track this, or deal with it.
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
name: inbox-zero
description: Work through an email or message inbox to zero, turning each item into a clear next action without drifting into deep work. Use when someone wants to triage, clear, or prioritize an inbox.
---

# Process an inbox to zero

Help the user empty one or more inboxes into a single trusted task system. Every item ends in exactly one bucket: **do now**, **quick win**, **delegate**, **task**, or **no action**. When a run is finished, nothing that needs doing should exist only in an email, team chat, comment thread, or messaging app. Each item is done, delegated, recorded as a task, or cleared because it needs nothing.

This follows the Getting Things Done and Inbox Zero methods. Processing an inbox means deciding what each item is and where it goes. It does not mean doing all the work the items describe. The task system is the one trusted list. Choosing what to work on from that list belongs to a separate planning workflow.

A message is urgent because of what happens if it waits. Being new, unread, long, loud, or in a busy group chat does not raise its priority on its own.

## Setup choices

Confirm these once with the user, or use the defaults. Store the answers as configuration, not as message content.

| Choice | Default | Notes |
|---|---|---|
| Work cap for do-now items | 15 minutes | Anything longer becomes a task |
| Quick win threshold | 2 minutes | Short reply, yes or no, RSVP, forward, access approval |
| Batch sizes | Do now 1, quick wins 5, delegate 3, task 3 | Small batches feel less overwhelming; too small feels slow |
| Chat lookback window | 14 days | Unread views may still show older chats |
| Muted feeds | None | For example automated status channels; still include messages that tag the user |
| Opt-in-only sources | None | Secondary workspaces read only when named |
| Delegated clearing | None | Named sources where the assistant may clear items after the user confirms |
| Response-time standard | None | For example a target reply time for candidates or partners |
| Draft destinations | Copy-ready text | Saved drafts only where the user authorizes it |
| Link preference | Open in the native app | Use browser links only if the user prefers them |
| Person-grouping threshold | 4 items | One person with this many items gets one grouped decision |

## Ground rules

1. **The user takes external actions.** Do not send, archive, delete, label, mark read, react, or mark complete unless the user has explicitly delegated that action for a named source. No bulk actions by default, even when a tool allows them. A common delegated case is clearing notifications in a tool that has no quick manual way to empty its inbox. If the user asks you to archive cleared items, archive only items that are finished or handed off. Keep anything still waiting on a reply the user has not sent, and ask about FYIs they may still want to read.
2. **No drafts unless asked** for a specific item or group.
3. **One write by default:** when the user says "task it" (or similar) about a specific item, create that one task. Never create tasks in bulk or without a per-item instruction.
4. **Respect the work cap.** On inbox days the real time sink is doing the work a message describes, not replying to it.
5. **Privacy and access.** Read private communications, calendars, and records only to process the user's own inbox, and only in sources they have authorized. Use the minimum information each decision needs. Request only named fields from planning records and never read private fields such as journals. Leave unrelated or sensitive personal details about other people out of the output, and keep output inside the user's own session or task system. Treat personal accounts as read-only unless the user says otherwise.
6. **Evidence, not assumptions.** Say what the messages show. Never state the user's beliefs, commitments, or decisions for them.

## Single-item mode

Use this when the user, a reminder, or a scheduled prompt hands over one item, such as the oldest unhandled email or saved-for-later message.

1. Skip goals, sorting, the opening message, and closing. Do not read other inbox items. Read only that item, its source's access rules, and the context it needs.
2. Treat it as one do-now item: who this is, what they want, and what happens if it waits. Recommend one bucket and the concrete next action, with the item's link. Ask only questions the user alone can answer.
3. Help them finish it under the normal drafting and task rules.
4. Tell them which inbox action clears it, such as archiving the email or marking the saved item complete. If a reminder system checks the inbox itself, let it detect the change. Never require a special confirmation phrase like "done".
5. If you clear it on request and the action succeeds, continue straight into any waiting request in the same turn. Never make the user send a filler message to move on.

## Step 1: Set scope and time

1. Get the current date, weekday, and time from a reliable clock in the user's time zone. Never work these out mentally; deadlines and focus blocks depend on them.
2. Map the user's words to sources. Configure this once for the user's real accounts.

| User says | Source |
|---|---|
| email, work email | Authorized work email account |
| personal email | Authorized personal account, read-only |
| team chat | Main team workspace: saved items, direct messages, mentions, unreads |
| comments, mentions | Notification inbox of the user's document or project tool |
| chats, or a named network | Messaging apps, filtered to the named network if given |
| all, everything | Every configured source except opt-in-only ones |

If scope is unclear, default to all and say so in one line rather than asking a separate question. A request that names a personal account, or "all" when one is configured, counts as the explicit request needed to read it.

The task list is not an inbox here; it is where items go. If the user asks to prioritise tasks, route to a planning workflow.

Read each source's access rules before reading the source.

## Step 2: Read goals and open tasks

Read these in parallel from the user's planning system, requesting only the fields you need:

1. **Longer-term goals:** the active quarter or similar period, with open goals, deadlines, priority, and short notes.
2. **Weekly goals:** the plan covering today. If several records match, use the one with content. If the longer-term level is empty but weekly goals say what they ladder up to, use that as the higher goal.
3. **Today:** intention, plan, and most important task (MIT).
4. **Open tasks:** title, status, and due date, so you can spot items that are already tasked.

Use the system's documented date functions. Plain string comparisons on dates often fail silently, so treat an unexpectedly empty result as a possible query error. If a level is missing, say so in one line and continue with what exists. Do not invent goals. Summarise the goals in three to six lines for yourself and use them to judge every item.

**MIT check.** If today's MIT is not inbox work and the user is inside or near its planned block, ask once, before reading any inbox: "Is this the most important thing right now, or does it just feel productive?" Trust the answer. Skip this when there is no MIT or inbox work is part of the plan.

## Step 3: Read the inboxes

Read every source in parallel. For each item collect: source, sender, subject or chat, date of the last message, who sent the last message, a one-line gist, and a link.

Apply these principles across sources:

- **Use the right view.** Prefer a purpose-built inbox, notification, or reply-debt view over general search, which often misses saved, unread, and last-sender state.
- **Get everything.** If a result hits its page limit, query again for older items. For a notification inbox, process every uncleared item, read or unread; the run is done only when the total is zero. Opening a notification may mark it read without clearing it.
- **Group to the decision unit.** Group email messages by thread and keep the latest. Treat several comments feeding one document as one decision: has the user already used them? If yes, clear them; if not, offer one task for the document rather than one per comment.
- **Skim, then open only when needed.** Send obvious newsletters and automated mail straight to no action. Open the full thread when the preview leaves the ask, deadline, owner, or status unclear. A reply deep in a long thread usually needs the full thread.
- **Find reply debt by last sender, then read back.** For chats, check who sent the last meaningful message within the lookback window. Before calling a chat handled, read back to the user's last real reply: a quick logistics exchange or closing message can sit on top of an older unanswered ask, such as an invitation sent the day before.
- **Rank direct above broadcast.** Direct messages and explicit mentions come before group or channel traffic, unless a group message names the user or has a time-bound consequence.
- **Respect deliberate saves; mute chosen noise.** Saved-for-later items count, even from muted feeds, because the user chose to keep them. Unreads are attention debt, not priority. Leave muted-feed unreads out of every bucket and count unless a message tags the user.
- **Default automated items to no action.** Newsletters, receipts, calendar notices, reactions, automated mentions, pointers to deleted or emptied content, and resolved discussions go to no action, unless they point to a deadline, a money or security issue, or a record that now needs the user (for example a record newly assigned to them with no next step). Permission requests are quick wins. Items over two weeks old with no open ask are usually stale; group them for one decision.
- **Never invent links.** Prefer links that open the exact item in the app the user uses, when that is their preference. Copy links from tool output, or build them only from a format verified in this setup. Otherwise cite sender, subject, and date and say the link is missing.

**Failures.** If a source fails or is disconnected, name the source, the exact error, and the missing data. Try the safe repairs in its access rules, such as re-authentication steps, then continue with the other sources. Never drop a source quietly or substitute one that cannot provide the same data. Put failures at the top of the output so the user sees the gap first.

## Step 4: Sort into buckets

Put every item in exactly one bucket:

1. **Do now:** important and urgent, finishable within the cap. Aim for three to five; extras are probably tasks.
2. **Quick wins:** under the quick win threshold. The user batches these.
3. **Delegate:** someone else should own it. Name the suggested owner by name or role with brief evidence ("owns operations", "is running this hiring process"). Find owners from the thread, recent discussion in the relevant channel, project records, and notes on team roles. Check notes against current evidence, because roles change. If nothing is credible, say "owner unclear" rather than guessing.
4. **Task:** real work over the cap, or work that cannot happen yet. Give a suggested name, any implied due date, and why. If an open task already covers it, say so and suggest clearing the inbox copy.
5. **No action:** FYIs, resolved threads, automated notices, chats that ended naturally. The user clears these rather than deleting them, so do not call this bucket "delete". Show counts by type and name only items the user might be surprised to see.

Rank do-now items, and order every other bucket, by these signals in order:

1. **Hard deadline or time-bound decision:** due today or tomorrow, an expiring offer or event, a meeting that needs a reply first.
2. **Someone blocked on the user:** a teammate, partner, or candidate cannot move until they answer. Apply any response-time standard the user sets.
3. **Ladders to a goal:** today's MIT, then weekly, then longer-term. Name the goal.
4. **Relationship cost of delay:** key contacts, funders, personal relationships that go cold. Age is a supporting signal that differs by channel: an email unanswered for two days or a direct chat unanswered for three usually matters more than an old saved item.

## Step 5: Open the run

Do not show the full sorted list; seeing every bucket at once overwhelms. The opening message holds only:

```markdown
## Inbox zero: <date>, <sources>

**Missing data:** <failed or stale sources, or "none">
**Counts:** <N items: X do now, Y quick wins, Z delegate, T task, A no action>
```

Then go straight into the first non-empty bucket (or a person group, below) in the same message. Keep the full sort to yourself and reveal one batch at a time.

## Step 6: Work the buckets, one batch at a time

Go in bucket order and stop whenever the user wants. Each message shows one batch, or one do-now item, and asks only about what is on screen. Never ask about a later bucket early. End the turn and wait.

Answering a batch's questions is a decision, not completion. Move on only when the user says the batch is done. Until then, help them finish it, for example by drafting the replies they chose.

**Formatting:**

- Every time you name an item or person, including status notes, recaps, reminders, and question titles, link the name to its source.
- Number questions and letter options so the user can reply `1b, 2a`.
- Use real lists for groups. Never show severity or status by colour alone; use words, symbols, and order.

**Group by person first.** When one person accounts for several items across buckets (at or above the grouping threshold), show their pile before the buckets in one message, split into "needs you", "discussion", and "reading or FYI", and suggest one way to batch them, such as one task or an already scheduled one-to-one. Clearing a person's pile in one decision beats meeting the same name in every bucket.

**Batches:**

1. **Do now, one item per message.** Read the full thread and check the calendar around any dates it mentions; the user may already have added holds. Gather only the context this decision needs, such as earlier threads with the sender or a related project record. Before saying the user still owes a reply or introduction, search every channel they might have used; it is often done elsewhere. For hiring or assessment items, use the user's chosen hiring guidance and only authorized evidence about role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Then write a short paragraph: who this is, what they want, what is at stake if it waits, and the recommended action, with evidence linked. Ask one to three questions only the user can answer. When they say it is done, show the next item.
2. **Quick wins, a small batch per message.** Each item gets its link, a line of context, and one recommended action, with lettered options when there is a real choice. Say how many remain. Show the next batch when the user says this one is done.
3. **Delegate, a small batch per message.** Link, suggested owner, evidence. The user confirms or changes the owner.
4. **Task, a small batch per message.** Link, suggested name, due date. Create each one the user says to task. Flag existing tasks that already cover an item.
5. **No action.** Counts by type plus surprising items. The user clears them, unless they delegated clearing to you.

**Meeting-related items.** When an item asks for a meeting, check the calendar for meetings already booked with that person in the next week before suggesting a new slot; an existing one-to-one or session often covers the ask. When a do-now item is preparation for a meeting in the next day or two, such as a document to review before a call, offer a meeting-prep workflow once the user has decided on the item.

**Tick lists for items only the user can clear.** When the user must clear several saved items themselves, give them a list that mirrors their app's screen, in the same order the app shows:

| # | Opening words as previewed | Date | Decision |
|---|---|---|---|
| [position] | [first words of the message] | [date] | [✓ Clear, or Keep, plus a few words of reason] |

Afterwards, re-read the saved list to check the right items were cleared.

**Delegated clearing.** Clear an item only after the user says it is handled, done, or not worth acting on, or confirms the no action bucket. Never clear an item that is decided but not yet acted on, such as a reply still to post. Clearing a notification or marking a chat processed must never resolve, edit, or delete the underlying comment, thread, page, or record. Pass item identifiers in a way the tool reliably accepts, retry a transient error once, verify the result, and report it in one line ("Cleared 4, all verified, 29 left"). Name anything unverified as a failure, and know how to undo a mistaken clear. For chats, marking an item processed (so it does not return next run) is appropriate when the user handled it elsewhere, chose to ignore it, or confirmed no action; do not mark chats the user still has to answer, since a sent reply drops off on its own.

**Catch work done mid-run.** Users often reply while the run is going. Before each new batch, check recently sent mail and messages, drop anything already answered, and note each in one line instead of asking again.

**Good questions** resolve real uncertainty: whether a goal is still live, whether the user wants to handle a relationship or hiring thread personally, whether an unfamiliar sender matters, how much time they have. Do not ask what the data already answers. The user can move any item to any bucket; their choice is final.

### Drafts, only when asked

- **Check the request against the thread first.** If a requested point repeats or contradicts what the other person already said, or misreads the ask, say so in one line and draft the version that makes sense. Follow the user's voice and channel conventions.
- **Saved drafts, where authorized:** save each draft as a reply in its own thread, never at the top level of a channel or conversation. Confirm it attached to the right thread, then open it in the app the user prefers so they can edit and send. In group threads, use the channel's real mention format for the person being answered and anyone the draft asks to act. Do not also paste the draft into the conversation; just say it is saved and opened. If a draft already exists there, say so rather than overwriting it. If you cannot read saved drafts back, never recreate an edited draft from your own version: ask the user to paste their current text, and save the revision only after they remove the old one. Never send.
- **Everywhere else:** give one draft per response as copy-ready plain text in the final block, with the item's link on the line directly above. If the user wants it, also copy the text to their clipboard and say so. Finish all tool calls first so nothing pushes the draft out of the final block.

### Creating a task

Create one record with: a clear action name, open status, due date, importance, urgency, time estimate, and domain or project. Notes:

```markdown
**What:** one line: the ask and who is waiting.
**Source:** <link, or "<network>: <role or contact>, <date>">
**Context:**
- Key fact or constraint, with link.
- Deadline or related record.
**Next step:** the first concrete action.
```

Do not pre-draft replies in the task unless asked. Afterwards, tell the user the item can now leave its inbox and give the record link if available.

## Step 7: Close and improve

End with a short per-source status:

| Source | Cleared | Tasked | Delegated | Still open | Unreviewed |
|---|---|---|---|---|---|
| [source] | [n] | [n] | [n] | [n] | [n and reason] |

If many loops remain open, say so plainly.

**Readiness check before calling a run complete:**

- Every in-scope source was read, or its failure is named.
- Every item is in exactly one bucket.
- Nothing actionable lives only in an inbox: it is done, delegated, tasked, or explicitly left open.
- Every delegated clear was verified.
- No private or unrelated personal detail left the user's session or task system.

Then audit the run for friction: a pointless question, an item in the wrong bucket, a misbehaving source, context you had to hunt for, or a privacy risk. With the user's permission, update the workflow's configuration to fix the cause, keeping changes general rather than tied to one message. Never store message content, credentials, or unnecessary personal details.

## Common failure modes

- Dumping every bucket at once instead of one batch at a time.
- Moving on after the user decided but before they acted.
- Doing the work a message describes instead of tasking it.
- Flagging a reply as owed when it was sent elsewhere, or calling a chat handled when an older ask sits under small talk.
- Proposing a new meeting when one with the same person is already booked.
- Showing the same person in every bucket instead of grouping their pile.
- Duplicating a task that already exists, or guessing an owner instead of saying "owner unclear".
- Quietly dropping a failed source or substituting a weaker one.
- Treating unread, new, or loud as urgent.
- Inventing links, or clearing a notification by changing the record behind it.
- Taking an external action, such as sending or archiving, that the user did not delegate.


---
name: design-a-work-sample
description: Design a short, paid, take-home work sample that produces job-relevant evidence and is tested with simulated submissions. Use when someone is hiring and needs a work test or wants to improve one.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A work sample usually sits between application review and interviews. It is often the stage that gives the best evidence of whether a candidate can actually do the work, because it is hard to fake.

A weak work sample wastes candidate time, buries reviewers in submissions that tell them little, and lets poor matches through. A strong one compresses days of on-the-job judgment into a few hours of clear evidence.

The workflow is opinionated about order. First agree on what to measure. Then choose a shape. Then draft. Then test the draft with simulated candidates before calling it done.

## When to use this workflow

Use it when someone asks to design a work sample, create a take-home exercise for a role, or tighten an existing one.

Inputs to collect:

- **Role name.** If it is not given, ask once.
- **Intent.** Create a new exercise or improve an existing one. Infer this from context when you can.
- **Destination system.** Where the instructions will be pasted, such as an applicant tracking system, a shared document, or a message. This drives the formatting rules.
- **Hiring owner.** The person who approves each gate. All approvals below come from this role.

Do not use this workflow for:

- Interview questions, panel formats, or interview scoring guides.
- Multi-day or in-person work trials.
- Screening questions on an application form.

If the request could mean one of these, ask which format is needed before starting.

## Hard rules

1. **No design without a role description and a role-success profile.** The exercise is a function of the profile. Without one, it produces noise.
2. **Alignment memo before any draft.** Agree on what is being measured before writing candidate-facing text.
3. **Simulate two candidates before declaring version 1 done.** Analysis alone misses gaps that real submissions reveal.
4. **Candidate-facing text must read as edited by a person.** Apply the format checks on every pass.
5. **Every draft ends with notes for the hiring owner.** These surface choices worth challenging.
6. **Follow the people-data boundary below.** Hiring materials are about real people and must be handled with care.
7. **Measure only role-relevant capability.** Exclude protected characteristics and proxies for them. Offer a route to reasonable accommodations or an accessible equivalent format without lowering the role-relevant standard.

## People-data boundary

Designing an exercise rarely needs information about specific people. When the workflow does touch records about people, such as past hiring feedback, team notes, or prior submissions, apply these rules:

- **Legitimate purpose and authorization.** Use people-related records only to design or validate this exercise, and only when the hiring owner has confirmed you are authorized to use them for that purpose.
- **Minimum necessary.** Read only the sources and passages relevant to the role's capabilities. Prefer role descriptions, profiles, and anonymized examples of strong work over records about named individuals.
- **Omit unrelated or sensitive details.** Do not carry personal circumstances, health, family, compensation history, identity characteristics, or other unrelated details into memos, scenarios, simulations, or notes. Do not infer protected traits.
- **Respect consent and privacy expectations.** Do not reuse a past candidate's submission, words, or situation in a new scenario. Do not put real staff or real contacts into a scenario without their agreement.
- **Keep outputs inside the access boundary.** Alignment memos, simulations, reviewer guidance, and owner notes stay with the people approved to see hiring materials for this role. Candidate-facing text contains no internal or personal information.
- **If in doubt, ask.** If a source seems out of scope or sensitive, ask the hiring owner before using it.

## Step 1: Pre-flight

Confirm that two things exist:

1. A current role description: responsibilities, level, expected outcomes, reporting line.
2. A role-success profile, hiring plan, or equivalent: the capabilities and experience most likely to produce the role's outcomes.

If either is missing, stop. Do not accept "we will figure out the profile while designing the test." That creates a moving target. Use this message:

> Before we design the work sample, I need the role description and a role-success profile. I found [what exists], but not [what is missing]. Want me to help draft the missing piece first? It usually takes less time than iterating the exercise against an unclear target.

Do not proceed until both exist and the hiring owner confirms them.

## Step 2: Read the context

Read in full, within the people-data boundary:

- The role description and role-success profile.
- Linked planning notes the owner has authorized: sourcing notes, design notes, team constraints, anonymized examples of strong work.
- One or two existing work samples for comparable roles, if available. Use them only to calibrate tone, length, and structure. Do not copy their task shape. Different roles need different evidence.

Give a one-line status, for example: "Read 5 pages of role context and 2 reference exercises. Moving to the alignment memo."

## Step 3: Write the alignment memo

Do not draft candidate-facing text yet. Write a one-page memo titled **What we are testing for and why: [Role] work sample** with these sections.

1. **Load-bearing traits (3 to 5).** What the role succeeds or fails on that this exercise can surface in the time window. Phrase each as an observable capability. Weak: "strategic thinking." Better: "Finds the highest-leverage problem in a messy situation, explains the tradeoff, and delivers a useful first action."
2. **What we are not testing.** Important qualities that belong to other stages. Interviews can assess motivation, live reasoning, and conversational sharpness. A work trial can assess reliability over days and judgment under pressure. References can assess reliability over months and integrity. Naming these keeps the exercise honest about its limits.
3. **Calibration to level.** Junior, mid, senior, or leadership. Level drives payment, expected output volume, and how much context to provide. Junior candidates need more context and narrower tasks. Senior candidates should make tradeoffs and produce work another person could use without explanation.
4. **Failure modes to catch (2 or 3).** Specific work patterns that could look fine in a conventional process but would not meet this role's needs. Describe the pattern, not the person. Examples: a polished planner who does not ship; a fast executor who misses the central problem; a careful candidate who defers every meaningful decision.
5. **What strong looks like.** One paragraph describing a top submission: what it notices, what it decides, what it produces, how it handles uncertainty.

Present the memo and stop. Ask: "Does this match what you want this work sample to assess?" Do not move on until the owner confirms or amends it.

## Step 4: Propose three shapes

Once the memo is locked, propose three shapes. Each must:

- Test the load-bearing traits, each in a different way.
- Be scorable in about 20 minutes per submission.
- Be self-contained, with no access to internal tools or private data.
- Be graspable by a candidate in about 60 seconds.

For each option give the shape, what it tests, two sentences on why it is evaluable, and one main risk. Keep each to about 150 words.

Shapes that often work:

- **Triage pile.** For high-volume, communication-heavy roles. The candidate gets a start-of-week pile of 8 to 10 items, writes a plan, ships real drafts, and proposes one systemic fix.
- **Pick the highest-leverage thing and ship it.** For strategic operations and builder roles. The candidate chooses one priority from a brief, justifies it, and ships a minimum usable version.
- **Diagnose and ship one fix.** For pattern-recognition roles. The candidate reads a messy situation, writes a diagnosis, and ships one targeted intervention.
- **Source and pitch.** For recruiting, partnerships, and outreach roles. The candidate defines the bar for a target profile, finds non-obvious channels from supplied information, and drafts outreach.
- **Decision-useful analysis.** For research, strategy, and specialist roles. The candidate picks one of two areas and produces a take a decision-maker could act on.
- **Design a repeatable system.** For program and community roles. The candidate designs one event or process and the reusable system behind it.

If none land, propose three more based on the confirmed traits. Do not force a familiar shape onto a role because it worked elsewhere. Do not draft until the owner picks a shape.

## Step 5: Draft version 1

Fill in the template below for the chosen shape. Apply the format checks as you write. End with the notes section.

### Candidate-facing template

Replace bracketed placeholders. Use bold lines rather than headings for section headers if that pastes better into the destination system.

```
## [Role] Work Sample

This work sample assesses your ability to [2 or 3 trait verbs from the memo].

You have **[N] hours** total.

**Your mission**

[One paragraph. A specific situation, not an abstract task. Include any authority or unavailable-stakeholder constraint that forces decisions. End with one line restating what the candidate will produce.]

**Deliverables**

[2 to 4 parts with rough time guidance. Common operations pattern:
- Part 1: plan or analysis (about 45 to 60 minutes, about 400 to 500 words, shorter if sharp; name what you are choosing to skip).
- Part 2: ship the work (about 75 to 90 minutes, 5 to 7 real drafts or outputs; do not let the planning eat the shipping).
- Part 3: one systemic fix (about 20 to 30 minutes, usable by a teammate without further explanation).]

**Context**

[The program, project, or team being operated: size, audience, current state. If relevant, a list of fictional roles the candidate can reach this week, with deliberate availability choices.]

[Optional for triage shapes: The pile, then Reference notes.]

**Instructions**

- Spend **[N] hours** on this work sample.
- Submit **within [X] days** of receiving this message. Sooner is better.
- Submit a **single document or PDF**. If you built supporting materials (a spreadsheet, diagram, or database), include links with sharing enabled.
- **This is a paid work sample.** After submitting, use [the payment form] to request **[BASE AMOUNT]**. [Optional: We will pay **[BONUS AMOUNT]** if you submit within [Y] days.]
- You may use AI tools. Use them carefully and with judgment, and do not submit filler. Briefly note any material use.
- Show your **depth or sharpness** somewhere. Do not try to be comprehensive everywhere; invest your time where it shows what you can do.
- [Optional: Include a short, unpolished walkthrough video of 3 to 5 minutes. A minute of you thinking out loud beats five minutes of rehearsed narration.]
- If you need an accommodation or alternative format, contact [contact route].

**Anticipated questions**

- *A requirement is unclear. What should I do?* Make a reasonable assumption, as if you had asked us and the answer did not surprise you. Note the assumption briefly.
- *What if I do not finish in time?* Submit what you have, with a short note on where you got to and what you would do next.
```

Optional additions when the shape calls for them:

- **Time-zone question** for scenario exercises: "Respond as if it is [day] morning at your desk in [scenario location]. No need to adjust for your actual time zone."
- **Use-of-work question:** "Your work is used only to evaluate candidates for this role. Any other use we will agree with you separately."
- **The pile.** For triage shapes: 8 to 10 realistic, fictional items, each with timestamp, source role, and full text where communication is central. Several items should connect so that seeing the whole picture is rewarded.
- **Reference notes.** Inline data the candidate needs to make fair calls, such as backup capacity, escalation policy, or refund policy.

### Payment

Payment amounts are the hiring owner's choice. A broadly useful pattern is a base payment for submission within a week and a modest bonus for faster submission. Amounts can scale with level but do not need to match a senior candidate's hourly rate; the bonus mainly signals that speed matters. For roles where speed is central, a three-tier structure (for example within a week, within three days, within one day) filters on speed more strongly.

| Role level | Base payment | Early-submission payment | Early window |
| --- | --- | --- | --- |
| [Junior] | [amount] | [amount] | [days] |
| [Mid or senior] | [amount] | [amount] | [days] |

If the payment form supports prefilled links, create one link per amount (role name, amount, payment type), and hyperlink each dollar figure itself rather than generic text like "this form." Check every link before finalizing.

## Format checks for candidate-facing text

Sweep these on every pass. Many are signs of unedited AI output; others are rendering problems.

- **Dashes sparingly.** Prefer commas, semicolons, periods, or parentheses. One or two long dashes are fine; a text full of them reads unedited.
- **"By the end of [day]",** never "by end of [day]".
- **No horizontal divider lines** if the destination editor mishandles them. Use bold headers and natural breaks.
- **No tables** if the destination system does not render them. Use bullets with bold leads.
- **No punchy contrast slogans** such as "the bar is X, not Y" or "it's not just X, it's Y".
- **No stacked repetition,** such as three sentences in a row starting the same way, or several sentences each ending in a list of three.
- **One consistent locale** for spelling, chosen by the owner.
- **Sign-offs on two lines** ("Best," then the name on the next line) in fictional messages.
- **Clearly fictional contact details.** Use obviously placeholder addresses on a domain reserved for documentation examples. Never use realistic-looking personal addresses, because candidates may try to contact them. Do not wrap addresses in angle brackets, which can trigger autolinks.
- **Soft line breaks for metadata blocks.** Some paste flows merge consecutive lines (From, To, Subject) into one paragraph. Use the destination's soft-break method, such as an explicit line-break tag at the end of each metadata line. Avoid blank lines between header fields; they look wrong. Bullet lists are usually safe.
- **Names in the scenario.** Default to fictional names or role titles. Use a real colleague's name only with that person's agreement and the owner's approval. Keep fictional names consistent across items.
- **No confidential details,** credentials, private contact information, real candidate material, or sensitive internal data.

## Notes for the hiring owner

End every draft with a section titled **Notes for the hiring owner (not for the candidate)**. Write 3 to 6 tight bullets on choices worth challenging. Good entries look like:

- "I split the problem items across two groups to test pattern-spotting, but it feels contrived. Easy to concentrate them in one group instead."
- "Item 6 is obvious noise that takes five seconds to skip. Drop it or make it subtler; right now it does not separate stronger from weaker work."
- "Payment matches your other exercises for this level. For a speed-critical role, we could add a one-day tier."
- "I left out a recorded briefing from the project lead. More realistic, but costs production time."

Close with one question that pushes the next decision, such as "Where do you want to push first?"

## Step 6: Iterate

Expect three to seven rounds. Each round, output the **full updated exercise**, not a diff, so it can be pasted directly.

Typical feedback: too vague (tighten), too prescriptive (loosen), cut a section (cut and renumber), unrealistic details (check facts such as program length, team size, prices), format problems found late.

Apply feedback unless it would materially harm validity, fairness, privacy, or safety. If you disagree, say so once, briefly, offer an alternative, then follow the owner's decision.

## Step 7: Simulate two candidates (mandatory)

When the owner says the draft is close, run two simulations in parallel. Embed the full candidate-facing text in each. Both personas are synthetic; do not base them on real applicants or their materials.

- **Role-aligned persona.** A strong candidate matching the role-success profile. Produces a real submission for every part, as they would type it, plus about five sentences reflecting on choices, uncertainty, and time use.
- **Plausible role-misaligned persona.** An earnest, conscientious candidate who would pass screening at most organizations but whose work lacks one role-critical capability. Pick a relevant mismatch from the memo's failure modes: process-first where the role needs action, hedging where it needs decisions, designing systems where it needs shipping. Tie the difference to work evidence only, never identity or background. Same complete submission, in character.

Then write a synthesis:

1. **Where the exercise separated them sharply.** Items or parts with visibly different work.
2. **Where it did not.** Items both handled the same way. Floor checks are fine, but a central trait that fails to produce different evidence is a problem.
3. **What this tells us.** What the exercise does and does not predict.
4. **Improvements,** specific and ranked by impact.

## Step 8: Apply improvements

Rewrite the exercise and output the full version. Useful changes include making connected items more interdependent, removing obvious noise, adding a constraint that forces a real tradeoff, replacing an opinion prompt with a usable deliverable, sharpening reviewer guidance so it rewards the intended behavior, and removing trainable knowledge requirements. Make the exercise more diagnostic, not merely harder.

## Step 9: Optional external review

If others give feedback, assess each suggestion against the memo. State which to integrate, which to skip, and why, then output the full version. Treat review as input; the hiring owner decides. Share drafts with reviewers only within the approved access boundary.

## Step 10: Final readiness gate

Do not mark the exercise complete until:

- Role description, profile, and alignment memo are confirmed.
- The shape maps directly to the load-bearing traits.
- A qualified candidate can finish in the stated time.
- It is self-contained and needs no private access.
- Scenario facts are plausible and consistent with the real program or team.
- Payment amounts, links, deadline, and submission format are correct.
- Section order matches the owner's preferred layout (commonly mission, deliverables, instructions, anticipated questions, with context and the pile either appended or in a separate document).
- The format checks pass for the destination system.
- A reviewer can score a submission in about 20 to 25 minutes.
- Both simulations ran and led to any needed revisions.
- No sensitive or personal data appears in candidate-facing text, internal notes stay within the access boundary, there is no unpaid production work, an accommodation route is included, and proxy bias has been checked.

## Step 11: Capture lessons

Before closing, record anything learned in the team's own reference for this workflow: new format problems, new shapes that worked, failure modes the simulation exposed, payment changes, better template wording, memo refinements. Record lessons as general principles, without details about individual candidates. Summarize the changes in one or two bullets. Make small wording fixes freely; ask before structural changes such as adding a step or dropping the simulation.

## Common failure modes

- **Drafting before the memo is locked.** It costs several wasted rounds.
- **Testing trainable things.** Specific tool fluency, domain vocabulary, or field knowledge that a capable hire can learn in a few weeks. No item should require it.
- **Slow grading.** Over about 25 minutes per submission, a long exercise scales worse than a short one.
- **Dozens of micro-decisions.** Aim for one piece of substantive reasoning, five to seven substantive outputs, and one usable artifact.
- **A pile that does not connect.** Independent items test volume, not judgment.
- **Reachable stakeholders.** If every decision can be deferred to someone who replies quickly, decisiveness is not being tested. Make key roles unavailable during the window.
- **Word-count targets that invite padding.** "About 400 to 500, shorter if sharp" beats a wide range, or drop the target.
- **An optional video nobody records.** If it adds signal, frame it as something most strong submissions include.
- **Rewarding polish over substance** when the role needs something else.
- **Reusing real people's material** in scenarios or simulations without consent.
- **Declaring success without checking** that the exercise distinguishes the role-relevant performance it was built to measure.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, quick to score, and clear about what good work looks like.


---
name: run-a-reference-call
description: Prepare a focused reference call for a job candidate, with a briefing page, an opening, and questions that draw out specific evidence. Use when someone has a reference call coming up.
---

# Run a reference call

Use this workflow when a hiring manager is checking references on a candidate for a role at their own organization. The output is a ready-to-use call page saved in the user's notes or meeting system. It holds context, a tailored opening, briefing notes, and a question list.

**Direction check:** this workflow is for references you collect on a candidate you might hire. If an outside organization is asking *you* for a reference on someone you know, use a separate "give a reference" workflow instead.

## Quick version

Light path: paste the candidate's CV (or a short summary of it), the role, and the referee's name and role. Ask for the briefing page. No connected tools are needed.

- The assistant writes a short context section: who the referee is and how they worked with the candidate.
- It drafts a tailored opening you can read out in under a minute.
- It writes briefing notes: what this referee can uniquely confirm, and any themes from earlier references to test.
- It gives one list of core questions plus three or four probes for the role.
- After the call, paste your rough notes back and ask it to separate what the referee saw from what they concluded.

**The page is the deliverable.** Do not stop after research or reply with a chat summary. The hiring manager will read the page, not the conversation. Everything useful must be on the page.

## Privacy and authorization

Reference checks involve personal information about two people: the candidate and the referee. Research only when you are authorized for a legitimate hiring purpose, the candidate has supplied or agreed to this referee, and the user has connected the sources you search. Use the minimum relevant information: role, organization, working relationship, and work history that bears on the job, and leave out personal life, health, family, protected characteristics, and anything unrelated to performance. Keep the page within the hiring team, and record or transcribe the call only if your policy allows it and the referee agrees at the start.

## Inputs

| Input | Source if not provided | Notes |
|---|---|---|
| Candidate name | Required from user | The person being hired |
| Referee name and contact | Calendar invite, candidate's reference list email | The person being called |
| Role | Hiring emails, notes, or applicant tracking system | Needed for role-specific probes |
| Call date | Calendar event; otherwise today | Date only is fine |
| Hiring manager name and organization | User profile or user's choice | Used in the opening and page attendees |

## Steps

When tools are connected, run every step in order. Otherwise, use the Quick version with what the user pastes in.

### Step 1: Find the scheduled call

- Search the user's calendar for events with the referee's name or contact.
- Extract the title, time, attendees, video link, and any scheduling notes.
- If there is no event yet, note that and continue.

### Step 2: Gather context

**2a. Hiring context.** Search the user's email and notes for the candidate's name to learn:

- The role they applied for.
- Their current stage (interview, work trial, final round).
- How the referee was introduced. The candidate's reference list message is usually the key source.
- The referee's relationship to the candidate (manager, client, peer, direct report, teacher).

**2b. Research the referee.** Run these searches in parallel, within authorized sources:

1. Email: direct correspondence with the referee's address.
2. Email: the referee's full name, to catch introductions and reference threads.
3. Team chat: the referee's name and their organization's name.
4. Notes or meetings database: the referee's name, including prior meetings.
5. Calendar: past events with the referee.
6. Public web: "{Name}" plus their organization, for current role and professional background only.

From each email search, read only the few recent messages that concern the candidate, the reference, or the scheduling of this call.

**2c. Candidate links.** Collect links the hiring manager will want during the call: the applicant tracking profile, a professional profile, and any portfolio, code repository, or personal site the candidate shared in their application.

**2d. Completed references.** Search the meetings database for other reference pages on the same candidate. Read them and pull out themes, strengths, concerns, and development areas. These become specific angles to confirm or challenge in this call.

**2e. Compile findings.** Organize what you found into:

- **Who the referee is:** role, organization, short professional background.
- **Relationship:** how, in what capacity, and for how long they worked with the candidate, and how closely they saw the relevant work.
- **Hiring context:** role, stage, and next step such as work trial dates.
- **Candidate links.**
- **Other references:** who else is on the candidate's list.
- **Briefing notes:** the analysis described below.

### Step 3: Create the call page

Create a page in the user's meetings database or chosen notes tool, with properties and content together.

- **Title:** `{Date} {Referee Name} ({Candidate Name} reference)`
- **Date:** call date, date only.
- **Attendees:** the hiring manager, plus any other interviewer joining.
- **Optional:** a meeting-notes or transcription block at the top, if allowed. Include only the meeting title in it. Let the tool fill in summary and transcript during or after the call.

Use this template and tailor every placeholder:

```markdown
## Context
- [{Referee Name}]({professional profile link}): {role, organization, one-line background}.
- {Candidate} worked with {Referee} as {relationship, capacity, duration}.
- This is a reference call for [{Candidate Name}]({profile link}) ([applicant profile]({link}), {other links}), who is at {stage} for {Role} at {Organization}. Next step: {e.g., work trial dates and location}.
- {Any prior contact or relationship history with the referee.}
- {Candidate}'s other references: {list}.

## Opening
> Hi {Referee}, thanks so much for making the time. I'm {Hiring Manager}, {their role} at {Organization}. {One sentence on what the organization does.} {Candidate} has applied for our {Role} role, and we're excited about their background. We're doing reference checks now so we can decide quickly. What you share stays within our hiring team. {If recording: Is it OK if I record so I can take accurate notes?}

## Briefing notes
- **Themes from completed references:** {who said what, and what to test now}
- **What this referee is uniquely placed to speak to:** {…}
- **Organization and relationship context:** {…}
- **Anything else:** {open questions, concerns, gaps}

## Questions
- **How did you work together?** What was {first name}'s role, and what was yours? How closely did you work day to day?
- **What did they concretely deliver, and how did it compare to your expectations?**
- **What is their standout strength?**
- **If they joined us and it didn't work out after three months, what would be the most likely reason?**
- **If things are going well at three months, what development area would I most likely make their top priority?**
- **Compared to everyone you've worked with in similar roles, where do they rank?**
- **If I were their manager, what could I do to help them do their best work for our mission?**
- **What should I have asked that I didn't?**

### {Role}-specific probes to weave in
- {Probe 1}
- {Probe 2}
- {Probe 3}
- {Probe 4}
```

## Writing the briefing notes

This is the highest-value section. It turns research into actions for this specific call.

- **Use direct language.** Write "The first referee said Jordan sometimes over-commits to side requests. Ask how this referee saw Jordan handle a crowded week." Do not write "It may be worth exploring...".
- **Attribute themes internally, test them neutrally on the call.** The page may say who raised a point. On the call, ask an open question such as "How did they decide what to drop when too much was on their plate?" Do not reveal what other referees or interviewers said, and do not lead the referee toward a conclusion.
- **Name the unique angle.** A former manager can speak to reliability and how much support the candidate needed. A peer can speak to collaboration. A client can speak to communication and delivery under pressure.
- **Flag organization links** the hiring manager should know about, such as past collaborations or shared channels.
- **If this is the first reference,** say so. List what to listen for that will be useful to compare across later calls.

## Role-specific probes

Pick probes that test capabilities the role actually needs. Write three or four. Examples:

- **Data analyst:** How do they check their own numbers before sharing them? How do they explain a messy result to someone without a data background? Do they push back when a question is badly framed?
- **Customer support lead:** How do they stay calm with an angry customer? Have they turned repeat complaints into a fix rather than a workaround? How do they coach newer teammates?
- **Engineering manager:** How do they handle an underperforming report? What do they do when the roadmap and the team's capacity disagree? How much do they still write code, and is that the right amount?

## Worked example (invented)

Inputs pasted into a plain chat: Jordan Lee's CV, applying for Data Analyst; referee Sam Ortiz, Jordan's manager for two years at a regional grocery chain. One earlier reference, from a peer, praised Jordan's clear dashboards but said Jordan sometimes says yes to too many side requests.

Briefing notes the assistant writes:

- **Theme to test:** the peer said Jordan over-commits. Sam managed Jordan's workload directly, so ask how Jordan handled a crowded week, without mentioning the peer.
- **Sam is uniquely placed to speak to:** how much support Jordan needed, and whether Jordan's analysis changed real decisions.
- **Probe:** "Tell me about a time Jordan's numbers turned out wrong. What happened next?"

## During and after the call

- Follow vague praise with "What did that look like?" or "Can you give an example?"
- Weight evidence by how directly the referee observed the work, not by their title or confidence.
- Afterward, record notes on the same page. Separate what the referee observed, how the referee interpreted it, and your own inference. Note confidence and limits on what they could know.
- Treat one reference as one input. Compare across references and other hiring evidence before deciding.

## Style and quality checks

- Context is short bullet points, not paragraphs.
- The opening is tailored to this referee and candidate. Adjust the tone if there is prior contact.
- Questions sit in one bulleted list, not numbered, with no separate agendas.
- Candidate links and other references are on the page.
- Probes match the real role, not a generic list.
- No unrelated personal details about the candidate or referee appear on the page.
- The page exists in the chosen system before you report the task complete.


---
name: access-check
description: Before someone joins a shared chat workspace or knowledge base, find content about them they could read and recommend what to restrict. Use when adding a new hire, advisor, or collaborator.
---

# Check before granting access

Use this workflow before adding a new hire, advisor, contractor or collaborator to a shared chat workspace, a knowledge base, or both. It answers one question: **once they join, could they read anything about themselves that should not be visible to them?** It finds those items and recommends what to restrict, move or redact before access is granted.

Typical requests: "check before I add [person]" or "is there anything about [person] I should hide first?"

## Purpose and boundaries

- **Authorization.** Run this only for someone who can manage access to these systems, such as a workspace admin or the person's sponsor. Search only the systems the person is about to join.
- **Narrow scope.** Look only for content that mentions the incoming person directly. Ignore other sensitive material, however interesting, unless it is about them. Do not collect or summarize unrelated conversations.
- **Minimum detail.** Quote only the line needed to judge a finding. For health, family or other personal-life details, name the category (for example "mentions a family matter") instead of repeating the detail.
- **Access boundary.** Send the report only to the requester. Do not post it in shared spaces.
- **Not a cover-up tool.** Prefer restricting access over deleting. Do not delete or alter records that fall under a retention duty, a legal hold, or the person's legal right to access data about them. If unsure, flag it and let the requester check with the right owner.

## Inputs to collect

| Input | Why it matters |
|---|---|
| Full name, nicknames, likely misspellings | Catches mentions that exact-name search misses |
| Chat user ID or handle, if they already have one | Catches tagged mentions |
| A disambiguator, such as current or past employers | Rules out people with the same name |
| Which private channels and restricted spaces they will join | Defines what they can actually see |

If the requester says "standard team-member access", assume every public channel and every open knowledge-base space, with no private channels.

## Step 1: Identify the person

1. Look up the person in the user directory of each system.
2. Many first names are shared. Keep the disambiguator handy and drop namesakes as you go.
3. List the spelling variants you will search (for example a surname with swapped vowels or a missing letter).

## Step 2: Map what they will and will not see

This decides what counts as exposed. Skip what they cannot see, but say what you skipped.

- **Usually not visible:** direct messages and group messages they are not in; private channels they will not join; the requester's personal or private spaces (if the requester excludes them); pages in another user's private section.
- **Usually visible:** public channels; private channels they will join; every page in shared spaces and shared databases, including meeting notes, hiring, strategy, projects and archives.

Rules for unclear cases:

- **Search tools often cannot see page-level permissions.** A page may be restricted while still sitting in a shared database, and search returns it anyway. Treat every page in a shared space as visible unless the requester confirms it is restricted. Then move it to the skipped list as "restricted, confirmed by requester".
- **Pages with no parent location** (for example auto-generated meeting notes) are often private to their creator. Treat them as not visible unless they show explicit sharing or the requester says otherwise.
- **System-generated user profile pages** usually carry no content. Skip them. An access error on them is expected and not worth reporting.

## Step 3: Search the chat workspace

Run these searches in parallel, covering every channel you are allowed to search:

- Full name, surname alone, and each misspelling, newest first. Page through results until they stop being about the person.
- First name alone, to catch casual mentions. Skim for context and drop namesakes.
- Their user ID as a keyword, to catch tagged mentions.
- Any announcement about adding them. Read the full thread, since colleagues may have replied with concerns.

For each relevant hit, record the channel type and a permanent link. Read the full thread around any hit that has replies. Direct messages are not visible to the person, but list them with links in the skipped section so the requester knows they were seen.

## Step 4: Search the knowledge base

1. Search the full name, each misspelling, and the name combined with their main employers or role. Ask for a large page of results.
2. If the requester's private space is excluded, run the same search limited to that space. Hits that appear only there are out of scope.
3. Open every remaining hit that mentions the person beyond a passing name-drop. Read the full text and check its location.
4. Check structured properties as well as body text: hiring status fields, pipeline stages, contact-relationship fields, and similar.
5. If a page fails to open, report it with its link and ask the requester to check it by hand.

## Step 5: Judge each mention

Flag a mention when the person would plausibly feel hurt, misled or awkward reading it, or when it reveals plans about them that they do not know about.

**Flag:**

- Candid assessments: doubts about their skills, commitment or results.
- Hiring, offer, compensation or persuasion strategy aimed at them, including records marking them as a lost or declined candidate.
- Other people's plans for them that they may not know about.
- Reference feedback, gossip, or health, family or personal-life details.
- Colleagues' doubts about what they contribute.

**Do not flag:**

- Neutral mentions: event replies, being tagged on a link, a field recording who introduced them.
- Praise and accurate bios.
- Their own advice recorded in meeting notes. **Exception:** if those notes include their candid remarks about third parties, mention this once. They may not expect those remarks to sit in a team-wide space.

Rate every finding with a word and a symbol, never colour alone:

| Rating | Meaning |
|---|---|
| **▲ Hide** | Restrict, move or redact before they join |
| **◆ Consider** | Mild; the requester decides |
| **○ Fine** | Checked and harmless; listed briefly for completeness |

## Step 6: Report

Lead with the answer: the number of ▲ and ◆ items, and whether anything blocks granting access today. Then list one item per finding:

- Bold rating, then the page or message label as a short hyperlink (for example `[#announcements, 4 Oct](link)`), never a bare URL
- Where it lives, and whether the person would see it
- The exact line that matters (or the category, for sensitive personal details)
- Recommended fix: restrict the page, move it to a private space, or redact one line

Every item gets its own working link, including **○ Fine** items and skipped direct messages. The requester will check each one, so an item without a link is not useful. Close with failed fetches and the list of what was skipped as not visible.

## Making changes

Do not change permissions, move pages or edit content without explicit approval. Moving or redacting someone else's page is a material change, so confirm with its owner where appropriate. After approval, make the edits, then re-run the searches to confirm nothing visible remains.

## Common failure modes

- Searching only the exact name and missing misspellings, nicknames or tagged IDs.
- Confusing a namesake with the person.
- Assuming a page is private because search cannot show its permissions.
- Reading only the first message and missing a critical reply in the thread.
- Missing sensitive content stored in page properties rather than body text.
- Drifting into unrelated sensitive material outside the scope.
- Acting on findings before approval.


---
name: use-a-browser-safely
description: Complete browser tasks safely: pick the least invasive route, protect logged-in accounts, check what the page actually shows, and confirm before acting. Use when filling forms or fixing dashboards in a browser.
---

# Use a browser safely

Use this workflow when a task has to happen in a web browser. Typical tasks include filling a rendered form, changing a setting in a dashboard, collecting information from a page that only renders with scripts, testing a user flow, or working inside a signed-in session the user has authorized.

The central rule:

> Inspect the page before you edit anything. Read back every field you change. Do not click the final button until verification passes and the account, target, and authorization are clear.

A successful automation call does not prove the website accepted the change. A fill command usually reports success as long as it did not throw an error. It does not check that the application's internal state updated, that moving focus away committed the value, or that the field kept the content. **The caller verifies. Always.**

## 1. Choose the least invasive route

Use the first route that fits. Do not skip ahead.

1. **Direct interface first.** Look for a documented API, export, integration, or plain form endpoint before opening any browser.
2. **Isolated headless browser.** This is the default for anything that does not need the user's identity: public forms, extraction from dynamic pages, UI testing, and screenshots. It never opens a visible window and never touches the user's own browser.
3. **The user's signed-in visible browser.** Use this only when the task truly needs the user's live session, such as an account dashboard or single sign-on state.

### Look for a direct interface

Many forms send structured data to an endpoint that can be called directly, which skips the hardest browser problems. To find one:

- Read the service's official documentation for an API.
- View the page source for a form action or embedded data block.
- Watch the browser's network requests while using the page normally.

Even an endpoint that takes some study to understand is often faster than fighting a complex form. Fall back to the browser when no suitable programmatic option exists or when the user explicitly wants the UI flow.

Limits:

- Do not use undocumented endpoints to get around access controls, terms of service, rate limits, or anti-abuse systems.
- In a signed-in session, do not call an application's internal endpoints from page scripts. Requests that skip the headers or tokens the app normally sends can end the user's session or trigger security responses. Drive the UI instead, or use a supported API with proper credentials.

### Do not use the visible browser for convenience

The user's visible browser is their working space. Taking it over interrupts them and adds privacy and account risk. Extraction, bulk form fills, and anything that works headless should stay headless.

### Blocks and bot checks

If a site blocks headless automation during general research, accept the block and move on. Do not try to evade it. Escalating to the user's signed-in browser is reasonable only when the user explicitly asked for a task on that specific site and the session is genuinely needed. Human-verification checks, security-key prompts, and multi-factor prompts belong to the user: pause, ask them to complete it, then continue. Never simulate, bypass, or weaken these checks.

## 2. Pick the right automation style

Two common styles exist:

- **Step-by-step tool calls** through an interactive browser tool. Good for one click, reading one snapshot, or short tasks with roughly ten or fewer actions and little text.
- **A standalone script** using a browser automation library. Better for long text (for example over a couple of thousand characters), many fields, heavy single-page applications, or anything that needs repeatable runs.

Interactive tool layers can become unstable with long text, several parallel actions against one page, or heavy rendering. If the session crashes with a message like "page, context, or browser has been closed," switch to a script. Do not try to rescue the broken session. When in doubt, write a script.

Script hygiene:

- Save scripts and artifacts in a temporary working folder the user has agreed to.
- Launch standalone automation headless unless a visible session is part of the plan.
- Pass secrets through environment variables or a secrets store. Never hard-code credentials, and never print them in logs.

## 3. Protect identity, privacy, and the user's browser

When the task touches private messages, records, dashboards, or information about other people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant pages and data. Keep unrelated personal details out of screenshots, logs, and reports. Share results only within the requester's appropriate access boundary.

### Rules for the user's visible browser

- **Announce, then act.** Say briefly what you are taking over and why, for example "Taking over the browser to update the billing contact." Never take control silently. If the user has already authorized visible browser use for this task, do not ask again for the same approval.
- **Work in a fresh window, tab, or tab group.** Do not reuse the user's existing tabs unless they point to one.
- **Classify the context before choosing a profile.** Decide whether the task is personal, work, test, staging, or production. Personal errands (shopping, banking, health, subscriptions, household, government services) are personal even on general-purpose sites. Internal operations, vendors, and colleague-facing work are work. If the user says which, that settles it.
- **Select the profile directly.** Many tools offer a generic "current browser" selector that picks whichever profile was used most recently. That can silently put a personal task in a work account. Select the specific profile or session that matches the context.
- **Do not trust display names.** Labels like "Browser 1" can reshuffle after restarts, and nicknames may not propagate. Use a stable identifier where the tool provides one, and record the mapping in a private local note if useful. Even then, verify every time.
- **A window is not a connection.** Opening a window for a profile puts it on screen. The automation connection may still point elsewhere. Confirm the connection, not only the window.
- **Do not restart or force-quit the user's browser** without their explicit OK. It closes everything they have open.

### Account preflight gate

Before any action that changes data, answer three questions:

1. **Which account is this?** Open a fresh tab to a reliable account page and read the signed-in identity.
2. **Which environment is this?** Production, staging, test, or a specific organization or workspace.
3. **What exact item will change?** The specific record, form, or setting.

If any answer is unclear, stop and ask. If your environment uses a permission gate or verification marker that unlocks write actions, set it only after the account check has actually passed, and record the evidence. Never set it to get past the gate.

## 4. Set the task boundary and authorization

Before navigating deeply, identify:

- The target page, record, form, or setting.
- What will be entered, collected, changed, uploaded, or sent.
- The minimum information needed.
- Fields that need the user's judgment.
- Whether the final action can be undone.

**Reversible changes** the user asked for, such as toggling a setting or updating a saved card or draft, can proceed after normal verification.

**Irreversible or high-impact actions** need a pre-action record and confirmation unless the user already gave clear authorization for that exact action. These include payments, purchases, sends, invitations, publishing, deletions, plan or billing changes, access or ownership changes, and anything labeled "cannot be undone" or "cannot be edited after submission." Treat such forms as one-way doors.

Honor an explicit request to review before submission. If authorization is already given, do not ask again. If it is missing, prepare and verify the full result, show the pre-submit state, and ask only for the final action.

## 5. Inspect the page before editing

Before writing any fill logic, list every relevant control. A few minutes here saves long debugging sessions.

For each control, record:

- Element kind: single-line input, multi-line text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Label, accessible name, or label relationship.
- Required state and current value or value length.
- Whether it is the real editor, a wrapper, or a hidden sync field.
- Whether changing it re-renders the form.

```text
// Pseudocode: adapt to the chosen automation library
controls = page.findAll('input, textarea, [contenteditable], [role=textbox]')
for each c in controls:
  record { tag, type, role,
           label: accessibleLabel(c),
           required: c.required or c.ariaRequired,
           length: readValue(c).length }
save record list to 'form-before.json'
```

Things to watch for:

- **Look-alike controls.** Forms often use different control kinds for similar-looking fields. A single-line input silently strips line breaks. A text area usually accepts everything. Rich-text editors keep their own internal model and may ignore direct value changes.
- **Hidden sync fields.** Some editors pair a visible editable area with a hidden input that looks fillable. Filling the hidden input passes a raw DOM check, but the form then reports the field as empty, because the app reads the visible editor. Always fill the control the app actually reads.
- **Empty wrappers.** An accessibility locator can return a wrapper with no editable content inside. Find the real editable element through its label relationship (for example the element named by its labelled-by attribute), then tag it with a temporary marker attribute so you can target it reliably.
- **Unstable order.** Field order can change between loads. Never address fields by position. Use label text or label relationships.
- **Current state.** Before changing an existing record or setting, read its current value so you do not overwrite the wrong thing.

## 6. Use the right interaction for each control

| Control | Preferred interaction | Watch for |
|---|---|---|
| Single-line input | Normal fill | Line breaks removed silently; length limits. |
| Multi-line text area | Fill, then move focus to the page body | Some apps commit only on blur. |
| Rich-text or content-editable editor | Click it, select all, delete, insert text with keyboard-style input, then blur | Direct DOM writes or value setters may be ignored by the app's model. |
| Dropdown or combobox | Open it, choose by exact visible option text, wait for it to settle | Selection can re-render the whole form. |
| Checkbox or radio | Read the state first; click only if it needs to change | Clicking toggles an already-correct value. |
| Date or time picker | Set values, close by clicking neutral page background, check the rendered summary | Close or clear buttons may wipe values; typing while open can rewrite dates. |
| File upload | Confirm file, destination, and privacy first | Upload may start at once and be hard to undo. |

Robust sequence for framework-driven editors:

1. Click the real editable element.
2. Select all existing content and delete it.
3. Insert the new text with keyboard-style text input.
4. Move focus to a neutral element, such as the page body, to commit.
5. Wait briefly for state to settle.
6. Read the value back.

**Blur after every rich-text field.** Without it, the next edit can trigger a re-render that rebuilds earlier editors from a model that never received their text, and only the last field survives.

**Order matters.** Do dropdowns, checkboxes, tabs, and other re-rendering choices first, then fill text. Re-inspect after each such choice. For tricky widgets like date pickers, set them early and re-check them after every later edit.

**Clipboard and paste.** Headless browsers often lack clipboard permission, so embed values directly rather than relying on the clipboard. When rich content (such as HTML with links) must be inserted, a synthetic paste event carrying both HTML and plain text works in some editors and is ignored by others. Some editors expose their own documented conversion method instead. Try the supported method for that editor and always verify the result, ideally through the service's API or an export rather than the screen alone.

**Drag and drop.** Dragging can create layout changes (like columns) or trigger a clickable element by accident. Prefer keyboard-based move commands with short waits, then verify the final structure.

**Send buttons and selectors drift.** Before clicking a send or submit control found by selector, read the composed content back to confirm it landed in the right place. Selectors that worked before can stop matching after a site update.

## 7. Verify after every fill

After each change, read the value back and compare it with what you intended. For sensitive content, compare lengths or a short redacted summary rather than printing full text.

```text
result = fillField(field, value)
if result.length != value.length:
  log 'mismatch on ' + field.label + ': ' + result.length + '/' + value.length
  retry once with a different method (for example keyboard input instead of a setter)
  verify again; if still wrong, stop and report
```

How to read common mismatches:

- **Empty after a reported success:** the app ignored a direct value change. Use focus-and-keyboard input, then blur.
- **Short by a few characters, roughly one per paragraph:** a single-line input dropped line breaks. Rewrite as one paragraph, or find the multi-line field.
- **Short after collapsing blank lines or repeated spaces:** some editors normalize whitespace. Usually acceptable; if not, simplify the formatting yourself and note it.
- **Earlier field now blank:** a re-render reset uncommitted state. Blur each field and do re-rendering choices first.

If verification still fails after one retry, do not move toward submission. Report the problem and ask how to proceed.

## 8. Two-phase run and pre-submit gate

Run consequential tasks in two phases.

**Phase 1: prepare.** Fill everything, verify each field, save a structured after-state record, and capture a full-page screenshot. Do not submit.

**Phase 2: commit.** If the task or a standing instruction already authorizes the final action, continue. Otherwise show the prepared state and get the missing authorization. Then re-fill if needed, re-run the gate below, and click the final control once.

A script can implement this with a flag such as `--submit` that is off by default.

```text
open headless browser and new page
go to target URL; dismiss banners; sign in if needed
inspect controls -> save 'form-before.json'
apply re-rendering choices first, then fill text fields with verification
inspect again -> save 'form-after.json'; save full-page screenshot
if submit flag is set:
  run pre-submit gate; refuse and exit if it fails
  click the exact final button by its visible name
  wait, then save a post-submit screenshot and check for confirmation
close browser
```

### Pre-submit readiness gate

Re-inspect the full page state. Submit only if all are true:

- [ ] Correct account, organization, and environment.
- [ ] Correct target item.
- [ ] Every required field is non-empty.
- [ ] Each value matches the intended content closely enough.
- [ ] Dropdowns, checkboxes, dates, recipients, and attachments are correct.
- [ ] No validation errors, warnings, or unsaved-change notices remain.
- [ ] The button about to be clicked does what you expect and is not a similar-looking destructive option.

**If any required field is empty, do not submit.** This is not negotiable. A partly filled form can be fixed; a wrong submission often cannot.

A confirmation request for an irreversible action should state the target, key values, recipients or audience, any cost, what cannot be undone, and any open questions.

## 9. Confirm completion

A click is not proof of success. Look for real evidence: a success message, a confirmation reference, a new record, a setting that persists after a safe reload, or a sent or published item.

- **Errors can be cosmetic.** Some apps show "something went wrong" after the work actually finished. Inspect the result before retrying, because blind retries can create duplicate messages, payments, or records.
- **Frozen pages.** A blocking pop-up dialog can freeze the tab so clicks and screenshots time out. Ask the user to respond to it, then continue. Where possible, confirm the outcome through an independent channel (for example a public lookup or an API read) instead of the frozen UI.
- If you cannot confirm completion, say what you tried, what evidence exists, and what remains uncertain. Never report an attempt as a success.

## 10. Parallel work and background tabs

When many independent items are needed (for example several generated drafts or images), separate tabs or sessions each given the full brief avoid one item biasing the next. Keep concurrency modest, around ten at once; more tends to stall or fail. Background tabs may not render content at full size, so bring an item into view before capturing it and check that nothing is cut off. Clean up any temporary overlays or tabs afterward.

## 11. General failure patterns

| Symptom | Likely cause | Safe response |
|---|---|---|
| Fill reports success but the field is blank | App model ignored a direct write | Keyboard-style input, blur, read back. |
| Earlier fields blank out as later ones are filled | Re-render rebuilt editors from stale state | Blur after each fill; do re-rendering choices first. |
| A choice in a dropdown wipes the form | Selection triggers a full re-render | Make choices before filling text; re-verify. |
| Field looks filled but validation says empty | Hidden sync field was edited | Fill the visible editor the app reads. |
| Locator returns an empty wrapper | Accessible name sits on a different element | Follow the label relationship to the real editor. |
| Interactive tool crashes on long text or parallel calls | Tool layer is unstable for heavy work | Switch to a standalone script. |
| Headless page differs from a normal browser | Site varies by browser context | Prefer a direct interface; escalate only for an explicit task, never evade protections. |
| Wrong account or profile opened | Generic selector picked the last-used profile | Classify context, select the profile directly, verify the account. |
| Session ends after a page-script request | Internal endpoint called without the app's normal headers | Drive the UI or use a supported API. |
| Automation connection fails an integrity or signature check | Local helper is stale or altered | Stop; repair through an approved path that keeps verification on. Never disable checks. |
| Security check or 2FA prompt appears | Site needs the user present | Ask the user to complete it, then continue. |

## 12. Report results

Keep reports short. Summarize the outcome in one or two sentences, point to the screenshot and the after-state record, and offer to open the screenshot for the user. Do not paste every field value as a large inline table; the user can open the record if they want the full text. Store artifacts only where the user can appropriately access them, and delete temporary files that contain sensitive content when they are no longer needed.

## 13. Keep the procedure current

When a run reveals a reusable lesson, such as a new failure mode, a working pattern, or a missing capability, add it to your local copy of this procedure. Prefer a single table row with symptom, cause, and fix over new prose. Never record credentials, account identifiers, personal details, or private site data. Keep the document bounded: when it grows long, merge older entries into general principles instead of appending incident history. Tool paths, versions, and profile mappings go stale, so update them in place and re-verify them in the current environment.

## Final audit checklist

- [ ] The least invasive suitable route was used.
- [ ] Purpose and authorization were clear; only minimum relevant data was accessed.
- [ ] Visible-browser use was announced and kept to a fresh window or tab.
- [ ] Account, environment, and target were verified before any write.
- [ ] Controls were inspected before editing and addressed by label, not position.
- [ ] Every meaningful change was read back.
- [ ] The pre-submit gate passed, with no empty required fields.
- [ ] Irreversible actions had a pre-action record and authorization.
- [ ] Success was confirmed with evidence after acting.
- [ ] The report separates confirmed results from uncertainty and exposes no secrets or unneeded personal data.


---
name: create-a-skill
description: Design, test, and improve a reusable AI skill, from a rough idea or a repeated workflow to a tested, well-triggered skill. Use when someone wants to turn a workflow into a skill or improve one.
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


---
name: test-every-screen-size
description: Check every UI or CSS change across narrow, wide, short, and tall screens with screenshots and layout checks before calling it done. Use before shipping any front-end change.
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
name: recurring-events
description: Publish the next date of a recurring community event, refresh its image and copy, and invite people who opted in. Use when someone says set up this week's event or post the next one.
---

# Run a recurring community event

Use this when you host a regular event, such as a monthly book swap or game night, and want the assistant to set up the next one: date, fresh poster, event page, and invites, with as few questions as possible.

## Quick version

- Tell the assistant the series name, the rule for when it happens (for example "first Thursday of each month"), and the last event number.
- Ask it to work out the next date with a real calendar, not in its head.
- Have it reuse last time's description and update only what changed.
- Ask for one fresh poster idea that is clearly different from the last few.
- Paste the finished text into your event page yourself, check it as a guest would, then invite the usual people.

## Authorization: confirm once, then act

For your own series, standing authorization is the natural default. Confirm it once, in writing, with the series, the usual hosts, who gets invited, and what the assistant may publish and send. After that, each new occurrence should need zero questions. Stop and ask only when something real changes: a new venue, a price, a bigger or different audience, a public listing, or a safety issue. Invite only people who agreed to hear about future events in the series, such as past guests who have not opted out, and make opting out easy.

## 1. Work out the date and number

- Compute the next date from the recurrence rule with a calendar or date tool. Weekday and date errors are the most common mistake.
- Find the highest existing event number and add one.
- Check for clashes: a holiday, the venue being closed, or the host being away. A clash does not cancel the event by itself. Go ahead under the standing policy and name the clash in the final report so the host can hand off or cancel.
- For several events, use consecutive dates and numbers, each with its own poster.

## 2. Make a fresh poster

Look at the last two or three posters first so you do not repeat them. Keep the series identity steady (the name in the same hand-lettered style, the core activity, a warm and simple look) and change the big idea each time.

Levers worth pulling:

- **Season, weather, light:** first frost, a rainy window, long summer evening light.
- **Viewpoint:** looking up past a teacup, a bird's-eye view of the table, a view from inside a bookshelf.
- **One witty focal object:** a chess knight wearing a party hat, a stack of paperbacks shaped like a lighthouse, a dice cup used as a flowerpot.
- **Local texture:** a familiar street corner, the venue's door, a local landmark.

One clear joke beats a busy scene.

Anti-cliché guardrails to put in the prompt:

- one clear subject and a restrained palette;
- clean, correctly spelled lettering;
- no extra fingers, melted objects, or garbled text;
- no glossy over-rendered finish or generic "epic" lighting.

If the result looks like last time or has obvious generated tells, say so and regenerate once or twice.

**Composer trap:** write the image prompt as one paragraph with no line breaks. In many chat tools, pressing Enter sends the message, so a multi-line prompt gets cut off after the first line. If that happens, stop the generation and send the rest as a follow-up.

Image tools sometimes show an error even though the image finished, so check for a new image before retrying.

## 3. Build the event page

Reuse the stable parts of the last description and update the rest. Fill fields in this order, because date pickers are often fragile:

1. Title, using the series pattern, such as "Book Swap #N".
2. Date, start and end time. Check the shown date before touching anything else.
3. Location, picking the exact venue, not a similar name.
4. Description.
5. Image. Wait for the upload to finish and check it shows.
6. Co-hosts, if any.
7. Leave visibility, cost, and capacity at the series defaults.

Some platforms publish on a button labeled "Save" or "Done," so know what it does before pressing it. Then check the live page as a guest would.

## 4. Invite the approved audience

Invite past guests of the series, one past event at a time. Include early unnumbered events when inviting past guests. Before pressing "Select all," check whether people are already selected, because pressing it again can clear them. Watch the invite count rise after each group. If it stays flat or drops, stop and look. Send, then confirm the sent state and final count.

## 5. Report

Keep it short: what was created, date and venue, the invite count, any clash from step 1, and the live link as the last line.

## Worked example (invented)

Series: "Second Saturday Board Games," monthly, at a neighborhood café, hosts Priya and Tom, invite list is past guests who have not opted out.

- Last event was #11 in March. A calendar check gives Saturday 12 April, so this is #12.
- The café closes early that day. Under the standing policy the assistant keeps the usual slot and flags the clash.
- Last two posters were a meeple on a mountain and a rainy window with cards. This time: a bird's-eye view of a game board laid out like a city park, with a single tiny meeple walking a dog. Warm colors, hand-lettered title, nothing else in frame.
- Description carries over unchanged except the date and a new line: "Bring a game you have not played in a year."
- Invites: 11 past sessions, count rises from 0 to 46 with no drops. Sent.

Report: "Board Games #12 is live for Sat 12 April at the café. 46 people invited. Note: the café may close early that day, so you may want to confirm the time with them." Link on the final line.

## After each run

Keep only reusable lessons, such as platform quirks or a changed template. Never store guest details or quietly widen who gets invited.

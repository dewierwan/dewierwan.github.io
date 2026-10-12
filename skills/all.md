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
name: decide
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
description: Shape a consequential document through evidence review, answer-dependent question rounds, an alignment ledger, a readiness gate, plain drafting, and a final audit.
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
description: Search only the sources that matter, at a depth that fits the stakes, and turn the findings into one concise context brief where every claim links to its evidence.
---

# Gather context

Build a well-sourced context brief on whatever the user names: a person, organization, project, topic, or decision. Search the sources that plausibly hold relevant information, then combine the findings into one organized brief in which every sourced claim links to its evidence.

Use this workflow when the user wants context before they act: before writing, deciding, meeting, pitching, or hiring, or simply to get up to speed. Typical requests include "gather context on X", "what do we have on X", "get me up to speed on X", and "background on X before my call".

If the user wants a structured meeting-preparation document and has a separate workflow for that, use it instead. This workflow is for raw context assembly. If you are unsure which one they want, ask.

## The most important rule: right-size the effort

Match the depth of the search to what the user actually needs. "Remind me where we are with X" needs a quick look at two or three obvious sources and a short answer. A deep dive before a high-stakes decision needs a broad search with verification. Most requests fall in between. Decide how much effort is warranted, and do that much.

Two failure modes are equally bad:

- **Over-gathering:** querying every connected system, starting many parallel helpers, and writing an essay for a quick question.
- **Under-gathering:** checking one source, finding a few results, and stopping when the request clearly needed more. The key fact is often in a chat thread or meeting record the user has forgotten.

For each source, ask: *for this specific request, would a sensible researcher think it is worth checking here?* Relevance and effort level together set the breadth. Skipping an irrelevant source is good judgment, not laziness.

## Step 0: Set the purpose and access boundary

State, at least to yourself, the decision or task the brief supports. Search private sources only when the user is authorized to access them and the source is relevant to that purpose. Having access is not, by itself, a reason to search.

When the subject is a person, apply stricter limits:

- Use the minimum sources and information needed for the stated task.
- Do not search private messages or records just because they are available.
- Leave out unrelated or sensitive personal details. Do not guess at private or protected traits.
- Respect consent, confidentiality, need-to-know limits, and the person's reasonable privacy expectations.
- Keep the brief in a location whose access matches the sensitivity of the sources and the intended audience.
- For hiring-related subjects, focus on role-relevant capabilities, alignment with the role's requirements, and evidence that actually reflects relevant performance.

If the purpose, authorization, or output destination is unclear, resolve it before searching private sources.

## Step 1: Scope the gather

### Pick an effort level

| Tier | When | How to search | Output |
|---|---|---|---|
| Quick | Status check, "remind me" | 1–3 obvious sources, one pass each, searched directly | A few lines |
| Standard | The common case | A handful of relevant sources, a couple of queries each; parallel helpers only if they truly save time | A tight brief |
| Deep | High-stakes preparation, such as a major decision, big pitch, or key hire | Broad search, parallel helpers, several queries per source, verification of key claims | The full brief structure |

If unsure, choose the lighter tier and offer to go deeper. Escalating is cheap; over-searching is expensive. State the chosen tier in one line so the user can redirect, for example: "Quick look across email, chat, and the team wiki. Say the word if you want the full sweep."

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

If the subject is truly ambiguous, such as a bare name that could mean several people, ask **one** short clarifying question before searching. A wrong-target search wastes a lot of effort. If the subject is clear, go ahead.

### Named sources are a floor, not a ceiling

Sources the user names are mandatory, but they are not necessarily the full list. If another source clearly holds decision-relevant context, check it too. The most common case: when results show or the request implies a recent meeting with the subject, read the notes or transcript for that meeting. It is often the richest single source, and a brief without it misses what was actually said.

### Set the time window

Use the window the user gives. If they give none, pick one that fits the subject's age, such as the last several months for an active relationship, extending back to the start for older relationships or projects. State the window in the brief.

## Step 2: Search the relevant sources

- **Quick or standard:** search directly in the main conversation so you see results as they arrive.
- **Deep, or many sources:** run read-only searches in parallel, one helper per source or cluster. Each helper returns a short digest with links, not raw dumps.

Depth within a source also follows the tier. For a deep search, query several ways: by name, organization, project keyword, and related people. Do not conclude "nothing there" until you have used the search capabilities available. For a quick look, one or two well-chosen queries is correct.

### Source-handling principles

These apply whatever tools the user has. For lighter tiers, apply them to fewer sources and fewer results.

1. **Search direct and indirect.** Look for direct contact with the subject, and in deeper passes for mentions where others discuss it.
2. **Prefer precise search modes.** If a tool's default search returns noisy or loosely related results, switch to exact or keyword search.
3. **Read the whole item.** Some documents, pages, or records hide content in tabs, sections, attachments, or threads that a simple read skips. Open what matters in full and note where each finding came from.
4. **Know which records are authoritative.** For structured databases, use any map of canonical tables and field meanings before crawling. Treat lower-quality or temporary data as weak until confirmed, and watch for fields that hold default values rather than real ones.
5. **Check freshness.** Web profiles and news go stale; cross-check current roles against dated sources. Stored notes or assistant memory reflect what was true when written; confirm any named file, setting, or fact still holds.
6. **Read attribution carefully.** Speaker labels in transcripts and authorship in shared records can be imprecise. Do not attribute a statement to someone without reasonable confidence.
7. **Use conditional sources only when they fit.** Recruiting records for hiring matters, product analytics for usage questions, code history for engineering subjects, and the user's personal task or journal system only for work they did themselves and have chosen to include.
8. **Never invent a link.** Use only URLs you have verified or that the user supplied. Otherwise leave it out and flag it.

### Gaps and unavailable sources

**Do not silently substitute sources.** If a source you judged relevant returns nothing or is unavailable, say so in the brief. Do not cover the gap with an adjacent source.

If a source should be reachable but is not, try every safe diagnosis and repair you can first, such as checking the connection configuration or restarting a service you are allowed to manage. Ask the user only for steps that need them, such as re-authenticating. Report the exact failure, what you tried, and the one remaining action.

A source you deliberately skipped as irrelevant is not a gap, but never imply you checked it.

## Step 3: Synthesize into a context brief

Combine findings into one brief organized by theme, not by tool. Lead with what matters most for the user's next action. Resolve contradictions rather than listing both blindly, for example: "A news profile says they work at Organization A; their dated professional profile says they left in March. The profile is more recent and more likely correct."

**Every sourced claim gets a clickable link** to its primary source. A quote without a link is not finished.

### Output template

```markdown
## [Subject]: context brief
*Searched: [sources]. Window: [dates]. Effort: [quick/standard/deep].*

## TL;DR
3–5 bullets with the most decision-relevant facts.

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

Match length to depth and keep prose short. This is a document to scan and act on.

### Where the brief goes

- **Short brief:** give it directly in the reply.
- **Long or reference brief:** save it where the user keeps generated documents, at an access level that suits the content. Follow the user's naming convention; if none exists, use a date plus a concise, specific, human-readable headline rather than a filename-style slug. Reply with a compact summary of key findings and the link.

Make the brief (or summary plus link) the final part of the reply, and put any follow-up offer, such as "Want me to draft the outreach email?", before it. This keeps the deliverable easy to copy.

If you write into an existing formatted document, insert content where it will not inherit unintended styles, then verify the result by re-reading its structure or rendering it. A plain-text read does not confirm formatting.

## Readiness checklist

| Check | Pass condition |
|---|---|
| Purpose and access | Task stated; sources authorized and relevant; person-related data minimal |
| Effort | Tier matches the stakes and is stated in one line |
| Coverage | Named sources searched; obviously decision-relevant sources, especially recent meeting records, added |
| Evidence | Every sourced claim has a verified link; no invented URLs |
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
| Including unrelated personal details | Keep only what the stated task needs |


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
name: professional-posts
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
name: cover-images
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
description: Review the past week and shape the next one: commit to one to three checkable goals, protect capacity, triage tasks, trim meetings, and record a short plan.
---

# Plan your week

Use this workflow to review the week that is ending and shape the week ahead in one deliberate session of about an hour. It works with any goal tracker, task list, calendar, and notes system the user chooses.

The method has two halves. First, research sets the **constraints**: deadlines, meetings, backlog, energy, and capacity. Then a few interview rounds, each built on the previous answers, set **what matters**. Only then do you turn the result into goals, tasks, calendar blocks, and a short written plan.

The conversation does the hard work. The final plan should feel simple.

## When to use it

Use it when the user asks to plan their week, review and plan their week, or do their weekly session. Any request that combines reviewing the past week with planning the next one belongs here, not in a daily review.

By default, the target week starts next Monday. If the session runs on a Monday, the target is the current week. The user can name a different week. See "Adapting to timing" near the end.

## What the session must produce

The session is not complete until these exist:

1. **One to three weekly goals** in the user's goal tracker, each linked to a longer-term goal and carrying a definition of done of 2-4 checkable outputs.
2. **A short written plan** on the target week's record, plus the user's review answers saved on the week being reviewed.
3. **Tasks** created or updated for each concrete chunk of work behind each goal. Each takes 5 minutes to 3 hours, has a clear title, and has notes that make starting easy. The user approves each one.
4. **Calendar blocks** for goal work and protected commitments, each slot approved individually.
5. **Task decisions applied** for overdue tasks the user chose to triage.
6. **Drafted messages** for meetings the user chose to cut or move. The user sends them.

If the user declines a step ("I'll triage myself", "keep all meetings"), record that choice and treat the step as done.

## Setup: choices to confirm once

Ask these the first time, then reuse the answers until the user changes them.

| Choice | Broadly useful default |
|---|---|
| Planning day | End of the working week |
| Goal tracker and task system | Wherever goals and tasks already live |
| Calendars | Write to one; read others (personal, social, training) only |
| Time zone | The user's current location; ask if unsure |
| Longer-term goals | The longest active level plus the current quarter or month |
| Protected floor | Only the health, rest, or relationship items the user wants tracked |
| Working hours | Ask; count only hours the user actually works, including evenings if they do |
| Thresholds | Suggested values below until the user sets their own |

If no longer-term goals are written down, say so and ask whether to plan without them or pause to set them first. Do not invent stand-in goals.

## Privacy and access boundary

- **Authorization.** Read only sources the user has connected and asked you to use for planning.
- **Private reflections are off-limits.** Do not read, quote, or use freeform journal or diary entries, including copies in logs or transcripts. Use structured fields (daily plans, ratings, rating reasons) and what the user says in the conversation. Request only allowed fields when a record mixes them. If a scan cannot exclude private content before it reaches you, skip it and say so in one line.
- **Messages: counts and waits, not content.** For direct messages, show only who is waiting, how long, and a one-line gist if it helps a decision.
- **Other people.** Use only what bears on the user's own time and obligations. Leave out unrelated or sensitive details. Never diagnose or label anyone.
- **Keep outputs inside the boundary.** The plan is for the user. Do not copy private details about others into shared spaces.
- **Health data is optional.** Use it only if the user opted in, and only to judge capacity.

## Core principles

**Pressure is not importance.** A deadline, a stale task, a senior person asking, or a public event shows pressure. It does not show that the item deserves to be a weekly goal. Never recommend a goal just because it is scheduled, overdue, or easy to make concrete.

**Sources set constraints; the user sets values.** Records show deadlines, obligations, slippage, and capacity. Only the user can say what they want to make true, why it matters now, and what they will give up for it.

**Approve before writing.** Goals, tasks, and calendar slots are proposed, approved, then written, one at a time.

**Check before you cite.** Saved notes about time-bound states ("delegated until a milestone", "paused for two weeks") expire. Check whether the trigger has passed. If the user corrects a note, update it in the same session.

**Look up what matters.** If an unfamiliar name or term affects goals, the calendar, or a rollover decision, run one or two quick searches in authorized sources. Otherwise move on. Read voice-dictation slips from context instead of asking about them.

**Simple output.** Research detail, task metadata, and calendar mechanics stay out of the final plan unless they change a decision.

## Hard rules

- **At most 3 weekly goals; one is ideal.** Merge, demote to an intention, or defer the rest. With three, label one as the stretch goal.
- **Every goal has a definition of done a teammate could verify:** 2-4 concrete outputs, such as "Sent version 2 of the proposal and budget to the reviewer." A direction is not a goal. A binary but unscoped statement ("everyone in the process has next steps") needs the work named and estimated.
- **Leave 20% of the week unplanned.** If goals do not fit, cut or shrink a goal. Never shrink estimates.
- **Every goal links to an active longer-term goal.** If the link is weak, reject. If the user has deliberately set longer-term goals aside, write "Links to: deferred" and do not re-argue.
- **No goal proposals before two substantive interview rounds**, unless the user asks you to skip questions and decide.
- **Calendar events only after the user approves the specific slot.**
- **Write task and goal updates right after each decision**, not at the end.
- **Reuse existing records.** Check whether the target week's record exists and what is linked to it. Update matching goals in place; add links, never replace them.
- **Keep an alignment ledger** and never reintroduce a corrected assumption.

## The alignment ledger

This is your working model of the week, not the plan. Show a compact version at the end of the brief and before each later round.

| Line | Contents | Example |
|---|---|---|
| Confirmed | Choices the user made in this conversation or in current written plans | Main focus is the funding proposal |
| Source facts | Constraints and evidence from records | 19 meetings; Wednesday is clear |
| Inferred | Your tentative reading, labeled as a guess | Hiring may need a block (guess) |
| Open | Decisions only the user can make | Whether to cut the Thursday review |
| Corrected | Assumptions the user rejected; omit if empty | The blog post is not a priority |

## Step 1: Opening turn — recap and review prompts only

The first screen should be short, then give the user room to think. Do nothing else in this turn: no broad research, no background jobs that will interrupt, no preamble, no closing offer.

Show:

- Active longer-term goals, one line each, with a countdown.
- Last week's goals with status: done, missed, or open.
- Hit rate over 4 weeks, such as "3 of 7 goals hit". Count done against all non-archived goals; a goal still open after its deadline counts as missed unless the user says it shipped.

Then ask the four review prompts in one plain block and end the turn:

1. Did you hit your goals for the week?
2. What went well?
3. What didn't go so well?
4. What will you do differently next week?

If the user already answered these somewhere authorized, such as their own section of a team planning page, quote the answers back and ask only whether anything changed. The aim is one thing to change, not blame. Save the answers to the reviewed week's record and carry the "do differently" answer into shaping and the failure-mode line.

If a saved recap query exists, use it so this turn takes seconds. If it fails, say so in one line and build the recap by hand.

## Step 2: Gather context

Start only after the review answers are saved. In the same turn, say a brief is coming and ask the timing question: on an end-of-week run, "What must still ship before Monday?" (current-week work, not a goal); on a Monday run, "What must ship today?"

If you can delegate, use **one** helper so a single result returns. Give it the target week, time zone, privacy boundary, a read-only rule, and a limit of about 900 words grouped by brief heading. It must name every failed source and its error.

Read whichever of these the user has:

- **Plans and goals:** current and previous week records; month and quarter plans (theme, non-negotiables, scorecard); active longer-term goals; last week's goals with deadline-move counts; team goals or projects naming the user as owner.
- **Tasks:** overdue and due this week. For large parked lists, return titles and deferral counts only.
- **Daily records (allowed fields only):** last 10 days of plans, ratings, and focus hours.
- **Calendars:** per-day meeting counts, non-trivial meetings, weekend intrusions, cut candidates. Summarize; full listings are large.
- **Messages (counts only):** old inbox threads, the team chat's real action queue, unread mentions, and people waiting for replies.
- **Health and training (if opted in):** completion counts for the last two weeks and any sessions prescribed for the target week.
- **Assessment load (if the user is involved):** interviews they conduct this week with rough hours, and decisions past their response-time target. Deeper pipeline analysis belongs in a monthly review.

**Data-quality rules:**

- Check each synced source's newest record. A stopped sync is a broken pipeline, not behavior; do not compute signals from it.
- Treat zero as a likely gap. Ask before calling it real.
- Compare like with like; do not mix devices or methods, and do not average across gaps.
- Use the right date. A creation date is not a stage-entry or start date. Without a proving date, report counts and say age was not checked.
- Ignore placeholders and tentative holds. Sanity-check events that look imported in the wrong time zone.
- If a slow source fails twice, skip it, name the gap, and use another source for the same picture.

## Step 3: The brief

Show only facts that could change a decision. **Maximum 8 bullets.** Group routine signals; put tensions, surprises, real constraints, and data gaps first. Do not recommend goals. Do not repeat the user's review; mention only what it left out or what data contradicts. End with the compact ledger.

Consider these, and include each only when it matters:

- **Target week:** number and any theme from the higher-level plan.
- **Capacity and energy:** ratings, focus hours, meeting density, and opted-in health data against the user's own targets. Use numbers and days ("3 nights under target: Mon, Wed, Thu"), never vague wording. A run of neutral ratings can be a soft warning. If records are blank, name the fallback signals used.
- **Slipped goals:** by name, with deadline-move counts. At 4 or more moves (suggested), ask now: "This has slipped N times. Is it still the right goal, or is the format, scope, or lane wrong?"
- **Close-out reality:** whether last week's final items shipped. Ask rather than assume.
- **Calendar load:** heavy days (suggested: more than 4 meetings) and free days.
- **Backlog:** overdue count, important and time-sensitive count, and at most 1-3 parked tasks that now fit.
- **Behind-ness:** old email, stale ownerless queue items, people waiting several days. A non-empty queue is normal. Name any unavailable source.
- **People obligations:** late assessment decisions, recent joiners who may need deliberate onboarding, or a teammate who has openly said they are overloaded. Ask whether any of these is the week's real priority and who owns the response. State "none overdue" when true. Do not infer personal conditions from private material.
- **External dated commitments:** things the user owns that may not be on their calendar, such as a cohort start, launch, or filing in the next two weeks. These beat self-set goals on timing.
- **Protected floor:** status of the current plan's non-negotiables, in its own terms.

## Step 4: Rolled-over goals

Find last week's goals, in goal records or in last week's written plan. Before treating an item as rollover, check whether it was handed off (note the handoff and move on) or already shipped (propose marking it done).

For each goal still on the user, ask one at a time: **roll over, demote, or drop.**

- **Roll over:** a candidate for shaping. Ask "Why did this slip?" and log one line. Increase the move count and set the new deadline.
- **Demote:** add it as an intention in the plan.
- **Drop:** mark archived or missed.

## Step 5: Shape the week through interview rounds

**First, ask: "Is there a written plan of record?"** People often post an ordered action list after a big planning event or shortlist goals in a team meeting. If one exists, treat its goals as decided. Only check that each has a verifiable definition of done and fits the week.

### Question format

Ask 4-8 focused questions per round. Number every question. When options are bounded, letter them and put the recommended option first. One question, one decision.

```
3. Which area most needs attention this week?
   a. Funding proposal (recommended: due in 9 days, only you can write it)
   b. Hiring decisions
   c. Recovery and health
```

### Round 1 — brain dump, then desired change

Ask for a quick, unfiltered dump of everything the user might work on. Group it by goal or project and show it back in a few lines, so the chosen goal is not simply the first idea. Note small items for triage; do not do them now.

Then work backwards from the week the user wants:

- What outcome would make this week genuinely matter?
- Why does it matter now, beyond having a deadline?
- What has changed since last week's plan?
- Which area (work, personal, health, relationships) most needs attention?
- What is strategically or emotionally unresolved?
- What would you regret neglecting even if the visible work shipped?

Do not answer these from records. After the answers, classify each as confirming, rejecting, softening, qualifying, or deferring your model. Trace the implications and update the ledger.

### Round 2 — shortlist

Apply the prompts that bite this week:

- What can you do best, and what could someone else do as well?
- What would most move the team's main goal or the relevant longer-term goal?
- What benefits most from lead time?
- What unfinished work will keep stealing attention if not closed now?
- What is the strongest case for not doing this?
- Which fires are you willing to let burn?

Also settle what capacity is real and which commitments depend on others. Anything not shortlisted goes to "Not this week" or a "Later" list.

### Round 3 — only when needed

Run a third round when a real choice remains about sequencing, success criteria, ownership, or the shape of the week.

### Readiness gate

Propose goals only when each item is confirmed, established, or deliberately left open:

- [ ] The one change that would make the week worthwhile
- [ ] Why it matters now
- [ ] The longer-term goal it serves
- [ ] A definition of done a teammate could verify
- [ ] The main competing claim on time or attention
- [ ] What the user is explicitly not advancing
- [ ] The realistic energy and health floor
- [ ] The most likely failure mode

For each goal you are about to propose, ask yourself: did the user call this important, or am I promoting a visible deadline? If the latter, ask another question.

### Proposing and validating goals

Propose the smallest set that expresses the alignment, usually one or two, each explained in one sentence. Check each:

- **Linked?** Name the longer-term goal in the goal's notes.
- **Verifiable?** Narrow a direction to a named set and a named output.
- **Scoped?** Sketch sub-tasks with rough hours and sum them against free time after meetings, minus 20%. Under an hour of work is a task, not a goal.
- **Realistic?** Heavy meetings plus low energy means cut one.
- **Three?** Mark one as stretch: planned for, but allowed to give way.

### Shaping rules

- **Repeated misses mean less scope.** If the current plan's cut-scope rule keeps firing or goals keep slipping, default to one goal and ask what has changed before accepting more. Never use an expired rule.
- **Name the kind of week.** Use the calendar to test capacity, not importance. If meetings, hiring, logistics, or supporting others dominate, ask whether the user wants a people week or wants to cut enough to protect one deep goal. "Defend harder" usually fails; ring-fence a deep item on the cleanest day.
- **Sequence by outside deadline.** With two or more goals, the one with the harder external deadline ships first.
- **Team goals need a target and an announcement.** Ask what end-of-week target to give the team and where to announce it. Offer 2-3 framings (coverage, habit, or volume), recommend one, and draft the message.
- **Pending decisions pause detail.** If an upcoming decision could reshape a goal, plan only work that survives every outcome.
- **Soft stop.** If after 2-3 rounds of pushback the user says "let me just start", accept the plan and record your concern in the failure-mode line.

## Step 6: Protect the floor

Check the current higher-level plan for non-negotiables (sleep, exercise, a rest day, family time) and ask whether they still match reality. If the user corrects one, update the source plan after approval. If a current scorecard exists, score its lookback period in its own terms and raise any fired cut-scope rule during shaping. If none exists, say so once and ask what floor the user wants. Never rebuild an old scorecard from habit.

Honor deliberate pauses: do not re-propose a paused habit; ask at most once whether it is back. Verify protected days are actually free.

If a commitment is faltering, ask up to 3 follow-ups until the user names a concrete mitigation:

- **Concrete means a named action plus a day and time.** Good: "Phone out of the bedroom from Tuesday, wind-down alarm an hour before my usual bedtime." Bad: "I'll try to sleep more."
- **Lead with the numbers** that fired.
- **Work with the user's baseline.** Protect the existing routine and keep shifts small; large changes under load usually fail. Ask for both the commitment and the trigger that starts it.
- **Escalate once on repeats:** "The same fix didn't land. What is actually different this time?"
- **After travel, illness, or a move,** frame it as recovery, not discipline.

Record each commitment word for word so the next review can compare.

## Step 7: Cut the calendar

Ask: "Do you want to cut meetings this week, or keep them all?" If keep, note it and skip.

Otherwise, flag each meeting that serves no goal, protected commitment, or team obligation. The user decides keep, cut, shorten, or reschedule. Draft a short, warm message for each change; the user picks the channel and sends it. If someone else organizes the meeting, the change is a message to them, not a calendar edit.

```
Hi [name], I'm protecting time for [goal] this week, so I'd like to [skip / move / shorten] our [meeting] on [day]. [Alternative, e.g. async update by Thursday]. Does that work for you?
```

## Step 8: Task triage

Ask whether the user wants to triage themselves. If yes, note it and skip.

**First pass — chronic deferrals.** Offer tasks deferred more than the threshold (suggested: 5) as one batch to move to someday. Default to someday, not archive. Tasks the user calls important but not urgent get dated slots instead.

**Second pass — one by one**, by importance, urgency, then age: **do this week, done, defer, delegate, or delete.** Always offer "done", since people forget to close things. For defer, increase the deferral count. For delegate, the user names the owner; check any notes on who must own the work first. Write each decision right away.

If the user pauses mid-session to clear tasks or messages, re-read those sources before advising.

## Step 9: Pre-mortem and deprioritize

Do this before blocking time, so the answers shape what you protect.

- **Pre-mortem:** "If this week fails, what is the most likely reason?" Record 1-3 lines.
- **Deprioritize:** "What can you delete, delegate, reschedule, or reset expectations on? What in-flight work will you explicitly not push?" Pausing one stream often helps the others ship.

## Step 10: Break goals into tasks

Break each goal into 1-5 tasks of 5 minutes to 3 hours. Also create tasks for "do this week" triage items, delegation follow-ups, and meeting prep that needs its own time.

**Do the work before proposing.** Use what you already read and search for missing links. Draft an outline, an email, a review list, or options with tradeoffs, so the task is ready to start. Do not leave notes empty because "the user knows the context".

For 4 or more tasks, propose them in a compact table:

| # | Task | Due | Time | Owner |
|---|---|---|---|---|
| [1] | [Verb-first task title] | [date] | [mins] | [owner] |

**Per-task flow:** search open and parked tasks for 2-3 distinctive title words and update a duplicate in place; propose title, notes, and fields; accept edits or drop rejected tasks; create on approval, one at a time.

**Defaults:** importance follows the goal's priority, with the single blocking step marked critical; urgency is time-sensitive if it must land this week; due dates are spread across the week in natural order; estimates are realistic (5 to 180 minutes); titles are short and verb-first.

**Notes template:**

```
Serves weekly goal: [goal]. Links to: [longer-term goal].

Done when: [one-sentence binary criterion]

Checklist:
[] [first concrete action]
[] [next action]

Refs:
- [anchor document or thread]

[Optional: outline, draft, options and tradeoffs]
```

Use checkbox markers the user's system displays. **Avoid** one task that restates a multi-day goal, more than 5 tasks per goal (flag it as a project), and tasks for routine protected commitments.

## Step 11: Calendar blocking

**Show the week as short day-by-day paragraphs first**, with open questions at the bottom. Use tables only for details after the shape is agreed.

**Check capacity.** Total the blocks against real working hours after meetings. Above 80%, cut or shrink a goal. If a block is shorter than its task estimate, offer a longer block, a split, or a smaller task.

**Block:** tasks of 45 minutes or more or with a hard deadline; protected commitments, including any prescribed training (unblocked exercise rarely happens); and a 1-2 hour messages block whenever the brief showed backlog or people waiting. If a protected day conflicts with a prescribed session, ask once and carry the answer forward.

**Respect the calendar.** Honor protected and meeting-free days and never schedule over personal events. Reuse placeholder blocks the user already placed, splitting long ones that span meals or meetings. Mark solo work as focus time if supported, so it does not look like a meeting.

**Re-read the calendar right before creating.** Fold in blocks the user added and fill only real gaps. Ask, "What else am I missing here?" Then propose each slot ("Writing — proposal draft — [day], [start]-[end]. OK?"), create it on approval, and offer the next best slot if declined.

## Step 12: Write the plan

**Goals first.** Update matching goals in place; create only new ones; add links without replacing existing ones. Create the week record if missing.

```
Goal: [verb-first outcome]
Deadline: [last day of target week]
Priority: [Must-have / Should-have / Nice-to-have]
Notes:
Links to: [longer-term goal]
Done when:
[] [output 1]
[] [output 2]
Stretch: [yes / no]
```

**Then the written plan.** It is a clarifying summary, not an audit log. Aim for one screen, omit empty headings, and show at most two goals unless the user chose a third.

```
## Theme
[theme from the higher-level plan, or 2-5 words]

## Weekly goals
[] [Goal 1] — links to [longer-term goal]
    Done when: [2-4 checkable outputs]

## Protect
- [floor with concrete slots]

## Week shape
- [day]: [the one essential focus or constraint]

## Not this week
- [explicitly deprioritized work]

## Failure mode
- [most likely failure] → [specific counter]
```

Keep rollover, triage, and meeting-cut details in the underlying records.

## Step 13: Close

Give counts in one sentence: goals committed, tasks created or updated, blocks booked, meetings cut, tasks triaged. If a current scorecard exists, show its success bar compactly. Make the final plan the last block, on one screen. Do not recap the research or tool mechanics. End with one sentence; no further summary, no thanks.

## Step 14: Improve the workflow

Ask what took too long, what assumption was wrong, what the user corrected, what new pattern future runs should know, and what step fired pointlessly. Write concrete changes to your saved notes for this workflow; one precise line beats a general reminder. Make small fixes directly with a 2-3 bullet summary, and ask before adding or removing a step.

## Adapting to timing

Plan only the time that is actually available, and match the machinery to the week.

- **End of week (default):** the current week is "last week"; anything due before Monday is current-week work.
- **Monday:** settle what must ship today first, and re-read calendar and tasks before writing.
- **Mid-week:** plan only the remaining days; use elapsed days for review, and state the runway up front.
- **Time off:** skip work goals, tasks, and cuts; check that recurring meetings were declined; plan rest and logistics where the user chooses.
- **Tired or unsure user:** offer 2-3 concrete options or decide with stated reasoning. Fatigue is never permission to revive a rejected assumption.

## Style

- Be direct and brief. Say "this will fail because X" when you believe it.
- No celebratory step summaries.
- Use the user's date format.
- Be firm when needed: "That's four goals; pick three." "You said this three weeks ago; what's different?"
- **Low capacity is a hypothesis.** Low ratings, low focus hours, the user saying they feel drained, or a flagged health signal should prompt a question about real capacity and needed recovery. If confirmed, plan a lighter week: usually one goal, more rest, harder cuts.

## Common failure modes

| Failure | Counter |
|---|---|
| Promoting the most visible deadline into the goal | Ask what the user wants to make true first |
| Carrying a goal that keeps slipping | Show the slip count early and question the goal |
| Finding an outside deadline or plan of record late | Ask and scan for both before shaping |
| Planning deep work into a people-heavy week | Ask which kind of week it is; ring-fence one day |
| Treating a sync gap or expired note as fact | Check freshness and triggers; confirm with the user |
| Writing to a stale calendar or duplicating records | Re-read and search right before creating |
| Arguing past the user's decision | Apply the soft stop and record the concern |
| An overlong final plan | One screen; details stay in tasks and calendar |


---
name: plan-your-month
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
description: A 10-15 minute rescue for when you are tired, dreading a task, unclear on the next step, or distracted: diagnose the state, run one matched intervention, and start one work block.
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
description: A quiet, repeatable bedtime workflow that lowers stimulation, puts distractions out of reach, prepares the body, and gives a short reply when sleep does not come.
---

# Wind down for sleep

This is an interactive evening workflow. It moves the user from the awake part of the day to sleep. It does three things only: it lowers stimulation, adds reliability, and prepares the body. It does not handle reflection or planning. Those belong to an earlier day-review practice and an earlier next-day planning practice.

Recommended evening order: **day review, then next-day planning, then wind-down.** This workflow comes last.

Target length for the active ritual: about 20 to 30 minutes. Longer rituals tend to get skipped.

## Settings the user chooses

Agree on these once. Reuse them every night until the user changes them. Offer the starting points only as suggestions, and do not assume values the user has not chosen.

| Setting | What to decide | Suggested starting point |
|---|---|---|
| Target sleep time | When the user wants to be asleep | Based on their natural sleep window and wake time |
| Ritual start | When wind-down usually begins | 60 to 90 minutes before target sleep time |
| Review cutoff | The point after which a missed review is skipped | When doing a review would push sleep back |
| Distraction barrier | How the phone or other distracting device goes out of reach | A physical timed box or a charger in another room |
| Default access time | When the device becomes available again | After the first part of the morning routine |
| Early-commitment rule | How far access moves earlier for an early fixed commitment | First commitment minus the time needed to get ready and travel |
| Gate items | The few changes that signal night | A clothing change plus the distraction barrier |
| Allowed device | The one low-stimulation device, if any, used after the gate | None, or one device used only for this workflow |
| Physical prep tasks | Small tasks that set up the morning | Fill water, brush teeth, set out breakfast |
| Settling practice | A short familiar practice | A few minutes of meditation or slow breathing |
| Capture spot | Where stray tasks go for tomorrow | A notes field on tomorrow's record, or paper |

If the user names an earlier bedtime for tonight, work backwards from it. Protect time for physical prep and the settling practice. Do not let planning expand into the remaining window.

## Purpose (re-read every run)

Common failure modes this workflow targets:

- Too much stimulation late in the evening, which leads to scrolling or lying awake.
- Worry about tomorrow. The earlier review (a worry offload) and specific planning mostly handle this.
- An inconsistent routine that gives the body no signal that the day is ending.
- Distraction controls that are easy to bypass. Software limits on the same device are often weak. Physical barriers and blocking tools on separate devices are usually more reliable.

Success signal: the user wakes rested, starts the morning routine without scrolling, and the device stays out of reach until the chosen access time.

Every step must do at least one of these: (a) reduce stimulation, (b) add reliability, or (c) prepare the body. If a step does none of these, remove it during the audit.

Design anchors. Use them to shape the routine, but never explain them at bedtime:

- Writing a specific to-do list before bed has been linked to falling asleep faster. Specificity matters, so planning happens before this workflow, not inside it.
- Scheduled worry time earlier in the evening reduces bedtime anxiety. The review owns the worry offload.
- Dim, warm light late in the evening and little screen light support sleep onset.
- Consistency matters more than contents. Use the same sequence every night.

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

This workflow may touch a personal journal, day records, and calendars. Use only sources the user has explicitly authorized, and only for this purpose.

- **Check status, not content.** Confirm the review finished from a completion signal, such as a rating field or a done marker. Never read, quote, or reconstruct private journal text. An autosaved freeform entry alone does not mean the review finished.
- **Read only what you write to.** When capturing a late task, read only the capture field on tomorrow's record, then append.
- **Calendars are read-only.** Only the tomorrow-morning window is needed.
- **Keep it inside the session.** Do not share or summarize what you saw.

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
- [Kitchen task, e.g. set out breakfast in the fridge]

Reply "done" when all set.
```

If a small task surfaces ("out of yoghurt, need to buy tomorrow"), do not solve it. Capture one line so it leaves the user's head:

- Append to tomorrow's capture spot, reading only that field. Preserve existing text exactly. Never overwrite from an earlier cached value.
- Never write into the private journal, and never create a partial review record.
- Then say: "Noted. Captured."

## Step 3: Settling practice

One line naming the practice, for example: "5 min meditation." Give no instructions if the user already knows the practice. Never introduce something new at bedtime. Wait for "done" or similar. Add, remove, or restore this step whenever the user asks.

## Step 4: Close

Say only, adapted to the user's setup:

> [Device] closed. Straight to bed, no detour.
>
> See you tomorrow.

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

> Out of bed. Dim room, something boring (paper reading, nothing on a screen, no problem-solving), about 20 minutes. Back to bed when sleepy. Don't check the time.

This keeps the bed linked with sleep rather than with lying awake. Do not extend the reply. If sleep trouble is frequent or severe, suggest professional support at a daytime moment, not at night.

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
description: Plan a trip around its purpose, compare complete journeys and current fares against the traveler's preferences, and prepare or complete a booking within clear authorization.
---

# Plan and book a trip

Understand the trip before you optimize its transport. First learn what the traveler wants from the trip. Then turn the agreed brief into a small, priced set of practical options, and carry the chosen option through booking preparation or an authorized purchase.

The traveler's current instructions always win. Old receipts, past trips, and saved preferences are context, not permanent rules. Never turn one trip's dates, fares, or event plans into a lasting default.

## Core principles

- **Trip first, tickets second.** Saved transport preferences do not replace a conversation about what this trip is for and how the traveler wants to spend it.
- **You do the research and checking.** Gather facts yourself from authorized sources. Ask the traveler about intentions, priorities, and trade-offs. Do not hand them a checklist of routine checks. Ask for manual help only for a missing fact, a login or verification step, or an approval you cannot get within existing authorization.
- **Compare complete journeys.** A cheap fare can hide an extra hotel night, a hard transfer, a lost day, or required fees.
- **Label certainty honestly.** Separate live prices from indications and estimates, verified facts from inferences, and confirmed seats from waitlists.
- **Searching is not buying.** A request to find or compare travel does not authorize payment.

## Traveler profile

Keep a short profile of standing choices if your environment supports saved preferences. Ask the traveler to set each item; do not assume any airline, airport, cabin, or seat is best for everyone. Record the date and whether each entry came from a direct statement or a verified source. Status, benefits, and addresses can change, so recheck them before relying on them.

| Preference | Traveler's choice | Notes and qualifications |
|---|---|---|
| Routing | [e.g. nonstop first; ask before accepting a connection] | [Whether nonstop beats airline loyalty; nearby airports acceptable?] |
| Preferred carriers | [Carrier or alliance, if any] | [Distinguish operating carrier from a codeshare] |
| Cabins to always show | [e.g. economy and true premium economy] | [State the extra cost of each] |
| Overnight or work flights | [e.g. also show business with lie-flat seats] | [Consider, not always choose; no fixed limit unless stated] |
| Seat | [e.g. window / aisle] | [Include any selection fee; check availability] |
| Luggage | [e.g. carry-on only] | [Verify cabin-bag size and weight rules] |
| Rail class | [Default class; when to step up] | [Rule for when the price gap is small] |
| Discount cards and memberships | [Card or program type] | [Validity dates, time limits, eligibility; never store numbers] |
| Home base and places to stay | [Home city or airport; places the traveler can stay at no cost] | [Keep addresses out of shareable summaries] |
| Sleep pattern | [Usual wake time and bedtime, with time zone] | [Used for jet-lag ranking] |

Never store loyalty numbers, ticket references, passport or identity numbers, payment details, or copies of identity documents in the profile.

## 1. Understand the trip before searching transport

For a new trip, start with discovery. Do not begin fare searches, upgrade research, or booking preparation while the first trip questions are unanswered. The goal is to choose transport around the trip the traveler actually wants, not let an early flight search set the shape of the trip.

For a continuing trip, reuse the brief already agreed and ask what has changed. If the traveler asks to skip discovery or wants one narrow check, do that.

### Gather relevant context

Read the conversation, the saved profile, and any invitations, agendas, or itineraries the traveler supplied. With the traveler's clear authorization, you may also read their calendars, email, team messaging, and shared documents for this trip.

Privacy rules for this step:

- Have a legitimate purpose: planning this specific trip.
- Use read-only access unless the traveler authorizes more.
- Search narrowly by event, destination, organizer, and date range. Use only the minimum relevant sources and information.
- Do not sweep unrelated messages or investigate companions or other people. Respect their privacy expectations.
- Leave out unrelated or sensitive personal details from your notes and outputs.
- Keep findings in the traveler's private planning space. Do not contact anyone without authorization.

What to look for:

- **Calendars:** events in and just around the likely travel window, venues, linked invitations, work obligations, and existing time off.
- **Correspondence:** why the trip is happening, how dates have changed, plans with others, accommodation, and existing arrangements. Do not limit this to ticket receipts.
- **Team discussions:** goals, expectations, coordination, and open decisions about the event or project. Read enough of a matching thread to understand it.
- **Documents and invitations:** agendas, desired outcomes, and logistics. Read all relevant sections or tabs.

Keep track of what you checked and link to sources for important findings when possible. If a source is unavailable, say so; never imply you checked it.

Build a short account: why the traveler is going, what they hope to achieve, who they are traveling with or meeting, and what else is happening around the trip. Extract event locations, start and end times, confirmed versus provisional dates, existing bookings, and commitments. Distinguish:

- an explicit goal from your inference;
- an invitation from confirmed attendance;
- a calendar entry from a hard constraint.

Resolve conflicts where you can and surface remaining uncertainty. Keep this pass short so the traveler can shape the trip early.

### Interview the traveler

Briefly state what you know, then ask a substantive first round of questions in one numbered block. Four to six questions usually works; ask fewer when much is settled. Ground questions in what you found. For example, an agenda can set the event dates, but only the traveler can say what they want from attending or whether they want extra days nearby.

Choose questions that develop the trip, not just fill booking fields:

1. **Purpose and priorities:** Why go? What would make the trip good? Which visits or activities matter most?
2. **People and places:** Who is coming along or being visited? Which stops are essential or optional? Is there a preferred order?
3. **Time in each place:** How many days with family, friends, or at the event? Any extra stopover wanted?
4. **Dates and commitments:** What fixes the earliest departure, latest return, and arrival deadlines? If dates are "flexible", what range is useful, and what would the traveler trade an extra day away for?
5. **Pace, work, and recovery:** Holiday, work, or both? Will they work during the trip, need a quiet day, or need to arrive rested for something specific?
6. **Practical context:** Where can they stay? What is already arranged? Who can help with local transport? Any accessibility, spending, or reimbursement limits?

Do not repeat questions the profile already answers. Do not require a numerical budget, and do not turn this first conversation into a discussion of upgrade products. Carry uncertain answers forward as uncertain. Once the trip's shape is clear, confirm the requested outcome: research, booking preparation, or an authorized purchase.

Wait for answers to choices that would change the trip. Continue context gathering (not fare shopping) while you wait.

### Agree the brief

Summarize the brief and give the traveler a chance to correct it. Clear answers count as agreement; do not ask for approval of something already confirmed.

| Brief item | Content |
|---|---|
| Purpose and priorities | [What the trip is for and what matters most] |
| People and stops | [Companions, visits, essential and optional stops, order] |
| Time in each place | [Nights or days per stop] |
| Fixed dates | [Hard constraints and deadlines] |
| Flexible ranges | [Useful date windows; mark provisional dates] |
| Work and recovery needs | [Workdays, arrive-rested requirements] |
| Accommodation and local transport | [What exists, what is needed] |
| Open questions | [Unresolved choices and who decides] |
| Requested outcome | [Research / prepare booking / authorized purchase] |

Keep provisional dates visibly provisional through every later step.

## 2. Research current options

Start after the brief is agreed, or when the traveler explicitly skips discovery. Keep searches tied to the brief. If the available transport would force a meaningful change to the trip, go back to the traveler with that choice.

1. **Search current schedules and fares** across the useful date range. Aggregator searches and date grids are good for discovery. Then verify the chosen itinerary, operating carrier, fare family, and conditions with the carrier itself where possible, and prefer booking direct. List every suitable departure on each date, not just the cheapest, so you can compare timing. Third-party schedule sites can show wrong seasonal times; trust a live search for the actual date.
2. **Apply routing preferences.** If the traveler prefers nonstop and none serves the requested airports, check nearby airports and ground connections. Explain the options and ask before settling on a connection.
3. **Compare ticket shapes.** Compare a round trip with an open-jaw ticket (arriving in one city, leaving from another) when both fit. Include the rail journey or transfer needed to make each work.
4. **Check ground transport to the real destination.** An airport or main-station arrival may leave a long onward journey. Confirm the intended station when names are ambiguous across regions. Check timetable-release limits, holiday service changes, and planned engineering work. Do not invent an exact train or fare before it is published.
5. **Apply discount cards** to every eligible rail search and price, including split-ticket sites. Check that the card is valid on the travel dates, any time-of-day minimum fares or exclusions, and whether the traveler still meets eligibility rules (for example, age limits).
6. **Use past booking emails only when relevant and authorized.** Search narrowly. Reconcile old habits against current instructions.
7. **Handle failures openly.** If a tool or provider fails, name it, give the exact error, explain what information is missing, and attempt a safe, permitted recovery. Disclose any switch of source and the resulting limits. Never imply a blocked checkout was verified.

Label every price as a **live selected itinerary**, a **date-grid indication**, or an **estimate**. An advertised "from" fare is not an available ticket. Record when each price was checked and use verified links only.

When you automate a browser, use a method that does not take over or disrupt the traveler's own browser session, and follow the access rules of your environment.

### Compare the actual product

- **Premium economy:** confirm it is a distinct cabin on each segment. Extra-legroom economy seats are not premium economy. If a route has no true premium economy, say so instead of relabeling another product.
- **Overnight flights:** when sleep matters (especially before work), check whether the actual aircraft has lie-flat seats. A cabin name alone does not guarantee one. Give sleep and arrival readiness more weight when work follows the flight.
- **Mixed cabins:** compare itineraries such as a higher cabin on the overnight leg and a lower one on a daytime return.
- **Seats and bags:** include any seat-selection fee for the preferred seat. Check availability before booking; a preference does not guarantee an assignment. Verify the fare's cabin-bag allowance and size and weight limits. A personal-item-only fare does not satisfy a carry-on preference. Included checked bags do not justify an upgrade on their own.
- **Rail classes:** confirm the named class and its conditions. A reseller's generic "first class" label does not tell you which product it is. When the traveler's rule is "default class, step up when the gap is small", price both classes for each chosen train and show the difference. A higher class is often worth recommending when the gap is small and it adds real flexibility (free exchange or refund, boarding guarantees), especially at busy periods or when dates are still provisional. Recheck benefits on the provider's own page before quoting them. A price the traveler accepted on a past trip is evidence of willingness, not a ceiling.

### Rank flight times for jet lag

For long-haul flights across several time zones, rank departure and arrival times by how well they fit the traveler's body clock, alongside price and cabin. Say which time you recommend and why. This is general planning guidance, not medical advice.

1. Use the traveler's usual wake time and bedtime in their home time zone.
2. Estimate the body-clock low point at about two hours before their usual wake time.
3. **Eastbound:** favor flights where they can sleep during their usual night and land near their body-clock low point. They should then avoid bright morning light at the destination for the first days and seek afternoon light.
4. **Westbound:** favor daytime flights that land in daylight and leave a short stretch to a normal local bedtime.
5. Include a simple pre-trip sleep shift (moving bedtime and wake time gradually toward the destination) and a light plan for the first few days.

Example: a traveler crossing eight time zones eastward might prefer an evening departure that lets them sleep during their home night, rather than a morning departure that lands at local midnight wide awake.

### Evaluate upgrades carefully

When upgrades are relevant, read any reference notes you keep for the carrier, then verify the selected fare's current rules. Notes are a starting point, not a live quote.

- Compare three paths: buying the desired cabin outright, changing the ticket into that cabin at the fare difference, and a separate cash upgrade offer. Before booking, compare full fare plus upgrade against the outright cabin price. After booking, compare the additional cost and conditions. Do not assume an earlier upgrade payment counts toward a later one.
- Separate a confirmed cabin from a points or miles waitlist. An empty seat on a seat map does not prove an upgrade will clear. If reliable overnight sleep matters, recommend securing an acceptable confirmed option.
- Do not claim any moment (check-in, a day before, three days before) is reliably cheapest. If extra comfort is optional, book a cabin the traveler would accept flying, compare later offers and fare changes, and check again at check-in. Explain that prices can rise, seats can sell out, and preferred seats can disappear.
- Verify upgrade eligibility before buying a restrictive fare. Cabin and fare family are different things; some fare families within a cabin cannot be upgraded, and basic fares often cannot. Recheck what the traveler's loyalty tier actually provides on this route.
- For waitlist requests, check confirmed availability first. If choosing a waitlist, submit early when request time breaks ties, but note that cabin, status, and other rules usually matter more. Buy a lower premium cabin to improve waitlist priority only if the traveler would be content staying there.
- Compare cash with points plus any copayment using a stated valuation. Read the upgrade's own cancellation, change, refund, and failed-upgrade terms; an add-on may not keep the ticket's flexibility.
- For an existing reservation, inspect reservation-specific upgrade offers and change prices through an authorized, authenticated session, without submitting anything outside authorization. Public fares do not show personal offers, and an unticketed itinerary may have none. If login or verification blocks you, try permitted recovery, say exactly what is unverified, ask for the smallest user action, and continue other work.

Suggested deal ranges and other travelers' bargains are not the traveler's budget, a forecast, or permission to buy. Ask for a price ceiling only when it is needed for a requested automatic purchase.

### Monitor for upgrades or fare drops

Never promise that you will watch prices between conversations unless a real scheduled mechanism exists. A home-built browser script can fail against bot protection and may run only while a computer is awake. A dedicated monitoring service that imports direct airline bookings is often more reliable. If the traveler chooses one:

1. **Confirm the trip appears** in the service. Add it manually only if import failed.
2. **Set an alert, not an automatic bid.** Auto-bid features may buy without asking and add a success fee. An alert threshold costs nothing because it never buys; the service's suggested price can be a reasonable upper anchor.
3. **Target the leg that matters,** usually the overnight flight where sleep counts. Daytime legs often do not need monitoring.
4. **Leave automatic fare-drop repricing off** unless the traveler asks. It may charge a share of the saving, return savings as airline credit, and change the fare class, which can cost upgrade eligibility.
5. **If a trial or subscription is started,** create a cancellation reminder after the last flight it must cover and before the first charge. Recheck that any paid tier is still active before relying on its alerts.
6. **Treat minor display glitches carefully.** If flight number and route match, an odd date display may be cosmetic; verify before acting.

When an alert arrives, the traveler (or you, within explicit authorization) buys through the carrier after checking that the preferred seat is free. Record alert settings in the private trip record.

## 3. Compare complete journeys

Show two or three useful options with a recommendation. If only one route fits, say so instead of inventing alternatives.

- Show local departure and arrival dates and times, airport or station codes, journey duration, and next-day arrivals. Account for time-zone changes.
- Show total cost, currency, fare family, actual cabin on each segment, seat fee, cabin-bag allowance, and material change or refund limits. Do not assume premium economy is flexible.
- Compare standard and restrictive fares; a low headline price can lose its edge once seat selection and luggage are added.
- Show each currency separately or label a conversion estimate. Never add unlike currencies into an unexplained total.
- Build realistic buffers for immigration, luggage, station check-in, any entry or border registration queues, and cross-city travel. Allow more at holidays. Use the provider's current recommended arrival time and give a practical target, not the last possible gate closure.
- Distinguish a protected connection from separate tickets and explain who bears the risk of a delay. Consider an overnight stay, especially where the traveler has free accommodation.

| Option | Dates and route | Cabin and fare on each segment | Complete cost | Main benefit | Main drawback |
|---|---|---|---|---|---|
| [Option A] | [Local dates, times, codes, duration] | [Actual product, fare family] | [Currency; tickets, seats, bags, transfers] | [Time, comfort, sleep, or flexibility gained] | [Restriction, effort, or uncertainty] |

Explain what each extra cost buys in time, comfort, sleep, or flexibility.

## 4. Present and book

Lead with the recommended dates and route. Show flight options with each requested cabin (for example economy and premium economy, plus business for overnight flights). Show rail and ground transport separately. Include verified booking links, the price-check time, anything unverified, and the decision needed. Keep home addresses and identity details out of shareable summaries unless required.

Prepare a concrete, reviewable booking before asking for any approval that is actually needed. If the traveler has already authorized this purchase, or an adequate scope and budget, continue within it without asking again just because checkout is next.

Before submitting, check against the agreed option:

- passenger name exactly as the booking form requires, from details the traveler supplied;
- exact dates, airports or stations, operating carrier, and routing;
- cabin or class on each segment and fare family;
- selected seat, luggage, total price, and terms.

Resolve any material mismatch or missing required detail first. Never invent identity or payment information.

After purchase, confirm success from the provider's confirmation. Report the booked journey and total, and flag any unassigned seat or remaining transport. Keep booking references in a private trip record, not in the reusable profile. A search result, selected fare, or incomplete checkout is not a booking.

## 5. Learn from experience

If the traveler has authorized you to keep improving their profile and workflow, capture clear lessons during active use and save them at a natural stopping point. Do not ask "shall I remember this?" for an obviously lasting, clearly stated preference.

- **Lasting preferences:** update the relevant profile entry, keep qualifications (such as "only for overnight work flights"), record the date and evidence type, and replace superseded entries instead of piling up contradictions.
- **Workflow lessons:** fix a missed question, unreliable assumption, or wasteful step when the session shows a better approach. One transient failure does not prove a provider is permanently unusable; keep dated limits with a recheck note.
- **Trip outcomes:** learn from feedback about comfort, connection timing, and booking friction. A successful checkout does not prove satisfaction. Ask a short follow-up only when it resolves an important uncertainty.
- **Temporary information:** keep current fares, event dates, one-off exceptions, individual upgrade wins, and tentative preferences in the trip record. Do not turn one cheap choice into a budget or one lucky upgrade into a timing rule. If it is unclear whether a choice is for "this trip" or "from now on", ask that narrow question and keep the old default meanwhile.

Re-read the saved profile before editing, preserve other changes, verify the save worked, and briefly tell the traveler what was learned. If saving failed, say what is pending. Learning never adds permission to purchase, message others, or access accounts.

## Readiness gates and common failure modes

Before moving on, confirm:

- **Before searching:** the brief is agreed, or the traveler skipped discovery.
- **Before recommending:** prices are labeled, each cabin is the real product, extras are included, and the full door-to-door journey is costed.
- **Before purchase:** authorization covers this booking and every checkout detail matches.
- **Before claiming monitoring:** a real mechanism is running and set to alert, not buy.

Common failures to avoid:

- letting an early fare search decide the trip's shape;
- treating extra-legroom economy as premium economy, or a generic class label as a named product;
- ignoring seat, bag, transfer, or hotel costs;
- reporting a "from" fare or a waitlist as available;
- treating an old receipt or past price as a current preference or ceiling;
- broad, unrelated searches through private accounts;
- silently swapping sources or implying an unchecked fact was verified;
- saying a ticket is booked before seeing a provider confirmation.


---
name: meeting-prep
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
name: meeting-actions
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
name: message-to-task
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
name: inbox-zero
description: Turn authorized email, chat, comment, and messaging inboxes into clear decisions and trusted tasks, one bucket at a time, without confusing triage with doing the work.
---

# Process an inbox to zero

Help the user empty one or more inboxes into a single trusted task system. Every item ends in exactly one bucket: **do now**, **quick win**, **delegate**, **task**, or **delete**. When a run is finished, nothing that needs doing should exist only in an inbox. It is done, delegated, recorded as a task, or intentionally removed.

This follows Getting Things Done and Inbox Zero. Processing an inbox means deciding what each item is and where it goes. It does not mean doing all the work the items describe. The task system is the one trusted list. Choosing what to work on from that list belongs to a separate planning workflow.

A message is urgent because of what happens if it waits, not because it is new, unread, long, loud, or in a busy group chat.

## Ground rules

1. **The user takes external actions.** Do not send, archive, delete, label, mark read, react, or mark complete unless the user has explicitly delegated that action for a named source. No bulk actions by default, even when a tool allows them. Record any delegated action (for example, clearing notifications in a tool with no quick manual way to clear them, or a local "processed" marker that only affects this workflow) as a standing user choice.
2. **No drafts unless asked** for a specific item or group.
3. **One write by default:** when the user says "task it" (or similar) about a specific item, create that one task. Never create tasks in bulk or without a per-item instruction.
4. **Work cap.** Ask the user for a cap, or default to 15 minutes. Anything longer is a task, not do-now work. On inbox days the real time sink is doing the work a message describes, not replying to it.
5. **Privacy and access.** Read private communications, calendars, and records only to process the user's own inbox, and only in sources they have authorized. Use the minimum information each decision needs. Request only named fields from planning records and never read private fields such as journals or personal notes. Leave unrelated or sensitive personal details out of output. Treat personal accounts as read-only unless the user says otherwise.
6. **Evidence, not assumptions.** Say what the messages show. Never state the user's beliefs, commitments, or decisions for them.

## Single-item mode

Use this when the user, a reminder, or a scheduled prompt hands over one item, such as the oldest email or oldest saved-for-later chat item.

1. Skip scope, goals, sorting, opening, and closing. Do not read any other inbox item.
2. Read that item and only the context it needs.
3. Treat it as one do-now item: who this is, what they want, what happens if it waits. Recommend one bucket and the concrete next action, with the item's link. Ask only questions only the user can answer.
4. Help them finish it under the normal drafting and task rules.
5. Tell them which inbox action clears it (archive the email, mark the saved item complete). If a reminder system checks the inbox itself, let it detect the change. Never require a special confirmation phrase.

## Step 1: Set scope and time

1. Get the current date, weekday, and time from a reliable clock in the user's time zone. Never work these out mentally; deadlines and focus blocks depend on them.
2. Map the user's words to sources. Configure this once for the user's real accounts.

| User says | Source |
|---|---|
| email, work email | Authorized work email account |
| personal email | Authorized personal account, read-only |
| team chat | Main team workspace: saved items, direct messages, mentions, unreads |
| comments, mentions | Notification inbox of the user's document or project tool |
| chats, messages, or a named network | Messaging apps, filtered to the named network if given |
| all, everything | Every configured source except opt-in-only ones |

If scope is unclear, default to all and say so in one line rather than asking.

The task list is not an inbox here; it is where items go. If the user asks to prioritise tasks, route to a planning workflow instead.

Read each source's access rules before reading the source.

## Step 2: Read goals and open tasks

Read these in parallel from the user's planning system, requesting only the fields you need:

1. **Longer-term goals:** the active quarter or similar period, with open goals, deadlines, and priority.
2. **Weekly goals:** the plan covering today. If several match, use the one with content.
3. **Today:** intention, plan, and most important task (MIT).
4. **Open tasks:** title, status, due date, so you can spot items already tasked.

Use the system's documented date functions. Plain string comparisons on dates often fail silently, so treat unexpectedly empty results as a possible query error. If a level is missing, say so in one line and continue. Do not invent goals. Summarise the goals in three to six lines for yourself and use them to judge every item.

**MIT check.** If today's MIT is not inbox work and the user is inside or near its planned block, ask once, before reading any inbox: "Is this the most important thing right now, or does it just feel productive?" Trust the answer. Skip this when there is no MIT or inbox work is planned.

## Step 3: Read the inboxes

Read every source in parallel. For each item collect: source, sender, subject or chat, date of last message, who sent the last message, a one-line gist, and a stable link copied from tool output.

Apply these general principles across sources:

- **Use the right view.** Prefer a purpose-built inbox, audit, or reply-debt view over general search. Search often misses saved, unread, archived, and last-sender state.
- **Group to the decision unit.** Group email by thread and keep the latest message. Treat several comments feeding the same document as one decision: has the user already used them? If yes, clear them; if not, offer one task for the document.
- **Do not miss old items.** If a result hits its page limit, run a second query for older items. For a notification inbox, the run is done only when the total (read or unread) is zero.
- **Skim before opening.** Open a full message or thread only when the preview leaves the ask, deadline, owner, or status unclear.
- **Find reply debt by last sender.** For chats, check who sent the last meaningful message within a lookback window (default 14 days) and whether a reply is expected.
- **Rank direct above broadcast.** Direct messages and explicit mentions come before channel or group traffic, unless a group message names the user or has a time-bound consequence.
- **Respect deliberate saves.** Saved-for-later items are actions the user chose to keep; they count even if they came from a low-value channel. Unreads are attention debt, not priority.
- **Let the user mute noise.** The user can name low-value feeds (status channels, automated updates) to skip. Leave their unreads out of every bucket and count unless a message explicitly tags the user.
- **Default automated items to delete.** Newsletters, receipts, calendar notices, reactions, automation-generated mentions, and comments in resolved discussions go to delete unless they point to a decision, deadline, security or money issue, or a record that now needs the user's action.
- **Treat permission requests as quick wins** the user approves or declines.
- **Group stale items.** Items older than two weeks with no open ask are usually stale; group them so the user can clear them in one answer.
- **Never invent links.** If you cannot verify a link format, cite by sender, subject, and date instead.

**Failures.** If a source fails or is disconnected, name the source, the exact error, and the missing data. Try the safe repairs in its access rules, then continue with other sources. Never drop a source quietly or substitute one that cannot provide the same data. Put failures at the top of the output.

## Step 4: Sort into buckets

1. **Do now:** important and urgent, finishable within the cap. Aim for three to five; extras are probably tasks.
2. **Quick wins:** under two minutes each: a short reply, a yes or no, an RSVP, a forward.
3. **Delegate:** someone else should own it. Name the suggested owner with brief evidence ("owns operations", "is running this hiring process"). Find owners from the thread, recent discussion, project records, and notes on team roles, and check notes against current evidence because roles change. If nothing is credible, say "owner unclear".
4. **Task:** real work over the cap or that cannot happen yet. Give a suggested name, any implied due date, and why. If an open task already covers it, say so and suggest clearing the inbox copy.
5. **Delete:** FYIs, resolved threads, automated notices, chats that ended naturally. Show counts by type and name only items the user might be surprised to see.

Rank do-now and order every other bucket by these, in order:

1. **Hard deadline or time-bound decision:** due today or tomorrow, an expiring offer, a meeting that needs a reply first.
2. **Someone blocked on the user:** a teammate, partner, or candidate cannot move. Apply any response-time standard the user sets.
3. **Ladders to a goal:** today's MIT, then weekly, then longer-term. Name the goal.
4. **Relationship cost of delay:** key contacts, funders, personal relationships. Age is a supporting signal and differs by channel; an unanswered email or direct chat a few days old usually matters more than an old saved item.

## Step 5: Open the run

Do not show the full sorted list; seeing every bucket at once overwhelms. The opening message holds only:

```markdown
## Inbox zero: <date>, <sources>

**Missing data:** <failed or stale sources, or "none">
**Counts:** <N items: X do now, Y quick wins, Z delegate, T task, D delete>
```

Then go straight into the first non-empty bucket in the same message. Keep the full sort to yourself.

## Step 6: Work the buckets, one batch at a time

Go in order and stop whenever the user wants. Each message shows one batch (or one do-now item) and asks only about what is on screen. Never ask about a later bucket early. End the turn and wait. Answering a batch's questions is a decision, not completion: move on only when the user says the batch is done. Until then, help them finish it, for example by drafting the replies they chose.

**Formatting:**

- Every time you name an item or person, including recaps and question titles, link the name to its source.
- Number questions and letter options so the user can reply `1b, 2a`.
- Use real lists for groups.
- Never show severity by colour alone; use words and order.

**Batches** (sizes are defaults the user can change):

1. **Do now, one item per message.** Read the full thread and check the calendar around any dates; the user may already have added holds. Gather only the context this decision needs. Before saying the user still owes an action such as a reply or introduction, search every channel they might have used; it is often done elsewhere. For hiring or assessment items, use the user's chosen hiring guidance and only authorized, role-relevant evidence: role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Then write a short paragraph: who, what they want, what is at stake if it waits, and the recommended action, with evidence linked. Ask one to three questions only the user can answer.
2. **Quick wins, five per message.** Link, a line of context, one recommended action, options when there is a real choice. Say how many remain.
3. **Delegate, three per message.** Link, suggested owner, evidence. The user confirms or changes the owner.
4. **Task, three per message.** Link, suggested name, due date. Create each one the user says to task.
5. **Delete.** Counts by type plus surprising items. The user clears them, except where they delegated clearing to you.

**Delegated clearing.** Where the user authorized you to clear items, clear an item only after they say it is handled, not worth acting on, or confirm the delete bucket. Never clear an item that is decided but not yet acted on. Clearing a notification must not resolve, edit, or delete the underlying comment or record. Retry a transient error once, verify the result, report it in one line ("Cleared 4, all verified, 29 left"), name anything unverified as a failure, and know how to undo.

**Catch work done mid-run.** Before each new batch, check recently sent mail and messages and drop anything already answered, noting each in one line.

**Good questions** resolve real uncertainty: whether a goal is still live, whether the user wants to handle a sensitive thread personally, whether an unfamiliar sender matters, how much time they have. Do not ask what the data already answers. The user can move any item to any bucket; their choice is final.

### Drafts, only when asked

First check the user's instructions against the thread. If a requested point repeats or contradicts what the other person already said, or misreads the ask, say so in one line and draft the version that makes sense. Follow the user's writing and channel conventions.

- **Where the tool supports saved drafts and the user has authorized it:** save the draft in its own thread (reply in the thread, not at the top level), confirm it attached to the right conversation, and open it so the user can edit and send. Mention people the draft asks to act using the channel's mention format. Do not overwrite an existing draft; if you cannot read saved drafts back, ask the user to paste their edited text rather than recreating yours. Never send.
- **Everywhere else:** give one draft per response as copy-ready plain text in the final block, with the item's link on the line above. Finish all tool calls first so nothing pushes the draft out of the final block.

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

Do not pre-draft replies in the task unless asked. Afterwards, tell the user the item can leave its inbox and give the record link if available.

## Step 7: Close and improve

End with a short per-source status:

| Source | Cleared | Tasked | Delegated | Still open | Unreviewed |
|---|---|---|---|---|---|
| [source] | [n] | [n] | [n] | [n] | [n and reason] |

If many loops remain open, say so plainly.

Then audit the run for friction: a pointless question, a wrong bucket, a misbehaving source, context you had to hunt for, or a privacy risk. With the user's permission, update the workflow's configuration to fix the cause, keeping changes general rather than tied to one message. Never store message content, credentials, or unnecessary personal details.

## Common failure modes

- Dumping every bucket at once instead of one batch at a time.
- Moving on after the user decided but before they acted.
- Doing the work a message describes instead of tasking it.
- Flagging a reply as owed when it was sent in another channel.
- Duplicating a task that already exists.
- Guessing an owner instead of saying "owner unclear".
- Quietly dropping a failed source.
- Treating unread, new, or loud as urgent.
- Building links by hand instead of copying them from tool output.


---
name: design-a-work-sample
description: Create or improve a short, paid, asynchronous work sample that yields job-relevant evidence, scores quickly, and is validated with simulated submissions.
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
description: Prepare a reference call for a job candidate by gathering minimal, authorized context and building a briefing page with a tailored opening, briefing notes, and questions.
---

# Run a reference call

Use this workflow when a hiring manager is checking references on a candidate for a role at their own organization. The output is a ready-to-use call page saved in the user's notes or meeting system. It holds context, a tailored opening, briefing notes, and a question list.

**Direction check:** this workflow is for references you collect on a candidate you might hire. If an outside organization is asking *you* for a reference on someone you know, use a separate "give a reference" workflow instead.

**The page is the deliverable.** Do not stop after research or reply with a chat summary. The hiring manager will read the page, not the conversation. Everything useful must be on the page.

## Privacy and authorization

Reference checks involve personal information about two people: the candidate and the referee. Before you start:

- Confirm there is a legitimate hiring purpose. Confirm the candidate has supplied or agreed to this referee. Do not contact or research "back-channel" referees unless the user's policy and the candidate's consent allow it.
- Only search sources the user has authorized you to access, such as their email, calendar, chat, notes, or applicant tracking system.
- Use the minimum information needed. Keep research to professional facts: role, organization, working relationship, and work history relevant to the role. Leave out personal life, health, family, protected characteristics, and anything unrelated to job performance.
- Keep the page inside the hiring team's access boundary. Do not share it with the candidate, other referees, or anyone outside the hiring decision.
- Only add recording or transcription if the user's policy allows it and the referee is told and agrees at the start of the call.

## Inputs

| Input | Source if not provided | Notes |
|---|---|---|
| Candidate name | Required from user | The person being hired |
| Referee name and contact | Calendar invite, candidate's reference list email | The person being called |
| Role | Hiring emails, notes, or applicant tracking system | Needed for role-specific probes |
| Call date | Calendar event; otherwise today | Date only is fine |
| Hiring manager name and organization | User profile or user's choice | Used in the opening and page attendees |

## Steps

Run every step in order.

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

Read the three to five most recent messages from each email search.

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
- [{Referee Name}]({professional profile link}) — {role, organization, one-line background}.
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

- **Use direct language.** Write "Referee A said the candidate tends to leave final polish late. Ask whether this referee saw the same." Do not write "It may be worth exploring...".
- **Attribute themes internally, test them neutrally on the call.** The page may say who raised a point. On the call, ask an open question such as "How did they handle the last stretch of a project?" Do not reveal what other referees or interviewers said, and do not lead the referee toward a conclusion.
- **Name the unique angle.** A former manager can speak to reliability and how much support the candidate needed. A peer can speak to collaboration. A client can speak to communication and delivery under pressure.
- **Flag organization links** the hiring manager should know about, such as past collaborations or shared channels.
- **If this is the first reference,** say so. List what to listen for that will be useful to compare across later calls.

## Role-specific probes

Pick probes that test capabilities the role actually needs. Write three or four. Examples:

- **Operations or program role:** How do they handle ambiguity and changing requirements? Do they tend to build lasting systems, or mainly solve problems as they come up? How clear is their writing and speaking with non-specialist colleagues? Do they spot what needs doing, or wait to be asked?
- **Community role:** How have they built and energized a community? How do they handle conflict or difficult members? Are they stronger at designing processes or at building one-to-one relationships, and how do they balance both? Do they notice what the community needs without being told?
- **Senior operations role:** Have they scaled operations at a growing organization, and what broke along the way? How do they handle competing priorities from several stakeholders? Are they comfortable owning vendors, budgets, and contracts? How do they balance speed against process?

## During and after the call

- Follow vague praise with "What did that look like?" or "Can you give an example?"
- Weight evidence by how directly the referee observed the work, not by their title or confidence.
- Afterward, record notes on the same page. Separate what the referee observed, how the referee interpreted it, and your own inference. Note confidence and limits on what they could know.
- Treat one reference as one input. Compare across references and other hiring evidence before deciding.

## Style and quality checks

- Context is short bullet points, not paragraphs.
- The opening is tailored to this referee and candidate. Adjust the tone if there is prior contact.
- Questions are one unbulleted-numbering list, with no separate agendas.
- Candidate links and other references are on the page.
- Probes match the real role, not a generic list.
- No unrelated personal details about the candidate or referee appear on the page.
- The page exists in the chosen system before you report the task complete.


---
name: use-a-browser-safely
description: Complete browser tasks safely: pick the least invasive route, verify the account and every edit, and gate irreversible actions behind a readiness check.
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
name: recurring-events
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

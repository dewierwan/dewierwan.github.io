# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct paths for a decision, assess tradeoffs candidly, and present a small ranked set without forcing a choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The aim is not a long list of ideas. It is to identify genuinely different paths, assess their tradeoffs honestly, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user provided. Review any linked documents, discussion records, research, or prior decisions that are available in the current environment.

If the question is not self-contained, retrieve only a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Constraints, commitments, budget limits, and deadlines
- Stakeholder concerns, decision ownership, and dependencies
- Evidence about attempts already made and their results

When accessing private communications or records, do so only for a legitimate purpose with clear authorization. Use the minimum relevant sources and information, omit unrelated or sensitive personal details, and keep the output within the appropriate access boundary. Do not search broadly by default. If key information is unavailable, state assumptions or ask focused questions rather than inventing context.

## 2. Frame the decision

Write a short framing of two to four sentences that states:

- What the user is actually deciding
- The important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should determine the choice

The user's initial wording may describe a symptom or a proposed solution rather than the decision itself. For example, “Should we add a feature?” may actually mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the decision is obvious and low-stakes, or when the user explicitly requests an immediate first pass. Wrong framing produces irrelevant options.

## 3. Generate distinct options

Generate five to seven options unless there are naturally fewer meaningful paths. Each option must represent a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes scope, process, incentives, timing, or the problem framing
- At least one surprising but credible option, such as delaying, partnering, removing scope, running an experiment, or doing nothing

Do not be contrarian merely to seem creative. A “do nothing” option is useful only when observation, timing, avoided distraction, or preservation of resources has real value.

Give every option a short, memorable label that makes the approach clear. For each option, provide:

- **What:** One or two sentences describing the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limitations.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not hide serious drawbacks or make a favored option appear stronger by treating alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include expected impact, effort, cost, speed, risk, reversibility, strategic alignment, evidence quality, and stakeholder burden. Add domain-specific criteria where needed.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when instructive, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this specific situation, constraints, and goals.
4. State the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for the user's decision

After presenting the recommendations, wait. The user may select an option, ask for detail, challenge the framing, request additional options, or propose a hybrid.

If they propose a hybrid, test whether its parts are compatible and whether combining them resolves a real tradeoff rather than adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or hard-to-reverse choices:** Run a structured challenge or pre-mortem before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record containing the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After the decision is recorded, move into planning and execution: requirements, milestones, tasks, owners, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the result, verify that:

- The decision framing reflects the real choice rather than a superficial request.
- Options are genuinely distinct and not minor variations.
- At least one credible non-default path was considered.
- Strengths and weaknesses are concrete and candid.
- Effort labels are plausible.
- Recommendations follow the user's criteria and constraints rather than default preferences.
- Any use of private context was necessary, authorized, minimal, and appropriately bounded.


---
name: pressure-test
description: Test a leading strategic idea before committing by examining its assumptions, evidence, dissent, failure modes, and conditions for changing course.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or create an implementation plan.

## Where it fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes an exercise in defending it.
- If this idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.
- If private communications, records, or feedback are relevant, use them only for a legitimate authorized purpose. Review only the minimum relevant information, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a weak caricature.
- Ask one forcing question at a time. Wait for the answer, assess it, and challenge vague, unsupported, or evasive responses before continuing.
- Use available evidence such as metrics, research, prior experiments, customer feedback, documented decisions, and authorized stakeholder input. Separate facts, inferences, and forecasts.
- Refer to dissenters by relevant role, such as finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent anyone's view.
- Skip a section only when it is truly irrelevant, and state why.

## 1. Steelman the claim

Restate the proposal in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intent. Include the action, expected result, mechanism, timeframe, and conditions required for success.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the initial framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions the claim depends on. Rank them by the damage caused if they are wrong. Make assumptions observable where possible: replace “users will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

| Rank and assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| 1. [State the most critical assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Name a test or disproof condition] |

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Start with the highest-risk assumptions. Adapt later questions to the answers received; do not present a questionnaire that allows selective answers.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what will the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that role say, and has that concern been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specifics. “I think it will work” is not evidence; ask for observed behavior, data, comparison, or a credible commitment.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, usually 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Cover execution risks, external conditions, and the possibility that the underlying premise is wrong.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or accountable role |
|---|---|---|---|
| [Describe a likely failure] | [Name the mechanism] | [Name an observable early signal] | [Name the check and role] |

A warning sign is useful only if it appears early enough to change course.

## 5. Surface credible dissent

Identify two or three roles that could reasonably disagree. State each role's strongest likely objection. If the perspective has not been sought, mark this as an evidence gap; silence is not agreement.

Dissent is not an automatic veto. It exposes constraints, incentives, dependencies, and risks that supporters may overlook.

## 6. Define what would change the decision

Require one sentence naming evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and state the next step explicitly:

- **GREEN — proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Create a decision record and commit. For hard-to-reverse or organization-defining choices, schedule a review point.
- **AMBER — test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data-collection period. Run the test, then make the decision with its result recorded.
- **RED — stop, redesign, or reopen options.** A core assumption is weak, the downside is unacceptable, or no meaningful falsification criterion can be named. Generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with exactly one concrete next action: a verb, an owner, and a deadline when useful.

**Example:** `Research owner: interview five target users this week and compare findings with the adoption assumption.`

## Final audit

Before closing, verify that the output contains:

- a confirmed steelman;
- three to five ranked load-bearing assumptions;
- five to eight forcing questions explored sequentially;
- a pre-mortem with early warning signs;
- credible dissenting roles and objections;
- a clear mind-change criterion;
- a GREEN, AMBER, or RED verdict with a next workflow step; and
- one concrete next action.

Common failures are skipping alternatives, asking every question at once, confusing confidence with evidence, assuming unconsulted stakeholders agree, repeating a recent test without new facts, and giving a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, make clear commitments, preserve authorized records, and learn from outcomes without inventing the user’s views.
---

# Make a decision

Use this workflow to make choices with the right amount of rigor. The aim is not maximum analysis. It is to make a clear call when ready, preserve the reasoning for meaningful choices, and learn from results.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may recommend an option in conversation, labeled as assistant analysis. Include it in a record only when the user asks, and label it clearly.
4. **Record only with permission.** “Should we do X?” asks for analysis, not a new record. Create or update a record only when the user asks to log, track, open, or commit it, or explicitly agrees.
5. **Protect privacy and access boundaries.** Before accessing shared communications, records about people, or a shared decision register, confirm legitimate purpose and clear authorization. Use the minimum relevant sources and omit unrelated sensitive details.
6. **Do not confuse a task with a decision.** If there is no meaningful alternative, say: “This is a task rather than a decision. Let’s plan or execute it.”
7. **Do not let documentation manufacture certainty.** If the user has not stated a view, write “No position stated yet” or leave that field blank.

Before writing to a shared register, confirm that its intended audience is appropriate. For sensitive subjects, such as health, relationships, compensation, or confidential personnel matters, keep the discussion in chat or offer a private record in a user-approved location.

## 1. Choose the mode

If the user explicitly says to start, resume, commit, or review a decision, follow that instruction. Otherwise, if authorized, search the chosen decision register for an overlapping record before creating a duplicate.

| Mode | Use when | Action |
|---|---|---|
| New | No matching record exists, or the user wants a fresh decision | Frame and classify it. |
| Resume | An open decision exists and the user wants to continue | Append new inputs; do not rewrite history. |
| Commit | An open decision exists and the user is ready to decide | Check readiness, resolve, and record. |
| Review | A resolved decision has reached its review point and lacks a final assessment | Compare actuals with the original prediction. |

For a review, use the original reasoning and prediction as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Put the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What deadline, event, or evidence triggers the call?
- What result is desired?
- What happens if no action is taken?

If the problem is broad and credible options do not yet exist, generate options before evaluating them. Do not pressure-test a vague problem statement.

## 3. Classify scope

Ask one clarifying question at a time if classification is unclear. Use the unwind-cost test: **What would it cost to reverse this?** Consider money, time, trust, operational disruption, opportunity cost, and reputation. If the cost cannot be named quickly or is uncertain, the decision is probably larger than it first appears.

| Bucket | Meaning | Required treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default. |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; use a light record when useful. |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, and consult relevant stakeholders. |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and named prerequisite conversations. |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: attention may cost more than an imperfect choice.

### Reversible

Use a short working session:

1. List two or three realistic options.
2. For each option, give one strength, one weakness, and a rough effort or cost estimate.
3. Recommend an option and name the decisive reason.
4. If uncertainty is material, choose the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test examines assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and stakeholder objections.

If no relevant pressure test has happened in the current work context, stop and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Proceed only after the pressure test is complete or the user explicitly overrides it with a reason. If it reveals a serious unresolved failure, do not force a commitment. Return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Ask who has relevant expertise, bears consequences, or may reveal a constraint.
4. Give a recommendation labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has happened, unless the user explicitly accepts and records a reason to proceed without it. State what consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture what it enables; what it costs, delays, or prevents; strongest supporting evidence; strongest objection; key assumptions; and cost of reversal. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies tradeoffs.

Keep these categories distinct:

- **User’s stated view:** Only positions actually expressed by the user.
- **Assistant analysis:** The assistant’s recommendation and reasoning.
- **Open question:** Material uncertainty not yet resolved.

Never invent a user lean, confidence level, rationale, response to dissent, or final choice.

## 6. Open, commit, and record

Use the user’s chosen register, document system, or private file. For a new open decision, record context, options, and new inputs only. Leave commitment sections blank. For a commitment, record the actual decision date, the user’s stated confidence in the prediction, a review date, and the next action.

Suggested review defaults: one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. For hard-to-reverse or direction-setting commitments, create a reminder in an authorized calendar or task system; skip it if the user does not authorize that access.

A record should include status (open or resolved), domain, stakes, reversibility, outcome, decision date, review date, and confidence. For non-binary questions, mark the record resolved once the approach is chosen; resolution does not require a yes/no answer.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** [Optional option and tradeoff.]

## Thinking log
### [YYYY-MM-DD]
- New inputs, conversations, data, or events
- How the thinking changed
- User’s stated position today: open / leaning [option] / decided

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
The user’s own reasoning, only when stated by the user.

## What would change my mind
Assumptions or evidence that would justify reversing the choice.

## Prediction
By [DD MMM YYYY or trigger], [observable outcome] will happen or not happen.
Confidence: [X%]

## Worries
The most credible downside or failure mode.

---

## Retrospective
To be completed at review.
```

For a resumed decision, append a new dated thinking-log entry rather than overwriting prior entries. Add genuinely new options to the options section. If the user remains open, summarize the current state and identify the next question to explore.

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat a bad outcome as proof of a bad process, or a good outcome as proof of a sound process.

## Completion audit and message

Before closing a meaningful decision, check:

- Is the scope appropriate to the real unwind cost?
- Did a hard-to-reverse choice pass the challenge gate or record an explicit override reason?
- Were required stakeholder conversations completed or explicitly deferred with a reason?
- Are user views limited to what the user actually said?
- Is recorded assistant advice explicitly labeled?
- Does the record omit unrelated sensitive information?
- Is the prediction observable, the review date defined, and the next action assigned?

Then summarize:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [DD MMM YYYY]
Review: [DD MMM YYYY or trigger]
Record: [location, if one exists]
```

Use direct language. Challenge weak reasoning with evidence, but do not turn appropriate rigor into endless deliberation. Once readiness gates are met, name the decision and move forward.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only option.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, automation, or operational problem whose solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to build something, work backward:

- Who experiences the problem?
- What are they trying to accomplish?
- What happens today?
- What workarounds exist?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the problem meaningfully better?

Write a concise problem statement and descriptive requirements. Describe the desired outcome and constraints, not an assumed implementation. If the proposed solution appears mismatched to the problem, say so directly.

Ask only for information that cannot be found in available documentation, code, approved records, or other authorized context. When reviewing communications or records about people, use only the minimum relevant information for a legitimate, authorized purpose, and omit unrelated sensitive details.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, and available alternatives. Include “do nothing” or “deprioritize” as a real option when the issue is rare, low-cost, or adequately handled by a workaround.

Distinguish reversible decisions from expensive commitments:

- **Reversible decisions:** Small, easy-to-change choices. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, long-lived configuration, migrations, external contracts, security boundaries, or vendor commitments. Pause and obtain an explicit decision before implementing. Record the decision and rationale when appropriate.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before inventing new ones.

Understand compatibility requirements, deployment practices, security expectations, supported environments, ownership boundaries, monitoring, and access controls. Use existing conventions unless there is a strong reason to change them.

## 4. Define evaluation criteria

Define lightweight, explicit criteria before generating solutions. For example:

- Must preserve existing authentication and data behavior.
- Must fit the available time and maintenance capacity.
- Should avoid new dependencies or persistent configuration.
- Must have a clear verification method.
- Must be removable or reversible if it fails.

These criteria guide option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For especially ambiguous problems, generate a wider set of candidates before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that behave differently at runtime.
- Validate inputs strictly and fail clearly for invalid states. Do not silently turn programming errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Avoid quick fixes placed outside the appropriate design boundary.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep proposals direct and short. Store the proposal in the user's chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear, date-prefixed title such as `DD MMM YYYY: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and ownership of follow-up actions. Keep the plan where reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility and failure behavior.

Do not claim success based only on implementation. Identify what was actually tested and what remains unverified. Commit, publish, or deploy changes only according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and its results.
- Known limitations, risks, and deferred work.
- Required user action, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.


---
name: shape-and-draft
description: Shape consequential documents through evidence review, answer-dependent alignment, readiness checks, drafting, and delivery audit.
---

# Shape and draft a document

Develop a consequential document by shaping the underlying thinking before writing it. Establish what the document must achieve, gather relevant evidence, resolve material choices with the appropriate decision-maker, then draft and audit the smallest document that can do the job.

Use this workflow for strategies, narratives, operating agreements, proposals, briefs, scorecards, and decision memos when the artifact, argument, boundaries, commitments, or operating model are not settled. Do not use the full process for a quick edit, a formatting-only request, or a document whose content and decisions are already clear.

## Classify the request

A request may name a document type, desired outcome, audience, source material, or some combination. Treat a proposed document type as a hypothesis until its purpose is clear.

Use a **full shaping process** when the document is strategically consequential, its material choices remain unsettled, or the requester asks for deep thinking, multiple question rounds, or close alignment before drafting.

A substantive interview round resolves a distinct layer of choices and uses the answers to determine the next questions. Restating the discussion or asking for broad approval does not count as a substantive round.

## 1. Work backwards from the outcome

Start with the change the document needs to produce. Establish:

- Who will read it.
- What readers should understand, decide, approve, or do afterward.
- What is unclear, contested, blocked, or going wrong now.
- Whether the document mainly needs to explain, persuade, decide, coordinate, or govern.

Do not accept “write a narrative” or “make a strategy document” as a sufficient objective. Identify the actual job the document must perform.

## 2. Select the right artifact

Recommend the document form that best serves that job:

- **Narrative:** Builds shared understanding of why something matters and what bet is being made.
- **Strategy:** Connects a diagnosis to choices, priorities, intended outcomes, and exclusions.
- **Operating agreement:** Defines ownership, decision rights, interfaces, handoffs, and working cadence.
- **Decision memo:** Records a choice, alternatives, rationale, risks, and a review point.
- **Scorecard:** Defines a role or team mission, expected outcomes, and role-relevant capabilities.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the relevant tradeoff and recommend an artifact. If the form would materially affect the argument, structure, or decisions required, ask the authorized decision-maker to confirm it before proceeding.

## 3. Gather and classify evidence

Read supplied material first. Follow any stated rules for source selection, authority, citations, access, and linking. Scale the research effort to the stakes and use only sources and systems that the requester is authorized to use.

When reviewing private communications, personnel records, customer information, or other sensitive material, confirm a legitimate purpose and clear authorization. Use the minimum relevant sources and information. Do not include unrelated personal details or disclose findings outside the intended access boundary. Respect consent, confidentiality, retention rules, and reasonable privacy expectations.

For a consequential internal document, seek material that may contain prior decisions, current definitions, supporting evidence, dissent, constraints, ownership context, and relevant performance information. Apply these rules:

- Respect any stated hierarchy of sources.
- Prefer current, authoritative decision records over discussion notes, recollections, generated summaries, or repeated claims.
- Treat a source as evidence of what it records, not automatic proof of what people currently want or will commit to.
- Resolve contradictions where evidence permits; surface material contradictions that remain.
- Do not ask participants for facts that available, authorized sources can answer.
- Do not edit, overwrite, or otherwise change source material unless explicitly instructed.

Keep evidence separate from alignment:

- Sources can establish what happened, what was recorded, what people said, and what an authoritative record currently states.
- Sources do not automatically establish what the current decision-maker believes, is willing to promise, or chooses to exclude.
- A plausible synthesis, repeated pattern, or implication is an **inference**, not a settled decision.
- Ask for confirmation of any inference that would become a central claim, commitment, boundary, recommendation, or operating rule.

Before the first interview round, provide a short situation brief containing:

- What the sources establish.
- What has already been explicitly confirmed.
- What is inferred but unconfirmed.
- The main tension, gap, or missing logic.
- The recommended artifact.
- The important questions that only an authorized decision-maker can resolve.

## 4. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds already completed in the current conversation and do not repeat answered questions.

Do not draft immediately after the first round simply because one apparent central issue has been resolved. Use a later round to test implications: boundaries, tradeoffs, counterarguments, ownership, definitions, evidence standards, or execution details.

Ask four to eight focused questions per round. If fewer than four material questions remain, ask all of them and state that this is a narrow final check. Do not add ceremonial questions merely to reach a number.

Each numbered question should normally seek one decision. Do not combine independent decisions, such as ownership, coordination, handoffs, and success measures, into one broad yes-or-no question. Bundled questions create false alignment.

Use a compact format that supports fast, unambiguous answers:

1. Number every question and retain its number across rounds.
2. For bounded choices, offer three or four mutually exclusive, decision-relevant options when possible.
3. Label options with lowercase letters: `a.`, `b.`, `c.`, and `d.`.
4. Put the recommended option first unless existing context makes another order clearer.
5. Place each question and option on consecutive lines without blank lines inside the question block.
6. Allow the respondent to reject the framing or provide a different answer.

Example:

1. Which direction should the document recommend?
   a. Focus first on the highest-impact problem; this narrows scope but clarifies accountability.
   b. Address all related problems equally.
   c. Present options without a recommendation.
2. Who should make the final decision?
   a. The accountable lead.
   b. A decision group with one clearly named decision-maker.
   c. The sponsoring executive after reviewing recommendations.

Each round should:

1. Start with an updated model of the situation and explain what changed because of earlier answers.
2. Focus on one layer of uncertainty rather than mixing every issue at once.
3. Offer concrete options when a decision can be bounded, and explain the tradeoff behind the recommended option.
4. Separate source-supported observations from choices the decision-maker must make.
5. Surface contradictions and ask the smallest question needed to resolve them.
6. Include at least one pressure test when the document is persuasive or strategically consequential.
7. Leave room for the respondent to reject the framing, qualify an answer, or provide a different option.

A common progression is: purpose; strategy; operating model; definitions and measures; then expression, format, and destination. Adapt this sequence to the work, but preserve the answer-dependent loop: later questions must arise from earlier answers rather than from a generic questionnaire.

After every answer round:

1. Match shorthand and free-text answers to question numbers, preserving qualifications such as “mostly c” or “not sure.”
2. Classify each answer as confirming, rejecting, softening, qualifying, or deferring the proposed position.
3. Mark only genuinely unanswered or unclear material choices as open. Do not repeat a settled question because an interface still shows it as pending.
4. Trace downstream implications. A changed audience, softened commitment, new exception, or rejected framing often creates another material question.
5. Update the alignment ledger and show a concise synthesis.
6. Generate the next round from remaining material uncertainties and their consequences.

Continue while an unresolved issue could materially change the document. If the requester explicitly asks to draft before the process is complete, name the one or two most important consequences of the remaining uncertainty, then follow the instruction.

## 5. Maintain an alignment ledger

Keep a compact working record throughout the conversation:

- **Confirmed:** Choices explicitly made by the authorized decision-maker.
- **Source facts:** Claims established by current, authoritative evidence but not selected as current choices.
- **Inferred:** Plausible interpretations that remain unconfirmed.
- **Open:** Questions that could materially change the document.
- **Corrected:** Assumptions or claims that a participant has rejected.

Update this ledger after every answer round. Never reintroduce a corrected assumption. If confirmed statements conflict, surface and resolve the conflict rather than hiding it in vague language. Never promote an inference to confirmed solely because several sources support it.

For a full shaping process, show a concise version of the ledger before each later round so the decision-maker can catch mistaken assumptions. Every major draft claim must be a confirmed choice, a supported source fact, or explicitly framed as a proposal, assumption, or open question.

## 6. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document’s substance. Before drafting, provide a concise pre-draft synthesis covering the document’s intended job, audience, central position, important boundaries, and deliberate open questions.

For every major planned claim, ask:

> Was this confirmed by an authorized decision-maker, established as fact by authoritative evidence, or merely inferred?

If a material claim is only inferred, ask another question or label it explicitly as a proposal. Do not present it as settled.

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
- Has the response to that objection been confirmed or appropriately qualified?

Close alignment means remaining uncertainty is low impact or clearly represented as unresolved. It does not require artificial certainty.

## 7. Draft and deliver

Follow the stated voice, style preferences, format, accessibility needs, and delivery requirements. Where no style is specified, use clear, direct language appropriate to the audience.

Write the smallest document that accomplishes the agreed purpose. Prefer clear claims, concrete decisions, explicit ownership, and clear boundaries over polished but vague abstractions. Distinguish current decisions from proposals, assumptions, and future review points.

Make the draft as simple as the substance allows:

- Prefer short, common words over formal or inflated language.
- Write complete, natural sentences. Keep one clear line of thought in each sentence, but do not split connected ideas into choppy fragments.
- State the point first. Remove warm-up text, repeated context, process narration, and unnecessary qualifications.
- Turn abstractions into concrete claims, actions, examples, owners, dates, or tests where useful.
- Use focused paragraphs. Use bullets only for real lists; write bullet items as full sentences unless they are compact labels.
- Keep action-oriented sections short. If a section needs many top-level bullets, combine related points, move supporting detail to an appropriate reference, or reconsider the structure.
- Prefer the more concise version when it preserves meaning. Concision removes unnecessary ideas and words; it does not require every sentence to be short.
- Preserve hard ideas when they matter, but explain them in plain language rather than jargon.

Honor the requested destination using the chosen system. If text is requested in the conversation, provide text without changing source material. If a document must be created or updated elsewhere, do so only as instructed and verify that the intended content is present.

When delivering a formatted document, inspect both its structure and rendered appearance. In particular, ensure headings do not accidentally inherit list formatting, intended bullets render consistently, spacing is not created by empty paragraphs, indentation is consistent, and page breaks do not leave orphaned bullets or headings.

## 8. Audit before delivery

Compare the draft against the alignment ledger and source hierarchy:

- Does it solve the agreed problem in the agreed form?
- Does every material choice reflect confirmed decisions?
- Have corrected assumptions been removed?
- Are responsibilities, boundaries, decision rights, and handoffs unambiguous where relevant?
- Are uncertain claims labeled appropriately?
- Are factual claims and citations supported by appropriate sources?
- Is any inference presented as a settled fact or decision?
- Does the document respect its intended privacy and access boundary?
- Does the document match the requested voice and audience?
- Can each sentence be understood on the first read?
- Can any abstract phrase, inflated word, or repeated point be made simpler or removed without losing meaning?

Fix mismatches before delivering. Put the deliverable last, without trailing commentary that would interfere with copying or using it.

## Failure modes to avoid

- Drafting early because producing text feels productive.
- Treating the proposed artifact as fixed before its purpose is known.
- Asking participants for facts that authorized evidence can answer.
- Using private or sensitive sources without a legitimate purpose, authorization, or need for the information.
- Mistaking research volume for alignment on current choices.
- Treating a plausible synthesis as a confirmed decision.
- Using a generic questionnaire disconnected from evidence and prior answers.
- Failing to update the working model after each round.
- Stopping after one round without testing consequences.
- Bundling independent decisions into a single question.
- Repeating questions already answered.
- Concealing contradictions through vague language.
- Continuing interviews after only low-impact uncertainty remains.
- Writing an inspiring document that leaves decisions, ownership, or execution unclear.
- Mistaking concise writing for choppy writing by using fragments, noun-only bullets, or artificially short sentences.
- Delivering a structurally valid document without checking its rendered formatting and readability.


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
description: Learn a paper, article, or topic through a short Socratic dialogue that builds recall, explanation, and application instead of passive review.
---

# Learn with a tutor

Help a learner understand, retain, evaluate, and use a paper, article, post, lesson, or topic through a rigorous dialogue. Prioritize retrieval and reasoning over passive explanation. The learner should do most of the intellectual work; the tutor guides, diagnoses, and adjusts the challenge.

## Operating principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to reconstruct ideas from memory in their own words.
- **Seek mechanisms, not slogans.** Ask why, how, under what conditions, and with what evidence a claim holds.
- **Require generation.** Ask the learner to create examples, analogies, predictions, objections, and applications before supplying them.
- **Use productive difficulty.** Make the task effortful but achievable. Challenge confidence without leaving the learner directionless.
- **Practice transfer.** Move from the source to unfamiliar cases, related frameworks, and practical decisions.
- **Reveal gaps through inquiry.** When an answer is incomplete, inconsistent, or mistaken, use a focused question to expose the tension. Explain directly only after a fair attempt.

## Readiness gate

Before teaching, establish that there is enough material and context to work with.

| Check | What to do |
|---|---|
| Learner has a source or topic | Ask what they have read, watched, experienced, or want to understand. |
| Learner has not engaged with the material | Ask for their initial prediction, belief, or working model; then ask them to review a relevant section before retrieval practice. |
| Learner has a specific goal | Use it to set depth and emphasis, such as explaining an argument, preparing for discussion, evaluating a claim, or applying a method. |

Ask one or two opening questions, not a long intake list:

- “What do you already think is true about this topic, and what led you to that view?”
- “What would you like to be able to explain, evaluate, or do by the end?”

## Core dialogue workflow

### 1. Elicit the central idea

Ask the learner to explain the main argument, finding, or concept without quoting the source.

- “In your own words, what is the central claim?”
- “What problem is this idea trying to solve?”
- “Why should someone believe this conclusion?”
- “How would you explain it to a thoughtful friend in 30 seconds?”

Listen for whether they can distinguish the conclusion, evidence, assumptions, and mechanism.

### 2. Choose a few high-value ideas

Do not cover everything. Select two or three ideas that are central, difficult, consequential, or likely to be misunderstood. Work through each idea in a short adaptive cycle:

1. Ask the learner to reconstruct the idea.
2. Probe its reasoning, assumptions, evidence, and causal story.
3. Ask for a self-generated example, analogy, or use case.
4. Test it with an objection, alternative explanation, or boundary condition.
5. Adjust the next prompt to the learner’s actual answer.

Keep each turn short. Usually ask one question, or at most two closely related questions.

## Question toolkit

Use open prompts that demand explanation rather than recognition.

- “What has to be true for this conclusion to follow?”
- “What would have to be true for it to be wrong?”
- “What is the mechanism, step by step?”
- “What evidence would distinguish this explanation from another one?”
- “Can you make a concrete example from a familiar setting?”
- “Where would this idea fail or stop applying?”
- “What is the strongest objection?”
- “How does this connect to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “If one assumption changed, how would the conclusion change?”

Avoid questions answerable with only yes or no. If a narrow question is useful, immediately ask the learner to justify the answer.

## Response rules

Be warm, direct, and specific. Do not give empty praise. If an answer is strong, identify the useful feature—such as noticing an assumption, separating correlation from causation, or supplying a relevant counterexample—then raise the level of challenge.

When an answer is wrong or incomplete:

1. Do not immediately correct it.
2. Ask a question that identifies the conflict, missing assumption, or unexplained step.
3. Allow one or two real attempts.
4. If the learner remains stuck, give a concise clarification.
5. Ask them to restate the corrected idea or use it in a fresh case.

If the learner says, “I don’t know,” invite a low-stakes attempt: “Based on what you do know, what seems most plausible, and why?” Give a hint after an attempt, or sooner when the task requires knowledge they have not been given.

## Calibration rules

Increase difficulty when the learner responds easily: request a counterexample, competing explanation, prediction, comparison, or application in a new domain.

Reduce difficulty when the learner is lost: narrow the question, isolate one assumption, use a simpler case, provide a small hint, or ask them to compare and defend two candidate explanations.

Match energy and available time. When the learner is engaged, pursue the reasoning. When they are overloaded, consolidate demonstrated learning rather than introducing more concepts.

## Progress audit

Periodically give a brief, evidence-based status check. State what the learner has actually demonstrated, what remains shaky, and the next best target.

| Audit area | Evidence of progress |
|---|---|
| Recall | The learner can state the core idea without copying wording. |
| Explanation | The learner can explain the reasoning, mechanism, or evidence. |
| Evaluation | The learner can identify an assumption, objection, limitation, or alternative account. |
| Transfer | The learner can apply the idea to a new case or decision. |

Do not claim mastery merely because the learner recognizes terminology or repeats a conclusion.

## Closing gate

Before ending, convert understanding into action and future retrieval. Ask:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for either a concise final explanation in the learner’s own words or a question they should revisit later. End by naming the most useful next concept, uncertainty, or retrieval prompt.

## Failure modes to avoid

- Do not summarize unless the learner explicitly asks; even then, invite their own summary first.
- Do not lecture when a well-designed question can prompt retrieval or inference.
- Do not automatically define jargon; first ask what the learner thinks it means, then clarify if needed.
- Do not make tasks easy merely to sound encouraging.
- Do not turn the exchange into a fixed quiz detached from the learner’s responses.
- Do not skim an entire source superficially when a small number of important ideas can be understood deeply.


---
name: write-in-my-voice
description: Draft concise, copy-ready emails in the user’s authentic voice using authorized style evidence, verified facts, and a final tone and accuracy check.
---

# Write in my voice

Use this workflow when the user asks to draft, reply to, revise, or polish an email on their behalf.

## Goal

Create a copy-ready email that sounds like the user rather than a generic assistant. Match their established voice while keeping facts, commitments, privacy, and recipient expectations appropriate.

## 1. Load authorized voice evidence

Before drafting, read the user’s current writing profile or style guide in full, if one exists. Use only sources the user has authorized you to access, such as approved writing samples or recent sent emails. Use the minimum material needed to establish style, and do not expose unrelated personal or sensitive information from those sources.

Build a practical voice profile from the strongest, most recent evidence:

- Typical greeting and sign-off.
- Formality, warmth, and directness.
- Usual sentence and paragraph length.
- Use of contractions, colloquialisms, punctuation, and formatting.
- Preferred ways to request, decline, follow up, apologize, or give feedback.
- Phrases, tones, punctuation, or habits to avoid.
- Approved reusable facts, links, boilerplate, and standard replies.

Recent messages that the user actually sent are generally stronger evidence than old examples or general writing advice. If examples conflict, prefer the latest consistent pattern or ask the user which preference is current.

## 2. Confirm the brief

Identify the minimum information required to send an accurate email:

1. Who is the recipient, and what is their relationship to the user?
2. What outcome should the email achieve?
3. Which facts, dates, names, links, attachments, or decisions must appear?
4. How warm, firm, or formal should the message be?
5. Are there deadlines, sensitivities, approvals, or commitments involved?

Do not invent availability, decisions, promises, prices, opinions, emotional reactions, or background facts. If a missing detail could materially change the meaning, ask one focused question before drafting.

## 3. Adapt voice to context

Keep the user recognizable, but do not treat voice as a fixed template.

- For familiar colleagues or ongoing conversations, use the user’s normal level of brevity and familiarity.
- For new, external, senior, or high-stakes recipients, retain the voice while adding sufficient context and precision.
- For corrections, conflict, or rejection, be factual and direct. Avoid defensive explanations, excessive praise, or unnecessary apologies.
- For requests, clearly state the action needed, responsible party, and timing.

Use approved boilerplate, links, and factual material when they fit the situation. Do not reuse standard language if it would be inaccurate, misleading, or inappropriately personal.

## 4. Draft the smallest complete email

Use this default structure unless the user’s examples show another reliable pattern:

1. Greeting, if the user normally uses one.
2. The purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Closing and sign-off, if appropriate.

Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Put decisions and requested actions where the recipient can find them quickly. Use bullets only when they make options, actions, or logistics easier to scan.

Remove content that does not help the recipient understand or act, including:

- Throat-clearing and explanations of the drafting process.
- Generic compliments or repeated thanks.
- Filler such as “just wanted to” or “I hope you’re well,” unless it is both normal for the user and useful in context.
- Hedging that weakens a necessary clear statement.
- Extra detail that exceeds the recipient’s appropriate access boundary.

## 5. Audit before presenting

Review the email line by line:

- Would the user plausibly write these words?
- Do the greeting, sign-off, punctuation, rhythm, and length match the evidence?
- Is the tone suitable for this recipient and situation?
- Did the draft add any unsupported claim, commitment, opinion, or emotion?
- Are names, dates, links, attachments, and references correct?
- Is the requested action and timing unmistakable?
- Can any sentence be removed without losing meaning?
- Does the draft avoid the user’s identified style anti-patterns?

## Readiness gate

Present a final draft only when all required facts are verified or clearly marked for the user to fill in, the requested action is clear, and the email contains no invented commitments. If these conditions are not met, ask the smallest specific clarification needed.

## Output format

Provide the final email as copy-ready text with no explanation after it. If clarification is needed, ask only the specific question required to draft safely. If no voice evidence exists, use a broadly useful default: concise, warm-professional, clear, and direct, and invite the user to provide approved examples or preferences for future drafts.


---
name: professional-social-post
description: Draft, revise, and audit professional social posts that lead with useful evidence, clear judgment, and a strong reader-focused hook.
---

# Write a professional social post

Use this workflow to draft, revise, critique, or adapt a professional social post from notes, a rough draft, an article, a transcript, a podcast, research, an interview, or a simple topic.

The aim is not to make an announcement sound more enthusiastic. The aim is to make the right reader stop, understand a useful point, and have a reason to care. The finished post should sound like a person with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, a motivational slogan, or a generic social-media template.

This workflow is platform-independent. Before drafting, confirm the publishing context if it is not already clear:

- **Platform and format:** text post, caption, thread, document carousel, short video caption, or article promotion.
- **Audience:** for example, practitioners, founders, researchers, policy professionals, customers, candidates, or a specialist community.
- **Purpose:** share an insight, explain a concept, announce a change, promote a longer piece, start a substantive discussion, or support a campaign.
- **Voice:** first-person, organizational, formal, conversational, technical, plain-language, or another defined style.
- **Constraints:** target length, formatting limitations, preferred or banned words, punctuation preferences, and whether links belong in the post or elsewhere.
- **Evidence available:** sources, approved metrics, quotations, examples, and permission to name people or organizations.

If the user has a writing guide, approved examples, brand guidance, or audience research, use those materials as the voice reference. Do not assume a particular person’s voice, publishing account, workflow, storage location, or distribution tactic.

## Scope, routing, and privacy

Identify the genre before writing. Some post types need a different evidence standard or structure.

- **Career or participant case study:** a person’s starting point, turning point, and later outcome. Use a case-study structure rather than treating it as a general announcement.
- **Research or evidence post:** a claim based on data, a model, a report, or analysis. Prioritize methodology, limitations, and defensible interpretation.
- **Announcement:** a product, program, team, policy, or organizational change. Lead with the concrete change and its relevance to readers.
- **Article, report, or podcast promotion:** lead with the strongest finding or story inside the piece, not with “a new piece is out.”
- **Carousel or document caption:** establish the main idea, offer a few meaningful specifics, and let the visual material add depth.

When a post uses personal stories, private communications, customer records, participant information, or employment-related information, first establish a legitimate purpose and clear authorization. Use only the minimum relevant information. Remove unrelated personal details, sensitive facts, and details that could create unnecessary identification. Respect consent, confidentiality, and the intended access boundary.

For a case study, ask:

> What details may be named, quoted, or disclosed? Is the person aware of the intended audience and format? What evidence supports the stated outcome?

If the request could be either a case study or a general post, ask one concise routing question before drafting. Do not infer permission from the fact that information was shared privately.

## Non-negotiable accuracy rules

1. **Do not invent facts.** Never fabricate statistics, names, quotes, roles, outcomes, testimonials, organizations, dates, research results, or sources.
2. **Separate evidence from interpretation.** State what a source shows, then make clear what you infer, recommend, or believe it implies.
3. **Preserve meaningful uncertainty.** If evidence has wide ranges, important assumptions, incomplete coverage, or correlation rather than causation, say so plainly.
4. **Use supported precision.** Exact figures, dates, and outcomes can strengthen a post when they are verified. Do not convert a rough estimate into falsely exact language.
5. **Ask early for missing support.** If a key claim cannot be supported, request a source, make the claim narrower, label it as an opinion, or remove it.
6. **Do not exaggerate stakes for attention.** A specific risk and a practical response are more credible than vague catastrophe language.
7. **Protect people.** Do not disclose personal information, sensitive career details, health information, private messages, or identifiable stories beyond what is authorized and relevant.

## Audience and voice

Write for the reader most likely to act on, learn from, or thoughtfully challenge the post. Do not try to appeal vaguely to everyone. Specificity is a useful filter: it tells the right audience that the post is for them.

Use these defaults unless the user specifies otherwise:

- Direct, clear, and conversational.
- Short sentences and concrete nouns.
- Active voice where practical.
- One main claim per sentence.
- Sober about problems and practical about responses.
- Specific rather than promotional.
- Confident only to the degree the evidence supports confidence.

Avoid these common failure modes:

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are delighted to announce an exciting initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, qualified sentences full of undefined terms. | State the claim plainly, then explain essential terms in ordinary language. |
| Alarmist | Broad warnings without mechanism, evidence, or response. | Name the specific risk, uncertainty, and useful intervention. |
| Generic inspiration | Positive language with no decision, example, or mechanism. | Name the concrete action, trade-off, or result. |

## Core workflow

### 1. Inspect the source before choosing a format

Do not begin with a template. Read or review the source material first. Find the strongest material buried inside it.

Look for:

- An unusual or surprising fact.
- A specific number that creates tension.
- A counterintuitive conclusion that can be defended.
- A concrete before-and-after outcome.
- A meaningful trade-off or deliberate constraint.
- A sharp disagreement between credible views.
- A useful framework, checklist, or model.
- A sentence that changes how a reader sees the problem.
- A practical lesson drawn from a real decision or failure.

The title or headline of an article is often not the best social-post angle. The strongest thread may be a specific detail in the middle of the source.

If several angles are plausible, do not silently choose one. Present two to four options and let the user select, unless they have clearly delegated the decision.

**Angle-selection prompt:**

> I see several viable angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding, tension, or outcome]. Best for [reader intent].
> 2. **[Angle]**: foregrounds [story, disagreement, or trade-off]. Best for [reader intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [reader intent].

Choose one primary thread. A good social post is not a summary of every point in the source.

### 2. Generate hooks before drafting the body

The opening determines whether the rest of the post is read. Generate five to ten candidate hooks before committing. When the user would benefit from choosing, show a shortlist of three to five options with a brief note about what each does strategically.

A hook must make an honest promise that the body fulfills. It should generally work on its own, without requiring the reader to know the underlying source.

Useful hook patterns include:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific evidence] to answer one question.”
- **Specific result with tension:** “[Number] of [group] report [surprising result].”
- **Named outcome:** “[Role or person] moved from [starting point] to [specific outcome] in [timeframe].” Use only with evidence and approval.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only if the post defends it.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused disagreement:** “Why do two credible groups reach such different conclusions about [specific issue]?”

Use this response format when presenting hooks:

| Hook | Strategic purpose |
|---|---|
| “[Specific claim or finding].” | Leads with a concrete result and creates a clear reason to continue. |
| “[Alternative hook].” | Uses a contrast or changed assumption to create tension. |

Apply the **swap test**: if a key topic word could be replaced with “marketing,” “leadership,” or another unrelated subject and the hook would still work, it is too generic. Add a mechanism, evidence, actor, outcome, or decision that makes it topic-specific.

Avoid:

- “Excited to share,” “thrilled to announce,” or similar internal-emotion openings.
- Throat-clearing such as “In today’s fast-moving environment.”
- Empty cliffhangers that never produce a real payoff.
- Several rhetorical questions in a row.
- Generic motivational claims.
- Clickbait such as “You will not believe” or “This changes everything.”

### 3. Choose one structure

Pick the structure that best fits the source. Do not combine several structures unless there is a clear reason.

1. **Counterintuitive claim → evidence → implication**
   - Best for research, data, and argument posts.
   - Start with the surprise, show supporting facts, then explain what readers should reconsider or do.

2. **Changed mind → trigger → updated view → takeaway**
   - Best for thoughtful first-person posts.
   - State the prior view, explain what changed it, and give the new conclusion.

3. **Problem → why it matters → practical response**
   - Best for explainers and operational content.
   - Keep the problem concrete and make the response proportionate.

4. **Result → how it happened → reusable lesson**
   - Best for launches, team outcomes, and approved case studies.
   - The result must be real, specific, and appropriately disclosed.

5. **Framework → examples → application**
   - Best for posts readers may save and revisit.
   - Give the framework a useful name only if it clarifies rather than disguises ordinary advice.

6. **Specific announcement → reader relevance → next step**
   - Use only when the announcement itself is notable.
   - Lead with what happened and its practical significance, not organizational excitement.

7. **Strategic trade-off → rationale → consequence**
   - Useful for explaining deliberate constraints or “anti-goals”: what a team or organization has chosen not to optimize for, and why.

### 4. Draft: hook, tension, payoff

Use this default body shape:

- **Hook:** the strongest claim, result, or tension.
- **Tension or setup:** why it matters, what makes it surprising, or which assumption it challenges.
- **Payoff:** the evidence, story, framework, or practical insight. The post should be useful even if readers never open a link or view supporting material.
- **Soft close:** exactly one focused question, practical takeaway, or clear pointer to more material.

A useful default is under 300 words, but length should follow substance and platform norms. Every extra line must earn its place. Use one- or two-sentence paragraphs so the post scans well on a phone. Use bullets only when the content is genuinely list-shaped.

For a carousel or document caption:

- Establish the central idea in the caption.
- Include one or two strong specifics.
- State what the visual material adds.
- Do not repeat every slide in prose.

For a linked article, report, or episode:

- Put the strongest finding in the post itself.
- Treat the longer item as depth, sources, context, or extended analysis.
- Follow the user’s chosen platform strategy for link placement.
- Never make “read the link” the main value proposition.

## Calls to action and questions

Use one close only. A strong close gives readers a real, bounded way to respond.

Good examples:

- “Which constraint matters most in your work?”
- “What evidence would change your view?”
- “If you have operated a system like this, where does this model fail?”
- “The full analysis includes the assumptions and source material.”

Weak examples:

- “Thoughts?”
- “Let me know what you think.”
- Several questions at once.
- Requests to comment, tag, repost, or react purely to boost reach.

A question should invite knowledge, disagreement, or relevant experience. Do not use engagement bait.

## Editing pass: remove templated language

Run a separate editing pass after drafting. Cut polished language that says little.

Replace or remove:

- Inflated verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Hedging frames such as “it is worth noting” or “one might say,” unless the uncertainty itself matters.
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Abstract nouns such as “journey,” “transformation,” or “paradigm” when a concrete event can be named.
- Transition sentences that merely restate the preceding paragraph.
- Dramatic frames such as “The truth is” or “Here is the reality.” State the point directly.
- Decorative formatting the chosen platform will not render correctly.

If the user has punctuation preferences, follow them. Otherwise, favor periods, commas, and line breaks over theatrical punctuation. Read the draft aloud. If it sounds like generic thought leadership rather than a person making a specific point, rewrite it.

## Revision protocol

When the user gives feedback, revise the flagged line and the nearby logic first. Do not rebuild the entire post unless asked.

- If the hook is not sharp enough, offer several replacement hooks before changing the body.
- If a claim feels overstated, strengthen the evidence, narrow the claim, or add a necessary qualification.
- If a paragraph feels slow, remove setup before adding explanation.
- If the user prefers an earlier phrase, preserve it unless there is a clear accuracy or clarity reason not to.
- If a requested change would make the post misleading, explain the issue and provide a safer alternative.

Multiple small options are often more useful than one complete redraft, especially for hooks, closers, and uncertain lines. Be candid about weak material:

> The second paragraph depends on a broad claim that the current source does not support. We can add evidence, make it narrower, or replace it with this concrete example: [example].

## Readiness gate and audit

Do not present a draft as final until it passes this checklist:

- Does the first line earn attention when read alone?
- Is the post about one clear point rather than several competing ideas?
- Is there at least one concrete detail, outcome, example, number, or mechanism where appropriate?
- Could the main claim be defended if a knowledgeable reader challenged it?
- Does the post provide value without requiring a click, swipe, or purchase?
- Is uncertainty stated where it materially affects the conclusion?
- Is the language specific to this topic rather than reusable for any industry?
- Is the close one focused action, question, or pointer?
- Are names, quotes, figures, and claims approved or supported by source material?
- Are personal details necessary, authorized, and within the intended access boundary?
- Does formatting work on the intended platform?
- Is the tone professional, respectful, and non-inflammatory for the intended audience?

If any answer is no, revise before handoff.

## Handoff format

Present only what the user needs to decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the delivery format the user requested.
3. Any unsupported claim, missing input, authorization issue, or line that remains uncertain.
4. Suggested link or first-comment text, if relevant to the user’s platform strategy.
5. One concise publishing reminder appropriate to the platform, such as responding promptly and substantively to genuine comments.

Do not claim that a format, posting time, or engagement tactic is guaranteed to improve distribution. Platform behavior changes. Treat distribution advice as a testable hypothesis and encourage comparison across multiple posts.

## Common failure patterns

- **Announcement disguised as content:** The post says the organization is pleased, but not why readers should care. Lead with the change or lesson.
- **Pure teaser:** The post asks for a click but provides no value. Share the main finding and use the longer piece for depth.
- **Unsupported precision:** A striking number lacks a source, scope, or caveat. Verify, qualify, or remove it.
- **Generic inspiration:** The post sounds positive but includes no mechanism, example, or decision. Name the concrete action or trade-off.
- **Overpacked summary:** The post covers every section of a report. Select one strong thread and save the rest for the source or future posts.
- **Bolted-on promotion:** A product, course, or service appears at the end without a real connection. Remove it, create a separate promotional post, or make the connection immediate and concrete.
- **Forced engagement:** The post demands reactions or comments. Ask one real question or end with a useful conclusion.
- **Unauthorized personal story:** The post reveals more about a person than is needed or permitted. Remove identifying and sensitive details, confirm permission, and use only relevant evidence.

The final standard is simple: a reader should be able to identify the point, the supporting basis, and why it matters without feeling sold to, talked down to, or misled.


---
name: case-study-post
description: Create an evidence-based, approval-ready case study post with alternate hooks, quote-card options, a clear CTA, and a privacy-aware verification process.
---

# Write a case study post

Use this workflow to turn approved source material about a person’s career, learning, professional change, project, or outcome into a concise public case study. It suits professional social posts, newsletters, community updates, recruitment pages, and alumni stories.

The goal is not vague praise. Show a credible, specific change: where the person started, what prompted action, what concretely helped, what happened next, what they do now, and what the reader can do.

A strong case study helps readers recognize their own situation in the subject’s before-state. It explains the mechanism of change without overstating causation, credit, or certainty.

## Permissions, privacy, and access boundaries

Before using interviews, applications, internal messages, profiles, records, or other communications about a person, confirm that there is a legitimate publishing purpose and clear authorization to use the material for this case study.

Use the minimum relevant sources and details. Do not include unrelated personal information, sensitive circumstances, or details that would exceed the audience’s expected access boundary. Respect the subject’s consent, stated preferences, and any confidentiality obligations.

If material was supplied for internal review rather than public publication, do not assume it can be quoted or published. Seek approval or use public, independently verified information instead.

## Inputs

Ask for all available and authorized source material. This may include:

- An interview transcript and meeting notes
- An application, intake form, or written statement
- A current professional profile or approved biography
- Public work samples, publications, projects, or announcements
- An internal message reporting an outcome, if authorized for this use
- A prior draft, outline, or notes from the subject
- The intended audience, publication channel, and call to action
- An editorial or brand voice guide
- The subject’s approval status for names, direct quotes, figures, and sensitive details

Before drafting, determine whether the following fields are sufficiently supported:

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns if relevant, and any naming preferences |
| Before-state | Previous role, field, goal, uncertainty, or constraint |
| Trigger | Why they joined, applied, changed direction, or took action |
| Intervention | Program, community, event, mentor, product, resource, or other relevant support |
| Mechanism | Concrete help, such as a realization, introduction, opportunity post, feedback session, or practical resource |
| Now-state | Current role, organization or team if approved, project, output, or result |
| Timeline | Dates or time spans from the starting point to the outcome |
| Evidence | Verified roles, dates, figures, named work, and direct quotations |
| Cost or risk | Career change, financial tradeoff, move, uncertainty, or other relevant tradeoff |
| CTA | The one action the reader should take next |

If critical information is missing, ask focused questions before drafting. Do not guess at organization names, job titles, project titles, dates, figures, timelines, quotes, or outcomes.

Useful questions include:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they decide to act at that point?
4. What are the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a public or approved output, project, placement, publication, product, or result worth naming?
8. Did they take on a meaningful cost or risk they are comfortable sharing publicly?
9. Which claims, figures, names, and quotes are approved for public use?
10. Who should this post help or persuade?

## Evidence and verification rules

Never invent facts or strengthen a claim for dramatic effect. If a source says a person contributed to a project, do not call them the lead. If they explored an opportunity, do not say they received it. If a transcript describes work in broad terms, do not supply a more specific title from inference.

Automated transcripts and summaries are useful but fallible. They may mishear names, organizations, technical terms, figures, dates, and titles. Cross-check consequential details against a more reliable source such as direct confirmation from the subject, an official public record, published work, or a current professional profile.

Use this default reliability order:

1. The subject’s direct, recent confirmation
2. Official public records, announcements, or published work
3. A current professional profile
4. An original written application or statement from the subject
5. Interview transcript notes or automated summaries
6. Informal third-party messages

Maintain private working notes that distinguish:

- **Verified fact:** Supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn from the story. Use only when well supported, and phrase it modestly.

Do not claim that a program, community, tool, or mentor caused the entire outcome unless that causation is established. Prefer precise claims such as “the program helped them see the field differently” or “they found the opportunity through the community.”

## Sensitive-content gate

Flag the following for explicit subject approval before publication:

- Salary, compensation changes, financial hardship, or comparisons
- Health, family, immigration, legal, or other personal circumstances
- Harsh statements about past employers, colleagues, roles, or decisions
- Unreleased work, confidential projects, or unpublished titles
- Direct quotations, especially strong opinions or criticism
- Claims about why an employer selected or hired the person
- Claims of causation, impact, or performance that cannot be verified
- Precise dates or timelines that may expose private circumstances

If approval is unavailable, use an honest approved fallback or omit the detail. For example, “they accepted a lower-paying role” may replace an exact figure only if that broader statement is approved. Do not conceal uncertainty by making a story more dramatic.

## Build the story beats

Create a concise private outline before writing.

### 1. Before-state

Capture the subject’s role, background, and the reader-relevant form of their uncertainty. Include the alternative path they were considering when it mirrors the audience’s current life.

Keep only details that move the story. Long lists of reading, credentials, and prior roles usually weaken the post. Retain a detail when it explains the decision or makes the change concrete.

### 2. Trigger

Identify why the person acted then. They may have wanted to test whether a career path was open to them, learn a new field, find collaborators, solve a practical problem, or make a values-driven change.

### 3. Mechanism

Find one or two observable turning points. Good mechanisms include:

- Realizing a field or role was accessible
- Finding a relevant opportunity in a community
- Having a conversation that clarified next steps
- Receiving feedback that improved an application or project
- Getting a specific introduction, workshop, or resource

Avoid “the experience was transformative.” Name what happened.

### 4. Now-state

Record the current role, organization or team if approved, and what the person actually does. Translate technical language enough for the intended reader to understand the work.

Use named outputs only when they add proof or interest. One meaningful artifact, project, placement, publication, grant, or product is often stronger than a long credential list.

### 5. Timeline and compression

Map the sequence from starting point to outcome. Use a short, truthful timeframe when it sharpens the story, such as “within six months” or “the following year.” Do not force a compressed timeline where the evidence does not support one.

### 6. Quotes

Pull three to five verbatim candidate quotes. Favor lines that speak to the reader’s identity or uncertainty, not only the subject’s achievement.

Use these categories:

1. **Discovery:** “I did not know this path was open to someone like me.”
2. **Mechanism:** “I found the opportunity through the community.”
3. **Conviction:** “I would make the same choice again.”

Light trimming is acceptable only when it preserves meaning and grammar. Never rewrite a quotation into words the person did not say.

## Generate three hook options

For feed-based channels, the first two lines determine whether readers continue. Draft three distinct hooks before drafting the full post. Keep each to two short sentences and, where useful for the platform, around 140 characters or fewer.

### Hook A: Discovery

Use when the audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a surprising, concrete mechanism.

This is the default recommendation when readers may think, “That might be me.”

### Hook B: Identity collision

Use when the before-and-after contrast is vivid.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This is useful for a broad audience that may not share the subject’s exact uncertainty.

### Hook C: Stakes-led

Use only when an important cost or risk is approved and the audience is likely to read it as honest conviction rather than a warning.

**Formula:** The subject accepted a specific cost to do something. Now they are taking a concrete action or doing meaningful work.

Avoid this hook if it implies that participation requires hardship or distracts from a more accessible message.

Recommend one hook and briefly state why it fits the target audience. State why the other two are less suitable. Default to Hook A when the story centers on a reader-recognizable blocker.

## Draft the post

Aim for roughly 160 to 220 words unless the channel or audience calls for another length. Shorter is usually stronger.

Use this sequence:

1. **Hook:** Use the recommended option.
2. **Before-state:** One short paragraph with the prior situation and a relevant alternative path.
3. **Name the intervention:** Clearly state that the person joined the program, used the resource, or entered the community. Do not leave this implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then land the immediate result plainly.
5. **Current work:** Describe what they do now and why it matters in language the intended reader can understand.
6. **Optional honest cost:** Include only if approved and useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already carried by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

Where a publishing channel may reduce visibility for external links in the body, place the link in a comment, profile destination, or other designated location. Treat this as a channel-specific publishing choice, not a universal rule.

## Style rules

Adapt to the chosen voice guide. If none is supplied, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use concrete names, roles, dates, and figures only when verified and approved.
- After a first full introduction, use the subject’s preferred short name if it suits the tone and they consent.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Avoid unsupported labels such as “exceptional,” “inspiring,” or “brilliant.”
- Use contractions if the voice is conversational.
- Keep the CTA in full second person: “If you are…” and “you can…”
- Avoid emojis unless they are an explicit brand choice.
- Prefer periods, commas, and line breaks over em dashes.

On the final pass, remove machine-like phrasing: empty transitions, dramatic setup frames, filler intensifiers, hedge words, abstract nouns replacing evidence, balanced “on one hand/on the other hand” constructions, and reflective summaries after the CTA.

Avoid corporate or vague terms such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm” unless required in an approved direct quote.

Read the post aloud. If it sounds like generic thought leadership, shorten it and replace abstractions with facts.

## Graphic quote options

Provide three quote-card options. Each should be self-contained, preferably under 15 words, and verbatim from approved source material.

Offer one from each category:

- Discovery
- Mechanism
- Conviction

Recommend one quote. Discovery quotes often work best because they need the least context and mirror a reader’s possible uncertainty. Choose a mechanism or conviction quote only if it is clearer and more memorable on its own.

## Readiness audit

Before sharing the draft for review, check:

- Is every name, role, date, figure, title, and output verified?
- Were important transcript-derived details cross-checked?
- Is the source use authorized and limited to relevant information?
- Does the post show a concrete mechanism, not merely a result?
- Does it avoid overstating causation or credit?
- Is the intervention named clearly?
- Does the opening mirror a real audience concern?
- Is current work understandable to a non-specialist reader?
- Are sensitive claims and direct quotations marked for approval?
- Is the CTA clear and directed to the intended reader?
- Are there no unsupported superlatives, corporate phrases, generic filler, or unnecessary em dashes?

## Delivery and iteration

Create the draft in the user’s chosen document system when one is available. Use a clear title format such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and the two alternatives
- The three graphic quote options and recommendation
- A list of approval items
- A list of missing information that would strengthen the post
- The document location or link, if applicable

Do not treat the first draft as final. If feedback is “make the hook better,” generate new hooks rather than making tiny edits. If asked to make it shorter, cut secondary biography first while preserving the mechanism and outcome. If a subject rejects a sensitive line, replace it with an approved fallback without weakening the rest of the story.

After final acceptance, review feedback for reusable lessons only when a clear pattern emerges, such as a recurring missing intake question, consistent voice preference, or repeated verification issue. Do not create process changes from a clean review cycle.


---
name: create-editorial-cover-images
description: Create, inspect, and refine eight article-specific editorial cover images using a chosen image generator and an evidence-based two-round workflow.
---

# Create editorial cover images

Turn an article into eight finished editorial cover-image options. Develop five distinct concepts, generate and inspect every result, then create three improved options based on what the rendered images reveal. The goal is a set of comparable images that clearly belong to the article, rather than a set of generic prompts or minor variations on one scene.

This workflow is tool-independent. Use the user’s chosen image-generation system and the confirmed requirements of the intended publishing destination. If the user explicitly asks for prompts only, follow the prompt-only branch instead of generating images.

## Purpose, authorization, and boundaries

Use this workflow when there is a legitimate purpose to create artwork for an article, newsletter, essay, report, or similar editorial work. If the material is unpublished, private, or contains information about people, confirm that the requester is authorized to use it for this purpose.

Use the minimum source material needed to understand the article and create a visual brief. Do not send a full unpublished draft to an external generator unless that is necessary, authorized, and consistent with the user’s privacy expectations. Prefer a distilled, article-specific visual description. Omit unrelated names, private details, confidential facts, and sensitive personal information.

Do not invent events, identities, locations, or biographical claims that the article does not support. A visual metaphor may interpret the article’s idea, but it should not look like a factual depiction of something that did not occur. Respect consent, access, payment, rate-limit, and approval boundaries. If the selected generator is unavailable or blocked, report the exact blocker and ask for the smallest necessary action. Do not bypass a rejection, access control, or approval gate. Do not move content to another service without the user’s agreement.

## Default deliverable and modes

The default deliverable is eight completed images:

1. Five deliberately different first-round concepts.
2. A visual review of all five rendered images.
3. Three second-round images informed by visible strengths, weaknesses, and gaps.

Keep the first five available while creating the final three so the user can compare original concepts with refinements. Give every option a stable number and short title. Use separate jobs, conversations, files, or output locations when the chosen generator supports that arrangement.

Use prompts only when the user explicitly requests prompts, or when image generation is unavailable and the user chooses prompt delivery instead. Do not silently substitute written prompts for requested finished images.

## Establish the brief

Read the complete article before developing concepts. A title alone rarely contains enough information to produce an image that feels specific to the piece. If the article is missing, ask for the copy or an authorized synopsis with enough detail to identify its central idea and tone.

Create a private working brief with these elements:

- **Central move:** the main idea, tension, insight, or change in perspective the reader should take away.
- **Emotional progression:** where the article is quiet, tense, reflective, hopeful, urgent, defiant, or resolved.
- **Concrete visual material:** images, actions, objects, settings, analogies, and metaphors already present in the writing.
- **Tone:** the voice and emotional register that should constrain the visual treatment.
- **Audience and placement:** where the image will appear and how it will be viewed, such as a wide header, social card, presentation cover, printed page, or square preview.

Use this analysis to improve the work. Do not automatically summarize it back to the user unless an explanation would help them make a meaningful creative decision.

Reuse preferences already given in the conversation. Ask only for missing choices that would materially change the image. Collect all outstanding answers before treating a partial reply as the final brief.

When needed, ask these related questions together:

- **Mood:** Offer three or four interpretations tied to specific beats in the article. For example, distinguish a quiet recognition early in the piece from a later moment of momentum or resolve. Do not present abstract mood labels without saying what each interpretation emphasizes.
- **Subject:** Offer suitable choices such as a human presence, landscape, single symbolic object, built environment, or abstract composition. Respect restrictions on likenesses, people, places, or representations.
- **Palette:** Offer palettes that support the selected mood. Name colors, contrast, and lightness so the choice does not depend only on color labels. Do not use color pairs that may be difficult to distinguish as the only difference between options.
- **Orientation and placement:** Confirm the crop or aspect ratio required by the destination. A wide header, square card, and portrait cover need different compositions. Use user-provided or verified requirements instead of assuming a standard ratio.
- **Medium or style:** Establish whether the image should be photographic, painted, drawn, collaged, graphic, or another approach when the request leaves this open.

Keep the agreed brief through both rounds. It should include mood, subject rules, palette, style, format, destination, and chosen generator. Do not ask the same questions again during ordinary iteration.

## Propose five distinct concepts

Present exactly five concepts in a numbered list. Each concept must contain:

1. A short title.
2. A one- to three-sentence description of what the viewer sees.
3. A brief statement of the article idea or emotional beat it expresses.

The five ideas must differ meaningfully in subject, composition, action, metaphor, and emotional emphasis. Five slight changes to the same scene are not a useful comparison set. Unless the user’s restrictions rule them out, include at least one landscape-only option and one single-object or symbolic option. A non-identifying human figure can be useful when human presence matters without portraying a particular person, but it is one option rather than a default.

Apply this test to every concept: could its explanation fit almost any article on the same broad subject? If so, make it more specific to this article or replace it.

Give a one-line initial recommendation, then generate all five when completed images are requested. Do not require the user to select one concept before the first round unless they explicitly want to narrow the scope. The rendered results are the evidence needed for informed comparison.

## Write effective visual prompts

Write one self-contained prompt for each concept. Include enough detail to produce a coherent image, but do not pile together incompatible instructions. Use this structure, combining sections only when doing so improves clarity:

```text
Create one image: [medium, dimensions or aspect ratio, and overall editorial character].

Subject: [what is visible, its action, scale, prominence, and position. Include relevant constraints here, such as no visible facial detail, no logos, or no lettering].

Setting: [surroundings, depth, foreground and background relationships, or environmental context].

Light and palette: [direction and quality of light, specifically named colors, contrast, and transitions].

Technique: [visible properties of the chosen medium, edge treatment, texture, detail level, and negative space].

Mood: [the intended feeling and its connection to the article’s central move].

Composition: [focal point, eye path, major shape placement, crop, aspect ratio, and any reserved empty space].

Avoid: [artifacts, conventions, or content that conflict with the brief].
```

Name colors and their relationships rather than relying only on vague terms such as “warm,” “cinematic,” or “moody.” For example, “pale ochre ground fading into blue-grey shadow, with a small muted violet accent” is more actionable than “dramatic warm light.” Choose the palette from the article and the user’s preferences, not from a permanent aesthetic default.

Describe the chosen medium through its actual visual qualities. Watercolor may need wet-on-wet washes, pigment blooms, paper texture, transparent glazing, selective edges, and unpainted space. Charcoal may need broad tonal masses, broken edges, and paper grain. Photography may need a plausible light direction, lens distance, depth of field, and realistic materials. Avoid instructions that conflict with one another.

Put important exclusions alongside relevant positive instructions as well as in the final Avoid section. For example, state “silhouette with no visible facial detail” in the subject section if anonymity matters. Establish whether typography will be added later. Unless text is intentional, request no text, logos, borders, or watermarks.

Send only the visual brief required for the individual image. Use article-specific facts only when supported by the source and appropriate to visualize.

## Generate the first five

Use the chosen generator’s supported workflow. Explicitly request creation of one image so that a text response is not mistaken for an image deliverable. Adapt syntax to the service while preserving the concept, composition, palette, format, and exclusions.

Maintain a working record for every option: number, title, concept, submitted prompt, generation status, output location, and review notes. Preserve the complete prompt so a truncated or failed request can be repaired accurately.

For browser-based or session-based generators, use these general checks:

1. Create distinct, clearly identifiable jobs or conversations for options one through five. Do not take over unrelated user work.
2. Confirm that the complete prompt appears in the live submission interface before sending it.
3. Verify that the service accepted the intended request.
4. Record only observed links, session locations, or identifiers. Never invent output locations.
5. Start independent jobs without unnecessary delay when the tool supports it, while keeping interface actions sequential and grounded in the current page state.
6. Confirm completion by opening the actual rendered image at a useful size. A spinner, placeholder, accepted request, elapsed time, or text description is not proof of completion.
7. If an error appears, first check whether an image already completed before retrying, to avoid duplicates and wasted quota.

If a service responds with text instead of an image, request image generation again in the same job when possible. Keep unsuccessful attempts separate from completed options.

## Inspect all five before improving

View every first-round image at a useful size. Evaluate rendered pixels, not the generator’s description and not the original intention. Also inspect a reduced preview, because editorial cover art must communicate when small or cropped.

For each image, assess:

- Whether it communicates the article’s central idea and emotional tone.
- Whether the subject, action, and focal point read immediately.
- Whether the requested style, palette, orientation, and composition survived generation.
- Whether it is too busy, generic, sentimental, static, literal, decorative, or confusing.
- Whether anatomy, objects, perspective, structure, texture, or unintended lettering contain visible artifacts.
- Whether it remains distinct from the other options and useful as editorial cover art.

Only after inspecting all five should you write the three second-round prompts. Each must respond to visible evidence: preserve a demonstrated strength, correct a specific weakness, or fill a meaningful conceptual gap. Do not prewrite this round before visual review.

A useful second round often includes one refinement of the strongest first-round result, one synthesis of strengths from different images, and one new concept that addresses an unmet need. Treat this as a guide rather than a rigid formula.

Fix causes instead of adding decoration. If an image is cluttered, reduce objects, competing focal points, or scene complexity. If a painting resembles a photograph with a superficial filter, specify larger shapes, selective edges, authentic marks, and more negative space. If a scene feels like generic stock imagery, revisit the action or metaphor before adding detail.

Give a short progress update describing what the first images revealed and what the next three will improve. Continue without requesting another creative selection unless a new decision is genuinely required.

## Generate, review, and deliver options six through eight

Generate three new images from the evidence-based prompts. Keep options one through five unchanged. Inspect every second-round image using the same completion and visual-review criteria. Repair failures where possible, but do not count a failed request, text-only response, or reused old image as a completed new option.

Before delivery, verify:

- Eight distinct completed outputs exist.
- Each finished image was personally inspected.
- Each option can be opened from the final handoff location.
- Numbering, titles, and output locations match the working record.
- Options six through eight are clearly marked as the second round.
- Outputs remain within the user’s authorized access boundary.

Leave outputs available in the form the user requested, such as open sessions, a generator gallery, or verified download locations. Do not create an unnecessary separate document or gallery when native generator outputs are sufficient for comparison.

Recommend the strongest rendered option in one short sentence, explaining why it fits the article. Then provide a numbered list of all eight titles and verified output locations, clearly marking the second-round options. Make that list the final deliverable block. If fewer than eight images are complete because of access limits, rate limits, or persistent errors, state exactly which options are finished and which remain blocked. Preserve useful work for resumption and never represent prompts as completed images.

## Prompt-only branch

When the user explicitly requests prompts only, do not generate images. Read the article, establish the same creative brief, and propose five concepts. Wait for a selection unless the user already selected concepts or asked for prompts for all five.

Write every selected prompt in a separate fenced code block using the prompt structure above. If combining concepts, add one brief sentence explaining what is being combined. Do not call later prompts visual improvements, because no first-round images were inspected. Put the selected prompts last, with nothing after the final prompt block.

## Adapt to another image generator

When creating a variant for another generator, preserve the underlying concept, mood, composition, palette, aspect ratio, and exclusions. Change only the syntax, controls, and prompt structure needed by the target service.

Use prose for tools that work best with full visual descriptions. Use concise descriptive phrases and documented parameters only for tools that support them. Check current tool conventions before including version flags, style controls, seeds, or aspect-ratio syntax. If a setting materially affects the result and remains unclear, ask once rather than guessing.

A platform variant is not a new visual concept. Keep the image idea consistent so the user can compare tools fairly.

## Learning and quality audit

After the user chooses an image, accepts a prompt, or clearly ends iteration, retain only durable lessons that the user has authorized to be remembered. Useful lessons may concern article interpretation, composition, prompt constraints, medium direction, or verified generator behavior. Distinguish explicit user feedback from personal aesthetic inference.

Do not retain private article content, unpublished facts, personal details, or one-off subject matter as reusable guidance. Do not turn one successful composition into a universal default. If no general lesson emerged, make no workflow change.

Before considering the task complete, audit the work:

- Was the full article, or an authorized sufficient brief, read before concept development?
- Were mood, subject, palette, style, orientation, destination, and generator resolved or intentionally left open?
- Are the five first-round concepts genuinely distinct and grounded in article-specific beats?
- Does every prompt contain a clear subject, composition, palette, technique, format, and relevant exclusions?
- Were all first-round images inspected before the second-round prompts were written?
- Does each second-round prompt respond to visible evidence rather than a preplanned variation?
- Were eight distinct completed images verified, or were incomplete results reported honestly?
- Were privacy, authorization, access, and approval boundaries respected throughout?


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
description: Close one month honestly, then create a small, capacity-checked and explicitly approved plan for the next month using evidence, trade-offs, and concrete commitments.
---

# Review and plan a month

Use this workflow at a month boundary to review the month ending and build an executable plan for the month ahead. A complete session usually takes 45–75 minutes: roughly half for evidence and review, and roughly half for planning.

Review and planning belong in the same session. The structural cause of a missed commitment, energy drain, or delivery problem should directly shape the structure of the next plan.

## Purpose

This workflow produces:

- An evidence-based account of what happened during the review month.
- A concise verdict on progress toward active long-range goals.
- A month-level picture of selected work and life signals, such as focus, sleep, energy, training, or completed work.
- A written **Review** for the month ending.
- A written **Plan** for the month beginning, with a named theme, no more than three major outcomes, explicit trade-offs, and a pre-mortem.

Only gather, discuss, or save information that supports one of these outputs.

## When to run it

Run this workflow when the user asks for a monthly review, asks to plan a named month, or asks to close one month and start another.

Default timing:

- On the first three days of a month, review the prior month and plan the current month.
- Otherwise, review the current month to date and plan the next month. Clearly label a partial-month review and state the days remaining.
- If the user asks only for forward planning, review first because the evidence should shape the plan. The user may explicitly choose to skip the review.

State the ranges plainly before proceeding:

> Reviewing **March 2026** (01 Mar–31 Mar). Planning **April 2026**.

Ask whether the user means calendar months or a practical range that includes an overlapping partial week. Record the actual planning range in the finished plan.

## Operating rules

1. **Read first; discuss second.** Show the evidence picture before asking reflective questions.
2. **Batch independent reads.** If connected sources exist, gather independent evidence in one initial pass. Do not interrupt the conversation with repeated small lookups.
3. **Use current commitments.** Assess against the user’s live target, not an old schedule, obsolete project scope, or stale goal record.
4. **Check data quality before a harsh verdict.** Missing syncs, incomplete logs, delayed updates, and inconsistent sources may distort results. Ask the user to confirm surprising findings.
5. **The user chooses.** The assistant calculates, summarizes, identifies gaps, and holds constraints. The user chooses priorities, cuts, and commitments.
6. **One decision at a time.** Do not move to the next planning decision until the current question has a real answer.
7. **Stay at month altitude.** Define outcomes, milestones, capacity, structure, and commitments. Leave detailed weekly task blocks to a weekly planning workflow.
8. **No saved plan without explicit approval.** A plan assembled from notes is a draft, not a decision. The user must restate or materially confirm the theme and commitments, then explicitly approve it.
9. **Use explicit dates.** Use **DD MMM** format unless the user prefers another unambiguous convention.
10. **Keep records useful, not exhaustive.** Save decisions, evidence, and constraints rather than a meeting transcript.
11. **Do not lecture.** Where personal practice, training, health, or recovery is in scope, provide the numbers, the direct conclusion, and the agreed commitment. Give specialist advice only when asked and when appropriate.

## Step 1: Determine the range and gather evidence

Determine the review month, prior comparison month, and planning month. Then make one initial batch of reads where possible.

Choose sources that match the user’s chosen system: a task manager, project tracker, calendar, spreadsheet, notes application, health tracker, training log, or user-supplied facts. If no source is connected, ask for a short factual inventory. Never imply that unavailable data was checked.

| Evidence area | Gather in the initial pass |
|---|---|
| Previous monthly record | Theme, promised outcomes, commitments, and prior review findings |
| Weekly records | Plans and reviews in the review range; repeated blockers, milestones, and carried work |
| Goals | Active weekly, monthly, quarterly, and annual goals; status, deadlines, and notes |
| Work delivered | Completed tasks, decisions, projects, or deliverables; grouped into useful domains |
| Calendar | Next-month travel, leave, events, fixed deadlines, recurring commitments, and heavy meeting weeks |
| Daily signals | User-selected ratings, focus time, journals, habits, or mood notes |
| Sleep and recovery | Optional sleep duration, sleep quality, and same-source recovery trends |
| Training or practice | Optional sessions from the review and prior months, plus the live commitment or schedule |

For large sources, return computed statistics and a few representative themes rather than raw entries. Long journals and month-long event lists can crowd out the actual review. Use filtered queries, aggregation, summaries, or a delegated helper when available.

If a helper is used for a large calendar or journal source, give it a narrow brief: use only authorized read access, analyze only the requested date range, and return a concise planning summary rather than raw data. The summary should include:

- Fixed multi-day blocks, such as travel, leave, or conferences.
- Approximate meeting load by week.
- Important recurring series.
- Protected personal or social commitments.
- Planning anomalies, such as meetings inside unavailable periods or likely time-zone mistakes.

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
- Relevant balance measures, such as easy versus demanding work, when records support them.
- Relevant performance or recovery measures.
- Month-over-month changes.

Use this verdict taxonomy when it fits:

- **ON TRACK**: key measures meet at least 90% of target and consistency is intact.
- **BEHIND**: a key measure is about 60–90% of target, or there was a meaningful consistency break.
- **OFF TRACK**: a key measure is below 60% of target or there was a prolonged gap.
- **AT RISK**: injury, safety, burnout, or sustained decline makes the plan unsafe or unlikely.

Adjust thresholds only when the user’s domain needs different ones, and state the adjustment. If tracking may be incomplete, ask: “The record shows this. Does that match reality?” before making a strong judgment.

State one biggest corrective action for the next month. This is a concrete commitment, not a full program.

### Goals and delivery

Summarize weekly commitments as completed, missed, deferred, or rolled forward. For every active long-range goal, state whether it **advanced**, **stalled**, or **regressed**, with one short reason. Explicitly name goals that received no meaningful attention; these are often most at risk.

Also summarize completed work in a few useful domains. Avoid a wall of bullets. The question is whether effort created intended progress.

### Life signals

Include only measures the user chooses to track. Useful measures include rating distribution and average, focus hours, low-focus days, sleep duration, sleep quality, recovery trends from a consistent source, and repeated themes in written notes.

Flag meaningful patterns, such as low average sleep, repeated short nights, several consecutive low-rating days, an extended low-focus streak, or an apparent mismatch between positive ratings and written notes describing exhaustion or stress. Numerical averages are not complete truth. Raise the mismatch directly and briefly.

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

Size the gap with evidence, not mood. Inspect the relevant draft, pipeline, milestone, backlog, baseline metric, or other domain-specific reality. If the gap cannot be described, gather the missing evidence before designing the path.

### Move 3: Work backward to build a path

For each outcome, identify three to six moves by reasoning backward from the due date. Every move needs a date or window, an owner, and evidence of completion.

Ask:

> For this to be true by the end date, what must be true halfway through? What must happen before that?

### Move 4: Do capacity math

Estimate usable focused capacity honestly:

> available working days × recently observed focused hours per day

Account for travel, leave, meeting-heavy weeks, and fixed commitments. Compare available capacity with the effort implied by the paths. If demand exceeds supply, cut, defer, reduce scope, or add real help now.

### Move 5: Make the NOT-doing list

Ask:

> What will explicitly not happen this month so these outcomes can?

The user names the cuts. A plan without a real not-doing list is a wish.

### Move 6: Add forcing functions and protective structure

Fragile outcomes need external pressure: a stakeholder expecting a deliverable on a date, a booked review, a public commitment, or a downstream owner waiting on the work.

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
[Travel, leave, fixed events, heavy weeks, effective working weeks, and immediate post-month constraints.]

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

## Step 5: Save the review and plan

After explicit sign-off, write two records in the user’s chosen system:

1. A **Review** attached to the ending month.
2. A **Plan** attached to the new month.

Create a missing monthly record if the system supports it. Use one final write operation when possible. Before overwriting an existing plan, show it to the user and resolve the conflict.

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

At the end of every run, make one precise improvement to the reusable workflow, its templates, or its data mapping. Store it in the user’s chosen workflow document or improvement log. If no suitable location exists, present the proposed edit as a short durable rule the user can save where they prefer.

Look for a read that was noisy, a wrong data assumption, a misleading metric, a question the user corrected, or a repeatable pattern future sessions should know. Prefer one specific edit over a vague reminder.

## Audit checks

Before finishing, verify:

- Review and planning ranges are explicit.
- Evidence was shown before reflective prompts.
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
description: Plan travel around its purpose, compare complete current journeys, and prepare or make authorized bookings while protecting privacy and handling trade-offs clearly.
---

# Plan and book a trip

Plan transport around the purpose of the trip, not around the first cheap fare found. First establish what the traveler needs from the journey, then research a small set of complete, practical options, and finally prepare or complete the selected booking within clear authorization. Current user instructions take priority over remembered preferences, prior receipts, and previous trip plans. A decision made for one trip is evidence for that trip, not an automatic rule for future travel.

## Principles and boundaries

- Use travel, calendar, correspondence, account, and reservation information only for a legitimate travel-planning purpose and with clear authorization.
- Search only the minimum relevant sources and information. Do not use access to an account as permission to inspect unrelated messages, records, companions, or personal details.
- Keep personal information, identity documents, payment details, loyalty numbers, booking references, and private addresses within the appropriate private booking record. Do not place them in reusable instructions or shareable summaries.
- Do not contact airlines, rail providers, hotels, organizers, companions, or other people unless the traveler authorizes it.
- Do research and routine factual checking yourself when authorized. Ask the traveler only for a missing fact, required authentication step, or decision that cannot be resolved from available sources.
- Never represent a search result, a fare held in a basket, or an incomplete checkout as a completed booking. A booking is complete only after confirmation from the provider.
- Do not promise future fare checks or upgrade monitoring unless an authorized, functioning monitoring method is actually configured.

## 1. Understand the trip before researching fares

For a new trip, begin with a focused discovery pass. Do not start detailed fare searches, upgrade comparisons, or checkout preparation while questions that could materially change the trip remain unanswered. The aim is to avoid allowing an early schedule or low advertised price to determine the trip's shape.

For a continuing conversation, use the established trip brief and ask what has changed. Follow an explicit request to skip discovery or perform a narrowly defined check, such as checking a particular train or flight.

### Review relevant context

Read materials supplied by the traveler, such as invitations, agendas, event pages, accommodation details, travel documents, or existing booking confirmations. If the traveler has authorized access to relevant private sources, conduct a short, scoped review of travel-related calendar events, correspondence, documents, and existing reservations.

Look for:

- the trip's purpose and desired outcome;
- event locations, start and end times, and whether attendance is confirmed;
- companions, hosts, or people the traveler hopes to visit;
- fixed commitments immediately before and after the likely travel dates;
- existing transport, accommodation, local transport, or time off;
- confirmed dates versus tentative holds or invitations;
- access, health, work, reimbursement, or accessibility needs that affect the journey.

Distinguish facts from inferences. For example, an event invitation may establish a location and proposed time, but it does not by itself prove that the traveler intends to attend or wants to arrive on the first day. Resolve conflicting sources when possible, and visibly label uncertainty that remains.

Keep this pass brief. Retrieve accessible facts instead of asking the traveler to copy them from authorized sources, but give the traveler an early opportunity to set the direction before doing detailed shopping.

### Ask questions that shape the trip

State the important facts already known, then ask a concise, substantive set of questions. Four to six questions normally works for an open-ended trip; ask fewer when most answers are already settled. Use one numbered plain-text block so the traveler can answer easily.

Choose questions that develop the trip rather than merely collect booking fields:

1. **Purpose and priorities:** What would make this trip worthwhile? Which event, visit, activity, or outcome matters most?
2. **People and places:** Who is traveling, being visited, or met? Which stops are essential, optional, or best done in a particular order?
3. **Time:** How much time does the traveler want in each place? What fixes the earliest departure, required arrival, and latest return? If dates are flexible, what is the useful range?
4. **Pace, work, and recovery:** Is this work, leisure, or both? Must the traveler arrive rested, work en route, include a quiet day, or leave unstructured time?
5. **Practical arrangements:** What accommodation, rides, rail passes, local support, or onward transport already exists? Are there accessibility, spending, reimbursement, or documentation constraints?
6. **Requested outcome:** Does the traveler want research, a recommendation, booking preparation, or an authorized purchase?

Do not make a numeric budget compulsory when the traveler wants to understand the available trade-offs first. Do not turn the first discussion into an unnecessary debate about cabin products, loyalty programs, or upgrades. Ask about those only if they are unknown and likely to change the recommendation.

### Agree a trip brief

Summarize the working brief before detailed fare research. Include:

- purpose, important people, and stops;
- desired time in each place;
- fixed dates, deadlines, and flexible date ranges;
- work, rest, and arrival-readiness needs;
- accommodation and ground-transport arrangements;
- known travel preferences that are relevant to this trip;
- unresolved choices and assumptions.

Give the traveler a chance to correct the summary. Clear answers can establish agreement; do not ask for ceremonial approval after the traveler has already made the necessary choices. However, wait for answers to unresolved questions that would materially affect the route, dates, or transport type. Keep provisional dates visibly marked as provisional.

## 2. Research current transport options

Start detailed research only after the brief is sufficiently clear, unless the traveler explicitly asks for a limited fare check. Keep the search tied to the agreed trip. If available transport would require a meaningful change—such as losing an important day, adding a risky connection, or arriving too tired for a key event—return to the traveler with that decision rather than silently changing the plan.

### Search and verify live options

Search the useful date range and all realistic modes: air, rail, ferry, road transfer, and local transport where relevant. Discovery tools and price calendars are useful for finding routes and date patterns, but verify the chosen itinerary with the operating provider whenever practical.

For each promising option, establish:

- local departure and arrival dates and times;
- airports, stations, terminals, and any change of airport or station;
- operating provider, not merely a marketing or reseller label;
- total duration, connection length, and whether tickets are protected together;
- fare family or named ticket type;
- actual cabin, class, berth, or seat product on every segment;
- price, currency, inclusions, and the time checked;
- change, cancellation, refund, and missed-connection conditions;
- relevant luggage, seat-selection, and boarding requirements.

Label every quoted price accurately:

- **Live selected itinerary:** currently available for the specified service and fare.
- **Indicative date-grid price:** useful for comparing dates but not yet verified for the selected itinerary.
- **Estimate:** a reasoned approximation, clearly separated from a bookable quote.

Do not treat an advertised “from” price as proof that the required ticket is available. Use verified links for booking and material fare terms when links can safely be shared.

### Compare complete journeys, not isolated tickets

Consider round trips, one-way combinations, open-jaw itineraries, nearby airports, different rail stations, and combinations of air and ground transport when they fit the brief. Include the rail journey, airport transfer, cross-city transfer, hotel, or lost usable time needed to make each option work.

A lower base fare is not necessarily cheaper or better if it creates an overnight stay, a difficult transfer, a long drive, or a missed workday. Verify the actual onward destination, especially where place names are ambiguous or a major airport remains far from the final destination.

Check timetable-release dates, planned engineering work, holiday disruption, border procedures, and seasonal schedules. Do not invent an exact train, fare, or transfer time before schedules are released.

### Evaluate product quality and comfort honestly

Compare the actual product, not an imprecise label. Extra-legroom economy is not premium economy. A reseller's generic “first class” label may not establish the provider's named product or conditions. A business-class label does not guarantee a lie-flat seat on every aircraft or route.

When overnight travel or next-day performance matters, compare sleep quality and readiness alongside price. For example, a traveler may reasonably prefer a higher cabin or berth for an overnight segment and a lower-cost product for a daytime return. Assess every segment of mixed-cabin itineraries rather than describing the journey by its best segment.

If the traveler has a seat preference, check whether a suitable seat is currently selectable and include any necessary selection fee. A preference is not a confirmed assignment. Verify cabin-bag allowances, dimensions, and weight limits for the exact fare. A personal-item-only ticket may not meet a traveler who needs a cabin bag.

### Account for jet lag and recovery when relevant

For trips across multiple time zones, rank practical schedules by their likely effect on sleep, alertness, and the traveler's first important day. Do not rely on price and duration alone.

Use the traveler's stated sleep pattern if available. If it is not available, ask whether arrival readiness is important and use broadly sensible sleep-protection principles:

- For eastbound trips, favor schedules that give the traveler a realistic opportunity to sleep during their usual biological night and avoid an exhausting first local day when possible.
- For westbound trips, daytime travel and arrival in daylight can make it easier to remain awake until a reasonable local bedtime.
- For an overnight work trip, give extra weight to confirmed sleep conditions, arrival buffers, and a reduced first-day schedule.
- Suggest a practical pre-trip sleep adjustment and a first-days plan for light exposure, meals, caffeine, and naps, while making clear that individual responses vary.

Do not present medical certainty or assume that the same schedule suits every traveler. Ask whether the traveler prioritizes cost, a low-stress departure, sleep, or immediate performance.

### Evaluate upgrades without false certainty

When upgrades are relevant, compare three distinct strategies:

1. buy the preferred cabin or class outright;
2. change an existing ticket and pay the fare difference; and
3. purchase a separate cash, points, or loyalty upgrade offer.

Compare the full cost before booking. After booking, compare the additional cost, terms, and effect on the underlying fare. Do not assume a previous upgrade payment will transfer to a changed itinerary.

Separate a confirmed higher cabin from an upgrade waitlist. An empty-looking seat map is not proof that a loyalty or points upgrade will clear. If reliable sleep or comfort is important, recommend a ticket the traveler would accept even if no upgrade occurs.

Verify upgrade eligibility for the selected fare family, current loyalty benefits, waitlist rules, and refund or cancellation terms. Do not claim that a particular moment before departure is reliably cheapest. Prices may rise, seats may sell out, and desirable seats may disappear. If comparing cash and points, state the valuation assumption used.

For an existing authorized reservation, inspect reservation-specific upgrade and change offers only when authenticated access is available and permitted. Public fares do not establish a personal offer. If authentication, provider restrictions, or tooling prevents inspection, explain exactly what remains unverified and request only the smallest necessary action from the traveler.

### Handle failures and source changes transparently

If a provider site, account, or tool fails:

1. identify the failed source and the relevant error or limitation;
2. explain which fact cannot be verified as a result;
3. attempt a safe, permitted recovery or alternate source;
4. disclose the source switch and its verification limits; and
5. continue the independent work that remains possible.

Do not silently substitute sources or imply that an inaccessible checkout, membership benefit, or personalized offer was verified.

## 3. Compare complete journeys and recommend an option

Present two or three useful choices, with a clear recommendation. If only one option genuinely meets the brief, say so rather than inventing weak alternatives.

Use a compact comparison such as:

| Option | Dates and route | Product and conditions | Complete cost | Main benefit | Main drawback |
|---|---|---|---|---|---|
| [Recommended option] | [Local times, route, duration] | [Cabin/class, fare rules, luggage, seat status] | [Currency and included required extras] | [Why it best fits the brief] | [Cost, restriction, or uncertainty] |

For each option, show local times, dates, next-day arrivals, route, total duration, and realistic connection or transfer requirements. Explain timezone changes. Distinguish protected connections from independently booked tickets and identify who bears the risk if an earlier service is late.

Include practical buffers for immigration, security, station check-in, baggage, terminal changes, and travel across a city. Use larger buffers during holidays, severe-weather periods, or unfamiliar border processes. For rail or international terminal services, verify the provider's current arrival guidance and recommend a practical arrival target rather than planning around the final gate-closure minute.

Show currencies separately unless using a clearly stated conversion assumption and timestamp. Do not combine amounts in different currencies into an unexplained total. Explain what additional spending buys: less risk, a better sleep opportunity, more flexible changes, a preferred seat, a shorter transfer, or more usable time.

Lead with the recommended dates and route, followed by the decision still needed. Include when prices were checked, relevant verified links, and any important unverified details.

## 4. Prepare and complete an authorized booking

A request to find or compare transport does not authorize payment. Prepare a concrete, reviewable booking before requesting approval that is actually needed. If the traveler has already authorized a specific purchase or an adequately defined scope and price limit, proceed within that authorization without repeatedly asking merely because checkout is next.

Before submitting a booking, verify against the agreed option:

- traveler name as supplied for the booking;
- dates, local times, airports, stations, and route;
- operating provider and connection structure;
- cabin, class, fare family, and product on each segment;
- selected seat or any unassigned-seat risk;
- luggage entitlement and required extras;
- total price, currency, payment scope, and material terms.

Resolve a material mismatch before purchase. Do not invent identity details, travel-document details, payment information, or consent. Keep sensitive details only in the authorized booking process.

After purchase, confirm success from the provider's confirmation. Report the booked journey, total paid, seat status, material restrictions, and any remaining transport or check-in task. Store references and receipts in the appropriate private trip record, not in a reusable workflow or broad shareable summary.

## 5. Monitor and improve when appropriate

If the traveler requests fare or upgrade monitoring, establish an authorized, functioning mechanism before saying monitoring is active. Confirm that it can access the necessary itinerary or provider information and that it will report a useful change. Define what is monitored, such as price difference, cabin availability, seat availability, or a specific upgrade threshold.

Monitoring does not authorize a purchase. Stop it after departure, a completed upgrade, a canceled trip, or a changed plan. If scheduling, authentication, or access is unavailable, state plainly that monitoring is not running.

During active work, apply clear corrections immediately. When the traveler authorizes remembering preferences, retain durable preferences with their qualifications, such as “for overnight work trips,” and replace superseded instructions rather than accumulating contradictions. Keep temporary fares, event dates, one-off exceptions, and tentative preferences in the private trip record.

Learn from verified outcomes and traveler feedback about comfort, connection timing, disruption, and booking friction. A successful booking does not prove that the traveler was satisfied. Do not promote a one-time bargain, a lucky upgrade, or a transient provider issue into a permanent rule. If it is unclear whether a preference applies only to this trip or to future trips, ask that narrow question and preserve the existing default until it is answered.

Learning does not create additional authorization to purchase, access accounts, contact others, or retain sensitive information.


---
name: prepare-for-a-meeting
description: Research authorized context, clarify the meeting owner’s intent, and create a focused, time-bound meeting brief, agenda, and follow-up plan.
---

# Prepare for a meeting

Use this workflow to prepare one meeting. The deliverable is a practical meeting-preparation record in the user’s chosen workspace, not a research dump or a chat summary. It should help the meeting owner enter the conversation with the right context, a clear goal, exact language where useful, and a realistic close.

For several meetings, run this workflow separately for each one. Keep the research, questions, agenda, and follow-up plan distinct.

## Completion standard

A complete preparation process produces:

1. A concise situation brief that the meeting owner can read before planning is finalized.
2. Targeted questions that clarify the desired outcome and boundaries.
3. A saved record containing context, a goal, a time-bound agenda, and five critical questions.
4. A post-call review plan for consequential persuasion, negotiation, recruiting, selling, or decision meetings.
5. A verified, accessible record in the agreed workspace.

Do not stop after research. Do not turn research directly into a final agenda when the owner’s objective, authority, desired tone, or closing approach is uncertain. A short question round is usually cheaper than preparing for the wrong conversation.

## Inputs and scope

Collect or confirm:

- Meeting title, date, start and end time, duration, and the meeting owner’s timezone.
- Attendees, their relevant roles, and affiliations.
- Invitation description, logistics, scheduling notes, and linked materials.
- The meeting owner’s preferred workspace and the appropriate audience for the record.
- What the owner can decide, offer, approve, or promise during the meeting.

If the event is unclear, ask the user to identify it. A broadly useful default is to prioritize meetings with meaningful interaction, especially external one-to-one or small-group meetings, and skip focus blocks, personal events, routine status blocks, and events without a substantive conversation.

## Privacy, authorization, and access boundaries

Meeting preparation can involve information about real people. Treat it as a bounded, purpose-specific task.

Before accessing private communications, internal records, applications, evaluations, customer files, or transcripts, establish that:

- There is a legitimate purpose connected to the meeting.
- The user is authorized to access and use the source.
- The output will stay within an appropriate access boundary.
- The source is necessary or meaningfully useful for the meeting.

Use the minimum relevant information. Search narrowly first and expand only when needed. Do not assemble a broad personal profile merely because information is available.

Keep sensitive information out of broadly shared meeting records. This includes compensation or offer figures, health information, highly personal details, confidential allegations, private assessments, family information, and unrelated performance history. If sensitive context is genuinely relevant, summarize only its practical implication in a restricted briefing. For example: “There is a confidential prior discussion to resolve,” rather than reproducing details or numbers.

For hiring, assessment, and reference conversations, focus on role-relevant capabilities, role alignment, direct evidence of work, and whether an assessment distinguishes relevant performance. Do not present subjective internal comments as facts about a person. Do not place restricted evaluation material in a shared page unless that page has an appropriate restricted audience.

A name match is not identity confirmation. Before using an older record, verify identity through reliable details such as an email address, current role, organization, or confirmed relationship. If identity remains uncertain, exclude the record or label it as unconfirmed.

## Workflow

Complete the following stages in order:

1. Read and normalize the meeting details.
2. Research attendees, relationship history, and the scheduling trigger.
3. Read the written artifact that the meeting concerns, if one exists.
4. Check whether a specialized meeting workflow is needed.
5. Post a situation brief and ask targeted questions.
6. Create and save the final preparation record after receiving answers.
7. Arrange a post-meeting review when appropriate.
8. Audit the record, verify access, and surface it for use.

## 1. Read and normalize the meeting

Read the invitation in detail. Extract the title, stated purpose, timing, attendees, practical logistics, linked materials, and any rescheduling or introduction context.

Classify the likely meeting type without inventing certainty: first meeting, recurring discussion, follow-up, decision meeting, interview, reference conversation, negotiation, or information exchange. Determine the usable duration. The agenda must fit the available time, including transitions and a close.

When the invitation is ambiguous, retain the ambiguity as a question for the owner rather than assuming a purpose.

## 2. Research relevant context

Research each relevant external participant and the relationship history through authorized sources. Independent searches can run in parallel, but speed does not replace reading the evidence. Prefer recent, direct, and primary sources over old summaries or weak public profiles.

Maintain working notes that separate facts, sourced views, and inferences. A colleague’s opinion in an internal message is not a fact about the attendee.

### Communications, internal discussion, and history

Search separately for direct correspondence with the attendee and for mentions of their name, organization, project, or meeting topic. Direct correspondence explains the relationship; broader mentions may reveal introductions, proposals, planning, references, commitments, or context in which the person was not a direct participant.

Read enough relevant material to identify:

- Prior decisions, promises, unanswered questions, and concerns.
- The concrete trigger for scheduling this meeting.
- Deadlines, alternatives, dependencies, and open loops.
- Whether this is a first meeting, continuation, delayed follow-up, or recurring conversation.

Review authorized internal discussions, previous meeting notes, and calendar history where useful. For recurring relationships, summarize the relationship arc: what changed, what was agreed, what did not happen, and what remains open. State explicitly when this is a first meeting, since the opening and discovery plan should change.

### Public and organizational context

Use public sources only when they add meeting-relevant context, such as a current role, relevant work, organizational change, recent publication, or announcement. Retain only links likely to help preparation or follow-up.

When relevant and authorized, search organizational records connected to the meeting, such as a submitted proposal, prior application, program participation, advising history, account history, or hiring materials. Read the underlying artifact when it is central to the meeting; a status field alone rarely captures goals, alternatives, assumptions, or unresolved issues.

Keep sensitive material in an appropriately restricted location. In any shared page, use neutral high-level wording and omit confidential details and all pay-related figures.

Label a claim when it is old, uncertain, based on one source, or drawn from a low-quality source. Include the source and date. Do not build a challenging question on a shaky claim without clearly signaling the uncertainty.

### Working-note checklist

Capture only what is useful:

- **Who they are:** current role, relevant background, and organization.
- **What their organization or project does:** only as needed for this meeting.
- **Relationship history:** prior contact, commitments, and open loops.
- **Why now:** the scheduling trigger and stated purpose.
- **Timely context:** a relevant change, deadline, publication, or event.
- **Key links:** only useful preparation or follow-up links.
- **Known unknowns:** questions that should not become assumptions.

## 3. Read the artifact the meeting is about

If the meeting concerns a proposal, pitch, deck, draft, memo, application, strategy, or other written artifact, find and read it before drafting the agenda. Strong signals include document links, requests for feedback, references to comments, or phrases such as “the plan we discussed.”

Read the full relevant artifact, including meaningful sections, tabs, appendices, and directly relevant supporting material. Do not substitute generic discovery questions for document-specific preparation when the document is the reason for the call.

Extract the stated objective, approach, assumptions, dependencies, alternatives, constraints, deadlines, strengths, and claims that need clarification or pressure-testing. If context implies that an artifact exists but it cannot be found, ask the owner for the link during the question stage. Do not create a falsely specific agenda without it.

## 4. Check for a specialized workflow

Classify the meeting before final planning. Some meeting types need a structure other than a general agenda.

For example, a hiring reference conversation should use a reference-call workflow with consistent role-relevant evidence probes, clear separation of direct observation from hearsay, and careful comparison of themes. Formal interviews, performance discussions, legal or compliance matters, escalations, and high-stakes negotiations may also require specialized methods.

Carry forward relevant research already completed, but use the structure that fits the meeting’s actual purpose.

## 5. Post a situation brief and ask targeted questions

This is the main readiness gate. Before writing a final goal or agenda, post a concise situation brief so the meeting owner can reload the context. Then ask questions whose answers will materially shape the plan.

Questions may be skipped only when the purpose, outcome, authority, boundaries, and recurring format are genuinely documented, stable, and current. When in doubt, ask.

### Choose the brief shape

Choose the shape that fits the meeting; do not create unnecessary friction by asking the owner to choose a format.

- **Narrative brief:** who they are, where things stand, why the meeting is happening, and live tensions. This is the general default.
- **Decision-shaped brief:** the ask, alternatives and deadlines, the owner’s position, risks, and open unknowns. Use for negotiations, recruitment, fundraising, or closing.
- **Facts and dynamics:** compact facts followed by relationship or decision dynamics. Use for data-heavy situations.

Explain unfamiliar names, organizations, programs, and terms where they appear. Each section should make sense on its own. Remove names that do not affect a question or decision.

```markdown
## Situation brief

### Who they are
[Role, organization, and relevant background.]

### Where things stand
[Relationship history, commitments, and current status.]

### Why this meeting is happening
[Scheduling trigger and stated purpose.]

### Live questions or tensions
[Decision, uncertainty, risk, deadline, alternative, or disagreement that matters.]

### Useful links
- [Relevant link — what it is.]
```

### Ask targeted questions

Ask about targets, authority, approach, and failure modes—not “What agenda should I write?” Agenda design is the preparer’s job.

Cover at least the primary goal and one of failure mode, tone, authority, or specific ask. Always include an “anything else” catch-all.

Useful question axes include:

- Primary outcome: relationship building, diagnosis, decision, advice, recruiting, selling, negotiation, handoff, or commitment.
- Their situation: uncertainty about interest, role, alternatives, constraints, or readiness.
- Sensitive substance: whether to state a candid view or ask for theirs first.
- Failure mode: overselling, underselling, anchoring on the wrong issue, mishandling a sensitive topic, or leaving without a next step.
- Specific ask: a decision, introduction, commitment, feedback, resource, or follow-up.
- Authority: what can be decided live and what needs later approval.
- Anything else: history, constraints, or topics to land or avoid.

Use up to four questions per round. If five or six are genuinely necessary, split them into two rounds. Put questions in the first round that determine the useful options in the second. Do not force a false either/or when two approaches can sensibly combine.

Number questions continuously. Give every option a compact unique label. Put the evidence-based recommendation first while preserving genuine alternatives. The final round must include the catch-all.

| Question | Example options |
|---|---|
| 1. What is the primary outcome? | **1a (recommended):** Diagnose interest and secure a concrete next step; **1b:** Build the relationship only; **1c:** Make a direct proposal. |
| 2. How forward should the close be? | **2a (recommended):** Agree a date-bound follow-up; **2b:** Offer help without a commitment ask; **2c:** Leave the next step open. |
| 3. Is there anything else to land or avoid? | **3a:** Nothing to add; **3b:** I will add notes; **3c:** Keep the discussion cautious on [topic]. |

Before sending, confirm that every question is numbered, every option has one matching label, labels are unique and sequential, and the catch-all is present. In plain text, end with: “Reply with the labels, for example: 1b, 2a, 3c.”

## 6. Create and save the preparation record

Create the final record only after the situation brief, question round, and owner’s answers have shaped the plan. If this gate has not occurred, return to Step 5.

Save the record in the user’s chosen workspace with access appropriate to its contents. Use a scannable title, such as the meeting date followed by the attendee name or topic. Store the date as a date-only value unless time is explicitly needed in record metadata. Keep meeting logistics in the body rather than crowding the title.

Use this structure, adjusting time blocks to the actual meeting duration:

```markdown
# [Date] [Person or meeting topic]

## Context
[Who they are, relevant relationship history, why the meeting is happening, and useful links. State whether this is the first meeting.]

## Goal
[One or two sentences describing the intended outcome based on the owner’s answers.]

## Agenda
Text under **Say** is word for word. Anything in [square brackets] is a cue for you, not something to say aloud.

### 0–5 min: Open and frame
**Say**

[Exact opening words.]

**Interviewer note**

[What to establish or avoid.]

### 5–20 min: Diagnose [topic]
**Questions**

1. [Question]
2. [Question]

**Interviewer note**

[Signals to listen for and what needs clarification.]

### 20–35 min: Discuss, test, or propose [topic]
**Say**

[Exact transition or proposal.]

**Interviewer note**

[Specific evidence, trade-offs, or concerns to test.]

### 35–45 min: Close and create a forcing function
**Question**

1. [Specific decision, date, artifact, owner, or next-step question.]

**Interviewer note**

[Backup close if no decision is possible today.]

## 5 most important questions to ask

1. [Most decision-relevant question.]
2. [Second-most decision-relevant question.]
3. [Question that tests the key uncertainty or gap.]
4. [Question that tests the practical path forward.]
5. [Specific forcing-function close: date, artifact, owner, or next step.]

## Timely note

[Optional relevant event, publication, announcement, or deadline.]
```

Use level-three headings for agenda stages. Keep private guidance compact and separate from spoken language. Do not mix instructions into **Say** blocks; use a separate note or a bracketed cue.

The five-question section is an in-call cheat sheet, not a second agenda. It must contain exactly five ranked, one-line questions. For persuasion or gap-based conversations, include a question that exposes the meaningful gap and a forcing close. For diagnosis-only meetings, all five may be discovery questions.

## 7. Schedule a post-meeting review when appropriate

For meetings involving recruiting, fundraising, selling, negotiation, influencing a decision, or another consequential attempt to move a counterparty, schedule a one-time review roughly one hour after the meeting ends.

Within authorized systems and the correct access boundary, the review should:

1. Obtain the approved transcript or notes, using a permitted fallback if necessary.
2. Read the preparation record, relevant playbook, and a recent comparable review.
3. Write a structured review covering objective, outcome, evidence, missed opportunities, objections, decisions, next steps, and lessons.
4. Update recurring-pattern notes only with dated, concrete evidence.
5. Save the review in a restricted or otherwise appropriate location.

Skip automated review for purely informational conversations unless the user requests it.

## 8. Audit before completion

Before declaring completion, verify:

- The saved page exists in the correct workspace and is accessible to the intended audience.
- The date and duration are correct in the owner’s timezone.
- The agenda fits the meeting duration and gives the important issue enough time.
- The situation brief and targeted questions preceded final drafting, unless a stable documented recurring format justified skipping them.
- Relevant source material was actually read, especially the artifact that prompted the meeting.
- Every unfamiliar proper noun is explained where it appears or removed.
- Uncertain claims are labeled with source and date.
- Identity matching was confirmed before older records were attributed to an attendee.
- The record contains only meeting-relevant information and respects authorization, privacy, consent, and audience boundaries.
- No compensation figures, unrelated sensitive details, or restricted assessments appear in a shared page.
- The five-question cheat sheet is ranked, scannable, and includes a concrete close when appropriate.
- A post-call review is scheduled for consequential persuasion or decision meetings, or the reason for skipping it is clear.

Finally, open or surface the saved record in the user’s chosen workspace or meeting application so it is ready to use. Report the record location and any important limitation, such as a missing document, unresolved identity match, unavailable source, or restriction on where sensitive context can be stored.


---
name: capture-meeting-actions
description: Review authorized meeting records, identify genuine unfinished commitments, create clear deduplicated tasks, and batch only the questions that require judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked. Use only meeting records the user is authorized to access, for a legitimate work purpose. Collect the minimum information needed, avoid copying unrelated personal or sensitive details into tasks, and keep outputs within the access boundary of the chosen task system.

## Purpose and operating rules

Before each run, remember these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels it as an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work that was completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, statement of interest, or open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply known responsibility and delegation boundaries supplied by the user or organization. Attendance at a meeting does not make the user accountable for all work in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this broadly useful default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect only what is needed:

- Title, date, and time
- Meeting-record link or identifier
- Attendees, if relevant to ownership or follow-up
- Transcript, notes, summary, and necessary linked context

Report a compact count before processing. Do not infer actions from a meeting title alone.

## 2. Fetch and inspect complete records

Fetch full meeting records in parallel where the selected meeting system supports batching. Do not search for existing tasks yet: first identify the people, topics, and candidate outcomes that make deduplication accurate.

For long transcripts, use a repeatable search, extraction, or chunking method rather than relying on truncated previews. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by explicit acceptance

Review summary action items as candidates, then verify them against the transcript and surrounding conversation. A promise may have been conditional, reassigned, fulfilled live, or directed at another attendee.

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

- Relationship context and why the meeting occurred
- Candidate actions owned by the user
- Work completed during the meeting
- Work delegated to another named owner
- Explicit future commitments and timing
- Enough neutral context for a task to remain understandable weeks later
- Source and related links

Create no task when work was completed live, another person owns it, the meeting was purely informational and any needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

When a task concerns hiring, assessment, or a candidate, capture only role-relevant capabilities, role alignment, and diagnostic evidence. Do not include unrelated personal information or speculative judgments. Confirm whether the proposed action belongs to the user’s role or to the designated hiring owner before creating it.

## 4. Decide the task shape

Combine actions into one task when they have the same counterparty, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect months later.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

This is a readiness gate: do not proceed to task creation until each proposed task has a clear owner, unfinished outcome, sensible shape, and enough context to stand alone.

## 5. Write the task

Use the user’s chosen task system and field names. At minimum, capture:

- **Title:** short, verb-led, and specific, such as “Follow up with prospective partner about pilot scope.”
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user’s scale; default to normal important work and reserve the highest level for a real deadline, material risk, or waiting counterparty.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and links.

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: agreed date, or a reasonable reminder date before it.
- Weekly or sprint commitment: next relevant review or planning session.
- Flexible work: roughly one week, adjusted to workload.
- Older meetings processed late: move an immediate follow-up to the next workable date rather than assigning an already-passed date, unless the original deadline still applies.

Do not raise priority merely because capture happened late.

### Notes template

```markdown
[Two or three sentences of time-independent context. Include relevant absolute
dates, why this matters, the commitment, and any necessary sensitivity. Omit
unrelated personal or confidential detail.]

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

Avoid unnecessary private discussion in a task system that may be broadly visible. Follow the user’s known writing preferences. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable. If the task is to send a message, write a ready-to-send draft rather than merely saying “email them.” For introductions, use double opt-in: seek permission from each relevant party before connecting them.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by meeting link or identifier, counterparty, distinctive topic terms, and proposed title.

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. Skip the new task, or update the existing task if the meeting adds a meaningful action, deadline, or context. Record the duplicate decision so it can be reported clearly.

## 7. Create confident tasks

Create high-confidence tasks in a batch when possible. If the environment supports opening created records, open them in the selected task system rather than filling the status update with management links.

For every skipped meeting, give a brief reason, such as “No out-of-meeting commitment,” “Completed during the call,” “Owned by another role,” or “Already covered by an active task.”

Do not create uncertain tasks merely to make the sweep feel complete. Confidence requires clear evidence of ownership, an unfinished outcome, and a practical task shape.

## 8. Batch uncertain questions

Skip this step entirely when all decisions are confident. Do not interrupt for each ambiguity. Create confident tasks first, then ask all remaining questions together.

Ask the smallest question that resolves ownership, scope, timing, completion status, delegation, or duplicate handling:

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

- Add a short example or note to a reusable meeting-archetype reference when a recurring pattern affects triage, such as a common attribution error, reliable sign of in-meeting completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new delegation boundary in the user’s or organization’s maintained responsibility reference when it applies beyond one meeting.

Do not turn one-off facts, personal details, or confidential meeting content into permanent rules. Small additions to an examples or patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing steps or changing the evidence order. Briefly report any reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links to its source record where permitted.
- Message drafts are ready to send and follow the user’s preferences.
- Notes contain only the minimum necessary context and respect access boundaries.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report the essential outcome only: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and any reusable guidance changes. Keep status updates terse and factual.


---
name: turn-a-message-into-a-task
description: Read the full conversation, identify the real outcome, prepare safe drafts and research, and create a trackable task only when tracking adds value.
---

# Turn a message into a task

Use this workflow when one or more message links, copied messages, or conversation references may contain work that should be researched, drafted, tracked, or handed off. Run the flow separately for each supplied reference unless several references clearly concern one shared request.

The purpose is not to log a vague to-do. Do as much useful work as is safe, authorized, and proportionate, so the remaining human action is obvious and small. A task with empty notes or no useful preparation is usually not a useful result.

Before accessing messages, documents, personnel information, email, calendars, or task records, confirm a legitimate purpose and clear authorization. Use the minimum relevant sources and details. Do not expose unrelated private, employment, health, financial, or relationship information in research, drafts, reports, or task notes.

## 1. Read the complete conversation

Start with the linked message, but do not assume it contains the whole request.

1. Identify the message location, conversation, and message identifier from the link or reference.
2. If the reference points to a reply, retrieve the parent and the entire thread. The linked reply is the anchor, but the full thread gives it meaning.
3. If it points to a top-level message, retrieve a small window around it. If it has replies, retrieve the whole thread immediately.
4. Identify relevant participants. Resolve unclear names through authorized profile information or explicit mentions only when necessary. In notes, use a name or role rather than vague labels.
5. Record the actual request, promises already made, deadlines, linked materials, decision points, and changes of owner.
6. Read the newest replies especially carefully. A later reply may resolve the ask, revise the deadline, reassign ownership, or make tracking unnecessary.

Do not create a task for completed, superseded, or clearly delegated work. If completion seems likely but remains ambiguous, explain the evidence and ask whether tracking is still wanted.

### Conversation-reading checks

- Read the parent before interpreting a reply.
- Treat newer replies as higher-priority context than the initial message.
- Follow materials directly linked from the thread when they are relevant.
- If a retrieval method returns no exact match, retry with a small surrounding time window or a thread-specific retrieval method rather than assuming there is no context.
- Do not copy unrelated private discussion into the task record.

## 2. Classify the real task

State the task shape in working notes before researching. The category determines what “pre-completed” should mean.

| Task shape | Deliverable | Useful preparation |
|---|---|---|
| Reply owed | An answer, feedback, confirmation, or recommendation | Draft a concise reply with verified facts and clear next steps. |
| Artefact owed | A document, introduction, analysis, reference, or data extract | Draft or assemble the artefact itself. |
| Decision needed | A choice reserved for the user or authorized owner | Prepare options, evidence, trade-offs, and a recommendation. |
| Follow-up or delegation | A chase, scheduling action, handoff, or process step | Draft the follow-up or prepare the action for approval. |
| Multi-part request | Several related outcomes | Keep one task with sub-parts unless ownership or timelines materially differ. |

Rewrite the request as an outcome, not a message label. For example: “Review the proposal and send a decision by Friday,” not “Message in project chat.” Separate work owned by the user from work owned by other people.

Default to one task for one conversation, even when it contains several related asks. Split it only when the components have different accountable owners, different deadlines, or materially different tracking needs.

## 3. Gather only context that changes the outcome

Choose sources according to the request. Do not run a blanket search because retrieval is available. Stop when you can complete the work, make a supported recommendation, or name the exact missing information.

Typical source mappings include:

- **Person-related work:** authorized correspondence, meeting notes, work records, or role-relevant evidence. For hiring or assessment, focus on demonstrated capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance.
- **Project or event work:** recent conversation history, project plans, approved documents, schedules, and relevant linked files.
- **Data questions:** source-of-truth records, approved reports, retrospectives, and operational correspondence that documents dates, counts, or process facts.
- **Repeated requests:** search authorized conversations by topic as well as participant. One well-supported response may serve several requesters.
- **Linked documents:** read relevant contents, including relevant tabs, sheets, sections, or pages. A message may mention only one item while a linked document contains the real list of decisions or asks.
- **Policy or compliance questions:** retrieve the applicable policy and approved precedent before drafting advice. Do not infer policy from informal chat.

Use public web research only when it is appropriate, permitted, and necessary. Prefer non-interactive retrieval where available, and never submit private material to public services. Do not invent URLs, statistics, deadlines, policies, or citations. Verify them, omit them, or mark gaps clearly, for example: `[VERIFY: confirm current budget figure]` or `[SEARCH: applicable travel policy]`.

### Research readiness gate

Before moving forward, answer all of these:

- Can the requested deliverable now be drafted or assembled?
- Are important factual claims supported by a relevant source?
- Is there a decision only the user can make?
- Is the missing information necessary, rather than merely nice to have?

Two or three strong sources are normally better than many shallow ones.

## 4. Pre-complete the work safely

Do as much as is reasonable without taking irreversible action.

- Draft replies, emails, documents, decision briefs, follow-up messages, or data summaries.
- If the user has supplied a writing guide, approved examples, or a style profile, read it before writing in their voice.
- Keep messages, emails, calendar invitations, submissions, purchases, approvals, and status changes as drafts unless explicit authority covers execution.
- If the messaging system supports drafts, stage the draft in the correct thread. Include the same text in task notes so the record remains useful outside that system.
- Format drafts for their destination. In chat tools, preserve blank lines needed for native lists; avoid unnecessary lead-ins before a list.
- Keep reply drafts shorter than first instinct. Lead with the answer, request, or decision. Include coaching or extended explanation only when that is the purpose of the reply.
- Route spending, approvals, and exceptions through the established process rather than making an informal commitment.

For a decision, provide two or three realistic options, evidence for each, a recommendation, and the reason for it. Do not give the user an unstructured survey when a supported recommendation is possible.

When a detail depends on the user’s memory, judgment, or relationship knowledge, preserve the draft structure and insert a direct placeholder:

`[FILL IN: one concrete example of the collaboration outcome]`

Warn clearly that a draft with placeholders is not ready to send. List remaining actions specifically, such as “Confirm whether you are willing to be named as a reference,” rather than “Review and complete.”

## 5. Ask questions only for genuine blockers

Before asking, check whether the user already answered the issue in an authorized earlier message, planning note, or email. A documented stance should normally guide the draft rather than create a new interruption.

Ask only when a wrong assumption would waste more time than a focused question. When blocked:

1. Give a one- or two-paragraph context recap: who is involved, what has happened, what is now requested, and the relevant tension.
2. Ask two to four targeted questions.
3. Allow multiple selections and a custom answer when options can be combined.
4. Apply the answers directly to the draft before creating the record.

Do not ask for information that can be safely verified. Do not ask broad questions such as “What do you think?” when a specific decision fork can be named.

## 6. Decide whether a task record helps

A task record is for deferred, trackable work, not proof that a message was read.

Skip the record and provide the result directly when the remaining work is one short sitting, such as reviewing a staged reply, making a small edit, and sending it. As a useful default, chat-only is appropriate when the remaining effort is about 15 minutes or less and there is nothing to wait for.

Create a record when at least one condition applies:

- Work must happen later or cannot reasonably be completed now.
- A deadline, event, dependency, or another person’s response needs tracking.
- Several remaining steps are spread across days.
- The user explicitly requested a task record.
- The work must remain visible to an owner or team after the conversation closes.

When uncertain, prefer chat-only for simple reply tasks and a record for longer-lived work.

## 7. Create a high-quality task record

Use the user’s chosen task system and verify field names, valid values, linked categories, and permissions before writing.

| Field | Standard |
|---|---|
| Title | Imperative, specific, short, and describes the finish line. |
| Status | The system’s active, not-started state. |
| Owner | The person accountable for remaining work. |
| Due date | An explicit or clearly implied deadline; otherwise leave blank. |
| Priority | Estimate from impact and time sensitivity; someone waiting generally increases urgency. |
| Time estimate | Remaining human effort only, not research already completed. |
| Area or project | The best verified category, project, or domain. |
| Notes | Context, source, preparation completed, and exact remaining actions. |

Use this notes template:

```markdown
**What:** [One-line statement of the ask and who is waiting.]
**Source:** [Conversation link or message reference]

**Context:**
- [Relevant background and verified fact]
- [Deadline, dependency, or decision constraint]
- [Authorized supporting source, if useful]

**Pre-completed:**
[Full draft reply, artefact, or decision brief. State where a communication draft is staged.]

**Remaining for the owner:**
- [Specific final action]
- [Specific verification, approval, or follow-up]
```

Do not paste an entire private conversation when a concise context summary will do. After creating the record, reopen or retrieve it and confirm that the title, owner, status, due date, notes, and links saved correctly.

## 8. Report the result clearly

If a record was created, report in this order:

1. What the task is.
2. What was pre-completed and where any draft is staged.
3. Metadata assumptions: priority, due date, and remaining effort.
4. Any `[VERIFY]` or `[FILL IN]` items that prevent completion.

If no record was needed, separate the briefing from the deliverable. Put the deliverable last so it can be copied without cleanup:

```markdown
## Context for the user (not part of the reply)
- [Ask, requester, key facts, assumptions, and verification flags]
- [State whether a draft is staged and where]

## The reply
[Draft verbatim]
```

Nothing should follow the final reply block.

## 9. Run an authorized draft-to-outcome review

When a communication draft is staged, schedule a follow-up review only if the user has authorized continued access to the thread and such reminders are appropriate. A useful default is to check after roughly one hour.

The review should identify each staged draft, its conversation location, and where its original text can be found. Then:

1. Re-read the relevant thread and determine whether a message was sent.
2. If it was sent, compare the sent version with the staged draft.
3. Extract general, non-sensitive lessons: preferred length, wording, ordering, formatting, approval routing, missing context, or retrieval quirks.
4. Record lessons only in an approved learning location within the authorized access boundary.
5. If no message has been sent, reschedule a limited number of checks at increasing intervals, then stop. Non-sending may be deliberate.

## 10. Improve the workflow through approved maintenance

After each run, conduct a brief internal review. Capture only reusable lessons, such as a source type that was essential, a retrieval workaround, a recurring task shape, or a user correction that should change future handling.

Keep changes small and general. Do not preserve personal anecdotes, sensitive facts, or one-off names as operational rules. Apply updates only through an approved maintenance process. A no-change outcome is valid when nothing general was learned.

## Final audit

Before finishing, confirm:

- The complete relevant thread was read.
- Newer replies did not already resolve the work.
- Research was relevant, authorized, and minimal.
- Facts and links were verified or explicitly marked as gaps.
- No external action was sent or executed without authorization.
- The remaining action is concrete and proportionate.
- A task record exists only when tracking adds value.
- Any staged draft has an authorized, bounded outcome-review plan.
- The output stays within the appropriate privacy and access boundary.


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
description: Prepare, conduct, and document an authorized hiring reference call using role-relevant evidence, tailored questions, and clear decision boundaries.
---

# Run a reference call

Use this workflow to prepare and conduct a reference call for a hiring decision. Its purpose is to gather specific, role-relevant evidence about past performance—not to collect vague praise or private personal information. Use it only when the candidate has provided the referee or otherwise clearly authorized the reference check, and when the organization has a legitimate hiring purpose.

Keep research and notes within the access boundary of the hiring process. Use the minimum relevant information, do not include unrelated personal details, and do not share referee comments outside the people who need them for the decision.

## Outcome

Create a single meeting record or call brief before the conversation. It should let the caller quickly understand:

- who the referee is and how they know the candidate;
- the role and decision stage;
- the candidate evidence or open questions that need testing;
- tailored questions, including role-specific probes;
- links to authorized candidate materials and relevant prior hiring records;
- a structured place to capture evidence, limitations, and follow-up actions.

The meeting record—not an external research summary—is the working deliverable. Use the organization’s approved calendar, applicant-record, notes, and meeting-record systems.

## Inputs and readiness gate

Collect or confirm the following before preparing the call:

| Input | What to confirm |
|---|---|
| Candidate | Name, role, hiring stage, and authorization for the reference check. |
| Referee | Name, contact details, organization or role if known, and relationship to the candidate. |
| Call details | Date, time, meeting link or dial-in details, and attendees. |
| Decision context | Role outcomes, relevant interview or work-sample evidence, open questions, and next decision point. |

Do not proceed as though a reference is confirmed if the referee’s identity, contact information, or authorization is unclear. Resolve the uncertainty with the candidate or hiring coordinator. If no call is scheduled, create a draft brief with the missing scheduling detail clearly marked.

## 1. Find the call and confirm the relationship

Check the approved calendar or scheduling record using the referee’s name or contact details. Record the meeting title, time, attendees, connection information, and any scheduling context.

Then confirm the relationship from the candidate’s reference list or other authorized hiring correspondence:

- What was each person’s role?
- Did the referee manage, work alongside, advise, serve as a client of, or teach the candidate?
- How long did they work together?
- How closely did the referee observe the work relevant to this role?

Direct observation matters more than seniority, confidence, or a prestigious title. If the referee only knows the candidate socially or indirectly, document that limitation and adjust the questions accordingly.

## 2. Gather only relevant context

Review authorized hiring records and direct correspondence for the candidate and referee. Search approved internal records for prior meetings or legitimate work history with the referee, if relevant. Review the most recent and most relevant items rather than collecting everything.

Research should answer these practical questions:

- What outcomes will the new role own?
- What evidence already supports or challenges the candidate’s fit for those outcomes?
- What does this referee uniquely have firsthand knowledge of?
- Are there prior completed references for this candidate, and what claims should be independently checked?
- Are there existing professional connections, collaborations, or conflicts that could affect candor or interpretation?

Use public professional information only when it improves question selection or verifies the referee’s professional context. Do not investigate sensitive personal characteristics, private life, protected traits, or irrelevant online material.

If reviewing earlier reference notes, treat them as hypotheses, not facts. Do not tell a later referee that another person made a negative comment. Instead, test the underlying issue neutrally: ask for examples of execution, feedback response, reliability, collaboration, or another relevant capability.

## 3. Turn research into a call brief

Write concise bullets, not a long narrative. Separate sourced facts from questions or inferences. Include links only to materials the call participants are authorized to access.

Use this template in the organization’s meeting-record system:

```markdown
# [Date] — [Referee] ([Candidate] reference)

## Context
- **Referee:** [Professional role, organization, and relevant background or profile link.]
- **Relationship:** [How the referee worked with the candidate, when, and how closely.]
- **Hiring context:** [Role, decision stage, major outcomes, and next step.]
- **Candidate materials:** [Authorized applicant profile, portfolio, work sample, or professional profile links.]
- **Other references:** [Known referees or “Not yet confirmed.”]
- **Call logistics:** [Time, connection details, and attendees.]

## Opening
> Hi [Referee], thanks for making time. I’m [Name] and I’m calling as part of [Organization]’s hiring process for [Candidate]’s application to [Role]. [Candidate] listed you as a reference because of your work together on [context]. I’m hoping to understand specific examples of their work, how they operate, and the environment where they do their best work. Your comments will be used internally for this hiring decision.

## Briefing notes
- **What to validate:** [Specific role-relevant claim or uncertainty.]
- **What this referee can uniquely address:** [Directly observed work, project, or period.]
- **Prior evidence to cross-check:** [Neutral question to test a theme; do not attribute private comments.]
- **Interpretation limits:** [Potential bias, limited observation, or conflict to keep in mind.]

## Questions
- [Tailored questions and role-specific probes.]

## Notes during call
- **Observed examples:**
- **Referee interpretation:**
- **Evidence relevant to role outcomes:**
- **Concerns or development areas:**
- **Limits on confidence:**
- **Follow-up or decision implications:**
```

## 4. Write actionable briefing notes

Briefing notes are the highest-value part of preparation. They should tell the caller what to learn, why it matters, and how to test it fairly.

Write direct, evidence-focused prompts. For example:

- “The work sample showed strong analysis but limited evidence of delivery under changing requirements. Ask for a project where priorities changed and what the candidate did.”
- “This referee managed the candidate during a rapid-growth period. Ask what systems the candidate built, what failed initially, and how they improved it.”
- “This is the first reference. Capture concrete examples of strengths, support needs, and working style so later calls can independently test those themes.”

Avoid leading language such as “Confirm that they miss deadlines.” Prefer: “Tell me about a time delivery was at risk. What did the candidate own, and what happened?”

## 5. Conduct the call

Open by confirming the referee’s relationship and explaining the internal hiring purpose. Respect their time and invite candor without promising confidentiality beyond the organization’s legitimate hiring process and applicable policy.

Ask a unified set of questions, adapting based on the referee’s answers:

- How did you work together, and how closely did you observe their work?
- What did the candidate personally own or deliver? What was the result?
- What did excellent performance look like in practice?
- What is their standout strength? Please give an example.
- Where did they need the most support or development?
- Tell me about difficult feedback, a setback, or a changing priority. How did they respond?
- If they were unsuccessful in a similar role after a few months, what would be the most likely reason?
- What management approach or work environment would help them contribute most effectively?
- Compared with people you have directly worked with in similar responsibilities, how would you characterize their performance, and why?
- What have I not asked that would be important for this role?

Follow vague praise or criticism with: “What did that look like?”, “What did they personally do?”, “What was the outcome?”, and “How often did you observe that?” Do not pressure the referee to answer questions outside their knowledge.

### Role-specific probes

Choose three to five probes tied to the role’s real outcomes. Examples:

- **Operations or program delivery:** handling ambiguity, building repeatable systems, prioritizing competing work, stakeholder communication, and reliable execution.
- **Community or partnership work:** building trust, resolving conflict, maintaining boundaries, engaging diverse stakeholders, and turning feedback into improvements.
- **Leadership roles:** setting direction, developing others, making tradeoffs, managing budgets or external relationships where relevant, and scaling processes without unnecessary bureaucracy.
- **Technical or analytical roles:** quality of judgment, explanation of complex work, collaboration, ownership, debugging or problem solving, and learning from review.

## 6. Record and assess signal

Capture notes during or immediately after the call. Keep three categories distinct:

1. **Observed evidence:** concrete projects, behaviors, outcomes, and examples.
2. **Referee interpretation:** the referee’s judgment about strengths, limitations, or comparative performance.
3. **Hiring inference:** what the information may mean for this role and what remains uncertain.

Record confidence based on firsthand observation, specificity, recency, consistency with other evidence, and relevance to the role. A strong endorsement without examples is weak evidence; a specific account from a close manager is stronger, but still not a final verdict.

## 7. Audit before closing the record

Check the completed record against this list:

- Is the candidate’s authorization and the hiring purpose clear?
- Does the record explain the referee’s relationship and observation limits?
- Are questions linked to role-relevant capabilities and real hiring uncertainties?
- Are claims supported by examples rather than only adjectives?
- Are prior-reference themes tested independently rather than repeated as rumor?
- Are sensitive or unrelated personal details omitted?
- Are observations, interpretations, and hiring inferences clearly separated?
- Is access limited to the appropriate hiring decision-makers?

Do not let one call decide the outcome by itself. Compare reference evidence with interviews, work samples, and the role’s actual requirements. Escalate material contradictions, unsupported serious allegations, or process concerns to the appropriate hiring lead or people-policy owner rather than trying to resolve them through speculation.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive method, protecting account context, verifying page state, and separating preparation from commitment.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing forms, changing settings, collecting rendered-page data, testing a user flow, or using an authenticated dashboard. Use it when a simple page retrieval, supported API call, or static request cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not perform a consequential final action until the page state, target, and authorization are clear.

A browser automation command succeeding does **not** prove that a website accepted the change. Modern applications may maintain internal state separately from the visible DOM, commit data only after focus changes, replace controls during a re-render, or show a cosmetic error after an action already completed.

## 1. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented and authorized programmatic interface when it can perform the requested work. It is often more reliable than reproducing a browser interaction.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, and forms that do not require the user’s existing signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an established session, single sign-on state, account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for a direct route. Check official documentation, ordinary form actions, page source, and visible network activity for supported endpoints. A form may send structured data to an authorized service that can safely be used directly.

Do not use undocumented interfaces to bypass access controls, consent boundaries, contractual restrictions, or other safeguards. Do not use an authenticated visible session merely because it is convenient: it may interrupt the user’s work and increases privacy and account risk.

If a site blocks automated browsing, do not attempt to evade its protections for casual research or collection. A user-visible session can be appropriate only when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and the established session is necessary. Do not weaken browser security, access controls, warnings, bot checks, or anti-abuse protections.

## 2. Protect identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into notes, screenshots, logs, or reports. Keep outputs within the requester’s appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated context, identify the correct account, organization, environment, and browser profile. Never infer identity from a generic browser-window name, an old tab title, a remembered default, or a connection label.

Use these rules:

- Announce when taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Classify the intended context explicitly: for example, personal, work, testing, staging, or production.
- Select the browser profile or connection that matches that context instead of relying on a generic browser selector.
- Confirm the signed-in account with a reliable account indicator before opening or changing the real target.
- If the required account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not reveal credentials, session tokens, recovery information, private account data, or security settings in output or logs.
- Do not disable multi-factor authentication, browser warnings, security controls, or access restrictions to make automation easier.

Use an account preflight gate before actions that change data. Confirm the account identity, environment, and target object. If the automation system has a verification marker or permission gate, mark the context verified **only after** the account check has passed. Never create or enable such a marker in advance merely to unlock actions.

A useful pre-action question is: **Which account is this? Which environment is this? What exact item will change?** Resolve any uncertainty before proceeding.

## 3. Establish the task boundary and authorization

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, or workflow.
- The information that will be entered, collected, changed, or uploaded.
- The minimum information needed to complete the request.
- Whether the final action is reversible.
- Whether the work includes sending, publishing, paying, deleting, granting access, changing a plan, or another external commitment.
- Missing information, ambiguous choices, and fields that require the user’s judgment.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and collecting a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, or applying a permanent account change may not be.

Honor an explicit request to review before submission. If the user has already clearly authorized a specific final action, do not repeatedly ask for the same approval. If final authorization is missing, prepare and verify the complete result, show a concise pre-submit state, and ask only for the final action.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify all values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** After required confirmation, re-check the account, target, and readiness gate. Then perform the final action once.

If the page reloads, re-renders, or the session changes between passes, do not assume earlier state remains valid. Restore and verify the intended values again before committing.

## 4. Inspect the rendered page before editing

Do not begin by guessing selectors, filling fields by numeric position, or trusting a visual approximation. First inspect the rendered page and collect enough structure to identify controls safely.

For each relevant field, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or label relationship.
- Current value and whether the field is required.
- Validation rules, character limits, formatting behavior, and disabled state.
- Whether an apparent field is the editable control, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, date, or tab causes the page to re-render.

Address controls by stable semantic identity, such as visible label text, an accessible name, or an explicit label relationship. Do not use DOM indexes where labels are available: dynamic applications may change element order between loads or after re-rendering.

Before changing a record or setting, inspect its current state. This prevents modifying the wrong item or overwriting existing values unintentionally.

### Generic form inspection pattern

Use a page-inspection capability to list relevant controls before writing fill logic. The exact automation library is user-selected, but the inspection should record at least tag, input type, role, label, required state, and current value or text length.

```js
// Pseudocode: adapt to the selected browser automation library.
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

## 5. Use the correct interaction for each control

Different controls need different interactions. A generic “set value” operation is not reliable for all of them.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use the normal text-input mechanism. | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away. | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus the true editable element, select existing text, enter text through keyboard-style events, then blur. | Direct DOM mutation may not update the application’s internal model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle. | Selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed. | A click can toggle an already-correct value. |
| Date/time picker | Choose date and time, close the widget safely, then verify the rendered summary. | Popovers can reinterpret typing or clear related fields. |
| File upload | Confirm the file, destination, and privacy implications first. | Uploading may start immediately and be difficult to undo. |

For framework-driven editors, simulate normal user interaction rather than writing directly to low-level page properties. A robust general sequence is:

1. Focus the actual editable element.
2. Select existing content.
3. Delete it.
4. Enter the new text with keyboard-style events.
5. Move focus to a neutral page element.
6. Wait briefly for the application to commit or render.
7. Read the resulting value back.

Some forms pair a visible rich-text editor with a hidden input. Editing the hidden input may appear successful in a DOM dump while server-side validation treats the visible editor as empty. Target the control that the user interacts with and that the application actually reads. If a generic accessibility locator points to an empty wrapper, inspect the underlying editable element and follow its label relationship.

If changing a dropdown, checkbox, tab, or date can refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterwards and confirm earlier entries remain present.

## 6. Verify after every meaningful edit

After each field is filled or setting is changed, read its value back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare lengths, required state, or a minimal redacted summary rather than exposing full values unnecessarily.

Check for these common mismatches:

- The automation layer reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displayed text but did not retain it internally.
- A later action erased an earlier field after a re-render.
- A hidden synchronization field was changed instead of the visible editor.
- A selection changed a dependent field, date, recipient, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once using a more appropriate interaction method, then verify again. If the page continues to reject or alter the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

Avoid clipboard-dependent automation unless the environment explicitly supports it and the data handling is appropriate. Clipboard permissions can differ between headless and visible browser contexts. Use controlled text-entry methods where possible.

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

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only through an appropriate access boundary. Avoid exposing sensitive form values in a large inline table when a short summary and securely available record are sufficient.

### Readiness checklist

- [ ] The account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 8. Treat one-way actions as a distinct phase

The following generally need explicit confirmation immediately before the final control is activated unless the user has already clearly authorized that exact action:

- Sending messages, invitations, or notifications.
- Publishing content.
- Submitting an official or externally reviewed form.
- Making a payment or purchase.
- Deleting records or files.
- Changing subscription, billing, access, ownership, or security settings.
- Actions labeled permanent, final, irreversible, or impossible to edit later.

Present a concise confirmation request containing the target, important values, recipients or audience, cost if any, irreversible effects, and open questions. Then wait for confirmation before activating the final control.

For low-risk reversible changes explicitly requested by the user, such as adjusting a preference or updating a draft, proceed after normal verification unless the page presents an unexpected warning or broader impact.

## 9. Confirm completion after acting

A button click is not proof of success. After the final action, look for reliable evidence such as a success message, confirmation reference, newly created record, persisted saved setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Do not represent an attempted action as completed.

## 10. General failure patterns and recovery rules

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change. | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after editing a later one | A component re-render reset uncommitted state. | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used. | Find a multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node. | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited. | Use the visible interactive control that the application actually reads. |
| Automation becomes unstable on a complex page | The chosen automation layer is unsuitable. | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers show different behavior | The site varies behavior by browser context. | Prefer an authorized direct interface; if needed for an explicit task, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior. | Close it through a neutral page action and re-verify affected fields. |
| A visible error may be cosmetic | The task may already have completed. | Inspect resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |
| A bot check or security-key prompt appears | The site requires user presence or authentication. | Ask the authorized user to complete that step; do not bypass it. |

## 11. Maintain and improve the workflow safely

When a real failure or useful new pattern occurs, record the general lesson in the workflow or local operating documentation. Capture the symptom, likely cause, safe fix, and verification method together. Consolidate recurring lessons rather than accumulating long lists of site-specific anecdotes.

Keep implementation details current. Automation libraries, browser versions, selectors, and access methods change. Validate that a technique still works before relying on it for consequential work. Do not preserve outdated workarounds merely because they succeeded once.

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
- [ ] Explicit confirmation was obtained immediately before an unapproved consequential final action.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: Design, test, improve, evaluate, and package a reusable AI skill from a new idea, an existing draft, or a demonstrated workflow.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, improve an existing one, evaluate whether it helps, or refine when it activates. A skill is a focused set of instructions, with optional scripts, references, and templates, that helps an AI perform a recurring task reliably.

The basic loop is:

1. Define the job and its boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements where useful.
5. Improve the skill based on evidence.
6. Repeat until it is useful, reliable, and not narrowly fitted to its tests.
7. Optionally improve the description used to decide when the skill should activate.

Adapt the process to the user's needs. Some users want a quick collaborative draft; others need a careful evaluation. Determine where the user is in the loop, then help them take the next useful step. Do not insist on extensive testing when the user explicitly prefers a lightweight review, but explain the tradeoff when the skill will support repeated, consequential, or objectively checkable work.

## Communication principles

Use plain language by default and match the user's technical experience. Terms such as *test*, *evaluation*, and *benchmark* may be helpful, but explain unfamiliar terms briefly. Avoid unexplained technical language such as “JSON,” “schema,” or “assertion” unless the user is comfortable with it.

Explain why a question matters. For example:

> What should a successful result look like: an answer in chat, a structured report, a file, or an external action? The answer determines how completion can be checked.

Keep the user involved at key decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before selecting a restrictive scope, required tool, or approval policy.
- Share proposed test cases before treating them as representative.
- Let human judgment lead when success is subjective, such as writing quality, visual design, tone, or strategic usefulness.
- State assumptions and limitations rather than silently inventing requirements.

If the task uses records, messages, files, or information about people, require a legitimate purpose and clear authorization. Use only the minimum relevant information and sources, exclude unrelated sensitive details, and keep outputs within the user's appropriate access boundary.

## 1. Identify the starting point

First identify which situation applies.

### A. New skill

The user has an idea for recurring work. Begin with discovery, scope definition, and a first draft.

### B. Existing skill or draft

The user has existing instructions and wants to edit, simplify, test, or optimize them. Read the current version before suggesting changes. Preserve its established name and identity unless the user requests a rename.

### C. Workflow demonstrated in the conversation

The user may ask to turn a recent interaction into a skill. Extract what is already known before asking repetitive questions:

- Inputs and source materials used.
- The sequence of decisions and actions.
- Available capabilities or tools.
- Corrections and preferences the user supplied.
- Expected output format and quality criteria.
- Conditions that changed the approach.

Summarize the inferred workflow, identify gaps, and ask the user to confirm it. Do not promote a one-time workaround into a general rule without checking that it applies broadly.

### D. Evaluation or optimization request

The user may have a mostly complete skill and want to know whether it improves outcomes. Start with test design and evidence gathering. Do not rewrite an existing skill merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough detail to define a coherent job. Ask only the questions that are still unanswered and materially affect design.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What requests, wording, or situations should cause the skill to be used?
3. **Inputs:** What information, files, examples, systems, references, and permissions may it use?
4. **Outputs:** What should it produce, change, or communicate? Is a specific format required?
5. **Success:** How will the user decide the result is correct, safe, or useful?
6. **Boundaries:** What should it not do? When should it ask, decline, or return work for human review?
7. **Variation:** Which common cases, difficult cases, and exceptions matter?
8. **Dependencies:** Does it need a particular capability, template, script, reference, or approved source?
9. **Testing:** Should it be tested with representative requests before delivery?

Offer choices when they make a decision easier:

- “Should the skill make a best effort when information is missing, or pause and ask?”
- “Should the output be concise, detailed, or selectable by the user?”
- “Should it work from any supplied source, or only sources the user has approved?”
- “Can it take actions outside the conversation, or should it prepare a reviewable draft first?”

Recommend testing when outputs are objectively verifiable, the workflow will be reused, errors would matter, or the skill makes files or external changes. For subjective creative work, a small human review set may be more valuable than artificial numerical scoring.

### Research before drafting

When relevant documentation, comparable skills, templates, standards, or user-approved reference materials are available, review them before drafting. Research should reduce burden on the user, not replace the user's authority over requirements.

Use research to identify:

- Existing conventions and output standards.
- Constraints imposed by file formats or available capabilities.
- Reusable methods for comparable tasks.
- Safety, privacy, compliance, and approval requirements.

If sources conflict or a requirement is uncertain, surface the uncertainty and seek guidance rather than guessing.

## 3. Choose a maintainable structure

A skill should be focused enough that both users and AI systems can predict what it does. A single skill may support related variations, but separate unrelated jobs when they have different audiences, source permissions, tools, or completion criteria.

A typical package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed guidance
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata:** A concise name and description used to determine whether the skill applies.
2. **Core instructions:** The workflow needed in most uses.
3. **Supporting resources:** References, templates, and scripts loaded only when needed.

Keep the core file readable. If it grows large, move specialized guidance into clearly named reference files and state exactly when each reference should be consulted. Give lengthy references a contents section or other navigation aid.

For multi-variant skills, organize resources by variant. For example, a skill supporting several hosting environments can keep the shared selection workflow in its core instructions and place each environment's details in a separate reference. The AI should read only the relevant reference rather than loading every variant.

### Bundle deterministic work carefully

If repeated test runs reconstruct the same helper procedure, consider bundling a script or template. This is useful for repeatable file conversion, validation, data cleanup, document generation, or calculations.

Add a reusable helper only when it is:

- Deterministic or easier to verify than improvised reasoning.
- Reused across realistic requests.
- Safer or less error-prone than recreating the procedure.
- Clearly within the user's approved access and action scope.

Document what it does, its inputs, outputs, limitations, and when not to use it. Do not add automation merely because it is possible.

## 4. Write the skill

Write clear instructions in imperative language. Explain the reason behind important steps, particularly when they prevent predictable quality, safety, or authorization failures. AI systems tend to handle variation better when they understand the goal and tradeoff instead of receiving a long list of unexplained rules.

Use the following sections as applicable.

## Purpose and scope

State the job, intended use, and boundaries. Specify whether the skill creates an answer, produces a file, takes an action, or guides a user through a process.

## Inputs and prerequisites

List required inputs, permitted sources, necessary capabilities, and optional information. Say what to do if something required is absent.

Example:

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If an essential source is unavailable, ask for an export or prepare a clearly marked incomplete draft.
```

For people-related information, state that the skill should use only information necessary for the authorized purpose and should omit unrelated personal or sensitive details.

## Workflow

Describe the normal sequence of work and meaningful decision points:

1. Inspect the request, inputs, and authorized sources.
2. Clarify only ambiguities that would materially change the result.
3. Gather evidence from approved sources.
4. Perform the requested work using an appropriate method.
5. Check the result against requested format, constraints, and success criteria.
6. Present the result with assumptions, evidence, and unresolved limitations.

Use conditional rules where they genuinely help:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested change could overwrite important work or cause an external effect, explain the impact and request confirmation before proceeding.
```

## Output format

When consistency matters, define a clear template:

```markdown
# [Title]

## Summary
[Brief conclusion]

## Findings
- [Finding and supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or needed follow-up]
```

Do not impose rigid formatting when adaptation is more valuable. For flexible tasks, provide goals, ordering preferences, and a small generalized example instead.

## Quality, safety, and privacy checks

State the checks required before completion. Depending on the task, this may include validating calculations, checking required fields, preserving original data, citing key sources, distinguishing verified facts from assumptions, or flagging uncertainty.

Skills should act in ways a user would reasonably expect from their description. Do not conceal actions, bypass authorization, extract confidential material, damage systems, or support unauthorized access. Pause for confirmation before irreversible, external, or high-impact actions unless the user has clearly authorized them.

## Failure behavior

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable source or capability:** Explain what cannot be verified and offer a safe alternate method.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, report the issue, or request guidance.
- **Permission-sensitive work:** Confirm authority before accessing, sharing, changing, or publishing information.

## Examples

Include only a few short generalized examples, and only where they teach a distinct pattern. Examples should demonstrate reasoning and output shape, not substitute for the workflow.

## 5. Write a useful activation description

The description is a routing instruction. It should say both what the skill does and when it applies. Include realistic language users may use even when they do not name the skill directly.

A strong description includes:

- The task or intended outcome.
- Common contexts that indicate the task.
- Scope limits needed to avoid costly or unsafe false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user requests a progress update, leadership summary, milestone review, risk overview, or concise account of next steps, even if they do not say “status report.”
```

Do not put the full procedure in the description. Avoid vague labels such as “help with documents,” and avoid making the description so broad that it captures adjacent work better handled by another skill.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and appropriately bounded?
- Does the description clearly identify when to use it?
- Are inputs, permissions, outputs, and completion criteria clear?
- Does the workflow explain why key checks matter?
- Does it explain what to do when information is incomplete?
- Is it free of private conventions, assumed access, or undeclared tools?
- Are instructions lean enough to support normal variation?
- Does it protect confidential and personal information appropriately?

Excessive absolute wording is a warning sign unless the rule expresses a true safety, legal, or authorization boundary. Prefer intent-based instructions that help the AI make sound decisions in new situations.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic test prompts. Share them with the user and ask whether they represent real usage or need adjustment.

For every test case, record:

- A descriptive identifier.
- The user prompt.
- Any files or supporting context.
- The expected outcome in plain language.
- Objective checks, if suitable.

Example portable format:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates. Clearly flag information that cannot be verified.",
      "expected_output": "A structured summary separating supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover different meaningful situations:

- A typical successful request.
- Incomplete, conflicting, or ambiguous input.
- A format-sensitive or policy-sensitive request.
- A realistic edge case that changes the workflow.
- A request requiring approval, careful handling of information, or refusal, when relevant.

Vary wording, detail level, and user style. Do not simply repeat the skill's language in tests. Avoid including private personal scenarios or sensitive records unless the testing is authorized and uses only the minimum necessary information.

## 8. Run comparisons and preserve evidence

When independent runs are available, compare the skill against a meaningful baseline:

- **New skill:** Run each test with the skill and without it.
- **Existing skill:** Save an unchanged copy before editing, then compare the revised version against that prior version or another explicitly chosen baseline.

Run conditions should be comparable. When possible, launch skill and baseline runs at the same time for all test cases. Preserve the prompt, supplied inputs, resulting outputs, and available run metadata such as duration and resource use. Record timing when it is reported because some environments do not retain it afterward.

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

If independent comparison is unavailable, perform a transparent sanity check: execute the skill on each test prompt, preserve outputs, and ask the user to review them. Do not describe this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs are in progress, draft objective checks where they add real value. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and tied to user value. Examples include:

- Required sections are present.
- A generated file opens and contains required fields.
- Calculations match a known source within an agreed tolerance.
- The response identifies missing mandatory information.
- Required citations or source references are included.

Record each check with descriptive text, a pass/fail result, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when essential source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests it before finalization."
    }
  ]
}
```

Use programmatic checks when practical. They are more repeatable than visual inspection and can be reused across iterations. Do not force quantitative checks onto subjective work: writing quality, aesthetics, tone, strategic judgment, and practical usefulness often need informed human review.

## 10. Review results with a human

Present qualitative outputs and quantitative evidence together. Use an available review interface when possible; otherwise present outputs clearly in the conversation or as accessible files.

For each test case, show:

- The original prompt and relevant supplied inputs.
- The skill output and comparison output, if available.
- Objective grades and supporting evidence.
- Timing or resource data, if available.
- A clear way for the user to provide feedback.

Ask useful review questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, too slow, or hard to use?
- Did the skill add work that did not improve the outcome?
- Would this work for similar requests with different wording or data?

Empty feedback can mean a test case is acceptable, but it is not proof that every important case is solved. Consider outputs and measurements as well.

## 11. Analyze beyond pass rates

When possible, aggregate pass rate, time, resource use, and variability. Present the revised skill before its comparison condition for easy reading. Then look for patterns that summary numbers can hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill's value.
- **High variance:** Similar runs differ significantly, suggesting unclear instructions or environmental instability.
- **Tradeoffs:** Quality may improve while time or resource use becomes disproportionate.
- **Failure concentration:** Several failures may trace to one cause, such as unclear source selection or missing output rules.
- **Unproductive work:** Execution traces may reveal redundant planning, research, or formatting.
- **Repeated reconstruction:** Multiple runs independently recreate the same helper process, suggesting a script, template, or reference would help.

A small benchmark is evidence for the next revision, not conclusive proof of quality.

## 12. Improve without overfitting

Base revisions on user feedback, outputs, traces, and evaluation results. Change the smallest part of the skill likely to address the underlying cause.

Generalize from a complaint. If one output fails to identify an uncertain source, do not merely mention that exact test. Clarify the broader behavior: distinguish verified information from assumptions whenever source evidence is incomplete or mixed.

Use these principles:

1. **Fix causes, not examples.** Design for future requests, not only the current test set.
2. **Keep instructions lean.** Remove guidance that does not affect useful behavior or causes wasted effort.
3. **Explain intent.** Tie instructions to quality, safety, usability, or authorization.
4. **Add reusable assets only when justified.** Bundle helpers when repeated work demonstrates value.
5. **Preserve successful behavior.** Do not discard what users value while correcting a separate weakness.
6. **Expand coverage gradually.** Add a test for a genuine class of failure, not every isolated incident.

After revision, run the full relevant test set in a new iteration. Retest against the same baseline policy, show prior outputs where useful, collect feedback, and repeat.

Stop when the user says the skill is ready, feedback is consistently positive on meaningful cases, objective requirements are reliably met, or further changes no longer create meaningful improvement. If remaining problems require missing information, unavailable capabilities, or a product decision, state that clearly instead of continuing to edit instructions.

## 13. Optional blind comparison

For a more rigorous comparison of two versions, provide an independent evaluator with two outputs without identifying which version produced each one. Give the evaluator a shared rubric and reveal the mapping only after it records its judgment.

Blind comparison is useful when versions have similar formal scores but differ in qualitative quality, when a decision is important, or when recency bias may affect review. Base the rubric on user value: correctness, completeness, clarity, adherence to constraints, safety, and practical usability. Analyze why the preferred output won before revising again.

## 14. Optimize activation behavior

Optimize the description only after the skill itself is stable. Create a realistic set of requests that should activate the skill and difficult near-misses that should not.

Positive cases should vary across:

- Formal and casual phrasing.
- Direct requests and requests that imply the job.
- Common and less common valid situations.
- Situations where another related skill might compete.

Negative cases should be genuinely close. They should share terms or context with the skill but require another job, a different capability, or lack conditions that make this skill appropriate.

Example format:

```json
[
  {
    "query": "I need a concise leadership update from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain why teams use progress reports without preparing one for my project?",
    "should_trigger": false
  }
]
```

Review the query set with the user before evaluating descriptions. If the environment supports repeated activation testing, separate examples used to improve the description from held-out examples used to choose it. Select the description that performs best on held-out cases, not merely the one that fits the drafting examples.

Use substantive requests: an AI may solve a simple one-step request directly without consulting a specialized skill, even when the description matches. Ensure the final description remains honest about scope.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Audit the package before delivery:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on private conventions, personal access, or undeclared capabilities.
- Scripts, references, and assets are present, clearly named, and documented.
- No confidential data, credentials, identifiers, or unnecessary personal information remain.
- The user can install, access, or adapt the skill in their chosen environment.
- Test material is retained only when safe and useful.

Provide a short handoff note covering what the skill does, required capabilities, known limitations, authorization boundaries, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an honest activation description, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for real recurring work.


---
name: test-every-screen-size
description: Verify UI and CSS changes across representative widths, heights, realistic content states, screenshots, and layout checks before release.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to a small spacing, color, or background adjustment: a local edit can change wrapping, overflow, height, alignment, or visible backgrounds elsewhere.

A single viewport, a bounding-box measurement, or one desktop and one mobile screenshot is not enough. Combine real screenshots with programmatic layout checks.

## 1. Define a representative test matrix

Choose viewports based on the product’s supported devices, analytics, design breakpoints, and known user environments. If no project-specific matrix exists, use this practical starting set of widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large width, such as 1920 px, when large displays are in scope. Include any reported or contractually supported viewport that differs from these defaults.

When vertical layout matters, test both a short and a tall height at relevant widths. Broad defaults are about 700 px for short and 1400 px or more for tall. Include an especially tall viewport—for example, 1800 px—when changing viewport-height rules, flexible page shells, backgrounds, vertical spacing, sticky footers, or bottom alignment.

Use a repeatable browser automation or testing capability selected by the project. Run it in a consistent non-interactive mode when possible.

## 2. Prepare realistic page states

Test the real interface in an authorized environment. Populate the affected area with representative content before capture:

- long paragraphs, formatted content, and long field values;
- realistic lists, cards, rows, and validation messages;
- typical and near-limit item counts;
- loading, empty, and error states when the change can affect them.

Do not validate only an empty or unusually sparse state. Sparse content often hides clipping, overlap, wrapping, and unintended blank space.

## 3. Capture and inspect screenshots

Capture screenshots at each relevant viewport and state. Use full-page captures when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect every changed component on all four sides:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design after the component changed role, size, or containment.

Give extra attention to full-bleed or edge-to-edge changes. Removing containment on one side can expose remaining margins or wrapper padding on another side as visible background strips. Check every edge, not only the edge edited.

Reread the requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is meant to fit the viewport;
- no changed element overlaps neighboring content or its intended container;
- buttons, links, and fields remain visible and operable;
- fixed or sticky UI does not obscure essential content;
- cards, lists, and controls remain within intended bounds;
- prose retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height while allowing a small rendering tolerance. For overlap detection, compare relevant element rectangles with adjacent elements and container boundaries. Check interactive targets themselves, not only their parent containers.

For prose-heavy pages, flag excessively wide text measures. A useful warning threshold is roughly 80 characters per line; reading-focused layouts commonly target about 60–70 characters per line.

## 5. Require both forms of evidence

Measurements can miss visible defects such as exposed background strips, poor visual balance, and unexpected empty regions. Screenshots can miss off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and relevant programmatic checks pass.

## 6. Fix failures and rerun

If any viewport or realistic state fails:

1. stop completion, review, publication, or release;
2. identify the layout rule causing the failure;
3. fix the underlying layout behavior rather than adding a narrow viewport-specific patch;
4. rerun the complete relevant sweep, not only the viewport that failed.

If a change corrects one viewport but creates a defect at another, reconsider the diagnosis. The layout model or design constraint is likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights and states, and checks performed.

Use a concise report such as:

> Verified across the project viewport matrix, including narrow, medium, and wide widths; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, say so clearly. Do not represent the UI change as complete until required checks pass or the remaining limitation is explicitly accepted by the appropriate project owner.


---
name: run-a-recurring-community-event
description: Create and publish the next occurrence of a recurring community event, prepare fresh materials, invite the approved audience, and verify the live result across the chosen tools.
---

# Run a recurring community event

Use this workflow for a repeated social, sports, learning, volunteer, or community event. Adapt it to the organizer's chosen calendar, event platform, image-creation tool, storage location, and communication channels.

## Set authority and boundaries

Before taking external actions, establish which mode applies:

- **Prepare only:** create materials and an unpublished draft.
- **Review before publish:** prepare the event, then request approval before publishing or inviting.
- **Standing authorization:** publish and send invitations under a documented audience policy.

Standing authorization should state the recurrence, normal audience, platform, and any limits. Ask for a decision if the occurrence introduces a material change, such as a new audience, paid admission, changed venue, unusual safety concern, or altered privacy setting.

## 1. Determine the next occurrence

Calculate the date from the recurrence rule and local time zone; do not rely on mental arithmetic. Confirm the date, weekday, start time, end time, venue, and host arrangement.

If events are numbered, inspect prior occurrences and use the next number after the highest existing one. Include early unnumbered events when reviewing the series history.

Check for relevant conflicts such as holidays, venue closures, organizer availability, or weather-sensitive conditions. A conflict does not automatically cancel the event. Follow the organizer's policy; if the event proceeds, report the conflict and any remaining handoff or cancellation decision.

## 2. Reuse stable information and update changing details

Review the latest event or two before creating the new one. Separate details into:

- **Stable details:** purpose, usual format, meeting point, regular instructions, contact route, and accessibility guidance.
- **Occurrence-specific details:** date, sequence number, hosts, route, weather plan, capacity, theme, and exceptions.

Use the approved title pattern and description template. Update every changing detail deliberately. Do not carry forward stale dates, expired links, temporary announcements, or venue instructions that no longer apply.

## 3. Prepare event artwork when needed

If the series uses recurring visuals, keep a recognizable identity while making each new image distinct. Review recent artwork first so the next concept is not a minor variation of the last one.

Create an image brief containing:

- event name or required text;
- the core activity or recognizable symbols;
- desired style and mood;
- one new central visual idea; and
- quality constraints for the selected image capability.

Vary the main idea through season, light, weather, viewpoint, local texture, an activity detail, or one small humorous focal object. Prefer one clear subject over a crowded scene. Request clean composition, restrained color, readable text, and no obvious generation artifacts.

Review the result before use. If it repeats recent work or contains visible defects, revise the concept and regenerate a limited number of times. Do not retry indefinitely. Before treating a tool error as a failed generation, check whether the requested image was actually produced.

Export the selected file to a location that the event platform can access, then confirm that the uploaded file is the intended image and displays well after cropping.

## 4. Create the event

Use the authorized organizer account and verify the account before editing. Prefer a real draft or preview when the platform supports one, but recognize that some platforms create a live event when the control says "Save" or similar.

Complete fields in this order when practical:

1. **Title:** apply the approved naming pattern, such as `Event Name #N`.
2. **Date and time:** set the local date and complete time range.
3. **Location:** choose the exact venue or map result, not a similarly named listing.
4. **Description:** apply the current template and occurrence-specific updates.
5. **Image:** upload and inspect the image.
6. **Hosts:** add only people authorized to host or co-host.
7. **Settings:** confirm visibility, capacity, cost, RSVP rules, accessibility information, and notifications.

Date pickers and dynamic forms deserve extra care. Finish and verify the date/time selection before editing other fields. After opening a menu, resizing a window, scrolling substantially, or causing the page layout to change, re-check the visible state before clicking. Prefer controls identified by their labels or roles rather than fixed screen positions.

## 5. Verify before and after publishing

Review the draft or preview as an attendee would. Confirm:

- title and occurrence number;
- weekday, date, start time, end time, and time zone;
- exact venue and map pin;
- description, links, and contact information;
- image presence, crop, and legibility;
- host/co-host status; and
- visibility, capacity, cost, and RSVP settings.

If a required item cannot be verified, do not claim the event is ready. Correct it, use a safe fallback, or request a decision under the selected authority mode.

Publish only when authorized. Then open the live page and repeat the attendee-facing checks. Save the live URL.

## 6. Invite the approved audience

Follow the documented invitation policy. A common policy is to invite prior attendees of the same series, but this is not a default. Respect opt-outs, privacy expectations, consent boundaries, and platform restrictions. Do not expand the audience without authorization.

When inviting from prior events, list all relevant occurrences and process them systematically. Filter or review one occurrence at a time, add its attendees, clear the filter, and continue. Check whether people are already selected before using a bulk-select control, since platforms may preselect recent attendees.

After each batch, verify that the invitee count increased by a plausible amount. If it drops or stays unchanged unexpectedly, stop and inspect the current selection before proceeding. Use platform deduplication where available; otherwise compare lists before sending.

Send invitations only when authorized. Confirm the platform's sent state, delivery status, or final invited count. If the platform cannot provide confirmation, state that limitation clearly.

## 7. Report completion

Provide a brief operational report with:

- what was created and whether it was published;
- date, time, and venue;
- invitation outcome or current invitee count;
- conflicts, unresolved items, or nonstandard settings; and
- the live event URL.

When the URL must be easy to copy, put it on the final line with no text after it.

## 8. Maintain the workflow

After each occurrence, record only reusable lessons: changed platform behavior, durable audience rules, template changes, field-order constraints, and content preferences. Keep temporary facts for one event separate from the recurring process.

## Readiness check

Before declaring success, confirm:

- The date and sequence number were calculated and checked.
- The correct organizer account and public event page were verified.
- Stable details are current and occurrence-specific details were updated.
- The artwork is fresh, usable, and correctly uploaded, if artwork is required.
- The end time, time zone, venue, and settings were confirmed.
- Invitations followed the approved policy and respected opt-outs.
- Publishing and invitation results were verified or any verification limit was reported.

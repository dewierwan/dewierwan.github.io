# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and present a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas; it is a set of meaningfully different paths, clear tradeoffs, and two or three credible choices.

## 1. Gather relevant context

Start with information the user has provided. Review linked documents, discussion records, prior decisions, research, or other sources only if you have legitimate access and they are relevant to the decision.

When the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Current constraints, commitments, budgets, or deadlines
- Stakeholder concerns, decision ownership, and access boundaries
- Evidence from previous attempts or experiments

Use targeted retrieval rather than broad searching. If records include personal or sensitive information, use only the minimum relevant information, omit unrelated details, and respect consent, confidentiality, and the user’s authorized access level. If key context is unavailable, state the assumption or ask a focused question; do not invent facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- The decision the user is actually making
- Important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging options

The stated request may describe a symptom or a preferred solution rather than the underlying choice. For example, “Should we add a feature?” may really mean, “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip the pause only when the framing is obvious and low-stakes, or when the user explicitly requests an immediate first pass. A wrong frame produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision genuinely has fewer meaningful paths. Options must represent fundamentally different approaches, not different intensity levels of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes process, incentives, scope, ownership, or the framing of the problem
- At least one surprising but plausible option, such as delaying, partnering, narrowing scope, or deliberately doing nothing

Do not be contrarian just to seem creative. A “do nothing” option is useful only when observation, timing, avoided distraction, or preservation of resources is a real strategic choice.

Give each option a short, memorable label that makes its approach clear. For every option, provide:

- **What:** One or two sentences describing the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limits.
- **Effort:** Low, Medium, or High.

Use specific and comparable tradeoffs. Do not soften serious drawbacks or make a preferred option look better by evaluating alternatives unfairly.

### Option template

| Option | What | Strengths | Weaknesses | Effort |
|---|---|---|---|---|
| [Short, clear label] | [One or two sentence approach.] | [Concrete benefits.] | [Concrete risks or costs.] | [Low / Medium / High] |

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic alignment, operational burden, and stakeholder impact. Add domain-specific criteria when they matter more than generic defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are informative, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not merely why it is attractive in general.
4. State the key assumption most likely to change the ranking, if there is one.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

### Recommendation format

| Rank | Option | Why it fits | Key condition or assumption |
|---|---|---|---|
| 1 | [Option label] | [Situation-specific reason.] | [What could change the ranking.] |

## 5. Stop for a decision

After presenting the options and recommendations, wait for the user. They may:

- Choose an option
- Request more detail on one option
- Correct the framing or constraints
- Ask for additional options
- Combine options into a hybrid

If the user proposes a hybrid, test whether its components are compatible and whether the combination resolves a real tradeoff rather than adding complexity and cost.

Do not start implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user chooses a path, select the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing decisions, or choices with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record that states the choice, decision owner, rationale, assumptions, and a review point.
- **Build-oriented choice:** After the decision is recorded, move to planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision, not just the first solution mentioned.
- Options are genuinely distinct and not degree variations.
- At least one conventional option and one non-obvious but plausible option are considered where relevant.
- Strengths and weaknesses are candid, concrete, and comparably described.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than the assistant’s default preferences.
- Any retrieved context was authorized, relevant, and handled within appropriate privacy and access boundaries.
- The response ends with a clear invitation for the user to choose, refine, reject, or combine options.


---
name: pressure-test
description: Find the weak points in a leading strategic idea before committing to it. Steelman the case, test its load-bearing assumptions through sequential challenge, and finish with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or build the implementation.

## Position in the decision process

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision at a level of rigor that matches its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing a single idea too early can become an exercise in defending it.

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.

## Evidence, access, and privacy

Use only evidence that the user is authorized to access and use for this decision. If reviewing internal records, customer feedback, interviews, or private communications, confirm there is a legitimate purpose and use the minimum relevant material. Do not expose unrelated personal details, confidential content, or information outside the intended access boundary.

Distinguish clearly between documented facts, informed inferences, forecasts, and unknowns.

## Rules of engagement

- Be direct. Do not treat confidence as evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Use available evidence such as research, metrics, prior experiments, customer feedback, documented decisions, or stakeholder input.
- Refer to relevant dissenters by role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's actual intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

**Template**

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, starting with the assumption most likely to undermine the decision.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | How to test or disprove it |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence and its quality] | [Low, medium, or high] | [Name the smallest useful test] |

Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Choose questions based on the highest-risk assumptions and adapt later questions to the answers received. Do not present the full set as a questionnaire, because that permits selective answering.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed? Why is this case materially different?
- **Opportunity cost:** What is the best valuable work that will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence. Ask what observed behavior, data, comparison, or commitment supports that belief.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failures, external changes, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable signal] | [Name the check or accountable role] |

The warning sign must be observable early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap; do not assume silence means agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence that names the evidence that would reverse or materially alter the position.

**Template**

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, include a scheduled review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data collection period. Next: run that test, then make the decision with its result recorded.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, the downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with exactly one concrete next action: a verb, an owner, and a deadline when useful.

**Example:** `Research owner: interview five target users this week and compare results against the adoption assumption.`

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

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and giving a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make a clear decision with only as much process as the decision deserves. The objective is timely commitment, an honest record for consequential choices, and better judgment through review.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** Keep the assistant's recommendation clearly labeled as assistant analysis. Include it in a decision record only if the user asks.
4. **Record only with permission.** “Should we do X?” asks for analysis, not for a record. Create or update a record only when the user asks to log, track, open, or commit it, or explicitly agrees to that practice.
5. **Respect privacy and access boundaries.** Before consulting shared communications, personnel information, customer records, or a shared register, confirm a legitimate purpose and clear authorization. Use the minimum relevant material and omit unrelated sensitive details.
6. **Do not confuse a task with a decision.** If there is no meaningful alternative, it is execution. Say so and move to planning or doing the task.

For health, relationships, compensation, confidential personnel matters, or similarly sensitive subjects, confirm that the proposed record and audience are appropriate. Offer a private document or keep the matter in conversation if needed.

## 1. Select the mode

Identify whether this is a new decision, a continuation, a commitment, or a review.

| Mode | Use when | Action |
|---|---|---|
| New | No matching record exists, or the user requests a fresh decision | Frame and classify it |
| Resume | An open decision exists | Add new inputs without rewriting history |
| Commit | An open decision exists and the user is ready to decide | Complete readiness checks and record the call |
| Review | A resolved decision has reached its review point | Compare actuals with the original prediction |

If the user explicitly names a mode, follow that instruction. Otherwise, when authorized to access the chosen decision register, look for an overlapping decision before creating another record. Trust explicit instructions over automated matching.

## 2. Frame the question

Write the decision in a form that can be answered. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What deadline, event, or trigger requires a decision?
- What outcome is desired?
- What happens if no action is taken?

If the question is open-ended and credible options do not exist yet, generate options before evaluating them. Ask one clarifying question at a time when the missing answer changes the analysis.

## 3. Classify scope

Use the cost of unwinding the choice, not just its apparent size. Consider money, time, trust, operational disruption, opportunity cost, and reputation.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not record by default |
| Reversible | Moderate stakes; reversible in days or weeks | Brief comparison and optional light record |
| Hard to reverse | Meaningful cost or disruption to undo | Full analysis and challenge gate |
| Direction-setting | Shapes strategy, culture, finances, or operating model for a long period | Full analysis plus dissent and prerequisite consultation |

If the user calls a choice trivial, ask: “What would it cost to unwind?” If they cannot name the cost quickly or the answer is uncertain, treat it as a larger decision.

## 4. Apply the appropriate rigor

### Trivial

Choose a reasonable default, give a one-sentence rationale, and move on. If the user is delaying without a decision-changing reason, say directly that further deliberation is consuming more attention than the choice merits.

### Reversible

1. List two or three realistic options.
2. For each, state one major strength, one major weakness, and a rough effort, time, or cost estimate.
3. Give a recommendation and the decisive reason.
4. When uncertainty matters, prefer the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid challenge examines its assumptions, contrary evidence, likely failure modes, strongest alternative, and relevant stakeholder objections.

If this has not happened in the current work context, stop the commitment flow and state:

> This decision is hard to reverse. Challenge the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not waive the gate because of urgency alone. Proceed only after the challenge is complete or the user explicitly overrides it with a reason. If the challenge reveals a serious unresolved failure, return to option generation, redesign the option, obtain a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Identify stakeholders with expertise, consequences, or constraints relevant to the decision.
4. Provide a recommendation labeled **Assistant analysis** unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process, plus two further gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and represent their strongest case fairly.

The decision is not ready until the required conversation has occurred, unless the user explicitly accepts and records why proceeding is necessary. If the choice is rushed, name exactly what consultation, evidence, or dissent is being skipped and why it matters.

## 5. Keep facts, views, and uncertainty separate

For each serious option, capture what it enables, what it costs or prevents, the best evidence for it, the strongest objection, key assumptions, and the cost of reversal. Distinguish non-negotiable requirements from preferences.

Maintain these categories:

- **User’s stated view:** only the user's actual words or clearly confirmed position.
- **Assistant analysis:** the assistant's recommendation and reasoning.
- **Open question:** uncertainty not yet resolved.

If the user has not stated a position, write “No position stated yet” or leave their position blank. Never manufacture a lean, confidence percentage, rationale, dissent response, or final choice.

## 6. Commit and record

Before finalizing, confirm the choice, rationale, reversal conditions, next action owner and date, observable prediction, and the user's confidence in that prediction.

Use the user's chosen document, decision register, or private file. A useful record includes status, decision type, stakes, reversibility, decision date, review date, confidence, and outcome. Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar or reminder system for higher-stakes reviews.

For an open decision, record context, options, and new inputs only. Leave choice, confidence, prediction, and personal reasoning blank until the user supplies them. When resuming, append a dated entry rather than replacing earlier thinking.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** [Optional additional option]

## Thinking log
### [Date]
- New inputs, conversations, data, or events
- How the thinking changed
- User’s stated position today: open / leaning / decided

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
The user’s own reasoning, only when stated by the user.

## What would change my mind
Assumptions or evidence that would justify reversing the choice.

## Prediction
By [date or trigger], [observable outcome] will happen or not happen.
Confidence: [X%]

## Worries
The most credible downside or failure mode.

## Retrospective
To be completed at review.
```

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals rather than impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat a bad outcome as proof of a poor process, or a good outcome as proof of sound reasoning.

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

Use direct language. Challenge weak reasoning with evidence, but do not turn rigor into endless deliberation. Once the appropriate gates are met, name the decision and move forward.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem whose solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to "build X," work backward:

- Who experiences the problem?
- What are they trying to accomplish?
- What happens today?
- What workarounds exist?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the problem meaningfully better?

Write a concise problem statement and descriptive requirements. Describe the desired outcome and constraints, not an assumed implementation. If the proposed solution appears mismatched to the problem, say so directly.

Ask only for information that cannot be found in the available context, documentation, code, or records.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, and available alternatives. Include “do nothing” or “deprioritize” as a real option when the issue is rare, low-cost, or adequately handled by a workaround.

Distinguish reversible decisions from expensive commitments:

- **Reversible decisions:** small, easy-to-change choices. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** public interfaces, persistent data changes, long-lived configuration, migrations, external contracts, security boundaries, or vendor commitments. Pause and obtain an explicit decision before implementing. Record the decision and its rationale when appropriate.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before doing substantial design or implementation work.

## 3. Research the current context

Read the relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before inventing new ones.

Understand constraints such as compatibility requirements, deployment practices, security expectations, supported environments, ownership boundaries, and monitoring. Use the system's existing conventions unless there is a strong reason to change them.

## 4. Define evaluation criteria

Define lightweight, explicit criteria before generating solutions. For example:

- Must preserve existing authentication and data behavior.
- Must be feasible within the available time and maintenance capacity.
- Should avoid new dependencies or persistent configuration.
- Must have a clear verification method.
- Must be removable or reversible if it fails.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of the same design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, or a capability already available in an existing platform.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For especially ambiguous problems, generate a wider set of candidates before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that behave differently depending on runtime conditions.
- Use strict validation and fail fast for invalid states. Do not silently convert programmer errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Do the work cleanly; avoid quick fixes placed outside the appropriate design boundary.

## 6. Evaluate and recommend

Compare each viable option against the criteria from Step 4. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- The viable options and tradeoffs.
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
- The verification performed and its results.
- Known limitations, risks, and deferred work.
- Any required user action, rollout step, or monitoring.
- Links or references to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.


---
name: shape-and-draft
description: Shape consequential documents by reviewing evidence, resolving material choices, and checking readiness. Then draft and audit the smallest document that can achieve the goal.
---

# Shape and draft a document

Develop a consequential document by shaping the underlying thinking before writing it. Determine what the document must achieve, gather relevant evidence, resolve material choices with the appropriate decision-maker, and then draft the smallest document that can do the job.

Use this workflow for strategies, narratives, operating agreements, briefs, proposals, scorecards, and decision memos when the artifact, argument, boundaries, commitments, or operating model are not yet settled. Do not use it for a quick edit, a formatting request, or a document whose content and decisions are already specified.

## Classify the request

The request may name a document type, outcome, audience, source material, or some combination. Treat a proposed document type as a starting hypothesis, not a fixed instruction, until its purpose is clear.

Use a **full shaping process** when the document is consequential and material choices remain unsettled, or when the requester asks for deep thinking, several rounds of questions, or close alignment before drafting.

A substantive interview round resolves a distinct layer of choices and uses the answers to determine the next questions. Restating prior discussion or asking for broad approval is not a substantive round.

## 1. Work backwards from the desired outcome

Start with the change the document must produce. Establish:

- Who will read it.
- What those readers should understand, decide, approve, or do.
- What is unclear, contested, blocked, or going wrong now.
- Whether the document primarily needs to explain, persuade, decide, coordinate, or govern.

Do not treat “write a strategy” or “make a narrative” as a sufficient goal. Identify the actual job the document must perform.

## 2. Select the right artifact

Recommend the document form that best serves that job:

- **Narrative:** Creates shared understanding of why something matters and what bet is being made.
- **Strategy:** Connects a diagnosis to choices, priorities, intended outcomes, and exclusions.
- **Operating agreement:** Defines ownership, decision rights, interfaces, handoffs, and working cadence.
- **Decision memo:** Records a choice, alternatives, rationale, risks, and a review point.
- **Scorecard:** Defines a role or team mission, outcomes, and required capabilities.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the relevant tradeoff and recommend an artifact. If the form would materially affect the argument, structure, or decisions required, ask the authorized decision-maker to confirm it before proceeding.

## 3. Gather and classify evidence

Read supplied material first. Follow any stated rules for source selection, authority, citations, and linking. Scale the research effort to the stakes and use the sources and systems available for the work.

For a consequential internal document, look for material likely to contain prior decisions, current definitions, supporting evidence, dissent, constraints, ownership context, and relevant performance information.

Apply these evidence rules:

- Respect a stated hierarchy of sources.
- Prefer current, authoritative decision records over discussion notes, recollections, generated summaries, or repeated claims.
- Resolve contradictions where evidence permits; surface material contradictions that remain.
- Do not ask participants for factual information that available sources can answer.
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
- The important questions that only a decision-maker can resolve.

## 4. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds already completed in the current conversation, and do not repeat answered questions.

Do not draft immediately after the first round merely because one apparent central issue has been resolved. Use a later round to test consequences: boundaries, tradeoffs, counterarguments, ownership, definitions, or execution implications.

Ask four to eight focused questions per round. If fewer than four material questions remain, ask only those questions and state that it is a narrow final check. Do not add ceremonial questions simply to reach a number.

Each numbered question should normally seek one decision. Do not combine separate decisions, such as ownership, coordination, handoffs, and success measures, into one broad yes-or-no question. Bundled questions create false alignment.

Use a compact question format that supports quick answers:

1. Number each question: `1.`, `2.`, `3.`.
2. For bounded choices, label options with lowercase letters: `a.`, `b.`, `c.`.
3. Put the recommended option first unless prior context clearly makes another ordering more useful.
4. Put questions and options on consecutive lines, with no blank lines within the question block.
5. Allow the respondent to reject the framing or provide an alternative answer.

Example:

1. Which direction should the document recommend?
   a. Focus on the highest-impact problem first; this narrows scope but clarifies accountability.
   b. Cover all related problems equally.
   c. Present options without a recommendation.
2. Who should make the final decision?
   a. The accountable lead.
   b. A cross-functional decision group.

Each round should:

1. Begin with an updated model of the situation and state what changed because of earlier answers.
2. Focus on one layer of uncertainty rather than mixing every issue at once.
3. Offer two or three concrete options when the decision can be bounded.
4. Explain the tradeoff behind the recommended option.
5. Separate source-supported observations from choices participants must make.
6. Surface contradictions and ask the smallest question needed to resolve them.
7. Include a pressure test when the document is persuasive or strategically consequential.

A common progression is purpose; strategy; operating model; definitions and measures; then expression, format, and destination. Adapt the sequence to the work, but preserve the answer-dependent loop: later questions must arise from earlier answers, not from a generic questionnaire.

After every answer round:

1. Classify each answer as confirming, rejecting, softening, qualifying, or deferring the proposed position.
2. Trace downstream implications. A changed audience, softened commitment, new exception, or rejected framing often creates another material question.
3. Update the alignment ledger and show a concise synthesis.
4. Generate the next round from the remaining material uncertainties and their consequences.

Continue while an unresolved issue could materially change the document. If the requester explicitly asks to draft before the process is complete, name the one or two most important consequences of the remaining uncertainty, then follow the instruction.

## 5. Maintain an alignment ledger

Keep a compact working record throughout the conversation:

- **Confirmed:** Choices explicitly made by the authorized decision-maker.
- **Source facts:** Claims established by current, authoritative evidence but not selected as present choices.
- **Inferred:** Plausible interpretations that remain unconfirmed.
- **Open:** Questions that could materially change the document.
- **Corrected:** Assumptions or claims that a participant has rejected.

Update this ledger after every answer round. Never reintroduce a corrected assumption. If confirmed statements conflict, surface and resolve the conflict rather than hiding it in vague language. Never promote an inference to confirmed solely because several sources support it.

For a full shaping process, show a concise version of the ledger before each later round. Every major draft claim must be a confirmed choice, a supported source fact, or explicitly framed as a proposal, assumption, or open question.

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
- Has the response to that objection been confirmed?

Close alignment means remaining uncertainty is low impact or clearly represented as unresolved. It does not require artificial certainty.

## 7. Draft and deliver

Follow the stated voice, style preferences, format, accessibility needs, and delivery requirements. Where no style is specified, use clear, direct language appropriate to the audience.

Write the smallest document that accomplishes the agreed purpose. Prefer clear claims, concrete decisions, named ownership, and explicit boundaries over polished but vague abstractions. Distinguish current decisions from proposals, assumptions, and future review points.

Make the draft as simple as the substance allows:

- Prefer short, common words over formal or inflated language.
- Write complete, natural sentences. Keep one clear line of thought in each sentence, but do not split connected ideas into choppy fragments.
- State the point first. Remove warm-up text, repeated context, process narration, and unnecessary qualifications.
- Turn abstractions into concrete claims, actions, examples, owners, dates, or tests where useful.
- Use focused paragraphs. Use bullets only for real lists; write bullet items as full sentences unless they are compact labels.
- Prefer the more concise version when it preserves meaning. Concision removes unnecessary ideas and words; it does not require every sentence to be short.
- Preserve hard ideas when they matter, but explain them in plain language rather than jargon.

Honor the requested destination using the chosen system. If text is requested in the conversation, provide text without changing source material. If a document must be created or updated elsewhere, do so only as instructed and verify that the intended content is present.

## 8. Audit before delivery

Compare the draft against the alignment ledger and source hierarchy:

- Does it solve the agreed problem in the agreed form?
- Does every material choice reflect confirmed decisions?
- Have corrected assumptions been removed?
- Are responsibilities, boundaries, decision rights, and handoffs unambiguous where relevant?
- Are uncertain claims labeled appropriately?
- Are factual claims and citations supported by appropriate sources?
- Is any inference presented as a settled fact or decision?
- Does the document match the requested voice and audience?
- Can each sentence be understood on the first read?
- Can any abstract phrase, inflated word, or repeated point be made simpler or removed without losing meaning?

Fix mismatches before delivering. Put the deliverable last, without trailing commentary that would interfere with copying or using it.

## Failure modes to avoid

- Drafting early because producing text feels productive.
- Treating the proposed artifact as fixed before its purpose is known.
- Asking participants for facts that available evidence can answer.
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
description: Learn a paper, article, post, or topic through a short Socratic dialogue that builds recall, explanation, and application instead of passive reading.
---

# Learn with a tutor

Help a learner understand, retain, and use material they provide, such as a paper, article, post, lesson, or topic. Use a Socratic dialogue: the learner does most of the recalling and reasoning, while the tutor diagnoses understanding, asks productive questions, and supplies concise clarification only when needed.

## Purpose and learning principles

The aim is durable understanding, not quick recognition. Favor these principles:

- **Retrieval before review:** Ask the learner to reconstruct ideas from memory before giving an explanation or summary.
- **Elaboration:** Ask why, how, under what conditions, and with what evidence an idea holds.
- **Learner-generated connections:** Have the learner create examples, analogies, predictions, and applications before offering your own.
- **Productive difficulty:** Make questions demanding enough to require thought, while keeping them answerable with an informed attempt.
- **Transfer:** Test whether the learner can use an idea in a different setting, compare it with related ideas, or revise a real decision.
- **Constructive error discovery:** Surface contradictions and missing assumptions through questions. Give direct correction after a fair opportunity to reason.

Do not assume that recognizing terminology, repeating a conclusion, or agreeing with a statement demonstrates understanding.

## Conversation workflow

### 1. Establish prior knowledge, source status, and goal

Start with one or two open questions. Find out what the learner already believes, what they have read or watched, and what they want to do with the knowledge.

Examples:

- “What do you already think you know about this topic, and what led you to that view?”
- “What are you trying to be able to explain, evaluate, or do by the end?”
- “Have you engaged with the material already? If so, what seems most important or confusing?”

If the learner has not yet engaged with the source, do not immediately summarize it. Ask for an initial prediction or working model, then direct them to inspect a relevant section before beginning recall.

### 2. Elicit the central claim from memory

Ask the learner to explain the main argument, finding, or concept in their own words. Do not let them substitute a quotation for understanding.

Useful prompts:

- “What is the main claim, in your own words?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “How would you explain this to a thoughtful friend in 30 seconds?”

Listen for the claim, its mechanism, its evidence, and its assumptions. Use the response to identify what to explore next.

### 3. Select two or three high-value ideas

Do not attempt to cover every point. Choose a small set of ideas that are central, difficult, consequential, or likely to be misunderstood. Explore each through this cycle:

1. Ask the learner to reconstruct the idea.
2. Probe the mechanism, assumptions, evidence, or causal reasoning.
3. Ask for a concrete example, analogy, or application.
4. Test a boundary case, objection, alternative explanation, or changed assumption.
5. Adjust the next prompt based on the learner’s answer.

Keep each turn short. Usually ask one question, or at most two closely linked questions, at a time.

## Question toolkit

Choose prompts that require explanation rather than recognition. Adapt their wording to the learner and material.

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What is the mechanism, step by step?”
- “What evidence would distinguish this explanation from another one?”
- “Can you give a concrete example from a familiar setting?”
- “Where might this fail or not apply?”
- “What is the strongest objection to this argument?”
- “How does this connect with another idea you know?”
- “What surprised you, and what did you expect instead?”
- “If one assumption changed, how would the conclusion change?”

Avoid standalone yes/no questions. If a binary choice is useful, require the learner to defend the choice and explain the alternative.

## Responding to learner answers

Maintain a warm, rigorous tone. Do not use generic praise. When an answer is strong, identify what specifically worked, such as identifying an assumption, separating correlation from causation, or giving a relevant counterexample. Then raise the challenge.

When an answer is incomplete or mistaken:

1. Do not immediately state the correction.
2. Ask a focused question that reveals the tension or missing distinction.
3. Allow one or two real attempts.
4. If the learner remains stuck, explain the missing step briefly and plainly.
5. Ask them to restate the idea in their own words or apply it to a new case.

When the learner says “I do not know,” invite a low-stakes attempt: “Take a guess based on what you do know. What seems most plausible, and why?” Offer a hint after an attempt, or sooner when the task requires background they do not yet have.

Ask the learner to define unfamiliar jargon before defining it yourself. Clarify the term only when their definition is missing, inaccurate, or insufficient for the current reasoning.

## Calibration and pacing

Increase challenge when answers are easy or fluent:

- request a counterexample;
- compare two explanations;
- change an assumption;
- ask for a prediction; or
- require application in a new domain.

Reduce challenge when the learner is genuinely lost:

- narrow the question to one claim or assumption;
- use a simpler case;
- provide a small hint;
- ask them to choose between plausible explanations and defend one; or
- briefly rebuild prerequisite knowledge before resuming.

Match the learner’s energy. Go deeper when they are engaged. When they are tired or overloaded, consolidate the most valuable ideas rather than introducing new ones. The exchange should feel like a thoughtful dialogue, not a fixed quiz.

## Progress checks and readiness gate

Periodically give a brief, evidence-based progress check. State what the learner has shown, what remains uncertain, and the next most useful focus.

| Check | Evidence to look for | Next move |
|---|---|---|
| Core understanding | The learner can state the central claim and explain why it follows. | Test assumptions or evidence. |
| Mechanism | The learner can describe how the idea works, not only its conclusion. | Ask for a boundary case or alternative mechanism. |
| Transfer | The learner can apply the idea accurately in a new situation. | Move toward a decision or action. |
| Remaining gap | The learner relies on terms, authority, or memorized wording without reasoning. | Return to a narrower retrieval question. |

Treat the learner as ready to close only when they can explain a core idea accurately in their own words and make at least one reasoned application, comparison, or prediction.

## Closing

Before ending, turn understanding into action. Ask:

> Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?

Then request either a concise final explanation, a new example, or a future retrieval prompt they can answer later. End by naming the most useful concept or question to revisit.

## Guardrails and common failure modes

- Do not provide an unsolicited summary. If the learner explicitly asks for one, first invite their own summary; then provide a concise version if still useful.
- Do not lecture when a well-designed question can prompt retrieval or inference.
- Do not make the task easy merely to be encouraging; challenge should be meaningful but achievable.
- Do not cover an entire source superficially when deeper work on a few key ideas will teach more.
- Do not turn the conversation into a sequence of disconnected test items. Build each question from the learner’s actual response.
- Do not delay correction indefinitely. If questioning no longer helps, clarify the point concisely, then return responsibility to the learner through restatement or application.
- Do not claim mastery based only on confidence, familiarity, or repeated wording. Look for explanation, reasoning, and transfer.


---
name: write-in-my-voice
description: Draft or revise email in the user’s authentic voice by using approved style evidence, verified facts, and a concise pre-send audit. The workflow keeps messages clear, appropriate to the relationship, and ready to copy and send.
---

# Write in my voice

Use this workflow when drafting, replying to, or polishing an email on the user’s behalf.

## Goal

Produce a copy-ready email that sounds recognizably like the user while remaining accurate, purposeful, and appropriate for the recipient and situation. Match the user’s normal writing habits without treating any style rule as more important than clarity, truthfulness, or professional judgment.

## 1. Load the voice profile

Before drafting, review the user’s current writing guide in full, if available. Use recent emails the user actually sent as additional evidence, especially messages to a similar audience or for a similar purpose.

Build a practical profile from the evidence:

- Typical greeting, closing, and signature.
- Usual formality, warmth, and directness.
- Sentence and paragraph length.
- Use of contractions, colloquial language, bullets, and punctuation.
- Preferred phrasing for requests, follow-ups, declines, corrections, and thanks.
- Words, tones, punctuation, or formatting the user avoids.
- Approved standard facts, links, boilerplate, or reusable responses.

Recent sent messages outweigh older examples. If the guide conflicts with recent consistent writing, ask which preference is current when it matters. Do not infer a personal style rule from one isolated example.

If accessing private drafts, sent mail, or records, do so only for a legitimate purpose with clear authorization. Use the minimum relevant examples, do not include unrelated personal information in the output, and keep the draft within the user’s appropriate access boundary.

## 2. Confirm the email brief

Identify the minimum information needed to write safely. Ask focused questions only when missing information would materially change the message.

1. Who is the recipient, and what is their relationship to the user?
2. What outcome should the email achieve?
3. What facts, dates, names, links, attachments, decisions, or commitments must be included?
4. What tone is needed: routine, warm, firm, formal, sensitive, or urgent?
5. Is there a deadline, approval requirement, or privacy concern?

Do not invent availability, pricing, decisions, promises, opinions, emotional reactions, or prior conversations. If an attachment or link is mentioned but unavailable, either ask for it or use a clear placeholder only if the user requests a draft template.

## 3. Adapt voice to the situation

Keep the user’s recognizable voice, but adjust it for the recipient and stakes.

| Situation | Adaptation |
|---|---|
| Close colleague or established contact | Use the user’s normal familiarity and concise rhythm. |
| New, external, senior, or formal recipient | Keep the user’s voice, but add enough context and careful wording to avoid ambiguity. |
| Request or follow-up | State the requested action, responsible person, and timing plainly. |
| Decline, correction, or conflict | Be direct, factual, and respectful. Avoid defensive explanations, exaggerated praise, or vague language. |
| Sensitive matter | Include only necessary details, avoid unnecessary personal information, and use neutral, clear wording. |

Use approved standard wording, factual details, and reusable links when they genuinely fit. Never use a canned response or factual claim merely because it is available.

## 4. Draft the smallest complete email

Use this default structure unless the user’s style evidence supports another pattern:

1. Greeting, when appropriate.
2. The purpose, answer, or decision in the first sentence.
3. Essential context and the next action.
4. Closing and sign-off, when appropriate.

Prefer active verbs, concrete nouns, short sentences, and short paragraphs. Put decisions, deadlines, requests, and questions where the recipient can find them quickly. Use bullets only when they improve actionability, such as for several requested items or scheduling options.

Remove language that does not help the recipient understand or act, including:

- Generic opening filler.
- Process narration about writing or reviewing the email.
- Repeated thanks or hollow compliments.
- Weak hedging around a clear decision or request.
- Unnecessary apologies or over-explanations.
- Details that exceed the recipient’s need to know.

## 5. Audit before presenting

Review the draft line by line:

- Does it plausibly sound like the user?
- Do the greeting, sign-off, punctuation, and rhythm match the evidence?
- Is the tone right for this recipient and context?
- Are all names, dates, links, attachments, and references verified?
- Did the draft add any unsupported claim, promise, commitment, opinion, or emotion?
- Is the intended action and timing unmistakable?
- Does it protect private or sensitive information appropriately?
- Can any sentence be removed without losing meaning or usefulness?
- Does it avoid the user’s known style anti-patterns?

## Readiness gate

Present a final draft only when these conditions are met:

- The purpose and recipient are clear.
- Material facts and commitments are supplied or verified.
- The tone is appropriate to the relationship and stakes.
- The email contains a clear next step when one is needed.
- The draft is consistent with the available voice evidence.

If these conditions are not met, ask the single most important clarifying question. If no voice evidence exists, use a broadly useful default: concise, warm-professional, direct, and free of unsupported assumptions. Invite the user to share a few sent examples or a style guide for future drafts.

## Output format

Provide the final email as copy-ready text. Do not add explanation after it unless the user asks for alternatives, rationale, or edits. If clarification is required, ask only the specific question needed to proceed.


---
name: professional-social-post
description: Draft, revise, and audit professional social posts from notes, drafts, articles, transcripts, or a topic. The workflow emphasizes concrete claims, strong hooks, useful substance, and targeted revision.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a draft, an article, a transcript, a podcast, a research finding, or a simple topic.

The goal is not to make an announcement sound enthusiastic. The goal is to make the right reader stop, understand a useful point, and have a reason to care. Write for a specific professional audience with low tolerance for fluff, generic inspiration, and vague claims.

This workflow is platform-independent. Before drafting, ask the user to choose or confirm:

- The platform and format: text post, caption, document carousel, thread, or article promotion.
- The audience: for example, technical practitioners, founders, policy professionals, researchers, customers, or job candidates.
- The purpose: share an insight, explain a concept, announce something, promote a longer piece, start a substantive discussion, or support a campaign.
- Any voice constraints: formal or conversational, first-person or organizational voice, preferred words, forbidden words, punctuation preferences, and length.
- Whether an external link will be included, and the platform’s preferred link placement.

If the user has an existing writing guide, approved posts, brand guidance, or audience research, use that as the source of voice rules. Do not assume a particular individual’s voice or a particular publishing system.

## Routing and scope

Some genres need a dedicated structure. Identify them before drafting.

- **Career or participant case study:** A named person’s before-and-after story, usually involving a program, employer, or career change. Use a case-study structure: starting point, turning point, concrete outcome, evidence, and lesson. Ask for permission before sharing personal details.
- **Research or evidence post:** A claim based on data, a model, a report, or an analysis. Prioritize methodology, uncertainty, and defensible interpretation.
- **Product or organizational announcement:** Lead with the concrete change and why it matters to readers. Do not lead with internal excitement.
- **Article, podcast, or report promotion:** Lead with the strongest finding from the piece, not with “new article” or “new episode.”
- **Carousel or document caption:** Give one or two meaningful findings, then point readers to the visual material. Do not duplicate every slide.

If a request could be a sensitive case study or contains personal information, ask what may be named, quoted, or disclosed. If the genre is unclear, ask one concise routing question before writing.

## Non-negotiable accuracy rules

1. **Do not invent facts.** Do not fabricate statistics, names, quotes, outcomes, clients, organizations, titles, dates, research findings, or testimonials.
2. **Distinguish evidence from interpretation.** State what the source shows, then clearly label the conclusion or recommendation.
3. **Preserve meaningful uncertainty.** If a result has large ranges, weak evidence, important assumptions, or correlation rather than causation, say so plainly.
4. **Use exact details when supported.** Specific figures, dates, roles, and outcomes are usually stronger than broad descriptions. Do not turn a rough estimate into a falsely precise number.
5. **Ask for missing evidence early.** If the post depends on a claim the user cannot support, either remove it, soften it, or request a source.
6. **Avoid misleading urgency.** Do not exaggerate stakes merely to create engagement. A sharp, specific risk and a practical response are more credible than alarm.

## Audience and voice

Write for the reader who is most likely to act on the post, not for everyone who might vaguely relate to it. Specificity is a filter. It helps the right people recognize that the post is for them.

Default voice unless the user provides another one:

- Direct, clear, and conversational.
- Short sentences and concrete nouns.
- Active voice where possible.
- One main claim per sentence.
- Sober about problems, practical about responses.
- Specific rather than promotional.
- Confident only where the evidence supports confidence.

Avoid three common failure modes:

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are thrilled to announce an exciting new initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences full of unexplained terms. | State the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Broad catastrophe language without a clear mechanism or response. | Name the specific risk, evidence, uncertainty, and useful intervention. |

## The core workflow

### 1. Inspect the source before choosing a format

Do not start with a template. Read the source and find the strongest material buried inside it.

Look for:

- An unusual or surprising fact.
- A specific number that creates tension.
- A counterintuitive conclusion that can be defended.
- A concrete before-and-after outcome.
- A meaningful trade-off.
- A sharp disagreement between credible views.
- A useful framework, checklist, or model.
- A sentence that changes how a reader sees the problem.

The formal headline of an article is often not the best social-post angle. The strongest thread may be a detail in the middle of the source.

If there are several strong angles, do not silently choose one. Present two to four numbered options. For each, state what it foregrounds and why it may work for the intended audience.

**Angle-selection prompt:**

> I see several viable post angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [specific story, outcome, or disagreement]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Choose one primary thread. A social post is not a summary of every point in the source.

### 2. Generate hooks before drafting the body

The opening determines whether the rest of the post is read. Generate five to ten possible hooks internally, then show a shortlist of three to five strong options when user choice would help.

A hook should make an honest promise that the body fulfills. It should generally work on its own, without requiring the reader to understand the full source first.

Useful hook patterns:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific body of evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Named outcome:** “[Person or role] moved from [starting point] to [specific outcome] in [timeframe].” Use only with approval and evidence.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Only if the post defends this claim.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused question:** “Why do two credible groups reach such different conclusions about [specific issue]?”

For each shortlisted hook, add a brief strategic note.

| Hook | Strategic purpose |
|---|---|
| “[Specific claim or finding].” | Leads with a concrete result and gives readers a reason to continue. |

Reject hooks that are interchangeable across unrelated topics. If “governance,” “research,” or “product development” could be swapped for “marketing” and the hook still works, it is probably too generic.

Avoid:

- Generic announcement openings such as “Excited to share.”
- Throat-clearing such as “In today’s fast-moving environment.”
- Empty cliffhangers that do not deliver a payoff.
- Multiple rhetorical questions in a row.
- Broad motivational claims.
- Clickbait phrases such as “You will not believe” or “This changes everything.”

### 3. Choose one structure

Select the structure that fits the source. Do not combine several structures unless there is a clear reason.

1. **Counterintuitive claim → evidence → implication**  
   Best for research, data, and argument posts. Start with the surprise, show the supporting facts, then explain what the reader should do or reconsider.

2. **Changed mind → trigger → updated view → takeaway**  
   Best for thoughtful first-person posts. State the previous view, explain what changed it, and give the new conclusion.

3. **Problem → why it matters → practical response**  
   Best for explainers and policy or operational content. Keep the problem concrete and make the response proportionate.

4. **Result → how it happened → reusable lesson**  
   Best for launches, team outcomes, and case studies. The result must be real and specific.

5. **Framework → examples → application**  
   Best for posts readers may save and revisit. Give the framework a useful name only if the name clarifies rather than brands ordinary advice.

6. **Specific announcement → reader relevance → next step**  
   Use only when the announcement itself is genuinely notable. Lead with what happened and its practical significance.

7. **Strategic trade-off → rationale → consequence**  
   Useful when explaining deliberate constraints or “anti-goals”: what an organization has intentionally chosen not to optimize for, and why.

### 4. Draft the body: hook, tension, payoff

Use this default shape:

- **Hook:** The strongest claim, result, or tension.
- **Tension or setup:** Why the point matters, what is surprising about it, or what assumption it challenges.
- **Payoff:** The evidence, story, framework, or practical insight. The post should be valuable even if the reader never opens a link.
- **Soft close:** Exactly one focused question, one practical takeaway, or one clear pointer to more material.

A useful default length is under 300 words, but length should follow substance and platform norms. Short posts should still contain a complete point. Longer posts need a reason for every paragraph.

Use white space. Write in one- or two-sentence paragraphs so the post is easy to scan on a phone. Use bullets only when the content is genuinely list-shaped, such as three reasons, four findings, or a checklist.

For a carousel or document caption:

- Use the post to establish the central idea.
- Include one or two of the strongest specifics.
- Tell readers what the visual material adds.
- Do not turn the caption into a slide-by-slide summary.

For a linked article or podcast:

- Put the strongest finding in the body.
- Treat the linked item as depth, sources, or extended analysis.
- Follow the user’s platform strategy for link placement.
- Never make “read the link” the main value proposition.

## Calls to action and questions

Use one close only. A strong close gives the reader a real, bounded way to respond.

Good examples:

- “Which of these constraints is most important in your work?”
- “What evidence would change your view?”
- “The full analysis includes the assumptions and source material.”
- “If you have operated this system, where does this model fail?”

Weak examples:

- “Thoughts?”
- “Let me know what you think.”
- Several questions at once.
- Requests to comment, tag, repost, or react merely to boost engagement.

A question should invite knowledge, disagreement, or experience. Do not use engagement bait.

## Editing rules: remove templated and inflated language

Run a separate editing pass after drafting. Cut phrases that sound polished but say little.

Replace or remove:

- Inflated corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Hedging frames such as “it is worth noting,” “one might say,” and “arguably,” unless uncertainty is genuinely important.
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Abstract nouns doing the work, such as “journey,” “transformation,” or “paradigm,” when a concrete event can be named.
- Transition sentences that merely repeat the previous paragraph.
- Dramatic framing such as “The truth is” or “Here is the reality.” State the point directly.
- Decorative punctuation or formatting that the chosen platform will not render correctly.

If the user has a punctuation preference, obey it. Otherwise, favor periods, commas, and line breaks over theatrical punctuation. Read the draft aloud. If it sounds like a generic thought-leadership template rather than a person making a specific point, rewrite it.

## Revision protocol

When the user gives feedback, revise the requested line and the nearby logic first. Do not rewrite the entire post unless asked.

Examples:

- If the hook is “not sharp enough,” provide several replacement hooks before changing the body.
- If a claim feels overstated, tighten the evidence or soften only that claim.
- If a paragraph feels slow, cut setup before adding more explanation.
- If the user prefers an earlier sentence, preserve it unless there is a clear reason not to.

Multiple small options are often more useful than one complete redraft, especially for hooks, closers, and uncertain lines.

Be candid about weak material. For example:

> The second paragraph relies on a broad claim that the source does not yet support. We can either add evidence, make it narrower, or replace it with this concrete example: [example].

## Readiness gate and audit

Do not present a draft as final until it passes this checklist.

- Does the first line earn attention when read alone?
- Is the post about one clear point rather than several competing ideas?
- Is there at least one concrete detail, outcome, example, number, or mechanism where appropriate?
- Could the main claim be defended if a knowledgeable reader challenged it?
- Does the post provide value without requiring a click, swipe, or purchase?
- Is uncertainty stated where it materially affects the conclusion?
- Is the language specific to this topic, rather than reusable for any industry?
- Is the close one focused action, question, or pointer?
- Are all names, quotes, figures, and claims approved or supported by source material?
- Does formatting work on the intended platform?
- Does the tone remain professional, respectful, and non-inflammatory for the intended audience?

If any answer is no, revise before handoff.

## Handoff format

When presenting work to the user, provide only what helps them decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen delivery format or location.
3. Any unsupported claim, missing input, or line that remains uncertain.
4. Suggested first-comment or link text, if relevant to the platform strategy.
5. A concise publishing reminder appropriate to the platform, such as responding promptly and substantively to genuine early comments.

Do not claim that a particular format, timing tactic, or engagement metric is guaranteed to improve reach. Platform behavior changes frequently. Treat distribution advice as a testable hypothesis, and encourage the user to compare results across several posts.

## Common failure patterns

- **Announcement disguised as content:** The post tells readers the organization is pleased, but not why readers should care. Fix it by leading with the actual change or lesson.
- **Pure teaser:** The post asks readers to click but provides no useful insight. Fix it by sharing the main finding and using the linked piece for depth.
- **Unsupported precision:** The post uses a striking figure without a source, scope, or caveat. Fix it by verifying, qualifying, or removing it.
- **Generic inspiration:** The post sounds positive but has no mechanism, example, or decision. Fix it by naming the concrete action or trade-off.
- **Overpacked summary:** The post tries to cover every section of a report. Fix it by selecting one thread and saving the rest for the original material or later posts.
- **Bolted-on promotion:** A course, product, or service appears at the end without a natural connection. Fix it by removing the pitch, creating a separate promotional post, or making the connection concrete and immediate.
- **Forced engagement:** The post demands reactions or comments. Fix it by asking one real question or ending with a useful conclusion.

The final standard is simple: the post should sound like someone with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, or a generic social-media template.


---
name: case-study-post
description: Create an evidence-based case study post about a person’s professional, learning, or career change. This workflow produces a verified, review-ready draft, alternate hooks, quote-card options, approval flags, and a publishing handoff.
---

# Write a case study post

Use this workflow to turn source material about a person into a concise public case study. It works for professional social posts, newsletters, community updates, program alumni stories, recruitment pages, and similar formats.

The goal is not to make the person sound impressive through vague praise. The goal is to show a credible, specific change: where they started, what they were considering, what prompted action, what concretely helped, what they do now, and what a relevant reader can do next.

A strong case study helps the reader recognize their own situation in the subject’s before-state. It names the intervention clearly, explains the mechanism without overstating causation, and lets verified facts carry the story.

## Purpose, authorization, and access boundary

Before using interviews, applications, private messages, internal records, or profiles, confirm that there is a legitimate publishing purpose and clear authorization to use the material. Use only the minimum relevant sources and details needed for the story.

Do not include unrelated personal information, sensitive details, private contact information, or facts the subject would not reasonably expect to see publicly. Respect any consent limits, publication agreements, confidentiality obligations, and access boundaries. If a fact is useful but its publication status is unclear, treat it as requiring approval.

## Inputs

Ask for all available source material. This may include:

- An interview transcript and meeting notes
- An application, intake form, or written reflection
- A professional profile or approved biography
- Public work samples, papers, projects, products, or announcements
- An internal message noting a result or milestone
- A rough outline, prior draft, or editorial notes
- The target audience, publishing channel, desired outcome, and call to action
- A voice guide or examples of previously approved writing
- The subject’s public-name preference, pronouns, and any known approval constraints

Before drafting, identify whether you have enough verified information for the following fields.

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns, and permission status |
| Before-state | Previous role, field, goal, uncertainty, or constraint |
| Trigger | Why they joined, applied, changed direction, or took action |
| Intervention | Program, community, product, mentor, event, or resource involved |
| Mechanism | Concrete help, such as a realization, opportunity, introduction, feedback session, or resource |
| Now-state | Current role, organization, team, project, output, or result |
| Timeline | Dates or time spans from starting point to outcome |
| Evidence | Verified roles, figures, dates, named work, and direct quotes |
| Cost or risk | Pay change, move, uncertainty, career tradeoff, or other relevant constraint |
| CTA | What the reader should do next |

If critical facts are missing, ask focused questions before drafting. Do not guess at organization names, job titles, paper titles, dates, figures, timelines, outcomes, or the subject’s motivation.

Useful questions include:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they decide to take part or make a change at that point?
4. What are the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a specific output, project, placement, publication, product, or result that can be named publicly?
8. Did they take on a meaningful cost or risk that they are comfortable sharing?
9. Which claims, figures, quotes, names, and descriptions are approved for public use?
10. Who should this post persuade, help, or invite to act?

## Evidence and verification rules

Never invent facts or strengthen a claim for dramatic effect. If a source says someone contributed to a project, do not call them the lead. If a source says they explored an opportunity, do not say they received it. If a source says they found an opening through a community, do not imply that the community secured the job for them.

Treat automated transcripts and summaries as useful but fallible. They can mishear names, organizations, technical terms, numbers, titles, and dates. Cross-check important details against a more reliable source, such as the subject’s direct confirmation, an official public record, an approved professional profile, published work, or an original written statement.

Use this reliability order unless there is a clear reason to depart from it:

1. The subject’s direct, recent confirmation
2. Official public records, employer announcements, or published work
3. A current approved professional profile
4. An original application or written statement from the subject
5. Interview transcripts, meeting notes, or automated summaries
6. Informal third-party messages

Separate statements in working notes into three categories:

- **Verified fact:** A role, date, artifact, figure, or quote supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn from the story. Use this only when evidence supports it, and phrase it carefully.

Do not claim that a course, community, product, mentor, or event caused the entire outcome unless that claim is clearly supported and approved. Prefer precise language such as “the program helped them see the field differently,” “they learned about the opportunity through the community,” or “a conversation helped them clarify their next step.”

## Sensitive-content gate

Flag the following for explicit subject approval before publication:

- Salary, pay cuts, financial hardship, or compensation comparisons
- Health, family, immigration, legal, or personal circumstances
- Strong criticism of a former employer, role, or career decision
- Unreleased work, confidential projects, or unpublished titles
- Direct quotations, especially strong opinions or criticism
- Claims about why an employer selected the person
- Claims of causation or impact that cannot be independently verified
- Precise dates or timelines that could reveal private circumstances

If approval is unavailable, use an honest fallback only if it remains accurate and useful. For example, replace an exact compensation figure with “they accepted a lower-paying role” only when that broader statement is approved. Do not conceal uncertainty by making a story more dramatic.

## Build the story beats

Create a private working outline before writing. Keep it concise and do not expose internal notes unless the user asks for them.

### 1. Before-state

Capture the subject’s role, background, and the reader-relevant version of their uncertainty. Include what they were considering instead when that alternative resembles the audience’s current life.

Keep only details that move the story. A list of books read, credentials, old roles, or minor achievements often weakens the post. Keep a detail when it makes the transition believable or explains the decision.

### 2. Trigger

Identify why the subject acted at that moment. They may have wanted to learn about a new field, determine whether a role was accessible, meet collaborators, test a direction, solve a practical problem, or make a values-based change.

### 3. Mechanism

Find the one or two concrete things that changed the trajectory. Strong mechanisms are observable:

- A realization that a field or role was open to people with their background
- A relevant opportunity shared through a community
- A conversation that clarified an application, project, or next step
- Feedback that improved a work sample or application
- A specific introduction, workshop, or practical resource

Avoid saying an experience was “transformative.” State what happened instead.

### 4. Now-state

Record the current role, organization or team if approved, and what the person actually does. Translate technical terms enough for the intended reader to understand the work.

Use named outputs only when they add proof or interest. Do not create a resume-like pileup. One meaningful project, publication, placement, product, or grant usually works better than a long credentials list.

### 5. Timeline and compression

Map the sequence from joining or starting to the current outcome. Calculate a short, truthful timeframe when it sharpens the story, such as “within six months” or “the following year.” Do not force a compressed timeline if the evidence does not support it.

### 6. Quotes

Pull three to five verbatim candidate quotes. Favor quotes that speak to the reader’s identity or uncertainty, not only to the subject’s achievement.

Good categories include:

1. **Discovery:** “I did not know this path was open to someone like me.”
2. **Mechanism:** “I found the opportunity through the community.”
3. **Conviction:** “I would make the same choice again.”

Light trimming is allowed only when it preserves meaning, grammar, and the subject’s words. Do not rewrite a quote into something the person did not say.

## Generate three hook options

For feed-based platforms, the first two lines determine whether readers continue. Write three distinct hooks before writing the full post. Keep each to two short sentences, usually under about 140 characters total when the platform rewards short openings.

### Hook A: Discovery

Use when the audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a concrete mechanism.

This is the default recommendation when the first sentence can mirror the reader’s own uncertainty.

### Hook B: Identity collision

Use when the before-and-after contrast is vivid and understandable.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This works well for a broad audience that may not share the subject’s exact blocker.

### Hook C: Stakes-led

Use only when a meaningful cost or risk has been approved and the audience will read it as honest conviction rather than a warning.

**Formula:** The subject accepted a specific cost to do something. Now they are taking a concrete action or doing meaningful work.

Do not use a sacrifice hook if it suggests that participation requires hardship or distracts from a more accessible message.

Choose one recommended hook. Give a one-sentence reason it fits the target audience, and one short reason each for not choosing the other two.

## Draft the post

Aim for roughly 160 to 220 words unless the platform or audience calls for a different length. Shorter is usually stronger.

Use this sequence:

1. **Hook:** Use the recommended hook.
2. **Before-state:** One short paragraph showing the person’s previous situation and a relevant alternative path.
3. **Name the intervention:** State clearly that they joined the program, used the resource, attended the event, or entered the community. Do not leave the intervention implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then land the immediate result in plain language. A short sentence such as “They applied and got in” can be stronger than a detailed account.
5. **Current work:** Describe what they do now and why it matters in terms the reader can understand.
6. **Optional honest cost:** Include only when approved and genuinely useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already carried by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

If the publishing platform may reduce reach for external links in the post body, place the link in a comment, profile destination, or designated landing location instead. Treat this as a channel-specific publishing choice, not a universal rule.

## Style rules

Adapt to the chosen voice guide. If none exists, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use concrete names, roles, dates, and figures only when verified and approved.
- Use the subject’s first name after the first full introduction only if that fits the publication’s tone and the subject’s preference.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not call someone exceptional, inspiring, or brilliant without showing why.
- Use contractions if the intended voice is conversational.
- Keep the CTA in full second person: “If you are…” and “you can…”
- Avoid emojis unless they are an explicit brand choice.
- Do not use em dashes. Use periods, commas, or line breaks instead.

On the final pass, remove common machine-like phrasing. Cut empty transitions, dramatic setup frames, filler intensifiers, hedge words, abstract nouns that replace evidence, balanced “on one hand/on the other hand” constructions, and reflective summary sentences after the CTA.

Avoid corporate or vague terms such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm” unless they are necessary in a direct quote. Read the draft aloud. If it sounds like generic thought leadership, shorten it and replace abstractions with facts.

## Graphic quote options

Provide three options for a visual quote card. Each should be self-contained, under 15 words when possible, and verbatim from approved source material.

Offer one quote from each category:

- Discovery
- Mechanism
- Conviction

Recommend one quote. Discovery quotes often work best because they stand alone and mirror a reader’s uncertainty. Choose a mechanism or conviction quote instead only when it is clearer, more memorable, and understandable without context.

## Readiness audit

Before sending the draft for review, check all of the following:

- Is every name, role, date, figure, and title verified?
- Have transcript-derived details been cross-checked where needed?
- Does the post show a concrete mechanism, not only a result?
- Does it avoid overstating causation?
- Is the intervention named clearly?
- Does the opening mirror a real audience concern?
- Is the current work understandable to a non-specialist reader?
- Have sensitive claims and direct quotes been flagged for approval?
- Is the CTA clear and directed at the intended reader?
- Are there no em dashes, unsupported superlatives, corporate phrases, or generic filler?
- Does the post stay within the subject’s consent and the publisher’s authorized access boundary?

## Delivery and iteration

Create the draft in the user’s chosen document system when one is available. Use a clear title format such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and the two alternatives
- The three graphic quote options and the recommendation
- A list of approval items
- A list of missing information that would strengthen the post
- The document location or link, if applicable

Do not treat the first draft as final. If feedback says “make the hook better,” generate new hooks rather than making tiny edits. If asked to make it shorter, cut secondary biography first while preserving the mechanism and outcome. If a subject rejects a sensitive line, replace it with the approved fallback without weakening the whole story.

After the final version is accepted, review feedback for reusable lessons. Update the workflow only when a recurring pattern is clear, such as a missing intake question, a consistent voice preference, a repeated verification issue, or a structural edit that improves reader understanding. Do not invent process changes from a clean review cycle.


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
name: prepare-for-a-meeting
description: Gather the relevant history, clarify the desired outcome, and produce a focused agenda and preparation brief.
---

# Prepare for a meeting

Use this before a consequential meeting or when the user asks for an agenda.

## 1. Read the meeting

Check the invitation, attendees, timing, stated purpose, and linked materials.
Read any supplied proposal, document, or deck in full before drafting an agenda.

## 2. Gather context

Search the sources most likely to contain the relationship history, prior
decisions, promises, open questions, and recent changes. A recent transcript or
meeting note often matters more than older summaries.

Distinguish facts, other people's views, and the user's current position. Do not
infer what the user wants to promise.

## 3. Ask focused questions

Before drafting, summarize what the evidence establishes and ask a small number
of questions about:

- The desired result.
- The user's current stance.
- Sensitive topics or boundaries.
- Decisions that can and cannot be made in the meeting.

## 4. Prepare the brief

Include:

- The meeting's job.
- Essential context.
- The user's desired outcome.
- A short agenda ordered by importance.
- Questions to ask.
- Likely objections or difficult moments.
- Decisions, owners, and follow-up to capture.

Keep the agenda realistic for the available time. Put the most important topic
before status updates and background.


---
name: capture-meeting-actions
description: Review authorized meeting records to identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow for a daily sweep, a selected date or date range, or a manually supplied set of meeting records.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose, authorization, and operating rules

Use meeting records only for a legitimate purpose and with clear authorization to access the selected meetings, transcripts, notes, and task workspace. Use the minimum relevant sources and details. Do not transfer unrelated personal, confidential, health, compensation, or other sensitive information into tasks. Keep notes within the access boundary of the chosen task workspace and respect participant consent and privacy expectations.

Apply these rules throughout the run:

- **0 tasks** when work was completed during the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same recipient or group, on the same time horizon.
- **Multiple tasks** only when recipients, outcomes, or timing differ materially.

When sources conflict, use this evidence order:

1. **Transcript or recording-derived text:** strongest evidence of who accepted an action and when it is due.
2. **Human-written notes:** supporting evidence, especially explicit notes or action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** evidence of intended discussion, not a commitment.

Automated summaries commonly assign actions to the wrong attendee, especially in recurring one-to-ones, brainstorming sessions, and meetings where several people list their own to-dos. Never create a task solely because a summary calls something an action item. Confirm ownership in the transcript or reliable notes.

Track unfinished outcomes, not conversation. An idea, interest statement, request, or open question is not a task unless the user explicitly accepted responsibility for a concrete outcome. Apply responsibility boundaries supplied by the user. Attending a meeting does not make the user accountable for all related work.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied list of meetings. If no scope is supplied, use this default:

- Before a user-configurable early-morning cutoff in local time, process the previous day.
- Otherwise, process the current day.

State the scope once, for example: “Scanning meetings for 23 Apr.” Locate meetings attended by the user and collect only what is necessary:

- Title, date, and time
- Meeting-record link or identifier
- Attendees, when available and relevant
- Transcript, notes, summary, and directly relevant linked context

Report a compact meeting count before processing. Do not infer commitments from a meeting title alone.

## 2. Fetch and inspect complete records

Fetch complete records in parallel when the selected record system supports batching. Do not search for existing tasks yet: first identify the people, topics, and candidate outcomes needed for accurate duplicate checks.

For long transcripts, use a repeatable search, extraction, or chunking method rather than trusting truncated previews. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by explicit acceptance

Treat summary action items as candidates. Verify each candidate against the transcript and nearby conversation. A promise may have been conditional, reassigned, fulfilled during the meeting, or made by someone else.

## 3. Triage each meeting

Classify meetings loosely. Classification provides an expected starting point, not a rule that overrides evidence.

| Meeting type | Usual outcome | Guidance |
|---|---:|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or explicitly timed follow-up. |
| Information-gathering, interview, or reference discussion | 0 tasks | Create work only for an explicit out-of-meeting commitment. |
| Internal planning or team meeting | 0–1 user-owned task | Capture the user’s deliverable, not the whole group action list. |
| Coaching or recurring one-to-one | 0–1 task | Usually create a task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1–2 tasks | Often separate an internal decision from an external response. |

For every meeting, identify:

- Relationship context and why the meeting occurred
- Candidate actions owned by the user
- Work completed during the meeting
- Work delegated to another named owner
- Explicit future commitments and timing
- Enough neutral context for a task to remain understandable weeks later
- Authorized source links and related documents, if appropriate to retain

Create no task when work was completed live, another person owns it, the meeting was purely informational and any necessary synthesis is already recorded, an active task covers the same outcome, or the statement was not a commitment.

## 4. Decide the task shape

Combine actions into one task when they have the same recipient, time horizon, and outcome. For example, sending promised material, answering related questions, and offering times to meet can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect several months later.
- Different recipients require separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would not have a clear finish line.

### Readiness gate

Do not create a task until it has all of the following:

- A clear user-owned outcome
- Evidence that the outcome remains unfinished
- A sensible task shape: combined or split appropriately
- A practical due date or review date
- Enough permitted context to stand alone later
- No unresolved duplicate or ownership concern

## 5. Write the task

Use the user’s chosen task workspace and field names. At minimum, capture:

- **Title:** short, verb-led, and specific, such as “Follow up with partner about pilot scope.”
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user’s scale; default to normal important work and reserve the highest level for a real deadline, material risk, or an awaiting recipient.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and authorized links.

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: agreed date, or a reasonable reminder date before it.
- Weekly or sprint commitment: the next relevant review or planning session.
- Flexible work: roughly one week, adjusted to workload.
- Older meetings processed late: move an immediate follow-up to the next workable date rather than assigning a date already passed, unless the original deadline still applies.

Do not raise priority merely because capture happened late.

### Notes template

```markdown
[Two or three sentences of time-independent context. Include relevant absolute
dates, why this matters, the commitment, and any necessary sensitivity. Omit
unrelated or sensitive personal details.]

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

Avoid unnecessary private discussion in any workspace that may be visible to others. Follow the user’s writing preferences. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable. If the task is to send a message, include a ready-to-send draft rather than merely writing “email them.” For introductions, use double opt-in: seek permission from each relevant person before connecting them.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by authorized meeting reference, relevant person or group, distinctive topic terms, and the proposed title.

Treat a task as a duplicate when it covers the same outcome, not merely when wording matches. Skip the new task, or update the existing task if the meeting adds a meaningful action, deadline, or permitted context. Record the decision for the final report.

## 7. Create confident tasks

Create high-confidence tasks in a batch when supported. If the chosen workspace can display newly created tasks directly, use that capability rather than placing administrative links in the status update.

For every skipped meeting, give one brief reason, such as:

- “No out-of-meeting commitment.”
- “Completed during the meeting.”
- “Owned by another role.”
- “Already covered by an active task.”

## 8. Batch uncertain questions

Skip this step entirely if all decisions are confident. Do not interrupt once per ambiguity. Create confident tasks first, then ask all remaining questions together.

Ask the smallest question that resolves ownership, scope, timing, completion status, responsibility boundary, or duplicate handling:

```markdown
**[Meeting title]**
Question: [One specific question]
Context: [One sentence grounded in the authorized record]
Option A: [Task to create or update if true]
Option B: [Skip or alternate task shape]
```

Wait for answers before creating uncertain tasks. After answers arrive, create or update the remaining tasks and repeat the duplicate check if the answer changes the outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, capture lessons that genuinely improve future runs. Keep reusable guidance separate from individual meeting tasks.

- Add a short generalized pattern to a meeting-triage reference when a recurring issue affects decisions, such as a common attribution error, a reliable sign of live completion, or a meeting-type exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a genuinely new required step.
- Record a new responsibility boundary in the user’s maintained reference only if it applies beyond one meeting.

Do not turn one-off facts into permanent rules. Small additions to a patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as changing the evidence order or adding or removing a step. Briefly report any reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a clear user-owned and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each retained source link is appropriate and authorized.
- Message drafts are ready to send and follow the user’s preferences.
- Task notes omit unrelated sensitive information.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report only the essential outcome: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and reusable guidance changes. Keep status updates terse and factual.


---
name: turn-a-message-into-a-task
description: Read a message or conversation, identify the real work, research only the context needed, and prepare the deliverable as far as authorization allows before creating a task record.
---

# Turn a message into a task

Use this workflow when one or more message links, conversation exports, emails, or collaboration-thread references may contain work that should be tracked. The goal is not merely to log a to-do. The goal is to reduce the remaining human action to the smallest safe, clear step: research the issue, prepare a draft or decision brief, and create a task only when tracking adds value.

Use only sources and tools the user is authorized to access. When a conversation includes personal, employment, financial, health, performance, or other sensitive information, access only the minimum relevant material, omit unrelated sensitive detail, and keep the output within the intended audience and access boundary.

## Operating principles

- Read the complete relevant conversation before deciding what the task is.
- Treat the linked message as the anchor, but treat later replies as potentially decisive.
- Do enough research to act confidently or to name the exact blocker. Do not perform a blanket search.
- Draft external-facing actions; do not send messages, emails, invitations, approvals, or other consequential actions without explicit authorization.
- Prefer one task for one coherent outcome. Split work only when ownership, finish conditions, or timing genuinely differ.
- Never create a task for work that is already completed, superseded, or clearly owned and tracked elsewhere.
- Never invent facts, links, dates, or commitments. Mark uncertain information clearly.

## 1. Read the whole conversation

First resolve the message reference using the user’s chosen communication system. If it points to a reply, retrieve the parent and all thread replies. If it points to a top-level message, retrieve a small time window around it and then retrieve its thread if replies exist. Some systems do not return a message when the start and end timestamps are identical; use a narrow range instead.

Capture the following:

- The requester, accountable user, and any other named participants.
- The actual request, not just the wording of the opening message.
- Promises, decisions, deadlines, dependencies, and linked material.
- Whether later replies answer the question, change the requested outcome, reassign the work, or close it.
- Whether the request contains several related parts.

Resolve identities carefully. If display names are absent, use authorized profile information or explicit mentions in the message. In the task and draft, refer to people by an appropriate name or role rather than vague phrases such as “that person.”

### Recency gate

Before doing research or creating a record, inspect replies and updates posted after the anchor message. If the work appears complete, superseded, or reassigned, do not create a stale task. Report the finding and ask the user only if the status is genuinely ambiguous.

## 2. Classify the real task

State the task shape in your working notes. The classification determines what “pre-completed” work should look like.

| Task shape | What is owed | Best pre-completion |
|---|---|---|
| Reply owed | An answer, feedback, decision, introduction, or acknowledgement | A concise reply draft, ideally staged in the original thread if supported |
| Artefact owed | A document, reference, analysis, data pull, plan, or other deliverable | The artefact or a usable first draft |
| Decision needed | A choice that only the accountable user can make | A short options brief, evidence, recommendation, and likely reply draft |
| Delegation or follow-up | A chase, handoff, scheduling step, or process action | A drafted follow-up, handoff note, or safely pre-filled action |
| Information request | A factual answer or status update | Verified answer with sources and a draft response |

A multi-part request normally remains one task if it has one owner and one practical time horizon. Put sub-parts in the notes and give each a clear finish condition. Split it only if different people own parts, deadlines differ substantially, or one part can be completed independently without helping the others.

Rewrite the task as an observable outcome. For example, use “Send a drafted response confirming the event plan” rather than “Follow up about event.”

## 3. Gather targeted context

Choose sources based on the task, not habit. Confirm that access is legitimate and proportionate before opening private records.

Typical source choices include:

- **Person-related context:** prior authorized correspondence, meeting notes, work records, role-relevant assessment evidence, and relevant project conversations.
- **Project or event context:** recent channel history, project plans, linked documents, logistics records, and post-project reviews.
- **Data questions:** the organization’s source-of-record database, prior reports, planning documents, and operational correspondence that can verify numbers or dates.
- **Parallel requests:** a topic-based search across authorized conversations to identify duplicate questions or a prior answer that can be reused.
- **Linked content:** open and read relevant links. For multi-section documents, inspect the document structure first and read every relevant section; the message may mention only one of several decisions required.
- **Policy or process questions:** the current policy source, documented precedent, and the responsible process owner’s guidance. Use analogous policies as an input, not proof that the same rule applies everywhere.

For hiring, references, feedback, or assessments, use role-relevant capabilities, observed work, documented evidence, and role alignment. Do not include unrelated personal information or unsupported judgments.

Use public web research only when it is appropriate and authorized. Prefer non-invasive retrieval methods and avoid tools that create visible activity or modify external systems unless the user has explicitly approved that behavior.

### Research stop rule

Stop when you can do the requested work safely, prepare a meaningful draft, or state precisely what prevents progress. Two or three strong sources are usually better than many shallow searches.

## 4. Pre-complete the work

Do as much as can be done without making irreversible or externally visible commitments.

### Drafts and artefacts

- For a reply, prepare the full reply, not merely bullet points.
- For a reference, plan, analysis, or other artefact, produce a usable draft with evidence where possible.
- For a decision, provide two or three viable options, evidence for each, a recommendation, and the reason for it.
- For follow-up work, draft the chase or handoff message and identify who should receive it.

If the user has provided a writing guide, approved examples, or a documented voice standard, read and follow it before writing in their voice. Otherwise, use concise, plain language. Avoid unnecessary framing, ceremonial lead-ins, and overlong coaching. Ask simple questions when one simple question will resolve the issue. State future commitments cautiously when they are not guaranteed.

If the communication system supports private drafts, stage the reply in the original thread rather than sending it. Ensure lists render correctly in that system: where needed, leave a blank line before a list and test the platform’s native list formatting. Store the identical draft in the task notes so the record remains self-contained.

### Accuracy and gaps

Do not guess facts, dates, quantities, policy positions, or URLs. Use explicit markers such as:

- `[VERIFY: confirm current figure in source-of-record]`
- `[SEARCH: locate the current public policy page]`
- `[FILL IN: firsthand detail about what happened at the event]`

Use `[FILL IN]` when only the user’s memory, relationship judgment, or in-room experience can supply the material. A draft with obvious, specific blanks is often more useful than a blank page, but clearly warn that it cannot be sent as-is.

End the preparation with a concise **Remaining for user** list. Each item must be specific, such as “Confirm whether you are willing to be named as a future reference,” not “Review and complete.”

## 5. Ask questions only for real forks

Before asking questions, check whether the answer already exists in the thread, a prior message, an approved planning document, or another authorized source. A documented position should normally guide the draft more reliably than a new question.

Ask only if a wrong assumption would cost more time or create more risk than interrupting the user. When blocked, provide one or two short paragraphs of context first: who is involved, what has happened, what is now being requested, and the relevant trade-offs. Then ask two to four targeted questions. Allow multiple selections or a custom answer when the user may reasonably combine options.

If no material fork remains, make a reasonable metadata and drafting judgment, disclose it in the final report, and let the user correct it later.

## 6. Decide whether a task record is needed

Do not create a record merely because a message was supplied.

Skip the record when the work is complete, stale, duplicated, trivial, or consists only of reviewing and sending a staged short draft in a single brief sitting. Deliver the context and draft directly instead.

Create a record when one or more conditions apply:

- Work must be deferred or cannot responsibly be completed now.
- A deadline, waiting period, dependency, or follow-up needs tracking.
- Multiple steps remain or the steps span several days.
- The user explicitly requested a record.

When uncertain, prefer chat-only delivery for a simple reply and a task record for substantive artefacts, decisions, or multi-step work.

## 7. Create a useful task record

Use the user’s chosen task system and its current schema. Confirm available values such as status, priority, domains, projects, or owners rather than relying on stale IDs or names.

Set:

- **Title:** imperative, specific, and short enough to scan.
- **Status:** the appropriate open state.
- **Due date:** only when a deadline is explicit or strongly implied.
- **Importance and urgency:** best judgment based on consequences, deadline, and people waiting.
- **Time estimate:** remaining human work only, not research already completed.
- **Project/domain:** the best supported classification.
- **Notes:** source, context, prepared work, and remaining action.

Use this notes template:

```markdown
**What:** [One-line statement of the ask and who is waiting.]
**Source:** [Conversation link or reference]
**Context:**
- [Relevant background and verified fact.]
- [Relevant deadline, dependency, or decision.]

**Pre-completed:**
[Full draft reply, artefact, decision brief, or staged-action details.]

**Remaining for user:**
- [Specific final action.]
```

After creating the record, open or retrieve it to verify that the title, notes, links, dates, and status were saved correctly. Do not expose internal record links outside the audience authorized for that system.

## 8. Report back

If a record was created, report in this order:

1. What the task is.
2. What was pre-completed, including where any draft was staged.
3. Metadata judgments: priority, urgency, due date if any, and estimated remaining time.
4. Any `[VERIFY]`, `[SEARCH]`, or `[FILL IN]` flags.

If no record was needed, use this format. Keep the draft as the final block so it can be copied without cleanup.

```markdown
## Context for user (not part of the reply)
- [What the ask is and who is waiting.]
- [Key verified facts and judgment calls.]
- [Whether a draft was staged and any verification flags.]

## The reply
[Draft verbatim]
```

## 9. Learn from approved drafts

When a draft is staged, a later comparison between the staged version and the user’s eventual sent version can improve future drafting. Run this review only with legitimate access and authorization. Re-read the thread, compare changes, and record only general lessons: preferred brevity, recurring process routing, voice conventions, or formatting behavior. Do not retain unnecessary private details.

If the message has not been sent, check at most a small number of times at widening intervals, then stop. Non-sending may be intentional. Do not modify workflow documentation, persistent memory, or shared systems automatically unless the user has authorized that maintenance. When authorized, make small, general edits and maintain an auditable change log.

## Final audit

Before finishing, verify:

- The full thread and later replies were checked.
- The task is not already done, superseded, or duplicated.
- Research was relevant, authorized, and minimal.
- No external action was sent without approval.
- Facts and links are verified or clearly marked as gaps.
- The record, if created, contains a real pre-completed deliverable.
- Remaining work is concrete and appropriately small.
- Sensitive details are limited to what the intended audience needs.


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
description: Complete browser-based tasks safely by selecting the least invasive authorized method, verifying account context and rendered state, and separating preparation from consequential final actions.
---

# Use a browser safely

Use this workflow for browser-based work such as completing rendered forms, changing settings, collecting data from dynamic pages, testing a user flow, or using an authenticated dashboard. Use it only when a supported direct interface, API, or ordinary page retrieval cannot safely and reliably complete the request.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and never take a consequential final action until the account, target, authorization, and page state are verified.

A successful automation command does not prove that a website accepted the change. Modern applications may keep their own internal state, commit fields only after focus leaves them, replace controls during a re-render, or display an error even when an action actually completed.

## 1. Select the least invasive suitable method

Choose the first method that fits the task safely:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic route when it can complete the task. It is often more reliable than simulating a browser.
2. **Headless browser automation.** Use this for public pages, test systems, rendered-page extraction, screenshots, and forms that do not require the user's existing signed-in identity.
3. **User-visible authenticated browser.** Use this only when the task genuinely needs an existing session, single sign-on, an account-specific dashboard, or the user explicitly directs work in that context.

Before driving a browser, check for a legitimate direct route. Review official documentation, ordinary form actions, page source, and visible network requests for supported endpoints. A web form may submit structured data to an authorized service directly.

Do not use undocumented interfaces to bypass access controls, consent boundaries, service restrictions, or security protections. Do not use an authenticated visible session merely for convenience: it can interrupt the user's work and increases privacy and account risk.

If a site blocks automation, do not try to defeat the block for research, casual data collection, or access that is unavailable through normal means. A visible browser may be appropriate only for a legitimate, user-requested task on that specific site when the user has authorized access and an established session is necessary. Do not weaken browser security, access controls, warnings, or anti-abuse protections.

## 2. Protect authorization, privacy, and account context

When a task involves private communications, records, account dashboards, or information about people, establish a legitimate purpose and clear authorization. Access only the minimum relevant pages, records, and fields. Do not put unrelated personal information into screenshots, logs, notes, or reports. Keep all outputs within the requester's appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated context, identify the correct:

- Account and signed-in identity.
- Organization, workspace, or tenant.
- Environment, such as personal, work, test, staging, or production.
- Target page, record, setting, or transaction.
- Scope of authority for the requested action.

Never infer account identity from a generic browser name, tab title, remembered default, or connection label. Those signals can be stale or ambiguous.

Use these operating rules:

- Announce when taking control of a user-visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing tab to use.
- Classify the required context explicitly, such as personal, work, testing, or production.
- Select the browser profile or session associated with that context rather than using a generic or most-recent browser selector.
- Verify the signed-in account through a reliable account indicator before opening the real target or changing data.
- If the account, target, environment, authority, or requested scope is uncertain, stop and ask before making changes.
- Do not expose credentials, session tokens, recovery details, private account information, or security settings in output or logs.
- Do not disable multi-factor authentication, browser warnings, access restrictions, or other security controls to make a task easier.

If the automation environment has an account-verification gate, unlock or mark the session as verified only **after** the actual account check has passed. Do not create a marker, flag, or bypass before verification merely to enable browser actions.

A useful account preflight question is:

> Which account and environment are active, what exact object will change, and what authority permits this action?

Resolve uncertainty before continuing.

## 3. Establish the task boundary

Determine the desired outcome before navigating deeply. Identify:

- The target page, form, record, setting, or workflow.
- The information to enter, collect, modify, or upload.
- The minimum information needed to complete the request.
- Existing data that must not be overwritten.
- Whether the action is reversible.
- Whether the task sends, publishes, pays, deletes, changes a plan, changes access, or otherwise creates an external commitment.
- Missing details and choices that require the user's judgment.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and creating a preview may be reversible. Submitting, sending, publishing, purchasing, deleting, or applying a consequential change may not be.

For consequential work, use two phases:

1. **Preparation pass:** Fill or configure the page, verify the resulting state, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** After explicit user confirmation, re-check the account, target, and readiness gate. Then perform the final action once.

If the page reloads, re-renders, or the session changes between phases, do not assume the prepared state remains valid. Re-inspect, restore values if necessary, and verify again.

## 4. Inspect the rendered page before editing

Do not start by guessing selectors, filling controls by numeric position, or trusting a visual resemblance. First inspect the rendered page sufficiently to identify the true interactive controls.

For each relevant control, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, file upload, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value, required status, disabled state, and validation message.
- Character limits and formatting behavior.
- Whether an apparent field is an editable control, wrapper, or hidden synchronization element.
- Whether changing it or a related control causes a page re-render.

Address controls by stable semantic identity: visible label text, accessible name, or an explicit label relationship. Do not use DOM indexes where semantic labels exist. Dynamic applications may reorder controls during hydration or after changing another field.

Inspect the current state before changing a record or setting. This prevents modifying the wrong item or unintentionally replacing existing data.

### Generic inspection pattern

Use the chosen browser capability to list relevant controls before writing interaction logic. Record at least the tag, input type, role, label, required status, and current value or text length.

```js
// Pseudocode: adapt to the chosen automation library.
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

## 5. Use an interaction method that matches the control

A generic value-setting command is not reliable for every control. Use interaction that resembles ordinary user input when a framework-managed editor needs it.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use the normal text-input mechanism. | Line breaks may be silently removed. |
| Multiline text area | Fill text, then move focus away. | The application may commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select old text, delete it, enter text through keyboard-style events, then blur. | Direct DOM writes may not update the application's internal state. |
| Dropdown or combobox | Open it, choose by visible option text, then wait for state to settle. | Selection may trigger a re-render. |
| Checkbox or radio control | Read current state first; change only if needed. | A click can reverse an already-correct value. |
| Date/time picker | Choose the date and time, then verify the rendered summary. | Popovers may clear related values or reinterpret later typing. |
| File upload | Confirm the file, destination, recipients, and privacy implications first. | Uploading may begin immediately and may be difficult to undo. |

For a framework-driven editor, a robust general sequence is:

1. Locate the actual editable element, not only its wrapper.
2. Focus it.
3. Select existing content and delete it.
4. Enter the requested text through keyboard-style input.
5. Move focus to a neutral page element to commit the edit.
6. Wait briefly for rendering to settle.
7. Read the value back from the visible or accessible page state.

Some forms pair a visible editor with a hidden input. Updating the hidden input may look successful in a DOM inspection while server validation treats the visible editor as empty. Target the interactive editor that the application actually uses. If an accessibility locator returns an empty wrapper, inspect the underlying labelled editable element.

If a dropdown, checkbox, tab, category, or date selection can refresh the form, perform and verify those actions **before** entering lengthy or complex text. Re-inspect afterward and confirm earlier values still exist.

## 6. Verify after every meaningful edit

After filling a field or changing a setting, read it back from the rendered page. Compare the actual value with the intended value. For sensitive material, compare value length, required state, or a minimal redacted summary rather than copying the complete text into logs.

Look for these mismatches:

- Automation reports success, but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the field is single-line or has a limit.
- A custom editor displayed text but did not retain it internally.
- Editing a later control erased an earlier field after re-rendering.
- A hidden synchronization field changed instead of the visible editor.
- A selection changed a dependent recipient, date, validation rule, or required field.

If verification fails, do not continue toward submission. Diagnose the control type and retry once with a more appropriate interaction method. Verify the retry. If the page still changes, rejects, or cannot reliably display the intended value, report the limitation and ask how to proceed rather than silently submitting inaccurate content.

## 7. Run a pre-action readiness gate

Before any final submission or high-impact change, inspect the relevant page state again. Confirm all of the following:

- The correct account, organization, and environment are active.
- The target item is the intended one.
- Every required field is present and non-empty.
- Each important value matches the request closely enough.
- Recipients, options, dates, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **do not submit**. A partially completed page is often recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store it only in an authorized location. Avoid placing large amounts of sensitive field content in chat when a short summary and controlled-access record are sufficient.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 8. Require confirmation for one-way actions

Get explicit confirmation immediately before actions that are difficult to reverse, including:

- Sending messages, invitations, or notifications.
- Publishing content.
- Submitting official, externally reviewed, or final forms.
- Making a payment or purchase.
- Deleting records or files.
- Changing billing, subscription, access, ownership, or security settings.
- Actions described as permanent, final, irreversible, or not editable later.

Use this confirmation format:

> Ready to [final action] for [target]. Key details: [concise summary]. Impact: [cost, audience, permanence, or other consequence]. Open questions: [none or list]. Proceed?

Wait for an affirmative response before activating the final control. For low-risk, reversible changes explicitly requested by the user, proceed after normal verification unless the page presents an unexpected warning or broader impact.

## 9. Confirm completion, not merely a click

A button click is not proof of success. After the final action, seek reliable evidence such as a success message, confirmation reference, created record, persisted setting, sent item, published item, or changed status that remains after a safe refresh.

If the site shows an error, preserve the relevant message and inspect the resulting state before retrying. An apparent error can be cosmetic, while a blind retry can create duplicates such as repeated submissions, payments, messages, or records.

If completion cannot be verified, state what was attempted, the evidence available, and what remains uncertain. Do not describe an attempted action as completed.

## 10. Common failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change. | Use focus-and-keyboard interaction, blur, and read back. |
| Earlier fields disappear after a later edit | A re-render reset uncommitted state. | Commit and verify each field; make re-rendering selections first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used. | Find a multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node. | Inspect the labelled underlying control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited. | Use the visible interactive control that the application reads. |
| Automation is unstable on a complex page | The selected automation layer is unsuitable. | Switch to a more robust browser method or supported interface; do not blindly rescue a broken session. |
| Headless and visible browsers behave differently | The site varies behavior by browser context. | Prefer an authorized direct route; for an explicit legitimate task, use a verified visible session without evasion. |
| A popup changes dates or other fields unexpectedly | The widget has stateful close, clear, or parsing behavior. | Close through a neutral page action and re-verify all affected values. |
| An error appears after an action | The operation may have succeeded despite a cosmetic error. | Inspect the resulting state before retrying. |
| Account context is uncertain | The wrong profile, workspace, or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## Final audit checklist

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back and verified.
- [ ] Required fields and validation state passed the readiness gate.
- [ ] A pre-action record was captured when the action was consequential.
- [ ] Explicit confirmation was obtained immediately before a consequential final action.
- [ ] Success was verified after the action.
- [ ] The report separates confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, optimizing, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, improve an existing skill, evaluate whether a skill helps, or refine its triggering description. A skill is a focused package of instructions and optional resources that helps an AI complete a recurring type of work consistently.

The core loop is:

1. Understand the intended job and its boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements when appropriate.
5. Improve the skill based on evidence.
6. Repeat until the skill is useful, reliable, and not tailored only to its tests.
7. Optionally optimize the description that determines when the skill is used.
8. Package and hand off the finished skill.

Adapt the process to the user’s needs. Some users want a quick collaborative draft; others need comparison runs, formal checks, and several iterations. First determine where the user is in the loop, then help them take the next useful step. Do not require extensive testing when the user explicitly wants an exploratory or “good enough” draft, but explain what confidence is being traded away.

## Communication principles

Match the user’s technical vocabulary. Use plain English by default. Terms such as *evaluation* and *benchmark* are usually understandable, but define them briefly when useful. Do not use unexplained technical terms such as *JSON*, *schema*, or *assertion* unless the user signals familiarity or you explain them.

Ask questions because their answers change the design, not as a fixed questionnaire. For example:

- “What should a successful result look like: a chat response, a report, a file, or an action?”
- “Should the skill make a reasonable low-risk assumption when information is missing, or pause and ask?”
- “Which information sources are approved for this work?”
- “What errors would make the output unusable or risky?”

Keep the user involved at meaningful choices:

- Confirm the job before writing a large instruction set.
- Ask before imposing a restrictive scope, tool requirement, approval rule, or output format.
- Share proposed test cases before treating them as representative.
- Let human judgment lead when quality is subjective, such as tone, design, originality, or strategic usefulness.

When a task involves private communications, personnel records, customer information, health information, financial information, or other sensitive material, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and details. Exclude unrelated personal details, respect consent and privacy expectations, and keep outputs within the appropriate access boundary.

## 1. Identify the starting point

Classify the request before choosing the workflow.

### New skill

The user has an idea such as “make a skill that prepares weekly project updates.” Start with discovery, scope definition, and a first draft.

### Existing skill

The user has a skill they want to simplify, repair, extend, test, or optimize. Read the current instructions before proposing changes. Preserve its established name and identity unless the user asks to change them. If the installed copy cannot be edited, work from an editable copy and preserve the original until the revision is validated.

### Workflow demonstrated in conversation

The user may ask to “turn what we just did into a skill.” Extract what is already known from the conversation before asking repetitive questions:

- Inputs and source material used.
- Steps, decisions, and tool capabilities used.
- Corrections and preferences the user expressed.
- Output structure and acceptance criteria.
- Points where the workflow changed based on conditions.
- Assumptions that were safe in this instance but may not generalize.

Present the inferred workflow and its open questions for confirmation. Do not silently convert a one-time workaround or personal preference into a universal rule.

### Evaluation or optimization request

The user may have a complete-looking skill and ask whether it works. Go directly to test design, comparison, review, and revision. Do not rewrite an instruction set merely because rewriting is possible.

## 2. Capture intent, scope, and safety boundaries

Gather enough information to define a coherent job. Start with the answers most likely to affect the design.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Trigger:** What user requests, phrases, or contexts should cause the skill to be used?
3. **Inputs:** What information, files, systems, examples, and approved sources may it use?
4. **Outputs:** What should it produce, change, or communicate? Is a particular format required?
5. **Success criteria:** How will the user know the result is correct, useful, complete, or ready to use?
6. **Boundaries:** What should the skill not do? When should it ask, decline, or hand a decision back to the user?
7. **Variations:** What normal variants, difficult cases, and exceptions matter?
8. **Dependencies:** Are particular capabilities, templates, policies, reference materials, or permissions required?
9. **Testing level:** Does the user want a quick review, realistic test cases, objective checks, or a formal comparison?

For skills that access records about people, add these questions:

- What is the authorized purpose for accessing this information?
- Which sources and fields are necessary for that purpose?
- Who is allowed to receive the result?
- What details should be omitted, aggregated, or anonymized?
- Is human approval required before sharing, changing, or acting on the result?

For hiring, performance assessment, or similar decisions, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Do not make claims about people that go beyond the evidence or the authorized decision process.

### Research before drafting

If the environment provides user-approved documentation, existing skills, relevant templates, domain standards, or authoritative references, inspect them before drafting. Research should reduce the user’s burden, not substitute for the user’s authority over goals and constraints.

Use research to identify:

- Existing conventions and output standards.
- File, data, or system constraints.
- Similar reusable patterns.
- Required approvals, compliance rules, or privacy boundaries.
- Whether a proposed action is technically feasible.

If sources conflict or a requirement remains uncertain, state the uncertainty. Do not hide a guess inside a confident instruction.

## 3. Choose a maintainable skill structure

Keep each skill focused enough that a user and an AI can predict what it does. A single skill may support related variants, but separate unrelated jobs that have different source-of-truth rules, access needs, outputs, or definitions of completion.

A portable skill package commonly has this shape:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed guidance
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test cases and checks
```

Use progressive disclosure:

1. **Metadata or registration information:** Short name and description used to decide whether the skill applies.
2. **Core instructions:** The workflow needed for most invocations.
3. **Supporting resources:** Detailed references, scripts, templates, and domain variants loaded only when needed.

Keep the core instruction file readable. If it becomes too long, move detailed or specialized material into clearly named resources and state exactly when the AI should read them. Give large references a table of contents or clear navigation headings.

For skills with several technical or domain variants, use one selection workflow plus separate references by variant. The AI should identify the relevant variant and load only that material rather than treating every variant as required context.

### Bundle scripts only when justified

A script or deterministic helper is useful when repeated tests show the AI independently rebuilding the same procedure, such as validating data, generating a structured file, converting a format, or checking required fields. Bundle it when it is reusable, safer, and easier to verify than repeated free-form work.

Document each helper’s:

- Purpose and allowed use.
- Inputs and expected outputs.
- Preconditions and permission requirements.
- Failure behavior.
- Cases where the AI should use a different method.

Do not automate destructive, external, or permission-sensitive actions without clear user confirmation and appropriate safeguards.

## 4. Draft the skill instructions

Write in clear, direct, imperative language. Explain the reason for important rules, especially rules that prevent a predictable quality, safety, or authorization failure. A capable AI generally handles variation better when it understands the goal and tradeoff instead of receiving a long list of unexplained commands.

Include the following sections when applicable.

### Purpose and scope

State what the skill does, who it serves, and what is outside its scope. Clarify whether the skill produces advice, creates an artifact, modifies data, performs an external action, or guides the user through a decision.

### Inputs, sources, and prerequisites

List required inputs, permitted sources, necessary capabilities, and optional material. Explain what to do when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and the approved source material.
If a required source is unavailable, ask for an export or provide a draft clearly marked with the information that could not be verified.
```

For private or sensitive material, specify minimum necessary access and output handling. For example, instruct the AI to summarize only role-relevant evidence and omit unrelated personal information.

### Workflow and decision points

Describe the normal sequence of work and the conditions that change it. A durable sequence often looks like this:

1. Inspect the request, available inputs, and permissions.
2. Identify missing information that materially affects the result.
3. Ask focused questions or make a stated low-risk assumption, as appropriate.
4. Gather evidence from approved sources only.
5. Complete the task using the relevant method or variant.
6. Validate the output against requested format and success criteria.
7. Present the result with assumptions, evidence, and unresolved limitations.

Use conditional rules rather than trying to enumerate every situation:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite important work, create an irreversible external effect, or expose sensitive information, explain the impact and request confirmation before proceeding.
```

### Output format

When consistency matters, provide an exact or near-exact template.

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding and supporting evidence]

## Recommendations or next steps
1. [Action]

## Assumptions and open questions
- [Uncertainty, missing data, or decision needed]
```

Use flexible goals rather than rigid templates when adaptation is central to the task, such as creative work or context-dependent analysis.

### Quality, privacy, and safety checks

State what must be checked before completion. Useful checks include:

- Required sections, fields, or file properties are present.
- Calculations are validated against approved data.
- Important claims distinguish evidence from assumptions.
- Sources for consequential claims are identified when appropriate.
- Original data is preserved before transformation.
- Sensitive details are minimized and recipients are authorized.
- Uncertainty is visible rather than concealed.

A skill must not surprise the user by concealing actions, bypassing authorization, extracting confidential information, or attempting access beyond the user’s authority. If a request is unsafe, deceptive, outside the user’s authority, or cannot be verified responsibly, explain the limitation and offer a safe alternative where possible.

### Failure behavior

Give general recovery rules:

- **Missing or conflicting inputs:** Identify the gap and ask the smallest useful question.
- **Unavailable capability or reference:** Explain what cannot be verified and offer an alternative method or partial result.
- **Ambiguous request:** Make a clear low-risk assumption only when it will not materially change the result; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, flag it, or request guidance.
- **Irreversible or high-impact action:** Pause for confirmation before proceeding.
- **Sensitive information:** Limit collection and disclosure to what is necessary for the authorized purpose.

### Examples

Include a few short, generalized examples only when each teaches a distinct behavior. Examples should illustrate reasoning and output shape, not become narrow scripts for matching test prompts.

## 5. Write a description that triggers appropriately

The description is a routing instruction. It should say both what the skill does and when to use it. Include realistic contexts and phrasing that imply the task even if the user does not name the skill.

A good description contains:

- The outcome the skill helps achieve.
- Common request types or contexts where it applies.
- Important boundaries that prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a progress update, leadership summary, milestone review, risk overview, or next-step report, even if they do not use the phrase “status report.”
```

Keep the entire workflow out of the description. Avoid vague labels such as “help with documents,” and avoid making it so broad that it captures adjacent tasks better handled by another skill.

## 6. Audit the draft before testing

Read the draft as a first-time user and as the AI that must follow it. Check:

- Is the job clear and bounded?
- Does the description identify when to use the skill?
- Are inputs, source permissions, outputs, and completion criteria clear?
- Does the workflow explain important reasoning rather than merely issue commands?
- Does it handle missing information and validation failure?
- Does it avoid hidden assumptions about a particular person, organization, tool, access level, or local setup?
- Are private records handled only for an authorized purpose and with minimum necessary disclosure?
- Are there repeated rules, brittle wording, or unnecessary procedures?
- Does the AI have enough flexibility to handle ordinary variation?

Prefer lean instructions over a long list of commands that do not change behavior. Repeated capitalized absolutes are a warning sign unless the rule is a genuine safety, authorization, or integrity boundary.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user before running them and invite corrections or additions.

Each test case should record:

- A descriptive identifier.
- The prompt.
- Relevant files or context.
- Expected outcome in plain language.
- Objective checks, if appropriate.

A portable format is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates and identify information that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful categories, not merely different wording:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive, privacy-sensitive, or rule-sensitive request.
- A realistic exception that changes the workflow.
- A request requiring confirmation or a safe refusal, when relevant.

Avoid tests that simply repeat the skill’s own language. Vary wording, detail, and context. Use generalized scenarios and authorized or synthetic data rather than personal or confidential examples.

## 8. Run evaluations and comparisons

When independent execution is available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revised skill against the earlier version.

Start all comparable runs under similar conditions. When parallel execution is available, launch the skill-assisted and comparison runs for every test case at the same time. This reduces timing bias and prevents later baseline changes from distorting the comparison.

Organize results by iteration and descriptive test name:

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

For each run, retain the prompt, supplied files, resulting outputs, run configuration, and any available timing or resource data. Capture timing information as soon as the execution environment reports it, because some systems do not retain it later.

If independent agents, parallel runs, or a comparison environment are unavailable, conduct a transparent sanity check: apply the skill to each test prompt, save the outputs, and ask the user to review them. Do not represent this as a rigorous baseline experiment.

## 9. Define and grade objective checks

While runs are in progress, create objective checks where they genuinely help. Explain them to the user before treating them as measures of success.

Good checks are observable, specific, and tied to user value. Examples:

- Required sections are present.
- A produced file opens and contains required fields.
- Calculated values match an agreed source within a defined tolerance.
- The response identifies missing mandatory inputs.
- The output distinguishes evidence from assumptions.
- A required authorization or confirmation was requested before a consequential action.

Record each grade with stable fields for the check, outcome, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable information and requests the needed source."
    }
  ]
}
```

Use scripts for programmatic checks whenever practical. They are faster, more repeatable, and reusable across iterations. Do not force numerical checks onto subjective work. Tone, visual quality, strategic judgment, and creative usefulness often require human review; weak proxy metrics can cause a skill to optimize for a score rather than the user’s actual goal.

## 10. Review results with a human

Present outputs and measurements in a review format the user can access. If a review interface is available, use it to show each prompt, output, comparison output, grades, timing, and a place for feedback. If no interface is available, present the same material clearly in conversation or as downloadable files.

Ask focused review questions:

- Which output would you trust in normal use, and why?
- What was missing, misleading, unsafe, or difficult to use?
- Did the skill add work or detail that did not help?
- Did it appropriately identify uncertainty and preserve privacy boundaries?
- Would it work for similar requests with different wording or data?

For later iterations, show prior outputs and prior feedback alongside the new result when possible. Empty feedback usually means the user found that case acceptable, but it is not proof that the skill is generally solved.

## 11. Analyze results beyond pass rates

Aggregate available results: pass rates, time, resource use, variation, and per-test outcomes. Present the revised version before the comparison version for easier reading.

Then inspect patterns that averages can hide:

- **Non-discriminating checks:** Both versions pass, so the check does not reveal the skill’s value.
- **High variation:** Comparable runs differ substantially, suggesting ambiguity, instability, or weak instructions.
- **Tradeoffs:** Quality gains may cost too much time or effort.
- **Failure concentration:** Several failures may stem from one root issue, such as unclear source selection or output rules.
- **Unproductive work:** Execution traces reveal repeated planning, redundant research, or needless formatting.
- **Repeated reconstruction:** Several runs independently rebuild the same helper procedure, indicating that a reusable resource may be warranted.

A small evaluation set is evidence for the next revision, not conclusive proof of quality.

## 12. Improve without overfitting

Revise based on user feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from feedback. If one response fails to distinguish verified facts from uncertain claims, do not add a rule mentioning only that scenario. Clarify the broader principle: when sources are incomplete, mixed, or uncertain, separate supported findings from assumptions and unresolved questions.

Use these principles:

1. **Fix causes, not examples.** Build for future requests, not only current tests.
2. **Keep instructions lean.** Remove guidance that adds cost without improving results.
3. **Explain intent.** Connect important actions to quality, safety, clarity, or user control.
4. **Add reusable resources selectively.** Bundle templates, scripts, or references only when repeated work demonstrates their value.
5. **Preserve useful behavior.** Do not erase what users already value while fixing a defect.
6. **Expand test coverage gradually.** Add a test when it represents a meaningful class of failure.

After a revision, rerun the full test set in a new iteration. Use the same baseline policy unless there is a documented reason to change it. Continue until the user is satisfied, objective requirements are reliably met, feedback is consistently positive, or further revisions no longer produce meaningful improvement.

## 13. Optional blind comparison

When a decision between two versions needs stronger evidence, use blind comparison. Give an independent evaluator two outputs without revealing which version produced each one. Ask it to judge using a shared rubric, record the judgment, and only then reveal the mapping.

Use blind comparison when versions have similar scores but visibly different quality, when preference bias may be strong, or when the decision has material consequences. Judge against user-centered criteria: correctness, completeness, clarity, constraint adherence, safety, and practical usefulness. Analyze why the preferred output won before revising again.

## 14. Optimize triggering behavior after the workflow works

Only optimize the triggering description once the skill itself is useful. Create a balanced set of realistic requests that should trigger and difficult near-misses that should not.

Positive cases should vary across:

- Formal and casual wording.
- Direct and implied requests.
- Common and less common valid use cases.
- Situations where a related skill might compete but this one should apply.

Negative cases should be genuinely adjacent, not obviously irrelevant. They should share concepts or language with the skill but need another workflow, lack required conditions, or ask for explanation rather than task execution.

```json
[
  {
    "query": "Turn these approved team updates into a concise leadership summary with risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Explain what a status report is and when teams use one.",
    "should_trigger": false
  }
]
```

Review the query set with the user. If the environment supports repeated routing tests, divide cases into an improvement set and a held-out selection set. Test candidate descriptions more than once when routing can vary, and choose the description that performs best on held-out cases rather than merely fitting the examples used during editing.

Use substantive trigger queries. An AI may complete a simple one-step request directly without consulting a specialized skill even when the description matches. Test requests should therefore be complex enough that the skill would provide genuine value.

Show the user the before-and-after description and the observed results. Keep the final wording accurate about the skill’s real scope.

## 15. Package and hand off

Package the core instructions and only the resources required for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately represents activation conditions.
- Instructions do not depend on undeclared private conventions, local paths, personal access, or a particular vendor tool.
- Scripts and references are present, clearly named, and documented.
- No credentials, identifiers, confidential records, or sensitive examples remain.
- Privacy and authorization requirements are explicit where relevant.
- Test materials are retained only when safe and useful.
- The user can install, adapt, and test the package in their chosen environment.

Provide a short handoff note stating what the skill does, required capabilities, known limitations, how to test it, and any approval steps needed for consequential actions.

## Final readiness gate

A skill is ready when it has a clear job, a description that routes appropriate requests, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not mistake a long instruction file for a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for the user’s real recurring work.


---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using real screenshots plus programmatic layout checks. Fix and retest failures before reporting the change as complete.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. This is required even for a one-line spacing, background, or sizing edit: a local change can alter wrapping, height, overflow, alignment, or visible backgrounds elsewhere.

A single viewport is not sufficient. Bounding-box measurements alone are not sufficient. Real screenshots and numerical checks each find failures the other can miss.

## 1. Prepare a safe, realistic test state

Run the interface in an authorized test environment and populate the affected area with representative content. Use only data appropriate for that environment; do not expose private, unrelated, or sensitive personal information in screenshots or reports.

Include, when relevant:

- long paragraphs, formatted text, and long field values;
- representative cards, rows, lists, and item counts;
- validation messages and error states;
- loading, empty, and populated states;
- content near expected length or count limits.

Do not validate only an empty or unusually clean state. Sparse content often hides clipping, overlap, wrapping failures, and blank background regions.

## 2. Select the viewport sweep

Test these baseline viewport widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large width, such as 1920 px, for landing pages, dashboards, or interfaces expected on large displays.

When vertical layout can matter, test at least two heights at each relevant width:

- a short viewport, approximately 700 px high;
- a tall viewport, approximately 1400 px high.

Explicitly include a very tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, backgrounds, vertical padding, sticky footers, or bottom alignment. A narrow, short window and a narrow, tall window can expose different defects.

Also test any viewport known to be important for intended users or product requirements.

## 3. Capture real screenshots

Use a repeatable browser automation or testing system selected for the project. Run it in headless mode for consistent, repeatable capture. Capture:

- a visible-viewport screenshot when fixed, sticky, viewport-height, or bottom-alignment behavior matters;
- a full-page screenshot when page length, background continuity, or trailing space matters;
- screenshots for each relevant content state.

Inspect the changed area and its neighbors on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does this match the intended design now that the element's role or size has changed?

Be especially careful with full-bleed, edge-to-edge, or flush layouts. Removing horizontal containment can reveal wrapper margins, padding, or spacing rules as visible strips on another edge. Check every edge, not only the edge edited.

Reread the original requested outcome, then compare it directly with the screenshots. Do not accept a result merely because the implementation appears logically correct.

## 4. Run programmatic checks at each relevant viewport

Run numerical checks alongside visual review. Adapt selectors to the interface, but use concrete checks rather than relying on general impressions.

### Overflow and viewport-fit check

For screens intended to fit within the viewport, verify that document height does not exceed the viewport except for a small rendering tolerance:

```js
document.documentElement.scrollHeight <= window.innerHeight + 1
```

Also check for unintended horizontal overflow, for example by comparing document scroll width with viewport width. Do not apply the viewport-fit rule to pages intentionally designed to scroll.

### Geometry, overlap, and visibility checks

For changed elements and their relevant neighbors, compare `getBoundingClientRect()` values. Confirm that an element's bottom does not extend past the next element's intended top, unless their overlap is deliberate. Also confirm that controls remain inside their intended container and are not clipped or covered.

Verify, where applicable:

- no unintended horizontal scroll or overflow;
- no unintended vertical scrolling on fit-to-viewport screens;
- no unintended overlap with neighboring content, containers, or essential controls;
- buttons, links, inputs, and other controls are visible, reachable, and usable;
- fixed or sticky UI does not cover essential content;
- cards, lists, and controls remain within intended bounds.

### Prose-width check

For prose-heavy surfaces, measure line length using rendered paragraph width and computed font size. A simple approximation is:

```js
const paragraphs = document.querySelectorAll('article p, .prose p, main p');
const measures = [...paragraphs].map((p) => {
  const width = p.getBoundingClientRect().width;
  const fontSize = parseFloat(getComputedStyle(p).fontSize);
  return { width, fontSize, estimatedCharactersPerLine: width / (fontSize * 0.5) };
});
```

Flag paragraphs whose estimated measure exceeds about 80 characters per line. Reading-focused layouts commonly target roughly 60–70 characters per line. Treat this as a warning threshold and assess the actual typography and design intent.

## 5. Require both kinds of evidence

A viewport passes only when both of these pass:

1. **Visual evidence:** screenshots show no unintended blank strips, imbalance, clipping, bad wrapping, or layout defects.
2. **Programmatic evidence:** relevant overflow, bounds, overlap, visibility, and usability checks pass.

Numbers can miss visible background strips and awkward empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small geometry collisions.

## 6. Fix failures at the cause, then retest

If any viewport or content state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying layout behavior rather than adding a size-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the failing viewport.

If a change corrects one viewport but creates a problem at another, reconsider the diagnosis. The layout model is incomplete; do not continue layering patches until the symptom disappears.

## 7. Readiness gate

Do not report the UI work as complete until all of the following are true:

- [ ] Representative content and relevant states were tested.
- [ ] Baseline widths were tested, plus any required target widths.
- [ ] Short and tall heights were tested where vertical behavior matters.
- [ ] A very tall viewport was tested for viewport-height or bottom-layout changes.
- [ ] Screenshots were reviewed on all four sides of the affected area.
- [ ] Relevant programmatic checks passed, including the explicit viewport-fit check when applicable.
- [ ] Every discovered failure was fixed and retested.
- [ ] Screenshots and reports remain within the appropriate access boundary.

## 8. Report the evidence

Do not say only “works on mobile and desktop.” State what was actually tested, including omissions.

| Report item | Example |
|---|---|
| Completed sweep | Verified at 320, 480, 600, 720, 1024, and 1440 px. |
| Vertical coverage | Tested short and tall viewports where vertical layout matters; very tall viewport clean. |
| Checks | No unintended overflow or overlap; controls remain visible and usable. |
| Exception | [State any untested viewport, state, or known limitation clearly.] |

A concise completion report can read:

> Verified at 320, 480, 600, 720, 1024, and 1440 px with realistic content. Tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; very tall viewport is clean.

If any viewport or state remains unverified, say so clearly and do not represent the UI change as complete.


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

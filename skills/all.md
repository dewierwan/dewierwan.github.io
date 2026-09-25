# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate distinct options for a decision or problem, assess their tradeoffs honestly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when a user needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not to produce a long idea list. It is to surface genuinely different paths, make their tradeoffs clear, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources that the current environment can access, review them first.

If the question is not self-contained, look for a small number of high-value sources of context, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, or deadlines
- Stakeholder concerns and ownership boundaries
- Evidence about what has already been tried

Do not search broadly by default. Use targeted retrieval only when it could materially change the options. If important information is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The user’s wording may describe a symptom or requested solution rather than the real decision. For example, “Should we add a feature?” may really mean “How should we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip the pause only when the framing is obvious, low-stakes, or the user explicitly asks for an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes the process, incentives, scope, or problem framing
- At least one surprising option, such as delaying, partnering, removing scope, or doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when it is a real strategic choice, such as when observation, timing, or avoided distraction has value.

Give every option a short, memorable label that communicates its core approach. For each, provide:

- **What:** One or two sentences explaining the approach
- **Strengths:** One or two concrete advantages
- **Weaknesses:** One or two concrete disadvantages or failure risks
- **Effort:** Low, Medium, or High

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose evaluation criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, and stakeholder burden. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this user’s situation, constraints, and goals—not why it is generally attractive.
4. Name the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. The output should preserve meaningful choice.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may choose an option, request detail, reject the framing, ask for new options, or combine approaches. If they propose a hybrid, test whether the components are compatible and whether combining them solves a real tradeoff rather than adding complexity.

Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge or pre-mortem before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Move to a right-sized decision record: define the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After the decision is recorded, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Avoid skipping the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that the options are truly distinct, the framing reflects the actual decision, weaknesses are candid, effort labels are plausible, and recommendations follow the user’s criteria rather than the assistant’s default preferences.


---
name: pressure-test
description: Find weak points in a leading strategic idea before committing. Steelman the case, test its load-bearing assumptions through sequential challenge, and finish with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes an exercise in defending it.
- If the same topic was pressure-tested recently and no material evidence, assumption, or condition has changed, do not repeat the exercise. Use the existing findings to make the decision.
- If the review uses internal communications, customer records, personnel information, or other restricted material, confirm a legitimate purpose and authorization. Use only the minimum relevant sources, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive responses before moving on.
- Use available evidence such as research, metrics, prior experiments, customer feedback, documented decisions, and stakeholder input. Separate facts, inferences, and forecasts.
- Surface dissent through relevant roles, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent anyone's view.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intent. Include the action, expected result, mechanism, timeframe, and conditions required for success.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the strengthened restatement changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold. Rank them by the damage caused if they are wrong, beginning with the most consequential.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [How to test or disprove it] |

Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Choose questions based on the highest-risk assumptions, and adapt later questions to answers received. Do not present the whole list as a questionnaire, because that enables selective answering.

Use the categories below as needed:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that role say, and has the concern been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence; ask what observed behavior, data, comparison, or commitment supports the belief.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failures, external changes, and a wrong underlying premise when relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable signal] | [Check or accountable role] |

Warning signs must appear early enough to allow a change of course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap; do not treat silence as agreement.

Dissent is not an automatic veto. Its purpose is to reveal constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data-collection period. Next: run that test, then make the decision with the result recorded. Do not commit while the stated gap remains open.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, the downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with exactly one concrete next action: a verb, an owner, and a deadline when useful.

**Example:** `Research owner: interview five target users this week and compare the results with the adoption assumption.`

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

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and issuing a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make decisions with the right amount of rigor. The objective is not maximum analysis: it is to make a clear call when ready, preserve an accurate record for meaningful choices, and learn from outcomes.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **Record every non-trivial decision when a decision register is in use.** Reversible, hard-to-reverse, and direction-setting decisions should have a record, including decisions that remain open across several sessions. Do not create or update that record without the user’s explicit instruction or prior agreement to the recording practice.
3. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
4. **Separate advice from attribution.** Assistant recommendations belong in the conversation and must be labeled as assistant analysis. Add them to a decision record only if the user asks for that.
5. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution. Plan or perform the task instead of opening a decision process.
6. **Respect privacy and access boundaries.** Before searching shared records, communications, personnel material, customer information, or a shared decision register, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and omit unrelated sensitive details.

If a decision register is visible to others, confirm that its audience is appropriate before writing. For health, relationships, compensation, confidential personnel issues, or similarly sensitive topics, offer a private record in the user’s chosen secure location or keep the discussion in chat.

## 1. Choose the mode

Determine whether the work is new or continues an existing decision.

- **New:** No matching record exists, or the user requests a fresh decision.
- **Resume:** An open decision exists and the user wants to continue considering it.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review point and has not received an outcome assessment.

If the user explicitly names the mode, follow that instruction. Otherwise, only if authorized, search the available decision register for overlapping records before creating a duplicate.

For a resume, retrieve the existing record and append new information rather than rewriting history. For a review, use the original prediction and reasoning as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Write the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What is the deadline or decision trigger?
- What result is desired?
- What happens if no action is taken?

If the question is broad and credible options do not yet exist, generate options before evaluating them. Do not pressure-test a vague problem statement.

If there is only one viable path, say so directly: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time when needed. Put the decision in a bucket.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; create a light record if recording is authorized |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, consult relevant stakeholders, and record it |
| Direction-setting | Shapes strategy, culture, finances, or the operating model for an extended period | Full analysis, explicit dissent, prerequisite conversations, and a full record |

Use this test if classification is unclear: **What would it cost to unwind this?** Include money, time, trust, operational disruption, opportunity cost, and reputational effects. If the cost cannot be stated quickly or remains uncertain, the decision is probably larger than it first appears.

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: attention may cost more than an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. For each, state one major strength, one major weakness, and a rough effort or cost estimate.
3. Recommend an option and name the decisive reason.
4. If uncertainty is material, choose the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

A hard-to-reverse decision should be pressure-tested before commitment. A valid pressure test examines the leading option’s assumptions, disconfirming evidence, likely failure modes, strongest alternative, and major stakeholder objections.

If no relevant pressure test has occurred in the current work context, stop the commitment flow and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not continue merely because the user is in a hurry. Proceed only after the pressure test is complete or the user explicitly overrides it with a reason.

If the pressure test identifies a serious unresolved failure, do not force a decision. Return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check stakeholders: who has relevant expertise, bears consequences, or may reveal a constraint?
4. Give a recommendation, labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has happened, unless the user explicitly accepts and records a reason for proceeding without it. If it is being rushed, state which consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence in its favor.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies tradeoffs rather than disguising judgment.

Keep these categories distinct:

- **User’s stated view:** Only positions the user actually expressed.
- **Assistant analysis:** Recommendation and reasoning supplied by the assistant.
- **Open question:** Uncertainty not yet resolved.

If the user has not expressed a position, write “No position stated yet” or leave the user-position field blank. Never invent a lean, confidence level, rationale, response to dissent, or final choice for them.

## 6. Commit and record

Before finalizing, confirm:

- What is the decision?
- Which option was chosen?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable result is predicted?
- What is the user’s confidence in that prediction?

For meaningful decisions, make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Use the user’s chosen decision register, document system, or private file. A useful record contains status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. Use an **Open** status while deliberation continues. When a decision is made, mark it **Resolved**; for a binary question, record the answer, while for a non-binary question, record that a choice or direction was decided.

Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar, task system, or other reminder mechanism for high-stakes reviews when the user authorizes it.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** What it is and its central tradeoff.

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
By [date], [observable outcome] will happen or not happen.
Confidence: [X%]

## Worries
The most credible downside or failure mode.

## Retrospective
To be completed at review.
```

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until the user commits. When resuming, append a new dated thinking-log entry rather than rewriting history.

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not collapse a bad outcome into a bad decision process, or a good outcome into a sound process.

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

Use direct language. Challenge weak reasoning with evidence, but do not turn rigor into endless deliberation. Once the appropriate readiness gates have been met, name the decision and move forward.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, recommendation, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, or automation problem whose solution is not already obvious. Do not use it for a small fix, a routine task with a known implementation, or a request that only needs a direct factual answer.

By default, work from understanding through implementation and handoff. If the user asks for analysis only, stop after the recommendation and wait for a decision.

When reviewing private communications, records, or data about people, first confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and information, omit unrelated sensitive details, respect consent and privacy expectations, and keep findings within the appropriate access boundary.

## 1. Understand the problem

Start with the underlying problem, not the user’s first proposed solution. If they ask to “build X,” work backward:

- Who experiences the problem, and in what role or context?
- What are they trying to accomplish?
- What happens today?
- What workarounds exist?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the situation meaningfully better?

Write a concise problem statement and descriptive requirements. Describe desired outcomes, constraints, and evidence of success rather than assuming an implementation. If the proposed solution appears mismatched to the problem, say so directly and explain why.

Ask only for information that cannot reasonably be found in the available documentation, project context, authorized records, or system behavior.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, maintenance cost, and available alternatives. Include **do nothing**, **deprioritize**, or **improve the current workaround** as real options when the issue is rare, low-cost, or already adequately handled.

Distinguish between decisions that are easy to reverse and commitments that are expensive to undo:

- **Reversible decisions:** small, isolated choices that can be changed cheaply. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** public interfaces, persistent data changes, long-lived settings, migrations, security boundaries, external contracts, vendor commitments, or changes with broad compatibility effects. Pause and obtain an explicit decision before implementation. Record the rationale when useful.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in substantial design or implementation.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns, reusable components, and existing platform capabilities before inventing something new.

Understand relevant constraints, including compatibility expectations, deployment practices, ownership boundaries, security requirements, supported environments, monitoring, and maintenance capacity. Follow existing conventions unless there is a clear reason not to.

When research involves personal or confidential information, summarize only what is necessary to solve the stated problem. Do not expose private details merely because they were available.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve existing authentication, authorization, and data behavior.
- Must fit the available delivery time and maintenance capacity.
- Should avoid new dependencies, persistent settings, or external commitments.
- Must have a clear verification method.
- Must be removable or reversible if it fails.
- Must respect privacy, access controls, and applicable policy.

These criteria guide option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, training, or a capability already available in an existing platform.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For especially ambiguous problems, generate a wider candidate set before narrowing. Keep each option concise: what it is, what it solves, its main costs, and its key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that behave differently depending on runtime conditions.
- Validate inputs and states strictly. Fail visibly for invalid internal states rather than silently producing plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, public interfaces, and data structures as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where practical.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Avoid quick fixes that bypass the appropriate design boundary.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep proposals direct and short. Store durable proposals in the user’s chosen shared documentation system when review, editing, or a decision record is needed; otherwise provide the proposal in the current workspace. Use a clear date-prefixed title, such as `25 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, data or migration effects, rollback strategy, test strategy, deployment steps, and follow-up ownership.

Implement the approved solution using the project’s conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, security, and failure behavior.

Do not claim success based only on implementation. State what was actually tested, what passed or failed, and what remains unverified. Commit, publish, or deploy only according to the user’s repository, review, and release practices.

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
description: Learn a paper, article, post, or topic through a short Socratic dialogue that builds understanding, retention, and practical judgment through retrieval, explanation, and application rather than passive summary.
---

# Learn with a tutor

Help a learner understand, retain, evaluate, and use a provided paper, article, post, or topic through a rigorous, supportive dialogue. Prioritize active recall and reasoning over explanation: the learner should do most of the intellectual work, while the tutor guides attention, diagnoses gaps, and adjusts the challenge.

## Core learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to recall, explain, and reconstruct ideas in their own words.
- **Ask for mechanisms.** Move beyond stated conclusions. Ask why, how, under what conditions, and with what evidence an idea works.
- **Use learner-generated connections.** Ask for the learner's own examples, analogies, predictions, objections, and applications before offering them.
- **Create productive difficulty.** Make the task demanding enough to require thought, but not so difficult that the learner cannot make a meaningful attempt.
- **Practice transfer.** Move from the source material to unfamiliar cases, adjacent concepts, and real decisions.
- **Surface gaps through questions.** When an answer is incomplete, inconsistent, or mistaken, use focused questions to help the learner discover the tension. Explain directly only after a fair opportunity to reason.

## Purpose, authorization, and privacy boundaries

Use this workflow only for a legitimate learning purpose, such as studying material, preparing for a discussion, evaluating an argument, or learning a method. Work with material that the learner provided, is authorized to discuss, or can accurately describe from memory.

If the learning material includes private communications, records, or information about identifiable people:

- Confirm that the learner has a clear, legitimate purpose and appropriate authorization to use the material for learning.
- Use the minimum sources and details necessary for the stated learning goal.
- Do not request, repeat, infer, or preserve unrelated personal details.
- Avoid sensitive information unless it is necessary to understand the learning objective and the learner is authorized to share it.
- Respect relevant consent, confidentiality, privacy expectations, and access restrictions.
- Keep examples, explanations, notes, and summaries within the same appropriate access boundary as the original material. Do not turn restricted content into a broadly shareable output.
- When possible, replace identifying details with general roles, neutral descriptions, or hypothetical examples.

If these boundaries are unclear, ask the learner to use a non-sensitive excerpt, a redacted version, or a general description of the concept instead.

## Conversation workflow

### 1. Establish prior knowledge and a learning target

Begin by finding out what the learner already knows, believes, or has experienced. Also identify what they want to be able to explain, evaluate, remember, or do.

Ask one or two open questions, such as:

- “What do you already think is true about this topic, and what led you to that view?”
- “What are you hoping to be able to explain or do by the end of this conversation?”
- “What part of this material seems most important, confusing, or surprising so far?”

Use the response to estimate background knowledge, likely misconceptions, useful connections, and an appropriate level of challenge.

If the learner has not read or engaged with the material, ask for an initial prediction or working model. Then ask them to inspect a relevant portion before returning to retrieval practice.

### 2. Elicit the central idea from memory

Ask the learner to explain the main argument, finding, method, or idea without quoting the source.

Useful prompts include:

- “In your own words, what is the main claim or takeaway?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “If you had 30 seconds to explain this to a thoughtful friend, what would you say?”

Do not correct immediately. First establish whether the learner can distinguish the central claim from supporting details, examples, or conclusions the source does not support.

### 3. Select a few high-value ideas

Do not cover the entire source superficially. Select two or three ideas that are central, difficult, consequential, or likely to be misunderstood. Go deeply enough to test understanding rather than recognition.

For each idea, use this cycle:

1. Ask the learner to reconstruct the idea.
2. Probe the reasoning, assumptions, evidence, and causal or logical steps.
3. Ask for a self-generated example, analogy, or application.
4. Test the idea with an objection, boundary case, alternative explanation, or changed assumption.
5. Adjust the next question based on the learner's answer.

Keep turns short. Usually ask only one or two questions at a time.

## Question toolkit

Choose questions that require explanation rather than simple recognition. Adapt them to the source, the learner's goals, and their demonstrated level.

### Explain and reconstruct

- “What is the claim in your own words?”
- “What is the mechanism here, step by step?”
- “What problem does this solve, and why does the proposed solution address it?”
- “Which part is an observation, which part is an interpretation, and which part is a conclusion?”

### Test assumptions and evidence

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What evidence would distinguish this explanation from another one?”
- “Which assumption is doing the most work here?”
- “How would the conclusion change if that assumption changed?”

### Generate and transfer

- “Can you construct a concrete example from your experience or a familiar setting?”
- “Where else might this apply, and what would need to stay the same?”
- “Where might this fail or not apply?”
- “How does this connect to another idea or framework you know?”
- “What prediction would this idea make in a new situation?”

### Evaluate and communicate

- “What is the strongest objection to this argument?”
- “What surprised you, and what did you expect instead?”
- “What would a reasonable critic say?”
- “How would you explain this clearly without using the source's jargon?”

Avoid yes-or-no questions unless they are immediately followed by a request for reasoning.

## Responding to learner answers

Be warm, direct, and specific. Avoid generic praise. When an answer is strong, identify the feature that made it useful—for example, identifying an assumption, distinguishing correlation from causation, explaining a mechanism, or offering a relevant counterexample—then raise the level of challenge.

When an answer is incomplete or mistaken:

1. Do not immediately state the correction.
2. Identify the tension with one focused follow-up question.
3. Give the learner one or two genuine attempts to revise or reason further.
4. If they remain stuck, provide a concise explanation of the missing distinction, fact, or reasoning step.
5. Ask them to restate the corrected idea in their own words or apply it to a fresh case.

If the learner says, “I don't know,” invite a low-stakes attempt:

> “Take a guess based on what you do know. What seems most plausible, and why?”

Offer a hint after an attempt, or sooner when the task clearly requires knowledge the learner has not been given.

## Calibration and pacing

Increase difficulty when the learner answers easily. Ask for a counterexample, comparison, prediction, objection, or application in a new domain.

Reduce difficulty when the learner is lost. Narrow the question, isolate one assumption, use a simpler case, revisit a prerequisite concept, or ask them to compare two explanations and defend a choice.

Use the learner's energy as a pacing signal:

| Learner signal | Tutor response |
|---|---|
| Engaged and reasoning deeply | Pursue mechanisms, objections, and transfer in greater depth. |
| Answering accurately but briefly | Ask for evidence, assumptions, or a novel application. |
| Confused or overloaded | Simplify the task, consolidate one key distinction, and rebuild from there. |
| Tired or disengaging | Review demonstrated learning, ask for one practical takeaway, and close cleanly. |

Maintain a dialogue, not a fixed quiz. Every question should build on the learner's actual response.

## Progress checks

Periodically give a brief, evidence-based assessment. State:

- What the learner has demonstrated they understand.
- What remains uncertain, incomplete, or confused.
- The most useful next concept, distinction, or question to examine.

Do not claim mastery because the learner recognized a term or repeated a conclusion. Look for accurate explanation, defensible reasoning, and successful transfer to a new case.

A useful check-in format is:

> “You have shown that you can explain [idea] and connect it to [application]. The part still worth testing is [gap or assumption]. Let's examine [next question].”

## Closing gate

Before ending, ask the learner to convert learning into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for one final concise explanation, application, or future retrieval prompt. End by naming the next concept or question worth revisiting.

## Guardrails

- Do not summarize the material unless the learner explicitly requests a summary. Even then, first invite them to try their own summary.
- Do not lecture when a well-chosen question can prompt retrieval or inference.
- Do not define jargon automatically. Ask the learner to define it first, then clarify if needed.
- Do not make the interaction easy merely to be encouraging.
- Do not cover everything when a few core ideas can be understood deeply.
- Do not turn the conversation into a test with disconnected questions. Keep questions responsive and cumulative.
- Do not hide important corrections indefinitely. Once the learner has had a fair chance to reason, explain the missing point clearly and return the work to them through restatement or application.
- Do not expose sensitive or restricted source details in examples, feedback, or outputs beyond what is necessary for the authorized learning purpose.


---
name: write-in-my-voice
description: Draft email in the user's real voice while keeping facts, commitments, and tone appropriate. Use a style guide or recent sent messages as evidence, then audit voice and accuracy.
---

# Write in my voice

Use this workflow when drafting or replying to an email on the user's behalf.

## Goal

Write a copy-ready email that sounds like the user, not like a generic assistant. Preserve the user's usual level of warmth, directness, structure, and punctuation while adapting to the recipient, relationship, and stakes.

## 1. Gather voice evidence

Before drafting, read the user's current style guide in full, if one exists. Also use recent examples of emails the user actually sent, especially examples that are similar in audience or purpose.

Extract a practical voice profile:

- Typical greeting and sign-off.
- Formality level and relationship cues.
- Usual sentence and paragraph length.
- Preferred vocabulary, contractions, and degree of directness.
- Punctuation habits and formatting preferences.
- Words, phrases, punctuation, or tones to avoid.
- How the user makes requests, declines, follows up, apologizes, gives feedback, or expresses uncertainty.
- Approved reusable facts, links, boilerplate, and standard responses.

Recent edits and sent messages are stronger evidence than old examples or general writing advice. If the evidence conflicts, ask the user which preference is current, or use the most recent consistent pattern.

## 2. Confirm the email brief

Identify or ask for the minimum information needed to send a safe email:

1. Who is the recipient, and what is their relationship to the user?
2. What outcome should the email produce?
3. What facts, dates, links, attachments, names, or commitments must be included?
4. What level of warmth or firmness is appropriate?
5. Is there a deadline, sensitivity, or approval requirement?

Do not invent facts, availability, decisions, promises, prices, opinions, or emotional reactions. If a missing detail materially changes the meaning, ask a focused question rather than guessing.

## 3. Choose the right level of adaptation

Voice is not a fixed template. Adjust formality to the recipient and stakes without losing the user's recognizable style.

- For close working relationships, use the user's normal concise, familiar pattern.
- For new, senior, external, or sensitive recipients, retain the user's voice but use clearer context and more careful wording.
- For conflict, rejection, or correction, be direct and factual. Do not add defensive explanations, exaggerated praise, or unnecessary apologies.
- For requests, state the requested action, owner, and timing plainly.

Use approved standard wording or factual material when it fits. Do not reuse it when the context makes it misleading.

## 4. Draft the smallest complete email

Write only what helps the recipient understand and act. A useful default structure is:

1. Greeting, if the user's examples normally include one.
2. Purpose or response in the first sentence.
3. Essential context, decision, request, or next step.
4. Clear close and sign-off, if appropriate.

Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Put requests and decisions where they are easy to find. Use bullets only when they make actions, options, or logistics clearer.

Remove:

- Throat-clearing and process narration.
- Generic compliments or repeated thanks.
- Filler such as "just wanted to," "I hope you're well," or similar language unless it is genuinely part of the user's normal voice and useful here.
- Unnecessary hedging that weakens a clear message.
- Explanations of how the draft was produced.

## 5. Run a voice and safety audit

Review line by line before presenting the email. Ask:

- Would the user plausibly write these exact words?
- Does the greeting, closing, punctuation, and rhythm match the evidence?
- Is the tone right for this recipient and situation?
- Did the draft add a commitment, claim, opinion, or emotion the user did not provide?
- Are all names, dates, links, attachments, and references accurate?
- Is the requested action unmistakable?
- Can any sentence be removed without losing meaning or usefulness?
- Does the email avoid language the user has identified as undesirable?

If no style evidence exists, state the assumption briefly and use a broadly useful default: clear, warm-professional, concise, and direct. Invite the user to provide a few real examples or preferences for future drafts.

## Output format

Provide the final email as copy-ready text. If clarification is necessary, ask only the specific question needed to draft safely. Do not add commentary after the final copy unless the user asks for alternatives, rationale, or a revision.


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
description: Create an evidence-based, review-ready case study post about a person’s professional, learning, or career change, with verified story beats, hook options, quote-card choices, approval flags, and a readiness audit.
---

# Write a case study post

Use this workflow to turn raw material about a person into a concise public case study. It is designed for professional social posts, but it can be adapted for newsletters, community updates, recruitment pages, or program alumni stories.

The goal is not to make the person sound impressive through vague praise. The goal is to show a credible, specific change: where they started, what they did, what helped, what they do now, and what a reader can do next.

A strong case study lets the reader recognize their own situation in the subject’s before-state. It explains the mechanism of change without overstating causation.

## Inputs

Ask for all available source material. This can include:

- An interview transcript and meeting notes
- An application or intake form
- A professional profile or biography
- Public work samples, papers, projects, or announcements
- A message celebrating a result
- A prior draft, outline, or notes from the subject
- The target audience, publishing platform, and desired call to action
- Any established editorial or brand voice guide

Use this workflow only for a legitimate publishing purpose and with clear authorization to use the person’s information. Use the minimum relevant sources and facts. Do not expose unrelated personal details, confidential information, or material outside the intended audience and access boundary.

Before drafting, identify whether you have enough verified information for these fields:

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns, and consent status |
| Before-state | Previous role, field, goal, uncertainty, or constraint |
| Trigger | Why they joined, applied, changed direction, or took action |
| Intervention | Program, community, product, mentor, event, or resource involved |
| Mechanism | The concrete things that helped, such as a realization, introduction, job post, feedback session, or practical resource |
| Now-state | Current role, organization, team, project, output, or result |
| Timeline | Dates or time spans from starting point to outcome |
| Evidence | Verified roles, figures, dates, named work, and direct quotes |
| Cost or risk | Pay change, move, uncertainty, career change, or other tradeoff |
| CTA | What the reader should do next |

If critical facts are missing, ask focused questions before drafting. Do not guess at organization names, job titles, paper titles, dates, figures, timelines, or outcomes.

Useful questions include:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they decide to take part or make a change at that point?
4. What are the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a specific output, project, placement, publication, or result that can be named publicly?
8. Did they take on a meaningful cost or risk that they are comfortable sharing?
9. Which claims, figures, quotes, and names have been approved for public use?
10. Who should this post persuade or help?

## Evidence and verification rules

Never invent facts or strengthen a claim for dramatic effect. If the source says someone contributed to a project, do not call them the lead. If a source says they explored an opportunity, do not say they received it.

Treat transcripts as useful but fallible. Automated transcription can mishear names, organizations, technical terms, numbers, and titles. Cross-check important details against a primary or more reliable source, such as the subject’s approved profile, application, official announcement, published work, or direct confirmation.

When sources disagree, use this reliability order unless there is a reason not to:

1. The subject’s direct, recent confirmation
2. Official public records or published work
3. A current professional profile
4. An original application or written statement from the subject
5. Interview transcript notes or automated summaries
6. Informal third-party messages

Separate three kinds of statements in your working notes:

- **Verified fact:** A role, date, artifact, figure, or quote supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion you might draw from the story. Use only when the evidence supports it, and phrase it modestly.

Do not claim that a course, community, tool, or mentor caused the whole outcome unless the evidence clearly supports that claim. Prefer precise language such as “the program helped them see the field differently” or “they found the opportunity through the community.”

## Sensitive-content gate

Flag these items for explicit subject approval before publication:

- Salary, pay cuts, financial hardship, or compensation comparisons
- Health, family, immigration, legal, or personal circumstances
- Harsh language about a past employer, role, or career decision
- Unreleased work, confidential projects, or unpublished titles
- Direct quotations, especially strong opinions or criticisms
- Claims about why an employer hired the person
- Claims of causation or impact that cannot be independently verified
- Precise timelines that could reveal private circumstances

If approval is unavailable, use an honest fallback. For example, replace an exact compensation figure with “they accepted a lower-paying role” only if that broader statement is approved and still useful. Do not hide uncertainty by making the story more dramatic.

## Build the story beats

Create a private working outline before writing. Keep it concise.

### 1. Before-state

Capture the subject’s role, background, and the reader-relevant version of their uncertainty. Include what they were considering instead when that alternative mirrors the audience’s current life.

Keep only details that move the story. A long list of reading, credentials, or earlier roles usually weakens the post. Include a detail when it makes the change feel real or explains the subject’s decision.

### 2. Trigger

Identify why the subject acted at that moment. They may have wanted to learn about a new field, test whether a career path existed, find collaborators, solve a practical problem, or make a values-driven change.

### 3. Mechanism

Find the one or two concrete things that changed the trajectory. Strong mechanisms are observable:

- A realization that a field or role was accessible
- A relevant opportunity shared in a community
- A conversation that clarified next steps
- Feedback that improved an application or project
- A specific introduction, workshop, or resource

Avoid vague phrases such as “the experience was transformative.” State what happened instead.

### 4. Now-state

Record the current role, organization or team if approved, and what the person actually does. Translate technical jargon enough for the target audience to understand the work.

Use named outputs only when they add proof or interest. Do not pile up credentials. One meaningful project, publication, placement, product, or grant can do more work than a long resume list.

### 5. Timeline and compression

Map the sequence from joining or starting to the current result. Calculate a short, truthful timeframe when it sharpens the story, such as “within six months” or “the following year.” Do not force a compressed timeline if the facts do not support one.

### 6. Quotes

Pull three to five verbatim candidate quotes. Favor quotes that speak to the reader’s identity or uncertainty, not only the subject’s achievement.

Good quote categories are:

1. **Discovery:** “I did not know this path was open to someone like me.”
2. **Mechanism:** “I found the opportunity through the community.”
3. **Conviction:** “I would make the same choice again.”

Light trimming is allowed only when it preserves the exact meaning and grammar. Do not rewrite a quote into something the subject did not say.

## Generate three hook options

For feed-based platforms, the first two lines determine whether someone keeps reading. Write three distinct hooks before writing the full post. Keep each to two short sentences, usually under about 140 characters total where platform limits make that useful.

### Hook A: Discovery

Use when the audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a surprising concrete mechanism.

This is often the best default because it makes the reader think, “That might be me.”

### Hook B: Identity collision

Use when the before-and-after contrast is vivid and easy to understand.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This works well for broader audiences who may not share the subject’s exact blocker.

### Hook C: Stakes-led

Use only when a meaningful cost or risk is approved and the audience will read it as honest conviction rather than a warning.

**Formula:** The subject accepted a specific cost to do something. Now they are taking a concrete action or doing meaningful work.

Do not use a sacrifice hook if it implies that participation requires hardship or if it distracts from a more accessible message.

Choose one recommended hook. Briefly explain why it fits the target audience, and state why the other two are less suitable.

## Draft the post

Aim for roughly 160 to 220 words unless the platform or audience calls for another length. Shorter is usually stronger.

Use this sequence:

1. **Hook:** Use the recommended hook.
2. **Before-state:** One short paragraph showing the subject’s previous situation and a relevant alternative path.
3. **Name the intervention:** State clearly that they joined the program, used the resource, or entered the community. Do not leave the mechanism implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then land the immediate result in plain language.
5. **Current work:** Describe what they do now and why it matters in understandable terms.
6. **Optional honest cost:** Include only if approved and genuinely useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already carried by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

For external links on platforms that reduce reach for in-post links, place the link in a comment, profile page, or designated destination instead of the body. Make this a publishing choice, not an unverified universal rule.

## Style rules

Adapt to the chosen brand voice, but use these broadly useful defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use concrete names, roles, dates, and figures only when verified and approved.
- Use the subject’s first name after the first full introduction if that fits the publication’s tone and consent.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not call the subject exceptional, inspiring, or brilliant without showing why.
- Use contractions if the voice is conversational.
- Keep the CTA in full second person: “If you are…” and “you can…”
- Avoid emojis unless they are an explicit brand choice.
- Do not use em dashes. Use periods, commas, or line breaks instead.

Remove common machine-like phrasing on the final pass. Cut empty transitions, dramatic setup frames, filler intensifiers, hedge words, abstract nouns that replace evidence, balanced “on one hand/on the other hand” constructions, and reflective summary sentences after the CTA.

Avoid words such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm” unless they are necessary in a direct quote.

Read the post aloud. If it sounds like a generic thought-leadership template, shorten it and replace abstractions with facts.

## Graphic quote options

Provide three options for a visual quote card. Each should be self-contained, under 15 words when possible, and taken verbatim from approved source material.

Offer one quote from each category:

- Discovery
- Mechanism
- Conviction

Recommend one. Discovery quotes are often strongest because they work without surrounding context and reflect the reader’s possible uncertainty. Choose a mechanism or conviction quote instead only if it is clearer, more memorable, and understandable on its own.

## Readiness audit

Before sending the draft for review, check:

- Is there a legitimate purpose and clear authorization for this publication?
- Did you use only the minimum relevant personal information?
- Is every name, role, date, figure, and title verified?
- Are transcript-derived details cross-checked where needed?
- Does the post show a concrete mechanism, not just a result?
- Does it avoid overstating causation?
- Is the intervention named clearly?
- Does the opening mirror a real audience concern?
- Is the current work understandable to a non-specialist reader?
- Have sensitive claims and direct quotes been flagged for approval?
- Is the CTA clear and directed at the intended reader?
- Are there no em dashes, unsupported superlatives, corporate phrases, or generic filler?

## Delivery format

Create the draft in the user’s chosen document system if one is available. Use a clear title format such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and the two alternatives
- The three graphic quote options and recommendation
- A list of approval items
- A list of missing information that would strengthen the post
- The document location or link, if applicable

Do not treat the first draft as final. If feedback says “make the hook better,” generate new hooks rather than making tiny edits. If asked to make it shorter, cut secondary biography first while preserving the mechanism and outcome. If a subject rejects a sensitive line, replace it with the approved fallback without weakening the whole story.

After the final version is accepted, review the feedback for reusable lessons. Update the workflow only when a recurring pattern is clear, such as a missing intake question, a consistent voice preference, or a repeated verification issue. Do not invent process changes from a clean review cycle.


---
name: create-editorial-cover-images
description: Create cover images from an article through five distinct concepts, visual review, and three informed improvements using the chosen image generator.
---

# Create editorial cover images

Turn an article into eight finished cover-image options. Develop five distinct concepts, generate and inspect every result, then create three improvements based on what actually worked. The user chooses from finished images with a clear connection to the article.

Use the user's chosen image generator and publishing format. No particular medium, palette, account, or service is assumed. If the user explicitly requests prompts only, follow the prompt-only branch instead of generating images.

## Establish the brief

Read the complete article before developing concepts. A title alone is rarely enough to distinguish an image that belongs to this piece from a generic illustration of its topic. If the copy is missing, ask for it before generating.

Identify the article's central move: the idea or change in perspective the reader should take away. Notice its emotional progression, including where it becomes quieter, turns, or reaches its conclusion. Extract concrete images, actions, and metaphors already present in the writing. Note the tone, such as reflective, urgent, hopeful, sober, or celebratory, because it constrains the image's mood. Use this analysis to shape the work; do not begin with a lengthy summary unless requested.

Reuse preferences already supplied. Ask only for missing choices that materially change the output, keeping related questions together:

- **Mood:** Offer interpretations grounded in specific parts of this article. Explain which part each mood emphasizes, so the choice concerns the story rather than abstract adjectives.
- **Subject:** Explore a human figure, a landscape, a single symbolic object, or an abstract composition as appropriate. Respect explicit restrictions on people, settings, or representations.
- **Palette:** Offer a few palettes suited to the proposed moods. Describe their lightness, contrast, and character as well as naming colors, so choices do not depend on color labels alone.
- **Orientation:** Establish the intended placement and crop. A wide header, square preview, and portrait cover need different compositions. Use dimensions supplied by the user or verified for the destination; do not assume one publication's ratio suits another.

Also establish the medium or style, such as photography, drawing, painting, or collage, if the request leaves it open. The article and intended audience should guide the options. Do not turn one person's aesthetic into a universal default. Confirm the generator if it is not already clear. Collect outstanding answers before treating a partial reply as the full brief.

Keep a short working brief containing the agreed mood, subject restrictions, palette, medium, format, and generator. Carry it through both rounds without asking the same preference questions again.

## Propose five distinct concepts

Present exactly five ideas in a numbered list. Give each a short title, a one- to three-sentence description of what the viewer sees, and a brief explanation of the article's idea or emotional beat it expresses.

Vary subjects, compositions, and interpretations. Five changes to one scene do not provide a meaningful range. Unless subject restrictions rule them out, include at least one landscape-only option and one single-object or symbolic option. Check that each concept has a specific reason to belong to this article. Replace any concept whose explanation could accompany almost any article about the same topic.

Give a one-line initial recommendation, then generate all five without asking the user to choose first. The first round provides visible alternatives for comparison. Do not stop at concepts or written prompts when finished images were requested.

## Write useful visual prompts

Write one self-contained prompt per concept. Keep the visual direction specific enough to render while avoiding competing instructions. Use this structure, combining sections where that reduces repetition:

```
Create one image: [medium, format, and overall visual character].

Subject: [what is visible, its action, prominence, and position; place relevant exclusions alongside the description].

Setting: [surroundings, depth, and foreground or background relationships where useful].

Light and palette: [direction and quality of light, specific colors, contrast, and transitions].

Technique: [visible properties of the chosen medium, edge treatment, texture, detail level, and negative space].

Mood: [the intended feeling and its connection to the article's central idea].

Composition: [focal point, where the eye enters, placement of major shapes, requested dimensions or aspect ratio, and crop considerations].

Avoid: [only the artifacts, visual conventions, or content that conflict with this brief].
```

Name colors and their relationships instead of relying only on words such as warm or moody. For example, a pale ochre field against dark violet shadows describes a more concrete visual decision than dramatic lighting. Use examples to clarify the selected palette, not to impose a fixed palette on every article.

Explain the physical appearance of the chosen medium. A charcoal drawing might depend on broad tonal masses, broken edges, and visible paper; a photograph might depend on depth of field and the direction of natural light. Avoid incompatible technique instructions simply because they appeared in an earlier prompt.

Place exclusions beside the relevant positive instruction as well as in a final list when useful. If an anonymous figure matters, describe how anonymity is achieved. If the design requires empty space for later typography, specify where it belongs. Establish whether lettering is part of the brief, and avoid unintended text, logos, borders, or watermark-like artifacts.

Send the generator only the visual brief needed for the image. Do not paste the full unpublished article or unrelated personal details by default. Use article-specific facts only when supported by the copy and appropriate for the user's intended publication. A visual metaphor should not invent an event or imply a factual depiction the source does not support.

## Generate the first five

Use the chosen generator's supported workflow. Adapt the prompt format to its actual capabilities, and explicitly request an image so a text response is not mistaken for the deliverable. Respect existing access, spending, and approval boundaries. If the chosen service is unavailable, report the limitation and attempt safe recovery; agree on any replacement before sending content elsewhere.

Keep a working record of each option's number, title, concept, submitted prompt, generation status, output location, and review notes. Preserve the complete prompt so a truncated or failed submission can be repaired accurately. Start independent jobs concurrently only when the tool supports that safely and within its limits.

Confirm that every submission was accepted with the intended brief. Then confirm the actual image completed and can be opened at a useful size. An accepted request, elapsed time, placeholder, progress indicator, or text description does not establish completion. If an error appears, check whether an image already exists before retrying to avoid unnecessary duplicate work. Keep failed attempts separate from finished options.

## Inspect all five before improving

View every completed image at a useful size and evaluate the actual pixels. Do not evaluate only the generator's description or what you hoped the prompt would produce. Also inspect a small preview, because a cover must communicate when reduced or cropped.

For each image, record:

- Whether it communicates the article's central idea and emotional tone.
- Whether the subject and action read immediately, with a clear focal point.
- Whether the requested style, palette, orientation, and composition survived generation.
- Whether it feels too busy, generic, sentimental, static, or literal.
- Any visible anatomy, object, perspective, construction, or lettering artifacts.

Only after reviewing all five, design three new prompts. Tie each improvement to a visible observation: a strength to retain, a weakness to correct, and the change likely to help. Do not prewrite this round before seeing the first outputs.

A useful spread is one refinement of the strongest image, one combination of strengths from different images, and one new concept addressing a gap. Use judgment when a different spread would serve the article better. Each new image should contribute a meaningful alternative rather than another copy of an existing result.

Fix the cause of a weak result. If a composition is cluttered, reduce the number of objects or competing focal points before adding more instructions. If an image looks like a photograph with a painting filter, describe larger shapes, selective edges, and the medium's actual marks. If the scene resembles generic travel or office imagery, reconsider its action or metaphor instead of adding decoration.

Give a short progress update explaining what the first images revealed and what the next three will improve. Continue without requesting another selection or repeating the creative brief.

## Generate, review, and deliver options six through eight

Generate three new images from the revised prompts. Keep the first five intact so the user can compare originals with improvements. Inspect each new result using the same visual criteria and completion checks. Repair failed generation attempts where possible without counting them as finished options or substituting an old image.

Before delivery, verify that there are eight distinct, completed outputs that you personally inspected. Check that each can be opened from the final handoff and that titles and numbering match the working record. Use accessible files or verified output links supported by the chosen generator. Preserve the finished outputs for the user to compare.

Recommend the strongest rendered image in a short sentence explaining why it fits the article. Follow with a numbered list of all eight titles and their outputs, clearly identifying the final three as the second round. Keep the outputs as the final deliverable block. Avoid turning the handoff into a long design report.

If access, rate limits, or repeated generation errors prevent completion, state exactly which options are finished and which remain blocked. Preserve useful work for resuming. Do not claim eight images exist when some are only prompts or unsuccessful attempts.

After completion or selection, learn from explicit user feedback and observed results. When authorized to remember or update the workflow, save reusable lessons about interpreting articles, composition, prompt constraints, or verified generator conventions. Distinguish the user's stated preferences from your own aesthetic judgments. Do not turn one article's subject or a single successful image into a permanent default. Keep private article content out of reusable lessons, and make no update when nothing durable was learned. Report any saved lesson before the final deliverable block.

## Prompt-only branch

When the user explicitly wants prompts only, read the article and reuse or collect the same creative preferences. Propose five concepts, then wait for a selection unless the request already specifies concepts or asks for all prompts. Write each selected prompt in a separate fenced code block. If combining concepts, explain the combination in one line before the prompt.

Do not generate images in this branch. Do not describe hypothetical second-round prompts as improvements informed by visual review. Put the selected prompts last, with nothing after the final block.

## Adapt to another generator

When the user requests a version for another generator, preserve the concept, mood, composition, palette, and format. Change the prompt's structure or parameters only as needed by the target tool. A prose-oriented generator may suit a compact paragraph; another may accept short descriptive phrases and separate controls.

Check the target tool's supported conventions before specifying parameter flags or version identifiers. If the version matters and remains unclear, ask once rather than guessing. Keep each platform variant separate and clearly labeled. Changing generators should not quietly change the underlying creative idea.


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
description: Close one month honestly, then create a small, capacity-checked, explicitly approved plan for the next month using evidence, trade-offs, concrete commitments, and appropriately bounded records.
---

# Review and plan a month

Use this workflow at a month boundary to review the month ending and create an executable, month-level plan for the month ahead. A complete session usually takes 45–75 minutes: roughly half for evidence and review, and roughly half for planning.

Review and planning belong in one session. The structural cause of a missed commitment, energy drain, or delivery problem should directly shape the structure of the new plan.

## Purpose

This workflow produces:

- An evidence-based account of the review month.
- A direct verdict on progress toward active long-range goals and any in-scope training, health, or personal-practice commitment.
- A compact picture of completed work and selected life signals, such as focus, sleep, energy, or recovery.
- A written **Review** for the ending month.
- A written **Plan** for the new month, with a named theme, no more than three outcomes, explicit trade-offs, capacity evidence, and a pre-mortem.

Gather, discuss, and save only information that supports these outputs. Do not turn a monthly review into a broad life history, task dump, or retrospective transcript.

## When to run it

Run this workflow when the user asks for a monthly review, asks to plan a named month, or asks to close one month and start another.

Use these defaults unless the user names a range:

- During the first three days of a month, review the prior calendar month and plan the current month.
- Later in a month, review the current month to date and plan the next month. Clearly state that the review is partial and how much time remains.
- For a forward-planning request, review first because the evidence should shape the plan. The user may explicitly choose to skip the review.

State the ranges before proceeding:

> Reviewing **March 2026** (01 Mar–31 Mar). Planning **April 2026**.

Ask whether “the month” means calendar dates or a practical range that includes an overlapping partial week. Record the actual planning range in the plan.

## Privacy, authorization, and record boundaries

Use calendars, journals, health records, task records, project records, or communications only for a legitimate planning purpose and with clear authorization. Read the minimum relevant sources, fields, and date range.

- Summarize patterns and constraints rather than exposing unrelated event details.
- Prefer paraphrase over quotations from private notes or communications. Quote only when authorized and necessary to establish a material pattern.
- Do not place sensitive health, journal, family, financial, or relationship details in a record that could have a broader audience.
- Do not include unnecessary details about other people. Record only role-relevant commitments, owners, dependencies, and deadlines.
- If a source is unavailable, incomplete, or outside the permitted access boundary, say so. Never imply it was checked.
- When producing a shared plan, use the least sensitive wording that still preserves the decision. For example, write “unavailable for a personal commitment” rather than details that are not needed for planning.

## Operating rules

1. **Read first; discuss second.** Show the evidence picture before reflective questions.
2. **Batch independent reads.** Gather independent evidence in one initial pass rather than repeatedly interrupting the conversation with small lookups.
3. **Use live commitments.** Assess against the user’s current target, not an obsolete schedule, old scope, or stale goal record.
4. **Check data quality before a harsh verdict.** Missing syncs, delayed logs, incomplete records, and inconsistent sources can distort conclusions.
5. **The user chooses.** The assistant calculates, summarizes, identifies constraints, and asks hard questions; the user chooses priorities, cuts, and commitments.
6. **One decision at a time.** Do not move to the next planning decision until the current question has a real answer.
7. **Stay at month altitude.** Plan outcomes, milestones, capacity, and structure. Leave detailed weekly task blocks to a weekly planning workflow.
8. **No saved plan without explicit approval.** Brainstorms, dictated notes, imported tasks, and earlier drafts are candidate inputs, not confirmed decisions.
9. **Use explicit dates.** Use **DD MMM** unless the user prefers another unambiguous format.
10. **Do not overwrite silently.** Show and resolve a material conflict with an existing plan before saving.
11. **Do not lecture.** For training, health, or recovery, provide the evidence, direct conclusion, and agreed commitment. Offer specialist guidance only when requested and appropriate.

## Step 1: Determine the range and gather evidence

Determine the review month, comparison month, and planning month. Then gather available evidence in one initial batch.

Use sources the user has chosen and authorized, such as a project tracker, task manager, calendar, spreadsheet, notes collection, training log, health tracker, or user-provided facts. If no source is connected, ask for a short factual inventory rather than broad background.

| Evidence area | Gather in the initial pass |
|---|---|
| Previous monthly record | Theme, promised outcomes, commitments, and prior review findings |
| Weekly records | Plans and reviews in the review range; repeated blockers, milestones, and carried work |
| Goals | Active weekly, monthly, quarterly, and annual goals; status, deadlines, and notes |
| Work delivered | Completed tasks, decisions, projects, or deliverables, grouped into useful domains |
| Calendar | Next-month fixed deadlines, travel or leave, recurring commitments, and meeting-heavy weeks |
| Daily signals | User-selected ratings, focus time, habits, or brief note themes |
| Sleep and recovery | Optional sleep duration, quality, and same-source recovery trends |
| Training or practice | Optional sessions for the review and comparison months, plus the current commitment |

For large sources, return computed statistics and a few relevant themes rather than raw entries. Filter long journals and event lists to the requested period. If delegated analysis is available, give it a narrow, authorized brief: analyze only the necessary range, return a concise planning summary, and omit raw sensitive material.

A calendar summary should capture fixed multi-day blocks, approximate meeting load by week, important recurring commitments, protected personal time, and planning anomalies such as events during unavailable time. Describe personal events only as broadly as needed.

Before detailed planning, check weekly plans overlapping the beginning of the planning range. Reference and reconcile their commitments with the monthly plan; do not duplicate or overwrite them.

## Step 2: Show the evidence picture

Present a compact factual picture before asking the user to interpret it. Use direct language and numbers where useful.

### Training, health, or personal-practice verdict

If the user has an active commitment in this area, include it unless they explicitly put it out of scope. Compare actual activity with the live target. Depending on the domain, calculate:

- Total volume, sessions, repetitions, or practice instances.
- Average weekly volume and number of active days.
- Completion of key sessions or milestones.
- Longest gap between sessions.
- Relevant balance, performance, or recovery measures.
- Change from the comparison month.

Use this taxonomy when it fits:

- **ON TRACK:** Key measures meet at least 90% of target and consistency is intact.
- **BEHIND:** A key measure is roughly 60–90% of target, or there was a meaningful consistency break.
- **OFF TRACK:** A key measure is below 60% of target or there was a prolonged gap.
- **AT RISK:** A safety, injury, burnout, or sustained-decline signal makes the commitment unsafe or unlikely.

Adjust thresholds only when the domain requires it, and state the adjustment. If tracking may be incomplete, ask: “The record shows this. Does that match reality?” before making a strong judgment.

State one biggest corrective action for the new month. It must be a concrete commitment, not a full programme.

### Goals and delivery

Summarize weekly commitments as completed, missed, deferred, or rolled forward. For every active long-range goal, state whether it **advanced**, **stalled**, or **regressed**, with one short reason. Explicitly identify goals that received no meaningful attention.

Also summarize completed work in a few useful domains. The question is whether effort created intended progress, not whether every completed task can be listed.

### Life signals

Include only measures the user chooses to track. Useful measures include rating distribution and average, focused hours, low-focus days, sleep duration, sleep quality, recovery trends from a consistent source, and repeated themes in notes.

Flag meaningful patterns: repeated short sleep, several consecutive low-rating days, extended low-focus periods, or a mismatch between positive ratings and notes describing strain. Averages are not complete truth; raise contradictions briefly and directly.

## Step 3: Reflect on the month

Open with one specific observation grounded in the evidence. Ask one question at a time and pursue no more than two or three threads unless the user wants depth.

Cover these decisions:

1. What genuinely shipped and feels like a win?
2. What cost more time or energy than it returned?
3. Was the main miss structural, circumstantial, or a genuine priority change?
4. What one behavior, boundary, or pattern must change next month?
5. If a personal practice is in scope, what is the concrete next-month commitment?

Useful prompts include:

- “This outcome slipped across several weeks. What made it structurally difficult?”
- “The ratings were stable, but the notes suggest strain. What was driving that?”
- “This goal moved while the others did not. What conditions made that possible?”

For a time-constrained session, complete the in-scope practice verdict, any material wellbeing flags, one structural fix, and one concrete next-month commitment.

## Step 4: Plan the new month

A plan is not a description of events plus optimistic targets. A real plan contains a defined outcome, honest baseline, path, proof of capacity, trade-offs, forcing functions, a pre-mortem, and explicit approval.

### Move 1: Define outcomes

For each candidate priority, ask:

> What specifically is true by the final day of this planning range?

Make the answer measurable or plainly verifiable. Limit the plan to three outcomes; one or two is usually better. Connect each outcome to a long-range goal or an explicitly chosen responsibility.

### Move 2: Establish current state

Size the gap with evidence, not mood. Inspect the relevant draft, pipeline, milestone, backlog, baseline metric, or equivalent domain reality. Gather missing evidence before designing the path if the gap is unclear.

### Move 3: Work backward to build a path

For each outcome, identify three to six moves by reasoning backward from the due date. Each move needs a date or window, an owner, and completion evidence.

> For this to be true by the end date, what must be true halfway through? What must happen before that?

### Move 4: Do capacity math

Estimate usable focused capacity honestly:

> available working days × recently observed focused hours per day

Account for fixed commitments, travel, leave, meeting-heavy weeks, and essential operational work. Compare supply with the effort implied by the paths. If demand exceeds supply, cut, defer, reduce scope, or assign genuine help now.

### Move 5: Make the NOT-doing list

Ask:

> What will explicitly not happen this month so these outcomes can?

The user names the cuts. A plan without genuine cuts is a wish.

### Move 6: Add forcing functions and protective structure

Fragile outcomes need an external forcing function: a stakeholder expecting a deliverable on a date, a booked review, a public commitment, or a downstream owner waiting on the work.

Protect interruption-sensitive work. Batch flexible work around meetings and reserve the best available blocks for work that needs depth. If calendar conflicts undermine protected time, add resolving them as an immediate action.

### Move 7: Run a pre-mortem

Ask:

> It is the final day of the month and this plan failed. What happened?

The user answers first. Record the top two or three failure modes and a specific counter for each.

### Move 8: Get sign-off

Read the full plan back in ten lines or fewer. The user must be able to state the theme and main outcomes from memory, then explicitly approve it.

> Is this the plan?

If approval is vague, revise. Do not save yet.

## Required plan structure

```markdown
## THEME: [MEMORABLE, ACTION-ORIENTED LINE]

**Planning range:** [DD MMM–DD MMM].

## Shape of the month
[Fixed events, heavy weeks, effective working weeks, and immediate post-month constraints.]

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
[Behavior, boundary, or environment change that counters last month’s drain; include delegated-but-tracked work and owners.]

## Personal or training commitment
[Specific measurable commitment, if in scope.]

## Pre-mortem
- Failure mode: [likely cause]. Counter: [specific response.]
```

## Step 5: Save the review and plan

After explicit sign-off, save two records in the user’s chosen system:

1. A **Review** attached to the ending month.
2. A **Plan** attached to the new month.

Create a missing monthly record if the chosen system supports it. Use one final write operation when possible. Keep sensitive material out of records with a broader audience. If an existing plan differs materially, resolve the difference with the user before replacing it.

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

At the end of every run, capture one precise improvement to the reusable workflow, template, or source mapping in a user-approved durable location. If no suitable location exists, present the improvement as a short rule the user can save later.

Look for a noisy read, wrong data assumption, misleading metric, user correction, or repeatable pattern. Prefer one exact edit over a vague reminder. For example: “Use completed-work dates rather than due dates when measuring monthly delivery.”

## Audit checks

Before finishing, verify:

- Review and planning ranges are explicit.
- Private sources were used only for a legitimate purpose, with authorization and appropriate scope.
- Evidence appeared before reflective prompts.
- Strong verdicts account for known data-quality limits.
- The plan has a named theme and no more than three outcomes.
- Each outcome has a test of done, date, path, owner, and forcing function.
- Capacity demand fits supply, or an explicit scope decision was made.
- The NOT-doing list contains genuine cuts.
- The structural fix responds to a reviewed drain.
- Overlapping weekly plans were checked and reconciled.
- In-scope personal commitments are specific.
- The pre-mortem includes counters.
- The user explicitly approved the plan before it was saved.
- Saved records remain within their intended access boundary.

## Common failure modes

- Starting with prompts rather than evidence.
- Judging performance against stale targets or incomplete tracking.
- Confusing a list of events with a plan.
- Overloading capacity and refusing to cut scope.
- Letting the assistant choose priorities or treating brainstorming as commitment.
- Saving an unapproved draft or silently overwriting an existing plan.
- Duplicating or conflicting with a weekly plan.
- Treating wellbeing averages as more truthful than repeated written evidence.
- Applying generic productivity rituals instead of addressing the actual drain.
- Pulling detailed private material into a shared planning record when a concise summary would suffice.


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

A separate daily-review practice and next-day planning practice should happen earlier in the evening. This workflow can work without any app, database, calendar, or particular device.

## Purpose and design rules

Every step should serve at least one of these functions:

1. **Reduce stimulation.** Lower bright light, screen use, active conversation, and problem-solving.
2. **Increase reliability.** Make it harder to drift into scrolling, work, or new decisions.
3. **Prepare the body and morning.** Complete small practical actions that reduce avoidable friction after waking.

Consistency matters more than complexity. Use a similar sequence on most nights. Keep the active ritual short enough that it does not become another task to avoid. A typical active ritual takes about 20–30 minutes, excluding time asleep.

Choose an intended in-bed time with the user in advance, or use a reasonable default. Work backward from that time. Preserve enough time for the environment gate, essential physical preparation, and a short settling practice. Do not fill the remaining bedtime window with expanded planning or reflection.

## Interaction rules

- Be quiet, direct, and low-stimulation. Use short prompts with no coaching language, jokes, emojis, or sleep-science lecture.
- Give one small group of actions at a time. Do not turn the ritual into a long conversation.
- For checklists, use plain bullet lists rather than interactive checkboxes. End each list with: **Reply “done” when all set.**
- Do not ask the user about tomorrow after the wind-down has started. Do not ask for priorities, intentions, goals, wins, or backup to-do lists.
- Do not reopen journaling, reflection, planning, messages, task systems, or calendars during the ritual.
- If the user raises a work problem, worry, or task, do not solve it. Say: **“Put a brief note somewhere safe for tomorrow. Do not work on it tonight.”**
- If the user is clearly exhausted, let them skip optional preparation steps. Do not skip the environment and distraction-control gate unless a safety, health, accessibility, caregiving, or urgent practical need makes it unsuitable.
- After the final close message, stop. Do not summarize what was completed, offer more help, create a follow-up prompt, or simulate another turn.

## Readiness check

Before beginning, establish only what is needed. Do not inspect messages, news, social feeds, task lists, private notes, or other attention-grabbing sources.

If the assistant can use records, calendars, or prior-session context, it must have a legitimate purpose and clear authorization. Read only the minimum information needed, such as whether a review was completed or whether an early fixed commitment affects morning device access. Do not read private journal content merely to verify completion, and do not expose unrelated personal details.

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

If a small missing item creates a worry, capture it in one designated location without solving it. For example: “Buy breakfast item.” Do not search for alternatives, open shopping tools, message someone, or start a planning conversation. If using a personal record, write only the minimum necessary note and only with authorization. Say only:

> Noted. Captured for later.

## Step 4: Brief settling practice

Offer one familiar, low-stimulation practice. Do not teach a new or complex exercise at bedtime.

Default prompt:

> 5 min meditation.

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

> Get out of bed. Keep the room dim and do a boring, screen-free activity for about 20 minutes, or until sleepy. Return to bed when sleepy. Do not check the time.

Suitable activities include reading on paper, folding laundry slowly, or another neutral task. Avoid work, emotionally engaging reading, exercise, food preparation, screens, and clock-checking. The goal is to keep the bed associated with sleep rather than wakeful frustration.

For recurring, severe, or safety-relevant sleep difficulty, encourage appropriate medical or sleep-care support.

## Routine audit and adaptation

Review the workflow after a run only if doing so will not re-engage the user at bedtime. This should normally happen later, during a suitable daytime review, or silently within an authorized workflow configuration process. Make changes based on observable friction, not novelty. Do not invent improvements after a clean run.

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
description: Gather authorized, relevant context; clarify the intended outcome before committing to an agenda; and create a practical meeting brief with a timed agenda, decision-focused questions, and a clear follow-up plan for consequential meetings.
---

# Prepare for a meeting

Use this workflow to prepare for a consequential meeting, a calendar-preparation session, or a meeting where the user needs a focused agenda. The deliverable is a durable meeting-preparation record in the user’s chosen workspace, plus a concise situation brief and targeted questions before the agenda is finalized.

Do not treat background research as the final deliverable. The preparation is complete only when the agreed meeting record has been created or updated, subject to the user’s access permissions and chosen system.

## Principles

- Research only for a legitimate meeting purpose and only from sources the user is authorized to access.
- Use the minimum relevant information. Do not copy unrelated personal details, confidential material, or sensitive information into a broadly visible meeting record.
- Read the substantive artifact when a document, proposal, deck, memo, or draft is the reason for the meeting. Do not create generic questions about a document that is available but unread.
- Separate verified facts, reported views, open questions, and assumptions.
- Ask the user about goals and constraints before finalizing the agenda when their choices could materially change it.
- Design the agenda around decisions, learning, or relationship outcomes—not around a chronological retelling of prior correspondence.
- Keep shared meeting pages appropriate for their audience. In particular, omit compensation figures, private personnel information, credentials, and other restricted information. Use neutral references such as “offer follow-up” or “commercial terms discussion” where necessary.

## Inputs and scope

Collect or confirm the following:

| Input | Default if not specified | Why it matters |
|---|---|---|
| Date or event | The next relevant meeting | Identifies the invitation and deadline |
| Meetings to prepare | External 1:1s and small working meetings | Avoids preparing routine blocks or personal holds |
| Meeting duration | The invitation duration | Sets realistic agenda timing |
| Output location | User’s selected workspace or meeting-record system | Ensures the preparation is durable and accessible |
| Access boundary | Sources the user is authorized to use | Protects privacy and confidentiality |
| Meeting type | Informational, decision, negotiation, recruiting, feedback, or relationship-building | Determines the brief and agenda shape |

Exclude obvious non-meetings unless the user explicitly includes them: personal holds, focus time, travel blocks, routine administrative blocks, and internal events without a preparation need.

If several meetings are in scope, process them one at a time when their context or goals differ. Batch the initial event collection and basic research where practical, but do not blend relationship histories or confidential details between meetings.

## Step 1: Read the meeting invitation carefully

Collect the meeting title, date and time, duration, participants, organization or affiliation where known, location or video details, description, links, and scheduling context. Look for clues about why the meeting exists:

- An introduction from a mutual contact.
- A follow-up from an event, prior call, or written exchange.
- A request for feedback, advice, approval, partnership, or support.
- A live decision, deadline, competing option, or required next step.
- A linked proposal, deck, memo, draft, or shared workspace item.

Do not infer that a meeting is routine merely because the title is generic. A short description, recent message, or attendee change may reveal a more consequential purpose.

## Step 2: Gather relevant context

Use only authorized sources and prioritize recency, directness, and relevance. Typical sources include the user’s correspondence, internal discussion channels, prior meeting notes, calendar history, approved contact records, and public professional information.

For each external participant, gather enough information to answer these questions:

1. **Who are they?** Their current role, organization, relevant background, and public professional links where useful.
2. **What is their organization or work?** What it does, its current priorities if known, and its relationship to the user’s organization or objective.
3. **What is the relationship history?** Earlier meetings, direct exchanges, introductions, promises, decisions, and unresolved questions.
4. **Why is this meeting happening now?** Identify the scheduling trigger or most likely immediate reason.
5. **What has changed recently?** Relevant announcements, publications, transactions, role changes, or recent correspondence.
6. **What materials matter?** Identify linked or referenced artifacts that should be read before preparation.

### Recommended source checks

Use the sources that are available and appropriate; do not require any particular product or search tool.

- **Direct correspondence:** Review recent messages sent to or from the person. Look for commitments, prior questions, scheduling context, and tone.
- **Name and organization mentions:** Search for messages or notes that mention the person or organization without including them directly. This can reveal introductions, prior evaluations, historical context, or why a meeting was arranged.
- **Internal conversation history:** Search approved team channels or records for relevant decisions, prior interactions, and ownership. Do not reproduce unrelated internal discussion.
- **Prior meeting records:** Find earlier meetings with the attendee and summarize the relationship arc, not only the latest interaction.
- **Calendar history:** Confirm whether this is a first meeting, a recurring meeting, or a continuation of a specific thread.
- **Public research:** Use public sources to verify role, organization, relevant work, recent news, publications, or public statements. Prefer primary sources and stable professional profiles over speculation.

For sensitive meetings, such as hiring, performance, legal, medical, financial, or personal matters, use a narrower source set. Include only details that are necessary for the user’s legitimate purpose and suitable for the intended record audience.

## Step 3: Read the artifact the meeting is about

This step is mandatory when the meeting centers on a written artifact such as a proposal, pitch deck, strategy document, memo, draft agreement, research paper, or planning document.

Signals include phrases such as “feedback on the draft,” “review the proposal,” “comments on the deck,” “the memo we discussed,” or “consult about the plan,” as well as links in invitations or recent messages.

1. Open the artifact through an authorized route.
2. Read the complete relevant content, including sections, tabs, appendices, and comments that materially affect the discussion.
3. Identify the central claim, requested decision, assumptions, alternatives, risks, dependencies, and unclear points.
4. Anchor the later questions and agenda in specific substance.

If the context implies an artifact exists but it cannot be found or accessed, ask the user for the link or a summary before creating a detailed agenda. Do not pretend to have pressure-tested a document that was not available.

## Step 4: Identify meetings that need a specialized workflow

Before drafting a general meeting brief, check whether the meeting is a reference conversation, formal assessment, legal matter, performance review, incident review, or another meeting governed by a specialized process.

For example, a reference conversation may involve a person who can speak to an applicant’s prior work. If so, switch to the organization’s authorized reference-check workflow rather than using a generic relationship agenda. That process should focus on role-relevant capabilities, concrete evidence, consent and authorization, structured questions, and whether the reference can distinguish relevant performance. Keep the record within the appropriate hiring access boundary.

Carry forward relevant research rather than repeating it, but do not copy sensitive information into a general meeting page.

## Step 5: Write and share a situation brief before asking questions

After research is complete, give the user a brief that lets them rapidly reload the situation. Do this before proposing the final goal or agenda. The user may know constraints, history, or intent that the records do not show.

Choose a shape that fits the meeting.

### Narrative brief

Use for most meetings. It should be readable in about a minute and include:

- Who the participant is and why they matter.
- Where the relationship stands.
- Why the meeting is occurring now.
- The key tensions, decisions, or unknowns.

### Decision-shaped brief

Use for negotiations, recruiting, sales, fundraising, partnership discussions, or other meetings with a live decision. Include:

- Their likely ask or desired outcome.
- Their alternatives, incentives, and known deadlines.
- The user’s position, leverage, and constraints.
- Main risks and open unknowns.
- What must be true for a successful close.

These formats can be combined: begin with a short narrative, then add a compact decision section. For data-heavy discussions, a facts table followed by dynamics and unknowns may be clearer.

Do not ask the user to choose a format unless the choice itself is consequential and genuinely unclear. Select the format that best supports the upcoming decision.

## Step 6: Ask targeted questions

Ask focused questions after the situation brief and before drafting the final agenda. Do not ask the user to invent an agenda; ask for choices that determine its purpose, tone, and risks.

Always cover the primary outcome and at least one of: the major failure mode, preferred tone, or concrete ask. Always include a final catch-all question.

Useful question axes include:

- **Primary outcome:** What should be different by the end of the meeting?
- **Their situation:** Is there uncertainty about their role, interest, authority, timing, or decision process?
- **Sensitive substance:** Should the user state their view early, ask for the other party’s view first, or avoid a topic?
- **Failure mode:** What would make the meeting go poorly—overselling, under-asking, losing trust, focusing on the wrong issue, or leaving without a next step?
- **Specific ask:** Is the user seeking an introduction, decision, commitment, advice, approval, information, or follow-up? How direct should the ask be?
- **Anything else:** What context, constraints, or outcomes should be added or avoided?

Use two to six substantive questions. If the answers to early questions change later options, ask in rounds: first ask about outcome and authority; then tailor questions about closing, follow-up, or tone based on the answers.

Make answer choices fast to respond to and auditable. Number every question continuously and label every option with the matching question number and a letter. Offer mutually exclusive choices when possible, while including a “both” option when two actions can sensibly coexist.

Example:

```markdown
1. What is the primary outcome?
   - **1a (recommended):** Diagnose their priorities and agree a concrete next step.
   - **1b:** Build the relationship without seeking a commitment.
   - **1c:** Make a direct proposal and seek a decision.

2. What should the close optimize for?
   - **2a (recommended):** Set a date-bound follow-up with a named owner.
   - **2b:** Offer a useful resource or introduction first.
   - **2c:** Keep the close open and gather more information.

3. Is there anything else to land or avoid?
   - **3a:** Nothing to add.
   - **3b:** I will add notes or constraints.
   - **3c:** There is sensitive context to discuss privately.
```

Before sending, verify that every question has a number, every option has one unique matching label, labels are sequential, and the catch-all question is present.

You may skip questions only when the meeting purpose, user objective, boundaries, and recurring agenda are genuinely established and current. When uncertain, ask: a short clarification round is usually less costly than an agenda based on a wrong assumption.

## Step 7: Create or update the meeting record

Once the user has answered, create a meeting record in the user’s chosen workspace. If no workspace is available, produce the same structure as portable Markdown and ask the user where it should be stored.

Use the event date as a date-only field unless the user explicitly needs time-based tracking. Give the page a clear title such as the date plus participant or topic. Add attendees only when the system’s permissions and data model support it.

Use this structure:

```markdown
# [Date] — [Participant or meeting topic]

## Context

- Who the participant is and their relevant role.
- Relationship history and important prior commitments.
- Why this meeting is happening now.
- Links to authorized, relevant background material.
- Whether this is a first meeting or a continuing relationship.

## Goal

[The agreed outcome, written as a practical result rather than a vague intention.]

## Agenda

### 0–5 min: Open and frame

**Say**

[Brief opening, context, or transition.]

**Interviewer note**

[What to avoid, clarify, or establish early.]

### 5–20 min: Diagnose [topic]

**Questions**

1. [Decision-relevant question.]
2. [Question that tests a key assumption.]

**Interviewer note**

[Signals to listen for and what must be learned.]

### 20–35 min: Discuss, test, or propose [topic]

**Say**

[Transition and concise framing.]

**Questions**

1. [Question or proposal that moves the conversation forward.]

**Interviewer note**

[How to respond to likely concerns or ambiguity.]

### 35–45 min: Close and create momentum

**Questions**

1. [Specific next-step, owner, artifact, or date question.]

**Interviewer note**

[Backup close if the preferred outcome is not possible.]

## Five most important questions to ask

1. [Most decision-relevant question.]
2. [Key diagnostic question.]
3. [Question that tests the central assumption or gap.]
4. [Question that identifies constraints or decision process.]
5. [Specific forcing-function close.]

## Timely note

[Optional recent development or relevant point to mention.]
```

Adapt timing to the actual meeting duration. Put the most important topic before general updates. For shorter meetings, use fewer stages; for longer working sessions, add decision checkpoints or breaks. The time allocations should add up to the scheduled duration.

The five-question section is an in-meeting cheat sheet. Rank questions by decision relevance, keep each to one line, and include a concrete closing question when the meeting needs a next step. Do not turn it into a second full agenda.

## Step 8: Quality and privacy audit

Before finalizing, check the record against this list:

| Check | Pass condition |
|---|---|
| Purpose | The meeting goal reflects the user’s answers, not an unsupported assumption. |
| Evidence | Context distinguishes facts, reported views, and unresolved questions. |
| Artifact use | Any central proposal, memo, or deck has been read or explicitly marked unavailable. |
| Timing | Agenda stages fit the actual duration and prioritize the critical issue. |
| Questions | The five key questions are ranked, specific, and include the needed close where applicable. |
| Privacy | The record omits unrelated personal data, restricted details, and compensation figures. |
| Access | Sources and outputs remain within authorized access and sharing boundaries. |
| Next step | The close identifies an owner, artifact, date, or clear reason not to commit yet. |

Correct any failure before marking the preparation complete.

## Step 9: Plan the post-meeting follow-up when appropriate

For high-stakes meetings intended to move a decision—such as a negotiation, recruiting conversation, proposal discussion, partnership conversation, or sales process—schedule or create a reminder for a short post-call review, usually about an hour after the meeting ends.

The review should use the authorized transcript or notes, the preparation record, and the organization’s approved coaching or review format. Capture:

- What happened versus the intended goal.
- Decisions, commitments, objections, and unanswered questions.
- Evidence of what worked and what did not.
- The next action, owner, and deadline.
- Any recurring communication or execution pattern, recorded carefully and with evidence.

Do not schedule this review for purely informational meetings unless the user requests it. Do not rely on unavailable recording tools; use the meeting notes or a manual reminder as the fallback.

## Common failure modes

- **Research without a usable record:** Context was gathered but no durable meeting page or portable brief was created.
- **Generic agenda despite a specific artifact:** A proposal existed but was not read, producing shallow questions.
- **Assumed objective:** The agenda was drafted before the user confirmed the desired outcome or boundaries.
- **Context dump:** The brief contains many facts but does not identify the live decision, tension, or unknown.
- **Weak close:** The meeting ends with “let’s stay in touch” instead of a named next step, owner, artifact, or date.
- **Overloaded agenda:** More topics are scheduled than the meeting can support; reduce scope and prioritize.
- **Unsafe recordkeeping:** Sensitive information, compensation figures, or unrelated personal details are added to a shared page.
- **Unclear provenance:** Opinions or secondhand claims are presented as facts. Label them or verify them.

A strong meeting preparation record helps the user enter the conversation informed, aligned on purpose, ready to listen for the right evidence, and able to close with an appropriate next step.


---
name: capture-meeting-actions
description: Review meeting records, identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only questions that require judgment.
---

# Capture meeting actions

Turn meeting records into reliable post-meeting follow-up tasks. Use this as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose and operating rules

Before each run, remember these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text**: strongest evidence of who agreed to do what and when.
2. **Human-written notes**: useful supporting evidence, especially explicit action sections.
3. **Automated summary**: useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda**: describes intended discussion, not a commitment.

Automated summaries often misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels it as an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work that was completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, a statement of interest, or an open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply known delegation boundaries supplied by the user or organization. Attendance at a meeting does not make the user accountable for all work in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this broadly useful default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect:

- Title, date, and time
- Meeting-record link or identifier
- Attendees, if available
- Transcript, notes, summary, and relevant linked context

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
dates, why this matters, the commitment, and any necessary sensitivity.]

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

Do not turn one-off facts into permanent rules. Small additions to an examples or patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing steps or changing the evidence order. Briefly report any reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links to its source record.
- Message drafts are ready to send and follow the user’s preferences.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report the essential outcome only: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and any reusable guidance changes. Keep status updates terse and factual.


---
name: turn-a-message-into-a-task
description: Read the full conversation, work out the real action, do useful preparation, and create a clear task only when needed.
---

# Turn a message into a task

Use this when a conversation contains a request or follow-up that may need a
task record.

## 1. Read the whole conversation

Open the parent message and all replies. Identify the people involved, the
actual request, promises already made, deadlines, links, and whether someone has
already completed the work.

## 2. Work out the real action

Rewrite the request as an outcome. Separate the user's action from work owned by
other people. If the message can be answered or resolved immediately, do that
instead of creating a task for its own sake.

## 3. Gather enough context

Check relevant documents, prior conversations, meeting notes, records, or public
sources when they can answer factual questions. Match research effort to the
stakes. Do not delay a simple task with an exhaustive search.

## 4. Do useful preparation

When authorized, draft the reply, assemble the figures, outline the document,
or prepare the decision before creating the record. Keep actions that affect
other people in draft form until the user approves them.

## 5. Decide whether a record helps

Create a task when work remains, it may be forgotten, or another commitment
depends on it. Skip the record when the action is complete, trivial, duplicated,
or better owned elsewhere.

## 6. Create a useful task

Use a clear title, binary finish line, relevant context, source link, owner, and
real deadline. Avoid copying a whole conversation into the notes. Verify the
record after writing it.


---
name: design-a-work-sample
description: Create or improve a short, paid, asynchronous work sample that produces job-relevant evidence, can be scored consistently, and is validated through realistic simulated submissions.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A strong work sample asks candidates to complete a realistic, bounded version of the job, produces evidence beyond polished generalities, and gives reviewers enough evidence to make a consistent decision.

Use it for a new exercise or a revision. Do not use it for an interview-question set, an application-form screener, a live assessment center, or a multi-day work trial. If the request could mean one of these formats, ask which format is needed before proceeding.

## Purpose and design principles

A work sample usually sits after initial application review and before later interviews. Its purpose is narrow: determine whether a candidate can demonstrate the few capabilities that matter most in this role under realistic constraints.

Do not try to assess the whole person or every part of the job in a short asynchronous exercise. Other stages usually provide better evidence for different questions:

- Interviews can assess live communication, motivation, collaboration, and conversational reasoning.
- References can assess reliability, integrity, and sustained performance over time.
- A later trial can assess work quality across several days, adaptability in real systems, and consistency.
- Training can often close gaps in a specific tool, internal process, or domain vocabulary.

The work sample should focus on three to five load-bearing capabilities that are important to the role and observable in the exercise window. Examples include prioritization, practical judgment, clear writing, diagnosis, sourcing, execution, systems thinking, and turning ambiguity into useful work.

Use these default constraints unless the hiring owner deliberately chooses otherwise:

- Make the exercise paid.
- Set a clear expected time limit, commonly two to four hours.
- Use a realistic but fictionalized or safely anonymized scenario.
- Keep assessment time to roughly 20 to 25 minutes per submission.
- Make the task self-contained. Candidates should not require internal-system access, private data, unavailable stakeholders, or proprietary tools.
- State the policy on AI tools clearly. Evaluate judgment and usefulness, rather than trying to infer tool use from writing style.
- Do not ask candidates to produce work the organization will use commercially unless that use is separately agreed and compensated.
- Test capabilities that are material to the role. Do not test protected characteristics, unrelated personal circumstances, or weak proxies for them.
- Offer a route for reasonable accommodations or an equivalent accessible format while preserving the role-relevant standard.

When the design process uses internal hiring materials or records about people, use them only for a legitimate hiring purpose and with clear authorization. Read the minimum relevant material, omit unrelated or sensitive details, and keep drafts, simulations, reviewer guidance, and candidate materials inside the approved hiring access boundary.

## Step 1: Pre-flight

Before designing the exercise, confirm that the hiring team has both of the following:

1. A current job description or role brief explaining responsibilities, level, expected outcomes, reporting context, and major constraints.
2. A role-success profile, hiring plan, or equivalent document identifying the capabilities and experience most likely to produce the required outcomes.

If either item is missing, stop. Do not attempt to define the role-success profile while drafting the test. That creates a moving target and usually produces an exercise that sounds credible while measuring the wrong things.

Use this request format:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

Once both exist, read the full role context. This may include linked project notes, expected operating conditions, examples of strong work, prior hiring feedback, and existing exercises for comparable roles. Read one or two reference exercises only to calibrate tone, length, and operational format. Do not copy a familiar task shape automatically. Different roles need different evidence.

Give a brief status update before moving on. For example:

> Read the role brief, hiring plan, and two reference exercises. Moving to the alignment memo.

## Step 2: Write the alignment memo before drafting

Do not write candidate-facing instructions yet. First produce a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five abilities that the role succeeds or fails on and that can be surfaced in the exercise window. Phrase them as observable capabilities rather than broad virtues.

Weak: “Strategic thinking.”

Better: “Can identify the highest-leverage problem in a messy operating situation, explain the tradeoff, and deliver a useful first action.”

### What the exercise will not test

Name important criteria that belong in other stages. This keeps the exercise honest and prevents it from becoming an unrealistic proxy for the entire job.

For example, a three-hour written exercise may not fairly test long-term reliability, leadership over months, responsiveness in live meetings, specialized software fluency, or working relationships with a manager.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level. Explain how this changes the exercise.

- Entry-level candidates may need more context and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make tradeoffs, establish direction, and create an artifact another person could use without further explanation.

### Role-relevant failure modes to catch

Identify two or three plausible work patterns that could otherwise look strong in conventional hiring but would create problems in this role. Describe observable behavior, not a type of person.

Examples include:

- A polished planner who does not ship usable work.
- A fast executor who misses the central problem or creates avoidable risk.
- A careful candidate who defers every meaningful decision when the role requires judgment under uncertainty.
- A technically capable candidate who cannot communicate for the intended audience.

### What strong looks like

Write one short paragraph describing a top submission. Focus on the evidence: what it notices, what choices it makes, what it produces, and how it handles uncertainty.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the owner explicitly confirms or revises the memo.

## Step 3: Propose exercise shapes

Once the memo is approved, offer three possible exercise shapes. Each option must test the load-bearing capabilities in a distinct way, be understandable within about a minute, be self-contained, and be scorable quickly.

For each option, include:

- **Shape:** A plain-language description of the task.
- **What it tests:** The specific load-bearing capabilities it reveals.
- **Why it is evaluable:** The evidence reviewers will see and why it can be assessed consistently.
- **Main risk:** The most likely source of noise, unfairness, or poor signal.

Keep each option concise, usually no more than about 150 words. Useful shapes include:

- **Triage pile:** The candidate receives a realistic set of messages, requests, and constraints. They prioritize, draft responses or work products, and recommend one systemic improvement. This suits operations, coordination, support, and communications-heavy roles.
- **Choose the highest-leverage action and ship it:** The candidate receives a brief with several possible priorities, selects one, explains the choice, and creates a small usable output. This suits strategic operations and builder roles.
- **Diagnose and fix:** The candidate reviews a messy situation, identifies the key problem, and ships one targeted intervention. This suits product, program, analytical, and process-improvement roles.
- **Source and pitch:** The candidate defines a target profile, identifies promising channels or prospects from supplied information, and drafts outreach. This suits recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** The candidate assesses a defined intervention area using supplied evidence and makes a recommendation for a decision-maker. This suits research, policy, strategy, and specialist roles.
- **Design a repeatable system:** The candidate creates a lightweight process, playbook, or operating artifact that a teammate could use. This suits program, community, enablement, and operational-design roles.

Do not draft the full exercise until the hiring owner chooses a shape. If none fit, generate three more from the approved capabilities rather than forcing a familiar format.

## Step 4: Draft version 1

Write the candidate-facing exercise in this order.

## [Role] Work Sample

This work sample assesses your ability to [two or three observable capability verbs].

You have **[time limit]** total.

**Your mission**

Describe a specific situation rather than an abstract assignment. Provide enough context to make the work realistic. If decisiveness is part of the assessment, state which stakeholders are unavailable during the exercise so candidates must make reasonable calls instead of deferring every decision.

End with one sentence that restates what the candidate will produce.

**Deliverables**

List two to four parts with rough time guidance where useful. A common operations pattern is:

- A short prioritization or analysis section.
- Several actual drafts, decisions, or shipped outputs.
- One systemic fix, process improvement, or reusable artifact.

Avoid excessive micro-tasks. A few substantive outputs reveal more than dozens of shallow decisions. If both planning and execution matter, explicitly tell candidates not to spend all their time planning.

**Context**

Provide the minimum information needed to complete the exercise: project state, intended audience, constraints, available resources, relevant policies, and stakeholder availability. Use fictional names and identifiers unless the hiring owner has approved use of real public information.

For a triage-pile exercise, include roughly eight to ten realistic items. Some items should connect so candidates are rewarded for seeing patterns across the whole situation. Include reference notes with any information needed to make a fair decision, such as escalation rules, capacity limits, or refund policy.

**Instructions**

Include the following:

- The expected time limit.
- A clear submission deadline.
- The submission format, such as one document or PDF, plus links to supplementary artifacts if needed.
- The payment amount, payment process, and any early-submission bonus if offered.
- The policy on tools and AI assistance.
- A request to document important assumptions briefly.
- Permission to submit incomplete work if time runs out.
- Optional guidance on a short walkthrough video if it would add useful signal.

Use a transparent AI policy. For example:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

Use a transparent payment policy. Choose compensation based on applicable law, expected time, seniority, candidate burden, and the organization’s hiring budget. State whether payment is fixed, whether a timely-submission bonus is available, and how candidates request payment. Do not make payment contingent on quality or hiring outcome.

**Anticipated questions**

Include answers to common questions:

- *I am unclear about a requirement. What should I do?* Make a reasonable assumption and state it briefly.
- *What if I do not finish within the expected time?* Submit what you have and note what you would do next.
- *How will my work be used?* It will be used only to evaluate candidates for this position unless another use is agreed separately.
- *What if I need an accommodation or an alternative format?* Contact the hiring team through the stated hiring channel before beginning, where possible. The team will discuss an equivalent accessible format.

## Candidate-facing writing and format checks

Write in direct, plain language. Use the locale and spelling conventions appropriate to the candidate audience. Keep instructions easy to paste into the organization’s chosen hiring system and easy to read in a document.

Before sharing a draft, check that the candidate-facing text:

- Uses simple headings and bullets.
- Has no tables if the destination system renders tables poorly.
- Avoids horizontal divider lines if they break the destination editor.
- Avoids generic slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.
- Uses complete phrasing such as “by the end of Tuesday,” rather than abbreviated phrasing.
- Uses clearly fictional names and contact identifiers in fictional scenarios.
- Formats multi-line message metadata clearly. If the target editor collapses line breaks, use its supported soft-break method.
- Does not include credentials, private contact details, sensitive internal data, or confidential personal information.

After every draft, add a separate section that is not for candidates:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets identifying choices the owner may want to change. Useful notes include whether a scenario item is too obvious, whether the scenario is realistic enough, whether payment matches the exercise burden, whether a deliverable is too prescriptive, or whether a walkthrough video should be optional.

End with one focused decision question, such as:

> Which part should we tighten first?

## Step 5: Iterate with the hiring owner

Expect multiple rounds of feedback. For each revision, provide the complete updated work sample rather than only a change list, so it can be copied directly into the selected system.

Apply feedback directly unless it would materially undermine assessment validity, accessibility, fairness, privacy, or safety. If that happens, state the concern once in plain language, offer an alternative, and let the hiring owner decide.

Common revision directions include tightening vague instructions, loosening over-prescriptive tasks, correcting scenario facts, simplifying deliverables, changing payment, replacing unrealistic details, and changing formatting for the delivery system.

## Step 6: Simulate two candidates

Before declaring version 1 complete, simulate two full submissions in parallel using the exact candidate-facing instructions.

### Role-aligned simulation

Use a persona that matches the approved role-success profile. Have them complete the actual deliverables under the stated time limit. Ask for a short reflection on their choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest, capable candidate who could pass ordinary screening but whose demonstrated work lacks one capability central to this role. Choose a relevant mismatch, such as a planner where the role needs a builder, a cautious hedger where it needs decisive judgment, or an executor who cannot see systemic patterns. Keep the difference tied to job evidence, never identity, background, or protected characteristics.

Have this persona produce the same complete submission shape.

Then synthesize the results:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both candidates performed similarly.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by likely impact.

Floor checks that both candidates pass are not automatically bad. The concern is when a central capability produces no meaningful difference in evidence.

## Step 7: Apply validation improvements

Revise the complete exercise based on the simulation. Address the weakest diagnostic points first. Useful revisions may include:

- Making scenario items more interdependent.
- Removing obvious noise that takes seconds to dismiss.
- Adding a concrete constraint that forces a meaningful tradeoff.
- Replacing a broad opinion prompt with a usable deliverable.
- Clarifying reviewer guidance so it rewards the intended evidence.
- Removing specialized knowledge requirements that are trainable and not essential at the start of the role.

Do not make the task harder merely to make it more selective. Make it more diagnostic of the approved capabilities.

## Step 8: Optional external review

If other reviewers provide feedback, assess each suggestion against the approved alignment memo. State which suggestions to integrate, which to skip, and why. External review is evidence, not an automatic instruction. The hiring owner remains accountable for the assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The role description and role-success profile are confirmed.
- The alignment memo is approved.
- The chosen task shape maps directly to the load-bearing capabilities.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and does not require private access.
- Payment, accommodation, and submission instructions are clear.
- Candidate-facing text is formatted for the destination system.
- A reviewer can assess a submission in roughly 20 to 25 minutes.
- A role-aligned and plausible role-misaligned simulation has been completed.
- The simulation led to any necessary revisions.
- The final version contains no unnecessary sensitive data and does not create unpaid production work.
- Role-relevant criteria, accessibility needs, privacy expectations, and potential proxy bias have been checked.

## Common failure modes

Avoid these patterns:

- Designing the task before agreeing what it should measure.
- Testing tool familiarity, domain trivia, or trainable knowledge instead of durable judgment.
- Asking for too many small outputs instead of a few meaningful ones.
- Making every scenario item independent, which tests volume but not pattern recognition.
- Allowing candidates to defer every decision to an available stakeholder when decisiveness is meant to matter.
- Giving vague context that rewards insider knowledge.
- Setting word-count guidance that encourages padding.
- Creating a test that takes longer to grade than the signal justifies.
- Treating polished writing or presentation as the main signal when the role requires something else.
- Using private communications, records, or real identities in a scenario when fictionalized details would provide the same assessment value.
- Declaring success without checking whether the exercise distinguishes the role-relevant evidence it was designed to measure.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, useful for assessment, respectful of candidate time, and clear about what good performance looks like.


---
name: run-a-reference-call
description: Prepare, conduct, and document a hiring reference call that gathers role-relevant, concrete evidence while protecting privacy and supporting a fair hiring decision.
---

# Run a reference call

Use this workflow when an authorized hiring team needs to speak with a candidate-provided or otherwise appropriately sourced professional referee. Its purpose is to test role-relevant evidence, resolve specific hiring uncertainties, and create a useful internal record—not to collect vague praise or unrelated personal information.

## Scope and authorization gate

Before researching or contacting anyone, confirm all of the following:

- The organization has a legitimate hiring purpose for the reference check.
- The candidate has provided the referee or has otherwise been informed and consented where required by law, policy, or reasonable privacy expectations.
- You are authorized to access the relevant hiring records and internal communications.
- The planned questions concern job-related capabilities, working relationships, performance evidence, and support needs.
- You will use only the minimum relevant information and keep notes within the approved hiring-access boundary.

Do not use a reference call to investigate protected characteristics, health, family circumstances, political or religious beliefs, private conduct unrelated to work, or rumors. Do not seek information that the referee is not permitted to share.

## Inputs

Collect or confirm:

- Candidate name and the role under consideration.
- Referee name, contact details, organization, and relationship to the candidate.
- Call date, time, format, and meeting link if applicable.
- Current hiring stage and decision timeline.
- Role outcomes, key capabilities, and unresolved questions from the selection process.
- Candidate-provided professional links or work samples, if relevant.
- Other planned or completed references, if available.

If essential inputs are missing, ask for them or mark the gap clearly. Do not invent relationship details, prior feedback, or hiring-stage information.

## 1. Find and verify the call

Search the organization’s approved calendar and scheduling records for the referee’s name or contact details. Record the meeting title, scheduled time, attendees, format, and any relevant scheduling context.

If no event exists, continue preparation using the information available, but mark the call as unscheduled or awaiting confirmation. Do not create calendar events, send messages, or contact the referee unless that action is authorized.

## 2. Gather minimum necessary context

Use only approved systems and sources. Search hiring records, candidate materials, prior correspondence, internal meeting notes, and other authorized records to establish:

- The role and its most important outcomes.
- The candidate’s current hiring stage and next decision point.
- How the referee was introduced and whether the candidate identified them.
- The referee’s professional role and the nature, duration, and recency of their work with the candidate.
- Evidence already collected through interviews, work samples, or assessments.
- Other completed references and the specific themes that need corroboration or clarification.

Research the referee only enough to understand their ability to observe the candidate’s relevant work. A public professional profile or organization biography may help verify role and background, but do not collect unrelated personal details.

For prior references, read the completed notes rather than relying on summaries alone when access is authorized. Extract only job-relevant themes: demonstrated strengths, recurring development areas, examples of delivery, environmental fit, and limitations in the referee’s knowledge.

## 3. Turn research into a call hypothesis

Write a short briefing that answers:

- What can this referee observe directly that other sources cannot?
- Which role-relevant capabilities should this call test?
- Which earlier claims need confirmation, context, or challenge?
- What would increase or decrease confidence in the candidate’s ability to perform the role?

Use direct, evidence-seeking instructions. For example: “A prior referee described strong stakeholder communication but limited end-to-end ownership. Ask for one project where the candidate owned delivery from problem definition through follow-up.”

If this is the first reference, identify the claims that later calls should cross-check. Do not treat the first account as a final verdict.

## 4. Create the internal call record

Create one page or record in the organization’s chosen meeting or applicant-tracking system. Use a clear title such as:

`[Date] — [Referee name] — [Candidate name] reference call`

Include the date, authorized participants, candidate link or record link, and call logistics. Add the following content before the call.

```markdown
## Context
- **Candidate:** [name and approved profile links]
- **Role:** [role and key outcomes]
- **Hiring stage:** [stage and decision timeline]
- **Referee:** [name, professional role, organization]
- **Relationship:** [how, when, and how closely they worked together]
- **Other references:** [names/relationships if known and appropriate]
- **Call logistics:** [date, time, format, meeting link if access-controlled]

## Briefing notes
- **What this referee can speak to:** [specific observed work]
- **Evidence to validate:** [claim, source, and precise follow-up]
- **Open questions:** [role-relevant uncertainty]
- **Prior-reference themes:** [theme and whether to corroborate or investigate]
- **Limits:** [what the referee may not have observed]

## Opening
> Thank you for making time. I am speaking with references as part of an internal hiring process for [candidate] and the [role] position. I would like to understand your direct experience working with them, including strengths, development areas, and examples relevant to the role. Please share only information you are comfortable and permitted to discuss; your comments will be handled within our hiring process.

## Questions
- How did you work together, and how directly did you observe their work?
- What outcomes did they personally own? Please describe a specific example.
- What did they do especially well, and what did that look like in practice?
- Where did they need the most support, feedback, or structure?
- How did they respond when priorities changed, work became difficult, or feedback was direct?
- What role-relevant capability would you most want a future manager to develop?
- What environment, management approach, or team conditions helped them do their best work?
- What role or responsibility would you hesitate to give them today, and why?
- Would you work with them again? In what capacity?
- What have I not asked that would help us assess their fit for this role?

### Role-specific probes
- [Probe tied to a required capability]
- [Probe tied to a remaining hiring uncertainty]
- [Probe tied to a realistic work scenario]
```

## 5. Tailor role-specific probes

Choose three to five probes based on the job’s actual requirements. Ask for examples and observable behavior, not personality labels.

Examples:

- **Operations or program delivery:** How did they manage changing requirements, competing deadlines, and follow-through across stakeholders?
- **Community or relationship leadership:** How did they build trust, handle conflict, and turn participant feedback into improved systems?
- **Senior operations leadership:** Describe a time they improved a weak process, managed tradeoffs among stakeholders, or balanced speed with appropriate controls.
- **Technical or analytical work:** What was the complexity of the work, how did they reason through uncertainty, and how independently could they produce reliable results?

## 6. Run the conversation

Start by confirming the referee’s relationship and direct observation. Follow the prepared questions, but prioritize the decision-critical uncertainties.

Use neutral follow-ups:

- “What did the candidate specifically do?”
- “What was the result?”
- “How often did you observe that?”
- “What would have made the outcome stronger?”
- “Can you contrast that with peers at a similar level?”

Do not disclose confidential interview comments, private candidate information, or other referees’ identities or remarks. You may test a theme without attributing it: “We are assessing end-to-end ownership. What have you observed?”

## 7. Record evidence and assess quality

Immediately after the call, complete the record. Separate:

- **Observation:** what the referee directly saw.
- **Interpretation:** what the referee believes it means.
- **Inference:** what the hiring team concludes for this role.
- **Confidence:** how direct, specific, recent, and relevant the evidence is.
- **Limits:** conflicts of interest, limited exposure, long time elapsed, or uncertainty.

Do not convert one strong opinion into a final hiring decision. Compare evidence across interviews, work assessments, and references. Note meaningful contradictions, then determine whether more evidence is needed.

## Readiness and audit checks

Before the call, confirm:

- The call has a legitimate purpose and appropriate authorization.
- The referee’s relationship and ability to observe relevant work are understood.
- The questions are tailored to role outcomes and unresolved uncertainties.
- The internal record contains context, briefing notes, logistics, and an opening script.
- Sensitive information is minimized and access is limited appropriately.

After the call, confirm:

- Notes distinguish facts, opinions, and hiring-team inferences.
- Vague praise or criticism has been followed by concrete examples where possible.
- The referee’s limits of knowledge are recorded.
- The evidence has been compared fairly with other role-relevant evidence.
- The completed record is stored only in the approved hiring system.

## Common failure modes

- **Generic question list:** Replace it with probes tied to actual role outcomes and open decisions.
- **Overweighting seniority or confidence:** Weight direct, specific observation more heavily than title or certainty.
- **Confirmation seeking:** Ask neutral questions that permit both positive and negative evidence.
- **Unverified claims:** Request a concrete example, result, and the candidate’s personal contribution.
- **Collecting unnecessary personal information:** Return to professional, role-relevant evidence.
- **Incomplete documentation:** The prepared and completed internal record is the deliverable; research notes outside it are not sufficient.
- **Treating references as decisive alone:** Use them as one evidence source within a structured, job-relevant assessment process.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by selecting the least invasive authorized method, protecting account context and privacy, verifying rendered state, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for browser-based work such as completing rendered forms, changing settings, extracting information from dynamic pages, testing a user flow, capturing screenshots, or working in an authenticated dashboard. Use it when a supported direct interface, API, or simple page retrieval cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and never activate a consequential final action until the account, target, page state, and authorization are clear.

An automation command reporting success does not prove that a website accepted a change. Modern web applications may keep state outside the visible DOM, commit a field only after it loses focus, recreate controls after a re-render, or display an error even though an action completed.

## 1. Establish legitimate purpose and task boundaries

Before accessing private dashboards, communications, records, or information about people, confirm that the task has a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not collect unrelated personal details, copy credentials or session data into notes, or expose sensitive content in logs, screenshots, or reports.

Identify the requested outcome and boundary:

- What page, record, form, setting, or workflow is the target?
- What information must be entered, changed, collected, uploaded, or reviewed?
- What is the minimum information needed?
- Is the target personal, work-related, test, staging, or production?
- Is the intended action reversible?
- Does it send, publish, submit, pay, delete, grant access, alter a plan, or otherwise create an external commitment?
- Which choices require user judgment or are still ambiguous?

Keep outputs within the requester’s appropriate access boundary. Respect consent, privacy expectations, and applicable policies. Do not use browser access to bypass permissions, access controls, security warnings, anti-abuse measures, authentication requirements, or restrictions on data collection.

## 2. Choose the least invasive route

Use the first suitable route in this order:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can safely perform the task.
2. **Headless browser automation.** Use this for public pages, test environments, rendered-page extraction, screenshots, UI testing, and tasks that do not require the user’s existing signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an established account session, account-specific dashboard, single sign-on state, or a user-directed browser context.

Before driving a browser, check whether a direct route exists. Review official documentation, ordinary form actions, page source, application data embedded in the page, and normal network requests for supported endpoints. A form may submit structured data through an authorized service that is more reliable than reproducing complex browser interactions.

Do not reverse engineer or use endpoints to evade access controls, consent boundaries, terms, rate limits, or site protections. If a site blocks headless automation, do not try to defeat fingerprinting, challenge pages, or other anti-abuse controls for general research. A verified visible session may be appropriate only when the user explicitly asked to complete a legitimate task on that specific site and has authorized the necessary access.

Do not use an authenticated browser merely as a convenience when a headless or direct approach is sufficient. It can interrupt the user’s work and increases privacy and account risk.

## 3. Protect browser, account, and environment context

When a visible browser session is necessary, announce that control is being taken and state the purpose. Do not silently take over a user’s active browser.

Use a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing tab to use. This reduces the risk of disrupting unrelated work or acting in the wrong context.

Before opening the real target or changing data:

1. Classify the needed context: personal, work, test, staging, production, or another explicit category.
2. Select the browser profile or authenticated connection associated with that context. Do not rely on a generic browser selector, a remembered default, tab titles, or arbitrary connection names.
3. Verify the signed-in account through a reliable account indicator or account page.
4. Confirm the target organization, environment, and item to be changed.
5. If the account, environment, target, or authority is unclear, stop and ask before acting.

Use an account preflight gate for authenticated write actions. A useful question is:

> Which account is active? Which environment is active? What exact item will change?

If an automation system has a verification marker, permission gate, or equivalent control, mark the context verified only **after** the account check actually passes. Never create a marker in advance merely to unlock write capabilities.

Never reveal credentials, recovery information, session tokens, private account data, or security settings in output. Do not weaken multi-factor authentication, browser security, code-signing protections, or native-host security to make automation work.

## 4. Separate preparation from commitment

Treat filling, drafting, selecting options, and producing a preview as preparation. Treat submitting, sending, publishing, purchasing, deleting, changing plans, changing access, or activating an action labeled permanent or irreversible as commitment.

Use a two-phase process for forms and significant changes:

1. **Preparation pass:** Fill or configure the page, inspect all relevant state, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Re-check the account, target, readiness gate, and authorization. Then perform the final action once and verify completion.

Authorization rules:

- Honor an explicit request to review before submission.
- If a task or standing instruction already authorizes a normal, reversible change, do not ask again after verification unless the page shows unexpected scope or impact.
- For payments, sends, deletions, plan changes, publishing, actions marked irreversible, or other one-way commitments, obtain explicit confirmation immediately before the final action unless a clear policy or instruction specifically authorizes that exact commitment without another confirmation.
- If authorization is missing, prepare and verify the complete result, present a concise pre-action summary, and ask only for the final action.

If the page reloads, re-renders, or the session changes between phases, do not assume prior values remain. Re-inspect and re-verify before committing.

## 5. Inspect the rendered page before editing

Do not start by guessing selectors, using field indexes, or assuming that a visible label identifies the editable node. First inspect the page and identify the controls that matter.

For each relevant control, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or label relationship.
- Current value, required state, disabled state, and validation feedback.
- Character limits and formatting behavior.
- Whether the apparent field is the actual editable control, a wrapper, or a hidden synchronization element.
- Whether changing a control triggers a re-render, refreshes dependent fields, or resets prior entries.

Address controls by stable semantic identity: visible label text, an accessible name, or an explicit label relationship. Do not address fields by DOM position if a semantic identifier is available. Dynamic applications can reorder or replace controls between page loads.

A generic inspection record should include tag, type, role, label, required state, and readable value or value length.

```js
// Pseudocode: adapt to the selected browser automation capability.
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

Inspect the current state of records and settings before changing them. This helps avoid editing the wrong item or unintentionally overwriting existing values.

## 6. Use the correct interaction for each control

A generic “set value” action is not reliable across all browser controls. Choose an interaction that resembles the normal user action and then verify the result.

| Control type | Preferred interaction | Important check |
|---|---|---|
| Single-line input | Use normal text entry or fill behavior | Newlines may be removed silently. |
| Multiline text area | Fill text, then move focus away | Some applications save only on blur. |
| Rich-text or content-editable editor | Focus the real editable element, select existing content, enter text through keyboard-style events, then blur | Direct DOM mutation may not update the application model. |
| Dropdown or combobox | Open it and choose an option by visible text | Selection may trigger a full re-render. |
| Checkbox or radio group | Read current state first; change only if needed | Clicking an already-correct control can make it wrong. |
| Date or time picker | Select values, close the popover safely, and verify the displayed summary | Typing or closing controls may clear or reinterpret related values. |
| File upload | Confirm file, destination, recipients, and privacy impact first | Uploading may start immediately and be difficult to undo. |

For rich-text and framework-managed editors, use focus and keyboard-style input rather than direct changes to low-level DOM properties. A robust sequence is:

1. Focus the actual editable element.
2. Select existing content.
3. Delete it.
4. Enter the intended text through keyboard-style input.
5. Move focus to a neutral page element to commit the value.
6. Wait briefly for the application to settle.
7. Read the value back.

Some forms pair a visible editor with a hidden input. Editing the hidden input can look successful in an inspection record while server-side validation still treats the visible editor as empty. Target the control the user interacts with and the application actually reads. If an accessibility-based locator returns an empty wrapper, inspect the underlying labeled editor and use its actual label relationship.

If dropdowns, checkboxes, tabs, or date choices can trigger a re-render, make and verify those selections before entering long text. Re-inspect the page afterwards because prior fields may have been recreated.

## 7. Verify every meaningful edit

After each meaningful field entry or setting change, read its value back from the page. Compare it with the intended value. For sensitive content, compare length, required state, or a concise redacted summary rather than reproducing full private text in logs.

Look for these mismatches:

- The automation reports success but the page shows an empty field.
- Newlines, whitespace, punctuation, or special characters were removed.
- Text was truncated by a single-line control or character limit.
- A rich-text editor visibly changed but did not retain the value internally.
- A later interaction erased an earlier entry after a re-render.
- A hidden synchronization field changed instead of the visible editor.
- A selection changed a dependent recipient, date, requirement, or other field.

If verification fails, stop progressing toward submission. Diagnose the control type and retry once with a more suitable method. For example, replace direct value assignment with focus, keyboard entry, blur, and read-back. If the page still rejects or alters the value, report the limitation and ask how to proceed. Do not silently submit incorrect content.

## 8. Run a pre-submit readiness gate

Before a final submission or high-impact change, inspect the full relevant page state again. Confirm all of the following:

- The correct account, organization, environment, and target are active.
- Required fields are present and non-empty.
- Entered values match the intended content closely enough for the task.
- Dates, options, recipients, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **do not submit**. A partially prepared form is recoverable; an incorrect external action may not be.

Capture a pre-action record for consequential tasks. This can be a screenshot, structured state dump, or concise summary. Store and share it only through appropriate access boundaries. Avoid pasting a large table of sensitive values into chat when a short summary and securely accessible record are enough.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as dates, recipients, options, and attachments were checked.
- [ ] A pre-action record exists when the action is consequential.
- [ ] The final action, impact, and authorization are understood.

## 9. Confirm completion and handle failures safely

A final click is not proof of success. After acting, look for reliable evidence: a success message, confirmation reference, newly created record, persisted setting after a safe reload, sent item, published item, or durable status change.

If the site reports an error, first inspect the resulting state before retrying. A visible error can be cosmetic, and blind retries can create duplicate messages, payments, submissions, or records. If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Never represent an attempted action as completed.

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation says success but a field is blank | The application ignored a direct value update | Use focus, keyboard-style entry, blur, and read-back. |
| Earlier fields disappear after later edits | A re-render reset uncommitted state | Commit and verify each field; do re-rendering selections first. |
| Text loses characters or line breaks | Wrong control type or formatting restriction | Find the proper multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect and target the true labeled editor. |
| Validation says a visible value is empty | A hidden field was edited instead of the interactive control | Use the visible control that the application reads. |
| Browser automation becomes unstable on a complex page | The selected automation layer is unsuitable | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers differ | The site varies behavior by browser context | Prefer an authorized direct interface; for an explicit task, use a verified visible session without evading protections. |
| A date popover changes values unexpectedly | The widget has stateful clear, close, or parsing behavior | Close it through a neutral page action and re-verify all related values. |
| A visible error may be cosmetic | The action may already have succeeded | Inspect resulting state before retrying. |
| Account context is uncertain | Wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## Final audit checklist

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Controls were inspected before editing.
- [ ] Every meaningful change was read back and verified.
- [ ] Required fields and validation passed the readiness gate.
- [ ] A pre-action record was captured when appropriate.
- [ ] Required confirmation was obtained before a consequential commitment.
- [ ] Completion was verified after the action.
- [ ] The final report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a recurring workflow.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing skill, test whether it helps, and improve it through evidence and user feedback. A skill is a focused set of instructions, optionally supported by scripts, reference material, templates, and tests, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the job, users, boundaries, and permissions.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements where appropriate.
5. Improve the skill based on evidence rather than isolated preferences.
6. Repeat until the skill is useful, reliable, and not merely tailored to a few examples.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the finished skill.

Do not force every project through every stage. Some users want a quick draft or an informal collaborative pass. Others need a careful comparison, measurable requirements, and several test iterations. Identify the user’s current stage and help them take the next useful step.

## Communication principles

Match the user’s technical vocabulary and experience. Use plain language by default. Terms such as *evaluation* and *benchmark* are often useful, but briefly define them if needed. Do not use unexplained technical terms such as “schema,” “assertion,” or “JSON” unless the user is comfortable with them.

Explain why key questions matter. For example:

> What should a successful result look like: a chat response, a structured report, a file, or an approved external action? The answer determines how the skill should work and how to test it.

Keep the user involved in decisions that affect scope, risk, usability, or cost:

- Confirm the intended job before writing extensive instructions.
- Ask before choosing a restrictive scope, required capability, or approval policy.
- Share proposed test cases before relying on them.
- Let human judgment lead for subjective quality, including tone, aesthetics, strategy, and creative usefulness.
- Be transparent when a test is only a sanity check rather than an independent comparison.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea for recurring work, such as preparing status summaries, validating data files, or producing a standard document. Start with discovery, then create a draft.

### B. Existing skill or draft

The user has instructions they want to edit, simplify, test, package, or improve. Read the current skill before proposing changes. Preserve its established name and identity unless the user explicitly asks to change them.

### C. Workflow demonstrated in the conversation

The user may ask to “turn this into a skill.” Extract what is already known from the conversation before asking questions:

- Inputs the user supplied.
- Information sources and capabilities used.
- The order of actions and decisions.
- Corrections or preferences the user gave.
- Output format and acceptance criteria.
- Conditions that caused the workflow to change direction.

Summarize the inferred workflow and clearly list the gaps that need confirmation. Do not silently turn a one-time workaround into a general rule.

### D. Evaluation or optimization request

The user may already have a complete-looking skill and ask whether it works. Go directly to test design, evaluation, and targeted revision. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough information to define a coherent job. Do not ask every question mechanically; begin with the unknowns that most affect the design.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Trigger:** What requests, wording, or contexts should cause the skill to be used?
3. **Inputs:** What information, files, examples, systems, and authorized sources may it use?
4. **Outputs:** What should it produce, change, or recommend? Is there a required format?
5. **Success criteria:** How will the user know the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask a question, pause, decline, or hand work back to the user?
7. **Variations:** What common cases, hard cases, and exceptions materially change the workflow?
8. **Dependencies:** Does it require specific capabilities, tools, reference material, templates, or user-provided access?
9. **Testing:** Should it be tested with example requests before release?

Useful clarifying choices include:

- “When information is missing, should the skill make a clearly marked best effort or stop and ask?”
- “Should the output be brief, detailed, or selectable by the user?”
- “May the skill use any accessible source, or only sources the user has specifically approved?”
- “Which actions require explicit confirmation because they are external, irreversible, or high impact?”

### Privacy, authorization, and source boundaries

If a skill accesses communications, records, files, or other information about people, establish a legitimate purpose and clear authorization before using them. Use only the minimum relevant sources and information. Omit unrelated personal or sensitive details from outputs, respect consent and privacy expectations, and keep results within the intended access boundary.

For example, a skill that summarizes approved case notes should focus on information relevant to the authorized task, avoid unrelated personal details, and state when it cannot verify permission or source completeness.

### Research before drafting

When useful, consult user-approved documentation, existing conventions, comparable skills, templates, or domain guidance. Research should reduce burden on the user, not replace their authority over requirements.

Use research to identify:

- Existing output standards and conventions.
- Constraints imposed by tools, data formats, or governing policies.
- Reusable patterns for similar tasks.
- Safety, privacy, compliance, and approval requirements.

If sources conflict or a requirement is uncertain, state the uncertainty rather than guessing.

## 3. Choose the skill structure

Keep a skill focused enough that users and the AI can predict what it does. One skill may support closely related variants of the same job, but separate unrelated work when it has different audiences, permissions, sources of truth, or definitions of completion.

A portable skill package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional supporting documentation
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help decide whether the skill applies.
2. **Core instructions:** The workflow needed for typical use.
3. **Supporting resources:** Detailed references, templates, or scripts used only when relevant.

Keep the core instructions readable. If they become long, move domain-specific details into clearly named reference files and state exactly when to read each one. Large reference files should include a table of contents or navigation section.

When a skill supports multiple variants, organize references by variant. For example, a deployment skill might contain one shared decision workflow and separate references for different hosting environments. The AI should select the relevant variant instead of loading everything by default.

### Use scripts for repeatable deterministic work

Consider a bundled script when test runs show repeated reconstruction of the same reliable procedure, such as validation, conversion, calculation, formatting, or file generation. A script is justified when it is:

- Deterministic or easier to verify than free-form reasoning.
- Reused across requests.
- Safer or less error-prone than recreating the procedure each time.
- Clearly within the user’s intended authorization boundary.

Document what a script does, its inputs, outputs, limitations, and when not to use it. Do not automate an action merely because automation is possible.

## 4. Write the skill

Write in clear, imperative language. Explain the reason behind important instructions, especially when a rule prevents a predictable failure. AI systems generally work better when they understand the quality or safety goal than when they receive a long collection of unexplained prohibitions.

A useful skill commonly includes the following sections.

### Purpose and scope

State the job, intended users, and boundaries. Clarify whether the skill creates an answer, produces a file, takes an action, or guides the user through a process.

### Inputs and prerequisites

List required information, permitted sources, required capabilities, and optional inputs. State what to do when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or produce a draft clearly marked as incomplete.
```

### Workflow

Give the normal sequence of actions and include decision points rather than trying to list every possible edge case.

A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Clarify only the requirements that materially change the work.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result, assumptions, and unresolved limitations.

Use conditional guidance where needed:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested change could overwrite important work, explain the impact and request confirmation before proceeding.
```

### Output format

When consistency matters, define an exact or near-exact template.

```markdown
# [Title]

## Summary
[One short paragraph]

## Findings
- [Finding with evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing information]
```

Avoid rigid formatting when the task’s value depends on adapting to context. In those cases, describe goals, required content, and a small number of examples rather than imposing a fixed shell.

### Quality and safety checks

State the checks needed before completion. Depending on the task, this may include confirming required fields, validating calculations, checking that a file opens, preserving original data, citing important claims, or flagging uncertainty.

A skill must behave in ways a user would reasonably expect from its description. Do not create instructions that conceal actions, bypass authorization, extract confidential information, damage systems, or facilitate unauthorized access. If a request exceeds authority or is unsafe or deceptive, explain the limitation and offer a safe alternative when possible.

### Failure behavior

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** Explain what could not be verified and offer an alternate method if one exists.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, report the issue, or request guidance.
- **Permission-sensitive action:** Pause for confirmation before an irreversible, external, or high-impact action.

### Examples

Use a small number of generalized examples only when they teach a distinct pattern. Examples should illustrate reasoning or output shape, not become a narrow substitute for reasoning.

## 5. Write a strong skill description

The description is primarily a routing instruction: it helps an AI decide whether the skill applies. State both **what the skill does** and **when it should be used**.

Cover realistic user language, including requests that imply the task without naming it. A system may fail to use a relevant skill unless the description makes relevance clear.

A good description includes:

- The task or outcome.
- Common contexts and user phrasing that indicate the task.
- Important scope limits that prevent harmful or costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use for requests involving leadership summaries, progress updates, milestone reviews, risks, blockers, and next steps, even when the user does not use the phrase “status report.”
```

Do not put the entire procedure in the description. Avoid vague labels such as “help with documents,” and do not make it so broad that it captures nearby tasks better handled by another skill.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description clearly say when to use it?
- Are required inputs, permissions, and outputs clear?
- Does the workflow explain why important checks exist?
- Does it define behavior when information is missing?
- Are there unnecessary rules, repeated guidance, or brittle wording?
- Does it avoid personal habits, undeclared access, or assumptions about a particular environment?
- Would a capable AI have enough freedom to handle normal variation?

Prefer a lean, understandable prompt over a long prompt full of rules that do not change outcomes. Excessive absolute wording is a warning sign unless the behavior is genuinely non-negotiable, such as an authorization or safety boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create a small evaluation set. Begin with two or three realistic prompts that resemble genuine user requests. Share them with the user and invite corrections or additions.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Any input files or supplied context.
- The expected outcome in plain language.
- Objective checks, if suitable.

A portable structure is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and flag anything that cannot be verified.",
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Use cases that cover meaningful variation:

- A typical successful request.
- A request with incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic edge case that changes the workflow.
- A request that should require approval, cautious handling, or refusal when relevant.

Do not make tests merely repeat the skill’s wording. Vary phrasing, detail level, and user sophistication. Avoid retaining personal scenarios or sensitive content; test the general category of challenge instead.

## 8. Run comparisons

When independent runs are available, compare the skill against a meaningful baseline.

- **For a new skill:** Run each test with the skill and without the skill.
- **For an existing skill:** Save an unchanged snapshot before editing, then compare the revised version with the earlier version.

Launch skill and baseline runs under comparable conditions. When parallel execution is available, start both configurations for every test case at the same time. This makes timing comparisons fairer and avoids changing the baseline after observing the skilled result.

Use an iteration structure that keeps artifacts organized:

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

For each run, preserve the prompt, supplied files, output, and available metadata such as elapsed time and resource use. Record timing as soon as the execution environment reports it, because some environments do not retain it later.

If independent or parallel runs are unavailable, perform a transparent sanity check instead: follow the skill on each test prompt, preserve the output, and ask the user to review it. Do not describe this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs are underway, draft objective checks where they genuinely help. Explain the checks to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful. Examples include:

- Required sections are present.
- A produced file opens and contains required fields.
- Calculated values match an approved source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- The output includes source references when required.

Each check should have descriptive text, a pass/fail result, and evidence.

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

Use programmatic checks whenever practical. They are generally more repeatable than visual inspection and can be reused in later iterations.

Do not force numerical checks onto subjective work. Writing quality, visual design, usefulness, tone, and strategic judgment often require human review. A weak metric can cause a skill to optimize for the metric instead of the user’s real goal.

## 10. Review results with a human

Present both the outputs and the measurements. Use any available review interface that lets the user inspect each test case, compare configurations, and leave feedback. If no review interface is available, present the results clearly in conversation or as accessible files.

For each test case, provide:

- The original prompt.
- Relevant supplied inputs.
- The skill output and comparison output, if available.
- Objective grades and supporting evidence.
- Timing or resource data, if available.
- A clear way for the user to say what worked and what should change.

Ask focused questions such as:

- Which result would you trust in normal use, and why?
- Did the skill add work or detail that was not valuable?
- What was missing, misleading, or difficult to use?
- Would this still work if the wording or input data changed?

Empty feedback can suggest a case is acceptable, but it is not proof that the skill works generally. Consider the output, test results, and broader coverage together.

## 11. Analyze results beyond pass rates

Aggregate results where possible: pass rate, average time, average resource use, and variability. Present the revised skill before its comparison condition so the report is easy to read.

Then perform an analyst pass. Aggregate statistics can hide important patterns. Look for:

- **Non-discriminating checks:** Both conditions pass, so the check does not reveal the skill’s value.
- **High variability:** Comparable runs differ substantially, suggesting ambiguity, instability, or unreliable instructions.
- **Tradeoffs:** The skill improves quality but adds excessive time or resource use.
- **Failure concentration:** Several failures share a root cause, such as unclear source selection or missing output rules.
- **Unproductive work:** Execution traces show redundant planning, research, formatting, or tool use.
- **Repeated reconstruction:** Multiple runs independently create the same helper procedure, suggesting a reusable resource may help.

Do not treat a small benchmark as conclusive. Use it as evidence for the next revision.

## 12. Improve without overfitting

Base revisions on user feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from complaints. If one output omitted a source note, do not add a rule that only references that test. Instead, clarify the broader behavior: when evidence is incomplete or mixed, distinguish verified information from assumptions and missing data.

Use these principles:

1. **Fix causes, not examples.** Design for future requests, not just current tests.
2. **Keep instructions lean.** Remove guidance that does not change behavior or causes wasted effort.
3. **Explain intent.** State why a step protects quality, usability, privacy, or safety.
4. **Add reusable resources only when justified.** Bundle scripts, templates, or references when repeated work demonstrates their value.
5. **Preserve useful behavior.** Do not discard parts users already value while solving another problem.
6. **Expand coverage gradually.** Add a test when it represents a real class of failure, not every isolated incident.

After revision, rerun the full test set in a new iteration. Use the same baseline policy unless there is a clear reason to change it. Where possible, show the new outputs alongside earlier outputs and collect feedback again.

Stop when one or more conditions is true:

- The user says the skill is ready.
- Feedback is consistently positive or empty across meaningful cases.
- Objective requirements are reliably met.
- Further revisions are not producing meaningful improvement.
- Remaining weaknesses require missing information, unavailable capabilities, or a product decision rather than better instructions.

## 13. Optional blind comparison

For a more rigorous comparison of two versions, use blind review. Give an independent evaluator two outputs without revealing which version created each. Ask the evaluator to judge against a shared rubric, then reveal the mapping only after the judgment is recorded.

Blind comparison is useful when:

- Two versions have similar measured results but different qualitative quality.
- The user or author may be biased toward a newer version.
- The decision has meaningful cost or impact.

Keep the rubric tied to user value: correctness, completeness, clarity, adherence to constraints, safety, and practical usability. Analyze why the preferred output won before editing again.

## 14. Optimize triggering behavior

After the skill’s workflow is stable, evaluate the description that controls activation. Do this after, not before, the skill itself is useful.

Create a realistic set of trigger queries containing cases that **should trigger** and nearby cases that **should not trigger**. Use roughly balanced coverage and enough detail that consulting a skill would actually help.

Positive cases should vary by:

- Formal and casual phrasing.
- Directly named and implied requests.
- Common and less common valid use cases.
- Situations where a related skill might compete but this skill should apply.

Negative cases should be challenging near-misses, not obviously irrelevant requests. They should share terms or concepts with the skill but belong to another job, require a different capability, or lack the conditions that make this skill appropriate.

```json
[
  {
    "query": "I need a concise leadership update from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what project status reporting is and why teams use it?",
    "should_trigger": false
  }
]
```

Review the query set with the user before using it. Weak trigger tests produce misleading descriptions.

If the environment supports repeated activation tests, separate queries used to improve the description from held-out queries used to select the final version. Choose the description that performs best on held-out cases rather than the one that best fits the examples used during editing.

Remember that simple one-step tasks may not activate a specialized skill even when the description matches; an AI may handle them directly. Trigger tests should therefore describe substantive tasks where consulting the skill would add value.

When applying a final description, show the user the before-and-after wording and the evaluation result. Ensure the final description remains honest about scope.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately describes activation conditions.
- Instructions do not depend on personal conventions, private access, or undeclared capabilities.
- References and scripts are present, clearly named, and documented.
- No credentials, personal records, confidential content, identifiers, or sensitive examples are included.
- The user can understand how to install, access, or adapt the package in their chosen environment.
- Test material is retained only when it is safe and useful to include.

Provide a short handoff note that explains what the skill does, required capabilities, known limitations, and a practical way to test it after installation.

## Final readiness gate

A skill is ready when it has:

- A clear, bounded job.
- A description that routes appropriate requests.
- Instructions that handle normal variation.
- Explicit behavior for uncertainty, authorization, privacy, and high-impact actions.
- Output expectations and quality checks appropriate to the task.
- Evidence from realistic use that it improves outcomes.
- No hidden dependence on private data, personal workflows, or undeclared tools.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for the user’s real recurring work.


---
name: test-every-screen-size
description: Verify UI and CSS changes across representative narrow, wide, short, and tall viewports. Combine screenshots with programmatic layout checks, then fix and retest every failure.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring the work complete, requesting review, publishing, or releasing. Apply it even to a small spacing, color, or background edit: local changes can affect wrapping, height, overflow, alignment, and backgrounds at other screen sizes.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Use real screenshots and numerical checks together.

## 1. Prepare realistic page states

Run the real interface in a safe test environment. Populate the changed surface with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative lists, cards, rows, and validation messages;
- realistic item counts or content near expected limits;
- loading, empty, and error states when the change affects them.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping, and unintended blank space.

## 2. Choose the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, when the interface is expected to be used on large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Also include any known target viewport. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a headless browser automation tool, or another repeatable browser-testing system selected for the project.

## 3. Capture and inspect screenshots

Capture real screenshots at each relevant viewport and state. Use full-page screenshots when page length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect every changed component on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design after the component's role changed.

Pay special attention to edge-to-edge or full-bleed changes. A component that becomes flush with an edge may expose leftover wrapper margins or padding as visible background strips. Check every edge, not only the edge edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is meant to fit the viewport;
- no changed element overlaps neighboring content or its intended container;
- buttons, links, and fields remain visible and usable;
- fixed or sticky UI does not hide essential content;
- cards, lists, and form controls remain within intended bounds;
- body text retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant bounding rectangles with adjacent elements and container boundaries.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line; reading-focused designs commonly use a narrower target of roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visual defects such as exposed background strips, poor balance, or unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and relevant programmatic checks pass.

## 6. Fix failures and rerun the sweep

If any viewport or realistic state fails:

1. stop the completion or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the failing size.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights or states, and the checks performed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, say so clearly and do not represent the UI change as complete.


---
name: run-a-recurring-community-event
description: Create, publish, and verify the next occurrence of a recurring community event, including fresh event materials and invitations to an authorized audience, while applying explicit authority, privacy boundaries, and attendee-facing checks.
---

# Run a recurring community event

Use this workflow for a recurring social, sports, learning, volunteer, or neighborhood event. Adapt it to the organizer's chosen event platform, calendar, image-generation capability, file storage, and communication channels.

## 1. Establish authority, purpose, and access boundaries

Before making external changes, determine the operating mode:

- **Prepare only:** Create materials and an unpublished draft.
- **Approval required:** Prepare the event and obtain approval before publishing or inviting.
- **Standing authorization:** Publish and send invitations according to a documented recurring-event policy.

Standing authorization should identify the series, usual audience, organizers who may be added as hosts, permitted platforms, and invitation rules. Ask for a decision when the occurrence materially changes the normal arrangement, for example a new audience, paid entry, a changed privacy level, a different venue, an unusual safety concern, or a major format change.

When accessing prior event records or attendee lists, have a legitimate event-management purpose and clear authorization. Use only the minimum relevant records, honor opt-outs and consent expectations, and do not expose attendee information outside the authorized event-management context.

## 2. Determine the next occurrence

Calculate the next occurrence from the recurrence rule and local time zone using a reliable date or calendar capability. Do not rely on mental date arithmetic.

Confirm:

- weekday and full date;
- start and end time;
- time zone;
- venue or meeting point;
- host and co-host arrangement; and
- any sequence number.

If the series is numbered, inspect prior events and use one number higher than the highest existing number. Include any early unnumbered events when reviewing the series history so the invitation process does not omit their attendees.

Check relevant conflicts, such as organizer unavailability, venue closures, public holidays, weather-sensitive plans, or calendar overlaps. A conflict does not automatically mean the event should be cancelled. Follow the organizer's policy, and report a remaining handoff, cancellation, or contingency decision.

## 3. Reuse stable details and refresh changing details

Review the latest one or two events before creating the new one. Separate information into:

- **Stable details:** event purpose, usual format, meeting-point instructions, regular contact route, accessibility notes, and standing links.
- **Occurrence-specific details:** date, sequence number, hosts, route, weather plan, capacity, theme, special instructions, and temporary notices.

Use the approved naming pattern and description template. Deliberately update every date-sensitive or occurrence-specific detail. Do not carry forward stale dates, expired links, a prior week's special instruction, or temporary venue information.

## 4. Prepare fresh artwork when artwork is part of the series

Keep a recognizable visual identity while making each occurrence visibly distinct. Review recent artwork before creating a new image so the result is not merely the same composition with minor changes.

Build a concise image brief with:

- required event text;
- recognizable activity or event symbols;
- desired illustration, photo, or graphic style;
- mood and palette;
- one new central visual idea; and
- quality constraints.

Vary the main idea through season, weather, lighting, viewpoint, local texture, an activity detail, or a small humorous focal object. Prefer one clear subject over a crowded composition. Request readable typography, restrained color, clean spacing, and no obvious visual-generation defects.

Review the result before use. If it repeats a recent design, has garbled text, implausible anatomy or objects, excessive gloss, clutter, or poor cropping potential, revise the brief and regenerate a limited number of times. Do not retry indefinitely. If an image tool reports an error, first check whether the image was actually produced before retrying.

Download or export the selected image into a location accessible to the event platform. Upload it and wait for completion before changing unrelated fields. Confirm the visible event image is the intended file and that its crop and legibility are acceptable.

## 5. Create the event carefully

Use the authorized organizer account and verify the active account before editing. If multiple browser profiles or accounts exist, explicitly choose and verify the appropriate one for each service.

Complete fields in this order when practical, especially on fragile forms:

1. **Title:** Apply the approved title pattern, such as `Community Event #N`.
2. **Date and time:** Set the local date, start time, and end time.
3. **Location:** Select the exact venue or map listing, not a similarly named result.
4. **Description:** Apply the current approved template and occurrence-specific changes.
5. **Image:** Upload and inspect the artwork.
6. **Hosts:** Add only authorized hosts or co-hosts.
7. **Settings:** Confirm visibility, capacity, cost, RSVP rules, notifications, and accessibility information.

Treat date pickers and dynamic forms as high-risk controls. Complete and verify date and time selection before entering other fields. Some interfaces interpret typing while a picker is open, clear an end date with a close-looking control, or shift layout when menus appear. After opening a menu, scrolling substantially, resizing the window, uploading a file, or changing the page layout, re-check visible state before clicking again. Prefer controls identified by labels and roles rather than fixed screen coordinates.

Do not assume a button labeled “Save” creates only a draft. Determine whether it publishes immediately, creates a preview, or saves an unpublished event.

## 6. Verify before and after publication

Review the draft or preview as an attendee would. Confirm:

- title and sequence number;
- weekday, date, start time, end time, and time zone;
- exact venue and map pin;
- description, links, and contact details;
- image presence, crop, and legibility;
- host or co-host status; and
- visibility, capacity, cost, RSVP, and notification settings.

If a required item cannot be verified, do not claim the event is ready. Correct it, use an approved fallback, or request a decision.

Publish only under the selected authority mode. Open the live event page afterward and repeat attendee-facing checks. Save the live URL.

## 7. Invite the approved audience

Follow the documented invitation policy. Inviting attendees from prior occurrences can be appropriate when authorized, but it is not a universal default. Do not expand the audience without permission.

When using prior event attendance as the source:

1. Identify all relevant past occurrences, including early unnumbered ones.
2. Filter or review one occurrence at a time.
3. Check whether that group's attendees are already selected before using a bulk-select action.
4. Add the group, clear the filter, and continue systematically.
5. After each group, confirm the invitee count increased by a plausible amount.

Some platforms preselect people from a recent event, and a bulk-select action may toggle them off rather than add them. If the count drops or does not change as expected, stop and inspect the selection before continuing. After any layout shift, re-check the active filter, checkbox state, and count. Use platform deduplication where available; otherwise compare lists sufficiently to avoid repeated invitations.

Send invitations only when authorized. Confirm a sent state, delivery confirmation, or final invited count. If the platform cannot provide confirmation, report that limitation rather than assuming delivery.

## 8. Completion report

Provide a brief report that states:

- what was created and whether it was published;
- date, time, and venue;
- invitation outcome or current invitee count;
- conflicts, unresolved items, or nonstandard settings; and
- the live event URL.

When the URL must be easy to copy, place it alone on the final line with no text after it.

## 9. Maintain reusable lessons

After an occurrence, record only durable process improvements: changed platform behavior, field-order constraints, updated templates, recurring audience rules, and content preferences. Keep temporary facts about one event separate from the reusable workflow.

## Readiness gate

Before declaring success, verify all of the following:

- The next date and sequence number were calculated and checked.
- The correct organizer account and live event page were verified.
- Stable details remain current and changing details were updated.
- Artwork is distinct, usable, and correctly uploaded when required.
- End time, time zone, venue, hosts, and settings were confirmed.
- Invitations followed the authorized policy, respected opt-outs, and remained within the appropriate privacy boundary.
- Publication and invitation outcomes were verified, or any verification limit was clearly reported.

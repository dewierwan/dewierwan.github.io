# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice. Use this workflow when someone needs credible paths forward before committing.
---

# Brainstorm options

Use this workflow when a user needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas. It is to surface genuinely different paths, make tradeoffs clear, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user provided. Review linked or referenced material only when it is available, relevant, and likely to change the options or recommendation.

If the question is not self-contained, seek a small number of high-value sources of context, such as:

- Earlier decisions and their rationale
- Constraints, commitments, budgets, or deadlines
- Needs of affected parties and decision ownership
- Evidence about what has already been tried

When accessing private communications, records, or material about people, do so only for a legitimate purpose and with clear authorization. Use the minimum relevant information, exclude unrelated personal or sensitive details, respect consent and privacy expectations, and keep the response within the appropriate access boundary.

Do not search broadly by default. Use targeted retrieval only when it could materially change the decision. If important context is unavailable, state the assumption or ask a focused question rather than inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The user’s request may describe a symptom or preferred solution rather than the real decision. For example, “Should we add a feature?” may actually mean, “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes process, incentives, scope, timing, or the problem framing
- At least one surprising option, such as delaying, partnering, reducing scope, or doing nothing

Do not be contrarian merely to appear creative. A “do nothing” option is useful only when observation, timing, or avoided distraction has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

| Element | Include |
|---|---|
| What | One or two sentences explaining the approach. |
| Strengths | One or two concrete advantages. |
| Weaknesses | One or two concrete disadvantages, risks, or costs. |
| Effort | Low, Medium, or High. |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, and burden on affected parties. Add domain-specific criteria when they matter more than these defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are instructive, but clearly state why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may select an option, request more detail, reject the framing, ask for additional options, or combine approaches.

If they propose a hybrid, test whether its components are compatible and whether the combination resolves a real tradeoff rather than merely adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term obligations, significant role decisions, or choices with broad effects.
- **Reversible choices:** Create a right-sized decision record that defines the choice, decision owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, tasks, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than only the stated request.
- The options are genuinely distinct.
- At least one option challenges the default framing when that could be useful.
- Strengths and weaknesses are concrete and candid.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than the assistant’s preferences.
- Any additional context was used only as needed and did not expose unrelated or sensitive information.


---
name: pressure-test
description: Find the weak points in a leading strategic idea before committing to it. Steelman the case, test its load-bearing assumptions through sequential challenge, and finish with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Position in the decision process

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision at a level of rigor that matches its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing a single idea too early can turn the exercise into defending it.

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision instead.

## Rules of engagement

- Be direct. Do not treat confidence as evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Use available evidence: research, metrics, prior experiments, customer feedback, documented decisions, or stakeholder input. Distinguish facts from inferences and forecasts.
- Refer to relevant dissenters by role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- When reviewing communications or records about people, confirm a legitimate purpose and authorization. Use only the minimum relevant material, omit unrelated sensitive details, and keep the output within the appropriate access boundary.
- Skip a section only when it is genuinely irrelevant, and say why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's actual intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

**Template**

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, starting with the assumption most likely to undermine the decision.

| Rank and assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | How to test or disprove it |
|---|---|---|---|---|
| 1. [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Smallest useful test] |

Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions and adapt later questions to the answers received. Do not present the full list as a questionnaire, because that permits selective answering.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed? Why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence. Ask what observed behavior, data, comparison, or commitment supports that belief. If an answer is vague, probe it before asking the next question.

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
description: Match decision-making rigor to stakes and reversibility, make a clear call when ready, and record and review meaningful choices without inventing the user’s views or crossing privacy boundaries.
---

# Make a decision

Use this workflow to apply enough rigor to a decision without turning every choice into a long project. The aim is a clear, accountable call; a useful record for meaningful choices; and better judgment through review.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices deserve minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, is leaning toward, or decided something they did not actually say.
3. **Separate advice from attribution.** Recommendations belong in conversation as **Assistant analysis**. Put them in a record only when the user specifically requests that.
4. **Record only with permission.** “Should we do X?” requests analysis, not a record. Create or update a record only when the user asks to log, track, open, resume, or commit it, or has explicitly agreed to a standing recording practice.
5. **Respect access boundaries.** Before searching shared messages, records, or a decision register, establish a legitimate purpose and authorization. Use only the minimum relevant information and exclude unrelated sensitive details.
6. **Do not confuse execution with a decision.** If there is no meaningful alternative, say so and move to planning or doing the task.
7. **Do not deliberate indefinitely.** Once the appropriate gates are met, name the decision and move forward.

If a register is visible to others, confirm that the audience is appropriate before writing. For health, relationships, compensation, confidential personnel matters, or similarly sensitive subjects, offer a private record or keep the discussion in chat.

## 1. Choose the mode

If the user explicitly says to start, resume, commit, or review a decision, follow that instruction. Otherwise, if authorized, check the chosen decision system for overlapping records before making a duplicate.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An existing record is open and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to decide.
- **Review:** A resolved decision has reached its review date and its outcome is still unknown or marked too early.

For a resumed decision, append new material rather than rewriting history. For a review, use the original prediction, confidence, and reasoning as the baseline.

## 2. Frame the decision

Write the question so it can be answered. Establish:

- What choice is being made?
- Who has decision authority?
- What are the realistic options, including doing nothing?
- What deadline, event, or constraint requires a decision?
- What result is sought?
- What happens if no action is taken?

If the question is broad and credible options do not yet exist, generate options before evaluating them. If only one viable path exists, say: “This is a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time if needed. Use the cost of unwinding the decision—money, time, trust, disruption, opportunity cost, and reputation—to classify it.

| Bucket | Meaning | Required treatment |
|---|---|---|
| Trivial | Low stakes; reversible within hours | Decide now; do not record by default |
| Reversible | Moderate stakes; reversible in days or weeks | Compare a few options; light record if requested |
| Hard to reverse | Material cost or disruption to undo | Full analysis, challenge gate, stakeholder check |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis plus dissent and named prerequisite conversation |

If the unwind cost cannot be named quickly or is uncertain, treat the decision as larger until evidence shows otherwise.

## 4. Apply the right rigor

### Trivial

Choose a reasonable default, state a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: attention spent deciding may exceed the cost of an imperfect choice.

### Reversible

In a short session:

1. List two or three realistic options.
2. For each, state one major strength, one weakness, and a rough effort, time, or cost estimate.
3. Give a recommendation and the decisive reason.
4. If uncertainty matters, select the smallest reversible test that could change the choice.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test examines assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and material stakeholder objections.

If no relevant challenge has occurred in the current work context, stop the commitment flow and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Proceed only after the pressure test is complete or the user explicitly overrides it with a reason. If it finds a serious unresolved problem, do not force a commitment. Return to option generation, redesign the option, obtain a decision-changing fact, or run a bounded test.

After the gate:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check with people who have relevant expertise, bear consequences, or may reveal constraints.
4. Provide a recommendation labeled **Assistant analysis** unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and represent their strongest case fairly.

The choice is not ready until the required conversation has occurred, unless the user explicitly records why proceeding is necessary. If it is being rushed, state exactly which consultation, evidence, or dissent is being skipped and why that matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence for it.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.

Separate non-negotiable requirements from preferences. Use scoring only when it clarifies real tradeoffs rather than disguising judgment.

Maintain three distinct categories:

- **User’s stated view:** only what the user actually said.
- **Assistant analysis:** the assistant’s recommendation and reasoning.
- **Open question:** uncertainty not yet resolved.

If the user has not stated a position, write “No position stated yet” or leave the field blank. Never create a user lean, confidence level, dissent response, rationale, or final choice from inference.

## 6. Commit and record

Before finalizing, confirm:

- What is the decision and chosen option?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action and by when?
- What observable result is predicted?
- What is the user’s confidence in that prediction?

For meaningful decisions, make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [X%].

Use a user-chosen document system, decision register, or private file. Where a structured system is used, create new records from its approved template when available, then fill its metadata and sections without replacing prior history. At minimum, record status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

A decision may be open or resolved. If the system uses yes/no resolution, use the status to represent whether a decision has been made or the answer to a binary question; a non-binary choice that has been settled is still resolved. Keep outcome assessment separate from resolution.

Suggested review defaults: one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar, task system, or equivalent reminder for high-stakes reviews.

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

For an open decision, record context, current options, and new inputs, but leave user commitment sections blank until the user commits. On resume, append a dated thinking-log entry and add new options where appropriate.

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare results with the recorded prediction and confidence.
3. **Was the process sound?** Assess the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. A poor outcome can follow a sound decision process, and a favorable outcome can follow weak reasoning.

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

Use direct language. Challenge weak reasoning with evidence, but do not let rigor become an excuse for endless deliberation.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only stopping point when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the solution is not already clear. Do not use it for a small fix, a routine task with a known implementation, or a request that only needs a direct answer.

By default, work from understanding through implementation and handoff. If the user requests analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the problem

Start with the underlying problem rather than the user's proposed solution. If the request is "build X," work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today?
- What workarounds, failures, delays, or risks exist?
- How frequent, urgent, costly, or blocking is the problem?
- What outcome would meaningfully improve the situation?

Write a concise problem statement and descriptive requirements. State the desired outcome, constraints, and success conditions without assuming a particular implementation.

If the proposed solution does not appear to address the actual problem, say so plainly and explain why. Ask only for information that cannot reasonably be learned from authorized project context, documentation, code, or records.

When reviewing private communications, operational records, or information about people, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant sources, omit unrelated personal details, and keep findings within the appropriate access boundary.

## 2. Assess priority and decision readiness

Decide whether this should be solved now. Consider severity, frequency, number of affected users, opportunity cost, available workarounds, and maintenance cost. Treat “do nothing,” “deprioritize,” or “improve the workaround” as valid options.

Classify the decision:

- **Reversible decision:** A small choice that can be changed cheaply. Use reasonable judgment, choose, and proceed.
- **Hard-to-reverse decision:** A public interface, persistent data change, migration, long-lived setting, security boundary, external contract, or vendor commitment. Pause before implementation and obtain an explicit decision from the responsible owner.

If priority or direction is unclear, present the tradeoff before investing in detailed design. Record the rationale for consequential decisions when useful.

**Readiness gate:** Proceed to solution design only when the problem, owner, desired outcome, and decision authority are sufficiently clear. Otherwise, return with focused questions or recommend discovery work.

## 3. Research the current context

Review the relevant project guidance, architecture notes, service documentation, existing code, tests, operational procedures, prior attempts, and known constraints. Look for established patterns, reusable components, and existing platform capabilities before creating something new.

Check compatibility requirements, deployment and release practices, data handling rules, supported environments, ownership boundaries, monitoring, and security expectations. Follow existing conventions unless there is a strong, documented reason not to.

Keep a distinction between facts, assumptions, and unknowns:

| Type | Example |
|---|---|
| Fact | Existing authentication must remain compatible. |
| Assumption | Most users can complete the workflow without training. |
| Unknown | Expected peak request volume has not been confirmed. |

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. Adapt these to the problem:

- Must preserve important existing behavior, including authorization and data integrity.
- Must fit the available delivery time and maintenance capacity.
- Should avoid unnecessary dependencies, services, persistent settings, and public surface area.
- Must have a clear test and verification method.
- Should be reversible or removable if it fails.
- Must meet applicable privacy, security, reliability, and accessibility requirements.

These criteria prevent the first plausible solution from winning by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change: clearer instructions, a process change, a template, training, or use of an existing capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For an ambiguous or high-impact problem, expand the candidate set before narrowing. Keep each option concise: what it is, what it solves, major costs, important risks, and reversibility.

### Technical design principles

- Prefer one understandable execution path over special cases that vary by runtime condition.
- Validate inputs and invariants strictly. Fail clearly when an invalid state indicates a defect; do not silently convert bugs into plausible output.
- Prefer established conventions over new abstractions, and new abstractions over permanent configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed without widespread entanglement.
- Use familiar, proven technology and existing infrastructure unless a new tool clearly earns its cost.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is a stated requirement.
- Avoid quick fixes that bypass the appropriate system boundary.

## 6. Evaluate and recommend

Compare viable options against the criteria. Provide a concise proposal with:

- Problem statement and current impact.
- Evaluation criteria.
- Options and material tradeoffs.
- One clear recommendation and why it is preferred.
- Key risks, assumptions, irreversible consequences, and open decisions.

Use a durable shared documentation system when review, approval, or future reference is needed; otherwise use the current workspace. Use a clear title such as `DD MMM YYYY: Solve — [topic]`.

**Recommendation gate:** Do not implement a hard-to-reverse choice without explicit approval. If the user requested analysis only, stop here.

## 7. Plan, implement, and verify

For larger work, prepare an implementation plan before changing the system. Include scope, ordered steps, affected components, dependencies, migration or rollback strategy, test strategy, release steps, monitoring, and follow-up ownership.

Implement the approved solution using the project's conventions. Run relevant automated tests, static checks, and focused manual verification. Verify both normal behavior and meaningful failure behavior.

### Completion audit

Before declaring completion, check:

- The delivered behavior addresses the stated problem and evaluation criteria.
- Existing critical behavior remains compatible.
- Tests and checks actually ran; report their results accurately.
- Errors are visible and actionable rather than silently masked.
- Security, privacy, and access boundaries remain appropriate.
- Rollback, removal, or operational recovery is understood where relevant.

Do not claim success based solely on code changes or a successful build.

## 8. Hand off

Report the outcome in operationally useful terms:

- What changed and what user outcome it enables.
- Verification performed, results, and anything not verified.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change record when applicable.

Keep the handoff focused. Separate confirmed results from assumptions, and state clearly if implementation is blocked pending a decision, authorization, or missing information.


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
description: Search the minimum set of relevant, authorized sources and turn the findings into a clear, evidence-linked context brief for a person, organization, project, topic, or decision.
---

# Gather context

Use this workflow when someone needs to get up to speed before writing, deciding, meeting, pitching, planning, hiring, or taking another consequential action. The result is a concise, well-sourced context brief that helps the user act; it is not a raw search dump.

## 1. Establish purpose, authority, and audience

First identify the action, decision, or question the research must support. Examples include preparing for a partner conversation, understanding the current state of an initiative, assessing options for a project decision, or reviewing a candidate’s role-relevant background.

Before searching private systems, confirm all of the following:

- There is a legitimate organizational, professional, or personal purpose.
- The user is authorized to access the proposed sources and use them for that purpose.
- The intended audience is permitted to receive the resulting information.
- The requested scope is proportionate to the decision and its stakes.

For research about a person, use a stricter minimum-necessary standard:

- Search only sources likely to contain information relevant to the stated purpose.
- Do not inspect private messages, journals, recordings, personnel material, or other sensitive records merely because they are available.
- Omit unrelated personal details, sensitive characteristics, and speculation.
- Do not infer private attributes from limited evidence.
- For hiring or assessment, focus on role-relevant capabilities, work evidence, role alignment, and whether an assessment distinguishes relevant performance.
- Keep the brief within the appropriate access boundary. Do not place restricted findings in a broadly accessible location.

If the purpose, authorization, intended audience, or subject identity is unclear, ask one focused question before accessing private information. Do not over-question a request that is otherwise clear.

## 2. Scope the research before searching

Right-size the effort. The two main failure modes are equally harmful:

- **Over-gathering:** searching every connected system, creating excessive parallel work, and producing a long report for a simple status question.
- **Under-gathering:** relying on one convenient source when the relevant history, decision, or agreement is likely elsewhere.

Choose an effort level based on wording, stakes, time sensitivity, and the likely cost of being wrong.

### Quick

Use for requests such as “remind me,” “where are we,” or a narrow status check. Search one to three obvious sources, use one or two strong queries per source, and return a few concise findings. Search directly rather than creating unnecessary parallel tasks.

### Standard

Use for ordinary preparation for a meeting, decision, outreach, or project update. Search several relevant sources, follow meaningful leads, and write a compact structured brief. Parallelize only when it materially reduces delay.

### Deep

Use for high-stakes decisions, major commitments, sensitive negotiations, senior hiring, material investments, or complex strategic work. Search broadly across relevant source categories, run multiple queries per category, retrieve primary records, verify important claims, and resolve contradictions.

When uncertain, start with the lighter reasonable tier and offer to extend the review. State the selected scope briefly so the user can redirect it. For example: “I’ll do a quick review of the obvious internal records and public information; I can expand this into a deeper sweep if needed.”

Set a time window as well. A useful default is recent activity plus enough older history to explain the current state. Extend farther back when the relationship, project, or decision has a long history.

## 3. Classify the subject and select sources

Classify the request before choosing systems. A source is worth searching only when a sensible researcher would expect it to contain decision-relevant evidence for this particular request.

- **Person:** relevant correspondence, collaboration messages, meeting records, calendar history, authorized relationship records, and public professional information. Include hiring systems only for a legitimate hiring-related purpose.
- **Organization:** current public materials first, then internal correspondence, partnership records, prior meeting notes, and authorized pipeline or relationship records.
- **Project or initiative:** project documents, work-tracking records, team messages, decision logs, shared files, code repositories where relevant, and product or operational metrics when relevant.
- **Topic or question:** public research plus internal strategy documents, prior analyses, team discussions, and technical records where they bear on the question.
- **Decision:** gather evidence around the options, decision criteria, owners, constraints, risks, and arguments for and against each option.

Named sources are mandatory, not exhaustive. If the user requests email and public research, search both. Add another source only when it is clearly likely to contain material evidence, such as a meeting record discovered through a calendar entry or message thread.

If a recent meeting with the subject appears likely, especially one in the current week, retrieve authorized notes or a transcript. Meeting records often contain the clearest account of what was agreed, requested, or deferred. Attribute speakers carefully: labels such as “me” or “participant” may not uniquely identify a person.

## 4. Search systematically and proportionately

Use the capabilities available in the user’s environment. Typical source categories include:

- Email and direct correspondence.
- Team chat and discussion threads.
- Shared documents, knowledge bases, and file storage.
- Calendar events, meeting notes, and authorized transcripts.
- Relationship-management, applicant-tracking, project-tracking, or operational databases.
- Product analytics or operational metrics.
- Source code and version history for engineering questions.
- Public web sources, including official sites and current professional profiles.
- Approved internal memory or prior briefs, treated as leads rather than unquestioned truth.

For a standard or deep review, search from multiple useful angles: the subject’s name, organization, project name, alternate names, related people, relevant decision terms, and dated milestones. Read the primary record behind high-value search results rather than relying solely on snippets.

When opening a multi-part document, inspect all tabs, sections, pages, and relevant attachments. Some document tools expose only the first section by default. Record which section supports each material finding.

For public research, prefer official and current sources for role, status, funding, product, or policy claims. Cross-check time-sensitive facts against current primary sources or reliably dated professional profiles. Include a direct evidence link only when it was supplied by the user or verified directly. If a useful source cannot be verified, omit the link and state the limitation.

For structured databases, first understand the relevant schema, table purpose, field definitions, and known data-quality limits. Route searches to the table most likely to be canonical rather than crawling every database. Treat stale, incomplete, or low-confidence records as supporting evidence rather than definitive truth.

## 5. Handle unavailable sources honestly

Do not silently substitute one source for another. If a source was judged relevant but returns no results, is inaccessible, or fails technically, say so in the brief.

Distinguish among:

- A source deliberately skipped because it was not relevant.
- A relevant source searched with no meaningful results.
- A relevant source that could not be searched.

Attempt safe, tool-appropriate diagnostics before asking the user to intervene: check source configuration, permissions, authentication state, supported search syntax, and service availability. Do not expose credentials or ask users to share secrets. If user action is necessary, name the exact remaining action and explain the resulting evidence gap.

## 6. Evaluate and reconcile evidence

Prefer evidence in roughly this order:

1. Primary records and current official decisions.
2. Direct correspondence, meeting notes, and original documents.
3. Current public statements and reliably dated professional information.
4. Internal summaries, database fields, and secondary reporting.
5. Search snippets, unverified claims, and recollections.

Resolve contradictions rather than listing incompatible claims without analysis. State what conflicts, why one source is more reliable or recent, and what remains uncertain. For example, an older article may list a leader at one organization while a current professional profile and recent meeting record indicate a later move. Report the stronger current evidence and note that the older material appears stale.

Separate facts, reasonable inferences, and open questions. Do not turn absence of evidence into evidence of absence unless the searched sources and time window make that conclusion justified.

## 7. Write the context brief

Organize the brief by what the user needs to understand, not by the systems searched. Lead with the findings that affect the next action.

Use this adaptable structure:

```markdown
## [Subject] — context brief
*Scope: [effort level]. Sources reviewed: [categories]. Window: [dates].*

## TL;DR
- [Most decision-relevant finding with direct evidence link.]
- [Current state, decision, or risk with direct evidence link.]
- [Key implication for the user’s next action.]

## What we know
### [Theme]
[Synthesized finding with direct evidence links.]

### [Theme]
[Synthesized finding with direct evidence links.]

## Relationship or timeline
[Relevant chronology of contact, decisions, milestones, or changes.]

## Open questions and gaps
- [Unanswered question and the source most likely to answer it.]
- [Relevant source unavailable, empty, or not searched, with reason.]

## Sources
- [Primary source title and direct evidence link]
- [Supporting source title and direct evidence link]
```

Every factual claim drawn from a source should include a direct, clickable path to the underlying evidence where the system supports it. Link to the message thread, document, meeting record, database entry, or verified public page, rather than merely to search results. Keep quotations short and necessary; paraphrase where possible.

Calibrate length to the chosen effort level. A quick brief may contain only a short summary, key facts, and gaps. A deep brief may include a fuller timeline, competing options, evidence quality, and a detailed source list. Keep paragraphs short enough to scan and act on.

## 8. Deliver the brief safely

Return short briefs directly in the conversation when appropriate for the sensitivity of the material. Create a longer reference document only in a user-approved shared location with access controls appropriate to the sources used.

Use a clear, human-readable title with a date when useful, such as “Current partnership background and open decisions.” Avoid file-like slugs and vague labels.

When editing an existing formatted document:

- Insert into a known normal body-text location or replace an entire verified section.
- Do not insert ordinary text at the start of an existing heading, list item, or table cell where it may inherit incorrect formatting.
- Re-read the affected content after insertion and verify paragraph and list styles.
- If visual layout matters, render or inspect the document before reporting completion.

The brief itself should be the final deliverable. If offering a follow-on task, such as drafting questions, an outreach note, or a decision memo, offer it before the brief rather than appending unrelated commentary afterward.

## Final audit

Before sending, check:

- The effort level matches the user’s actual need.
- Private sources were searched only for an authorized, legitimate purpose.
- Sensitive or irrelevant personal information is omitted.
- Relevant recent meetings were considered.
- Important claims are current, attributed, and linked.
- Contradictions are explained rather than hidden.
- Relevant unavailable or empty sources are disclosed.
- No link, source access, or fact was invented.
- The output is organized around action and decision relevance.


---
name: learning-tutor
description: Learn a paper, article, post, or topic through a short Socratic dialogue that builds durable understanding with retrieval, explanation, challenge, and application rather than passive summary.
---

# Learn with a tutor

Help the learner understand, retain, evaluate, and use a provided paper, article, post, or topic through a rigorous dialogue. Prioritize active recall and reasoning over explanation: the learner should do most of the intellectual work, while the tutor guides, diagnoses, and raises the level of challenge.

## Learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to recall and reconstruct ideas in their own words.
- **Ask for mechanisms.** Move beyond stated conclusions: ask why, how, under what conditions, and based on what evidence an idea should hold.
- **Have the learner generate connections.** Ask for their own examples, analogies, predictions, and applications before supplying any.
- **Use productive difficulty.** Make the task demanding enough to require thought, but not so difficult that the learner cannot make a meaningful attempt.
- **Practice transfer.** Connect the source to unfamiliar cases, related ideas, and real decisions.
- **Reveal gaps through questions.** When an answer is incomplete or inconsistent, use a focused question to help the learner notice the issue. Explain directly only after they have had a fair chance to reason it through.

## Conversation workflow

### 1. Establish prior knowledge and a learning target

Begin by asking what the learner already knows, believes, or has experienced about the topic. Also ask what they want to be able to explain, evaluate, or do by the end.

Ask one or two open questions, such as:

- “What do you already think is true about this topic, and why?”
- “What is your current best explanation of this idea?”
- “What are you hoping to understand or use after this conversation?”

Use the response to identify useful background knowledge, possible misconceptions, and an appropriate level of challenge.

### 2. Elicit the central idea from memory

Ask the learner to explain the core argument, finding, or concept without quoting the source.

Useful prompts include:

- “In your own words, what is the main claim?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “If you had 30 seconds to explain this to a thoughtful friend, what would you say?”

If the learner has not read or engaged with the material yet, first ask for a prediction or working model. Then ask them to inspect the relevant section before returning to retrieval.

### 3. Choose a few important ideas and go deep

Do not attempt to cover every detail. Select two or three ideas that are central, difficult, consequential, or likely to be misunderstood.

For each idea, use this cycle:

1. Ask the learner to reconstruct the idea.
2. Probe their reasoning, evidence, assumptions, and causal story.
3. Ask them to generate an example, comparison, or application.
4. Test the idea with an objection, boundary case, or alternative explanation.
5. Adapt the next question to their actual response.

Keep turns short. Usually ask only one or two questions at a time.

## Question toolkit

Choose questions that require explanation, not simple recognition. Adapt the wording to the material and the learner’s level.

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What evidence would distinguish this explanation from another one?”
- “What is the mechanism here, step by step?”
- “Can you construct a concrete example from a familiar setting?”
- “Where might this fail, or where would it not apply?”
- “What is the strongest objection to this argument?”
- “How does this connect to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one assumption changed?”

Avoid questions answerable with only “yes” or “no.” If such a question is useful, immediately ask for the reasoning behind the answer.

## Responding to answers

Be warm, direct, and specific. Avoid generic praise. When an answer is strong, identify what made it useful—for example, it named an assumption, separated correlation from causation, or supplied a relevant counterexample—then raise the challenge.

When an answer is incorrect or incomplete:

1. Do not immediately provide the correction.
2. Ask a focused follow-up that exposes the tension or missing step.
3. Give the learner one or two genuine attempts to revise their reasoning.
4. If they remain stuck, provide a concise explanation of the missing distinction.
5. Ask them to restate the corrected idea or apply it to a new case.

If the learner says, “I don’t know,” do not immediately rescue them. Invite a low-stakes attempt:

> “Take a guess based on what you do know. What seems most plausible, and why?”

Offer a hint after an attempt, or earlier when the task clearly requires knowledge the learner has not had an opportunity to acquire.

## Calibration and pacing

Increase difficulty when the learner answers easily. Ask for a counterexample, a comparison, a prediction, a stronger objection, or an application in a new domain.

Reduce difficulty when the learner is lost. Narrow the question, isolate one assumption, use a simpler case, or ask them to compare two explanations and defend one. Do not turn challenge into frustration.

Match the learner’s energy. When they are engaged, pursue the reasoning further. When they are tired or overloaded, consolidate the strongest ideas rather than introducing more material.

Maintain a dialogue, not a fixed quiz. Each question should build on what the learner actually said.

## Progress checks

Periodically give a brief, evidence-based assessment of:

- What the learner has demonstrated they understand.
- What remains uncertain, incomplete, or confused.
- The most useful next focus.

Do not treat recognition of a term or repetition of a conclusion as mastery. Look for accurate explanation, sound reasoning, and successful transfer to a new case.

## Closing gate

Before ending, ask the learner to turn understanding into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation, example, or future retrieval prompt. End by identifying the next concept or question that would be most valuable to revisit.

## Guardrails

- Do not summarize the material unless the learner explicitly requests it; even then, invite their own summary first.
- Do not lecture when a well-chosen question can make the learner retrieve or infer the point.
- Do not define jargon automatically; first ask the learner to define it, then clarify if needed.
- Do not make the interaction easy merely to be encouraging.
- Do not cover an entire source superficially when a few core ideas can be understood deeply.
- Keep the learner’s own goals and context in view, and avoid requesting personal details that are unnecessary for the learning task.


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
description: Draft, revise, and audit professional social posts from source material or a topic, emphasizing concrete claims, strong hooks, useful substance, and targeted revision.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, an existing draft, an article, a transcript, a podcast, research findings, or a simple topic.

The aim is not to make an announcement sound enthusiastic. The aim is to make the right reader stop, understand a useful point, and have a reason to care. Write for a defined professional audience with low tolerance for fluff, generic inspiration, vague claims, and empty calls to action.

This workflow is platform-independent. Adapt it to the user’s chosen platform, publishing process, brand guidance, and access permissions.

## Start with a brief

Before drafting, ask for or confirm the following. Do not make private assumptions about the writer, organization, audience, or publishing tools.

- **Platform and format:** text post, caption, carousel or document caption, thread, short video script, or article promotion.
- **Audience:** for example, technical practitioners, founders, policy professionals, researchers, customers, operators, candidates, or community members.
- **Purpose:** share an insight, explain a concept, announce a change, promote longer work, start a substantive discussion, or support a campaign.
- **Voice:** first-person, team, or organizational voice; formal or conversational tone; preferred and prohibited language; punctuation and formatting preferences; target length.
- **Evidence and permissions:** sources supporting claims, and permission to use names, quotes, images, career outcomes, testimonials, or personal stories.
- **Link plan:** whether an external link is needed and where the selected platform’s current publishing strategy places it.
- **Delivery method:** whether the user wants the draft in chat, a plain-text document, a content-management system, or another authorized workspace.

If the user supplies a style guide, prior approved posts, audience research, or brand guidance, use it. If the workflow needs access to private messages, internal documents, customer records, or information about identifiable people, confirm a legitimate purpose and clear authorization first. Use only the minimum relevant source material. Exclude unrelated personal information, sensitive details, and anything outside the intended access boundary.

## Route the request before drafting

Some post types need different structures. Identify the genre before selecting a hook or template.

- **Career or participant case study:** A person’s before-and-after story involving a program, employer, career move, or other development. Use a case-study structure: starting point, turning point, concrete outcome, evidence, and lesson. Confirm what may be named, quoted, or disclosed.
- **Research or evidence post:** A claim based on data, modeling, surveys, reports, or analysis. Prioritize methodology, source quality, uncertainty, and a conclusion that the evidence actually supports.
- **Product or organizational announcement:** Lead with the concrete change and why it matters to readers. Do not lead with internal excitement.
- **Article, report, or podcast promotion:** Lead with the strongest finding, argument, or guest insight, not “new article” or “new episode.”
- **Carousel or document caption:** Give one or two meaningful findings, then explain what the visual material adds. Do not repeat every slide.
- **Hiring or assessment post:** Focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Avoid vague claims about “culture fit” or personal worth.

If the genre is unclear, ask one concise routing question before writing. If it is a sensitive case study, do not proceed until disclosure boundaries are clear.

## Non-negotiable accuracy and privacy rules

1. **Do not invent facts.** Do not fabricate statistics, names, organizations, job titles, dates, quotations, testimonials, outcomes, research findings, or sources.
2. **Separate evidence from interpretation.** State what the source shows, then label the conclusion, recommendation, or hypothesis clearly.
3. **Preserve meaningful uncertainty.** If evidence has large ranges, weak data, important assumptions, correlation rather than causation, or disputed interpretation, say so plainly.
4. **Use exact details only when supported.** Specific figures, dates, roles, and outcomes are stronger than broad language when they are accurate. Do not turn estimates into false precision.
5. **Ask for missing support early.** If the post depends on an unsupported claim, request a source, remove the claim, or narrow it.
6. **Respect consent and context.** Do not expose private career history, health information, personal communications, or sensitive background details merely because they make a stronger post.
7. **Avoid misleading urgency.** Do not inflate stakes to create engagement. A specific risk, clear mechanism, and proportionate response are more credible than alarm.

## Audience and voice

Write for the reader most likely to benefit from or act on the post, not for everyone who might vaguely relate to it. Specificity is a filter: it helps the right reader recognize that the post is for them.

Use this default voice unless the user supplies another one:

- Direct, clear, and conversational.
- Short sentences with concrete nouns and verbs.
- Active voice where it improves clarity.
- One main claim per sentence.
- Sober about problems and practical about responses.
- Specific rather than promotional.
- Confident only where the evidence supports confidence.

Avoid these common failure modes:

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are thrilled to announce an exciting initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences full of unexplained terms. | State the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Broad catastrophe language without a clear mechanism or response. | Name the specific risk, the evidence, uncertainty, and a useful intervention. |
| Generic motivational | “Success comes from embracing change.” | Name the decision, trade-off, example, or result that makes the point useful. |

## The core workflow

### 1. Inspect the source before choosing a format

Do not start with a template. Read the source material and find the strongest material inside it.

Look for:

- An unusual or surprising fact.
- A specific number that creates tension.
- A counterintuitive conclusion that can be defended.
- A concrete before-and-after outcome.
- A meaningful trade-off or deliberate constraint.
- A sharp disagreement between credible views.
- A useful framework, checklist, or model.
- A sentence that changes how a reader sees the problem.

The formal headline of an article is often not the best social-post angle. The strongest thread may be a detail in the middle of the source.

If several strong angles exist, do not silently choose one. Present two to four numbered options and state what each foregrounds and why it may work for the intended audience.

**Angle-selection prompt:**

> I see several viable post angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [specific story, outcome, or disagreement]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Choose one primary thread. A social post should not attempt to summarize every section of a report or transcript.

### 2. Generate hooks before drafting the body

The opening determines whether the rest of the post is read. Generate five to ten possible hooks before committing. When user choice would help, show a numbered shortlist of three to five strong options, with one sentence on the strategic role of each.

A hook should make an honest promise that the body fulfills. It should generally work by itself, without requiring the reader to understand the source first.

Useful hook patterns include:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific body of evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Named outcome:** “[Person or role] moved from [starting point] to [specific outcome] in [timeframe].” Use only with consent and evidence.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only if the post defends it.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused question:** “Why do two credible groups reach such different conclusions about [specific issue]?”

| Hook | Strategic purpose |
|---|---|
| “[Specific claim or finding].” | Leads with a concrete result and gives the reader a reason to continue. |

Reject hooks that are interchangeable across unrelated topics. If a key noun can be replaced with “marketing,” “leadership,” or “innovation” and the sentence still works, the hook is likely too generic.

Avoid:

- Generic announcement openings such as “Excited to share.”
- Throat-clearing such as “In today’s fast-moving environment.”
- Empty cliffhangers that do not deliver a payoff.
- Several rhetorical questions in a row.
- Broad motivational claims.
- Clickbait such as “You will not believe” or “This changes everything.”

### 3. Choose one structure

Select the structure that fits the source. Do not combine several structures unless there is a clear reason.

1. **Counterintuitive claim → evidence → implication**  
   Best for research, data, and argument posts. Start with the surprise, show support, then explain what readers should reconsider or do.

2. **Changed mind → trigger → updated view → takeaway**  
   Best for thoughtful first-person posts. State the former view, explain what changed it, then give the revised conclusion.

3. **Problem → why it matters → practical response**  
   Best for explainers, policy, and operational content. Keep the problem concrete and the response proportionate.

4. **Result → how it happened → reusable lesson**  
   Best for launches, team outcomes, and case studies. The result must be real, specific, and appropriately disclosed.

5. **Framework → examples → application**  
   Best for posts readers may save and revisit. Give the framework a name only if it clarifies the idea rather than disguising ordinary advice.

6. **Specific announcement → reader relevance → next step**  
   Use only when the announcement itself is notable. Lead with what happened and its practical significance.

7. **Strategic trade-off → rationale → consequence**  
   Useful when explaining deliberate constraints or “anti-goals”: what a team or organization has chosen not to optimize for, why, and what that choice enables.

### 4. Draft the body: hook, tension, payoff

Use this default shape:

- **Hook:** The strongest claim, result, or tension.
- **Tension or setup:** Why the point matters, what is surprising about it, or which assumption it challenges.
- **Payoff:** The evidence, story, framework, or practical insight. The post should be valuable even if the reader never clicks, swipes, or buys.
- **Soft close:** Exactly one focused question, one practical takeaway, or one clear pointer to more material.

A useful default is under 300 words, but length should follow substance and platform norms. A short post still needs a complete point. A longer post needs a reason for every paragraph.

Use white space. Write in one- or two-sentence paragraphs so the post scans well on a phone. Use bullets only when the content is genuinely list-shaped, such as three reasons, four findings, or a checklist.

For a carousel or document caption:

- Establish the central idea in the post.
- Include one or two strong specifics.
- Explain what the visual material adds.
- Do not turn the caption into a slide-by-slide summary.

For a linked article, report, or podcast:

- Put the strongest finding in the post body.
- Treat the linked material as depth, sources, or extended analysis.
- Follow the user’s current platform strategy for link placement.
- Never make “read the link” the main value proposition.

## Calls to action and questions

Use one close only. A strong close gives readers a real, bounded way to respond.

Good examples:

- “Which of these constraints is most important in your work?”
- “What evidence would change your view?”
- “The full analysis includes the assumptions and source material.”
- “If you have operated a system like this, where does this model fail?”

Weak examples:

- “Thoughts?”
- “Let me know what you think.”
- Several questions at once.
- Requests to comment, tag, repost, or react merely to boost engagement.

A question should invite knowledge, disagreement, or relevant experience. Do not use engagement bait.

## Editing pass: remove templated and inflated language

Run a separate editing pass after drafting. Cut phrases that sound polished but say little.

Replace or remove:

- Corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Hedging frames such as “it is worth noting,” “one might say,” and “arguably,” unless uncertainty is genuinely necessary.
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Abstract nouns such as “journey,” “transformation,” or “paradigm,” when a concrete event can be named.
- Transition sentences that merely repeat the prior paragraph.
- Dramatic framing such as “The truth is” or “Here is the reality.” State the point directly.
- Decorative punctuation or formatting that the selected platform does not support.

If the user has a punctuation preference, follow it. Otherwise, favor periods, commas, and line breaks over theatrical punctuation. Read the post aloud. If it sounds like a generic thought-leadership template rather than a person making a specific, supported point, rewrite it.

## Revision protocol

When the user gives feedback, revise the requested line and the nearby logic first. Do not rewrite the entire post unless asked.

- If the hook is not sharp enough, provide several replacement hooks before changing the body.
- If a claim feels overstated, tighten the evidence or soften only that claim.
- If a paragraph feels slow, cut setup before adding explanation.
- If the user prefers an earlier sentence, preserve it unless there is a clear reason to replace it.
- If a line is weak because the source does not support it, say so directly and offer a supported alternative.

Multiple small options are often more useful than one complete redraft, especially for hooks, closers, and uncertain lines.

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
- Are all names, quotations, figures, and claims supported and authorized?
- Does formatting work on the intended platform?
- Does the tone remain professional, respectful, and non-inflammatory for the intended audience?
- Does the post stay within the agreed privacy, consent, and access boundaries?

If any answer is no, revise before handoff.

## Handoff format

When presenting the work, provide only what helps the user decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen delivery format or authorized location.
3. Any unsupported claim, missing input, or line that remains uncertain.
4. Suggested link or first-comment text, if relevant to the chosen platform strategy.
5. A concise publishing reminder appropriate to the platform, such as responding promptly and substantively to genuine comments.

Do not claim that a particular format, timing tactic, or engagement metric is guaranteed to improve reach. Platform behavior changes frequently. Treat distribution advice as a testable hypothesis and compare results across several posts.

## Common failure patterns

- **Announcement disguised as content:** The post says the organization is pleased but never explains why readers should care. Lead with the actual change or lesson.
- **Pure teaser:** The post asks readers to click but offers no useful insight. Share the main finding and use the linked piece for depth.
- **Unsupported precision:** The post uses a striking figure without source, scope, or caveat. Verify, qualify, or remove it.
- **Generic inspiration:** The post sounds positive but has no mechanism, example, or decision. Name the concrete action or trade-off.
- **Overpacked summary:** The post covers every section of a report. Select one thread and save the rest for the original material or future posts.
- **Bolted-on promotion:** A product, course, or service appears at the end without a natural connection. Remove the pitch, create a separate promotional post, or make the connection concrete and immediate.
- **Forced engagement:** The post demands reactions or comments. Ask one real question or end with a useful conclusion.
- **Overexposure:** The post reveals more about a person, client, employee, or participant than is necessary. Remove identifiers and sensitive detail unless they are essential, authorized, and appropriate for the audience.

The final standard is simple: the post should sound like someone with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, or a generic social-media template.


---
name: case-study-post
description: Create an evidence-based case study post about a person’s professional change, learning experience, or current work. The workflow produces a review-ready social post, alternate hooks, quote-card options, approval flags, and a publishing QA.
---

# Write a case study post

Use this workflow to turn source material about a person into a concise, credible public case study. It works especially well for professional social posts, and can be adapted for newsletters, community updates, program pages, recruitment stories, or alumni profiles.

The aim is not vague praise. Show a real, supportable change: where the person started, what they were considering, what they did, what concretely helped, what happened next, and what the reader can do.

A good case study gives readers a reason to recognize themselves in the subject’s earlier situation. It explains the mechanism behind the outcome without claiming that one program, community, or person caused everything.

## Purpose, authorization, and access boundary

Before using interviews, applications, internal messages, or professional records, confirm that there is a legitimate publishing purpose and clear authorization to use them. Use only the minimum relevant material.

- Confirm whether the subject has agreed to a public story, a named story, or an anonymized story.
- Use sources that the publisher is authorized to access.
- Do not include unrelated personal information, private contact details, health information, family details, immigration status, compensation, or confidential work unless it is necessary, approved, and appropriate for the intended audience.
- Respect the subject’s preferred public name, pronouns, role description, and privacy expectations.
- Keep internal notes, evidence logs, and drafts within the appropriate access boundary.

If the available evidence does not support public use, pause and ask for approval or use a different story.

## Inputs

Ask for all available, relevant source material. This may include:

- An interview transcript, meeting notes, or written Q&A
- An application, intake form, or survey response
- A current professional profile or approved biography
- Public work samples, project pages, publications, or announcements
- An internal message reporting a result, if its use is authorized
- Notes from the subject or a prior draft
- The target audience, platform, length, and desired call to action
- An editorial or brand voice guide
- Any restrictions on what may be named or quoted

Before drafting, build an evidence sheet. If a critical field is missing, ask focused questions rather than guessing.

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns, and naming permission |
| Before-state | Previous role, field, goal, uncertainty, or constraint |
| Trigger | Why they joined, applied, changed direction, or took action |
| Intervention | Program, community, event, mentor, resource, or product involved |
| Mechanism | Concrete events that helped, such as feedback, an introduction, a job post, or a practical resource |
| Now-state | Current role, organization or team if approved, project, output, or result |
| Timeline | Relevant start and outcome dates or truthful time spans |
| Evidence | Verified names, figures, dates, artifacts, and direct quotes |
| Cost or risk | Career change, move, pay change, uncertainty, or tradeoff, if approved |
| CTA | The action the intended reader should take |

Useful intake questions:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they act at that point?
4. What were the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a named project, output, placement, publication, product, or result that may be mentioned publicly?
8. Did they take on a meaningful cost or risk that they want to share?
9. Which facts, figures, names, and quotes are approved for public use?
10. Who should this post help or persuade?

## Evidence and verification rules

Never invent facts or strengthen a claim for effect. If the source says someone contributed to a project, do not call them the lead. If they explored an opportunity, do not say they received it. If a paper is not published, do not describe it as published.

Treat automated transcripts and summaries as useful but fallible. They can mishear names, organizations, technical terms, numbers, dates, and titles. Cross-check important details against a stronger source before publication.

Use this reliability order unless a specific case gives you a reason to depart from it:

1. The subject’s direct, recent confirmation
2. Official public records, published work, or an approved organizational announcement
3. A current professional profile maintained by the subject
4. An original application or written statement from the subject
5. Interview transcripts and meeting notes
6. Informal third-party messages

In working notes, separate three types of statement:

- **Verified fact:** A role, date, figure, output, or quote supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn from the story. Use only when evidence supports it, and phrase it carefully.

Do not claim that a course, network, mentor, or resource caused an entire career outcome unless that causation is clearly established. Prefer precise language such as “the program helped them see the field differently,” “they learned about the opportunity through the community,” or “feedback improved their application.”

## Sensitive-content gate

Flag the following for explicit subject approval before publication:

- Salary, pay cuts, financial hardship, or compensation comparisons
- Health, family, legal, immigration, or other sensitive personal circumstances
- Strong criticism of a former employer, team, role, or career decision
- Unreleased projects, unpublished titles, confidential work, or private client information
- Direct quotations, especially forceful opinions
- Claims about why an employer selected the subject
- Claims of impact or causation that cannot be independently verified
- Details that could expose private timing, location, or identity information

If approval is unavailable, use an honest fallback only if it remains approved. For example, replace an exact pay figure with “they accepted a lower-paying role” only when that broader statement is true, useful, and authorized. Do not conceal uncertainty by making the story more dramatic.

## Build the story beats

Create a concise private outline before drafting. Do not publish the outline unless the user asks for it.

### 1. Before-state

Capture the subject’s role, background, and reader-relevant uncertainty. Include the alternative path they were considering when it resembles the audience’s present situation.

Keep only details that move the story. A list of credentials, reading habits, or past roles usually weakens the post. Retain a detail when it makes the decision understandable or makes the change feel real.

### 2. Trigger

Identify why the subject acted then. They may have wanted to test whether a career path was open to them, learn a field, find collaborators, solve a practical problem, or make a values-based choice.

### 3. Mechanism

Find one or two observable events that helped move the story forward. Good mechanisms include:

- Realizing that a field or role was accessible
- Seeing a relevant opportunity through a community
- Having a conversation that clarified next actions
- Receiving feedback that strengthened an application or project
- Getting an introduction to a relevant person or team
- Using a workshop, resource, or practical tool

Avoid “the experience was transformative.” Name what happened instead.

### 4. Now-state

Record the current role, approved organization or team name, and what the person actually does. Translate specialized language enough for the intended reader to understand why the work matters.

Use a named output only when it adds proof or interest. One meaningful project, publication, product, grant, or placement usually works better than a long list of credentials.

### 5. Timeline and compression

Map the sequence from the intervention to the result. Use a short, truthful timeframe when it sharpens the story, such as “within six months” or “the following year.” Do not force a compressed timeline when the facts do not support it.

### 6. Quotes

Pull three to five candidate quotations verbatim. Prefer lines that reflect the reader’s identity, uncertainty, or motivation, not only the subject’s achievement.

Look for these categories:

1. **Discovery:** “I did not know this path was open to someone like me.”
2. **Mechanism:** “I found the opportunity through the community.”
3. **Conviction:** “I would make the same choice again.”

Light trimming is allowed only when it preserves the speaker’s exact meaning and grammar. Never rewrite a quote into words the person did not say.

## Generate three hook options

For feed-based platforms, the first two lines determine whether someone reads further. Draft three distinct hooks before drafting the body. Keep each to two short sentences. For short-form professional platforms, aim for about 140 characters total when practical.

### Hook A: Discovery

Use this when the audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a concrete mechanism.

This is the usual default because it mirrors the reader’s uncertainty.

### Hook B: Identity collision

Use this when the before-and-after contrast is vivid.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This can work well for a broad audience that does not share the subject’s exact starting point.

### Hook C: Stakes-led

Use this only when an approved cost or risk is meaningful and the audience will see it as honest context rather than a warning.

**Formula:** The subject accepted a specific cost to do something. Now they are taking a concrete action or doing meaningful work.

Avoid this approach if it makes the path appear inaccessible or if a discovery hook would better invite readers in.

Recommend one hook. Give one sentence explaining why it fits the target audience, then one sentence each on why the other two are less suitable.

## Draft the post

Aim for roughly 160 to 220 words unless the chosen platform needs a different length. Shorter is usually stronger.

Use this sequence:

1. **Hook:** Use the recommended option.
2. **Before-state:** One short paragraph about the previous situation and a relevant alternative path.
3. **Name the intervention:** State clearly that they joined the program, used the resource, or participated in the community. Do not make the mechanism implicit.
4. **Mechanism and outcome:** Explain the concrete turning points and land the immediate result in plain language.
5. **Current work:** Describe what they do now and why it matters in understandable terms.
6. **Optional cost:** Include only if approved and genuinely useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already carried by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

For platforms where external links may reduce distribution or interrupt reading, consider placing the link in a first comment, profile destination, or other designated location. Treat this as a platform-specific publishing decision, not a universal rule.

## Style rules

Adapt to the selected editorial voice. If no voice guide is available, use these defaults:

- Use short paragraphs and whitespace for scanning.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use concrete names, roles, dates, and figures only when verified and approved.
- After the initial introduction, use the person’s preferred short name when that fits the tone and consent.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not call someone exceptional, inspiring, or brilliant without showing relevant evidence.
- Use contractions if the voice is conversational.
- Keep the CTA in full second person: “If you are…” and “you can…”
- Avoid emojis unless they are an explicit brand choice.
- Default to periods, commas, and line breaks rather than em dashes.

On the final pass, remove common machine-like phrasing: empty transitions, dramatic setup frames, filler intensifiers, hedging, abstract nouns that replace evidence, balanced “on one hand/on the other hand” constructions, and reflective summaries after the CTA.

Avoid corporate or vague phrases such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm” unless they are necessary in an approved direct quote.

Read the post aloud. If it sounds like generic thought leadership, shorten it and replace abstractions with facts.

## Graphic quote options

Provide three quote-card options for a visual asset. Each should be self-contained, ideally under 15 words, and taken verbatim from approved source material.

Offer one from each category:

- Discovery
- Mechanism
- Conviction

Recommend one option. Discovery quotes often work best because they need less context and mirror the reader’s possible uncertainty. Choose a mechanism or conviction quote only if it is clearer and more memorable on its own.

## Readiness audit

Before sending the draft for review, check:

- Is every name, role, date, figure, title, and output verified?
- Were important transcript-derived details cross-checked?
- Is there a legitimate purpose and authorization for the information used?
- Does the post use only the necessary personal information?
- Does it show a concrete mechanism, not merely a result?
- Does it avoid overstating causation?
- Is the intervention named clearly?
- Does the opening reflect a real audience concern?
- Is current work understandable to a non-specialist reader?
- Have sensitive claims and direct quotes been flagged for approval?
- Is the CTA clear and directed at the intended reader?
- Are unsupported superlatives, corporate phrases, generic filler, and excessive em dashes removed?

## Delivery format

Create the draft in the user’s chosen document system if one is available. Use a clear title format such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and the two alternatives
- The three graphic quote options and a recommendation
- Items needing approval before publishing
- Missing information that would materially strengthen the draft
- The document location or link, if applicable

Do not treat the first draft as final. If feedback says “make the hook better,” generate new hooks rather than making minor adjustments to the first set. If asked to make the post shorter, cut secondary biography first while preserving the mechanism and outcome. If a subject rejects a sensitive line, replace it with the approved fallback without weakening the overall story.

After the final version is accepted, review feedback for reusable lessons. Update the workflow only when a recurring pattern is clear, such as a missing intake question, a repeated verification issue, or a consistent editorial preference. Do not invent process changes after a clean review cycle.


---
name: create-editorial-cover-images
description: Create eight article-specific editorial cover-image options through a two-round process: five distinct concepts, visual review of rendered results, and three evidence-based improvements using a user-chosen image generator.
---

# Create editorial cover images

Turn an article into eight finished cover-image options. Develop five distinct concepts, generate and inspect every result, then create three improvements based on what actually worked. The user chooses from finished images that have a clear visual and emotional connection to the article.

Use the user’s chosen image generator, publishing destination, and delivery method. Do not assume a particular service, account, visual medium, palette, or aspect ratio. If the user explicitly asks for prompts only, use the prompt-only branch instead of generating images.

## Purpose, permissions, and scope

Use the complete article as the creative source. If the article is unpublished, private, or contains personal information, confirm that the user is authorized to use it for this purpose. Use only the minimum text and facts needed to create the visual brief. Do not send the whole article to an external generator unless that is necessary, authorized, and expected by the user.

Do not invent factual scenes, personal histories, locations, events, or identities that the article does not support. A cover image may be metaphorical, but it should not imply that a fictional visual is documentary evidence. Avoid unrelated sensitive details, recognizable private individuals, logos, or confidential material unless the user has clearly requested and authorized their use.

If the intended output involves a real person, make the representation appropriate to the article’s purpose and audience. Use an anonymous or non-identifying depiction when a specific identity is unnecessary.

## Establish the creative brief

Read the complete article before developing concepts. A title alone is rarely enough to distinguish an image that belongs to this piece from a generic illustration of its topic. If the copy is missing, ask for it before beginning.

Identify the following privately as working notes:

- The **central move**: the idea, realization, or change in perspective the reader should take away.
- The **emotional progression**: where the piece is quiet, tense, hopeful, reflective, challenging, or conclusive.
- The **concrete images, actions, and metaphors** already used in the writing. These often make stronger visual anchors than invented imagery.
- The **tone of voice**: for example, sober, playful, urgent, reflective, celebratory, or defiant.
- Any factual, ethical, or representational constraints that affect the image.

Use this analysis to make the concepts specific. Do not begin by giving the user a long article summary unless they ask for one.

Reuse preferences that the user has already supplied. Ask only for missing choices that would materially change the result. Ask related questions together and collect all outstanding answers before treating a partial reply as the full brief.

1. **Mood:** Offer three or four interpretations grounded in distinct beats of this article. Explain what each one emphasizes. For example, an article about recovering confidence might support a quiet rebuilding mood, a forward-motion mood, or a hard-won hopeful mood.
2. **Subject:** Offer suitable approaches such as a human figure, landscape only, a single symbolic object, an interior scene, or an abstract composition. Respect restrictions on people, settings, objects, or realism.
3. **Palette:** Offer a few palettes that support the article and the chosen mood. Describe contrast, value, and lightness as well as naming colors, so the choice remains clear for people who do not distinguish colors in the same way.
4. **Orientation:** Establish the final placement and crop. Common options include a wide header, square social preview, portrait cover, or a user-supplied size. Verify destination dimensions when possible rather than assuming that one publishing format fits all.
5. **Medium or style:** If the user has not already chosen it, establish whether the image should read as photography, painting, illustration, collage, printmaking, or another medium.

Keep a short working brief with the agreed mood, subject restrictions, palette, medium, format, intended destination, and generator. Carry it through both rounds. Do not repeatedly ask for the same preferences during iteration.

## Propose five distinct concepts

Present exactly five ideas in a numbered list. Each idea must include:

- A short title.
- A one- to three-sentence description of what the viewer sees.
- A brief statement of the article idea or emotional beat that the concept expresses.

The concepts must be meaningfully different. Vary subject, scale, composition, visual metaphor, and emotional emphasis. Five slight variations of one scene are not a useful range.

Unless the user’s restrictions rule them out, include at least:

- One landscape-only or environment-led concept.
- One single-object or symbolic concept.

Check that every concept earns its place by connecting to this specific article. Replace any concept whose explanation could fit almost any article on the same broad topic.

Give a one-line initial recommendation, then generate all five when the requested deliverable is finished images. Do not make the user choose a concept before the first round unless they specifically ask to do so. The point of the first round is to provide real visual alternatives for comparison.

## Write strong visual prompts

Write one self-contained prompt per concept. Use concrete visual direction without overloading the generator with competing instructions. Adapt the final syntax to the chosen generator, but build each prompt from this structure:

```text
Create one image: [medium, format, and overall editorial character].

Subject: [what is visible, its action, prominence, and position. Put relevant exclusions here, such as no visible face, no logos, or no lettering.]

Setting: [surroundings, depth, layers, and foreground-to-background relationships where useful.]

Light and palette: [time of day or light direction, specifically named colors, contrast, and transitions.]

Technique: [visible traits of the selected medium, edge quality, texture, detail level, and negative space.]

Mood: [the intended emotional effect and its connection to the article’s central move.]

Composition: [focal point, eye path, placement of major shapes, crop, dimensions, or aspect ratio.]

Avoid: [only artifacts, content, or visual conventions that conflict with the brief.]
```

Name colors and relationships rather than relying only on words such as “warm,” “moody,” or “dramatic.” For example, “pale ochre ground fading into blue-grey shadow, with a muted violet horizon” is more actionable than “warm evening light.” Name colors to improve precision, but also describe brightness, darkness, and contrast so the direction does not depend only on color labels.

Describe the physical behavior of the chosen medium. A watercolor image may need wet-on-wet washes, pigment blooms, transparent glazes, visible paper, selective edges, and unpainted space. A charcoal drawing may need broad tonal masses, broken edges, and paper grain. A photograph may need a lens perspective, depth of field, natural light direction, and believable material detail.

Put important exclusions near the instruction they constrain, not only at the end. For example, say “an anonymous figure seen from behind, with no facial detail” in the subject description. Use a final avoidance list as reinforcement, not as the only place where a critical constraint appears.

Unless requested, avoid unintended lettering, logos, borders, watermarks, and interface-like elements. If the cover needs space for later typography, specify the location and character of that negative space. Do not request text rendered inside the image unless the user has explicitly approved it.

Send the generator only the visual brief required to make the image. Do not paste the full article, private correspondence, or unrelated user data by default.

## Generate the first five

Use the chosen generator’s supported workflow. Explicitly request an image so a text response is not mistaken for the deliverable. Respect access controls, spending limits, account boundaries, content policies, and live approval decisions. If the service is unavailable, report the blocker and ask before moving article material to a different service.

Maintain a working record for every option:

| Option | Record to keep |
|---|---|
| 1–8 | Title, concept, submitted prompt, generation status, output location, and visual-review notes. |

Preserve the full submitted prompt so a cut-off or failed request can be repaired accurately. Start independent jobs concurrently only if the tool safely supports it. Keep browser or interface actions sequential when they share focus or state.

For each option, verify all of the following:

1. The generator received the intended complete prompt.
2. The request became an image-generation task rather than a text-only response.
3. A real image completed and can be opened at a useful size.
4. The output location or link is real and observed, not inferred or invented.

An accepted submission, elapsed time, loading placeholder, thumbnail shell, progress indicator, or textual description is not proof of image completion. If an error appears, first check whether an image already exists before retrying, to avoid unnecessary duplicates. Keep unsuccessful attempts separate from finished options.

## Inspect all five before creating improvements

View every first-round image at a useful size. Evaluate the actual pixels, not the generator’s description and not what the prompt was meant to produce. Also inspect each result as a small preview, because a cover image must still communicate when reduced or cropped.

For each image, record:

- Whether it communicates the article’s central idea and emotional tone.
- Whether the subject or visual action reads quickly, with a clear focal point.
- Whether the requested style, palette, orientation, and composition survived generation.
- Whether it feels too busy, generic, sentimental, static, literal, or visually confusing.
- Any visible anatomy, object, perspective, texture, construction, lettering, or watermark-like artifacts.

Only after reviewing all five should you design the next three prompts. Tie every improvement to visible evidence: identify the strength to retain, the weakness to correct, and the visual change most likely to help. Do not prewrite the second round before seeing the first results.

A useful second-round spread is often:

1. A refinement of the strongest first-round image.
2. A concept combining strengths observed in two different images.
3. A new direction that fills a missing emotional or compositional gap.

Use judgment instead of forcing this pattern. The important requirement is that options six through eight are informed by inspection and add meaningful alternatives.

Fix causes rather than decorating symptoms. If an image is cluttered, reduce objects and competing focal points before adding detail. If a painting looks like a photograph with a style filter, request fewer large shapes, selective edges, and the actual marks of the chosen medium. If a scene resembles generic travel, workplace, or lifestyle imagery, reconsider the action or metaphor rather than adding ornamental detail.

Give the user a short progress update: state what the first round revealed and what the next three images will improve. Continue without asking for another selection unless the user has asked to approve each stage.

## Generate, inspect, and deliver options six through eight

Generate three new images from the revised prompts. Keep the first five available so the user can compare original directions with improvements. Inspect each new output using the same completion checks and visual criteria.

If a generation fails or returns text only, repair it where possible in the same task context. Do not count an unsuccessful attempt as a finished option. Do not silently replace a missing image with an old result, a written prompt, or a different concept.

Before delivery, verify that there are eight distinct completed outputs that you personally inspected. Check that their numbering and titles match the working record, and that each output can be accessed from the handoff method supported by the chosen generator.

Give a short recommendation naming the strongest rendered option and why it fits the article. Then provide a numbered list of all eight titles and verified output locations, clearly marking options six through eight as the second round. Keep this list as the final deliverable block.

If rate limits, access requirements, or repeated errors prevent completion, state exactly which options are finished, which are blocked, and what action is needed to resume. Preserve useful work. Never claim that eight completed images exist when some are only prompts or unsuccessful attempts.

## Prompt-only branch

When the user explicitly requests prompts only, do not generate images. Read the article, collect or reuse the same creative preferences, and propose five concepts. Wait for the user to select concepts unless they have already selected them or asked for all five prompts.

Write each selected prompt in its own fenced code block using the prompt structure above. If combining concepts, give one short line explaining the combination before the prompt. Keep the selected prompts last, with nothing after the final prompt block.

Do not describe hypothetical second-round prompts as if they were informed by visual review. Without rendered images, there is no evidence base for that stage.

## Adapt to another generator

When the user asks for a version of the same concept in another image generator, preserve the concept, mood, composition, palette, and format. Change the prompt structure only where the target tool requires different conventions.

A prose-oriented generator may work best with a compact paragraph. A parameter-oriented generator may work better with short descriptive phrases plus verified controls for aspect ratio, style, or quality. Check current supported conventions before specifying flags, model versions, or unsupported controls. If a version materially affects the prompt and remains unclear, ask once rather than guessing.

Keep platform variants separate and clearly labeled. Changing tools should not quietly change the underlying creative idea.

## Learn from completed work

After the user chooses an image, accepts a prompt, or provides clear feedback, identify reusable lessons only when the user has authorized memory or workflow updates. Favor general lessons about article interpretation, palette specificity, composition, medium constraints, or generator behavior.

Distinguish explicit user feedback from your own aesthetic judgment. Do not make one article’s subject, one person’s preferred style, or a one-off generation result into a universal default. Keep private article content and personal details out of reusable notes. If there is no durable lesson, make no update.


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
- In the final week of a month, review the current month to date and plan the next month. Clearly label it as a partial-month review and state the remaining days.
- At other times, ask whether the user wants to review the current month to date or the previous complete month.
- If the user asks only for forward planning, review first because the evidence should shape the plan. The user may explicitly choose to skip the review.

State the ranges plainly before proceeding:

> Reviewing **March 2026** (01 Mar–31 Mar). Planning **April 2026**.

Ask whether “the month” means calendar dates or a practical range that includes an overlapping partial week. Record the actual planning range in the finished plan.

## Operating rules

1. **Read first; discuss second.** Show the evidence picture before asking reflective questions.
2. **Batch independent reads.** If connected sources exist, gather independent evidence in one initial pass. Do not interrupt the conversation with repeated small lookups.
3. **Use current commitments.** Assess against the user’s live target, not an old schedule, obsolete project scope, or stale goal record.
4. **Check data quality before a harsh verdict.** Missing syncs, incomplete logs, delayed updates, and inconsistent sources may distort results. Ask the user to confirm surprising findings.
5. **Use authorized minimum necessary information.** Access private calendars, journals, health records, tasks, or communications only for a legitimate planning purpose and with clear authorization. Read only the requested date range and fields needed for the review. Do not reproduce unrelated personal details or expose them outside the user’s appropriate access boundary.
6. **The user chooses.** The assistant calculates, summarizes, identifies gaps, and holds constraints. The user chooses priorities, cuts, and commitments.
7. **One decision at a time.** Do not move to the next planning decision until the current question has a real answer.
8. **Stay at month altitude.** Define outcomes, milestones, capacity, structure, and commitments. Leave detailed weekly task blocks to a weekly planning workflow.
9. **No saved plan without explicit approval.** A plan assembled from notes is a draft, not a decision. The user must restate or materially confirm the theme and commitments, then explicitly approve it.
10. **Use explicit dates.** Use **DD MMM** format unless the user prefers another unambiguous convention.
11. **Keep records useful, not exhaustive.** Save decisions, evidence, and constraints rather than a meeting transcript.
12. **Do not lecture.** Where training, health, recovery, or personal practice is in scope, provide the numbers, direct conclusion, and agreed commitment. Give specialist advice only when asked and appropriate.

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

For large sources, return computed statistics and a few representative themes rather than raw entries. Long journals and month-long event lists can crowd out the review. Use filtered queries, aggregation, summaries, or a delegated helper when available.

If a helper is used for a large calendar, journal, or task source, give it a narrow brief: use only authorized read access, analyze only the requested date range, omit sensitive details not needed for planning, and return a concise summary rather than raw records. For a calendar, request:

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

At the end of every run, capture one precise improvement to the reusable workflow, its templates, or its data mapping. Store it in the user’s chosen workflow document or improvement log. If no suitable location exists, present the proposed edit as a short durable rule the user can save where they prefer.

Look for a read that was noisy, a wrong data assumption, a misleading metric, a question the user corrected, or a repeatable pattern future sessions should know. Prefer one specific edit over a vague reminder.

Example improvement log entry:

| Date | Observation | Durable change |
|---|---|---|
| [DD MMM] | [A source was incomplete or a planning assumption failed.] | [One precise rule for future monthly reviews.] |

## Audit checks

Before finishing, verify:

- Review and planning ranges are explicit.
- Evidence was shown before reflective prompts.
- Only authorized, relevant private information was used.
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
- Reading whole journals, calendars, or communications when aggregate measures and a few relevant themes would suffice.


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
description: Read a complete message conversation, identify the real outcome, research and pre-complete safe work, and create a durable task only when tracking will help someone finish it.
---

# Turn a message into a task

Use this workflow when a message, conversation link, email thread, or other communication may contain work that needs attention. The goal is not to copy a message into a task system. The goal is to understand the real outcome, complete as much safe preparation as possible, and leave the task owner with a small, clear next action.

Use only sources and systems you are authorized to access for a legitimate work purpose. Access the minimum information needed. Do not copy unrelated personal, employment, health, financial, or confidential details into the task, draft, or report. Keep outputs within the access boundary of the intended recipients.

## Operating principles

1. **Read before acting.** A linked reply is not the whole request. Parent messages and later replies can change, resolve, or reassign the work.
2. **Prepare rather than impersonate.** Draft communications and reversible actions where authorized. Do not send messages, emails, invitations, approvals, or public posts without explicit approval.
3. **Research selectively.** Use a few high-value sources rather than a blanket search across every system.
4. **Preserve uncertainty.** Verify facts, dates, figures, policy claims, and links. Mark missing information instead of guessing.
5. **Track only useful work.** A task record should support remembering, coordination, waiting, or deferred action—not add administration to a trivial action.
6. **Make completion easy.** The remaining human work should be obvious and small: review and send, choose an option, add a firsthand detail, or wait for a response.

## 1. Resolve the source and read the complete conversation

Start with the supplied message or link. Use the chosen communication system’s supported retrieval method to identify the message, its conversation, and its parent thread.

- If the link points to a reply, retrieve the parent and the entire thread. The linked reply identifies the initial issue, but the full thread supplies the meaning.
- If the link points to a top-level message, retrieve a narrow time window around it rather than relying on an exact timestamp match; some systems do not return results for an exact boundary. If the message has replies, retrieve the full thread immediately.
- If one or more links are supplied, run this workflow independently for each conversation unless the messages clearly concern one shared outcome.
- Open relevant attachments and linked documents. For multi-section documents, inspect every relevant tab, page, or section. A message may mention only one question while the linked document contains several decisions.

Capture these points in working notes:

- The requester, task owner, and other relevant participants.
- The current request, promise, question, decision, or dependency.
- What has already been said, agreed, or delivered.
- Explicit deadlines and credible implied timing.
- Linked documents, attachments, and referenced systems.
- Whether later messages show completion, replacement, reassignment, or a blocker.

If names are absent from an export, recover them only through authorized profiles or unambiguous context. Use a suitable name or role rather than vague wording such as “the person.” Do not expose names more broadly than the task requires.

### Completion and recency gate

Before researching or creating anything, compare the linked message with all later replies. If the work appears complete, superseded, declined, or reassigned, do not create a task. Report the evidence and ask whether tracking is still wanted only if the status remains genuinely ambiguous.

## 2. Identify the real task shape

State the task shape in working notes before researching. The shape determines what “pre-completed” work should look like.

| Task shape | What remains | Useful pre-completion |
|---|---|---|
| Reply owed | Someone needs an answer, feedback, confirmation, or recommendation | Draft a concise reply with verified facts and clear asks |
| Artefact owed | A document, introduction, reference, analysis, data pull, or other deliverable is needed | Draft or outline the artefact and gather supporting evidence |
| Decision needed | An authorized decision-maker must choose between meaningful options | Prepare options, evidence, trade-offs, and a recommendation |
| Follow-up or delegation | Someone needs to chase, schedule, assign, or coordinate work | Draft the follow-up, identify an owner and next action, or prepare a reversible handoff |
| Waiting or monitoring | Progress depends on another person, date, or external event | Record what is awaited, who owns it, and the next check date |

A conversation may contain multiple asks. Keep them in one task when they share an owner and timescale, using sub-parts in the notes. Split them only when different owners are responsible, deadlines materially differ, or one part can finish independently.

Rewrite the request as an outcome, not a message reference. Prefer “Review and send project feedback” over “Respond to project chat.”

## 3. Gather the minimum useful context

Choose sources based on the task, not habit. Use approved communication archives, document repositories, meeting notes, project workspaces, task trackers, operational data, and public research tools as appropriate.

Typical source choices include:

- **Person-related work:** relevant prior correspondence, meeting notes, documented work evidence, and role-related records. For hiring or assessment, use role-relevant capabilities, role alignment, and diagnostic evidence. Omit unrelated personal details.
- **Project or event work:** recent discussion, planning documents, prior decisions, schedules, and source files linked from the conversation.
- **Data questions:** authoritative operational data first, then relevant retrospectives or records. Read underlying records when a summary may omit important qualifications.
- **Repeated topic requests:** search authorized communications for parallel asks. Where appropriate, prepare one consistent answer and direct other requesters to it rather than duplicating effort.
- **Policy or process questions:** retrieve the applicable policy and a comparable approved precedent. Clearly distinguish established rules from a proposed adaptation.
- **Linked external material:** retrieve and read it through approved methods. Do not bypass access controls or use tools outside the authorized workflow.

For a person’s prior work, use evidence that is relevant to the current request, such as examples of deliverables, decisions, or collaboration. Do not collect a broad personal dossier merely because it is available.

Stop gathering when you can do the useful work or can name the exact missing information. Two or three well-chosen sources are usually better than many shallow ones.

## 4. Pre-complete the work safely

Do as much reversible work as is reasonable.

### Draft communications

Before drafting in someone’s voice, consult an approved style guide or prior approved examples when available. If there is no approved guide, use clear, concise, respectful language and label the text as a draft.

Keep drafts shorter than research notes. Remove unnecessary praise, long framing, repeated context, and complicated lists of questions. Ask the smallest question that unlocks progress. Make future commitments conditional when they are not guaranteed.

Use readable destination formatting. Leave a blank line before a bulleted or numbered list so the destination system renders it correctly. Avoid decorative lead-ins before a short list; move directly to the substantive point.

For money, contractual commitments, employment matters, policy exceptions, or other consequential approvals, route the draft through the established process. Do not make an informal assurance that bypasses required review.

If the system supports draft staging, place the draft in the relevant thread or approved draft location, but do not send it. Preserve the draft text or a durable draft link in the task notes so the work is recoverable.

### Prepare artefacts and decisions

For an artefact, draft the document, outline, analysis, or evidence pack to the point where remaining judgment is clear.

For a decision, provide two or three meaningful options. For each option, state evidence, benefits, risks, and constraints. End with a recommendation and why it best fits the known goals. A decision brief should support a choice, not merely list possibilities.

### Handle unknowns honestly

Never invent a date, number, URL, policy rule, or factual claim. Use visible placeholders such as:

- `[VERIFY: confirm current participant count from approved data source]`
- `[FILL IN: firsthand observation needed from task owner]`
- `[SEARCH: official policy page or approved internal record]`

Never guess a link. Verify it through an approved retrieval method or omit it. A draft with clear gaps can still save substantial work, but say plainly when it cannot be sent as written.

## 5. Ask questions only when a real fork remains

Before asking the user, check prior messages, planning documents, and recorded decisions for an existing answer. A documented position is better than requiring someone to repeat it.

Ask only when the answer changes the stance, decision, recipient, commitment, or essential content, and a wrong assumption would cost more than a question. If no meaningful fork exists, make a reasonable assumption, state it in the report, and continue.

Before questions, provide a short context recap: who is involved, what happened, what is now requested, what evidence was found, and what tension requires a choice. Ask two to four focused questions. Allow multiple selections and a custom answer when options can reasonably be combined.

| Question component | Required content |
|---|---|
| Context | Current request, relevant history, evidence, and the decision tension |
| Choice | Two or more meaningful options, plus a custom response where useful |
| Consequence | How the answer changes the draft, action, or commitment |

## 6. Decide whether a task record is warranted

Skip the record when the work is complete, duplicated, owned elsewhere, or can be finished in one short sitting with no wait or meaningful deadline. In particular, if a staged reply only needs a brief review and send, deliver it directly rather than creating bureaucracy.

Create a task record when one or more of these are true:

- Work is deferred and could be forgotten.
- There is a deadline, dependency, waiting period, or follow-up date.
- Multiple steps remain or work spans several days.
- Coordination or handoff needs a durable record.
- The user explicitly requested tracking.

When uncertain, use chat-only delivery for simple reply work and a task record for multi-step, waiting, or coordination work.

## 7. Create and verify a useful task record

Use the user’s chosen task system and current schema. Verify required field names, permitted status and priority values, categories, and linked records before writing. Do not rely on remembered identifiers, old URLs, or stale category lists.

Set:

- A specific imperative title, preferably short enough to scan quickly.
- A current status.
- An evidence-based due date only if one exists.
- Priority and urgency proportionate to the impact and timing.
- An estimate for **remaining human work**, not time already spent researching or drafting.
- The best-fit domain, project, or category when the system uses one.

Use this notes template:

```markdown
**What:** [One-sentence outcome and who is waiting.]
**Source:** [Original conversation or approved source link]
**Context:**
- [Relevant background, verified fact, or decision already made]
- [Relevant dependency or deadline]
- [Relevant supporting source]

**Pre-completed:**
[Draft reply, decision brief, artefact outline, or location of staged draft.]

**Remaining for the task owner:**
- [Specific next action]
- [Specific next action or waiting condition]
```

Keep context concise and relevant. Do not paste an entire private conversation. After creation, open or retrieve the record and confirm that fields, links, formatting, and notes saved correctly.

## 8. Report the result

If a record was created, report in this order:

1. What the task is.
2. What was pre-completed and where any draft was staged.
3. Key metadata choices: priority, urgency, due date, and remaining-time estimate.
4. Any `[VERIFY]`, `[FILL IN]`, or blockers.

If no record was needed, separate briefing from the deliverable exactly as follows. Put nothing after the reply block because users may want to copy it directly.

```markdown
## Context for the user (not part of the reply)
- [What is being asked and who is waiting]
- [Key verified facts and judgment calls]
- [Where the draft is staged, if applicable]
- [Any verification flags]

## The reply
[Draft reply verbatim]
```

## 9. Review approved outcomes and improve the workflow

When a staged draft is later sent or materially edited, compare the approved version with the staged version only if you have legitimate access and a work-related reason. Use a delayed review where the system supports it; if the message is not yet sent, check again only a limited number of times at increasing intervals, then stop. Non-sending may be intentional.

Identify durable, general lessons: preferred length, wording patterns, process routing, formatting conventions, source gaps, or system quirks. Record only non-sensitive workflow improvements in the authorized playbook or configuration. Do not silently change organizational policy, retain personal details merely to improve drafts, or make unrelated follow-ups.

## Final audit

Before finishing, check:

- [ ] Read the parent and all relevant replies.
- [ ] Confirmed the work is not already done, superseded, or reassigned.
- [ ] Used only authorized, relevant sources and minimized sensitive details.
- [ ] Identified the task shape and true outcome.
- [ ] Opened relevant linked materials and checked all relevant sections.
- [ ] Verified facts and links or marked uncertainty clearly.
- [ ] Drafted or prepared as much reversible work as possible.
- [ ] Did not send a communication or make an irreversible commitment.
- [ ] Asked questions only for a real unresolved fork, after giving context.
- [ ] Created a task only when tracking adds value.
- [ ] Verified that any created task saved correctly.
- [ ] Made the remaining human action specific, small, and visible.


---
name: design-a-work-sample
description: Create or improve a short, paid, asynchronous work sample that produces role-relevant evidence, is practical to review, and is validated through structured simulated submissions before use.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A work sample asks candidates to complete a bounded, realistic version of important work in the role. Its purpose is to generate useful evidence about role-relevant capabilities that resumes and interviews may not reveal clearly.

Use this workflow for a new exercise or a revision to an existing one. Do not use it for application-form questions, interview questions, live panels, or multi-day work trials. If the requested format is unclear, ask one focused question before continuing.

A useful work sample is not a substitute for the whole hiring process. It should assess a small number of capabilities that matter greatly to success in the role, can be demonstrated in a short exercise, and can be reviewed consistently. A poor exercise costs candidates and reviewers time while producing vague, misleading, or easily coached evidence.

## Principles and boundaries

Apply these defaults unless the hiring owner makes an informed alternative choice:

- Pay candidates for a substantive take-home exercise.
- Set a clear expected effort limit. Two to four hours is often appropriate; three hours is a useful default for roles that require both judgment and execution.
- Make the task self-contained. Candidates should not need internal accounts, private data, proprietary tools, or access to unavailable people.
- Design for approximately 20 to 25 minutes of review time per submission.
- Assess three to five observable, role-relevant capabilities, rather than broad personal qualities.
- State what AI assistance is allowed. Evaluate judgment, reasoning, and usefulness, rather than trying to infer tool use from prose style.
- Do not ask for work the organization will use commercially or operationally unless that use is specifically agreed with the candidate.
- Offer a route for reasonable accommodations or an accessible equivalent format while preserving the essential role-relevant standard.
- Use only sources and information that the hiring team is authorized to use for this role.

If role context requires private communications, performance records, or information about individuals, confirm a legitimate hiring purpose and clear authorization first. Read only the minimum relevant materials. Do not include unrelated personal details, sensitive information, private contact details, credentials, or confidential operational data in the exercise. Keep notes, simulations, and reviewer materials within the approved hiring access boundary.

Do not assess protected characteristics, personal background, or unrelated proxies. Describe the assessment in terms of capabilities needed for the role, alignment with the work, and evidence that distinguishes relevant performance.

## Step 1: Confirm the inputs

Before drafting candidate-facing instructions, confirm that the hiring team has both:

1. A current job description or role brief that covers responsibilities, level, expected outcomes, reporting context, and material constraints.
2. A role-success profile, hiring plan, or equivalent document that identifies the capabilities and work patterns needed for success.

Do not attempt to define the role-success profile while designing the exercise. The work sample must follow an agreed view of role success. Otherwise, it will tend to measure what is easy to prompt for instead of what actually matters.

If either input is missing, stop and ask:

> Before we design the work sample, I need a current role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

When both exist, review the relevant role context. This may include planning notes, examples of strong outputs, major constraints, prior hiring feedback, or approved materials describing the work. Read one or two comparable work samples only to calibrate tone, length, structure, and delivery format. Do not copy another role’s task shape automatically.

Give a brief status update before moving on, for example:

> Read the role brief, role-success profile, and two reference exercises. Moving to the alignment memo.

## Step 2: Write an alignment memo before drafting

Do not draft the exercise yet. First write a one-page memo titled:

**What we are testing for and why: [Role] work sample**

The memo must contain the following sections.

### Load-bearing capabilities

List three to five capabilities that the role succeeds or fails on and that a short asynchronous exercise can realistically surface. Phrase them as observable behaviors, not abstract traits.

Weak: “Strategic thinking.”

Better: “Can identify the highest-leverage issue in a messy operating situation, explain the tradeoff, and deliver a useful first action.”

Other examples include prioritizing under constraints, writing clearly for a defined audience, diagnosing a recurring problem, sourcing relevant opportunities, turning ambiguity into an executable plan, or designing a repeatable process.

### What the exercise will not test

Name important criteria that belong elsewhere in the hiring process. This prevents overclaiming and keeps the test bounded.

For example, interviews may assess live communication and collaborative reasoning. References may provide evidence about reliability and sustained performance. A later trial may assess work over days in real systems. Training can often address a specific tool, internal workflow, or domain vocabulary that is not essential on day one.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level, and explain what that changes.

- Entry-level exercises usually need clearer context and narrower deliverables.
- Mid-level exercises should often require independent prioritization and execution within stated constraints.
- Senior or leadership exercises may require explicit tradeoffs, direction-setting, and an output that another person can use without further explanation.

### Failure modes to catch

Identify two or three plausible work patterns that this assessment should reveal. Describe the pattern in terms of work, not personal labels.

Examples include a polished planner who does not produce usable work; a fast executor who misses the central issue; a careful candidate who defers every meaningful decision; or a technically capable candidate whose output does not serve the intended audience.

### What strong looks like

Write a short paragraph describing the evidence in a strong submission. Cover the choices it makes, the priorities it identifies, the assumptions it states, the quality of its outputs, and how it handles uncertainty.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the owner explicitly confirms or revises the memo.

## Step 3: Propose exercise shapes

Once the memo is approved, propose three possible exercise shapes. Each option must test the agreed capabilities, be understandable in roughly one minute, be self-contained, fit the allotted time, and produce evidence a reviewer can assess quickly.

For each option, provide:

- **Shape:** a plain-language description of the assignment.
- **What it tests:** the load-bearing capabilities it is intended to reveal.
- **Why it is evaluable:** what reviewers can observe and why they can compare submissions consistently.
- **Main risk:** the most likely source of noise, unfairness, or weak signal.

Keep each option concise. Common shapes include:

- **Triage pile:** The candidate receives messages, requests, and constraints; prioritizes them; drafts selected outputs; and recommends one systemic improvement. Useful for operations, coordination, support, and communications-heavy roles.
- **Choose a priority and ship it:** The candidate selects the highest-leverage action from a brief, explains the choice, and creates a small usable output. Useful for builder and strategic operations roles.
- **Diagnose and fix:** The candidate reviews a messy situation, identifies the central problem, and produces one targeted intervention. Useful for analytical, product, program, and process-improvement roles.
- **Source and pitch:** The candidate defines a target, identifies channels or examples using supplied information, and drafts outreach or a pitch. Useful for recruiting, partnerships, sales, and growth roles.
- **Decision-useful analysis:** The candidate assesses an issue using supplied evidence and gives a recommendation to a decision-maker. Useful for research, strategy, policy, and specialist roles.
- **Design a repeatable system:** The candidate creates a lightweight process, playbook, or artifact that another teammate could use. Useful for enablement, community, program, and operations roles.

Do not draft the complete exercise until the hiring owner chooses a shape. If none fit, propose three more based on the approved memo rather than forcing a familiar format.

## Step 4: Draft version 1

Use this candidate-facing order unless there is a clear reason to change it.

## [Role] Work Sample

Open with one or two sentences explaining the capabilities being assessed. State the total expected time.

**Your mission**

Describe a specific situation, not an abstract assignment. Give enough context for a candidate to act. If decisiveness is being assessed, identify which stakeholders are unavailable during the exercise so candidates must make reasonable assumptions rather than defer all consequential decisions.

End with one sentence restating what the candidate will produce.

**Deliverables**

List two to four substantive deliverables. Add rough time guidance where it helps candidates allocate effort. A common operational structure is a short analysis or prioritization section, several actual drafts or decisions, and one reusable process improvement.

Avoid excessive micro-tasks. A few meaningful outputs reveal more than many shallow choices. If planning and execution both matter, say explicitly that candidates should not let planning consume the time needed to ship work.

**Context**

Provide the minimum information needed: audience, project state, constraints, available resources, relevant policy, and stakeholder availability. Use fictional or safely anonymized names and identifiers unless approved public information is necessary.

For a triage exercise, include a realistic set of items, often around eight to ten. Connect some of them so candidates are rewarded for recognizing patterns across the full situation. Supply reference notes with all information needed for fair decisions, such as capacity limits, escalation rules, service policies, or available support.

**Instructions**

Include the expected time limit, submission deadline, submission format, payment amount and process, permitted tools, AI policy, and a way to document important assumptions. Tell candidates to submit what they have if they do not finish, with a brief note on what they would do next.

Use a transparent AI policy, such as:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

If useful for the role, invite a short informal walkthrough video. Do not require polished production unless that is itself a genuine role requirement.

**Anticipated questions**

Answer common questions directly:

- If a requirement is unclear, make a reasonable assumption and state it briefly.
- If time runs out, submit the work completed and explain what you would do next.
- The work will be used only to evaluate candidates for this role unless another use is agreed separately.
- Candidates who need an accommodation or accessible alternative format can contact the designated hiring contact.

### Payment and timing

Set compensation before inviting candidates. The amount should reflect expected time, role level, local legal requirements, and candidate burden. A base payment with a modest early-submission bonus can be appropriate when timely execution is genuinely relevant, but accommodations and reasonable scheduling needs must remain protected.

### Candidate-facing format checks

Use direct, plain language and the locale appropriate to the candidate group. Before sharing, check that the text works in the selected hiring or document system. Use simple headings and bullets. Avoid tables or horizontal dividers where the destination renders them poorly. Avoid generic slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.

Use clearly fictional names, domains, and email addresses in fictional scenarios. If the destination collapses ordinary line breaks in message headers, use its supported soft-break method. Do not include confidential information, private contact details, credentials, or unnecessary personal information.

After every draft, add a clearly separate section:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets identifying design choices worth reviewing: an item that may be too obvious, a scenario detail that may feel unrealistic, a payment choice, an overly prescriptive deliverable, or whether a video should remain optional. End with one focused decision question, such as: “Which part should we tighten first?”

## Step 5: Iterate with the hiring owner

Expect several rounds of revision. For each round, provide the complete updated exercise, not only a change list, so the owner can use it directly.

Apply feedback unless it materially undermines assessment validity, fairness, privacy, legal obligations, or candidate safety. If it does, state the concern once in plain language, offer an alternative, and let the accountable hiring owner decide. Typical revisions include tightening vague instructions, loosening excessive prescription, correcting scenario facts, simplifying deliverables, adjusting payment, and improving formatting.

## Step 6: Simulate two submissions

Before declaring the first usable version complete, simulate two full submissions using the exact candidate-facing instructions.

First, simulate a role-aligned candidate based on the approved role-success profile. Have them complete the actual deliverables within the stated time and add a short reflection on choices, uncertainty, and time allocation.

Second, simulate an earnest, capable candidate who could pass ordinary screening but whose work lacks one central role-relevant capability. Examples include someone who plans carefully where the role needs building, someone who avoids making justified decisions, or someone who executes individual tasks without noticing system-level patterns. The distinction must be based on work evidence, never identity, background, protected characteristics, or stereotypes.

Then synthesize:

1. Where the exercise distinguished relevant performance sharply.
2. Where both submissions looked similar.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by likely impact.

A capability that both simulations pass can be a useful floor check. The concern is when a central capability produces no meaningful difference in evidence.

## Step 7: Improve and finalize

Revise the full exercise based on the simulation, targeting the weakest diagnostic points first. Useful changes include connecting scenario items, removing obvious noise, adding a real constraint that forces a tradeoff, replacing broad opinion prompts with usable outputs, clarifying reviewer criteria, and removing specialized knowledge requirements that are trainable and not essential on day one.

Do not make the task harder merely to make it more selective. Make it more diagnostic of the agreed capabilities.

External reviewers may offer useful input. Assess each suggestion against the approved alignment memo, state which suggestions to use or skip and why, and keep final accountability with the hiring owner.

## Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The role description and role-success profile are confirmed.
- The alignment memo is approved.
- The selected shape maps directly to load-bearing capabilities.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and does not require private access.
- Payment, deadline, accommodations, and submission instructions are clear.
- A reviewer can assess a submission in about 20 to 25 minutes.
- Both simulations have been completed and led to necessary revisions.
- The exercise does not create unpaid production work.
- Privacy, authorization, access boundaries, and role-relevant criteria have been checked.

## Common failure modes

Avoid designing before agreeing what to measure; testing trainable tool fluency or domain trivia instead of durable judgment; requesting many shallow outputs; making every scenario item independent; allowing candidates to defer every decision; providing vague context that rewards insider knowledge; setting targets that encourage padding; or creating a test that takes longer to grade than its evidence justifies.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, paid, respectful of candidate time, and capable of producing evidence that helps reviewers make a role-relevant decision.


---
name: run-a-reference-call
description: Prepare, conduct, and document a hiring reference call that gathers specific, role-relevant evidence, protects privacy, and supports a fair decision.
---

# Run a reference call

Use this workflow to prepare and run a reference conversation for a hiring decision. Its purpose is to reduce specific uncertainty about a candidate’s likely performance in a role, not to collect general praise, investigate private life, or seek unrelated information.

Only conduct a reference check when there is a legitimate hiring purpose and appropriate authorization from the candidate or another authorized hiring process. Use only the minimum relevant information. Keep notes within the approved hiring access boundary, omit unrelated sensitive details, and share referee comments only with people responsible for the decision.

## 1. Confirm the call scope

Before researching or scheduling, record:

- Candidate name and role under consideration.
- Referee name, contact method, and stated relationship to the candidate.
- Call date, time, format, and participants, if known.
- Hiring stage and next decision point.
- The role-relevant questions that this reference should help answer.

Distinguish a hiring reference from a request to provide a reference about someone to an outside party. Use the workflow that matches the direction of the request.

If the relationship, authorization, or purpose is unclear, pause and ask the hiring lead or candidate for clarification. Do not infer permission from a public profile, an old contact record, or a prior professional connection.

## 2. Gather relevant context

Review authorized hiring materials and the candidate’s supplied reference information. Prefer the candidate’s application, interview records, work samples, assessments, and reference list. If access is authorized and necessary, review relevant prior professional contact with the referee.

Establish:

- The role’s core outcomes, constraints, and capabilities needed in the first several months.
- The candidate’s current stage and unresolved, role-relevant questions.
- How the referee knows the candidate: reporting relationship, collaboration type, time period, and closeness of observation.
- Which work the referee personally observed and which claims are secondhand.
- Other planned or completed references, so evidence can be compared without treating one call as decisive.
- Any authorized candidate materials the interviewer may need during the conversation.

Limit external research to confirming professional context relevant to the call, such as the referee’s current professional role or the kind of work they did with the candidate. Do not collect personal, sensitive, speculative, or gossip-based information. Do not access private communications, calendars, chat records, or people records unless access is authorized and the material is necessary for the hiring purpose.

## 3. Define the call’s job

Read relevant hiring evidence and completed reference notes before drafting questions. Separate findings into three categories:

- **Observed evidence:** Concrete work, outcomes, behaviors, and examples.
- **Interpretation:** What an interviewer or referee thinks those observations mean.
- **Open question:** A capability, risk, or condition that needs more evidence.

Turn open questions into neutral checks. For example, if prior evidence suggests the candidate has mainly worked in structured settings, ask for examples of how they handled changing priorities. Do not tell the referee that someone else raised a concern, identify other referees unnecessarily, or invite confirmation of a negative conclusion.

If this is the first reference, select a small set of dimensions that later calls can cross-check: ownership, reliability, communication, response to feedback, judgment under ambiguity, and conditions for effective performance.

## 4. Create a call brief

Create a meeting record in an authorized, access-controlled location before the call. Put the full useful brief in that record rather than relying on temporary chat messages or personal notes.

```markdown
# [Referee name] — reference for [Candidate name]

## Context
- **Candidate and role:** [Candidate] is being considered for [role].
- **Hiring stage:** [stage and next decision point].
- **Referee:** [name and relevant professional context].
- **Working relationship:** [how they worked together, when, for how long, and how directly the referee observed the work].
- **Relevant candidate materials:** [authorized materials or records].
- **Other references:** [known references or “not yet confirmed”].

## Briefing notes
- **Decision questions:** [two to four role-relevant uncertainties].
- **Evidence to cross-check:** [specific, neutral themes from prior evidence].
- **Unique perspective:** [what this referee is especially well placed to assess].
- **Context to know:** [limits of observation or possible conflicts of interest].
- **First-reference note:** [what to capture consistently for later comparison, if applicable].

## Opening
> Thank you for taking the time. I am speaking with references as part of the process for [candidate]’s application for [role]. I would like to understand the work you directly observed, its context, and where they are likely to thrive or need support. Please share only information relevant to their professional work. Your comments will be handled within the authorized hiring process, subject to applicable policy.

## Questions
- [Questions and role-specific probes]

## Notes and assessment
- **Direct observations:**
- **Referee’s interpretation:**
- **Examples and outcomes:**
- **Limits or possible bias in the evidence:**
- **Follow-up needed:**
```

Write briefing notes as direct actions. For example: “Ask for a concrete example of how the candidate handled conflicting stakeholder requests.” Avoid vague instructions such as “explore communication.”

## 5. Ask structured questions and follow the evidence

Start by confirming the referee’s basis for knowledge:

- How did you work together, and how closely did you work day to day?
- What was the candidate responsible for, and what were you responsible for?
- Which parts of their work did you personally observe?

Then ask for evidence:

- What did the candidate personally deliver, and what was the result?
- What did strong performance look like in practice?
- What is their most distinctive strength in this type of work?
- Where did they need the most support, development, or feedback?
- Tell me about a difficult project, setback, or conflict. What did they do?
- How did they respond when priorities or requirements changed?
- What conditions helped them do their best work? What conditions made success harder?
- If they struggled in this role after several months, what role-relevant factor would be the most likely cause?
- If they were doing well after several months, what development area would be most useful next?
- What could a manager do to help them contribute effectively?
- Would you work with them again? In what type of role or environment?
- What have I not asked that would matter to someone managing or collaborating with them?

Follow broad claims with evidence prompts:

- “What did that look like in a specific situation?”
- “What did they personally do rather than the team as a whole?”
- “How did you know it was successful?”
- “What was the outcome?”
- “Was that typical or an exception?”

Do not pressure the referee to rank the candidate against others, speculate about protected characteristics, reveal confidential hiring deliberations, or answer outside their direct knowledge.

## 6. Add role-specific probes

Choose probes from the role’s actual outcomes rather than using a fixed list by title. Examples:

- **Operations work:** Handling ambiguity, building repeatable systems, prioritizing competing work, and balancing speed with reliable process.
- **Community-facing work:** Building trust, communicating with varied stakeholders, addressing conflict constructively, and turning feedback into improved programs.
- **Leadership work:** Setting priorities, making sound tradeoffs, developing others, managing resources or external partners where relevant, and building durable operating practices.
- **Technical or analytical work:** Quality of reasoning, documentation, collaboration, judgment under uncertainty, and turning analysis into useful decisions.

Use only as many probes as the call can support. Specific examples are more useful than shallow coverage of every capability.

## 7. Record and assess the signal

Write notes promptly after the call. Attribute claims clearly and distinguish observations from inferences. Include the referee’s confidence, observation period, and meaningful limits, such as limited direct contact or a potentially conflicted relationship.

Compare the call with other evidence. Look for patterns across independent sources, but do not count repeated hearsay as independent confirmation. A contradiction is a prompt for clarification, not proof that either person is unreliable.

Finish with a concise assessment:

- What role-relevant evidence was strengthened?
- What concern was reduced, remained open, or became more important?
- What conditions appear important for the candidate’s success?
- What follow-up, if any, is justified before a decision?

## Readiness gate

Do not mark preparation complete until the meeting record includes:

- Confirmed candidate, role, referee, and call details, or a clear note that details are unavailable.
- The referee’s relationship to the candidate and limits of observation.
- Role outcomes and the specific uncertainty the call should reduce.
- Authorized candidate materials and prior reference evidence, where available.
- A tailored opening, core questions, and role-specific probes.
- Direct briefing notes explaining what to validate and why.

## Quality check and common failure modes

Before the call, check that the brief is useful without access to a separate research thread. After the call, check that an authorized hiring reviewer who was not present can understand the notes.

Avoid these failures:

- Treating a reference as a generic endorsement rather than evidence for a decision.
- Asking questions disconnected from the role’s actual outcomes.
- Repeating private allegations or interview impressions as facts.
- Accepting praise without requesting a concrete example.
- Overweighting title, confidence, or personal affinity over direct observation.
- Collecting unrelated personal or sensitive information.
- Recording vague conclusions without source, context, or evidence limits.
- Letting one highly positive or negative call determine the final decision alone.

A good reference call produces specific, attributable evidence about relevant performance, identifies the limits of that evidence, and helps the hiring team make a more informed and fair decision.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and privacy, verifying rendered state, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for tasks that require interacting with a website: completing forms, changing dashboard settings, collecting information from rendered pages, testing a user flow, or working in an authenticated account. Use it when a simple page request or supported direct interface cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until the account, target, page state, and authorization are clear.

A browser automation command reporting success does **not** prove that a website accepted a change. Modern applications can store state separately from the visible DOM, commit only after focus leaves a field, replace controls during re-rendering, or show misleading errors after an action has succeeded.

## 1. Establish legitimacy, scope, and authorization

Before opening private records, authenticated dashboards, communications, or data about people, confirm all of the following:

- There is a legitimate purpose for the task.
- The requester has appropriate authority to access the account and perform the requested action.
- The requested account, organization, environment, and target are identified.
- Only the minimum relevant sources and information will be used.
- The output will stay within the appropriate access boundary.

Respect consent and reasonable privacy expectations. Do not copy unrelated personal information into notes, screenshots, logs, or reports. Do not expose credentials, session cookies, access tokens, recovery data, financial details, health information, or other sensitive content unless it is essential and the user has explicitly authorized its handling.

Define the task boundary before navigating deeply:

- What page, record, form, setting, or workflow is the target?
- What information will be entered, changed, uploaded, or collected?
- What is the minimum information needed?
- Is the action reversible?
- Does it send, publish, pay, delete, grant access, change a plan, or create another external commitment?
- Which choices require the user’s judgment?

If identity, authority, target, or intended effect is unclear, stop and ask before changing data.

## 2. Choose the least invasive suitable route

Choose the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can complete the task. It is often more reliable than reproducing browser interactions.
2. **Headless browser automation.** Use this for public pages, routine rendered-page extraction, screenshots, UI testing, and forms that do not require an established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task truly needs an existing session, account-specific state, single sign-on, or a user-directed browser context.

Before driving a browser, look for a legitimate direct route. Review official documentation, normal form actions, visible page structure, and ordinary network activity for supported endpoints. A form may submit structured data through an approved service interface that is safer and more reliable than interacting with a complex front end.

Do not use undocumented interfaces to bypass access controls, consent boundaries, service restrictions, or security controls. Do not use an authenticated visible session merely for convenience: it can interrupt the user’s work and increases privacy and account risk.

If a site blocks automated browsing, do not try to evade its protections for research or routine collection. A verified visible session may be appropriate only when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and the established session is necessary. Do not disable browser security, multi-factor authentication, warnings, bot protections, or access controls.

## 3. Protect browser and account context

When using a visible authenticated browser, announce that you are taking control and state the purpose. For example: “I am using the authorized work browser session to update the requested dashboard setting.” Do not take control silently, but do not unnecessarily delay a task that is already clearly authorized.

Use a fresh tab, window, or isolated tab group unless the user explicitly directs you to an existing tab. Avoid disturbing tabs, drafts, or workflows that may belong to the user.

Classify the required context explicitly, such as:

- personal or work;
- test, staging, or production;
- one organization or another;
- a particular account, project, or workspace.

Select the corresponding browser profile or connection directly. Never rely on a generic browser selector, a window title, a remembered default, a tab label, or an old connection name as proof of identity. Verify the signed-in account using a reliable account indicator before opening the real target or making changes.

Use an account preflight gate before actions that change data:

1. Confirm the account identity.
2. Confirm the environment.
3. Confirm the exact record, recipient, or setting that will change.
4. Confirm the user’s authority and requested outcome.
5. Only then mark the context as verified if the automation system has a verification marker or permission gate.

Never enable a verification marker before actually completing the identity check. If the required account, profile, or environment cannot be verified, stop rather than guessing.

A useful pre-action question is: **Which account is this? Which environment is this? What exact item will change?**

## 4. Separate preparation from commitment

Treat preparation and commitment as distinct phases.

Preparation commonly includes drafting text, filling fields, selecting options, collecting information, setting up a preview, and taking a screenshot. These actions are often reversible. Commitment includes submitting an official form, sending a message, publishing content, placing an order, making a payment, deleting data, changing a plan, changing access, or activating anything labeled permanent or impossible to undo.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify the result, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Re-check the account, target, and readiness gate. Then perform the final action once if appropriate authorization covers it.

Obtain confirmation immediately before an irreversible action—such as a payment, deletion, permanent plan change, or one-way submission—unless the user has already provided clear, specific authorization for that exact action and no material facts have changed. Honor an explicit user request to review before submission even if standing authorization exists.

For a reversible, low-risk change that the user explicitly requested, normal verification is generally sufficient unless the page presents an unexpected warning or wider impact.

If the page reloads, re-renders, or the session changes between phases, do not assume the earlier state remains valid. Inspect and verify again.

## 5. Inspect the rendered page before editing

Do not start by guessing selectors, using numeric field positions, or trusting that a visible label maps to the first nearby input. First inspect the rendered page and identify every relevant control.

For each field or setting, determine:

- Element type: single-line input, text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether the field is required.
- Validation rules, length limits, formatting behavior, and disabled state.
- Whether the apparent control is the real editor, a wrapper, or a hidden synchronization element.
- Whether changing an option, checkbox, date, or tab causes a re-render.

Address controls by stable semantic identity: visible label text, accessible name, an identifier explicitly linked to the label, or another meaningful relationship. Do not rely on DOM indexes when semantic labels are available; reactive applications can reorder elements between loads and after updates.

Before changing a record or setting, inspect its current state. This reduces the chance of editing the wrong item or overwriting information unintentionally.

### Generic inspection pattern

Use the page-inspection capability of the selected automation tool to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

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

## 6. Use the right interaction for each control

A generic “set value” operation is not reliable for every web control. Use interactions that resemble the application’s intended user behavior.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use normal text entry or the automation library’s standard fill method. | Newlines may be removed silently. |
| Multiline text area | Fill text, then move focus away. | Some applications commit only after blur. |
| Rich-text or content-editable editor | Focus the real editor, select old text, delete it, enter text through keyboard-style events, then blur. | Direct DOM writes may not update the application model. |
| Dropdown or combobox | Open it, select the visible intended option, and wait for the page to settle. | A selection can cause a full re-render. |
| Checkbox or radio group | Read current state first; change only if necessary. | Blind clicking can reverse an already-correct choice. |
| Date/time picker | Select the intended values, close the picker safely, and verify the rendered summary. | Popovers can clear, reinterpret, or alter related values. |
| File upload | Confirm the file, destination, audience, and privacy implications first. | Uploading may begin immediately and be difficult to undo. |

Framework-driven editors often reject low-level property changes even when the DOM appears modified. For a content-editable field, use this general sequence:

1. Focus the actual editable element, not merely an accessible wrapper.
2. Select the existing content.
3. Delete it.
4. Enter the new content through keyboard-style input.
5. Move focus to a neutral page element to commit the change.
6. Wait briefly for any re-render.
7. Read the result back.

Some forms pair a visible editor with a hidden input. Updating the hidden input can appear successful in a technical inspection while server-side validation treats the visible editor as empty. Target the interactive control that the application actually reads.

If a dropdown, checkbox, tab, date, or similar control may refresh the form, perform and verify those changes **before** entering lengthy text. Re-inspect after the refresh and confirm that previous values remain present.

## 7. Verify every meaningful edit

After filling a field or changing a setting, read it back from the page. Compare the actual visible or accessible result with the intended value. For sensitive content, compare a length, required-state flag, checksum-like summary, or minimal redacted excerpt rather than exposing full content unnecessarily.

Look for these mismatches:

- The automation tool reports success but the field is blank.
- Newlines, repeated spaces, punctuation, or special characters changed.
- Text was truncated by a single-line control or length limit.
- An editor displayed text but did not retain it in application state.
- Editing a later field erased an earlier one after a re-render.
- A hidden synchronization field changed instead of the visible editor.
- A selection changed a dependent field, recipient, date, or validation rule.

If verification fails, do not proceed toward submission. Diagnose the control type, retry once with a more appropriate method, and verify again. If the page still rejects or alters the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 8. Run a pre-submit readiness gate

Before any final submission or high-impact change, inspect the full relevant page state again. Confirm:

- The correct account, organization, and environment are active.
- The target record, recipient, page, or setting is the intended one.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Dropdowns, checkboxes, dates, recipients, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final control has the intended effect and is not a similarly named destructive alternative.

If any required field is empty, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially prepared form is recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only through an appropriate access boundary. Avoid pasting a large table of sensitive field values into chat when a short summary and authorized record are enough.

### Readiness checklist

- [ ] The account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependent data such as recipients, dates, options, and attachments was checked.
- [ ] A pre-action record exists when the action is consequential.
- [ ] Authorization for the final action is clear.
- [ ] The final action and its effect are understood.

## 9. Confirm completion after acting

A final button click is not proof of success. Look for reliable evidence such as a success message, confirmation reference, newly created record, persisted setting, sent or published item, updated status, or a safe reload that preserves the intended result.

If the site reports an error, inspect the resulting state before retrying. An error can be cosmetic, while blind retries can create duplicate messages, submissions, purchases, or records.

If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Do not describe an attempted action as completed.

## 10. General failure patterns and recovery rules

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank | The application ignored a direct value update. | Focus the actual editor, use keyboard-style input, blur, and read back. |
| Earlier fields disappear after a later edit | A component re-render reset uncommitted state. | Commit and verify each field; perform re-rendering selections first. |
| Text loses line breaks or characters | The wrong control type or a formatting rule was used. | Find a multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node. | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited. | Use the visible interactive control that the application reads. |
| Automation becomes unstable on a complex page | The automation layer is unsuitable for the operation. | Switch to a more robust browser method or approved direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers behave differently | The site varies behavior by browser context. | Prefer an authorized direct interface; if necessary for the explicit task, use a verified visible session without evading protections. |
| A popup unexpectedly changes dates or fields | The widget has stateful close, clear, or parsing behavior. | Close it through a neutral page action and re-verify affected fields. |
| A visible error may be cosmetic | The action may already have completed. | Inspect the resulting record or status before retrying. |
| Account context is uncertain | The wrong profile or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
- [ ] The final action was authorized at the appropriate level.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: Create, improve, test, evaluate, and package a reusable AI skill from a new idea, an existing draft, or a demonstrated workflow, with optional optimization of the description that controls when the skill activates.
---

# Create an AI skill

Use this workflow to design a new reusable AI skill, improve an existing skill, test whether a skill helps, or turn a repeated conversation workflow into portable instructions. A skill is focused guidance, with optional resources, that helps an AI perform a recurring job consistently.

The core cycle is:

1. Define the intended job and its boundaries.
2. Draft or revise the skill.
3. Test it using realistic user requests.
4. Review outputs with a human and measure objective requirements where useful.
5. Improve the instructions based on evidence.
6. Repeat until the result is useful, reliable, and not merely fitted to a few examples.
7. Optionally refine the description that determines when the skill activates.
8. Package and hand off the final skill.

Adapt the rigor to the user’s needs. Some users want a quick collaborative draft; others need comparison runs, formal checks, and multiple revisions. First determine where the user is in the process, then help them take the next useful step.

## Communication principles

Match the user’s familiarity with technical language. Use plain English by default. Terms such as *evaluation* and *benchmark* can be useful, but explain them briefly if needed. Do not use terms such as “JSON,” “assertion,” or “schema” without explanation unless the user has indicated comfort with them.

Explain why key questions matter. For example: “What should a successful result look like: a chat response, a structured report, a file, or a completed action? This determines how we test it.”

Keep the user involved at important decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before introducing restrictive scope limits, tool dependencies, or approval requirements.
- Share proposed test requests before relying on them.
- Let human review lead for subjective qualities such as voice, design, strategy, or usefulness.
- Be flexible when the user asks for a lightweight, exploratory process rather than a formal benchmark.

## 1. Identify the starting point

Classify the request before choosing a workflow.

### A. New skill

The user has an idea for a recurring task. Start with discovery, scope definition, and a draft.

### B. Existing skill or draft

The user already has instructions and wants them simplified, tested, improved, or repackaged. Read the current material first. Preserve the established skill name and identity unless the user explicitly wants a rename.

### C. Workflow demonstrated in the conversation

The user may say, “Turn what we just did into a skill.” First extract what the conversation already establishes:

- Inputs and source material used.
- Actions and tools used.
- Sequence of decisions.
- Corrections and preferences supplied by the user.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow and identify gaps for the user to confirm. Do not silently convert one-time details into general rules.

### D. Evaluation or optimization request

The user may have a finished-looking skill and want evidence about whether it helps. Go directly to test design, comparison, review, and revision. Do not rewrite a skill only because rewriting is possible.

## 2. Capture intent, access boundaries, and scope

Gather enough information to define a coherent job. Do not ask every question mechanically; begin with what most affects the design.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** Which requests, phrases, or contexts should cause the skill to apply?
3. **Inputs:** What information, files, systems, examples, and capabilities may it use?
4. **Authorization:** What access is legitimate for this task?
5. **Outputs:** What should it produce, change, or recommend? Is there a required structure or file format?
6. **Success criteria:** How will the user know the result is correct or useful?
7. **Boundaries:** What should the skill not do? When should it ask a question, stop, decline, or request approval?
8. **Variation:** Which common cases, difficult cases, and meaningful exceptions matter?
9. **Dependencies:** Does it need particular capabilities, templates, scripts, references, or approved data sources?
10. **Testing:** Should it be tested on example requests?

Offer useful choices where appropriate:

- “Should the skill make a low-risk best effort when information is missing, or stop and ask?”
- “Should it default to a concise response, a detailed response, or let the user choose?”
- “Should it use only sources the user explicitly approves, or may it use authorized sources already available in the workspace?”

### Privacy and authorization boundaries

For workflows that access private communications, records, or information about people:

- Require a legitimate purpose and clear authorization before accessing material.
- Use only the minimum relevant sources and information.
- Omit unrelated personal information and sensitive details from outputs.
- Respect consent, confidentiality, and reasonable privacy expectations.
- Keep findings within the appropriate access boundary; do not repurpose them for unrelated audiences or decisions.
- State uncertainty when authorization, source relevance, or data-handling expectations are unclear.

For hiring, assessment, or review workflows, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Do not make claims based on irrelevant personal characteristics or use demeaning language about people.

### Research before drafting

If relevant documentation, comparable skills, approved reference materials, or domain guidance are available, inspect them before drafting. Research should reduce burden on the user, not replace the user’s authority over requirements.

Research may identify:

- Existing conventions and output standards.
- Constraints of available tools or file formats.
- Similar reusable patterns.
- Safety, privacy, compliance, and approval requirements.

If evidence conflicts, present the uncertainty and available choices rather than inventing a rule.

## 3. Choose a skill structure

Keep a skill focused enough that its purpose and limits are predictable. One skill may support closely related variants, but separate unrelated jobs when they have different users, permissions, sources of truth, or definitions of completion.

A typical portable package looks like this:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed documentation
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Routing description:** A short statement of what the skill does and when it applies.
2. **Core instructions:** The workflow needed on most uses.
3. **Supporting resources:** Detailed references, templates, and scripts loaded only when relevant.

Keep core instructions readable. If they become long, move detailed domain variants into clearly named reference files and say exactly when to consult each one. Add a contents list to large references.

For skills serving multiple variants, provide a selection step in the core instructions and separate resources by variant. Load only the applicable material rather than treating every variant as mandatory.

### Bundle repeatable deterministic work

If test runs show repeated reconstruction of the same helper procedure, consider bundling a script or template. This is useful for repeatable validation, file conversion, report assembly, data cleanup, or other work that is easier to verify than free-form reasoning.

Bundle a helper only when it is reusable, authorized, and clearly valuable. Document what it does, its inputs and outputs, required capabilities, when to use it, when not to use it, and its checks or limitations.

Do not add automation merely because it is possible. The skill should never conceal actions, bypass access controls, export data beyond authorization, damage systems, or surprise the user relative to its stated purpose.

## 4. Write the skill

Draft in clear, imperative language. Explain the reason for important instructions, especially where a step protects quality, privacy, safety, or user control. A capable AI can adapt better when it understands the purpose of a rule rather than receiving unexplained rigid commands.

Use the following sections where applicable.

### Purpose and scope

State the job, intended context, and boundaries. Clarify whether the skill produces an answer, creates a file, modifies data, performs an external action, or guides the user through a process.

### Inputs and prerequisites

List required inputs, permitted sources, needed capabilities, and optional information. State what happens when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved data source.
If the source is unavailable, ask the user for an export or provide a draft clearly marked as incomplete.
```

### Workflow

Describe the normal sequence and decision points:

1. Inspect the request and available inputs.
2. Clarify only questions whose answers materially change the work.
3. Gather evidence from approved sources.
4. Complete the task with the appropriate method.
5. Check the result against requested format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limitations.

Use conditional instructions rather than trying to enumerate every edge case:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested action could overwrite important work or affect an external system, explain the impact and request confirmation before proceeding.
```

### Output format

When consistency matters, provide a fixed or near-fixed template:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or needed follow-up]
```

Avoid rigid shells where contextual adaptation is more valuable. In those cases, state goals and show a short representative example instead.

### Quality, safety, and completion checks

Describe checks before delivery. Examples include required fields, calculation validation, source support for key claims, preservation of original data, or flagging uncertainty.

A skill’s behavior should be unsurprising given its description. Do not create misleading, harmful, or unauthorized skills. When a request exceeds authority or creates substantial risk, explain the limit and offer a safe alternative where possible.

### Failure behavior

Specify general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable source or capability:** Explain what cannot be verified and offer an alternative.
- **Ambiguous request:** Make a low-risk assumption when it does not materially affect results; otherwise ask.
- **Validation failure:** Do not present the output as complete; correct it, report the issue, or request guidance.
- **High-impact action:** Pause for confirmation before irreversible, external, or consequential changes.

### Examples

Use a small number of generalized examples only when each teaches a distinct decision pattern. Examples should illustrate reasoning rather than replace it with narrow rules.

## 5. Write the routing description

The skill description controls activation. It should say both **what the skill does** and **when to use it**. Include common user language, including requests that imply the job without naming it directly.

A useful pattern is:

```text
Create clear project status reports from approved updates and source material. Use for requests involving progress summaries, leadership updates, milestone reviews, project risks, blockers, and next steps, even when the user does not use the phrase “status report.”
```

Avoid vague descriptions such as “help with documents.” Do not make the description so broad that it captures adjacent work better handled by another skill. Keep the description honest: it should not imply tools, authority, or outcomes the skill cannot provide.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description clearly state when to activate it?
- Are required inputs, access limits, permissions, and outputs clear?
- Does the workflow explain why important checks matter?
- Does it handle missing information and validation failures?
- Are there unnecessary rules, duplicated guidance, or brittle wording?
- Does it rely on private conventions, personal access, or undeclared tools?
- Does it preserve appropriate privacy boundaries?
- Does it leave a capable AI enough flexibility for normal variation?

Prefer lean instructions over a long list of rules that do not improve outcomes. Repeated emphatic language is a warning sign unless the boundary is genuinely non-negotiable, such as authorization or safety.

## 7. Design realistic test cases

After the draft is stable enough to test, propose two or three realistic requests. Ask the user whether they represent genuine use and whether important cases are missing.

For each test, record a descriptive name, prompt, supplied files or context, expected result, and objective checks if appropriate.

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

Include meaningful coverage:

- A typical successful request.
- An incomplete or ambiguous request.
- A format-sensitive or rule-sensitive request.
- A realistic case that changes the workflow.
- A request requiring approval, privacy protection, or a safe refusal, when relevant.

Do not test only wording copied from the skill. Vary phrasing, detail level, and context. Avoid retaining private examples when a generalized prompt can test the same capability.

## 8. Run comparisons and preserve evidence

When independent execution is available, compare the skill with a meaningful baseline.

- **New skill:** Run each test with the skill and without it.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the new version with the previous version.

Start all comparable runs under similar conditions. When parallel execution is available, launch skill and baseline runs together for every test case. Preserve the prompt, input files, outputs, and available execution metadata.

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

Record elapsed time and resource-use data as soon as the execution environment reports them, because some systems do not retain this metadata later.

If independent execution is unavailable, run transparent sanity checks instead: apply the skill to each test request, preserve outputs, and ask the user to review them. Do not claim this is equivalent to an independent baseline comparison.

## 9. Define and grade objective checks

While tests run, draft objective checks where they truly help. Explain them to the user before treating them as success criteria.

Good checks are observable and meaningful:

- Required sections are present.
- A generated file opens and contains required fields.
- Calculations match known values within an agreed tolerance.
- The output identifies missing mandatory inputs.
- Claims include required source references.

Store each result with a clear statement, pass/fail value, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable information and requests it."
    }
  ]
}
```

Use programmatic checks when practical. They are more repeatable than visual inspection and can be reused. Do not force numerical checks onto subjective work such as writing quality, visual design, or strategic judgment; those need human review.

## 10. Review results with a human

Present outputs and measurements in an accessible review format. If a review interface is available, use it to show each prompt, output, comparisons, grades, and feedback field. In a headless or limited environment, generate a shareable static review artifact if possible; otherwise present material directly in conversation or as downloadable files.

For each case, show:

- The original prompt and relevant input context.
- The skill output and baseline or earlier-version output when available.
- Objective grades and evidence.
- Timing and resource data when available.
- A clear place for the reviewer to leave feedback.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add effort or detail without value?
- Would the result work for similar requests with different wording or data?

Do this review before making speculative revisions. Human feedback should guide what matters most.

## 11. Analyze results beyond pass rates

Aggregate results when possible: pass rates, average time, average resource use, and variation. Place revised-skill results before the comparison condition in reports.

Then inspect patterns that summary statistics can hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill’s contribution.
- **High variance:** Similar runs differ widely, indicating ambiguity or instability.
- **Tradeoffs:** Quality improves but time or resource use becomes excessive.
- **Failure concentration:** Several misses share a root cause, such as unclear source selection.
- **Unproductive work:** Execution records show redundant research, planning, or formatting.
- **Repeated reconstruction:** Multiple runs create the same helper process, indicating a reusable resource may help.

For a consequential comparison between two versions, use blind review: provide two outputs to an independent evaluator without identifying their origins, grade them with a shared rubric, and reveal the mapping afterward.

## 12. Improve without overfitting

Revise based on user feedback, outputs, and analysis. Change the smallest part likely to fix the underlying cause.

Use these principles:

1. **Fix causes, not examples.** A complaint from one test should lead to a general rule only if it represents a recurring class of problem.
2. **Keep instructions lean.** Remove guidance that does not change behavior or causes wasted effort.
3. **Explain intent.** State why a step protects quality, usability, authorization, or privacy.
4. **Add reusable resources only when justified.** Bundle scripts, templates, or references when repeated work shows their value.
5. **Preserve useful behavior.** Do not discard outcomes the user already values.
6. **Expand tests gradually.** Add a case when it represents a real class of failure, not every one-off incident.

After revision, rerun the full test set in a new iteration, using the same baseline policy. Compare new outputs with prior outputs where possible and collect feedback again.

Stop when the user says the skill is ready, feedback is consistently positive across meaningful cases, objective requirements are reliably met, or further revisions are no longer producing meaningful gains.

## 13. Optimize triggering behavior

Only optimize the activation description after the workflow itself is useful.

Create a realistic trigger-evaluation set with roughly balanced positive and negative examples. Positive examples should be requests that should activate the skill; negative examples should be difficult near-misses that share language or context but need a different capability.

```json
[
  {
    "query": "I need a concise update for leadership from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain when teams usually write progress reports?",
    "should_trigger": false
  }
]
```

Use substantive prompts. Very simple one-step requests may not activate a specialized skill even when the description matches, because the AI can often handle them directly.

Review the test set with the user before optimization. If the environment supports repeated trigger tests, separate examples used to improve the description from held-out examples used to choose it. Select the description by held-out performance rather than by fit to the examples used during editing. Show the user the before-and-after wording and results.

## 14. Package and hand off

Package the core instructions and only the resources required for normal use. Before delivery, audit the package:

- The skill name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on private conventions, personal access, or undeclared capabilities.
- Scripts and references are present, clearly named, and documented.
- No credentials, private identifiers, confidential data, or sensitive examples are included.
- The user can install or adapt the package in their chosen environment.
- Evaluation material is retained only when it is safe and useful.

Provide a concise handoff note describing the skill’s purpose, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an accurate activation description, instructions that handle normal variation, explicit authorization and uncertainty boundaries, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user needs.


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

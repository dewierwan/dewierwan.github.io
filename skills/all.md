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
description: Find the weak points in a leading strategic idea before committing to it. Steelman the case, test its load-bearing assumptions through sequential challenge, and finish with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or build the solution.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor that matches its consequences.
4. Plan or build the selected approach, if applicable.

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing one option too early can become an exercise in defending it.

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the earlier findings to make the decision.

If reviewing private communications, records, or feedback about people, use them only for a legitimate purpose with clear authorization. Use the minimum relevant information, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Use available evidence such as research, metrics, prior experiments, customer feedback, documented decisions, and authorized stakeholder input. Distinguish facts, inferences, and forecasts.
- Refer to potential dissenters by relevant role, such as finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

**Template**

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, with the most consequential first.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Name a test] |

Make assumptions observable where possible. Replace “customers will value this” with a behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions, then adapt later questions to the answers received. Do not present the full list as a questionnaire, because that permits selective answering.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed? Why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence. Ask what observed behavior, data, comparison, or commitment supports the belief.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failures, external changes, and an incorrect premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable signal] | [Name the check or accountable role] |

The warning sign must be observable early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap. Do not treat silence as agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence that names the evidence that would reverse or materially alter the position.

**Template**

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than approving the idea.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next step:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as targeted interviews, expert review, a prototype, or a short data collection period. Next: run that test, then make the decision with its result recorded.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, the downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with exactly one concrete next action containing a verb, an owner, and a deadline when useful.

**Example:** `Research owner: interview five target users this week and compare the results against the adoption assumption.`

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

Use this workflow to make decisions with the right amount of rigor. The goal is not maximum analysis. It is to make a clear call when ready, preserve the reasoning for meaningful choices, and learn from outcomes.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may recommend an option in conversation, clearly labeled as assistant analysis. Put that analysis in a decision record only if the user asks for it.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution. Start or plan the task instead of opening a decision process.
5. **Record only with permission.** A request such as “Should we do X?” requests analysis, not creation of a record. Create or update a decision record only when the user asks to log, track, open, or commit it, or has explicitly agreed to that practice.
6. **Protect privacy and access boundaries.** Before accessing shared communications, personnel records, customer data, or a shared decision register, ensure there is a legitimate purpose and clear authorization. Use only the minimum relevant information. Omit unrelated sensitive details.

If an organization uses a shared decision register, confirm that its audience is appropriate before writing to it. For sensitive topics such as health, relationships, compensation, or confidential personnel matters, offer a private record or keep the discussion in chat.

## 1. Choose the mode

Determine whether this is a new or existing decision.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review date and has not yet received an outcome assessment.

If the user explicitly names the mode, follow that instruction. Otherwise, if authorized, search the available decision register for overlapping decisions before creating a duplicate.

For a resume, retrieve the existing record and append new information rather than overwriting history. For a review, use the original prediction and reasoning as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Write the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What is the deadline or decision trigger?
- What result is desired?
- What happens if no action is taken?

If the question is broad and no credible options exist yet, generate options before evaluating them. Do not pressure-test a vague problem statement.

If the request has only one viable path, say so directly: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time when needed. Put the choice in one bucket.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, consult relevant stakeholders |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and named prerequisite conversations |

Use this test if classification is unclear: **What would it cost to unwind this?** Consider money, time, trust, operational disruption, opportunity cost, and reputational effects. If the cost cannot be stated quickly or is uncertain, the decision is probably larger than it first appears.

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: continued attention may cost more than an imperfect choice.

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

Use the user’s chosen decision register, document system, or private file. A useful record contains status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

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

## Workflow audit

Before closing the session, check:

- Was the question actually a decision rather than a task?
- Did the level of analysis match reversibility and stakes?
- Was a hard-to-reverse decision pressure-tested or explicitly overridden with a reason?
- Were required stakeholder conversations and dissent handled before a direction-setting commitment?
- Are the user’s views clearly separated from assistant analysis?
- If a record was created or updated, did the user authorize it and have an appropriate access boundary?
- Does the record contain a next action, review date, and testable prediction where appropriate?

If the workflow itself did not fit the decision, note the improvement for the user or workflow owner. Do not silently alter shared processes, records, or instructions.


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
description: Learn a paper, article, post, or topic through a short Socratic dialogue that builds durable understanding with retrieval, explanation, challenge, and application rather than passive summary.
---

# Learn with a tutor

Help a learner understand, retain, and use a provided paper, article, post, or topic through an active dialogue. Prioritize retrieval and reasoning over exposition: the learner should do most of the intellectual work, while the tutor asks focused questions, identifies gaps, and adjusts the challenge.

## Learning principles

- **Retrieve before reviewing.** Do not provide an unsolicited summary. Ask the learner to recall and reconstruct ideas in their own words.
- **Require explanation.** Move beyond stated conclusions: ask why, how, under what conditions, and based on what evidence an idea holds.
- **Have the learner generate connections.** Ask for their own examples, analogies, predictions, and applications before supplying examples.
- **Use productive difficulty.** Make the task demanding enough to require real thought, but not so difficult that the learner cannot make a meaningful attempt.
- **Practice transfer.** Connect the source to unfamiliar cases, related concepts, and real decisions.
- **Reveal gaps through inquiry.** When an answer is incomplete, inconsistent, or mistaken, first use questions to help the learner locate the gap. Explain directly only after a fair attempt.

## Readiness and scope

Before beginning, establish:

1. The material or topic to discuss.
2. The learner’s goal, such as explaining an argument, preparing for a discussion, applying a method, or evaluating a claim.
3. Their current familiarity and available time.

If the learner has not read the material, do not pretend they can retrieve it. Ask for an initial prediction, model, or question; have them inspect a relevant section; then resume the dialogue. If the source is broad, select two or three central, difficult, or consequential ideas rather than covering everything superficially.

## Conversation workflow

### 1. Activate prior knowledge

Start with one or two open questions:

- “What do you already think is true about this topic, and why?”
- “What experience or related idea does this bring to mind?”
- “What are you hoping to be able to explain, evaluate, or do by the end?”

Use the response to choose an appropriate starting point and identify likely assumptions or misconceptions.

### 2. Elicit the core idea from memory

Ask the learner to reconstruct the central claim without quoting the source:

- “In your own words, what is the main claim or finding?”
- “What problem is this idea trying to solve?”
- “Why should someone believe this conclusion?”
- “How would you explain it to a thoughtful friend in 30 seconds?”

Do not replace this step with a lecture. If their answer is vague, narrow the request: ask for the claim, its supporting reason, and its implied consequence.

### 3. Explore each key idea deeply

Use a short cycle for each selected idea:

1. Ask the learner to state or reconstruct it.
2. Probe the mechanism, assumptions, evidence, and causal reasoning.
3. Ask for a concrete example, analogy, or application they generate themselves.
4. Test it with an objection, boundary case, alternative explanation, or changed assumption.
5. Adapt the next question to their response.

Keep each turn short. Usually ask one question, or at most two closely related questions, at a time.

## Question toolkit

Choose questions that require explanation rather than recognition:

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What is the mechanism, step by step?”
- “What evidence would distinguish this explanation from an alternative?”
- “Can you build a concrete example from a familiar setting?”
- “Where might this fail or not apply?”
- “What is the strongest objection to this argument?”
- “How does this relate to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one assumption changed?”

Avoid questions answerable with only yes or no. If a brief choice is useful, immediately ask the learner to defend it.

## Responding to learner answers

Be warm, rigorous, and specific. Avoid generic praise. When an answer is strong, identify what made it useful—for example, it named an assumption, separated correlation from causation, or gave a relevant counterexample—then raise the level of challenge.

When an answer is incorrect or incomplete:

1. Do not immediately state the correction.
2. Ask a focused follow-up that exposes the tension or missing step.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, provide a concise clarification.
5. Ask them to restate the revised idea or apply it to a new case.

If the learner says, “I don’t know,” invite a low-stakes attempt: “Take a guess based on what you do know. What seems most plausible, and why?” Give a hint only after an attempt, or sooner when the task requires missing foundational knowledge.

Do not define jargon automatically. First ask what the learner thinks the term means, then refine or correct the definition as needed.

## Calibration and progress checks

Increase difficulty when answers are easy: request a counterexample, comparison, prediction, competing explanation, or transfer to a new domain. Reduce difficulty when the learner is lost: isolate one assumption, use a simpler case, provide a small hint, or ask them to compare two explanations and defend one.

Periodically give a brief, evidence-based progress check:

| Check | What to state |
|---|---|
| Demonstrated understanding | The idea the learner explained accurately and the evidence shown in their answer. |
| Remaining uncertainty | A missing distinction, unsupported assumption, or weak application. |
| Next focus | The single most useful question, concept, or practice task to address next. |

Do not claim mastery because the learner recognizes a term or repeats a conclusion. Look for accurate explanation, sound reasoning, and successful application to a fresh case.

## Closing gate

Before ending, ask the learner to convert understanding into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then request a final concise explanation, self-generated example, or future retrieval prompt. End by naming the next concept or question worth revisiting.

## Guardrails

- Do not summarize unless the learner explicitly asks; even then, invite their own summary first.
- Do not lecture when a well-designed question can prompt retrieval or inference.
- Do not make the exchange easy merely to sound encouraging.
- Do not turn the conversation into a fixed quiz; build on the learner’s actual answers.
- Do not cover an entire source at shallow depth when a few important ideas can be learned deeply.
- Match the learner’s energy: pursue depth when they are engaged, and consolidate when they are overloaded or fatigued.


---
name: write-in-my-voice
description: Draft or revise email in the user’s established voice by using an approved writing profile and verified reusable information, then produce concise, copy-ready text that preserves appropriate facts, commitments, tone, and privacy.
---

# Write in my voice

Use this workflow when the user asks to draft, reply to, revise, or polish an email on their behalf.

## Goal

Produce a copy-ready email that sounds recognizably like the user while remaining accurate, appropriate for the recipient, and limited to what the recipient needs to know.

## 1. Load the canonical voice profile

Before drafting, read the user’s current writing profile in full, if one is available. The profile may define:

- Greeting and sign-off patterns.
- Preferred level of formality and warmth.
- Typical sentence and paragraph length.
- Vocabulary, contractions, punctuation, and formatting habits.
- Phrases, tones, punctuation, or stylistic habits to avoid.
- How the user makes requests, follows up, declines, gives feedback, or handles sensitive topics.
- An approved information bank containing reusable facts, standard responses, approved links, role labels, or scheduling instructions.

Treat the profile as the primary style authority. Recent sent emails may supplement it, especially when they match the recipient and purpose of the current email. If recent examples conflict with the profile, prefer the most recent clearly approved pattern or ask the user which preference is current.

Do not expose, quote unnecessarily, or repurpose private information from the profile. Use only information relevant to the requested email and within the user’s authorization.

## 2. Establish the email brief

Identify the minimum information needed to write safely:

1. Who is the recipient, and what is their relationship to the sender?
2. What outcome should the email achieve?
3. What facts, decisions, dates, links, files, or next steps must be included?
4. What tone is appropriate: familiar, neutral, formal, firm, apologetic, or otherwise?
5. Are there deadlines, approvals, confidentiality constraints, or commitments involved?

Do not invent availability, pricing, decisions, promises, attachments, opinions, emotional reactions, or claims. If a missing detail would materially change the message, ask one focused question before drafting.

When working from private communications or records, use them only for a legitimate, authorized purpose. Read only the minimum relevant material, omit unrelated personal details, and keep the draft within the access boundary appropriate to the sender and recipient.

## 3. Apply the user’s voice without treating it as a rigid template

Follow the profile’s explicit rules. For example, if the profile specifies a particular greeting, closing, punctuation rule, or brevity standard, apply it consistently unless the user asks otherwise.

Adapt the voice to context:

- **Close colleagues or familiar contacts:** preserve the user’s normal level of brevity and familiarity.
- **New, external, senior, or sensitive recipients:** retain recognizable voice while adding enough context and care to avoid ambiguity.
- **Requests:** state the requested action, responsible party, and timing plainly.
- **Corrections, declines, or conflict:** be direct, factual, and respectful. Avoid defensive process explanations, inflated praise, or apologies that are not warranted.
- **Follow-ups:** make the needed response easy to identify without sounding repetitive or demanding.

Use approved reusable wording, links, and factual material from the information bank when they fit the situation. Do not use a canned response merely because it exists; it must remain accurate and natural in context.

## 4. Draft the smallest complete email

Write only what helps the recipient understand and act. A reliable structure is:

1. Greeting, if the user normally uses one.
2. The purpose, answer, or decision in the first sentence.
3. Essential context and the requested action or next step.
4. Closing and sign-off, if appropriate to the user’s style and the thread.

Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Put dates, choices, deadlines, and requests where they are easy to scan. Use bullets only when they improve clarity for multiple actions, options, or logistical details.

Remove material that does not add value, including:

- Generic opening pleasantries that do not fit the user’s normal style or the situation.
- Empty praise, repeated thanks, or vague reassurance.
- Throat-clearing such as “I just wanted to” when it weakens the message.
- Excessive hedging when the user has made a clear decision.
- Narration about drafting, reviewing, or internal process.
- Unnecessary personal or sensitive details.

## 5. Audit before presenting the draft

Review the draft line by line:

- Would the user plausibly write these words?
- Does the greeting, sign-off, rhythm, punctuation, and formatting match the profile?
- Is the tone appropriate for the recipient, relationship, and stakes?
- Are all names, facts, dates, links, and attachment references verified?
- Did the draft add any commitment, claim, decision, opinion, or emotion not supplied by the user?
- Is the requested action clear, including who should act and by when when relevant?
- Is the draft concise enough?
- Does it avoid the profile’s stated anti-patterns?
- Does it reveal only information appropriate for this recipient?

If the email includes a link, standard fact, or reusable response from the information bank, confirm that it is current and applicable before using it.

## Missing profile fallback

If no voice profile or usable examples are available, say so briefly and use a broadly useful default: concise, clear, warm-professional, and direct. Do not claim to imitate the user’s voice without evidence. Invite the user to provide a few representative sent emails or explicit preferences for future drafts.

## Output format

Provide the final email as copy-ready text. Ask only the specific clarification needed when a material fact is missing. Do not add drafting commentary, rationale, or multiple alternatives unless the user requests them.


---
name: professional-social-post
description: A platform-independent workflow for drafting, revising, and auditing professional social posts from source material, with strong hooks, defensible claims, useful substance, and focused publishing choices.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a rough draft, an article, a report, a transcript, a podcast, a research finding, or a simple topic.

The aim is not to make an announcement sound enthusiastic. The aim is to make the right reader stop, understand a useful point, and have a reason to care. A good post is specific, defensible, easy to scan, and useful even if the reader never opens a link.

This is platform-independent. Adapt formatting, length, link placement, and publishing mechanics to the user’s chosen platform.

## Start with a brief

Before drafting, collect or confirm the following. If the user has already supplied most of it, do not repeat questions unnecessarily.

- **Platform and format:** text post, caption, document carousel, thread, short-form article, or promotion of longer content.
- **Audience:** for example, technical practitioners, founders, customers, researchers, policy professionals, candidates, or a professional community.
- **Purpose:** share an insight, explain a concept, announce a change, promote a resource, begin a substantive discussion, or support a campaign.
- **Voice:** first-person, organizational, formal, conversational, technical, plain-English, or another stated preference.
- **Constraints:** length, required facts, forbidden phrases, formatting preferences, required terminology, and punctuation preferences.
- **Source and evidence:** notes, approved figures, quotations, documents, links, or internal facts that may be used.
- **Link plan:** whether an external link is needed and where the platform strategy places it.

If the user has an established writing guide, approved past posts, audience research, or brand guidance, treat it as the primary voice source. Do not assume a particular person’s style, a specific organization, or a particular document-storage system.

### Privacy and authorization gate

If the source contains private communications, employment history, participant records, customer information, or other personal information, confirm that the user has a legitimate purpose and clear authorization to use it.

Use only the minimum relevant source material. Exclude unrelated personal details, sensitive information, and details that the person would not reasonably expect to be published. For quotes, testimonials, personal stories, or career outcomes, confirm what may be named, attributed, or anonymized. Keep the output within the intended access and publishing boundary.

## Route the request before writing

Some post types need a dedicated approach. Identify the genre before drafting.

| Request type | Primary approach |
|---|---|
| Career or participant story | Use a case-study structure: starting point, turning point, concrete outcome, evidence, and lesson. Obtain permission for personal details. |
| Research, analysis, or evidence post | Lead with the finding, explain the evidence and limits, then state the implication. |
| Product or organizational announcement | Lead with the concrete change and why it matters to readers, not internal excitement. |
| Article, podcast, or report promotion | Lead with the strongest finding or story from the piece, not “a new article” or “a new episode.” |
| Carousel or document caption | Give the central idea and one or two strong specifics. Let the visual material carry the fuller breakdown. |
| Strategy or positioning post | Explain the deliberate trade-off, the reason for it, and the consequence. |

If the genre is unclear, ask one concise routing question. If the post is a sensitive personal case study, clarify consent and disclosure choices before proposing hooks.

## Non-negotiable accuracy rules

1. **Do not invent facts.** Never fabricate statistics, names, organizations, job titles, dates, research findings, quotations, testimonials, customer outcomes, or credentials.
2. **Separate evidence from interpretation.** State what the source establishes, then make clear what is your conclusion, recommendation, or hypothesis.
3. **Preserve meaningful uncertainty.** If results depend on assumptions, broad ranges, weak evidence, correlations, or a preliminary model, say so plainly.
4. **Use specific details only when supported.** Exact figures, roles, dates, mechanisms, and outcomes are stronger than vague language when they are verified. Do not turn a rough estimate into falsely precise language.
5. **Ask for missing support early.** If a key claim cannot be substantiated, ask for a source, narrow the claim, identify it as an opinion, or remove it.
6. **Avoid misleading urgency.** Do not inflate stakes for attention. A concrete risk plus a practical response is more credible than broad catastrophe language.
7. **Respect context.** Do not quote selectively in a way that changes a speaker’s meaning or use personal stories as proof of a broad claim without appropriate limits.

## Audience and voice

Write for the reader most likely to care or act, not for everyone who might vaguely relate. Specificity is a useful filter: it helps the intended reader recognize that the post is for them.

Use this broadly useful default voice unless the user provides a different one:

- Direct, clear, and conversational.
- Short sentences with concrete nouns and plain verbs.
- Active voice where it improves clarity.
- One main claim per sentence.
- Sober about problems and practical about responses.
- Confident only to the degree the evidence supports confidence.
- Specific rather than promotional.

Avoid these common modes.

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are delighted to announce an exciting new initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences with unexplained terms and side arguments. | State the point plainly, then explain necessary terms in ordinary language. |
| Alarmist | Broad danger language without a mechanism, evidence, or response. | Name the specific risk, its basis, its uncertainty, and a proportionate intervention. |
| Motivational | General encouragement without a decision, example, or method. | Give a concrete action, trade-off, framework, or observed result. |

## Core workflow

### 1. Inspect the source before choosing the format

Do not begin with a template. First identify the strongest material in the source.

Look for:

- An unusual or surprising fact.
- A specific number that creates tension.
- A counterintuitive but defensible conclusion.
- A concrete before-and-after outcome.
- A meaningful strategic trade-off.
- A sharp disagreement between credible views.
- A useful framework, checklist, or model.
- A sentence that changes how the reader sees the issue.

The title or headline of a source is often not the best social-post angle. The strongest thread may be a specific detail buried in the middle.

If several angles are plausible, do not silently choose. Present two to four options and let the user choose when the distinction matters.

> I see several viable angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [story, outcome, or disagreement]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Choose one primary thread. A social post should not attempt to summarize every point in a report or conversation.

### 2. Generate hooks before drafting the body

The opening decides whether readers continue. Generate five to ten possible hooks before selecting one. When user input would be useful, show a numbered shortlist of three to five hooks, each with a short note about its strategy.

A hook must make an honest promise that the post fulfills. It should make sense on its own, even to a reader who has not seen the source material.

Useful patterns include:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific body of evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Named outcome:** “[Person or role] moved from [starting point] to [specific outcome] in [timeframe].” Use only with evidence and permission.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only if the post supports it.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused disagreement:** “Why do two credible groups reach different conclusions about [specific issue]?”

| Hook | Strategic purpose |
|---|---|
| “[Specific finding that challenges a familiar assumption].” | Leads with a concrete result and creates a reason to continue. |

Run the swap test: if the key noun could be replaced with “marketing,” “leadership,” or another unrelated topic and the hook still works, it is too generic. Add the mechanism, number, outcome, or topic-specific tension.

Avoid:

- “Excited to share,” “thrilled to announce,” and similar announcement framing.
- Throat-clearing such as “In today’s fast-moving environment.”
- Empty cliffhangers that do not deliver a payoff.
- Several rhetorical questions in sequence.
- Generic motivational statements.
- Clickbait claims such as “You will not believe this.”

### 3. Select one structure

Choose the structure that matches the material. Do not combine several structures without a clear reason.

1. **Counterintuitive claim → evidence → implication**  
   Best for research, data, and arguments. Start with the surprise, show the evidence, then explain what should change.

2. **Changed mind → trigger → updated view → takeaway**  
   Best for first-person thought leadership. State the prior belief, explain what changed it, and give the updated conclusion.

3. **Problem → why it matters → practical response**  
   Best for explainers and operational or policy topics. Keep both the problem and the response concrete.

4. **Result → how it happened → reusable lesson**  
   Best for launches, team outcomes, and approved case studies. The result must be real and specific.

5. **Framework → examples → application**  
   Best for material readers may save and revisit. Use a framework name only if it clarifies the idea.

6. **Specific announcement → reader relevance → next step**  
   Use when the announcement is genuinely notable. Lead with what happened and its relevance, not organizational pride.

7. **Strategic trade-off → rationale → consequence**  
   Best for explaining a deliberate constraint or “anti-goal”: something the organization has chosen not to optimize for in order to protect a more important aim.

### 4. Draft: hook, tension, payoff, close

Use this default body shape:

- **Hook:** the strongest claim, result, or tension.
- **Tension or setup:** why it matters, why it is surprising, or what assumption it challenges.
- **Payoff:** the evidence, story, model, examples, or practical lesson. Deliver value in the post itself.
- **Soft close:** exactly one focused question, practical takeaway, or pointer to more material.

A useful default is under 300 words, but length should follow substance and platform norms. Every extra paragraph must earn its place.

Use white space. One- or two-sentence paragraphs are easier to scan on a phone. Use bullets only where the content is genuinely list-shaped, such as three lessons, four findings, or a checklist. Do not force prose into bullets merely to look structured.

For a carousel or document caption:

- State the central idea in the caption.
- Include one or two meaningful specifics.
- Explain what the visual material adds.
- Do not turn the caption into a slide-by-slide summary.

For an article, report, or podcast promotion:

- Put the strongest finding or story in the post body.
- Use the longer piece for depth, sources, methodology, and secondary points.
- Follow the chosen platform’s link-placement strategy.
- Never make “read the link” the main value proposition.

## Calls to action and questions

Use one close only. A good close gives readers a bounded, real reason to respond or continue.

Strong examples:

- “Which constraint is hardest to manage in your work?”
- “What evidence would change your view?”
- “If you have operated a similar system, where does this model fail?”
- “The full analysis includes the assumptions and source material.”

Weak examples:

- “Thoughts?”
- “Let me know what you think.”
- Multiple questions at once.
- Requests to comment, tag, repost, or react purely to increase engagement.

A question should invite knowledge, disagreement, or experience. Do not use engagement bait.

## Editing pass: remove templated language

Run a separate editing pass after drafting. Cut phrases that sound polished but add little.

Replace or remove:

- Corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” “cultivate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Hedging frames such as “it is worth noting,” “one might say,” and “arguably,” unless the uncertainty itself matters.
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Abstract nouns such as “journey,” “transformation,” and “paradigm” when a concrete event can be named.
- Transition sentences that merely restate the preceding paragraph.
- Dramatic frames such as “The truth is” or “Here is the reality.” State the point directly.
- Decorative formatting that the target platform will not render reliably.

Obey user-specified punctuation constraints. Otherwise, favor periods, commas, and line breaks over theatrical punctuation. Use emphasis sparingly, and verify that any special formatting will display correctly on the chosen platform.

Read the post aloud. If it sounds like a generic thought-leadership template rather than a person making a specific point, rewrite it.

## Revision protocol

When the user gives feedback, revise the requested line and the nearby logic first. Do not rewrite the whole post unless asked.

- If the hook is not sharp enough, offer several replacement hooks before rebuilding the body.
- If a claim feels overstated, strengthen its evidence, narrow it, or soften only that claim.
- If a paragraph feels slow, cut setup before adding explanation.
- If a prior line was stronger, preserve it unless the user explicitly wants it changed.
- If a sentence is uncertain, say so. Offer a concrete alternative rather than presenting weak material as polished.

Multiple small options are often more useful than one complete redraft, especially for hooks, closers, and disputed claims.

## Readiness gate and audit

Do not present a post as final until it passes the following checks.

- Does the first line earn attention when read alone?
- Is the post about one clear point rather than several competing ideas?
- Does it contain at least one relevant concrete detail, outcome, mechanism, example, or number?
- Can a knowledgeable reader challenge the main claim without exposing unsupported reasoning?
- Does the post provide value without requiring a click, swipe, or purchase?
- Is uncertainty stated where it materially changes the conclusion?
- Is the language specific to this topic rather than reusable across unrelated industries?
- Is the close one focused action, question, or pointer?
- Are names, quotes, figures, and personal details authorized and supported?
- Does the formatting work on the intended platform?
- Is the tone professional, respectful, and appropriate for the audience?
- Have irrelevant or sensitive personal details been removed?

If any answer is no, revise before handoff.

## Handoff format

Present only what helps the user decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen delivery format or location.
3. Any unsupported claim, missing input, or remaining soft spot.
4. Suggested first-comment or link text, if relevant to the platform strategy.
5. One concise publishing reminder appropriate to the platform, such as responding promptly and substantively to genuine early comments.

Do not claim that any format, posting time, engagement tactic, or metric is guaranteed to improve reach. Platform behavior changes. Treat distribution guidance as a testable hypothesis and compare results across multiple posts.

## Common failure patterns

- **Announcement disguised as content:** The post says the organization is pleased, but not why readers should care. Lead with the actual change or lesson.
- **Pure teaser:** The post asks for a click but gives no useful insight. Share the main finding and use the linked piece for depth.
- **Unsupported precision:** A striking number appears without source, scope, or caveat. Verify, qualify, or remove it.
- **Generic inspiration:** The post is positive but contains no mechanism, example, action, or trade-off. Name the concrete point.
- **Overpacked summary:** The post tries to cover every section of a source. Choose one thread and save the rest for later content.
- **Bolted-on promotion:** A course, product, or service appears at the end without a natural connection. Remove it, create a separate promotional post, or make the connection immediate and concrete.
- **Forced engagement:** The post demands reactions or comments. Ask one genuine question or end with a useful conclusion.
- **Sensitive oversharing:** A post includes more personal history or identifying detail than the point requires. Remove nonessential details and confirm permission.

The final standard is simple: the post should sound like someone with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, or a generic social-media template.


---
name: case-study-post
description: Create an evidence-based case study post about a person’s professional, learning, or career change, with verified story beats, alternate hooks, quote-card options, approval checks, and a review-ready draft.
---

# Write a case study post

Use this workflow to turn authorized source material about a person into a concise, credible public case study. It works for professional social posts, community updates, newsletters, program alumni stories, recruitment content, and similar formats.

The goal is not vague praise. Show a specific and truthful change: where the person started, why they acted, what concretely helped, what happened next, what they do now, and what a reader can do next.

A strong case study gives the intended reader a recognizable before-state. It explains a plausible mechanism without claiming that a program, community, employer, mentor, or resource caused more than the evidence supports.

## When to use this workflow

Use it when you have raw material such as interviews, application responses, approved profiles, work samples, authorized announcements, notes, or a previous draft, and need a first draft that an editor can lightly revise.

Before using private communications, internal records, or information about an identifiable person, confirm all of the following:

- There is a legitimate purpose for creating the post.
- You have clear authorization to access and use the relevant material.
- The subject reasonably expects the information to be used for this purpose, or you will obtain their approval before publication.
- You will use only the minimum sources and details needed for the story.
- The draft and supporting notes will stay within the appropriate access boundary.
- The final post will not disclose unrelated private facts, confidential work, or details that would surprise the subject.

Do not use this workflow to infer sensitive facts about a person, expose nonpublic career information, or make public claims based only on private material without appropriate permission.

## Inputs and intake gate

Request all available relevant material and identify the publishing context before drafting. Possible inputs include:

- Interview transcript, call notes, or an approved meeting summary
- Application, intake form, or written statement from the subject
- A current professional profile or approved biography
- Public work samples, published work, project descriptions, or official announcements
- An authorized internal update reporting a result
- The subject’s own notes, outline, or prior draft
- Editorial or brand voice guidance
- Target audience, platform, post objective, and call to action

Do not assume that an automated transcript, summary, or informal message is accurate enough to publish directly. Ask focused questions before drafting if critical facts are missing.

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, relevant pronouns, and consent status |
| Before-state | Previous role, field, goal, uncertainty, constraint, or relevant alternative path |
| Trigger | Why the person joined, applied, changed direction, or took action then |
| Intervention | Program, community, event, mentor, product, resource, or experience involved |
| Mechanism | Concrete help, such as an insight, introduction, opportunity, feedback session, or resource |
| Now-state | Current role, approved workplace description, project, output, or result |
| Timeline | Dates or intervals from starting point to outcome |
| Evidence | Verified roles, figures, dates, artifacts, and direct quotes |
| Cost or risk | Career change, move, financial tradeoff, uncertainty, or other meaningful constraint |
| Audience and CTA | Who the post should help or persuade, and one clear next action |

### Questions to ask when information is incomplete

1. What was the person doing before this experience?
2. What were they considering instead, if anything?
3. Why did they act at this point rather than later?
4. What one or two concrete things helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a project, publication, product, placement, grant, or other result that can be named publicly?
8. Did they take on a meaningful cost or risk that they are comfortable sharing publicly?
9. Which names, figures, direct quotes, and claims are approved for public use?
10. Who should see themselves in this story, and what should they do after reading it?

Do not guess at workplace names, job titles, team names, project titles, dates, figures, timelines, or outcomes. If a fact would strengthen the post but cannot be verified, ask for it or leave it out.

## Evidence and verification rules

Never invent facts or upgrade claims for drama. If a source says a person contributed to a project, do not call them the lead. If it says they explored an opportunity, do not say they received an offer. If it says they co-authored work, do not imply sole authorship or leadership.

Treat automated transcripts as useful but fallible. They can mishear names, workplaces, technical terms, numbers, job titles, and quotes. Cross-check publication-critical details against more reliable sources.

Use this source order unless there is a clear reason to do otherwise:

1. The subject’s direct, recent confirmation
2. Official public records, published work, or an authorized organizational record
3. A current professional profile maintained by the subject
4. An original application or written statement from the subject
5. Interview notes or automated summaries
6. Informal third-party messages

In working notes, separate these three statement types:

- **Verified fact:** A role, date, artifact, figure, or quote supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn from the story. Use it only when the evidence supports it, and phrase it modestly.

Do not claim that an intervention caused the entire outcome unless the subject and evidence clearly support that claim. Prefer language such as “the program helped them see the field differently,” “they found the opportunity through the community,” or “the feedback improved their application.”

When sources conflict, resolve the conflict before publication. A current subject confirmation or official source normally takes priority over an automated transcript. Do not quietly choose the version that makes a better story.

## Sensitive-content approval gate

Flag the following for explicit subject approval before publication, even when they appear in an interview or internal record:

- Salary, compensation comparisons, pay cuts, financial hardship, or debt
- Health, disability, family, relationship, immigration, legal, or safety-related circumstances
- Criticism of a former workplace, colleague, role, or career decision
- Unreleased work, confidential projects, unpublished titles, or nonpublic hiring information
- Direct quotations, especially strong opinions or criticism
- Claims about why an employer selected the person
- Specific timelines that could reveal private circumstances
- Claims about personal identity, motivation, or values not clearly stated by the subject

If approval is unavailable, use an approved and truthful fallback or remove the line. For example, replace an exact compensation comparison with “they accepted a lower-paying role” only if the subject approves that broader statement. Do not conceal uncertainty by making the story more dramatic.

## Build the story beats

Create a private working outline before writing. Keep sensitive source details out of the final post and review message unless they are needed, approved, and appropriate for the publishing context.

### 1. Before-state

Capture the person’s role, background, and reader-relevant uncertainty. Include an alternative path they were considering only when it helps the reader recognize their own situation.

Keep details that move the story. Cut reading lists, long credential histories, and unrelated biography unless a detail explains the decision or makes the change credible.

### 2. Trigger

Identify why the person acted at that time. They may have wanted to understand a field, test whether a career path was available, find collaborators, solve a practical problem, or make a values-driven decision.

### 3. Mechanism

Find one or two observable turning points. Strong mechanisms include:

- Realizing that a field or role was open to someone with their background
- Seeing a relevant opportunity in a professional community
- Receiving an introduction or having a conversation that clarified next steps
- Getting feedback that improved an application, project, or portfolio
- Finding a practical workshop, resource, or event that enabled action

Avoid saying that an experience was transformative. State what happened instead.

### 4. Now-state

Record the current role, an approved workplace or team description if needed, and what the person actually does. Translate specialized language enough for the intended audience to understand the work.

Use named outputs only when they add real proof or interest. One relevant project, publication, product, placement, or grant is usually stronger than a long credential list.

### 5. Timeline and compression

Map the sequence from the intervention or starting point to the result. Use a short, truthful timeframe when it sharpens the story, such as “within six months” or “the following year.” Do not force a compressed timeline when the evidence does not support it.

### 6. Quotes

Extract three to five candidate quotes verbatim. Favor quotes that express the reader’s likely uncertainty, not only the subject’s achievement.

Useful categories are:

1. **Discovery:** “I did not know this path was open to someone like me.”
2. **Mechanism:** “I found the opportunity through the community.”
3. **Conviction:** “I would make the same choice again.”

Light trimming is allowed only if it preserves the person’s exact meaning and grammar. Do not rewrite a quote into a cleaner or stronger statement than the person made.

## Generate three hook options

For feed-based platforms, the first two lines determine whether a reader continues. Write three distinct hooks before drafting the full post. Keep each to two short sentences and, where useful for the platform, around 140 characters or fewer.

### Hook A: Discovery

Use when the audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a concrete mechanism.

This is the default recommendation when the post needs the reader to think, “That could be me.”

### Hook B: Identity collision

Use when the before-and-after contrast is vivid and accessible.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This often works well for a broad audience that may not share the subject’s exact blocker.

### Hook C: Stakes-led

Use only when a meaningful cost or risk is approved and the audience will understand it as informed conviction rather than as a warning that the path is inaccessible.

**Formula:** The subject accepted a specific cost to take a concrete action. Now they are doing meaningful work or pursuing a specific result.

Choose one hook as the recommendation. State in one sentence why it suits the target audience, and briefly state why each alternative is less suitable. Do not use a sacrifice hook merely because it is dramatic.

## Draft the post

Aim for roughly 160 to 220 words unless the platform, audience, or format calls for another length. Shorter is usually stronger.

Use this sequence:

1. **Hook:** Use the recommended hook.
2. **Before-state:** One short paragraph with the subject’s previous situation and a relevant alternative path.
3. **Name the intervention:** Clearly state that they joined the program, used the resource, or took part in the community. Do not leave this connection implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then land the immediate result in plain language. A concise sequence such as “They applied. They got in.” can work when supported by evidence.
5. **Current work:** State what they do now and why it matters in understandable terms.
6. **Optional honest cost:** Include only when approved and genuinely useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already carried by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

If a platform may reduce distribution for external links in the post body, use a comment, profile destination, or designated landing page instead. Treat this as a platform-specific publishing choice, not an unverified universal rule.

## Style rules

Adapt to the selected editorial voice. If no voice guide exists, use these broadly useful defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use concrete names, roles, dates, and figures only when verified and approved.
- Use the subject’s first name after the initial full introduction only if it fits the publication’s tone and the subject’s preference.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not label someone exceptional, inspiring, or brilliant when facts can show their work.
- Use contractions if the voice is conversational.
- Keep the CTA in full second person, such as “If you are…” and “you can…”
- Avoid emojis unless they are an explicit brand choice.
- Do not use em dashes. Use periods, commas, parentheses sparingly, or line breaks instead.

On the final pass, remove common machine-like phrasing:

- Empty transitions that restate the preceding sentence
- Slow date-first openings that delay the actual hook
- Corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “cultivate”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably”
- Abstract nouns that replace evidence, such as “journey,” “transformation,” or “paradigm”
- Hedging and softeners, including “it is worth noting,” “arguably,” “just,” and “ultimately”
- Artificially balanced constructions such as “on one hand, on the other hand”
- Dramatic frames such as “The truth is:”
- Reflective summary sentences after the CTA

Read the draft aloud. If it sounds like generic thought leadership, cut it and replace abstractions with verified details.

## Graphic quote options

Provide three options for a visual quote card. Each should be self-contained, ideally under 15 words, and drawn verbatim from approved source material.

Offer one from each category:

- Discovery
- Mechanism
- Conviction

Recommend one quote with a one-sentence rationale. Discovery quotes often work best because they make sense without surrounding context and mirror the reader’s uncertainty. Choose a mechanism or conviction quote instead only if it is clearer and more memorable on its own.

## Readiness audit

Before sending the draft for review, verify the following:

- Every name, role, date, figure, workplace description, and title is verified.
- Transcript-derived details have been cross-checked where necessary.
- The post identifies a concrete mechanism, not only an outcome.
- It does not overstate causation.
- The intervention is named clearly.
- The opening reflects a real audience concern.
- The current work is understandable to the intended reader.
- Sensitive claims and direct quotes are flagged for approval.
- The CTA is clear and directed at the intended reader.
- The draft has no em dashes, unsupported superlatives, corporate phrases, or generic filler.
- The post stays within the authorized publishing scope and omits unrelated private details.

## Delivery format

Create the draft in the user’s chosen document system when available. Use a clear, searchable title such as:

`[Date]: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and the two alternatives
- The three graphic quote options and a recommendation
- A list of items requiring subject approval
- A list of missing information that would strengthen the post
- The document location or link, if applicable

Do not treat the first draft as final. If feedback says “make the hook better,” generate new hooks rather than making tiny edits. If asked to make it shorter, cut secondary biography first while preserving the mechanism and outcome. If the subject rejects a sensitive line, replace it with an approved fallback without weakening the entire story.

## Improve the workflow from feedback

After the final version is accepted or the review cycle clearly ends, review feedback for reusable lessons. Update the workflow only when a recurring pattern is clear, such as a missing intake question, a consistent voice preference, a structural change that repeatedly improves clarity, or a verification issue that appears more than once.

Do not create new rules from a clean review cycle or from one editor’s one-off preference. Preserve the evidence, approval, privacy, and access-boundary gates even when a faster draft is requested.


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
description: Gather authorized, relevant context; clarify the meeting owner’s intended outcome; and create a structured meeting-preparation record with a practical agenda, decision-relevant questions, and follow-up plan.
---

# Prepare for a meeting

Use this workflow when someone asks to prepare for a meeting, review a day of meetings, or create a meeting brief. The deliverable is a saved preparation record in the user’s chosen workspace, not merely a chat summary.

This workflow is intended for legitimate work purposes. Only access calendars, messages, documents, notes, and people-related records when the user is authorized to access them and the information is relevant to the meeting. Use the minimum necessary sources and details. Do not copy unrelated personal information, sensitive information, or private employment details into a broadly visible meeting record.

## Outcome

For each selected meeting, produce a preparation record that helps the meeting owner:

- Reload the relevant relationship and meeting context quickly.
- Know why the meeting is happening now.
- Decide what outcome to pursue.
- Follow a realistic, time-bounded agenda.
- Ask the few questions that matter most.
- Close with a specific next step, decision, owner, or artifact when appropriate.

The preparation record should be saved in a shared or private system chosen by the user, such as a notes database, document workspace, CRM, or meeting-management tool. Match the access level of the destination to the sensitivity of the material.

## 1. Establish scope and select meetings

Ask for or infer the target date and meetings to prepare.

Useful defaults:

- Default date: the user’s local current date.
- Default meeting set: external meetings, candidate or partner meetings, customer meetings, and small decision-making groups.
- Usually exclude personal blocks, focus time, routine internal ceremonies, and events with no substantive attendees unless the user asks to include them.

For every selected meeting, collect the invitation details:

- Title and scheduled start/end time.
- Attendees and their organizations or roles, where available.
- Location or call link, if useful to the meeting owner.
- Invitation description and stated purpose.
- Attached or linked material.
- Scheduling context, such as an introduction, rescheduling note, prior commitment, or stated decision deadline.

Do not assume a meeting title explains the real purpose. A short title such as “Catch-up” can conceal a hiring decision, proposal review, partnership discussion, escalation, or request for advice.

## 2. Research the relevant context

Research should be proportional to the stakes and limited to authorized sources. Start with the sources most likely to explain the relationship and the immediate reason for the meeting. Recent direct evidence generally matters more than old summaries.

For each external attendee or principal participant, gather enough information to answer:

1. Who are they and what is their relevant role?
2. What does their organization, project, or team do that matters here?
3. What is the relationship history with the meeting owner or organization?
4. Why is this meeting happening now?
5. What commitments, decisions, unresolved questions, or tensions carry into the call?
6. What timely context may change the conversation?

### Source review sequence

Use the available, authorized capabilities in parallel where practical.

1. **Direct correspondence**
   - Search messages exchanged directly with the person.
   - Review several recent, relevant messages rather than relying on search snippets.
   - Look for commitments, asks, concerns, introductions, deadlines, and changes in position.

2. **Indirect mentions**
   - Search for the person’s name and, when useful, their organization or project name.
   - This may reveal context not visible in direct correspondence, such as introductions, prior discussions, feedback requests, or planning threads.
   - Treat indirect claims carefully. Distinguish verified facts from someone else’s view.

3. **Internal notes and prior meeting records**
   - Search the user’s authorized workspace for prior meetings, relationship notes, decision logs, project documents, and relevant account or candidate records.
   - Summarize the relationship arc for recurring contacts rather than repeating only the last interaction.

4. **Calendar history**
   - Check for previous meetings involving the same attendees.
   - Identify whether this is a first meeting, a recurring working session, a follow-up after a specific event, or a long-delayed reconnection.

5. **Public information**
   - When useful, review reliable public sources for the attendee’s current role, organization, published work, and recent relevant announcements.
   - Save only links that help the meeting owner prepare. Do not gather personal trivia.

6. **The artifact at issue**
   - If the meeting concerns a proposal, deck, memo, draft agreement, plan, report, design, or other written artifact, read the artifact before drafting an agenda.
   - Read the complete relevant artifact, including sections, appendices, comments, and linked material needed to understand the core argument.
   - If the artifact is unavailable but clearly central to the meeting, ask the user for access or a link before pretending to prepare a substantive review.

A generic agenda is a failure when the meeting exists to discuss a specific written proposal. Anchor the preparation in the actual claims, assumptions, choices, risks, and open questions in that artifact.

### Research synthesis

Create concise research notes under these headings:

- **Who they are:** Relevant role, organization, and background.
- **Relationship history:** Prior meetings, commitments, introductions, and notable interactions.
- **Why now:** The scheduling trigger and immediate purpose.
- **Current situation:** Known constraints, deadlines, alternatives, decisions, or unresolved issues.
- **Relevant links:** Only useful public or authorized internal references.
- **Open unknowns:** Important facts that are unclear or based on conflicting evidence.

Do not state inferences as facts. Label uncertain points clearly, for example: “It is unclear whether they are still evaluating alternatives” or “The current decision owner is not confirmed.”

## 3. Route specialized meetings correctly

Before using a general meeting-prep structure, determine whether the meeting needs a specialized workflow.

Examples include:

- A reference or background conversation related to a candidate or appointment.
- A formal performance, disciplinary, legal, or compliance discussion.
- A negotiation governed by a standard approval process.
- A customer escalation with an established incident or account-review process.

For a reference conversation, use an authorized reference-check workflow rather than a generic agenda. Focus on role-relevant capabilities, observed work, collaboration patterns, scope, and diagnostic evidence. Avoid irrelevant personal details and do not include sensitive hiring information in a broadly accessible meeting record.

If no specialized workflow applies, continue with the general process.

## 4. Provide a situation brief before proposing an agenda

Do not jump directly from research to an agenda. First provide a short situation brief so the meeting owner can correct the context and make the key strategic choices.

Choose the brief format based on the meeting.

### Narrative brief

Use for most meetings. It should take about a minute to read and cover:

- Who the participant is.
- Where the relationship stands.
- Why the meeting is happening.
- The main live tensions, opportunities, or unknowns.

### Decision-shaped brief

Use when the meeting is fundamentally about a decision, close, recruitment, negotiation, or other situation with competing options. Cover:

- The ask or desired movement.
- Their likely alternatives and known timing.
- The meeting owner’s position, leverage, and constraints.
- Main risks.
- What remains unknown.

For a high-stakes meeting, combine a short narrative brief with a decision-shaped section.

Keep the brief factual and usable. Do not bury the meeting owner in raw search output. Do not write an agenda yet.

## 5. Ask targeted questions that shape the agenda

After sharing the brief, ask focused questions. The goal is not to ask the user to write the agenda; the goal is to learn the desired outcome, boundaries, and failure modes so the workflow can write it well.

Ask at least:

- One question about the primary outcome.
- At least one question about a failure mode, tone, or concrete ask.
- One catch-all question that lets the user add omitted context or constraints.

Use only the questions that genuinely change the preparation. Typical axes include:

- **Primary outcome:** What should be true by the end of the meeting?
- **Their situation:** Is there uncertainty about their role, commitment, authority, or alternatives?
- **Sensitive substance:** Should the meeting owner state a view, test the other party’s view first, or avoid a topic?
- **Failure mode:** What would make the meeting go badly: overselling, underselling, losing focus, creating false expectations, or failing to close?
- **Specific ask:** Is there an introduction, decision, commitment, time allocation, artifact, or follow-up to secure? How direct should the ask be?
- **Anything else:** What should be landed, avoided, or remembered that is not covered above?

### Question format

Make questions quick to answer and auditable. Number questions continuously and label every option with the question number and a lowercase letter. Provide three or four mutually exclusive choices where possible. Put the most likely or recommended option first, but include meaningful alternatives.

Example:

```markdown
1. What is the primary outcome?
   - **1a (recommended):** Test their interest and agree a concrete next step.
   - **1b:** Build the relationship without making a direct ask.
   - **1c:** Seek a decision during this meeting.

2. What should be avoided?
   - **2a (recommended):** Do not commit before understanding their constraints.
   - **2b:** Do not spend most of the meeting on background.
   - **2c:** Do not raise the proposal unless they do first.

3. Is there anything else to land or avoid?
   - **3a:** Nothing to add.
   - **3b:** I will add notes or context.
   - **3c:** I need to discuss a constraint before the agenda is drafted.
```

If more than four questions are necessary, use multiple rounds. Ask questions whose answers change later options first. For example, whether the meeting owner has authority to make a decision may determine which closing options are useful.

Before sending questions, check that:

- Every question is numbered.
- Every option has one unique matching label.
- Labels are sequential and unambiguous.
- The catch-all question is included in the final round.
- No option creates a false either/or when both actions could reasonably be combined.

A clarification round may be skipped only when the meeting purpose, goal, and recurring structure are genuinely settled and documented. When uncertain, ask; an agenda built on the wrong assumption is more costly than one short question round.

## 6. Create the saved meeting-preparation record

Only draft the final record after the user has answered the agenda-shaping questions, unless the clarification round was legitimately unnecessary.

Create the record in the user’s selected system with appropriate metadata. Use date-only fields for the meeting date unless the system has a separate, intentional time field. Use a clear title such as the date plus attendee name or meeting topic. Add authorized participants according to the workspace’s sharing model.

Verify that the saved record has the intended title, date, location, access boundary, and content. Repair obvious metadata errors before declaring the task complete.

Use this content structure:

```markdown
# [Meeting title]

## Context

- Who the participant is and why they are relevant.
- Relationship history and important prior commitments.
- Why this meeting is happening now.
- Relevant links and the specific artifact under discussion, if any.
- Timely context or open unknowns.

## Goal

[One concise statement of the desired meeting outcome, based on the user’s answers.]

## Agenda

### 0–5 min: Open and frame

**Say**

[An example opening that establishes purpose and desired shape of the conversation.]

**Facilitator note**

[What to avoid or what signal to establish early.]

### 5–20 min: Diagnose [topic]

**Questions**

1. [Decision-relevant question.]
2. [Question that tests assumptions, needs, or constraints.]

**Facilitator note**

[What evidence to listen for and what not to assume.]

### 20–35 min: Discuss, test, or propose [topic]

**Say**

[Transition or concise proposal.]

**Questions**

1. [Question that pressure-tests the proposal or explores the gap.]

**Facilitator note**

[Specific move, boundary, or contingency.]

### 35–45 min: Close and create momentum

**Questions**

1. [A specific close for a decision, owner, date, artifact, or next meeting.]

**Facilitator note**

[Fallback close if a decision cannot be made now.]

## Five most important questions to ask

1. [Most decision-relevant question.]
2. [Second most important question.]
3. [Question that tests the crucial uncertainty or gap.]
4. [Question that identifies constraints, decision process, or ownership.]
5. [Specific forcing-function close: date, artifact, owner, or next step.]

## Follow-up to capture

- Decision or current status:
- Owner:
- Next artifact or action:
- Due date:
- Remaining risks or open questions:
```

Adapt the time blocks to the actual meeting duration. The agenda must add up realistically. Put the most important issue before routine updates or broad background.

For first meetings, say explicitly that it is a first meeting. For recurring relationships, summarize the arc and the change since the last meaningful interaction.

## 7. Apply agenda-writing standards

The agenda is a meeting aid, not a transcript. It should be detailed enough to use before and during the call without becoming a script the user must read aloud.

Use these rules:

- Make each agenda stage a heading, not a list item.
- Use **Say**, **Questions**, and **Facilitator note** labels consistently.
- Write spoken prompts without quotation marks.
- Number spoken questions.
- Keep facilitator guidance compact and action-oriented.
- Include actual transitions and closes for consequential conversations.
- Ensure the “Five most important questions” section contains exactly five ranked, one-line questions with no sub-bullets.
- Include at least one gap-testing question and one forcing close for a meeting intended to move a decision, commitment, or relationship forward.
- If the meeting is purely informational, use all five questions for discovery and do not manufacture a sales-style close.

Never include compensation figures, compensation bands, personal medical information, protected personal characteristics, credentials, account details, or other sensitive details in a shared meeting record. If sensitive context is essential, use an approved private channel or refer to it at a high level, such as “offer follow-up” or “private employment consideration,” without recording unnecessary specifics.

## 8. Plan post-meeting review when persuasion or a decision matters

For recruiting, fundraising, sales, partnership, negotiation, or other high-stakes conversations intended to move a counterparty, schedule or recommend a short post-meeting review after the meeting, subject to the user’s tools and authorization.

The review should use the meeting notes or authorized transcript and answer:

- What outcome was achieved?
- What did the other party actually say, decide, or commit to?
- Which assumptions were confirmed or disproved?
- Which questions produced useful diagnostic evidence?
- Where did the meeting owner miss a signal, over-explain, rush, or fail to close?
- What is the next action, owner, artifact, and date?
- Is there a recurring communication or decision pattern worth tracking?

Store reviews in an appropriate private coaching or operating location, not in a broadly shared meeting database unless that access is suitable.

## Final readiness gate

Before marking preparation complete, verify:

| Check | Pass condition |
|---|---|
| Meeting selection | The meeting is substantive and within the requested scope. |
| Authorization | Sources and records were accessed for a legitimate purpose with appropriate permission. |
| Artifact review | Any central proposal, memo, deck, or document was read, or its absence was surfaced. |
| Context quality | The brief explains who, why now, relationship history, and meaningful unknowns. |
| Clarification | The meeting owner answered targeted questions, unless the purpose and agenda were already genuinely settled. |
| Agenda quality | The agenda is time-bounded, outcome-led, and includes a workable close. |
| In-call utility | Exactly five ranked decision-relevant questions are present. |
| Privacy | The saved record excludes unnecessary sensitive or unrelated personal information. |
| Record integrity | The page or record was created, saved, checked, and shared only within the appropriate access boundary. |

Do not report the task as complete merely because research is complete. It is complete when the verified preparation record is saved and ready for the meeting owner to use.


---
name: capture-meeting-actions
description: Review authorized meeting records to identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow for a daily sweep, a selected date range, or a manually supplied set of meetings.

The goal is not to turn every discussion into work. Each meeting should produce zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose, authorization, and operating rules

Use meeting records only for a legitimate work purpose and with clear authorization to access them. Use the minimum relevant sources and details needed to identify commitments. Do not copy unrelated personal, confidential, health, compensation, performance, or sensitive relationship information into tasks. Keep task content within the access boundary of the chosen task system.

Before each run, apply these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text**: strongest evidence of who agreed to do what and when.
2. **Human-written notes**: useful supporting evidence, especially explicit action sections.
3. **Automated summary**: useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda**: describes intended discussion, not a commitment.

Automated summaries often misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels it as an action item. Confirm ownership in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work that was completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, statement of interest, or open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply known responsibility and delegation boundaries supplied by the user or organization. Attendance at a meeting does not make the user accountable for all work in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this broadly useful default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect:

- Title, date, and time
- Meeting-record link or identifier
- Attendees, if available and relevant
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

If a person says they will send a document and the document is actually shared, drafted, or completed during the meeting, treat it as completed. Do not create a duplicate task merely because the transcript contains the promise.

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
- Source and related links that the task audience is authorized to access

Create no task when work was completed live, another person owns it, the meeting was purely informational and needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

## 4. Decide the task shape

Combine actions into one task when they have the same counterparty, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect months later.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

This is a readiness gate. Do not proceed to task creation until each proposed task has a clear owner, unfinished outcome, sensible shape, and enough context to stand alone.

## 5. Write the task

Use the user’s chosen task system and field names. At minimum, capture:

- **Title:** short, verb-led, and specific, such as “Follow up with partner about pilot scope.”
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user’s scale; default to normal important work and reserve the highest level for a real deadline, material risk, or waiting counterparty.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and authorized links.

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
dates, why this matters, the commitment, and any necessary sensitivity.
Omit unrelated or sensitive personal details.]

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
- Meeting record: <authorized-link>
- Related document: <authorized-link>
```

Use time-independent wording: write “On 23 Apr, you agreed to…” rather than “Earlier today…”. If the task is to send a message, write a ready-to-send draft rather than merely saying “email them.” Follow the user’s known writing preferences; otherwise use concise, warm, professional language with a clear request or promised deliverable.

For introductions, use double opt-in: ask each relevant person for permission before connecting them. Do not disclose one person’s contact details, interest, or context beyond what they have agreed can be shared.

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
- Record a new responsibility boundary in the user’s or organization’s maintained responsibility reference when it applies beyond one meeting.

Do not turn one-off facts into permanent rules. Small additions to an examples or patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing steps or changing the evidence order. Briefly report any reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links only to sources appropriate for the task audience.
- Message drafts are ready to send and follow the user’s preferences.
- Sensitive or unrelated meeting details were omitted.
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
description: Complete browser-based tasks safely, including rendered forms and authenticated dashboards, by choosing the least invasive method, protecting account context, verifying page state, and separating preparation from commitment.
---

# Use a browser safely

Use this workflow for tasks that require real interaction with a website: completing forms, changing settings, collecting data from rendered pages, testing a user flow, or working in an authenticated dashboard. Use it when a simple page retrieval, supported API call, or static-page request cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not perform a consequential final action until the page state, target, and authorization are clear.

A browser automation command succeeding does **not** prove that a website accepted the change. Modern web applications may maintain internal state separately from the DOM, commit data only after focus leaves a field, replace controls during a re-render, or show a cosmetic error after an action has actually succeeded.

## 1. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can perform the requested task. It is usually more reliable than reproducing browser behavior.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, and forms that do not require the user's established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing session, single sign-on state, account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for a direct route. Check official documentation, ordinary form actions, page source, and visible network activity for supported endpoints. A form may submit structured data to an authorized service that is safer to use directly.

Do not use undocumented endpoints to bypass access controls, terms, consent boundaries, or other restrictions. Do not use an authenticated visible session merely because it is convenient: it can interrupt the user's work and creates greater privacy and account risk.

If a site blocks automated browsing, do not attempt to evade its protections for casual research or collection. A user-visible browser session may be appropriate only when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and the established session is necessary. Do not weaken browser security, access controls, warnings, or anti-abuse protections.

## 2. Protect account identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, confirm there is a legitimate purpose and clear authorization. Use the minimum relevant sources and data. Do not copy unrelated personal details into notes, screenshots, logs, or reports. Keep results within the requester's appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated context, identify the correct account, organization, environment, and browser profile. Never infer identity from a generic browser-window name, an old tab title, a remembered default, or a browser connection label.

Use these rules:

- Announce when taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Classify the intended context explicitly: for example, personal, work, testing, staging, or production.
- Select the browser profile or connection that corresponds to that context rather than relying on a generic browser selector.
- Confirm the signed-in account using a reliable account indicator before opening or changing the real target.
- If the required account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not reveal credentials, session tokens, recovery information, private account data, or security settings in output or logs.
- Do not disable security controls, multi-factor authentication, browser warnings, or access restrictions to make automation easier.

Use an account preflight gate before actions that change data. Confirm the account identity, environment, and target object. If the automation system provides a verification marker or permission gate, mark the context verified **only after** the account check has actually passed. Never create or enable such a marker in advance merely to unlock actions.

A useful pre-action question is: **Which account is this? Which environment is this? What exact item will change?** If any answer is uncertain, resolve it before proceeding.

## 3. Establish the task boundary

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, or workflow.
- The information that will be entered, collected, changed, or uploaded.
- The minimum information needed to complete the request.
- Whether the final action is reversible.
- Whether the task includes sending, publishing, paying, deleting, granting access, changing a plan, or another external commitment.
- Missing information, ambiguous choices, and fields that require the user's judgment.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and collecting a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, or applying an irreversible account change may not be.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify all values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** After explicit confirmation of the prepared state, re-check the account, target, and readiness gate. Then perform the final action once.

If a page reloads, re-renders, or the session changes between passes, do not assume the earlier state remains valid. Restore the intended values if needed and verify them again before committing.

## 4. Inspect the rendered page before editing

Do not begin by guessing selectors, filling fields by numeric position, or trusting a visual approximation. First inspect the rendered page and collect enough structure to identify controls safely.

For each relevant field, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or label relationship.
- Current value and whether the field is required.
- Validation rules, character limits, formatting behavior, and disabled state.
- Whether an apparent field is the editable control, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, date, or tab causes the page to re-render.

Address controls by stable semantic identity, such as visible label text, an accessible name, or an explicit label relationship. Do not use DOM indexes where labels are available: dynamic applications can change element order between loads or after re-rendering.

Before changing a record or setting, inspect its current state. This prevents modifying the wrong item or overwriting existing values unintentionally.

### Generic form inspection pattern

Use a page-inspection capability to list relevant controls before writing fill logic. The exact automation library is user-selected, but the inspection should record at least tag, input type, role, label, required state, and current value or text length.

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

## 5. Use the correct input method for each control

Different controls need different interactions. A generic “set value” operation is not reliable for all of them.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use the normal text-input mechanism | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus it, select existing content, enter text through keyboard-style events, then blur | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle | Selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed | A click can toggle an already-correct value. |
| Date/time picker | Choose date and time, then verify the rendered summary | Popovers can reinterpret typing or clear related fields. |
| File upload | Confirm file, destination, and privacy implications first | Uploading may begin immediately and can be difficult to undo. |

For framework-driven editors, simulate normal user interaction rather than writing directly to low-level page properties. A robust general sequence is: focus the actual editable element, select existing text, delete it, enter the new text with keyboard-style events, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible rich-text editor with a hidden input. Editing the hidden input may appear successful in a DOM dump while server-side validation treats the visible editor as empty. Target the control that the user interacts with and that the application actually reads. If a generic accessibility locator points to an empty wrapper, inspect the underlying editable element and follow its label relationship.

If changing a dropdown, checkbox, tab, or date can refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterwards and confirm that earlier entries remain present.

## 6. Verify after every meaningful edit

After each field is filled or setting is changed, read its value back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare lengths, required state, or a minimal redacted summary rather than exposing the full value unnecessarily.

Check for these common mismatches:

- The automation layer reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displayed text but did not retain it internally.
- An action on a later field erased an earlier field after a re-render.
- A hidden synchronization field was changed instead of the visible editor.
- A selection changed a dependent field, date, recipient, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once using a more appropriate interaction method, then verify again. If the page continues to reject or alter the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

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

The following generally need explicit confirmation immediately before the final control is activated:

- Sending messages, invitations, or notifications.
- Publishing content.
- Submitting an official or externally reviewed form.
- Making a payment or purchase.
- Deleting records or files.
- Changing subscription, billing, access, ownership, or security settings.
- Actions labeled permanent, final, irreversible, or impossible to edit later.

Present a concise confirmation request containing the target, important values, recipients or audience, cost if any, irreversible effects, and any open questions. Then wait for confirmation before activating the final control.

For low-risk reversible changes explicitly requested by the user, such as adjusting a preference or updating a draft, proceed after normal verification unless the page presents an unexpected warning or broader impact.

## 9. Confirm completion after acting

A button click is not proof of success. After the final action, look for reliable evidence such as a success message, confirmation reference, newly created record, persisted saved setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Do not represent an attempted action as completed.

## 10. General failure patterns and recovery rules

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after editing a later one | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control that the application actually reads. |
| Automation becomes unstable on a complex page | The chosen automation layer is unsuitable | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and normal browsers show different behavior | The site varies behavior by browser context | Prefer an authorized direct interface; if needed for an explicit task, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior | Close it through a neutral page action and re-verify affected fields. |
| A visible error may be cosmetic | The task may already have completed | Inspect resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
- [ ] Explicit confirmation was obtained immediately before a consequential final action.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: Create, test, improve, evaluate, and package a reusable AI skill from a new idea, an existing draft, or a demonstrated workflow, using realistic reviews and evidence to improve reliability without overfitting.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, revise an existing skill, test whether it improves outcomes, or improve when it activates. A skill is a focused set of instructions, plus optional resources, that helps an AI complete a recurring kind of work consistently.

The core loop is:

1. Define the job and its boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements where useful.
5. Improve the skill from evidence.
6. Repeat until the skill is useful, reliable, and not narrowly fitted to the test cases.
7. Optionally improve the description that determines when the skill should activate.
8. Package and hand off the final skill.

Identify where the user is in this loop and help with the next useful step. Do not force a full benchmark when the user wants a quick collaborative draft. Conversely, recommend testing when the skill will be reused, affects important decisions, changes files or systems, or has objectively checkable outputs.

## Communication principles

Use plain language by default and match the user’s technical level. Briefly explain terms such as *evaluation*, *benchmark*, *structured data*, or *assertion* if they are needed. Avoid assuming that a user knows programming terminology, file formats, or automation concepts.

Keep the user involved in decisions that affect scope, access, risk, or success criteria:

- Confirm the intended recurring job before writing extensive instructions.
- Explain why missing information matters before asking a question.
- Share proposed tests before treating them as the evaluation standard.
- Let human review lead for subjective quality, including writing quality, design, strategy, and tone.
- Do not assume a particular tool, file path, operating system, account, or development environment.

If the skill will access private communications, records, customer data, employee information, or other sensitive material, first establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Exclude unrelated personal details, honor consent and privacy expectations, and keep outputs within the user’s authorized access boundary.

## 1. Determine the starting point

First identify which situation applies.

### New skill

The user has an idea for recurring work. Start with discovery, then create a first draft.

### Existing skill

The user has a draft, an installed package, or a working instruction set that needs revision, simplification, testing, or better triggering. Preserve its established name and identity unless the user asks to rename it. Read the existing instructions before proposing changes.

If the existing copy cannot be edited directly, make an editable working copy in a user-approved location. Keep the original unchanged until the user accepts the revision.

### Workflow demonstrated in the conversation

The user may ask to turn a process already performed into a skill. Extract what can be learned from the conversation first:

- Inputs, files, and approved sources used.
- The sequence of actions and decisions.
- Corrections or preferences supplied by the user.
- Output forms that proved useful.
- Failure points, exceptions, and validation steps.

Summarize the inferred workflow and ask the user to confirm gaps. Do not convert a one-time workaround into a general requirement without confirming that it applies broadly.

### Evaluation or optimization request

The user may have a skill that appears complete and wants evidence that it helps. Begin with test design and comparison rather than rewriting it unnecessarily.

## 2. Capture intent and scope

Gather enough information to define one coherent job. Do not ask every question mechanically; prioritize missing details that materially change the design.

Use questions such as:

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Trigger:** What requests, wording, or contexts should activate it?
3. **Inputs:** What information, files, systems, examples, or approved sources can it use?
4. **Outputs:** What should it produce, modify, or recommend? Is a specific format needed?
5. **Success:** What makes an output correct, useful, complete, or safe?
6. **Boundaries:** What should it not do? When should it ask, stop, or hand work back to the user?
7. **Variation:** What common variants, difficult cases, or exceptions matter?
8. **Dependencies:** Does it need a particular capability, template, reference, script, or permission?
9. **Testing:** Should it be evaluated with representative requests?

Useful follow-up choices include:

- “When information is missing, should the skill make a clearly labeled best effort or ask before continuing?”
- “Should the result be concise, detailed, structured, or user-selectable?”
- “Which sources are authorized, and which sources should it avoid?”
- “Does this action require approval before it changes a file, sends information, or affects an external system?”

### Research before drafting

When relevant materials are available and authorized, inspect documentation, user-provided examples, comparable skills, output standards, and domain requirements before drafting. Research should reduce burden on the user, not override their requirements.

Use it to identify:

- Existing conventions and required formats.
- Constraints of available tools or file types.
- Reusable patterns and reliable validation methods.
- Privacy, safety, legal, compliance, or approval requirements.

If the evidence conflicts or a requirement remains unclear, state the uncertainty rather than inventing a rule.

## 3. Choose the package structure

Keep a skill focused enough that an AI can predict its purpose and a user can predict its behavior. Separate unrelated jobs when they have different audiences, permissions, sources of truth, or completion criteria.

A portable package might look like this:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional documentation
├── assets/                  # Optional templates or resources
└── evals/                   # Optional test and grading material
```

Use progressive disclosure:

1. **Metadata:** A brief name and description that help route requests.
2. **Core instructions:** The workflow needed for ordinary use.
3. **Resources:** References, scripts, or templates loaded only when relevant.

Keep the core instructions readable. If they become long, move detailed, domain-specific content into clearly named resources and tell the AI exactly when to consult each one. Large references should include a short table of contents or navigation guide.

For a skill with meaningful variants, keep one selection workflow in the core instructions and separate variant-specific guidance into resources. The AI should select the relevant variant instead of reading every possible reference.

### Bundle helpers only when they earn their place

If repeated test runs independently reconstruct the same conversion, validation, report-generation, or cleanup procedure, a reusable helper may be justified. Prefer a script or template when it is deterministic, repeatedly needed, easier to verify, and within the intended permission boundary.

Document each helper’s purpose, inputs, outputs, limitations, and when not to use it. Do not include automation that conceals actions, expands access, overwrites work unexpectedly, or depends on undeclared credentials.

## 4. Write the skill

Write instructions in clear, practical language, usually using imperative phrasing. Explain the reason behind consequential steps: an AI is more likely to adapt well when it understands what a check protects against.

A useful skill commonly includes the following sections.

### Purpose and scope

State the job, intended outcome, and limits. Clarify whether the skill gives advice, creates a file, analyzes approved information, guides a workflow, or takes an approved action.

### Inputs and prerequisites

List required information, approved sources, available capabilities, and optional inputs. Explain what to do when a required input is missing.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or provide a draft that clearly marks unverified sections.
```

### Workflow

Describe the normal sequence and meaningful decision points:

1. Inspect the request and available inputs.
2. Clarify only details that materially affect the result.
3. Gather evidence from authorized sources.
4. Complete the work using the appropriate method.
5. Validate the output against requested requirements.
6. Present the result with assumptions, evidence, and unresolved limitations.

Use conditional rules rather than a long catalog of special cases:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite, disclose, or externally publish important information, explain the impact and request confirmation first.
```

### Output format

Specify a template when consistency is important:

```markdown
# [Title]

## Summary
[Brief overview]

## Findings
- [Finding and supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or needed information]
```

For context-sensitive work, specify quality goals and examples rather than enforcing an inflexible shell.

### Quality, privacy, and safety checks

Name the checks needed before completion. Depending on the job, this can include required fields, calculations, citations, source attribution, preservation of originals, access checks, or clearly flagged uncertainty.

The skill must behave in ways a user would reasonably expect from its description. Do not create instructions to deceive, bypass authorization, extract confidential data, compromise security, or conceal external actions. For sensitive tasks, minimize collection and retention, quote or expose only what is needed, and avoid including unrelated personal details in the output.

### Failure behavior

Define recovery in general terms:

- **Missing or conflicting input:** identify the gap and ask a focused question.
- **Unavailable tool or reference:** explain what cannot be verified and offer a safe alternative.
- **Ambiguous request:** make a low-risk assumption only when it does not materially alter the outcome; otherwise ask.
- **Validation failure:** do not present the result as complete; correct it, label it, or request guidance.
- **High-impact action:** request confirmation before an irreversible, external, or permission-sensitive step.

### Examples

Use a small number of generalized examples only when they teach a distinct pattern. Examples should illustrate judgment and format, not replace reasoning with a list of narrowly memorized cases.

## 5. Write the description for reliable activation

The description is a routing instruction. It should say both what the skill does and when it should be used. Cover realistic user language, including requests that imply the job without naming it exactly.

A strong description includes:

- The expected outcome.
- Common request types or contexts that indicate relevance.
- Important scope limits that prevent costly false activation.

Example:

```text
Create concise project status reports from approved updates and source material. Use for requests involving progress summaries, milestone reviews, risks, dependencies, next steps, or leadership updates, even when the user does not say “status report.”
```

Do not put the full procedure in the description. Avoid vague labels such as “help with documents,” but do not make the description so broad that it captures nearby tasks better handled by another skill.

## 6. Review the draft before testing

Read the skill as a first-time user and auditor. Check:

- Is the job clear, coherent, and bounded?
- Does the description explain when to activate it?
- Are inputs, outputs, permissions, and dependencies explicit?
- Does the workflow handle normal variation and missing information?
- Do consequential instructions explain why they exist?
- Are there repeated, brittle, or low-value rules?
- Does it avoid personal defaults, hidden access assumptions, and tool-specific language?
- Would a capable AI have enough flexibility to solve normal cases well?

Prefer a lean instruction set over an accumulation of rigid commands. Repeated absolute language is a warning sign unless it protects a true safety, privacy, authorization, or correctness boundary.

## 7. Design realistic tests

Once the draft is stable enough to test, create two or three representative prompts. Share them with the user before treating them as the test set. Expand the set after early iterations reveal meaningful new failure categories.

Record each evaluation with a descriptive name, prompt, inputs, expected outcome, and objective checks when appropriate.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates and clearly flag information that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover different meaningful conditions:

- A normal successful request.
- Incomplete or ambiguous input.
- A format- or rule-sensitive request.
- A realistic edge case that changes the workflow.
- A request requiring permission, escalation, or refusal when relevant.

Do not build tests that merely repeat the wording of the instructions. Vary detail, phrasing, and user context. If test materials contain private information, use authorized, minimized, and appropriately protected examples.

## 8. Run and preserve comparisons

When independent execution is available, compare the skill with a meaningful baseline:

- For a new skill, compare a run using the skill with a run without it.
- For an existing skill, preserve an unchanged snapshot and compare the revision with the prior version.

Run all comparison conditions under similar conditions. If parallel execution is available, start skill and baseline runs for every test at the same time. This limits timing distortions and keeps the comparison fair.

Use an iteration structure such as:

```text
workspace/
├── iteration-1/
│   ├── standard-request/
│   │   ├── with-skill/
│   │   └── baseline/
│   └── incomplete-input/
│       ├── with-skill/
│       └── baseline/
└── iteration-2/
```

For each run, retain the prompt, input files, outputs, and available execution metadata such as elapsed time or resource use. Record timing as soon as the environment reports it, because some environments do not preserve it later.

If independent runs are unavailable, perform a transparent sanity check: follow the skill on each prompt, save the results, and ask the user to review them. Do not claim this is a rigorous baseline comparison.

## 9. Define and grade objective checks

While test runs are in progress, write objective checks where they genuinely represent user value. Explain them to the user. Good checks are observable, specific, and meaningful, such as required sections, valid file output, correct calculations, source attribution, or proper identification of missing required inputs.

Use this portable grading shape:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when required source information is absent.",
      "passed": true,
      "evidence": "The final section identifies two unavailable data points and requests them."
    }
  ]
}
```

Use programmatic validation when practical. Scripts are more repeatable than visual inspection and can be reused in later iterations. Do not force numerical checks onto subjective work such as writing style, visual quality, or strategic judgment; these require qualitative human review.

## 10. Review, analyze, and improve

Present outputs and measurements in a review format the user can inspect. Use any available review interface; otherwise provide accessible files or a clear in-conversation comparison.

For each evaluation, show the prompt, relevant inputs, outputs for each condition, objective grades with evidence, and available timing or resource data. Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, excessive, or difficult to use?
- Did the skill add work that was not valuable?
- Would this still work with different wording or data?

Aggregate results when possible, but inspect beyond pass rates. Look for non-discriminating checks that pass everywhere, high-variance results, quality-versus-cost tradeoffs, clustered failures with one root cause, redundant work in execution traces, and repeated reconstruction of the same helper procedure.

Revise from underlying causes, not individual examples. If a test reveals missing source notes, clarify how to distinguish verified information from assumptions whenever evidence is incomplete; do not merely mention the exact test scenario.

Apply these principles:

1. Fix causes rather than test-specific symptoms.
2. Remove guidance that does not improve results or causes wasted work.
3. Explain intent behind important checks.
4. Add scripts, templates, or references only when repeat use justifies them.
5. Preserve behavior the user already values.
6. Add tests only for real categories of failure.

Rerun the test set in a new iteration after meaningful changes. Continue until the user is satisfied, feedback is consistently positive across meaningful cases, objective requirements are reliable, or further changes no longer produce useful improvement.

## 11. Optional blind comparison

For a more rigorous choice between two versions, give an independent reviewer two outputs without identifying their origins. Ask it to apply a shared rubric based on correctness, completeness, clarity, adherence to constraints, safety, and practical usefulness. Reveal which version produced which output only after the judgment is recorded.

Use blind comparison when versions have similar measured results, qualitative judgment is important, or a decision has meaningful cost.

## 12. Optimize activation after the workflow is stable

Only optimize the description after the skill itself is useful. Create a realistic, roughly balanced set of requests that should trigger and should not trigger the skill. Favor difficult near-misses over obviously irrelevant negative cases.

```json
[
  {
    "query": "I need a concise leadership update from these team notes, with risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Explain the purpose of project status reports and when teams use them.",
    "should_trigger": false
  }
]
```

Include formal and casual phrasing, direct and implied requests, common and uncommon valid cases, and adjacent tasks that should go elsewhere. Review the set with the user before using it.

If the environment supports repeated routing tests, separate cases used to improve the description from held-out cases used to select it. Choose the description that performs best on held-out cases, not merely the one that fits the development set. Use substantive requests: very simple tasks may be completed directly without consulting a specialized skill even when the description matches.

Show the before-and-after description and the results before applying the change.

## 13. Package and hand off

Package only the instructions and resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not rely on undeclared tools, private habits, local paths, or special access.
- Scripts and references are present, clearly named, and documented.
- No credentials, private records, personal identifiers, confidential examples, or unnecessary sensitive material are included.
- The package respects access boundaries and does not imply authority the user lacks.
- The user can install or adapt it in their chosen environment.
- Retained test material is safe, authorized, and useful.

Provide a handoff note explaining what the skill does, required capabilities, known limitations, and how to run a simple post-installation check.

## Final readiness gate

A skill is ready when it has a clear job, accurate activation guidance, instructions that handle normal variation, explicit behavior for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not mistake a long instruction file for a reliable skill. The goal is a reusable workflow that helps an AI make sound decisions and deliver better results for the user’s recurring work.


---
name: test-every-screen-size
description: Verify every UI or CSS change across representative narrow, wide, short, tall, and content-heavy states using both screenshots and programmatic layout checks, then fix and retest every failure before completion.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to a small spacing, background, or typography edit: a local change can alter wrapping, height, overflow, alignment, or exposed page backgrounds elsewhere.

A bounding-box check alone is not enough. A single desktop screenshot and a single mobile screenshot are not enough. Real screenshots and programmatic checks find different failure types, so require both.

## 1. Prepare a realistic test state

Run the interface in an authorized test environment using only the minimum test data needed. Populate the changed surface with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative cards, rows, lists, and item counts;
- form validation messages and error text where relevant;
- loading, empty, and error states when the change affects them;
- content close to expected maximum length or density.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, unexpected whitespace, and wrapping failures.

## 2. Define the viewport sweep

Test these baseline viewport widths:

- 320 px;
- 480 px;
- 600 px;
- 720 px;
- 1024 px;
- 1440 px.

Add a large desktop width, such as 1920 px, for landing pages, dashboards, or interfaces expected to be used on large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short viewport, around 700 px high;
- a tall viewport, around 1400 px high or greater.

Also test any viewport known to matter for the intended audience or environment. Explicitly include a very tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable browser automation system chosen for the project. Run it headlessly unless visual browser interaction is specifically needed for diagnosis.

## 3. Capture real screenshots

Capture screenshots at every relevant viewport and state. Use full-page screenshots when page length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect the affected area on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does it match the design intent now that this element has changed role or size?

Be especially careful with edge-to-edge or full-bleed changes. Making a component flush on one edge can expose leftover margins or wrapper padding on another edge as visible background strips. Check every edge, not only the edge edited.

Reread the original requested outcome after making the change. Compare that goal directly with the screenshots. Do not accept a result only because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify the following where applicable:

- no unintended horizontal overflow;
- no unintended vertical overflow for screens intended to fit within the viewport;
- no changed element overlaps neighboring content or escapes its intended container;
- buttons, links, fields, and other interactive controls remain visible and usable;
- cards, lists, and form controls stay within intended bounds;
- fixed or sticky UI does not hide essential content;
- readable text does not become excessively wide.

For a page intended to fit the viewport, compare document height with viewport height and allow only a small rendering tolerance. For overlap checks, compare bounding rectangles of relevant neighboring elements, including their top, bottom, left, and right edges.

For prose-heavy pages, flag overly wide text measures. A useful warning threshold is roughly 80 characters per line; reading-focused layouts commonly target about 60–70 characters per line.

## 5. Require both kinds of evidence

A viewport passes only when both of these pass:

1. **Visual review:** screenshots show no unintended blank strips, poor alignment, clipping, imbalance, or exposed wrapper background.
2. **Programmatic checks:** measurements show no unintended overflow, collision, hidden control, or out-of-bounds layout.

Measurements can miss visually obvious defects. Screenshots can miss subtle off-screen overflow, small collisions, and inaccessible controls. Neither replaces the other.

## 6. Fix failures at the cause, then retest

If any viewport or realistic content state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying layout behavior rather than applying a one-viewport cosmetic patch;
4. rerun the complete relevant sweep, not only the viewport that first exposed the problem.

If a fix improves one viewport but breaks another, reconsider the diagnosis. The layout model is incomplete; do not stack compensating patches until the screenshots appear acceptable.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the widths, relevant heights, realistic states, and checks actually completed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, say so clearly. Do not represent the UI change as complete until the required relevant sweep has passed.


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

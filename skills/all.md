# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs honestly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when a user needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not to produce a long idea list. It is to surface genuinely different paths, make their tradeoffs clear, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources that are available in the current environment, review the relevant material first.

When accessing private communications, records, or information about people, do so only for a legitimate purpose and with clear authorization. Use the minimum sources and details needed for the decision. Do not expose unrelated personal, confidential, or sensitive information in the output; keep findings within the appropriate access boundary.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, deadlines, and ownership boundaries
- Stakeholder concerns or operational dependencies
- Evidence about what has already been tried

Do not search broadly by default. If important context is unavailable, state the assumption or ask a focused question rather than inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- Important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging options

The user’s wording may describe a symptom or a proposed solution rather than the real decision. For example, “Should we add a feature?” may actually mean, “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same idea. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes process, incentives, scope, or the framing of the problem
- At least one surprising but credible option, such as delaying, partnering, narrowing scope, or intentionally doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, avoided cost, or reduced distraction has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

- **What:** One or two sentences explaining the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages or failure risks.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, stakeholder burden, and evidence strength. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not merely why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may:

- Choose an option
- Request more detail on a specific option
- Reject or revise the framing
- Ask for additional options
- Combine approaches into a hybrid

If the user proposes a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that states the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than only the user’s first proposed solution.
- Options are genuinely distinct and not variations in scale.
- At least one credible non-default path was considered.
- Weaknesses are candid, concrete, and proportionate.
- Effort labels are plausible.
- Recommendations follow the stated criteria and constraints rather than default assistant preferences.
- Any retrieved private context was authorized, minimized, and represented without unnecessary personal or sensitive detail.


---
name: pressure-test
description: Find the weak points in a leading strategic idea before committing. Steelman the case, test its load-bearing assumptions through sequential challenge, and finish with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Position in the decision process

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportional to its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes an exercise in defending it.

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.

## Evidence, access, and privacy

Use research, metrics, experiments, customer feedback, documented decisions, and stakeholder input where available. Distinguish facts, inferences, and forecasts.

When reviewing private communications, internal records, or information about identifiable people, confirm there is a legitimate decision-related purpose and clear authorization. Use only the minimum relevant sources and details. Do not expose unrelated personal information, sensitive details, or content outside the intended access boundary. Summarize evidence rather than reproducing private material unless reproduction is necessary and authorized.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Refer to relevant dissenters by role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the actual intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, starting with the assumption most likely to undermine the decision.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | How to test or disprove it |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Smallest useful test] |

Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions and adapt later questions to the answers received. Do not present the full list as a questionnaire, because that permits selective answering.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed? Why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what will the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence. Ask what observed behavior, data, comparison, or commitment supports that belief.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution risks, external conditions, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable early signal] | [Check or accountable role] |

The warning sign must be observable early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role’s strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap; do not assume silence means agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence that names the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data collection period. Next: run that test, then make the decision with its result recorded.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, the downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with exactly one concrete next action: a verb, an owner, and a deadline when useful.

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

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and giving a positive verdict without falsifiable criteria or monitoring.


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

For a resume, fetch the existing record and append new information rather than overwriting history. For a review, use the original prediction and reasoning as the baseline rather than reconstructing them from memory.

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

Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar, task system, or other reminder mechanism for high-stakes reviews.

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
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only stopping point when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the solution is not already clear. Do not use it for a small fix or routine task with a known implementation path.

By default, work end-to-end. If the requester says not to implement yet, or asks for analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the actual problem

Start with the outcome needed, not the first solution proposed. If someone asks to build a feature, work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today?
- What workaround, if any, exists?
- How often does it happen, how severe is it, and what does it block?
- What would a successful outcome look like?
- What constraints matter: time, budget, compatibility, security, privacy, operations, or maintainability?

Write a concise problem statement and descriptive requirements. Describe the required result rather than assuming a particular technology or design. If the proposed solution does not match the problem, say so plainly.

Ask only for information that cannot be learned from authorized, relevant context such as project documentation, code, tests, or process records. When reviewing private communications or records, confirm a legitimate purpose and authorization, use the minimum relevant material, and exclude unrelated or sensitive personal information.

## 2. Decide whether to act now

Assess severity, frequency, affected users, alternatives, opportunity cost, and urgency. Treat **do nothing**, **deprioritize**, or **improve the workaround** as real options when the problem is low impact or adequately handled already.

Separate decisions by reversibility:

- **Reversible decisions:** Small choices that are cheap to change. Make a reasonable choice and proceed.
- **Hard-to-reverse decisions:** Persistent data changes, migrations, public interfaces, long-lived settings, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the commitment is material.

If direction or priority is unresolved, present the tradeoff to the responsible decision-maker before spending substantial effort on detailed design or implementation.

## 3. Research the current context

Read relevant repository instructions, architecture notes, service documentation, code, tests, operational runbooks, and records of prior attempts. Identify existing patterns, shared components, and project conventions before proposing new abstractions.

Check practical constraints: supported environments, deployment and rollback practices, access boundaries, dependency policy, monitoring, ownership, performance expectations, and compatibility requirements. Prefer the existing system's conventions unless there is a strong, stated reason to depart from them.

## 4. Define evaluation criteria

Set explicit criteria before generating options. Keep them proportionate to the problem. Typical criteria include:

- Preserves existing behavior, access controls, and data integrity.
- Fits available engineering and maintenance capacity.
- Avoids unnecessary dependencies and permanent configuration.
- Has a clear, realistic test and verification method.
- Can be removed, rolled back, or contained if it fails.
- Meets stated performance, reliability, or delivery constraints.

These criteria prevent the first plausible solution from winning by default.

## 5. Generate varied approaches

Create genuinely different options, not minor variants of one design. Consider:

1. Do nothing, defer, or improve the existing workaround.
2. A non-code solution: guidance, process change, template, training, or an existing platform capability.
3. A small, targeted technical change.
4. A broader integrated solution.
5. Build, buy, or integrate with an existing service.

For ambiguous or high-impact problems, generate a wider candidate set before narrowing. For each option, state what it is, the expected outcome, main costs, risks, and irreversible consequences.

### Design rules for technical options

- Prefer one understandable execution path over runtime-specific special cases.
- Validate inputs and invariants strictly. Fail visibly for invalid states rather than silently producing plausible but incorrect output.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new data fields, settings, and public interfaces as maintenance commitments.
- Favor bounded, loosely coupled changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure when suitable.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is a stated requirement.
- Place changes in the appropriate design boundary; do not use a quick workaround that creates lasting structural debt.

## 6. Evaluate and recommend

Compare viable options against the criteria. Produce a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Options and their tradeoffs.
- One clear recommendation and why it best fits the criteria.
- Key risks, hard-to-reverse consequences, assumptions, and open decisions.

Use a shared documentation location selected by the requester when review, editing, or durable decision records are needed. Otherwise, provide the proposal in the agreed workspace. Use a clear date-prefixed title, such as `19 Sep 2026: Solve — topic`.

**Analysis-only gate:** If implementation is not authorized, stop here. Do not begin changes merely because a recommendation has been made.

## 7. Plan, implement, and verify

For larger work, prepare an implementation plan before making changes. Include scope, ordered steps, affected components, dependencies, migration and rollback approach, test strategy, deployment steps, and follow-up ownership. Put the plan where relevant reviewers can inspect and edit it.

Implement the approved approach using project conventions. Run relevant automated tests, static checks, and focused manual verification. Test expected behavior, important failure modes, access boundaries, compatibility, and rollback assumptions where applicable.

Audit before declaring success:

- Does the delivered change solve the stated problem rather than merely match the original suggestion?
- Does it meet the evaluation criteria?
- Were irreversible changes explicitly approved?
- Are failures visible and diagnosable rather than silently masked?
- Is the change appropriately bounded, testable, and maintainable?
- What was actually verified, and what remains unverified?

Do not claim success based only on code being written. Commit, publish, deploy, or otherwise release changes only through the user's authorized repository and release practices.

## 8. Hand off

Report the outcome in operational terms:

- What changed and what it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required rollout, user action, monitoring, or ownership follow-up.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused and direct. Surface failure modes and unresolved decisions rather than burying them in implementation detail.


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
description: Learn a paper, article, or topic through a short Socratic dialogue that uses retrieval, explanation, and application instead of passive summary.
---

# Learn with a tutor

Help the learner understand, retain, and use a provided paper, article, or topic through a rigorous conversation. Prioritize active recall and reasoning over explanation. The learner should do most of the intellectual work; the tutor guides, diagnoses, and raises the level of challenge.

## Learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to recall and reconstruct ideas in their own words.
- **Ask for mechanisms.** Move beyond conclusions by asking why, how, under what conditions, and with what evidence an idea works.
- **Make the learner generate connections.** Ask for their own examples, analogies, predictions, and uses before offering any.
- **Use productive difficulty.** Challenge the learner enough to require thought, but not so much that they cannot make a meaningful attempt.
- **Practice transfer.** Move from the original material to unfamiliar cases, related ideas, and real decisions.
- **Surface gaps through questions.** When an answer is incomplete or inconsistent, ask questions that help the learner notice the problem. Explain directly only after they have had a fair chance to reason it through.

## Conversation workflow

### 1. Establish prior knowledge and a target

Start by asking what the learner already knows, believes, or has experienced about the topic. Also identify their purpose: for example, understanding an argument, preparing for discussion, applying a method, or evaluating a claim.

Ask one or two open questions, such as:

- “What do you already think is true about this topic, and why?”
- “What are you hoping to be able to explain or do by the end?”

Use their response to identify likely misconceptions, useful background knowledge, and an appropriate level of challenge.

### 2. Elicit the central claim from memory

Ask the learner to explain the main argument, finding, or idea without quoting the source.

Useful prompts:

- “In your own words, what is the main claim?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “If you had 30 seconds to explain it to a thoughtful friend, what would you say?”

If the learner has not yet read or engaged with the material, ask them to state their initial prediction or working model first. Then guide them to inspect the relevant part before resuming retrieval.

### 3. Select a small number of important ideas

Do not try to cover every detail. Choose two or three ideas that are central, difficult, consequential, or likely to be misunderstood. Go deep on each one.

For each idea, use a short cycle:

1. Ask the learner to state or reconstruct the idea.
2. Probe their reasoning, evidence, assumptions, and causal story.
3. Ask them to generate an example, comparison, or application.
4. Test the idea with an objection, boundary case, or alternative explanation.
5. Adjust the next question based on their answer.

Keep turns brief. Usually ask only one or two questions at once.

## Question toolkit

Choose questions that require explanation rather than recognition. Adapt wording to the material and the learner’s level.

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What evidence would distinguish this explanation from another one?”
- “What is the mechanism here, step by step?”
- “Can you construct a concrete example from your experience or a familiar setting?”
- “Where might this fail, or where would it not apply?”
- “What is the strongest objection to this argument?”
- “How does this connect to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one key assumption changed?”

Avoid yes/no questions unless they are immediately followed by a request for reasoning.

## Responding to answers

Be warm, direct, and specific. Do not use generic praise. When an answer is strong, name the useful feature—for example, that it identified an assumption, distinguished correlation from causation, or gave a relevant counterexample—then extend the challenge.

When an answer is wrong or incomplete:

1. Do not immediately provide the correction.
2. Point to the tension with a focused follow-up question.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, give a concise explanation of the missing distinction or reasoning step.
5. Ask them to restate the corrected idea in their own words or apply it to a fresh case.

If the learner says they do not know, invite a low-stakes attempt: “Take a guess based on what you do know. What seems most plausible, and why?” Offer a hint only after an attempt or when the task is beyond their current foundation.

## Calibration and pacing

Increase difficulty when the learner answers easily: ask for a counterexample, a comparison, a prediction, or an application in a new domain. Reduce difficulty when they are lost: narrow the question, isolate one assumption, use a simpler case, or ask them to choose between competing explanations and defend a choice.

Match the learner’s energy. When they are engaged, pursue the reasoning in more depth. When they are tired or overloaded, consolidate the strongest ideas instead of introducing more material.

Maintain a dialogue rather than a quiz. Questions should build on the learner’s actual responses, not appear as a fixed test sequence.

## Progress checks

Periodically state a brief evidence-based assessment:

- What the learner has demonstrated they understand.
- What remains uncertain, incomplete, or confused.
- The most useful next focus.

Do not claim mastery merely because the learner recognized a term or repeated a conclusion. Look for accurate explanation, reasoning, and transfer.

## Closing gate

Before ending, ask the learner to convert learning into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation or a future retrieval prompt. End with a clear statement of the next concept or question worth revisiting.

## Guardrails

- Do not summarize the material unless the learner explicitly requests it; even then, first invite their own summary.
- Do not lecture when a well-chosen question can make the learner retrieve or infer the point.
- Do not define jargon automatically; ask the learner to define it first, then clarify if needed.
- Do not make the interaction easy merely to be encouraging.
- Do not cover the entire source superficially when a few core ideas can be understood deeply.


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
description: Create an evidence-based professional case study post that shows a person’s credible change, the concrete mechanisms that helped, and a clear next step for the intended reader.
---

# Write a case study post

Use this workflow to turn approved source material about a person’s professional, learning, or career change into a concise public case study. It works best for professional social posts, but can be adapted for newsletters, community updates, program alumni stories, recruitment pages, or similar formats.

The purpose is not to praise someone vaguely. Show a credible, specific story: where they started, what they were considering, what they did, what concretely helped, what they do now, and what the reader can do next. A strong post lets a reader recognize their own situation in the subject’s before-state without overstating that a program, community, or organization caused the entire outcome.

## Authorization, privacy, and scope

Use personal records, private communications, applications, transcripts, internal notes, or other non-public sources only for a legitimate publishing purpose and with clear authorization to access and use them. Use the minimum information needed to tell the story.

Before drafting:

- Confirm the organization is allowed to publish a story about the subject.
- Confirm the subject’s preferred public name, pronouns where relevant, and any limits on what may be shared.
- Keep private details out unless they are necessary, approved, and appropriate for the audience.
- Do not include unrelated sensitive information found in source material.
- Keep the draft, source excerpts, and approval notes within the appropriate access boundary.
- Do not imply an employer’s motives, an assessment of the person, or a causal story that the evidence cannot support.

If consent, authorization, or the intended public scope is unclear, pause and ask before drafting.

## Inputs and intake

Ask for all available source material and any publishing constraints. Useful sources include:

- An interview transcript and meeting notes
- An application, intake form, or written statement from the subject
- A current professional profile or public biography
- Official announcements, work samples, publications, projects, or product pages
- A community message celebrating a result
- A prior draft, outline, or notes
- An editorial or brand voice guide
- The target audience, platform, desired length, and call to action

Do not assume the organization, publishing system, folder, platform, or link-placement rule. Use the system and destination chosen by the user.

Before writing, capture the following in a private working outline:

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns if relevant, and publishing consent status |
| Before-state | Previous role, field, goal, uncertainty, or constraint that matters to the reader |
| Alternative path | What they were considering or doing instead, if it makes the change relatable |
| Trigger | Why they joined, applied, changed direction, or acted at that time |
| Intervention | Program, community, resource, event, mentor, or product involved |
| Mechanism | One or two concrete things that helped, such as a realization, opportunity, conversation, feedback session, or introduction |
| Now-state | Current role, organization or team if approved, practical work, output, or result |
| Timeline | Verified dates or time spans between the starting point and outcome |
| Evidence | Sources for names, roles, figures, artifacts, and direct quotes |
| Cost or risk | Any tradeoff, move, uncertainty, or career change that is approved for publication |
| CTA | The reader, desired action, and destination after reading |

If critical facts are missing, ask focused questions before drafting. Never guess at names, organizations, job titles, team names, paper titles, dates, figures, timelines, or outcomes.

Useful questions:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they act at that point?
4. What are the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a specific project, placement, publication, product, grant, or other result that can be named publicly?
8. Did they take on a meaningful cost or risk they are comfortable sharing?
9. Which claims, figures, names, and quotes are approved for public use?
10. Who should this post help or persuade, and what should they do next?

## Evidence and verification rules

Never invent facts or make claims sound stronger for dramatic effect. If a source says someone contributed to a project, do not call them the lead. If they explored an opportunity, do not say they received it. If work is forthcoming, do not call it published.

Automated transcripts and summaries are useful but fallible. They can mishear names, organizations, technical terms, numbers, titles, and dates. Cross-check consequential details against a stronger source.

Use this reliability order unless there is a clear reason to do otherwise:

1. The subject’s direct, recent confirmation
2. Official public records, announcements, or published work
3. A current professional profile
4. An original application or written statement from the subject
5. Interview transcript notes or automated summaries
6. Informal third-party messages

Classify working notes into three groups:

- **Verified fact:** Supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn by the writer. Use it only if the evidence supports it, and phrase it modestly.

Do not claim a course, community, mentor, or resource caused the whole outcome unless there is clear evidence. Prefer precise wording such as “the program helped them see the field differently” or “they found the opportunity through the community.”

## Sensitive-content gate

Flag the following for explicit subject approval before publication:

- Salary, compensation comparisons, pay reductions, debt, or financial hardship
- Health, family, immigration, legal, or other personal circumstances
- Strong criticism of a past employer, role, or career decision
- Confidential projects, unreleased work, or unpublished titles
- Direct quotations, especially sharp opinions or criticism
- Claims about why an employer hired the person
- Claims of causation or impact that cannot be independently verified
- Precise dates or timelines that expose private circumstances

If approval is unavailable, use an honest approved fallback where possible. For example, replace an exact compensation figure with “they accepted a lower-paying role” only if that statement is still accurate, useful, and approved. Do not conceal uncertainty by making the story more dramatic.

## Build the story beats

Create a concise private outline before writing.

### 1. Before-state

Capture the subject’s prior role, background, and the reader-relevant form of their uncertainty. Include the alternative path they were considering when it mirrors the audience’s current life.

Keep only details that move the story. Long lists of credentials, reading, or unrelated earlier roles usually weaken the post. Include a detail only when it makes the decision real or explains the change.

### 2. Trigger

Identify why the subject acted at that moment. They may have wanted to learn about a field, test whether a role was open to them, find collaborators, solve a practical problem, or make a values-driven change.

### 3. Mechanism

Find the one or two observable things that changed the trajectory. Strong mechanisms include:

- Realizing that a field or role was accessible
- Finding a relevant opportunity through a community
- A conversation that clarified next steps
- Feedback that improved an application or project
- A specific introduction, workshop, or resource

Avoid “the experience was transformative.” Name what happened instead.

### 4. Now-state

Record the current role, organization or team if approved, and what the person actually does. Translate technical language enough for the intended reader to understand the work.

Use named outputs only when they add proof or interest. One meaningful artifact can be stronger than a long list of credentials.

### 5. Timeline

Map the sequence from the intervention to the result. Calculate a short, truthful timeframe only when it sharpens the story, such as “within six months” or “the following year.” Do not force a compressed timeline.

### 6. Quotes

Pull three to five candidate quotes verbatim from approved source material. Favor quotes that reflect the reader’s identity, uncertainty, or decision, rather than only the subject’s achievement.

Choose candidates in these categories:

1. **Discovery:** “I did not know this path was open to someone like me.”
2. **Mechanism:** “I found the opportunity through the community.”
3. **Conviction:** “I would make the same choice again.”

Light trimming is acceptable only when it preserves exact meaning and grammar. Do not rewrite a quote into something the subject did not say.

## Generate three hooks

For feed-based platforms, the first two lines determine whether a reader continues. Write three distinct hooks before writing the full post. Each should usually be two short sentences and, where useful for the platform, remain under roughly 140 characters total.

### Hook A: Discovery

Use when the audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific result through a surprising, concrete mechanism.

This is the default recommendation when the first sentence can mirror the reader’s own uncertainty.

### Hook B: Identity collision

Use when the before-and-after contrast is vivid and understandable.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This often works for a broad audience that may not share the subject’s exact blocker.

### Hook C: Stakes-led

Use only when a meaningful cost or risk is approved and the audience will read it as honest conviction rather than a warning.

**Formula:** The subject accepted a specific cost to do something. Now, they are taking a concrete action or doing meaningful work.

Do not use this approach if it implies that participation requires hardship, or if it makes the opportunity seem inaccessible.

Recommend one hook and state briefly why it fits the target audience. State why the other two are less suitable. Default to Discovery when the reader’s likely question is, “Could this be a path for someone like me?”

## Draft the post

Aim for roughly 160 to 220 words unless the platform or audience calls for another length. Shorter is usually stronger.

Use this sequence:

1. **Hook:** Use the recommended hook.
2. **Before-state:** One short paragraph showing the prior situation and a relevant alternative path.
3. **Name the intervention:** State clearly that the subject joined the program, used the resource, or participated in the community. Do not leave this implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then land the immediate result in plain language.
5. **Current work:** Describe what they do now and why it matters in understandable terms.
6. **Optional cost:** Include only if approved and genuinely useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already carried by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

Use a short outcome sentence when it has force: “They applied and got in.” A three-beat version can work when each beat adds evidence, but do not use rhythm as a substitute for substance.

If the chosen platform may reduce distribution for posts with external links, place the link in a comment, profile destination, or other chosen location rather than the body. Treat this as a platform-specific publishing decision, not a universal rule.

## Style rules

Adapt to the chosen voice guide. If none exists, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use verified, approved names, roles, dates, and figures.
- Use the subject’s first name after their first full introduction only if it fits the publication’s tone and the subject is comfortable with it.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not call someone exceptional, inspiring, or brilliant without showing why.
- Use contractions if the voice is conversational.
- Keep the CTA in full second person.
- Avoid emojis unless they are an explicit brand choice.
- Do not use em dashes. Use periods, commas, or line breaks instead.

On the final pass, remove machine-like phrasing: empty transition sentences, dramatic setup frames, filler intensifiers, hedges, abstract nouns replacing evidence, false balance, and reflective summary lines after the CTA.

Avoid terms such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm” unless they are necessary inside a direct quote. Read the post aloud. If it sounds like a generic thought-leadership template, shorten it and replace abstractions with facts.

## Graphic quote options

Provide three options for a visual quote card. Each should be self-contained, under 15 words where possible, and verbatim from approved material.

Offer one quote in each category:

- Discovery
- Mechanism
- Conviction

Recommend one quote with a one-sentence rationale. Discovery quotes often work best because they make sense without context and mirror the reader’s uncertainty. Choose a mechanism or conviction quote only when it is clearer, more memorable, and understandable by itself.

## Readiness audit

Before sending the draft for review, check:

- Is every name, role, date, figure, title, and stated outcome verified?
- Have important transcript-derived details been cross-checked?
- Does the post show a concrete mechanism, not only a result?
- Does it avoid overstating causation?
- Is the intervention named clearly?
- Does the opening reflect a real audience concern?
- Is the current work understandable to a non-specialist reader?
- Have sensitive claims and direct quotes been flagged for approval?
- Does the post honor the agreed public scope and omit unrelated personal details?
- Is the CTA clear and directed at the intended reader?
- Are there no em dashes, unsupported superlatives, corporate phrases, or generic filler?

## Delivery and iteration

Create the draft in the user’s chosen document system if one is available. Use a clear title format such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and two alternatives
- Three graphic quote options and the recommendation
- Approval items
- Missing information that would strengthen the post
- The document location or link, if applicable

Do not treat the first draft as final. If feedback says “make the hook better,” regenerate three hooks rather than making minor edits. If asked to make it shorter, cut secondary biography first while preserving the mechanism and outcome. If the subject rejects a sensitive line, replace it with the approved fallback without weakening the whole story.

After the final version is accepted, review feedback for reusable lessons. Update this workflow only when a recurring pattern is clear, such as a missing intake question, a stable voice preference, or a repeated verification issue. Do not invent process changes after a clean review cycle.


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
description: Close one month honestly, then create a small, capacity-checked, explicitly approved plan for the next month using evidence, trade-offs, and concrete commitments.
---

# Review and plan a month

Use this workflow at a month boundary to review the month ending and create an executable plan for the month ahead. A complete session usually takes 45–75 minutes: roughly half for evidence and review, and roughly half for planning.

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
- In the final week of a month, review the current month to date and plan the next month. Clearly label this as a partial-month review and state the days remaining.
- At other times, use the named month or ask the user which month they intend to review.
- If the user asks only for forward planning, review first because evidence should shape the plan. The user may explicitly choose to skip the review.

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
11. **Do not lecture.** Where training, health, or recovery is in scope, provide the numbers, direct conclusion, and agreed commitment. Give specialist advice only when asked and appropriate.
12. **Respect access boundaries.** When reviewing private communications, calendars, journals, health records, or records about other people, require a legitimate purpose and clear authorization. Use only the minimum relevant sources and details. Do not expose unrelated, sensitive, or third-party personal information in summaries or saved records.

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

If a helper is used for a large calendar, journal, or task source, give it a narrow brief: use only authorized read access, analyze only the requested date range, omit unnecessary personal details, and return a concise planning summary rather than raw material. The summary should include:

- Fixed multi-day blocks, such as travel, leave, or conferences.
- Approximate meeting load by week.
- Important recurring series.
- Protected personal or social commitments when relevant to capacity.
- Planning anomalies, such as meetings during unavailable periods or likely time-zone mistakes.

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
- Access to private records was authorized and the saved output stays within the appropriate privacy boundary.

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
- Reading or repeating private details that are not needed for the monthly decision.


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
description: Gather authorized, relevant context, clarify the desired outcome, and create a focused, privacy-respecting meeting brief, agenda, and follow-up plan in the user’s chosen system.
---

# Prepare for a meeting

Use this workflow to prepare for one meeting or a selected set of upcoming meetings. It turns calendar details, relationship history, relevant materials, and the user’s direction into a practical meeting page: a concise brief, a realistic agenda, and a five-question in-call cheat sheet.

The final deliverable belongs in the user’s chosen notes system, workspace, or calendar-linked record. If no destination is available, produce a structured Markdown page that the user can save or copy.

## Operating principles

- **Research before drafting; clarify before deciding.** Do not turn partial context into an agenda when the user’s goal, stance, authority, or constraints could materially change it.
- **Use information legitimately and minimally.** Access private messages, records, transcripts, or information about people only for an authorized meeting-preparation purpose. Use the minimum sources and details needed.
- **Respect the access boundary.** A shared meeting page is not the place for unrelated sensitive information, private personal details, credentials, compensation figures, legal advice, health information, or confidential hiring material. Put necessary sensitive context only in an appropriately restricted location, or omit it.
- **Separate evidence from interpretation.** Distinguish verified facts, another person’s reported view, open questions, and the user’s own position. Do not imply a promise or decision that the user has not made.
- **Read the material the meeting is about.** If the call concerns a proposal, deck, memo, draft, plan, application, or other written artifact, read it fully before designing the agenda.
- **Optimize for the meeting’s job.** The agenda should help the user learn, decide, persuade, coordinate, or preserve a relationship. It should not merely fill time.

## 1. Select the meeting and establish scope

Identify the meeting or meetings to prepare. The user may select them directly, provide a date range, or authorize review of their calendar. If the selection criteria are not clear, ask.

Useful selection criteria include meeting importance, whether an external party is involved, whether a decision or commitment is expected, and whether there is meaningful prior context to reload. Skip events that are clearly not discussions, such as personal blocks, focus time, or administrative placeholders, unless the user asks to include them.

For each selected meeting, record:

- Title, date, time, duration, and timezone.
- Participants, roles, and organizations when known.
- Location or call details if useful.
- The invitation description and any scheduling context.
- Linked materials, prior notes, and stated objectives.
- Signs of a reschedule, third-party introduction, deadline, or recent trigger.

### Initial meeting record

| Field | Record |
|---|---|
| Meeting | [Title, date, time, duration, timezone] |
| Participants | [Names, roles, organizations] |
| Stated purpose | [Invitation purpose or unknown] |
| Linked materials | [Relevant files, notes, or none found] |
| Scope decision | [Prepare / skip / ask user] |

Do not silently exclude an ambiguous event. Ask the user whether it deserves preparation.

## 2. Research the relationship and subject matter

Research only the sources the user has authorized. Work efficiently, but preserve enough source context to avoid treating rumor, stale notes, or a third party’s interpretation as fact.

### 2.1 Review private relationship history

For each relevant external participant, inspect the most useful available records:

1. **Direct correspondence.** Review recent messages sent to or received from the person. Look for commitments, requests, introductions, unresolved questions, and the immediate reason for the meeting.
2. **Name mentions.** Search authorized messages and notes for the person’s name, even where they were not a direct participant. This may reveal an introduction, prior discussion, decision context, or a relevant project thread.
3. **Team discussion.** Search relevant chat or discussion spaces for the person and, where useful, their organization. Capture decisions and current context, not unrelated commentary.
4. **Prior notes and knowledge records.** Find earlier meeting notes, project records, decision logs, and promises.
5. **Calendar history.** Check previous meetings with the participant to establish whether this is a first meeting, recurring relationship, or follow-up.

Prioritize recency and relevance. A recent promise, decision, or unresolved issue generally matters more than a large collection of old background.

### 2.2 Review public context selectively

Use public sources when they improve the meeting. Useful research may include:

- Current role, organization, and relevant professional background.
- What the organization does and how it relates to the user’s work.
- Recent publications, announcements, projects, or events relevant to the conversation.
- A small number of useful public links, such as an organization site, professional profile, personal site, or publication.

Do not over-research biography for its own sake. Include public details only if they improve rapport, clarify the meeting’s substance, or affect a decision.

### 2.3 Read linked artifacts completely

Reading the artifact is mandatory when the artifact is why the meeting exists. Signals include:

- A request for comments on a proposal, strategy, pitch, draft, or deck.
- References to feedback or comments on a document.
- A meeting about a plan, memo, application, decision document, or written recommendation.
- A relevant link or attachment in the invitation or recent correspondence.
- Phrases such as “the draft we discussed” or “the proposal I shared.”

Read the complete artifact, including meaningful sections, tabs, appendices, and supporting material necessary to understand its argument. Do not skim a substantial document and then prepare generic questions.

Extract:

- The central claim, ask, or decision sought.
- Assumptions, evidence, and dependencies.
- Constraints, timelines, alternatives, and trade-offs.
- Main risks and open unknowns.
- Specific claims or choices that warrant pressure-testing.

If the context strongly suggests an artifact exists but it cannot be found, ask the user for it before writing an agenda around assumptions.

### 2.4 Synthesize findings

Before designing the meeting, create a compact research record.

| Area | What to capture |
|---|---|
| Who they are | Role, organization, and background relevant to the meeting |
| Relationship history | Prior meetings, introductions, commitments, and unresolved threads |
| Meeting trigger | Why this meeting is happening now |
| Organization context | Relevant work, priorities, and connection to the user’s work |
| Current dynamics | Interests, authority, alternatives, deadlines, leverage, and uncertainty where relevant |
| Key links and materials | Public sources, artifacts, prior notes, and records worth revisiting |
| Timely context | Recent developments worth mentioning or accounting for |

Use qualified language when appropriate: “reported,” “appears,” “according to the invitation,” or “needs confirmation.”

## 3. Detect whether a specialized workflow is needed

Before creating a general meeting brief, determine whether the meeting has a purpose requiring a specialized workflow.

A **reference or assessment call** may involve an attendee discussing another person’s prior work, role-relevant capabilities, collaboration, or suitability for a role. Signals can include references to an application process, work sample, interview process, prior manager, collaborator, or referee.

When this applies, use a dedicated reference or assessment workflow rather than a general meeting agenda. Carry forward relevant research already completed. The specialized workflow should:

- Confirm the legitimate purpose and authorized scope.
- Focus on role-relevant capabilities and concrete observed examples.
- Use consistent questions that distinguish relevant performance.
- Separate direct evidence, opinion, and hearsay.
- Avoid unrelated sensitive personal information.
- Keep notes within the appropriate assessment or hiring access boundary.

Similarly, use a suitable specialist process for regulated, legal, medical, safety, or incident-response discussions when one is available.

## 4. Share a situation brief and ask targeted questions

Do not draft the final goal or agenda until the user has received a concise situation brief and answered targeted questions, except for a genuinely routine meeting with a stable, fully documented purpose. When uncertain, ask.

### 4.1 Write the situation brief

Choose the format that fits the meeting.

**Narrative brief** is the default. In short headed sections, cover who the participant is, where the relationship stands, why the meeting is happening, and the live tensions or unknowns. It should be readable in about a minute.

**Decision-shaped brief** suits negotiations, recruiting conversations, sales, fundraising, partnerships, or other meetings with a live choice. Structure it around:

- The ask or decision.
- Their apparent alternatives and deadlines.
- The user’s position, constraints, or leverage.
- Primary risks.
- Unknowns the meeting must resolve.

These formats can be combined: use a short narrative to orient the user, followed by a compact decision section. Choose the format yourself unless the format choice itself is consequential and genuinely unclear.

### 4.2 Ask questions that change the agenda

Ask about targets, shape, and failure modes. Do not ask the user to write the agenda for you.

Always ask about the **primary outcome** and at least one of: tone, a specific ask, sensitive substance, authority, or a failure mode. Always include a final catch-all question.

Useful question axes:

- **Primary outcome:** What should be true after the meeting: a decision, diagnosis, relationship progress, commitment, handoff, or follow-up?
- **Their situation:** What uncertainty about their interest, role, authority, or priorities needs confirmation?
- **Sensitive substance:** Should the user share a candid view, ask for the other person’s view first, or avoid the subject unless raised?
- **Failure mode:** What would make the meeting go badly: overselling, under-asking, moving too slowly, discussing the wrong topic, or leaving without a next step?
- **Specific ask:** Is there a concrete request to make, and how direct should it be?
- **Anything else:** What context, constraint, history, or desired outcome has not been covered?

Use compact labels so the answers are easy to give and audit. Offer three or four meaningful, mutually exclusive options per question. Make the first option the current recommendation, but include real alternatives.

```markdown
1. What is the primary outcome?
   - **1a (recommended):** Test their interest and agree a concrete next step
   - **1b:** Build the relationship without making an ask
   - **1c:** Seek a decision during the meeting

2. What should the user avoid?
   - **2a (recommended):** Making commitments before understanding their constraints
   - **2b:** Letting the conversation remain too exploratory
   - **2c:** Raising the sensitive topic unless they raise it first

3. Is there anything else to account for?
   - **3a:** Nothing to add
   - **3b:** I will add notes or constraints
   - **3c:** There is sensitive context to handle separately
```

If more than four questions are useful, ask in multiple rounds. Put questions that affect later options first. For example, whether the user can make a decision in the meeting changes the appropriate close. Do not create a false either/or when two actions can sensibly be combined.

Before sending questions, verify that:

- Every question is numbered.
- Every option has one unique matching label.
- Labels remain sequential across rounds.
- The final catch-all question is included.
- The answers will materially change the agenda.

## 5. Pass the agenda readiness gate

Do not create the final meeting page until all applicable conditions are true:

- Meeting duration and scheduling details are known or reasonably estimated.
- Relevant relationship history has been reviewed.
- Relevant artifacts have been read, or their absence has been surfaced to the user.
- The user has received the situation brief.
- The user has answered the targeted questions, unless the meeting clearly qualifies for the routine exception.
- The user’s goal, desired tone, authority, and meaningful constraints are understood.
- Sensitive details have been omitted or placed in a properly restricted location.

If an important condition is missing, stop and resolve it. A polished agenda based on an untested assumption is not ready.

## 6. Create the meeting page

Create the page in the user’s chosen system. Include clear, searchable metadata: the meeting date, title, participants, and permitted links. Use a date-only field by default; add time-based metadata only when the user’s system or workflow needs it.

Use a title that reliably identifies the meeting, such as `[Date] [Participant or Topic]`.

Use this structure:

```markdown
# [Date] [Participant or meeting topic]

## Context

Who the participant is, relationship history, why the meeting is happening, and the small amount of timely context that matters. State if this is the first meeting. For recurring contacts, summarize the relationship arc rather than only the latest interaction.

## Goal

[One or two sentences describing the outcome shaped by the user’s answers.]

## Agenda

### 0–[time] min: Open and frame

**Say**

[Opening that establishes purpose and tone.]

**Interviewer note**

[What to clarify or avoid early.]

### [time]–[time] min: Diagnose [topic]

**Questions**

1. [Decision-relevant question]
2. [Decision-relevant question]

**Interviewer note**

[Signals to listen for and assumptions to test.]

### [time]–[time] min: Discuss, pressure-test, or propose [topic]

**Say**

[Transition, summary, or proposal grounded in evidence and the user’s direction.]

**Questions**

1. [Specific question about trade-offs, objections, or evidence]

**Interviewer note**

[What requires a decision; how not to overcommit.]

### [time]–end: Close and next step

**Questions**

1. [Concrete question identifying an owner, artifact, date, commitment, or follow-up.]

**Interviewer note**

[Fallback close if a decision cannot be made now.]

## Five most important questions to ask

1. [Most decision-relevant question]
2. [Second most decision-relevant question]
3. [Key uncertainty or diagnostic question]
4. [Question that tests the main risk, trade-off, or gap]
5. [Specific close: date, owner, artifact, commitment, or next step]

## Timely note

[Optional: relevant announcement, publication, or event to mention.]
```

Use real headings. Keep agenda stages as headings rather than list items. Use **Say**, **Questions**, and **Interviewer note** consistently. Do not put spoken prompts in quotation marks.

Fit time blocks to the actual duration. Put the most important discussion early enough to survive a late start or extended introductions.

## 7. Design the five-question cheat sheet

The five-question list is an in-call navigation aid, not a second agenda. It must be readable in seconds.

Rank questions by decision relevance. Include the central diagnosis, the key risk or gap, and a forcing close when the meeting is intended to move toward a decision or commitment. For an information-gathering meeting, all five may be diagnostic. Use exactly five questions; do not add scripts, explanations, or sub-bullets.

## 8. Arrange post-meeting follow-up when appropriate

For meetings involving persuasion, recruiting, fundraising, sales, negotiation, or a high-stakes decision, arrange a post-call review when the user authorizes it and has an appropriate system for it. A common default is shortly after the meeting, while notes and transcripts are still available.

The review should:

1. Retrieve authorized notes or a transcript, using an approved fallback if needed.
2. Re-read the preparation page and any relevant playbook or recent review.
3. Record what happened, what evidence emerged, what moved the other party, and what did not.
4. Identify recurring communication or decision patterns only when supported by dated evidence.
5. Capture commitments, owners, dates, and the next artifact.
6. Store the review in the appropriate access-controlled location.

Skip automated review for a purely informational meeting unless the user requests it.

## 9. Final audit

Before delivery, verify:

- The correct meeting date, title, and participants are recorded.
- The page is stored in the intended system and visible only to the intended audience.
- The brief reflects evidence rather than unsupported assumptions.
- The user’s answers changed the goal or agenda where appropriate.
- The agenda duration is realistic.
- Relevant artifacts were read.
- The five-question list contains exactly five ranked, decision-relevant questions.
- The close produces a concrete next step when one is appropriate.
- No unnecessary personal data, compensation figures, credentials, private links, or unrelated sensitive details appear in a broadly shared page.
- Any post-meeting review is useful, authorized, and access-controlled.

Common failures are drafting before clarifying the user’s aim, researching people while ignoring the document under discussion, treating unclear context as fact, using generic questions for a specific proposal, failing to define a next step, and exposing confidential material in a shared note. Revise the page if any of these failures are present.


---
name: capture-meeting-actions
description: Review authorized meeting records, identify genuine unfinished commitments, create clear deduplicated follow-up tasks for confident actions, and batch only the questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this as a daily sweep, for a selected date or date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked. Access meeting recordings, transcripts, notes, and related records only for a legitimate work purpose and with clear authorization. Use the minimum relevant information, omit unrelated sensitive details, and keep task outputs within the appropriate access boundary.

## Purpose and operating rules

Before each run, apply these outcomes:

- **0 tasks** when work was completed during the meeting, belongs to another owner, is already tracked, or the meeting was solely for information gathering.
- **1 task** when related actions can be completed together for the same counterparty and time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels something as an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, statement of interest, or open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply documented responsibility and delegation boundaries supplied by the user or organization. Meeting attendance does not make the user accountable for all work in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect:

- Title, date, and time
- Meeting-record link or identifier
- Attendees, if available
- Transcript, notes, summary, and relevant linked context

Report a compact count before processing. Do not infer actions from a meeting title alone.

## 2. Fetch and inspect complete records

Fetch full meeting records in parallel where the selected meeting system supports batching. Do not search for existing tasks yet: first identify people, topics, and candidate outcomes so duplicate checks are accurate.

For long transcripts, use a repeatable search, extraction, or chunking method rather than relying on truncated previews. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by explicit acceptance

Review summary action items as candidates, then verify them against the transcript and surrounding conversation. A promise may have been conditional, reassigned, fulfilled live, or directed to another attendee.

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
- Source and related links that the intended task audience may access

Create no task when work was completed live, another person owns it, the meeting was purely informational and needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

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
- **Priority:** use the user’s scale; default to important, time-sensitive work and reserve the highest level for a real deadline, material risk, or waiting counterparty.
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

Use time-independent wording and absolute dates where useful. Avoid unnecessary private discussion in a task system that may be broadly visible. Follow the user’s known writing preferences. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable. If the task is to send a message, write a ready-to-send draft rather than merely saying “email them.” For introductions, use double opt-in: seek permission from each relevant party before connecting them.

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

- Add a short example or note to a reusable meeting-pattern reference when a recurring pattern affects triage, such as a common attribution error, reliable sign of in-meeting completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new responsibility boundary in the user’s or organization’s maintained reference when it applies beyond one meeting.

Do not turn one-off facts into permanent rules. Small additions to an examples or patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing steps or changing the evidence order. Briefly report reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links to its source record where appropriate.
- Message drafts are ready to send and follow the user’s preferences.
- Outputs do not expose unrelated or sensitive personal information.
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
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and privacy, verifying rendered state after each meaningful edit, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing rendered forms, changing dashboard settings, collecting information from dynamic pages, testing a user flow, or working in an authenticated account. Use it when a supported direct interface, ordinary page retrieval, or static request cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not perform a consequential final action until the account, target, page state, and authorization are clear.

A successful browser-automation call does **not** prove that a website accepted a change. Modern applications may keep state outside the visible document, commit a value only after focus leaves a field, replace controls during a re-render, or show an error after an action actually succeeded.

## 1. Establish purpose, authority, and boundaries

Before accessing private records, authenticated dashboards, communications, or information about people, confirm:

- The task has a legitimate purpose.
- The requester has authorized the access and requested outcome.
- The selected account, organization, environment, and target are appropriate.
- Only the minimum relevant sources and information will be used.
- The output will remain within the requester's appropriate access boundary.

Respect consent and reasonable privacy expectations. Do not copy unrelated personal information into logs, screenshots, code, notes, or reports. Do not expose credentials, session tokens, recovery details, private messages, or sensitive record contents unless strictly necessary, authorized, and safely handled.

Define the work before navigating deeply:

- What page, form, record, setting, or workflow is the target?
- What information must be entered, collected, changed, or uploaded?
- Which choices require user judgment rather than mechanical execution?
- Is the final action reversible?
- Does the task send, publish, pay, delete, grant access, change a plan, or create another external commitment?
- What information or approval is missing?

Separate **preparation** from **commitment**. Filling a form, creating a draft, selecting options, and collecting a preview are usually preparation. Submitting, sending, publishing, purchasing, deleting, or changing access may be commitments.

## 2. Choose the least invasive route

Use the first suitable route. Do not choose a more intrusive method merely because it is convenient.

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it safely performs the requested task.
2. **Headless browser automation.** Use it for public pages, test environments, routine dynamic-page extraction, UI testing, screenshots, and forms that do not require an established signed-in identity.
3. **User-visible authenticated browser session.** Use it only when the task genuinely needs an existing session, single sign-on state, account-specific data, or a user-directed browser context.

Before driving a form in a browser, check for a supported backend route. Review official documentation, ordinary form actions, page source, and visible network activity for authorized endpoints. A structured submission route is often more reliable than reproducing a complex user interface.

Do not use an interface to bypass access controls, consent boundaries, site restrictions, payment controls, or security mechanisms. Do not use an authenticated visible browser for routine scraping or bulk work that a direct interface or headless browser can safely perform.

If a site blocks automation, do not try to evade its protections for research or collection. An authorized visible session may be appropriate when the user explicitly asked to complete a legitimate task on that site and the established session is necessary. Never weaken browser security, warnings, multi-factor authentication, or access restrictions to make automation easier.

## 3. Protect browser and account context

Authenticated browsing can affect the wrong account or interrupt the user's work. Before changing data in an authenticated session:

1. Announce that you are taking control of a visible browser and state the purpose.
2. Classify the intended context explicitly, such as personal, work, test, staging, or production.
3. Select the profile or browser connection for that context directly. Do not rely on a generic selector, browser-window title, remembered default, or arbitrary connection name.
4. Work in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing one.
5. Verify the signed-in account using a reliable account indicator before opening the real target or editing data.
6. Confirm the exact record, page, recipient, or setting before making changes.

Ask this pre-action question:

> Which account is this? Which environment is this? What exact item will change?

If any answer is uncertain, stop and resolve it before acting. If the automation environment has a gate that unlocks write actions after account verification, mark the context verified **only after** the real check passes. Never create a verification marker in advance to unlock controls.

### Account-context audit

- [ ] The task was classified into the correct account or environment.
- [ ] The selected profile or connection matches that context.
- [ ] The signed-in account was confirmed from a reliable indicator.
- [ ] A fresh work area was used unless an existing tab was explicitly designated.
- [ ] The intended record, form, or setting was identified before editing.
- [ ] No credentials, tokens, or unnecessary private details were exposed.

## 4. Inspect before editing

Do not begin by guessing selectors, filling controls by numeric position, or trusting a visual approximation. Inspect the rendered page first.

For each relevant control, determine:

- Its type: single-line input, multiline area, rich-text editor, dropdown, checkbox, radio group, date/time picker, upload, or custom widget.
- Its accessible name, visible label, placeholder, or explicit relationship to a label.
- Its current value, required state, validation state, disabled state, and relevant limits.
- Whether it is the true editable control, a wrapper, or a hidden synchronization field.
- Whether changing it can refresh the form or alter dependent values.

Address controls by stable semantic identity: visible label, accessible name, or explicit label relationship. Do not use DOM indexes where labels are available. Dynamic applications can reorder or replace elements during loading and re-rendering.

Before changing an existing record or setting, inspect its current state. This prevents modifying the wrong item or overwriting a value unintentionally.

### Generic inspection template

Use the selected automation capability to save a pre-edit inventory. Record safe representations of content—such as length rather than full sensitive text—when practical.

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

## 5. Change controls in a safe order

Some actions trigger full re-renders that erase uncommitted text. In general, make and verify structure-affecting choices before entering lengthy content:

1. Select category, type, checkbox, radio option, tab, or dropdown values.
2. Set dates and times, then verify the displayed summary.
3. Confirm file identity, destination, and privacy implications before attaching a file.
4. Fill text fields and rich-text editors.
5. Commit and verify each field before moving to the next.

Read the current state of a checkbox or toggle before clicking it. A click on an already-correct control can reverse it.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use normal text input and read it back. | Line breaks may disappear silently. |
| Multiline text area | Fill text, move focus away, then read it back. | Some sites commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select existing content, enter text through keyboard-style events, blur, then read back. | Direct document mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, and wait for the interface to settle. | Selection can trigger a re-render. |
| Checkbox or radio group | Read current state first; change only if needed. | A click can toggle an already-correct selection. |
| Date/time picker | Set the value, close through a neutral page action, and verify the displayed summary. | Popovers may clear, reinterpret, or alter related fields. |
| File upload | Confirm file and destination, upload, then verify attachment state. | Uploading may begin immediately. |

For framework-driven rich-text controls, avoid directly setting low-level page properties. A robust sequence is: focus the true editable element, select existing content, delete it, enter text through keyboard-style input, move focus to a neutral page element, wait briefly, and read the result back.

Some forms place a visible editor next to a hidden input. Editing the hidden input can appear successful in an inspection result while validation treats the real field as empty. Target the visible interactive control that the application actually reads. If an accessibility locator identifies an empty wrapper, inspect the underlying labeled editable control.

If a short input removes line breaks or repeated whitespace, locate a multiline or rich-text control. If none exists, use a simplified format only when that loss is acceptable for the task; otherwise ask for guidance.

## 6. Verify every meaningful edit

After each filled field or changed setting, read it back from the rendered page and compare it with the intended result. For sensitive values, compare length, status, or a minimal redacted summary rather than reproducing full content in output.

Check for common mismatches:

- The automation layer reports success but the field is empty.
- Text lost line breaks, spacing, punctuation, special characters, or trailing content.
- A custom editor displayed text but did not retain it internally.
- A later action erased an earlier value after a re-render.
- A hidden synchronization field changed instead of the visible editor.
- A selection altered a dependent date, recipient, validation rule, or field value.

If read-back fails, do not continue toward submission. Diagnose the true control type and retry once with a more appropriate method. Re-inspect after a re-render rather than using stale references. If the page continues to alter or reject the value, report the limitation and ask how to proceed. Do not silently submit incorrect content.

Keep a proportionate verification record when useful: a structured before-and-after control dump, a screenshot of the prepared state, or a concise privacy-respecting summary. Store these artifacts only in authorized locations. Do not paste a large table of sensitive field values into chat when a short summary and protected artifact are sufficient.

## 7. Apply the readiness gate

Before activating a final submit, save, send, publish, payment, delete, or other high-impact control, inspect the relevant page state again.

Confirm all of the following:

- The correct account, organization, environment, and target are active.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Recipients, audience, dates, options, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, the account is uncertain, or the target is unclear, **refuse to submit**. A partially prepared form is recoverable; an incorrect external action may not be.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Each meaningful edit was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Recipients, dates, attachments, options, and dependencies were checked.
- [ ] A pre-action record exists when the task is consequential.
- [ ] The final action and likely impact are understood.

## 8. Separate preparation from commitment

Use two phases for consequential work.

**Phase 1 — Preparation:** fill or configure the page, run the readiness gate, and capture a pre-action screenshot or structured state record. Do **not** activate the final control.

**Phase 2 — Commitment:** re-check the account, target, and readiness gate. Activate the final control once, only with appropriate authorization.

Obtain explicit confirmation immediately before actions such as sending messages, publishing content, submitting official or externally reviewed forms, making payments, deleting records, changing subscriptions or access, or taking an action described as permanent or irreversible.

A confirmation request should identify the target, major values, recipients or audience, cost if any, irreversible effects, and unresolved questions. For low-risk reversible changes explicitly requested by the user, proceed after normal verification unless the page presents an unexpected warning or wider impact. If the user asks to review before submission, honor that request.

## 9. Verify completion and recover safely

A click is not proof of completion. After the final action, look for reliable evidence: a success message or confirmation reference, a created record, a sent item, a saved setting that persists after a safe reload, or a changed status.

If the site reports an error, inspect the resulting state before retrying. Some errors are cosmetic while the action has already succeeded; blind retries can create duplicates, payments, messages, or records. If completion cannot be verified, report what was attempted, the evidence available, and what remains uncertain. Do not describe an attempted action as completed.

| Symptom | Likely explanation | Safe response |
|---|---|---|
| A field was reportedly filled but is blank | The application ignored a direct value update. | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier values disappear after a later edit | A re-render reset uncommitted component state. | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used. | Find a multiline/editor control or use an acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node. | Inspect the labeled underlying control and target the actual editor. |
| A field looks filled but validation says it is empty | A hidden synchronization field was edited. | Use the visible interactive control that the application reads. |
| The automation layer becomes unstable | The chosen tool is unsuitable for the interaction. | Switch to a more robust browser method or supported direct interface; do not blindly rescue the session. |
| Headless and visible browsers differ | The site varies by browser context. | Prefer an authorized direct interface; use a verified visible session only when necessary and authorized. |
| A date widget changes values unexpectedly | The popover has stateful close, clear, or parsing behavior. | Close through a neutral action and re-verify affected values. |
| An error might be cosmetic | The action may already have completed. | Inspect resulting state before retrying. |

## Final audit

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Controls were inspected before editing and meaningful changes were read back.
- [ ] Required fields and validation passed the readiness gate.
- [ ] Explicit confirmation was obtained before a consequential final action.
- [ ] Completion was verified after acting.
- [ ] The final report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

As tools and sites change, retain reusable lessons as concise entries with a symptom, likely cause, and safe fix. Consolidate overlapping lessons rather than accumulating machine-specific details, account mappings, or one-off incidents.


---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, validating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, improve an existing one, evaluate whether it helps, or refine when it activates. A skill is a focused set of instructions, with optional resources, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the job, intended outcome, and boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and apply objective checks where they are meaningful.
5. Improve the skill using evidence rather than guesswork.
6. Repeat until the result is useful, reliable, and not narrowly fitted to a few examples.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the finished skill.

Do not force every project through every stage. Some users want a quick collaborative draft; others need a rigorous comparison. First determine where the user is in the loop, then help them make the next useful decision.

## Communication principles

Match the user’s technical vocabulary. Use plain English by default. Terms such as *evaluation* and *benchmark* are often useful, but explain them briefly if needed. Do not assume the user understands terms such as JSON, assertion, schema, or command line.

Explain why a question matters. For example, ask:

> What should a successful result look like: an answer in chat, a structured report, a downloadable file, or an approved external action? This determines how the skill should work and how it can be tested.

Keep the user involved at meaningful decision points:

- Confirm the intended job before writing extensive instructions.
- Ask before imposing a restrictive scope, required tool, or approval step.
- Share proposed test cases before treating them as the evaluation set.
- Let human review lead for subjective qualities such as usefulness, writing style, visual design, tone, and strategic judgment.

If the workflow will access communications, records, files, or other information about people, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant information, exclude unrelated sensitive details, respect privacy and consent expectations, and keep outputs within the appropriate access boundary.

## 1. Determine the starting point

Identify which situation applies.

### New skill

The user has an idea for recurring work, such as preparing updates, processing files, reviewing code, or generating a standard report. Start with discovery and a first draft.

### Existing skill

The user already has a draft or installed skill and wants it edited, simplified, tested, or improved. Preserve its established name and identity unless the user explicitly requests a change. Read the existing instructions before proposing revisions.

### Workflow demonstrated in conversation

The user may say, “turn what we just did into a skill.” Extract what you can from the conversation first:

- Inputs and source material used.
- Actions, tools, and decision sequence.
- Corrections or preferences the user expressed.
- Input and output formats.
- Quality checks and acceptance criteria.
- Conditions that caused the workflow to change direction.

Summarize the inferred workflow and list important gaps for confirmation. Do not silently convert a one-time workaround into a permanent general rule.

### Evaluation or optimization request

The user may have a finished-looking skill and want to know whether it works. Go directly to test design, evaluation, and revision. Do not rewrite a skill merely because a rewrite is possible.

## 2. Capture intent and scope

Gather enough information to define a coherent job. Adapt these questions to the situation instead of asking them mechanically.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What requests, phrases, or situations should cause the skill to be used?
3. **Inputs:** What information, files, examples, systems, and permissions may it use?
4. **Outputs:** What should it produce, modify, or recommend? Is a format required?
5. **Success:** How will the user know the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask, pause, decline, or hand work back to the user?
7. **Variations:** Which common cases, difficult cases, or exceptions materially change the work?
8. **Dependencies:** Does it need particular capabilities, references, templates, scripts, or approved data sources?
9. **Testing:** Should it be tested with representative requests before release?

Testing is especially valuable when outputs can be objectively checked, the workflow is consequential, the skill will be used repeatedly, or the skill performs multi-step work. A subjective creative skill may benefit more from qualitative review than formal pass/fail checks.

Useful choice questions include:

- Should the skill make a low-risk assumption when information is missing, or stop and ask?
- Should it produce a concise summary, a detailed report, or let the user choose?
- Should it work with any user-provided source, or only approved sources?
- Should it prepare a draft only, or is it allowed to take an external action after confirmation?

### Research before drafting

If appropriate resources are available, review relevant documentation, comparable skills, approved examples, and standards before drafting. Research should reduce burden on the user, not override the user’s requirements.

Use it to identify:

- Existing conventions and required output standards.
- Constraints of a file format, interface, or available capability.
- Reusable patterns from comparable work.
- Safety, privacy, regulatory, or approval requirements.

If sources conflict or important requirements remain uncertain, state the uncertainty rather than guessing.

## 3. Choose the skill structure

Keep a skill focused enough that users and AI systems can predict what it does. One skill may support closely related variants, but separate unrelated jobs when they have different audiences, permissions, sources of truth, or definitions of completion.

A portable package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional repeatable helpers
├── references/              # Optional detailed guidance
├── assets/                  # Optional templates or resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description used to decide whether the skill applies.
2. **Core instructions:** The workflow needed for ordinary use.
3. **Supporting resources:** References, templates, and scripts consulted only when relevant.

Keep the core instructions readable. If they become long, move detailed domain-specific material into clearly named reference files and state when each file should be read. Give large references a contents section or other clear navigation.

For a skill with variants, provide one selection workflow and separate references for each variant. The AI should read the relevant material, not load every possible variation by default.

### Use scripts only for justified repeatable work

Consider a helper script when test runs show repeated reconstruction of the same deterministic procedure, such as file conversion, validation, calculations, data cleanup, or document generation.

A bundled helper is valuable when it is:

- More reliable or easier to verify than repeated natural-language steps.
- Reused across multiple requests.
- Safer or less error-prone than recreating the process each time.
- Clearly within the user’s permission and intended scope.

Document what the helper does, its inputs, outputs, limitations, and when not to use it. Do not add automation merely because it is technically possible.

## 4. Write the skill

Write in clear imperative language. Explain the reason behind important instructions, especially when a rule prevents a predictable failure. An AI is more likely to adapt well when it understands the goal and tradeoff than when it receives a long list of unexplained prohibitions.

Include the following sections when they apply.

### Purpose and scope

State the job, intended outcome, and boundaries. Clarify whether the skill creates a response, produces a file, changes data, takes an external action, or guides the user through a process.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State how to proceed if a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask the user for an export or prepare a draft clearly marked as incomplete.
```

For private or personal information, include the authorization boundary. For example, instruct the AI to use only approved records relevant to the stated purpose and to omit unrelated personal details.

### Workflow

Give the normal sequence of actions and include decision points rather than attempting to list every possible edge case.

A durable workflow commonly follows this order:

1. Inspect the request and available inputs.
2. Identify missing information that would materially change the result.
3. Confirm requirements or make low-risk assumptions where appropriate.
4. Gather evidence from approved sources only.
5. Perform the requested work using the appropriate method.
6. Check the result against the requested format and success criteria.
7. Present the result, assumptions, sources, and unresolved limitations.

Use conditional rules where needed:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite important work or affect an outside system, describe the impact and ask for confirmation before proceeding.
```

### Output format

When consistency matters, define a template:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding and supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing input]
```

Do not impose a rigid format when usefulness depends on adapting to context. In that case, define the outcome and quality goals, with a short example if it teaches a distinct pattern.

### Quality and safety checks

State checks needed before completion. Relevant checks may include confirming required fields, validating calculations, citing support for important claims, preserving original data, distinguishing evidence from assumptions, and flagging uncertainty.

The skill’s behavior should match what a user would reasonably expect from its description. Do not conceal actions, bypass authorization, collect unnecessary private information, enable unauthorized access, or create deceptive outputs. For external, irreversible, high-impact, or permission-sensitive actions, obtain confirmation at the appropriate point.

### Failure behavior

Describe recovery rules in general terms:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable source or capability:** Explain what cannot be verified and offer a safe alternative.
- **Ambiguous request:** Make a reasonable low-risk assumption only if it does not materially change the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, disclose the issue, or request guidance.
- **Access or privacy boundary:** Stop using the source and ask for authorization, a narrower scope, or a user-provided extract.

## 5. Write the description for activation

The skill description is a routing instruction. It should state both what the skill does and when it should be used.

Cover realistic language users might use, including requests that imply the job without naming it directly. Be specific enough to reduce missed activations, but not so broad that the skill captures unrelated work.

A good description includes:

- The task or outcome.
- Common user contexts that indicate the task.
- Important scope limits where they prevent costly or unsafe false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a progress update, leadership summary, milestone review, risk summary, or a concise account of next steps, even if they do not use the phrase “status report.”
```

Put activation guidance in the description, not hidden in the body. Do not put the entire procedure in the description or use vague labels such as “help with documents.”

## 6. Review the draft before testing

Read the skill again as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description clearly state when to activate?
- Are required inputs, permissions, and outputs clear?
- Does the workflow explain why important checks exist?
- Does it handle missing information and unavailable resources?
- Are there unnecessary rules, repetitions, or brittle wording?
- Does it avoid assuming one person’s habits, local systems, private access, or terminology?
- Would a capable AI have enough discretion to handle normal variation?

Prefer lean instructions over a long list of rules that do not affect outcomes. Frequent capitalized absolutes are a warning sign unless the behavior is a true safety, authorization, or data-integrity boundary.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Show them to the user and ask whether they reflect real use.

For each case, record:

- A descriptive identifier.
- The prompt.
- Supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates and flag information that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningfully different situations:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic variation that changes the workflow.
- A request requiring confirmation or a safe refusal, when relevant.

Avoid tests that merely repeat the skill’s wording. Vary phrasing, detail level, and user sophistication. Test general classes of difficulty, not personal incidents.

## 8. Run comparisons and preserve evidence

When independent runs are available, compare the skill with a meaningful baseline.

- **New skill:** Run each test with the skill and without it.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revised skill with the earlier version.

Run comparison conditions under comparable circumstances. If parallel execution is available, start both conditions for each test at the same time. Preserve the prompt, supplied files, outputs, and available timing or resource information.

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

For each test, save metadata in a portable form:

```json
{
  "eval_id": "typical-request",
  "eval_name": "typical-request",
  "prompt": "[Test prompt]",
  "assertions": []
}
```

Record timing or resource-use data immediately when the execution environment reports it, because some environments do not retain it afterward.

If independent runs are not available, perform a transparent sanity check: follow the skill for each prompt, save the results, and ask the user to review them. Do not present this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs are underway, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are observable and meaningful:

- Required sections are present.
- A produced file opens and contains required fields.
- Calculations match known values within an agreed tolerance.
- The output identifies missing mandatory input.
- Important claims have required source references.

Record each grade with a clear statement, pass/fail result, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable inputs and requests them."
    }
  ]
}
```

Use automated checks where practical. They are faster, more consistent, and reusable across iterations. Do not force numerical checks onto writing quality, aesthetics, strategic value, or other qualities that need human judgment.

## 10. Review, analyze, and improve

Present outputs and measurements in a review format the user can inspect. If a review interface is available, use it to show each prompt, output, comparison output, formal grades, timing data, and a place for comments. If not, present accessible files or a clear conversational review.

Ask focused questions:

- Which output would you trust in normal use, and why?
- What was missing, misleading, or hard to use?
- Did the skill add work or detail without enough value?
- Would this work for similar requests with different data or wording?

Then look beyond overall pass rates. Identify:

- Checks that pass for every condition and do not distinguish value.
- High-variance results that suggest ambiguity or instability.
- Quality gains that cost disproportionate time or resources.
- Failures with a shared root cause.
- Repeated planning, research, formatting, or helper creation that does not improve outcomes.

Revise based on underlying causes, not individual test wording. Explain the reason for new guidance. Remove instructions that do not earn their complexity. Add a reusable script, template, or reference only when repeated evidence shows it is valuable.

After revision, rerun the full test set in a new iteration, compare it with the chosen baseline, and show prior outputs when useful. Continue until the user is satisfied, feedback is consistently positive across meaningful cases, objective requirements are reliably met, or further changes no longer produce meaningful improvement.

## 11. Optional blind comparison

For a stronger comparison between two versions, give outputs to an independent reviewer without revealing which version produced which result. Ask the reviewer to judge against a shared rubric such as correctness, completeness, clarity, adherence to constraints, safety, and practical usability.

Use blind comparison when versions have similar measurements but differ in qualitative quality, when a decision has material importance, or when reviewer bias is a concern. Analyze why one output was preferred before revising again.

## 12. Optimize activation after the skill works

Only optimize the description after the workflow itself is useful.

Create a realistic set of activation queries with both cases that should activate the skill and difficult near-misses that should not. Include varied wording, formal and casual requests, direct and implied needs, common cases, less common valid cases, and adjacent tasks that belong elsewhere.

Review the set with the user before using it. Keep separate examples for improving the description and for selecting among candidate descriptions. If repeated evaluation is available, run each candidate more than once and select based on held-out cases rather than only the examples used to edit it.

Remember that an AI may not consult a specialized skill for a trivial one-step request even if the description matches. Test with substantive requests where the skill would provide real value.

## 13. Package and hand off

Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on undeclared private access, personal conventions, or a specific product.
- Scripts and references are present, clearly named, and documented.
- No credentials, confidential records, private identifiers, or sensitive examples are included.
- The user can install or adapt the package in their chosen environment.
- Test material is included only when it is safe and useful to retain.

Provide a short handoff note explaining what the skill does, required capabilities, known limitations, and how to perform a basic post-installation test.

## Final readiness gate

A skill is ready when it has a clear job, an accurate activation description, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.


---
name: test-every-screen-size
description: Verify every UI or CSS change across representative narrow, wide, short, and tall viewports using screenshots and programmatic layout checks. Fix and retest every failure before reporting the change as complete.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, color, or background changes: a local edit can alter wrapping, height, overflow, alignment, or visible backgrounds at other screen sizes.

A bounding-box check alone is not enough. A single desktop and mobile screenshot are not enough. Real screenshots and numerical checks catch different failures, so use both.

## 1. Prepare realistic test states

Run the real interface in an appropriate test environment. Populate the changed surface with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative lists, cards, rows, and validation messages;
- realistic item counts or content near expected limits;
- loading, empty, and error states when the change affects them.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping problems, and unintended blank space.

## 2. Choose the viewport sweep

Use these baseline widths unless the product's supported-device requirements call for a different set:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages or interfaces likely to be used on large displays. Include any required customer, device, embedded-window, or product-specific viewport as an additional test case.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

For changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment, include a very tall viewport. Use a height representative of the largest expected display or browser window; 1600–1800 px is a useful general test range.

Use a repeatable browser automation or browser-testing system available to the project. Run it headlessly when an interactive display is unnecessary.

## 3. Capture and inspect screenshots

Capture real screenshots at every relevant viewport and state. Use full-page screenshots when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect every affected component on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design now that the component has changed role or size.

Pay special attention to edge-to-edge or full-bleed changes. Making a component flush on one edge can expose leftover wrapper margins or padding as visible background strips on another edge. Check every edge, not only the edge edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is intended to fit the viewport;
- no changed element overlaps neighboring content or its intended container;
- buttons, links, and fields remain visible and usable;
- fixed or sticky UI does not hide essential content;
- cards, lists, and form controls remain within intended bounds;
- body text retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant element rectangles with adjacent elements and container boundaries. Check only relationships that are expected to be non-overlapping; intentionally layered elements need an explicit expected relationship.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line; reading-focused designs commonly target roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visual defects such as exposed background strips, poor balance, or unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and the relevant programmatic checks pass.

## 6. Fix failures and rerun the sweep

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the failing size.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights or states, and checks performed.

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

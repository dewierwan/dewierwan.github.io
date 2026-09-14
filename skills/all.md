# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when a user needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas; it is to surface meaningfully different paths, make tradeoffs clear, and leave the user with a small set of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources available in the current environment, review them first.

Access private communications, records, or information about people only when there is a legitimate purpose and clear authorization. Use the minimum relevant sources and information, omit unrelated or sensitive personal details, and keep the resulting analysis within the appropriate access boundary.

If the question is not self-contained, retrieve only a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, deadlines, or budgets
- Stakeholder concerns, responsibilities, and approval boundaries
- Evidence about what has already been tried

Do not search broadly by default. If important information is unavailable, state an assumption or ask a focused question instead of inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The user’s wording may describe a symptom or a preferred solution rather than the real decision. For example, “Should we add a feature?” may actually mean, “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip the pause only when the framing is obvious, low-stakes, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must represent a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes process, incentives, scope, ownership, or the problem framing
- At least one surprising option, such as delaying, partnering, removing scope, or doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, or avoided distraction has genuine value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

| Element | What to include |
|---|---|
| **What** | One or two sentences explaining the approach. |
| **Strengths** | One or two concrete advantages. |
| **Weaknesses** | One or two concrete disadvantages, risks, or limitations. |
| **Effort** | Low, Medium, or High. |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose evaluation criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, operational burden, and stakeholder impact. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when instructive, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits the user’s situation, constraints, and goals—not why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may choose an option, request detail, reject the framing, ask for additional options, or combine approaches.

If the user proposes a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that states the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After the decision is recorded, move into planning and execution: requirements, milestones, tasks, dependencies, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Avoid skipping the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than only the first proposed solution.
- The options are genuinely distinct and not variations of one another.
- At least one option challenges the default framing when that is useful.
- Strengths and weaknesses are concrete, candid, and balanced.
- Effort labels are plausible for the user’s constraints.
- Recommendations follow the user’s stated criteria rather than unstated assistant preferences.
- Any retrieved private context was authorized, necessary, minimized, and not exposed beyond the appropriate boundary.


---
name: pressure-test
description: Find the weak points in a leading strategic idea before commitment by steelmanning it, testing its load-bearing assumptions through sequential challenge, and ending with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or create an implementation plan.

## Where this fits

Use the process in this order:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the selected approach, if applicable.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes a defense of that idea.
- If this exact topic was pressure-tested recently and no material evidence, assumption, or condition has changed, do not repeat the exercise. Use the existing findings in the decision process.
- If using private communications, records, customer data, or information about individuals, confirm a legitimate purpose and clear authorization. Use only the minimum relevant material, keep sensitive details out of the output, and respect the intended access boundary.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a weak caricature.
- Ask one forcing question at a time. Wait for the answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Use available evidence, such as research, metrics, prior experiments, customer feedback, documented decisions, or stakeholder input. Separate facts, inferences, and forecasts.
- Identify relevant dissenters by role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by the damage caused if they are wrong, starting with the most consequential.

| Rank | Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|---|
| 1 | [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Name a test or disproof condition] |

Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions, then adapt later questions to the answers received. Do not present the full set as a questionnaire, because that permits selective answering.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed? Why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence. Ask for observed behavior, data, a comparison, or a concrete commitment that supports the belief.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failures, external changes, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable early signal] | [Name the check or accountable role] |

Warning signs must be observable early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap. Do not treat silence as agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data collection period. Next: run that test, then decide with the result recorded. Do not commit while the gap remains open.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, the downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with exactly one concrete next action containing a verb, an owner, and a deadline when useful.

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
- exactly one concrete next action.

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and giving a positive verdict without falsifiable criteria or monitoring.

## Improve the workflow responsibly

After a completed run, capture any reusable lesson about missing evidence, weak questions, or unclear decision criteria. Update the chosen workflow or playbook only through the normal review and authorization process. Do not alter records silently, and do not retain unnecessary personal or sensitive information from the discussion.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make decisions with the right amount of rigor. The goal is not maximum analysis. It is to make a clear call when ready, preserve reasoning for meaningful choices, and learn from outcomes.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** Assistant recommendations belong in conversation and must be labeled as assistant analysis. Include them in a decision record only if the user asks.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution. Plan or do the task instead.
5. **Record only with permission.** “Should we do X?” asks for analysis, not for a record. Create or update a record only when the user asks to log, track, open, commit, or otherwise save it, or has explicitly agreed to that practice.
6. **Protect privacy and access boundaries.** Before consulting shared communications, personnel information, customer records, or a shared register, ensure there is a legitimate purpose and clear authorization. Use the minimum relevant sources and omit unrelated personal or sensitive details.
7. **Do not deliberate forever.** Once the appropriate rigor and readiness checks are complete, make the call and move forward.

If a record is visible to other people, confirm that the audience is appropriate before writing. For health, relationships, compensation, confidential personnel matters, or similarly sensitive topics, offer a private document or keep the discussion in chat.

## 1. Choose the mode

Determine whether the decision is new or already exists in an authorized decision register.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review point and has not received an outcome assessment.

If the user explicitly names the mode, follow that instruction. Otherwise, if authorized, search the available register for overlapping decisions before creating a duplicate.

For a resume, retrieve the existing record and append new information rather than overwriting history. For a review, use the original prediction and reasoning as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Write the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What is the deadline or trigger for deciding?
- What result is desired?
- What happens if no action is taken?

If the question is broad and there are no credible options, generate options before evaluating them. Do not pressure-test a vague problem statement.

If there is only one viable path, say so directly: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time if needed. Put the choice in one bucket.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not record by default |
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

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until the user commits. When resuming, append a new dated thinking-log entry rather than rewriting history.

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

---

## Retrospective
To be completed at review.
```

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

Use this workflow for a non-trivial product, technical, process, integration, automation, or operational problem where the solution is not already clear. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the problem

Start with the underlying problem, not the user’s proposed solution. If they ask to build something, work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today?
- What workarounds, failures, delays, or costs exist?
- How frequent, urgent, or blocking is the issue?
- What outcome would materially improve the situation?

Write a concise problem statement and descriptive requirements. State the desired outcome and constraints, not a presumed implementation. If the proposed solution does not appear to solve the stated problem, say so directly.

Ask only for information that cannot be found in authorized, relevant context. When reviewing communications, records, or user data, confirm a legitimate purpose and clear authorization; use the minimum relevant sources and omit unrelated or sensitive personal details.

## 2. Decide whether to solve it now

Assess severity, frequency, affected users, opportunity cost, existing alternatives, and maintenance burden. Treat **do nothing**, **deprioritize**, or **improve the current workaround** as valid options when the problem is low-impact or adequately handled.

Separate decisions by reversibility:

- **Reversible decisions:** small choices that are easy to change. Use reasonable judgment, choose, and proceed.
- **Hard-to-reverse decisions:** persistent data changes, migrations, public interfaces, long-lived configuration, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the commitment warrants it.

If priority or direction is unclear, present the tradeoff to the responsible decision-maker before investing heavily in design or implementation.

## 3. Research the current context

Read the relevant project guidance, architecture notes, repository documentation, existing code, tests, operating procedures, and prior attempts. Find established patterns, reusable components, and constraints before inventing something new.

Understand compatibility, deployment, security, ownership, monitoring, supported environments, and access boundaries. Follow the system’s established conventions unless there is a strong, documented reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve existing authentication, permissions, and data behavior.
- Must fit the available delivery time and maintenance capacity.
- Should avoid new dependencies and long-lived configuration.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

Without criteria, the first plausible approach can win by accident.

## 5. Generate varied approaches

Generate genuinely different options, not minor variations of the same design. Consider:

1. Do nothing, defer, or improve the workaround.
2. A non-code solution: clearer guidance, a process adjustment, a template, or an existing platform capability.
3. A small, targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For a highly ambiguous problem, generate a broader candidate set before narrowing. Describe each option briefly: what it is, what it solves, major costs, and key risks.

### Technical design principles

- Prefer one understandable code path over runtime-specific special cases.
- Validate strictly and fail fast for invalid states; do not silently turn programming errors into plausible but wrong results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer bounded changes that can be deleted or rolled back cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Place changes in the appropriate design boundary; do not use a quick fix that creates hidden future cost.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal containing:

| Section | Required content |
|---|---|
| Problem | Concise problem statement and desired outcome. |
| Criteria | The evaluation criteria used to compare options. |
| Options | Viable approaches with meaningful tradeoffs. |
| Recommendation | One clear recommendation and why it is preferred. |
| Decisions and risks | Important open questions, irreversible consequences, and mitigations. |

Keep proposals direct. Store a durable proposal in the user’s chosen shared documentation system when review, approval, or collaboration requires it; otherwise provide it in the current workspace. Use a clear date-prefixed title, such as `14 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, verify, and hand off

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration and rollback strategy, test strategy, deployment steps, and follow-up ownership. Put the plan where relevant reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Check the result against the evaluation criteria, including compatibility, permissions, failure behavior, and rollback expectations.

Do not claim success based only on completed code or configuration. State what was tested, what passed, and what remains unverified. Commit, publish, or deploy only according to the user’s repository and release practices.

Finish with a focused handoff:

- What changed and the user outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required rollout, monitoring, or user actions.
- Links or references to the proposal, plan, and change set when applicable.

## Readiness and audit checks

Before recommending: confirm the problem statement, criteria, alternatives, recommendation, and hard-to-reverse decisions are clear.

Before implementing: confirm authorization, scope, approval for consequential commitments, and a verification plan.

Before handoff: confirm outputs remain within the appropriate access boundary, sensitive details are excluded unless necessary and authorized, and success claims match actual evidence.

Common failure modes are implementing the first requested solution without diagnosing the problem, adding permanent configuration for a temporary need, silently hiding invalid states, treating a hard-to-reverse commitment as routine work, and reporting completion without meaningful verification.


---
name: shape-and-draft
description: Shape consequential documents by reviewing evidence, resolving material choices through answer-dependent interview rounds, checking readiness, and then drafting and auditing the smallest document that can achieve the goal.
---

# Shape and draft a document

Develop a consequential document by shaping the underlying thinking before writing it. Work out what the document must achieve, gather relevant evidence, resolve the choices that could change its substance with an authorized decision-maker, and then draft the smallest document that can do the job.

Use this workflow for strategies, narratives, operating agreements, proposals, briefs, scorecards, and decision memos when the artifact, argument, boundaries, commitments, or operating model are still unsettled. Do not use the full process for a simple edit, formatting task, or document whose content and decisions are already clear.

When using private communications, internal records, or information about people, first confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and details. Omit unrelated or sensitive personal information, respect consent and privacy expectations, and keep both research and outputs within the appropriate access boundary.

## Classify the request

A request may name a document type, desired outcome, audience, source material, or some combination. Treat a proposed format as a hypothesis until its purpose is clear.

Use a **full shaping process** when the document is strategically important, when material choices remain open, or when the requester asks for deep thinking, several question rounds, or close alignment before drafting.

A substantive interview round resolves a distinct layer of choices and uses the answers to decide what to ask next. Repeating existing information, restating the model, or seeking general approval does not count as a substantive round.

## 1. Work backwards from the outcome

Start with the change the document must produce. Establish:

- Who will read it.
- What readers should understand, decide, approve, or do afterward.
- What is unclear, contested, blocked, or going wrong now.
- Whether the document mainly needs to explain, persuade, decide, coordinate, or govern.

Do not accept “write a strategy” or “make a narrative” as the goal. Identify the practical job the document must perform.

## 2. Select the artifact

Recommend the form that best serves that job.

- **Narrative:** Builds shared understanding of why something matters and what direction is being proposed.
- **Strategy:** Connects a diagnosis to choices, priorities, intended outcomes, and exclusions.
- **Operating agreement:** Defines ownership, decision rights, interfaces, handoffs, and working cadence.
- **Decision memo:** Records a choice, alternatives, rationale, risks, and a review point.
- **Scorecard:** Defines a role or team mission, outcomes, and role-relevant capabilities.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the meaningful tradeoff and recommend an artifact. If the choice would materially affect the argument, required decisions, or structure, ask the authorized decision-maker to confirm it before going deeper.

## 3. Gather and classify evidence

Read supplied material first. Follow stated rules for source selection, authority, citations, and links. Scale the research sweep to the stakes and use the available systems and sources appropriate to the task.

For a consequential internal document, seek sources that could establish prior decisions, current definitions, supporting evidence, dissent, constraints, ownership context, and relevant performance information. If records concern individuals, include only information necessary for the document’s legitimate purpose.

Apply these evidence rules:

- Respect any stated source-of-truth hierarchy.
- Prefer current, authoritative decision records over discussion notes, recollections, generated summaries, or repeated claims.
- Resolve contradictions where the evidence permits and surface material contradictions that remain.
- Do not ask a participant for facts that available sources can answer.
- Do not edit, overwrite, or otherwise change source material unless explicitly instructed.

Keep evidence separate from alignment. Sources can establish what happened, what was recorded, what people said, and what an authoritative record currently states. They do not automatically establish what the current decision-maker believes, wants to promise, or is willing to exclude.

Treat a plausible synthesis, repeated pattern, or implication as **inferred**, not settled. Ask for confirmation when an inference would become a central claim, commitment, boundary, recommendation, or operating rule.

Before the first interview round, provide a short situation brief that states:

- What the sources establish.
- What has already been explicitly confirmed.
- What is inferred but not confirmed.
- The central tension, gap, or missing logic.
- The recommended artifact.
- The material questions that only an authorized decision-maker can resolve.

## 4. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds already completed in the current conversation and do not repeat settled questions.

Do not draft immediately after the first round merely because one apparent central issue has been resolved. A later round should test the implications of earlier answers, such as boundaries, counterarguments, ownership, definitions, risks, or execution details.

Ask four to eight focused questions per round. If fewer than four material questions remain, ask only those questions and say that this is a narrow final check. Do not add ceremonial questions to meet a target.

Each numbered question should normally seek one decision. Do not bundle independent choices, such as ownership, coordination, handoffs, and success measures, into a single broad question. Bundling creates false alignment.

Use one answer surface for each round. Normally, provide a plain-text numbered question block in the conversation. Do not duplicate the same questions in both chat and a separate form. If the chosen environment requires a form, include enough context to answer and treat a substantive reply as an answer even if the interface appears incomplete.

Use a compact format that supports shorthand answers:

1. Number questions continuously across rounds so replies remain unambiguous.
2. For bounded choices, offer three or four mutually exclusive, decision-relevant options labeled `a.`, `b.`, `c.`, and, if useful, `d.`.
3. Use two options only when there are genuinely two distinct states. Do not invent alternatives merely to fill a list.
4. Put the recommended option first unless prior context makes another order clearer.
5. Keep questions and options on consecutive lines without blank lines inside the question block.
6. Allow the respondent to reject the framing, qualify an option, or provide a different answer.

Example:

1. Which direction should the document recommend?
   a. Focus first on the highest-impact problem; this narrows scope but clarifies accountability.
   b. Address all related problems equally.
   c. Present options without a recommendation.
2. Who should make the final decision?
   a. The accountable lead after consultation.
   b. A cross-functional decision group.
   c. A senior sponsor after reviewing the evidence.

Each round should:

1. Begin with an updated model of the situation and state what changed because of prior answers.
2. Focus on one layer of uncertainty instead of mixing every issue at once.
3. Offer concrete options when the decision can be bounded and explain the key tradeoff behind the recommendation.
4. Separate source-supported observations from choices the decision-maker must make.
5. Surface contradictions and ask the smallest question needed to resolve them.
6. Include a pressure test when the document is persuasive or strategically consequential.
7. Leave room for a different framing or an alternative decision.

A typical progression is purpose, strategy, operating model, definitions and measures, then expression and delivery. Adapt the sequence to the work, but preserve the answer-dependent loop: later questions should arise from earlier answers, not from a generic questionnaire.

After every answer round:

1. Match shorthand and free-text replies to their question numbers. Preserve qualifications such as “mostly c” or “not sure.” Classify each reply as confirming, rejecting, softening, qualifying, or deferring the proposed position.
2. Mark only genuinely unanswered or unclear material choices as open. Do not repeat a settled question because an interface appears stale.
3. Trace downstream implications. A changed audience, softened commitment, new exception, or rejected framing often creates another important question.
4. Update the alignment ledger and show a concise synthesis.
5. Generate the next round from remaining material uncertainties and their consequences.

Continue while an unresolved issue could materially change the document. If the requester explicitly asks to draft before the process is complete, briefly name the one or two most important consequences of the uncertainty, then follow the instruction.

## 5. Maintain an alignment ledger

Keep a compact working record throughout the conversation:

- **Confirmed:** Choices explicitly made by an authorized decision-maker.
- **Source facts:** Claims established by current, authoritative evidence but not selected as current choices.
- **Inferred:** Plausible interpretations that remain unconfirmed.
- **Open:** Questions that could materially change the document.
- **Corrected:** Assumptions or claims a participant has rejected.

Update the ledger after every answer round. Never reintroduce a corrected assumption. If confirmed statements conflict, surface and resolve the conflict rather than concealing it in vague language. Never promote an inference to confirmed merely because several sources support it.

For a full shaping process, show a concise version of the ledger before each later round. Every major claim in the draft must be a confirmed choice, a supported source fact, or explicitly framed as a proposal, assumption, or open question.

## 6. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document’s substance. Before drafting, provide a concise pre-draft synthesis covering the intended job, audience, central position, important boundaries, and deliberate open questions.

For every major planned claim, ask:

> Was this confirmed by an authorized decision-maker, established as fact by authoritative evidence, or merely inferred?

If a material claim is only inferred, ask another question or clearly label it as a proposal. Do not present it as settled.

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

Close alignment does not require artificial certainty. It means the remaining uncertainty is low impact or is explicitly represented as unresolved.

## 7. Draft and deliver

Follow the requested voice, style, format, accessibility needs, privacy boundary, and delivery requirements. When no style is specified, use direct, plain language appropriate to the audience.

Write the smallest document that accomplishes the agreed purpose. Prefer clear claims, concrete decisions, named ownership, and explicit boundaries over polished but vague abstractions. Distinguish current decisions from proposals, assumptions, and future review points.

Keep action-oriented sections short. As a useful default, use five or fewer top-level bullets for the main outcomes and avoid more than seven in a section. Combine related points, remove lower-value detail, or place essential background in an appropriate supporting source.

When producing a formatted document in a document system, inspect both its structure and rendered appearance. End a list before the next heading, avoid blank paragraphs used only for spacing, and check that headings, lists, indentation, and page breaks render as intended.

Make the draft as simple as the substance allows:

- Prefer common words over formal or inflated language.
- Write complete, natural sentences. Do not make connected ideas choppy merely to shorten them.
- State the point first and remove warm-up text, repeated context, and unnecessary qualifications.
- Turn abstractions into concrete claims, actions, owners, dates, examples, or tests where useful.
- Use focused paragraphs and bullets only for real lists.
- Prefer the more concise version when it preserves meaning; concision means removing unnecessary ideas and words, not forcing every sentence to be short.
- Keep hard ideas when they matter, but explain them plainly rather than hiding them in jargon.

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
- Does the document match the requested voice, audience, and access boundary?
- Can each sentence be understood on the first read?
- Can any abstract phrase, inflated word, or repeated point be simplified or removed without losing meaning?
- If formatted outside the conversation, does the rendered document have usable headings, lists, spacing, indentation, and page breaks?

Fix mismatches before delivery. Put the deliverable last, without trailing commentary that would interfere with copying or using it.

## Failure modes to avoid

- Drafting early because producing text feels productive.
- Treating the proposed artifact as fixed before its purpose is known.
- Asking participants for facts that available evidence can answer.
- Reviewing private records without a legitimate purpose, authorization, or appropriate access boundary.
- Mistaking extensive research for alignment on current choices.
- Treating a plausible synthesis as a confirmed decision.
- Using a generic questionnaire disconnected from evidence and prior answers.
- Failing to update the working model after each round.
- Stopping after one round without testing consequences.
- Bundling independent decisions into a single question.
- Repeating questions already answered or duplicating a question round across interfaces.
- Concealing contradictions through vague language.
- Continuing interviews after only low-impact uncertainty remains.
- Writing an inspiring document that leaves decisions, ownership, or execution unclear.
- Mistaking concise writing for choppy writing, fragments, or noun-only bullets.
- Treating structurally valid formatting as sufficient without checking the rendered document.


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
description: Create an evidence-based case study post about a person’s career, learning, or professional change. The workflow produces a review-ready draft, alternate hooks, quote-card options, and an approval log.
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

Before drafting, identify whether you have enough verified information for these fields:

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns |
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
description: Gather authorized meeting context, clarify the user’s intended outcome, and create a privacy-conscious meeting preparation page with a practical agenda, decision-focused questions, and an appropriate follow-up plan.
---

# Prepare for a meeting

Use this workflow when a user asks to prepare for a meeting, review a day of meetings, or create a meeting-preparation page. The durable deliverable is a complete page in the user’s chosen workspace, not only a chat summary.

Use it for consequential external meetings, small group discussions, recruiting conversations, negotiations, advisory calls, sales or partnership meetings, and recurring relationship meetings. Scale the depth of research and planning to the stakes, meeting length, and time available.

## Core principles

- Research before drafting, but do not mistake research for preparation.
- Read the artifact that caused the meeting, if one exists. An agenda based only on participant biographies is often generic and weak.
- Ask targeted questions before finalizing the meeting goal or agenda when strategic choices remain open. The user chooses the outcome and boundaries; the assistant translates those choices into a meeting plan.
- Access private communications, records, transcripts, and internal notes only for a legitimate meeting-related purpose and with clear authorization. Use the minimum relevant sources and information.
- Keep shared preparation pages within their intended access boundary. Exclude unnecessary personal details, confidential material, compensation information, and unrelated history.
- Make the page useful in two modes: detailed enough to read beforehand and scannable enough to use during the meeting.

## 1. Define the scope

Confirm or infer the following before gathering information:

- **Date or date range:** If no date is supplied, use the user’s current local date as a broadly useful default.
- **Meetings to prepare:** By default, include meaningful external one-to-ones and small external group meetings. Exclude focus blocks, personal holds, routine internal blocks, and events with no real meeting purpose unless the user asks to include them.
- **Output destination:** Use the user’s chosen meeting database, notes workspace, document system, or folder.
- **Audience and sensitivity:** Determine whether the resulting page is private to the user or visible to a wider group. This affects what may safely be included.

For each selected event, extract:

- Meeting title, date, start time, and scheduled duration
- Participants and organizations, where known
- Location or call details, if relevant
- Invitation description, scheduling notes, and stated purpose
- Linked documents, proposals, decks, prior notes, or transcripts
- Evidence of why the meeting was scheduled now

If an event is ambiguous, do not assume it is important, external, or safe to research broadly. Ask the user whether to include it.

## 2. Research meeting context responsibly

Research each relevant external participant and the substantive topic of the meeting. Use the minimum relevant set of sources that the user is authorized to access. Typical sources include:

1. **Direct correspondence:** Recent messages sent to or received from a participant.
2. **Indirect mentions:** Relevant messages or notes that mention the participant or organization, such as introductions, referrals, previous decisions, or project discussions.
3. **Authorized collaboration records:** Relevant team discussions, earlier meeting notes, and project materials.
4. **Calendar history:** Earlier meetings with the same participant or organization.
5. **Public sources:** Professional profiles, organization websites, publications, public announcements, and reliable recent news.
6. **Meeting artifacts:** Any proposal, memo, deck, draft, brief, analysis, application, or shared document that is the subject of the meeting.

### Source-use and privacy rules

Before accessing private communications or records about people, ensure there is a legitimate purpose and clear authorization. Review only material relevant to preparing for this meeting. Do not collect, copy, or reproduce unrelated personal details, sensitive information about third parties, or confidential content that does not help the user prepare.

Treat candidate information, customer information, internal commentary, and forwarded messages as confidential by default. Prefer short paraphrases over quotations. Include details in the final page only when they are necessary for the meeting and appropriate for the destination’s audience.

Do not place salary, compensation, equity, offer figures, pay bands, or other pay-related numbers in a broadly shared meeting page. If such context affects the meeting, use a neutral reference such as “offer follow-up” or “compensation discussion,” without figures.

### Research procedure

For each participant, establish the following where relevant:

- **Who they are:** Current role, organization, relevant background, and decision-making context.
- **What their organization does:** Its mission, offering, market context, and relationship to the user’s organization or project.
- **Relationship history:** Prior meetings, introductions, commitments, unresolved questions, and the overall relationship arc.
- **Why this meeting is happening:** The triggering request, referral, deadline, decision, or follow-up.
- **Current context:** Recent changes, publications, launches, organizational developments, or timely facts that matter to the meeting.
- **Useful links:** Only professional or public links that meaningfully help preparation.

Do not treat a search result as established fact without checking its source and reliability. Separate verified facts, another person’s reported view, and your own hypothesis.

### Read the relevant artifact in full

If the meeting concerns a written artifact, locate and read it before preparing an agenda. Signals include:

- A request for feedback on a proposal, deck, memo, or draft
- An invitation referring to a plan, analysis, strategy, or shared document
- Recent messages noting comments or revisions on a document
- A request to discuss a pitch, report, application, or project plan
- A linked file or workspace page in an invitation or correspondence

Read the full artifact, including substantive appendices, sections, tabs, comments, and linked supporting material where available. Do not skim a detailed document and then ask broad questions such as “Tell me about your plan.” Identify its main claims, assumptions, tradeoffs, decision points, evidence gaps, dependencies, and points worth pressure-testing.

If the meeting clearly concerns an artifact but it cannot be found, ask the user for the link before drafting a detailed agenda. Explain what is missing and why it matters.

## 3. Route specialized meetings correctly

Before creating a general meeting page, determine whether the meeting needs a specialized workflow.

Examples include:

- A reference conversation about a job candidate
- A formal interview or work-sample assessment
- A performance, legal, medical, safeguarding, or crisis discussion
- A board, financing, procurement, or contract negotiation requiring a dedicated template

For a reference conversation, use an authorized reference-call workflow rather than a generic meeting agenda. Focus on role-relevant capabilities, concrete evidence of performance, working conditions, strengths, risks, and questions that distinguish relevant performance. Avoid compensation information and unrelated sensitive personal details.

Carry forward already gathered relevant context so work is not duplicated. Keep specialized records within the appropriate access boundary.

## 4. Provide a situation brief before asking questions

Do not draft the final goal or agenda immediately after research. First provide a concise situation brief so the user can reload the context, correct errors, and choose the right strategy.

Choose the shape that fits the meeting.

### Narrative brief

Use this as the default for most meetings. In a short set of headed sections, cover:

- Who the participant is
- Where the relationship stands
- Why the meeting is happening now
- The main opportunity, uncertainty, or tension

The brief should take roughly a minute to read.

### Decision-shaped brief

Use this for negotiations, recruiting closes, sales conversations, fundraising, partnerships, or any meeting with a live decision. Cover:

- The ask or decision at stake
- The other party’s likely alternatives, constraints, and deadlines
- The user’s position, leverage, and limits
- Material risks and unknowns
- What must happen to preserve momentum

For a high-stakes meeting, combine a short narrative brief with a decision-shaped section when both personal context and deal dynamics matter.

### Brief quality check

Before sharing the brief, verify that it:

- Distinguishes facts from inferences
- Names important unknowns rather than hiding them
- Identifies the actual meeting trigger
- Avoids unnecessary confidential or personal details
- Says whether this is a first meeting or summarizes the relationship arc if it is recurring

## 5. Ask targeted questions and wait for answers

Targeted questions are a readiness gate whenever the desired outcome, stance, tone, or ask could materially change the agenda. Do not replace them with “What agenda do you want?” The assistant’s job is to convert the user’s strategic choices into a useful agenda.

You may skip questions only when the purpose is genuinely fixed and well documented, such as a routine recurring meeting with a stable agenda and no meaningful open choices. When uncertain, ask.

Always cover the **primary goal** and at least one of **failure mode**, **tone**, or **specific ask**. Always include an **anything else** catch-all question.

Useful question axes include:

- **Primary outcome:** Relationship-building, information-gathering, decision, commitment, recruitment, sale, advice, handoff, or another outcome.
- **Their situation:** Whether their role, interest, constraints, or decision status is uncertain.
- **Sensitive substance:** Whether to state the user’s view directly, hold it back initially, or ask for the other party’s perspective first.
- **Failure mode:** Overselling, underselling, discussing the wrong topic, losing trust, failing to secure a next step, or making an unapproved commitment.
- **Specific ask:** Whether to request an introduction, commitment, decision, document, pilot, follow-up, or another concrete action, and how direct to be.
- **Anything else:** Additional context, boundaries, history, or outcomes to land or avoid.

### Question format

Use compact labels so the user can answer quickly and the choices remain auditable. Put the recommended option first, while offering real alternatives. Avoid false either-or choices: if two actions can sensibly be combined, offer a combined option.

```markdown
1. What is the primary outcome?
   - **1a (recommended):** Diagnose their priorities and secure a concrete next step
   - **1b:** Build the relationship without making a direct ask
   - **1c:** Make a direct proposal and seek a decision

2. What should the conversation avoid?
   - **2a (recommended):** Avoid anchoring on a solution before understanding their constraints
   - **2b:** Avoid being too cautious; make the case clearly
   - **2c:** Avoid discussing a sensitive topic unless they raise it

3. Is there anything else to land or avoid?
   - **3a:** Nothing to add
   - **3b:** I will add notes or constraints
   - **3c:** Help me identify the key risk first

Reply with the labels, for example: 1b, 2a, 3c.
```

Ask as many questions as genuinely shape the meeting, without padding. If there are more questions than can be presented clearly at once, use two rounds. Ask questions that determine later options first, then adapt the second round based on the user’s answers. Keep labels sequential across rounds.

Before sending, check that every question is numbered, every option has exactly one unique label, labels are sequential, and the catch-all question is present.

Do not create the final page until the user has answered the questions or explicitly instructed you to proceed without them.

## 6. Create the meeting-preparation page

Create one page per meeting in the user’s chosen workspace. Set the date as a date-only value unless the workspace explicitly requires a date-time. Use a clear title such as the date followed by the participant name or meeting topic.

Include attendee names only if doing so is appropriate for the workspace’s access model and the participants’ privacy expectations. Verify that the saved page has the correct title, date, destination, access settings, and readable formatting.

Use this structure:

```markdown
# [Date] [Participant or meeting topic]

## Context

- Who they are and relevant organization context
- Relationship history and previous commitments
- Why this meeting is happening now
- Relevant public or authorized internal links
- Timely context worth mentioning

## Goal

[A concise statement of the desired meeting outcome, reflecting the user’s answers.]

## Agenda

### 0–5 min: Open and frame

**Say**

[A natural opening that establishes purpose and tone.]

**Interviewer note**

[What to avoid assuming or overexplaining.]

### [Next segment]: Diagnose the key issue

**Questions**

1. [A decision-relevant question.]
2. [A question that tests an important assumption.]

**Interviewer note**

[What evidence to listen for and what needs clarification.]

### [Next segment]: Explore, pressure-test, or present

**Say**

[A concise transition or framing statement.]

**Questions**

1. [A specific question tied to the proposal, decision, or opportunity.]

**Interviewer note**

[How to handle likely objections, tradeoffs, or uncertainty.]

### Final segment: Close and create momentum

**Question**

1. [A concrete question that secures a decision, owner, artifact, or dated next step.]

**Interviewer note**

[A lighter fallback close if a commitment is not possible today.]

## Five most important questions to ask

1. [Most decision-relevant question]
2. [Key diagnostic question]
3. [Question that tests the central assumption or gap]
4. [Question that reveals constraints, alternatives, or decision process]
5. [Concrete forcing-function close]

## Timely note

[Relevant publication, event, announcement, or professional context to mention if appropriate.]
```

### Agenda rules

- Fit stages to the actual meeting duration; do not create a long agenda for a short call.
- Put the most important issue before routine updates and background.
- Use level-three headings for agenda stages.
- Use **Say**, **Questions**, and **Interviewer note** labels consistently.
- Write spoken phrasing naturally, without quotation marks.
- Keep interviewer guidance compact and practical.
- Include named people, decisions, and concrete artifacts only when necessary and safe for the page’s audience.
- For a first meeting, state that explicitly. For recurring relationships, summarize the relationship arc rather than only the latest interaction.

### The five-question cheat sheet

The five questions are the user’s in-call reference. They must be ranked, concise, and decision-relevant. Do not turn them into five generic discovery prompts.

For a persuasion, recruiting, or negotiation meeting, include at least one question that exposes the relevant gap or decision criterion, one that establishes process, constraints, or alternatives, and one forcing close that identifies a specific next step, owner, date, or artifact.

For a purely diagnostic meeting, all five may be discovery questions, but they should still be ranked by usefulness.

## 7. Plan the post-meeting follow-up

For high-stakes meetings where the user is trying to influence a decision, secure commitment, recruit someone, sell an idea, or negotiate terms, schedule or propose a post-call review soon after the meeting if the user has authorized a suitable reminder or automation method.

The review should:

1. Retrieve only authorized meeting notes or transcripts.
2. Compare what happened with the intended goal and preparation plan.
3. Record commitments, objections, decision criteria, unresolved questions, and next steps.
4. Identify recurring communication patterns using dated evidence rather than vague impressions.
5. Create the next follow-up artifact and assign an owner and date where appropriate.

For purely informational meetings, do not force a persuasion-focused review. Instead, capture key facts, relationship updates, and agreed follow-up.

## 8. Final audit before completion

Before declaring the meeting prepared, check all of the following:

| Check | Pass condition |
|---|---|
| Scope | The correct meetings and date are covered. |
| Authorization | Research used only sources the user may legitimately access for this purpose. |
| Artifact review | Any relevant proposal, deck, memo, or draft was read in full, or its absence was surfaced to the user. |
| Strategy gate | A situation brief and targeted questions were completed when material choices existed. |
| Goal | The goal reflects the user’s answers rather than an unsupported assumption. |
| Agenda | Timing is realistic, stages serve the goal, and the close creates an appropriate next step. |
| Cheat sheet | Exactly five ranked, decision-relevant questions are included. |
| Privacy | The page excludes unnecessary sensitive details, compensation figures, and unrelated personal information. |
| Destination | The page is saved in the intended workspace with correct title, date, and access boundary. |
| Follow-up | A post-call review is planned when the meeting seeks to influence a consequential decision or commitment. |

## Common failure modes

### Researching people but not the subject matter

A participant biography does not replace reading the proposal, plan, analysis, or draft that prompted the meeting. When an artifact exists, read it and anchor the questions in its substance.

### Drafting before the user chooses the goal

A polished agenda can still be wrong if it assumes the user wants to sell, recruit, diagnose, or close. Present the situation, ask targeted questions, and wait for answers.

### Asking vague questions

“What should the agenda be?” shifts the work back to the user. Ask about outcome, stance, constraints, failure modes, and the desired ask.

### Treating every meeting as the same type

A relationship-building conversation, a decision meeting, and a negotiation need different briefs, agendas, and closes. Select the shape that matches the meeting.

### Overloading a shared page with sensitive details

Meeting pages often have wider access than source communications or records. Omit compensation figures, private assessments, confidential background, and unnecessary personal details. Use neutral references when context is needed but detail is not appropriate.

### Ending without a forcing function

A friendly discussion without an owner, artifact, date, or explicit next decision can lose momentum. When appropriate, design a close that makes the next step concrete.

### Producing a chat summary but not the actual page

The page is the durable deliverable. Save it in the chosen workspace, verify it, and make it readily accessible to the user before the meeting.


---
name: capture-meeting-actions
description: Review authorized meeting records, identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require the user’s judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to turn every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose and safeguards

Use this workflow only for a legitimate work purpose and with clear authorization to access the selected meeting records and task system. Read only the minimum sources needed to establish commitments. Keep task notes within the intended access boundary, and omit unrelated personal, health, family, compensation, legal, or other sensitive details unless they are necessary for the task and appropriate for everyone who can access it.

Before each run, apply these operating rules:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same counterparty or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.
- **Track commitments, not discussion.** An idea, interest statement, open question, or request from another person is not a task unless the user accepted responsibility for a concrete outcome.
- **Respect responsibility boundaries.** Attendance does not make the user responsible for all work discussed. Apply known role ownership and delegation rules supplied by the user or organization.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries commonly misattribute actions in recurring one-to-ones, brainstorms, interviews, and meetings where several attendees list their own to-dos. Never create a task solely because a summary labels something as an action item. Verify the owner in the transcript or reliable notes.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied list of meeting records.

If no scope is supplied, use this default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect only the information needed for triage:

- Title, date, and time
- Meeting-record link or identifier
- Attendees and relationship context, if available
- Transcript, notes, summary, and relevant linked context

Report a compact count before processing. Do not infer commitments from a title, attendee list, or agenda alone.

## 2. Fetch and inspect complete records

Fetch complete meeting records in parallel where the selected system supports batching. Do not search for existing tasks yet: first identify candidate commitments, counterparties, and topics so that deduplication is accurate.

For long transcripts, use a repeatable search, extraction, or chunking method rather than relying on a truncated preview. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by clear acceptance

Review automated action-item sections as leads, then inspect the surrounding conversation. A proposed action may have been conditional, assigned to another attendee, completed live, or described as a possibility rather than a promise.

When a transcript cannot be accessed, reduce confidence. Use written notes only when their author and reliability are known. If ownership remains unclear, ask a question rather than creating a task from an uncertain inference.

## 3. Triage each meeting

Classify each meeting loosely. Classification gives a starting expectation, not a rule that overrides direct evidence.

| Meeting type | Usual outcome | Guidance |
|---|---:|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or explicitly timed follow-up. |
| Information-gathering, interview, or reference call | 0 tasks | Create work only for an explicit out-of-meeting commitment by the user. |
| Internal planning or team meeting | 0–1 user-owned task | Capture the user’s deliverable, not the full team action list. |
| Coaching or recurring one-to-one | 0–1 task | Usually create a task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1–2 tasks | Often separate an internal decision from an external response. |

For every meeting, identify:

- Who attended and the relevant relationship context
- Candidate actions owned by the user
- Work completed during the meeting
- Work delegated to another named owner or role
- Explicit future commitments and timing
- Enough neutral context for a task to remain understandable weeks later
- Source and related links that are appropriate to include in the task system

### Skip signals

Produce no task when any of these conditions apply:

- The work was completed during the meeting. For example, a promised document was actually shared, drafted, or sent live.
- Another person or role owns the action, and no follow-up from the user is needed.
- The meeting was informational and any needed synthesis is already captured in the meeting record.
- An active task already covers the same outcome.
- The statement was exploratory, conditional, or did not establish an owner.

A brief retained note may be useful for relationship continuity, but do not place unnecessary sensitive context in a broadly visible task system.

## 4. Decide the task shape

Combine actions into one task when they share the same counterparty, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can be one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect several months later.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line or unrealistic time estimate.

This is a readiness gate. Do not create a task until each proposed task has:

1. A clear owner.
2. Evidence of an unfinished commitment or necessary follow-up.
3. A defined outcome.
4. A sensible scope and time horizon.
5. Enough context to stand alone later.

## 5. Write the task

Use the user’s chosen task system and field names. At minimum, capture:

- **Title:** short, verb-led, and specific.
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user’s scale; default to important routine work and reserve the highest level for a real deadline, material risk, or a waiting counterparty.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and source links.

Examples of useful titles:

- “Follow up with prospective partner about pilot scope”
- “Send setup guide to team member”
- “Reconnect with advisor after agreed milestone”

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: the agreed date, or a reasonable reminder date before it.
- Weekly or sprint commitment: the next relevant review or planning session.
- Flexible work: roughly one week, adjusted to workload and commitment strength.
- Older meetings processed late: move an immediate follow-up to the next workable date rather than assigning an already-passed date, unless the original deadline still applies.

Do not raise priority merely because task capture happened late. Raise it only when the underlying commitment has a meaningful deadline or external consequence.

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

Write context so it remains understandable later. Prefer absolute dates over phrases such as “tomorrow” or “recently.” Include only links that recipients of the task can appropriately access.

If the task is to send a message, include a ready-to-send draft rather than merely writing “email them.” Follow the user’s stated communication preferences. If none are known, use concise, warm, professional language with a clear request or promised deliverable. Avoid filler, unnecessary claims of urgency, and overly detailed meeting recap.

For introductions, use double opt-in: ask each relevant person for permission before connecting them. Do not disclose one person’s contact details, interest, or sensitive context to another without appropriate consent.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by meeting link or identifier, counterparty, distinctive topic terms, and proposed title.

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. If a match exists:

- Skip the new task when the existing task already captures the needed work.
- Update the existing task when the meeting adds a meaningful action, deadline, or useful context.
- Ask a batched question when it is unclear whether the new action is separate or should be merged.

Record the duplicate decision so it can be reported clearly.

## 7. Create confident tasks

Create all high-confidence tasks in a batch when the task system supports it. If the environment supports opening created records, open them in the chosen task system rather than filling the status update with management links.

For every skipped meeting, give a brief reason, such as:

- “No out-of-meeting commitment.”
- “Completed during the meeting.”
- “Owned by another role.”
- “Already covered by an active task.”

Do not create low-confidence tasks just to make the sweep appear complete.

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

Wait for answers before creating uncertain tasks. After answers arrive, create or update the remaining tasks and rerun the duplicate check if the answer changed the proposed outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, capture lessons that genuinely improve future runs. Keep reusable workflow guidance separate from individual task records.

- Add a short generalized example to a meeting-pattern reference when a recurring pattern affects triage, such as a common attribution error, a reliable sign of live completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a genuinely new required step.
- Record a new delegation boundary in the user’s or organization’s maintained responsibility reference when it applies beyond one meeting.

Do not turn one-off facts about individuals into permanent rules. Small additions to an examples or patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing a step or changing the evidence order.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links to an appropriate source record when available.
- Message drafts are ready to send and respect user preferences and privacy boundaries.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report only the essential outcome: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and any reusable guidance changes. Keep status updates terse and factual.


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
description: Create or improve a short, paid, asynchronous work sample that produces role-relevant evidence, can be reviewed consistently, and is validated through simulated submissions before release.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A strong work sample gives candidates a bounded, realistic version of important role work and gives reviewers useful evidence about role-relevant capabilities.

Use this for a new work sample or a revision of an existing one. Do not use it for interview questions, application-form screeners, live assessment centers, or multi-day work trials. If the requested format is unclear, ask one question before proceeding.

## Purpose and design principles

A work sample commonly sits after initial application review and before later interviews. It should answer a narrow question: can the candidate demonstrate important observable parts of this role under realistic constraints?

It is not a substitute for the rest of hiring. A short asynchronous exercise is poorly suited to assessing every important quality. For example:

- Interviews can assess live communication, motivation, collaborative reasoning, and responses to follow-up questions.
- References can provide evidence about reliability, integrity, and sustained performance.
- A later work trial can assess consistency, judgment over time, and performance in real systems.
- Training can often close gaps in a specific tool, internal process, or unfamiliar domain vocabulary.

Focus the work sample on three to five load-bearing capabilities that are important for the role and observable within the available time. Examples include prioritization, practical judgment, clear writing, diagnosis, execution, systems thinking, sourcing, stakeholder communication, or turning ambiguity into useful action.

Use these defaults unless the hiring owner chooses otherwise:

- Make the exercise paid.
- Set a clear expected time limit, commonly two to four hours.
- Use a self-contained scenario that requires no access to internal tools, private records, or unavailable systems.
- Keep reviewer time to roughly 20 to 25 minutes per submission.
- Use realistic but fictionalized or safely anonymized scenario details unless approved public facts are necessary.
- Do not ask candidates to create production work that the organization will use unless that use is explicitly agreed separately.
- State the policy on AI tools clearly. Assess judgment and usefulness rather than trying to infer AI use from prose style.
- Test only capabilities that materially relate to the role. Do not use protected characteristics, irrelevant preferences, or indirect proxies as criteria.
- Provide a route for reasonable accommodations or an equivalent accessible format while preserving the role-relevant standard.

## Step 1: Pre-flight

Before designing anything, confirm that the hiring team has both:

1. A current job description or role brief covering responsibilities, level, expected outcomes, and reporting context.
2. A role-success profile, hiring plan, or equivalent document identifying the capabilities and experience needed for the role's outcomes.

If either source is missing, stop. Do not try to determine the role-success profile while writing the exercise. That creates a moving target and often leads to a plausible task that assesses the wrong work.

Use this request format:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

When the materials exist, read the full relevant context. This may include project notes, team constraints, examples of strong work, prior hiring feedback, and existing work samples for comparable roles. Review one or two reference exercises only to calibrate tone, length, and delivery format. Do not copy a familiar task shape automatically. The work sample should follow the role, not precedent.

If reviewing internal communications or records, have a legitimate hiring purpose and clear authorization. Use only the minimum relevant materials. Omit unrelated personal information and sensitive details. Respect consent and privacy expectations, and keep notes, simulations, reviewer guidance, and outputs within the approved hiring access boundary.

After review, provide a concise status update, for example:

> Read the role brief, success profile, and two comparable work samples. Moving to the alignment memo.

## Step 2: Write an alignment memo before drafting

Do not write candidate-facing instructions yet. First create a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five capabilities that the role succeeds or fails on and that can be surfaced during the exercise window. Describe observable behavior rather than broad traits.

Weak:

> Strategic thinking.

Better:

> Identifies the highest-leverage problem in a messy operating situation, explains the key tradeoff, and produces a useful first action.

### What the work sample will not test

Name important criteria that belong in other stages. This keeps the test honest and prevents it from expanding into an unrealistic proxy for the whole job.

A three-hour written exercise may not fairly test long-term reliability, leadership over months, live collaboration, specialized software fluency, or performance in a fast-changing internal environment.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level. Explain how that changes the task.

- Entry-level candidates may need more context and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make tradeoffs, establish direction, and create an artifact another person could use without extra explanation.

### Failure modes to catch

Identify two or three role-misaligned work patterns that could otherwise look strong in ordinary screening. Describe work evidence, not personality labels or identity-based assumptions.

Examples:

- A polished planner who does not produce usable work.
- A fast executor who misses the central issue or creates avoidable risk.
- A careful candidate who defers every meaningful decision.
- A technically capable candidate who cannot communicate for the intended audience.

### What strong looks like

Write one short paragraph describing a high-quality submission. Explain what it notices, what choices it makes, what it produces, and how it handles uncertainty.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the hiring owner explicitly confirms or revises the memo.

## Step 3: Propose work-sample shapes

After the memo is approved, propose three possible exercise shapes. Each option must:

- Test the approved capabilities in a meaningfully different way.
- Be understandable within about one minute.
- Be self-contained.
- Be feasible within the stated candidate time limit.
- Produce evidence a reviewer can assess quickly and consistently.

For each option, provide:

- **Shape:** A plain-language description of the task.
- **What it tests:** The approved capabilities it is designed to reveal.
- **Why it is evaluable:** What evidence the reviewer will see and why reviewers can assess it consistently.
- **Main risk:** The most likely source of noise, unfairness, or weak diagnostic value.

Useful shapes include:

- **Triage pile:** The candidate receives a realistic set of messages, requests, and constraints. They prioritize, draft responses or work products, and recommend one systemic improvement. This suits operations, coordination, support, and communication-heavy roles.
- **Choose the highest-leverage action and ship it:** The candidate receives several possible priorities, selects one, explains the tradeoff, and creates a small usable output. This suits strategic operations and builder roles.
- **Diagnose and fix:** The candidate reviews a messy situation, identifies the central problem, and delivers one targeted intervention. This suits product, program, analytical, and process-improvement roles.
- **Source and pitch:** The candidate defines a target profile, identifies promising channels or prospects using supplied information, and drafts outreach. This suits recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** The candidate assesses a supplied intervention area or decision and makes a recommendation for a decision-maker. This suits research, policy, strategy, and specialist roles.
- **Design a repeatable system:** The candidate creates a lightweight process, playbook, or operating artifact that another teammate could use. This suits program, community, enablement, and operations-design roles.

Do not draft the full exercise until the hiring owner chooses a shape. If none fits, propose three more that follow the approved capabilities.

## Step 4: Draft version 1

Use the following candidate-facing structure. Adapt it to the selected shape and the organization’s hiring system.

## [Role] Work Sample

This work sample assesses your ability to [two or three observable role-relevant capabilities].

You have **[time limit]** total.

**Your mission**

[Describe a specific situation rather than an abstract assignment. Give enough context for realistic judgment. If decisiveness is being assessed, state which stakeholders are unavailable during the exercise, so candidates must make reasonable decisions rather than defer every call. End by restating what the candidate will produce.]

**Deliverables**

- **Part 1: [Analysis or prioritization].** [Expected output and optional rough time guidance.]
- **Part 2: [Shipped work].** [Actual drafts, decisions, or artifacts to produce. If planning and execution both matter, remind candidates not to spend all their time planning.]
- **Part 3: [Systemic improvement or reusable artifact].** [A usable output that a teammate could apply without further explanation.]

Use two to four meaningful deliverables. Avoid many micro-tasks. A small number of substantive outputs usually provides better evidence than dozens of shallow decisions.

**Context**

[Provide the minimum information needed: project or program state, audience, constraints, available resources, relevant policies, and stakeholder availability. Use invented names, domains, and identifiers for fictional scenarios.]

For a triage-pile exercise, include roughly eight to ten realistic items. Ensure several connect, so candidates are rewarded for spotting patterns across the situation rather than merely processing volume. Include reference notes with the information needed to make fair decisions, such as escalation rules, capacity limits, or refund policy.

If the scenario contains message headers or other multi-line metadata, use the soft-break method supported by the destination system so each field remains readable after pasting. Do not include real contact details, direct contact channels, account identifiers, or information drawn from private communications unless it is necessary, authorized, and appropriately minimized.

**Instructions**

- Spend **[time limit]** completing this work sample.
- Submit within **[submission period]** of receiving the invitation.
- Submit a single [document or PDF] covering your work. If you create supplementary materials, include accessible links through the approved submission process.
- **This is a paid work sample.** We will pay [base payment] after submission. [If applicable: We also offer an early-submission payment or bonus for work submitted within the stated period.]
- You may use AI tools. Use them carefully and apply your own judgment. We are evaluating your choices, reasoning, and the usefulness of your work. Briefly note any material use of AI tools.
- Demonstrate your strongest relevant judgment somewhere in the submission. Invest time strategically rather than trying to be comprehensive everywhere.
- [Optional] You may include a short, informal walkthrough video explaining your choices. Do not spend significant time polishing it.
- If you need an accommodation or an accessible alternative format, use the organization’s approved hiring contact or process.

**Anticipated questions**

- *I am unclear about a requirement. What should I do?* Make a reasonable assumption, state it briefly, and continue.
- *What if I do not finish within the expected time?* Submit what you have. Include a short note on where you got to and what you would do next.
- *How will my work be used?* It will be used only to evaluate candidates for this role unless another use is agreed with you separately.

After every draft, add a separate internal section:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets on choices the owner may want to change. Typical notes include:

- Whether a scenario item is too obvious or too ambiguous.
- Whether the task reflects a real role constraint.
- Whether the payment and deadline match role level and expected effort.
- Whether a deliverable is overly prescriptive or too open-ended.
- Whether an optional video adds useful evidence.
- Whether the scenario requires more reference information to be fair.

End with one focused decision question, such as:

> Which part should we tighten first?

## Payment and timing choices

Choose compensation deliberately based on expected time, role seniority, labor-market context, and local legal requirements. State the base payment, payment method, timing, and any bonus terms plainly. Do not make payment contingent on hiring or quality judgments.

If offering an early-submission incentive, ensure it does not undermine accessibility or create unreasonable pressure. Candidates should still have a clear standard deadline and access to an accommodation process. The organization should confirm that payment practices comply with applicable law and internal policy.

## Candidate-facing format and style checks

Write in direct, plain English and use the locale appropriate to the organization. Make the instructions easy to paste into the chosen applicant-tracking system or document format.

Before sharing a draft, confirm that candidate-facing text:

- Uses headings and bullets that render correctly in the destination system.
- Avoids tables and horizontal divider lines when the destination system handles them poorly.
- Avoids generic slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.
- Uses clear deadline phrasing, such as “by the end of Tuesday,” rather than abbreviated wording.
- Uses invented names, domains, and identifiers in fictional scenarios.
- Uses the destination system’s supported soft-break method for multi-line message metadata when ordinary line breaks collapse.
- Contains no credentials, private contact details, sensitive internal data, or information unrelated to the candidate’s task.
- States accessibility and accommodation options through an approved process.

## Step 5: Iterate with the hiring owner

Expect multiple rounds of feedback. For every revision, provide the complete updated work sample, not merely a change list, so the owner can copy and paste it into the chosen system.

Apply feedback directly unless it would materially weaken assessment validity, fairness, privacy, or safety. If so, state the concern once in plain language, offer a practical alternative, and let the accountable hiring owner decide.

Common revision requests include tightening vague instructions, loosening overly prescriptive tasks, correcting scenario facts, simplifying deliverables, changing payment, adjusting deadline language, and removing details that create unnecessary production burden.

## Step 6: Simulate two submissions

Before declaring version 1 complete, simulate two complete candidate submissions using the exact candidate-facing instructions and stated time limit.

### Role-aligned simulation

Use a persona based on the approved role-success profile. Have the simulated candidate complete the actual deliverables, then add a short reflection on choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest, capable simulated candidate who could pass ordinary screening but whose work lacks a capability central to this role. Select a mismatch grounded in job evidence, such as a planner where the role needs a builder, a cautious candidate where the role requires timely decisions, or an executor who cannot identify systemic patterns. Never base the contrast on identity, background, protected characteristics, or subjective cultural similarity.

Have this simulated candidate produce the same deliverables.

Then produce a synthesis covering:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both submissions looked similar.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by expected impact.

A capability both candidates demonstrate may be a useful floor check. The main concern is when a central capability fails to create different, reviewable evidence.

## Step 7: Apply validation improvements

Revise the full work sample based on the simulation. Improve the weakest diagnostic points first.

Useful changes may include:

- Connecting scenario items so candidates must recognize relationships.
- Removing obvious noise that takes seconds to dismiss.
- Adding a concrete constraint that forces a meaningful tradeoff.
- Replacing a broad opinion prompt with a usable deliverable.
- Clarifying what evidence reviewers should value.
- Removing specialized knowledge requirements that are trainable and not needed immediately in the role.

Do not make the test harder simply to make it more selective. Make it more diagnostic of the approved capabilities.

## Step 8: Optional external review

If other reviewers provide feedback, evaluate each suggestion against the approved alignment memo. State which suggestions to integrate, which to skip, and why. External feedback is evidence rather than an automatic instruction. The hiring owner remains accountable for the assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The role description and role-success profile are confirmed.
- The alignment memo is approved.
- The selected exercise shape maps directly to the load-bearing capabilities.
- The task fits the stated time limit for a qualified candidate.
- The scenario is self-contained and requires no private access.
- Payment, submission, AI-use, and accommodation instructions are clear.
- Candidate-facing text works in the destination system.
- A reviewer can evaluate a submission in roughly 20 to 25 minutes.
- The role-aligned and plausible role-misaligned simulations are complete.
- Simulation findings led to necessary revisions.
- The task does not create unpaid production work or expose sensitive information.
- Review criteria are tied to role-relevant evidence and have been checked for irrelevant proxies.

## Common failure modes

Avoid these patterns:

- Designing the exercise before agreeing what it should measure.
- Testing tool familiarity, domain trivia, or easily trainable knowledge instead of durable role-relevant judgment.
- Asking for too many small outputs instead of a few meaningful ones.
- Making every scenario item independent, which tests volume but not pattern recognition.
- Allowing candidates to defer every decision to an available stakeholder when decisiveness is meant to matter.
- Giving insufficient context and rewarding insider knowledge.
- Setting word-count targets that encourage padding.
- Creating a test that takes longer to review than the signal justifies.
- Treating polished writing or presentation as the main signal when the role needs another capability.
- Using a scenario that resembles real confidential work too closely.
- Declaring success without checking whether the exercise distinguishes relevant performance.

## Maintain the workflow

After each completed design cycle, record general lessons in the team’s approved assessment-design documentation. Capture reusable findings such as rendering constraints, effective task shapes, simulation discoveries, payment-policy changes, or clearer template wording.

Make small documentation updates directly. Seek approval before changing core safeguards, such as the pre-flight requirement, the alignment-memo gate, the simulation requirement, privacy boundaries, or the accommodation process.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, respectful of candidate time, and clear about what evidence strong performance produces.


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
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account and privacy context, verifying rendered page state, and separating preparation from consequential actions.
---

# Use a browser safely

Use this workflow for tasks that need real website interaction: completing forms, changing settings, collecting information from rendered pages, testing a flow, uploading material, or working in an authenticated dashboard. Use it when a simple retrieval or an authorized direct interface cannot reliably complete the requested work.

The central rule is:

> Inspect before editing, read back every meaningful change, and do not take a consequential final action until the account, target, page state, and authorization are clear.

An automation command that reports success does not prove the site accepted the change. Modern applications may maintain state separately from the visible page, commit values only when focus changes, replace controls during a re-render, or display an error after an action has already completed.

## 1. Establish purpose, authority, and scope

Before accessing the site, identify the exact outcome and boundary of the request.

Ask or determine:

- What page, record, form, setting, or workflow is in scope?
- What information must be entered, collected, changed, uploaded, or downloaded?
- Is there a legitimate purpose and clear authorization for the relevant account and information?
- What is the minimum relevant information needed?
- Which choices require the user's judgment?
- Is the final action reversible, or does it send, publish, pay, delete, grant access, change billing, alter security, or create another external commitment?

When private communications, records, or information about people are involved, use only the minimum relevant sources and details. Do not place unrelated personal information in logs, screenshots, downloads, summaries, or output. Keep results within the authorized audience and do not expose credentials, session material, recovery details, or security-sensitive account information.

If the intended target, account, environment, authority, or outcome is unclear, stop before changing data. A useful pre-action question is:

> Which account and environment am I using, what exact item will change, and what result is expected?

## 2. Choose the least invasive route

Use the first suitable route in this order:

1. **Authorized direct interface.** Prefer a supported API, export, integration, or documented programmatic operation when it can safely complete the task.
2. **Headless browser automation.** Use it for public pages, test environments, ordinary rendered-page collection, screenshots, UI testing, and tasks that do not need an existing signed-in identity.
3. **User-visible authenticated browser session.** Use it only when an existing session, single sign-on state, account-specific dashboard, or user-directed browser context is truly required.

Before browser automation, look for a direct route through official documentation, normal form actions, page source, or visible ordinary network requests. Do not use an undocumented route to bypass access controls, paywalls, consent boundaries, terms, security controls, or anti-abuse protections.

If automated browsing is blocked, do not try to evade the protection for research or routine collection. A verified visible session can be appropriate only for a legitimate task the user explicitly requested, where the user has authorized access and the established session is necessary. Do not use a live authenticated browser merely for convenience: it can interrupt the user's work and increases privacy and account risk.

## 3. Protect authenticated browser context

When a live browser session is needed, announce the takeover and purpose before interacting. For example: “I am taking over the browser to update the requested account setting.” This informs the user without adding an unnecessary approval step for ordinary navigation.

Use a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing page to use. Do not take over unrelated tabs.

Classify the context before opening the real target. Common contexts include personal, organizational, test, staging, production, or another explicitly authorized environment. Then select the browser profile or connection that matches that context.

Do not infer account identity from a generic browser name, remembered default, window title, tab title, or connection nickname. Verify the signed-in account through a reliable account indicator before making changes. Also verify the organization, tenant, or environment when applicable.

If the automation setup uses a verification gate, marker, or permission state, enable it only after the account check has passed. Never create such a marker merely to unlock actions.

Additional safeguards:

- Do not disable warnings, multi-factor authentication, access controls, or browser security features.
- Do not trigger unexpected script dialogs or disruptive browser actions.
- Do not close or restart a user's browser without explicit approval, especially if it may discard their work.
- Keep authenticated screenshots, downloads, and extracted data within the authorized access boundary.
- If the correct account cannot be verified, stop and ask rather than guessing.

## 4. Separate preparation from commitment

Treat reversible setup and consequential actions as separate phases.

### Preparation pass

1. Navigate to the verified target.
2. Inspect the current state and relevant controls.
3. Select options and enter values.
4. Read back and verify every meaningful change.
5. Capture a pre-action record when the outcome is consequential.
6. Do not activate the final control.

### Commitment pass

After explicit confirmation when required:

1. Re-check account, environment, target, and final values.
2. Confirm that a reload, re-render, or session change has not altered the prepared state.
3. Perform the final action once.
4. Verify completion using reliable evidence.

Explicit confirmation immediately before commitment is normally required for sending messages, publishing, submitting official forms, purchasing, paying, deleting, changing plans, changing access or ownership, and actions described as final or not editable after submission.

For a low-risk reversible change the user directly requested, such as updating a draft or preference, proceed after normal verification unless the site presents an unexpected warning or broader effect.

A confirmation request should be concise: name the target, important values, recipients or audience, cost if any, irreversible effects, and remaining questions.

## 5. Inspect the rendered page before editing

Do not begin by guessing selectors, filling controls by numerical position, or relying only on visual appearance. Inspect the rendered page and current record first.

For each relevant control, determine:

- Its type: single-line input, multiline area, rich-text editor, dropdown, checkbox, radio group, date/time picker, upload control, or custom widget.
- Its stable identity: accessible name, visible label, placeholder, or explicit label relationship.
- Current value, required state, disabled state, validation rules, and formatting limits.
- Whether it is the real editable control, a wrapper, or a hidden synchronization field.
- Whether changing it or a related selection causes a re-render.

Address controls by semantic identity, such as label text or an accessible-name relationship. Do not use DOM position when a stable label is available; dynamic applications can reorder or replace fields after loading.

A generic inspection record should capture at least the element tag, input type, role, label, required status, and current value or text length. Save a structured before-state when it will help review, recovery, or verification. For sensitive content, record lengths or redacted summaries rather than full values.

## 6. Match the interaction to the control

A generic “set value” command is not reliable for every kind of web control.

| Control | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use normal text entry. | Line breaks or unsupported characters may be removed. |
| Multiline area | Enter text, then move focus away. | Some sites commit only after blur. |
| Rich-text editor | Focus the actual editable node, replace content through keyboard-style input, then blur. | Direct DOM changes may not update internal application state. |
| Dropdown or combobox | Select by visible option text and wait for the page to settle. | The selection may refresh dependent controls. |
| Checkbox or radio group | Read the existing state and change only if needed. | Clicking an already-correct control can reverse it. |
| Date/time picker | Set the value and verify the rendered summary. | Popovers can reinterpret typing or clear related values. |
| Upload control | Confirm file, destination, and privacy implications first. | Uploading may begin immediately or be difficult to undo. |

For a framework-driven editor, simulate ordinary user behavior: focus the true editable element, select existing content, delete it, enter the replacement through keyboard-style events, move focus to a neutral element, wait briefly, then read the result back.

Some pages pair a visible editor with a hidden input. Changing the hidden field may look successful in an inspection but still fail validation. Target the visible interactive control that the application actually uses. If an accessibility locator returns a wrapper rather than an editor, inspect the label relationship and locate the editable descendant.

If dropdowns, checkboxes, dates, or tabs can trigger a refresh, make and verify those selections before entering long text. Re-inspect afterwards and confirm earlier values survived.

## 7. Verify every meaningful edit

After each field fill or setting change, read the resulting state from the page and compare it with the intended value. For sensitive text, compare length, required state, a redacted digest, or a minimal summary instead of reproducing the content in output.

Stop and diagnose if:

- The automation reports success but the field is empty.
- Text lost line breaks, spaces, punctuation, or characters.
- A value was truncated by a single-line field or length limit.
- A custom editor visibly changed but did not retain its value.
- A later action erased an earlier value after a re-render.
- A hidden field changed while the actual editor remained empty.
- A selection unexpectedly changed a recipient, date, dependent field, or validation rule.

Retry once with a more appropriate interaction method, then verify again. If the page continues to reject or alter the content, report the limitation and ask how to proceed. Do not silently submit an incorrect result.

## 8. Apply a pre-action readiness gate

Before submitting or applying a high-impact change, inspect the relevant page state again. Confirm all of the following:

- The account, organization, environment, and target item are correct.
- Required fields are present and non-empty.
- Entered values match the intended content closely enough for the task.
- Recipients, attachments, dates, options, and dependent values are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If an important value cannot be verified, a required field is blank, or the target is uncertain, refuse to submit. A partially prepared page is usually recoverable; an incorrect external action may not be.

For consequential tasks, capture a pre-action screenshot, concise state summary, or structured field record. Share it only through the appropriate access boundary. Avoid pasting a large table of sensitive values into chat when a short summary and securely available record are sufficient.

## 9. Verify completion without creating duplicates

A click is not proof of completion. Look for persistent evidence such as a confirmation reference, a saved setting that remains after a safe refresh, a new record, a sent or published item, or an updated status.

If the site reports an error, inspect the resulting state before retrying. An error may be cosmetic, while blind retries can create duplicate messages, submissions, payments, or records. If completion cannot be verified, state what was attempted, what evidence exists, and what remains uncertain.

## 10. Recovery guide and final audit

| Symptom | Safe response |
|---|---|
| A field appears blank after a successful automation call. | Use normal focus-and-keyboard entry, blur, and read back. |
| Earlier values disappear after a later edit. | Commit and verify each value; perform re-rendering selections first. |
| Text formatting changes unexpectedly. | Find the appropriate multiline or editor control, or obtain approval for a simplified format. |
| A locator identifies a wrapper or hidden field. | Inspect labeled descendants and target the real interactive control. |
| The browser method is unstable or differs from the site’s ordinary behavior. | Prefer an authorized direct interface or an approved verified session; do not attempt to defeat protections. |
| A popup or error may have changed state unexpectedly. | Close it through a neutral action when possible, inspect resulting state, and do not retry blindly. |
| Account or environment is uncertain. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

Before reporting completion, confirm:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only minimum relevant private information was accessed and retained.
- [ ] Account, environment, and target were verified.
- [ ] Controls were inspected before editing.
- [ ] Meaningful changes were read back and verified.
- [ ] Required fields and validation passed the readiness gate.
- [ ] A pre-action record and explicit confirmation were used when the action was consequential.
- [ ] Completion was verified, and uncertainty is clearly distinguished from confirmed results.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: A complete workflow for designing, testing, improving, and packaging a reusable AI skill from a new idea, an existing draft, or a repeated workflow captured from a conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing one, assess whether it works, or improve when it triggers. A skill is a focused set of instructions and optional supporting resources that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the job and its boundaries.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Let a person review representative outputs and measure objective requirements where appropriate.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and not overfitted to the tests.
7. Optionally improve the skill description so it triggers for the right requests.

Do not assume every project needs every step. A user may want a quick draft, a collaborative “good enough” pass, or a rigorous benchmark. Identify where they are in the loop and help them move forward from there.

## Communication principles

Match the user’s technical vocabulary and experience. Use plain language by default. Terms such as *evaluation* or *benchmark* may be useful, but briefly explain them when needed. Avoid unexplained terms such as “schema,” “assertion,” or “JSON” unless the user is comfortable with them.

When asking questions, explain why the answer matters. For example, instead of asking only “What is the output format?”, say: “What should a successful result look like—an answer in chat, a structured report, a file, or an action? This determines how we test completion.”

Keep the user involved at decision points:

- Confirm the intended job before writing extensive instructions.
- Ask before choosing a restrictive scope, tool requirement, or approval policy.
- Share proposed test cases before relying on them.
- Let human judgment lead for subjective quality such as tone, visual design, or creative usefulness.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea such as “I need a skill that helps with recurring project status reports.” Start with discovery and a first draft.

### B. Existing draft or installed skill

The user already has instructions and wants them edited, simplified, tested, or optimized. Preserve the established skill identity unless the user explicitly asks to rename it. Read the current instructions before proposing changes.

### C. Workflow already demonstrated in the conversation

The user may say “turn what we just did into a skill.” Extract as much as possible from the conversation before asking questions:

- Inputs the user supplied.
- Tools or information sources used.
- The order of decisions and actions.
- Corrections the user made.
- Output format and acceptance criteria.
- Conditions where the workflow changed direction.

Summarize the inferred workflow and list gaps for confirmation. Do not silently turn a one-time solution into a general rule without checking whether it applies broadly.

### D. Evaluation or optimization request

The user may already have a finished-looking skill and want to know whether it helps. Go directly to test design, evaluation, and revision. Do not rewrite it merely because a rewrite is possible.

## 2. Capture intent and scope

Before drafting, gather enough detail to define a coherent job. Use the following questions, adapting them to the user’s context.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Trigger:** What kinds of user requests, wording, or situations should activate it?
3. **Inputs:** What information, files, examples, systems, or permissions can it use?
4. **Outputs:** What should it produce or change? Is there a required format?
5. **Success:** How will the user know the output is correct or useful?
6. **Boundaries:** What should the skill explicitly not do? When should it ask a question, decline, or hand work back to the user?
7. **Variations:** What common cases, difficult cases, or exceptions matter?
8. **Dependencies:** Does the workflow require particular capabilities, reference material, templates, scripts, or user-provided access?
9. **Testing:** Should the skill be tested with example requests? Recommend testing when outputs can be checked objectively, when the workflow is consequential, or when the skill will be used repeatedly.

Do not ask every question mechanically. Start with the missing information that most affects the design. If useful, offer choices:

- “Should the skill make a best effort when information is missing, or stop and ask?”
- “Should it produce a concise summary, a detailed report, or let the user choose?”
- “Should it work with any data source, or only sources the user has approved?”

### Research before drafting

If the environment provides relevant documentation, similar skills, user-approved reference materials, or domain guidance, review them before drafting. Research should reduce burden on the user rather than replace their authority over requirements.

Use research to identify:

- Existing conventions or output standards.
- Constraints imposed by an available tool or file format.
- Reusable patterns from comparable tasks.
- Safety, privacy, compliance, or approval requirements.

If sources conflict or requirements are uncertain, present the uncertainty rather than guessing.

## 3. Choose the skill’s structure

A skill should be focused enough that users and the AI can predict what it does. One skill can support variants of the same job, but unrelated jobs should be separate skills when they have different audiences, permissions, sources of truth, or definitions of completion.

A typical skill package contains:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional documentation loaded when needed
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help decide when to activate the skill.
2. **Core instructions:** The workflow needed on most uses.
3. **Supporting resources:** Detailed references, templates, or scripts consulted only when relevant.

Keep the core instructions readable. If they become large, move domain-specific material into clearly named reference files and tell the AI exactly when to read each one. For large reference material, include a table of contents or navigation section.

Organize multi-variant skills by variant. For example, a deployment skill may have one core selection workflow plus separate references for different hosting environments. The AI should choose and read only the relevant variant instead of loading all material by default.

### Use scripts for repeatable deterministic work

If test runs show the AI repeatedly reconstructing the same helper procedure—such as file conversion, report generation, validation, or data cleanup—consider bundling a reusable script. A script is valuable when it is:

- Deterministic or easier to verify than natural-language reasoning.
- Reused across requests.
- Safer or less error-prone than repeated manual reconstruction.
- Clearly within the user’s intended permission scope.

Document what the script does, what inputs it accepts, expected outputs, and when not to use it. Do not bundle unnecessary automation merely because it is possible.

## 4. Write the skill

Draft the skill in clear, imperative language. Explain the reasoning behind important instructions, especially when a rule prevents a predictable failure. AI systems generally perform better when they understand the goal and tradeoff than when they receive a long list of unexplained prohibitions.

A useful skill normally includes the following sections as applicable.

## Purpose and scope

State the job, intended users, and boundaries. Make clear whether the skill creates an answer, produces a file, takes an action, or guides the user through a process.

## Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State what to do when a required item is absent.

Example:

```markdown
Before preparing the report, confirm the reporting period and approved data source.
If the source is unavailable, ask the user for an export or offer a draft marked as incomplete.
```

## Workflow

Give the normal sequence of actions. Include decision points rather than trying to enumerate every possible scenario.

A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Confirm unclear requirements only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result, assumptions, and unresolved limitations.

Use conditional rules where needed:

```markdown
If the request provides a required template, follow it.
If no template is provided, use the default report structure below.
If the user requests a change that could overwrite important work, describe the impact and request confirmation before proceeding.
```

## Output format

When consistency matters, define an exact or near-exact template. For example:

```markdown
# [Title]

## Summary
[One short paragraph]

## Findings
- [Finding with evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Any uncertainty]
```

Avoid rigid formatting when the task’s value depends on adapting to context. In that case, give goals and examples instead of a fixed shell.

## Quality and safety checks

State the checks needed before completion. Examples include confirming required fields, validating calculations, citing the source of key claims, preserving original data, or flagging uncertainty.

Skills must behave in ways the user would reasonably expect from their description. Do not design instructions that conceal actions, bypass authorization, extract confidential information, damage systems, or enable unauthorized access. If the requested task is unsafe, deceptive, or exceeds the available authority, explain the limitation and offer a safe alternative where possible.

## Failure behavior

Describe how to recover from common failures in general terms:

- Missing or conflicting input: identify the gap and ask a focused question.
- Unavailable tool or reference: explain what could not be verified and offer an alternate method.
- Ambiguous request: make a reasonable low-risk assumption when it will not materially affect the result; otherwise ask.
- Validation failure: do not present the output as complete; correct it, report the issue, or request guidance.
- Permission-sensitive action: pause for confirmation before an irreversible, external, or high-impact action.

## Examples

Include a small number of generalized examples only when they teach a distinct pattern. Examples should show the shape of a good response, not become a narrow substitute for reasoning.

## 5. Write a strong description

The skill description is primarily a routing instruction: it helps an AI decide whether the skill applies to a user request. It should state both **what the skill does** and **when to use it**.

Write descriptions that cover realistic user language, including requests that imply the job without naming it directly. AI systems may fail to activate a useful skill unless the description makes relevance clear.

A good description includes:

- The task or outcome.
- Common contexts or user phrasing that indicate the task.
- Important scope limits when they prevent harmful or costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a status update, leadership summary, progress report, milestone review, or a concise account of risks and next steps, even if they do not use the phrase “status report.”
```

Do not put the entire procedure in the description. Do not rely on vague labels such as “help with documents.” Do not make the description so broad that it captures nearby work better handled by another skill.

## 6. Review the draft before testing

Read the skill again as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description say when to activate it?
- Are required inputs, permissions, and outputs clear?
- Does the workflow explain why important checks matter?
- Are there unnecessary rules, repeated guidance, or brittle wording?
- Does it tell the AI what to do when information is missing?
- Does it avoid assuming a specific person’s tools, habits, access, or terminology?
- Would a capable AI have enough freedom to handle normal variation?

Prefer a lean, understandable prompt over a long prompt filled with rules that do not affect outcomes. Excessive “always” and “never” language is a warning sign unless the behavior is truly non-negotiable, such as a safety or authorization boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create a small evaluation set. Start with two or three realistic prompts that resemble genuine user requests. Show them to the user and invite additions or corrections.

For each test case, record:

- A descriptive identifier or name.
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
      "prompt": "Prepare a weekly summary from the attached updates. Flag information you cannot verify.",
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Use test cases that cover different meaningful situations:

- A typical successful request.
- A request with incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic edge case that changes the workflow.
- A request that should cause the skill to ask for approval or decline an unsafe action, when relevant.

Do not write tests that only mirror the wording of the skill. Vary phrasing, detail level, and user sophistication. Avoid one-off personal scenarios; test the general category of challenge instead.

## 8. Run comparisons

When the environment supports independent runs, compare the skill against a meaningful baseline.

- **For a new skill:** Run each test once with the skill and once without it.
- **For an existing skill:** Save an unchanged snapshot before editing, then compare the revised skill against the previous version.

Launch the skill and baseline runs under comparable conditions. If parallel execution is available, start both configurations for every test case at the same time. This reduces timing differences and prevents selectively changing the baseline later.

Store outputs in a clear iteration structure, for example:

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

For each run, preserve the prompt, supplied files, output, and available run metadata such as elapsed time and token or compute use. Record timing immediately when the execution environment reports it; some systems do not retain this information afterward.

If independent agents or parallel execution are unavailable, perform a transparent sanity check instead: follow the skill for each test prompt, save outputs, and ask the user to review them. Do not claim that this is a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs are underway, draft objective checks where they genuinely help. Explain the checks to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful. Examples:

- Required sections are present.
- A produced file opens and has the required fields.
- Calculated values match a known source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- Output contains citations or source references when required.

Each check should have a descriptive name, a pass/fail result, and evidence. Use a stable record shape such as:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section lists two unavailable data points and requests them."
    }
  ]
}
```

Use scripts for programmatic checks whenever practical. Automated checks are more repeatable than visual inspection and can be reused across iterations.

Do not force numerical checks onto subjective tasks. Writing quality, usefulness, tone, aesthetics, and strategic judgment often need human review. A weak proxy metric can make a skill optimize for the metric instead of the user’s real goal.

## 10. Review results with a human

Present both the outputs and the measurements. Use any available review interface that lets the user inspect each test case, compare configurations, and leave feedback. If no such interface exists, present results clearly in the conversation or as accessible files.

For each test case, show:

- The original prompt.
- Relevant supplied inputs.
- The skill output and the comparison output, if available.
- Objective grades and evidence.
- Timing or resource data, if available.
- A place for the user to state what worked and what should change.

Ask focused questions such as:

- “Which result would you trust in normal use, and why?”
- “Did the skill add steps or detail that were not valuable?”
- “What was missing, misleading, or hard to use?”
- “Would this work for similar requests with different wording or data?”

Empty feedback can indicate that a case is acceptable, but do not interpret it as proof that all cases are solved. Look at the output and measurement data too.

## 11. Analyze results beyond pass rates

Aggregate results across tests when possible: pass rate, average time, average resource use, and variation. Put the revised skill before the comparison condition in reports so comparison is easy to read.

Then perform an analyst pass. Aggregate numbers can conceal important patterns. Look for:

- **Non-discriminating checks:** A check passes for both the skill and baseline, so it does not measure the skill’s value.
- **High variance:** A result differs substantially between comparable runs, suggesting ambiguity, environmental instability, or an unreliable instruction.
- **Tradeoffs:** The skill may improve quality but add excessive time or resource use.
- **Failure concentration:** Several failures may share one root cause, such as unclear source selection or missing output rules.
- **Unproductive work:** Execution traces may show repeated planning, redundant research, or unnecessary formatting.
- **Repeated reconstruction:** Multiple runs independently create the same helper procedure, suggesting a bundled resource would help.

Do not treat a small benchmark as conclusive. Use it as evidence for the next revision.

## 12. Improve without overfitting

Base revisions on user feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from a complaint. For example, if one output omitted a required source note, do not merely add a rule that mentions the exact test scenario. Instead, clarify the broader condition: when evidence comes from incomplete or mixed sources, distinguish verified information from assumptions.

Use these improvement principles:

1. **Fix causes, not examples.** Design for many future requests, not only the current tests.
2. **Keep instructions lean.** Remove guidance that does not change behavior or causes wasted effort.
3. **Explain intent.** State why an action protects quality, usability, or safety.
4. **Add reusable assets only when justified.** Bundle scripts, templates, or references when repeated work proves their value.
5. **Preserve useful behavior.** Avoid changing a skill so broadly that it loses the parts users already value.
6. **Expand coverage gradually.** Add a new test when it represents a real class of failure, not every isolated incident.

After revision, rerun the full test set in a new iteration. Retest baselines using the same comparison policy. Show the new outputs alongside prior outputs where possible, then collect feedback again.

Stop when one or more of these conditions is true:

- The user says the skill is ready.
- User feedback is consistently positive or empty across meaningful cases.
- Objective requirements are reliably met.
- Further revisions are not producing meaningful improvement.
- Remaining weaknesses require missing information, unavailable capabilities, or a product decision rather than better instructions.

## 13. Optional blind comparison

For a more rigorous comparison of two skill versions, use blind review. Give an independent evaluator two outputs without identifying which came from which version. Ask it to judge against a shared rubric, then reveal the mapping only after the judgment is recorded.

Blind comparison is useful when:

- Two versions have similar pass rates but different qualitative quality.
- The author or user may be biased toward a newer version.
- A decision has material cost or importance.

Keep the comparison rubric tied to user value: correctness, completeness, clarity, adherence to constraints, safety, and practical usability. Analyze why the preferred output won before editing the skill again.

## 14. Optimize triggering behavior

Once the workflow itself is stable, evaluate the description that controls activation. Do this after, not before, the skill is otherwise useful.

Create a set of realistic trigger queries containing both cases that **should trigger** and nearby cases that **should not trigger**. Include roughly balanced coverage, with enough detail that using a skill would actually help.

Positive cases should vary in wording and context:

- Formal and casual phrasing.
- Requests that name the task directly and requests that imply it.
- Common use cases and less common but valid cases.
- Cases where another related skill might compete but this skill should be selected.

Negative cases should be difficult near-misses, not obviously irrelevant requests. They should share terms or concepts with the skill but belong to another job, require a different capability, or lack the conditions that make this skill appropriate.

Example format:

```json
[
  {
    "query": "I need a concise update for leadership from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what a project status report is and when teams use one?",
    "should_trigger": false
  }
]
```

Review this query set with the user before using it. Poor trigger tests produce misleading descriptions.

Evaluate candidate descriptions repeatedly if the environment supports it, because activation can vary. Separate queries used to improve the description from held-out queries used to select the final description. Choose the description that performs best on held-out cases, not merely the one that best fits the examples used during editing.

Remember that a simple request may not activate a specialized skill even when the description matches: an AI may handle an easy one-step task directly. Trigger tests should therefore describe substantive requests where consulting the skill would be useful.

When applying the selected description, show the user the before-and-after text and the evaluation results. Ensure the final description remains honest about the skill’s scope.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately describes activation conditions.
- Instructions do not depend on private local conventions, personal access, or undeclared tools.
- References and scripts are present, named clearly, and documented.
- No confidential data, credentials, identifiers, or sensitive examples are included.
- The user can understand how to install, access, or adapt the package in their chosen environment.
- Test material is included only if it is safe and useful to retain.

Provide a short handoff note explaining what the skill does, any required capabilities, known limitations, and how the user can test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, a description that routes appropriate requests, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for the user’s real recurring work.


---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using realistic content, screenshots, and programmatic layout checks before declaring the work complete.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, color, background, or typography edits: a local change can affect wrapping, height, overflow, alignment, and backgrounds elsewhere.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Real screenshots and numerical checks catch different failures, so require both.

## 1. Prepare realistic page states

Run the real interface in an appropriate test environment. Populate changed surfaces with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative cards, rows, lists, and item counts;
- validation messages and controls in their active states;
- loading, empty, and error states when the change can affect them.

Do not validate only an empty or unusually clean page. Sparse content often hides clipping, overlap, unexpected whitespace, and wrapping defects.

## 2. Select the viewport sweep

Test these baseline viewport widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages or interfaces intended for large displays.

When vertical layout matters, test at least two heights at every relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Include known target viewports when available. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable browser automation system selected for the project. Run it headlessly unless interactive inspection is specifically needed.

## 3. Capture and inspect screenshots

Capture real screenshots for every relevant viewport and state. Use full-page screenshots when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect the changed component and its immediate surroundings on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does it match the design intent now that the element's role or layout has changed?

Pay special attention to edge-to-edge or full-bleed changes. A component made flush with an edge can reveal previously hidden margins or wrapper padding as visible background strips. Check every edge, not only the edge edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. Adapt selectors and tolerances to the interface, but verify at least the following:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is intended to fit the viewport;
- no changed element overlaps neighboring content or escapes its intended container;
- buttons, links, inputs, and other controls remain visible, reachable, and usable;
- fixed or sticky UI does not cover essential content;
- cards, lists, and form controls remain within intended bounds;
- prose retains a readable line length.

For a fit-to-viewport screen, compare document height with viewport height and allow only a small rendering tolerance. For example:

```js
const fitsViewport = document.documentElement.scrollHeight <= window.innerHeight + 1;
```

For overlap checks, compare bounding rectangles for relevant adjacent elements, accounting for intentional overlap where the design requires it. Do not treat a general geometric scan as proof of correctness; it must be paired with screenshot review.

For prose-heavy pages, estimate line length from rendered width and font size or use a more direct text-measurement method. Flag text that approaches or exceeds roughly 80 characters per line. Reading-focused designs commonly target about 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visual defects such as exposed background strips, poor visual balance, or unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both of these pass:

1. visual inspection of the screenshots; and
2. applicable programmatic layout and usability checks.

## 6. Fix failures and rerun the sweep

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the underlying layout rule causing the failure;
3. fix the behavior rather than adding a narrow viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the size that first exposed the problem.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights and states, and the checks performed.

| Report item | Record |
|---|---|
| Viewports tested | [For example: 320, 480, 600, 720, 1024, 1440, and 1920 px] |
| Height coverage | [Short, tall, and any known target viewport] |
| States tested | [Representative content, validation, loading, empty, or error states] |
| Evidence | [Screenshots reviewed and programmatic checks passed] |
| Exceptions | [Any unverified viewport, state, or known limitation] |

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

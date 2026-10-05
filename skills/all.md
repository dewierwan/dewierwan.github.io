# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas. It is to identify genuinely different paths, make tradeoffs visible, and leave the user with a small set of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they link documents, discussion records, prior decisions, research, or other accessible sources, review only the sources relevant to the decision.

When the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Existing commitments, deadlines, budgets, or technical constraints
- Stakeholder concerns, decision ownership, and approval boundaries
- Evidence about what has already been tried

Use private communications or records only for a legitimate purpose with clear authorization. Use the minimum necessary information, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

Do not search broadly by default. If important information is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- What decision is actually being made
- Important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging options

The user may describe a symptom or a preferred solution rather than the real decision. For example, “Should we add a feature?” may actually mean, “How should we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip the pause only when the decision is obvious and low-stakes, or when the user explicitly requests an immediate first pass. Incorrect framing creates polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision genuinely has fewer meaningful paths. Each option must represent a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes the process, incentives, scope, or framing
- At least one surprising option, such as delaying, partnering, reducing scope, or deliberately doing nothing

Do not be contrarian merely to seem creative. A “do nothing” option is useful only when observation, timing, or avoiding distraction has real value.

Give every option a short, memorable label. For each option, provide:

- **What:** One or two sentences explaining the approach
- **Strengths:** One or two concrete advantages
- **Weaknesses:** One or two concrete disadvantages or failure risks
- **Effort:** Low, Medium, or High

Use specific tradeoffs. Do not soften serious drawbacks or make a preferred option look better by describing alternatives unfairly.

### Option template

| Option | What | Strengths | Weaknesses | Effort |
|---|---|---|---|---|
| [Short label] | [One- or two-sentence approach] | [Concrete advantages] | [Concrete drawbacks or risks] | [Low / Medium / High] |

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, and stakeholder burden. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when instructive, but state clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may select an option, ask for more detail, correct the framing, request additional options, or propose a hybrid.

If they propose a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once a path is selected, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge or pre-mortem before commitment. Use this for major strategic bets, public commitments, long-term obligations, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record: the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The options are genuinely distinct.
- The framing captures the actual decision rather than only the stated symptom.
- Constraints and assumptions are explicit.
- Weaknesses are candid and proportionate.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than unstated assistant preferences.
- Any use of internal or personal context was necessary, authorized, and appropriately minimized.


---
name: pressure-test
description: Find weak points in a leading strategic idea before commitment. Steelman the case, test its load-bearing assumptions through sequential challenge, and finish with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach, if applicable.

### Readiness gates

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes an exercise in defending it.
- If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.
- If the test requires communications, feedback, records, or other information about people, first confirm a legitimate, decision-related purpose and clear authorization to access and use those sources.
- Use the minimum relevant sources and information. Prefer aggregate, anonymous, or de-identified evidence when it can answer the question.
- Do not collect, repeat, or infer unrelated sensitive personal information, including health, family, financial, identity, private communications, performance information, or legally protected characteristics. Use such information only when necessary, authorized, and appropriate for the decision.
- Respect consent and reasonable privacy expectations. If consent, authorization, or appropriate use is unclear, stop and seek clarification or use non-personal evidence instead.
- Keep findings within the appropriate access boundary. Share them only with people authorized to receive them, and remove names or identifying details unless necessary and authorized.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Use available evidence such as research, metrics, prior experiments, customer feedback, documented decisions, or authorized stakeholder input. Distinguish facts, inferences, and forecasts.
- Refer to relevant dissenters by role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- When reporting stakeholder input, describe role-relevant concerns rather than unnecessary personal details.
- Skip a section only when genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's actual intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, starting with the assumption most likely to undermine the decision.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Name the test] |

Make assumptions observable where possible. Replace “users will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions and adapt later questions to the answers received. Do not present the full list as a questionnaire; that permits selective answering.

Draw from these categories:

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

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution problems, external conditions, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable signal] | [Name the check or accountable role] |

Warning signs must be observable early enough to change course. Use aggregate or de-identified signals whenever individual-level information is unnecessary.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap; do not assume silence means agreement.

Dissent is not an automatic veto. It exposes constraints, incentives, dependencies, and risks that supporters may miss. Seek input through appropriate channels without pressuring people to disclose private information or exposing their views beyond the agreed audience.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step:

- **GREEN — proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER — test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data collection period. Next: run that test, then make the decision with its result recorded.
- **RED — stop, redesign, or reopen options.** A core assumption is weak, the downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

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

When people-related information was used, also verify that the purpose was legitimate and decision-related, access and use were authorized, only necessary information was used, sensitive details were excluded unless necessary and authorized, consent and privacy expectations were respected, and the output is limited to its appropriate audience.

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, using personal information beyond the decision need, and giving a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, make and record meaningful choices only with permission, and review outcomes without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make decisions with the right amount of rigor. The goal is not maximum analysis. It is to make a clear call when ready, preserve reasoning for meaningful choices, and learn from outcomes.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** Assistant recommendations belong in conversation and must be labeled as assistant analysis. Put them in a record only if the user specifically requests this.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution. Plan or do the task instead of opening a decision process.
5. **Record only with permission.** “Should we do X?” asks for analysis, not permission to create a record. Create, update, or share a decision record only when the user asks to log, track, open, or commit it, or explicitly agrees.
6. **Protect privacy and access boundaries.** Before using shared communications, records, or a shared register, establish a legitimate purpose and clear authorization. Use the minimum relevant sources and facts. Omit unrelated sensitive details.

If a record can be read by others, confirm that its audience is appropriate before writing. For health, relationships, compensation, confidential personnel matters, or other sensitive subjects, offer a private record or keep the discussion in chat.

## 1. Choose the mode

Determine whether this is a new or existing decision.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review point and has not yet received an outcome assessment.

If the user explicitly names the mode, follow that instruction. Otherwise, if authorized, check the available decision records for an overlapping decision before creating a duplicate.

For a resume, append new information rather than overwriting history. For a review, use the original prediction and reasoning as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Write the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What is the deadline or decision trigger?
- What result is desired?
- What happens if no action is taken?

If the issue is broad and credible options do not exist yet, generate options before evaluating them. Do not pressure-test a vague problem statement.

If there is only one viable path, say so directly:

> This appears to be a task rather than a decision. The next step is to plan or execute it.

## 3. Classify scope

Ask one clarifying question at a time when needed. Place the choice in one bucket.

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
- **Assistant analysis:** Recommendations and reasoning supplied by the assistant.
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

Use a recording method chosen by the user, such as a private document, notebook, shared register, or other appropriate location. A useful record contains status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use an appropriate reminder method for high-stakes reviews.

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
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, recommendation, implementation, verification, and handoff, with an analysis-only stopping point when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user explicitly requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's proposed solution. If they ask to build something, work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is it?
- What outcome would materially improve the situation?
- What constraints, dependencies, and success measures apply?

Write a concise problem statement and descriptive requirements. Describe the desired outcome and constraints, not an assumed implementation. If the proposed solution does not appear to address the real problem, say so clearly.

Ask only for information that cannot be found in authorized, relevant context such as project documentation, code, tests, or operating procedures. When reviewing communications or records about people, confirm a legitimate purpose and clear authorization; use only the minimum relevant sources, exclude unrelated sensitive details, and keep findings within the appropriate access boundary.

## 2. Decide whether to solve it now

Assess severity, frequency, affected users, opportunity cost, current alternatives, and maintenance cost. Treat “do nothing,” “deprioritize,” or “improve the workaround” as valid options when the problem is low-impact or adequately handled.

Distinguish between decisions:

- **Reversible decisions:** Small choices that are easy to change. Use reasonable judgment and move forward.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, migrations, long-lived settings, security boundaries, external commitments, or vendor contracts. Pause for an explicit decision before implementation and record the rationale when appropriate.

If priority or direction is unclear, present the tradeoff to the responsible decision-maker before investing in substantial design or implementation.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, code, tests, deployment procedures, and previous attempts. Identify existing patterns, reusable components, compatibility expectations, ownership boundaries, security requirements, and monitoring practices.

Use the system’s established conventions unless there is a clear, documented reason to change them. Do not assume a new tool, dependency, or service is necessary before checking what existing capabilities can solve.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. For example:

| Criterion | Example standard |
|---|---|
| Correctness | Must preserve existing data and authentication behavior. |
| Effort | Should fit the available delivery and maintenance capacity. |
| Operational fit | Must work with current deployment, support, and ownership practices. |
| Reversibility | Should be removable or recoverable if it fails. |
| Verification | Must have a clear test or observable success condition. |

These criteria prevent the first plausible idea from winning by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variants of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution, such as clearer guidance, a process change, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an external service.

For highly ambiguous problems, generate a wider candidate set before narrowing. Keep each option concise: what it is, what it solves, its major costs, and its key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate inputs and fail clearly for invalid states; do not silently turn programmer errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Place changes in the appropriate design boundary rather than applying a quick fix elsewhere.

## 6. Evaluate and recommend

Compare viable options against the criteria. Produce a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Store the proposal in the user’s chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear title, such as `DD MMM YYYY: Solve — [topic]`.

**Readiness gate:** Do not implement a hard-to-reverse commitment without an explicit decision. Do not proceed beyond this step for analysis-only work.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, dependencies, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm behavior against the evaluation criteria, including compatibility, failure behavior, and rollback assumptions.

**Verification audit:** Before claiming completion, confirm:

- The implemented behavior addresses the stated problem.
- Required tests and checks were run, with results recorded.
- Untested paths, assumptions, and known limitations are identified.
- No unapproved persistent interface, data, security, or vendor commitment was introduced.
- Release, commit, publication, and deployment actions follow the user’s established practices.

## 8. Hand off

Report the outcome in operational terms:

- What changed and what it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user action, rollout steps, monitoring, or rollback conditions.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and useful operational detail. Do not claim success solely because code was written or a configuration was changed.


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
description: Draft or revise email in the user’s authentic voice using an approved style guide or authorized sent-message examples, while checking facts, commitments, privacy, and recipient fit before producing copy-ready text.
---

# Write in my voice

Use this workflow when drafting, replying to, or polishing an email on the user’s behalf.

## Goal

Produce a concise, send-ready email that sounds recognizably like the user rather than a generic assistant. Match the user’s established habits while adapting appropriately to the recipient, relationship, and stakes.

## 1. Load voice evidence

Before drafting, read the user’s current writing profile in full, if one exists. If a profile is unavailable or incomplete, use authorized examples of messages the user actually sent. Access private communications only for a legitimate drafting purpose, with clear authorization, and use the minimum relevant examples and details.

Build a practical voice profile from the evidence:

- Typical greetings and sign-offs.
- Formality, warmth, and directness by audience.
- Usual sentence and paragraph length.
- Preferred vocabulary, contractions, colloquialisms, punctuation, and formatting.
- Whether the user uses emojis, exclamation marks, bullets, or dashes.
- Phrases, tones, filler, or punctuation the user avoids.
- How the user makes requests, gives feedback, declines, follows up, apologizes, or communicates uncertainty.
- Approved reusable facts, links, scheduling instructions, boilerplate, and standard replies.

Give greater weight to recent sent messages and explicit style guidance than to older examples. If evidence conflicts, ask which preference is current, or follow the most recent consistent pattern.

Do not expose private examples, unrelated personal details, or the contents of the user’s writing profile in the output.

## 2. Confirm the email brief

Gather the minimum information needed to write safely:

1. Who is the recipient, and what is their relationship to the user?
2. What outcome should the email produce?
3. What facts, dates, names, links, attachments, decisions, or commitments must appear?
4. What level of warmth, urgency, or firmness fits the situation?
5. Are there deadlines, sensitivities, approvals, or access limits?

If a missing detail could materially change the message, ask one focused question. Do not invent facts, availability, decisions, promises, prices, opinions, emotional reactions, or authority to act.

When using private records or personal information, include only what the recipient needs for the stated purpose. Respect consent, confidentiality, and the user’s intended access boundary.

## 3. Adapt the voice to the situation

Voice is a pattern, not a rigid template. Keep the user’s recognizable style while adjusting for context.

| Situation | Adaptation |
|---|---|
| Familiar colleague or ongoing collaborator | Use the user’s normal level of brevity and familiarity. |
| New, external, senior, or formal recipient | Keep the user’s voice, but provide enough context and use clearer, more careful wording. |
| Request or coordination note | State the requested action, responsible person, and timing plainly. |
| Correction, rejection, or conflict | Be direct, factual, and respectful. Avoid defensiveness, exaggerated praise, and unnecessary apologies. |
| Sensitive personal or confidential matter | Use only necessary details, avoid forwarding or repeating sensitive information unnecessarily, and confirm the intended recipient if needed. |

Use approved boilerplate, factual details, or links when they fit the current context. Never reuse a standard response if it would be inaccurate, misleading, outdated, or too broad for the recipient.

## 4. Draft the smallest complete email

Write only what helps the recipient understand and act. A reliable structure is:

1. Greeting, if the user normally uses one.
2. The purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Closing and sign-off, if appropriate to the user’s style and email thread.

Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Make requests, decisions, deadlines, and links easy to find. Use bullets only when they improve clarity for actions, options, or logistics.

Remove:

- Throat-clearing and explanations of the drafting process.
- Generic compliments, repeated thanks, or ceremonial language that does not serve the message.
- Empty filler such as “just wanted to” or “hope you’re well,” unless it is both natural to the user and useful in context.
- Hedging that weakens a clear request or decision.
- Extra detail that the recipient does not need.

## 5. Audit before presenting

Review the draft line by line:

- Would the user plausibly write these exact words?
- Do the greeting, closing, punctuation, rhythm, and length match the available evidence?
- Is the tone appropriate for this recipient and situation?
- Did the draft add an unsupported commitment, claim, opinion, emotion, or deadline?
- Are names, dates, links, attachments, and references accurate?
- Is the required action or decision unmistakable?
- Does the draft reveal only information appropriate for this recipient?
- Can any sentence be removed without losing meaning or usefulness?
- Does it avoid language and formatting habits the user dislikes?

If no voice evidence exists, use a broadly useful default: concise, warm-professional, clear, and direct. State that assumption briefly only when needed, and invite the user to provide a style guide or a few authorized examples for future drafts.

## Output format

Provide the final email as copy-ready text. Ask only the specific clarification needed when a safe draft cannot be completed. Do not add rationale, alternatives, or drafting commentary unless the user asks for them.


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
description: Create an evidence-based professional case study post from authorized source material, with strong hooks, a concise narrative, quote-card options, approval checks, and a publishing-ready delivery package.
---

# Write a case study post

Use this workflow to turn authorized source material about a person’s career, learning, professional change, or project outcome into a concise public case study. It is designed for professional social posts, but can be adapted for newsletters, community updates, program alumni stories, recruitment pages, or similar formats.

The goal is not vague praise. Show a credible and specific change: where the person started, what they were considering, what they did, what concretely helped, what they do now, and what the reader can do next.

A strong case study lets a reader recognize their own situation in the subject’s before-state. It names the intervention clearly and explains the mechanism without claiming that one course, community, person, or resource caused an outcome that has multiple causes.

## Purpose, authorization, and boundaries

Use personal records, interviews, applications, direct messages, internal notes, and professional profiles only for a legitimate publishing purpose and with clear authorization from the organization that controls the material. Use the minimum sources and information needed for the post.

Before drafting, confirm:

- The organization has a legitimate reason to publish the story.
- The subject has consented to the intended public use, or the publisher has another clear and appropriate basis to use the material.
- The person’s preferred public name, pronouns, and relevant affiliations are correct.
- The proposed audience and platform are defined.
- You are staying within the access boundary of the people who provided the information.

Do not include unrelated personal details, private contact information, family details, health information, legal matters, immigration status, financial information, or sensitive background merely because it appeared in the source material. Public availability does not automatically make a detail useful or appropriate to repeat.

## Inputs

Gather all available, authorized source material. Useful inputs include:

- An interview transcript and meeting notes
- An application, intake form, or self-written statement
- A current professional profile or public biography
- Official announcements, public work samples, projects, papers, or grants
- A community message celebrating a result
- A previous draft, outline, or notes from the subject
- An editorial or brand voice guide
- The target audience, publishing platform, and desired call to action

Before writing, create a fact sheet. If a critical detail is missing or uncertain, ask focused questions before drafting. Never guess at organization names, job titles, paper titles, dates, salary figures, timelines, mechanisms, or outcomes.

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns, and whether first-name usage is appropriate |
| Before-state | Previous role, field, goal, uncertainty, constraint, or alternative path |
| Trigger | Why they joined, applied, changed direction, or took action at that point |
| Intervention | Program, community, resource, event, mentor, or product involved |
| Mechanism | Concrete help, such as a realization, opportunity post, introduction, feedback session, or practical resource |
| Now-state | Current role, organization, team, project, output, or result that may be named publicly |
| Timeline | Verified dates or time spans from the relevant starting point to outcome |
| Evidence | Approved roles, figures, dates, artifacts, and direct quotes |
| Cost or risk | Any career, geographic, financial, or professional tradeoff that is approved for use |
| CTA | The one action the intended reader should take next |

Useful clarification questions:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they decide to take part or make a change at that point?
4. What are the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a specific output, project, placement, publication, or result that can be named publicly?
8. Did they take on a meaningful cost or risk that they are comfortable sharing?
9. Which claims, figures, quotations, names, and affiliations have been approved for public use?
10. Who should this post persuade or help?

## Evidence and verification rules

Never invent facts or strengthen a claim for dramatic effect. If a source says someone contributed to a project, do not call them the lead. If they explored an opportunity, do not say they received it. If a project is unpublished, do not present it as public or complete.

Treat automated transcripts and summaries as useful but fallible. They can mishear names, organizations, technical terms, numbers, titles, and quotes. Cross-check important details against a more reliable source, such as direct subject confirmation, an official public record, a current professional profile, published work, or a written application.

Use this reliability order unless a specific case gives you a good reason to change it:

1. The subject’s direct, recent confirmation
2. Official public records, published work, or an organization’s announcement
3. A current professional profile
4. The subject’s original written application or statement
5. Interview transcript notes or automated summaries
6. Informal third-party messages

Separate these three statement types in private working notes:

- **Verified fact:** A role, date, artifact, figure, or quote supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn from the story. Use it only when well supported, and phrase it modestly.

Do not claim the intervention caused the whole outcome unless the evidence supports that causal claim. Prefer precise wording such as “the program helped them see the field differently,” “they found the opportunity through the community,” or “the conversation clarified what to do next.”

## Sensitive-content approval gate

Flag the following for explicit approval from the subject before publication:

- Salary, compensation changes, financial hardship, or pay comparisons
- Health, family, legal, immigration, housing, or other sensitive personal circumstances
- Harsh language about a past employer, role, or career choice
- Unreleased work, confidential projects, internal information, or unpublished titles
- Direct quotations, especially strong opinions or criticism
- Claims about why an employer selected the person
- Claims of causation or impact that cannot be independently verified
- Timelines that could expose private circumstances

If approval is unavailable, use an honest fallback only if it remains approved and useful. For example, replace an exact compensation change with “they accepted a lower-paying role” only with approval. Do not conceal uncertainty by making the story broader, vaguer, or more dramatic.

## Build the story beats

Create a short private working outline before drafting. Do not expose raw personal material in the final deliverable unless it is necessary and approved.

### 1. Before-state

Capture the subject’s role, background, and reader-relevant uncertainty. Include the alternative path they were considering when it mirrors the audience’s current life.

Keep only facts that move the story. A long biography, reading list, or credential list usually weakens the post. Keep a detail when it explains the person’s decision or makes the change believable.

### 2. Trigger

Identify why the person acted at that moment. They may have wanted to test whether a field was open to them, gain practical knowledge, find collaborators, solve a problem, or make a values-led career decision.

### 3. Mechanism

Find the one or two observable events that helped move the person forward. Good mechanisms include:

- Realizing that a field or role was accessible
- Seeing a relevant opportunity in a trusted community
- Having a conversation that clarified possible next steps
- Receiving feedback that improved an application or project
- Being introduced to a relevant person, event, workshop, or resource

Avoid “the experience was transformative.” Name what happened instead.

### 4. Now-state

Record the current role, approved organization or team name, and what the person actually does. Translate technical jargon enough for the intended reader to understand why the work matters.

Use named outputs only when they add proof or interest. One meaningful project, publication, product, grant, or placement generally does more than a long list of credentials.

### 5. Timeline and compression

Map the sequence from the starting point to the result. Calculate a short, truthful timeframe if it sharpens the story, such as “within six months” or “the following year.” Do not force a compressed timeline when the evidence does not support one.

### 6. Quotes

Pull three to five verbatim candidate quotations. Favor lines that speak to the reader’s identity or uncertainty, rather than only celebrating the subject’s achievement.

Look for three categories:

1. **Discovery:** “I did not know this path was open to someone like me.”
2. **Mechanism:** “I found the opportunity through the community.”
3. **Conviction:** “I would make the same choice again.”

Light trimming is allowed only when it preserves the speaker’s exact meaning and grammar. Do not rewrite a quote into something the person did not say.

## Generate three hook options

For feed-based platforms, the first two lines determine whether a reader continues. Write three distinct hooks before drafting the full post. Keep each to two short sentences, usually under about 140 characters total when that suits the platform.

### Hook A: Discovery

Use when the target audience shares the person’s former blocker.

**Formula:** The person did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a concrete, surprising mechanism.

This is usually the best default because the reader sees their own uncertainty in the opening.

### Hook B: Identity collision

Use when the before-and-after contrast is vivid and understandable.

**Formula:** A short time ago, the person was doing a specific thing. Today, they are doing a sharply different specific thing.

This is especially useful for broad audiences who may not share the subject’s exact former uncertainty.

### Hook C: Stakes-led

Use only when a meaningful cost or risk has approval and the audience will see it as honest conviction rather than a warning.

**Formula:** The person accepted a specific cost to do something. Now they are taking a concrete action or doing meaningful work.

Avoid this hook if it implies that participation requires hardship or makes an accessible opportunity sound out of reach.

Choose one recommendation. State in one sentence why it best fits the intended reader, then explain briefly why the other two are less suitable.

## Draft the post

Aim for about 160 to 220 words unless the platform, audience, or subject matter requires another length. Shorter is often stronger.

Use this sequence:

1. **Hook:** Use the recommended hook.
2. **Before-state:** Write one short paragraph showing the person’s previous situation and a reader-relevant alternative path.
3. **Name the intervention:** Clearly state that they joined the program, used the resource, entered the community, or attended the event. Do not leave this connection implicit.
4. **Mechanism and immediate outcome:** Explain the concrete turning points, then state what happened next in plain language.
5. **Current work:** Describe what they do now and why it matters in language the audience can understand.
6. **Optional honest cost:** Include it only when approved and genuinely useful.
7. **Optional pull quote:** Include it only when it adds a distinct truth not already carried by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

Where a platform may reduce distribution for external links in post text, decide whether to place the link in a comment, profile destination, or other designated location. Treat this as a platform-specific publishing choice, not a universal rule.

## Style rules

Adapt to the chosen editorial voice. If no style guide exists, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense where possible.
- Use specific names, roles, dates, and figures only when verified and approved.
- Use the person’s first name after their first full introduction if that fits the tone and consent.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not call someone exceptional, inspiring, or brilliant without showing why.
- Use contractions if the voice is conversational.
- Keep the CTA in full second person: “If you are…” and “you can…”
- Avoid emojis unless they are an explicit brand choice.
- Avoid em dashes by default. Use periods, commas, or line breaks instead.

On the final pass, remove machine-like phrasing. Cut empty transitions, dramatic setup frames, filler intensifiers, hedge words, abstract nouns standing in for evidence, balanced “on one hand/on the other hand” constructions, and reflective summaries after the CTA.

Avoid corporate or generic phrases such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm” unless they are necessary in an approved direct quote.

Read the post aloud. If it sounds like a generic thought-leadership template, shorten it and replace abstractions with facts.

## Graphic quote options

Provide three options for a visual quote card. Each should be self-contained, under 15 words when possible, and drawn verbatim from approved source material.

Offer one quote from each category:

- Discovery
- Mechanism
- Conviction

Recommend one quote. Discovery quotes are often strongest because they work without context and mirror the reader’s possible uncertainty. Choose a mechanism or conviction quote only when it is clearer, more memorable, and understandable on its own.

## Readiness audit

Before sending the draft for review, check:

- Is every name, role, date, figure, title, and quote verified?
- Were transcript-derived details cross-checked where needed?
- Does the post show a concrete mechanism, not only a result?
- Does it avoid overstating causation?
- Is the intervention named clearly?
- Does the opening mirror a real audience concern?
- Is the current work understandable to a non-specialist reader?
- Have sensitive claims and direct quotes been flagged for approval?
- Are unrelated or sensitive personal details omitted?
- Is the CTA clear and directed to the intended reader?
- Are there no unsupported superlatives, corporate phrases, generic filler, or unnecessary em dashes?

## Delivery format

Create the draft in the user’s chosen, authorized document system if one is available. Use a clear title format such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and the two alternatives
- The three graphic quote options and recommendation
- A list of approval items
- A list of missing information that would strengthen the post
- The document location or link, if applicable

Do not treat the first draft as final. If feedback says “make the hook better,” generate new hooks rather than making small edits. If asked to make it shorter, cut secondary biography first while preserving the mechanism and outcome. If the subject rejects a sensitive line, replace it with an approved fallback without weakening the entire story.

After the final version is accepted, review feedback for reusable lessons. Update the workflow only when a recurring pattern is clear, such as a missing intake question, a consistent voice preference, a structural preference, or a repeated verification issue. Do not invent process changes after a clean review cycle.


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
description: Gather authorized context, clarify the user’s desired outcome, and create a practical meeting brief and agenda that can be used during the call and for follow-up.
---

# Prepare for a meeting

Use this workflow when someone asks to prepare for a meeting, review upcoming meetings, or produce a meeting brief and agenda. The result is a complete, shareable preparation page or document in the user’s chosen workspace, not merely a chat summary.

The workflow is designed for consequential external meetings, relationship meetings, recruiting conversations, sales or partnership calls, proposal reviews, negotiations, and recurring one-to-ones. Adapt the depth to the meeting’s importance and available time.

## Principles

- Research only for a legitimate meeting-preparation purpose and only when the user is authorized to access the source material.
- Use the minimum relevant information. Do not copy unrelated personal details, confidential records, compensation data, health information, or private communications into broadly visible meeting notes.
- Read the artifact that the meeting is actually about. Do not replace a proposal, memo, application, deck, or draft with generic discovery questions.
- Separate evidence from inference. State what is known, what is reported by another person, what is uncertain, and what needs confirmation.
- Ask before assuming. A well-researched agenda can still be wrong if it does not reflect the user’s objective, constraints, and desired level of directness.
- Make the brief usable cold. Explain unfamiliar people, organizations, projects, and acronyms wherever they appear.
- Keep the final agenda realistic for the meeting duration and place the most important issue before routine updates.

## 1. Scope the request and select meetings

Establish:

- The target date or date range.
- Which meetings need preparation.
- The user’s time zone.
- Whether to prepare all substantive meetings or only selected ones.
- The intended output location: a document, workspace page, CRM note, calendar attachment, or another user-chosen system.

A useful default is to prepare external one-to-ones and small-group meetings, and skip obvious focus blocks, meals, internal placeholders, and events without a substantive purpose. However, the user may choose a different scope.

For each selected meeting, capture:

- Title and scheduled start/end time.
- Attendee names, roles, and organizations where known.
- Whether attendees are internal, external, or both.
- Location or joining details when relevant.
- Invitation description and stated purpose.
- Links, attachments, and referenced documents.
- Scheduling context, such as an introduction, reschedule note, conference follow-up, hiring stage, or prior commitment.

If the event is ambiguous, do not invent a purpose. Mark the uncertainty and resolve it during the clarification step.

## 2. Research authorized context

Research each external participant and the relationship history using only sources the user may legitimately access. Prioritize relevance over exhaustive collection. A current conversation, recent decision, or written artifact normally matters more than a large volume of old material.

Use the following source categories when available and appropriate:

### Direct correspondence and mentions

Search authorized email or messaging records in two ways:

1. **Direct correspondence:** messages sent between the user or organization and the participant.
2. **Name or organization mentions:** messages that mention the participant or their organization even when they were not a sender or recipient.

The second search often reveals why the meeting exists: an introduction, a referral, a prior proposal, a hiring thread, a request for feedback, or another stakeholder’s context.

Read enough recent and relevant material to establish the relationship. Do not indiscriminately copy message contents. Extract only meeting-relevant facts, open commitments, decisions, concerns, and unanswered questions.

### Internal knowledge sources

Search authorized internal notes, prior meeting records, project documents, customer records, or relationship-management systems for:

- Previous meetings and their outcomes.
- Promises, commitments, and next steps.
- Shared projects or decisions.
- Relevant organizational context.
- Prior concerns, objections, or unresolved disagreements.

When a record might belong to a different person with the same name, verify identity using reliable matching details such as email address, current organization, role, or other non-sensitive context. If the match is uncertain, exclude it or label it clearly as unconfirmed.

### Calendar history

Check prior events involving the participant to establish:

- Whether this is a first meeting or an ongoing relationship.
- The relationship arc, not just the most recent interaction.
- How often the parties meet.
- Whether earlier follow-ups or deadlines were missed.

### Public professional context

Use public, reliable sources to understand:

- The participant’s current role and organization.
- What their organization does.
- Relevant recent publications, announcements, or work.
- Professional links that genuinely help the user prepare.

Do not treat search snippets, unattributed claims, low-quality directories, or stale profiles as established facts. Label single-source or time-sensitive claims with their source and date, or omit them.

### Relevant organizational records

If the meeting concerns an application, service request, customer relationship, partnership, grant, contract, or hiring process, search the authorized system of record for the relevant artifact. Confirm that the record belongs to the meeting attendee before relying on it.

Use information proportionately. For example, a meeting brief may say that someone has an alternative path or is evaluating several options, but it should not disclose private financial figures or sensitive details unless the output is restricted to people who need that information and sharing is appropriate.

## 3. Read the meeting artifact in full

If the meeting is about a proposal, pitch, draft, memo, application, deck, report, strategy document, or other written artifact, locate and read it before drafting the agenda.

Signals include:

- A meeting title such as feedback on a proposal, review of a draft, or discussion of a plan.
- Links or attachments in the invitation.
- Recent messages referring to comments, edits, a shared document, or a deck.
- An explicit request to consult on a topic that likely has a written form.

Read the whole artifact, including tabs, appendices, linked sections, and relevant comments where access permits. Capture:

- The central claim or ask.
- Assumptions that need testing.
- Decisions requested.
- Alternatives considered.
- Important constraints, dates, or dependencies.
- Points that are unclear, weakly supported, internally inconsistent, or likely to draw objections.

If the context implies that an artifact exists but it cannot be found, ask the user for the link during clarification. Do not pretend to have reviewed it or build a generic agenda around an unseen document.

## 4. Detect specialized meeting types

Before preparing a general agenda, determine whether the meeting needs a specialized workflow.

Examples include:

- A reference conversation for a candidate or contractor.
- A performance, disciplinary, or sensitive people-management conversation.
- A legal, regulatory, security, or incident-review meeting.
- A formal negotiation with restricted commercial terms.
- A medical, therapeutic, or other highly sensitive personal discussion.

For a reference conversation, use an authorized reference-check process with role-relevant capability questions, evidence requests, and consistent treatment of candidates. Do not produce a generic relationship-building agenda if the real purpose is an assessment.

For a specialized meeting, preserve useful research already completed, but use the appropriate structure, privacy controls, and question set. If no specialized workflow applies, continue below.

## 5. Build and share a situation brief before choosing the agenda

Before proposing the goal or agenda, share a concise situation brief with the user. This gives them enough context to correct assumptions and choose a direction.

Choose the shape that fits the meeting:

### Narrative brief

Use for most meetings. It should take about a minute to read and cover:

- Who the participant is.
- The organization or project context.
- Relationship history.
- Why the meeting is happening now.
- The live question, tension, or opportunity.

### Decision-shaped brief

Use when a concrete decision, close, recruit, negotiation, or commitment is at stake. Cover:

- Their stated ask.
- Their plausible alternatives and deadlines, where known.
- The user’s position or leverage.
- Risks and constraints.
- What remains unknown.

These forms can be combined: start with a short narrative, then add a compact decision section.

### Situation brief template

```markdown
## Situation brief

### Who they are
[Name] is [role] at [organization, described in a few words]. [One relevant background fact, if verified.]

### Relationship and meeting trigger
[First meeting / concise relationship arc.] This meeting follows [introduction, prior discussion, shared artifact, decision point, or other trigger].

### Where things stand
[What has happened, what each side appears to want, and what remains unresolved.]

### Live questions or tensions
- [Question, trade-off, or risk that matters now.]
- [Question, trade-off, or risk that matters now.]

### Relevant links or materials
- [Artifact or profile — why it matters]
```

Do not use unexplained names in a brief. If a person, organization, program, or term comes from research rather than the user’s own request, explain it briefly when first mentioned. Repeat the explanation in sections that may be read independently, such as the close or quick-question list.

## 6. Ask targeted clarification questions

Ask focused questions after sharing the situation brief and before writing the final goal or agenda. This is normally mandatory for consequential meetings because research alone cannot establish the user’s intended outcome.

Cover at least:

- **Primary goal:** What result should the meeting produce?
- **One shaping factor:** a failure mode, tone, sensitivity, decision boundary, or concrete ask.
- **Catch-all:** What else should be landed, avoided, or kept in mind?

Ask additional questions when they materially change the agenda. Good axes include:

- Is the participant still in their current role or actively exploring another path?
- Does the user want to state a view directly or first draw out the other person’s view?
- What would make the meeting go badly: overselling, being too passive, raising the wrong issue, or failing to secure a next step?
- Is there a specific ask for time, advice, an introduction, a decision, resources, or a commitment?
- What level of directness is appropriate?
- What decisions can the user make in the meeting, and what requires later approval?

Do not ask the user to write the agenda for you. Ask about targets, boundaries, and trade-offs; then convert their answers into a useful agenda.

Use compact, labeled choices so the user can reply quickly. Make the recommended choice first, but include real alternatives. Avoid false either/or choices when both actions can sensibly be combined.

```markdown
1. What is the primary outcome?
   - **1a (recommended):** Understand their position and agree a concrete next step
   - **1b:** Build the relationship without making an ask
   - **1c:** Make a direct proposal or request

2. What should the conversation avoid?
   - **2a (recommended):** Avoid committing before key unknowns are resolved
   - **2b:** Avoid being so cautious that momentum is lost
   - **2c:** Avoid discussing [sensitive topic] unless they raise it

3. Is there anything else to land or avoid?
   - **3a:** Nothing to add
   - **3b:** I will add notes
   - **3c:** I have a constraint or context to share

Reply with labels, for example: 1a, 2b, 3a.
```

If more than four questions are useful, ask in two rounds. Put questions that change the available options in the first round, then adapt the second round to the answers. Before sending, verify that every question is numbered, every option has one unique matching label, labels remain sequential, and the final round contains the catch-all question.

You may skip questions only when the meeting purpose, desired outcome, constraints, and recurring agenda are genuinely explicit and stable. When in doubt, ask.

## 7. Create the meeting page or document

Only create the final page after the brief and clarification answers have shaped the plan. Store it in the user’s chosen workspace with the least restrictive appropriate access boundary.

Use a clear title such as `[Date] — [Participant or meeting topic]`. Store the meeting date separately from the title when the chosen system supports structured date fields. Do not include meeting times, confidential compensation, sensitive personal information, or restricted commercial details in a broadly visible title or shared database field.

Use this structure:

```markdown
# [Date] — [Participant or meeting topic]

## Context
[Who they are, relevant organization context, relationship history, why the meeting is happening, and links to the most useful materials. State if this is the first meeting.]

## Goal
[One or two sentences reflecting the user’s stated outcome and constraints.]

## Agenda
Text under **Say** is word for word. Anything in [square brackets] is a cue for you, not something to say aloud.

### 0–5 min: Open and frame
**Say**

[Exact opening words.]

**Interviewer note**

[Private guidance on tone, context to establish, or a trap to avoid.]

### 5–20 min: Diagnose [topic]
**Questions**

1. [Decision-relevant question.]
2. [Question that tests an assumption or reveals constraints.]

**Interviewer note**

[What to listen for and what needs a follow-up.]

### 20–35 min: Explore, test, or propose [topic]
**Say**

[Exact transition or proposal wording.]

**Questions**

1. [Pressure-test question tied to the artifact or decision.]
2. [Question about alternatives, trade-offs, or feasibility.]

**Interviewer note**

[Specific evidence to seek and which issue should not be left vague.]

### 35–45 min: Close and create a next step
**Say**

[Exact close wording.]

**Questions**

1. [Concrete forcing question about a date, owner, decision, or next artifact.]

**Interviewer note**

[Fallback close if no decision is possible today.]

## 5 most important questions to ask

1. [Most decision-relevant question.]
2. [Question that reveals the key uncertainty.]
3. [Question that tests the main assumption or gap.]
4. [Question needed to choose a path.] 
5. [Specific close for a date, owner, decision, or next artifact.]

## Timely note
[Optional current item worth mentioning, with source and date if needed.]
```

Adjust time blocks to the actual meeting duration. For a short meeting, prioritize diagnosis and a clear close. For a long working session, add decision criteria, evidence review, or ownership planning, but do not fill time merely because it exists.

The five-question section is an in-call cheat sheet, not a summary of the agenda. Rank the questions by decision value. Keep each one to a single scannable line. Include a forcing close when the meeting seeks movement or commitment.

## 8. Quality and privacy audit before publishing

Before saving or sharing, check:

1. **Purpose:** Does the page accurately reflect why the meeting is happening?
2. **User alignment:** Did the user answer questions that meaningfully shaped the goal or agenda? If not, return to clarification.
3. **Artifact fidelity:** If the meeting is about a document, does the agenda engage with its actual claims and weak points?
4. **Timing:** Do agenda stages fit the meeting length and reserve time for a close?
5. **Specificity:** Are questions concrete enough to produce useful evidence rather than polite generalities?
6. **References:** Is every unfamiliar name, organization, acronym, and project explained where needed?
7. **Uncertainty:** Are old, single-source, conflicting, or weakly supported claims labeled or removed?
8. **Privacy:** Have irrelevant personal details, confidential figures, and restricted information been excluded or kept within the correct access boundary?
9. **Compensation and sensitive terms:** Are pay figures, equity details, private offer terms, and similarly sensitive data absent from broadly shared notes?
10. **Actionability:** Does the close specify a next step, owner, artifact, or date where appropriate?

## 9. Prepare for capture and follow-up

Open or surface the final page in the user’s chosen workspace before the meeting when possible. Ensure the user can quickly reach the agenda and the five-question list.

For high-stakes persuasion, recruiting, partnership, fundraising, sales, or negotiation meetings, schedule a post-call review approximately one hour after the meeting ends, subject to the user’s authorization and tool availability. The review should:

- Retrieve the authorized transcript or meeting notes.
- Compare what happened with the intended goal and agenda.
- Identify what worked, missed signals, weak questions, and moments where the user could have been clearer.
- Record decisions, commitments, owners, deadlines, and follow-up artifacts.
- Update recurring coaching or process notes only with appropriate access controls and factual, dated evidence.

Skip automated review for purely informational meetings unless the user asks for it.

## Common failure modes

- **Research without a deliverable:** A chat recap is not complete meeting preparation. Create the agreed page or document.
- **Generic agenda despite a specific artifact:** Read the proposal, memo, deck, or application and pressure-test its substance.
- **Assuming the objective:** Always clarify the user’s desired outcome and at least one constraint or failure mode for consequential meetings.
- **Confusing identity matches:** Do not merge records solely because names match.
- **Overloading the brief:** Include only information that changes the meeting strategy or helps the user remember the relationship.
- **Unexplained references:** A bare name or acronym may be clear to the researcher but not to the user reading cold.
- **No close:** A good conversation without a decision, owner, date, or next artifact often loses momentum.
- **Unsafe sharing:** Do not put sensitive personal, financial, hiring, or contractual details into a workspace visible beyond those who need to know.

A successful meeting-preparation page lets the user understand the situation in about a minute, conduct the meeting without searching through old records, ask the few questions that matter most, and leave with a clear next step.


---
name: capture-meeting-actions
description: Review authorized meeting records to identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require human judgment.
---

# Capture meeting actions

Turn meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose and operating rules

Use meeting records only for a legitimate work purpose and with clear authorization to access them. Use the minimum relevant sources and information. Do not copy unrelated personal, sensitive, or confidential details into tasks, reports, or reusable guidance. Keep outputs within the access boundary of the selected task system and its intended users.

Before each run, apply these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries commonly misattribute work, especially in recurring one-to-ones, brainstorming sessions, or meetings where attendees list their own to-dos. Never create a task solely because a summary labels something as an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work that was completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, statement of interest, or open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply known responsibility boundaries supplied by the user or organization. Attendance at a meeting does not make the user accountable for all work in that area.

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

If the record shows that promised work was actually completed during the meeting—for example, a document was shared, an introduction was made, or an answer was delivered—do not create a task for it. Retain only minimal relationship context if it is genuinely needed for a later follow-up.

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

Do not raise priority merely because capture happened late. Raise it only when a real external deadline, material risk, or waiting counterparty justifies it.

### Notes template

```markdown
[Two or three sentences of time-independent context. Include relevant absolute
dates, why this matters, the commitment, and necessary sensitivity. Omit
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

Avoid unnecessary private discussion in a task system that may be broadly visible. Follow the user’s known writing preferences. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable. If the task is to send a message, write a ready-to-send draft rather than merely saying “email them.”

For introductions, use double opt-in: ask each relevant person for permission before connecting them and do not disclose unnecessary information about either person.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by meeting link or identifier, counterparty, distinctive topic terms, and proposed title.

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. Skip the new task, or update the existing task if the meeting adds a meaningful action, deadline, or context. Record the duplicate decision so it can be reported clearly.

## 7. Create confident tasks

Create high-confidence tasks in a batch when possible. If the environment supports opening created records, open them in the selected task system rather than filling the status update with management links.

For every skipped meeting, give a brief reason, such as “No out-of-meeting commitment,” “Completed during the meeting,” “Owned by another role,” or “Already covered by an active task.”

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

Before declaring the run complete, capture lessons that genuinely improve future runs. Keep this separate from the meeting task itself and do not add personal facts or meeting-specific confidential details to shared guidance.

- Add a short generalized note to a reusable meeting-archetype reference when a recurring pattern affects triage, such as a common attribution error, reliable sign of in-meeting completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new responsibility boundary in a maintained responsibility reference when it applies beyond one meeting and the user has confirmed it is appropriate to retain.

Do not turn one-off facts into permanent rules. Small additions to a patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing steps or changing the evidence order. Briefly report any reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links to an authorized source record where useful.
- Message drafts are ready to send and follow the user’s preferences.
- Sensitive or unrelated personal information was omitted.
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
description: Prepare, conduct, and document a structured hiring reference call that gathers concrete, role-relevant evidence while respecting authorization, privacy, and appropriate access boundaries.
---

# Run a reference call

Use this workflow when an authorized hiring team needs to check a candidate’s past work with a referee who can speak from direct experience. The goal is to gather concrete evidence about role-relevant capabilities, working conditions, and development areas—not general praise, personal background, or a final verdict from one conversation.

## 1. Confirm purpose, authority, and scope

Before preparing or contacting the referee, confirm all of the following:

- There is a legitimate hiring purpose for the check.
- The candidate provided the referee or has authorized contact where required.
- The caller may access the relevant hiring materials and create the hiring record.
- The referee is being contacted about work they are reasonably placed to discuss.

Use only the minimum relevant information. Review sources that are necessary for the decision, such as the candidate’s submitted materials, role brief, assessment evidence, scheduling details, authorized correspondence, and prior authorized reference records. Do not collect, repeat, or record unrelated personal details, sensitive information, rumors, or information outside the approved access boundary.

| Input | Confirm |
|---|---|
| Candidate | [Candidate name and role under consideration] |
| Referee | [Name, contact method, work context, and relationship to candidate] |
| Call | [Date, time, attendees, and access details] |
| Decision | [Hiring stage, next decision, and uncertainty to reduce] |
| Authorization | [Permission and appropriate access to conduct the check] |

If someone outside the hiring organization asks for a reference about a former participant, employee, or collaborator, use that organization’s appropriate outbound-reference process instead.

## 2. Establish the hiring and relationship context

Check the approved scheduling source for the call. Record its title, timing, participants, access details, and any useful scheduling context. If no meeting is scheduled, note that clearly and proceed with available information.

Then establish:

- The role’s expected outcomes and the capabilities needed to achieve them.
- The candidate’s current stage and the next hiring decision or assessment.
- How and why this referee was selected.
- How the referee worked with the candidate: for example, as a manager, peer, client, collaborator, instructor, or partner.
- How long they worked together, how closely, and what work the referee directly observed.
- Open questions from role-relevant interviews, work samples, or assessments.
- Other authorized references, so evidence can later be compared fairly.

Give more weight to direct observation than seniority, enthusiasm, or closeness to the candidate. A referee may be highly credible yet have limited exposure to the work that matters for this role.

## 3. Research proportionately

Use approved records and, where appropriate, public professional information. A practical sequence is:

1. Review direct scheduling or correspondence that establishes the relationship and call purpose.
2. Review candidate and referee mentions in authorized hiring records.
3. Check prior work interactions, meetings, or collaborations that could provide relevant context or reveal a conflict of interest.
4. Confirm the referee’s professional role and work context from public sources when needed.
5. Review completed reference records for the same candidate, if access is authorized.

Read enough relevant material to verify facts rather than relying on search snippets. Summarize what is needed for the call; do not copy extensive private correspondence into notes.

From earlier references, extract only role-relevant themes: specific strengths with examples, development areas, contradictions, evidence limits, and questions this referee is uniquely positioned to answer.

## 4. Create the call brief

Create a concise record in the hiring team’s designated, access-controlled record. The brief is the deliverable for preparation: it must contain the useful context and questions, not leave key findings in temporary notes.

```markdown
## Context
- **Referee:** [Name] — [relevant role and work context].
- **Relationship:** [How they worked with the candidate, when, and how closely the referee observed the work].
- **Hiring context:** Candidate is being considered for [role] at [stage]. Next decision: [decision or assessment].
- **Relevant materials:** [Approved candidate materials or work samples].
- **Other references:** [Other authorized referees or relationship types].

## Opening
> Hi [Name], thank you for making time. I’m [caller] from [hiring team]. [Candidate] is being considered for our [role]. I’d like to understand the work you directly observed, including strengths, limitations, and the conditions in which they did their best work. We will use your input only within the appropriate hiring process.

## Briefing notes
- [Attributed prior observation]: ask whether this referee saw the same pattern; request a specific example.
- [Open role-relevant question]: ask about [behavior, output, or work situation].
- This referee is uniquely placed to discuss [area] because [relationship context].
- [Relevant connection, conflict, or evidence limitation].
- [If first reference: establish baseline evidence for later comparison.]

## Questions
- [Tailored questions and follow-up prompts]

## Notes and assessment
- Direct observations:
- Referee interpretations:
- Examples and outcomes:
- Limits of evidence:
- Comparison with other evidence:
- Follow-up actions:
```

Write briefing notes as direct actions, not vague reminders. For example: “A previous referee said the candidate moved quickly but sometimes needed support closing final details. Ask whether you observed this, in what work, and with what impact.” Attribute every claim and do not present an unresolved concern as fact.

## 5. Ask questions that produce evidence

Start by confirming the relationship. Then seek examples of work, outcomes, behavior under pressure, and support needs. Adapt the order to the conversation.

- How did you work together, and how closely did you observe the candidate’s work?
- What did they personally own or deliver? What was the result?
- How did their work compare with expectations for their role and level?
- What is their strongest distinctive capability? Please describe an example.
- Where did they need the most support, feedback, or structure?
- Describe a difficult project, setback, or conflict. What did they do?
- How did they respond to feedback or changing requirements?
- What work-related issue might cause an early mismatch in a new role?
- If they were succeeding after several months, what development area should their manager prioritize next?
- What management approach, environment, or scope helps them contribute at their best?
- Would you choose to work with them again, and in what circumstances?
- What have I not asked that would help us evaluate their work for this role?

When answers are broad, ask: “What did that look like in practice?”, “What did they personally do?”, “What was the outcome?”, or “Can you give a contrasting example?”

### Role-specific probes

Choose probes based on actual job requirements, not personal similarity or culture fit.

| Role area | Example probes |
|---|---|
| Operations or program delivery | How did they handle ambiguous requirements, competing priorities, and repeatable process design? |
| Community or stakeholder work | How did they build trust, handle difficult conversations, identify needs, and follow through? |
| Operational leadership | How did they improve processes, balance speed and risk, and coordinate budgets, suppliers, or cross-functional work where relevant? |
| Technical or analytical work | How did they define quality, explain trade-offs, and revise an approach when evidence changed? |

## 6. Run the call fairly

State the purpose and confidentiality boundary, then ask whether the referee is comfortable speaking candidly within it. Listen for observable behavior, conditions, outputs, and outcomes.

Do not disclose confidential interview judgments, unnecessary details about other referees, or information that pressures the referee to agree with a conclusion. Test concerns neutrally: ask what they observed rather than inviting confirmation of a negative claim.

If a serious concern arises, ask for context, behavior, impact, frequency, support provided, and evidence of improvement. Record it as the referee’s account, not as proven fact. Seek corroboration where appropriate.

## 7. Record and synthesize promptly

Complete the call record while details are fresh. Separate:

- **Direct observations:** what the referee saw, including examples and outcomes.
- **Referee interpretation:** their explanation, comparison, or recommendation.
- **Hiring-team inference:** what the evidence may mean for this role, including uncertainty.

Compare the reference with role-relevant assessment evidence and other references. Look for convergence, meaningful contradictions, and gaps. A single reference should inform a decision, not determine it alone.

## 8. Readiness gate and audit check

Before the call, verify:

- [ ] Purpose, authorization, and access boundaries are clear.
- [ ] The referee’s relationship and direct observation are understood.
- [ ] Role outcomes and decision uncertainties are identified.
- [ ] Only relevant, authorized information was used.
- [ ] The brief includes tailored questions and follow-up angles.
- [ ] Prior themes are attributed rather than stated as facts.

Before relying on the call in a hiring decision, verify:

- [ ] Notes separate observation, interpretation, and inference.
- [ ] Important claims have examples where possible.
- [ ] Unrelated or sensitive details were omitted.
- [ ] Contradictory evidence was investigated rather than ignored.
- [ ] The assessment addresses role-relevant capabilities and role alignment.
- [ ] Record access remains limited to the appropriate hiring group.

## Common failure modes

- **Generic questions only:** produces praise but little evidence. Tailor probes to actual role risks.
- **Over-researching:** increases privacy risk without improving the decision. Use the minimum relevant sources.
- **Leading questions:** invite confirmation rather than reliable evidence. Ask neutrally and request examples.
- **Confusing confidence with observation:** a persuasive referee may still have limited firsthand knowledge.
- **Treating a concern as settled fact:** attribute it, seek context, and compare it with other evidence.
- **Recording labels instead of evidence:** replace “strong communicator” with what they communicated, to whom, under what conditions, and with what result.
- **Leaving findings outside the official record:** put decision-useful evidence and follow-up actions in the designated hiring record, within the appropriate access boundary.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and private data, verifying rendered state, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for tasks requiring real website interaction: completing forms, changing settings, collecting data from rendered pages, testing a flow, or working in an authenticated dashboard. Use it when a static request, supported API, or ordinary page retrieval cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not take a consequential final action until the page state, target, and authorization are clear.

A browser command that reports success does **not** prove that a website accepted the change. Modern web applications may keep internal state separate from the visible DOM, commit data only after focus changes, replace controls during a re-render, or display an error even after an action succeeded.

## 1. Establish purpose, authority, and boundaries

Before accessing a site, identify the requested outcome and its limits:

- What exact page, record, form, setting, or workflow is in scope?
- What information must be entered, collected, changed, or uploaded?
- What is the minimum information needed?
- Is the final action reversible?
- Does the task send, publish, pay, delete, grant access, change a plan, alter security, or create another external commitment?
- Which choices require the user's judgment?

When working with private communications, records, dashboards, or information about people, require a legitimate purpose and clear authorization. Access only the minimum relevant sources and information. Do not copy unrelated sensitive details into logs, screenshots, notes, or reports. Respect consent, privacy expectations, and the appropriate access boundary.

Do not reveal credentials, session cookies, authentication codes, recovery information, private account data, or security settings in output. Do not weaken access controls, multi-factor authentication, browser warnings, or anti-abuse protections to make a task easier.

## 2. Choose the least invasive route

Use the first suitable route below. Do not use a visible authenticated session merely for convenience.

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can complete the task. It is often more reliable than reproducing browser behavior.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, UI testing, and forms that do not require an established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing account session, single sign-on state, account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for a direct route. Check official documentation, ordinary form actions, visible network activity, and page source for supported endpoints. A form may submit structured data to an authorized service that can be used directly.

Do not use undocumented endpoints to bypass access restrictions, consent boundaries, site protections, or applicable terms. If a site blocks automated browsing, do not evade the block for routine research or collection. A verified visible browser may be appropriate only when the user explicitly requested a legitimate task on that specific site, has authorized access, and the established session is necessary.

## 3. Protect browser and account context

When using an authenticated browser, treat account identity and environment as a preflight requirement.

1. Announce that you are taking control of the visible browser and state the purpose.
2. Classify the intended context explicitly, such as personal, work, testing, staging, or production.
3. Select the profile or browser connection for that context directly. Do not rely on a generic browser selector, remembered default, tab title, or connection nickname.
4. Work in a fresh tab, window, or isolated tab group unless the user explicitly directs you to an existing tab.
5. Verify the signed-in account and relevant environment using a reliable account indicator before opening or changing the actual target.
6. Confirm the target record, organization, workspace, or site before making changes.

A useful pre-action question is: **Which account is this? Which environment is this? What exact item will change?** If any answer is uncertain, stop and resolve it before acting.

If the automation system has a verification marker, action gate, or permission state, set it only after the account check has genuinely passed. Never create a verification marker merely to unlock blocked controls.

## 4. Separate preparation from commitment

Separate reversible preparation from final commitment:

- **Preparation:** drafting, filling fields, selecting options, collecting evidence, and configuring a reversible setting.
- **Commitment:** submitting, sending, publishing, purchasing, deleting, changing billing or access, or activating an irreversible change.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify every relevant value, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Re-check account, target, and readiness. Then perform the final action once authorization is present.

Honor an explicit user request to review before submission. For actions that are irreversible, costly, externally consequential, or labeled final or impossible to undo, obtain confirmation immediately before the final control unless the user has clearly and specifically authorized that exact final action. For requested reversible changes, proceed after ordinary verification unless the page shows an unexpected warning or broader impact.

If the page reloads, re-renders, or the session changes between phases, do not assume the prior state remains valid. Re-inspect and re-verify before committing.

## 5. Inspect the rendered page before editing

Do not begin by guessing selectors, using numeric field positions, or trusting a visual approximation. Inspect the rendered page first.

For each relevant control, identify:

- Element type: single-line input, multiline area, rich-text editor, dropdown, checkbox, radio group, date picker, upload, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether the field is required.
- Validation rules, formatting behavior, length limits, and disabled state.
- Whether the apparent field is the true editable control, a wrapper, or a hidden synchronization element.
- Whether changing it may cause the page to re-render or reset dependent fields.

Address controls by semantic identity: visible label, accessible name, stable identifier, or explicit label relationship. Do not address fields by DOM index when labels are available; dynamic applications can reorder elements between loads and after state changes.

Before changing a record or setting, inspect its existing state. This prevents changes to the wrong item and unintended overwrites.

### Generic inspection pattern

Use the selected browser capability to record tag, input type, role, label, required state, and readable value or text length before editing.

```js
// Pseudocode: adapt to the selected automation library.
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

## 6. Use the interaction suited to the control

A generic value-setting command is not reliable for every component. Use normal user-like interaction for framework-controlled controls.

| Control type | Preferred interaction | Key verification concern |
|---|---|---|
| Single-line input | Use ordinary text entry | Newlines may be silently removed. |
| Multiline text area | Fill text, then move focus away | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus the true editable node, select existing text, enter text through keyboard-style events, then blur | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it and select a visible option by text | A selection can trigger a full re-render. |
| Checkbox or radio group | Read state first; change only when needed | A click can toggle an already-correct selection. |
| Date/time picker | Select values, close safely, and read the rendered summary | The popover can clear or reinterpret related values. |
| File upload | Confirm file, destination, audience, and privacy implications first | Upload may begin immediately and be difficult to undo. |

For a rich-text editor, a robust general sequence is: focus the actual editable element, select existing content, delete it, enter replacement text using keyboard-style input, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible editor with a hidden input. Editing the hidden input may appear correct in a DOM dump while validation treats the form as empty. Target the visible interactive control that the application actually reads. If an accessibility locator reaches an empty wrapper, inspect the underlying labeled editable element.

If dropdowns, checkboxes, tabs, or date controls can refresh the form, set and verify them **before** filling lengthy text. Re-inspect afterward and confirm earlier values still exist.

## 7. Verify every meaningful edit

After each field is filled or each setting is changed, read it back from the page. Compare the observed value with the intended value. For sensitive content, use lengths, required-state checks, or a short redacted summary rather than exposing full content unnecessarily.

Look for these mismatches:

- Automation reports success but the field is empty in rendered state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated by a single-line control or length limit.
- A custom editor displayed text but did not retain it internally.
- A later interaction erased an earlier value after a re-render.
- A hidden synchronization field changed instead of the true editor.
- A selection altered a dependent date, recipient, option, or validation rule.

If verification fails, do not continue toward submission. Diagnose the control type, retry once with a more appropriate interaction method, then verify again. If the site continues to reject or alter a value, report the limitation and ask how to proceed. Do not silently submit incorrect content.

## 8. Run a readiness gate before final action

Before submitting or applying a high-impact change, inspect the full relevant state again. Confirm:

- The correct account, organization, environment, and target item are active.
- Every required field is present and non-empty.
- Each entered value matches the intended content closely enough for the task.
- Recipients, options, dates, attachments, access settings, and dependent fields are correct.
- No validation error, warning, or unsaved-change indicator remains.
- The final control has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially filled form can usually be corrected; an incorrect external action may not be reversible.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only within the appropriate access boundary. Do not paste a large table of sensitive values into a chat when a brief summary and securely retained record are sufficient.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists when the action is consequential.
- [ ] The final action and its impact are understood and authorized.

## 9. Confirm completion, not just the click

A final button click is not proof of success. Look for reliable evidence such as a success message, confirmation reference, newly created record, persisted setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect resulting state before retrying. Some visible errors are cosmetic, while blind retries can create duplicate messages, purchases, submissions, or records.

If completion cannot be verified, report what was attempted, the evidence available, and what remains uncertain. Do not present an attempted action as complete.

## 10. Failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation succeeds but the field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier values disappear after a later edit | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | Wrong control type or formatting rule | Find the multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the labeled underlying control and target the true editor. |
| A value looks correct but validation says empty | A hidden synchronization field was edited | Use the visible interactive control that the application reads. |
| The automation layer becomes unstable | The chosen method is unsuitable for the page | Switch to a more robust browser method or supported interface; do not blindly rescue a broken session. |
| Headless and visible browsers differ | The site changes behavior by browser context | Prefer an authorized direct interface; for an explicitly requested task, use a verified visible session without bypassing protections. |
| A popup unexpectedly changes a date or field | The widget has stateful clear, close, or parsing behavior | Close it through a neutral page action and re-verify affected values. |
| A visible error appears after an action | The action may already have completed | Inspect durable resulting state before retrying. |
| Account context is uncertain | Wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
- [ ] Required final authorization was present before commitment.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, validating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing skill, assess whether a skill helps, or improve when it activates. A skill is a focused set of instructions, with optional scripts, references, and templates, that helps an AI perform a recurring job consistently.

The core cycle is:

1. Understand the intended job and its boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with a person and, where suitable, measure objective requirements.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and not narrowly fitted to the tests.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the completed skill.

Do not force every project through every stage. Some users want a quick collaborative draft; others need repeatable tests and comparisons. Identify where the user is in the process, state the recommended next step, and adapt the level of rigor to the task’s importance and repeat use.

## Communication principles

Match the user’s technical knowledge. Use plain English by default. Words such as *evaluation* and *benchmark* are usually acceptable if briefly explained. Avoid unexplained technical terms such as “schema,” “assertion,” or “JSON” unless the user is clearly comfortable with them.

Explain why questions matter. For example:

> What should a successful result look like: a chat response, a structured report, a file, or an approved external action? The answer determines both the instructions and how completion can be tested.

Keep the user involved at meaningful decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before choosing a narrow scope, a required tool, or an approval rule.
- Share proposed test cases before treating them as the evaluation set.
- Let human review lead for subjective qualities such as writing, visual design, tone, usefulness, and judgment.
- Do not imply that a weak or unavailable test is proof of quality.

If the skill uses communications, records, files, or information about people, require a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Omit unrelated personal or sensitive details, respect consent and privacy expectations, and keep outputs within the appropriate access boundary.

## 1. Determine the starting point

First establish which situation applies.

### A. New skill

The user has an idea, such as a recurring report, document workflow, analysis task, or support process. Start with discovery and create a first draft.

### B. Existing skill

The user already has instructions and wants them edited, simplified, tested, or improved. Read the current material before proposing changes. Preserve the established name and identity unless the user asks to change them. If the installed copy cannot be edited safely, make a writable working copy and preserve the original unchanged.

### C. A workflow demonstrated in conversation

A user may say, “Turn what we just did into a skill.” First extract what can be learned from the conversation:

- Inputs and source materials used.
- The sequence of actions and decisions.
- Tools or capabilities used.
- Corrections and preferences the user supplied.
- Output formats and acceptance criteria.
- Points where the process branched because conditions changed.

Summarize the inferred workflow and list gaps for confirmation. Do not silently convert a one-time workaround, private habit, or personal access pattern into a general rule.

### D. Evaluation or triggering request

The user may have a finished-looking skill and ask whether it works, whether a revision is better, or whether it activates appropriately. Start with test design and evidence gathering. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough detail to define a coherent job. Ask only the questions that are still unanswered and materially affect the design.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What requests, phrases, or contexts should cause the AI to use it?
3. **Inputs:** What information, files, examples, systems, or authorized permissions may it use?
4. **Outputs:** What should it produce or change? Is a particular format required?
5. **Success:** How will the user know the result is correct, useful, or complete?
6. **Boundaries:** What should it not do? When should it ask, pause, decline, or hand work back to the user?
7. **Variations:** What common cases, difficult cases, exceptions, or failure conditions matter?
8. **Dependencies:** Does it require a capability, reference source, template, script, or user-provided access?
9. **Testing:** Should it be tested with example requests before release?

Offer useful choices when appropriate:

- “Should the skill make a best effort when information is missing, or stop and ask?”
- “Should it provide a concise result, a detailed report, or let the user choose?”
- “Should it work from any available source, or only sources the user explicitly approves?”
- “Should it prepare a draft only, or may it take an external action after confirmation?”

Recommend test cases when the work is repeated, consequential, objective, file-based, structured, or capable of causing costly errors. For highly subjective work, recommend representative examples and human review rather than pretending there is a complete numerical measure.

### Research before drafting

When available and useful, inspect user-approved documentation, existing skills, templates, standards, and relevant technical guidance. Research should reduce the user’s burden, not replace their authority over requirements.

Use research to find:

- Existing output conventions and quality standards.
- Constraints of relevant file formats or tools.
- Reusable approaches from similar approved workflows.
- Safety, privacy, compliance, or approval requirements.

If evidence conflicts or a requirement is uncertain, identify the uncertainty instead of inventing a rule.

## 3. Choose a maintainable structure

Keep each skill focused enough that a user and an AI can predict what it does. A skill may support related variants of the same task, but separate unrelated jobs when they have different users, permissions, sources of truth, or definitions of completion.

A portable package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed guidance
├── assets/                  # Optional templates and resources
└── evals/                   # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata or registration text:** A short name and description that help route requests.
2. **Core instructions:** The workflow needed in normal use.
3. **Supporting resources:** Details loaded only when relevant.

Keep the core instructions concise enough to be understood as a whole. If they become large, move domain-specific material into clearly named references and state exactly when to consult each one. Give large references a navigation section or table of contents.

For skills with variants, use one shared workflow plus separate variant references. For example, a publishing skill might have distinct references for different output channels. Read only the applicable reference rather than all references by default.

### Add reusable scripts only when justified

If several test runs independently recreate the same helper procedure, consider bundling it as a script. This is especially useful for repeatable conversion, validation, formatting, extraction, or calculation work.

A bundled helper should be:

- Deterministic or easier to verify than a manual procedure.
- Reused enough to justify maintenance.
- Clearly authorized and within the user’s intended scope.
- Documented with inputs, outputs, limitations, and conditions for use.

Do not automate actions that conceal effects, bypass review, exceed authorization, or make irreversible changes without an appropriate confirmation step.

## 4. Write the skill

Draft in clear imperative language. Explain the purpose behind important requirements, especially when a rule prevents a known failure. A capable AI can adapt better when it understands the goal and tradeoff rather than receiving a long list of unexplained commands.

Use these sections as applicable.

### Purpose and scope

State the job, intended audience, normal result, and boundaries. Clarify whether the skill answers in chat, creates a file, changes a system, or guides a person through a process.

### Inputs and prerequisites

List required inputs, approved sources, available capabilities, and optional information. State what to do when a required item is missing.

```markdown
Before preparing the report, confirm the time period and approved source material.
If a required source is unavailable, ask for an export or provide a clearly labeled incomplete draft.
```

### Workflow

Provide the normal sequence of actions and decision points. A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Ask focused questions only when an answer would materially change the work.
3. Gather evidence from approved sources.
4. Perform the task with the appropriate method.
5. Verify the result against the requested format and success criteria.
6. Present the result, assumptions, source limitations, and any unresolved questions.

Use conditional guidance rather than brittle lists of special cases:

```markdown
If the user provides a required template, follow it.
If no template is available, use the default structure below.
If an action could overwrite important work or affect an external audience, describe the impact and request confirmation before proceeding.
```

### Output format

Where consistency matters, define a stable template:

```markdown
# [Title]

## Summary
[Brief overview]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing input]
```

Avoid fixed structures when the task depends on adapting to context. In those cases, describe the outcome goals and include a brief example rather than imposing a rigid shell.

### Quality, safety, and privacy checks

Specify checks before completion: required sections, calculation validation, source attribution, preservation of original data, or clear uncertainty labels.

A skill must act in ways a reasonable user would expect from its description. Do not design instructions that mislead people, enable unauthorized access, extract confidential information, evade safeguards, or damage systems. If a requested action lacks authorization or is unsafe, explain the limit and offer a safe alternative when possible.

For work involving personal records or communications, include these checks:

- Confirm legitimate purpose and access authorization.
- Use the minimum relevant information.
- Exclude unrelated sensitive details from outputs.
- Respect consent, confidentiality, retention, and sharing expectations.
- Do not make consequential judgments about people from irrelevant or insufficient information.

### Failure behavior

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or source:** Explain what cannot be verified and offer an alternate path.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, label the limitation, or request guidance.
- **High-impact action:** Pause for confirmation before irreversible, external, or consequential changes.

## 5. Write a strong activation description

The short description is primarily routing guidance. It should say both what the skill does and when it is relevant. Include realistic ways users might imply the task without naming the skill.

A useful pattern is:

> Create clear project status reports from approved updates and source material. Use for requests involving progress summaries, milestone reviews, risks, next steps, or leadership updates, even when the user does not say “status report.”

Make the description broad enough to catch valid variations, but not so broad that it captures adjacent work better handled by another skill. Put detailed procedure in the body, not in the description.

## 6. Review before testing

Read the draft as if encountering it for the first time. Check:

- Is the job coherent and appropriately bounded?
- Does the description explain when to activate it?
- Are required inputs, permissions, outputs, and approval points clear?
- Does the workflow explain important quality and safety checks?
- Does it say what to do when information is missing?
- Are there unnecessary rules, duplicated guidance, or brittle wording?
- Does it avoid private conventions, hidden access assumptions, and personal terminology?
- Does it give the AI enough flexibility for normal variation?

Prefer lean instructions. Repeated capitalized prohibitions are a warning sign unless the instruction protects a genuine safety, privacy, or authorization boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create two or three realistic prompts. Share them with the user before running them, and invite additions or corrections.

For each test case, keep:

- A descriptive name.
- The prompt.
- Supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

A portable record format is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates. Clearly flag information that cannot be verified.",
      "expected_output": "A structured summary separating supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful variation:

- A normal successful request.
- Incomplete or ambiguous input.
- A format-sensitive or rule-sensitive case.
- A realistic condition that changes the workflow.
- A permission, privacy, or approval boundary when relevant.

Do not test only phrases copied from the skill. Vary wording, detail level, and user sophistication. Avoid retaining personal scenarios or confidential examples when generalized cases teach the same lesson.

## 8. Run comparisons and retain evidence

When the environment supports independent execution, compare the skill with a meaningful baseline:

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revision against that version or another explicitly chosen baseline.

Start all comparable runs under similar conditions. If parallel execution is available, launch skill and baseline runs together for each test. Store outputs by iteration and descriptive test name, for example:

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

For every run, retain the prompt, relevant supplied inputs, outputs, and available execution metadata such as time and resource use. Record timing when it is reported because some systems do not preserve it later.

If independent runs are unavailable, perform a transparent sanity check: follow the skill for each prompt, save the outputs, and ask the user to review them. Do not claim this is an unbiased baseline comparison.

## 9. Define and grade objective checks

While tests run, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A file opens and includes required fields.
- Calculations match a known source within an agreed tolerance.
- Missing mandatory inputs are identified.
- Claims include required source references.

Store each grade with a clear statement, pass/fail result, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section lists unavailable data and requests it."
    }
  ]
}
```

Use automated checks when practical. They are more repeatable than visual inspection. Do not force numerical checks onto subjective work; human review is often the right method for tone, usefulness, aesthetics, and strategic quality.

## 10. Review results with a human

Present outputs and measurements through any accessible review method: a review interface, shared files, or a clear conversational comparison. Prefer a standard review capability when one is available rather than creating a custom interface without need.

For each test case, show the prompt, relevant inputs, each output, objective grades with evidence, and timing or resource data if available. Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add work or detail that did not help?
- Would this work for similar requests with different wording or inputs?

Empty feedback can mean the case was acceptable, but it is not proof that all cases are solved. Review outputs and measurements as well.

## 11. Analyze beyond pass rates

Aggregate pass rates, time, resource use, and variation when possible. Then look for patterns that summary numbers hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill’s value.
- **High variance:** Similar runs differ sharply, suggesting unclear instructions or unstable conditions.
- **Tradeoffs:** Quality improves but time or resource use becomes excessive.
- **Failure concentration:** Multiple failures have one root cause.
- **Unproductive work:** Execution traces show redundant planning, research, or formatting.
- **Repeated reconstruction:** Multiple runs rebuild the same helper procedure, suggesting a reusable asset.

Use a small benchmark as evidence for the next revision, not as conclusive proof.

## 12. Improve without overfitting

Revise based on feedback, outputs, and analysis. Change the smallest part likely to address the underlying cause.

If one test omitted source notes, do not add a rule tied only to that exact example. Clarify the general condition: when evidence is incomplete or mixed, distinguish verified content from assumptions and unknowns.

Apply these principles:

1. Fix causes, not examples.
2. Keep instructions lean; remove guidance that does not improve outcomes.
3. Explain intent, especially for quality, safety, or user-experience requirements.
4. Add scripts, templates, or references only when repeated use justifies them.
5. Preserve behaviors users already value.
6. Add tests only for real classes of failure, not every isolated incident.

After revision, run the full evaluation set in a new iteration, using the same baseline policy. Where possible, show prior and current outputs side by side. Continue until the user is satisfied, feedback is consistently positive, objective requirements are reliably met, or further instruction changes no longer produce meaningful improvement.

## 13. Optional blind comparison

For a more rigorous comparison, give two outputs to an independent reviewer without saying which version produced each one. Ask the reviewer to judge with a shared rubric, then reveal the mapping only after the judgment is recorded.

Use blind comparison when versions have similar measured results, qualitative judgment is important, or a decision has material consequences. Tie the rubric to user value: correctness, completeness, clarity, adherence to constraints, safety, and practical usability.

## 14. Optimize activation behavior

After the skill itself is stable, test its routing description. Create a balanced set of realistic queries that should activate the skill and difficult nearby queries that should not.

Positive cases should vary in formality, wording, detail, and whether they name the task directly. Negative cases should be meaningful near-misses: requests sharing keywords or context but requiring another workflow.

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

Review the query set with the user before using it. If the environment supports repeated routing tests, separate examples used to improve the description from held-out examples used to select it. Choose the description that works best on held-out cases, not merely the examples used during editing.

Simple requests may not activate a specialized skill even when the wording matches, because an AI can handle a simple task directly. Make routing tests substantive enough that consulting the skill would provide real value.

## 15. Package and hand off

Package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not rely on undeclared tools, private conventions, or hidden access.
- Scripts and references are present, clearly named, and documented.
- No credentials, confidential data, personal identifiers, or sensitive examples remain.
- The user can install or adapt the package in their chosen environment.
- Retained test material is safe and useful.

Provide a short handoff note covering what the skill does, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, appropriate activation guidance, instructions that handle normal variation, explicit rules for uncertainty and authorization, and evidence from realistic use that it improves results.

Do not mistake a long instruction file for a reliable skill. The goal is a reusable workflow that helps an AI make sound decisions and deliver better results for recurring real-world work.


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

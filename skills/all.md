# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice. Use this workflow when a user asks to brainstorm approaches, explore possible.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not to create a long list of ideas; it is to surface genuinely different paths, make tradeoffs clear, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources that are available in the current environment, review the relevant material first.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the recommendation, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, deadlines, or budgets
- Stakeholder concerns, responsibilities, and approval boundaries
- Evidence about what has already been tried
- Comparable outcomes, customer feedback, or operational data

Use targeted retrieval rather than broad searching. Where sources contain personal or confidential information, access them only with a legitimate purpose and clear authorization. Use the minimum relevant information, omit unrelated sensitive details, and keep the response within the appropriate access boundary.

If important context is unavailable, either state the assumption being made or ask a focused question. Do not invent missing facts.

## 2. Frame the decision before ideating

Write a short framing of the decision, usually two to four sentences. It should identify:

- What the user is actually deciding
- The key constraints and non-negotiables
- What a good outcome looks like
- The criteria by which options should be compared

The user's first wording may describe a symptom or a proposed solution rather than the underlying decision. For example, “Should we add a feature?” may actually mean, “How should we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the framing is obvious, the choice is low-stakes, or the user explicitly requests an immediate first pass. A wrong framing produces polished but irrelevant options.

### Framing template

> **Decision:** [What must be chosen or resolved?]
>
> **Constraints:** [Budget, time, risk, dependencies, permissions, or other limits]
>
> **A good outcome:** [What success looks like]
>
> **Evaluation criteria:** [For example: impact, speed, cost, reversibility, risk, strategic fit]

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes the process, incentives, scope, ownership, or problem framing
- At least one surprising option, such as delaying, partnering, removing scope, running an experiment, or deliberately doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when waiting, observing, preserving capacity, or avoiding a premature commitment has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

| Element | Include |
|---|---|
| **What** | One or two sentences explaining the approach. |
| **Strengths** | One or two concrete advantages. |
| **Weaknesses** | One or two concrete disadvantages, risks, or limitations. |
| **Effort** | Low, Medium, or High; use a rough estimate of work, coordination, and time. |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option appear stronger by describing alternatives unfairly.

### Option format

#### [Short option label]

- **What:** [Describe the approach.]
- **Strengths:** [Concrete benefits.]
- **Weaknesses:** [Concrete costs, risks, or limitations.]
- **Effort:** [Low / Medium / High]

## 4. Evaluate and recommend

Select evaluation criteria that fit the decision. Common criteria include likely impact, effort, cost, speed, risk, reversibility, strategic fit, stakeholder burden, and learning value. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are instructive, but state clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this user's specific situation, constraints, and goals—not merely why it is generally attractive.
4. Name the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice when several options are credible.

### Recommendation format

1. **[Option label]** — Best fit because [specific connection to the user's constraints and goals].
2. **[Option label]** — Strong alternative because [specific tradeoff it handles better].
3. **[Option label]** — Best if [condition or priority changes].

**Not recommended now:** [Option label], because [dealbreaker weakness].

**Ranking-changing assumption:** [The fact, estimate, or priority that would alter the recommendation].

## 5. Stop for a decision

After presenting recommendations, wait for the user's response. They may:

- Select an option
- Request more detail on an option
- Correct the framing or constraints
- Ask for additional or different options
- Propose a hybrid approach

If the user proposes a hybrid, check whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity.

Do not begin implementation merely because an option appears promising. Move into execution only after the user selects or explicitly authorizes a path.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing choices, or decisions with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record that states the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choice:** After the decision is recorded, move into planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify:

- The framing reflects the actual decision rather than only the user's initial phrasing.
- Any contextual retrieval was necessary, authorized, and limited to relevant information.
- The options are genuinely distinct rather than variations in scale.
- The obvious option and at least one meaningfully different option are represented where appropriate.
- Strengths and weaknesses are concrete, balanced, and candid.
- Effort labels reflect both execution work and coordination burden.
- Eliminations are tied to stated constraints rather than hidden preferences.
- Recommendations are tailored to the user's criteria.
- The response preserves the user's decision authority and does not begin implementation prematurely.


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
3. Make and document the decision with rigor that matches its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing a single idea too early can become an exercise in defending it.

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.

## Rules of engagement

- Be direct. Do not treat confidence as evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Use available, authorized evidence: research, metrics, prior experiments, customer feedback, documented decisions, or stakeholder input. Distinguish facts from inferences and forecasts.
- If reviewing private communications or records, have a legitimate purpose and clear authorization. Use only the minimum relevant material, omit unrelated sensitive details, and keep findings within the appropriate access boundary.
- Refer to relevant dissenters by role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's actual intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, starting with the assumption most likely to undermine the decision.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Name a test or disproof condition] |

Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions, and adapt later questions to the answers received. Do not present the full set as a questionnaire, because that permits selective answering.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed? Why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence. Ask what observed behavior, data, comparison, or commitment supports that belief.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution risks, external conditions, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable signal] | [Name the check or accountable role] |

Warning signs must be observable early enough to permit a course correction.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap; do not assume silence means agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next step:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data collection period. Next: run that test, then make the decision with its result recorded.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, the downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with exactly one concrete next action: a verb, an owner, and a deadline when useful.

Example: `Research owner: interview five target users this week and compare results against the adoption assumption.`

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

Use this workflow to make decisions with the right amount of rigor. The aim is not exhaustive analysis. It is to make a clear call when ready, preserve reasoning for meaningful choices, and learn from outcomes.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may recommend an option in conversation, clearly labeled as assistant analysis. Put that analysis in a decision record only if the user asks for it.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution. Plan or start the task instead of opening a decision process.
5. **Record only with permission.** “Should we do X?” asks for analysis, not creation of a record. Create or update a decision record only when the user asks to log, track, open, or commit it, or explicitly agrees to the practice.
6. **Protect privacy and access boundaries.** Before accessing shared communications, personnel records, customer data, or a shared decision register, ensure there is a legitimate purpose and clear authorization. Use only the minimum relevant information, omit unrelated sensitive details, and respect consent and expected visibility.
7. **Do not deliberate forever.** Once the required evidence, consultation, and challenge steps are complete, name the decision and move forward.

If a shared register has an audience beyond the decision-maker, confirm that audience is appropriate before writing to it. For sensitive subjects such as health, relationships, compensation, or confidential personnel matters, offer a private record or keep the discussion in chat.

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
- What are the realistic options, including doing nothing where relevant?
- What is the deadline or decision trigger?
- What result is desired?
- What happens if no action is taken?

If the question is broad and no credible options exist yet, generate options before evaluating them. Do not pressure-test a vague problem statement.

If only one viable path exists, say so directly:

> This appears to be a task rather than a decision. The next step is to plan or execute it.

## 3. Classify scope

Ask one clarifying question at a time when needed. Put the choice in one bucket.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, consult relevant stakeholders |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and named prerequisite conversations |

Use this test if classification is unclear: **What would it cost to unwind this?** Consider money, time, trust, operational disruption, opportunity cost, legal or contractual exposure, and reputational effects. If the cost cannot be stated quickly or is uncertain, the decision is probably larger than it first appears.

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: continued attention may cost more than an imperfect choice. Do not create a record by default.

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

For hiring or assessment decisions, focus on role-relevant capabilities, role alignment, evidence from the assessment, and whether the assessment distinguishes relevant performance. Avoid unsupported conclusions based on personal characteristics or irrelevant private information.

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
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only stopping point when requested.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, automation, or operational problem whose solution is not already clear. Do not use it for a small fix or a routine task with a known implementation path.

By default, work from understanding through implementation and handoff. If the user requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start from the underlying problem, not the user's proposed solution. If they ask to “build X,” work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today?
- What workarounds exist?
- How frequent, costly, urgent, or blocking is the issue?
- What outcome would materially improve the situation?

Write a concise problem statement and descriptive requirements. State desired outcomes, constraints, and success conditions without prematurely assuming an implementation. If the proposed solution does not address the underlying problem, say so clearly.

Ask only for information that cannot be found in authorized, relevant project context. When consulting private records or communications, have a legitimate purpose and clear authorization, use the minimum relevant material, and exclude unrelated or sensitive personal details.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, alternatives, and maintenance burden. Treat “do nothing,” “deprioritize,” or “improve the current workaround” as valid options when appropriate.

Separate decisions by reversibility:

- **Reversible decisions:** Small choices that are cheap to change. Use reasonable judgment and proceed.
- **Hard-to-reverse decisions:** Persistent data changes, public interfaces, long-lived settings, migrations, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the decision will matter later.

If priority or direction is unclear, present the tradeoff and obtain a decision before investing heavily in design or implementation.

## 3. Research the current context

Review relevant instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns, reusable components, and constraints before designing something new.

Identify compatibility requirements, deployment practices, security expectations, supported environments, ownership boundaries, monitoring, and rollback limits. Follow existing conventions unless there is a clear reason not to.

## 4. Define evaluation criteria

Set explicit, lightweight criteria before generating options. For example:

- Must preserve existing authentication, privacy, and data behavior.
- Must fit available time and maintenance capacity.
- Should avoid unnecessary dependencies or durable configuration.
- Must have a clear verification method.
- Should be removable or reversible if it performs poorly.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the workaround.
2. A non-code solution: clearer guidance, a process change, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For ambiguous problems, generate a broader candidate set before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that vary with runtime conditions.
- Validate strictly and fail fast for invalid states. Do not hide programmer errors by returning plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Make clean changes in the appropriate design boundary; avoid quick fixes that create future debt.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal with:

- Problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep the proposal direct. Store it in the user's chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear date-prefixed title, such as `29 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Check results against the evaluation criteria, including compatibility, privacy, security, and failure behavior.

Do not claim success based solely on implementation. State what was tested, what passed, and what remains unverified. Commit, publish, or deploy only according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user action, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail rather than temporary implementation notes.


---
name: shape-and-draft
description: Shape consequential documents by gathering evidence, resolving material choices through answer-dependent interviews, applying a readiness gate, and auditing the smallest draft that can achieve the intended result.
---

# Shape and draft a document

Develop a consequential document by shaping the underlying thinking before writing it. First determine what the document must achieve, gather relevant evidence, resolve material choices with the appropriate decision-maker, and then draft the smallest document that can do the job.

Use this workflow for strategies, narratives, operating agreements, proposals, scorecards, decision memos, and similar documents when the argument, scope, commitments, or operating model are unsettled. Do not use the full process for a simple edit, formatting task, or document whose key decisions are already clear.

## Classify the request

A request may name a document type, audience, outcome, or source material. Treat the named document type as a hypothesis until its purpose is clear.

Use a **full shaping process** when the document is important enough that unresolved choices could change its substance, or when the requester asks for deep thinking, multiple question rounds, or close alignment before drafting.

A substantive interview round resolves a distinct layer of choices and uses the answers to determine the next round. Restating earlier discussion or asking for general approval is not a substantive round.

## 1. Work backwards from the outcome

Start with the change the document needs to produce. Establish:

- Who will read it.
- What they should understand, decide, approve, or do afterward.
- What is unclear, contested, blocked, or going wrong now.
- Whether the document mainly needs to explain, persuade, decide, coordinate, or govern.

Do not accept “write a strategy” or “make a narrative” as the goal. Identify the job the document must perform.

## 2. Choose the artifact

Recommend the document form that best serves that job:

- **Narrative:** Builds shared understanding of why something matters and what bet is being made.
- **Strategy:** Connects a diagnosis to choices, priorities, intended outcomes, and exclusions.
- **Operating agreement:** Defines ownership, decision rights, interfaces, handoffs, and working cadence.
- **Decision memo:** Records a choice, alternatives, rationale, risks, and a review point.
- **Scorecard:** Defines a role or team mission, outcomes, and role-relevant capabilities.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the meaningful tradeoff and recommend one form. If the artifact choice would materially change the argument or structure, ask the authorized decision-maker to confirm it before proceeding.

## 3. Gather and classify evidence

Read supplied material first. Follow any stated rules for source authority, citations, links, and delivery. Scale research to the stakes.

When using private communications, internal records, or information about people, confirm there is a legitimate purpose and clear authorization. Use the minimum relevant information and sources. Exclude unrelated sensitive details, respect reasonable privacy and consent expectations, and keep notes and outputs within the appropriate access boundary.

For a consequential internal document, seek evidence that may contain prior decisions, current definitions, supporting evidence, constraints, dissent, ownership context, and relevant performance information.

Apply these rules:

- Respect a stated source-of-truth hierarchy.
- Prefer current, authoritative decision records over discussion notes, recollections, generated summaries, or repeated claims.
- Resolve contradictions where evidence permits, and surface material contradictions that remain.
- Do not ask people for facts that authorized available sources can answer.
- Do not modify source material unless explicitly instructed.

Keep evidence separate from alignment:

- Sources can establish what happened, what was recorded, what people said, and what an authoritative record currently states.
- Sources do not automatically establish what the current decision-maker believes, is willing to promise, or chooses to exclude.
- A plausible synthesis, repeated pattern, or implication is an **inference**, not a settled decision.
- Ask for confirmation before using a material inference as a central claim, commitment, boundary, recommendation, or operating rule.

Before the first interview round, provide a short situation brief that states:

- What the sources establish.
- What has already been explicitly confirmed.
- What is inferred but unconfirmed.
- The main tension, gap, or missing logic.
- The recommended artifact.
- The important choices that only the decision-maker can resolve.

## 4. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds already completed in the conversation. Do not repeat settled questions.

Do not draft immediately after the first round just because one central issue appears resolved. Use the next round to test implications: scope, boundaries, counterarguments, ownership, definitions, handoffs, or measures.

Ask four to eight focused questions per round. If fewer than four material questions remain, ask only those and say that it is a narrow final check. Do not add ceremonial questions merely to reach a number.

Each numbered question should normally seek one decision. Do not combine independent choices, such as ownership, coordination, and success measures, into one broad question. Bundling creates false alignment.

Use one clear answer surface per round. In a conversation, provide the updated situation and a plain-text numbered question block together so the respondent can answer in shorthand. Do not duplicate the same questions in chat and another form unless the requester requires that format. If a structured form is necessary, include enough context to answer each question and treat actual answers, rather than interface status, as the record of progress.

Format questions for quick, unambiguous answers:

1. Number questions continuously and keep each number tied to the same decision.
2. For bounded choices, use lowercase option labels such as `a.`, `b.`, `c.`, and `d.`.
3. Default to three or four mutually exclusive, decision-relevant options. Use two only when there are truly two states.
4. Put the recommended option first unless prior context makes another order clearer.
5. Keep the block compact, with questions and options on consecutive lines and no blank lines inside it.
6. Let the respondent reject the framing or provide a different answer.

Example:

1. Which direction should the document recommend?
   a. Focus first on the highest-impact problem; this narrows scope but clarifies accountability.
   b. Address the related problems as one coordinated program.
   c. Present options without a recommendation.
2. Who should hold the final decision right?
   a. One accountable lead, with required input from affected groups.
   b. A standing cross-functional group.
   c. A senior sponsor after written input from the accountable lead.

Each round should:

1. Start with an updated model and state what changed because of earlier answers.
2. Focus on one layer of uncertainty rather than mixing every issue at once.
3. Explain the tradeoff behind recommended options.
4. Separate source-supported observations from choices the decision-maker must make.
5. Surface contradictions and ask the smallest question needed to resolve them.
6. Include a pressure test when the document is persuasive or strategically consequential.
7. Leave room for an answer outside the offered framing.

A common progression is: purpose and audience; strategy and scope; operating model; definitions and measures; then expression, format, and destination. Adapt the sequence to the task, but preserve the answer-dependent loop.

After every answer round:

1. Match shorthand and free-text replies to question numbers, preserving qualifications such as “mostly c” or “not sure.” Classify answers as confirming, rejecting, softening, qualifying, or deferring the proposed position.
2. Mark only genuinely unanswered or unclear material choices as open.
3. Trace downstream implications. A softened commitment, new exception, or changed audience may create a new material question.
4. Update the alignment ledger and show a concise synthesis.
5. Generate the next round from remaining uncertainties and their consequences.

Continue while an unresolved issue could materially change the document. If the requester asks to draft early, name the one or two most important consequences of the remaining uncertainty, then follow the instruction.

## 5. Maintain an alignment ledger

Keep a compact working record throughout the process:

- **Confirmed:** Choices explicitly made by the authorized decision-maker.
- **Source facts:** Claims established by current, authoritative evidence but not chosen as current direction.
- **Inferred:** Plausible interpretations that remain unconfirmed.
- **Open:** Questions that could materially change the document.
- **Corrected:** Assumptions or claims that someone has rejected.

Update the ledger after every answer round. Never reintroduce a corrected assumption. If confirmed statements conflict, surface and resolve the conflict rather than hiding it in vague language. Never promote an inference to confirmed merely because several sources support it.

For a full shaping process, show a concise ledger before each later round so the decision-maker can correct misunderstandings. Every major claim in the draft must be a confirmed choice, a supported source fact, or explicitly framed as a proposal, assumption, or open question.

## 6. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document’s substance. Before drafting, provide a concise pre-draft synthesis covering the document’s intended job, audience, central position, important boundaries, and deliberate open questions.

For every major planned claim, ask:

> Was this confirmed by the decision-maker, established as fact by authoritative evidence, or merely inferred?

If a material claim is only inferred, ask another question or label it as a proposal. Do not present it as settled.

Check that each relevant category is confirmed, evidence-based, deliberately open, or not applicable:

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
- Has the proposed response been confirmed or supported?

Close alignment means remaining uncertainty is low impact or clearly represented as unresolved. It does not require artificial certainty.

## 7. Draft and deliver

Follow the requested voice, style, accessibility needs, format, and delivery requirements. Where no style is specified, use clear, direct language appropriate to the audience.

Write the smallest document that accomplishes the agreed purpose. Prefer clear claims, concrete decisions, explicit ownership, and clear boundaries over polished but vague language. Distinguish current decisions from proposals, assumptions, and future review points.

Use these writing rules:

- Prefer common words over formal or inflated language.
- Write complete, natural sentences. Keep a clear line of thought in each sentence without splitting connected ideas into fragments.
- State the point first. Remove warm-up text, repeated context, process narration, and qualifications that do not affect a decision.
- Turn abstractions into concrete claims, actions, examples, owners, dates, or tests where useful.
- Use focused paragraphs and bullets only for real lists. Write bullets as full sentences unless they are compact labels.
- Keep action-oriented sections short. Combine related points, move supporting detail to an appropriate reference, or remove lower-value detail rather than creating a long flat inventory.
- Preserve difficult ideas when they matter, but explain them in plain language.

Honor the requested destination using the chosen system. If text is requested in the conversation, do not change source material. If a document must be created or updated elsewhere, do so only as instructed and verify the intended content is present. When rendering or converting a document, inspect headings, lists, indentation, spacing, and page breaks so headings do not inherit list formatting and empty paragraphs do not create awkward gaps.

## 8. Audit before delivery

Compare the draft with the alignment ledger and source hierarchy:

- Does it solve the agreed problem in the agreed form?
- Does every material choice reflect confirmed decisions?
- Have corrected assumptions been removed?
- Are responsibilities, boundaries, decision rights, and handoffs clear where relevant?
- Are uncertain claims labeled appropriately?
- Are factual claims and citations supported by appropriate sources?
- Is any inference presented as settled fact or decision?
- Does the document match the requested audience and voice?
- Can each sentence be understood on the first read?
- Can any abstract phrase, inflated word, or repeated point be simplified or removed?

Fix mismatches before delivery. Put the deliverable last, without trailing commentary that interferes with copying or use.

## Failure modes to avoid

- Drafting early because producing text feels productive.
- Treating a proposed artifact as fixed before its purpose is known.
- Asking for facts that available evidence can answer.
- Mistaking extensive research for alignment on current choices.
- Treating a plausible synthesis as a confirmed decision.
- Using a generic questionnaire disconnected from evidence and previous answers.
- Failing to update the model after each round.
- Stopping after one round without testing consequences.
- Bundling independent decisions into one question.
- Repeating answered questions or duplicating them across answer surfaces.
- Hiding contradictions through vague language.
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

Help a learner understand, retain, and use a provided paper, article, post, or topic through a rigorous dialogue. Prioritize active recall and reasoning over explanation. The learner should do most of the intellectual work; the tutor guides, diagnoses, and raises the level of challenge.

## Learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to recall and reconstruct ideas in their own words.
- **Ask for mechanisms.** Move beyond conclusions by asking why, how, under what conditions, and with what evidence an idea works.
- **Make the learner generate connections.** Ask for their own examples, analogies, predictions, and uses before offering any.
- **Use productive difficulty.** Challenge the learner enough to require thought, but not so much that they cannot make a meaningful attempt.
- **Practice transfer.** Move from the original material to unfamiliar cases, related ideas, and real decisions.
- **Surface gaps through questions.** When an answer is incomplete or inconsistent, ask questions that help the learner notice the problem. Explain directly only after they have had a fair chance to reason it through.

## Conversation workflow

### 1. Establish prior knowledge and a learning target

Start by asking what the learner already knows, believes, or has experienced about the topic. Identify their purpose, such as understanding an argument, preparing for a discussion, applying a method, or evaluating a claim.

Ask one or two open questions:

- “What do you already think is true about this topic, and why?”
- “What are you hoping to be able to explain or do by the end?”

Use the response to identify useful background knowledge, likely misconceptions, and an appropriate level of challenge.

### 2. Elicit the central claim from memory

Ask the learner to explain the main argument, finding, or idea without quoting the source.

Useful prompts:

- “In your own words, what is the main claim?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “If you had 30 seconds to explain it to a thoughtful friend, what would you say?”

If the learner has not read or engaged with the material, ask for an initial prediction or working model. Then ask them to inspect the relevant section and return to explain it from memory.

### 3. Choose a few high-value ideas

Do not try to cover every detail. Select two or three ideas that are central, difficult, consequential, or likely to be misunderstood. Explore each idea with this cycle:

1. Ask the learner to state or reconstruct the idea.
2. Probe their reasoning, evidence, assumptions, and causal story.
3. Ask them to generate an example, comparison, or application.
4. Test the idea with an objection, boundary case, or alternative explanation.
5. Adapt the next question to their answer.

Keep turns brief. Usually ask only one or two questions at a time.

## Question toolkit

Choose questions that require explanation rather than recognition. Adapt wording to the learner’s level and the material.

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

Avoid yes-or-no questions unless they are immediately followed by a request for reasoning.

## Responding to answers

Be warm, direct, and specific. Do not use generic praise. When an answer is strong, identify what made it useful—for example, it named an assumption, distinguished correlation from causation, or supplied a relevant counterexample—then extend the challenge.

When an answer is incorrect or incomplete:

1. Do not immediately provide the correction.
2. Point to the tension with a focused follow-up question.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, give a concise explanation of the missing distinction or reasoning step.
5. Ask them to restate the corrected idea in their own words or apply it to a fresh case.

If the learner says they do not know, invite a low-stakes attempt: “Take a guess based on what you do know. What seems most plausible, and why?” Offer a hint after an attempt, or sooner when the task requires knowledge they have not been given.

## Calibration and pacing

Increase difficulty when the learner answers easily: ask for a counterexample, comparison, prediction, or application in a new domain. Reduce difficulty when they are lost: narrow the question, isolate one assumption, use a simpler case, or ask them to choose between competing explanations and defend a choice.

Match the learner’s energy. When they are engaged, pursue the reasoning in more depth. When they are tired or overloaded, consolidate the strongest ideas rather than introducing more material.

Maintain a dialogue rather than a quiz. Questions should build on the learner’s actual responses, not follow a fixed test sequence.

## Progress checks and audit

Periodically provide a brief, evidence-based assessment:

- What the learner has demonstrated they understand.
- What remains uncertain, incomplete, or confused.
- The most useful next focus.

Do not treat recognition of a term or repetition of a conclusion as mastery. Look for accurate explanation, sound reasoning, and transfer to a new case.

Before moving on, check that the learner can do at least one of the following for each major idea: explain its mechanism, identify an assumption, give an example, respond to a plausible objection, or apply it in a different setting.

## Closing gate

Before ending, ask the learner to turn learning into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation or create a future retrieval prompt. End by naming the next concept or question worth revisiting.

## Guardrails and failure modes

- Do not summarize the material unless the learner explicitly requests it; even then, first invite their own summary.
- Do not lecture when a well-chosen question can make the learner retrieve or infer the point.
- Do not define jargon automatically; ask the learner to define it first, then clarify if needed.
- Do not make the interaction easy merely to be encouraging.
- Do not cover an entire source superficially when a few core ideas can be understood deeply.
- Do not turn challenge into frustration: when repeated attempts show that a prerequisite is missing, give a small scaffold and resume retrieval.
- Do not treat the dialogue as a performance test. Its purpose is to develop understanding, reveal uncertainty, and support durable learning.


---
name: write-in-my-voice
description: Draft or revise email in the user’s voice by using an approved style profile or relevant sent examples, then checking facts, commitments, tone, and brevity before producing copy-ready text.
---

# Write in my voice

Use this workflow when the user asks to draft, reply to, revise, or polish an email on their behalf.

## Goal

Produce a concise, copy-ready email that sounds recognizably like the user while remaining appropriate for the recipient and situation. Match the user’s established writing patterns without inventing facts, commitments, or personal sentiment.

## 1. Load the voice profile

Before drafting, review the user’s current writing profile in full, if one is available. A profile may include:

- Usual greetings and sign-offs.
- Preferred level of formality and warmth.
- Typical email length, sentence rhythm, and paragraph structure.
- Preferred vocabulary, contractions, punctuation, and formatting.
- Phrases, tones, or punctuation to avoid.
- Standard facts, approved links, reusable replies, and role or scheduling information.

If authorized to access the user’s sent messages or drafts, use only the minimum relevant examples needed to understand their voice. Prefer recent examples and examples addressed to a similar audience. Do not expose unrelated private details from those messages.

When a current profile conflicts with old examples, follow the current profile. When evidence is inconsistent, ask the user which pattern they want.

## 2. Establish the email brief

Identify the minimum details required to write safely:

1. Who is receiving the email, and what is their relationship to the user?
2. What outcome should the email produce?
3. What facts, dates, links, attachments, decisions, or requests must be included?
4. How warm, direct, or formal should it be?
5. Are there deadlines, sensitivities, approvals, or commitments that need special care?

Ask a focused clarifying question only when a missing answer could materially change the message. Do not invent availability, prices, decisions, promises, names, links, attachments, opinions, or emotional reactions.

## 3. Adapt the voice to the situation

Keep the user’s recognizable style, but adjust for relationship and stakes.

- **Familiar working relationship:** Use the user’s usual concise and natural pattern.
- **New, external, senior, or formal recipient:** Preserve the user’s voice while adding enough context and clarity for the recipient to act.
- **Sensitive, corrective, or declining message:** Be direct, respectful, and factual. Avoid defensive explanations, exaggerated praise, or apologies that the user did not intend.
- **Request or follow-up:** State the requested action, responsible party, and timing clearly.

Use approved reusable language, links, and facts when relevant. Do not force a standard response into a context where it would be inaccurate or misleading.

## 4. Draft the smallest complete email

Use the user’s normal greeting and closing where supported by the voice evidence. A reliable structure is:

1. Greeting, when appropriate.
2. Purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Closing and sign-off, when appropriate.

Keep the message short unless the subject genuinely requires detail. Prefer active verbs, concrete language, short sentences, and short paragraphs. Use bullets only when they make actions, choices, or logistics easier to scan.

Remove anything that does not help the recipient understand or act, including:

- Generic opening filler or unnecessary process narration.
- Repeated thanks, hollow praise, or excessive flattery.
- Unnecessary hedging that weakens a clear message.
- Explanations of how the email was drafted.
- Decorative language, punctuation, or formatting that does not match the user’s voice.

## 5. Audit before presenting

Review the draft line by line:

- Does it sound like the user’s actual writing?
- Do the greeting, sign-off, pacing, and punctuation match the voice evidence?
- Is the tone appropriate for this recipient and the stakes?
- Are all names, dates, links, attachments, and references accurate?
- Did the draft add any claim, promise, decision, opinion, or emotion not supplied by the user?
- Is the requested action or next step easy to find?
- Can any sentence be removed without losing useful meaning?
- Does the draft avoid the user’s stated style anti-patterns?

## Output

Provide the final email as copy-ready text. If a material detail is missing, ask only the specific question needed to complete the draft safely. Do not add commentary after the email unless the user requests alternatives, reasoning, or a revision.

If no voice profile or examples are available, say so briefly and use a broadly useful default: concise, clear, warm-professional, and direct. Invite the user to provide a few approved examples or explicit preferences for better future matching.


---
name: professional-social-post
description: Draft, revise, and audit professional social posts from source material or a topic, using concrete hooks, defensible claims, useful substance, and targeted iteration for a defined audience.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a rough draft, an article, a transcript, a podcast, a research finding, a launch, or a simple topic.

The goal is not to make an announcement sound enthusiastic. The goal is to make the right reader stop, understand a useful point, and have a reason to care. Write for a defined professional audience with low tolerance for fluff, generic inspiration, vague claims, and empty engagement prompts.

This is platform-independent. Before drafting, confirm the following when they are not already clear:

- **Platform and format:** Text post, caption, document carousel, thread, image caption, or article promotion.
- **Audience:** For example, technical practitioners, founders, policy professionals, researchers, customers, operators, or job candidates.
- **Purpose:** Share an insight, explain a concept, announce a concrete change, promote a longer piece, start a substantive discussion, or support a campaign.
- **Voice constraints:** Formal or conversational, first-person or organizational voice, preferred words, forbidden words, punctuation preferences, and target length.
- **Evidence and permissions:** What sources support factual claims, and what names, quotes, outcomes, images, or personal details may be shared.
- **Link plan:** Whether an external link is needed and where it should appear under the chosen platform strategy.

If the user has an existing writing guide, approved posts, brand guidance, audience research, or prior examples, use those as the source of voice rules. Do not assume a particular person’s voice, publishing tool, distribution tactic, or access to private files.

## Routing and scope

Some post types need their own structure. Identify the genre before drafting.

- **Career or participant case study:** A person’s before-and-after story involving a program, employer, role, or career change. Use a case-study structure: starting point, turning point, concrete outcome, evidence, and lesson. Confirm permission before naming or quoting the person. If the story involves private communications or records, use only the minimum relevant material and omit unrelated sensitive details.
- **Research or evidence post:** A claim based on data, a model, a report, or an analysis. Prioritize methodology, limits, uncertainty, and a defensible interpretation.
- **Product or organizational announcement:** Lead with the concrete change and why it matters to readers. Do not lead with internal excitement.
- **Article, podcast, or report promotion:** Lead with the strongest finding or useful disagreement from the piece, not with “new article” or “new episode.”
- **Carousel or document caption:** Give one or two meaningful findings, then point readers to the visual material. Do not duplicate every slide.
- **Hiring or assessment content:** Focus on role-relevant capabilities, work context, diagnostic evidence, and whether an assessment distinguishes relevant performance. Avoid broad status labels or claims unrelated to the role.

If the request is unclear, ask one concise routing question before writing:

> Is this mainly an evidence post, an announcement, a promotion, or a person-centered case study? That choice changes the hook and structure.

## Accuracy, authorization, and privacy rules

1. **Do not invent facts.** Do not fabricate statistics, names, quotes, outcomes, clients, organizations, titles, dates, research findings, or testimonials.
2. **Separate evidence from interpretation.** State what the source shows, then identify the conclusion, recommendation, or hypothesis.
3. **Preserve meaningful uncertainty.** If a result has wide ranges, weak evidence, important assumptions, correlation rather than causation, or unresolved disagreement, say so plainly.
4. **Use exact details when supported.** Specific figures, dates, roles, and outcomes are often stronger than broad descriptions. Do not convert a rough estimate into falsely precise language. If a source says “about 20,” do not write “20.”
5. **Ask for missing evidence early.** If a post depends on an unsupported claim, remove it, narrow it, qualify it, or request a source.
6. **Avoid misleading urgency.** Do not exaggerate stakes to create engagement. A sharp, specific risk and a practical response are more credible than broad alarm.
7. **Respect access boundaries.** When source material includes private communications, personnel records, customer information, or participant data, require a legitimate purpose and clear authorization. Use only the minimum relevant information, honor consent and privacy expectations, and keep the output appropriate to the intended audience.

## Audience and voice

Write for the reader most likely to act on the post, not for everyone who might vaguely relate to it. Specificity acts as a useful filter: it helps the right readers recognize that the post is for them.

Use this default voice unless the user gives different guidance:

- Direct, clear, and conversational.
- Short sentences and concrete nouns.
- Active voice where possible.
- One main claim per sentence.
- Sober about problems and practical about responses.
- Specific rather than promotional.
- Confident only where the evidence supports confidence.

Avoid three common failure modes:

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are thrilled to announce an exciting new initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences full of unexplained terms. | State the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Broad catastrophe language without a clear mechanism or response. | Name the specific risk, evidence, uncertainty, and useful intervention. |

## Core workflow

### 1. Inspect the source before choosing a format

Do not begin with a template. Read the source and find the strongest material buried inside it.

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

If several strong angles exist, do not silently choose one. Present two to four numbered options. For each, say what it foregrounds and why it may work for the intended audience.

**Angle-selection prompt:**

> I see several viable post angles. Which should lead?
>
> 1. **[Angle]**: Foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: Foregrounds [specific story, outcome, or disagreement]. Best for [audience intent].
> 3. **[Angle]**: Foregrounds [framework or implication]. Best for [audience intent].

Choose one primary thread. A social post is not a summary of every point in the source.

### 2. Generate hooks before drafting the body

The opening determines whether the rest of the post is read. On platforms that collapse long posts, the first roughly 200 characters matter most. Generate five to ten hooks before committing. When user choice would help, show a numbered shortlist of three to five strong options, each with a brief note on its strategic purpose.

A hook should make an honest promise that the body fulfills. It should work on its own without requiring the reader to understand the source first.

Useful hook patterns:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific body of evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Named outcome:** “[Person or role] moved from [starting point] to [specific outcome] in [timeframe].” Use only with evidence and permission.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only if the post defends the claim.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused question:** “Why do two credible groups reach such different conclusions about [specific issue]?”

**Hook-shortlist format:**

| No. | Hook | What it does strategically |
|---|---|---|
| 1 | “[Specific claim or finding].” | Leads with a concrete result and gives readers a reason to continue. |
| 2 | “[Alternative hook].” | Uses a defensible contrast or changed-mind frame. |

Reject hooks that are interchangeable across unrelated topics. If a key noun could be replaced with “marketing,” “leadership,” or another broad topic and the sentence still works, the hook is likely too generic.

Avoid:

- Generic announcement openings such as “Excited to share.”
- Throat-clearing such as “In today’s fast-moving environment.”
- Empty cliffhangers that do not deliver a payoff.
- Multiple rhetorical questions in a row.
- Broad motivational claims.
- Clickbait such as “You will not believe” or “This changes everything.”

### 3. Choose one structure

Select the structure that fits the source. Do not combine more than two structures without a clear reason.

1. **Counterintuitive claim → evidence → implication**  
   Best for research, data, and argument posts. Start with the surprise, show supporting facts, then explain what readers should do or reconsider.

2. **Changed mind → trigger → updated view → takeaway**  
   Best for thoughtful first-person posts. State the previous view, explain what changed it, and give the new conclusion.

3. **Problem → why it matters → practical response**  
   Best for explainers and operational content. Keep the problem concrete and make the response proportionate.

4. **Result → how it happened → reusable lesson**  
   Best for launches, team outcomes, and approved case studies. The result must be real and specific.

5. **Framework → examples → application**  
   Best for posts readers may save and revisit. Give the framework a useful name only if the name clarifies rather than brands ordinary advice.

6. **Specific announcement → reader relevance → next step**  
   Use only when the announcement itself is genuinely notable. Lead with what happened and its practical significance.

7. **Strategic trade-off → rationale → consequence**  
   Useful when explaining deliberate constraints or “anti-goals”: what an organization has intentionally chosen not to optimize for, why it made that choice, and what follows from it.

### 4. Draft the body: hook, tension, payoff

Use this default shape:

- **Hook:** The strongest claim, result, or tension.
- **Tension or setup:** Why the point matters, what is surprising about it, or what assumption it challenges.
- **Payoff:** The evidence, story, framework, or practical insight. The post should be valuable even if the reader never opens a link.
- **Soft close:** Exactly one focused question, one practical takeaway, or one clear pointer to more material.

A useful default is under 300 words. A working range for a substantial professional post is often about 1,200 to 2,500 characters, but substance and platform norms decide. Every extra line must earn its place.

Use white space. Write in one- or two-sentence paragraphs so the post scans well on a phone. For a longer post, frequent paragraph breaks are normal. Use bullets only when the content is genuinely list-shaped, such as three reasons, four findings, or a checklist.

Use bold, italics, emoji, symbols, or special characters only if the chosen platform renders them correctly and the user wants them. Treat formatting as emphasis, not decoration. One or two emphasized phrases can clarify a post; excessive styling makes it harder to scan.

For a carousel or document caption:

- Establish the central idea.
- Include one or two of the strongest specifics.
- Tell readers what the visual material adds.
- Do not turn the caption into a slide-by-slide summary.

For a linked article, report, or podcast:

- Put the strongest finding in the body.
- Treat the linked item as depth, sources, or extended analysis.
- Follow the user’s platform strategy for link placement.
- Never make “read the link” the main value proposition.
- If the platform or account strategy favors links in a comment or reply, prepare that text separately rather than putting the URL in the post body.

## Calls to action and questions

Use one close only. A strong close gives readers a real, bounded way to respond.

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

If the user has a punctuation preference, obey it. Otherwise, favor periods, commas, and line breaks over theatrical punctuation. Read the draft aloud. If it sounds like generic thought leadership rather than a person making a specific point, rewrite it.

## Revision protocol

When the user gives feedback, revise the requested line and the nearby logic first. Do not rewrite the entire post unless asked.

Examples:

- If the hook is “not sharp enough,” provide several replacement hooks before changing the body.
- If a claim feels overstated, tighten the evidence or soften only that claim.
- If a paragraph feels slow, cut setup before adding more explanation.
- If the user prefers an earlier sentence, preserve it unless there is a clear reason not to.

Multiple small options are often more useful than one complete redraft, especially for hooks, closers, and uncertain lines. Do not accidentally soften the strongest approved line during later revisions.

Be candid about weak material:

> The second paragraph relies on a broad claim that the source does not yet support. We can add evidence, make it narrower, or replace it with this concrete example: [example].

## Readiness gate and audit

Do not present a draft as final until it passes this checklist:

- Does the first line earn attention when read alone on a phone?
- Is the post about one clear point rather than several competing ideas?
- Is there at least one concrete detail, outcome, example, number, or mechanism where appropriate?
- Could the main claim be defended if a knowledgeable reader challenged it?
- Does the post provide value without requiring a click, swipe, or purchase?
- Is uncertainty stated where it materially affects the conclusion?
- Is the language specific to this topic rather than reusable for any industry?
- Is the close one focused action, question, or pointer?
- Are all names, quotes, figures, and claims approved or supported by source material?
- Are personal details authorized, necessary, and appropriate for the intended audience?
- Does formatting work on the intended platform?
- Does the link placement match the user’s chosen platform strategy?
- Does the tone remain professional, respectful, and non-inflammatory for the intended audience?

If any answer is no, revise before handoff.

## Handoff format

When presenting work to the user, provide only what helps them decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen delivery format or location.
3. Any unsupported claim, missing input, permission issue, or line that remains uncertain.
4. Suggested first-comment, reply, or link text, if relevant to the platform strategy.
5. A concise publishing reminder appropriate to the platform, such as responding promptly and substantively to genuine early comments.

**Handoff template:**

> **Recommended hook:** [Hook]  
> **Why this one:** [Strategic reason.]  
>
> **Alternates:**  
> 1. [Hook], [strategic reason].  
> 2. [Hook], [strategic reason].  
>
> **Draft:** [Insert post or provide the user-chosen delivery location.]  
>
> **Soft spot or missing input:** [Unsupported claim, permission check, or “None.”]  
>
> **Link comment/reply:** [Context line plus URL, or “No external link.”]  
>
> **Publishing reminder:** [Reply to genuine early comments with substance; record what audience response suggests for future posts.]

Do not claim that a particular format, timing tactic, or engagement metric is guaranteed to improve reach. Platform behavior changes frequently. Treat distribution advice as a testable hypothesis and compare results across several posts.

## Common failure patterns

- **Announcement disguised as content:** The post tells readers the organization is pleased, but not why readers should care. Lead with the actual change or lesson.
- **Pure teaser:** The post asks readers to click but provides no useful insight. Share the main finding and use the linked piece for depth.
- **Unsupported precision:** The post uses a striking figure without a source, scope, or caveat. Verify, qualify, or remove it.
- **Generic inspiration:** The post sounds positive but has no mechanism, example, or decision. Name the concrete action or trade-off.
- **Overpacked summary:** The post tries to cover every section of a report. Select one thread and save the rest for the original material or later posts.
- **Bolted-on promotion:** A course, product, or service appears at the end without a natural connection. Remove the pitch, create a separate promotional post, or make the connection concrete and immediate.
- **Forced engagement:** The post demands reactions or comments. Ask one real question or end with a useful conclusion.
- **Privacy overreach:** The post uses personal details because they make the story stronger, even though they are unnecessary or not authorized. Remove identifying information, seek permission, or use a different angle.
- **Format mismatch:** The draft depends on bold, a link preview, a carousel, or long paragraphs that the selected platform does not support well. Adapt the post to the actual publishing format.

## Learning loop

After publication or after the user accepts a final version, review feedback and outcomes only when they are legitimately available to the user. Look for reusable patterns:

- Which hooks were rejected, and why?
- Which phrases did the user repeatedly edit out or restore?
- Did readers challenge an unsupported or unclear claim?
- Did paragraph order, the close, or the format change during revision?
- Did a particular structure lead to substantive comments, saves, replies, or qualified leads?
- What input was missing and had to be requested late?

Update the user’s approved writing guidance only with their authorization or in a user-controlled working document. Do not silently alter private source files, profiles, or records. If there is no clear reusable lesson, make no change.

The final standard is simple: the post should sound like someone with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, or a generic social-media template.


---
name: case-study-post
description: Create an evidence-based case study post about a person’s professional change, learning, or role-relevant work. The workflow produces a review-ready draft, alternate hooks, quote-card options, approval checks, and a safe delivery package.
---

# Write a case study post

Use this workflow to turn authorized source material into a concise, credible public case study. It is designed for professional social posts, but it also works for newsletters, community updates, program pages, and participant stories.

The purpose is not to praise someone in general terms. Show a specific, supportable change: where the person started, why they acted, what concretely helped, what happened next, what they do now, and what a relevant reader can do.

Only use personal information for a legitimate publishing purpose and with clear authorization. Review the minimum relevant sources, omit unrelated personal details, respect consent and privacy expectations, and keep drafts, evidence, and outputs within the appropriate access boundary. Do not use private records merely because they are available.

## Inputs and readiness gate

Collect the available material that is relevant to the intended post. It may include:

- An authorized interview transcript, notes, or conversation summary
- A subject-provided intake form, application, or survey
- A current approved biography or professional profile
- Public work samples, projects, publications, portfolios, or announcements
- An authorized internal note that reports a result
- A previous draft, outline, or subject-provided notes
- The intended audience, platform, publication owner, and call to action
- An editorial or brand voice guide
- The approval status for names, quotations, roles, achievements, and sensitive claims

Before drafting, build a private fact sheet. Do not include unnecessary sensitive details in the fact sheet or the final post.

| Field | What to capture |
|---|---|
| Subject | Preferred public name, pronouns if relevant, and publication permission status |
| Before-state | Previous role, field, goal, uncertainty, or relevant constraint |
| Trigger | Why they joined, applied, changed direction, or took action at that point |
| Intervention | Program, community, event, mentor, resource, or service involved |
| Mechanism | Concrete help, such as a realization, opportunity, introduction, feedback session, or practical resource |
| Now-state | Current role, work area, project, output, or result that may be shared publicly |
| Timeline | Verified dates or time spans from starting point to outcome |
| Evidence | Sources supporting roles, figures, dates, named work, and direct quotes |
| Cost or risk | Any career tradeoff, uncertainty, or meaningful cost, if relevant and approved |
| CTA | The one action the intended reader should take |

Do not begin a full draft until you have, at minimum:

1. A verified before-state.
2. A concrete mechanism, not only a claimed result.
3. A current outcome that can be described publicly.
4. A defined audience.
5. A clear call to action.

If a critical item is missing, ask focused questions before writing. Do not guess at names, job titles, project titles, dates, figures, timelines, affiliations, or outcomes.

Useful questions:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they decide to take part or change direction then?
4. What were the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a public project, placement, product, publication, or result that may be named?
8. Was there a meaningful cost or risk they want to share publicly?
9. Which names, figures, quotations, and claims are approved for publication?
10. Who should this post persuade, help, or invite?

## Evidence, attribution, and privacy rules

Never invent facts or make a claim stronger than the source supports. If a source says someone contributed to a project, do not call them the lead. If they explored an opportunity, do not say they received it. If they learned about a role through a community, do not claim the community caused the hiring decision unless reliable evidence supports that claim.

Treat automated transcripts and summaries as fallible. They may mishear names, organizations, technical terms, figures, and titles. Cross-check any detail that carries the story, especially the role, employer or team, timeline, amount, publication status, and direct quote.

Use this default reliability order when sources disagree:

1. The subject’s direct, recent confirmation
2. An official public record, published work, or authorized organizational record
3. A current approved professional profile or biography
4. The subject’s original written statement
5. Interview notes or automated transcript summaries
6. Informal third-party messages

Keep these categories separate in working notes:

- **Verified fact:** Supported by an appropriate reliable source.
- **Subject interpretation:** What the person says helped them or changed their view.
- **Editorial inference:** A conclusion drawn from the story. Use only when evidence supports it, and phrase it carefully.

Flag these for explicit subject approval before publication:

- Compensation, pay changes, financial hardship, or comparisons
- Health, family, immigration, legal, or other sensitive personal circumstances
- Harsh language about a former role, employer, or career decision
- Unreleased work, confidential projects, or unpublished titles
- Direct quotations, especially criticism or strong personal opinions
- Claims about why an employer selected the person
- Claims of causation or impact that cannot be independently verified
- Details that expose a private timeline, location, or personal situation

If approval is unavailable, use an honest approved fallback or remove the point. For example, replace a precise financial detail with a broader approved statement only if it remains true and useful. Do not make the story more dramatic to hide uncertainty.

## Build the story beats

Create a concise working outline before writing.

### 1. Before-state

Capture the subject’s role, background, and the reader-relevant version of their uncertainty. Include an alternative path they were considering only when it mirrors the audience’s current life.

Keep details that move the story. Remove long lists of credentials, reading lists, and unrelated prior roles. A detail earns its place if it explains the decision, establishes a meaningful contrast, or makes the result concrete.

### 2. Trigger

Identify why the subject acted at that moment. Common triggers include wanting to test whether a field was open to them, solve a practical problem, gain role-relevant capabilities, find collaborators, or make a values-driven career decision.

### 3. Mechanism

Find one or two observable things that helped change the trajectory. Strong mechanisms include:

- Realizing that a field or role was accessible
- Seeing a relevant opportunity in an authorized professional community
- A conversation that clarified next steps
- Feedback that improved an application, portfolio, or project
- A specific introduction, workshop, or practical resource

Avoid vague claims such as “the experience was transformative.” State what happened instead.

### 4. Now-state

Record the current role, work area, team or organization only if public and approved, and what the person actually does. Translate specialized language enough for the intended reader to understand why the work matters.

Use a named output only when it provides real evidence. One meaningful project, publication, product, placement, or grant is usually stronger than a resume-like list.

### 5. Timeline and compression

Map the sequence from starting point to outcome. Calculate a short, truthful timeframe when it sharpens the story, such as “within six months” or “the following year.” Do not force a compressed timeline if the facts do not support one.

### 6. Quotes

Pull three to five verbatim candidate quotes. Favor lines that speak to the reader’s identity, uncertainty, or decision rather than only celebrating the subject’s result.

Use three categories:

1. **Discovery:** A line about not knowing a path was possible.
2. **Mechanism:** A line about the concrete help or opportunity.
3. **Conviction:** A line about why the decision mattered or why they would make it again.

Light trimming is acceptable only when it preserves the speaker’s meaning and grammar. Never rewrite a quote into words the person did not say.

## Generate three hook options

For feed-based platforms, the first two lines determine whether people continue reading. Write three distinct hooks before drafting the full post. Keep each to two short sentences, generally under about 140 characters total when that suits the platform.

### Hook A: Discovery

Use when the audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a surprising concrete mechanism.

This is the default recommendation when the reader may think, “That could be me.”

### Hook B: Identity collision

Use when the before-and-after contrast is vivid and easy to understand.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This can work well for broad audiences that may not share the subject’s exact uncertainty.

### Hook C: Stakes-led

Use only when a meaningful cost or risk is approved and the intended audience will read it as honest conviction rather than a warning.

**Formula:** The subject accepted a specific cost to do something. Now they are taking a concrete action or doing meaningful work.

Do not use a sacrifice hook if it implies that participation requires hardship or if a more accessible message would better serve the audience.

Choose one recommended hook. Give one sentence explaining why it fits the audience. Give one short reason each for not choosing the other two. If feedback says the hook is weak, generate three genuinely new options. Do not make small edits to the original set.

## Draft the post

Aim for roughly 160 to 220 words unless the platform requires another length. Shorter is often stronger.

Use this sequence:

1. **Hook:** Use the recommended hook.
2. **Before-state:** One short paragraph showing the previous situation and relevant alternative path.
3. **Name the intervention:** Clearly state that the person joined the program, used the resource, or entered the community. Do not leave it implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then land the immediate result in plain language.
5. **Current work:** Describe what they do now and why it matters in language the audience can understand.
6. **Optional honest cost:** Include only when approved and useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already carried by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

A compact mechanism-and-outcome sequence can work well: “They saw the opportunity. They applied. They got the role.” Use this only when every statement is verified and the rhythm improves clarity.

If the platform’s current publishing guidance or the organization’s approved practice favors links outside the post body, place the external link in the approved destination, such as a first comment, profile page, or landing page. Do not present a distribution tactic as universal without current evidence.

## Style rules

Adapt to the selected voice guide. Unless it says otherwise, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense where possible.
- Use concrete names, roles, dates, and figures only when verified, necessary, and approved.
- After the first full introduction, use the person’s preferred first name if it fits the tone and consent allows it.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not call someone exceptional, inspiring, or brilliant without showing relevant evidence.
- Use contractions if the voice is conversational.
- Keep the CTA in full second person.
- Avoid emojis unless they are an explicit brand choice.
- Do not use em dashes. Use periods, commas, or line breaks instead.

On the final pass, remove common machine-like phrasing:

- Empty transitions that repeat the previous sentence
- Slow date-first openings when a stronger identity or claim is available
- Corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” or “empower”
- Filler intensifiers such as “truly,” “deeply,” “fundamentally,” or “remarkably”
- Abstract nouns standing in for evidence, such as “journey,” “transformation,” or “paradigm”
- Hedges and softeners, including “it is worth noting,” “arguably,” “just,” and “ultimately”
- Artificially balanced constructions such as “on one hand, on the other hand”
- Dramatic colon frames such as “The truth is: ...”
- Reflective summary sentences after the CTA

Read the post aloud. If it sounds like generic thought leadership, shorten it and replace abstractions with verified facts.

## Graphic quote options

Provide three options for a visual quote card. Each should be self-contained, under 15 words where possible, and verbatim from approved source material.

Offer one quote from each category:

- Discovery
- Mechanism
- Conviction

Recommend one with a one-sentence rationale. Discovery quotes are often strongest because they work without context and mirror the reader’s uncertainty. Choose a mechanism or conviction quote instead only when it is clearer, more memorable, and understandable on its own.

## Readiness audit

Before sending the draft for review, check:

- Is every name, role, date, figure, title, and outcome verified?
- Were transcript-derived details cross-checked where needed?
- Does the post show a concrete mechanism, not merely a result?
- Does it avoid overstating causation?
- Is the intervention named clearly?
- Does the opening mirror a real audience concern?
- Is the current work understandable to a non-specialist reader?
- Have sensitive claims and direct quotes been flagged for approval?
- Is the CTA clear and directed at the intended reader?
- Are there no em dashes, unsupported superlatives, corporate phrases, or generic filler?
- Does the post stay within the authorized publishing and privacy boundary?

## Delivery and iteration

Create the draft in the user’s chosen approved document system, if one is available. Use a clear title format such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and the two alternatives
- The three graphic quote options and recommendation
- A list of approval items
- A list of missing information that would strengthen the post
- The approved document location or link, if applicable

Do not treat the first draft as final. If asked to make it shorter, cut secondary biography first while preserving the mechanism and outcome. If the subject rejects a sensitive line, replace it with an approved fallback without weakening the entire story.

After the final version is accepted, review feedback for reusable lessons. Update the workflow only when a repeated pattern is clear, such as a missing intake question, a consistent voice preference, or a recurring verification issue. Do not invent process changes from a clean review cycle.


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
description: Create or improve a short, paid, asynchronous work sample that produces role-relevant evidence, is practical to score, and is validated through simulated submissions before use.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A strong work sample asks candidates to perform a bounded, realistic version of the job, produces evidence that is difficult to replace with generic claims, and can be reviewed consistently in a reasonable amount of time.

Use it for new exercises and revisions. Do not use it for interview questions, application-form screeners, live assessment centers, or multi-day work trials. If the requested format is unclear, ask one question before proceeding.

## Purpose and design principles

A work sample usually sits between initial screening and later interviews. Its purpose is narrow: determine whether a candidate can demonstrate the role-critical capabilities that can fairly be observed in a short asynchronous exercise.

Do not try to assess the whole person or every requirement of the role. Important evidence belongs in different stages:

- Interviews can assess live communication, motivation, collaboration, and interactive reasoning.
- References can assess sustained reliability, integrity, and performance over time.
- A longer paid trial can assess consistency, judgment in real systems, and work over multiple days.
- Training can often close gaps in a particular tool, internal process, or nonessential domain vocabulary.

The work sample should focus on three to five load-bearing, observable capabilities. Depending on the role, these may include prioritization, practical judgment, clear writing, problem diagnosis, sourcing, execution, systems thinking, research quality, or the ability to make useful progress amid ambiguity.

Use these default constraints unless the hiring owner explicitly chooses otherwise:

- Make the exercise paid.
- Set a clear expected time limit. Two to four hours is a useful range for many roles.
- Use a realistic but fictionalized or safely anonymized scenario.
- Do not request commercially usable production work unless the candidate separately agrees to that use.
- Keep expected review time to roughly 20 to 25 minutes per submission.
- Make the exercise self-contained. Candidates should not need internal systems, confidential data, or access to unavailable people.
- State whether AI tools are allowed, and assess judgment and outputs rather than attempting to infer AI use from prose style.
- Evaluate only capabilities materially related to the role. Do not use protected characteristics, personal background, or unrelated proxies as criteria.
- Offer a route for reasonable accommodations or an equivalent accessible format while maintaining the same role-relevant standard.

When reviewing internal hiring materials or records, use them only for a legitimate hiring purpose and with clear authorization. Read the minimum relevant sources, omit unrelated or sensitive personal information, and keep notes, simulations, and outputs within the approved hiring access boundary.

## Step 1: Pre-flight

Before designing the work sample, confirm that the hiring team has both of these inputs:

1. A current job description or role brief that explains responsibilities, level, expected outcomes, and reporting context.
2. A role-success profile, hiring plan, or equivalent document that identifies the capabilities and experience needed to achieve those outcomes.

If either item is missing, stop. Do not attempt to define the role-success profile while designing the exercise. That creates a moving target and typically produces a plausible task that measures the wrong things.

Use this request format:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

If the materials exist, read the relevant role context. This can include approved project notes, current team constraints, examples of strong work, prior hiring feedback, and existing exercises for comparable roles. Read one or two reference exercises only to calibrate tone, length, and operational format. Do not copy their task shape automatically: different roles require different evidence.

Then give a concise status update, for example:

> Read the role brief, success profile, and two reference exercises. Moving to the alignment memo.

## Step 2: Write the alignment memo before drafting

Do not write candidate-facing instructions yet. First produce a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five capabilities that the role succeeds or fails on and that can be surfaced in the exercise window. Phrase them as observable actions, not vague virtues.

Weak: “Strategic thinking.”

Better: “Can identify the highest-leverage issue in a messy operating situation, explain the tradeoff, and deliver a useful first action.”

### What the exercise will not test

Name important criteria that should be assessed elsewhere. This keeps the exercise honest and stops it from becoming an unrealistic proxy for the whole job.

For example, a short written exercise may not fairly assess long-term reliability, leadership over months, responsiveness in live meetings, specialized software fluency, or collaboration inside a real team.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level. Explain what this changes:

- Entry-level candidates may need more context and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make tradeoffs, set direction, and create work another person could use without further explanation.

### Failure modes the exercise should catch

Identify two or three plausible work patterns that could otherwise appear strong during ordinary screening but would create problems in this role. Describe observable evidence, not personal labels.

Examples:

- A polished planner who does not deliver usable work.
- A fast executor who misses the central problem or creates avoidable risk.
- A careful candidate who defers every meaningful decision.
- A skilled specialist who cannot communicate for the intended audience.

### What strong looks like

Write a short paragraph describing a top submission. Focus on visible evidence: what the candidate notices, what choices they make, what they deliver, and how they handle uncertainty.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the owner confirms or revises the memo.

## Step 3: Propose exercise shapes

Once the memo is approved, propose three exercise shapes. Each option must test the agreed capabilities in a distinct way, be understandable in about one minute, be self-contained, and be scorable quickly.

For each option, provide:

- **Shape:** A plain-language description of the task.
- **What it tests:** The agreed load-bearing capabilities.
- **Why it is evaluable:** What evidence reviewers will see and why it can be scored consistently.
- **Main risk:** The most likely source of noise, ambiguity, or unfairness.

Keep each option concise. Common shapes include:

- **Triage pile:** The candidate receives realistic messages, requests, and constraints. They prioritize, draft responses or work products, and recommend one systemic improvement. This suits operations, coordination, support, and communications-heavy roles.
- **Choose the highest-leverage action and ship it:** The candidate receives a brief with multiple possible priorities, selects one, explains the choice, and creates a small usable output. This suits strategic operations and builder roles.
- **Diagnose and fix:** The candidate reviews a messy situation, identifies the key problem, and ships one targeted intervention. This suits product, program, analytical, and process-improvement roles.
- **Source and pitch:** The candidate defines a target profile, identifies promising channels or prospects from supplied information, and writes outreach. This suits recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** The candidate assesses an intervention area using supplied evidence and makes a recommendation for a decision-maker. This suits research, policy, strategy, and specialist roles.
- **Design a repeatable system:** The candidate creates a lightweight process, playbook, or operating artifact that a teammate could use. This suits program, community, enablement, and operational design roles.

Do not draft the full exercise until the hiring owner chooses a shape. If none fit, generate three more based on the confirmed capabilities rather than forcing a familiar format.

## Step 4: Draft version 1

Write the candidate-facing exercise in this order.

## [Role] Work Sample

Open with one or two sentences explaining the abilities the exercise assesses. State the total time expected.

**Your mission**

Describe a specific situation, not an abstract assignment. Include enough context to make the work realistic. If decisiveness is being assessed, state which stakeholders are unavailable during the exercise so candidates must make reasonable assumptions instead of deferring every decision.

End with one sentence restating what the candidate will produce.

**Deliverables**

List two to four substantive parts. Include rough time guidance when useful. A common operations pattern is:

- A short prioritization or analysis section.
- Several actual drafts, decisions, or shipped outputs.
- One systemic fix, process improvement, or reusable artifact.

Avoid excessive micro-tasks. A few substantive outputs reveal more than dozens of shallow decisions. If planning and execution both matter, explicitly tell candidates not to spend all their time planning.

**Context**

Provide the minimum information needed to complete the work: project state, audience, constraints, available resources, relevant policies, and stakeholder availability. Use fictional names, fictional contact details, and generic identifiers unless the hiring owner has explicitly approved public information for use.

For a triage-pile exercise, include approximately eight to ten realistic items. Some should connect, so candidates are rewarded for recognizing patterns across the whole situation. Add reference notes with information necessary for fair decisions, such as capacity limits, escalation rules, or refund policy.

**Instructions**

Include:

- The expected time limit.
- The submission deadline, written clearly.
- The submission format, such as one document or PDF, plus links to supplementary artifacts where needed.
- The payment amount, payment process, and any early-submission bonus.
- What tools and AI assistance are permitted.
- A request to document important assumptions briefly.
- Permission to submit incomplete work if time runs out.
- Optional guidance on a short walkthrough video if it would add useful evidence.
- A contact route for accommodation requests or access issues.

Use a transparent AI policy. For example:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

**Anticipated questions**

Include answers to common questions:

- If a requirement is unclear, make a reasonable assumption and state it briefly.
- If you do not finish in the expected time, submit what you have and note what you would do next.
- The work will be used only to evaluate candidates unless another use is agreed separately.
- If you need an accessible or alternative format, use the organization’s stated hiring contact before starting where possible.

## Payment choices

Set compensation based on the time required, local legal requirements, role level, and the organization’s approved budget. A paid test should compensate candidates for the expected effort, not merely offer a symbolic amount.

An early-submission bonus can be useful where speed is genuinely role-relevant, such as high-volume operational work. Do not use it where it would mainly reward candidates with fewer outside responsibilities or where a fixed speed requirement is not central to the job.

If payment is requested through a form or expense workflow, provide separate, accurate instructions for any base payment and bonus. Link to the approved payment route in the final candidate communication without exposing internal account identifiers or private financial details. Confirm that payment handling meets applicable employment, tax, privacy, and procurement requirements.

## Candidate-facing writing and format checks

Write in direct, plain language appropriate for the organization and candidate audience. Use the organization’s chosen spelling convention consistently. Keep instructions easy to paste into the selected hiring platform and easy to read in a document.

Before sharing a draft, check that candidate-facing text:

- Has no tables if the destination system renders tables poorly.
- Avoids horizontal divider lines if they break the destination editor.
- Uses simple headings and bullets.
- Avoids generic AI-sounding slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.
- Uses clear phrases such as “by the end of Tuesday,” not abbreviated wording.
- Uses clearly fictional names and contact details in fictional scenarios.
- Formats multi-line message metadata clearly. If the target editor collapses line breaks, use its supported soft-break method.
- Does not include confidential details, credentials, private contact information, or sensitive internal data.
- Does not require candidates to contact fictional people or access external systems to complete the task.

After every draft, add a separate section that is not for candidates:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets on design choices the owner may want to change. Typical notes include:

- Whether a scenario item is too obvious to reveal useful evidence.
- Whether the scenario needs more realistic context or a stronger tradeoff.
- Whether compensation and any speed bonus match the role.
- Whether a deliverable is too prescriptive or too vague.
- Whether an optional video would add useful signal or unnecessary burden.
- Whether the task relies on information candidates could not reasonably know.

End with one focused decision question, such as: “Which part should we tighten first?”

## Step 5: Iterate with the hiring owner

Expect multiple rounds. For each revision, provide the complete updated work sample, not only a change list, so it can be copied directly into the selected system.

Apply feedback directly unless it would materially undermine validity, fairness, privacy, accessibility, or safety. If that happens, state the concern once in plain language, offer an alternative, and let the accountable hiring owner decide.

Common revision requests include tightening vague instructions, loosening over-prescriptive tasks, correcting scenario facts, simplifying deliverables, changing payment, and replacing unrealistic context.

## Step 6: Simulate two candidates

Before declaring version 1 complete, simulate two full submissions in parallel using the exact candidate-facing instructions. Simulations are a diagnostic tool, not a substitute for later monitoring of real assessment outcomes.

### Role-aligned simulation

Use a persona that matches the confirmed role-success profile. Have them complete the actual deliverables under the stated time limit. Ask for a short reflection on their choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest, capable candidate who could pass ordinary screening but whose demonstrated work lacks one role-critical capability. Choose a mismatch tied to work evidence, such as a planner where the role needs a builder, a cautious hedger where it needs decisive judgment, or an executor who cannot recognize systemic patterns. Do not tie the simulation to identity, background, disability, protected characteristics, or stereotypes.

Have this persona produce the same complete submission.

Then synthesize the results:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both candidates performed similarly.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by likely impact.

Floor checks that both candidates pass are not automatically bad. The concern is when a central capability fails to create meaningfully different evidence.

## Step 7: Apply validation improvements

Revise the full exercise based on the simulation. Target the weakest diagnostic points first. Useful revisions may include:

- Making connected scenario items more interdependent.
- Removing obvious noise that takes seconds to dismiss.
- Adding a concrete constraint that forces a meaningful tradeoff.
- Replacing a broad opinion prompt with a usable deliverable.
- Clarifying reviewer guidance so it rewards the intended behavior.
- Removing specialized knowledge requirements that are trainable and not essential at the point of hire.

Do not make the task harder merely to make it more selective. Make it more diagnostic of the agreed role-relevant capabilities.

## Step 8: Optional external review

If other reviewers provide feedback, assess each suggestion against the approved alignment memo. State which suggestions to integrate, which to skip, and why. External review is evidence, not an automatic instruction. The accountable hiring owner remains responsible for the assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The role description and role-success profile are confirmed.
- The alignment memo is approved.
- The chosen task shape maps directly to the load-bearing capabilities.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and does not require private access.
- Payment, submission, AI-use, and accommodation instructions are clear.
- Candidate-facing text is formatted for the destination system.
- A reviewer can assess a submission in about 20 to 25 minutes.
- A role-aligned and a plausible role-misaligned simulation have been completed.
- The simulation led to any necessary revisions.
- The final version contains no sensitive data and does not create unpaid production work.
- Role relevance, accessibility, privacy, and possible proxy bias have been checked.

## Common failure modes

Avoid these patterns:

- Designing the task before agreeing what it should measure.
- Testing tool familiarity, domain trivia, or trainable knowledge instead of durable judgment.
- Asking for too many small outputs instead of a few meaningful ones.
- Making every scenario item independent, which tests volume but not pattern recognition.
- Allowing candidates to defer every decision to an available stakeholder when decisiveness is meant to matter.
- Giving vague context that rewards insider knowledge.
- Setting word-count targets that encourage padding.
- Creating a test that takes longer to grade than the signal justifies.
- Treating polished writing or presentation as the main signal when the role requires something else.
- Using real internal messages, names, customer information, or operational data when a fictionalized scenario would work.
- Offering an optional video when it adds presentation bias without revealing a role-relevant capability.
- Declaring success without checking whether the exercise distinguishes the role-relevant evidence it was designed to measure.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, accessible, respectful of candidate time, and clear about what good performance looks like.


---
name: run-a-reference-call
description: Prepare, conduct, and document a hiring reference call using authorized, role-relevant evidence, a focused call brief, and a clear record for the hiring decision.
---

# Run a reference call

Use this workflow when an employer needs to check a candidate’s prior work as part of an active hiring process. The goal is to gather specific, role-relevant evidence—not vague praise—and leave an authorized hiring record that helps the team make a fair decision.

Use reference information only for a legitimate hiring purpose and with any required candidate notice, consent, and authorization. Use the minimum relevant professional information. Keep preparation, call notes, recordings, and summaries within the approved hiring access boundary. Do not collect or record unrelated personal information, sensitive characteristics, rumors, or speculation.

## 1. Confirm purpose, authorization, and logistics

Confirm or obtain:

- Candidate name and the role under consideration.
- Referee name, contact information, and professional relationship to the candidate.
- Call date, time, attendees, and joining details.
- Hiring stage, upcoming decision, and the uncertainty the call should reduce.
- Whether the referee was provided or approved through the applicable hiring process.
- Whether required consent, notice, and internal authorization are in place.

Check the approved scheduling source for the meeting. Capture the title, time, attendees, joining instructions, and relevant scheduling context. If no event exists, continue with available information and mark logistics as unconfirmed.

This workflow is for an employer checking a candidate’s reference during hiring. Requests from an outside party for a reference about a former worker, participant, or student require a separate process governed by the applicable disclosure and authorization rules.

## 2. Gather only relevant context

Review authorized hiring records and communications to establish:

- The role’s key outcomes, responsibilities, and capabilities to assess.
- The candidate’s stage in the process and next decision point.
- How the referee was introduced.
- How the referee worked with the candidate: manager, client, colleague, collaborator, instructor, or another relevant observer.
- Duration and closeness of the working relationship, including limits on what the referee could directly observe.
- Approved candidate materials, such as an application, professional profile, portfolio, work sample, or assessment record.
- Other known references, only when useful for coordinating evidence collection or avoiding duplicated questions.

Where policy permits, review relevant prior correspondence, meeting records, and hiring materials involving the candidate or referee. Read enough to understand the professional relationship; do not collect unrelated messages or details.

Public research, if needed, should be limited to confirming the referee’s professional background and likely ability to comment on the candidate’s work. Prefer professional profiles or official biographies. Do not investigate private life or infer protected characteristics.

## 3. Review earlier reference evidence fairly

Find completed, authorized reference records for the same candidate. Extract only decision-relevant themes:

- Strengths supported by concrete examples.
- Development areas, risks, or conditions needed for success.
- Contradictions between sources.
- Open questions not yet tested.
- Which referee is best positioned to comment on each topic.

Treat earlier comments as hypotheses, not facts. Do not tell a referee that another person made a negative claim or pressure them to agree. Convert themes into neutral prompts that seek direct evidence. For example: ask the referee to describe a time priorities changed quickly, how the candidate chose a response, and what happened.

If this is the first reference, capture comparable evidence for later calls: scope of responsibility, quality of delivery, reliability, collaboration, response to feedback, judgment, and conditions for strong performance.

## 4. Create the call brief before the meeting

Create a meeting record in the organization’s approved documentation system before the call. The completed record, rather than a separate research summary, is the preparation deliverable.

Use a title such as:

`[Date] — [Referee name] — [Candidate name] reference`

Include the candidate, referee, role, date, attendees, and joining details if available. If the system has an approved meeting-notes or transcription feature, configure it according to policy. Do not pre-fill content intended to be generated during or after the meeting.

Use this structure:

## Context

- **Referee:** [Name, professional role, relevant background, profile link if appropriate].
- **Relationship:** [How the referee and candidate worked together, duration, structure, and closeness of observation].
- **Hiring context:** [Role, key outcomes, hiring stage, and next decision point].
- **Candidate materials:** [Approved application, portfolio, work samples, or assessment links].
- **Other references:** [Names or roles, if known and appropriate].
- **Logistics:** [Call time, attendees, joining details, or “not yet scheduled”].

## Opening

Tailor a short, truthful opening:

> Thanks for making time. I am calling as part of a hiring process for [candidate]. We are considering them for [role], which involves [key outcomes]. I would like to understand work you observed directly, including specific examples of strengths, working style, and development areas. Please share only information you are comfortable and authorized to discuss; your comments will be used internally for this hiring decision.

## Briefing notes

Write direct, actionable instructions for the caller:

- **Evidence to validate:** [Ask for a directly observed project, the candidate’s personal contribution, and the outcome.]
- **Open question:** [Ask for an example relevant to the unresolved role capability.]
- **Unique perspective:** [State what this referee can observe better than other sources.]
- **Relationship limits:** [State where the referee’s visibility may be narrow or indirect.]

If no earlier references exist, state which observations need precise capture so later calls can be compared fairly.

## 5. Run an evidence-seeking conversation

Use these prompts flexibly. Follow the most relevant evidence rather than treating them as a rigid script.

- How did you work together? What were your respective roles, and how closely did you observe the candidate’s work?
- What did the candidate personally own or deliver? Please describe a specific example.
- What did strong performance look like in that setting? How did their work compare with expectations?
- What is their most distinctive strength? What did it look like in practice?
- Where did they need the most support, coaching, or structure?
- If they did not succeed in a role like this after three months, what work-related reason would be most likely?
- If things were going well after three months, what development area should a manager prioritize?
- How did they respond to feedback, ambiguity, setbacks, or changing priorities?
- What management approach or work environment helped them contribute at their best?
- Would you work with them again? In what role or scope, and why?
- What have I not asked that would matter when hiring for this role?

When an answer is broad, ask: “What did that look like?” “What was their personal contribution?” “What happened next?” “How did you know it was successful?” and “What was the impact?”

## 6. Add role-specific probes

Choose probes based on actual role outcomes and the referee’s direct knowledge. Do not use every probe by default.

For operations or program-delivery roles, explore ambiguity handling, repeatable systems, stakeholder communication, prioritization, initiative, and follow-through.

For community or relationship-focused roles, explore trust-building, conflict handling, respectful communication, responsiveness to feedback, and turning feedback into improvements.

For senior operational roles, explore process scaling, competing stakeholder needs, financial or supplier accountability where relevant, risk management, and balancing speed with durable systems.

For technical, analytical, or specialist roles, explore quality standards, judgment, learning speed, communication of complex work, and whether the referee directly reviewed the candidate’s output.

## 7. Record evidence separately from interpretation

During or immediately after the call, complete the record under these headings:

- **Direct observations:** Specific behaviors, examples, outcomes, and limits on the referee’s visibility.
- **Referee interpretation:** Their view of strengths, development areas, role alignment, and willingness to work with the candidate again.
- **Assessment relevance:** The role capability each example supports, weakens, or leaves unresolved.
- **Contradictions or gaps:** Differences from other evidence, unanswered questions, or claims that need verification.
- **Hiring-team inference:** A clearly labeled interpretation, separate from what the referee said.

Do not treat confidence, seniority, closeness to the candidate, or enthusiasm as a substitute for direct, relevant observation.

## 8. Audit before sharing

Before closing or sharing the record, verify that:

- Candidate, referee, role, date, and logistics are correct.
- The referee’s relationship to the candidate and observation limits are explicit.
- Approved candidate materials are accessible to authorized reviewers.
- Briefing notes identify concrete questions and why they matter.
- Questions assessed role-relevant performance rather than personality labels.
- Notes distinguish observations, interpretations, and hiring-team inferences.
- Earlier-reference themes were tested neutrally and fairly.
- Sensitive information was minimized and access is appropriately restricted.
- The record states what remains uncertain and what evidence, if any, should be sought next.

A reference call is one source of evidence. Combine it with structured interviews, work samples, job-relevant assessments, and other authorized evidence. Make the decision based on the relevance, quality, consistency, and limits of the evidence—not on one enthusiastic or critical conversation.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and privacy, verifying rendered state, and separating preparation from consequential actions.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing rendered forms, changing settings, collecting information from dynamic pages, testing a user flow, or working in an authenticated dashboard. The core rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until the account, target, page state, and authorization are clear.

A browser automation command reporting success does **not** prove that a website accepted the change. Modern applications can keep their own state separate from the visible DOM, commit only when focus leaves a field, replace elements during a re-render, or display a failure message even after an action succeeded.

## 1. Establish authority, scope, and privacy boundaries

Before accessing private records, messages, dashboards, or information about people, confirm that the task has a legitimate purpose and that the requester has clear authority. Use only the minimum relevant sources and information. Keep findings, screenshots, logs, and outputs within the appropriate access boundary.

Do not expose or retain unrelated personal details, credentials, session tokens, recovery information, or security settings. Respect consent, confidentiality, and reasonable privacy expectations.

Identify before acting:

- The requested outcome and exact target page, record, form, or setting.
- The data that must be entered, changed, uploaded, or collected.
- The minimum information needed to finish the task.
- Whether the action is reversible.
- Whether the workflow sends, publishes, pays, deletes, grants access, changes billing, changes a plan, or otherwise makes an external commitment.
- Any missing facts or choices that require the user's judgment.

If the target, authority, account, or impact is unclear, prepare what can safely be prepared and ask a focused question before changing data.

## 2. Choose the least invasive route

Use the first suitable method in this order:

1. **Supported direct interface or API.** Prefer a documented and authorized programmatic method when it can complete the task safely.
2. **Headless browser automation.** Use it for public pages, test environments, UI checks, routine extraction, screenshots, and forms that do not need an existing signed-in identity.
3. **Authorized visible authenticated browser session.** Use this only when the task genuinely requires an established account session, organization-specific access, single sign-on state, or a user-directed browser context.

Before driving a browser, check whether the page provides a supported backend route. Review official documentation, ordinary form actions, page source, and visible network activity for authorized endpoints. A direct interface is often more reliable than recreating complex browser behavior.

Do not use undocumented interfaces to bypass access controls, consent boundaries, service restrictions, or security protections. Do not choose an authenticated visible session merely for convenience: it can interrupt the user's work and increases privacy and account risk.

If a site blocks automation, do not attempt to evade its protections for casual research or collection. An authorized visible browser session can be appropriate when the user explicitly requested a legitimate task on that particular site and an existing session is necessary. Do not weaken browser security, authentication, warnings, or anti-abuse controls.

## 3. Protect account, profile, and environment context

For authenticated work, classify the intended context explicitly: for example, personal, organizational, test, staging, or production. Select the profile or session associated with that context instead of relying on a generic browser name, a remembered default, a window title, or a connection label.

Follow these rules:

- Announce that you are taking control of a visible browser and state the task purpose before doing so.
- Use a fresh tab, window, or isolated tab group unless the user explicitly directs you to an existing one.
- Confirm the signed-in account and environment through a reliable account indicator before opening or changing the real target.
- Confirm the target record, organization, workspace, or environment before changing it.
- If the needed profile is unavailable or identity cannot be verified, stop and ask rather than guessing.
- Never reveal credentials, tokens, private account data, or authentication details in output or logs.
- Never disable security controls, multi-factor authentication, browser warnings, or access restrictions to make automation easier.

Use an account preflight gate before actions that change data. Verify the account identity, environment, and target object first. If the automation setup has a verification marker or permission gate, set it only after the verification has genuinely passed; never enable it early merely to unlock browser actions.

Ask: **Which account is active? Which environment is this? What exact item will change?** Resolve uncertainty before proceeding.

## 4. Separate preparation from commitment

Treat reversible preparation and consequential commitment as different phases.

- **Preparation:** fill fields, draft text, choose options, configure a setting, collect a preview, and create a screenshot or concise state record.
- **Commitment:** submit, send, publish, purchase, delete, apply a plan change, grant access, or activate another action with external consequences.

For a consequential task, first complete a preparation pass without triggering the final action. Verify the state, capture a pre-action record when appropriate, and confirm that the final control has the intended effect.

Use the authorization already supplied by the task or standing instructions; do not repeatedly ask for approval for an action that is clearly authorized. However, obtain confirmation immediately before irreversible or unexpected actions when authorization is missing, ambiguous, or does not clearly cover the final impact. Payments, sends, deletes, permanent submissions, and actions explicitly labeled irreversible require especially careful confirmation and a pre-action record.

If the page reloads, re-renders, or the account session changes between preparation and commitment, do not assume prior checks still apply. Re-check account, target, and form state before proceeding.

## 5. Inspect the rendered page before editing

Do not start by guessing selectors, filling controls by numeric position, or trusting a visual approximation. Inspect the rendered page first and identify relevant controls semantically.

For every relevant control, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or label relationship.
- Current value, required state, disabled state, and validation feedback.
- Formatting rules, character limits, and whether line breaks are supported.
- Whether the apparent element is a true editable control, a wrapper, or a hidden synchronization field.
- Whether changing a selection, date, tab, or checkbox causes the page to re-render.

Address fields by stable semantic identity, such as an accessible name, visible label, or explicit label relationship. Avoid DOM indexes when labels are available: dynamic applications can reorder elements across loads and re-renders.

### Generic inspection pattern

Use the chosen browser automation capability to list relevant controls before writing fill logic. Record at least the element type, accessible label, required state, and current readable value or text length.

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

Inspect the current state of an existing record or setting before editing it. This prevents changing the wrong item or unintentionally overwriting information.

## 6. Use the interaction method that matches the control

A generic “set value” operation is not reliable for all controls.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use normal text input | Newlines may be silently removed. |
| Multiline text area | Fill text, then move focus away | Some applications commit only after blur. |
| Rich-text or content-editable editor | Focus the true editable element, select existing content, use keyboard-style text entry, then blur | Direct DOM writes may not update the application's internal model. |
| Dropdown or combobox | Select by visible option text and wait for state to settle | Selection may trigger a full re-render. |
| Checkbox or radio group | Read the current state and change only when needed | A blind click can toggle a correct state off. |
| Date or time picker | Choose values and verify the rendered summary | A popover can clear related values or reinterpret typing. |
| File upload | Confirm the file, destination, and privacy impact before choosing it | Upload can begin immediately and may be difficult to undo. |

For framework-driven rich-text controls, simulate ordinary user interaction rather than changing low-level page properties. A robust sequence is: focus the actual editable element, select existing content, delete it, enter text through keyboard-style events, move focus to a neutral page element, wait briefly, then read the result back.

Some pages pair a visible editor with a hidden input. Updating the hidden input may look successful in a DOM dump while server-side validation still treats the visible editor as blank. Target the control a user would actually edit and that the application reads when submitting. If an accessibility locator resolves to an empty wrapper, inspect the labeled underlying control.

If dropdowns, checkboxes, date controls, or tabs can refresh the form, set and verify them **before** entering long text. Re-inspect afterward to ensure earlier values remain intact.

## 7. Verify every meaningful change

After filling a field or changing a setting, read it back from the rendered page. Compare the actual value with the intended value. For sensitive content, compare length, required state, or a minimal redacted summary instead of copying the full content into logs.

Check for these mismatches:

- Automation reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters changed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displays text but does not retain it internally.
- A later interaction erased an earlier value after a re-render.
- A hidden synchronization field was changed instead of the visible editor.
- A selection changed a dependent field, date, recipient, attachment, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once with a more suitable interaction method, and verify again. If the page still rejects or alters the value, report the limitation and ask how to proceed rather than silently submitting inaccurate content.

## 8. Run a readiness gate before final action

Before submitting or making a high-impact change, inspect the full relevant state again. Confirm:

- The correct account, organization, environment, and target are active.
- Every required field is present and non-empty.
- Entered values match the requested content closely enough for the task.
- Recipients, dates, options, attachments, and dependent fields are correct.
- No validation errors, unsaved-change indicators, or unexpected warnings remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a meaningful value cannot be verified, or the target is uncertain, **refuse to submit**. A partially completed page can usually be corrected; an incorrect external action may not be reversible.

Capture a pre-action screenshot, concise state summary, or structured field dump for consequential tasks. Store it only within the appropriate access boundary. Avoid pasting a large table of sensitive values into chat when a short summary and securely available artifact are enough.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists when the action is consequential.
- [ ] Authorization covers the final action, or required confirmation was obtained.

## 9. Confirm completion after acting

A final button click is not proof of success. Look for reliable evidence such as a persistent success message, confirmation reference, newly created record, changed status, sent or published item, or a saved setting that remains after a safe reload.

If the site reports an error, inspect the resulting state before retrying. Some errors are cosmetic, while a blind retry can create duplicate requests, messages, purchases, or records. If success cannot be verified, report what was attempted, the evidence available, and what remains uncertain. Do not describe an attempted action as completed.

## 10. Failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after a later edit | A component re-render reset uncommitted state | Commit and verify each field; make re-rendering selections first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the labeled underlying control and target the true editor. |
| A field looks populated but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control that the application reads. |
| Browser automation becomes unstable on a complex page | The chosen automation layer is unsuitable | Switch to a more robust browser method or authorized direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers differ | The site varies behavior by browser context | Prefer an authorized direct method; if necessary, use a verified visible session without evading protections. |
| A date or popup changes values unexpectedly | The widget has stateful close, clear, or parsing behavior | Close it through a neutral page action and re-verify all affected fields. |
| A visible error may be cosmetic | The action may already have completed | Inspect resulting state before retrying. |
| Account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## Final audit checklist

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back and verified.
- [ ] Required fields and validation passed the readiness gate.
- [ ] A pre-action record was captured when appropriate.
- [ ] Authorization or confirmation covered any consequential final action.
- [ ] Success was verified after the action, or uncertainty was clearly reported.
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
description: Verify every UI or CSS change across representative narrow, wide, short, and tall viewports using both real screenshots and programmatic layout checks. Fix and retest any failure before reporting the change as complete.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, color, background, or typography edits: a local change can affect wrapping, height, overflow, alignment, visibility, and backgrounds at other screen sizes.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Real screenshots and numerical checks catch different classes of defects, so require both.

## 1. Prepare a realistic test state

Run the real interface in an authorized test or development environment. Populate the changed surface with representative content before testing:

- long paragraphs, formatted content, and long field values;
- representative lists, cards, rows, and validation messages;
- realistic item counts or content near expected limits;
- loading, empty, and error states when the change can affect them.

Do not validate only an empty or unusually clean state. Sparse content often hides clipping, overlap, wrapping, and unintended blank space.

## 2. Choose the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages or interfaces intended for large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Include any known target viewport for the intended users or deployment environment. Explicitly test a very tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, bottom alignment, or similar vertical behavior.

Use a repeatable browser-testing system selected by the project. Run it headlessly when practical so the sweep is reproducible in local and automated environments.

## 3. Capture and inspect screenshots

Capture real screenshots at every relevant viewport and state. Use full-page screenshots when page length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect each affected component on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design now that the component's role may have changed.

Pay special attention to edge-to-edge or full-bleed changes. A component made flush with an edge can expose leftover wrapper margins or padding as visible background strips. Check every edge, not only the edge that was edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is designed to fit the viewport;
- no changed element overlaps neighboring content or its intended container;
- buttons, links, and fields remain visible and usable;
- fixed or sticky UI does not hide essential content;
- cards, lists, and form controls remain within intended bounds;
- body text retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant element rectangles with adjacent elements and container boundaries. Do not rely on rectangle checks as visual proof: they may miss exposed background areas, poor balance, or incorrect spacing.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line; reading-focused designs commonly use a narrower target of roughly 60–70 characters per line.

## 5. Require both forms of evidence

A viewport passes only when both of the following are true:

1. The screenshot shows the intended visual result, including clean edges and appropriate spacing.
2. The relevant programmatic checks show no unintended overflow, overlap, hidden controls, or out-of-bounds content.

| Evidence type | What it is most likely to catch |
|---|---|
| Screenshot inspection | Visible blank strips, incorrect backgrounds, poor visual balance, and spacing defects |
| Programmatic checks | Off-screen overflow, subtle collisions, hidden controls, and bounds failures |

## 6. Fix failures and rerun the sweep

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the failing size.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is likely incomplete. Do not ship the new defect for someone else to discover.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the widths tested, relevant heights or states, and the checks performed.

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

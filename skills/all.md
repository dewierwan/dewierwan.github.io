# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a small ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas; it is a set of meaningfully different paths, clear tradeoffs, and two or three credible choices to consider.

## 1. Gather relevant context

Start with the information provided in the request. Review any documents, discussion records, prior decisions, research, or links that are available within the current environment and relevant to the decision.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the answer, such as:

- Earlier decisions and their rationale
- Constraints, commitments, budget limits, deadlines, or dependencies
- Stakeholder concerns, ownership boundaries, and decision authority
- Evidence about what has already been tried and what happened

Use targeted retrieval rather than broad searching. If reviewing private communications or records about people, do so only for a legitimate purpose with clear authorization. Use the minimum relevant sources and details, omit unrelated sensitive information, and keep the output within the appropriate access boundary.

If material information is unavailable, state the assumption or ask a focused question. Do not invent context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that identifies:

- What decision is actually being made
- Important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should be used to compare options

The stated request may describe a symptom or a proposed solution rather than the underlying decision. For example, “Should we add a feature?” may really mean “How should we reduce a recurring user problem within a limited budget and timeline?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly asks for an immediate first pass. A wrong framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must represent a fundamentally different approach, not merely a different intensity level of the same approach. Merge near-duplicates.

Where relevant, include:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes scope, process, incentives, timing, or the framing of the problem
- At least one surprising but credible path, such as delaying, partnering, reducing scope, observing longer, or doing nothing

Do not be contrarian merely to appear creative. A “do nothing” option is useful only when waiting, learning, preserving focus, or avoiding a bad commitment has real value.

Give each option a short, memorable label that makes the approach clear. For every option, provide:

| Element | Include |
|---|---|
| What | One or two sentences describing the approach. |
| Strengths | One or two concrete advantages. |
| Weaknesses | One or two concrete disadvantages, risks, or limitations. |
| Effort | Low, Medium, or High. |

Use concrete tradeoffs. Do not soften serious weaknesses, and do not make a preferred option appear stronger by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, stakeholder burden, and confidence in the evidence. Add domain-specific criteria where needed.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are informative, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not merely why it is attractive in general.
4. Name the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless explicitly asked. Preserve meaningful choice when more than one option is viable.

## 5. Stop for a decision

After presenting the options and recommendations, wait for the user. They may:

- Select an option
- Ask for more detail on one option
- Correct the framing or constraints
- Request additional options
- Propose a hybrid approach

If the user proposes a hybrid, check whether the components are compatible and whether combining them resolves a real tradeoff rather than adding unnecessary complexity.

Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once a path is selected, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that captures the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, implementation tasks, owners, and validation measures.

A useful sequence is: brainstorm options, challenge consequential choices, make the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The options are genuinely distinct rather than variations of one approach.
- The framing reflects the actual decision, not just the first proposed solution.
- The obvious option is included when relevant.
- At least one non-obvious but credible alternative was considered.
- Weaknesses are candid and specific.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria and constraints rather than default preferences.
- The response does not expose unnecessary private, sensitive, or unrelated information.


---
name: pressure-test
description: Find the weak points in a leading strategic idea before commitment by steelmanning it, testing its load-bearing assumptions through sequential challenge, and ending with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design the implementation.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes an exercise in defending it.
- If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings in the decision process.
- If using internal communications, records, customer feedback, or other personal information, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources, omit unrelated sensitive details, and keep findings within the appropriate access boundary.

## Rules of engagement

- Be direct. Do not treat confidence, seniority, or enthusiasm as evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive responses before moving on.
- Use available evidence such as research, metrics, prior experiments, customer feedback, documented decisions, and stakeholder input. Separate facts, inferences, and forecasts.
- Refer to relevant dissenters by role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

**Template**

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If strengthening it changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, with the most consequential first. Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

| Rank | Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test or disproof |
|---|---|---|---|---|---|
| 1 | [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Name the test] |

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select the next question based on the highest-risk assumption and on the previous answer. Do not present the entire list as a questionnaire, because that enables selective answers.

Choose from these categories as relevant:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed? Why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence. Ask what observed behavior, data, comparison, or commitment supports the claim. If an answer is thin, push back before advancing.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution risks, external conditions, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or accountable role |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable early signal] | [Name the check or role] |

Warning signs must appear early enough to permit a course correction.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap; do not assume silence means agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

**Template**

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step.

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data-collection period. Next: run that test, then make the decision with the result recorded. Do not commit while the stated gap remains open.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

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

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and issuing a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make a clear decision with only as much analysis as the situation needs. The aim is not maximum certainty. It is to make a responsible call, preserve reasoning for meaningful choices, and learn from results.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may recommend an option in conversation, clearly labeled as assistant analysis. Include it in a decision record only if the user asks.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution. Plan or do the task instead of opening a decision process.
5. **Record only with permission.** “Should we do X?” asks for analysis, not creation of a record. Create or update a record only when the user asks to log, track, open, or commit it, or explicitly agrees to that practice.
6. **Protect privacy and access boundaries.** Before accessing shared communications, personnel records, customer data, or a shared register, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and details.

If a record is visible to others, confirm that its audience is appropriate. For sensitive subjects, including health, relationships, compensation, confidential personnel matters, or private financial information, offer a private record or keep the discussion in chat. Do not copy unrelated personal details into the record.

## 1. Choose the mode

Determine whether this is a new or existing decision.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review date and has not yet received an outcome assessment.

If the user explicitly names the mode, follow that instruction. Otherwise, if authorized and a decision register is available, search it for overlapping decisions before creating a duplicate.

For a resume, retrieve the existing record and append new information rather than rewriting history. For a review, use the original prediction and reasoning as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Write the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What deadline or event requires a decision?
- What result is desired?
- What happens if no action is taken?

If the question is broad and no credible options exist yet, generate options before evaluating them. Do not pressure-test a vague problem statement.

If only one viable path exists, say so directly: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time when needed. Put the choice in one bucket.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, consult relevant stakeholders |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and named prerequisite conversations |

Use this test when classification is unclear: **What would it cost to unwind this?** Consider money, time, trust, operational disruption, opportunity cost, and reputational effects. If the cost cannot be stated quickly, or is materially uncertain, the decision is probably larger than it first appears.

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

Use the user’s chosen decision register, document system, task system, or private file. A useful record contains status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

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

## 8. Audit before closing

Before announcing completion or saving a record, check:

- Is this genuinely a decision rather than a task?
- Is the scope proportionate to the stated stakes and reversal cost?
- For a hard-to-reverse choice, was the challenge gate completed or explicitly overridden with a reason?
- For a direction-setting choice, did the required stakeholder conversation and dissent pass occur, or is an explicit exception recorded?
- Are facts, the user’s stated position, and assistant analysis clearly separated?
- Did the record avoid unrelated or sensitive personal information?
- Is the record being saved only with authorization and within its intended access boundary?
- Does the prediction have an observable outcome and a review date?

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
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff. The workflow supports analysis-only work when requested and emphasizes deliberate decisions.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, automation, or operational problem whose solution is not already obvious. Do not use it for a small fix or routine task with a known implementation.

By default, work from understanding through implementation. If the user requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to "build X," work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including workarounds and failure points?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the situation meaningfully better?
- What constraints, such as timing, compatibility, security, or budget, apply?

Write a concise problem statement and descriptive requirements. Describe outcomes and constraints rather than assuming a particular implementation. If the proposed solution is poorly matched to the problem, say so directly.

Ask only for information that cannot be found in the available context, documentation, code, or authorized records. When consulting private communications or records about people, confirm a legitimate purpose and clear authorization; use only the minimum relevant information, omit unrelated sensitive details, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Include “do nothing,” “defer,” or “improve the workaround” as real options when appropriate.

Distinguish decisions by reversibility:

- **Reversible decisions:** Small, easy-to-change choices. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** Persistent data changes, public interfaces, long-lived settings, migrations, security boundaries, vendor contracts, or externally visible commitments. Pause for an explicit decision before implementation. Record the decision and rationale when useful.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in substantial design or build work.

## 3. Research the current context

Read relevant project guidance, architecture notes, service documentation, code, tests, operational procedures, and prior attempts. Look for established patterns, reusable components, and existing platform capabilities before inventing something new.

Understand compatibility requirements, deployment and release practices, supported environments, ownership boundaries, security expectations, observability, and rollback options. Follow established conventions unless there is a strong, documented reason not to.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

| Criterion | Example standard |
|---|---|
| Compatibility | Must preserve existing authentication and data behavior. |
| Delivery effort | Must fit the available time and maintenance capacity. |
| Operational risk | Must have a clear verification and rollback method. |
| Long-term cost | Should avoid unnecessary dependencies, settings, and persistent surfaces. |

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of the same design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change: clearer instructions, a process adjustment, a template, training, or an existing platform feature.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For ambiguous problems, generate a broader candidate set before narrowing. Keep each option concise: what it is, which outcome it supports, principal costs, risks, and irreversible commitments.

### Design principles for technical options

- Prefer one understandable code path over special cases that vary by runtime conditions.
- Validate strictly and fail clearly for invalid states. Do not silently convert programmer errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, public interfaces, and contracts as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Put changes in the appropriate design boundary; do not rely on expedient patches that create hidden debt.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- Problem statement and current-state evidence.
- Evaluation criteria.
- Viable options and their tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, hard-to-reverse consequences, assumptions, and open decisions.

Store the proposal in the user's chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear, date-prefixed title such as `DD MMM YYYY: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, write an implementation plan before changing the system. Include scope, ordered steps, affected components, data migration or rollback strategy, test strategy, deployment steps, and ownership of follow-up actions. Keep the plan somewhere reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, permissions, privacy, and failure behavior.

Do not claim success based only on implementation. State what was actually tested, the observed result, and what remains unverified. Commit, publish, or deploy changes only according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user action, rollout steps, monitoring, or rollback triggers.
- References to the proposal, plan, and change set where applicable.

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
description: Learn a paper, article, post, or topic through a short Socratic dialogue that uses retrieval, explanation, and application rather than passive summary. The tutor adapts its questions to the learner’s goals and demonstrated understanding.
---

# Learn with a tutor

Help a learner understand, retain, evaluate, and use a provided paper, article, post, lesson, or topic through a rigorous dialogue. Prioritize active recall and reasoning over passive explanation. The learner should do most of the intellectual work; the tutor should guide, diagnose, and steadily raise or lower the challenge as needed.

If the material includes private communications, records, or personal information, use it only for a legitimate learning purpose with clear authorization. Use the minimum relevant material, do not introduce unrelated sensitive details, and keep the discussion within the learner’s appropriate access boundary.

## Learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to recall and reconstruct ideas in their own words.
- **Ask for mechanisms.** Move beyond conclusions by asking why, how, under what conditions, and with what evidence an idea works.
- **Have the learner generate connections.** Ask for their own examples, analogies, predictions, objections, and uses before supplying any.
- **Use productive difficulty.** Make the learner think, but keep the task achievable enough for a meaningful attempt.
- **Practice transfer.** Move from the source material to unfamiliar cases, related concepts, and practical decisions.
- **Surface gaps through questions.** When an answer is incomplete or inconsistent, use questions to help the learner notice the issue. Explain directly only after a fair opportunity to reason.

## Conversation workflow

### 1. Establish prior knowledge and a learning target

Begin by asking what the learner already knows, believes, or has experienced about the topic. Identify their goal, such as understanding an argument, preparing for a discussion, evaluating evidence, or applying a method.

Ask one or two open questions:

- “What do you currently think is true about this topic, and why?”
- “What are you hoping to explain, evaluate, or do by the end?”
- “What part of this material seems most confusing or consequential to you?”

Use the response to choose an appropriate starting point and likely misconceptions to test.

### 2. Elicit the central idea from memory

Ask the learner to explain the main claim, finding, or argument without quoting the source.

Useful prompts:

- “In your own words, what is the main claim?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “If you had 30 seconds to explain this to a thoughtful friend, what would you say?”

If the learner has not yet read or reviewed the material, ask for an initial prediction or working model. Then direct them to examine the relevant section before returning to retrieval.

### 3. Select a few high-value ideas

Do not cover every detail. Choose two or three ideas that are central, difficult, consequential, or likely to be misunderstood. Explore each idea deeply using this cycle:

1. Ask the learner to state or reconstruct the idea.
2. Probe the reasoning, evidence, assumptions, and causal story.
3. Ask for a concrete example, analogy, or application.
4. Test the claim with an objection, boundary case, or alternative explanation.
5. Adjust the next question based on the learner’s response.

Keep turns short. Usually ask only one or two questions at a time.

## Question toolkit

Choose questions that require explanation rather than recognition. Adapt the wording to the learner’s knowledge and the material.

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What is the mechanism here, step by step?”
- “What evidence would distinguish this explanation from another one?”
- “Can you construct a concrete example from a familiar setting?”
- “Where might this fail, or where would it not apply?”
- “What is the strongest objection to this argument?”
- “How does this connect to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one assumption changed?”

Avoid questions that can be answered with only “yes” or “no.” If a narrow question is useful, immediately follow it by asking for reasoning.

## Responding to answers

Be warm, direct, and specific. Do not use generic praise. When an answer is strong, identify what made it useful—for example, it named an assumption, separated correlation from causation, or provided a relevant counterexample—then extend the challenge.

When an answer is wrong or incomplete:

1. Do not immediately provide the correction.
2. Point to the tension with one focused follow-up question.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, give a concise explanation of the missing distinction or reasoning step.
5. Ask the learner to restate the corrected idea in their own words or apply it to a new case.

If the learner says they do not know, invite a low-stakes attempt:

> “Take a guess based on what you do know. What seems most plausible, and why?”

Offer a hint after an attempt, or sooner when the task clearly requires knowledge the learner has not been given.

## Calibration and pacing

Increase difficulty when the learner answers easily. Ask for a counterexample, comparison, prediction, causal explanation, or application in a new domain.

Reduce difficulty when the learner is lost. Narrow the question, isolate one assumption, use a simpler example, or present a small set of competing explanations and ask the learner to defend one.

Match the learner’s energy. If they are engaged, explore the reasoning more deeply. If they are tired or overloaded, consolidate the strongest ideas rather than introducing new ones. Maintain a dialogue, not a fixed quiz: each question should respond to what the learner has actually said.

## Progress checks

Periodically provide a brief, evidence-based check-in:

- What the learner has demonstrated they understand.
- What remains uncertain, incomplete, or confused.
- The most useful next question or concept to revisit.

Do not claim mastery because the learner recognizes a term or repeats a conclusion. Look for accurate explanation, justified reasoning, and transfer to a different case.

## Closing gate

Before ending, ask the learner to convert learning into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation, application, or future retrieval prompt. End by naming the next concept or question worth revisiting.

## Guardrails

- Do not summarize the material unless the learner explicitly requests it; even then, invite their own summary first.
- Do not lecture when a well-chosen question can make the learner retrieve or infer the point.
- Do not define jargon automatically; ask the learner to define it first, then clarify if needed.
- Do not make the interaction easy merely to be encouraging.
- Do not cover the entire source superficially when a few core ideas can be understood deeply.
- Do not turn the exchange into a detached test. Build on the learner’s actual reasoning and maintain a collaborative, demanding tone.


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
description: A platform-independent workflow for drafting, revising, and auditing professional social posts with strong hooks, concrete evidence, useful substance, privacy safeguards, and focused publication handoff.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a draft, an article, a transcript, a podcast, a research finding, a carousel, or a simple topic.

The objective is not to make an announcement sound enthusiastic. It is to help the right professional reader stop, understand a useful point, and have a reason to care. The final post should sound like someone with evidence, judgment, and a real point to make, not a press release, academic abstract, or generic social-media template.

## Start with the publishing brief

Before drafting, confirm only the inputs that are not already clear:

- **Platform and format:** text post, caption, carousel or document caption, thread, article promotion, or another format.
- **Audience:** such as practitioners, founders, researchers, policy professionals, customers, partners, candidates, or a defined specialist group.
- **Purpose:** share an insight, explain a concept, announce a change, promote a longer piece, invite substantive discussion, or support a campaign.
- **Voice:** first-person or organizational voice; formal, conversational, or technical tone; preferred and forbidden words; punctuation rules; length target; approved writing samples.
- **Link plan:** whether an external link is included and where it should appear under the user’s platform strategy.
- **Disclosure boundary:** what names, quotes, outcomes, images, internal information, and source details may appear publicly.

If the user provides a writing guide, approved examples, audience research, or brand guidance, treat it as the primary voice source. Do not assume a particular person’s style, folder, publishing tool, or distribution practice.

## Scope, routing, and authorization

Identify the genre before drafting. A strong format depends on what kind of post this is.

- **Evidence or research post:** A claim based on data, a model, a report, or analysis. Lead with the finding, explain the evidence, and retain material uncertainty.
- **Announcement:** A product, organizational, or program change. Lead with what changed and why it matters to readers, not internal excitement.
- **Article, podcast, report, or event promotion:** Lead with the strongest finding, striking detail, or argument. Do not lead with “new article,” “new episode,” or “register now.”
- **Carousel or document caption:** Establish the core idea and share one or two meaningful specifics. Point to the visual material for the rest without repeating every slide.
- **Case study or outcome story:** A person’s or organization’s starting point, turning point, result, evidence, and lesson. Use only approved public details.

If the genre is unclear, ask one short routing question. For example:

> Is this mainly an individual outcome story, or should it be a broader insight post? Which details are approved for public use?

When a request relies on private communications, internal records, or information about identifiable people, proceed only for a legitimate purpose and clear authorization. Use the minimum relevant material. Exclude unrelated sensitive details, respect consent and reasonable privacy expectations, and keep the output within the intended access boundary. Do not infer personal circumstances, motivations, health information, protected characteristics, or other sensitive facts not clearly authorized for public disclosure.

## Accuracy and evidence rules

1. **Do not invent facts.** Never fabricate names, figures, quotes, dates, titles, testimonials, research findings, outcomes, or affiliations.
2. **Separate evidence from interpretation.** State what the source establishes, then label a recommendation, conclusion, or hypothesis as such.
3. **Use supported specificity.** Exact figures, dates, roles, mechanisms, and outcomes are usually stronger than vague language, but do not turn an estimate into false precision.
4. **Retain material uncertainty.** Mention wide ranges, weak data, major assumptions, or correlation-versus-causation limits when they change how readers should interpret the claim.
5. **Resolve evidence gaps early.** If a key claim lacks support, request a source, narrow the claim, qualify it, or remove it.
6. **Avoid manufactured urgency.** A concrete risk and proportionate response are more credible than broad catastrophe language.
7. **Obtain an appropriate basis for personal proof.** Public quotes, testimonials, photos, career outcomes, and client results need permission or another clear authorization for disclosure.

## Audience and voice

Write for the reader most likely to act on the post, not for everyone who might vaguely relate to it. Specificity helps the right readers recognize relevance. Broad, motivational language usually weakens credibility with a professional audience.

Use these defaults unless the user provides different guidance:

- Direct, clear, and conversational.
- Short sentences, concrete nouns, and plain verbs.
- Active voice where it improves clarity.
- One main claim per sentence.
- Sober about problems and practical about responses.
- Specific rather than promotional.
- Confident only where the evidence supports confidence.

Avoid three recurring failure modes:

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are thrilled to announce an exciting initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences full of unexplained terms. | State the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Broad disaster language without a mechanism or response. | Name the risk, evidence, uncertainty, and practical intervention. |

## Core workflow

### 1. Inspect the source before selecting the format

Do not begin with a template. Read the source and identify the strongest material inside it. Look for:

- An unusual fact or surprising number.
- A counterintuitive but defensible conclusion.
- A concrete before-and-after outcome.
- A meaningful trade-off or deliberate non-goal.
- A sharp disagreement between credible views.
- A useful framework, checklist, or model.
- A sentence that changes how readers see the problem.

The title or headline of a longer piece is often not the best social angle. The strongest thread may be buried in the middle.

When several viable angles exist, do not silently choose one. Present two to four options and let the user choose when the choice affects direction.

> I see several viable post angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [specific outcome, disagreement, or story]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework, trade-off, or implication]. Best for [audience intent].

Choose one primary thread. A social post should not summarize every section of a report.

### 2. Generate hooks before writing the body

The opening determines whether the rest is read. Generate five to ten candidate hooks before committing. If user input would be useful, show a shortlist of three to five, each with a brief strategic note.

A hook must make an honest promise that the post fulfills. It should work on its own for a reader who has not seen the source material.

Useful hook patterns include:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific evidence set] to answer one question.”
- **Number with tension:** “[Number] of [group] report [surprising result].”
- **Approved named outcome:** “[Person or role] moved from [starting point] to [specific result] in [timeframe].”
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only when the body supports it.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused question:** “Why do two credible groups reach such different conclusions about [specific issue]?”

| Hook | Strategic purpose |
|---|---|
| “[Specific claim or finding].” | Leads with a concrete result and gives the reader a reason to continue. |

Apply the **topic-swap test**: if a key noun can be replaced with an unrelated topic and the hook still works, it is probably too generic. Make the line specific to the actual evidence, problem, or audience.

Avoid generic announcements, throat-clearing, empty cliffhangers, multiple rhetorical questions in a row, broad motivational claims, and clickbait such as “You will not believe this.”

### 3. Select one structure

Choose the structure that fits the source. Do not combine several structures unless there is a clear reason.

1. **Counterintuitive claim → evidence → implication** for research, data, and argument posts.
2. **Changed mind → trigger → updated view → takeaway** for thoughtful first-person posts.
3. **Problem → why it matters → practical response** for explainers, policy, and operational content.
4. **Result → how it happened → reusable lesson** for launches, team outcomes, and approved case studies.
5. **Framework → examples → application** for posts readers may save and revisit.
6. **Specific announcement → reader relevance → next step** for genuinely notable changes.
7. **Strategic trade-off → rationale → consequence** for explaining what an organization has deliberately chosen not to optimize for and what that choice enables.

### 4. Draft: hook, tension, payoff

Use this default shape:

- **Hook:** The strongest claim, result, or tension.
- **Tension or setup:** Why it matters, what is surprising, or what assumption it challenges.
- **Payoff:** The evidence, story, framework, or practical insight. The post should still be useful if the reader does not click, swipe, or buy.
- **Soft close:** Exactly one focused question, practical takeaway, or pointer to further material.

A useful default is under 300 words, but substance and platform norms should determine length. Every extra paragraph must earn its place. Use one- or two-sentence paragraphs for mobile scanning. Use bullets only when the information is genuinely list-shaped, such as findings, reasons, steps, or categories.

For visual posts, give readers a meaningful point before directing them to the carousel or document. For linked content, put the main insight in the post and use the linked item for depth, sources, methods, or the complete argument.

## Calls to action and platform presentation

Use one close only. A good question creates a bounded space for real expertise, disagreement, or experience.

Strong closes:

- “Which constraint matters most in your work?”
- “What evidence would change your view?”
- “If you have operated a system like this, where does this model fail?”
- “The full analysis includes assumptions and source material.”

Avoid “Thoughts?”, several questions at once, or requests to comment, tag, repost, or react solely to increase reach. Engagement bait may reduce trust and can be penalized by some platforms.

Check the target platform’s formatting behavior before publishing. Do not rely on markup that will render as literal characters. Use emphasis, bullets, emojis, links, and line spacing only where they serve readability. If a platform strategy favors links in comments rather than the post, provide a separate first-comment draft; otherwise follow the user’s preferred placement.

Distribution behavior changes. Treat claims about algorithms, timing, formats, and metrics as testable hypotheses rather than guarantees. In many professional networks, useful reference material, substantive discussion, clear topical relevance, and thoughtful replies to genuine early comments can be worth testing. Compare results across multiple posts before adopting a rule.

## Editing pass: remove templated language

Run a distinct editing pass after drafting. Cut polished phrases that say little.

Replace or remove:

- Inflated verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Empty hedges such as “it is worth noting” or “one might say,” unless uncertainty itself matters.
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Abstract nouns such as “journey,” “transformation,” and “paradigm” when a concrete event can be named.
- Transition sentences that merely repeat the preceding paragraph.
- Dramatic frames such as “The truth is” or “Here is the reality.” State the point directly.
- Decorative punctuation or formatting that the platform does not support.

Follow user-provided punctuation rules. Otherwise, favor periods, commas, and line breaks over theatrical punctuation. Read the post aloud. If it sounds like generic thought leadership rather than a specific person or organization making a defensible point, rewrite it.

## Revision protocol

When the user gives feedback, revise the requested line and nearby logic first. Do not rebuild the entire post unless asked.

- If the hook is weak, offer several sharper hooks before rewriting the body.
- If a claim is overstated, improve the evidence, narrow the scope, or soften only that claim.
- If a paragraph is slow, cut setup before adding explanation.
- If a prior sentence is stronger, preserve it unless the user requests a change.
- If a source gap remains, flag it rather than filling it with plausible-sounding language.

Multiple small options are often more useful than one complete redraft, especially for hooks, closers, and uncertain lines. Be candid about weak material:

> The second paragraph depends on a broad claim that the source does not yet support. We can add evidence, make the claim narrower, or replace it with this concrete example: [example].

## Readiness gate and audit

Do not present a draft as final until it passes every relevant check:

- Does the first line earn attention when read alone?
- Does the post make one clear point rather than several competing points?
- Does it include a concrete detail, mechanism, example, number, or outcome where appropriate?
- Can a knowledgeable reader challenge the central claim and receive a defensible answer?
- Does it provide value without requiring a click, swipe, or purchase?
- Is uncertainty stated where it materially affects the conclusion?
- Is the language specific to this topic rather than reusable for any industry?
- Is the close one focused action, question, or pointer?
- Are all facts, quotes, names, images, and claims supported and approved?
- Are personal details within the authorized disclosure boundary?
- Does formatting work on the intended platform?
- Is the tone professional, respectful, and non-inflammatory for the intended audience?

If any answer is no, revise before handoff.

## Handoff format

Provide only what helps the user decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen format or delivery location.
3. Any unsupported claim, missing input, or line that remains uncertain.
4. Suggested link or first-comment text, when relevant.
5. One concise publishing reminder appropriate to the platform, such as responding substantively to genuine comments.

## Common failure patterns

- **Announcement disguised as content:** It reports internal excitement but not reader relevance. Lead with the actual change or lesson.
- **Pure teaser:** It asks readers to click but gives no useful insight. Share the main finding and use the linked material for depth.
- **Unsupported precision:** It uses a striking number without source, scope, or caveat. Verify, qualify, or remove it.
- **Generic inspiration:** It sounds positive but gives no mechanism, decision, or example. Name the action or trade-off.
- **Overpacked summary:** It attempts to cover an entire report. Select one thread and reserve the rest for follow-up posts or the original work.
- **Bolted-on promotion:** It adds a product, course, or service without a natural connection. Remove the pitch, write a separate post, or make the relationship concrete and immediate.
- **Forced engagement:** It demands reactions rather than inviting substantive response. Ask one real question or end with a useful conclusion.
- **Unapproved personal proof:** It shares an identifiable person’s story, outcome, or quote without authorization. Remove identifying details, generalize the example, or obtain permission.


---
name: case-study-post
description: Create an evidence-based professional case study post that shows a person’s credible change, the concrete mechanisms that helped, and a clear next step for the intended reader.
---

# Write a case study post

Use this workflow to turn authorized source material about a person into a concise, credible public case study. It is designed for professional social posts, and can also support community updates, newsletters, program alumni stories, or recruitment content.

The goal is not vague praise. Show a specific and supportable story: where the person started, what prompted action, what concretely helped, what happened next, what they do now, and what the reader can do.

A strong case study helps a reader recognize their own situation in the subject’s before-state. It explains the mechanism of change without claiming that a course, community, product, mentor, or organization caused more than the evidence supports.

## Authorization, privacy, and access boundary

Use this workflow only for a legitimate publishing purpose and with clear authorization to use the relevant materials. This is especially important when sources include private interviews, applications, messages, internal records, or information about a person’s career and personal circumstances.

Use the minimum relevant sources and facts. Do not include unrelated personal details, sensitive background information, private contact details, or material outside the audience and access boundary agreed for the post. Respect the subject’s reasonable expectations about what may be shared publicly.

Before drafting, establish:

| Check | Required decision |
|---|---|
| Publishing purpose | [Why the post is being made and who it should help or persuade.] |
| Authorization | [Who approved access to the sources and who can approve publication.] |
| Audience | [The intended reader, platform, and distribution scope.] |
| Public naming | [Whether the person, organization, team, and work may be named.] |
| Sensitive details | [Facts requiring explicit approval or omission.] |

If authority to use a private source or publish an identifying detail is unclear, pause and ask. Do not assume that access to information is permission to publicize it.

## Inputs

Ask for all available, authorized source material. Useful inputs include:

- An interview transcript, meeting notes, or approved recording summary
- An application, intake form, or written statement from the subject
- A current professional profile or approved biography
- Public work samples, publications, projects, announcements, or organization pages
- An internal message that documents a result, when its use is authorized
- A previous draft, outline, or notes from the subject
- The publishing platform, target audience, desired call to action, and editorial voice guide
- The subject’s approval status for named organizations, figures, quotes, and sensitive claims

Before drafting, determine whether you have enough verified information for these fields:

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns, and naming consent |
| Before-state | Previous role, field, goal, uncertainty, or constraint |
| Trigger | Why they joined, applied, changed direction, or took action |
| Intervention | Program, community, product, mentor, event, or resource involved |
| Mechanism | Concrete help, such as a realization, opportunity, conversation, feedback session, or introduction |
| Now-state | Current role, organization, team, project, output, or result |
| Timeline | Start date, outcome date, and any truthful time compression |
| Evidence | Verified roles, dates, figures, artifacts, and direct quotes |
| Cost or risk | A pay change, move, uncertainty, or career tradeoff, if relevant and approved |
| CTA | The reader’s next action and where they should take it |

If a critical fact is missing, ask focused questions before drafting. Do not guess at organization names, job titles, paper titles, dates, figures, timelines, outcomes, or causal links.

Useful questions include:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they decide to take part or make a change at that point?
4. What are the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a specific output, project, placement, publication, product, or grant that may be named publicly?
8. Did they take on a meaningful cost or risk that they are comfortable sharing publicly?
9. Which claims, figures, quotes, and names have been approved for public use?
10. Who should this post help or persuade?

## Evidence and verification rules

Never invent facts or intensify a claim for punch. If the source says a person contributed to a project, do not call them the lead. If they explored an opportunity, do not say they received it. If a work is unpublished, do not describe it as published.

Automated transcripts can mishear names, organizations, technical terms, numbers, and titles. Cross-check important transcript-derived details against a more reliable source, such as direct subject confirmation, an official public record, published work, or a current professional profile.

When sources conflict, use this default reliability order:

1. The subject’s direct, recent confirmation
2. Official public records or published work
3. A current professional profile
4. An original application or written statement from the subject
5. Interview transcript notes or automated summaries
6. Informal third-party messages

In private working notes, separate these statement types:

- **Verified fact:** A role, date, artifact, figure, or quotation supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn from the story. Use it only when evidence supports it, and phrase it cautiously.

Do not claim the intervention caused the whole outcome unless evidence supports that conclusion. Prefer precise language such as “the program helped them see the field differently,” “they learned about the opportunity through the community,” or “a conversation clarified their next step.”

## Sensitive-content gate

Require explicit subject approval before publishing any of the following:

- Compensation, pay cuts, financial hardship, or comparisons of earnings
- Health, family, immigration, legal, or other sensitive personal circumstances
- Strong criticism of a past employer, role, or career choice
- Unreleased work, confidential projects, or unpublished titles
- Direct quotations, especially criticism or strong opinions
- Claims about why an employer hired the subject
- Claims of causation, impact, or performance that cannot be verified
- Timelines or combinations of details that could reveal private circumstances

If approval is unavailable, use an honest fallback only if it remains accurate and useful. For example, replace an exact compensation claim with an approved broad statement about accepting a different role. Do not make the story more dramatic to conceal uncertainty.

## Build the story beats

Create a concise private working outline before writing. Do not expose unnecessary personal information in the final output.

### 1. Before-state

Capture the subject’s role, background, and reader-relevant uncertainty. Include an alternative path they were considering if it mirrors the audience’s current situation.

Keep only details that move the story. A long credential list, reading list, or work history usually weakens the post. Keep a detail when it makes the decision understandable or makes the change concrete.

### 2. Trigger

Identify why the subject acted at that point. They may have wanted to test whether a career path was viable, learn a field, find collaborators, solve a practical problem, or make a values-driven change.

### 3. Mechanism

Find one or two observable turning points. Strong mechanisms include:

- Realizing that a field or role was accessible to people with their background
- Finding a relevant opportunity through a community
- Having a conversation that clarified next steps
- Receiving feedback that improved an application or project
- Getting a useful introduction, workshop, resource, or referral

Avoid “the experience was transformative.” Name what happened instead.

### 4. Now-state

Record the person’s current role and, where approved, their organization, team, project, or output. Explain what the work involves in language the intended audience can understand.

Use named artifacts only when they add proof or interest. One meaningful project, publication, placement, product, or grant often does more work than a resume-style pileup.

### 5. Timeline and compression

Map the sequence from participation or starting point to the result. Calculate a short, truthful timeframe when it clarifies the story, such as “within six months” or “the following year.” Do not force a compressed timeline where the facts do not support it.

### 6. Quotes

Pull three to five candidate quotations verbatim. Favor quotes that speak to the reader’s uncertainty or identity, not only the subject’s achievement.

Look for these categories:

1. **Discovery:** “I did not know this path was open to someone like me.”
2. **Mechanism:** “I found the opportunity through the community.”
3. **Conviction:** “I would make the same choice again.”

Light trimming is allowed only when it preserves the speaker’s meaning and grammar. Never rewrite a quote into something the person did not say.

## Generate three hook options

For feed-based platforms, the first two lines determine whether readers continue. Write three distinct hooks before drafting the body. Keep each hook to two short sentences, usually under about 140 characters total when that suits the platform.

### Hook A: Discovery

Use when the target audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a concrete mechanism.

This is often the best default because it mirrors the reader’s situation.

### Hook B: Identity collision

Use when the before-and-after contrast is vivid.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This works well for a broad audience that may not share the subject’s exact initial uncertainty.

### Hook C: Stakes-led

Use only when a meaningful cost or risk is approved and likely to read as honest conviction rather than a warning.

**Formula:** The subject accepted a specific cost to do something. Now they are taking a concrete action or doing meaningful work.

Do not use a sacrifice hook if it suggests hardship is required or distracts from a more accessible message.

Choose one hook as the recommendation. State briefly why it fits the intended reader and why each alternative is less suitable.

## Draft the post

Aim for roughly 160 to 220 words unless the platform, audience, or format calls for another length. Shorter is usually stronger.

Use this sequence:

1. **Hook:** Use the recommended option.
2. **Before-state:** One short paragraph with the prior situation and, if relevant, the alternative path.
3. **Name the intervention:** State clearly that they joined the program, used the resource, or entered the community. Do not leave this connection implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then state the immediate result plainly.
5. **Current work:** Describe what they do now and why it matters in understandable terms.
6. **Optional honest cost:** Include only if approved and useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already delivered by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

If the platform may reduce distribution for external links in the post body, place the link in a comment, profile destination, or other approved location. Treat this as a platform-specific publishing decision, not a universal rule.

## Style rules

Adapt to the selected editorial voice. In the absence of a voice guide, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use concrete names, roles, dates, and figures only when verified and approved.
- After the first full introduction, use the subject’s preferred shorter name if it fits the tone and consent.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not call someone exceptional, inspiring, or brilliant when the facts can show it.
- Use contractions if the voice is conversational.
- Keep the CTA in full second person: “If you are…” and “you can…”
- Avoid emojis unless they are an explicit brand choice.
- Do not use em dashes. Use periods, commas, parentheses only when necessary, or line breaks.

On the final pass, remove common machine-like language:

- Empty transitions that repeat the prior paragraph
- Slow, date-first setup lines when an identity or outcome can lead
- Corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “cultivate”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably”
- Abstract nouns doing the work of facts, such as “journey,” “transformation,” and “paradigm”
- Hedging, softeners, and balanced “on one hand, on the other hand” constructions
- Dramatic colon frames such as “The truth is: …”
- Reflective summary sentences after the CTA

Read the draft aloud. If it sounds like a generic thought-leadership template, shorten it and replace abstractions with evidence.

## Graphic quote options

Provide three options for a visual quote card. Each should be self-contained, under 15 words when possible, and drawn verbatim from approved material.

Offer one quote from each category:

- Discovery
- Mechanism
- Conviction

Recommend one quote with a one-sentence rationale. Discovery quotes often work best because they make sense without context and mirror the reader’s uncertainty. Choose a mechanism or conviction quote instead only if it is clearer and more memorable on its own.

## Readiness audit

Before sending the draft for review, check:

- Is there a legitimate purpose and authorization for all non-public source material used?
- Is every name, role, date, figure, title, and quoted statement verified and approved for this audience?
- Have important transcript-derived details been cross-checked?
- Does the post show a concrete mechanism, not only a result?
- Does it avoid overstating causation?
- Is the intervention named clearly?
- Does the opening reflect a real audience concern?
- Is the current work understandable to a non-specialist reader?
- Have sensitive facts and direct quotes been flagged for approval?
- Is the CTA clear, audience-appropriate, and in second person?
- Are there no em dashes, unsupported superlatives, corporate phrases, or generic filler?
- Does the output omit unrelated or overly sensitive personal information?

## Delivery format

Create the draft in the user’s chosen document system if one is available and authorized. Use a clear title format such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and two alternatives
- The three graphic quote options and recommendation
- Approval items before publication
- Missing information that would strengthen the post
- The document location or link, if applicable

Do not treat the first draft as final. If feedback says “make the hook better,” generate genuinely new hooks rather than making tiny edits. If asked to make it shorter, cut secondary biography first while preserving the mechanism and outcome. If the subject rejects a sensitive line, use the approved fallback without weakening the entire story.

After final acceptance, review feedback for reusable lessons. Update this workflow only when a recurring pattern is clear, such as a missing intake question, consistent voice preference, structural preference, or repeated verification problem. Do not invent process changes from a clean review cycle.


---
name: create-editorial-cover-images
description: Create eight editorial cover-image options from an article by generating five distinct concepts, reviewing the rendered results, and producing three evidence-based improvements. It supports a user-chosen image generator, format, and visual.
---

# Create editorial cover images

Turn an article into eight finished editorial cover-image options. Develop five genuinely different concepts, generate and inspect each result, then create three additional images informed by what the first round actually revealed. The goal is a set of rendered options that belong to the article, not generic illustrations of its broad topic.

Use the image generator, publication destination, aspect ratio, delivery method, and visual style chosen by the user. Do not assume a particular account, service, browser, medium, or publishing platform. The default deliverable is finished images, not prompts. Use the prompt-only branch only when the user explicitly asks for prompts without generation.

When the source includes unpublished work, private communications, or records about people, proceed only for a legitimate purpose with clear authorization. Use only the minimum relevant material. Do not send unnecessary personal details to an image generator, and keep outputs within the user’s appropriate access and publication boundary.

## Readiness gate

Do not generate from a title alone unless the user explicitly says no further copy exists and accepts a more interpretive result. Ask for the complete article or a sufficient approved excerpt before developing concepts.

Before beginning, establish the following:

- The article or approved excerpt.
- The intended destination and its dimensions or aspect ratio.
- The selected generator and authorization to use it.
- Whether the user wants finished images, prompts only, or a version for a specific generator.
- Any restrictions, such as no people, no faces, no text, no logos, no factual depictions, or required empty space for later typography.

Reuse preferences already provided. Ask only for missing choices that materially change the result, and collect related choices together. Do not repeat the same questions during later rounds.

## Build the visual brief

Read the article end to end. Identify these points internally and use them to direct the images. Do not return a long literary summary unless the user asks for one.

1. **Central move:** The idea, realization, or change in perspective the reader should carry away.
2. **Emotional progression:** Where the article opens, shifts, intensifies, quietens, or resolves.
3. **Concrete imagery:** Objects, settings, actions, metaphors, and visual language already present in the writing.
4. **Voice and register:** For example, reflective, urgent, skeptical, hopeful, sober, intimate, or celebratory.
5. **Factual boundaries:** Details that may be shown literally and details that should remain abstract, omitted, or clearly metaphorical.

Do not invent facts, identities, events, or locations unsupported by the source. A visual metaphor can be imaginative, but it should not imply that a speculative scene is a factual depiction.

Ask only the unresolved creative questions that would affect the output. Shape answer choices around the actual article rather than using generic menus.

- **Mood:** Offer three or four plausible emotional readings, each tied to a distinct beat in the article.
- **Subject:** Offer appropriate choices such as an anonymous figure, landscape only, a single symbolic object, or abstract composition. Respect stated representation restrictions.
- **Palette:** Offer a few palettes suited to the mood. Describe specific colors plus useful non-color distinctions, such as pale versus dark, muted versus vivid, or low versus high contrast.
- **Orientation:** Confirm the crop and placement, such as wide header, square preview, or portrait cover. Use verified destination requirements when available.
- **Medium or style:** If unspecified, ask whether the user wants photography, painting, ink, collage, graphic abstraction, or another visual language.

Keep a concise working brief with the chosen mood, subject limits, palette, medium, format, generator, and publishing constraints.

## Propose five distinct concepts

Present exactly five numbered image ideas. Each must include:

- A short title.
- A one- to three-sentence description of what the viewer sees.
- A short statement of the article idea or emotional beat it expresses.

The five concepts must differ in subject, composition, and interpretive approach. Five minor variations on the same scene do not create a useful choice set. Unless the user’s restrictions rule them out, include at least one landscape-only option and one single-object or symbolic option.

Test each concept before retaining it: could the same explanation fit nearly any article on this broad topic? If so, replace it with a more article-specific interpretation. Give a one-line initial recommendation, then generate all five when finished images were requested. Do not require concept approval first unless the user asks to approve concepts before generation.

## Write self-contained visual prompts

Write one prompt per concept. Send the generator only the visual material needed to render the image. Do not paste the full unpublished article, private correspondence, or irrelevant details about real people.

Use this structure, combining sections where that improves clarity:

```text
Create one image: [medium, dimensions or aspect ratio, and overall editorial character].

Subject: [what is visible, its action, prominence, position, and relevant exclusions].

Setting: [surroundings, depth, and foreground/background relationships where useful].

Light and palette: [light source, specific colors, contrast, and transitions].

Technique: [physical qualities of the medium, texture, edge treatment, detail level, and negative space].

Mood: [feeling and its connection to the article’s central move].

Composition: [focal point, eye path, arrangement of major shapes, crop, and aspect ratio].

Avoid: [artifacts, content, or conventions that conflict with the brief].
```

Name colors specifically. “Pale ochre, dusty rose, muted blue-grey, and deep violet shadows” gives clearer direction than “warm and moody.” Describe relationships too: whether a dark form sits against a pale field, cool shadows recede, or one restrained accent directs the eye.

Describe the real qualities of the selected medium. Watercolor may require wet-on-wet washes, pigment blooms, visible paper, selective edges, and substantial unpainted space. Charcoal may require broad tonal masses, broken contours, and paper grain. Photography may require lens perspective, depth of field, credible materials, and a defined light source. Do not combine incompatible instructions simply because they sound visually appealing.

Put important exclusions next to the positive instruction as well as in the final avoidance list. For example, say “anonymous silhouette with no facial detail” in the subject description, not only “avoid faces” at the end. Unless lettering is expressly requested and appropriate for the generator, specify no text, logos, borders, watermarks, or unintended signage.

## Generate the first five

Use the chosen generator’s supported workflow. Respect account access, payment, rate-limit, consent, and approval boundaries. Do not bypass an approval gate or access restriction. If the chosen service is unavailable, report the blocker, take only safe recovery steps, and ask whether the user wants to resume later or authorize a specific alternative. Do not send the article to another service without agreement.

Create five distinct generation tasks or conversations where the platform permits. Keep a working record for every option: number, title, concept, submitted prompt, output location, status, and review notes. Preserve the exact prompt so a failed or truncated request can be repaired accurately.

Explicitly request an image. Confirm that the complete intended prompt was submitted, then confirm that an actual image completed and can be viewed at useful size. A text reply, accepted request, elapsed time, thumbnail placeholder, spinner, or progress message is not a finished image.

Start independent requests without waiting for each image only when the tool supports this safely. Keep actions sequential when they share browser focus or a workspace. If an error appears, first check whether an image was already created before retrying. Keep failed attempts separate from completed options.

## Inspect all five before improving

View every rendered image at useful size and evaluate the actual pixels, not the generator’s description or the intended prompt. Also inspect a small preview or intended crop, because a cover must communicate when reduced.

For each option, assess:

- Whether it communicates the central idea and emotional tone.
- Whether the subject or action reads quickly, with a clear focal point.
- Whether the requested medium, palette, dimensions, and composition survived generation.
- Whether it is too busy, generic, sentimental, static, literal, or vague.
- Whether anatomy, objects, perspective, construction, lettering, or rendering show visible errors.
- Whether it still works in the destination crop and thumbnail size.

Only after reviewing all five, write three new prompts. Each should identify an observed strength to retain, a visible weakness to correct, and a visual change likely to improve the result. Do not prewrite the second round before visual review.

A useful spread is often one refinement of the strongest result, one combination of strengths from different images, and one new concept that addresses a gap. Use judgment rather than forcing this pattern. Every new option must be meaningfully informed by rendered evidence.

Fix causes rather than symptoms. If an image is cluttered, reduce objects and competing focal points before adding decoration. If a painting looks like a photograph with a filter, request fewer large shapes, selective edges, and the actual marks of the medium. If a scene feels generic, reconsider the action or metaphor rather than adding detail.

Give a brief progress update explaining what the first round revealed and what the next three images will improve. Continue without requesting another selection or repeating the full brief.

## Generate, inspect, and deliver options six through eight

Generate three new images from the revised prompts. Preserve the first five so the user can compare originals and improvements. Inspect all three using the same completion checks and visual criteria. Repair a failed attempt where practical, but do not count text-only output, an error state, or an unfinished placeholder as a completed option.

Before handoff, verify that eight distinct completed images exist, that each was inspected at useful size, that each can be opened through the agreed delivery method, and that numbering and titles match the working record. Clearly identify options six through eight as the second round. If the platform supports a persistent handoff or preservation action, perform it for every completed output.

Give a short recommendation based on the rendered images. Then provide a numbered list of all eight titles and verified output locations, with the second-round options identified. Keep this list as the final deliverable block.

If access, rate limits, generation failures, or approval gates prevent completion, state exactly which options are finished and which remain blocked. Preserve useful partial work for resumption. Never claim that eight images exist when some are only prompts, placeholders, or unsuccessful attempts.

## Prompt-only branch

When the user explicitly requests prompts only, do not open generation tasks. Read the article, collect the necessary preferences, and propose five concepts. Wait for selection unless the user already selected concepts or asked for all prompts.

Write each selected prompt in its own fenced code block using the prompt structure above. If combining concepts, provide a one-line explanation before the relevant prompt. Do not describe speculative second-round prompts as visually informed improvements, because no rendered evidence exists. Put the selected prompts last, with nothing after the final prompt block.

## Adapt to another generator

When producing a version for another image generator, preserve the core concept, subject, mood, composition, palette, and format. Change only the syntax and controls required by the target tool.

Use compact prose for prose-oriented generators and subject-first descriptive phrases for phrase-oriented generators when appropriate. Verify current tool conventions before using model versions, flags, or proprietary controls. If a version choice materially affects results and cannot be verified, ask once rather than guessing. Keep variants separate and clearly labeled.

## Learn from completed work

After the user selects an image, accepts a prompt, or gives clear feedback, retain only durable, authorized lessons: recurring composition problems, missing prompt constraints, reliable medium descriptions, destination crop requirements, or verified generator behavior. Distinguish explicit user feedback from aesthetic judgment.

Do not save private article content, names, sensitive details, credentials, account information, or one-off subject matter as reusable guidance. Do not turn a single successful image into a universal style default. If no general lesson emerged, make no workflow change.


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
description: Close one month honestly, then build a small, capacity-checked, explicitly approved plan for the next month using evidence, trade-offs, and concrete commitments.
---

# Review and plan a month

Use this workflow at a month boundary to review the month ending and create an executable plan for the month ahead. A complete session normally takes 45–75 minutes: approximately half for evidence and review, and half for planning.

Review and planning belong in one session. The structural cause of a missed commitment, delivery problem, or energy drain should directly shape the structure of the next plan.

## Purpose

This workflow produces:

- An evidence-based account of what happened during the review period.
- A direct assessment of progress toward current long-range goals.
- A month-level picture of selected delivery, wellbeing, training, or personal-practice signals.
- A written **Review** for the month ending.
- A written **Plan** for the upcoming month, with a memorable theme, no more than three major outcomes, capacity limits, explicit trade-offs, and a pre-mortem.

Only gather, discuss, or retain information that serves these outputs.

## When to run it

Run this workflow when the user asks for a monthly review, asks to plan a named month, or asks to close one month and start another.

Default timing:

- On the first three days of a month, review the prior calendar month and plan the current month.
- Otherwise, review the current month to date and plan the next month. Label this clearly as a partial-month review and state the remaining days.
- If the user asks only for forward planning, review first because the evidence should shape the plan. The user may explicitly choose to skip the review.

State the date ranges before proceeding:

> Reviewing **March 2026** (01 Mar–31 Mar). Planning **April 2026**.

Ask whether “the month” means calendar dates or a practical range that includes an overlapping partial week. Record the actual planning range in the completed plan.

## Operating rules

1. **Read first; discuss second.** Show the evidence picture before reflective questions.
2. **Batch independent reads.** Gather independent evidence in one initial pass whenever the selected systems allow it. Do not repeatedly interrupt the conversation for small lookups.
3. **Use live commitments.** Assess performance against the current agreed target, not an obsolete schedule, old scope, or stale goal record.
4. **Check data quality before a harsh verdict.** Missing syncs, delayed updates, incomplete logs, and inconsistent sources can distort conclusions. Ask the user to confirm surprising records.
5. **The user chooses.** The assistant calculates, summarizes, identifies constraints, and asks hard questions. The user chooses priorities, cuts, and commitments.
6. **One decision at a time.** Do not advance to the next planning decision until the current question has a real answer.
7. **Stay at month altitude.** Set outcomes, milestones, capacity, structure, and commitments. Leave detailed weekly task blocks to a weekly planning process.
8. **No saved plan without explicit approval.** Notes and assistant drafts are not decisions. The user must restate or materially confirm the theme and commitments, then explicitly approve the plan.
9. **Use explicit dates.** Use **DD MMM** format unless the user prefers another unambiguous convention.
10. **Save useful records, not transcripts.** Preserve decisions, evidence, commitments, and constraints rather than a full conversation log.
11. **Do not lecture.** For health, training, recovery, or personal practice, present the numbers, direct conclusion, and agreed commitment. Give specialist advice only when requested and appropriate.
12. **Respect privacy and access boundaries.** Access private calendars, journals, health records, work systems, or communications only for a legitimate planning purpose and with clear authorization. Use the minimum relevant sources and facts. Exclude unrelated personal details, sensitive information, and content outside the intended audience or storage boundary.

## Step 1: Determine the range and gather evidence

Determine the review month, prior comparison month, and planning month. Then make one initial batch of reads where possible.

Use only sources the user has authorized: a task manager, project tracker, calendar, spreadsheet, notes system, health tracker, training log, or user-supplied facts. If no system is connected, ask for a concise factual inventory. Never imply that unavailable data was checked.

| Evidence area | Gather in the initial pass |
|---|---|
| Previous monthly record | Theme, promised outcomes, commitments, and previous review findings |
| Weekly records | Plans and reviews in the review range; repeated blockers, milestones, and carried work |
| Goals | Active weekly, monthly, quarterly, and annual goals; status, deadlines, and notes |
| Work delivered | Completed tasks, decisions, projects, or deliverables, grouped into useful domains |
| Calendar | Next-month travel, leave, fixed deadlines, recurring commitments, personal commitments, and meeting-heavy weeks |
| Daily signals | User-selected ratings, focus time, journals, habits, or mood notes |
| Sleep and recovery | Optional sleep duration, sleep quality, and same-source recovery trends |
| Training or practice | Optional sessions in the review and comparison months, plus the live target or commitment |

For large sources, return computed statistics and a few representative themes rather than raw entries. Long journals and month-long event lists can crowd out the actual review. Use filtering, aggregation, summaries, or an authorized delegated helper where available.

When using a helper to inspect a calendar, journal, or other private source, give it a narrow brief:

- Use only the authorized source and requested date range.
- Return a concise planning summary, not raw event or journal content.
- Identify fixed multi-day commitments, approximate meeting load by week, important recurring series, protected personal commitments, and planning anomalies.
- Flag conflicts such as meetings inside unavailable periods or likely time-zone mistakes.
- Do not use unrelated browsing, messaging, or account-access capabilities.

Before detailed monthly planning, re-read any weekly plans that overlap the beginning of the planning range. A weekly plan may already define that period in more detail. Reference and reconcile it with the monthly outcomes; do not duplicate or overwrite it.

## Step 2: Show the evidence picture

Present a compact factual picture before asking the user to explain it. Be direct, numeric where useful, and concise.

### Training, health, or personal-practice verdict

If the user has a current commitment in this area, include this section unless they explicitly put it out of scope. Compare actual activity against the live target.

Depending on the domain, calculate:

- Total volume, sessions, repetitions, or practice instances.
- Average weekly volume.
- Number of active days.
- Completion of key sessions or milestones.
- Longest gap between sessions.
- Relevant balance measures, such as routine versus demanding work, where the records support them.
- Relevant performance or recovery measures.
- Month-over-month changes.

Use this verdict taxonomy when it fits:

- **ON TRACK**: key measures meet at least 90% of target and consistency is intact.
- **BEHIND**: a key measure is approximately 60–90% of target, or there was a meaningful consistency break.
- **OFF TRACK**: a key measure is below 60% of target or there was a prolonged gap.
- **AT RISK**: an injury, safety, burnout, or sustained-decline signal makes the plan unsafe or unlikely.

Adjust thresholds only when the user’s domain requires it, and state the adjustment. If tracking may be incomplete, ask: “The record shows this. Does that match reality?” before issuing a strong verdict.

State one biggest corrective action for the next month. It must be a concrete commitment, not a complete program.

### Goals and delivery

Summarize weekly commitments as completed, missed, deferred, or rolled forward. For every active long-range goal, state whether it **advanced**, **stalled**, or **regressed**, with one short reason. Explicitly name goals that received no meaningful attention; they are often most at risk.

Also summarize completed work in a few useful domains. Avoid a wall of bullets. The question is whether effort created intended progress.

### Life signals

Include only measures the user has chosen to track. Useful measures include rating distribution and average, focus hours, low-focus days, sleep duration, sleep quality, same-source recovery trends, and repeated themes in written notes.

Flag meaningful patterns such as:

- Low average sleep or repeated short nights.
- Several consecutive low-rating days.
- An extended low-focus streak.
- A mismatch between positive numeric ratings and notes that repeatedly describe exhaustion, strain, or stress.

Averages are not complete truth. Raise a meaningful mismatch briefly and directly.

## Step 3: Reflect on the month

Start with one specific observation grounded in the evidence. Ask one question at a time and pursue no more than two or three threads unless the user wants depth.

Cover these questions before closing the review:

1. What genuinely shipped and feels like a win?
2. What cost more time or energy than it returned?
3. Was the main miss structural, circumstantial, or a genuine priority change?
4. What one behavior, boundary, or pattern must change next month?
5. If training or personal practice is in scope, what is the concrete next-month commitment?

Useful prompts include:

- “This outcome slipped across several weeks. What made it structurally hard to complete?”
- “Your ratings were stable, but your notes repeatedly mention strain. What was happening?”
- “This goal moved while others did not. What conditions made that possible?”

For a time-constrained user, the minimum viable review is the in-scope practice verdict, material wellbeing flags, one structural fix, and one concrete next-month commitment.

## Step 4: Plan the new month

A plan is not a description of events plus optimistic targets. A real plan contains a defined outcome, honest baseline, path, proof of capacity, trade-offs, forcing functions, a pre-mortem, and explicit approval.

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

Account for travel, leave, meeting-heavy weeks, fixed commitments, and recovery needs. Compare available capacity with the effort implied by the paths. If demand exceeds supply, cut, defer, reduce scope, or add real support now.

### Move 5: Make the NOT-doing list

Ask:

> What will explicitly not happen this month so these outcomes can?

The user names the cuts. A plan without a real not-doing list is a wish.

### Move 6: Add forcing functions and protective structure

Fragile outcomes need external pressure: a stakeholder expecting a deliverable on a date, a booked review, a public commitment, or a downstream owner waiting on work.

Also protect work that is vulnerable to interruption. If one outcome needs long uninterrupted work while another can tolerate fragmentation, batch the flexible work around meetings and reserve the best available blocks for the fragile work. If calendar conflicts undermine protected time, add their removal to the plan as an immediate action.

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

Do not store sensitive journal details, health information, private communications, or personal-calendar specifics unless they are necessary for the agreed review and the destination is within the appropriate access boundary. Prefer aggregated signals and concise conclusions.

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

At the end of every run, make one precise improvement to the reusable workflow, its templates, or its data mapping. Store it in the user’s selected workflow document or improvement log. If no suitable location exists, present the proposed edit as a short durable rule the user can save.

Look for a noisy read, a wrong data assumption, a misleading metric, a user correction, or a repeatable pattern that future sessions should know. Prefer one specific edit over a vague reminder.

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
- Private sources were accessed only with legitimate purpose and authorization.
- Stored output excludes unnecessary sensitive or unrelated personal details.

## Common failure modes

- Starting with prompts instead of evidence.
- Judging performance against stale targets.
- Treating incomplete tracking as proof of poor performance.
- Confusing a list of events with a plan.
- Overloading capacity and refusing to cut scope.
- Letting the assistant choose the user’s priorities.
- Saving an unapproved draft.
- Duplicating or conflicting with weekly plans.
- Treating wellbeing averages as more truthful than repeated written evidence.
- Applying generic productivity rituals instead of fixing the actual drain.
- Overwriting an existing record without resolving the difference.
- Treating a voice note, brainstorm, or imported task list as a confirmed commitment.
- Reading or storing more private information than the planning purpose requires.


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
description: Review authorized meeting records, identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only questions that require judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

Use only records the user is authorized to access for a legitimate work purpose. Review the minimum relevant sources, omit unrelated or sensitive personal details from tasks and reports, and keep task content within the appropriate access boundary.

## Purpose and operating rules

Before each run, use these outcome rules:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries commonly misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels it as an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work that was completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, expression of interest, or open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply known responsibility and delegation boundaries supplied by the user or organization. Attendance at a meeting does not make the user accountable for every workstream discussed.

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

Fetch full meeting records in parallel where the selected meeting system supports batching. Do not search for existing tasks yet: first identify people, topics, and candidate outcomes so deduplication is accurate.

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

- **Title:** short, verb-led, and specific, such as “Follow up with partner about pilot scope.”
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
- Each task links to its source record where appropriate.
- Message drafts are ready to send and follow the user’s preferences.
- Outputs contain only information appropriate for the selected task system and audience.
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
description: Complete browser-based tasks safely by choosing the least invasive authorized method, verifying account context and rendered state, and separating preparation from consequential final actions.
---

# Use a browser safely

Use this workflow for tasks that require active interaction with a website: completing rendered forms, changing dashboard settings, collecting data from client-rendered pages, testing a user flow, uploading material, or working in an authenticated account. Use it when a normal page request, supported API, or static extraction cannot reliably accomplish the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not perform a consequential final action until the account, target, page state, and authorization are clear.

A browser automation command succeeding does **not** prove that a website accepted the change. Modern applications may keep state outside the visible DOM, commit data only when focus leaves a field, replace controls during rendering, or report an error after an action actually completed.

## 1. Establish purpose, authority, and boundaries

Before opening a private dashboard, authenticated session, communication, or record about a person, establish all of the following:

- There is a legitimate task-related purpose.
- The requester has authorized the access and intended action.
- The requested account, organization, environment, and target item are known.
- Only the minimum relevant sources and information will be accessed.
- The intended result will remain within the requester's appropriate access boundary.

Respect consent and reasonable privacy expectations. Do not collect, copy, summarize, or expose unrelated private material merely because it is visible in an account. Do not place credentials, session tokens, recovery details, private records, or unnecessary personal data in logs, screenshots, code, or reports.

Define the task boundary before navigation becomes complex:

- What exact page, form, record, setting, or workflow is the target?
- What information must be entered, read, changed, or uploaded?
- What fields require user judgment rather than inference?
- Is the final action reversible?
- Does the task send, publish, pay, delete, grant access, change a plan, modify security, or create another external commitment?

If a material choice is missing or ambiguous, prepare only what is safe to prepare and ask a focused question before making the choice.

## 2. Choose the least invasive route

Use the first suitable route below. Do not move to a more privileged browser context simply because it is convenient.

1. **Supported direct interface or API.** Prefer a documented and authorized programmatic interface when it can perform the task safely and reliably.
2. **Headless browser automation.** Use this for public pages, testing environments, rendered-page extraction, screenshots, and tasks that do not require an established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing session, account-specific state, single sign-on, or a user-directed browser context.

Before automating a page, look for a direct route through official documentation, an ordinary form action, visible network requests, page source, or a supported integration. A browser form may submit structured data to an authorized endpoint, making a direct method safer and more reliable than reproducing complex UI behavior.

Do not use undocumented interfaces to bypass access controls, consent boundaries, service restrictions, payment flows, or security measures. If a site blocks automated traffic, do not attempt to evade its protections for research or routine collection. An authenticated visible session may be appropriate only for a legitimate, explicitly requested task on that site, with authorized access, where the established session is necessary.

Use a robust scriptable browser automation library directly for long, complex, or highly dynamic flows. Lightweight browser-control tools are appropriate for short, simple interactions such as reading one page or clicking one control. If the lightweight layer becomes unstable during long text entry, heavy rendering, or concurrent page operations, stop trying to rescue it and restart with the more robust method.

## 3. Protect authenticated browser context

An authenticated browser is a privileged environment. Before performing any action there:

1. Announce that you are taking control of a visible browser and state the task purpose.
2. Work in a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing tab.
3. Classify the intended context: for example, personal, work, test, staging, or production.
4. Select the profile or connected browser instance for that context directly; do not rely on a generic default or most-recently-used selector.
5. Verify the signed-in account through a reliable account indicator before visiting or changing the actual target.
6. Confirm the target object, record, or setting before editing.

Do not infer identity from a browser window title, a connection label, a tab name, a remembered default profile, or a previously observed mapping. Browser connections, names, and profile arrangements can change. If the task context cannot be verified reliably, stop and ask.

Use an account preflight gate before authenticated actions that change data. The gate should require evidence that the correct account, environment, and target have been checked. If the automation environment has a verification marker or permission flag, set it only **after** the verification actually passes. Never create such a marker in advance to unlock action tools.

A useful pre-action question is:

> Which account is active? Which environment is active? What exact item will change?

If any answer is uncertain, resolve it before editing.

Do not disable security warnings, multi-factor authentication, access restrictions, signature checks, browser protections, or anti-abuse controls. If the user must personally complete an authentication challenge, security-key prompt, or human-verification step, explain what is needed and wait rather than attempting to bypass it.

## 4. Separate preparation from commitment

Treat reversible preparation and consequential commitment as separate phases.

### Preparation pass

- Navigate to the intended page.
- Inspect controls and current state.
- Make reversible selections and fill fields.
- Verify every meaningful value.
- Capture a pre-action screenshot or structured state record when appropriate.
- Do **not** activate the final commitment control.

### Commitment pass

- Reconfirm the account, environment, target, and readiness state.
- Confirm that the page has not reloaded, re-rendered, or changed context since preparation.
- Obtain any required final approval.
- Perform the final action once.
- Verify durable completion.

For actions already explicitly authorized by the request or standing instructions, do not ask again merely because a final button exists. However, request confirmation immediately before actions that are irreversible, unusually costly, or broader in impact than the authorization clearly covers.

The following usually require explicit confirmation immediately before the final action:

- Sending messages, invitations, notifications, or applications.
- Publishing material to an audience.
- Submitting an official, externally reviewed, or non-editable form.
- Making a payment, purchase, donation, or transfer.
- Deleting records, files, or account content.
- Changing billing, subscriptions, ownership, access, security, or recovery settings.
- Any action labeled permanent, final, or impossible to undo.

For a requested, low-risk, reversible change, such as a preference adjustment or a draft update, proceed after normal verification unless the page reveals an unexpected warning or broader effect.

## 5. Inspect the rendered page before editing

Do not start by guessing selectors, filling controls by numeric position, or trusting a visual approximation. First inspect the rendered page sufficiently to identify real interactive elements.

For each relevant control, determine:

- Element type: input, text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value, current selection, required state, and disabled state.
- Validation rules, limits, formatting behavior, and any visible warnings.
- Whether an apparent field is a real editor, a wrapper, or a hidden synchronization element.
- Whether selecting an option, toggling a control, changing a date, or opening a tab triggers a re-render.

Address controls by stable semantic identity: visible label, accessible name, or an explicit label relationship. Do not address fields by DOM index where semantic identifiers are available. Component order can vary between page loads and can change after rendering.

Before editing an existing record or setting, inspect its current state. This reduces the risk of changing the wrong item or unintentionally overwriting information.

### Generic inspection pattern

Use the chosen automation system to list editable controls before writing fill logic. Record the tag, type, role, accessible label, required state, and readable value or text length.

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

## 6. Use the interaction method that matches the control

A generic “set value” operation is not reliable for every field type.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use normal text entry or fill behavior | Line breaks can be removed silently. |
| Multiline text area | Fill text, then move focus away | The application may commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select existing content, enter through keyboard-style events, then blur | Direct DOM mutation may not update the application model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle | Selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed | Clicking an already-correct control can reverse it. |
| Date/time picker | Set values, close through a neutral page action if needed, then verify the displayed summary | Popovers can clear related values or reinterpret typing. |
| File upload | Confirm source file, destination, audience, and privacy implications first | Uploading may begin immediately or be hard to reverse. |

For framework-driven editors, simulate normal user interaction rather than setting low-level page properties. A robust sequence is:

1. Focus the actual editable node.
2. Select existing content.
3. Delete it.
4. Enter new text through keyboard-style input.
5. Move focus to a neutral page element to commit the value.
6. Wait briefly for rendering.
7. Read the content back.

Some forms pair a visible editor with a hidden input. Editing the hidden input can look successful in an inspection dump while validation still treats the real field as empty. Target the visible interactive editor that the application reads. If an accessibility locator finds an empty wrapper, inspect the underlying labeled element and locate the true editor through its label relationship.

If dropdowns, checkboxes, date controls, tabs, or other choices trigger full re-renders, set and verify those choices **before** filling long or complex text. Re-inspect the form afterward and ensure earlier entries remain present.

## 7. Verify every meaningful edit

After each meaningful field entry or setting change, read the state back from the page. Compare it with the intended value. For sensitive values, compare length, presence, required state, or a redacted summary instead of printing the full value.

Check specifically for:

- A successful automation call but an empty page field.
- Lost newlines, repeated spaces, punctuation, or special characters.
- Truncation due to a single-line field or length limit.
- Text that appears visually but was not retained by the application model.
- An earlier value erased by a later control change or re-render.
- A hidden synchronization field modified instead of the visible editor.
- A dependent date, recipient, attachment, validation rule, or selection changed unexpectedly.

If verification fails, do not continue toward submission. Diagnose the control type and retry once with a more appropriate interaction pattern. If the page still rejects, alters, or cannot reliably expose the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 8. Apply the pre-submit readiness gate

Before submission or any high-impact change, inspect the full relevant state again. Confirm:

- The correct account, organization, and environment are active.
- The target item is the intended one.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Recipients, options, dates, attachments, and dependent fields are correct.
- No validation errors, warning banners, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, an important value cannot be verified, or the target is uncertain, **refuse to submit**. A partially filled form can usually be corrected; an incorrect external action may not be recoverable.

Capture a pre-action record for consequential tasks: a screenshot, concise state summary, or structured field dump. Keep it within the appropriate access boundary. Avoid exposing full sensitive values in a large inline report when a concise summary and securely retained record are enough.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Recipients, dates, attachments, and dependent options were checked.
- [ ] A pre-action record exists when the action is consequential.
- [ ] The final action and its impact are understood.

## 9. Verify completion and avoid duplicate actions

A clicked button is not proof of completion. After acting, look for durable evidence such as a success message, confirmation reference, newly created record, persisted setting, changed status, sent item, or published item that remains after a safe reload.

If the page displays an error, inspect resulting state before retrying. Some errors are cosmetic or delayed, while blind retries can create duplicate messages, requests, purchases, or records. If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Never describe an attempted action as completed without confirmation.

## 10. Failure patterns and recovery rules

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank | The application ignored a direct value change | Focus the true editor, use keyboard-style entry, blur, and read back. |
| Earlier fields disappear after later edits | A re-render reset uncommitted state | Commit and verify each field; make re-rendering selections first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible node is not the editable node | Inspect the labeled underlying control and target the real editor. |
| A field looks filled but validation says it is empty | A hidden synchronization field was edited | Use the visible control the application actually reads. |
| Automation becomes unstable on a complex page | The selected control layer is unsuitable | Restart with a more robust direct automation method or supported interface. |
| Headless and visible browsers differ | The site varies by browser context | Prefer an authorized direct interface; for an explicitly requested task, use a verified visible session without evasion. |
| A date or popup changes values unexpectedly | The widget has stateful close, clear, or parsing behavior | Close through a neutral page action and re-verify all related values. |
| An error may be cosmetic | The action may already have completed | Inspect the resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
- [ ] Necessary final confirmation was obtained before consequential commitment.
- [ ] Completion was verified after acting.
- [ ] The final report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing one, assess whether it works, or improve when it activates for the wrong requests. A skill is a focused set of instructions, plus optional resources, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the job, users, boundaries, and authorization requirements.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Review representative outputs with a person and measure objective requirements where appropriate.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and not narrowly fitted to the tests.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the finished skill.

Do not assume every project needs every step. A user may want a quick collaborative draft, a sanity check, or a rigorous benchmark. Determine where they are in the loop and help them make the next useful move.

## Communication principles

Match the user’s technical vocabulary and experience. Use plain language by default. Terms such as *evaluation* and *benchmark* are often understandable, but briefly define them if needed. Avoid unexplained terms such as “schema,” “assertion,” or “JSON” unless the user is comfortable with them.

When asking questions, explain why the answer matters. For example:

> What should a successful result look like: an answer in chat, a structured report, a file, or an external action? This determines how the skill should validate completion.

Keep the user involved at important decisions:

- Confirm intended scope before writing extensive instructions.
- Ask before choosing a restrictive policy, required tool, or approval threshold.
- Share proposed test cases before treating them as representative.
- Let human judgment lead when quality is subjective, such as tone, visual design, or strategic usefulness.
- Clearly state when an evaluation is a lightweight sanity check rather than an independent comparison.

If a skill uses private communications, records, or information about people, require a legitimate purpose and clear authorization. Use only the minimum relevant sources and information, omit unrelated or sensitive details, respect consent and privacy expectations, and keep results within the appropriate access boundary.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea such as “I need a skill that prepares recurring project updates.” Start with discovery and a first draft.

### B. Existing draft or installed skill

The user already has instructions and wants them edited, simplified, tested, or optimized. Preserve the established skill identity unless the user explicitly asks to rename it. Read the current instructions and resources before proposing changes.

If the current location is not writable, make an editable copy in a user-approved working location. Do not overwrite the original until the user approves the revision or has a recovery path.

### C. Workflow demonstrated in the conversation

The user may say, “Turn what we just did into a skill.” Extract what is already known before asking questions:

- Inputs the user supplied.
- Approved tools, sources, and permissions.
- The order of decisions and actions.
- Corrections the user made.
- Observed input and output formats.
- Acceptance criteria and quality checks.
- Conditions that changed the approach.

Summarize the inferred workflow and list gaps for confirmation. Do not silently convert a one-time workaround or personal preference into a general rule.

### D. Evaluation or optimization request

The user may have a finished-looking skill and want to know whether it helps. Go directly to test design, evaluation, and targeted revision. Do not rewrite a skill merely because a rewrite is possible.

## 2. Capture intent and scope

Before drafting, collect enough detail to define a coherent, reusable job. Adapt the following questions to the request rather than asking all of them mechanically.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Trigger:** What user requests, wording, or situations should activate it?
3. **Inputs:** What information, files, examples, systems, or approved sources can it use?
4. **Authorization:** What access is permitted, who owns the information, and what actions need confirmation?
5. **Outputs:** What should it produce or change? Is there a required format?
6. **Success:** How will the user know the result is correct, useful, and complete?
7. **Boundaries:** What should the skill not do? When should it ask, decline, or return work to the user?
8. **Variations:** What common cases, difficult cases, or exceptions materially change the workflow?
9. **Dependencies:** Does the work require capabilities, reference material, templates, scripts, or user-provided access?
10. **Testing:** Should the skill be tested with realistic example requests?

Recommend testing when outputs are objectively checkable, the workflow is consequential, the skill will be used repeatedly, or a revision claims to improve an existing skill. For subjective tasks, recommend representative human review rather than artificial numerical scoring.

Useful choice questions include:

- “Should the skill make a best effort when information is missing, or stop and ask?”
- “Should it produce a concise answer, a detailed report, or let the user choose?”
- “May it use any connected source, or only sources the user explicitly approves?”
- “Which actions are safe to perform automatically, and which require confirmation?”

### Research before drafting

If relevant documentation, similar skills, user-approved references, or domain standards are available, review them before drafting. Research should reduce burden on the user, not replace their authority over requirements.

Use research to identify:

- Existing conventions and output standards.
- Constraints of an available tool, system, or file format.
- Reusable patterns from comparable tasks.
- Safety, privacy, compliance, or approval requirements.

If sources conflict or requirements remain uncertain, identify the uncertainty instead of guessing. Do not access private systems or personal records merely because they are technically available; confirm that the purpose and authorization are appropriate first.

## 3. Choose the skill structure

A skill should be focused enough that users and the AI can predict what it does. One skill may support variants of the same job, but separate unrelated jobs when they have different audiences, permissions, sources of truth, or definitions of completion.

A typical package can contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional material read when needed
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help decide whether to activate the skill.
2. **Core instructions:** The workflow needed for most requests.
3. **Supporting resources:** Detailed references, templates, and scripts used only when relevant.

Keep core instructions readable. If they become too long, move specialized material into clearly named references and state exactly when each reference should be used. Large reference files should include a table of contents or other navigation.

Organize skills with multiple variants by variant. For example, a deployment skill might include one core selection workflow and separate guidance for each supported environment. The AI should select and read the relevant material rather than load everything by default.

### Use scripts for repeatable, deterministic work

If test runs show the AI repeatedly reconstructing the same helper procedure—such as file validation, data conversion, report assembly, or calculation checking—consider bundling a reusable script.

A script is valuable when it is:

- Deterministic or easier to verify than free-form reasoning.
- Reused across multiple requests.
- Safer or less error-prone than rebuilding the procedure.
- Clearly within the user’s intended authorization scope.

Document what each script does, its inputs, expected outputs, limitations, and when not to use it. Do not add automation solely because it is possible. Never bundle code intended to conceal actions, bypass access controls, exfiltrate data, or compromise systems.

## 4. Write the skill

Draft the skill in clear, imperative language. Explain the reason behind important instructions, especially when a rule prevents a predictable failure. A capable AI can adapt better when it understands the goal and tradeoff than when it receives a long list of unexplained prohibitions.

Use the following sections where they apply.

### Purpose and scope

State the job, intended users, and boundaries. Make clear whether the skill produces an answer, creates a file, changes a system, or guides a person through a process.

### Inputs and prerequisites

List required information, permitted sources, required capabilities, and optional inputs. State what to do when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If the source is unavailable, ask the user for an export or provide a draft clearly marked as incomplete.
```

When people’s information is involved, specify the legitimate purpose, allowed audience, and handling expectations. The skill should include only information needed for the task and should avoid repeating sensitive details in outputs unless necessary and authorized.

### Workflow

Give the normal action sequence and include meaningful decision points rather than trying to enumerate every possible scenario.

A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Confirm unclear requirements only when the answer materially changes the work.
3. Gather evidence from approved, relevant sources.
4. Perform the task using an appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limitations.

Use conditional rules where needed:

```markdown
If the request includes a required template, follow it.
If no template is provided, use the default report structure below.
If a requested change could overwrite important work or affect an external system, describe the impact and ask for confirmation before proceeding.
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

Avoid rigid formatting when the task’s value depends on adapting to context. In that case, define goals and give examples instead of prescribing a fixed shell.

### Quality and safety checks

State checks needed before completion. Examples include confirming required fields, validating calculations, preserving original data, citing key evidence, flagging uncertainty, and confirming authorization for consequential actions.

Skills should behave in ways users reasonably expect from their description. Do not create misleading skills or instructions that hide actions, bypass authorization, extract confidential information, damage systems, or facilitate unauthorized access. If a request is unsafe, deceptive, or outside the available authority, explain the limitation and offer a safe alternative where possible.

### Failure behavior

Describe recovery behavior in general terms:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** Explain what could not be verified and offer an alternate method.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, report the issue, or request guidance.
- **Permission-sensitive action:** Pause for confirmation before an irreversible, external, or high-impact action.
- **Sensitive information:** Minimize collection and disclosure, exclude unrelated personal details, and ask for direction if the allowed audience is unclear.

### Examples

Include a small number of generalized examples only when each teaches a distinct pattern. Examples should illustrate the shape of a good response, not replace reasoning or encode private circumstances.

## 5. Write a strong description

The skill description is primarily a routing instruction: it helps an AI decide whether the skill applies to a user request. It should state both **what the skill does** and **when to use it**.

Write descriptions that cover realistic user language, including requests that imply the job without naming it. AI systems may fail to activate a useful skill unless relevance is explicit.

A good description includes:

- The task or outcome.
- Common contexts or phrasing that indicate the task.
- Important limits that prevent harmful or costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use for requests involving progress updates, leadership summaries, milestone reviews, risks, decisions, or next steps, including requests that imply a status report without naming one.
```

Do not put the entire procedure in the description. Do not rely on vague labels such as “help with documents.” Do not make the description so broad that it captures nearby work better handled by another skill.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description explain when to activate the skill?
- Are required inputs, permissions, and outputs clear?
- Does the workflow explain why key checks exist?
- Does it tell the AI what to do when information is missing?
- Are there unnecessary rules, repeated guidance, or brittle wording?
- Does it avoid assuming a specific person’s tools, habits, access, or terminology?
- Does it protect privacy and keep outputs within the permitted audience?
- Would a capable AI retain enough freedom to handle normal variation?

Prefer a lean, understandable prompt over one filled with rules that do not affect outcomes. Excessive absolute language is a warning sign unless the behavior is genuinely non-negotiable, such as an authorization or safety boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create a small evaluation set. Start with two or three realistic prompts resembling genuine user requests. Share them with the user and invite additions or corrections before relying on them.

For each test case, record:

- A descriptive identifier or name.
- The user prompt.
- Supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

A portable structure is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached approved updates. Flag information you cannot verify.",
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Use cases that cover meaningfully different situations:

- A typical successful request.
- A request with incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic case that changes the workflow.
- A request that should require approval, safe refusal, or privacy-aware handling, when relevant.

Do not write tests that merely repeat the skill’s language. Vary phrasing, detail level, and user sophistication. Use generalized, authorized test data; do not include real confidential details merely to make a test feel realistic.

## 8. Run comparisons

When the environment supports independent runs, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revised version with the previous version.

Run each configuration under comparable conditions. If parallel execution is available, start skill and comparison runs for all test cases together. This reduces timing differences and avoids selectively changing the baseline later.

Store outputs in a clear iteration structure:

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

For each run, preserve the prompt, approved input files, output, and available metadata such as elapsed time and token or compute use. Record timing when the execution environment reports it, because some systems do not preserve it afterward.

If independent agents or parallel execution are unavailable, perform a transparent sanity check instead: follow the skill for each test prompt, save the results, and ask the user to review them. Do not describe this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While runs are underway, draft objective checks where they genuinely help. Explain the checks to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A produced file opens and includes required fields.
- Calculated values match a known source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- Output includes citations or source references when required.

Each check should have a descriptive statement, a pass/fail result, and evidence:

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

Use scripts for programmatic checks whenever practical. Automated checks are faster, more repeatable, and reusable across iterations.

Do not force numerical checks onto subjective tasks. Writing quality, usefulness, tone, aesthetics, and strategic judgment generally need human review. A weak proxy can make the skill optimize for the metric instead of the user’s real goal.

## 10. Review results with a human

Present both outputs and measurements. Use an available review interface that lets the user inspect each test case, compare configurations, and leave feedback. If no such interface exists, present results clearly in conversation or as accessible files.

For each test case, show:

- The original prompt.
- Relevant supplied inputs.
- The skill output and comparison output, if available.
- Objective grades and evidence.
- Timing or resource data, if available.
- A clear place for the user to state what worked and what should change.

Ask focused questions:

- “Which result would you trust in normal use, and why?”
- “Did the skill add steps or detail that were not valuable?”
- “What was missing, misleading, or hard to use?”
- “Would this work for similar requests with different wording or data?”

Empty feedback can indicate that a case is acceptable, but it is not proof that all cases are solved. Consider the outputs and measurements too.

## 11. Analyze results beyond pass rates

Aggregate results where possible: pass rate, average time, average resource use, and variation. Make reports easy to compare by placing the revised-skill result before its baseline counterpart.

Then perform an analyst pass. Aggregate statistics can hide important patterns:

- **Non-discriminating checks:** A check passes with and without the skill, so it does not measure the skill’s added value.
- **High variation:** Comparable runs differ substantially, suggesting ambiguity, environmental instability, or unreliable instructions.
- **Tradeoffs:** The skill improves quality but imposes excessive time or resource costs.
- **Failure concentration:** Several failures share a root cause, such as unclear source selection or missing output rules.
- **Unproductive work:** Execution traces show redundant planning, unnecessary research, or excessive formatting.
- **Repeated reconstruction:** Multiple runs independently create the same helper process, suggesting a bundled resource would help.

Do not treat a small benchmark as conclusive. Use it as evidence for the next revision.

## 12. Improve without overfitting

Base revisions on user feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from a complaint. If one output omitted a source note, do not add a rule tied only to that test. Clarify the broader condition: when evidence comes from incomplete or mixed sources, distinguish verified information from assumptions.

Use these improvement principles:

1. **Fix causes, not examples.** Design for future requests, not just current tests.
2. **Keep instructions lean.** Remove guidance that does not change behavior or causes wasted effort.
3. **Explain intent.** State why an action protects quality, usability, privacy, or safety.
4. **Add reusable assets only when justified.** Bundle scripts, templates, or references when repeated work demonstrates their value.
5. **Preserve useful behavior.** Do not lose parts users already value while fixing another problem.
6. **Expand coverage gradually.** Add a test when it represents a real class of failure, not every isolated incident.

After revision, rerun the full test set in a new iteration. Use the same comparison policy, show new outputs beside prior outputs where possible, and collect feedback again.

Stop when one or more conditions is true:

- The user says the skill is ready.
- Feedback is consistently positive or empty across meaningful cases.
- Objective requirements are reliably met.
- Further revisions are not producing meaningful improvement.
- Remaining weaknesses require unavailable information, missing capabilities, or a user decision rather than better instructions.

## 13. Optional blind comparison

For a more rigorous comparison of two skill versions, use blind review. Give an independent evaluator two outputs without identifying which version produced each. Ask the evaluator to judge them using a shared rubric, then reveal the mapping only after the judgment is recorded.

Blind comparison is useful when:

- Two versions have similar pass rates but differ in qualitative quality.
- The author or reviewer may favor a newer version.
- The decision has material cost or importance.

Keep the rubric tied to user value: correctness, completeness, clarity, adherence to constraints, safety, privacy, and practical usability. Analyze why the preferred output won before revising again.

## 14. Optimize triggering behavior

After the workflow itself is stable, assess the description that controls activation. Do this after—not before—the skill is otherwise useful.

Create a realistic set of trigger queries containing both cases that **should trigger** and nearby cases that **should not trigger**. Use roughly balanced coverage and enough detail that consulting a skill would be useful.

Positive cases should vary in wording and context:

- Formal and casual phrasing.
- Requests that name the task directly and requests that imply it.
- Common use cases and less common valid cases.
- Cases where another related skill might compete but this skill should be selected.

Negative cases should be difficult near-misses, not obviously irrelevant requests. They should share terms or concepts with the skill but belong to another job, require another capability, or lack the conditions that make this skill appropriate.

```json
[
  {
    "query": "I need a concise leadership update from these approved team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what a project status report is and when teams use one?",
    "should_trigger": false
  }
]
```

Review the query set with the user before using it. Poor trigger tests produce misleading descriptions.

If the environment permits repeated activation tests, separate the queries used to improve a description from held-out queries used to choose the final description. Choose the description that performs best on held-out cases, not merely the one that fits the examples used during editing.

A simple one-step request may not activate a specialized skill even when its description matches, because an AI may handle it directly. Trigger tests should therefore use substantive requests for which the skill would provide real benefit.

When applying the chosen description, show the user the before-and-after wording and the evaluation results. Ensure the final description remains honest about the skill’s scope.

## 15. Package and hand off

When the skill is ready, package the core instructions and only resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately represents activation conditions.
- Instructions do not depend on private local conventions, undeclared tools, or personal access.
- References and scripts are present, clearly named, and documented.
- No credentials, confidential data, personal identifiers, private URLs, or sensitive examples are included.
- Test materials are retained only when they are safe and useful.
- The user can understand how to install, access, adapt, and test the skill in their chosen environment.

Provide a short handoff note explaining what the skill does, required capabilities, known limitations, authorization expectations, and how the user can verify it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an accurate description that routes appropriate requests, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for real recurring work.


---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, tall, and target viewports using both real screenshots and programmatic layout checks. Fix every failure and rerun the relevant sweep before reporting the work as完成.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, background, or typography edits: a local change can affect wrapping, height, overflow, alignment, and background visibility at other viewport sizes.

A bounding-box measurement alone is not sufficient. One desktop and one mobile screenshot are not sufficient. Real screenshots and numerical checks catch different failure types, so use both.

## 1. Prepare realistic test states

Run the actual interface in an appropriate test environment. Populate changed surfaces with representative content before capture:

- long paragraphs, formatted text, and long field values;
- representative lists, cards, rows, and validation messages;
- realistic item counts, including content near expected limits;
- loading, empty, and error states when the change can affect them.

Do not validate only a clean or empty state. Sparse content often hides clipping, overlap, unexpected whitespace, and wrapping failures.

## 2. Select the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages, dashboards, or interfaces expected on large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short viewport of about 700 px;
- a tall viewport of about 1400 px or greater.

Include any known target viewport supplied by the requester or product requirements. Explicitly test a very tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, bottom alignment, or similar vertical behavior.

Use a repeatable headless browser automation capability chosen for the project. Capture evidence from the rendered interface, not only from style rules or element measurements.

## 3. Capture and inspect screenshots

Capture screenshots at every relevant viewport and content state. Use full-page screenshots when page length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect each changed component on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design now that the component's role has changed.

Give extra attention to full-bleed, edge-to-edge, or flush changes. Making a component flush on one side can reveal leftover margin or wrapper padding on another side as a visible background strip. Verify every edge, not only the edge directly edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result solely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshot inspection. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is intended to fit the viewport;
- no changed element overlaps neighboring content or escapes its intended container;
- buttons, links, and form fields remain visible, reachable, and usable;
- fixed or sticky UI does not hide required content;
- cards, lists, and controls remain within intended bounds;
- body text retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare the bounding rectangles of relevant elements with adjacent elements and container boundaries.

For prose-heavy pages, flag excessively wide text measures. A useful warning threshold is roughly 80 characters per line; reading-focused designs commonly target about 60–70 characters per line.

## 5. Require both forms of evidence

Measurements can miss visible defects such as exposed background strips, poor visual balance, and unexpected blank regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and all relevant programmatic checks pass.

## 6. Fix failures and retest

If any viewport or realistic state fails:

1. Stop the completion, review, or release process.
2. Identify the layout rule or structural behavior causing the failure.
3. Fix the underlying cause rather than adding a narrow viewport-specific cosmetic patch.
4. Rerun the complete relevant sweep, not only the viewport that exposed the problem.

If a change makes one viewport correct but breaks another, reconsider the diagnosis. The layout model or component constraint is likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights and states, and the checks performed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, state that clearly and do not represent the UI change as complete.


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

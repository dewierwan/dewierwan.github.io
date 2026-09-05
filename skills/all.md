# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a small ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not to make a long list of ideas. The goal is to identify meaningfully different paths, show the tradeoffs honestly, and leave the user with a small set of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources available in the current environment, review the minimum material needed to understand the decision.

If the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Constraints, commitments, budgets, or deadlines
- Stakeholder concerns, responsibilities, and approval boundaries
- Evidence about what has already been tried

Use targeted retrieval only when it could materially change the options. When reviewing private communications or records, have a legitimate purpose and clear authorization; use only relevant information, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

Do not search broadly by default. If important context is unavailable, state the assumption or ask a focused question rather than inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- What the user is actually deciding
- Important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should distinguish the options

The user’s wording may describe a symptom or an assumed solution rather than the actual decision. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited delivery window?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious and low-stakes, or when the user explicitly requests an immediate first pass. A wrong frame creates polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless there are genuinely fewer meaningful paths. Each option must be a fundamentally different approach, not merely a different intensity level of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes process, incentives, scope, ownership, or the framing of the problem
- At least one surprising but plausible option, such as delaying, partnering, reducing scope, observing longer, or doing nothing

Do not be contrarian merely to seem creative. A wait-or-do-nothing option is useful only when timing, learning, risk reduction, or avoiding distraction has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

- **What:** One or two sentences describing the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limitations.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option appear stronger by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, evidence strength, and stakeholder burden. Use domain-specific criteria where they matter more.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are useful for comparison, but state clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, goals, and constraints—not why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may:

- Choose an option
- Ask for more detail on one option
- Correct the framing or constraints
- Request additional options
- Combine options into a hybrid

If the user proposes a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than adding complexity. Do not begin implementation simply because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity according to consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, significant staffing decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that captures the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, implementation tasks, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before responding, verify that:

- The framing reflects the real decision rather than only the initial wording.
- The options are genuinely distinct.
- At least one plausible non-default path was considered.
- Strengths and weaknesses are candid and concrete.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than the assistant’s preferences.
- The output does not expose unnecessary private, sensitive, or unrelated information.


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

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing a single idea too early can turn the process into defending it.

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision instead.

## Evidence, access, and privacy

Use research, metrics, prior experiments, customer feedback, documented decisions, and stakeholder input where available. If reviewing private communications, records, or feedback about people, do so only for a legitimate decision purpose and with clear authorization. Use the minimum relevant sources and details, omit unrelated personal or sensitive information, and keep the output within the intended access boundary.

Distinguish facts, interpretations, estimates, and forecasts. Do not invent evidence, stakeholder views, or agreement.

## Rules of engagement

- Be direct. Do not treat confidence as evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Prioritize questions against the assumptions whose failure would do the most damage.
- Refer to credible dissenters by relevant role, such as a finance owner, delivery lead, customer representative, domain expert, legal or risk reviewer, or skeptical peer. Do not assume their views without consulting them.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's actual intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

**Template**

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, starting with the assumption most likely to undermine the decision.

| Rank | Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|---|
| [1] | [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Name the test] |

Make assumptions observable where possible. Replace “users will value this” with a defined behavior, target group, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions and adapt later questions to the answers received. Do not show the full list as a questionnaire, because that permits selective answering.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence. Ask what observed behavior, data, comparison, or commitment supports that belief. Record a short conclusion after each answer: supported, uncertain, contradicted, or untested.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution problems, external conditions, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable signal] | [Name the check or accountable role] |

The warning sign must appear early enough to change course. If no practical warning exists, treat the risk as harder to manage and revisit reversibility.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection and whether their view has been sought.

| Relevant role | Strongest plausible objection | Consulted directly? | What is needed next? |
|---|---|---|---|
| [Role] | [Objection] | [Yes, no, or partly] | [Conversation, evidence, or decision constraint] |

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss. If a relevant perspective has not been consulted, mark this as an evidence gap rather than treating silence as agreement.

## 6. Define what would change the decision

Require one sentence that names the evidence that would reverse or materially alter the position.

**Template**

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data-collection period. Next: run that test, then make the decision with its result recorded.
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

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, exposing unnecessary private information, and giving a positive verdict without falsifiable criteria or monitoring.


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
description: Search only the sources justified for the user’s purpose, then turn the findings into a proportionate, evidence-linked context brief that supports an upcoming action or decision.
---

# Gather context

Use this workflow when the user needs to understand a person, organization, project, topic, or decision before writing, deciding, meeting, pitching, planning, or taking another consequential action. The result is a concise, organized context brief with direct links to supporting evidence.

## 1. Confirm purpose, access, and output boundary

Start by identifying what the brief must help the user do. Examples include preparing for a call, deciding between options, assessing project status, drafting outreach, or understanding a market question.

Use private communications, internal records, meeting transcripts, or personnel-related systems only when all of the following are true:

- The user has a legitimate purpose and clear authorization to access them.
- The source is relevant to the stated purpose.
- The information used is the minimum needed to answer the question.
- The intended recipient and destination are appropriate for the sensitivity of the material.

For a person-focused request, apply an especially narrow boundary. Do not search private messages, personal notes, or broad people databases merely because they are available. Omit unrelated personal details, sensitive information, and speculation. Do not infer private traits. Respect consent, confidentiality, need-to-know limits, and reasonable privacy expectations.

For hiring or assessment work, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Do not use unrelated personal information to characterize a person or support a recommendation.

If the purpose, authorization, subject identity, or intended destination is unclear, ask one focused question before accessing private sources. Otherwise, proceed without over-questioning.

## 2. Right-size the research effort

Choosing the effort level is the most important judgment in this workflow. Do not automatically perform a full sweep of every connected system.

| Tier | Use when | Expected work | Output |
|---|---|---|---|
| Quick | The user asks for a reminder, simple status, or immediate answer. | Check one to three obvious sources with one or two focused queries each. | A few evidence-linked bullets. |
| Standard | The user needs reliable context for normal planning, communication, or a routine decision. | Search several relevant sources, inspect the strongest records, and compare findings. | A compact structured brief. |
| Deep | The decision is high-stakes, externally visible, costly to reverse, or depends on a detailed history. | Search broadly, use multiple queries per relevant source, inspect primary records, verify important claims, and reconcile conflicts. | A full context brief with clear gaps and source groups. |

When uncertain, choose the lighter tier and state it briefly: “I’ll do a standard review of messages, documents, and recent meeting notes; I can expand it if needed.” Escalating later is inexpensive. Over-gathering can waste time, expose unnecessary private information, and bury the useful answer.

Avoid both failure modes:

- **Over-gathering:** searching every available system, collecting marginal facts, or producing a long report for a simple status question.
- **Under-gathering:** relying on one convenient source when the request clearly calls for broader context, such as a decision that may depend on a meeting transcript or a project document.

For each possible source, ask: **Would a sensible researcher expect this source to contain information that could materially change the answer for this request?** Relevance and effort tier both determine whether to search it.

## 3. Classify the subject and set a time window

Classify the request before searching. This determines the most useful source clusters.

| Subject type | Usually relevant source capabilities | Main research focus |
|---|---|---|
| Person | Direct correspondence, internal messages, meeting notes, calendar history, authorized relationship records, public profiles. | Current role, relationship history, commitments, and context for the next interaction. |
| Organization | Public website, public reporting, correspondence, internal discussions, partnership or pipeline records. | Current position, relationship history, strategic relevance, and decision-makers. |
| Project or initiative | Project documents, internal messages, shared files, task systems, meeting notes, code, or operational data where relevant. | Status, decisions, ownership, risks, blockers, and next steps. |
| Topic or question | Public research, prior internal thinking, technical documents, strategy notes, and relevant discussions. | Definitions, current evidence, options, trade-offs, and unanswered questions. |
| Decision | Sources relevant to each option, including prior decisions, owner input, operational data, and authoritative records. | Options, evidence for and against, dependencies, risks, and what would change the recommendation. |

Use a default time window suited to the request, such as recent months for a current-status question. Expand the window when the relationship, project, or decision has a longer history. State the window in the brief when it matters.

If a name or topic could refer to multiple things, ask one tight disambiguation question. For example: “Do you mean the prospective partner or the internal project with the same name?” Do not begin an expansive search against an uncertain target.

## 4. Select and search sources

Sources explicitly named by the user are mandatory, provided access is authorized. They are not necessarily exhaustive: add another source only when it is clearly likely to contain decision-relevant evidence.

Typical source capabilities include:

- **Email:** Search direct correspondence and relevant mentions in threads involving others. Read enough of each thread to understand the decision, not merely the subject line.
- **Internal messaging:** Search names, organization names, project terms, and related participants. Preserve direct links to load-bearing posts or threads.
- **Knowledge bases and shared documents:** Search workspace content rather than relying on broad automated summaries. Open the most relevant pages in full. If documents support tabs, sections, or embedded subdocuments, inspect all relevant parts before drawing conclusions.
- **Calendar and meeting material:** Use past events to establish relationship history and upcoming events to explain urgency. If a recent meeting is discovered, especially one near the requested decision or conversation, retrieve its authorized notes or transcript. It is often the best account of what was actually agreed.
- **Structured operational records:** Use only systems relevant to the question, such as an applicant system for an authorized hiring review, a project tracker for status, a customer record for relationship history, or product analytics for usage questions. Prefer the canonical record over stale copies.
- **Code and technical records:** For engineering topics, inspect the relevant repository, current implementation, change history, issue tracker, and operational evidence as appropriate.
- **Public web:** For people and organizations, prioritize official sites and current public profiles. For topics, use several search angles and distinguish primary research from commentary.

For quick and standard work, search inline and inspect the strongest results. For deep work across many independent sources, parallelize read-only research only if it genuinely saves time. Give each parallel researcher a clear source cluster and require a short digest with evidence links, not an unfiltered dump.

Use multiple queries in deep reviews: subject name, organization, project terms, related stakeholders, and likely aliases. Do not conclude that a source contains nothing after one weak query. Conversely, do not keep searching after the answer is sufficiently supported.

## 5. Validate evidence and manage gaps

Prefer current, primary, and authoritative evidence. A signed decision record, direct meeting transcript, current public profile, or source document is generally stronger than a summary, memory, or second-hand discussion.

When sources conflict:

1. Check dates and authorship.
2. Prefer the source closest to the event or decision.
3. Verify whether one source is stale, incomplete, or discussing a different entity.
4. State the conflict and the reason for the conclusion when it remains material.

Never invent a link, citation, title, date, or source access. Verify links before including them. Every factual claim derived from a source should include a direct, clickable route to the supporting item whenever the system permits it.

If a source judged relevant is unavailable, returns no usable results, or cannot be accessed, state that explicitly under gaps. Do not silently substitute a nearby source and imply the expected source was checked. A deliberately skipped source need not be listed as a gap.

If a connected source fails, attempt safe, tool-appropriate diagnosis first: confirm the configured capability, check authorization state, retry a narrowly scoped read, and inspect available tool documentation. If user action is still required, report the exact failure, what was tried, and the single remaining action, such as completing authorization or restarting the connection. Do not provide environment-specific repair instructions unless they match the user’s environment.

## 6. Synthesize by theme, not by tool

Write for the action the user is about to take. Lead with the facts that matter most. Do not present a chronological log of searches or a pile of source summaries.

Use this structure, adapting headings to the subject and effort level:

```markdown
## [Subject] — context brief
*Scope: [quick/standard/deep]. Sources reviewed: [source categories]. Window: [dates].*

## TL;DR
- [Most decision-relevant finding with a direct evidence link.]
- [Current state, risk, opportunity, or recommendation-relevant fact.]
- [Important uncertainty or immediate next step.]

## What we know
### [Theme]
Synthesized finding with inline evidence links.

### [Theme]
Synthesized finding with inline evidence links.

## Relationship or timeline
Relevant history, commitments, decisions, and changes over time.

## Open questions and gaps
- [Question not answered; likely source or owner.]
- [Relevant unavailable or empty source, if applicable.]

## Key sources
- [Source title]([verified direct link]) — why it matters.
```

A quick brief may include only a title, TL;DR, and key sources. A deep brief should include the full structure, but keep prose scannable. Use short paragraphs, meaningful headings, dates where useful, and bullets for decisions, risks, and open questions.

## 7. Deliver in the appropriate place

Deliver short briefs directly in the conversation. Make the brief the final block of the response; do not append a meta-summary that makes copying difficult. If offering a follow-on task, such as drafting an email or preparing questions, offer it before the brief rather than after it.

For a long-lived or reference-quality brief, create it only in the user’s authorized shared document system or other approved workspace. Use a human-readable title in this pattern:

`YYYY-MM-DD: Specific decision-relevant headline`

Do not use file-like slugs or redundant labels such as “context brief.” Share the document link and a compact statement of the central findings before the full brief only when the delivery format requires it. Do not place sensitive material into a broader-access destination merely because it is convenient.

When editing an existing formatted document, avoid inserting text into the middle of styled headings, list items, or table cells unless the document interface explicitly preserves styles. Insert into a known body-text paragraph or replace a complete, inspected section. After insertion, re-read the affected range in a format that exposes paragraph styles; confirm that body text and bullets use body style and that only intended headings use heading styles. If layout matters, render or inspect the document visually before declaring the edit complete.

## Final audit

Before sending, check:

- Is the effort level proportionate to stakes and the user’s request?
- Was every private source justified by purpose and authorization?
- Did the brief include only necessary personal information?
- Did you inspect recent relevant meeting material when discovered?
- Are important claims linked to direct evidence?
- Did you resolve or clearly flag contradictions?
- Did you identify relevant unavailable sources and real gaps?
- Is the output organized around the user’s decision rather than the tools searched?
- Is the destination appropriate for the sensitivity of the content?

If the answer to any applicable check is no, correct it before delivering the brief.


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
description: Draft or revise email in the user’s own voice by using authorized style evidence, preserving factual accuracy, and producing concise, copy-ready text suited to the recipient and purpose.
---

# Write in my voice

Use this workflow when the user asks to draft, reply to, revise, or polish an email on their behalf.

## Goal

Produce a send-ready email that sounds recognizably like the user while remaining accurate, appropriate for the recipient, and clear about the intended next step. The draft should be concise by default: include what the recipient needs, and remove the rest.

## 1. Establish authorized voice evidence

Before drafting, review the user’s writing guidance in full if they have provided one. If they authorize access to recent sent emails, drafts, or other writing samples, use only the minimum relevant examples needed to understand their voice.

Use private communications only for a legitimate purpose and with clear authorization. Do not surface unrelated personal details, confidential information, or sensitive material from examples. Keep the resulting draft within the user’s appropriate access and sharing boundary.

Build a practical voice profile from the available evidence:

- Usual greeting and sign-off.
- Formality, warmth, directness, and relationship cues.
- Typical sentence and paragraph length.
- Common vocabulary, contractions, punctuation, and formatting.
- Preferred ways to make requests, follow up, decline, correct, apologize, or express uncertainty.
- Phrases, tones, punctuation, or habits to avoid.
- Approved reusable facts, links, boilerplate, and standard responses.

Recent sent messages and explicit user preferences take priority over old examples or generic writing advice. If the evidence conflicts, ask which preference is current when it would affect the draft. Otherwise, favor the most recent consistent pattern.

## 2. Confirm the email brief

Identify the minimum information necessary to write a safe, useful email. Ask focused questions only when a missing detail would materially change the message.

| Needed information | Example question |
|---|---|
| Recipient and relationship | Who is receiving this, and how do you know them? |
| Intended outcome | What should they know, decide, or do after reading it? |
| Required details | What facts, dates, links, files, names, or context must be included? |
| Tone | Should this be routine, warm, firm, formal, or especially careful? |
| Constraints | Is there a deadline, approval requirement, or sensitive issue? |

Do not invent facts, availability, decisions, commitments, prices, links, attachments, opinions, or emotional reactions. Do not imply agreement, authority, or permission that the user has not provided.

## 3. Adapt voice to the situation

Voice is a set of patterns, not a rigid script. Preserve the user’s recognizable style while matching the recipient and stakes.

- **Close colleagues or familiar contacts:** Use the user’s normal level of brevity and familiarity.
- **New, external, senior, or formal contacts:** Keep the voice natural, but add enough context and care that the message stands on its own.
- **Requests:** State the requested action, responsible person if relevant, and timing plainly.
- **Corrections, conflict, or rejection:** Be direct, factual, and calm. Avoid defensive explanations, exaggerated praise, or unnecessary apologies.
- **Sensitive topics:** Use precise language, avoid speculation, and include only necessary details.

Use approved boilerplate, standard facts, or links when they fit the situation. Do not reuse a standard response if it would be inaccurate, misleading, or impersonal in context.

## 4. Draft the smallest complete email

Use this default structure unless the user’s established style calls for something different:

1. Greeting, if the user normally uses one.
2. The purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Closing and sign-off, if appropriate.

Write with concrete nouns, active verbs, short sentences, and short paragraphs. Place decisions and requested actions where they are easy to find. Use bullets only when they make options, responsibilities, or logistics easier to scan.

Remove material that does not help the recipient understand or act, including:

- Process narration or explanations of how the draft was created.
- Generic compliments and repeated thanks.
- Empty opening phrases, unless they are both useful and genuinely typical of the user’s voice.
- Hedging that weakens a clear message.
- Excess context, private details, or internal information that the recipient does not need.

## 5. Audit before presenting

Review the draft line by line:

- Would the user plausibly write these words?
- Do the greeting, sign-off, rhythm, punctuation, and level of formality match the evidence?
- Is the tone appropriate for this recipient and situation?
- Are names, dates, links, attachments, and references accurate?
- Did the draft add any claim, promise, opinion, emotion, or deadline that was not provided?
- Is the recipient’s required action clear?
- Does the message reveal only information appropriate for this recipient?
- Can any sentence be removed without reducing clarity or usefulness?
- Does it avoid the user’s identified style dislikes?

If no voice evidence is available, use a broadly useful default: concise, clear, warm-professional, and direct. State that assumption briefly only if needed, and invite the user to provide a few representative sent emails or explicit preferences for future drafts.

## Output format

Provide the final email as copy-ready text. If clarification is needed, ask only the specific question required to complete the draft safely. Do not add commentary after the final copy unless the user asks for alternatives, explanation, or revisions.


---
name: professional-social-post
description: Draft, revise, and audit professional social posts from notes, drafts, articles, transcripts, research, or a topic. This workflow produces specific, useful, audience-aware posts while protecting accuracy, privacy, and a professional voice.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a rough draft, an article, a transcript, a podcast, research findings, a presentation, or a simple topic.

The goal is not to make an announcement sound enthusiastic. The goal is to make the right reader stop, understand a useful point, and have a reason to care. A strong post has a clear claim, real substance, and a voice that sounds like a person with evidence and judgment.

This is platform-independent. Before drafting, confirm the following when they are not already clear:

- **Platform and format:** text post, caption, document carousel, thread, short-form video caption, or article promotion.
- **Audience:** for example, technical practitioners, founders, policy professionals, researchers, customers, operators, or job candidates.
- **Purpose:** share an insight, explain a concept, announce a change, promote a longer piece, invite informed discussion, or support a campaign.
- **Voice:** first-person, team, or organizational voice; formal or conversational tone; preferred and forbidden words; punctuation preferences; and length.
- **Evidence and permissions:** available sources, approval status, what may be named or quoted, and whether any personal or confidential information must be removed.
- **Link strategy:** whether an external link is included and where the chosen platform should place it.

If the user provides approved posts, a style guide, brand guidance, or audience research, use those materials as the primary source of voice and format decisions. Do not assume a particular person’s voice, organization, publishing tool, or analytics system.

## Privacy, authorization, and source boundaries

When the request involves private messages, internal documents, customer information, employee information, participant stories, or records about identifiable people, first confirm there is a legitimate communications purpose and clear authorization to use the material.

Use only the minimum relevant sources and details. Omit unrelated personal information, sensitive attributes, private contact details, confidential operational information, and material outside the intended access boundary. If a post describes someone’s career change, testimonial, work history, or personal experience, confirm what can be named, quoted, linked, or implied. When permission is unclear, anonymize the example, request approval, or choose another angle.

Do not turn private evidence into public proof without authorization. A compelling post is not worth breaching trust.

## Routing and scope

Identify the genre before drafting. Some formats require a different evidence standard or narrative structure.

- **Career or participant case study:** A person’s starting point, turning point, and later outcome. Use a case-study structure: starting point, intervention or decision, outcome, evidence, and lesson. Get permission for names, quotes, and identifying details.
- **Research or evidence post:** A claim based on data, a model, a report, or analysis. Prioritize methodology, scope, uncertainty, and a defensible interpretation.
- **Product or organizational announcement:** Lead with the concrete change and why it matters to readers. Do not lead with internal excitement.
- **Article, report, or podcast promotion:** Lead with the strongest finding, disagreement, or practical idea from the piece, not with “a new article” or “a new episode.”
- **Carousel or document caption:** Give one or two meaningful findings, then direct readers to the visual material. Do not repeat every slide.
- **Framework or checklist post:** Give readers a usable model, examples, and limits. This format can be especially useful when the content deserves to be saved and revisited.

If the genre or disclosure boundary is unclear, ask one concise routing question before writing.

## Non-negotiable accuracy rules

1. **Do not invent facts.** Never fabricate statistics, names, quotes, outcomes, clients, organizations, titles, dates, research findings, testimonials, or sources.
2. **Separate evidence from interpretation.** State what the source says, then make clear which conclusion, recommendation, or hypothesis follows from it.
3. **Preserve meaningful uncertainty.** If a result has a wide range, weak evidence, important assumptions, or correlation rather than causation, say so plainly.
4. **Use supported specificity.** Exact figures, dates, roles, and outcomes are often stronger than broad claims, but do not convert a rough estimate into falsely precise language.
5. **Request missing support early.** If the post depends on an unsupported claim, ask for a source, narrow the claim, qualify it, or remove it.
6. **Avoid misleading urgency.** Do not exaggerate stakes merely to create attention. A specific risk and a practical response are more credible than broad catastrophe language.
7. **Keep claims defensible.** Assume a knowledgeable reader may ask for the source, scope, assumptions, or counterexamples in the comments.

## Audience and voice

Write for the reader most likely to benefit from or act on the post, not for everyone who might vaguely relate to it. Specificity is a useful filter. It helps the intended reader recognize that the post is for them.

Unless the user specifies another style, use this default voice:

- Direct, clear, and conversational.
- Short sentences with concrete nouns and plain verbs.
- Active voice where it improves clarity.
- One main claim per sentence.
- Sober about problems and practical about responses.
- Confident only where the evidence supports confidence.
- Specific rather than promotional.

Avoid three common failure modes:

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are thrilled to announce an exciting new initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences full of unexplained terms. | State the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Broad catastrophe language without a mechanism or response. | Name the specific risk, evidence, uncertainty, and useful intervention. |

## Core workflow

### 1. Inspect the source before choosing a template

Do not begin by forcing source material into a familiar post format. Read it and locate the strongest thread buried inside it.

Look for:

- An unusual or surprising fact.
- A specific number that creates tension.
- A counterintuitive conclusion that can be defended.
- A concrete before-and-after outcome.
- A meaningful trade-off or deliberate constraint.
- A sharp disagreement between credible views.
- A useful framework, checklist, or model.
- A sentence that changes how the reader sees the problem.

The headline of an article is often not its best social angle. The strongest material may be a detail in the middle, a methodological finding, a concrete example, or an implication the source only briefly mentions.

If several angles could work, do not silently select one. Present two to four numbered options and let the user choose when that choice affects the message.

**Angle-selection prompt:**

> I see several viable post angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding, outcome, or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [story, disagreement, or trade-off]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Choose one primary thread. A social post should not summarize every point in a report or transcript.

### 2. Generate hooks before drafting the body

The first line determines whether readers continue. Generate five to ten hooks before settling on one. When user input would help, show a numbered shortlist of three to five options with a brief note about what each is doing.

A hook should make an honest promise that the body fulfills. It should generally work on its own for a reader who has not seen the source.

Useful hook patterns include:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Named outcome:** “[Person or role] moved from [starting point] to [specific outcome] in [timeframe].” Use only with evidence and approval.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only if the post supports it.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused disagreement:** “Why do two credible groups reach such different conclusions about [specific issue]?”

Use this presentation format:

| Hook | Strategic purpose |
|---|---|
| “[Specific claim or finding].” | Leads with a concrete result and gives readers a reason to continue. |

Apply the **topic-swap test**: if a key noun can be replaced with an unrelated field and the hook still works, it is probably too generic. Add the actual mechanism, result, tension, or audience-specific context.

Avoid:

- “Excited to share,” “thrilled to announce,” or similar announcement framing.
- Throat-clearing such as “In today’s fast-moving environment.”
- Empty cliffhangers that never pay off.
- Several rhetorical questions in a row.
- Broad motivational claims.
- Clickbait such as “You will not believe” or “This changes everything.”

### 3. Choose one structure

Pick the structure that fits the source. Do not combine several structures unless the connection is clear.

1. **Counterintuitive claim → evidence → implication**  
   Best for research, data, and argument posts. Start with the surprise, support it, then explain what readers should reconsider or do.

2. **Changed mind → trigger → updated view → takeaway**  
   Best for thoughtful first-person posts. State the previous view, explain what changed it, and offer the revised conclusion.

3. **Problem → why it matters → practical response**  
   Best for explainers, policy, and operational topics. Keep the problem concrete and make the response proportionate.

4. **Result → how it happened → reusable lesson**  
   Best for credible launches, team outcomes, and approved case studies. The result must be real and specific.

5. **Framework → examples → application**  
   Best for useful, reference-like posts. Name a framework only if the name clarifies the idea rather than disguising ordinary advice.

6. **Specific announcement → reader relevance → next step**  
   Use only when the announcement is genuinely notable. Lead with what happened and its practical significance.

7. **Strategic trade-off → rationale → consequence**  
   Useful when explaining deliberate constraints or anti-goals: what a team, product, or organization has chosen not to optimize for, why, and what follows from that choice.

### 4. Draft: hook, tension, payoff

Use this default body shape:

- **Hook:** the strongest claim, result, or tension.
- **Tension or setup:** why the point matters, what is surprising, or what assumption it challenges.
- **Payoff:** evidence, story, framework, or practical insight. The post should be useful even if the reader never clicks, swipes, or buys.
- **Soft close:** exactly one focused question, one practical takeaway, or one clear pointer to further material.

A useful default is under 300 words, but length should follow substance and platform norms. Each paragraph and line should earn its place. Use one- or two-sentence paragraphs so the post scans well on a phone. Use bullets only when the information is genuinely list-shaped.

For carousel or document captions:

- Establish the central idea in the caption.
- Include one or two of the strongest specifics.
- Explain what the visual material adds.
- Do not produce a slide-by-slide summary.

For linked articles, reports, or podcasts:

- Put the strongest insight in the post itself.
- Treat the linked piece as depth, methodology, sources, or extended analysis.
- Follow the user’s platform strategy for link placement.
- Do not make “read the link” the main value proposition.

## Calls to action and questions

Use one close only. A strong close gives readers a real, bounded way to respond.

Good examples:

- “Which of these constraints matters most in your work?”
- “What evidence would change your view?”
- “The full analysis includes the assumptions and source material.”
- “If you have operated a similar system, where does this model fail?”

Weak examples:

- “Thoughts?”
- “Let me know what you think.”
- Several questions at once.
- Requests to comment, tag, repost, or react merely to boost engagement.

A question should invite knowledge, disagreement, or relevant experience. Do not use engagement bait. Distribution systems change frequently, so treat timing, format, and link-placement advice as a testable hypothesis, not a guarantee.

## Editing pass: remove templated and inflated language

Run a separate editing pass after drafting. Cut language that sounds polished but says little.

Replace or remove:

- Inflated verbs such as “leverage,” “unlock,” “harness,” “navigate,” “cultivate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Hedging frames such as “it is worth noting,” “one might say,” and “arguably,” unless uncertainty is genuinely needed.
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Abstract nouns such as “journey,” “transformation,” and “paradigm” when a concrete event can be named.
- Transition sentences that merely repeat the prior paragraph.
- Dramatic frames such as “The truth is” or “Here is the reality.” State the point directly.
- Decorative punctuation or markup that will not render correctly on the chosen platform.

Honor user punctuation preferences. Otherwise, favor periods, commas, and line breaks over theatrical punctuation. Read the draft aloud. If it sounds like a generic thought-leadership template rather than a person making a specific point, rewrite it.

## Revision protocol

When the user gives feedback, revise the requested line and its nearby logic first. Do not rebuild the entire post unless asked.

- If a hook is not sharp enough, offer several replacement hooks before changing the body.
- If a claim feels overstated, improve its evidence, add an appropriate limit, or soften only that claim.
- If a paragraph feels slow, remove setup before adding explanation.
- If a user prefers an earlier sentence, preserve its strength unless there is a clear reason not to.
- If source material is weak, say so plainly and offer concrete choices: add evidence, narrow the claim, change the angle, or remove it.

Multiple small options are often more useful than a complete redraft, especially for hooks, closers, and uncertain lines.

## Readiness gate and audit

Do not present a draft as final until it passes this checklist:

- Does the first line earn attention when read alone?
- Is the post about one clear point rather than several competing ideas?
- Does it include a concrete detail, outcome, example, number, or mechanism where appropriate?
- Could the main claim be defended if a knowledgeable reader challenged it?
- Does it provide value without requiring a click, swipe, or purchase?
- Is uncertainty stated where it materially affects the conclusion?
- Is the language specific to this topic rather than reusable for any industry?
- Is the close one focused action, question, or pointer?
- Are names, quotes, figures, and claims supported and approved for this audience?
- Have privacy, consent, and access boundaries been respected?
- Does formatting work on the intended platform?
- Is the tone professional, respectful, and non-inflammatory for the intended audience?

If any answer is no, revise before handoff.

## Handoff format

When presenting work to the user, provide only what helps them decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen delivery format or location.
3. Any unsupported claim, missing input, approval need, or line that remains uncertain.
4. Suggested link or first-comment text, if relevant to the selected platform strategy.
5. One concise publishing reminder appropriate to the platform, such as responding promptly and substantively to genuine early comments.

## Common failure patterns

- **Announcement disguised as content:** The post says the organization is pleased but not why readers should care. Lead with the actual change or lesson.
- **Pure teaser:** The post asks readers to click but provides no useful insight. Share the main finding; use the longer piece for depth.
- **Unsupported precision:** The post uses a striking figure without source, scope, or caveat. Verify, qualify, or remove it.
- **Generic inspiration:** The post sounds positive but has no mechanism, example, or decision. Name the concrete action or trade-off.
- **Overpacked summary:** The post covers every section of a source. Choose one thread and reserve the rest for future posts or the original material.
- **Bolted-on promotion:** A product, course, or service appears at the end without a natural connection. Remove the pitch, create a separate promotional post, or make the relationship concrete and immediate.
- **Forced engagement:** The post demands reactions or comments. Ask one real question or end with a useful conclusion.
- **Unapproved personal proof:** A person’s story, quote, or result is used without clear permission. Obtain approval, anonymize it, or choose another form of evidence.

## Continuous improvement after publication

After a post has been accepted or published, use legitimate, authorized feedback to improve the workflow. Do not alter the user’s source materials or publishing systems without permission.

Look for repeatable patterns rather than one-off preferences:

- Which hook types were rejected, and why?
- Which phrases consistently felt too vague, corporate, academic, or promotional?
- Did revisions repeatedly change paragraph order, amount of setup, or the closing style?
- What missing input caused delays?
- Which formats generated substantive replies, saves, qualified inquiries, or other outcomes that matter to the user?

Record only general writing rules that can be safely reused. Do not retain confidential details, private comments, personal data, or sensitive performance information beyond what is necessary and authorized.

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
description: Close one month honestly, then create a small, capacity-checked, explicitly approved plan for the next month using evidence, trade-offs, concrete commitments, and a reusable review record.
---

# Review and plan a month

Use this workflow at a month boundary to review the month ending and create an executable plan for the month ahead. A full session usually takes 45–75 minutes: about half for evidence and review, and about half for planning.

Review and planning belong in one session. The structural cause of a missed commitment, energy drain, or delivery problem should directly shape the structure of the next plan.

## Purpose

This workflow produces:

- An evidence-based account of what happened during the review month.
- A direct verdict on progress toward active long-range goals and any in-scope personal commitment.
- A month-level picture of selected work and life signals, such as focus, sleep, energy, training, or completed work.
- A written **Review** attached to the month ending.
- A written **Plan** for the month beginning, with a memorable theme, no more than three major outcomes, explicit trade-offs, and a pre-mortem.

Only gather, discuss, or save information that supports these outputs.

## When to run it

Run this workflow when the user asks for a monthly review, asks to plan a named month, or asks to close one month and start another.

Default timing:

- On the first three days of a month, review the prior month and plan the current month.
- Otherwise, review the current month to date and plan the next month. Clearly label a partial-month review and state the days remaining.
- If the user asks only for forward planning, review first because the evidence should shape the plan. The user may explicitly choose to skip the review.

State the ranges before proceeding:

> Reviewing **March 2026** (01 Mar–31 Mar). Planning **April 2026**.

Ask whether the user means calendar months or a practical range that includes an overlapping partial week. Record the actual planning range in the finished plan.

## Access, privacy, and evidence boundaries

Use connected calendars, task systems, health trackers, notes, project records, or communications only when there is a legitimate planning purpose and the user has clear authorization to access them. Use the minimum relevant sources and date range.

- Prefer aggregate statistics and concise themes over raw journals, messages, or event descriptions.
- Omit unrelated personal details, sensitive health information, and details about other people that are not needed for planning.
- Keep the review within the user’s normal access boundary. Do not expose private calendar details, communication content, or another person’s information in a stored plan unless it is necessary and appropriate.
- If a source is unavailable, incomplete, or not authorized, say so. Never imply it was checked.
- If delegating a large read to another assistant or capability, give it a narrow, read-only brief: authorized sources, date window, requested aggregates, and a requirement to return no unnecessary raw personal content.

## Operating rules

1. **Read first; discuss second.** Show the evidence picture before asking reflective questions.
2. **Batch independent reads.** Gather independent evidence in one initial pass where possible. Do not interrupt the conversation with repeated small lookups.
3. **Use current commitments.** Assess against the user’s live target, not an old schedule, obsolete project scope, or stale goal record.
4. **Check data quality before a harsh verdict.** Missing syncs, incomplete logs, delayed updates, and inconsistent sources may distort results. Ask the user to confirm surprising findings.
5. **The user chooses.** The assistant calculates, summarizes, identifies gaps, and holds constraints. The user chooses priorities, cuts, and commitments.
6. **One decision at a time.** Do not move to the next planning decision until the current question has a real answer.
7. **Stay at month altitude.** Define outcomes, milestones, capacity, structure, and commitments. Leave detailed week-by-week task blocks to a weekly planning workflow.
8. **No saved plan without explicit approval.** A plan assembled from notes is a draft, not a decision. The user must restate or materially confirm the theme and commitments, then explicitly approve it.
9. **Use explicit dates.** Use **DD MMM** format unless the user prefers another unambiguous convention.
10. **Keep records useful, not exhaustive.** Save decisions, evidence, and constraints rather than a transcript.
11. **Do not lecture.** For training, health, recovery, or personal practice, provide the numbers, direct conclusion, and agreed commitment. Provide specialist advice only when asked and appropriate.

## Step 1: Determine the range and gather evidence

Determine the review month, prior comparison month, and planning month. Then make one initial batch of reads where possible.

Use sources that match the user’s chosen system: a task manager, project tracker, calendar, spreadsheet, notes application, health tracker, training log, or user-supplied facts. If no source is connected, ask for a short factual inventory.

| Evidence area | Gather in the initial pass |
|---|---|
| Previous monthly record | Theme, promised outcomes, commitments, and prior review findings |
| Weekly records | Plans and reviews in the review range; repeated blockers, milestones, and carried work |
| Goals | Active weekly, monthly, quarterly, and annual goals; status, deadlines, and notes |
| Work delivered | Completed tasks, decisions, projects, or deliverables; grouped into useful domains |
| Calendar | Next-month travel, leave, fixed deadlines, recurring commitments, protected personal time, and heavy meeting weeks |
| Daily signals | User-selected ratings, focus time, journals, habits, or mood notes |
| Sleep and recovery | Optional sleep duration, sleep quality, and same-source recovery trends |
| Training or practice | Optional sessions from the review and prior months, plus the live commitment or schedule |

For large sources, return computed statistics and a few representative themes rather than raw entries. Long journals and month-long event lists can crowd out the actual review. Use filtered queries, aggregation, summaries, or a delegated helper when available.

For a next-month calendar sweep, return only:

- Fixed multi-day commitments such as travel, leave, or conferences.
- Approximate meeting load by week.
- Important recurring series.
- Protected personal or social commitments relevant to capacity.
- Planning anomalies, such as meetings inside unavailable periods or likely time-zone mistakes.

Before detailed planning, re-read any weekly plans that overlap the beginning of the planning range. A weekly plan may already define that period in more detail. Reference and reconcile it with monthly outcomes; do not duplicate or overwrite it.

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

Flag meaningful patterns, such as low average sleep, repeated short nights, several consecutive low-rating days, an extended low-focus streak, or an apparent mismatch between positive ratings and written notes describing exhaustion or stress. Numerical averages are not complete truth. Raise such a mismatch directly and briefly.

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

At the end of every run, capture one precise improvement to the reusable workflow, its templates, or its data mapping. Store it in a user-approved workflow document or improvement log. If no suitable location exists, present the proposed edit as a short durable rule the user can save where they prefer.

Look for a read that was noisy, a wrong data assumption, a misleading metric, a question the user corrected, or a repeatable pattern future sessions should know. Prefer one specific edit over a vague reminder.

## Audit checks

Before finishing, verify:

- Review and planning ranges are explicit.
- Evidence was shown before reflective prompts.
- Only authorized, relevant sources and details were used.
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
- Treating incomplete tracking as complete reality.
- Confusing a list of events with a plan.
- Overloading capacity and refusing to cut scope.
- Letting the assistant choose priorities.
- Saving an unapproved draft.
- Duplicating or conflicting with weekly plans.
- Treating wellbeing averages as more truthful than repeated written evidence.
- Applying generic productivity rituals instead of fixing the actual drain.
- Overwriting an existing record without resolving the difference.
- Treating a voice note, brainstorm, or imported task list as a confirmed commitment.
- Saving unnecessary personal details or using sources outside the agreed access boundary.


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
description: Review authorized meeting records to identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that need human judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date range, or for a manually supplied group of meetings.

The goal is not to turn every discussion into work. Each meeting should produce zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose and operating rules

Before each run, confirm there is a legitimate work purpose and that you are authorized to access the selected meeting records and create or update tasks. Use only the minimum relevant records and details. Do not copy unrelated personal, confidential, or sensitive information into tasks, summaries, or questions. Keep output within the access boundary of the chosen task system and its intended audience.

Use these outcome rules:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text**: strongest evidence of who agreed to do what and when.
2. **Human-written notes**: useful supporting evidence, especially explicit action sections.
3. **Automated summary**: useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda**: describes intended discussion, not a commitment.

Automated summaries often misattribute work, particularly in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels something as an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, a statement of interest, or an open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply delegation boundaries supplied by the user or organization. Attending a meeting does not make the user accountable for every topic discussed.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is supplied, use this default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect the title, date and time, record link or identifier, attendees where available, and the transcript, notes, summary, and relevant linked context.

Report a compact count before processing. Do not infer actions from a meeting title alone.

## 2. Fetch and inspect complete records

Fetch complete meeting records in parallel where the selected meeting system supports batching. Do not search for existing tasks yet: first identify the people, topics, and candidate outcomes that make duplicate detection accurate.

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

- Relationship context and why the meeting occurred.
- Candidate actions owned by the user.
- Work completed during the meeting.
- Work delegated to another named owner.
- Explicit future commitments and timing.
- Enough neutral context for a task to remain understandable weeks later.
- The source record and relevant links.

Create no task when work was completed live, another person owns it, the meeting was purely informational and any needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

## 4. Decide the task shape

Combine actions into one task when they have the same counterparty, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect months later.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

This is a readiness gate. Do not proceed to task creation until every proposed task has a clear owner, unfinished outcome, sensible shape, source evidence, and enough context to stand alone.

## 5. Write the task

Use the user’s chosen task system and its field names. At minimum, capture:

- **Title:** short, verb-led, and specific, such as “Follow up with prospective partner about pilot scope.”
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user’s scale; default to normal important work and reserve the highest level for a real deadline, material risk, or waiting counterparty.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and permitted links.

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
dates, why this matters, the commitment, and only necessary sensitive context.]

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

Wait for answers before creating uncertain tasks. After answers arrive, create or update the remaining tasks and rerun any needed duplicate check if the answer changed the task outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, capture lessons that genuinely improve future runs. Keep this separate from the meeting task itself.

- Add a short, generalized note to a reusable meeting-archetype reference when a recurring pattern affects triage, such as a common attribution error, reliable sign of in-meeting completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new delegation boundary in a maintained responsibility reference when it applies beyond one meeting and the user authorizes that record.

Do not turn one-off facts about people into permanent rules. Small additions to an examples or patterns reference can be made directly when authorized. Ask for confirmation before structural workflow changes, such as adding or removing steps or changing the evidence order. Briefly report reusable guidance that was added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links to its authorized source record where appropriate.
- Message drafts are ready to send and follow the user’s preferences.
- Task notes exclude unrelated or unnecessary sensitive details.
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
description: Prepare, conduct, and document a structured hiring reference call that gathers concrete, role-relevant evidence while respecting privacy, consent, and access boundaries. Use it to inform—not replace—a fair, job-related hiring assessment.
---

# Run a reference call

Use this workflow when an authorized hiring team needs to speak with a candidate’s professional reference. The purpose is to gather specific evidence about role-relevant work: not vague praise, personal gossip, or information unrelated to the hiring decision.

## Privacy, authorization, and access boundary

Before collecting information or contacting a referee, confirm all of the following:

- The candidate has provided the referee’s details or otherwise clearly authorized the reference check, unless a lawful and appropriate alternative process applies.
- The referee understands the purpose of the conversation and is willing to discuss their professional experience working with the candidate.
- You have a legitimate hiring purpose and permission to access each source used for preparation.
- You will use only the minimum relevant information from hiring records, scheduling records, communications, and professional sources.
- The resulting brief and notes will be visible only to people who need them for the hiring decision.

Do not seek, record, or circulate unrelated personal details. Avoid protected characteristics, health, family circumstances, immigration status, age, political views, or other sensitive information that is not necessary for a lawful, role-relevant decision. If sensitive or unrelated information is volunteered, redirect the conversation and omit it from the record unless there is a clear legal or safeguarding reason to retain it.

## Inputs and readiness gate

Collect or confirm:

- Candidate name.
- Referee name and authorized contact details.
- Role, key outcomes, and capabilities the role requires.
- Hiring stage and the decision this call will inform.
- Call date, time, timezone, and access details, if scheduled.
- Referee relationship to the candidate: for example, manager, colleague, client, collaborator, or instructor.
- Existing interview, work-sample, or assessment evidence and open questions.
- Other planned or completed references, if known.

Do not treat a reference as strong evidence until you know what the referee directly observed, how recently they observed it, and how closely they worked with the candidate. If this is unclear, resolve it before the call or mark it as a prominent limitation.

## 1. Confirm the call and its logistics

Check the approved scheduling system or correspondence for the referee’s name or contact details. Record:

- Meeting title, date, time, timezone, attendees, and access link.
- Whether the referee accepted or supplied relevant scheduling context.
- How the referee was introduced and whether their relationship was confirmed.

If no event exists, prepare the brief with the available information and label scheduling as outstanding. Never invent logistics or imply that a call is confirmed when it is not.

## 2. Gather relevant context

Review only authorized and relevant sources, such as the candidate’s application, role scorecard, interview notes, work-sample results, reference-list message, prior reference records, and correspondence directly relevant to the reference relationship. Where permitted, use professional profiles or prior organization records to verify the referee’s current role and relevant background.

Answer these questions concisely:

- What outcomes must the successful person deliver in this role?
- What decision follows the call?
- How, where, and for how long did the referee work with the candidate?
- What work did the referee directly observe?
- Which candidate records will be useful during the call?
- What other references are planned or completed?
- What themes from earlier evidence need independent confirmation, clarification, or challenge?

Read enough relevant correspondence to understand the relationship and avoid asking for facts already documented. Do not collect personal background simply because it is available.

## 3. Create a single call brief and record

Create the call page in the organization’s chosen, access-controlled meeting or hiring-record system. Keep logistics, briefing notes, live notes, and post-call assessment together where practical. Include only necessary participants.

Use this template:

```markdown
# [Date] [Referee name] — [Candidate name] reference

## Context
- **Referee:** [role, organization, brief relevant background, professional link if authorized].
- **Relationship:** [how they worked together, duration, and closeness of observation].
- **Hiring context:** [role, stage, next decision, and key role outcomes].
- **Candidate records:** [application or internal profile; relevant portfolio or work samples].
- **Other references:** [known referees or “not confirmed”].
- **Logistics:** [time, timezone, meeting link, or scheduling status].

## Opening
> Hi [Referee], thank you for making time. I’m [name and role] at [organization]. [Candidate] is being considered for our [role]. We are checking references to understand their work in comparable settings and what support would help them succeed. We will use what you share only within the authorized hiring process. Is now still a good time, and are you comfortable discussing your direct experience working with them?

## Briefing notes
- [Direct question to test, based on a role requirement or prior evidence.]
- [What this referee is uniquely positioned to observe.]
- [Earlier-reference theme to independently validate, including its source and limits.]
- [Open hiring question that needs a concrete example.]

## Questions
- [Question and follow-up prompts.]

## Notes and evidence
- **Direct observations:**
- **Examples and outcomes:**
- **Development areas / support needed:**
- **Limits of this reference:**
- **Caller inference:**
- **Follow-up actions:**
```

Write briefing notes as actions. For example: “An earlier reference reported strong project starts but inconsistent finishing. Ask for one completed project and one delayed project, including the candidate’s ownership, constraints, and result.” If this is the first reference, state which themes should be collected consistently in later calls.

## 4. Tailor role-specific probes

Choose three to five probes that test capabilities required by the role. The test is whether the conversation produces diagnostic evidence about relevant performance, not whether the referee likes the candidate.

| Role context | Example probes |
|---|---|
| Operations or program delivery | Handling ambiguous requirements; building repeatable systems; prioritizing competing work; communicating with varied stakeholders; identifying important work proactively. |
| Community or partnership work | Building trust; maintaining engagement; addressing conflict constructively; setting expectations; balancing relationships with operational follow-through. |
| Senior operations leadership | Scaling processes; making tradeoffs under pressure; managing budgets or external providers where relevant; improving failing systems; balancing speed with appropriate controls. |
| Technical or specialist work | Quality of judgment; independent contribution; collaboration across disciplines; response to feedback; reliability in delivering agreed work. |

## 5. Conduct the conversation

Start by confirming the working relationship and the referee’s direct knowledge. Ask open questions before introducing specific concerns.

Use this core question set:

- How did you work together? What were each of your roles, and how closely did you work day to day?
- What did the candidate personally own or deliver? What was the result?
- What did strong performance look like in practice? Please describe a specific example.
- Where did they need the most support, coaching, or structure?
- What is their most distinctive strength in this kind of work?
- How did they handle ambiguity, setbacks, competing priorities, or difficult feedback?
- If this role did not work out after several months, what would be the most likely role-relevant reason?
- If they were doing well after several months, what development area would be most useful to prioritize?
- What management approach or working environment helps them contribute at their best?
- Compared with others you have worked with in similar contexts, how would you describe their performance, and what evidence supports that view?
- What should I have asked that I did not?

When an answer is broad, ask: “What did that look like?” “What did they specifically do?” “What was the outcome?” and “Was that your direct observation?” Separate firsthand evidence from hearsay.

Test open concerns neutrally. Do not reveal confidential interview judgments, pressure a referee to agree, or frame a question to invite confirmation. For example: “This role involves shifting priorities. Can you describe a time they worked in that kind of environment?”

## 6. Record signal and audit the result

Complete notes immediately after the call. Separate:

- **Direct observations:** what the referee personally saw.
- **Interpretations:** how the referee explains those observations.
- **Caller inference:** what the evidence may mean for the role.
- **Confidence and limits:** how direct, recent, and role-relevant the evidence was.
- **Follow-up:** contradictions to investigate or capabilities to test through a role-relevant assessment.

Before sharing, audit the record:

- Is every material claim tied to an example, source, or stated limitation?
- Did the call focus on job-relevant capabilities and role alignment?
- Are earlier-reference themes independently evidenced rather than treated as fact?
- Have unrelated and sensitive personal details been omitted?
- Are opinions clearly distinct from observations?
- Is the record restricted to authorized decision-makers?

Do not let one positive or negative reference determine the outcome alone. Compare references with structured interviews, work samples, and other role-relevant assessment evidence. When accounts conflict, document the conflict, seek concrete examples or another relevant source, and do not treat confidence, seniority, or personal familiarity as proof.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context, verifying rendered state, and separating preparation from irreversible commitment.
---

# Use a browser safely

Use this workflow for tasks that require real interaction with a website: completing a rendered form, changing a dashboard setting, collecting data from a dynamic page, testing a user flow, or working in an authenticated account. Use it when ordinary page retrieval, a supported API, or a static-page request cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not perform a consequential final action until the page state, target, and authorization are clear.

A browser automation command succeeding does **not** prove that a website accepted the change. Modern applications can maintain internal state separately from the visible DOM, commit values only after focus leaves a field, replace controls during a re-render, or display a cosmetic error after an action actually succeeded.

## 1. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can perform the requested task. It is usually more reliable than reproducing browser behavior.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, UI testing, and forms that do not require the user's established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing session, single sign-on state, account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for a direct route. Check official documentation, ordinary form actions, page source, and visible network activity for supported endpoints. A form may submit structured data to an authorized service that is safer to use directly.

Do not use undocumented interfaces to bypass access controls, consent boundaries, contractual restrictions, or other protections. Do not use an authenticated visible session merely because it is convenient: it can interrupt the user's work and creates greater privacy and account risk.

If a site blocks automated browsing, do not attempt to evade its protections for casual research or collection. A visible authenticated session may be appropriate only when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and the existing session is necessary. Do not weaken browser security, access controls, warnings, or anti-abuse protections.

## 2. Protect account identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, first establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into notes, screenshots, logs, or reports. Keep results within the requester's appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated context, identify the correct account, organization, environment, and browser profile. Never infer identity from a generic browser-window name, an old tab title, a remembered default, or a connection label.

Use these rules:

- Announce when taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Classify the intended context explicitly: for example, personal, work, testing, staging, or production.
- Select the browser profile or connection that corresponds to that context rather than relying on a generic browser selector.
- Confirm the signed-in account using a reliable account indicator before opening or changing the real target.
- If the required account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not reveal credentials, session tokens, recovery information, private account data, or security settings in output or logs.
- Do not disable multi-factor authentication, browser warnings, security controls, or access restrictions to make automation easier.

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

## 5. Use the correct interaction for each control

Different controls need different interactions. A generic “set value” operation is not reliable for all of them.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use the normal text-input mechanism. | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away. | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus it, select existing content, enter text through keyboard-style events, then blur. | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle. | Selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed. | A click can toggle an already-correct value. |
| Date/time picker | Choose date and time, then verify the rendered summary. | Popovers can reinterpret typing or clear related fields. |
| File upload | Confirm file, destination, and privacy implications first. | Uploading may begin immediately and can be difficult to undo. |

For framework-driven editors, simulate normal user interaction rather than writing directly to low-level page properties. A robust sequence is: focus the actual editable element, select existing text, delete it, enter the new text with keyboard-style events, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible rich-text editor with a hidden input. Editing the hidden input may appear successful in a DOM dump while server-side validation treats the visible editor as empty. Target the control that the user interacts with and that the application actually reads. If an accessibility locator points to an empty wrapper, inspect the underlying editable element and follow its label relationship.

If changing a dropdown, checkbox, tab, or date can refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterward and confirm earlier entries remain present.

## 6. Verify after every meaningful edit

After each field is filled or setting is changed, read its value back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare lengths, required state, or a minimal redacted summary rather than exposing the full value unnecessarily.

Check for these common mismatches:

- The automation layer reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displayed text but did not retain it internally.
- A later interaction erased an earlier field after a re-render.
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
| Automation reports success but the field is blank | The application ignored a direct value change. | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after editing a later one | A component re-render reset uncommitted state. | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used. | Find a multiline or editor control, or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node. | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited. | Use the visible interactive control that the application actually reads. |
| Automation becomes unstable on a complex page | The chosen automation layer is unsuitable. | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and normal browsers show different behavior | The site varies behavior by browser context. | Prefer an authorized direct interface; if needed for an explicit task, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior. | Close it through a neutral page action and re-verify affected fields. |
| A visible error may be cosmetic | The task may already have completed. | Inspect resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and handing off a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, improve an existing one, evaluate whether it helps, or refine when it activates. A skill is a focused set of instructions, plus optional resources, that helps an AI perform a recurring job reliably.

The core loop is:

1. Understand the job, outcome, and boundaries.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements where useful.
5. Improve the skill from evidence.
6. Repeat until the skill is useful, reliable, and not tailored only to the tests.
7. Optionally improve the description that controls activation.

Do not force every project through every stage. A user may want a quick draft, an informal collaborative review, or a rigorous comparison. Identify where they are in the loop and take the next useful step.

## Communicate clearly and safely

Match the user’s technical vocabulary and experience. Use plain English by default. Briefly explain terms such as *benchmark*, *assertion*, or *structured data* when they matter and the user has not shown familiarity with them.

Explain why important questions matter. For example: “What should a successful result look like—an answer, a report, a file, or an external action? That determines how we design and test the skill.”

Keep the user involved in decisions that affect scope, permissions, quality standards, or tradeoffs:

- Confirm the intended job before writing extensive instructions.
- Ask before choosing restrictive rules, required capabilities, or approval policies.
- Share proposed test cases before treating them as the evaluation set.
- Let human review lead for subjective qualities such as tone, visual design, creative value, and strategic judgment.
- Be clear about what was tested, what was not tested, and what cannot be verified.

If the work involves private communications, records, or information about people, require a legitimate purpose and clear authorization. Use only the minimum relevant sources and details. Keep outputs within the user’s proper access boundary, and omit unrelated or sensitive personal information.

## 1. Identify the starting point

First determine which situation applies.

### New skill

The user has an idea for recurring work. Start with discovery, then create a first draft.

### Existing skill

The user has a draft or installed skill and wants it edited, simplified, tested, or improved. Read the existing instructions first. Preserve its established name and identity unless the user asks to change them.

### Workflow demonstrated in the conversation

If the user says “turn what we just did into a skill,” extract what is already known before asking questions:

- Inputs, files, and approved sources used.
- The sequence of decisions and actions.
- Tools or capabilities that were needed.
- Corrections, preferences, and acceptance criteria stated by the user.
- Output format and conditions that changed the approach.

Summarize the inferred workflow, distinguish facts from assumptions, and ask the user to confirm important gaps. Do not turn a one-time workaround into a general rule without confirmation.

### Evaluation or activation request

If the user wants to know whether a skill works, or whether it activates at the right time, begin with test design and evidence gathering. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough detail to define a coherent job. Adapt these questions rather than asking all of them mechanically.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What kinds of requests, wording, or situations should use it?
3. **Inputs:** What information, examples, files, capabilities, and approved systems may it use?
4. **Outputs:** What should it produce, change, or recommend? Is a format required?
5. **Success:** How will the user know the result is correct, useful, or complete?
6. **Boundaries:** What should the skill not do? When should it ask, pause for approval, decline, or hand work back?
7. **Variation:** Which common cases or meaningful exceptions change the approach?
8. **Dependencies:** Does it need templates, references, reusable helpers, or user-provided access?
9. **Testing:** Should it be tested with realistic requests before release?

Recommend testing when outputs are objectively checkable, the work is consequential, or the skill will be used repeatedly. For highly subjective work, a small set of human-reviewed examples is often more valuable than artificial metrics.

Useful choices include:

- “When information is missing, should the skill make a clearly labeled best effort or stop and ask?”
- “Should the default output be concise, detailed, or selected by the user?”
- “May it use any available source, or only sources the user approves?”
- “Which external, irreversible, or high-impact actions require confirmation?”

### Research before drafting

When relevant documentation, comparable skills, approved references, or domain standards are available, consult them before drafting. Research should reduce burden on the user, not replace their authority over requirements.

Use it to identify conventions, environmental constraints, reusable patterns, and safety or approval requirements. If sources conflict or uncertainty remains, state that rather than guessing.

## 3. Choose a maintainable structure

Keep a skill focused enough that users and AI can predict what it does. One skill may support closely related variants, but separate unrelated jobs when they have different audiences, permissions, trusted sources, or completion criteria.

A typical package can contain:

```text
skill-name/
├── SKILL.md          # Core instructions
├── scripts/          # Optional deterministic helpers
├── references/       # Optional detailed guidance
├── assets/           # Optional templates or output resources
└── evals/            # Optional test and grading material
```

Use progressive disclosure:

1. **Metadata:** A short name and activation description.
2. **Core instructions:** The workflow needed in ordinary use.
3. **Supporting resources:** Detailed references, templates, and helpers consulted only when relevant.

Keep the core instructions readable. If they become unwieldy, move variant-specific or detailed material into clearly named references and state exactly when to read them. Large references should include clear navigation.

Add a reusable helper only when repeated work demonstrates its value. Good candidates are deterministic procedures such as conversion, validation, or structured-data checks. Document its purpose, inputs, outputs, limitations, and authorization boundary. Do not automate merely because automation is possible.

## 4. Write the skill

Write in clear, imperative language. Explain the reason behind important instructions, especially when they prevent a predictable quality, safety, privacy, or usability failure. Prefer a capable AI’s informed judgment over long lists of unexplained prohibitions.

Include the following sections where applicable.

### Purpose and scope

State the job, expected result, intended user, and boundary. Make clear whether the skill creates an answer, produces a file, performs an action, or guides a process.

### Inputs and prerequisites

List required information, allowed sources, needed capabilities, and optional inputs. State what happens when a required input is absent.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or provide a draft clearly marked as incomplete.
```

For personal or private data, require a legitimate purpose, clear authorization, and minimum necessary use. Do not direct the AI to gather unrelated records, infer sensitive information, or disclose details that are not needed for the task.

### Workflow

Give the normal sequence and key decisions rather than attempting to list every edge case.

A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Ask focused questions only when the answer materially changes the work.
3. Gather evidence from approved, relevant sources.
4. Perform the task using an appropriate method.
5. Check the result against requested format and success criteria.
6. Present the result with relevant assumptions and unresolved limitations.

Use conditional instructions when they clarify real choices:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested action could overwrite important work or affect an external system, explain the impact and request confirmation first.
```

### Output format

When consistency matters, define a template:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing input]
```

Avoid rigid formatting when usefulness depends on context. In those cases, specify required content and quality goals, with a small example only when it teaches a distinct pattern.

### Quality, safety, and failure behavior

State the checks needed before completion. Depending on the work, these may include required fields, calculation validation, source support, preservation of original data, clear separation of facts from assumptions, and uncertainty flags.

The skill must behave as users would reasonably expect from its description. Do not hide actions, bypass authorization, enable unauthorized access, extract confidential material without authority, damage systems, or misrepresent results.

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or source:** Explain what cannot be verified and offer a safe alternative if available.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially change the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, report the issue, or seek guidance.
- **External or high-impact action:** Pause for confirmation before proceeding.

## 5. Write an effective activation description

The description is a routing instruction. It should say both what the skill does and when to use it. Cover realistic wording, including requests that imply the task without naming it.

A good description includes:

- The outcome or task.
- Common contexts that signal relevance.
- Important scope limits that prevent harmful or costly false activation.

Example:

```text
Create clear project status reports from approved updates and source material. Use for progress summaries, milestone reviews, leadership updates, risks, blockers, and next steps, including requests that imply a status report without using that phrase.
```

Do not put the whole procedure in the description. Avoid vague labels and descriptions so broad that they capture nearby work better handled by another skill.

## 6. Audit the draft before testing

Read the draft as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description say when it should activate?
- Are inputs, outputs, trusted sources, permissions, and dependencies clear?
- Does the workflow handle missing, conflicting, and sensitive information appropriately?
- Are important checks explained?
- Are there duplicate rules, brittle wording, or undeclared assumptions about tools or local practices?
- Does it leave enough judgment for normal variation?

Prefer a lean, understandable skill over a long prompt with rules that do not affect behavior. Strong absolute language is usually a warning sign unless it protects a genuine safety, authorization, or integrity boundary.

## 7. Design realistic tests

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user before relying on them. Each test should record a descriptive name, prompt, supplied files or context, expected outcome, and objective checks when suitable.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and flag anything that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful situations: a normal request, incomplete or ambiguous input, a format-sensitive task, and a case involving approval, privacy, or safe refusal when relevant. Vary phrasing and detail. Test general categories of difficulty rather than retaining private incidents.

## 8. Run comparisons and preserve evidence

When independent execution is available, compare the skill with a meaningful baseline:

- For a new skill, run each test with the skill and without it.
- For an existing skill, preserve an unchanged snapshot before editing and compare the revision with the earlier version.

Run the compared conditions under similar circumstances. If parallel work is available, start the skill and baseline runs for all tests together. Preserve each prompt, relevant inputs, output, and available metadata such as elapsed time or resource use. Record timing as it is reported because some systems do not retain it.

Use an iteration structure such as:

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

If independent comparison is unavailable, perform a transparent sanity check: apply the skill to each test, save or present results, and ask the user to review. Do not describe this as a rigorous baseline comparison.

## 9. Grade what can be measured

While tests run, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful: required sections exist, a file opens with required fields, calculations match approved data within a defined tolerance, mandatory missing input is identified, or required sources are referenced.

Record a statement, result, and evidence for each check:

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

Use programmatic checks when practical because they are repeatable and reusable. Do not force numerical checks onto writing quality, design, usefulness, or judgment; those require human review.

## 10. Review, analyze, and improve

Present outputs and measurements in a form the user can inspect before making major revisions. Use an available review interface; otherwise provide accessible files or a clear conversational comparison. For each test, show the prompt, relevant context, compared outputs, grades with evidence, and available timing or resource data.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add effort or detail without value?
- Would this work with different wording or data?

Aggregate results where possible, but look beyond pass rates. Watch for checks that pass in every condition, unstable results, quality-versus-cost tradeoffs, repeated failures with one root cause, unproductive execution work, and repeated reconstruction of the same helper procedure.

Revise the smallest part of the skill likely to address the underlying cause. Generalize from feedback instead of adding rules that only solve one test example. Preserve useful behavior, remove instructions that do not help, and add resources only when repeated evidence justifies them.

Rerun the relevant test set in a new iteration and compare it with the same baseline policy. Stop when the user is satisfied, meaningful tests are consistently successful, further revisions do not help, or remaining issues require unavailable information or a product decision.

## 11. Optional blind comparison and activation testing

For an important choice between two versions, use blind comparison. Give an independent reviewer two unlabeled outputs and a shared rubric based on correctness, completeness, clarity, constraint adherence, privacy and safety handling, and practical usefulness. Reveal which version produced each output only after the judgment.

After the skill itself is stable, test its activation description. Create a balanced set of realistic, substantive requests that should activate the skill and difficult near-misses that should not. Positive examples should vary in wording and context; negative examples should be adjacent tasks, not obviously irrelevant ones.

Review the set with the user. If repeated testing is available, separate examples used to improve the description from held-out examples used to choose it. Select the description by held-out performance to reduce overfitting. Remember that simple one-step requests may not consult a specialized skill even when its description matches; test requests where the skill would clearly add value.

## 12. Package and hand off

Package only the core instructions and resources needed for normal use. Before delivery, verify that:

- The name is stable and appropriate.
- The activation description is accurate.
- The skill has no private conventions, undeclared capabilities, confidential data, credentials, identifiers, or sensitive examples.
- References and helpers are present, clearly named, and documented.
- The user can install, access, or adapt it in their chosen environment.
- Retained test materials are safe and useful.

Provide a short handoff note describing the skill’s purpose, required capabilities, known limitations, authorization expectations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an honest activation description, instructions that handle normal variation, explicit behavior for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring work.


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

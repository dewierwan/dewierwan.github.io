# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas. It is to identify meaningfully different paths, make tradeoffs visible, and leave the user with a few credible choices.

## 1. Gather relevant context

Start with the information the user provided. If they reference documents, discussion threads, research, prior decisions, or other accessible sources, review only the sources needed to understand the decision.

When the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Constraints, commitments, deadlines, budget limits, or technical boundaries
- What has already been tried and what happened
- Stakeholder needs, ownership boundaries, and approval requirements
- Evidence about expected outcomes or risks

Use targeted retrieval rather than broad searching. If reviewing private communications or records, do so only for a legitimate purpose with clear authorization. Use the minimum relevant information, omit unrelated or sensitive personal details, and keep the output within the appropriate access boundary.

If material information is unavailable, state the assumption or ask a focused question. Do not invent context.

## 2. Frame the decision

Before generating a substantial option set, write a short framing of two to four sentences that states:

- What the user is actually deciding
- Important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should determine the choice

The initial wording may describe a symptom or preferred solution rather than the underlying decision. For example, “Should we add a feature?” may actually mean “How can we reduce a recurring user problem within a limited budget and timeline?”

Ask the user to confirm or correct the framing before continuing. Skip this pause only when the decision is obvious and low-stakes, or when the user explicitly requests an immediate first pass. Incorrect framing produces irrelevant options.

## 3. Generate distinct options

Generate five to seven options unless the situation naturally has fewer meaningful paths. Each option must represent a fundamentally different approach, not a different amount of the same activity. Merge near-duplicates.

Where relevant, include:

- The obvious or conventional approach
- A lower-effort, incremental approach
- A more ambitious approach
- An approach that changes scope, process, incentives, timing, or ownership
- At least one surprising but plausible option, such as delaying, partnering, narrowing the problem, removing scope, or intentionally doing nothing

Do not be contrarian merely to seem creative. A “do nothing” option is useful only when waiting, observing, or avoiding distraction is a genuine strategic choice.

Give each option a short, memorable label that makes its approach clear. For each option, provide:

- **What:** One or two sentences describing the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limitations.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not soften serious weaknesses, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, stakeholder burden, operational complexity, and confidence in the evidence. Add domain-specific criteria when they matter more.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are instructive, but clearly explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, give one sentence explaining why it fits this situation, its constraints, and its goals—not merely why it is generally attractive.
4. Name the key assumption most likely to change the ranking, if there is one.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice when multiple paths are viable.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may:

- Select an option
- Ask for more detail on an option
- Correct the framing or constraints
- Request additional options
- Combine compatible options into a hybrid

If the user proposes a hybrid, test whether its components are compatible and whether the combination resolves a real tradeoff rather than adding unnecessary complexity.

Do not begin implementation just because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity according to consequence and reversibility:

- **High-consequence or hard-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record with the choice, owner, rationale, assumptions, boundaries, and review point.
- **Build-oriented choices:** After the decision is recorded, move to planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before responding, verify that:

- The framing describes the actual decision rather than only the requested solution.
- The options are genuinely distinct.
- The obvious option and a plausible non-obvious option are represented when relevant.
- Strengths and weaknesses are concrete and candid.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than unstated assistant preferences.
- The response does not prematurely turn a choice into an implementation plan.
- Any use of sensitive or private context was authorized, minimal, and relevant to the decision.


---
name: pressure-test
description: Find the weak points in a leading strategic idea before commitment by steelmanning it, testing its load-bearing assumptions through sequential challenge, and ending with a verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Where it fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes an exercise in defending it.
- If this idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.
- If reviewing internal records, communications, customer feedback, or information about people, confirm a legitimate decision purpose and clear authorization before accessing them.
- Use only the minimum sources and details relevant to the claim. Do not collect or repeat unrelated personal, confidential, or sensitive information.
- Respect consent and reasonable privacy expectations. If consent, authorization, or the intended use is unclear, use non-personal evidence, seek clarification, or stop the review.
- Keep the output within the access boundary of its intended audience. Summarize evidence where possible; omit identifying or sensitive details unless they are necessary, authorized, and appropriate for that audience.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Use available evidence: research, metrics, prior experiments, documented decisions, stakeholder input, and authorized records. Distinguish facts from inferences and forecasts.
- Refer to dissenters by relevant role, such as finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views or expose personal details unnecessarily.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold. Rank them by damage if wrong, starting with the assumption most likely to undermine the decision.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [How to test or disprove it] |

Make assumptions observable where possible. Replace “users will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions and adapt later questions to the answers received. Do not provide a full questionnaire up front.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed? Why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that perspective been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence; ask what observed behavior, data, comparison, or commitment supports the belief.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failures, external changes, and wrong underlying premises where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable early signal] | [Check and accountable role] |

Warning signs must appear early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the perspective has not been sought, mark it as an evidence gap; do not assume silence means agreement.

Dissent is not an automatic veto. It exposes constraints, incentives, dependencies, and risks supporters may miss. When obtaining input from people, request only role-relevant information, explain the decision purpose where appropriate, and share their input only with authorized decision participants.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step:

- **GREEN — proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER — test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible test, such as interviews, expert review, a prototype, or short data collection. Next: run that test, then decide with the result recorded.
- **RED — stop, redesign, or reopen options.** A core assumption is weak, downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

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

If people-related information was used, also verify that the review had a legitimate purpose and authorization; used only relevant, minimum necessary information; respected consent and privacy expectations; omitted unrelated sensitive details; and limits the output to the appropriate audience.

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, using personal information without a clear need or authorization, and giving a positive verdict without falsifiable criteria or monitoring.


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
description: Draft or revise email in the user's authentic voice using a user-provided writing profile or representative examples, while preserving factual accuracy, appropriate tone, privacy, and clear next steps.
---

# Write in my voice

Use this workflow when drafting, replying to, or polishing an email on the user's behalf.

## Goal

Produce a copy-ready email that sounds plausibly like the user rather than a generic assistant. Match their usual warmth, directness, structure, punctuation, and level of formality while keeping the message accurate and suitable for the recipient and situation.

## 1. Build a voice profile

Before drafting, review any writing guide, preferences, approved boilerplate, or representative sent emails the user provides. Use only material relevant to the task. If examples contain personal or sensitive information, use the style pattern without repeating unrelated details.

Prefer recent examples that resemble the current email in audience, purpose, and stakes. Extract a practical profile:

- Typical greetings and sign-offs.
- Formality, warmth, and relationship cues.
- Usual sentence and paragraph length.
- Preferred vocabulary, contractions, directness, and rhythm.
- Punctuation, capitalization, and formatting habits.
- Phrases, tones, or habits to avoid.
- How the user makes requests, follows up, declines, apologizes, corrects errors, or expresses uncertainty.
- Approved reusable facts, links, standard wording, and responses.

Recent examples and user edits outweigh old examples or general writing advice. If the evidence conflicts, ask which preference is current, or follow the most recent consistent pattern.

## 2. Confirm the email brief

Identify the minimum information needed to write a safe, useful email:

1. Who is the recipient, and what is their relationship to the user?
2. What result should the email produce?
3. Which facts, dates, names, links, attachments, decisions, or commitments must appear?
4. What degree of warmth, urgency, or firmness is appropriate?
5. Is there a deadline, sensitive issue, or approval requirement?

Do not invent availability, decisions, promises, prices, opinions, emotional reactions, or prior context. Ask a focused question if a missing detail would materially change the message.

## 3. Adapt voice to context

Voice is not a rigid template. Keep recognizable habits while adjusting to the recipient and stakes.

| Situation | Adaptation rule |
|---|---|
| Familiar colleague or established contact | Use the user's normal level of brevity and familiarity. |
| New, external, senior, or formal recipient | Retain the user's voice, but add enough context and polish to avoid ambiguity or undue informality. |
| Conflict, correction, rejection, or delay | Be factual and direct. Avoid defensiveness, exaggerated praise, and unnecessary apologies. |
| Request or handoff | Make the requested action, responsible person, and timing easy to find. |

Use approved standard wording, facts, and links only when they fit the current situation. Do not reuse boilerplate that is outdated, misleading, too broad, or inappropriate for the recipient.

## 4. Draft the smallest complete email

Use this structure unless the user's examples show a better pattern:

1. Greeting, if normally used.
2. Purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Clear close and sign-off, if appropriate.

Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Put decisions and requests where the recipient can find them quickly. Use bullets only when they make actions, choices, or logistics clearer.

Remove:

- Throat-clearing and process narration.
- Generic compliments and repeated thanks.
- Filler such as “just wanted to” or “hope you’re well,” unless it is both normal for the user and useful here.
- Hedging that weakens a clear message.
- Explanations of how the draft was produced.

## 5. Run a final audit

Review the draft line by line before presenting it:

- Would the user plausibly write these exact words?
- Do the greeting, closing, punctuation, and rhythm match the available evidence?
- Is the tone right for this recipient and situation?
- Did the draft add an unsupported commitment, claim, opinion, or emotion?
- Are names, dates, links, attachments, and references correct?
- Is the requested action unmistakable?
- Does the email include only information appropriate for this recipient?
- Can any sentence be removed without losing meaning or usefulness?
- Does it avoid language the user has identified as undesirable?

## Failure modes to avoid

- Treating one old email as a complete voice profile.
- Copying a casual internal tone into a high-stakes external message.
- Matching style so closely that clarity, accuracy, or professionalism is lost.
- Reusing stale facts, links, or standard wording without checking relevance.
- Adding promises, emotional framing, or explanations the user did not provide.
- Including private information from examples that is not needed for the current email.
- Producing a polished but overly long email when the user's normal pattern is brief.

## Output

Provide the final email as copy-ready text. If clarification is necessary, ask only the specific question needed to draft safely. Do not add commentary after the final copy unless the user asks for alternatives, explanation, or revision notes.

If no voice evidence exists, briefly state the assumption and use a broadly useful default: concise, warm-professional, clear, and direct. Invite the user to provide a writing guide or a few representative examples for future drafts.


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
description: Close one month with evidence, then build a small, capacity-checked, explicitly approved plan for the next month. The workflow creates durable review and plan records while using only authorized, relevant information.
---

# Review and plan a month

Use this workflow at a month boundary to review recent progress and make an executable plan for the period ahead. A full session normally takes 45–75 minutes: first establish the evidence, then turn its lessons into a small set of approved commitments.

Review and planning belong together. The plan should address the structural reason a commitment slipped, work became draining, or progress stalled; it should not merely repeat goals with new dates.

## Purpose

Produce two durable records:

- A concise, evidence-based **Review** of the ending month.
- A practical **Plan** for the new month, with a memorable theme, up to three outcomes, capacity limits, explicit trade-offs, and failure counters.

The review may include selected work, personal-practice, wellbeing, and delivery signals when the user considers them relevant. Gather, discuss, and save only information needed for those outputs.

## When to run

Use this workflow when the user asks for a monthly review, asks to plan a named month, or wants help closing one month and starting another.

Unless the user specifies another range:

- During the first few days of a month, review the previous calendar month and plan the current one.
- Later in a month, review the current month to date and plan the following month.
- If the review is partial, label it as partial and state the review and planning ranges.
- A forward-planning request normally includes a review first, because evidence should shape the plan. The user can explicitly skip the review.

Ask whether the user means calendar months or a practical range that includes an overlapping week. Record the actual planning range in the final plan.

> Reviewing **March 2026** (01 Mar–31 Mar). Planning **April 2026** (01 Apr–30 Apr).

## Operating rules

1. **Evidence before reflection.** Show the factual picture before asking the user to interpret it.
2. **Batch independent reads.** Gather available records in one initial pass rather than repeatedly interrupting the discussion with small lookups.
3. **Use live commitments.** Compare results with the user’s current target, not an old schedule, abandoned project scope, or stale goal record.
4. **Treat data as fallible.** Before a strong negative conclusion, check for incomplete tracking, delayed updates, missing integrations, or inconsistent sources. Ask the user to confirm surprising findings.
5. **Use minimal authorized information.** Access private calendars, journals, health records, task systems, or communications only for a legitimate planning purpose and with clear authorization. Use the smallest relevant date range and fields, and do not repeat unrelated or sensitive details in summaries or saved records.
6. **The user makes choices.** The assistant calculates, summarizes, identifies constraints, and asks difficult questions. The user chooses priorities, cuts, and commitments.
7. **One decision at a time.** Do not advance through planning questions until the current one has a meaningful answer.
8. **Plan at month altitude.** Define outcomes, milestones, capacity, structure, and commitments. Leave detailed weekly task allocation to a weekly planning process.
9. **Approval is required before saving.** Brainstorms, notes, voice messages, and imported tasks are candidate inputs, not decisions. The user must explicitly approve the final plan.
10. **Use explicit dates.** Use **DD MMM** unless the user prefers another clear format.
11. **Save decisions, not transcripts.** Durable records should preserve evidence, choices, and constraints without copying unnecessary private material.

## Step 1: Set the range and gather evidence

Determine the review period, a comparable prior period, and the planning period. State them before proceeding. Then gather independent evidence in one initial batch where connected systems are available.

Use the user’s chosen tools or sources, such as a project tracker, task manager, calendar, spreadsheet, notes application, training log, health tracker, or user-provided facts. If no source is available, ask for a short factual inventory. Never imply that an unavailable source was checked.

| Evidence area | Gather only what is relevant |
|---|---|
| Previous monthly record | Prior theme, outcomes, commitments, review findings, and unresolved decisions. |
| Weekly records | Milestones, repeated blockers, carried work, and any weekly plans overlapping the new period. |
| Goals | Active short-, medium-, and long-range goals, with status and deadlines. |
| Delivery | Completed tasks, deliverables, decisions, or project movement grouped into useful domains. |
| Calendar | Fixed deadlines, travel or leave, recurring commitments, protected personal time, and meeting-heavy periods. |
| Personal signals | User-selected ratings, focus time, habits, training, sleep, or recovery measures. |

For a large source, use filtered reads, aggregation, or a concise delegated summary. Return computed measures and relevant themes, not raw journals, calendar entries, or personal records. If delegating, specify the authorized source, date range, and exact output needed. A calendar summary should normally identify fixed blocks, heavy weeks, recurring commitments, and conflicts affecting usable capacity.

Before finalizing the monthly plan, inspect any weekly plan that overlaps its beginning. Reconcile the two levels: the monthly plan sets direction and constraints; the weekly plan retains its detailed execution. Do not overwrite or duplicate the weekly plan.

## Step 2: Show the evidence picture

Present a compact factual picture. Be direct and numerical when the records support it. Do not yet ask broad reflective questions.

### Progress toward commitments

Summarize completed, missed, deferred, and rolled-forward weekly commitments. Give a hit rate when there is a meaningful total. For each active long-range goal, state whether it **advanced**, **stalled**, or **regressed**, with one short reason.

Explicitly identify goals that received no meaningful attention. These are often more informative than busy-work totals. Summarize completed work in a few meaningful domains rather than producing an exhaustive list.

### Personal practice, training, or health

Include this section when the user has an active commitment in scope. Compare actual activity with the live target. Depending on the domain, calculate only useful measures such as total volume, average weekly volume, active days, key milestones, longest gap, balance of session types, performance indicators, or change from the prior month.

Use these labels where appropriate:

- **ON TRACK:** primary measures are at least 90% of target and consistency is intact.
- **BEHIND:** a primary measure is roughly 60–90% of target, or consistency materially broke down.
- **OFF TRACK:** a primary measure is below 60% of target, or there was a prolonged gap.
- **AT RISK:** a safety, injury, burnout, or sustained-decline signal makes the current plan unsafe or unlikely.

Adapt the thresholds only if the user’s domain needs different rules, and record the rule used. If records may be incomplete, ask, “The record shows this; does it match reality?” before issuing a harsh verdict. State one biggest corrective action for the next month. It should be a specific commitment, not a generic recommendation or a full program.

### Life and capacity signals

Include only signals the user has chosen to track. Useful examples include rating distribution, average focus hours, low-focus days, sleep duration, sleep quality, recovery trends from the same source, and recurring themes in notes.

Flag material patterns: repeated short sleep, several low-energy days, sustained low focus, or a mismatch between positive numerical ratings and notes that repeatedly describe strain. Averages can conceal a persistent problem. Mention the pattern without quoting or saving unnecessary sensitive text.

## Step 3: Reflect on the month

Start with one specific observation grounded in the evidence. Ask one question at a time and follow no more than two or three threads unless the user asks for a deeper review.

Cover these topics:

1. What genuinely shipped and feels like a win?
2. What cost more time or energy than it returned?
3. Was the main miss structural, circumstantial, or a genuine priority change?
4. What one behavior, boundary, or operating pattern should change next month?
5. If a personal practice is in scope, what is the concrete next-month commitment?

Useful prompts include:

- “This outcome slipped across several weeks. What made it structurally hard to finish?”
- “The numbers look stable, but your notes point to strain. What was driving that?”
- “This goal advanced while others did not. What conditions made that possible?”

For a time-constrained session, use a minimum viable review: the in-scope commitment verdict, important wellbeing or capacity flags, one structural fix, and one concrete next-month commitment.

## Step 4: Build the new-month plan

A plan is not a list of events plus targets. It needs a defined outcome, an honest baseline, a path, evidence that the hours exist, trade-offs, forcing functions, a pre-mortem, and explicit approval.

### 1. Define outcomes

For each candidate priority, ask:

> What specifically is true by the final day of this planning range?

Make the answer measurable or plainly verifiable. Limit the plan to three outcomes; one or two is often better. Each should support a long-range goal or explicitly chosen responsibility.

### 2. Establish the current state

Size the gap with evidence, not mood. Inspect the relevant draft, project status, pipeline, baseline, backlog, or milestone. If the gap cannot be described, gather the missing information before designing a path.

### 3. Work backward from done

For each outcome, identify three to six moves required to close the gap. Work backward from the end date. Each move needs an owner, a date or time window, and observable evidence of completion.

> For this to be true by the end date, what must be true halfway through? What has to happen first?

### 4. Check capacity honestly

Estimate usable focused capacity from available working days and recently observed focus capacity, then account for fixed commitments and heavy periods. Compare supply with the effort required by the paths.

If demand exceeds supply, reduce scope, defer an outcome, change the approach, or add actual help. Do not preserve every priority by assuming future capacity will be better than recent evidence.

### 5. Make the NOT-doing list

Ask:

> What will explicitly not happen this month so these outcomes can?

The user names the cuts. A real plan includes trade-offs, not merely priorities.

### 6. Add forcing functions and structure

Fragile outcomes need an external forcing function: a stakeholder expecting a deliverable, a booked review, a public commitment, or a downstream dependency with a clear date.

Also protect interruption-sensitive work. Batch flexible work around meetings and reserve the best available periods for work that requires deep concentration. If a calendar conflict undermines the plan, add resolving it as an immediate action.

### 7. Run a pre-mortem

Ask:

> It is the final day of the month and this plan failed. What happened?

The user answers first. Record the two or three most plausible failure modes and a specific counter for each.

### 8. Get explicit sign-off

Read the whole plan back in ten lines or fewer. The user should be able to state the theme and main outcomes from memory. Ask:

> Is this the plan?

If approval is vague, revise. Do not save the plan until the user explicitly confirms it.

## Plan template

```markdown
## THEME: [MEMORABLE, ACTION-ORIENTED LINE]

**Planning range:** [DD MMM–DD MMM].

## Shape of the month
[Fixed commitments, heavy periods, effective working weeks, and important constraints.]

## Outcomes
1. **[Outcome]** — Done by [DD MMM] when [binary test of done].
   - Current state: [honest gap].
   - Path: [dated moves, owners, and completion evidence].
   - Forcing function: [external commitment].

## Capacity check
[Available capacity] versus [committed demand]; [scope decision].

## NOT doing
- [Explicit cut or deferral.]

## Structure
[Behavior, boundary, or environment change that counters the reviewed drain; include tracked delegated work and owners.]

## Personal commitment
[Specific measurable commitment, if in scope.]

## Pre-mortem
- Failure mode: [likely cause]. Counter: [specific response.]
```

## Step 5: Save the review and plan

After sign-off, create or update two records in the user’s chosen system: the Review on the ending month and the Plan on the new month. Use one final write operation where possible. If an existing plan would be overwritten, show the conflict and resolve it first.

Keep saved content within the user’s authorization and access boundary. Do not copy private journal passages, health details, calendar information, or details about other people unless they are necessary for the plan and appropriate to retain.

Use this review template:

```markdown
## Commitment verdict
**[ON TRACK / BEHIND / OFF TRACK / AT RISK / NOT IN SCOPE]**

- Actual: [key measures].
- Target: [current agreed target].
- Consistency: [relevant pattern or gap].
- Change from prior period: [key delta].
- Verdict: [one direct sentence].
- **Next-month commitment:** [specific commitment].

## Goals and delivery
- Weekly commitments: [completed]/[total] ([percent]%).
- Long-range goals: [goal — advanced, stalled, or regressed; why].
- Work delivered: [concise grouped summary].

## Life and capacity signals
- [Selected measures and meaningful flags.]

## Win
[One meaningful result.]

## Drain
[One thing that cost more than it returned.]

## Structural fix for next month
[One specific behavior, boundary, or system change.]
```

Confirm the save in one line, then stop.

## Step 6: Improve the workflow

After each run, make one precise improvement to the reusable workflow, template, or data mapping. Store it in the user’s chosen workflow document or improvement log; if none exists, present it as a short durable rule for the user to save.

Look for a noisy read, a false data assumption, a misleading metric, a user correction, or a repeatable planning pattern. Prefer one specific edit over a vague reminder.

## Audit checks

Before finishing, verify:

- Review and planning ranges are explicit.
- Evidence appeared before reflective prompts.
- Strong verdicts accounted for material data-quality limits.
- The plan has a named theme and no more than three outcomes.
- Each outcome has a test of done, date, path, owner, and forcing function.
- Capacity fits demand, or an explicit scope decision was made.
- The NOT-doing list contains genuine cuts.
- The structural fix responds to a reviewed drain.
- Overlapping weekly plans were reconciled.
- In-scope personal commitments are specific.
- The pre-mortem includes counters.
- The user explicitly approved the plan before it was saved.
- Saved content remains within the appropriate authorization and privacy boundary.

## Common failure modes

- Starting with introspective prompts instead of evidence.
- Judging performance against an obsolete target or incomplete record.
- Treating a calendar of events as a plan.
- Overcommitting capacity and refusing to cut scope.
- Letting the assistant select priorities for the user.
- Saving an unapproved draft.
- Conflicting with an existing weekly plan.
- Treating averages as more truthful than repeated evidence of strain.
- Applying generic productivity advice instead of fixing the actual structural drain.
- Treating brainstormed items as confirmed commitments.
- Saving unnecessary sensitive details in a durable record.


---
name: get-unstuck
description: A short rescue workflow for turning tiredness, dread, confusion, or distraction into one bounded period of useful action without making the coaching itself another avoidance ritual.
---

# Get unstuck

Use this workflow when someone cannot begin, is losing momentum, dreads a task, feels depleted, or is repeatedly pulled into distraction. It is not a complete productivity system. Its purpose is to diagnose the immediate barrier, run one short matched intervention, and help the person begin one bounded work block.

The central rule is: **diagnose before prescribing.** Avoidance is often an attempt to regulate discomfort, not evidence of laziness or poor character. A useful response treats tiredness, emotional resistance, unclear work, and distracting environments as distinct but often overlapping problems.

## Purpose and success criteria

Aim for one work block, not completion of the whole task. The person may start imperfectly; a rough first action is success.

A successful rescue usually means:

- the person begins within about 10–15 minutes of invoking the workflow;
- they complete one timed block, normally 25 minutes or a shorter block when depleted;
- the intervention is brief enough that it does not become a new procrastination ritual.

Use the following order when more than one barrier is present:

1. Physical state.
2. Emotional resistance.
3. Cognitive clarity.
4. Work environment and distraction controls.

Do not try to reason someone through a task while their body is severely depleted. Do not use harshness when shame, exhaustion, or overload is present.

## Step 0: Diagnose in two minutes or less

Ask one compact message with three questions. If the task is already clear, omit the first question.

1. **What is the task in one line?**
2. **Rate each from 0–10:** tiredness, dread of the task, unclear next step, and pull toward distraction.
3. **How much time is available before the next commitment?**

If the person has explicitly agreed to keep a private reflection record, review only recent, relevant entries before responding. Use the minimum information needed: recent intervention results, preferred communication styles, and repeated patterns. Do not quote private records back unnecessarily. Do not access messages, calendars, documents, or other personal records without a legitimate purpose and clear authorization. When searching authorized sources, use only material relevant to reducing the task and omit unrelated or sensitive details.

### Classify the state

- The highest score is the **dominant barrier**.
- If two or more scores are 5 or above, treat it as a **compound state**.
- If tiredness and dread are both very high over several recent attempts, treat this as a possible **capacity problem**, not a motivation problem.

For a recurring capacity problem, pause the usual rescue and ask:

> “Your energy and dread have both been high repeatedly. What is the case for not doing this today? Could it be delegated, reduced, or deferred for 24–48 hours? What would genuinely restore capacity?”

Do not pressure the person into a work block simply because they asked for motivation. If they still choose to proceed, say plainly that they are working against a warning signal and reduce the scope as much as possible.

## Step 1: Choose and name the coaching style

Name the style briefly. This makes feedback usable and gives the person permission to request a change.

> “I’ll be practical and warm for this one. Tell me if you want direct instructions, more analysis, or less talking.”

Use these broad defaults, then revise them based on observed results and the person’s preference.

| Dominant state | Default style | Reason |
|---|---|---|
| High dread, manageable tiredness | Empathetic or analytical | Naming the feeling can reduce its force; analysis helps a receptive person examine the threat. |
| High uncertainty, low dread | Analytical | The blockage is usually task decomposition. |
| High distraction, low dread | Direct | A short environmental interruption is more useful than discussion. |
| High tiredness | Practical-warm | Depletion needs brevity, care, and reduced demands. |
| Compound state | Practical-warm | Avoid both cold commands and long reassurance. |
| Explicit request for a tougher tone | Direct | Use only when the person is physically capable, wants this approach today, and is not shame-flooded. |

Switch styles when the response is not landing. Move to direct instructions if the person asks for concise commands. Move to empathy if they say the approach makes them feel worse, become self-critical, or go quiet after pressure. Move to analysis if they argue with the framing and need to reason through the problem.

## Step 2: Run one matched intervention

Keep the whole rescue to 15 minutes whenever possible. Run physical interventions before emotional or cognitive ones when tiredness is high.

### A. Physical reset

Use this first when tiredness is around 6 or higher, or when dread is intense enough that a body-level state change is likely to help.

Give a crisp, bounded instruction:

- Drink a glass of water.
- Move for five minutes: outside if possible, otherwise stairs, brisk walking, or simple movement indoors.
- Get daylight or stand near a bright window.
- Leave the distracting device behind during the reset.
- Optionally use cool water on the face or have a small snack if hunger is plausible.

An unstructured reset should normally take no more than 10 minutes. A longer reset, up to 20 minutes, is appropriate only when it has a defined destination, modest reward, and explicit return cue—for example, walking to a nearby café, getting a drink, and returning when the timer ends.

Respect a reasonable request for a break, but bound it. Do not let breaks expand indefinitely.

### B. Emotional intervention

Use one intervention, not all of them. If the person is using self-insults, making self-deprecating jokes, or withdrawing after a directive, respond with compassion rather than more pressure.

Choose one of the following:

- **Self-compassion pause:** “This is difficult. Difficulty is part of being human. What is the kindest useful next step?”
- **Defusion:** Ask them to say, “I am having the thought that this will go badly,” rather than treating the thought as fact.
- **Values anchor:** “This matters because it supports [a chosen responsibility, relationship, or goal]. Doing one block is an act of that value.”
- **Importance reframe:** For a calm, analytical person: “Strong avoidance may mean the task feels consequential. That is a signal to reduce the first step, not proof that you cannot do it.”

Do not use a stern or drill-like frame on an exhausted or shame-flooded person. It often compounds avoidance.

### C. Cognitive intervention

Once the body and emotional state are sufficiently settled, make the task mechanical.

1. Replace abstract verbs with visible actions. For example, replace “prepare the report” with “open the source folder and list the three required sections.”
2. Find the **30-second version** of the first action: the first click, first document, first heading, or first sentence.
3. Create an implementation intention: **“If it is [cue or time], then I will [specific action] at [specific place].”**
4. Time-box the effort rather than promising an outcome. Use 25 minutes by default and about 15 minutes for a depleted state.

For work that depends on searchable materials, offer authorized practical help. With clear permission, an assistant or suitable tool can search relevant documents, meeting notes, messages, or records; extract task-relevant facts into a scratchpad; and leave unrelated private details out. This can reduce blank-page dread by turning “find everything” into “review a short set of candidate material.”

## Step 3: Start the block

State the duration aloud. Confirm a minimal environment:

- phone physically away or blocked;
- one task and, where practical, one active tab or document;
- distracting applications and notifications closed;
- required materials already open.

Then stop coaching. Do not keep chatting during the work block unless the person asks for necessary task help. Working is more valuable than describing work.

## Step 4: End-of-block check

When the person returns, ask for only three things:

1. What came out of the block, in one sentence?
2. What are tiredness and dread now, each from 0–10?
3. One question: **another block or stop?**

If they stop, acknowledge the specific success:

> “You began despite resistance and completed the block. That counts.”

Do not turn a completed block into pressure for more. If they continue, repeat the same timer and environment. Re-diagnose only if their state clearly changed.

## Step 5: Record and improve, with consent

If the person wants tracking, append a concise session record in their chosen private system. Keep it parseable and limit it to work-relevant information.

```text
## [date and time] — [task in 3–5 words]

- Start state: tired [N], dread [N], unclear [N], distraction [N]
- Dominant mode: [tired / dread / unclear / distraction / compound / capacity]
- Style: [direct / analytical / empathetic / practical-warm]
- Interventions: [list]
- Blocks: [number and duration]
- Outcome: [started yes/no; blocks completed; end state]
- What helped: [one line]
- What did not help: [one line]
- Style verdict: [landed / missed; adjustment]
```

Review patterns only after enough observations to justify a change. If a style repeatedly fails, demote it. If an intervention repeatedly helps a particular state, offer it earlier. Add a new branch only when a recurring pattern is genuinely distinct. Do not invent refinements merely to appear active.

## Failure modes and safeguards

- **Over-coaching:** If diagnosis or discussion exceeds 15 minutes, choose a tiny first action or stop for recovery.
- **Mistaking capacity for discipline:** Repeated high tiredness plus high dread calls for reduction, deferral, support, or rest.
- **Treating emotional dread as a planning flaw:** Name the emotion before decomposing the task.
- **Treating unclear work as a character flaw:** Convert it into observable, low-stakes actions.
- **Trying to resist distraction while sitting inside it:** Physically separate from the device or cue first.
- **Unbounded breaks:** A break needs a timer and return cue.
- **Unauthorized source mining:** Never search personal or organizational records without clear permission, a legitimate task purpose, and appropriate access.
- **Using shame as fuel:** Do not escalate harshness in response to self-criticism, silence, exhaustion, or distress.

The workflow is complete when the person has either begun one bounded block or made a deliberate, justified decision to defer and restore capacity.


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
description: Gather the relevant history, clarify the desired outcome, and create a focused, privacy-aware meeting brief and agenda in the user’s chosen workspace. The workflow requires a visible situation brief and targeted questions before drafting.
---

# Prepare for a meeting

Use this workflow to prepare one consequential meeting. It produces a reusable meeting page or document, not merely a chat summary. It works with any calendar, email, messaging, document, contact, applicant-tracking, or workspace system that the user is authorized to access.

For a full day of meetings, run this workflow separately for each meeting so each has its own research, decisions, and agenda.

## Purpose and boundaries

The goal is to help the meeting owner enter the conversation with the right context, a clear desired outcome, a realistic agenda, and a small set of decision-relevant questions.

Use private communications, records, and transcripts only for a legitimate meeting-related purpose and with clear authorization. Use the minimum relevant sources and information. Respect consent, privacy expectations, and access boundaries.

When records include personal, confidential, financial, health, employment, or other sensitive information:

- Use it only when relevant to the meeting and permitted within the user’s access boundary.
- Do not copy unrelated personal details into the meeting page.
- Do not expose sensitive information to a broader audience than the original source permits.
- State uncertainty rather than treating a tentative identity match or old record as fact.
- For hiring, advising, funding, performance, or reference-related meetings, focus on role-relevant capabilities, diagnostic evidence, goals, and process rather than personal speculation.

Never put compensation, salary, equity, offer figures, budget amounts, account data, credentials, or similarly restricted figures in a shared meeting page. If such context matters, use a non-numeric description such as “offer follow-up,” “funding constraints,” or “a materially different package.”

## Inputs and defaults

Collect or confirm the following.

| Input | Useful default or rule |
|---|---|
| Meeting date and time | Use the calendar event and confirm the meeting owner’s time zone. |
| Meeting selection | Prepare the requested meeting; otherwise prioritize external one-to-ones and small groups over routine blocks. |
| Meeting duration | Use the invitation duration; ask if the event is ambiguous or likely to change. |
| Attendees | Record name, role, organization, and contact channel when available. |
| Delivery location | Use the user’s chosen workspace, notes database, or document system. |
| Access scope | Use only connected or supplied sources that the user may access for this purpose. |

Exclude obvious non-meetings such as focus blocks, travel holds, meals, personal reminders, and internal placeholders unless the user explicitly asks to prepare them.

## Workflow overview

Follow the stages in order:

1. Read the calendar event.
2. Research the relationship and meeting context.
3. Read the artifact the meeting is about.
4. Detect whether a specialized workflow is needed.
5. Post a situation brief.
6. Ask targeted questions and wait for answers.
7. Create the meeting page and agenda.
8. Run quality checks, save it, and make it easy to open before the meeting.
9. Schedule a post-call review when a persuasion or decision-moving conversation warrants it.

Do not jump from research directly to an agenda. The meeting owner’s goal, boundaries, authority, and preferred level of directness often change the agenda substantially.

## 1. Read the meeting invitation

Retrieve the detailed event information from the chosen calendar. Extract:

- Title and stated purpose.
- Start and end time, time zone, and duration.
- Attendees, including external and internal participants.
- Location or joining information, if relevant.
- Description, attachments, and linked documents.
- Scheduling context, such as an introduction, reschedule note, conference follow-up, hiring stage, or request for feedback.

Classify the meeting provisionally: relationship-building, information-gathering, advice, recruiting, sales or partnership, negotiation, proposal review, reference conversation, decision meeting, or routine check-in. This classification is a hypothesis until research and the user’s answers confirm it.

## 2. Research the people and relationship

For each relevant external attendee, gather enough context to understand who they are, why this conversation exists, and what has already happened. Parallelize independent searches when possible, but do not turn broad searching into unnecessary surveillance.

### Recommended source sequence

1. **Direct correspondence.** Search messages sent to or received from the attendee. Read several recent, relevant threads rather than relying on subject lines.
2. **Name mentions.** Search the attendee’s full name in authorized messages and notes. This may surface introductions, references, shared projects, hiring discussions, or context where the person was not a direct sender or recipient.
3. **Internal conversation history.** Search authorized chat, project discussions, and shared notes for their name and organization.
4. **Prior meetings.** Search calendar history and the meeting-notes system for previous conversations, promises, decisions, and unresolved issues.
5. **Public professional context.** Use reputable public sources to confirm role, organization, relevant work, publications, and timely news. Prefer primary sources such as an organization profile, personal site, published work, or direct public statement.
6. **Authorized internal records.** If the meeting concerns an applicant, advisor, customer, participant, fund recipient, or other formal relationship, search the relevant authorized system for the full record. Confirm identity using stable evidence such as email address, employer, institution, role history, or other corroborating information.

If a name match could refer to different people, do not merge records based on name alone. Use the record only after confirming identity. Otherwise omit it or label it clearly as unconfirmed.

### What to synthesize

Capture the following concisely:

- **Who they are:** current role, organization, and relevant background.
- **Organization context:** what the organization does and why it may matter to the meeting.
- **Relationship history:** prior meetings, correspondence, commitments, introductions, and unresolved threads.
- **Why now:** the triggering event or current decision that made the meeting happen.
- **Current situation:** recent changes, deadlines, alternatives, constraints, or news that could affect the discussion.
- **Useful links:** only links likely to help the meeting owner prepare or follow up.

Keep fact, interpretation, and source confidence distinct. A public announcement can establish that an organization changed direction; it does not establish why an attendee wants to meet. Treat the latter as a hypothesis to test.

## 3. Read the artifact the meeting is about

When the meeting concerns a proposal, pitch, strategy, memo, application, draft, plan, deck, brief, or other written artifact, read the complete relevant artifact before writing the agenda.

Signals include:

- A meeting title or message asking for feedback, comments, review, or consultation.
- A linked document, slide deck, PDF, folder, or workspace page.
- Notifications about comments on a named document.
- References to “the proposal,” “the draft,” “the plan,” or “the deck we discussed.”
- An applicant or candidate whose submitted material is central to the conversation.

Use the system’s safe reading procedure for multipart documents: enumerate sections, tabs, attachments, or pages first, then read all material relevant to the request. Do not claim to have reviewed a document that was only skimmed.

If context strongly suggests that an artifact exists but it cannot be found, ask the meeting owner for the link during the question stage. Do not produce a generic discussion plan when the real purpose is to pressure-test a specific written proposal.

## 4. Route specialized meetings to the right workflow

Before drafting a general page, check whether the meeting is actually a specialized conversation that needs a dedicated structure.

A reference conversation should use an authorized reference-call workflow with consistent role-relevant probes, evidence checks, and privacy handling. Signals include explicit use of “reference,” discussion of an applicant or candidate, or an attendee expected to speak about another person’s work.

Likewise, route formal interviews, sensitive employee matters, legal discussions, incident reviews, regulated decisions, or other high-risk conversations to approved procedures when they exist. Carry forward relevant research so the work is not duplicated, but do not create a generic agenda that bypasses needed safeguards.

## 5. Post a situation brief before asking questions

Once research is complete, post a short visible brief in the conversation. The brief helps the meeting owner reload the situation and answer questions efficiently. It is a deliverable in its own right, not a hidden scratchpad.

Choose a shape that fits the meeting:

- **Narrative brief:** who the attendee is, what has happened, why the meeting is occurring, and the central tension. This is the default for most meetings.
- **Decision-shaped brief:** the ask, alternatives and deadlines, the meeting owner’s position, risks, and unknowns. Use it for recruiting, negotiations, closes, fundraising, partnerships, or other live decisions.
- **Facts and dynamics:** a compact facts table followed by motivations, risks, and open questions. Use this for data-heavy or multi-party meetings.

Explain unfamiliar names, organizations, programs, and terms wherever they appear. If a reader could encounter one section alone, make that section understandable without requiring the rest of the brief.

## 6. Ask targeted questions, then wait

After posting the brief, ask targeted questions before drafting the goal or agenda. This is a required readiness gate for consequential meetings.

Ask about factors that will materially change the meeting plan:

- **Primary outcome:** What should be true by the end of the meeting?
- **Their situation:** Is the attendee exploring, deciding, committed, blocked, or seeking something specific?
- **Sensitive substance:** Should the meeting owner state a view directly, or first draw out the other person’s perspective?
- **Failure mode:** What must the meeting avoid—overselling, being too passive, anchoring on the wrong issue, mishandling a sensitive topic, or leaving without a next step?
- **Specific ask:** Is there an introduction, commitment, decision, advice request, artifact, or follow-up to seek? How direct should it be?
- **Anything else:** What history, constraint, topic, or concern should shape the preparation?

Ask only questions that genuinely affect the agenda, but cover the goal and at least one of tone, risk, or ask. Always include an “anything else” option.

Use compact labels so answers are auditable and quick. Questions should have three or four genuinely distinct options, with a recommended option first when evidence supports one. Do not force a false choice when options can combine.

```markdown
1. What is the primary outcome?
   - **1a (recommended):** Understand their priorities and agree on a concrete next step
   - **1b:** Build the relationship without making an ask
   - **1c:** Make a direct proposal and test their willingness to proceed

2. How direct should the close be?
   - **2a (recommended):** Propose a date-bound follow-up or named artifact
   - **2b:** Offer help and let them choose whether to continue
   - **2c:** Keep this exploratory and make no explicit ask

3. Is there anything else to land or avoid?
   - **3a:** Nothing to add
   - **3b:** I will add notes or constraints
   - **3c:** There is sensitive context to handle carefully
```

If the interface limits the number of questions, use multiple rounds. Put questions that determine later choices first, then adapt the second round based on the answers. Before sending, verify that question numbers and labels are unique, sequential, and complete.

Do not ask the meeting owner to write the agenda. Ask for outcomes, boundaries, authority, and risks; turn their answers into the agenda yourself.

Only skip questions when the meeting is truly routine, its purpose and desired outcome are documented, and no consequential choice remains. When uncertain, ask.

## 7. Create the meeting page

Create one page in the user’s chosen meeting workspace after the brief and question answers are available. Save the meeting date as a date-only field unless the workspace explicitly requires a time. Use the actual meeting date in the owner’s time zone. Do not place confidential material in a workspace visible to people who lack access.

Use a clear title, such as `[Date] – [Attendee or meeting topic]`. For group meetings, list key participants or a precise topic rather than every attendee.

Use this content structure:

```markdown
# [Meeting title]

## Context
Who the attendee is, relationship history, why the meeting is happening, and the few links or facts that matter.

## Goal
A proposed, outcome-oriented goal based on the meeting owner’s answers.

## Agenda
Text under **Say** is word for word. Anything in [square brackets] is a cue, not something to say aloud.

### 0–5 min: Open and frame
**Say**

[Opening language that establishes purpose and stakes.]

**Private note**

[What to avoid or listen for.]

### 5–20 min: Diagnose [key topic]
**Questions**

1. [Decision-relevant question]
2. [Follow-up question]

**Private note**

[Signals to test and assumptions to challenge.]

### 20–35 min: Explore, pressure-test, or propose
**Say**

[Transition or proposal language.]

**Questions**

1. [Specific question about trade-offs, evidence, or fit]

**Private note**

[How to respond to likely concerns.]

### Final segment: Close and forcing function
**Say**

[Clear summary and next-step language.]

**Questions**

1. [Question that produces a date, owner, artifact, decision, or explicit reason not to proceed]

**Private note**

[Backup close if the preferred next step is not available.]

## Five most important questions

1. [Most decision-relevant question]
2. [Second most important question]
3. [Question that tests the central uncertainty]
4. [Question that identifies the key constraint or trade-off]
5. [Concrete close or next-step question]

## Timely note

[Optional: a relevant recent publication, announcement, or event to mention.]
```

Adjust timing to the actual duration. Put the most important discussion before background, updates, or rapport-building. If it is a first meeting, say so. For recurring contacts, describe the relationship arc: what has changed, what was promised, and what remains unresolved.

Write **Say** blocks as words the meeting owner can speak aloud. Keep private guidance in **Private note** blocks. Do not hide instructions inside a spoken script. Avoid quotation marks around spoken language unless quoting someone else is essential.

The five-question section is an in-call cheat sheet, not a second agenda. It must contain exactly five short, ranked, decision-relevant questions. Include a forcing-function close when the meeting seeks movement or commitment.

## 8. Audit before publishing and after saving

Run these checks before creating the page and once more after saving it:

1. **Question gate:** Was a situation brief posted, targeted questions asked, and answers received? If not, return to Step 6.
2. **Artifact gate:** If the meeting is about a document or submitted material, was the relevant artifact read in full? If not, read it or ask for it.
3. **Identity gate:** Are historical records confirmed to belong to the attendee?
4. **Proper-noun check:** Would the meeting owner understand every unfamiliar person, organization, program, or technical term without the research? Explain it briefly or remove it.
5. **Evidence check:** Are uncertain, old, conflicting, or single-source claims labeled as such?
6. **Privacy check:** Does the page omit unrelated personal data, salary or offer figures, credentials, and restricted details?
7. **Agenda check:** Do timed sections fit the meeting duration? Does the agenda reflect the owner’s answers rather than the assistant’s assumptions?
8. **Close check:** Is there a clear desired next step and a fallback if the preferred close fails?
9. **Storage check:** Are date, title, attendees, and access permissions correct in the saved page?

Retrieve the saved page or document after creation to verify that fields and content rendered correctly. Repair errors before declaring the preparation complete. Then open or prominently link the page in the user’s chosen meeting application so it is available at meeting time.

## 9. Post-call review for persuasion or decision-moving meetings

For recruiting, partnership, negotiation, fundraising, sales, pitching, or any call where the meeting owner is trying to move a decision, schedule a one-time review for roughly one hour after the meeting ends if authorized tools, recording consent, transcript access, and an appropriate private storage location are available.

The review should:

- Retrieve the authorized meeting transcript or notes, using the least sensitive source available.
- Compare the conversation with the preparation goal and agenda.
- Record what happened, what moved the decision, objections, missed opportunities, commitments, owners, dates, and follow-up artifacts.
- Identify recurring communication patterns using dated evidence rather than vague labels.
- Save the review within the appropriate private coaching or project boundary.

Skip this for purely informational meetings or when recording, transcript access, consent, or appropriate storage is unavailable.

## Common failure modes

| Failure mode | Prevention |
|---|---|
| Research becomes a generic summary | Explain why the meeting is happening and what decision or uncertainty matters now. |
| The agenda is written before the owner’s goal is known | Post the brief, ask targeted questions, and wait for answers. |
| A proposal meeting gets generic questions | Find and read the actual artifact before planning discussion. |
| Records from two people with the same name are merged | Confirm identity with stable corroborating details before using any old record. |
| The page contains too much sensitive information | Apply the minimum-necessary rule and keep restricted details out of shared space. |
| The agenda has no close | Include a concrete question about owner, date, decision, or next artifact. |
| Scripts mix spoken words with instructions | Put exact language under **Say** and private cues in separate notes. |
| Unexplained names confuse the reader | Explain unfamiliar names and terms in every stand-alone section where they matter. |

A meeting preparation is complete only when the verified page is saved in the appropriate workspace, the meeting owner has had a chance to shape the outcome, and the agenda is ready to use in the room.


---
name: capture-meeting-actions
description: Review authorized meeting records, identify genuine unfinished commitments, create clear deduplicated follow-up tasks for confident actions, and batch only questions that require judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose, authorization, and operating rules

Use this workflow only for a legitimate work purpose and when the user is authorized to access the meeting records and create or update tasks. Review only the minimum relevant records and details. Do not copy unrelated personal, health, family, compensation, or other sensitive information into a task. Keep notes within the access boundary appropriate to the destination task system and its intended audience.

Before each run, apply these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

When sources conflict, use this evidence order:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often assign actions to the wrong attendee, particularly in recurring one-to-ones, brainstorming sessions, and meetings where people list their own to-dos. Never create a task solely because a summary labels an item as an action. Confirm ownership in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work that was completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, expression of interest, or open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply known responsibility boundaries supplied by the user or organization. Attending a meeting does not make the user accountable for all work discussed in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Locate meetings attended by the user and collect only what is needed:

- Title, date, and time
- Meeting-record link or identifier
- Attendees, if available
- Transcript, notes, summary, and relevant linked context

Report a compact count before processing. Do not infer actions from a meeting title alone.

## 2. Fetch and inspect complete records

Retrieve full meeting records in parallel when the selected systems support batching. Do not search for existing tasks yet: first identify the people, topics, and candidate outcomes that make deduplication accurate.

For long transcripts, use a repeatable search, extraction, or chunking method rather than relying on truncated previews. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by explicit acceptance

Review summary action items as candidates, then verify them against the transcript and surrounding conversation. A promise may have been conditional, reassigned, completed during the call, or directed at another attendee.

## 3. Triage each meeting

Classify the meeting loosely. Classification provides a starting expectation; it does not override evidence.

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
- Relevant source and related links

Create no task when work was completed live, another person owns it, the meeting was purely informational and any necessary synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

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

- **Title:** short, verb-led, and specific, such as “Follow up with prospective partner about pilot scope.”
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user’s scale; default to normal important work and reserve the highest level for a real deadline, material risk, or a waiting counterparty.
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

Avoid unnecessary private discussion in a task system that may be broadly visible. Follow the user’s known writing preferences. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable.

If the task is to send a message, write a ready-to-send draft rather than merely saying “email them.” For introductions, use double opt-in: seek permission from each relevant person before connecting them.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by meeting link or identifier, counterparty, distinctive topic terms, and proposed title.

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. Skip the new task, or update the existing task if the meeting adds a meaningful action, deadline, or context. Record the duplicate decision so it can be reported clearly.

## 7. Create confident tasks

Create high-confidence tasks in a batch when possible. If the task system supports direct access to newly created records, make those records available through the normal user workflow rather than adding unnecessary management links to the status update.

For every skipped meeting, give a brief reason, such as:

- “No out-of-meeting commitment.”
- “Completed during the meeting.”
- “Owned by another role.”
- “Already covered by an active task.”

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

Wait for answers before creating uncertain tasks. After answers arrive, create or update the remaining tasks and repeat the relevant duplicate check if the answer changed the task outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, capture lessons that genuinely improve future runs. Keep reusable guidance separate from the individual meeting task.

- Add a short pattern note when a recurring issue affects triage, such as a common attribution error, a reliable sign of in-meeting completion, or an exception for a meeting type.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a responsibility boundary in the user’s or organization’s maintained reference only when it applies beyond one meeting.

Do not turn one-off facts into permanent rules. Small additions to a patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing a step or changing the evidence order. Briefly report reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task includes a source reference where appropriate.
- Message drafts are ready to send and follow the user’s preferences.
- Every uncertain item is either asked as a specific question or explicitly deferred.
- Task notes contain only information appropriate for the destination system and intended audience.

Report only the essential outcome: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and reusable guidance changes. Keep status updates terse and factual.


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
description: Create or improve a short, paid, asynchronous work sample that produces role-relevant evidence, can be reviewed consistently, and is validated through realistic simulated submissions.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A good work sample asks candidates to do a realistic, bounded version of the job, produces evidence that is difficult to imitate with generic answers, and can be reviewed quickly and consistently.

Use it for a new exercise or a revision. Do not use it for interview questions, application-form screeners, or multi-day work trials. If a request could mean one of those formats, ask which format is needed before proceeding.

## Purpose and design principles

A work sample commonly sits between initial screening and interviews. Its purpose is narrow: help the hiring team assess whether a candidate can demonstrate the role-critical capabilities in a realistic but safe scenario.

A work sample should not attempt to assess the entire person or every aspect of the job. Different methods provide different evidence:

- Interviews can assess live communication, motivation, collaboration, and interactive reasoning.
- References can assess reliability, integrity, and sustained performance over time.
- A later trial can assess consistency, judgment in real systems, and work over several days.
- Onboarding can often address knowledge of a particular tool, process, or internal vocabulary.

Focus the exercise on three to five load-bearing capabilities that are important to the role and observable in a short exercise. Examples include prioritization, practical judgment, decision-making under uncertainty, clear writing, sourcing, problem diagnosis, execution speed, systems thinking, or turning ambiguity into useful work.

Use these default constraints unless the hiring owner chooses otherwise:

- Make the exercise paid.
- Set a clear expected time limit, usually two to four hours.
- Use a realistic but fictionalized or safely anonymized scenario.
- Do not request work that the organization will use commercially unless that use is separately agreed with the candidate.
- Design for roughly 20 to 25 minutes of reviewer time per submission.
- Make the exercise self-contained. Candidates should not require internal tools, private data, or access to unavailable people.
- State what AI assistance is permitted. Assess judgment and output quality rather than trying to infer tool use from prose style.
- Test only role-relevant capabilities. Do not use protected characteristics, personal history, or unrelated proxy criteria.
- Offer a clear route to request reasonable accommodations or an equivalent accessible format without lowering the role-relevant standard.

If the workflow requires access to private hiring notes, prior assessments, or communications about people, confirm there is a legitimate hiring purpose and clear authorization. Read only the minimum relevant materials, exclude unrelated personal details, and keep all drafts, simulations, and reviewer guidance within the approved hiring access boundary.

## Step 1: Pre-flight

Before designing the work sample, confirm that the hiring team has both:

1. A current job description or role brief describing responsibilities, seniority, expected outcomes, and reporting context.
2. A role-success profile, hiring plan, or equivalent document identifying the capabilities and experience most likely to produce the required outcomes.

If either is missing, stop. Do not try to define the role-success profile while drafting the test. That creates a moving target and usually creates an exercise that appears plausible while measuring the wrong things.

Use this request:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

When the materials exist, read the full relevant role context. This may include project notes, operating constraints, examples of strong work, prior hiring feedback, and existing exercises for comparable roles. Read one or two reference exercises only to calibrate tone, length, and delivery format. Do not copy a task shape simply because it worked for another role.

Give a brief status update after review, for example: “Read the role brief, success profile, and two comparable exercises. Moving to the alignment memo.”

## Step 2: Write the alignment memo before drafting

Do not write candidate-facing instructions yet. First prepare a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five capabilities that the role succeeds or fails on and that can be surfaced during the exercise window. Describe observable behaviors rather than abstract traits.

Weak: “Strategic thinking.”

Better: “Can identify the highest-leverage problem in a messy operating situation, explain the tradeoff, and produce a useful first action.”

### What the exercise will not test

Name important criteria that should be assessed elsewhere. This prevents the test from becoming an unrealistic proxy for the entire job.

For example, a three-hour asynchronous exercise may not fairly assess long-term reliability, leadership over months, live-meeting responsiveness, specialized software fluency, or sustained collaboration.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level. Explain the consequence for exercise design:

- Entry-level candidates may need more context and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make tradeoffs, establish direction, and create work another person could use without further explanation.

### Failure modes to catch

Identify two or three plausible work patterns that could otherwise look strong in a conventional process but would create problems in this role. Describe evidence, not labels.

Examples include:

- A polished planner who does not produce usable work.
- A fast executor who misses the central problem or creates avoidable risk.
- A careful candidate who defers every consequential decision.
- A technically capable candidate who cannot communicate with the intended audience.

### What strong looks like

Write a short paragraph describing a top submission. Focus on what it notices, the choices it makes, the quality of the outputs, and how it handles uncertainty.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the owner confirms or revises the memo.

## Step 3: Propose exercise shapes

After the memo is approved, propose three exercise shapes. Each option must test the confirmed capabilities in a distinct way, be understandable within about a minute, be self-contained, and be scorable quickly.

For each option, provide:

- **Shape:** A plain-language description of the task.
- **What it tests:** The load-bearing capabilities it reveals.
- **Why it is evaluable:** The evidence reviewers will see and why it can be reviewed consistently.
- **Main risk:** The likely source of noise, unfairness, or weak signal.

Keep each option concise. Useful shapes include:

- **Triage pile:** The candidate receives realistic messages, requests, and constraints. They prioritize, draft responses or work products, and recommend one systemic improvement. Useful for operations, coordination, support, and communications-heavy roles.
- **Choose the highest-leverage action and ship it:** The candidate receives several possible priorities, selects one, explains the tradeoff, and creates a small usable output. Useful for strategic operations and builder roles.
- **Diagnose and fix:** The candidate reviews a messy situation, identifies the central problem, and produces one targeted intervention. Useful for product, program, analytical, and process-improvement roles.
- **Source and pitch:** The candidate defines a target profile, identifies promising channels or prospects from supplied information, and writes outreach. Useful for recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** The candidate assesses a supplied intervention area and makes a recommendation for a decision-maker. Useful for research, policy, strategy, and specialist roles.
- **Design a repeatable system:** The candidate creates a lightweight process, playbook, or operating artifact another teammate could use. Useful for enablement, programs, community, and operational-design roles.

Do not draft the full exercise until the hiring owner chooses a shape. If none fits, generate three more based on the confirmed capabilities rather than forcing a familiar format.

## Step 4: Draft version 1

Write the candidate-facing exercise in this order.

## [Role] Work Sample

Open with one or two sentences explaining the role-relevant capabilities being assessed. State the total expected time.

**Your mission**

Describe a specific situation, not an abstract assignment. Include enough context to make the work realistic. If decisiveness is being assessed, state which stakeholders are unavailable during the exercise so candidates must make reasonable decisions rather than defer every call.

End with one sentence restating what the candidate will produce.

**Deliverables**

List two to four parts, with rough time guidance where useful. A common operations pattern is:

- A short prioritization or analysis section.
- Several actual drafts, decisions, or shipped outputs.
- One systemic fix, process improvement, or reusable artifact.

Avoid excessive micro-tasks. A few substantive outputs provide better evidence than dozens of shallow choices. If planning and execution both matter, explicitly tell candidates not to spend all their time planning.

**Context**

Provide the minimum information required to complete the task: project state, audience, constraints, available resources, relevant policies, and stakeholder availability. Use fictional names, domains, and identifiers unless the hiring owner has explicitly approved public information for use.

For a triage-pile exercise, include roughly eight to ten realistic items. Make some items connected, so candidates are rewarded for recognizing patterns across the whole situation. Provide reference notes containing any data needed to make fair decisions, such as capacity limits, escalation rules, or refund policy.

**Instructions**

Include:

- The expected time limit.
- A clear submission deadline.
- The submission format, such as one document or PDF, plus links to supplementary artifacts if needed.
- Payment amount, payment process, and any early-submission bonus.
- Permitted tools and AI assistance.
- A request to document important assumptions briefly.
- Permission to submit incomplete work if time runs out.
- Optional guidance on a short walkthrough video, if it would add useful evidence.
- A route to request an accommodation or alternative accessible format.

Use a transparent AI policy, such as:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

**Anticipated questions**

Include answers to common questions:

- If a requirement is unclear, make a reasonable assumption and state it briefly.
- If you do not finish in the expected time, submit what you have and explain what you would do next.
- The work will be used only to evaluate candidates unless another use is agreed separately.

After every draft, add a separate section that is not for candidates:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets on choices the owner may want to revise. For example:

- Whether a scenario item is too obvious to produce useful evidence.
- Whether the scenario is realistic enough without exposing internal information.
- Whether payment and an early-submission bonus match the role level and candidate time commitment.
- Whether a deliverable is too prescriptive or too vague.
- Whether an optional video adds signal worth the additional burden.

End with one focused decision question, such as: “Which part should we tighten first?”

## Candidate-facing format and language checks

Write in direct, plain language and use the locale chosen for the role. Ensure the exercise can be pasted cleanly into the organization’s selected hiring system.

Before sharing a draft, confirm that candidate-facing text:

- Uses simple headings and bullets.
- Has no tables if the destination system renders tables poorly.
- Avoids horizontal divider lines if they break the destination editor.
- Avoids generic slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.
- Uses clear phrases such as “by the end of [day]” rather than abbreviated wording.
- Uses clearly fictional email addresses and names for fictional scenario materials.
- Formats multi-line message metadata with the soft-break method supported by the destination system.
- Contains no credentials, private contact details, sensitive internal data, or unrelated personal information.

## Step 5: Iterate with the hiring owner

Expect multiple revision rounds. For each round, provide the complete updated work sample, not only a change list, so it can be copied into the selected system.

Apply feedback directly unless it would materially undermine validity, fairness, accessibility, or safety. If that happens, state the concern once in plain language, offer a practical alternative, and let the hiring owner decide.

Typical revisions include tightening vague instructions, loosening overly prescriptive tasks, correcting scenario facts, simplifying deliverables, changing payment, and replacing unrealistic details.

## Step 6: Simulate two submissions

Before declaring version 1 complete, simulate two full candidate submissions in parallel using the exact candidate-facing instructions.

### Role-aligned simulation

Use a persona aligned with the approved role-success profile. Have them complete the actual deliverables within the stated time limit, then add a short reflection on choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest and capable persona who might pass ordinary screening but whose work lacks one capability that is central to this role. Choose a mismatch tied to observable job evidence, such as planning without execution, excessive caution where judgment is needed, or rapid output without systemic awareness. Never base the distinction on identity, background, or protected characteristics.

Have this persona complete the same deliverables.

Then write a synthesis covering:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both submissions looked similar.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by likely impact.

Floor checks that both simulated candidates pass are not automatically bad. The concern is when a central capability produces no meaningful difference in evidence.

## Step 7: Apply validation improvements

Revise the full exercise based on the simulations. Fix the weakest diagnostic points first. Useful revisions may include:

- Making scenario items more connected.
- Removing obvious noise that takes seconds to dismiss.
- Adding a concrete constraint that requires a real tradeoff.
- Replacing a broad opinion question with a usable deliverable.
- Clarifying reviewer expectations so they reward the intended evidence.
- Removing specialized knowledge requirements that are trainable and not essential on day one.

Do not make the task harder merely to make it more selective. Make it more diagnostic of the confirmed role requirements.

## Step 8: Optional external review

If other reviewers give feedback, assess each suggestion against the approved alignment memo. State which suggestions to integrate, which to skip, and why. External review is evidence, not an automatic instruction; the hiring owner remains accountable for the assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The role description and role-success profile are confirmed.
- The alignment memo is approved.
- The chosen task shape maps directly to the load-bearing capabilities.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and does not require private access.
- Payment, deadline, submission, AI-use, and accommodation instructions are clear.
- A reviewer can assess a submission in about 20 to 25 minutes.
- Candidate-facing text works in the intended delivery system.
- A role-aligned and plausible role-misaligned simulation has been completed.
- Simulation findings led to necessary revisions.
- The final version does not expose sensitive data or create unpaid production work.
- Role-relevant criteria and potential proxy-bias risks have been checked.

## Common failure modes

Avoid these patterns:

- Designing the task before agreeing what it should measure.
- Testing tool familiarity, domain trivia, or trainable knowledge instead of durable judgment.
- Asking for too many small outputs instead of a few meaningful ones.
- Making every scenario item independent, which tests volume but not pattern recognition.
- Allowing candidates to defer every meaningful decision to an available stakeholder when decisiveness is intended to matter.
- Giving vague context that rewards insider knowledge.
- Setting word-count targets that encourage padding.
- Creating a test that takes longer to grade than the signal justifies.
- Treating polished writing or presentation as the main signal when the role requires something else.
- Declaring success without checking whether the exercise distinguishes relevant performance.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, respectful of candidate time, and clear about the evidence it is intended to produce.


---
name: run-a-reference-call
description: Prepare, conduct, and document a structured hiring reference call that produces role-relevant, privacy-respecting evidence for a fair hiring decision.
---

# Run a reference call

Use this workflow to prepare and document a reference conversation for a hiring decision. Its purpose is to gather specific, role-relevant evidence—not vague praise or a private biography—and to make the evidence usable by the hiring team.

Only access communications, calendars, applicant records, and prior reference notes when you have a legitimate hiring purpose and appropriate authorization. Use the minimum relevant information. Keep notes within the hiring team’s approved access boundary, omit unrelated personal or sensitive details, and respect any consent or confidentiality expectations set during the reference process.

## 1. Confirm the call and its purpose

Before researching, verify:

- Candidate name and the role under consideration.
- Referee name, contact details, and stated relationship to the candidate.
- Call date, time, joining details, and attendees.
- The hiring stage and the decision this reference can inform.
- Whether the candidate has authorized reference checking at this stage, if that is required by the organization’s process or local law.

If no calendar invitation exists, create a preparation record anyway and mark the call logistics as unconfirmed. Do not invent a meeting link, relationship, or hiring stage.

## 2. Gather only relevant context

Use approved hiring records and authorized internal sources to establish the context. Search the candidate’s application, interview materials, reference list, scheduling correspondence, and any prior approved interactions with the referee. Where permitted, use public professional information to confirm the referee’s current role and relevant background.

Capture:

- The role’s expected outcomes and the capabilities the call should assess.
- The candidate’s current hiring stage and unresolved role-relevant questions.
- How the referee knows the candidate: reporting line, working relationship, time period, proximity of observation, and type of work observed.
- Relevant candidate links or record locations, such as the approved applicant profile, professional profile, portfolio, or work samples.
- Other named referees, for coordination only.
- Previous completed reference findings, if access is authorized.

Do not search unrelated private communications, collect sensitive personal information, or include rumors. Treat a referee’s title, confidence, and personal affinity as weaker evidence than direct observation of relevant work.

## 3. Analyze the evidence before the call

Turn the research into a small number of questions that reduce the most important decision uncertainty. Identify what this referee is uniquely able to observe compared with other referees.

When prior references exist, distinguish:

- **Repeated pattern:** independently reported, concrete behavior across contexts.
- **Unconfirmed claim:** one person’s view that needs another specific example or a different perspective.
- **Contradiction:** accounts differ; ask about circumstances, scope, and evidence rather than choosing a side prematurely.
- **Information gap:** an important capability that no available referee can credibly assess.

Write direct, neutral prompts. For example: “A previous referee described strong early project momentum but inconsistent final handoff. What did you observe when this candidate closed complex work?” Do not reveal confidential interview comments, private ratings, or other referees’ identities unless your process permits it and doing so is necessary.

## 4. Create the reference-call record

Create a meeting page or record in the organization’s chosen hiring system before the call. Include the call date, candidate, referee, interviewer, secure joining information where appropriate, and access controls consistent with the hiring process.

Use this template:

## Context

- **Candidate:** [Name and approved profile link]
- **Role and stage:** [Role; current decision stage]
- **Referee:** [Name, role, organization or professional context]
- **Relationship:** [How they worked together, when, and how closely]
- **Call logistics:** [Date, time, format, interviewer]
- **Other references:** [Names or “not available”]
- **Relevant records:** [Approved applicant, portfolio, or work-sample links]

## Opening

> Thanks for making time to speak with me. We are considering [Candidate] for a [Role] position. I would like to understand the work you directly observed, the context for that work, and where they were most effective or needed support. Please share only information you are comfortable and authorized to discuss. We will use your input only for this hiring process and handle it within our hiring process confidentiality expectations.

Adapt this wording to the relationship and the organization’s policy. If there is a prior professional connection between the interviewer and referee, acknowledge it briefly where useful, but do not let it substitute for evidence.

## Briefing notes

- **Decision uncertainty:** [What this call should clarify]
- **What this referee can uniquely assess:** [Directly observed work or context]
- **Patterns to test:** [Prior evidence, framed without unnecessary attribution]
- **Open questions:** [Capability, delivery, collaboration, judgment, or environment fit]
- **Limits:** [What the referee may not have seen]

## Questions

- **How did you work together?** What were each of your roles, and how directly did you observe their work?
- **What did the candidate personally own or deliver?** What was the outcome, and what evidence shows their contribution?
- **What did strong performance look like in practice?** Please share a specific example.
- **Where did they need the most support or development?** What happened, and how did they respond?
- **How did they handle feedback, ambiguity, setbacks, or competing priorities?**
- **What conditions helped them do their best work, and what conditions made performance harder?**
- **If you were managing them in this role, what would you do to help them contribute effectively in the first few months?**
- **What role-relevant concern should we examine carefully before making a decision?**
- **What have I not asked that would help us evaluate their ability to perform this role?**

### Role-specific probes

Add three to five probes tied to the role’s real work. Examples include:

| Role area | Evidence-seeking probe |
|---|---|
| Operations | How did they build or improve a repeatable process while balancing speed, quality, and stakeholder needs? |
| Community or partnerships | How did they build trust, handle conflict, and follow through with different stakeholders? |
| Leadership | How did they set priorities, develop others, and make decisions when information was incomplete? |
| Technical or analytical work | How did they validate assumptions, communicate trade-offs, and translate analysis into useful action? |

## Notes and assessment

During the call, separate three layers:

- **Observed facts:** concrete examples, outcomes, scope, dates or timeframes where relevant.
- **Referee interpretation:** the referee’s explanation of strengths, limitations, or comparative judgment.
- **Hiring-team inference:** what the information may mean for this role, including uncertainty.

Record the referee’s observation limits. For example, a senior sponsor may be well placed to discuss outcomes and stakeholder trust but not daily execution. Avoid recording unnecessary personal details or making broad personality judgments.

## 5. Readiness gate before ending the call

Before closing, check that you have:

- Confirmed the relationship and observation period.
- Collected at least one concrete example of meaningful contribution.
- Asked about a development area or performance risk.
- Tested the most important role-specific uncertainty.
- Clarified any vague praise, rankings, or concerns with examples.
- Captured what the referee could and could not directly observe.

If a key answer remains vague, ask: “What did that look like in practice?” or “What specific result or behavior led you to that view?”

## 6. Complete the record and audit it

After the call, promptly complete the meeting record. Summarize evidence in concise bullets and identify follow-up actions, such as checking a claim with another referee or reviewing a work sample. Do not treat one reference as a final verdict.

Use this audit checklist:

- Are statements attributed to the referee, documented evidence, or clearly marked as the hiring team’s inference?
- Does each important conclusion connect to a role-relevant capability or outcome?
- Are conclusions proportionate to the referee’s direct knowledge?
- Have contradictory accounts been recorded fairly rather than resolved by assumption?
- Are sensitive, unrelated, or excessive personal details excluded?
- Is the record accessible only to authorized participants?

Common failure modes are generic question lists, accepting praise without examples, leading a referee toward a preferred conclusion, sharing confidential interview information, overweighting a prestigious referee, and leaving useful findings in private chat rather than the approved hiring record. The completed record—not informal recollection—is the durable output of the workflow.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account and privacy boundaries, verifying rendered state, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for browser-based work such as completing rendered forms, changing dashboard settings, collecting data from dynamic pages, testing a user flow, or working in an authenticated account. Use it when a supported direct interface, a simple page request, or static-page retrieval cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not perform a consequential final action until the account, target, page state, and authorization are clear.

A successful automation command does **not** prove that a website accepted a change. Modern applications may keep state separately from the visible page, save only on blur, replace controls during re-rendering, or report an error even after an action has completed. Treat page state and durable confirmation—not tool success—as evidence.

## 1. Confirm purpose, authority, and boundaries

Before accessing private communications, records, dashboards, or accounts, confirm that the task has a legitimate purpose and the requester has clear authority for both the access and the intended action.

Use the minimum relevant sources and information. Do not collect, retain, screenshot, summarize, or disclose unrelated personal information. Keep outputs within the requester’s appropriate access boundary. Do not expose passwords, session data, recovery details, authentication prompts, or security configuration.

Establish the task boundary before navigating deeply:

- What exact page, record, form, setting, or workflow is the target?
- What information must be entered, collected, changed, or uploaded?
- What is the minimum information needed to complete the task?
- Is the proposed action reversible?
- Does it send, publish, purchase, delete, grant access, alter billing, change a plan, or otherwise create an external commitment?
- Which choices need the user’s judgment?

Stop and ask before changing data if the target, authority, account, environment, intended audience, or final effect is unclear.

## 2. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported API or direct interface.** Prefer a documented and authorized programmatic interface when it can complete the task. It is often more reliable and auditable than reproducing browser interactions.
2. **Headless browser automation.** Use this for public pages, test environments, UI testing, screenshots, routine rendered-page extraction, and forms that do not need an established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when an existing session, single sign-on state, account-specific dashboard, or user-directed browser context is genuinely required.

Before driving a browser, check for an appropriate direct route: official documentation, ordinary form actions, page source, and visible network requests may reveal supported endpoints. Use only interfaces that the requester is authorized to use.

Do not use an undocumented endpoint to bypass access controls, consent boundaries, contractual restrictions, paywalls, or anti-abuse systems. Do not use an authenticated visible browser merely for convenience: it can interrupt the user’s work and increases privacy and account risk.

If a site blocks automation, do not evade that protection for research or routine collection. A verified visible session can be appropriate when the user explicitly requested a legitimate task on that specific site and the session is necessary to do it. Do not weaken browser security, warnings, multi-factor authentication, access restrictions, or bot protections.

## 3. Protect account identity and browser context

Before acting in an authenticated context, identify the correct account, organization, environment, and browser profile. Never infer identity from a generic browser name, remembered default, old tab title, or connection label.

Use these operating rules:

- Announce when taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly directs you to an existing page.
- Classify the context explicitly, such as personal, work, test, staging, or production.
- Select the matching profile or browser connection directly rather than relying on a generic or most-recent selector.
- Confirm the signed-in account through a reliable account indicator before opening or changing the real target.
- Confirm the environment and target object again before data-changing actions.
- Do not restart, close, or disrupt someone else’s active browser work without explicit approval.
- Do not mix personal and organizational contexts unless the user explicitly directs it and has authority to do so.

Use an account preflight gate before actions that modify data. Answer these questions with evidence: **Which account is this? Which environment is this? What exact item will change?** If the automation system has a verification marker or permission gate, set it only after the account check passes. Never enable it early merely to unlock controls.

## 4. Separate preparation from commitment

Filling fields, drafting text, selecting options, and gathering a preview are usually preparation. Submitting, sending, publishing, purchasing, deleting, granting access, or applying an account change is commitment.

For consequential tasks, use two phases:

1. **Preparation pass:** Configure the page, verify the relevant values, and capture a pre-action record. Do not activate the final control.
2. **Commitment pass:** Re-check account, target, authorization, and readiness. Perform the final action once, then verify the result.

Treat payments, external sends, deletes, plan or access changes, and actions labelled permanent, final, irreversible, or impossible to edit later as one-way actions. Capture the pre-action state and obtain explicit approval immediately before commitment unless clear standing authorization covers that exact final action.

For a reversible, low-risk change the user explicitly requested, proceed after ordinary verification unless the page presents an unexpected warning, a broader impact, or an unclear target.

If the page reloads, re-renders, times out, or the session changes between preparation and commitment, do not assume the earlier state remains valid. Inspect and verify again.

## 5. Inspect the rendered page before editing

Do not start by guessing selectors, filling controls by numeric position, or trusting a visual approximation. Inspect the rendered page first and identify the actual interactive controls.

For each relevant field, determine:

- Control type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Stable semantic identity: accessible name, visible label, placeholder, or explicit label relationship.
- Current value, required state, disabled state, and validation messages.
- Formatting rules, length limits, and whether line breaks or special characters are accepted.
- Whether the apparent field is an editable control, a wrapper, or a hidden synchronization element.
- Whether changing a selection, date, tab, or option causes a re-render.

Address controls by semantic identity, such as a visible label or accessible name. Avoid DOM indexes when labels are available: dynamic applications can change control order across loads and re-renders.

Before changing a record or setting, inspect its current state. This helps avoid modifying the wrong item or overwriting an existing value unintentionally.

### Generic inspection pattern

Use the chosen browser automation capability to list relevant controls before writing fill logic. Record at least the tag, input type, role, label, required state, and readable value or text length.

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

## 6. Use the interaction that matches the control

A generic “set value” operation is not reliable for every control. Use normal user-like interaction where framework-managed controls require it.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Enter text through the normal text-input mechanism | Line breaks can be removed silently. |
| Multiline text area | Fill text, then move focus away | Some applications save only on blur. |
| Rich-text or content-editable editor | Focus the true editor, select prior text, enter text through keyboard-style events, then blur | Direct page-property changes may not update the application model. |
| Dropdown or combobox | Open it, choose by visible option text, then wait for state to settle | Selection may re-render the form. |
| Checkbox or radio group | Read the current state first; change only if needed | A blind click can reverse a correct state. |
| Date/time picker | Set date and time, then verify the rendered summary | Popovers may clear, reinterpret, or alter related values. |
| File upload | Confirm file, destination, recipient, and privacy impact first | Uploading can begin immediately and may be hard to reverse. |

For framework-managed editors, avoid directly setting low-level DOM properties. A robust sequence is:

1. Focus the actual editable element.
2. Select and remove prior text if replacement is intended.
3. Enter the new text with keyboard-style input.
4. Move focus to a neutral page element to commit the change.
5. Wait briefly for the application to settle.
6. Read the value back from the rendered page or the application’s reliable state.

Some forms pair a visible editor with a hidden input. Editing the hidden input can appear successful in an inspection dump while server validation treats the visible editor as empty. Target the interactive control that the user would edit and that the application actually reads. If an accessibility locator finds an empty wrapper, inspect the underlying labelled editor.

If dropdowns, checkboxes, tabs, or dates can refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterward and confirm that previous entries remain present.

## 7. Verify every meaningful edit

After each field is filled or setting is changed, read it back from the rendered page. Compare the visible or accessible value with the intended value. For sensitive content, compare length, required state, or a minimal redacted summary rather than exposing full text unnecessarily.

Watch for these mismatches:

- Automation reports success but the field is empty.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displayed content but did not retain it internally.
- A later edit erased an earlier value after a re-render.
- A hidden synchronization field changed instead of the visible editor.
- A selection changed a dependent date, recipient, validation rule, or required field.

If verification fails, do not continue toward submission. Diagnose the control type, retry once with a more suitable method, and verify again. If the page still rejects or alters the value, report the limitation and ask how to proceed. Do not silently submit incorrect content.

## 8. Run a pre-submit readiness gate

Before any final submission or high-impact change, inspect the full relevant state again. Confirm all of the following:

- The correct account, organization, and environment are active.
- The target item is the intended one.
- Every required field is present and non-empty.
- Each entered value matches the intended content closely enough for the task.
- Recipients, dates, attachments, selected options, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially completed form is recoverable; an incorrect external action may not be.

Capture a pre-action record for consequential work: a screenshot, concise state summary, or structured field dump. Store and share it only through the appropriate access boundary. Avoid pasting large amounts of sensitive field content into chat when a short summary and securely available record are enough.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Recipients, dates, attachments, and dependent options were checked.
- [ ] A pre-action record exists for consequential work.
- [ ] The final action and its impact are understood.
- [ ] Required authorization for commitment is present.

## 9. Confirm completion without blind retries

A button click is not proof of success. After acting, seek durable evidence such as a success message, confirmation reference, newly created record, persisted setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, the evidence available, and what remains uncertain. Do not represent an attempted action as completed.

## 10. Common failures and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier values disappear after a later edit | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find the multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the underlying labelled control and target the true editor. |
| Validation says a field is empty although it looks filled | A hidden synchronization field was edited | Use the visible interactive control the application actually reads. |
| Automation is unstable on a complex page | The selected automation layer is unsuitable | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers differ | The site varies behavior by browser context | Prefer an authorized direct interface; if necessary for an explicit task, use a verified visible session without evading protections. |
| A popup unexpectedly changes dates or values | The widget has stateful close, clear, or parsing behavior | Close it with a neutral page action and re-verify all affected fields. |
| An error may be cosmetic | The action may already have completed | Inspect durable resulting state before retrying. |
| Account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
- [ ] Explicit approval was obtained before an irreversible or otherwise unapproved commitment.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, validating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing skill, evaluate whether it improves results, or improve when and how it activates. A skill is a focused set of instructions, with optional scripts, references, templates, and test material, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the intended job and its limits.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Review outputs with the user and apply objective checks where they are meaningful.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and not overfitted to a few examples.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the finished skill.

Do not assume every project needs every step. Some users want a quick collaborative draft; others need a rigorous comparison. Identify where the user is in the process and help them take the next useful step.

## Communication principles

Match the user’s technical experience and vocabulary. Use plain language by default. Terms such as *evaluation* and *benchmark* are often acceptable, but briefly define them if needed. Do not use terms such as “JSON,” “schema,” or “assertion” without explanation unless the user has signaled familiarity.

Explain why a question matters. For example:

> What should a successful result look like: a chat response, a structured report, a downloadable file, or an action in another system? This determines how the skill should validate completion.

Keep the user involved at meaningful decisions:

- Confirm the job before writing extensive instructions.
- Ask before choosing restrictive scope, required tools, or approval rules.
- Share proposed test prompts before relying on them.
- Let human judgment lead for subjective qualities such as writing quality, visual design, tone, or strategic usefulness.
- Be flexible when the user prefers an informal review rather than formal testing.

If the workflow involves private communications, organizational records, or information about people, use it only for a legitimate purpose and with clear authorization. Use the minimum relevant sources and information, omit unrelated sensitive details, respect consent and privacy expectations, and keep outputs within the appropriate access boundary.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea such as “I need a skill that prepares recurring project updates.” Start with discovery and a first draft.

### B. Existing draft or installed skill

The user already has instructions and wants them edited, simplified, tested, or optimized. Read the current instructions before proposing changes. Preserve the existing skill name and identity unless the user explicitly asks to rename it.

If the current copy cannot be edited directly, make a writable copy in a user-approved working location. Preserve the original unchanged. Package or export the revised copy only after the user has reviewed the result.

### C. A workflow demonstrated in the conversation

The user may say “turn what we just did into a skill.” Extract as much as possible from the conversation before asking questions:

- Inputs the user provided.
- Sources, tools, and capabilities used.
- The order of decisions and actions.
- Corrections or preferences the user gave.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow and list the gaps for confirmation. Do not silently treat a one-time workaround as a general rule.

### D. Evaluation or optimization request

The user may already have a finished-looking skill and want to know whether it helps. Go directly to test design, evaluation, and revision. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent and scope

Before drafting, gather enough information to define a coherent job. Adapt these questions to the situation rather than asking all of them mechanically.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Trigger:** What requests, wording, or contexts should activate it?
3. **Inputs:** What information, files, systems, examples, or approved sources can it use?
4. **Outputs:** What should it produce, change, or recommend? Is a format required?
5. **Success:** How will the user know the result is correct, useful, or complete?
6. **Boundaries:** What should the skill not do? When should it ask, pause, decline, or return work to the user?
7. **Variations:** What common cases, difficult cases, or exceptions materially change the work?
8. **Dependencies:** Does it require particular capabilities, references, templates, permissions, or deterministic helper scripts?
9. **Testing:** Should it be tested with realistic requests? Recommend testing for repeated, consequential, or objectively verifiable work, but let the user decide.

Useful choice questions include:

- “When information is missing, should the skill make a best-effort draft or stop and ask?”
- “Should the default output be concise, detailed, or selected by the user?”
- “May it use any available source, or only sources the user has explicitly approved?”
- “Which decisions require user confirmation before an external or irreversible action?”

### Research before drafting

If relevant documentation, comparable skills, approved reference material, or standards are available, review them before drafting. Research should reduce burden on the user, not replace the user’s authority over requirements.

Use research to identify:

- Existing conventions and output standards.
- Constraints of a relevant file format, tool, or system.
- Reusable patterns for comparable tasks.
- Safety, privacy, compliance, and approval requirements.

When research requires access to sensitive records, confirm legitimate purpose and authorization first. Use only sources needed for the requested result. If sources conflict or requirements remain unclear, present the uncertainty rather than guessing.

## 3. Choose the skill structure

Keep a skill focused enough that users and AI systems can predict what it does. One skill may support variants of the same job, but separate unrelated jobs that have different users, permissions, sources of truth, or definitions of completion.

A typical package can contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional documentation read when needed
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help decide whether the skill applies.
2. **Core instructions:** The workflow needed for most requests.
3. **Supporting resources:** Detailed references, templates, and scripts consulted only when relevant.

Keep the core instruction file readable. If it grows large, move domain-specific details into clearly named reference files and say exactly when to consult each one. Long references should include navigation or a table of contents.

For a skill with multiple supported environments or variants, keep a shared selection workflow in the core instructions and use separate references for each variant. The AI should read only the relevant reference rather than loading every variant by default.

### Use scripts for repeatable deterministic work

If test runs show that the AI repeatedly rebuilds the same helper procedure, consider bundling a script. Good candidates include file conversion, data validation, calculations, report assembly, and repeatable transformations.

A bundled script is worthwhile when it is:

- Deterministic or easier to verify than free-form reasoning.
- Reused across requests.
- Safer or less error-prone than repeated reconstruction.
- Within the user’s intended authorization boundary.

Document what the script does, its inputs, outputs, failure behavior, and when not to use it. Do not automate actions that the user would not reasonably expect from the skill description.

## 4. Write the skill

Draft the skill in clear, imperative language. Explain why important instructions exist, especially when they prevent predictable errors. AI systems usually handle variation better when they understand the goal and tradeoff than when they receive a long list of unexplained rigid rules.

Include the following sections when applicable.

### Purpose and scope

State the job, intended user, normal outcome, and boundaries. Make clear whether the skill produces advice, creates a file, changes a system, or guides a process.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State what happens when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If the source is unavailable, ask for an export or produce a draft clearly marked as incomplete.
```

### Workflow

Describe the normal sequence of actions and meaningful decision points:

1. Inspect the request and available inputs.
2. Confirm unclear requirements only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result, assumptions, and unresolved limitations.

Use conditional rules for important branches:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite important work or affect an external system, explain the impact and request confirmation before proceeding.
```

### Output format

When consistency matters, define an exact or near-exact structure.

```markdown
# [Title]

## Summary
[One short paragraph]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or required follow-up]
```

Avoid rigid templates where context-sensitive judgment matters more than uniform presentation. In those cases, give output goals and short examples instead.

### Quality, safety, and privacy checks

State the checks needed before completion. Depending on the task, these may include validating calculations, confirming required sections, retaining source references, preserving original data, checking that a produced file opens, or flagging uncertainty.

The skill must behave in ways a reasonable user would expect from its description. Do not include instructions that conceal actions, bypass authorization, extract unrelated confidential information, damage systems, mislead people, or enable unauthorized access.

For work involving records about people:

- Confirm a legitimate purpose and appropriate authorization.
- Use only the minimum relevant information and sources.
- Exclude unrelated personal or sensitive information from outputs.
- Respect consent, confidentiality, and access expectations.
- Keep conclusions tied to evidence and the requested decision.

For hiring, assessment, or review workflows, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Do not make unsupported inferences about a person beyond the evidence available.

### Failure behavior

Describe how to recover from common failures in general terms:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** Explain what could not be verified and offer a safe alternate method.
- **Ambiguous request:** Make a low-risk assumption only if it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, report the issue, or request guidance.
- **Permission-sensitive action:** Pause for confirmation before irreversible, external, or high-impact actions.

### Examples

Use a small number of generalized examples only when each teaches a distinct pattern. Examples should demonstrate the shape of good work, not replace reasoning with narrow imitation.

## 5. Write a strong description

The description is a routing instruction: it helps an AI decide when the skill applies. State both what the skill does and when it should be used.

Cover realistic user wording, including requests that imply the job without naming it. Descriptions should be specific enough to avoid capturing unrelated work, but broad enough to cover normal phrasings.

A useful pattern is:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a status update, leadership summary, progress report, milestone review, or a concise account of risks and next steps, even if they do not use the phrase “status report.”
```

Do not put the entire procedure in the description. Do not use vague labels such as “help with documents.” Keep scope limits that prevent costly or unsafe false activation.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description say when to activate it?
- Are required inputs, permissions, sources, and outputs clear?
- Does the workflow explain why important checks matter?
- Does it say what to do when information is missing?
- Are there unnecessary rules, repeated guidance, or brittle wording?
- Does it avoid relying on private habits, undeclared access, or a particular local environment?
- Does it give a capable AI enough freedom to handle normal variation?

Prefer lean, understandable instructions over a long prompt filled with rules that do not affect outcomes. Repeated absolute language is a warning sign unless the behavior is genuinely non-negotiable, such as an authorization or safety boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create two or three realistic test prompts. Share them with the user and invite additions or corrections before relying on them.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Any supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

A portable format is:

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

Cover meaningfully different conditions, such as:

- A typical successful request.
- A request with incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic edge condition that changes the workflow.
- A request that should require confirmation or a safe refusal, when relevant.

Do not make tests merely repeat the skill’s wording. Vary phrasing, detail, and user sophistication. Avoid retaining personal scenarios or sensitive data when a generalized equivalent can test the same behavior.

## 8. Run comparisons and preserve evidence

When independent runs are available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Save an unchanged snapshot before editing, then compare the revised version against the earlier version.

Start all comparable configurations under similar conditions. When parallel execution is available, launch skill and baseline runs for all test cases at the same time. This makes timing comparisons fairer and prevents a selectively altered baseline.

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

For each run, retain the prompt, supplied inputs, produced output, and available metadata such as elapsed time and resource use. Record timing as soon as the execution environment reports it because some environments do not preserve it afterward.

If independent execution is unavailable, conduct a transparent sanity check instead: follow the skill for each test prompt, save the results, and ask the user to review them. Do not represent this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While tests run, draft objective checks only where they help. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and valuable. Examples:

- Required sections are present.
- A produced file opens and contains the expected fields.
- Calculations match an approved source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- The output provides source references where required.

Record results with descriptive text, pass/fail status, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests follow-up information."
    }
  ]
}
```

Use scripts for programmatic checks when practical. They are faster, more repeatable, and reusable across iterations. Do not force numerical scoring onto subjective work such as aesthetic quality, tone, or strategic judgment; human review is more meaningful there.

## 10. Review results with a human

Present both outputs and measurements. Use an available review interface if it can display each test case, comparisons, grades, and feedback fields. If no interface is available, present accessible files or a clear conversation-based review.

For each test case, show:

- The original prompt and relevant supplied inputs.
- The skill output and comparison output, if available.
- Objective grades and evidence.
- Timing or resource data, if available.
- A way for the user to provide feedback.

Ask focused questions:

- Which result would you trust in normal use, and why?
- Did the skill add effort or detail that was not valuable?
- What was missing, misleading, or difficult to use?
- Would this work for a similar request with different wording or data?

If a review interface can export feedback, save that feedback with the iteration records. Empty feedback can mean a case is acceptable, but it is not proof that all cases are solved.

## 11. Analyze results beyond pass rates

Aggregate results when possible: pass rate, average time, average resource use, and variation. List the revised skill before its comparison condition so the report is easy to read.

Then analyze patterns that aggregate numbers can hide:

- **Non-discriminating checks:** Both configurations pass, so the check does not demonstrate the skill’s value.
- **High variation:** Comparable runs differ substantially, suggesting ambiguity or instability.
- **Tradeoffs:** Quality improves but time or resource use rises too much.
- **Failure concentration:** Several failures share a root cause, such as unclear source selection.
- **Unproductive work:** Execution traces show redundant planning, research, or formatting.
- **Repeated reconstruction:** Multiple runs independently recreate the same helper procedure, suggesting a bundled resource would help.

Use a small benchmark as evidence for the next revision, not as final proof of general reliability.

## 12. Improve without overfitting

Base revisions on user feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from complaints. If one output omits a source note, do not add a rule mentioning only that test. Instead clarify the broader behavior: when sources are incomplete or mixed, distinguish verified information from assumptions.

Use these improvement principles:

1. **Fix causes, not examples.** Design for future requests, not only current tests.
2. **Keep instructions lean.** Remove guidance that does not change behavior or creates wasted effort.
3. **Explain intent.** State why an action protects quality, usability, privacy, or safety.
4. **Add reusable assets only when justified.** Bundle scripts, templates, or references when repeated work proves their value.
5. **Preserve useful behavior.** Do not lose the aspects users already value.
6. **Expand coverage gradually.** Add a test only when it represents a genuine class of failure.

After revision, rerun the full test set in a new iteration. Use the same baseline policy unless a changed comparison is explicitly justified. Where possible, show new outputs beside prior outputs before collecting feedback.

Stop when the user is satisfied, feedback is consistently positive across meaningful cases, objective requirements are reliably met, further revisions are not meaningful, or remaining weaknesses require unavailable information or a product decision rather than better instructions.

## 13. Optional blind comparison

For a more rigorous comparison between two versions, use blind review. Give an independent evaluator two outputs without identifying their origins. Ask it to judge them against a shared rubric, and reveal the mapping only after the judgment is recorded.

Blind comparison is useful when two versions have similar measurements but different qualitative quality, when reviewers may favor a newer version, or when the decision is important.

Keep the rubric tied to user value: correctness, completeness, clarity, constraint adherence, safety, and practical usability. Analyze why one output won before editing again.

## 14. Optimize triggering behavior

Only optimize activation after the underlying workflow is useful.

Create a realistic set of trigger queries containing both cases that **should activate** the skill and nearby cases that **should not**. Include enough detail that consulting a skill would genuinely help.

Positive cases should vary in wording and context:

- Formal and casual phrasing.
- Direct requests and requests that imply the work.
- Common and less common valid uses.
- Cases where a related skill could compete but this one should be selected.

Negative cases should be difficult near-misses, not obviously irrelevant requests. They should share concepts with the skill but belong to another job, require a different capability, or lack necessary conditions.

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

Review the query set with the user before evaluating descriptions. If the environment supports repeated tests, separate the queries used to improve a description from held-out queries used to choose the final one. Choose the description that performs best on held-out cases rather than the one that merely fits the editing examples.

Simple one-step requests may not activate a specialized skill even when the description matches, because an AI can handle them directly. Use substantive trigger tests where the skill would provide real value.

Show the user the description before and after optimization and report the observed tradeoffs. Keep the final description honest about the skill’s scope.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not rely on private conventions, personal access, or undeclared tools.
- References and scripts are present, clearly named, and documented.
- No credentials, confidential material, personal identifiers, or sensitive examples are included.
- The user can install, access, or adapt the package in their chosen environment.
- Test material is retained only when it is safe and useful.

Provide a short handoff note stating what the skill does, required capabilities, known limitations, and how the user can test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an accurate description that routes appropriate requests, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.


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

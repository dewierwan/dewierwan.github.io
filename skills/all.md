# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a small ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The aim is not a long list of ideas; it is a set of meaningfully different paths, clear tradeoffs, and a small number of credible choices.

## 1. Gather relevant context

Start with the information supplied in the request. If the requester provides links, documents, discussion records, prior decisions, research, or other materials that you are authorized to access, review the minimum relevant material first.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the recommendation, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, deadlines, and budgets
- Stakeholder responsibilities and concerns
- Evidence about prior attempts, outcomes, or risks

Use targeted retrieval, not broad searching. Access private communications or records only for a legitimate purpose and with clear authorization. Include only information relevant to the decision; omit unrelated personal or sensitive details. If important context is unavailable, state the assumption or ask a focused question rather than inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the requester is actually making
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The initial wording may name a symptom or preferred solution rather than the real choice. For example, “Should we add a feature?” may actually mean “How can we reduce a recurring user problem within a limited budget?”

Ask the requester to confirm or correct the framing before generating a substantial option set. You may skip the pause when the framing is obvious, low-stakes, or the requester explicitly asks for an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not merely a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes process, incentives, scope, timing, or the problem framing
- At least one surprising option, such as delaying, partnering, reducing scope, observing longer, or doing nothing

Do not be contrarian merely to appear creative. A “do nothing” option is useful only when waiting, learning, or avoiding distraction is a real strategic choice.

Give every option a short, memorable label that communicates its core approach. Use this format:

| Option | What | Strengths | Weaknesses | Effort |
|---|---|---|---|---|
| **[Clear option label]** | [One or two sentences describing the approach.] | [One or two concrete advantages.] | [One or two candid disadvantages or failure risks.] | Low / Medium / High |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose evaluation criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, operational burden, and stakeholder impact. Add domain-specific criteria when they matter more than these defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they teach something useful, but clearly state why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not why it is generally attractive.
4. State the assumption most likely to change the ranking, if there is one.

Do not force a single winner unless the requester explicitly asks for one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the options and recommendations, wait for the requester. They may select an option, ask for detail, correct the framing, request additional options, or combine approaches.

If they propose a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once a path is selected, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record with the choice, decision owner, rationale, assumptions, boundaries, and review point.
- **Build-oriented choice:** After recording the decision, move to planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing addresses the actual decision rather than only the stated symptom.
- Options are genuinely distinct and not minor variants.
- At least one conventional and one meaningfully different path were considered when appropriate.
- Strengths and weaknesses are concrete, balanced, and candid.
- Effort labels are plausible for the requester’s context.
- Recommendations follow the stated criteria rather than unstated assistant preferences.
- Any retrieved private context was authorized, minimal, relevant, and kept within the appropriate access boundary.


---
name: pressure-test
description: Find the weak points in a leading strategic idea before committing. Steelman the case, test its load-bearing assumptions through sequential challenge, and finish with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or build the chosen approach.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportional to its consequences.
4. Plan, build, or execute the chosen approach.

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing a single idea too early often becomes an exercise in defending it.

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.

When using internal records, research, customer feedback, or communications, access them only for a legitimate decision-related purpose and with clear authorization. Use the minimum relevant material, omit unrelated sensitive personal details, and keep the output within the appropriate access boundary.

## Rules of engagement

- Be direct. Do not treat confidence as evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask **one forcing question at a time**. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before continuing.
- Use available evidence such as metrics, prior experiments, research, customer feedback, documented decisions, and stakeholder input. Separate facts, inferences, and forecasts.
- Refer to potential dissenters by relevant role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, with the most damaging first. Make assumptions observable where possible. Replace “users will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

| Rank | Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|---|
| 1 | [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Name the test] |

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Start with the highest-risk assumption and adapt later questions to the answers received. Do not present all questions as a questionnaire, because that enables selective answering.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence. Ask what observed behavior, comparison, data, or commitment supports the belief.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, usually 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failure, external conditions, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable signal] | [Check or accountable role] |

Warning signs must appear early enough to permit a course correction.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role’s strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap. Do not treat silence as agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test incomplete or failed rather than approving the idea.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next step:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data-collection period. Next: run that test, then decide with the result recorded. Do not commit while the named gap remains open.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

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

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and issuing a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make a clear decision with enough rigor, but not more than needed. The goal is to move forward, preserve the reasoning for meaningful choices, and learn from results without treating every outcome as proof that the original process was good or bad.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may recommend an option in conversation, clearly labeled as assistant analysis. Add that analysis to a decision record only if the user explicitly requests it.
4. **Record only with permission.** “Should we do X?” is a request for analysis, not a request to create or update a record. Log a decision only when the user asks to log, track, open, resume, or commit it, or has clearly agreed to a standing recording practice.
5. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution. Plan or start the task instead of opening a decision process.
6. **Protect privacy and access boundaries.** Before accessing shared communications, personnel records, customer information, or a shared register, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and facts.

For sensitive subjects, including health, relationships, compensation, confidential personnel matters, or private legal concerns, confirm that the intended record audience is appropriate. Offer a private record or keep the discussion in chat when a shared workspace is unsuitable.

## 1. Select the mode

Determine whether the user is starting, continuing, committing, or reviewing a decision.

| Mode | When to use it | Action |
|---|---|---|
| New | No relevant record exists, or the user wants a fresh decision | Frame and classify the decision |
| Resume | An open record exists and the user wants to continue thinking | Append new inputs and current stated position |
| Commit | An open decision exists and the user is ready to decide | Confirm readiness, then finalize and record |
| Review | A resolved decision has reached its review point | Compare actual outcomes with the original prediction |

If the user explicitly names a mode, follow that instruction. Otherwise, if authorized to access the chosen record system, look for overlapping decisions before creating a duplicate.

For a resume, retrieve the existing record and append to the history rather than rewriting it. For a review, use the original reasoning and prediction as the baseline; do not reconstruct them from memory.

## 2. Frame the decision

Write the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What deadline, trigger, or cost of delay applies?
- What result is desired?
- What happens if no action is taken?

If the question is broad and credible options do not yet exist, generate options before evaluating them. If there is only one viable path, say so directly:

> This appears to be a task rather than a decision. The next step is to plan or execute it.

## 3. Classify scope

Ask one clarifying question at a time when classification is unclear. Use the cost to unwind the choice, not just its apparent size.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default |
| Reversible | Moderate stakes and changeable within days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, trust loss, or opportunity cost if undone | Full analysis, challenge gate, stakeholder check, full record if authorized |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and required senior-stakeholder conversation |

Use this test when unsure: **What would it cost to unwind this?** Consider money, time, operational disruption, trust, opportunity cost, and reputational effects. If the cost cannot be stated quickly, or the answer is highly uncertain, the decision is probably larger than it first appears.

## 4. Apply the right rigor

### Trivial

Choose a reasonable default, state a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: continued attention may cost more than an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. Give each option one major strength, one major weakness, and a rough effort or cost estimate.
3. Recommend an option and name the decisive reason.
4. If uncertainty is material, identify the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid challenge examines:

- Important assumptions and evidence that would disconfirm them.
- Likely failure modes and a brief pre-mortem.
- The strongest alternative.
- Material stakeholder objections or constraints.
- Whether a smaller test, staged commitment, or reversible version is possible.

If no relevant pressure test has occurred in the active work context, stop the commitment flow and say:

> This decision is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not continue merely because the user is in a hurry. Proceed only after the challenge is complete or the user explicitly overrides it with a reason. If it exposes a serious unresolved failure, return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or affected stakeholder whose conversation is required before commitment.
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
- **Assistant analysis:** The recommendation and reasoning supplied by the active assistant.
- **Open question:** An uncertainty not yet resolved.

If the user has not expressed a position, write “No position stated yet” or leave their position blank. Never invent a lean, confidence level, response to dissent, rationale, or final decision for the user.

## 6. Commit and record

Before finalizing, confirm:

- What is the decision?
- Which option was chosen?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable outcome is predicted?
- What is the user’s confidence in that prediction?

For meaningful decisions, make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Use the user’s chosen document system, decision register, or private file. A useful record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. For a non-binary question, mark it resolved when a direction has been chosen.

Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar, task system, or other reminder for high-stakes reviews.

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

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until the user commits. When resuming, append a new dated thinking-log entry rather than overwriting history.

## 7. Review the outcome

At the review point, assess four separate questions:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle that could improve a future decision.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not collapse a bad outcome into a bad decision process, or a good outcome into a sound process.

## Completion check and message

Before closing the workflow, audit the decision:

- Is the scope classification plausible given the unwind cost?
- Was the appropriate challenge gate completed or explicitly overridden?
- Were relevant stakeholders consulted, or was the omission acknowledged?
- Is assistant advice clearly separate from the user’s stated view?
- Does any record contain only authorized, relevant information?
- Is the next action owned and dated?
- Is there a testable prediction and a review trigger for meaningful choices?

Then summarize clearly:

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

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the solution is not already clear. Do not use it for a small fix or routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the first proposed solution. If the request is to “build X,” work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the situation meaningfully better?
- What constraints, compatibility needs, or access boundaries apply?

Write a concise problem statement and descriptive requirements. Describe the intended outcome and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so directly.

Ask only for information that cannot be found in authorized, relevant context. When reviewing private communications, records, or data about people, confirm a legitimate purpose and clear authorization; use the minimum relevant sources and omit unrelated or sensitive personal details.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, and available alternatives. Include **do nothing**, defer, or improving the current workaround as genuine options when appropriate.

Distinguish between:

- **Reversible decisions:** Small choices that are inexpensive to change. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, migrations, long-lived configuration, security boundaries, external contracts, and vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the decision has lasting consequences.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read the relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before inventing new ones.

Understand constraints such as deployment practices, supported environments, ownership boundaries, security expectations, monitoring, and maintenance capacity. Use the system’s existing conventions unless there is a strong reason to change them.

## 4. Define evaluation criteria

Define lightweight, explicit criteria before generating solutions. For example:

- Must preserve existing authentication, privacy, and data behavior.
- Must be feasible within the available time and maintenance capacity.
- Should avoid unnecessary dependencies, configuration, and persistent commitments.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For especially ambiguous problems, generate a wider set of candidates before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that behave differently by runtime condition.
- Use strict validation and fail fast for invalid states. Do not silently turn programmer errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Make clean changes at the appropriate design boundary; avoid quick fixes that create hidden maintenance cost.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep proposals direct and short. Store the proposal in the user’s chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear date-prefixed title, such as `DD MMM YYYY: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership. Keep the plan where reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, and failure behavior.

Do not claim success based only on implementation. State what was tested, what passed, and what remains unverified. Commit, publish, or deploy changes only according to the user’s repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and its results.
- Known limitations, risks, and deferred work.
- Required user action, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

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
description: Learn a paper, article, post, or topic through a short Socratic dialogue that builds recall, reasoning, retention, and practical application instead of relying on passive summary.
---

# Learn with a tutor

Help a learner understand, retain, evaluate, and use a provided paper, article, post, or topic through an active dialogue. Prioritize retrieval, explanation, and application over delivering information. The learner should do most of the intellectual work; the tutor should guide, diagnose, and increase challenge at an appropriate pace.

## Operating principles

- **Retrieve before review.** Do not provide an unsolicited summary. First ask the learner to reconstruct ideas in their own words.
- **Seek mechanisms, not slogans.** Ask why, how, under what conditions, and on what evidence a claim works.
- **Require generation.** Have the learner create examples, analogies, predictions, counterexamples, and applications before offering your own.
- **Use productive difficulty.** The learner should need to think, but still have enough foundation to make a meaningful attempt.
- **Practice transfer.** Move from the source material to unfamiliar cases, adjacent concepts, and real decisions.
- **Reveal gaps through inquiry.** When an answer is incomplete or inconsistent, use focused questions to expose the tension. Explain directly only after a fair attempt.
- **Go deep selectively.** Prefer two or three central ideas explored well over broad, shallow coverage.

## Readiness gate

Before beginning substantive instruction, establish what material is available and what the learner needs.

| Check | What to ask or do |
|---|---|
| Source access | Confirm whether the learner has read the material, has an excerpt, or wants to learn a general topic. |
| Goal | Identify whether they want to explain an argument, prepare for a discussion, assess a claim, solve a problem, or apply a method. |
| Starting point | Ask what they already know, believe, or have experienced related to the topic. |
| Scope | Agree on a small learning target rather than attempting every detail. |

If the learner has not engaged with the source, do not pretend they can retrieve it. Ask for a prediction or prior model, direct them to inspect a relevant portion, then return to recall-based questions.

## Conversation workflow

### 1. Activate prior knowledge

Start with one or two open questions:

- “What do you already think is true about this topic, and what led you to that view?”
- “What are you hoping to be able to explain, evaluate, or do by the end?”
- “Before reading this, what would you have predicted?”

Use the response to estimate background knowledge, likely misconceptions, and a suitable challenge level.

### 2. Elicit the central idea from memory

Ask the learner to explain the main claim, finding, or argument without quoting the material.

Useful prompts:

- “In your own words, what is the main claim?”
- “What problem is this idea trying to solve?”
- “Why should someone believe this conclusion?”
- “How would you explain it to a thoughtful friend in 30 seconds?”

If they merely repeat wording from the source, ask them to restate it using a concrete example or causal explanation.

### 3. Choose the key ideas

Select two or three ideas that are central, difficult, consequential, or easy to misunderstand. For each idea, run a short learning cycle:

1. Ask the learner to reconstruct the idea.
2. Probe assumptions, evidence, mechanisms, and causal steps.
3. Ask for a self-generated example, analogy, or application.
4. Test the idea with an objection, boundary case, or alternative explanation.
5. Adjust the next question according to the learner’s answer.

Ask only one or two questions at a time. Let each answer determine the next move; do not run a fixed quiz script.

## Question toolkit

Choose prompts that require explanation rather than recognition.

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What is the mechanism, step by step?”
- “What evidence would distinguish this explanation from a competing one?”
- “Can you make a concrete example from a familiar setting?”
- “Where might this fail or cease to apply?”
- “What is the strongest objection to this argument?”
- “How does this connect with another idea you know?”
- “What surprised you, and what did you expect instead?”
- “If one assumption changed, how would the conclusion change?”
- “What prediction does this idea make in a new situation?”

Avoid questions that can be answered with only yes or no. If a binary choice is useful, require the learner to defend the choice.

## Response rules

Be warm, direct, and specific. Avoid generic praise. When an answer is strong, identify what made it strong—such as naming an assumption, distinguishing correlation from causation, or supplying a relevant counterexample—then raise the difficulty.

When an answer is wrong or incomplete:

1. Do not immediately state the correction.
2. Ask a focused question that reveals the conflict or missing distinction.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, provide a brief, clear explanation.
5. Ask them to restate the corrected idea or apply it to a new case.

When the learner says, “I don’t know,” invite a low-stakes attempt: “Take a guess based on what you do know. What seems most plausible, and why?” Give a hint after an attempt, or sooner when the task clearly requires missing prerequisite knowledge.

Do not define jargon automatically. First ask what the learner thinks the term means and how it functions in the argument. Clarify concisely if needed.

## Calibration rules

| Learner signal | Tutor response |
|---|---|
| Answers are quick and accurate | Increase difficulty with a counterexample, comparison, prediction, or transfer task. |
| Explanation is vague | Ask for a mechanism, concrete example, or distinction between related concepts. |
| Learner is confidently mistaken | Ask a question that tests the implication of their view before correcting it. |
| Learner is stuck | Narrow the task, isolate one assumption, use a simpler case, or offer a small hint. |
| Learner is tired or overloaded | Consolidate demonstrated learning and reduce scope rather than introducing another major idea. |

Maintain a demanding but collaborative tone. The goal is a dialogue with a thoughtful colleague, not a performance test.

## Progress checks and audit

Periodically give a short, evidence-based status update. Distinguish demonstrated understanding from familiarity with terms.

| Area | Evidence to look for |
|---|---|
| Recall | The learner can state the central idea without relying on source wording. |
| Explanation | The learner can describe why the claim follows and identify its mechanism or assumptions. |
| Evaluation | The learner can name evidence, objections, limitations, or alternative explanations. |
| Transfer | The learner can apply the idea accurately to a new case or decision. |
| Remaining work | The learner can identify a specific uncertainty, confusion, or question worth revisiting. |

A useful progress check is: “You have shown that you can explain [demonstrated capability]. The uncertain part is [specific gap]. The best next step is [focused retrieval or application task].”

Do not declare mastery because the learner recognizes vocabulary or repeats a conclusion. Look for accurate explanation, reasoning, and transfer.

## Closing gate

Before ending, convert understanding into action. Ask:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then request one final retrieval task, such as a concise explanation, a self-written study prompt, or an application to a fresh example. End by naming the next question or concept that would be most valuable to revisit.

## Guardrails

- Do not summarize material unless the learner explicitly requests it; even then, invite their own summary first.
- Do not lecture when a well-chosen question can prompt retrieval or inference.
- Do not make the task easy merely to sound encouraging.
- Do not cover an entire source superficially when a few core ideas can be learned deeply.
- Keep tutor turns short and aim for substantially more learner reasoning than tutor exposition.
- Adapt examples and applications to the learner’s stated context without assuming personal details.


---
name: write-in-my-voice
description: Draft or revise email in the user’s recognizable voice using approved style evidence, accurate information, and a concise, recipient-appropriate structure.
---

# Write in my voice

Use this workflow when drafting, replying to, or polishing an email on the user’s behalf.

## Goal

Create a copy-ready email that sounds recognizably like the user while remaining accurate, appropriate for the recipient, and clear about what happens next. Match the user’s established writing habits without treating a style preference as a rigid rule in situations with different stakes or audiences.

## 1. Gather authorized voice evidence

Before drafting, review the user’s current writing guide in full, if available. You may also review recent messages the user actually sent when there is a legitimate purpose and clear authorization to access them.

Use only the minimum relevant examples. Do not expose unrelated message content, personal details, sensitive information, or private records in the output. Keep drafts within the user’s appropriate access and sharing boundary.

Build a practical voice profile from the evidence:

- Typical greetings and sign-offs.
- Formality, warmth, directness, and relationship cues.
- Average sentence and paragraph length.
- Preferred vocabulary, contractions, punctuation, and formatting.
- Common ways of making requests, following up, declining, apologizing, correcting, or expressing uncertainty.
- Words, phrases, tones, punctuation, or formatting the user avoids.
- Approved facts, reusable links, standard responses, and boilerplate.

Give greater weight to recent sent messages and examples similar to the current recipient and purpose. If examples conflict, use the most recent consistent pattern or ask the user which preference is current.

## 2. Confirm the email brief

Identify the minimum information needed to write safely. Ask focused questions only when an unknown detail could materially change the message.

| Needed information | Example prompt |
|---|---|
| Recipient and relationship | “Who is this going to, and how do you know them?” |
| Intended result | “What should they do or understand after reading this?” |
| Required details | “What dates, links, files, decisions, or names must be included?” |
| Tone and stakes | “Should this be warm, firm, neutral, or more formal?” |
| Constraints | “Is there a deadline, approval requirement, or sensitive context?” |

Never invent facts, availability, prices, links, decisions, commitments, attachments, opinions, or emotional reactions. Do not imply approval, authority, or agreement that the user did not provide.

## 3. Adapt the voice to the situation

Preserve the user’s recognizable voice, but adjust the level of formality and context for the recipient and stakes.

- **Close colleagues or familiar contacts:** Use the user’s normal shorthand and concise rhythm when appropriate.
- **New, external, senior, or formal recipients:** Keep the user’s style, but make context, requests, and references easier to understand.
- **Sensitive, corrective, or conflict-related messages:** Be direct, factual, and respectful. Avoid defensive explanations, exaggerated praise, and unnecessary apologies.
- **Requests and coordination:** State the needed action, responsible person, and timing plainly.
- **Reusable material:** Use approved standard wording, links, or facts only when they are current and fit the situation. Do not reuse boilerplate in a misleading way.

## 4. Draft the smallest complete email

Use a structure that helps the recipient understand and act:

1. Greeting, if consistent with the user’s normal practice.
2. Purpose, answer, or decision early in the message.
3. Essential context, request, or next step.
4. Closing and sign-off, if appropriate.

Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Put decisions and requested actions where they are easy to find. Use bullets only when they improve clarity for multiple actions, options, or logistics.

Remove anything that does not help the recipient:

- Process narration or explanations of how the draft was produced.
- Generic praise, repeated thanks, or empty pleasantries.
- Filler such as “just wanted to” unless it is both authentic to the user and useful.
- Hedging that weakens a message when the user’s intent is clear.
- Extra context that could create confusion or disclose information unnecessarily.

## 5. Audit before presenting

Review the draft line by line:

- Would the user plausibly write these words?
- Do the greeting, sign-off, rhythm, and punctuation fit the available evidence?
- Is the tone appropriate for this recipient and situation?
- Are names, dates, links, attachments, and references accurate?
- Did the draft add any claim, promise, opinion, emotion, or commitment not supplied by the user?
- Is the requested action and timing clear?
- Is sensitive information limited to what the recipient legitimately needs?
- Can any sentence be removed without losing meaning or usefulness?
- Does the email avoid the user’s identified style anti-patterns?

## Readiness gate

Present a final draft only when all of the following are true:

- The recipient and purpose are clear.
- Material facts and commitments are confirmed or safely omitted.
- The tone matches both the user’s voice and the context.
- The next step is clear when one is needed.
- The message contains no unnecessary private or sensitive detail.

If a required detail is missing, ask one concise, specific question rather than guessing.

## Default when no voice evidence exists

Say briefly that you are using a default voice, then draft in a clear, warm-professional, concise, and direct style. Invite the user to provide a style guide or a few authorized examples of sent messages for better future matching.

## Output format

Provide the final email as copy-ready text. If clarification is necessary, ask only the specific question needed to proceed. Do not add rationale, alternatives, or commentary after the final draft unless the user requests them.


---
name: professional-social-post
description: Draft, revise, and audit professional social posts from notes, drafts, articles, transcripts, research, or a topic. This workflow helps create specific, useful, evidence-grounded posts with strong hooks, clear structure, and focused calls.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a rough draft, an article, a transcript, a podcast, a research finding, an announcement, or a simple topic.

The goal is not to make an announcement sound enthusiastic. The goal is to make the right reader stop, understand a useful point, and have a reason to care. The post should sound like a person with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, a generic motivational message, or an empty teaser.

This is platform-independent. Adapt the final formatting, length, link placement, and publication process to the user’s chosen platform.

## Start with context and authorization

Before drafting, gather or confirm the minimum information needed:

- **Platform and format:** text post, caption, document carousel, thread, short-form post, or article promotion.
- **Audience:** for example, practitioners, founders, researchers, policy professionals, customers, partners, or job candidates.
- **Purpose:** share an insight, explain a concept, announce something, promote a longer piece, invite substantive discussion, or support a campaign.
- **Voice:** first-person, organizational, formal, conversational, technical, plain-language, or another approved style.
- **Constraints:** word or character limit, required facts, forbidden phrases, punctuation preferences, accessibility requirements, and preferred closing style.
- **Link strategy:** whether a link is needed and where it should appear under the platform’s current norms.
- **Source status:** whether claims, data, quotations, names, and outcomes have been approved or can be publicly shared.

If the user provides a writing guide, approved prior posts, brand guidance, or audience research, use it as the primary source for voice and positioning. Do not assume an individual’s personal writing style or a particular publishing system.

If the request involves private communications, participant records, employee records, customer stories, or career outcomes, require a legitimate purpose and clear authorization. Use only the minimum relevant material. Omit unrelated personal details, sensitive information, and identifiable details that are not necessary to make the point. Confirm what may be named, quoted, or disclosed.

## Route the request before drafting

Some post types need distinct handling. Identify the genre before selecting a hook or structure.

- **Career or participant case study:** A person’s starting point, turning point, and outcome. Obtain permission before sharing identifying information or quotations. Use a case-study sequence: starting point, relevant action or mechanism, concrete outcome, evidence, and lesson.
- **Research or evidence post:** A claim based on data, a model, a report, or analysis. Prioritize methodology, scope, uncertainty, and a defensible interpretation.
- **Product, program, or organizational announcement:** Lead with the concrete change and reader relevance. Do not lead with internal excitement.
- **Article, report, or podcast promotion:** Lead with the strongest finding or tension in the longer piece, not with “a new article is out.”
- **Carousel or document caption:** Give one or two substantive findings, then explain what the visual material adds. Do not reproduce every slide.
- **Strategy or positioning post:** Explain a deliberate trade-off, including what the organization or team has chosen not to optimize for and why.

If the genre is unclear, ask one concise routing question. For example:

> Is this mainly an evidence post, an announcement, a case study, or promotion for a longer piece? The answer changes the strongest structure.

## Non-negotiable accuracy and safety rules

1. **Do not invent facts.** Never fabricate statistics, names, quotations, roles, organizations, dates, outcomes, testimonials, research findings, or customer results.
2. **Separate evidence from interpretation.** State what the source shows, then make clear when a conclusion is an inference, recommendation, or personal view.
3. **Preserve material uncertainty.** If results have broad ranges, weak evidence, important assumptions, or correlation rather than causation, say so plainly.
4. **Use specific details only when supported.** Exact figures, dates, roles, and outcomes can make a post stronger. Do not convert an estimate into falsely precise language.
5. **Ask for missing evidence early.** If a post relies on an unsupported claim, request a source, remove the claim, or narrow it.
6. **Avoid misleading urgency.** Do not exaggerate risks or stakes to create engagement. Name the specific risk, mechanism, uncertainty, and practical response.
7. **Respect the access boundary.** Do not reveal information that the intended audience is not authorized or expected to receive.

## Audience and voice

Write for the reader most likely to benefit from or act on the post, not for everyone who might vaguely relate to it. Specificity is a useful filter. It helps the right audience recognize that the post is for them.

Use this broadly useful default voice unless the user provides another:

- Direct, clear, and conversational.
- Short sentences and concrete nouns.
- Active voice where possible.
- One main claim per sentence.
- Specific rather than promotional.
- Sober about problems and practical about responses.
- Confident only where the evidence supports confidence.
- Technical terms only when useful, with a plain-English gloss on first use.

Avoid these three common failure modes:

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are thrilled to announce an exciting new initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences with unexplained terminology. | State the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Broad catastrophe language without a clear mechanism or response. | Name the specific risk, evidence, uncertainty, and useful intervention. |

## Core workflow

### 1. Inspect the source before choosing a format

Do not begin with a template. Read the source and find the strongest material inside it. A report title or article headline is often not the best social-post angle. The strongest thread may be a specific detail in the middle.

Look for:

- An unusual or surprising fact.
- A specific number that creates tension.
- A counterintuitive conclusion that can be defended.
- A concrete before-and-after result.
- A meaningful strategic trade-off.
- A sharp disagreement between credible views.
- A useful framework, checklist, or model.
- A sentence that changes how the reader sees a problem.

If several angles are plausible, do not silently choose one. Present two to four numbered options and let the user choose when the choice is material.

**Angle-selection prompt:**

> I see several viable angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [specific story or outcome]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Choose one primary thread. A post is not a summary of every section in the source.

### 2. Generate hooks before drafting the body

The opening determines whether the rest of the post is read. Generate five to ten possibilities, then show a shortlist of three to five strong hooks when user input would help. Do not commit to the first acceptable hook.

A hook should make an honest promise that the body fulfills. It should work on its own, without requiring the reader to understand the complete source.

Useful hook patterns include:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific evidence base] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Specific outcome:** “[Role or participant] moved from [starting point] to [outcome] in [timeframe].” Use only with evidence and permission.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only when the post supports the claim.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused disagreement:** “Why do two credible groups reach such different conclusions about [specific issue]?”

For each shortlisted hook, add a brief strategic note.

| Hook | Strategic purpose |
|---|---|
| “[Specific finding or claim].” | Leads with a concrete result and creates a clear reason to continue. |

Use the **swap test**: if a key noun could be replaced with an unrelated topic and the hook still works, it is probably too generic. Make the opening specific to the actual subject.

Avoid:

- “Excited to share,” “thrilled to announce,” or similar internal-excitement framing.
- Throat-clearing such as “In today’s fast-moving environment.”
- Empty cliffhangers that do not deliver a payoff.
- Several rhetorical questions in a row.
- Broad motivational statements with no mechanism, result, or decision.
- Clickbait such as “You will not believe” or “This changes everything.”

### 3. Choose one structure

Select the structure that matches the source. Do not combine several structures unless there is a clear reason.

1. **Counterintuitive claim → evidence → implication**  
   Best for research, data, and argument posts. Start with the surprise, show supporting facts, then explain what the reader should reconsider or do.

2. **Changed mind → trigger → updated view → takeaway**  
   Best for thoughtful first-person posts. State the previous view, explain what changed it, then give the new conclusion.

3. **Problem → why it matters → practical response**  
   Best for explainers and operational or policy content. Keep both the problem and response concrete.

4. **Result → how it happened → reusable lesson**  
   Best for launches, team outcomes, and approved case studies. The result must be real and specific.

5. **Framework → examples → application**  
   Best for material readers may save and revisit. Use a name for the framework only if the name clarifies rather than brands ordinary advice.

6. **Specific announcement → reader relevance → next step**  
   Use only when the announcement itself is genuinely notable. Lead with what happened and its practical significance.

7. **Strategic trade-off → rationale → consequence**  
   Useful for explaining deliberate constraints or anti-goals: what a team has chosen not to optimize for, why, and what this enables.

### 4. Draft: hook, tension, payoff

Use this default shape:

- **Hook:** the strongest claim, result, or tension.
- **Tension or setup:** why it matters, what is surprising, or which assumption it challenges.
- **Payoff:** evidence, story, framework, or practical insight. The post must provide value even if the reader does not click, swipe, or buy.
- **Soft close:** exactly one focused question, one practical takeaway, or one clear pointer to more material.

A useful default is under 300 words, but substance and platform norms should govern. Longer posts need a reason for every paragraph.

Use white space. One- or two-sentence paragraphs are easier to scan on a phone. Use bullets only when the content is genuinely list-shaped, such as three reasons, four findings, or a checklist. Do not turn flowing prose into bullets merely to look structured.

For a carousel or document caption:

- Establish the central idea in the post.
- Include one or two of the strongest specifics.
- State what the visual material adds.
- Do not write a slide-by-slide summary.

For an article, report, or podcast:

- Put the strongest finding in the body.
- Treat the longer piece as depth, evidence, and extended analysis.
- Follow the user’s chosen platform strategy for links.
- Never make “read the link” the main value proposition.

## Calls to action and questions

Use one close only. A strong close gives readers a real, bounded way to respond.

Examples of useful closes:

- “Which of these constraints matters most in your work?”
- “What evidence would change your view?”
- “The full analysis includes assumptions and source material.”
- “If you have operated a similar system, where does this model fail?”

Avoid weak or manipulative closes:

- “Thoughts?”
- “Let me know what you think.”
- Several questions at once.
- Requests to comment, tag, repost, or react solely to increase reach.

A question should invite knowledge, disagreement, or experience. Do not use engagement bait.

## Editing pass: remove templated language

Run a separate editing pass after drafting. Cut phrases that sound polished but say little.

Replace or remove:

- Corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Hedging frames such as “it is worth noting,” “one might say,” and “arguably,” unless uncertainty is genuinely important.
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Abstract nouns such as “journey,” “transformation,” and “paradigm” when a concrete event can be named.
- Transition sentences that only restate the previous paragraph.
- Dramatic frames such as “The truth is” and “Here is the reality.” State the point directly.
- Decorative punctuation or formatting that the platform will not render correctly.

Follow user-specified punctuation preferences. Otherwise, favor periods, commas, and line breaks over theatrical punctuation. Read the draft aloud. If it sounds like a generic thought-leadership template rather than a person making a specific point, rewrite it.

Use visual emphasis sparingly. Before using special characters, bold styling, or emoji, verify that the chosen platform renders them reliably and that they improve scanning rather than decorate the prose.

## Revision protocol

When the user gives feedback, revise the requested line and nearby logic first. Do not rewrite the entire post unless asked.

- If the hook is not sharp enough, provide several replacement hooks before changing the body.
- If a claim feels overstated, tighten the evidence or soften only that claim.
- If a paragraph feels slow, cut setup before adding explanation.
- If the user prefers an earlier sentence, preserve it unless there is a clear reason not to.
- If a draft has a weak spot, identify it honestly and offer a concrete alternative.

Multiple small options are often more useful than one full redraft, especially for hooks, closers, and uncertain lines.

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
- Are names, quotations, figures, and personal details supported, approved, and appropriate for this audience?
- Does the formatting work on the intended platform and device?
- Does the tone remain professional, respectful, and non-inflammatory for the intended audience?
- Does the post stay within its authorized information boundary?

If any answer is no, revise before handoff.

## Handoff format

Present only what helps the user decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen delivery format.
3. Any unsupported claim, missing input, or uncertain line.
4. Suggested link or first-comment text, if relevant to the platform strategy.
5. One concise publishing reminder, such as responding promptly and substantively to genuine comments.

Do not claim that a particular format, timing tactic, or engagement metric is guaranteed to improve reach. Platform behavior changes. Treat distribution advice as a testable hypothesis and compare results across several posts.

## Common failure patterns

- **Announcement disguised as content:** The post says the organization is pleased, but not why readers should care. Lead with the actual change or lesson.
- **Pure teaser:** The post asks readers to click but shares no useful insight. Give the main finding and use the linked piece for depth.
- **Unsupported precision:** A striking number has no source, scope, or caveat. Verify, qualify, or remove it.
- **Generic inspiration:** The post sounds positive but has no mechanism, example, or decision. Name the concrete action or trade-off.
- **Overpacked summary:** The post covers every section of a report. Select one thread and save the rest for the source or later posts.
- **Bolted-on promotion:** A product, program, or service appears at the end without a natural connection. Remove it, make a separate post, or make the connection immediate and concrete.
- **Forced engagement:** The post demands reactions or comments. Ask one real question or end with a useful conclusion.
- **Unapproved personal disclosure:** The post turns an individual’s experience into promotional evidence without clear permission. Generalize, anonymize, or obtain approval.

The final standard is simple: make a specific, useful, defensible point for a defined audience. Every sentence should earn its place.


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
description: Close one month honestly, then create a small, capacity-checked, explicitly approved plan for the next month using evidence, trade-offs, and concrete commitments.
---

# Review and plan a month

Use this workflow at a month boundary to review the month ending and build an executable plan for the month ahead. A complete session usually takes 45–75 minutes: roughly half for evidence and review, and roughly half for planning.

Review and planning belong in one session. The structural cause of a missed commitment, energy drain, or delivery problem should directly shape the structure of the next plan.

## Purpose

This workflow produces:

- An evidence-based account of what happened during the review month.
- A direct verdict on progress toward active long-range goals and any in-scope personal commitment.
- A concise month-level picture of selected work, energy, recovery, and delivery signals.
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

Ask whether the user means calendar months or a practical planning range that includes an overlapping partial week. Record the actual planning range in the finished plan.

## Privacy, authorization, and access boundaries

If this workflow uses connected records, calendars, journals, health data, task systems, project records, or communications:

- Confirm there is a legitimate planning purpose and clear authorization to access the source.
- Use the minimum relevant sources, fields, date range, and personal information.
- Do not retrieve or repeat unrelated journal entries, private messages, sensitive health details, or information about other people that is not needed for the plan.
- Keep summaries within the user’s access boundary. Do not expose private calendar details, names, or sensitive context in a record that has a wider audience.
- If data access is unavailable or authorization is unclear, ask the user for a short factual inventory instead. Never imply that unavailable data was checked.

## Operating rules

1. **Read first; discuss second.** Show the evidence picture before asking reflective questions.
2. **Batch independent reads.** If connected sources exist, gather independent evidence in one initial pass. Do not interrupt the conversation with repeated small lookups.
3. **Use current commitments.** Assess against the user’s live target, not an old schedule, obsolete project scope, or stale goal record.
4. **Check data quality before a harsh verdict.** Missing syncs, incomplete logs, delayed updates, and inconsistent sources may distort results. Ask the user to confirm surprising findings.
5. **The user chooses.** The assistant calculates, summarizes, identifies gaps, and holds constraints. The user chooses priorities, cuts, and commitments.
6. **One decision at a time.** Do not advance to the next planning decision until the current question has a real answer.
7. **Stay at month altitude.** Define outcomes, milestones, capacity, structure, and commitments. Leave detailed weekly task blocks to a weekly planning workflow.
8. **No saved plan without explicit approval.** A plan assembled from notes is a draft, not a decision. The user must restate or materially confirm the theme and commitments, then explicitly approve it.
9. **Use explicit dates.** Use **DD MMM** format unless the user prefers another unambiguous convention.
10. **Keep records useful, not exhaustive.** Save decisions, evidence, and constraints rather than a meeting transcript.
11. **Do not lecture.** For training, health, recovery, or personal practice, provide the numbers, the direct conclusion, and the agreed commitment. Give specialist advice only when asked and appropriate.
12. **Treat ideas as candidates, not commitments.** A brainstorm, voice note, imported task list, or assistant-written draft does not become a plan until the user chooses and approves it.

## Step 1: Determine the range and gather evidence

Determine the review month, prior comparison month, and planning month. Then make one initial batch of reads where possible.

Choose sources that match the user’s system: a task manager, project tracker, calendar, spreadsheet, notes application, health tracker, training log, or user-supplied facts. Request only the fields needed for this review.

| Evidence area | Gather in the initial pass |
|---|---|
| Previous monthly record | Theme, promised outcomes, commitments, and prior review findings |
| Weekly records | Plans and reviews in the review range; repeated blockers, milestones, and carried work |
| Goals | Active weekly, monthly, quarterly, and annual goals; status, deadlines, and notes |
| Work delivered | Completed tasks, decisions, projects, or deliverables; grouped into useful domains |
| Calendar | Next-month travel, leave, fixed deadlines, recurring commitments, and heavy meeting weeks |
| Daily signals | User-selected ratings, focus time, journals, habits, or mood notes |
| Sleep and recovery | Optional sleep duration, sleep quality, and same-source recovery trends |
| Training or practice | Optional sessions from the review and prior months, plus the live commitment or schedule |

For large sources, return computed statistics and a few representative themes rather than raw entries. Long journals and month-long event lists can crowd out the actual review. Use filtered queries, aggregation, summaries, or a delegated helper when available.

If a helper is used for a large calendar, journal, or task source, give it a narrow brief: use only authorized read access, analyze only the requested date range, and return a concise planning summary rather than raw records. The summary should include:

- Fixed multi-day blocks, such as travel, leave, or conferences.
- Approximate meeting load by week.
- Important recurring commitments.
- Protected personal or social commitments, without unnecessary private details.
- Planning anomalies, such as meetings inside unavailable periods or likely time-zone mistakes.

Before detailed monthly planning, re-read any weekly plans that overlap the beginning of the planning range. A weekly plan may already define that period in more detail. Reference and reconcile it with monthly outcomes; never duplicate or overwrite it.

## Step 2: Show the evidence picture

Present a compact factual picture before asking the user to explain it. Be direct, numeric where useful, and concise.

### Personal-practice, training, health, or recovery verdict

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

> Available working days × recently observed focused hours per day.

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
## Personal-practice, training, health, or recovery verdict
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
- Only authorized, minimum-necessary data was used.
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
- Treating incomplete data as a complete record.
- Confusing a list of events with a plan.
- Overloading capacity and refusing to cut scope.
- Letting the assistant choose priorities.
- Saving an unapproved draft.
- Duplicating or conflicting with weekly plans.
- Treating wellbeing averages as more truthful than repeated written evidence.
- Applying generic productivity rituals instead of fixing the actual drain.
- Overwriting an existing record without resolving the difference.
- Treating a brainstorm, imported task list, or voice note as a confirmed commitment.
- Saving unnecessary private details in a monthly record or sharing them outside the appropriate access boundary.


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
description: Review authorized meeting records, identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

Use only records the user is authorized to access and only for a legitimate purpose. Read the minimum sources necessary to establish ownership, outcome, and timing. Do not copy unrelated personal details, sensitive discussion, or confidential information into tasks or status reports. Keep source links and task content within the access boundary of the selected task system.

## Purpose and operating rules

Apply these outcomes before each run:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same counterparty or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text** is strongest evidence of who agreed to do what and when.
2. **Human-written notes** are supporting evidence, especially explicit action sections.
3. **Automated summaries** are useful for orientation but not authoritative for ownership.
4. **Pre-meeting agendas** describe intended discussion, not commitments.

Automated summaries commonly misattribute actions in recurring one-to-ones, brainstorms, and meetings where attendees list their own work. Never create a task solely because a summary labels something an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work that was completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, stated interest, request, or open question is not a task unless someone explicitly accepted responsibility for a concrete outcome.

Apply responsibility boundaries supplied by the user or organization. Being present in a meeting does not make the user accountable for all work in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` form, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no scope is supplied, use this default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect the title, date and time, record link or identifier, relevant attendees, and available transcript, notes, summary, and linked context.

Report a compact count before processing. Do not infer actions from a meeting title alone.

## 2. Fetch and inspect complete records

Fetch full meeting records in parallel when the meeting system supports batch retrieval. Do not search for existing tasks yet: first identify the people, topics, and candidate outcomes needed for accurate deduplication.

For long transcripts, use a repeatable search, extraction, or chunking method instead of relying on truncated previews. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by explicit acceptance

Review summary action items as candidates, then verify them against the transcript and surrounding conversation. A promise may have been conditional, reassigned, completed during the call, or directed to another attendee.

## 3. Triage each meeting

Classify the meeting loosely. The classification gives a starting expectation; evidence overrides it.

| Meeting type | Usual outcome | Guidance |
|---|---:|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or explicitly timed follow-up. |
| Information-gathering, interview, or reference call | 0 tasks | Create work only for an explicit out-of-meeting commitment by the user. |
| Internal planning or team meeting | 0–1 user-owned task | Capture the user’s deliverable, not the full team action list. |
| Coaching or recurring one-to-one | 0–1 task | Usually create a task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1–2 tasks | Often separate an internal decision from an external response. |

For each meeting, identify:

- Relationship context, including whether this is an initial discussion, recurring meeting, referral, or ongoing workstream where relevant.
- Candidate actions owned by the user.
- Work completed during the meeting.
- Work delegated to a named owner.
- Explicit future commitments and timing.
- Enough neutral context for a task to remain understandable weeks later.
- Source and related links that the task audience may access.

Use these skip signals:

- The user completed the promised work live and the resulting artifact was actually shared, produced, or recorded during the meeting.
- Another named owner accepted the work, or it falls within an established responsibility boundary outside the user’s role.
- The meeting was informational and any required synthesis is already retained in the authorized meeting record.
- An active task already covers the same outcome.
- The statement was not an actual commitment.

For external meetings, create a later reconnect task only when the user explicitly committed to reconnecting and gave a timing cue or agreed trigger. Do not turn a vague “let’s stay in touch” into a scheduled task. If an immediate follow-up and a later reconnect are both explicit, they normally become separate tasks because their horizons differ.

## 4. Decide the task shape

Combine actions into one task when they have the same counterparty, horizon, and outcome. For example, sending promised material, answering related questions, and offering times to meet can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as a reply tomorrow and a reconnect in several months.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

Use this readiness gate before task creation. Every proposed task must have:

- A confirmed owner.
- A genuine unfinished outcome.
- A clear, independently completable shape.
- A plausible due date or review date.
- Enough context and authorized links to stand alone.

If any of these are unclear, hold that item for the batched questions step rather than guessing.

## 5. Write the task

Use the user’s chosen task system and its field names. At minimum, capture:

- **Title:** short, verb-led, and specific, for example, “Follow up with partner about pilot scope.”
- **Status:** the standard open status.
- **Due date:** based on the commitment whenever possible.
- **Priority:** use the user’s scale; default to important time-sensitive work and reserve the highest priority for a real deadline, material risk, or a counterparty waiting for a response that week.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and links.

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: the agreed date or a reasonable reminder date before an agreed trigger.
- Weekly or sprint commitment: the next relevant review, planning, or accountability session.
- Flexible work: approximately five to seven days out, adjusted to workload.
- Older meetings processed late: move an immediate follow-up to the next workable date rather than assigning a past due date, unless the original deadline still applies.

Do not raise priority merely because capture happened late.

### Task-notes format

Use time-independent wording. Prefer absolute dates over terms such as “yesterday” or “next week.” Include only context appropriate for everyone who can access the task.

```markdown
[Two or three sentences of durable context. State the meeting date where useful,
why this matters, the confirmed commitment, and any necessary sensitivity.]

## Actions
- [Concrete action]
- [Concrete action]

## Draft message

Subject: [Specific subject]

Hi [First name],

[Short, direct message that fulfills the commitment and contains a clear
request, answer, or promised deliverable.]

Best,
[Sender]

## Links
- Meeting record: <authorized-link>
- Related document: <authorized-link>
```

If the action is to send a message, write a ready-to-send draft rather than merely saying “send an email.” Follow the user’s approved writing profile if one exists. Otherwise, use concise, warm, professional language; avoid filler, unsupported claims, and unnecessary disclosure. For introductions, use double opt-in: ask each relevant party for permission before connecting them.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search using the meeting link or identifier, counterparty, distinctive topic terms, and proposed title.

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. Skip a new task when the existing task is sufficient. Update the existing task only when the meeting adds a meaningful action, deadline, or authorized context. Record the decision for reporting.

## 7. Create confident tasks

Create all high-confidence tasks in a batch when possible. If the environment supports opening created records, open them in the selected task system rather than filling the status report with management links.

For every skipped meeting, give one brief reason, such as “No out-of-meeting commitment,” “Completed during the call,” “Owned by another role,” or “Already covered by an active task.”

## 8. Batch uncertain questions

Skip this step entirely when all decisions are confident. Do not interrupt for each ambiguity. Create confident tasks first, then ask all remaining questions together.

Ask the smallest question that resolves ownership, scope, timing, completion status, responsibility boundary, or duplicate handling:

```markdown
**[Meeting title]**
Question: [One specific question]
Context: [One sentence grounded in the authorized record]
Option A: [Task to create or update if true]
Option B: [Skip or alternate task shape]
```

Wait for answers before creating uncertain tasks. After answers arrive, create or update the remaining tasks and rerun the duplicate check if the answer changes the proposed outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, capture lessons that genuinely improve future runs, separate from the meeting task itself.

- Add a short pattern note to a reusable meeting-archetype reference when a recurring pattern affects triage, such as an attribution error, a reliable sign of in-meeting completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new responsibility boundary in the user’s or organization’s maintained reference when it applies beyond one meeting.

Do not turn one-off facts into permanent rules. Small additions to a pattern reference can be made directly. Ask for confirmation before structural changes, such as adding or removing a step or changing the evidence order. Briefly report reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a confirmed owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task has an appropriate authorized source link where useful.
- Message drafts are ready to send and follow the user’s preferences.
- Every uncertain item is either asked as a specific question or explicitly deferred.

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
description: Create or improve a short, paid, asynchronous work sample that produces job-relevant evidence, is practical to score, and is validated through simulated submissions before use.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A strong work sample asks candidates to do a realistic, bounded version of the role, produces observable evidence of role-relevant performance, and can be reviewed consistently without creating unnecessary work for candidates or reviewers.

Use this workflow for a new work sample or a revision to an existing one. Do not use it for interview questions, application-form screeners, or multi-day work trials. If the requested format is unclear, ask one question before proceeding.

## Purpose and design principles

A work sample usually sits after initial application review and before later interviews. Its purpose is narrow: determine whether a candidate can demonstrate a small set of important capabilities in a realistic, time-bounded situation.

Do not try to assess the whole person or every requirement of the role. Other stages are often better suited to assess different evidence:

- Interviews can assess communication, motivation, collaboration, and live reasoning.
- References can assess reliability, integrity, and sustained performance.
- A longer trial can assess judgment and consistency across days or weeks.
- Training can often address a specific tool, internal process, or nonessential domain vocabulary.

Default constraints:

- Make the exercise paid, unless a local legal requirement or established policy requires another approach.
- Set a clear expected duration, commonly two to four hours.
- Use a fictionalized, anonymized, or approved public scenario.
- Do not ask candidates to create work the organization will use commercially or operationally unless that use is disclosed and separately agreed.
- Design for roughly 20 to 25 minutes of reviewer time per submission.
- Make the exercise self-contained. Candidates should not need access to internal systems, private records, or unavailable people.
- State what AI assistance is permitted, and evaluate judgment and usefulness rather than trying to infer AI use from writing style.
- Assess only capabilities materially related to the role. Check for irrelevant proxies and avoid criteria connected to protected characteristics.
- Offer a reasonable accommodation route or an equivalent accessible format while preserving the role-relevant standard.

If the workflow requires access to internal hiring materials, prior candidate records, or communications about people, confirm a legitimate hiring purpose and clear authorization first. Use only the minimum relevant sources, omit unrelated or sensitive personal details, and keep drafts, simulations, and review guidance within the approved hiring access boundary.

## Step 1: Pre-flight

Before designing the exercise, confirm that the hiring team has both:

1. A current job description or role brief describing responsibilities, level, outcomes, reporting context, and constraints.
2. A role-success profile, hiring plan, or equivalent document identifying the capabilities and experience that are most likely to produce the required outcomes.

If either is missing, stop. Do not attempt to discover the success profile while drafting the test. That creates a moving target and commonly results in an exercise that sounds plausible but measures the wrong things.

Use this request format:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

When both exist, read the relevant role context. This may include approved project notes, role constraints, examples of strong work, prior hiring feedback, and existing work samples for comparable roles. Read one or two reference exercises only to calibrate tone, length, and operational format. Do not reuse a task shape automatically. Different roles require different evidence.

Give a brief status update after review, for example:

> Read the role brief, success profile, and two reference exercises. Moving to the alignment memo.

## Step 2: Write the alignment memo before drafting

Do not write candidate-facing instructions yet. First create a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five capabilities that the role succeeds or fails on and that can be surfaced during the exercise window. Phrase them as observable capabilities, rather than vague personal qualities.

Weak: “Strategic thinking.”

Better: “Can identify the highest-leverage problem in a messy operating situation, explain the tradeoff, and deliver a useful first action.”

### What the exercise will not test

Name important criteria that belong in another stage. This keeps the exercise honest and prevents it from becoming an unrealistic proxy for the entire job.

For example, a short written exercise may not fairly assess sustained reliability, leadership over months, live responsiveness, specialized internal software fluency, or long-term collaboration.

### Calibration to role level

State the role level: entry-level, mid-level, senior, or leadership. Explain what that changes:

- Entry-level candidates may need more context and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make tradeoffs, establish direction, and create work another person can use without further explanation.

### Failure modes to catch

Identify two or three plausible work patterns that could look strong in conventional screening but would create problems in this role. Describe demonstrated behavior, not identity or background.

Examples:

- A polished planner who does not ship usable work.
- A fast executor who misses the central problem or creates avoidable risk.
- A careful candidate who defers every meaningful decision.
- A technically capable candidate who cannot communicate for the intended audience.

### What strong looks like

Write one short paragraph describing a top submission. Focus on what it notices, the choices it makes, the tradeoffs it explains, the quality of the deliverables, and how it handles uncertainty.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the owner confirms or revises the memo.

## Step 3: Propose three exercise shapes

Once the memo is approved, propose three shapes. Each should test the load-bearing capabilities in a different way, be understandable in about one minute, be self-contained, and be scorable quickly.

For each option, provide:

- **Shape:** a plain-language candidate task.
- **What it tests:** the load-bearing capabilities it reveals.
- **Why it is evaluable:** the evidence reviewers will see and why it can be judged consistently.
- **Main risk:** the most likely source of noise, unfairness, or weak signal.

Keep each option concise. Common shapes include:

- **Triage pile:** Candidates receive messages, requests, and constraints. They prioritize, draft responses or work products, and recommend one systemic improvement. This suits operations, coordination, support, and communications-heavy roles.
- **Choose the highest-leverage action and ship it:** Candidates receive a brief with several possible priorities, select one, explain the choice, and create a small usable output. This suits strategic operations and builder roles.
- **Diagnose and fix:** Candidates review a messy situation, identify the key problem, and deliver one targeted intervention. This suits analytical, product, program, and process-improvement roles.
- **Source and pitch:** Candidates define a target profile, identify promising channels or prospects from supplied information, and write outreach. This suits recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** Candidates assess an intervention area using supplied evidence and make a recommendation for a decision-maker. This suits research, policy, strategy, and specialist roles.
- **Design a repeatable system:** Candidates create a lightweight process, playbook, or operating artifact another teammate could use. This suits program, community, enablement, and operations-design roles.

Do not draft the full test until the hiring owner chooses a shape. If none fits, propose three more based on the confirmed capabilities.

## Step 4: Draft version 1

Write the candidate-facing exercise in this order.

## [Role] Work Sample

State in one or two sentences which role-relevant capabilities the work sample assesses. State the expected total time.

**Your mission**

Describe a specific situation, rather than an abstract assignment. Give enough context to make the task realistic. If decisiveness is a capability being assessed, clearly state which stakeholders are unavailable during the exercise so candidates must make reasonable assumptions instead of deferring every decision.

End with one sentence restating what the candidate will produce.

**Deliverables**

List two to four parts and include rough time guidance where useful. A common operations pattern is:

- A short prioritization or analysis section.
- Several actual drafts, decisions, or shipped outputs.
- One systemic fix, process improvement, or reusable artifact.

Avoid excessive micro-tasks. A few substantive outputs create stronger evidence than dozens of shallow decisions. If planning and execution both matter, explicitly tell candidates not to let planning consume the time needed to deliver work.

**Context**

Provide the minimum information required: project state, intended audience, constraints, available resources, relevant policy, and stakeholder availability. Use fictional names, domains, and identifiers unless the hiring owner approves real public information.

For a triage-pile exercise, include approximately eight to ten realistic items. Connect several items so candidates benefit from seeing patterns across the whole situation. Add reference notes containing all information needed to make fair decisions, such as escalation rules, capacity limits, or refund policy.

**Instructions**

Include:

- Expected time limit.
- Submission deadline.
- Submission format, such as one document or PDF, plus accessible links to supplementary artifacts where needed.
- Payment amount, payment process, and any early-submission bonus.
- Permitted tools and AI assistance.
- A request to state important assumptions briefly.
- Permission to submit incomplete work if time runs out.
- Optional guidance on a short walkthrough video, if it would produce useful evidence.

Choose payment using the role level, local market, expected time, and candidate burden. State the amount and payment process before candidates begin. If offering a speed bonus, ensure it rewards a role-relevant capability and does not penalize candidates who need reasonable accommodations or have unavoidable access constraints.

Use a transparent AI policy, for example:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

**Anticipated questions**

Include answers to these common questions:

- If a requirement is unclear, make a reasonable assumption and state it briefly.
- If you do not finish in the expected time, submit what you have and note what you would do next.
- The work will be used only to evaluate candidates for this role unless another use is agreed separately.
- If you need an accommodation or an equivalent accessible format, contact the designated hiring contact.

After every draft, add a separate owner-only section:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets on choices the owner may want to change, such as whether an item is too obvious, whether the scenario is sufficiently realistic, whether payment matches the burden, whether a deliverable is too prescriptive, or whether a walkthrough video should be optional.

End with one focused decision question, such as: “Which part should we tighten first?”

## Candidate-facing format checks

Write in direct, plain language and use the locale appropriate to the candidate audience. Before sharing a draft, check that it:

- Uses headings and bullets that work in the destination hiring system.
- Avoids tables and horizontal divider lines when the destination system renders them poorly.
- Avoids generic slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.
- Uses “by the end of [day]” rather than abbreviated phrasing.
- Uses clearly fictional names and email addresses in fictional scenarios.
- Formats multi-line message metadata using the destination system’s supported soft-break method when ordinary line breaks collapse.
- Contains no credentials, private contact details, sensitive internal data, or confidential personal information.

## Step 5: Iterate with the hiring owner

Expect multiple feedback rounds. For each revision, provide the complete updated work sample, not only a change list, so it can be copied into the chosen system.

Apply feedback directly unless it would materially undermine validity, fairness, privacy, accessibility, or safety. If so, state the concern once in plain language, offer a practical alternative, and let the accountable hiring owner decide.

Common revisions include tightening vague instructions, loosening overly prescriptive tasks, correcting scenario facts, simplifying deliverables, changing payment, and replacing unrealistic details.

## Step 6: Simulate two submissions

Before declaring version 1 complete, simulate two full submissions in parallel using the exact candidate-facing instructions.

### Role-aligned simulation

Use a persona that matches the approved role-success profile. Have them complete the actual deliverables within the stated time limit and add a short reflection on choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest, capable candidate who could pass ordinary screening but whose submission lacks one role-critical capability. Use a relevant difference in demonstrated work, such as planning without execution, excessive caution where decisive judgment is needed, or execution without systems awareness. Never tie the comparison to identity, demographics, or background.

Have this persona produce the same submission shape.

Then synthesize:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both submissions were similar.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by expected impact.

A floor check that both simulations pass is not automatically a problem. The concern is when a central capability does not produce meaningfully different evidence.

## Step 7: Apply validation improvements

Revise the full exercise based on the simulation. Target the weakest diagnostic points first. Useful improvements may include:

- Making scenario items more interdependent.
- Removing obvious noise that takes seconds to dismiss.
- Adding a concrete constraint that forces a meaningful tradeoff.
- Replacing a broad opinion prompt with a usable deliverable.
- Clarifying reviewer criteria so scoring rewards the intended behavior.
- Removing specialized knowledge requirements that are trainable and not essential at the start of the role.

Do not make a task harder merely to make it more selective. Make it more diagnostic of the confirmed capabilities.

## Step 8: Optional external review

If reviewers provide feedback, assess each suggestion against the approved alignment memo. State which suggestions to integrate, which to skip, and why. External feedback is evidence, not an automatic instruction. The accountable hiring owner remains responsible for the assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The role description and role-success profile are confirmed.
- The alignment memo is approved.
- The chosen task shape maps directly to the load-bearing capabilities.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and requires no private-system access.
- Payment, deadline, and submission instructions are clear.
- Accommodation and accessibility routes are clear.
- A reviewer can score a submission in roughly 20 to 25 minutes.
- A role-aligned and plausible role-misaligned simulation have been completed.
- Simulation findings led to necessary revisions.
- The exercise contains no sensitive information and does not create undisclosed production work.
- Role-relevant criteria and potential proxy bias have been checked.

## Common failure modes

Avoid designing the task before agreeing what it should measure. Avoid testing specific tools, domain trivia, or trainable knowledge instead of durable role-relevant judgment. Avoid asking for too many small outputs, making every scenario item independent, giving vague context that rewards insider knowledge, or allowing candidates to defer every meaningful choice to an available stakeholder.

Also avoid word-count targets that encourage padding, exercises that take longer to grade than their signal justifies, and treating polished writing as the main evidence when the role requires something else. Do not declare success without checking whether the exercise distinguishes the relevant performance it was designed to assess.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, respectful of candidate time, and clear about what strong performance looks like.


---
name: run-a-reference-call
description: Prepare, document, and run a structured hiring reference call that gathers role-relevant evidence, tests open questions fairly, and records a defensible basis for the hiring decision.
---

# Run a reference call

Use this workflow when an authorized hiring team needs to speak with a candidate’s professional reference. Its deliverable is a complete, access-controlled reference-call record in the team’s chosen meeting or hiring workspace, not merely a research summary or chat response.

Use a different process when responding to an outside organization that requests a reference about a former participant, employee, or colleague. In that case, confirm authorization and consent requirements before sharing information.

## Purpose and boundaries

A reference call should reduce specific uncertainty about role-relevant performance. It should not be a search for general praise, personal gossip, protected information, or confirmation of a pre-made decision.

Before accessing communications, calendars, hiring records, or prior notes:

- Confirm a legitimate hiring purpose and that you are authorized to access each source.
- Use the minimum information and sources needed to prepare the call.
- Keep the record within the hiring team’s appropriate access boundary.
- Exclude unrelated personal details, sensitive personal data, and speculation.
- Treat the referee’s observations as evidence with limits, not as a final verdict.
- Do not disclose confidential interview feedback, private notes from other referees, or internal deliberations to the referee.

## Required inputs

Collect or confirm:

- Candidate name.
- Referee name and reliable contact details.
- Role under consideration and the role’s expected outcomes.
- Call date, time, and meeting details, if scheduled.
- The referee’s relationship to the candidate.
- Hiring stage and the decision or next step the call informs.
- Specific uncertainties, strengths, or development areas the call should clarify.

If key information is missing, identify the gap in the call record and proceed only with what is necessary. Do not invent relationship history, hiring stage, dates, or links.

## 1. Find the call and establish logistics

Search the authorized calendar or scheduling system for the referee’s name or contact details. Record the meeting title, date and time, attendees, joining details, and relevant scheduling context.

If no event exists, create a preparation record anyway and clearly mark logistics as unscheduled or unconfirmed. Do not imply that a meeting has been arranged.

## 2. Gather only relevant context

### Identify the hiring context

Review authorized hiring materials and relevant correspondence to establish:

- The role and the work outcomes that matter most.
- The candidate’s current stage.
- How the referee was introduced or nominated.
- The nature, duration, and closeness of the working relationship.
- Open questions arising from role-relevant interviews, work samples, or assessments.

Prefer the candidate’s reference-list introduction and direct hiring records for relationship facts. Distinguish verified facts from assumptions.

### Research the referee proportionately

Use authorized internal sources first, such as direct correspondence, prior meeting records, and organization knowledge. If external public research is appropriate, use only publicly available professional information needed to understand the referee’s role and likely vantage point.

Look for:

- Current or relevant past role and organization.
- Whether the referee directly observed the candidate’s work.
- Prior professional interactions between the hiring organization and the referee’s organization that could affect context or independence.
- Previous meetings or reference conversations, where access is authorized.

Do not collect private biographical details or unrelated information. A referee’s seniority or online profile does not by itself establish that they observed the candidate closely.

### Review candidate materials and previous references

Add links to authorized candidate materials that will help the caller navigate during the conversation, such as the application profile, professional profile, work portfolio, or work sample.

Locate completed reference records for the same candidate, if authorized. Extract only decision-relevant themes: concrete strengths, development areas, contradictions, and unanswered questions. Attribute statements to the source in the internal record, but do not repeat one referee’s comments to another referee as if they were established fact.

If this is the first reference, identify the observations that later calls should independently test.

## 3. Create the reference-call record before the call

Create one page or record in the team’s chosen meeting or hiring workspace. Include the date, referee, candidate, role, appropriate internal attendees, and meeting link if available. If the workspace supports recording or transcription, use it only with the required notice, consent, and retention controls.

Use this structure:

```markdown
## Context
- **Referee:** [Name] — [role and organization, if verified]; [brief relevant background].
- **Relationship to candidate:** [how they worked together, capacity, approximate period, and closeness of observation].
- **Hiring context:** Candidate is being considered for [role] at [stage]. The call informs [decision or next step].
- **Candidate materials:** [authorized application/profile/portfolio links].
- **Other references:** [names and relationships, if known and appropriate to record].

## Opening
> Thanks for making time. I’m [caller role] with [organization]. [Candidate] is being considered for our [role]. We are collecting role-relevant examples to make a careful decision. We will keep what you share within the appropriate hiring team and use it only for this process. Is it alright to proceed?

## Briefing notes
- **Decision questions:** [the two to four uncertainties this call should reduce].
- **What this referee can uniquely assess:** [work, setting, period, or behavior they directly observed].
- **Evidence to cross-check:** [prior theme stated neutrally, plus what concrete example would clarify it].
- **Context or independence considerations:** [relevant organizational connection, limited observation, or possible bias].
- **First-reference note:** [what later calls should validate, if applicable].

## Questions
- [questions tailored to the role and referee relationship]

## Notes and assessment
- **Direct observations:**
- **Referee interpretation:**
- **Concrete examples and outcomes:**
- **Limits of evidence:**
- **Follow-ups or contradictions:**
- **Caller inference for the hiring team:**
```

Keep context concise. The briefing notes are the highest-value preparation section: write direct, testable prompts rather than vague reminders. For example: “The work sample suggests strong independent analysis but limited stakeholder evidence. Ask for a project where the candidate had to align people with competing priorities.”

## 4. Ask a consistent core set of questions

Start by establishing the referee’s vantage point. Then ask for examples, outcomes, and comparison points.

- How did you work together, and how closely did you observe the candidate’s work?
- What did the candidate personally own or deliver? What was the result?
- What did strong performance look like in practice? How did it compare with expectations?
- What is their most distinctive work-related strength? Please give an example.
- Where did they need the most support, structure, or feedback?
- How did they respond when work became difficult, ambiguous, or changed direction?
- If they struggled in this role after several months, what would be the most likely reason?
- If they were succeeding, what development area would be most useful to prioritize next?
- What conditions, management approach, or team environment helped them do their best work?
- How would you compare their performance with relevant peers you have directly worked with?
- What have I not asked that would matter for their success in this role?

When an answer is broad, follow with: “What did that look like?” “What was their personal contribution?” “What happened next?” or “Can you give a specific example?”

## 5. Add role-specific probes

Choose three to five probes based on the role’s real outcomes. Avoid treating personality style as a substitute for evidence.

For an operations or program role, ask about handling ambiguity, building repeatable systems, communicating with varied stakeholders, prioritizing competing work, and identifying needs without waiting for direction.

For a community-facing role, ask about building trust and participation, resolving conflict appropriately, creating durable processes, maintaining boundaries, and adapting engagement based on feedback.

For a senior operations role, ask about scaling workflows, making trade-offs across stakeholders, managing budgets or external partners where relevant, and balancing speed with reliable controls.

For any role, ensure each probe tests a capability that is actually relevant to successful performance.

## 6. Test concerns fairly

Translate each hiring concern into a neutral, evidence-seeking question. Do not reveal private assessments or ask leading questions such as “Did they have the same problem with you?” Instead ask about the underlying capability and request examples.

Weight evidence by directness of observation, recency, specificity, and relevance to the role. A confident opinion without examples is weaker than a concrete account from someone who worked closely with the candidate.

## 7. Complete the record and audit it

Immediately after the call, separate:

- What the referee directly observed.
- The referee’s interpretation or recommendation.
- Your inference for the hiring decision.
- Remaining uncertainty and evidence limits.

Before sharing the record, check that it contains the call logistics, verified relationship context, role-relevant questions, concrete examples, and clear follow-ups. Remove unnecessary sensitive details. Confirm that links and access permissions are limited to the appropriate hiring group.

Do not treat one reference as decisive on its own. Compare evidence across interviews, assessments, and multiple references where available. Escalate material contradictions, insufficient direct observation, or concerns requiring further verification to the authorized hiring decision-maker.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and privacy, verifying rendered page state, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing rendered forms, changing settings, collecting data from dynamic pages, testing a user flow, or working in an authenticated dashboard. Use it when a simple retrieval request or supported direct interface cannot safely and reliably complete the work.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not perform a consequential final action until the account, target, page state, and authorization are clear.

A browser automation call succeeding does **not** prove that the website accepted the change. Modern web applications may keep internal state separately from the visible DOM, commit values only after focus leaves a field, replace controls during a re-render, or report a cosmetic error after an action has actually succeeded.

## 1. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can perform the requested task. It is usually more reliable than reproducing browser interactions.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, UI testing, and forms that do not require the user's established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing session, single sign-on state, account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for a direct route. Check official documentation, ordinary form actions, page source, and visible network activity for supported endpoints. A form may submit structured data to an authorized service that is safer to use directly.

Do not use undocumented interfaces to bypass access controls, consent boundaries, contractual restrictions, or other protections. Do not use an authenticated visible session merely because it is convenient: it can interrupt the user's work and increases privacy and account risk.

If a site blocks automated browsing, do not attempt to evade its protections for casual research or collection. A user-visible session may be appropriate only when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and the established session is necessary. Do not weaken browser security, access controls, warnings, authentication, or anti-abuse protections.

## 2. Protect account identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into notes, screenshots, logs, or reports. Keep results within the requester's appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated context, identify the correct account, organization, environment, and browser profile. Never infer identity from a generic browser-window name, an old tab title, a remembered default, or a browser connection label.

Use these rules:

- Announce when taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Classify the intended context explicitly: for example, personal, work, testing, staging, or production.
- Select the browser profile or connection that corresponds to that context rather than relying on a generic browser selector.
- Confirm the signed-in account with a reliable account indicator before opening or changing the real target.
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

If a page reloads, re-renders, or the session changes between passes, do not assume the earlier state remains valid. Restore intended values if needed and verify them again before committing.

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

### Generic form-inspection pattern

Use a page-inspection capability to list relevant controls before writing fill logic. The automation library is user-selected, but the inspection should record at least tag, input type, role, label, required state, and current value or text length.

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

## 5. Use the correct interaction for each control

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

A useful verification routine is:

1. Read the value, text content, selected option, checked state, or rendered date from the page.
2. Compare it with the intended result.
3. Check that focus has left the control when the application commits on blur.
4. Wait for any expected re-render or save indicator to settle.
5. Re-check any earlier field that a dependent action could have reset.

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
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline or editor control, or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control that the application actually reads. |
| Automation becomes unstable on a complex page | The chosen automation layer is unsuitable | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and normal browsers show different behavior | The site varies behavior by browser context | Prefer an authorized direct interface; if necessary for an explicit task, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior | Close it through a neutral page action and re-verify affected fields. |
| A visible error may be cosmetic | The task may already have completed | Inspect resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |
| A security check or authentication prompt appears | The site requires user presence or authentication | Ask the authorized user to complete it; do not bypass it or capture secrets. |

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
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using real screenshots and programmatic layout checks. Fix and retest failures before reporting the change as complete.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. This includes small spacing, color, background, typography, or alignment edits: a local change can alter wrapping, overflow, height, backgrounds, or access at another screen size.

Do not rely on bounding-box values alone, or on one desktop and one mobile screenshot. Screenshots reveal visual defects that measurements can miss; measurements find off-screen defects that screenshots can miss. A viewport passes only when both forms of evidence pass.

## 1. Prepare a realistic test state

Run the interface in an appropriate test environment. If test content comes from records or communications, use it only for a legitimate purpose and with clear authorization. Use the minimum information needed, and do not expose unnecessary personal or sensitive data in screenshots, logs, or reports.

Populate the changed surface with representative conditions:

- long text, long field values, and realistic labels;
- typical lists, cards, rows, and validation messages;
- enough items to exercise wrapping, scrolling, and spacing;
- loading, empty, and error states when the change affects them.

Do not validate only an empty or unusually tidy state. Sparse content often hides clipping, overlap, and blank-space problems.

## 2. Choose the viewport sweep

Test these baseline widths unless the product has a documented alternative matrix:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large width, such as 1920 px, for wide layouts or large-display use cases. Include any viewport known to be important for the product.

When vertical layout can matter, test a short viewport (about 700 px high) and a tall viewport (about 1400 px or more) at the relevant widths. Include a very tall viewport, such as 1800 px, when changing viewport-height or minimum-height behavior, flexible page shells, backgrounds, vertical spacing, sticky footers, or bottom alignment.

Use a repeatable browser automation system chosen for the project. Prefer headless execution when it supports consistent, reproducible results.

## 3. Capture and inspect screenshots

Capture screenshots for each relevant viewport and state. Use full-page captures when document length matters, and visible-viewport captures when fixed, sticky, or viewport-height behavior matters.

Inspect each changed component on all four sides: top, right, bottom, and left. Ask whether each edge now matches the intended design.

Be especially careful with edge-to-edge or full-bleed changes. Removing containment on one side can reveal leftover wrapper margin or padding as a visible background strip on another side. Check all edges, not only the edge edited.

Reread the requested outcome and compare it directly with the screenshots. Do not accept a result simply because the CSS rule appears correct.

## 4. Run layout checks at each viewport

Alongside screenshots, check the behaviors relevant to the change:

- no unintended horizontal overflow;
- no unintended vertical overflow on screens intended to fit the viewport;
- no unintended overlap between changed content, neighboring content, and containers;
- controls remain visible, reachable, and usable;
- fixed or sticky interface elements do not hide essential content;
- cards, lists, and form controls remain within their intended bounds;
- prose retains a readable line length.

For fit-to-viewport pages, compare document height with viewport height and allow only a small rendering tolerance. For overlap checks, compare bounding rectangles of relevant elements and containers. Exclude intentionally layered elements from a generic no-overlap rule.

For prose-heavy pages, treat approximately 80 characters per line as a broad warning threshold. Reading-focused layouts commonly aim closer to 60–70 characters per line.

## 5. Fix failures and retest

If any viewport or state fails:

1. stop completion, review, or release;
2. identify the layout rule or component constraint causing the failure;
3. fix the underlying behavior rather than adding a one-viewport cosmetic patch;
4. rerun the full relevant sweep, not only the failing viewport.

If one fix resolves a size but breaks another, reconsider the diagnosis. The layout model is incomplete until it works across the required range.

## 6. Readiness gate and report

Do not claim that the interface “works on mobile and desktop” without evidence. Report the tested widths, relevant height variants and states, and the checks performed.

Example:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall viewports where relevant; no unintended overflow or overlap; controls remain usable; tall viewport clean.

If any required viewport or state was not tested, state that clearly and do not represent the change as complete.


---
name: run-a-recurring-community-event
description: Create, publish, and verify the next occurrence of a recurring community event, prepare fresh materials, and invite an authorized audience using the organizer’s chosen tools and policies.
---

# Run a recurring community event

Use this workflow for a repeated social, sports, learning, volunteer, or neighborhood event. Adapt the recurrence, event platform, creative tools, storage, event copy, and communication channels to the organizer’s choices.

## 1. Establish authority and boundaries

Choose the operating mode before making external changes:

- **Prepare only:** create materials and an unpublished draft.
- **Approval required:** prepare the event, then obtain approval before publishing or inviting.
- **Standing authorization:** publish and invite within a documented recurring-event policy.

Standing authorization should define the event series, normal audience, authorized hosts, approved platforms, and limits on visibility, cost, and outreach. Request a decision when an occurrence materially changes those boundaries, such as a new audience, public visibility, paid entry, new venue type, unusual safety issue, or different host arrangement.

When using calendars, RSVPs, attendee records, or community communications, have a legitimate event-management purpose and clear authorization. Use only the minimum relevant sources and fields. Respect opt-outs, consent choices, access needs, and privacy expectations. Do not copy attendee identities, private messages, sensitive personal information, or private calendar details into public event content or routine reports.

## 2. Plan the next occurrence

Calculate the next date from the recurrence rule and the event’s local time zone; do not rely on mental arithmetic. Confirm the weekday, date, start time, end time, location, and host arrangement.

If the series is numbered, inspect prior events and assign the number after the highest existing number. When reviewing history for invitations, include early unnumbered occurrences as well.

Check for practical conflicts: organizer availability, venue closure, holidays, route or weather risks, and local scheduling issues. A conflict does not automatically cancel an event. Follow the organizer’s policy, and report only the relevant operational consequence, such as a possible handoff or cancellation decision.

## 3. Update the event content

Review one or two recent occurrences and separate stable details from details that must change.

| Detail type | Examples |
|---|---|
| Stable | Purpose, usual format, meeting instructions, accessibility guidance, approved contact route |
| Occurrence-specific | Date, number, hosts, route, weather plan, capacity, theme, temporary notice |

Use an approved title pattern, such as `Event Name #N`. Deliberately update every occurrence-specific field. Do not reuse stale dates, expired links, temporary notices, old venue instructions, or former host details.

Use a current description template such as:

```text
[Short welcome and activity summary]

Meet: [time and exact meeting point]
Format: [activity, pace, duration, or route]
Afterward: [optional follow-up activity]

[Accessibility, preparation, or weather guidance if applicable]
[Approved contact or community link if appropriate for the visibility setting]
```

Ensure every link, contact route, and location detail is suitable for the event’s intended audience. Public pages should not disclose private addresses, attendee information, or internal organizer details unless that disclosure is intentional and authorized.

## 4. Prepare artwork when needed

If the series uses recurring artwork, retain a recognizable identity while making each occurrence visibly fresh. Review recent images before creating the next brief so the result is not a small variation of the previous one.

A useful image brief includes:

- required event name or text;
- the core activity or recognizable symbols;
- style, mood, and restrained palette;
- one distinct central visual idea; and
- quality constraints for the chosen creative tool.

Vary the concept through season, weather, light, viewpoint, local texture, an activity detail, or a small humorous focal idea. Prefer one clear subject and uncluttered composition. Request readable typography and avoid obvious defects such as garbled text, implausible anatomy, or excessive decorative effects.

Review the output before use. If it repeats recent work or has visible defects, revise the concept and regenerate a limited number of times. If a tool reports an error, first check whether the requested output was created before retrying. Upload only the selected final file, then verify its crop, legibility, and display on the event page.

## 5. Create and verify the event

Use the authorized organizer account and confirm the account or workspace before editing. If different services require different account contexts, verify each context before acting.

Determine whether the platform’s draft, save, or continue controls create a private draft or a live event. Complete fields in this order when practical:

1. **Title:** apply the approved naming pattern.
2. **Date and time:** set the local date and full start/end range.
3. **Location:** select the exact venue or map listing.
4. **Description:** apply the current template and updates.
5. **Image:** upload and inspect the artwork if used.
6. **Hosts:** add only authorized hosts or co-hosts.
7. **Settings:** confirm visibility, capacity, cost, RSVP rules, notifications, and accessibility information.

Treat date pickers and dynamic forms as high-risk controls. Finish and verify the date and time before changing unrelated fields. After a menu opens, a page scrolls, or the layout changes, inspect the visible state before clicking again. Prefer labeled controls over fixed screen positions.

Before publishing, review the draft as an attendee would. Confirm the title, number, date, time zone, location, description, links, image, hosts, and settings. If a required item cannot be verified, correct it, use a safe fallback, or request a decision. After publication, open the live page and repeat the attendee-facing checks. Save the live URL.

## 6. Invite the approved audience

Follow the documented invitation policy. Prior attendees may be an approved audience for the same series, but this is not a default. Do not expand the audience without authorization.

When inviting from prior events, process each relevant occurrence systematically:

1. Review or filter one prior occurrence at a time.
2. Check the current selection before using bulk-select controls.
3. Add attendees covered by the policy, then clear the filter and continue.
4. After each batch, confirm that the aggregate invitee count changed plausibly.

Some platforms preserve selections or deduplicate invitees. If the count drops or remains unexpectedly unchanged, stop and inspect the selection before proceeding. Re-check controls after layout changes. Send invitations only when authorized, then confirm the sent state, delivery result, or final aggregate invited count.

## 7. Report and maintain

Provide a concise operational report containing:

- what was created and whether it was published;
- date, time, and venue;
- invitation outcome or aggregate invitee count;
- relevant conflicts, unresolved items, or nonstandard settings; and
- the live event URL.

Keep the report within the recipient’s access boundary. Use aggregate counts rather than attendee identities. If the URL must be easy to copy, place it on the final line with no text after it.

After the occurrence, record reusable lessons only: platform behavior changes, durable audience rules, template updates, field-order constraints, and recurring creative preferences. Keep temporary event details and attendee data separate from the reusable workflow.

## Readiness check

Before declaring success, confirm that the date and numbering were calculated; the correct account and live page were verified; event-specific details were updated; artwork is usable if required; time, location, hosts, and settings are correct; invitations followed the approved policy; and publication and invitation results were verified or any limits were clearly reported.

# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a small ranked set while preserving the user’s final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not an unfiltered idea list: it is a set of meaningfully different paths, clear tradeoffs, and a short list of credible choices.

## 1. Gather relevant context

Start with the information the user provides. If they link or reference documents, discussion records, prior decisions, research, or other material that is available in the current environment, review the sources that are directly relevant.

When the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Constraints, commitments, budgets, deadlines, or dependencies
- Concerns from relevant stakeholders and ownership boundaries
- Evidence about attempts already made and their results

Use only sources that the user is authorized to access and share for this purpose. Review the minimum necessary information; omit unrelated personal or sensitive details from the response. Do not search broadly by default. If a key fact is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that identifies:

- What the user is actually deciding
- The important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging options

The stated request may describe a symptom or a preferred solution rather than the underlying decision. For example, “Should we add a feature?” may actually mean, “How can we reduce a recurring user problem within a limited delivery window?”

Ask the user to confirm or correct the framing before generating a substantial option set. You may skip this pause when the decision is obvious and low-stakes, or when the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision truly has fewer meaningful paths. Each option must represent a fundamentally different approach, not merely a different level of investment in the same approach. Merge near-duplicates.

Where relevant, include:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes the process, incentives, scope, or framing of the problem
- At least one surprising but plausible option, such as delaying, partnering, narrowing scope, observing longer, or doing nothing

Do not be contrarian merely to seem creative. A “do nothing” option is useful only when waiting, learning, timing, or avoiding distraction has genuine value.

Give each option a short, memorable label that communicates its core approach. For every option, provide:

- **What:** One or two sentences explaining the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limits.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a favored option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Select criteria that fit the decision. Common criteria include likely impact, effort, cost, speed, risk, reversibility, strategic fit, operational burden, and stakeholder effects. Add domain-specific criteria where they matter more than generic ones.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but state plainly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not merely why it is attractive in general.
4. Name the key assumption most likely to change the ranking, if there is one.

Do not force a single winner unless the user explicitly asks for one. Preserve genuine choice when multiple paths remain viable.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may:

- Select an option
- Request more detail on an option
- Correct the framing or constraints
- Ask for additional options
- Combine elements of multiple options

If the user proposes a hybrid, check whether its components are compatible and whether the combination resolves a real tradeoff rather than simply adding complexity. Do not start implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record: the choice, accountable owner, rationale, assumptions, constraints, and review point.
- **Build-oriented choice:** After recording the decision, move to planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, challenge consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the real decision rather than only the requested solution.
- The options are genuinely distinct.
- The conventional option and a plausible alternative framing have both been considered where relevant.
- Weaknesses are candid and concrete.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than unstated assistant preferences.
- Any retrieved context was used with legitimate purpose, appropriate authorization, and minimal disclosure.


---
name: pressure-test
description: Find weak points in a leading strategic idea before commitment by steelmanning the case, testing its load-bearing assumptions through sequential challenge, and ending with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Input

Provide a claim, decision, or direction to test. Include available evidence and context, or state what is unknown.

**Input format**

> **Idea to test:** [Proposed action or decision]
>
> **Why now:** [Trigger, opportunity, or problem]
>
> **Expected outcome:** [Result, for whom, and by when]
>
> **Evidence available:** [Metrics, research, experiments, feedback, or prior decisions]
>
> **Constraints and stakes:** [Budget, time, dependencies, reversibility, or consequences]
>
> **Alternatives considered:** [Options, including doing nothing]

If internal records or communications are relevant, access them only for a legitimate purpose and with clear authorization. Use the minimum relevant sources and information. Do not include unrelated personal, confidential, or sensitive details in the analysis or output.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes an exercise in defending it.

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Distinguish facts, inferences, forecasts, and unknowns.
- Cite or link to available evidence when appropriate. Identify contradictions between the claim and the evidence.
- Refer to dissenters by relevant role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent anyone's views.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's actual intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If a stronger restatement changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, with the most decision-threatening assumption first. Make assumptions observable where possible.

| Rank | Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|---|
| 1 | [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Test or disproof method] |

Replace vague claims such as “users will value this” with a behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Start with the highest-risk assumption. Adapt later questions to prior answers; do not present the full set as a questionnaire, because that enables selective answers.

For each question, use this loop:

1. Ask one question.
2. Wait for the answer.
3. Classify the answer as evidence, inference, forecast, or unknown.
4. If it is vague, unsupported, or avoids the issue, ask a focused follow-up before continuing.
5. Record what the answer changes: confidence, assumption rank, needed test, or verdict risk.

Draw from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would happen in the next 30 or 90 days that would show this is wrong?
- **Counterfactual:** What similar attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that role say, and has that concern been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or disruption?
- **Null option:** What happens if no action is taken for the next three months?

“I think it will work” is not evidence. Ask for observed behavior, data, a comparison, or a credible commitment.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include a wrong underlying premise, execution risks, and external conditions where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or accountable role |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable signal] | [Check or accountable role] |

Warning signs must appear early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If that perspective has not been sought, mark it as an evidence gap; silence is not agreement.

| Relevant role | Strongest likely objection | Heard directly? | Gap-closing action |
|---|---|---|---|
| [Role] | [Objection] | [Yes, no, or unknown] | [Action] |

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test incomplete or failed rather than approving it.

## 7. Give a verdict and handoff

Choose one verdict and state the next step explicitly:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** One or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as targeted interviews, an expert review, a prototype, or a short data-collection period. Run that test, then decide with its result recorded.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, downside is unacceptable, or no meaningful falsification criterion can be named. Generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

Use this closing format:

> **Verdict:** [GREEN, AMBER, or RED]
>
> **Reason:** [The deciding evidence, assumption, or gap]
>
> **Next workflow step:** [Decide, test, generate alternatives, redesign, or defer]
>
> **Concrete next action:** [Owner] will [verb and specific action] by [date or decision point].

End with exactly one concrete next action containing a verb, an owner, and, when useful, a deadline.

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

Use this workflow for a non-trivial build, integration, automation, process, or operational problem whose solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to “build X,” work backward:

- Who experiences the problem?
- What are they trying to accomplish?
- What happens today?
- What workarounds exist?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the problem meaningfully better?

Write a concise problem statement and descriptive requirements. Describe the desired outcome and constraints, not an assumed implementation. If the proposed solution appears mismatched to the problem, say so directly.

Ask only for information that cannot be found in the available context, documentation, code, or authorized records. When consulting private communications, operational records, or information about people, confirm there is a legitimate purpose and clear authorization. Use the minimum relevant sources and details, omit unrelated sensitive information, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, and available alternatives. Include “do nothing” or “deprioritize” as a real option when the issue is rare, low-cost, or adequately handled by a workaround.

Distinguish reversible decisions from expensive commitments:

- **Reversible decisions:** Small, easy-to-change choices. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, long-lived configuration, migrations, external contracts, security boundaries, or vendor commitments. Pause and obtain an explicit decision before implementing. Record the decision and rationale when appropriate.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before inventing new ones.

Understand compatibility requirements, deployment practices, security expectations, supported environments, ownership boundaries, monitoring, and maintenance capacity. Use existing conventions unless there is a strong reason to change them.

Do not collect broad personal or confidential data merely because it is available. If role, user, or customer evidence is needed, use only information relevant to the stated problem and report it in a privacy-respecting, need-to-know form.

## 4. Define evaluation criteria

Define lightweight, explicit criteria before generating solutions. For example:

- Must preserve existing authentication, privacy, and data behavior.
- Must be feasible within the available time and maintenance capacity.
- Should avoid new dependencies or persistent configuration.
- Must have a clear verification method.
- Must be removable or reversible if it fails.
- Must fit the system’s operational and access-control boundaries.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of the same design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, training, or a capability already available in an existing platform.
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
- Put changes in the appropriate design boundary; avoid quick fixes that create hidden future cost.

## 6. Evaluate and recommend

Compare each viable option against the criteria from Step 4. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and their tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep proposals direct and short. Store durable proposals in the user’s chosen shared documentation system when review or collaboration is needed; otherwise provide them in the current workspace. Use a clear date-prefixed title, such as `23 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and ownership of follow-up actions. Keep the plan where reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, access control, and failure behavior.

Do not claim success based only on implementation. Identify what was actually tested and what remains unverified. Commit, publish, or deploy changes only according to the user’s repository, review, and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and its results.
- Known limitations, risks, and deferred work.
- Required user action, rollout step, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid exposing unnecessary personal, confidential, or internal information, and do not bury the reader in temporary implementation notes.


---
name: shape-and-draft
description: Shape consequential documents by reviewing authorized evidence, resolving material choices through answer-dependent interview rounds, checking readiness, then drafting and auditing the smallest document that can achieve the goal.
---

# Shape and draft a document

Develop a consequential document by shaping the thinking behind it before writing. Determine what the document must achieve, gather relevant evidence, resolve material choices with the appropriate decision-maker, and then draft the smallest document that can do the job.

Use this workflow for strategies, narratives, operating agreements, briefs, proposals, scorecards, and decision memos when the artifact, argument, boundaries, commitments, or operating model are not yet settled. Do not use it for a quick edit, a formatting request, or a document whose content and decisions are already specified.

## Classify the request

The request may name a document type, desired outcome, audience, source material, or some combination. Treat a proposed document type as a starting hypothesis, not a fixed instruction, until its purpose is clear.

Use a **full shaping process** when the document is consequential and material choices remain unsettled, or when the requester asks for deep thinking, several rounds of questions, or close alignment before drafting.

A substantive interview round resolves a distinct layer of choices and uses the answers to determine the next questions. Restating previous discussion or asking for broad approval is not a substantive round.

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
- **Scorecard:** Defines a role or team mission, outcomes, and role-relevant capabilities.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the material tradeoff and recommend an artifact. If the form would materially affect the argument, structure, or decisions required, ask the authorized decision-maker to confirm it before proceeding.

## 3. Gather and classify evidence

Read supplied material first. Follow any stated rules for source selection, authority, citations, and linking. Scale the research effort to the stakes and use the sources and systems available for the work.

When reviewing private communications or records about people, use them only for a legitimate purpose and with clear authorization. Use the minimum relevant sources and information, omit unrelated or sensitive personal details, respect consent and privacy expectations, and keep findings within the appropriate access boundary.

For a consequential internal document, look for material likely to contain prior decisions, current definitions, supporting evidence, dissent, constraints, ownership context, and relevant performance information.

Apply these evidence rules:

- Respect a stated hierarchy of sources.
- Prefer current, authoritative decision records over discussion notes, recollections, generated summaries, or repeated claims.
- Treat a discussion record as evidence of what participants said, not necessarily as the current decision.
- Resolve contradictions where evidence permits; surface material contradictions that remain.
- Do not ask participants for factual information that available authorized sources can answer.
- Do not edit, overwrite, or otherwise change source material unless explicitly instructed.

Keep evidence separate from alignment:

- Sources can establish what happened, what was recorded, what people said, and what an authoritative record currently states.
- Sources do not automatically establish what the current decision-maker believes, is willing to promise, or chooses to exclude.
- A plausible synthesis, repeated pattern, or implication is an **inference**, not a settled decision.
- Ask for confirmation of any inference that would become a central claim, commitment, boundary, recommendation, or operating rule.

Before the first interview round, provide this concise situation-brief format:

```text
Situation brief
- Sources establish: [authoritative facts, decisions, and unresolved contradictions]
- Already confirmed: [explicit current choices]
- Inferred, not confirmed: [interpretations that need confirmation]
- Central tension or missing logic: [the material gap]
- Recommended artifact: [form and short tradeoff]
- Decision-maker questions: [uncertainties only they can resolve]
```

## 4. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds already completed in the current conversation, and do not repeat answered questions.

Do not draft immediately after the first round merely because one apparent central issue has been resolved. Use a later round to test consequences: boundaries, tradeoffs, counterarguments, ownership, definitions, or execution implications.

Ask four to eight focused questions per round. If fewer than four material questions remain, ask only those questions and say that this is a narrow final check. Do not add ceremonial questions merely to reach a number.

Each numbered question should normally seek one decision. Do not combine separate decisions, such as ownership, coordination, handoffs, and success measures, into one broad yes-or-no question. Bundled questions create false alignment.

Deliver each question round once through the active conversation channel, unless the requester explicitly asks for another format or a higher-priority requirement requires one. Do not duplicate the same questions across chat and a separate form. Progress depends on the answers received, not on whether an interface still shows a question as pending.

Use a plain-text numbered block unless the requester requires a native question form. Put the updated situation model and the question block in the same message, so the respondent can answer in shorthand. Keep the block compact and single-spaced: each question and option must appear on consecutive lines, with no blank lines inside the block. Do not use artificial line-break markup.

Use this question format:

```text
1. Which direction should the document recommend?
   a. Focus first on the highest-impact problem; this narrows scope but makes accountability clear.
   b. Address all related problems equally; this is broader but may weaken prioritization.
   c. Present the choices without a recommendation; this preserves flexibility but delays commitment.
   d. Propose a short pilot before selecting a direction; this reduces risk but slows action.
2. Who should make the final decision?
   a. The accountable lead, after consulting affected functions.
   b. A cross-functional decision group with one designated tie-breaker.
   c. The executive sponsor after reviewing a recommendation.
```

Apply these format rules:

1. Number questions continuously across rounds so shorthand replies remain unambiguous.
2. For bounded choices, offer three or four mutually exclusive, decision-relevant options when that reflects the real decision. Use two options only when the decision is genuinely binary.
3. Label options with lowercase letters.
4. Put the recommended option first unless prior context makes another ordering clearer.
5. Include enough context and tradeoff information for a quick, informed answer.
6. Leave room for the respondent to reject the framing, qualify an answer, or provide another option.

Each round should:

1. Begin with an updated model of the situation and state what changed because of earlier answers.
2. Focus on one layer of uncertainty rather than mixing every issue at once.
3. Explain the tradeoff behind the recommended option.
4. Separate source-supported observations from choices participants must make.
5. Surface contradictions and ask the smallest question needed to resolve them.
6. Include a pressure test when the document is persuasive or strategically consequential.
7. Generate questions from prior answers and remaining uncertainties, not from a generic questionnaire.

A common progression is purpose; strategy; operating model; definitions and measures; then expression, format, and destination. Adapt the sequence to the work, but preserve the answer-dependent loop.

After every answer round:

1. Match shorthand and free-text answers to question numbers, preserving qualifications such as “mostly c” or “not sure.” Classify each answer as confirming, rejecting, softening, qualifying, or deferring the proposed position.
2. Trace downstream implications. A changed audience, softened commitment, new exception, or rejected framing often creates another material question.
3. Update the alignment ledger and show a concise synthesis.
4. Generate the next round from the remaining material uncertainties and their consequences.

Continue while an unresolved issue could materially change the document. If the requester explicitly asks to draft before the process is complete, name the one or two most important consequences of the remaining uncertainty, then follow the instruction.

## 5. Maintain an alignment ledger

Keep a compact working record throughout the conversation:

```text
Alignment ledger
- Confirmed: [explicit choices made by the authorized decision-maker]
- Source facts: [current authoritative facts, distinct from present choices]
- Inferred: [plausible interpretations that remain unconfirmed]
- Open: [issues that could materially change the document]
- Corrected: [rejected assumptions or claims that must not return]
```

Update this ledger after every answer round. Never reintroduce a corrected assumption. If confirmed statements conflict, surface and resolve the conflict rather than hiding it in vague language. Never promote an inference to confirmed solely because several sources support it.

For a full shaping process, show a concise version of the ledger before each later round. Every major draft claim must be a confirmed choice, a supported source fact, or explicitly framed as a proposal, assumption, or open question.

## 6. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document’s substance. Before drafting, provide this concise pre-draft synthesis:

```text
Pre-draft check
- Intended job: [what the document must cause]
- Audience: [primary readers and required action]
- Artifact: [selected form]
- Central position: [confirmed choice or clearly labeled proposal]
- Boundaries: [scope, exclusions, and key definitions]
- Deliberate open questions: [low-impact items represented in the draft]
- Readiness decision: [ready / draft on instruction with stated risks]
```

For every major planned claim, ask: **Was this confirmed by an authorized decision-maker, established as fact by authoritative evidence, or merely inferred?** If a material claim is only inferred, ask another question or label it explicitly as a proposal. Do not present it as settled.

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

For action, operating, or onboarding documents, avoid long flat inventories. Keep sections to seven top-level bullets or fewer, and preferably five or fewer for a main outcomes section. Combine related points under a clear lead phrase, cut weaker points, or move supporting detail to an appropriate reference.

Make the draft as simple as the substance allows:

- Prefer short, common words over formal or inflated language.
- Write complete, natural sentences. Keep one clear line of thought in each sentence, but do not split connected ideas into choppy fragments.
- State the point first. Remove warm-up text, repeated context, process narration, and unnecessary qualifications.
- Turn abstractions into concrete claims, actions, examples, owners, dates, or tests where useful.
- Use focused paragraphs. Use bullets only for real lists; write bullet items as full sentences unless they are compact labels.
- Prefer the more concise version when it preserves meaning. Concise writing removes unnecessary ideas and words; it does not require every sentence to be short.
- Preserve hard ideas when they matter, but explain them in plain language rather than jargon.

Honor the requested destination using the chosen system. If text is requested in the conversation, provide text without changing source material. If a document must be created or updated elsewhere, do so only as instructed and verify that the intended content is present.

When delivering a formatted document with lists, inspect the rendered result. Ensure that a heading following a list is a separate, non-list paragraph; intended bullets render as bullets rather than numbers; indentation is consistent across sections; and page breaks do not create orphaned or awkward list items. Do not insert empty paragraphs merely to separate a final list item from the next heading if the heading’s own spacing can provide separation.

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
- If formatted externally, has the rendered output been checked for list and layout failures?

Fix mismatches before delivering. Put the deliverable last, without trailing commentary that would interfere with copying or using it.

## Failure modes to avoid

- Drafting early because producing text feels productive.
- Treating the proposed artifact as fixed before its purpose is known.
- Asking participants for facts that available authorized evidence can answer.
- Using private records without a legitimate purpose, authorization, or a need for the information.
- Mistaking research volume for alignment on current choices.
- Treating a plausible synthesis as a confirmed decision.
- Using a generic questionnaire disconnected from evidence and prior answers.
- Failing to update the working model after each round.
- Stopping after one round without testing consequences.
- Bundling independent decisions into a single question.
- Repeating questions already answered or duplicating them across answer channels.
- Concealing contradictions through vague language.
- Continuing interviews after only low-impact uncertainty remains.
- Writing an inspiring document that leaves decisions, ownership, or execution unclear.
- Mistaking concise writing for choppy writing by using fragments, noun-only bullets, or artificially short sentences.
- Delivering a structurally valid formatted document without checking how it actually renders.


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
description: Learn a paper, article, post, or topic through a short Socratic dialogue that uses retrieval, explanation, and application rather than passive summary. The tutor adapts challenge to the learner’s responses and focuses on durable, usable理解.
---

# Learn with a tutor

Help a learner understand, retain, and use a provided paper, article, post, or topic through a rigorous dialogue. Prioritize active recall and reasoning over unsolicited explanation. The learner should do most of the intellectual work; the tutor guides, diagnoses, and raises the level of challenge.

## Learning principles

- **Retrieve before reviewing.** Do not give an unrequested summary. Ask the learner to recall and reconstruct ideas in their own words.
- **Ask for mechanisms.** Move beyond conclusions by asking why, how, under what conditions, and with what evidence an idea works.
- **Have the learner generate connections.** Ask for their own examples, analogies, predictions, and uses before offering any.
- **Use productive difficulty.** Challenge the learner enough to require thought, but not so much that they cannot make a meaningful attempt.
- **Practice transfer.** Move from the original material to unfamiliar cases, related ideas, and real decisions.
- **Surface gaps through questions.** When an answer is incomplete or inconsistent, use questions to help the learner notice the issue. Explain directly only after they have had a fair chance to reason it through.

## Conversation workflow

### 1. Establish prior knowledge and a learning target

Start by asking what the learner already knows, believes, or has experienced about the topic. Also identify their purpose: for example, understanding an argument, preparing for a discussion, applying a method, evaluating a claim, or remembering the material for later.

Ask one or two open questions, such as:

- “What do you already think is true about this topic, and why?”
- “What experience or related knowledge do you bring to this?”
- “What are you hoping to be able to explain, evaluate, or do by the end?”

Use the response to identify useful background knowledge, likely misconceptions, and an appropriate level of challenge.

### 2. Elicit the central idea from memory

Ask the learner to explain the main argument, finding, or idea without quoting the source.

Useful prompts include:

- “In your own words, what is the main claim?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “If you had 30 seconds to explain it to a thoughtful friend, what would you say?”

If the learner has not yet read or engaged with the material, ask for an initial prediction or working model. Then direct them to inspect the relevant section before returning to retrieval.

### 3. Choose a few important ideas and go deep

Do not attempt to cover every detail. Select two or three ideas that are central, difficult, consequential, or likely to be misunderstood.

For each idea, use this cycle:

1. Ask the learner to state or reconstruct the idea.
2. Probe their reasoning, evidence, assumptions, and causal story.
3. Ask them to generate an example, comparison, prediction, or application.
4. Test the idea with an objection, boundary case, or alternative explanation.
5. Adjust the next question based on the learner’s actual answer.

Keep turns short. Usually ask only one or two questions at a time.

## Question toolkit

Choose questions that require explanation rather than recognition. Adapt the wording to the material and the learner’s level.

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What evidence would distinguish this explanation from another one?”
- “What is the mechanism here, step by step?”
- “Can you construct a concrete example from a familiar setting?”
- “Where might this fail, or where would it not apply?”
- “What is the strongest objection to this argument?”
- “How does this connect to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one key assumption changed?”

Avoid yes-or-no questions unless they are immediately followed by a request for reasoning.

## Responding to learner answers

Be warm, direct, and specific. Do not use generic praise. When an answer is strong, identify what made it useful—for example, it named an assumption, distinguished correlation from causation, or supplied a relevant counterexample—then raise the challenge.

When an answer is wrong or incomplete:

1. Do not immediately provide the correction.
2. Point to the tension with one focused follow-up question.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, provide a concise explanation of the missing distinction or reasoning step.
5. Ask the learner to restate the corrected idea in their own words or apply it to a fresh case.

If the learner says, “I don’t know,” invite a low-stakes attempt: “Take a guess based on what you do know. What seems most plausible, and why?” Offer a hint after an attempt, or sooner if the task clearly requires missing foundational knowledge.

## Calibration and pacing

Increase difficulty when answers come easily. Ask for a counterexample, comparison, prediction, objection, or application in a new domain.

Reduce difficulty when the learner is lost. Narrow the question, isolate one assumption, introduce a simpler case, or ask them to compare a small number of explanations and defend one.

Match the learner’s energy. When they are engaged, pursue the reasoning in more depth. When they are tired or overloaded, consolidate the strongest ideas instead of introducing new material.

Maintain a dialogue rather than a test. Questions should build on the learner’s actual responses, not appear as a fixed sequence of quiz items.

## Progress checks

Periodically give a brief, evidence-based assessment of:

- What the learner has demonstrated they understand.
- What remains uncertain, incomplete, or confused.
- The most useful next focus.

Do not claim mastery because the learner recognized a term or repeated a conclusion. Look for accurate explanation, reasoning, and transfer to a new case.

## Closing gate

Before ending, ask the learner to convert learning into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation, a self-generated example, or a future retrieval prompt. End by naming the next concept or question worth revisiting.

## Guardrails

- Do not summarize the material unless the learner explicitly requests it. Even then, invite their own summary first.
- Do not lecture when a well-chosen question can prompt retrieval or inference.
- Do not define jargon automatically; ask the learner to define it first, then clarify if needed.
- Do not make the interaction easy merely to be encouraging.
- Do not cover the entire source superficially when a few core ideas can be understood deeply.
- Keep any provided source material within the learner’s authorized context. If the material includes personal or sensitive information, use only what is relevant to the learning goal and avoid repeating unnecessary details.


---
name: write-in-my-voice
description: Draft or revise emails in the user’s authentic voice by using authorized style evidence, confirmed facts, and a concise final audit. Adapt the user’s recognizable style to the recipient and stakes without inventing commitments or details.
---

# Write in my voice

Use this workflow when drafting, replying to, or polishing an email on the user’s behalf.

## Goal

Produce a copy-ready email that sounds like the user rather than a generic assistant. Match the user’s normal tone, rhythm, greeting, closing, and formatting while ensuring the message is accurate, appropriate for its audience, and easy to act on.

## 1. Load the voice profile

Before drafting, review the user’s current writing guidance in full, if available. Use only materials the user is authorized to share or access, such as a personal style guide, approved templates, or recent emails the user sent.

Build a working voice profile from the strongest available evidence:

- Usual greetings and sign-offs.
- Formality level, warmth, directness, and relationship cues.
- Typical sentence and paragraph length.
- Preferred vocabulary, contractions, punctuation, and formatting.
- Phrases, tones, punctuation, or habits to avoid.
- How the user makes requests, follows up, declines, corrects someone, apologizes, or gives feedback.
- Approved reusable facts, links, boilerplate, and standard responses.

Prefer recent sent emails over old examples, drafts, or general preferences. If examples conflict, use the most recent consistent pattern or ask the user which preference is current.

Do not inspect unrelated private communications. Use the minimum relevant examples and avoid carrying sensitive personal information, private facts, or recipient-specific details into a different message.

## 2. Confirm the email brief

Identify the smallest set of details needed to send a safe, useful message:

1. Who is the recipient, and what is their relationship to the user?
2. What outcome should the email produce?
3. Which facts, names, dates, links, attachments, decisions, or commitments must be included?
4. What tone is appropriate: warm, neutral, firm, apologetic, celebratory, or concise?
5. Is there a deadline, sensitivity, approval requirement, or access boundary?

Do not invent availability, decisions, pricing, promises, opinions, authority, emotional reactions, or factual claims. If a missing detail would materially change the meaning, ask one focused question before drafting.

## 3. Adapt voice to context

Keep the user recognizable, but do not treat voice as a rigid template.

- **Close colleagues or familiar contacts:** Use the user’s normal level of familiarity and brevity.
- **New, external, senior, or formal contacts:** Preserve the user’s directness and style while adding enough context and care to make the message clear.
- **Sensitive, corrective, or conflict-related messages:** Be factual, calm, and specific. Avoid defensiveness, excessive praise, process narration, and unnecessary apologies.
- **Requests and follow-ups:** State the action requested, responsible person, and timing clearly.
- **Reusable responses:** Use approved wording, facts, links, and templates only when they fit the situation. Do not reuse material that could mislead the recipient or disclose information outside its intended audience.

## 4. Draft the smallest complete email

Use this default structure when it fits the user’s style:

1. Greeting, if the user normally includes one.
2. Purpose or response in the first sentence.
3. Essential context, decision, request, or next step.
4. Closing and sign-off, if appropriate.

Write only what the recipient needs to understand and act. Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Put the request, decision, deadline, or next action where it is easy to find.

Use bullets only when they improve clarity for actions, choices, dates, or logistics.

Remove:

- Throat-clearing and explanations of the drafting process.
- Generic flattery or repeated thanks.
- Filler such as “just wanted to,” “I hope you’re well,” or similar phrases unless they are both useful and genuinely normal for the user.
- Hedging that weakens a message that should be clear.
- Details that are unrelated to the purpose or inappropriate for the recipient’s access level.

## 5. Audit before presenting

Review the draft line by line:

- Would the user plausibly write these exact words?
- Do the greeting, sign-off, punctuation, and rhythm match the available evidence?
- Is the tone appropriate for this recipient and situation?
- Does the email clearly state its purpose and required next step?
- Are names, dates, links, attachments, and references accurate?
- Did the draft add any claim, promise, decision, opinion, or emotion the user did not provide?
- Does it reveal only information the recipient should receive?
- Can any sentence be removed without losing meaning or usefulness?
- Does it avoid the user’s known style anti-patterns?

## Readiness gate

The email is ready only when all of the following are true:

- The intended recipient and purpose are clear.
- Material facts and commitments are confirmed.
- The wording matches the user’s available voice evidence.
- The requested action or decision is easy to identify.
- The content stays within the appropriate privacy and access boundary.

If no voice evidence exists, state the assumption briefly and use a broadly useful default: concise, clear, warm-professional, and direct. Invite the user to provide a few representative sent emails or explicit preferences for future drafts.

## Output format

Provide the final email as copy-ready text. If clarification is required, ask only the specific question needed to draft safely. Do not add explanation after the final copy unless the user asks for alternatives, rationale, or edits.


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
description: Create an evidence-based case study post about a person’s professional, learning, or career change, with a review-ready draft, alternate hooks, quote-card options, approvals, and verification checks.
---

# Write a case study post

Use this workflow to turn source material about a person into a concise, credible public case study. It works especially well for professional social posts, and can also be adapted for newsletters, community updates, program stories, recruitment pages, or customer stories.

The purpose is not to praise someone vaguely. Show a specific and supportable change: where they started, what they were considering, what they did, what concretely helped, what happened next, and what a relevant reader can do.

A strong post lets the target reader recognize their own situation in the subject’s before-state. It explains the role of a program, community, product, or resource without overstating causation.

## Purpose, authorization, and access boundary

Use personal communications, application materials, interview notes, employment details, or other records only for a legitimate publishing purpose and with clear authorization from the relevant organization and subject.

Use the minimum information necessary to tell the story. Exclude unrelated personal details, sensitive background information, and claims outside the intended audience or publication boundary. Do not publish private facts merely because they appeared in source material.

Before beginning, establish:

- The publishing organization or account.
- The intended audience and desired reader action.
- The approved source material and who may access it.
- Whether the subject has approved the story, or which items still require approval.
- The publication channel and any platform-specific constraints.
- The relevant editorial voice guide, if one exists.

## Inputs

Gather all available source material. Useful inputs include:

- An interview transcript, recording notes, or meeting summary.
- An application, intake form, or written statement from the subject.
- A current professional profile, biography, or official announcement.
- Public projects, publications, products, grants, placements, or work samples.
- An internal message reporting a result, where authorized for this use.
- A prior draft, rough outline, or notes from the subject or editor.
- The target audience, platform, and desired call to action.
- An editorial or brand voice guide.

Before drafting, check whether the following information is sufficient and verified.

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns, and consent status. |
| Before-state | Previous role, field, goal, uncertainty, or practical constraint. |
| Alternative path | What they were considering or doing instead, if relevant to the reader. |
| Trigger | Why they joined, applied, changed direction, or acted at that time. |
| Intervention | The program, community, resource, event, mentor, or product involved. |
| Mechanism | Concrete things that helped, such as a realization, opportunity, introduction, feedback session, or resource. |
| Now-state | Current role, team or organization if approved, current work, and practical outcome. |
| Timeline | Dates or intervals from starting point to outcome. |
| Evidence | Verified titles, figures, artifacts, quotes, and source references. |
| Cost or risk | Any career, financial, geographic, or personal tradeoff that is both relevant and approved. |
| CTA | The exact next action for the reader. |

If critical details are missing, ask focused questions before writing. Never guess at names, organization names, job titles, dates, paper or project titles, compensation figures, timelines, or outcomes.

Useful questions include:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they take part or make a change at that moment?
4. What were the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a public project, placement, publication, product, or result worth naming?
8. Did they take on a meaningful cost or risk that they are comfortable sharing publicly?
9. Which names, figures, claims, and direct quotes are approved for publication?
10. Who should this post persuade or help, and what should they do next?

## Evidence and verification rules

Never invent facts or upgrade a claim to make it stronger. If a source says someone contributed to a project, do not call them the lead. If they explored an opportunity, do not say they received it. If a work is unpublished, do not present it as published.

Treat automated transcripts and summaries as useful but fallible. They can mishear names, organization names, technical terms, numbers, titles, and dates. Cross-check important details against a more reliable source, such as direct subject confirmation, an official public record, a current professional profile, an approved application, or published work.

Use this general reliability order when sources conflict:

1. The subject’s direct and recent confirmation.
2. Official public records, published work, or formal announcements.
3. A current professional profile.
4. An original written application or statement from the subject.
5. Interview transcripts, meeting notes, or automated summaries.
6. Informal third-party messages.

Keep three categories separate in working notes:

- **Verified fact:** A role, date, artifact, figure, or quote supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion the writer draws. Use this only when evidence supports it, and phrase it carefully.

Do not claim that an intervention caused an entire outcome unless the evidence clearly supports that conclusion. Prefer precise statements such as “the program helped them understand the field,” “they found the opportunity through the community,” or “a conversation clarified the next step.”

## Sensitive-content approval gate

Flag the following for explicit subject approval before publication:

- Salary, compensation changes, financial hardship, or pay comparisons.
- Health, family, legal, immigration, or other sensitive personal circumstances.
- Harsh descriptions of a past employer, role, or career decision.
- Unreleased work, confidential projects, unpublished titles, or internal information.
- Direct quotes, especially criticism, strong opinions, or emotionally charged language.
- Claims about why another organization hired, selected, or promoted the person.
- Strong causal claims or impact claims that cannot be independently verified.
- Dates or timelines that could expose private circumstances.

If approval is not available, use an honest approved fallback. For example, an approved general statement such as “they accepted a lower-paying role” may replace a precise compensation comparison. Do not make the story more dramatic to cover uncertainty.

## Build the story beats

Create a concise private working outline before drafting. Do not expose raw sensitive notes in the public draft.

### 1. Before-state

Capture the subject’s role, background, and reader-relevant uncertainty. Include the alternative path they were considering when it resembles the audience’s current life.

Keep only details that move the story. A long list of credentials, reading, or earlier jobs usually weakens the post. Keep a detail when it explains the person’s decision, makes the change concrete, or helps the reader recognize themselves.

### 2. Trigger

Identify why the subject acted at that time. They may have wanted to understand a field, test whether a career path was open to them, find collaborators, solve a practical problem, or make a values-driven decision.

### 3. Mechanism

Find the one or two observable things that changed the trajectory. Strong mechanisms include:

- Realizing a field or role was accessible.
- Finding a relevant opportunity through a community.
- Having a conversation that clarified a next step.
- Receiving feedback that improved an application, project, or plan.
- Being introduced to a collaborator, mentor, or hiring contact.
- Using a workshop, resource, or tool that made action possible.

Avoid vague claims such as “the experience was transformative.” Say what happened instead.

### 4. Now-state

Record the current role, approved organization or team name, and what the person actually does. Translate jargon enough for the intended reader to understand why the work matters.

Use named outputs only when they add proof or interest. One meaningful project, publication, placement, product, or grant often does more work than a long credential list.

### 5. Timeline and compression

Map the sequence from joining or starting to the present result. Use a short truthful interval, such as “within six months” or “the following year,” when it sharpens the story. Do not force a compressed timeline if the facts do not support one.

### 6. Quotes

Pull three to five verbatim quote candidates. Favor lines that speak to the reader’s possible identity or uncertainty, rather than only celebrating the subject’s outcome.

Look for three categories:

1. **Discovery:** A line about not knowing a path was available.
2. **Mechanism:** A line about the opportunity, conversation, or resource that helped.
3. **Conviction:** A line about why the decision mattered or why they would make it again.

Light trimming is acceptable only when it preserves the original meaning and grammar. Never rewrite a quote into language the subject did not use.

## Generate three hook options

On feed-based platforms, the first two lines determine whether readers continue. Write three distinct hooks before drafting the full post. Keep each to two short sentences. Where useful, aim for roughly 140 characters total.

### Hook A: Discovery

Use this when the audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a surprising concrete mechanism.

This is often the best default because the first line mirrors the reader’s own uncertainty.

### Hook B: Identity collision

Use this when the before-and-after contrast is vivid and easy to understand.

**Formula:** A short time ago, the subject was doing one specific thing. Today, they are doing a sharply different specific thing.

This is useful for broad audiences who may not share the subject’s exact blocker.

### Hook C: Stakes-led

Use only when a meaningful cost or risk is approved and readers are likely to interpret it as honest conviction, not as a warning that participation requires hardship.

**Formula:** The subject accepted a specific cost to do something. Now they are taking a concrete action or doing meaningful work.

Choose one recommendation. Give one short reason it fits the audience and one short reason each alternate is less suitable. Default to Discovery when the post aims to help readers see a path that they did not know was open to them.

## Draft the post

Aim for about 160 to 220 words unless the platform or audience calls for another length. Shorter is often stronger.

Use this sequence:

1. **Hook:** Use the recommended hook.
2. **Before-state:** One short paragraph showing the previous situation and a relevant alternative path.
3. **Name the intervention:** State clearly that they joined the program, used the resource, or entered the community. Do not leave its role implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then land the immediate result in plain language.
5. **Current work:** Describe what they do now and why it matters in terms the reader can understand.
6. **Optional honest cost:** Include only if approved and genuinely useful.
7. **Optional pull quote:** Include only if it introduces a distinct truth that the hook and body do not already convey.
8. **CTA:** Address the reader directly and give one clear next action.

If the publishing platform may reduce distribution for posts containing external links, put the link in a comment, profile destination, or other approved location rather than the post body. Treat this as a platform and publishing decision, not a universal rule.

## Style rules

Adapt to the chosen editorial voice. When no voice guide exists, use these practical defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use concrete names, roles, dates, and figures only when verified and approved.
- After the first full introduction, use the subject’s preferred short name if the tone and consent make that appropriate.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not call the subject exceptional, inspiring, or brilliant without showing why.
- Use contractions when the voice is conversational.
- Keep the CTA in full second person: “If you are…” and “you can…”
- Avoid emojis unless they are an explicit brand choice.
- Do not use em dashes. Use periods, commas, or line breaks instead.

On the final edit, remove machine-like phrasing. Cut empty transitions, dramatic setup frames, filler intensifiers, hedging, abstract nouns that replace evidence, balanced “on one hand, on the other hand” constructions, and reflective summaries after the CTA.

Avoid corporate or generic phrasing such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm” unless it is necessary in an approved direct quote.

Read the post aloud. If it sounds like a generic thought-leadership template, shorten it and replace abstractions with specific facts.

## Graphic quote options

Provide three options for a visual quote card. Each should be self-contained, preferably under 15 words, and drawn verbatim from approved source material.

Provide one quote from each category:

- Discovery.
- Mechanism.
- Conviction.

Recommend one quote. Discovery quotes are usually strongest because they work without context and mirror the reader’s uncertainty. Choose a mechanism or conviction quote instead only if it is clearer, more memorable, and understandable on its own.

## Readiness audit

Before sending the draft for review, confirm:

- Every name, role, date, figure, and title is verified.
- Important transcript-derived details were cross-checked.
- The story shows a concrete mechanism, not only a result.
- The wording does not overstate causation.
- The intervention is named clearly.
- The opening reflects a real audience concern.
- The current work is understandable to the intended reader.
- Sensitive claims and quotes are approved or clearly flagged.
- The CTA is clear and directed at the intended reader.
- There are no em dashes, unsupported superlatives, corporate phrases, or generic filler.
- The post stays within the agreed privacy, consent, and access boundary.

## Delivery format

Create the draft in the user’s chosen document system when available. Use a clear title format such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and two alternatives.
- The three graphic quote options and the recommendation.
- A list of approval items.
- A list of missing information that would strengthen the post.
- The document location or link, if applicable.

Do not treat the first draft as final. If feedback says “make the hook better,” generate new hooks rather than making minor edits to the old one. If asked to make the post shorter, cut secondary biography first while preserving the mechanism and outcome. If a subject rejects a sensitive line, replace it with the approved fallback without weakening the whole story.

After final acceptance, review feedback for reusable lessons. Update the workflow only when a recurring pattern is clear, such as a missing intake question, a consistent voice preference, a repeated structural change, or a verification gap. Do not invent process changes after a clean review cycle.


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
description: Create or improve a short, paid, asynchronous work sample that produces role-relevant evidence, can be reviewed efficiently, and is validated through realistic simulated submissions.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A good work sample gives candidates a bounded, realistic version of relevant work and gives reviewers evidence that resumes and interviews may not reveal.

Use this for a new exercise or an existing exercise that needs improvement. Do not use it for interview questions, application-form screeners, live assessment centers, or multi-day work trials. If the requested format is unclear, ask once which format is intended.

## Purpose and design principles

A work sample usually follows initial screening and precedes later interviews or a longer trial. Its purpose is narrow: assess a small number of role-critical capabilities under realistic constraints.

Do not try to assess the whole person or every requirement of the role in a short asynchronous task. Other stages may provide better evidence:

- Interviews can assess live communication, motivation, collaborative reasoning, and follow-up judgment.
- References can assess reliability, integrity, and sustained performance.
- A longer trial can assess consistency, judgment over time, and work in real systems.
- Training can often address familiarity with a particular tool, internal process, or nonessential domain vocabulary.

A strong work sample should:

- Be paid, with payment terms disclosed before work begins.
- Have a clear expected time limit, commonly two to four hours.
- Assess capabilities that materially relate to the role.
- Be self-contained. Candidates should not need private-system access, confidential data, or unavailable infrastructure.
- Use a fictionalized or safely anonymized scenario unless use of real public information is authorized.
- Avoid producing free work for the organization. Any intended use beyond assessment requires separate agreement.
- Take about 20 to 25 minutes to review per submission.
- State whether AI tools are permitted and assess judgment, reasoning, and usefulness rather than attempting to infer AI use from prose style.
- Provide a route for reasonable accommodations or an accessible equivalent format while preserving the role-relevant standard.

When reviewing internal records, project materials, or communications to build the exercise, use them only for a legitimate hiring purpose and with clear authorization. Read the minimum relevant material. Keep working notes and outputs within the approved hiring access boundary. Exclude unrelated personal information and sensitive details.

## Step 1: Pre-flight

Before designing the exercise, confirm that the hiring team has both of the following:

1. A current job description or role brief describing responsibilities, expected outcomes, reporting context, and level.
2. A role-success profile, hiring plan, or equivalent document identifying the capabilities and experience most important for success.

If either is missing, stop. Do not try to establish the role-success profile while drafting the exercise. That creates a moving target and usually produces an assessment that feels plausible but measures the wrong things.

Use this request:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

Once both exist, read the relevant role context. This may include project constraints, examples of successful work, prior hiring feedback, and one or two comparable exercises. Reference exercises are useful for calibrating tone, length, and delivery format, but do not copy their task shape automatically. Different roles need different evidence.

Give a short status update after review. For example:

> Read the role brief, success profile, and two reference exercises. Moving to the alignment memo.

## Step 2: Write the alignment memo before drafting

Do not write candidate-facing instructions yet. First produce a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five capabilities that the role succeeds or fails on and that a short asynchronous exercise can genuinely surface. Phrase them as observable performance, not broad virtues.

Weak: “Strategic thinking.”

Better: “Can identify the highest-leverage problem in a messy operating situation, explain the tradeoff, and deliver a useful first action.”

### What the exercise will not test

Name important criteria that belong elsewhere. A short written exercise may not fairly assess sustained reliability, leadership over months, live collaboration, specialized software fluency, or motivation for the organization’s mission.

This section prevents scope creep and makes the assessment’s limits explicit.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level. Explain what this changes:

- Entry-level candidates may need more context and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make tradeoffs, set direction, and create artifacts another person could use without further explanation.

### Failure modes the exercise should catch

Identify two or three observable patterns that could lead to weak role performance but may be missed in ordinary screening. Examples include:

- A polished planner who does not ship usable work.
- A fast executor who misses the central problem or creates avoidable risk.
- A careful candidate who defers every meaningful decision.
- A technically capable candidate who cannot communicate for the intended audience.

Describe work patterns, not identities, backgrounds, or personality labels.

### What strong looks like

Write one paragraph describing the evidence in a top submission: what it notices, what choices it makes, how it handles uncertainty, and what useful outputs it produces.

Present the memo and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the accountable hiring owner confirms or changes the memo.

## Step 3: Propose exercise shapes

Once the memo is approved, propose three possible exercise shapes. Each option must test the agreed capabilities in a meaningfully different way, be understandable within about a minute, be self-contained, and be scorable quickly.

For each option, provide:

- **Shape:** A plain-language description of the task.
- **What it tests:** The agreed load-bearing capabilities.
- **Why it is evaluable:** The evidence reviewers will see and why it supports reasonably consistent scoring.
- **Main risk:** The primary way the format could introduce noise, unfairness, or weak evidence.

Keep each option concise. Useful shapes include:

- **Triage pile:** Candidates receive messages, requests, and constraints; prioritize the work; draft responses or outputs; and recommend one systemic improvement. This suits operations, coordination, support, and communications-heavy roles.
- **Choose the highest-leverage action and ship it:** Candidates receive several possible priorities, select one, explain the choice, and create a small usable output. This suits strategic operations and builder roles.
- **Diagnose and fix:** Candidates assess a messy situation, identify the key problem, and produce one targeted intervention. This suits product, program, analytical, and process-improvement roles.
- **Source and pitch:** Candidates define a target profile, identify promising channels or prospects from supplied information, and draft outreach. This suits recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** Candidates assess supplied evidence and make a recommendation for a decision-maker. This suits research, policy, strategy, and specialist roles.
- **Design a repeatable system:** Candidates create a lightweight process, playbook, or operating artifact that a teammate could use. This suits program, enablement, community, and operational-design roles.

Do not draft the full exercise until the hiring owner selects a shape. If none fits, propose three more grounded in the approved memo rather than forcing a familiar format.

## Step 4: Draft version 1

Use this structure and adapt it to the chosen shape.

```markdown
# [Role] Work Sample

This work sample assesses your ability to [two or three observable role-relevant capabilities].

You have approximately [time limit] to complete it.

**Your mission**

[Describe a specific situation and its important constraints. If decisiveness is being assessed, state which stakeholders are unavailable during the exercise. End by restating what the candidate will produce.]

**Deliverables**

[Two to four substantive outputs, with rough time guidance where useful.]

**Context**

[Provide the minimum information required: project state, audience, policy, resources, and stakeholder availability.]

**Instructions**

- Spend approximately [time limit] completing this work sample.
- Submit within [deadline] of receiving the exercise.
- Submit [format and method].
- This is a paid work sample. We will pay [amount, eligibility, and timing].
- You may use [permitted tools, including the AI policy].
- Briefly state material assumptions where needed.
- Submit what you have if you do not finish. You may note what you would do next.
- [Optional: Include a short informal walkthrough video if it would add useful evidence.]

**Anticipated questions**

- If a requirement is unclear, make a reasonable assumption and state it briefly.
- If you do not finish in the expected time, submit your work and explain where you got to.
- The work will be used only to evaluate candidates for this role unless another use is agreed separately.
```

For many operational roles, a useful pattern is a short prioritization or analysis section, several substantive drafts or decisions, and one reusable process improvement. Avoid many micro-tasks. A few meaningful outputs reveal more than dozens of shallow decisions. If planning and execution both matter, tell candidates not to spend all available time on planning.

For a triage-pile exercise, provide roughly eight to ten realistic items. Connect some items so candidates are rewarded for recognizing patterns across the situation, rather than merely processing volume. Add reference notes for any policy, capacity, escalation, or resource data needed to make fair decisions.

### Candidate-facing format and content checks

Write in direct, plain language and use the locale appropriate to the organization. Before sharing, check that the candidate-facing text:

- Works in the selected applicant-tracking system or document format.
- Avoids tables and divider lines if the destination editor renders them poorly.
- Uses simple headings and bullets.
- Avoids generic slogans, forced contrasts, repetitive rhetorical patterns, and unnecessary flourishes.
- Uses clear deadline wording, such as “by the end of [day]” where applicable.
- Uses fictional names, domains, and email addresses in fictional scenarios.
- Uses the destination system’s supported soft-break method for multi-line message metadata.
- Contains no confidential information, credentials, private contact details, or sensitive internal data.

After every draft, include a separate section:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets on choices worth reviewing, such as whether a scenario item is too obvious, whether a constraint is realistic, whether payment fits the role, whether an output is too prescriptive, or whether a video should be optional.

End with one focused question, for example: “Which part should we tighten first?”

## Step 5: Iterate with the hiring owner

Expect several feedback rounds. For every revision, provide the complete updated work sample, not merely a change list, so it can be copied directly into the selected system.

Apply feedback unless it would materially undermine assessment validity, fairness, privacy, accessibility, or safety. If it would, explain the concern once, offer a practical alternative, and let the accountable hiring owner decide.

Common revisions include tightening vague instructions, loosening overly prescriptive deliverables, correcting scenario facts, simplifying outputs, changing payment, and improving accessibility or formatting.

## Step 6: Simulate two submissions

Before declaring version 1 complete, simulate two full candidate submissions using the exact candidate-facing instructions and stated time limit.

### Role-aligned simulation

Use a persona based on the approved role-success profile. Have them complete the actual deliverables and add a short reflection on choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest, capable candidate who could perform well in many hiring processes but does not demonstrate one central capability required by this role. Choose a job-relevant difference, such as planning rather than building, excessive caution where decisive judgment is required, or execution without systems awareness. Do not base the distinction on identity, background, or protected characteristics.

Have this persona complete the same deliverables.

Then synthesize:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both submissions looked similar.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by likely impact.

A floor check that both simulated candidates pass is not automatically a problem. The central question is whether the intended capabilities produce distinguishable, role-relevant evidence.

## Step 7: Apply validation improvements

Revise the complete exercise based on the simulation. Prioritize weak diagnostic points. Useful changes may include:

- Connecting scenario items so cross-item pattern recognition matters.
- Removing obvious noise that takes seconds to dismiss.
- Adding a concrete constraint that forces a meaningful tradeoff.
- Replacing a broad opinion prompt with a usable deliverable.
- Clarifying reviewer criteria so the intended evidence is rewarded.
- Removing specialized knowledge requirements that are trainable and not essential at the point of hire.

Do not make the task harder solely to make it more selective. Make it more diagnostic of the approved capabilities.

## Step 8: Optional external review

If another reviewer provides feedback, assess each suggestion against the alignment memo. Identify what to integrate, what to skip, and why. External feedback is evidence, not an automatic instruction. The hiring owner remains accountable for the assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The job description and role-success profile are confirmed.
- The alignment memo is approved.
- The task shape maps directly to the load-bearing capabilities.
- A qualified candidate can complete the task in the stated time.
- The scenario is self-contained and does not require private access.
- Payment, submission, AI-use, and accommodation instructions are clear.
- A reviewer can evaluate a submission in approximately 20 to 25 minutes.
- A role-aligned and a plausible role-misaligned simulation were completed.
- Simulation findings led to appropriate revisions.
- The final exercise contains no sensitive data and does not create unpaid production work.
- The exercise assesses role-relevant evidence and has been checked for irrelevant proxy criteria.

## Common failure modes

Avoid these patterns:

- Drafting the exercise before agreeing what it should measure.
- Testing specific tool familiarity, domain trivia, or easily trainable knowledge instead of durable judgment.
- Asking for too many small outputs instead of a few meaningful ones.
- Making every scenario item independent, which tests throughput but not pattern recognition.
- Letting candidates defer every important decision to an available stakeholder when decisiveness is the intended capability.
- Giving vague context that rewards insider knowledge.
- Providing word-count targets that encourage padding.
- Creating a test that takes longer to review than its evidence justifies.
- Treating polished writing or presentation as the main signal when the role requires another kind of performance.
- Declaring success without checking whether the assessment distinguishes the role-relevant evidence it was designed to measure.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, understandable, respectful of candidate time, and useful for making a hiring decision.


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
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and private data, verifying rendered page state, and separating preparation from consequential commitments.
---

# Use a browser safely

Use this workflow for tasks that need real interaction with a website: completing forms, changing settings, collecting data from rendered pages, testing a user flow, or working in an authenticated dashboard. Use it when a simple page request, supported API call, or static-page retrieval cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not perform a consequential final action until the page state, target, and authorization are clear.

A browser automation command succeeding does **not** prove that a website accepted the change. Modern web applications may keep state separately from the visible DOM, commit only after focus leaves a field, replace controls during a re-render, or show a cosmetic error after an action has already completed.

## 1. Establish purpose, authority, and task boundary

Before accessing a site, identify the requested outcome and the limits of the request:

- The exact target page, record, form, setting, or workflow.
- The information to enter, collect, change, or upload.
- The minimum information necessary to complete the task.
- The intended account, organization, environment, and browser profile.
- Whether the final action is reversible.
- Whether it sends, publishes, pays, deletes, grants access, changes a plan, or creates another external commitment.
- Missing information, ambiguous choices, and fields requiring the user's judgment.

When the work involves private communications, records, dashboards, or information about people, require a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not collect, expose, retain, or report unrelated personal details. Keep screenshots, logs, exports, and results within the requester’s appropriate access boundary, and respect consent and reasonable privacy expectations.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and collecting a preview are usually preparatory. Submitting, sending, publishing, purchasing, deleting, or applying an irreversible account change is a commitment.

## 2. Choose the least invasive route

Use the first suitable method in this order:

1. **Supported direct interface or API.** Prefer a documented and authorized programmatic interface when it can safely perform the task.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, and tasks that do not require the user’s established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when a live signed-in session, single sign-on state, account-specific dashboard, or user-directed browser context is genuinely required.

Before driving a browser, look for a direct route. Check official documentation, ordinary form actions, page source, and visible network activity for supported endpoints. Many forms submit structured data to an authorized service; using that service may be more reliable than reproducing browser interactions.

Do not use undocumented interfaces to bypass access controls, consent boundaries, terms, or site protections. Do not use an authenticated visible session merely for convenience: it can interrupt the user’s work and creates more privacy and account risk.

If a site blocks automation, do not try to evade its protections for casual research or data collection. A visible authenticated session may be appropriate only when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and the established session is necessary. Do not weaken browser security, multi-factor authentication, warnings, access controls, or anti-abuse protections.

### Tool selection principles

Choose an automation capability that is stable enough for the task. A lightweight browser integration can be suitable for a small number of simple actions or a short page inspection. Use a direct script with a well-supported browser automation library for long text, complex client-rendered pages, repeated form interaction, or a task requiring structured dumps and screenshots.

If the automation layer crashes, closes the page, mishandles complex rendering, or cannot reliably verify state, do not repeatedly attempt to rescue the same broken session. Switch to a more robust authorized method, restart from a known state, and re-check the task boundary.

## 3. Protect browser and account context

When taking control of a visible browser, announce that control and the purpose before acting. Do not take over silently. Once visible access is authorized for the task, proceed without repeatedly asking the user to open windows or approve ordinary navigation.

Use a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab. This reduces the chance of disrupting unrelated work or acting on the wrong page.

Before changing data in an authenticated context:

1. Classify the intended context explicitly: for example, personal, work, testing, staging, or production.
2. Select the browser profile or connection matching that context. Do not rely on a generic browser selector, remembered default, window title, or arbitrary connection label.
3. Verify the signed-in account through a reliable account indicator before opening or changing the real target.
4. Confirm the target object, record, recipient, or environment.
5. If the required account, environment, target, or authority is uncertain, stop and ask before changing data.

Do not reveal credentials, session tokens, recovery information, private account data, or security settings in output or logs. Do not disable security controls to make automation easier.

If an automation environment provides an account-verification gate or marker before write actions, mark the context verified **only after** the account check passes. Never create or enable a verification marker in advance merely to unlock actions.

A useful pre-action question is: **Which account is this? Which environment is this? What exact item will change?** Resolve uncertainty before proceeding.

## 4. Inspect the rendered page before editing

Do not begin by guessing selectors, filling controls by numeric position, or trusting a visual approximation. First inspect the rendered page and collect enough structure to identify the relevant controls safely.

For each relevant control, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether the field is required.
- Validation rules, character limits, formatting behavior, and disabled state.
- Whether an apparent field is the editable control, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, tab, or date causes the page to re-render.

Address controls by stable semantic identity, such as visible label text, accessible name, or label relationship. Do not use DOM indexes where labels are available: dynamic applications can change element order after loading or re-rendering.

Before changing a record or setting, inspect the current state. This prevents changing the wrong item or overwriting existing values unintentionally.

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

## 5. Use the correct interaction for each control

Different controls need different interactions. A generic “set value” operation is not reliable for all of them.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use the normal text-input mechanism | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus it, select existing content, enter text through keyboard-style events, then blur | Direct DOM mutation may not update the application’s internal model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle | Selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed | A click can toggle an already-correct value. |
| Date/time picker | Choose date and time, then verify the rendered summary | Popovers can reinterpret typing or clear related fields. |
| File upload | Confirm file, destination, and privacy implications first | Uploading may begin immediately and can be difficult to undo. |

For framework-driven editors, simulate ordinary user interaction rather than writing directly to low-level page properties. A robust general sequence is:

1. Focus the actual editable element.
2. Select any existing content.
3. Delete it.
4. Enter the new text using keyboard-style events.
5. Move focus to a neutral page element.
6. Wait briefly for the application to commit state.
7. Read the result back.

Some forms pair a visible rich-text editor with a hidden input. Editing the hidden input may appear successful in a DOM dump while server-side validation treats the visible editor as empty. Target the control the user interacts with and that the application actually reads. If a generic accessibility locator finds an empty wrapper, inspect the underlying labeled editable element.

If a dropdown, checkbox, date control, tab, or other selection may refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterwards and confirm prior entries remain present.

## 6. Verify after every meaningful edit

After each field is filled or setting is changed, read its value back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare lengths, required state, or a minimal redacted summary instead of exposing full content unnecessarily.

Check for these common mismatches:

- The automation layer reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displayed text but did not retain it internally.
- A later edit erased an earlier field after a re-render.
- A hidden synchronization field was changed instead of the visible editor.
- A selection changed a dependent field, date, recipient, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once using a more appropriate interaction method, then verify again. If the page still rejects or alters the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

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

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only through an appropriate access boundary. Avoid exposing sensitive form values in a large inline table when a short summary and a securely available record are sufficient.

### Readiness checklist

- [ ] The account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 8. Treat consequential actions as a distinct phase

Use two phases for consequential tasks:

1. **Preparation pass:** Fill or configure the page, verify all values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Re-check the account, target, and readiness gate, then perform the final action once authorization is established.

Payments, sends, publication, deletion, access grants, subscription or plan changes, and actions labeled permanent, final, or impossible to edit later require explicit confirmation immediately before the final control, unless the user has already clearly authorized that exact final action in the current task or applicable standing instruction.

For a confirmation request, state only what is necessary: target, important values, recipients or audience, cost if any, irreversible effect, and open questions. Do not ask again for a send or publish that the user already specifically approved. For low-risk reversible changes explicitly requested by the user, such as updating a preference or preparing a draft, proceed after normal verification unless the page reveals an unexpected broader impact.

If the page reloads, re-renders, or the session changes between preparation and commitment, do not assume earlier state remains valid. Restore and verify the intended values again before committing.

## 9. Confirm completion after acting

A button click is not proof of success. After the final action, look for reliable evidence such as a success message, confirmation reference, newly created record, persisted saved setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Never represent an attempted action as completed.

## 10. General failure patterns and recovery rules

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after a later edit | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline or rich-text control, or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control that the application actually reads. |
| A selection clears or changes other fields | The selection triggers a dependency or full re-render | Make selections first, then re-inspect and refill only after state settles. |
| Automation becomes unstable on a complex page | The chosen automation layer is unsuitable | Switch to a more robust browser method or supported direct interface; restart from a known state. |
| Headless and visible browsers show different behavior | The site varies by browser context | Prefer an authorized direct interface; if needed for an explicit task, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior | Close it through a neutral page action and re-verify all affected fields. |
| A visible error may be cosmetic | The action may already have completed | Inspect the resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## 11. Maintain the workflow responsibly

After a real failure or a newly validated pattern, capture the lesson in a concise reusable form: symptom, likely cause, and safe fix. Consolidate recurring lessons rather than accumulating a long list of one-off incidents. Keep environment-specific commands, account mappings, local paths, and personal operating details out of the general workflow.

Re-check tool and browser capabilities as they evolve. Update assumptions about supported controls, authentication behavior, and automation reliability in place rather than treating old implementation details as permanent rules.

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
- [ ] Explicit confirmation was obtained before an irreversible final action unless exact prior authorization covered it.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: A complete workflow for designing, testing, improving, validating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Create, revise, test, and package reusable AI skills: focused instruction sets and optional resources that help an AI perform a recurring job reliably. Use this workflow for a new idea, an existing skill, a repeated workflow demonstrated in conversation, or a request to evaluate whether a skill actually improves results.

The core loop is:

1. Understand the intended job and its boundaries.
2. Draft or revise the skill.
3. Test realistic user requests.
4. Review outputs with the user and measure objective requirements where appropriate.
5. Improve the skill based on evidence.
6. Repeat until the skill is useful, reliable, and not merely fitted to the test examples.
7. Optionally improve the description that determines when the skill should activate.
8. Package and hand off the final skill.

Do not force every project through every stage. Some users want a quick collaborative draft; others need a rigorous comparison. Identify the current stage and help the user make the next useful decision.

## Communication principles

Match the user's level of technical familiarity. Use plain language by default. Terms such as *evaluation* and *benchmark* are usually acceptable if briefly defined when helpful. Do not use terms such as “JSON,” “schema,” or “assertion” without explanation unless the user clearly works with them already.

Explain why a question matters. For example:

> What should a successful result look like: an answer in chat, a structured report, a file, or an action? This determines how we check whether the skill completed the job.

Keep the user involved in consequential choices:

- Confirm the job before writing a large instruction set.
- Ask before choosing a restrictive scope, required tool, approval policy, or external action.
- Share proposed test prompts before relying on them.
- Let human review lead for subjective outcomes such as writing quality, visual design, tone, and strategic usefulness.

If the skill will access communications, records, files, or systems containing information about people, first establish a legitimate purpose and clear authorization. Use only the minimum relevant approved sources, omit unrelated sensitive details, respect consent and privacy expectations, and keep the output within the appropriate access boundary.

## 1. Determine the starting point

First identify which situation applies.

### New skill

The user has an idea such as “I need consistent project update reports.” Start with discovery, scope, and a first draft.

### Existing skill

The user has an existing instruction file or installed skill and wants it edited, simplified, tested, or improved. Read the current instructions before proposing changes. Preserve its established name and identity unless the user explicitly requests a rename.

If the installed copy is not writable, work from a writable copy. Do not modify the original until the user approves or the environment makes the intended destination clear.

### Workflow demonstrated in conversation

The user may ask to “turn what we just did into a skill.” Extract what is already known before asking repeated questions:

- Inputs and source material used.
- Tools or capabilities used.
- Sequence of decisions and actions.
- User corrections and preferences.
- Observed input and output formats.
- Acceptance criteria and exceptions.

Summarize the inferred workflow and list the gaps for confirmation. Do not silently turn a one-time workaround into a general requirement.

### Evaluation or optimization request

The user may already have a finished-looking skill and want evidence that it helps. Go directly to test design, comparison, review, and targeted revision. Do not rewrite merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough information to define a coherent, reusable job. Adapt these questions; do not ask them mechanically.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Trigger:** What requests, phrases, or contexts should cause it to activate?
3. **Inputs:** What information, files, examples, systems, and permissions can it use?
4. **Outputs:** What should it produce, change, or recommend? Is a format required?
5. **Success:** How will the user decide the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask, stop, decline, or return work to the user?
7. **Variations:** What common cases, difficult cases, and exceptions matter?
8. **Dependencies:** Does it need particular capabilities, reference documents, templates, scripts, or approved access?
9. **Testing:** Should representative requests be used to test it?

Start with missing answers that most affect the design. Offer useful choices where appropriate:

- Should the skill make a best effort when information is missing, or ask before proceeding?
- Should it produce a concise answer, a detailed report, or offer both?
- Should it use any available source, or only sources explicitly approved by the user?
- What actions require confirmation because they are external, irreversible, expensive, or high impact?

Recommend testing when the skill is repeated often, has consequential outcomes, produces files or transformations, has objective requirements, or will be handed to others. For highly subjective work, lightweight examples and human review may be more useful than formal metrics.

### Research before drafting

If relevant approved documentation, existing skills, examples, standards, or reference materials are available, examine them before drafting. Use research to reduce burden on the user, not to replace their authority over requirements.

Research may identify:

- Existing conventions and output standards.
- Tool or file-format constraints.
- Reusable patterns from similar work.
- Privacy, safety, legal, compliance, or approval requirements.

If sources conflict or a requirement remains uncertain, surface the uncertainty rather than inventing a rule.

## 3. Choose a skill structure

A skill should be focused enough that a user and an AI can predict its behavior. Keep related variants together only when they share inputs, permissions, and a definition of completion. Split unrelated work into separate skills.

A typical package might contain:

```text
skill-name/
├── SKILL.md          # Core instructions
├── scripts/          # Optional deterministic helpers
├── references/       # Optional detailed documentation
├── assets/           # Optional templates or reusable files
└── evals/            # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata or listing text:** A short name and description used to decide whether to activate the skill.
2. **Core instructions:** The workflow needed in most cases.
3. **Supporting resources:** Detailed references, templates, or scripts loaded only when relevant.

Keep core instructions readable. If they become long, move specialized detail into clearly named resources and state exactly when to consult each one. Give large reference files a table of contents or another navigable structure.

For skills supporting several platforms, domains, or variants, put selection logic in the core instructions and variant-specific material in separate references. Read only the relevant reference rather than loading everything.

### Bundle deterministic repeated work carefully

If several test runs independently recreate the same conversion, validation, calculation, or file-generation procedure, consider bundling a script or template. This is appropriate when the work is repeatable, safer, easier to validate, and likely to recur.

Document for each helper:

- Its purpose and permitted use.
- Required inputs and expected outputs.
- How failures are reported.
- When the AI should use it and when it should not.

Do not automate access, data collection, or external changes beyond the user’s authorization. Do not bundle automation simply because it is technically possible.

## 4. Write the skill

Write in clear imperative language. Explain the reason behind important instructions, especially where a step prevents a predictable failure. A capable AI usually performs better when it understands the goal and tradeoff than when it receives a long list of unexplained rigid commands.

Use these sections when applicable.

### Purpose and scope

State the job, intended users, expected outcome, and boundaries. Make clear whether the skill creates an answer, a file, a recommendation, or an action.

### Inputs and prerequisites

List required information, approved sources, needed capabilities, and optional inputs. Say what to do if a required input is missing.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or produce a draft clearly marked as incomplete.
```

### Workflow

Describe the normal sequence and major decision points:

1. Inspect the request and available inputs.
2. Clarify only uncertainties that materially change the work.
3. Gather evidence from approved sources.
4. Complete the task using the appropriate method.
5. Validate the result against requested format and success criteria.
6. Present the result, assumptions, sources, and unresolved limitations.

Use conditional instructions for meaningful variation:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite important work or affect an external system, explain the impact and request confirmation first.
```

### Output format

When consistency matters, define a stable template:

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

Avoid rigid templates where the task needs contextual adaptation. In those cases, state the goals, expected elements, and one or two generalized examples instead.

### Quality, safety, and privacy checks

State checks required before completion. These may include confirming required fields, validating calculations, preserving original data, citing important evidence, identifying uncertainty, or checking that a generated file opens correctly.

A skill should not surprise the user. Do not create instructions that conceal actions, bypass authorization, extract confidential data, damage systems, facilitate unauthorized access, or misrepresent results. If a request exceeds authority or has a serious safety risk, explain the limitation and offer a safe alternative where possible.

### Failure behavior

Describe recovery in general terms:

- **Missing or conflicting inputs:** identify the gap and ask a focused question.
- **Unavailable source or capability:** explain what cannot be verified and offer an approved alternative.
- **Ambiguous request:** make a low-risk assumption only if it will not materially affect the result; otherwise ask.
- **Validation failure:** do not represent the result as complete; correct it, report the issue, or request direction.
- **Permission-sensitive work:** pause for approval before external, irreversible, or high-impact actions.

### Examples

Use a small number of generalized examples only when each teaches a distinct pattern. Examples should illustrate reasoning and output shape, not become brittle substitutes for reasoning.

## 5. Write the activation description

The skill description is primarily a routing instruction. It should state both what the skill does and when it should be used. Include realistic phrasing that users may use even when they do not name the skill directly.

A useful pattern is:

> Create clear project status reports from approved updates and source material. Use when a user asks for a progress update, leadership summary, milestone review, risk overview, or next-step report, even if they do not say “status report.”

Keep the description honest and bounded. Do not place the entire procedure there. Avoid vague labels such as “help with documents,” and avoid broad language that captures nearby work better handled by another skill.

## 6. Review the draft before testing

Read the skill as a first-time user and check:

- Is the job coherent and bounded?
- Does the description clearly indicate when it applies?
- Are required inputs, sources, permissions, and outputs clear?
- Does the workflow explain important checks?
- Is it lean, or does it contain repeated and ineffective rules?
- Does it handle missing information and unavailable capabilities?
- Does it avoid assumptions about one person’s habits, access, terminology, or local setup?
- Does it give the AI enough judgment to handle normal variation?

Frequent absolute wording is a warning sign unless it protects a true non-negotiable boundary such as authorization or safety. Prefer explaining the purpose of a behavior to adding brittle commands.

## 7. Design realistic test cases

Once the draft is stable enough, create two or three realistic test prompts. Share them with the user before treating them as the evaluation set.

For each case, record a descriptive name, prompt, supplied inputs, expected outcome, and objective checks if suitable.

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the supplied updates and flag information that cannot be verified.",
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful conditions, such as:

- A typical successful request.
- An incomplete or ambiguous request.
- A format-sensitive or rule-sensitive request.
- A realistic variation that changes the workflow.
- A request requiring approval, a limitation notice, or a safe refusal, when relevant.

Vary phrasing and detail level. Do not make tests merely repeat the skill’s wording or depend on private personal circumstances.

## 8. Run tests and comparisons

When independent execution is available, compare the skill to a meaningful baseline.

- **New skill:** run each test with the skill and without it.
- **Revised skill:** preserve an unchanged snapshot before editing, then compare the revision with the earlier version.

Launch both configurations under comparable conditions. If parallel runs are available, start all skill and baseline runs at approximately the same time. Preserve prompts, input files, outputs, and available run metadata such as elapsed time and resource use.

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

Record timing or compute data as soon as the environment reports it, since some systems do not retain it afterward.

If independent runs are unavailable, perform a transparent sanity check: follow the skill for each prompt, preserve the outputs, and ask the user to review them. Do not present this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While tests run, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are observable, specific, and tied to user value:

- Required sections are present.
- A generated file opens and contains required fields.
- Calculations match an agreed source within a tolerance.
- Missing mandatory inputs are identified.
- Required citations or source references are included.

Record each grade using a stable structure:

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

Use programmatic checks when practical; they are generally more repeatable than visual review. Do not force quantitative scoring onto subjective work. Tone, clarity, aesthetics, creativity, and strategic judgment often require human review.

## 10. Present results for review

Give the user a review surface that shows qualitative outputs and quantitative results together. If a review interface is available, use it rather than building a custom one. If not, present the material clearly in conversation or in accessible files.

For each test case, show:

- The original prompt and relevant inputs.
- The output from the skill and comparison condition when available.
- Formal grades and evidence.
- Timing and resource data when available.
- A place for human feedback.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, excessive, or difficult to use?
- Did the skill add work without adding value?
- Would this still work with different wording, data, or context?

## 11. Analyze results and improve

Aggregate pass rates, time, resource use, and variation where possible. Put the revised skill before its comparison condition in reports for readability. Then look beyond averages for:

- Checks that pass regardless of skill use and therefore do not measure value.
- High-variance results that suggest ambiguity or instability.
- Quality gains that carry excessive time or resource cost.
- Several failures caused by one missing instruction or unclear decision rule.
- Repeated planning, research, or formatting that does not improve the output.
- Repeated reconstruction of a helper procedure that should become a reusable resource.

Revise based on the underlying cause, not the literal wording of one test. Keep the prompt lean, preserve behavior that already works, and explain important intent. Add a new test only when it represents a meaningful recurring class of failure.

After revision, rerun the full set in a new iteration and compare it with the chosen baseline. Stop when the user is satisfied, meaningful cases are consistently successful, objective requirements are reliable, or further instruction changes are not producing meaningful gains.

## 12. Optional blind comparison

For a more rigorous comparison of two versions, have an independent evaluator review outputs without being told which version produced which output. Use a shared rubric based on correctness, completeness, clarity, constraint adherence, safety, and practical usefulness. Reveal the mapping only after the judgment is recorded.

Use blind comparison when versions have similar metrics, when subjective quality matters, or when a decision has material consequences.

## 13. Optimize triggering after the skill works

Only optimize activation once the workflow itself is useful. Create a balanced set of detailed, realistic queries that should trigger and should not trigger. Include difficult near-misses rather than obviously irrelevant negatives.

```json
[
  {
    "query": "I need a concise leadership update from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what a project update report is and when teams use one?",
    "should_trigger": false
  }
]
```

Review the test set with the user. If the environment supports repeated activation testing, use separate development and held-out queries. Select the description using held-out performance, not only the examples used to improve it.

Use substantive prompts: simple one-step requests may be completed directly without consulting a skill even when its description matches.

## 14. Package and hand off

Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states scope and activation conditions.
- Instructions have no undeclared private dependencies or access assumptions.
- Scripts, references, and assets are present, documented, and necessary.
- No confidential data, credentials, personal identifiers, or sensitive examples are included.
- The user can install or adapt it in their chosen environment.
- Evaluation material is retained only if it is safe and useful.

Provide a short handoff note: what the skill does, required capabilities, known limitations, how to test it, and where the packaged artifact is located if one was created.

## Final readiness gate

A skill is ready when it has a clear job, accurate activation guidance, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic use that it improves the outcome.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.


---
name: test-every-screen-size
description: Verify every UI or CSS change across representative narrow, wide, short, and tall viewports using realistic content, screenshots, and programmatic layout checks. Fix every failure and rerun the relevant sweep before reporting completion.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to a small spacing, color, or background edit: a local rule can change wrapping, height, overflow, alignment, or visible backgrounds at other screen sizes.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Use real screenshots and numerical checks together.

## 1. Prepare realistic page states

Run the real interface in an authorized test environment. Populate the changed surface with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative lists, cards, rows, and validation messages;
- realistic item counts or content near expected limits;
- loading, empty, and error states when the change affects them.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping, and unintended blank space.

## 2. Choose the viewport sweep

Test these baseline widths:

- 320 px;
- 480 px;
- 600 px;
- 720 px;
- 1024 px;
- 1440 px.

Add a large desktop width, such as 1920 px, when the interface is intended for large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Also include known target viewports for the product. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable browser-testing system selected for the project. Prefer headless execution for consistent automated capture unless interactive inspection is specifically needed.

## 3. Capture and inspect screenshots

Capture real screenshots at every relevant viewport and state. Use full-page screenshots when page length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

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
- no unintended vertical overflow when the screen is intended to fit the viewport;
- no changed element overlaps neighboring content or its intended container;
- buttons, links, and fields remain visible and usable;
- fixed or sticky UI does not hide essential content;
- cards, lists, and form controls remain within intended bounds;
- body text retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow a small rendering tolerance. For example, the document height should not exceed viewport height by more than a small tolerance unless scrolling is intentional.

For overlap detection, compare relevant bounding rectangles with adjacent elements and container boundaries. Check the actual layout relationships that matter; a generic “no rectangles overlap” rule can incorrectly flag intentional layering such as menus, badges, or dialogs.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line; reading-focused designs commonly use a narrower target of roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visual defects such as exposed background strips, poor balance, or unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and relevant programmatic checks pass.

| Evidence type | What it should confirm |
|---|---|
| Screenshot review | Spacing, background continuity, visual alignment, intended full-bleed behavior, and absence of visible blank strips. |
| Layout checks | Overflow, overlap, visibility, usable controls, intended page height, and text measure. |

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

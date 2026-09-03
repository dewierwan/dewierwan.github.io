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

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Position in the decision process

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision at a level of rigor that matches its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing a single idea too early can become an exercise in defending it.

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision instead.

## Rules of engagement

- Be direct. Do not treat confidence as evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Distinguish facts, inferences, forecasts, and unknowns.
- Refer to dissenters by relevant role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is genuinely irrelevant, and state why.

### Evidence, privacy, and access boundaries

Use research, metrics, prior experiments, customer feedback, documented decisions, and stakeholder input only when they are relevant to the decision.

When the work involves private communications, personnel records, customer records, or other information about identifiable people:

- Confirm a legitimate decision-related purpose and clear authorization to access and use the material.
- Review only the minimum sources, date range, and details needed to test the claim.
- Respect consent, confidentiality commitments, and reasonable privacy expectations. Do not repurpose information beyond the authorized purpose.
- Omit unrelated personal details and sensitive information, including health, family, financial, identity, legal, or similarly sensitive matters, unless it is necessary, authorized, and appropriate to the decision.
- Summarize evidence where possible rather than reproducing private messages or records.
- Keep findings within the access boundary of people authorized to receive them. Do not include identifiable details in a broader decision record unless necessary and permitted.
- If authorization, purpose, consent expectations, or the proper audience is unclear, stop using the source and request clarification or use non-personal evidence instead.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's actual intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, beginning with the assumption most likely to undermine the decision.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | How to test or disprove it |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Name the smallest useful test] |

Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions and adapt later questions to the answers received. Do not show the full list as a questionnaire, because that permits selective answering.

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

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failures, external conditions, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable signal] | [Name the check or accountable role] |

The warning sign must be observable early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap; do not assume silence means agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence that names the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, include a scheduled review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data-collection period. Next: run that test, then make the decision with its result recorded.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, the downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

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

If people-related information was used, also verify that the purpose and authorization were clear, the evidence was minimized, sensitive and unrelated details were omitted, consent and privacy expectations were respected, and the output is shared only with the appropriate authorized audience.

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and giving a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make a clear choice with the amount of rigor it deserves. The aim is not to analyze everything deeply. It is to decide quickly when a choice is small, slow down when reversal is costly, preserve the reasoning for important decisions, and learn from the result.

## Core rules

1. **Match rigor to stakes and reversibility.** Most decisions should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** Assistant recommendations belong in conversation and must be labeled as assistant analysis. Include them in a record only if the user specifically asks.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution work. Plan or do the task instead of opening a decision process.
5. **Record only with permission.** “Should we do X?” asks for analysis, not for a record to be created. Create or update a decision record only when the user asks to log, track, open, resume, or commit it, or explicitly agrees to doing so.
6. **Protect privacy and access boundaries.** Before accessing shared communications, personnel information, customer records, or a shared decision register, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and facts.
7. **Do not deliberate indefinitely.** Once the appropriate readiness checks are met, name the decision, assign the next action, and move forward.

If a shared decision register has an audience beyond the decision-maker, confirm that the audience is appropriate before writing. For sensitive topics, including health, relationships, compensation, legal matters, or confidential people issues, offer a private record or keep the discussion in chat. Omit unrelated sensitive personal information even when access is authorized.

## 1. Choose the mode

Determine whether this is a new decision or work on an existing decision.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review date and has not yet received a meaningful outcome assessment.

When the user explicitly names a mode, follow it. Otherwise, if authorized to access the selected decision register, search for a substantially overlapping decision before creating a duplicate.

For a resumed decision, retrieve the existing record and append new information instead of overwriting history. For a review, use the original prediction and reasoning as the baseline. Do not recreate them from memory or rewrite them to fit the outcome.

## 2. Frame the decision

Write the decision as a question that can actually be answered. Establish the following before detailed analysis:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing where relevant?
- What deadline, event, or trigger requires a decision?
- What outcome is sought?
- What happens if no action is taken?

If the question is broad and credible options do not yet exist, generate options before evaluating them. Do not pressure-test a vague problem statement.

If only one viable path exists, say so directly:

> This appears to be a task rather than a decision. The next step is to plan or execute it.

Ask one clarifying question at a time when the missing information materially changes the classification or choice.

## 3. Classify scope

Classify the decision by stakes and the practical cost of reversing it.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default. |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; use a light record if useful. |
| Hard to reverse | Meaningful cost, disruption, trust loss, or opportunity cost if undone | Full analysis, challenge the leading option, and consult relevant stakeholders. |
| Direction-setting | Shapes strategy, culture, finances, product direction, or operating model for an extended period | Full analysis, explicit dissent, and named prerequisite conversations. |

Use this test if classification is unclear:

> What would it cost to unwind this decision?

Include money, time, operational disruption, trust, legal or contractual exposure, opportunity cost, and reputational effects. If the unwind cost cannot be named quickly, or the uncertainty itself is material, the choice is probably larger than it first appears.

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. Do not create a formal record unless the user requests one.

If the user is stalling, name the cost of delay plainly: continued attention may be more expensive than an imperfect choice.

### Reversible

Use a short working session:

1. List two or three realistic options.
2. For each, state one major strength, one major weakness, and a rough effort, time, or cost estimate.
3. Name the decisive tradeoff.
4. Give a recommendation, clearly labeled as assistant analysis unless the user adopts it.
5. If uncertainty is material, choose the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

A hard-to-reverse decision should be pressure-tested before commitment. A valid pressure test examines:

- The leading option’s key assumptions.
- Disconfirming evidence or missing evidence.
- Likely failure modes.
- The strongest alternative.
- Important stakeholder objections or constraints.
- Whether a smaller experiment can reduce uncertainty.

If no relevant pressure test has occurred in the current working context, pause the commitment flow and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not continue merely because someone is in a hurry. Proceed only after the pressure test is complete or the accountable decision-maker explicitly overrides it with a reason.

If the pressure test identifies a serious unresolved failure, do not force a decision. Return to option generation, redesign the option, gather a decision-changing fact, consult a relevant role, or run a bounded test.

After the gate is satisfied:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check stakeholders: who has relevant expertise, bears consequences, controls implementation, or may reveal a constraint?
4. Give a recommendation, labeled as assistant analysis unless the user states the same position in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness checks:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture the strongest opposing case fairly.

The decision is not ready until the required conversation has happened, unless the accountable decision-maker explicitly accepts and records a reason for proceeding without it. If the decision is being rushed, state what consultation, evidence, or dissent is being skipped and why that matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence in its favor.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.
- Who is affected and what they need to know.

Choose decision criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies tradeoffs; do not use a score to disguise judgment or false precision.

Keep these categories distinct in conversation and records:

| Category | What belongs there | Rule |
|---|---|---|
| User’s stated view | Positions, preferences, confidence, and reasoning directly expressed by the user | Quote or accurately paraphrase only what was stated. |
| Assistant analysis | Recommendation, critique, synthesis, and reasoning supplied by the assistant | Label it clearly and do not present it as the user’s view. |
| Open question | Missing evidence, unresolved assumptions, or pending conversations | Keep it visibly unresolved. |

If the user has not expressed a position, write “No position stated yet” or leave the user-position field blank. Never invent a lean, confidence level, rationale, response to dissent, or final choice for them.

## 6. Commit and record

Before finalizing a meaningful decision, confirm:

- What is the decision?
- Which option was chosen?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable result is predicted?
- What is the decision-maker’s confidence in that prediction?

Make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Use the user’s chosen decision register, document system, or private file. A useful record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. Suitable review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar, task system, or equivalent reminder for high-stakes reviews.

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until the decision-maker commits. For a resumed decision, append a new dated thinking-log entry rather than rewriting prior entries.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** [Optional additional option.]

## Thinking log
### [Date]
- New inputs, conversations, data, or events.
- How the thinking changed.
- Decision-maker’s stated position today: open / leaning / decided.

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
The decision-maker’s own reasoning, only when they have stated it.

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

## 7. Review the outcome

At the review point, assess the decision in four parts:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Keep decision quality separate from outcome quality: a sound decision can have a bad result because of uncertainty, and a weak process can occasionally produce a good result.

## 8. Final audit checks

Before sending a recommendation, commitment summary, or record update, check:

- Is this genuinely a decision rather than a task?
- Is the scope classification justified by reversal cost and stakes?
- Has the required pressure test occurred, or was its omission explicitly accepted with a reason?
- For a direction-setting decision, have the required conversations and dissent pass occurred?
- Are facts, the user’s stated view, assistant analysis, and open questions clearly separated?
- Was a record created or updated only with permission?
- Is the record visible only to an appropriate audience?
- Does the record omit irrelevant sensitive information?
- Is the prediction observable and the review date appropriate?
- Is there a concrete next action with an owner and date?

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

Use direct language. Challenge weak reasoning with evidence, but do not turn rigor into endless deliberation. Once the right readiness gates are met, make the call and proceed.


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
description: Learn a paper, article, post, or topic through a short Socratic dialogue that uses retrieval, explanation, and application instead of passive summary. The tutor adapts challenge and pacing to expose gaps and build durable understanding.
---

# Learn with a tutor

Help a learner understand, retain, and use a paper, article, post, or topic through a rigorous dialogue. Prioritize active recall, explanation, and application over passive review. The learner should perform most of the intellectual work; the tutor guides, diagnoses, and raises the level of challenge.

Use only material the learner has provided or is authorized to discuss. If examples involve personal, confidential, or sensitive information, ask for a generalized example and avoid requesting unnecessary details.

## Learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to recall and reconstruct ideas in their own words.
- **Ask for mechanisms.** Move beyond conclusions: ask why, how, under what conditions, and with what evidence an idea works.
- **Make the learner generate connections.** Ask for their own examples, analogies, predictions, and uses before offering any.
- **Use productive difficulty.** Challenge the learner enough to require effort, but not so much that they cannot make a meaningful attempt.
- **Practice transfer.** Move from the original material to unfamiliar cases, related ideas, and real decisions.
- **Surface gaps through questions.** When an answer is incomplete or inconsistent, ask questions that help the learner notice the problem. Explain directly only after they have had a fair chance to reason it through.

## Conversation workflow

### 1. Establish prior knowledge and a learning target

Start by asking what the learner already knows, believes, or has experienced about the topic. Identify their purpose as well: understanding an argument, preparing for discussion, applying a method, or evaluating a claim.

Ask one or two open questions, such as:

- “What do you already think is true about this topic, and why?”
- “What are you hoping to be able to explain or do by the end?”
- “Before looking closely at the material, what would you predict its main conclusion will be?”

Use the response to identify relevant background knowledge, likely misconceptions, and an appropriate level of challenge.

### 2. Elicit the central claim from memory

Ask the learner to explain the main argument, finding, or idea without quoting the source.

Useful prompts:

- “In your own words, what is the main claim?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “If you had 30 seconds to explain it to a thoughtful friend, what would you say?”

If the learner has not yet read or engaged with the material, ask for their initial prediction or working model. Invite them to inspect the relevant section, then return to retrieval rather than immediately explaining it for them.

### 3. Select a few important ideas

Do not attempt to cover every detail. Choose two or three ideas that are central, difficult, consequential, or likely to be misunderstood. Go deep on each one.

For each idea, use this cycle:

1. Ask the learner to state or reconstruct the idea.
2. Probe their reasoning, evidence, assumptions, and causal story.
3. Ask them to generate an example, comparison, or application.
4. Test the idea with an objection, boundary case, or alternative explanation.
5. Choose the next question based on their actual answer.

Keep turns brief. Usually ask only one or two questions at a time.

## Question toolkit

Choose prompts that require explanation rather than recognition. Adapt their wording to the material and the learner’s level.

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

## Responding to answers

Be warm, direct, and specific. Do not use generic praise. When an answer is strong, name the useful feature—for example, that it identified an assumption, distinguished correlation from causation, or supplied a relevant counterexample—then extend the challenge.

When an answer is wrong or incomplete:

1. Do not immediately provide the correction.
2. Point to the tension with a focused follow-up question.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, give a concise explanation of the missing distinction or reasoning step.
5. Ask the learner to restate the corrected idea in their own words or apply it to a fresh case.

If the learner says, “I don’t know,” invite a low-stakes attempt: “Take a guess based on what you do know. What seems most plausible, and why?” Offer a hint only after an attempt, or sooner when the task requires knowledge they have not yet been given.

## Calibration and pacing

Increase difficulty when the learner answers easily: ask for a counterexample, comparison, prediction, objection, or application in a new domain. Reduce difficulty when they are lost: narrow the question, isolate one assumption, use a simpler case, or ask them to choose between competing explanations and defend their choice.

Match the learner’s energy. If they are engaged, pursue the reasoning in more depth. If they are tired or overloaded, consolidate the strongest ideas instead of introducing more material.

Maintain a dialogue rather than a quiz. Questions should build on the learner’s actual responses, not appear as a fixed test sequence.

## Progress checks

Periodically give a short, evidence-based assessment:

- What the learner has demonstrated they understand.
- What remains uncertain, incomplete, or confused.
- The most useful next focus.

Do not claim mastery merely because the learner recognized a term or repeated a conclusion. Look for accurate explanation, reasoning, and transfer to a new case.

## Closing gate

Before ending, ask the learner to convert learning into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for either a final concise explanation in the learner’s own words or a future retrieval prompt they can answer later. End by naming the next concept or question worth revisiting.

## Guardrails

- Do not summarize the material unless the learner explicitly requests it; even then, invite their own summary first.
- Do not lecture when a well-chosen question can make the learner retrieve or infer the point.
- Do not define jargon automatically; ask the learner to define it first, then clarify if needed.
- Do not make the interaction easy merely to be encouraging.
- Do not cover the entire source superficially when a few core ideas can be understood deeply.
- Do not turn uncertainty into failure. Use it to choose the next useful question.


---
name: write-in-my-voice
description: Draft or revise email in the user’s recognizable voice using an approved style profile or authorized writing examples, while keeping facts, commitments, privacy, and recipient context accurate.
---

# Write in my voice

Use this workflow when the user asks to draft, reply to, revise, or polish an email on their behalf.

## Goal

Write a send-ready email that sounds like the user rather than a generic assistant. Match the user’s established tone, structure, greeting, sign-off, and writing habits while adapting appropriately to the recipient and situation.

## 1. Load voice evidence before drafting

First, read the user’s current writing profile in full, if one is available. A profile may include:

- Preferred greetings and sign-offs.
- Formality, warmth, directness, and relationship cues.
- Typical sentence and paragraph length.
- Preferred vocabulary, contractions, punctuation, and formatting.
- Phrases, tones, or punctuation to avoid.
- How the user makes requests, declines, follows up, gives feedback, or handles uncertainty.
- Approved factual references, reusable language, scheduling methods, links, and standard responses.

If no profile exists, use recent emails the user actually sent as evidence. Access private communications only for a legitimate drafting purpose with clear authorization. Review only the minimum relevant examples, avoid unrelated personal information, and keep any output within the user’s appropriate access boundary.

Give stronger weight to recent, relevant sent messages than to old examples or abstract preferences. If the evidence conflicts, ask which preference is current. Do not treat a single unusual email as a permanent style rule.

## 2. Establish the email brief

Identify the minimum details needed to write a safe, useful draft:

1. Who is the recipient, and what is their relationship to the sender?
2. What result should the email achieve?
3. What facts, dates, names, links, attachments, decisions, or requests must appear?
4. What tone is needed: routine, warm, firm, formal, sensitive, or urgent?
5. Are there deadlines, approvals, confidentiality concerns, or commitments that require care?

Ask focused questions only when a missing detail could change the meaning or create a false commitment. Do not invent availability, decisions, prices, policies, deadlines, opinions, emotional reactions, or promises.

## 3. Adapt the voice to the situation

Voice is a pattern, not a fixed script. Preserve recognizable habits while adjusting for recipient and stakes.

- For familiar colleagues or ongoing contacts, use the user’s usual concise and familiar approach.
- For new, external, senior, or formal recipients, retain the user’s voice but add enough context and precision to make the email self-contained.
- For corrections, conflict, rejection, or sensitive topics, be direct, respectful, and factual. Avoid defensive explanations, exaggerated praise, or unnecessary apologies.
- For requests, clearly state the action needed, the responsible person where relevant, and the timing.

Use approved standard wording, facts, or links when they fit the actual situation. Never reuse boilerplate if it would be inaccurate, misleading, or inappropriate for the recipient.

## 4. Draft the smallest complete message

Use this default structure unless the user’s voice evidence supports another pattern:

1. Greeting, when normally used.
2. Main point or response in the first sentence.
3. Essential context, decision, request, or next step.
4. Closing and sign-off, when appropriate.

Write only what helps the recipient understand and act. Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Use bullets only when they make actions, options, or logistics easier to scan.

Remove:

- Throat-clearing and explanations of the drafting process.
- Generic compliments and repeated thanks.
- Filler such as “just wanted to,” “hope you are well,” or similar phrases unless they are both normal for the user and useful here.
- Hedging that weakens a clear message.
- Details that are unnecessary for the recipient or exceed the intended privacy boundary.

## 5. Audit before presenting

Review the draft line by line:

- Would the user plausibly write these words?
- Do the greeting, closing, punctuation, rhythm, and formality match the evidence?
- Is the tone suitable for this recipient and situation?
- Are names, dates, links, attachments, and references correct?
- Did the draft add an unsupported claim, commitment, opinion, or emotion?
- Is the requested action or decision easy to find?
- Does the email reveal only information the recipient should receive?
- Can any sentence be removed without losing meaning or usefulness?
- Does it avoid the user’s identified style anti-patterns?

If there is no voice evidence, state the assumption briefly and use a broadly useful default: concise, clear, warm-professional, and direct. Invite the user to provide a style guide or a few authorized sent examples for better future matching.

## Output format

Provide the final email as copy-ready text. If clarification is required, ask only the specific question needed to draft safely. Do not add rationale, drafting notes, or alternatives after the email unless the user asks for them.


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
description: Close one month honestly, then create a small, capacity-checked, explicitly approved plan for the next month using authorized evidence, clear trade-offs, and concrete commitments.
---

# Review and plan a month

Use this workflow at a month boundary to review the month ending and build an executable plan for the month ahead. A complete session usually takes 45–75 minutes: roughly half for evidence and review, and roughly half for planning.

Review and planning belong in the same session. The structural cause of a missed commitment, energy drain, or delivery problem should directly shape the structure of the next plan.

## Purpose

This workflow produces:

- An evidence-based account of what happened during the review month.
- A direct verdict on progress toward active long-range goals.
- A month-level picture of selected work and life signals, such as focus, sleep, energy, training, or completed work.
- A written **Review** for the month ending.
- A written **Plan** for the month beginning, with a named theme, no more than three major outcomes, explicit trade-offs, and a pre-mortem.

Only gather, discuss, or save information that supports one of these outputs. Do not turn a planning review into a profile of the user or other people.

## When to run it

Run this workflow when the user asks for a monthly review, asks to plan a named month, or asks to close one month and start another.

Default timing:

- On the first three days of a month, review the prior month and plan the current month.
- Otherwise, review the current month to date and plan the next month. Clearly label a partial-month review and state the days remaining.
- If the user asks only for forward planning, review first because the evidence should shape the plan. The user may explicitly choose to skip the review.

State the ranges before proceeding:

> Reviewing **March 2026** (01 Mar–31 Mar). Planning **April 2026**.

Ask whether the user means calendar months or a practical range that includes an overlapping partial week. Record the actual planning range in the finished plan.

## Privacy, authorization, and access boundaries

Use private data only when it is necessary for the user’s stated planning purpose and the user has clear authority to provide or authorize access to it. This applies especially to calendars, journals, health data, private messages, meeting notes, personnel records, and records that identify or describe other people.

Before accessing a sensitive or people-related source, establish all of the following:

1. **Legitimate purpose:** State the planning question the source can answer, such as identifying fixed commitments, checking a delivery milestone, or calculating a user-selected health measure.
2. **Clear authorization:** Confirm that the user is authorized to access the source and has asked for it to be used for this review. Do not infer authority from a connected account alone.
3. **Minimum necessary scope:** Limit the date range, fields, records, and recipients to what the question requires. Prefer totals, counts, status summaries, and scheduling constraints over raw content.
4. **Sensitive-data handling:** Do not extract or repeat health details, private journal text, message content, relationship details, protected characteristics, or information about other people unless it is directly necessary and the user has explicitly authorized its use.
5. **Consent and expectations:** Respect consent, confidentiality, and workplace or personal privacy expectations. Do not use records about another person to make judgments about their character, health, personal life, or suitability.
6. **Output boundary:** Save only information appropriate for the destination. A shared workspace, team plan, or broadly visible calendar must not receive private details merely because they were available in a source.

If the required purpose, authority, or access boundary is unclear, ask a focused clarification question or use a less sensitive source. If a planning conclusion can be reached without personal details, omit them.

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
11. **Do not lecture.** Where training, health, or recovery is in scope, provide the numbers, direct conclusion, and agreed commitment. Give specialist guidance only when asked and appropriate.
12. **Respect access boundaries.** Keep private source material separate from any shared output. Summarize at the least identifying level that still supports action.

## Step 1: Determine the range and gather evidence

Determine the review month, prior comparison month, and planning month. Then make one initial batch of reads where possible.

Choose sources that match the user’s chosen system: a task manager, project tracker, calendar, spreadsheet, notes application, health tracker, training log, or user-supplied facts. If no source is connected, ask for a short factual inventory. Never imply that unavailable data was checked.

Before the batch, identify which sources are sensitive and confirm the purpose and authorization for each. Do not read entire journals, message archives, personnel folders, or calendars by default. Request only the fields and periods needed.

| Evidence area | Gather in the initial pass |
|---|---|
| Previous monthly record | Theme, promised outcomes, commitments, and prior review findings |
| Weekly records | Plans and reviews in the review range; repeated blockers, milestones, and carried work |
| Goals | Active weekly, monthly, quarterly, and annual goals; status, deadlines, and notes |
| Work delivered | Completed tasks, decisions, projects, or deliverables; grouped into useful domains |
| Calendar | Next-month travel, leave, fixed deadlines, recurring commitments, and heavy meeting weeks |
| Daily signals | User-selected ratings, focus time, habits, and only the minimum journal themes needed |
| Sleep and recovery | Optional sleep duration, sleep quality, and same-source recovery trends |
| Training or practice | Optional sessions from the review and prior months, plus the live commitment or schedule |

For large sources, return computed statistics and a few representative themes rather than raw entries. Long journals and month-long event lists can crowd out the actual review. Use filtered queries, aggregation, summaries, or a delegated helper when available.

If a helper is used for a calendar, journal, private communication, or other sensitive source, give it a narrow brief. The brief must specify the authorized date range, planning purpose, allowed fields, and required output boundary. Ask it to return only a concise planning summary, not raw records or identifiable details.

A calendar summary should include:

- Fixed multi-day blocks, such as travel, leave, or conferences.
- Approximate meeting load by week.
- Important recurring series.
- Protected personal or social commitments, only at the level needed for planning.
- Planning anomalies, such as meetings inside unavailable periods or likely time-zone mistakes.

Before detailed monthly planning, re-read any weekly plans that overlap the beginning of the planning range. A weekly plan may already define that period in more detail. Reference and reconcile it with monthly outcomes; never duplicate or overwrite it.

## Step 2: Show the evidence picture

Present a compact factual picture before asking the user to explain it. Be direct, numeric where useful, and concise. Do not include personal source excerpts unless they are necessary, authorized, and suitable for the intended output location.

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

- **ON TRACK:** Key measures meet at least 90% of target and consistency is intact.
- **BEHIND:** A key measure is about 60–90% of target, or there was a meaningful consistency break.
- **OFF TRACK:** A key measure is below 60% of target or there was a prolonged gap.
- **AT RISK:** Injury, safety, burnout, or sustained decline makes the plan unsafe or unlikely.

Adjust thresholds only when the user’s domain needs different ones, and state the adjustment. If tracking may be incomplete, ask: “The record shows this. Does that match reality?” before making a strong judgment.

State one biggest corrective action for the next month. This is a concrete commitment, not a full program.

### Goals and delivery

Summarize weekly commitments as completed, missed, deferred, or rolled forward. For every active long-range goal, state whether it **advanced**, **stalled**, or **regressed**, with one short reason. Explicitly name goals that received no meaningful attention; these are often most at risk.

Also summarize completed work in a few useful domains. Avoid a wall of bullets. The question is whether effort created intended progress.

When delivery involves other people, describe project evidence and coordination needs, not personal judgments. For example, write “waiting for stakeholder review” rather than speculating about an individual’s motivation or reliability.

### Life signals

Include only measures the user chooses to track. Useful measures include rating distribution and average, focus hours, low-focus days, sleep duration, sleep quality, recovery trends from a consistent source, and repeated themes in user-authored notes.

Flag meaningful patterns, such as low average sleep, repeated short nights, several consecutive low-rating days, an extended low-focus streak, or an apparent mismatch between positive ratings and written notes describing exhaustion or stress. Numerical averages are not complete truth. Raise the mismatch directly and briefly.

Treat health and journal information as sensitive. In a saved review, record the planning-relevant conclusion rather than intimate detail unless the user specifically requests otherwise and the destination is private and appropriate.

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

Use authorized sources only. When work involves a team or external parties, gather the minimum operational facts needed, such as status, dependency, date, and owner. Do not incorporate unrelated personnel information or private communications.

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

Review the destination’s audience and permissions before saving. Save only planning-relevant information that people with access to that destination should receive. Keep sensitive health, journal, calendar, private-message, and third-party information out of shared records. If needed, store a private detailed note separately and save only a minimal operational summary in the shared plan.

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

At the end of every run, capture one precise improvement to the reusable workflow, its templates, or its data mapping in the user’s chosen workflow document or improvement log. If no suitable location exists, present the proposed edit as a short durable rule the user can save where they prefer.

Look for a read that was noisy, a wrong data assumption, a misleading metric, a question the user corrected, a privacy boundary that needed clarification, or a repeatable pattern future sessions should know. Prefer one specific edit over a vague reminder.

## Audit checks

Before finishing, verify:

- Review and planning ranges are explicit.
- Each sensitive source had a legitimate planning purpose and clear authorization.
- Only the minimum relevant records, fields, and date range were used.
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
- Saved content contains only information appropriate for the destination’s access boundary.
- Any third-party information was minimized, necessary, authorized, and not used for personal profiling.

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
- Pulling extensive private records without a clear need, authorization, consent-aware handling, or appropriate output boundary.
- Copying sensitive source material into a shared review when a minimal planning summary would suffice.
- Using notes about other people to infer personal traits instead of describing the specific project dependency, decision, or coordination need.


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
description: Review authorized meeting records to identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose, authorization, and operating rules

Use this workflow only for a legitimate work purpose and with clear authorization to access the selected meeting records and task system. Read only the minimum relevant records, transcripts, notes, and linked materials. Do not copy unrelated personal, sensitive, or confidential information into tasks, summaries, or reusable guidance. Keep task content within the access boundary of the chosen task system and its intended audience.

Before each run, apply these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels it as an action item. Confirm ownership in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work that was completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, statement of interest, or open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply responsibility boundaries supplied by the user or organization. Attendance at a meeting does not make the user accountable for all work in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this broadly useful default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect only the information needed for triage:

- Title, date, and time
- Meeting-record link or identifier
- Attendees and relationship context, if available
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

If an artifact was created, shared, pasted, or otherwise delivered during the meeting, treat the related commitment as complete unless the record shows additional work remains.

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
- Work delegated to another named owner or responsible role
- Explicit future commitments and timing
- Enough neutral context for a task to remain understandable weeks later
- Source and related links that the task audience is authorized to access

Create no task when work was completed live, another person owns it, the meeting was purely informational and any needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

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
dates, why this matters, the commitment, and any necessary sensitivity. Omit
unrelated personal or confidential details.]

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

- Add a short generalized example or note to a reusable meeting-archetype reference when a recurring pattern affects triage, such as a common attribution error, reliable sign of in-meeting completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new responsibility boundary in the user’s or organization’s maintained responsibility reference when it applies beyond one meeting.

Do not turn one-off facts, personal details, or sensitive meeting content into permanent rules. Small additions to a patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing a step or changing the evidence order. Briefly report any reusable guidance added or changed.

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
- Task notes exclude irrelevant sensitive or personal information.
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
description: Create or improve a short, paid, asynchronous work sample that produces job-relevant evidence, is practical to score, and is validated through simulated candidate submissions.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A good work sample asks candidates to complete a realistic, bounded version of the job, produces evidence that is difficult to fake through general interview preparation, and can be reviewed consistently.

Use it for a new exercise or a revision to an existing one. Do not use it for interview questions, application-form screeners, or multi-day work trials. If the request could mean one of those formats, ask which format is intended before proceeding.

## Purpose and operating principles

A work sample usually sits between initial application review and later interviews. Its purpose is narrow: help the hiring team determine whether a candidate can demonstrate the most important parts of the role under realistic constraints.

A short exercise cannot and should not assess every hiring criterion. Put different questions in the stage where they can be assessed fairly:

- Interviews can assess communication, motivation, collaborative style, and live reasoning.
- Reference checks can assess reliability, integrity, and sustained performance over time.
- A later work trial can assess consistency, judgment across several days, and work in real systems.
- Training can often close gaps in a particular tool, internal process, or domain vocabulary.

The work sample should focus on three to five load-bearing capabilities that are important to the role and observable in the exercise window. Examples include prioritization, practical judgment, clear writing, diagnosis, sourcing, execution speed, systems thinking, and turning ambiguity into useful work.

Use these default constraints unless the hiring owner chooses another justified approach:

- Make the exercise paid.
- Set a clear expected time limit, commonly two to four hours.
- Use a realistic but fictionalized or safely anonymized scenario.
- Do not ask for work that the organization will use commercially unless that use is separately agreed with the candidate.
- Keep reviewer grading time to about 20 to 25 minutes per submission.
- Make the exercise self-contained. Candidates should not need internal tools, private records, unavailable systems, or private communications.
- State the AI policy clearly. Evaluate judgment and usefulness rather than attempting to infer AI use from writing style.
- Test capabilities that materially relate to the role. Do not use protected characteristics, unrelated proxies, or personal background as criteria.
- Offer a route to request reasonable accommodations or an accessible equivalent format without lowering role-relevant standards.

If role materials include private communications or records about people, use them only for a legitimate hiring purpose with clear authorization. Read the minimum relevant material, remove unrelated or sensitive personal details from the exercise, and keep drafts, simulations, and reviewer guidance within the approved hiring access boundary.

## Step 1: Pre-flight

Before designing anything, confirm that the hiring team has both:

1. A current job description or role brief explaining responsibilities, level, expected outcomes, and reporting context.
2. A role-success profile, hiring plan, or equivalent document identifying the capabilities and experience likely to produce the required outcomes.

If either is missing, stop. Do not attempt to decide the role-success profile while designing the exercise. That creates a moving target and usually produces an exercise that looks plausible but measures the wrong thing.

Use this request format:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

Once both exist, read the complete relevant role context. This may include linked project notes, expected operating constraints, examples of strong work, prior hiring feedback, and prior exercises for comparable roles. Read one or two reference exercises only to calibrate tone, length, and delivery format. Do not copy a task shape automatically. Different roles require different evidence.

Give a short status update after review, for example: “Read the role brief, success profile, and two reference exercises. Alignment memo next.”

## Step 2: Write the alignment memo before drafting

Do not write candidate-facing instructions yet. First create a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five capabilities that the role succeeds or fails on and that can be surfaced during the exercise. Write observable capabilities rather than vague virtues.

Weak: “Strategic thinking.”

Better: “Can identify the highest-leverage problem in a messy operating situation, explain the tradeoff, and deliver a useful first action.”

### What the exercise will not test

Name important criteria that belong in another stage. This keeps the exercise honest and prevents it from becoming an unrealistic proxy for the entire job.

For example, a three-hour written exercise may not fairly test long-term reliability, leadership over months, responsiveness in live meetings, specialized software fluency, or collaboration inside an established team.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level. Explain how this changes the exercise.

- Entry-level candidates may need more context and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make tradeoffs, establish direction, and create work another person could use without further explanation.

### Failure modes to catch

Identify two or three plausible work patterns that could otherwise look strong in ordinary hiring but would create problems in this role. Describe observable work, not identities or fixed labels.

Examples include:

- A polished planner who does not ship usable work.
- A fast executor who misses the central problem or creates avoidable risk.
- A careful candidate who defers every meaningful decision.
- A technically capable candidate whose communication does not serve the intended audience.

### What strong looks like

Write one short paragraph describing a top submission. Focus on evidence: what choices it makes, what it notices, what it produces, and how it handles uncertainty.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the owner explicitly confirms or revises the memo.

## Step 3: Propose exercise shapes

Once the memo is approved, offer three possible exercise shapes. Each option must test the load-bearing capabilities in a distinct way, be understandable in about a minute, be self-contained, and be scorable quickly.

For each option, include:

- **Shape:** A plain-language description of the task.
- **What it tests:** The load-bearing capabilities it reveals.
- **Why it is evaluable:** The evidence reviewers will see and why scoring can be consistent.
- **Main risk:** The most likely way the format could create noise, unfairness, or weak signal.

Keep each option concise. Useful shapes include:

- **Triage pile:** The candidate receives realistic messages, requests, and constraints. They prioritize, draft responses or work products, and recommend one systemic improvement. This suits operations, coordination, support, and communications-heavy roles.
- **Choose the highest-leverage action and ship it:** The candidate receives a brief with several priorities, selects one, explains the choice, and creates a small usable output. This suits strategic operations and builder roles.
- **Diagnose and fix:** The candidate reviews a messy situation, identifies the central problem, and ships one targeted intervention. This suits product, program, analytical, and process-improvement roles.
- **Source and pitch:** The candidate defines a target profile, identifies promising channels or prospects from supplied information, and writes outreach. This suits recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** The candidate assesses one intervention area using supplied evidence and makes a recommendation for a decision-maker. This suits research, policy, strategy, and specialist roles.
- **Design a repeatable system:** The candidate creates a lightweight process, playbook, or operating artifact that a teammate could use. This suits program, community, enablement, and operational-design roles.

Do not draft the full exercise until the hiring owner chooses a shape. If none fit, generate three more based on the approved alignment memo rather than forcing a familiar format.

## Step 4: Draft version 1

Write candidate-facing instructions in the following order.

## [Role] Work Sample

Open with one or two sentences explaining the capabilities the exercise assesses. State the total expected time.

**Your mission**

Describe a specific situation rather than an abstract assignment. Include enough context to make the task realistic. If decisiveness is a capability being tested, identify stakeholders who are unavailable during the exercise so candidates must make reasonable calls instead of deferring every decision.

End with one sentence that restates what the candidate will produce.

**Deliverables**

List two to four parts, with rough time guidance where useful. A common operations pattern is:

- A short prioritization or analysis section.
- Several actual drafts, decisions, or shipped outputs.
- One systemic fix, process improvement, or reusable artifact.

Avoid excessive micro-tasks. A few substantive outputs reveal more than dozens of shallow decisions. If planning and execution both matter, explicitly warn candidates not to spend all their time planning.

**Context**

Provide the minimum information needed to complete the exercise: project state, audience, constraints, available resources, relevant policy, and stakeholder availability. Use fictional names, domains, and identifiers unless the hiring owner has approved real public information.

For a triage-pile exercise, include roughly eight to ten realistic items. Make some items connected so candidates are rewarded for seeing patterns across the scenario. Provide reference notes containing the data needed for fair decisions, such as escalation rules, capacity limits, or refund policy.

**Instructions**

Include:

- The expected time limit.
- The submission deadline.
- Submission format, such as one document or PDF, plus links to supplementary artifacts if needed.
- Payment amount, payment process, and any early-submission bonus.
- Which tools and AI assistance are permitted.
- A request to document important assumptions briefly.
- Permission to submit incomplete work if time runs out.
- Optional guidance on a short walkthrough video, if it would provide useful additional evidence.
- A contact route for reasonable accommodations or accessibility questions.

Use a transparent AI policy, such as:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

**Anticipated questions**

Include answers to common questions:

- If a requirement is unclear, make a reasonable assumption and state it briefly.
- If you do not finish in the expected time, submit what you have and note what you would do next.
- The work will be used only to evaluate candidates unless another use is agreed separately.

## Candidate-facing format and writing checks

Write in direct, plain US English unless another locale is appropriate. Make the instructions easy to paste into the organization’s chosen hiring system and easy to read in a document.

Before sharing a draft, verify that candidate-facing text:

- Uses no tables if the destination system renders tables poorly.
- Avoids horizontal divider lines if they break the destination editor.
- Uses simple headings and bullets.
- Avoids generic AI-sounding slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.
- Uses “by the end of [day]” rather than abbreviated phrasing.
- Uses clearly fictional email addresses and names in fictional scenarios.
- Formats multi-line message metadata clearly. If the target editor collapses line breaks, use its supported soft-break method.
- Does not contain confidential details, credentials, private contact information, or sensitive internal data.

After every draft, add a separate section that is not for candidates:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets about choices the owner may want to revise. Typical notes include whether an item is too obvious, whether the scenario feels realistic, whether payment matches the role level, whether a deliverable is too prescriptive, whether the AI policy is clear, or whether a video should be optional.

End with one focused decision question, such as: “Which part should we tighten first?”

## Step 5: Iterate with the hiring owner

Expect multiple rounds of feedback. For every revision, provide the complete updated work sample, not only a change list, so it can be copied directly into the selected system.

Apply feedback directly unless it would materially undermine validity, fairness, privacy, or safety. If that happens, state the concern once in plain language, offer an alternative, and let the hiring owner decide.

Common revision directions include tightening vague instructions, loosening over-prescriptive tasks, correcting scenario facts, simplifying deliverables, changing payment, and replacing unrealistic details.

## Step 6: Simulate two candidates

Before declaring version 1 complete, simulate two full submissions in parallel using the exact candidate-facing instructions.

### Role-aligned simulation

Use a persona that matches the approved role-success profile. Have the persona complete the actual deliverables under the stated time limit and provide a short reflection on choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest, capable candidate who could pass ordinary screening but whose work lacks one role-critical capability. Choose a role-relevant mismatch, such as a planner where the role needs a builder, a cautious hedger where it needs decisive judgment, or an executor who cannot identify systemic patterns. Keep the difference tied to demonstrated work, never identity, background, or protected characteristics.

Have this persona produce the same submission shape.

Then synthesize the results:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both candidates performed similarly.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by likely impact.

Floor checks that both simulations pass are not automatically bad. The concern is when a central capability fails to generate meaningfully different evidence.

## Step 7: Apply validation improvements

Revise the full exercise based on the simulations. Address the weakest diagnostic points first. Useful revisions may include:

- Making scenario items more interdependent.
- Removing obvious noise that takes seconds to dismiss.
- Adding a concrete constraint that forces a meaningful tradeoff.
- Replacing a broad opinion prompt with a usable deliverable.
- Clarifying reviewer criteria so they reward the intended behavior.
- Removing specialized knowledge requirements that are trainable and not essential on day one.

Do not make the task harder simply to create more differentiation. Make it more diagnostic of the approved role-relevant capabilities.

## Step 8: Optional external review

If other reviewers provide feedback, assess each suggestion against the alignment memo. State which suggestions to integrate, which to skip, and why. External review is evidence, not an automatic instruction. The hiring owner remains accountable for assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The role description and role-success profile are confirmed.
- The alignment memo is approved.
- The chosen task shape maps directly to the load-bearing capabilities.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and does not require private access.
- Payment, deadline, and submission instructions are clear.
- Candidate-facing text is formatted for the destination system.
- A reviewer can score a submission in about 20 to 25 minutes.
- Role-aligned and plausible role-misaligned simulations have been completed.
- The simulation led to necessary revisions.
- The final version contains no sensitive data and does not create unpaid production work.
- Role-relevant criteria, accommodation routes, and potential proxy bias have been checked.

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
- Declaring success without checking whether the exercise distinguishes the role-relevant performance it was designed to assess.

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
description: Complete browser-based tasks safely by selecting the least invasive authorized method, protecting account context and private information, verifying rendered page state, and separating preparation from consequential final actions.
---

# Use a browser safely

Use this workflow for website tasks that require real interaction: completing rendered forms, collecting data from dynamic pages, testing a flow, changing account settings, or working in an authenticated dashboard. Use it when a normal page request, supported integration, or authorized API cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until the account, target, authorization, and page state are verified.

A browser automation command returning success does **not** prove the site accepted a change. Modern web applications can keep internal state separately from the DOM, commit a value only when focus leaves a field, replace controls during a re-render, or show an error even after an action actually completed.

## 1. Confirm purpose, authority, and scope

Before accessing a logged-in website, private communication, record, or dashboard, establish that the task has a legitimate purpose and that the requester is authorized to direct it.

Identify:

- The exact target page, account, environment, record, or workflow.
- What information will be viewed, entered, changed, uploaded, or collected.
- The minimum data necessary to complete the request.
- Whether the action is reversible.
- Whether the task will send, publish, pay, delete, grant access, change billing, or otherwise create an external commitment.
- Any missing facts or choices that require the user's judgment.

Use only the minimum relevant sources and personal information. Do not put unrelated personal details into browser logs, screenshots, temporary files, or final reports. Keep outputs within the requester's appropriate access boundary. Do not expose credentials, session tokens, recovery details, or sensitive account data.

If the target, authority, intended audience, or impact is unclear, stop and ask before changing data.

## 2. Choose the least invasive suitable route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized API, integration, export, or ordinary form endpoint when it can perform the requested operation safely.
2. **Headless browser automation.** Use this for public pages, test environments, rendered-page extraction, screenshots, UI tests, and tasks that do not need an existing signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an established account session, single sign-on state, or account-specific dashboard.

Before driving a browser, inspect official documentation, ordinary form actions, page source, and visible request behavior for a supported programmatic path. A form may have an authorized structured submission route that is more reliable than reproducing complex browser interactions.

Do not use undocumented interfaces to bypass access controls, consent boundaries, terms, security controls, payment walls, or anti-abuse protections. If automated browsing is blocked during general research or collection, report the limitation rather than escalating to evade the block. A visible session can be appropriate for an explicitly requested, legitimate task on that site when the user already has authorized access and a normal session is necessary.

Do not use a live authenticated browser merely for convenience when a headless or direct route will work. It can interrupt the user's work and exposes more account and privacy context.

## 3. Protect browser, account, and environment context

When using a visible or authenticated browser:

- Announce that browser control is beginning and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly directs work in an existing tab.
- Explicitly classify the needed context, such as personal, work, test, staging, or production.
- Select the browser profile or session connection for that context directly. Do not rely on generic browser selection, recent-use order, tab titles, or connection labels.
- Confirm the signed-in account and environment using a reliable account indicator before opening or changing the actual target.
- Confirm the target object before editing: for example, the correct record, recipient list, workspace, or subscription.
- Do not disable browser protections, multi-factor authentication, security warnings, access controls, or anti-abuse controls to make automation easier.

Treat browser identity verification as a preflight gate. The minimum question is:

> Which account is active, which environment is active, and what exact item will change?

If an automation system has a verification marker or permission gate, enable it only after the account check has actually passed. Never create a marker early simply to unlock write actions.

For private information about people, access only the records required for the stated task. Omit unrelated sensitive details from screenshots, notes, and reports.

## 4. Separate preparation from commitment

Separate reversible preparation from irreversible commitment.

Preparation can include drafting text, filling fields, selecting options, collecting a preview, or assembling an upload. Commitment includes submitting, sending, publishing, paying, deleting, changing access, or applying a final plan or billing change.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify the resulting state, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Obtain explicit confirmation of the prepared state. Re-check the account, target, and readiness gate, then perform the final action once.

If the page reloads, re-renders, or the session changes between phases, do not assume prior values persisted. Re-inspect, restore if needed, and verify again.

Explicit confirmation is normally required immediately before:

- Sending a message, invitation, notification, or application.
- Publishing content or submitting an externally reviewed form.
- Making a payment, purchase, or donation.
- Deleting records, files, or content.
- Changing subscription, billing, ownership, access, security, or plan settings.
- Taking an action labeled permanent, final, irreversible, or impossible to edit later.

For a reversible, low-risk change that the user explicitly requested, normal verification is usually enough unless the page presents an unexpected warning or broader impact.

## 5. Inspect the rendered page before editing

Do not begin by guessing selectors, using control indexes, or trusting a visual approximation. Inspect the rendered page first.

For each relevant control, determine:

- Its type: single-line input, multiline area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Its accessible name, visible label, placeholder, or explicit label relationship.
- Its current value, required state, disabled state, and validation requirements.
- Whether it is the actual editable element, a wrapper, or a hidden synchronization field.
- Whether changing it or a related control causes a re-render.

Address controls by stable semantic identity: accessible name, visible label, or a label relationship. Do not use DOM order when labels are available, because dynamic applications can reorder or replace elements during loading and re-rendering.

Before editing an existing record or setting, inspect its current state. This helps avoid changing the wrong item or overwriting information unintentionally.

### Generic inspection pattern

Use the chosen browser automation capability to list relevant controls before writing interaction logic. Record at least tag, type, role, label, required state, and current value or text length.

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

## 6. Use the interaction method that matches the control

A generic “set value” action is not reliable for every web control.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use normal text-input interaction | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away | The application may commit on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select existing text, enter text through keyboard-style events, then blur | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, and wait for state to settle | Selection may trigger a full re-render. |
| Checkbox or radio group | Read current state first; change only when needed | A click may toggle an already-correct value. |
| Date or time picker | Select values, close using a neutral page action where possible, then verify the displayed summary | The popover can clear, reinterpret, or reset related values. |
| File upload | Confirm the file, destination, and privacy implications first | Uploading may start immediately and be hard to reverse. |

For framework-driven editors, simulate normal user interaction instead of writing to low-level DOM properties. A robust sequence is:

1. Focus the actual editable element.
2. Select existing text.
3. Delete it.
4. Enter the new text through keyboard-style input.
5. Move focus to a neutral page element to commit the change.
6. Wait briefly for the application to settle.
7. Read the value back.

Some forms pair a visible editor with a hidden input. Changing the hidden input can look successful in an inspection result while server-side validation treats the visible editor as empty. Target the interactive control the application actually reads. If an accessibility locator finds an empty wrapper, inspect the underlying editable control and its label relationship.

If dropdowns, checkboxes, tabs, date pickers, or other controls can refresh the form, set and verify those dependencies **before** filling long or complex text. Re-inspect afterward to ensure earlier values remain present.

## 7. Verify every meaningful edit

After each meaningful field edit or setting change, read the state back from the page. Compare the actual visible or accessible value with the intended value.

For sensitive content, verify a minimal safe representation, such as length, required state, a redacted excerpt, or a checksum-like comparison, rather than placing full private content in logs.

Check specifically for:

- Automation reports success but the field remains empty.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated due to a single-line control or length limit.
- Text displays but was not retained by the application's internal state.
- Editing a later field erased an earlier field after a re-render.
- A hidden synchronization field was changed instead of the visible editor.
- A selection changed a dependent recipient, date, option, validation rule, or required field.

If verification fails, do not continue toward submission. Diagnose the actual control type, retry once with a more suitable interaction method, and verify again. If the page still alters or rejects the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 8. Run a pre-action readiness gate

Before submitting or making any high-impact change, inspect the relevant page state again. Confirm all of the following:

- The correct account, organization, and environment are active.
- The target item is the intended one.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Recipients, options, dates, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final control has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **do not submit**. A partially filled form is usually recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store it only through an appropriate access boundary. Avoid pasting a large table of sensitive field values into a chat or report when a brief summary and a securely available record are enough.

### Readiness checklist

- [ ] Account, environment, and target are verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 9. Confirm completion after acting

A click is not evidence of completion. After a final action, look for reliable evidence such as a success notice, confirmation reference, newly created record, persisted setting, sent item, published page, or changed status that remains after a safe refresh.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, the available evidence, and what remains uncertain. Do not present an attempted action as completed.

## 10. Common failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after a later edit | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline or editor control, or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the underlying labeled control and target the actual editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control that the application reads. |
| The automation layer becomes unstable on a complex page | The selected browser method is unsuitable | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers behave differently | The site varies behavior by browser context | Prefer an authorized direct interface; if a visible session is necessary for an explicit task, verify its account and proceed normally without evasion. |
| A date or option popup changes values unexpectedly | The widget has stateful close, clear, or parsing behavior | Close it through a neutral page action and re-verify all affected fields. |
| A visible error may be cosmetic | The requested task may already have completed | Inspect the resulting state before retrying. |
| Account or environment is uncertain | The wrong profile, tenant, or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
- [ ] Explicit confirmation was obtained immediately before a consequential final action.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing one, assess whether it works, or improve its activation behavior. A skill is a focused set of instructions, with optional resources, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the job, boundaries, and intended users.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review representative outputs with the user and measure objective requirements where appropriate.
5. Improve the skill from evidence rather than intuition alone.
6. Repeat until the skill is useful, reliable, and not narrowly fitted to a few tests.
7. Optionally improve the description that determines when the skill is selected.

Adapt the depth of this process to the user’s needs. Some users want a quick collaborative draft. Others need a careful evaluation and revision cycle. First determine where the user is in the process, then help them make the next useful decision.

## Communication principles

Match the user’s technical familiarity. Use plain language by default. Terms such as *evaluation* and *benchmark* can be useful, but briefly explain them if needed. Avoid unexplained technical terms such as “schema,” “assertion,” or “JSON” unless the user is already using them comfortably.

Explain why questions matter. For example:

> What should a successful result look like: a response in chat, a structured report, a file, or an approved external action? The answer determines how completion should be checked.

Keep the user involved at important decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before imposing restrictive scope, required tools, or approval rules.
- Share proposed test cases before treating them as representative.
- Let human judgment lead for subjective quality such as writing style, visual design, tone, or creative usefulness.
- State assumptions when the user has not provided enough information for a confident choice.

## 1. Determine the starting point

Identify which situation applies.

### A. New skill

The user has an idea for recurring work, such as preparing project updates, reviewing documents, transforming data, or guiding a structured process. Start with discovery and create a first draft.

### B. Existing skill or draft

The user already has instructions and wants them edited, simplified, tested, or improved. Read the current material before proposing changes. Preserve its established name and identity unless the user asks to rename it.

### C. A workflow demonstrated in the conversation

The user may ask to turn a recent interaction into a skill. Extract what can be learned from the conversation before asking repetitive questions:

- Inputs the user supplied.
- Approved information sources and tools used.
- The sequence of decisions and actions.
- Corrections or preferences expressed by the user.
- Output format and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow and identify gaps for the user to confirm. Do not silently convert a one-time workaround into a general rule.

### D. Evaluation or optimization request

The user may have a finished-looking skill and want to know whether it actually helps. Go directly to test design, evaluation, and focused revision. Do not rewrite a skill just because rewriting is possible.

## 2. Capture intent and scope

Gather enough information to define a coherent job. Adapt these questions to the situation rather than asking all of them mechanically.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What kinds of requests, wording, or contexts should make this skill relevant?
3. **Inputs:** What information, files, examples, systems, or permissions may it use?
4. **Outputs:** What should it produce, change, or recommend? Is a format required?
5. **Success criteria:** How will the user know the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask, stop, decline, or hand a decision back to the user?
7. **Variations:** What common cases, difficult cases, or meaningful exceptions matter?
8. **Dependencies:** Does it need a particular capability, reference, template, script, or user-provided access?
9. **Testing:** Should it be tested with example requests before release?

Recommend testing when outputs can be checked objectively, the workflow is consequential, the skill will be used repeatedly, or errors could be costly. For highly subjective work, recommend a smaller qualitative review instead of inventing misleading numerical metrics.

When helpful, offer explicit choices:

- Should the skill make a low-risk best effort when information is missing, or stop and ask?
- Should it use a concise default output, a detailed default output, or let the user choose?
- Should it use any available source, or only user-approved sources?
- Should it prepare a draft, or take an external action after confirmation?

### Research and source boundaries

If relevant documentation, prior examples, standards, or similar skills are available, review them before drafting. Research should reduce burden on the user, not override their authority over requirements.

If the workflow uses private communications, records, or information about people, proceed only with a legitimate purpose and clear authorization. Use the minimum relevant sources and information. Exclude unrelated personal details, respect consent and privacy expectations, and keep outputs within the appropriate access boundary. Do not use private material merely because it is technically accessible.

Use research to identify:

- Existing conventions and output standards.
- Constraints imposed by the user’s chosen system or file format.
- Reusable patterns from comparable work.
- Safety, privacy, compliance, and approval requirements.

If sources conflict or requirements remain uncertain, surface the uncertainty rather than guessing.

## 3. Choose the skill structure

A skill should be focused enough that users and the AI can predict what it does. One skill may support closely related variants, but separate unrelated jobs when they have different users, access boundaries, sources of truth, or definitions of completion.

A typical package may contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional supporting documentation
├── assets/                  # Optional templates or resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help determine whether to select the skill.
2. **Core instructions:** The process needed for most requests.
3. **Supporting resources:** Detailed references, templates, and scripts loaded only when relevant.

Keep the main instruction file readable. If it becomes large, move specialized material into clearly named references and state exactly when each reference should be used. Give long references a contents list or clear navigation.

For skills with several variants, organize resources by variant. The core instructions should explain how to select the relevant path, rather than requiring the AI to read every reference by default.

### Use reusable helpers carefully

If evaluations show that the AI repeatedly rebuilds the same reliable procedure, consider bundling a helper script, template, or checklist. A reusable helper is most valuable when it is:

- Deterministic or easier to verify than free-form reasoning.
- Reused across many requests.
- Less error-prone than recreating the procedure each time.
- Clearly within the user’s intended permission scope.

Document what each helper does, its inputs and outputs, its limitations, and when not to use it. Do not automate sensitive, destructive, or external actions without clear approval points.

## 4. Write the skill

Write in clear, imperative language. Explain the purpose behind important steps, especially when a rule prevents a predictable failure. A capable AI can adapt better when it understands the goal and tradeoff than when it receives a long list of unexplained prohibitions.

Include the following sections as appropriate.

### Purpose and scope

State the job, intended use, and boundaries. Make clear whether the skill produces advice, a chat response, a file, a draft, or an external action.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State what to do when something required is absent.

```markdown
Before preparing the report, confirm the reporting period and approved data source.
If the source is unavailable, ask for an export or prepare a draft clearly marked as incomplete.
```

### Workflow

Give the normal sequence of actions and include meaningful decision points. A durable workflow commonly follows this pattern:

1. Inspect the request and available inputs.
2. Clarify only where an answer would materially change the work.
3. Gather evidence from approved sources.
4. Perform the task using the suitable method.
5. Check the result against format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limitations.

Use conditional instructions when they help:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested action could overwrite work or create an external commitment, explain the impact and request confirmation first.
```

### Output format

When consistency matters, provide an exact or near-exact template.

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding supported by evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing information]
```

Avoid rigid templates when usefulness depends on adapting to context. In those cases, specify goals, ordering, and examples rather than a fixed shell.

### Quality, safety, and privacy checks

State what must be checked before completion. Examples include validating calculations, confirming required sections, preserving original data, identifying the source of key claims, or flagging uncertain information.

The skill’s behavior should match what a reasonable user expects from its description. Do not conceal actions, bypass authorization, expose confidential information, facilitate unauthorized access, or take destructive action without confirmation. If a request exceeds authorization or creates material risk, explain the limitation and offer a safer alternative where possible.

### Failure behavior

Describe recovery from general failure types:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or source:** Explain what cannot be verified and offer an alternative method.
- **Ambiguity:** Make a reasonable low-risk assumption if it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the output as complete. Correct it, report the issue, or seek guidance.
- **Permission-sensitive action:** Pause before irreversible, external, or high-impact changes.

### Examples

Use a small number of generalized examples only when each teaches a distinct decision pattern. Examples should illustrate reasoning, not replace it with narrow rules.

## 5. Write a strong skill description

The description is a routing instruction: it tells an AI what the skill does and when it is relevant. It should cover realistic user wording, including requests that imply the task without naming it directly.

A useful description includes:

- The task or outcome.
- Common contexts or phrasing that indicate the task.
- Important scope boundaries when they prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a leadership update, progress report, milestone review, risk summary, or a concise account of next steps, even if they do not use the phrase “status report.”
```

Do not put the full workflow in the description. Do not rely on vague labels such as “help with documents.” Do not make it so broad that it captures adjacent work better handled by another skill.

## 6. Review the draft before testing

Read the skill as if seeing it for the first time. Check:

- Is the job coherent and bounded?
- Does the description explain when to use it?
- Are inputs, permissions, and outputs clear?
- Does the workflow explain important quality checks?
- Does it say what happens when information is missing?
- Are there unnecessary rules, repeated wording, or brittle instructions?
- Does it depend on undeclared tools, personal habits, or private access?
- Can a capable AI handle normal variation without becoming constrained by the wording?

Prefer lean, understandable instructions over a long list of rigid commands. Excessive absolute language is a warning sign unless the behavior concerns a genuine safety, privacy, or authorization boundary.

## 7. Design realistic test cases

After the draft is stable enough to test, create two or three realistic test prompts. Share them with the user and invite corrections or additions before relying on them.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Any supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

A portable test record can look like this:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and flag information that cannot be verified.",
      "expected_output": "A structured summary that separates verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover different meaningful situations:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic variation that changes the workflow.
- A request that should require approval, decline, or privacy protection when relevant.

Do not make tests merely repeat the skill’s phrasing. Vary wording, detail level, and user sophistication. Avoid retaining unnecessary private context in prompts or fixtures.

## 8. Run comparisons and preserve evidence

When independent execution is available, compare the skill against a meaningful baseline:

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged copy before editing, then compare the revised version with the prior version.

Run comparison conditions under comparable circumstances. If parallel execution is available, start all skill and baseline runs together to reduce timing differences and avoid changing one condition after seeing another result.

Store each iteration clearly, for example:

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

For every run, retain the prompt, permitted inputs, output, evaluation criteria, and available metadata such as elapsed time or resource use. Capture timing immediately if the execution environment reports it, since it may not remain available later.

If independent runs are unavailable, perform a transparent sanity check: follow the skill on each test request, save the results, and ask the user to review them. Do not present this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While test runs are underway, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and connected to user value:

- Required sections are present.
- A produced file opens and contains required fields.
- Calculated values match a known approved source within an agreed tolerance.
- The output identifies missing mandatory information.
- Claims include source references when required.

Record each check with a clear statement, a pass/fail result, and evidence:

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

Use programmatic validation when practical. Reusable automated checks are generally more reliable than visual inspection. Do not force numerical checks onto subjective work: tone, writing quality, design, usefulness, and strategic judgment often require human review.

## 10. Review results with a human

Present outputs and measurements in a form the user can inspect. Use an available review interface when one exists; otherwise present accessible files or a clear in-conversation comparison.

For each test case, show:

- The original prompt.
- Relevant permitted inputs.
- The skill output and comparison output, if available.
- Objective grades and evidence.
- Timing or resource data, if available.
- A way for the user to state what worked and what should change.

Ask focused questions:

- Which result would you trust in ordinary use, and why?
- Did the skill add steps or detail that were not valuable?
- What was missing, misleading, unsafe, or difficult to use?
- Would it work for a similar request with different wording or data?

Treat empty feedback as a useful signal for that case, not proof that every future case is solved.

## 11. Analyze results beyond pass rates

Aggregate results where possible: pass rate, elapsed time, resource use, and variation. Then inspect patterns that summary statistics may hide:

- **Non-discriminating checks:** Both versions pass, so the check does not measure the skill’s added value.
- **High variation:** Comparable runs differ substantially, suggesting ambiguity or unreliable instructions.
- **Tradeoffs:** Quality improves, but time or resource cost may be too high.
- **Failure concentration:** Several failures share one cause, such as unclear source selection or missing output rules.
- **Unproductive work:** Execution records show redundant planning, research, or formatting.
- **Repeated reconstruction:** Multiple runs recreate the same helper process, indicating a reusable resource may help.

For consequential decisions, consider a blind comparison. Give an independent reviewer two outputs without revealing which version produced each, use a shared rubric, record the judgment, then reveal the mapping. Judge role-relevant qualities such as correctness, completeness, clarity, adherence to constraints, safety, and practical usefulness.

## 12. Improve without overfitting

Revise the smallest part of the skill likely to fix the underlying cause. Generalize from feedback instead of adding rules that only match one test.

For example, if a report fails to distinguish unsupported claims, do not add a rule mentioning only that report. Clarify the broader principle: distinguish verified information, assumptions, and unavailable evidence whenever sources are incomplete or mixed.

Use these improvement principles:

1. Fix causes, not isolated examples.
2. Keep instructions lean and remove guidance that does not change outcomes.
3. Explain intent so the AI can adapt intelligently.
4. Add scripts, templates, or references only when repeated work justifies them.
5. Preserve behavior the user already values.
6. Add tests only for genuine classes of failure, not every one-off event.

After revision, rerun the full test set in a new iteration. Use the same baseline policy, compare against prior outputs where useful, and collect feedback again.

Stop when the user is satisfied, meaningful cases are consistently successful, objective requirements are reliably met, or further edits are not producing useful improvement.

## 13. Optimize activation behavior

After the workflow itself is stable, evaluate the description that controls when the skill is selected.

Create a realistic set of activation queries containing both cases that **should activate** the skill and difficult nearby cases that **should not**. Use roughly balanced coverage. Queries should be substantive enough that consulting a skill would be useful.

Positive cases should vary by:

- Formal and casual language.
- Direct and implied requests.
- Common and less common valid uses.
- Situations where a related skill might compete.

Negative cases should be near-misses rather than obviously irrelevant requests. They should share terms or concepts with the skill but require a different job, different access, or different conditions.

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

Review the query set with the user before using it. If repeated activation testing is available, separate improvement queries from held-out queries used to choose the final description. Select the description that performs best on held-out cases, not merely the one that fits the examples used for editing.

Remember that simple one-step requests may be handled directly without selecting a specialized skill. Test requests should therefore be complex enough that the skill would add real value.

## 14. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not rely on private conventions, undeclared access, or a specific proprietary tool.
- References and helpers are present, clearly named, and documented.
- No credentials, identifiers, confidential records, or unnecessary sensitive examples are included.
- The user can adapt the skill to their chosen environment.
- Test material is retained only if it is safe and useful to keep.

Provide a handoff note stating what the skill does, required capabilities, known limitations, approval boundaries, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has:

- A clear, bounded job.
- A description that routes appropriate requests.
- Instructions that handle normal variation.
- Explicit behavior for uncertainty, authorization, privacy, and high-impact actions.
- Evidence from realistic use that it improves outcomes.
- A package that another user can understand and adapt without relying on hidden personal context.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for real recurring work.


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

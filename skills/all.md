# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set while preserving the user’s final choice.
---

# Brainstorm options

Use this workflow when a user needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long idea list: surface genuinely different paths, make their tradeoffs clear, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources that the current environment can access, review the relevant material first.

Only access private communications, records, or documents when there is a legitimate purpose, clear authorization, and an appropriate access boundary. Use the minimum relevant sources and information. Do not include unrelated personal, confidential, or sensitive details in the output.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, ownership boundaries, or deadlines
- Evidence about what has already been tried
- Relevant stakeholder needs or operational dependencies

Do not search broadly by default. Use targeted retrieval. If important information is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- Important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The user’s wording may describe a symptom or a preferred solution rather than the underlying decision. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, low-consequence, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must represent a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes process, incentives, scope, timing, or the problem framing
- At least one surprising option, such as delaying, partnering, removing scope, or deliberately doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, avoided distraction, or preserving resources has genuine value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

| Element | Include |
|---|---|
| **What** | One or two sentences explaining the approach. |
| **Strengths** | One or two concrete advantages. |
| **Weaknesses** | One or two concrete disadvantages, risks, or limitations. |
| **Effort** | Low, Medium, or High; use a rough, context-appropriate estimate. |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option appear stronger by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose evaluation criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, evidence strength, and stakeholder burden. Add domain-specific criteria when they matter more than these defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but clearly explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this user’s situation, constraints, and goals—not merely why it is attractive in general.
4. Name the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may:

- Choose an option
- Request more detail on a specific option
- Correct the framing or constraints
- Ask for additional options
- Combine options into a hybrid

If the user proposes a hybrid, test whether its components are compatible and whether the combination resolves a real tradeoff rather than simply adding complexity.

Do not begin implementation merely because an option appears promising. Move into execution only after the user selects or explicitly authorizes a path.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence, reversibility, and implementation needs:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that identifies the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After the decision is recorded, move into planning and execution: requirements, milestones, tasks, ownership, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Response template

Use the following structure for a typical response:

```markdown
## Decision framing
[Two to four sentences describing the actual decision, constraints, and success criteria.]

## Options

### [Memorable option label]
- **What:** [Approach.]
- **Strengths:** [Concrete advantages.]
- **Weaknesses:** [Concrete disadvantages or risks.]
- **Effort:** [Low / Medium / High]

### [Memorable option label]
- **What:** [Approach.]
- **Strengths:** [Concrete advantages.]
- **Weaknesses:** [Concrete disadvantages or risks.]
- **Effort:** [Low / Medium / High]

## Assessment
- **Not recommended:** [Any option with a dealbreaker, and why.]
- **1. [Recommended option]:** [Why it fits this situation.]
- **2. [Recommended option]:** [Why it fits this situation.]
- **3. [Recommended option, if useful]:** [Why it fits this situation.]
- **Ranking could change if:** [Key assumption or missing evidence.]

## Next step
[Ask the user to choose, request detail, revise the framing, or propose a hybrid.]
```

## Quality checks

Before sending, verify that:

- The framing reflects the actual decision rather than only the first solution proposed.
- The options are truly distinct and not minor variants of one another.
- The option set includes the obvious path and, where useful, a genuinely different or surprising path.
- Strengths and weaknesses are concrete and candid.
- Effort labels are plausible for the stated context.
- Recommendations follow the user’s criteria and constraints rather than default assistant preferences.
- The response does not expose unnecessary private, sensitive, or irrelevant information.
- The response ends by returning control to the user rather than prematurely starting implementation.


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
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing a single idea too early can become an exercise in defending it.

If the same idea was tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.

## Rules of engagement

- Be direct. Do not treat confidence as evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before continuing.
- Use available evidence, such as research, metrics, prior experiments, customer feedback, documented decisions, and stakeholder input. Distinguish facts, inferences, and forecasts.
- If reviewing internal communications, records, or information about people, do so only for a legitimate purpose with clear authorization. Use the minimum relevant sources, omit unrelated sensitive details, and keep findings within the appropriate access boundary.
- Refer to dissenters by relevant role, such as finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, starting with the assumption most likely to undermine the decision.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [How to test or disprove it] |

Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, target group, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions and adapt later questions to the answers received. Do not present the full list as a questionnaire, because that enables selective answering.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that view been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence. Ask what observed behavior, data, comparison, or commitment supports the belief.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failure, external changes, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable signal] | [Name the check or accountable role] |

The warning sign must appear early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap; do not assume silence means agreement.

Dissent is not an automatic veto. Its purpose is to reveal constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test incomplete or failed rather than approving the idea.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step:

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

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the appropriate solution is not already clear. Do not use it for a small fix or routine task with a known implementation.

By default, work from understanding through implementation. If the requester asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the proposed solution. If someone asks to “build X,” work backward:

- Who experiences the problem, and in what role or situation?
- What are they trying to accomplish?
- How does the work happen today?
- What workarounds, failures, delays, or risks exist?
- How frequent, costly, urgent, or blocking is it?
- What outcome would meaningfully improve the situation?

Write a concise problem statement and descriptive requirements. State desired outcomes and constraints rather than assuming a particular implementation. If the proposed solution does not appear to solve the underlying problem, say so directly and explain why.

Ask only for information that cannot reasonably be found in authorized project context, documentation, code, or relevant records. When accessing records about people, use them only for a legitimate, authorized purpose; review the minimum relevant material; and omit unrelated or sensitive personal details.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Treat “do nothing,” “deprioritize,” or “improve the current workaround” as valid options when the problem is rare, low-impact, or adequately handled already.

Distinguish between reversible choices and hard-to-reverse commitments:

- **Reversible choices:** Small, easy-to-change decisions. Use reasonable judgment, choose a path, and proceed.
- **Hard-to-reverse commitments:** Public interfaces, persistent data changes, migrations, long-lived settings, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the decision, alternatives, and rationale when the impact warrants it.

If direction or priority remains unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in extensive design or implementation.

## 3. Research the current context

Read relevant project guidance, architecture notes, repository instructions, service documentation, existing code, tests, operating procedures, and prior attempts. Look for established patterns and reusable components before creating a new approach.

Identify relevant constraints, including compatibility, supported environments, security expectations, ownership boundaries, deployment practices, observability, and operational support. Follow existing conventions unless there is a clear, documented reason to depart from them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. For example:

| Criterion | Example expectation |
|---|---|
| Compatibility | Must preserve current authentication and existing data behavior. |
| Delivery | Must fit the available time and maintenance capacity. |
| Complexity | Should avoid unnecessary dependencies, settings, and special cases. |
| Verification | Must have a clear test and validation method. |
| Reversibility | Should be removable or recoverable if it does not work. |

These criteria guide both option generation and selection. Without them, the first plausible solution can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution, such as clearer instructions, a process change, a template, or an existing platform capability.
3. A small, targeted technical change.
4. A larger integrated solution.
5. Building internally, purchasing a service, or integrating an existing service.

For an ambiguous problem, generate a wider candidate set before narrowing. Keep each option concise: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-specific special cases.
- Validate inputs and fail clearly for invalid states. Do not hide programmer errors by returning plausible but incorrect results.
- Prefer established conventions over flexible abstractions, and flexible abstractions over permanent configuration.
- Treat new fields, settings, and public interfaces as long-term maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and available infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Put changes in the appropriate design boundary; avoid quick fixes that create hidden coupling.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal containing:

- Problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Keep proposals direct. Store them in the requester’s approved shared documentation system when durable review or collaboration is needed; otherwise provide them in the current workspace. Use a clear title, such as `DD MMM YYYY: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, data or migration strategy, rollback approach, test strategy, deployment steps, and follow-up ownership.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm results against the evaluation criteria, including compatibility and failure behavior.

Do not claim success based only on completed code. State what was actually tested and what remains unverified. Commit, publish, or deploy only under the requester’s repository, review, release, and access practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and its results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set where applicable.

Keep the handoff focused on useful outcomes and operational facts rather than temporary implementation detail.


---
name: shape-and-draft
description: Shape consequential documents by reviewing evidence, resolving material choices with authorized decision-makers, checking readiness, then drafting and auditing the smallest document that can achieve the goal.
---

# Shape and draft a document

Develop an important document by shaping the thinking behind it before writing. Determine what the document must achieve, gather relevant evidence, resolve material choices with the appropriate authorized decision-maker, and then draft the smallest document that can do the job.

Use this workflow for strategies, narratives, operating agreements, proposals, scorecards, and decision memos when the artifact, argument, boundaries, commitments, or operating model are not yet settled. Do not use it for a quick edit, a formatting request, or a document whose content and decisions are already specified.

## Classify the request

The request may name a document type, desired outcome, audience, source material, or some combination. Treat a proposed document type as a hypothesis until its purpose is clear.

Use a **full shaping process** when the document is strategically consequential and material choices remain unsettled, or when the requester asks for deep thinking, multiple rounds of questions, or close alignment before drafting.

A substantive interview round resolves a distinct layer of choices and uses the answers to determine the next questions. Restating prior discussion or asking for general approval is not a substantive round.

## 1. Work backwards from the outcome

Start with the change the document must produce. Establish:

- Who will read it.
- What readers should understand, decide, approve, or do afterward.
- What is unclear, contested, blocked, or currently going wrong.
- Whether the document mainly needs to explain, persuade, decide, coordinate, or govern.

Do not accept “write a narrative” or “make a strategy page” as the goal. Identify the actual job the document must perform.

## 2. Choose the artifact

Recommend the form that best serves the job:

- **Narrative:** Builds shared understanding of why something matters and what bet is being made.
- **Strategy:** Connects a diagnosis to choices, priorities, outcomes, and exclusions.
- **Operating agreement:** Defines ownership, interfaces, decision rights, handoffs, and cadence.
- **Decision memo:** Records a choice, alternatives, rationale, risks, and review point.
- **Scorecard:** Defines a role or team mission, outcomes, and role-relevant capabilities.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the important tradeoff and recommend one. If the form would materially affect the argument, structure, or decisions required, ask the authorized decision-maker to confirm it before proceeding.

## 3. Gather and classify evidence

Read supplied material first. Follow any stated rules for source selection, authority, citations, and linking. Scale the evidence sweep to the stakes and use only sources and systems that are available and appropriate for the task.

When using private communications, internal records, or information about people, confirm there is a legitimate purpose and clear authorization. Use the minimum relevant sources and information, omit unrelated or sensitive personal details, respect consent and privacy expectations, and keep the resulting document within its appropriate access boundary.

For a consequential internal document, seek material that may contain prior decisions, current definitions, supporting evidence, dissent, constraints, ownership context, and relevant performance information.

Apply these rules:

- Respect any stated hierarchy of sources.
- Prefer current, authoritative decision records over discussion notes, recollections, generated summaries, or repeated claims.
- Resolve contradictions where evidence permits and surface material contradictions that remain.
- Do not ask participants for factual information that available sources can answer.
- Do not edit, overwrite, or otherwise change source material unless explicitly instructed.

Keep evidence separate from alignment:

- Sources can establish what happened, what was recorded, what people said, and what an authoritative record currently states.
- Sources do not automatically establish what the current decision-maker believes, is willing to promise, or chooses to exclude.
- A plausible synthesis, repeated pattern, or implication is an **inference**, not a settled decision.
- Ask for confirmation of any inference that would become a central claim, commitment, boundary, recommendation, or operating rule.

Before the first interview round, provide a short situation brief covering:

- What the sources establish.
- What has already been explicitly confirmed.
- What is inferred but unconfirmed.
- The main tension, gap, or missing logic.
- The recommended artifact.
- The important questions that only an authorized decision-maker can resolve.

## 4. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds already completed in the current conversation and do not repeat answered questions.

Do not draft immediately after the first round merely because one apparent central issue has been resolved. Use a later round to test consequences: boundaries, tradeoffs, counterarguments, ownership, definitions, or execution implications.

Ask four to eight focused questions per round. If fewer than four material questions remain, ask all of them and state that this is a narrow final check. Do not add ritual questions merely to reach a number.

Each numbered question should normally seek one decision. Do not combine separate choices, such as ownership, coordination, handoffs, and success measures, into one broad yes-or-no question. Bundled questions create false alignment.

Use a compact format that supports quick answers:

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
- **Source facts:** Claims established by current, authoritative evidence but not selected as current choices.
- **Inferred:** Plausible interpretations that remain unconfirmed.
- **Open:** Questions that could materially change the document.
- **Corrected:** Assumptions or claims that a participant has rejected.

Update this ledger after every answer round. Never reintroduce a corrected assumption. If confirmed statements conflict, surface and resolve the conflict rather than hiding it in vague language. Never promote an inference to confirmed solely because several sources support it.

For a full shaping process, show a concise version of the ledger before each later round. Every major draft claim must be a confirmed choice, a supported source fact, or explicitly framed as a proposal, assumption, or open question.

## 6. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document’s substance. Before drafting, provide a concise pre-draft synthesis covering the intended job, audience, central position, important boundaries, and deliberate open questions.

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
- Keep action or onboarding sections to no more than seven top-level bullets and prefer five or fewer for the main outcome section. Combine points or move supporting detail to an appropriate reference when necessary.
- Prefer the more concise version when it preserves meaning. Concision removes unnecessary ideas and words; it does not require every sentence to be short.
- Preserve hard ideas when they matter, but explain them in plain language rather than jargon.

Honor the requested destination using the chosen system. If text is requested in the conversation, provide text without changing source material. If a document must be created or updated elsewhere, do so only as instructed and verify that the intended content is present, structurally correct, and readable in its rendered form. In particular, inspect lists, headings, indentation, and page breaks so headings do not accidentally inherit list formatting and no empty spacer paragraphs create poor layout.

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
description: Learn a paper, article, post, or topic through a short Socratic dialogue that builds durable understanding with retrieval, explanation, challenge, and application rather than passive summary.
---

# Learn with a tutor

Help a learner understand, retain, and use a provided paper, article, post, or topic through a rigorous dialogue. Prioritize active recall and reasoning over explanation. The learner should do most of the intellectual work; the tutor guides, diagnoses, and adjusts the challenge.

## Learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to recall and reconstruct ideas in their own words.
- **Ask for mechanisms.** Go beyond conclusions: ask why, how, under what conditions, and with what evidence an idea works.
- **Have the learner generate connections.** Ask for their own examples, analogies, predictions, and applications before supplying any.
- **Use productive difficulty.** Make the task effortful enough to build learning, but not so difficult that the learner cannot make a meaningful attempt.
- **Practice transfer.** Move from the original material to unfamiliar cases, related concepts, and practical decisions.
- **Surface gaps through questions.** When an answer is incomplete or inconsistent, use a focused question to make the tension visible. Explain directly only after a fair chance to reason.

## Readiness check

Before beginning, establish the learning context with one or two open questions:

- “What do you already think is true about this topic, and why?”
- “What are you trying to be able to explain, evaluate, or do?”
- “Have you read the material, or are you starting from an initial impression?”

If the learner has not engaged with the source, ask for a prediction or working model first. Then ask them to inspect a relevant section before continuing with retrieval. Do not replace this step with a full tutor-led explanation unless the learner explicitly asks for one.

## Conversation workflow

### 1. Elicit the central idea

Ask the learner to state the main argument, finding, or concept from memory, without quoting the source.

Useful prompts:

- “In your own words, what is the main claim?”
- “What problem is this idea trying to solve?”
- “Why should someone believe this claim?”
- “If you had 30 seconds to explain it to a thoughtful friend, what would you say?”

### 2. Choose a few high-value ideas

Do not attempt to cover every detail. Select two or three ideas that are central, difficult, consequential, or likely to be misunderstood. Go deep rather than broad.

For each selected idea, use this cycle:

1. Ask the learner to reconstruct the idea.
2. Probe the reasoning, evidence, assumptions, or causal story.
3. Ask for a self-generated example, analogy, or application.
4. Test the idea with an objection, boundary case, or alternative explanation.
5. Adjust the next question to the learner’s actual answer.

Keep turns brief: usually ask one or two questions at a time.

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

Avoid questions that can be answered only with yes or no. If a binary choice is useful for reducing difficulty, immediately ask the learner to defend the choice.

## Responding to learner answers

Be warm, direct, and specific. Avoid generic praise. If an answer is strong, name what made it useful—such as identifying an assumption, distinguishing correlation from causation, or giving a relevant counterexample—then raise the level of challenge.

When an answer is wrong or incomplete:

1. Do not immediately provide the correction.
2. Ask a focused follow-up that reveals the tension or missing step.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, give a concise explanation of the relevant distinction.
5. Ask the learner to restate the corrected idea or apply it to a new case.

If the learner says, “I don’t know,” invite a low-stakes attempt: “Take a guess based on what you do know. What seems most plausible, and why?” Give a hint after an attempt, or sooner when the learner lacks necessary background.

## Calibration and pacing

Increase difficulty when the learner answers comfortably: ask for a counterexample, comparison, prediction, objection, or application in a different domain.

Reduce difficulty when the learner is lost: narrow the question, isolate one assumption, use a simpler case, or ask them to compare a small number of explanations and defend one. Match the learner’s energy: go deeper when they are engaged; when they are overloaded, consolidate rather than introduce more material.

Maintain a dialogue, not a fixed quiz. Each question should build on evidence from the learner’s previous answer.

## Progress checks

Periodically give a brief, evidence-based check-in that states:

| Check | What to report |
|---|---|
| Demonstrated understanding | [What the learner has accurately explained, reasoned through, or applied.] |
| Remaining uncertainty | [What is still incomplete, confused, or unsupported.] |
| Next focus | [The most useful concept, assumption, or application to examine next.] |

Do not claim mastery because the learner recognizes terminology or repeats a conclusion. Look for accurate explanation, sound reasoning, and transfer to a fresh case.

## Closing gate

Before ending, convert the discussion into action. Ask:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then request either a concise final explanation in the learner’s own words or a future retrieval prompt they can answer later. End by naming the next concept or question worth revisiting.

## Guardrails and audit

- Do not summarize the material unless the learner explicitly requests it; even then, invite their own summary first.
- Do not lecture when a well-chosen question can make the learner retrieve or infer the point.
- Do not define jargon automatically; first ask the learner what they think it means, then clarify if necessary.
- Do not make the interaction easy merely to be encouraging.
- Do not cover an entire source superficially when a few core ideas can be understood deeply.
- Keep the exchange roughly question-led, with explanations used only to unblock, correct, or consolidate learning.
- Before closing, verify that the learner has retrieved, explained, tested, and applied at least one important idea rather than merely discussed it.


---
name: write-in-my-voice
description: Draft or revise email in the user’s authentic voice by using an approved style profile and relevant writing examples, while verifying facts, commitments, privacy, and recipient fit before producing copy-ready text.
---

# Write in my voice

Use this workflow when the user asks to draft, reply to, revise, or polish an email on their behalf.

## Goal

Produce a concise, send-ready email that sounds like the user rather than generic assistant prose. Match the user’s established voice while keeping the message accurate, appropriate for the recipient, and limited to supported commitments.

## 1. Load the voice profile first

Before drafting, read the user’s current writing profile in full, if one is available. The profile may include:

- Greeting and sign-off patterns.
- Formality, warmth, directness, and relationship cues.
- Typical sentence and paragraph length.
- Preferred wording, contractions, punctuation, and formatting.
- Words, phrases, tones, or punctuation to avoid.
- Guidance for requests, follow-ups, declines, corrections, and apologies.
- Approved reusable facts, links, boilerplate, and standard replies.

Use recent emails the user actually sent as supporting evidence, especially messages with a similar audience and purpose. More recent, repeated patterns outweigh older examples. If the profile and recent examples conflict, ask which preference is current or follow the most recent consistent pattern.

If accessing email, drafts, sent messages, or records involving other people, do so only for a legitimate purpose with clear authorization. Use the minimum relevant material, avoid exposing unrelated personal or sensitive information, and keep the draft within the user’s appropriate access boundary.

## 2. Establish the email brief

Identify the minimum information needed to write safely:

1. Who is the recipient, and what is their relationship to the user?
2. What outcome should the email achieve?
3. What facts, dates, names, links, attachments, or decisions must appear?
4. What action is requested, who owns it, and when is it needed?
5. Are there sensitivities, confidentiality limits, approval requirements, or risks?

Do not invent availability, promises, pricing, decisions, opinions, emotional reactions, links, or attachments. Ask a focused clarification question when a missing fact would materially change the message.

## 3. Adapt voice to context

Preserve recognizable voice without treating every recipient the same.

| Situation | Adaptation |
|---|---|
| Familiar colleague or ongoing contact | Use the user’s normal level of brevity and familiarity. |
| New, external, senior, or formal recipient | Keep the user’s voice, but add enough context and care to prevent ambiguity. |
| Request or follow-up | State the action, owner, and timing plainly. |
| Correction, decline, or conflict | Be direct and factual. Avoid defensiveness, exaggerated praise, and unnecessary apologies. |
| Sensitive matter | Use only necessary details and avoid forwarding or restating private information without a clear need. |

Use approved standard wording, facts, or links when relevant. Do not reuse boilerplate when it would be inaccurate, stale, or misleading.

## 4. Draft the smallest complete message

Use this default structure unless the user’s profile indicates otherwise:

1. Greeting, if customary.
2. Purpose, answer, or decision in the first sentence.
3. Essential context and the requested action or next step.
4. Closing and sign-off, if appropriate.

Prefer active verbs, concrete nouns, short sentences, and short paragraphs. Use bullets only when they make actions, options, or logistics easier to scan.

Remove content that does not help the recipient understand or act, including:

- Throat-clearing, process narration, and assistant commentary.
- Generic compliments, repeated thanks, and empty pleasantries.
- Filler such as “just wanted to” unless it is both natural to the user and useful.
- Hedging that weakens a clear message.
- Unsupported claims or commitments.

## 5. Audit before presenting

Review the draft line by line:

- Does it plausibly sound like the user?
- Do the greeting, sign-off, punctuation, rhythm, and level of directness match the evidence?
- Is the tone appropriate for this recipient and the stakes?
- Are names, dates, links, attachments, and references correct?
- Did the draft add any unsupported commitment, claim, feeling, or decision?
- Is the requested action unmistakable?
- Does it reveal only information needed for the recipient and purpose?
- Can any sentence be removed without reducing usefulness?
- Does it avoid the user’s stated anti-patterns?

If no voice evidence exists, use a broadly useful default: clear, warm-professional, concise, and direct. Briefly state that assumption when needed, and invite the user to provide a style guide or a few representative sent emails for future drafts.

## Output

Provide the final email as copy-ready text. Ask only the specific clarification needed when required. Do not add explanation after the draft unless the user asks for alternatives, reasoning, or revision notes.


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
description: Review authorized meeting records to identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date range, or for a manually supplied list of meetings. It is tool-independent: use any meeting-record source, transcript capability, and task system that the user is authorized to access.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine unfinished commitment that should be tracked.

## Purpose, access, and operating rules

Use this workflow only for a legitimate work or personal purpose and with clear authorization to access both the meeting records and the task system. Retrieve only the minimum records and passages needed to identify commitments. Keep task notes within the access boundary of the task system: omit unrelated personal information, sensitive details, and private discussion that is not necessary to complete the task. Respect participant consent, applicable policies, and retention expectations.

Before each run, apply these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same counterparty or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels something as an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. An idea, statement of interest, request, or open question is not a task unless someone accepted responsibility for a concrete outcome. Apply delegation boundaries supplied by the user or maintained in an authorized responsibility reference. Attendance at a meeting does not make the user accountable for all work discussed there.

## 1. Select the meeting scope

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect only what is relevant:

- Title, date, and time.
- Meeting-record reference or link, if the task audience is permitted to access it.
- Attendees, when needed to establish ownership or perform a follow-up.
- Transcript, notes, summary, and relevant linked context.

Report a compact count before processing. Do not infer actions from a meeting title alone.

## 2. Fetch and inspect complete records

Fetch complete meeting records in parallel when the selected system supports batching. Do not search for existing tasks yet: first identify people, topics, and candidate outcomes so that duplicate checks are accurate.

For long transcripts, use a repeatable search, extraction, or chunking method rather than relying on truncated previews. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by explicit acceptance.

Review summary action items as candidates, then verify them against the transcript and nearby discussion. A stated promise may have been conditional, reassigned, fulfilled live, or directed at another attendee.

## 3. Triage each meeting

Classify the meeting loosely. Classification is a starting expectation, not a rule that overrides evidence.

| Meeting type | Usual outcome | Guidance |
|---|---:|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or explicitly timed follow-up. |
| Information-gathering, interview, or reference call | 0 tasks | Create work only for an explicit out-of-meeting commitment. |
| Internal planning or team meeting | 0–1 user-owned task | Capture the user’s deliverable, not the full team action list. |
| Coaching or recurring one-to-one | 0–1 task | Create a task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1–2 tasks | Often separate an internal decision from an external response. |

For every meeting, identify:

- Relationship context and why the meeting occurred.
- Candidate actions owned by the user.
- Work actually completed during the meeting.
- Work delegated to another named owner.
- Explicit future commitments and timing.
- Enough neutral context for a task to remain understandable weeks later.
- Relevant source references and related materials that the task audience may access.

Create no task when work was completed live, another person owns it, the meeting was purely informational and any needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

A live completion requires evidence that the deliverable was actually provided or created during the meeting, not merely that someone said they would do it. For example, material shared in the meeting may close a promise to send that same material.

## 4. Decide the task shape

Combine actions into one task when they have the same counterparty, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect months later.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

This is a readiness gate: do not create a task until it has a clear owner, an unfinished outcome, a sensible shape, and enough context to stand alone.

## 5. Write the task

Use the user’s chosen task system and field names. At minimum, capture:

- **Title:** short, verb-led, and specific, such as “Follow up with partner about pilot scope.”
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user’s scale; default to normally important work and reserve the highest level for a real deadline, material risk, or waiting counterparty.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and permitted references.

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: agreed date, or a reasonable reminder date before it.
- Weekly or sprint commitment: next relevant review or planning session.
- Flexible work: roughly one week, adjusted to workload.
- Older meetings processed late: move an immediate follow-up to the next workable date rather than assigning an already-passed date, unless the original deadline still applies.

Do not raise priority merely because capture happened late. Raise it only for a real deadline, material risk, or an external party awaiting a response within a short time frame.

### Notes template

```markdown
[Two or three sentences of time-independent context. Include relevant absolute
dates, why this matters, the commitment, and necessary sensitivity. Omit
unrelated or sensitive personal details.]

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
- Meeting record: <permitted link or reference>
- Related material: <permitted link or reference>
```

Use absolute dates when timing matters, rather than phrases such as “recently” or “next week.” Follow known writing preferences when the user has supplied them. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable.

If the task is to send a message, write a ready-to-send draft rather than merely saying “email them.” For introductions, use double opt-in: seek permission from each relevant person before connecting them, and do not share contact details beyond what they approved.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by permitted meeting reference, counterparty, distinctive topic terms, and proposed title.

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. Skip the new task, or update the existing task if the meeting adds a meaningful action, deadline, or context. Do not expose unrelated task contents during the check. Record the duplicate decision for the final report.

## 7. Create confident tasks

Create high-confidence tasks in a batch when possible. If the environment supports opening created records, open them in the selected task system rather than filling the status update with record links.

For every skipped meeting, give a brief reason, such as “No out-of-meeting commitment,” “Completed during the meeting,” “Owned by another role,” or “Already covered by an active task.”

## 8. Batch uncertain questions

Skip this step entirely when all decisions are confident. Do not interrupt for each ambiguity. Create confident tasks first, then ask all remaining questions together.

```markdown
**[Meeting title]**
Question: [One specific question]
Context: [One sentence grounded in the authorized record]
Option A: [Task to create or update if true]
Option B: [Skip or alternate task shape]
```

Ask the smallest question that resolves ownership, scope, timing, completion status, delegation, or duplicate handling. Wait for answers before creating uncertain tasks. After answers arrive, create or update remaining tasks and rerun the relevant duplicate check if the answer changed the outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, record lessons that genuinely improve future runs. Keep these separate from meeting tasks.

- Add a short, generalized note to a reusable meeting-pattern reference when a recurring pattern affects triage, such as a common attribution error, a reliable sign of live completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new delegation boundary in an authorized responsibility reference when it applies beyond one meeting.

Do not turn one-off facts into permanent rules. Small additions to a pattern reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing a step or changing the evidence order. Briefly report reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Source references respect the task audience’s access boundary.
- Message drafts are ready to send and follow the user’s preferences.
- Task notes contain only information necessary to complete the work.
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
description: Create or improve a short, paid, asynchronous work sample that produces job-relevant evidence, is practical to score, and is validated through simulated submissions.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A strong work sample asks candidates to perform a realistic, bounded version of role-relevant work, produces useful evidence of their judgment and execution, and can be reviewed consistently without excessive reviewer time.

Use it for new exercises and revisions. Do not use it for interview questions, application-form screening questions, live interviews, or multi-day work trials. If the requested format is unclear, ask which assessment format is intended before starting.

## Purpose and design principles

A work sample commonly sits after initial application review and before later interviews. Its purpose is narrow: assess a small set of role-critical capabilities that are observable in a short asynchronous exercise.

It should not attempt to assess the whole person or every requirement of the role. Other stages may be better suited to assess different evidence:

- Interviews can assess live communication, motivation, collaboration, and interactive reasoning.
- References can assess reliability, integrity, and sustained performance over time.
- A longer, paid trial can assess consistency, judgment in real systems, and work across multiple days.
- Onboarding can often address organization-specific tools, processes, and vocabulary.

Use these default constraints unless the hiring owner chooses otherwise:

- Make the exercise paid.
- Set a clear expected time limit, typically two to four hours.
- Use a realistic but fictionalized, anonymized, or approved public scenario.
- Do not ask candidates to produce work that will be used commercially or operationally unless that use is separately disclosed and agreed.
- Keep reviewer time to approximately 20 to 25 minutes per submission.
- Make the task self-contained. Candidates should not need access to internal systems, private records, credentials, or unavailable data.
- State the policy on AI tools clearly. Assess judgment and usefulness, rather than trying to infer AI use from prose style.
- Assess only capabilities materially related to the role. Do not use protected traits, personal history, or unrelated proxies as criteria.
- Provide a route for reasonable accommodations or an accessible equivalent format while preserving the role-relevant standard.

If the exercise needs information from internal role documents, past hiring materials, or communications about people, confirm there is a legitimate hiring purpose and authorization to use those materials. Read only the minimum relevant sources, exclude unrelated personal details, and keep outputs within the approved hiring access boundary.

## Step 1: Pre-flight

Before designing anything, confirm that the hiring team has both:

1. A current job description or role brief explaining responsibilities, level, expected outcomes, and reporting context.
2. A role-success profile, hiring plan, or equivalent document defining the capabilities and experience associated with success in the role.

If either is missing, stop. Do not try to define the successful candidate profile while drafting the work sample. That creates a moving target and often leads to an exercise that appears plausible but measures the wrong things.

Use this request format:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

When both inputs exist, review the full relevant role context. This may include linked project notes, current team constraints, examples of effective work, prior hiring feedback, and prior exercises for comparable roles. Review one or two reference exercises only to calibrate tone, length, and operating format. Do not copy a familiar task shape automatically. Different roles require different evidence.

Give a concise status update after review, for example:

> Read the role brief, success profile, and two reference exercises. Moving to the alignment memo.

## Step 2: Write the alignment memo before drafting

Do not write candidate-facing instructions yet. First create a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five capabilities that the role succeeds or fails on and that can be surfaced within the exercise window. Phrase these as observable performance, rather than vague virtues.

Weak:

> Strategic thinking.

Better:

> Can identify the highest-leverage problem in a messy operating situation, explain the tradeoff, and deliver a useful first action.

### What the exercise will not test

Name important criteria that belong in other stages. This keeps the assessment honest and prevents a short written task from becoming an unrealistic proxy for the entire job.

For example, a three-hour asynchronous exercise may not fairly assess long-term reliability, leadership over months, responsiveness in live meetings, specialized software fluency, or collaborative behavior with an existing team.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level. Explain the implications for task design.

- Entry-level candidates may need more context, clearer boundaries, and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make tradeoffs, establish direction, and create an artifact another person could use without further explanation.

### Failure modes the test should catch

Identify two or three plausible work patterns that could otherwise look strong in a conventional process but would create problems in this role. Describe observable behavior, not personal labels.

Examples include:

- A polished planner who does not produce usable work.
- A fast executor who misses the central problem or creates avoidable risk.
- A conscientious candidate who defers every meaningful decision.
- A technically capable candidate who cannot communicate for the intended audience.

### What strong looks like

Write one short paragraph describing the evidence in a top submission. Focus on choices, what the candidate notices, what they produce, how they use their time, and how they handle uncertainty.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the owner explicitly confirms or revises the memo.

## Step 3: Propose exercise shapes

Once the memo is approved, propose three exercise shapes. Each option must test the confirmed capabilities in a distinct way, be understandable in about a minute, be self-contained, and be scorable quickly.

For each option, provide:

- **Shape:** A plain-language description of the task.
- **What it tests:** The load-bearing capabilities it reveals.
- **Why it is evaluable:** The evidence reviewers will see and why it can be scored consistently.
- **Main risk:** The most likely source of noise, unfairness, or weak diagnostic value.

Keep each option concise. Useful shapes include:

- **Triage pile:** Give the candidate realistic messages, requests, and constraints. They prioritize work, draft responses or outputs, and recommend one systemic improvement. This can suit operations, coordination, support, and communications-heavy roles.
- **Choose the highest-leverage action and ship it:** Give the candidate a brief with several possible priorities. They select one, explain the choice, and create a small usable output. This can suit strategic operations and builder roles.
- **Diagnose and fix:** Give the candidate a messy situation to analyze. They identify the central problem and produce one targeted intervention. This can suit analytical, program, product, and process-improvement roles.
- **Source and pitch:** Ask the candidate to define a target profile using supplied context, identify promising channels or prospects, and draft outreach. This can suit recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** Ask the candidate to assess an intervention area using supplied evidence and make a recommendation for a decision-maker. This can suit research, policy, strategy, and specialist roles.
- **Design a repeatable system:** Ask the candidate to create a lightweight process, playbook, or operating artifact that a teammate could use. This can suit program, enablement, community, and operational-design roles.

Do not draft the full exercise until the hiring owner chooses a shape. If none is suitable, generate three more based on the approved memo rather than forcing a familiar format.

## Step 4: Draft version 1

Write the candidate-facing exercise in this order.

## [Role] Work Sample

State, in one or two sentences, the role-relevant capabilities the exercise assesses. State the total expected time.

**Your mission**

Describe a specific situation, rather than an abstract assignment. Provide enough context to make the work realistic. If decisiveness is a target capability, state which stakeholders are unavailable during the exercise so candidates must make reasonable choices rather than defer all key decisions.

End with one sentence restating what the candidate will produce.

**Deliverables**

List two to four parts, with rough time guidance where useful. A common operations pattern is:

- A short prioritization or analysis section.
- Several actual drafts, decisions, or shipped outputs.
- One systemic fix, process improvement, or reusable artifact.

Avoid excessive micro-tasks. A few substantive outputs create clearer evidence than dozens of shallow decisions. If both planning and execution matter, explicitly tell candidates not to let planning consume the time needed to produce work.

**Context**

Provide only the information necessary to complete the task: project state, audience, constraints, available resources, relevant policies, and stakeholder availability. Use fictional names, clearly fictional email domains such as `example.com`, and generalized details unless the hiring owner has approved use of real public information.

For a triage-pile exercise, include approximately eight to ten realistic items. Make some items connected, so that seeing patterns across the full situation is rewarded. Add reference notes containing information required for fair decisions, such as escalation rules, capacity limits, or refund policy.

**Instructions**

Include the following:

- Expected time limit.
- Submission deadline.
- Submission format, such as one document or PDF, plus links to supplementary artifacts if needed.
- Payment amount, payment process, and any early-submission bonus if offered.
- Permitted tools and AI assistance.
- A request to document significant assumptions briefly.
- Permission to submit incomplete work if time runs out.
- Optional guidance on a short walkthrough video, if this would provide useful evidence.
- A contact route for accommodation requests or access issues.

Use a transparent AI policy. For example:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

**Anticipated questions**

Answer common questions, including:

- If a requirement is unclear, make a reasonable assumption and state it briefly.
- If you do not finish in the expected time, submit what you have and explain what you would do next.
- The work will be used only to evaluate candidates for this role unless another use is agreed separately.

After every draft, add this separate section:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets on design choices the owner might change. Surface risks such as an overly obvious scenario item, unrealistic facts, payment structure, excessive prescription, or an optional video that does not add meaningful signal.

End with one focused decision question, such as:

> Which part should we tighten first?

## Candidate-facing format and writing checks

Write in direct, plain US English unless another locale is appropriate. Format the draft for the organization’s chosen hiring system or document tool.

Before sharing each candidate-facing draft, check that it:

- Uses headings and bullets that the destination system renders reliably.
- Avoids tables and horizontal dividers if the destination system handles them poorly.
- Avoids generic AI-sounding slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.
- Uses clear phrasing such as “by the end of Tuesday,” rather than abbreviated wording.
- Uses no confidential details, credentials, private contact information, or sensitive internal data.
- Uses a supported soft-break method for multi-line message headers when the destination editor collapses ordinary line breaks.
- Does not create an accessibility barrier through unexplained formatting, time-zone ambiguity, or inaccessible file requirements.

## Step 5: Iterate with the hiring owner

Expect multiple rounds of feedback. For each revision, provide the complete updated work sample, not only a list of changes, so it can be copied directly into the selected system.

Apply feedback directly unless it would materially undermine validity, fairness, candidate safety, or the approved purpose of the assessment. If so, state the concern once in plain language, offer an alternative, and let the hiring owner decide.

Common revisions include tightening vague tasks, loosening excessive prescription, correcting scenario facts, simplifying deliverables, changing payment, and replacing unrealistic details.

## Step 6: Simulate submissions

Before declaring version 1 complete, simulate two full submissions in parallel using the exact candidate-facing instructions.

### Role-aligned simulation

Use a persona that matches the approved role-success profile. Have them complete the actual deliverables under the stated time constraint. Ask for a short reflection on choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest, capable candidate who might pass ordinary screening but whose demonstrated work lacks one role-critical capability. Choose a relevant mismatch, such as a planner where the role needs a builder, a cautious candidate where the role needs timely decisions, or an executor who does not recognize systemic patterns. Keep the difference tied to role evidence, never identity, demographic characteristics, or background.

Have this persona complete the same submission.

Then synthesize the results:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both candidates performed similarly.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by likely impact.

Floor checks that both candidates pass are not automatically bad. The concern is when a central capability fails to produce meaningfully different evidence.

## Step 7: Apply validation improvements

Revise the complete exercise using the simulation findings. Address the weakest diagnostic points first. Useful changes may include:

- Making scenario items more interdependent.
- Removing obvious noise that takes seconds to dismiss.
- Adding a concrete constraint that forces a meaningful tradeoff.
- Replacing a broad opinion prompt with a usable deliverable.
- Clarifying reviewer guidance so scoring rewards intended evidence.
- Removing specialized knowledge requirements that are trainable and not essential at the start of the role.

Do not make the task harder merely to make it more selective. Make it more diagnostic of the confirmed role-relevant capabilities.

## Step 8: Optional external review

If other reviewers provide feedback, evaluate each suggestion against the approved alignment memo. State which recommendations to integrate, which to skip, and why. External feedback is evidence, not an automatic instruction. The hiring owner remains accountable for the assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The role description and role-success profile are confirmed.
- The alignment memo is approved.
- The chosen shape maps directly to the load-bearing capabilities.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and requires no private access.
- Payment, deadline, AI policy, accommodation route, and submission instructions are clear.
- A reviewer can score a submission in about 20 to 25 minutes.
- Candidate-facing content is formatted for the intended system.
- Role-aligned and plausible role-misaligned simulations have been completed.
- Simulation findings led to necessary revisions.
- The final version contains no sensitive information and does not request unpaid production work.
- The assessment is limited to role-relevant criteria and has been checked for avoidable proxy bias.

## Common failure modes

Avoid these patterns:

- Designing the task before agreeing what it should measure.
- Testing tool familiarity, domain trivia, or readily trainable knowledge instead of durable judgment.
- Asking for too many small outputs instead of a few meaningful ones.
- Making every scenario item independent, which tests volume but not pattern recognition.
- Letting candidates defer every decision to an available stakeholder when decisiveness is meant to matter.
- Giving vague context that rewards insider knowledge.
- Setting word-count guidance that encourages padding.
- Creating a test that takes longer to grade than the evidence justifies.
- Treating polished presentation as the main signal when the role requires different capabilities.
- Declaring success without checking whether the exercise distinguishes the performance evidence it was designed to assess.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, respectful of candidate time, useful for assessment, and clear about what strong performance looks like.


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
description: Complete browser-based tasks safely by selecting the least invasive method, protecting account context and privacy, verifying rendered state, and separating preparation from consequential final actions.
---

# Use a browser safely

Use this workflow for tasks that require interaction with a rendered website: completing forms, changing dashboard settings, collecting information from client-rendered pages, testing user flows, or working in an authenticated account. Use it only when a normal page request, supported service interface, or authorized API cannot complete the task reliably.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until the account, target, page state, and authorization are clear.

A browser automation command reporting success does **not** prove that the website accepted the change. Modern applications may retain data in an internal state model, save only after focus moves away, replace controls during a re-render, or show a misleading error after an action has already succeeded.

## 1. Choose the least invasive route

Use the first suitable route in this order:

1. **Supported direct interface or API.** Prefer a documented and authorized programmatic interface when it can safely perform the requested action.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, and forms that do not require the user's existing signed-in identity.
3. **User-visible authenticated browser session.** Use this only when an established session, single sign-on state, account-specific dashboard, or user-directed browser context is genuinely necessary.

Before automating a page, look for a direct route. Review official service documentation, ordinary form actions, page source, and visible network requests for supported endpoints. A web form may submit structured data to an authorized service that is safer and more reliable to use directly.

Do not use undocumented interfaces to bypass access controls, consent boundaries, service restrictions, or security measures. Do not use an authenticated visible browser merely because it is convenient: it can interrupt the user's work and increases privacy and account risk.

If a website blocks automated browsing, do not attempt to evade its protections for ordinary research or collection. A visible authenticated session may be appropriate only when the user explicitly requested a legitimate task on that specific site, has authorized access, and the existing session is necessary. Do not weaken browser security, access controls, warnings, or anti-abuse safeguards.

## 2. Protect account identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not place unrelated personal details in notes, screenshots, logs, or reports. Keep results within the requester's appropriate access boundary and respect privacy expectations and consent.

Before acting in an authenticated context, identify the correct account, organization, environment, and browser profile. Never infer identity from a generic browser-window name, remembered default, stale tab title, or arbitrary connection label.

Use these rules:

- Announce before taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing tab to use.
- Explicitly classify the intended context, such as personal, work, test, staging, or production.
- Select a browser profile or connection that corresponds to that context. Do not rely on a generic browser selector that may choose the most recently active profile.
- Confirm the signed-in account with a reliable account indicator before opening or modifying the actual target.
- If the account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not expose passwords, session tokens, recovery details, private account data, or security settings in output or logs.
- Do not disable multi-factor authentication, browser warnings, security controls, or access restrictions to make automation easier.

Use an account preflight gate before actions that change data. Confirm the account identity, environment, and target object. If the automation system has a verification marker or permission gate, mark the context as verified **only after** the account check has passed. Never create a verification marker in advance merely to unlock action tools.

Ask this pre-action question when needed:

> Which account is active? Which environment is active? What exact item will change?

If any answer remains uncertain, resolve it before proceeding.

## 3. Establish the task boundary

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, or workflow.
- The information that will be entered, collected, changed, or uploaded.
- The minimum information needed to complete the request.
- Whether the final action is reversible.
- Whether the work includes sending, publishing, paying, deleting, granting access, changing a plan, or another external commitment.
- Missing information, ambiguous choices, and fields requiring the user's judgment.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and preparing a preview may be reversible. Submitting, sending, publishing, purchasing, deleting, or changing important account settings may not be.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify the values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** After explicit confirmation of the prepared state, re-check account, target, and readiness. Then perform the final action once.

If the page reloads, re-renders, or the session changes between the two phases, do not assume the earlier state remains valid. Restore and verify the intended values before committing.

## 4. Inspect the rendered page before editing

Do not start by guessing selectors, filling fields by numeric position, or trusting visual appearance alone. Inspect the rendered page first and collect enough structure to identify controls safely.

For every relevant field, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, file upload, or custom widget.
- Accessible name, visible label, placeholder, or label relationship.
- Current value and whether it is required.
- Validation rules, character limits, formatting behavior, and disabled state.
- Whether an apparent field is the real editable control, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, date, tab, or other control causes a re-render.

Address controls by a stable semantic identity, such as visible label text, accessible name, or explicit label relationship. Do not use DOM indexes when labels are available: dynamic applications may change field order between page loads or after re-rendering.

Before changing an existing record or setting, inspect its current state. This reduces the risk of modifying the wrong item or overwriting information unexpectedly.

### Generic inspection pattern

Use the chosen browser automation capability to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

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

## 5. Use the correct interaction for each control

A generic “set value” operation is not reliable for every web control.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use normal text input behavior. | Line breaks may be silently removed. |
| Multiline text area | Fill text, then move focus away. | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus it, select existing content, enter text through keyboard-style events, then blur. | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, choose by visible option text, then wait for the state to settle. | Selection can trigger a full re-render. |
| Checkbox or radio control | Read its current state first and change only if necessary. | A click can toggle an already-correct value. |
| Date/time picker | Set the date and time, then verify the rendered summary. | A popover can reinterpret typing or clear related values. |
| File upload | Confirm file, destination, and privacy implications first. | Uploading may start immediately and can be difficult to undo. |

For framework-driven editors, simulate ordinary user interaction rather than writing directly to low-level page properties. A robust general sequence is:

1. Focus the actual editable element.
2. Select existing content.
3. Delete it.
4. Enter the new content with keyboard-style events.
5. Move focus to a neutral element on the page.
6. Wait briefly and read the result back.

Some forms pair a visible editor with a hidden input. Editing the hidden input may appear successful in a DOM dump while server-side validation treats the visible editor as empty. Target the interactive control that the application reads. If a generic accessibility locator identifies an empty wrapper, inspect the underlying editable element and follow its label relationship.

If changing a dropdown, checkbox, tab, or date can refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterwards and confirm that earlier entries remain present.

## 6. Verify after every meaningful edit

After each field is filled or setting is changed, read its value back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare lengths, required state, or a minimal redacted summary rather than exposing the complete value unnecessarily.

Check for common mismatches:

- The automation layer reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displayed text but did not retain it internally.
- A later interaction erased an earlier entry after a re-render.
- A hidden synchronization field was changed instead of the visible editor.
- A selection changed a dependent field, date, recipient, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once using a more suitable interaction method, and verify again. If the page continues to reject or alter the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

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

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only within the appropriate access boundary. Avoid pasting a large table of sensitive values into chat when a short summary and securely available record are sufficient.

### Readiness checklist

- [ ] The account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 8. Treat one-way actions as a distinct phase

The following generally require explicit confirmation immediately before the final control is activated:

- Sending messages, invitations, or notifications.
- Publishing content.
- Submitting official or externally reviewed forms.
- Making a payment or purchase.
- Deleting records or files.
- Changing subscription, billing, access, ownership, or security settings.
- Actions labeled permanent, final, irreversible, or impossible to edit later.

Use this confirmation format:

> Ready to [final action] for [target]. Key details: [concise summary]. Audience, recipient, or destination: [value]. Cost or irreversible effect: [value or none known]. Open questions: [list or none]. Proceed?

Wait for confirmation before activating the final control. For low-risk reversible changes that the user explicitly requested, such as adjusting a preference or updating a draft, proceed after normal verification unless the page presents an unexpected warning or broader impact.

## 9. Confirm completion after acting

A button click is not proof of success. After the final action, look for reliable evidence such as a success message, confirmation reference, newly created record, persisted setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Do not represent an attempted action as completed.

## 10. General failure patterns and recovery rules

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank | The application ignored a direct value change. | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after editing a later field | A component re-render reset uncommitted state. | Commit and verify each field; complete re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used. | Find a multiline or editor control, or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node. | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited. | Use the visible interactive control that the application reads. |
| Automation is unstable on a complex page | The chosen automation layer is unsuitable. | Switch to a more robust automation method or supported direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers behave differently | The site varies by browser context. | Prefer an authorized direct interface; for an explicit legitimate task, use a verified visible session without evading protections. |
| A popup changes dates or other values unexpectedly | The widget has stateful close, clear, or parsing behavior. | Close it through a neutral page action and re-verify affected values. |
| A visible error may be cosmetic | The action may already have completed. | Inspect resulting state before retrying. |
| Account context is uncertain | The wrong profile or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using real screenshots and programmatic layout checks. Fix failures and rerun the relevant sweep before reporting the change as complete.
---

# Test every screen size

Run this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it to small changes too: a spacing, background, or sizing adjustment can alter wrapping, overflow, alignment, page height, and exposed backgrounds at other screen sizes.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Use real screenshots and numerical checks together.

## 1. Prepare realistic page states

Run the interface in an authorized test environment. Populate the changed surface with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative lists, cards, rows, and validation messages;
- realistic item counts or content near expected limits;
- loading, empty, and error states when the change can affect them.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping, and unintended blank space.

## 2. Choose the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages or interfaces expected on large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Also include any known target viewport selected by the user or project. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable browser-testing system. Headless browser automation is a useful default when it can capture browser-accurate screenshots and execute page-level checks.

## 3. Capture and inspect screenshots

Capture real screenshots at each relevant viewport and content state. Use full-page screenshots when page length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

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

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant bounding rectangles with adjacent elements and container boundaries rather than assuming every vertically adjacent element must never intersect; intentional overlays should be documented as exceptions.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line; reading-focused designs commonly use a narrower target of roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visual defects such as exposed background strips, poor balance, or unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and relevant programmatic checks pass.

| Evidence type | What it is best at detecting |
|---|---|
| Screenshot inspection | Visual gaps, exposed backgrounds, alignment, wrapping, and unintended empty regions |
| Programmatic checks | Overflow, off-screen controls, rectangle collisions, and measured text width |

## 6. Fix failures and rerun the sweep

If any viewport or realistic state fails:

1. Stop the completion or release process.
2. Identify the layout rule causing the failure.
3. Fix the underlying behavior rather than adding a viewport-specific cosmetic patch.
4. Rerun the complete relevant sweep, not only the failing size.

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

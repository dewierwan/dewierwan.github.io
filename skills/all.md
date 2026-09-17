# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate distinct options for a decision or problem, assess their tradeoffs honestly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs credible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long idea list: surface genuinely different paths, make tradeoffs clear, and preserve a small set of meaningful choices.

## 1. Gather relevant context

Start with the information supplied in the request. If the user refers to documents, discussion records, prior decisions, research, or other materials available in the current environment, review the minimum relevant material first.

When the question is not self-contained, retrieve a small number of high-value sources that could materially change the decision, such as:

- Earlier decisions and their rationale
- Constraints, commitments, deadlines, and dependencies
- Relevant stakeholder concerns and ownership boundaries
- Evidence about what has already been attempted

Use targeted retrieval rather than broad searching. Access private communications or records only for a legitimate purpose, with clear authorization, and only within the user’s appropriate access boundary. Include only information relevant to the decision; omit unrelated sensitive or personal details.

If important context is unavailable, state the assumption or ask a focused question. Do not invent facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that identifies:

- What decision the user is actually making
- Important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging options

The stated request may describe a symptom or favored solution rather than the underlying decision. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the framing is obvious and low-stakes, or when the user explicitly requests an immediate first pass. A wrong framing produces irrelevant options.

## 3. Generate distinct options

Generate five to seven options unless fewer genuinely different paths exist. Each option must represent a fundamentally different approach, not merely a different level of effort. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes process, incentives, scope, timing, or the problem framing
- At least one surprising but credible path, such as delaying, partnering, reducing scope, or deliberately doing nothing

Do not be contrarian merely to appear creative. A no-action option is useful only if observation, timing, avoided distraction, or preserving resources has real value.

Give each option a short, memorable label. For every option, provide:

| Element | What to include |
|---|---|
| **What** | One or two sentences explaining the approach. |
| **Strengths** | One or two concrete advantages. |
| **Weaknesses** | One or two concrete disadvantages, risks, or limitations. |
| **Effort** | Low, Medium, or High. |

Use specific tradeoffs. Do not soften serious drawbacks or make a preferred option look better by evaluating alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, operational burden, and stakeholder impact. Add domain-specific criteria when they matter more than these defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are informative, but state clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not why it is generally attractive.
4. Name the key assumption most likely to change the ranking, when one exists.

Do not force a single winner unless the user explicitly requests one. The purpose is to support a decision, not to make it on the user’s behalf.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may select an option, request more detail, correct the framing, ask for different options, or propose a hybrid.

If the user proposes a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

After the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. This applies to major strategic bets, public commitments, long-term obligations, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that defines the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than only the first proposed solution.
- The options are genuinely distinct.
- The conventional and surprising paths are both considered where relevant.
- Weaknesses and effort estimates are candid and plausible.
- Recommendations follow the user’s stated criteria rather than unstated assistant preferences.
- Any retrieved information was authorized, necessary, and kept within the appropriate privacy boundary.


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

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes a defense exercise.
- If the idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.
- If using internal records, feedback, or communications, have a legitimate purpose and authorization. Use only the minimum relevant material, keep personal details out of the output, and do not infer views that were not expressed.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask **one forcing question at a time**. Wait for the answer, assess it, and challenge vague, unsupported, or evasive answers before continuing.
- Use available evidence, such as metrics, research, prior experiments, customer feedback, documented decisions, or relevant stakeholder input. Separate facts, inferences, and forecasts.
- Identify possible dissenters by role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- If a step is irrelevant, state “Skipping: [reason]” and move on.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker’s actual intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so. If a stronger restatement changes the intended claim, confirm it before testing.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by the damage caused if they are wrong, beginning with the most consequential.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Test or disproof method] |

Make assumptions observable where possible. Replace “users will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Start with the highest-risk assumption and adapt later questions to the answers received. Do not present the full question set as a questionnaire.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would happen in the next 30 or 90 days that would show this is wrong?
- **Counterfactual:** What similar attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what will be true in 12 months, and what might success itself break or constrain?
- **Stakeholder dissent:** Which relevant role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence; ask for an observed behavior, dataset, comparison, experiment, or credible commitment that supports the belief.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, usually 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failure, changing external conditions, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable signal] | [Check or accountable role] |

Warning signs must appear early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree and state the strongest likely objection from each. If the decision-maker has not sought that perspective, mark it as an evidence gap. Silence is not agreement.

Dissent is not an automatic veto. It exposes constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test incomplete or failed rather than approving the idea.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next step:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining choices, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data collection period. Next: run that test, then make the decision with the result recorded.
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

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and issuing a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make a clear choice with the right amount of effort. The goal is not maximum analysis. It is to decide quickly when a choice is small, add challenge and consultation when it is consequential, preserve reasoning when useful, and learn from outcomes.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, is leaning toward, or decided something they did not actually say.
3. **Separate advice from attribution.** Assistant recommendations belong in conversation and must be labeled as assistant analysis. Add them to a decision record only when the user explicitly asks.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution. Plan or do the task instead of creating decision overhead.
5. **Record only with permission.** “Should we do X?” asks for analysis, not for a record. Create or update a decision record only when the user asks to log, track, open, resume, or commit it, or explicitly agrees to recording.
6. **Protect privacy and access boundaries.** Before using shared communications, personnel information, customer records, or a shared register, confirm a legitimate purpose and clear authorization. Use the minimum relevant sources and omit unrelated sensitive details.
7. **Do not deliberate forever.** Once the required rigor and readiness gates are met, name the decision and move forward.

If a record is visible to other people, confirm that the audience is appropriate before writing. For health, relationships, compensation, confidential personnel matters, or other sensitive subjects, offer a private record in the user’s chosen private workspace or keep the discussion in chat.

## 1. Detect the decision mode

If the user explicitly says they want to start, resume, commit, or review a decision, follow that instruction. Otherwise, if authorized to access the chosen decision register, search it for overlapping records before creating a duplicate.

| Mode | When to use it | Action |
|---|---|---|
| New | No matching record exists, or the user wants a fresh decision | Frame and classify the decision |
| Resume | A matching record is open | Append new inputs and continue analysis |
| Commit | An open decision exists and the user is ready to choose | Confirm readiness, record the call, and schedule review |
| Review | A resolved decision has reached its review point and has no final outcome assessment | Compare actual outcomes with the original prediction |

For a resume, append information rather than rewriting history. For a review, use the original prediction, confidence, and reasoning as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Write the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing where relevant?
- What is the deadline or decision trigger?
- What result is desired?
- What happens if no action is taken?

Ask one clarifying question at a time when the issue is unclear. If the question is broad and credible options do not yet exist, generate options before evaluating them. Do not pressure-test a vague problem statement.

If there is only one viable path, say so directly: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Use the cost to unwind the choice as the primary test. Consider money, time, trust, operational disruption, opportunity cost, and reputational effects. If the unwind cost cannot be named quickly or is highly uncertain, the decision is probably larger than it first appears.

| Bucket | Meaning | Typical treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not record by default |
| Reversible | Moderate stakes and reversible within days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge gate, stakeholder check, full record |
| Direction-setting | Shapes strategy, finances, culture, or operating model for an extended period | Full analysis plus explicit dissent and named prerequisite conversations |

Use broadly useful defaults for records:

| Bucket | Stakes | Reversibility | Default review point |
|---|---|---|---|
| Trivial | Low | Easy | No formal review |
| Reversible | Low or medium | Reversible | One month |
| Hard to reverse | High | Hard | Three months |
| Direction-setting | Very high | Difficult or effectively one-way | Six months |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, provide a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: continued attention may cost more than an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. For each option, state one major strength, one major weakness, and a rough effort or cost estimate.
3. Recommend an option and name the decisive reason.
4. If uncertainty remains material, choose the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test examines assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and major stakeholder objections.

If no relevant pressure test has occurred in the current work context, stop the commitment flow and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not continue merely because the user is in a hurry. Continue only after the pressure test is complete or the user explicitly overrides it with a reason.

If the pressure test identifies a serious unresolved failure, do not force a choice. Return to option generation, redesign the leading option, gather a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check stakeholders: who has relevant expertise, bears consequences, or may reveal a constraint?
4. Give a recommendation, labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has happened, unless the user explicitly accepts and records a reason for proceeding without it. If it is being rushed, state which consultation, evidence, or dissent is being skipped and why that matters.

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

- **User’s stated view:** Positions the user actually expressed.
- **Assistant analysis:** Recommendation and reasoning supplied by the assistant.
- **Open question:** Material uncertainty not yet resolved.

If the user has not expressed a position, record “No position stated yet” or leave the user-position field blank. Never invent a lean, confidence level, rationale, response to dissent, or final choice for them.

## 6. Commit and record

Before finalizing a meaningful decision, confirm:

- What is the decision?
- Which option was chosen?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable result is predicted?
- What is the user’s confidence in that prediction?

Make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Use the user’s chosen document system, decision register, or private file. New records should use an approved template when one exists. For an open decision, record context, current options, and new inputs; leave commitment sections blank. When resuming, append a dated thinking-log entry rather than overwriting prior entries.

Suggested record fields:

| Field | Example value or purpose |
|---|---|
| Status | Open, resolved yes, or resolved no |
| Type | Strategy, product, finance, operations, people, or personal |
| Stakes | Low, medium, high, or direction-setting |
| Reversibility | Reversible, hard, or one-way |
| Decision date | Date the user actually made the call |
| Review date | Date or trigger for retrospective |
| Confidence | User’s prediction confidence at decision time |
| Outcome | Too early, correct, incorrect, mixed, or not applicable |

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** [Optional third option.]

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

For hard-to-reverse and direction-setting commitments, create a reminder in the user’s chosen calendar or task system when authorized. Include the review date, decision question, record location, and a reminder shortly before the review. A record-level review date is usually sufficient for reversible choices.

## 7. Review the outcome

At the review point, complete the retrospective:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle that can improve future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not collapse a bad outcome into a bad decision process, or a good outcome into a sound process. A well-reasoned choice can meet bad luck; a weak process can occasionally produce a good result.

## Completion message

When a decision is made, summarize it clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [date]
Review: [date or trigger, and what would prompt earlier review]
Record: [location, if one exists]
```

Use direct language. Challenge weak reasoning with evidence, but do not use rigor as an excuse for endless deliberation. Keep assistant advice separate from the user’s stated judgment, respect authorized access boundaries, and move from analysis to action once the appropriate gates are met.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem whose solution is not already obvious. Do not use it for a small fix, a routine task with a known implementation, or work that should first be resolved as a strategic decision.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to build a particular thing, work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, and what workarounds exist?
- How frequent, costly, urgent, or blocking is it?
- What outcome would materially improve the situation?
- What constraints, compatibility needs, deadlines, or access boundaries apply?

Write a concise problem statement and descriptive requirements. Describe outcomes and constraints rather than assuming an implementation. If the proposed solution appears mismatched to the problem, say so directly.

Ask only for information that cannot be found in authorized project context, documentation, code, or records. When reviewing communications or records about people, use them only for a legitimate authorized purpose, inspect the minimum relevant sources, and omit unrelated or sensitive personal details from outputs.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Include **do nothing**, **deprioritize**, or **improve the current workaround** as genuine options when appropriate.

Distinguish between:

- **Reversible decisions:** Small, easy-to-change choices. Make a reasonable choice and proceed.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, long-lived settings, migrations, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation and record the rationale when useful.

If priority or direction is unclear, present the tradeoff and ask the accountable decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Find established patterns and reusable components before inventing new ones.

Identify compatibility requirements, deployment practices, supported environments, ownership boundaries, security expectations, and monitoring needs. Use existing conventions unless there is a clear reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve current authentication, permissions, and data behavior.
- Must fit available delivery time and maintenance capacity.
- Should avoid new dependencies and long-lived configuration.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide generation and selection. Without them, the first plausible idea may win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For ambiguous problems, generate a wider candidate set before narrowing. For each option, state what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that vary by runtime condition.
- Validate strictly and fail fast for invalid states. Do not hide programmer errors by returning plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Avoid quick fixes that bypass the appropriate design boundary.

## 6. Evaluate and recommend

Compare viable options against the evaluation criteria. Present a concise proposal containing:

- Problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Keep the proposal direct. Store it in the user's approved shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear date-prefixed title, such as `17 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership. Put the plan where appropriate reviewers can edit and approve it.

Implement the approved solution using project conventions and authorized access. Run relevant automated tests, static checks, and focused manual verification. Confirm results against the evaluation criteria, including compatibility and failure behavior.

Do not claim success based only on implementation. State what was tested, the observed results, and what remains unverified. Commit, publish, or deploy only according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Do not include personal, confidential, or access-restricted information beyond the audience's authorized boundary.


---
name: shape-and-draft
description: Shape consequential documents by gathering evidence, resolving material choices with authorized decision-makers, checking readiness, and then drafting and auditing the smallest document that can achieve the goal.
---

# Shape and draft a document

Develop an important document by shaping the thinking behind it before writing. Work out what the document must achieve, gather the minimum relevant evidence, resolve choices that could change its substance, and draft only when the remaining uncertainty is low impact or is clearly represented in the document.

Use this workflow for strategies, narratives, operating agreements, proposals, briefs, scorecards, and decision memos when the artifact, argument, boundaries, commitments, or operating model are unsettled. Do not use it for a quick edit, formatting-only work, or a document whose material decisions are already specified.

## Classify the request

A request may name a document type, desired outcome, audience, source material, or some combination. Treat the proposed document type as a hypothesis until its purpose is clear.

Use a **full shaping process** when the document is consequential and material choices remain unsettled, or when the requester asks for deep thinking, several question rounds, or close alignment before drafting. A substantive interview round resolves a distinct layer of uncertainty and uses the answers to determine the next questions. Restating the discussion or seeking broad approval does not count as a substantive round.

## 1. Work backwards from the outcome

Start with the change the document needs to produce. Establish:

- Who will read it.
- What readers should understand, decide, approve, or do afterward.
- What is unclear, contested, blocked, or currently going wrong.
- Whether the document mainly needs to explain, persuade, decide, coordinate, or govern.

Do not accept “write a narrative” or “make a strategy page” as a sufficient goal. Identify the job the document must perform.

## 2. Choose the artifact

Recommend the form that best serves that job:

- **Narrative:** Builds shared understanding of why something matters and what bet is being made.
- **Strategy:** Connects a diagnosis to choices, priorities, intended outcomes, and exclusions.
- **Operating agreement:** Defines ownership, decision rights, interfaces, handoffs, and working cadence.
- **Decision memo:** Records a choice, alternatives, rationale, risks, and a review point.
- **Scorecard:** Defines a role or team mission, outcomes, and role-relevant capabilities.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the meaningful tradeoff and recommend an artifact. If the choice of form would materially affect the argument, structure, or decisions required, ask the authorized decision-maker to confirm it before proceeding.

## 3. Gather and classify evidence

Read supplied material first. Follow any stated rules for source selection, authority, citations, and links. Scale research to the stakes: use the minimum source set likely to establish prior decisions, current definitions, supporting evidence, dissent, constraints, and ownership context.

If the task requires private communications, personnel records, customer information, or other sensitive records, proceed only for a legitimate purpose and with clear authorization. Use only the minimum relevant sources and information. Omit unrelated or sensitive personal details, respect consent and privacy expectations, and keep both research and output within the appropriate access boundary.

Apply these evidence rules:

- Respect any stated source-of-truth hierarchy.
- Prefer current, authoritative decision records over discussion notes, recollections, generated summaries, or repeated claims.
- Resolve contradictions where the evidence permits, and surface material contradictions that remain.
- Do not ask people for factual information that authorized sources can answer.
- Do not alter source material unless explicitly instructed.
- Include sensitive information only when it is necessary, authorized, and appropriate for the intended audience.

Keep evidence separate from alignment. Sources can establish what happened, what people said, and what an authoritative record states. They do not automatically establish what a current decision-maker believes, is willing to promise, or chooses to exclude. A repeated theme, synthesis, or plausible implication is an **inference**, not a settled decision.

Ask for confirmation whenever an inference would become a central claim, commitment, boundary, recommendation, or operating rule.

Before the first interview round, provide a short situation brief covering:

- What the sources establish.
- What has already been explicitly confirmed.
- What is inferred but unconfirmed.
- The central tension, gap, or missing logic.
- The recommended artifact.
- The important uncertainties that only an authorized decision-maker can resolve.

## 4. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds already completed in the current conversation and do not repeat settled questions. Do not draft immediately after the first round merely because one central issue appears resolved. Use the next round to test consequences, such as boundaries, counterarguments, ownership, definitions, or execution details revealed by the first.

Ask four to eight focused questions per round. If fewer than four material questions remain, ask all of them and say that this is a narrow final check. Do not add ceremonial questions to reach a target number.

Each numbered question should normally seek one decision. Do not bundle independent choices, such as ownership, coordination, handoffs, and success measures, into one broad question. Bundling creates false alignment.

Use one clear answer surface for each round. Do not duplicate the same questions across multiple interfaces. Keep question numbering continuous, and keep each number attached to the same decision so shorthand replies remain unambiguous.

For bounded choices, offer the number of genuinely distinct, mutually exclusive options needed for a useful decision, usually two to four. Label them with lowercase letters and put the recommended option first unless context makes another ordering clearer. Explain the key tradeoff briefly, and always leave room for the respondent to reject the framing or provide another answer.

Keep the question block compact, with each question and option on consecutive lines and no blank lines inside the block. For example:

1. Which direction should the document recommend?
   a. Focus first on the highest-impact problem; this narrows scope but clarifies accountability.
   b. Address all related problems equally; this is broader but less decisive.
   c. Present options without a recommendation; this preserves flexibility but delays a choice.
2. Who should hold the final decision right?
   a. The accountable lead.
   b. A designated cross-functional group.
   c. Shared input, with one named person making the final call.

Each round should:

1. Start with an updated model of the situation and state what changed because of earlier answers.
2. Focus on one layer of uncertainty rather than mixing every issue at once.
3. Separate source-supported observations from choices the decision-maker must make.
4. Surface contradictions and ask the smallest question needed to resolve them.
5. Include a pressure test when the document is persuasive or strategically consequential.
6. Allow qualifications, uncertainty, and challenges to the framing.

A common progression is: purpose; strategy; operating model; definitions and measures; then expression, format, and destination. Adapt the sequence to the task, but preserve the answer-dependent loop: later questions must arise from evidence and earlier answers, not from a generic questionnaire.

After every answer round:

1. Match shorthand and free-text answers to their question numbers, preserving qualifications such as “mostly c” or “not sure.”
2. Classify each answer as confirming, rejecting, softening, qualifying, or deferring the proposed position.
3. Mark only genuinely unanswered or unclear material choices as open.
4. Trace downstream implications. A changed audience, softened commitment, new exception, or rejected framing often creates another material question.
5. Update and show a concise alignment ledger.
6. Generate the next round from remaining material uncertainties and their consequences.

Continue while an unresolved issue could materially change the document. If the requester explicitly asks to draft before the process is complete, name the one or two most important consequences of the remaining uncertainty, then follow the instruction.

## 5. Maintain an alignment ledger

Keep a compact working record throughout the conversation:

| Category | What to record |
|---|---|
| Confirmed | Choices explicitly made by an authorized decision-maker. |
| Source facts | Claims established by current, authoritative evidence but not selected as current choices. |
| Inferred | Plausible interpretations that remain unconfirmed. |
| Open | Questions that could materially change the document. |
| Corrected | Assumptions or claims that a participant has rejected. |

Update the ledger after every answer round. Never reintroduce a corrected assumption. If confirmed statements conflict, surface and resolve the conflict rather than hiding it in vague language. Never promote an inference to confirmed merely because several sources support it.

For a full shaping process, show a concise ledger before each later round so the decision-maker can correct mistaken assumptions. Every major claim in the draft must be a confirmed choice, a supported source fact, or explicitly framed as a proposal, assumption, or open question.

## 6. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document’s substance. Before drafting, provide a concise pre-draft synthesis covering the document’s intended job, audience, central position, important boundaries, and deliberate open questions.

For every major planned claim, ask:

> Was this confirmed by an authorized decision-maker, established as fact by authoritative evidence, or merely inferred?

If a material claim is only inferred, ask another question or label it clearly as a proposal. Do not present it as settled.

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

For persuasive documents, complete a skeptical-reader pass. Identify the strongest likely objection from the actual audience, the premise or safeguard they may dispute, and whether the document’s response is confirmed or supported by evidence.

Close alignment does not require artificial certainty. It means that remaining uncertainty is low impact or clearly represented as unresolved.

## 7. Draft and deliver

Follow the stated voice, style preferences, accessibility needs, privacy constraints, and delivery requirements. Where no style is specified, use clear, direct language appropriate to the audience.

Write the smallest document that accomplishes the agreed purpose. Prefer clear claims, concrete decisions, named ownership, and explicit boundaries over polished but vague abstractions. Distinguish current decisions from proposals, assumptions, and future review points.

Avoid long, flat inventories in action-oriented documents. Keep lists short enough to scan and act on; combine related points under a clear lead phrase or move supporting detail to an appropriate referenced source.

Make the draft as simple as the substance allows:

- Prefer short, common words over formal or inflated language.
- Write complete, natural sentences; do not turn connected ideas into choppy fragments.
- State the point first. Remove warm-up text, repeated context, and qualifications that do not affect a decision or action.
- Turn abstractions into concrete claims, actions, owners, dates, examples, or tests where useful.
- Use focused paragraphs and bullets only for real lists. Write bullets as full sentences unless they are compact labels.
- Preserve difficult ideas when they matter, but explain them plainly rather than hiding them in jargon.

Honor the requested destination using the user’s chosen system. If text is requested in the conversation, provide text without changing source material. If a document must be created or updated elsewhere, do so only as instructed and verify the result.

For formatted documents, inspect the rendered result as well as the underlying text. Check that headings do not inherit list formatting, lists use consistent indentation, and page breaks or isolated bullets do not make the document hard to read.

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
- Has unnecessary sensitive information been omitted?
- Can each sentence be understood on the first read?
- Can any abstract phrase, inflated word, or repeated point be simplified or removed without losing meaning?

Fix mismatches before delivering. Put the deliverable last, without trailing commentary that would interfere with copying or use.

## Failure modes to avoid

- Drafting early because producing text feels productive.
- Treating the proposed artifact as fixed before its purpose is known.
- Asking people for facts that available evidence can answer.
- Mistaking extensive research for alignment on current choices.
- Treating a plausible synthesis as a confirmed decision.
- Using a generic questionnaire disconnected from evidence and prior answers.
- Failing to update the working model, repeating settled questions, or hiding contradictions in vague language.
- Stopping after one round without testing the consequences of the answers.
- Bundling independent decisions into one question.
- Continuing interviews after only low-impact uncertainty remains.
- Sharing sensitive information more broadly than the task requires.
- Writing an inspiring document that leaves decisions, ownership, or execution unclear.
- Mistaking concise writing for choppy writing, or delivering formatted output without checking that the layout is usable.


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
description: Draft or revise email in the user's authentic voice while keeping facts, commitments, privacy, and recipient context appropriate.
---

# Write in my voice

Use this workflow when drafting, replying to, or polishing an email on the user's behalf.

## Goal

Produce a copy-ready email that sounds recognizably like the user rather than generic assistant prose. Match the user's usual warmth, directness, structure, greeting, sign-off, and punctuation while adapting appropriately to the recipient, relationship, and stakes.

## 1. Establish voice evidence

Before drafting, review the user's current writing guide in full, if one exists. If the user authorizes access to prior sent emails or drafts, use only the minimum relevant examples needed to understand their voice. Prefer recent messages and examples similar in audience and purpose.

Access private communications only for a legitimate purpose with clear authorization. Do not expose, repeat, or use unrelated personal details, confidential information, or sensitive facts from those materials.

Create a practical voice profile from the evidence:

- Typical greeting and sign-off.
- Formality level and relationship cues.
- Sentence and paragraph length.
- Preferred vocabulary, contractions, directness, and colloquialisms.
- Punctuation, capitalization, and formatting habits.
- Phrases, tones, or punctuation the user avoids.
- How the user requests action, declines, follows up, corrects, apologizes, or expresses uncertainty.
- Approved reusable facts, links, boilerplate, and standard responses.

Recent sent messages and deliberate user edits outweigh older examples or generic style advice. If evidence conflicts, ask which preference is current. Never treat an old pattern as a rule when the user gives a different instruction for the current email.

## 2. Confirm the email brief

Identify the minimum information needed to send a correct and appropriate email. Ask focused questions only when a missing answer would materially change the message.

| Needed information | What to establish |
|---|---|
| Recipient and relationship | Who will receive it and whether they are a colleague, client, partner, manager, or another contact. |
| Desired outcome | What the recipient should know, decide, do, or reply to. |
| Required details | Accurate names, dates, links, attachments, amounts, decisions, and context. |
| Tone and stakes | Whether it should be routine, warm, firm, formal, sensitive, or urgent. |
| Boundaries | Deadlines, approvals, confidentiality needs, and commitments the user is authorized to make. |

Do not invent availability, decisions, promises, prices, credentials, opinions, emotional reactions, or facts. Do not imply that an attachment was included, a meeting was scheduled, or another person approved something unless that is confirmed.

## 3. Adapt voice to context

Voice is not a rigid template. Preserve recognizable habits while choosing wording suitable for the recipient and situation.

- **Close working relationships:** Use the user's normal concise and familiar style.
- **New, external, senior, or high-stakes recipients:** Keep the user's voice, but provide enough context and use more careful wording.
- **Requests:** State the requested action, responsible party, and timing plainly.
- **Corrections, conflict, or rejection:** Be direct, factual, and respectful. Avoid defensive explanations, exaggerated praise, and unnecessary apologies.
- **Sensitive matters:** Include only information appropriate for the recipient and channel. Avoid unnecessary personal detail and make no disclosure beyond the user's stated access boundary.

Use approved standard wording, links, or factual material when it fits the current context. Do not reuse boilerplate if it would mislead, overpromise, or sound out of place.

## 4. Draft the smallest complete email

Use the shortest structure that lets the recipient understand and act. A useful default is:

1. Greeting, when the user's examples normally include one.
2. Purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Closing and sign-off, when appropriate.

Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Put the main request or decision where it is easy to find. Use bullets only when they make actions, options, dates, or logistics easier to scan.

Remove content that does not help the recipient:

- Throat-clearing and narration about the drafting process.
- Generic compliments, repeated thanks, or empty pleasantries.
- Filler such as “just wanted to” or “I hope you’re well,” unless it is both normal for the user and useful in context.
- Hedging that weakens a clear message.
- Details that belong in internal notes rather than the recipient-facing email.

## 5. Audit before presenting

Review the draft line by line:

- Would the user plausibly write these words?
- Do greeting, sign-off, punctuation, rhythm, and formatting match the available evidence?
- Is the formality right for this recipient and situation?
- Does the email make an unsupported commitment, claim, opinion, or emotional statement?
- Are names, dates, links, amounts, attachments, and references accurate?
- Is the requested action unmistakable?
- Does the email reveal only information appropriate for the recipient?
- Can any sentence be removed without losing meaning or usefulness?
- Does it avoid language or habits the user has identified as undesirable?

If no voice evidence exists, use a broadly useful default: concise, clear, warm-professional, and direct. Briefly state that assumption if needed, and invite the user to provide a few authorized examples or preferences for future drafts.

## Output format

Provide the final email as copy-ready text. If clarification is necessary, ask only the specific question needed to draft safely. Do not add explanations after the draft unless the user asks for alternatives, rationale, or revisions.


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
description: Create an evidence-based case study post about a person’s professional, learning, or career change, with review-ready hooks, quote-card options, approval checks, and a clear publication plan.
---

# Write a case study post

Use this workflow to turn authorized source material into a concise, credible public case study. It works well for professional social posts, community updates, newsletters, recruitment pages, program stories, and alumni features.

The goal is not vague praise. Show a specific, evidence-supported change: where the person started, what they were considering, what prompted action, what concretely helped, what happened next, what they do now, and what a relevant reader can do.

A strong post helps readers recognize their own situation in the subject’s before-state. It explains a plausible mechanism without claiming that a course, community, employer, mentor, or tool single-handedly caused an outcome.

## Use and authorization boundary

Use this workflow only for a legitimate publishing purpose and with clear authorization to use the source material.

If sources include private interviews, applications, internal messages, private profiles, meeting notes, or records about an individual:

- Use the minimum relevant sources and information needed for the approved story.
- Include only details relevant to the public message.
- Respect the subject’s consent, privacy expectations, and the publisher’s access boundary.
- Do not include unrelated sensitive details about finances, health, family, housing, legal matters, immigration, identity, employment conflicts, or personal relationships.
- Do not reveal nonpublic organizations, teams, projects, locations, or dates unless they are approved for publication.
- Do not treat an internal celebration message as sufficient proof when direct confirmation or a reliable public source is available.

When in doubt, ask whether a detail is both necessary for the story and approved for the intended audience. Omit it if the answer is unclear.

## Inputs and intake gate

Collect the available material. Useful inputs include:

- Authorized interview transcripts and meeting notes
- Intake, application, or survey responses
- An approved biography or current professional profile
- Public work samples, published projects, announcements, or papers
- Authorized internal notes that point to verifiable facts
- A rough draft, outline, or notes from the subject
- The publishing platform, target audience, intended call to action, and desired voice
- An approved editorial or brand guide

Before writing, create a private working record. Do not include this record in the public post.

| Field | What to capture |
|---|---|
| Subject | Approved public name, preferred short name, pronouns if relevant, and consent status |
| Before-state | Previous role, field, goal, uncertainty, or relevant constraint |
| Alternative | What they were considering or doing instead |
| Trigger | Why they joined, applied, changed direction, or acted at that time |
| Intervention | The approved program, resource, event, community, mentor, or product involved |
| Mechanism | One or two concrete things that helped, such as feedback, an introduction, a shared opportunity, or a realization |
| Now-state | Approved current role, type of work, output, or result |
| Timeline | Verified dates and elapsed time from starting point to outcome |
| Evidence | Sources for claims, figures, quotations, artifacts, and dates |
| Cost or risk | Any approved tradeoff that is useful to the story |
| CTA | Intended reader, next action, and destination |

If a material fact is missing, ask focused questions before drafting. Do not guess at names, role titles, organization names, team names, dates, timelines, figures, publication titles, or outcomes.

Use questions such as:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they act at that particular time?
4. What were the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a public project, placement, product, publication, grant, or other output that can be named?
8. Did they take on a meaningful cost or risk that they are comfortable sharing publicly?
9. Which claims, figures, names, and quotes are approved for publication?
10. Who should see themselves in this story, and what should they do after reading it?

## Evidence and verification rules

Never invent facts or strengthen a claim to make it more dramatic. If a source says someone contributed to a project, do not call them the lead. If they explored an opportunity, do not write that they received it. If work is unpublished, do not present it as published.

Automated transcripts are useful but fallible. They can mishear names, organizations, technical terms, job titles, numbers, and dates. Cross-check important transcript details with a more reliable source.

Use this default evidence order:

1. The subject’s direct, recent approval or confirmation
2. Official public records, published work, or an authorized announcement
3. A current professional profile approved by the subject
4. The person’s original written application or statement
5. Interview transcripts and automated summaries
6. Informal third-party messages

If sources disagree, resolve the disagreement before publication. If it cannot be resolved, omit the detail or mark it as unconfirmed in review notes. Do not make uncertainty disappear through smoother prose.

In working notes, distinguish:

- **Verified fact:** A claim supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn from the story. Use it only when evidence supports it, and phrase it carefully.

Do not claim that an intervention caused a job, publication, or career outcome unless evidence supports that claim. Prefer precise wording such as “They found the opportunity through the community” or “The program helped them see roles that matched their experience.”

## Sensitive-content approval gate

Require explicit subject approval before publishing:

- Salary, compensation, pay cuts, financial hardship, or comparisons
- Health, family, legal, immigration, housing, or other personal circumstances
- Strong language about a past employer, role, colleague, or career decision
- Unreleased work, confidential projects, unpublished titles, or nonpublic hiring information
- Named direct quotes, especially criticism or strong opinions
- Claims about why an employer selected the person
- Precise facts that could create personal risk or expose private circumstances
- Claims that a program, community, mentor, or individual caused an outcome

If approval is unavailable, use an approved and honest fallback or remove the line. For example, replace a precise compensation statement with “they accepted a lower-paying role” only if that broader statement is also approved. Do not conceal uncertainty with vague drama.

## Build the story beats

Create a concise private outline before drafting.

### 1. Before-state

Capture the person’s previous role, relevant background, and reader-relevant uncertainty. Include the alternative they were considering when it mirrors the reader’s current life.

Keep only details that drive the story. Long lists of credentials, reading, former roles, or accomplishments usually weaken the post. A specific alternative plan, interview, project, or decision can make the change feel real.

### 2. Trigger

Identify why the person acted then. They may have wanted to learn whether a field was viable, find collaborators, test a career direction, solve a practical problem, or make a values-driven choice.

### 3. Mechanism

Find one or two observable turning points. Strong mechanisms include:

- Realizing that a field has roles suited to their existing experience
- Finding a relevant opportunity through a community
- A conversation that clarified a practical next step
- Feedback that improved an application, project, or portfolio
- An introduction, event, workshop, or concrete resource

Avoid “the experience was transformative.” Say what happened instead.

### 4. Now-state and timeline

Record the person’s approved current role, practical work, and relevant output. Translate specialized language enough for the intended reader to understand it.

Map the sequence from beginning to outcome. Use a short, truthful timeframe when it sharpens the story, such as “five months later” or “the following year.” Do not force a compressed timeline when the dates do not support it.

### 5. Quotes

Extract three to five verbatim quote candidates. Favor lines that speak to the reader’s uncertainty or identity, not only the subject’s achievement. Light trimming is allowed only when it preserves wording, meaning, and grammar.

Use these categories:

1. **Discovery:** A line about not knowing a path was available.
2. **Mechanism:** A line about what concretely helped.
3. **Conviction:** A line about why the choice was worthwhile.

## Generate three hooks

For feed-based platforms, the first two lines determine whether people continue reading. Draft three distinct hooks before drafting the body. Keep each to two short sentences. Where brevity matters, aim for roughly 140 characters total.

### Hook A: Discovery

Use when the target reader shares the subject’s former blocker.

**Formula:** The person did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a concrete mechanism.

This is the default when the reader should think, “That might be me.”

### Hook B: Identity collision

Use when the before-and-after contrast is unusually vivid.

**Formula:** A short time ago, the person was doing a specific thing. Today, they are doing a sharply different specific thing.

This often works best for broad audiences rather than close peers of the subject.

### Hook C: Stakes-led

Use only when an approved cost or risk communicates honest conviction rather than avoidable hardship.

**Formula:** The person accepted a specific cost to do something. Now they are taking a concrete action or doing meaningful work.

Do not use this hook if it makes the desired path seem inaccessible or implies that sacrifice is expected.

Choose one recommendation. State in one sentence why it fits the audience, and briefly state why each alternative is less suitable.

## Draft the post

Aim for 160 to 220 words unless the platform or audience requires another length. Shorter is usually stronger.

Use this structure when evidence supports it:

1. **Hook:** Use the recommended option.
2. **Before-state:** One short paragraph with the previous situation and relevant alternative.
3. **Name the intervention:** Clearly say that the person joined the program, used the resource, or entered the community.
4. **Mechanism and immediate outcome:** Explain the turning points, then land the result in plain language.
5. **Current work:** State what they do now and why it matters in understandable terms.
6. **Optional cost:** Include only if approved and genuinely useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already carried by the hook or body.
8. **CTA:** Address the reader directly and offer one clear next action.

For platforms that may reduce distribution for external links in post text, place the destination in a comment, profile, or another designated location. Treat this as a platform-specific publishing choice, not a universal rule.

## Style rules

Adapt to the chosen voice guide. If none is provided, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense where possible.
- Use names, roles, dates, figures, and artifacts only when verified and approved.
- After the first full introduction, use the subject’s approved short name if it fits the publication tone.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not call someone exceptional, inspiring, or brilliant without showing relevant evidence.
- Use contractions if the voice is conversational.
- Keep the CTA in full second person.
- Avoid emojis unless they are an explicit brand choice.
- Do not use em dashes. Use periods, commas, or line breaks instead.

On the final pass, remove machine-like phrasing: empty transitions, dramatic setup frames, filler intensifiers, hedge words, abstract nouns that replace evidence, balanced arguments, and reflective summaries after the CTA.

Avoid terms such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm” unless they are essential in an approved direct quote.

Read the post aloud. If it sounds like generic thought leadership, shorten it and replace abstractions with facts.

## Quote-card options

Provide three quote options for a graphic. Each should be self-contained, under 15 words when possible, and verbatim from approved material.

Provide one from each category: Discovery, Mechanism, and Conviction. Recommend one with a one-sentence rationale. Discovery usually works best because it needs little context and mirrors a reader’s uncertainty. Choose another category only if it is clearer and stronger on its own.

## Readiness audit

Before sending for review, verify:

- Every name, role, figure, title, date, and timeline is supported.
- Important transcript-derived details were cross-checked.
- The post shows a concrete mechanism, not merely an outcome.
- Causation is not overstated.
- The intervention is named clearly.
- The opening reflects a real audience concern.
- Current work is understandable to the intended reader.
- Sensitive claims and quotes are flagged for approval.
- The CTA is clear and appropriate to the platform.
- There are no em dashes, unsupported superlatives, corporate phrases, or generic filler.
- The draft stays within the approved access and privacy boundary.

## Delivery and iteration

Create the draft in the user’s chosen document system when available. Use a clear title format:

`YYYY-MM-DD: Case study post, [Subject short name]`

In the accompanying message, provide only:

- The recommended hook and two alternatives
- The three graphic-quote options and recommendation
- Approval items before publication
- Missing information that would strengthen the draft
- The document location or link, if available

Do not treat the first draft as final. If feedback is “make the hook better,” generate new hooks rather than making minor edits. If asked to shorten the post, cut secondary biography first while preserving the mechanism and outcome. If a subject declines a sensitive line, replace it with the approved fallback without weakening the entire story.

After a final version is accepted, review feedback for reusable lessons. Update the workflow only when a clear recurring pattern emerges, such as a missing intake question, repeated editorial preference, or a recurring verification problem. Do not create new process rules from a clean review cycle.


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
description: Review authorized meeting records, identify genuine unfinished commitments, create clear deduplicated follow-up tasks for confident decisions, and batch only the questions that require human judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked. Access meeting records only for a legitimate work purpose, with clear authorization, and use the minimum relevant material. Keep sensitive personal information out of task notes unless it is necessary for completing the work and appropriate for everyone with access to the task system.

## Purpose and operating rules

Before each run, apply these outcome rules:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels it as an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work that was completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, a statement of interest, or an open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply delegation boundaries and responsibility assignments supplied by the user or organization. Attendance at a meeting does not make the user accountable for all work in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this broadly useful default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect only the information needed for action capture:

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

If the record includes sensitive information unrelated to the follow-up, do not copy it into the task. Link to the authorized source where appropriate instead of reproducing private details.

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
- Authorized source links and relevant supporting materials

Create no task when work was completed live, another person owns it, the meeting was purely informational and any needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

## 4. Decide the task shape

Combine actions into one task when they have the same counterparty, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect months later.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

Use this readiness gate before task creation: every proposed task must have a clear owner, an unfinished outcome, a sensible scope, a plausible due date, and enough context to stand alone. If any of these are uncertain, hold that item for the batched-question step.

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
- Meeting record: <authorized link>
- Related document: <authorized link>
```

Avoid unnecessary private discussion in a task system that may be broadly visible. Follow the user’s known writing preferences. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable. If the task is to send a message, write a ready-to-send draft rather than merely saying “email them.” For introductions, use double opt-in: seek permission from each relevant party before connecting them.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by meeting link or identifier, counterparty, distinctive topic terms, and proposed title.

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. Skip the new task, or update the existing task if the meeting adds a meaningful action, deadline, or context. Record the duplicate decision so it can be reported clearly.

## 7. Create confident tasks

Create high-confidence tasks in a batch when possible. If the environment supports opening created records, open them in the selected task system rather than filling the status update with management links.

For every skipped meeting, give a brief reason, such as “No out-of-meeting commitment,” “Completed during the call,” “Owned by another role,” or “Already covered by an active task.” Do not expose more personal detail than necessary in the report.

## 8. Batch uncertain questions

Skip this step entirely when all decisions are confident. Do not interrupt for each ambiguity. Create confident tasks first, then ask all remaining questions together.

Ask the smallest question that resolves ownership, scope, timing, completion status, delegation, or duplicate handling:

```markdown
**[Meeting title]**
Question: [One specific question]
Context: [One sentence grounded in the authorized record]
Option A: [Task to create or update if true]
Option B: [Skip or alternate task shape]
```

Wait for answers before creating uncertain tasks. After answers arrive, create or update the remaining tasks and rerun any necessary duplicate check if the answer changed the task outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, capture lessons that genuinely improve future runs. Keep this separate from the meeting task itself.

- Add a short, generalized note to a reusable meeting-archetype reference when a recurring pattern affects triage, such as a common attribution error, reliable sign of in-meeting completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new delegation boundary in the user’s or organization’s maintained responsibility reference when it applies beyond one meeting.

Do not turn one-off facts into permanent rules. Small additions to a patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing steps or changing the evidence order. Briefly report any reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links to an authorized source record.
- Message drafts are ready to send and follow the user’s preferences.
- Sensitive or unrelated personal details were omitted.
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
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account and privacy boundaries, verifying rendered page state, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing dynamic forms, changing dashboard settings, collecting information from rendered pages, testing user flows, or working in authenticated accounts. Choose the least invasive authorized method, inspect page state before editing, read back meaningful changes, and treat consequential actions as a separate commitment step.

> A browser command that reports success does not prove the website accepted the change. Verify the page's actual state before relying on it or proceeding.

Modern web applications may maintain state outside the visible DOM, commit a value only after focus leaves a control, replace controls during a re-render, or display an error even after an action has succeeded.

## 1. Choose the least invasive authorized route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented and authorized programmatic interface when it can complete the task. It is often more reliable than reproducing browser behavior.
2. **Headless browser automation.** Use for public pages, test environments, routine dynamic-page extraction, screenshots, UI testing, and forms that do not require an existing signed-in identity.
3. **User-visible authenticated browser session.** Use only when the task genuinely requires an existing session, single sign-on, an account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for a legitimate direct route. Check official documentation, ordinary form actions, page source, and visible network activity for supported endpoints. A rendered form may submit structured data through an authorized service that is safer and more reliable to use directly.

Do not use undocumented endpoints to bypass access controls, consent boundaries, service restrictions, or security protections. Do not use an authenticated visible session merely for convenience: it can interrupt the user's work and increases privacy and account risk.

If a site blocks automated browsing, do not try to evade the block for research or collection. A verified visible session can be appropriate when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and an established session is necessary. Do not weaken browser security, authentication, warnings, or anti-abuse controls to make automation work.

## 2. Protect privacy, authorization, and account context

When a task accesses private communications, records, dashboards, or information about people, first confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into notes, screenshots, logs, or reports. Keep outputs within the requester's appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated browser, identify the correct account, organization, environment, and browser profile. Do not infer identity from a generic browser label, remembered default, old tab title, or connection name.

Use these rules:

- Announce when taking control of a visible browser and state the task purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing tab to use.
- Classify the context explicitly, such as personal, work, testing, staging, or production.
- Select the browser profile or connection that corresponds to that context rather than using a generic selector that may choose a recent profile.
- Confirm the signed-in account with a reliable account indicator before opening or changing the real target.
- If the required account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not reveal credentials, session tokens, recovery details, security settings, or unnecessary private account data in output or logs.
- Do not disable multi-factor authentication, browser warnings, security checks, or access controls.

Use an account preflight gate before any action that changes data. Answer these questions: **Which account is this? Which environment is this? What exact item will change?** If the automation environment provides a verification marker or permission gate, mark the context verified only after the account check actually passes. Never enable a gate in advance merely to unlock more powerful actions.

## 3. Establish the task boundary and authorization

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, or workflow.
- The information that will be entered, collected, changed, or uploaded.
- The minimum information needed to complete the request.
- Whether the final action is reversible.
- Whether the task sends, publishes, pays, deletes, grants access, changes a plan, or creates another external commitment.
- Missing information, ambiguous choices, and fields that require user judgment.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and collecting a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, or applying an irreversible account change may not be.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify all values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Re-check the account, target, and readiness gate. If clear authorization for the exact final action already exists, proceed. If authorization is absent, ambiguous, or the user requested review before submission, show a concise prepared-state summary and ask only for the final action.

Payments, deletion, access or plan changes, and actions clearly labeled final, permanent, or impossible to undo require confirmation immediately before acting unless the user has already explicitly authorized that exact commitment. For low-risk reversible changes explicitly requested by the user, proceed after normal verification unless the page presents an unexpected warning or broader effect.

If the page reloads, re-renders, or the session changes between phases, do not assume the earlier state remains valid. Restore the intended values if needed and verify them again before committing.

## 4. Inspect the rendered page before editing

Do not start by guessing selectors, filling controls by numeric position, or trusting a visual approximation. First inspect the rendered page and collect enough structure to identify controls safely.

For each relevant field, determine:

- Element type: single-line input, multiline area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether the field is required.
- Validation rules, character limits, formatting behavior, and disabled state.
- Whether an apparent field is an editable control, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, tab, or date causes a re-render.

Address controls by stable semantic identity, such as visible label text, accessible name, or an explicit label relationship. Do not use DOM indexes where labels are available: dynamic applications can reorder controls after loading or re-rendering.

Before changing an existing record or setting, inspect its current state. This avoids modifying the wrong item or unintentionally overwriting existing values.

### Generic inspection pattern

Use the selected automation library to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

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

A generic “set value” action is not reliable for every widget.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use normal text entry or fill behavior | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select existing content, enter text through keyboard-style events, then blur | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle | Selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed | Clicking may toggle an already-correct value. |
| Date/time picker | Choose date and time, then verify the rendered summary | Popovers can reinterpret typing or clear related values. |
| File upload | Confirm file, destination, and privacy implications first | Uploading may start immediately and be difficult to undo. |

For framework-driven editors, simulate ordinary user interaction rather than writing low-level page properties. A robust sequence is: focus the actual editable element, select existing text, delete it, enter the new text with keyboard-style events, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible rich-text editor with a hidden input. Editing the hidden input can appear successful in a DOM dump while server-side validation treats the actual editor as empty. Target the visible interactive control that the application reads. If an accessibility locator finds an empty wrapper, inspect the underlying labeled control and follow its label relationship.

If dropdowns, checkboxes, tabs, or dates can refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterward and confirm earlier entries remain present.

## 6. Verify after every meaningful edit

After each field is filled or setting is changed, read its value back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare lengths, required state, or a minimal redacted summary rather than exposing the full value unnecessarily.

Check for these common mismatches:

- Automation reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displayed text but did not retain it internally.
- A later interaction erased an earlier field during a re-render.
- A hidden synchronization field was changed instead of the visible editor.
- A selection altered a dependent field, date, recipient, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once using a more appropriate interaction method, and verify again. If the page continues to reject or alter the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 7. Run a pre-submit readiness gate

Before a final submission or high-impact change, inspect the full relevant page state again. Confirm all of the following:

- The correct account, organization, environment, and target item are active.
- Every required field is present and non-empty.
- Each entered value matches the intended content closely enough for the task.
- Dropdowns, checkboxes, dates, recipients, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially filled form is recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only within the appropriate access boundary. Avoid placing sensitive field values in a large inline table when a short summary and a securely available record are sufficient.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] Authorization for the final action is present.
- [ ] The final action and its impact are understood.

## 8. Commit once and verify completion

A button click is not proof of success. Activate the final control only after the readiness gate and any needed confirmation pass. Avoid repeated clicks and blind retries, especially for actions that can create duplicates such as messages, submissions, payments, invitations, or records.

After the action, look for reliable evidence such as a success message, confirmation reference, newly created record, persisted setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve only relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Do not describe an attempted action as completed.

## 9. Failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after a later edit | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline or editor control, or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control the application actually reads. |
| A date or option changes unexpectedly after another edit | A popup, dependency, or re-render altered related state | Close transient controls through a neutral page action and re-verify all affected fields. |
| The automation layer becomes unstable on a complex page | The selected method is unsuitable | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and ordinary browsers differ | The site changes behavior by browser context | Prefer an authorized direct interface; if needed for an explicit task, use a verified visible session without evading protections. |
| A visible error may be cosmetic | The task may already have completed | Inspect resulting state before retrying. |
| Account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## 10. Final audit checklist

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only the minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back and verified.
- [ ] Required fields and validation state passed the readiness gate.
- [ ] A pre-action record was captured when the action was consequential.
- [ ] Authorization was confirmed for any consequential final action.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, improve an existing skill, evaluate whether a skill helps, or refine when it activates. A skill is a focused set of instructions, with optional resources such as scripts, references, and templates, that helps an AI carry out a recurring job consistently.

The core loop is:

1. Understand the intended job, boundaries, and user value.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with a person and measure objective requirements where appropriate.
5. Improve the skill using the evidence.
6. Repeat until the result is useful, reliable, and not narrowly fitted to the test examples.
7. Optionally improve the skill description so it activates for the right requests.
8. Package and hand off the finished skill.

Do not assume every project needs every step. Some users want a quick collaborative draft. Others need a rigorous comparison. First determine where the user is in the loop, then help them make the next useful decision.

## Communication principles

Match the user’s technical vocabulary and experience. Use plain language by default. Terms such as *evaluation* and *benchmark* are often acceptable, but explain them briefly when helpful. Avoid unexplained technical terms such as “schema,” “assertion,” or “JSON” unless the user is already using them comfortably.

Explain why questions matter. For example:

> What should a successful result look like: a chat response, a structured report, a file, or an approved external action? The answer determines how the skill should work and how we can test it.

Keep the user involved at important choices:

- Confirm the intended job before writing extensive instructions.
- Ask before introducing restrictive policies, required tools, or approval steps.
- Share proposed test cases before treating them as the evaluation set.
- Let human judgment lead for subjective outcomes such as writing quality, visual design, tone, or strategic usefulness.
- State uncertainty plainly rather than inventing a requirement or pretending a result was verified.

If the proposed skill would access communications, records, files, or information about people, establish a legitimate purpose and clear authorization first. Use only the minimum relevant sources and data, omit unrelated sensitive details, respect reasonable privacy and consent expectations, and keep outputs within the user’s authorized access boundary.

## 1. Determine the starting point

Identify which starting condition applies.

### New skill

The user has an idea such as “I need help producing recurring project updates.” Start with discovery, scope, and a first draft.

### Existing skill

The user has a current instruction set and wants it edited, simplified, tested, or optimized. Read it before proposing changes. Preserve the established name and identity unless the user explicitly requests a rename.

Before modifying an installed or otherwise protected copy, work from a writable copy. Preserve an unchanged snapshot so later evaluation can compare the revision to the prior version.

### Workflow demonstrated in the conversation

The user may say “turn what we just did into a skill.” Extract what can already be inferred from the conversation:

- Inputs and source materials used.
- Tools or capabilities used.
- The sequence of actions and decisions.
- Corrections, preferences, and approval points from the user.
- Observed output format.
- Acceptance criteria and failure handling.

Summarize the inferred workflow and explicitly list gaps that need confirmation. Do not turn a one-time workaround into a general rule without checking whether it applies broadly.

### Evaluation or optimization request

The user may already have a finished-looking skill and want to know whether it is effective. Go directly to test design, evaluation, and evidence-based revision. Do not rewrite a skill only because rewriting is possible.

## 2. Capture intent and scope

Gather enough detail to define one coherent job. Do not ask every question mechanically; start with the missing information that most changes the design.

Use these questions as needed:

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What user requests, wording, or situations should cause the skill to be used?
3. **Inputs:** What information, files, references, systems, or permissions may it use?
4. **Outputs:** What should it produce, change, or recommend? Is there a required format?
5. **Success:** How will a user tell whether the output is correct, useful, or complete?
6. **Boundaries:** What should the skill not do? When should it ask a question, pause for approval, decline, or return work to the user?
7. **Variations:** Which common cases, difficult cases, exceptions, or decision points matter?
8. **Dependencies:** Does the work require a particular capability, template, reference, script, or user-provided access?
9. **Testing:** Should the skill be evaluated using representative requests?

Offer useful choices when requirements are unclear:

- “When information is missing, should the skill make a clearly marked best-effort draft or stop and ask?”
- “Should the default be concise, detailed, or selected by the user?”
- “May it use any accessible source, or only sources the user explicitly approves?”
- “Should it prepare a recommendation, or is it allowed to make a reversible change without further confirmation?”

Recommend realistic tests when the workflow is repeated, consequential, format-sensitive, or objectively checkable. For primarily subjective work, recommend a small human review set rather than forcing weak numerical measures.

### Research before drafting

If approved documentation, comparable skills, standards, example artifacts, or domain references are available, consult them before drafting. Research should reduce the burden on the user, not replace the user’s authority over goals and constraints.

Use research to identify:

- Existing conventions and output standards.
- Constraints of available file formats or capabilities.
- Reusable patterns from related work.
- Privacy, safety, compliance, or approval requirements.

If sources disagree, are incomplete, or are outside the user’s authority, present the uncertainty and ask how to proceed.

## 3. Choose the skill structure

Keep a skill focused enough that people and AI systems can predict what it does. A skill may support related variants of one job, but separate unrelated jobs that have different audiences, permissions, source-of-truth rules, or definitions of completion.

A typical package can contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional supporting documentation
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A concise name and description that support activation.
2. **Core instructions:** The workflow used in most cases.
3. **Supporting resources:** Detailed references, templates, or executable helpers loaded only when relevant.

Keep the core instruction file readable. If it grows too large, move specialized material into clearly named references and state exactly when to consult each one. Large reference documents should include a contents or navigation section.

For a skill with multiple technical or domain variants, keep a shared selection workflow in the core instructions and place variant-specific guidance in separate files. The AI should choose the relevant variant rather than load every reference by default.

### Bundle reusable helpers carefully

If repeated test runs independently reconstruct the same helper procedure, consider bundling it as a script, template, or checklist. This is especially useful for deterministic tasks such as conversion, validation, extraction, calculations, or repetitive formatting.

Add a helper only when it is clearly reusable, understandable, and within the user’s authority. Document:

- What it does.
- Its inputs and outputs.
- When to use it.
- Its limits and failure behavior.
- How it handles data safely.

Do not add automation merely because it is possible. The skill should not conceal actions, bypass access controls, extract confidential information, damage systems, or take surprising external actions.

## 4. Write the skill

Write in clear, imperative language. Explain the reason behind important instructions, especially where a rule prevents a predictable error. AI systems can adapt better when they understand the goal and tradeoff than when they receive a long list of unexplained restrictions.

Include the following sections when they fit the task.

### Purpose and scope

State the job, intended outcome, and boundaries. Clarify whether the skill produces advice, a chat response, a file, a draft, or an external action.

### Inputs and prerequisites

List required inputs, permitted sources, required capabilities, and optional materials. State what to do if a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and approved data source.
If a source is unavailable, ask for an export or provide a draft clearly marked as incomplete.
```

For sensitive information, specify the authorization boundary. For example, direct the AI to use only approved records relevant to the stated purpose and to exclude unnecessary personal details from the result.

### Workflow

Describe the normal sequence and the meaningful decisions. A durable general pattern is:

1. Inspect the request and available inputs.
2. Confirm ambiguity only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Complete the task using the appropriate method.
5. Validate the result against the requested format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limitations.

Use conditional rules rather than attempting to list every possible situation:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a requested action could overwrite important work, explain the impact and request confirmation first.
```

### Output format

Use a stable template when consistency matters:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or missing information]
```

Do not impose a rigid structure if the value of the task depends on adapting to context. In that case, define the desired qualities and show a short generalized example instead.

### Quality, safety, and readiness checks

State what must be checked before the skill presents work as complete. Suitable checks include:

- Required fields, sections, or files are present.
- Calculations are validated against an approved source.
- Important claims identify their supporting source.
- Original data is preserved when modification is risky.
- Assumptions and gaps are visible to the user.
- External, irreversible, or high-impact actions have the required approval.

The actual behavior of the skill should match what its description reasonably leads a user to expect. Refuse or redirect requests that would enable unauthorized access, deception, harmful surveillance, data exfiltration, destructive behavior, or other actions outside legitimate authority.

### Failure behavior

Define recovery behavior in general terms:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or source:** State what could not be checked and offer a safe alternative.
- **Ambiguous request:** Make a low-risk assumption only if it does not materially affect the outcome; otherwise ask.
- **Validation failure:** Correct the issue, mark the output incomplete, or request guidance. Do not present an unverified result as final.
- **Permission-sensitive action:** Pause for confirmation before external, irreversible, or high-impact changes.

### Examples

Use only a few short, generalized examples when they teach a distinct pattern. Examples should illustrate reasoning or format, not replace reasoning with a narrow collection of cases.

## 5. Write the activation description

The skill description is a routing instruction. It should state both what the skill does and when it should be consulted.

A strong description includes:

- The outcome or job.
- Common contexts and user phrasing that signal the job.
- Important scope limits that prevent costly or unsafe false activation.

Example:

```text
Create clear project status reports from approved updates and source material. Use for requests for progress summaries, leadership updates, milestone reviews, risks, blockers, or next steps, including requests that imply a status report without naming one.
```

Cover realistic wording, including requests that imply the task instead of naming it. Do not place the full procedure in the description. Do not make the wording so broad that it captures unrelated work better handled by another skill.

## 6. Review the draft before testing

Read the draft as if encountering it for the first time. Check:

- Is the job coherent and appropriately bounded?
- Does the description explain when to activate the skill?
- Are inputs, permissions, sources, outputs, and completion criteria clear?
- Does the workflow handle normal variation and missing information?
- Are safety and privacy boundaries explicit where needed?
- Are there repeated instructions, brittle wording, or unnecessary rules?
- Does the skill assume a particular person’s habits, access, tools, or terminology?
- Does a capable AI have enough flexibility to solve normal cases well?

Prefer lean, understandable instructions. Excessive absolute language is a warning sign unless the behavior is truly non-negotiable, such as an authorization boundary or safety requirement.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user before relying on them. Add more cases after the first iteration when a new case represents a meaningful category of work or failure.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Supplied files or context.
- The expected outcome in plain language.
- Objective checks, if appropriate.

A portable record format is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates. Flag information you cannot verify.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful variation:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or policy-sensitive request.
- A realistic edge case that changes the workflow.
- A request requiring approval, safe redirection, or refusal when relevant.

Avoid tests that merely repeat the skill’s wording. Vary detail level, phrasing, and user sophistication. Do not use personal or confidential scenarios when a generalized equivalent will test the same capability.

## 8. Run comparisons and preserve evidence

When independent execution is available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged copy before editing and compare the revision against that prior version, or against the previous iteration when that is the more useful decision baseline.

Start all configurations under comparable conditions. If parallel execution is available, launch the skill and comparison runs for every test case together. This reduces environmental differences and avoids selectively creating baselines later.

Organize artifacts by iteration and descriptive test name:

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

For each test, save metadata containing the prompt, a descriptive name, and the checks to be applied. Preserve supplied inputs, outputs, and any available execution information. Capture timing, resource use, and other run metadata immediately when reported, because some systems do not retain it afterward.

If independent comparisons are not available, run a transparent sanity check: follow the skill on each test prompt, preserve the outputs, and ask the user to review them. Do not claim that this is a rigorous baseline evaluation.

## 9. Define and grade objective checks

While runs are in progress, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A produced file opens and has required fields.
- Calculated values match an approved source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- Required source references or approval notes are included.

Record each grade with stable fields for the requirement text, pass/fail result, and supporting evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when required source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests it before finalization."
    }
  ]
}
```

Use programmatic checks when practical. They are generally faster, more repeatable, and reusable across iterations. Do not force numerical checks onto subjective work. Tone, clarity, aesthetics, usefulness, and judgment often require human review; weak proxy measures can cause the skill to optimize for the metric rather than the user’s actual goal.

## 10. Review results with a human

Present both qualitative outputs and quantitative results. Use an available review interface when one exists; otherwise provide accessible files or a clear in-conversation comparison.

For each test case, show:

- The original prompt and relevant inputs.
- The skill output and comparison output, when available.
- Objective grades and evidence.
- Timing or resource information, if available.
- Prior iteration output and feedback, when useful.
- A clear way for the user to leave feedback.

Ask focused review questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, unsafe, or difficult to use?
- Did the skill add work or detail that did not create value?
- Would this work for similar requests with different wording or data?

If a review interface can export feedback, save that feedback with the iteration artifacts. Empty feedback can mean a result is acceptable, but it is not proof that the skill is generally solved. Review the outputs and measurements as well.

## 11. Analyze results beyond pass rates

Aggregate results when possible: pass rate, average duration, average resource use, variation, and differences from the baseline. Present the revised skill before its comparison condition for easier reading.

Then look beyond summary numbers for patterns:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill’s added value.
- **High variation:** Similar runs differ substantially, suggesting ambiguity, unstable conditions, or brittle instructions.
- **Tradeoffs:** The skill improves quality but adds disproportionate time or resource use.
- **Failure concentration:** Multiple failures share one cause, such as unclear source selection or weak output rules.
- **Unproductive work:** Execution traces reveal redundant planning, research, formatting, or tool use.
- **Repeated reconstruction:** Multiple runs recreate the same helper process, indicating a reusable resource may help.

A small benchmark is evidence for the next iteration, not conclusive proof of general quality.

## 12. Improve without overfitting

Revise based on user feedback, outputs, grades, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from complaints. If one test output fails to identify a source limitation, do not add a rule tied only to that exact prompt. Clarify the general behavior: when evidence is incomplete, mixed, or uncertain, distinguish supported information from assumptions and missing data.

Use these principles:

1. **Fix causes, not examples.** Design for future requests, not only the current tests.
2. **Keep instructions lean.** Remove rules that do not improve behavior or create wasted effort.
3. **Explain intent.** State why a step protects correctness, usability, safety, or privacy.
4. **Add reusable resources only when justified.** Bundle scripts, templates, or references when repeated work shows their value.
5. **Preserve useful behavior.** Avoid broad revisions that remove features users already value.
6. **Expand coverage gradually.** Add tests for real categories of failure rather than every isolated incident.

After revision, rerun the full evaluation set in a new iteration and apply the same baseline policy. Show new results alongside previous results when possible. Stop when the user is satisfied, feedback is consistently positive across meaningful tests, objective requirements are reliably met, or further edits no longer make meaningful progress.

## 13. Optional blind comparison

For a more rigorous comparison between two versions, use a blind review. Give an independent evaluator two outputs without identifying which version produced each output. Ask it to judge against a shared rubric, then reveal the mapping only after the judgment is recorded.

Use blind comparison when versions have similar measured performance but visibly different quality, when preference bias is a concern, or when the decision matters enough to justify additional review. Base the rubric on user value: correctness, completeness, clarity, adherence to constraints, safety, privacy, and practical usability.

Analyze why the preferred output won before changing the skill again.

## 14. Optimize triggering behavior

Only optimize the activation description after the skill’s workflow is already useful. Create a realistic set of requests that should activate the skill and nearby requests that should not.

Use a roughly balanced set, commonly eight to ten cases in each group. Make prompts substantive enough that consulting a specialized skill would help.

Positive cases should vary in wording and context:

- Formal and casual requests.
- Directly named and implicitly requested work.
- Common and less common valid uses.
- Cases where a related skill might compete but this one is the better fit.

Negative cases should be challenging near-misses, not obviously irrelevant requests. They should share vocabulary or context with the skill but actually require a different job, capability, or scope.

```json
[
  {
    "query": "I need a concise update for leadership from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what project status reports are generally used for?",
    "should_trigger": false
  }
]
```

Review the query set with the user before evaluating descriptions. If repeated testing is available, separate examples used to improve a description from held-out examples used to select it. Choose the description that performs best on held-out requests, not merely the one that fits the editing set.

Remember that an AI may handle a simple one-step request directly without consulting a skill, even if the description matches. Test with sufficiently complex requests where the skill’s guidance would add real value.

Show the user the before-and-after description and the test results before applying the final version.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description truthfully states what activates the skill.
- The instructions do not depend on personal conventions, undeclared access, or a specific tool unless clearly documented.
- Scripts, references, and assets are included only when needed and are clearly named.
- No credentials, confidential data, unique identifiers, private records, or sensitive examples are included.
- Data-handling guidance respects authorization, purpose limitation, and privacy expectations.
- The user can install or adapt the package in their chosen environment.
- Test material is retained only when safe and useful.

Provide a handoff note explaining what the skill does, required capabilities, known limitations, how to test it after installation, and when users should seek confirmation rather than rely on automation.

## Final readiness gate

A skill is ready when it has:

- A clear, bounded job.
- An honest description that activates for appropriate requests.
- Instructions that handle normal variation and missing information.
- Explicit boundaries for authorization, privacy, uncertainty, and high-impact actions.
- A usable output format or adaptable presentation guidance.
- Evidence from realistic use that it improves outcomes.
- No unnecessary dependence on a particular person, organization, platform, or private operating environment.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user needs.


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

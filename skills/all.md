# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long idea list: it is to identify genuinely different paths, make their tradeoffs clear, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources that are available in the current environment, review the relevant material first.

Only access private communications, records, or personal information when there is a legitimate purpose and clear authorization. Use the minimum relevant sources and details. Do not include unrelated personal information, sensitive details, or material outside the user’s access boundary in the output.

If the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, deadlines, or budgets
- Relevant stakeholder concerns, responsibilities, and approval boundaries
- Evidence about what has already been tried

Do not search broadly by default. Use targeted retrieval only when it could materially change the options. If important information is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- Important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The user’s wording may describe a symptom or proposed solution rather than the real decision. For example, “Should we add a feature?” may actually mean, “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, low-stakes, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must represent a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes the process, incentives, scope, or framing
- At least one surprising option, such as delaying, partnering, narrowing scope, removing a commitment, or doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, or avoiding distraction has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

| Field | Include |
|---|---|
| What | One or two sentences explaining the approach. |
| Strengths | One or two concrete advantages. |
| Weaknesses | One or two concrete disadvantages, limits, or failure risks. |
| Effort | Low, Medium, or High. |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, stakeholder burden, and quality of evidence. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but state clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this user’s situation, constraints, and goals—not merely why it is generally attractive.
4. Name the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may choose an option, request more detail, reject the framing, ask for new options, or combine approaches.

If the user proposes a hybrid, test whether its components are compatible and whether combining them resolves a genuine tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or adversarial review before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that states the choice, owner, rationale, assumptions, constraints, and review point.
- **Build-oriented choices:** After the decision is recorded, move into planning and execution: requirements, milestones, implementation tasks, owners, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than only the user’s first proposed solution.
- The options are genuinely distinct and not cosmetic variations.
- At least one conventional option and one meaningfully different option were considered where relevant.
- Weaknesses are candid, concrete, and proportionate.
- Effort labels are plausible given the available context.
- Recommendations follow the user’s stated criteria rather than the assistant’s default preferences.
- Any private or sensitive context was used only as authorized and only to the extent needed for the decision.


---
name: pressure-test
description: Find the weak points in a leading strategic idea before committing: steelman the case, test its load-bearing assumptions through sequential challenge, and finish with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing a single idea too early can become an exercise in defending it.

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.

## Inputs and evidence boundaries

Start with a claim, decision, or proposed direction. It may be self-contained or supported by research, metrics, experiments, customer feedback, documented decisions, or stakeholder input.

When reviewing communications, records, or documents about people:

- Use them only for a legitimate decision purpose and with clear authorization.
- Review only the minimum relevant sources and information.
- Exclude unrelated personal, confidential, or sensitive details from the analysis and output.
- Respect consent, privacy expectations, and the audience's access boundary.
- Distinguish direct evidence from inference, forecast, and hearsay.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, then challenge vague, unsupported, or evasive answers before continuing.
- Select questions based on the highest-risk assumptions. Do not send the full question list as a questionnaire; that invites selective answers.
- Refer to relevant dissenters by role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is genuinely irrelevant, and state why.
- Keep the output concise. State plainly when the available evidence does not support a conclusion.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intended claim. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

**Template**

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, beginning with the assumption most likely to undermine the decision.

| Rank and assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| [1. State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Name a test or disconfirming signal] |

Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Adapt each later question to the prior answer. Push back on claims such as “I think it will work” by asking for observed behavior, data, a comparison, or a credible commitment.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed? Why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that role say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Record concise answers and the evidence quality behind them. If an answer remains unsupported after follow-up, mark the relevant assumption as unresolved.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failures, external conditions, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or accountable role |
|---|---|---|---|
| [Describe a likely failure] | [Name the mechanism] | [Name an observable early signal] | [Name the check and owner] |

A warning sign is useful only if it appears early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If that perspective has not been sought, mark it as an evidence gap; do not treat silence as agreement.

| Relevant role | Strongest likely objection | Heard directly? | What must be checked |
|---|---|---|---|
| [Role] | [Objection] | [Yes, no, or unclear] | [Question, evidence, or review needed] |

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks supporters may miss.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

**Template**

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step.

- **GREEN — proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER — test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data-collection period. Next: run that test, then make the decision with its result recorded. Do not commit while the named gap remains open.
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

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and giving a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make a clear choice with the right amount of rigor. The goal is not maximum analysis: make routine choices quickly, give consequential choices appropriate scrutiny, preserve an accurate record when authorized, and learn from results.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** Assistant recommendations belong in the conversation and must be labeled as **Assistant analysis**. Put them in a decision record only if the user specifically asks.
4. **Record only with permission.** “Should we do X?” asks for analysis, not creation of a record. Create or update a record only when the user asks to log, track, open, or commit it, or has explicitly agreed to that practice.
5. **Protect privacy and access boundaries.** Before searching shared records, communications, personnel information, or other sensitive sources, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and details. Do not place sensitive information in a record visible to people who should not receive it.
6. **Do not confuse a task with a decision.** If there is no meaningful alternative, say so and move to planning or execution.

For health, relationships, compensation, personnel matters, or similarly sensitive subjects, confirm that a shared record is appropriate before logging. Offer a private document or keep the discussion in chat when that better respects consent and access expectations.

## 1. Select the mode

Determine whether this is a new or existing decision.

- **New:** No relevant record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review date and has not received a meaningful outcome assessment.

If the user explicitly says which mode they want, follow that instruction. Otherwise, if authorized, search the chosen decision register for overlapping titles or questions before creating a duplicate. Do not search private or shared sources merely as a default.

Use these mode checks:

| Signal | Mode | Next action |
|---|---|---|
| No matching authorized record | New | Frame and classify the decision |
| Matching record is open | Resume | Fetch it and append new inputs |
| Open record plus “I’ve decided” or equivalent | Commit | Confirm the choice and complete the commitment record |
| Resolved record, review date reached, and outcome is blank or too early | Review | Run the retrospective |

For a resume, append new information rather than rewriting history. For a review, use the original prediction and reasoning as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Put the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What is the deadline or trigger for deciding?
- What result is desired?
- What happens if no action is taken?

If the request is broad and credible options have not yet been generated, generate options before evaluating them. Do not pressure-test a vague problem statement.

If there is one viable path and the issue is simply whether to execute it, say: “This appears to be a task rather than a decision. The next step is to plan or do it.”

## 3. Classify scope

Ask one clarifying question at a time when classification is unclear. Use the unwind test: **What would it cost to reverse this?** Consider money, time, trust, operational disruption, opportunity cost, and reputational effects. If the cost cannot be named quickly or is uncertain, the choice is probably larger than it first appears.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Choose a reasonable default; do not log by default |
| Reversible | Moderate stakes; can change within days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, and consult relevant stakeholders |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and named prerequisite conversations |

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right rigor

### Trivial

Pick the reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name the attention cost directly: continued deliberation can cost more than an imperfect choice. Do not create a record by default.

### Reversible

Use a short working session:

1. List two or three realistic options.
2. For each, state one principal strength, one principal weakness, and a rough effort or cost estimate.
3. Give a recommendation and the decisive reason.
4. If uncertainty is material, identify the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test considers the main assumptions, disconfirming evidence, likely failure modes, strongest alternative, and significant stakeholder objections.

If no relevant pressure test has occurred in the current work context, stop the commitment flow and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not bypass this merely because the user is in a hurry. Continue only after a pressure test is complete or the user explicitly overrides the gate with a reason.

If the pressure test identifies a serious unresolved failure, do not force a commitment. Return to option generation, redesign the option, gather decision-changing evidence, or run a bounded test.

After the gate is satisfied:

1. Define the options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check who has relevant expertise, bears consequences, or may reveal a constraint.
4. Provide a recommendation, labeled as Assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The choice is not ready until the required conversation has happened, unless the user explicitly accepts and records why proceeding is necessary. If it is being rushed, name the consultation, evidence, or dissent being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence in its favor.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it genuinely clarifies tradeoffs rather than disguising judgment.

Keep these categories distinct:

- **User’s stated view:** Only positions the user actually expressed.
- **Assistant analysis:** The assistant’s recommendation and reasoning.
- **Open question:** Material uncertainty not yet resolved.

If the user has not stated a position, write “No position stated yet” or leave the user-position field blank. Never invent a lean, confidence percentage, rationale, response to dissent, or final choice for them.

## 6. Open, resume, or commit a record

Use the user’s chosen record system only when access is authorized and its audience is suitable. A useful record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

### Open record

For a decision the user wants to continue across sessions, record:

- Status: **Open**.
- Classification, stakes, and reversibility.
- Context and options currently under consideration.
- New factual inputs or conversations.

Leave commitment sections blank until the user commits. Do not fill in a choice, rationale, confidence, or dissent response on the user’s behalf.

### Resume flow

1. Fetch the existing authorized record.
2. Append a dated entry under the thinking log; do not overwrite earlier thinking.
3. Capture new inputs, how the reasoning changed, and the user’s stated position today.
4. Add genuinely new options to the options section.
5. If the user remains open, summarize the current state and identify the next question, evidence, conversation, or test needed.
6. If the user is ready to decide, move to the commit flow.

### Commit flow

Before finalizing, confirm:

- What is the decision and chosen option?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable result is predicted?
- What is the user’s confidence in that prediction?

Set the record to resolved. For a binary question, record the relevant affirmative or negative result. For a non-binary question, record it as resolved once the direction or approach has been chosen.

For meaningful decisions, make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Adjust for a user-specified trigger. For hard-to-reverse and direction-setting decisions, create a calendar or task reminder if authorized and supported; include the decision question and a link or reference to the record. A record-field review date alone is usually sufficient for reversible decisions.

Use clear local dates, such as `DD MMM YYYY`.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** What it is and its central tradeoff.

## Thinking log
### [DD MMM YYYY]
- New inputs, conversations, data, or events
- How the thinking changed
- User’s stated position today: open / leaning / decided

## Dissent
Who raised a concern, their strongest argument, and how it was handled.

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

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat a poor outcome as proof of a poor process, or a good outcome as proof of a sound process.

## Completion message

When a decision is made, summarize it clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [DD MMM YYYY]
Review: [DD MMM YYYY or trigger]
Record: [location, if one exists]
```

Use direct language. Challenge weak reasoning with evidence, but do not use rigor as an excuse for endless deliberation. Once the appropriate readiness gates are met, name the decision and move forward.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, while allowing analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem whose solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start from the underlying problem, not the user's proposed solution. If the request is to “build X,” work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today?
- What workarounds exist?
- How frequent, costly, urgent, or blocking is the issue?
- What outcome would materially improve the situation?

Write a concise problem statement and descriptive requirements. Describe the required outcome and constraints, not an assumed implementation. If the proposed solution does not fit the problem, say so directly.

Ask only for information that cannot be found in authorized project context, documentation, code, or records. When reviewing private communications or records about people, confirm a legitimate purpose and clear authorization; use only the minimum relevant material, omit unrelated sensitive details, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, available alternatives, opportunity cost, and maintenance cost. “Do nothing,” “deprioritize,” or “improve the workaround” are valid options when the issue is rare, low-impact, or adequately addressed already.

Distinguish between decision types:

- **Reversible decisions:** Small choices that are cheap to change. Make a reasonable choice and proceed.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, migrations, long-lived configuration, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the commitment matters.

A useful sequence is: explore possibilities, test the preferred direction, make the commitment, then solve and implement. If direction or priority is unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in detailed design.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before creating new ones.

Identify compatibility requirements, deployment practices, privacy and security expectations, supported environments, ownership boundaries, and monitoring needs. Use established system conventions unless there is a strong reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve existing authentication, authorization, and data behavior.
- Must fit the available delivery time and maintenance capacity.
- Should avoid new dependencies and long-lived configuration where practical.
- Must have a clear verification method.
- Must be reversible or removable if it fails.

These criteria guide solution generation and selection. Without them, the first plausible idea may win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the existing workaround.
2. A non-code solution, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For an ambiguous or high-impact problem, generate a broader candidate set before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases whose behavior changes with runtime conditions.
- Validate inputs and fail clearly for invalid states. Do not silently turn programmer errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is a stated requirement.
- Put changes at the correct design boundary; avoid quick fixes that bypass the system’s structure.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and their tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep the proposal direct. Store it in the user’s chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear, date-prefixed title such as `30 Sep 2026: Solve — topic`.

**Readiness gate:** Do not implement until the problem, recommendation, scope, decision owner, and any hard-to-reverse commitments are clear. If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, dependencies, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership. Keep the plan where appropriate reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, authorization, privacy, and failure behavior.

Use this audit before declaring completion:

- The implemented behavior matches the approved problem statement.
- Tests cover the main path and meaningful failure cases.
- Invalid inputs and internal faults fail visibly rather than producing misleading output.
- Rollback, migration, and operational effects are understood where relevant.
- Documentation, monitoring, and access controls are updated when needed.

Do not claim success based only on implementation. State what was tested and what remains unverified. Commit, publish, or deploy changes only according to the user’s repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and its results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- Links or references to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Common failure modes are solving the requested implementation rather than the real problem, skipping explicit evaluation criteria, treating a permanent commitment as a minor choice, silently masking defects, and declaring completion without meaningful verification.


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
description: Learn a paper, article, post, or topic through a short Socratic dialogue that builds recall, explanation, and application instead of passive reading.
---

# Learn with a tutor

Help a learner understand, retain, and use a paper, article, post, or topic through an active dialogue. Prioritize retrieval, explanation, and application over passive summary. The learner should do most of the thinking; the tutor should guide the process, identify gaps, and adjust the challenge.

## Learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. First ask the learner to reconstruct the ideas in their own words.
- **Probe mechanisms.** Ask why, how, under what conditions, and based on what evidence an idea works. Do not stop at a stated conclusion.
- **Require generation.** Ask the learner to create examples, analogies, predictions, objections, and applications before supplying them.
- **Use productive difficulty.** Make questions demanding enough to require effort, but not so difficult that the learner cannot make a meaningful attempt.
- **Practice transfer.** Move from the original material to new cases, related concepts, and practical decisions.
- **Expose gaps through dialogue.** If an answer is incomplete or inconsistent, use focused questions to help the learner notice the problem. Explain directly only after a fair opportunity to reason.

## Conversation workflow

### 1. Establish prior knowledge and a learning goal

Begin by finding out what the learner already knows, believes, or has experienced. Also ask what they want to be able to explain, evaluate, or do after the session.

Ask one or two open prompts:

- “What do you already think is true about this topic, and what led you to that view?”
- “What are you trying to get better at: explaining the argument, evaluating the evidence, applying the idea, or something else?”
- “Before reading this, what would you have predicted?”

Use the response to set the level of difficulty and identify useful background knowledge or likely misunderstandings.

### 2. Elicit the central idea from memory

Ask the learner to explain the main claim, finding, or problem without quoting the source.

Useful prompts include:

- “In your own words, what is the main claim?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “How would you explain this to a thoughtful friend in 30 seconds?”

If the learner has not read the material, ask for an initial model or prediction. Then direct them to inspect a relevant portion of the source before returning to retrieval.

### 3. Choose a few high-value ideas

Do not attempt to cover every detail. Select two or three ideas that are central, difficult, consequential, or commonly misunderstood. Go deeply enough to test actual understanding.

For each idea, follow this cycle:

1. Ask the learner to reconstruct the idea.
2. Probe assumptions, evidence, causal reasoning, and limits.
3. Ask for an example, analogy, prediction, or application.
4. Test the idea with an objection, alternative explanation, or boundary case.
5. Adapt the next question to the learner’s answer.

Keep turns short. Usually ask only one or two questions at a time.

## Question toolkit

Use questions that require explanation rather than recognition:

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What evidence would distinguish this explanation from another one?”
- “What is the mechanism, step by step?”
- “Can you give a concrete example from a familiar setting?”
- “Where might this fail or stop applying?”
- “What is the strongest objection to this argument?”
- “How does this connect with another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one important assumption changed?”

Avoid questions answerable with only “yes” or “no.” If such a question is useful, immediately follow it by asking for reasoning.

## Responding to learner answers

Be warm, rigorous, and specific. Avoid generic praise. When an answer is strong, identify what makes it useful—for example, it named an assumption, separated correlation from causation, or supplied a relevant counterexample—then raise the level of challenge.

When an answer is incorrect or incomplete:

1. Do not immediately state the correction.
2. Ask a focused question that reveals the tension or missing distinction.
3. Allow one or two real attempts to reason it through.
4. If the learner remains stuck, give a concise explanation.
5. Ask the learner to restate the revised idea or apply it to a new case.

If the learner says, “I don’t know,” encourage an attempt before rescuing them: “Take a guess based on what you do know. What seems most plausible, and why?” Offer a hint after an attempt, or sooner when essential background is missing.

## Calibration and progress checks

Increase difficulty when answers are easy: request a counterexample, competing explanation, prediction, or cross-domain application. Reduce difficulty when the learner is lost: narrow the question, isolate one assumption, use a simpler case, or ask them to defend a choice between two explanations.

Periodically give a brief evidence-based progress check:

- What the learner has demonstrated they understand.
- What remains shaky, uncertain, or incomplete.
- What to focus on next.

Do not treat recognition of a term or repetition of a conclusion as mastery. Look for accurate explanation, sound reasoning, and successful transfer.

## Closing gate

Before ending, ask the learner to turn the lesson into an implication for action or judgment:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation, a self-test question, or a retrieval prompt for later practice. End by naming the most useful idea or question to revisit.

## Guardrails

- Do not summarize unless the learner explicitly asks; even then, invite their own summary first.
- Do not lecture when a well-designed question could prompt retrieval or inference.
- Do not define jargon automatically. Ask the learner to define it first, then clarify as needed.
- Do not make the interaction easy merely to be encouraging.
- Do not cover the whole source superficially when a few important ideas can be understood deeply.
- Keep the exchange collaborative rather than making it feel like a fixed quiz. Base each next question on the learner’s actual response.


---
name: write-in-my-voice
description: Draft or revise emails in the user’s authentic voice using authorized style evidence, verified facts, and a concise final audit. Adapt tone to the recipient and stakes without inventing commitments, details, or emotions.
---

# Write in my voice

Use this workflow when drafting, replying to, or polishing an email on the user’s behalf.

## Goal

Produce a copy-ready email that sounds recognizably like the user rather than a generic assistant. Preserve their usual warmth, directness, structure, punctuation, and brevity while making the message appropriate for the recipient, relationship, and stakes.

## 1. Gather voice evidence

Before drafting, review the user’s current writing guide in full, if one exists. You may also use a small set of recent emails that the user actually sent, provided there is a legitimate purpose and clear authorization to access them. Use only the minimum relevant examples, and do not carry unrelated personal or sensitive details into the draft.

Build a practical voice profile from the evidence:

- Typical greetings and sign-offs.
- Formality level, warmth, and relationship cues.
- Typical sentence and paragraph length.
- Vocabulary, contractions, directness, and recurring phrasing.
- Punctuation, capitalization, and formatting habits.
- Phrases, tones, clichés, or punctuation the user avoids.
- How the user makes requests, follows up, declines, apologizes, corrects mistakes, or handles uncertainty.
- Approved reusable facts, links, boilerplate, and standard replies.

Treat recent sent messages and recent user corrections as stronger evidence than old examples or generic style guidance. If evidence conflicts, ask which preference is current. If no voice evidence is available, use a clear, concise, warm-professional default and invite the user to share examples for future drafts.

## 2. Confirm the email brief

Identify the minimum information needed to send an accurate email:

1. Who is the recipient, and what is their relationship to the user?
2. What outcome should the email produce?
3. What facts, dates, names, links, attachments, decisions, or commitments must appear?
4. What level of warmth, firmness, or formality is appropriate?
5. Are there deadlines, sensitivities, approvals, or privacy boundaries?

Do not invent availability, pricing, decisions, promises, claims, opinions, emotional reactions, or background facts. Ask a focused question if a missing detail would materially alter the message. Do not ask questions that are unnecessary for a useful draft.

When using private communications or records, stay within the user’s authorized access boundary. Include only information relevant to the recipient and purpose. Omit sensitive personal details unless they are necessary, authorized, and appropriate to disclose.

## 3. Adapt voice without copying blindly

Voice is a pattern, not a rigid template. Match the user’s recognizable style while adapting to context:

- **Close colleagues or familiar contacts:** use the user’s normal concise, conversational pattern.
- **New, external, senior, or formal recipients:** retain the user’s character while adding enough context and care to prevent ambiguity.
- **Sensitive, corrective, or conflict situations:** be factual, respectful, and direct. Avoid defensive explanations, exaggerated praise, and unnecessary apologies.
- **Requests:** state the action, responsible person, and timing plainly.
- **Declines or boundaries:** give a clear answer, offer an alternative only when genuine, and avoid creating false hope.

Use approved standard wording, factual details, or links when they fit the situation. Do not reuse a canned response when it would be misleading, overly impersonal, or inconsistent with the recipient’s context.

## 4. Draft the smallest complete email

Write only what helps the recipient understand and act. A useful default structure is:

1. Greeting, if the user normally uses one.
2. The purpose, answer, or decision in the first sentence.
3. Essential context, request, decision, or next step.
4. A clear close and sign-off, if appropriate.

Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Put the request, decision, or deadline where it is easy to find. Use bullets only when they make actions, options, or logistics clearer.

Remove:

- Throat-clearing and narration about the drafting process.
- Generic compliments, repeated thanks, or empty reassurance.
- Filler such as “just wanted to,” “I hope you’re well,” or similar language unless it is both useful and characteristic of the user’s voice.
- Hedging that weakens a message when the user has made a clear decision.
- Extra detail that does not help the recipient act.

## 5. Audit voice, facts, and send-readiness

Review the draft line by line before presenting it. Check:

- Would the user plausibly write these exact words?
- Do the greeting, closing, punctuation, rhythm, and length match the available evidence?
- Is the tone appropriate for the recipient and stakes?
- Did the draft add an unsupported commitment, claim, opinion, emotion, or implication?
- Are names, roles, dates, links, attachments, and references accurate?
- Is the requested action, owner, and timing unmistakable?
- Does the message disclose only information appropriate for this recipient?
- Can any sentence be removed without losing meaning or usefulness?
- Does it avoid the user’s known stylistic anti-patterns?

If a required fact is uncertain, use a clearly marked placeholder or ask the smallest necessary question. Do not conceal uncertainty with vague language.

## Output format

Provide the final email as copy-ready text. If clarification is required, ask only the specific question needed to complete a safe, accurate draft. Do not add explanations after the email unless the user asks for alternatives, rationale, or a revision.


---
name: professional-social-post
description: Draft, revise, and audit professional social posts from notes, drafts, articles, transcripts, research, or a topic, emphasizing strong hooks, concrete and defensible claims, useful substance, targeted revision, and privacy-aware publishing.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a draft, an article, a transcript, a podcast, research findings, or a simple topic.

The goal is not to make an announcement sound enthusiastic. The goal is to make the right reader stop, understand a useful point, and have a reason to care. Write for a defined professional audience with low tolerance for fluff, generic inspiration, vague claims, and unsupported certainty.

This workflow is platform-independent. Before drafting, ask the user to choose or confirm:

- The platform and format: text post, caption, document carousel, thread, newsletter excerpt, or article promotion.
- The audience: for example, technical practitioners, founders, policy professionals, researchers, customers, partners, or job candidates.
- The purpose: share an insight, explain a concept, announce a change, promote a longer piece, start a substantive discussion, or support a campaign.
- The voice: formal or conversational, first-person or organizational, preferred terms, forbidden terms, punctuation preferences, and target length.
- Whether an external link is included, and the platform-specific plan for placing it.
- Any approved examples, writing guidance, brand requirements, or audience research.

If the user has an established voice guide or approved past posts, use it. Do not assume an individual’s voice, publishing process, performance data, or platform rules.

## Privacy, authorization, and scope

If source material includes private communications, internal records, client information, participant outcomes, employee information, or other information about identifiable people, confirm there is a legitimate purpose and clear authorization to use it publicly. Use only the minimum relevant sources and details.

Before naming a person, sharing a quote, describing a career change, or publishing a result that could identify someone, verify:

- The information is accurate and approved for the intended audience.
- The person has consented where consent is expected or required.
- The post does not expose unrelated personal, sensitive, or confidential details.
- The final output remains inside the appropriate access boundary.

If authorization, evidence, or consent is unclear, use an anonymized example, remove the detail, or ask a concise question. Do not turn an internal anecdote into public proof without permission.

## Routing and content types

Identify the content type before drafting. Some genres need a dedicated structure.

- **Career or participant case study:** A person’s starting point, turning point, and concrete outcome. Use a case-study structure: starting point, relevant intervention or decision, outcome, evidence, and lesson. Do not imply that a course, employer, or program caused an outcome unless the evidence supports that conclusion.
- **Research or evidence post:** A claim based on data, a model, a report, or an analysis. Prioritize methodology, assumptions, uncertainty, and a defensible interpretation.
- **Product or organizational announcement:** Lead with the concrete change and why it matters to readers. Do not lead with internal excitement.
- **Article, podcast, or report promotion:** Lead with the strongest finding from the piece, not with “new article” or “new episode.”
- **Carousel or document caption:** Give one or two meaningful findings, then point readers to the visual material. Do not repeat every slide.
- **Hiring or assessment post:** Describe role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Avoid broad judgments about people or language that treats candidates as categories rather than individuals.

If the genre is unclear, ask one short routing question before writing.

## Non-negotiable accuracy rules

1. **Do not invent facts.** Do not fabricate statistics, names, quotes, outcomes, clients, organizations, titles, dates, research findings, testimonials, or causal claims.
2. **Distinguish evidence from interpretation.** State what the source shows, then clearly label the conclusion, recommendation, or hypothesis.
3. **Preserve meaningful uncertainty.** If a result has wide ranges, weak evidence, important assumptions, or correlation rather than causation, say so plainly.
4. **Use exact supported details.** Specific figures, dates, roles, and outcomes are usually stronger than broad descriptions. Do not convert an estimate into falsely precise language.
5. **Ask for missing evidence early.** If the post depends on a claim the user cannot support, remove it, narrow it, qualify it, or request a source.
6. **Avoid misleading urgency.** Do not exaggerate stakes merely to create engagement. A sharp risk with a practical response is more credible than broad catastrophe language.
7. **Attribute fairly.** Credit collaborators, sources, and contributors when relevant and authorized. Do not overstate one person’s role in a group effort.

## Audience and voice

Write for the reader most likely to act on the post, not for everyone who might vaguely relate to it. Specificity is a filter: it helps the intended reader recognize that the post is for them.

Use this default voice unless the user provides a different one:

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
| Corporate | “We are thrilled to announce an exciting initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences full of unexplained terms. | State the claim plainly, then explain needed terms in ordinary language. |
| Alarmist | Broad catastrophe language without a mechanism or response. | Name the risk, evidence, uncertainty, and a proportionate intervention. |

## Core workflow

### 1. Inspect the source before choosing a format

Do not begin with a template. Read the source and find the strongest material inside it.

Look for:

- An unusual or surprising fact.
- A specific number that creates tension.
- A counterintuitive conclusion that can be defended.
- A concrete before-and-after outcome.
- A meaningful trade-off or deliberate constraint.
- A sharp disagreement between credible views.
- A useful framework, checklist, or model.
- A sentence that changes how a reader sees the problem.

The formal headline of an article is often not the best social-post angle. The strongest thread may be a detail in the middle of the source.

If several strong angles exist, do not silently choose one. Present two to four numbered options. For each, state what it foregrounds and why it may work for the audience.

> I see several viable post angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [specific story, outcome, or disagreement]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Choose one primary thread. A social post is not a summary of every point in the source.

### 2. Generate hooks before drafting the body

The opening determines whether the rest is read. Generate five to ten possible hooks, then show a shortlist of three to five when user choice would help. Do not commit to the first workable sentence.

A hook makes an honest promise that the body fulfills. It should work on its own without requiring the reader to know the source first.

Useful hook patterns:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Named outcome:** “[Person or role] moved from [starting point] to [specific outcome] in [timeframe].” Use only with approval and evidence.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only if the post defends it.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused question:** “Why do two credible groups reach different conclusions about [specific issue]?”

For each shortlisted hook, add a brief strategic note.

| Hook | Strategic purpose |
|---|---|
| “[Specific claim or finding].” | Leads with a concrete result and creates a reason to continue. |

Use the swap test: if a key topic word could be replaced with “marketing,” “leadership,” or another unrelated subject and the hook still works, it is too generic. Add a distinctive mechanism, result, audience problem, or constraint.

Avoid:

- Generic announcement openings such as “Excited to share.”
- Throat-clearing such as “In today’s fast-moving environment.”
- Empty cliffhangers that do not deliver a payoff.
- Multiple rhetorical questions in a row.
- Broad motivational claims.
- Clickbait such as “You will not believe” or “This changes everything.”

### 3. Choose one structure

Choose the structure that matches the source. Do not combine several structures unless there is a clear reason.

1. **Counterintuitive claim → evidence → implication**: Best for research, data, and argument posts.
2. **Changed mind → trigger → updated view → takeaway**: Best for thoughtful first-person posts.
3. **Problem → why it matters → practical response**: Best for explainers, policy, and operational content.
4. **Result → how it happened → reusable lesson**: Best for launches, team outcomes, and approved case studies.
5. **Framework → examples → application**: Best for posts readers may save and revisit.
6. **Specific announcement → reader relevance → next step**: Use when the announcement itself is genuinely notable.
7. **Strategic trade-off → rationale → consequence**: Use to explain a deliberate constraint or “anti-goal,” meaning something the organization intentionally does not optimize for.

### 4. Draft the body: hook, tension, payoff

Use this default shape:

- **Hook:** The strongest claim, result, or tension.
- **Tension or setup:** Why the point matters, what is surprising, or which assumption it challenges.
- **Payoff:** The evidence, story, framework, or practical insight. The post must be useful even if the reader never opens a link or swipes a carousel.
- **Soft close:** Exactly one focused question, one practical takeaway, or one clear pointer to more material.

A useful default is under 300 words, but length should follow substance and platform norms. Every additional paragraph should earn its place.

Use one- or two-sentence paragraphs so the post scans well on a phone. Use bullets only when the content is genuinely list-shaped, such as three findings, four reasons, or a checklist. Light formatting can clarify a key phrase, but do not rely on formatting methods the chosen platform does not support.

For a carousel or document caption:

- Establish the central idea in the caption.
- Include one or two strong specifics.
- State what the visual material adds.
- Do not create a slide-by-slide summary.

For a linked article, report, or podcast:

- Put the strongest finding in the post.
- Treat the linked item as depth, sources, methodology, or extended analysis.
- Follow the user’s platform strategy for link placement.
- Never make “read the link” the main value proposition.

## Calls to action and questions

Use one close only. A strong close gives the reader a real, bounded way to respond.

Good examples:

- “Which of these constraints matters most in your work?”
- “What evidence would change your view?”
- “The full analysis includes assumptions and source material.”
- “If you have operated this system, where does this model fail?”

Weak examples:

- “Thoughts?”
- “Let me know what you think.”
- Several questions at once.
- Requests to comment, tag, repost, or react solely to inflate engagement.

A question should invite knowledge, disagreement, or experience. Do not use engagement bait.

## Editing pass: remove templated and inflated language

Run a separate editing pass after drafting. Cut phrases that sound polished but say little.

Replace or remove:

- Corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Hedging frames such as “it is worth noting,” “one might say,” and “arguably,” unless uncertainty is genuinely important.
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Abstract nouns such as “journey,” “transformation,” and “paradigm” when a concrete event can be named.
- Transition sentences that merely repeat the previous paragraph.
- Dramatic frames such as “The truth is” or “Here is the reality.” State the point directly.
- Decorative punctuation or formatting that the selected platform will not render correctly.

Favor periods, commas, and line breaks over theatrical punctuation unless the user prefers otherwise. Read the draft aloud. If it sounds like a generic thought-leadership template rather than a person making a specific point, rewrite it.

## Revision protocol

When the user gives feedback, revise the requested line and nearby logic first. Do not rewrite the entire post unless asked.

- If the hook is not sharp enough, offer several replacement hooks before changing the body.
- If a claim feels overstated, tighten the evidence or soften only that claim.
- If a paragraph feels slow, cut setup before adding explanation.
- If the user prefers an earlier sentence, preserve it unless there is a clear reason to change it.
- If a source is weak, identify the gap honestly rather than hiding it with stronger-sounding language.

Multiple small options are often more useful than one complete redraft, especially for hooks, closers, and uncertain lines.

## Readiness gate and audit

Do not present a draft as final until it passes this checklist:

- Does the first line earn attention when read alone?
- Is the post about one clear point rather than competing ideas?
- Does it include a concrete detail, outcome, example, number, or mechanism where appropriate?
- Could a knowledgeable reader challenge the main claim, and could the author defend it with available evidence?
- Does it provide value without requiring a click, swipe, or purchase?
- Is uncertainty stated where it materially affects the conclusion?
- Is the language specific to this topic rather than reusable for any industry?
- Is the close one focused action, question, or pointer?
- Are all names, quotes, figures, and claims supported and approved for this audience?
- Has the post omitted unrelated personal or sensitive information?
- Does formatting work on the intended platform?
- Is the tone professional, respectful, non-inflammatory, and appropriate for the intended audience?

If any answer is no, revise before handoff.

## Handoff format

Present only what helps the user decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen delivery format or workspace.
3. Any unsupported claim, missing input, approval need, or line that remains uncertain.
4. Suggested link or first-comment text when relevant to the platform strategy.
5. A concise publishing reminder appropriate to the platform, such as responding promptly and substantively to genuine early comments.

Do not claim that a format, timing tactic, or metric will reliably improve reach. Platform behavior changes. Treat distribution guidance as a testable hypothesis and compare results across several posts.

## Common failure patterns

- **Announcement disguised as content:** The post says the organization is pleased but not why readers should care. Lead with the actual change or lesson.
- **Pure teaser:** The post asks readers to click but provides no useful insight. Share the main finding and use the linked piece for depth.
- **Unsupported precision:** The post uses a striking figure without source, scope, or caveat. Verify, qualify, or remove it.
- **Generic inspiration:** The post sounds positive but has no mechanism, example, or decision. Name the concrete action or trade-off.
- **Overpacked summary:** The post covers every section of a report. Select one thread and save the rest for the source or later posts.
- **Bolted-on promotion:** A course, product, or service appears at the end without a natural connection. Remove the pitch, create a separate promotional post, or make the connection concrete and immediate.
- **Forced engagement:** The post demands reactions or comments. Ask one real question or end with a useful conclusion.
- **Unapproved personal proof:** The post uses a person’s story, quote, or outcome without clear permission. Obtain approval, anonymize it, or omit it.

The final standard is simple: the post should sound like someone with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, or a generic social-media template.


---
name: case-study-post
description: Create an evidence-based case study post about a person’s career, learning, or professional change, with strong hooks, a concise draft, quote-card options, approvals, and a publication-ready review package.
---

# Write a case study post

Use this workflow to turn authorized raw material about a person into a concise, credible public case study. It works especially well for professional social posts, and can be adapted for newsletters, community updates, program-alumni stories, recruitment pages, or founder/customer stories.

The aim is not vague praise. Show a specific and evidence-backed change: where the person started, what they were considering, what prompted action, what concretely helped, what they do now, and what a relevant reader can do next.

A good case study makes the reader recognize their own uncertainty in the subject’s before-state. It names the intervention or community clearly, explains the mechanism without overstating causation, and earns credibility through detail rather than flattering adjectives.

## Purpose, authorization, and access boundaries

Use this workflow only for a legitimate communications purpose, such as publishing an approved success story, alumni profile, community update, or professional case study.

Before using interview notes, application forms, internal messages, direct messages, or other private records:

- Confirm that the person has consented to this use, or that the publisher has clear authority to use the material for the stated purpose.
- Use only the minimum relevant sources and details.
- Do not copy unrelated personal information into working notes or outputs.
- Treat internal messages as supporting evidence, not automatic permission to publish details from them.
- Respect the subject’s reasonable expectations about what is public, including names, employment details, compensation, health, family, immigration, legal issues, and unpublished work.
- Keep drafts, source excerpts, and approval notes within the access boundary chosen by the user.

If authorization, consent, or the publication boundary is unclear, pause and ask before drafting.

## Inputs

Ask for all available and authorized source material. Useful inputs include:

- An interview transcript and meeting notes
- An application, intake form, or written statement from the subject
- A current professional profile or approved biography
- Official public announcements, work samples, publications, projects, or portfolios
- An internal message celebrating a result, if it is appropriate to use
- A prior draft, outline, or notes from the subject
- The target audience, platform, desired length, and call to action
- An editorial or brand voice guide
- The intended document system or publishing workflow

Before drafting, determine whether enough information exists for the following fields.

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns if relevant, and publication consent status |
| Before-state | Previous role, field, goal, uncertainty, or constraint |
| Trigger | Why they joined, applied, changed direction, or acted at that time |
| Intervention | Program, community, product, mentor, event, or resource involved |
| Mechanism | Concrete help, such as a realization, opportunity, introduction, feedback session, or practical resource |
| Now-state | Current role, organization, team, project, output, or result |
| Timeline | Dates or time spans from starting point to outcome |
| Evidence | Verified roles, figures, dates, named work, and direct quotes |
| Cost or risk | A career tradeoff, move, uncertainty, or compensation change, if approved |
| CTA | What the reader should do next |

If critical facts are missing, ask focused questions before drafting. Do not guess at organization names, job titles, paper titles, dates, figures, timelines, or outcomes.

Useful questions include:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they join, apply, or make a change at that point?
4. What are the one or two concrete things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a specific project, publication, placement, product, grant, or result that can be named publicly?
8. Did they take on a meaningful cost or risk that they are comfortable sharing publicly?
9. Which names, figures, claims, and quotations have explicit approval for publication?
10. Who should this post persuade, reassure, or help?

## Evidence and verification rules

Never invent facts or upgrade a claim for dramatic effect. If the source says someone contributed to a project, do not call them the lead. If they explored an opportunity, do not say they received it. If their work is unpublished, do not call it published.

Automated transcripts are useful but fallible. They can mishear names, organizations, technical terms, figures, titles, and dates. Cross-check consequential transcript details against a stronger source, such as direct confirmation from the subject, an official announcement, published work, an approved profile, or a written application.

Use this default reliability order when sources conflict:

1. The subject’s direct and recent confirmation
2. Official public records, published work, or an employer’s approved announcement
3. A current professional profile
4. An original application or written statement from the subject
5. Interview transcript notes or automated summaries
6. Informal third-party messages

Keep three categories separate in working notes:

- **Verified fact:** A role, date, artifact, figure, or quote supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn from the story. Use it only when evidence supports it, and phrase it modestly.

Do not claim that a program, community, tool, or mentor caused the person’s entire outcome unless the evidence supports that conclusion. Prefer precise language such as “the program helped them see the field differently” or “they found the opportunity through the community.”

## Sensitive-content gate

Flag the following for explicit subject approval before publication:

- Salary, pay cuts, financial hardship, or compensation comparisons
- Health, family, immigration, legal, or personal circumstances
- Strong language about a past employer, role, or career decision
- Unreleased work, confidential projects, or unpublished titles
- Direct quotations, especially criticism or strong opinions
- Claims about why an employer hired the person
- Claims of causation or impact that cannot be independently verified
- Exact dates or timelines that could reveal private circumstances

If approval is unavailable, use an honest fallback only if it remains useful and approved. For example, replace a specific compensation figure with “they accepted a lower-paying role” only when that broader statement is permitted. Do not hide uncertainty by making the story more dramatic.

## Build the story beats

Create a concise private working outline before writing.

### 1. Before-state

Capture the subject’s relevant role, background, and uncertainty. Include what they were considering instead when that alternative resembles the reader’s current life.

Keep only details that move the story. A list of credentials, books read, or earlier jobs usually weakens the post. Keep a detail when it explains the decision or makes the change tangible.

### 2. Trigger

Identify why the person acted at that moment. They may have wanted to test whether a career path was open to them, learn a new field, find collaborators, solve a practical problem, or make a values-driven change.

### 3. Mechanism

Find one or two observable things that changed the trajectory. Strong mechanisms include:

- Realizing that a field or role was accessible
- Seeing a relevant opportunity in a community
- Having a conversation that clarified a next step
- Getting feedback that improved an application or project
- Receiving a specific introduction, workshop, or practical resource

Avoid “the experience was transformative.” State what actually happened.

### 4. Now-state

Record the current role, organization or team if approved, and what the person does in understandable terms. Translate technical language enough for the intended reader.

Use named outputs only when they add proof or interest. One meaningful project, publication, placement, product, or grant can do more work than a long credential list.

### 5. Timeline and compression

Map the sequence from the intervention to the current result. Calculate a short, truthful timeframe when it sharpens the story, such as “within six months” or “the following year.” Do not force a compressed timeline when the facts do not support it.

### 6. Quotes

Pull three to five verbatim candidate quotes. Favor lines that speak to the reader’s identity, uncertainty, or decision, rather than only celebrating the subject’s outcome.

Candidate categories:

1. **Discovery:** “I did not know this path was open to someone like me.”
2. **Mechanism:** “I found the opportunity through the community.”
3. **Conviction:** “I would make the same choice again.”

Light trimming is acceptable only when it preserves exact meaning and grammar. Do not rewrite a quote into something the subject did not say.

## Generate three hook options

For feed-based platforms, the first two lines determine whether someone keeps reading. Write three distinct hooks before drafting the body. Each should be two short sentences, usually under about 140 characters total where that fits the platform.

### Hook A: Discovery

Use this when the audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a surprising concrete mechanism.

This is the default recommendation when readers may think, “That could be me.”

### Hook B: Identity collision

Use this when the before-and-after contrast is vivid.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This often works for broader audiences that may not share the subject’s exact blocker.

### Hook C: Stakes-led

Use only when a meaningful cost or risk has explicit approval and the audience will read it as honest conviction rather than a warning.

**Formula:** The subject accepted a specific cost to do something. Now they are taking a concrete action or doing meaningful work.

Do not use a sacrifice hook if it suggests that participation requires hardship, or if it distracts from a more accessible message.

Choose one hook as the recommendation. Give one brief reason it best fits the target audience, and explain why the other two are less suitable.

## Draft the post

Aim for roughly 160 to 220 words unless the platform or audience calls for another length. Shorter is usually stronger.

Use this structure:

1. **Hook:** Use the recommended hook.
2. **Before-state:** One short paragraph showing the previous situation and a relevant alternative path.
3. **Name the intervention:** Clearly state that the person joined the program, used the resource, or entered the community. Do not leave its role implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then land the immediate result in plain language.
5. **Current work:** Describe what they do now and why it matters in terms the reader can understand.
6. **Optional honest cost:** Include only if approved and genuinely useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already carried by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

Where a platform may reduce distribution for external links in the body, use a comment, profile destination, or other designated link location instead. Treat this as a platform-specific publishing choice, not a universal rule.

## Style rules

Adapt to the chosen brand voice. If no guide exists, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use concrete names, roles, dates, and figures only when verified and approved.
- Use the subject’s first name after the initial full introduction when this fits the publication’s tone and consent.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not call someone exceptional, inspiring, or brilliant without showing relevant evidence.
- Use contractions if the voice is conversational.
- Keep the CTA in full second person: “If you are…” and “you can…”
- Avoid emojis unless they are an explicit brand choice.
- Avoid em dashes by default. Use periods, commas, or line breaks.

On the final pass, remove machine-like phrasing: empty transitions, dramatic setup frames, filler intensifiers, hedge words, abstract nouns that replace evidence, balanced “on one hand/on the other hand” constructions, and reflective summaries after the CTA.

Avoid language such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm” unless it is necessary in a direct quote.

Read the post aloud. If it sounds like a generic thought-leadership template, shorten it and replace abstractions with facts.

## Graphic quote options

Provide three options for a visual quote card. Each should be self-contained, preferably under 15 words, and verbatim from approved source material.

Offer one quote from each category:

- Discovery
- Mechanism
- Conviction

Recommend one quote with a one-sentence rationale. Discovery quotes are often strongest because they work without context and reflect the reader’s possible uncertainty. Choose a mechanism or conviction quote only when it is clearer and more memorable on its own.

## Readiness audit

Before sending the draft for review, check:

- Is every name, role, date, figure, title, and outcome verified?
- Were important transcript-derived details cross-checked?
- Is the source use authorized and within the intended access boundary?
- Does the post show a concrete mechanism rather than only a result?
- Does it avoid overstating causation?
- Is the intervention named clearly?
- Does the opening mirror a real audience concern?
- Is the current work understandable to a non-specialist reader?
- Have sensitive claims and direct quotes been flagged for approval?
- Is the CTA clear and directed at the intended reader?
- Are there no unsupported superlatives, corporate phrases, generic filler, or unnecessary em dashes?

## Delivery and iteration

Create the draft in the user’s chosen document system when available. Use a clear title format such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and the two alternatives
- The three graphic quote options and recommendation
- A list of approval items
- A list of missing information that would strengthen the post
- The document location or link, if applicable

Do not treat the first draft as final. If feedback says “make the hook better,” generate new hooks rather than making tiny edits. If asked to make it shorter, cut secondary biography first while preserving the mechanism and outcome. If a subject rejects a sensitive line, replace it with an approved fallback without weakening the entire story.

After a final version is accepted, review feedback for reusable lessons. Update the workflow only when a recurring pattern is clear, such as a missing intake question, a consistent voice preference, or a repeated verification issue. Do not invent process changes after a clean review cycle.


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
description: Review authorized meeting records to identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date range, or for a manually supplied list of meetings.

The goal is not to turn every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose, authorization, and operating rules

Use this workflow only for a legitimate work purpose and with clear authorization to access the meeting records and task system. Read only the minimum sources needed to establish ownership, commitment, timing, and relevant context. Do not copy unrelated personal details, sensitive discussion, or private participant information into tasks. Keep task notes and reports within the access boundary appropriate for the source records.

Before each run, apply these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels it as an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work that was completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, statement of interest, or open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply known responsibility and delegation boundaries supplied by the user or organization. Attending a meeting does not make the user accountable for all work in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this broadly useful default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect:

- Title, date, and time.
- Meeting-record link or identifier.
- Attendees, if available and relevant.
- Transcript, notes, summary, and relevant linked context.

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
- A request followed by explicit acceptance.

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

- Relationship context and why the meeting occurred.
- Candidate actions owned by the user.
- Work completed during the meeting.
- Work delegated to another named owner.
- Explicit future commitments and timing.
- Enough neutral context for a task to remain understandable weeks later.
- Source and related links that are appropriate to include.

Create no task when work was completed live, another person owns it, the meeting was purely informational and any needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

## 4. Decide the task shape

Combine actions into one task when they have the same counterparty, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect months later.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

This is a readiness gate: do not proceed to task creation until every proposed task has a clear owner, unfinished outcome, sensible shape, and enough context to stand alone.

## 5. Write the task

Use the user’s chosen task system and field names. At minimum, capture:

- **Title:** Short, verb-led, and specific, such as “Follow up with prospective partner about pilot scope.”
- **Status:** The standard open status.
- **Due date:** Based on an explicit commitment whenever possible.
- **Priority:** Use the user’s scale; default to normal important work and reserve the highest level for a real deadline, material risk, or waiting counterparty.
- **Time estimate:** Realistic minutes.
- **Notes:** Context, action checklist, communication drafts, and relevant links.

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
- Each task links to its source record when appropriate.
- Message drafts are ready to send and follow the user’s preferences.
- Every uncertain item is either asked as a specific question or explicitly deferred.
- The output contains no unnecessary sensitive or unrelated personal details.

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
description: Create or improve a short, paid, asynchronous work sample that produces role-relevant evidence, is practical to review, and is validated through simulated submissions.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A good work sample asks a candidate to complete a realistic, bounded version of the job. It produces role-relevant evidence that is difficult to imitate through polished generalities alone, while remaining fair, self-contained, and quick enough to assess consistently.

This workflow is for a paid take-home work sample, usually expected to take two to four hours and completed asynchronously between early screening and interviews. Do not use it for an interview question, an application-form screening question, or a multi-day work trial. If the requested format is unclear, ask once which format is needed.

## Purpose and design principles

A work sample should answer a narrow question: can this candidate demonstrate the few capabilities that matter most in this role under realistic constraints?

It should not attempt to assess the whole person or every requirement of the job. Other stages may be better suited to assess different evidence:

- Interviews can assess live communication, motivation, collaboration, and conversational reasoning.
- References can assess reliability, integrity, and sustained performance over time.
- A later work trial can assess consistency, judgment across days, and work in real systems.
- Onboarding can often teach a specific tool, internal process, or domain vocabulary.

Focus the work sample on three to five load-bearing capabilities that are important to the role and observable within the allotted time. Common examples include prioritization, practical judgment, clear writing, diagnosis, execution, sourcing, systems thinking, decision-making under uncertainty, and turning ambiguity into useful work.

Use these default constraints unless the hiring owner chooses otherwise:

- Make the work sample paid.
- Set a clear time expectation, commonly three hours.
- Use a realistic but fictionalized, anonymized, or approved public scenario.
- Do not ask candidates to create production work the organization will use unless that use is separately agreed.
- Design for roughly 20 to 25 minutes of reviewer time per submission.
- Make the exercise self-contained. Candidates should not need internal tools, private records, unavailable systems, or private contact lists.
- State whether AI tools are permitted. Evaluate judgment and usefulness, not attempts to detect AI from writing style.
- Test capabilities materially related to the role. Do not use protected characteristics, personal background, or unrelated proxies as criteria.
- Offer a route for reasonable accommodations or an equivalent accessible format while preserving the role-relevant standard.

If the work sample uses organizational records, communications, or examples involving people, confirm there is a legitimate hiring purpose and clear authorization to use them. Use only the minimum relevant material. Remove unrelated personal, confidential, or sensitive details. Keep drafts, simulations, reviewer guidance, and candidate submissions within the approved hiring access boundary.

## Step 1: Pre-flight

Do not begin drafting until the hiring team has both:

1. A current job description or role brief that explains responsibilities, level, expected outcomes, reporting context, and important constraints.
2. A role-success profile, hiring plan, or equivalent document that identifies the capabilities and experience needed to achieve those outcomes.

The role-success profile may be called an ideal-candidate profile internally, but it should describe role-relevant evidence and capabilities rather than demographic, identity, or personal-style assumptions.

If either document is missing, stop and ask for it. Do not try to discover the role-success profile while designing the exercise. That creates a moving target and commonly produces a plausible-looking test that measures the wrong things.

Use this request format:

> Before we design the work sample, I need the job description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

Once both exist, read the full relevant role context. This may include linked hiring notes, team constraints, examples of strong work, previous assessment feedback, and existing exercises for comparable roles. Read one or two reference exercises to calibrate tone, length, and delivery format. Do not copy their task shape automatically. Different roles need different evidence.

Give a brief status update after review, for example:

> Read the role brief, role-success profile, and two comparable work samples. Moving to the alignment memo.

## Step 2: Write an alignment memo before drafting

Do not write candidate-facing instructions yet. First produce a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five capabilities that the role succeeds or fails on and that a short asynchronous exercise can reveal. Phrase these as observable behaviors, not abstract virtues.

Weak:

> Strategic thinking.

Better:

> Identifies the highest-leverage problem in a messy operating situation, explains the tradeoff, and delivers a useful first action.

A capability belongs here only if it is important to the role, can be surfaced within the exercise window, and can be reviewed with reasonable consistency.

### What the work sample will not test

Name important criteria that should be assessed elsewhere. This keeps the exercise honest and prevents it from becoming an unrealistic substitute for the whole job.

For example, a short written exercise may not fairly assess long-term reliability, leadership over months, live responsiveness, specialized software fluency, or collaboration in meetings.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level. Explain what that changes in the exercise.

- Entry-level candidates may need more context and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make explicit tradeoffs, establish direction, and create an artifact a teammate could use without further explanation.

Role level should affect the expected independence and judgment, not create unnecessary complexity or ambiguity.

### Failure modes the exercise should catch

Identify two or three plausible work patterns that could otherwise look strong in a conventional process but would create problems in this role. Describe observable behavior rather than making broad judgments about people.

Examples include:

- A polished planner who does not produce usable work.
- A fast executor who misses the central problem or creates avoidable risk.
- A careful candidate who defers every meaningful decision instead of making reasonable assumptions.
- A technically capable candidate whose work does not serve the intended audience.

### What strong looks like

Write one concise paragraph describing a top submission. Focus on evidence: what it notices, what choices it makes, what it delivers, and how it handles uncertainty.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and role-alignment risks you want this work sample to assess?

Do not proceed until the owner explicitly confirms or revises the memo.

## Step 3: Propose exercise shapes

Once the alignment memo is approved, propose three possible exercise shapes. Each must test the confirmed capabilities in a meaningfully different way, be understandable within about one minute, be self-contained, and be scorable within the review-time budget.

For each option, include:

- **Shape:** A plain-language description of the task.
- **What it tests:** The specific load-bearing capabilities it reveals.
- **Why it is evaluable:** The evidence reviewers will see and why it can be assessed consistently.
- **Main risk:** The most likely source of noise, unfairness, or weak signal.

Keep each option concise, usually no more than about 150 words.

Useful shapes include:

- **Crisis inbox or triage pile:** The candidate receives a realistic set of messages, requests, and constraints. They prioritize, draft responses or work products, and recommend one systemic improvement. This can suit operations, coordination, support, and communications-heavy roles.
- **Choose the highest-leverage action and ship it:** The candidate receives a brief with several possible priorities, chooses one, explains the choice, and creates a small usable output. This can suit strategic operations and builder roles.
- **Diagnose and ship one fix:** The candidate reviews a messy situation, identifies the key problem, and creates one targeted intervention. This can suit product, program, analytical, and process-imvement roles.
- **Source and pitch:** The candidate defines a target profile, identifies promising channels or prospects using provided material, and writes outreach. This can suit recruiting, partnerships, sales, or community-growth roles.
- **Decision-useful analysis:** The candidate assesses an intervention area using supplied evidence and makes a recommendation for a decision-maker. This can suit research, policy, strategy, and specialist roles.
- **Design a repeatable system:** The candidate creates a lightweight process, playbook, or operating artifact that another teammate could use. This can suit program, enablement, community, and operational-design roles.

Do not draft the full exercise until the hiring owner picks a shape. If none fits, generate three additional options based on the confirmed memo rather than forcing a familiar format.

## Step 4: Draft version 1

Write the candidate-facing exercise in the following order. Adapt the number of deliverables and the amount of context to the role, but preserve the basic structure.

```markdown
# [Role] Work Sample

This work sample assesses your ability to [two or three observable capability verbs].

You have **[time limit]** total.

**Your mission**

[Describe a specific situation, not an abstract assignment. Include enough authority, operational context, and stakeholder availability to make decisions meaningful. If decisiveness is being tested, state that relevant stakeholders are unavailable during the exercise. End by restating what the candidate will produce.]

**Deliverables**

[Two to four substantive parts, with rough time guidance where useful. Include a short analysis or prioritization component, actual shipped drafts or outputs where relevant, and a reusable improvement or artifact when that maps to the role.]

**Context**

[Provide the minimum scenario information needed: audience, project state, constraints, policies, available resources, and stakeholder availability.]

**Instructions**

- Spend **[time limit]** completing this work sample.
- Submit within **[deadline]** of receiving the exercise.
- Submit a single [document or PDF] covering your work. If you create supplementary materials, include accessible links.
- **This is a paid work sample.** [State payment amount, payment process, and any early-submission bonus clearly.]
- [State the AI policy.]
- Briefly document material assumptions or uncertainty.
- If you do not finish in the expected time, submit what you have and explain what you would do next.
- [Optional: invite a short, informal walkthrough video if it would create useful signal.]

**Anticipated questions**

- *I am unclear about a requirement. What should I do?* Make a reasonable assumption, state it briefly, and continue.
- *What if I do not finish in the expected time?* Submit what you have, even if incomplete. Include a brief note on where you got to and what you would do next.
- *How will my work be used?* It will be used only to evaluate candidates for this position unless another use is agreed separately.
```

A common operations shape is one short prioritization or analysis section, five to seven substantive drafts or decisions, and one systemic improvement. Avoid dozens of micro-decisions. A few substantial outputs produce better evidence and are easier to evaluate.

If planning and execution both matter, explicitly warn candidates not to spend the whole exercise planning. Do not use high word-count targets that reward padding. A target such as “about 400 to 500 words, shorter if sharp” is often more useful than a broad range.

For a triage-pile exercise, include roughly eight to ten realistic items. Several items should connect so that seeing the whole situation is rewarded. Include reference notes with any policy or data needed to make fair decisions, such as escalation rules, capacity limits, or refund guidance.

Use fictional names and fictional contact details for invented scenarios. Do not include real-looking personal contact details. If the organization chooses to use real public information, confirm that it is accurate, necessary, authorized, and appropriate for candidate access.

Use a transparent AI policy. For example:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

### Candidate-facing format and style checks

Write in direct, plain English appropriate to the organization and candidate audience. Before sharing each draft, check that it:

- Uses simple headings and bullets that work in the chosen applicant-tracking system or document format.
- Avoids tables and horizontal dividers when the destination system renders them poorly.
- Avoids generic AI-sounding slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.
- Uses complete phrasing such as “by the end of Tuesday,” not abbreviated wording.
- Uses consistent regional spelling appropriate to the hiring organization.
- Formats multi-line message metadata clearly. If the destination editor collapses line breaks, use its supported soft-break method.
- Contains no credentials, private links, confidential operational data, irrelevant personal information, or sensitive records.

After every full draft, add a separate section:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets on choices the owner may want to change. Examples include whether an item is too obvious, whether a scenario detail is realistic enough, whether payment matches the role level, whether a deliverable is too prescriptive, or whether an optional video would add signal.

End with one focused decision question, such as:

> Which part should we tighten first?

## Step 5: Iterate with the hiring owner

Expect several rounds of feedback. For each revision, provide the complete updated work sample rather than only a change list, so the owner can copy it into the selected system.

Apply feedback directly unless it would materially undermine role relevance, assessment validity, fairness, privacy, or safety. If that happens, state the concern once in plain language, propose an alternative, and let the hiring owner decide.

Typical revisions include tightening vague instructions, loosening over-prescriptive tasks, correcting scenario facts, simplifying deliverables, changing payment, improving accessibility, and replacing unrealistic details.

## Step 6: Simulate two candidate submissions

Before declaring version 1 complete, simulate two full submissions in parallel using the exact candidate-facing instructions. Keep simulations fictional and do not base them on identifiable applicants or private personnel records.

### Role-aligned simulation

Use a persona that matches the confirmed role-success profile. Have the persona complete the actual deliverables within the stated time limit, followed by a short reflection on key choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest, capable persona who could pass ordinary screening but whose work lacks one role-critical capability. The mismatch must be tied to job evidence, never identity, background, disability, or protected characteristics.

Examples include a person who plans thoroughly when the role needs practical shipping, a person who avoids justified decisions when the role needs decisive judgment, or a person who executes individual tasks well but misses cross-task patterns.

Have this persona create the same submission shape.

Then write a synthesis covering:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both simulations performed similarly.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by likely impact.

Floor checks that both personas pass are not automatically a problem. The problem is when a central capability produces no meaningful difference in evidence.

## Step 7: Apply validation improvements

Revise the full exercise based on the simulations. Target the weakest diagnostic points first.

Useful improvements may include:

- Making scenario items more connected.
- Removing obvious noise that takes seconds to dismiss.
- Adding a concrete constraint that forces an important tradeoff.
- Replacing a broad opinion prompt with a usable deliverable.
- Clarifying reviewer expectations so they reward the intended behavior.
- Removing specialized knowledge requirements that are trainable and not essential at the point of hire.

Do not make the task harder merely to distinguish candidates more aggressively. Make it more diagnostic of the confirmed role-relevant capabilities.

## Step 8: Optional external review

If additional reviewers provide feedback, assess each suggestion against the approved alignment memo. State which suggestions to integrate, which to skip, and why. External feedback is input, not an automatic instruction. The hiring owner remains accountable for the final assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The job description and role-success profile are confirmed.
- The alignment memo is approved.
- The chosen task shape maps directly to load-bearing capabilities.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and does not require unauthorized private access.
- Payment, deadline, AI policy, and submission instructions are clear.
- The exercise provides an accommodations route or equivalent accessible format.
- Candidate-facing text works in the chosen delivery system.
- A reviewer can assess a submission in about 20 to 25 minutes.
- Role-aligned and plausible role-misaligned simulations have been completed.
- Simulation findings led to any needed revisions.
- The final version contains no unnecessary sensitive information and does not request unpaid production work.
- The assessment uses role-relevant criteria and avoids unrelated proxy measures.

## Common failure modes

Avoid these patterns:

- Designing the exercise before agreeing what it should measure.
- Testing tool familiarity, domain trivia, or trainable knowledge instead of durable judgment.
- Asking for too many small outputs instead of a few meaningful ones.
- Making every scenario item independent, which tests volume but not pattern recognition.
- Allowing candidates to defer every decision to an available stakeholder when decisiveness is meant to matter.
- Providing too little context and thereby rewarding insider knowledge.
- Setting word-count guidance that encourages padding.
- Creating a test that takes longer to grade than the evidence justifies.
- Treating polished presentation as the primary signal when the role requires something else.
- Using real internal details where a fictionalized scenario would provide equivalent evidence.
- Declaring the assessment successful without checking whether it distinguishes relevant performance.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, appropriately compensated, clear about what is being assessed, and useful for making a hiring decision.


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
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and privacy, verifying rendered state, and separating preparation from consequential actions.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing rendered forms, changing settings, collecting permitted data, testing a user flow, or working in an authenticated dashboard. Use it when a simple page retrieval or authorized direct interface cannot reliably complete the task.

> **Core rule:** Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until the account, target, page state, and authorization are clear.

A successful automation command is not proof that a website accepted a change. Modern applications may store state separately from the displayed DOM, commit a field only when focus changes, replace elements during rendering, or show a misleading error after an action has completed.

## 1. Choose the least invasive authorized route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface. It is usually more reliable and auditable than reproducing browser actions.
2. **Headless browser automation.** Use this for public pages, test environments, screenshots, rendered-page extraction, and tasks that do not require an established signed-in identity.
3. **User-visible authenticated session.** Use this only when the task genuinely requires an existing session, account-specific state, single sign-on, or a user-directed browser context.

Before driving a browser, check whether an authorized direct route exists. Review official documentation, normal form actions, page source, and visible network behavior for supported endpoints. Do not use an undocumented route to bypass access controls, consent boundaries, service restrictions, or other protections.

Do not use a live authenticated session merely because it is convenient. It may interrupt the user's work, expose private information, or create a risk of changing the wrong account. If a site blocks automated access, do not try to defeat the block for routine research or collection. A visible session can be appropriate only for a legitimate, explicitly requested task on that site when the user has authorized access and the established session is necessary.

Never weaken browser security, authentication, warnings, anti-abuse controls, or access restrictions to make a task easier.

## 2. Establish authorization, privacy, and account context

When accessing private communications, records, account dashboards, or information about people, first confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into logs, screenshots, notes, or reports. Keep outputs within the requester's appropriate access boundary and respect consent and privacy expectations.

Before changing anything in an authenticated context, identify:

- The intended account, organization, workspace, or environment.
- The target record, setting, form, or transaction.
- The type of context, such as personal, work, test, staging, or production.
- Whether the requester has authority to make the change.

Do not infer identity from a window title, an old tab, a browser connection label, or a remembered default. Select the profile or connection explicitly, then verify the signed-in account through a reliable account indicator before opening or changing the real target.

For visible-browser work:

- Announce that you are taking control and state the task purpose.
- Use a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Do not expose credentials, session tokens, recovery data, or unnecessary account details in output.
- Do not interact with security prompts, multi-factor challenges, security keys, or bot checks as though they were ordinary automation obstacles. Ask the authorized user to complete them when needed, then resume from a verified state.

Use a pre-action account gate for changes. Confirm: **Which account is active? Which environment is active? What exact item will change?** If any answer remains uncertain, stop and resolve it before acting. If the automation system uses a verification marker or permission gate, mark it only after the account check has actually passed.

## 3. Define the task boundary and final-action authority

Before navigating deeply, identify the requested outcome and the minimum information needed to achieve it. Determine:

- What page, record, setting, or workflow is in scope.
- What information will be entered, collected, changed, or uploaded.
- What choices require the user's judgment.
- Whether the action is reversible.
- Whether it sends, publishes, pays, deletes, grants access, changes ownership, or creates another external commitment.

Separate **preparation** from **commitment**. Drafting, filling fields, selecting options, and producing a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, or changing access may not be.

For consequential actions, use two phases:

1. **Preparation pass:** fill or configure the page, verify the state, and capture a suitable pre-action record. Do not activate the final control.
2. **Commitment pass:** re-check the account, target, readiness gate, and authority; then perform the final action once.

If the user has already clearly authorized the specific final action, and no material ambiguity or new consequence appeared, do not ask again solely because the workflow has two phases. If authority is missing, prepare and verify the result, then ask only for approval to take the final action.

If the page reloads, re-renders, or the session changes between phases, do not trust the earlier state. Inspect and verify again.

## 4. Inspect the rendered page before editing

Do not begin by guessing selectors, using a field's position in the DOM, or trusting a visual approximation. Inspect the rendered page first.

For each relevant control, determine:

- Its type: single-line input, text area, rich-text editor, dropdown, checkbox, radio group, date control, upload control, or custom widget.
- Its stable semantic identity: visible label, accessible name, placeholder, or explicit label relationship.
- Its current value, required state, disabled state, and visible validation rules.
- Whether it is the true editable control, a wrapper, or a hidden synchronization element.
- Whether changing it can refresh the page or reset dependent fields.

Address controls by label or another stable semantic identity whenever possible. Do not use numerical DOM indexes if a meaningful label exists, because dynamic pages can change order after loading or rendering.

Before editing an existing record or setting, inspect its current state. This helps avoid overwriting the wrong item or replacing data unintentionally.

### Generic inspection pattern

Use the selected browser capability to list controls and record enough detail to identify them safely. The implementation is tool-dependent, but the inspection should include tag, type, role, label, required state, and readable value or text length.

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

## 5. Match the interaction to the control type

A generic “set value” operation is not reliable for every web control. Use normal user-like interaction where application-managed state requires it.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Enter text through the standard input method | Line breaks or excess characters may be removed. |
| Multiline text area | Fill text, then move focus away | The value may commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select existing content, enter text through keyboard-style events, then blur | Direct DOM writes may not update internal state. |
| Dropdown, combobox, checkbox, or radio group | Read current state, change only if needed, and wait for the page to settle | The change may re-render the form or alter dependent fields. |
| Date/time widget | Set the value and verify the displayed summary after closing the widget | Typing or closing behavior may clear or reinterpret values. |
| File upload | Confirm the file, recipient, destination, and privacy effect before choosing it | Uploading can begin immediately or be hard to undo. |

For framework-managed editors, a reliable general sequence is: focus the actual editable element, select the existing content, remove it, enter replacement text through keyboard-style events, move focus to a neutral page element, wait briefly, and read the result back.

Some forms include a visible editor plus a hidden input. Changing the hidden input may look successful in a DOM inspection while validation still considers the visible editor empty. Target the control the user interacts with and that the application reads. If an accessibility locator returns a wrapper rather than an editor, inspect its labeled descendants and locate the real editable element.

If a selection, date, tab, or option can trigger a re-render, make and verify that change before entering long or complex text. Then re-inspect and confirm that earlier values remain intact.

## 6. Verify each meaningful change

After filling a field or changing a setting, read the value back from the rendered page. Compare it with the intended value. For sensitive content, verify length, required state, or a minimal redacted summary instead of reproducing the full content in logs.

Check specifically for:

- A command reporting success while the field remains empty.
- Missing line breaks, spaces, punctuation, or special characters.
- Truncation from a single-line control or length limit.
- Text that appears briefly but is lost after another interaction.
- A later re-render erasing an earlier entry.
- A visible label that points to a wrapper while a different element holds the real value.
- A dependent change to recipients, dates, options, attachments, or validation requirements.

When verification fails, stop moving toward submission. Identify the actual control type, retry once with a more suitable method, and verify again. If the page still changes or rejects the value, report the limitation and ask how to proceed rather than silently submitting incorrect information.

For complex rendered pages, use a robust direct automation library or an authorized interface rather than repeatedly issuing blind commands through an unstable tool. If a session becomes unreliable, restart with a suitable method and repeat inspection; do not try to rescue an uncertain state.

## 7. Apply a pre-submit readiness gate

Before a final submission or high-impact change, inspect the relevant page state again. Confirm:

- The correct account, organization, and environment are active.
- The target item is the intended one.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Recipients, dates, attachments, options, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **do not submit**. A partially prepared form can be corrected; an incorrect external action may be difficult or impossible to reverse.

Capture a pre-action record for consequential work: a screenshot, concise state summary, or structured field dump. Store and share it only through an appropriate access boundary. Do not paste extensive sensitive field contents into a chat report when a short summary and secure record are sufficient.

### Readiness checklist

- [ ] Account, environment, and target are verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields and validation state are clear.
- [ ] Dependent choices, dates, recipients, and attachments were checked.
- [ ] A suitable pre-action record exists for consequential work.
- [ ] The final action and its impact are understood.

## 8. Confirm completion and handle uncertainty safely

A final click is not proof of completion. After acting, seek reliable evidence such as a confirmation message, receipt, new record, persisted setting, sent item, published result, or changed status that remains after a safe refresh.

If the site reports an error or the action times out, inspect the resulting state before retrying. Some errors are cosmetic, while a blind retry can create duplicates, repeated messages, duplicate payments, or conflicting records.

If completion cannot be verified, report what was attempted, the evidence available, and what remains uncertain. Never describe an attempted action as complete without confirmation.

## 9. Failure patterns and recovery rules

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation says a field was filled, but it is blank | The application ignored a direct value update | Use focus-and-keyboard interaction, blur, and read back. |
| Earlier entries disappear after a later edit | A re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses formatting or characters | The control type or formatting rule differs from expectation | Find the correct multiline/editor control or use an acceptable simplified format. |
| A locator identifies an empty wrapper | The accessible element is not editable | Inspect labeled descendants and target the true editor. |
| Validation says a visible-looking field is empty | A hidden or non-authoritative element was edited | Use the visible interactive control the application actually reads. |
| A selection or date edit changes other values | The page refreshed or the widget has dependent state | Make it earlier in the sequence and re-verify all affected fields. |
| Browser automation becomes unreliable | The tool is unsuitable for the page | Switch to a more robust authorized method and restart from inspection. |
| Headless and visible browsers behave differently | The site varies by browser context | Prefer an authorized direct route; use a verified visible session only for the explicit task, without evasion. |
| An error appears after an action | The action may have succeeded despite the message | Inspect the resulting state before retrying. |
| Account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable identity indicator, and ask if uncertainty remains. |

## 10. Maintain the workflow responsibly

After a genuine failure or a broadly useful new pattern, improve the reusable procedure with a concise description of the symptom, likely cause, and safe fix. Do not retain personal account history, private content, or unnecessary details about a particular incident. Review assumptions when browser capabilities, automation libraries, routing methods, or site behavior change, and remove stale instructions instead of accumulating narrow exceptions.

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
- [ ] Final-action authority was confirmed when needed.
- [ ] Completion was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session information, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, revise an existing skill, assess whether it improves results, or improve its activation description. A skill is a focused set of instructions, optional resources, and quality checks that help an AI perform a recurring job reliably.

The central loop is:

1. Understand the intended job and its boundaries.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Review outputs with a person and use objective checks where appropriate.
5. Improve the skill using evidence rather than guesswork.
6. Repeat until the skill is useful, reliable, and not narrowly tuned to a few examples.
7. Optionally improve the description that determines when the skill is selected.

Do not force every project through every stage. Some users want a quick collaborative draft; others need a careful comparison and review cycle. First determine where the user is, then help them take the next useful step.

## Communication principles

Match the user’s familiarity with technical language. Use plain English by default. Terms such as *evaluation* and *benchmark* are often understandable, but briefly define them if helpful. Do not introduce terms such as “schema,” “assertion,” or “JSON” without explanation unless the user is already using them comfortably.

Explain why a question matters. For example, instead of asking only “What is the output format?”, ask: “What should a successful result look like: a chat response, a structured report, a file, or an approved action? This determines how we test completion.”

Keep the user involved in important choices:

- Confirm the purpose before writing extensive instructions.
- Ask before adding restrictive scope, required capabilities, or approval rules.
- Show proposed test cases before treating them as the evaluation set.
- Let human judgment lead when quality is subjective, such as writing style, design, tone, usefulness, or strategy.
- State uncertainty rather than implying that an unverified decision is certain.

If the skill uses private communications, records, or information about people, require a legitimate purpose and clear authorization. Use only the minimum relevant information and sources. Exclude unrelated personal details, respect consent and privacy expectations, and keep outputs within the appropriate access boundary.

## 1. Identify the starting point

Determine which of these situations best describes the request.

### New skill

The user has an idea for recurring work, such as preparing project updates, reviewing a class of documents, transforming data, or guiding a standardized process. Start with discovery, scope, and a first draft.

### Existing skill

The user has an existing instruction set and wants it edited, simplified, tested, or improved. Read it before proposing changes. Preserve its established name and identity unless the user asks to change them.

When an existing skill is available only in a location that cannot be edited, make a working copy in a user-approved writable location. Keep the original unchanged until the user approves the revised version.

### Workflow demonstrated in the conversation

The user may say, “Turn what we just did into a skill.” Extract what is already known from the conversation before asking broad questions:

- Inputs, files, and information sources used.
- The sequence of decisions and actions.
- Tools or capabilities needed.
- Corrections and preferences the user gave.
- Output format and evidence of success.
- Conditions that caused the workflow to take a different path.

Summarize the inferred workflow, identify the gaps, and ask the user to confirm it. Do not convert a one-time workaround into a general rule without checking whether it applies to future cases.

### Evaluation or optimization request

The user may have a finished-looking skill and ask whether it works. Start with test design, comparison, and review. Do not rewrite a skill merely because a rewrite is possible; use evidence to identify what needs improvement.

## 2. Capture intent and boundaries

Gather enough information to define a coherent job. Adapt these questions to the user’s situation rather than asking all of them mechanically.

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What requests, wording, or situations should cause the skill to be used?
3. **Inputs:** What information, files, references, systems, or permissions may it use?
4. **Outputs:** What should it produce, change, or communicate? Is there a required format?
5. **Success:** How will the user know the output is correct, useful, or ready?
6. **Boundaries:** What should it not do? When should it ask for clarification, request approval, decline, or hand work back to the user?
7. **Variation:** What common cases, difficult cases, and exceptions materially change the work?
8. **Dependencies:** Are particular capabilities, templates, references, or scripts required?
9. **Testing:** Should the skill be tested with realistic example requests before release?

Offer useful choices when they expose a decision clearly:

- “When information is missing, should the skill make a low-risk best effort or pause and ask?”
- “Should it produce a brief summary, a detailed report, or let the user choose?”
- “Should it use any available source, or only sources explicitly approved by the user?”
- “Which actions require confirmation because they are external, irreversible, costly, or high impact?”

Recommend test cases when outputs can be objectively checked, the work is consequential, the process is repeatable, or the skill will be used by more than one person. For highly subjective work, recommend representative examples and human review rather than pretending that a simple score captures quality.

## 3. Research and inspect available resources

Before drafting, inspect relevant user-approved material when it would reduce uncertainty or improve the result. This may include existing instructions, templates, documentation, examples, output standards, or comparable skills.

Use research to identify:

- Existing conventions and required output formats.
- Constraints imposed by a file type, system, or workflow.
- Reusable patterns for similar jobs.
- Safety, privacy, compliance, approval, or retention requirements.

Research should reduce burden on the user, not replace their authority over requirements. If sources conflict, distinguish the conflict from established facts and ask the user which source should govern.

For private or sensitive sources, verify authorization before accessing them. Limit review to information necessary for the requested task. Do not include private details in test fixtures, examples, logs, reports, or package contents unless they are essential, authorized, and appropriate for every intended recipient.

## 4. Choose an appropriate skill structure

A skill should be focused enough that both the user and the AI can predict what it does. A skill may support related variants of the same job, but unrelated work should usually be separate skills when it has different users, sources of truth, approval requirements, or definitions of completion.

A typical package may contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed guidance
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional tests and evaluation material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help decide when to use the skill.
2. **Core instructions:** The workflow required for normal use.
3. **Supporting resources:** Detailed references, templates, and scripts loaded only when relevant.

Keep core instructions readable. If they become too large, move specialized details into clearly named reference files and state exactly when each file should be consulted. Large reference files should include a navigation section or table of contents.

For skills with several variants, organize supporting material by variant. The core instructions should explain how to choose the relevant variant so the AI does not load or apply unrelated rules.

### Bundle resources only when they earn their place

If test runs show repeated reconstruction of the same deterministic task, consider bundling a reusable script, template, or reference. Good candidates include data validation, standard file transformations, repeatable calculations, report assembly, or format checks.

A bundled resource is justified when it is:

- Repeatable and meaningfully more reliable than recreating the procedure each time.
- Safe and understandable within the user’s authorization boundary.
- Likely to be reused across ordinary requests.
- Documented with expected inputs, outputs, and failure behavior.

Do not add automation solely because it is possible. A bundled resource should not conceal actions, require undeclared access, or make changes outside the user’s intended scope.

## 5. Write the skill instructions

Write in clear, direct language. Prefer imperative instructions, but explain why important steps matter. AI systems generally handle variation better when they understand the goal and tradeoff than when given a long sequence of unexplained prohibitions.

Use the following components when they apply.

### Purpose and scope

State the job, intended outcome, and boundaries. Clarify whether the skill produces an answer, creates a file, guides a user, or performs an approved action.

### Inputs and prerequisites

List required information, permitted sources, necessary permissions, and optional inputs. State what to do if a required item is missing.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or provide a clearly marked incomplete draft.
```

### Workflow

Give the normal sequence of work and include decision points rather than attempting to list every imaginable exception.

A durable workflow often follows this pattern:

1. Inspect the request and available inputs.
2. Clarify only uncertainties that materially affect the result.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the result against requested format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limits.

Use conditional guidance where it helps:

```markdown
If the user provides a required template, follow it.
If no template is available, use the default structure below.
If an action could overwrite important work or affect an external system, explain the impact and request confirmation before proceeding.
```

### Output format

When consistency is important, provide a template. For example:

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

Avoid rigid templates when contextual adaptation is the main source of value. In those cases, describe the desired qualities and provide a small example instead.

### Quality, safety, and privacy checks

State the checks required before completion. These may include verifying required fields, checking calculations, preserving originals, citing key sources, identifying uncertainty, or confirming that output access is appropriate.

The skill must behave as a reasonable user would expect from its description. Do not create instructions that facilitate unauthorized access, conceal material actions, misrepresent evidence, bypass consent, exfiltrate sensitive information, damage systems, or produce deceptive outputs.

### Failure behavior

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or reference:** Explain what could not be verified and offer an alternative method if one is safe.
- **Ambiguous request:** Make a low-risk assumption only when it does not materially change the outcome; otherwise ask.
- **Validation failure:** Do not present the work as complete. Correct it, report the issue, or request guidance.
- **High-impact action:** Pause for confirmation before external, irreversible, costly, or sensitive actions.

### Examples

Use a small number of generalized examples only when they teach a distinct pattern. Examples should show the shape of good reasoning or output, not become brittle substitutes for the actual workflow.

## 6. Review the draft before testing

Read the draft as if encountering it for the first time. Check:

- Is the job coherent and appropriately bounded?
- Does the description make activation conditions clear?
- Are inputs, permissions, outputs, and completion criteria defined?
- Does the workflow explain the reason for meaningful safeguards?
- Does it handle missing information and conflicting sources?
- Does it rely on a specific person’s habits, private access, or local setup?
- Are rules repetitive, overly rigid, or unlikely to change behavior?
- Can a capable AI adapt to normal variation without losing the goal?

Prefer lean instructions over a long list of rules that do not improve outcomes. Repeated capitalized commands or absolute language can signal brittle design unless they protect a genuine safety, authorization, or data-integrity boundary.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user and invite corrections or additions before treating them as the evaluation set.

For each test, record:

- A descriptive test name.
- The user prompt.
- Input files or context, if any.
- The expected result in plain language.
- Objective checks, if suitable.

A portable format is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and identify information that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Design coverage around meaningful situations:

- A typical successful request.
- A request with incomplete or ambiguous input.
- A format-sensitive or rule-sensitive request.
- A realistic case that changes the workflow.
- A request that should require approval, privacy protection, or safe refusal, when relevant.

Vary wording, detail level, and user sophistication. Do not simply restate the skill’s own language. Avoid using private information in tests; use fictional or properly anonymized examples that preserve the relevant challenge.

## 8. Run comparable evaluations

When independent runs are available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revised version to the prior version.

Run both conditions under comparable circumstances. If parallel execution is available, start all skill and baseline runs together. This reduces timing distortion and makes the comparison fairer.

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

For every run, preserve the prompt, allowed inputs, outputs, and available metadata such as elapsed time or compute use. Record timing when the environment reports it because some environments do not retain it later.

If independent comparison runs are not available, complete a transparent sanity check instead. Apply the skill to each test case, save the outputs, and ask the user to review them. Do not describe this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While testing is in progress, draft objective checks where they genuinely measure user value. Explain them to the user before relying on them as success criteria.

Good checks are observable, specific, and meaningful. Examples include:

- Required sections or fields are present.
- A generated file opens and follows the requested format.
- Calculated values match a known source within an agreed tolerance.
- The output identifies missing mandatory inputs.
- Important claims include approved source references when required.

Use a stable grading record such as:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests it before finalization."
    }
  ]
}
```

Use programmatic checks when practical because they are repeatable and reusable. Do not force numerical metrics onto subjective work. Tone, writing quality, aesthetics, strategic value, and practical usability often require informed human review.

## 10. Review results with a human

Present outputs and measurements through any available review method. A review interface is useful when it allows the user to inspect each test, compare configurations, and leave feedback. If no interface is available, present results clearly in conversation or as accessible files.

For each case, show:

- The original prompt and relevant inputs.
- The skill output and comparison output, if available.
- Objective grades and supporting evidence.
- Timing or resource information, if available.
- A clear place for feedback.

Ask focused review questions:

- Which output would you trust in normal use, and why?
- What was missing, misleading, or hard to use?
- Did the skill add steps or detail that did not help?
- Would this work for similar requests with different wording or data?

Empty feedback can indicate that a specific result is acceptable, but it does not prove the skill is complete. Consider feedback alongside actual outputs and evaluation results.

## 11. Analyze beyond aggregate scores

When possible, aggregate pass rate, time, resource use, and variation across tests. Place the revised skill before the comparison condition in reports for easier reading.

Then inspect patterns that summary metrics may hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not demonstrate the skill’s contribution.
- **High variation:** Similar runs differ substantially, suggesting ambiguity, instability, or unreliable instructions.
- **Quality-cost tradeoffs:** The skill improves quality but requires disproportionate time or resources.
- **Concentrated failures:** Several failures may share one cause, such as unclear source selection or missing output guidance.
- **Unproductive work:** Execution traces show redundant planning, repeated research, or unnecessary formatting.
- **Repeated reconstruction:** Multiple runs independently create the same helper procedure, showing that a reusable asset may help.

A small evaluation set is evidence, not proof. Use it to guide the next revision.

## 12. Improve without overfitting

Base revisions on user feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from complaints. If a test output fails to distinguish sourced information from assumptions, do not add a rule that merely names the test. Clarify the broader behavior: when sources are incomplete or mixed, separate verified information, assumptions, and unresolved gaps.

Apply these principles:

1. **Fix causes, not examples.** Design for future requests, not only current tests.
2. **Keep instructions lean.** Remove guidance that does not improve results or causes wasted effort.
3. **Explain intent.** State how an action protects correctness, usability, privacy, or safety.
4. **Bundle assets only when justified.** Add scripts, templates, or references when repeated work demonstrates their value.
5. **Preserve useful behavior.** Do not lose outcomes users already value while fixing another issue.
6. **Expand coverage gradually.** Add a test only when it represents a meaningful category of failure.

After revision, rerun the evaluation set in a new iteration. Use the same baseline policy unless the user agrees a different comparison is more meaningful. Show changes alongside prior outputs when possible, collect feedback, and repeat until improvement levels off.

Stop when the user is satisfied, objective requirements are reliably met, feedback is consistently positive, further changes do not yield meaningful gains, or remaining problems require a product decision or unavailable capability rather than better instructions.

## 13. Optional blind comparison

For a more rigorous qualitative comparison, use a blind review. Give an independent evaluator two outputs without revealing which skill version produced each one. Provide a shared rubric, record the evaluation, and reveal the mapping only afterward.

Blind comparison is useful when two versions have similar numerical results, when presentation quality matters, or when a decision has material importance. Evaluate role-relevant correctness, completeness, clarity, adherence to constraints, safety, and practical usability. Analyze why one output was preferred before revising the skill.

## 14. Optimize activation behavior

After the workflow itself is stable, improve the short description that helps an AI decide whether to use the skill.

Create a realistic set of activation queries with both cases that should activate the skill and difficult near-misses that should not. Use substantive requests where consulting the skill would help; very simple one-step requests may be handled directly even if the description is relevant.

Positive cases should vary in phrasing and context:

- Formal and casual wording.
- Requests that name the task and requests that imply it.
- Common and less common valid uses.
- Requests where a related skill might compete but this skill is the better fit.

Negative cases should be genuine near-misses, not obviously unrelated requests. They should share terms or concepts with the skill but require another kind of work, another capability, or conditions that make this skill inappropriate.

```json
[
  {
    "query": "I need a concise leadership update from these project notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what project reporting is and why teams use it?",
    "should_trigger": false
  }
]
```

Review the query set with the user before using it. If repeated activation testing is available, separate queries used to improve the description from held-out queries used to select the final version. Choose the description that works best on held-out cases, not simply the one that fits the examples used during editing.

A good description says what the skill does and when it applies. It should cover realistic user language without making claims broader than the skill can support.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for ordinary use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately represents activation conditions and scope.
- Instructions do not rely on private conventions, personal access, or undeclared capabilities.
- Scripts, references, and assets are present, clearly named, and documented.
- No credentials, private records, identifiers, confidential examples, or sensitive test material are included.
- The package stays within intended authorization and access boundaries.
- The user can install, access, or adapt it in their chosen environment.
- Test materials are retained only when they are safe and useful for future maintenance.

Provide a short handoff note explaining what the skill does, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has:

- A clear, bounded job.
- A description that routes appropriate requests.
- Instructions that handle normal variation.
- Explicit behavior for uncertainty, privacy, authorization, and high-impact actions.
- Outputs and formats that match user needs.
- Evidence from realistic use that it improves results or supports a valuable workflow.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable, understandable workflow that helps an AI make better decisions and deliver better results for real recurring work.


---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using real screenshots and programmatic layout checks. Fix every detected failure and rerun the relevant sweep before reporting the work as ready.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, color, background, or typography edits: a local change can affect wrapping, height, overflow, alignment, and backgrounds at other screen sizes.

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

Add a large desktop width, such as 1920 px, for landing pages or interfaces expected to be used on large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Also include any known target viewport chosen by the project or requester. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable browser automation system, such as a headless browser runner available to the project. Do not rely on manually resized personal browser windows as the only evidence.

## 3. Capture and inspect screenshots

Capture real screenshots at each relevant viewport and state. Use full-page screenshots when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect every changed component on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design now that the component's role may have changed.

Pay special attention to edge-to-edge or full-bleed changes. A component made flush with an edge can expose leftover wrapper margins or padding as visible background strips. Check every edge, not only the edge edited.

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

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant bounding rectangles with adjacent elements and container boundaries. Test actual interaction targets where possible rather than assuming that a visible control is clickable.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line; reading-focused designs commonly use a narrower target of roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visual defects such as exposed background strips, poor visual balance, or unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and relevant programmatic checks pass.

## 6. Fix failures and rerun the sweep

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the failing size.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is likely incomplete; do not accumulate patches without understanding the shared cause.

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

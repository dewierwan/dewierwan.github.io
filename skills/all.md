# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when a user needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas; it is to surface genuinely different paths, make tradeoffs clear, and leave the user with a small set of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources accessible in the current environment, review them when they are likely to affect the answer.

When accessing non-public communications or records, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant sources and information, omit unrelated or sensitive personal details, and keep the output within the appropriate access boundary.

If the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, budgets, or deadlines
- Stakeholder concerns, responsibilities, and approval boundaries
- Evidence about what has already been tried

Do not search broadly by default. Use targeted retrieval only when it could materially change the options. If important context is unavailable, state an assumption or ask a focused question instead of inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The user’s wording may describe a symptom or a preferred solution rather than the real decision. For example, “Should we add a feature?” may really mean, “How should we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip the pause only when the framing is obvious, the choice is low-stakes, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes the process, incentives, scope, or problem framing
- At least one surprising option, such as delaying, partnering, removing scope, or doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, or avoided distraction has genuine value.

Give every option a short, memorable label that communicates its core approach. For each, provide:

| Element | Include |
|---|---|
| What | One or two sentences explaining the approach. |
| Strengths | One or two concrete advantages. |
| Weaknesses | One or two concrete disadvantages, constraints, or failure risks. |
| Effort | Low, Medium, or High. |

Use specific tradeoffs. Do not soften serious drawbacks or make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, and stakeholder burden. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not why it is generally attractive.
4. Name the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may choose an option, request more detail, reject the framing, ask for new options, or combine approaches.

If the user proposes a hybrid, test whether the components are compatible and whether combining them resolves a real tradeoff rather than adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record: define the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After the decision is recorded, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Avoid skipping the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than only the stated symptom or solution.
- The options are genuinely distinct and not variations in scale.
- At least one option challenges the default framing when that could be useful.
- Strengths and weaknesses are candid, concrete, and comparably detailed.
- Effort labels are plausible.
- Recommendations follow the user’s criteria and constraints rather than unstated assistant preferences.
- Sensitive or private context, if used, was authorized, minimized, and not exposed unnecessarily.


---
name: pressure-test
description: Find weak points in a leading strategic idea before committing: strengthen the case, test its load-bearing assumptions through sequential challenge, and finish with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or create an implementation plan.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes a defense of that idea.
- If the idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.
- If the work requires access to private communications, records, or information about people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources, exclude unrelated sensitive details, and keep findings within the appropriate access boundary.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for the answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Use available evidence such as research, metrics, prior experiments, customer feedback, documented decisions, and stakeholder input. Separate facts, inferences, and forecasts.
- Identify relevant dissenters by role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's actual intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

**Template**

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, starting with the assumption most likely to undermine the decision.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | How to test or disprove it |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Smallest useful test] |

Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Start with the highest-risk assumptions. Adapt later questions to the answers received. Do not present the full list as a questionnaire, because that enables selective answering.

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

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failures, external changes, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable early signal] | [Check or accountable role] |

The warning sign must be observable early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role’s strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap. Do not assume silence means agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

| Relevant role | Strongest plausible objection | Heard directly? | Required follow-up |
|---|---|---|---|
| [Role] | [Objection] | [Yes, no, or unknown] | [Action] |

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

**Template**

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step.

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data-collection period. Next: run that test, then make the decision with its result recorded. Do not commit while the named gap remains open.
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

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and giving a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to reach a clear decision with an appropriate amount of analysis. The aim is not maximum deliberation: make small choices quickly, apply stronger safeguards to consequential choices, record meaningful decisions only with authorization, and learn from outcomes.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user prefers, believes, is leaning toward, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may give a recommendation in chat, clearly labeled **Assistant analysis**. Add it to a record only when the user asks for it there.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, plan or execute the work instead of opening a decision process.
5. **Record only with permission.** “Should we do X?” requests analysis, not a new record. Create or update a record only when the user asks to log, track, open, resume, or commit it, or has explicitly agreed to an established recording practice.
6. **Protect privacy and access boundaries.** Before searching a shared register or using private communications, personnel information, customer information, or other records, establish a legitimate purpose and clear authorization. Use the minimum relevant sources and facts. Omit unrelated personal or sensitive details.
7. **Do not use rigor as delay.** Once the relevant readiness gates are met, name the decision and proceed.

If a decision record is visible to other people, confirm its audience is appropriate before writing. For sensitive topics, including health, relationships, compensation, confidential personnel matters, or private legal matters, offer a private record or keep the discussion in chat.

## 1. Determine the working mode

If the user explicitly says they want to start, resume, commit, or review a decision, follow that instruction. Otherwise, if authorized, search the chosen decision register for a substantially overlapping record before creating a duplicate.

| Mode | When to use it | Required action |
|---|---|---|
| New | No relevant record exists, or the user requests a fresh decision | Frame and classify it. |
| Resume | A matching record is open and the user wants to continue thinking | Retrieve it and append new information. |
| Commit | An open decision exists and the user is ready to make the call | Confirm readiness, then resolve it. |
| Review | A resolved decision has reached its review date and its outcome is blank or still marked too early | Compare actuals with the original prediction. |

For a resumed decision, append new information rather than rewriting history. For a review, use the original prediction, confidence, assumptions, and stated rationale as the baseline. Do not replace them with hindsight.

## 2. Frame a decidable question

Establish:

- What exact choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing where relevant?
- What is the deadline, trigger, or cost of waiting?
- What result is desired?
- What happens if no action is taken?

If the issue is broad and credible options do not exist yet, generate options before evaluating them. Do not pressure-test a vague problem statement.

If only one viable path exists, say so plainly:

> This appears to be a task rather than a decision. The next step is to plan or execute it.

## 3. Classify the scope

Ask one clarifying question at a time if needed. Classify by consequences and cost of reversal, not by how emotionally difficult the choice feels.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not record by default. |
| Reversible | Moderate stakes and reversible within days or weeks | Compare a few options; use a light record when authorized. |
| Hard to reverse | Meaningful cost, disruption, lost trust, or strategic impact if undone | Full analysis, challenge gate, stakeholder check, and full record when authorized. |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and a named prerequisite consultation. |

Use this test when uncertain:

> What would it cost to unwind this?

Consider money, time, trust, operational disruption, opportunity cost, contractual constraints, and reputational effects. If the unwind cost cannot be stated quickly, or remains highly uncertain, treat the decision as larger rather than smaller.

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right level of rigor

### Trivial

Choose a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: continued attention may cost more than an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. For each, state one meaningful strength, one meaningful weakness, and a rough effort, time, or cost estimate.
3. Identify the decisive tradeoff.
4. Give a recommendation labeled as Assistant analysis unless the user adopts it in their own words.
5. If uncertainty is material, choose the smallest reversible test likely to change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test examines its key assumptions, disconfirming evidence, strongest alternative, likely failure modes, stakeholder objections, and relevant reversal conditions.

If no relevant pressure test has been completed in the current work context, stop the commitment flow and state:

> This decision is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Continue only after the pressure test is complete or the user explicitly overrides it with a reason. If it reveals a serious unresolved failure, do not force commitment. Return to option generation, redesign the option, obtain a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check stakeholders with relevant expertise, consequences, or hidden constraints.
4. Provide a recommendation as Assistant analysis unless the user states their own choice.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required consultation has happened, unless the user explicitly accepts and records a reason for proceeding without it. If it is being rushed, name what consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture what it enables; what it costs, delays, or prevents; its strongest supporting evidence; its strongest objection; its key assumptions; and the ease and cost of reversal.

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies a real tradeoff rather than disguising judgment as precision.

Keep these categories separate in conversation and records:

| Category | Rule | Example |
|---|---|---|
| User’s stated view | Include only positions actually expressed by the user | “The user stated a preference for Option B.” |
| Assistant analysis | Label assistant advice and reasoning | “Assistant analysis: Option A reduces execution risk.” |
| Open question | Identify uncertainty without treating it as resolved | “Unknown: whether the provider can meet the timeline.” |

If the user has not expressed a position, write “No position stated yet” or leave the user-position field blank. Never invent a lean, confidence level, rationale, response to dissent, or final choice.

## 6. Open, commit, and maintain a record

Use the user’s chosen decision register, document system, or private file. If an organization has an approved practice for recording non-trivial decisions, use it only within the user’s access and authorization boundary.

A record should include at least these fields:

| Field | Purpose | Example value |
|---|---|---|
| Status | Whether the decision remains open or has been resolved | Open; Resolved: Yes; Resolved: No |
| Type or domain | Area affected | Strategy; operations; finance |
| Stakes and reversibility | Rigor and unwind context | High; hard to reverse |
| Decision and review dates | Timing for commitment and learning | [Date] |
| Confidence | User’s confidence in the prediction at decision time | [X%] |
| Outcome | Prediction result, distinct from process quality | Too early; correct; incorrect; mixed; not applicable |

For non-binary questions, use a resolved status once a direction is chosen. Resolution is about whether the call was made, not whether the question has a yes-or-no form.

### Open record

For a decision the user wants to think about across sessions, record the context, options, and factual new inputs. Set its status to open. Leave commitment sections, including the user’s choice, confidence, prediction, and worries, blank unless the user has actually provided them.

### Commit record

Before resolving a meaningful decision, confirm:

- What is the decision and chosen option?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable result is predicted?
- What is the user’s confidence in that prediction?

Make predictions testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Set the decision date to when the user actually made the call. Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Adjust when the user identifies a more meaningful trigger.

For hard-to-reverse and direction-setting decisions, create a reminder in the user’s calendar, task system, or other reminder tool when available and authorized. Include the review date, decision question, and permitted link or record location. A record-level review date is usually sufficient for reversible decisions.

Use this body structure:

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

When resuming an open record, append a new dated thinking-log entry and add newly credible options without deleting earlier history. If the user remains open, summarize the current state and identify what to explore next rather than filling commitment sections.

## 7. Review the outcome

At the review point, assess four separate questions:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle that can improve future decisions.

Update the record’s outcome to correct, incorrect, mixed, too early, or not applicable, and fill the retrospective. Do not collapse a bad outcome into a bad process, or a good outcome into a sound process.

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

Use direct language. Challenge weak reasoning with evidence while preserving the user’s ownership of the decision. Once the appropriate rigor has been applied, make the call and move forward.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, recommendation, implementation, verification, and handoff. The workflow supports analysis-only work when requested and requires explicit,.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, automation, or operational problem whose solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to “build X,” work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including existing workarounds?
- How frequent, costly, urgent, or blocking is it?
- What outcome would materially improve the situation?
- What constraints matter: time, budget, reliability, privacy, compatibility, or ownership?

Write a concise problem statement and descriptive requirements. Describe desired outcomes and constraints, not an assumed implementation. If the proposed solution does not fit the problem, say so directly.

Ask only for information that cannot be found in authorized project context, documentation, code, or records. When examining communications or records about people, use them only for a legitimate purpose with clear authorization; inspect the minimum relevant sources, omit unrelated sensitive details, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and the cost of delay. Include **do nothing**, **defer**, or **improve the current workaround** as real options when appropriate.

Distinguish between:

- **Reversible decisions:** Small, easy-to-change choices. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, long-lived settings, migrations, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record rationale when the decision has lasting consequences.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before spending substantial effort on design or implementation.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before inventing a new mechanism.

Identify constraints such as compatibility requirements, deployment practices, supported environments, ownership boundaries, monitoring, security expectations, and privacy requirements. Use existing conventions unless there is a strong, documented reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve existing authentication, access controls, and data behavior.
- Must fit available delivery time and maintenance capacity.
- Should avoid new dependencies, public interfaces, or persistent configuration.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide option generation and selection. Without them, the first plausible solution can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change: instructions, a process adjustment, a template, training, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For an ambiguous or high-impact problem, generate a broader set of candidates before narrowing. Keep each option concise: what it is, which requirement it addresses, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate inputs and states strictly; fail visibly for invalid states rather than silently producing plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, persistent data, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Place changes in the appropriate design boundary; do not use a quick fix that creates hidden long-term complexity.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Keep the proposal direct. Store it in the user's chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear date-prefixed title, such as `10 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and ownership of follow-up actions. Keep the plan in a location where relevant reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, access control, privacy, and failure behavior.

Do not claim success based only on implementation. State what was actually tested, what passed or failed, and what remains unverified. Commit, publish, or deploy only according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.


---
name: shape-and-draft
description: Shape consequential documents by reviewing authorized evidence, resolving material choices through answer-dependent interviews, checking readiness, and then drafting and auditing the smallest document that can achieve the goal.
---

# Shape and draft a document

Develop a consequential document by shaping the underlying thinking before writing it. Determine what the document must achieve, gather relevant evidence, resolve material choices with the appropriate decision-maker, and then draft the smallest document that can do the job.

Use this workflow for strategies, narratives, operating agreements, briefs, proposals, scorecards, and decision memos when the artifact, argument, boundaries, commitments, or operating model are not yet settled. Do not use it for a quick edit, a formatting request, or a document whose content and decisions are already specified.

When reviewing private communications, personnel records, internal documents, or other sensitive material, ensure there is a legitimate work purpose and clear authorization. Use only the minimum relevant sources and details, avoid unrelated personal or sensitive information, honor consent and privacy expectations, and keep the output within the intended access boundary.

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

Read supplied material first. Follow any stated rules for source selection, authority, citations, and linking. Scale the research effort to the stakes and use only sources and systems that the requester is authorized to access.

For a consequential internal document, look for material likely to contain prior decisions, current definitions, supporting evidence, dissent, constraints, ownership context, and relevant performance information.

Apply these evidence rules:

- Respect a stated hierarchy of sources.
- Prefer current, authoritative decision records over discussion notes, recollections, generated summaries, or repeated claims.
- Resolve contradictions where evidence permits; surface material contradictions that remain.
- Do not ask participants for factual information that available, authorized sources can answer.
- Do not edit, overwrite, or otherwise change source material unless explicitly instructed.
- Do not copy sensitive personal details into a draft unless they are necessary for the document’s legitimate purpose and appropriate for its audience.

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
2. For bounded choices, provide three or four mutually exclusive, decision-relevant options where possible, labeled `a.`, `b.`, `c.`, and `d.`. Use two options only when there are genuinely only two distinct states.
3. Put the recommended option first unless prior context clearly makes another order more useful.
4. Put questions and options on consecutive lines, with no blank lines within the question block.
5. Allow the respondent to reject the framing or provide an alternative answer.

Example:

1. Which direction should the document recommend?
   a. Focus on the highest-impact problem first; this narrows scope but clarifies accountability.
   b. Address all related problems equally; this is broader but less decisive.
   c. Present the alternatives without a recommendation.
   d. Keep the direction open pending a defined decision.
2. Who should make the final decision?
   a. The accountable lead makes the decision after consultation.
   b. A cross-functional group decides jointly.
   c. The accountable lead proposes a decision for executive approval.

Each round should:

1. Begin with an updated model of the situation and state what changed because of earlier answers.
2. Focus on one layer of uncertainty rather than mixing every issue at once.
3. Explain the tradeoff behind the recommended option.
4. Separate source-supported observations from choices participants must make.
5. Surface contradictions and ask the smallest question needed to resolve them.
6. Include a pressure test when the document is persuasive or strategically consequential.

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
- Keep action-oriented sections short. As a useful default, use no more than seven top-level bullets in a section and usually five or fewer for the main outcomes; combine or move detail when needed.
- Preserve hard ideas when they matter, but explain them in plain language rather than jargon.

Honor the requested destination using the chosen system. If text is requested in the conversation, provide text without changing source material. If a document must be created or updated elsewhere, do so only as instructed and verify that the intended content is present.

When the target format supports lists and headings, inspect the rendered result. Ensure headings do not accidentally inherit bullets or numbering, no unintended blank paragraphs appear after lists, indentation is consistent, and page breaks do not leave orphaned bullets or awkward section starts.

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
- Does it expose only information appropriate for the intended audience and access boundary?
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
- Including private or sensitive details that are not needed for the authorized purpose.
- Mistaking concise writing for choppy writing by using fragments, noun-only bullets, or artificially short sentences.
- Delivering structurally valid content without checking how it renders in the destination format.


---
name: gather-context
description: Search the sources most likely to matter and turn the findings into a concise, evidence-linked context brief for a decision, task, or conversation, while scaling research to the stakes and respecting authorization and privacy limits.
---

# Gather context

Assemble a well-sourced context brief about a person, organization, project, topic, or decision. Use it when the user needs to get up to speed before writing, deciding, meeting, planning, pitching, hiring, or taking another concrete action.

The central rule is **right-size the research**. Search enough to answer the real question reliably, but do not sweep every available source merely because access exists. A quick status question should not become a lengthy investigation; a high-stakes decision should not rely on one convenient message thread.

## 1. Confirm purpose, access, and output boundary

First identify:

- **Purpose:** What action, decision, meeting, or question will this support?
- **Subject:** Is this a person, organization, project, topic, or decision?
- **Audience:** Who may see the result?
- **Authorization:** Is there a legitimate purpose and clear permission to use any private source?
- **Destination:** Is chat sufficient, or should the result be placed in an approved shared workspace?

Access to a private system is not, by itself, a reason to search it. Search only sources that are relevant to the stated purpose.

### Additional rules for research about people

When the subject is a person, use a stricter standard:

- Use the minimum relevant sources and information needed for the task.
- Do not search private messages, personal notes, or sensitive records simply because they are accessible.
- Do not include unrelated personal details, speculative inferences, health information, family information, or protected characteristics unless clearly necessary, authorized, and appropriate.
- Respect confidentiality, consent, need-to-know limits, and reasonable privacy expectations.
- Keep the brief within the access boundary of its evidence. Do not copy restricted details into a broader or less secure destination.
- For hiring or assessment, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether the process distinguishes relevant performance. Do not make broad character judgments from incomplete information.

If purpose, authorization, subject identity, or destination is unclear, ask before searching private sources.

## 2. Scope the gather

Choose an effort level before using tools. State it in one short line so the user can redirect the work, for example: “I’ll do a standard review across the most relevant internal records and public sources.”

| Level | Use when | Typical approach |
|---|---|---|
| Quick | A reminder, simple status check, or low-stakes question. | Check one to three obvious sources, use one or two focused queries, and return a few concise findings. |
| Standard | The usual case: preparation for a normal discussion, update, or moderate-impact choice. | Search several relevant sources, inspect the strongest results, and produce a compact structured brief. |
| Deep | A high-stakes decision, major partnership, important hire, sensitive issue, or consequential commitment. | Search broadly but purposefully, use multiple query angles, verify important claims, compare conflicting evidence, and document meaningful gaps. |

When uncertain, start lighter and offer to deepen the work. Escalating is inexpensive; collecting excessive private or irrelevant material is not.

Then classify the subject to select likely sources:

- **Person:** correspondence, collaboration messages, relationship records, meeting notes, calendar history, authorized recruitment records where relevant, and public professional information.
- **Organization:** public website and credible reporting first, then correspondence, partnership records, internal notes, and relationship databases.
- **Project or initiative:** project documents, task records, working messages, meeting notes, code or change history when relevant, and usage or outcome data.
- **Topic or question:** public research plus internal strategy documents, prior discussions, and decision records.
- **Decision:** evidence about the options, assumptions, owners, constraints, risks, prior decisions, and consequences of each path.

If a name or term could reasonably refer to several things, ask one focused clarification question before searching. Otherwise, proceed without unnecessary questioning.

Set a time window. A useful default is the most recent six months, extending further back for longstanding relationships, recurring projects, or decisions with important historical context.

## 3. Select and search sources

Named sources are mandatory, but they are not necessarily exhaustive. Add another source only when a sensible researcher would expect it to contain decision-relevant evidence.

Possible source capabilities include:

- Email and direct correspondence.
- Team messages and discussion threads.
- Internal documents, knowledge bases, and decision logs.
- Shared file storage and documents.
- Calendar events and meeting notes.
- Meeting transcripts or recordings, where authorized.
- Relationship, project, applicant, customer, or operations databases.
- Product analytics or operational metrics.
- Code repositories and change history.
- Public websites, professional profiles, filings, publications, and reputable news.

For a quick or standard gather, search inline and inspect the strongest results. For deep research involving many independent source clusters, parallelize read-only searches where doing so saves time and does not expand access unnecessarily. Ask each parallel researcher to return a concise digest with direct evidence references, not a raw data dump.

### Query method

Use queries appropriate to the source and effort level:

1. Search the exact name, organization, project title, or distinctive phrase.
2. For deeper work, search aliases, related organizations, relevant colleagues, alternate spellings, and important project keywords.
3. Inspect the most relevant full threads, documents, or records rather than relying only on search snippets.
4. For a person or organization, distinguish direct correspondence from third-party mentions.
5. For a project, search both its name and the work terms likely to appear in planning or implementation records.
6. For a decision, search for options, objections, approvals, milestones, owners, and prior commitments.

If results reveal a recent or imminent meeting, check the authorized meeting notes or transcript. Such records often contain the clearest account of current decisions, commitments, and unresolved questions. Attribute speakers carefully: transcript participant labels may not perfectly identify every speaker.

When reading multi-section documents, inspect every relevant section, tab, attachment, or linked subdocument. Do not assume that the first visible section contains all material. Attribute findings precisely enough that another reader can locate them.

For public web research, prefer current primary sources for roles, dates, organizational status, product details, and announcements. Cross-check time-sensitive claims against recent authoritative evidence. Do not include a web address unless it was verified or supplied by the user.

For operational databases, first understand the relevant schema, record meaning, and field limitations. Do not treat a record system as authoritative without checking whether it is complete, current, and used consistently. Use canonical systems for their intended domain, such as an applicant system for application status or an approved project system for delivery status.

For technical projects, inspect the relevant repository, issues, release notes, and change history only when they are needed to answer the question. Code presence alone does not establish that a feature is deployed, used, or successful.

## 4. Handle missing, unavailable, and conflicting evidence

Do not silently substitute one source for another. If a source was judged relevant but is unavailable, inaccessible, or returns no useful result, say so in the brief. A deliberately skipped source does not need to be listed as a gap.

When a connected source fails:

1. Confirm the exact source, search, and failure.
2. Attempt safe diagnostics available to the researcher, such as checking configuration, connection state, account permissions, or authentication status.
3. Repair only what can be safely repaired without changing user data or expanding permissions.
4. If user action is required, state the exact remaining action, such as completing authentication or restoring access.
5. Do not claim the source was searched successfully until it was.

Treat evidence quality explicitly:

- Prefer primary records, current records, direct statements, and canonical decisions.
- Treat informal summaries, search snippets, and third-party discussion as weaker evidence.
- Separate facts, informed interpretations, and open hypotheses.
- Resolve contradictions where possible. State which evidence is more credible and why.
- Preserve uncertainty when it cannot be resolved; do not force a clean narrative.

## 5. Synthesize into a context brief

Organize findings by what the user needs to know, not by the order in which systems were searched. Lead with the facts that change the next action.

Every material sourced claim should include a direct, clickable reference to its underlying evidence when the destination supports links. Link to the specific thread, document, meeting record, database record, repository revision, or verified public page—not merely a generic home page. Do not expose a reference outside the access boundary appropriate to its source.

Use this adaptable structure:

```markdown
## [Subject] — context brief
*Scope: [quick, standard, or deep]. Sources reviewed: [source categories]. Window: [date range].*

## TL;DR
- [Most decision-relevant finding, with direct evidence reference.]
- [Current state, risk, opportunity, or recommendation-relevant fact.]
- [Important uncertainty or next milestone.]

## What we know
### [Theme]
[Synthesized finding with direct evidence references.]

### [Theme]
[Synthesized finding with direct evidence references.]

## Relationship or timeline
- [Date]: [Relevant interaction, decision, or event with evidence reference.]

## Open questions and gaps
- [Question not answered] — expected evidence source: [source category].
- [Unavailable, empty, or conflicting relevant source], if applicable.

## Key sources
- [Descriptive source title — direct evidence reference]
```

Adapt headings to the subject. A decision brief may use “Options,” “Evidence for and against,” “Constraints,” and “Decision needed.” A project brief may use “Current status,” “Milestones,” “Risks,” and “Owners.”

Keep prose scan-friendly. A quick brief may be only a short summary and a few linked facts. A deep brief may include a fuller timeline, evidence comparison, and explicitly separated risks and unknowns.

## 6. Choose the delivery method

Deliver a short brief directly in the conversation when it fits comfortably on screen and the audience is appropriate. Put the brief itself at the end of the response; place any offer of follow-up work before the brief.

For a long-lived or substantial reference brief, create it only in a user-approved, access-controlled shared document location. Use a concise, readable title containing the date and subject. Do not place private findings in local files, public locations, or broad-access workspaces without approval.

When editing an existing formatted document:

- Insert content only in a known body-text location or replace a complete, inspected section.
- Do not insert markdown or placeholders into the first character of an existing heading, list item, table cell, or styled paragraph.
- Re-read the affected range after insertion and verify heading, body, and list styles.
- If visual layout matters, render or inspect the document rather than relying only on plain-text extraction.
- Do not report completion until both content and formatting checks pass.

## Final audit

Before delivering, check:

- Is the effort level proportionate to the user’s need?
- Was each private source necessary, authorized, and used minimally?
- Did the research address the actual decision or task?
- Are material claims connected to direct evidence?
- Did the brief distinguish fact, interpretation, and uncertainty?
- Were contradictions resolved or clearly flagged?
- Are unavailable or empty relevant sources disclosed?
- Does the destination respect the sensitivity and access boundary of the evidence?
- Is the result concise enough to act on?


---
name: learning-tutor
description: Learn a paper, article, post, or topic through a short Socratic dialogue that emphasizes retrieval, explanation, challenge, and application rather than passive summary.
---

# Learn with a tutor

Help a learner understand, retain, and use a provided paper, article, post, or topic through a rigorous dialogue. Prioritize active recall and reasoning over explanation: the learner should do most of the intellectual work, while the tutor guides, diagnoses, and raises the level of challenge.

## Learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to recall and reconstruct ideas in their own words.
- **Ask for mechanisms.** Move beyond conclusions by asking why, how, under what conditions, and with what evidence an idea works.
- **Require generated connections.** Ask the learner to create their own examples, analogies, predictions, and uses before offering examples yourself.
- **Use productive difficulty.** Make the task effortful enough to promote learning, but not so difficult that the learner cannot make a meaningful attempt.
- **Practice transfer.** Move from the original material to unfamiliar cases, related ideas, and real decisions.
- **Surface gaps through questions.** When an answer is incomplete or inconsistent, use a focused question to help the learner notice the issue. Explain directly only after a fair opportunity to reason.

## Conversation workflow

### 1. Establish prior knowledge and a learning target

Begin before explaining the material. Ask what the learner already knows, believes, or has experienced about the topic, along with what they want to be able to understand or do.

Ask one or two open questions, such as:

- “What do you already think is true about this topic, and why?”
- “What experience or prior knowledge do you have that might connect to this?”
- “What are you hoping to be able to explain, evaluate, or do by the end?”

Use the response to identify useful background knowledge, likely misunderstandings, and an appropriate challenge level.

### 2. Elicit the central claim from memory

Ask the learner to explain the main argument, finding, or idea without quoting the source.

Useful prompts:

- “In your own words, what is the main claim?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “If you had 30 seconds to explain this to a thoughtful friend, what would you say?”

If the learner has not yet read or engaged with the material, ask for their initial prediction or working model. Then direct them to inspect the relevant material before returning to retrieval.

### 3. Select a few high-value ideas

Do not attempt to cover every detail. Select two or three ideas that are central, difficult, consequential, or likely to be misunderstood. Explore those deeply.

For each idea, use this cycle:

1. Ask the learner to state or reconstruct the idea.
2. Probe their reasoning, assumptions, evidence, and causal story.
3. Ask for a self-generated example, analogy, comparison, or application.
4. Test the idea with an objection, boundary case, competing explanation, or changed assumption.
5. Adapt the next question to the learner’s actual answer.

Keep turns short. Usually ask one or two questions at a time.

## Question toolkit

Choose questions that require explanation, reconstruction, or judgment rather than simple recognition. Adapt the wording to the learner and material.

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
- “What prediction does this idea make in a new situation?”

Avoid questions answerable only with yes or no. If a closed question is necessary, immediately ask the learner to explain and defend their answer.

## Responding to learner answers

Be warm, direct, and specific. Avoid generic praise. When an answer is strong, identify what made it useful—for example, it named an assumption, separated correlation from causation, described a mechanism, or provided a relevant counterexample—then raise the challenge.

When an answer is wrong or incomplete:

1. Do not immediately provide the correction.
2. Identify the tension with a focused follow-up question.
3. Allow one or two genuine attempts to resolve it.
4. If the learner remains stuck, give a concise explanation of the missing distinction, evidence, or reasoning step.
5. Ask the learner to restate the corrected idea in their own words or apply it to a fresh case.

If the learner says, “I don’t know,” invite a low-stakes attempt first:

> “Take a guess based on what you do know. What seems most plausible, and why?”

Offer a hint after an attempt, or earlier when the task clearly depends on knowledge the learner has not yet encountered.

## Calibration and pacing

Adjust difficulty based on demonstrated understanding.

| Learner signal | Tutor response |
|---|---|
| The learner answers easily or repeats the source language without explanation. | Ask for a mechanism, counterexample, alternative explanation, prediction, or transfer to a new setting. |
| The learner has part of the idea but misses a key distinction. | Narrow the question to the relevant assumption, comparison, or evidence. |
| The learner is lost or overloaded. | Reduce the scope, use a simpler case, isolate one step, or ask them to compare two explanations and defend a choice. |
| The learner is engaged and reasoning deeply. | Pursue implications, objections, limitations, and applications in greater depth. |
| The learner is tired or losing focus. | Consolidate demonstrated learning and end with a clear retrieval prompt rather than introducing more material. |

Maintain a dialogue rather than a fixed quiz. Questions should build on the learner’s responses and remain focused on understanding, not performance display.

Aim for a question-heavy exchange: roughly 70% questions and 30% explanations or feedback. Explain when needed, but do not lecture when a well-chosen prompt can make the learner retrieve or infer the point.

## Progress checks

Periodically give a brief, evidence-based assessment of learning:

- What the learner has demonstrated they understand.
- What remains uncertain, incomplete, or confused.
- The most useful concept, distinction, or question to revisit next.

Do not treat recognition of a term or repetition of a conclusion as mastery. Look for accurate explanation, reasoning, and transfer to a new case.

A useful check can follow this pattern:

> “You have shown that you can explain [idea] and apply it to [case]. The remaining uncertainty is [gap or assumption]. Let’s test that by considering [next question].”

## Closing gate

Before ending, ask the learner to convert understanding into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for either a concise final explanation in their own words or a future retrieval prompt they can answer later. End by naming the next concept or question worth revisiting.

## Guardrails

- Do not summarize the material unless the learner explicitly asks; even then, invite their own summary first.
- Do not define jargon automatically. Ask the learner to define it first, then clarify or correct as needed.
- Do not make the interaction easy merely to be encouraging.
- Do not cover the entire source superficially when a few core ideas can be understood deeply.
- Do not turn the dialogue into a sequence of detached test questions; connect each prompt to what the learner just said.
- Do not rely on praise without evidence. Name the reasoning or evidence that was useful, then help the learner extend it.
- Do not end without an application, changed belief, decision, prediction, or future retrieval task.


---
name: write-in-my-voice
description: Draft or revise email in the user's established voice by applying an approved writing profile, verified facts, and a concise final audit. Keep the result copy-ready, accurate, appropriately bounded, and suited to the recipient and purpose.
---

# Write in my voice

Use this workflow when the user asks to draft, reply to, revise, or polish an email on their behalf.

## Goal

Produce a short, copy-ready email that sounds recognizably like the user while remaining accurate, useful, and appropriate for the recipient and situation.

## 1. Load the voice profile first

Before drafting, read the user's current writing profile in full, if one is available and the assistant is authorized to use it. A profile may include:

- Preferred greetings and sign-offs.
- Formality level, warmth, directness, and common phrasing.
- Sentence and paragraph length.
- Contraction, punctuation, capitalization, and formatting habits.
- Language, tones, or punctuation to avoid.
- Approved factual references, reusable replies, scheduling methods, links, and boilerplate.

Treat the profile as the primary source for voice. If it includes an approved reusable response or factual detail that directly fits the request, use it rather than inventing a replacement.

Only access user-provided or authorized writing examples and records. Use the minimum material needed to establish style, and do not expose unrelated personal, confidential, or sensitive information in the output.

## 2. Establish the email brief

Identify the minimum facts needed for a safe draft. Ask focused questions only when a missing detail would materially change the email.

| Needed information | Example question |
|---|---|
| Recipient and relationship | Who is receiving this, and how well do you know them? |
| Purpose | What do you want them to know, decide, or do? |
| Required details | Are there dates, links, attachments, names, or facts that must be included? |
| Tone and stakes | Should this be casual, firm, apologetic, or more formal? |
| Commitments | Can you confirm any timing, availability, pricing, approval, or next step? |

Do not invent facts, decisions, availability, commitments, links, attachments, emotional reactions, or approval status. Where the user has not provided enough information, either ask one concise question or use wording that does not imply an unsupported commitment.

## 3. Adapt voice to context

Keep the user's core voice, but adjust the level of formality and context for the recipient.

- **Familiar recipient:** Use the user's normal level of brevity and informality.
- **New, external, senior, or high-stakes recipient:** Preserve the user's directness while adding enough context to avoid ambiguity.
- **Conflict, correction, or decline:** Be clear, factual, and respectful. Avoid defensive explanations, hollow praise, or excessive apology.
- **Request or follow-up:** State the requested action and timing plainly.
- **Sensitive topic:** Include only information necessary for the recipient's legitimate purpose. Do not disclose private details that are not needed to act.

Do not mechanically apply a phrase, greeting, or sign-off if it would be inappropriate for the relationship or situation.

## 4. Draft the smallest complete email

Use a compact structure unless the situation requires more detail:

1. Greeting, when consistent with the user's normal practice.
2. Main point or response in the first sentence.
3. Essential context, request, decision, or next step.
4. Closing and sign-off, when appropriate.

Prefer concrete wording, active verbs, short sentences, and short paragraphs. Put requests, decisions, deadlines, and needed actions where the recipient can quickly find them.

Use bullets only when they make a list of actions, options, or logistics easier to scan.

Remove anything that does not add value, including:

- Generic opening pleasantries that are not useful or characteristic of the user.
- Process narration, such as explaining how the message was prepared.
- Repeated thanks, generic compliments, or filler.
- Hedging that weakens a clear request or decision.
- Unnecessary background, especially private or sensitive context.

## 5. Audit before presenting

Review the final draft line by line.

### Voice check

- Does the greeting, sign-off, rhythm, and punctuation match the approved profile?
- Does the draft use the user's usual degree of warmth, directness, and brevity?
- Does it avoid words, tones, or formatting the profile says not to use?
- Would the user plausibly send these exact words?

### Accuracy and action check

- Are names, dates, links, attachments, and stated facts correct?
- Does the draft avoid unsupported promises or assumptions?
- Is the recipient's requested action clear?
- Are ownership and timing clear when they matter?
- Can any sentence be removed without reducing meaning or usefulness?

### Privacy and boundary check

- Is there a legitimate purpose and authorization for using any source material?
- Does the email include only the personal or confidential information needed for the recipient?
- Is the message appropriate for the recipient's access level and the communication channel?

## Readiness gate

Present a final draft only when all of the following are true:

- The recipient and purpose are understood.
- Material facts and commitments are confirmed or safely omitted.
- The tone matches both the user's voice and the situation.
- The requested action or decision is understandable.
- The draft contains no unnecessary filler or sensitive detail.

If the draft fails a gate, ask the smallest useful clarification rather than guessing.

## Output format

Provide the email as copy-ready text with no commentary after it. If clarification is required, ask only the specific question needed to continue.

If no voice profile or authorized examples exist, say so briefly and use a broadly useful default: concise, clear, warm-professional, and direct. Invite the user to provide a few approved examples or explicit preferences for future drafts.


---
name: professional-social-post
description: Draft, revise, and audit professional social posts from notes, drafts, articles, transcripts, research, or a topic, emphasizing evidence-backed specificity, strong hooks, useful substance, respectful audience targeting, and targeted edits.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a rough draft, an article, a transcript, a podcast, research findings, a visual asset, or a simple topic.

The goal is not to make an announcement sound enthusiastic. The goal is to help the right reader stop, understand a useful point, and have a reason to care. Write for a defined professional audience with low tolerance for fluff, generic inspiration, vague claims, and unsupported certainty.

This is platform-independent. Before drafting, ask the user to choose or confirm:

- **Platform and format:** text post, caption, document carousel, thread, article promotion, or another format.
- **Audience:** for example, technical practitioners, founders, policy professionals, researchers, customers, partners, or job candidates.
- **Purpose:** share an insight, explain a concept, announce something, promote a longer piece, begin a substantive discussion, recruit participants, or support a campaign.
- **Voice:** formal or conversational; first-person, team, or organizational voice; preferred words; forbidden words; punctuation preferences; and length.
- **Evidence and permissions:** what sources support the claims, and what names, quotes, outcomes, images, or personal details may be shared.
- **Link plan:** whether an external link is needed and where the user prefers to place it for the selected platform.

If the user provides approved posts, a style guide, brand guidance, audience research, or an editorial policy, treat those as the primary source of voice and formatting rules. Do not assume a particular person’s voice, publishing system, audience, or distribution tactic.

## Scope, routing, and privacy

Some post types need a dedicated structure. Identify the genre before drafting.

- **Career or participant case study:** A person’s starting point, turning point, and later outcome. Use a case-study structure: starting point, trigger, concrete outcome, supporting evidence, and lesson. Confirm that the individual has consented to the disclosure and that the user is authorized to use relevant records or quotes.
- **Research or evidence post:** A claim based on a report, model, survey, experiment, or analysis. Prioritize the method, assumptions, uncertainty, and defensible interpretation.
- **Product or organizational announcement:** Lead with the concrete change and why it matters to readers. Do not lead with internal excitement.
- **Article, podcast, or report promotion:** Lead with the strongest finding, disagreement, or useful framework from the piece. Do not lead with “new article” or “new episode.”
- **Carousel or document caption:** Give one or two meaningful findings, then explain what the visual asset adds. Do not repeat every slide in the caption.

If the request involves private communications, employment records, participant records, customer information, or information about identifiable people, proceed only when there is a legitimate purpose and clear authorization. Use the minimum relevant sources and details. Omit unrelated, sensitive, embarrassing, or confidential information. Respect consent, privacy expectations, contractual restrictions, and the intended access boundary of the final post.

If the genre, permissions, or intended disclosure level are unclear, ask one concise routing question before writing.

## Accuracy and evidence rules

1. **Do not invent facts.** Do not fabricate statistics, names, quotes, outcomes, clients, organizations, titles, dates, research findings, testimonials, or endorsements.
2. **Separate evidence from interpretation.** State what the source shows, then identify the conclusion, recommendation, or hypothesis as such.
3. **Preserve meaningful uncertainty.** If a result has large ranges, limited evidence, important assumptions, or correlation rather than causation, say so plainly.
4. **Use exact details when supported.** Specific figures, dates, roles, outcomes, and mechanisms are usually stronger than broad descriptions. Do not turn a rough estimate into falsely precise language.
5. **Ask for missing evidence early.** If the post depends on an unsupported claim, remove it, narrow it, qualify it, or ask the user for a source.
6. **Avoid misleading urgency.** Do not inflate stakes merely to create engagement. A specific risk and a proportionate response are more credible than broad catastrophe language.
7. **Use personal stories carefully.** Share only information that is approved, relevant, and necessary to make the point. A role-relevant outcome is usually enough; unnecessary biographical details are not.

## Audience and voice

Write for the reader most likely to act on the post, not for everyone who might vaguely relate to it. Specificity is useful because it helps the right readers recognize that the post is for them.

Default voice, unless the user gives a different brief:

- Direct, clear, and conversational.
- Short sentences and concrete nouns.
- Active voice where possible.
- One main claim per sentence.
- Sober about problems and practical about responses.
- Specific rather than promotional.
- Confident only where the evidence supports confidence.

Avoid these common failure modes:

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are thrilled to announce an exciting new initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences full of unexplained terms. | State the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Broad catastrophe language without a clear mechanism or response. | Name the specific risk, evidence, uncertainty, and useful intervention. |

For hiring, admissions, or assessment-related posts, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Avoid language that treats people as objects, reduces them to categories, or frames fair assessment differences as inherently suspect.

## Core workflow

### 1. Inspect the source before choosing a format

Do not begin with a template. Read the source and locate the strongest material inside it.

Look for:

- An unusual or surprising fact.
- A specific number that creates tension.
- A counterintuitive conclusion that can be defended.
- A concrete before-and-after outcome.
- A meaningful strategic trade-off.
- A sharp disagreement between credible views.
- A useful framework, checklist, or model.
- A sentence that changes how the reader sees the problem.

The formal headline of an article is often not the best social-post angle. The strongest thread may be a detail in the middle of the source.

If several viable angles exist, do not silently choose one. Present two to four numbered options. For each, explain what it foregrounds and why it may fit the audience.

**Angle-selection prompt:**

> I see several viable post angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [specific story, outcome, or disagreement]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Choose one primary thread. A social post should not attempt to summarize every point in the source.

### 2. Generate hooks before drafting the body

The opening determines whether the rest of the post is read. Generate five to ten candidate hooks internally. When user choice would help, show a shortlist of three to five options with a short strategic note for each.

A hook should make an honest promise that the body fulfills. It should generally work on its own, without requiring the reader to understand the source first.

Useful hook patterns include:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific body of evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Named outcome:** “[Person or role] moved from [starting point] to [specific outcome] in [timeframe].” Use only with evidence and approval.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only if the post defends the claim.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused disagreement:** “Why do two credible groups reach such different conclusions about [specific issue]?”

Use a hook table when presenting options:

| Hook | Strategic purpose |
|---|---|
| “[Specific claim or finding].” | Leads with a concrete result and gives readers a reason to continue. |

Apply the **swap test**: if a key subject in the hook could be swapped for an unrelated field and the sentence would still work, the hook is probably too generic. Add the mechanism, outcome, constraint, or detail that makes it specific to this post.

Avoid:

- Generic announcement openings such as “Excited to share.”
- Throat-clearing such as “In today’s fast-moving environment.”
- Empty cliffhangers that do not provide a payoff.
- Multiple rhetorical questions in a row.
- Broad motivational claims.
- Clickbait such as “You will not believe” or “This changes everything.”

### 3. Choose one structure

Select the structure that fits the material. Do not combine several structures unless there is a clear reason.

1. **Counterintuitive claim → evidence → implication**  
   Best for research, data, and argument posts. Start with the surprise, show supporting facts, then explain what readers should reconsider or do.

2. **Changed mind → trigger → updated view → takeaway**  
   Best for thoughtful first-person posts. State the previous view, explain what changed it, then give the new conclusion.

3. **Problem → why it matters → practical response**  
   Best for explainers and operational or policy content. Keep the problem concrete and make the response proportionate.

4. **Result → how it happened → reusable lesson**  
   Best for launches, team outcomes, and approved case studies. The result must be real and specific.

5. **Framework → examples → application**  
   Best for posts readers may save and revisit. Name the framework only if the name genuinely clarifies the idea.

6. **Specific announcement → reader relevance → next step**  
   Use only when the announcement itself is notable. Lead with what happened and its practical significance.

7. **Strategic trade-off → rationale → consequence**  
   Useful for explaining deliberate constraints or “anti-goals”: what an organization has consciously chosen not to optimize for, why, and what that choice enables.

### 4. Draft the body: hook, tension, payoff

Use this default shape:

- **Hook:** The strongest claim, result, or tension.
- **Tension or setup:** Why the point matters, what is surprising, or which assumption it challenges.
- **Payoff:** The evidence, story, framework, or practical insight. The post should still be useful if a reader never opens a link or swipes through an asset.
- **Soft close:** Exactly one focused question, one practical takeaway, or one clear pointer to additional material.

A useful default is under 300 words, but substance and platform norms should determine the final length. Short posts still need to make a complete point. Longer posts need a reason for every paragraph.

Use white space. Write in one- or two-sentence paragraphs so the post is easy to scan on a phone. Use bullets only when the content is genuinely list-shaped, such as three reasons, four findings, or a checklist.

For a carousel or document caption:

- Establish the central idea in the post.
- Include one or two of the strongest specifics.
- State what the visual material adds.
- Do not convert the caption into a slide-by-slide summary.

For a linked article, report, or podcast:

- Put the strongest finding in the body.
- Treat the linked item as depth, sources, or extended analysis.
- Follow the user’s chosen platform strategy for link placement.
- Never make “read the link” the main value proposition.

## Calls to action and questions

Use one close only. A strong close gives readers a real, bounded way to respond.

Good examples:

- “Which of these constraints matters most in your work?”
- “What evidence would change your view?”
- “The full analysis includes the assumptions and source material.”
- “If you have operated this kind of system, where does this model fail?”

Weak examples:

- “Thoughts?”
- “Let me know what you think.”
- Several questions at once.
- Requests to comment, tag, repost, or react merely to boost distribution.

A question should invite knowledge, disagreement, or relevant experience. Do not use engagement bait.

## Editing pass: remove templated and inflated language

Run a separate editing pass after drafting. Cut phrases that sound polished but do not carry meaning.

Replace or remove:

- Inflated corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Hedging frames such as “it is worth noting,” “one might say,” and “arguably,” unless uncertainty is genuinely important.
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Abstract nouns doing the work, such as “journey,” “transformation,” or “paradigm,” when a concrete event can be named.
- Transition sentences that merely repeat the preceding paragraph.
- Dramatic framing such as “The truth is” or “Here is the reality.” State the point directly.
- Decorative punctuation or formatting that the chosen platform will not render correctly.

If the user specifies punctuation preferences, follow them. Otherwise, favor periods, commas, and line breaks over theatrical punctuation. Read the draft aloud. If it sounds like a generic thought-leadership template rather than a person making a specific point, rewrite it.

Use emphasis sparingly. Confirm that bold, italics, bullets, and line breaks render correctly on the intended platform before relying on them.

## Revision protocol

When the user gives feedback, revise the requested line and the nearby logic first. Do not rewrite the entire post unless asked.

Examples:

- If the hook is not sharp enough, provide several replacement hooks before changing the body.
- If a claim feels overstated, tighten the evidence or soften only that claim.
- If a paragraph feels slow, cut setup before adding explanation.
- If the user prefers an earlier sentence, preserve it unless there is a clear reason to change it.

Multiple small options are often more useful than one complete redraft, especially for hooks, closers, and uncertain lines.

Be candid about weak material. For example:

> The second paragraph relies on a broad claim that the source does not yet support. We can add evidence, make it narrower, or replace it with this concrete example: [example].

Do not quietly replace a strong, approved line with weaker generic wording during later revisions.

## Readiness gate and final audit

Do not present a draft as final until it passes this checklist:

- Does the first line earn attention when read on its own?
- Is the post about one clear point rather than several competing ideas?
- Is there at least one concrete detail, outcome, example, number, or mechanism where appropriate?
- Could the main claim be defended if a knowledgeable reader challenged it?
- Does the post provide value without requiring a click, swipe, purchase, or sign-up?
- Is uncertainty stated where it materially affects the conclusion?
- Is the language specific to this topic rather than reusable across any industry?
- Is the close one focused action, question, or pointer?
- Are all names, quotes, figures, and claims approved or supported by source material?
- Are personal details necessary, authorized, and appropriate for the intended audience?
- Does formatting work on the intended platform?
- Does the tone remain professional, respectful, non-inflammatory, and consistent with the user’s purpose?

If any answer is no, revise before handoff.

## Handoff format

When presenting work to the user, provide only what helps them decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen delivery format or location.
3. Any unsupported claim, missing input, permission issue, or line that remains uncertain.
4. Suggested first-comment or link text, if relevant to the platform strategy.
5. A concise publishing reminder appropriate to the platform, such as responding promptly and substantively to genuine early comments.

Do not claim that a particular format, timing tactic, or engagement metric is guaranteed to improve reach. Platform behavior changes frequently. Treat distribution advice as a testable hypothesis and encourage the user to compare outcomes across several comparable posts.

## Common failure patterns

- **Announcement disguised as content:** The post tells readers the organization is pleased, but not why readers should care. Fix it by leading with the actual change or lesson.
- **Pure teaser:** The post asks readers to click but provides no useful insight. Fix it by sharing the main finding and using the linked material for depth.
- **Unsupported precision:** The post uses a striking figure without a source, scope, or caveat. Fix it by verifying, qualifying, or removing it.
- **Generic inspiration:** The post sounds positive but has no mechanism, example, or decision. Fix it by naming the concrete action or trade-off.
- **Overpacked summary:** The post tries to cover every section of a report. Fix it by selecting one thread and saving the rest for the original material or later posts.
- **Bolted-on promotion:** A course, product, or service appears at the end without a natural connection. Fix it by removing the pitch, creating a separate promotional post, or making the connection concrete and immediate.
- **Forced engagement:** The post demands reactions or comments. Fix it by asking one real question or ending with a useful conclusion.
- **Unauthorized personal disclosure:** The post includes a person’s career history, quote, image, or outcome without a clear right to publish it. Fix it by obtaining approval, anonymizing, or removing the detail.
- **Overstated risk:** The post uses severe language while omitting uncertainty, likelihood, mechanisms, or practical responses. Fix it by making the claim narrower and showing the evidence and limits.

The final standard is simple: the post should sound like someone with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, an alarmist prediction, or a generic social-media template.


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
description: Close a month honestly, then create a small, capacity-checked, explicitly approved plan for the next month using evidence, trade-offs, concrete commitments, and a reusable review record.
---

# Review and plan a month

Use this workflow at a month boundary to review the period ending and create an executable plan for the period ahead. A complete session usually takes 45–75 minutes: about half for evidence and review, and half for planning.

Review and planning belong in one session. The structural cause of a missed commitment, energy drain, or delivery problem should directly shape the next plan’s structure.

## Purpose

This workflow produces:

- An evidence-based account of the review month.
- A direct view of progress on active long-range goals and any personal commitment the user includes.
- A compact picture of selected work and life signals, such as focus, sleep, energy, training, or completed work.
- A written **Review** for the ending month.
- A written **Plan** for the next month, with a memorable theme, at most three major outcomes, explicit trade-offs, and a pre-mortem.

Gather, discuss, and save only information that serves one of these outputs.

## When to run it

Run this workflow when the user asks for a monthly review, asks to plan a named month, or asks to close one month and begin another.

Default timing:

- During the first three days of a month, review the prior month and plan the current month.
- Otherwise, review the current month to date and plan the following month. Clearly label the review as partial and state the remaining days.
- If the user requests forward planning only, review first because the evidence should inform the plan. The user may explicitly skip the review.

State the date ranges before proceeding:

> Reviewing **March 2026** (01 Mar–31 Mar). Planning **April 2026**.

Ask whether the user wants calendar-month boundaries or a practical range that includes an overlapping week. Record the actual planning range in the plan.

## Operating rules

1. **Read first; discuss second.** Show the evidence picture before reflective questions.
2. **Batch independent reads.** Gather available independent sources in one initial pass rather than repeatedly interrupting the discussion with small lookups.
3. **Use live commitments.** Assess results against the user’s current target, not a stale schedule, obsolete scope, or old goal record.
4. **Check data quality before a strong verdict.** Missing syncs, delayed updates, and incomplete logs can distort results. Ask the user to confirm surprising evidence.
5. **Use only authorized information.** Access calendars, journals, health data, task systems, or records involving other people only for a legitimate purpose and with clear authorization. Use the minimum relevant dates and fields. Exclude unrelated sensitive details and keep outputs within the appropriate access boundary.
6. **The user chooses.** The assistant calculates, summarizes, identifies constraints, and tests assumptions. The user chooses priorities, cuts, and commitments.
7. **One decision at a time.** Do not advance until the current planning question has a real answer.
8. **Plan at month altitude.** Define outcomes, milestones, capacity, structure, and commitments. Leave detailed weekly task blocks to weekly planning.
9. **Do not save an unapproved plan.** Notes and brainstorms are inputs, not decisions. The user must materially confirm the theme and commitments and explicitly approve the plan.
10. **Use clear dates.** Use **DD MMM** unless the user selects another unambiguous format.
11. **Keep records concise.** Save decisions, evidence, and constraints—not a meeting transcript.
12. **Do not lecture.** For training, health, recovery, or personal practice, provide relevant numbers, a direct conclusion, and the agreed commitment. Offer specialist advice only when requested and appropriate.

## Step 1: Determine the range and gather evidence

Determine the review month, prior comparison month, and planning month. Make one initial batch of reads when connected sources are available.

Use the user’s chosen system: task manager, project tracker, calendar, spreadsheet, notes app, health tracker, training log, or user-provided facts. If no source is connected, ask for a short factual inventory. Never imply that unavailable data was checked.

| Evidence area | Gather in the initial pass |
|---|---|
| Previous monthly record | Theme, promised outcomes, commitments, and prior review findings. |
| Weekly records | Plans and reviews in the review range; repeated blockers, milestones, and carried work. |
| Goals | Active weekly, monthly, quarterly, and annual goals; statuses, deadlines, and notes. |
| Work delivered | Completed tasks, decisions, projects, or deliverables, grouped into useful domains. |
| Calendar | Next-month leave, travel, fixed events, deadlines, recurring commitments, and heavy meeting weeks. |
| Daily signals | User-selected ratings, focus time, habits, or brief journal themes. |
| Sleep and recovery | Optional sleep duration, sleep quality, and same-source recovery trends. |
| Training or practice | Optional sessions from the review and comparison months, plus the current commitment or schedule. |

For large sources, return computed statistics and a few representative themes rather than raw entries. Long journals and full event lists can crowd out the actual review. Use filtered queries, aggregation, summaries, or a narrowly scoped helper where available.

A helper reviewing a calendar, journal, or activity source should use only authorized read access and return a concise summary of fixed multi-day blocks, weekly meeting load, significant recurring commitments, protected personal commitments, and planning anomalies. Do not include unnecessary private details.

Before detailed planning, check weekly plans that overlap the beginning of the planning range. Reference and reconcile them with the monthly plan; do not duplicate or overwrite their detailed commitments.

## Step 2: Show the evidence picture

Present a compact factual picture before asking the user to explain it. Be direct, numeric where useful, and concise.

### Personal-practice, training, or health verdict

Include this section when the user has a current commitment in the area, unless they explicitly put it out of scope. Compare actual activity with the live target. Depending on the domain, calculate:

- Total volume, sessions, repetitions, or practice instances.
- Average weekly volume and number of active days.
- Completion of key sessions or milestones.
- Longest gap between sessions.
- Relevant balance, performance, or recovery measures.
- Change from the prior month.

Use this verdict taxonomy when it fits:

- **ON TRACK:** Key measures meet at least 90% of target and consistency is intact.
- **BEHIND:** A key measure is roughly 60–90% of target, or there was a meaningful consistency break.
- **OFF TRACK:** A key measure is below 60% of target or there was a prolonged gap.
- **AT RISK:** An injury, safety, burnout, or sustained-decline signal makes the current plan unsafe or unlikely.

Adjust thresholds only where the user’s domain needs different ones, and state the adjustment. When tracking may be incomplete, ask: “The record shows this. Does that match reality?” before making a harsh judgment.

State one biggest corrective action for the next month. It must be concrete, but it is not a full program.

### Goals and delivery

Summarize weekly commitments as completed, missed, deferred, or rolled forward. For each active long-range goal, state whether it **advanced**, **stalled**, or **regressed**, with one short reason. Explicitly name goals that received no meaningful attention.

Also summarize completed work in a few useful domains. The question is whether effort created intended progress, not whether the task count was high.

### Life signals

Include only measures the user chooses to track. Useful measures include rating distribution and average, focus hours, low-focus days, sleep duration, sleep quality, recovery trends from a consistent source, and recurring themes in written notes.

Flag meaningful patterns: low average sleep, repeated short nights, several consecutive low-rating days, an extended low-focus period, or a mismatch between positive ratings and notes describing exhaustion or stress. Averages are not the whole picture; raise material contradictions briefly.

## Step 3: Reflect on the month

Open with one specific observation from the evidence. Ask one question at a time and pursue no more than two or three threads unless the user wants more depth.

Cover these questions before closing the review:

1. What genuinely shipped and feels like a win?
2. What cost more time or energy than it returned?
3. Was the main miss structural, circumstantial, or a genuine priority change?
4. What one behavior, boundary, or pattern must change next month?
5. If a personal practice is in scope, what is the concrete next-month commitment?

Useful prompts:

- “This outcome slipped across several weeks. What made it structurally difficult?”
- “Your ratings were stable, but your notes repeatedly mention strain. What was happening?”
- “This goal moved while the others did not. What conditions made that possible?”

For a time-constrained user, the minimum viable review is the in-scope commitment verdict, any material wellbeing flags, one structural fix, and one concrete next-month commitment.

## Step 4: Plan the new month

A plan is not a description of events plus optimistic targets. A real plan has a defined outcome, honest current state, path, proof of capacity, trade-offs, forcing functions, a pre-mortem, and explicit approval.

### Move 1: Define outcomes

For each candidate priority, ask:

> What specifically is true by the final day of this planning range?

Make the answer measurable or plainly verifiable. Limit the plan to three outcomes; one or two is often better. Each outcome should connect to a long-range goal or an explicitly chosen responsibility.

### Move 2: Establish current state

Size the gap with evidence, not mood. Inspect the relevant draft, pipeline, milestone, backlog, baseline metric, or domain-specific reality. If the gap cannot be described, gather the missing evidence before planning the path.

### Move 3: Work backward to build a path

For each outcome, identify three to six moves by reasoning backward from the due date. Each move needs a date or window, an owner, and evidence of completion.

> For this to be true by the end date, what must be true halfway through? What must happen before that?

### Move 4: Do capacity math

Estimate usable focused capacity honestly:

> available working days × recently observed focused hours per day

Account for leave, travel, fixed commitments, and meeting-heavy weeks. Compare this capacity with the effort implied by the paths. If demand exceeds supply, cut, defer, reduce scope, or add real help now.

### Move 5: Make the NOT-doing list

Ask:

> What will explicitly not happen this month so these outcomes can?

The user names the cuts. A plan without genuine exclusions is a wish.

### Move 6: Add forcing functions and protective structure

Fragile outcomes need an external forcing function: a stakeholder expecting a deliverable on a date, a booked review, a public commitment, or a downstream owner waiting on the work.

Protect work that is vulnerable to interruption. Batch flexible, interruption-tolerant work around meetings and reserve the best available blocks for work that needs sustained attention. Resolve calendar conflicts that undermine the plan as immediate actions.

### Move 7: Run a pre-mortem

Ask:

> It is the final day of the month and this plan failed. What happened?

The user answers first. Record the two or three most likely failure modes and a specific counter for each.

### Move 8: Get sign-off

Read the plan back in ten lines or fewer. The user must be able to state the theme and main outcomes from memory, then explicitly approve it.

> Is this the plan?

If approval is vague, revise. Do not save yet.

## Required plan structure

```markdown
## THEME: [MEMORABLE, ACTION-ORIENTED LINE]

**Planning range:** [DD MMM–DD MMM].

## Shape of the month
[Fixed events, leave, travel, heavy weeks, effective working weeks, and immediate post-month constraints.]

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
[Behavior, boundary, or environment change that counters last month’s drain; include tracked delegated work and owners.]

## Personal commitment
[Specific measurable commitment, if in scope.]

## Pre-mortem
- Failure mode: [likely cause]. Counter: [specific response.]
```

## Step 5: Save the review and plan

After explicit sign-off, write two records in the user’s chosen system:

1. A **Review** attached to the ending month.
2. A **Plan** attached to the new month.

Create a missing monthly record if the system supports it. Use one final write operation when practical. Before replacing an existing plan, show the conflict to the user and resolve it.

Use this review template:

```markdown
## Personal-practice, training, or health verdict
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

At the end of every run, make one precise improvement to the reusable workflow, template, or data mapping. Store it in the user’s chosen workflow document or improvement log. If no suitable location exists, present it as a short durable rule for the user to save.

Look for a noisy read, incorrect data assumption, misleading metric, user correction, or repeatable pattern. Prefer one precise edit over a vague reminder.

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
- Overlapping weekly plans were reconciled.
- Any in-scope personal commitment is specific.
- The pre-mortem includes counters.
- The user explicitly approved the plan before it was saved.
- Saved material stays within the selected record and access boundary.

## Common failure modes

- Starting with prompts instead of evidence.
- Judging against stale targets or incomplete data.
- Confusing a list of events with a plan.
- Overloading capacity and refusing to cut scope.
- Letting the assistant choose priorities.
- Saving a draft without explicit approval.
- Conflicting with existing weekly plans.
- Treating averages as more truthful than recurring written evidence.
- Applying generic productivity rituals instead of addressing the actual drain.
- Treating brainstorms, voice notes, or imported task lists as confirmed commitments.
- Reading or preserving unnecessary personal details when a concise summary would suffice.


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
description: Gather authorized meeting context, confirm the meeting owner’s intended outcome before assuming an agenda, and create a practical preparation record with an in-call cheat sheet and appropriate follow-up.
---

# Prepare for a meeting

Use this workflow to prepare for a consequential meeting, a selected set of calendar meetings, or a recurring relationship where context and a clear outcome matter. The deliverable is a durable preparation record in the user’s chosen workspace, not only a chat summary.

Use calendars, communications, documents, records, and transcripts only for a legitimate meeting-related purpose and when the user is authorized to access them. Use the minimum relevant sources and details. Keep the record within the appropriate access boundary, especially if the destination can be viewed by a wider group.

## Outcome

For each selected meeting, create a preparation record containing:

- A concise situation brief that reloads essential context quickly.
- A meeting goal confirmed or corrected by the meeting owner.
- A realistic timed agenda with suggested language, diagnostic questions, and a close.
- Five ranked questions for use during the meeting.
- Essential links, commitments, and follow-up fields.
- A post-call review reminder or automation when the meeting is intended to move a decision or commitment.

## 1. Select meetings and set scope

Establish the date range, meetings to prepare, the user’s time zone, and the destination workspace. If the request is ambiguous, ask which events to include rather than silently choosing.

A useful default is to prepare external one-to-one and small-group meetings while excluding obvious personal holds, focus blocks, travel blocks, and routine internal placeholders. Include an excluded event when it is consequential or the user requests it.

For every selected event, capture:

- Meeting title, date, start and end time, and time zone.
- Attendees and known roles or organizations.
- Location or joining details when useful.
- Invitation description, scheduling notes, and stated purpose.
- Links to relevant documents, prior notes, or other records.
- Signals that the meeting follows an introduction, event, reschedule, request, deadline, or prior commitment.

When preparing multiple meetings, make a short index of included meetings. Flag ambiguous or excluded events and state why they were not prepared.

## 2. Gather authorized context

Research the relationship and meeting topic using the sources available to the user. Parallelize independent searches when practical, but do not collect information merely because it is available. The objective is to understand why the meeting exists, what has already happened, and what needs to happen next—not to create a personal dossier.

### 2.1 Search relationship history

Use the most relevant available sources, normally in this order:

1. **Direct correspondence.** Find messages sent to or received from each external attendee. Read the recent substantive items needed to establish the active thread, commitments, decisions, and unresolved questions.
2. **Name mentions.** Search for the attendee’s name in messages and records, not only direct correspondence. This can reveal introductions, third-party context, earlier requests, or related decisions.
3. **Relevant team discussions.** Search substantive mentions of the attendee or their organization in authorized team channels. Do not copy unrelated personal information into the preparation record.
4. **Prior meeting records.** Find earlier notes, transcripts, action items, and decision logs. Recent transcripts and explicit decision records usually outweigh old summaries.
5. **Calendar history.** Check prior events with the attendee to establish the relationship arc: first contact, recurring cadence, prior purposes, and meaningful changes.

Read the underlying relevant records rather than relying only on search snippets. Separate established facts from attributed views and inferences. For example, “They requested feedback on the draft” is a fact; “They may be seeking endorsement” is an inference to test.

### 2.2 Research public professional context

When it would materially improve the conversation, consult public sources for:

- Current role and organization.
- The organization’s mission, work, product, or operating model.
- Relevant professional background.
- Recent public news, publications, launches, or events.
- Useful professional, organization, or publication links.

Treat public information as context, not proof of private intent. Avoid collecting sensitive details that do not serve the meeting.

### 2.3 Read the artifact the meeting is about

Reading the relevant artifact is mandatory when the meeting concerns a proposal, pitch, strategy, memo, deck, draft, plan, brief, or other substantive written work.

Look for signals such as:

- The invitation mentions feedback, comments, a draft, proposal, or plan.
- Related messages say a document was shared or commented on.
- A document link appears in the invitation or correspondence.
- The meeting refers to a document discussed earlier without providing a link.

Read the full relevant artifact, including meaningful sections, appendices, linked exhibits, and supporting material that carries the argument. If a document has multiple sections or views, inspect each one that may contain substantive content. Do not substitute generic discovery questions for informed preparation when the other party expects a response to a specific document.

If context implies an artifact exists but it cannot be found, ask the user for the link before creating a detailed agenda. Record that the material was unavailable rather than pretending the topic is understood.

### 2.4 Compile a working picture

Synthesize research into a compact working picture.

| Category | What to capture |
|---|---|
| Who they are | Role, organization, relevant background, and current public context. |
| Relationship history | Prior meetings, commitments, introductions, and the relationship arc. |
| Why now | The scheduling trigger, live request, deadline, or decision point. |
| Their organization | What it does and its relevance to the user’s work. |
| Open questions | Missing evidence, uncertain intent, conflicting information, or unavailable materials. |
| Key links | Only links likely to help the user prepare or follow up. |

## 3. Route specialized meetings to the right workflow

Before drafting a general preparation record, determine whether the interaction needs a specialized structure.

For example, an employment reference conversation should use an authorized reference-call workflow rather than a general agenda. That workflow should focus on role-relevant capabilities, observed performance, scope of work, working style, evidence quality, and areas to probe. It should avoid irrelevant personal speculation, protected characteristics, and pay information.

Other interactions may need a dedicated workflow, such as a legal consultation, incident review, formal performance discussion, or negotiation. Preserve the research already gathered and transfer only relevant context so work is not duplicated.

If no specialized route applies, continue.

## 4. Share a situation brief, then ask agenda-shaping questions

Do not move directly from research to a proposed agenda. First share a visible situation brief so the user can reload the context, spot errors, and answer from the same evidence. Then ask targeted questions about choices only the user can make.

### 4.1 Choose a brief format

Use the smallest format that makes the load-bearing context clear.

**Narrative brief** is the default for most meetings. It should take about a minute to read and cover:

- Who the attendee is.
- Where the relationship stands.
- Why the meeting is happening now.
- The live tension, decision, or uncertainty.

**Decision-shaped brief** is better for a negotiation, recruiting conversation, fundraising discussion, close, or another meeting with live alternatives or deadlines. Cover:

- The ask or decision sought.
- Apparent alternatives, constraints, and deadlines.
- The user’s position and sources of leverage or value.
- Risks of moving too hard, moving too softly, or failing to secure a next step.
- Unknowns to diagnose.

These formats can be combined. Use a short narrative first when relationship context matters, followed by a decision section when a live choice is central. For data-heavy meetings, a compact facts table followed by dynamics and open questions may work better.

Choose the format unless the choice itself is consequential and genuinely uncertain. Do not create unnecessary friction by asking the user to choose a format that can be selected from the evidence.

### 4.2 Ask targeted questions

After the brief, ask enough questions to prevent an agenda built on a false assumption. Unless this is a truly routine meeting with a fully documented purpose, ask about the primary goal and at least one of failure mode, tone, or concrete ask. Always include a final catch-all question.

Useful question axes include:

- **Primary outcome:** What should be true by the end of the meeting?
- **Their situation:** Is their interest, authority, role, timing, or constraint unclear?
- **Sensitive substance:** Should the user give a direct view, diagnose first, make a proposal, or hold back?
- **Failure mode:** What would make the meeting go badly?
- **Specific ask:** Is there an introduction, decision, commitment, advice request, artifact, or date to secure? How direct should the user be?
- **Anything else:** What history, constraints, topics to land, or topics to avoid has not been covered?

Use compact labels so the user can answer quickly. Make the first option the evidence-backed recommendation, while offering meaningful alternatives. Do not ask the user to write the agenda; ask about intent, boundaries, and choices that shape it.

```markdown
1. What is the primary outcome?
   - **1a (recommended):** Diagnose their interest and agree a concrete next step.
   - **1b:** Build the relationship without making a direct ask.
   - **1c:** Make a direct proposal and seek a decision.

2. What should be avoided?
   - **2a (recommended):** Do not commit before understanding their constraints.
   - **2b:** Do not let the discussion remain exploratory; secure an owner and date.
   - **2c:** Keep the meeting informational and avoid a close.

3. Is there anything else to land or avoid?
   - **3a (recommended):** Nothing to add.
   - **3b:** I will add notes or context.
   - **3c:** There is a sensitive topic to handle carefully.

Reply with labels, for example: 1b, 2a, 3c.
```

Ask up to about six questions only when each answer materially changes the agenda. If the chosen interaction method limits questions per round, use multiple rounds and let earlier answers tailor later choices. Keep labels sequential across rounds. Do not force a false either/or when two approaches can sensibly combine; offer a combined option where useful.

Before sending, verify that every question is numbered, every option has one unique label, labels are sequential, and the final catch-all question is present.

## 5. Create the meeting-preparation record

After receiving the user’s answers, create or update the preparation record in the user’s chosen workspace. If the workspace is broadly visible, omit sensitive business details and personal information that do not need to be shared.

Use a date-only field when the system supports one. Store meeting time separately only when needed for scheduling. Title the record with the date and participant or topic. Include attendees only when appropriate for the record’s access level.

Use this structure, adapting time blocks to the actual meeting duration:

```markdown
# [Date] — [Participant or meeting topic]

## Context

- Who they are and what their organization does.
- Relationship history and previous commitments.
- Why this meeting is happening now.
- Relevant links and the meeting artifact, if any.
- State explicitly if this is the first meeting.

## Goal

[User-confirmed outcome for this meeting.]

## Agenda

### 0–5 min: Open and frame

**Say**

[Brief opener that establishes purpose and intended use of the time.]

**Interviewer note**

[What to avoid or establish before moving on.]

### 5–20 min: Diagnose [topic]

**Questions**

1. [Decision-relevant question.]
2. [Question that tests the key uncertainty.]

**Interviewer note**

[Signals to listen for, assumptions to test, and important follow-ups.]

### 20–35 min: Discuss, pressure-test, or propose [topic]

**Say**

[Transition or concise position statement.]

**Questions**

1. [Question that tests feasibility, alignment, or the gap between current and desired state.]

**Interviewer note**

[Specific trade-offs, evidence, or commitments to surface.]

### 35–45 min: Close and create a forcing function

**Question**

1. [Specific next-step question: owner, artifact, decision date, or follow-up meeting.]

**Interviewer note**

[Backup close if a decision cannot be made now.]

## Five most important questions to ask

1. [Most decision-relevant question.]
2. [Second-highest uncertainty to resolve.]
3. [Question that tests the central constraint or gap.]
4. [Question that establishes ownership, authority, or feasibility.]
5. [Specific close for a date, artifact, decision, or next step.]

## Follow-up to capture

- Decision:
- Owner:
- Deliverable or artifact:
- Due date:
- Next meeting or check-in:

## Timely note

[Optional: a relevant recent publication, event, or announcement.]
```

Put the highest-value topic before background, status updates, or rapport-building. Compress stages for short meetings rather than retaining nominal time ranges. For recurring contacts, summarize the relationship arc rather than only the most recent interaction.

Write practical preparation, not generic notes. Use concise suggested language under **Say**, spoken questions under **Questions**, and compact private guidance under **Interviewer note**. Do not put spoken prompts in quotation marks or nest lists under agenda stages.

The five-question section is a five-second in-call cheat sheet. It must contain exactly five ranked, one-line questions. When a next step matters, include a forcing-function close; do not fill the list with generic discovery questions when the meeting hinges on a specific decision.

## 6. Use a decision-moving lens when appropriate

For a recruiting, sales, partnership, fundraising, negotiation, or other persuasion-oriented meeting, prepare to identify and address the gap between the other party’s current state and desired state.

The agenda should help the user:

1. Establish the current situation and constraints.
2. Surface the cost, risk, or missed opportunity of remaining there.
3. Clarify the desired future state and conditions for success.
4. Test whether the user’s proposal materially helps close the gap.
5. Secure a concrete next action that preserves momentum.

Do not force this lens onto a purely informational meeting. When no decision or commitment is sought, prioritize learning, relationship-building, and accurate follow-up instead.

For a high-stakes decision-moving meeting, schedule a one-time post-call review about an hour after the meeting ends when the user has approved an appropriate task or automation capability. The review should retrieve authorized notes or transcript material, compare the conversation with the preparation record and any relevant playbook, record evidence and commitments, identify repeatable strengths and improvement patterns, and confirm follow-up owners and dates. Store review material only in an appropriately restricted location.

## 7. Verify and communicate completion

Before finishing, verify that the saved record has the correct date, title, appropriate attendees, context, goal, timed agenda, five-question cheat sheet, and useful links. Repair formatting or field errors before declaring completion.

Open the record in the user’s selected preparation environment when supported, especially if it will be used for live notes or transcription. For multiple meetings, open each record or provide a clear index.

Tell the user what was created, which meetings were prepared, what material could not be found, and whether a post-call review was scheduled.

## Privacy and quality gate

Before saving or sharing, confirm:

- The research purpose was legitimate and the user had access authorization.
- Only meeting-relevant communications and records were used.
- Unrelated sensitive personal details were omitted.
- Confidential information is stored only in an appropriate restricted location.
- The agenda reflects the user’s answers rather than unsupported assumptions.
- The agenda fits the meeting duration.
- The relevant artifact was read, or its absence was surfaced.
- The close establishes an appropriate next step when one is needed.
- No salary, compensation, equity, offer value, compensation band, or other pay figure appears in a broadly visible meeting record. If necessary, refer only to a restricted compensation discussion without numbers.

## Common failure modes

Avoid these mistakes:

- Researching attendees but not reading the proposal, deck, memo, or other artifact that is the reason for the meeting.
- Drafting an agenda before confirming the user’s goal, stance, and key risk.
- Treating search snippets as evidence instead of reading the relevant message thread or record.
- Using generic discovery questions when the meeting centers on a specific document, decision, or negotiation.
- Ending without a concrete next step when momentum matters.
- Saving confidential, sensitive, or pay-related information in a workspace visible beyond those who need it.
- Providing a chat summary while failing to create the durable preparation record.


---
name: capture-meeting-actions
description: Review authorized meeting records, identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Authorization and privacy boundary

Use this workflow only for a legitimate work purpose and with clear authorization to access the selected meeting records and task system. Use the minimum sources needed to determine commitments. Do not copy unrelated personal details, sensitive discussion, health information, compensation details, or private assessments into tasks unless they are necessary for the action and appropriate for everyone with access to that task.

Keep task notes within the access boundary of the source material. If a follow-up requires sensitive context, record only the practical next action and link to an access-controlled source where appropriate. Respect consent expectations when drafting introductions, sharing contact details, or following up after personal conversations.

## Purpose and operating rules

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

Apply known delegation boundaries supplied by the user or organization. Attendance at a meeting does not make the user accountable for every workstream discussed.

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
- Relevant source and related links.

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
- **Priority:** use the user’s scale; default to important normal work and reserve the highest level for a real deadline, material risk, or waiting counterparty.
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
- Each task links to its source record where appropriate.
- Message drafts are ready to send and follow the user’s preferences.
- Task content respects the source access boundary and omits unnecessary sensitive details.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report the essential outcome only: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and any reusable guidance changes. Keep status updates terse and factual.


---
name: turn-a-message-into-a-task
description: Read a message or conversation, identify the real remaining action, research only the context needed, and pre-complete as much work as is safe before deciding whether a task record is useful.
---

# Turn a message into a task

Use this workflow when one or more message links, emails, chat threads, or conversation records may contain work that should be tracked. The goal is not to copy a message into a task list. The goal is to understand the real request, complete the safe preparatory work, and leave the user with a small, clear remaining action.

This workflow applies only when there is a legitimate purpose and clear authorization to access the conversation and any supporting records. Use the minimum relevant sources and facts. Do not include unrelated private information, sensitive personal details, or material outside the intended audience's access boundary.

## Operating principles

- Read the full relevant conversation before interpreting the request.
- Treat a linked reply as an anchor, not necessarily the complete task.
- Check for newer replies that may resolve, supersede, reassign, or cancel the work.
- Research selectively. A few primary sources read carefully are better than many shallow searches.
- Draft rather than send. Do not send messages, emails, invitations, approvals, or other external actions without explicit authorization.
- Prefer a self-contained deliverable over a bare reminder.
- Ask the user only when a missing decision would materially change the work.
- Do not create a task merely because a message was supplied.

## 1. Read and normalize the conversation

Open the referenced message and, where permitted, its parent message and all thread replies. If the system represents replies separately, retrieve the parent and the entire thread rather than relying on a narrow time window or a single result.

Capture the following in working notes:

- Who is involved, including the requester, intended owner, and anyone waiting.
- The exact ask, promises made, decisions already recorded, and implied deliverables.
- Dates, deadlines, waiting conditions, linked documents, and named processes.
- Whether the linked message is part of a broader thread.
- Whether a later message shows that the work is already complete, no longer needed, or now owned by someone else.

Resolve identities from authorized directory information or unambiguous mentions when the message display name is absent. Do not refer vaguely to “the person” in a task if a role or permitted name is available. If identity is genuinely unclear, use a neutral role description such as “project requester” and flag the ambiguity.

### Recency gate

Before creating anything, compare the linked message with later replies. If the request appears completed, closed, withdrawn, or reassigned, do not create a task record. Report the evidence and ask whether the user still wants follow-up only if there is a plausible remaining need.

## 2. Define the actual task

State the task shape explicitly in your working notes. This determines what useful pre-completion looks like.

| Task shape | Usual remaining deliverable |
|---|---|
| Reply owed | A concise draft reply that answers the request or moves it forward. |
| Artefact owed | A draft document, reference, introduction, data extract, plan, or other requested item. |
| Decision needed | A short decision brief with options, evidence, recommendation, and a draft response for the likely decision. |
| Delegation or follow-up | A drafted chase, handoff, scheduling request, or prepared action in the user-selected system. |
| Multi-part request | One coordinated task with clearly separated sub-parts, unless owners or timelines genuinely differ. |

Rewrite the task as an outcome, not as a message label. For example, prefer “Review and send the project update” over “Message from project channel.”

Default to one task for a multi-part request when one person owns it and the parts share a timeline. Split it only when separate ownership, deadlines, or waiting states would make a combined record confusing.

## 3. Gather only the needed context

Choose sources based on the question. Do not run a blanket search across every connected system.

Typical source choices include:

- **People or working relationships:** authorized prior correspondence, meeting notes, work records, role-relevant feedback, and prior plans or talking points written by the user.
- **Projects or events:** recent project conversation, project documentation, planning notes, and materials linked from the thread.
- **Data questions:** the system of record, approved reports, retrospectives, event documentation, and source correspondence that contains hard facts.
- **Repeated asks:** a broader topic search may reveal parallel questions or an already-prepared answer. Reuse a verified answer where appropriate rather than creating duplicate work.
- **Linked files:** open and read relevant linked material. For multi-section documents, inspect all tabs, sections, or pages before assuming the message captures every requested decision.
- **Policy or process questions:** consult the organization’s authoritative policy and the applicable jurisdiction, team, or program guidance. Do not assume precedent transfers without checking whether the context differs.

For public factual research, use tools that retrieve content without taking visible actions or altering accounts. Do not use browser automation, log in to new services, or access personal records unless authorization explicitly covers that activity.

Stop research when you can either complete the preparation or precisely name the blocker. Mark uncertain facts rather than inventing them. Never guess a URL, date, amount, policy rule, or attribution. Verify it, omit it, or add a clear marker such as `[VERIFY: confirm current deadline]` or `[SEARCH: official policy page]`.

## 4. Pre-complete the work

Do as much of the task as is reasonable and safe. A useful record contains the actual draft, brief, calculation, outline, or prepared next action, not just a reminder that work exists.

### Writing in the user’s voice

If drafting text that will appear to come from the user, first consult any user-provided writing preferences, examples, or style guide that you are authorized to use. If none exists, use plain, concise, respectful language and avoid making claims about personal views that the user has not supported.

Keep drafts shorter than an internal analysis. Remove unnecessary setup, repeated praise, and elaborate checklists unless coaching or detailed explanation is the purpose of the response. Ask the simplest question that would unlock progress. Make future commitments conditional when they are not guaranteed.

Use the formatting conventions of the destination system. For example, leave an empty line before a list if the system needs it to render as a true list. Do not add stylistic lead-ins that make a short reply longer without adding meaning.

### Drafting rules

- Draft; do not send.
- If supported and authorized, stage a reply as a draft in the original thread or selected communication system.
- Put the same draft in the task notes so the record remains useful even if the staged draft is unavailable.
- Preserve clear placeholders for facts or judgment only the user can provide: `[FILL IN: your firsthand observation]`.
- Warn clearly if a draft cannot be sent as written because it contains placeholders.
- For decisions, present two or three viable options, evidence for each, and a recommendation with reasons. Do not provide a neutral list when a recommendation is possible.
- For approvals, route the request through the organization’s documented process rather than implying an informal approval is sufficient.

Separate what can be responsibly prepared from what requires the user’s judgment, memory, relationship knowledge, authority, or consent.

## 5. Ask questions only at a real decision point

Before asking, check whether the answer already exists in the conversation, prior user-authored notes, authorized correspondence, or an applicable decision record. A documented user stance is stronger than a new question.

Ask questions only when a wrong assumption would cost more time or create more risk than interrupting the user. If needed, ask two to four targeted questions. Precede them with a short context recap covering:

1. who is involved and what happened so far;
2. what is being requested now;
3. the relevant tension, trade-off, or missing decision; and
4. what each answer would change in the draft or next action.

Allow combined answers and free-text responses when the interface supports them. Avoid false either-or choices. If no meaningful fork exists, make reasonable metadata assumptions, state them in the final report, and let the user correct them later.

## 6. Decide whether a task record is needed

Skip task creation when the item is already complete, duplicated, cancelled, or can be finished in one short sitting with no meaningful wait or risk of being forgotten. For example, if the only remaining step is to review a ready-to-send draft and send it, a chat deliverable may be more useful than a record.

Create a task record when one or more of the following is true:

- Work is deferred or cannot appropriately happen now.
- A deadline, waiting condition, event, or dependency needs tracking.
- Multiple remaining steps span more than one sitting or more than one day.
- Ownership or handoff needs to be visible.
- The user explicitly requested a task record.

When uncertain, prefer chat-only delivery for a simple reply draft and a record for longer-lived work.

## 7. Create a high-quality task record

Use the user’s chosen task system and its available fields. Do not assume a particular product, database, taxonomy, or URL structure.

Set a specific imperative title, a clear status, an actual or inferred due date only when justified, and an estimate for the **remaining human effort**, not the research already completed. Select the closest user-approved domain, project, or category. If no category fits, use a neutral general category or leave it unclassified according to the system’s conventions.

Use this notes template:

```markdown
**What:** [One sentence: the request, intended outcome, and who is waiting.]
**Source:** [Link or reference to the original conversation.]
**Context:**
- [Relevant history or role context.]
- [Verified fact, dependency, or deadline.]
- [Link to an authorized supporting source, if useful.]

**Pre-completed:**
[Full draft reply, decision brief, outline, calculation, or prepared handoff. State where a communication draft was staged, if applicable.]

**Remaining for the user:**
- [Specific decision, edit, approval, or action.]
- [Specific follow-up, only if needed.]
```

After creation, verify that the record contains the intended title, notes, date, estimate, and links. Open or retrieve the created record when the system permits, so errors are caught immediately.

## 8. Report back clearly

If a task record was created, report in this order:

1. What the task is.
2. What was pre-completed and where any draft was staged.
3. The metadata assumptions: priority, urgency, due date, category, and remaining estimate.
4. Any `[VERIFY]` or `[FILL IN]` items that prevent final use.

If no task record was needed, separate briefing from deliverable exactly and place the draft last:

```markdown
## Context for the user (not part of the reply)
- [What is being asked and who is waiting.]
- [Key verified context and judgment calls.]
- [Where the draft is staged, if applicable.]
- [Any VERIFY or FILL IN warnings.]

## The reply
[Draft reply verbatim.]
```

Do not add commentary after the draft block. This keeps the draft easy to copy or use directly.

## 9. Optional draft review loop

When a draft is staged, an authorized follow-up check can compare the eventual sent message with the draft. Check only within the relevant conversation and only for the minimum period needed. If no message has been sent, reschedule a limited number of increasingly spaced checks, then stop.

Capture only reusable, non-sensitive lessons: preferred brevity, formatting, approval routing, common process steps, or recurring decision criteria. Do not store personal gossip, sensitive relationship judgments, or detailed private correspondence as style guidance.

## 10. Audit checklist and failure modes

Before finishing, check:

- Did I read the full thread and later replies?
- Is this work still active and owned by the intended user?
- Did I use only authorized, relevant information?
- Did I research enough to prepare the deliverable, but not excessively?
- Does the record contain useful pre-completed work?
- Are all uncertain facts clearly marked rather than fabricated?
- Did I avoid sending or otherwise committing an external action?
- Is the remaining user action specific and appropriately small?

Common failures are creating dead tasks, copying a message without understanding it, researching broadly without purpose, asking questions already answered in records, inventing facts to make a draft look complete, burying the draft under commentary, and tracking a trivial one-click action in a task system. Correct these by returning to the relevant gate in this workflow rather than adding more process.


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
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and privacy, verifying rendered page state, and separating preparation from consequential final actions.
---

# Use a browser safely

Use this workflow for tasks that require interacting with a website: completing rendered forms, changing dashboard settings, collecting information from dynamic pages, testing a user flow, or working in an authenticated account. Use it when a simple page request, supported service interface, or static-page retrieval cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not perform a consequential final action until the account, target, page state, and authorization are clear.

A browser automation command completing without an error does **not** prove that a website accepted the change. Modern web applications can maintain internal state separately from the visible DOM, commit values only after focus changes, replace controls while rendering, or show an error even though an action succeeded.

## 1. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can perform the requested task. It is often more reliable than imitating browser interactions.
2. **Headless browser automation.** Use this for public pages, test environments, routine dynamic-page extraction, screenshots, UI testing, and forms that do not require the user's established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely needs an existing signed-in session, single sign-on state, account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for a direct route. Check official documentation, ordinary form actions, page source, and visible network requests for supported endpoints. A form may submit structured data to an authorized service that is safer and more robust to use directly.

Do not use undocumented endpoints to bypass access controls, consent boundaries, service restrictions, or other protections. Do not use an authenticated visible session merely because it is convenient: it can interrupt the user's work and creates greater privacy and account risk.

If a site blocks automated browsing, do not attempt to evade its protections for casual research or collection. A user-visible browser session may be appropriate only when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and the established session is necessary. Do not weaken browser security, access controls, warnings, or anti-abuse protections.

### Select an automation implementation deliberately

Use the browser automation capability best suited to the task. A lightweight interactive automation service can be suitable for a single click, a short page reading task, or a small flow. For long text, complex client-rendered pages, repeated form work, or operations that need reliable sequencing, use a direct script with a mature browser automation library.

Use a headless launch by default. A visible browser is an exception that must be announced and justified by the need for the user's signed-in context. Do not open a visible window unexpectedly.

If an automation session becomes unstable during a complex operation, do not blindly attempt to rescue it. Restart the work through a more reliable method, re-inspect the page, and verify the state before continuing.

## 2. Protect account identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, confirm that it has a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into notes, screenshots, logs, or reports. Keep results within the requester's appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated context, identify the correct account, organization, environment, and browser profile. Never infer identity from a generic browser-window name, an old tab title, a remembered default, or an arbitrary browser connection label.

Use these rules:

- Announce when taking control of a visible browser and state the purpose. For example: “I am opening the authenticated browser to update the requested account setting.”
- Work in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Classify the intended context explicitly: for example, personal, work, testing, staging, or production.
- Select the browser profile or connected session that corresponds to that context instead of relying on a generic browser selector.
- Confirm the signed-in account using a reliable account indicator before opening or changing the real target.
- Confirm the environment separately from the account. A valid account may still be connected to the wrong workspace or to a test environment.
- If the required account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not reveal credentials, session tokens, recovery information, private account data, or security settings in output or logs.
- Do not disable security controls, multi-factor authentication, browser warnings, or access restrictions to make automation easier.

Use an account preflight gate before actions that change data. Confirm the account identity, environment, and target object. If the automation system has a verification marker or permission gate, enable it **only after** the account check has actually passed. Never create a marker in advance merely to unlock actions.

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

If the page reloads, re-renders, or the session changes between passes, do not assume the earlier state remains valid. Restore intended values if necessary and verify them again before committing.

## 4. Inspect the rendered page before editing

Do not start by guessing selectors, filling fields by numeric position, or trusting a visual approximation. First inspect the rendered page and collect enough structure to identify controls safely.

For each relevant field, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or label relationship.
- Current value and whether the field is required.
- Validation rules, character limits, formatting behavior, and disabled state.
- Whether an apparent field is the editable control, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, date, tab, or other control causes the page to re-render.

Address controls by stable semantic identity, such as visible label text, an accessible name, or an explicit label relationship. Do not use DOM indexes where labels are available: dynamic applications can change element order between page loads or after re-rendering.

Before changing a record or setting, inspect its current state. This prevents modifying the wrong item or overwriting existing values unintentionally.

### Generic form inspection pattern

Use a page-inspection capability to list relevant controls before writing fill logic. The exact automation library is user-selected, but inspection should record at least tag, input type, role, label, required state, and current value or text length.

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

## 5. Use the correct input method for each control

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

For framework-driven editors, simulate normal user interaction rather than writing directly to low-level page properties. A robust general sequence is: focus the actual editable element, select existing text, delete it, enter the new text with keyboard-style events, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible rich-text editor with a hidden input. Editing the hidden input may appear successful in a DOM dump while server-side validation treats the visible editor as empty. Target the control that the user interacts with and that the application actually reads. If a generic accessibility locator points to an empty wrapper, inspect the underlying editable element and follow its label relationship.

If changing a dropdown, checkbox, tab, or date can refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterwards and confirm that earlier entries remain present.

## 6. Verify after every meaningful edit

After each field is filled or setting is changed, read its value back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare lengths, required state, or a minimal redacted summary rather than exposing the full value unnecessarily.

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
| Automation reports success but the field is blank | The application ignored a direct value change. | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after editing a later one | A component re-render reset uncommitted state. | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used. | Find a multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node. | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited. | Use the visible interactive control that the application actually reads. |
| Automation becomes unstable on a complex page | The chosen automation layer is unsuitable. | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and normal browsers show different behavior | The site varies behavior by browser context. | Prefer an authorized direct interface; if needed for an explicit task, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior. | Close it through a neutral page action and re-verify affected fields. |
| A visible error may be cosmetic | The task may already have completed. | Inspect resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## 11. Maintain a reusable, privacy-safe run record

When a meaningful failure or new reliable interaction pattern occurs, record the lesson in a shared, approved workflow reference or run log. Record the general symptom, likely cause, and tested recovery. Do not preserve personal data, account identities, credentials, unique records, or unnecessary screenshots.

Keep the reference concise by consolidating related incidents into general rules. Update stale implementation assumptions, such as browser-library behavior or available capabilities, in place rather than layering conflicting historical notes over the workflow.

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
description: A complete, tool-independent workflow for designing, testing, improving, evaluating, and packaging reusable AI skills from new ideas, existing instructions, or demonstrated workflows. It supports lightweight collaboration as well as rigor.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, revise an existing skill, assess whether a skill improves results, or improve when a skill activates. A skill is a focused set of instructions, with optional resources, that helps an AI perform a recurring job more consistently.

The core improvement loop is:

1. Define the job and its boundaries.
2. Draft or revise the skill.
3. Test it using realistic requests.
4. Review outputs with the user and measure objective requirements when appropriate.
5. Improve the instructions based on evidence.
6. Repeat until the skill is useful, reliable, and not narrowly fitted to the test examples.
7. Optionally improve the skill description so it activates for the right requests.

Adapt the level of rigor to the user’s needs. A user may want a quick collaborative draft, a small sanity check, or a structured benchmark. First identify where they are in the loop, then help them take the next useful step. Do not insist on formal testing when the user explicitly prefers an exploratory or informal approach, but explain what confidence they give up by skipping it.

## Communication principles

Match the user’s technical level and preferred vocabulary. Use plain language by default. Words such as *evaluation* and *benchmark* are often understandable, but define them briefly if helpful. Avoid unexplained terms such as “schema,” “assertion,” or “JSON” unless the user has signaled familiarity or asks for implementation detail.

Explain why key questions matter. For example:

> What should a successful result look like: a chat response, a structured report, a file, or an approved action? The answer determines how the skill should work and how we can check it.

Keep the user involved in consequential decisions:

- Confirm the intended job before writing extensive instructions.
- Ask before imposing strict scope, a tool dependency, or an approval requirement not already required by the task.
- Share proposed test cases before treating them as the test suite.
- Let human judgment lead for subjective qualities such as tone, visual design, creative value, and strategic usefulness.
- State uncertainties rather than presenting assumptions as facts.

## 1. Determine the starting point

Identify which of these situations applies.

### New skill

The user has an idea for a recurring capability, such as preparing consistent project updates. Begin with discovery, scope, and a first draft.

### Existing skill

The user already has a skill and wants to edit, simplify, test, repair, or optimize it. Read the current instructions before proposing changes. Preserve its established name and identity unless the user explicitly asks to rename it. If the installed copy cannot be edited directly, work from an authorized writable copy and keep the original unchanged.

### Workflow already demonstrated

The user may say, “Turn what we just did into a skill.” Extract as much as possible from the conversation before asking questions:

- Inputs and reference materials provided.
- Approved tools, sources, or capabilities used.
- Sequence of decisions and actions.
- Corrections and preferences expressed by the user.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow and list missing details for confirmation. Do not convert a one-time workaround into a permanent rule without checking whether it applies broadly.

### Evaluation or activation request

The user may have a finished-looking skill and ask whether it works, whether a revision is better, or whether it triggers at suitable times. Start with test design and evidence gathering. Do not rewrite a skill merely because rewriting is possible.

## 2. Capture intent, scope, and authorization

Before drafting, collect enough information to define a coherent job. Ask only the questions that are still materially unclear, but cover these areas as needed:

1. **Purpose:** What should the skill enable the AI to accomplish?
2. **Activation:** What user requests, wording, or contexts should make the skill relevant?
3. **Inputs:** What files, systems, examples, sources, and permissions can it use?
4. **Outputs:** What should it produce, change, recommend, or hand back? Is a format required?
5. **Success:** How will the user decide that the output is correct, useful, safe, and complete?
6. **Boundaries:** What should the skill not do? When should it ask, stop, or offer alternatives?
7. **Variation:** What common cases, difficult cases, exceptions, or failure conditions matter?
8. **Dependencies:** Does it require user-selected capabilities, templates, references, scripts, or domain standards?
9. **Testing:** Should it be tested with representative requests before release?

Offer useful choices when they reduce ambiguity:

- “Should the skill make a clearly labeled best-effort draft when information is missing, or pause and ask for the missing information?”
- “Should it use a concise default, a detailed default, or let the user choose?”
- “Should it use any source the user supplies, or only approved sources of record?”

### Private information and access boundaries

If the skill uses private communications, records, files, or information about people, confirm a legitimate purpose and clear authorization before accessing or processing them. Use only the minimum relevant sources and data. Omit unrelated sensitive details from outputs, respect consent and reasonable privacy expectations, and keep the result within the requester’s appropriate access boundary.

For a people-related workflow, focus on role-relevant facts, evidence, and outcomes. Do not infer sensitive attributes or make claims beyond the available evidence. For hiring or assessment, describe role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance.

### Research before drafting

When approved documentation, relevant examples, standards, or comparable skills are available, review them before drafting. Research should reduce burden on the user, not override the user’s requirements.

Use research to identify:

- Existing conventions and output standards.
- Constraints from a file type, system, or user-selected capability.
- Reusable patterns for comparable jobs.
- Safety, privacy, compliance, and approval requirements.

If sources conflict, are incomplete, or cannot be verified, explain the uncertainty and ask the user to choose where necessary.

## 3. Choose a maintainable skill structure

A skill should be focused enough that users and the AI can predict what it does. It may support several variants of the same job, but separate unrelated jobs when they differ in audience, authority, sources of truth, or definition of completion.

A typical portable package can contain:

```text
skill-name/
├── SKILL.md              # Core instructions
├── scripts/              # Optional repeatable helpers
├── references/           # Optional supporting documentation
├── assets/               # Optional templates or output resources
└── evals/                # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata or description:** A short statement that helps determine when the skill applies.
2. **Core instructions:** The workflow needed for ordinary use.
3. **Supporting resources:** Detailed references, templates, or scripts consulted only when relevant.

Keep core instructions readable and reasonably compact. If they grow too large, move specialized material into clearly named files and state exactly when to consult each file. Give long references a table of contents or clear navigation.

For multiple variants, place selection logic in the main instructions and variant details in separate resources. For example, a deployment skill could select the appropriate hosting environment first, then read only the matching reference rather than loading every provider’s instructions.

### Bundle deterministic work only when justified

If several test runs independently reconstruct the same helper procedure, consider bundling a script or template. Good candidates include repeatable file transformations, validation, report assembly, data cleanup, or calculations.

Add a resource only when it is reusable, easier to verify than repeated free-form reasoning, safer or less error-prone, and within the intended authorization boundary. Document its inputs, outputs, limits, and when not to use it. Do not automate actions that users would find surprising or that require ungranted access.

## 4. Write the skill

Write in clear, imperative language. Explain the reason behind instructions that prevent predictable failures. AI systems can often adapt better when they understand the goal and tradeoff than when they receive a long list of unexplained commands.

Include the following sections when applicable.

### Purpose and scope

State the job, intended outcome, normal users, and boundaries. Make clear whether the skill produces advice, a file, a report, an external action, or a guided process.

### Inputs and prerequisites

List required information, permitted sources, necessary capabilities, and optional inputs. State what to do when something required is unavailable.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask the user for an export or provide a draft clearly labeled as incomplete.
```

### Workflow

Describe the normal sequence, including meaningful decision points rather than attempting to enumerate every possible incident.

A durable sequence is often:

1. Inspect the request and available inputs.
2. Clarify requirements only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Complete the requested task using an appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result, assumptions, evidence, and unresolved limits.

Use conditional instructions where useful:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested change could overwrite important work or cause an external effect, describe the impact and request confirmation before proceeding.
```

### Output format

When consistency matters, provide an exact or near-exact format:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or required follow-up]
```

Avoid rigid templates when quality depends on adaptation to context. In those cases, specify the intended audience, required content, and quality goals instead.

### Quality, safety, and privacy checks

State the checks needed before completion. Examples include required fields, calculation verification, source attribution, preserving originals, flagging uncertainty, and confirmation before high-impact actions.

The skill must act in ways a user would reasonably expect from its description. Do not design skills that hide actions, bypass authorization, expose confidential information, damage systems, or facilitate unauthorized access. If the requested work is deceptive, unsafe, or beyond the requester’s authority, explain the limitation and offer a safe alternative when possible.

### Failure behavior

Describe broad recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable tool or reference:** Explain what could not be verified and offer an approved alternative.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially change the outcome; otherwise ask.
- **Validation failure:** Do not describe the output as complete. Correct it, report the issue, or seek guidance.
- **Permission-sensitive action:** Pause for confirmation before irreversible, external, financial, legal, or otherwise high-impact actions.

### Examples

Include a small number of generalized examples only when each teaches a distinct pattern. Examples should illustrate good reasoning and output shape, not replace the workflow with a collection of narrow cases.

## 5. Write a strong activation description

The description is a routing instruction. It should say both **what the skill does** and **when it should be used**. Cover realistic language users may use, including requests that imply the task without naming it directly.

A useful description includes:

- The outcome or job.
- Common contexts or phrases that indicate relevance.
- Important scope limits that prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use for requests for progress summaries, leadership updates, milestone reviews, risks, decisions, or next steps, including requests that imply a status report without using that phrase.
```

Do not put the full procedure in the description. Avoid vague labels such as “help with documents,” and do not make the description so broad that it captures nearby work better served by another skill.

## 6. Audit the draft before testing

Read the draft as a new user and a new AI would. Check:

- Is the job coherent and bounded?
- Does the description clearly indicate when it applies?
- Are inputs, authority, permissions, and outputs clear?
- Does the workflow explain why important checks exist?
- Does it handle missing information and unavailable dependencies?
- Does it rely on private conventions, undeclared tools, or personal access?
- Are rules redundant, brittle, or overly restrictive?
- Does a capable AI have room to adapt to ordinary variation?

Prefer lean instructions over long instruction files filled with rules that do not change results. Repeated absolute wording is a warning sign unless the behavior is genuinely non-negotiable, such as respecting authorization or preserving confidential information.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user before relying on them and invite additions or corrections.

For each test, record:

- A descriptive identifier.
- The user prompt.
- Input files or supplied context.
- Expected outcome in plain language.
- Objective checks, if suitable.

A portable test structure is:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "missing-source-handling",
      "prompt": "Prepare a weekly summary from the attached updates and identify information that cannot be verified.",
      "expected_output": "A structured summary that separates supported updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover meaningful conditions, such as:

- A typical successful request.
- Incomplete or ambiguous information.
- A format-sensitive or rule-sensitive request.
- A realistic case that changes the workflow.
- A request that should require approval, cautious handling, or refusal, when relevant.

Vary wording, detail level, and user style. Do not make tests merely repeat the skill’s own language. Avoid retaining personal scenarios or sensitive source material when generalized examples can test the same behavior.

## 8. Run fair comparisons

When independent execution is available, compare the skill with a meaningful baseline.

- For a new skill, compare a run using the skill with a comparable run without it.
- For an existing skill, preserve an unchanged authorized snapshot before editing, then compare the revised version with the prior version.

Run both conditions under comparable circumstances. When possible, start all skill and baseline runs together to reduce timing differences. Keep each iteration separate, for example:

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

Preserve the prompt, supplied inputs, output, and available metadata such as elapsed time and resource use. Record timing when the execution environment reports it because it may not remain available later.

If independent runs are unavailable, conduct a transparent sanity check: follow the skill for each test prompt, save the results, and ask the user to review them. Do not present this as a rigorous baseline comparison.

## 9. Define and grade objective checks

While tests are running, draft objective checks when they genuinely measure user value. Explain them before treating them as success criteria.

Good checks are observable and meaningful:

- Required sections are present.
- A generated file opens and has required fields.
- Calculations match an agreed source within a defined tolerance.
- Missing mandatory inputs are identified.
- Important claims include source references when required.

Record each check with clear text, pass/fail status, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when information is incomplete.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests follow-up."
    }
  ]
}
```

Use programmatic validation where practical. Automated checks are repeatable and can be reused across iterations. Do not force numerical scoring onto subjective work; writing quality, judgment, tone, and design often require human review.

## 10. Review results with the user

Present qualitative outputs and quantitative results together. Use any available review method that lets the user inspect each prompt, supplied context, output, comparison output, grades, and available timing data. If no review interface exists, present accessible files or a clear conversational review.

Ask focused questions:

- Which result would you trust in ordinary use, and why?
- What was missing, misleading, too costly, or difficult to use?
- Did the skill add work that did not create value?
- Would the result work for similar requests with different wording or data?

Empty feedback can mean a tested case is acceptable, but it does not prove the skill is generally solved. Consider outputs and objective evidence as well.

## 11. Analyze beyond aggregate scores

Aggregate pass rates, time, resource use, and variation when possible. Then inspect patterns that averages may hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill’s contribution.
- **High variation:** Comparable runs differ substantially, suggesting ambiguity, instability, or weak instructions.
- **Tradeoffs:** Quality improves, but time or resource use may be disproportionate.
- **Failure concentration:** Several failures may share a root cause such as unclear source selection.
- **Unproductive work:** Execution evidence shows redundant planning, research, or formatting.
- **Repeated reconstruction:** Multiple runs recreate the same helper process, suggesting a resource should be bundled.

Treat a small test set as evidence for the next revision, not final proof.

## 12. Improve without overfitting

Revise based on user feedback, outputs, and analysis. Change the smallest part likely to address the underlying cause.

Generalize from complaints. If one result omits source notes, do not add a rule naming that exact test. Clarify the broader condition: when evidence is incomplete or mixed, separate verified facts from assumptions and identify what cannot be confirmed.

Use these principles:

1. Fix causes, not individual examples.
2. Keep instructions lean and remove guidance that does not help.
3. Explain intent so the AI can adapt intelligently.
4. Add scripts, templates, or references only when repeated work demonstrates their value.
5. Preserve behavior the user already values.
6. Add tests only for real classes of failure, not every isolated incident.

After revising, rerun the relevant test set in a new iteration, using the same baseline policy. Show previous outputs or feedback alongside new outputs when useful.

Stop when the user says the skill is ready, feedback is consistently positive across meaningful cases, objective requirements are reliable, or further revisions are not producing meaningful improvement.

## 13. Optional blind comparison

For a more rigorous comparison between two versions, use blind review. Give an independent evaluator two outputs without identifying their origins. Ask for a judgment against a shared rubric, then reveal the mapping only after the assessment is recorded.

Use blind review when versions have similar metrics, qualitative judgment is important, or the decision has meaningful cost. Tie the rubric to correctness, completeness, clarity, constraint adherence, safety, and practical usability. Analyze why one result was preferred before changing the skill.

## 14. Optimize triggering behavior

After the workflow itself is useful, test the description that controls activation. Build a realistic set of requests that should trigger and nearby requests that should not. Use roughly balanced coverage and include enough detail that consulting a skill would actually be useful.

Positive examples should include formal and casual wording, direct and implied requests, common and uncommon valid cases, and cases where related skills could compete.

Negative examples should be challenging near-misses, not irrelevant requests. They should share language or concepts with the skill but belong to a different job, need another capability, or lack the conditions that make the skill appropriate.

```json
[
  {
    "query": "I need a concise leadership update from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Explain what project status reports are and why teams use them.",
    "should_trigger": false
  }
]
```

Review the query set with the user. If the environment supports repeated activation testing, separate cases used to refine the description from held-out cases used to choose it. Select the description that performs best on held-out cases, not merely on the cases used during editing.

Simple one-step requests may not activate a specialized skill even with a strong description because an AI can handle them directly. Make activation tests substantive enough that using the skill would add real value.

## 15. Package and hand off

Package the core instructions and only resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on private conventions, hidden access, or undeclared tools.
- Scripts and references are present, clearly named, and documented.
- No credentials, private identifiers, confidential data, or unnecessary personal details remain.
- The user can install or adapt the package in their chosen environment.
- Test material is retained only when it is safe and useful.

Provide a handoff note describing what the skill does, required capabilities, known limitations, permission boundaries, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, an honest description that routes suitable requests, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.


---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using real screenshots and programmatic layout checks. Treat a change as complete only after failures are fixed and the relevant sweep is rerun.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to a small spacing, color, or background edit: a local change can alter wrapping, height, overflow, alignment, or backgrounds elsewhere.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Use real screenshots and numerical checks together.

## 1. Prepare realistic page states

Run the real interface in an authorized test environment. Populate the changed surface with representative content before testing:

- long paragraphs, formatted text, long field values, and validation messages;
- representative cards, rows, lists, and item counts;
- loading, empty, and error states when the change can affect them;
- realistic data that exercises wrapping, scrolling, and vertical growth.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping defects, and unintended blank space. Use only the minimum test data needed, and avoid exposing unrelated personal or sensitive information in screenshots or reports.

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

Also include known target viewports when they are available. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable browser-testing system selected for the project. Run it headlessly unless interactive inspection is necessary.

| Test condition | Minimum expectation |
|---|---|
| Standard responsive layout | Baseline width sweep |
| Vertical or viewport-height behavior | Relevant widths at short and tall heights |
| Large-display experience | Include a large desktop width |
| Known user or device target | Include that viewport when practical |

## 3. Capture and inspect screenshots

Capture real screenshots at every relevant viewport and state. Use full-page screenshots when page length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect every changed component on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design now that the component's role may have changed.

Pay special attention to edge-to-edge or full-bleed changes. A component made flush with an edge may expose leftover wrapper margins or padding as visible background strips. Check every edge, not only the edge edited.

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

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant bounding rectangles with adjacent elements and container boundaries. Check visibility and usability through the project’s chosen automation capability, such as verifying that controls have non-zero visible bounds and can receive an intended interaction.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line; reading-focused designs commonly use a narrower target of roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visual defects such as exposed background strips, poor balance, or unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and the relevant programmatic checks pass.

## 6. Fix failures and rerun the sweep

If any viewport or realistic state fails:

1. stop the completion or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the failing size.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is likely incomplete. Do not ship a known failure for another person to discover unless an authorized decision explicitly accepts and documents the limitation.

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

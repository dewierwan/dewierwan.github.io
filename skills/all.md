# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate distinct options for a decision, assess their tradeoffs honestly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs credible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas; it is a small set of genuinely different paths with candid tradeoffs and a clear basis for choosing.

## 1. Gather relevant context

Start with the information provided in the request. If the user links documents, prior decisions, research, discussion records, or other materials that are available in the current environment, review the minimum sources needed to understand the decision.

When the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Previous decisions and their rationale
- Existing commitments, deadlines, budgets, and technical constraints
- Evidence about attempts already made and their results
- Relevant stakeholder needs, ownership boundaries, or risks

Access private communications or records only for a legitimate purpose and with clear authorization. Use only relevant information, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

Do not search broadly by default. If essential context is unavailable, state the assumption or ask a focused question instead of inventing facts.

## 2. Frame the decision

Before generating a substantial option set, write a short framing of two to four sentences that states:

- What decision is actually being made
- The key constraints and non-negotiables
- What a good outcome looks like
- The criteria that should determine the choice

The stated question may describe a symptom or a proposed solution rather than the real decision. For example, “Should we add this feature?” may actually mean “What is the lowest-risk way to reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before continuing. Skip this pause only when the decision is obvious and low-stakes, or when the user explicitly requests an immediate first pass. Bad framing creates polished but irrelevant options.

## 3. Generate distinct options

Generate five to seven options unless the decision naturally contains fewer meaningful paths. Each option must be a fundamentally different approach, not a variation in scale or intensity. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes scope, incentives, process, timing, or framing
- At least one surprising but plausible option, such as delaying, partnering, reducing scope, or deliberately doing nothing

Do not be contrarian merely to seem creative. A “do nothing” option is useful only when waiting, observing, or avoiding distraction is a real strategic choice.

Give each option a brief, memorable label that communicates its core idea. For every option, provide:

- **What:** One or two sentences explaining the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limits.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not hide serious drawbacks or make a preferred option look better by evaluating alternatives unfairly.

## 4. Evaluate and recommend

Select criteria that fit the decision. Common criteria include likely impact, effort, cost, speed, reversibility, strategic fit, risk, stakeholder burden, and confidence in the evidence. Add domain-specific criteria when they matter more.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but clearly explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not merely why it is generally attractive.
4. State the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user asks for one. Preserve real choices when the evidence does not justify false certainty.

## 5. Stop for a decision

After presenting the options and recommendations, wait for the user. They may:

- Pick an option
- Ask for more detail on one option
- Correct the framing or constraints
- Request additional options
- Propose a hybrid approach

For a hybrid, check whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option seems promising.

## 6. Hand off with appropriate rigor

Once a path is selected, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge or pre-mortem before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record with the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choice:** After recording the decision, create an execution plan covering requirements, milestones, tasks, dependencies, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than a superficial request.
- Options are meaningfully distinct.
- The obvious option and at least one non-obvious option were considered where relevant.
- Strengths and weaknesses are concrete and candid.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria and constraints.
- Any retrieved private information was necessary, authorized, minimized, and handled within the proper access boundary.


---
name: pressure-test
description: Find weak points in a leading strategic idea before commitment through a steelman, sequential challenge, pre-mortem, verdict, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or build an implementation plan.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes a defense of that idea.
- If the same topic was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the prior findings to make the decision.
- If using internal records, communications, research, or feedback about people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Steelman the idea before attacking it. Test the strongest reasonable case, not a caricature.
- Ask **one forcing question at a time**. Wait for an answer, evaluate it, and push back on vague, unsupported, or evasive answers before continuing.
- Use available evidence such as metrics, experiments, research, customer feedback, prior decisions, and stakeholder input. Label facts, inferences, and forecasts clearly.
- Refer to credible dissenters by role. Do not invent their views or assume silence means agreement.
- Skip a section only if it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's actual intent. Include the action, expected outcome, mechanism, timeframe, and conditions required for success.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so. If a stronger restatement changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions the claim depends on. Rank them by the damage caused if they are wrong. Make them observable where possible: replace “users will value this” with a defined behavior, group, threshold, or willingness-to-pay condition.

| Rank | Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|---|
| 1 | [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Test or disproof method] |

Prioritize the assumptions with both high damage and weak support.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Choose questions based on the highest-risk assumptions; later questions should respond to what earlier answers reveal. Do not present a full questionnaire that allows selective answering.

Use these categories as needed:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar effort failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what will the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which relevant role would object most strongly? What would that person say, and has that perspective been sought directly?
- **Reversibility:** If this is wrong, what would unwinding require in time, money, commitments, trust, or operational disruption?
- **Null option:** What happens if no action is taken for the next three months?

If an answer is “I think it will work,” ask for observable behavior, data, a comparison, or a commitment that supports it.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, usually 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution problems, changed external conditions, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or accountable role |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable early signal] | [Check or role] |

Warning signs must appear early enough to change course.

## 5. Surface credible dissent

Identify two or three roles that could reasonably disagree, such as a finance owner, delivery lead, customer representative, domain expert, risk owner, or skeptical peer. State the strongest likely objection from each.

If the decision-maker has not sought a relevant perspective, mark it as an evidence gap. Dissent is not an automatic veto; it exposes constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test incomplete or failed rather than approving the idea.

## 7. Give a verdict and handoff

Choose one verdict and state the next step explicitly:

- **GREEN — proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Create a decision record and commit. For hard-to-reverse or organization-defining choices, schedule a review point.
- **AMBER — test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible test, such as a focused interview set, expert review, prototype, or short data collection period. Run the test, then make the decision with the result recorded.
- **RED — stop, redesign, or reopen options.** A core assumption is weak, downside is unacceptable, or no meaningful falsification criterion can be named. Generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with **exactly one concrete next action**: a verb, an owner, and a deadline when useful.

Example: `Research owner: interview five target users by 18 Oct and compare findings against the adoption assumption.`

## Final audit

Before closing, verify that the output contains:

- a confirmed steelman;
- three to five ranked load-bearing assumptions;
- five to eight forcing questions explored sequentially;
- a pre-mortem with early warning signs;
- credible dissenting roles and objections;
- a clear mind-change criterion;
- a GREEN, AMBER, or RED verdict with an explicit next step; and
- one concrete next action.

Common failures are skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and issuing a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, make authorized records without inventing the user’s views, and review outcomes to improve future choices.
---

# Make a decision

Use this workflow to make a clear choice with rigor proportional to its stakes and reversibility. The aim is not maximum analysis: most decisions should take minutes, while costly or direction-setting choices deserve challenge, consultation, a record, and a later review.

## Core rules

1. **Match rigor to stakes.** Use a quick default for small, reversible choices; reserve lengthy work for decisions that are expensive to unwind.
2. **The user owns their position.** Never state, record, or imply that the user favors, opposes, is leaning toward, or decided an option unless they explicitly said so.
3. **Separate advice from attribution.** Put recommendations in chat under **Assistant analysis**. Add them to a record only if the user specifically asks. If the user has stated no position, write “No position stated yet” or leave their position blank.
4. **Record only with permission.** “Should we do this?” asks for analysis, not for a new record. Create or update a record only when the user asks to log, track, open, record, or commit it, or explicitly agrees.
5. **Respect privacy and access boundaries.** Before consulting shared messages, internal records, personal information, or a shared register, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and omit unrelated sensitive information.
6. **Do not turn execution into a decision.** If there is no meaningful alternative, say so and move to planning or doing the task.
7. **Do not use rigor to delay.** Once the appropriate checks are complete, name the call and move forward.

Before writing to a shared record, confirm that its audience is appropriate. For sensitive subjects, including health, relationships, compensation, or confidential personnel matters, keep the discussion in chat or offer a private record.

## 1. Select the mode

Choose the mode from the user’s request and, only if authorized, the relevant decision register.

- **New:** No relevant record exists, or the user wants a fresh decision.
- **Resume:** An existing decision is still open and the user wants to continue.
- **Commit:** An open decision exists and the user is ready to decide.
- **Review:** A resolved decision has reached its review point and has not yet received an outcome assessment.

Follow an explicit user instruction over automatic detection. Otherwise, search for overlapping records before creating a duplicate. On resume, append new inputs and shifts in thinking; do not rewrite history. On review, use the original prediction and reasoning as the baseline.

## 2. Frame the decision

Write a question that can be answered. Ask one clarifying question at a time when needed:

- What is being chosen?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What is the deadline or decision trigger?
- What outcome is sought, and what happens if nothing changes?

If the problem is open-ended and there are no credible options, generate options first. If only one viable path exists, say: “This is a task rather than a decision; the next step is to plan or execute it.”

## 3. Classify scope

Classify by the cost of unwinding the choice: money, time, trust, operational disruption, opportunity cost, and reputation—not apparent size alone.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes; reversible within hours | Decide now; do not record by default |
| Reversible | Moderate stakes; reversible in days or weeks | Short comparison and, if useful, a light record |
| Hard to reverse | Material cost, disruption, or loss if undone | Full analysis, challenge, and stakeholder check |
| Direction-setting | Shapes strategy, culture, finances, or operating model for a long period | Full analysis, explicit dissent, and prerequisite conversations |

If the user calls it trivial, ask: **“What would it cost to unwind?”** If the cost is uncertain, disruptive, or cannot be stated quickly, use a larger bucket.

## 4. Apply the appropriate rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, say so plainly: further attention may cost more than an imperfect choice.

### Reversible

Aim for roughly ten minutes:

1. List two or three realistic options.
2. For each, state one strength, one weakness, and a rough effort, cost, or time estimate.
3. Give an **Assistant analysis** recommendation and the decisive reason.
4. Where uncertainty matters, choose the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

A hard-to-reverse decision normally deserves roughly 30–60 minutes of work. Before commitment, pressure-test the leading option by examining assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and important objections from affected people or relevant experts.

If no relevant challenge has occurred in the current working context, stop and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not bypass this merely because the user is in a hurry. Continue only after the challenge is complete or the user explicitly overrides it with a reason.

Use the challenge result as a decision rule:

- **Green:** No material unresolved issue; proceed with options, pre-mortem, stakeholder check, and recommendation.
- **Amber:** Risks or unknowns remain but are understood and bounded; proceed only after stating mitigations, owners, and review triggers.
- **Red:** A serious failure mode, missing evidence, or unresolved constraint remains; do not force commitment. Return to option generation, redesign the proposal, gather a decision-changing fact, or run a bounded test.

### Direction-setting

Use the hard-to-reverse process plus two gates:

1. Name the specific leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has happened, unless the user explicitly records why proceeding is necessary. If the choice is being rushed, identify exactly what consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture what it enables; what it costs, delays, or prevents; strongest supporting evidence; strongest objection; key assumptions; and reversal cost. Choose criteria before comparison and separate non-negotiables from preferences. Use scores only when they clarify tradeoffs.

| Category | What belongs here |
|---|---|
| User’s stated view | Only the user’s expressed choice, reasoning, confidence, and response to concerns |
| Assistant analysis | The assistant’s recommendation, evidence, and reasoning |
| Open question | Material uncertainty not yet resolved |

Run a pre-mortem: “It is later and this failed. What most likely caused it?” Then identify stakeholders with relevant expertise, consequences, or constraints.

## 6. Commit and record

Before finalizing a meaningful decision, confirm the choice, rationale, reversal conditions, next action owner and date, observable prediction, and the user’s confidence in that prediction. Make predictions testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [X%].

Use the user’s chosen document system, register, or private file. A record should include status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. For non-binary questions, mark the record resolved when a decision has been made.

| Scope | Default review point | Reminder approach |
|---|---|---|
| Reversible | One month | Record a review date |
| Hard to reverse | Three months | Record a review date and reminder |
| Direction-setting | Six months | Record a review date and reminder |

Use a meaningful milestone or trigger instead when it is better than a calendar date. For high-stakes choices, create a reminder in the user’s chosen calendar or task capability if authorized.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** [What it is and central tradeoff]
- **Option B:** [What it is and central tradeoff]
- **Option C:** [What it is and central tradeoff]

## Thinking log
### [Date]
- New inputs, conversations, data, or events
- How the thinking changed
- User’s stated position: open / leaning / decided

## Dissent
[Who raised concerns, their strongest argument, and how it was handled.]

## My choice and why
[User’s own reasoning, only when stated by the user.]

## What would change my mind
[Assumptions or evidence that would justify reversal.]

## Prediction
By [date], [observable outcome] will happen or not happen.
Confidence: [X%]

## Worries
[Most credible downside or failure mode.]

---

## Retrospective
[To be completed at review.]
```

For a new open decision, record context, current options, and new inputs; leave commitment sections blank. On resume, append a dated thinking-log entry and add genuinely new options without replacing prior reasoning.

## 7. Review the outcome

At the review point, complete four sections:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare actual events to the recorded prediction and confidence.
3. **Was the process sound?** Judge the evidence, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle that can improve a later decision.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Keep outcome quality separate from decision quality: a sound decision can have a poor result under uncertainty, and a weak process can get lucky.

## Completion message

When a decision is made, summarize it plainly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [date]
Review: [date or trigger]
Record: [location, if one exists]
```

Use direct language and challenge weak reasoning with evidence. Once the required gates are satisfied, commit, record only within the authorized boundary, and proceed.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only mode.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, operational, integration, or automation problem whose solution is not already obvious. Do not use it for a small fix or routine task with a known implementation.

By default, work from understanding through implementation. If the user requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's proposed solution. If they ask to “build X,” work backward:

- Who experiences the problem, and in what role or context?
- What are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the situation meaningfully better?

Write a concise problem statement and descriptive requirements. Describe desired outcomes and constraints, not an assumed implementation. If the proposed solution does not fit the problem, say so directly.

Ask only for information that cannot reasonably be found in authorized context, documentation, code, or records. When using communications or records about people, have a legitimate purpose and clear authorization; use only the minimum relevant material, omit unrelated sensitive details, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, and available alternatives. Include “do nothing,” “deprioritize,” or “improve the workaround” as real options when appropriate.

Distinguish decisions by reversibility:

- **Reversible decisions:** Small, easy-to-change choices. Use reasonable judgment, choose, and proceed.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, long-lived settings, migrations, external contracts, security boundaries, or vendor commitments. Pause and obtain an explicit decision before implementation. Record the decision and rationale when useful.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Find established patterns and reusable components before inventing new ones.

Understand compatibility needs, deployment practices, security expectations, supported environments, ownership boundaries, monitoring, and maintenance capacity. Follow existing conventions unless there is a strong, documented reason to change them.

## 4. Define evaluation criteria

Define lightweight, explicit criteria before generating solutions. For example:

- Must preserve existing authentication, authorization, and data behavior.
- Must fit the available time and maintenance capacity.
- Should avoid new dependencies, persistent settings, or public interfaces.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide both option generation and selection. Without them, the first plausible idea may win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small, targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For especially ambiguous problems, generate a wider candidate set before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate strictly and fail fast for invalid states. Do not silently convert programming errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Place changes in the appropriate design boundary; avoid quick fixes that create hidden coupling.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep proposals direct and short. Store them in the user’s chosen shared documentation system when durable review or collaboration is needed; otherwise use the current workspace. Use a clear, date-prefixed title such as `DD MMM YYYY: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership. Keep the plan where reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm results against the evaluation criteria, including compatibility, authorization, privacy, and failure behavior.

Do not claim success based only on implementation. State what was tested and what remains unverified. Commit, publish, or deploy changes only according to the user’s repository and release practices.

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
description: Search only the sources that matter, then produce a proportionate, evidence-linked context brief for a person, organization, project, topic, or decision.
---

# Gather context

Use this workflow when a user needs to get up to speed before writing, deciding, meeting, pitching, planning, hiring, or acting. It turns relevant material from approved private and public sources into a clear, evidence-linked context brief.

The central rule is **right-size the research**. A quick status question should not trigger a broad investigation. A consequential decision should not rest on one convenient message. Choose the smallest search that can reliably answer the request, then expand only when the stakes, uncertainty, or evidence justify it.

## 1. Confirm purpose, authority, and output boundary

Identify:

- The subject: a person, organization, project, topic, or decision.
- The action, decision, or conversation the brief will support.
- The intended audience.
- The appropriate delivery location.
- Whether the user has legitimate authority to access and use each proposed private source.

Private information requires a legitimate, task-relevant purpose. Access to a system does not itself justify searching it.

For research about people, apply a stricter boundary:

- Search only the minimum relevant private sources.
- Use only information needed for the stated purpose.
- Do not collect unrelated personal, sensitive, or confidential details.
- Do not infer protected traits or private facts that are unnecessary to the task.
- Respect consent, confidentiality, need-to-know limits, and reasonable privacy expectations.
- Keep the brief within an access boundary appropriate to its evidence and audience.

If the purpose, authorization, subject identity, or intended destination is unclear, ask one focused question before accessing private material. Do not ask unnecessary questions when the request is already clear.

If the user requests structured meeting preparation rather than general context, use their approved meeting-preparation process if one exists. This workflow assembles context; it does not prescribe an agenda, meeting page, or follow-up plan.

## 2. Scope the work before searching

Choose an effort level and state it in one short line so the user can redirect the scope. For example: “Standard review across messages, documents, and recent meeting notes; I can expand the review if needed.”

- **Quick:** For “where are we?”, “remind me,” or a narrow status question. Search one to three obvious sources, make one focused pass through each, and return a short answer.
- **Standard:** The usual level. Search a handful of sources that plausibly contain useful evidence, use a few queries where needed, and write a compact brief.
- **Deep:** For consequential decisions, major negotiations, important meetings, significant hires, or complex strategic questions. Search broadly across relevant sources, verify important claims, inspect primary records, and resolve contradictions.

When uncertain, start lighter and offer to deepen the research. It is easy to expand a focused brief; it is costly to overwhelm the user with material they did not need.

Avoid two opposite failure modes:

1. **Over-gathering:** Searching every available system, doing excessive parallel research, or producing a long report for a simple request.
2. **Under-gathering:** Treating a single email, message, or document as a complete answer when the request clearly calls for wider evidence.

Apply this source-selection rule to every possible source:

> Would a sensible researcher think this source is worth checking for this specific request, at this effort level?

Both relevance and effort level must pass. A source can be relevant in principle but not worth checking for a quick question. Conversely, a normally secondary source may become essential if it contains a recent decision, direct agreement, or meeting record.

Set a time window. A useful default is the previous several months, extending further back when the relationship, project, or decision has a longer history. For a status update, prioritize recent changes. For a history or decision review, include earlier turning points, original decisions, and commitments that remain active.

## 3. Classify the subject and select source clusters

Classify the request because likely evidence differs by subject.

| Subject type | Usually relevant source capabilities | Primary research aim |
|---|---|---|
| Person | Correspondence, internal messages, meeting notes, calendar history, relationship records, public professional sources | Role, relationship, commitments, recent interactions, and relevant background |
| Organization | Public website, correspondence, internal discussions, documents, partner or pipeline records | Current position, relationship history, commercial or strategic context |
| Project or initiative | Planning documents, internal messages, shared files, task records, product data, and source code where relevant | Current state, decisions, ownership, blockers, milestones, and evidence of progress |
| Topic or question | Public research, internal strategy documents, prior discussions, and technical material | Existing thinking, evidence, alternatives, risks, and unanswered questions |
| Decision | Sources relevant to each option, plus decision records and current evidence | Options, support and trade-offs, owners, timing, and unresolved risks |

If a name or term could refer to multiple subjects, ask one tight disambiguating question. Otherwise, proceed.

Sources explicitly named by the user are mandatory, but they are not necessarily exhaustive. Treat them as a floor, not a ceiling: add another source only when it clearly contains decision-relevant context.

A special rule applies to meetings: if messages, calendar entries, or documents show that a relevant meeting occurred recently, retrieve authorized meeting notes or a transcript. This is particularly important for a same-day or same-week interaction, because it may be the most complete record of what was discussed or agreed. Apply the same privacy, consent, and audience limits to transcripts as to the meeting itself.

## 4. Search proportionately and preserve evidence

For quick and standard work, search directly and inspect results as they arrive. For deep work across independent source groups, divide read-only research into a small number of clear workstreams only when this saves time or improves coverage. Each workstream should return a concise digest with direct evidence links, not a raw data export.

Scale search depth with the effort level:

- **Quick:** Use one or two precise queries in each selected source and inspect the strongest results.
- **Standard:** Search by subject name, organization, project terms, related people, and useful alternate names.
- **Deep:** Use multiple queries per source. Do not conclude “nothing found” until reasonable names, aliases, related terms, and source-specific search methods have been checked.

Use the capabilities available in the user’s approved environment. Typical source practices include:

- **Email:** Search direct correspondence and meaningful mentions in other threads. Read relevant conversations, not only snippets. Link to the conversation or message with a verified navigable link.
- **Internal messages:** Search names, organizations, project terms, and decision language. Read surrounding messages and complete threads for claims that carry weight in the brief.
- **Knowledge bases and documents:** Prefer focused content search over broad automated summaries when broad search produces noise. Retrieve the full relevant page or document. If a document has multiple sections, pages, tabs, sheets, or attachments, inspect each relevant part rather than assuming the first view is complete. Attribute material to the relevant section where useful.
- **Calendar and meeting records:** Check past events for relationship history and upcoming events for urgency. Retrieve authorized notes or transcripts. Be cautious about speaker attribution where a recording may include multiple people in one location.
- **Structured records:** Consult available schema descriptions, field definitions, and data-quality notes before querying. Use the record type designed for the question. Treat stale or weak relationship-management data as a lead to verify, not decisive evidence.
- **Product, operational, and code sources:** Use these only when the request concerns a product, feature, operational process, delivery status, or technical implementation. Check recent history and current state, not merely one snapshot.
- **Public web:** Prefer official sources, current professional profiles, reputable reporting, and primary publications. Verify role and date claims against current evidence. Do not invent, guess, or reproduce an unverified link.

If a source judged relevant returns no results, is unavailable, or cannot be accessed, say so in the brief. Do not silently substitute a nearby source and imply the intended source was checked. A source deliberately skipped as irrelevant does not need to be listed as a gap.

When an approved source connection is unavailable, perform only safe checks permitted in the user’s environment, such as confirming that the connection is enabled or that authorization has not expired. If user action is still required, state the exact problem, what was checked, and the one remaining action, such as completing authorization or restoring access. Never request credentials or sensitive access information through the brief.

## 5. Evaluate evidence before writing

Prefer current, primary evidence. A formal decision record, a direct participant statement, an official public page, or a complete meeting record is generally stronger than a secondhand summary.

For every important claim:

1. Identify the supporting source.
2. Check its date, author, scope, and reliability.
3. Compare it with conflicting or newer evidence.
4. State uncertainty when it cannot be resolved.

Do not list contradictions without interpretation. If an older public article gives a role that conflicts with a current professional profile and recent correspondence, identify the discrepancy and explain which evidence is more current and why. Distinguish facts, reported claims, interpretations, and open questions.

Every sourced claim should have a clickable, verified path to underlying evidence when the source system supports links. Do not expose links that exceed the intended audience’s access boundary.

## 6. Write a scan-and-act context brief

Organize the brief by themes and decisions, not by the order in which sources were searched. Lead with what matters for the user’s next action. Keep prose blocks short and use bullets where they improve scanability.

Adapt this structure to the subject:

```markdown
## [Subject] — context brief
*Scope: [quick, standard, or deep]. Sources checked: [source categories]. Window: [dates].*

## TL;DR
- [Most decision-relevant finding, with evidence link.]
- [Current state, risk, or opportunity, with evidence link.]
- [Immediate implication, clearly marked as an interpretation if needed.]

## What we know
### [Theme]
[Concise synthesis with inline evidence links.]

## Relationship or timeline
[Relevant contact history, milestones, commitments, and changes over time.]

## Decision context
[Options, supporting and opposing evidence, owners, deadlines, and dependencies.]

## Open questions and gaps
- [Question not answered; expected source or next validation step.]
- [Relevant source unavailable, empty, or too weak to support a conclusion.]

## Sources
- [Primary source link]
- [Supporting source link]
```

A quick brief may use only the title, short summary, current state, and gaps. A deep brief should include the full structure, but remain concise enough to act on.

For hiring or assessment-related context, describe role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Do not include irrelevant personal information or make inferences unrelated to the role.

## 7. Deliver and verify

Deliver short briefs directly in the conversation when the audience and sensitivity permit. For long reference briefs, create or update a document in a user-approved shared location with a clear date-and-subject title. Do not place sensitive material in a broader location than the source material permits.

Before writing to a shared document, confirm that the destination is appropriate for the evidence and intended readers. Preserve links to primary evidence where recipients are authorized to access them.

If editing an existing formatted document:

- Insert content into a known normal body-text location, or replace a fully inspected section.
- Do not insert at the first character of an existing heading, list item, or table cell if it may inherit the wrong style.
- Re-read the affected range after insertion using a format-aware representation.
- Confirm body paragraphs and list items use body-text styles and that only intended headings use heading styles.
- If visual layout matters, render or inspect the document before reporting completion.

The brief itself is the deliverable. Do not append a redundant meta-summary after it. If offering follow-up work, such as drafting a message or preparing decision options, place that offer before the final brief rather than after it.


---
name: learning-tutor
description: Learn a paper, article, or topic through a Socratic dialogue that builds recall, reasoning, and practical application instead of passive review.
---

# Learn with a tutor

Help a learner understand, retain, and use a paper, article, post, lesson, or topic through an active dialogue. Favor retrieval, explanation, and application over passive summary. The learner should do most of the thinking; the tutor should diagnose understanding, create productive challenge, and help the learner form durable connections.

## Core learning principles

- **Retrieve before reviewing.** Do not provide an unsolicited summary. Ask the learner to reconstruct ideas from memory in their own words.
- **Probe mechanisms.** Ask why, how, under what conditions, and with what evidence an idea holds. Do not stop at a repeated conclusion.
- **Require generation.** Have the learner create examples, analogies, predictions, objections, and applications before offering your own.
- **Use productive difficulty.** Make the task effortful but achievable. Challenge confidence without leaving the learner unable to attempt an answer.
- **Practice transfer.** Connect the material to unfamiliar cases, adjacent concepts, and real decisions.
- **Reveal gaps through questions.** When reasoning is incomplete or inconsistent, use a focused question to expose the tension. Explain directly only after a fair attempt to reason it out.

## Conversation workflow

### 1. Establish prior knowledge and a learning goal

Begin by finding out what the learner already knows, believes, or has experienced, and what they need from the session. Ask one or two open questions, such as:

- “What do you already think is true about this topic, and why?”
- “What are you hoping to explain, evaluate, or do by the end?”
- “What has been confusing, surprising, or important so far?”

Use the response to set an appropriate level of difficulty and identify likely misconceptions or useful background knowledge.

### 2. Elicit the central idea from memory

Ask the learner to explain the main argument, finding, or concept without quoting the source.

- “In your own words, what is the main claim?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “How would you explain it to a thoughtful friend in 30 seconds?”

If the learner has not engaged with the material yet, ask for an initial prediction or working model. Then invite them to inspect a relevant section and return to retrieval rather than giving a full explanation immediately.

### 3. Choose a few high-value ideas

Do not attempt to cover everything. Select two or three ideas that are central, difficult, consequential, or easy to misunderstand. Explore each through a short cycle:

1. Ask the learner to state or reconstruct the idea.
2. Probe assumptions, evidence, causal reasoning, and limits.
3. Ask for a concrete example, analogy, or application.
4. Test the idea with an objection, alternative explanation, or boundary case.
5. Adapt the next question to the learner’s actual answer.

Keep turns short. Usually ask one or two questions at a time.

## Question toolkit

Choose prompts that require explanation rather than recognition. Adapt them to the learner and subject.

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What is the mechanism, step by step?”
- “What evidence would distinguish this explanation from another one?”
- “Can you give a concrete example from a familiar setting?”
- “Where might this fail or not apply?”
- “What is the strongest objection to this argument?”
- “How does this relate to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one assumption changed?”

Avoid questions that can be answered only with yes or no. If a short factual check is needed, follow it immediately with a request for reasoning.

## Responding to learner answers

Be warm, rigorous, and specific. Avoid generic praise. When an answer is strong, identify what made it useful—for example, it named an assumption, separated correlation from causation, or supplied a relevant counterexample—then raise the level of challenge.

When an answer is inaccurate or incomplete:

1. Do not immediately state the correction.
2. Ask a question that points to the conflict, missing distinction, or unsupported inference.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, give a concise explanation or hint.
5. Ask them to restate the improved idea or apply it to a fresh example.

If the learner says, “I don’t know,” invite an attempt first: “Take a guess based on what you do know. What seems most plausible, and why?” Narrow the task or provide a hint only after an attempt, or when the necessary foundation is missing.

## Calibration and progress checks

Increase difficulty when answers come easily: ask for a counterexample, prediction, comparison, or transfer to a new setting. Reduce difficulty when the learner is lost: isolate one assumption, use a simpler case, offer a constrained choice, or break the explanation into one reasoning step at a time.

Periodically provide a brief, evidence-based progress check:

- What the learner has demonstrated they understand.
- What remains uncertain, incomplete, or confused.
- The most useful next question or concept to revisit.

Do not treat recognition of a term or repetition of a conclusion as mastery. Look for accurate explanation, justified reasoning, and successful application.

## Closing gate

Before ending, ask the learner to turn understanding into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation, example, or future retrieval prompt. End by naming the next concept, question, or application worth revisiting.

## Guardrails

- Do not summarize unless the learner explicitly requests it; even then, invite their own summary first.
- Do not lecture when a well-designed question can prompt retrieval or inference.
- Do not define jargon automatically; first ask the learner what they think it means, then clarify if needed.
- Do not make the dialogue easy merely to be encouraging.
- Do not cover an entire source superficially when a few central ideas can be understood deeply.
- Keep the exchange conversational rather than turning it into a fixed quiz.


---
name: write-in-my-voice
description: Draft or revise email in the user’s authentic voice using approved style evidence, verified facts, and a concise final audit.
---

# Write in my voice

Use this workflow when drafting, replying to, or polishing an email on the user’s behalf.

## Goal

Produce a copy-ready email that sounds recognizably like the user while remaining appropriate for the recipient, relationship, and stakes. Match the user’s established habits where evidence supports them, but never invent facts, commitments, sentiment, or authority.

## 1. Establish a voice profile

Before drafting, review the user’s current writing guidance in full, if available. With legitimate purpose and clear authorization, review only the minimum relevant examples of emails the user has sent or approved. Prefer recent examples and examples written for a similar audience or purpose.

Do not expose unrelated personal details from private messages, contacts, or records. Keep any output within the user’s authorized access boundary.

Extract a practical profile from the evidence:

- Typical greeting and sign-off.
- Formality level, warmth, and directness.
- Typical sentence and paragraph length.
- Use of contractions, colloquialisms, punctuation, bullets, and exclamation points.
- Preferred wording for requests, follow-ups, declines, corrections, apologies, and thanks.
- Phrases, tones, formatting, or punctuation the user avoids.
- Approved reusable facts, links, boilerplate, and standard replies.

Use a style instruction only when it is supported by current examples or explicitly confirmed by the user. If examples conflict, give greater weight to recent, repeated patterns. If the conflict matters, ask the user which style is current.

### Voice-profile template

| Element | Observed or approved preference |
|---|---|
| Greeting | [Example: first-name greeting, or no greeting for ongoing threads] |
| Sign-off | [Preferred closing or when to omit it] |
| Tone | [Example: concise, warm-professional, direct] |
| Avoid | [Example: generic pleasantries, excessive hedging] |

## 2. Confirm the email brief

Identify the minimum information needed to send an accurate email. Ask focused questions only when a missing answer would materially change the message.

1. Who is the recipient, and what is their relationship to the sender?
2. What outcome should the email produce?
3. What facts, dates, names, links, attachments, or prior context must appear?
4. What action is requested, who owns it, and by when?
5. How warm, firm, formal, or brief should the message be?
6. Are there confidentiality, approval, legal, financial, or reputational constraints?

Do not infer availability, decisions, pricing, policy, timelines, opinions, emotional reactions, or commitments. If the user has not provided a necessary detail, either ask for it or write around it without making a claim.

## 3. Adapt voice to context

The user’s voice is a range, not a rigid template. Preserve recognizable patterns while adjusting for audience and consequences.

- **Close colleagues or familiar contacts:** Use the user’s normal degree of brevity and informality.
- **New, senior, external, or formal recipients:** Keep the user’s directness, but provide enough context and use clearer, more careful wording.
- **Sensitive, corrective, or conflict-related messages:** Be factual, calm, and explicit. Avoid blame, defensive process explanations, excessive praise, or apologies that imply responsibility the user did not accept.
- **Requests and decisions:** Put the requested action or decision near the start. State the owner and timing when known.
- **Scheduling and logistics:** Use approved links, availability, and standard language only when current and applicable.

Approved boilerplate can save time and improve consistency, but do not use it if it is outdated, inaccurate, too broad, or mismatched to the recipient.

## 4. Draft the smallest complete email

Write only what the recipient needs to understand and act. A reliable structure is:

1. Greeting, if appropriate for the user and thread.
2. Purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Close and sign-off, if appropriate.

Use concrete nouns, active verbs, short sentences, and short paragraphs. Make decisions, deadlines, and asks easy to find. Use bullets only when they improve clarity for multiple actions, options, or logistics.

Remove content that does not serve the recipient:

- Throat-clearing such as “I just wanted to reach out.”
- Generic pleasantries that are not useful or characteristic of the user.
- Repeated thanks, praise, or apologies.
- Hedging that weakens an intentional request or decision.
- Internal process narration.
- Explanations of how the draft was created.

### Generalized example

Instead of: “I was hoping that you might be able to let me know whether you have had a chance to review the proposal.”

Use: “Have you had a chance to review the proposal? Please send feedback by Thursday if possible.”

## 5. Audit before presenting

Review the draft line by line:

- Would the user plausibly write these words?
- Do the greeting, closing, rhythm, and punctuation match the available evidence?
- Is the tone appropriate for this recipient and situation?
- Does every factual statement have support from the brief or approved materials?
- Did the draft introduce a promise, deadline, opinion, decision, or emotion not supplied by the user?
- Are names, titles, dates, links, attachments, and thread references correct?
- Is the requested action clear?
- Is sensitive information necessary, authorized, and limited to the intended recipient?
- Can any sentence be removed without losing meaning or usefulness?
- Does the draft avoid the user’s known style anti-patterns?

If voice evidence is unavailable, use a broadly useful default: clear, concise, warm-professional, and direct. Briefly state that assumption if needed, and invite the user to provide approved examples or preferences for future drafts.

## Output

Provide the final email as copy-ready text. If clarification is required, ask only the specific question needed to draft safely. Do not add commentary after the final copy unless the user requests alternatives, an explanation, or a revision.


---
name: professional-social-post
description: Draft, revise, and audit professional social posts with strong hooks, defensible claims, useful substance, and privacy-aware publishing controls.
---

# Write a professional social post

Use this workflow to draft, revise, critique, or promote a professional social post from notes, a draft, an article, a transcript, a podcast, research, a carousel, or a simple topic.

The goal is not to make a person or organization sound enthusiastic. The goal is to make the right reader stop, understand a useful point, and have a reason to care. A strong post is specific, defensible, easy to read on a phone, and useful even if the reader never opens a link.

This workflow is platform-independent. Adapt formatting, link placement, length, publishing steps, and delivery method to the user’s chosen platform and access controls.

## Start with the brief

Before drafting, gather or confirm the minimum information needed to make sound decisions:

- **Platform and format:** text post, caption, thread, document carousel, article promotion, or another format.
- **Audience:** for example, technical practitioners, founders, researchers, policy professionals, customers, candidates, or a specialist community.
- **Purpose:** share an insight, explain a concept, announce a change, promote a longer piece, invite substantive discussion, or support a campaign.
- **Point of view:** personal, team, or organizational voice.
- **Voice constraints:** formal or conversational; preferred and prohibited words; punctuation preferences; desired length; examples of approved writing.
- **Evidence:** the sources that support claims, including the status of figures, quotations, names, results, and dates.
- **Publication permissions:** what may be named, quoted, linked, attributed, or disclosed publicly.
- **Link strategy:** whether a link is needed and where the user’s platform strategy places it.
- **Delivery boundary:** who may see drafts, source materials, final copy, and any publishing instructions.

If the user has a writing guide, approved posts, audience research, or brand guidance, use those materials as the primary voice reference. Do not assume a particular person’s writing style, private records, storage location, or publishing system.

### Privacy, consent, and data boundary

When source material includes private communications, personnel records, participant stories, customer information, health information, financial details, performance records, or other personal data, pause before extracting material for a public post.

Confirm all of the following where relevant:

1. **Legitimate purpose:** There is a clear, appropriate reason to use the information in this post.
2. **Clear authorization:** The requester has authority to use the source, and the person or organization represented has approved the intended disclosure where approval is needed.
3. **Consent and expectations:** The use matches any consent given and does not exceed reasonable privacy expectations. Information supplied privately is not automatically approved for public publication.
4. **Minimum necessary information:** Use only details needed to make the post’s point. Remove unrelated biographical, personal, sensitive, or identifying information.
5. **Sensitive-data review:** Avoid publishing protected or high-risk details, including contact information, private dates, health or disability information, family details, immigration status, compensation, disciplinary history, confidential business information, or private assessments, unless disclosure is necessary, authorized, and appropriate.
6. **Output-access boundary:** Keep drafts, supporting notes, and final copy within the authorized audience. Do not move sensitive source material into a wider-access document, chat, shared folder, or publishing queue without approval.

If authorization, consent, or appropriate public disclosure is unclear, use an anonymized and generalized version only if it still serves the purpose and cannot reasonably identify the person. Otherwise, ask for clarification or omit the material.

## Route the request before drafting

Some post types need different evidence and structure. Identify the genre early.

| Post type | Primary approach |
|---|---|
| Career or participant story | Use starting point, turning point, concrete outcome, evidence, and lesson. Confirm what personal details can be disclosed. |
| Research or evidence post | Lead with a defensible finding; explain method, limits, and implications. |
| Product or organizational announcement | Lead with the concrete change and reader relevance, not internal excitement. |
| Article, report, or podcast promotion | Lead with the strongest finding or story from the longer piece, not “new article” or “new episode.” |
| Carousel or document caption | Give the central claim plus one or two strong specifics, then explain what the visual material adds. |
| Hiring or assessment post | Focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether the assessment distinguishes relevant performance. |

For a personal case study, ask one concise question before writing: **What may be named, quoted, or disclosed publicly, and has the person approved that use?**

For hiring, assessment, or performance-related posts, do not disclose identifiable assessment results or private performance details without explicit authorization and a legitimate purpose. Describe the role, work sample, process, or aggregate learning instead. Avoid claims that imply a person’s general worth; discuss role-relevant evidence and fit for the work.

If the genre is unclear, ask which outcome the post should prioritize: understanding, discussion, traffic, applications, awareness, or conversion.

## Accuracy and evidence rules

These rules apply to every draft.

1. **Do not invent facts.** Do not fabricate figures, names, quotes, roles, dates, organizations, testimonials, titles, outcomes, or research findings.
2. **Separate evidence from interpretation.** State what the material shows, then label the recommendation, inference, or opinion.
3. **Preserve material uncertainty.** If the evidence is uncertain, assumptions are strong, ranges are wide, or the result is correlational, say so plainly.
4. **Use exact supported details.** Specific figures and outcomes are often stronger than broad language, but do not convert an estimate into false precision.
5. **Request missing support early.** When a central claim is unsupported, ask for a source, remove it, or narrow it.
6. **Avoid misleading urgency.** A defined risk and a proportionate response are more credible than dramatic claims made for attention.
7. **Use social proof responsibly.** Named outcomes and testimonials require authorization, context, accurate attribution, and a clear public-use basis.
8. **Protect confidential information.** A fact may be true and still be inappropriate to publish. Do not reveal confidential plans, nonpublic metrics, private communications, or commercially sensitive details without approval.

## Audience and voice

Write for the reader most likely to benefit from or act on the post, not for everyone who might vaguely relate to it. Specificity helps the right reader recognize that the post is for them.

Use these default voice rules unless the user supplies better ones:

- Direct, clear, and conversational.
- Short sentences and concrete nouns.
- Active voice where it improves clarity.
- One main claim per sentence.
- Sober about problems and practical about responses.
- Specific rather than promotional.
- Confident only where the evidence warrants confidence.

Avoid these recurring failure modes:

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are thrilled to announce an exciting initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences with unexplained terminology. | Make one clear claim, then explain necessary terms in ordinary language. |
| Alarmist | Broad catastrophe language without a mechanism or response. | Name the risk, evidence, uncertainty, and a useful intervention. |

## Core workflow

### 1. Inspect the source before choosing a template

Do not begin by filling in a format. Read the source and find the strongest material inside it. The formal title or headline is often not the best social angle.

Look for:

- An unusual fact.
- A specific number that creates tension.
- A counterintuitive conclusion that can be defended.
- A concrete outcome or before-and-after change.
- A meaningful trade-off or deliberate constraint.
- A sharp disagreement between credible views.
- A useful framework, checklist, or model.
- A sentence that changes how the reader sees the issue.

During source review, extract only material relevant to the stated post purpose. Do not copy sensitive notes or personal details into working drafts merely because they are available. If an example can make the same point with fewer identifying details, use the less revealing version.

If more than one angle is plausible, do not silently choose. Present two to four options and explain what each foregrounds.

**Angle-selection prompt:**

> I see several viable directions. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [specific story or outcome]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Choose one primary thread. A social post should not summarize every part of the source.

### 2. Generate hooks before drafting the body

The first line determines whether readers continue. Generate five to ten candidate hooks before settling on one. When user choice would be helpful, present a numbered shortlist of three to five, each with a brief strategic note.

A hook makes an honest promise that the body fulfills. It should work on its own and create interest without relying on empty suspense.

Useful patterns include:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Approved outcome:** “[Role or approved person] moved from [starting point] to [specific outcome] in [timeframe].”
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only if the post supports it.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused disagreement:** “Why do two credible groups reach different conclusions about [specific issue]?”

| Hook | Strategic purpose |
|---|---|
| “[Specific result or claim].” | Leads with a concrete payoff and creates a reason to continue. |

Use the swap test: if a key topic word could be replaced with “marketing,” “leadership,” or another unrelated subject and the hook still works, the hook is probably too generic.

Avoid generic announcement openings, throat-clearing, multiple rhetorical questions, vague inspiration, and clickbait such as “You will not believe” or “This changes everything.” Do not use an individual’s sensitive story as a hook unless the disclosure is authorized, necessary, and proportionate.

### 3. Select one structure

Pick the structure that best fits the material. Do not combine multiple structures unless there is a clear reason.

1. **Counterintuitive claim → evidence → implication**  
   Best for data, research, and argument posts.

2. **Changed mind → trigger → updated view → takeaway**  
   Best for thoughtful first-person posts.

3. **Problem → why it matters → practical response**  
   Best for explainers, policy, and operational content.

4. **Result → how it happened → reusable lesson**  
   Best for real outcomes, launches, and authorized case studies.

5. **Framework → examples → application**  
   Best for material readers may save and revisit.

6. **Specific announcement → reader relevance → next step**  
   Use only when the announcement itself is notable.

7. **Strategic trade-off → rationale → consequence**  
   Use when explaining an intentional constraint or “anti-goal”: something the organization has deliberately chosen not to optimize for, and why.

### 4. Draft: hook, tension, payoff, close

Use this default body shape:

- **Hook:** the strongest claim, result, or tension.
- **Tension or setup:** why the point matters or what assumption it challenges.
- **Payoff:** the evidence, story, framework, or practical insight.
- **Soft close:** exactly one focused question, takeaway, or pointer.

A useful default is under 300 words, adjusted for platform and substance. Every extra line should earn its place. Use one- or two-sentence paragraphs so the post scans well on a phone. A dense block of text is easy to skip.

Use lists only when the content is genuinely list-shaped: three findings, four choices, a process, or a checklist. Do not turn ordinary flowing prose into bullets merely to create visual activity.

For a carousel or document caption:

- Establish the central idea in the caption.
- Include one or two meaningful specifics.
- Explain what the visual material contains.
- Do not reproduce every slide.
- Ensure images, screenshots, quotations, and case examples meet the same authorization and privacy standard as the caption.

For an article, report, or podcast promotion:

- Put the most useful finding in the post.
- Use the linked material for depth, sources, and expanded analysis.
- Follow the user’s platform-specific link strategy.
- Never make the request to click the main value proposition.
- Do not link to restricted, private, or sensitive materials from a public post.

## Calls to action

Use one close only. A strong close gives the reader a real and bounded way to respond.

Good examples:

- “Which constraint matters most in your work?”
- “What evidence would change your view?”
- “The full analysis includes the assumptions and sources.”
- “If you have operated a similar system, where does this model fail?”

Weak examples include “Thoughts?”, “Let me know what you think,” several questions at once, or requests to react, repost, tag people, or comment merely to increase reach.

A question should invite knowledge, disagreement, or relevant professional experience. Do not use engagement bait or invite people to disclose confidential, personal, or sensitive details in public comments.

## Editing pass: remove inflated language

Run a separate editing pass after drafting. Replace polished language that says little with plain, concrete language.

Cut or rewrite:

- Corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Hedging frames such as “it is worth noting” and “one might say,” unless uncertainty itself is important.
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Abstract nouns such as “journey,” “transformation,” and “paradigm” when a concrete event can be named.
- Transition sentences that merely restate the previous paragraph.
- Dramatic frames such as “The truth is” or “Here is the reality.” State the point directly.
- Decorative punctuation or formatting that the intended platform does not render correctly.

Favor periods, commas, and line breaks over theatrical punctuation unless the user has a stated preference. Use emphasis sparingly and only if the platform supports it reliably. Read the draft aloud: if it sounds like a generic thought-leadership template rather than a person making a specific point, rewrite it.

## Revision protocol

When the user gives feedback, revise the flagged line and nearby logic first. Do not rebuild the entire post unless requested.

- If the hook is not sharp enough, provide several replacement hooks before changing the body.
- If a claim feels overstated, improve the evidence, narrow the claim, or add a necessary limitation.
- If a paragraph is slow, remove setup before adding explanation.
- If the user prefers an earlier strong sentence, preserve it unless there is a clear reason to change it.
- If feedback requests more personal detail, recheck authorization, necessity, consent, and the intended audience before adding it.

Multiple small options are often more useful than a complete redraft, especially for hooks, closers, and uncertain lines. Be candid about weak material rather than presenting it as finished.

## Readiness gate and audit

Do not present a post as final until it passes this audit:

- Does the first line earn attention when read alone?
- Is the post about one clear point?
- Does it include a concrete detail, example, outcome, number, or mechanism where appropriate?
- Could a knowledgeable reader challenge the main claim, and could the author defend it with available evidence?
- Does the post provide value without requiring a click, swipe, or purchase?
- Is material uncertainty stated?
- Is the language specific to this subject rather than reusable across any industry?
- Is the close one focused action, question, or pointer?
- Are all names, quotations, figures, images, and claims supported and authorized?
- For personal or sensitive material, is there a legitimate purpose, clear authorization, appropriate consent, and a minimum-necessary disclosure?
- Does the post avoid disclosing confidential, private, or restricted information?
- Is the final draft shared only with people authorized to access it?
- Does the formatting work on the chosen platform?
- Is the tone professional, respectful, and suitable for the intended audience?

If any answer is no, revise before handoff.

## Handoff format

Provide only what helps the user decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen delivery format or authorized location.
3. Any unsupported claim, missing input, uncertain line, or permission issue.
4. Suggested first-comment or link text, if relevant to the selected platform strategy.
5. A concise publishing reminder, such as responding promptly and substantively to genuine comments.

Keep source excerpts, personal data, and confidential evidence out of the handoff unless the recipient is authorized to access them and they are necessary for review. When in doubt, provide a redacted summary and request approval through the user’s chosen process.

Do not promise that a format, timing tactic, or engagement metric will improve distribution. Platform behavior changes. Treat publishing advice as a testable hypothesis and compare results across several posts.

## Common failure patterns

| Failure pattern | Fix |
|---|---|
| Announcement disguised as content | Lead with the actual change, lesson, or reader consequence. |
| Pure teaser | Share the central finding in the post; use the link for depth. |
| Unsupported precision | Verify the figure, add scope and caveats, or remove it. |
| Generic inspiration | Name the action, mechanism, evidence, or trade-off. |
| Overpacked summary | Choose one thread and save the rest for the source or future posts. |
| Bolted-on promotion | Remove the pitch, create a dedicated promotional post, or make the connection immediate and concrete. |
| Forced engagement | Ask one real question or end with a useful conclusion. |
| Sensitive personal disclosure | Confirm legitimate purpose, authorization, consent, and minimum necessary detail before publishing. |
| Private source treated as public | Do not publish, quote, link, or circulate it without a clear public-use basis and appropriate access controls. |
| Draft shared too broadly | Use the user’s authorized delivery channel and remove sensitive supporting material from the handoff. |

The final standard is simple: the post should sound like someone with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, a generic social-media template, or a disclosure that exceeds its legitimate purpose.


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
description: Create eight article-grounded cover-image options through five concepts, visual review, and three evidence-based improvements in any chosen image generator.
---

# Create editorial cover images

Turn an article into eight finished editorial cover-image options. Develop five distinct concepts, generate and inspect every result, then create three improvements based on what the rendered images actually reveal. The user chooses from finished images that have a clear, honest connection to the article.

Use the user's chosen image generator, publishing destination, and delivery method. Do not assume a particular service, account, medium, aspect ratio, palette, or visual aesthetic. If the user explicitly requests prompts only, use the prompt-only branch rather than generating images.

## Purpose, authorization, and boundaries

Work from the complete article, not from a title alone. If the article is unpublished, confidential, or includes personal information, confirm that the user is authorized to use it for this purpose. Send only the minimum visual brief required to the selected generator. Do not paste full unpublished copy, private correspondence, sensitive facts, unrelated names, or identifying details unless they are necessary to the image and the user has clearly authorized their use.

Do not invent scenes, events, identities, or claims that the article does not support. A metaphor may interpret an idea, but it should not falsely present a real event as a factual depiction. Respect access controls, account permissions, spending limits, approval gates, consent expectations, and the intended audience for the final image.

## Establish the brief

Read the article from beginning to end before creating concepts. If the copy is missing, request it before generating. A title rarely provides enough information to create an image that belongs specifically to the piece.

Identify the following internally and use them to guide the work:

- **Central move:** the idea, shift in perspective, or conclusion a reader should retain.
- **Emotional progression:** where the piece is quiet, tense, hopeful, defiant, reflective, or resolved.
- **Concrete source material:** images, actions, settings, symbols, and metaphors already present in the writing.
- **Tone:** the article's voice and level of seriousness, intimacy, energy, or restraint.
- **Publication context:** where the image will appear, how small it may be displayed, and whether later typography will be added.

Do not begin with a long summary unless the user requests one. Translate this understanding into visual choices instead.

Reuse preferences already supplied in the conversation. Ask only for missing choices that would materially change the image. Group related questions together and collect all outstanding answers before treating a partial response as the complete brief.

Ask about these areas when they remain unclear:

- **Mood:** Offer three or four interpretations tied to actual beats in the article. For example, distinguish a contemplative opening from a more forward-moving conclusion rather than offering generic labels alone.
- **Subject:** Establish whether the image should use a human figure, landscape, symbolic object, abstract composition, or another article-appropriate subject. Respect restrictions about faces, bodies, places, cultural references, or factual depictions.
- **Palette:** Offer a small set of palettes appropriate to the mood. Name specific colors and describe contrast, value, and lightness so the choice does not depend only on color labels.
- **Orientation and crop:** Determine the intended placement: wide header, social preview, square tile, portrait cover, or a user-supplied dimension. Verify the destination's requirements when possible rather than assuming a universal ratio.
- **Medium or style:** Establish photography, watercolor, ink, collage, charcoal, digital painting, or another treatment if the user has not already specified one.

Keep a short working brief with the confirmed format, generator, mood, subject constraints, palette, medium, and any required empty space for text. Carry this brief through both rounds without repeatedly asking the same questions.

## Propose five distinct concepts

Present exactly five initial concepts in a numbered list. Each concept must include:

1. A short title.
2. A one- to three-sentence description of what the viewer sees.
3. A brief statement of the article idea or emotional beat it expresses.

The five concepts must differ in subject, composition, visual metaphor, or emotional emphasis. Five minor variations on the same scene are not a useful range. Unless user constraints rule them out, include at least one landscape-only option and one single-object or symbolic option. A human figure can be effective, but it should serve the article rather than become an automatic default.

For every concept, ask: could this image reasonably accompany many unrelated articles on the same topic? If yes, replace it with something more grounded in this article's actual language, movement, or insight.

Give a one-line initial recommendation, then generate all five concepts when finished images are requested. Do not make the user choose before the first visual round unless they explicitly ask to select concepts first.

## Write effective visual prompts

Write one self-contained prompt per concept. The prompt should be precise enough to render, but should not pile up competing instructions. Use the following structure, merging sections only when doing so improves clarity:

```text
Create one image: [medium, format, and overall editorial character].

Subject: [what is visible, what it is doing, its prominence and position. Put relevant exclusions here, such as no visible face, no logo, or no lettering.]

Setting: [surroundings, depth, foreground and background relationships, and what recedes from view.]

Light and palette: [time of day or light direction, named colors, contrast, and visible color transitions.]

Technique: [the medium's actual marks, texture, edge treatment, level of detail, and use of negative space.]

Mood: [the feeling and its connection to the article's central move.]

Composition: [focal point, eye path, placement of major forms, crop, aspect ratio, and reserved space if needed.]

Avoid: [only artifacts, visual conventions, or content that conflict with the brief.]
```

Name colors and their relationships rather than relying on vague directions such as “warm” or “moody.” For example, “pale ochre ground against muted violet shadows and a cool blue-gray horizon” gives more useful direction than “dramatic golden-hour light.” Use palette examples to make the selected direction concrete, not to impose a fixed palette on every assignment.

Describe the physical behavior of the chosen medium. Watercolor may need transparent washes, pigment blooms, softened edges, paper texture, and unpainted space. Charcoal may need broad tonal masses, broken edges, and visible tooth of paper. Photography may need lens distance, depth of field, natural light direction, and believable materials. Do not combine incompatible instructions merely because they sound attractive.

Put important exclusions beside the relevant positive instruction as well as in the final avoidance list. For example, say “a back-turned silhouette with no facial detail” in the subject description, not only “avoid faces” at the end. Specify whether the image should contain no text, borders, logos, or watermark-like marks.

Send the generator only the visual prompt needed for that image. Explicitly request that it create an image, so a text explanation is not mistaken for a completed result.

## Generate the first five

Use the chosen generator's supported workflow. If browser or account access is required, use the authorized account and current supported controls. Do not take over unrelated workspaces or conversations. If access is unavailable, an approval gate blocks action, or a rate limit applies, report the blocker and ask for only the action needed to continue. Do not silently send the article to another service as a substitute.

Maintain a working record for each option: number, title, concept, full submitted prompt, generation status, output location, and visual-review notes. Preserve the exact prompt so a truncated or failed request can be repaired accurately.

Independent jobs may be started without waiting for each image to finish when the tool supports this safely. Keep browser actions sequential, grounded in the current page state, and within the generator's limits. Confirm that each submission contains the complete intended prompt. If text is cut off, cancel or correct the incomplete attempt and resend the complete brief.

A submitted prompt, spinner, thumbnail placeholder, elapsed time, or text response is not proof of completion. Confirm that a real image has rendered and can be opened at useful size. If an error appears, check whether an image was nonetheless completed before retrying, to avoid duplicate output. Keep unsuccessful attempts separate from the five finished options.

## Inspect all five before improving

View every completed image at useful size. Evaluate the actual pixels, not the generator's description or the intended prompt. Also inspect a small preview or reduced crop, because editorial covers often need to communicate quickly at thumbnail size.

For each option, assess:

- Whether it communicates the central idea and emotional tone.
- Whether the subject and action read immediately and have a clear focal point.
- Whether the requested style, palette, orientation, and composition survived generation.
- Whether it feels too busy, generic, sentimental, static, overly literal, or visually confusing.
- Whether anatomy, objects, perspective, construction, lettering, or other visible artifacts undermine it.

Only after all five have been inspected, write three new prompts. Each improved prompt must name, in working notes, a visible strength to retain, a weakness to correct, and a concrete visual change likely to help. Do not prewrite the second round before reviewing the first results.

A useful second-round spread is often: one refinement of the strongest result, one combination of strengths from different results, and one new concept that addresses an uncovered gap. This is a guide, not a rigid formula. Choose another distribution if it better serves the article.

Correct causes rather than decorating symptoms. If an image is cluttered, reduce competing objects and focal points before adding detail. If a painting looks like a photograph with a filter applied, request fewer large forms, selective edges, visible medium marks, and more negative space. If a scene reads as generic travel, business, or lifestyle imagery, reconsider the action or metaphor instead of adding ornamental detail.

Give the user a short progress update on what the first round revealed and what the next three will improve. Continue without asking for another selection unless the user requests a pause.

## Generate, review, and deliver options six through eight

Generate three images from the revised prompts. Keep the first five intact so the user can compare originals and improvements. Inspect each new result with the same completion checks and visual criteria. If a generation fails or returns only text, repair it where possible in the same task context. Do not count a failed attempt as a finished option and do not quietly substitute an older image.

Before delivery, verify that there are eight distinct completed images that you personally inspected. Confirm that titles, numbering, prompts, and output locations match the working record. Preserve the final outputs using the generator's supported links, assets, tabs, or files so the user can compare them.

Give a short recommendation based on the rendered work, explaining why the strongest option fits the article. Then provide a numbered list of all eight titles and verified output locations, clearly marking options six through eight as the second round. Make that list the final deliverable block. If output is delivered through browser tabs, leave the finished tabs open and clearly identifiable when the environment supports doing so.

If access restrictions, rate limits, or repeated errors prevent completion, state exactly which options are finished and which are blocked. Preserve useful partial work for resumption. Never claim that eight images exist when some are only prompts, placeholders, or unsuccessful attempts.

## Prompt-only branch

When the user explicitly requests prompts only, do not generate images. Read the article, establish the same creative brief, and propose five concepts. Wait for a selection unless the user already selected concepts or requested prompts for all five.

Write each selected prompt in a separate fenced code block using the prompt structure above. If combining concepts, provide one sentence describing what is being combined before the prompt. Put the selected prompts last, with nothing after the final code block.

Do not describe hypothetical second-round prompts as though they were informed by visual review. No visual review occurred in this branch.

## Adapt to another generator

When the user requests a version for another generator, preserve the core concept, mood, palette, composition, and format. Change only the syntax and structure required by the target tool. A prose-oriented tool may use a compact paragraph, while another tool may work best with short descriptive phrases and supported controls.

Verify current conventions before adding parameter flags, version identifiers, style codes, or aspect-ratio syntax. If a version choice materially affects the result and is unclear, ask once rather than guessing. Keep platform variants separate and clearly labeled. Changing tools should not quietly change the underlying image idea.

## Learn from completed work

After the user chooses an image, accepts a prompt, or clearly ends iteration, identify durable lessons from explicit feedback and observed results. Useful lessons include better ways to translate article structure into a visual metaphor, constrain composition, describe a medium, or avoid a repeated generator failure.

Separate stated user preferences from personal aesthetic judgment. Do not save article-specific names, private content, sensitive facts, or one-off subject matter as a general rule. Do not treat a single successful image as a permanent default. Save or apply a reusable lesson only when the user has authorized memory or workflow updates; otherwise use the lesson only within the current task.


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
description: Diagnose why someone is stuck, use one brief matched intervention, start a bounded work block, and learn from the result without making coaching another avoidance ritual.
---

# Get unstuck

Use this workflow when a person cannot start, has lost momentum, dreads a task, feels depleted, or keeps being pulled into distraction. It is a 10–15 minute rescue process, not a complete productivity system. Its aim is to help the person begin one useful, bounded block of work—not finish the entire task.

Before reviewing prior notes, communications, calendars, documents, or work records, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources, do not expose unrelated or sensitive personal information, and keep any output within the person’s authorized access boundary.

## Operating principles

1. **Diagnose before prescribing.** Avoidance can come from physical depletion, emotional dread, an unclear next action, or an environment full of easier rewards. More than one cause may be active.
2. **Work in order: physical, emotional, cognitive.** Do not ask an exhausted or shame-flooded person to solve a complex planning problem first.
3. **Choose a coaching style deliberately.** Name the style briefly and invite the person to request a switch.
4. **Make success small and observable.** Success is starting a relevant action and completing one bounded work block if feasible. Rough work counts.
5. **Keep the rescue shorter than the work.** If the conversation becomes a substitute for action, it has failed.
6. **Learn from outcomes, not assumptions.** With permission, use a minimal session record to identify patterns over several sessions.

Do not frame avoidance as laziness or a character defect. Avoidance often brings immediate relief from discomfort, which makes it likely to repeat. Motivation may follow action rather than precede it.

## When to use this workflow

Use it for statements such as:

- “I can’t get started.”
- “I’m avoiding this task.”
- “I keep checking my phone instead of working.”
- “I’m tired and can’t face this.”
- “I know what I should do, but I’m not doing it.”

Use a problem-solving or planning workflow instead when the person has sufficient energy and willingness but lacks technical knowledge, required information, or a defined problem. This process addresses activation and avoidance, not every difficult task.

## Step 0: Diagnose the state

Ask one compact message with no extended preamble:

1. **What is the task in one line?** Skip if it is already clear.
2. **Rate these from 0–10:** tiredness, dread of the content, uncertainty about the next step, and pull toward distraction.
3. **How much time is available before the next commitment?**

If the person has opted into a session record, review only a small recent sample before responding. Look for repeated style preferences, interventions that helped or failed, and recurring combinations of blockers. Do not quote the record back unless the person asks.

### Decision rules for the diagnosis

- The highest score is the initial **dominant blocker**.
- If two or more scores are **5 or above**, treat the situation as a **compound state**. Address more than one blocker, but still use the physical → emotional → cognitive order.
- If tiredness is **below 4**, do not assume capacity is the problem; focus on the higher-scoring blocker.
- If tiredness is **4 or below**, do a short physical reset before demanding cognitive work.
- If tiredness is **6 or above**, or dread is **7 or above**, use a physical reset before any detailed decomposition.
- If dread is **5 or above**, include one emotional intervention before or alongside cognitive task reduction.
- If distraction is high but dread is low, treat the environment as the first problem. Do not rely on willpower while the distraction remains immediately available.

### Capacity escalation

Check for a recurring red pattern only when authorized session history exists. If both tiredness and dread have been **7 or higher across about five recent sessions**, treat this as a capacity warning rather than an ordinary motivation problem.

Say something direct, such as:

> “This has looked like high depletion and high dread repeatedly. It may be a capacity problem, not a discipline problem. What is the case for not doing this today? Could it be delegated, reduced, or deferred for a short period? What would genuinely restore capacity?”

Do not immediately steer the person back into a work block. Hold the boundary long enough to consider deferral, delegation, workload reduction, rest, or support from an appropriate person.

If the person still chooses to proceed, acknowledge that they are working against a warning signal and reduce the task to the smallest safe and useful action. If there are signs of acute distress, inability to meet basic needs, or risk of self-harm, prioritize immediate local support, emergency services where appropriate, or qualified professional help rather than productivity coaching.

## Step 1: Choose and name the style

State the chosen style in one sentence:

> “I’m going to be practical and warm for this one. Tell me to switch if it isn’t helping.”

Use these defaults unless the person expresses a preference or authorized history shows a different approach works better.

| Dominant state | Default style | Decision rule |
|---|---|---|
| High dread, adequate energy | Empathetic or analytical | Use empathy when emotions are prominent; use analysis when the person is calm and wants to reason through resistance. |
| High uncertainty, low dread | Analytical | Break the work into visible actions and remove ambiguity. |
| High distraction, low dread | Direct | Interrupt the cue-reward loop quickly and change the environment. |
| High tiredness | Practical-warm | Be brief, realistic, and reduce demands without becoming vague. |
| Compound state | Practical-warm | Acknowledge the load, then give one clear next action. |
| Explicit same-day request for firmness | Direct | Use only when physical capacity is adequate and the person agrees the task matters. |

Switch styles when evidence says the current one is not landing:

- If the person says “just tell me what to do,” stop elaborating and become direct.
- If they say the framing makes them feel worse, become self-critical, make self-deprecating jokes, or go quiet after pressure, switch to empathy and reduce the task.
- If they argue with the framing, switch to analytical and examine the obstacle together.
- If they ask for a firmer tone, confirm that they want it for this session. Do not use insults, shame, contempt, or coercive language.

A drill-like style is never a default. It is inappropriate for a depleted, overwhelmed, or shame-flooded person.

## Step 2: Run one matched intervention

Use the minimum effective intervention. Do not stack every technique merely because several are available.

### A. Physical reset

Run this first if tiredness is 4 or below, tiredness is 6 or above, or dread is intense enough to make the person feel physically flooded. The purpose is to change state, not create a long break.

Offer a bounded sequence:

- Drink a glass of water.
- Move for about five minutes: walk outside, climb stairs, stretch, or take brisk steps.
- Get daylight or stand near a bright window where possible.
- Leave the distracting device behind during the reset.
- Optionally use cool water on the face, a small snack, or a non-disruptive drink.

Keep an unstructured reset to **10 minutes or less**. A structured outing may last up to **20 minutes** only if it has all three of these features:

1. a named destination,
2. a small defined reward, and
3. a specific return cue or time.

Ask the person to state the plan before leaving. If they request a reasonable break, respect it and bound it. Do not repeatedly extend breaks without making a new explicit decision.

Avoid recommending stimulant use late in the day when it is likely to harm sleep. The aim is a manageable state shift, not artificial intensity.

### B. Emotional intervention

Use one emotional intervention when dread is 5 or above or when shame appears. Shame signals include harsh self-labels, statements such as “I can’t even do one simple thing,” self-deprecating humor, or silence after a directive.

Choose one tool:

- **Self-compassion break:** “This is hard right now. Difficulty is part of being human. May I be kind to myself while I take the next step.”
- **Defusion:** “I’m having the thought that ___.” The phrase creates distance without requiring the person to prove the thought false.
- **Values anchor:** “This matters because ___.” Connect the task to a role, commitment, or value the person recognizes.
- **Importance reframe:** For a calm, analytical person only: “Strong avoidance can mean the work matters. The feeling is a threshold, not evidence that you cannot do it.”

Do not use the importance reframe when someone is overwhelmed. It can add pressure. When shame is present, switch to self-compassion and task reduction rather than pushing harder.

### C. Cognitive intervention

Once the person is physically settled enough and the emotional threat is lower, make the work mechanical.

1. **Replace abstract language with visible verbs.** Change “prepare the report” to “open the brief and list the required sections.”
2. **Find the 30-second first action.** This may be opening a file, locating one source, creating a heading, or writing a deliberately rough sentence.
3. **Use an if–then plan.** Require this format: “If it is [cue or time], then I will [action] at [place].” Ask the person to say it once.
4. **Time-box rather than outcome-box.** Use 25 minutes by default. Use 10–15 minutes when energy is very low. When the timer ends, stopping is allowed; do not turn an open-ended task into “just five more minutes” by default.

For tasks involving authorized searchable material, offer practical task assistance, not only encouragement. For example, help locate relevant messages, meeting notes, documents, or records; extract task-relevant facts into a scratchpad; or build a source list. Access only authorized material and omit unrelated personal details. Removing the blank-page problem can reduce dread substantially.

## Step 3: Start the work block

State the duration plainly. Confirm the environment:

- Put the phone in another room or otherwise out of reach.
- Keep one relevant document or tab open where feasible.
- Close, block, or sign out of high-pull distractions.
- Keep only the materials needed for the first action visible.

Then stop coaching. Do not keep a motivational conversation running during the block unless the person needs active, task-specific help. Working matters more than reporting progress.

## Step 4: End-of-block check

When the person returns, ask only:

1. “What came out of the block, in one sentence?”
2. “What are tiredness and dread now, each from 0–10?”
3. “Another block, or stop?”

If they stop, acknowledge the concrete success:

> “You showed up for the task when it was difficult. That counts.”

Then end the rescue. Do not pressure them into another block.

If they continue, repeat the same timer and environment. Re-diagnose only when their state has clearly changed.

## Step 5: Record and improve, with permission

If the person opts into records, append a concise entry in their chosen secure system. Avoid unnecessary sensitive details. Use a consistent format:

```text
## [date and time] — [brief task label]

- Start state: tired [0–10], dread [0–10], unclear [0–10], distraction [0–10]
- Dominant mode: [tired / dread / unclear / distraction / compound / capacity]
- Style: [direct / analytical / empathetic / practical-warm]
- Interventions: [short list]
- Work blocks: [count and duration]
- Outcome: [started yes/no; brief result; end state]
- What helped: [one line]
- What did not help: [one line]
- Next adjustment: [one line]
```

Review patterns after enough sessions to distinguish a trend from a one-off. A useful rule is to consider an adjustment when the same style or intervention has clearly helped or failed in **three or more recent comparable sessions**. Demote repeatedly unhelpful styles, elevate consistently useful interventions for the relevant state, and revise prompts that the person dislikes. Do not make changes merely to appear adaptive.

## Failure modes and safeguards

- **The rescue becomes procrastination:** Cap diagnosis and intervention at about 15 minutes. Then either start badly with the 30-second action or stop and address capacity.
- **A break expands indefinitely:** Set a duration and return cue before the break begins.
- **Pressure worsens shame:** Switch immediately to compassion and a smaller task.
- **Planning replaces action:** Return to the first visible action and start a timer.
- **Distraction is treated as a willpower test:** Change the environment and separate the competing device or cue.
- **A capacity problem is treated as a discipline problem:** Consider deferral, delegation, reduction, recovery, or appropriate support.
- **Private data is overused:** Review only authorized, task-relevant sources and retain only what is necessary.

The standard for success is intentionally modest: start a relevant action, complete one bounded block when feasible, and leave with better evidence about what helps next time.


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
description: Plan travel around its purpose, compare complete current journeys, and prepare or complete authorized bookings with clear decisions and privacy-aware research.
---

# Plan and book a trip

Plan transport around the trip the traveler actually wants, rather than allowing an early fare search to define the trip. Establish the purpose and constraints first, research a small set of complete current options, recommend a practical choice, and prepare or complete a booking only within clear authorization.

Treat current traveler instructions as authoritative. Earlier trips, calendar entries, receipts, and saved preferences are context, not permanent instructions. Do not turn a one-time fare, date choice, upgrade, or event plan into a lasting default.

## Operating principles

1. **Understand before optimizing.** Do not begin broad fare shopping, upgrade research, or checkout preparation while material trip questions remain unanswered, unless the traveler explicitly requests a narrow check or asks to skip discovery.
2. **Research facts; ask about intent.** Retrieve accessible factual details from authorized sources. Ask the traveler about goals, priorities, and trade-offs that records cannot establish.
3. **Compare whole journeys.** Consider flights or trains, airport and station choice, transfers, connection risk, accommodation needs, and usable time together. A cheap ticket is not necessarily a good journey.
4. **Verify the actual product.** Confirm the operating provider, route, fare family, cabin or class, baggage, seat availability, and material terms. Generic labels such as “premium,” “first class,” or “extra legroom” are not enough.
5. **Keep authority boundaries clear.** Research, planning, and checkout preparation do not authorize payment. A selected fare or incomplete checkout is not a reservation.
6. **Protect privacy.** Use the minimum relevant information and sources for a legitimate travel-planning purpose. Keep findings within the approved access boundary and omit unrelated or sensitive personal details.
7. **State uncertainty accurately.** Label estimates, date-grid indications, live quotes, unavailable sources, and unverified benefits. Do not make claims stronger than the evidence supports.

## 1. Discover the trip

For a new trip, begin with a focused context pass and a short interview. For a continuing trip, reuse the established brief and ask what changed. Do not restart an interview when the answers are already known.

Follow an explicit request to check a specific route, date, or fare without forcing a full discovery discussion. State assumptions that materially limit a narrow result.

### Use authorized context carefully

Read the conversation and trip material supplied by the traveler, such as invitations, agendas, accommodation details, existing itineraries, or event documents. If the traveler has clearly authorized access to relevant calendars, travel correspondence, reservations, or planning records, inspect only sources and records that bear on this trip.

Access to an inbox, calendar, workspace, or account does not permit unrelated searches. Do not investigate companions, review unrelated personal communications, contact people, or write to accounts without separate authorization. Use only the minimum relevant sources and details, respect consent and privacy expectations, and keep outputs within the approved private planning space.

Look for:

- the trip purpose, event location, agenda, and attendance expectations;
- confirmed, provisional, and conflicting dates;
- companions, visits, or meetings that affect route or schedule;
- existing reservations, accommodation, local pickup, or local transport;
- commitments immediately before and after the likely travel period; and
- work obligations, reimbursement requirements, accessibility needs, and recovery needs.

Distinguish facts from inferences. An invitation is not confirmed attendance, a calendar hold is not necessarily a hard deadline, and an old receipt is not proof of a current benefit or preference. Resolve conflicts where possible and label uncertainty that remains.

If an authorized source is unavailable, say what could not be checked, use a safe alternative when permitted, and explain the resulting verification limit. Do not imply that an inaccessible source was reviewed.

### Ask questions that shape the journey

After the focused context pass, briefly state what is known and ask a compact numbered block of substantive questions. For an open-ended trip, four to six questions usually suffice; ask fewer when most answers are settled.

Use questions that develop the trip rather than merely fill booking fields:

1. **Purpose and outcomes:** What would make this trip worthwhile? Which event, visit, activity, or meeting matters most?
2. **People and places:** Who is traveling or being visited? Which stops are essential, optional, or best done in a particular order?
3. **Time:** How much time is wanted in each place? What fixes the earliest departure, required arrival, and latest return? If dates are flexible, what is the useful range?
4. **Pace and readiness:** Is the trip for work, leisure, or both? Is arriving rested, protecting a workday, or leaving unstructured time important?
5. **Practical constraints:** What accommodation, local transport, accessibility support, reimbursement rules, or spending constraints already exist?
6. **Requested outcome:** Does the traveler want research, a booking-ready recommendation, or an authorized purchase?

Do not make a numerical budget mandatory when the traveler wants to understand trade-offs first. Do not make the initial discussion about minor seat products or speculative upgrades. Carry uncertainty forward rather than inventing preferences.

### Agree the trip brief

Before detailed transport research, summarize:

- purpose, important people, and planned stops;
- desired time in each place and preferred order;
- fixed dates, arrival deadlines, and useful flexibility ranges;
- work, rest, and recovery needs;
- known accommodation and local transport;
- relevant standing preferences; and
- unresolved choices that could materially change the plan.

Give the traveler an opportunity to correct the brief. Clear answers establish agreement; do not require a separate approval ritual once a choice is clear. Keep tentative dates visibly marked as provisional.

Do not move to broad fare research until material choices are resolved. If available transport would meaningfully change the trip, return to the traveler with that decision instead of silently reshaping the plan.

## 2. Establish relevant transport preferences

Ask only about preferences that are unknown and materially affect the choices. Saved preferences are defaults, not commands, and may be overridden for a particular trip. Do not assume that a preferred provider, airport, cabin, train class, or loyalty program is always best.

Relevant preference areas may include:

- nonstop versus connecting travel and acceptance of nearby airports;
- economy, true premium economy, business, or another verified cabin;
- overnight sleep needs and the importance of arriving ready for work or an event;
- seat preference and willingness to pay for confirmed seat selection;
- cabin-bag and checked-bag requirements;
- flexibility, refundability, and tolerance for separate tickets or self-transfers;
- rail class, station convenience, and border or station-arrival needs; and
- loyalty benefits, points, credits, vouchers, or upgrades, if eligibility can be verified.

Do not treat a past fare as a budget ceiling, and do not infer that flexible dates mean every day is equally acceptable.

### Overnight travel and time-zone adjustment

For long-haul travel across several time zones, assess schedule quality alongside price and cabin. Use the traveler’s normal sleep pattern, travel direction, arrival-day obligations, and ability to adjust before departure when these are available.

- **Eastbound:** Prefer options that allow meaningful sleep during the traveler’s usual biological night and leave reasonable recovery before important obligations.
- **Westbound:** Daytime travel and daylight arrival can make it easier to remain awake until a normal local bedtime.
- **Work or important events after arrival:** Give reliable sleep, recovery time, and a confirmed suitable product more weight than a modest saving. A mixed-cabin itinerary may be sensible when only one leg is especially important.

Recommend based on the actual trip, not a universal clock-time rule. Present sleep timing, light exposure, hydration, and caffeine suggestions as general travel guidance rather than medical advice.

## 3. Research current transport options

Start this stage after discovery is complete, unless the traveler explicitly narrowed the request. Search useful dates and routes against the agreed brief.

Use current schedules and fares. Route-discovery services and date grids can reveal options, but verify selected itineraries and fare conditions with the operating provider whenever practical. Prefer direct booking with the provider unless a third party offers a clear, verified advantage the traveler accepts.

### Search and verification method

1. Search useful departure times, not just the cheapest result. For overnight or long-haul travel, schedule quality may change the recommendation.
2. Compare return tickets, one-way combinations, open-jaw itineraries, nearby airports, rail alternatives, and ground transfers when they fit the brief.
3. Include transport to the true destination. An airport or central station may still leave a slow, costly, or risky onward journey.
4. Check schedule-release limits, seasonal changes, holiday disruption, planned works, border requirements, and realistic transfer times. Do not invent a precise future service or fare before it is available.
5. Verify the operating provider, fare family, named class, and material conditions. A marketing name, reseller label, or advertised “from” fare is insufficient.
6. Label every price as a **live selected itinerary**, **indicative date-grid price**, or **estimate**, with currency and check time.

If a provider, login, tool, or checkout fails, attempt permitted recovery. State the failed source, the limitation or error, the facts that remain unverified, and any substitute source used. Do not silently substitute a weaker source or imply that a blocked checkout was verified.

### Check the actual product

For every viable option, verify what the traveler would actually receive:

- Confirm each flight segment’s operating airline, cabin, fare family, connection protection, and baggage rules. Check aircraft and seating layout when sleep or comfort depends on them.
- Treat true premium economy as distinct from extra-legroom economy. Do not assume business class includes a lie-flat seat without verifying the actual service.
- Inspect mixed-cabin itineraries by segment. A higher cabin on an overnight leg and a lower cabin on a daytime leg can offer better value than upgrading everything.
- Check preferred-seat availability and any selection fee. A preference is not a confirmed assignment.
- Verify cabin-bag allowance, size, weight, and fare restrictions. A personal-item-only fare does not meet a carry-on requirement.
- For rail, verify the named class and fare conditions directly with the operator where possible. A reseller’s generic class label may not identify the actual product or flexibility rules.

### Evaluate upgrades realistically

When upgrades matter, compare these strategies where available:

1. buying the desired cabin or class outright;
2. changing an existing ticket and paying the fare difference; and
3. purchasing a separate cash, points, or loyalty upgrade.

Compare total cost before booking and incremental cost after booking. Do not assume an earlier upgrade payment applies to a later fare change.

Separate confirmed upgrades from waitlists, bids, or loyalty requests. An empty seat map does not prove an upgrade will clear. If reliable sleep or arrival readiness is important, recommend a ticket the traveler would accept even if no upgrade clears.

Verify fare eligibility, relevant benefits, points copayments, priority rules, and change, refund, or missed-upgrade terms. Do not claim there is a reliably cheapest time before departure to upgrade. Prices, availability, and seat choices can all worsen.

For an existing reservation, inspect reservation-specific upgrade offers and alternative change prices only when authenticated access is both authorized and available. Public fares do not establish a personal offer. If access is blocked, identify the exact gap and request only the smallest necessary traveler action while continuing independent comparison work.

Do not promise ongoing monitoring between conversations. Describe monitoring as active only if an authorized mechanism, schedule, itinerary access, and notification path have been verified.

## 4. Compare complete journeys

Present two or three useful options and a recommendation. If only one route meets the brief, say so rather than inventing alternatives.

Show local departure and arrival dates and times, airport or station codes where useful, total journey time, overnight arrivals, and time-zone changes. Include realistic buffers for airport arrival, security, border controls, baggage collection, station check-in, terminal changes, and travel across a city. Allow more contingency at busy periods and for independently booked connections.

Distinguish protected connections from separate tickets. Explain who bears the risk if the first service is late. Consider a longer connection or overnight stay when it protects an important event, especially if suitable accommodation is already available.

| Option | Schedule and route | Actual product | Complete cost | Main benefit | Main drawback |
|---|---|---|---|---|---|
| Recommended option | [Local dates, route, duration, connection status] | [Cabin or class by segment, fare family, seat status] | [Currency; tickets, required seat fees, transfers] | [Why it best fits the brief] | [Restriction or uncertainty] |
| Alternative | [Local dates, route, duration] | [Actual product] | [Currency and inclusions] | [Saving, flexibility, or convenience] | [Time, comfort, or risk trade-off] |

Show different currencies separately, or state the exchange-rate assumption and time if converting. Never add unlike currencies into an unexplained total.

For each option, include material change and refund restrictions, baggage allowance, required seat fees, significant ground costs, and unresolved details. Explain what additional spending buys: usable time, better sleep, a protected connection, flexibility, or lower travel effort.

## 5. Prepare and complete a booking

Lead with the recommended dates and route, the comparison, verified booking links where appropriate, quote-check time, unresolved facts, and the decision needed.

A request to find or compare transport does not authorize payment. Prepare a concrete, reviewable option before requesting any approval that is actually necessary. If the traveler has already authorized a specific purchase or a clearly defined scope and price limit, proceed within that authorization without asking again merely because checkout is next.

Before submitting an authorized purchase, verify:

| Verification item | Required check |
|---|---|
| Traveler details | Use traveler-supplied identity details exactly as required by the booking form; never invent missing details. |
| Itinerary | Confirm dates, local times, airports or stations, provider, operating carrier, routing, and connection protection. |
| Product | Confirm cabin or class on every segment, fare family, selected-seat status, baggage allowance, and accessibility needs. |
| Price and terms | Confirm total price, currency, taxes, fees, seat charges, payment scope, and material change or refund terms. |

Resolve a material mismatch, missing required detail, or price outside authorization before purchase. Do not use invented identity information, payment data, loyalty numbers, or document details.

After purchase, verify success from the provider’s confirmation, not a search result, selected fare, or partial checkout. Report the booked journey, total cost, confirmed seats, any unassigned seat, and remaining transport tasks. Keep booking references, payment records, and identity details only in the appropriate private trip record, not in a reusable workflow or shareable summary.

## 6. Monitor and improve responsibly

If the traveler requests fare or upgrade monitoring, first verify that an available authorized service can access the itinerary, run on a real schedule, and deliver alerts. Define what is monitored, the threshold or decision rule, the end date, and whether an alert merely informs the traveler or can trigger an authorized action.

Monitoring does not authorize a purchase. Stop monitoring after departure, a completed upgrade, or a changed plan. If reliable scheduling, authentication, or access is unavailable, say monitoring is not active. Never represent a one-time check as continuing monitoring.

During active use, apply corrections to current work immediately. Retain a lasting preference only when the traveler clearly indicates it applies beyond this trip and retention is authorized. Preserve qualifications such as “for overnight work travel,” and replace superseded instructions rather than accumulating contradictions.

Keep temporary facts with the trip: current fares, provisional dates, one-off exceptions, individual upgrade outcomes, and tentative preferences. Do not infer satisfaction merely because a booking succeeded. Learn from verified feedback about comfort, connection timing, and booking friction without collecting unnecessary personal history, credentials, identity documents, or payment details.

A remembered preference or workflow improvement does not create authorization to purchase, message others, access additional accounts, or expand private research.


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

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose, authorization, and operating rules

Use this workflow only for a legitimate work purpose and with clear authorization to access the selected meeting records and task system. Use the minimum relevant records and details. Do not copy unrelated personal, confidential, health, compensation, legal, or sensitive information into tasks. Keep outputs within the access boundary of the chosen task system and audience.

Before each run, apply these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries commonly misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels it as an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, statement of interest, or open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply known delegation boundaries supplied by the user or organization. Attendance at a meeting does not make the user accountable for all work in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this broadly useful default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect:

- Title, date, and time
- Meeting-record link or stable identifier
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

If an artifact was created, sent, pasted, or otherwise delivered during the meeting, treat that action as complete unless there is clear evidence of additional follow-up.

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
- Source and related links that the intended task audience may access

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
- **Notes:** context, action checklist, communication drafts, and approved links.

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
dates, why this matters, the commitment, and only necessary sensitivity.] 

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
- Each task links to an authorized source record where appropriate.
- Message drafts are ready to send and follow the user’s preferences.
- Notes contain no unnecessary sensitive or unrelated personal information.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report the essential outcome only: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and any reusable guidance changes. Keep status updates terse and factual.


---
name: turn-a-message-into-a-task
description: Read a complete conversation, research and pre-complete safe work, then create a useful task only when tracking the remaining action will help.
---

# Turn a message into a task

Use this workflow when a message, thread, email, support request, or other conversation may require follow-up. The goal is not merely to log work. The goal is to identify the real request, complete as much safe preparation as possible, and leave the user with the smallest clear remaining action.

Use only communication, task-management, document, calendar, and research capabilities the user has authorized. Do not assume a particular product, database schema, organization, or internal process.

If this workflow accesses private communications or records about people, first confirm a legitimate purpose and clear authorization. Use the minimum relevant sources and information. Keep unrelated personal, health, financial, family, performance, or other sensitive details out of the task and report unless they are necessary, authorized, and suitable for the intended access boundary.

## Core principles

- Read the entire relevant conversation before deciding what the task is.
- Treat later replies as potentially decisive. They may resolve, change, reassign, or cancel the work.
- Research selectively: a few deeply read sources are better than a blanket search.
- Draft communications and consequential actions; do not send, publish, schedule, approve, or commit on the user's behalf unless explicitly authorized.
- Never invent facts, dates, links, commitments, policies, or first-hand experience.
- Create a task only when it improves follow-through. A task should not outlive a very short finishing action.
- Make task records self-contained enough that the user can finish without reopening a long research trail.

## 1. Open the source and read the full conversation

Start with the linked or supplied message. If it points to a reply, open the parent and every reply. If it points to a top-level message, check for and read its full thread. For email, read the complete chain, including relevant quoted text. For a shared document, inspect all relevant sections, tabs, attachments, and linked materials that may contain requests, decisions, or dependencies.

Capture these points in working notes:

- The anchor message and why it triggered follow-up.
- The actual ask, including implied deliverables.
- Who is involved and who is waiting for an answer.
- Existing commitments, owners, deadlines, and dependencies.
- Links, files, records, policies, or procedures referenced.
- Later updates that affect status.

Resolve identities carefully when a system displays incomplete names. Use an authorized profile, displayed identity, or clear identifier from the conversation. Name a person or describe their role where necessary for clarity; do not rely on vague labels.

### Recency gate

Before researching or creating a record, determine whether the work is already complete, no longer needed, reassigned, or waiting on another party. Later replies deserve particular attention.

If the work appears complete, do not create duplicate work. Report the evidence and ask whether further follow-up is wanted. If status is unclear, describe the ambiguity rather than assuming work remains open.

## 2. Define the real task shape

State the task shape in working notes. This determines what “pre-completed” should mean.

| Task shape | What remains for the user | Best preparation |
|---|---|---|
| Reply owed | Answer, feedback, decision, or acknowledgement | Draft a concise, fact-checked reply |
| Artefact owed | A document, reference, introduction, analysis, or data output | Draft or assemble the artefact |
| Decision needed | A choice only the user can make | Prepare options, evidence, recommendation, and a likely reply |
| Follow-up or delegation | Chase, hand off, schedule, or monitor work | Draft the follow-up or prepare handoff details |
| Multi-part request | Several related deliverables | One coordinated plan with separated sub-parts |

Default to one task for related asks in one conversation. Split tasks only when they have different owners, materially different deadlines, or independent completion paths.

Rewrite the request as an outcome, not a message label. Prefer “Review proposal and send decision” to “Message from project group.”

## 3. Gather only relevant context

Choose sources based on the actual task, not habit. Stop when you can complete useful preparation or can name exactly what blocks it.

Useful source choices include:

- **Person-related work:** relevant prior correspondence, meeting notes, role records, documented agreements, and prior feedback. For a reference, feedback, transition, or negotiation, look for the user’s documented stance or talking points before asking them to repeat it.
- **Project or event work:** recent project messages, plans, decision logs, linked documents, schedules, and retrospective notes.
- **Data questions:** authoritative records, source datasets, prior reports, and operational correspondence that may contain underlying numbers or dates.
- **Policy or process questions:** the current approved policy, relevant precedent, and procedures from the responsible function. Where a comparable established policy exists, use it as an anchor rather than inventing a new approach.
- **Repeated asks:** search broadly for the topic, not only a person’s name. A prior answer or parallel request may avoid duplicated effort.
- **Linked materials:** open them. If a document has multiple sections, tabs, or attachments, check all potentially relevant parts before concluding that the message captures the whole ask.

Use public research only when appropriate. Prefer methods that do not expose private information through unnecessary external queries. If a source cannot be accessed or verified, say so rather than guessing.

## 4. Pre-complete the work safely

Do as much useful work as possible without making an external commitment.

For communication in the user’s voice, first consult authorized writing guidance, prior approved examples, or stated preferences. If none exists, use clear, direct language and do not claim to know the user’s personal view. Keep drafts shorter than the research brief unless detail is needed for accuracy or care.

### Drafting rules

- Draft; do not send.
- Stage a draft in the relevant conversation only when authorized and when the system supports a reversible draft state.
- Include the complete draft in task notes or the final report so it remains recoverable.
- Use readable formatting: leave a blank line before lists and write direct list items instead of unnecessary lead-ins.
- Ask one simple question when one will do; do not turn a small request into a long questionnaire.
- State future commitments as conditional unless they are already authorized.
- Route funding, approval, or exception requests through the established process rather than granting an informal approval.

For a decision, prepare a compact brief with two or three viable options, the strongest evidence for each, and a recommendation with reasons. The purpose is to reduce the user’s thinking load, not merely list information.

### Uncertainty and memory gaps

Never fabricate a fact. Mark unresolved details directly where they matter:

- `[VERIFY: confirm the date in the source record]`
- `[SEARCH: locate the current policy link]`
- `[FILL IN: personal observation or relationship context needed]`

Put essential gaps inside the draft rather than removing the affected section. A partial draft can still save framing work if the missing step is obvious. Clearly warn when it cannot be sent unchanged.

List judgment calls, sensitive relationship context, and first-hand experience the user must provide under **Remaining for the user**. Make every item specific.

## 5. Ask questions only for real forks

Before asking, check whether the user already answered the question in a prior message, planning document, decision record, or email. A documented stance is usually better than interrupting the user for the same decision again.

Ask questions only when a wrong assumption would create meaningful rework, risk, or an inappropriate commitment. If questions are needed:

1. Give a short context recap: who is involved, what has happened, what is now needed, and the relevant tension.
2. Ask two to four focused questions at most.
3. Allow combined choices and a free-text response.
4. Explain the practical consequence of each choice when helpful.

Do not ask merely to perfect metadata such as priority or category. Make a reasonable default and disclose it.

## 6. Decide whether a task record is needed

Skip task creation when the remaining action is one short sitting, such as reviewing a prepared reply, making a small edit, and sending it. In that case, provide the context and draft directly.

Create a record when one or more of these are true:

- The work is deferred or cannot be done now.
- There is a deadline, wait, dependency, or follow-up worth tracking.
- Multiple steps remain or work will span several days.
- Another person is waiting and follow-through could be lost.
- The user explicitly requested a task.

When uncertain, prefer chat-only delivery for a simple reply and a task record for longer-lived work.

## 7. Create a high-quality task record

Use the user’s chosen task system. Verify available fields and valid values instead of assuming a schema.

| Field | Guidance |
|---|---|
| Title | Imperative, specific, and short; describe the finish line |
| Status | The appropriate open status, such as “To do” |
| Due date | Only when supported by an explicit or clearly implied deadline |
| Priority | Best judgment based on stakes, waiting parties, and urgency |
| Estimate | Remaining user time, not time already spent researching |
| Area or project | Best-fit category, verified against available options |
| Notes | Context, source, prepared work, and exact remaining steps |

Use this notes template:

```markdown
**What:** [One-line outcome and who is waiting.]
**Source:** [Conversation or record link, if authorized to store it.]
**Context:**
- [Key fact or decision]
- [Key dependency or deadline]
- [Relevant supporting source]

**Pre-completed:**
[Full draft, decision brief, outline, or prepared materials. State where a draft is staged, if applicable.]

**Remaining for the user:**
- [Specific finishing action]
- [Specific verification, choice, or approval]
```

Open or re-read the saved record after creation to confirm the title, notes, links, ownership, and fields are correct.

## 8. Report back clearly

If a task record was created, report in this order:

1. What the task is.
2. What was pre-completed and where any draft is staged.
3. Metadata assumptions: priority, urgency, due date, and remaining estimate.
4. Any `[VERIFY]`, `[SEARCH]`, or `[FILL IN]` items.

If no record was created, sharply separate briefing from deliverable. Put the deliverable last so it can be copied without cleanup:

```markdown
## Context for the user (not part of the reply)
- [Ask, waiting party, key facts, assumptions, and unresolved checks.]
- [State whether a draft has been staged.]

## The reply
[Verbatim draft]
```

Do not add commentary after the reply block.

## 9. Review staged drafts after the outcome is known

Whenever a communication draft is staged, schedule a single later review where authorized and technically available. A reasonable initial delay is about one hour, adjusted for the conversation’s urgency and the user’s normal working pattern.

The review instruction should identify each staged draft, its conversation location, and where the draft text can be found. At review time:

1. Re-read the relevant conversation and determine whether the user sent a final message.
2. If a final message exists, compare it with the staged draft. Note what was cut, reworded, reordered, added, or left out.
3. Extract only general reusable lessons, such as preferred brevity, tone, ordering, conditional commitments, approval routing, or useful source types.
4. If no message has been sent, reschedule at most two additional checks with increasing intervals, then stop. The user may have deliberately chosen not to send it.

Do not repeatedly chase the user, and do not store private conversation content, individual judgments, or sensitive facts merely to improve future drafts.

## 10. Improve the workflow after each run

After delivering the task or draft, perform a brief internal quality review. Update approved workflow guidance only when the run revealed a durable, general lesson, such as a necessary source type, a tool limitation and workaround, a missing task shape, or an instruction that caused avoidable effort.

Keep improvements small and general. Do not encode names, private events, confidential facts, or one-off interpersonal judgments. If no reusable lesson emerged, make no change.

## 11. Quality audit

Before finishing, check:

- Did I read the whole relevant conversation and linked materials?
- Did I confirm the work is still open?
- Is the task outcome clear and owned by the right person?
- Did I use only necessary, authorized private information?
- Did I research enough to prepare useful work without over-researching?
- Did I draft rather than send or make an external commitment?
- Are unknown facts marked clearly rather than guessed?
- Is a task record genuinely useful?
- Can the user see exactly what remains and complete it quickly?
- If a draft was staged, is a bounded follow-up review scheduled or consciously unavailable?

If any answer is no, correct it before creating the record or delivering the draft.


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
description: Complete browser tasks safely by choosing the least invasive method, protecting authenticated context, verifying page state, and separating preparation from consequential action.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing rendered forms, collecting information from dynamic pages, testing a user flow, changing a dashboard setting, or working in an authenticated account. It applies when a plain page request or approved direct interface cannot reliably accomplish the task.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until the account, target, page state, and authorization are clear.

A successful browser-automation call does not prove that a site accepted a change. Modern applications may store state outside the visible DOM, commit only when focus leaves a control, replace controls during re-rendering, or display an error even after an operation completed. Treat browser actions as claims that require evidence.

## 1. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized API, export, webhook, form action, or other direct interface when it can accomplish the request safely.
2. **Headless browser automation.** Use this for public pages, test environments, screenshots, ordinary rendered-page extraction, and forms that do not require an established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing session, account-specific state, single sign-on, or an interaction that cannot be performed safely through the first two routes.

Before automating a page, look for an approved programmatic route. Review official documentation, ordinary form actions, page source, and visible requests made by the page. A form may send structured data to a supported endpoint, avoiding fragile UI automation.

Do not use undocumented interfaces to bypass access controls, consent boundaries, payment controls, terms, or anti-abuse protections. Do not use a live authenticated session merely as a convenience: it can interrupt the user and increases privacy and account risk.

If a site blocks automated access, do not try to evade those protections for casual research or data collection. A verified visible session can be appropriate when the user explicitly asked to complete a legitimate action on that site, has appropriate access, and the established session is necessary. Never weaken browser security, warnings, multi-factor authentication, or anti-abuse controls to make automation easier.

### Selecting an automation implementation

Choose an implementation that matches the work:

- Use a direct browser automation library or script for long text, repeated interactions, heavy client-side applications, screenshots, and workflows requiring structured retries and state dumps.
- A lightweight browser-control service may be suitable for a short, simple task such as reading one page or making one ordinary click.
- If the lightweight layer becomes unstable, loses the page, fails on large input, or cannot represent the page correctly, restart with a more robust method. Do not keep attempting to rescue a broken session.
- Keep secrets in a secure runtime mechanism such as environment variables or an authorized credential store. Never hardcode them into a script, screenshot, report, or saved page dump.

## 2. Protect identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into logs, screenshots, notes, or outputs. Respect consent, reasonable privacy expectations, and the requester's appropriate access boundary.

Before acting in an authenticated context, explicitly identify the correct account, organization, environment, and browser profile. Never infer identity from a generic window title, connection name, remembered default, or the order in which browser instances appeared.

Use these rules:

- Announce that you are taking control of a visible browser and state the purpose before doing so.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Classify the intended context, such as personal, work, test, staging, or production.
- Select the profile or browser connection that corresponds to that context; do not use a generic selector that may silently choose a recently used profile.
- Confirm the signed-in account using a reliable account indicator before opening or changing the real target.
- Confirm the destination environment and target record before making changes.
- If account identity, environment, target, or authority is unclear, stop and ask before modifying data.
- Do not reveal credentials, recovery data, session tokens, security settings, or unrelated account information in output.
- Do not disable security controls or ask the user to complete a security challenge merely to make automation more convenient.

Use an account preflight gate before actions that change data. Verify the account identity, environment, and target object first. If the automation environment has a verification marker, permission flag, or similar gate, mark the context verified only **after** the verification has genuinely passed. Never create such a marker in advance merely to unlock actions.

A useful pre-action question is: **Which account is active? Which environment is this? What exact item will change?** Resolve uncertainty before proceeding.

## 3. Establish the task boundary and authority

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, workflow, or transaction.
- The information to be entered, collected, changed, or uploaded.
- The minimum information necessary to fulfill the request.
- Missing details and decisions that require the user's judgment.
- Whether the final action is reversible.
- Whether the task sends, publishes, pays, deletes, grants access, changes a plan, changes security, or otherwise creates an external commitment.

Separate **preparation** from **commitment**. Filling fields, configuring a draft, selecting options, and assembling a preview are commonly reversible. Submitting, sending, publishing, purchasing, deleting, or applying a permanent account change may not be.

Honor an explicit request to review before submission. For a normal submission that the user already clearly authorized as part of the request, do not ask again solely because a final button exists. However, obtain confirmation immediately before a one-way or materially consequential action unless standing authority clearly covers that exact action and its impact. Examples include payments, final official submissions, irreversible deletion, publishing to an audience, access changes, and changes explicitly labeled permanent or impossible to undo.

For consequential work, use two phases:

1. **Preparation pass:** Fill or configure the page, verify values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Re-check account, target, readiness, and authorization. Then activate the final control once and verify the result.

If the page reloads, the session changes, or a component re-renders between phases, do not assume the earlier state survived. Re-inspect and restore values as needed.

## 4. Inspect the rendered page before editing

Do not start by guessing selectors, filling by numeric position, or trusting visual resemblance. Inspect the rendered page first. For every relevant control, determine:

- Element type: single-line input, text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether the field is required.
- Validation rules, maximum length, formatting behavior, disabled state, and error messages.
- Whether the apparent field is the true editable element, a wrapper, or a hidden synchronization element.
- Whether changing a control triggers a re-render or resets other controls.

Address controls by stable semantic identity: visible label, accessible name, stable record identifier, or label relationship. Do not use field indexes when semantic identifiers exist. Client-side rendering can change element order between loads and after interactions.

Before changing an existing record or setting, inspect its current state. This prevents editing the wrong item and reduces accidental overwrites.

### Generic inspection pattern

Use your selected browser capability to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

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

Do not include sensitive field values in a broadly visible diagnostic dump unless they are necessary for the task and can be stored within the correct access boundary. Lengths, field names, status, and redacted summaries are often enough.

## 5. Use the correct interaction for each control

A generic “set value” command is not reliable for every control. Use the interaction a normal user would use, then verify it.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use normal text entry | Newlines may be removed silently. |
| Multiline text area | Fill text, then move focus away | The application may commit only on blur. |
| Rich-text or content-editable editor | Focus, select existing content, use keyboard-style text entry, then blur | Direct DOM mutation may not update the internal editor model. |
| Dropdown or combobox | Open and select by visible option text, then wait for state to settle | Selection may trigger a full re-render. |
| Checkbox or radio group | Read current state; change only if needed | A click can reverse an already-correct choice. |
| Date/time picker | Set the value and verify the rendered summary | Popovers can clear related values or reinterpret typing. |
| File upload | Confirm file, destination, recipient, and privacy impact first | Uploading may start immediately and be hard to reverse. |

For framework-driven rich-text editors, avoid low-level property assignment. A robust general sequence is: focus the actual editable element, select existing text, delete it, enter replacement text through keyboard-style input, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible editor with a hidden input. Editing the hidden input may look correct in a DOM inspection while server validation still treats the field as empty. Target the control the user interacts with and the application actually reads. If an accessibility locator resolves to an empty wrapper, inspect the underlying editable element and its label relationship.

Dropdowns, checkboxes, tabs, and date controls can refresh the form. Perform and verify those state-changing selections before entering long text. Re-inspect afterward and confirm earlier entries remain present.

## 6. Verify each meaningful edit

After filling a field or changing a setting, read it back from the page. Compare the actual visible or accessible state with the intended result. For sensitive text, compare length, required state, or a redacted checksum-like summary rather than exposing the full content unnecessarily.

Check for:

- An automation call reporting success while the field is empty.
- Removed line breaks, repeated spaces, punctuation, or special characters.
- Truncation from a single-line field or character limit.
- Text that displays temporarily but was not retained by the application's internal state.
- A later interaction that erased an earlier value after a re-render.
- Editing a hidden synchronization field rather than the visible control.
- A selection changing dependent dates, recipients, attachments, or validation requirements.

If verification fails, stop progressing toward submission. Diagnose the control type and retry once with a more suitable interaction. If the page still rejects or alters the content, report the limitation and ask how to proceed. Never submit content known to be incorrect or incomplete.

## 7. Run a pre-submit readiness gate

Before final submission or a high-impact change, inspect the complete relevant state again. Confirm:

- The correct account, organization, environment, and target are active.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Recipients, options, dates, attachments, permissions, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final control has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially completed form can usually be corrected; an incorrect external action may not be recoverable.

Capture a pre-action record for consequential tasks: a screenshot, concise state summary, or structured field dump. Store and share it only within the appropriate access boundary. Prefer a short summary plus a securely available record over pasting a large table of sensitive values into chat.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Each meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists when the action is consequential.
- [ ] The final action and its impact are understood and authorized.

## 8. Verify completion and handle failure safely

A click is not proof of success. After acting, look for reliable evidence: a confirmation message, reference number, newly created record, persisted setting after a safe reload, sent item, published state, or a changed status.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate messages, requests, payments, or records. If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Do not represent an attempted action as completed.

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank | The application ignored a direct value update | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier entries vanish after a later edit | Re-rendering reset uncommitted state | Commit and verify each field; make re-rendering selections first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline/editor control or use an approved simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the labeled underlying control and target the true editor. |
| Validation says a visible-looking field is empty | A hidden synchronization field was edited | Use the visible interactive control the application reads. |
| Browser automation becomes unstable | The chosen control layer is unsuitable for the page | Restart with a more robust method or supported direct interface. |
| Headless and visible contexts differ | The site varies behavior by browser context | Prefer an approved direct interface; use a verified visible session only for an explicitly authorized task. |
| A popup changes dates or other fields | The widget has stateful clear, close, or parsing behavior | Close through a neutral page action and re-verify all affected values. |
| A visible error may be cosmetic | The action may already have completed | Inspect resulting state before retrying. |
| Account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## 9. Final audit

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful edit was read back and verified.
- [ ] Required fields and validation passed the readiness gate.
- [ ] A pre-action record was captured when appropriate.
- [ ] Required confirmation was obtained before consequential commitment.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed outcomes from uncertainty.
- [ ] No credentials, session data, or unnecessary personal information was exposed.

When a new general failure pattern is discovered, record the symptom, likely cause, and safe fix in the workflow documentation. Consolidate related lessons rather than collecting personal incidents or site-specific workarounds. Keep the method current as browser capabilities and application behavior change.


---
name: create-an-ai-skill
description: Design, test, improve, evaluate, and package reusable AI skills through a practical, user-centered iteration workflow.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, improve an existing one, evaluate whether a skill helps, or optimize when it activates. A skill is a focused set of instructions, with optional scripts, references, templates, and tests, that helps an AI perform a recurring job reliably.

The core loop is:

1. Understand the intended job and its limits.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Review outputs with the user and measure objective requirements where useful.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and generalizes beyond the tests.
7. Optionally improve the description that determines when the skill is used.
8. Package and hand off the completed skill.

Do not assume every project needs the full loop. Some users want a quick collaborative draft; others need a rigorous comparison. Determine where the user is and help them take the next useful step.

## Communication principles

Match the user’s technical knowledge and vocabulary. Use plain language by default. Words such as *evaluation* and *benchmark* may be helpful, but briefly define them if needed. Do not use terms such as “JSON,” “assertion,” or “schema” without explanation unless the user clearly understands them.

Explain why important questions matter. For example:

> What should a successful result look like: an answer in chat, a structured report, a file, or an action? This determines how the skill should validate completion.

Keep the user involved at meaningful decision points:

- Confirm the intended job before writing a large instruction set.
- Ask before introducing restrictive scope rules, required tools, approval steps, or irreversible actions.
- Share proposed test cases before treating them as the evaluation set.
- Let human review lead for subjective qualities such as usefulness, tone, visual design, or creative judgment.
- Be flexible if the user explicitly prefers an informal, low-testing collaboration.

When working with private communications, records, or files about people, first confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Omit unrelated personal details, preserve consent and privacy expectations, and keep outputs within the user’s appropriate access boundary.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea such as: “I need a reusable workflow for preparing project updates.” Start with discovery, then produce a draft.

### B. Existing skill

The user already has instructions and wants them edited, simplified, tested, or improved. Read the current instructions before proposing changes. Preserve the established name and identity unless the user asks to rename it.

If the installed or supplied version may be read-only, work from a writable copy. Preserve the original until the user accepts the revision.

### C. Workflow demonstrated in the conversation

The user may say, “Turn what we just did into a skill.” Extract what you can from the conversation before asking questions:

- Inputs and sources used.
- Tools or capabilities used.
- Sequence of decisions and actions.
- Corrections and preferences the user supplied.
- Input and output formats.
- Acceptance criteria.
- Situations that caused the workflow to change direction.

Summarize the inferred workflow and list gaps for confirmation. Do not silently turn a one-time workaround into a universal rule.

### D. Evaluation or optimization request

The user may have a finished-looking skill and want to know whether it actually improves outcomes. Start with test design, evaluation, and evidence-based revision. Do not rewrite merely because a rewrite is possible.

## 2. Capture intent and scope

Before drafting, gather enough information to define a coherent job. Adapt these questions to the context instead of asking them mechanically.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What requests, wording, or contexts should cause the skill to be used?
3. **Inputs:** What information, files, examples, systems, and permissions may it use?
4. **Outputs:** What should it produce, modify, or recommend? Is there a required format?
5. **Success:** How will the user know the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask a question, pause for approval, or decline?
7. **Variations:** What normal variants, difficult cases, or exceptions materially change the work?
8. **Dependencies:** Does it require a particular capability, reference, template, script, or approved data source?
9. **Testing:** Should realistic test requests be used to verify the skill?

Suggest testing by default when the result is objectively checkable, used repeatedly, consequential, or dependent on a fixed procedure. Subjective work may benefit more from representative examples and human review than numerical scoring.

Offer choices when they reduce ambiguity:

- “Should the AI make a best effort with missing information, or stop and ask?”
- “Should the default output be concise, detailed, or selected by the user?”
- “May it use any available source, or only sources the user explicitly approves?”
- “Should it prepare a draft only, or take an external action after approval?”

### Research before drafting

If approved documentation, comparable skills, domain standards, or relevant references are available, examine them before drafting. Research should reduce user effort, not override the user’s authority over requirements.

Use research to identify:

- Existing conventions and required output standards.
- Constraints of an available system, file type, or interface.
- Reusable patterns for similar work.
- Safety, privacy, compliance, and approval requirements.

If information conflicts or remains uncertain, surface the uncertainty. Do not fill a consequential gap with an unmarked assumption.

## 3. Choose the skill structure

Keep a skill focused enough that users and the AI can predict what it does. A skill can support variants of one job, but separate unrelated jobs when they have different audiences, permissions, sources of truth, or completion criteria.

A typical package may contain:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed documentation
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata:** A short name and description that help route the request.
2. **Core instructions:** The normal workflow used whenever the skill applies.
3. **Supporting resources:** References, templates, or scripts loaded only when relevant.

Keep the core instructions readable. If they become too long, move specialized details into clearly named references and state exactly when each should be consulted. Give large reference files a navigation section or table of contents.

For a skill with domain variants, keep a common selection workflow in the core file and place variant-specific guidance in separate references. The AI should load the relevant variant, rather than treating every variant as required context.

### Use scripts only for repeatable work

Bundle a helper script when test runs show the AI repeatedly reconstructing the same deterministic procedure, such as validating files, converting formats, generating a standard report, or checking calculations.

A script is worth bundling when it is:

- Deterministic or easier to validate than a natural-language process.
- Reused across multiple requests.
- Safer or less error-prone than repeated manual reconstruction.
- Clearly within the user’s approved authority and technical environment.

Document what the script does, its inputs and outputs, failure behavior, and when not to use it. Do not add automation simply because it is possible.

## 4. Write the skill

Use clear, imperative language. Explain the reason behind important instructions, especially where a rule prevents a predictable failure. AI systems generally perform better when they understand the goal and tradeoff than when given an unexplained list of rigid prohibitions.

A useful skill commonly includes the following sections.

### Purpose and scope

State the job, intended use, and boundaries. Make clear whether the skill creates an answer, produces a file, changes data, takes an external action, or guides the user through a process.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State what to do when something required is missing.

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If an approved source is unavailable, ask for an export or produce a draft clearly marked as incomplete.
```

### Workflow

Describe the normal sequence of actions and meaningful decision points:

1. Inspect the request and available inputs.
2. Clarify only information that would materially change the result.
3. Gather evidence from approved sources.
4. Perform the task with an appropriate method.
5. Check the result against requested format and success criteria.
6. Present the result, assumptions, and unresolved limitations.

Use conditional rules rather than trying to list every possible edge case:

```markdown
If the user supplies a required template, follow it.
If no template is supplied, use the default structure below.
If a requested action could overwrite, publish, or materially change important work, explain the impact and request approval before proceeding.
```

### Output format

Define an exact template when consistency matters.

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

Do not impose a rigid shell when the task depends on contextual adaptation. In that case, state goals, quality criteria, and short examples instead.

### Quality, safety, and privacy checks

Specify checks needed before completion. These might include validating required fields, verifying calculations, identifying the source for important claims, preserving original data, or clearly flagging uncertainty.

The skill must behave in a way users would reasonably expect from its description. Do not create instructions that conceal actions, bypass authorization, extract confidential information, damage systems, or facilitate unauthorized access.

For person-related material, use only information relevant to the legitimate task. Avoid unsupported personal inferences and sensitive details. In hiring or assessment work, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance.

### Failure behavior

Describe general recovery rules:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or reference:** Explain what could not be checked and offer an alternate method.
- **Ambiguous request:** Make a low-risk assumption only if it will not materially affect the outcome; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, report the issue, or request guidance.
- **Permission-sensitive action:** Pause for approval before an irreversible, external, or high-impact step.

### Examples

Include a small number of generalized examples only when they teach a distinct pattern. Examples should demonstrate reasoning and output shape, not replace adaptable instructions with narrow test-specific rules.

## 5. Write a strong description

The description is a routing instruction: it helps the AI decide whether the skill applies. It should state both what the skill does and when it should be used.

Cover realistic user wording, including requests that imply the job without naming it directly. A useful description often includes:

- The task or outcome.
- Common contexts or phrases that indicate it applies.
- Important scope limits that prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use when a user asks for a status update, leadership summary, progress report, milestone review, or a concise account of risks and next steps, even when they do not say “status report.”
```

Do not put the full procedure in the description. Do not use vague labels such as “help with documents.” Do not make the description so broad that it captures nearby work better handled by another workflow.

## 6. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description explain when to activate it?
- Are required inputs, permissions, and outputs clear?
- Does the workflow explain why important checks matter?
- Does it state what to do when information is missing?
- Are any rules redundant, brittle, or unlikely to affect outcomes?
- Does it depend on undeclared tools, personal conventions, or private access?
- Does it preserve enough judgment for normal variation?

Prefer a lean, understandable prompt over a long prompt full of rules that do not affect behavior. Repeated absolute language is a warning sign unless it protects a genuine safety, authorization, or correctness boundary.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic initial test prompts. Share them with the user and invite corrections or additions before treating them as the test set.

For each test case, record:

- A descriptive identifier.
- The user prompt.
- Supplied files or context.
- Expected outcome in plain language.
- Objective checks, if appropriate.

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

Cover meaningful situations, such as:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or policy-sensitive request.
- A realistic edge case that changes the workflow.
- An approval, privacy, or safety boundary where relevant.

Vary phrasing, detail level, and user sophistication. Do not make tests merely repeat the skill’s wording. Avoid retaining personal scenarios or sensitive content when generalized cases teach the same lesson.

## 8. Run comparisons and preserve evidence

When independent runs are possible, compare the skill with a meaningful baseline.

- **New skill:** Run each test with the skill and without a specialized skill.
- **Existing skill:** Save an unchanged snapshot before editing, then compare the revised version with the original or another user-approved baseline.

Start skill and baseline runs under comparable conditions. If the environment supports parallel runs, launch both configurations for all test cases at the same time. This reduces avoidable timing differences.

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

For each test, preserve the prompt, inputs, outputs, and available run metadata. Record elapsed time and resource-use information immediately when the environment reports it, because some systems do not retain those notifications.

If independent or parallel agents are unavailable, do a transparent sanity check: follow the skill for each test request, save outputs, and ask the user to review them. Do not claim this is a rigorous baseline comparison. In constrained environments, prioritize qualitative review over artificial metrics.

## 9. Define and grade objective checks

While test runs are underway, draft objective checks where they genuinely help. Explain them to the user before treating them as success criteria.

Good checks are observable, meaningful, and specific:

- Required sections are present.
- A produced file opens and contains required fields.
- Calculations match an approved source within an agreed tolerance.
- The output identifies missing mandatory inputs.
- Important claims include required sources or citations.

Record each result with clear text, a pass/fail outcome, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when source information is missing.",
      "passed": true,
      "evidence": "The final section lists unavailable data points and requests them."
    }
  ]
}
```

Use programmatic checks when practical. They are more repeatable than visual inspection and can be reused in later iterations. Do not force quantitative checks onto subjective work such as writing quality, aesthetics, strategic judgment, or tone; these need human evaluation.

## 10. Review results with a human

Before making major revisions based solely on internal analysis, give the user an accessible way to inspect representative outputs. Use an available review interface when one exists; otherwise present outputs in the conversation or as files the user can access.

For each test case, show:

- The prompt and relevant input context.
- The skill output and comparison output, if available.
- Objective grades and evidence.
- Timing or resource data, if available.
- A place for feedback.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, or hard to use?
- Did the skill add work or detail that was not valuable?
- Would this work for similar requests with different wording or data?

Empty feedback often means a case was acceptable, but it is not proof that the skill is solved. Consider the outputs, grades, and resource tradeoffs as well.

## 11. Analyze results beyond pass rates

Aggregate results where possible: pass rates, average time, average resource use, and variation. Present the revised skill before its comparison condition so the report is easy to scan.

Then examine patterns that summaries can hide:

- **Non-discriminating checks:** Both configurations pass, so the check does not reveal the skill’s value.
- **High variation:** Similar runs differ substantially, suggesting ambiguity, instability, or unreliable instructions.
- **Tradeoffs:** Quality improves, but time or resource use rises beyond the value gained.
- **Failure concentration:** Multiple failures share a root cause, such as unclear source selection or missing output guidance.
- **Unproductive work:** Execution traces reveal repeated planning, unnecessary research, or redundant formatting.
- **Repeated reconstruction:** Several runs independently build similar helpers, suggesting a reusable script or template would help.

Use small benchmarks as evidence for a next revision, not as proof of universal performance.

## 12. Improve without overfitting

Base revisions on feedback, outputs, and analysis. Change the smallest part of the skill likely to address the underlying cause.

Generalize from complaints. If one output fails to distinguish verified facts from assumptions, do not add a rule mentioning only that one test. Explain the broader condition: when sources are incomplete or mixed, separate confirmed information from assumptions and missing evidence.

Use these principles:

1. **Fix causes, not examples.** Design for future requests, not only the current tests.
2. **Keep instructions lean.** Remove guidance that does not change behavior or causes wasted effort.
3. **Explain intent.** State how a step protects accuracy, usability, privacy, or safety.
4. **Add reusable assets only when justified.** Bundle scripts, templates, and references when repeated work demonstrates their value.
5. **Preserve useful behavior.** Do not erase features the user already values.
6. **Expand coverage gradually.** Add tests for real classes of failure, not every isolated incident.

After revision, rerun the test set in a new iteration. Keep baseline policy consistent unless the user agrees that another comparison is more useful. Where possible, show prior outputs alongside new outputs to make changes visible.

Stop when one or more conditions apply:

- The user says the skill is ready.
- Meaningful test cases receive consistently positive or empty feedback.
- Objective requirements are reliably met.
- Further revisions no longer produce meaningful gains.
- Remaining gaps require unavailable information, a missing capability, or a product decision rather than better instructions.

## 13. Optional blind comparison

When two versions appear close and the decision matters, use blind comparison. Give an independent evaluator two outputs without identifying which version produced which output. Ask it to judge against a shared rubric, then reveal the mapping after the evaluation is recorded.

Blind comparison is helpful when:

- Versions have similar objective scores but visibly different quality.
- Reviewers may favor a newer version by default.
- The decision has material cost or impact.

Use a user-centered rubric: correctness, completeness, clarity, constraint adherence, safety, and practical usability. Analyze why one output was preferred before changing the skill again.

## 14. Optimize activation behavior

Optimize the description only after the workflow itself is useful. Create a realistic query set with both cases that should activate the skill and nearby cases that should not.

Use a roughly balanced set of substantive requests. Simple one-step requests are poor activation tests because an AI may handle them directly without consulting a specialized skill, even if the description is relevant.

Positive cases should vary:

- Formal and casual language.
- Direct names for the task and indirect descriptions of the need.
- Common and less common valid use cases.
- Cases where related skills might compete but this one should be selected.

Negative cases should be difficult near-misses, not obviously irrelevant requests. They should share concepts or keywords but belong to another job, need a different capability, or lack the conditions that make this skill useful.

```json
[
  {
    "query": "I need a concise leadership update from these team notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain what project status reports are used for?",
    "should_trigger": false
  }
]
```

Review the activation set with the user before relying on it. If the environment supports repeated activation testing, separate queries used to improve the description from held-out queries used to choose the final wording. Select the description by held-out performance to reduce overfitting.

Show the user the before-and-after description and report the results. Keep the final description honest about the skill’s scope.

## 15. Package and hand off

When the skill is ready, package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states when the skill applies.
- Instructions do not depend on private conventions, personal access, undeclared tools, or hidden assumptions.
- References and scripts are present, clearly named, and documented.
- No credentials, personal data, private identifiers, confidential files, or sensitive examples are included.
- Required capabilities and known limitations are clear.
- Test materials are included only when safe and useful to retain.
- The user can install, access, or adapt the package in their chosen environment.

Provide a short handoff note that explains what the skill does, what it needs, how to test it after installation, and any important limitations.

## Final readiness gate

A skill is ready when it has:

- A clear, bounded job.
- A description that routes appropriate requests.
- Instructions that handle normal variation and important failure modes.
- Explicit boundaries for authorization, privacy, uncertainty, and high-impact actions.
- Evidence from realistic use that it improves outcomes or provides dependable value.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for the user’s recurring work.


---
name: test-every-screen-size
description: Verify UI and CSS changes across representative widths, heights, content states, and target devices using screenshots plus programmatic layout checks before release.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, color, or background edits: a local rule can change wrapping, height, overflow, alignment, or backgrounds elsewhere.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Use real screenshots and numerical checks together.

## 1. Define the test scope

Choose viewports based on the product’s supported devices, analytics, design requirements, and the changed layout behavior. If no project-specific viewport matrix exists, use this broadly useful baseline:

- narrow: 320 px and 480 px;
- intermediate: 600 px and 720 px;
- desktop: 1024 px and 1440 px;
- large desktop: 1920 px when large displays are a supported or likely use case.

When vertical layout matters, test both a short viewport (about 700 px tall) and a tall viewport (about 1400 px or taller) at each relevant width. Include an especially tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Also test any explicitly supported device size or viewport named in the task. Treat the baseline as a default starting point, not a substitute for product requirements.

## 2. Prepare realistic page states

Run the real interface in an appropriate test environment. Populate the changed surface with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative lists, cards, rows, and validation messages;
- realistic item counts and content near expected limits;
- loading, empty, and error states when the change affects them.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping, and unintended blank space.

## 3. Capture and inspect screenshots

Use a repeatable browser-testing system, preferably headless automation, to capture screenshots at every relevant viewport and state. Use full-page screenshots when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect each changed component on all four sides:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design now that the component’s role or size has changed. Pay particular attention to edge-to-edge or full-bleed changes: removing containment can expose leftover wrapper margin or padding as visible background strips on an untouched edge.

Reread the requested outcome after the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks

Run numerical checks alongside screenshots at each relevant viewport. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow where the screen is intended to fit the viewport;
- no changed element overlaps neighboring content or its intended container;
- buttons, links, and fields remain visible and operable;
- fixed or sticky UI does not hide essential content;
- cards, lists, and controls remain within intended bounds;
- prose retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant bounding rectangles with adjacent elements and container boundaries rather than assuming every stacked element should never intersect.

For prose-heavy pages, flag overly wide text measures. About 80 characters per line is a useful warning threshold; reading-focused layouts commonly target roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visible defects such as exposed background strips, poor visual balance, and unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and the relevant programmatic checks pass.

## 6. Fix failures and rerun

If any viewport or realistic state fails:

1. stop the completion or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior instead of adding a viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the failing size.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model or component constraints are likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Record the tested widths, relevant heights and states, and checks performed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any required viewport or state remains unverified, say so clearly and do not represent the UI change as complete.


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

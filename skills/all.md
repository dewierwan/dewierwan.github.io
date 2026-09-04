# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate distinct options for a decision or problem, assess their tradeoffs honestly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long idea list: surface genuinely different paths, state their tradeoffs plainly, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they refer to documents, discussion threads, prior decisions, research, or other records available in the current environment, review only the sources needed to understand the decision.

When accessing non-public communications or records, do so only for a legitimate purpose with clear authorization. Use the minimum relevant information, omit unrelated personal or sensitive details, and keep the response within the appropriate access boundary.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Constraints, commitments, deadlines, or available resources
- Relevant stakeholder concerns and decision ownership
- Evidence about prior attempts, results, or risks

Do not search broadly by default. If a material fact is unavailable, state the assumption or ask a focused question instead of inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- What the user is actually deciding
- Important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging it

The stated request may describe a symptom or preferred solution rather than the underlying decision. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Options must be fundamentally different approaches, not different intensity levels of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes process, incentives, scope, timing, or problem framing
- At least one surprising but plausible path, such as delaying, partnering, reducing scope, or doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, or avoided distraction has real value.

Give each option a short, memorable label that communicates its core approach. Use this format:

| Option | What | Strengths | Weaknesses | Effort |
|---|---|---|---|---|
| [Short label] | [One or two sentences describing the approach.] | [One or two concrete advantages.] | [One or two concrete disadvantages or failure risks.] | [Low / Medium / High] |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, evidence strength, and stakeholder burden. Add domain-specific criteria where needed.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are instructive, but clearly state why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not merely why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may:

- Pick an option
- Ask for more detail on a specific option
- Correct the framing or challenge the options
- Request additional alternatives
- Combine options into a hybrid

If the user proposes a hybrid, check whether its components are compatible and whether the combination resolves a real tradeoff rather than merely adding complexity. Do not start implementation simply because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that captures the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move to planning and execution: requirements, milestones, tasks, ownership, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before responding, verify that:

- The framing reflects the actual decision rather than only the requested solution.
- The options are truly distinct and not variations in degree.
- The set includes the conventional path and a meaningfully different alternative where appropriate.
- Strengths and weaknesses are concrete, balanced, and candid.
- Effort labels are plausible for the user’s context.
- Recommendations follow the stated criteria and constraints rather than default assistant preferences.
- The response does not expose unnecessary private, sensitive, or unrelated information.


---
name: pressure-test
description: Find the weak points in a leading strategic idea before committing. Steelman the case, test its load-bearing assumptions through sequential challenge, and finish with a clear verdict, handoff, and concrete next action.
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

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the prior findings to make the decision.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for the answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Use available evidence, such as research, metrics, prior experiments, customer feedback, documented decisions, or stakeholder input. Distinguish facts, inferences, and forecasts.
- If reviewing internal communications, records, or feedback about people, do so only for a legitimate decision purpose and with clear authorization. Use the minimum relevant material, omit unrelated sensitive details, and keep findings within the appropriate access boundary.
- Refer to possible dissenters by relevant role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold. Rank them by damage if wrong, with the most decision-changing assumption first. Make assumptions observable where possible. Replace “people will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [How to test or disprove it] |

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions and adapt later questions to the answers received. Do not present the full list as a questionnaire, because that enables selective answering.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed? Why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence. Ask what observed behavior, data, comparison, or commitment supports the claim.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution problems, external conditions, and a wrong underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable signal] | [Name the check or accountable role] |

The warning sign must appear early enough to permit a course correction.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap; do not treat silence as agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data collection period. Next: run that test, then make the decision with the result recorded.
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

Use this workflow to make decisions with the right amount of rigor. The aim is a clear, timely call, not maximum analysis. Record meaningful decisions only with permission, preserve the decision-maker’s actual reasoning, and learn from results.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices deserve minutes, not days.
2. **The decision-maker owns their position.** Never state, record, or imply that they favor, believe, or chose something they have not actually said.
3. **Separate advice from attribution.** Assistant recommendations belong in the conversation and must be labeled as assistant analysis. Add them to a record only if the user requests that.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution. Plan or do the task instead.
5. **Record only with explicit permission.** “Should we do X?” asks for analysis, not for a permanent record. Create or update a record only when the user asks to log, track, open, update, or commit the decision, or clearly agrees to doing so.
6. **Respect privacy and access boundaries.** Before searching a decision register, shared communications, personnel material, or other records about people, establish a legitimate purpose and clear authorization. Use the minimum relevant sources and details. Exclude unrelated personal, confidential, or sensitive information.

If a record will be visible to others, confirm that the audience is appropriate. For sensitive subjects, such as health, relationships, compensation, or confidential people matters, offer a private record in the user’s chosen private workspace or keep the discussion in chat.

## 1. Select the mode

If the user explicitly says to start, resume, commit, or review a decision, follow that instruction. Otherwise, if authorized, search the available decision register for an overlapping record before creating a duplicate.

| Mode | When to use it | Action |
|---|---|---|
| New | No matching decision exists | Frame and classify the decision |
| Resume | A matching record is still open | Append new inputs and continue analysis |
| Commit | An open decision exists and the user is ready to decide | Complete readiness checks and record the commitment |
| Review | A resolved decision has reached its review date | Compare actual outcomes with the original prediction |

For a resume, append information rather than rewriting the history. For a review, use the original prediction and reasoning as the baseline instead of reconstructing them from memory.

## 2. Frame the question

Write the decision as a concrete, decidable question. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing where relevant?
- What deadline, event, or trigger requires a decision?
- What result is desired?
- What happens if no action is taken?

If the issue is broad and credible options do not yet exist, generate options first. Do not pressure-test a vague problem statement. If there is only one viable path, say: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time when classification is unclear. Use the cost of reversal as the primary test: consider money, time, trust, operational disruption, opportunity cost, and reputational effects. If the unwind cost cannot be named quickly, the choice is likely larger than it first appears.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not record by default |
| Reversible | Moderate stakes and reversible in days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, and consult relevant people |
| Direction-setting | Shapes strategy, operating model, culture, or finances for a long period | Full analysis, explicit dissent, and named prerequisite conversations |

## 4. Apply the appropriate rigor

### Trivial

Choose a reasonable default, state a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: attention spent debating may exceed the cost of an imperfect choice.

### Reversible

Use a short working session:

1. List two or three realistic options.
2. For each, state one major strength, one major weakness, and a rough effort, cost, or time estimate.
3. Recommend an option and identify the decisive reason.
4. If uncertainty matters, choose the smallest reversible test likely to change the call.

### Hard to reverse: challenge gate

Before committing, pressure-test the leading option. A valid challenge examines core assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and important stakeholder objections.

If no relevant pressure test has occurred in the current decision context, stop and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not bypass this gate merely because the user is in a hurry. Proceed only after the pressure test is complete or the user explicitly overrides it with a reason. If it exposes a serious unresolved problem, return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

After the gate is met:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check relevant stakeholders: who has expertise, bears consequences, or may reveal a constraint?
4. Give a recommendation, clearly labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has happened, unless the user explicitly accepts and records a reason for proceeding without it. If the decision is being rushed, state what consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest supporting evidence.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scores only when they clarify tradeoffs rather than hiding judgment.

Keep these categories distinct:

- **Decision-maker’s stated view:** Positions they actually expressed.
- **Assistant analysis:** The assistant’s recommendation and reasoning.
- **Open question:** Important uncertainty not yet resolved.

If the decision-maker has not expressed a view, write “No position stated yet” or leave their position blank. Never invent their lean, confidence, rationale, response to dissent, or final choice.

## 6. Commit and record

Before finalizing, confirm:

- What is the decision?
- Which option was chosen?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable result is predicted?
- What is the decision-maker’s confidence in that prediction?

For meaningful decisions, make the prediction testable:

> By [date or trigger], [observable outcome] will happen or will not happen.  
> Confidence: [percentage].

Use the user’s chosen document system, register, or private file. A useful decision record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar, task system, or equivalent reminder for high-stakes reviews.

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until a choice is made. When resuming, append a dated thinking entry rather than replacing earlier reasoning.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** [Optional additional option.]

## Thinking log
### [Date]
- New inputs, conversations, data, or events
- How the thinking changed
- Decision-maker’s stated position today: open / leaning / decided

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
The decision-maker’s own reasoning, only when they have stated it.

## What would change my mind
Assumptions or evidence that would justify reversing the choice.

## Prediction
By [date], [observable outcome] will happen or will not happen.
Confidence: [X%]

## Worries
The most credible downside or failure mode.

## Retrospective
To be completed at review.
```

## 7. Review the outcome

At the review point, assess four separate questions:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat a bad outcome as proof of a bad decision process, or a good outcome as proof of sound reasoning.

## Completion message

When a decision is made, summarize it clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [DD MMM]
Review: [DD MMM or trigger]
Record: [location, if one exists]
```

Use direct language and challenge weak reasoning with evidence. Do not let rigor become endless deliberation: once the appropriate readiness gates are met, name the decision and move forward.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, recommendation, implementation, verification, and handoff. Supports analysis-only work when the user asks not to implement yet.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the solution is not already clear. Do not use it for a small fix or routine task with a known implementation.

By default, proceed from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the underlying problem

Start with the problem, not the requested solution. If the request is “build X,” work backward:

- Who is affected, and what are they trying to accomplish?
- What happens now, including workarounds?
- How often does it occur, and how severe, costly, urgent, or blocking is it?
- What outcome would materially improve the situation?
- What constraints are already known: time, security, compatibility, budget, ownership, or access?

Write a concise problem statement and descriptive requirements. State outcomes and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so clearly.

### Rules for people-related information

If understanding the problem requires reviewing communications, records, analytics, or other information about people:

1. Establish and state the legitimate purpose before accessing or analyzing the information.
2. Confirm clear authorization for the specific sources, people, and use. Do not infer authorization from general system access.
3. Use only the minimum relevant sources, date range, fields, and excerpts needed to answer the problem.
4. Do not collect, repeat, or expose unrelated personal information or sensitive information, such as health, financial, identity, family, private communications, or protected characteristics, unless it is necessary, authorized, and lawful to use.
5. Respect applicable consent, notice, retention, confidentiality, and privacy expectations. If consent or expected use is unclear, pause and seek clarification.
6. Keep notes, proposals, and outputs within the authorized audience and access boundary. Prefer aggregated, de-identified, or role-level findings when they answer the question.

Do not use people-related information for a purpose beyond the stated problem, and do not make claims about an individual that are unsupported by relevant evidence.

## 2. Check priority and decision readiness

Assess whether this is worth solving now. Consider severity, frequency, people affected, available workarounds, opportunity cost, and the cost of delay. “Do nothing,” “defer,” or “improve the workaround” must remain real options.

Classify decisions:

- **Reversible:** Small choices that can be changed cheaply. Use reasonable judgment and proceed.
- **Hard to reverse:** Public interfaces, persistent data changes, migrations, long-lived settings, security boundaries, vendor commitments, or external contracts. Pause for an explicit decision before implementation.

If direction, ownership, priority, or authority is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design work. Record rationale for consequential decisions when useful.

**Readiness gate:** Do not design a committed solution until the problem, priority, decision owner, authority to proceed, and any required data-access authorization are sufficiently clear.

## 3. Research current context

Inspect relevant project guidance, architecture notes, repository documentation, existing code, tests, operational procedures, service documentation, and prior attempts. Look for established patterns and reusable components before creating new ones.

Identify compatibility requirements, deployment practices, security expectations, supported environments, data flows, ownership boundaries, observability, and rollback limits. Use existing conventions unless there is a strong, documented reason not to.

When research involves people-related data, record the authorized purpose, sources used, and access limits. Avoid copying raw records into broadly shared documents. Redact or omit personal and sensitive details unless their inclusion is necessary and authorized for the intended audience.

## 4. Define evaluation criteria

Define explicit criteria before selecting an approach.

| Criterion | Example threshold or question |
|---|---|
| Correctness | Does it preserve required behavior and data integrity? |
| Safety and privacy | Does it maintain authorization, consent expectations, confidentiality, and minimum-necessary data use? |
| Effort | Is it feasible within available delivery and maintenance capacity? |
| Reversibility | Can it be removed or rolled back safely? |
| Verification | Can success and failure behavior be tested clearly? |

Add problem-specific criteria such as latency, accessibility, reliability, cost, or operational burden. These criteria prevent the first plausible idea from winning by accident.

## 5. Generate varied approaches

Generate genuinely different options, not minor variations. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution: instructions, training, process changes, templates, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For ambiguous or high-impact work, produce a wider candidate set before narrowing. Describe each viable option briefly: what it is, what it solves, main costs, risks, data implications, and irreversible commitments.

### Technical design rules

- Prefer one understandable code path over runtime-specific special cases.
- Validate strictly and fail visibly for invalid states; do not silently turn programming errors into plausible results.
- Prefer established conventions over new abstractions, and abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer bounded changes that can be removed cleanly.
- Use proven technology and existing infrastructure unless a new choice has a clear advantage.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Avoid quick fixes outside the appropriate design boundary.

## 6. Evaluate and recommend

Compare options against the criteria. Provide a short proposal with:

- Problem statement and current-state evidence.
- Evaluation criteria.
- Viable options and key tradeoffs.
- One clear recommendation and why it is preferred.
- Risks, irreversible effects, assumptions, data-handling implications, and open decisions.

Store durable proposals in the user’s chosen shared documentation system when review or collaboration is needed; otherwise use the current workspace. Apply access controls appropriate to the proposal’s contents. Do not place personal or sensitive source material in a document shared beyond the authorized audience. Use a clear date-prefixed title, such as `04 Sep 2026: Solve — topic`.

**Analysis-only gate:** If implementation was not requested, stop here. Do not make changes merely because a recommendation exists.

## 7. Plan, implement, and verify

For larger work, create a reviewable implementation plan covering scope, ordered steps, affected components, data migration and rollback, tests, deployment, monitoring, and follow-up ownership. Obtain required approval before crossing hard-to-reverse boundaries.

Implement using project conventions. Run relevant tests, static checks, and focused manual verification. Test normal behavior, important failure behavior, compatibility, authorization boundaries, and rollback or recovery where applicable.

If the solution processes information about people, verify that it enforces the approved purpose, least-privilege access, minimum necessary collection and retention, sensitive-data protections, consent or notice requirements where applicable, and output access controls. Test that unauthorized users cannot retrieve records, inferences, or exports.

Audit before declaring completion:

- Does the result meet each evaluation criterion?
- Were authorized sources and the minimum necessary information used?
- Were personal or sensitive details omitted, protected, or restricted to the authorized audience?
- Were tests actually run, and what did they show?
- Are migrations, releases, or external changes reversible or explicitly accepted?
- Are known limitations and unverified assumptions recorded?

Do not claim success based solely on completed code. Commit, publish, or deploy only under the user’s repository and release practices.

## 8. Hand off

Report the user outcome, what changed, verification performed and results, known limitations, deferred work, rollout or monitoring needs, and any required user action. Include links or references to the proposal, plan, and change record when applicable.

Share the handoff only with people authorized to receive it. Use concise, audience-appropriate detail; provide de-identified summaries where possible and avoid including raw personal records, sensitive details, credentials, or unnecessary internal implementation data.

Common failure modes are implementing the initial request without diagnosing the need, treating an irreversible commitment as routine, selecting the first plausible option without criteria, adding permanent configuration for a temporary case, hiding defects through broad error handling, using people-related data without a clear purpose or authorization, collecting more personal data than needed, exposing sensitive details to an overly broad audience, and reporting completion without evidence of verification.


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
description: Learn a paper, article, post, or topic through a short Socratic dialogue built around retrieval, explanation, challenge, and application rather than passive summary.
---

# Learn with a tutor

Help a learner understand, retain, and use a provided paper, article, post, lesson, or topic through a rigorous conversation. Prioritize active recall and reasoning over explanation. The learner should do most of the intellectual work; the tutor guides, diagnoses, and adjusts the challenge.

## Purpose and boundaries

Use this workflow when the learner wants to understand an idea, prepare for a discussion or assessment, evaluate an argument, or apply a concept in practice.

If the material includes private communications, personal records, or sensitive information, use it only for a legitimate learning purpose and with clear authorization. Refer only to the minimum relevant content, avoid exposing unrelated personal details, and keep the discussion within the learner's authorized access boundary.

## Learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to recall and reconstruct ideas in their own words.
- **Ask for mechanisms.** Move beyond conclusions: ask why, how, under what conditions, and with what evidence an idea works.
- **Make the learner generate connections.** Ask for their own examples, analogies, predictions, objections, and uses before offering examples yourself.
- **Use productive difficulty.** Challenge the learner enough to require thought, but not so much that they cannot make a meaningful attempt.
- **Practice transfer.** Move from the original material to unfamiliar cases, related concepts, and real decisions.
- **Surface gaps through questions.** When an answer is incomplete or inconsistent, ask questions that help the learner notice the gap. Explain directly only after they have had a fair chance to reason it through.

## Readiness check

Before teaching, establish:

1. **Material:** What paper, article, passage, or topic is being discussed?
2. **Starting point:** What does the learner already know, believe, or suspect?
3. **Goal:** What should they be able to explain, evaluate, or do afterward?
4. **Scope:** Which two or three ideas are most important, difficult, or useful?

If the learner has not read the material, do not begin with a full explanation. Ask for an initial prediction or working model, direct them to inspect a relevant section, then resume with retrieval questions.

## Conversation workflow

### 1. Activate prior knowledge

Start with one or two open questions:

- “What do you already think is true about this topic, and why?”
- “What experience or related idea does this bring to mind?”
- “What are you hoping to be able to explain or do by the end?”

Use the answer to identify useful background knowledge, possible misconceptions, and an appropriate level of challenge.

### 2. Elicit the central claim from memory

Ask the learner to explain the main argument, finding, or idea without quoting the source.

- “In your own words, what is the main claim?”
- “What problem is this idea trying to solve?”
- “Why should someone believe this claim?”
- “If you had 30 seconds to explain it to a thoughtful friend, what would you say?”

Do not accept a repeated sentence from the material as evidence of understanding. Ask for a paraphrase, causal story, example, or implication.

### 3. Explore a small number of core ideas

Do not cover every detail. Select two or three ideas that are central, consequential, confusing, or likely to be misunderstood. For each, use this cycle:

1. Ask the learner to reconstruct the idea.
2. Probe assumptions, evidence, reasoning, and mechanism.
3. Ask for a self-generated example, comparison, or application.
4. Test it with an objection, boundary case, or alternative explanation.
5. Adjust the next question to the learner's actual answer.

Keep turns short. Usually ask one or two questions at a time.

## Question toolkit

Choose prompts that require explanation rather than recognition:

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What is the mechanism here, step by step?”
- “What evidence would distinguish this explanation from another one?”
- “Can you construct a concrete example from a familiar setting?”
- “Where might this fail, or where would it not apply?”
- “What is the strongest objection to this argument?”
- “How does this connect to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one assumption changed?”

Avoid simple yes-or-no questions unless they are immediately followed by a request for reasoning.

## Responding to learner answers

Be warm, direct, and specific. Avoid generic praise. If an answer is strong, identify what makes it strong—such as naming an assumption, distinguishing correlation from causation, explaining a mechanism, or providing a relevant counterexample—then raise the challenge.

When an answer is inaccurate or incomplete:

1. Do not immediately provide the correction.
2. Ask one focused question that reveals the tension or missing distinction.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, give a concise explanation or hint.
5. Ask them to restate the idea in their own words or apply it to a new case.

If the learner says, “I don’t know,” invite a low-stakes attempt: “Take a guess based on what you do know. What seems most plausible, and why?” Give more support only after an attempt or when the task clearly requires missing foundational knowledge.

## Calibration rules

Increase difficulty when the learner is answering comfortably:

- ask for a counterexample;
- compare the idea with a related framework;
- change one assumption and ask for a prediction;
- request an application in a new domain; or
- ask them to defend the claim against a strong objection.

Reduce difficulty when the learner is lost:

- narrow the question to one claim or assumption;
- use a simpler case;
- offer two competing explanations and ask them to defend one;
- provide a partial hint; or
- briefly clarify essential vocabulary, then return to retrieval.

Ask the learner to define jargon before defining it for them whenever possible. Match their energy: go deeper when they are engaged; consolidate when they are overloaded or fatigued.

## Progress checks and audit

Periodically give a brief, evidence-based update:

- **Demonstrated understanding:** what the learner can accurately explain, reason about, or apply.
- **Remaining uncertainty:** what is still vague, unsupported, inconsistent, or untested.
- **Next best focus:** the single concept, distinction, or practice question most worth revisiting.

Do not claim mastery because the learner recognizes terminology or repeats a conclusion. Strong evidence of learning includes accurate explanation, causal reasoning, handling objections, and transfer to a fresh example.

## Closing gate

Before ending, convert learning into action. Ask:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation, an application to a new case, or a retrieval prompt to answer later. End by naming the next concept or question worth revisiting.

## Common failure modes

- **Passive summary:** Replace it with a request for recall first. Summarize only when explicitly asked, and invite the learner to try before receiving one.
- **Rapid-fire quiz questions:** Build a dialogue from the learner’s answers rather than using a fixed test sequence.
- **Too much breadth:** Focus on a few core ideas deeply rather than skimming the entire source.
- **Premature correction:** Use questions to reveal the problem before explaining it.
- **Empty encouragement:** Give specific feedback tied to reasoning or evidence.
- **Challenge without support:** Preserve productive difficulty, but simplify or hint when the learner lacks the foundation to proceed.
- **No transfer:** Do not end with recall alone; require a decision, prediction, example, or changed belief.


---
name: write-in-my-voice
description: Draft or revise email in the user’s authentic voice while keeping facts, commitments, privacy, and recipient context appropriate. Build a current voice profile from authorized evidence, write the smallest complete message, and audit it for.
---

# Write in my voice

Use this workflow when drafting, replying to, or revising an email on the user’s behalf.

## Goal

Produce a copy-ready email that sounds recognizably like the user rather than a generic assistant. Match their usual warmth, directness, rhythm, formatting, and conventions while adapting appropriately to the recipient, relationship, and stakes.

## 1. Gather authorized voice evidence

Before drafting, read the user’s current style guide in full if one exists. You may also use recent emails the user actually sent, approved templates, and an approved bank of standard facts or links.

Access communications or records only for a legitimate drafting purpose and with clear authorization. Use the minimum relevant examples. Do not expose unrelated correspondence, personal information, confidential details, or internal notes in the output.

Build a practical voice profile from the evidence:

- Typical greeting and sign-off.
- Formality level, warmth, and relationship cues.
- Usual sentence and paragraph length.
- Preferred vocabulary, contractions, directness, and colloquialisms.
- Punctuation, capitalization, and formatting habits.
- Phrases, tones, or punctuation the user avoids.
- How the user requests action, follows up, declines, corrects, apologizes, or expresses uncertainty.
- Approved reusable facts, links, boilerplate, and standard responses.

Recent sent messages and direct user instructions outweigh older examples. If evidence conflicts, ask which preference is current, or follow the most recent consistent pattern.

## 2. Confirm the email brief

Identify the minimum information needed for a safe, useful draft:

1. Who will receive the email, and what is their relationship to the user?
2. What outcome should the message produce?
3. What facts, dates, names, links, attachments, decisions, or commitments must appear?
4. What tone is needed: routine, warm, firm, formal, sensitive, or urgent?
5. Are there deadlines, approval requirements, confidentiality limits, or consequences if the message is misunderstood?

Do not invent availability, decisions, prices, promises, opinions, emotional reactions, or facts. If a missing detail would materially change the message, ask one focused question instead of guessing.

## 3. Adapt the voice to the context

Voice is not a rigid template. Preserve recognizable habits while making the message fit its audience and purpose.

| Situation | Adaptation rule |
|---|---|
| Familiar colleague or ongoing contact | Use the user’s normal concise and familiar pattern. |
| New, external, senior, or formal recipient | Keep the user’s voice, but add sufficient context and use more careful wording. |
| Request or handoff | State the action, responsible person, and timing plainly. |
| Conflict, correction, or rejection | Be direct, factual, and respectful. Avoid defensiveness, excessive praise, and unnecessary apology. |
| Sensitive or confidential matter | Include only necessary details, avoid forwarding private context, and keep the draft within the user’s authorized access boundary. |

Use approved standard wording, factual material, or links when they fit. Do not reuse a template if it would be inaccurate, misleading, or too broad for the situation.

## 4. Draft the smallest complete email

Write only what helps the recipient understand and act. A useful default structure is:

1. Greeting, when consistent with the user’s normal practice.
2. Purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Closing and sign-off, when appropriate.

Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Put requests, deadlines, and decisions where they are easy to find. Use bullets only when they improve clarity for actions, options, or logistics.

Remove:

- Throat-clearing and process narration.
- Generic praise or repeated thanks.
- Filler such as “just wanted to” or “I hope you’re well” unless it is both natural to the user and useful in context.
- Hedging that weakens a clear message.
- Claims about how the draft was created.

## 5. Run a voice, accuracy, and privacy audit

Review the draft line by line before presenting it:

- Would the user plausibly write these exact words?
- Do the greeting, closing, punctuation, and rhythm match the available evidence?
- Is the tone appropriate for the recipient and stakes?
- Did the draft add an unsupported commitment, claim, opinion, or emotion?
- Are names, dates, links, attachments, and references correct?
- Is the requested action and deadline unmistakable?
- Does the email reveal only information needed by this recipient?
- Can any sentence be removed without losing meaning or usefulness?
- Does it avoid language the user has identified as undesirable?

## Readiness gate

Do not present a final draft until these conditions are met:

| Check | Ready when |
|---|---|
| Voice basis | A style guide, relevant sent examples, direct instructions, or a stated default is available. |
| Facts | Material details are supplied, verified, or clearly marked for confirmation. |
| Commitments | The draft does not create obligations the user did not authorize. |
| Recipient fit | Tone and detail level suit the relationship and sensitivity. |
| Privacy | The draft contains no unnecessary personal, confidential, or unrelated information. |

If no voice evidence exists, state the assumption briefly and use a broadly useful default: concise, clear, warm-professional, and direct. Invite the user to provide a few approved examples or preferences for future drafts.

## Output format

Provide the final email as copy-ready text. If clarification is necessary, ask only the specific question needed to draft safely. Do not add commentary after the final copy unless the user asks for alternatives, rationale, or revisions.


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
description: Gather authorized meeting context, clarify the user’s intended outcome, and create a focused preparation record with a practical agenda, decision-relevant questions, and an appropriate follow-up plan.
---

# Prepare for a meeting

Use this workflow when a user asks to prepare for one meeting, a day of meetings, or a recurring relationship. The deliverable is a durable meeting-preparation record in the user’s chosen workspace, not merely a chat summary. It should help the user quickly reload the situation before the meeting and guide the conversation toward the intended outcome.

This workflow is designed for external meetings, partner conversations, customer calls, recruiting discussions, negotiations, advisory conversations, and other consequential small-group meetings. Adapt it for internal meetings when preparation will materially improve the outcome.

## Core principles

- Start with meeting evidence, not assumptions.
- Read the material that the meeting is actually about. Researching attendees is not a substitute for reading a proposal, brief, deck, draft, or plan under discussion.
- Ask targeted questions before committing to a goal or agenda when the user’s priorities, authority, boundaries, or desired level of directness are unclear.
- Use the minimum relevant information. Do not copy sensitive personal, employment, financial, health, legal, or private-communication details into a broadly visible meeting record.
- Keep the agenda realistic for the available time. Put the decision-relevant topic before background updates.
- Separate verified facts, other people’s reported views, and the user’s intended position.
- Make the final record useful in two modes: detailed preparation before the meeting and a short question list during it.

## Authorization and access boundary

Before searching communications, calendars, contact records, transcripts, or internal documents, confirm there is a legitimate purpose and that the user is authorized to access and use those sources for meeting preparation.

Use only sources and details needed for this meeting. Respect confidentiality labels, consent expectations, and workspace permissions. Do not expose unrelated personal details from messages or records. If the final preparation record may be visible to a wider group, omit information that should remain restricted and describe sensitive matters at an appropriate level of abstraction.

For example:

- Write **offer follow-up** rather than including compensation figures.
- Write **a personal constraint may affect timing** rather than copying a private explanation.
- Summarize a confidential internal concern as **internal decision still pending** unless the exact detail is necessary and the record is access-restricted.

If access, intended use, or the appropriate audience is unclear, ask the user before searching or recording information.

## Inputs and scope

Collect or confirm the following:

- Target date or date range.
- Meetings to prepare.
- The user’s timezone.
- Available authorized sources, such as calendar events, email, internal discussions, prior meeting notes, documents, contact records, public web sources, and call transcripts.
- The destination workspace or record system.
- The access level and intended audience of the final record.

A useful default is to prepare external one-to-one and small-group meetings, while skipping obvious focus blocks, meals, personal holds, routine internal status meetings, and out-of-office events. Do not automatically exclude an internal meeting if it involves a decision, negotiation, sensitive alignment issue, or important stakeholder.

## Workflow overview

1. Identify the meetings and extract meeting facts.
2. Gather relevant relationship and topic context.
3. Read the artifact under discussion, if one exists.
4. Identify special meeting types that need a different preparation structure.
5. Share a concise situation brief.
6. Ask targeted questions and wait for answers when clarification is needed.
7. Create the meeting-preparation record.
8. Review privacy, validate the result, and deliver it through the chosen workspace.
9. Arrange a post-call review when appropriate and authorized.

Do these steps in order. Do not jump from background research directly to a generic agenda when the user’s aim is uncertain.

## 1. Identify and read the meeting

Retrieve target events from the user’s authorized calendar or meeting list. For each candidate meeting, extract:

- Title or topic.
- Start and end time, including timezone and duration.
- Attendee names, roles, organizations, and contact details where available.
- Organizer and any relevant relationship to the user.
- Meeting location or joining details.
- Invitation description, attachments, and links.
- Scheduling context, such as an introduction, reschedule explanation, event follow-up, or stated request.
- Whether this appears to be a first meeting, a recurring meeting, or a continuation of an earlier discussion.

Filter out non-meeting blocks unless the user explicitly wants them included. For group meetings, identify the key decision makers, subject-matter contributors, and relationship owners rather than treating every attendee as equally central.

Create an initial fact sheet before interpreting motives. Mark unknowns explicitly.

| Field | What to capture |
|---|---|
| Meeting | [Title or working topic] |
| Timing | [Date, start/end time, timezone, duration] |
| Participants | [Key attendees and roles] |
| Stated purpose | [Invitation language or scheduling trigger] |
| Decision context | [Known decision, request, or unknown] |
| Linked material | [Documents, decks, notes, or none found] |

## 2. Gather relationship and topic context

Research each important external participant and the relevant organization using the least intrusive, highest-signal sources first. Independent research may be done in parallel, but organize the final findings by meeting rather than by source.

### Recommended source order

1. **Direct correspondence:** Review recent messages to or from the attendee. Look for commitments, open questions, introductions, earlier requests, and the immediate trigger for the meeting.
2. **Name and organization mentions:** Search authorized communication and discussion spaces for references to the person or organization, including discussions where they were not a direct participant.
3. **Prior meetings:** Find earlier calendar events, meeting records, notes, and transcripts involving the attendee or topic. For recurring relationships, identify the arc: what has progressed, stalled, changed, or been promised.
4. **Relevant internal records:** Search project notes, decision logs, customer records, or relationship-management records when authorized.
5. **Public sources:** Use public professional profiles, organization websites, publications, interviews, and recent reporting to verify role, background, organization context, and timely developments.

Do not treat a search result as fact without checking its source and recency. Prefer direct records and primary sources over hearsay or stale public profiles.

Synthesize findings into:

- **Who they are:** Current role, relevant experience, and relationship to the topic.
- **Organization context:** What the organization does and why it may matter to the user’s work.
- **Relationship history:** Prior meetings, promises, introductions, decisions, and unresolved threads.
- **Why this meeting is happening now:** The concrete scheduling trigger and likely decision or exchange.
- **Timely context:** Relevant recent news, publication, organizational change, deadline, or event.
- **Key links:** Only links that directly help the user prepare.
- **Unknowns and confidence:** What is uncertain, ambiguous, or based on incomplete evidence.

Avoid creating a biography dump. Every included detail should help the user decide what to ask, say, avoid, or close.

## 3. Read the artifact the meeting is about

If the meeting concerns a proposal, pitch, draft, memorandum, presentation, plan, brief, agreement, or other written artifact, locate and read it before drafting substantive questions or an agenda.

Signals that an artifact exists include:

- The invitation or message asks for feedback on a document, plan, proposal, or deck.
- Someone says they shared a draft or left comments.
- The meeting description includes a file link.
- Notifications or message threads refer to a named document.
- The meeting is framed as discussing a strategy, recommendation, application, or plan that normally exists in writing.

Read the full relevant artifact, including appendices, sections, tabs, and comments where accessible and appropriate. Do not skim a complex document and then ask generic questions such as “Tell me about your plan.”

Extract:

- The artifact’s stated objective.
- Its core claims, assumptions, dependencies, and proposed actions.
- Decisions requested from the user or other participants.
- Ambiguities, trade-offs, risks, and missing evidence.
- The few issues that most need pressure-testing in the meeting.

If context strongly suggests that a document exists but it cannot be found, ask the user for the link or relevant extract before designing a detailed agenda. You may still prepare relationship context and high-level questions, but label the agenda as provisional.

## 4. Detect special meeting types

Before continuing, determine whether the meeting needs a specialized workflow.

### Reference or employment assessment conversations

If the meeting is a reference conversation, work-history assessment, or another discussion intended to inform a hiring decision, use an authorized reference or assessment preparation workflow instead of a generic meeting agenda.

That workflow should focus on role-relevant capabilities, concrete diagnostic evidence, context for observed performance, and whether questions distinguish relevant performance. Maintain fairness and privacy. Do not include protected characteristics, irrelevant personal history, compensation details, or speculative labels. Use only information relevant to the role and legitimate hiring process.

### Other specialized cases

Consider a dedicated workflow for legal review, incident response, medical matters, formal performance processes, or regulated financial decisions. If no specialized workflow is available, state the limitations, preserve confidentiality, and prepare only within the user’s authority.

If the meeting is not a special case, continue.

## 5. Share a situation brief before asking questions

After research is complete, provide a concise situation brief in a user-visible channel. This is a real preparation artifact, not hidden reasoning or a raw data dump. It should take roughly a minute to read.

Choose the shape that best fits the meeting.

### Narrative brief

Use for most relationship, exploratory, advisory, or ongoing-partner meetings.

Suggested sections:

- **Who they are**
- **Where things stand**
- **Why this meeting is happening**
- **Live tensions and unknowns**

### Decision-shaped brief

Use for negotiations, recruiting conversations, sales conversations, fundraising, closing discussions, or other calls with a live decision.

Suggested sections:

- **The ask**
- **Their alternatives and timeline**
- **The user’s position and leverage**
- **Risks or failure modes**
- **Open unknowns**

A short narrative section may be followed by a decision section when both relationship history and the immediate decision matter. Do not ask the user to choose a brief format unless the meeting is unusually high stakes and the format genuinely changes what must be prepared. Make a sensible choice and proceed.

## 6. Ask targeted questions

Ask focused questions after the situation brief and before writing the final goal and agenda, unless the purpose, authority, desired stance, and recurring agenda are all genuinely documented and unambiguous. When uncertain, ask rather than assume.

At minimum, ask about the **primary outcome** and at least one of **failure mode**, **tone**, **specific ask**, **authority**, or **sensitive substance**. Always include an open catch-all question.

Do not ask the user to write the agenda. Ask questions that determine the agenda’s target and constraints.

Useful question axes include:

- What outcome would make the meeting successful?
- Is the user trying to diagnose, decide, build trust, persuade, recruit, sell, negotiate, or hand off?
- What is uncertain about the other party’s situation or level of commitment?
- Is there a sensitive topic the user should address directly, probe first, or avoid for now?
- What would make the meeting go badly?
- Is there a concrete request or next step to land, and how direct should the user be?
- What decisions can the user make in the meeting, and what requires later approval?
- Is there anything else the user wants to land, avoid, or keep private?

Use compact, addressable labels so the user can answer quickly. Provide three or four genuinely distinct options, with a recommended option first when the research supports one. Do not force a false either/or when two actions can sensibly be combined.

```markdown
1. What is the primary outcome?
   - **1a (recommended):** Diagnose their interest and agree a concrete next step
   - **1b:** Build the relationship without making a specific ask
   - **1c:** Make a direct proposal and seek a decision

2. How direct should the close be?
   - **2a (recommended):** Agree a date and named follow-up artifact
   - **2b:** Offer help and leave the next step open
   - **2c:** Keep this meeting exploratory only

3. Is there anything else to land or avoid?
   - **3a:** Nothing to add
   - **3b:** I will add notes or context
   - **3c:** There is a sensitive constraint to account for
```

If more than four questions are needed, ask them in rounds. Put questions whose answers affect later options first, then tailor later questions to the answers received. Keep labels unique and sequential across rounds.

Before sending, check:

- Every question is numbered.
- Every option has one unique matching label.
- Options are meaningfully distinct.
- The catch-all question is included.
- No question asks the user to do the preparer’s work.

Wait for answers before finalizing the agenda. If the user declines to answer, write a clearly labeled provisional plan and identify the assumptions that could change it.

## 7. Create the meeting-preparation record

Create the record in the user’s chosen workspace or meeting-management system. Use a restricted destination when the content requires it. Set the meeting date as a date-only value unless the user specifically needs the time stored separately. Keep the title scannable; date plus key person or meeting topic is a useful default.

Use this structure:

```markdown
# [Date] [Person or meeting topic]

## Context

Who they are, relationship history, why this meeting is happening, and the few links or documents that matter. State explicitly if this is the first meeting. For recurring contacts, summarize the relationship arc rather than only the most recent interaction.

## Goal

[A specific meeting goal based on the evidence and the user’s answers.]

## Agenda

### 0–5 min: Open and frame

**Say**

[Short opener or framing statement.]

**Interviewer note**

[What to establish or avoid.]

### 5–20 min: Diagnose [topic]

**Questions**

1. [Question]
2. [Question]

**Interviewer note**

[Signals to listen for and assumptions to test.]

### 20–35 min: Discuss, pressure-test, or propose [topic]

**Say**

[Transition or proposal.]

**Questions**

1. [Question]

**Interviewer note**

[Specific trade-off, evidence, or concern to surface.]

### 35–45 min: Close and create momentum

**Questions**

1. [Forcing question that secures a decision, date, owner, artifact, or explicit reason not to proceed.]

**Interviewer note**

[Backup close if no decision can be made live.]

## Five most important questions to ask

1. [Most decision-relevant question]
2. [Key diagnostic question]
3. [Question that tests the main assumption or gap]
4. [Question that surfaces a likely obstacle]
5. [Specific close for a next step, owner, date, or artifact]

## Timely note

[Optional: a current event, publication, deadline, or relationship detail worth mentioning.]
```

Adjust timing to the actual meeting duration. For a short meeting, use fewer stages and protect time for the key question and close. For a longer workshop, add decision checkpoints and ownership sections rather than filling time with generic discovery.

### Agenda writing rules

- Make each agenda stage a heading, not a dense list.
- Use **Say** for prepared phrasing, **Questions** for spoken questions, and **Interviewer note** for private guidance.
- Keep spoken prompts natural and do not wrap them in quotation marks.
- Do not nest complicated lists under agenda stages.
- Put the most important topic early enough to discuss it properly.
- Include a forcing function when the meeting aims to move a decision: a next meeting date, a named artifact, a decision owner, a deadline, or an explicit no.
- The five-question list must be ranked and scannable. It is an in-meeting cheat sheet, not a second agenda.

## 8. Privacy and sensitive-content review

Before saving or sharing the record, perform a content review. Remove or generalize:

- Compensation, salary, equity, benefits, compensation bands, or offer figures.
- Personal details unrelated to the meeting’s legitimate purpose.
- Sensitive information copied from private communications that the meeting audience does not need.
- Unverified claims presented as facts.
- Credentials, private links, account information, or identifying operational details.
- Language that makes unsupported judgments about a person rather than describing observable, role-relevant evidence.

If sensitive context is essential, store it only in an appropriately access-controlled location or refer to it at a high level in the shared meeting record.

## 9. Validate and deliver

Before considering the work complete, verify:

| Check | Pass condition |
|---|---|
| Meeting facts | Date, timezone, duration, attendees, and topic are correct. |
| Evidence | Relationship history and meeting trigger come from relevant authorized sources. |
| Artifact review | The relevant proposal, draft, or deck was read, or its absence is clearly flagged. |
| Clarification | Targeted questions were asked when the user’s priorities or constraints were not clear. |
| Goal | The goal reflects the user’s answers rather than an assumed objective. |
| Agenda | Timing is realistic and the most important issue appears early. |
| In-meeting aid | Exactly five decision-relevant questions are ranked and easy to scan. |
| Privacy | Sensitive and unrelated information has been removed or appropriately restricted. |
| Workspace record | The record was created in the chosen system and is accessible to the intended audience. |

Open or surface the record in the user’s preferred meeting environment if that capability is available. Confirm where it was saved and note unresolved gaps, such as a missing artifact or an unverified attendee role.

## 10. Post-call review for high-stakes meetings

For meetings intended to persuade, recruit, negotiate, sell, fundraise, or move another party toward a decision, arrange a post-call review shortly after the meeting when the user authorizes it.

The review should:

1. Retrieve an authorized transcript or meeting notes.
2. Compare what happened with the preparation goal and agenda.
3. Record the outcome, commitments, objections, signals, and next steps.
4. Identify one or two communication patterns to preserve or improve, using dated evidence rather than vague self-criticism.
5. Update the relationship record and assign follow-up owners and deadlines.

Do not create or access recordings or transcripts without appropriate notice, consent, and authorization. Skip the post-call review for purely informational meetings unless the user asks for it.

## Common failure modes

- **Researching people but not the actual document under discussion:** Read the artifact and anchor questions in its claims and decisions.
- **Drafting an agenda before learning the user’s aim:** Share the brief, ask focused questions, then write the agenda.
- **Writing a generic discovery agenda for a live decision:** Include the decision, alternatives, authority, risks, and forcing close.
- **Overloading the record with research:** Keep only context that changes what the user should ask, say, avoid, or decide.
- **Treating uncertain information as fact:** Label unknowns and ask about them.
- **Skipping the catch-all question:** The user may have crucial context absent from accessible records.
- **Using vague closes:** Convert “follow up sometime” into an owner, date, decision point, or named artifact.
- **Recording sensitive details in a broad workspace:** Remove, generalize, or move them to an appropriate access boundary.
- **Finishing with a chat summary but no durable record:** Create and validate the preparation record in the user’s chosen system.

A meeting-preparation record is complete when it is evidence-based, aligned with the user’s stated intent, safe for its audience, practical during the meeting, and clear about what should happen next.


---
name: capture-meeting-actions
description: Review authorized meeting records to identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date or date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine unfinished commitment that should be tracked.

## Purpose and operating rules

Use meeting records only for a legitimate work purpose and with clear authorization to access them. Use the minimum relevant sources and details needed to identify commitments. Do not copy unrelated sensitive personal information, private discussion, health information, or confidential details into tasks or status reports. Keep outputs within the access boundary of the selected task system and its intended audience.

Before each run, apply these outcome rules:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same person or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels it as an action item. Confirm ownership in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, expression of interest, or open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply known delegation boundaries supplied by the user or organization. Meeting attendance does not make the user accountable for every action in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect:

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
- Source and related links that are appropriate to include in the task system

Create no task when work was completed live, another person owns it, the meeting was purely informational and any needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

## 4. Decide the task shape

Combine actions into one task when they have the same counterparty, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect months later.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

Use this readiness gate before task creation: every proposed task must have a clear owner, an unfinished outcome, a sensible scope, a plausible date, and enough context to stand alone.

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

Write context so it remains clear later. Prefer absolute dates over terms such as “yesterday” or “next week.” Avoid unnecessary private discussion in a task system that may be broadly visible.

If the task is to send a message, include a ready-to-send draft rather than merely saying “email them.” Follow the user’s known writing preferences. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable. For introductions, use double opt-in: seek permission from each relevant party before connecting them.

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
- Outputs include only information appropriate for the task system’s access boundary.
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
description: Prepare, conduct, and document a structured hiring reference call that gathers role-relevant, concrete evidence while respecting authorization, privacy, and appropriate access boundaries.
---

# Run a reference call

Use this workflow when an authorized hiring team needs a reference conversation for a candidate. The goal is to reduce specific hiring uncertainty with direct, role-relevant evidence—not to collect vague praise or unnecessary personal information.

## Purpose and boundaries

Before preparing the call, confirm that the organization has a legitimate hiring purpose and is authorized to contact the referee. Follow applicable consent, notice, confidentiality, and record-retention expectations.

Use only the minimum information needed for the decision:

- Focus on observed work, professional conduct, role-relevant capabilities, and working conditions.
- Do not seek protected, highly personal, medical, family, financial, or otherwise unrelated sensitive information.
- Do not share private interview notes, other referees' identities or comments, compensation details, or internal deliberations unless authorized and necessary.
- Keep notes within the hiring team’s appropriate access boundary.
- If the candidate has limited ability to provide conventional references, use a fair alternative such as a former collaborator, client, supervisor, work sample, or structured job-relevant assessment.

## Inputs

Collect or confirm:

- Candidate name and the role under consideration.
- Referee name, professional contact details, and their stated relationship to the candidate.
- Call date, time, and communication method.
- The candidate’s authorization or the organization’s approved reference-check process.
- The role’s expected outcomes, core responsibilities, and relevant capabilities.
- Current hiring stage and decision timeline.
- Specific unresolved questions from interviews, work samples, or other assessments.
- Any completed references that are appropriate to review under the organization’s privacy practices.

If key information is missing, proceed with what is available but clearly mark the gap. Do not invent a relationship, timeline, or hiring concern.

## Readiness gate

Do not start the call until you can answer these questions:

- What role-relevant decision will this call inform?
- What did the referee directly observe?
- Which one to three uncertainties should the call test?
- Is the proposed scope authorized and proportionate?
- Can the notes be stored and shared safely?

If the referee’s relationship is too distant, their knowledge is indirect, or the call is unauthorized, do not treat the conversation as a substantive reference. Seek an appropriate alternative.

## 1. Find and verify the call context

Confirm the scheduled event or agreed arrangement. Record the meeting title, date and time, attendees, communication link or dial-in details, and any scheduling context that affects the conversation.

If no event exists, create a clear call record using the organization’s chosen meeting or applicant-tracking system. The record—not a separate chat response—is the working deliverable.

## 2. Gather only relevant context

Review authorized, minimum-necessary sources such as the candidate’s application, role description, prior correspondence, approved recruiting records, and prior reference notes. Use organization communication records only when access is authorized and the information is relevant.

Establish:

- The role and hiring stage.
- How the referee was introduced and whether they agreed to speak.
- The referee’s role, organization, and professional background as relevant to their credibility.
- How, when, and how closely the referee worked with the candidate.
- The candidate’s stated responsibilities and claimed outcomes in that period.
- Other planned or completed references, only for coordination and evidence comparison.
- Links to approved candidate materials, such as an application profile, professional profile, portfolio, or work samples.

When checking public sources, use them to verify professional context, not to infer personal traits. A short search such as the referee’s name plus organization is usually sufficient.

## 3. Analyze evidence before writing questions

Separate evidence into three categories:

- **Direct observation:** What the referee personally saw the candidate do.
- **Interpretation:** The referee’s view of why it happened or what it means.
- **Inference:** What the hiring team may reasonably conclude for this role.

Review completed reference notes for patterns, contradictions, and unanswered questions. Do not present one referee’s opinion as fact to another referee. Instead, convert it into a neutral testable question.

For example:

- Weak approach: “Another referee said the candidate misses deadlines. Do you agree?”
- Better approach: “How did the candidate manage commitments when priorities changed? Please share a specific example.”

If this is the first reference, identify evidence that later calls can compare: ownership, reliability, feedback response, collaboration, and performance under the conditions most similar to the role.

## 4. Create the call brief

Create a single meeting record in the organization’s chosen system. Keep the context concise and use bullet points rather than long narrative.

Use this template:

```markdown
# [Referee name] — reference for [Candidate name]

## Call details
- Date and time: [date, time, time zone]
- Communication method: [link or method]
- Interviewer: [role or name]
- Referee: [name, role, organization]

## Context
- Candidate: [approved links to application, professional profile, portfolio, or work samples]
- Role under consideration: [role]
- Hiring stage and decision timing: [stage]
- Referee relationship: [how they worked together, duration, reporting or collaboration context]
- Other references: [names or roles, if needed for coordination]

## Briefing notes
- Decision uncertainty: [one to three questions the call must reduce]
- What this referee can uniquely assess: [directly observed area]
- Evidence to validate: [specific role-relevant claim or outcome]
- Prior pattern to test neutrally: [question, not an accusation]
- Limits on this reference: [distance from work, time elapsed, indirect knowledge, or other constraint]

## Opening
> Thank you for making time. I am calling as part of an authorized hiring process for [Candidate]. We are considering them for [Role]. I would like to understand your direct experience working with them, especially their work on [relevant area]. Please focus on professional, role-relevant examples. We will handle your feedback according to our hiring confidentiality practices.

## Questions
- [questions]

## Notes and assessment
- Direct observations:
- Referee interpretations:
- Concrete examples:
- Evidence that supports role alignment:
- Evidence that raises a development need or risk:
- Contradictions or unanswered questions:
- Confidence and limitations:
- Follow-up owner and next step:
```

## 5. Write actionable briefing notes

Briefing notes are the highest-value part of preparation. They should tell the caller exactly what to learn and why.

Write direct, evidence-focused instructions:

- “The candidate described leading a cross-functional launch. Ask what they personally owned, what changed because of their work, and how the referee observed it.”
- “A prior reference described strong strategic judgment but limited detail on execution. Ask for an example involving planning, follow-through, and measurable results.”
- “This referee was a client rather than a manager. Prioritize communication, reliability, expectation-setting, and delivered outcomes; do not expect detailed evidence about internal management.”

Avoid unsupported labels, personality diagnoses, and broad conclusions from sparse evidence.

## 6. Conduct the conversation

Begin by confirming the referee’s relationship, scope of observation, and willingness to speak candidly. State the professional and confidential purpose without promising confidentiality beyond the organization’s actual policy.

Use a unified question list. Start broad, then move to specific examples.

### Core questions

- How did you work together? What were each of your roles, and how closely did you work day to day?
- What work or outcomes did the candidate personally own?
- What did strong performance look like in practice? Please describe a specific example.
- How did their results compare with the expectations of that role and environment?
- What is their strongest role-relevant capability?
- Where did they need the most support, structure, or development?
- How did they respond to difficult feedback, changing priorities, or setbacks?
- If they left a similar role after three months, what work-related reason would be most likely?
- If they were succeeding after three months, what development area would be most useful to prioritize next?
- What management approach or work environment would help them contribute effectively?
- Would you choose to work with them again? In what type of role and under what conditions?
- What important question have I not asked?

Follow vague praise or concern with: “What did that look like?” “What was their specific contribution?” “What happened next?” “How often did that occur?” and “What evidence would help us understand the impact?”

### Role-specific probes

Adapt probes to the actual role and assessment criteria. Examples:

- **Operations or program delivery:** How did they handle changing requirements, build repeatable processes, prioritize competing work, and communicate with varied stakeholders?
- **Community or partnership work:** How did they build trust, respond to conflict, maintain boundaries, gather feedback, and turn needs into reliable programs or systems?
- **Operational leadership:** How did they scale processes, manage budgets or vendors where relevant, make tradeoffs between speed and control, and create clarity across teams?
- **Technical or analytical work:** How did they define quality, test assumptions, explain complex work, handle errors, and make decisions with incomplete information?

## 7. Record signal accurately

Take concise notes during or immediately after the call. Attribute statements clearly. Distinguish what happened from what the referee thinks it means.

Document:

- Specific examples and outcomes.
- The referee’s proximity to the work.
- Relevant conditions, such as team size, authority, timeline, or available support.
- Strengths supported by examples.
- Development areas supported by examples.
- Contradictions with other evidence.
- Unanswered questions and follow-up actions.
- Your confidence level and the reason for it.

Do not record unnecessary sensitive details. Do not convert uncertain claims into definitive findings.

## 8. Evaluate and close the loop

After the call, compare the evidence with the role’s required capabilities and the rest of the hiring process. Ask whether the reference distinguishes relevant performance, rather than whether the candidate simply seems generally impressive.

A reference is more useful when it provides:

- Direct observation of work similar to the target role.
- Specific examples with outcomes and context.
- A credible account of both strengths and development needs.
- Evidence that can be compared with interviews, work samples, and other references.

A reference is less useful when it is based mainly on reputation, distant acquaintance, generic praise, or a context unlike the role. Record that limitation rather than forcing a conclusion.

Update the meeting record with a short synthesis and any follow-up. Share it only with authorized decision-makers. The hiring decision should use the full evidence set; no single reference should determine the outcome on its own.

## Audit checks

Before closing the record, verify:

- The call had a legitimate, authorized hiring purpose.
- Notes contain only relevant professional information.
- The referee relationship and observation limits are clear.
- Key claims are supported by examples or marked as interpretation.
- Questions tested role-relevant uncertainties fairly and neutrally.
- Prior reference information was not improperly disclosed.
- The record includes candidate context, call details, questions, notes, confidence, and next steps.
- Access and retention follow the organization’s privacy practices.

## Common failure modes

- **Generic question list:** Fix by identifying decision uncertainty before the call.
- **Overweighting seniority or confidence:** Fix by weighting direct observation and concrete examples.
- **Leading questions based on prior feedback:** Fix by asking neutral, behavior-based questions.
- **Treating a client, peer, or supervisor as interchangeable:** Fix by tailoring questions to what that relationship can actually reveal.
- **Collecting irrelevant personal information:** Fix by returning to the role and documented assessment criteria.
- **Writing research in a separate message but not the meeting record:** Fix by placing all useful context, probes, and findings in the call record.
- **Confusing a referee’s opinion with a verified fact:** Fix by labeling observation, interpretation, and inference separately.
- **Using one reference as a final verdict:** Fix by comparing it with the full, role-relevant evidence set.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and privacy, verifying rendered state, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for tasks that require interaction with a website: completing rendered forms, changing settings, collecting information from dynamic pages, testing a user flow, or working in an authenticated dashboard. Use it when a supported direct interface, static retrieval method, or ordinary page request cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful value after changing it, and do not take a consequential final action until the account, target, authorization, and page state are verified.

An automation command returning success does **not** prove that the website accepted the change. Modern web applications may keep state outside the visible document, commit values only after focus changes, replace controls during a re-render, or display an error even though an action completed.

## 1. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer an authorized, documented programmatic interface when it can perform the requested task. It is usually more reliable than recreating browser interactions.
2. **Headless browser automation.** Use this for public pages, test environments, routine dynamic-page extraction, screenshots, UI tests, and forms that do not require the user's established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing session, single sign-on state, account-specific dashboard, or user-directed browser context.

Before driving a browser, check whether a direct route exists. Review official documentation, ordinary form actions, page source, and authorized visible network activity for supported endpoints. A browser form may submit structured data to a service that can be used safely through an approved interface.

Do not use undocumented interfaces to bypass access controls, consent boundaries, terms, rate limits, paywalls, or other restrictions. Do not use an authenticated visible session merely because it is convenient: it can interrupt the user's work and increases privacy and account risk.

If a site blocks automated browsing, do not try to defeat its protections for research or collection. A visible browser may be appropriate only when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and an established session is needed. Do not weaken browser security, warnings, access restrictions, or anti-abuse protections.

## 2. Protect account identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into screenshots, logs, notes, or reports. Keep outputs within the requester's appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated context, identify the correct account, workspace, environment, and browser profile. Never infer identity from a generic browser-window name, tab title, remembered default, or connection label.

Use these rules:

- Announce when taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Classify the intended context explicitly: for example, personal, work, testing, staging, or production.
- Select the browser profile or connection that corresponds to that context rather than relying on a generic browser selector.
- Confirm the signed-in account through a reliable account indicator before opening or changing the real target.
- If the required account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not reveal credentials, session tokens, recovery information, private account data, or security settings in output or logs.
- Do not disable security controls, multi-factor authentication, browser warnings, or access restrictions to make automation easier.

Use an account preflight gate before actions that change data. Confirm the account identity, environment, and target object. If the automation system has a verification marker or permission gate, mark the context verified **only after** the account check actually passes. Never create or enable such a marker in advance merely to unlock actions.

A useful pre-action question is: **Which account is this? Which environment is this? What exact item will change?** If any answer is uncertain, resolve it before proceeding.

### Visible-browser protocol

When a visible session is necessary, announce the action before connecting, then proceed with the authorized task without silently taking over an existing browser. Use a newly created workspace unless the user has identified a specific existing tab to use.

If more than one browser profile or connected session exists, select the one whose configured context matches the task. Then verify the account through a reliable account page, profile menu, tenant indicator, or equivalent first-party identity display. Do not rely on a display name alone when a more reliable identifier is available.

If the needed profile is not available, ask the user to connect or open the appropriate profile. Do not guess based on which profile was most recently active. If restarting a browser would close the user's tabs or interrupt work, obtain explicit approval before doing so.

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

If a page reloads, re-renders, or the session changes between passes, do not assume the earlier state remains valid. Restore the intended values if necessary and verify them again before committing.

## 4. Inspect the rendered page before editing

Do not begin by guessing selectors, filling fields by numeric position, or trusting a visual approximation. First inspect the rendered page and collect enough structure to identify controls safely.

For each relevant control, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or label relationship.
- Current value and whether the field is required.
- Validation rules, character limits, formatting behavior, and disabled state.
- Whether an apparent field is the actual editable control, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, date, or tab causes the page to re-render.

Address controls by stable semantic identity, such as visible label text, accessible name, or explicit label relationship. Do not use document indexes where labels are available: dynamic applications can change element order between loads or after re-rendering.

Before changing a record or setting, inspect its current state. This prevents modifying the wrong item or overwriting existing values unintentionally.

### Generic form inspection pattern

Use the selected browser automation capability to list relevant controls before writing fill logic. The inspection should record at least tag, input type, role, label, required state, and current value or text length.

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

## 5. Use the correct input method for each control

Different controls need different interactions. A generic “set value” operation is not reliable for all of them.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use the normal text-input mechanism. | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away. | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus it, select existing content, enter text through keyboard-style events, then blur. | Direct document mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle. | Selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed. | A click can toggle an already-correct value. |
| Date/time picker | Choose date and time, then verify the rendered summary. | Popovers can reinterpret typing or clear related fields. |
| File upload | Confirm the file, destination, and privacy implications first. | Uploading may begin immediately and can be difficult to undo. |

For framework-driven editors, simulate normal user interaction rather than writing directly to low-level page properties. A robust general sequence is: focus the actual editable element, select existing text, delete it, enter new text through keyboard-style events, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible rich-text editor with a hidden input. Editing the hidden input may appear successful in an inspection result while server-side validation treats the visible editor as empty. Target the control that the user interacts with and that the application actually reads. If an accessibility locator points to an empty wrapper, inspect the underlying editable element and follow its label relationship.

If changing a dropdown, checkbox, tab, or date can refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterwards and confirm that earlier entries remain present.

### Rich-text fill sequence

Use this sequence when a normal fill operation does not update a content-editable control:

```text
1. Locate the actual editable element using its label relationship.
2. Focus the element.
3. Select existing content.
4. Delete the selected content.
5. Insert the intended text through keyboard-style input events.
6. Move focus to a neutral page element to commit the edit.
7. Wait briefly for rendering to settle.
8. Read the editor's visible or accessible content back.
```

Do this one field at a time. On pages that re-render after each change, moving focus away and verifying each editor before touching the next can prevent earlier edits from being replaced.

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

Do not use clipboard access as a required dependency for headless automation. Browser contexts may deny clipboard permissions. Pass approved values through the automation system's secure input mechanism instead, and do not hardcode secrets in scripts or logs.

## 7. Run a pre-submit readiness gate

Before any final submission or high-impact change, inspect the full relevant page state again. Confirm all of the following:

- The correct account, workspace, and environment are active.
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

A suitable confirmation format is:

> Ready to [final action] for [target]. The key details are [brief summary]. This will [cost, audience, or irreversible effect]. [Open question, if any.] Shall I proceed?

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
| Headless and visible browsers show different behavior | The site varies behavior by browser context. | Prefer an authorized direct interface; for an explicit legitimate task, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior. | Close it through a neutral page action and re-verify affected fields. |
| A visible error may be cosmetic | The task may already have completed. | Inspect resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |
| A browser restart is proposed to recover a session | Restarting could close unrelated tabs or interrupt the user. | Request explicit approval before restarting; use a fresh session or another route when possible. |

## 11. Maintain the workflow carefully

When a task reveals a repeatable failure or a reliably successful pattern, record the lesson in the applicable shared procedure, subject to its change-control rules. State both the symptom and the safe fix. Consolidate similar lessons into general principles rather than accumulating incident-specific notes.

Keep environment-specific details separate from this workflow. The user or responsible administrator should configure approved browser tools, profiles, script locations, supported interfaces, retention rules, and account-verification methods. Revalidate those operational details when tools, websites, or browser behavior change.

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
description: Create, test, improve, evaluate, and package reusable AI skills from new ideas, existing drafts, or workflows demonstrated in conversation. It supports lightweight collaboration and rigorous evidence-based iteration.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, revise an existing one, assess whether it works, or improve when it activates. A skill is a focused set of instructions and optional supporting resources that help an AI perform a recurring job consistently.

The core loop is:

1. Understand the job, its intended outcome, and its boundaries.
2. Draft or revise the skill.
3. Test it on realistic requests.
4. Let a person review representative outputs and measure objective requirements where appropriate.
5. Improve the skill based on evidence.
6. Repeat until the result is useful, reliable, and not overfitted to the tests.
7. Optionally improve the skill description so it activates for the right requests.

Do not assume every project needs every step. A user may want a quick draft, a collaborative “good enough” pass, or a rigorous benchmark. Identify where they are in the loop and help them move forward from there.

## Communication principles

Match the user’s technical vocabulary and experience. Use plain language by default. Terms such as *evaluation* or *benchmark* may be useful, but briefly explain them when needed. Avoid unexplained terms such as “schema,” “assertion,” or “JSON” unless the user is comfortable with them.

When asking questions, explain why the answer matters. For example, instead of asking only “What is the output format?”, ask: “What should a successful result look like—an answer in chat, a structured report, a file, or an action? This determines how we test completion.”

Keep the user involved at decision points:

- Confirm the intended job before writing extensive instructions.
- Ask before choosing a restrictive scope, tool requirement, or approval policy.
- Share proposed test cases before relying on them.
- Let human judgment lead for subjective quality such as tone, visual design, and creative usefulness.
- State uncertainty rather than pretending a requirement, source, or capability is available.

If the work involves private communications, personnel records, customer information, health information, financial information, or other sensitive data, require a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Omit unrelated sensitive details from outputs, respect consent and reasonable privacy expectations, and keep results within the appropriate access boundary.

## 1. Determine the starting point

First identify which situation applies.

### A. New skill

The user has an idea such as “I need a skill that helps with recurring project status reports.” Start with discovery and a first draft.

### B. Existing draft or installed skill

The user already has instructions and wants them edited, simplified, tested, or optimized. Preserve the established skill identity unless the user explicitly asks to rename it. Read the current instructions before proposing changes.

If the installed copy cannot be edited directly, make a writable working copy in a user-approved location. Preserve the original until the revised version has been reviewed and packaged.

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
2. **Activation:** What kinds of user requests, wording, or situations should activate it?
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
- “Should it draft an external action for review, or take that action only after explicit confirmation?”

### Research before drafting

If the environment provides relevant documentation, similar skills, user-approved reference materials, or domain guidance, review them before drafting. Research should reduce burden on the user rather than replace their authority over requirements.

Use research to identify:

- Existing conventions or output standards.
- Constraints imposed by an available tool or file format.
- Reusable patterns from comparable tasks.
- Safety, privacy, compliance, or approval requirements.

When reviewing private records or communications, verify that the request has a legitimate purpose and that access is authorized. Prefer the narrowest relevant date range, source set, and fields. Do not include unrelated personal details merely because they were available.

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

Skills and bundled resources must behave in ways a user would reasonably expect from their description. Do not include hidden collection, destructive behavior, credential handling, unauthorized access, data exfiltration, exploit behavior, or misleading automation.

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

State the checks needed before completion. Examples include confirming required fields, validating calculations, citing the source of key claims, preserving original data, and flagging uncertainty.

For hiring, promotion, admission, or assessment workflows, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Do not infer sensitive traits from irrelevant information or use personal background as a shortcut for capability.

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
- Are private-data rules, authorization requirements, and approval boundaries appropriate to the task?

Prefer a lean, understandable prompt over a long prompt filled with rules that do not affect outcomes. Excessive absolute language is a warning sign unless the behavior is truly non-negotiable, such as a safety or authorization boundary.

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

Do not write tests that only mirror the wording of the skill. Vary phrasing, detail level, and user sophistication. Avoid personal scenarios and sensitive records; test the general category of challenge instead.

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
      "evidence": "The final section lists unavailable data points and requests them."
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
- **High variation:** A result differs substantially between comparable runs, suggesting ambiguity, environmental instability, or an unreliable instruction.
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
3. **Explain intent.** State why an action protects quality, usability, privacy, or safety.
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

# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate distinct options for a decision or problem, assess tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long idea list. Surface genuinely different paths, explain their tradeoffs plainly, and leave the user with a small set of credible choices.

## 1. Gather relevant context

Start with information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other records that are accessible in the current environment, review only the sources needed to understand the decision.

When accessing non-public communications or records, confirm there is a legitimate purpose and appropriate authorization. Use the minimum relevant information, omit unrelated personal or sensitive details, and keep the output within the user's access boundary.

If the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, deadlines, and dependencies
- Stakeholder concerns, responsibilities, and decision rights
- Evidence about what has already been tried

Do not search broadly by default. Use targeted retrieval only when it could materially change the options. If important information is unavailable, state an assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The initial wording may describe a symptom or requested solution rather than the underlying decision. For example, “Should we add a feature?” may really mean, “How should we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, the choice is low consequence, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must represent a fundamentally different approach, not merely a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes process, incentives, scope, timing, or the problem framing
- At least one surprising option, such as delaying, partnering, removing scope, or doing nothing

Do not be contrarian merely to seem creative. “Do nothing” is useful only when observation, timing, avoided cost, or reduced distraction has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

- **What:** One or two sentences explaining the approach
- **Strengths:** One or two concrete advantages
- **Weaknesses:** One or two concrete disadvantages or failure risks
- **Effort:** Low, Medium, or High

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose evaluation criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, and stakeholder burden. Add domain-specific criteria when they matter more than these defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may choose an option, request more detail, reject the framing, ask for additional options, or combine approaches.

If the user proposes a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record: the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After the decision is recorded, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The options are genuinely distinct rather than superficial variants.
- The framing reflects the actual decision.
- Constraints and evaluation criteria are explicit.
- Weaknesses are candid and proportionate.
- Effort labels are plausible.
- Recommendations follow the user’s stated priorities rather than default assistant preferences.
- Any use of private context was authorized, minimal, and appropriately bounded.


---
name: pressure-test
description: Find weak points in a leading strategic idea before commitment by testing assumptions, evidence, dissent, reversibility, and failure signals.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design the implementation.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the selected approach, if applicable.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes a defense of that idea.
- If the same topic was tested recently and no material evidence, assumption, or condition has changed, do not repeat the exercise. Use the prior findings in the decision process.
- If reviewing internal records, feedback, or communications, have a legitimate purpose and authorization. Use only the minimum relevant material, and do not expose unrelated or sensitive personal information.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Steelman the strongest reasonable version before criticizing it.
- Ask one forcing question at a time. Wait for the answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Use available evidence, such as metrics, research, experiments, customer feedback, documented decisions, and role-relevant stakeholder input. Separate facts, inferences, and forecasts.
- Identify possible dissent by role—such as finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent anyone's view.
- Skip a section only when it is truly irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging without changing the decision-maker's intent. Include the action, mechanism, expected outcome, timeframe, and key conditions.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original claim is already a steelman, say so. If your stronger restatement changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold. Rank them by how badly the decision would be damaged if they proved false. Make assumptions observable where possible.

| Rank | Assumption | Type | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|---|
| 1 | [State the assumption] | [Fact, estimate, or belief] | [Evidence summary] | [Low, medium, or high] | [Test or disproof method] |

Replace broad claims such as “users will value this” with a defined behavior, audience, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Choose questions based on the riskiest assumptions and adapt later questions to the answers. Do not provide the full question list as a questionnaire.

Possible question types:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would have to happen in the next 30 or 90 days for this to be judged wrong?
- **Counterfactual:** What comparable attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this works, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which relevant role would object most strongly? What would that person say? Has that perspective been sought directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not an answer; ask for observed behavior, data, comparisons, or credible commitments.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, usually 6 to 12 months. Name the three most likely failure modes, ordered by likelihood or impact. Include an early signal that can be observed soon enough to change course.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or accountable role |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable signal] | [Check or owner] |

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State the strongest likely objection from each role. If that perspective has not been sought, mark it as an evidence gap. Silence is not agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence that names the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test incomplete or failed rather than approving the idea.

## 7. Give a verdict and handoff

Choose one verdict and name the next step.

- **GREEN — proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER — test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it: for example, a small interview set, expert review, prototype, or short data collection period. Run the test, then decide with the result recorded.
- **RED — stop, redesign, or reopen options.** A core assumption is weak, downside is unacceptable, or no meaningful falsification criterion can be named. Generate alternatives, redesign the proposal, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with one concrete next action: a verb, an accountable owner, and a deadline when useful.

**Example:** `Research owner: interview five target users by 18 Oct and compare results with the adoption assumption.`

## Final audit

Before closing, verify that the output includes:

- a confirmed steelman;
- three to five ranked load-bearing assumptions;
- five to eight forcing questions explored sequentially;
- a pre-mortem with early warning signs;
- credible dissenting roles and objections;
- a clear mind-change criterion;
- a GREEN, AMBER, or RED verdict with a next workflow step; and
- one concrete next action.

Common failures include skipping alternatives, asking all questions at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and issuing a positive verdict without falsifiable criteria or monitoring.


---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to apply the right amount of rigor, make a clear call when ready, preserve reasoning for meaningful choices, and learn from outcomes. The goal is not maximum analysis: most decisions should take minutes, while a small number deserve a complete record and later review.

## Core rules

1. **Match rigor to stakes and reversibility.** Spend more time only where reversal is costly or consequences are broad.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may recommend an option in conversation, clearly labeled as assistant analysis. Add it to a record only if the user asks for that.
4. **Record only with permission.** “Should we do X?” asks for analysis, not for a decision record. Create or update a record only when the user asks to log, track, open, or commit it, or explicitly agrees to recording.
5. **Protect privacy and access boundaries.** Before accessing shared communications, personnel information, customer data, or a shared register, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and omit unrelated sensitive personal details.
6. **Do not confuse a task with a decision.** If there is no meaningful alternative, redirect to planning or execution.

If a shared register has an audience beyond the user, confirm that the audience is appropriate before writing. For sensitive matters such as health, relationships, compensation, or confidential personnel issues, offer a private record in the user’s chosen private workspace or keep the discussion in chat.

## 1. Select the mode

Determine whether the work concerns a new or existing decision.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review point and has not yet received a meaningful outcome assessment.

If the user explicitly names the mode, follow that instruction. Otherwise, if authorized to access the decision register, search for overlapping records before creating a duplicate. Search only the authorized register and only for information relevant to the decision.

For a resumed decision, append new information rather than rewriting history. For a review, use the recorded prediction and original reasoning as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Put the question in a decidable form. Establish:

- What exact choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing where relevant?
- What is the deadline or decision trigger?
- What result is sought?
- What happens if no action is taken?

If the issue is broad and credible options do not yet exist, generate options before evaluating them. If there is only one viable route, say so directly: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time when classification is unclear. Use the cost of unwinding the choice as the main test: consider money, time, trust, operational disruption, opportunity cost, and reputational effects.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default. |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; use a light record if useful. |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, and consult relevant stakeholders. |
| Direction-setting | Shapes strategy, culture, finances, or operations over an extended period | Full analysis, explicit dissent, and named prerequisite conversations. |

If a user calls something trivial, ask what it would cost to unwind. If they cannot state the cost quickly, or the cost is uncertain, treat the choice as at least reversible rather than trivial.

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: continued attention can cost more than an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. For each option, state one major strength, one major weakness, and a rough effort or cost estimate.
3. Recommend an option and name the decisive reason.
4. If uncertainty matters, identify the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before committing, pressure-test the leading option. A valid pressure test examines assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and substantial stakeholder objections.

If no relevant pressure test has occurred in the current work context, stop the commitment flow and state:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not bypass the gate merely because the user is in a hurry. Continue only after the pressure test is complete or the user explicitly overrides it with a reason. If the test reveals a serious unresolved failure, return to option generation, redesign the option, gather decision-changing evidence, or run a bounded test.

After the gate is satisfied:

1. Define the options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check stakeholders: who has relevant expertise, bears consequences, or may reveal a constraint?
4. Offer a recommendation labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has occurred, unless the user explicitly accepts and records a reason for proceeding without it. If the work is being rushed, state which consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence in its favor.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies a tradeoff rather than disguising judgment.

Keep these categories distinct:

- **User’s stated view:** Positions the user actually expressed.
- **Assistant analysis:** Recommendation and reasoning supplied by the assistant, identified using the assistant identity active in the current environment.
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

Use the user’s chosen document system, decision register, or private file. A useful record contains status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. Use these review defaults unless the user names a better trigger: one month for reversible choices, three months for hard-to-reverse choices, and six months for direction-setting choices. Add a reminder through the user’s authorized calendar or task system for high-stakes reviews.

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until the user commits. When resuming, append a dated thinking-log entry rather than altering earlier entries.

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

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat a bad outcome as proof of a bad process, or a good outcome as proof of a sound process.

## Completion message

When a decision is made, summarize it clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [DD MMM]
Review: [DD MMM YYYY or trigger]
Record: [location, if one exists]
```

Use direct language. Challenge weak reasoning with evidence, but do not turn rigor into endless deliberation. Once the appropriate readiness gates are met, name the decision and move forward.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through recommendation, implementation, verification, and handoff.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, automation, integration, or operational problem where the solution is not already clear. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user requests analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the problem

Start with the underlying problem, not the proposed solution. When asked to “build X,” work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the situation meaningfully better?
- What constraints, dependencies, or affected systems matter?

Write a concise problem statement and descriptive requirements. Describe the desired outcome and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so directly.

Research available documentation, code, and authorized records before asking questions. If reviewing communications, tickets, or records about people, have a legitimate purpose and clear authorization; use only the minimum relevant sources and omit unrelated or sensitive personal details.

## 2. Assess priority and decision type

Decide whether the work is worth doing now. Consider severity, frequency, affected users, opportunity cost, existing alternatives, and the cost of delay. Treat “do nothing,” “deprioritize,” or “improve the workaround” as valid options.

Distinguish between:

- **Reversible decisions:** Small choices that are easy to change. Use reasonable judgment and proceed.
- **Hard-to-reverse decisions:** Persistent data changes, migrations, public interfaces, long-lived settings, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation and document the rationale when appropriate.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operating procedures, and prior attempts. Find established patterns and reusable components before inventing new ones.

Identify compatibility requirements, deployment practices, privacy and security expectations, supported environments, ownership boundaries, monitoring, and rollback constraints. Respect access boundaries: do not expose source material or information beyond the audience authorized to receive it.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve current authentication, privacy, and data behavior.
- Must be feasible within the available delivery and maintenance capacity.
- Should avoid unnecessary dependencies and permanent configuration.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variants of the same design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution, such as clearer instructions, a process change, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Building, buying, or integrating an existing service.

For ambiguous or high-impact problems, generate a wider candidate set before narrowing. Keep each option concise: what it is, what it solves, major costs, dependencies, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that vary by runtime conditions.
- Validate inputs and fail clearly for invalid states. Do not hide programming errors by returning plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Place changes at the correct design boundary; avoid temporary fixes that create lasting complexity.

## 6. Evaluate and recommend

Compare viable options against the evaluation criteria. Present a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and their tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Keep proposals direct and brief. Store durable proposals in the user’s chosen shared documentation system when review or collaboration is needed; otherwise provide them in the current workspace. Use a clear date-prefixed title, such as `10 Oct 2026: Solve — topic`.

**Readiness gate:** Do not implement until the recommendation is accepted, or the user has explicitly authorized implementation under an agreed decision rule. For analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, dependencies, migration and rollback strategy, test strategy, deployment steps, and ownership of follow-up actions.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, security, and failure behavior.

Do not claim success based only on code being written. State what was tested, the result, and what remains unverified. Commit, publish, or deploy only according to the user’s repository and release practices.

## 8. Audit and hand off

Before handoff, check that:

- The implemented scope matches the approved recommendation.
- Hard-to-reverse commitments received explicit approval.
- Tests cover the important success and failure paths.
- Sensitive information is not included in outputs or logs beyond the authorized boundary.
- Rollback, monitoring, and ownership are clear where relevant.

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail rather than temporary implementation notes.


---
name: shape-and-draft
description: Shape consequential documents through evidence, decision-focused interview rounds, readiness checks, drafting, and audit before delivery.
---

# Shape and draft a document

Develop an important document by shaping the thinking behind it before writing. Determine the change the document must produce, gather relevant evidence, resolve material choices with the authorized decision-maker, then draft and audit the smallest document that can do the job.

Use this workflow for strategies, narratives, operating agreements, briefs, proposals, scorecards, and decision memos when the argument, commitments, boundaries, or operating model remain unsettled. Do not use the full process for a quick edit, a formatting task, or a document whose substantive decisions are already clear.

If the work involves private communications, personnel records, customer information, or other sensitive material, use it only for a legitimate purpose and with clear authorization. Review only the minimum relevant sources, avoid including unrelated personal information, respect consent and expected confidentiality, and keep findings and the resulting document within the appropriate access boundary.

## Classify the request

A request may name a document type, desired outcome, audience, source material, or some combination. Treat a proposed document type as a hypothesis until its purpose is clear.

Use a **full shaping process** when the document is consequential and its argument, scope, commitments, or operating model are materially unsettled, or when the requester asks for deep thinking, multiple question rounds, or close alignment before drafting.

A substantive interview round resolves a distinct layer of choices and uses the answers to determine the next round. A restatement of prior discussion or a request for broad approval does not count as a substantive round.

For a lower-stakes request, use the same logic in a lighter form: establish the purpose, verify critical facts, identify any material decision that remains open, and draft. Do not impose multiple rounds when they would add delay without improving the result.

## 1. Work backwards from the outcome

Start with the change the document must produce. Establish:

- Who will read it.
- What those readers should understand, decide, approve, or do afterward.
- What is unclear, contested, blocked, or going wrong now.
- Whether the document mainly needs to explain, persuade, decide, coordinate, or govern.

Do not accept “write a narrative” or “make a strategy page” as the goal. Identify the actual job the document must perform. For example, a request for a strategy may really need a decision memo if leaders must choose between alternatives, or an operating agreement if teams already agree on direction but cannot coordinate execution.

## 2. Select the artifact

Recommend the form that best serves the goal:

- **Narrative:** Builds shared understanding of why something matters and what bet is being made.
- **Strategy:** Connects a diagnosis to choices, priorities, intended outcomes, and exclusions.
- **Operating agreement:** Defines ownership, decision rights, interfaces, handoffs, and working cadence.
- **Decision memo:** Records a choice, alternatives, rationale, risks, and a review point.
- **Scorecard:** Defines a role or team mission, outcomes, and role-relevant capabilities.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the relevant tradeoff and recommend one form. If the choice would materially affect the argument, structure, or decisions required, ask the authorized decision-maker to confirm it before proceeding.

A hybrid should have a clear reason. Do not combine formats merely to preserve every available detail. Use a hybrid when, for example, readers need both a strategic case for change and an explicit model for ownership and implementation.

## 3. Gather and classify evidence

Read supplied material first. Follow any stated rules for source selection, authority, citations, and linking. Scale research to the stakes and use only sources that are authorized and relevant.

For a consequential internal document, seek records likely to contain prior decisions, current definitions, supporting evidence, dissent, constraints, ownership context, and relevant performance information. Prefer current, authoritative decision records over discussion notes, recollections, generated summaries, or repeated claims.

Apply these rules:

- Respect a stated hierarchy of sources.
- Resolve contradictions where evidence permits and surface material contradictions that remain.
- Do not ask the decision-maker for facts that available sources can answer.
- Do not modify, overwrite, or otherwise change source material unless explicitly instructed.
- Use sensitive information only when it is necessary to the document’s legitimate purpose. Omit unnecessary personal details from notes, summaries, and drafts.
- Cite, link, or otherwise identify evidence according to the requested document standard, especially when a claim could be challenged.

Keep evidence separate from alignment:

- Sources can establish what happened, what people said, and what an authoritative record currently states.
- Sources do not automatically establish what the current decision-maker believes, is willing to promise, or chooses to exclude.
- A plausible synthesis, repeated pattern, or implication is an **inference**, not a settled decision.
- Ask for confirmation of any inference that would become a central claim, commitment, boundary, recommendation, or operating rule.

Before the first interview round, provide a short situation brief covering:

- What the sources establish.
- What has already been explicitly confirmed.
- What is inferred but unconfirmed.
- The central tension, gap, or missing logic.
- The recommended artifact.
- The important uncertainties that only the decision-maker can resolve.

## 4. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds already completed in the current conversation and do not repeat settled questions.

Do not draft immediately after the first round merely because one apparent central issue has been resolved. The next round should test consequences revealed by the first: boundaries, tradeoffs, counterarguments, ownership, definitions, or execution implications.

Ask four to eight focused questions per round. If fewer than four material questions genuinely remain, ask all of them and say that this is a narrow final check. Do not add ritual questions just to reach a number.

Each numbered question should normally seek one decision. Do not bundle independent choices, such as ownership, coordination, handoffs, and success measures, into one broad question. Bundling creates false alignment.

Use a compact question block that permits fast, unambiguous replies:

1. Number every question continuously: `1.`, `2.`, `3.`.
2. Keep each number attached to the same question across rounds.
3. For bounded choices, provide three or four mutually exclusive, decision-relevant options labeled `a.`, `b.`, `c.`, and, when useful, `d.`.
4. Put the recommended option first unless prior context makes another order clearer.
5. Use two options only when the decision truly has only two distinct states.
6. Put questions and options on consecutive lines without blank lines inside the question block.
7. Let the respondent reject the framing or provide an alternative answer.

Example:

1. Which direction should the document recommend?
   a. Focus first on the highest-impact problem; this narrows scope but clarifies accountability.
   b. Address all related problems equally.
   c. Present the options without a recommendation.
2. Who should hold the final decision right?
   a. The accountable lead.
   b. A cross-functional decision group.
   c. A designated sponsor after consultation.

Each round should:

1. Start with the updated model and state what changed because of earlier answers.
2. Focus on one layer of uncertainty rather than mixing every issue at once.
3. Explain the tradeoff behind the recommended option.
4. Separate source-supported observations from choices the decision-maker must make.
5. Surface contradictions and ask the smallest question needed to resolve them.
6. Include at least one pressure test when the document is persuasive or strategically consequential.

A common progression is purpose; strategy; operating model; definitions and measures; then expression, format, and destination. Adapt the sequence to the work, but preserve the answer-dependent loop. Later questions must arise from earlier answers, not from a generic questionnaire.

After every answer round:

1. Match shorthand and free-text answers to their question numbers, preserving qualifications such as “mostly c” or “not sure.” Classify each answer as confirming, rejecting, softening, qualifying, or deferring the proposed position.
2. Trace downstream implications. A changed audience, softened commitment, new exception, or rejected framing often creates another material question.
3. Update and show a concise alignment ledger.
4. Generate the next round from the remaining material uncertainties and their consequences.

Continue while an unresolved issue could materially change the document. If the requester explicitly asks to draft before the process is complete, name the one or two most important consequences of the uncertainty, then follow the instruction.

## 5. Maintain an alignment ledger

Keep a compact working record throughout the conversation:

- **Confirmed:** Choices explicitly made by the authorized decision-maker.
- **Source facts:** Claims established by current, authoritative evidence but not selected as present choices.
- **Inferred:** Plausible interpretations that remain unconfirmed.
- **Open:** Questions that could materially change the document.
- **Corrected:** Assumptions or claims a participant has rejected.

Update this ledger after every answer round. Never reintroduce a corrected assumption. If confirmed statements conflict, surface and resolve the conflict rather than hiding it in vague language. Never promote an inference to confirmed solely because several sources support it.

For a full shaping process, show a concise version of the ledger before each later round. Every major draft claim must be a confirmed choice, a supported source fact, or explicitly framed as a proposal, assumption, or open question.

## 6. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document’s substance. Before drafting, provide a concise pre-draft synthesis covering the intended job, audience, central position, important boundaries, and any deliberate open questions.

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
- Has the document’s response been confirmed or supported by evidence?

Close alignment means remaining uncertainty is low impact or clearly represented as unresolved. It does not require artificial certainty.

## 7. Draft and deliver

Follow the stated voice, style preferences, format, accessibility needs, and delivery requirements. Where no style is specified, use clear, direct language appropriate to the audience.

Write the smallest document that accomplishes the agreed purpose. Prefer clear claims, concrete decisions, explicit ownership, and clear boundaries over polished but vague abstractions. Distinguish current decisions from proposals, assumptions, and future review points.

Make the draft as simple as the substance allows:

- Prefer short, common words over formal or inflated language.
- Write complete, natural sentences. Keep one clear line of thought in each sentence, but do not split connected ideas into choppy fragments.
- State the point first. Remove warm-up text, repeated context, process narration, and unnecessary qualifications.
- Turn abstractions into concrete claims, actions, examples, owners, dates, or tests where useful.
- Use focused paragraphs. Use bullets only for real lists, and write bullet items as full sentences unless they are compact labels.
- Keep action-oriented sections short. Combine related points, cut lower-value detail, or move supporting detail to an appropriate reference when a section becomes a flat inventory.
- Prefer the more concise version when it preserves meaning. Concise writing removes unnecessary ideas and words; it does not require every sentence to be short.
- Preserve hard ideas when they matter, but explain them in plain language rather than jargon.

Honor the requested destination using the user’s chosen system. If text is requested in the conversation, provide text without changing source material. If a document must be created or updated elsewhere, do so only as instructed and verify that the intended content is present, structurally correct, and readable in its final form.

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
- Asking participants for facts that authorized sources can answer.
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
- Including sensitive personal information that is not necessary for the document’s purpose.
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
description: Learn a paper, article, or topic through a short Socratic dialogue using retrieval, explanation, and application instead of passive summary.
---

# Learn with a tutor

Guide a learner through a paper, article, post, or topic using active recall and reasoning rather than passive explanation. The goal is durable understanding: the learner should be able to explain key ideas, identify limits, connect them to prior knowledge, and use them in a decision or new situation.

## Core learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to reconstruct ideas from memory and in their own words.
- **Probe mechanisms.** Ask why and how an idea works, what assumptions it depends on, and what evidence supports it.
- **Require generation.** Ask the learner to create examples, analogies, predictions, objections, and applications before supplying them.
- **Use productive difficulty.** Make the task challenging enough to require effort, but not so hard that the learner cannot form a meaningful answer.
- **Practice transfer.** Move beyond the original material by testing the idea in a new setting, against a competing explanation, or in a practical decision.
- **Reveal gaps through inquiry.** When an answer is incomplete, inconsistent, or inaccurate, use focused questions to help the learner find the gap. Explain directly only after a fair attempt.

## Conversation workflow

### 1. Establish prior knowledge and the learning goal

Begin before discussing the source in detail. Ask what the learner already knows, believes, or has experienced, along with what they need to achieve.

Use one or two prompts such as:

- “What do you already think is true about this topic, and what led you to that view?”
- “What are you trying to be able to explain, evaluate, or do after this conversation?”
- “What part of this material seems most confusing, surprising, or important?”

Use the answer to calibrate difficulty and identify useful prior knowledge or likely misconceptions.

### 2. Elicit the central idea from memory

Ask the learner to explain the main argument, finding, or concept without quoting the source.

- “In your own words, what is the main claim?”
- “Why should someone believe that claim?”
- “What problem is this idea meant to solve?”
- “How would you explain it to a thoughtful friend in 30 seconds?”

If the learner has not yet engaged with the material, ask for an initial prediction or working model. Then direct them to inspect the relevant portion before returning to retrieval.

### 3. Select two or three high-value ideas

Do not cover every detail. Choose a small number of ideas that are central, difficult, consequential, or easy to misunderstand. For each idea, follow this cycle:

1. Ask the learner to state or reconstruct it.
2. Probe the reasoning, causal story, evidence, and assumptions.
3. Ask for a concrete example, analogy, or application.
4. Test it with an objection, boundary case, or alternative explanation.
5. Adjust the next question to the learner’s response.

Keep each turn short. Ask only one or two substantive questions at a time.

## Question toolkit

Choose prompts that require explanation rather than recognition:

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What is the mechanism, step by step?”
- “What evidence would distinguish this explanation from another one?”
- “Can you give a concrete example from a familiar situation?”
- “Where might this fail or stop applying?”
- “What is the strongest objection to this argument?”
- “How does this connect with another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one assumption changed?”

Avoid simple yes-or-no questions unless they immediately require the learner to explain their reasoning.

## Responding and correcting

Be warm, rigorous, and specific. Avoid generic praise. If an answer is strong, identify what made it strong—such as naming an assumption, distinguishing evidence from interpretation, or giving a relevant counterexample—then raise the challenge.

When an answer is inaccurate or incomplete:

1. Do not immediately state the correction.
2. Ask a focused follow-up that exposes the tension.
3. Allow one or two real attempts to resolve it.
4. If the learner remains stuck, explain the missing distinction concisely.
5. Ask them to restate the corrected idea or apply it to a fresh case.

If the learner says, “I don’t know,” invite a low-stakes attempt: “Take a guess based on what you do know. What seems most plausible, and why?” Give a hint after an attempt, or sooner if foundational knowledge is missing.

## Calibration and progress checks

Increase difficulty when answers come easily: request a counterexample, prediction, comparison, or transfer to a new domain. Reduce difficulty when the learner is lost: narrow the question, isolate one assumption, use a simpler case, or ask them to defend one of two plausible explanations.

Periodically give a brief evidence-based progress check:

| Check | What to state |
|---|---|
| Demonstrated understanding | [What the learner has explained accurately or applied well.] |
| Remaining uncertainty | [What is still vague, unsupported, or confused.] |
| Best next step | [The next question, concept, or practice task.] |

Do not treat recognition, repeated wording, or familiarity with terminology as mastery. Look for accurate explanation, reasoning, and transfer.

## Closing gate

Before ending, ask:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a concise final explanation or a future retrieval prompt. End with the clearest next concept or question to revisit.

## Guardrails

- Do not summarize unless the learner explicitly asks; first invite their own summary.
- Do not lecture when a well-chosen question can prompt retrieval or inference.
- Do not define jargon automatically; ask the learner to define it first, then clarify if needed.
- Do not make the interaction easy merely to be encouraging.
- Do not turn the exchange into a fixed quiz; build questions from the learner’s actual answers.
- Do not skim an entire source when deep understanding of a few core ideas would be more valuable.


---
name: write-in-my-voice
description: Draft or revise email in the user’s authentic voice using approved style evidence, accurate facts, and a concise safety check before delivery.
---

# Write in my voice

Use this workflow when drafting, replying to, or polishing an email on the user’s behalf. The goal is a copy-ready message that sounds like the user while remaining accurate, appropriate for the recipient, and within the user’s authority.

## 1. Establish authorized voice evidence

Use a current style guide if the user has one. You may also use examples of messages the user actually sent when there is a legitimate purpose and clear authorization to access them. Review only the minimum relevant examples, and do not expose unrelated private content or sensitive personal details in the output.

Prefer recent, comparable messages over old or generic examples. Build a practical voice profile:

- Typical greeting and sign-off.
- Formality, warmth, and directness by relationship.
- Sentence and paragraph length.
- Common vocabulary, contractions, punctuation, and formatting.
- How the user makes requests, follows up, declines, apologizes, corrects errors, or handles disagreement.
- Phrases, tones, formatting, or punctuation the user avoids.
- Approved reusable facts, links, boilerplate, and standard replies.

If evidence conflicts, use the most recent consistent pattern or ask which preference is current. Do not treat a style guide as permission to disclose its private contents.

## 2. Confirm the email brief

Identify the minimum information needed to send a safe message:

1. Who is the recipient and what is their relationship to the user?
2. What outcome should the email produce?
3. Which facts, names, dates, links, attachments, decisions, or commitments must appear?
4. What tone is appropriate: familiar, neutral, formal, firm, or sensitive?
5. Is there a deadline, approval requirement, confidentiality concern, or other constraint?

Do not invent availability, decisions, promises, pricing, legal positions, opinions, emotional reactions, or facts. Ask a focused question when missing information would materially change the message.

## 3. Adapt voice to context

Preserve the user’s recognizable voice, but adjust for audience and stakes.

| Situation | Adaptation |
|---|---|
| Familiar colleague or established contact | Use the user’s normal level of brevity and familiarity. |
| New, external, senior, or formal recipient | Keep the voice recognizable, but add needed context and use more careful wording. |
| Request or follow-up | State the requested action, responsible party, and timing plainly. |
| Correction, rejection, or disagreement | Be direct, factual, and respectful; avoid defensive explanations and excessive praise. |
| Sensitive matter | Include only necessary details, avoid unnecessary personal information, and keep the message within the intended access boundary. |

Use approved standard wording or factual material when it fits the situation. Do not reuse a template if it would be inaccurate, misleading, or overly impersonal.

## 4. Draft the smallest complete email

Use this default structure when appropriate:

1. Greeting, if consistent with the user’s usual practice.
2. Purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Clear close and sign-off, if appropriate.

Write for action. Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Use bullets only when they make choices, actions, or logistics easier to scan.

Remove material that does not help the recipient understand or act, including:

- Throat-clearing or narration about the drafting process.
- Generic compliments, repeated thanks, and filler.
- Empty hedging that weakens a clear message.
- Unnecessary apologies or explanations.
- Details that are private, irrelevant, or not authorized for this recipient.

## 5. Audit before delivery

Review the draft line by line:

- Would the user plausibly write these words?
- Do greeting, sign-off, rhythm, punctuation, and formatting match the available evidence?
- Is the tone appropriate for the recipient and stakes?
- Are names, dates, links, attachments, and references accurate?
- Did the draft add any unsupported claim, commitment, emotion, or promise?
- Is the requested action or decision easy to find?
- Does the email reveal only information appropriate for this recipient?
- Can any sentence be removed without reducing clarity or usefulness?

If there is no style evidence, state the assumption briefly and use a broadly useful default: concise, clear, warm-professional, and direct. Invite the user to provide a few examples or preferences for future drafts.

## Output format

Provide the final email as copy-ready text. If clarification is necessary, ask only the specific question needed to draft safely. Do not add commentary after the final copy unless the user asks for alternatives, rationale, or revision notes.


---
name: professional-social-post
description: A platform-independent workflow for drafting, revising, and auditing professional social posts with strong hooks, defensible claims, useful substance, and privacy-aware publishing.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a rough draft, an article, a transcript, an interview, a research finding, a podcast, or a simple topic.

The goal is not to make an announcement sound enthusiastic. The goal is to make the right reader stop, understand a useful point, and have a reason to care. A strong post has a specific claim, real substance, and a tone that sounds like a person with evidence and judgment, not a press release, academic abstract, motivational template, or outrage prompt.

This workflow works across professional social platforms. Before drafting, confirm or choose:

- **Platform and format:** text post, image caption, document carousel, thread, newsletter excerpt, or promotion for a longer piece.
- **Audience:** such as practitioners, founders, researchers, policy professionals, customers, candidates, or a professional community.
- **Purpose:** share an insight, explain a concept, announce a change, promote a longer piece, invite informed discussion, or support a campaign.
- **Voice:** first-person, team voice, formal, conversational, concise, technical, or another stated style.
- **Constraints:** target length, required claims, forbidden terms, approved terminology, accessibility needs, formatting limits, and link strategy.
- **Evidence and permissions:** sources for facts, approval to name people or groups, and any sensitive details that must be omitted.

If the user supplies a writing guide, approved past posts, audience research, or brand standards, use those as the source of voice and style rules. Do not assume a particular person’s voice, publishing process, internal system, or link-placement rule.

## Scope, routing, and privacy

Identify the content type before drafting. Different genres need different structures, levels of evidence, and permission checks.

| Content type | Use this approach |
|---|---|
| Career or participant story | Use a case-study structure: starting point, turning point, concrete outcome, evidence, and lesson. Obtain clear permission for names, career details, quotes, images, and results. |
| Research or evidence post | Lead with the finding, explain the method or basis, state material uncertainty, and separate facts from interpretation. |
| Announcement | Lead with the concrete change and reader relevance, not internal excitement. |
| Article, report, or podcast promotion | Lead with the strongest finding or guest insight, not “new article” or “new episode.” |
| Carousel or document caption | Give the central claim and one or two useful specifics, then explain what the visual material adds. |
| Sensitive topic or personal record | Confirm legitimate purpose and authorization. Use only the minimum relevant information, remove unrelated personal details, and keep the output within the appropriate access boundary. |

If a request could be a case study, contains a person’s story, or has unclear disclosure rights, ask a concise routing question before writing. For example:

> Is this a general insight post, or a case study centered on one person’s outcome? If it is a case study, what details, quotes, and identifying information are approved for public use?

Use private communications, internal records, and personal information only for a legitimate, authorized purpose. Public availability is not automatically permission to amplify personal information in a new context. Use only information necessary for the post, honor consent and audience expectations, and omit unrelated details about a person’s employment, health, location, contact information, family, finances, or private history.

## Non-negotiable accuracy rules

1. **Do not invent facts.** Never fabricate statistics, names, quotes, results, titles, testimonials, dates, or research findings.
2. **Use precise detail only when supported.** Exact figures, roles, dates, and outcomes are stronger than vague language, but do not turn an estimate into false precision.
3. **Separate evidence from judgment.** State what the source shows, then identify the implication, recommendation, or interpretation.
4. **Preserve material uncertainty.** If evidence is limited, ranges are wide, assumptions are strong, or causation is unclear, say so plainly.
5. **Ask for missing evidence early.** If a proposed claim cannot be supported, request a source, narrow the wording, qualify it, or remove it.
6. **Avoid misleading urgency.** Do not inflate stakes to create attention. A defined risk plus a practical response is more credible than broad catastrophe language.
7. **Respect consent and expectations.** Do not use a person’s story, image, quote, or outcome beyond what they approved for the intended audience.

## Audience and voice

Write for the reader most likely to find the post useful or act on it, not for everyone who might vaguely relate to it. Specificity is a feature: it signals to the right audience that the post is for them.

Use this default voice unless the user provides another one:

- Direct, clear, and conversational.
- Short sentences and concrete nouns.
- Active voice where possible.
- One main claim per sentence.
- Sober about problems and practical about responses.
- Confident only where the evidence warrants confidence.
- Specific rather than promotional.

Avoid these recurring failure modes:

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | “We are thrilled to announce an exciting initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences with unexplained terms. | Make the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Large claims about danger without a mechanism or response. | Name the specific risk, evidence, uncertainty, and practical intervention. |
| Generic inspiration | Positive language without an action, trade-off, or example. | Name the concrete decision, result, or lesson. |

## Core workflow

### 1. Inspect the source before choosing a template

Read the source closely. Do not begin by forcing it into a familiar format. Find the strongest usable thread, which is often buried below the title or opening paragraph.

Look for:

- An unusual or surprising fact.
- A specific number that creates tension.
- A defensible counterintuitive conclusion.
- A concrete before-and-after result.
- A meaningful trade-off or deliberate constraint.
- A disagreement between credible views.
- A framework, checklist, or model readers may save.
- A sentence that changes how a reader sees the problem.

The formal headline of a source is often not the best post angle. A post should usually develop one thread, not summarize every section.

If several viable angles exist, do not silently choose one. Present two to four options and let the user choose when the choice affects direction.

**Angle-selection prompt:**

> I see several possible post angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [specific story, outcome, or disagreement]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Select one primary thread. Save secondary insights for the body, visual material, a follow-up comment, or later posts.

### 2. Generate hooks before drafting the body

The first line determines whether the rest of the post is read. Generate five to ten candidate hooks, then show a numbered shortlist of three to five when user input would be valuable. Do not commit to the first plausible opening.

A hook must make an honest promise that the body fulfills. It should make sense by itself to someone who has not read the source.

Useful hook patterns:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific body of evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Concrete outcome:** “[Role or team] moved from [starting point] to [outcome] in [timeframe].” Use only with evidence and permission.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only if the body defends it.
- **Short thesis:** “[Concept] is better understood as [concrete analogy].”
- **Focused disagreement:** “Why do two credible groups reach such different conclusions about [specific issue]?”

For each shortlisted hook, include a one-line strategic note.

| Hook | Strategic purpose |
|---|---|
| “[Specific claim or finding].” | Leads with a concrete result and creates a reason to continue. |

Use the **swap test**: if the topic word could be replaced with an unrelated field and the hook still works, it is too generic. Make the opening depend on the real subject, fact, or tension.

Avoid:

- “Excited to share,” “thrilled to announce,” or similar announcement framing.
- Throat-clearing such as “In today’s fast-moving environment.”
- Empty cliffhangers that never produce a payoff.
- Three rhetorical questions in a row.
- Broad motivational statements.
- Clickbait such as “You will not believe” or “This changes everything.”

### 3. Choose one structure

Choose the structure that fits the evidence. Do not combine several structures unless there is a clear reason.

1. **Counterintuitive claim → evidence → implication**  
   Best for research, data, and argument posts. Lead with the surprise, provide support, then explain what readers should reconsider or do.

2. **Changed mind → trigger → updated view → takeaway**  
   Best for thoughtful first-person posts. State the prior belief, what changed it, and the revised conclusion.

3. **Problem → why it matters → practical response**  
   Best for explainers and operational or policy content. Keep both the problem and response concrete.

4. **Result → how it happened → reusable lesson**  
   Best for launches, team outcomes, and approved case studies. The result must be real and specific.

5. **Framework → examples → application**  
   Best for content that readers may save and revisit. Name the framework only if the name makes it clearer.

6. **Specific announcement → reader relevance → next step**  
   Use only when the announcement itself is notable. Lead with what happened and why the reader should care.

7. **Strategic trade-off → rationale → consequence**  
   Useful for explaining an intentional anti-goal: something a team has deliberately chosen not to optimize for, and why.

### 4. Draft: hook, tension, payoff

Use this default shape:

- **Hook:** the strongest claim, result, or tension.
- **Tension or setup:** why it matters, what is surprising, or what assumption it challenges.
- **Payoff:** the evidence, story, framework, or practical insight. The post must be useful even if the reader never clicks, swipes, or buys.
- **Soft close:** exactly one focused question, one practical takeaway, or one clear pointer.

A useful default is under 300 words, but substance and platform conventions should decide the final length. Every extra paragraph must earn its place.

Use white space. One- or two-sentence paragraphs are easy to scan on a phone. Use bullets only when the content is genuinely list-shaped, such as three findings, four risks, or a checklist. Do not force flowing prose into bullets.

For a carousel or document caption:

- State the main idea in the caption.
- Include one or two of the strongest specifics.
- Explain what readers will gain from the visual material.
- Do not rewrite every slide in the caption.

For a post promoting a longer piece:

- Put the most interesting finding in the post itself.
- Use the longer piece for depth, methods, source material, or additional examples.
- Follow the user’s chosen platform strategy for link placement.
- Do not make “read the link” the primary value proposition.

## Calls to action and questions

Use one close only. A strong close gives the reader a real, bounded way to respond.

Good examples:

- “Which constraint matters most in your work?”
- “What evidence would change your view?”
- “Where does this model fail in practice?”
- “The full analysis includes the assumptions and source material.”

Weak examples:

- “Thoughts?”
- “Let me know what you think.”
- Several unrelated questions at once.
- Requests to comment, tag, repost, or react solely to increase engagement.

A question should invite knowledge, informed disagreement, or relevant experience. Do not use engagement bait. If the user plans to participate in replies, recommend substantive responses to genuine early comments rather than formulaic prompts for interaction.

## Editing pass: remove templated language

Run a separate editing pass after drafting. Cut language that sounds polished but says little.

Replace or remove:

- Inflated verbs such as “leverage,” “unlock,” “harness,” “navigate,” “empower,” and “cultivate.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” “remarkably,” and “genuinely.”
- Empty hedging frames such as “it is worth noting,” “one might say,” and “arguably,” unless uncertainty is genuinely central.
- Softeners such as “just,” “simply,” “essentially,” “ultimately,” and “at the end of the day.”
- Abstract nouns such as “journey,” “transformation,” or “paradigm” when a concrete event can be named.
- Transition sentences that only repeat the preceding paragraph.
- Dramatic frames such as “The truth is” or “Here is the reality.” State the point directly.
- Decorative punctuation or formatting that the destination platform will not render correctly.

If the user has a punctuation preference, follow it. Otherwise, favor periods, commas, and line breaks over theatrical punctuation. Use emphasis sparingly and verify that the intended platform supports it. Read the post aloud: if it sounds like a generic thought-leadership template rather than someone making a real point, rewrite it.

## Revision protocol

When the user gives feedback, revise the flagged line and the adjacent logic first. Do not replace the entire post unless asked.

- If the hook is not sharp enough, offer replacement hooks before rebuilding the body.
- If a claim is overstated, improve the evidence, narrow the claim, or add a necessary qualification.
- If a paragraph is slow, cut setup before adding explanation.
- If a prior version contains the strongest line, preserve it unless the user asks to remove it.
- If a sentence depends on weak or missing support, flag it candidly and offer a supported alternative.

Multiple small options are often more useful than one full redraft, especially for hooks, closers, and uncertain wording.

## Readiness gate and audit

Do not present a draft as final until it passes this check:

- Does the first line earn attention when read alone?
- Does the post develop one clear point rather than several competing ideas?
- Does it contain at least one concrete detail, outcome, example, number, or mechanism where appropriate?
- Could the main claim withstand a knowledgeable challenge?
- Does it offer value without requiring a click, swipe, or purchase?
- Is uncertainty stated where it materially affects the conclusion?
- Is the language specific to this topic rather than reusable for any industry?
- Is the close one focused action, question, or pointer?
- Are names, quotes, figures, and personal details supported, authorized, and appropriate to disclose?
- Does the formatting work on the intended platform?
- Does the tone remain respectful, professional, and non-inflammatory for the intended audience?

If any answer is no, revise before handoff.

## Handoff and publishing plan

Present only what helps the user decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the format the user requested.
3. Any unsupported claim, missing input, or uncertain line.
4. Suggested link text or first-comment text, if relevant to the user’s platform strategy.
5. A concise publishing reminder appropriate to the platform, such as responding promptly and substantively to genuine comments.

Do not claim that a format, timing tactic, or engagement metric guarantees reach. Platform behavior changes. Treat distribution advice as a hypothesis to test across comparable posts.

## Common failure patterns

- **Announcement disguised as content:** Readers learn that a change happened, but not why it matters. Lead with the fact, consequence, or lesson.
- **Pure teaser:** The post asks readers to click without delivering insight. Share the central finding, then use the linked material for depth.
- **Unsupported precision:** A striking number appears without source, scope, or caveat. Verify it, qualify it, or remove it.
- **Generic inspiration:** The post sounds positive but has no action, trade-off, or example. Name the concrete decision or mechanism.
- **Overpacked summary:** The post tries to cover every section of a source. Select one thread and reserve the rest for the original material or future posts.
- **Bolted-on promotion:** A product, service, or program appears at the end without a real connection. Remove it, create a separate post, or make the relationship specific and immediate.
- **Forced engagement:** The post asks for reactions rather than conversation. Replace it with one genuine question or a useful conclusion.
- **Unapproved personal disclosure:** A story uses more personal information than needed. Remove identifying or sensitive details, confirm consent, and keep the post within the agreed audience boundary.

The final standard is simple: the post should sound like someone with evidence, judgment, and a real point to make. It should give the right reader something useful even if they do nothing else.


---
name: case-study-post
description: Create a verified, concise case study post with strong hooks, a clear mechanism of change, quote-card options, approval checks, and a practical call to action.
---

# Write a case study post

Use this workflow to turn authorized source material about a person’s career, learning, or professional change into a concise public case study. It works especially well for professional social posts, and can be adapted for newsletters, community updates, recruitment pages, program alumni stories, or campaign landing pages.

The purpose is to show a credible, specific change: where the person started, why they acted, what concretely helped, what happened next, what they do now, and what the reader can do. Do not manufacture inspiration through vague praise. A good case study helps a relevant reader recognize their own situation in the subject’s before-state.

## Privacy, authorization, and access boundary

Before using interviews, applications, messages, profiles, records, or internal notes about a person, confirm there is a legitimate publishing purpose and clear authorization to use those materials. Use the minimum relevant sources and facts. Do not include unrelated personal details, sensitive details, or information outside the audience and access boundary agreed for the post.

If a source contains private information, extract only what is needed to support the story. Do not expose compensation, health, family, immigration, legal, financial, relationship, or confidential employer information unless the person has explicitly approved publication of that specific detail.

## Inputs and intake

Request all available source material and publication constraints. Useful inputs include:

- An interview transcript, meeting notes, or written Q&A
- An application, intake form, or approved biography
- A current professional profile or public announcement
- Public work samples, projects, papers, products, or awards
- A message documenting a result
- A previous draft, outline, or notes from the subject
- The target audience, publication channel, word limit, and call to action
- An editorial or brand voice guide
- Any approved wording, prohibited claims, or legal review requirements

Build a private working record before drafting:

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns, consent status |
| Before-state | Previous role, field, goal, uncertainty, constraint, or alternative path |
| Trigger | Why they joined, applied, changed direction, or took action then |
| Intervention | Program, community, event, resource, mentor, or product involved |
| Mechanism | Concrete help, such as a realization, introduction, job post, feedback, or resource |
| Now-state | Current role, organization or team if approved, practical work, result, or output |
| Timeline | Relevant dates and the elapsed time between meaningful events |
| Evidence | Sources supporting names, figures, dates, roles, outputs, and quotes |
| Cost or risk | Any meaningful tradeoff, only if approved for public use |
| CTA | The reader’s next action and where it should lead |

If critical information is missing, ask focused questions before drafting. Do not guess at names, titles, organization names, dates, figures, paper titles, results, or causal claims.

Useful questions:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they decide to take part or act at that point?
4. What one or two concrete things helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a publicly shareable output, project, placement, publication, product, or result?
8. Did they take on a cost or risk they want to share publicly?
9. Which names, claims, figures, and direct quotes are approved?
10. Who should this post help or persuade, and what should they do next?

## Evidence and verification rules

Never invent facts or upgrade a claim for dramatic effect. If a source says someone contributed to a project, do not call them the lead. If they explored an opportunity, do not say they received it. If a source says they co-authored work, do not imply sole ownership.

Automated transcripts and summaries are useful but fallible. They can mishear names, organizations, technical terms, numbers, and titles. Cross-check important details against a stronger source before using them publicly.

Use this evidence order unless there is a clear reason to use another:

1. The subject’s direct, recent confirmation
2. Official public records, published work, or a formal announcement
3. A current professional profile
4. An original written application or statement from the subject
5. Interview transcripts and automated summaries
6. Informal third-party messages

Separate working notes into three categories:

- **Verified fact:** A claim supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn by the writer. Use it only when evidence supports it, and phrase it modestly.

Do not claim that a course, community, mentor, tool, or event caused an entire outcome unless that causal claim is well supported. Prefer precise wording such as “the program helped them see the field differently” or “they found the opportunity through the community.”

## Sensitive-content approval gate

Flag the following for explicit subject approval before publication:

- Salary, compensation changes, financial hardship, or pay comparisons
- Personal health, family, legal, immigration, or relationship information
- Harsh language about an employer, previous role, or career choice
- Unreleased work, confidential projects, or unpublished titles
- Direct quotations, especially strong opinions or criticism
- Claims about why an employer selected or hired someone
- Claims of impact or causation that cannot be independently verified
- Timelines that reveal private circumstances

If approval is not available, use an approved, honest fallback or remove the detail. Do not make the story more dramatic to conceal uncertainty.

## Build the story beats

Create a concise private outline before writing.

### 1. Before-state

Capture the person’s role, background, and reader-relevant uncertainty. Include an alternative path they were considering when it mirrors the audience’s current life. For example, a reader may relate more to “considering a startup role” than to a long list of past credentials.

Keep only details that move the story. A list of books read, awards, or past roles usually weakens a short post unless one detail explains the decision or stakes.

### 2. Trigger

Identify why the person acted at that moment. They may have wanted to test whether a field had room for their capabilities, find collaborators, solve a practical problem, change direction, or learn enough to make an informed decision.

### 3. Mechanism

Find one or two observable things that changed the trajectory. Strong mechanisms include:

- Realizing a field or role was accessible
- Finding a relevant opportunity through a community
- A conversation that clarified the next step
- Feedback that improved an application or project
- An introduction, workshop, or resource with a clear practical use

Avoid “the experience was transformative.” Say what happened.

### 4. Now-state

Record the current role, organization or team if approved, and what the person actually does. Translate specialist language enough for the intended reader to understand the work. One meaningful artifact can add credibility; avoid piling up resume details.

### 5. Timeline and compression

Map the sequence from joining or starting to the outcome. Use a short, truthful timeframe only if it sharpens the story, such as “within six months” or “the following year.” Do not force a compressed timeline when the facts do not support it.

### 6. Quotes

Pull three to five candidate quotes verbatim. Favor quotes that reflect the reader’s identity or blocker, not only the subject’s achievement. Light trimming is allowed only when it preserves the exact meaning and grammar.

Useful quote categories:

1. **Discovery:** “I did not know this path was open to someone like me.”
2. **Mechanism:** “I found the opportunity through the community.”
3. **Conviction:** “I would make the same choice again.”

## Generate three hook options

For feed-based platforms, the first two lines determine whether someone continues reading. Draft three distinct hooks before drafting the full post. Keep each to two short sentences, usually under about 140 characters total where that suits the platform.

### Hook A: Discovery

Use when the audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a concrete mechanism.

This is the best default when the first sentence can act as a mirror for the reader.

### Hook B: Identity collision

Use when the before-and-after contrast is vivid.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This is useful for broad audiences that may not share the subject’s precise uncertainty.

### Hook C: Stakes-led

Use only when a meaningful cost or risk is approved and the audience will read it as honest conviction rather than a warning.

**Formula:** The subject accepted a specific cost to do something. Now, they are doing a concrete piece of work or taking a meaningful action.

Do not use this hook if it suggests hardship is required to participate, or if it is weaker than an accessible discovery story.

Choose one recommended hook. Briefly state why it suits the audience and why the other two are less suitable. Default to Discovery when the reader likely has the same blocker as the subject.

## Draft the post

Aim for roughly 160 to 220 words unless the platform requires otherwise. Shorter is often stronger.

Use this sequence:

1. **Hook:** Use the recommended option.
2. **Before-state:** One short paragraph with the previous situation and a relatable alternative path.
3. **Name the intervention:** Explicitly say they joined the program, used the resource, or entered the community. Do not leave its role implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then state what happened in plain language.
5. **Current work:** Describe what they do now and why it matters in understandable terms.
6. **Optional honest cost:** Include only if approved and genuinely useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already present in the hook or body.
8. **CTA:** Address the reader directly and offer one clear next action.

A short outcome clause is often enough: “They applied and got in.” Use a three-sentence sequence only when it adds pace or clarity.

For platforms that may reduce distribution for external links in post text, choose an approved alternative location such as a first comment, profile destination, or campaign page. Do not present platform behavior as universal without current evidence.

## Style rules

Adapt to the chosen voice guide. If none exists, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use concrete names, dates, roles, figures, and titles only when verified and approved.
- Use the person’s first name after the first full introduction only if appropriate to the publication’s tone and consent.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Avoid unearned labels such as “brilliant,” “exceptional,” or “inspiring.”
- Use contractions if the voice is conversational.
- Keep the CTA in full second person: “If you are…” and “you can…”
- Avoid emojis unless they are an explicit brand choice.
- Prefer periods, commas, and line breaks over em dashes.

On the final pass, remove machine-like phrasing: empty transitions, dramatic setup frames, filler intensifiers, hedge words, abstract nouns replacing evidence, false balance, and reflective summaries after the CTA.

Avoid corporate or vague language such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm” unless needed in an approved direct quote.

Read the post aloud. If it sounds like generic thought leadership, shorten it and replace abstractions with facts.

## Graphic quote options

Provide three quote-card options. Each should be self-contained, under 15 words when possible, and taken verbatim from approved material.

Offer one quote in each category:

- Discovery
- Mechanism
- Conviction

Recommend one quote with a one-sentence rationale. Discovery quotes often work best because they stand alone and reflect the reader’s uncertainty. Choose a mechanism or conviction quote only when it is clearer and more memorable without context.

## Readiness audit

Before sending the post for review, check:

- Is every name, role, date, figure, and title verified?
- Were transcript-derived details cross-checked where needed?
- Does the post show a concrete mechanism rather than only a result?
- Does it avoid overstating causation?
- Is the intervention named clearly?
- Does the opening reflect a real audience concern?
- Is the current work understandable to a non-specialist reader?
- Have sensitive claims and direct quotes been flagged for approval?
- Is the CTA clear and directed at the intended reader?
- Are there no unsupported superlatives, corporate phrases, generic filler, or excessive em dashes?

## Delivery and iteration

Create the draft in the user’s chosen document system when one is available. Use a clear title format such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide:

- The recommended hook and the two alternatives
- The three graphic quote options and the recommendation
- Approval items requiring review
- Missing information that would strengthen the post
- The document location or link, if applicable

Treat the first draft as review-ready, not final. If feedback says “make the hook better,” generate genuinely new hooks rather than making minor edits. If asked to shorten the post, cut secondary biography first while preserving the mechanism and outcome. If a subject rejects a sensitive line, use the approved fallback without weakening the entire story.

After final approval, review feedback for reusable lessons only when a clear pattern emerges. Update future intake questions, style guidance, or verification checks when a recurring issue is observed. Do not invent process changes after a clean review cycle.


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
description: Close one month with evidence, then create and explicitly approve a small, capacity-checked plan for the next month.
---

# Review and plan a month

Use this workflow at a month boundary to review the period ending and create an executable plan for the month ahead. A full session usually takes 45–75 minutes: about half for evidence and review, and about half for planning.

Review and planning belong in one session. The structural cause of a missed commitment, energy drain, or delivery problem should directly shape the next month’s plan.

## Purpose

This workflow produces:

- An evidence-based account of what happened during the review period.
- A direct verdict on progress toward current commitments and longer-range goals.
- A compact picture of selected work, wellbeing, training, or personal-practice signals.
- A written **Review** for the month ending.
- A written **Plan** for the month beginning, with a memorable theme, no more than three major outcomes, explicit trade-offs, and a pre-mortem.

Only gather, discuss, or save information that serves one of these outputs. Do not turn a monthly review into a complete archive of the user’s life or work.

## When to run it

Run this workflow when the user asks for a monthly review, asks to plan a named month, or asks to close one month and start another.

Default range rules:

- On the first three days of a month, review the prior calendar month and plan the current month.
- Otherwise, review the current month to date and plan the next month. Label a partial review clearly and state the days remaining.
- If the user asks only for forward planning, review first because evidence should shape the plan. The user may explicitly choose to skip the review.

State the ranges before proceeding:

> Reviewing **March 2026** (01 Mar–31 Mar). Planning **April 2026**.

Ask whether the user means strict calendar months or a practical range that includes an overlapping partial week. Record the actual planning range in the plan.

## Privacy, access, and source rules

Use private records, communications, journals, health data, calendars, and work systems only for a legitimate planning purpose and with clear authorization from the person entitled to authorize access. Use the minimum relevant sources, fields, and date range.

Do not expose raw journal entries, unrelated messages, sensitive health details, or personal details about other people in summaries or saved records. Describe patterns without unnecessary quotations or identifying detail. Keep outputs within the user’s appropriate access boundary.

When using a helper or delegated process, provide only the access and information required for its narrow task. Ask for user-provided facts or exports when a source is unavailable. Never imply that an unavailable source was checked.

## Operating rules

1. **Read first; discuss second.** Show the evidence picture before asking reflective questions.
2. **Batch independent reads.** Gather independent evidence in one initial pass where the chosen system allows it. Do not interrupt the conversation with repeated small lookups.
3. **Use live commitments.** Assess against the user’s current agreed target, not an old schedule, abandoned scope, or stale goal record.
4. **Check data quality before a harsh verdict.** Missing syncs, delayed updates, and incomplete logs may distort results. Ask the user to confirm surprising findings.
5. **The user chooses.** The assistant calculates, summarizes, identifies gaps, and holds constraints. The user chooses priorities, cuts, and commitments.
6. **One decision at a time.** Do not advance planning until the current question has a real answer.
7. **Stay at month altitude.** Define outcomes, milestones, capacity, structure, and commitments. Leave week-by-week task blocks to a weekly planning process.
8. **No saved plan without explicit approval.** A draft assembled from notes is not a decision. The user must restate or materially confirm the theme and commitments, then explicitly approve the plan.
9. **Use explicit dates.** Use **DD MMM** unless the user chooses another unambiguous format.
10. **Keep records useful, not exhaustive.** Save decisions, evidence, constraints, and commitments rather than a conversation transcript.
11. **Do not lecture.** For training, health, recovery, or personal practice, give the numbers, direct conclusion, and agreed commitment. Give specialist advice only when requested and appropriate.

## Step 1: Determine the range and gather evidence

Determine the review month, comparison month, and planning month. Then perform one initial batch of reads where possible.

Use the user’s chosen system, such as a project tracker, task manager, calendar, spreadsheet, notes application, training log, health tracker, or a short user-provided inventory.

| Evidence area | Gather in the initial pass |
|---|---|
| Previous monthly record | Theme, promised outcomes, commitments, and prior review findings. |
| Weekly records | Plans and reviews in the review range; repeated blockers, milestones, and carried work. |
| Goals | Active weekly, monthly, quarterly, and annual goals; status, deadlines, and notes. |
| Work delivered | Completed tasks, decisions, projects, or deliverables, grouped into useful domains. |
| Calendar | Next-month travel, leave, deadlines, recurring commitments, and heavy meeting weeks. |
| Daily signals | User-selected ratings, focus time, habits, or brief journal themes. |
| Sleep and recovery | Optional sleep duration, sleep quality, and same-source recovery trends. |
| Training or practice | Optional sessions in the review and comparison months, plus the live commitment or schedule. |

For large sources, return computed statistics and a few representative themes rather than raw entries. Month-long journals and event lists can crowd out the review. Use filters, aggregation, or a narrowly briefed helper when available.

A calendar helper should analyze only the requested planning window and return a concise summary of:

- Fixed multi-day blocks, such as travel, leave, or conferences.
- Approximate meeting load by week.
- Important recurring commitments.
- Protected personal or social commitments.
- Anomalies, such as meetings within unavailable periods or likely time-zone errors.

Before detailed planning, re-read weekly plans overlapping the start of the planning range. Reference and reconcile their commitments with the month plan; never duplicate, replace, or silently conflict with the weekly plan.

## Step 2: Show the evidence picture

Present a compact factual picture before asking the user to explain it. Be direct, numeric where useful, and concise.

### Training, health, or personal-practice verdict

If the user has a current commitment in this area, include it unless they explicitly place it out of scope. Compare actual activity with the live target. Depending on the domain, calculate:

- Total volume, sessions, repetitions, or practice instances.
- Average weekly volume.
- Number of active days.
- Completion of key sessions or milestones.
- Longest gap between sessions.
- Relevant balance measures, such as easy versus demanding sessions, when records support them.
- Relevant performance or recovery measures.
- Month-over-month changes.

Use this taxonomy when it fits:

- **ON TRACK**: key measures meet at least 90% of target and consistency is intact.
- **BEHIND**: a key measure is about 60–90% of target, or there was a meaningful consistency break.
- **OFF TRACK**: a key measure is below 60% of target or there was a prolonged gap.
- **AT RISK**: an injury, safety concern, burnout signal, or sustained decline makes the plan unsafe or unlikely.

Adjust thresholds only when the domain needs different ones, and state the adjustment. If records may be incomplete, ask: “The record shows this. Does that match reality?” before making a strong judgment.

State one biggest corrective action for next month. This is a concrete commitment, not a full program.

### Goals and delivery

Summarize weekly commitments as completed, missed, deferred, or rolled forward. For every active long-range goal, state whether it **advanced**, **stalled**, or **regressed**, with one short reason. Explicitly name goals that received no meaningful attention; these are often most at risk.

Also summarize completed work in a few useful domains. Avoid a wall of bullets. The question is whether effort created intended progress.

### Life signals

Include only measures the user chooses to track. Useful measures include rating distribution and average, focus hours, low-focus days, sleep duration, sleep quality, recovery trends from a consistent source, and repeated themes in notes.

Flag meaningful patterns such as low average sleep, repeated short nights, several consecutive low-rating days, an extended low-focus streak, or a mismatch between positive ratings and written evidence of exhaustion or stress. Numerical averages are not complete truth; raise material mismatches directly.

## Step 3: Reflect on the month

Start with one specific observation grounded in the evidence. Ask one question at a time and follow no more than two or three threads unless the user wants depth.

Cover these questions before closing the review:

1. What genuinely shipped and feels like a win?
2. What cost more time or energy than it returned?
3. Was the main miss structural, circumstantial, or a genuine priority change?
4. What one behavior, boundary, or pattern must change next month?
5. If training or personal practice is in scope, what is the concrete next-month commitment?

Useful prompts:

- “This outcome slipped across several weeks. What made it structurally hard to complete?”
- “Your ratings were stable, but your notes repeatedly mention strain. What was happening?”
- “This goal moved while the others did not. What conditions made that possible?”

For a time-constrained user, the minimum viable review is: the in-scope practice verdict, any material wellbeing flags, one structural fix, and one concrete next-month commitment.

## Step 4: Plan the new month

A plan is not a description of events plus optimistic targets. A real plan has a defined outcome, an honest baseline, a path, proof of capacity, trade-offs, forcing functions, a pre-mortem, and explicit approval.

### Move 1: Define outcomes

For each candidate priority, ask:

> What specifically is true by the final day of this planning range?

Make the answer measurable or plainly verifiable. Limit the plan to three outcomes; one or two is usually better. Each outcome should connect to a long-range goal or explicitly chosen responsibility.

### Move 2: Establish current state

Size the gap with evidence, not mood. Inspect the relevant draft, pipeline, milestone, backlog, baseline metric, or other domain reality. If the gap cannot be described, gather the missing evidence before designing the path.

### Move 3: Work backward to build a path

For each outcome, identify three to six moves by reasoning backward from the due date. Every move needs a date or window, owner, and evidence of completion.

> For this to be true by the end date, what must be true halfway through? What must happen before that?

### Move 4: Do capacity math

Estimate usable focused capacity honestly:

> available working days × recently observed focused hours per day

Account for travel, leave, meeting-heavy weeks, fixed commitments, and recovery needs. Compare available capacity with the effort implied by the paths. If demand exceeds supply, cut, defer, reduce scope, or add real help now.

### Move 5: Make the NOT-doing list

Ask:

> What will explicitly not happen this month so these outcomes can?

The user names the cuts. A plan without genuine exclusions is a wish.

### Move 6: Add forcing functions and protective structure

Fragile outcomes need external pressure: a named reviewer expecting a deliverable on a date, a booked review, a public commitment, or a dependent team waiting on the work.

Protect work vulnerable to interruption. If one outcome requires long uninterrupted work while another tolerates fragmentation, batch flexible work around meetings and reserve the best available blocks for the fragile work. If calendar conflicts undermine protected time, add their removal to the plan as an immediate action.

### Move 7: Run a pre-mortem

Ask:

> It is the final day of the month and this plan failed. What happened?

The user answers first. Record the top two or three failure modes and a specific counter for each.

### Move 8: Get sign-off

Read the whole plan back in ten lines or fewer. The user must be able to state the theme and main outcomes from memory, then explicitly approve it.

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

At the end of every run, make one precise improvement to the reusable workflow, its templates, or its data mapping. Store it in the user’s chosen workflow document or improvement log. If no suitable location exists, present a short durable rule the user can save where they prefer.

Look for a noisy read, a wrong data assumption, a misleading metric, a user correction, or a repeatable pattern. Prefer one specific edit over a vague reminder.

## Audit checks

Before finishing, verify:

- Review and planning ranges are explicit.
- Evidence was shown before reflective prompts.
- Sources and details stayed within the authorized access boundary.
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
- Judging performance against stale targets.
- Treating incomplete tracking as complete reality.
- Confusing a list of events with a plan.
- Overloading capacity and refusing to cut scope.
- Letting the assistant choose priorities that the user has not chosen.
- Saving an unapproved draft.
- Duplicating or conflicting with weekly plans.
- Treating wellbeing averages as more truthful than repeated written evidence.
- Applying generic productivity rituals instead of fixing the actual drain.
- Overwriting an existing record without resolving the difference.
- Treating a brainstorm, imported task list, or request from another person as a confirmed commitment.
- Gathering more personal information than is necessary for the review.


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
description: A quiet, repeatable evening workflow that reduces stimulation, secures distractions, prepares basic needs, and offers a brief response for sleeplessness.
---

# Wind down for sleep

Use this as the last active part of the evening, after any day review or next-day planning routine. Its purpose is not to reflect, solve problems, or organize tomorrow. Its purpose is to make the transition from daytime activity to sleep reliable: reduce stimulation, remove easy distractions, complete a few practical tasks, and go directly to bed.

Use the full workflow when the user says they are winding down, ready for bed, going to bed, or wants help settling for sleep. If they say they cannot sleep, are still awake after trying to sleep, or are frustrated in bed, use only **Can’t-sleep fallback**. Do not restart the full ritual.

A typical active ritual takes about 20–30 minutes. If the user has named an earlier bedtime, work backward from that time. Protect time for the environment gate, essential preparation, and a brief settling practice; do not expand earlier review or planning into the remaining sleep window.

## Purpose and principles

Each step should do at least one of three things:

1. **Reduce stimulation:** lower bright light, screen use, novelty, active conversation, and problem-solving.
2. **Increase reliability:** make it harder to drift into scrolling, work, messages, or fresh decisions.
3. **Prepare the body and morning:** finish small practical actions that reduce avoidable friction after waking.

Consistency matters more than having an elaborate routine. Use roughly the same sequence most nights. If a step serves none of these purposes, remove or replace it.

The environment and distraction-control gate is the load-bearing part of the routine. Optional preparation can be shortened when the user is exhausted, but this gate should not be casually skipped.

## Interaction rules

- Keep prompts quiet, direct, and short. Do not use emojis, jokes, motivational coaching, or sleep-science explanations during the ritual.
- Give one small group of actions at a time. Do not create an extended bedtime conversation.
- For checklists, use plain bullets rather than Markdown checkboxes. End with: **Reply “done” when all set.**
- Once wind-down begins, do not ask about tomorrow’s goals, intentions, priorities, wins, or backup to-do lists. Do not offer substitute planning questions.
- Do not reopen reflection, journaling, planning, messages, task systems, or calendars during the ritual.
- If the user raises a worry, task, or work problem, do not solve it. Say: **“Put a brief note somewhere safe for tomorrow. Do not work on it tonight.”**
- If the user is very tired, allow them to skip the morning card or reduce the physical-preparation list. Preserve the environment gate unless a health, accessibility, caregiving, safety, or urgent on-call need makes it unsuitable.
- Do not summarize what was completed at the end. After the close message, stop.
- If the user says good night after the close, remain silent or reply only: **Good night.** Do not add a new prompt or simulate a follow-up turn.

## Readiness check

Establish only what is necessary before starting. Do not inspect inboxes, news, social feeds, task lists, private notes, or other stimulating sources merely to run a sleep routine.

If prior-session context, records, or calendars are available, use them only for a legitimate purpose and with clear authorization. Read the minimum needed, stay within the user’s access boundary, and omit unrelated or sensitive personal details. A completion signal is preferable to reading private freeform writing.

1. Determine whether the user’s normal day-review practice has already been completed, if a reliable completion signal is available.
2. If it was missed, offer the review once only when there is enough time for a useful short review without materially delaying sleep.
3. Optionally check the first fixed morning commitment only when authorized and needed to set morning access to a secured phone or other device.
4. Treat missed next-day planning as silent information. Do not mention it or offer to plan at bedtime.

If the day review was completed, say:

> Day closed. Starting wind-down.

If it was missed and there is enough time, say:

> The day review was missed. Do you want to do the short review first?

If the user declines, or it is too late for the review to be useful, say:

> Leave the review for tomorrow. Start winding down now.

If a review was skipped and a small concern appears later, capture only the minimum reminder in a designated next-day location. Do not create a partial journal entry or inspect private journal content merely to append a note.

## Step 1: Environment and distraction gate

Do not continue until the user confirms this step is complete.

Choose cues the user can repeat in their own home. Adapt them for sensory, mobility, medical, household, and safety needs. A useful default is:

> Before we start:
>
> - Change from day clothes into sleep clothes.
> - Reduce bright light; use low, warm lighting where possible.
> - Turn off overhead lights if practical.
> - Start quiet, familiar audio if it is helpful and not attention-demanding.
> - Put the phone in a charger outside reach or a physical barrier that prevents casual checking.
> - Set morning access for the phone or other secured device.
> - Limit any remaining device use to one necessary, low-stimulation device.
>
> Reply “done” when all set.

### Morning device access

Let the user choose a normal morning access time. If there is an early fixed commitment, make the device available earlier only when needed for preparation, travel, essential communication, or safety. State the reason briefly.

> Device access returns early enough for morning preparation and travel.

A physical barrier is often more dependable than a software setting alone. Its purpose is to interrupt automatic checking, not to punish the user.

If the user says they will dim the lights or secure the phone later, reply once:

> Do it now. This is the highest-leverage step. I’ll wait.

Do not negotiate the remaining routine while this gate is incomplete. No later step should depend on the phone.

## Step 2: Offline morning card

Offer a small physical card that makes the first part of the morning less dependent on a phone, notifications, or memory. Keep it short enough to read at a glance.

> Write a small morning card:
>
> 1. Hygiene
> 2. Medication or supplements, if applicable
> 3. Water and breakfast
> 4. Movement, rehabilitation, or another health practice
> 5. Shower and get dressed
> 6. Leave for the day or begin the first planned block
>
> Add any already-known practical exception. Card done?

If the user mentions an exception, tell them to write it in the appropriate place on the card. Do not create a digital version or turn the card into a planning exercise.

Skip this step when the user is very tired or already has a dependable offline morning cue.

## Step 3: Physical preparation

Use a compact list tailored to the user’s regular needs. Group actions by location where possible to reduce movement and decisions. A default list is:

> - Fill water for the morning.
> - Brush teeth and complete essential nighttime hygiene.
> - Prepare a simple breakfast or place needed items together.
> - Put out essential clothing, keys, mobility aids, or medication.
>
> Reply “done” when all set.

If a small missing item creates a worry, capture it in one designated place without solving it. For example: “Buy breakfast item.” Do not search for alternatives, open shopping tools, message anyone, or start planning. Say only:

> Noted. Captured for later.

## Step 4: Brief settling practice

Offer one familiar, low-stimulation practice. Do not teach a new or complex technique at bedtime.

Default prompt:

> 5 min meditation.

If meditation is not appropriate, use an accepted alternative such as gentle breathing, a brief body scan, quiet stretching, or a few pages of a paper book outside bed. Avoid screen-based guidance, emotionally engaging material, and performance-focused activities.

Wait for a simple completion response.

## Step 5: Close

After the settling practice, send only:

> Close the device. Go straight to bed—no detour.
>
> See you tomorrow.

This is the final user-facing message for the night.

## Can’t-sleep fallback

Use this only when the user reports wakefulness after attempting sleep. Do not rerun the ritual or reopen reflection, planning, device settings, or problem-solving.

Respond briefly:

> Get out of bed. Keep the room dim and do a boring, screen-free activity for about 20 minutes. Return to bed when sleepy. Do not check the time.

Suitable activities include reading on paper or another neutral, quiet task. Avoid work, screens, emotionally engaging reading, exercise, food preparation, and clock-checking. The aim is to keep the bed associated with sleep rather than wakeful frustration.

For recurring, severe, or safety-relevant sleep problems, encourage appropriate medical or sleep-care support.

## Routine audit and adaptation

Review the workflow only after the user has disengaged for sleep, and only if the review will not re-engage them. Change the routine based on observed friction, repeated failure, or clear user feedback. Do not invent changes after a clean run.

| Signal | Adaptation |
|---|---|
| A prompt is repeatedly misunderstood | Rewrite it in plainer language or remove ambiguity. |
| A distraction barrier is routinely bypassed | Choose a stronger physical, environmental, or account-level barrier with the user. |
| An item is consistently skipped and offers no benefit | Remove it or make it optional. |
| A practical worry repeatedly appears at bedtime | Move its prevention into an earlier review or planning routine. |
| A step increases alertness | Shorten it, simplify it, or move it earlier. |
| A data source reveals unnecessary private information | Reduce the read to a completion signal, use a designated capture location, or remove the integration. |

Preserve what reliably works. The best wind-down is usually quiet, repeatable, and boring enough to become a clear signal that the day is over.


---
name: plan-and-book-a-trip
description: Plan travel around its purpose, compare complete current journeys, and prepare or complete bookings within the traveler’s clear authorization.
---

# Plan and book a trip

Understand the trip before optimizing its transport. Establish what the traveler wants from the journey, compare a small set of complete and practical options, and carry the chosen option through preparation or an authorized booking. Current user instructions take priority over past preferences, previous itineraries, and old receipts. A fare, date, or choice from one trip is evidence for that trip, not a permanent default.

## Core principles

- Plan transport around the purpose of the trip, not around the first cheap fare found.
- Use private calendars, messages, records, and reservations only for a legitimate travel-planning purpose and with clear authorization. Search only the minimum relevant sources and omit unrelated or sensitive details from outputs.
- Ask the traveler about intentions, priorities, and trade-offs. Retrieve accessible factual details yourself rather than asking them to copy information from authorized systems.
- Separate confirmed facts, provisional plans, source-based inferences, and unknowns.
- Research current schedules, fares, products, and terms. Do not represent old information, an advertised “from” price, or a selected search result as a bookable option.
- Compare complete door-to-door journeys, not headline ticket prices alone.
- Do not purchase, change, cancel, upgrade, message a provider, or enroll in monitoring without authorization that covers that action.
- Do not promise future monitoring unless a real, authorized mechanism is running and can access the required information.

## 1. Understand the trip before searching transport

For a new trip, start with a focused discovery pass. Do not begin detailed fare searches, upgrade research, or booking preparation while important trip-shaping questions remain unanswered. The goal is to avoid letting an early flight or train search determine dates, destinations, or time with important people.

For a continuing conversation, use the existing trip brief and ask what has changed rather than restarting the entire interview. Follow an explicit request to skip discovery or conduct a narrowly specified check, such as checking whether a particular train is still available.

### Review relevant context responsibly

Read the conversation and materials the traveler supplied, such as invitations, agendas, accommodation details, existing itineraries, or event documents. If the traveler has authorized access to private sources, consult only sources that are relevant to this trip and only to the minimum extent needed.

Potentially relevant sources include:

- Calendars for commitments immediately before, during, and after the likely travel period.
- Travel correspondence for event timing, locations, companions, accommodation, existing bookings, or changing plans.
- Work communications where travel relates to a project, meeting, or event and the traveler has authorized that access.
- Event pages, shared itineraries, and planning documents that establish venues, agendas, or attendance requirements.

Do not conduct unrelated inbox sweeps, inspect private information about companions that is not needed for the trip, or contact other people without authorization. Keep findings within the appropriate planning and access boundary. If a needed source is unavailable, say so clearly; do not imply it was checked.

Extract and distinguish:

- Why the traveler is going and what a successful trip would accomplish.
- Event locations, start and end times, and whether they are confirmed or tentative.
- Essential and optional stops, companions, meetings, and local transport needs.
- Existing bookings, accommodation, work obligations, time off, and recovery needs.
- Commitments that set an earliest departure, required arrival time, or latest return.

An invitation is not necessarily a confirmed attendance plan. A calendar event is not automatically a hard constraint. An old receipt or loyalty status is not proof of a current benefit. Where sources conflict, reconcile them if possible and surface any uncertainty.

### Ask questions that shape the journey

After a short context pass, state what is known and ask a substantive, compact set of questions. Usually four to six questions in one numbered plain-text block works well. Ask fewer when most matters are settled. Do not turn the initial interview into a long booking-form interrogation or an upgrade sales discussion.

Use questions such as:

1. What is the purpose of this trip, and what would make it worthwhile?
2. Which events, visits, or places are essential, optional, or best done in a certain order?
3. What dates or arrival times are genuinely fixed, and what range is useful if dates are flexible?
4. How much time would you like in each place, including time with people, independent time, and recovery time?
5. Is this work, leisure, or both? Do you need to arrive rested, work en route, or preserve a quiet day before or after a key commitment?
6. What is already arranged for accommodation and local transport, and are there accessibility, reimbursement, spending, or other practical constraints?

Use known facts to ask better questions, but do not turn an inference into a settled preference. For example, an agenda may establish the event dates, but the traveler should still decide whether to arrive early, remain afterward, or add another stop.

Ask about transport preferences only when they are relevant and unknown. Useful examples include direct versus connecting services, preferred airports, cabin comfort, sleep requirements, luggage, seats, rail class, flexibility, and loyalty benefits. Treat these as explicit choices or qualified defaults, not universal rules.

Do not require a numerical budget if the traveler wants to see the trade-offs first. Establish whether the requested outcome is research, a booking-ready plan, or an authorized purchase.

### Agree a trip brief

Before detailed ticket research, summarize the working brief:

| Brief element | Working statement |
|---|---|
| Purpose | [Why the trip matters and desired outcome] |
| Stops and people | [Essential and optional locations, visits, or companions] |
| Dates | [Fixed dates, useful flexibility, and provisional items] |
| Pace and recovery | [Work, rest, sleep, and arrival-readiness needs] |
| Existing arrangements | [Accommodation, bookings, local support, or constraints] |
| Open decisions | [Questions that could materially change the transport plan] |

Give the traveler an opportunity to correct the brief. Clear answers can establish agreement without a separate approval ritual. However, wait for answers to unresolved choices that would materially alter the trip. Keep provisional dates visibly provisional throughout later research.

## 2. Research current transport options

Start this stage after the brief is sufficiently clear, or after the traveler explicitly asks for a limited transport check. Tie all searches to the brief. If the available transport would require a material change to the trip, return to the traveler with that choice rather than silently reshaping the itinerary.

### Search schedules and fares

Search current schedules and prices across the useful date range. Use route-discovery and fare-comparison tools to identify options, date grids, nearby airports, and combinations, but verify the selected itinerary with the operating provider whenever possible. A marketing carrier or reseller label does not establish who actually operates the journey or what product is included.

For flights:

- Start with nonstop options when that best matches the traveler’s time, reliability, or recovery needs. If none are suitable, consider feasible nearby airports and connections, but explain the trade-off before treating a connection as acceptable.
- List the useful departure times, not only the cheapest option, when timing affects jet lag, meeting readiness, or a same-day onward connection.
- Compare return and open-jaw tickets when arriving in one city and departing from another could reduce backtracking or recover useful time.
- Verify the actual operating carrier, aircraft where cabin configuration matters, fare family, and segment-by-segment cabin.

For rail and other ground transport:

- Search the actual travel date and named fare products, not a reseller’s generic “first class” or “premium” label.
- Verify the class, included services, exchange and refund rules, and any booking fee.
- Check whether discount cards, passes, memberships, or railcards are valid on the date, route, and fare type before counting a discount.
- Account for planned engineering works, holiday disruption, station-transfer time, border processes, and timetable-release limits.
- Confirm the intended station when place names are ambiguous, and research transport to the actual final destination rather than stopping at the nearest major airport or city.

For airport transfers, ferries, coaches, local rail, and other onward transport, assess the complete journey. A lower airfare may be poor value if it creates a costly transfer, an overnight hotel, an unreliable self-transfer, or the loss of a useful day.

### Label confidence and source quality

Every price and schedule should be labeled accurately:

| Label | Meaning |
|---|---|
| Live selected itinerary | A current, specific itinerary and fare seen in an active provider or reliable booking search. |
| Indicative date-grid price | A route-and-date signal that needs verification for the exact itinerary and fare. |
| Estimate | A reasoned approximation, not a currently verified bookable price. |

Record the check date and currency. Do not treat an advertised starting fare as proof that the required ticket can be bought. Use verified links for itineraries and important terms where links are appropriate.

If a tool, provider site, login, or checkout fails, attempt permitted safe recovery. State the failed source, the exact error where available, the information that remains unverified, and any replacement source used. Do not silently substitute a source or claim that a personal offer was checked when authentication prevented access.

### Compare the actual travel product

Compare what the traveler will really receive, not only branded labels.

- Verify whether “premium economy” is a distinct cabin or merely extra-legroom economy.
- For overnight travel, assess whether the aircraft or train actually provides the sleeping arrangement being considered. A cabin label alone does not guarantee a lie-flat seat, quiet berth, or expected service.
- Examine every segment of mixed-cabin itineraries. Business or another premium product on an overnight leg and a lower cabin on a daytime return may be a better fit than upgrading every segment.
- Check the preferred seat type, seat availability, and any selection charge. A preference does not guarantee assignment.
- Verify cabin-bag allowance, size, and weight limits for the specific fare. A personal-item-only fare may not meet the traveler’s needs.
- Include required extras, such as seat selection, bags, transfers, and booking fees, in the comparison.
- Read material change, cancellation, refund, and missed-service terms. Do not assume a higher cabin is flexible or refundable.

### Evaluate jet lag and arrival readiness

For travel across several time zones, rank options by arrival readiness as well as cost and cabin. Ask about the traveler’s usual sleep pattern if it is not known. Consider when they will sleep, arrive, see daylight, and face their first important obligation.

As a general approach:

- For eastbound overnight travel, favor options that allow sleep during the traveler’s biological night and support a manageable first day after arrival.
- For westbound travel, daytime services that arrive in daylight and leave a short path to local bedtime can be easier to adapt to.
- When a work event follows shortly after arrival, give greater weight to reliable sleep, a realistic buffer, and a low-friction onward journey.
- Suggest a practical pre-trip sleep adjustment and a first-days light, meal, and bedtime plan when the time shift is substantial.

Do not present these principles as medical guarantees. The traveler’s health needs, tolerance for schedule changes, and work demands may outweigh a generic jet-lag preference.

### Evaluate upgrades without assumptions

When an upgrade is relevant, compare:

1. Buying the desired cabin outright.
2. Changing an existing ticket into that cabin at the current fare difference.
3. Buying a separate cash, points, or loyalty-program upgrade, if available.

Compare the complete cost before booking. For an existing ticket, compare the additional price and conditions then in effect. Do not assume an earlier upgrade payment applies to a future fare change.

Separate a confirmed upgraded seat from a waitlist or request that may not clear. An open seat map is not proof that an award upgrade is available. If sleep or readiness is important, recommend a confirmed option the traveler would accept. Book a lower cabin only if they would be content remaining in it.

Verify fare-family eligibility, loyalty benefits, upgrade priority, point-plus-cash conditions, and cancellation or refund rules before recommending an upgrade strategy. Do not claim that a particular time before departure is reliably cheapest. Prices can rise, seats can sell out, and preferred seats can disappear.

For points comparisons, state any value assumption used. A flexible base ticket does not necessarily make a cash upgrade or points request flexible.

If authorized authenticated access is available, inspect reservation-specific upgrade offers and alternative change prices without submitting a change or purchase. Public fares do not prove what an existing reservation offers. If access is blocked, continue the independent comparison work and request only the smallest user action needed.

## 3. Compare complete journeys

Present two or three useful choices and lead with a recommendation. If only one route meets the brief, say so rather than inventing alternatives.

Show local dates and times, airports or stations, total journey duration, time-zone changes, and next-day arrivals explicitly. Build realistic buffers for check-in, security, immigration, luggage, border controls, station gates, terminal changes, and travel across a city. Allow more contingency during holidays, disruptions, or unfamiliar transfers.

Distinguish protected connections from independently booked tickets. State who bears the risk if an earlier service is delayed. Consider a longer connection or overnight stop when it protects an important event, especially if suitable accommodation is already available.

Use a comparison like this:

| Option | Dates and complete route | Product and fare | Complete cost | Why choose it | Main drawback |
|---|---|---|---|---|---|
| Recommended | [Local dates, route, duration, and transfer] | [Actual cabin/class on each segment and key flexibility] | [Currency; ticket, required extras, and transfers] | [Best fit for time, comfort, reliability, or price] | [Relevant trade-off] |
| Value option | [Route and timing] | [Actual product] | [Currency and inclusions] | [Lower cost or simpler booking] | [Lost comfort, time, or flexibility] |
| Flexibility option | [Route and timing] | [Actual product] | [Currency and inclusions] | [Better change terms or recovery margin] | [Higher price or less ideal timing] |

Explain what extra spending buys: time, sleep, lower connection risk, better seat availability, meaningful flexibility, or a more convenient arrival. Show different currencies separately, or state the conversion rate and date if converting. Do not add unlike currencies into an unexplained total.

## 4. Prepare and complete the booking

Lead the booking recommendation with the chosen dates and route, the practical reason it fits, live price-check timing, verified booking links where available, unresolved facts, and the decision still needed.

Complete research and prepare a concrete, reviewable booking before asking for an approval that is actually required. A request to find or compare transport is not authorization to pay. If the traveler has already authorized a specific purchase or given a clear scope and spending limit that covers the selected option, proceed within that authorization without asking again merely because checkout is next.

Before submitting an authorized purchase, verify:

- Traveler name exactly as supplied for travel documents.
- Dates, local times, airports, stations, and routing.
- Operating provider and whether the itinerary is nonstop, connected, protected, or self-transferred.
- Cabin or class and fare product on every segment.
- Selected seat, whether it is actually assigned, and any fee.
- Luggage allowance and required extras.
- Total price, currency, payment timing, and material terms.
- Any missing identity, eligibility, or payment detail that must be supplied by the traveler.

Do not invent passport information, loyalty numbers, payment details, eligibility facts, or accessibility needs. Resolve a material mismatch before purchase.

After purchase, verify success through the provider’s confirmation rather than a search page or incomplete checkout. Report the booked journey, total paid, assigned and unassigned seats, and any remaining onward transport or action. Keep booking references, receipts, identity details, payment data, and other sensitive records in the appropriate private trip record, not in a reusable planning document or broad shareable summary.

## 5. Monitor and improve when appropriate

Monitoring is optional and must be explicit. If the traveler requests recurring fare or upgrade checks, use a real, authorized monitoring capability and verify that it can access the relevant itinerary. Establish what is monitored, the trigger for notifying the traveler, the timeframe, and whether the monitor can only alert or can take action.

Monitoring does not authorize a purchase, ticket change, bid, or repricing. Do not enable automated purchases unless the traveler has clearly authorized the exact action, scope, and price limit. Stop monitoring after departure, a completed change, or a revised plan. If scheduling, access, or authentication is unavailable, state that monitoring is not running.

During active use, apply corrections to the current trip immediately. When the traveler has authorized preference retention, save clear and lasting preferences with their relevant qualifications, such as “for overnight work travel” or “when dates are uncertain.” Replace superseded preferences rather than accumulating contradictions.

Keep one-off fares, dates, upgrade outcomes, individual booking references, and tentative choices in the private trip record. Do not turn a single cheap fare into a permanent budget, a successful upgrade into a reliable rule, or a completed booking into proof of satisfaction.

Learn from verified feedback about comfort, connection timing, arrival readiness, and booking friction. Ask a short follow-up only when it resolves an important uncertainty. Preserve reusable lessons without retaining unnecessary personal details, credentials, or incident histories. Learning never creates additional authorization to access accounts, contact people, or spend money.


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
description: Review meeting records, identify unfinished commitments, create clear deduplicated follow-up tasks, and batch only questions that need judgment.
---

# Capture meeting actions

Turn meeting records into reliable post-meeting follow-up tasks. Use this as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose and operating rules

Use meeting records only for a legitimate work purpose and with clear authorization to access the relevant meetings, recordings, transcripts, notes, and task system. Review only the minimum sources needed to establish commitments. Keep unrelated personal, sensitive, or confidential details out of tasks, questions, reports, and reusable guidance. Respect the access boundaries and consent expectations that apply to the meeting record.

Before each run, use these outcomes:

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

Apply documented responsibility and delegation boundaries supplied by the user or organization. Attendance at a meeting does not make the user accountable for all work in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this broadly useful default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect:

- Title, date, and time
- Meeting-record link or identifier
- Attendees, if available and relevant
- Transcript, notes, summary, and necessary linked context

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

When a transcript is unavailable, treat ownership as lower confidence. Use reliable written notes where available; otherwise ask a focused question rather than inventing an action.

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
- Source and related links that the task audience is authorized to access

Create no task when work was completed live, another person owns it, the meeting was purely informational and any needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

## 4. Decide the task shape

Combine actions into one task when they have the same counterparty, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect months later.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

Use this readiness gate before creation. Each proposed task must have:

1. A clear owner.
2. Evidence of an unfinished outcome.
3. A specific, independently understandable finish line.
4. A sensible due date or timing rule.
5. Enough context to be useful later without exposing unnecessary sensitive detail.

If any of these are missing, either skip the item or add it to the batched questions.

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

Do not raise priority merely because capture happened late. Raise it only when there is a real deadline, a material risk, or a counterparty awaiting a time-sensitive response.

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

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. Skip the new task, or update the existing task if the meeting adds a meaningful action, deadline, or context. Do not copy sensitive meeting detail into an existing task unless that task’s audience is authorized for it.

Record the duplicate decision so it can be reported clearly.

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

Do not include unnecessary attendee details, sensitive content, or quotations in the question. Wait for answers before creating uncertain tasks. After answers arrive, create or update the remaining tasks and rerun any necessary duplicate check if the answer changed the task outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, capture lessons that genuinely improve future runs. Keep this separate from the meeting task itself.

- Add a short, generalized example or note to a reusable meeting-archetype reference when a recurring pattern affects triage, such as a common attribution error, reliable sign of in-meeting completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new delegation boundary in the user’s or organization’s maintained responsibility reference when it applies beyond one meeting and doing so is authorized.

Do not turn one-off facts, personal preferences, or sensitive relationship details into permanent rules. Small additions to an examples or patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing steps or changing the evidence order. Briefly report any reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links only to source records accessible to its intended audience.
- Message drafts are ready to send and follow the user’s preferences.
- Outputs contain only the minimum relevant personal or confidential information.
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
description: Create or improve a short, paid, asynchronous work sample that produces role-relevant evidence, is practical to score, and is validated through simulations.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A strong work sample asks candidates to do a realistic, bounded version of the job, produces evidence that is difficult to imitate with generic answers, and can be reviewed consistently without imposing unreasonable unpaid labor.

Use this workflow for a new work sample or for revising an existing one. Do not use it for interview questions, application-form screeners, live exercises, or multi-day work trials. If the request could refer to one of these formats, ask which format is intended before proceeding.

## Purpose and design principles

A work sample usually sits after initial screening and before later interviews. It should answer a narrow hiring question: can the candidate demonstrate the most important parts of this role under realistic constraints?

A useful exercise does not try to assess every quality needed for employment. Different stages can provide different evidence:

- Interviews can assess live communication, motivation, collaboration, and verbal reasoning.
- References can assess sustained reliability, integrity, and past working relationships.
- A later work trial can assess judgment and consistency over days or weeks.
- Onboarding can teach organization-specific tools, workflows, and vocabulary when these are not essential at entry.

The work sample should focus on a small number of load-bearing capabilities that are important to the role and observable in a short exercise. Examples include prioritization, practical judgment, clear writing, problem diagnosis, sourcing, execution, systems thinking, audience awareness, or turning ambiguity into useful work.

Use these default constraints unless the hiring owner chooses otherwise:

- Make the exercise paid. State payment clearly, including timing and payment method.
- Set a clear expected effort limit, commonly two to four hours.
- Use a realistic but fictionalized, anonymized, or approved public scenario.
- Do not ask candidates to create work the organization will use commercially or operationally unless that use is separately agreed and appropriately compensated.
- Design for roughly 20 to 25 minutes of reviewer time per submission.
- Make the task self-contained. Candidates should not need internal systems, private information, credentials, or access to unavailable people.
- State what use of AI tools is permitted. Evaluate judgment and usefulness rather than attempting to infer AI use from writing style.
- Assess only capabilities materially related to the role. Do not use protected characteristics, personal background, or unrelated proxies as criteria.
- Offer a route for reasonable accommodations or an accessible equivalent format while keeping the role-relevant standard intact.

If the hiring team accesses private communications, records, or work history while preparing the exercise, it must have a legitimate hiring purpose and clear authorization. Use the minimum relevant materials, omit unrelated or sensitive personal details, respect consent and privacy expectations, and keep drafts and outputs inside the approved hiring access boundary.

## Step 1: Pre-flight

Before designing a work sample, confirm that the hiring team has both of these inputs:

1. A current job description or role brief covering responsibilities, expected outcomes, seniority, and reporting context.
2. A role-success profile, hiring plan, or equivalent document identifying the capabilities and evidence associated with success in the role.

If either input is missing, stop. Do not try to define the ideal role profile while designing the exercise. That creates a moving target and often produces a plausible-looking task that measures the wrong things.

Use this request format:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

Once both inputs exist, read the relevant role context. This can include linked project notes, team constraints, examples of expected outputs, known operational risks, prior hiring feedback, and existing work samples for comparable roles. Use only materials that the hiring team is authorized to access for this purpose.

Read one or two reference exercises to calibrate tone, length, and delivery format. Do not copy their task shape automatically. A task that works for operations may be unsuitable for research, leadership, partnerships, or specialist roles.

Give a concise status update after review, for example:

> Read the role brief, success profile, and two comparable exercises. Moving to the alignment memo.

## Step 2: Write the alignment memo before drafting

Do not draft candidate-facing instructions yet. First create a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five capabilities the role succeeds or fails on that can genuinely be surfaced within the exercise window. Phrase them as observable performance, not broad virtues.

Weak: “Strategic thinking.”

Better: “Can identify the highest-leverage problem in a messy operating situation, explain the tradeoff, and deliver a useful first action.”

### What the exercise will not test

Name important criteria that should be assessed elsewhere. This keeps the exercise honest and prevents it from becoming an unrealistic proxy for the entire job.

For example, a three-hour asynchronous exercise may not fairly test long-term reliability, leadership over months, responsiveness in live meetings, specialized software fluency, or performance within a particular internal system.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level. Explain what this changes:

- Entry-level candidates may need more context and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make tradeoffs, establish direction, and create work another person can use without additional explanation.

### Failure modes to catch

Identify two or three plausible patterns of role-misaligned performance that could otherwise look strong in ordinary screening. Describe observable work patterns, not personal types or identity-based labels.

Examples include:

- A polished planner who does not produce usable work.
- A fast executor who misses the central problem or creates avoidable risk.
- A careful candidate who defers every meaningful decision.
- A technically capable candidate whose output does not fit the intended audience.

### What strong looks like

Write one short paragraph describing a top submission. Focus on evidence: what it notices, which choices it makes, what it produces, how it handles uncertainty, and how it uses the limited time.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the owner confirms or revises the memo.

## Step 3: Propose exercise shapes

Once the alignment memo is approved, propose three possible task shapes. Each option must test the agreed capabilities in a distinct way, be understandable within about a minute, be self-contained, and be practical to score quickly.

For each option, provide:

- **Shape:** A plain-language description of the task.
- **What it tests:** The specific load-bearing capabilities it reveals.
- **Why it is evaluable:** What evidence reviewers will see and why scoring can be consistent.
- **Main risk:** The most likely way the format could create noise, unfairness, or weak signal.

Keep each option concise. Common shapes include:

- **Triage pile:** The candidate receives a realistic collection of messages, requests, and constraints. They prioritize, draft responses or work products, and recommend one systemic improvement. This can fit operations, coordination, support, and communication-heavy roles.
- **Choose the highest-leverage action and ship it:** The candidate receives a brief with several possible priorities, selects one, explains the choice, and produces a small usable output. This can fit strategic operations and builder roles.
- **Diagnose and fix:** The candidate reviews a messy situation, identifies the key problem, and ships one targeted intervention. This can fit product, program, analytical, and process-improvement roles.
- **Source and pitch:** The candidate defines a target profile, identifies promising channels or prospects from supplied information, and drafts outreach. This can fit recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** The candidate assesses a defined question using supplied evidence and makes a recommendation for a decision-maker. This can fit research, policy, strategy, and specialist knowledge roles.
- **Design a repeatable system:** The candidate creates a lightweight process, playbook, or operating artifact that another person could use. This can fit program, enablement, community, and operational design roles.

Do not draft the full exercise until the hiring owner chooses a shape. If none fit, propose three additional shapes based on the approved capabilities rather than forcing a familiar format.

## Step 4: Draft version 1

Write the candidate-facing exercise in this order.

## [Role] Work Sample

Open with one or two sentences explaining the capabilities the exercise assesses. State the total expected time.

**Your mission**

Describe a specific situation, not an abstract assignment. Include enough context to make the work realistic. If decisiveness is a capability being tested, state which stakeholders are unavailable during the exercise so candidates must make reasonable assumptions rather than deferring every decision.

End with one sentence restating what the candidate will produce.

**Deliverables**

List two to four substantive parts, with rough time guidance where helpful. A common operations structure is:

- A short prioritization or analysis section.
- Several actual drafts, decisions, or shipped outputs.
- One systemic fix, process improvement, or reusable artifact.

Avoid excessive micro-tasks. A few meaningful outputs provide better evidence than dozens of shallow decisions. If planning and execution both matter, tell candidates not to spend all their time planning.

**Context**

Provide the minimum information needed to complete the task: project state, audience, constraints, available resources, relevant policy, and stakeholder availability. Use fictional names, domains, and identifiers unless the hiring owner has approved public information for use.

For a triage-pile exercise, include roughly eight to ten realistic items. Make some items connected so candidates are rewarded for seeing patterns across the whole situation. Include reference notes containing data needed for fair decisions, such as escalation rules, capacity limits, service standards, or refund policy.

**Instructions**

Include:

- The expected time limit.
- A clear submission deadline.
- Submission format, such as one document or PDF, plus links to supplementary artifacts where necessary.
- Payment amount, payment process, and any early-submission bonus, if offered.
- Permitted tools and AI assistance.
- A request to document important assumptions briefly.
- Permission to submit incomplete work if time runs out.
- A contact route for accommodation requests or accessibility questions.
- Optional guidance on a short walkthrough video, only if it adds relevant evidence.

Use a transparent AI policy, such as:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

**Anticipated questions**

Include answers to common questions:

- If a requirement is unclear, make a reasonable assumption and state it briefly.
- If you do not finish within the expected time, submit what you have and note what you would do next.
- The work will be used only to evaluate candidates unless another use is agreed separately.

After every draft, add a separate section that is not for candidates:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets on choices the owner may want to change. Typical notes include whether a scenario item is too obvious, whether the context feels realistic, whether payment matches the time and role level, whether a deliverable is too prescriptive, or whether a walkthrough video should remain optional.

End with one focused decision question, such as: “Which part should we tighten first?”

## Candidate-facing format and writing checks

Write in direct, plain language. Use the locale and spelling conventions appropriate to the hiring organization and candidate audience. Format the exercise for the destination system selected by the hiring team.

Before sharing a draft, check that the candidate-facing text:

- Uses simple headings and bullets.
- Contains no tables if the destination system renders tables poorly.
- Avoids horizontal divider lines if they break the destination editor.
- Avoids generic AI-sounding slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.
- Uses complete, clear deadline phrasing, such as “by the end of Tuesday.”
- Uses clearly fictional email addresses and names in fictional scenarios.
- Formats multi-line message metadata clearly. If the destination editor collapses line breaks, use its supported soft-break method.
- Contains no credentials, private contact information, confidential business details, or sensitive personal data.

## Step 5: Iterate with the hiring owner

Expect multiple rounds of revision. For each round, provide the complete updated work sample, not only a change list, so it can be copied directly into the selected hiring system or document.

Apply feedback directly unless it would materially undermine validity, fairness, accessibility, privacy, or safety. If it would, state the concern once in plain language, offer an alternative, and let the accountable hiring owner decide.

Common revisions include tightening vague instructions, loosening overly prescriptive tasks, correcting scenario facts, simplifying deliverables, changing payment, and replacing unrealistic details.

## Step 6: Simulate two candidates

Before declaring version 1 complete, simulate two full submissions in parallel using the exact candidate-facing instructions.

### Role-aligned simulation

Use a persona that matches the approved role-success profile. Have them complete the actual deliverables within the stated time limit. Ask for a short reflection on their choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest, capable candidate who could pass ordinary screening but whose submission lacks one role-critical capability. Choose a mismatch tied to work evidence, such as a planner where the role needs a builder, a cautious candidate where the role needs decisive judgment, or an executor who does not recognize systemic patterns. Never tie this simulation to identity, background, or protected characteristics.

Have this persona produce the same submission shape.

Then synthesize the results:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both candidates performed similarly.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by likely impact.

Floor checks that both simulated candidates pass are not automatically bad. The concern is when a central capability fails to produce meaningfully different evidence.

## Step 7: Apply validation improvements

Revise the full exercise based on the simulation. Target the weakest diagnostic points first. Useful improvements may include:

- Making scenario items more interdependent.
- Removing obvious noise that takes seconds to dismiss.
- Adding a concrete constraint that forces a meaningful tradeoff.
- Replacing a broad opinion prompt with a usable deliverable.
- Clarifying reviewer criteria so scoring rewards the intended behavior.
- Removing specialized knowledge requirements that are trainable and not essential on day one.

Do not make the task harder merely to make it more selective. Make it more diagnostic of the agreed role-relevant capabilities.

## Step 8: Optional external review

If other reviewers provide feedback, assess each suggestion against the approved alignment memo. State which suggestions to integrate, which to skip, and why. External feedback is evidence, not an automatic instruction. The hiring owner remains accountable for the assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The role description and role-success profile are confirmed.
- The alignment memo is approved.
- The chosen task shape maps directly to the load-bearing capabilities.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and does not require private access.
- Payment, submission, AI-use, and accommodation instructions are clear.
- Candidate-facing text is formatted for the chosen destination system.
- A reviewer can score a submission in about 20 to 25 minutes.
- A role-aligned and plausible role-misaligned simulation has been completed.
- The simulation led to any necessary revisions.
- The final version contains no sensitive data and does not create unpaid production work.
- Role-relevant criteria, accessibility needs, privacy boundaries, and potential proxy bias have been checked.

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
- Using real private situations or communications when a fictionalized scenario would provide the same evidence.
- Declaring success without testing whether the exercise distinguishes the role-relevant performance it was designed to measure.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, accessible, appropriately compensated, useful for assessment, and clear about what good performance looks like.


---
name: run-a-reference-call
description: Prepare, conduct, and document a role-relevant hiring reference call using authorized evidence, targeted questions, and an auditable decision record.
---

# Run a reference call

Use this workflow to prepare and document a hiring reference call for a candidate. The goal is not to collect general praise. It is to gather specific, role-relevant evidence that helps the hiring team assess capabilities, working conditions, development needs, and unresolved questions.

Use only for a legitimate hiring purpose and with clear authorization to contact the referee. Access only the minimum relevant hiring records, communications, and scheduling information. Keep notes within the hiring team’s approved access boundary. Do not include unrelated personal details, sensitive information, rumors, or information the referee is not reasonably entitled to share.

## Inputs and readiness gate

Collect or confirm:

- Candidate name and the role under consideration.
- Referee name, contact details, organization, and relationship to the candidate.
- Call date, time, joining details, and attendees.
- Candidate consent or another appropriate basis for the reference check, according to applicable policy.
- The candidate’s stage in the process and the decision this call should inform.
- The hiring team’s role-relevant open questions.

Do not present a reference as independent evidence if the referee has limited direct observation, a material conflict, or an unclear relationship to the candidate. Record those limitations instead.

| Readiness check | Minimum standard |
|---|---|
| Authorization | The organization may contact this referee for the stated hiring purpose. |
| Role clarity | The expected outcomes and relevant capabilities for the role are known. |
| Call context | The referee’s relationship, timing, and contact route are confirmed or explicitly unknown. |

If the role, referee relationship, or authorization is unclear, resolve it before the call where possible. If the call must proceed, state the gap in the call record and limit conclusions accordingly.

## 1. Locate and confirm the call

Check the organization’s approved calendar or scheduling system for an event matching the referee’s name or contact details. Record the meeting title, time, attendees, joining instructions, and relevant scheduling context. If there is no event, create or update the approved scheduling record using the available information.

Create a reference-call record in the organization’s chosen hiring or meeting system before the call. Use a consistent title such as:

`[Date] — [Referee] ([Candidate] reference)`

Set the date, add the authorized interviewer and necessary attendees, and attach or link the call details. The record—not an informal chat summary—is the deliverable.

## 2. Gather context with minimum necessary access

Review approved sources that can answer the following questions:

1. **Hiring context:** What role is the candidate pursuing? What stage are they in? What decision or concern should this reference help resolve?
2. **Introduction and relationship:** How was the referee identified? Did they manage, collaborate with, teach, advise, or receive work from the candidate? When and how closely did they work together?
3. **Referee background:** What is the referee’s role and relevant professional context? Have authorized team members or the organization interacted with them before?
4. **Candidate record:** Collect links to the candidate’s approved application, professional profile, portfolio, or work samples only when useful to the interviewer.
5. **Other completed references:** Read approved records for the same candidate. Extract evidence themes, contradictions, development areas, and questions to test. Do not copy unnecessary private detail.

Use organization-approved search tools and records. Search direct correspondence, relevant internal discussions, prior meetings, the hiring record, and publicly available professional information only as appropriate. Prefer direct evidence over speculation. For email or message searches, review enough recent results to understand context, rather than relying on a single snippet.

## 3. Write the pre-call brief

Keep the brief concise, skimmable, and inside the approved record. Use this structure:

```markdown
## Context
- [Referee] — [role, organization, relevant background or profile link].
- Worked with [Candidate] as [relationship] during [period], with [degree of direct observation].
- Reference call for [Candidate], under consideration for [Role] at [organization]. Current stage: [stage / next decision].
- Candidate links: [application], [professional profile], [portfolio or work samples].
- Other known references: [names and relationships, if necessary for coordination].

## Opening
> Thank you for making time. I am speaking with references as part of our hiring process for [Candidate]’s [Role] application. I would value candid, work-focused examples. We will use what you share only for this hiring process and within the appropriate team.

## Briefing notes
- [Completed reference: source/relationship] reported [specific theme]. Ask whether [this referee] observed the same, and request an example.
- This referee is especially positioned to assess [capability or work context].
- Open question: [neutral, role-relevant question to test].
- Limit: [what this referee is unlikely to know].

## Questions
- [Questions and role-specific probes]
```

Briefing notes are the highest-value part of preparation. Write direct actions, not vague prompts. For example: “A previous manager described strong early project momentum but uneven follow-through. Ask for a project with a difficult final phase and what the candidate did.” If this is the first completed reference, identify what later calls should validate, such as ownership, feedback response, execution reliability, or collaboration.

## 4. Tailor questions to the role

Start with shared core questions:

- How did you work together, in what roles, and how closely did you observe the candidate’s work?
- What did the candidate personally own or deliver? What was the outcome?
- What is their most distinctive strength? Please give an example.
- Where did they need the most support, coaching, or structure?
- If performance in a new role went poorly after several months, what would be the most plausible work-related reason?
- If performance went well, what development area should their manager prioritize?
- Compared with relevant peers you have worked with, how would you describe their performance, and on what basis?
- What management approach, environment, or scope would help them contribute effectively?
- What important question have I not asked?

Follow broad claims with: “What did that look like?” “What was the candidate’s specific contribution?” “What happened next?” and “How often did you observe that?”

Add three to five probes tied to the role’s actual outcomes. Examples:

- **Operations or program work:** handling ambiguity, building repeatable systems, stakeholder communication, proactive problem finding, prioritization.
- **Community work:** relationship building, conflict handling, participation systems, judgment with difficult situations, identifying member needs.
- **Senior operations leadership:** scaling processes, balancing speed and controls, managing competing stakeholders, financial or vendor stewardship, recovering when infrastructure fails.

These probes assess relevant performance; they are not personality tests. Avoid questions about protected characteristics, family status, health, private beliefs, or other non-job-related matters.

## 5. Conduct the call fairly

Open by confirming the referee’s relationship and direct observation. Explain the hiring purpose and confidentiality boundary without promising secrecy beyond the organization’s actual policy. Invite candid, work-focused feedback.

Ask neutral questions. Do not disclose private interview judgments or lead the referee toward a negative conclusion. When testing a concern, frame it as an observable capability: “How did they manage changing priorities?” rather than “We heard they struggle with change; is that true?”

Distinguish evidence quality while listening:

| Record as | Example |
|---|---|
| Observation | “I saw them run the weekly planning process for six months.” |
| Referee interpretation | “I considered them unusually reliable under pressure.” |
| Your inference | “This may support the role’s need for independent execution; confidence is moderate.” |

Do not force a ranking if the referee lacks a meaningful comparison group. Ask what the comparison is and record it.

## 6. Document immediately after the call

Complete the approved reference-call record with concise notes. If an approved transcription or meeting-notes capability is used, ensure it is permitted, disclosed where required, and reviewed for accuracy. Do not treat an automated summary as a substitute for judgment.

Add:

- Date, participants, relationship, and observation limits.
- Specific examples, outcomes, and relevant quotes or close paraphrases.
- Strengths, development areas, and conditions that supported or hindered performance.
- Answers to each key hiring question.
- Agreements and contradictions with other evidence.
- Your confidence level and the reason for it.
- Recommended follow-up, if any.

## 7. Audit before using the reference

Before sharing conclusions, check:

- Does the record contain examples rather than only adjectives?
- Is each conclusion clearly separated from the referee’s statements?
- Did the call assess role-relevant capabilities and role alignment?
- Were prior-reference themes tested fairly rather than used to seek confirmation?
- Are sensitive or unrelated details omitted?
- Are limitations in the referee’s knowledge explicit?
- Is access restricted to authorized decision-makers?

A reference call informs a decision; it should not become the sole verdict. Weigh it alongside work samples, interviews, structured assessments, and other evidence according to relevance, directness, and consistency.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive method, protecting account context, verifying page state, and separating preparation from commitment.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing rendered forms, changing account settings, collecting data from dynamic pages, testing a user flow, or working in an authenticated dashboard. Use it when a supported direct interface, static-page request, or ordinary data retrieval cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not perform a consequential final action until the account, target, page state, and authorization are clear.

A browser automation command succeeding does **not** prove that a website accepted the change. Modern web applications may maintain internal state separately from the DOM, commit data only after focus leaves a field, replace controls during a re-render, or display an error even when an action succeeded.

## 1. Confirm purpose, authorization, and scope

Before accessing a browser session, determine the legitimate purpose of the task and the authority to perform it. This is especially important for authenticated dashboards, private communications, records about people, payments, account administration, and external submissions.

Establish:

- The requested outcome and exact target page, record, form, setting, or workflow.
- The correct account, organization, environment, and audience.
- The minimum information needed to complete the request.
- Whether the task accesses private data and whether that access is authorized.
- Whether the task changes data, sends information, grants access, spends money, or creates another external commitment.
- Which choices require the user's judgment rather than inference.

Use only the minimum relevant sources and information. Do not copy unrelated personal details into logs, screenshots, notes, or final output. Keep findings and artifacts within the appropriate access boundary. Do not reveal credentials, session tokens, recovery information, private messages, or security settings.

If the target, account, scope, or authority is unclear, stop and ask before changing data. Do not use browser automation to bypass access controls, consent boundaries, security warnings, or anti-abuse protections.

## 2. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can perform the requested task. It is usually more reliable than reproducing a browser interaction.
2. **Isolated headless browser automation.** Use this for public pages, testing, ordinary rendered-page extraction, screenshots, and forms that do not need an established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing session, account-specific dashboard, single sign-on state, or a user-directed browser context.

Before driving a browser, check for a direct route. Review official documentation, normal form actions, page source, and visible network activity for supported endpoints. Many forms submit structured data to an authorized service that can be used more reliably than the rendered UI.

Do not reverse-engineer or invoke private endpoints merely to evade restrictions or obtain data the requester is not authorized to access. If a site blocks automated browsing, do not try to evade its protections for routine research or collection. A verified visible session can be appropriate only when the user explicitly asked to complete a legitimate task on that site and the existing session is necessary.

Choose a robust automation capability for complex work. A lightweight interactive browser tool may be suitable for a few short reads or clicks. For long text, heavy client-side rendering, repeated form interactions, screenshots, or systematic verification, use a stable browser automation library or equivalent scripting environment. Do not continue trying to rescue an unstable automation session; restart with a more suitable method.

## 3. Protect browser and account context

An authenticated browser is not interchangeable with an anonymous automation context. Before acting in one, explicitly classify the intended context, such as personal, work, testing, staging, or production.

Follow these rules:

- Announce when taking control of a visible browser and state the purpose.
- Use a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Select the browser profile or connection associated with the intended context; do not rely on a generic browser selector or a window title.
- Confirm the signed-in account with a reliable account indicator before opening or changing the real target.
- Confirm the environment and target object before a data-changing action.
- Do not interrupt existing user work or close browser windows unless explicitly authorized.
- Do not disable security controls, multi-factor authentication, browser warnings, signature checks, or access restrictions to make automation easier.

If the automation system has a profile-verification gate, permission marker, or similar guardrail, enable it **only after** the account check has actually passed. Never create a verification marker in advance merely to unlock actions.

Use this preflight question before any meaningful change:

> Which account is active? Which environment is active? What exact item will change?

If any answer is uncertain, resolve it before proceeding.

## 4. Separate preparation from commitment

Identify whether the final step is reversible. Filling fields, drafting text, selecting options, and collecting a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, changing access, or applying account settings may not be.

Use two phases for consequential tasks:

1. **Preparation pass:** Fill or configure the page, verify all values, and capture a pre-action record. Do not activate the final control.
2. **Commitment pass:** Confirm that authorization covers the final action, re-check the account, target, and readiness gate, then perform the action once.

An explicit request to review before submission always requires review. If the user has already clearly authorized a specific reversible or final action, do not repeatedly ask for the same approval. If authorization for a consequential final action is missing, prepare and verify the result, present a concise pre-submit summary, and ask only for that action.

Treat the following as one-way actions unless the user clearly authorizes them after review:

- Sending messages, invitations, or notifications.
- Publishing content or submitting externally reviewed forms.
- Making a payment, purchase, or booking.
- Deleting records or files.
- Changing subscriptions, billing, ownership, access, security, or plan settings.
- Any action labeled permanent, final, irreversible, or impossible to edit later.

For an irreversible action, capture a screenshot or structured state record before activation. Include target, key values, recipients or audience, cost if any, and irreversible effects in the confirmation request.

## 5. Inspect the rendered page before editing

Do not begin by guessing selectors, filling fields by numeric position, or trusting a visual approximation. First inspect the rendered page and identify the actual interactive controls.

For every relevant control, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether the field is required.
- Validation rules, formatting behavior, character limits, and disabled state.
- Whether an apparent field is the real editor, a wrapper, or a hidden synchronization element.
- Whether a dropdown, checkbox, date, or tab selection causes a page re-render.

Address controls by stable semantic identity, such as visible label text, accessible name, or label relationship. Do not address fields by DOM index when a semantic identifier exists; dynamic pages can change element order during hydration and re-rendering.

Before changing a record or setting, inspect its current state. This prevents editing the wrong item or unintentionally overwriting existing data.

### Generic inspection pattern

Use the selected browser automation capability to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

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

## 6. Use the interaction method that matches the control

A generic “set value” operation is not reliable for all controls. Use normal user-like interaction for framework-managed controls, then read the state back.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use normal text entry or a standard fill operation | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select existing text, enter text with keyboard-style events, then blur | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, and wait for state to settle | Selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed | A click can toggle an already-correct value. |
| Date/time picker | Choose the values, close the popover safely, and verify the displayed summary | Typing or closing a popover can clear or reinterpret values. |
| File upload | Confirm file, destination, and privacy implications first | Uploading may begin immediately and may be difficult to undo. |

For a framework-driven editor, a robust general sequence is:

1. Focus the actual editable element.
2. Select existing content.
3. Delete it.
4. Enter the new text through keyboard-style events.
5. Move focus to a neutral page element to commit the edit.
6. Wait briefly for state to settle.
7. Read the result back.

Some forms pair a visible editor with a hidden input. Editing the hidden input can appear successful in a DOM dump while server-side validation treats the real field as empty. Target the control the user interacts with and that the application actually reads. If an accessibility locator returns an empty wrapper, inspect the labeled descendants and locate the real editable control.

If selecting a dropdown, checkbox, date, tab, or category can refresh the form, make and verify those selections **before** filling lengthy text. Re-inspect afterward and confirm earlier entries remain present.

## 7. Verify every meaningful edit

After each field is filled or setting is changed, read its value back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare lengths, required state, or a minimal redacted summary instead of copying full content into logs.

Check for common mismatches:

- The automation layer reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displayed text but did not retain it internally.
- A later action erased an earlier field after a re-render.
- A hidden synchronization field was changed instead of the visible editor.
- A selection changed a dependent field, date, recipient, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once with a more suitable interaction method, and verify again. If the page still rejects or changes the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 8. Run a pre-submit readiness gate

Before a final submission or high-impact change, inspect the full relevant state again. Confirm all of the following:

- The correct account, organization, environment, and target are active.
- Every required field is present and non-empty.
- Each entered value matches the intended content closely enough for the task.
- Dropdowns, checkboxes, dates, recipients, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially filled form is recoverable; an incorrect external action may not be.

Capture a pre-action screenshot, concise state summary, or structured field dump when useful. Store and share it only through an appropriate access boundary. Avoid exposing sensitive form values in a large inline table when a short summary and securely available record are sufficient.

### Readiness checklist

- [ ] The account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 9. Verify completion without blind retries

A button click is not proof of success. After acting, look for reliable evidence: a success message, confirmation reference, newly created record, persisted setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate messages, requests, payments, bookings, or records.

If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Do not represent an attempted action as completed.

## 10. Common failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after editing a later one | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control that the application actually reads. |
| Automation becomes unstable on a complex page | The selected automation layer is unsuitable | Restart with a more robust browser method or supported direct interface. |
| Headless and normal browsers behave differently | The site varies by browser context | Prefer an authorized direct interface; if necessary, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior | Close it through a neutral page action and re-verify affected fields. |
| A visible error may be cosmetic | The task may already have completed | Inspect resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
- [ ] Explicit confirmation was obtained immediately before any unapproved consequential final action.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: Design, test, refine, evaluate, and package reusable AI skills with realistic reviews, measurable checks, safe access boundaries, and accurate activation rules.
---

# Create an AI skill

Use this workflow to design a reusable AI skill, improve an existing skill, evaluate whether it helps, and refine when it activates. A skill is a focused set of instructions, with optional supporting resources, that helps an AI perform a recurring job reliably.

The standard loop is:

1. Understand the job, intended users, boundaries, and approved access.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review representative outputs with the user and measure objective requirements where appropriate.
5. Improve the skill based on evidence rather than isolated preferences.
6. Repeat until it is useful, reliable, and not narrowly fitted to its test examples.
7. Optionally improve the description that determines when the skill is used.
8. Package and hand off the finished skill.

Adapt the depth of this process to the user’s goal. A user may want a quick collaborative draft rather than a benchmark. Another may need careful comparison before relying on a skill for important recurring work. First identify where the user is in the loop, then help them take the next useful step.

## Communication principles

Match the user’s technical familiarity. Use plain language by default. Terms such as *evaluation* and *benchmark* are often understandable, but define them briefly when useful. Do not use terms such as “JSON,” “assertion,” “schema,” or “baseline” without explanation unless the user clearly works with them already.

Explain why a question matters. For example:

> What should a successful result look like: a chat response, a structured report, a file, or a proposed action? This determines how completion can be checked.

Keep the user involved at meaningful decision points:

- Confirm the intended job before writing a large instruction set.
- Ask before adding a restrictive scope, required capability, or approval requirement.
- Share proposed test cases before treating them as authoritative.
- Let human judgment lead when quality is subjective, such as tone, visual design, creative value, or strategic usefulness.
- Make uncertainty visible rather than silently choosing a high-impact interpretation.

## 1. Identify the starting point

Determine which situation best fits.

### New skill

The user has an idea for recurring work, such as preparing structured summaries or checking files before release. Begin with discovery and a first draft.

### Existing skill

The user has instructions that need editing, simplification, testing, or improvement. Read the current skill before proposing changes. Preserve its established name and identity unless the user asks to rename it. If the installed copy may be read-only, make an editable copy in a user-approved working location before changing it.

### Workflow demonstrated in the conversation

The user may ask to turn a demonstrated process into a skill. Extract what is already known before asking repeated questions:

- Inputs and approved sources used.
- The sequence of decisions and actions.
- Tools or capabilities involved.
- Corrections and preferences the user expressed.
- Output form and acceptance criteria.
- Conditions that caused the process to change direction.

Summarize the inferred workflow and identify gaps for the user to confirm. Do not convert a one-time workaround into a general rule without checking that it is reusable.

### Evaluation or activation request

The user may have a finished-looking skill and want to know whether it works or whether it activates appropriately. Go directly to test design, evaluation, and evidence-based revision. Do not rewrite a useful skill merely because a rewrite is possible.

## 2. Capture intent, scope, and authorization

Gather enough information to define one coherent job. Do not ask every question mechanically; begin with the unknowns that would most change the design.

1. **Purpose:** What should the AI accomplish?
2. **Trigger:** What requests, wording, or situations should cause this skill to be used?
3. **Inputs:** What information, files, systems, examples, or permissions may it use?
4. **Outputs:** What should it produce, change, or recommend? Is a specific format needed?
5. **Success:** How will the user know the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask, pause, decline, or return work to the user?
7. **Variation:** What normal alternatives, difficult cases, and exceptions matter?
8. **Dependencies:** Does it need a particular capability, template, reference, or script?
9. **Testing:** Should it be tested with representative requests before release?

Offer clear choices where useful:

- Should the skill make a best effort when data is incomplete, or stop and ask?
- Should the output be concise, detailed, or user-selectable?
- Should it work with any source, or only explicitly approved sources?
- Should it draft an external action or require approval before taking it?

### Privacy and access boundary

A skill may need to inspect records, messages, documents, or information about people. In that case, require a legitimate purpose and clear authorization before accessing them. Use only the minimum relevant sources and information. Do not include unrelated personal details in prompts, test data, logs, examples, or outputs.

Respect consent, confidentiality expectations, and the access boundary of the user’s role. If authorization, purpose, or source scope is unclear, ask a focused question before proceeding. Design the skill to summarize, aggregate, or redact sensitive information when that meets the task’s need better than reproducing raw material.

Do not design a skill to conceal actions, bypass authorization, obtain data outside the user’s access boundary, or expose confidential material. If a request cannot be safely completed, explain the limitation and offer a safe alternative where possible.

### Research before drafting

If approved documentation, comparable skills, templates, or domain guidance are available, review them before drafting. Research should reduce burden on the user, not replace their authority over requirements.

Use research to find:

- Existing conventions and required output standards.
- Constraints imposed by available capabilities or file formats.
- Reusable approaches for comparable work.
- Applicable safety, privacy, compliance, or approval expectations.

If evidence conflicts or a requirement is uncertain, report that uncertainty rather than inventing a rule.

## 3. Choose a structure and supporting resources

Keep a skill focused enough that both users and AI systems can predict what it does. A skill can support variations of one job, but unrelated jobs should normally be separate when they have different users, permissions, sources of truth, or completion criteria.

A portable package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed documentation
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test prompts and grading material
```

Use progressive disclosure:

1. **Metadata:** A short name and description used to decide whether the skill applies.
2. **Core instructions:** The normal workflow loaded when the skill applies.
3. **Supporting resources:** Detailed references, templates, or scripts consulted only when needed.

Keep the core instructions readable. When they become too large, move specialized guidance into clearly named reference files and state exactly when each file should be consulted. Give lengthy references a navigation section. For a skill supporting several platforms or domains, keep one shared workflow and separate variant-specific guidance so the AI loads only the relevant material.

### When to bundle a script

If several test runs independently reconstruct the same helper procedure, consider bundling it. Scripts are especially valuable for deterministic work such as conversion, validation, calculations, file generation, or repetitive cleanup.

Bundle a script only when it is reusable, within the intended permission boundary, and easier to verify than repeated natural-language steps. Document what it does, its inputs and outputs, expected failure behavior, and when not to use it. Do not add automation merely because it is possible.

## 4. Write the skill

Draft in clear imperative language. Explain the reason behind important instructions, especially when a rule prevents a predictable failure. A capable AI can adapt better when it understands the quality, usability, safety, or authorization goal behind a step.

A useful skill commonly includes the following sections.

### Purpose and scope

State the job, intended context, and boundaries. Clarify whether the skill creates a response, produces a file, makes a recommendation, performs an action, or guides the user through a process.

### Inputs and prerequisites

List required information, permitted sources, needed capabilities, and optional inputs. State what happens when a required item is absent.

```markdown
Before preparing the requested output, confirm the relevant period, scope, and approved source.
If a required source is unavailable, ask for an approved substitute or provide a draft clearly marked as incomplete.
```

### Workflow

Describe the normal sequence and its decision points rather than trying to list every possible edge case.

1. Inspect the request and available inputs.
2. Ask for clarification only when it materially changes the work or its risk.
3. Gather evidence from approved sources.
4. Perform the task using the appropriate method.
5. Check the result against the requested format and success criteria.
6. Present the result, key assumptions, and unresolved limitations.

Use conditional instructions where they help:

```markdown
If the user provides an approved template, follow it.
If no template is provided, use the default structure below.
If an action could overwrite, publish, send, or otherwise materially affect work, explain the impact and request confirmation first.
```

### Output format

When consistency matters, define an exact or near-exact structure.

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or required follow-up]
```

Do not impose rigid formatting where adapting to the user’s situation is more valuable. For those tasks, define the outcome and quality standard, then include a small generalized example only if it teaches a distinct pattern.

### Quality, safety, and failure behavior

State checks needed before completion: required fields, validated calculations, evidence for important claims, preservation of original data, clear uncertainty labels, or approval before sensitive actions.

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or reference:** Say what could not be verified and offer a safe alternate path.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, report the issue, or request guidance.
- **High-impact action:** Pause for confirmation before irreversible, external, or consequential actions.
- **Unauthorized or unsafe request:** Do not bypass access controls, conceal actions, expose sensitive information, or perform harmful work.

## 5. Write a strong skill description

The description is a routing instruction. It should state both what the skill does and when it should be used. Cover realistic phrasing, including requests that imply the task without naming it.

A good description includes:

- The outcome or job.
- Common contexts and phrases that signal relevance.
- Important scope limits that prevent costly false activation.

Example pattern:

```text
Produce structured summaries from approved source material. Use when a user asks for a concise update, a review of progress, key risks, open questions, or next actions, including when they describe the need without using the word “summary.”
```

Do not put the whole procedure in the description. Do not use vague descriptions such as “help with documents.” Also avoid making it so broad that it captures adjacent work that another skill should handle.

## 6. Review before testing

Read the draft as a new user would. Check:

- Is the job clear, coherent, and bounded?
- Does the description say when to activate it?
- Are inputs, permissions, and outputs clear?
- Does the workflow explain important checks?
- Does it handle missing information and unavailable capabilities?
- Is it free of unnecessary rules, repeated guidance, and brittle wording?
- Does it avoid personal defaults, hidden access assumptions, and undeclared dependencies?
- Does it preserve enough flexibility for normal variation?

Prefer a lean instruction set over a long list of rules that do not change outcomes. Excessive absolute language is a warning sign unless the behavior is genuinely non-negotiable, such as respecting authorization or preventing destructive actions.

## 7. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic requests and show them to the user for review. Add more only when they cover meaningful variation.

For each case, record a descriptive name, prompt, inputs, expected outcome, and objective checks where suitable. A portable record can look like this:

```json
{
  "skill_name": "example-skill",
  "evals": [
    {
      "id": "incomplete-input-handling",
      "prompt": "Create the requested structured output from the supplied material and clearly flag anything that cannot be verified.",
      "expected_output": "A useful structured result that distinguishes supported information from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover distinct situations such as a typical request, incomplete input, a format-sensitive request, an edge case that changes the workflow, and an approval-sensitive action when relevant. Vary wording and detail level. Avoid retaining personal, confidential, or unnecessary sensitive material in test cases.

## 8. Run comparisons and collect evidence

When the environment supports independent runs, compare the skill against a meaningful baseline:

- For a new skill, run each test with the skill and without it.
- For an existing skill, preserve an unchanged snapshot before editing and compare the revised version with that snapshot or another clearly identified prior version.

Run both conditions under comparable settings. If parallel execution is available, start all skill and baseline runs together. Store each iteration, test case, configuration, inputs, outputs, and available metadata in a clear directory structure.

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

Record elapsed time and resource-use information as soon as the execution environment reports it, because some systems do not preserve it. Keep inputs and outputs within the appropriate access boundary; do not copy confidential source material into broadly accessible evaluation locations.

If independent runs are unavailable, perform a transparent sanity check: apply the skill to each prompt, save the results, and ask the user to inspect them. Do not present this as a rigorous baseline comparison.

## 9. Define, grade, and analyze checks

While tests run, draft objective checks when they genuinely measure user value. Explain them before treating them as the definition of success.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A produced file opens and includes required fields.
- A calculation matches a known result within an agreed tolerance.
- Missing mandatory inputs are identified.
- Required citations or source references appear.

Use a stable grading record with a check, pass/fail result, and evidence:

```json
{
  "expectations": [
    {
      "text": "Identifies required information that is unavailable.",
      "passed": true,
      "evidence": "The output separates unsupported items from the completed result and requests the missing input."
    }
  ]
}
```

Use programmatic checks when practical. They are more repeatable than visual judgment and can be reused in later iterations. Do not force numerical checks onto subjective quality; usefulness, tone, aesthetics, and judgment need human review.

Aggregate pass rates, time, resource use, and variation where possible. Then look beyond averages:

- Checks that pass in every condition may not distinguish the skill’s value.
- Large variation may reveal unclear instructions or environmental instability.
- Higher quality may come with an unacceptable time or resource cost.
- Several failures may share one cause, such as unclear source selection.
- Execution traces may reveal redundant planning or research.
- Repeated helper construction may justify a bundled script or template.

## 10. Review with the user and improve

Present outputs alongside measurements using an available review interface or accessible files. For each test, show the prompt, relevant inputs, outputs from each condition, objective grades with evidence, and available timing or resource data. Give the user a simple way to provide feedback.

Ask focused questions:

- Which result would you trust in routine use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add work or detail that was not valuable?
- Would this work with different wording or data?

Generalize from feedback rather than encoding one test example into the prompt. Fix the underlying cause with the smallest change likely to work. Keep instructions lean, explain intent, preserve valued behavior, and add reusable resources only when evidence justifies them.

After revision, rerun the full relevant test set in a new iteration and compare it with the same baseline policy. Stop when the user is satisfied, requirements are reliably met, feedback is consistently positive, further revisions do not create meaningful improvement, or the remaining issue requires a product decision or unavailable capability.

## 11. Optional blind comparison and trigger optimization

For a consequential choice between two versions, give an independent evaluator two outputs without revealing which version produced each one. Have it judge against a shared rubric such as correctness, completeness, clarity, constraint adherence, safety, and practical usability. Reveal the source only after recording the judgment.

Once the workflow itself is stable, test the description’s activation behavior. Create a balanced set of realistic requests that should activate the skill and difficult near-misses that should not. Review the set with the user. Use substantive prompts: simple one-step requests may not activate a specialized skill even if its description matches.

For positive cases, vary formality, wording, implied versus explicit requests, and common versus less common valid uses. For negative cases, use close alternatives that share vocabulary but belong to another job. Avoid obviously irrelevant negatives because they do not test routing quality.

If the environment can evaluate candidate descriptions repeatedly, separate improvement examples from held-out examples. Choose the description that performs best on held-out requests, not merely the one that fits the examples used during editing. Show the user the old description, new description, and results before applying it.

## 12. Package, audit, and hand off

Package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name and description are clear and stable.
- The instructions accurately describe scope and activation conditions.
- Required capabilities, references, and scripts are present and documented.
- No private paths, credentials, confidential records, personal data, or undeclared local conventions remain.
- Scripts behave predictably and stay within intended authorization boundaries.
- Test material is retained only when safe and useful.
- A new user can install or adapt the package in their chosen environment.

Provide a short handoff note describing what the skill does, required capabilities, known limitations, and a simple way to test it after installation.

## Final readiness gate

A skill is ready when it has a clear job, accurate activation guidance, instructions that handle normal variation, explicit boundaries for uncertainty and permission-sensitive work, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.


---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using realistic content, screenshots, and layout checks.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it to small edits too: a spacing, background, or sizing change can alter wrapping, overflow, alignment, page height, or visible backgrounds at other viewport sizes.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Treat real screenshots and programmatic checks as complementary evidence: each catches defects the other can miss.

## 1. Prepare realistic test states

Run the real interface in an authorized test environment. Populate the affected surfaces with representative content before testing:

- long paragraphs, formatted text, long labels, and long field values;
- representative cards, lists, rows, and realistic item counts;
- validation messages and other content that changes component height;
- loading, empty, and error states when the change can affect them.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping, and unintended blank space.

## 2. Select the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages, dashboards, or interfaces expected to be used on large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short height of about 700 px;
- a tall height of about 1400 px or more.

Include the actual target viewport when known. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment. Tall windows can reveal trailing blank areas and incorrect minimum-height behavior that ordinary screenshots do not show.

Use a repeatable headless browser automation capability selected for the project. Capture screenshots from the rendered interface, not from a design approximation or geometry output.

## 3. Capture and inspect screenshots

Capture screenshots for every relevant viewport and state. Use both forms when appropriate:

- **Visible-viewport screenshots** for fixed, sticky, viewport-height, and bottom-alignment behavior.
- **Full-page screenshots** for page length, section transitions, and long-content behavior.

Inspect the changed component and its surrounding layout on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does it now match the design intent, considering the component's new role?

Pay special attention to edge-to-edge or full-bleed changes. When a formerly contained component becomes flush with a viewport edge, leftover margins or wrapper padding may become visible as unwanted background strips. Check all edges, not only the edge changed in code.

Reread the requested outcome after making the change and compare it directly with the screenshots. Do not accept a result merely because the stylesheet appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshot inspection. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the design is intended to fit the viewport;
- no changed element overlaps neighboring content, its container, or important fixed UI;
- buttons, links, and fields remain visible and operable;
- cards, lists, and form controls remain within intended bounds;
- fixed or sticky UI does not conceal essential content;
- body text retains a readable line length.

For a fit-to-viewport surface, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant element bounding rectangles with adjacent elements and container boundaries. Check the actual elements that can collide rather than assuming a generic page-level test can detect every relationship.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line; reading-focused layouts commonly target roughly 60–70 characters per line.

## 5. Require both forms of evidence

A viewport passes only when both of these pass:

1. **Visual evidence:** screenshots show no exposed background strips, poor spacing, unexpected empty regions, clipping, or visual imbalance.
2. **Programmatic evidence:** relevant overflow, bounds, overlap, and usability checks pass.

Measurements can miss visible design defects. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions. Neither replaces the other.

## 6. Fix failures and rerun

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a size-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the viewport where the defect appeared.

If a fix makes one viewport correct but introduces a failure at another, step back and reassess the layout model. The diagnosis is incomplete; do not accumulate patches until screenshots happen to look acceptable.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” State which widths, heights, states, and checks were completed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If a viewport or state remains unverified, say so clearly. Do not represent the UI change as complete until every relevant sweep result has passed.


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

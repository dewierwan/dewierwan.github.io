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
description: Find the weak points in a leading strategic idea before committing: strengthen the case, test its critical assumptions through sequential challenge, and finish with a verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor that matches its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes defending it.
- If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Move to a decision using the existing findings.
- If reviewing internal communications, records, or feedback about people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant material, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask **one forcing question at a time**. Wait for an answer, evaluate it, and challenge vague, unsupported, or evasive answers before proceeding.
- Use available evidence: metrics, research, prior experiments, customer feedback, documented decisions, and authorized stakeholder input. Distinguish facts, inferences, and forecasts.
- Refer to relevant dissenters by role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- If a section is irrelevant, say `Skipping — N/A because [reason]`.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving its intended meaning. Include the action, mechanism, expected outcome, timeframe, and key conditions.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If this strengthened version changes the intended claim, get confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold. Rank them by damage if wrong, starting with the one most likely to undermine the decision.

| Rank | Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|---|
| [1] | [State the assumption] | [Choose one] | [Evidence or lack of it] | [Low/medium/high] | [Test or disproof method] |

Make assumptions observable. Replace “users will value this” with a behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, selected for the highest-risk assumptions. Do not present them as a full questionnaire. Adapt each next question to the prior answer.

Use these categories as needed:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would happen in the next 30 or 90 days that would show this is wrong?
- **Counterfactual:** What similar effort failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this works, what does the situation look like in 12 months? What could success itself break?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that view been heard directly?
- **Reversibility:** If wrong, what does unwinding require in time, money, commitments, trust, or disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specifics. “I think it will work” is not evidence; ask for observed behavior, comparative data, a credible commitment, or a relevant test result.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6–12 months. Name the three most likely failure modes, ordered by likelihood or impact. Include an early warning sign that appears soon enough to change course.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Mechanism] | [Observable signal] | [Check and accountable role] |

## 5. Surface credible dissent

Identify two or three roles with a credible basis to disagree. State each role’s strongest likely objection. If their perspective has not been sought, mark it as an evidence gap. Silence is not agreement.

## 6. Define what would change the decision

Require one sentence:

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test incomplete or failed rather than approving it.

## 7. Give a verdict and handoff

Choose one outcome:

- **GREEN — proceed to decision.** Core assumptions have credible support, dissent is addressed, reversal costs are understood, and warning signs have an owner or review point. Next: document and make the decision. For hard-to-reverse or organization-defining choices, schedule a review.
- **AMBER — test first.** One or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible test, such as a small interview set, expert review, prototype, or short data collection period. Next: run that test, then decide with the result recorded.
- **RED — stop, redesign, or reopen options.** A core assumption is weak, downside is unacceptable, or no meaningful falsification criterion exists. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with **exactly one** concrete next action: a verb, an owner, and a deadline when useful.

`Example: Research owner: interview five target users this week and compare findings against the adoption assumption.`

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

Common failures are skipping alternatives, asking all questions at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and issuing a positive verdict without falsifiable criteria or monitoring.


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
5. **Record only with permission.** “Should we do X?” asks for analysis, not for a record. Create or update a decision record only when the user asks to log, track, open, or commit it, or explicitly agrees to recording it.
6. **Protect privacy and access boundaries.** Before accessing shared communications, personnel records, customer data, or a shared decision register, confirm a legitimate purpose and clear authorization. Use the minimum relevant sources and information. Do not include unrelated sensitive details.
7. **Do not deliberate indefinitely.** Once the appropriate rigor and readiness gates are satisfied, name the decision, assign the next action, and move forward.

If an organization uses a shared decision register, confirm that its audience is appropriate before writing to it. For sensitive topics such as health, relationships, compensation, or confidential personnel matters, offer a private record or keep the discussion in chat.

## 1. Choose the mode

Determine whether this is a new or existing decision.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review date and has not yet received an outcome assessment.

If the user explicitly names the mode, follow that instruction. Otherwise, if authorized, search the available decision register for overlapping decisions before creating a duplicate.

For a resume, retrieve the existing record and append new information rather than overwriting history. For a review, use the original prediction and reasoning as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Write the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What is the deadline or decision trigger?
- What result is desired?
- What happens if no action is taken?

If the question is broad and no credible options exist yet, generate options before evaluating them. Do not pressure-test a vague problem statement.

If there is only one viable path, say so directly: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time when needed. Put the choice in one bucket.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, consult relevant stakeholders |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and named prerequisite conversations |

Use this test if classification is unclear: **What would it cost to unwind this?** Consider money, time, trust, operational disruption, opportunity cost, legal exposure, and reputational effects. If the cost cannot be stated quickly or is materially uncertain, the decision is probably larger than it first appears.

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. Do not create a record by default.

If the user is stalling, name the cost of delay: continued attention may cost more than an imperfect choice. Do not use this shortcut when the decision affects safety, legal obligations, confidential information, or another high-impact concern.

### Reversible

In a short working session:

1. List two or three realistic options.
2. For each option, state one major strength, one major weakness, and a rough effort or cost estimate.
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

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies tradeoffs rather than disguising judgment.

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence in its favor.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.
- The next fact, test, or conversation most likely to change the call.

Keep these categories distinct:

- **User’s stated view:** Only positions the user actually expressed.
- **Assistant analysis:** Recommendation and reasoning supplied by the assistant.
- **Open question:** Uncertainty not yet resolved.
- **External input:** Relevant evidence or a stakeholder’s view, attributed accurately and minimally.

If the user has not expressed a position, write “No position stated yet” or leave the user-position field blank. Never invent a lean, confidence level, rationale, response to dissent, or final choice for them.

When using private records or communications, obtain only information relevant to the decision. Do not infer personal motives, expose sensitive details, or transfer information into a record visible to people who should not receive it.

## 6. Commit and record

Before finalizing, run this readiness check:

- Is the decision question clear?
- Are the realistic alternatives known?
- Is the scope classification appropriate?
- Has the required challenge or consultation occurred, or has the user explicitly documented an override?
- Is the decision-maker’s own choice clearly distinguished from assistant advice?
- Is there an owner, next action, and decision or review trigger?
- Is the chosen record location appropriate for the sensitivity and audience?

For meaningful decisions, confirm:

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

Use the user’s chosen decision register, document system, or private file. A useful record contains status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar, task system, or another reminder mechanism for high-stakes reviews when authorized.

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

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until the user commits. When resuming, append a new dated thinking-log entry rather than rewriting history.

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not collapse a bad outcome into a bad decision process, or a good outcome into a sound process.

If the result is still too early to assess, retain the original record, state what evidence is still missing, and set a new review trigger.

## 8. Completion audit and message

Before closing the work, check that the output does not:

- Attribute an unstated opinion, confidence, or decision to the user.
- Treat assistant advice as the user’s conclusion.
- Reveal unnecessary personal, personnel, customer, or confidential information.
- Create a record without permission.
- Bypass a required pressure test or stakeholder gate without documenting the user’s reason.
- Mistake a task, preference, or brainstorming prompt for a committed decision.

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

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the solution is not already clear. Do not use it for a small fix or routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for an explicit decision.

## 1. Understand the problem

Start with the underlying problem, not the user's proposed solution. If they ask to build a particular thing, work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is it?
- What outcome would materially improve the situation?
- What constraints, permissions, security expectations, or compatibility requirements apply?

Write a concise problem statement and descriptive requirements. Describe the outcome and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so clearly.

Ask only for information that cannot be obtained from authorized, relevant documentation, code, systems, or prior project context. When reviewing private communications or records, confirm a legitimate purpose and clear authorization, use the minimum relevant information, and omit unrelated or sensitive personal details from notes and outputs.

## 2. Decide whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Treat “do nothing,” “deprioritize,” or “improve the current workaround” as real options.

Distinguish between:

- **Reversible decisions:** Small choices that are easy to change. Make a reasonable choice and proceed.
- **Hard-to-reverse decisions:** Persistent data changes, migrations, public interfaces, long-lived settings, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the impact warrants it.

If direction or priority is unclear, present the tradeoff to the responsible decision-maker before investing in detailed design or implementation.

## 3. Research the current context

Read applicable project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and evidence from earlier attempts. Look for established patterns and reusable components before introducing new ones.

Understand deployment practices, ownership boundaries, supported environments, monitoring, data handling, and security expectations. Follow existing conventions unless there is a clear reason to change them.

## 4. Define evaluation criteria

Set explicit, lightweight criteria before generating solutions. For example:

- Must preserve current authentication, privacy, and data behavior.
- Must fit the available delivery time and maintenance capacity.
- Should avoid unnecessary dependencies and persistent configuration.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide both selection and explanation. Without them, the first plausible option can win by accident.

## 5. Generate varied approaches

Generate genuinely different options, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code intervention, such as clearer instructions, a process change, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For highly ambiguous problems, generate a wider candidate set before narrowing. Keep each option concise: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate strictly and fail fast for invalid states. Do not hide programming errors by returning plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where practical.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is a stated requirement.
- Avoid quick fixes that bypass the appropriate design boundary.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal containing:

- Problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep proposals direct: usually one or two short paragraphs per option. Store durable proposals in the user's approved shared documentation system when review or collaboration is needed; otherwise provide them in the current workspace. Use a clear date-prefixed title, such as `04 Oct 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration and rollback strategy, test strategy, deployment steps, and ownership of follow-up actions. Keep the plan in a location where authorized reviewers can inspect and edit it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, and failure behavior.

Do not claim success based only on code changes. State what was tested, what passed, and what remains unverified. Commit, publish, or deploy only according to the user's repository, access-control, and release practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and useful operational detail. Do not include unrelated private information or expose material outside the intended access boundary.


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
description: Search the authorized sources most likely to matter and turn relevant evidence into a proportionate, well-sourced context brief for a person, organization, project, topic, or decision.
---

# Gather context

Use this workflow when someone needs to get up to speed before writing, deciding, meeting, planning, making a pitch, evaluating a role-related process, or taking another concrete action. The deliverable is a proportionate context brief: clear, evidence-backed, easy to scan, and safe to share with its intended audience.

## 1. Establish purpose, authority, and boundaries

Start by identifying the action this research should support. For example: prepare for a partner call, understand project status, assess options for a strategic decision, or review a role-related process.

Before accessing private sources, confirm all of the following:

- There is a legitimate purpose connected to the user's work or decision.
- The user is authorized to access the source and use the information for that purpose.
- The planned output destination and audience are appropriate for the source material.
- The search uses only the minimum sources and information needed.

A source being connected or technically available does not make it relevant or appropriate to search.

### Additional rules for information about people

When the subject is a person, use a stricter relevance standard:

- Search private communications, records, calendars, transcripts, or databases only when they are necessary to the stated purpose.
- Do not collect unrelated personal information, sensitive details, or material outside the appropriate access boundary.
- Do not infer protected, health, family, financial, or other private traits unless they are explicitly necessary, authorized, and appropriate to the task.
- Respect consent, confidentiality, retention rules, and reasonable privacy expectations.
- For hiring or assessment, focus on role-relevant capabilities, role alignment, documented experience, diagnostic evidence, and whether an assessment distinguishes relevant performance.
- Share only what the intended audience has a legitimate need to know.

If purpose, authority, scope, or destination is unclear, ask one focused question before searching private systems.

## 2. Scope the request before searching

Right-size the effort. This is the main control against both over-researching and shallow research.

Choose an effort tier based on the request wording, stakes, urgency, and likely consequences:

- **Quick:** A status check, reminder, or narrow factual question. Search one to three obvious sources, use one or two focused queries per source, and return a short answer.
- **Standard:** The usual case. Search several likely sources, use a few targeted queries, inspect the most relevant evidence, and produce a compact brief.
- **Deep:** High-stakes preparation or a consequential decision. Search broadly across relevant source categories, use multiple query angles, verify important claims, inspect primary records, and resolve contradictions.

When uncertain, begin with the lighter tier and offer to deepen the search. It is usually easier to expand a brief than to undo an unnecessary broad sweep.

State the tier in one short line when useful, such as: “I’ll do a standard review across messages, internal documents, meeting records, and public information.” This gives the user a chance to redirect the scope.

### Clarify only genuine ambiguity

Ask one tight clarifying question when the target is unclear enough that searching could produce the wrong result. Examples include a name shared by multiple people, an ambiguous project title, or a term with several meanings.

Do not ask unnecessary setup questions when the target and purpose are clear. Proceed with reasonable assumptions and state them briefly if they materially affect the result.

### Set a working time window

Use a time window that matches the subject:

- For current status, begin with recent activity.
- For a long-running relationship or project, extend backward far enough to establish context and key decisions.
- For a decision, prioritize evidence from the period in which the options, constraints, and commitments were formed.

State the reviewed period in the final brief when it affects interpretation.

## 3. Classify the subject and select sources

Classify the request so the search follows the evidence rather than every available tool.

- **Person:** Relevant correspondence, messages, meeting history, shared documents, authorized relationship records, and public professional information.
- **Organization:** Public information first, then internal correspondence, relationship records, project documents, and authorized pipeline or account records.
- **Project or initiative:** Plans, working documents, messages, task or issue trackers, decision logs, meeting notes, repositories, operational data, and relevant metrics.
- **Topic or question:** Public research plus prior internal analysis, discussions, documents, and technical materials.
- **Decision:** Evidence for each option, prior decisions, ownership, constraints, risks, data, stakeholder views, and unresolved questions.

Named sources are mandatory when authorized. They are a floor, not necessarily a ceiling: add another source only when it is clearly likely to contain decision-relevant evidence.

Do not search all systems by reflex. Skipping an irrelevant source is sound judgment, not incomplete work.

## 4. Search each source deliberately

Use read-only search and retrieval where possible. Search inline for quick and standard work. For a deep review with many independent sources, parallelize by source category or research question only when this reduces delay without creating duplicated effort.

Give each parallel researcher a narrow assignment and require a compact digest containing direct evidence links where permitted, key findings, uncertainty, and gaps. Do not request raw dumps unless they are needed to verify a claim.

### Query strategy

For a deeper review, use multiple useful query angles:

- Exact name, organization, project title, or distinctive phrase.
- Related names, alternate titles, abbreviations, and prior names.
- Decision keywords, commitments, dates, deliverables, or product terms.
- Relevant participants, teams, or counterparties.

For a quick review, use the best one or two queries rather than trying to exhaust the source.

### Source-specific practices

Apply the capabilities below to systems the user is authorized to use:

- **Email:** Search direct correspondence and relevant mentions by others. Read enough of each thread to understand the decision, not only the latest message. Preserve a stable direct link to the actual conversation when the platform supports it.
- **Team messaging:** Search names, organizations, project terms, and decision phrases across channels within the access boundary. Open load-bearing threads and preserve message permalinks.
- **Documents and knowledge bases:** Use workspace-wide content search rather than a mode dominated by calendar entries or automated summaries. Open relevant pages in full and distinguish draft discussion from approved decisions.
- **Cloud documents:** Search file names and contents. If a document platform supports multiple tabs, sheets, or sections, inspect each relevant part rather than assuming the first visible section is complete. Attribute findings precisely.
- **Calendar and meeting records:** Use past events to establish relationship history and upcoming events to explain urgency. If search results indicate a recent meeting, retrieve authorized notes or the transcript; it may contain the most current commitments and context. Be careful with speaker attribution in group or shared-room recordings.
- **Internal databases:** Read available schema, field definitions, and data-quality notes before querying. Prefer the authoritative table for the question, and verify known weak or stale records against stronger evidence.
- **Code, issue trackers, and technical records:** For engineering work, inspect current implementation, issue status, release notes, and version history. Separate what is deployed, planned, discussed, and experimentally observed.
- **Analytics:** Use product or operational metrics only when they answer the question. Record the date range, segment definitions, and measurement limitations.
- **Public web:** Prefer official sites, current professional profiles, filings, primary publications, and reputable reporting. Verify every link before including it. Do not invent, guess, or reconstruct links.

## 5. Handle missing sources and tool failures honestly

Never silently substitute an adjacent source for one judged relevant. If a relevant source is unavailable, empty, inaccessible, or could not be searched, say so in the brief and describe the resulting limitation.

First attempt safe, user-independent remedies: check the configured connection, available permissions, source-name mapping, authentication state, and read-only search capability. Do not alter data, permissions, or retention settings merely to complete research.

If user action is still required, report:

1. The exact source or capability that failed.
2. What safe checks or repairs were attempted.
3. The single remaining action the user needs to take, such as completing authorization or restarting a client-managed connection.

A source deliberately excluded as irrelevant is not a gap and need not be listed as one.

## 6. Evaluate and reconcile evidence

Prefer current, primary, and directly attributable evidence in roughly this order:

1. Approved decisions, signed records, official system-of-record entries, direct correspondence, and full meeting records.
2. Current internal documents and authorized operational data.
3. Credible public sources and current professional profiles.
4. Summaries, informal discussion, and older secondary reporting.

Do not merely place conflicting claims side by side. Investigate the conflict where feasible, explain which evidence is stronger and why, and state any remaining uncertainty. For example, a current official profile may outweigh an old article, while a meeting transcript may clarify a commitment missing from a task tracker.

Separate facts, interpretations, and recommendations. Use calibrated wording such as “confirmed,” “reported,” “appears likely,” and “not verified.”

## 7. Write the context brief

Organize the brief by the user’s decision or action, not by the order tools were searched. Lead with what matters most.

Use this adaptable structure:

```markdown
## [Subject] — context brief
*Reviewed: [source categories]. Window: [dates or scope].*

## TL;DR
- [Most important finding, with supporting evidence link if appropriate.]
- [Key status, risk, decision, or opportunity.]
- [Most important uncertainty or next step.]

## What we know
### [Theme]
[Synthesized finding with direct evidence links where appropriate.]

## Relationship or timeline
[Relevant chronology, commitments, ownership, and changes over time.]

## Open questions and gaps
- [Unanswered question and the source most likely to answer it.]

## Key sources
- [Source title or privacy-preserving reference]
```

Every sourced factual claim should include a direct, clickable link to the supporting record when the platform supports one and sharing that link is appropriate. Link to the primary item, not merely a search result. If a link cannot be safely shared, identify the evidence in a privacy-preserving way and state the access limitation.

Keep prose blocks short. A brief should support scanning and action, not become an essay. A quick request may need only a few bullets; a deep review can use the full structure with themed sections and a timeline.

## 8. Deliver safely and verify completion

Return short briefs inline. For a long-lived or detailed reference brief, create it only in a user-approved, access-controlled workspace that matches the sensitivity of the sources. Use a clear, human-readable title with the date and subject.

Before declaring completion, run this audit:

- Is the effort tier proportionate to the request?
- Was there a legitimate purpose and clear authority for each private source searched?
- Did the search cover the sources most likely to answer the question?
- Were recent meeting records checked when they were clearly relevant?
- Are major claims supported by direct evidence links or explicitly marked as unverified?
- Are contradictions resolved or clearly explained?
- Are sensitive and unrelated personal details excluded?
- Are unavailable relevant sources and resulting gaps disclosed?
- Is the brief organized around the user’s action and usable without rereading raw search results?
- Is the output stored or shared only within the appropriate access boundary?

If editing an existing formatted document, insert text only into a known body-text location or replace a fully identified section. Re-read the edited range in a structured format when available and confirm that headings, body paragraphs, lists, and tables retained their intended styles. Do not report the document complete until both content and formatting checks pass.


---
name: learning-tutor
description: Learn a paper, article, or topic through a short Socratic dialogue that uses retrieval, explanation, and application instead of passive summary.
---

# Learn with a tutor

Help the learner understand, retain, and use a provided paper, article, or topic through a rigorous dialogue. Prioritize active recall and reasoning over passive explanation. The learner should do most of the intellectual work; the tutor guides, diagnoses gaps, and adjusts the level of challenge.

## Core learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to recall and reconstruct ideas in their own words.
- **Ask for mechanisms.** Move beyond conclusions: ask why, how, under what conditions, and with what evidence an idea works.
- **Require generation.** Ask the learner to create examples, analogies, predictions, objections, and applications before supplying them.
- **Use productive difficulty.** Make the task demanding enough to require effort, but not so difficult that the learner cannot make a meaningful attempt.
- **Practice transfer.** Connect the material to unfamiliar cases, adjacent concepts, and real decisions.
- **Surface gaps through questions.** If an answer is incomplete or inconsistent, help the learner notice the tension. Explain directly only after a fair opportunity to reason.

## Conversation workflow

### 1. Establish prior knowledge and a learning goal

Begin by asking what the learner already knows, believes, or has experienced about the topic. Also ask what they want to be able to explain, evaluate, or do.

Ask one or two open questions, such as:

- “What do you already think is true about this topic, and why?”
- “What are you hoping to be able to explain or do by the end?”
- “What experience or related idea does this remind you of?”

Use the answer to identify useful background knowledge, possible misconceptions, and an appropriate starting difficulty.

### 2. Elicit the central idea from memory

Ask the learner to explain the central claim, finding, or problem in their own words. Do not let them merely quote the source.

Useful prompts include:

- “What is the main claim in your own words?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “How would you explain it to a thoughtful friend in 30 seconds?”

If the learner has not read the material, ask for an initial prediction or working model. Then direct them to examine the relevant portion before returning to retrieval.

### 3. Choose a few high-value ideas

Do not attempt to cover everything. Select two or three ideas that are central, difficult, consequential, or likely to be misunderstood. Explore each idea deeply using this cycle:

1. Ask the learner to state or reconstruct the idea.
2. Probe the reasoning, assumptions, evidence, and causal story.
3. Ask for an example, analogy, comparison, or application.
4. Test the idea with an objection, boundary case, or alternative explanation.
5. Adjust the next question based on the learner’s response.

Keep each turn short. Usually ask only one or two questions at a time.

## Question toolkit

Use questions that require explanation rather than recognition. Adapt them to the learner’s level and the material.

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What is the mechanism here, step by step?”
- “What evidence would distinguish this explanation from another one?”
- “Can you construct a concrete example from a familiar setting?”
- “Where might this fail, or where would it not apply?”
- “What is the strongest objection to this argument?”
- “How does this connect to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one key assumption changed?”

Avoid standalone yes-or-no questions. If one is useful for narrowing the discussion, immediately ask the learner to explain their reasoning.

## Responding to answers

Be warm, direct, and specific. Do not use generic praise. When an answer is strong, identify what made it useful—such as naming an assumption, distinguishing correlation from causation, or offering a relevant counterexample—then raise the challenge.

When an answer is incorrect or incomplete:

1. Do not immediately state the correction.
2. Ask a focused question that exposes the tension or missing step.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, provide a concise explanation of the missing distinction.
5. Ask the learner to restate the corrected idea or apply it to a fresh case.

If the learner says, “I don’t know,” invite a low-stakes attempt: “Take a guess based on what you do know. What seems most plausible, and why?” Give a hint after an attempt, or sooner if the task requires knowledge they have not been given.

## Calibration and pacing

Increase difficulty when answers are easy: request a counterexample, a comparison, a prediction, or an application in a different domain. Reduce difficulty when the learner is lost: narrow the question, isolate one assumption, use a simpler case, or present competing explanations and ask them to defend one.

Match the learner’s energy. If they are engaged, pursue the reasoning further. If they are tired or overloaded, consolidate the strongest ideas rather than introducing new ones. Maintain a dialogue, not a fixed quiz: every question should build on the learner’s actual response.

## Progress checks

Periodically provide a brief, evidence-based check-in:

| Check | What to state |
|---|---|
| Demonstrated understanding | [What the learner has accurately explained, reasoned through, or applied.] |
| Remaining uncertainty | [What is incomplete, confused, or unsupported.] |
| Best next focus | [The next concept, distinction, or retrieval task to practice.] |

Do not claim mastery because the learner recognizes terminology or repeats a conclusion. Look for accurate explanation, reasoning, and transfer to a new case.

## Closing gate

Before ending, turn the learning into action. Ask:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation, a self-generated example, or a future retrieval prompt. End by naming the next concept or question worth revisiting.

## Guardrails

- Do not summarize the material unless the learner explicitly asks; even then, invite their own summary first.
- Do not lecture when a well-chosen question can prompt retrieval or inference.
- Do not define jargon automatically; first ask the learner to define it, then clarify if needed.
- Do not make the interaction easy merely to be encouraging.
- Do not cover an entire source superficially when a few core ideas can be understood deeply.
- Keep the tutor’s contribution mostly questions, with concise explanations used to unblock or consolidate learning.


---
name: write-in-my-voice
description: Draft or revise email in the user’s authentic voice by grounding the work in approved style evidence, verifying the message brief, and auditing tone, facts, commitments, and next steps before delivering copy-ready text.
---

# Write in my voice

Use this workflow when drafting, replying to, or polishing an email on the user’s behalf.

## Goal

Produce a copy-ready email that sounds like the user rather than a generic assistant. Preserve their normal warmth, directness, structure, and punctuation while adapting appropriately to the recipient, relationship, and stakes.

## 1. Establish authorized voice evidence

Before drafting, use the strongest available evidence:

1. Read the user’s current style guide in full, if they provide one.
2. Review a small set of recent emails the user actually sent, preferably messages similar in purpose or audience.
3. Identify any approved reusable facts, links, signatures, boilerplate, and standard replies.

Access private messages, drafts, or records only for a legitimate purpose and with clear authorization from the user. Use only the minimum relevant examples. Do not expose unrelated content, personal details, or sensitive information in the output.

Create a practical voice profile:

- Typical greeting and sign-off.
- Formality level and relationship cues.
- Typical sentence and paragraph length.
- Preferred vocabulary, contractions, directness, and degree of warmth.
- Punctuation and formatting habits.
- Words, phrases, tones, or punctuation to avoid.
- How the user makes requests, declines, follows up, apologizes, expresses uncertainty, or gives feedback.
- Approved factual details and reusable language.

Recent sent messages and recent user edits are stronger evidence than older samples or general writing advice. If evidence conflicts, ask which preference is current. If a decision is needed immediately, use the most recent consistent pattern.

## 2. Confirm the email brief

Identify the minimum information required to write a safe, useful message:

1. Who is the recipient, and what is their relationship to the user?
2. What outcome should the email produce?
3. What facts, dates, names, links, attachments, or decisions must appear?
4. What level of warmth, firmness, or formality fits the situation?
5. Is there a deadline, sensitive topic, approval requirement, or commitment that needs confirmation?

Do not invent availability, decisions, promises, prices, opinions, emotional reactions, or factual claims. If a missing detail could materially change the meaning or create a commitment, ask one focused question rather than guessing.

## 3. Adapt the voice to the situation

Voice is not a rigid template. Keep the user recognizable while adjusting for audience and risk.

- **Close colleagues or familiar contacts:** use the user’s usual concise and familiar pattern.
- **New, senior, external, or formal contacts:** retain the user’s voice while providing sufficient context and clearer wording.
- **Sensitive messages, corrections, conflict, or rejection:** be direct, factual, and respectful. Avoid defensive explanations, exaggerated praise, or unnecessary apologies.
- **Requests:** make the action, responsible person, and timing easy to identify.
- **Scheduling or logistical messages:** use approved links, availability, or standard wording only when current and relevant.

Reuse approved standard language when it accurately fits. Do not force a canned response into a context where it could be misleading, outdated, or impersonal.

## 4. Draft the smallest complete email

Include only material that helps the recipient understand and act. A useful default structure is:

1. Greeting, when consistent with the user’s usual pattern.
2. Purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Closing and sign-off, when appropriate.

Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Put decisions, requests, and deadlines where they are easy to find. Use bullets only when they improve clarity for actions, options, or logistics.

Remove:

- Throat-clearing or narration about the drafting process.
- Generic compliments and repeated thanks.
- Filler such as “just wanted to” or “I hope you’re well,” unless it is both natural to the user and useful in context.
- Hedging that weakens an otherwise clear message.
- Details unrelated to the recipient’s need to know.

## 5. Audit before delivery

Review the draft line by line:

- Would the user plausibly write these exact words?
- Do the greeting, closing, punctuation, and rhythm match the available evidence?
- Is the tone suitable for the recipient, relationship, and stakes?
- Did the draft add any unsupported claim, commitment, opinion, emotion, or promise?
- Are names, dates, links, attachments, and references accurate and appropriate to share?
- Is the requested action and timing unmistakable?
- Is sensitive information limited to what the recipient is authorized and expected to receive?
- Can any sentence be removed without reducing meaning or usefulness?
- Does the draft avoid the user’s identified dislikes and known tone problems?

If the audit reveals uncertainty about a consequential fact or commitment, stop and ask for clarification.

## Default when no voice evidence exists

State the assumption briefly and use a broadly useful default: concise, warm-professional, clear, and direct. Invite the user to provide a style guide or a few representative sent emails for stronger future matching.

## Output format

Provide the final email as copy-ready text. If clarification is necessary, ask only the specific question needed to draft safely. Do not add commentary after the final copy unless the user asks for alternatives, rationale, or a revision.


---
name: professional-social-post
description: Draft, revise, and audit professional social posts from notes, drafts, articles, transcripts, research, or a topic, emphasizing strong evidence-based hooks, useful substance, clear audience fit, and targeted iteration.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a draft, an article, a transcript, a podcast, a research finding, or a simple topic.

The goal is not to make an announcement sound enthusiastic. The goal is to make the right reader stop, understand a useful point, and have a reason to care. Write for a defined professional audience with little patience for fluff, generic inspiration, vague claims, or exaggerated stakes.

This is platform-independent. Before drafting, ask the user to choose or confirm:

- The platform and format: text post, caption, document carousel, thread, or article promotion.
- The audience: for example, technical practitioners, founders, policy professionals, researchers, customers, applicants, or peers.
- The purpose: share an insight, explain a concept, announce something, promote a longer piece, start a substantive discussion, or support a campaign.
- The voice: formal or conversational, first-person or organizational voice, preferred words, forbidden words, punctuation preferences, and length.
- Whether an external link will be included and the platform strategy for link placement.
- Whether the post includes private information, a client story, an employee story, or a participant outcome, and what may be named, quoted, or disclosed.

If the user provides approved posts, a writing guide, audience research, or brand guidance, use those materials as the primary voice source. Do not assume a particular person’s voice, publishing system, or distribution tactic.

## Scope, routing, and authorization

Some post types need a different structure. Identify the genre before drafting.

- **Career or participant case study:** A person’s before-and-after story involving a program, employer, or career change. Use a case-study structure: starting point, turning point, concrete outcome, evidence, and lesson.
- **Research or evidence post:** A claim based on data, a model, a report, or an analysis. Prioritize methodology, uncertainty, and defensible interpretation.
- **Product or organizational announcement:** Lead with the concrete change and why it matters to readers. Do not lead with internal excitement.
- **Article, podcast, report, or event promotion:** Lead with the strongest finding, argument, story, or guest insight. Do not lead with “new article,” “new episode,” or “we published.”
- **Carousel or document caption:** Give one or two meaningful findings, then point readers to the visual material. Do not duplicate every slide.

If the post relies on private communications, personnel records, participant records, or other sensitive material, use it only for a legitimate purpose with clear authorization. Use the minimum relevant information. Omit unrelated personal details, respect consent and privacy expectations, and keep the final post within the intended access and publication boundary.

If the genre is unclear, ask one concise routing question before writing. For example:

> Is this primarily a research insight, an announcement, a case study, or promotion for a longer piece?

## Non-negotiable accuracy rules

1. **Do not invent facts.** Do not fabricate statistics, names, quotes, outcomes, clients, organizations, titles, dates, research findings, or testimonials.
2. **Separate evidence from interpretation.** State what the source shows, then clearly label the conclusion, recommendation, or hypothesis.
3. **Preserve meaningful uncertainty.** If a result has broad ranges, weak evidence, major assumptions, or correlation rather than causation, say so plainly.
4. **Use exact details when supported.** Specific figures, dates, roles, mechanisms, and outcomes are usually stronger than broad claims. Do not turn an estimate into false precision.
5. **Ask for missing evidence early.** If the post depends on an unsupported claim, remove it, narrow it, qualify it, or request a source.
6. **Avoid misleading urgency.** Do not enlarge the stakes merely to create engagement. A specific risk and practical response are more credible than catastrophe language.
7. **Use personal stories responsibly.** Obtain confirmation that names, roles, quotes, and outcomes may be published. If approval is not clear, anonymize or use a different angle.

## Audience and voice

Write for the reader most likely to act on the post, not for everyone who might vaguely relate to it. Specificity is a filter: it helps the right reader recognize that the post is for them.

Default voice unless the user provides another one:

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
| Corporate | “We are thrilled to announce an exciting new initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Long, hedged sentences full of unexplained terms. | State the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Broad catastrophe language without a clear mechanism or response. | Name the specific risk, evidence, uncertainty, and useful intervention. |

## The core workflow

### 1. Inspect the source before choosing a format

Do not start with a template. Read the source and find the strongest material inside it.

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

If several plausible threads exist, do not silently choose one. Present two to four numbered options and let the user choose. For each option, explain what it foregrounds and why it fits the audience.

**Angle-selection prompt:**

> I see several viable post angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [specific story, outcome, or disagreement]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Choose one primary thread. A social post should not summarize every point in the source.

### 2. Generate hooks before drafting the body

The opening determines whether the rest of the post is read. Generate five to ten possible hooks before drafting. When user choice would be useful, show a shortlist of three to five strong options.

A hook must make an honest promise that the body fulfills. It should generally work on its own, without requiring the reader to understand the full source first.

Useful hook patterns:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific body of evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Named outcome:** “[Person or role] moved from [starting point] to [specific outcome] in [timeframe].” Use only with evidence and publication approval.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only if the post supports the claim.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused disagreement:** “Why do two credible groups reach such different conclusions about [specific issue]?”

For each shortlisted hook, add a brief strategic note.

| Hook | Strategic purpose |
|---|---|
| “[Specific claim or finding].” | Leads with a concrete result and gives readers a reason to continue. |

Apply the **topic-swap test**: if a key noun can be replaced with an unrelated field and the hook still works, it is probably too generic. Make the hook impossible to write about anything else.

Avoid:

- Generic announcement openings such as “Excited to share.”
- Throat-clearing such as “In today’s fast-moving environment.”
- Empty cliffhangers that do not deliver a payoff.
- Several rhetorical questions in a row.
- Broad motivational claims.
- Clickbait such as “You will not believe” or “This changes everything.”

### 3. Choose one structure

Select the structure that fits the source. Do not combine several structures unless there is a clear reason.

1. **Counterintuitive claim → evidence → implication**  
   Best for research, data, and argument posts. Start with the surprise, show supporting facts, then explain what readers should do or reconsider.

2. **Changed mind → trigger → updated view → takeaway**  
   Best for thoughtful first-person posts. State the earlier view, explain what changed it, and give the new conclusion.

3. **Problem → why it matters → practical response**  
   Best for explainers and operational or policy content. Keep the problem concrete and make the response proportionate.

4. **Result → how it happened → reusable lesson**  
   Best for launches, team outcomes, and approved case studies. The result must be real and specific.

5. **Framework → examples → application**  
   Best for posts readers may save and revisit. Give the framework a name only if the name clarifies rather than brands ordinary advice.

6. **Specific announcement → reader relevance → next step**  
   Use only when the announcement is genuinely notable. Lead with what happened and its practical significance.

7. **Strategic trade-off → rationale → consequence**  
   Useful for explaining deliberate constraints or “anti-goals”: what a team has consciously chosen not to optimize for, why, and what that choice enables.

### 4. Draft the body: hook, tension, payoff

Use this default shape:

- **Hook:** The strongest claim, result, or tension.
- **Tension or setup:** Why the point matters, what is surprising about it, or what assumption it challenges.
- **Payoff:** The evidence, story, framework, or practical insight. The post should be valuable even if the reader never opens a link.
- **Soft close:** Exactly one focused question, one practical takeaway, or one clear pointer to more material.

A useful default length is under 300 words, but length should follow substance and platform norms. Short posts should still make a complete point. Longer posts need a reason for every paragraph.

Use white space. Write in one- or two-sentence paragraphs so the post is easy to scan on a phone. Use bullets only when the content is genuinely list-shaped, such as three reasons, four findings, or a checklist.

For a carousel or document caption:

- Establish the central idea in the post.
- Include one or two of the strongest specifics.
- State what the visual material adds.
- Do not turn the caption into a slide-by-slide summary.

For a linked article, podcast, or report:

- Put the strongest finding in the body.
- Treat the linked material as depth, sources, or extended analysis.
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

If the user has a punctuation preference, obey it. Otherwise, favor periods, commas, and line breaks over theatrical punctuation. Use special text styling or emoji sparingly, and only if the platform supports it reliably. Read the draft aloud. If it sounds like a generic thought-leadership template rather than a person making a specific point, rewrite it.

## Revision protocol

When the user gives feedback, revise the requested line and nearby logic first. Do not rewrite the entire post unless asked.

Examples:

- If the hook is “not sharp enough,” provide several replacement hooks before changing the body.
- If a claim feels overstated, tighten the evidence or soften only that claim.
- If a paragraph feels slow, cut setup before adding explanation.
- If the user prefers an earlier sentence, preserve it unless there is a clear reason not to.

Multiple small options are often more useful than one complete redraft, especially for hooks, closers, and uncertain lines.

Be candid about weak material. For example:

> The second paragraph relies on a broad claim that the source does not yet support. We can add evidence, make it narrower, or replace it with this concrete example: [example].

Do not silently weaken a strong, approved sentence during later revisions. Preserve the best supported phrasing unless the user asks to change it.

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
- Are all names, quotes, figures, outcomes, and claims authorized and supported by source material?
- Does formatting work on the intended platform?
- Does the tone remain professional, respectful, and non-inflammatory for the intended audience?
- If personal information appears, is its use necessary, authorized, and appropriate for public distribution?

If any answer is no, revise before handoff.

## Handoff format

When presenting work to the user, provide only what helps them decide and publish:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft in the user’s chosen delivery format or location.
3. Any unsupported claim, missing input, or line that remains uncertain.
4. Suggested first-comment or link text, if relevant to the platform strategy.
5. A concise publishing reminder appropriate to the platform, such as responding promptly and substantively to genuine early comments.

Do not claim that a format, timing tactic, or engagement metric is guaranteed to improve reach. Platform behavior changes. Treat distribution advice as a testable hypothesis and encourage the user to compare results across several posts.

## Common failure patterns

- **Announcement disguised as content:** The post tells readers the organization is pleased, but not why readers should care. Fix it by leading with the actual change or lesson.
- **Pure teaser:** The post asks readers to click but provides no useful insight. Fix it by sharing the main finding and using the linked piece for depth.
- **Unsupported precision:** The post uses a striking figure without a source, scope, or caveat. Fix it by verifying, qualifying, or removing it.
- **Generic inspiration:** The post sounds positive but has no mechanism, example, or decision. Fix it by naming the concrete action or trade-off.
- **Overpacked summary:** The post tries to cover every section of a report. Fix it by selecting one thread and saving the rest for the original material or later posts.
- **Bolted-on promotion:** A course, product, or service appears at the end without a natural connection. Fix it by removing the pitch, creating a separate promotional post, or making the connection concrete and immediate.
- **Forced engagement:** The post demands reactions or comments. Fix it by asking one real question or ending with a useful conclusion.
- **Unapproved personal disclosure:** The post includes someone’s outcome, quote, role change, or sensitive background without clear permission. Fix it by obtaining authorization, anonymizing it, or choosing a different example.

The final standard is simple: the post should sound like someone with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, or a generic social-media template.


---
name: case-study-post
description: Create an evidence-based, review-ready case study post that shows a person’s credible professional, learning, or career change through specific facts, a clear mechanism, and an audience-relevant call to action.
---

# Write a case study post

Use this workflow to turn source material about a person into a concise public case study for a professional social platform, newsletter, community update, program page, or recruitment campaign. It produces a complete first draft, three alternate hooks, quote-card options, an approval log, and a short delivery note.

The purpose is not to make the subject sound impressive through praise. The purpose is to show a credible change: where they started, what they were considering, what prompted action, what specifically helped, what happened next, what they do now, and what a relevant reader can do.

A good case study gives the reader a recognizable before-state and a concrete path forward. It should not imply that a program, community, employer, or resource single-handedly caused an outcome unless the evidence supports that claim.

## Authorization, privacy, and publishing boundary

Only use personal records, private messages, applications, interview notes, or internal communications when there is a legitimate publishing purpose and clear authorization to access and use them. Use the minimum information needed to tell the story.

Before drafting, establish:

- Who is authorized to provide the source material.
- Whether the subject has agreed to be featured, or what review process applies.
- Which details are public, approved for publication, internal-only, or unknown.
- The intended audience, channel, and access boundary for the finished post.
- Whether naming employers, teams, projects, compensation, or personal circumstances could create risk for the subject.

Omit unrelated sensitive details. Do not publish confidential work, private contact information, health or family information, immigration or legal details, financial circumstances, or personal opinions unless they are relevant, approved, and appropriate for the intended audience.

## Inputs

Ask for all available source material. Useful inputs include:

- Interview transcript, recording notes, or meeting summary
- Application, intake form, or survey response
- The subject’s current professional profile or approved biography
- Official announcements, public work samples, publications, projects, or portfolio pages
- A public or authorized internal message about an outcome
- A previous draft, outline, or the subject’s own notes
- A brand or editorial voice guide
- The intended audience, platform, word count, and CTA
- The subject’s preferred name, pronouns, and review requirements

Build a working fact sheet before drafting:

| Field | What to capture |
|---|---|
| Subject | Full name for verification, preferred public name, pronouns, and whether first-name usage is appropriate |
| Before-state | Previous role, field, uncertainty, constraint, or goal |
| Alternative path | What they were considering or doing instead |
| Trigger | Why they joined, applied, changed direction, or acted at that moment |
| Intervention | The program, community, event, resource, mentor, product, or experience involved |
| Mechanism | One or two concrete things that helped, such as an introduction, opportunity listing, feedback session, or realization |
| Now-state | Current role, organization, team, project, output, or result |
| Timeline | Confirmed dates or elapsed time from participation to result |
| Evidence | Sources supporting names, dates, figures, claims, and quotations |
| Cost or risk | Any meaningful tradeoff that may be relevant and approved |
| CTA | What the target reader should do next |

If critical information is missing, ask focused questions before writing. Never guess at organization names, role titles, project titles, dates, compensation, timelines, or outcomes.

Useful questions include:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they act at that point?
4. What one or two specific things helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there a named output, project, publication, placement, product, or grant that is public and useful to mention?
8. Did they take on a tradeoff or risk they are comfortable sharing publicly?
9. Which names, figures, quotes, and claims have explicit approval?
10. Who should see themselves in this story, and what blocker do they have?

## Evidence and verification rules

Never invent, upgrade, or dramatize a fact. If the evidence says the subject contributed to a project, do not describe them as its lead. If they explored an opportunity, do not say they received it. If they found a listing through a community, do not claim the community secured the role for them.

Automated transcripts and summaries are useful but fallible. They commonly mishear names, organizations, technical terms, numbers, job titles, and dates. Cross-check every detail that affects credibility or could be sensitive.

Use this reliability order unless a stronger source is available:

1. The subject’s direct, recent confirmation
2. Official public records, published work, or an organization’s formal announcement
3. A current professional profile maintained by the subject
4. An original written application or intake response
5. Interview transcript notes or automated summaries
6. Informal third-party messages

Keep three categories separate in working notes:

- **Verified fact:** Supported by a reliable source.
- **Subject interpretation:** The person’s account of what helped or changed their mind.
- **Editorial inference:** A conclusion drawn by the writer. Use sparingly, and only when clearly supported.

If sources conflict, do not quietly choose the most dramatic version. Resolve the conflict with the subject or use the narrower, verified claim.

## Sensitive-content gate

Flag the following for explicit subject approval before publication:

- Pay, compensation changes, financial hardship, or salary comparisons
- Health, family, immigration, legal, or other personal circumstances
- Strong criticism of a former employer, role, or career choice
- Unreleased work, confidential projects, or unpublished titles
- Direct quotes, especially forceful opinions or criticism
- Claims about why an employer selected or hired the person
- Claims of causation, impact, or attribution that cannot be verified
- Exact dates or timelines that reveal private circumstances

If approval is unavailable, use an approved, honest fallback or remove the line. For example, replace a precise compensation figure with a broader approved description only if it remains accurate and useful. Do not make a story vaguer merely to conceal uncertainty, and do not make it more dramatic to compensate for missing evidence.

## Build the story beats

Create a private working outline. Do not show raw notes unless requested.

### 1. Before-state

Capture the subject’s previous role, background, and reader-relevant uncertainty. Include the alternative path they were considering when it mirrors the target reader’s current life.

Keep details only when they explain the decision or make the contrast concrete. A long biography, reading list, or credential inventory usually weakens the post.

### 2. Trigger

Identify why the person acted at that moment. Common triggers include wanting to understand a field, testing whether a career path exists, finding collaborators, improving a practical skill, or aligning work with a concern they had been following.

### 3. Mechanism

Find one or two observable turning points. Strong mechanisms include:

- Realizing that a field has roles for someone with their background
- Seeing a relevant role or opportunity in a community
- Receiving feedback that improved an application, project, or decision
- Having a conversation that clarified a next step
- Receiving an introduction, resource, workshop, or practical example

Avoid claims such as “the experience transformed them.” State what happened instead.

### 4. Now-state

Record the subject’s current role and what they actually do. Name an organization, team, or output only when verified, approved, and useful. Translate specialist language enough for the intended reader to understand why the work matters.

One meaningful artifact can establish credibility. Avoid a resume-like pileup of credentials.

### 5. Timeline and compression

Map the sequence from participation or decision to current outcome. Calculate a concise, truthful timeframe when it strengthens the story, such as “within six months” or “the following year.” Do not force a compressed timeline if the evidence does not support it.

### 6. Quotes

Pull three to five candidate quotes verbatim. Favor quotes that speak to the reader’s identity, uncertainty, or decision, rather than merely celebrating the subject.

Useful quote categories:

1. **Discovery:** “I did not know this path was open to someone like me.”
2. **Mechanism:** “I found the opportunity through the community.”
3. **Conviction:** “I would make the same choice again.”

Light trimming is acceptable only when it preserves the speaker’s exact meaning and grammar. Never rewrite a quote into a more polished claim.

## Generate three hook options

For feed-based platforms, the first two lines determine whether readers continue. Write three hooks before writing the body. Keep each hook to two short sentences and, where useful for the platform, roughly 140 characters or fewer.

### Hook A: Discovery

Use when the target audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a concrete mechanism.

This is the default recommendation when the reader should think, “That could be me.”

### Hook B: Identity collision

Use when the before-and-after contrast is unusually vivid.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This often works well for a broader audience that may not share the subject’s exact initial uncertainty.

### Hook C: Stakes-led

Use only when a meaningful cost or risk has been approved and the audience is likely to read it as honest conviction rather than a warning.

**Formula:** The subject accepted a specific cost to do something. Now, they are doing a concrete piece of work or taking a meaningful action.

Avoid this hook if it implies that participation requires hardship or sacrifice, especially when the aim is to make an opportunity feel accessible.

Recommend one hook. Give one sentence explaining why it fits the audience and one brief reason each alternate is less suitable.

## Draft the post

Aim for approximately 160 to 220 words unless the platform or campaign requires another length. Shorter is usually stronger.

Use this structure:

1. **Hook:** Use the recommended hook.
2. **Before-state:** One short paragraph with the previous situation and a relevant alternative path.
3. **Name the intervention:** Clearly state that the person joined the program, used the resource, or participated in the community. Do not leave this connection implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then land the immediate result in plain language.
5. **Current work:** Say what the person does now and why it matters in understandable terms.
6. **Optional cost:** Include only if approved and genuinely useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already stated in the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

A concise outcome line can be powerful: “They applied and got the role.” Use a short sequence of sentences only when each adds meaning. Do not add credential details merely because they are available.

For platforms that may reduce reach for external links in post copy, put the link in an approved comment, profile destination, or other designated location. Treat this as a platform-specific publishing choice, not a universal rule.

## Style rules

Adapt to the chosen voice guide. If no voice guide exists, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense when possible.
- Use specific names, roles, dates, and figures only when verified and approved.
- Use the subject’s first name after the first full introduction if it suits the publication tone and their preference.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Do not call someone exceptional, inspiring, or brilliant without showing the work.
- Use contractions when the tone is conversational.
- Keep the CTA in full second person: “If you are…” and “you can…”.
- Avoid emojis unless they are an explicit brand choice.
- Prefer periods, commas, and line breaks over em dashes.

On the final pass, remove machine-like phrasing. Cut empty transition sentences, dramatic setup frames, filler intensifiers, hedges, abstract nouns standing in for evidence, false balance, and reflective summaries after the CTA.

Avoid corporate or vague language such as “leverage,” “unlock,” “harness,” “navigate,” “deep dive,” “journey,” “transformation,” and “paradigm,” unless it is necessary in an approved direct quote.

Read the post aloud. If it sounds like a generic thought-leadership template, shorten it and replace abstractions with facts.

## Graphic quote options

Provide three quotes for a visual quote card. Each should be self-contained, ideally under 15 words, and verbatim from approved source material.

Provide one from each category:

- Discovery
- Mechanism
- Conviction

Recommend one quote and explain why it will work without surrounding context. Discovery quotes are often strongest because they mirror the reader’s uncertainty. Choose a mechanism or conviction quote only when it is clearer and more memorable on its own.

## Readiness audit

Before sending for review, check:

- Is every name, role, date, figure, and title verified?
- Have transcript-derived details been cross-checked where needed?
- Is the story within the agreed authorization and privacy boundary?
- Does the post explain a concrete mechanism, not merely a result?
- Does it avoid overstating causation?
- Is the intervention named clearly?
- Does the opening mirror a real audience concern?
- Is the current work understandable to a non-specialist reader?
- Are sensitive claims and direct quotes flagged for approval?
- Is the CTA clear and directed at the intended reader?
- Are there no unsupported superlatives, corporate phrases, generic filler, or excessive em dashes?

## Delivery format

Create the draft in the user’s chosen document system when available. Use a clear title, such as:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and the two alternatives
- The three graphic quote options and the recommendation
- Approval items before publication
- Missing information that would strengthen the post
- The document location or link, if applicable

Do not treat the first draft as final. If feedback says “make the hook better,” generate new hooks rather than making small edits. If asked to make it shorter, cut secondary biography first while preserving the mechanism and outcome. If a subject rejects a sensitive line, replace it with the approved fallback without weakening the whole story.

After final approval, review feedback for reusable lessons. Update this workflow only when a recurring pattern is clear, such as a missing intake question, a consistent voice preference, or a repeated verification issue. Do not invent process changes after a clean review cycle.


---
name: create-editorial-cover-images
description: Create editorial cover images from an article through five distinct concepts, visual review, and three informed improvements using the user’s chosen image-generation workflow. The method produces eight completed options or, when requested,.
---

# Create editorial cover images

Turn an article into eight finished cover-image options. Develop five distinct concepts, generate and inspect every result, then create three improvements based on what actually worked. The user chooses from finished images that clearly connect to the article.

Use the user’s chosen image generator and publishing format. Do not assume a particular account, service, medium, palette, or publication platform. If the user explicitly requests prompts only, follow the prompt-only branch instead of generating images.

When working with unpublished drafts, private communications, or records about people, have a legitimate editorial purpose and clear authorization. Use only the minimum relevant material needed to understand the article. Do not include unrelated personal details, identifiable information, or confidential facts in prompts unless the user has specifically authorized their use and the intended output boundary makes that appropriate.

## Establish the brief

Read the complete article before developing concepts. A title alone is rarely enough to distinguish an image that belongs to this piece from a generic illustration of its topic. If the copy is missing, ask for it before generating.

Identify the article’s central move: the idea, realization, or changed perspective a reader should take away. Notice its emotional progression, including where it becomes quieter, turns, or reaches its conclusion. Extract concrete images, actions, and metaphors already present in the writing. Note the tone, such as reflective, urgent, hopeful, sober, or celebratory, because it constrains the image’s mood.

Use this analysis to make the creative work sharper. Do not begin with a long summary unless the user asks for one. Never invent factual events, places, people, or claims that the article does not support. A visual metaphor may interpret the article, but it should not imply that an imagined scene is a literal depiction of real events.

Reuse preferences already supplied. Ask only for missing choices that materially change the result, keeping related questions together. Collect all outstanding answers before treating a partial reply as the complete brief.

Ask about the following areas when they are not already clear:

- **Mood:** Offer three or four interpretations grounded in particular beats of this article. Explain what each option emphasizes, so the user chooses among real readings of the piece rather than generic adjectives.
- **Subject:** Explore appropriate options such as an anonymous human figure, a landscape, a single symbolic object, or an abstract composition. Respect restrictions on people, places, representations, or factual depictions.
- **Palette:** Offer several palettes suited to the selected mood. Name colors specifically and describe contrast, value, and lightness as well, so the decision does not depend on color labels alone.
- **Orientation:** Establish where the image will appear and how it will be cropped. A wide header, square preview, portrait cover, and social card need different compositions. Use dimensions supplied by the user or verified for the destination.
- **Medium or style:** Establish whether the image should be photographic, painted, drawn, collaged, graphic, or another medium. If the user names a style up front, treat that as the default rather than asking again.

A useful question format is:

1. **Mood:** Which emotional entry point should lead: [article-specific interpretation A], [article-specific interpretation B], or [article-specific interpretation C]?
2. **Subject:** Should the image center on [an article-specific figure or action], a landscape, a symbolic object, or an abstract treatment?
3. **Palette:** Which palette best supports that reading: [specific palette A], [specific palette B], or [specific palette C]?
4. **Format:** Is this for a wide header, a square preview, a portrait cover, or another specified placement?

Keep a concise working brief containing the agreed mood, subject restrictions, palette, medium, format, generator, and any accessibility or brand constraints. Carry it through both rounds without asking the same questions again.

## Propose five distinct concepts

Present exactly five ideas in a numbered list. Each idea needs:

- A short title.
- A one- to three-sentence description of what the viewer sees.
- A brief statement of the article’s idea or emotional beat that the concept expresses.

Vary the subjects, compositions, and interpretations. Five minor changes to one scene do not provide meaningful range. Unless subject restrictions rule them out, include at least one landscape-only option and one single-object or symbolic option. An anonymous, back-turned, or distant figure can be useful when a human presence is needed without making the image about a specific person, but it is not a required default.

Check that every concept has a specific reason to belong to this article. Replace any concept whose explanation could accompany nearly any article on the same broad topic.

Give a one-line initial recommendation, then generate all five without asking the user to choose first. The first round provides visual material for comparison. Do not stop at concepts or written prompts when finished images were requested.

## Write useful visual prompts

Write one self-contained prompt per concept. Keep visual direction specific enough to render while avoiding competing instructions. Use this structure, combining sections where that reduces repetition:

```text
Create one image: [medium, format, and overall visual character].

Subject: [what is visible, its action, prominence, and position; place relevant exclusions alongside the description].

Setting: [surroundings, depth, and foreground or background relationships where useful].

Light and palette: [direction and quality of light, specific colors, contrast, and transitions].

Technique: [visible properties of the chosen medium, edge treatment, texture, detail level, and negative space].

Mood: [the intended feeling and its connection to the article’s central idea].

Composition: [focal point, where the eye enters, placement of major shapes, requested dimensions or aspect ratio, and crop considerations].

Avoid: [only the artifacts, visual conventions, or content that conflict with this brief].
```

Name colors and their relationships instead of relying only on words such as *warm* or *moody*. For example, “pale ochre field against deep violet shadows, with cool blue-grey at the horizon” makes a more usable visual decision than “dramatic warm lighting.” Name colors to clarify the selected palette, not to impose a fixed aesthetic on every article.

Explain the physical appearance of the chosen medium. A watercolor image may need broad wet-on-wet washes, visible pigment bleeds, textured paper, selective edges, transparent layers, and substantial unpainted space. A charcoal drawing may depend on broad tonal masses, broken edges, and visible paper. A photograph may depend on lens perspective, depth of field, natural light, and believable material detail. Do not combine incompatible technique instructions merely because they appeared in another prompt.

Place exclusions beside the relevant positive instruction as well as in a final list when helpful. For example, say “distant silhouette with no facial detail” in the subject description rather than relying only on “no faces” at the end. If empty space is needed for later typography, specify where it belongs. Establish whether lettering is desired; otherwise prevent unintended text, logos, borders, and watermark-like artifacts.

Send the generator only the visual brief needed to create the image. Do not paste a full unpublished article, private records, or unrelated personal context by default. Use article-specific facts only when supported by the copy, authorized, and appropriate for the intended publication.

## Generate the first five

Use the chosen generator’s supported workflow. Explicitly request an image so a text response is not mistaken for the deliverable. Respect existing access, spending, licensing, approval, and account boundaries. Do not bypass approval gates, inspect unrelated account areas, or move content to another service without the user’s agreement.

If the selected service is unavailable, report the limitation and attempt safe recovery within the authorized workflow. If a replacement generator would require sending material to a different service, ask before doing so.

Keep a working record for each option: number, title, concept, submitted prompt, generation status, output location, and review notes. Preserve the complete prompt so a truncated or failed submission can be repaired accurately. Start independent jobs concurrently only when the tool supports that safely and within its limits.

Confirm each submission was accepted with the intended brief. Then confirm that the actual image completed and can be opened at a useful size. An accepted request, elapsed time, placeholder, progress indicator, thumbnail, or text description does not establish completion. If an error appears, check whether an image already exists before retrying to avoid duplicate work. Keep failed attempts separate from completed options.

## Inspect all five before improving

View every completed image at a useful size and evaluate the actual pixels. Do not judge only the generator’s description or what the prompt intended. Also inspect a small preview, because a cover must communicate when reduced or cropped.

For each image, record:

- Whether it communicates the article’s central idea and emotional tone.
- Whether the subject and action read immediately, with a clear focal point.
- Whether the requested style, palette, orientation, and composition survived generation.
- Whether it feels too busy, generic, sentimental, static, or overly literal.
- Any visible anatomy, object, perspective, construction, or lettering artifacts.

Only after reviewing all five, design three new prompts. Tie each improvement to a visible observation: a strength to retain, a weakness to correct, and a change likely to help. Do not prewrite this round before seeing the first outputs.

A useful spread is one refinement of the strongest image, one combination of strengths from different images, and one new concept addressing a gap. Use judgment when another distribution would better serve the article. Each new image must contribute a meaningful alternative rather than a near-copy of an earlier result.

Fix the cause of a weak result. If a composition is cluttered, reduce the number of objects or competing focal points before adding more instructions. If an image looks like a photograph with a paint filter, request fewer large shapes, selective edges, genuine medium marks, and more negative space. If a scene resembles generic travel, workplace, or lifestyle imagery, reconsider the action or metaphor before adding decoration.

Give a short progress update explaining what the first images revealed and what the next three will improve. Continue without requesting another selection or repeating the creative brief.

## Generate, review, and deliver options six through eight

Generate three new images from the revised prompts. Keep the first five intact so the user can compare originals with improvements. Inspect each new result using the same visual criteria and completion checks. Repair failed generation attempts where possible without counting them as finished options or substituting an old image.

Before delivery, verify that there are eight distinct completed outputs that you personally inspected. Check that each can be opened from the final handoff and that titles and numbering match the working record. Use accessible files, saved outputs, or verified links supported by the chosen generator. Preserve the finished outputs for the user to compare.

Recommend the strongest rendered image in a short sentence explaining why it fits the article. Follow with a numbered list of all eight titles and their outputs, clearly identifying the final three as the second round. Keep the outputs as the final deliverable block. Avoid turning the handoff into a long design report.

If access, rate limits, policy restrictions, licensing concerns, or repeated generation errors prevent completion, state exactly which options are finished and which remain blocked. Preserve useful work for resuming. Do not claim eight images exist when some are only prompts, placeholders, or unsuccessful attempts.

After completion or selection, learn only from explicit user feedback and clearly observed results. When the user has authorized memory or workflow updates, save reusable lessons about article interpretation, composition, prompt constraints, or verified generator conventions. Keep private article content out of reusable lessons. Do not convert one article’s subject or a single successful image into a permanent universal default.

## Prompt-only branch

When the user explicitly wants prompts only, do not generate images. Read the article and reuse or collect the same creative preferences. Propose five concepts, then wait for a selection unless the request already specifies concepts or asks for all prompts.

Write each selected prompt in a separate fenced code block using the prompt structure above. If combining concepts, give a one-line explanation of the combination before the prompt. Do not describe hypothetical second-round prompts as improvements informed by visual review, because no rendered results have been inspected. Put the selected prompts last, with nothing after the final block.

## Adapt to another generator

When the user requests a version for another generator, preserve the concept, mood, composition, palette, and format. Change prompt structure or parameters only as needed by the target tool. A prose-oriented generator may suit a compact paragraph, while another may work better with front-loaded descriptive phrases and separate controls.

Check the target tool’s supported conventions before specifying parameter flags, model versions, aspect-ratio syntax, seed controls, or style settings. If a version matters and remains unclear, ask once rather than guessing. Keep each platform variant separate and clearly labeled. Changing generators should not quietly change the underlying image idea.


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
description: Create or improve a short, paid, asynchronous work sample that produces role-relevant evidence, is practical to review, and is validated through simulated submissions before use.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise. A good work sample asks candidates to do a realistic, bounded version of the job, produces evidence that is difficult to imitate without relevant capability, and can be reviewed consistently.

Use it for a new work sample or a revision. Do not use it for interview questions, application-form screeners, or multi-day work trials. If the request could mean one of those formats, ask which format is needed before proceeding.

## Purpose and design principles

A work sample usually sits between initial screening and interviews. It should answer a narrow hiring question: can this candidate demonstrate the most important parts of this role under realistic constraints?

The exercise should not attempt to assess every quality required for the job. Other stages are better suited to other evidence:

- Interviews can assess live communication, motivation, collaboration, and real-time reasoning.
- References can assess reliability, integrity, and sustained performance.
- A later work trial can assess consistency, judgment over time, and performance in real systems.
- Onboarding can often close gaps in a specific tool, internal process, or nonessential domain vocabulary.

Focus the work sample on a small number of load-bearing capabilities that are important to the role and observable in a short exercise. Examples include prioritization, practical judgment, clear writing, problem diagnosis, sourcing, execution speed, systems thinking, or turning ambiguity into useful work.

Use these default constraints unless the hiring owner chooses otherwise:

- Make the exercise paid.
- Set a clear expected completion time, commonly two to four hours.
- Use a realistic but fictionalized or safely anonymized scenario.
- Do not ask candidates to create production work that the organization will use unless that use is explicitly agreed separately.
- Keep expected review time to about 20 to 25 minutes per submission.
- Make the task self-contained. Candidates should not need internal systems, private records, credentials, or access to unavailable people.
- State whether and how AI tools may be used. Evaluate judgment and usefulness, not attempts to guess whether AI was used.
- Assess only capabilities materially related to the role. Do not use protected traits, personal circumstances, or unrelated proxies.
- Offer a route for reasonable accommodations or an equivalent accessible format without lowering the role-relevant standard.

If designing from internal communications, employee records, customer information, or other private sources, confirm a legitimate hiring purpose and clear authorization first. Use the minimum relevant information, remove unrelated or sensitive details, respect privacy expectations, and keep materials within the approved hiring access boundary.

## Step 1: Pre-flight

Before designing anything, confirm that the hiring team has both:

1. A current job description or role brief explaining responsibilities, level, expected outcomes, and reporting context.
2. A role-success profile, hiring plan, or equivalent document identifying the capabilities and experience most likely to produce those outcomes.

If either is missing, stop. Do not try to define the role-success profile while drafting the test. That creates a moving target and usually results in a plausible-looking exercise that measures the wrong things.

Use this request format:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

Once both exist, read the full relevant role context. This may include linked project notes, current team constraints, examples of strong work, prior hiring feedback, and existing exercises for comparable roles. Review one or two reference exercises only to calibrate tone, length, and operating format. Do not copy their task shape automatically; different roles need different evidence.

After reviewing, give a short status update such as: “Read the role brief, hiring plan, and two reference exercises. Alignment memo next.”

## Step 2: Write the alignment memo before drafting

Do not draft candidate-facing instructions yet. First create a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five abilities that the role succeeds or fails on and that can be surfaced within the exercise window. Phrase them as observable capabilities rather than vague virtues.

Weak: “Strategic thinking.”

Better: “Can identify the highest-leverage problem in a messy operating situation, explain the tradeoff, and deliver a useful first action.”

### What the exercise will not test

Name important criteria that belong elsewhere in the hiring process. This keeps the test honest and prevents it from becoming an unrealistic proxy for the whole job.

For example, a three-hour written exercise may not fairly test long-term reliability, leadership over months, responsiveness in meetings, specialized software fluency, or collaboration within a team.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level. Explain what this changes:

- Entry-level candidates may need more context and narrower deliverables.
- Mid-level candidates may need to prioritize and execute independently.
- Senior candidates may need to make tradeoffs, set direction, and create work another person could use without further explanation.

### Failure modes to catch

Identify two or three plausible work patterns that could otherwise look strong in ordinary hiring but would not meet the role’s needs. Describe evidence patterns, not identity-based labels.

Examples:

- A polished planner who does not ship usable work.
- A fast executor who misses the central problem or creates avoidable risk.
- A careful candidate who defers every meaningful decision.
- A technically capable candidate who cannot communicate for the intended audience.

### What strong looks like

Write one short paragraph describing a top submission. Focus on evidence: what it notices, what choices it makes, what it produces, and how it handles uncertainty.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the owner confirms or revises the memo.

## Step 3: Propose exercise shapes

Once the memo is approved, offer three possible exercise shapes. Each must test the load-bearing capabilities in a meaningfully different way, be understandable in about a minute, be self-contained, and be scorable quickly.

For each option, include:

- **Shape:** A plain-language description of the task.
- **What it tests:** The capabilities it reveals.
- **Why it is evaluable:** The evidence reviewers will see and why it supports consistent scoring.
- **Main risk:** The most likely source of noise, unfairness, or weak signal.

Keep each option concise. Useful shapes include:

- **Triage pile:** The candidate receives realistic messages, requests, and constraints. They prioritize, draft responses or work products, and recommend one systemic improvement. This suits operations, coordination, support, and communications-heavy roles.
- **Choose the highest-leverage action and ship it:** The candidate receives several possible priorities, selects one, explains the choice, and creates a small usable output. This suits strategic operations and builder roles.
- **Diagnose and fix:** The candidate reviews a messy situation, identifies the key problem, and produces one targeted intervention. This suits product, program, analytical, and process-improvement roles.
- **Source and pitch:** The candidate defines a target profile, identifies promising channels or prospects from supplied information, and writes outreach. This suits recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** The candidate assesses a supplied intervention area or decision using provided evidence and makes a recommendation. This suits research, policy, strategy, and specialist roles.
- **Design a repeatable system:** The candidate creates a lightweight process, playbook, or operating artifact another teammate could use. This suits program, community, enablement, and operational design roles.

Do not draft the complete exercise until the hiring owner chooses a shape. If none fit, generate three more based on the approved alignment memo rather than forcing a familiar format.

## Step 4: Draft version 1

Write the candidate-facing exercise in this order.

## [Role] Work Sample

Open with one or two sentences explaining the capabilities the exercise assesses. State the total expected time.

**Your mission**

Describe a specific situation rather than an abstract assignment. Give enough context to make the work realistic. If decisiveness is being assessed, make clear which stakeholders are unavailable during the exercise so candidates must make reasonable calls rather than deferring every decision.

End with one sentence restating what the candidate will produce.

**Deliverables**

List two to four parts and include rough time guidance when useful. A common operations pattern is:

- A short prioritization or analysis section.
- Several actual drafts, decisions, or shipped outputs.
- One systemic fix, process improvement, or reusable artifact.

Avoid many tiny tasks. A few substantive outputs reveal more than dozens of shallow decisions. If both planning and execution matter, state clearly that candidates should not spend all their time planning.

**Context**

Provide the minimum information needed to complete the exercise: project state, audience, constraints, available resources, relevant policy, and stakeholder availability. Use fictional names, domains, and identifiers unless real public information is necessary and approved.

For a triage-pile exercise, include roughly eight to ten realistic items. Connect some items so candidates are rewarded for recognizing patterns across the whole situation. Add reference notes for information needed to make fair decisions, such as escalation rules, capacity limits, or refund policies.

**Instructions**

Include:

- The expected time limit.
- The submission deadline, written clearly.
- The required format, such as one document or PDF, plus links to supplementary materials if needed.
- Payment amount, payment process, and any early-submission bonus, if offered.
- A contact route for accommodation requests or accessibility questions.
- What tools and AI assistance are permitted.
- A request to state significant assumptions briefly.
- Permission to submit incomplete work if time runs out.
- Optional guidance on a short walkthrough video, only if it adds useful evidence.

Use a transparent AI policy. For example:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

If payment varies by seniority, effort, or timing, state the terms plainly. Choose compensation that reasonably recognizes the requested time and local legal requirements. Early-submission incentives should reward timely completion without pressuring candidates to disregard accessibility needs or other agreed accommodations.

**Anticipated questions**

Include answers to common questions:

- If a requirement is unclear, make a reasonable assumption and state it briefly.
- If you do not finish in the expected time, submit what you have and state what you would do next.
- The work will be used only to evaluate candidates unless another use is agreed separately.
- If the candidate needs an accessible format or reasonable accommodation, they can contact the designated hiring contact.

## Candidate-facing writing and format checks

Write in direct, plain language and use the locale appropriate to the hiring organization. Keep instructions easy to paste into the chosen applicant-tracking system or document format.

Before sharing a draft, check that the candidate-facing text:

- Has no tables if the destination system renders them poorly.
- Avoids horizontal divider lines if they break the destination editor.
- Uses simple headings and bullets.
- Avoids generic slogans, forced contrasts, repetitive sentence patterns, and unnecessary rhetorical flourishes.
- Uses “by the end of [day]” rather than abbreviated phrasing.
- Uses clearly fictional email addresses and names in fictional scenarios.
- Formats multi-line message metadata clearly. If the target editor collapses line breaks, use its supported soft-break method.
- Does not contain confidential details, private contact information, credentials, sensitive internal data, or unnecessary personal information.

After every draft, add a separate section that is not for candidates:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets on choices the owner may want to change. Typical notes include whether an item is too obvious, whether the scenario is realistic enough, whether payment fits the role level, whether a deliverable is too prescriptive, or whether a video should be optional.

End with one focused decision question, such as: “Which part should we tighten first?”

## Step 5: Iterate with the hiring owner

Expect several rounds of feedback. For each revision, provide the complete updated work sample, not only a change list, so it can be copied directly into the chosen system.

Apply feedback directly unless it would materially undermine validity, fairness, privacy, or safety. If so, state the concern once in plain language, offer an alternative, and let the hiring owner decide.

Common revision directions include tightening vague instructions, loosening over-prescriptive tasks, correcting scenario facts, simplifying deliverables, changing compensation, and replacing unrealistic details.

## Step 6: Simulate two candidates

Before declaring version 1 complete, simulate two full submissions in parallel using the exact candidate-facing instructions.

### Role-aligned simulation

Use a persona that matches the approved role-success profile. Have them complete the actual deliverables within the stated time limit. Ask for a short reflection on their choices, uncertainty, and time allocation.

### Plausible role-misaligned simulation

Use an earnest, capable candidate who could pass ordinary screening but whose work lacks one role-critical capability. Choose a relevant evidence gap, such as a planner where the role needs a builder, a cautious hedger where it needs decisive judgment, or an executor who does not identify systemic patterns. Keep the difference tied to role-relevant work evidence, never identity, background, or protected characteristics.

Have this persona produce the same submission shape.

Then synthesize the results:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both candidates performed similarly.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by likely impact.

Floor checks that both candidates pass are not automatically bad. The concern is when a central capability fails to produce meaningfully different evidence.

## Step 7: Apply validation improvements

Revise the full exercise based on the simulations. Fix the weakest diagnostic points first. Useful revisions may include:

- Making scenario items more interdependent.
- Removing obvious noise that takes seconds to dismiss.
- Adding a concrete constraint that forces a meaningful tradeoff.
- Replacing a broad opinion prompt with a usable deliverable.
- Clarifying reviewer guidance so it rewards the intended behavior.
- Removing specialized knowledge requirements that can be learned quickly and are not essential on day one.

Do not make the task harder merely to narrow the pool. Make it more diagnostic of the approved role-relevant capabilities.

## Step 8: Optional external review

If other reviewers provide feedback, assess each suggestion against the alignment memo. State which suggestions to integrate, which to skip, and why. External review is useful evidence, not an automatic instruction. The hiring owner remains accountable for the assessment design.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The role description and role-success profile are confirmed.
- The alignment memo is approved.
- The chosen task shape maps directly to the load-bearing capabilities.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and does not require private access.
- Payment, deadline, submission, and accommodation instructions are clear.
- Candidate-facing text is formatted for the destination system.
- A reviewer can assess a submission in about 20 to 25 minutes.
- A role-aligned and a plausible role-misaligned simulation have been completed.
- The simulation produced any necessary revisions.
- The final version contains no sensitive data and does not create unpaid production work.
- Role-relevant criteria, accommodation routes, privacy, and potential proxy bias have been checked.

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
- Using real private communications or records when a fictionalized scenario would provide the same evidence.
- Declaring success without checking whether the exercise distinguishes relevant performance.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, accessible, useful for assessment, and clear about what good performance looks like.


---
name: run-a-reference-call
description: Prepare, document, and run a role-relevant hiring reference call using authorized information, targeted questions, and evidence-based notes that support a fair hiring decision.
---

# Run a reference call

Use this workflow when an authorized hiring team needs to prepare for, conduct, and document a reference conversation about a candidate. The goal is to collect specific, role-relevant evidence rather than vague endorsement, then preserve the evidence and its limits in the organization’s approved hiring record.

## Purpose and boundaries

Use reference information only for a legitimate hiring purpose and with appropriate authorization. Confirm that the candidate has supplied the referee’s contact details or authorized contact where required by policy or law.

Use the minimum relevant information from approved hiring records, scheduling records, candidate-provided materials, communications, and public professional sources. Keep notes within the appropriate hiring access boundary. Do not copy unrelated personal details, sensitive information, rumors, or private communications into the call record.

Do not ask about protected characteristics, health, family, immigration status, or other matters unrelated to performance in the role. Focus on demonstrated work, working relationship, role alignment, and evidence useful to the hiring decision.

## Inputs

Collect or confirm:

- Candidate name and role under consideration.
- Referee name, professional contact details, organization or professional context, and stated relationship to the candidate.
- Call date, time, conferencing details, and expected attendees.
- Candidate’s application record and authorized professional links or work samples.
- Current hiring stage and the next decision, work sample, trial, or interview step.
- Role outcomes, capabilities being assessed, evidence already collected, and unresolved questions.

If a detail is unavailable, mark it as unknown rather than guessing. Do not delay preparation solely because a calendar invitation has not yet been created.

## 1. Find and verify the call

Search the approved scheduling system for the referee’s name or contact details. Capture:

- Meeting title, date, time, and expected attendees.
- Conferencing details, if available.
- Relevant scheduling context, such as whether the call is confirmed, tentative, or awaiting a reply.

If no event exists, create the preparation record using an expected or tentative date. Clearly distinguish confirmed details from assumptions.

## 2. Gather hiring context

Review only relevant, authorized hiring material: the candidate’s application, interview notes, role brief, reference-list message, and work-sample or trial evidence.

Identify:

- The role, expected outcomes, and current hiring stage.
- How the referee was introduced and whether contact is authorized.
- The referee’s relationship to the candidate, such as manager, colleague, client, collaborator, or instructor.
- How closely and for how long the referee observed the candidate’s work.
- Open questions from the hiring process that this referee may be well placed to answer.
- Other listed referees, for coordination and later comparison.

Do not present interview opinions as facts when speaking with a referee. Convert concerns into neutral, evidence-seeking questions.

## 3. Research the referee proportionately

Use the minimum useful sources. Review relevant authorized correspondence, prior meeting records, and public professional information where appropriate. Look for direct correspondence, prior meetings, shared projects, the referee’s current professional role, and any organizational connection that may affect context.

Read enough recent material to understand the relationship, not every available message. A practical default is to review a small set of the most relevant recent records from each useful source.

Compile:

- Who the referee is: professional role, current context, and relevant background.
- Their likely vantage point on the candidate’s work.
- Any prior working relationship, conflict, or incentive that could affect interpretation.
- Previous completed reference conversations for the same candidate.

Weight evidence by direct observation, duration, recency, and relevance to the role—not by seniority, confidence, or familiarity alone.

## 4. Review prior references and form a call brief

If prior reference records exist, extract only decision-relevant themes:

- Reported strengths and concrete examples.
- Development areas or constraints.
- Contradictions, unresolved claims, and recurring patterns.
- Questions this referee is uniquely placed to confirm, nuance, or challenge.

Do not treat one referee’s view as settled fact. Frame cross-checks fairly and directly. For example: “A previous referee described strong initiative during unclear projects. Ask this referee for a concrete example and any limits they observed.”

If this is the first reference, identify what will be useful to compare across later calls, such as delivery reliability, response to feedback, stakeholder management, or performance amid changing priorities.

## 5. Create the meeting record before the call

Create one record in the organization’s approved meeting or hiring system. Include the date, referee, candidate, role, call details if applicable, and permitted attendees.

If the system supports recording, transcription, or automated summaries, use those features only with appropriate notice, consent, and organizational approval. Do not assume that a scheduling invitation alone provides permission to record.

Use the following structure.

## Context

- **Referee:** [Name, professional role, organization or professional context, relevant background].
- **Relationship to candidate:** [How they worked together, capacity, approximate duration, and closeness of observation].
- **Hiring context:** [Candidate] is being considered for [role] and is at [stage]. Next step: [decision, work sample, trial, interview, or unknown].
- **Candidate materials:** [Application record], [professional profile], [portfolio or work samples if relevant].
- **Other referees:** [Names and relationship, if known].
- **Call logistics:** [Date/time, attendees, call details, or “not yet scheduled”].

## Opening

> Hi [Referee], thank you for making time. I’m [interviewer role] at [organization]. [Candidate] is being considered for our [role]. We are speaking with people who have worked with them to understand their role-relevant strengths, development areas, and the environments where they do their best work. Please share concrete examples where you can. We will use your input only for this hiring process and handle it within the appropriate hiring team.

Tailor this wording to any existing professional relationship and the organization’s confidentiality policy. Do not promise absolute confidentiality if notes may be reviewed by an authorized hiring panel.

## Briefing notes

Write direct, actionable notes before the call:

- **Decision questions:** [What uncertainty must this call reduce?]
- **Prior-reference themes:** [Who reported what, and what needs confirmation or challenge?]
- **Unique vantage point:** [What this referee can speak to better than others].
- **Role-relevant probes:** [Capabilities or outcomes to test].
- **Context to handle carefully:** [Conflict, limited observation, or unclear relationship], if relevant.

Example: “Earlier feedback described reliable delivery but limited evidence of handling difficult stakeholder situations. Ask for a specific situation, what the candidate did, and the result.”

## Questions

Ask these as one conversation. Adapt the order and follow-up questions to the referee’s evidence.

- **How did you work together?** What were your respective roles, how long did you work together, and how closely did you observe their work?
- **What did the candidate personally own?** What did they concretely deliver, and how did it compare with expectations?
- **What is their strongest contribution?** Please describe a specific example rather than a general impression.
- **Where did they need the most support or development?** What did that look like in practice?
- **How did they respond to difficult feedback, setbacks, or changing requirements?**
- **If they started this role and struggled in the first few months, what is the most likely reason?**
- **If they were doing well after several months, what development area should their manager prioritize next?**
- **What working conditions, management approach, or team environment helped them contribute at their best?**
- **Would you choose to work with them again?** In what kind of role or context?
- **What have I not asked that would help us understand their alignment with this role?**

### Role-specific probes

Select three to five probes tied to actual role outcomes.

| Role capability | Evidence-seeking probe |
|---|---|
| Operations and delivery | “Tell me about a process they improved. What was broken, what did they change, and what result followed?” |
| Community or stakeholder work | “How did they build trust, handle difficult interactions, and know whether relationships were improving?” |
| Leadership | “How did they prioritize competing demands and help others deliver through uncertainty?” |
| Technical or analytical work | “How did they turn analysis into a decision, product, or operational result that others could use?” |
| Written communication | “Can you describe a time their writing clarified a complex decision or moved work forward?” |

## 6. Run the call and test for evidence

Start by confirming the relationship and level of observation. Ask open questions first, then follow vague praise with prompts such as:

- “What did that look like?”
- “What was their personal contribution?”
- “Can you give a specific example?”
- “What was the outcome?”
- “How often did you observe that?”

Do not lead the referee toward a preferred answer. Test concerns neutrally without disclosing confidential interview judgments or unnecessarily attributing claims to other people. If evidence conflicts, record the contradiction and seek examples rather than forcing agreement.

## 7. Record signal and audit the notes

After the call, separate three layers:

1. **Observation:** What the referee directly saw or experienced.
2. **Interpretation:** The referee’s assessment of what it means.
3. **Hiring inference:** What the hiring team concludes for this role.

For each important claim, note confidence and limits: directness of observation, recency, duration of collaboration, relevant examples, and possible bias or conflict.

Before closing the record, check:

- Does it identify the referee’s relationship and evidence quality?
- Does it contain concrete examples, not only traits or rankings?
- Does it distinguish observation, opinion, and inference?
- Does it address the role’s most important uncertainties?
- Does it avoid unrelated or sensitive personal information?
- Does it preserve disagreements or uncertainty rather than smoothing them away?
- Is access limited to the authorized hiring group?

A reference call is one input, not a final verdict. Compare it with role-relevant interview, work-sample, and other reference evidence before making a hiring decision.


---
name: use-a-browser-safely
description: Complete browser-based tasks safely by using the least invasive authorized method, protecting account and privacy boundaries, verifying what the rendered page accepted, and separating preparation from consequential actions.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing forms, changing settings, collecting information from rendered pages, testing a flow, taking screenshots, or working in an authenticated dashboard. Select the safest practical method, verify the state the website actually accepted, and do not treat a successful automation command as proof that the intended result occurred.

> **Central rule:** Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until the account, target, page state, and authorization are clear.

Modern web applications may keep visible controls, the browser document, and internal application state separate. A text-entry command can finish without error even though the application rejected the value, has not committed it until focus changes, replaced the control during a re-render, or will submit a different value.

## 1. Choose the least invasive authorized route

Use the first route that can safely complete the task:

1. **Supported direct interface or API.** Prefer an official, authorized programmatic interface when it can complete the requested work. It is usually more reliable and less disruptive than reproducing a user interface.
2. **Headless browser automation.** Use this for public pages, testing, screenshots, routine rendered-page extraction, and forms that do not require an established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing account session, single sign-on state, account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for an appropriate direct method. Check official documentation, standard form actions, page source, and observable requests for supported interfaces. A form may submit structured data through an authorized service that is safer than manipulating a complex interface.

Do not use an undocumented route to bypass access controls, consent boundaries, security measures, contractual restrictions, or site protections. Do not use a signed-in visible browser merely because it is convenient; it can interrupt the user and increases privacy and account risk.

If a site blocks automated browsing, do not evade the block for research or collection. For a legitimate task the user specifically requested on that site, an authorized visible session may be appropriate when it is necessary to complete the task normally. Never weaken authentication, anti-abuse controls, browser warnings, or access restrictions.

## 2. Confirm authority, privacy boundaries, and scope

Before accessing private communications, records, dashboards, or information about people, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Keep outputs within the requester's appropriate access boundary and respect consent and privacy expectations.

Do not copy unrelated personal information into screenshots, logs, notes, or reports. Do not expose credentials, session tokens, recovery details, authentication prompts, private account content, or security settings.

Identify the intended outcome before navigating deeply:

- What exact page, record, form, setting, or workflow is the target?
- What information must be entered, collected, changed, or uploaded?
- What is the minimum information required to complete the task?
- Which choices require the user's judgment?
- Is the final action reversible?
- Does it send, publish, submit, purchase, delete, grant access, change a plan, or create another external commitment?

If the target, authority, requested outcome, or a material choice is unclear, stop and ask a focused question before changing data.

### Separate preparation from commitment

Treat preparation and commitment as different phases:

- **Preparation:** drafting, filling fields, selecting options, configuring settings, and producing a preview.
- **Commitment:** submitting, sending, publishing, paying, deleting, changing access, or activating an irreversible setting.

Use authorization the user has already clearly provided for the requested action. If the user explicitly requests review before submission, honor that request. If authorization for the final action is missing, prepare and verify the result, then ask only for permission to perform that action.

For high-impact or one-way actions, capture the pre-action state and obtain confirmation unless the user already gave clear authorization for that specific commitment. This is especially important for payments, sends, publication, deletion, billing or plan changes, access changes, and actions labeled final or impossible to undo.

## 3. Protect account and browser context

An authenticated task requires an account preflight. Explicitly determine the intended context before opening or changing the real target: for example, personal, work, test, staging, or production.

Follow these rules:

- Announce when taking control of a visible browser and state the purpose.
- Use a fresh tab, window, or isolated tab group unless the user specifically identifies an existing tab to use.
- Select the intended browser profile or connection directly. Do not rely on a generic default, browser-window name, remembered label, or tab title.
- Verify the signed-in account through a reliable account indicator before acting on the actual target.
- Confirm the environment and the exact record, page, or object that will change.
- Stop and ask if account, environment, target, or authority remains uncertain.
- Do not disable security controls, authentication, warnings, or browser protections to make automation easier.

Use this preflight question:

> Which account is active? Which environment is active? What exact item will change?

If the automation environment has a verification marker, permission gate, or action unlock, enable it only after the account check has passed. Never create such a marker in advance merely to permit actions.

## 4. Inspect the rendered page before editing

Do not begin by guessing selectors, filling controls by numeric order, or assuming a visually similar element is the real editable field. Inspect the rendered page first.

For each relevant control, determine:

- Its type: single-line input, multiline field, rich-text editor, dropdown, checkbox, radio group, date/time picker, upload control, or custom widget.
- Its stable semantic identity: visible label, accessible name, placeholder, or label relationship.
- Its current value, required state, disabled state, and validation requirements.
- Whether it is the true editable control, a wrapper, or a hidden synchronization element.
- Whether it or a related control causes the form to re-render.
- Whether formatting rules, length limits, or dependencies can alter entered content.

Address controls by semantic identity whenever possible, such as visible label text or an explicit accessible-label relationship. Avoid document indexes because dynamic pages can change control order during loading or re-rendering.

Before editing an existing record or setting, inspect its current state. This avoids changing the wrong item or unintentionally overwriting information.

### Generic inspection pattern

Use the selected browser automation capability to record enough structure to distinguish controls safely. At minimum, capture the element type, role, label, required state, and readable current value or text length.

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

## 5. Use an interaction that matches the control

A generic value-setting operation is not reliable for every widget. Use normal user-like interaction when the application maintains its own state.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use the normal text-entry method. | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away. | Some pages commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editable node, replace content through keyboard-style input, then blur. | Direct document writes may not update internal state. |
| Dropdown or combobox | Choose an option by visible text, then wait for the page to settle. | Selection can cause a full re-render. |
| Checkbox or radio control | Read current state first; change only when needed. | A click can reverse an already-correct value. |
| Date/time picker | Select the value and verify the rendered summary. | A popover may clear or reinterpret related values. |
| File upload | Confirm the file, destination, audience, and sensitivity first. | Uploading may begin immediately and be difficult to undo. |

For a framework-driven editor, use this sequence:

1. Focus the actual editable element rather than an accessible wrapper.
2. Select and remove existing content if replacement is intended.
3. Enter the new content with keyboard-style events.
4. Move focus to a neutral page element so the control can commit.
5. Wait briefly for rendering to settle.
6. Read the result back from the page.

Some pages pair a visible editor with a hidden input. Editing the hidden element can look successful in a document inspection while server-side validation treats the editor as empty. Edit the user-facing control that the application reads.

If a dropdown, checkbox, tab, or date control can refresh the form, make and verify those selections before entering long text. Re-inspect afterwards and confirm earlier values remain present.

## 6. Verify every meaningful change

A completed automation command is not verification. After each field edit or meaningful setting change, read the result back from the rendered page and compare it with the intended value.

For sensitive content, do not reproduce full values unnecessarily in logs or reports. Compare length, required state, a redacted excerpt, or a minimal summary.

Check for:

- A command reporting success while the field remains empty.
- Missing line breaks, whitespace, punctuation, special characters, or text near a length limit.
- Truncation caused by a single-line or constrained field.
- Content that appears visible but was not retained by the application's editor state.
- A later interaction erasing an earlier value after a re-render.
- Editing a hidden synchronization field instead of the visible control.
- Dependent values, such as dates, recipients, attachments, permissions, or validation rules, changing unexpectedly.

When verification fails, do not continue toward submission. Diagnose the control type and retry once using a more appropriate method. If the page still rejects or changes the value, do not silently submit an approximation. Report the limitation and ask how to proceed.

## 7. Apply a readiness gate before commitment

Before a final submission or other high-impact action, inspect the relevant page state again. Confirm all of the following:

- The correct account, organization, and environment are active.
- The target record, page, or workflow is the intended one.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Recipients, dates, attachments, permissions, options, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final control has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a material value cannot be verified, or the target is uncertain, **do not submit**. A partially completed form is usually recoverable; an incorrect external action may not be.

For consequential work, create a pre-action record such as a screenshot, concise state summary, or structured field dump. Store and share it only within the appropriate access boundary. Avoid pasting large tables of sensitive values into ordinary chat when a short summary and securely available record are sufficient.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, permissions, and options were checked.
- [ ] A pre-action record exists when the action is consequential.
- [ ] The final action and its impact are understood and authorized.

## 8. Commit once, then verify completion

For consequential work, use two passes:

1. **Preparation pass:** Fill or configure the page, verify the state, and create a pre-action record. Do not activate the final control.
2. **Commitment pass:** Confirm authorization where needed, re-check account, target, and readiness, then activate the final action once.

If the page reloads, re-renders, or the session changes between passes, do not assume the prepared state remains valid. Re-check and restore values as necessary, then verify again.

A final button click is not proof of success. Look for reliable evidence: a persistent success message or reference, a newly created or sent item, a changed status or saved setting that survives a safe reload, or a confirmation screen identifying the intended action.

If the site reports an error, inspect the resulting state before retrying. Some errors are cosmetic while the action succeeded; blind retries can create duplicates. If completion cannot be verified, report what was attempted, the available evidence, and what remains uncertain.

## 9. Common failures and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank. | The application ignored a direct value change. | Use focus, keyboard-style entry, blur, and read-back verification. |
| Earlier values disappear after later edits. | A re-render reset uncommitted state. | Commit and verify each field; complete re-rendering selections first. |
| Text loses line breaks or characters. | The wrong control type or formatting rule was used. | Find a multiline or editor control, or use a clearly acceptable simplified format. |
| A locator finds an empty wrapper. | The accessible element is not editable. | Inspect the labeled underlying control and target the true editor. |
| Validation says a visible field is empty. | A hidden synchronization element was edited. | Use the visible interactive control that the application reads. |
| Automation is unstable on a complex page. | The chosen automation layer is unsuitable. | Switch to a more robust method or supported direct interface; do not blindly rescue a broken session. |
| The account context is uncertain. | The wrong profile or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |
| An error appears after a final action. | The action may have succeeded despite the message. | Inspect persisted state before retrying. |

## Final audit

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back and verified.
- [ ] Required fields and validation passed the readiness gate.
- [ ] A pre-action record was captured when appropriate.
- [ ] Required confirmation was obtained before commitment.
- [ ] Completion was verified after the action.
- [ ] The final report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: Create, revise, test, evaluate, and package a reusable AI skill from a new idea, an existing draft, or a workflow demonstrated in conversation. Use this workflow to build skills that are clear, safe, evidence-based, and adaptable to the AI.
---

# Create an AI skill

Use this workflow to create a new reusable AI skill, improve an existing one, assess whether a skill helps, or turn a repeated conversation workflow into instructions another AI can follow. A skill is a focused set of instructions, plus optional scripts, references, templates, and tests, that helps an AI perform a recurring job consistently.

The core loop is:

1. Understand the intended job and its limits.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review outputs with the user and measure objective requirements where appropriate.
5. Improve the skill from evidence rather than guesswork.
6. Repeat until the skill is reliable enough for its intended use.
7. Optionally improve the description that determines when the skill activates.
8. Package and hand off the final skill.

Do not assume every project needs a full benchmark. Some users want a quick draft, a collaborative exploratory session, or a simple sanity check. First determine where the user is in the loop, then help them take the next useful step.

## Communication principles

Match the user’s technical background. Use plain language by default and briefly define unfamiliar terms. For example, explain that an *evaluation* is a repeatable test of whether the skill produces the needed result, and that an *assertion* is a specific pass/fail check.

Keep the user involved at consequential decisions:

- Confirm the intended job before writing a large instruction set.
- Ask before selecting a narrow scope, mandatory tool, external action, or approval policy.
- Share proposed test prompts before treating them as the evaluation set.
- Let human judgment lead when quality is subjective, such as writing tone, design, strategy, or usefulness.

Explain why important questions matter. For example: “Should the result be a chat response, a structured report, a file, or an action in another system? That changes both the instructions and how we verify completion.”

When a task involves private communications, records, or information about people, proceed only for a legitimate purpose and with clear authorization. Use the minimum relevant sources and details, exclude unrelated sensitive information, respect consent and access expectations, and keep all outputs within the appropriate access boundary.

## 1. Identify the starting point

Classify the request before choosing a workflow.

### New skill

The user has an idea for recurring work. Start with discovery, scope, and a first draft.

### Existing skill

The user has a skill that needs editing, simplification, testing, or improvement. Read its current instructions before proposing changes. Preserve the established name and identity unless the user explicitly requests a rename.

### Workflow demonstrated in conversation

The user may say, “Turn what we just did into a skill.” Extract what the conversation already establishes:

- Inputs and source material.
- Tools or capabilities used.
- The sequence of decisions and actions.
- Corrections and preferences supplied by the user.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow, identify missing decisions, and ask the user to confirm it. Do not turn a one-time workaround into a general rule without checking that it will apply in future cases.

### Evaluation-focused request

The user may already have a finished-looking skill and want to know whether it helps. Start with test design and comparison. Do not rewrite a skill merely because it can be rewritten.

## 2. Capture intent and scope

Gather enough information to define a coherent, reusable job. Do not ask every question mechanically; prioritize the unknowns that would most change the design.

Use these questions as needed:

1. **Purpose:** What should the AI accomplish?
2. **Activation:** What user requests, wording, or situations should use this skill?
3. **Inputs:** What information, files, systems, references, and permissions may it use?
4. **Outputs:** What should it produce, change, or communicate? Is there a required format?
5. **Success:** How will the user decide that the result is correct or useful?
6. **Boundaries:** What should it not do? When should it ask a question, pause, decline, or return work to the user?
7. **Variations:** What common cases, difficult cases, or exceptions matter?
8. **Dependencies:** Does it need user-provided access, a specialized capability, templates, reference material, or deterministic helper scripts?
9. **Testing:** Should the skill be tested with realistic examples before it is adopted?

Offer choices when useful:

- “When a required detail is missing, should the skill make a clearly labeled best-effort assumption or stop and ask?”
- “Should the default result be concise, detailed, or chosen by the user?”
- “May the skill use any available source, or only sources the user has explicitly approved?”
- “Should it prepare a draft only, or may it perform an external action after confirmation?”

Recommend testing when work is repeated, consequential, objectively checkable, file-producing, or likely to vary with input quality. For highly subjective creative work, lightweight human review may be more valuable than forced numerical metrics.

## 3. Research and authorization checks

If relevant resources are available, review approved documentation, existing skills, user-provided examples, format requirements, and applicable standards before drafting. Research should reduce the user’s effort, not replace their authority over requirements.

Use it to identify:

- Existing conventions and output standards.
- Constraints imposed by an available tool, API, file type, or environment.
- Reusable patterns from comparable work.
- Safety, legal, privacy, compliance, and approval requirements.

If research requires access to internal records, personal data, or private communications, confirm that the task has a legitimate purpose and the user is authorized to request it. Use only the minimum necessary sources. Do not expose unrelated personal details in drafts, test data, screenshots, logs, or packaged resources.

When sources conflict or a requirement cannot be verified, report the uncertainty rather than presenting a guess as fact.

## 4. Choose a skill structure

Keep each skill focused enough that users and the AI can predict what it does. A skill may support related variants, but separate unrelated jobs when they differ in audience, permissions, sources of truth, or definition of completion.

A portable package can use this structure:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional deterministic helpers
├── references/              # Optional detailed documentation
├── assets/                  # Optional templates or output resources
└── evals/                   # Optional test prompts and grading material
```

Use progressive disclosure:

1. **Metadata or description:** A short statement that helps the AI decide whether the skill applies.
2. **Core instructions:** The normal workflow, loaded whenever the skill is used.
3. **Supporting resources:** References, templates, and scripts consulted only when relevant.

Keep the core instructions readable. If they become too large, move detailed variants into clearly named reference files and say exactly when to read them. Give large reference files a table of contents or other clear navigation.

For a skill with multiple variants, use a shared selection workflow and separate references by variant. The AI should load the relevant material rather than treating every variant as mandatory context.

### When to bundle scripts

Bundle a script when repeated runs show that the AI repeatedly reconstructs the same deterministic procedure, such as conversion, validation, calculation, report generation, or data cleanup. A bundled script should be:

- Reusable across requests.
- Easier to verify than a fresh natural-language procedure.
- Clearly documented with inputs, outputs, and limits.
- Safe and within the user’s authorized scope.

Do not automate an action just because it is possible. Scripts must not conceal behavior, bypass authorization, alter systems unexpectedly, or create security risks.

## 5. Write the skill

Draft in clear, imperative language. Explain the reason for important instructions, especially where a rule prevents a likely failure. A capable AI usually performs better when it understands the desired outcome and tradeoff than when it receives a long list of unexplained prohibitions.

Use the following sections where applicable.

### Purpose and scope

State what the skill does, its intended context, and its boundaries. Clarify whether it creates an answer, produces a file, guides a process, or performs an action.

### Inputs and prerequisites

List required information, allowed sources, required capabilities, and optional inputs. State what happens when required information is unavailable.

Example:

```markdown
Before preparing the report, confirm the reporting period and approved source material.
If a required source is unavailable, ask for an export or prepare a clearly marked incomplete draft.
```

### Workflow

Give a normal sequence with decision points instead of attempting to enumerate every scenario.

A durable pattern is:

1. Inspect the request and available inputs.
2. Ask focused questions only when the answer materially changes the work.
3. Gather evidence from approved sources.
4. Perform the task using an appropriate method.
5. Check the result against requested format and success criteria.
6. Present the output, assumptions, evidence, and unresolved limits.

Use conditional instructions where needed:

```markdown
If the user provides an approved template, follow it.
If no template is provided, use the default structure below.
If an action could overwrite work, publish information externally, or create a material commitment, explain the impact and request confirmation first.
```

### Output format

Define a template when consistency matters:

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

Use flexible goals rather than a rigid shell when the task requires substantial adaptation to context.

### Quality, safety, and privacy checks

Specify checks needed before completion: required fields, accurate calculations, source support for significant claims, preservation of original data, clear uncertainty labels, and approval before high-impact action.

The skill must behave in ways a user would reasonably expect from its description. Do not create instructions that facilitate deception, unauthorized access, data exfiltration, security compromise, harmful automation, or covert collection of private information.

### Failure behavior

Describe general recovery behavior:

- **Missing or conflicting input:** Identify the gap and ask a focused question.
- **Unavailable capability or source:** State what could not be verified and offer a safe alternative.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the result; otherwise ask.
- **Validation failure:** Do not present the result as complete. Correct it, flag it, or request direction.
- **Permission-sensitive action:** Pause for confirmation before irreversible, external, or high-impact work.

### Examples

Include only a few generalized examples when each teaches a distinct pattern. Examples should demonstrate reasoning and format, not turn the skill into a narrow collection of memorized cases.

## 6. Write a strong activation description

The skill description is a routing instruction. It should say both what the skill does and when it should be used.

Cover realistic user language, including requests that imply the job without naming it. A useful pattern is:

```text
Create clear project status reports from approved updates and source material. Use for leadership summaries, progress reports, milestone reviews, risk updates, and requests to explain current work, next steps, or blockers, even when the user does not say “status report.”
```

A good description includes:

- The task or outcome.
- Common contexts or phrases that indicate the task.
- Important scope limits that prevent expensive or harmful false activation.

Do not put the entire procedure in the description. Avoid vague descriptions such as “help with documents,” but also avoid descriptions so broad that they capture nearby work better handled by another skill.

## 7. Review the draft before testing

Read the skill as if encountering it for the first time. Check:

- Is the job coherent and bounded?
- Does the description identify when to use it?
- Are inputs, permissions, and outputs clear?
- Does the workflow explain why important checks exist?
- Does it handle missing information and validation failure?
- Does it rely on undeclared personal conventions, private access, or a particular tool?
- Are there redundant, brittle, or overly restrictive instructions?
- Does it give a capable AI enough freedom to handle ordinary variation?

Prefer lean instructions that affect behavior. Repeated absolute language is a warning sign unless it protects a real safety, privacy, authorization, or correctness boundary.

## 8. Design realistic test cases

Once the draft is stable enough to test, create two or three realistic prompts. Share them with the user and invite changes before relying on them.

For each test case, record:

- A descriptive identifier.
- The prompt.
- Input files or context.
- The expected result in plain language.
- Objective checks, if suitable.

A portable structure is:

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

Cover meaningful variation:

- A typical successful request.
- Incomplete or ambiguous input.
- A format-sensitive or rule-sensitive case.
- A realistic edge case that changes the workflow.
- A request that should require approval, a privacy boundary, or a safe refusal, if relevant.

Do not merely restate the skill’s instructions in test prompts. Vary phrasing, detail level, and the user’s apparent familiarity. Use synthetic or authorized material for tests; never embed private records, credentials, or unnecessary personal data.

## 9. Run tests and comparisons

When independent execution is available, compare the skill against a meaningful baseline.

- **New skill:** Run each prompt with the skill and without the skill.
- **Existing skill:** Save an unchanged copy before editing, then compare the revised version with the earlier version.

Start both conditions under comparable circumstances. When parallel execution is available, start all skill and baseline runs together. Save the prompt, inputs, outputs, and available metadata such as elapsed time and resource usage. Record timing as soon as the environment reports it, since some systems do not retain it.

Use a clear iteration layout:

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

If independent or parallel runs are unavailable, perform a transparent sanity check: follow the skill for each prompt, save outputs, and ask the user to inspect them. Do not describe this as a rigorous baseline comparison.

## 10. Define and grade objective checks

While runs are in progress, draft objective checks where they genuinely help. Explain them to the user before using them as success criteria.

Good checks are specific, observable, and meaningful:

- Required sections are present.
- A produced file opens and contains the required fields.
- Calculations match an agreed source within a defined tolerance.
- The response identifies missing mandatory inputs.
- Significant claims include required source references.

Record each check with a descriptive statement, pass/fail value, and evidence:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when required source information is missing.",
      "passed": true,
      "evidence": "The final section lists unavailable data and requests the missing source."
    }
  ]
}
```

Use programmatic checks when practical. They are more repeatable than visual inspection and can be reused in later iterations. Do not force numerical checks onto subjective work such as tone, aesthetics, or strategic judgment; human review is more appropriate there.

## 11. Review and analyze results

Present outputs and measurements in an accessible review format. If a review interface is available, use it to show each prompt, output, comparison condition, grades, and feedback field. Otherwise provide accessible files or a clear conversation-based review.

Ask focused questions:

- Which result would you trust in normal use, and why?
- What was missing, misleading, difficult to use, or unnecessarily time-consuming?
- Did the skill introduce steps that did not add value?
- Would this work for similar requests with different wording or data?

Analyze more than the average pass rate. Look for:

- Checks that pass regardless of condition and do not distinguish useful performance.
- High variation that suggests ambiguity or unreliable instructions.
- Quality gains that cost too much time or compute.
- Repeated failures with the same root cause.
- Repeated planning, research, or formatting that does not improve outcomes.
- Helper procedures repeatedly recreated across runs, suggesting a script or template should be bundled.

Small evaluations are evidence, not proof. Use them to guide the next revision.

## 12. Improve without overfitting

Base revisions on feedback, outputs, and analysis. Change the smallest part likely to address the underlying cause.

Generalize from complaints. If one test omitted a source note, do not add a rule mentioning that exact prompt. Instead clarify the broader condition: when evidence is incomplete or mixed, distinguish verified information from assumptions and identify the missing source.

Use these principles:

1. Fix causes, not individual examples.
2. Remove instructions that do not improve behavior or create wasted work.
3. Explain the reason behind important actions.
4. Add reusable scripts, templates, and references only when evidence justifies them.
5. Preserve behavior the user already values.
6. Add tests only for genuine classes of failure.

After revision, rerun the test set in a new iteration and apply the same comparison policy. Show prior and current results when possible. Stop when the user is satisfied, feedback is consistently positive, objective requirements are reliably met, further revisions no longer help, or remaining issues require unavailable information or a product decision.

## 13. Optional blind comparison

For a more rigorous comparison between two versions, give an independent evaluator two outputs without identifying their origins. Ask it to judge against a shared rubric, record the judgment, then reveal which output came from which version.

Use blind comparison when versions have similar numerical results, qualitative quality matters, or the decision has meaningful cost. Evaluate correctness, completeness, clarity, adherence to constraints, safety, and practical usefulness. Analyze why one output was preferred before changing the skill again.

## 14. Optimize triggering behavior

Only optimize the description after the skill’s workflow is stable. Create a realistic set of requests that should activate the skill and nearby requests that should not.

Include roughly balanced coverage. Positive cases should vary in formality, wording, directness, and context. Negative cases should be difficult near-misses, not irrelevant requests. They should share concepts with the skill but require another workflow or lack conditions that make this skill useful.

```json
[
  {
    "query": "I need a concise leadership update from these project notes, including risks and next steps.",
    "should_trigger": true
  },
  {
    "query": "Can you explain when teams usually use progress reports?",
    "should_trigger": false
  }
]
```

Review the set with the user. If repeated activation tests are supported, separate examples used to improve the description from held-out examples used to select the final version. Choose the description that performs best on held-out cases rather than the one that best fits the editing examples.

Remember that simple one-step tasks may not activate a specialized skill even if the description matches, because the AI may complete them directly. Use substantive trigger tests where consulting the skill would add real value.

## 15. Package and hand off

Package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The description accurately states activation conditions.
- Instructions do not depend on private habits, undeclared tools, or unavailable access.
- References and scripts are included, clearly named, and documented.
- No confidential data, credentials, identifiers, private records, or sensitive examples remain.
- The user can install, access, or adapt the skill in their chosen environment.
- Test material is retained only when it is safe and useful.

Provide a short handoff note explaining what the skill does, required capabilities, known limitations, and how to test it after installation.

## Final readiness gate

A skill is ready when it has a clear and bounded job, an accurate activation description, instructions that handle normal variation, explicit boundaries for uncertainty and permissions, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for the user’s recurring work.


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

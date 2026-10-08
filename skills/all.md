# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate distinct options for a decision or problem, assess tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs credible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas. It is a set of genuinely different paths, with candid tradeoffs and a small number of well-matched choices.

## Inputs and access boundaries

Start with the decision or question, plus any context the user provides. Relevant context may include prior decisions, requirements, deadlines, research, stakeholder concerns, or results from earlier attempts.

If the user points to records or communications, review only sources that are necessary and authorized for the stated purpose. Use the minimum relevant information, avoid unrelated personal or sensitive details, and keep the output within the user's access boundary. Do not assume access to linked material; if it is unavailable, state the gap or ask for the needed excerpt.

## 1. Gather context

First determine whether the question is self-contained. If it is not, retrieve a small number of high-value sources that could materially change the option set, such as:

- Earlier decisions and the reasoning behind them
- Existing commitments, budgets, deadlines, or technical constraints
- Evidence of what has already been tried
- Ownership, approval, and stakeholder requirements

Use targeted research rather than broad searching. When uncertainty remains, distinguish facts from assumptions. Ask a focused question when the missing answer would substantially alter the recommendation.

## 2. Frame the decision

Write a two- to four-sentence decision framing that states:

- What the user is actually deciding
- The key constraints and non-negotiables
- What a good outcome looks like
- The criteria that should distinguish the options

The stated request may be a proposed solution rather than the underlying decision. For example, “Should we add this feature?” may actually be “How can we reduce this recurring problem within a fixed delivery window?”

Ask the user to confirm or correct the framing before producing a substantial option set. You may proceed immediately when the issue is obvious and low-stakes, or when the user explicitly requests a first pass. Make any assumptions visible.

## 3. Generate distinct options

Generate five to seven meaningful options, unless fewer genuinely distinct paths exist. Distinct options differ in their core approach, not merely in intensity or scale. Merge near-duplicates such as “do more of the current process” and “do much more of the current process.”

Include, when relevant:

- The obvious or conventional path
- An incremental or lower-effort path
- A more ambitious path
- A path that changes scope, sequencing, incentives, ownership, or the problem framing
- At least one surprising but plausible alternative, such as delaying, partnering, reducing scope, running an experiment, or deliberately doing nothing

Do not be unconventional merely for novelty. A wait-or-do-nothing path belongs only when it has a credible benefit, such as preserving resources, gathering evidence, or avoiding premature commitment.

Give each option a short, memorable label rather than a number. For every option, provide:

- **What:** One or two sentences describing the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, constraints, or failure risks.
- **Effort:** Low, Medium, or High.

Be candid. Do not disguise dealbreakers, and do not make a preferred option appear better by applying softer standards to it than to alternatives.

## 4. Evaluate and recommend

Select criteria that fit the decision. Common criteria are expected impact, effort, cost, speed, risk, reversibility, strategic fit, evidence strength, and stakeholder burden. Add domain-specific criteria where needed.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they clarify the decision, but explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, give one sentence explaining why it fits this situation, its constraints, and its goals.
4. State the assumption or unknown most likely to change the ranking.

Do not force a single winner unless the user asks for one. The purpose is to preserve meaningful choice, not to simulate certainty.

## 5. Pause for the user's choice

After presenting the options and recommendations, stop. The user may:

- Select an option
- Ask for deeper analysis of one option
- Correct the framing or constraints
- Request additional options
- Combine options into a hybrid

For a hybrid, check whether its components are compatible and whether combining them resolves a genuine tradeoff rather than adding complexity. Do not begin implementation until the user chooses a direction or explicitly asks to plan it.

## 6. Choose the next activity

Once a path is selected, match the next step to the consequence and reversibility of the decision:

- **High-consequence or hard-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term obligations, significant staffing decisions, or choices with broad effects.
- **Reversible choice:** Create a right-sized decision record with the choice, owner, rationale, assumptions, boundaries, and review point.
- **Build-oriented choice:** After recording the decision, create an execution plan covering requirements, milestones, tasks, dependencies, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, decide, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before responding, verify that:

- The decision framing addresses the real choice, not just the first proposed solution.
- Options are fundamentally distinct.
- The obvious path and a credible alternative framing were considered.
- Strengths and weaknesses are specific and balanced.
- Effort labels are plausible.
- Recommendations follow the user's stated criteria and constraints.
- Important uncertainty, assumptions, and access limitations are explicit.
- The response ends with choices for the user rather than unrequested implementation.


---
name: pressure-test
description: Find weak points in a leading strategic idea before commitment through steelmanning, sequential challenge, a pre-mortem, and a clear verdict with next action.
---

# Pressure-test an idea

Use this workflow when someone is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it is not for generating a broad set of options or creating an implementation plan.

## Where this fits

Use a decision sequence appropriate to the situation:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its impact and reversibility.
4. Plan, build, or execute the chosen approach.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes an exercise in defending it.
- If this idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings in the decision process.
- If using internal communications, records, customer data, or other personal information, confirm a legitimate purpose and authorization. Use only the minimum relevant material; omit unrelated personal or sensitive details and keep the output within its proper access boundary.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Steelman the idea before criticizing it. Attack its strongest reasonable form, not a caricature.
- Ask **one forcing question at a time**. Wait for the response, assess it, and challenge unsupported, vague, or evasive answers before moving on.
- Use available evidence such as metrics, research, prior experiments, documented decisions, customer feedback, or expert input. Clearly distinguish facts, interpretations, and forecasts.
- Refer to potential dissenters by relevant role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent anyone's opinion.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging without changing the decision-maker's meaning. Include the action, expected outcome, mechanism, timeframe, and conditions needed for success.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original statement is already the strongest version, say so and continue. If the improved wording materially changes the claim, ask for confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions the claim requires. Rank them by the damage they would cause if wrong, with the most consequential first. Make vague assumptions observable where possible.

| Rank and assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest credible test |
|---|---|---|---|---|
| 1. [State the assumption] | [Choose one] | [Evidence or lack of evidence] | [Low, medium, or high] | [Test or disproof method] |

Replace claims such as “users will value it” with observable behavior, a defined group, and a threshold where possible.

## 3. Run forcing questions sequentially

Ask five to eight questions total, selecting them based on the highest-risk assumptions. Do not present all questions as a questionnaire. Later questions should respond to the answers already received.

Useful categories include:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What comparable attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break, constrain, or make harder?
- **Stakeholder dissent:** Which role would object most strongly? What would that role say, and has that view been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for concrete support. “I think it will work” is not enough; ask for observed behavior, data, comparison, or a credible commitment.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, usually 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include a flawed premise, execution failure, and external condition when relevant.

| Failure mode | Why it could happen | Earliest observable warning sign | Monitoring action or accountable role |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Signal that appears early enough to act] | [Check and owner] |

Warning signs must be observable early enough to support a course correction.

## 5. Surface credible dissent

Identify two or three roles that could reasonably challenge the idea. State the strongest likely objection from each role. If those perspectives have not been sought, mark that as an evidence gap. Silence is not agreement.

Dissent does not automatically veto an idea. It exposes constraints, incentives, dependencies, and risks supporters may overlook.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the idea is not falsifiable. Mark the pressure-test incomplete or failed rather than approving it.

## 7. Give a verdict and handoff

Choose one verdict and name the next step.

- **GREEN — proceed to decision.** Core assumptions have credible support, relevant objections have been addressed, reversal costs are understood, and warning signs have monitoring ownership. Next: create a decision record and commit. For hard-to-reverse or organization-defining choices, schedule a review point.
- **AMBER — test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible test, such as targeted interviews, an expert review, a prototype, or a short data-collection period. Next: run the test, then decide with the result recorded.
- **RED — stop, redesign, or reopen options.** A core assumption is weak, downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with exactly **one concrete next action**: a verb, an accountable owner, and a deadline when useful.

Example: `Research owner: interview five target users this week and compare results with the adoption assumption.`

## Final audit

Before closing, verify that the output includes:

- a confirmed steelman;
- three to five ranked load-bearing assumptions;
- five to eight forcing questions explored sequentially;
- a pre-mortem with early warning signs;
- credible dissenting roles and objections;
- a clear mind-change criterion;
- a GREEN, AMBER, or RED verdict with a named next step; and
- one concrete next action.

Common failures: skipping alternatives, asking all questions at once, mistaking confidence for evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, or issuing a positive verdict without falsifiable criteria and monitoring.


---
name: make-a-decision
description: Match decision rigor to stakes and reversibility, make and record meaningful choices with permission, and review predictions without inventing the user’s views.
---

# Make a decision

Use this workflow to give each decision enough rigor, but no more than it needs. The aim is to make a clear call, record meaningful reasoning only with permission, and learn from results without rewriting history.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices deserve minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user prefers, believes, or decided something they did not actually say.
3. **Separate advice from attribution.** Assistant recommendations belong in conversation and must be labeled as **Assistant analysis**. Add them to a decision record only when the user specifically requests that.
4. **Record only with permission.** “Should we do X?” requests analysis; it does not authorize creating a record. Create or update a record only when the user asks to log, track, open, resume, or commit it, or explicitly agrees to the practice.
5. **Protect privacy and access boundaries.** Before searching or writing shared records, communications, personnel information, customer information, or other sensitive sources, confirm a legitimate purpose and clear authorization. Use the minimum relevant sources and details.
6. **Do not mistake a task for a decision.** If there is no meaningful alternative, say so: “This is an execution task rather than a decision. Let’s plan or do it.”

If a record is visible to other people, confirm that its audience is appropriate before logging sensitive material. For health, relationships, compensation, confidential personnel matters, or similarly private topics, offer a private document or keep the discussion in chat.

## 1. Select the mode

Use the user’s explicit instruction when they provide one. Otherwise, if authorized to access the decision register, search for relevant overlapping records before creating a duplicate.

| Mode | When to use it | Action |
|---|---|---|
| New | No relevant record exists | Frame and classify the decision. |
| Resume | A matching decision remains open | Retrieve it and append new thinking. |
| Commit | An open decision exists and the user is ready to choose | Complete readiness checks, then resolve it. |
| Review | A resolved decision has reached its review date and lacks a final assessment | Compare actuals with the original prediction. |

A resolved decision can mean either answer to a binary question, or simply that a non-binary choice has been made. Do not override a clear instruction such as “start new,” “resume,” “I’ve decided,” or “review.”

For a resumed decision, append information rather than overwriting history. Use the original record as the baseline at review; do not reconstruct old reasoning from memory.

## 2. Frame the decision

Write the question in a form that can be answered. Establish:

- What exactly is being decided?
- Who has decision authority?
- What are the realistic options, including doing nothing when relevant?
- What deadline, trigger, or cost of delay applies?
- What result is desired?
- What happens if no action is taken?

If the problem is open-ended and credible options do not yet exist, generate options before evaluating them. Do not pressure-test a vague problem statement.

## 3. Classify scope

Ask one clarifying question at a time if necessary. Use this test: **What would it cost to unwind this?** Include money, time, trust, operational disruption, opportunity cost, and reputational effects. If the answer cannot be stated quickly or is uncertain, treat the choice as larger than it first appears.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default. |
| Reversible | Moderate stakes and reversible in days or weeks | Compare a few options; use a light record if useful. |
| Hard to reverse | Undoing it has meaningful cost or disruption | Full analysis, challenge gate, and stakeholder check. |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, dissent, and prerequisite conversations. |

If the user calls a decision trivial, test that judgment with the unwind-cost question. If they are stalling on a truly trivial choice, name the cost of delay and recommend a reasonable default.

## 4. Use the appropriate rigor

### Trivial

Choose a reasonable default, give a one-sentence rationale, and move on. Do not create a decision record unless the user asks.

### Reversible

In a short working session:

1. List two or three realistic options.
2. Give each option one meaningful strength, one meaningful weakness, and a rough effort or cost estimate.
3. State a recommendation labeled **Assistant analysis**.
4. Where uncertainty matters, prefer the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, confirm that the leading option has been pressure-tested in the current work context. A valid pressure test examines assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and major stakeholder objections.

If no relevant pressure test has occurred, stop the commitment flow and say:

> This decision is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Proceed only after the challenge is complete or the user explicitly overrides it with a reason.

Treat the pressure-test result as a decision rule:

- **Green:** No material unresolved objection was found. Continue to commitment after the remaining checks.
- **Amber:** Risks or unknowns remain, but are understood and acceptable, mitigated, or bounded by a test. Continue only if the record names those conditions.
- **Red:** A serious unresolved failure mode, invalid assumption, or better alternative was identified. Do not force commitment. Return to option generation, redesign the leading option, gather a decision-changing fact, or run a bounded test.

After a green or amber result, complete:

1. Options and decision criteria.
2. A pre-mortem: “It is later and this failed. What most likely caused it?”
3. A stakeholder check: who has relevant expertise, bears consequences, or may reveal a constraint?
4. A recommendation, clearly distinguished from the user’s view.

### Direction-setting

Use the hard-to-reverse process plus two gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and represent their strongest case fairly.

The decision is not ready until the required conversation has occurred, unless the user explicitly accepts and records a reason to proceed without it. If rushed, state exactly which consultation, evidence, or dissent is being skipped and why that matters.

## 5. Keep evidence, advice, and user views separate

For each serious option, capture what it enables, what it costs or prevents, the strongest supporting evidence, the strongest objection, key assumptions, and reversal difficulty.

Choose criteria before comparing options. Distinguish non-negotiable requirements from preferences. Use scoring only when it clarifies a real tradeoff rather than disguising judgment.

Maintain these labels:

- **User’s stated view:** Only positions the user has expressed.
- **Assistant analysis:** Recommendations and reasoning from the assistant.
- **Open question:** Material uncertainty not yet resolved.

If the user has not stated a position, write “No position stated yet” or leave that field blank. Never manufacture a lean, confidence percentage, rationale, treatment of dissent, or final choice.

## 6. Commit and record

Before finalizing a meaningful decision, confirm the choice, why it is preferred now, what could change it, next-action owner and date, observable prediction, and the user’s confidence in that prediction.

Use the user’s chosen authorized record system. Suggested fields include status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. Default review periods are one month for reversible choices, three months for hard-to-reverse choices, and six months for direction-setting choices, unless a concrete trigger is better.

For high-stakes decisions, create a reminder in the user’s chosen calendar or task system if authorized. A review-date field alone may be enough for lower-stakes reversible choices.

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
- User’s stated position today: open / leaning / decided / no position stated yet

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
User’s own reasoning, only when stated by the user.

## What would change my mind
Assumptions or evidence that would justify reversing the choice.

## Prediction
By [date or trigger], [observable outcome] will happen or not happen.
Confidence: [X%]

## Worries
Most credible downside or failure mode.

## Retrospective
To be completed at review.
```

For a new open decision, record only context, options, and actual new inputs. Leave commitment sections blank until the user commits. When resuming, append a dated thinking-log entry rather than replacing earlier reasoning.

## 7. Review outcomes

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare the event with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the evidence, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. A favorable outcome does not prove the process was good; an unfavorable outcome does not prove it was poor.

## Completion message

When the user makes a decision, summarize it clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [DD MMM]
Review: [DD MMM YYYY or trigger]
Record: [location, if one exists]
```

Use direct language and challenge weak reasoning with evidence. Do not let rigor become endless deliberation. Once the appropriate gates are met, name the decision, take the next action, and schedule the learning loop.


---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only mode.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, automation, integration, or operational problem where the right solution is not already clear. Do not use it for a small fix or routine task with a known implementation.

By default, work from understanding through implementation. If the user requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start from the underlying problem, not the first proposed solution. When someone asks to “build X,” work backward:

- Who is affected and what are they trying to accomplish?
- What happens today?
- What workarounds or alternatives exist?
- How frequent, costly, urgent, or blocking is the issue?
- What outcome would make the situation meaningfully better?

Write a concise problem statement and descriptive requirements. Define the desired outcome, constraints, and measures of success without assuming a particular implementation. If the proposed solution does not fit the problem, say so clearly.

Ask only for information that cannot be found in available documentation, code, approved records, or the user’s supplied context.

### Boundaries for people-related information

If understanding the problem requires reviewing communications, support cases, employee records, customer records, usage data, or other information about people:

- Establish a legitimate, specific purpose for the review.
- Confirm that the requester has clear authorization to access the sources and use them for this purpose.
- Use the minimum sources, date range, fields, and excerpts needed to answer the question.
- Respect applicable consent, notice, confidentiality, retention, and privacy expectations. Do not assume that access to a system authorizes a new use of its contents.
- Avoid collecting or repeating sensitive personal information unless it is necessary for the stated purpose and appropriately authorized. Sensitive information may include health, financial, identity, precise location, legal, family, demographic, or private communication details.
- Remove names, identifiers, and unnecessary personal details from working notes and outputs where possible. Prefer aggregated or anonymized findings.
- Keep outputs within the appropriate access boundary. Share findings only with people authorized to receive them, and do not move sensitive material into broader documentation, tickets, logs, or public channels.

If authorization, purpose, consent expectations, or the safe output audience is unclear, pause and ask for clarification before reviewing or disclosing the information.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, existing alternatives, and maintenance burden. “Do nothing,” “deprioritize,” or “improve the current workaround” are valid options when the problem is low impact or already adequately handled.

Distinguish between:

- **Reversible decisions:** Small choices that are inexpensive to change. Use reasonable judgment and proceed.
- **Hard-to-reverse decisions:** Persistent data changes, migrations, public interfaces, long-lived configuration, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation.

If priority or direction is unclear, present the tradeoff and ask the accountable decision-maker to choose before investing in detailed design or implementation. Record consequential decisions and their rationale when useful.

## 3. Research the current context

Read the relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operating procedures, and previous attempts. Find established patterns and reusable components before creating new ones.

Understand compatibility requirements, deployment practices, supported environments, access boundaries, security expectations, ownership, observability, and rollback constraints. Follow existing conventions unless there is a clear reason to change them.

When research involves restricted systems or people-related records, document the purpose, authorized sources, and intended audience at a level appropriate to the work. Do not copy raw sensitive content into proposals or implementation plans unless it is necessary, authorized, and access-controlled.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. For example:

| Criterion | Example expectation |
|---|---|
| Compatibility | Must preserve current authentication and data behavior. |
| Delivery | Should fit the available time and maintenance capacity. |
| Operational cost | Prefer no new dependency or long-lived configuration. |
| Quality | Must have a practical verification method. |
| Reversibility | Should be removable or recoverable if it fails. |
| Data handling | Must use only authorized data and keep outputs within the intended access boundary. |

These criteria guide both solution generation and selection. Without them, the first plausible approach can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, rather than small variations of one design. Always consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution, such as clearer guidance, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For especially ambiguous problems, generate a wider set of candidates before narrowing. Keep each option concise: what it is, what it solves, main costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate strictly and fail fast for invalid states. Do not silently transform programming errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer loosely coupled, well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure when suitable.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Avoid quick fixes that bypass the appropriate design boundary.
- For systems handling people-related information, minimize collection, restrict access, avoid unnecessary retention, and make authorization boundaries enforceable rather than relying only on policy.

## 6. Evaluate and recommend

Compare viable options against the evaluation criteria. Present a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.
- For people-data work, the legitimate purpose, authorized information scope, sensitive-data safeguards, consent or notice considerations, and intended output audience.

Keep proposals direct and brief. Store durable proposals in the user’s chosen shared documentation system when review or collaboration is needed; otherwise provide them in the current workspace. Use a clear date-prefixed title, such as `DD MMM YYYY: Solve — topic`.

Do not include raw private communications, unnecessary identifiers, or sensitive details in a broadly accessible proposal. Use summaries, aggregates, redaction, or a restricted appendix where needed. Confirm that proposal access matches the authorization boundary before sharing it.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, access and data handling, migration and rollback strategy, test strategy, deployment steps, and follow-up ownership.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm results against the evaluation criteria, including compatibility, privacy, security, authorization, and failure behavior.

If the implementation accesses or processes people-related data, verify that:

- Access is limited to authorized roles and systems.
- The solution collects and retains only necessary information.
- Sensitive values are protected in interfaces, logs, test fixtures, analytics, and error reporting.
- Consent, notice, and user-control requirements are met where applicable.
- Outputs, exports, alerts, and dashboards are available only to appropriate audiences.
- Test data is synthetic or otherwise approved for testing.

Do not claim success solely because code was written. State what was tested, the results, and what remains unverified. Commit, publish, or deploy only according to the user’s repository and release practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.
- Any continuing access, consent, retention, or output-sharing constraints relevant to the solution.

Keep the handoff focused on outcomes and operationally useful detail. Share it only through channels suitable for its information sensitivity, and avoid burying the reader in temporary implementation notes.


---
name: shape-and-draft
description: Shape consequential documents through evidence review, answer-dependent alignment rounds, readiness checks, concise drafting, and a final audit.
---

# Shape and draft a document

Develop a consequential document by shaping the thinking before writing it. Identify the change the document must create, review relevant evidence, resolve material choices with the appropriate decision-maker, and then draft the smallest document that can do the job.

Use this workflow for strategies, narratives, operating agreements, proposals, scorecards, decision memos, and similar documents when the argument, boundaries, commitments, or operating model are still unsettled. Use a lighter process for a simple edit, formatting task, or document whose content and decisions are already clear.

When working with private communications, records, or information about people, have a legitimate purpose and clear authorization. Use only the minimum relevant sources and information, omit unrelated or sensitive personal details, respect consent and privacy expectations, and keep both working material and output within the appropriate access boundary.

## Classify the request

A request may name a document, outcome, audience, or source material. Treat the named document type as a hypothesis until its purpose is understood.

Use a **full shaping process** when the document is strategically important and material choices remain open, or when the requester asks for deep thinking, several question rounds, or close alignment before drafting.

A substantive interview round resolves a distinct layer of choices and uses its answers to determine the next questions. Repeating prior discussion or asking for broad approval does not count as a substantive round.

## 1. Work backwards from the outcome

Start with the change the document must produce. Establish:

- Who will read it.
- What readers should understand, decide, approve, or do afterward.
- What is unclear, contested, blocked, or going wrong now.
- Whether the document mainly needs to explain, persuade, decide, coordinate, or govern.

Do not accept “write a narrative” or “make a strategy” as the goal. Identify the actual job the document must perform.

## 2. Choose the artifact

Recommend the form that best serves the job:

- **Narrative:** Builds shared understanding of why something matters and what bet is being made.
- **Strategy:** Connects a diagnosis to choices, priorities, outcomes, and exclusions.
- **Operating agreement:** Defines ownership, decision rights, interfaces, handoffs, and working cadence.
- **Decision memo:** Records a choice, alternatives, rationale, risks, and a review point.
- **Scorecard:** Defines a role or team mission, outcomes, and role-relevant capabilities.
- **Hybrid:** Combines forms when readers need both context and execution clarity.

Explain the meaningful tradeoff and recommend an artifact. If the choice of form would change the argument, structure, or required decisions, ask the authorized decision-maker to confirm it before proceeding.

## 3. Gather and classify evidence

Read supplied material first. Follow any stated source hierarchy, evidence standards, citation rules, and linking requirements. Scale research to the stakes and use only authorized sources and systems.

For a consequential internal document, seek the minimum relevant material that may contain prior decisions, current definitions, supporting evidence, dissent, constraints, and ownership context. Do not search broad private records merely because access is available.

Apply these rules:

- Prefer current, authoritative decision records over discussion notes, recollections, generated summaries, or repeated claims.
- Resolve contradictions where evidence permits; surface material contradictions that remain.
- Do not ask people for facts that the available sources can answer.
- Do not edit, overwrite, or otherwise change source material unless explicitly instructed.
- Include sensitive personal information only when it is necessary, authorized, and appropriate to the document’s purpose.

Keep evidence separate from alignment:

- Sources can establish what happened, what people said, and what an authoritative record currently states.
- Sources do not automatically establish what a current decision-maker believes, will promise, or chooses to exclude.
- A repeated theme, plausible synthesis, or implication is an **inference**, not a settled decision.
- Ask for confirmation before using an inference as a central claim, commitment, boundary, recommendation, or operating rule.

Before the first interview round, provide a short situation brief covering:

- What sources establish.
- What has already been explicitly confirmed.
- What is inferred but unconfirmed.
- The central tension, gap, or missing logic.
- The recommended artifact.
- Important uncertainties that only the decision-maker can resolve.

## 4. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds already completed in the current conversation. Do not repeat settled questions.

Do not draft immediately after the first round simply because one apparent central issue is resolved. Use a later round to test the implications: boundaries, tradeoffs, counterarguments, ownership, definitions, or execution details.

Ask four to eight focused questions per round. If fewer than four material questions remain, ask only those and say that this is a narrow final check. Do not add ritual questions to meet a number.

Each numbered question should normally seek one decision. Do not bundle independent choices, such as ownership, coordination, handoffs, and success measures, into a single broad question.

Use one answer surface unless the user requests another format or the environment requires it. Put the updated synthesis and questions together so the respondent can answer in shorthand. Do not duplicate the same questions across chat and an interactive form.

Use this compact format:

1. Number questions continuously: `1.`, `2.`, `3.`. Keep each number attached to the same decision.
2. For bounded choices, offer three or four mutually exclusive, decision-relevant options labeled `a.`, `b.`, `c.`, and optionally `d.`.
3. Put the recommended option first unless context makes another order clearer.
4. Use two options only when there are genuinely only two distinct states.
5. Put questions and options on consecutive lines with no blank lines inside the question block.
6. Let the respondent reject the framing or give a different answer.

Example:

1. Which direction should the document recommend?
   a. Focus first on the highest-impact problem; this narrows scope but clarifies accountability.
   b. Address all related problems equally; this is broader but may weaken ownership.
   c. Present options without a recommendation; this preserves flexibility but delays a decision.
2. Who should make the final decision?
   a. The accountable lead after required consultation.
   b. A cross-functional decision group.
   c. The sponsoring leader.

Each round should:

1. Start with an updated model and state what changed because of earlier answers.
2. Focus on one layer of uncertainty rather than every issue at once.
3. Explain the tradeoff behind the recommended option.
4. Separate source-supported observations from choices the decision-maker must make.
5. Surface contradictions and ask the smallest question needed to resolve them.
6. Include a pressure test when the document is persuasive or strategically consequential.
7. Leave room to correct assumptions or introduce a different framing.

A typical progression is purpose, strategy, operating model, definitions and measures, then expression and destination. Adapt the sequence to the task, but preserve the answer-dependent loop: later questions must arise from earlier answers rather than from a generic questionnaire.

After every answer round:

1. Match shorthand and free-text answers to question numbers, preserving qualifications such as “mostly c” or “not sure.” Classify each answer as confirming, rejecting, softening, qualifying, or deferring the proposed position.
2. Trace downstream implications. A changed audience, softened commitment, new exception, or rejected framing often creates another question.
3. Update the alignment ledger and show a concise synthesis.
4. Generate the next round from remaining material uncertainties and their consequences.

Continue while an uncertainty could materially change the document. If the requester asks to draft before the process is complete, state one or two important consequences of the uncertainty, then follow the instruction.

## 5. Maintain an alignment ledger

Keep a compact working record:

- **Confirmed:** Choices explicitly made by an authorized decision-maker.
- **Source facts:** Claims established by current, authoritative evidence, but not selected as current choices.
- **Inferred:** Plausible interpretations that remain unconfirmed.
- **Open:** Questions that could materially change the document.
- **Corrected:** Assumptions or claims someone has rejected.

Update the ledger after every answer round. Never reintroduce a corrected assumption. If confirmed statements conflict, surface and resolve the conflict rather than hiding it in vague language. Never promote an inference to confirmed just because several sources support it.

For a full shaping process, show a concise version of the ledger before each later round. Every major draft claim must be a confirmed choice, a supported source fact, or explicitly framed as a proposal, assumption, or open question.

## 6. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document’s substance. Before drafting, provide a concise synthesis of the intended job, audience, central position, important boundaries, and deliberate open questions.

For every major planned claim, ask:

> Was this confirmed by an authorized decision-maker, established as fact by authoritative evidence, or merely inferred?

If a material claim is only inferred, ask another question or label it clearly as a proposal. Do not present it as settled.

Check that each relevant category is confirmed, evidence-based, deliberately open, or not applicable:

- Goal and audience.
- Artifact type.
- Central argument or bet.
- Scope and exclusions.
- Definitions and thresholds.
- Ownership and decision rights.
- Interfaces and handoffs.
- Success measures and evidence standards.
- Tone, length, format, and destination.

For persuasive documents, perform a skeptical-reader pass:

- What is the strongest likely objection from the real audience?
- Which premise, commitment, evidence claim, or safeguard would they dispute?
- Has the document’s response been confirmed?

Close alignment means remaining uncertainty is low impact or clearly represented as unresolved. It does not require artificial certainty.

## 7. Draft and deliver

Follow stated voice, style, accessibility, privacy, format, and delivery requirements. If no style is specified, use clear, direct language suited to the audience.

Write the smallest document that accomplishes the agreed purpose. Prefer clear claims, concrete decisions, named ownership, and explicit boundaries over polished but vague abstraction. Distinguish current decisions from proposals, assumptions, and future review points.

For action-oriented documents, avoid long flat inventories. Keep top-level bullet lists manageable, usually five or fewer and rarely more than seven. Combine related points, cut lower-value detail, or move support material to an authorized reference.

When delivering in a formatted document system, inspect the rendered result. Ensure headings after lists are separate non-list paragraphs, with no unwanted blank spacing, inconsistent indentation, orphaned bullets, or poor page breaks.

Use plain, natural writing:

- Prefer common words over inflated language.
- Write complete sentences without turning connected ideas into choppy fragments.
- State the point first and remove warm-up text, repeated context, and unnecessary qualifications.
- Turn abstractions into concrete claims, actions, owners, dates, examples, or tests where useful.
- Use focused paragraphs and bullets only for real lists.
- Be concise by removing unnecessary ideas and words, not by making every sentence short.
- Keep difficult ideas when they matter, but explain them plainly.

Honor the requested destination. If text is requested in the conversation, provide text without changing source material. If a document must be created or updated in another system, do so only as instructed and verify the intended content is present.

## 8. Audit before delivery

Compare the draft with the alignment ledger and source hierarchy:

- Does it solve the agreed problem in the agreed form?
- Does every material choice reflect confirmed decisions?
- Have corrected assumptions been removed?
- Are responsibilities, boundaries, decision rights, and handoffs unambiguous where relevant?
- Are uncertain claims labeled appropriately?
- Are factual claims and citations supported by appropriate sources?
- Is any inference presented as a settled fact or decision?
- Does the document match the requested voice, audience, and access boundary?
- Can each sentence be understood on the first read?
- Can any abstract phrase, inflated word, or repeated point be simplified or removed?

Fix mismatches before delivery. Put the deliverable last, without trailing commentary that interferes with copying or use.

## Failure modes to avoid

- Drafting early because producing text feels productive.
- Treating the proposed artifact as fixed before its purpose is known.
- Asking for facts that authorized evidence can answer.
- Accessing unnecessary private material or including unrelated sensitive details.
- Mistaking research volume for alignment on current choices.
- Treating a plausible synthesis as a confirmed decision.
- Using a generic questionnaire disconnected from evidence and prior answers.
- Failing to update the working model after each round.
- Stopping after one round without testing consequences.
- Bundling independent decisions into one question or repeating settled questions.
- Concealing contradictions through vague language.
- Continuing interviews after only low-impact uncertainty remains.
- Writing an inspiring document that leaves decisions, ownership, or execution unclear.
- Mistaking concise writing for choppy writing through fragments, noun-only bullets, or artificially short sentences.


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
description: Learn a paper, article, or topic through a short Socratic dialogue using retrieval, explanation, challenge, and application rather than passive summary.
---

# Learn with a tutor

Help a learner understand, retain, and use a paper, article, post, or topic through an active dialogue. Prioritize retrieval, explanation, and application over passive review. The learner should do most of the thinking; guide their reasoning, identify gaps, and calibrate challenge without turning the exchange into a test.

## Core learning principles

- **Retrieve before reviewing.** Do not give an unsolicited summary. Ask the learner to reconstruct ideas in their own words.
- **Probe mechanisms.** Ask why, how, under what conditions, and based on what evidence a claim holds.
- **Require generation.** Have the learner create their own examples, analogies, predictions, and applications before supplying yours.
- **Use productive difficulty.** Make questions demanding enough to require effort, but not so difficult that the learner cannot attempt an answer.
- **Practice transfer.** Ask the learner to connect ideas to unfamiliar settings, adjacent concepts, and practical decisions.
- **Surface inconsistencies.** Use focused questions to reveal incomplete reasoning before giving a correction.

## Workflow

### 1. Establish starting point and purpose

Begin by learning what the person already believes, knows, or has experienced about the topic. Ask what they want to achieve, such as explaining an argument, evaluating a claim, preparing for discussion, or applying a method.

Ask one or two open questions:

- “What do you already think is true about this topic, and what led you to that view?”
- “What would you like to be able to explain, evaluate, or do by the end?”

Use the response to choose an appropriate level and identify useful background knowledge or likely misconceptions.

### 2. Elicit the central idea from memory

Ask the learner to state the main claim, finding, or problem in their own language. Do not invite quotation or recitation.

Useful prompts:

- “What is the main claim in your own words?”
- “Why should someone believe that claim?”
- “What problem is this trying to solve?”
- “How would you explain this to a thoughtful friend in 30 seconds?”

If the learner has not yet engaged with the material, ask for their initial prediction or working model. Then have them inspect the relevant portion and return to recall.

### 3. Choose a few high-value ideas

Do not attempt to cover everything. Select two or three ideas that are central, difficult, consequential, or easy to misunderstand. Explore each idea using this cycle:

1. Ask the learner to reconstruct the idea.
2. Probe assumptions, evidence, causal reasoning, and limits.
3. Ask for a self-generated example, analogy, or application.
4. Test it with an objection, alternative explanation, or boundary case.
5. Adapt the next question to the learner’s response.

Keep turns short. Usually ask only one or two questions at a time.

## Question toolkit

Choose questions that require explanation rather than recognition:

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What is the mechanism, step by step?”
- “What evidence would distinguish this explanation from an alternative?”
- “Can you give a concrete example from a familiar setting?”
- “Where might this fail or stop applying?”
- “What is the strongest objection?”
- “How does this connect to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one assumption changed?”

Avoid yes-or-no questions unless they immediately require reasoning.

## Responding to answers

Be warm, rigorous, and specific. Avoid generic praise. When an answer is strong, identify what made it strong—such as naming an assumption, separating correlation from causation, or offering a relevant counterexample—then raise the level of challenge.

When an answer is inaccurate or incomplete:

1. Do not correct it immediately.
2. Ask a focused question that reveals the tension or missing step.
3. Allow one or two real attempts to work through it.
4. If the learner remains stuck, give a brief, direct explanation.
5. Ask them to restate the distinction in their own words or apply it to a new case.

If the learner says “I don’t know,” invite a low-stakes attempt: “Take a guess from what you do know. What seems most plausible, and why?” Give a hint after an attempt, or sooner when the missing foundation makes an attempt unreasonable.

## Calibration and progress checks

Increase difficulty when answers come easily: ask for a counterexample, prediction, comparison, or transfer to a new domain. Reduce difficulty when the learner is lost: narrow the question, isolate an assumption, use a simpler case, or ask them to compare two explanations and defend one.

Periodically provide a concise, evidence-based check:

- What the learner has demonstrated they understand.
- What remains shaky, incomplete, or uncertain.
- What to focus on next.

Do not treat recognition of a term or repetition of a conclusion as mastery. Look for accurate explanation, reasoning, and transfer.

Match the learner’s energy. If they are engaged, go deeper. If they are overloaded, consolidate what they have learned rather than introducing more material.

## Closing gate

Before ending, ask the learner to turn understanding into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation, a new example, or a question they should revisit later. State the most useful next concept or retrieval prompt.

## Guardrails

- Do not summarize unless the learner explicitly asks; even then, invite their own summary first.
- Do not lecture when a well-chosen question can prompt retrieval or inference.
- Do not define jargon automatically; ask the learner to define it first, then clarify if necessary.
- Do not make the exchange easy merely to be encouraging.
- Do not cover the whole source superficially when a few core ideas can be understood deeply.
- Keep the interaction a responsive dialogue, not a fixed quiz.


---
name: write-in-my-voice
description: Draft or revise email in the user’s authentic voice using authorized style evidence, accurate facts, and a concise final audit.
---

# Write in my voice

Use this workflow to draft, reply to, or revise an email on the user’s behalf. The goal is a copy-ready message that sounds recognizably like the user while remaining accurate, appropriate for the recipient, and clear about what happens next.

## 1. Gather authorized voice evidence

Use only sources the user has provided or authorized you to access, and only for the legitimate purpose of drafting this email. Read any current style guide in full. If needed, review a small number of recent sent emails that match the audience or purpose.

Do not expose, quote unnecessarily, or reuse unrelated private details from those sources. Extract a practical profile instead:

- Typical greetings and sign-offs.
- Formality, warmth, directness, and relationship cues.
- Usual sentence and paragraph length.
- Preferred wording, contractions, punctuation, and formatting.
- Patterns for requests, follow-ups, apologies, declines, feedback, and uncertainty.
- Language, tones, or formatting the user avoids.
- Approved reusable facts, links, boilerplate, and standard responses.

Recent, comparable sent messages are stronger evidence than old examples or generic writing advice. If evidence conflicts, ask which preference is current. If no evidence is available, use a concise, warm-professional default and invite the user to share examples for future drafts.

## 2. Confirm the brief

Identify the minimum information needed to send a safe, useful message:

| Needed information | Example |
|---|---|
| Recipient and relationship | A prospective client the user has not met before |
| Desired outcome | Confirm a meeting and request a document |
| Required facts | Date, link, attachment, decision, or deadline |
| Tone and stakes | Friendly, firm, sensitive, or formal |
| Approval limits | Whether the user must approve commitments before sending |

Ask a focused question only when missing information could materially change the message. Do not invent names, availability, prices, decisions, promises, links, attachments, opinions, or emotional reactions.

## 3. Adapt the voice to the situation

Voice is a pattern, not a rigid template. Keep the user recognizable while adapting to the recipient and stakes.

- For familiar colleagues, use the user’s normal concise and natural pattern.
- For new, external, senior, or sensitive recipients, preserve the voice while adding enough context and care to prevent ambiguity.
- For conflict, correction, or rejection, be factual and direct. Avoid defensive explanations, excessive praise, or apologies that the user did not intend.
- For requests, state the requested action, responsible party, and timing plainly.
- Use approved boilerplate, links, and factual details only when they fit the current context and remain accurate.

## 4. Draft the smallest complete email

Use this default structure unless the user’s evidence suggests another pattern:

1. Greeting, if normally used.
2. The purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Closing and sign-off, if appropriate.

Prefer concrete nouns, active verbs, short sentences, and short paragraphs. Put decisions and requested actions where the recipient can find them quickly. Use bullets only when they make options, actions, or logistics easier to scan.

Remove content that does not help the recipient understand or act, including:

- Process narration or explanations of how the draft was made.
- Generic praise, repeated thanks, or empty pleasantries.
- Filler such as “just wanted to” unless it is both natural to the user and useful.
- Hedging that weakens a clear message.
- Private or sensitive details that are not necessary for this recipient.

## 5. Audit before presenting

Review the draft line by line:

- Does it plausibly sound like the user?
- Do greeting, sign-off, punctuation, rhythm, and formality match the evidence?
- Is the tone appropriate for this recipient and situation?
- Are all names, dates, links, attachments, and references accurate?
- Did the draft add any unsupported commitment, claim, opinion, or emotion?
- Is the requested action and deadline unmistakable?
- Can any sentence be removed without losing meaning?
- Does the draft stay within the user’s intended access and privacy boundary?

## Output

Provide the final email as copy-ready text. If clarification is required, ask only the specific question needed to draft safely. Do not add commentary after the email unless the user asks for alternatives, explanation, or revision.


---
name: professional-social-post
description: Draft, revise, and audit professional social posts from source material using strong hooks, supported claims, useful substance, and targeted editing.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, an existing draft, an article, transcript, podcast, report, research finding, campaign brief, or a simple topic.

The aim is not to make an organization sound enthusiastic about itself. The aim is to make the right reader stop, understand a useful point, and have a reason to care. A good post is specific, defensible, easy to scan, and useful even if the reader never follows a link, opens a document, or buys anything.

This workflow is platform-independent. Adapt formatting, length, link treatment, and publishing mechanics to the user’s chosen platform. Do not assume that a tactic, timing window, or format will improve distribution without testing it against the user’s own results.

## Start with a brief

Before drafting, confirm enough of the following to make sound choices. Ask only for what is missing or materially unclear.

- **Platform and format:** Text post, caption, document carousel, thread, video caption, or article promotion.
- **Audience:** Technical practitioners, founders, researchers, policy professionals, customers, candidates, peers, or another defined group.
- **Purpose:** Share an insight, explain a concept, announce a change, promote a longer piece, invite substantive discussion, or support a campaign.
- **Voice:** First-person or organizational voice; formal, conversational, concise, analytical, skeptical, or another specified style.
- **Length and constraints:** Target word count, required facts, banned phrases, punctuation preferences, and whether emojis or special text formatting are acceptable.
- **Evidence and permissions:** Source material, data, approvals, attribution requirements, and what personal or confidential information may be disclosed.
- **Call to action:** Whether the post should invite discussion, point to a resource, ask for a next step, or end without a question.
- **Link strategy:** Whether a link is needed and where the selected platform treats links best.
- **Delivery format:** Whether the user wants the complete draft in chat, copy-ready text, or content prepared for their chosen document or publishing system.

If the user has approved examples, a brand guide, audience research, or a writing guide, use those as evidence of voice. Do not assume one person’s preferences apply to every user.

## Privacy, permission, and source boundaries

When a post draws on private communications, participant records, client material, employee information, or other non-public sources, confirm a legitimate purpose and clear authorization before using that material publicly.

Use only the minimum relevant information. Omit unrelated personal details, sensitive facts, and identifying details that are not necessary to support the point. Respect consent, confidentiality commitments, and the access boundary of the source material.

For a career, participant, customer, or employee story, ask:

1. Is the person comfortable being named, quoted, or pictured?
2. Which facts are approved for public use?
3. Is the claimed outcome documented and attributable?
4. Can the person review a direct quote or sensitive characterization where appropriate?
5. Can the lesson be told with fewer identifying details?

If approval is absent, use an anonymized, non-sensitive example only when it remains accurate and the user has permission to use it. Do not imply that an organization, person, or program caused an outcome unless the evidence supports that conclusion.

## Route the request before drafting

Some post types need a distinct structure. Identify the genre before choosing hooks or writing copy.

| Post type | Best starting approach |
|---|---|
| Career or participant story | Use starting point, turning point, concrete outcome, evidence, and lesson. Obtain permission for personal details. |
| Research or evidence post | Lead with the finding, explain the method or source, state important uncertainty, then give the implication. |
| Product or organizational announcement | Lead with the concrete change and reader relevance, not internal excitement. |
| Article, report, or podcast promotion | Lead with the strongest insight from the piece, not “new article” or “new episode.” |
| Carousel or document caption | State the central idea and one or two meaningful specifics, then explain what the visual material adds. |
| Hiring or assessment post | Describe role-relevant capabilities, role alignment, diagnostic evidence, and whether the assessment distinguishes relevant performance. |

If the genre is unclear, ask one short routing question. Do not force a career story into a generic promotional format, and do not turn a research finding into a personal anecdote unless the source supports that framing.

## Accuracy rules

These rules apply to every draft.

1. **Do not invent facts.** Never fabricate statistics, names, quotes, organizations, roles, dates, research findings, testimonials, or outcomes.
2. **Separate evidence from interpretation.** Say what the source establishes, then identify the conclusion, recommendation, or opinion drawn from it.
3. **Keep meaningful uncertainty.** If a claim has broad ranges, major assumptions, weak evidence, or correlation rather than causation, state that plainly.
4. **Use supported specificity.** Exact details are usually stronger than broad wording, but do not turn an estimate into false precision.
5. **Request missing evidence early.** If the post depends on an unsupported claim, ask for a source, remove the claim, or narrow it.
6. **Avoid manufactured urgency.** A specific risk with a practical response is more credible than sweeping catastrophe language.
7. **Protect context.** Do not selectively quote or present a result in a way that changes its meaning.
8. **Keep claims defensible in public.** A knowledgeable reader should be able to see the source, scope, caveat, or reasoning behind any material claim.

## Audience and voice

Write for the reader most likely to act on, learn from, or meaningfully discuss the post. Trying to appeal to everyone often produces vague language that appeals to no one. Specificity is useful because it helps the intended audience recognize that the post is for them.

Default voice, unless the user specifies otherwise:

- Direct, clear, and conversational.
- Short sentences with concrete nouns and plain verbs.
- Active voice where practical.
- One main claim per sentence.
- Sober about problems and practical about responses.
- Confident only to the degree the evidence permits.
- Specific rather than promotional.

Avoid these common failures:

| Failure mode | Typical symptom | Better approach |
|---|---|---|
| Corporate | “We are thrilled to announce an exciting initiative.” | State what changed, who it affects, and why it matters. |
| Academic | Dense jargon and long qualifications before the point. | State the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Broad danger language without mechanism, evidence, or response. | Name the risk, evidence, uncertainty, and proportionate intervention. |
| Generic inspiration | Positive language without a decision, mechanism, or example. | Name the concrete action, trade-off, or result. |

## Core workflow

### 1. Inspect the source before selecting an angle

Do not start by filling a template. Read the source and find the strongest material inside it. The headline of an article is often not the strongest social-post angle.

Look for:

- An unusual fact or surprising number.
- A counterintuitive conclusion that can be defended.
- A concrete outcome or before-and-after change.
- A useful framework, checklist, or decision rule.
- A meaningful strategic trade-off.
- A sharp disagreement between credible views.
- A clear mechanism that changes how readers understand a problem.
- A sentence that turns a broad issue into a specific question.

If several strong angles exist, do not silently choose one. Show two to four numbered options and explain what each would foreground. Then ask the user to select one, unless they have explicitly delegated the choice. If they delegate, recommend one and state why it best matches the stated audience and purpose.

> I see several viable angles. Which should lead?
>
> 1. **[Angle]**: Foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: Foregrounds [story, outcome, or disagreement]. Best for [audience intent].
> 3. **[Angle]**: Foregrounds [framework or implication]. Best for [audience intent].

Choose one primary thread. A post should not attempt to summarize every section of a report, interview, or episode.

### 2. Generate hooks before drafting the body

The opening determines whether the reader sees the rest. Generate five to ten hooks internally. When user judgment would help, present a numbered shortlist of three to five, each with a brief note about its strategy. Do not commit to the first acceptable hook merely because it is grammatical.

Useful patterns include:

- **Changed mind:** “I changed my mind about [specific issue].”
- **Concrete investment:** “I reviewed [specific evidence] to answer one question.”
- **Specific number with tension:** “[Number] of [group] report [surprising result].”
- **Named outcome:** “[Person or role] moved from [starting point] to [specific outcome] in [timeframe].” Use only with evidence and permission.
- **Counterintuitive claim:** “[Common assumption] misses the more important problem.” Use only if the body supports it.
- **Short thesis:** “[Concept] is best understood as [concrete analogy].”
- **Focused disagreement:** “Why do two credible groups reach such different conclusions about [specific issue]?”

Use this presentation format when offering options:

| Hook | Strategic purpose |
|---|---|
| “[Specific claim or finding].” | Leads with a concrete result and creates an honest reason to continue. |
| “[Counterintuitive, defensible claim].” | Creates tension by challenging a familiar assumption. |
| “I changed my mind about [specific topic].” | Uses personal stakes when the source includes a genuine updated view. |

Use the swap test: if the main noun can be replaced with an unrelated field and the hook still works, it is probably too generic. Make the hook specific to the actual topic.

Avoid generic announcements, throat-clearing, empty cliffhangers, multiple rhetorical questions in a row, broad motivational claims, and clickbait promises the body cannot fulfill. The first visible lines should make an honest promise that the rest of the post delivers.

### 3. Choose one structure

Pick the structure that best fits the source. Do not combine several structures unless there is a clear reason.

1. **Counterintuitive claim → evidence → implication** for research, data, and argument posts.
2. **Changed mind → trigger → updated view → takeaway** for reflective first-person posts.
3. **Problem → why it matters → practical response** for explainers and operational or policy content.
4. **Result → how it happened → reusable lesson** for launches, case studies, and concrete outcomes.
5. **Framework → examples → application** for reference-style posts readers may save.
6. **Specific announcement → reader relevance → next step** for genuinely notable announcements.
7. **Strategic trade-off → rationale → consequence** for explaining a deliberate constraint or anti-goal: something an organization intentionally does not optimize for.

### 4. Draft: hook, tension, payoff

Use this default shape:

- **Hook:** The strongest claim, result, or tension.
- **Tension or setup:** Why it matters, what makes it surprising, or which assumption it challenges.
- **Payoff:** The evidence, story, framework, or practical insight.
- **Soft close:** Exactly one focused question, one takeaway, or one pointer to further material.

Default to fewer than 300 words unless the content needs more space. Every extra line should earn its place. Use one- or two-sentence paragraphs for mobile scanning. Use bullets only when the content is genuinely list-shaped, such as findings, a checklist, or distinct options.

For carousel captions, give readers a complete central idea and one or two strong details. Explain what the visual material adds, but do not duplicate every slide. For linked articles, reports, or podcasts, put the primary insight in the post and treat the linked item as depth, sources, examples, or full methodology. For an interview or guest episode, lead with the strongest relevant insight or documented outcome, not the fact that an episode exists.

### 5. Add one close, not several

Use one close only. A strong close creates a real and bounded response space.

Good examples:

- “Which constraint matters most in your work?”
- “What evidence would change your view?”
- “The full analysis includes the assumptions and source material.”
- “If you have operated this kind of system, where does this model fail?”

Avoid “Thoughts?”, multiple questions, and requests to comment, tag, repost, or react purely to increase reach. Ask for knowledge, disagreement, or experience, not performative engagement.

## Platform and formatting checks

Check the chosen platform before using formatting conventions. Some platforms do not render Markdown, while others treat special Unicode characters, long captions, links, line breaks, headings, or alt text differently.

- Use the platform’s native formatting where available.
- Do not rely on asterisks, underscores, or other Markdown markers unless the platform renders them.
- Use emphasis sparingly. One or two emphasized phrases are normally enough.
- Prefer periods, commas, and line breaks over theatrical punctuation unless the user has a clear preference.
- Follow the user’s link strategy. If the platform strategy uses a first comment or reply, prepare that text separately from the post body.
- For image, document, or video posts, ensure the caption provides value independently of the asset.
- If accessibility text is supported, suggest concise alt text that describes essential visual information rather than decorative details.

## Editing pass: remove inflated language

After drafting, do a separate editing pass. Replace phrases that sound polished but do not add meaning.

Cut or rewrite corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “empower”; filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably”; and empty hedges such as “it is worth noting” or “one might say.” Cut softenings such as “just,” “simply,” “essentially,” and “ultimately” unless they change meaning.

Replace abstract nouns such as “journey,” “transformation,” and “paradigm” with concrete events where possible. Delete transition sentences that only restate the previous paragraph. Remove dramatic frames such as “The truth is” and state the point directly. Read the post aloud: if it sounds like reusable thought-leadership copy rather than a person making a specific point, rewrite it.

## Revision protocol

When the user gives feedback, revise the flagged line and its nearby logic first. Do not rewrite the entire post unless asked.

- If the hook is weak, offer several replacement hooks before rebuilding the body.
- If a claim is overstated, improve the evidence, qualify only that claim, or remove it.
- If a paragraph feels slow, cut setup before adding explanation.
- If an earlier sentence was sharper, preserve it unless the user asks to change it.
- If a section is weak because the source lacks support, say so and offer a concrete alternative.
- If the user asks for small edits, retain the established structure and strongest lines rather than silently reverting to weaker language.

Multiple small options are often more useful than one full redraft, especially for hooks, closers, and uncertain lines. Be candid about a soft spot instead of presenting weak copy as finished.

## Readiness gate and audit

Do not present a post as final until it passes this checklist:

- Does the first line earn attention when read alone?
- Does the post make one clear point rather than several competing points?
- Is there a concrete detail, mechanism, outcome, example, or number where appropriate?
- Could a knowledgeable reader challenge the claim, and can the post support it?
- Does it provide value without requiring a click, swipe, purchase, or sign-up?
- Is important uncertainty stated?
- Is the language specific to this topic rather than reusable across any industry?
- Is the close one focused action, question, or pointer?
- Are every name, quote, figure, and claim supported and approved for public use?
- Does formatting work on the intended platform?
- Does the tone remain respectful, professional, and appropriate for the intended audience?
- Are private, sensitive, or identifying details omitted unless necessary and authorized?

If any answer is no, revise before handoff.

## Handoff format

Present only what the user needs to decide and publish:

1. The recommended hook and one or two alternatives, each with a brief strategic note.
2. The completed draft in the user’s chosen delivery format.
3. Any unsupported claim, missing input, permission concern, or uncertain line.
4. Suggested link, reply, or first-comment text when relevant to the platform strategy.
5. A concise publishing reminder appropriate to the platform, such as responding promptly and substantively to genuine early comments.

Do not promise that a format, timing tactic, or engagement metric will improve distribution. Treat publishing tactics as testable hypotheses and compare results across several posts.

## Common failure patterns

- **Announcement disguised as content:** The post says the organization is pleased but gives readers no reason to care. Lead with the change or lesson.
- **Pure teaser:** The post demands a click but provides no insight. Share the central finding and use the resource for depth.
- **Unsupported precision:** A striking number lacks source, scope, or caveat. Verify, qualify, or remove it.
- **Overpacked summary:** The post covers every section of the source. Select one thread and save the rest for another post or the original material.
- **Bolted-on promotion:** A course, product, or service appears without a natural connection. Remove it, make a separate post, or state the immediate relevance.
- **Forced engagement:** The post asks for reactions rather than inviting informed discussion. End with one real question or useful conclusion.
- **Overconfident case study:** A personal outcome is presented as universal proof. State the evidence, respect consent, and avoid unsupported causal claims.
- **Formatting mismatch:** The copy relies on formatting the target platform does not support. Convert it to plain, readable text or native formatting.

The final standard is simple: the post should sound like someone with evidence, judgment, and a real point to make. It should not sound like a press release, an academic abstract, or a generic social-media template.


---
name: case-study-post
description: Create an evidence-based case study post with verified story beats, alternate hooks, approved quote-card options, and a clear reader action.
---

# Write a case study post

Use this workflow to turn authorized material about a person’s professional, educational, or career change into a concise public case study. It works for a social post, newsletter, community update, program story, recruitment page, or similar format.

The goal is not to make the subject sound impressive through vague praise. Show a credible change: where they started, what they were considering, why they acted, what concretely helped, what happened next, what they do now, and what the reader can do next.

A strong case study helps the intended reader recognize their own situation in the subject’s before-state. It explains the role of a course, community, event, service, mentor, or resource accurately, without claiming it caused more than the evidence supports.

## Scope, authorization, and privacy

Create a case study only for a legitimate publishing purpose and with clear authorization to use the source material. Private interviews, applications, internal messages, meeting notes, recordings, and personnel records are research material, not automatically publishable content.

Use the minimum information needed to tell the story. Respect the subject’s consent, reasonable privacy expectations, and the access boundary of the intended publication. A post for a private member community may use different approved detail than a broad public post.

Do not include unrelated personal details or sensitive information unless it is necessary, authorized, and approved for public use. This includes contact details, compensation, health, family, legal or immigration circumstances, confidential employer information, unpublished work, and personal matters unrelated to the case study.

Before publication, confirm:

- Who may approve the post.
- Whether the subject has reviewed sensitive claims and direct quotes.
- Which names, roles, affiliations, team descriptions, dates, outputs, and figures may be public.
- Whether the post is for a limited audience or broad public distribution.
- Whether the stated outcome is still current and accurate.

When authorization or approval is unclear, omit the detail or ask a focused question. Do not infer consent merely because you can access a private record.

## Inputs and intake gate

Gather all available authorized material before drafting. Useful sources include:

- An interview transcript, recording notes, or meeting summary.
- A written application, intake form, or reflection from the subject.
- An approved professional biography or current profile.
- Official public announcements, work samples, publications, or project descriptions.
- An internal note identifying a possible outcome, subject to verification.
- A rough outline, previous draft, or notes from the subject.
- The target audience, publishing channel, desired result, and call to action.
- An editorial, brand, or author voice guide.

Before writing, verify that you have enough information for the following fields. Do not guess at names, titles, dates, figures, timelines, outcomes, or public affiliations.

| Field | What to capture |
|---|---|
| Subject | Public name, preferred references, and consent status. |
| Before-state | Previous role or context, goal, uncertainty, and reader-relevant constraint. |
| Alternative path | What they were considering or doing instead, when it helps the reader relate. |
| Trigger | Why they joined, applied, changed direction, or acted then. |
| Intervention | The program, community, event, mentor, service, or resource involved. |
| Mechanism | Concrete help, such as a realization, opportunity, introduction, feedback session, or conversation. |
| Now-state | Current role or activity, practical work, and an approved meaningful output. |
| Timeline | Start point, outcome point, and any truthful compressed timeframe. |
| Evidence | Verified facts, approved names, figures, artifacts, and direct quotes. |
| Cost or risk | A career tradeoff, move, pay change, uncertainty, or other relevant cost, if approved. |
| CTA | The action the intended reader should take next. |

If a critical field is missing, ask focused questions before drafting. Useful questions include:

1. What was the person doing before this experience?
2. What were they considering instead?
3. Why did they take part or make a change at that point?
4. What were the one or two specific things that helped them move forward?
5. What happened next, and when?
6. What do they do now in practical terms?
7. Is there an approved public project, publication, product, placement, or result that can be named?
8. Did they take a meaningful cost or risk they are comfortable sharing publicly?
9. Which claims, figures, names, and quotes have explicit approval?
10. Who should this post persuade, help, or invite to act?

## Evidence and verification rules

Never invent facts or strengthen a claim for punch. If a source says someone contributed to a project, do not call them its lead. If they explored an opportunity, do not write that they received it. If a source is tentative, retain that uncertainty or verify the claim elsewhere.

Automated transcripts and summaries are useful but fallible. They can mishear names, technical terms, job titles, dates, figures, and titles. Cross-check important details against a more reliable source before publication.

Use this default reliability order:

1. Direct, recent confirmation from the subject.
2. Official public records, announcements, or published work.
3. A current approved professional profile or biography.
4. The subject’s original written application or reflection.
5. An interview transcript or automated meeting summary.
6. An informal third-party message.

When sources disagree, resolve the conflict before drafting or omit the disputed detail. Do not select the more dramatic version.

In working notes, classify every important claim:

- **Verified fact:** Supported by a reliable source.
- **Subject interpretation:** What the person says helped them or changed their mind.
- **Editorial inference:** A conclusion drawn from the story. Use sparingly and only where evidence supports it.

Do not say an intervention caused an outcome unless that causal claim is well supported. Prefer precise statements such as “the program helped them understand the field,” “they found the opportunity through the community,” or “a conversation clarified their next step.”

## Sensitive-content approval gate

Flag these for explicit subject approval before publishing:

- Compensation, pay reductions, financial hardship, or salary comparisons.
- Health, family, legal, immigration, or other sensitive personal circumstances.
- Harsh criticism of a past employer, team, role, or career decision.
- Confidential work, unreleased projects, or unpublished titles.
- Direct quotes, especially sharp opinions, criticism, or strong language.
- Claims about why an employer or assessor selected the person.
- Exact dates or timeline details that could reveal private circumstances.
- Causal claims about a program, organization, or individual.

If approval is unavailable, replace the claim with an approved, truthful fallback or cut it. Do not conceal uncertainty by making the story more dramatic.

## Build the story beats

Create a concise working outline before writing. Keep raw personal details out of the delivered draft unless they are relevant and approved.

### 1. Before-state

Capture the subject’s role, background, and reader-relevant uncertainty. Include an alternative path when it mirrors the target audience’s current life, such as staying in an established role, building a product, continuing research, or pursuing a different field.

Cut biography that does not move the story. Keep a detail only when it explains the decision, makes the change concrete, or helps the reader recognize themselves.

### 2. Trigger

Identify why the person acted then. Common triggers include testing whether a field was accessible, finding collaborators, improving a practical skill, solving a problem, or making a values-driven career change.

### 3. Mechanism

Find one or two observable events that changed the trajectory. Strong mechanisms include:

- Realizing that a field or role was open to their background.
- Finding a relevant opportunity through a community.
- Receiving feedback that improved an application or project.
- Having a specific conversation or introduction.
- Attending a workshop that clarified a practical next step.

Avoid “the experience was transformative.” State what happened instead.

### 4. Now-state

Record the current role or activity and what the person actually does in understandable terms. Translate specialized jargon enough for the target audience to understand the work and why it matters.

Use one meaningful output when it adds proof: a project, publication, placement, grant, product, or public result. Avoid resume-style piles of credentials.

### 5. Timeline and compression

Map the sequence from joining or starting to the outcome. Use a compressed timeframe only when it is exact, approved, and useful. Do not force speed as the story if the evidence does not support it.

### 6. Quotes

Pull three to five candidate quotes verbatim. Favor lines that speak to the reader’s identity, uncertainty, or decision rather than only celebrating the subject’s result.

Choose candidates in these categories:

1. **Discovery:** The person did not know a path was open to them.
2. **Mechanism:** A concrete resource, opportunity, or conversation helped them act.
3. **Conviction:** The person explains why the choice mattered or why they would make it again.

Light trimming is allowed only when it preserves the speaker’s meaning and grammar. Never rewrite a quote into a stronger claim.

## Generate three hook options

For feed-based posts, the first two lines often determine whether readers continue. Draft three distinct hooks before writing the post. Keep each to two short sentences. Around 140 characters total is a useful default when the channel rewards brevity.

### Hook A: Discovery

Use when the target audience shares the subject’s former blocker.

**Formula:** The subject did not know or believe a relevant possibility. Soon afterward, they reached a specific outcome through a concrete mechanism.

This is the default recommendation when the reader is likely to think, “That could be me.”

### Hook B: Identity collision

Use when the before-and-after contrast is vivid.

**Formula:** A short time ago, the subject was doing a specific thing. Today, they are doing a sharply different specific thing.

This works well for broad audiences or especially clear career changes.

### Hook C: Stakes-led

Use only when a meaningful cost or risk is approved and the audience will read it as honest conviction, not as a warning that participation requires sacrifice.

**Formula:** The subject accepted a specific cost to do something. Now they are doing meaningful, concrete work.

Choose one recommendation. Give one sentence explaining why it fits the audience, plus a short reason for not choosing each alternative. Default to Hook A when in doubt.

## Draft the full post

Aim for approximately 160 to 220 words unless the channel requires another length. Shorter is usually stronger.

Use this sequence:

1. **Hook:** Use the recommended option.
2. **Before-state:** One short paragraph showing the previous situation and, if useful, the relatable alternative path.
3. **Name the intervention:** Clearly state that the person joined the program, attended the event, used the resource, or entered the community. Do not leave this implicit.
4. **Mechanism and outcome:** Explain the concrete turning points, then land the immediate result plainly. A short outcome line can work well.
5. **Current work:** Describe what they do now in language the reader can understand.
6. **Optional cost:** Include only when approved and genuinely useful.
7. **Optional pull quote:** Include only if it adds a distinct truth not already carried by the hook or body.
8. **CTA:** Address the reader directly and give one clear next action.

If the selected channel tends to reduce distribution of posts containing external links, use an approved destination such as a comment, profile destination, or follow-up message rather than putting the link in the post body. Confirm current channel practice instead of treating it as universal.

## Style rules and anti-template pass

Apply the chosen voice guide. If none exists, use these defaults:

- Use short paragraphs and generous whitespace.
- Write direct declarative sentences.
- Prefer simple past tense where possible.
- Use specific names, roles, dates, figures, and artifacts only when verified and approved.
- After the first full introduction, use the subject’s preferred short name if it suits the publication and they consent.
- Prefer plain verbs over corporate language.
- Let evidence create admiration. Avoid unsupported praise such as “brilliant,” “exceptional,” or “inspiring.”
- Use contractions when the voice is conversational.
- Keep the CTA in full second person.
- Avoid emojis unless they are an explicit brand choice.
- Avoid em dashes by default. Use periods, commas, or line breaks instead.

On the final pass, cut common machine-like patterns:

- Transition lines that merely repeat the prior paragraph.
- Slow date-first openings when an identity or claim is stronger.
- Corporate verbs such as “leverage,” “unlock,” “harness,” “navigate,” and “empower.”
- Filler intensifiers such as “truly,” “deeply,” “incredibly,” and “remarkably.”
- Abstract nouns replacing evidence, including “journey,” “transformation,” and “paradigm.”
- Hedges such as “it is worth noting” or “arguably.”
- Softeners such as “just,” “simply,” “essentially,” and “ultimately.”
- Balanced constructions such as “on one hand, on the other hand.”
- Dramatic colon frames such as “The truth is:”.
- Reflective summary sentences after the CTA.

Read the post aloud. If it sounds like a generic thought-leadership template, shorten it and replace abstractions with concrete facts.

## Graphic quote options

Provide three visual quote-card options. Each should be self-contained, preferably under 15 words, and taken verbatim from approved material.

Provide one from each category:

- Discovery.
- Mechanism.
- Conviction.

Recommend one with a one-sentence rationale. Discovery quotes are often strongest because they make sense without surrounding context and mirror the reader’s uncertainty. Choose a mechanism or conviction quote only when it is clearer and more memorable on its own.

## Readiness audit

Before sending the draft for review, confirm:

- Every name, role, date, figure, title, and artifact is verified.
- Important transcript-derived details have been cross-checked.
- The post shows a concrete mechanism, not only a result.
- It does not overstate causation.
- The intervention is named clearly.
- The hook reflects a genuine audience concern.
- Current work is understandable to the intended reader.
- Sensitive claims and direct quotes are flagged for approval.
- The CTA is clear and aimed at the intended reader.
- The post contains no unsupported superlatives, generic filler, corporate phrasing, or unnecessary em dashes.
- The publication is within the approved audience and access boundary.

## Delivery and iteration

Create the draft in the user’s chosen document system when available. Use a clear, searchable title format:

`YYYY-MM-DD: Case study post, [Subject first name]`

In the accompanying message, provide only:

- The recommended hook and two alternatives.
- Three graphic quote options and the recommendation.
- Items needing subject approval.
- Missing information that would strengthen the post.
- The document location or link, when applicable.

Do not treat the first draft as final. If asked to make the hook better, generate three new hooks rather than making a minor edit. If asked to shorten the post, cut secondary biography first while preserving the mechanism and outcome. If a subject rejects a sensitive line, use the approved fallback without weakening the entire story.

After the final draft is accepted, review feedback for reusable lessons. Update the workflow only when a recurring pattern is clear, such as a missing intake question, repeated voice preference, recurring structural edit, or repeated verification issue. Do not invent process changes from a clean review cycle.


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
description: Review a month with evidence, identify structural lessons, and create a small, capacity-checked next-month plan that the user explicitly approves.
---

# Review and plan a month

Use this workflow at a month boundary to close a review period honestly and create an executable plan for the next period. A complete session normally takes 45–75 minutes: about half for evidence and review, and about half for planning.

Keep review and planning together. The next plan should directly respond to the structural reason a commitment slipped, an energy drain appeared, or a result was delivered. Do not turn this into a long retrospective, a task dump, or a generic productivity exercise.

## Purpose

The workflow produces:

- An evidence-based **Review** of the period ending.
- A direct view of progress toward active commitments and longer-range goals.
- A concise picture of selected delivery, personal-practice, and wellbeing signals.
- A **Plan** for the period starting, with a memorable theme, up to three outcomes, explicit trade-offs, and a pre-mortem.

Gather, discuss, and save only information that supports those outputs.

If the workflow accesses calendars, journals, health records, work systems, or records that concern other people, first ensure there is a legitimate purpose and clear authorization. Use the minimum relevant sources, fields, and date range. Do not include unrelated personal details in summaries or saved records. Keep the output within the intended access boundary.

## When to run it

Run this workflow when the user asks for a monthly review, asks to plan a named month, or asks to close one month and start another.

Default timing:

- During the first three days of a month, review the prior calendar month and plan the current month.
- At other times, review the current month to date and plan the next month. Label this clearly as a partial-month review and state the days remaining.
- If the user asks only for forward planning, normally review first because the evidence should shape the plan. The user may explicitly choose to skip the review.

State the ranges before gathering evidence:

> Reviewing **March 2026** (01 Mar–31 Mar). Planning **April 2026**.

Ask whether the user means calendar months or a practical planning range that includes an overlapping partial week. Record the actual planning range in the plan.

## Operating rules

1. **Read first; discuss second.** Show the factual picture before asking reflective questions.
2. **Batch independent reads.** Gather independent evidence in one initial pass whenever the chosen system supports it. Do not repeatedly interrupt the conversation for small lookups.
3. **Use live commitments.** Assess results against the user’s current target, not an old schedule, obsolete scope, or stale goal record.
4. **Check data quality before a harsh verdict.** Missing entries, delayed syncing, and incomplete logs can distort the picture. Ask the user to confirm a surprising result before treating it as complete truth.
5. **The user chooses.** The assistant calculates, summarizes, identifies constraints, and asks hard questions. The user chooses priorities, cuts, and commitments.
6. **One decision at a time.** Do not move to the next planning decision until the current question has a substantive answer.
7. **Stay at month altitude.** Define outcomes, milestones, capacity, structure, and commitments. Leave detailed week-by-week task allocation to a separate weekly process.
8. **No saved plan without explicit approval.** Notes, voice recordings, brainstorms, and imported lists are candidate inputs, not confirmed decisions. The user must restate or materially confirm the theme and commitments, then explicitly approve the plan.
9. **Use explicit dates.** Use **DD MMM** format unless the user chooses another unambiguous format.
10. **Keep records useful, not exhaustive.** Save decisions, evidence, constraints, and commitments rather than a transcript.
11. **Do not lecture.** For training, health, recovery, or personal practice, present the evidence, a direct conclusion, and the agreed next commitment. Give specialist guidance only when requested and appropriate.

## Step 1: Determine the range and gather evidence

Determine the review month, comparison month, and planning month. Then gather independent evidence in one initial batch using the user’s chosen system. This may be a project tracker, task manager, calendar, spreadsheet, notes system, activity log, health tracker, or a short inventory supplied by the user.

Never imply that an unavailable source was checked. If there are no connected records, ask for a factual inventory rather than inventing completeness.

| Evidence area | Gather in the initial pass |
|---|---|
| Previous monthly record | Theme, promised outcomes, commitments, and prior review findings. |
| Weekly records | Plans and reviews in the review range; repeated blockers, milestones, and carried work. |
| Goals | Active weekly, monthly, quarterly, and annual goals; status, deadlines, and notes. |
| Work delivered | Completed tasks, decisions, projects, or deliverables, grouped into useful domains. |
| Calendar | Next-month unavailable periods, fixed deadlines, recurring commitments, and meeting-heavy weeks. |
| Daily signals | User-selected ratings, focus time, habits, or brief written reflections. |
| Sleep and recovery | Optional duration, quality, and same-source recovery trends. |
| Training or practice | Optional sessions from the review and comparison months, plus the current commitment or schedule. |

For large sources, request computed statistics and a few representative themes rather than raw records. A full month of diary text or event detail can consume attention without improving the plan.

If a separate analyst or automated summary capability is available, give it a narrow authorized brief: inspect only the specified source and date range, return aggregates and planning-relevant patterns, and omit unnecessary detail. For a calendar summary, request only:

- Fixed multi-day commitments or unavailable periods.
- Approximate meeting load by week.
- Important recurring commitments.
- Protected personal commitments, described only as broadly as needed.
- Planning anomalies, such as events inside unavailable periods or likely time-zone errors.

Before detailed planning, re-read any weekly plans overlapping the start of the new planning range. Reconcile them with the month outcomes. The monthly plan should reference detailed weekly work where appropriate, not duplicate or overwrite it.

## Step 2: Show the evidence picture

Present a compact factual picture before asking the user to explain it. Be direct, numeric where useful, and concise.

### Personal-practice, training, or health verdict

If the user has a current commitment in this area, include it unless the user explicitly puts it out of scope. Compare actual activity with the live target.

Depending on the domain, calculate:

- Total volume, sessions, repetitions, or practice instances.
- Average weekly volume.
- Number of active days.
- Completion of key sessions or milestones.
- Longest gap between sessions.
- Relevant balance measures, such as routine versus demanding sessions, when records support them.
- Relevant performance or recovery measures.
- Change from the comparison month.

Use this verdict taxonomy when it fits:

- **ON TRACK:** Key measures meet at least 90% of target and consistency is intact.
- **BEHIND:** A key measure is about 60–90% of target, or there was a meaningful consistency break.
- **OFF TRACK:** A key measure is below 60% of target or there was a prolonged gap.
- **AT RISK:** A safety concern, injury signal, burnout signal, or sustained decline makes the current approach unsafe or unlikely to work.

Adjust thresholds only when the user’s domain requires different thresholds, and state the adjustment. If records may be incomplete, ask: “The record shows this. Does that match reality?” before issuing a strong verdict.

State the single biggest corrective action for the new month. It must be a measurable commitment, not a full program or a lecture.

### Goals and delivery

Summarize weekly commitments as completed, missed, deferred, or rolled forward. For every active longer-range goal, state whether it **advanced**, **stalled**, or **regressed**, with one short reason. Explicitly name goals that received no meaningful attention; they are usually most at risk.

Also summarize completed work in a few useful domains. Avoid a wall of tasks. The question is whether effort produced intended progress.

### Life signals

Include only measures the user chooses to track. Useful measures include a rating distribution and average, focused-hours average, low-focus days, sleep duration, sleep quality, same-source recovery trends, and repeated themes in written reflections.

Flag meaningful patterns, including low average sleep, repeated short nights, several consecutive low-rating days, extended low-focus streaks, or a mismatch between positive ratings and written reflections describing exhaustion or strain. Averages are signals, not the whole truth; raise a meaningful mismatch directly and briefly.

## Step 3: Reflect on the month

Open with one specific observation grounded in the evidence. Ask one question at a time. Pursue no more than two or three threads unless the user asks for a deeper review.

Cover these questions before closing the review:

1. What genuinely shipped and feels like a win?
2. What cost more time or energy than it returned?
3. Was the main miss structural, circumstantial, or a real priority change?
4. What one behavior, boundary, or pattern must change next month?
5. If a personal practice is in scope, what is the concrete commitment for the new month?

Useful prompts:

- “This outcome slipped across several weeks. What made it structurally hard to complete?”
- “The numeric ratings were stable, but the written reflections repeatedly mention strain. What was happening?”
- “This goal moved while others did not. What conditions made that possible?”

For a time-constrained user, the minimum viable review is: the in-scope practice verdict, any material wellbeing flags, one structural fix, and one concrete next-month commitment.

## Step 4: Plan the new month

A plan is not a description of events plus optimistic targets. A real plan contains a defined outcome, an honest baseline, a path, proof of capacity, explicit trade-offs, forcing functions, a pre-mortem, and approval.

### Move 1: Define outcomes

For every candidate priority, ask:

> What specifically is true by the final day of this planning range?

Make the answer measurable or plainly verifiable. Limit the plan to three outcomes; one or two is usually better. Each should connect to a longer-range goal or an explicitly chosen responsibility.

### Move 2: Establish current state

Size the gap with evidence, not mood. Inspect the relevant draft, backlog, milestone, pipeline, baseline metric, or other domain-specific reality. If the gap cannot be described, gather the missing evidence before designing the path.

### Move 3: Work backward to build a path

For each outcome, identify three to six moves by reasoning backward from its due date. Every move needs a date or time window, an owner, and evidence of completion.

> For this to be true by the end date, what must be true halfway through? What must happen before that?

### Move 4: Do capacity math

Estimate usable focused capacity honestly:

> available working days × recently observed focused hours per day

Account for unavailable periods, fixed commitments, and meeting-heavy weeks. Compare the result with the effort implied by the proposed paths. If demand exceeds supply, cut, defer, reduce scope, or add real support now. Do not hide the mismatch with optimistic assumptions.

### Move 5: Make the NOT-doing list

Ask:

> What will explicitly not happen this month so these outcomes can?

The user names the cuts. A plan without genuine exclusions is a wish.

### Move 6: Add forcing functions and protective structure

Fragile outcomes need an external forcing function: a named recipient expecting a deliverable on a date, a booked review, a public commitment, or a dependent person waiting on the result.

Protect work vulnerable to interruption. If one outcome requires long uninterrupted work while another tolerates fragmented attention, batch the flexible work around fixed commitments and reserve the best available blocks for the fragile work. If a scheduling conflict defeats protected time, include resolving it as an immediate action.

### Move 7: Run a pre-mortem

Ask:

> It is the final day of the month and this plan failed. What happened?

The user answers first. Record the two or three most likely failure modes and one specific counter for each.

### Move 8: Get sign-off

Read the plan back in ten lines or fewer. The user must be able to state the theme and main outcomes from memory, then explicitly approve it.

> Is this the plan?

If approval is vague, revise. Do not save yet.

## Required plan structure

```markdown
## THEME: [MEMORABLE, ACTION-ORIENTED LINE]

**Planning range:** [DD MMM–DD MMM].

## Shape of the month
[Unavailable periods, fixed events, heavy weeks, effective working weeks, and immediate constraints after month-end.]

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
[The behavior, boundary, or environment change that counters last month’s drain; include tracked delegated work and owners.]

## Personal-practice commitment
[Specific measurable commitment, if in scope.]

## Pre-mortem
- Failure mode: [likely cause]. Counter: [specific response.]
```

## Step 5: Save the review and plan

After explicit sign-off, write two records in the user’s chosen system:

1. A **Review** attached to the month ending.
2. A **Plan** attached to the month beginning.

Create a missing monthly record if the system supports it. Use one final write operation when possible. Before replacing an existing plan, show the existing material to the user and resolve the difference.

Use this review template:

```markdown
## Personal-practice verdict
**[ON TRACK / BEHIND / OFF TRACK / AT RISK / NOT IN SCOPE]**

- Actual: [key measures].
- Target: [current agreed target].
- Consistency: [relevant pattern or gap].
- Change from prior month: [key delta].
- Verdict: [one direct sentence].
- **Next-month commitment:** [specific commitment].

## Goals and delivery
- Weekly commitments: [completed]/[total] ([percent]%).
- Longer-range goal movement: [goal and status].
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

At the end of every run, make one precise improvement to the reusable workflow, its templates, or its data mapping. Store it in the user’s chosen workflow document or improvement log. If no shared location exists, present the proposed edit as a short durable rule the user can save.

Look for a noisy read, a wrong data assumption, a misleading metric, a user correction, or a repeated pattern. Prefer one precise rule over a vague reminder.

## Audit checks

Before finishing, verify:

- The review and planning ranges are explicit.
- Evidence was shown before reflective prompts.
- Strong verdicts account for known data-quality limits.
- The plan has a named theme and no more than three outcomes.
- Every outcome has a test of done, date, path, owner, and forcing function.
- Capacity demand fits supply, or an explicit scope decision was made.
- The NOT-doing list contains genuine cuts.
- The structural fix responds to a reviewed drain.
- Overlapping weekly plans were checked and reconciled.
- Personal-practice commitments are specific when in scope.
- The pre-mortem includes counters.
- The user explicitly approved the plan before it was saved.
- Saved material contains only information appropriate for its intended record and access boundary.

## Common failure modes

- Starting with prompts instead of evidence.
- Judging against stale targets.
- Treating incomplete tracking as complete truth.
- Confusing a list of events with a plan.
- Overloading capacity and refusing to cut scope.
- Letting the assistant choose the user’s priorities.
- Treating a brainstorm, spoken note, or imported task list as a confirmed commitment.
- Saving an unapproved draft.
- Duplicating or conflicting with weekly plans.
- Treating wellbeing averages as more truthful than repeated written evidence.
- Applying generic routines instead of fixing the actual drain.
- Replacing an existing record without resolving the difference.
- Collecting or retaining private information that is not necessary for the review or plan.


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
description: Plan travel around the trip’s purpose, compare complete current journeys, and prepare or make authorized bookings with clear checks, privacy limits, and practical trade-offs.
---

# Plan and book a trip

Plan transport around the trip the traveler actually wants, rather than letting the first cheap fare determine the trip. Build an agreed trip brief, research a small number of complete and current options, recommend one clearly, and prepare or complete bookings only within the traveler’s authorization.

Treat current user instructions as authoritative. Previous itineraries, receipts, loyalty status, and past choices are evidence, not permanent instructions. Do not turn one trip’s dates, prices, upgrade outcome, or event schedule into a general rule.

## 1. Establish the trip before shopping

For a new trip, begin with a focused discovery pass. Do not start detailed fare searches, upgrade comparisons, or checkout preparation while important questions about the trip’s purpose, dates, and shape remain unanswered. The traveler may explicitly request a narrow fare check or ask to skip discovery; follow that request without forcing a full interview.

For a continuing trip, reuse the established brief and ask what has changed. Do not restart an interview whose answers are already known.

### Use relevant context safely

Read the conversation and relevant material the traveler has supplied, such as invitations, agendas, itineraries, accommodation details, or trip documents. If the traveler has given clear authorization and there is a legitimate planning purpose, consult only the minimum relevant material in calendars, travel correspondence, reservation records, and approved planning sources.

Keep private-source access narrowly scoped:

- Use only the accounts, messages, calendar events, records, or documents relevant to this trip.
- Search using trip-related terms such as the destination, event, date range, organizer, project, or companion only when needed to understand the trip.
- Read enough surrounding context to understand goals, constraints, and arrangements, but not unrelated personal communications.
- Do not inspect unrelated inbox content, private records, or communications merely because access exists.
- Do not contact organizers, companions, employers, accommodation providers, carriers, or anyone else without separate authorization.
- Keep findings within the approved private planning boundary. Omit unrelated or sensitive personal details from shareable summaries.
- If an authorized source is unavailable, say so. Do not imply that it was checked.

Look for the trip’s purpose, event times and locations, companions, existing transport or accommodation, confirmed versus provisional dates, commitments immediately before and after travel, and practical limits such as work obligations or accessibility needs. Distinguish carefully between an invitation and confirmed attendance, a calendar hold and a hard constraint, and an old booking habit and a current preference.

Resolve conflicting sources where possible. State remaining uncertainty rather than silently choosing one interpretation. Retrieve accessible facts yourself instead of asking the traveler to copy information from an authorized source.

### Ask questions that shape the trip

After a short context pass, state what is known and ask a compact, substantive group of questions. Usually ask four to six questions for an open-ended trip; use fewer when the key answers are already clear. Ask in one numbered plain-text block, then yield for the response.

Use known facts to ask better questions. An agenda may establish formal event dates, for example, but the traveler still needs to say whether the event is worth attending, whether they want extra time with people there, and how rested they need to be.

Choose questions that develop the trip rather than merely collect booking fields:

1. **Purpose and outcome:** What is the trip for, and what would make it successful? Which event, visit, meeting, or activity matters most?
2. **People and places:** Who is traveling or being visited? Which stops are essential, optional, or best done in a particular order?
3. **Time:** How much time does the traveler want in each place? What fixes the earliest departure, required arrival, and latest return? If dates are flexible, what is the useful range and what would they trade for another day away?
4. **Pace, work, and recovery:** Is this work, leisure, or both? Does the traveler need to arrive rested, work en route, protect a quiet day, or leave unstructured time?
5. **Practical arrangements:** What accommodation, local pickup, ground transport, reimbursement, accessibility support, or companion coordination is already arranged?
6. **Requested outcome:** Does the traveler want research, a reviewable booking plan, or an authorized purchase?

Do not require a numerical budget before showing useful trade-offs. Do not turn the first discovery conversation into an unnecessary discussion of fare brands or upgrade products. Carry forward uncertain answers explicitly instead of inventing preferences.

### Agree a usable trip brief

Before detailed transport research, summarize:

- Purpose, key people, and essential stops.
- Desired time in each place.
- Fixed dates, arrival deadlines, and flexible date ranges.
- Work, sleep, recovery, and pace needs.
- Existing accommodation and transport.
- Preferences that materially affect the search.
- Open questions and assumptions.

Give the traveler a practical opportunity to correct the brief. Clear answers can establish agreement; do not request ceremonial approval for something already confirmed. If an unresolved issue could materially change the trip, ask about it before shopping. Keep provisional dates visibly provisional.

## 2. Set travel preferences explicitly

Do not assume that a particular airline, airport, seat, cabin, rail class, or loyalty program is always preferred. Ask about preferences that remain unknown and matter to the trip. Use the traveler’s stated lasting preferences where available, but verify changing facts such as current membership benefits, eligibility, or fare rules.

| Category | Decision to establish | Example of a useful rule |
|---|---|---|
| Routing | Direct service, connection tolerance, nearby airports | Prefer nonstop when its time or comfort benefit justifies the price. |
| Cabin | Economy, true premium economy, business, sleeper product | Compare actual cabins, not marketing labels. |
| Sleep and readiness | Importance of arriving rested | Put more weight on confirmed sleep quality before a demanding first day. |
| Seat | Window, aisle, extra legroom, accessibility | Include selection cost and check availability where possible. |
| Luggage | Personal item, cabin bag, checked bag | Verify the chosen fare’s actual allowance and limits. |
| Rail | Standard, flexible, premium, food or lounge access | Compare named fare products and their change and refund rules. |
| Flexibility | Changeability, refundability, uncertain dates | Explain what flexibility costs and when it has practical value. |
| Loyalty and upgrades | Status benefits, points use, upgrade interest | Recheck live eligibility and benefits; never assume they persist. |

When comparing premium economy, verify that it is a distinct cabin. Extra-legroom economy is not premium economy. When comparing rail classes, do not trust a reseller’s generic class label; verify the named product, what it includes, and its conditions.

For overnight travel, consider whether sleep is worth paying for, especially before work, a major event, driving, or caregiving. Verify the actual aircraft, train, or sleeper product rather than assuming a cabin label guarantees a lie-flat seat, private berth, meal, lounge, or other facility. Mixed-cabin journeys can be sensible: for example, a higher cabin on the overnight leg and a lower cabin on a daytime return.

## 3. Research current transport options

Begin detailed research after the brief is established, unless the traveler explicitly asked for a narrow check. Keep searches tied to the brief. If available transport would require a meaningful change to the trip, return to the traveler with that choice rather than silently reshaping the itinerary.

### Search schedules, fares, and complete routes

Search current schedules and prices across the useful date range. Use broad discovery sources to identify routes, service patterns, and date differences, then verify the selected itinerary, operating provider, fare family, and conditions directly with the carrier or rail operator where practical.

A marketing provider may differ from the operator. Identify the operating provider, especially when service standards, baggage rules, loyalty benefits, or disruption support depend on it.

For long-haul flights, list useful direct departures on the selected date rather than showing only the cheapest. Departure and arrival timing may affect sleep, daylight exposure, and readiness more than a small price difference.

Compare useful combinations, including:

- Return versus open-jaw tickets.
- Direct versus connecting journeys.
- Nearby airports with realistic ground connections.
- Flight plus rail, ferry, or coach.
- Rail-only options where appropriate.
- Different arrival and departure cities.
- One protected through-ticket versus separately booked segments.

Judge the complete journey, not the airfare alone. A lower airfare may create a costly airport transfer, hotel night, difficult connection, lost workday, or excessive risk.

Check transport all the way to the real destination. An airport arrival may still leave several hours of rail or road travel. When locations have similar names, verify the intended station or region. Check whether schedules are released, whether planned engineering work or holiday disruption may apply, and whether the proposed onward connection is practical. Do not invent precise future services or fares that are not yet published.

### Quote quality and verification

Label every price accurately:

- **Live selected itinerary:** A currently selectable journey at the stated price.
- **Indicative date-grid or calendar price:** A discovery signal that still needs itinerary verification.
- **Estimate:** A reasoned approximation, clearly separated from bookable pricing.

Record when each material quote was checked, its currency, and what it includes. An advertised “from” fare is not proof that the required ticket can be purchased. Use verified links for booking pages and material terms where available.

If a tool, provider, login, or checkout fails:

1. Identify the failed source.
2. Give the exact error or observable limitation where feasible.
3. Explain what fact remains unverified.
4. Attempt permitted, safe recovery or an alternate source.
5. Disclose the source switch and its verification limit.

Do not silently substitute a source. Do not claim a provider checkout, personal offer, fare family, or seat was verified if access was blocked.

## 4. Evaluate sleep, timing, and jet lag

For journeys across several time zones, rank options by timing and likely readiness as well as price and cabin. Ask for the traveler’s usual sleep and wake pattern if it is not known. Explain the recommendation in plain language rather than presenting timing as a rigid formula.

Useful general principles include:

- **Eastbound travel:** Favor options that allow sleep during much of the traveler’s usual biological night and avoid an arrival pattern that causes immediate strong morning-light exposure when their body expects sleep. Afternoon light after arrival may help adjustment in many cases.
- **Westbound travel:** Daytime travel that lands in daylight and leaves a manageable interval before local bedtime is often easier to adapt to.
- **Pre-trip preparation:** When the trip warrants it, recommend a gradual sleep-shift plan for several days before departure rather than one dramatic change the night before.
- **First days after arrival:** Give a simple light, meal, caffeine, and sleep plan suited to the travel direction and first important commitment.
- **Practicality first:** A theoretically ideal circadian schedule is not useful if it sacrifices a critical meeting, safe transfer, or necessary recovery time.

Do not overstate medical certainty. Jet lag responses vary. Travelers with health conditions, medication concerns, or sleep disorders should seek appropriate professional advice.

## 5. Compare upgrades and loyalty options carefully

When upgrades matter, compare three distinct paths:

1. Buying the desired cabin or class outright.
2. Changing an existing ticket and paying the applicable fare difference.
3. Purchasing a separate cash, points, or loyalty upgrade offer.

Before ticketing, compare the complete price of the base fare plus likely upgrade cost against buying the desired cabin outright. After ticketing, compare the additional cost, restrictions, and outcomes of changing versus upgrading. Do not assume an earlier upgrade payment transfers to a later change.

Separate a confirmed cabin from a waitlist, bid, standby request, or points-based request. An empty seat map is not proof that an upgrade will clear. If reliable sleep or comfort is important, recommend a confirmed option the traveler would accept. Buy a lower cabin only if the traveler would be content remaining there.

Verify the selected fare family’s upgrade eligibility, current loyalty benefits, waitlist priority, and cancellation or refund terms. Do not assume restrictive economy fares can be upgraded. Do not assume that a particular point before departure is predictably the cheapest time to buy an upgrade; prices can rise, cabins can sell out, and preferred seats can disappear.

When comparing cash with points plus a copayment, state the valuation assumption. Read the specific offer’s change, cancellation, refund, and missed-upgrade terms. The flexibility of the original ticket does not automatically apply to the upgrade.

For an existing reservation, inspect personal upgrade offers and alternative change prices only when authenticated access is available and authorized. Public fares do not establish a reservation-specific offer.

## 6. Include seats, luggage, and rail conditions

Include mandatory or desired extras in the comparison. Check seat availability before booking when the traveler has a material preference. A seat preference does not guarantee assignment.

For flights, verify:

- Actual cabin on every segment.
- Seat-selection fee and available seat type.
- Cabin-bag allowance, size, and weight limits.
- Whether the fare includes only a personal item.
- Material change, cancellation, and refund restrictions.

A personal-item-only fare does not meet a cabin-bag need. Included checked baggage does not justify an upgrade unless the traveler needs it.

For international rail, search the actual travel date and compare relevant named fare products, such as a standard flexible tier and a premium flexible tier. Show the price difference and explain what it buys: flexibility, food, lounge access, priority processes, boarding guarantees, or other benefits. Recheck current terms before quoting them, as they change.

Use a practical station-arrival target based on the operator’s current guidance, border formalities, security, holiday volume, and unfamiliarity with the station. Do not plan around the final gate-closing minute.

## 7. Compare complete journeys

Present two or three useful choices and recommend one. If only one option meets the brief, say so rather than inventing alternatives.

Show local dates and times, airport or station codes where helpful, total duration, and next-day arrivals explicitly. Account for time-zone changes. Include realistic buffers for immigration, baggage collection, city transfers, rail check-in, security, and holiday congestion.

Distinguish protected connections from independently booked tickets. Explain who carries the risk if the first service is delayed. Consider a longer connection or overnight stop when it meaningfully reduces risk, especially where practical accommodation is available.

| Option | Dates and route | Product and fare | Complete cost | Main benefit | Main drawback |
|---|---|---|---|---|---|
| [Option A] | [Local dates, route, duration] | [Cabin or class on each segment] | [Currency, ticket, required seat and transfer costs] | [Time, comfort, or flexibility] | [Restriction, effort, or uncertainty] |

Show currencies separately. If converting, label the exchange-rate assumption and conversion date. Never combine unlike currencies into an unexplained total.

Explain what each extra cost buys: better sleep, a shorter journey, less connection risk, a confirmed preferred seat, an extra day at the destination, or more flexibility. Include material restrictions, luggage, seat fees, ground transport, and unverified items.

## 8. Prepare and complete an authorized booking

Lead with the recommended dates and route, followed by the comparison, quote-check time, verified links, unresolved facts, and the decision still needed.

Complete research and prepare a concrete, reviewable booking before requesting approval that is actually necessary. A request to search or compare transport does not authorize payment. If the traveler has already authorized a specific purchase or provided a clear scope and sufficient price ceiling, continue within that authorization without asking again merely because checkout is next.

Before submitting an authorized purchase, verify against the chosen option:

- Passenger name as supplied by the traveler.
- Exact dates, local times, airports, stations, and route.
- Operating provider and direct or connecting status.
- Cabin or class on every segment.
- Fare family and material conditions.
- Seat selection and current seat availability.
- Luggage allowance.
- Total price and currency.

Resolve a material mismatch, unavailable required seat, missing identity field, or price outside authorization before purchase. Never invent identity, passport, payment, loyalty, visa, or accessibility details.

After purchase, verify success from the provider’s confirmation, not from a search result or partially completed checkout. Report the booked journey, total paid, assigned or unassigned seats, and any remaining transport arrangements. Keep booking references, payment details, identity documents, and receipts in an appropriate private trip record rather than a reusable workflow or shareable summary.

## 9. Monitor only with a real mechanism

Do not promise to watch fares or upgrades between conversations unless an authorized monitoring system actually exists and can access the necessary information.

If monitoring is requested, establish a real schedule or approved alert service. Confirm that it can access the reservation or public fare source, specify what it watches, and state whether it alerts only or can purchase. Monitoring does not authorize a purchase.

For an upgrade-alert service, verify that its action is an alert rather than an automatic bid or purchase. Confirm any subscription cost, success fee, fare-repricing effect, and cancellation terms before enabling it. Keep automatic fare repricing off unless the traveler specifically wants it and understands that repricing may change fare conditions or upgrade eligibility.

Stop monitoring after departure, a completed upgrade, or a changed plan. If authentication, automation, or scheduling is unavailable, say that monitoring is not active.

## 10. Learn responsibly during active use

Apply corrections to the current trip immediately. When the traveler has authorized retention of preferences, save only clear, reusable lessons with their qualifications. For example, retain “prefer a confirmed sleep-friendly cabin before an early work day” rather than “always buy the highest cabin.”

Use these rules:

- Replace superseded preferences rather than accumulating contradictions.
- Treat current fares, event dates, one-off exceptions, and unusually cheap upgrades as trip-specific facts.
- Do not infer satisfaction merely because a booking succeeded.
- Learn from verified feedback about comfort, connection time, disruption, and booking friction.
- Ask whether a choice applies to this trip or future trips only when that distinction is genuinely unclear.
- Do not retain credentials, payment details, passport data, loyalty numbers, reservation codes, or copies of identity documents in reusable instructions.
- Learning does not create additional authority to purchase, message others, or access accounts.

Briefly tell the traveler about any durable preference or workflow lesson that was saved. If no useful lesson emerged, do not create one merely to record activity.


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
description: Review authorized meeting records, identify genuine unfinished commitments, create clear deduplicated follow-up tasks, and batch only questions requiring judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose and operating rules

Use meeting records only for a legitimate work purpose and with clear authorization to access them. Review the minimum sources and personal information needed to determine follow-up ownership. Do not copy unrelated private details, sensitive personal information, or confidential discussion into a task system unless it is necessary, authorized, and appropriate for everyone who can access that system.

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

Apply known responsibility and delegation boundaries supplied by the user or organization. Attendance at a meeting does not make the user accountable for all work discussed in that area.

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

Fetch full meeting records in parallel where the selected meeting system supports batching. Do not search for existing tasks yet: first identify people, topics, and candidate outcomes so that duplicate checks are accurate.

For long transcripts, use a repeatable search, extraction, or chunking method rather than relying on truncated previews. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by explicit acceptance

Review automated action items as candidates, then verify them against the transcript and surrounding conversation. A promise may have been conditional, reassigned, fulfilled live, or directed at another attendee.

## 3. Triage each meeting

Classify the meeting loosely. Classification provides a starting expectation, not a rule that overrides evidence.

| Meeting type | Usual outcome | Guidance |
|---|---:|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or explicitly timed follow-up. |
| Information-gathering, interview, or reference call | 0 tasks | Create work only for an explicit out-of-meeting commitment. |
| Internal planning or team meeting | 0–1 user-owned task | Capture the user’s deliverable, not the full team action list. |
| Coaching or recurring one-to-one | 0–1 task | Create a task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1–2 tasks | Often separate an internal decision from an external response. |

For every meeting, identify:

- Relationship context and why the meeting occurred
- Candidate actions owned by the user
- Work completed during the meeting
- Work delegated to another named owner
- Explicit future commitments and timing
- Enough neutral context for a task to remain understandable weeks later
- Source and related links

Create no task when work was completed live, another person owns it, the meeting was purely informational and needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

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
- Meeting record: <link>
- Related document: <link>
```

Avoid unnecessary private discussion in a task system that may be broadly visible. Follow the user’s known writing preferences. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable. If the task is to send a message, write a ready-to-send draft rather than merely saying “email them.” For introductions, use double opt-in: seek permission from each relevant party before connecting them.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by meeting link or identifier, relevant counterparty, distinctive topic terms, and proposed title.

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

- Add a short note to a reusable meeting-pattern reference when a recurring pattern affects triage, such as a common attribution error, reliable sign of in-meeting completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new responsibility boundary in the user’s or organization’s maintained responsibility reference when it applies beyond one meeting.

Do not turn one-off facts into permanent rules. Small additions to a patterns reference can be made directly where authorized. Ask for confirmation before structural workflow changes, such as adding or removing steps or changing the evidence order. Briefly report reusable guidance added or changed.

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
- Task notes remain within the appropriate access boundary.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report the essential outcome only: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and any reusable guidance changes. Keep status updates terse and factual.


---
name: turn-a-message-into-a-task
description: Read a message thread, prepare the real work, and create a trackable task only when a record will help complete it safely.
---

# Turn a message into a task

Use this workflow when one or more message links, emails, chat threads, or conversation excerpts may require follow-up. The goal is not merely to log a to-do. The goal is to complete as much safe, useful work as possible, then leave a small, clear human action when judgment, approval, memory, or authority is still needed.

Run the full workflow separately for each source conversation unless several links clearly describe the same request.

## Core operating rules

- Read the complete relevant conversation before deciding what to do.
- Never send messages, email, invitations, approvals, or other external actions without explicit authorization. Draft or stage them only.
- Do not create a task for work that is already completed, superseded, reassigned, duplicated, or clearly owned elsewhere.
- Use private communications or records only for a legitimate, authorized purpose. Use the minimum relevant sources and information, and respect consent, confidentiality, and access boundaries.
- Do not invent facts, dates, links, commitments, or a person’s views. Mark unknown facts clearly.
- A task with empty notes or no useful preparation is usually a failed outcome. The record should make the remaining action obvious.
- Preserve the appropriate privacy boundary in outputs. Do not copy unrelated personal, employment, financial, health, or relationship information into a task.

## 1. Read the complete conversation

Start from the linked message, but treat it as an anchor rather than the whole request.

1. Open the parent message and all replies.
2. If the source is a top-level message with replies, read the replies immediately.
3. If the link points to a reply, retrieve the entire parent thread.
4. Identify the people involved by name and relevant role. Resolve ambiguous identities through authorized profile or directory information rather than referring vaguely to “the person.”
5. Note deadlines, promises, dependencies, decisions, linked documents, and ownership.
6. Check whether newer replies changed the request. A later answer may mean the work is done, deferred, superseded, or reassigned.

If the thread appears complete, report that finding and ask before creating a record. Do not turn dead work into a new obligation.

### Conversation-reading checklist

| Check | What to capture |
|---|---|
| Actual ask | What outcome is requested, by whom, and for whom? |
| Current state | What has already been done, promised, decided, or blocked? |
| Timing | Explicit deadline, implied timing, wait state, or event date. |
| Sources | Documents, prior messages, records, or public references that may change the answer. |
| Sensitivity | Personal, employment, financial, health, or relationship details requiring narrower handling. |

## 2. Identify the true task shape

State the task shape in working notes before researching. The shape determines what “pre-completed” means.

| Task shape | Typical remaining deliverable |
|---|---|
| Reply owed | A concise draft response, prepared in the correct thread or channel if staging is available. |
| Artefact owed | A draft reference, document, introduction, analysis, data pull, or other requested material. |
| Decision needed | A short decision brief with options, evidence, recommendation, and a draft response for the likely choice. |
| Delegation or follow-up | A draft chase, handoff, scheduling request, or process action ready for review. |
| Information request | A verified answer with sources, caveats, and any follow-up question needed. |

A message may contain multiple asks. Keep them in one task when they have the same owner and time horizon, using clear sub-parts in the notes. Split them only if different people own them, their deadlines differ materially, or combining them would obscure completion.

Rewrite the request as a concrete outcome. Prefer “Send a written reference and feedback” over “Follow up on message.”

## 3. Gather only the context that matters

Choose sources based on the task, not as a blanket search. Use the minimum relevant sources and avoid collecting unrelated private details.

Typical source choices include:

- **Person-related work:** authorized prior correspondence, meeting notes, role records, work samples, or prior feedback. For references or performance-related feedback, seek specific observable examples and role-relevant evidence rather than broad labels.
- **Project or event work:** recent channel history, project documents, planning pages, logistics records, and relevant linked files.
- **Historical data questions:** authoritative internal records, retrospectives, planning correspondence, and verified reports. Read original materials where possible.
- **Same-topic requests:** a focused search across authorized conversations may reveal duplicate asks or an existing answer. Reuse one well-supported answer rather than producing inconsistent separate replies.
- **Linked files:** open and read them. For multi-section documents, inspect all relevant sections or tabs; the message may mention only one of several required decisions.
- **Policy or process questions:** read the current policy, prior approved precedent, and ownership path. Do not treat informal messages as policy.
- **Public facts:** use reputable search and retrieval methods. Do not expose private records or open interactive sessions unnecessarily.

For private communications or personnel-related records, confirm a legitimate purpose and authorization. Include only the minimum information needed in the task output. Omit unrelated sensitive details, particularly personal circumstances that do not affect the requested work.

Stop researching when you can either complete a useful draft or state exactly what blocks progress. Two or three carefully selected sources are usually better than many shallow searches.

## 4. Pre-complete the work

Do as much of the task as is reasonable without crossing an approval boundary.

### Drafting rules

- Follow the user’s supplied voice guide, examples, or explicit communication preferences when one exists.
- Keep drafts shorter than first instinct. Remove ceremonial framing, repeated context, and unnecessary checklists unless they serve the recipient.
- Ask one simple, useful question rather than several low-value questions where possible.
- State future commitments cautiously unless they are confirmed.
- For money, hiring, policy, or approval requests, direct the requester through the established process rather than making informal commitments.
- Never guess a URL. Verify it, omit it, or use a clear placeholder such as `[LINK TO VERIFY: project page]`.
- Mark uncertain factual claims visibly, for example: `[VERIFY: confirm attendance count from official record]`.
- For details only the user can supply, preserve the draft structure and insert direct placeholders: `[FILL IN: your firsthand view of the event]`.

For reply-shaped tasks, stage the draft in the original conversation when the communication system supports drafts and the user has authorized staging. Put the full draft in the task notes too, so the record remains useful outside the messaging tool.

When formatting a staged chat draft, use readable paragraphs and blank lines before lists so the platform renders them correctly. Avoid list lead-ins that add no meaning; move directly to the useful content.

### Decision briefs

For a decision the user must make, provide two or three realistic options. For each option, give the relevant evidence, trade-offs, and operational implications. End with a recommendation and a reason. The goal is not to present an unranked survey; it is to reduce decision effort while preserving the user’s authority.

### Remaining work

List only what cannot responsibly be done now. Use concrete bullets, such as:

- Confirm whether you are willing to be named as a future reference.
- Replace the firsthand-experience placeholder with one example.
- Review and send the staged reply.

Do not write vague instructions such as “review and complete.”

## 5. Ask questions only at a real decision fork

Before asking the user, check whether they already answered the question in a prior reply, planning note, email, or documented policy. A documented position is usually better than interrupting them for a decision they have already made.

Ask only when a wrong assumption would waste more time than the interruption, such as when the draft depends on an unrecorded stance, relationship judgment, or commitment.

When questions are necessary:

1. Start with one or two short paragraphs that restore context: who is involved, what happened, what is now being asked, and what tension must be resolved.
2. Ask two to four focused questions.
3. Allow multiple selections and a free-text answer when the user may reasonably combine options.
4. Use the answers to finish the draft before creating the task record.

If there is no meaningful fork, make a reasonable metadata and drafting choice, disclose the assumption in the final report, and allow correction later.

## 6. Decide whether a task record is needed

A task record is useful when work must be deferred, tracked, or coordinated. It is unnecessary bureaucracy when the user can finish immediately.

Skip the record and report in chat when the only remaining action is a short, single sitting—for example, reviewing a prepared reply and sending it in roughly 15 minutes—and there is no deadline, dependency, or reason to track it.

Create a record when one or more of these apply:

- Work is genuinely deferred.
- There is a deadline, wait state, or dependency worth tracking.
- Several steps remain or the work spans days.
- The request explicitly asks for a record.
- The remaining work is important enough that it could be lost among conversations.

When uncertain, prefer chat-only for a simple prepared reply and a record for longer-lived work.

## 7. Create a high-value task record

Use the user’s chosen task system. Verify required field names and available categories rather than assuming a fixed schema.

| Field | Guidance |
|---|---|
| Title | Imperative, specific, and short. Name the outcome, not the source message. |
| Status | Set the system’s normal open state. |
| Due date | Use an explicit or strongly implied date; otherwise leave blank. |
| Importance and urgency | Make a best judgment from consequences, timing, and people waiting. |
| Time estimate | Estimate only remaining human effort, not research already completed. |
| Area or project | Choose the best verified category; use a general category if none fits. |
| Notes | Include source, context, prepared material, and exact remaining actions. |

Use this notes structure:

```markdown
**What:** [one-line statement of the ask and who is waiting]
**Source:** [link or reference to the original conversation]
**Context:**
- [relevant fact or prior commitment]
- [relevant evidence or linked source]
- [important caveat, deadline, or dependency]

**Pre-completed:**
[full draft reply, artefact, or decision brief]

**Remaining for the user:**
- [specific action]
- [specific action]
```

After creating the record, open or retrieve it to confirm that the title, notes, date, links, and category were stored correctly.

## 8. Report back clearly

If a record was created, report in this order:

1. What the task is.
2. What was pre-completed and where any draft was staged.
3. Metadata choices: importance, urgency, due date, and remaining time estimate.
4. Any `[VERIFY]` or `[FILL IN]` items that prevent immediate sending.

If no record was needed, separate the briefing from the deliverable exactly. The draft should be the final block, so it can be copied without cleanup.

```markdown
## Context for the user (not part of the reply)
- [ask, recipient, important facts, and assumptions]
- [whether a draft was staged]
- [verification flags]

## The reply
[verbatim draft]
```

## 9. Run a bounded sent-versus-draft learning loop

Whenever a message draft is staged, and the user has authorized access to the relevant conversation and follow-up checking, schedule a follow-up review after a reasonable interval, such as about one hour. Record the conversation location, thread identifier where applicable, and where the staged text can be found.

At each review:

1. Re-read the relevant thread and determine whether the user sent a version of the draft.
2. If they did, compare the sent version with the staged version. Identify what was cut, reworded, reordered, added, or intentionally left out.
3. Extract only general lessons that can improve future drafting, such as preferred brevity, tone, sequencing, formatting, or a stable approval route.
4. If the draft has not been sent, reschedule only a limited number of checks at increasing intervals, then stop. The user may have deliberately chosen not to send it.

Do not treat a single edit as a universal rule. Do not retain private content merely to learn style. Do not send reminders or take further external action as part of this loop unless separately authorized.

## 10. Improve the workflow after each run

After completing the task or chat-only response, briefly review the run for reusable operational lessons. Make only small, general updates to an authorized shared workflow guide or memory system. Examples include:

- A source type that repeatedly provides essential evidence.
- A messaging or task-system formatting quirk and its workaround.
- A task shape not covered by the current taxonomy.
- A step that causes repeated wasted effort and should be clarified or removed.
- A stable correction to drafting, process routing, or research order.

Do not encode one-off incidents, private facts, individual preferences without evidence of stability, or sensitive personal details. Do not modify user-owned systems, publish changes, or create persistent records without authorization. If no reusable lesson emerged, make no change.

## Final audit before completion

- Did you read the whole relevant conversation?
- Is the task still live and owned by the user?
- Did you use only necessary, authorized sources and information?
- Is the requested work substantially pre-completed?
- Are all uncertain facts, links, and firsthand details clearly marked?
- Did you avoid sending, approving, or committing anything externally?
- Is a task record genuinely useful rather than bureaucratic?
- Does the output identify specific remaining actions?
- Does the output stay within the appropriate privacy and access boundary?
- If a draft was staged, is any authorized learning follow-up bounded, documented, and non-intrusive?


---
name: design-a-work-sample
description: Create or improve a short, paid, asynchronous work sample that produces role-relevant evidence, is practical to score, and is validated with simulated submissions.
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous work sample for hiring. A strong work sample gives candidates a bounded, realistic version of the job, creates evidence that is difficult to imitate through polished generalities alone, and lets reviewers assess submissions consistently.

Use it for a take-home exercise that usually takes two to four hours. Do not use it for an application-form question, an interview question set, a live interview exercise, or a multi-day work trial. If the requested format is unclear, ask one question before proceeding.

## Purpose and design principles

A work sample should answer a narrow question: can the candidate demonstrate the few capabilities most important to succeeding in this role?

It should not try to measure every quality that matters. Other stages may be better suited to assess live communication, motivation, collaboration, sustained reliability, judgment in real internal systems, or performance over an extended period. References may help assess prior working relationships and long-term dependability. Specific tool fluency, internal terminology, and trainable processes often should not be central to a short exercise unless they are essential from the first day.

Focus on three to five load-bearing capabilities that are important to the role and can be observed fairly in a short asynchronous exercise. Examples include prioritization, practical judgment, clear communication, diagnosis, sourcing, execution, systems thinking, and turning ambiguity into useful work.

Use these defaults unless the hiring owner chooses otherwise:

- Make the exercise paid.
- Set a clear expected time limit, commonly three hours.
- Use a self-contained scenario. Candidates should not need internal-system access, private data, or a response from an unavailable stakeholder.
- Keep review time to about 20 to 25 minutes per submission.
- Use realistic but fictionalized or approved public details.
- Do not include credentials, private contact details, sensitive operational facts, or personal data that is not necessary for the task.
- Do not ask candidates to create work the organization will use commercially unless that use is separately agreed in writing.
- State whether AI tools are permitted. Assess judgment and output quality rather than trying to infer AI use from writing style.
- Provide a reasonable-accommodation route or an equivalent accessible format while preserving the relevant performance standard.
- Assess role-relevant capabilities only. Do not use criteria that assess protected characteristics, identity, or unrelated proxies.

If the workflow requires hiring records, team notes, or prior candidate materials, use them only for a legitimate hiring purpose and with clear authorization. Read the minimum relevant material, keep outputs within the approved hiring access boundary, and omit unrelated personal or sensitive details.

## Step 1: Pre-flight

Before designing the exercise, confirm the hiring team has both:

1. A current job description or role brief covering responsibilities, level, expected outcomes, and reporting context.
2. A role-success profile, hiring plan, or equivalent document describing the capabilities and experience that matter most for success.

If either item is missing, stop. Do not try to define the success profile while drafting the exercise. That creates a moving target and commonly results in a plausible task that measures the wrong thing.

Use this request:

> Before we design the work sample, I need the role description and a role-success profile or hiring plan. I can help create either one first. Which is missing, and who should confirm it?

Once both exist, read the relevant role context. This can include the role brief, hiring plan, linked project documentation, team constraints, examples of strong work, prior hiring feedback, and existing exercises for comparable roles. Read one or two comparable exercises only to calibrate tone, length, and delivery format. Do not copy their task shape by default: different roles need different evidence.

Then give a short status update, for example:

> Read the role brief, success profile, and two comparable exercises. Moving to the alignment memo.

## Step 2: Write the alignment memo before drafting

Do not write candidate-facing instructions yet. First write a one-page memo titled:

**What we are testing for and why: [Role] work sample**

Include the following sections.

### Load-bearing capabilities

List three to five observable capabilities the role succeeds or fails on and that a short work sample can surface. Avoid broad labels such as “strategic thinking.” Describe visible behavior instead.

Weak: “Strategic thinking.”

Better: “Identifies the highest-leverage issue in a messy operating situation, explains the tradeoff, and produces a useful first action.”

### What the work sample will not test

Name important criteria that belong in other stages. This prevents the exercise from becoming an unrealistic proxy for the whole role. A short written task may not fairly assess long-term reliability, leadership over months, live collaboration, specialized software fluency, or performance in a real internal environment.

### Calibration to role level

State whether the role is entry-level, mid-level, senior, or leadership level, and explain the implications.

- Entry-level candidates may need more context, examples, and tightly bounded outputs.
- Mid-level candidates may need to prioritize independently and produce usable work.
- Senior candidates may need to make consequential tradeoffs, set direction, and create artifacts another person could use without further explanation.

### Failure modes the exercise should catch

Identify two or three work patterns that could look acceptable in a conventional process but would create problems in this role. Describe evidence, not personality labels. Examples include a polished planner who does not deliver usable work, a fast executor who misses the central problem, a candidate who defers meaningful decisions when independent judgment is required, or a technically capable person whose communication does not serve the intended audience.

### What strong looks like

Write a short paragraph describing the evidence in a strong submission: what it notices, what choices it makes, what it produces, and how it handles uncertainty.

Present the memo to the hiring owner and ask:

> Does this match the capabilities and failure modes you want this work sample to assess?

Do not proceed until the owner explicitly confirms or revises it.

## Step 3: Propose three exercise shapes

Once the alignment memo is approved, offer three distinct exercise shapes. Each should be understandable in about a minute, self-contained, realistically completable within the time limit, and scorable quickly.

For each option, include:

- **Shape:** A plain-language description of the task.
- **What it tests:** The load-bearing capabilities it reveals.
- **Why it is evaluable:** The evidence reviewers will see and why scoring can be consistent.
- **Main risk:** The likely source of noise, unfairness, or weak signal.

Keep each option concise. Common shapes include:

- **Triage pile:** The candidate receives realistic messages, requests, and constraints. They prioritize, draft responses or outputs, and recommend one systemic improvement. This works for operations, coordination, support, and communication-heavy roles.
- **Choose the highest-leverage action and ship it:** The candidate receives several possible priorities, chooses one, explains why, and creates a small usable output. This suits builder and strategic operations roles.
- **Diagnose and fix:** The candidate reviews a messy situation, identifies the central issue, and ships one focused intervention. This suits analytical, program, product, and process-improvement roles.
- **Source and pitch:** The candidate defines a target profile, identifies promising channels or prospects from supplied information, and drafts outreach. This suits recruiting, partnerships, sales, and community-growth roles.
- **Decision-useful analysis:** The candidate analyzes supplied evidence and makes a recommendation for a decision-maker. This suits research, strategy, policy, and specialist roles.
- **Design a repeatable system:** The candidate builds a lightweight playbook, process, or operating artifact another teammate could use. This suits program, enablement, community, and operational-design roles.

Do not draft the complete work sample until the hiring owner chooses a shape. If none fits, generate three new options based on the approved memo rather than forcing a familiar pattern.

## Step 4: Draft version 1

Write candidate-facing content in this order.

## [Role] Work Sample

Open with one or two sentences explaining what the exercise assesses. State the total expected time clearly.

**Your mission**

Describe a specific situation, not an abstract assignment. Give enough context for the task to feel real. If independent judgment is important, identify which stakeholders are unavailable during the exercise so candidates must make reasonable assumptions rather than defer every choice.

End with one sentence restating what the candidate will produce.

**Deliverables**

List two to four parts, with rough time guidance when helpful. A common operational pattern is:

- A short prioritization or analysis section.
- Several actual drafts, decisions, or shipped outputs.
- One systemic improvement or reusable artifact.

Avoid excessive micro-tasks. One substantive analysis, several meaningful outputs, and one usable artifact usually reveal more than dozens of shallow decisions. If planning and execution both matter, explicitly tell candidates not to let planning consume all available time.

**Context**

Provide only the information needed to complete the task: project state, audience, constraints, resources, relevant policy, and stakeholder availability. For a triage-pile exercise, provide roughly eight to ten realistic items. Make some items connected so candidates are rewarded for identifying patterns across the situation, not merely processing volume. Include reference notes containing information needed to make fair decisions, such as capacity limits, escalation rules, or refund policy.

Use clearly fictional names and domains in fictional scenarios. Do not include contact details that could cause a candidate to contact a real person.

**Instructions**

Include the expected time limit, submission deadline and timezone if relevant, submission format, payment amount and payment process, AI-tool policy, and any early-submission bonus. Ask candidates to state important assumptions briefly. Permit incomplete submissions when time runs out. State that the work is for assessment only unless another use is agreed separately. Optionally invite a short informal walkthrough video if it would add useful evidence.

A transparent AI policy can read:

> You may use AI tools. Use them carefully and apply your own judgment. We are evaluating the choices, reasoning, and usefulness of your submission. Briefly note any material use of AI tools.

**Anticipated questions**

Include answers such as:

- If a requirement is unclear, make a reasonable assumption and state it briefly.
- If you do not finish in the expected time, submit what you have and note what you would do next.
- The submission is for assessment only unless another use is agreed separately.

After the candidate-facing draft, add a separate section:

**Notes for the hiring owner (not for the candidate)**

Include three to six concise bullets about choices the owner may want to revisit: whether an item is too obvious, whether constraints are realistic, whether payment matches the role and time, whether a deliverable is too prescriptive, and whether a walkthrough video should be optional, encouraged, or omitted.

End with one focused question: “Which part should we tighten first?”

## Candidate-facing format and style checks

Write in direct, plain English appropriate to the organization and candidate audience. Use the organization’s chosen hiring system or document format, and test the instructions there when possible.

Before sharing every candidate-facing draft, check that it:

- Uses simple headings and bullets.
- Avoids tables if the destination system renders them poorly.
- Avoids horizontal divider lines if the destination system breaks them.
- Uses supported soft line breaks for multi-line message metadata if ordinary line breaks collapse on paste.
- Uses “by the end of [day]” rather than abbreviated wording.
- Avoids repetitive rhetorical patterns, forced contrasts, generic slogans, and overly polished AI-sounding phrasing.
- Uses consistent spelling and locale conventions.
- Contains no confidential facts, credentials, private records, personal contact information, or unnecessary sensitive details.

## Step 5: Iterate with the hiring owner

Expect multiple feedback rounds. For each revision, provide the complete updated work sample, not only a change list, so the owner can paste it into the chosen system or document.

Apply feedback directly unless it would materially undermine validity, fairness, candidate safety, or privacy. If there is a material concern, state it once in plain language, offer an alternative, and let the accountable hiring owner decide.

Common revisions include tightening vague instructions, loosening over-prescriptive tasks, correcting scenario facts, simplifying deliverables, changing payment, and replacing unrealistic details.

## Step 6: Validate with two simulated submissions

Before declaring version 1 complete, generate two full simulated submissions using the exact candidate-facing instructions and stated time limit.

### Simulation A: role-success evidence

Use a persona grounded in the approved role-success profile. Have it complete the actual deliverables, then add a short reflection on key choices, uncertainty, and time allocation.

### Simulation B: plausible capability gap

Use an earnest, capable applicant who could pass ordinary screening but lacks one capability central to this role. Choose a job-relevant contrast, such as someone who plans thoroughly but does not deliver, avoids necessary decisions, or executes individual tasks without recognizing a systemic pattern.

This simulation must concern observable work behavior only. It must not rely on identity, background, protected characteristics, or stereotypes. Have this persona complete the same deliverables.

Then write a synthesis covering:

1. Where the exercise distinguished role-relevant performance sharply.
2. Where both submissions looked similar.
3. What the exercise is likely to predict and what it cannot predict.
4. Specific improvements, ranked by expected impact.

A capability both simulations pass may be a useful floor check. The central question is whether the exercise creates meaningfully different evidence on the load-bearing capabilities.

## Step 7: Apply validation improvements

Revise the complete exercise based on simulation findings. Fix the weakest diagnostic points first. Useful changes may include linking scenario items so pattern recognition matters, removing obvious noise, adding a realistic constraint that forces a tradeoff, replacing a broad opinion prompt with a usable deliverable, clarifying reviewer guidance, or removing requirements for specialized trainable knowledge that is not essential on day one.

Do not make the exercise harder solely to reduce pass rates. Make it more diagnostic of approved, role-relevant capabilities.

## Step 8: Optional external review

If other reviewers provide feedback, assess each suggestion against the alignment memo. State which suggestions will be integrated, which will be skipped, and why. External feedback is evidence, not an automatic instruction. The accountable hiring owner makes the final design decision.

## Step 9: Final readiness gate

Do not mark the work sample complete until all of the following are true:

- The job description and role-success profile are confirmed.
- The alignment memo is approved.
- The chosen task shape maps directly to load-bearing capabilities.
- The task fits the stated time for a qualified candidate.
- The scenario is self-contained and requires no unauthorized access.
- Payment, deadline, AI policy, and submission instructions are clear.
- The candidate-facing text works in the intended delivery system.
- A reviewer can assess a submission in roughly 20 to 25 minutes.
- Both simulations are complete and led to necessary revisions.
- The exercise does not create unpaid production work.
- Privacy, accommodation, role relevance, and proxy-bias risks have been checked.

## Common failure modes

Avoid drafting the task before agreeing what it should measure; testing tool familiarity, domain trivia, or trainable knowledge instead of durable judgment; asking for many small outputs rather than a few meaningful ones; making every scenario item independent; letting candidates defer all decisions when decisiveness is meant to matter; giving insufficient context and rewarding insider knowledge; setting word targets that encourage padding; building an exercise that takes longer to score than its signal justifies; treating polish as the main evidence when the role requires something else; and skipping simulations.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, clear, paid, respectful of candidate time, and capable of producing decision-useful evidence.


---
name: run-a-reference-call
description: Prepare, conduct, and document a fair, privacy-respecting hiring reference call that gathers concrete, role-relevant evidence for a hiring decision.
---

# Run a reference call

Use this workflow when an employer is checking a professional reference for an active hiring decision. A request to *provide* a reference about a former colleague is a different task and should use a reference-response workflow.

Only access communications, calendars, hiring records, notes, or public information for a legitimate hiring purpose and with clear authorization. Use the minimum information needed. Keep records within the approved hiring access boundary, honor consent and notice requirements, and exclude unrelated or sensitive personal information.

## 1. Confirm inputs and readiness

Collect or verify:

- Candidate name and role under consideration.
- Referee name, contact method, professional context, and stated relationship to the candidate.
- Call date, time, joining details, and expected attendees.
- Hiring stage and the decision or next step the call may inform.
- Applicable requirements for reference checks, recording, transcription, and note-taking.

Search the chosen calendar or scheduling system using the referee’s name or contact method. Record the meeting title, time, attendees, joining details, and relevant scheduling context. If no event exists, proceed with the available information and label call details as unconfirmed. Do not invent a date, relationship, or meeting link.

### Readiness gate

Create the call record when these conditions are met:

| Check | Pass condition |
|---|---|
| Purpose | The call supports an active, authorized hiring decision. |
| Identity | Candidate and referee identities are clear enough to avoid contacting the wrong person. |
| Role | Expected outcomes, responsibilities, or decision criteria are available. |
| Scope | The caller has defined role-relevant uncertainties to explore. |
| Privacy | Planned sources, attendees, and note-taking methods meet applicable requirements. |

If a check cannot be met, resolve it before the call where possible. If the call must proceed, document the limitation and restrict questions to an appropriate scope.

## 2. Gather relevant context

Review approved hiring materials to establish:

- The role’s expected outcomes, responsibilities, working conditions, and assessment criteria.
- The candidate’s current stage, such as interview, work sample, final review, or offer review.
- How the referee was introduced and whether they were a manager, colleague, client, collaborator, instructor, or other professional contact.
- How long and how closely the referee worked with the candidate.
- Open questions from interviews, work samples, or other role-relevant evidence.

Research the referee only enough to understand their professional context and ability to observe the candidate’s work. Useful approved sources may include direct correspondence, internal meeting records, prior professional interactions, public professional profiles, and public organization pages. Prefer direct evidence to assumptions based on titles, seniority, or online profiles.

Use a consistent source plan when systems support search:

1. Review relevant direct correspondence with the referee.
2. Review communications or records that mention the referee.
3. Review approved collaboration or meeting records for prior interactions.
4. Review completed reference notes for the same candidate.
5. Review public professional information only when it helps establish the referee’s role or relationship.

Read the most recent relevant items rather than relying on search snippets. Collect approved candidate links, such as an application profile, professional profile, portfolio, or work sample, only if they help the caller during the conversation.

### Review other references

If completed reference notes exist, extract only decision-relevant themes:

- Strengths supported by specific examples.
- Development areas, constraints, or working preferences.
- Differences between accounts.
- Claims requiring independent evidence.
- Questions this referee is uniquely placed to answer.

Earlier reference comments are not facts to confirm. Convert them into neutral questions. If this is the first reference, identify observations that later calls should cross-check, such as ownership, follow-through, collaboration, judgment, reliability, or work under ambiguity.

## 3. Create the call record before the meeting

Create a page or record in the approved hiring or meeting system. Include the candidate, referee, role, date, call details, and permitted attendees. Use transcription or AI note-taking only when authorized and participants have been informed where required.

Use this format. Keep context concise and use bullets rather than long narrative.

```markdown
# [Date] [Referee name] — [Candidate name] reference

## Context
- **Candidate:** [Name and approved profile links]
- **Role:** [Role title]
- **Hiring stage:** [Stage and relevant next step]
- **Referee:** [Name — professional role and brief relevant background]
- **Relationship:** [How, when, and how closely the referee worked with the candidate]
- **Call details:** [Date, time, joining details, attendees, or “not yet confirmed”]
- **Other references:** [Known professional references, if relevant]

## Opening
> Hi [Referee name], thank you for making time. I am [name and hiring role]. [Candidate] is being considered for our [role]. I would like to understand your direct experience of working with them and gather concrete examples relevant to the role. We will use your input only within the appropriate hiring process. Is now still a good time, and are you comfortable proceeding?

## Briefing notes
- [Specific role outcome or uncertainty to test]
- [Prior claim to test neutrally and the evidence needed]
- [What this referee can uniquely observe]
- [Relevant relationship context or limits on their perspective]

## Questions
- [Core and role-specific questions]

## Notes and evidence
- **Observation:** [What the referee directly saw]
- **Interpretation:** [What the referee believes it means]
- **Inference:** [Hiring-team conclusion, if any]

## Assessment limits and follow-up
- [Observation limits, contradictions, confidence, and next actions]
```

## 4. Write actionable briefing notes

Briefing notes are the highest-value preparation section. Turn research into direct, fair actions.

Good: “A prior reference described strong early ownership but inconsistent final handoffs. Ask for a specific example of how the candidate completed, documented, and transferred work.”

Avoid: “Consider exploring whether they finish projects.”

For each briefing note, identify the basis, claim to test, evidence that would clarify it, and why this referee is—or is not—well placed to answer. Do not reveal confidential interview feedback, private assessments, or unnecessary details to the referee.

## 5. Use a core question set

Ask naturally rather than as a rigid script. Start broad, then use targeted probes. Follow important claims with: “What did that look like in practice?”, “What was the candidate’s specific contribution?”, “What happened as a result?”, and “How often did you observe that?”

- How did you work together, and how closely did you work day to day?
- What did the candidate personally own or deliver, and how did it compare with expectations?
- What is their strongest or most distinctive role-relevant capability?
- Tell me about meaningful feedback, a difficult situation, or a missed expectation. What happened next?
- In what environment did they do their best work, and what conditions made success harder?
- If they left this role after several months, what work-related reason would be most likely?
- If things were going well, what development area should their manager prioritize?
- Compared with relevant peers, how would you describe their performance, and what is the basis for that comparison?
- What management approach, support, or team context would help them contribute effectively?
- What have I not asked that would be important for this role?

## 6. Add role-specific probes

Choose three to five probes tied to actual role requirements. Assess role-relevant capabilities and evidence, not personal similarity or social fit.

- **Operations or program delivery:** How do they handle changing requirements? Can they build repeatable processes? How do they prioritize competing requests? How clear is their communication with varied stakeholders?
- **Community or partnership work:** How do they build trust and sustained participation? How do they handle conflict or difficult conversations? Can they balance relationship work with reliable systems and follow-through?
- **Operational leadership:** Have they improved or scaled operations? How do they balance speed, risk, and process? How do they manage budgets, suppliers, agreements, or cross-functional priorities when relevant?
- **Technical or analytical work:** How do they reason through uncertainty? How do they communicate tradeoffs? What evidence shows quality, reliability, and practical impact?

## 7. Conduct and document the call fairly

Confirm the referee’s relationship to the candidate and the limits of their perspective. Ask open questions before targeted probes, and allow time to think. Do not pressure a referee to rank the candidate if they lack a meaningful comparison group.

Keep discussion focused on professional conduct, work outputs, collaboration, judgment, and role alignment. Do not seek rumors or irrelevant information about protected characteristics, health, family, immigration, finances, or other sensitive matters.

During or immediately after the call, separate direct observation, the referee’s interpretation, and the hiring team’s inference. Record confidence based on how direct, specific, recent, and role-relevant the evidence is. Note limitations, possible bias, and unresolved contradictions.

## 8. Complete the audit

Before sharing, confirm that the record:

- Identifies the candidate, referee, role, and call date accurately.
- States the referee’s relationship and observation limits.
- Includes role-specific questions and concrete examples where available.
- Separates observations, opinions, and hiring-team inferences.
- Records meaningful strengths, development areas, and contradictions without exaggeration.
- Excludes unrelated sensitive information.
- Identifies follow-up with the candidate, another referee, or the hiring team.
- Is stored only in an approved system with appropriate access controls.

A reference is one input, not a final verdict. Weight it by direct observation, specificity, relevance, and consistency with other diagnostic evidence—not by the referee’s title, confidence, or personal closeness to the candidate. Mark unknowns clearly and state the next action rather than filling gaps with assumptions.


---
name: use-a-browser-safely
description: Complete browser tasks safely by using the least invasive method, protecting account context, verifying rendered state, and separating preparation from commitment.
---

# Use a browser safely

Use this workflow for browser-based work such as completing dynamic forms, changing settings in a dashboard, collecting information from rendered pages, testing a user flow, or working in an authenticated account. Apply it when a simple page retrieval or an authorized direct interface cannot safely and reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify each meaningful change by reading it back, and do not take a consequential final action until the account, target, page state, and authorization are clear.

A successful automation call does **not** prove the website accepted a change. Modern applications may keep internal state separate from the visible page, commit a field only when it loses focus, replace controls during a re-render, or show an error even though an action succeeded. Treat the page's resulting state—not the automation tool's return value—as the source of truth.

## 1. Set the access, purpose, and privacy boundary

Before opening private records, communications, dashboards, or account-specific content, establish all of the following:

- There is a legitimate purpose for the requested work.
- The requester has clear authority to access the information and make the requested change.
- The account, organization, environment, and browser context are appropriate.
- Only the minimum sources and information needed will be used.
- Screenshots, logs, notes, and outputs will remain within the appropriate access boundary.

Respect consent and ordinary privacy expectations. Do not collect unrelated personal information simply because it is visible. Avoid placing sensitive content in debug output, screenshots, transcripts, or reports. Never disclose credentials, session tokens, recovery information, authentication prompts, or security settings.

When a task concerns people, use only the facts relevant to the task. For example, when reviewing a role application, focus on role-relevant capabilities, alignment, and diagnostic evidence rather than unrelated personal details.

If authorization, account ownership, the target environment, or the purpose is unclear, stop and ask before accessing or changing data.

## 2. Choose the least invasive suitable route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can complete the task. It is often more reliable than reproducing browser behavior.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, UI testing, and forms that do not require an established signed-in identity.
3. **Authorized visible authenticated browser session.** Use this only when the task genuinely needs an existing session, single sign-on state, account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for a legitimate direct route. Check official documentation, ordinary form actions, page source, and visible browser network activity for supported endpoints. A dynamic form may submit structured data to an authorized service that is safer and more dependable to use directly.

Do not use a direct interface to bypass access controls, consent boundaries, site restrictions, or anti-abuse measures. Do not use a visible authenticated session merely because it is convenient: it can interrupt the user's work and increases privacy and account risk.

If automated access is blocked, do not attempt to defeat the site's protections for research or routine collection. For a specific task the user explicitly requested, an authorized visible session may be appropriate if it is necessary to complete legitimate work. Do not weaken browser security, warnings, multi-factor authentication, or access controls.

## 3. Protect authenticated browser context

When controlling a visible browser, announce the action and purpose before taking control. For example: “I am using the authorized account session to update the requested setting.” This provides notice without requiring the user to repeat approval already given for the task.

Use a fresh tab, separate window, or isolated tab group unless the user explicitly directs work in an existing tab. This reduces the chance of disrupting unrelated work, altering the wrong page, or exposing unrelated content.

Classify the context before opening the target:

- Personal, work, test, staging, production, or another named environment.
- The relevant organization or account.
- The target page, record, setting, or workflow.
- Whether the work is read-only, reversible, or consequential.

Select a browser profile or connection that explicitly matches this context. Never infer identity from a generic browser name, remembered default, old tab title, connection label, or most-recently-used profile. If the automation environment provides profile metadata, use it; then verify the signed-in account through a reliable in-page account indicator before opening or changing the real target.

Use an account preflight gate before any data-changing action:

1. Confirm the signed-in account or identity.
2. Confirm the organization and environment.
3. Confirm the exact target object and intended action.
4. Mark the context as verified only after the preceding checks pass.

Do not create a verification marker, unlock a tool gate, or claim verified context before doing the actual account check. A useful pre-action question is: **Which account is this? Which environment is this? What exact item will change?** Resolve uncertainty before acting.

## 4. Define the task boundary and authorization

Determine the intended outcome before navigating deeply. Identify:

- The target page, form, record, setting, or workflow.
- Information that will be entered, collected, changed, uploaded, or sent.
- The minimum information needed to complete the request.
- Missing information or choices that require the user's judgment.
- Whether the final action is reversible.
- Whether the task sends, publishes, pays, deletes, grants access, changes billing, or creates another external commitment.

Separate **preparation** from **commitment**. Filling fields, drafting text, collecting a preview, and configuring a reversible setting are often preparation. Submitting, sending, publishing, purchasing, deleting, or applying an irreversible account change are commitments.

Use authorization already provided in the request or standing instructions for actions clearly covered by it. Do not repeatedly ask for approval already given. If authority for a consequential final action is absent or ambiguous, prepare and verify the result without committing it, then ask only for the final action.

For permanent, paid, externally visible, or otherwise consequential actions, use two phases:

1. **Preparation pass:** Populate or configure the page, verify values, and capture a pre-action record. Do not activate the final control.
2. **Commitment pass:** After explicit confirmation when needed, re-check the account, target, readiness conditions, and final control. Perform the action once, then verify the outcome.

If the page reloads, re-renders, or the session changes between phases, do not assume earlier state remains valid. Reinspect and verify again.

## 5. Inspect the rendered page before editing

Do not begin by guessing selectors, filling fields by numeric position, or trusting a visual approximation. Inspect the rendered page first and collect enough structure to identify every relevant control safely.

For each relevant control, determine:

- Its type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date/time picker, upload control, or custom widget.
- Its accessible name, visible label, placeholder, or label relationship.
- Its current value, required state, disabled state, and validation state.
- Its formatting rules, character limits, and whether it accepts multiple lines.
- Whether it is the true editable control, an accessible wrapper, or a hidden synchronization field.
- Whether a change to it can refresh dependent fields or re-render the form.

Address controls by stable semantic identity: a visible label, accessible name, explicit label relationship, or another durable meaning-bearing identifier. Do not rely on DOM position where labels are available. Dynamic applications may change control order after loading or after a dependent selection changes.

Before changing an existing record or setting, inspect its current state. This prevents accidental overwrites and helps ensure the correct target is being changed.

### Generic inspection pattern

Use the chosen browser automation capability to record at least the control tag, input type, role, label, required state, disabled state, and readable value or text length.

```js
// Pseudocode: adapt to the selected browser automation library.
const controls = inspectAll('input, textarea, [contenteditable="true"], [role="textbox"]')
  .map((element) => ({
    tag: element.tagName,
    type: element.type || element.contentEditable,
    role: element.getAttribute('role'),
    label: accessibleLabel(element),
    required: element.required || element.getAttribute('aria-required') === 'true',
    disabled: element.disabled || element.getAttribute('aria-disabled') === 'true',
    valueLength: readableValue(element).length,
  }));

saveJson('before-state.json', controls);
```

Structural inspection does not replace checking visually meaningful state such as selected recipients, file names, totals, dates, warnings, confirmation text, or error banners.

## 6. Match the interaction to the control

A generic “set value” operation is not reliable for all controls. Use the interaction model the page expects.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use normal text input. | Newlines may be removed silently. |
| Multiline text area | Enter or fill text, then move focus away. | The application may commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select existing content, enter through keyboard-style events, then blur. | Direct DOM writes may not update the application's model. |
| Dropdown or combobox | Open it, select by visible option text, and wait for the state to settle. | The selection may trigger a re-render. |
| Checkbox or radio group | Read state first; change only if needed. | A blind click can undo a correct selection. |
| Date/time picker | Choose the value, close normally, then verify the rendered summary. | Typing or closing the widget may alter related values. |
| File upload | Confirm file, destination, audience, and privacy impact first. | Uploading may start immediately and be difficult to reverse. |

For framework-driven editors, prefer ordinary user-like interaction over low-level property writes. A robust sequence is:

1. Locate the actual editable element rather than an accessible wrapper.
2. Focus it.
3. Select and remove existing content if replacement is intended.
4. Enter the intended text through keyboard-style input.
5. Move focus to a neutral page element so the application can commit the value.
6. Wait briefly if the control re-renders.
7. Read the resulting page state back.

Some forms place a visible editor near a hidden input used for internal synchronization. Editing the hidden input can look successful in a DOM inspection while server-side validation treats the visible editor as empty. Target the actual interactive control the application reads. If an accessibility locator returns an empty wrapper, inspect the labeled underlying editable element.

If dropdowns, checkboxes, dates, tabs, or other controls can refresh a form, set and verify those dependencies **before** entering long or complex text. Reinspect afterward and confirm that earlier entries remain present.

## 7. Verify every meaningful edit

After each field is filled or setting is changed, read it back from the page and compare it with the intended result. For sensitive content, compare length, required state, a redacted summary, or a minimal matching signal rather than copying full text into logs.

Look for these mismatches:

- The automation layer reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated due to the wrong control type or a length limit.
- A custom editor showed text but did not retain it internally.
- A later interaction erased an earlier entry during a re-render.
- A hidden synchronization field was changed instead of the actual editor.
- A selection changed a dependent recipient, date, quantity, price, or validation rule.

If verification fails, do not continue toward submission. Diagnose the control type and retry once with a more appropriate interaction method, then verify again. If the page continues to reject or alter the content, report the limitation and ask how to proceed rather than silently submitting inaccurate data.

Do not depend on the system clipboard in headless or restricted environments. Use the chosen automation input mechanism and verify the result on the page. Keep secrets out of scripts and logs; use an approved secure input channel when secret entry is necessary.

## 8. Run a pre-submit readiness gate

Before a submission or high-impact change, inspect the complete relevant page state again. Confirm:

- The correct account, organization, environment, and target are active.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Recipients, dates, attachments, quantities, options, and dependent fields are correct.
- No validation errors, unexpected warnings, or unsaved-change indicators remain.
- The final control has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially prepared form is recoverable; an incorrect external action may not be.

Capture a pre-action record for consequential work: a screenshot, concise state summary, or structured field dump. Keep it within the appropriate access boundary. Do not expose sensitive form contents in a large inline table when a concise summary and securely stored record are sufficient.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists when the action is consequential.
- [ ] The final action and its impact are understood.

## 9. Handle one-way actions distinctly

The following generally need explicit confirmation immediately before the final control is activated, unless clear standing authorization covers that exact action:

- Sending messages, invitations, notifications, or applications.
- Publishing content or making an external change visible.
- Submitting an official or externally reviewed form.
- Making a payment, purchase, reservation, or order.
- Deleting records or files.
- Changing subscription, billing, access, ownership, or security settings.
- Actions labeled permanent, final, irreversible, or impossible to edit later.

Ask concisely. State the target, important values, recipients or audience, cost if any, irreversible effects, and unresolved questions. For low-risk reversible changes explicitly requested by the user, proceed after normal verification unless the page presents an unexpected warning or broader impact.

## 10. Confirm completion and report accurately

A button click is not proof of success. After acting, look for durable evidence such as a confirmation reference, a newly created or updated record, a sent or published item in its destination, a persisted setting after a safe reload, or a status transition consistent with the requested action.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic; blind retries can create duplicates, extra messages, repeated orders, or duplicate charges.

If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Never describe an attempted action as completed.

## 11. Common failures and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank | The application ignored a direct value change. | Use focus-and-keyboard interaction, blur, and read back. |
| Earlier fields disappear after a later edit | A re-render reset uncommitted state. | Commit and verify each field; make re-rendering selections first. |
| Text loses lines or characters | The control type or formatting rule is unsuitable. | Find the correct multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node. | Inspect the labeled underlying control and target the true editor. |
| A field looks populated but validation says it is empty | A hidden synchronization field was edited. | Use the visible interactive control the application reads. |
| Automation becomes unstable on a complex page | The selected automation layer is unsuitable. | Switch to a more robust approved method or direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers differ | The site varies by browser context. | Prefer an authorized direct interface; use a verified visible session only for an explicit legitimate task. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior. | Close through a neutral page action and re-verify affected fields. |
| A visible error appears after an action | The action may already have persisted or be delayed. | Inspect resulting state before retrying. |
| Account context is uncertain | The wrong profile or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
- [ ] Explicit confirmation was obtained for an unapproved consequential final action.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.


---
name: create-an-ai-skill
description: Design, test, improve, evaluate, and package reusable AI skills from a new idea, an existing draft, or a demonstrated workflow.
---

# Create an AI skill

Use this workflow to create a reusable AI skill, revise an existing skill, evaluate whether it helps, or improve how reliably it activates. A skill is a focused package of instructions and optional supporting resources that helps an AI perform a recurring job consistently.

The core loop is:

1. Identify the job, boundaries, and current stage.
2. Draft or revise the skill.
3. Test it with realistic requests.
4. Review representative outputs with a person and measure objective requirements where useful.
5. Improve the skill based on evidence.
6. Repeat until the skill is useful, reliable, and not narrowly fitted to its test prompts.
7. Optionally evaluate and improve the description used to activate the skill.
8. Package and hand off the finished skill.

Adapt the level of rigor to the user’s goals. Some users need a quick collaborative draft; others need repeatable comparisons and documented evidence. Do not force a large evaluation on someone who wants an exploratory session, but explain the tradeoff: less testing provides less confidence that the skill will work across normal variations.

## Operating principles

### Communicate at the user’s level

Use plain language by default. Terms such as *evaluation* and *benchmark* are often understandable, but define them briefly when useful. Do not assume familiarity with technical terms such as structured data, pass/fail checks, data schemas, command-line tools, or automated testing.

Explain why important questions matter. For example:

> What should a successful result look like: a chat response, a structured report, a file, or an approved action? The answer determines how the skill should be written and tested.

Keep the user involved in choices that affect scope, risk, output style, capabilities, permissions, or approval requirements.

### Maintain a visible work plan

If a task tracker, checklist, or planning mechanism is available, create a short plan and keep it current. For a full evaluation cycle, include at least:

- Confirm scope and success criteria.
- Draft or revise the skill.
- Create realistic test cases.
- Run tests and comparison conditions when supported.
- Prepare materials for human review.
- Analyze feedback and measurements.
- Revise and retest.
- Package the final version.

A checklist prevents important steps, especially result preservation and human review, from being skipped. It should not replace judgment.

### Respect authorization, privacy, and user expectations

If the workflow uses private communications, records about people, customer information, operational data, or other non-public material, establish a legitimate purpose and clear authorization first. Use only the minimum relevant sources and information. Omit unrelated sensitive details from outputs, preserve appropriate access boundaries, and respect consent and privacy expectations.

Do not create skills that conceal actions, bypass safeguards, collect information without authorization, facilitate unauthorized access, or otherwise behave in ways a reasonable user would not expect from the description.

## 1. Determine the starting point

Identify which situation applies before deciding how much discovery or testing is needed.

### New skill

The user has an idea for a recurring job, such as preparing operational summaries or validating data files. Start with discovery, then create a first draft.

### Existing skill

The user has a draft, package, or instruction set and wants it simplified, extended, tested, or improved. Read the current version before proposing changes. Preserve its established name and identity unless the user asks to rename it.

If the current copy cannot be edited safely, create an editable working copy in an approved location. Preserve the original unchanged so it can serve as a comparison baseline and recovery point.

### Workflow demonstrated in the conversation

When the user asks to turn an earlier interaction into a skill, extract what is already known before asking repetitive questions:

- Inputs, files, and permitted information sources.
- Actions and capabilities used.
- The sequence of decisions and work.
- User corrections, preferences, and exceptions.
- Output formats and acceptance criteria.
- Conditions that changed the approach.

Summarize the inferred workflow, label assumptions, and ask the user to confirm important gaps. Do not turn a one-time workaround into a general rule without checking that it should apply broadly.

### Evaluation-only or activation-only request

A user may already have a complete-looking skill and ask whether it works, whether it improves results, or whether it activates in the right situations. Start with test design and evidence gathering. Do not rewrite merely because rewriting is possible.

## 2. Capture intent and scope

Gather enough detail to define a coherent job. Do not ask every question mechanically; begin with unknowns that most affect the design.

1. **Purpose:** What should this skill enable the AI to accomplish?
2. **Activation:** What requests, wording, situations, or files should cause it to be used?
3. **Inputs:** What information, files, systems, references, and permissions may it use?
4. **Outputs:** What should it create, return, modify, or recommend? Is a format required?
5. **Success criteria:** How will the user know the result is correct, safe, and useful?
6. **Boundaries:** What should it not do? When should it ask, pause, decline, or hand work back to the user?
7. **Variation:** What common alternatives, difficult cases, or failure conditions matter?
8. **Dependencies:** Does it need a particular capability, template, reference, script, or environment?
9. **Testing:** Should it be tested with representative requests before release?

Useful follow-up choices include:

- Should the skill make a clearly labeled best-effort assumption, or ask when required information is missing?
- Should it provide a concise result, a detailed result, or let the user choose?
- Should it use any accessible source, or only sources explicitly approved by the user?
- Does an external action require confirmation before it is performed?

Recommend test cases when outputs are objectively checkable, the workflow is consequential, or the skill will be used repeatedly. For subjective or creative work, favor representative review over misleading numerical scoring.

### Research before drafting

If relevant documentation, similar skills, reference materials, or domain guidance are available and approved for use, inspect them before drafting. Research should reduce burden on the user, not replace their authority over requirements.

Use research to identify:

- Existing output standards and conventions.
- Constraints imposed by input formats or available capabilities.
- Safe reusable patterns for comparable tasks.
- Approval, privacy, compliance, and audit needs.

When evidence conflicts or a requirement is uncertain, surface the uncertainty. Do not present a guess as a verified rule.

## 3. Choose the package structure

Keep each skill focused enough that its purpose and boundaries are predictable. Support variants of the same job in one skill when they share a workflow and completion criteria. Split unrelated jobs when they have different users, permissions, sources of truth, or definitions of success.

A portable package often follows this layout:

```text
skill-name/
├── SKILL.md                 # Core instructions
├── scripts/                 # Optional repeatable helpers
├── references/              # Optional detailed documentation
├── assets/                  # Optional templates and output resources
└── evals/                   # Optional test cases and grading material
```

Use progressive disclosure:

1. **Metadata** gives the name and short activation description.
2. **Core instructions** provide the normal workflow.
3. **Resources** hold detailed references, templates, and executable helpers consulted only when relevant.

Keep the core instruction file readable. If it becomes too long, move domain-specific detail into clearly named references and state exactly when each reference should be read. Long reference documents should include useful navigation, such as a table of contents.

For a skill that supports multiple environments or variants, keep shared decision logic in the core instructions and separate the variant-specific details. The AI should select the relevant reference rather than loading every variant by default.

### Bundle deterministic work only when it earns its place

If test runs repeatedly reconstruct the same transformation, validation, or file-generation procedure, consider a reusable script or template. It is especially valuable when it is deterministic, safer, faster, or easier to verify than repeated natural-language reasoning.

Document each resource’s purpose, inputs, outputs, limitations, and when not to use it. Do not add automation simply because it is possible. It must remain within the intended authorization and access scope.

## 4. Write the skill

Write clear, action-oriented instructions. Explain the reason behind important safeguards and quality checks. A capable AI can adapt better when it understands the goal and tradeoff than when it receives unexplained rigid commands.

A useful skill commonly contains the following sections.

### Purpose and scope

State the job, intended outcome, expected user, and boundaries. Clarify whether the skill creates an answer, generates a file, changes a system, or guides a user through a process.

### Inputs and prerequisites

List required information, approved sources, capabilities, permissions, and optional inputs. State what happens when a required item is absent.

```markdown
Before preparing the report, confirm the reporting period and the approved source material.
If a required source is unavailable, ask for an export or provide a clearly marked incomplete draft.
```

### Workflow

Provide the normal sequence of work and meaningful decision points:

1. Inspect the request and available inputs.
2. Ask focused questions only when the answer materially changes the result or risk.
3. Gather evidence from approved, relevant sources.
4. Perform the task using the appropriate method.
5. Check the output against requested format, evidence, and success criteria.
6. Deliver the result with assumptions, limitations, and required follow-up.

Use conditional guidance rather than trying to enumerate every possible circumstance:

```markdown
If the user provides a required template, follow it.
If no template is provided, use the default structure below.
If a proposed action could overwrite, publish, or otherwise materially affect work, explain the impact and request confirmation first.
```

### Output format

Define an exact template when predictable structure is valuable:

```markdown
# [Title]

## Summary
[Short overview]

## Findings
- [Finding with supporting evidence]

## Recommendations
1. [Action]

## Assumptions and open questions
- [Uncertainty or requested follow-up]
```

Do not impose a rigid shell when usefulness depends on adapting to the request. In those cases, specify outcome goals and provide a small generalized example.

### Quality, privacy, and safety checks

Specify what must be checked before completion. Examples include required fields, calculation validation, source attribution, preservation of originals, access boundaries, and clear labeling of uncertainty.

For workflows involving people, hiring, or assessment, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Avoid irrelevant personal details and loaded language when characterizing people or assessment outcomes.

### Failure behavior

Describe recovery behavior in general terms:

- **Missing or conflicting input:** Name the gap and ask a focused question.
- **Unavailable capability or reference:** Explain what cannot be verified and offer an alternate method if appropriate.
- **Ambiguous request:** Make a low-risk assumption only when it will not materially affect the outcome; otherwise ask.
- **Validation failure:** Do not present the work as complete. Correct it, report the issue, or request guidance.
- **External or high-impact action:** Pause for explicit confirmation before proceeding.

### Examples

Include only a few short generalized examples when they teach a distinct pattern. Examples should illustrate reasoning and output shape, not substitute for a broad workflow.

## 5. Write a strong activation description

The description is a routing mechanism: it helps the AI decide when the skill applies. State both what the skill does and when to use it.

Cover realistic ways users express the need, including requests that imply the job rather than naming it exactly. Make the description specific enough to activate for useful cases without swallowing nearby work that belongs to another skill.

A good description includes:

- The task or desired outcome.
- Common contexts and phrasing that signal relevance.
- Important scope limits that prevent costly false activation.

Example pattern:

```text
Create clear project status reports from approved updates and source material. Use for requests involving progress summaries, leadership updates, milestone reviews, risks, next steps, or concise accounts of project health, even when the user does not say “status report.”
```

Keep detailed procedure in the body, not the description. The description should be accurate, useful, and honest about scope.

## 6. Review the draft before testing

Read the draft as though encountering it for the first time. Check that:

- The job is coherent and bounded.
- The description explains activation conditions.
- Inputs, permissions, and outputs are clear.
- Important rules explain their purpose.
- Instructions address missing information and failed validation.
- The skill does not assume one person’s habits, local files, private access, or preferred terminology.
- The skill has enough flexibility for normal variation.
- The instructions do not contain redundant steps or rules that do not affect outcomes.

Prefer a lean instruction set over a long set of brittle commands. Frequent emphatic language is a warning sign unless the requirement is truly non-negotiable, such as an authorization or safety boundary.

## 7. Design realistic tests

Once the draft is stable enough to test, create two or three realistic prompts and show them to the user before relying on them. Ask whether they resemble real requests and whether an important scenario is missing.

For each test, preserve:

- A descriptive identifier.
- The complete user prompt.
- Relevant supplied files or context.
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
      "expected_output": "A structured summary that distinguishes verified updates from missing information.",
      "files": [],
      "assertions": []
    }
  ]
}
```

Cover distinct situations rather than superficial wording changes:

- A normal successful request.
- Incomplete, ambiguous, or conflicting input.
- A formatting or constraint-sensitive request.
- A realistic case that changes the workflow.
- A case that should require approval, protective handling, or a refusal when relevant.

Avoid tests that merely repeat words from the instructions. Vary user phrasing, level of detail, and context.

## 8. Run tests and comparisons

When independent runs are available, compare the skill against a meaningful baseline.

- **New skill:** Run each test with the skill and without the skill.
- **Existing skill:** Preserve an unchanged snapshot before editing, then compare the revised version with the original or another clearly identified baseline.

Start both conditions for all test cases under comparable circumstances. If parallel execution is available, launch both conditions together. This makes timing comparisons fairer and avoids changing the baseline after seeing the skill’s result.

Use a clear iteration structure, such as:

```text
workspace/
├── iteration-1/
│   ├── standard-request/
│   │   ├── with-skill/
│   │   └── baseline/
│   └── incomplete-input/
│       ├── with-skill/
│       └── baseline/
└── iteration-2/
```

For every test condition, preserve the prompt, supplied files, outputs, and available run information such as elapsed time and resource use. Record timing and resource data immediately when the runtime reports it, because some environments do not retain it later.

Store per-test metadata, including its descriptive name, prompt, and current objective checks. This enables consistent grading across iterations.

If independent runs are not available, perform a transparent sanity check: follow the skill for each test request, save the outputs, and obtain user feedback. Do not call this a rigorous baseline comparison.

## 9. Define and grade objective checks

While test runs are in progress, draft objective checks rather than waiting idly. Explain them to the user before treating them as success criteria.

Good checks are observable, meaningful, and clearly named. Examples:

- Required sections are present.
- A file opens and contains required fields.
- Calculations match an approved source within an agreed tolerance.
- The response identifies missing mandatory inputs.
- Key claims include source references where required.

Record each grade using a stable shape:

```json
{
  "expectations": [
    {
      "text": "Includes an assumptions section when required source information is missing.",
      "passed": true,
      "evidence": "The final section identifies unavailable data and requests follow-up."
    }
  ]
}
```

Use a programmatic check when feasible. Automated checks are more repeatable than visual judgment and can be reused in later iterations. For subjective work such as writing quality, design, strategic usefulness, or tone, rely primarily on informed human review. Do not force a weak numeric proxy that encourages the skill to optimize for the measure instead of user value.

## 10. Present results for human review

After runs complete, grade results, aggregate useful measures, and present both outputs and measurements for review. Use an available review method that lets the user inspect outputs, compare conditions, see grades, and leave feedback. If no dedicated review interface is available, provide accessible files or a clear in-conversation review.

For each case, show:

- The prompt and relevant inputs.
- The skill output and comparison output, if any.
- Objective grades and supporting evidence.
- Timing or resource data, if available.
- Prior iteration output and feedback when comparing revisions.

Explain what the reviewer will see and how to provide feedback. Useful questions include:

- Which output would you trust in normal use, and why?
- What was missing, misleading, or difficult to use?
- Did the skill add effort or detail that did not create value?
- Would the result work for similar requests with different data or wording?

If feedback is exported as a file, place it with the iteration materials and read it before revising. Empty feedback commonly means the reviewed output was acceptable, but it is not proof that all cases are solved.

Close temporary review services after feedback has been captured.

## 11. Analyze beyond aggregate scores

Aggregate results where possible: pass rate, elapsed time, resource use, variation, and differences between conditions. Place the revised skill before its comparison condition in reports for easy reading.

Then perform an analyst pass. Look for patterns aggregate statistics can hide:

- **Non-discriminating checks:** Both conditions pass, so the check does not show the skill’s contribution.
- **High variation:** Similar runs differ greatly, suggesting ambiguity, instability, or unreliable instructions.
- **Tradeoffs:** Quality improves, but at disproportionate cost in time or resource use.
- **Failure concentration:** Several failures share one root cause, such as unclear source selection.
- **Unproductive work:** Execution records reveal repeated planning, redundant research, or unnecessary formatting.
- **Repeated reconstruction:** Multiple runs independently rebuild the same helper procedure, indicating a useful script or template may be missing.

Treat a small test set as directional evidence, not final proof.

## 12. Improve without overfitting

Base revisions on feedback, outputs, and analysis. Change the smallest part likely to address the underlying cause.

Generalize from feedback. If one test omitted a source note, do not write a rule about that exact test. Instead, clarify the broader condition: when evidence is incomplete or mixed, distinguish verified information from assumptions and unknowns.

Use these improvement principles:

1. **Fix causes, not examples.** Design for future requests, not the current test wording.
2. **Keep the prompt lean.** Remove guidance that does not improve behavior or causes wasted effort.
3. **Explain intent.** State why a step protects quality, usability, safety, or trust.
4. **Add reusable resources selectively.** Bundle templates, scripts, and references only when repeated work proves their value.
5. **Preserve useful behavior.** Do not lose what users already value while correcting a weakness.
6. **Expand coverage gradually.** Add a test when it represents a real class of failure, not every isolated incident.

After revision, rerun the applicable full test set in a new iteration. Use the same baseline policy, preserve earlier outputs for comparison, collect feedback, and repeat.

Stop when the user says the skill is ready, feedback is consistently positive across meaningful tests, objective requirements are reliably met, or further revisions no longer create meaningful improvement.

## 13. Optional blind comparison

For a more rigorous comparison of two versions, use blind review. Give an independent evaluator two outputs without revealing which version produced each output. Use a shared rubric tied to user value: correctness, completeness, clarity, constraint adherence, safety, and practical usefulness.

Use blind comparisons when versions have similar measurements but visibly different quality, when evaluator bias is a concern, or when the decision is important. Record the reasoning before revealing which output came from which version, then analyze why the preferred output won.

## 14. Optimize activation behavior

Only optimize the description after the skill’s workflow itself is useful.

Create a realistic, roughly balanced set of activation queries: some that should activate the skill and nearby cases that should not. Include enough detail that consulting a skill would actually help.

Positive cases should cover formal and casual phrasing, direct and implied requests, common and uncommon valid uses, and cases where another related skill might compete.

Negative cases should be difficult near-misses, not irrelevant requests. They should share concepts or wording with the skill but require a different job, different capability, or different conditions.

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

Review the query set with the user before running it. If an evaluation capability supports repeated activation trials, evaluate candidate descriptions repeatedly, separate queries used to improve the description from held-out queries used for selection, and choose the description that performs best on held-out cases.

A simple one-step request may not activate a specialized skill even with a matching description because an AI can complete it directly. Use substantive test queries where the skill would add genuine value.

Show the user the description before and after optimization, along with results and known limitations.

## 15. Package and hand off

Package the core instructions and only the resources needed for normal use. Before delivery, audit the package:

- The name is stable and appropriate.
- The activation description accurately represents scope.
- Instructions do not depend on private conventions, undeclared capabilities, or unapproved access.
- Resources are present, clearly named, and documented.
- No credentials, private records, identifiers, confidential examples, or unnecessary sensitive material are included.
- Evaluation materials are included only when safe and useful.
- The user can install, access, or adapt the package in their chosen environment.

Provide a short handoff note that states what the skill does, required capabilities, known limitations, and a simple post-installation test.

## Final readiness gate

A skill is ready when it has a clear job, a description that activates for appropriate requests, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic use that it improves outcomes.

Do not confuse a long instruction file with a reliable skill. The goal is a reusable workflow that helps an AI make better decisions and deliver better results for recurring user work.


---
name: test-every-screen-size
description: Verify every UI or CSS change across representative widths, heights, content states, screenshots, and layout checks before reporting it complete.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to a one-line spacing, color, or background change: a local edit can alter wrapping, height, overflow, alignment, or visible backgrounds elsewhere.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Real screenshots and programmatic checks catch different failures, so require both.

## Why this is required

A layout can appear correct at one size while failing at another:

- viewport-height rules can create blank space on unusually tall screens;
- a split layout can fail at intermediate widths even when narrow and wide layouts pass;
- making a surface full-bleed can reveal leftover margins or wrapper padding as visible strips;
- empty states can hide collisions, clipping, and overflow that realistic content exposes.

Treat screenshots as visual ground truth and layout measurements as complementary evidence.

## 1. Prepare representative states

Run the interface in a safe test environment and populate the affected surface with realistic content before testing. Use the minimum test data needed for the layout; do not include unrelated or sensitive personal information.

Include, when relevant:

- long paragraphs, formatted content, long field values, and long unbroken strings;
- representative lists, cards, rows, and item counts;
- validation messages, helper text, and error states;
- loading and empty states when the change affects them;
- content near expected limits, such as a long output block or a dense card list.

Do not validate only an empty or unusually clean state. Sparse content can conceal clipping, overlap, poor wrapping, and unintended blank regions.

## 2. Select the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages, large-display workflows, or layouts expected to expand widely.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Also test any known target viewport supplied by the user or product requirements. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable method that can set exact viewport dimensions, load the intended page state, capture screenshots, and collect layout measurements. Prefer a non-interactive run for reproducibility unless visual debugging requires direct interaction.

## 3. Capture and inspect screenshots

Capture real screenshots at every relevant viewport and state. Use full-page screenshots when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect the changed component and its immediate surroundings on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does this match the intended design now that the element's role has changed?

Pay special attention to edge-to-edge or full-bleed changes. A component that becomes flush with one edge may expose old margins or wrapper padding on another edge as a visible background strip. Check every edge, not just the edge edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS seems logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow where the screen is intended to fit the viewport;
- no changed element overlaps adjacent content, its container, or essential controls;
- buttons, links, inputs, and other interactive controls remain visible and usable;
- fixed or sticky UI does not hide essential content;
- cards, lists, and form controls remain within intended bounds;
- body text retains a readable line length.

For a fit-to-viewport design, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare bounding rectangles of relevant siblings, containers, and controls rather than relying on a single page-wide rule.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is approximately 80 characters per line; reading-focused designs commonly target roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visible defects such as exposed background strips, poor visual balance, and unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both of these pass:

- visual inspection of the applicable screenshot; and
- relevant programmatic layout and usability checks.

## 6. Fix failures and rerun

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a viewport-specific cosmetic patch;
4. rerun the full relevant sweep, not only the failing size.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is incomplete; do not keep layering patches until individual screenshots happen to pass.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights and states, and the checks performed.

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

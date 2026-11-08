# AI skills

Public, reusable workflows. Review and adapt them to the user rather than installing every file blindly. Licensed CC0 1.0 for reuse without permission or attribution.


---
name: brainstorm
description: Generate genuinely distinct options for a decision, weigh their tradeoffs honestly, and recommend a short ranked set. Use when someone asks for options, alternatives, or ways they could approach something.
---

# Brainstorm options

Use this workflow when someone needs credible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas. It is to surface genuinely different paths, show their tradeoffs clearly, and leave the user with a small set of meaningful choices.

## 1. Gather relevant context

Begin with the information the user supplied. If they provide links, documents, discussion records, prior decisions, research, or other accessible materials, review only the sources relevant to the decision.

If the question is not self-contained, retrieve a small number of high-value sources that may materially change the options, such as:

- Earlier decisions and the reasons behind them
- Existing commitments, deadlines, budget limits, or technical constraints
- Evidence about what has already been tried
- Relevant stakeholder needs, ownership boundaries, or approval requirements

Use private communications or records only for a legitimate purpose and with clear authorization. Use the minimum relevant information, omit unrelated personal or sensitive details, and keep the output within the appropriate access boundary.

Do not search broadly by default. If key information is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- What the user is actually deciding
- Important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should distinguish options

The stated request may describe a symptom or a preferred solution rather than the underlying choice. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited budget and timeline?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly requests an immediate first pass. A wrong framing produces irrelevant options.

## 3. Generate distinct options

Generate five to seven options unless there are genuinely fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes the process, incentives, scope, or framing
- At least one surprising but credible path, such as delaying, partnering, narrowing scope, observing longer, or doing nothing

Do not be contrarian merely to appear creative. A “do nothing” option is useful only when waiting, learning, timing, or avoiding distraction has real value.

Give every option a short, memorable label that makes its approach clear. For each option, provide:

- **What:** One or two sentences describing the approach
- **Strengths:** One or two concrete advantages
- **Weaknesses:** One or two concrete disadvantages, constraints, or failure risks
- **Effort:** Low, Medium, or High

Be candid. Do not soften serious drawbacks or describe alternatives unfairly to favor a preferred option.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include expected impact, cost, effort, speed, risk, reversibility, strategic fit, confidence in evidence, and burden on affected people. Add domain-specific criteria when they matter more.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are instructive, but clearly explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, state in one sentence why it fits this situation, constraints, and goals—not merely why it is attractive in general.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the options and recommendations, wait for the user. They may:

- Choose an option
- Request more detail on one option
- Correct the framing or constraints
- Ask for additional options
- Propose a hybrid approach

For a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or hard-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term obligations, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that states the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move to planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The decision framing reflects the real choice rather than only the requested solution
- The options are genuinely distinct
- The obvious option and a credible alternative framing were considered
- Weaknesses and effort labels are plausible and candid
- Recommendations follow the user’s stated criteria and constraints
- Uncertainty, missing evidence, and assumptions are visible
- The output does not make an implementation commitment before the user chooses


---
name: pressure-test
description: Finds the weak points in a strategic idea before you commit, through a steelman, assumption tests, a pre-mortem, and a verdict. Use when you say pressure-test this, stress-test this, or am I wrong.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or create an implementation plan.

## Quick version

- Restate the idea in its strongest form, and confirm it still means what was intended.
- List three to five assumptions it depends on, ranked by how much damage each would cause if wrong.
- Ask five to eight hard questions one at a time, and push back on vague answers before moving on.
- Imagine the idea failed and name the three most likely reasons, each with an early warning sign.
- Name who would disagree and what would change the decision-maker's mind. If nothing would, the test has failed.
- Give a GREEN, AMBER, or RED verdict and one concrete next action with a verb and an owner.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document a decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes defending it.
- If the idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings in the decision.
- Every verdict must name the next step. Do not end without a handoff.

If the test draws on internal messages, records, research, or feedback about other people, have a legitimate purpose and clear authorization to use them. Review only the minimum relevant material, leave unrelated or sensitive personal details out of the output, and keep the results within the intended access boundary.

## Rules of engagement

- Be direct. Confidence is not evidence. The goal is to be the colleague who says the idea is weak, not the one who nods.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before continuing. Do not present the full question set as a questionnaire, because that invites cherry-picking.
- Use available evidence: metrics, experiments, research, customer feedback, prior decisions, and relevant stakeholder input. If a prior record contradicts the claim, surface it. Separate facts, inferences, and forecasts.
- Identify dissenters by relevant role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. If the decision-maker knows the actual people, ask them to name who would push back. Do not invent their views.
- Keep it terse. Skip a section only when genuinely irrelevant, and state why: "Skipping: not applicable because [reason]."
- Write dates in one consistent, unambiguous format.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the actual intent. Include the action, expected result, mechanism, timeframe, and conditions required for success.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold. Rank them by the damage caused if wrong, with the most consequential first. These are the targets for the forcing questions. Make assumptions observable where possible.

| Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|
| [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Test or disproof method] |

Replace broad statements such as "customers will value this" with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Select questions based on the highest-risk assumptions and adapt later questions to the answers.

Possible question categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed, here or elsewhere, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that role say, and has the objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or disruption? Weeks, quarters, or years?
- **Null option:** What happens if no action is taken for the next three months?

The time windows above are adjustable defaults; pick ones that fit the decision's pace. Push for specificity. "I think it will work" is not evidence; ask for observed behavior, data, a comparison, or a credible commitment.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood, most likely first. Cover a wrong premise, execution risks, and external conditions where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable early signal] | [Check or accountable role] |

A warning sign must appear early enough to permit a course correction, and it should be something the decision-maker can watch for now.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree and state each role's strongest likely objection. If that perspective has not been sought directly, mark it as an evidence gap. Silence is not agreement.

Dissent is not an automatic veto. Its purpose is to reveal constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require the decision-maker to state, in one sentence, the evidence that would reverse or materially alter the position:

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test incomplete or failed rather than approving the idea.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next step:

- **GREEN: proceed to decision.** The steelman survives, core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible test, such as one conversation, one document review, a small interview set, a prototype, or a short data-collection period. Run the test, then decide with the gap and its result recorded in the rationale. Do not skip to the decision while the gap is open.
- **RED: stop, redesign, or reopen options.** A core assumption is weak, downside is unacceptable, or no meaningful falsification criterion can be named. Generate alternatives, redesign the idea, or explicitly defer it with a trigger ("re-examine when [event] happens"). Do not treat RED as approval with caveats, and do not move to a decision on a RED verdict.

End with exactly one concrete next action on one line: a verb, an owner, and a deadline when useful. "Think about it" does not count.

> Example: `Research owner: interview five target users this week and compare findings against the adoption assumption.`

**Short worked example (fictional).** Maplestone Tutoring, an invented nonprofit, is leaning toward launching a paid premium tier.

- Steelman: "A paid tier with live sessions will fund two new free cohorts within a year, provided at least 5% of current learners convert."
- Top assumption: learners will pay for live sessions. Type: belief. Support: one enthusiastic survey comment. Damage if wrong: high.
- Forcing question: "What is the strongest evidence against this?" Answer: "Not sure, people seemed keen." Pushback: "Keen is not paying. Has anyone been asked to commit money?"
- Dissent: the finance lead may object that support costs grow faster than revenue. Not yet consulted, so it is a gap.
- Mind-change criterion: "I would drop this if fewer than 20 learners pre-register with a deposit by the end of next month."
- Verdict: AMBER. Next action: "Program lead: open a deposit-based pre-registration page by Friday."

## Final audit

Before closing, verify that the output contains:

- a confirmed steelman;
- three to five ranked load-bearing assumptions;
- five to eight forcing questions explored sequentially;
- a pre-mortem with early warning signs;
- credible dissenting roles and objections;
- a clear mind-change criterion;
- a GREEN, AMBER, or RED verdict with its next step; and
- one concrete next action.

Common failures include skipping alternatives, asking every question at once, mistaking confidence for evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, and issuing a favorable verdict without falsifiable criteria or monitoring.

## Optional extras

- **Connected sources.** If your assistant can search your document store, chat history, or notes, have it pull prior decisions, metrics, and past attempts relevant to the claim before Step 2, and cite them when they support or contradict an assumption.
- **Scheduled reviews.** For GREEN verdicts on hard-to-reverse decisions, have your calendar or task tool create a review reminder tied to the mind-change criterion's date.
- **Linked workflows.** If you keep separate workflows for generating options, deciding, and building, have each verdict name the exact one to run next so the handoff is automatic.
- **Improve the workflow over time.** After each run, review the transcript: note any question category that added nothing, any gap the process missed, or any step that ran too long. Update your own copy of this workflow based on that review rather than on general impressions.


---
name: decide
description: Matches decision rigor to stakes and reversibility, records the call with a testable prediction, and reviews it later. Use when asked to help decide, weigh X against Y, or review a past decision.
---

# Make a decision

Use this workflow to apply the right amount of rigor to a decision. Small choices get made quickly. Consequential choices get examined properly, recorded only with permission, and reviewed later without rewriting history.

## Quick version

- Ask what it would cost to unwind the choice. Sort it as trivial, reversible, hard to reverse, or direction-setting.
- If one urgent, reversible choice is bundled with a slower, harder one, split them. Answer the urgent part now and handle the harder part separately.
- For trivial choices, pick a sensible default with a one-sentence reason. For reversible choices, compare two or three options with one strength, one weakness, and rough effort each.
- For hard-to-reverse or direction-setting choices, pressure-test the leading option and check who disagrees before committing.
- Never claim the user leans toward or decided something they did not say. Keep the assistant's recommendation clearly labeled as the assistant's.
- When the user commits, write down a testable prediction, their confidence in it, the next action, and a review date set for when real results will exist. At review, judge the prediction and the process separately.

## 1. Ground rules

1. **Match rigor to stakes and reversibility.** Most decisions deserve minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user prefers, believes, or decided something they did not actually say.
3. **Separate advice from attribution.** Keep the assistant's recommendation distinct from the user's stated view. Include assistant analysis in a record only on request, and label it clearly.
4. **Record only with permission.** "Should we do X?" asks for analysis, not for a record. Create or update a decision record only when the user asks to log, track, open, resume, or commit it, or explicitly agrees.
5. **Do not mistake execution for a decision.** If there is no meaningful alternative, say so and move to planning or doing the work.
6. **Do not deliberate indefinitely.** Once appropriate evidence, challenge, and consultation are complete, make the call and proceed.

Before searching a shared decision register or reading communications, personnel records, or customer information about other people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and details, leave out unrelated or sensitive personal information, and keep outputs within an appropriate access boundary.

Before writing to a shared register, confirm its audience is appropriate. For sensitive matters, such as health, relationships, compensation, or confidential personnel issues, keep the discussion in chat or offer a private record.

## 2. Select the mode

Use the user's explicit instruction when they give one. Otherwise, if access is authorized, check the user's chosen decision record for a substantially overlapping decision before creating a duplicate.

- **New:** No matching record exists, or the user asks to start fresh.
- **Resume:** A matching record is open and the user wants to keep thinking.
- **Commit:** An open record exists and the user says they are ready to decide.
- **Review:** A resolved record has reached its review date and has no completed outcome assessment, or is still marked "too early."

Resolution status means whether the decision was made, not whether the outcome was good. For a non-binary question, mark it resolved once a direction has been chosen.

For **Resume**, retrieve the record, append a dated entry with new inputs, how thinking shifted, and where the user stands today, and add any new options. Do not overwrite prior reasoning. If the user wants to keep thinking, summarize the current state and ask what to explore next. If they are ready, move to commitment. For **Review**, use the original prediction, confidence, and stated assumptions as the baseline.

## 3. Frame the decision

Put the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What realistic options exist, including doing nothing?
- What deadline, event, or trigger requires a decision?
- What result is sought?
- What happens if no action is taken?

If the issue is broad and credible options do not yet exist, generate options first. Do not pressure-test a vague problem statement.

If only one viable path exists, say:

> This appears to be a task rather than a decision. The next step is to plan or execute it.

Ask one clarifying question at a time when scope is unclear.

## 4. Classify scope

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes; reversible within hours | Decide now; do not record by default. |
| Reversible | Moderate stakes; changeable within days or weeks | Compare a few options; use a light record if useful. |
| Hard to reverse | Significant cost, disruption, or loss if undone | Full analysis, challenge gate, and stakeholder check. |
| Direction-setting | Shapes strategy, culture, finances, or operations for an extended period | Full analysis, explicit dissent, and prerequisite conversations. |

When classification is unclear, ask: **What would it cost to unwind this?** Consider money, time, trust, operational disruption, opportunity cost, and reputation. If the unwind cost cannot be named quickly or is highly uncertain, treat the decision as larger. If the user calls a decision trivial but cannot explain how to undo it quickly, reclassify it rather than accepting the label.

**Split bundled decisions.** A request often mixes an urgent, reversible step with a slower, harder choice. Separate them. Answer the urgent step now as a reversible decision, then classify and gate the harder one on its own terms. This prevents urgency from rushing the big choice and prevents the big choice from blocking a simple step.

*Fictional example:* A manager at Tallowbrook Studio asks, "Should I tell the admin team to pause the lease renewal paperwork today, and should we move to a new building?" Pausing the paperwork for a week is reversible and time-sensitive, so it gets a quick answer: yes, pause it, because the renewal deadline is still a month away. Moving buildings is hard to reverse, so it goes through the full challenge gate separately.

## 5. Apply the appropriate rigor

### Trivial

Choose a reasonable default, state a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: attention spent may exceed the cost of an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. For each, state one main strength, one main weakness, and a rough effort or cost.
3. Give a recommendation and the decisive reason.
4. If uncertainty is material, identify the smallest reversible test that could change the call.

| Option | Main strength | Main weakness | Effort or cost |
|---|---|---|---|
| [Option A] | [What it enables] | [Central tradeoff] | [Rough estimate] |

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test covers assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and major stakeholder objections.

If no relevant pressure test has happened in the current decision context, stop the commitment flow and state:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Proceed only after the test is complete or the user explicitly overrides the gate with a reason. Urgency alone is not an override; if urgency is real, check whether a smaller reversible step can be split off instead.

If the pressure test finds a serious unresolved failure, do not force commitment. Return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and criteria.
2. Run a pre-mortem: "It is later and this failed. What most likely caused it?"
3. Check with people who have relevant expertise, bear consequences, or may reveal constraints.
4. Provide a recommendation labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees, and capture their strongest case fairly.

The decision is not ready until the prerequisite conversation has occurred, unless the user explicitly accepts and records a reason for proceeding without it. If it is rushed, name what evidence, consultation, or dissent is being skipped and why that matters.

For people-related decisions, use role-relevant capabilities, role alignment, diagnostic evidence, and whether any assessment distinguishes relevant performance. Do not rely on irrelevant personal information or unsupported labels.

## 6. Analyze without inventing certainty

For each serious option, capture what it enables; what it costs, delays, or prevents; its strongest supporting evidence and objection; its key assumptions; and the cost of reversal.

Separate non-negotiable requirements from preferences. Use scores only if they clarify tradeoffs rather than conceal judgment.

Keep these categories separate:

- **User's stated view:** Only what the user actually expressed.
- **Assistant analysis:** The assistant's recommendation and reasoning.
- **Open question:** Material uncertainty not yet resolved.

If the user has not stated a position, write "No position stated yet" or leave the field blank. Never fabricate a lean, confidence level, rationale, response to dissent, or final choice.

## 7. Commit and record

Before finalizing, confirm the choice, rationale, reversal conditions, next action owner and date, observable prediction, and the user's confidence in that prediction.

Use a testable prediction:

> By [date or trigger], [observable outcome] will happen or not happen.
> Confidence: [percentage].

Use the user's chosen register, document, or private file. A useful record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

For an **open** decision, record context, options, and new inputs, but leave commitment sections blank. For a **commitment**, mark it resolved, record the actual decision date, set confidence, and fill the commitment sections. Do not infer missing user-owned fields.

Suggested default review timing, adjustable: about one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Prefer a meaningful event or trigger if the user names one.

**Check that results will exist by the review date.** Before proposing a date, ask what will actually be observable by then. If the thing being decided will not yet have launched or produced outcomes, move the review to when early outcomes become visible, and frame it as a checkpoint on leading signals rather than a chance to re-decide.

*Fictional example:* Harrowgate Learning commits to starting a mentorship program next term. A default three-month review would land before the first cohort has met more than twice. The review moves to when early retention and participant feedback exist, and its question becomes "Are the early signals on track?" rather than "Should we have launched?"

For hard-to-reverse and direction-setting commitments, make sure a review reminder exists. In a plain chat, give the user a reminder-ready line to add to their own calendar or task list. Use one consistent, unambiguous date format throughout the record.

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
- User's stated position today: open / leaning / decided

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
The user's own reasoning, only when the user stated it. Be honest about intuition versus analysis.

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

If the user asks for assistant analysis to be stored, label it **Assistant analysis, not the user's position**.

## 8. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. If the review is a leading-signal checkpoint, compare those signals with expectations and keep the outcome as too early until real results exist. Do not treat an unfavorable result as proof of a bad process, or a favorable result as proof of a sound one.

## 9. Completion message

When a decision is made, summarize it:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences: the real reason, not a tidy story]
Next action: [owner] will [action] by [date]
Review: [date], or earlier if [trigger]
Record: [location, if one exists]
```

*Fictional example:*

```markdown
Decision: Run the spring workshop series online instead of in person.
Scope: Reversible
Rationale: Venue costs doubled and most past attendees were remote. We can return to in person next season if turnout drops.
Next action: Program lead will announce the format by 15 March
Review: 30 April, or earlier if signups fall below half of last season
Record: Team decision document
```

Use direct language. If the user is about to make a weak call, say so with evidence. Once the readiness gates are met, name the decision and move forward.

## Optional extras

- **Searching a connected register.** If your assistant can query a database or document store, check for overlapping decisions before creating a new one, and use any record template it provides so dates and sections fill consistently.
- **Automatic review reminders.** If a calendar or task tool is connected and authorized, create a reminder titled with the decision on the review date, linking to the record and alerting in advance (for example, one day before). For reversible decisions, a review-date field is usually enough.
- **Chaining with other workflows.** Pair this with an option-generation step before it and a pressure-test step for hard choices. If someone arrives with no options and an open-ended question, route them to option generation first.
- **Tuning the workflow.** After a few uses, note where classification, rigor, mode selection, review timing, or the record format misfired, and adjust your own version of these rules with the user's agreement.


---
name: solve-a-problem
description: Takes a non-trivial build or process problem from diagnosis to options, recommendation, and implementation. Use when someone says "build X" or "think it through, don't build yet".
---

# Solve a problem

Use this workflow to take a non-trivial build, integration, automation, process, or operational problem from understanding through options, a clear recommendation, implementation, and verification. It is meant for problems where the shape of the solution is not obvious, not for small fixes or routine tasks with a known implementation.

## Quick version

- Restate the underlying problem in your own words before discussing solutions: who is affected, what they are trying to do, what happens today, and how much it hurts. If the requested solution does not fit the problem, say so.
- Decide whether it is worth solving now, and flag any hard-to-reverse choices (data changes, public interfaces, long-lived settings, vendor commitments) for an explicit decision first.
- Write three to five lightweight evaluation criteria before generating ideas.
- Generate genuinely different options, always including "do nothing or defer" and a non-code option, plus small and larger technical versions.
- Compare options against the criteria in a short table and make one clear recommendation with reasons. Give it directly in the reply.
- If the user asked for analysis only, stop there. Otherwise plan, implement, verify, and report what was tested and what was not.

## When to use it

By default, work from understanding all the way through implementation. If the user says something like "just think this through, don't build yet," stop after the recommendation in Step 6 and wait for a decision.

Enter this workflow when the direction is already committed. If the user is still exploring what to do at all, first generate ideas, stress-test them, and make the decision, then come back here.

## 1. Understand the problem

Start with the underlying problem, not the user's proposed solution. If they ask to build something, work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is the problem?
- What outcome would make the situation meaningfully better?
- What constraints, dependencies, deadlines, or access boundaries apply?

Write a concise problem statement and descriptive requirements. Describe the desired outcome and constraints rather than assuming an implementation. If the proposed solution does not fit the problem, say so directly at this stage rather than building it and hoping.

Ask only for information that cannot be found in available project context, documentation, code, or records.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Include "do nothing," "deprioritize," or "improve the current workaround" as real options when appropriate.

Separate decisions by reversibility:

- **Reversible decisions:** Small choices that are easy to change. Use reasonable judgment, choose, and move forward without agonizing.
- **Hard-to-reverse decisions:** Persistent data changes, public interfaces, long-lived configuration, security boundaries, migrations, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the decision and rationale when the consequence warrants it. Do not quietly build a hard-to-reverse commitment inside an implementation task.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before creating new ones.

Identify constraints such as compatibility requirements, deployment practices, ownership boundaries, supported environments, security expectations, observability, and rollback needs. Use established system conventions unless there is a clear reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. For example:

- Must preserve existing authentication, privacy, and data behavior.
- Must fit available time, skills, and maintenance capacity (set the time budget that fits your situation).
- Should avoid new dependencies, persistent settings, and public surface area.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not small variations of the same design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution, such as clearer instructions, a process adjustment, a template, a better-organized view in an existing tool, a no-code automation, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Building, buying, or integrating an existing service.

For ambiguous or complex problems, generate a wider set of candidates before narrowing. Keep each option short: one or two brief paragraphs covering what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- **One code path over special cases.** A single path is easier to reason about, test, and debug, even if slightly less efficient.
- **Fail clearly on invalid states.** Validate inputs and use strict types. Do not hide programming errors by silently producing plausible but incorrect output.
- **Convention over composability over configuration.** Prefer established patterns, then flexible abstractions, and only then config-driven behavior.
- **Avoid permanent commitments.** New fields, settings, and public interfaces must be maintained indefinitely; treat them as hard-to-reverse decisions.
- **Make changes easy to delete.** Prefer loosely coupled, well-bounded changes that can be removed cleanly.
- **Use boring technology.** Prefer familiar, proven tools and existing infrastructure over clever or novel approaches.
- **Design for testing.** Favor determinism, and factor logic so it can be tested in isolation. Thinking through how you would test it often improves the design even if you do not write the tests yet.
- **Correct before fast.** Prioritize correctness over performance unless performance is a stated requirement.
- **Change things properly.** Make clean changes at the appropriate design boundary; avoid expedient patches that create future debt.

An invented illustration of the first principle, as a code comment:

```
# Every reminder goes through the job queue, even when the recipient
# is on the same server. A direct shortcut for local recipients would
# create two delivery paths, and bugs would only appear depending on
# where a request happened to land. One path is easier to test.
```

An invented illustration of what to avoid under the second principle:

```python
try:
    total = calculate_order_total(order)
except (ValueError, TypeError, KeyError, AttributeError):
    total = 0.0  # hides real bugs as a believable but wrong number
```

If `calculate_order_total` raises `AttributeError`, that is a bug. It should fail loudly, not quietly report a zero total.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and their tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

A compact comparison table often helps. An invented example for Fernwood Garden Club, which wants members to stop missing volunteer shifts:

| Option | Fits criteria? | Main cost | Main risk |
|---|---|---|---|
| Do nothing | Yes, but problem persists | None | Shifts keep going unfilled |
| Shared calendar plus weekly reminder email | Yes | An hour of setup | Reminders get ignored |
| Custom sign-up program with text alerts | Partly; adds a new dependency | Days of work, ongoing upkeep | Hard to remove once members rely on it |

Recommendation: the shared calendar with reminders, because it solves the main problem with existing tools and is easy to undo. Revisit a custom program only if missed shifts continue.

Keep the proposal direct. Expect the decision-maker to ask questions or iterate before choosing; they may pick a different option.

By default, give the proposal directly in your reply. Only move it into a separate shared document when the user asks for one, and then follow their usual documentation practice. Do not park proposals in loose local files the reader has to go find and open. If you do create a document, give it a clear, date-prefixed title, using one unambiguous date format consistently (spelling out the month, as in `9 Oct 2026: Solve - topic`, avoids day/month confusion).

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration and rollback strategy, test strategy, deployment steps, and follow-up ownership. Put the plan somewhere reviewers can easily read, comment on, and edit.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, security, and failure behavior.

Do not claim success based only on implementation. State what was tested, the results, and what remains unverified. Commit, publish, or deploy changes according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.

## Common failure modes

- Building exactly what was asked when the request does not solve the real problem.
- Skipping criteria, so the first plausible idea wins.
- Offering only technical options, or only variations of one design.
- Leaving out "do nothing" when the priority is weak.
- Presenting several options without a recommendation.
- Slipping a hard-to-reverse commitment into implementation without an explicit decision.
- Writing long proposals that bury the recommendation.
- Sending the reader off to a separate file or document they did not ask for instead of answering in the reply.
- Reporting "done" without saying what was verified.

## Optional extras

- **Shared documents.** If the user asks for the proposal as a shared document, create it in their chosen documentation system with the date-prefixed title, following their usual conventions for location and sharing, and end your reply with a link. For larger implementation plans, editable shared documents are usually easier for reviewers than plans kept inside an assistant's private planning mode. Plans for pure code changes tied to a single branch can stay with the code if the user prefers.
- **Repository conventions.** If the user's practice is to commit and push after completing work, follow it, including any commit message prefixes (for example, feature, fix, or maintenance tags). Otherwise ask before publishing.
- **Wide idea generation.** For problems that need many candidates, run a separate brainstorm aiming for a large list (for example, ten or more ideas, adjustable) before narrowing to the few worth comparing.
- **Decision records.** For hard-to-reverse choices, keep a short record of the options considered, the choice, the rationale, and what would cause you to revisit it.


---
name: shape-and-draft
description: Shapes a high-stakes document through evidence review and rounds of questions, then drafts and audits it. Use when writing a strategy doc, proposal, or decision memo that must land.
---

# Shape and draft a document

Develop an important document by shaping the thinking behind it before writing: gather the evidence, resolve the material choices with the person who has authority to make them, and draft only when the remaining uncertainty will not materially change the result.

## Quick version

- Before any drafting, tell your assistant who will read the document and what they should understand, decide, or do afterward. Ask it to recommend a form (narrative, strategy, operating agreement, decision memo, scorecard, or hybrid) and explain the tradeoff.
- Paste in the relevant source material and ask for a short situation brief that separates what the sources establish from what the assistant only infers.
- Ask for questions in rounds of four to eight, numbered, one decision per question, with three or four lettered options and the recommended option first, so you can reply in shorthand like `1a, 2c, 3b`.
- After each round, have it show an updated ledger of what is confirmed, sourced, inferred, open, and corrected, then build the next round from the consequences of your answers. Do at least two rounds for consequential documents.
- Before drafting, have it check every major planned claim: did you confirm it, does a reliable source establish it, or is it only inferred? For persuasive documents, also ask for the strongest objection from the real audience and confirm the response.
- Then ask for the smallest document that does the job, in plain, complete sentences, and have it audit the draft against the ledger before handing it over.

## 1. Classify the request

Use this workflow for strategies, narratives, operating agreements, proposals, scorecards, decision memos, and hybrids when the argument, commitments, boundaries, operating model, or document form is not yet settled. Use a lighter process for simple edits, formatting work, or documents whose decisions and content are already clear.

A request may name a proposed document, a desired outcome, an audience, source material, or some combination. Treat any proposed document type as a hypothesis until its purpose is clear.

Use the **full shaping process** when the document is consequential and its argument, boundaries, commitments, or operating model are still materially unsettled. Also use it when the requester explicitly asks for deep thinking, many questions, multiple rounds, or close alignment before drafting.

A substantive round resolves a distinct layer of choices and uses the answers to decide the next layer. Restating the situation, asking for general approval, or repeating answered questions does not count as a round.

If you review private communications, internal records, or information about people, do so only for a legitimate purpose and with clear authorization. Use the minimum relevant sources and information, leave out unrelated or sensitive personal details, and keep the draft within the access boundary that fits its audience.

## 2. Work backwards from the outcome

Start with the change the document needs to produce. Establish:

- Who will read it.
- What they should understand, decide, approve, or do afterward.
- What is unclear, contested, blocked, or going wrong now.
- Whether the document mainly needs to explain, persuade, decide, coordinate, or govern.

Do not accept 'write a narrative' or 'make a strategy page' as the goal. Identify the job the document must do.

## 3. Choose the artifact

Recommend the form that best serves the goal:

- **Narrative:** Builds shared understanding of why something matters and what bet is being made.
- **Strategy:** Connects a diagnosis to choices, priorities, outcomes, and exclusions.
- **Operating agreement:** Defines ownership, interfaces, decision rights, handoffs, and cadence.
- **Decision memo:** Records a choice, the alternatives, the rationale, the risks, and a review point.
- **Scorecard:** Defines a role or team mission, its outcomes, and the role-relevant capabilities it needs.
- **Hybrid:** Combines forms when readers need both shared understanding and execution clarity.

Explain the tradeoff and recommend one form. If the choice of form is load-bearing, because it would change the argument, structure, or decisions required, ask the decision-maker to confirm it before going deeper.

## 4. Gather and classify the evidence

Read supplied material first. Follow any stated rules for source selection, authority, and citation. Scale the research to the stakes. For a consequential internal document, look at the authorized sources most likely to hold prior decisions, current definitions, relevant evidence, dissent, constraints, and ownership context.

Apply these rules:

- Respect any stated source-of-truth hierarchy.
- Treat discussion notes, recollections, and generated summaries as weaker than current, authoritative decision records.
- Resolve contradictions where the evidence allows, and surface the ones that remain.
- Do not ask the decision-maker for facts that available sources can answer.
- Do not modify any source document unless explicitly asked.

Keep a strict boundary between evidence and alignment:

- Sources can establish what happened, what people said, and what an authoritative record currently states.
- Sources do not establish what the decision-maker now believes, wants to promise, or is willing to exclude, unless they contain an explicit, current decision from that person.
- A synthesis, a repeated theme, or a plausible implication is **inferred**, not settled.
- Ask for confirmation of any inference that would become a central claim, commitment, boundary, or recommendation.

Before the first interview round, give a short situation brief covering:

- What the sources establish.
- What the decision-maker has already confirmed.
- What you infer but have not confirmed.
- The central tension or missing logic.
- The artifact you recommend.
- The important uncertainties that only the decision-maker can resolve.

## 5. Interview in answer-dependent rounds

For a full shaping process, complete at least two substantive, answer-dependent rounds before drafting. Count relevant rounds that already happened in the current conversation, and do not repeat them. Do not draft right after the first answer round just because one apparent core tension seems resolved. The second round should test the implications, boundaries, counterarguments, or execution details the first round revealed.

Ask four to eight focused questions per round. If fewer than four material questions genuinely remain, ask all of them and say this is a narrow final check. Do not pad a round with ritual questions.

Each numbered question should normally contain one decision. Do not bundle independent choices, such as ownership, coordination, handoffs, and success measures, into one yes-or-no question. A broad answer to a bundle creates false alignment.

**Deliver each round once, on one answer surface.** Put the situation brief or updated synthesis and the questions in the same message, at the end of your turn, so the respondent can read them together and reply in shorthand.

Format questions for fast, unambiguous replies:

1. Number every question (`1.`, `2.`, `3.`). Continue numbering across rounds and keep each number tied to the same question, so compact replies stay clear.
2. For bounded choices, default to three or four mutually exclusive, decision-relevant options labeled `a.`, `b.`, `c.`, `d.`. Binary questions hide useful middle positions, so use two options only when the decision truly has two states. Do not invent fake alternatives.
3. Make the recommended option `a.` unless the conversation makes another order clearer. This allows replies like `1a, 2c, 3b`.
4. Render the block as a compact, single-spaced list, with each question and option on its own line and no blank lines inside the block.

Example:

1. Which direction should the document recommend?
   a. Focus first on the highest-impact problem; this narrows scope but makes accountability clear.
   b. A more cautious, phased direction.
   c. A more ambitious direction that addresses all related problems.
   d. Leave this deliberately open for now.
2. Who should own it?
   a. The program lead.
   b. The functional lead.
   c. Shared ownership with one named decision-maker.

Each round should:

1. Start with the updated model and what changed because of earlier answers.
2. Focus on one layer of uncertainty.
3. Offer concrete options where the choice can be bounded, recommended option first, with a brief tradeoff.
4. Leave room to reject the framing or give a different answer.
5. Notice contradictions and ask the smallest question that resolves them.
6. Separate what the sources suggest from what you are asking the decision-maker to decide.
7. Include at least one pressure test of the emerging position when the document is persuasive or strategically consequential.

A typical progression of layers:

1. **Purpose:** audience, desired effect, artifact type.
2. **Strategy:** diagnosis, central bet, priority, scope, exclusions.
3. **Operating model:** owners, interfaces, handoffs, decision rights.
4. **Definitions:** thresholds, edge cases, success measures, evidence standards.
5. **Expression:** tone, length, destination, and any deliberate open questions.

After every answer round, do all four steps before deciding whether to draft:

1. Match shorthand and free-text answers to their question numbers, keeping qualifications such as 'mostly c' or 'not sure'. Classify each answer as confirming, rejecting, softening, qualifying, or deferring the proposed position. Mark only genuinely unanswered or unclear material choices as open.
2. Trace downstream implications. A changed audience, softened commitment, new exception, or rejected framing usually creates another question.
3. Update the alignment ledger and show a concise summary of it.
4. Build the next round from the remaining material uncertainties and the consequences of the answers.

Adapt the content of the rounds to the task, but keep the answer-dependent loop. Continue while an open issue could materially change the draft. Stop interviewing once only low-impact uncertainty remains and the readiness gate is met. If the requester asks to skip further questions and draft now, briefly name the material consequence and follow the instruction.

## 6. Maintain an alignment ledger

Keep a compact working record throughout the conversation:

| Category | Meaning | Current entries |
| --- | --- | --- |
| Confirmed | Choices the decision-maker explicitly made, including earlier ones in the conversation | [entry] |
| Source facts | Claims established by current, authoritative evidence, but not choices | [entry] |
| Inferred | Your interpretation, clearly marked as not yet a decision | [entry] |
| Open | Questions that could materially change the document | [entry] |
| Corrected | Assumptions or source claims the decision-maker has rejected | [entry] |

Update the ledger after every answer round, before asking more questions. Never reintroduce a corrected assumption. When two confirmed statements conflict, surface the conflict and resolve it instead of smoothing it over. Never promote an inference to confirmed just because several sources support it.

For a full shaping process, do not keep the ledger implicit. Show a concise version before each later round so the decision-maker can catch mistaken assumptions. Every major claim planned for the draft must be confirmed, a source fact, or deliberately presented as a proposal or open question.

## 7. Apply the readiness gate

Draft only when no unresolved issue is likely to change the document's substance. Before drafting, explicitly run the gate and give a short pre-draft synthesis: the intended job, the audience, the central position, the important boundaries, and any deliberate open questions.

For each major claim in the planned outline, ask: **Was this confirmed by the decision-maker, established as fact by an authoritative source, or am I only inferring it?** If a material claim is only inferred, ask another question instead of drafting.

Check that each relevant category is confirmed, evidence-based, deliberately left open, or genuinely not applicable:

- Goal and audience.
- Artifact type.
- Central argument or bet.
- Scope and exclusions.
- Definitions and thresholds.
- Ownership and decision rights.
- Interfaces and handoffs.
- Success measures and evidence standard.
- Tone, length, and destination.

For persuasive documents, also do a skeptical-reader pass:

- What is the strongest objection from the actual audience?
- Which premise, commitment, evidence claim, or safeguard would they dispute?
- Has the decision-maker confirmed the response the draft will give?

Resolving one central tension is not enough if the draft still depends on unconfirmed positions about the theory of change, scope, relationship model, commitments, evidence, or exclusions.

Close alignment is not a literal probability. It means the remaining uncertainty is low impact, or the document openly presents it as unresolved. If the requester asks for the draft before the gate is met, name the one or two consequences of the uncertainty and follow the instruction.

## 8. Draft in the requested voice

Apply any voice profile, style guide, or delivery rules the user has supplied. If none exist, write in clear, direct language that suits the audience and sounds like the document's owner rather than an outside consultant.

Write the smallest document that can do the job. Prefer clear claims, concrete decisions, and explicit ownership over polished abstractions. Distinguish current decisions from proposals and future review points.

Keep the structure readable. Do not let a section become a long, flat inventory. For action or onboarding documents, set a cap on top-level bullets per section (seven is a sensible adjustable default, with fewer in the main outcome section). If more points seem necessary, cut them, combine them under a clear lead phrase, or move detail to a linked reference.

Make the draft as simple as the substance allows. The hard thinking should produce a document that is easy to read, not one that displays how complex the thinking was.

- Prefer short, common words over formal or fancy ones.
- Write complete, natural sentences. Keep one clear line of thought in each sentence, but do not split connected ideas into choppy fragments.
- Let sentence length follow the thought. A longer sentence is fine when it makes a connected argument easier to follow.
- State the point first. Cut warm-up text, repeated context, process narration, and throat-clearing.
- Turn abstract ideas into concrete claims, actions, examples, owners, dates, or tests.
- Explain a complex idea as a clear sequence of full sentences rather than hiding it behind jargon.
- Cut qualifiers and side points that do not change a decision or action.
- Use focused paragraphs. Use bullets only for real lists, and write each bullet as a full sentence unless it is a compact label.
- Prefer the more concise version when it keeps the meaning. Concise means removing unneeded ideas and words, not shortening every sentence.

Do not flatten the substance. Keep a hard idea when it matters, and explain it in the simplest language possible.

Honor the requested destination. If text was requested in the conversation, give it there and do not edit any source document.

## 9. Audit before delivery

Compare the draft with the alignment ledger and the source hierarchy:

- Does it solve the agreed problem in the agreed form?
- Does every material choice reflect the decision-maker's answers?
- Are corrected assumptions gone?
- Are responsibilities, boundaries, and handoffs unambiguous?
- Are uncertain claims marked as such?
- Are factual claims and links supported by sources?
- Is anything presented as settled that was only inferred?
- Does it match the requested voice and audience?
- Can each sentence be understood on first read?
- Are prose and bullets written as full, natural sentences rather than clipped fragments?
- Can any fancy word, abstract phrase, or repeated point be simplified or cut? Keep a long sentence when it carries one connected thought clearly.

Fix any mismatch before delivering. Put the deliverable last, with no trailing summary or offer that gets in the way of copying it.

## Failure modes

- Drafting early because producing text feels useful.
- Treating the proposed artifact as fixed.
- Asking questions before researching facts the sources can answer.
- Mistaking extensive research for alignment with the decision-maker.
- Treating a plausible synthesis as a decision.
- Sending a generic questionnaire disconnected from the evidence.
- Failing to update the model after each answer.
- Drafting after one round because a single core tension seems resolved.
- Bundling several independent decisions into one question.
- Skipping a consequence round after a claim is softened or qualified.
- Repeating a question that has already been answered.
- Running the same round on two answer surfaces, or treating a stale queue as missing answers.
- Hiding a contradiction behind vague language.
- Continuing the interview after only low-impact uncertainty remains.
- Producing an inspiring narrative that leaves ownership or decisions unclear.
- Mistaking concise writing for choppy writing through fragments, noun-only bullets, or forcing every sentence to be short.

## Optional extras

**Question forms and tools.** If your assistant can show questions through a separate form or question tool, use only one surface per round. Do not mirror the chat block into a form, because two answer surfaces can produce conflicting or stale answers. If a form is required, show the questions there once with the context needed to answer them, and respect that tool's limits. If a reply arrives in chat while the form still looks pending, treat the chat reply as the answer. Progress depends on what has actually been answered, not on what an interface shows as pending.

**Writing into a document system.** If the draft must be created or edited in your chosen document system, use the appropriate tool and verify the result. Format conversions, such as Markdown into a word processor, often cause two problems: a stray empty paragraph between a list and the next heading, or a heading that inherits the list's bullet or numbering. Make sure each heading after a list is truly separate from it and that every intended bullet renders as a bullet, not a number. Inspect the rendered output or an export, not just the underlying structure, and fix uneven indentation across sections, orphaned bullets, and awkward page breaks rather than accepting output that is structurally valid but visually poor.


---
name: gather-context
description: Searches the right sources at a depth fitting the stakes and builds one brief where every claim links to evidence. Use when asked to gather context on X or get someone up to speed.
---

# Gather context

Build a well-sourced context brief on a person, organization, project, topic, or decision by checking the sources that plausibly hold relevant information. The result is one organized brief in which every sourced claim links to its evidence.

## Quick version

- Decide how much effort the request deserves: a quick reminder, a standard brief, or a deep dive before a high-stakes decision. Say which one you picked in one line.
- If the subject is truly ambiguous, such as a bare name or a one-word topic, ask one short clarifying question. Otherwise, proceed.
- Without connected tools, ask the user to paste what matters: recent emails, chat threads, documents, links, and especially notes from any recent meeting with the subject, which are often the richest source.
- Organize findings by theme, not by source, and lead with what matters most for the user's next action. Resolve contradictions instead of listing both sides blindly.
- Tie every claim to where it came from (the pasted email, the meeting notes, a link the user gave). Never invent a link or a fact.
- End with a short "Open questions / gaps" list: what no material answered and where the answer probably lives.

## 1. When to use this

Use this workflow when the user wants context before they act: before writing, deciding, meeting, pitching, or hiring, or simply to get up to speed. Typical requests include "gather context on X", "what do we have on X", "pull everything about X", "what's the latest with X", and "background on X before my call".

If the user has a separate workflow for structured meeting preparation and that is what they want, use it instead. This workflow is for raw context assembly. If you are unsure which they want, ask.

Because this workflow can read private messages and records about other people, use them only for a legitimate purpose the user is clearly authorized to pursue, and only the minimum relevant sources and information. Leave out unrelated or sensitive personal details, and summarize what others said in personal chats in your own words rather than quoting or saving their messages. Keep the finished brief somewhere whose access matches the sensitivity of the sources and the intended audience.

## 2. Right-size the effort

This is the most important rule. Match the depth of the search to what the user actually needs. "Remind me where we are with X" needs a quick look at two or three obvious sources and a short answer. A deep dive before a high-stakes decision needs a broad search with verification. Most requests fall in between. Decide how much effort is warranted and do that much. Do not reach for maximum effort by reflex.

Two failure modes are equally bad:

- **Over-gathering:** querying every connected system, starting many parallel helpers, and writing an essay for a quick question.
- **Under-gathering:** checking one source, finding a few results, and stopping when the request clearly needed more. The key fact is often in a chat thread or meeting record the user has forgotten.

For each source, ask: *for this specific request, would a sensible researcher think it is worth checking here?* Relevance and effort level together set the breadth. A topic question does not need recruiting records. A quick status check does not need every source, even if each might hold a small detail. Skipping an irrelevant source is good judgment, not laziness.

## 3. Scope the gather

### Pick an effort level

| Tier | When | How to search | Output |
|---|---|---|---|
| Quick | Status check, "remind me" | One to three obvious sources, one pass each | A few lines |
| Standard | The common case | A handful of relevant sources, a couple of queries each; parallel helpers only if they truly save time | A tight brief |
| Deep | High-stakes preparation, such as a major decision, big pitch, or key hire | Broad search, parallel helpers, several queries per source, verification of key claims | The full brief structure |

If unsure, choose the lighter tier and offer to go deeper. Escalating is cheap; over-searching is expensive. State the tier in one line so the user can redirect, for example: "Quick look across email, chat, and the team wiki. Say the word if you want the full sweep."

### Classify the subject

The subject type tells you which sources matter most.

| Subject | Usually most relevant |
|---|---|
| Person (partner, funder, contact, candidate) | Email, team chat, notes, calendar and meeting records, public professional profile; recruiting records only for hiring matters |
| Organization | Public web first; then email, chat, and notes for any existing relationship; CRM or pipeline records if they are a partner or prospect |
| Project or initiative | Notes and wiki, chat, shared documents, code repositories, operational databases, product analytics if there are metrics |
| Topic or question | Several angled web searches, plus internal documents and chat for earlier thinking |
| Decision | All of the above, organized around the options and the evidence for and against each |

For hiring matters, focus on role-relevant capabilities, alignment with the role's requirements, and evidence that actually reflects relevant performance.

### Clarify only when necessary

If the subject is truly ambiguous, ask **one** short clarifying question before searching. A wrong-target search wastes a lot of effort. If the subject is clear, go ahead. The default is to proceed, not to ask.

### Named sources are a floor, not a ceiling

Sources the user names are mandatory, but they are not necessarily the full list. If another source clearly holds decision-relevant context, check it too.

The most common case is a recent meeting. When results show, or the request implies, a recent meeting with the subject, read its notes or transcript. Signals include a calendar invite or a "great to meet you this morning" message. The meeting record is often the richest single source, and a brief without it misses what was actually said.

### Set the time window

Use the window the user gives. If none, pick an adjustable default, such as the last several months, and extend it for older relationships or projects. State the window in the brief.

## 4. Search the relevant sources

- **Quick or standard:** search directly in the main conversation so you see results as they arrive.
- **Deep, or many sources:** run read-only searches in parallel, one helper per source or cluster. Each returns a short digest with links, not raw dumps. Give helpers the same scope and handling rules you are following.

Depth within a source also follows the tier. For a deep search, query several ways: by name, organization, project keyword, and related people, and do not conclude "nothing there" until you have used the search capabilities available. For a quick look, one or two well-chosen queries on the obvious sources is correct, not a failure.

### Source-handling principles

These apply whatever tools the user has. Apply them fully on deep searches and lightly on quick ones.

1. **Search direct and indirect.** Look for direct contact with the subject, and in deeper passes, for places where others discuss the subject.
2. **Prefer precise search.** If a default search returns noisy or loosely related results, switch to exact or keyword search.
3. **Read the whole item.** Documents and records can hide content in tabs, sections, attachments, or threads that a simple read skips. Open what matters in full and note where each finding came from.
4. **Trust authoritative records.** Go first to the records the user's organization treats as the source of truth for that kind of subject, in their current home if they have moved. Treat temporary, sandbox, or low-quality data as weak until confirmed.
5. **Check freshness and attribution.** Web profiles, news, and stored notes reflect what was true when written; cross-check against dated, current sources. Speaker labels and authorship can be imprecise, so do not attribute a statement without reasonable confidence.
6. **Use conditional sources only when they fit.** Recruiting records for hiring, analytics for usage questions, code history for engineering subjects, and the user's personal task and planning records only for their own work when they choose to include it. In personal systems, request only the fields you need, such as tasks, priorities, and plans, and leave private journal entries and health data out even when they sit alongside.
7. **Cite with real links.** Link to threads, pages, messages, and documents, not raw internal IDs. Use only URLs you have verified or the user supplied; otherwise leave the link out and flag it.

### Gaps and unavailable sources

**Do not silently substitute sources.** If a source you judged relevant returns nothing or is unavailable, say so in the brief. Do not cover the gap with an adjacent source. A source you deliberately skipped as irrelevant is not a gap and need not be reported, but never imply you checked it.

## 5. Synthesize into a context brief

Combine findings into one brief organized by theme, not by tool. Lead with what matters most for the user's next action. Resolve contradictions rather than listing both blindly, for example: "A news profile says they work at Organization A; their dated professional profile says they left in March. The profile is more recent and more likely correct."

**Every sourced claim gets a clickable link** to its primary source. A quote without a link is not finished. The user must be able to click straight through to check.

### Output template

Adapt the headings to the subject, but keep this spine:

```markdown
## [Subject]: context brief
*Searched: [sources]. Window: [dates]. Effort: [quick/standard/deep].*

## TL;DR
Three to five bullets with the most decision-relevant facts.

## What we know
Who or what this is, current state, history. By theme, with inline evidence links.

## Relationship / timeline
(For people and organizations) How the user's organization connects to them; chronology of contact.

## Open questions / gaps
What no source answered, and which source would likely hold it.
Any relevant source that was unavailable or empty.

## Sources
Key links, grouped, so the user can dig in.
```

Match length to depth and keep prose blocks short. This is a document to scan and act on, not an essay.

## 6. Deliver the brief

- **Short brief (fits on screen):** give it directly in the reply.
- **Long or reference brief:** save it where the user keeps generated documents, following their naming convention. If none exists, use the date plus a concise, specific, human-readable headline, such as "[YYYY-MM-DD]: Options for next year's partner program", not a filename-style slug or a type suffix. Reply with a compact summary of key findings and the link.

Make the brief (or summary plus link) the final part of the reply, with no closing meta-summary after it. Put any follow-up offer, such as "Want me to draft the outreach email?", before the brief so the deliverable stays easy to copy.

## 7. Worked example

A program lead at the fictional Brightwater Learning Collective says: "Background on the Harbor Lane Community Fund before my call tomorrow."

The assistant classifies the subject as an organization with an existing relationship and picks Standard: "Standard look across email, team chat, notes, meeting records, and the web. Say the word if you want the full sweep." Email shows a thank-you message from yesterday, so it also opens that meeting's notes even though the user did not mention them. The brief opens like this:

```markdown
## Harbor Lane Community Fund: context brief
*Searched: email, team chat, notes, meeting records, web. Window: last 9 months. Effort: standard.*

## TL;DR
- Program officer asked for a revised budget by month end ([email thread])
- Yesterday's call: they favor multi-year grants over one-off awards ([meeting notes])
- Their public site lists a new grants director; our notes still name the old one ([fund website], [notes page])

## Open questions / gaps
- Current decision timeline: not in any source; likely in the program officer's next email
- Shared budget folder was unavailable during the search
```

## 8. Readiness checklist

| Check | Pass condition |
|---|---|
| Effort | Tier matches the stakes and is stated in one line |
| Coverage | Named sources searched; obviously decision-relevant sources, especially recent meeting records, added |
| Evidence | Every sourced claim has a verified, clickable link; no invented URLs |
| Conflicts | Contradictions resolved or clearly flagged |
| Gaps | Unavailable or empty relevant sources reported; skipped sources not implied as checked |
| Delivery | Output in the right place; brief is the final block |

## 9. Common failure modes

| Failure | Fix |
|---|---|
| Searching every system for a quick question | Choose the lighter tier and offer to go deeper |
| A one-source answer to a high-stakes request | Classify the subject and cover its source cluster |
| Missing what was said in a recent meeting | Read the meeting record when one appears |
| Trusting stale profiles, notes, or memory | Cross-check against dated, current sources |
| Reading only part of a document or record | Open hidden sections, tabs, and threads |
| Covering a gap with a nearby source | Report the gap explicitly |

## Optional extras

### Structured databases

If the user keeps a map of their databases (which tables are canonical, what fields mean, known quirks), read it before crawling so you go straight to the right place. Route by subject: each kind of record, such as applications, payments, or contacts, usually has one canonical home, and a consolidated table beats older scattered copies. Personal and organizational data may live in separate stores with separate access, so use the one that fits the question. If the map is out of date, suggest updating it. When a field seems to show when something happened, confirm it is a real value and not an automatic default; a record's creation date is often more reliable.

### Repairing an unavailable connection

If a connected source should be reachable but is not, treat it as a connection problem. Try every safe diagnosis and repair you can first, such as checking the configuration, confirming the source's name, or restarting a service you are allowed to manage. Ask the user only for steps that need them, such as re-authenticating or restarting the application. Report the exact failure, what you tried, and the one remaining action.

### Editing an existing formatted document

If you insert the brief into an existing formatted document, new text can inherit the style of the paragraph it lands in. Insert into a plain body paragraph or replace a complete section whose structure you have read, never at the start of a heading, list item, or table cell. Afterward, re-read the affected range at the structural level and confirm body text and bullets carry normal styles and only intended headings carry heading styles. A plain-text read does not confirm formatting, so do not report the edit complete until this check passes.


---
name: learning-tutor
description: Teaches a paper, article, or topic through Socratic questions and retrieval practice instead of passive summary. Use when someone says teach me this, help me understand it, or quiz me on it.
---

# Learn with a tutor

Help a learner understand, retain, and use a paper, article, post, lesson, or topic through an active dialogue that favors retrieval, explanation, and application over passive review. The learner should do most of the thinking; the tutor should guide, diagnose, and increase challenge without turning the exchange into a test.

## Quick version

- Share or name the material and tell your assistant: “Act as a Socratic tutor. Do not summarize. First ask what I already know, then have me explain the main claim from memory.”
- Ask it to focus on two or three of the most important ideas and probe each one for mechanism, evidence, a self-generated example, and the strongest objection.
- Ask for one or two questions per turn, no yes-or-no questions, and specific feedback instead of generic praise.
- When you get something wrong, have it ask a follow-up that exposes the gap, and explain directly only after one or two genuine attempts.
- Ask for short checkpoints on what you have shown you understand and what is still shaky, and end with “What would I actually do differently now?” plus one question to revisit later.

## 1. Core learning principles

- **Retrieve before reviewing.** Do not give an unrequested summary. Ask the learner to reconstruct ideas in their own words.
- **Require explanation.** Ask why, how, under what conditions, and based on what evidence an idea holds.
- **Use learner-generated connections.** Have the learner create examples, analogies, predictions, and applications before supplying them.
- **Create productive difficulty.** Make the task demanding enough to require effort, but calibrated enough that the learner can make a meaningful attempt.
- **Practice transfer.** Ask how an idea applies in an unfamiliar setting, relates to existing knowledge, or changes a decision.
- **Reveal gaps through inquiry.** When reasoning is incomplete or inconsistent, use focused questions to expose the tension. Explain directly only after the learner has had one or two fair attempts.

## 2. Readiness and scope

Start by establishing both the learner’s starting point and their goal. Ask one or two open questions, such as:

- “What do you already believe or know about this topic, and why?”
- “What are you trying to be able to explain, evaluate, or do by the end?”
- “Have you read the material already? If so, what do you remember as most important?”

If the learner has not encountered the source, ask for an initial prediction or working model. Then direct them to inspect a relevant portion before beginning retrieval practice. Do not replace their first engagement with a full explanation.

## 3. Elicit the central idea

Ask the learner to state the main claim, finding, or problem in their own words. Do not invite quotation as a substitute for understanding.

Useful prompts:

- “What is the central claim?”
- “Why should someone believe that claim?”
- “What problem is this idea trying to solve?”
- “How would you explain it to a thoughtful friend in 30 seconds?”

## 4. Choose a few high-value ideas

Select two or three ideas that are central, difficult, consequential, or likely to be misunderstood. Do not attempt to cover everything superficially.

For each idea, use this cycle:

1. Ask the learner to reconstruct the idea.
2. Probe its mechanism, assumptions, and evidence.
3. Ask for a self-generated example, comparison, or application.
4. Test it with an objection, alternative explanation, or boundary case.
5. Adjust the next question based on the learner’s response.

Keep each turn short. Usually ask only one or two questions at a time.

## 5. Question toolkit

Choose questions that require reasoning rather than recognition.

- “What has to be true for this conclusion to follow?”
- “What would have to be true for this conclusion to be wrong?”
- “What is the mechanism, step by step?”
- “What evidence would distinguish this explanation from another one?”
- “Can you construct a concrete example from a familiar setting?”
- “Where might this fail or not apply?”
- “What is the strongest objection to this argument?”
- “How does this connect to another idea you know?”
- “What surprised you, and what did you expect instead?”
- “How would the conclusion change if one assumption changed?”

Avoid yes-or-no questions unless they immediately require an explanation or defense.

## 6. Response rules

Be warm, rigorous, and specific. Generic praise is not useful. When an answer is strong, identify what makes it strong (for example, a clear causal mechanism, a relevant counterexample, or a distinction between correlation and causation), then raise the challenge.

When an answer is incomplete or incorrect:

1. Do not immediately give the correction.
2. Ask a focused follow-up that exposes the missing assumption, contradiction, or evidence.
3. Allow one or two genuine attempts.
4. If the learner remains stuck, provide a concise clarification.
5. Ask them to restate the corrected idea or apply it to a new case.

If the learner says, “I don’t know,” invite an informed guess first: “Based on what you do know, what seems most plausible, and why?” Give a hint after an attempt, or sooner when the learner lacks necessary foundations.

If jargon appears, ask the learner to define it before defining it yourself. Clarify only as needed for accurate reasoning.

## 7. Calibration and pacing

Increase difficulty when answers are easy or fluent. Ask for a counterexample, competing explanation, prediction, analogy, or application in a different domain.

Reduce difficulty when the learner is lost. Narrow the question, isolate one assumption, use a simpler case, or present two plausible explanations and ask them to defend a choice.

| Learner signal | Tutor response |
|---|---|
| Learner recalls a conclusion but cannot explain it | Ask for the mechanism or evidence that supports it. |
| Learner gives a confident but inconsistent answer | Ask a question that compares the answer with a relevant case or assumption. |
| Learner is overloaded or losing energy | Consolidate the strongest ideas and avoid introducing new major concepts. |

Match the learner’s energy while maintaining intellectual standards. A demanding dialogue should feel collaborative, not punitive.

## 8. Progress checks and audit

Periodically provide a brief, evidence-based checkpoint. State:

- What the learner has demonstrated they understand.
- What remains uncertain, incomplete, or confused.
- What question or concept would be most valuable to revisit next.

Do not treat recognition, memorized wording, or agreement as mastery. Look for accurate recall, explanation, reasoning, and transfer to a new case.

Before moving on, check whether the learner can:

- State the idea without quoting the source.
- Explain why it should be believed.
- Identify at least one assumption, limitation, or objection.
- Apply it to a concrete situation.

## 9. Closing gate

Before ending, ask the learner to turn understanding into action:

> “Given what you have learned, what would you actually do differently? What decision, prediction, or belief should this change?”

Then ask for a final concise explanation, a self-generated example, or a future retrieval prompt. End by naming the most useful concept or question to revisit later.

## 10. Guardrails

- Do not summarize unless the learner explicitly asks; even then, invite their own summary first.
- Do not lecture when a well-chosen question can prompt retrieval or inference.
- Do not make questions easy merely to be encouraging.
- Do not cover an entire source at shallow depth when a few important ideas can be understood deeply.
- Do not use a fixed question list as a substitute for responding to the learner’s actual reasoning.
- Keep the interaction primarily question-driven, with brief explanations used to unblock learning or correct persistent misunderstandings.

## Optional extras

**Short sample exchange (invented).** A learner is studying a fictional article from the Bramblewood Institute claiming that spaced practice beats cramming.

> Tutor: In your own words, what is the article’s main claim, and why should anyone believe it?
>
> Learner: Spreading study sessions out helps you remember more.
>
> Tutor: That is the conclusion. What mechanism would make spacing work better than the same hours in one block?
>
> Learner: Maybe because you forget a bit, and recalling it again is harder?
>
> Tutor: Good: you linked spacing to effortful recall rather than just time. Now, where might this fail? Think of a situation where cramming could be the better choice.

Notice the pattern: no summary, a push from conclusion to mechanism, specific feedback, then a boundary case.

**If your assistant can save notes or remember across sessions.** At the end of a session, have it record the learner’s goal, the ideas covered, the gaps named at the last checkpoint, and two or three retrieval prompts. Open the next session by asking those prompts before introducing anything new. The review interval is the learner’s choice; a few days for the first review is a reasonable adjustable default.


---
name: write-in-my-voice
description: Drafts or revises email in your own voice from real samples, with facts and commitments checked. Use when you say "write this email," "reply to this thread," or "polish my draft."
---

# Write in my voice

Use this workflow when you want an AI assistant to write, reply to, revise, or polish an email. The goal is a concise, copy-ready message that sounds like you while staying accurate, appropriate, and within your authority.

## Quick version

- Paste three to five emails you actually sent recently, plus any style rules (greeting, sign-off, words you avoid), and ask the assistant to summarize your voice before drafting.
- Give a short brief: who the recipient is, what you want the email to achieve, and any facts, dates, or links that must appear.
- Ask for the smallest complete message: purpose or answer in the first sentence, then only the context and next step the recipient needs.
- Tell the assistant not to invent availability, prices, decisions, promises, or feelings, and to ask one question if a missing fact matters.
- Have it check the draft against your voice and your known dislikes, then return only the email, ready to copy.
- Review and send it yourself.

## 1. Load the voice profile

Before drafting, read the user's current writing profile in full, if one is available. A profile may include examples of sent emails, a style guide, approved reusable wording, and a fact bank.

Build or confirm these settings:

| Voice element | What to identify |
|---|---|
| Greeting and sign-off | The user's usual opening, closing, and name format. |
| Tone | Their normal balance of casualness, warmth, directness, and formality. |
| Structure | Typical sentence length, paragraph length, use of bullets, and first-sentence pattern. |
| Language | Preferred contractions, recurring phrases, punctuation habits, and useful colloquialisms. |
| Avoidances | Words, filler, emojis, formatting, or tones the user does not use. |
| Approved material | Current facts, links, scheduling options, boilerplate, and standard replies the user has authorized. |

Use recent, genuinely sent messages as stronger evidence than older examples. If examples conflict, use the most recent consistent pattern or ask the user which preference is current.

A short profile might look like this (invented example):

> Greeting: "Hi [first name]," never last names. Sign-off: "Thanks, Sam." Length: usually two to four sentences. Tone: friendly, direct, contractions welcome. Avoid: emojis, "I hope this finds you well," long apologies, heavy dash use. Fact bank: booking link for intro calls, standard reply for speaking requests.

Do not access private messages, records, or mailboxes unless the user has a legitimate purpose and has clearly authorized access. Read only the minimum relevant messages, omit unrelated or sensitive personal details from the draft and response, and keep the output within the conversation or system the user intended.

## 2. Establish the email brief

Identify the minimum information needed to write safely:

1. Who is the recipient, and what is their relationship to the user?
2. What result should the email produce?
3. Is this a new message, a reply, a follow-up, or a revision?
4. What facts, dates, names, links, attachments, decisions, or commitments must appear?
5. What tone is appropriate: routine, warm, firm, sensitive, urgent, or formal?
6. Is there a deadline, approval boundary, or issue that needs careful wording?

If a missing fact would change the message or create a commitment, ask one focused question. Do not invent availability, decisions, prices, timelines, recipient context, opinions, emotional reactions, or promises.

## 3. Adapt voice to the situation

Keep the user recognizable, but do not treat voice as a rigid template.

- For familiar contacts, follow the user's ordinary level of brevity and informality.
- For new, external, senior, or sensitive recipients, keep the user's voice while making context and requests clearer.
- For corrections, refusals, conflict, or delays, state the relevant facts and next step plainly. Avoid defensiveness, hollow praise, and excessive apology.
- For requests, make the requested action, responsible party, and timing easy to identify.
- Use an approved reusable response, link, or fact when it fits the current context, rather than inventing one. Never reuse material that is stale, misleading, or unauthorized.

## 4. Draft the smallest complete message

Use the user's established greeting and sign-off when appropriate. If no evidence exists, use a broadly useful default: warm-professional, direct, concise, and conventional.

A reliable structure is:

1. Greeting, if useful.
2. The purpose, answer, or decision in the first sentence.
3. Essential context, request, or next step.
4. Closing and sign-off, if appropriate.

Prefer active verbs, concrete language, short sentences, and short paragraphs. Use bullets only when they make actions, choices, or logistics easier to scan. If the user dislikes emojis, convert them to plain punctuation or remove them.

Remove material that does not help the recipient act or understand:

- Generic openings or filler.
- Process explanations about drafting or internal work.
- Repeated thanks, praise, or apologies.
- Hedges that weaken a clear statement.
- Unnecessary context and unsupported claims.

Invented example, using the profile above. Brief: a partner at Larkfield Design asked for an intro call; Sam is happy to talk.

> Hi Priya,
>
> Happy to chat! Grab any open slot here: [booking link from fact bank].
>
> Thanks, Sam

## 5. Audit before delivery

Review the draft line by line:

- Does it plausibly sound like the user?
- Do the greeting, sign-off, punctuation, and rhythm match the available evidence?
- Is the level of warmth and formality right for this recipient and situation?
- Are all names, dates, links, attachments, references, and thread details accurate?
- Did the draft add any commitment, factual claim, decision, or emotion not supplied by the user?
- Is the requested action or decision unmistakable?
- Can any sentence be removed without reducing usefulness?
- Does the draft avoid the user's known style anti-patterns?

If no voice evidence exists, state the assumption briefly only when helpful, then provide the draft. Invite the user to share a few representative sent emails or preferences for future work.

## 6. Deliver the draft

By default, provide only the copy-ready email in chat. Do not add explanation after it unless the user asks for options, rationale, or edits.

Only create a draft inside an email system when the user explicitly asks for it (see Optional extras). The user remains responsible for reviewing and sending the message unless they explicitly authorize a separate sending action and the system's permissions and policies allow it.

## Optional extras

### Creating a reviewable draft in an email system

For assistants with connected tools, when the user explicitly asks for a draft in their email system:

1. Confirm authorization to use that system and the intended account or workspace when necessary.
2. Follow the user's applicable email-system policies, including which method is approved. Some setups allow drafting only through the regular web interface (for example, with a browser-control capability) and block direct programmatic draft or send tools. Never work around a blocked method.
3. For a reply, open the original conversation, choose Reply or Reply all as appropriate, type the body, and keep the existing subject unchanged so the draft stays in the same thread.
4. Before finishing, read back the recipients and body to confirm they match what the user approved and that the draft sits in the intended conversation.
5. Leave the draft unsent.
6. Give the user a safe way to open the draft for review and final sending, such as a link to the conversation, without exposing unnecessary account or message data.

### Maintaining the profile

Keep the voice profile and fact bank in one place the user controls. When the user corrects a draft in a way that reflects a lasting preference, suggest adding it to the profile. Review approved facts and links periodically (an adjustable default is every few months) so stale details are not reused.


---
name: professional-posts
description: Drafts, revises, and audits professional social posts that lead with concrete, accurate value. Use when someone says "make this into a post," wants hook options, or needs to promote an article.
---

# Write a professional social post

Use this workflow to draft, revise, or critique a professional social post from notes, a rough draft, an article, a transcript, a research finding, an announcement, or a simple topic. The goal is a specific, honest post that makes the right reader stop, understand a useful point, and have a reason to respond, save, share, or act.

## Quick version

- Paste your source and say who the post is for, what it should achieve, and which platform it is for. Ask the assistant to find two to four possible angles, usually a buried specific rather than the headline, and pick one yourself.
- Ask for five to ten hooks, then a shortlist of three to five with a one-line note on what each does. Reject any hook that would still work if you swapped in an unrelated topic.
- Draft as hook, tension, payoff, and one focused close. Keep it short by default, for example under 300 words, with one- or two-sentence paragraphs.
- Put real value in the post itself. Never invent facts, figures, names, or quotes. Mark gaps instead.
- Run an editing pass that cuts corporate verbs, filler intensifiers, hedges, restating transitions, and engagement bait.
- When you give feedback, ask for targeted edits to the flagged lines, not a full rewrite.

## 1. Set up the brief

This workflow is platform-independent. Before drafting, confirm these choices when they are not already clear:

- **Platform and format:** text post, image caption, document or carousel caption, thread, article promotion, or announcement.
- **Audience:** for example, practitioners, founders, researchers, policy professionals, customers, prospective applicants, or a specialist community.
- **Purpose:** share an insight, explain a concept, announce a meaningful change, promote a longer piece, start a substantive discussion, or support a campaign.
- **Voice:** first-person or organizational voice; formal or conversational; preferred and forbidden words; length; and punctuation, emoji, hashtag, or formatting preferences.
- **Distribution:** whether there is an external link, where it goes on that platform, and whether visual material accompanies the post.
- **Evidence and permissions:** what supports the claims, and what names, quotes, outcomes, or personal details may be shared.
- **Delivery:** by default, return the draft directly in the reply. If the user asks for a separate document, follow their chosen location and naming convention (for example, date plus topic).

If the user provides approved posts, a writing guide, audience research, or brand guidance, treat these as the primary voice reference. Do not assume an individual writing style, a particular organization's practices, or access to private systems.

## 2. Identify the genre

Different genres need different evidence, structures, and privacy checks.

- **Career or participant case study:** a person's before-and-after story, often involving training, a program, or a new role. Use a case-study structure: starting point, turning point, concrete outcome, evidence, and lesson. If the user has a dedicated case-study process, use that instead of improvising one here.
- **Research or evidence post:** a claim based on a report, model, survey, experiment, or analysis. Prioritize methodology, scope, uncertainty, and a conclusion the author can defend.
- **Organizational or product announcement:** lead with the concrete change and reader relevance, not internal excitement. Use this genre only when the news is interesting in itself.
- **Article, report, or podcast promotion:** lead with the strongest insight, finding, or disagreement in the longer piece, not with "new article" or "new episode." For an episode featuring a guest, lead with the most striking detail of their story.
- **Carousel or document caption:** give one or two meaningful findings and explain what the visual material adds.
- **Framework or checklist post:** present a reusable model, explain its boundaries, and give enough detail for readers to apply it.

When working with private communications, records, or stories about identifiable people, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant information, omit unrelated sensitive details, and keep the output within the intended publication boundary.

If the genre is unclear, ask one routing question before drafting:

> Is this primarily an evidence post, a concrete announcement, a case study, a framework, or promotion for a longer piece?

## 3. Follow accuracy and trust rules

1. **Never invent facts.** Do not fabricate statistics, names, organizations, quotes, testimonials, titles, dates, roles, outcomes, or sources.
2. **Separate evidence from interpretation.** State what the source establishes, then make the inference or personal judgment clear.
3. **Keep meaningful uncertainty.** If evidence has large ranges, assumptions, weak data, or limited scope, say so in plain language.
4. **Use exact details only when supported.** Exact figures beat vague claims, but do not convert a rough estimate into false precision.
5. **Request missing evidence early.** Ask for a source, narrow the claim, qualify it, or remove it.
6. **Avoid manufactured urgency.** A concrete risk plus a realistic response is more credible than catastrophe language.
7. **Stay even-handed on contested topics.** Avoid partisan framing and cheap shots unless the user explicitly wants an advocacy post.
8. **Respect attribution and consent.** Quote, name, or credit people only when authorized and accurately represented. Credit collaborators, such as whoever designed the visuals, when appropriate.
9. **Do not overstate a promotion.** A longer piece, event, service, course, or product may be relevant, but it must not substitute for actual value in the post.

## 4. Audience and voice

Write for the reader most likely to act on the post, not for every possible reader. A post that a small, relevant group finds unmissable usually beats one that everyone finds mildly interesting. Specificity and concrete claims attract that group; smooth, broad language repels it.

Default voice unless the user specifies otherwise:

- Direct, clear, and conversational, with contractions.
- Short sentences and concrete nouns. A useful working range is roughly 10 to 20 words per sentence.
- Active voice and one principal claim per sentence.
- Takes a position rather than balancing "on one hand" against "on the other."
- Sober about problems and practical about responses.
- Confident only where evidence supports confidence.

| Failure mode | What it sounds like | Better approach |
|---|---|---|
| Corporate | "We are thrilled to announce an exciting initiative." | State what changed, who it affects, and why that matters. |
| Academic | Long, hedged sentences with unexplained technical terms. | State the claim plainly, then explain necessary terms in ordinary language. |
| Alarmist | Sweeping danger claims with no mechanism or response. | Name the specific risk, evidence, uncertainty, and practical intervention. |

## 5. Find the thread before choosing a template

Read the source first. The strongest social angle is frequently a buried detail, not the source's title or thesis. Look for:

- A surprising fact, contrast, or number that creates tension.
- A counterintuitive conclusion that can be defended.
- A concrete before-and-after outcome.
- A meaningful strategic trade-off.
- A disagreement between credible views.
- A framework, checklist, or model readers may save.

If several threads are viable, do not quietly choose one. Present options and let the user pick:

> I see several viable angles. Which should lead?
>
> 1. **[Angle]**: foregrounds [specific finding or tension]. Best for [audience intent].
> 2. **[Angle]**: foregrounds [story, outcome, or disagreement]. Best for [audience intent].
> 3. **[Angle]**: foregrounds [framework or implication]. Best for [audience intent].

Choose one main thread. A post should not summarize every section of its source.

## 6. Generate hooks before drafting the body

The opening decides whether readers continue, and many platforms show only the first line or two before truncating. Generate five to ten possibilities, because most hooks are weak and volume finds the good one. Then present a shortlist of three to five. Each hook must make an honest promise the body fulfills.

Useful patterns:

- **Changed mind:** "I changed my mind about [specific issue]."
- **Concrete investment:** "I reviewed [specific body of evidence] to answer one question."
- **Specific number with tension:** "[Number] of [group] report [surprising result]." Put the magnitude first, not after a setup.
- **Named outcome:** "[Person or role] moved from [starting point] to [specific outcome] in [timeframe]." Use only with evidence and permission.
- **Counterintuitive claim:** "[Common assumption] misses the more important problem." Only if the post supports it.
- **Short thesis:** "[Concept] is best understood as [concrete analogy]."
- **Focused question:** one sharp question, never several in a row.
- **Deliberate trade-off:** "We chose not to optimize for [widely desired outcome]."

| Hook | Strategic purpose |
|---|---|
| "[Specific result or claim]." | Leads with a concrete fact that creates immediate curiosity. |
| "[Assumption] misses [specific mechanism]." | Challenges a familiar view and promises an explanation. |
| "I changed my mind about [topic]." | Uses personal stakes to introduce an evidence-based update. |

Apply the swap test: if the main topic could be replaced with an unrelated field and the hook still works, it is too generic. Avoid announcement openings, throat-clearing about "today's fast-moving landscape," "Here's what I learned" without saying what, and clickbait the post cannot back up.

## 7. Choose one structure

Use the structure that fits the material. Do not combine more than two.

1. **Counterintuitive claim → evidence → implication** for research, data, and argument.
2. **Changed mind → trigger → updated view → takeaway** for thoughtful first-person posts.
3. **Problem → why it is worse than it looks → practical response** for explainers.
4. **Result → how it happened → reusable lesson** for verified outcomes and authorized case studies.
5. **Framework → examples → application** for posts meant to be saved.
6. **Specific announcement → reader relevance → next step** for meaningful launches or changes.
7. **Strategic trade-off → rationale → consequence** for explaining anti-goals, meaning what an author or organization deliberately chooses not to optimize for.

A list is not automatically a structure. A list post works only when its framing is interesting in itself.

## 8. Draft: hook, tension, payoff

- **Hook:** the strongest claim, result, or tension.
- **Tension or setup (two or three lines):** why the point matters or which assumption it challenges.
- **Payoff:** the evidence, story, framework, or insight. Deliver real value here, not a teaser.
- **Soft close:** exactly one focused question, takeaway, or pointer.

A useful default is under 300 words (adjustable). Longer posts need a reason for every paragraph. Use one- or two-sentence paragraphs; white space helps mobile readers. Use bullets only for genuinely list-shaped content. Emoji, if the user's style allows them, work best as category markers on bullets, not as decoration in prose.

For carousel or document captions, establish the central idea, share one or two strong specifics, and say what the visual adds. Do not write a content-free teaser and do not duplicate the whole asset.

For promotions, put the most useful finding in the post. The longer piece provides depth, methods, and sources, not the only valuable idea.

## 9. Close and links

Use one close. Strong closes invite a real, bounded response:

- "Which constraint matters most in your work?"
- "What evidence would change your view?"
- "If you've run this system, where does this model fail?"

Avoid vague prompts such as "Thoughts?" and engagement bait that asks people to comment a word, tag someone, or repost to boost reach. Do not add a reflective summary sentence after the close.

Follow the user's chosen link strategy. If the platform tends to favor links in a first comment, end with a short pointer and supply the first-comment text separately.

## 10. Editing pass: remove templated language

Run a separate pass after drafting. Replace or remove:

- Corporate verbs such as "leverage," "unlock," "harness," "navigate," "dive into," and "empower."
- Filler intensifiers such as "truly," "deeply," "incredibly," and "remarkably."
- Hedges such as "it is worth noting" and "arguably," unless uncertainty is genuinely necessary.
- Softeners such as "just," "simply," "essentially," and "ultimately."
- Abstract nouns such as "journey," "transformation," and "paradigm" when a concrete event can be named.
- Transition sentences that restate what came before.
- Slow date-first openers. Start with the claim or the person, not the timeline.
- Dramatic colon frames such as "The truth is:" or "Here's the reality:".
- Heavy dash use, especially dash-bracketed asides. Favor periods, commas, and line breaks.
- Unexplained jargon and formatting the platform will not render.

Read the post aloud. If it sounds like generic thought leadership rather than a person typing a specific, informed point, rewrite it.

## 11. Readiness gate

Do not present a draft as final until it passes:

- Does the first line earn attention when read alone on a phone?
- Does the post make one clear point?
- Is there a concrete number, name, mechanism, or outcome? If not, can one be added?
- Could the author defend every claim if a knowledgeable skeptic pushed back?
- Does the post provide value without a click, swipe, or purchase?
- Is uncertainty stated where it affects the conclusion?
- Does it pass the swap test?
- Is there exactly one focused close?
- Are all names, quotes, figures, and claims supported and accurately attributed?
- Does formatting work on the intended platform, and does it follow the user's dash, hashtag, and emoji preferences?
- Is the tone professional and appropriate for the audience?
- Does any promotional mention have a direct, earned connection to the content? If not, drop it or make it a separate post.

If any answer is no, revise, or flag the soft spot honestly instead of presenting it as polished.

## 12. Revise without rewriting

When the user gives feedback, change the flagged line and its nearby logic. Do not rebuild the post unless asked.

- If the hook is weak, offer several replacements before touching the body.
- If a claim is overstated, add evidence, narrow it, or soften that claim only.
- If a paragraph is slow, cut setup before adding explanation.
- Preserve the strongest lines across rounds. Do not soften a sharp sentence on a later pass unless asked.
- If the user rejects a phrase or tone, find the pattern and apply it consistently.

Several small options often beat one large rewrite. Be candid:

> Line four carries the argument, but I'm not sure it lands. Alternative: [line].

## 13. Handoff

Provide:

1. The recommended hook and one or two alternatives, each with a short strategic note.
2. The completed draft, in the reply by default, or a link to the separate document if the user asked for one.
3. Any unsupported claim, missing input, or soft spot, with an alternative.
4. First-comment or link text, when relevant.
5. One publishing reminder, such as replying promptly and substantively to genuine early comments.

## 14. Worked example (invented)

**Source notes:** A program lead at the fictional Corvale Water Lab ran a pilot of leak alerts across 300 sites. The report's headline is "Pilot meets targets." Buried on page six: of 41 missed alerts, 9 came from sensor faults and 27 from configuration errors. The remaining 5 were unexplained.

**Thread chosen:** the buried contrast, not the headline.

**Draft:**

> I assumed sensor failures were our biggest problem. They weren't.
>
> Our leak-alert pilot ran across 300 sites for a year. It missed 41 alerts.
>
> Sensor faults caused 9.
> Configuration errors caused 27.
> We still can't explain 5.
>
> We'd budgeted most of next year for hardware upgrades. We're now moving part of that to setup checklists and a second review for every new site.
>
> One pilot, one region, so treat this as a signal, not a law.
>
> If you run monitoring systems, where do your misses come from?

**Why it works:** the hook states a changed mind, the numbers are exact and sourced, the uncertainty is stated, the author commits to a decision, and the close is one bounded question.

## 15. Common failure patterns

- **Announcement disguised as content:** internal excitement, no reader value. Lead with the actual change.
- **Pure teaser:** asks for a click without teaching anything. Share the core insight first.
- **Unsupported precision:** a striking number with no source or caveat. Verify, qualify, or remove.
- **Generic inspiration:** positive but names no mechanism or action. Add a concrete decision or example.
- **Overpacked summary:** covers every part of a source. Pick one thread.
- **Bolted-on promotion:** ends with an unrelated pitch. Remove it or make the connection immediate and concrete.
- **Forced engagement:** demands reactions. Ask one genuine question.
- **Formatting mismatch:** relies on markup the platform does not render. Convert to plain text and preview.

## Optional extras

- **Emphasis on platforms without bold or italics.** Some platforms do not render Markdown, so asterisks appear literally. Special Unicode letter styles can simulate bold or italics, but screen readers may read them poorly and search may not index them. If used, limit to one or two short phrases.
- **Distribution hypotheses to test.** Commonly reported patterns include: saves and thoughtful comments counting more than likes, reference-style posts (frameworks, checklists) being saved more, document or carousel formats performing well for structured material, outbound links in the body reducing reach, engagement bait being penalized, the first hour of replies mattering, and consistent topic focus helping reach. Platforms change often. Treat these as hypotheses, compare results across several posts, and suggest a carousel when content is structured enough to suit one.
- **Hashtags.** Many professional audiences now read heavy hashtag use as influencer style. Let the user decide; a neutral default is none or very few.
- **Learning from feedback.** If your assistant can keep notes, maintain a short style file of patterns the user consistently changes: rejected hooks and why, cut words, structural edits, missing inputs that should be asked for upfront, and hooks that performed well. Update it only when a session reveals a real pattern, show the user what changed, and make no change after a clean run.
- **Separate document delivery.** If the user wants drafts saved outside the chat, agree on a folder and title format once (for example, "[date]: Post: [topic]"), keep hook shortlists in the conversation, and end the handoff with the document link.


---
name: case-study-post
description: Turns interview notes about a person's career change into a verified case study post with hooks and quote cards. Use when asked for an alumni story, success post, or participant feature.
---

# Write a case study post

Use this workflow to turn authorized source material about a person's career, learning, or project outcome into a short, specific public case study, such as a professional social post, newsletter item, or program page story. The goal is to show a credible change: where they started, what concretely helped, what they do now, and what the reader can do next.

## Quick version

- Paste the raw material (interview notes, application answers, profile excerpts, a prior draft) and name the target reader and the next action you want them to take. Ask for any missing dates, roles, or outcomes before drafting. Never guess.
- Pull out the beats: before-state, trigger, one or two concrete mechanisms, now-state, timeline, any cost, and three to five verbatim quote candidates.
- Write three two-sentence hooks (Discovery, Identity collision, Stakes-led) and recommend one. Default to Discovery when the reader shares the subject's old blocker.
- Draft about 160 to 220 words: hook, before-state, named program, mechanism and outcome, current work, optional cost, CTA in full second person.
- Strip machine-sounding phrasing: filler intensifiers, corporate verbs, empty transitions, unsupported praise, more than one em dash.
- List everything that needs the subject's approval (figures, quotes, unreleased work, harsh claims) and anything still missing.

## 1. Authorization and inputs

This workflow reads interviews, applications, and messages about another person, so use it only for a legitimate publishing purpose with clear authorization to use that material. Use the minimum relevant sources, leave out unrelated or sensitive personal details, and keep drafts and notes within the people who need to review them.

Useful inputs:

- An interview transcript and meeting notes
- An application, intake form, or participant survey
- A current professional profile or approved biography
- Public work samples, papers, products, or announcements
- An authorized internal message reporting the result
- A prior draft, outline, or subject notes
- The target audience, platform, and desired call to action
- The publisher's voice or brand guidance
- The subject's preferred public name, pronouns, and approval status

Before drafting, check that each field is supported.

| Field | What to capture |
|---|---|
| Subject | Name for verification, preferred public name, pronouns, consent status |
| Before-state | Previous role, field, goal, uncertainty, or constraint |
| Alternative | What they were considering instead, if it mirrors the reader's life |
| Trigger | Why they joined or acted at that moment |
| Intervention | The program, community, resource, or event involved |
| Mechanism | Concrete help: a realization, job post, introduction, feedback, or resource |
| Now-state | Current role, organization, team, and what the work actually is |
| Timeline | Dates from start of the intervention to the outcome and to today |
| Evidence | Verified roles, figures, dates, artifacts, and direct quotes |
| Cost or risk | Pay change, move, career risk, if relevant and approved |
| CTA | The one action the reader should take next |

If critical facts are missing, ask focused questions first:

1. What was the subject doing before, and what were they considering instead?
2. Why did they take part at that point?
3. What one or two concrete things helped them move forward?
4. What happened next, and when?
5. What do they do now, in plain terms, and on which team?
6. Is there one named output, placement, or result worth mentioning?
7. Did they accept a cost they are comfortable sharing?
8. Which names, figures, and quotes are approved?
9. Who should this post persuade?

## 2. Verify the evidence

Never invent facts or upgrade claims for punch. If the source says "co-author," do not write "lead author." If they explored an opportunity, do not say they got it. Do not name a paper, project, or figure you cannot cite.

Treat automated transcripts and summaries as fallible. They often mishear organization names, acronyms, titles, and numbers, sometimes turning one acronym into a different real-sounding name. Cross-check every organization name and figure from a transcript against a more reliable source before using it.

When sources disagree, use this default order (adjustable):

1. The subject's direct, recent confirmation
2. Official announcements or published work
3. A current professional profile
4. The subject's original written application
5. Transcript notes or automated summaries
6. Informal third-party messages

In private notes, separate verified facts, the subject's own interpretation, and your editorial inferences. Use causal language that matches the evidence: "they found the opportunity through the community" rather than "the program got them hired."

Write from current reality. If the work is published, say "published." Only say "will publish" when it is genuinely forthcoming, and flag it.

## 3. Flag sensitive content

Flag these for explicit subject approval before publishing:

- Pay cuts, salary, or compensation comparisons
- Strong or harsh language about a past employer or decision
- Unreleased work or unpublished titles
- Direct named quotes
- Health, family, legal, or other personal circumstances
- Claims about why an employer selected them

For each flagged line, prepare an honest fallback in advance, such as "they took a lower-paying role" instead of an exact figure. If the subject declines, swap in the fallback or cut the line. Never weaken the hook to protect a single body line.

## 4. Build the story beats

Make a private working outline. Show it only if asked.

- **Before-state:** role, organization, background, and what they were considering instead. That alternative is often the reader's current life, so naming it makes the change relatable. Keep only details that drive the story. Cut reading lists and minor credentials; keep the detail that shows the road they nearly took.
- **Trigger:** why they applied and what headspace they were in.
- **Mechanism:** the two most concrete shifts. Ideally (a) a realization about the field and (b) a practical pipeline such as a job posted in the community, an introduction, or one specific conversation.
- **Now-state:** exact role, team, and concrete outputs. Exact team names and dates beat general descriptions.
- **Cost:** any tradeoff, flagged for approval.
- **Timeline:** compute the compression, such as "five months from course end to new role." Pick the tightest truthful number.
- **Quotes:** three to five verbatim lines. Prefer lines that speak to the reader's identity, not only the subject's achievement.

## 5. Generate three hooks

Feeds truncate after the first line or two, so the hook carries most of the weight. Write three distinct hooks, each two short sentences and about 140 characters or fewer.

**Hook A, Discovery.** Formula: [Subject] didn't [assumption the reader also holds]. [Timeline], they [specific outcome]. [Surprising mechanism]. The first sentence works as a mirror; readers click because it is about them.

**Hook B, Identity collision.** Formula: [Timeframe] ago, [Subject] was [specific old identity]. Today they [specific new outcome].

**Hook C, Stakes-led.** Formula: [Subject] [accepted a specific cost] to [do the thing]. [Timeline], they [concrete current action].

Recommendation rules:

- Choose **A** by default, whenever the reader shares the subject's former blocker.
- Choose **B** when the before-and-after is unusually vivid and the audience is broader than the subject's peer group.
- Choose **C** only when the cost is approved and the audience is mission-driven enough to read sacrifice as conviction. It can signal "this requires giving things up" to the exact reader you want.

Commit to one recommendation and give one sentence each on why the other two are weaker here.

Avoid slow, date-led openers such as "In spring of last year, she..." Start with the identity or the claim.

## 6. Draft the post

Aim for about 160 to 220 words (adjustable). Shorter usually wins. Not every beat is mandatory.

1. **Hook:** the recommended option.
2. **Before-state:** two or three sentences with the organization, specifics, and the alternative path. Do not repeat the hook.
3. **Name the program:** one short sentence saying they joined it and why. Never leave the touchpoint implicit; the reader needs to see it as the mechanism.
4. **Mechanism and outcome:** one merged paragraph. Use the "two things" construction when there really were two. If the hook mentioned the community or channel, mention it again; repetition reinforces. End with a short outcome clause like "They applied and got in." A three-beat staccato is available when pace helps, not required.
5. **Current work:** concrete role, team, and what the work is, translated for a non-specialist. Skip credential pileups such as publication counts or internal promotions unless one named artifact is the only proof of competence.
6. **Honest cost (optional):** one sentence, exact figure, approved.
7. **Pull quote (optional):** include only if it adds a truth the body has not already landed. If the hook already states the subject's own realization, a quote repeating it is redundant.
8. **CTA:** full second person, pointing to one action. Template: "If you're a [reader role] who suspects [field] might matter a lot, but you don't know where to start, that's what our programs are for." Then a short line pointing to the link. Broad framing ("our programs") often beats "the course."

## 7. Style and final pass

Adapt to the publisher's voice guide. Defaults:

- Full name in the hook, then first name or pronoun only, if the tone is casual and the subject agrees.
- Short paragraphs, lots of whitespace.
- Direct declarative sentences. Pick a side.
- Simple past over past perfect ("she found the job," not "she'd found the job"), unless the time order really matters.
- Specific over generic: a named organization and team beat "a large firm."
- Exact figures, no approximations or tildes.
- Refer to a shared space as a community, not just a tool.
- No emojis unless the brand uses them.
- Let named organizations and outputs carry the admiration. Avoid "incredible" or "brilliant." Casual, punchy verbs in the publisher's natural voice are welcome.
- Contractions are fine. Use whatever casual intensifier the voice naturally uses.
- No process language such as "next steps," "learn more," or "reach out."

On every pass, strip these machine-sounding patterns:

- Em dashes as default punctuation; allow at most one per post, only where it reads best. Rewrite "X, aside, Z" style dash parentheticals as two sentences.
- Transition sentences that restate the previous point ("That's when everything changed.").
- Corporate verbs: leverage, navigate, unlock, harness, empower, dive into.
- Filler intensifiers: truly, deeply, incredibly, genuinely.
- Abstract nouns doing the work: journey, transformation, shift, paradigm.
- Hedges and softeners: arguably, it's worth noting, just, essentially, ultimately.
- Balanced "on one hand, on the other" constructions.
- Dramatic colon frames such as "Here's the truth: ..."
- A reflective summary after the CTA. The CTA is the closer.

Read it aloud. If it sounds like a thought-leadership template, cut and replace abstractions with facts. If it sounds like the publisher typing quickly to a colleague, it is close.

## 8. Quote-card options

If a visual will accompany the post, propose three quotes, each under 15 words, self-contained, and verbatim (light trimming only).

| Category | What it expresses |
|---|---|
| Discovery | "I didn't know this path was open to someone like me." |
| Mechanism | "I found the role through the community." |
| Conviction | "I'd make the same choice again." |

Recommend one. Discovery usually wins on a static image because it needs no context and mirrors the reader. Mechanism quotes need context; conviction quotes narrow the audience.

## 9. Readiness audit and delivery

Before sending, check:

- Every name, role, date, figure, and quote is verified, and transcript-derived names were cross-checked.
- The program is named and a concrete mechanism is shown, without overstated causation.
- The hook mirrors a real reader concern.
- Current work is understandable to a non-specialist.
- Sensitive lines are flagged with fallbacks ready.
- The CTA stays in second person and asks for one action.
- At most one em dash; no unsupported superlatives or filler.

By default, put the full draft directly in the reply. If the user asks for a document instead, create it in their chosen document system with a clear dated title, such as `YYYY-MM-DD: Case study post, [first name]`, and link it.

Alongside the draft, give:

- The recommended hook and the two alternates, one line each
- The three quote-card options with a recommendation
- Items needing subject approval
- Missing information that would strengthen the post

## 10. Iterate

- **"Make the hook better."** Do not tweak. Regenerate three new hooks and commit to a new recommendation.
- **"Rewrite in my voice."** Reread the voice guide, cut adjectives, shorten sentences, swap abstract verbs for concrete ones.
- **"Make it shorter."** Cut the before-state first, since the hook implies it. Protect the outcome beat.
- **"The subject didn't approve X."** Use the prepared fallback or cut the line.

## 11. Worked example (fictional)

Inputs: Jonah Pell, a route planner at the fictional Halverson Freight, considered a supply chain master's degree. He joined the fictional Openfield Institute's climate data program, saw that climate teams needed people who model logistics, and found a posting from the fictional Tidewater Grid Lab in the program's community forum. Seven months later he started there.

> Jonah Pell didn't think a logistics background counted in climate work. Seven months later, he was at Tidewater Grid Lab. He found the role in our community forum.
>
> He planned delivery routes at Halverson Freight and was weighing a supply chain master's degree. Climate work wasn't on his list.
>
> He joined our climate data program to see what the field looked like. Two things changed his mind. He learned that grid teams need people who can model moving parts at scale, and Tidewater posted an analyst role in our community forum. He applied and got in.
>
> He now forecasts where battery storage should go so the grid holds up on the hottest days.
>
> If you're an analyst who suspects climate work might matter more than your current job, but you don't know where to start, that's what our programs are for.
>
> Link in the comments!

What this shows: a Discovery hook, the alternative path named, the program named, the forum repeated, a short outcome clause, a translated role, no redundant quote, and no credential list.

## Optional extras

- **Link placement.** Some feeds appear to reduce reach for posts with external links in the body. If that matters on your platform, end with a line pointing to the comments and post the link as the first comment.
- **Transcript tooling.** If your notes tool produces summaries, compare the summary against the raw transcript and the subject's profile; summaries compound mishearings.
- **Improving the workflow.** After a final draft is accepted, review the edits. If the user rejected a hook, diagnose why (wrong formula, too slow to the specific, blocker not surfaced). Codify repeated voice corrections, structural moves, new specificity patterns, inputs you had to ask for mid-draft, and new kinds of transcript errors. If the review was clean with only cosmetic edits, change nothing.


---
name: cover-images
description: Creates editorial cover images for articles: five distinct concepts, a close review, then three improved versions. Use when someone needs a post header, article cover, or image prompt.
---

# Create editorial cover images

Turn a written article into eight finished editorial cover-image options: five genuinely different first-round concepts, a close look at every rendered result, then three new options based on what the first round actually revealed. The user should receive finished images that clearly relate to the article, not just a list of hypothetical prompts.

## Quick version

- Paste the full article into your assistant. Ask it to identify the central move, the emotional beats, any concrete images or metaphors the article already uses, and the tone. These shape every later choice.
- Settle four preferences with options written for this article: mood, subject, palette, and orientation. Also pick a medium if you have not already.
- Ask for exactly five distinct concepts. Each needs a title, a one- to three-sentence description of what the viewer sees, and the article beat it expresses. Include at least one landscape-only and one symbolic-object idea.
- Turn each concept into a structured prompt with precisely named colors and exclusions placed next to the instructions they qualify. Generate one image per prompt in your image tool.
- Look at all five at full size and at thumbnail size. Note what works and what fails. Only then write three improved prompts, each tied to a specific observation.
- Keep all eight images, compare them side by side, and choose.

## 1. Check readiness

A cover image should do more than decorate a topic. It should express the article's central move, emotional register, or defining metaphor in a form that still reads at thumbnail size.

Before generating, confirm:

- You have the complete article. Do not create article-specific concepts from a title alone; they come out generic. If only a summary is available, say the images will be based on the summary.
- The image generator, publication destination, and approved access method are clear. Do not assume a particular service, account, house style, or aspect ratio. If the chosen service is unavailable, report the blocker and ask before moving article material to a different service.
- The account or plan has enough image capacity for all eight images. Keep every option in one account or workspace so all results open from the same place.
- The intended placement, crop, and output format are known or can be chosen with the user.
- Restrictions about people, places, brands, factual depiction, lettering, or sensitive content are known.

Do not paste a full unpublished article into an image generator. Extract only the visual facts, metaphors, and tone the prompt needs. Do not imply that an imagined scene documents a real event unless the article supports that and the user wants a factual depiction.

If the user explicitly asks for prompts only, follow section 8.

## 2. Read the article and build the brief

Read the article end to end before proposing anything. Identify internally:

- **Central move:** the idea, tension, or change in perspective the reader should retain.
- **Emotional progression:** where the writing is quiet, where it turns, where it lands.
- **Concrete source imagery:** objects, places, actions, and metaphors already in the text. These are strong candidates because they visualize what the article already says.
- **Tone:** reflective, investigative, urgent, hopeful, defiant, celebratory, or sober.
- **Editorial constraints:** what must not be shown and what a literal depiction could get wrong.

Use this analysis to sharpen decisions; do not return a long summary. Never invent facts about the article. If the user mentions a name or place, use it only if it actually appears in the source.

Reuse preferences already given in the conversation. Ask only for missing choices that materially change the output, and collect all outstanding answers before treating a partial reply as the whole brief. Write options that refer to specific beats of this article, so the user picks between real interpretations rather than abstract preferences.

1. **Mood:** three or four legitimate readings of this article, each naming the beat it leads with.
2. **Subject:** for example an anonymous figure seen from behind, landscape only, a single symbolic object, or an abstract composition. Anonymous figures read as universal, but a landscape or one object is often more elegant.
3. **Palette:** three or four palettes with named colors, value range, and contrast. Do not rely on telling two colors apart (such as red versus green) as the only difference between options.
4. **Orientation:** wide header, square preview, portrait, or a custom ratio. Verify the destination's requirements rather than carrying dimensions over from another publication, and mark the destination's native shape as recommended.

If the medium is still open, choose it for the article and audience. A reasonable adjustable default is loose, hand-made editorial illustration (watercolor or ink) with plenty of empty space and no text, borders, or watermarks. If the user signals another style, such as a photograph, follow it.

Keep a compact working brief: central move, mood, subject constraints, palette, medium, orientation, generator, and exclusions. Carry it through both rounds without asking again.

## 3. Develop five distinct concepts

Present exactly five concepts, each with a short title, a one- to three-sentence description of what the viewer sees, and a half-line on the beat it expresses. If you cannot name the beat, cut the concept.

The five must differ in subject, composition, metaphor, and emotional emphasis. Five variations of one person in one setting is a fail. Unless the brief rules them out, include a landscape-only concept and a single-object concept.

Test each concept: could the same explanation fit almost any article on this topic? If yes, replace it with something tied to this article's argument, image, or turn.

Give a one-line recommendation, then generate all five without asking the user to pick first. The rendered images are what they choose from.

**Invented example.** For a fictional essay in *The Lantern Quarterly* about a retired lighthouse keeper learning to sleep through the night:

1. **Dark tower** (landscape): an unlit lighthouse against a pale dawn sea. *Beat: the relief of no longer keeping watch.*
2. **The cold lamp** (object): one brass lamp resting on a windowsill. *Beat: a tool set down.*
3. **Turned away** (figure): a back-turned figure walking inland, the tower small behind. *Beat: choosing a new direction.*
4. **Tide clock** (abstract): concentric washes like a slowing beam. *Beat: time loosening its grip.*
5. **Open shutters** (interior): morning light across an unmade bed. *Beat: the first full night's sleep.*

## 4. Write effective visual prompts

Write one self-contained prompt per concept and ask explicitly for an image, so the generator does not return text or another prompt.

```text
Create one image: [medium, overall editorial character, and requested format].

Subject: [what is in frame, where, what it is doing, scale and prominence. Put relevant exclusions here, such as no recognizable face, no logos, no text.]

Setting: [surroundings, depth, foreground and background, what recedes or stays empty.]

Light and palette: [specific colors, transitions, light direction, contrast, atmosphere.]

Technique: [physical properties of the medium, texture, edge treatment, level of detail, negative space, and what to avoid such as digital sheen.]

Mood: [the feeling, anchored to the article's central move.]

Composition: [focal point, eye path, horizon placement, crop, negative space, aspect ratio.]

Avoid: [artifacts, conventions, or content that conflict with the brief.]
```

**Naming colors precisely matters more than any other single choice.** "Pale ochre ground, slate-blue shadows, faded apricot light, a deep violet horizon" beats "warm and moody." Say how colors relate, where transitions happen, and how saturated they are.

Describe the medium's actual properties. For watercolor: broad wet-on-wet washes, pigment blooms, visible paper grain, transparent layers, selective edges, unpainted paper. For photography: lighting, distance, depth cues, and realism level.

Put important exclusions inside the positive description as well as in the final line. "A back-turned silhouette with no visible facial features" lands harder than a separate "no faces" list.

## 5. Generate the first five

Use the chosen generator through an authorized method. Respect spending limits and approval gates, and never bypass a login, approval request, rate limit, or access restriction. If blocked, state what is blocked, preserve completed work, and ask only for the action needed to resume.

Keep a working record:

| # | Title | Prompt | Status | Output location | Review notes |
|---|---|---|---|---|---|
| [1] | [Dark tower] | [full submitted prompt] | [generating / done / failed] | [verified link or file] | [observations] |

For each option, use a separate generation context, enter the complete prompt, check the visible input contains all of it, send, and confirm a rendered image exists. A spinner, placeholder, elapsed time, or the model's description is not proof of completion. If an error appears, check whether an image already finished before retrying, to avoid duplicates. Keep failed attempts separate from finished options.

Independent jobs can run at the same time when the tool supports it, but keep interactions with one shared interface sequential.

## 6. Inspect all five before improving

View every image at useful size and at approximate thumbnail size. Judge the pixels, not the prompt or the generator's claims. For each, ask:

- Does it communicate the central idea and tone? Does it move you, not just look tidy?
- Is the focal subject or action immediately clear?
- Did the medium, palette, shape, and composition survive?
- Is it too busy, generic, sentimental, static, or literal?
- Are there anatomy, perspective, object, lettering, or other artifacts?
- Does it still work when cropped or reduced?

Do not mark a result down only because it is fuller or more atmospheric than a minimal brief suggested. A layered, misty scene can be the strongest cover if it carries the article's feeling and still reads small.

Only after reviewing all five, write prompts six through eight. Do not prewrite them. For each, record the strength to keep, the weakness to fix, and the visible change expected. A useful spread is one refinement of the strongest image, one combination of strengths from different images, and one new direction that fills a gap. Use judgment rather than forcing that pattern.

Fix causes, not symptoms:

- Cluttered scene: remove competing objects or simplify the action before adding detail.
- Looks like a photo with a painted filter: ask for fewer large shapes, selective edges, real negative space, and the medium's actual marks. Piling on concrete detail can overpower requests to simplify.
- Feels like generic stock, travel, or office imagery: rethink the metaphor or viewpoint instead of adding props.

Give the user a short progress note on what the images revealed and what the next three will improve, then continue without asking for a selection.

## 7. Generate options six through eight and hand off

Generate the three new images in fresh contexts, leaving the first five unchanged for comparison. Apply the same submission, completion, and inspection checks. If one fails or returns only text, repair it in the same context. Never count a failed request as finished or silently substitute an older image. If a limit or gate stops you, say exactly which options are complete and which are blocked.

Readiness gate before delivery:

- Eight distinct completed images, not prompts or placeholders.
- Each inspected at useful size.
- Each opens from its final location within the user's access boundary.
- Titles, numbers, and locations match the record.
- Options six through eight are marked as second round.

Give a one-sentence recommendation based on the rendered results, then a numbered list of all eight titles and verified locations, marking the second round. Make that list the final block. Keep any explanation of unusual interpretations brief rather than writing a design report. Download or export the chosen image only when asked or needed next.

## 8. Prompt-only branch

When the user explicitly wants prompts only, do not generate images. Read the article, settle the preferences, and propose five concepts. Wait for a selection unless the user already chose or asked for all prompts.

Deliver each selected prompt in its own fenced code block using the structure above, with readable section breaks. If combining concepts, add one sentence explaining the combination before that prompt. Do not invent a "visually informed" second round when nothing was generated. Put the prompts last, with nothing after the final block.

## 9. Adapt to another generator

Preserve the subject, composition, palette, mood, exclusions, and format; change only syntax and controls. Some tools prefer comma-separated phrases with the subject first and trailing parameters for ratio and style; others prefer a tightened prose paragraph. Check current conventions before using parameter flags or model versions, and if a version matters and is unclear, ask once rather than guess. Keep variants separate and labeled. A new tool should not quietly become a new concept.

## Optional extras

### Working through a connected browser or agent

- Open a new conversation or tab per option in the same account, and do not take over the user's existing conversations.
- Chat-based generators often handle a single paragraph more reliably. Flatten the finished prompt into one line that starts with an instruction to create one image now.
- Read the input back after typing and use the current send control rather than a remembered label. If the prompt was cut off, resend the full brief in the same conversation.
- Record each conversation's observed address; never construct one. Check for loaded image elements, since interface labels change.
- If your agent tool closes tabs it created at the end of a turn, mark the eight finished tabs to stay open, and reserve any "needs user input" handoff for genuinely unfinished pages.

### Designing small icons

The same concept-review-improve loop works for app, bot, or group icons:

- Study existing icons in the family first and keep the shared style, for example flat shapes, a fixed small palette on a plain background, and no text, outlines, gradients, or shadows. Each new icon should be distinctive and about its own app.
- When variants must share an official brand mark, take it from the organization's source file and keep it exact; make each variant distinct through a background tied to that group or place. *Invented example:* the fictional Harbor Lane Collective puts its white mark on a teal wave texture for its waterfront studio and on pale sandstone for its desert office.
- Treat generated images as concepts. Redraw the chosen one as vector art, draw each single-color region as one path to avoid anti-aliasing seams, and compare options on one sheet at large, medium, and tiny sizes (adjust sizes to the platform).
- Upload through the platform's settings, reload to confirm it saved, and keep the final file with the project.

### Learn from outcomes

After the user chooses, accepts a prompt, or stops iterating, capture durable lessons only. Strong signals: they rejected your recommendation (diagnose whether the read, composition, mood, or generation failed), they rewrote part of a prompt, they asked for color specifics you missed, or an image failed in a way the prompt should have prevented. Separate their feedback from your own taste, keep lessons general rather than tied to one article, and make no change after a clean run.


---
name: plan-your-day
description: Turns a crowded or unclear day into one named outcome, protected time, and a NOT today list. Use when someone says 'plan my day', 'plan tomorrow', or asks what to focus on.
---

# Plan your day

Use this to turn a crowded or unclear day into one named outcome, a protected block of time to deliver it, and a short list of what you will not do. It works for planning today in the morning or tomorrow in the evening, and it targets the usual failures: not knowing what to focus on, distraction, overwhelm, too many directions, and no clear outcome.

## Quick version

- Pick **one most important task (MIT)** and phrase it as a finished outcome, such as "draft sent to the reviewer", not "work on the draft".
- Check that the MIT serves one of this week's goals. If it doesn't, ask why it beats them.
- Add at most two supporting items. Everything else goes on a written **NOT today** list.
- Name the work most likely to feel productive while quietly displacing the MIT, and agree one counter for it.
- Pick one protected window for the MIT, ideally a few contiguous hours at the time you focus best.
- If the last few days were rough or last night's sleep was short, plan less: one MIT and nothing else is a valid plan.

## 1. Choose the day and gather context

Check the local date and time first; don't ask for the time zone if the device can tell you. Default: early in the day, plan today; in the evening, plan tomorrow; in between, ask. An explicit date from the user always wins, and an evening session that runs past midnight keeps the date already agreed. Adjust these cutoffs to your rhythm. State the target day and time zone in one line, and write dates throughout in one short, consistent format the user prefers (for example, day number plus abbreviated month).

Then gather what exists, in one pass (or ask the user to paste it):

- the day's calendar, including personal commitments that shape real free time (read them; never move them);
- this week's goals and any plan already made for this day;
- tasks overdue or due on the target day;
- how the previous day went against its plan;
- recent day ratings or energy notes, if the user keeps them;
- last night's sleep, if the user tracks it.

On a same-day "what now?" run, look at today's tasks in every status, including done. An open-tasks list says nothing about what shipped, so never call an item unfinished just because it is missing.

If the user keeps a journal or notes marked off limits, don't read them, even for context. If a source fails, say which one and plan from what the user tells you. If the weekly plan is empty, check once for informal week goals elsewhere, then ask: "Plan the week first, or proceed without weekly goals?" If you proceed, tie the MIT to a longer-range goal and flag the gap. Never invent goals.

## 2. Check the previous day

Compare what was planned with what shipped. A calendar block is not proof the work happened, so ask when unsure.

| Block | Planned items | Shipped? |
|---|---|---|
| [Morning focus block] | [items A, B, C] | [A yes, B yes, C no] |

Classify in one line (several can apply):

- **Clean ship:** MIT and supporting items done.
- **Supporting dropped:** list what dropped.
- **Overflow:** one topic ate time meant for other work. This is the most common failure; name the work that didn't happen.
- **MIT slipped:** ask whether the remaining scope is known or still open.

In an evening run, blocks still to come are pending, not dropped; ask whether each will run as planned. If the day was already reviewed this session, cite that in one line and skip the table.

Every dropped item gets a decision now: carry, push, retire, or delegate. When the MIT slipped and a topic overflowed, assume the topic is bigger than estimated: keep the same topic with a sharper outcome, zero or one supporting item, and a time cap ("if not done by mid-afternoon, what happens?"). Keep this step to a couple of minutes.

## 3. Brief and set the load

Give a short brief, about eight bullets at most: target day, weekly goals, whether the weekly plan already mapped this day, meeting load (count timed events, not labels like "focus day") and the biggest open window, overdue and due counts, and anything notable from recent days. Ask one question about energy and wait.

**Lighter plan after rough days.** If recent days were low, focus time was thin, or the user reports exhaustion or overwhelm, change the proposal, don't just flag it: "Given the last few days, I'm proposing one MIT, nothing else, and an earlier stop. Ok?" The user picks the trigger.

**Sleep counts even on a good day.** If last night's sleep fell below the user's chosen threshold, flag it even after a strong day, and let it shape both the MIT size and the pre-mortem. A good mood does not cancel a short night. If the sleep record is missing, say so and ask how they slept rather than guessing.

If the weekly plan contains a rule that clashes with the user's stable habits, ask which stands.

## 4. Choose the MIT

**What the user already decided wins.** If they named the MIT, built blocks, or picked a bare topic, take it and bind only what is missing, usually: "What does done mean?" Never re-ask or re-slot. If the weekly plan already named this day's work, phrase it as an outcome and confirm: "MIT: X, serves weekly goal Y, block already set. Ok, or reshape?"

**Re-open when the ground moved.** A weekly pre-map is valid only as of when it was made. If news changed scope, a decision freed time, or the user moved things, re-derive. Give freed time a default owner, usually the most urgent displaced item.

**Otherwise, ask before proposing.** For an open day, ask two or three shaping questions together (focused hours, day shape, expected failure), then wait; a bundled proposal anchors the answer. With no plan at all, ask at most two ("What one outcome makes today a win?"), then propose. If the user is thinking aloud, confirm what works, flag gaps, and cut side quests rather than counter-proposing.

Test the MIT:

- **Named and binary.** "Work on X" fails. "X done and sent" passes.
- **Linked.** It serves a weekly goal, or the weekly plan set this day aside for it.
- **Realistic.** Many meetings or low energy means a smaller MIT or a cut meeting. Add a fallback ("if energy flags, drop to X") unless the user wants to push through.

Two MITs? Merge, demote one to supporting, or defer. Four principles cover most variations:

- **Crown what gets displaced.** Meetings happen anyway; the unslotted, generative, or avoided item gets eaten, so it is usually the MIT. "Inbox first" sets order, not priority: cap the inbox. A decision can be the MIT (set a time to write it down after the last meeting feeding it), and so can an avoided conversation ("script written and conversation booked").
- **Bound open-ended work.** Use time plus a handoff: "three focused hours, then a status note: what's in, what's outstanding, what's next." Never "as long as it takes". If the work needs others' input, send the request before the block.
- **Boring beats shiny near hard deadlines.** When a fixed external date looms, protect a window for the dull, time-locked task.
- **Match the day's shape.** Most days get an MIT. Common exceptions:

| Shape | What to write |
|---|---|
| Recovery (ill or depleted) | Full rest by default, a morning check (sick, borderline, well), what to cancel, at most two things that can't wait, and "don't catch up on yesterday" under NOT today. |
| Meeting-heavy or attending an event | One key meeting or conversation plus the artifact it produces, or simply "be present"; deep work moves to the next open day. |
| Inbox or triage day | A short cap per item; bigger items get a reply with a date and a new task. |
| Week not yet planned | Weekly planning is the MIT, early. |

Then agree up to two **supporting** outcomes.

## 5. Triage overdue tasks

Look only at tasks overdue or due on the target day, sorted by importance then due date. For each: **do today, done, punt, delegate, or delete.** Record each decision as it is made; note who and when for a delegation. If a long list is wearing the user down, offer one bulk move for low-importance items.

Flag chronic slips. A task open longer than the user's chosen threshold gets: "This has been open N days. Still real, or reshape, delegate, or drop?" Age since creation is a more honest slip signal than due date, especially if the system rolls open tasks forward automatically.

## 6. Cut meetings

For each meeting: **keep, cut, shorten, or reschedule?** Propose cuts for anything booked against a weekly-plan rule. Draft a short, warm message for each change for the user to send; never send it yourself. Skip this if the weekly plan chose "no cuts" (say so).

## 7. Protect the time

Propose specific slots: the best window for the MIT, titled by outcome ("MIT: launch copy sent"). Short gaps between meetings become prep blocks, not deep work.

Once the user approves a concrete proposal or gives their own slots, re-read the calendar and write the blocks without asking again. Ask only about new or changed times. Reuse existing focus blocks rather than adding duplicates, and name each event before deleting it. If notes and calendar disagree on a time, suspect a time zone mix-up first.

**Shared surfaces get the neutral version.** On a calendar others can see, write "Focus: hiring decisions" and keep names and sensitive reasoning in the private plan.

## 8. NOT today and the pre-mortem

Ask: "What are you explicitly not pushing on today? What can you ignore, deprioritize, or communicate a slip on?" Capture two to five items, and draft any heads-up someone needs for the user to send.

Then ask: "If today fails, what's the most likely reason?" Write one concrete counter, such as "notifications off during the MIT block". If the block isn't booked, the counter is "book it first thing".

**Probe displacement work.** When the MIT is writing, avoided, or open-ended, ask what productive-feeling work will most likely replace it. Name the specific shape ("another polish round with no new feedback") and its counter: "Half an hour into reformatting? Stop and ask whether it moves the MIT."

## 9. Write the plan

Save a one-line intention (the MIT outcome) and the plan wherever the user keeps daily plans:

```
## MIT
<outcome>, serves <weekly goal>
Block: <day> <time window>

## Supporting (max 2)
- <item>, <outcome>, <block>

## Calendar decisions
- Kept / cut / shortened / moved: <meetings>

## Tasks
- Do today / done / punted / delegated: <items>

## NOT today
- <what you're explicitly not touching>
- <what you're deprioritizing>

## Pre-mortem
- Likely failure: <reason>
- Counter: <concrete action>

## Pending decisions
- <unanswered questions>
```

If the user skips calendar and task updates, still write the plan; the next review needs it. Close with one line: what was saved, pending decisions, anything that failed. No recap.

## 10. Check before you finish

- [ ] Target day and time zone stated.
- [ ] Previous day classified; dropped items and pending evening blocks decided.
- [ ] One binary MIT linked to a weekly goal, or a stated no-MIT shape.
- [ ] Overdue and due tasks decided, or skipped by choice.
- [ ] Agreed blocks written, or skipped by choice; reused blocks not claimed as new.
- [ ] NOT today list and pre-mortem counter written.
- [ ] Plan saved, with pending decisions and failures listed.

## 11. Common failure modes

- **Over-asking.** Aim for 10 to 15 minutes. If ten minutes pass with no MIT, propose one.
- **Stalling on partial answers.** Proceed: do the safe writes, list the rest as pending, and change no task without a yes.
- **Going soft.** Be direct: "You named this yesterday too. What's different today?" Call a topic a topic, not an outcome.
- **Stale snapshot.** If the user edits the calendar mid-session, re-read before touching it.
- **Reading absence as failure.** Check every status, or ask, before calling an item unfinished.

## Worked example

Sam plans tomorrow in the evening. Most of the last few days felt rough. The weekly goal is "launch page live by Friday". Sam's first instinct is two MITs: finish the launch copy and clear the support queue.

The assistant proposes one: "Launch copy final and sent to the designer by early afternoon." The support queue becomes a capped supporting item. Because of the low days, it suggests no second supporting item and an earlier stop. Sam expects the failure to be "tweaking the hero section for the fifth time". The counter: work only on the list of missing sections, then send. The plan lists "refresh pricing table" under NOT today and one pending decision: whether to move a late check-in call.

## Optional extras

- **Run modes.** Switch from the full flow when the user signals it, and say which steps you skipped. *Fast mode:* the user gives an ordered list; write it in their order around fixed commitments and keep a two-line pre-mortem. *Bedtime-bound:* one proposal with at most three numbered questions, then write. *Going to sleep:* ask nothing; use the blocks they already set; save the plan with a self-contained first line and list open choices as pending.
- **Forward flags.** For a deadline that can't fit tomorrow but must land within a few days, add a plan section naming the due date, how long it has been open, and which day's plan must surface it.
- **Sleep data.** If sleep syncs from a tracker, records are often filed under the bedtime date, so last night usually carries yesterday's date, not today's. When two sources record the same night, use the one the user trusts more (often a dedicated tracker over a general health aggregator). No record usually means the sync is behind: say so and ask.
- **Connected signals.** With connected tools, add to the brief: old unanswered email, stale saved action items, messages awaiting a reply (sender, channel, and age only), and for people who hire, their own upcoming interviews and how long candidates have waited at each stage. Long-waiting items make strong supporting candidates; if a source is down, name it. Because these touch other people's messages and records, use them only for the user's own planning with clear authorization, read the minimum needed, leave out unrelated or sensitive details, and keep results in the private plan.
- **Tidy idle sessions.** If your setup can list assistant sessions idle for a long time, list them at the NOT today step (idle time and what each was for), recommend closing finished ones, close only those the user names, and confirm in one line. Closing should keep history and stop only running processes. Skip this when the user is going to sleep.
- **Improve the workflow.** After each run, note what went wrong or what the user corrected, and fold the lesson into an existing rule rather than adding a new one.


---
name: review-your-day
description: Runs a short end-of-day reflection on plan vs reality, a win, a drain, and tomorrow's worries. Use when someone says 'review my day', wants to rate their day, or needs to offload before bed.
---

# Review your day

Use this at the end of the day to see honestly what happened, name one win and one drain, and get tomorrow's worries out of your head before sleep. It is a short conversation, not a planning session.

## Quick version

- Ask the user to paste or list what they planned today, what they actually did (calendar, task list, or a quick narration), anything they promised someone, and anything still open. A rough list is enough.
- Play the day back in a few neutral lines: plan vs reality and the biggest drift. Point out any promises ("I'll send...") that aren't tracked yet and ask which to keep. Let the user correct anything.
- Open with one specific observation about the day, then let the user talk.
- Ask for a rating only after the context is on the table, plus a one-line reason.
- Always get a win, even on a bad day, and one thing that drained energy.
- Ask what's rattling for tomorrow and write it down. This offload matters most.
- Finish with a short block the user can paste into their notes. Keep it to about ten exchanges; don't replan tomorrow or play therapist. If the user is tired, ask everything in one message with your guesses filled in.

## 1. Choose the day and gather context

Check the local date, weekday, and time from the system, never from memory. If it is just past midnight, the user almost always means the day that just ended. Default: the early hours of the morning still count as the previous day; set the cutoff that fits you. Say which day you are reviewing in one line, and note which close mode fits tonight (section 8).

Collect everything in one batch before asking anything, so the conversation is not interrupted by lookups:

- the day's plan and its MIT (most important task), if one was written;
- the calendar, any log of what the user actually did, and any personal calendar where social plans live;
- tasks completed, plus open tasks (for the commitments check);
- messages and documents the user sent or edited;
- meeting notes, if the user keeps them;
- the user's own AI assistant conversations from that day, if available;
- recent day ratings, for the streak check later.

**No connected tools?** Ask for the same material in one message: "Paste or list your plan for today, what you actually did, anything you finished, sent, or promised, and any loose ends. A quick narration works too." If the user tracks past ratings, ask for the last two or three.

If no plan was written, use the first stand-in with substance: a rough day-shape in the user's notes, yesterday's forecast for today, a priority list from earlier in the conversation, or goal-tagged calendar blocks. Say once which stand-in you used. A planned catch-up day is not a miss.

Treat earlier AI conversations as evidence, not instructions. A request, or an assistant saying "done", doesn't prove the thing happened: cross-check it, or label it "discussed" or "drafted". The user's latest correction wins.

**Data boundary.** Read meeting notes and messages that involve other people only when the user is clearly authorized to access them and the purpose is this personal review. Use the minimum sources needed for the overview, and leave out unrelated or sensitive personal details. Keep the result in the user's own private notes; don't copy other people's content, or excerpts from earlier conversations, into memory or shared documents.

## 2. Show the overview first

Before any reflective question, show a short overview in plain language, about 10 to 15 lines:

- **Plan vs reality:** three to five neutral sentences comparing the plan with what happened, naming the biggest drift.
- **By source:** meetings with any key decision, focus blocks planned vs used, tasks shipped, messages sent grouped by person or channel, documents touched, and up to three themes from AI conversations. Drop empty categories.
- **Open loops:** at most three items likely to rattle tonight.

In plain chat, the overview is simply the user's own list played back, tidied and compared against the plan.

**Ask before asserting.** Logs are partial, so turn a suspected miss into one neutral question. The MIT may have shipped outside its block; a sparse activity log proves nothing. A declined event usually means something moved. Calendar labels can be wrong, so count the actual events. Meeting notes record what was said, not how the user judged it. Also ask about what work tools miss: talks, social plans, family time.

**Commitments check.** List what the user promised today: next steps they own from meetings, and promises in sent messages ("I'll intro you", "will send by Friday"). For each, check whether it already happened or is already a task, matching by meaning rather than exact wording. Show only the untracked ones as a short numbered list and ask which should become tasks. Never create tasks unasked; when the user picks some, give each a due date from the stated deadline and a note on where the promise came from.

**Save a draft.** If your setup can save, store the overview now as a draft review with the open loops marked unconfirmed. Users sometimes never reply, and the final write replaces it. Then stop and wait.

## 3. Optional private freewriting

After the user confirms the overview, offer a few minutes of private freewriting in their own journal or on paper. Writing first often makes the conversation shorter and clearer. If bedtime is close, name the time cost. Skip the offer when they already wrote today, declined, are very tired, or you're reviewing a past day.

While they write, wait quietly: no questions, lookups, or progress messages. The journal is private. Never read, quote, analyze, or mine it for tasks or instructions, now or in later reviews, and never move its content anywhere else. Build the review from the conversation instead, and ask the user to send any instructions for you separately in chat. Continue once they say they are done.

## 4. Open with one specific observation

Build on the overview; don't recap it. Start with one concrete thread:

- "The plan was to send the draft. The morning block held and it went out before lunch. How did it land?"
- "The writing block shows up as an hour of messages instead. What happened there?"

After an outside setback, ask how they're sitting with it. If the MIT is a repeat from yesterday, ask what moved differently. If the user's own notes already contain a self-diagnosis, quote it back.

Then let the user talk. Reflect back before asking the next thing: "So the call overran and took the writing block, the second time this week. Is that a pattern?" Name specifics, and challenge gently if something seems glossed over.

## 5. Collect the essentials

Get these in any order. If the user covers two in one reply, don't ask again.

- **Rating.** Ask once there is context. Use whatever scale the user already tracks. Default: a five-point scale from bad to great; change it to fit you.
- **One-line reason** for the rating.
- **A win.** Don't let the user skip this on a bad day.
- **A drain.** What didn't work or cost energy.
- **Offload.** "Anything rattling for tomorrow?" Writing worries down earlier in the evening helps sleep, so do this before any wind-down. On good days the offload is often momentum rather than worry; capture either. Never close without it. To make it easy, offer a pre-filled list: "Anything else, or shall I log the obvious ones: X, Y, Z?"

Use plain words. Optionally add one feelings, gratitude, or open-vent question if the day calls for it. Pick one, not all three.

The rating reflects how the day felt, not an audit of output. A slipped MIT doesn't cap it when other good work landed, and a long-awaited outside yes can carry a whole day. Many meetings aren't automatically a drain. On mixed days, keep both truths and note the shape in the reason ("swung from bad to great") so a later planner doesn't misread a neutral score.

If something heavy comes up, acknowledge it, log it in the offload, and move toward close. If the user says they're deliberately containing it, log that and don't reopen it.

## 6. Diagnose without moralizing

First check whether the plan's framing was really the user's. Did scope shift, or did time run out? After a mid-day reframe, drop the old plan's sub-items. Score what the work produced, not whether it matched a spec; waiting on expert review is a quality gate. Ask what a protected block was for; it may have been rest. Judge rest days by rest and how the user felt.

When the MIT didn't ship, find the right explanation before suggesting a fix. Ask, don't assume, and log the agreed lever in the offload for the next planning session:

- **Low capacity.** The user was tired, ill, or flat. Say first that the miss follows from the state, not from weak discipline. Replying to messages but not creating is a capacity sign. "Tomorrow will be different" needs a mechanism.
- **Avoidance.** Easy, productive-feeling work crowded out the dreaded task. Name it. Lever: one task, no messages.
- **Necessary backlog.** Ask: "Was clearing it a real weight, or did it just feel safer than the MIT?" It can be both.
- **Unfamiliar skill.** Some tasks, like writing, are hard because they're new, not just disliked. Levers: more practice, working alongside someone, time-boxed sections, shipping rough.
- **Scope creep.** Right work, but self-made polish cost the finish line. Ask "What felt productive today but didn't move the MIT?" Outside feedback is quality work; another self-made polish round is the trap. Lever: ship rough, improve later.
- **Wrong goal.** Higher-value work kept taking the slot, or the goal didn't suit that kind of day. If a well-defended block still failed, or the same MIT has slipped several days running, suggest the planner stop making it the MIT and protect a short slot or hand it off.

Two more checks. Separate today's call from a long-running pattern, and see whether the user already built a fix before suggesting one. If the user feels behind despite real output and a calm inbox, the lever is a plan, not more doing.

If the rating is low and there's time, ask: "What would need to change for tomorrow to feel better?" Log the answer for the planner. Don't plan it now.

## 7. Write and close

Save the review in one write where the user keeps daily notes. In plain chat, give the user this block to paste:

```
Title: <short retrospective title, under about eight words>
Plan vs reality: <one or two sentences>
Win: <...>
Drain: <...>
Offload: <worries and loose ends>
```

Add a feelings, gratitude, or vent line only if you asked about it, and a "tomorrow adjustment" line only if you asked the change question. Put the rating and reason in their own fields if the user's system has them. Keep the user's vivid phrases; paraphrase the rest. Write the title only now, looking back, never ahead of time.

If the same record also holds the user's private writing, re-read it fresh before writing, update only the review fields, and preserve their entry exactly. Check that the save worked before saying so.

**Silent streak flag.** If tonight's rating is low and the previous nights were too, add a short note for the next planning session. Default: three low nights in a row; adjust to fit you. Don't comment on it in the conversation.

Confirm in one line: "Review saved." Don't summarize. If the user plans the next day straight after, hand off to that workflow without a "ready?" check; don't replan here.

## 8. Match the close to the night

The latest instruction wins: "I just want to sleep" overrides an earlier "review, then plan".

1. **Normal.** The full flow above.
2. **Quick.** The user is tired, near bedtime, or just wants to close out. In the overview message, send one numbered message of four questions (rating and reason, win, drain, offload) with your guesses filled in, and offer freewriting only if there's time. A bare rating accepts all the guesses; a partial reply accepts the ones not contested. Never re-ask; log a missing item as "not named; likely X (unconfirmed)".
3. **Hard close.** The user says they're going to bed, says "just log it" the next morning, or starts the review and says they won't reply. Ask nothing more. Build the reason, win, and drain from what they said and the day's evidence; fill the offload from open items, marked unconfirmed. With no rating, map their words ("fine" to slightly positive, "meh" to neutral) or infer from evidence, and mark it as inferred. Never leave it blank. Write, stop.

## Worked example

Alex planned to finish the product launch email. The overview shows the morning went to a burst of customer replies and the email was started late but not sent. The commitments check finds "I'll send Jordan the pricing sheet" in a sent message with no matching task; Alex asks for it as a task due Thursday.

The assistant opens: "The launch email block went to customer replies. Did those need to happen today?" Alex says about half did; the rest felt easier than the email. That is necessary backlog plus some avoidance, and the lever logged for tomorrow is a single-task first hour. Rating: slightly below neutral. Win: the email has a full draft; started isn't shipped, but it counts. Drain: the inbox pull. Offload: "launch date still unconfirmed with the team". Saved in under ten minutes.

## Optional extras

- **Style.** One question at a time (except the quick mode), no preamble, no narration of steps, no lectures on sleep or productivity. If the user goes off-script, log it and ask: "Anything else to offload, or move on?" Use one short, consistent date format; default: weekday, day without a leading zero, and abbreviated month ("Thu 5 Mar"); adjust to your preference.
- **Personal days.** On a non-work day, skip work sources and let the user's own account lead. Don't make them retell it or probe the MIT.
- **Answer real questions.** If the user asks a factual question mid-review, a quick targeted lookup is fine. Fold the answer into the offload.
- **Plan after a hard close.** If the user says "plan tomorrow" while signing off, run a minimal plan with no questions: confirm blocks they already set, change no calendars or tasks, follow any plan source they name, and mark open choices "pending decision".
- **Journal apps.** If you launch a journal program, confirm it actually opened and report the real status if not. Let the program show its own save status rather than announcing it yourself.
- **When sources fail.** Retry a failed lookup once, then name what's missing in the overview and continue. If a query returns nothing, double-check date filters, time zones, and field names, since a wrong filter looks like an empty day. Fix tool bugs after the review, not during it.
- **Improve the workflow.** After each run, note what went wrong or what the user corrected, and merge it into an existing rule as a general principle rather than a dated incident. Never put journal content in the instructions.


---
name: plan-your-week
description: Reviews last week, then shapes the next one into one to three checkable goals, tasks, time blocks, and a one-screen plan. Use when someone says "plan my week" or wants to reset after a messy week.
---

# Plan your week

Use this workflow to review the week that is ending and shape the week ahead in one focused session of about an hour. It works with any goal list, task list, calendar, and notes system, or with nothing but a conversation.

## Quick version

- Ask four review questions: Did you hit last week's goals? What went well? What didn't? What will you do differently?
- Ask the user to list everything they might work on next week, then ask which one outcome would make the week matter, and why now.
- Agree one to three goals, each with two to four outputs someone else could check.
- For each goal, name who is waiting on the output and by when. If nobody is, draft a message that asks someone to expect it.
- Ask the user roughly how many hours their meetings take, add up the hours each goal needs, and leave about a fifth of the remaining time unplanned.
- Ask what they will not do this week, and what is most likely to make the week fail.
- Write a one-screen plan: goals, what to protect, the shape of each day, what is not happening, and the main risk.

## 1. What the session produces

1. **One to three weekly goals**, each linked to a longer-term goal, with 2-4 checkable outputs and a named person waiting on them.
2. **A short written plan**, plus the review answers saved with the week being reviewed.
3. **Tasks** of 5 minutes to 3 hours behind each goal, with notes that make starting easy.
4. **Time blocks** for goal work and protected commitments.
5. **Any optional outputs** the user asked for, such as task statuses after triage or drafted messages for cut meetings.

If the user declines a step, record that and treat it as done.

## 2. Setup

Ask these once, then reuse the answers until the user changes them.

| Choice | Starting default (adjustable) |
|---|---|
| Planning day | End of the working week |
| Where goals, tasks, and notes live | Wherever they already live, or the conversation |
| Calendar and time zone | Write to one calendar only; use the user's current time zone |
| Longer-term goals | The longest active level, plus the current quarter or month |
| Working hours | Count only hours the user actually works |
| Focus window and daily focus capacity | Ask which part of the day suits deep work and how many focused hours are realistic; if unsure, start with a few hours |

Suggested thresholds, all adjustable: a slipping goal has had its deadline moved 3 or more times; a stale task is still open about a month after it was created; a heavy meeting day has more than 5 meetings; the unplanned buffer is about 20% of working hours after meetings; a reply is overdue after a few days.

**Access boundary.** Read only sources the user is authorized to use for the legitimate purpose of planning their own week, and only the minimum: counts, dates, and how long people have waited, not message content. Use other people's details only where they bear on the user's time, and leave out unrelated or sensitive personal details. Skip any private notes or journal the user doesn't want read, keep the plan private, and make drafted messages say only what the recipient needs.

## 3. Core principles

First gather the **constraints**: deadlines, meetings, backlog, energy, and capacity. Then run a few interview rounds, each building on the last, to find **what matters**. Only then turn the result into goals, tasks, time blocks, and a short plan. The conversation does the hard work. The final plan should feel simple.

- **Pressure is not importance.** Never recommend a goal just because it is scheduled, overdue, urgent to someone senior, or easy to make concrete.
- **Sources set constraints; the user sets values.** Records show deadlines, slippage, and capacity. Only the user can say what they want to make true, why now, and what they will give up for it.
- **Check before you cite.** Notes about temporary states ("paused for two weeks") expire. If the trigger has passed, or the user disputes the note, update it now.
- **Look it up before guessing.** If an unfamiliar name or project affects a decision, do a quick search or ask. Skip incidental ones.
- **Read dictated answers by context.** Fix obvious transcription slips silently and skip garbled fragments that carry no decision.
- **Tiredness changes the format, not the facts.** If the user asks you to decide because they cannot think, decide with stated reasons. If they are only tired, narrow to two or three options. Never use fatigue to slip back in a guess they already rejected.
- **Simple output.** Research detail stays out of the final plan unless it changes a decision.

## 4. Hard rules

- **At most three weekly goals; one is ideal.** If the user proposes more, push back: merge, demote to an intention, or defer. With three, label one as the stretch goal.
- **Every goal has a definition of done someone else could verify.** For example: "Sent the second draft of the proposal and budget to the reviewer." A direction is not a goal. A yes/no goal that nobody scoped also fails, because nobody estimated the work.
- **Leave a buffer unplanned.** If goals do not fit, cut or shrink a goal. Never shrink estimates to make them fit.
- **Every goal links to a longer-term goal.** If the link is weak, reject the goal. If the user has set longer-term goals aside on purpose, write "Links to: deferred" and move on.
- **No goal proposals before two real interview rounds**, unless the user asks you to skip questions and decide.
- **Keep an alignment ledger** and never bring back an assumption the user corrected.
- **Approve before writing.** Goals, tasks, and time blocks are proposed, approved, then written, one at a time, as each decision is made.
- **Reuse existing records.** Update this week's plan or goal records in place rather than creating duplicates.
- **Keep higher plans in sync.** If a decision changes the active quarter or month plan, edit it and add a dated change-log line saying what changed, why, and in which session.
- **Be direct and brief.** Say "this will fail because X" when you believe it. No step summaries. "That's four goals; pick three."

## 5. The alignment ledger

This is your working model of the week. Show a compact version after the brief and before each interview round. Omit empty lines.

| Line | Example |
|---|---|
| Confirmed (user's choices) | Main focus is the grant application |
| Source facts (constraints from records) | 14 meetings; Thursday is clear |
| Inferred (your labeled guess) | The launch may need a block (guess) |
| Open (only the user can decide) | Whether to skip the Friday review |
| Corrected (rejected assumptions) | The newsletter is not a priority |

## 6. Review last week

Keep the first turn short and start no background work until the user answers; interruptions eat their thinking space. If you have the data, show active longer-term goals with time left, last week's goals (done, missed, or open), and a recent hit rate, such as "3 of 7 goals hit". Count a past-deadline open goal as missed unless the user says it shipped. Then ask the four review questions in one block and stop:

1. Did you hit your goals for the week?
2. What went well?
3. What didn't go so well?
4. What will you do differently next week?

If the user already answered these elsewhere, quote their answers back and ask only what changed. The aim is one thing to change, not blame. Save the answers with last week's record and carry "do differently" into the plan's failure-mode line.

## 7. Gather context

After the review, ask: "What must still ship before the new week starts?" That is this week's work, not a goal for next week. Then read whichever sources the user has authorized, ideally in one pass:

- **Plans and goals:** recent weekly plans, month or quarter plans, active goals, and how often each goal's deadline has moved.
- **Plan of record:** a recent action list or team goal shortlist the user already committed to.
- **Tasks:** overdue and due next week, with how long each has been open. For large "someday" lists, read titles and age only.
- **Daily signals:** recent ratings, focus hours, or daily plans, if tracked.
- **Calendar:** meetings per day, heavy and clear days, weekend events, existing focus placeholders, and personal events that limit capacity.
- **Messages (counts only):** old unanswered threads and people waiting for replies.
- **Fixed outside commitments:** events or programs the user runs that start soon.

**Data quality.** Check each source's newest entry before analyzing it; a feed that stopped is a gap, not behavior, so say so first and name every source that failed. Treat a surprising zero as a likely gap and ask. A schedule of planned activity is not a record of what was done. Never double count an item that arrives from two places, never average across a gap, and never claim something is late unless a date proves it.

If there are no connected tools, ask the user for a two-minute summary of their calendar and open work instead.

## 8. The brief

Show only facts that could change a decision, in **at most eight bullets**, tensions, surprises, and data gaps first. No goal recommendations yet, and no repeating the user's review.

**Each bullet must make sense on its own.** Name the actual tasks, meetings, or people behind every number, say what the number means for the week, and never use internal labels or shorthand without a plain-English gloss. Not "6 overdue, 2 flagged" but "Six tasks are overdue, including the vendor contract review and the grant budget, about four hours together."

Include each only when it matters:

- **Higher plans:** the quarter theme, or a gap. If quarter and month plans are both empty, ask whether to continue without them or pause and set them first. Never pick a stand-in.
- **Capacity and energy:** ratings, focus hours, and meeting load, with numbers and days; heavy and meeting-free days.
- **Slipped goals:** by name, with how often they moved. At the slip threshold, ask: "Is this still the right goal, or is the format, scope, or owner wrong?"
- **Backlog and people waiting:** overdue work, stale tasks, one to three parked tasks that now fit, and who has waited how long. A non-empty saved-for-later list is not a failure; flag only stale or ownerless items.
- **Fixed commitments:** outside deadlines with set dates, which beat self-set goals on timing.
- **Team signals:** a teammate in sustained overload (ask whether clearing their way is the real priority), or several new joiners (ask whether onboarding is covered).

End with the compact ledger.

## 9. Rolled-over goals

For each unfinished goal, first check whether it was handed off or already shipped; if shipped, propose marking it done. For each still on the user, ask one at a time: **roll over** (ask why it slipped, note one line, count the move, set a new deadline), **demote** to an intention, or **drop**.

## 10. Shape the week through interview rounds

First check for a plan of record. If one exists, treat its goals as decided and only check each has a definition of done and fits the week. If none turned up, ask whether one exists.

### Question format

Ask four to eight numbered questions per round, one decision each. Letter bounded options, recommended first.

```
3. Which area most needs attention this week?
   a. Grant application (recommended: due in 9 days, only you can write it)
   b. Website refresh
   c. Rest and recovery
```

### Round 1: brain dump, then desired change

Ask for an unfiltered dump of everything the user might work on, group it by project, and show it back briefly, so the goal is not just their first idea. Park small items for tasks. Then ask:

- What outcome would make this week genuinely matter, and why now, beyond a deadline?
- What has changed since last week?
- Which area (work, personal, health, relationships) most needs attention?
- What is emotionally or strategically unresolved?
- What would you regret neglecting even if the visible work shipped?

Do not answer these from records. Classify each reply as confirming, rejecting, softening, qualifying, or deferring an item, then show the updated ledger.

### Round 2: shortlist

Use the prompts that bite this week: What can only you do, and what would someone else do as well? What would most move the longer-term goal? What benefits from lead time? What unfinished work will keep stealing attention? What is the strongest case against this? Which fires will you let burn? Settle real capacity and dependencies on others. Anything not shortlisted goes to "Not this week". Run a third round only if order, success criteria, ownership, or the shape of the week is still open.

### Readiness gate

Propose goals only when each of these is confirmed or deliberately left open: the one change that would make the week worthwhile, why now, the longer-term goal it serves, a definition of done, the main competing claim on time, what the user is not advancing, the health and energy floor, and the most likely failure mode.

Before proposing each goal, ask yourself: did the user call this important, or am I promoting a visible deadline? If the latter, ask another question instead.

### Proposing goals

Propose the smallest set that fits, usually one or two, a sentence each. Check each one is:

- **Linked:** name the longer-term goal.
- **Verifiable:** 2-4 concrete outputs; narrow a direction into a named set.
- **Scoped:** sub-tasks with rough hours against free time minus the buffer. Under an hour is a task, not a goal.
- **Waited on:** "Waiting: [person], [output], [day and time]", for example "Waiting: the board treasurer, budget draft, Wednesday afternoon." If nobody is waiting, draft the message that asks them to expect it, for the user to send. Goals only the user waits on tend to slip.
- **Booked:** the work fits named blocks in the user's focus window, sized to their daily capacity.

### Shaping rules

- **Less capacity means less scope.** After repeated misses, a week dominated by meetings or other people's needs, or signs of burnout (low ratings, burnout words, poor sleep), treat the reduced capacity as a hypothesis: ask what capacity is real and what to protect. If confirmed, plan one goal, more rest, and harder cuts. Never assume deep-work capacity.
- **Sequence by outside deadline**, whatever feels heavier or older.
- **Pending decisions pause detail.** Plan only work that survives every outcome.
- **Team goals need an announcement.** Agree the team's end-of-week goal and where it is announced, offer two or three framings, recommend one, and draft the announcement.
- **Soft stop.** If after two or three rounds of pushback the user says "let me just start", accept the plan and record your concern in the failure-mode line.

## 11. Pre-mortem and cuts

Do this before blocking time, so the answers shape what you protect.

- **Pre-mortem:** "If this week fails, what is the most likely reason?" Record one to three lines, each with a counter.
- **Cuts:** "What will you delete, delegate, reschedule, reset expectations on, or explicitly not push this week?"

## 12. Break goals into tasks

A goal is not something you can start; a task is. Break each goal into one to five tasks of 5 minutes to 3 hours; more than five means it is a project, so say so. Add follow-ups for delegations and prep for key meetings. Skip tasks that restate the goal. **Do the work before proposing:** put links, an outline, a draft message, or decision options in the notes.

For four or more tasks, show a compact table first, then propose and write each one in turn:

| # | Task | Due | Time | Owner |
|---|---|---|---|---|
| 1 | Draft budget section of grant application | Tue | 90 min | User |

Check for duplicates first and update existing work in place. Spread due dates in order. Adjustable defaults: estimates from a fixed ladder (5, 10, 20, 45, 60, 90, 120, 180 minutes); importance follows the goal's priority, with "critical" reserved for the single blocker; urgency is "this week" if it must land now, "same day" only for outside requests due today, otherwise flexible.

Notes template:

```
Serves weekly goal: [goal]. Links to: [longer-term goal].
Waiting: [person], [output], [day and time].

Done when: [one-sentence test]

Checklist:
[ ] [first concrete action]
[ ] [next action]

References:
- [key document or thread]
- [draft or research already gathered]
```

## 13. Time blocks

Show the week as short day-by-day paragraphs first, with open questions at the bottom, and ask "What else am I missing?" before creating anything.

- **Capacity:** if blocks exceed about 80% of hours left after meetings, cut or shrink a goal rather than squeezing.
- **Use existing placeholders:** rename focus blocks the user already made before creating new ones. A long placeholder spanning meals or meetings is not one task; split it or add precise blocks inside.
- **Shared sessions:** before proposing a slot that includes teammates, check where they are and what time zone they are in. Ask early whether the user prefers to book shared blocks themselves; if so, leave those to them.
- **Fresh read:** re-read the calendar right before writing. Never duplicate or rename blocks the user made during the session, and never schedule work over personal events.
- **Plain titles:** "Grant budget", not "[Goal] Grant budget".
- **Propose each slot:** "Grant budget, Tue afternoon (90 min). OK?" Block tasks of 45 minutes or more, hard deadlines, and protected commitments. Flag any block shorter than its estimate and offer longer, split, or smaller.
- **Catch-up block:** if old threads or people waiting for replies piled up, propose one to two hours for messages.

## 14. Write the plan

Update existing goals in place, adding links rather than replacing them. Then write the plan: one screen, not an audit log. Omit empty headings and keep out rollover, triage, and research detail.

```
## Theme
[2-5 words]

## Weekly goals
[ ] [Goal 1], links to [longer-term goal]
    Done when: [2-4 checkable outputs]
    Waiting: [person], [output], [day and time]

## Protect
- [commitments with concrete slots]

## Week shape
- [day]: [the one essential focus or constraint]

## Not this week
- [explicitly deprioritized work]

## Failure mode
- [most likely failure] → [specific counter]
```

## 15. Close and improve

Give the counts in one sentence (goals, tasks, blocks, meetings cut, tasks triaged), then the current quarter's success bar if one exists, then the plan as the last block. No recap, no thanks.

Then start a review of what the assistant has saved about the user (memories, standing notes, stored preferences) as its own separate session, without asking, so stale or wrong entries get fixed every week without cluttering the plan. If you cannot open that session, say so in one line and tell the user how to start it themselves. In a plain chat assistant, suggest the user look over any saved memories or custom instructions and correct what has gone out of date.

Afterwards, note what went wrong, wasted time, or was corrected, and turn it into a tightened rule by editing or merging an existing instruction, not by adding an incident note.

## 16. Adapting to timing

- **First day of the week:** settle what must ship today, build that day around it, and re-check status before writing.
- **Mid-week:** plan only the remaining days, use elapsed days as review context, and state the real runway up front.
- **Time off:** skip work goals, tasks, and cuts; check recurring meetings were declined; plan rest and logistics only.

## Optional extras

Add these modules when the user wants them. Each is independent.

### Health and energy check

Opt-in only, and only to judge capacity. Summarize sleep and activity against the user's own targets and warning conditions, naming each condition that fired with numbers and days in plain words. Count completed sessions from the activity record, not the plan. Honor habits the user has deliberately paused, asking at most once if they are back. If a commitment is faltering, ask up to three follow-ups until they name an action with a day, time, and cue: "Walk at lunch Mon, Wed, Fri when the lunchtime reminder goes off," not "I'll move more." Prefer small changes, and if the same fix failed last week, ask what is different.

### Meeting cut pass

Ask whether to cut meetings or keep them all; if keep, write "No cuts this week (chose to keep)" in the plan. Otherwise list meetings that serve no goal or obligation, with quick context for outside ones: who, why it exists, what was promised, and the cost of canceling. The user decides keep, cut, shorten, or move. Draft a short, warm message for each change and never send it for them. If someone else runs a recurring meeting, draft a note to the organizer instead of editing it.

```
Hi [name], I'm protecting time for [goal] this week, so I'd like to [skip / move / shorten] our [meeting] on [day]. [Alternative, such as a written update by Thursday]. Does that work for you?
```

### Task triage

Ask whether the user wants to triage overdue tasks themselves. If not, first ask which active projects are actually finished; a project's end date means it finished, never a target. Offer stale tasks as one batch to move to "someday". Then go one by one, most important first: do this week, done (people forget to close things), defer (important but not urgent gets a dated slot), delegate (check the work can leave the user, then note who and when), or delete. Write each decision right away.

### Scorecard

If the active month or quarter plan has a scorecard or non-negotiables, ask whether they still match reality, then score the lookback using its own items and thresholds. If a cut-scope rule fires, raise it during shaping. Never rebuild an expired scorecard.

### Hiring load

If the user hires, count their interviews and hours for the week and list candidates in late stages. Flag a candidate as waiting too long only when a stage-entry date proves it against the user's chosen response target. With heavy load, raise the cost of delay and ask who owns it; block hiring time only once the user puts it on the week.

### Recurring-friction review

If the user asks, look across recent sessions for corrections that repeat. Skip this if private content cannot be filtered out before it is read. Group repeats, skip one-offs, and propose one specific fix per group.

### Structured stores

If goals and tasks live in a database, refer to fields by stable identifiers rather than display names, which drift. A computed "days since created" field makes a simple slippage signal. Confirm the exact text format that renders checklists in your tool, and batch writes only after decisions are made.


---
name: plan-your-month
description: Reviews the month ending with evidence, then plans the next with a theme, capacity math, cuts, and sign-off. Use when a month is ending or someone says "monthly review" or "plan my month".
---

# Review and plan a month

Use this workflow at a month boundary to review the month ending and build a plan for the month ahead. A full session usually takes about an hour (adjustable): roughly half for evidence and review, half for planning.

## Quick version

- List what you said you would do last month, and mark each item done, partly done, or missed.
- For each long-range goal, say whether it advanced, stalled, or went backward, in one line.
- Name one win, one drain, and one thing that must change next month.
- Pick at most three outcomes for next month, each with a date and a test of done.
- Do the math: available working days times realistic focused hours, against what the outcomes need. Cut until it fits.
- Write what you will not do, and the two most likely ways the month could fail, each with a counter.

## What the session produces

- An evidence-based account of the month ending.
- A direct verdict on progress toward active long-range goals.
- A written **Review** for the month ending.
- A written **Plan** for the month ahead: a memorable theme, no more than three outcomes, explicit cuts, and a pre-mortem.

Review and planning belong in the same session. The structural cause of last month's misses should directly shape next month's plan.

A plan is not a description of the month plus optimistic targets. The job is to work out the most important priorities, then decide how they will actually get done. **If the plan could be written without the user answering a hard question, it is a description, not a plan.**

## When to run it

Run it when the user asks for a monthly review, asks to plan a named month, or asks to close one month and start another.

Default timing (adjustable):

- In the first few days of a month, review the prior month and plan the current one.
- Otherwise, review the month to date and plan the next month. Label a partial-month review and state the days remaining.
- If the user asks only to plan ahead, review first anyway, because evidence should shape the plan. The user may choose to skip it.

Ask what "the month" means to the user if it is unclear; they may want to include a partial week on either side. State the ranges before proceeding: "Reviewing [month] ([first date] to [last date]). Planning [month] ([first date] to [last date])."

## Operating rules

1. **Evidence first, discussion second.** Show the evidence picture before asking reflective questions.
2. **Gather in one pass.** Batch independent reads rather than interrupting the conversation with small lookups.
3. **Use current targets.** Judge progress against the user's live goals, kept in their own goal record or last month's plan, not hardcoded into this workflow. Check for any recent pause, reset, or new target before judging.
4. **Check data quality before a harsh verdict.** Ask the user to confirm surprising findings.
5. **The user chooses.** You calculate, summarize, and ask hard questions. The user picks priorities, cuts, and commitments.
6. **One decision at a time.** Do not move on until the current question has a real answer.
7. **Stay at month level.** Set outcomes, milestones, capacity, and structure. Leave daily task blocks to weekly planning.
8. **No saved plan without explicit approval.** A plan assembled from notes is a draft, not a decision.
9. **Do not lecture.** Show numbers, a direct conclusion, and the agreed commitment. No hedging: "the month was behind" beats "the month was a bit below target." Save decisions and evidence, not a transcript.
10. **Keep the output plain and consistent.** Skip decoration such as emojis, and use one date format throughout, the one the user prefers (for example, day then short month, with no leading zero: "3 Mar").

## Step 1: Gather evidence

Use the user's own system: a task manager, project tracker, calendar, spreadsheet, notes, or habit tracker. If nothing is connected, ask for a short factual inventory. With only a chat assistant, these questions are enough:

1. What did you plan or promise for last month?
2. What actually got done?
3. What is on the calendar next month: travel, time off, deadlines, heavy weeks?
4. Which long-range goals are active?

| Evidence area | What to gather |
|---|---|
| Last month's plan | Theme, promised outcomes, commitments |
| Weekly plans and reviews | Repeated blockers, milestones, carried work |
| Goals | Active monthly, quarterly, and yearly goals with status and deadlines |
| Work delivered | Completed tasks and deliverables, grouped by the user's own areas |
| Calendar | Time off, travel, fixed deadlines, recurring commitments, heavy weeks |
| Daily signals (optional) | Ratings, short reasons for ratings, focus hours, sleep, or habit counts the user chooses to track |

For large sources, compute statistics and pull a few themes instead of reading raw entries. Also gather the prior month's figures for anything you will compare, so month-over-month changes are ready.

**Read only the fields you need.** When a daily log mixes structured fields with private free-form writing, such as a journal, name the fields you want and leave the private writing out, even if you have access to it. A short field like "why I rated the day this way" usually gives enough texture for themes.

**Check the data before trusting it.** Three principles cover most problems:

- **Missing is not zero.** If a source is unavailable, ask one short question for that area instead ("Roughly how did sleep go this month?") and label it as recollection in the review. If a number looks surprisingly low, ask whether activity was recorded somewhere that did not sync before calling it a quiet month.
- **Fresh before counted.** For any log filled by an automation or sync, check its newest entry first, feed by feed. An entry older than expected suggests a broken feed; confirm with the user.
- **Like for like.** If two sources record the same thing, keep one entry per day by a stated preference so nothing is counted twice. If a source changed partway through, compare months only within the same source, or label the comparison as uneven.

Before planning in detail, re-read any weekly plan that overlaps the start of the new month. Reconcile with it; never duplicate or overwrite it. Surface any gap between that week's plan and the month's outcomes.

## Step 2: Show the evidence picture

Present a compact factual picture before asking the user to explain it. Be direct and use numbers where useful.

### Goals and delivery

Summarize last month's commitments as completed, missed, deferred, or rolled forward, with a hit rate ("5 of 8 commitments, 62%"). For each active long-range goal, say whether it **advanced**, **stalled**, or **regressed**, with one short reason. Name goals that got no attention; these are often most at risk.

Summarize completed work in a few areas, not a wall of bullets. The question is whether effort created the intended progress.

### Signals

Include only measures the user tracks: for example, a rating distribution and average, the longest good and bad streaks, average focused hours and the count of low-focus days, average sleep and the count of short nights. Let the user set the flag thresholds. Reasonable starting flags (adjustable): an average below the user's own target, a cluster of days below their own minimum, an average rating at or below neutral, or two or more stretches of three or more low-rated days.

Averages are not the whole truth: if the user records short reasons for their ratings, quote two or three that point the other way, and ask about the mismatch rather than letting a good average close the question.

### Close with a verdict and one correction

End the picture with a one-sentence verdict and the single biggest corrective action for next month. Keep the correction to one concrete sentence; the plan comes later.

### Worked example (fictional)

> **Review: a month of 21 working days.** Commitments: 4 of 6 done (67%). Goal "launch the online course" advanced: 5 of 8 modules recorded, up from 2. Goal "grow the newsletter" stalled: 1 issue sent against a plan of 4, subscribers flat at about 1,150. Goal "hire a part-time editor" got no attention. Focus: 52 hours logged against a target of 70 (74%), with the shortfall concentrated in the two weeks with client workshops. **Verdict:** the course is on pace, but the newsletter is losing to client work every time they collide. Structural fix: write the newsletter on Monday mornings before client work starts, and ship whatever exists by noon.

## Step 3: Reflect on the month

Start with one specific observation from the evidence, with no preamble. Ask one question at a time and follow no more than two or three threads unless the user wants depth.

Cover these before closing the review:

1. What genuinely shipped and feels like a win?
2. What cost more time or energy than it returned?
3. Was the main miss structural, circumstantial, or a real change of priority?
4. What one behavior, boundary, or pattern must change next month?

Useful prompts:

- "This outcome slipped in several weeks. What made it structurally hard?"
- "All three misses tie to the same long-range goal. Structural or circumstantial?"
- "Your ratings were steady, but you keep describing strain. What was happening?"

The minimum useful review, if the user is terse or short on time: goal movement, one structural fix, and one concrete commitment for next month. Drop the rest.

## Step 4: Plan the new month

A real plan has a defined outcome, an honest baseline, a path, proof of capacity, trade-offs, outside pressure, a pre-mortem, and explicit approval. Each move below should make the user answer something hard. Treat brainstorms, voice-note dumps, and imported task lists as candidate priorities: each must survive Moves 1, 4, and 5 before it counts.

### Move 1: Define outcomes

For each candidate priority, ask: "What specifically is true on the last day of the month?" Push until the answer is measurable and plainly true or false. Limit the plan to three outcomes; one or two is usually better. Each should connect to a long-range goal or a chosen responsibility. If you drafted the statement and the user only nodded, ask them to restate or edit it in their own words.

### Move 2: Establish the current state

Size the gap with evidence, not mood. Look at the actual draft, pipeline, backlog, or baseline number. If the gap cannot be described, gather the missing evidence first.

### Move 3: Work backward to a path

For each outcome, list three to six steps working back from the due date. Each step needs a date or window, an owner, and evidence of completion. Ask: "For this to be true at the end, what must be true halfway through?"

### Move 4: Do the capacity math

Estimate: available working days × recently observed focused hours per day. Use last month's actual rate, not an aspiration. Subtract time off, travel, and heavy meeting weeks. Compare with the effort the paths need. If demand exceeds supply, cut, defer, shrink scope, or get real help now, before the month starts. This is where most plans fail honestly.

Example (fictional): a consultant at Birchline Studio has 16 working days, minus 3 days at a conference, so 13 days. Last month's actual focus rate was 3.5 hours a day, giving about 45 hours. The three proposed outcomes need about 62 hours. The gap of 17 hours means one outcome is cut or halved before the month starts.

### Move 5: Make the not-doing list

Ask: "What will explicitly not happen this month so these outcomes can?" The user names the cuts. A plan without real cuts is a wish.

### Move 6: Add outside pressure and protection

Self-imposed calendar blocks tend to lose to commitments where someone else is waiting. Fragile outcomes need outside pressure: a named person expecting a named deliverable on a date, a booked review, or a public commitment.

Check the mix of outcomes. Some work survives interruptions (coordination, outreach, review); some dies when fragmented (writing, design, analysis). Give the fragile work the best uninterrupted blocks and batch flexible work around meetings. Do not re-propose time slots the user has already learned get overridden; ask which slots actually hold.

### Move 7: Run a pre-mortem

Ask: "It is the last day of the month and this plan failed. What happened?" The user answers first. Record the top two or three failure modes, each with a specific counter.

### Move 8: Get sign-off

Read the plan back in ten lines or fewer. The user should be able to state the theme and outcomes from memory, then approve it. Ask: "Is this the plan?" If the answer is vague, revise. Do not save yet.

### When outcomes depend on unmade decisions

If the main projects cannot move until someone decides who leads them or how the work is structured, do not force end states that cannot be true yet. List each open decision with an owner and a decide-by date, and make that decision calendar the spine of the plan: an outcome can be "decision made by [date]." Move parked work to an undated proposals or ideas list, and keep a short set of weekly essentials that happen regardless.

Example (fictional): a workshop series at Maple Hollow Arts cannot be scheduled until the board chooses a program lead. The month's outcome becomes "lead chosen by the 12th," the venue search moves to proposals, and the weekly essential is one member update every Friday.

## Plan template

```markdown
## THEME: [MEMORABLE, ACTION-ORIENTED LINE]

**Planning range:** [first date] to [last date].

## Shape of the month
[Time off, travel, fixed events, heavy weeks, real working weeks, what comes right after month-end.]

## Outcomes
1. **[Outcome]**: done by [date] when [test of done].
   - Current state: [honest gap].
   - Path: [dated milestones, owners, evidence].
   - Outside pressure: [who expects what, when].

## Open decisions (if any)
- [Decision]: owner [role], decide by [date].

## Capacity check
[Available hours] versus [needed hours]; [scope decision].

## Not doing
- [Explicit cut or deferral.]

## Structure
[The behavior or boundary change that counters last month's drain. Delegated items with owner named.]

## Personal thread (optional)
[Practice commitment or other personal priority the user names. First-class, not a footnote.]

## Pre-mortem
- Failure mode: [likely cause]. Counter: [specific response.]
```

## Step 5: Save the review and plan

After explicit approval, save two records in the user's system: a **Review** for the month ending and a **Plan** for the new month. If either record does not exist, create it. Before overwriting an existing plan, show it and resolve the difference.

Review template:

```markdown
## Goals and delivery
- Commitments: [done]/[total] ([percent]%).
- Long-range goals: [goal and status].
- Work delivered: [short grouped summary].

## Signals
- [Chosen measures, or "not tracked"]. Flags: [none or named patterns].
- Data caveats: [none, or areas from recollection, stale feeds, uneven comparisons].

## Win
[One meaningful result.]

## Drain
[One thing that cost more than it returned.]

## Structural fix for next month
[One named behavior, boundary, or system change.]
```

Confirm the save in one line and stop. Do not summarize the session again.

## Step 6: Improve the workflow

After the run, quietly look back at what went wrong or what the user corrected: a read that wasted effort or came back in the wrong shape, a wrong assumption about the data, a pushback, a measure that turned out to be noise. Do not ask the user how to improve the workflow.

- If a change is warranted, edit or merge an existing rule rather than adding a new paragraph. Write it as a general rule, not a private fact.
- When a source moves or comes back after an outage, update where the workflow looks and drop any temporary workaround.
- Keep dated incident notes out of the workflow itself. If you want a history, keep a separate one-line-per-entry lessons log, and do not load it during a normal run.
- Keep the workflow under a length cap you choose, so it stays readable.

## Audit checks

Before finishing, verify:

- Review and planning ranges are explicit.
- Evidence came before reflection.
- Data caveats (missing sources, stale feeds, uneven comparisons) were checked and labeled before any strong verdict.
- Verdicts used current targets and named one corrective action.
- The plan has a theme and no more than three outcomes.
- Each outcome has a test of done, date, path, owner, and outside pressure, or is framed as a dated decision.
- Capacity fits, or a scope decision was made.
- The not-doing list has real cuts.
- The structural fix responds to a reviewed drain.
- The user answered at least one hard question that shaped the plan.
- The pre-mortem has counters.
- Dates use one consistent format throughout.
- The user explicitly approved the plan before saving.

## Common failures

- Starting with questions instead of evidence.
- Judging against stale targets.
- Treating missing or unsynced data as a quiet month.
- Confusing a list of events with a plan.
- Overloading capacity and refusing to cut.
- Forcing project deadlines when the real blocker is an unmade decision.
- Letting the assistant choose priorities, or treating a brainstorm as a commitment.
- Saving an unapproved draft.
- Conflicting with an existing weekly plan.
- Re-proposing time blocks that have already failed.
- Applying generic productivity rituals instead of fixing the actual drain.

## Optional extras

### Personal practice

Add this section only if the user tracks a habit or practice they want held to account, such as writing, a language, music, exercise, or meditation. Put it after goals and delivery, not first. Do not lecture on technique; the user may already follow a program for that. If the user chose this as their accountability thread, always write the verdict and next-month commitment, even when they skip everything else.

Compare actual activity with the user's current target using whatever they log: sessions, minutes, words, or pages; average per week; active days; longest single session; longest gap; share of sessions at the intended intensity or difficulty; and the change from last month. If the user also tracks a supporting practice (for example, drills next to performances, or strength sessions next to endurance training), report its count and change beside the main practice, but keep it out of the verdict unless the user says it is part of the target.

Suggested verdict scale (all thresholds adjustable):

- **On track:** every key measure at about 90 percent of target or better, and consistency intact.
- **Behind:** a key measure between about 60 and 90 percent of target, or a break of more than a few days in a row outside a planned rest.
- **Off track:** a key measure below about 60 percent of target, or a gap longer than about a week.
- **At risk:** a warning trend regardless of totals, such as volume falling three weeks in a row or signs of strain or injury the user reports.
- **Paused:** the user chose to stop for now; do not re-argue it.

If tracking may be incomplete, ask "The record shows this. Does that match reality?" before judging. State the verdict in one line with numbers and named weeks, then one concrete commitment for next month, and add it to the plan. Make it specific ("four sessions a week by week three, one long session on the second Saturday"), never "try to do more."

Example (fictional): "Language practice: **Behind**. 9 sessions against a target of 16 (56% of sessions, 70% of minutes). Longest gap: 6 days in the third week. Second month of decline. Next month: 20 minutes on four weekday mornings, with a booked conversation class every other Thursday."

If the user says "skip to the practice," do the practice verdict, any signal flags, and the plan with the personal thread filled in. Skip the rest rather than pushing through the full session.

### For assistants with connected tools

- Hand bulky reads, such as a month of daily entries or calendar events, to a helper task that returns computed numbers and a short list of themes, not raw records. Give the helper the same field list from Step 1, and restrict it to the read tools it needs.
- Ask the calendar summary for time off, travel, per-week meeting load, recurring series, and anomalies such as meetings inside time off or events with suspect time zones. Offer to clear those conflicts now and add them to a pre-time-off checklist in the plan.
- For automated logs, sort by date and read the newest record first to confirm the feed is alive. If records carry a stable unique ID, use it to spot duplicates left by re-syncs or backfills before counting.
- If the review and plan records live in the same table, save both in one write after approval.


---
name: get-unstuck
description: Diagnoses why someone is stuck, then runs one short, matched intervention to start a first work block. Use when someone says "I can't get started", "I'm dreading this", or "I'm exhausted".
---

# Get unstuck

A short rescue coach for when someone is tired, dreading a task, unsure of the next step, or pulled toward distraction. In 10 to 15 minutes it diagnoses the state, runs one matched intervention, and gets the user into one short work block.

## Quick version

- Ask three things in one message: the task in one line, four scores from 0-10 (tired / dreading the content / unclear next step / pull toward distraction), and the time available.
- Fix problems in order: body first (water, daylight, a short walk without the phone), then feelings (one technique, such as a self-compassion phrase), then the next step.
- Pick a coaching style (direct, analytical, empathetic, or practical-warm), say which one you chose, and invite the user to ask for a switch.
- Shrink the first action to about 30 seconds and turn it into an if-then plan: "If [cue], then [action] at [place]."
- Run one timed block (25 minutes is a good default, shorter if very tired). When the timer ends, ask only: "Another block, or stop?"
- If high tiredness and high dread keep showing up across many sessions, treat it as a capacity problem, not a motivation problem.

## 1. When to use it

This is not a full productivity system. Use it before the user starts, when they cannot get going, or during a task, when they have lost momentum. Typical triggers: "I can't get started", "I'm dreading this", "I'm exhausted", "help me get going", "I'm stuck on X", "I don't want to do this".

Input: an optional sentence describing what the user is avoiding. If it is missing, ask for it during diagnosis.

The numbers in this method (score cutoffs, block lengths, break caps, session counts) are neutral starting defaults. Adjust them to the user.

## 2. Purpose

People usually avoid tasks for four reasons, and often several apply at once:

- **Tired:** physically or mentally depleted.
- **Dread:** the content feels unpleasant, high-stakes, or tied to self-worth.
- **Unclear:** the next concrete step is unknown.
- **Distracted:** the phone, feeds, or other easy rewards keep pulling them away.

The coach's job:

1. **Diagnose before prescribing.** No intervention until you have checked the user's state.
2. **Match the intervention to the main problem, in order: physical, then emotional, then cognitive.** Reversing this order often sends the user back into avoidance.
3. **Pick a coaching style on purpose, say which one, and invite a switch.** Over time this shows what works for this user.
4. **Aim for one time-boxed block, not a finished task.** Success means the user starts and does something, even badly.
5. **Learn from each session** if the user has agreed to logging.

Success: the user starts within about 15 minutes and completes at least one block. Failure: the rescue itself becomes a new way to procrastinate.

## 3. Design principles (shape the method; do not lecture the user)

- **Procrastination is mostly about managing emotions, not laziness.** Avoiding the task brings relief, and that relief reinforces the avoidance. Naming the feeling weakens it. Appeals to willpower usually fail.
- **Action comes before motivation.** Short actions of 5 to 15 minutes can lift mood quickly.
- **Self-compassion works better than self-criticism.** Criticism adds shame, and shame leads to more avoidance.
- **If-then plans work because they are specific.** "If [cue], then [action] at [place]" beats a vague intention.
- **When motivation is low, make the step easier.** Shrink the first action to about 30 seconds, and acknowledge it right after.
- **Thought distancing helps with heavy tasks.** "I'm having the thought that X" creates some space from the thought.
- **Match the task to the energy level.** A depleted brain should not draft careful writing. It can gather material, sort files, or tidy.
- **Physical levers, from strongest:** bright light, a few minutes of movement, and water are well supported. Cold water on the face helps a little. Avoid caffeine late in the day, because it harms sleep.
- **Feed-scrolling leaves a slump** that makes a dreaded task feel worse. Put physical distance between the user and the device before restarting. Do not try to resist the device while it is still in hand.
- **Bureaucratic and compliance tasks are their own category.** Official forms, legal filings, and applications carry learning costs, rule-following costs, and emotional costs. Do not apply ordinary project-work shortcuts to them.
- **Strong avoidance often signals that the work matters.** This reframe helps only when the user is calm and reflective, not when they are overwhelmed.
- **Harsh, drill-sergeant motivation has weak support for depleted people** and tends to add shame. Use it only when the user explicitly asks for it.

## 4. Hard rules

- **Diagnose every time.** No shortcuts.
- **Physical comes first.** If the user is very tired, do a physical reset before any thinking work.
- **No harsh style on a depleted user.** Use it only if all of these are true: the user is physically capable, the task matches their values, they are simply indulging in avoidance, and they asked for this style today.
- **Say the style each session** and invite a switch if it is not landing.
- **Cap the rescue at about 15 minutes.** If you are still diagnosing by then, the user either starts badly or stops. The rescue is not the work.
- **Honor break requests, but bound them.** A state-change break defaults to 5 minutes and can extend to 10, no further. The structured outing in section 7A has its own cap.
- **Watch for capacity problems.** If high tiredness and high dread keep recurring across many sessions, switch to the capacity branch instead of the usual rescue.
- **Offer to shrink the task directly.** If you have connected tools and authorized access to relevant material, offer to gather it (see Optional extras).
- **Do not narrate.** No "great, now let's...", no emoji, no recap of what you just did.

## 5. Diagnose (2 minutes or less)

Send one message with three short questions and no preamble:

1. **The task, in one line.** Skip this if the user already gave it.
2. **State, 0-10 each:** tired / dreading the content / unclear next step / pull toward distraction. High numbers mean more of the problem.
3. **Time available** before the next commitment.

If the user keeps a session log and has agreed to its use, review the last few entries quietly. In a plain chat, the user can paste them in. Note which styles landed, which missed, and any recurring problem. Do not quote the log back; let it inform section 6.

### Find the dominant problem

- The highest single score is the dominant problem.
- If two or more scores are 5 or above (adjustable), treat it as a **compound state**. This is common.
- If tiredness and dread are both high (default: 7 or above) across several recent sessions (default: 5), raise a **capacity flag** and go to the capacity branch.

### Capacity branch (a capacity problem, not a motivation problem)

Do not run the rescue. Say directly:

> "Tiredness and dread have been high for several sessions in a row. This looks like a capacity problem, not a motivation problem. What's the case for not doing this task today? Who else could take it? What would a 48-hour delay cost? What would actually help you recover?"

Stay with that conversation. Do not let it drift back to "fine, just one block." If the pattern looks like ongoing exhaustion or low mood, gently suggest talking to someone they trust or to a health professional.

If the user still insists on doing the task, go ahead, and say plainly: "We're working against the warning signs. Noted."

## 6. Pick and name a style (30 seconds)

Choose one style based on the diagnosis and any log history. Say it out loud:

> "I'll be [direct / analytical / empathetic / practical-warm] for this one. Tell me to switch if it's not landing."

Default mapping. Override it if the log shows a style has reliably worked or failed for this user.

| Dominant state | Default style | Why |
|---|---|---|
| High dread, low tiredness | Empathetic or analytical | Naming the emotion weakens it; analysis suits a calm user |
| High unclear, low dread | Analytical | Paralysis here is a breakdown problem |
| High distraction, low dread | Direct | Break the reward loop, briefly |
| Tiredness dominant | Practical-warm | A depleted brain needs warmth and brevity |
| Compound (two or more high) | Practical-warm | Warm but without waffle |
| User explicitly asked for harsh | Direct, then demanding | Rare, opt-in only |

**Signals to switch mid-session:**

- "Just tell me what to do" or impatience: switch to direct.
- "This is making me feel worse" or silence: switch to empathetic.
- The user argues with the framing: switch to analytical and let them reason their way in.

## 7. Intervene (physical, then emotional, then cognitive)

Do not skip ahead. Physical always comes first when tiredness is high.

### A. Physical reset (default trigger: tired 6 or more, or dread 7 or more)

This step is not optional when triggered. Moving the body often shifts emotional state too. Send one crisp message:

- Drink one glass of water now.
- Move: a walk outside if possible, otherwise stairs or brisk steps. No phone.
- Get light from a window or outdoors. No phone, not even for music.
- Optional: cold water on the face.
- No caffeine late in the day. A small snack or a decaf drink is fine; the ritual and the blood sugar are what matter.

**Caps (adjustable):**

- **Unstructured break:** about 10 minutes (water, walk, back).
- **Structured outing:** up to about 20 minutes. It is a round trip to a named place, with a small reward and a clear return cue. The user states the plan before leaving, and you hold them to it.

If the user proposes a break that fits these bounds, agree and set the limit.

### B. Emotional (default trigger: dread 5 or more, or shame shows up)

Pick one of these, not all of them:

- **Self-compassion break** (about 45 seconds, said aloud): "This is a hard moment. / Struggle is part of being human. / May I be kind to myself right now."
- **Thought distancing:** put "I'm having the thought that..." in front of the worry.
- **Values anchor** (about 20 seconds): "This task matters because [the user's own goal or value]. Doing it is an act of that value, even when it feels like a slog."
- **Avoidance-as-signal reframe**, only for a calm, reflective user: "How strongly you're avoiding this shows how much it matters. You're not weak; you're at the edge of something important."

**Shame signals:** "I'm such an idiot", "I can't even do this one thing", a long silence after a directive, or self-deprecating jokes. When you see one, switch to self-compassion right away. Never push harder on a shame-flooded user.

### C. Cognitive (once physical and emotional are handled)

- **Turn abstract goals into mechanical steps.** "Compile evidence" becomes "collect sources". "Respond to the official request" becomes "open the request and read section 1". Use mechanical verbs only.
- **Shrink the first step** to its 30-second version: the very first click, not the whole task.
- **Make an if-then plan.** Require the format "If [cue], then [action] at [place]" and have the user say it once.
- **Box the time, not the outcome.** Default 25 minutes, or 15 if the user is very tired. When the timer ends, the user stops. No "almost done" extensions; open-ended tasks have no "almost".

## 8. Start the block

- State the timer length out loud.
- Confirm the environment: phone in another room, only the tab or tool the task needs, everything else closed, and a site blocker on if the user uses one.
- Then stay silent. Do not chat during the block. The user working matters more than the user talking to you.

## 9. End-of-block check (30 seconds)

When the user returns:

- Ask for one sentence on what came out of the block.
- Ask them to re-rate tiredness and dread, 0-10.
- Ask only one question: "Another block, or stop?" Never ask how many more.

**If stopping:** acknowledge the effort out loud. The acknowledgement helps build the habit; it is not a platitude. For example: "You showed up when you didn't want to. That counts." Then stop.

**If continuing:** repeat section 8 with the same setup. Re-diagnose only if the user's state has clearly changed.

## 10. Log the session (with consent)

On first use, ask whether the user wants sessions logged and where to keep the log (a note, a document, or their chosen system). If they say no, skip this step. If yes, add an entry after each session in a stable format, using an unambiguous day-month date:

```
## D MMM YYYY HH:MM - <task in 3-5 words>

- State start: tired <N>, dread <N>, unclear <N>, distraction <N>
- Dominant problem: <tired / dread / unclear / distraction / compound / capacity>
- Style: <direct / analytical / empathetic / practical-warm / demanding>
- Interventions: <physical-reset / self-compassion / distancing / values / reframe / shrink / if-then / parallel-gather>
- Blocks: <N blocks of M min>
- Outcome: <started yes/no; state end tired/dread>
- What worked: <one line>
- What didn't: <one line>
- Style verdict: <landed / missed - try X next time>
- Notable: <optional one line>
```

In a plain chat, write the entry at the end so the user can copy it into their log.

## 11. Refine the method (only when a pattern appears)

Review recent log entries for patterns. Depending on the user's preference, either suggest a change or update the user's personal notes for this method.

Refine when:

- A style has failed in several recent sessions (default: 3): demote it in the mapping.
- An intervention keeps landing: make it the default for that state.
- A new state or combination appears that the method does not cover: add a branch or row.
- A rule was broken and it worked (for example, a demanding style helped a tired user who asked for it): record it as a narrow exception. Do not generalize it.
- The user pushed back on a prompt: rewrite that prompt.

If the session went smoothly, change nothing. Do not invent improvements.

## 12. Example session (fictional)

Jordan, a volunteer coordinator at the fictional Harbor Lane Food Co-op, needs to finish a quarterly report. Scores: tired 7, dread 6, unclear 5, distraction 3; 90 minutes free.

- **Diagnosis:** compound state, tiredness dominant.
- **Style:** "I'll be practical-warm for this one. Tell me to switch if it's not landing."
- **Physical:** water, a 10-minute walk around the block, phone left on the desk.
- **Emotional:** values anchor: "This report keeps the pantry funded."
- **Cognitive:** first step shrunk to "open last quarter's report and copy its headings into a new file." If-then: "If I'm back from the walk, then I open last quarter's report at my desk." Block: 15 minutes, because tiredness is high.
- **Check:** "Headings done and two numbers filled in." Tired 5, dread 3. Jordan chooses one more block.

## 13. Related workflows and style notes

- **Planning:** if the user gets stuck while planning, run this first, then resume planning.
- **Evening wind-down:** do not run this inside a wind-down routine. Wind-down is about leaving work, not starting it.
- **Problem-solving:** if the user is stuck because the problem itself is unclear, not because of motivation, use a problem-solving workflow instead.

Style:

- Crisp beats warm waffle. Empathetic does not mean long.
- Name an emotion once; do not circle back to it.
- Mention research only if it helps the user act.
- If a requested break is reasonable, say yes and set its limit.
- No emoji and no end-of-turn summaries. Confirm the next action and stop talking.

## Optional extras

**Parallel gathering with connected tools.** Many dreaded tasks draw on source material: messages, meeting notes, documents, or records. If you can search these, offer it without waiting to be asked: search while the user works and paste raw findings into a scratch document. This removes the blank-page problem and often cuts dread sharply.

Do this only for a legitimate task purpose and with the user's clear authorization to access those sources. Use the minimum sources and information the task needs, leave out unrelated or sensitive personal details about other people, and keep the output in the user's private workspace.

**Automatic log handling.** If you have file access, read the last few log entries silently at the start of each session and append the new entry at the end without showing it, so the user can review it later if curious.

**Distraction tools.** If the user has a site or app blocker, include switching it on as part of the environment check in section 8.


---
name: wind-down-for-sleep
description: Guides a short evening routine that lowers stimulation, prepares the body and morning, and handles sleepless nights. Use when someone says "wind down", "ready for bed", or "can't sleep".
---

# Wind down for sleep

This interactive evening workflow moves the user from the awake part of the day to sleep by lowering stimulation, adding reliability, and preparing the body. It runs last in the evening, after any day review and next-day planning, and does neither of those itself.

## Quick version

- Say "wind down" when you are ready to start.
- Put your phone or other distracting device out of reach first, ideally in another room or a timed box. Set it to come back only when tomorrow morning needs it, based on your first real commitment.
- Change into sleep clothes, do two or three small tasks for the morning, then a few minutes of a calming practice you already know.
- If a worry or task comes up, write one line on paper for tomorrow and leave it.
- Do not plan tomorrow or reflect on today during this ritual.
- If you are still awake after what feels like about 20 minutes in bed, get up, do something dull in dim light, and return when sleepy.

## 1. Purpose and evening order

Recommended evening order: **day review, then next-day planning, then wind-down.** Reflection belongs to the earlier day-review practice and tomorrow belongs to the earlier planning practice. This workflow comes last.

Target length for the active ritual: about 20 to 30 minutes. Longer rituals tend to get skipped.

It targets late stimulation (scrolling, lying awake), worry about tomorrow (mostly handled by the earlier review and specific planning), an inconsistent routine, and distraction controls that are easy to bypass. Physical barriers usually beat software limits on the same device.

Success signal: the user wakes rested, starts the morning without scrolling, and the device stays out of reach until the access time set from tomorrow's commitments. Every step must reduce stimulation, add reliability, or prepare the body; remove any step that does none of these. Re-read this purpose every run.

Design anchors, never explained at bedtime: a specific to-do list written earlier has been linked to falling asleep faster, which is why planning runs before this workflow rather than inside it; scheduled worry time earlier in the evening reduces bedtime anxiety; dim, warm light helps sleep onset; and consistency matters more than contents.

## 2. Standalone mode

You do not need daily records, a calendar, or any other workflow to use this. Tell the assistant tonight's bedtime and your first fixed commitment tomorrow morning, if any, then run Steps 1 to 4 from that alone, and skip Step 0. Use paper as the capture spot.

Chatting with an assistant on a bright screen works against winding down. Use voice if you can, or send one short message per step, with the screen dimmed and warm.

## 3. Settings the user chooses

Agree on these once. Reuse them every night until the user changes them. Offer the starting points only as adjustable suggestions, and do not assume values the user has not chosen.

| Setting | What to decide | Suggested starting point |
|---|---|---|
| Target sleep time | When the user wants to be asleep | Based on their natural sleep window and wake time |
| Ritual start | When wind-down usually begins | 60 to 90 minutes before target sleep time |
| Review cutoff | When a missed review is skipped | When a review would push sleep back |
| Distraction barrier | How the device goes out of reach | A timed box or another room |
| Default access time | When the device comes back if nothing early is booked | After the first part of the morning routine |
| Commitment cutoff | How early a commitment must be to move access earlier | Shortly after the default access time plus the commitment buffer |
| Commitment buffer | Time before a commitment to get ready and arrange transport | 45 to 60 minutes |
| Travel buffer | Time before a travel or commute block, which already marks departure | 15 to 20 minutes |
| Gate items | The few changes that signal night | A clothing change plus the distraction barrier |
| Allowed device | The one low-stimulation device, if any, after the gate | None |
| Physical prep and settling practice | Small morning-setup tasks, then a short familiar practice | Water, teeth, breakfast; a few minutes of slow breathing |
| Capture spot | Where stray tasks go for tomorrow | A notes field on tomorrow's record, or paper |

If the user names an earlier bedtime for tonight, work backwards from it. Protect time for physical prep and the settling practice. Do not let planning expand into the remaining window.

## 4. Triggers

- **Full ritual:** "wind down", "ready for bed", "going to bed", "time for bed", "help me get to sleep", or similar.
- **Can't-sleep fallback only:** "can't sleep", "still up", "still awake", or similar, after the ritual already ran tonight. Skip every other step and go straight to Step 6.

## 5. Hard rules

- **Gate first.** Do not continue past Step 1 until the user confirms it.
- **Keep the gate minimal.** Include only the gate items the user chose. If the user removes an item, do not add it back later.
- **No distracting-device step after Step 1.** Everything afterward must work offline or with the one allowed device.
- **Never ask about tomorrow, and do not reopen reflection or planning.** No outcomes, intentions, wins, or backup one-line plan. If planning was skipped, note it silently and continue. Planning questions raise alertness at the moment the goal is to lower it. Do not open a second writing session; any journal writing belongs to the review, before its questions.
- **Deflect tomorrow-concerns.** Say: "Put a short note in your capture spot. The review will handle it tomorrow. Not tonight."
- **No summary at the end.** Send the close and stop.
- **Stay silent after the close.** If the user says good night, reply with nothing or only "Good night." Never send a follow-up, a placeholder, or a simulated user turn. An unexpected message after bedtime can wake someone up.

## 6. Step 0: Readiness check

Gather only what is needed to confirm the earlier practices ran and to set the access time. Do not open inboxes, news, or feeds.

If the review and planning ran earlier in the same session, skip all lookups. That state and tomorrow's calendars are already known, so reuse them. Check the current time and continue.

If this workflow runs on its own, gather the following in one batch:

1. Current time, today's date, and tomorrow's date.
2. Whether today's review is complete.
3. Whether tomorrow's plan exists.
4. Tomorrow's morning events (midnight to midday) from every calendar the user approved. Include personal as well as work calendars, since social plans and early activities move the access time too.

| Review complete? | Time | Action |
|---|---|---|
| Yes | Any | Say "Day reviewed. Starting wind-down." Go to Step 1. |
| No | Before review cutoff | Say "The day review didn't run. Do it now (about 10 minutes)?" If yes, run it and return. If no, go to Step 1. |
| No | At or after cutoff | Say "Too late to review tonight. We'll pick it up tomorrow." Go to Step 1. |

If tomorrow's plan is missing, do not mention it, offer planning, or ask a fallback question.

## 7. Checklist format (Steps 1 and 2)

Use plain bullet lists, not checkboxes. Many interfaces cannot tick boxes, and "tick each one" wording confuses people. Send the whole list in one message and end with "Reply 'done' when all set." Expect one reply. Do not send items one at a time, because that adds turns at bedtime.

## 8. Step 1: Environment and distraction gate

Set the access time from tomorrow's calendars every night. There is no fixed time; the device comes back only when the morning needs it.

1. **Use every approved calendar** for tomorrow morning. If the evening's planning already read them, reuse those results as they stood after any blocks planning moved. Never set the time from the work calendar alone. If a source failed, say so once and use what the user has mentioned.
2. **Convert every event time to local time** from its returned zone or offset before comparing. An event that looks late may actually be early.
3. **Find the commitments.** A commitment is a timed event that fixes when the user must be somewhere or with someone: meetings and calls with other attendees the user has not declined, in-person plans, appointments, fixed-time exercise, and travel or commute blocks. These do not count: all-day events, declined or canceled events, sleep blocks, routine blocks, solo work and focus blocks, meals, and out-of-office placeholders.
4. **Take the earliest of:** each commitment's start minus the commitment buffer, and each travel block's start minus the travel buffer.
5. **If no commitment falls before the commitment cutoff,** use the default access time.
6. **If the result is before the user's usual wake time,** keep it and flag it as an early start.
7. **Put the access time, the reason (event and which calendar), and the countdown from now** on the checklist line.

```
Before we start:
- [Clothing change, e.g. day clothes off, sleep clothes on]
- [Distraction barrier], timer [duration] (access at [time], [reason, e.g. "for the early call (work)", or "nothing before the cutoff"])

Reply "done" when all set.
```

If the user delays an item ("I'll do the phone in a sec"), say once: "Do it now. These are the biggest levers. I'll wait." Then wait.

## 9. Step 2: Physical prep (about 5 minutes)

List the user's chosen tasks, grouped by location so they move around less.

```
- [Kitchen task, e.g. fill water bottle for the morning]
- [Bathroom task, e.g. brush teeth]
- [Hallway task, e.g. put keys and bag by the door]

Reply "done" when all set.
```

If a small task surfaces ("library book is due, return it tomorrow"), do not solve it. Capture one line so it leaves the user's head:

- Append to tomorrow's capture spot. Read only that spot first, preserve existing text exactly, and never overwrite from an earlier cached value. Never write into a private journal or a review record.
- Then say: "Noted. Captured."

## 10. Step 3: Settling practice

One line naming the practice, for example: "Ten slow breaths." Give no instructions if the user already knows the practice. Never introduce something new at bedtime. Wait for "done" or similar. Add, remove, or restore this step whenever the user asks.

## 11. Step 4: Close

Say only, adapted to the user's setup:

> That's everything. Lights off and straight to bed.
>
> Talk tomorrow.

No recap and no "sweet dreams". This is the last message tonight. Move silently to the audit.

## 12. Step 5: Routine audit (silent)

After the close, review the run without sending anything. Do not ask a tired person to diagnose their own ritual. If the user approved direct edits, update the routine. Otherwise, save proposed changes for daytime review. Do not report what changed.

| Signal | Change |
|---|---|
| User misread a prompt or asked what it meant | Rewrite it in plainer words |
| User pushed back on a step | Simplify it, make it optional, or cut it |
| A lookup failed or found the wrong record | Fix the lookup rule |
| The user corrected the access time | Check which calendar, commitment rule, or time conversion was missed and fix that rule |
| An item is skipped without comment | Remove it |
| User stated a preference ("don't ask me X") | Add it as a hard rule |
| The barrier keeps being bypassed | Choose a stronger physical barrier with the user |
| The same worry keeps appearing at bedtime | Move its prevention into the earlier review or planning |

How to edit:

- Edit or merge an existing rule rather than adding a new paragraph. The routine should stay short enough to run quickly.
- Write rules as general principles. Do not add dated incident stories to the routine itself.
- If you want a history, keep a separate one-line-per-entry log of what happened and why a rule changed. Do not load that log during a normal run.
- If the run was clean, change nothing. Do not invent improvements.

If the user re-engages because they cannot sleep, go to Step 6.

## 13. Step 6: Can't-sleep fallback (stimulus control)

Use only when the user reports being awake after the ritual. Do not rerun the ritual or reopen planning. Say:

> Get up for a bit. Low light, something dull like a paper book or folding laundry, nothing on a screen and nothing to solve. Go back to bed once you feel sleepy, and leave the clock alone.

This keeps the bed linked with sleep rather than with lying awake. Do not extend the reply. If sleep trouble is frequent or severe, suggest professional support at a daytime moment, not at night.

## 14. Worked example (invented)

Alex says "wind down" with no records connected. Bedtime is an hour away and nothing is booked early tomorrow, so the phone comes back at Alex's default time after breakfast.

- Assistant: "Before we start: sleep clothes on, phone in the kitchen drawer until after breakfast (nothing early tomorrow). Reply 'done' when all set."
- Alex: "done"
- Assistant: "Fill a water glass, brush teeth, keys by the door. Reply 'done' when all set."
- Alex: "done. oh, need to call the dentist"
- Assistant: "Write it on the paper by your bed. Not tonight." Then: "Ten slow breaths."
- Alex: "done"
- Assistant: "That's everything. Lights off and straight to bed. Talk tomorrow."

## 15. Exhaustion rule

If the user is clearly exhausted, they may skip Step 2 or Step 3. Do not skip Step 1, because it is the load-bearing step, unless a health, safety, accessibility, or caregiving need makes it unsuitable.

## 16. Style

- Quiet and short. One question at a time. No preamble.
- No narration ("great, now let's...") and no emojis.
- No sleep science at runtime.
- If the user goes off-script with a work problem, deflect to the capture spot and tomorrow's review.
- Use the user's preferred date and time format, and keep it consistent across the run.

The best wind-down is quiet, repeatable, and boring enough to become an automatic signal that the day is over.

## Optional extras

### Connected records and calendars

If the workflow connects to a journal, day records, or calendars, use only sources the user has authorized, and only to confirm status and set the access time. Treat calendars as read-only, and keep what you see inside the session.

Lookup principles:

- **Request only the fields you need.** Use an explicit list of fields on every record read, and leave private journal text off that list. Never read, quote, reconstruct, or write into it.
- **Confirm the review from a completion signal.** Use the review's own save confirmation from this session, or a dedicated rating or done marker. A saved free-form entry without that signal does not mean the review finished.
- **Test presence, not truthiness.** A zero rating is a valid, completed rating.
- **Match dates loosely** and expect more than one record per day. Exact-match date filters can miss records that exist. Check each matching record instead of assuming a single one.
- **Query calendars in local time.** Give the morning window an explicit local offset, then still convert each returned event to local time before comparing.
- **Degrade quietly.** If a source fails, say so once, compute from what you have plus anything the user mentioned, and leave repair for daytime.

### Invented access-time example

Jordan's example settings, all adjustable: commitment buffer 60 minutes, travel buffer 20 minutes. Times below are relative to Jordan's usual wake time.

- Work calendar: a solo focus block starting half an hour before wake time (does not count) and a team call one hour after wake time (commitment, so access at wake time).
- Personal calendar: "Bus to the climbing gym" returned with a different zone offset, so it first looks like a mid-morning event. Converted to local time, it starts right at wake time. It is a travel block, so access 20 minutes before wake time.

The earliest result is 20 minutes before wake time, which is earlier than usual, so keep it and flag it. The checklist line reads: "Phone in the box, timer [hours until then] (access 20 minutes before your usual wake time, for the gym bus (personal), early start)."


---
name: plan-and-book-a-trip
description: Plans a trip around its purpose, compares complete door-to-door journeys, and books within clear limits. Use when someone says "find me flights", "plan my trip", or "book the train".
---

# Plan and book a trip

Understand what a trip is for before optimizing its transport. Then turn an agreed brief into a small set of priced, door-to-door options, and carry the chosen one through booking preparation or an authorized purchase.

## Quick version

- Ask why the traveler is going, who they will see, which dates are fixed, and how much flexibility they have, before looking at any fares.
- Ask for their standing preferences (seat, bags, cabin, stops, budget style) instead of assuming them.
- Compare two or three complete door-to-door options, including bags, seats, transfers, and any extra hotel night.
- Say clearly which prices are live, which are rough indications, and which are your estimates.
- Never buy, or say something is booked, without explicit permission and a provider confirmation.

## Core principles

- **Current instructions win.** Old receipts, past trips, and saved preferences are context, not permanent rules. Never turn one trip's dates, fares, or event plans into a lasting default.
- **Trip first, tickets second.** Saved preferences do not replace a conversation about what this trip is for.
- **You do the research and checking.** Gather facts yourself from authorized sources. Ask the traveler only about intentions, priorities, trade-offs, a missing fact, a login step, or an approval.
- **Compare complete journeys.** A cheap fare can hide an extra hotel night, a hard transfer, a lost day, or fees.
- **Label certainty honestly.** Separate live prices from indications and estimates, and verified facts from guesses.
- **Searching is not buying.** A request to find or compare travel does not authorize payment.

## Traveler profile

If your environment can save preferences, keep a short profile. Ask the traveler to fill in each line. People differ a lot here, so never assume an airline, cabin, seat, or rule is best for everyone. Record the date and whether each entry came from the traveler directly. Recheck status, benefits, and addresses before relying on them.

| Preference | Question to ask | Example answers (varied, not defaults) |
|---|---|---|
| Stops | Do you prefer fewer stops, lower price, or a mix? | "Cheapest with at most one stop"; "Direct if under a set extra cost" |
| Airlines or rail operators | Any you prefer or avoid? | "No preference"; "Collect points with one alliance" |
| Cabin or class | Which cabins should I always show? | "Economy only"; "Show the next cabin up for flights over a set length" |
| Seat | Seat type and how much a seat fee is worth to you? | "Aisle, pay small fees"; "Any seat, never pay" |
| Luggage | What will you bring? | "One checked bag"; "Backpack only" |
| Timing | Earliest and latest times you will travel? | "No departures before mid-morning"; "Red-eyes are fine" |
| Discount cards and memberships | Any rail cards, memberships, or status? | "Senior rail card"; "None" |
| Home base and free places to stay | Home airport or station, and friends or family to stay with? | "Nearest major airport"; "Can stay with a sibling in the capital" |
| Sleep pattern | Usual wake time and bedtime, with time zone? | Used only for jet-lag ranking |
| Budget style | Fixed ceiling, or "show me what each step up buys"? | "Under a set amount"; "Value for money, no hard cap" |

## 1. Understand the trip before searching transport

For a new trip, start with discovery. Do not search fares until the first trip questions are answered. For a continuing trip, reuse the agreed brief and ask what changed. If the traveler asks to skip discovery or wants one narrow check, do that.

### Gather relevant context

Read the conversation, the saved profile, and any invitations, agendas, or itineraries the traveler supplied. If the traveler has connected tools and has clearly authorized it, you may also read their calendar, email, messages, and shared documents for this trip, read-only unless they authorize more.

These sources often mention other people, such as companions, hosts, and organizers. Read them only for the legitimate purpose of planning this trip and with the traveler's clear authorization, searching narrowly by event, destination, organizer, and dates. Use the minimum relevant information, leave unrelated or sensitive details about anyone out of your notes and outputs, and keep findings within the traveler's private planning space; do not contact anyone without authorization.

Keep the traveler's addresses and identity details out of shareable summaries. Never store loyalty numbers, passport or identity numbers, payment details, or document copies in the profile; booking references go only in a private trip record. Saving lessons or preferences never adds permission to purchase, message others, or access accounts.

Look for why the trip is happening, event dates and venues, existing bookings, and nearby commitments. If a source is unavailable, say so; never imply you checked it.

Distinguish an explicit goal from your guess, an invitation from confirmed attendance, and a calendar entry from a hard constraint.

### Interview the traveler

Briefly say what you know, then ask one numbered block of four to six questions. Ask fewer when much is settled. Ground each question in what you found.

1. **Purpose and priorities:** Why go? What would make the trip good?
2. **People and places:** Who is coming or being visited? Which stops are essential or optional?
3. **Time in each place:** How many days at each stop? Any extra stopover wanted?
4. **Dates:** What fixes the earliest departure and latest return? If dates are flexible, what range is useful?
5. **Pace, work, and recovery:** Holiday, work, or both? Do they need to arrive rested for something?
6. **Practical context:** Where can they stay? What is already arranged? Any accessibility needs, spending limits, or reimbursement rules?

Skip questions the profile already answers. Confirm the requested outcome: research, booking preparation, or an authorized purchase.

### Agree the brief

Summarize the brief and let the traveler correct it. Clear answers count as agreement.

| Brief item | Content |
|---|---|
| Purpose and priorities | [What the trip is for and what matters most] |
| People and stops | [Companions, visits, essential and optional stops] |
| Time in each place | [Nights per stop] |
| Fixed dates | [Hard constraints] |
| Flexible ranges | [Useful date windows; mark provisional dates] |
| Work and recovery needs | [Workdays, arrive-rested needs] |
| Accommodation and local transport | [What exists, what is needed] |
| Open questions | [Unresolved choices] |
| Requested outcome | [Research / prepare booking / authorized purchase] |

Keep provisional dates visibly provisional through every later step.

## 2. Research current options

Keep searches tied to the brief. If transport would force a real change to the trip, go back to the traveler with that choice.

1. **Search current schedules and fares** across the useful date range. Aggregators and date grids are good for discovery. Then verify the chosen itinerary, operating carrier, fare type, and conditions with the carrier where possible. List every suitable departure on each date, not just the cheapest.
2. **Apply routing preferences.** If the preferred routing is not available, check nearby airports and ground links, explain the options, and ask before settling.
3. **Compare ticket shapes.** Compare a round trip with an open-jaw ticket (arriving in one city, leaving from another) when both fit. Include the ground travel each one needs.
4. **Check ground transport to the real destination.** Confirm the right station when names are ambiguous. Check timetable release dates, holiday service, and planned works. Do not invent a train or fare before it is published.
5. **Apply discount cards** to every eligible price. Check validity on the travel dates, time-of-day rules, and eligibility.
6. **Handle failures openly.** If a tool or provider fails, name it, give the error, say what is missing, and try a safe recovery. Disclose any change of source.

Label every price as a **live selected itinerary**, a **date-grid indication**, or an **estimate**. A "from" fare is not an available ticket. Record when each price was checked, and share only links you have verified.

### Compare the actual product

- **Cabins:** confirm the cabin on each segment. Extra-legroom economy seats are not a separate premium cabin. If a route lacks the cabin the traveler wants, say so instead of relabeling another product.
- **Overnight flights:** when sleep matters, check the actual aircraft's seat type. A cabin name alone does not tell you whether the seat is flat.
- **Mixed cabins:** consider a higher cabin on one leg and a lower one on the other.
- **Seats and bags:** include seat fees. A seat preference does not guarantee an assignment. Check the fare's bag allowance, size, and weight limits. A personal-item-only fare does not cover a carry-on or checked-bag need.
- **Rail classes:** confirm the named class and its conditions. When the traveler has a rule about stepping up a class, price both classes for each train and show the difference, plus any extra flexibility the higher class gives.

### Rank flight times for jet lag

For long-haul flights across several time zones, rank times by fit with the traveler's body clock, alongside price and cabin. This is general planning guidance, not medical advice.

1. Use the traveler's usual wake time and bedtime in their home time zone.
2. Estimate the body-clock low point at about two hours before usual wake time.
3. **Eastbound:** favor flights that allow sleep during the usual night and land near the body-clock low point. Then avoid bright early light at the destination for the first days and seek afternoon light.
4. **Westbound:** favor daytime flights that land in daylight with a short stretch to a normal local bedtime.
5. Add a simple pre-trip shift (moving sleep gradually toward the destination) and a light plan for the first days.

Example: a traveler flying five time zones west for a family visit might prefer a late-morning departure that lands mid-afternoon local time, rather than a late-evening flight that lands after their body thinks it is the middle of the night.

## 3. Compare complete journeys

Show two or three useful options with a recommendation. If only one route fits, say so.

- Show local departure and arrival times, airport or station codes, duration, and next-day arrivals.
- Show total cost, currency, fare type, cabin on each segment, seat fee, bag allowance, and change or refund limits.
- Compare basic and standard fares; a low headline price can lose once seats and bags are added.
- Keep currencies separate or label a conversion estimate.
- Build realistic buffers for security, immigration, bags, and cross-city travel. Use the provider's recommended arrival time.
- Distinguish a protected connection from separate tickets and say who bears the risk of a delay.

### Worked example (fictional)

A traveler is going from Riverton to Lakeport for a four-day conference, wants an aisle seat, and is bringing one checked bag. All carriers, prices, and places below are invented.

| Option | Route and times | Cabin and fare | Complete cost | Main benefit | Main drawback |
|---|---|---|---|---|---|
| A (recommended) | RVT to LKP direct, depart Tue late morning, arrive mid-afternoon | Economy, standard fare | 412 (fare 340, bag 45, aisle seat 27) | Arrives in time for the opening dinner; free changes | 74 more than B |
| B | RVT to LKP via Hillford, depart Tue early morning, arrive early afternoon | Economy, basic fare | 338 (fare 255, bag 55, seat 28) | Cheapest | Very early start; tight connection; no changes |
| C | Train to Lakeport, depart Mon afternoon, arrive late evening | Standard class, flexible ticket | 298 (ticket 168, extra hotel night 130) | Calm journey, can work on board | Adds a night away and a hotel |

Recommendation: A. The extra 74 over B buys a sensible start time, no tight connection, and a changeable ticket. Prices for A and B are live; the hotel cost in C is an estimate.

## 4. Present and book

Lead with the recommended dates and route. Show each cabin the traveler asked to see. Show ground transport separately. Include verified booking links, when prices were checked, anything unverified, and the decision needed.

Prepare a concrete, reviewable booking before asking for any approval that is needed. If the traveler already authorized this purchase, or a clear scope and budget, continue within it.

Before submitting, check against the agreed option:

- passenger name exactly as the form requires, using details the traveler supplied;
- dates, airports or stations, operating carrier, and routing;
- cabin or class and fare type on each segment;
- seat, luggage, total price, and terms.

Resolve any mismatch first. Never invent identity or payment details.

After purchase, confirm success from the provider's confirmation. Report the booked journey and total, and flag any unassigned seat or remaining transport. A selected fare or unfinished checkout is not a booking.

## 5. Learn from experience

If the traveler wants you to keep improving their profile, save clear lessons at a natural stopping point.

- **Lasting preferences:** update the profile entry, keep any qualifications, and replace old entries rather than piling up contradictions.
- **Workflow lessons:** fix a missed question or wasteful step.
- **Temporary information:** keep one-off fares, exceptions, and lucky deals in the trip record. Do not turn one cheap choice into a budget. If it is unclear whether a choice is for "this trip" or "from now on", ask.

## Readiness gates and common failures

Before moving on, confirm:

- **Before searching:** the brief is agreed, or the traveler skipped discovery.
- **Before recommending:** prices are labeled, each cabin is the real product, extras are included, and the full journey is costed.
- **Before purchase:** authorization covers this booking and every checkout detail matches.

Common failures:

- letting an early fare search decide the shape of the trip;
- treating extra-legroom economy as a premium cabin;
- ignoring seat, bag, transfer, or hotel costs;
- reporting a "from" fare or a waitlist as available;
- treating an old receipt as a current preference or price ceiling;
- saying a ticket is booked before seeing a confirmation.

## Optional extras

Use these only when the traveler asks or the trip clearly calls for them.

### Upgrades

- Compare three paths: buying the higher cabin outright, changing the ticket into it at the fare difference, and a separate upgrade offer.
- Separate a confirmed cabin from a waitlist. An empty seat on a seat map does not prove an upgrade will clear. If a better cabin really matters, recommend securing a confirmed option.
- Do not claim any moment is reliably cheapest for upgrades. Prices can rise and seats can sell out.
- Check that the fare type can be upgraded before buying it; basic fares often cannot.
- Compare cash with points using a stated value per point, and read the upgrade's own refund and change terms.
- For an existing booking, check personal offers only through an authorized session, and never submit anything outside authorization.

### Fare and upgrade monitoring

Never promise to watch prices between conversations unless a real scheduled mechanism exists. If the traveler chooses a monitoring service:

1. Confirm the trip appears in the service.
2. Set an alert, not an automatic purchase or bid.
3. Monitor the leg that matters most.
4. Leave automatic repricing off unless the traveler asks; it may charge fees or change fare rules.
5. If a trial or subscription starts, set a cancellation reminder before the first charge.

When an alert arrives, the traveler (or you, within explicit authorization) books through the provider after rechecking the details.


---
name: meeting-prep
description: Researches a meeting's context, asks what outcome you want, then builds a focused brief and agenda page. Use when you say prep my meeting with someone or before an important call.
---

# Prepare for a meeting

Use this workflow to prepare one consequential meeting, such as a client, partner, hiring, advisory, project, fundraising, or negotiation conversation. The deliverable is a finished preparation page wherever the user keeps notes, not a research summary in the chat.

## Quick version

- Paste in the invitation, recent relevant emails or notes, and any document the meeting is about. Say who else will be able to read the finished page.
- Ask for a short situation brief: who they are professionally, where things stand, why the meeting is happening now, and the live tensions. No goal or agenda yet.
- Have the assistant ask you a few multiple-choice questions about your goal, the failure mode to avoid, and any specific ask, plus a final anything-else question. Every option gets a label such as 1a or 2b so you can answer quickly.
- Only after you answer, have it draft the page: context, goal, a time-boxed agenda, and a short ranked list of the most important questions. Script spoken lines only if no other attendee will read the page; otherwise write a neutral shared agenda.
- Use a title that names the real purpose, such as pilot scope and pricing rather than catch-up.
- Before using it, check that every unfamiliar name is explained, shaky facts carry their source, the times add up, and nothing sensitive appears on a shared page.

## Step 1: Set up

The order is fixed:

1. Research, scoped to the meeting's purpose.
2. Post a situation brief.
3. Ask targeted questions and wait for answers.
4. Build the page from those answers.

Skipping the questions is the most common and most costly failure. Research cannot tell you what the user wants, what they can offer, what tone they want, or what to avoid. The agenda often changes after one round of questions. Asking costs one turn; skipping can produce a wrong agenda. Time pressure is not a reason to skip: the user decides whether to go in without a page.

Because this workflow reads private communications and records about other people, use them only for a legitimate purpose tied to this meeting and with clear authorization from the user and their organization. Use only the minimum relevant sources and information, summarize rather than copy, and omit unrelated or sensitive personal details. Keep the brief in the user's private session and the page within its intended audience.

Keep compensation, offer, funding, budget, and similar figures off any page a wider group can read. Refer to them without numbers, such as compensation discussion or above the typical amount.

Confirm anything missing. The defaults are suggestions the user can change.

| Input | What to establish | Suggested default |
|---|---|---|
| Meeting | Title, date, time zone, duration, attendees, format | The meeting the user names |
| Purpose | Invitation wording or best-supported reason the meeting exists | From the invitation |
| Destination and audience | Where the page goes and who can read it there | Ask; assume shared when in doubt |
| Sources | Which messages, notes, records, and public sources are authorized | Ask |
| Page style | Title format, length, number of ranked questions, whether to script | The defaults in Step 8 |

If several events match, confirm which one. In group meetings, research only decision-makers and people central to the topic. To prepare several meetings, run the workflow once per meeting.

## Step 2: Read the meeting record

Open the full event, not just the title. Capture date, time, time zone, duration, organizer, attendees with their organizations, location or link, description, linked files, and any reschedule notes. Confirm it is a real meeting rather than a placeholder block.

## Step 3: Gather context in proportion to the stakes

Research answers four questions and nothing more:

1. What professional role does each relevant attendee play in this meeting?
2. What is the working relationship history?
3. Why is this meeting happening now?
4. Which facts, decisions, and materials will shape the conversation?

A routine check-in may need only the invitation and last meeting's notes. A first meeting about a large decision needs more. Start with the most promising sources and stop once the questions are answered.

**Sources, roughly in order of value:**

- **Correspondence.** Direct exchanges with the attendee first, for commitments, tone, and recent context. If the reason for the meeting is still unclear, look for threads that mention them; these often reveal the introduction or process that triggered the meeting. Read the most recent relevant items in full.
- **Earlier meetings and notes.** Past meeting pages, project notes, and calendar history with the same people, to build the relationship arc. If meeting pages live in more than one place, such as general, private, and restricted hiring areas, check every place you are authorized to read.
- **Your organization's own records.** If the meeting concerns something the person submitted, such as an application, proposal, or request, read it. Search by both email and full name, since people often used a different address earlier. State in the brief what you found, or that you checked and found nothing.
- **Public professional information.** Current role, what their organization does, a few professional links, and recent work-related news that bears on the topic.

Three principles apply to everything you find:

- **Identity.** A name match is not an identity match. Before using an older record, check that its email, employer, or project fits the current attendee. If not, drop it or label it as possibly a different person.
- **Origin.** First contact sometimes happens in channels you cannot search. Prefer direct evidence of who initiated the meeting, such as a note that a colleague recommended them, over indirect signals. If the origin is unclear, say so.
- **Evidence quality.** Label any claim from one source, an old source, or a weak source with its source and date. State conflicts. Never build a question on an unlabeled shaky claim.

For hiring and assessment meetings, focus on role-relevant capabilities, role alignment, work samples and other diagnostic evidence, and whether the planned questions will distinguish relevant performance. Use the same criteria for every candidate in a process.

## Step 4: Read the artifact the meeting is about

If a proposal, deck, draft, memo, plan, application, or contract is the reason for the call, read all of it, including every tab and appendix. Signals include feedback requests, draft or deck subject lines, comment notifications, phrases like I shared the proposal or I applied, and linked files in the invitation.

Extract the ask, key assumptions and evidence, decisions requested, risks, deadlines, alternatives, and the points where the user could challenge, support, or decide. For applications, the plan, stated alternatives, references, and weak points often give the sharpest questions. Generic questions look unprepared when a detailed plan exists. If the context implies an artifact you cannot find, ask the user for it in Step 7.

## Step 5: Check whether a specialized workflow applies

Some meetings need their own process, such as hiring reference calls, formal interviews, performance or compliance meetings, and incident reviews. A reference call is signaled when the attendee is introduced as someone who can speak to a candidate's work, the title says reference, or the attendee is a former manager or colleague of a current candidate.

If a specialized process exists, switch to it, carry forward the relevant research, and do not produce a generic page. A reference process typically confirms consent, uses a standard question list with role-specific probes, cross-checks themes from earlier referees, and separates direct observation from hearsay.

## Step 6: Post a situation brief

After research, post a brief the user can read in about a minute to reload the situation. Do not propose a goal or agenda yet; proposing first anchors the user before they say what they want. Pick the shape that fits and write it:

- **Narrative (default).** Short headed sections: who they are, where things stand, why now, and the live tensions.
- **Decision-shaped.** For negotiations, closes, or recruiting with a competing option: the ask, their alternatives and deadlines, your position, risks, and open unknowns.
- **Stacked.** A short narrative, then a decision section.

Run the reference check (Step 9) first. Never replace the brief with a one-line recap.

Invented example:

```markdown
**Who:** Priya Okonkwo, operations lead at Brightfield Logistics (fictional), first meeting.
**Where things stand:** She asked for pricing after a demo her colleague attended last month.
**Why now:** Her team's budget decision is due at quarter end (per her email).
**Live tension:** She wants a small pilot; our standard offer starts larger.
```

## Step 7: Ask targeted questions

Ask about targets, shape, and failure modes, never what the agenda should be; turning answers into an agenda is your job. Cover the goal, at least one other axis, and always a final catch-all.

| Axis | What it settles |
|---|---|
| Primary goal | Recruit, advise, build the relationship, decide, gather information, sell, close, or hand off |
| Their situation | Ambiguity in the research, such as whether they are still in a role or already committed |
| Sensitive substance | Whether the user shares an honest view early or hears theirs first |
| Failure mode | Overselling, underselling, the wrong topic, or no close |
| Specific ask | Introduction, money, time, advice, or commitment, and how direct to be |
| Authority | Whether the user can decide or offer something during the meeting |
| Anything else (always) | Context, history, constraints, or points to land or avoid |

Rules:

- Give each question a few mutually exclusive options, the most likely first and marked recommended. Offer real alternatives; a less obvious pick often flips the agenda.
- When two answers can sensibly combine, such as a date and a named deliverable, offer the combination as its own option.
- Ask only questions that shape the agenda. If you need several rounds, put questions whose answers change other options first, tailor later rounds, and put the catch-all last.
- Number questions continuously across rounds and label every option with question number plus letter.

```markdown
1. What is the primary outcome?
   - **1a (recommended):** Understand their interest and secure a concrete next step
   - **1b:** Build the relationship only
   - **1c:** Make a direct pitch

2. How direct should the close be?
   - **2a (recommended):** Propose a dated follow-up with a named deliverable
   - **2b:** Offer help and let them choose
   - **2c:** Make no ask

3. Anything else to land or avoid?
   - **3a (recommended):** Nothing to add
   - **3b:** I'll add notes

Reply with the labels, e.g. 1b, 2a, 3a.
```

Before sending, check that every question is numbered, every option has one unique label in sequence, and the catch-all is present. The only reason to skip this step is a recurring meeting with a fixed, documented purpose and no open decision. When unsure, ask.

## Step 8: Build the page

Confirm you have the user's answers; if not, go back. Then decide where the page lives. If other attendees can read the default location, store it somewhere private to the user. Use the private structure only when no other attendee will read the page; otherwise use the shared agenda.

**Title.** Use the user's format if they have one. A reasonable default: date, person's name, and a few words naming the real purpose, such as April 9, 2031 Priya Okonkwo: pilot scope and pricing. Avoid catch-up or check-in.

**Fields.** Fill date, attendees, and other fields as the user's system expects, checked against their time zone. After saving, read the page back and confirm the title, date, location, and permissions are right.

### Private preparation page

Split time to fit the meeting: a short open, most time on diagnosis and discussion, and enough at the end to close.

```markdown
## Context
[Role, relationship arc, why the meeting is happening, key links. Note if first meeting.]

## Goal
[Goal confirmed by the user's answers]

## Agenda
### [Start to end]: Open and frame
**Say**

[Exact opening words]

**Private note**

[What to avoid in the open]

### [Start to end]: Diagnose [topic]
**Questions**

1. [Question]
2. [Question]

**Private note**

[What to press on and signals to listen for]

### [Start to end]: Pitch or pressure-test [topic]
**Say**

[Exact transition]

### [Start to end]: Close
**Question**

1. [Close asking for a date, deliverable, or next step]

**Private note**

[Backup close]

## Most important questions
1. [Most decision-relevant question]
2. [Question]
3. [Forcing close]
```

Writing rules:

- Make times add up to the meeting length and keep spoken lines visibly separate from private notes.
- A spoken block holds only the exact words to say, written in full. Put any private cue on its own clearly marked line so nothing meant as a reminder gets read aloud.
- The ranked questions are an in-call cheat sheet: one line each, ordered by importance, short enough to scan in seconds. For persuasive meetings, include one question on the gap between the other party's current and desired state and end with the forcing close.
- For recurring contacts, summarize the relationship arc, not just the last interaction. Add a timely note at the end if something recent is worth mentioning.

### Shared agenda page

Remove scripts, private notes, tactics, candid assessments, and sensitive figures. Write in neutral or we voice.

```markdown
## Purpose
[Shared purpose]

## Agenda
### [Start to end]: Align on purpose
- [Topic]

### [Start to end]: [Main topic]
- [Question or decision]

### [Start to end]: Next steps
- [Owner, deliverable, timing]

## Decisions to leave with
1. [Decision]
```

## Step 9: Reference check

The user reads the brief and page cold, so everything you found is new to them. Run this before the brief and again before the page.

1. List every proper noun and ask whether the user would know it without your research.
2. Give researched names a short explanation where they appear, such as her co-founder, now at another company. Names the user supplied or clearly knows need none.
3. Make each section stand alone, or reword questions so they need no name.
4. Cut names that do not help a question or decision.
5. Keep source and date labels on shaky facts.

## Step 10: Audit and handoff

| Check | Pass condition |
|---|---|
| Questions | The brief was posted and the user's answers shaped the goal and agenda |
| Meeting | Date, time zone, attendees, duration, and destination are correct |
| Evidence | Claims are supported, labeled, or removed; identities confirmed |
| Coverage | Earlier meetings, relevant records, and the artifact were checked, or gaps are stated |
| Audience | Page sits where only the intended readers see it; shared pages have no script, tactics, or sensitive figures |
| Agenda | Times add up, questions are specific, and the close names a date, deliverable, or owner |

Finish by giving the page link and stating any limitations, such as a missing artifact, unconfirmed identity, or conflicting sources.

## Optional extras

**Post-call review.** For persuasive or high-stakes meetings, offer to schedule a review at a delay the user chooses after the meeting ends. Pass it the page location and counterparty's name so it can start without other context. It should record commitments, objections, and next steps with owners and dates and, if the user wants coaching, note recurring patterns in their own approach. Keep it as private as the preparation page.

**Tool-specific features.** If your notes system offers a meeting-notes or transcription feature, add it only with participant consent, and open the page wherever that feature works. If titles or fields support special elements such as date chips, use the form that actually renders; some systems store markup as literal text, so read the result back.

**Interfaces that drop text before a question prompt.** Some agent interfaces intermittently hide text posted just before a structured question in the same turn, especially after long research. If yours does, end the turn with the full brief and a fixed marker line, then ask the questions at the start of the next turn without repeating the brief. Retire the workaround only after a real research-heavy run shows it is fixed.

**Preparing a full day.** Run this workflow once per meeting, ideally in separate sessions, so each gets its own brief, questions, and page.


---
name: meeting-actions
description: Reviews meeting records, turns real unfinished commitments into clear tasks, and batches unclear ones as questions. Use when asking what you committed to today or for meeting follow-ups.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use it as a daily sweep, for a selected date or range, or for a set of meetings you paste in.

## Quick version

- Paste one meeting at a time: the transcript if you have it, plus your own notes and any automated summary. Say which attendee is you.
- Ask: "List only the concrete, unfinished things I agreed to do after this meeting. Quote the transcript line for each. Ignore anything done live, owned by someone else, or just discussed."
- Treat the transcript as stronger evidence than your notes, and your notes as stronger than an automated summary. Summaries often assign other people's to-dos to you.
- Have the assistant shape each meeting into 0 tasks, 1 combined follow-up, or separate tasks only when recipients or timing differ a lot.
- For each task, ask for a verb-led title, a due date with a reason, a time estimate, short notes that will make sense weeks later, and a ready-to-send draft if the action is a message.
- Ask it to save every unclear item for one batched list of questions at the end, each with two options.

## 1. Set the operating rules

The goal is not to turn every discussion into work. Each meeting should produce one of these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be done together for the same recipient or group on the same time horizon.
- **Multiple tasks** only when recipients, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful support, especially explicit action sections.
3. **Automated summary:** useful for orientation, not authoritative for ownership. Summaries also drop timing detail, such as turning "after her leave starts next week" into a vague "follow up later."
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often assign actions to the wrong attendee, especially in recurring one-to-ones, brainstorms, and meetings where others list their own to-dos. Never create a task only because a summary calls it an action item.

Track unfinished outcomes, not conversation. An idea, a statement of interest, or an open question is not a task unless someone accepted responsibility for a concrete outcome.

Apply responsibility boundaries supplied by the user or team, and always use the most recent version, because boundaries shift over time. Attending a meeting does not make the user responsible for every topic discussed. Skip a follow-up as someone else's only when it falls within work explicitly handed to them. Handing off one piece of an area (such as one stage of a process) does not hand off the whole area, so other follow-ups in that area may still belong to the user. When unsure whether an older boundary still applies, ask rather than skip.

This workflow reads records about other people, so use it only for a legitimate purpose with clear authorization to access those records. Use the minimum relevant sources and details, leave unrelated or sensitive personal information out of tasks and reusable guidance, and keep outputs within the access boundary of the chosen task system and its audience.

## 2. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as "yesterday," a date range, or a supplied meeting list. If no input is given, use this adjustable default:

- Before an early-morning cutoff in the user's local time, process the previous day.
- Otherwise, process the current day.

State the scope once, for example: "Scanning meetings for 23 Apr."

Check every place where the user's meeting records live, not just the main one. Many people keep a shared team meeting space, a separate private space for sensitive calls or internal one-to-ones, and sometimes a restricted space for a specific function, such as a hiring space that holds reference calls. When a new category of meeting moves to its own space, add that space to the sweep, or those meetings will silently drop out. Sources can differ in how they filter: one may already show only meetings the user attended, while another needs a direct query by date. Query each source for the selected scope, merge the results, and remove any meeting that appears in more than one.

For each meeting, collect:

- Title, date, and time.
- Record link or identifier.
- Attendees, only as needed to identify ownership.
- Transcript, notes, summary, and relevant linked context.

Report a compact count before processing, such as "7 meetings on 23 Apr." Do not infer actions from a title alone.

## 3. Fetch and inspect complete records

Fetch full records in parallel where the system supports batching. Do not search for existing tasks yet: first identify the people, topics, and candidate outcomes that make deduplication accurate.

For long transcripts, use a repeatable search, extraction, or chunking method rather than a truncated preview. Search for commitment language such as:

- "I'll ...", "Let me ...", "I can ..."
- "I'll send ...", "I'll follow up ...", "I'll introduce ..."
- A request followed by explicit acceptance.

Treat summary action items as candidates and verify each against the surrounding conversation. A promise may have been conditional, reassigned, fulfilled live, or made by another attendee.

If no transcript exists, lower confidence. Use notes or related messages only when they clearly identify the owner and outcome. Ask rather than guess when a wrong guess could create unwanted work or outreach.

## 4. Triage each meeting

Classify the meeting loosely. The type sets an expectation; evidence overrides it.

| Meeting type | Usual outcome | Guidance |
|---|---|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or an explicitly timed follow-up. Add a reconnect only for an explicit commitment with a stated timeline. |
| Information-gathering, interview, or reference call | 0 tasks | Create work only for an explicit out-of-meeting commitment. Synthesis is often already in the notes. |
| Internal planning or team meeting | 0 to 1 user-owned task | Capture the user's own deliverable, not the team's full action list. |
| Coaching or recurring one-to-one | 0 to 1 task | Usually handled live; task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1 to 2 tasks | Often separate an internal decision from an external response. |

For every meeting, identify:

- Relationship context: why the meeting happened, how many times you have met, who made the introduction.
- Candidate actions owned by the user.
- Work completed during the meeting.
- Work delegated to another named owner, checked against the current responsibility boundaries.
- Explicit future commitments and their timing.
- Enough neutral context for a task to stand alone weeks later.
- Source and related links the task audience may access.

Create no task when work was completed live, another person explicitly owns it, the meeting was purely informational and its synthesis is recorded, an active task covers it, or the statement was not a commitment. Users often pre-create tasks during a meeting, so expect some coverage already.

A test for live completion: if someone promised to send, create, paste, or share something and the artifact was actually delivered during the meeting, it is done. The initial promise in the transcript is not enough to create a task.

## 5. Decide the task shape

Combine actions into one task when they share recipient, time horizon, and outcome. Sending promised material, answering related questions, and offering meeting times can form one follow-up.

Split tasks when:

- Timing differs a lot, such as an immediate reply and a reconnect months later.
- Different recipients need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

**Readiness gate.** Do not create a task until it has:

- A clear owner.
- An unfinished, concrete outcome.
- Transcript or reliable-note evidence of ownership.
- A sensible scope and finish line.
- A due-date rationale.
- Enough context to stand alone.

## 6. Write the task

Use the user's chosen task system and field names. At minimum, capture:

- **Title:** short, verb-led, specific. A parenthetical hook helps later recall, such as "Follow up with partner lead (pilot scope)."
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user's scale. Default to important and time-sensitive; reserve the top level for a waiting recipient with a near deadline or a material risk.
- **Time estimate:** realistic minutes. As an adjustable guide: a few minutes for trivial sends, under an hour for a typical follow-up, longer for a decision plus several messages.
- **Notes:** context, action checklist, drafts, links.

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: the agreed date, or a reminder shortly before it.
- Weekly or sprint commitment: the next relevant review or planning session.
- Flexible work: roughly a week out, adjusted to workload.
- Older meetings processed late: move an immediate follow-up to the next workable date instead of a date already passed, unless the original deadline still applies.

Do not raise priority just because capture happened late. Raise it only for an external deadline, material risk, or an expected reply.

### Notes template

```markdown
[Two or three sentences of time-independent context. Include absolute dates,
why this matters, the commitment, and only necessary sensitivity.]

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

Use time-independent wording: "In the 12 May meeting," not "earlier today."

If the task is to send a message, write a ready-to-send draft rather than "email them." Follow the user's known writing preferences: greeting style by context (casual vs. formal or administrative), length, sign-off, phrases to avoid, and whether to include a scheduling link. Without preferences, draft a short, warm, professional message with a clear request or deliverable and no filler. For introductions, use double opt-in: ask each relevant party before connecting them.

### Worked example (fictional)

The user, from Northwind Collective, had a second call with Priya Nandakumar of Larkspur Labs about a pilot. The transcript shows the user saying, "I'll send the pilot outline and a couple of times to talk." The summary also lists "User to draft the budget," but the transcript shows Priya volunteering for that, so it is excluded.

```
Title:      Follow up with Priya Nandakumar (Larkspur pilot outline)
Due date:   14 Mar (next working day)
Status:     Open
Priority:   Important / Time-sensitive
Estimate:   20 minutes

Second call with Priya (Larkspur Labs) on 13 Mar about a three-month pilot.
The user promised the pilot outline and meeting times. Priya owns the budget
draft. No external deadline this week.

## Actions
- Send the message below with the outline attached

## Draft message
Subject: Pilot outline

Hi Priya,

Thanks for the time on our call. Attached is the pilot outline we discussed.
Would Tuesday or Thursday afternoon work for a short follow-up?

Best,
[Sender]

## Links
- Meeting record: <link>
- Pilot outline: <link>
```

Why this shape: one task because there is one recipient and one horizon; next-day due date; default priority since no deadline is pending; short estimate for one message; absolute dates; the misattributed item is left out.

## 7. Deduplicate before creation

Run one batched search of active tasks before creating anything. Search by meeting link or identifier, recipient name, distinctive topic terms, and proposed title.

A duplicate covers the same outcome, not just similar wording. Skip the new task, or update the existing one if the meeting adds a meaningful action, deadline, or context. Record each duplicate decision for the report.

## 8. Create confident tasks

Create high-confidence tasks in a batch when possible. Print one line per task with its due date. If the system can open created records directly, open them there rather than filling the update with links.

For every skipped meeting, give a one-sentence reason that names the actual cause:

- "No out-of-meeting commitment."
- "Completed during the call."
- "Reference call, synthesis already in the notes."
- "Explicitly handed to another role."
- "Already covered by an active task."

## 9. Batch uncertain questions

Skip this step when every decision is confident. Do not interrupt per ambiguity. Create confident tasks first, then ask all remaining questions together.

Typical uncertainties: unclear ownership in the transcript, overlap with an area that may or may not have been handed to someone else, dependence on something only the user knows ("did you already send this?"), an unusual commitment in an information-gathering call, or a person with several active tasks where it is unclear whether to append or create.

```markdown
**[Meeting title]**
Question: [One specific question]
Context: [One sentence grounded in the record]
Option A: [Task to create or update if true]
Option B: [Skip or alternate task shape]
```

Wait for answers. Then create or update the remaining tasks, rerunning the duplicate check if an answer changed the outcome.

## 10. Audit and report

Before finishing, verify that:

- Every meeting source for the scope, including private or restricted spaces, was checked and merged without duplicates.
- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries were unclear.
- Completed work was excluded, and delegation skips match current, explicitly named handoffs.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links to its source record where appropriate.
- Drafts are ready to send and match the user's preferences.
- Every uncertain item was asked or explicitly deferred.

Report tersely: meetings reviewed, tasks created or updated with due dates, skipped items with reasons, open questions, and any guidance changes. Keep it plain, with no decoration such as emojis.

## Optional extras

**Long-transcript helper.** If transcripts often exceed what the assistant can read at once, keep a small program that slices a saved record by section (such as the action items), scans for commitment phrases attributed to the user, searches by pattern, or returns the next window of text. Scanning for commitments directly beats trusting the summary's action list.

**Pattern guide.** Keep a user-maintained guide of recurring patterns organized by meeting type: common misattributions, reliable signs of live completion, type exceptions. After each run:

- Append a short, generalized note when a pattern will affect future triage. Do not rewrite old entries.
- Change the workflow itself only for cross-cutting principles, new defaults, or a new step, and ask before structural changes such as adding a step or changing the evidence order.
- Record a new responsibility boundary in the user's responsibility reference if it applies beyond one meeting. When a boundary changes, replace the outdated version and remove any examples or skip reasons that relied on it, so old handoffs do not keep suppressing tasks.
- Add any newly created meeting space to the list of sources in step 2.

Do not turn one-off facts about a person or meeting into permanent rules. Report any changes in one or two bullets.

**Scheduling.** Run the sweep once a day at a time the user chooses. The work typically scales with meeting count, so a heavy day takes longer.


---
name: message-to-task
description: Turns a message thread into researched, partly completed work and files or updates a task only when tracking helps. Use when someone says make this a task, track this, or deal with this message.
---

# Turn a message into a task

Use this workflow when one or more message links, copied conversations, or inbound requests may need follow-up. The goal is not to log a vague to-do but to complete as much useful work as is safe, then leave a small, clear human finish.

## Quick version

- Paste the whole conversation, including every later reply and any linked document, and check that the request is still live before doing anything else.
- Name the task shape: reply owed, artifact owed, decision needed, or follow-up. Then rewrite the request as an outcome with a clear finish line.
- Draft the actual deliverable (reply, document, decision brief, or chase message) instead of just describing it. Mark unverified facts as `[VERIFY: ...]` and gaps only you can fill as `[FILL IN: ...]`.
- Ask questions only if a wrong guess would cause real rework. Before asking, restate the full story in a paragraph or two so the choice is answerable.
- Decide whether you need a task record at all. A ready draft you can send in a few minutes needs none; deferred, multi-step, or deadline-bound work does. If you do need one, check whether a task for the same ask already exists and update it instead of adding a duplicate.
- Get the output with context first and the deliverable last, so the draft can be copied without cleanup.

This workflow is tool-independent. Use whatever messaging, document, task, calendar, and research capabilities you have. Run the full flow separately for each message reference unless several references clearly concern one shared outcome.

## 1. Open the message and read the complete conversation

For every supplied message reference:

1. Open the linked message or locate the quoted message.
2. If it is a reply in a thread, open the parent and read every reply.
3. If it is a top-level message, retrieve nearby conversation context. If the message has replies, read the full thread immediately, because replies often change or resolve the task.
4. Check whether replies after the linked message change the request, answer it, reassign it, or make it obsolete.
5. Open every substantive attachment, form, shared document, or cited source that could contain the real request.

Identify:

- The requester and all relevant participants, by name or clear role. Never write a task about "the person."
- The current ask, previous commitments, promises, deadlines, and dependencies.
- The current owner of each action.
- Whether work is already complete, withdrawn, delegated, or blocked.
- Whether several people have asked about the same topic elsewhere and could be served by one consistent answer.

If the work appears already done, do not file dead work. Tell the user what later context suggests and ask before creating a record if status remains unclear.

## 2. Classify the real work

State the task shape in working notes before researching, because the "do the work" step differs for each:

1. **Reply owed:** Someone needs an answer, feedback, a decision, or a confirmation. Deliverable: a drafted reply.
2. **Artifact owed:** The user owes a document, introduction, analysis, reference, briefing, or data extract. Deliverable: the artifact or a substantial draft.
3. **Decision needed:** The conversation ends at a choice only the user can make. Deliverable: a concise decision brief and, where useful, a draft reply for the likely choice.
4. **Follow-up or delegation:** The user needs to chase someone, schedule something, hand off work, or update a system. Deliverable: a drafted follow-up or a prepared internal action.

A message may contain several requests. Keep them in one task with sub-parts when they share an owner, deadline, and context. Split them only when different owners, timelines, or completion criteria make separate tracking clearer.

Rewrite the request as an outcome. For example, replace "Message about an event question" with "Send verified attendance figures and a next-step recommendation."

## 3. Gather targeted context

Research only what the task requires. Start with sources closest to the request, then expand only when needed.

Useful source types include:

- Earlier messages and topic searches for related commitments, decisions, or parallel requests. Search the topic, not just the person.
- Prior correspondence, meeting notes, and the user's own planning or talking-points notes about a relationship. A documented stance often answers questions you would otherwise ask, and it is the substance the draft should be built from.
- Project pages, event records, and operational correspondence for project facts. For past events, pre-event logistics messages are often the only written record of hard numbers such as counts, schedules, and process.
- Approved policies and established precedents for people-process, finance, or policy questions. When setting something up for the first time, start from the closest existing policy as the default anchor.
- Authoritative records or trusted public sources for quantitative questions.
- Every substantive linked document. Review all tabs, sections, pages, and appendices. The message often surfaces only one of a document's asks; the document is the real task list, and the message is just the knock on the door.

Because this workflow reads private communications and records about other people, use it only for a legitimate purpose with clear authorization from the user and, where relevant, the organization. Consult only the minimum relevant sources and information. Leave unrelated or sensitive personal details out of notes, drafts, and records, and keep all outputs within an appropriate access boundary.

For web research, follow whatever browsing policy the user has set. If automated browsing is allowed, run it without a visible window, and let any helper agents browse only under the same rules. Avoid tools that create other side effects unless the user has authorized them.

Stop gathering when you can either complete the preparation or name precisely what is missing. Two or three well-chosen sources beat many shallow ones.

## 4. Pre-complete the work safely

Do as much as is reasonable without taking irreversible external action.

- **Reply:** draft the full message in the user's voice.
- **Artifact:** create the outline, analysis, reference text, or document draft.
- **Decision:** prepare two or three viable options, the key evidence for each, and a recommendation with reasons. Give a recommendation, not a survey.
- **Follow-up:** draft the chase or handoff message and prepare any authorized internal update.

If a style guide or approved examples exist, read them in full before drafting in the user's voice. Drafts usually need to be shorter than first instinct suggests:

- Cut compliment-plus-scaffold openers and lead-in lines such as "Here's where I've landed."
- Ask one simple question when that is enough, rather than a structured checklist of everything you might need.
- Hedge future commitments explicitly (for example, "though I can't promise this yet").
- Include coaching or explanation only when coaching is the point of the reply.

Never invent facts, dates, amounts, names, links, or policy positions. Use explicit markers:

- `[VERIFY: confirm current figure in the reporting record]`
- `[FILL IN: first-hand observation or personal judgment needed]`
- `[SEARCH: locate the approved public link]`

Put gaps directly where they matter in the draft rather than dropping the section. A draft with two obvious blanks still saves the framing work, but warn the user that it cannot be sent as-is.

Do not send messages, email, invitations, applications, approvals, or other external communications. Drafts are the ceiling of autonomy. For approvals, payments, policy exceptions, and other governed actions, the draft should route the person through the organization's established process rather than offering an informal yes that bypasses controls.

List what you genuinely cannot do (judgment calls, sensitive relationship reads, anything needing the user's memory) as specific remaining steps, not "review and complete."

## 5. Ask questions only when truly blocked

Before asking, check whether the user's position is already documented in earlier messages, notes, decisions, or policies. A documented stance beats a fresh question.

Ask only when a wrong assumption would waste more of the user's time than the question itself, or would create risk or an inappropriate commitment. Ask two to four focused questions at most, before creating any record, so the answers land in the draft. Precede them with a one- or two-paragraph context recap that restores the full situation:

- who is involved and what has happened so far;
- what is now being requested;
- the real decision, trade-off, or tension;
- evidence already found; and
- the recommended default, if any.

Options without the story are unanswerable. Allow combined and custom answers, since the user may want two options at once or something else entirely. If no material fork remains, make reasonable choices, state them in the report, and let the user correct them.

## 6. Decide whether a task record is worthwhile

Skip the record when the remaining work is one short sitting with nothing to wait on, such as reviewing and sending a ready draft. A record for that would outlive the task. Provide the context and deliverable directly instead.

Create a record when one or more of these apply:

- Work is deferred or cannot be completed now.
- A deadline, dependency, or wait needs tracking.
- Several steps remain or work will span days.
- The user explicitly asked for a record.

When uncertain, prefer chat-only for a simple reply and a record for longer-lived work. Set the "short sitting" threshold to whatever the user finds natural (a default of about 15 minutes is a reasonable starting point).

## 7. Create or update a complete task record

First check for an existing record. Search the user's task system for a distinctive keyword, such as the requester's name or organization. If a record already covers the same ask, update it instead of creating a duplicate:

- Rewrite its notes from scratch rather than appending, because older notes go stale (for example, a line saying the thread had no replies when replies have since arrived).
- Move the due date and raise the priority if new deadlines or reminders have come in since it was filed.

Otherwise, create a new record in the user's chosen task system. Fill these fields where supported:

- **Title:** specific and action-led, short enough to scan.
- **Status:** the user's equivalent of not started.
- **Due date:** only when supported by an explicit or clearly implied deadline.
- **Priority:** best judgment from impact and time pressure. Someone waiting on the user generally raises urgency.
- **Estimate:** remaining human effort, not research already done. A pre-drafted reference to review and send is a short task, not a long one.
- **Area or project:** the best-fit category from the user's current list. Category lists get renamed and restructured over time, so re-check the live list rather than relying on a remembered one, and re-list the options if nothing seems to fit.
- **Notes:** a self-contained handoff:

```markdown
**What:** [One-sentence request and who is waiting.]
**Source:** [Original message or conversation link.]
**Context:**
- [Three to six bullets: who is involved, what led here, key facts with links.]

**Pre-completed:**
[Full draft reply, artifact, decision brief, or prepared action. State where any draft is staged.]

**Remaining for the user:**
- [Specific final action.]
```

Check how your task system renders formatted notes. Many systems flatten nested bullets and drop the indentation, so keep notes to a single bullet level and fold any sub-points into the parent line rather than indenting them.

Summarize rather than pasting an entire private conversation. After creating or updating the record, open or retrieve it to confirm the title, notes, links, deadline, and fields are correct.

## 8. Report back clearly

If a record was created or updated, report in this order, with nothing trailing after the last substantive block:

1. What the task is, and whether it is a new record or an update to an existing one.
2. What was pre-completed and where any draft is staged.
3. The chosen metadata in one line.
4. Any `[VERIFY]`, `[FILL IN]`, or other blockers.

If no record was created, separate briefing from deliverable and keep the deliverable last:

```markdown
## Context for the user (not part of the reply)
- [Ask, requester, key facts, judgment calls, staged-draft location, verification flags.]

## The reply
[Draft message verbatim.]
```

Nothing should appear after the draft reply.

**Invented example.** Tomas Reyke, a volunteer coordinator at the fictional Lanternfield Reading Trust, asks in a thread how many people attended last spring's workshop and whether the user would co-host the next one. A later reply shows a colleague already asked the same attendance question in another channel. The workflow classifies this as a reply owed, finds the headcount in the pre-event logistics email, drafts one answer and points the second asker to it, and marks the co-hosting question `[FILL IN: willing to co-host? dates that work]`. Because the user must decide on co-hosting and the next workshop has a date, a record is needed. A search turns up an older task titled "Reply to Lanternfield about workshop" whose notes say no one has replied yet, so the workflow rewrites those notes, sets the due date to the planning call, and raises the urgency. The metadata line reads: "Updated existing task: Important / Time-sensitive, due before the planning call, about 10 minutes remaining."

## 9. Learn from what the user actually sends

The user's final edits are the best evidence of their real voice and stance. After a draft has been used:

1. Re-read the conversation and find the message the user actually sent, or ask them to paste it.
2. Compare it with the draft: what was removed, reworded, reordered, added, or left unanswered.
3. Extract only general, reusable lessons, such as preferred brevity, wording, decision framing, formatting, or process routing (for example, "funding approvals go through the formal application").
4. If nothing has been sent yet, check again a limited number of times, then stop. The user may have deliberately chosen not to send it.

## 10. Improve the workflow carefully

After each run, review what helped and what caused avoidable work. Update the workflow only when authorized to maintain it, and keep changes small, general, and testable. Useful improvements include:

- adding a source type that reliably answered a class of requests;
- recording a tool limitation and its workaround;
- adding a genuinely distinct task shape;
- cutting or rewording an instruction that wasted time; or
- encoding a user correction as a general drafting or process rule.

Encode the lesson, not the specific example. Do not turn one unusual incident into a rigid rule. If nothing generalizable was learned, change nothing; no-op runs are normal once the workflow matures.

## 11. Final audit

Before finishing, check:

- Did I read later replies and confirm the work is still live?
- Did I identify the actual deliverable rather than merely log the message?
- Did I research enough, but not excessively, and within the user's browsing rules?
- Did I draft or prepare the useful work?
- Did I avoid sending, approving, or committing externally?
- Are unsupported facts and links clearly marked rather than guessed?
- If a record was needed, did I check for an existing one and update it instead of duplicating?
- If a record exists, does it have fresh notes, full context, verified fields, formatting that renders correctly, and specific remaining steps?
- Is the deliverable the final block of my report?

## Optional extras

These help when your assistant has connected tools.

- **Parsing message links.** Many messaging tools encode the conversation ID and a message timestamp in the link, plus a separate parent identifier when the message is a thread reply. Use the parent identifier to fetch the whole thread. Some tools return nothing for an exact-timestamp lookup, so query a small window around it instead.
- **Recovering identities.** If sender names come back blank, recover them from mentions in the text or by looking up the user ID.
- **Building an evidence base.** For references or feedback, searching for messages a person authored can surface concrete examples of their actual work.
- **Browsing policy.** If you keep a written browsing policy, point the workflow and any helper agents at it rather than restating rules in each prompt. A common default is to allow automated browsing only in headless mode, so research never takes over the user's screen.
- **Finding duplicates.** If your task system supports search, query the title and notes fields for the requester's name or organization before creating anything. Use the system's update operation on a match rather than deleting and recreating, so links and history are preserved.
- **Staging drafts.** If authorized, stage the reply as an unsent draft in the right thread so finishing is one click, and keep the same text in the task notes. Check rendering: many tools need a blank line between a paragraph and a list, or the list items show as plain text. Go straight from greeting to the first item rather than using a list lead-in line.
- **Scheduled review.** If the environment supports delayed reminders, schedule the step 9 check automatically. A default of about one hour is a reasonable start, adjusted for working hours and urgency. The reminder should name each staged draft, its conversation location, and where the draft text is stored, and allow a couple of follow-up checks at growing intervals before stopping.
- **Versioning the workflow.** If the workflow lives in a file under version control, commit each improvement with a short, dated message so changes are easy to review or revert.


---
name: inbox-zero
description: Works email, chat, and notification inboxes to zero, giving each item one bucket and a next step. Use when someone says triage my inbox, clear my messages, or help me prioritize email.
---

# Process an inbox to zero

Help someone empty one or more inboxes (email, team chat, document comments, messaging apps) into one trusted task list. Every item ends in exactly one bucket, and nothing that needs doing lives only in an inbox or an unsent draft. Processing means deciding what each item is and where it goes, not doing the work the items describe.

## Quick version

- Paste or export the messages you want to process, any unsent drafts, your current goals, and today's most important task (MIT). Ask the assistant to put each item in exactly one bucket: **do now** (urgent, important, short), **quick win** (a couple of minutes), **delegate**, **task**, or **no action**.
- Rank by consequence, not noise: hard deadline first, then someone blocked on you, then what serves a goal, then the relationship cost of waiting. New, unread, long, or loud does not make something urgent.
- For chats, judge everything since your last real reply, not just the last message. A "thanks!" on top of an earlier question still needs an answer. A chat you flagged to reply to is never no action unless you say so.
- Work one bucket at a time in small batches, and move on only after you have acted, not just decided.
- Anything longer than your work cap becomes a task with a name, due date, and first step. Do not start the work during the run.
- Finish with counts of what was cleared, tasked, delegated, and still open, including drafts left unsent.

## 1. Setup choices

Confirm these once, or use the defaults. All are adjustable. Store them as configuration, never with message content.

| Choice | Default (adjustable) | Notes |
|---|---|---|
| Work cap for do now | About 15 minutes | Longer work becomes a task |
| Quick win threshold | About 2 minutes | Short reply, yes or no, RSVP, forward |
| Batch sizes | Do now 1, others 3 to 5 | Big lists overwhelm; tiny batches feel slow |
| Chat lookback | About two weeks | Unread views may still show older chats |
| Sources | All the user names | Mark any feeds that count only when they mention the user, and any read only on request |
| Delegated actions | None | Named sources where the assistant may clear items after confirmation |
| Draft destination | Copy-ready text | Saved in-app drafts only where authorized |

## 2. Ground rules

1. **The user takes external actions.** Do not send, archive, delete, label, mark read, react, or mark complete unless the user has delegated that action for a named source. No bulk actions by default. When asked to archive cleared items, archive only what is finished or handed off; keep anything waiting on an unsent reply, and ask about FYIs they may still want to read.
2. **No drafts unless asked.** Never send, edit, or delete the user's existing drafts.
3. **One write by default:** when the user says "task it" about a specific item, create that one task. Never create tasks in bulk.
4. **Respect the work cap.** The real time sink on inbox days is doing the work a message describes, not replying to it.
5. **Evidence, not assumptions.** Say what the messages show. Never state the user's beliefs or decisions for them.

This workflow reads other people's messages, so use it only for a legitimate purpose: processing the user's own inbox, in sources they have clearly authorized. Read the minimum sources and information each decision needs, leave unrelated or sensitive personal details about others out of the output, and keep output inside the user's own session and task system.

## 3. Set scope, time, and goals

1. Get the date, weekday, and time from a reliable clock in the user's time zone. Never work them out mentally.
2. Map the user's words to configured sources ("email", "team chat", "comments", "chats" or a named network, "all"). If scope is unclear, default to all configured sources except request-only ones and say so in one line rather than asking. Naming a personal account counts as the request to read it, read-only.
3. Read each source's access rules before reading it. The task list is where items go, not an inbox; if the user wants to prioritize tasks, route to a planning workflow.

Then read, in parallel, only the fields you need from the user's planning system, never private fields such as journals:

- **Longer-term goals** for the current period, with deadlines and priority.
- **Weekly goals** covering today. If several records match, use the one with content.
- **Today:** intention, plan, and MIT.
- **Open tasks:** title, status, due date, so you can spot items already tasked.

If a query returns nothing where a record should exist, check the query before reporting a level as missing. If a level really is missing, say so in one line and continue; never invent goals. Summarize the goals in a few lines for yourself and judge every item against them.

**MIT check.** If today's MIT is not inbox work and the user is inside or near its planned block, ask once, before reading any inbox: "Is this the most important thing right now, or does it just feel productive?" Trust the answer.

## 4. Read the inboxes

Read every source in parallel. For each item collect: source, sender, subject or chat, date and sender of the last message, a one-line gist, and a link.

1. **Get everything from the right view.** Prefer purpose-built inbox, notification, or reply-debt views over general search, which misses saved, unread, and last-sender state. Page past result limits. A notification inbox is at zero only when every uncleared item, read or unread, is processed.
2. **Group to the decision unit.** Group email by thread. Several notes about one thing, such as comments on one document, are one decision.
3. **Open when the preview is not enough.** Skip obvious newsletters, receipts, and automated notices unless they point to a deadline, money or security issue, or a record that now needs the user. Otherwise open the full thread, and any attachment that carries the ask, before choosing a bucket. Never task an item you have not seen.
4. **Judge chats on everything unanswered, and honor the user's own flags.** Read back to the user's last real reply; a logistics exchange or friendly closer can sit on top of an older question. A chat with an unanswered question, or one the user marked to reply to, is never no action until the user says so. Unreads alone are attention debt, not priority.
5. **Rank direct above broadcast,** unless a group message names the user, asks them something, or carries a deadline. Old items with no open ask are usually stale; group them for one decision.
6. **Never invent links.** Copy links from tool output or use a format verified in this setup; otherwise cite sender, subject, and date.

*Example (fictional).* A chat with Robin from the Maple Street Rowing Club ends with the user's "Sounds good!" and Robin's "Great, see you there." Two messages earlier, Robin asked whether the user could host the spring meetup, and nobody answered. The chat is a quick win, not no action.

**Unsent drafts.** For every source in scope, also list unsent drafts, including text left in a messaging composer and drafts made earlier in this run. Each is an item in its own right, whatever its age. A draft listing is not always an open loop: stored templates, scheduled messages not yet due, and leftovers the app no longer shows are not loose replies. A template with no recipients may also keep appearing in a listing after the user deletes it. Mention these once as what they are, and if the user cannot find one, close it and do not ask again.

**Failures.** If a source fails or is disconnected, name it, the error, and the missing data. Try the safe repairs in its access rules, continue with the others, and never quietly drop a source or swap in a weaker one. Put failures at the top of the output.

## 5. Sort and rank

Put every item in exactly one bucket:

1. **Do now:** important, urgent, finishable within the cap. Aim for three to five; extras are probably tasks.
2. **Quick wins:** under the quick win threshold. The user batches these.
3. **Delegate:** someone else should own it. Name the suggested owner with brief evidence, checked against current information because roles change. If nothing is credible, say "owner unclear".
4. **Task:** work over the cap, or work that cannot happen yet. Suggest a name, any implied due date, and why. If an open task already covers it, say so and suggest clearing the inbox copy.
5. **No action:** FYIs, resolved threads, automated notices, chats that ended with nothing unanswered. Call it "no action", not "delete"; the user clears these.

Sort drafts the same way: a finished reply is a quick win (send it); one still being written is do now or a task; a stale one is a quick win to delete. A draft the user says is deliberate is listed as kept, not open.

Rank do now, and order every other bucket, by:

1. **Hard deadline or time-bound decision:** due today or tomorrow, an expiring offer, a meeting that needs a reply first.
2. **Someone blocked on the user,** applying any response-time standard they set.
3. **Ladders to a goal:** MIT, then weekly, then longer-term. Name the goal.
4. **Relationship cost of delay.** Age supports this, and channels differ: an unanswered email or direct chat a few days old usually matters more than an old saved item.

## 6. Open the run

Do not show the full sorted list. The opening message holds only:

```markdown
## Inbox zero: <date>, <sources>

**Missing data:** <failed or stale sources, or "none">
**Counts:** <N items: X do now, Y quick wins, Z delegate, T task, A no action>
**Unsent drafts:** <count by source, or "none">
```

Then go straight into the first non-empty batch in the same message.

## 7. Work the buckets, one batch at a time

Go in bucket order and stop whenever the user wants. Each message shows one batch, or one do-now item, and asks only about what is on screen. End the turn and wait. Answering questions is a decision, not completion: move on only when the user says the batch is done, and until then help them finish it.

**Formatting.** Link every item or person you name, including in recaps and question titles, and link any other conversation the user must visit. Number questions and letter options so the user can reply `1b, 2a`. Never show status by color alone.

**Group by person first.** When one person accounts for several items, show their pile once, split into "needs you", "discussion", and "reading or FYI", and suggest one way to batch it, such as one task or an existing one-to-one.

1. **Do now, one per message.** Read the full thread and check the calendar around any dates it mentions. Gather only the context this decision needs. Before saying the user still owes a reply or introduction, check replies inside threads and the other channels they use; it is often already done. For hiring or assessment items, use the user's chosen guidance and authorized evidence about role-relevant capabilities, role alignment, and whether an assessment distinguishes relevant performance. Write a short paragraph: who, what they want, what happens if it waits, and the recommended action, with evidence linked. Ask one to three questions only the user can answer.
2. **Quick wins.** Each item gets a link, a line saying what the thing is, and one recommended action. If a message refers to something you cannot explain, find it first rather than relaying the ask blind. When one item spans several conversations, say what each is waiting on. Say how many remain.
3. **Delegate.** Link, suggested owner, evidence. The user confirms or changes the owner.
4. **Task.** Link, suggested name, due date. Create each one the user says to task.
5. **No action.** Counts by type, naming only items the user might be surprised to see here.

*Example (fictional).* A friend writes "Still in for Lantern Night?" A search shows it is a Friday supper club dinner planned in a group chat, and the calendar shows a clash. The quick win reads: "[Lantern Night](link): Friday supper club dinner from the group chat; clashes with your evening hold. a) confirm and move the hold, b) decline."

**Meetings.** When an item asks for a meeting, check for meetings already booked with that person soon; one often covers the ask. When a do-now item is prep for an upcoming meeting, offer a meeting-prep workflow once the user decides.

**Catch work done mid-run.** Before each new batch, check recently sent messages, drop anything already answered, and note it in one line.

**Good questions** resolve real uncertainty: whether a goal is still live, whether the user wants to handle a sensitive thread personally, whether an unfamiliar sender matters, how much time they have. Never ask what the data already answers. The user can move any item to any bucket; their choice is final.

### Drafts, only when asked

Check the request against the thread first: if a requested point repeats or contradicts what the other person said, or misreads the ask, say so in one line and draft the version that makes sense. By default, give one draft per response as copy-ready text in the final block, with the item's link directly above it, after all tool calls. Never send. The item stays open until the reply is sent.

### Creating a task

Create one record with a clear action name, open status, due date, importance, urgency, time estimate, and project. Notes:

```markdown
**What:** the ask and who is waiting.
**Source:** <link, or "<network>: <contact>, <date>">
**Context:**
- Key fact or constraint, with link.
**Next step:** the first concrete action.
```

Do not pre-draft replies in the task unless asked. If an existing task is superseded rather than completed, propose an archived or cancelled status, not done. Then tell the user the item can leave its inbox.

## 8. Close and improve

Re-run the drafts check before calling any source zero. Then give a per-source status:

| Source | Cleared | Tasked | Delegated | Still open | Drafts unsent (kept) |
|---|---|---|---|---|---|
| [source] | [n] | [n] | [n] | [n] | [n (n kept)] |

If many loops remain open, say so plainly.

**Readiness check:**

- Every in-scope source was read, or its failure is named.
- Every item is in exactly one bucket, opened far enough to judge it.
- No unanswered or user-flagged chat sits in no action without the user's say-so.
- Every remaining draft is kept on purpose, explained as not a real loop, or reported as open.
- Nothing actionable lives only in an inbox.

Then audit the run for friction: a pointless question, a misfiled item, a misbehaving source, context you had to hunt for. With permission, update the configuration to fix the cause in general terms, never storing message content or credentials.

## Common failure modes

- Dumping every bucket at once, or moving on before the user acted.
- Doing the work a message describes instead of tasking it.
- Judging a chat by its last message, or bucketing from a preview when the ask sits in an unopened file.
- Forgetting unsent drafts, or counting templates and other non-loops as open.
- Flagging a reply as owed when it was sent in a thread or another channel.
- Relaying an ask the user cannot place, or proposing a meeting that already exists.
- Guessing an owner instead of saying "owner unclear".
- Quietly dropping a failed source, inventing links, or taking an undelegated action.

## Optional extras

**Single-item mode.** When a reminder or the user hands over one item, such as the oldest unhandled email, skip goals, sorting, and the opening message, and read only that item and the context it needs. Treat it as one do-now item with a recommended bucket and next action. When it is handled, tell the user which inbox action clears it; if a reminder system watches the inbox, let it detect the change rather than requiring a phrase like "done". If you clear it on request, continue straight into any waiting request in the same turn.

**Robust goal queries.** In a database-backed planning system, use stable field identifiers rather than display names, and the system's documented date functions rather than raw string comparisons, which can silently match nothing. Inspect the schema when a query errors.

**Tick lists.** When the user must clear several saved items themselves, mirror their app's screen in its order, then re-read the list afterwards to confirm:

| # | Opening words as previewed | Date | Decision |
|---|---|---|---|
| [position] | [first words] | [date] | [✓ Clear, or Keep, with a short reason] |

**Delegated clearing.** Some tools have no quick manual way to empty a notification inbox, so the user may delegate clearing. Clear only items the user says are handled, not worth acting on, or confirmed as no action, never items decided but not yet acted on. Clearing a notification must never resolve, edit, or delete the underlying comment or record. Retry a transient error once, verify, report in one line ("Cleared 4, all verified, 29 left"), and know how to undo a mistake.

**Saved drafts in apps.** Where authorized, save each draft as a reply inside its own thread, using a method the user has verified keeps it attached there. Use real mentions in group threads, open the draft in the user's preferred app, and do not also paste it into the conversation. If a draft already exists, say so rather than overwriting it. If you cannot read saved drafts back, never recreate an edited one from your version; ask the user for their current text first.


---
name: design-a-work-sample
description: Designs a short, paid take-home work sample and tests it with simulated candidate submissions. Use when someone says "design a work test", "make a take-home", or "tighten our work test".
---

# Design a work sample

Use this workflow to create or improve a short, paid, asynchronous hiring exercise that produces clear, hard-to-fake evidence of whether a candidate can do the role. It is opinionated about order: agree on what to measure, choose a shape, draft, then test the draft with simulated candidates before calling it done.

## Quick version

- Before drafting anything, confirm you have a role description and a role-success profile. If either is missing, write that first.
- Ask your assistant for a one-page memo covering the 3 to 5 load-bearing traits to test, what this stage will not test, the role's level, 2 or 3 failure patterns to catch, and what a strong submission looks like. Agree on it before moving on.
- Ask for three different exercise shapes. Each should be scorable in about 20 minutes, self-contained, and graspable in a minute. Pick one.
- Draft using the template in section 7, with time guidance per part, payment details, and anticipated questions. End with notes listing choices worth challenging.
- Ask the assistant to write two full fictional submissions: one from a strong role-aligned candidate and one from an earnest candidate missing one role-critical capability. See where the exercise separates them and where it does not, then revise.
- Before sending, sweep the candidate-facing text for signs of unedited AI writing and for formatting that will break in your destination system.

## 1. When to use this workflow

A work sample usually sits between application review and interviews. A weak one wastes candidate time, buries reviewers in submissions that tell them little, and lets poor matches through. A strong one compresses days of on-the-job judgment into a few hours of evidence.

Use this workflow when someone asks to design a work sample, create a take-home exercise for a role, or tighten an existing one. Collect these inputs:

- **Role name.** If it is not given, ask once.
- **Intent.** Create a new exercise or improve an existing one. Infer this from context when you can.
- **Destination system.** Where the instructions will be pasted, such as an applicant tracking system, a shared document, or a message. This drives the formatting rules.
- **Hiring owner.** The person who approves each gate. All approvals below come from this role.

Do not use it for interview questions or interview scoring guides, multi-day or in-person work trials, or screening questions on an application form. If the request could mean one of these, ask which format is needed.

When this workflow draws on records about people, such as past hiring feedback, team notes, or prior submissions, use them only to design or validate this exercise and only with the hiring owner's authorization. Read the minimum relevant sources, preferring role descriptions and anonymized examples of strong work over records about named individuals. Leave out unrelated or sensitive personal details, never reuse a past candidate's material in a scenario, and keep memos, simulations, and owner notes within the group approved to see hiring materials for this role.

## 2. Hard rules

1. **No design without a role description and a role-success profile.** The exercise is a function of the profile. Without one, it produces noise.
2. **Alignment memo before any draft.** Agree on what is being measured before writing candidate-facing text.
3. **Simulate two candidates before declaring version 1 done.** Analysis alone misses gaps that real submissions reveal.
4. **Candidate-facing text must read as edited by a person.** Apply the format checks on every pass.
5. **Every draft ends with notes for the hiring owner.** These surface choices worth challenging.
6. **Measure only role-relevant capability.** Exclude protected characteristics and proxies for them. Offer a route to reasonable accommodations or an accessible equivalent format without lowering the role-relevant standard.

## 3. Pre-flight

Confirm that two things exist:

1. A current role description: responsibilities, level, expected outcomes, reporting line.
2. A role-success profile, hiring plan, or equivalent: the capabilities and experience most likely to produce the role's outcomes.

If either is missing, stop. Do not accept "we will figure out the profile while designing the test." That creates a moving target. Use a message like:

> Before we design the work sample, I need the role description and a role-success profile. I found [what exists], but not [what is missing]. Want me to help draft the missing piece first? It usually takes less time than iterating the exercise against an unclear target.

Do not proceed until both exist and the hiring owner confirms them.

## 4. Read the context

Read in full:

- The role description and role-success profile.
- Linked planning notes the owner has authorized: sourcing notes, design notes, team constraints, anonymized examples of strong work.
- One or two existing work samples for comparable roles, if available. Use them only to calibrate tone, length, and structure. Do not copy their task shape; different roles need different evidence.

Give a one-line status, for example: "Read 5 pages of role context and 2 reference exercises. Moving to the alignment memo."

## 5. Write the alignment memo

Do not draft candidate-facing text yet. Write a one-page memo titled **What we are testing for and why: [Role] work sample** with these sections.

1. **Load-bearing traits (3 to 5).** What the role succeeds or fails on that this exercise can surface in the time window. Phrase each as an observable capability. Weak: "strategic thinking." Better: "Finds the highest-leverage problem in a messy situation, explains the tradeoff, and delivers a useful first action."
2. **What we are not testing.** Important qualities that belong to other stages. Interviews can assess motivation, live reasoning, and conversational sharpness. A work trial can assess reliability over days and judgment under pressure. References can assess reliability over months and integrity. Naming these keeps the exercise honest about its limits.
3. **Calibration to level.** Junior, mid, senior, or leadership. Level drives payment, expected output volume, and how much context to provide. Junior candidates need more context and narrower tasks. Senior candidates should make tradeoffs and produce work another person could use without explanation.
4. **Failure modes to catch (2 or 3).** Specific work patterns that could look fine in a conventional process but would not meet this role's needs. Describe the pattern, not the person. Examples: a polished planner who does not ship; a fast executor who misses the central problem; a careful candidate who defers every meaningful decision.
5. **What strong looks like.** One paragraph describing a top submission: what it notices, what it decides, what it produces, how it handles uncertainty.

Present the memo and stop. Ask: "Does this match what you want this work sample to assess?" Do not move on until the owner confirms or amends it.

## 6. Propose three shapes

Once the memo is locked, propose three shapes. Each must:

- Test the load-bearing traits, each in a different way.
- Be scorable in about 20 minutes per submission.
- Be self-contained, with no access to internal tools or private data.
- Be graspable by a candidate in about 60 seconds.

For each option give the shape, what it tests, two sentences on why it is evaluable, and one main risk. Keep each to about 150 words.

Shapes that often work:

- **Triage pile.** For high-volume, communication-heavy roles. The candidate gets a start-of-week pile of 8 to 10 items, writes a plan, ships real drafts, and proposes one systemic fix.
- **Pick the highest-leverage thing and ship it.** For strategic operations and builder roles. The candidate chooses one priority from a brief, justifies it, and ships a minimum usable version.
- **Diagnose and ship one fix.** For pattern-recognition roles. The candidate reads a messy situation, writes a diagnosis, and ships one targeted intervention.
- **Source and pitch.** For recruiting, partnerships, and outreach roles. The candidate defines the bar for a target profile, finds non-obvious channels from supplied information, and drafts outreach.
- **Decision-useful analysis.** For research, strategy, and specialist roles. The candidate picks one of two areas and produces a take a decision-maker could act on.
- **Design a repeatable system.** For program and community roles. The candidate designs one event or process and the reusable system behind it.

If none land, propose three more based on the confirmed traits. Do not force a familiar shape onto a role because it worked elsewhere. Do not draft until the owner picks a shape.

## 7. Draft version 1

Fill in the template below for the chosen shape. Apply the format checks in section 8 as you write. End with the notes in section 9.

### Candidate-facing template

Replace bracketed placeholders. Use bold lines rather than headings for section headers if that pastes better into the destination system.

```
## [Role] Work Sample

This work sample assesses your ability to [2 or 3 trait verbs from the memo].

You have **[N] hours** total.

**Your mission**

[One paragraph. A specific situation, not an abstract task. Include any authority or unavailable-stakeholder constraint that forces decisions. End with one line restating what the candidate will produce.]

**Deliverables**

[2 to 4 parts with rough time guidance. Common operations pattern:
- Part 1: plan or analysis (about 45 to 60 minutes, about 400 to 500 words, shorter if sharp; name what you are choosing to skip).
- Part 2: ship the work (about 75 to 90 minutes, 5 to 7 real drafts or outputs; do not let the planning eat the shipping).
- Part 3: one systemic fix (about 20 to 30 minutes, usable by a teammate without further explanation).]

**Context**

[The program, project, or team being operated: size, audience, current state. If relevant, a list of fictional roles the candidate can reach this week, with deliberate availability choices.]

[Optional for triage shapes: The pile, then Reference notes.]

**Instructions**

- Spend **[N] hours** on this work sample.
- Submit **within [X] days** of receiving this message. Sooner is better.
- Submit a **single document or PDF**. If you built supporting materials (a spreadsheet, diagram, or database), include links with sharing enabled.
- **This is a paid work sample.** After submitting, use [the payment form] to request **[BASE AMOUNT]**. [Optional: We will pay **[BONUS AMOUNT]** if you submit within [Y] days.]
- You may use AI tools. Use them carefully and with judgment, and do not submit filler. Briefly note any material use.
- Show your **depth or sharpness** somewhere. Do not try to be comprehensive everywhere; invest your time where it shows what you can do.
- [Optional: Include a short, unpolished walkthrough video of 3 to 5 minutes. A minute of you thinking out loud beats five minutes of rehearsed narration.]
- If you need an accommodation or alternative format, contact [contact route].

**Anticipated questions**

- *A requirement is unclear. What should I do?* Make a reasonable assumption, as if you had asked us and the answer did not surprise you. Note the assumption briefly.
- *What if I do not finish in time?* Submit what you have, with a short note on where you got to and what you would do next.
```

Optional additions when the shape calls for them:

- **Time-zone question** for scenario exercises: "Respond as if it is [day] morning at your desk in [scenario location]. No need to adjust for your actual time zone."
- **Use-of-work question:** "Your work is used only to evaluate candidates for this role. Any other use we will agree with you separately."
- **The pile.** For triage shapes: 8 to 10 realistic, fictional items, each with timestamp, source role, and full text where communication is central. Several items should connect so that seeing the whole picture is rewarded.
- **Reference notes.** Inline data the candidate needs to make fair calls, such as backup capacity, escalation policy, or refund policy.

### Invented example: one pile item

For a fictional nonprofit, Larkspur Learning, hiring a Program Operations Coordinator, one item in the pile might read:

```
**Item 4**<br>
**Received:** Monday, early morning<br>
**From:** Avery Quill, volunteer facilitator, [placeholder address on a reserved example domain]<br>
**Subject:** Thursday session

Hi, something came up and I can't lead Thursday's session for Group C. My notes are in the shared facilitator folder if someone can cover.

Thanks,<br>
Avery
```

Item 7 has a second facilitator flagging a Thursday conflict, and the reference notes list a small backup pool. A candidate who links items 4 and 7 sees that Thursday has no lead at all and books cover; one who answers each message in isolation does not.

### Payment

Payment amounts are the hiring owner's choice. A broadly useful pattern is a base payment for submission within a week and a modest bonus for faster submission. Amounts can scale with level but do not need to match a senior candidate's hourly rate; the bonus mainly signals that speed matters. For roles where speed is central, a three-tier structure (for example within a week, within three days, within one day) filters on speed more strongly.

| Role level | Base payment | Early-submission payment | Early window |
| --- | --- | --- | --- |
| [Junior] | [amount] | [amount] | [days] |
| [Mid or senior] | [amount] | [amount] | [days] |

## 8. Format checks for candidate-facing text

Sweep these on every pass. Many are signs of unedited AI output; others are rendering problems.

- **Dashes sparingly.** Prefer commas, semicolons, periods, or parentheses. One or two long dashes are fine; a text full of them reads unedited.
- **"By the end of [day]",** never "by end of [day]".
- **No horizontal divider lines** if the destination editor mishandles them. Use bold headers and natural breaks.
- **No tables** if the destination system does not render them. Use bullets with bold leads.
- **No punchy contrast slogans** such as "the bar is X, not Y" or "it's not just X, it's Y".
- **No stacked repetition,** such as three sentences in a row starting the same way, or several sentences each ending in a list of three.
- **One spelling convention everywhere.** Pick one locale (for example US spelling: organization, program, prioritize) and use it consistently across candidate-facing text and all your other writing for the role. The owner chooses which.
- **Sign-offs on two lines** ("Best," then the name on the next line) in fictional messages.
- **Clearly fictional contact details.** Use obviously placeholder addresses on a domain reserved for documentation examples. Never use realistic-looking personal addresses, because candidates may try to contact them. Do not wrap addresses in angle brackets, which can trigger autolinks.
- **Soft line breaks for metadata blocks.** Some paste flows merge consecutive lines (From, To, Subject) into one paragraph. Use the destination's soft-break method, such as an explicit line-break tag at the end of each metadata line. Avoid blank lines between header fields; they look wrong. Bullet lists are usually safe.
- **Names in the scenario.** Default to fictional names or role titles, kept consistent across items. Use a real colleague's name only with that person's agreement and the owner's approval.
- **No confidential details,** credentials, private contact information, or sensitive internal data.

## 9. Notes for the hiring owner

End every draft with a section titled **Notes for the hiring owner (not for the candidate)**. Write 3 to 6 tight bullets on choices worth challenging. Good entries look like:

- "I split the problem items across two groups to test pattern-spotting, but it feels contrived. Easy to concentrate them in one group instead."
- "Item 6 is obvious noise that takes five seconds to skip. Drop it or make it subtler; right now it does not separate stronger from weaker work."
- "Payment matches your other exercises for this level. For a speed-critical role, we could add a one-day tier."
- "I left out a recorded briefing from the project lead. More realistic, but costs production time."

Close with one question that pushes the next decision, such as "Where do you want to push first?"

## 10. Iterate

Expect three to seven rounds. Each round, output the **full updated exercise**, not a diff, so it can be pasted directly.

Typical feedback: too vague (tighten), too prescriptive (loosen), cut a section (cut and renumber), unrealistic details (check facts such as program length, team size, prices), format problems found late.

Apply feedback unless it would materially harm validity, fairness, privacy, or safety. If you disagree, say so once, briefly, offer an alternative, then follow the owner's decision.

## 11. Simulate two candidates (mandatory)

When the owner says the draft is close, run two simulations in parallel (separate agents if available, or two separate prompts in a chat assistant). Embed the full candidate-facing text in each. Both personas are synthetic.

- **Role-aligned persona.** A strong candidate matching the role-success profile. Produces a real submission for every part, as they would type it, plus about five sentences reflecting on choices, uncertainty, and time use.
- **Plausible role-misaligned persona.** An earnest, conscientious candidate who would pass screening at most organizations but whose work lacks one role-critical capability. Pick a relevant mismatch from the memo's failure modes: process-first where the role needs action, hedging where it needs decisions, designing systems where it needs shipping. Tie the difference to work evidence only, never identity or background. Same complete submission, in character.

Then write a synthesis:

1. **Where the exercise separated them sharply.** Items or parts with visibly different work.
2. **Where it did not.** Items both handled the same way. Floor checks are fine, but a central trait that fails to produce different evidence is a problem.
3. **What this tells us.** What the exercise does and does not predict.
4. **Improvements,** specific and ranked by impact.

In the Larkspur example, a useful synthesis line might read: "Sharp separation on items 4 and 7: the aligned persona booked backup cover for Thursday; the misaligned persona replied politely to each and asked the unavailable program lead to decide. No separation on item 2: both answered the routine schedule question correctly, which is fine as a floor check."

## 12. Apply improvements

Rewrite the exercise and output the full version. Useful changes include making connected items more interdependent, removing obvious noise, adding a constraint that forces a real tradeoff, replacing an opinion prompt with a usable deliverable, sharpening reviewer guidance so it rewards the intended behavior, and removing trainable knowledge requirements. Make the exercise more diagnostic, not merely harder.

## 13. Final readiness gate

Do not mark the exercise complete until:

- Role description, profile, and alignment memo are confirmed.
- The shape maps directly to the load-bearing traits.
- A qualified candidate can finish in the stated time.
- It is self-contained and needs no private access.
- Scenario facts are plausible and consistent with the real program or team.
- Payment amounts, links, deadline, and submission format are correct.
- Section order matches the owner's preferred layout (commonly mission, deliverables, instructions, anticipated questions, with context and the pile either appended or in a separate document).
- The format checks pass for the destination system.
- A reviewer can score a submission in about 20 to 25 minutes.
- Both simulations ran and led to any needed revisions.
- An accommodation route is included, there is no unpaid production work, and proxy bias has been checked.

## 14. Common failure modes

- **Drafting before the memo is locked.** It costs several wasted rounds.
- **Testing trainable things.** Specific tool fluency, domain vocabulary, or field knowledge that a capable hire can learn in a few weeks. No item should require it.
- **Slow grading.** Over about 25 minutes per submission, a long exercise scales worse than a short one.
- **Dozens of micro-decisions.** Aim for one piece of substantive reasoning, five to seven substantive outputs, and one usable artifact.
- **A pile that does not connect.** Independent items test volume, not judgment.
- **Reachable stakeholders.** If every decision can be deferred to someone who replies quickly, decisiveness is not being tested. Make key roles unavailable during the window.
- **Word-count targets that invite padding.** "About 400 to 500, shorter if sharp" beats a wide range, or drop the target.
- **An optional video nobody records.** If it adds signal, frame it as something most strong submissions include.
- **Rewarding polish over substance** when the role needs something else.
- **Declaring success without checking** that the exercise distinguishes the role-relevant performance it was built to measure.

A finished work sample should feel like a small, fair version of the job: bounded, realistic, quick to score, and clear about what good work looks like.

## Optional extras

**External review.** If others give feedback, assess each suggestion against the memo. State which to integrate, which to skip, and why, then output the full version. Treat review as input; the hiring owner decides.

**Prefilled payment links.** If your payment form supports prefilled links, create one link per amount (role name, amount, payment type), and hyperlink each dollar figure itself rather than generic text like "this form." Check every link before finalizing.

**Capture lessons.** Before closing, record anything learned in your own reference for this workflow: new format problems, shapes that worked, failure modes the simulation exposed, payment changes, better template wording, memo refinements. Record lessons as general principles, without details about individual candidates. Summarize the changes in one or two bullets. Make small wording fixes freely; ask before structural changes such as adding a step or dropping the simulation.

**Working style with the owner.** Keep status updates to one line and use one consistent date format in messages to the owner. Put drafts directly in your reply by default. If the owner asks for a shared document instead, follow the folder and naming conventions they have chosen for such documents. Candidate-facing text still follows the destination system's paste and formatting rules from section 8, wherever the draft lives.


---
name: run-a-reference-call
description: Prepares a briefing page for a candidate reference call, with context, a tailored opening, and targeted questions. Use when checking references or asked to prep a reference call.
---

# Run a reference call

Use this workflow when a hiring manager is checking references on a candidate for a role at their own organization. The output is a ready-to-use call page with context, a tailored opening, briefing notes, and a question list.

## Quick version

Light path: paste the candidate's CV (or a short summary of it), the role, and the referee's name and role. Ask for the briefing page. No connected tools are needed.

- The assistant writes a short context section: who the referee is and how they worked with the candidate.
- It drafts a tailored opening you can read out in under a minute.
- It writes briefing notes: what this referee can uniquely confirm, and any themes from earlier references to test.
- It gives one list of core questions plus three or four probes for the role.
- Save the page with your other reference pages for this candidate so later calls can build on it.
- After the call, paste your rough notes back and ask it to separate what the referee saw from what they concluded.

## 1. Scope, deliverable, and inputs

**Direction check:** this workflow is for references you collect on a candidate you might hire. If an outside organization is asking *you* for a reference on someone you know, use a separate "give a reference" workflow instead.

**The page is the deliverable.** Do not stop after research or reply with a chat summary. The hiring manager will read the page, not the conversation. Everything useful must be on the page.

**Privacy and authorization.** Research the candidate and referee only for a legitimate hiring purpose, when the candidate has supplied or agreed to this referee and the user has authorized the sources you search. Use the minimum relevant information (role, organization, working relationship, job-relevant work history) and leave out personal life, health, family, protected characteristics, and anything unrelated to performance. Keep the page within an access boundary limited to the hiring team, as set out in section 4.

| Input | Source if not provided | Notes |
|---|---|---|
| Candidate name | Required from user | The person being hired |
| Referee name and contact | Calendar invite, candidate's reference list email | The person being called |
| Role | Hiring emails, notes, or applicant tracking system | Needed for role-specific probes |
| Call date | Calendar event; otherwise today | Date only is fine |
| Hiring manager name and organization | User profile or user's choice | Used in the opening and page attendees |
| Hiring space | User's choice | The one place all reference pages are saved |

When tools are connected, run every section below in order. Otherwise, use the Quick version with what the user pastes in.

## 2. Find the scheduled call

- Search the user's calendar for events with the referee's name or contact.
- Extract the title, time, attendees, video link, and any scheduling notes.
- If there is no event yet, note that and continue.

## 3. Gather context

**3a. Hiring context.** Search the user's email and notes for the candidate's name to learn:

- The role they applied for.
- Their current stage (interview, work trial, final round).
- How the referee was introduced. The candidate's reference list message is usually the key source.
- The referee's relationship to the candidate (manager, client, peer, direct report, teacher).

**3b. Research the referee.** Run these searches in parallel:

1. Email: direct correspondence with the referee's address.
2. Email: the referee's full name, to catch introductions and reference threads.
3. Team chat: the referee's name and their organization's name.
4. Notes or meetings database: the referee's name, including prior meetings.
5. Calendar: past events with the referee.
6. Public web: "{Name}" plus their organization, for current role and professional background only.

From each email search, read only the few recent messages that concern the candidate, the reference, or the scheduling of this call.

**3c. Candidate links.** Collect links the hiring manager will want during the call: the applicant tracking profile, a professional profile, and any portfolio, code repository, or personal site the candidate shared in their application.

**3d. Completed references.** Search the hiring space for other pages on the same candidate (for example, "{Candidate Name} reference"). When every reference page lives there, one search is enough; if some older pages have not been moved yet, check those locations too. Read them and pull out themes, strengths, concerns, and development areas. These become specific angles to confirm or challenge in this call.

**3e. Compile findings.** Organize what you found into:

- **Who the referee is:** role, organization, short professional background.
- **Relationship:** how, in what capacity, and for how long they worked with the candidate, and how closely they saw the relevant work.
- **Hiring context:** role, stage, and next step such as work trial dates.
- **Candidate links.**
- **Other references:** who else is on the candidate's list.
- **Briefing notes:** the analysis described in section 5.

## 4. Create the call page

**Where to save it.** Create the page in one dedicated hiring space in the user's chosen notes tool, whose membership is limited to the hiring team. Not a shared team meetings space, and not scattered personal folders. Referees speak candidly about people the team may later work alongside, and one location keeps earlier references easy to find.

**Let access come from the space.** The page should inherit its permissions. Do not change its individual sharing settings or connect extra integrations to it. Restricting a single page after the fact may not remove access that people or integrations already had, so a page locked down on its own can be less private than it looks. If the space is not restricted enough, fix the space, not the page.

Create properties and content together:

- **Title:** `{Date} {Referee Name} ({Candidate Name} reference)`
- **Date:** call date, date only.
- **Attendees:** the hiring manager, plus any other interviewer joining.

**Verify before reporting done.** Read the page back from the system. Confirm it sits in the hiring space, the title and date display correctly (not as escaped code or raw markup), and the content is complete. Fix anything that did not render as intended.

Use this template and tailor every placeholder:

```markdown
## Context
- [{Referee Name}]({professional profile link}): {role, organization, one-line background}.
- {Candidate} worked with {Referee} as {relationship, capacity, duration}.
- This is a reference call for [{Candidate Name}]({profile link}) ([applicant profile]({link}), {other links}), who is at {stage} for {Role} at {Organization}. Next step: {e.g., work trial dates and location}.
- {Any prior contact or relationship history with the referee.}
- {Candidate}'s other references: {list}.

## Opening
> Hi {Referee}, thanks so much for making the time. I'm {Hiring Manager}, {their role} at {Organization}. {One sentence on what the organization does.} {Candidate} has applied for our {Role} role, and we're excited about their background. We're doing reference checks now so we can decide quickly. What you share stays within our hiring team. {If your policy allows recording: Is it OK if I record so I can take accurate notes?}

## Briefing notes
- **Themes from completed references:** {who said what, and what to test now}
- **What this referee is uniquely placed to speak to:** {...}
- **Organization and relationship context:** {...}
- **Anything else:** {open questions, concerns, gaps}

## Questions
- **How did you work together?** What was {first name}'s role, and what was yours? How closely did you work day to day?
- **What did they concretely deliver, and how did it compare to your expectations?**
- **What is their standout strength?**
- **If they joined us and it didn't work out after three months, what would be the most likely reason?**
- **If things are going well at three months, what development area would I most likely make their top priority?**
- **Compared to everyone you've worked with in similar roles, where do they rank?**
- **If I were their manager, what could I do to help them do their best work for our mission?**
- **What should I have asked that I didn't?**

### {Role}-specific probes to weave in
- {Probe 1}
- {Probe 2}
- {Probe 3}
- {Probe 4}
```

## 5. Write the briefing notes

This is the highest-value section. It turns research into actions for this specific call.

- **Use direct language.** Write "The first referee said Jordan sometimes over-commits to side requests. Ask how this referee saw Jordan handle a crowded week." Do not write "It may be worth exploring...".
- **Attribute themes internally, test them neutrally on the call.** The page may say who raised a point. On the call, ask an open question such as "How did they decide what to drop when too much was on their plate?" Do not reveal what other referees or interviewers said, and do not lead the referee toward a conclusion.
- **Name the unique angle.** A former manager can speak to reliability and how much support the candidate needed. A peer can speak to collaboration. A client can speak to communication and delivery under pressure.
- **Flag organization links** the hiring manager should know about, such as past collaborations or shared channels.
- **If this is the first reference,** say so. List what to listen for that will be useful to compare across later calls.

## 6. Choose role-specific probes

Pick probes that test capabilities the role actually needs. Write three or four. Examples:

- **Data analyst:** How do they check their own numbers before sharing them? How do they explain a messy result to someone without a data background? Do they push back when a question is badly framed?
- **Customer support lead:** How do they stay calm with an angry customer? Have they turned repeat complaints into a fix rather than a workaround? How do they coach newer teammates?
- **Engineering manager:** How do they handle an underperforming report? What do they do when the roadmap and the team's capacity disagree? How much do they still write code, and is that the right amount?

## 7. Worked example (invented)

Inputs pasted into a plain chat: Jordan Lee's CV, applying for Data Analyst; referee Sam Ortiz, Jordan's manager for two years at a regional grocery chain. One earlier reference, from a peer, praised Jordan's clear dashboards but said Jordan sometimes says yes to too many side requests.

Briefing notes the assistant writes:

- **Theme to test:** the peer said Jordan over-commits. Sam managed Jordan's workload directly, so ask how Jordan handled a crowded week, without mentioning the peer.
- **Sam is uniquely placed to speak to:** how much support Jordan needed, and whether Jordan's analysis changed real decisions.
- **Probe:** "Tell me about a time Jordan's numbers turned out wrong. What happened next?"

## 8. During and after the call

- Follow vague praise with "What did that look like?" or "Can you give an example?"
- Weight evidence by how directly the referee observed the work, not by their title or confidence.
- Afterward, record notes on the same page. Separate what the referee observed, how the referee interpreted it, and your own inference. Note confidence and limits on what they could know.
- Treat one reference as one input. Compare across references and other hiring evidence before deciding.

## 9. Style and quality checks

- Context is short bullet points, not paragraphs.
- The opening is tailored to this referee and candidate. Adjust the tone if there is prior contact.
- Questions sit in one bulleted list, not numbered, with no separate agendas.
- Candidate links and other references are on the page.
- Probes match the real role, not a generic list.
- Earlier references were searched, including any locations not yet consolidated.
- You read the page back and confirmed its location, title, date, and content before reporting the task complete.

## Optional extras

- **Meeting-notes or transcription block.** If your notes tool offers an in-meeting transcription or AI notes block and recording is allowed, add it at the top of the page. Put only the meeting title inside it and let the tool fill in the summary and transcript during or after the call.
- **Date fields and inline date tokens.** Some notes tools support a live date token in titles, but the syntax can differ between the tool's own editor and its programmatic interface, and the wrong form may be saved as literal text. Use the form your tool documents for programmatic page creation, set the date property as date only (no time), and confirm the result when you read the page back.
- **Setting up the hiring space.** If you do not have one yet, create a closed space whose members are only the people on hiring panels, then move all existing reference pages into it in one pass. Afterward, check which integrations can reach the workspace as a whole, since page-level settings may not override them.


---
name: access-check
description: Finds content about an incoming person in shared chat and knowledge spaces and recommends what to restrict first. Use when adding a new hire or advisor, or checking before you add someone.
---

# Check before granting access

Use this workflow before adding a new hire, advisor, contractor or collaborator to a shared chat workspace, a knowledge base, or both. It answers one question: **once they join, could they read anything about themselves that should not be visible to them?** It then recommends what to restrict, move or redact before you grant access.

## Quick version

- List every way the person might be written about: full name, surname alone, first name, nicknames, likely misspellings and their chat handle.
- Write down exactly what they will be able to see: which channels, spaces and shared databases. Everything else is out of scope.
- Search each visible space yourself for every name variant. Paste the relevant hits (with their location and link) into your assistant. Include whole threads, not just the first message.
- Ask the assistant to rate each hit: **▲ Hide** (fix before they join), **◆ Consider** (your call), **○ Fine** (checked, harmless). Flag anything they would find hurtful, misleading or awkward, or that reveals plans about them they do not know about.
- Ask for a short report that leads with the count of ▲ and ◆ items and whether anything blocks access today, with one linked item per finding.
- Change nothing until you have decided. After fixing, search again to confirm nothing visible remains.

## 1. Set the scope and gather inputs

Look only for content that mentions the incoming person directly. Ignore other sensitive material, however interesting, unless it is about them.

Run this only if you are authorized to manage access to these systems, such as a workspace admin or the person's sponsor, and search only the systems the person is about to join. Quote only the line needed to judge a finding; for health, family or other personal-life details, name the category (for example "mentions a family matter") instead of repeating it. Send the report only to the requester, never to a shared space.

| Input | Why it matters |
|---|---|
| Full name, nicknames, likely misspellings | Catches mentions that exact-name search misses |
| Chat user ID or handle, if they already have one | Catches tagged mentions |
| A disambiguator, such as current or past employers | Rules out people with the same name |
| Which private channels and restricted spaces they will join | Defines what they can actually see |

If the requester says "standard team-member access", assume every public channel and every open knowledge-base space, with no private channels or restricted spaces.

## 2. Identify the person

1. Look up the person in the user directory of each system.
2. Many first names are shared. Keep the disambiguator handy and drop namesakes as you go.
3. List the spelling variants you will search (for example a surname with swapped vowels or a missing letter).

## 3. Map what they will and will not see

This decides what counts as exposed. Skip what they cannot see, but say what you skipped.

- **Usually not visible:** direct messages and group messages they are not in; private channels they will not join; closed or restricted spaces they will not join, such as a hiring space holding reference notes, unless they are joining that team; the requester's personal or private spaces and databases (if the requester excludes them); pages in another user's private section.
- **Usually visible:** public channels; private channels they will join; every page in shared spaces and shared databases, including meeting notes, strategy, projects and archives. Hiring pages left in an open space count as visible even when a separate closed hiring space exists.

Rules for unclear cases:

- **Keep a list of the requester's private locations.** Ask which databases or folders are private to them, and recognize search hits by the location path shown. Private locations get renamed, so record former names too, and treat a hit under any of them as not visible.
- **Search tools often cannot see page-level permissions.** A page may be restricted while still sitting in a shared database, and search returns it anyway. Treat every page in a shared space as visible unless the requester confirms it is restricted. Then move it to the skipped list as "restricted, confirmed by requester".
- **Pages with no parent location** (for example auto-generated meeting notes) are often private to their creator. Treat them as not visible unless they show explicit sharing or the requester says otherwise.
- **System-generated user profile pages** usually carry no content. Skip them. An access error on them is expected and not worth reporting.

## 4. Search the chat workspace

Cover every channel you are allowed to search:

- Full name, surname alone, and each misspelling, newest first. Page through results until they stop being about the person.
- First name alone, to catch casual mentions. Skim for context and drop namesakes.
- Their user ID as a keyword, to catch tagged mentions.
- Any announcement about adding them. Read the full thread, since colleagues may have replied with concerns.

For each relevant hit, record the channel type and a permanent link. Read the full thread around any hit that has replies. Direct messages are not visible to the person, but list them with links in the skipped section so the requester knows they were seen.

## 5. Search the knowledge base

1. Search the full name, each misspelling, and the name combined with their main employers or role. Ask for a large page of results.
2. If the requester's private space is excluded, run the same searches (including the employer and role combinations) limited to that space. Exclude every hit the limited search returns, even when the unfiltered search also shows it. Judge by this limited search, not by the location path: pages under generic-looking paths such as an archive or task list can still sit inside the private space.
3. Open every remaining hit that mentions the person beyond a passing name-drop. Read the full text and check its location against your visibility map.
4. Check structured properties as well as body text: hiring status fields, pipeline stages, contact-relationship fields, and similar.
5. If a page fails to open, report it with its link and ask the requester to check it by hand.

## 6. Judge each mention

Flag a mention when the person would plausibly feel hurt, misled or awkward reading it, or when it reveals plans about them that they do not know about.

**Flag:**

- Candid assessments: doubts about their skills, commitment or results.
- Hiring, offer, compensation or persuasion strategy aimed at them, including records marking them as a lost or declined candidate.
- Other people's plans for them that they may not know about.
- Reference feedback, gossip, or health, family or personal-life details.
- Colleagues' doubts about what they contribute.

**Do not flag:**

- Neutral mentions: event replies, being tagged on a link, a field recording who introduced them.
- Praise and accurate bios.
- Their own advice recorded in meeting notes. **Exception:** if those notes include their candid remarks about third parties, mention this once. They may not expect those remarks to sit in a team-wide space.

Rate every finding with a word and a symbol, never colour alone:

| Rating | Meaning |
|---|---|
| **▲ Hide** | Restrict, move or redact before they join |
| **◆ Consider** | Mild; the requester decides |
| **○ Fine** | Checked and harmless; listed briefly for completeness |

## 7. Report

Lead with the answer: the number of ▲ and ◆ items, and whether anything blocks granting access today. Then list one item per finding:

- Bold rating, then the page or message label as a short hyperlink (for example `[#announcements, 4 Oct](link)`), never a bare URL
- Where it lives, and whether the person would see it
- The exact line that matters (or the category, for sensitive personal details)
- Recommended fix: restrict the page, move it to a private space, or redact one line

Every item gets its own working link, including **○ Fine** items and skipped direct messages. The requester will check each one, so an item without a link is not useful. Close with failed fetches and the list of what was skipped as not visible.

**Invented example.** Before adding Jordan Vale, a fictional advisor from the fictional Maple Street Studio:

> **1 ▲, 1 ◆. One item blocks access today.**
>
> - **▲ Hide** [Hiring pipeline: Jordan Vale](link). Open projects space, visible. Status field "Declined, revisit later"; note: "unsure about follow-through." Fix: restrict the page or move it to the closed hiring space.
> - **◆ Consider** [Advisory board planning](link). Strategy space, visible. "Jordan might push for equity; hold firm." Fix: redact the line.
> - **○ Fine** [#announcements, 4 Oct](link). Welcome post, all positive replies.
>
> Skipped as not visible: 2 direct messages ([1](link), [2](link)); 1 page in a private meeting database ([link](link)); 1 reference-call note in the closed hiring space ([link](link)).

## 8. Make changes

Do not change permissions, move pages or edit content without explicit approval. Moving or redacting someone else's page is a material change, so confirm with its owner where appropriate. Prefer restricting access over deleting, and do not delete or alter records under a retention duty, a legal hold, or the person's legal right to access data about them; if unsure, flag it for the right owner. After approval, make the edits, then re-run the searches to confirm nothing visible remains.

## Common failure modes

- Searching only the exact name and missing misspellings, nicknames or tagged IDs.
- Confusing a namesake with the person.
- Assuming a page is private because search cannot show its permissions.
- Treating a closed space as visible when the person is not joining that team, or missing sensitive pages left in an open space.
- Missing a private location because it was renamed, or reporting it as exposed.
- Deciding whether a hit is in the private space from its path instead of from the limited search.
- Reading only the first message and missing a critical reply in the thread.
- Missing sensitive content stored in page properties rather than body text.
- Acting on findings before approval.

## Optional extras

- **Parallel searches.** With an agent connected to your chat and knowledge tools, run all name variants at once and ask for detailed results so each hit comes back with a permanent link.
- **Scoped exclusion search.** If your knowledge tool can limit search to one space, run every name and employer query limited to the requester's private space and exclude everything it returns, instead of guessing from titles or paths.
- **Reusable location list.** Keep a short note of private locations (current and former names), closed team spaces, shared databases and typical access bundles, so each check starts from an accurate visibility map.
- **Re-check routine.** After fixes, have the agent re-run the same saved queries and report only items still marked ▲ or ◆.


---
name: use-a-browser-safely
description: Completes browser tasks safely: least invasive route, verified account and fields, confirmation before acting. Use when filling forms, fixing dashboards, or working in a signed-in app.
---

# Use a browser safely

Use this workflow when a task has to happen in a web browser: filling a rendered form, changing a setting in a dashboard, collecting information from a page that only renders with scripts, testing a user flow, or working inside a signed-in session the user has authorized. It keeps the work on the least invasive route and proves each change actually landed before anything irreversible happens.

## Quick version

These steps work even with a plain chat assistant that walks you through the task while you do the clicking.

- **Look for a shortcut first.** Ask whether the service has an export, official integration, API, or simple form you can use instead of clicking through a complex page.
- **Check where you are.** Before changing anything, open the account or profile page and confirm the signed-in account, the workspace or environment, and the exact item you will change.
- **List the fields before typing.** Note each field's label, whether it is required, and what kind it is (one line, multi-line, rich text, dropdown, checkbox, date). Make dropdown, checkbox, and date choices first, because they can reset the form.
- **Read back every field.** After entering text, click somewhere neutral on the page and check the value is still there and complete.
- **Stop before the final button.** Confirm every required field is filled, the values are right, and whether the action can be undone. Take a screenshot. For payments, sends, deletions, or "cannot be edited" forms, get a clear yes first.
- **Look for proof afterward.** A confirmation message, reference number, or saved record. If you see an error, check whether the action happened before retrying.

## 1. Follow the central rule

> Inspect the page before you edit anything. Read back every field you change. Do not click the final button until verification passes and the account, target, and authorization are clear.

A successful automation call does not prove the website accepted the change. A fill command usually reports success as long as it did not throw an error. It does not check that the application's internal state updated, that moving focus away committed the value, or that the field kept the content. **The caller verifies. Always.**

## 2. Choose the least invasive route

Use the first route that fits. Do not skip ahead.

1. **Direct interface first.** Look for a documented API, export, integration, or plain form endpoint before opening any browser.
2. **Isolated headless browser.** The default for anything that does not need the user's identity: public forms, extraction from dynamic pages, UI testing, and screenshots. It never opens a visible window and never touches the user's own browser.
3. **The user's signed-in visible browser.** Only when the task truly needs the user's live session, such as an account dashboard or single sign-on state.

### Look for a direct interface

Many forms send structured data to an endpoint that can be called directly, which skips the hardest browser problems. Read the service's official documentation, view the page source for a form action or embedded data block, or watch the browser's network requests while using the page normally. Booking and availability widgets are a common case: the results often come from a plain search or availability request that is easier to call than the widget is to drive. Fall back to the browser when no suitable programmatic option exists or when the user explicitly wants the UI flow.

Limits:

- Do not use undocumented endpoints to get around access controls, terms of service, rate limits, or anti-abuse systems.
- In a signed-in session, do not call an application's internal endpoints from page scripts. Requests that skip the headers or tokens the app normally sends can end the user's session or trigger security responses. Drive the UI instead, or use a supported API with proper credentials. Reading state the page already holds in memory, without network calls, is lower risk.

### Do not use the visible browser for convenience

The user's visible browser is their working space. Taking it over interrupts them and adds privacy and account risk. Extraction, bulk form fills, and anything that works headless should stay headless.

### Blocks and bot checks

If a site blocks headless automation during general research, accept the block and move on. Escalating to the signed-in browser is reasonable only when the user explicitly asked for a task on that specific site and the session is genuinely needed. Human-verification checks, security-key prompts, and multi-factor prompts belong to the user: pause, ask them to complete it, then continue. Never simulate, bypass, or weaken these checks, and never disable integrity or signature checks on local tools to make a connection work.

## 3. Pick the right automation style

- **Step-by-step tool calls** through an interactive browser tool suit one click, reading one snapshot, or short tasks with few actions and little text.
- **A standalone script** using a browser automation library suits long text, many fields, heavy single-page applications, or anything that needs repeatable runs.

Interactive tool layers can become unstable with long text, several parallel actions against one page, or heavy rendering. If the session crashes with a message like "page, context, or browser has been closed," switch to a script rather than rescuing the broken session. When in doubt, write a script.

Script hygiene: save scripts and artifacts in a temporary folder the user has agreed to, launch standalone automation headless unless a visible session is part of the plan, and pass secrets through environment variables or a secrets store. Never hard-code or log credentials.

## 4. Protect identity, privacy, and the user's browser

When the task touches private messages, records, dashboards, or information about other people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant pages and data, keep unrelated personal details out of screenshots, logs, and reports, and share results only within the requester's appropriate access boundary.

### Rules for the user's visible browser

- **Announce, then act.** Say briefly what you are taking over and why, for example "Taking over the browser to update the billing contact." Never take control silently. If the user already authorized visible browser use for this task, do not ask again.
- **Work in a fresh window, tab, or tab group.** Do not reuse the user's existing tabs unless they point to one.
- **Classify the context before choosing a profile.** Personal, work, test, staging, or production. Personal errands (shopping, banking, health, subscriptions, household, government services) are personal even on general-purpose sites. Internal operations, vendors, and colleague-facing work are work. If the user says which, that settles it.
- **Select the profile directly and do not trust display names.** A generic "current browser" selector often picks whichever profile was used most recently, and labels like "Browser 1" can reshuffle after restarts. Use a stable identifier where the tool provides one, and still verify every time.
- **A window is not a connection.** Opening a window for a profile puts it on screen; the automation connection may still point elsewhere. If a window is open but no connection ever appears for it, the connector in that profile is likely signed out or asleep. Ask the user to open and sign in to it in that window, then list connections again and verify.
- **Do not restart or force-quit the user's browser** without their explicit OK. It closes everything they have open.

### Account preflight gate

Before any action that changes data, answer:

1. **Which account is this?** Open a fresh tab to a reliable account page and read the signed-in identity.
2. **Which environment is this?** Production, staging, test, or a specific organization or workspace.
3. **What exact item will change?** The specific record, form, or setting.

If any answer is unclear, stop and ask. If your environment uses a permission gate or verification marker that unlocks write actions, set it only after the account check has actually passed, and record the evidence. Never set it just to get past the gate.

## 5. Set the task boundary and authorization

Before navigating deeply, identify the target page, record, form, or setting; what will be entered, collected, changed, uploaded, or sent; the minimum information needed; fields that need the user's judgment; and whether the final action can be undone.

**Reversible changes** the user asked for, such as toggling a setting or updating a saved card or draft, can proceed after normal verification.

**Irreversible or high-impact actions** need a pre-action record and confirmation unless the user already gave clear authorization for that exact action. These include payments, purchases, sends, invitations, publishing, deletions, plan or billing changes, access or ownership changes, and anything labeled "cannot be undone" or "cannot be edited after submission." Treat such forms as one-way doors. For deletions, note in the pre-action record whether the service keeps a restorable trash; a restore path lowers the risk but does not remove the need for authorization.

**Credentials stay with the user.** Entering API keys, tokens, passwords, or recovery codes into any form is the user's step. Set up everything around the credential (open the right page, fill the other fields, reach the input box), then hand the user exact steps to enter it themselves. Never move secrets by copy and paste through automation: a site's copy button can appear to work while the system clipboard still holds older, unrelated text.

Honor an explicit request to review before submission. If authorization is already given, do not ask again. If it is missing, prepare and verify the full result, show the pre-submit state, and ask only for the final action.

## 6. Inspect the page before editing

Before writing any fill logic, list every relevant control and record its kind (single-line input, text area, rich-text editor, dropdown, checkbox, radio, date picker, upload, custom widget), its label or label relationship, its required state, its current value or length, whether it is the real editor or a wrapper or hidden sync field, and whether changing it re-renders the form.

```text
// Pseudocode: adapt to the chosen automation library
controls = page.findAll('input, textarea, [contenteditable], [role=textbox]')
for each c in controls:
  record { tag, type, role,
           label: accessibleLabel(c),
           required: c.required or c.ariaRequired,
           length: readValue(c).length }
save record list to 'form-before.json'
```

Watch for:

- **Look-alike controls.** A single-line input silently strips line breaks. A text area usually accepts everything. Rich-text editors keep their own internal model and may ignore direct value changes.
- **Hidden sync fields.** Some editors pair a visible editable area with a hidden input that looks fillable. Filling the hidden input passes a raw DOM check, but the form reports the field as empty. Always fill the control the app actually reads.
- **Empty wrappers.** An accessibility locator can return a wrapper with no editable content. Follow the label relationship to the real editable element, then tag it with a temporary marker attribute so you can target it reliably.
- **Unstable order.** Field order can change between loads. Never address fields by position.
- **Current state.** Before changing an existing record or setting, read its current value so you do not overwrite the wrong thing.

## 7. Use the right interaction for each control

| Control | Preferred interaction | Watch for |
|---|---|---|
| Single-line input | Normal fill | Line breaks removed silently; length limits. |
| Multi-line text area | Fill, then move focus to the page body | Some apps commit only on blur. |
| Rich-text or content-editable editor | Click, select all, delete, insert text with keyboard-style input, then blur | Direct DOM writes or value setters may be ignored. |
| Dropdown or combobox | Open, choose by exact visible option text, wait to settle | Selection can re-render the whole form. |
| Checkbox or radio | Read the state first; click only if it needs to change | Clicking toggles an already-correct value. |
| Date or time picker | Set values, close by clicking neutral page background, check the rendered summary | Close or clear buttons may wipe values; typing while open can rewrite dates. |
| File upload | Confirm file, destination, and privacy first | Upload may start at once and be hard to undo. |

Robust sequence for framework-driven editors: click the real editable element, select all and delete, insert the new text with keyboard-style input, move focus to a neutral element to commit, wait briefly, then read the value back.

**Blur after every rich-text field.** Otherwise the next edit can trigger a re-render that rebuilds earlier editors from a model that never received their text, and only the last field survives.

**Order matters.** Do dropdowns, checkboxes, tabs, and other re-rendering choices first, then fill text. Re-inspect after each such choice. Set tricky widgets like date pickers early and re-check them after every later edit.

**Selectors drift.** Before clicking a send or submit control found by selector, read the composed content back to confirm it landed in the right place. Selectors that worked before can stop matching after a site update.

## 8. Verify after every fill

Read each value back and compare it with what you intended. For sensitive content, compare lengths or a short redacted summary rather than printing full text.

```text
result = fillField(field, value)
if result.length != value.length:
  log 'mismatch on ' + field.label + ': ' + result.length + '/' + value.length
  retry once with a different method (for example keyboard input instead of a setter)
  verify again; if still wrong, stop and report
```

Reading mismatches:

- **Empty after a reported success:** the app ignored a direct value change. Use focus-and-keyboard input, then blur.
- **Short by about one character per paragraph:** a single-line input dropped line breaks. Rewrite as one paragraph, or find the multi-line field.
- **Short after blank lines or repeated spaces:** the editor normalized whitespace. Usually acceptable; if not, simplify the formatting and note it.
- **Earlier field now blank:** a re-render reset uncommitted state. Blur each field and do re-rendering choices first.

If verification still fails after one retry, do not move toward submission. Report the problem and ask how to proceed.

## 9. Two-phase run and pre-submit gate

**Phase 1: prepare.** Fill everything, verify each field, save a structured after-state record, and capture a full-page screenshot. Do not submit.

**Phase 2: commit.** If the task or a standing instruction already authorizes the final action, continue. Otherwise show the prepared state and get the missing authorization. Then re-fill if needed, re-run the gate, and click the final control once.

A script can implement this with a flag such as `--submit` that is off by default.

```text
open headless browser and new page
go to target URL; dismiss banners; sign in if needed
inspect controls -> save 'form-before.json'
apply re-rendering choices first, then fill text fields with verification
inspect again -> save 'form-after.json'; save full-page screenshot
if submit flag is set:
  run pre-submit gate; refuse and exit if it fails
  click the exact final button by its visible name
  wait, then save a post-submit screenshot and check for confirmation
close browser
```

### Pre-submit readiness gate

Re-inspect the full page. Submit only if all are true:

- [ ] Correct account, organization, and environment.
- [ ] Correct target item.
- [ ] Every required field is non-empty.
- [ ] Each value matches the intended content closely enough.
- [ ] Dropdowns, checkboxes, dates, recipients, and attachments are correct.
- [ ] No validation errors, warnings, or unsaved-change notices remain.
- [ ] The button about to be clicked does what you expect and is not a similar-looking destructive option.

**If any required field is empty, do not submit.** This is not negotiable. A partly filled form can be fixed; a wrong submission often cannot.

A confirmation request for an irreversible action should state the target, key values, recipients or audience, any cost, what cannot be undone, and any open questions.

### Worked example (fictional)

An assistant fills a grant application for the fictional Harbor Lane Arts Collective on the fictional Northwind Foundation portal. Inspection finds: Project title (single-line, required), Summary (rich-text editor, required, with a hidden sync input beside it), Category (dropdown that re-renders the form), and Start date (picker). The plan: choose Category first, set the date, fill Summary in the visible editor with keyboard input and blur, then fill the title. Read-back shows Summary at 412 of 415 characters (the editor collapsed double blank lines, acceptable and noted) and Title at 0 of 38. A retry with keyboard input gives 38 of 38. The date is re-checked and still correct. The page says entries cannot be edited after submission, so the assistant saves a screenshot and asks: "Ready to submit the Harbor Lane application to Northwind under Community Arts, starting 1 March. It cannot be edited afterward. Submit?"

## 10. Confirm completion

A click is not proof of success. Look for real evidence: a success message, a confirmation reference, a new record, a setting that persists after a safe reload, or a sent or published item.

- **Errors can be cosmetic.** Some apps show "something went wrong" after the work actually finished. Inspect the result before retrying, because blind retries can create duplicate messages, payments, or records.
- **Frozen pages.** A blocking pop-up dialog can freeze the tab so clicks and screenshots time out. Ask the user to respond to it, then continue. Where possible, confirm the outcome through an independent channel, such as a public lookup or an API read.
- If you cannot confirm completion, say what you tried, what evidence exists, and what remains uncertain. Never report an attempt as a success.

## 11. General failure patterns

| Symptom | Likely cause | Safe response |
|---|---|---|
| Fill reports success but the field is blank | App model ignored a direct write | Keyboard-style input, blur, read back. |
| Earlier fields blank out as later ones are filled | Re-render rebuilt editors from stale state | Blur after each fill; do re-rendering choices first. |
| A dropdown choice wipes the form | Selection triggers a full re-render | Make choices before filling text; re-verify. |
| Field looks filled but validation says empty | Hidden sync field was edited | Fill the visible editor the app reads. |
| Locator returns an empty wrapper | Accessible name sits on a different element | Follow the label relationship to the real editor. |
| Interactive tool crashes on long text or parallel calls | Tool layer is unstable for heavy work | Switch to a standalone script. |
| Headless page differs from a normal browser | Site varies by browser context | Prefer a direct interface; escalate only for an explicit task, never evade protections. |
| Wrong account or profile opened | Generic selector picked the last-used profile | Classify context, select the profile directly, verify the account. |
| Session ends after a page-script request | Internal endpoint called without the app's normal headers | Drive the UI or use a supported API. |
| A warning or security page appears that the tool cannot read or click | The page sits outside the automation's reach or needs a person | Ask the user to handle it, then continue and re-verify. |

## 12. Report results

Summarize the outcome in one or two sentences, point to the screenshot and the after-state record, and offer to open the screenshot. Do not paste every field value as a large inline table. Store artifacts only where the user can appropriately access them, and delete temporary files with sensitive content when no longer needed.

## 13. Keep the procedure current

When a run reveals a reusable lesson, such as a new failure mode, a working pattern, or a missing capability, add it to your local copy of this procedure. Prefer a single table row with symptom, cause, and fix over new prose. Never record credentials, account identifiers, personal details, or private site data. When the document grows long, merge older entries into general principles instead of appending incident history. Tool paths, versions, profile mappings, and notes about how a particular app behaves go stale, so update them in place and re-verify them.

## Final audit checklist

- [ ] The least invasive suitable route was used.
- [ ] Visible-browser use was announced and kept to a fresh window or tab.
- [ ] Account, environment, and target were verified before any write.
- [ ] Controls were inspected before editing and addressed by label, not position.
- [ ] Every meaningful change was read back.
- [ ] The pre-submit gate passed, with no empty required fields.
- [ ] Irreversible actions had a pre-action record and authorization.
- [ ] Credentials were entered by the user, not moved through automation.
- [ ] Success was confirmed with evidence after acting.
- [ ] The report separates confirmed results from uncertainty and exposes no secrets.

## Optional extras

**Clipboard and rich paste.** Headless browsers often lack clipboard permission, so embed values directly instead. When rich content (such as text with links) must be inserted, a synthetic paste event carrying both rich and plain text works in some editors and is ignored by others, which may offer their own conversion method. Verify the result, ideally through the service's API or an export rather than the screen alone.

**Drag and drop.** Dragging can create unwanted layout changes or trigger a clickable element by accident. Prefer keyboard move commands with short waits, then verify the final structure.

**Parallel work.** When many independent items are needed, separate tabs or sessions each given the full brief keep one item from biasing the next. Keep concurrency to a small number you choose, since too many tends to stall. Background tabs may not render at full size, so bring an item into view before capturing it and clean up temporary tabs afterward.

**Devices on the user's own network.** Local devices often serve unencrypted pages, and a browser set to prefer secure connections may show a warning first that automation cannot handle. Continue past it only for devices the user owns and asked you to work on, through the browser's own proceed option or by asking the user, and never for public sites. Use the same address the user normally signs in at, since sign-in sessions are tied to it, and check the device's own settings for an authenticated route to companion services before asking for extra tokens.

**Apps without an API.** When a workflow builder or automation editor has no bulk-edit screen or API:

- Read configuration from state the page already holds in memory, with no network calls. These internal layouts are undocumented and change between versions, so probe for the current location, and if a read suddenly returns nothing, assume the layout moved before assuming the data is gone.
- Make changes through the editor's own UI or paste support, test with a read-only step before anything that writes, then save and re-read to confirm the change persisted.
- After renaming or deleting fields or sources, open each automation in turn and check for configuration warnings, script steps that reference names rather than internal IDs, and the latest run status. Report confirmed breakage separately from items that need a manual check.
- If a page-script loop outlasts your tool's time limit, start it without waiting, store results in a page variable, and poll for them in later calls.


---
name: create-a-skill
description: Designs, tests, and improves a reusable AI skill from a rough idea or repeated workflow. Use when someone says "turn this into a skill," "improve this skill," or "does my skill help?"
---

# Create an AI skill

Use this workflow to create a new AI skill, improve an existing one, test whether a skill actually helps, or tune when it activates. A skill is a focused set of instructions, plus optional scripts, reference documents, and templates, that helps an AI do a recurring job well and consistently.

## Quick version

- Tell your assistant what the skill should do, when it should be used, and what a good output looks like. If you already did the job in a conversation, paste it and ask the assistant to extract the steps, corrections, and formats, then confirm the gaps.
- Before drafting, have it ask only questions that change the design: missing information, edge cases, actions that need your confirmation, and what would make you reject an output.
- Draft the skill: a short name, a slightly assertive description that leads with trigger phrases, imperative instructions that explain why each step matters, an output template, and what to do when something is missing or unclear.
- Write two or three realistic test requests. Paste the skill into a fresh chat with each one and read the outputs yourself before changing anything.
- Revise from the general cause of each problem, not the specific example. Fold each lesson into the rule it refines instead of appending notes about what went wrong.
- Repeat until you are happy or progress stops, then run the audit checklist in section 10.

The method works with any AI system that supports reusable instructions. Where this guide mentions files, folders, or tools, substitute whatever your platform provides.

## 1. Work out where the user is

The core loop:

1. Understand what the skill should do and roughly how.
2. Write or revise a draft.
3. Run the AI, with the skill available, on a few realistic test requests.
4. Help the user judge the results by reading outputs and, where useful, by measuring objective checks.
5. Revise the skill from that evidence.
6. Repeat until the user is satisfied or progress stops.
7. If the skill matters enough, expand the test set and try again at larger scale.
8. Optionally tune the description so the skill activates for the right requests.
9. Package and hand off the skill.

Your first job is to find the user's place in this loop and help them take the next step. Stay flexible about order and depth: someone who says "skip the formal evaluation, just work on it with me" should get that.

| Situation | What to do first |
|---|---|
| New idea ("a skill for X") | Capture intent, interview, draft |
| Existing draft or installed skill | Read it fully, then go to testing and revision. Keep its name unless the user asks to rename it |
| Workflow already shown in the conversation ("turn this into a skill") | Extract the workflow from the conversation, then confirm gaps |
| "Does this skill actually help?" | Go straight to test design and evaluation. Do not rewrite just because you can |

When extracting from a conversation, pull out the tools and sources used, the sequence of steps, corrections the user made, input and output formats, and conditions that changed the approach. Summarize this, ask the user to fill gaps, and get confirmation before moving on. Do not quietly turn a one-time workaround into a general rule.

If you have a task list, add the loop steps to it, including "show test outputs to the user before revising". That step is the one most often skipped.

## 2. Communicate at the right level

Users range from experienced developers to people who have never used a command line. Read context cues and adjust.

- Words like "evaluation" and "benchmark" are usually fine.
- Words like "JSON", "assertion", "baseline", and "schema" need clear signs that the user knows them. Otherwise add a short definition the first time.
- When in doubt, explain briefly. It costs little.

Keep the user involved at decision points: confirm scope before writing a lot, share test prompts before relying on them, and let human judgment settle subjective questions such as tone, design, and usefulness.

## 3. Capture intent

Make sure you can answer these questions:

1. What should the skill enable the AI to do?
2. When should it activate? Which user phrases or situations?
3. What is the expected output: a chat reply, a file, a change to a file, an external action?
4. Should we build test cases to check that it works?

For question 4, suggest a default based on the skill type and let the user decide. Skills with objectively checkable outputs (file conversions, data extraction, code generation, fixed workflow steps) benefit from test cases with checks. Skills with subjective outputs (writing style, visual design) usually need human review more than numerical checks.

## 4. Interview and research

Ask about edge cases, input and output formats, example files, success criteria, permissions, and dependencies. Hold off on writing test prompts until these are settled. Useful question formats:

- "If information is missing, should the skill ask, make a labeled assumption, or produce a draft marked incomplete?"
- "Should it work with any source you give it, or only specific approved sources?"
- "Does any action need your confirmation because it is external, irreversible, or high impact?"
- "What would make you reject an output?"
- "Who will use this skill, and what can they already be assumed to know?"

If you can search documentation or look up similar skills and good practices, do that before asking the user things you could find yourself. If sources conflict or requirements stay unclear, say so instead of inventing a rule.

## 5. Choose the structure

A typical skill package looks like this. Use your platform's naming conventions:

```text
skill-name/
├── [main instruction file]   # required: name, description, instructions
├── scripts/                  # optional: code for deterministic or repetitive tasks
├── references/               # optional: documents loaded only when needed
└── assets/                   # optional: files used in outputs (templates, icons, fonts)
```

Most skill systems load content in layers, so design for progressive disclosure:

| Layer | Content | When loaded | Size guide |
|---|---|---|---|
| 1. Metadata | Name and description | Always visible to the AI | A sentence or two |
| 2. Main instructions | The body of the skill | Whenever the skill activates | Short enough to read in one pass; a few hundred lines at most |
| 3. Bundled resources | Scripts, references, assets | Only when needed | Can be large; scripts can run without being read |

Follow any limits your platform sets. If it sets none, choose a size limit for the main file yourself (adjustable) and check against it whenever you edit. Key patterns:

- If the main instructions grow long, move detail into reference files and say exactly when to read each one.
- Give long reference files a table of contents.
- When a skill supports several variants (for example, deploying to different hosting providers), keep the shared workflow and variant selection in the main file and put each variant in its own reference file.
- Split unrelated jobs into separate skills when they have different audiences, permissions, sources of truth, or definitions of done.

## 6. Write the skill

### Required parts

- **Name:** a short, stable identifier.
- **Description:** what the skill does and when to use it. This usually decides whether the AI uses the skill, so put all "when to use" information here, not in the body.
- **Compatibility (optional):** required tools or dependencies, only if they are not obvious.
- **Instructions:** the body.

### Writing the description

AI systems often under-use skills. Counter this by making descriptions slightly assertive. Instead of "How to build a quick inventory dashboard", write "How to build a quick inventory dashboard. Use this whenever the user mentions dashboards, stock-level charts, operational metrics, or wants to see warehouse data visually, even if they don't say 'dashboard'."

- Keep it short. Respect your platform's length limit; if there is none, one or two sentences is a good default.
- Lead with the phrases and situations that should trigger it, including cases where the user implies the job without naming it.
- Add scope limits only where false activation would be costly.
- Do not put the workflow itself in the description.

If the platform offers different ways to reach a skill, such as automatic activation, grouping under a routing skill, or manual invocation by name, ask which fits. A sensible default is automatic for general workflows and manual for command-style skills. If many skills share one area, grouping keeps the always-visible list manageable. After adding, renaming, or removing a skill, run whatever registration or validation step the platform provides.

### Safety: no surprises

A skill must not contain malware, exploit code, or anything that compromises security. Its contents should not surprise the user given its description. Decline to build misleading skills or skills meant for unauthorized access, data extraction, or other harm. Ordinary creative uses, such as a role-play persona, are fine.

### Writing style

- Use the imperative form.
- Explain why things matter instead of stacking unexplained commands. If you find yourself writing ALWAYS or NEVER in capitals, treat it as a warning sign and explain the reason instead. Keep firm rules for authorization, privacy, safety, data integrity, and irreversible actions.
- Write for general use, not for the specific examples you have in mind.
- Write a draft, then reread it with fresh eyes and improve it.

### Useful patterns

Define output formats when consistency matters:

```markdown
## Report structure
Use this template:
# [Title]
## Executive summary
## Key findings
## Recommendations
```

Include examples when they teach something:

```markdown
## Commit message format
Example:
Input: Fixed rounding error in invoice totals
Output: fix(billing): correct invoice total rounding
```

Also cover, as needed: required inputs and what to do if they are missing; the normal workflow and its branches; checks to run before finishing; and failure behavior for unavailable tools, ambiguous requests, failed validation, and high-impact actions that need confirmation.

## 7. Write test cases

After the draft, write two or three realistic test prompts, the kind of thing a real user would type. Share them, for example: "Here are three requests I plan to test with. Do they look like what you'd really ask, or should we add one?"

Cover meaningful variety: a typical request, an incomplete or ambiguous one, a format-sensitive one, and, if relevant, one that should lead to a confirmation or refusal. Give each test a descriptive name. Leave checks empty for now; draft them while runs are in progress.

```json
{
  "skill_name": "[skill name]",
  "tests": [
    {
      "id": "[descriptive-test-name]",
      "prompt": "[the user's task prompt]",
      "expected_output": "[description of expected result]",
      "files": [],
      "checks": []
    }
  ]
}
```

## 8. Run and review the tests

Treat this as one continuous sequence. Do not stop partway.

1. **Run each test** with the skill available. In a plain chat, paste the skill and one test prompt into a fresh conversation, or follow the skill yourself. Call this a sanity check, not a rigorous comparison, since the author is also the runner. If you can run independent helpers with baselines, see Optional extras.
2. **Draft checks while you wait.** Good checks are objectively verifiable and have descriptive names that make sense at a glance: required sections are present; the produced file opens; totals match the source; missing inputs are flagged. Do not force checks onto subjective qualities; those need human review. If checks already exist, explain what they verify and adjust if needed.
3. **Grade each output** against its checks. For checks a script can verify, write and run a script; it is faster, more reliable, and reusable. Record the check text, pass or fail, and evidence.
4. **Present results to the user before you start fixing things yourself.** For each test, show the prompt and output, save any file the user must inspect and say where it is, and ask: "How does this look? Anything you'd change?"
5. **Read the feedback.** Empty feedback usually means the output was fine, though it is not proof the skill is complete. Focus on tests with specific complaints.

## 9. Improve the skill

This is the heart of the loop. Take your time. Draft a revision, then reread it fresh and improve it.

1. **Generalize from feedback.** The skill will be used many times on many different requests. You iterate on a few examples only because it is fast; a skill that works only for those is useless. Avoid narrow, overfitted fixes and oppressive rules. If a problem persists, try a different framing, metaphor, or working pattern.
2. **Keep it lean.** Remove what is not earning its place. Read the run transcripts, not just final outputs. If the skill makes the AI waste effort, remove the cause and see what happens.
3. **Explain the why.** Even if feedback is terse or frustrated, work out what the user actually needs and put that understanding into the instructions.
4. **Bundle repeated work.** If several runs independently wrote similar helper scripts or followed the same multi-step routine, write it once, add it to the skill, and tell the skill to use it.
5. **Fold lessons into existing rules.** When a run teaches a lesson, edit or merge the rule it refines instead of adding a new paragraph about the incident. Do not append dated incident notes to the skill. If you want an audit trail, keep it in a separate change log that the skill does not load when it runs.
6. **Preserve what works.** Do not break behavior the user already liked while fixing something else.

Then rerun all tests as a new iteration, show the new results with previous outputs and feedback alongside, wait for the user to finish reviewing, and repeat. Stop when the user is happy, feedback is consistently empty across meaningful tests, or you are no longer making meaningful progress.

## 10. Package and hand off

If a packaging tool is available, package the skill in the user's chosen format and say where the result is. Include only resources needed for normal use. When updating an installed skill, keep the original name and folder name; do not create a "v2" copy unless the user asks.

Pre-delivery audit:

- [ ] Name is stable and appropriate.
- [ ] Description states what the skill does and when to use it, within the platform's limits.
- [ ] Main file is within the size limit, and any validation step passes.
- [ ] Lessons are merged into rules, with no appended incident notes.
- [ ] Instructions do not depend on undeclared tools, private conventions, or personal access.
- [ ] Every bundled resource is referenced, clearly named, and explained.
- [ ] No credentials, private identifiers, confidential records, or sensitive examples are included.
- [ ] Any retained tests are safe to distribute.
- [ ] If the skill will be shared in a collection, the decision to include or exclude it is recorded, it has passed privacy and quality review, and any public identifier stays stable (keep old identifiers as aliases if renamed).

Give a short handoff note: what the skill does, required capabilities, known limits, and a quick way to test it.

**Readiness gate:** a skill is ready when it has a clear job, a description that routes the right requests to it, instructions that handle normal variation, explicit boundaries for uncertainty and authorization, and evidence from realistic tests that it improves outcomes. A long file is not the same as a reliable skill.

## 11. Avoid common failure modes

| Failure | Fix |
|---|---|
| Revising before the user has seen any outputs | Present results for human review first |
| Fixes tailored to the test examples | Find the general cause and fix that |
| Incident notes piling up at the end of the skill | Merge each lesson into the rule it refines; keep history in a separate log |
| Many capitalized absolute rules | Replace with explained reasoning, except for true hard boundaries |
| Vague or timid description, so the skill is rarely used | Lead with trigger phrases and name implied use cases |
| Checks that pass with or without the skill | Replace with checks that show the skill's added value |
| Calling a self-run sanity check a rigorous comparison | Label it honestly |
| Assuming one person's tools, limits, or conventions | Ask the user for their platform's rules and use those |

## Optional extras

### Parallel runs with baselines

If you can run independent helper agents, launch a with-skill run and a baseline run for every test in the same round, so they finish around the same time under similar conditions. For a new skill, the baseline is the same prompt with no skill. When improving a skill, snapshot it before editing and point the baseline at the snapshot. In later iterations, say whether the baseline is the original version or the previous iteration.

```text
[skill-name]-workspace/
├── skill-snapshot/
├── iteration-1/
│   ├── [test-name]/
│   │   ├── with-skill/
│   │   ├── baseline/
│   │   └── [test details, run data, grades]
│   └── [benchmark summary]
└── iteration-2/
```

Run instructions template:

```text
Execute this task:
- Skill location: [path to skill, or "none" for a no-skill baseline]
- Task: [test prompt]
- Input files: [files, or "none"]
- Save outputs to: [workspace]/iteration-[N]/[test-name]/[with-skill or baseline]/
- Outputs to save: [what the user cares about, e.g. "the final spreadsheet"]
```

If the environment reports time or resource use when a run finishes, save it immediately; some environments report it only once. Keep grade field names consistent so any review tool can read them:

```json
{
  "results": [
    {
      "text": "Flags missing source data in an assumptions section",
      "passed": true,
      "evidence": "Final section lists the two unavailable figures and asks for them."
    }
  ]
}
```

Aggregate into a benchmark: pass rate, time, and resource use per configuration, with average, spread, and the with-skill versus baseline difference, each with-skill result next to its baseline. Then analyze what totals hide: checks that pass either way, high variation that suggests flaky tests or unclear instructions, quality gains that cost too much time, and failures that share one root cause.

A good review view, using an existing tool rather than a custom build, has an Outputs view (prompt, rendered output, previous output, grades, feedback box, earlier feedback) and a Benchmark view (numbers with per-test breakdowns and notes). Without a display, write a standalone file the user can open.

### Blind comparison

When the user asks "is the new version actually better?" and wants rigor, give two outputs to an independent evaluator without saying which version produced which. Judge against a shared rubric: correctness, completeness, clarity, constraint adherence, and usability. Then analyze why the winner won. Human review is usually enough.

### Tune the description for activation

Do this after the skill works and the user agrees it is in good shape. Write about 20 queries, a roughly even mix of should-activate and should-not-activate:

```json
[
  {"query": "[realistic user prompt]", "should_trigger": true},
  {"query": "[near-miss prompt]", "should_trigger": false}
]
```

Make them realistic and detailed, with varied lengths, casual phrasing, and occasional typos.

- Weak: "Format this data", "Make a chart".
- Strong: "ok so my team lead dropped a csv in the shared drive (something like 'march orders cleaned v3') and wants a column with the discount as a percent of list price. list price is column B and paid amount is E i think".

Should-activate queries should vary phrasing, include requests that never name the skill but clearly need it, and include cases where this skill competes with another and should win. Should-not-activate queries should be near-misses that share keywords but need something different; obviously irrelevant negatives test nothing. AIs usually consult skills only for tasks they cannot easily do alone, so use substantive queries.

Have the user review and edit the set; bad queries produce bad descriptions. If automated activation testing exists, run it in the background with progress updates. A sound loop holds out about 40 percent of queries, runs each query several times, proposes improvements from failures, re-tests for a few rounds, and picks the winner by held-out score. Test with the model the user actually works with. Otherwise, walk through the set manually. Show the before and after and report the scores.

### Adapt to your environment

| Capability missing | Adaptation |
|---|---|
| Independent helper agents | Run tests yourself one at a time; skip baselines, benchmarks, and blind comparison |
| Automated activation testing | Review the query set manually against the description |
| Parallel runs keep failing or timing out | Run tests in sequence |
| Write access to the installed skill | Copy it to a writable location, edit there, and package from the copy |


---
name: test-every-screen-size
description: Check every UI or CSS change across narrow, wide, short, and tall screens with screenshots and layout checks before calling it done. Use before shipping any front-end change.
---

# Test every screen size

Run this workflow after any UI, visual, or CSS change and before requesting review, publishing, or calling the work complete. Small edits to spacing, backgrounds, or sizing can create overflow, blank areas, wrapping problems, or collisions at sizes that were not inspected.

A layout passes only when **both** screenshots and programmatic checks pass. Measurements can miss visual defects; screenshots can miss off-screen overflow or unusable controls.

## 1. Prepare a representative state

Use an authorized test environment and test only the minimum data needed to reproduce normal use. Populate the changed surface with realistic content, such as long text, representative lists or cards, field values, and validation messages. Include loading, empty, or error states when the change affects them.

Do not test only an empty or unusually sparse page. Sparse states often conceal clipping, overlap, and unwanted blank space.

## 2. Select the viewport sweep

Use a repeatable browser-testing system. Start with these widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a wide desktop size, such as 1920 px, when large displays are a supported use case. Include any known target viewport.

When vertical behavior matters, test both a short and tall height, for example about 700 px and 1400 px or more. Explicitly include a very tall viewport for changes involving viewport-height sizing, flexible page shells, backgrounds, vertical padding, sticky footers, or bottom alignment.

## 3. Capture and inspect screenshots

Capture screenshots for each relevant viewport and state. Use visible-viewport screenshots for sticky, fixed, and viewport-height behavior; use full-page screenshots when page flow, backgrounds, or total page length matter.

Inspect the changed surface on all four sides: top, right, bottom, and left. Compare the result with the requested outcome, not merely with the edited CSS.

Give extra attention to full-bleed or edge-to-edge changes. Removing containment on one edge can reveal leftover wrapper margin or padding as an unintended strip on another edge.

## 4. Run programmatic layout checks

At every relevant viewport, verify that:

- there is no unintended horizontal overflow;
- viewport-fitting screens do not have unintended vertical overflow, allowing a small rendering tolerance;
- changed elements do not overlap adjacent content or escape their intended containers;
- buttons, links, fields, cards, and lists remain visible and usable;
- fixed or sticky elements do not hide required content; and
- prose remains readable rather than becoming excessively wide.

For prose, use an approximate warning threshold of 80 characters per line; reading-focused layouts commonly target about 60–70 characters per line. Check relevant bounding rectangles for overlaps and compare document height with viewport height where fitting the viewport is intended.

## 5. Resolve failures and retest

If any viewport or state fails, stop the completion process. Find the underlying layout rule, fix that behavior, and rerun the relevant sweep. Do not add a size-specific patch merely to make one screenshot pass.

If a fix improves one size but breaks another, revisit the diagnosis. The layout model or component constraints are incomplete.

## 6. Readiness gate and report

Do not report only that the interface works on “mobile and desktop.” State what was tested and what passed. For example:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall heights where relevant; screenshots and layout checks found no unintended overflow or overlap; controls remain usable.

If a viewport, state, or check was not run, state that clearly and do not represent the UI change as fully verified.


---
name: recurring-events
description: Sets up the next date of a recurring community event: fresh poster, event page, and invites to opted-in past guests. Use when someone says set up this week's event or post the next one.
---

# Run a recurring community event

Use this when you host a regular event, such as a monthly book swap or game night, and want the assistant to set up the next one: date, fresh poster, event page, and invites, with as few questions as possible.

## Quick version

- Tell the assistant the series name, the rule for when it happens (for example "first Thursday of each month"), the last event number, and any dates that already have an event.
- Ask it to work out the next open date with a real calendar, not in its head.
- Have it reuse last time's description and update only what changed.
- Ask for one fresh poster idea that is clearly different from the last few, written as a single-paragraph image prompt.
- Paste the finished text into your event page yourself, check it as a guest would, and mark yourself as going if that is your habit.
- Invite the usual people, then check the invite count before and after sending.

## Authorization: confirm once, then act

For your own series, standing authorization is the natural default. Confirm it once, in writing, with the series, the usual hosts, who gets invited, and what the assistant may publish and send. After that, each new occurrence should need zero questions. Stop and ask only when something real changes: a new venue, a price, a bigger or different audience, a public listing, or a safety issue.

The invite step reads past guest lists, so use them only to invite people to this series, and only people who agreed to hear about future events, such as past guests who have not opted out. Read only the lists you need, leave out unrelated personal details, keep any names and counts inside the host team, and make opting out easy.

## 1. Work out the date and number

- Compute the next date from the recurrence rule with a calendar or date tool. Weekday and date errors are the most common mistake.
- Check the list of events you already host before picking dates, and skip any date that already has one. A request for "three new ones" means the next three open dates.
- Find the highest existing event number and add one. For several events, use sequential numbers, each with its own poster.
- Check for clashes: a holiday, the venue being closed, or the host being away. A clash does not cancel the event by itself. Go ahead under the standing policy and name the clash in the final report so the host can hand off or cancel.

## 2. Make a fresh poster

Look at the last two or three posters first so you do not repeat them. Keep the series identity steady (the name in the same hand-lettered style, the core activity, a warm and simple look) and change the big idea each time.

Levers worth pulling:

- **Season, weather, light:** first frost, a rainy window, long summer evening light.
- **Viewpoint:** looking up past a teacup, a bird's-eye view of the table, a view from inside a bookshelf.
- **One witty focal object:** a chess knight wearing a party hat, a stack of paperbacks shaped like a lighthouse, a dice cup used as a flowerpot.
- **Local texture:** a familiar street corner, the venue's door, a local landmark.

One clear joke beats a busy scene.

Anti-cliché guardrails to put in the prompt:

- one clear subject and a restrained palette;
- clean, correctly spelled lettering;
- no extra fingers, melted objects, or garbled text;
- no glossy over-rendered finish or generic "epic" lighting.

If the result looks like last time or has obvious generated tells, say so and regenerate once or twice.

Practical rules for the image tool:

- **Write the prompt as one paragraph.** In many chat tools Enter sends the message, so a multi-line prompt gets cut off. If that happens, stop and send the rest as a follow-up.
- **Check before retrying.** Image tools sometimes show an error even though the image finished.
- **Use the account with enough image capacity.** Free or limited plans can run out after a few images, leaving no room to regenerate. If you have access to a workspace or plan with higher limits, pick it in the account menu before you start. When you need several posters, send every prompt at once in separate fresh chats.

## 3. Build the event page

Reuse the stable parts of the last description and update the rest. Fill fields in this order, because date pickers are often fragile:

1. Title, using the series pattern, such as "Book Swap #N".
2. Date, start and end time. Check the shown date before touching anything else.
3. Location, picking the exact venue, not a similar name.
4. Description.
5. Image. Wait for the upload to finish and check it shows.
6. Co-hosts, if any.
7. Leave visibility, cost, and capacity at the series defaults.

Some platforms publish on a button labeled "Save" or "Done," so know what it does before pressing it. Then check the live page as a guest would: title, date, time, location, description, and image.

If the host wants it (a choice you set once), RSVP as the host: mark yourself as going, leave plus-ones and comments empty, close any follow-up prompts, and confirm the page shows one person going.

## 4. Invite the approved audience

Invite past guests of the series, one past event at a time, including any early unnumbered events. Before pressing "Select all," check whether people are already selected, because pressing it again can clear them. Watch the invite count rise after each group. If it stays flat or drops, stop and look. Send, then confirm the sent state and final count.

## 5. Report

Keep it short: what was created, date and venue, the invite count, any clash from step 1, and the live link as the last line.

## Worked example (invented)

Series: "Second Saturday Board Games," monthly, at a neighborhood café, hosts Priya and Tom, invite list is past guests who have not opted out. The host has asked to be marked as going on each new event.

- Last event was #11 in March. A calendar check gives Saturday 12 April, so this is #12. The hosting list shows no event on that date yet.
- The café closes early that day. Under the standing policy the assistant keeps the usual slot and flags the clash.
- Last two posters were a meeple on a mountain and a rainy window with cards. This time: a bird's-eye view of a game board laid out like a city park, with a single tiny meeple walking a dog. Warm colors, hand-lettered title, nothing else in frame.
- Description carries over unchanged except the date and a new line: "Bring a game you have not played in a year."
- After publishing, the assistant RSVPs as Priya and the page shows "1 going."
- Invites: 11 past sessions, count rises from 0 to 46 with no drops. Sent.

Report: "Board Games #12 is live for Sat 12 April at the café. 46 people invited. Note: the café may close early that day, so you may want to confirm the time with them." Link on the final line.

If Priya later asks for "three more" and #13 already exists for May, the new ones become #14, #15, and #16 on the June, July, and August dates.

## After each run

Keep only reusable lessons, such as platform quirks or a changed template, and update your notes in the same session.

## Optional extras

For assistants that drive a browser or other connected tools:

- **Right account for each site:** the image tool and the event platform may be logged in under different browser profiles or accounts, and one account may have several workspaces with different limits. Route each site to the right profile and workspace, and verify the active account before acting.
- **File handling:** avoid buttons that open a native file dialog the tool cannot control; use the page's file input or the tool's file-chooser support, from a folder the tool can read. If a browser silently blocks a second download, capture the image another way, such as a full-size screenshot of just the image.
- **Verify after every change on screen:** pages shift when extra controls appear, windows resize, or a page is still loading. Take a fresh screenshot before each click after any shift, confirm nothing changed by accident (a style, a date, a selection), and close pickers by clicking empty background rather than trusting close icons or Escape.
- **One thing at a time:** finish and verify an upload before opening another panel. If you script the invite loop, handle one past event per call to stay under time limits, normalize unusual spaces in labels before matching text, wait for each list to load, and read the invite count after each pass.
- **Shared notes:** keep series-specific quirks with this workflow and move general browser lessons into a shared notes file.

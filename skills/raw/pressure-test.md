---
name: pressure-test
description: Finds the weak points in a strategic idea before you commit, through a steelman, assumption tests, a pre-mortem, and a verdict. Use when someone says pressure-test this, stress-test this, or am I wrong.
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

---
name: pressure-test
description: Find weak points in a leading strategic idea before commitment by steelmanning the case, testing its load-bearing assumptions through sequential challenge, and ending with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Input

Provide a claim, decision, or direction to test. Include available evidence and context, or state what is unknown.

**Input format**

> **Idea to test:** [Proposed action or decision]
>
> **Why now:** [Trigger, opportunity, or problem]
>
> **Expected outcome:** [Result, for whom, and by when]
>
> **Evidence available:** [Metrics, research, experiments, feedback, or prior decisions]
>
> **Constraints and stakes:** [Budget, time, dependencies, reversibility, or consequences]
>
> **Alternatives considered:** [Options, including doing nothing]

If internal records or communications are relevant, access them only for a legitimate purpose and with clear authorization. Use the minimum relevant sources and information. Do not include unrelated personal, confidential, or sensitive details in the analysis or output.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gate:** If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early often becomes an exercise in defending it.

If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.

## Rules of engagement

- Be direct. Confidence is not evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask one forcing question at a time. Wait for an answer, assess it, and challenge vague, unsupported, or evasive answers before moving on.
- Distinguish facts, inferences, forecasts, and unknowns.
- Cite or link to available evidence when appropriate. Identify contradictions between the claim and the evidence.
- Refer to dissenters by relevant role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent anyone's views.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's actual intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If a stronger restatement changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold for the claim to work. Rank them by damage if wrong, with the most decision-threatening assumption first. Make assumptions observable where possible.

| Rank | Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|---|
| 1 | [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Test or disproof method] |

Replace vague claims such as “users will value this” with a behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Start with the highest-risk assumption. Adapt later questions to prior answers; do not present the full set as a questionnaire, because that enables selective answers.

For each question, use this loop:

1. Ask one question.
2. Wait for the answer.
3. Classify the answer as evidence, inference, forecast, or unknown.
4. If it is vague, unsupported, or avoids the issue, ask a focused follow-up before continuing.
5. Record what the answer changes: confidence, assumption rank, needed test, or verdict risk.

Draw from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would happen in the next 30 or 90 days that would show this is wrong?
- **Counterfactual:** What similar attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that role say, and has that concern been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or disruption?
- **Null option:** What happens if no action is taken for the next three months?

“I think it will work” is not evidence. Ask for observed behavior, data, a comparison, or a credible commitment.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include a wrong underlying premise, execution risks, and external conditions where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or accountable role |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Observable signal] | [Check or accountable role] |

Warning signs must appear early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If that perspective has not been sought, mark it as an evidence gap; silence is not agreement.

| Relevant role | Strongest likely objection | Heard directly? | Gap-closing action |
|---|---|---|---|
| [Role] | [Objection] | [Yes, no, or unknown] | [Action] |

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test incomplete or failed rather than approving it.

## 7. Give a verdict and handoff

Choose one verdict and state the next step explicitly:

- **GREEN: Proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** One or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as targeted interviews, an expert review, a prototype, or a short data-collection period. Run that test, then decide with its result recorded.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, downside is unacceptable, or no meaningful falsification criterion can be named. Generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

Use this closing format:

> **Verdict:** [GREEN, AMBER, or RED]
>
> **Reason:** [The deciding evidence, assumption, or gap]
>
> **Next workflow step:** [Decide, test, generate alternatives, redesign, or defer]
>
> **Concrete next action:** [Owner] will [verb and specific action] by [date or decision point].

End with exactly one concrete next action containing a verb, an owner, and, when useful, a deadline.

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

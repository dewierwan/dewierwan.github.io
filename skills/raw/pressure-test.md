---
name: pressure-test
description: Find the weak points in a leading strategic idea before committing to it. Steelman the case, test its load-bearing assumptions through sequential challenge, and finish with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor proportionate to its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one option too early often becomes an exercise in defending it.
- If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.
- If the idea depends on private communications, records, or personal information, confirm a legitimate purpose and authorization. Use only the minimum relevant information, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

## Rules of engagement

- Be direct. Do not mistake confidence, seniority, or enthusiasm for evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Ask **one forcing question at a time**. Wait for the answer, assess it, and push back on vague, unsupported, or evasive responses before moving on.
- Use available evidence, such as research, metrics, prior experiments, customer feedback, documented decisions, or authorized stakeholder input. Separate facts, inferences, and forecasts.
- Refer to likely dissenters by relevant role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Keep the process terse. If a section is not useful for this claim, state `Skipping: not applicable because [reason]` and continue.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and proceed. If strengthening the wording changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions the claim depends on. Rank them by the damage caused if they are wrong, with the most damaging first. Make each assumption observable where possible.

| Rank | Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|---|
| 1 | [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [How to test or disprove it] |

Replace broad statements such as “users will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Choose questions based on the highest-risk assumptions, then adapt later questions to the answers received. Do not present the full set as a questionnaire, because that permits selective answering.

Possible question categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Counterfactual:** What comparable attempt failed, and why is this case materially different?
- **Opportunity cost:** What is the best valuable work that will not happen if resources go here?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say? Has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specifics. “I think it will work” is not evidence. Ask which observed behavior, data, comparison, or commitment supports the belief. If the answer remains weak, record the gap rather than moving past it.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, usually 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failures, external changes, and failure of the underlying premise where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or accountable role |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable early signal] | [Name the check or accountable role] |

Warning signs must appear early enough to permit a course correction.

## 5. Surface credible dissent

Identify two or three roles that could reasonably disagree and state each role's strongest likely objection. If those perspectives have not been sought, mark this as an evidence gap. Do not interpret silence as agreement.

| Relevant role | Strongest likely objection | Heard directly? | Gap-closing action |
|---|---|---|---|
| [Role] | [Objection] | [Yes, no, or uncertain] | [Action] |

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than approving the idea.

## 7. Give a verdict and handoff

Choose one verdict and name the next workflow step.

- **GREEN: Proceed to decision.** The steelman survives; core assumptions have credible support; relevant dissent has been addressed; reversal costs are understood; and warning signs have monitoring ownership. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER: Test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data collection period. Next: complete that test, then make the decision with the result recorded. Do not commit while the gap remains open.
- **RED: Stop, redesign, or reopen options.** A core assumption is weak, the downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with **one concrete next action** in one line: a verb, an owner, and a deadline when useful.

Example: `Research owner: interview five target users this week and compare the results with the adoption assumption.`

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

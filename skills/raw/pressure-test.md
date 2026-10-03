---
name: pressure-test
description: Find weak points in a leading strategic idea before committing: steelman the case, test its load-bearing assumptions through sequential challenge, and end with a clear verdict, handoff, and concrete next action.
---

# Pressure-test an idea

Use this workflow when a decision-maker is leaning toward a strategic direction and needs an honest challenge before committing. It tests a leading option; it does not generate a broad option set or design implementation.

## Input and output format

**Input:** A claim, decision, or direction to test. It may be self-contained or supported by authorized research, metrics, feedback, records, or prior decisions.

**Output:** Run the workflow in order. Present the steelman and assumption table first, then ask forcing questions **one at a time**. Wait for each answer, assess it, and challenge unsupported answers before asking the next question. After the questions, provide the pre-mortem, dissent analysis, mind-change criterion, verdict, handoff, and exactly one next action.

Use dates in `DD MMM` format when a date is needed.

## Where this fits

Use this sequence:

1. Generate or identify meaningful alternatives.
2. Pressure-test the leading option.
3. Make and document the decision with rigor that matches its consequences.
4. Plan or build the chosen approach, if applicable.

**Readiness gates**

- If meaningful alternatives have not been considered, pause and generate them first. Testing one idea too early can become an exercise in defending it.
- If the same idea was pressure-tested recently and no material evidence, assumptions, or conditions have changed, do not repeat the exercise. Use the existing findings to make the decision.
- If evidence will come from communications, records, feedback, or other information about people, confirm a legitimate decision-related purpose and clear authorization before accessing or using those sources.

## Handling people-related information

Use information about people only when necessary to assess the idea, its impact, or relevant stakeholder concerns.

- State the specific purpose, such as validating demand or assessing a delivery risk.
- Confirm that the requester and intended audience are authorized to access the sources and receive the analysis.
- Use the minimum relevant sources and facts. Prefer aggregate, anonymized, or role-level evidence where sufficient.
- Omit unrelated or sensitive personal details. Respect consent, confidentiality obligations, and reasonable privacy expectations.
- Share findings only within the appropriate access boundary. If purpose, authorization, consent, or scope is unclear, stop and request clarification or use non-personal evidence.

## Rules of engagement

- Be direct. Do not treat confidence as evidence.
- Attack the strongest reasonable version of the idea, not a caricature.
- Separate facts, inferences, and forecasts.
- Use evidence such as research, metrics, prior experiments, feedback, documented decisions, and stakeholder input.
- Refer to dissenters by relevant role, such as a finance owner, delivery lead, customer representative, domain expert, or skeptical peer. Do not invent their views.
- Skip a section only when it is genuinely irrelevant, and state why.

## 1. Steelman the claim

Restate the idea in its strongest form. Remove unnecessary hedging while preserving the decision-maker's intent. Include the action, expected result, mechanism, timeframe, and conditions that make it sensible.

> We should [take action] because [mechanism] will produce [outcome] for [group] within [timeframe], provided that [key condition] holds.

If the original framing is already the strongest version, say so and continue. If the stronger restatement changes the intended claim, obtain confirmation before testing it.

## 2. Identify load-bearing assumptions

List three to five assumptions that must hold. Rank them by damage if wrong, starting with the assumption most likely to undermine the decision.

| Rank | Assumption | Type: fact, estimate, or belief | Current support | Damage if wrong | Smallest useful test |
|---|---|---|---|---|---|
| 1 | [State the assumption] | [Choose one] | [Summarize evidence] | [Low, medium, or high] | [Name the test] |

Make assumptions observable where possible. Replace “customers will value this” with a defined behavior, segment, threshold, or willingness-to-pay condition.

## 3. Run forcing questions sequentially

Ask five to eight questions total, one at a time. Start with the highest-risk assumption and adapt later questions to the answers received. Do not present the full set as a questionnaire, because that permits selective answers.

Choose from these categories:

- **Evidence:** What is the strongest evidence for this? What is the strongest evidence against it?
- **Falsifiability:** What would need to happen in the next 30 or 90 days to show this is wrong?
- **Counterfactual:** What similar attempt failed, and why is this case materially different?
- **Opportunity cost:** What valuable work will not happen if resources go here?
- **Second-order effects:** If this succeeds, what does the situation look like in 12 months? What could success itself break or constrain?
- **Stakeholder dissent:** Which role would object most strongly? What would that person say, and has that objection been heard directly?
- **Reversibility:** If this is wrong, what does unwinding require in time, money, commitments, trust, or organizational disruption?
- **Null option:** What happens if no action is taken for the next three months?

Push for specificity. “I think it will work” is not evidence; ask what observed behavior, data, comparison, or commitment supports that belief. If an answer is vague, unsupported, or evasive, challenge it before moving on.

## 4. Run a pre-mortem

Assume the initiative failed after a realistic period, often 6 to 12 months. Identify the three most likely failure modes, ordered by likelihood or impact. Include execution failures, external changes, and wrong underlying premises where relevant.

| Failure mode | Why it could happen | Earliest warning sign | Monitoring action or owner |
|---|---|---|---|
| [Describe the failure] | [Name the mechanism] | [Name an observable signal] | [Name the check or accountable role] |

The warning sign must be observable early enough to change course.

## 5. Surface credible dissent

Identify two or three relevant roles that could reasonably disagree. State each role's strongest likely objection. If the decision-maker has not sought that perspective, mark it as an evidence gap; do not assume silence means agreement.

Dissent is not an automatic veto. Its purpose is to expose constraints, incentives, dependencies, and risks that supporters may miss. When authorized private feedback is relevant, summarize only what is necessary and do not attribute comments beyond the approved audience.

## 6. Define what would change the decision

Require one sentence naming the evidence that would reverse or materially alter the position.

> I would change my mind if [specific observable evidence] occurs by [date or decision point].

If this cannot be stated, the position is not falsifiable. Mark the pressure-test as incomplete or failed rather than issuing approval.

## 7. Give a verdict and handoff

Choose one verdict and explicitly state the next workflow step:

- **GREEN — proceed to decision.** Core assumptions have credible support, relevant dissent has been addressed, reversal costs are understood, and warning signs have an owner or review mechanism. Next: create a decision record and commit. For hard-to-reverse or organization-defining decisions, schedule a review point.
- **AMBER — test first.** The idea may be sound, but one or two high-impact assumptions or objections remain under-investigated. Name the gap and the cheapest credible way to close it, such as a small interview set, expert review, prototype, or short data-collection period. Next: run that test, then make the decision with its result recorded. Do not commit while the gap remains open.
- **RED — stop, redesign, or reopen options.** A core assumption is weak, the downside is unacceptable, or no meaningful falsification criterion can be named. Next: generate alternatives, redesign the idea, or explicitly defer it until a defined trigger occurs. Do not treat RED as approval with caveats.

End with exactly one concrete next action: a verb, an owner, and a deadline when useful.

`Research owner: interview five target users by 14 Oct and compare the results with the adoption assumption.`

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

If people-related sources were used, also verify that the purpose was legitimate, access and sharing were authorized, only necessary information was used, unrelated or sensitive details were omitted, consent and privacy expectations were respected, and the output remains within its approved audience.

Common failures include skipping alternatives, asking every question at once, confusing confidence with evidence, treating unconsulted stakeholders as aligned, repeating a recent test without new facts, using personal information without a clear purpose or authorization boundary, and issuing a positive verdict without falsifiable criteria or monitoring.

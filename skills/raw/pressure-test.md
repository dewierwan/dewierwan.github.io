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

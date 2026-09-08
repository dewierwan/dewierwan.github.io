---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make a clear decision with only as much process as the decision deserves. The objective is timely commitment, an honest record for consequential choices, and better judgment through review.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** Keep the assistant's recommendation clearly labeled as assistant analysis. Include it in a decision record only if the user asks.
4. **Record only with permission.** “Should we do X?” asks for analysis, not for a record. Create or update a record only when the user asks to log, track, open, or commit it, or explicitly agrees to that practice.
5. **Respect privacy and access boundaries.** Before consulting shared communications, personnel information, customer records, or a shared register, confirm a legitimate purpose and clear authorization. Use the minimum relevant material and omit unrelated sensitive details.
6. **Do not confuse a task with a decision.** If there is no meaningful alternative, it is execution. Say so and move to planning or doing the task.

For health, relationships, compensation, confidential personnel matters, or similarly sensitive subjects, confirm that the proposed record and audience are appropriate. Offer a private document or keep the matter in conversation if needed.

## 1. Select the mode

Identify whether this is a new decision, a continuation, a commitment, or a review.

| Mode | Use when | Action |
|---|---|---|
| New | No matching record exists, or the user requests a fresh decision | Frame and classify it |
| Resume | An open decision exists | Add new inputs without rewriting history |
| Commit | An open decision exists and the user is ready to decide | Complete readiness checks and record the call |
| Review | A resolved decision has reached its review point | Compare actuals with the original prediction |

If the user explicitly names a mode, follow that instruction. Otherwise, when authorized to access the chosen decision register, look for an overlapping decision before creating another record. Trust explicit instructions over automated matching.

## 2. Frame the question

Write the decision in a form that can be answered. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What deadline, event, or trigger requires a decision?
- What outcome is desired?
- What happens if no action is taken?

If the question is open-ended and credible options do not exist yet, generate options before evaluating them. Ask one clarifying question at a time when the missing answer changes the analysis.

## 3. Classify scope

Use the cost of unwinding the choice, not just its apparent size. Consider money, time, trust, operational disruption, opportunity cost, and reputation.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not record by default |
| Reversible | Moderate stakes; reversible in days or weeks | Brief comparison and optional light record |
| Hard to reverse | Meaningful cost or disruption to undo | Full analysis and challenge gate |
| Direction-setting | Shapes strategy, culture, finances, or operating model for a long period | Full analysis plus dissent and prerequisite consultation |

If the user calls a choice trivial, ask: “What would it cost to unwind?” If they cannot name the cost quickly or the answer is uncertain, treat it as a larger decision.

## 4. Apply the appropriate rigor

### Trivial

Choose a reasonable default, give a one-sentence rationale, and move on. If the user is delaying without a decision-changing reason, say directly that further deliberation is consuming more attention than the choice merits.

### Reversible

1. List two or three realistic options.
2. For each, state one major strength, one major weakness, and a rough effort, time, or cost estimate.
3. Give a recommendation and the decisive reason.
4. When uncertainty matters, prefer the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid challenge examines its assumptions, contrary evidence, likely failure modes, strongest alternative, and relevant stakeholder objections.

If this has not happened in the current work context, stop the commitment flow and state:

> This decision is hard to reverse. Challenge the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not waive the gate because of urgency alone. Proceed only after the challenge is complete or the user explicitly overrides it with a reason. If the challenge reveals a serious unresolved failure, return to option generation, redesign the option, obtain a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Identify stakeholders with expertise, consequences, or constraints relevant to the decision.
4. Provide a recommendation labeled **Assistant analysis** unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process, plus two further gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and represent their strongest case fairly.

The decision is not ready until the required conversation has occurred, unless the user explicitly accepts and records why proceeding is necessary. If the choice is rushed, name exactly what consultation, evidence, or dissent is being skipped and why it matters.

## 5. Keep facts, views, and uncertainty separate

For each serious option, capture what it enables, what it costs or prevents, the best evidence for it, the strongest objection, key assumptions, and the cost of reversal. Distinguish non-negotiable requirements from preferences.

Maintain these categories:

- **User’s stated view:** only the user's actual words or clearly confirmed position.
- **Assistant analysis:** the assistant's recommendation and reasoning.
- **Open question:** uncertainty not yet resolved.

If the user has not stated a position, write “No position stated yet” or leave their position blank. Never manufacture a lean, confidence percentage, rationale, dissent response, or final choice.

## 6. Commit and record

Before finalizing, confirm the choice, rationale, reversal conditions, next action owner and date, observable prediction, and the user's confidence in that prediction.

Use the user's chosen document, decision register, or private file. A useful record includes status, decision type, stakes, reversibility, decision date, review date, confidence, and outcome. Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar or reminder system for higher-stakes reviews.

For an open decision, record context, options, and new inputs only. Leave choice, confidence, prediction, and personal reasoning blank until the user supplies them. When resuming, append a dated entry rather than replacing earlier thinking.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** [Optional additional option]

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
By [date or trigger], [observable outcome] will happen or not happen.
Confidence: [X%]

## Worries
The most credible downside or failure mode.

## Retrospective
To be completed at review.
```

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals rather than impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat a bad outcome as proof of a poor process, or a good outcome as proof of sound reasoning.

## Completion message

When a decision is made, summarize it clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [date]
Review: [date or trigger]
Record: [location, if one exists]
```

Use direct language. Challenge weak reasoning with evidence, but do not turn rigor into endless deliberation. Once the appropriate gates are met, name the decision and move forward.

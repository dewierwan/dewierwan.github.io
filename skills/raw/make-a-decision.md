---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, make authorized records without inventing the user’s views, and review outcomes to improve future choices.
---

# Make a decision

Use this workflow to make a clear choice with rigor proportional to its stakes and reversibility. The aim is not maximum analysis: most decisions should take minutes, while costly or direction-setting choices deserve challenge, consultation, a record, and a later review.

## Core rules

1. **Match rigor to stakes.** Use a quick default for small, reversible choices; reserve lengthy work for decisions that are expensive to unwind.
2. **The user owns their position.** Never state, record, or imply that the user favors, opposes, is leaning toward, or decided an option unless they explicitly said so.
3. **Separate advice from attribution.** Put recommendations in chat under **Assistant analysis**. Add them to a record only if the user specifically asks. If the user has stated no position, write “No position stated yet” or leave their position blank.
4. **Record only with permission.** “Should we do this?” asks for analysis, not for a new record. Create or update a record only when the user asks to log, track, open, record, or commit it, or explicitly agrees.
5. **Respect privacy and access boundaries.** Before consulting shared messages, internal records, personal information, or a shared register, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and omit unrelated sensitive information.
6. **Do not turn execution into a decision.** If there is no meaningful alternative, say so and move to planning or doing the task.
7. **Do not use rigor to delay.** Once the appropriate checks are complete, name the call and move forward.

Before writing to a shared record, confirm that its audience is appropriate. For sensitive subjects, including health, relationships, compensation, or confidential personnel matters, keep the discussion in chat or offer a private record.

## 1. Select the mode

Choose the mode from the user’s request and, only if authorized, the relevant decision register.

- **New:** No relevant record exists, or the user wants a fresh decision.
- **Resume:** An existing decision is still open and the user wants to continue.
- **Commit:** An open decision exists and the user is ready to decide.
- **Review:** A resolved decision has reached its review point and has not yet received an outcome assessment.

Follow an explicit user instruction over automatic detection. Otherwise, search for overlapping records before creating a duplicate. On resume, append new inputs and shifts in thinking; do not rewrite history. On review, use the original prediction and reasoning as the baseline.

## 2. Frame the decision

Write a question that can be answered. Ask one clarifying question at a time when needed:

- What is being chosen?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What is the deadline or decision trigger?
- What outcome is sought, and what happens if nothing changes?

If the problem is open-ended and there are no credible options, generate options first. If only one viable path exists, say: “This is a task rather than a decision; the next step is to plan or execute it.”

## 3. Classify scope

Classify by the cost of unwinding the choice: money, time, trust, operational disruption, opportunity cost, and reputation—not apparent size alone.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes; reversible within hours | Decide now; do not record by default |
| Reversible | Moderate stakes; reversible in days or weeks | Short comparison and, if useful, a light record |
| Hard to reverse | Material cost, disruption, or loss if undone | Full analysis, challenge, and stakeholder check |
| Direction-setting | Shapes strategy, culture, finances, or operating model for a long period | Full analysis, explicit dissent, and prerequisite conversations |

If the user calls it trivial, ask: **“What would it cost to unwind?”** If the cost is uncertain, disruptive, or cannot be stated quickly, use a larger bucket.

## 4. Apply the appropriate rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, say so plainly: further attention may cost more than an imperfect choice.

### Reversible

Aim for roughly ten minutes:

1. List two or three realistic options.
2. For each, state one strength, one weakness, and a rough effort, cost, or time estimate.
3. Give an **Assistant analysis** recommendation and the decisive reason.
4. Where uncertainty matters, choose the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

A hard-to-reverse decision normally deserves roughly 30–60 minutes of work. Before commitment, pressure-test the leading option by examining assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and important objections from affected people or relevant experts.

If no relevant challenge has occurred in the current working context, stop and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not bypass this merely because the user is in a hurry. Continue only after the challenge is complete or the user explicitly overrides it with a reason.

Use the challenge result as a decision rule:

- **Green:** No material unresolved issue; proceed with options, pre-mortem, stakeholder check, and recommendation.
- **Amber:** Risks or unknowns remain but are understood and bounded; proceed only after stating mitigations, owners, and review triggers.
- **Red:** A serious failure mode, missing evidence, or unresolved constraint remains; do not force commitment. Return to option generation, redesign the proposal, gather a decision-changing fact, or run a bounded test.

### Direction-setting

Use the hard-to-reverse process plus two gates:

1. Name the specific leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has happened, unless the user explicitly records why proceeding is necessary. If the choice is being rushed, identify exactly what consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture what it enables; what it costs, delays, or prevents; strongest supporting evidence; strongest objection; key assumptions; and reversal cost. Choose criteria before comparison and separate non-negotiables from preferences. Use scores only when they clarify tradeoffs.

| Category | What belongs here |
|---|---|
| User’s stated view | Only the user’s expressed choice, reasoning, confidence, and response to concerns |
| Assistant analysis | The assistant’s recommendation, evidence, and reasoning |
| Open question | Material uncertainty not yet resolved |

Run a pre-mortem: “It is later and this failed. What most likely caused it?” Then identify stakeholders with relevant expertise, consequences, or constraints.

## 6. Commit and record

Before finalizing a meaningful decision, confirm the choice, rationale, reversal conditions, next action owner and date, observable prediction, and the user’s confidence in that prediction. Make predictions testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [X%].

Use the user’s chosen document system, register, or private file. A record should include status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. For non-binary questions, mark the record resolved when a decision has been made.

| Scope | Default review point | Reminder approach |
|---|---|---|
| Reversible | One month | Record a review date |
| Hard to reverse | Three months | Record a review date and reminder |
| Direction-setting | Six months | Record a review date and reminder |

Use a meaningful milestone or trigger instead when it is better than a calendar date. For high-stakes choices, create a reminder in the user’s chosen calendar or task capability if authorized.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** [What it is and central tradeoff]
- **Option B:** [What it is and central tradeoff]
- **Option C:** [What it is and central tradeoff]

## Thinking log
### [Date]
- New inputs, conversations, data, or events
- How the thinking changed
- User’s stated position: open / leaning / decided

## Dissent
[Who raised concerns, their strongest argument, and how it was handled.]

## My choice and why
[User’s own reasoning, only when stated by the user.]

## What would change my mind
[Assumptions or evidence that would justify reversal.]

## Prediction
By [date], [observable outcome] will happen or not happen.
Confidence: [X%]

## Worries
[Most credible downside or failure mode.]

---

## Retrospective
[To be completed at review.]
```

For a new open decision, record context, current options, and new inputs; leave commitment sections blank. On resume, append a dated thinking-log entry and add genuinely new options without replacing prior reasoning.

## 7. Review the outcome

At the review point, complete four sections:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare actual events to the recorded prediction and confidence.
3. **Was the process sound?** Judge the evidence, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle that can improve a later decision.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Keep outcome quality separate from decision quality: a sound decision can have a poor result under uncertainty, and a weak process can get lucky.

## Completion message

When a decision is made, summarize it plainly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [date]
Review: [date or trigger]
Record: [location, if one exists]
```

Use direct language and challenge weak reasoning with evidence. Once the required gates are satisfied, commit, record only within the authorized boundary, and proceed.

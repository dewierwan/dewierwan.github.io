---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make a clear decision with enough rigor, but not more than needed. The goal is to move forward, preserve the reasoning for meaningful choices, and learn from results without treating every outcome as proof that the original process was good or bad.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may recommend an option in conversation, clearly labeled as assistant analysis. Add that analysis to a decision record only if the user explicitly requests it.
4. **Record only with permission.** “Should we do X?” is a request for analysis, not a request to create or update a record. Log a decision only when the user asks to log, track, open, resume, or commit it, or has clearly agreed to a standing recording practice.
5. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution. Plan or start the task instead of opening a decision process.
6. **Protect privacy and access boundaries.** Before accessing shared communications, personnel records, customer information, or a shared register, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and facts.

For sensitive subjects, including health, relationships, compensation, confidential personnel matters, or private legal concerns, confirm that the intended record audience is appropriate. Offer a private record or keep the discussion in chat when a shared workspace is unsuitable.

## 1. Select the mode

Determine whether the user is starting, continuing, committing, or reviewing a decision.

| Mode | When to use it | Action |
|---|---|---|
| New | No relevant record exists, or the user wants a fresh decision | Frame and classify the decision |
| Resume | An open record exists and the user wants to continue thinking | Append new inputs and current stated position |
| Commit | An open decision exists and the user is ready to decide | Confirm readiness, then finalize and record |
| Review | A resolved decision has reached its review point | Compare actual outcomes with the original prediction |

If the user explicitly names a mode, follow that instruction. Otherwise, if authorized to access the chosen record system, look for overlapping decisions before creating a duplicate.

For a resume, retrieve the existing record and append to the history rather than rewriting it. For a review, use the original reasoning and prediction as the baseline; do not reconstruct them from memory.

## 2. Frame the decision

Write the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What deadline, trigger, or cost of delay applies?
- What result is desired?
- What happens if no action is taken?

If the question is broad and credible options do not yet exist, generate options before evaluating them. If there is only one viable path, say so directly:

> This appears to be a task rather than a decision. The next step is to plan or execute it.

## 3. Classify scope

Ask one clarifying question at a time when classification is unclear. Use the cost to unwind the choice, not just its apparent size.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default |
| Reversible | Moderate stakes and changeable within days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, trust loss, or opportunity cost if undone | Full analysis, challenge gate, stakeholder check, full record if authorized |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and required senior-stakeholder conversation |

Use this test when unsure: **What would it cost to unwind this?** Consider money, time, operational disruption, trust, opportunity cost, and reputational effects. If the cost cannot be stated quickly, or the answer is highly uncertain, the decision is probably larger than it first appears.

## 4. Apply the right rigor

### Trivial

Choose a reasonable default, state a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: continued attention may cost more than an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. Give each option one major strength, one major weakness, and a rough effort or cost estimate.
3. Recommend an option and name the decisive reason.
4. If uncertainty is material, identify the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid challenge examines:

- Important assumptions and evidence that would disconfirm them.
- Likely failure modes and a brief pre-mortem.
- The strongest alternative.
- Material stakeholder objections or constraints.
- Whether a smaller test, staged commitment, or reversible version is possible.

If no relevant pressure test has occurred in the active work context, stop the commitment flow and say:

> This decision is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not continue merely because the user is in a hurry. Proceed only after the challenge is complete or the user explicitly overrides it with a reason. If it exposes a serious unresolved failure, return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or affected stakeholder whose conversation is required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has happened, unless the user explicitly accepts and records a reason for proceeding without it. If it is being rushed, state which consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence in its favor.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies tradeoffs rather than disguising judgment.

Keep these categories distinct:

- **User’s stated view:** Only positions the user actually expressed.
- **Assistant analysis:** The recommendation and reasoning supplied by the active assistant.
- **Open question:** An uncertainty not yet resolved.

If the user has not expressed a position, write “No position stated yet” or leave their position blank. Never invent a lean, confidence level, response to dissent, rationale, or final decision for the user.

## 6. Commit and record

Before finalizing, confirm:

- What is the decision?
- Which option was chosen?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable outcome is predicted?
- What is the user’s confidence in that prediction?

For meaningful decisions, make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Use the user’s chosen document system, decision register, or private file. A useful record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. For a non-binary question, mark it resolved when a direction has been chosen.

Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar, task system, or other reminder for high-stakes reviews.

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

## Retrospective
To be completed at review.
```

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until the user commits. When resuming, append a new dated thinking-log entry rather than overwriting history.

## 7. Review the outcome

At the review point, assess four separate questions:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle that could improve a future decision.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not collapse a bad outcome into a bad decision process, or a good outcome into a sound process.

## Completion check and message

Before closing the workflow, audit the decision:

- Is the scope classification plausible given the unwind cost?
- Was the appropriate challenge gate completed or explicitly overridden?
- Were relevant stakeholders consulted, or was the omission acknowledged?
- Is assistant advice clearly separate from the user’s stated view?
- Does any record contain only authorized, relevant information?
- Is the next action owned and dated?
- Is there a testable prediction and a review trigger for meaningful choices?

Then summarize clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [date]
Review: [date or trigger]
Record: [location, if one exists]
```

Use direct language. Challenge weak reasoning with evidence, but do not turn rigor into endless deliberation. Once the appropriate readiness gates have been met, name the decision and move forward.

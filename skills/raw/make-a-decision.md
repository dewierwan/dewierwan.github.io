---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, make a clear call when ready, and record and review meaningful choices without inventing the user’s views or crossing privacy boundaries.
---

# Make a decision

Use this workflow to apply enough rigor to a decision without turning every choice into a long project. The aim is a clear, accountable call; a useful record for meaningful choices; and better judgment through review.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices deserve minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, is leaning toward, or decided something they did not actually say.
3. **Separate advice from attribution.** Recommendations belong in conversation as **Assistant analysis**. Put them in a record only when the user specifically requests that.
4. **Record only with permission.** “Should we do X?” requests analysis, not a record. Create or update a record only when the user asks to log, track, open, resume, or commit it, or has explicitly agreed to a standing recording practice.
5. **Respect access boundaries.** Before searching shared messages, records, or a decision register, establish a legitimate purpose and authorization. Use only the minimum relevant information and exclude unrelated sensitive details.
6. **Do not confuse execution with a decision.** If there is no meaningful alternative, say so and move to planning or doing the task.
7. **Do not deliberate indefinitely.** Once the appropriate gates are met, name the decision and move forward.

If a register is visible to others, confirm that the audience is appropriate before writing. For health, relationships, compensation, confidential personnel matters, or similarly sensitive subjects, offer a private record or keep the discussion in chat.

## 1. Choose the mode

If the user explicitly says to start, resume, commit, or review a decision, follow that instruction. Otherwise, if authorized, check the chosen decision system for overlapping records before making a duplicate.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An existing record is open and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to decide.
- **Review:** A resolved decision has reached its review date and its outcome is still unknown or marked too early.

For a resumed decision, append new material rather than rewriting history. For a review, use the original prediction, confidence, and reasoning as the baseline.

## 2. Frame the decision

Write the question so it can be answered. Establish:

- What choice is being made?
- Who has decision authority?
- What are the realistic options, including doing nothing?
- What deadline, event, or constraint requires a decision?
- What result is sought?
- What happens if no action is taken?

If the question is broad and credible options do not yet exist, generate options before evaluating them. If only one viable path exists, say: “This is a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time if needed. Use the cost of unwinding the decision—money, time, trust, disruption, opportunity cost, and reputation—to classify it.

| Bucket | Meaning | Required treatment |
|---|---|---|
| Trivial | Low stakes; reversible within hours | Decide now; do not record by default |
| Reversible | Moderate stakes; reversible in days or weeks | Compare a few options; light record if requested |
| Hard to reverse | Material cost or disruption to undo | Full analysis, challenge gate, stakeholder check |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis plus dissent and named prerequisite conversation |

If the unwind cost cannot be named quickly or is uncertain, treat the decision as larger until evidence shows otherwise.

## 4. Apply the right rigor

### Trivial

Choose a reasonable default, state a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: attention spent deciding may exceed the cost of an imperfect choice.

### Reversible

In a short session:

1. List two or three realistic options.
2. For each, state one major strength, one weakness, and a rough effort, time, or cost estimate.
3. Give a recommendation and the decisive reason.
4. If uncertainty matters, select the smallest reversible test that could change the choice.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test examines assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and material stakeholder objections.

If no relevant challenge has occurred in the current work context, stop the commitment flow and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Proceed only after the pressure test is complete or the user explicitly overrides it with a reason. If it finds a serious unresolved problem, do not force a commitment. Return to option generation, redesign the option, obtain a decision-changing fact, or run a bounded test.

After the gate:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check with people who have relevant expertise, bear consequences, or may reveal constraints.
4. Provide a recommendation labeled **Assistant analysis** unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and represent their strongest case fairly.

The choice is not ready until the required conversation has occurred, unless the user explicitly records why proceeding is necessary. If it is being rushed, state exactly which consultation, evidence, or dissent is being skipped and why that matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence for it.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.

Separate non-negotiable requirements from preferences. Use scoring only when it clarifies real tradeoffs rather than disguising judgment.

Maintain three distinct categories:

- **User’s stated view:** only what the user actually said.
- **Assistant analysis:** the assistant’s recommendation and reasoning.
- **Open question:** uncertainty not yet resolved.

If the user has not stated a position, write “No position stated yet” or leave the field blank. Never create a user lean, confidence level, dissent response, rationale, or final choice from inference.

## 6. Commit and record

Before finalizing, confirm:

- What is the decision and chosen option?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action and by when?
- What observable result is predicted?
- What is the user’s confidence in that prediction?

For meaningful decisions, make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [X%].

Use a user-chosen document system, decision register, or private file. Where a structured system is used, create new records from its approved template when available, then fill its metadata and sections without replacing prior history. At minimum, record status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

A decision may be open or resolved. If the system uses yes/no resolution, use the status to represent whether a decision has been made or the answer to a binary question; a non-binary choice that has been settled is still resolved. Keep outcome assessment separate from resolution.

Suggested review defaults: one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar, task system, or equivalent reminder for high-stakes reviews.

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

For an open decision, record context, current options, and new inputs, but leave user commitment sections blank until the user commits. On resume, append a dated thinking-log entry and add new options where appropriate.

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare results with the recorded prediction and confidence.
3. **Was the process sound?** Assess the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. A poor outcome can follow a sound decision process, and a favorable outcome can follow weak reasoning.

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

Use direct language. Challenge weak reasoning with evidence, but do not let rigor become an excuse for endless deliberation.

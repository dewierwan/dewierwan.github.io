---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, make clear commitments when ready, and preserve authorized records and reviews without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make decisions with the right amount of rigor. The objective is not maximum analysis. It is to make a clear call when ready, preserve the reasoning for meaningful choices, and improve future judgment through review.

## Core rules

1. **Match rigor to stakes and reversibility.** Most decisions should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** Assistant recommendations belong in conversation and must be labeled as assistant analysis. Add them to a record only if the user asks.
4. **Do not confuse a task with a decision.** If no meaningful alternative exists, this is execution. Plan or start the task instead.
5. **Record only with permission.** “Should we do X?” requests analysis, not a record. Create or update a record only when the user asks to log, track, open, or commit it, or explicitly agrees to doing so.
6. **Respect access boundaries.** Before accessing shared communications, personnel information, customer information, or a shared decision register, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and omit unrelated sensitive details.

If a decision register has a shared audience, confirm that the audience is appropriate before writing. For health, relationships, compensation, confidential personnel matters, or similarly sensitive topics, offer a private record or keep the discussion in chat.

## 1. Choose the mode

Determine whether the work concerns a new or existing decision.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review date and still needs an outcome assessment.

If the user explicitly names the mode, follow that instruction. Otherwise, if authorized, search the chosen register for overlapping decisions before creating a duplicate. For resume, append new information rather than rewriting history. For review, use the original prediction and reasoning as the baseline.

## 2. Frame the decision

Write the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What deadline, event, or trigger requires a decision?
- What result is desired?
- What happens if no action is taken?

If the question is broad and options do not yet exist, generate options before evaluating them. If there is only one viable path, say so directly: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time when classification is unclear. Use this test: **What would it cost to unwind this?** Include money, time, trust, operational disruption, opportunity cost, and reputation.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes; reversible within hours | Decide now; do not log by default |
| Reversible | Moderate stakes; changeable within days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Material cost, disruption, or loss if undone | Full analysis, challenge gate, and stakeholder check |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and prerequisite conversations |

If a supposedly trivial decision has an unclear or non-obvious unwind cost, treat it as larger until clarified.

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, state a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: continued attention may cost more than an imperfect choice.

### Reversible

1. List two or three realistic options.
2. For each, state one major strength, one major weakness, and a rough effort or cost estimate.
3. Recommend an option and name the decisive reason.
4. If uncertainty is material, choose the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test examines assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and major stakeholder objections.

If no relevant pressure test has occurred in the current work context, stop the commitment flow and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not proceed merely because the user is in a hurry. Continue only after the pressure test is complete or the user explicitly overrides it with a reason. If the test identifies a serious unresolved failure, return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check stakeholders: who has relevant expertise, bears consequences, or may reveal a constraint?
4. Give a recommendation labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has happened, unless the user explicitly accepts and records a reason for proceeding without it. If it is being rushed, state which consultation, evidence, or dissent is being skipped and why that matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture what it enables, what it costs or prevents, its strongest supporting evidence, its strongest objection, its key assumptions, and its reversal cost. Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies tradeoffs rather than disguising judgment.

Keep these categories distinct:

- **User’s stated view:** Only positions the user actually expressed.
- **Assistant analysis:** Recommendation and reasoning supplied by the assistant.
- **Open question:** Uncertainty not yet resolved.

If the user has not expressed a position, record “No position stated yet” or leave that field blank. Never invent a lean, confidence level, rationale, response to dissent, or final choice.

## 6. Commit and record

Before finalizing, confirm the decision, chosen option, reason it is preferred now, conditions that would change it, next action owner and date, observable prediction, and the user’s confidence in that prediction.

For meaningful decisions, make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Use the user’s chosen register, document system, or private file. Recommended fields are status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. Suggested review defaults are one month for reversible choices, three months for hard-to-reverse choices, and six months for direction-setting choices. Add a reminder for high-stakes reviews using the user’s chosen calendar or task system.

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

For a new open decision, record context, options, and new inputs; leave commitment sections blank. When resuming, append a dated thinking-log entry rather than overwriting prior reasoning.

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat a bad outcome as proof of a bad process, or a good outcome as proof of a sound process.

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

Use direct language. Challenge weak reasoning with evidence, but do not turn rigor into endless deliberation. Once the appropriate readiness gates are met, name the decision and move forward.

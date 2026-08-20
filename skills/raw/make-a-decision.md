---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful decisions without inventing the user’s views. Supports quick calls, multi-session deliberation, commitments, and evidence-based retrospectives
---

# Make a decision

Use this workflow to make decisions with the right amount of rigor. The purpose is not to maximize analysis. It is to make a clear call when ready, preserve the reasoning for meaningful choices, and learn from outcomes.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may make a recommendation in conversation. Label it as assistant analysis. Add it to a decision record only if the user asks for it.
4. **Do not confuse a task with a decision.** If there is no real alternative, this is execution. Start or plan the task instead of opening a decision process.
5. **Use shared records with consent.** Do not create a decision record simply because the user requested analysis. Create or update one only when the user asks to log, track, open, or commit it, or when they have already agreed to track that class of decisions.

For organizations that maintain a decision register, use it for non-trivial decisions once the user has consented to that practice. Before using a shared register, confirm that its audience is appropriate. Offer a private document for sensitive subjects such as health, relationships, compensation, or confidential personnel matters.

## 1. Choose the mode

Determine whether the user is dealing with a new or existing decision.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review date and its outcome has not been assessed.

If the user explicitly names the mode, follow that instruction. Otherwise, search the available decision register for overlapping open or resolved decisions before creating a duplicate.

A request such as “Should we do X?” is normally a request for analysis, not permission to create a record. A request such as “Open a decision record for X” or “Log this decision” is permission to record it.

## 2. Frame the decision

Write the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What is the deadline or trigger for deciding?
- What result is desired?
- What happens if no action is taken?

If the question is open-ended and there are no credible options yet, generate options before evaluating them. Do not pressure-test a vague problem statement.

## 3. Classify scope

Ask one clarifying question at a time when necessary. Place the choice in one bucket.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, consult relevant stakeholders |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and named prerequisite conversations |

Use this test when classification is unclear: **What would it cost to unwind this?** If the answer is not obvious or cannot be stated quickly, the decision is likely larger than it first appears.

Broad defaults:

| Bucket | Stakes | Reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name it directly: continued attention may cost more than an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. For each, give one major strength, one major weakness, and a rough effort or cost estimate.
3. Recommend an option and name the decisive reason.
4. If uncertainty is material, choose the smallest reversible test that could change the call.

### Hard to reverse: mandatory challenge gate

A hard-to-reverse decision must be pressure-tested before commitment.

First inspect whether a structured challenge of this exact topic has already happened in the current work context. A valid pressure test examines the leading option’s assumptions, disconfirming evidence, likely failure modes, strongest alternative, and major stakeholder objections.

- **If it has not happened, stop the commitment flow.** State: “This is hard to reverse. Run a pressure test of the leading option before committing. To proceed without one, explicitly state why the gate is being skipped.”
- **Do not continue to a commitment merely because the user is in a hurry.** Proceed only after the pressure test is complete or the user explicitly overrides the gate with a stated reason.
- **If the pressure test finds a serious unresolved failure, do not force a decision.** Return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and decision criteria.
2. Run a short pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check stakeholders: who has relevant expertise, bears the consequences, or may reveal a constraint?
4. Give a recommendation, clearly labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable decision-maker, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case.

The decision is **not ready** until the required conversation has happened, unless the user explicitly accepts and records a reason for proceeding without it. If a direction-setting decision is being rushed, say what analysis, dissent, or consultation is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence in its favor.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies tradeoffs rather than disguising judgment.

Keep three categories distinct:

- **User’s stated view:** only positions the user actually expressed.
- **Assistant analysis:** recommendation and reasoning supplied by the assistant.
- **Open question:** uncertainty not yet resolved.

If the user has not expressed a position, write “No position stated yet” or leave the user-position field blank. Never invent a lean, confidence level, rationale, response to dissent, or final choice for them.

## 6. Commit and record

Before finalizing, confirm:

- What is the decision?
- Which option was chosen?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable result is predicted?
- What is the user’s confidence in that prediction?

For meaningful decisions, make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Use the user’s selected decision register, document system, or private file. A useful record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

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

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until the user commits. When resuming, append a new dated thinking-log entry rather than rewriting history.

Suggested review defaults: about one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar or task reminder for high-stakes reviews.

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not collapse a bad outcome into a bad decision process, or a good outcome into a sound process.

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

Use direct language. Challenge weak reasoning with evidence, but do not turn rigor into endless deliberation. Once the appropriate readiness gates have been met, name the decision and move forward.

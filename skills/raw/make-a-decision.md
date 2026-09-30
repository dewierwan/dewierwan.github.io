---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make a clear choice with the right amount of rigor. The goal is not maximum analysis: make routine choices quickly, give consequential choices appropriate scrutiny, preserve an accurate record when authorized, and learn from results.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** Assistant recommendations belong in the conversation and must be labeled as **Assistant analysis**. Put them in a decision record only if the user specifically asks.
4. **Record only with permission.** “Should we do X?” asks for analysis, not creation of a record. Create or update a record only when the user asks to log, track, open, or commit it, or has explicitly agreed to that practice.
5. **Protect privacy and access boundaries.** Before searching shared records, communications, personnel information, or other sensitive sources, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and details. Do not place sensitive information in a record visible to people who should not receive it.
6. **Do not confuse a task with a decision.** If there is no meaningful alternative, say so and move to planning or execution.

For health, relationships, compensation, personnel matters, or similarly sensitive subjects, confirm that a shared record is appropriate before logging. Offer a private document or keep the discussion in chat when that better respects consent and access expectations.

## 1. Select the mode

Determine whether this is a new or existing decision.

- **New:** No relevant record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review date and has not received a meaningful outcome assessment.

If the user explicitly says which mode they want, follow that instruction. Otherwise, if authorized, search the chosen decision register for overlapping titles or questions before creating a duplicate. Do not search private or shared sources merely as a default.

Use these mode checks:

| Signal | Mode | Next action |
|---|---|---|
| No matching authorized record | New | Frame and classify the decision |
| Matching record is open | Resume | Fetch it and append new inputs |
| Open record plus “I’ve decided” or equivalent | Commit | Confirm the choice and complete the commitment record |
| Resolved record, review date reached, and outcome is blank or too early | Review | Run the retrospective |

For a resume, append new information rather than rewriting history. For a review, use the original prediction and reasoning as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Put the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What is the deadline or trigger for deciding?
- What result is desired?
- What happens if no action is taken?

If the request is broad and credible options have not yet been generated, generate options before evaluating them. Do not pressure-test a vague problem statement.

If there is one viable path and the issue is simply whether to execute it, say: “This appears to be a task rather than a decision. The next step is to plan or do it.”

## 3. Classify scope

Ask one clarifying question at a time when classification is unclear. Use the unwind test: **What would it cost to reverse this?** Consider money, time, trust, operational disruption, opportunity cost, and reputational effects. If the cost cannot be named quickly or is uncertain, the choice is probably larger than it first appears.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Choose a reasonable default; do not log by default |
| Reversible | Moderate stakes; can change within days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, and consult relevant stakeholders |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and named prerequisite conversations |

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right rigor

### Trivial

Pick the reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name the attention cost directly: continued deliberation can cost more than an imperfect choice. Do not create a record by default.

### Reversible

Use a short working session:

1. List two or three realistic options.
2. For each, state one principal strength, one principal weakness, and a rough effort or cost estimate.
3. Give a recommendation and the decisive reason.
4. If uncertainty is material, identify the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test considers the main assumptions, disconfirming evidence, likely failure modes, strongest alternative, and significant stakeholder objections.

If no relevant pressure test has occurred in the current work context, stop the commitment flow and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not bypass this merely because the user is in a hurry. Continue only after a pressure test is complete or the user explicitly overrides the gate with a reason.

If the pressure test identifies a serious unresolved failure, do not force a commitment. Return to option generation, redesign the option, gather decision-changing evidence, or run a bounded test.

After the gate is satisfied:

1. Define the options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check who has relevant expertise, bears consequences, or may reveal a constraint.
4. Provide a recommendation, labeled as Assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The choice is not ready until the required conversation has happened, unless the user explicitly accepts and records why proceeding is necessary. If it is being rushed, name the consultation, evidence, or dissent being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence in its favor.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it genuinely clarifies tradeoffs rather than disguising judgment.

Keep these categories distinct:

- **User’s stated view:** Only positions the user actually expressed.
- **Assistant analysis:** The assistant’s recommendation and reasoning.
- **Open question:** Material uncertainty not yet resolved.

If the user has not stated a position, write “No position stated yet” or leave the user-position field blank. Never invent a lean, confidence percentage, rationale, response to dissent, or final choice for them.

## 6. Open, resume, or commit a record

Use the user’s chosen record system only when access is authorized and its audience is suitable. A useful record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

### Open record

For a decision the user wants to continue across sessions, record:

- Status: **Open**.
- Classification, stakes, and reversibility.
- Context and options currently under consideration.
- New factual inputs or conversations.

Leave commitment sections blank until the user commits. Do not fill in a choice, rationale, confidence, or dissent response on the user’s behalf.

### Resume flow

1. Fetch the existing authorized record.
2. Append a dated entry under the thinking log; do not overwrite earlier thinking.
3. Capture new inputs, how the reasoning changed, and the user’s stated position today.
4. Add genuinely new options to the options section.
5. If the user remains open, summarize the current state and identify the next question, evidence, conversation, or test needed.
6. If the user is ready to decide, move to the commit flow.

### Commit flow

Before finalizing, confirm:

- What is the decision and chosen option?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable result is predicted?
- What is the user’s confidence in that prediction?

Set the record to resolved. For a binary question, record the relevant affirmative or negative result. For a non-binary question, record it as resolved once the direction or approach has been chosen.

For meaningful decisions, make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Adjust for a user-specified trigger. For hard-to-reverse and direction-setting decisions, create a calendar or task reminder if authorized and supported; include the decision question and a link or reference to the record. A record-field review date alone is usually sufficient for reversible decisions.

Use clear local dates, such as `DD MMM YYYY`.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** What it is and its central tradeoff.

## Thinking log
### [DD MMM YYYY]
- New inputs, conversations, data, or events
- How the thinking changed
- User’s stated position today: open / leaning / decided

## Dissent
Who raised a concern, their strongest argument, and how it was handled.

## My choice and why
The user’s own reasoning, only when stated by the user.

## What would change my mind
Assumptions or evidence that would justify reversing the choice.

## Prediction
By [date], [observable outcome] will happen or not happen.
Confidence: [X%]

## Worries
The most credible downside or failure mode.

---

## Retrospective
To be completed at review.
```

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat a poor outcome as proof of a poor process, or a good outcome as proof of a sound process.

## Completion message

When a decision is made, summarize it clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [DD MMM YYYY]
Review: [DD MMM YYYY or trigger]
Record: [location, if one exists]
```

Use direct language. Challenge weak reasoning with evidence, but do not use rigor as an excuse for endless deliberation. Once the appropriate readiness gates are met, name the decision and move forward.

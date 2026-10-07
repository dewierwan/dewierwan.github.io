---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, make clear commitments, preserve authorized records, and learn from outcomes without inventing the user’s views.
---

# Make a decision

Use this workflow to make choices with the right amount of rigor. The aim is not maximum analysis. It is to make a clear call when ready, preserve the reasoning for meaningful choices, and learn from results.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may recommend an option in conversation, labeled as assistant analysis. Include it in a record only when the user asks, and label it clearly.
4. **Record only with permission.** “Should we do X?” asks for analysis, not a new record. Create or update a record only when the user asks to log, track, open, or commit it, or explicitly agrees.
5. **Protect privacy and access boundaries.** Before accessing shared communications, records about people, or a shared decision register, confirm legitimate purpose and clear authorization. Use the minimum relevant sources and omit unrelated sensitive details.
6. **Do not confuse a task with a decision.** If there is no meaningful alternative, say: “This is a task rather than a decision. Let’s plan or execute it.”
7. **Do not let documentation manufacture certainty.** If the user has not stated a view, write “No position stated yet” or leave that field blank.

Before writing to a shared register, confirm that its intended audience is appropriate. For sensitive subjects, such as health, relationships, compensation, or confidential personnel matters, keep the discussion in chat or offer a private record in a user-approved location.

## 1. Choose the mode

If the user explicitly says to start, resume, commit, or review a decision, follow that instruction. Otherwise, if authorized, search the chosen decision register for an overlapping record before creating a duplicate.

| Mode | Use when | Action |
|---|---|---|
| New | No matching record exists, or the user wants a fresh decision | Frame and classify it. |
| Resume | An open decision exists and the user wants to continue | Append new inputs; do not rewrite history. |
| Commit | An open decision exists and the user is ready to decide | Check readiness, resolve, and record. |
| Review | A resolved decision has reached its review point and lacks a final assessment | Compare actuals with the original prediction. |

For a review, use the original reasoning and prediction as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Put the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing?
- What deadline, event, or evidence triggers the call?
- What result is desired?
- What happens if no action is taken?

If the problem is broad and credible options do not yet exist, generate options before evaluating them. Do not pressure-test a vague problem statement.

## 3. Classify scope

Ask one clarifying question at a time if classification is unclear. Use the unwind-cost test: **What would it cost to reverse this?** Consider money, time, trust, operational disruption, opportunity cost, and reputation. If the cost cannot be named quickly or is uncertain, the decision is probably larger than it first appears.

| Bucket | Meaning | Required treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default. |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; use a light record when useful. |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, and consult relevant stakeholders. |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and named prerequisite conversations. |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: attention may cost more than an imperfect choice.

### Reversible

Use a short working session:

1. List two or three realistic options.
2. For each option, give one strength, one weakness, and a rough effort or cost estimate.
3. Recommend an option and name the decisive reason.
4. If uncertainty is material, choose the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test examines assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and stakeholder objections.

If no relevant pressure test has happened in the current work context, stop and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Proceed only after the pressure test is complete or the user explicitly overrides it with a reason. If it reveals a serious unresolved failure, do not force a commitment. Return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Ask who has relevant expertise, bears consequences, or may reveal a constraint.
4. Give a recommendation labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has happened, unless the user explicitly accepts and records a reason to proceed without it. State what consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture what it enables; what it costs, delays, or prevents; strongest supporting evidence; strongest objection; key assumptions; and cost of reversal. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies tradeoffs.

Keep these categories distinct:

- **User’s stated view:** Only positions actually expressed by the user.
- **Assistant analysis:** The assistant’s recommendation and reasoning.
- **Open question:** Material uncertainty not yet resolved.

Never invent a user lean, confidence level, rationale, response to dissent, or final choice.

## 6. Open, commit, and record

Use the user’s chosen register, document system, or private file. For a new open decision, record context, options, and new inputs only. Leave commitment sections blank. For a commitment, record the actual decision date, the user’s stated confidence in the prediction, a review date, and the next action.

Suggested review defaults: one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. For hard-to-reverse or direction-setting commitments, create a reminder in an authorized calendar or task system; skip it if the user does not authorize that access.

A record should include status (open or resolved), domain, stakes, reversibility, outcome, decision date, review date, and confidence. For non-binary questions, mark the record resolved once the approach is chosen; resolution does not require a yes/no answer.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** [Optional option and tradeoff.]

## Thinking log
### [YYYY-MM-DD]
- New inputs, conversations, data, or events
- How the thinking changed
- User’s stated position today: open / leaning [option] / decided

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
The user’s own reasoning, only when stated by the user.

## What would change my mind
Assumptions or evidence that would justify reversing the choice.

## Prediction
By [DD MMM YYYY or trigger], [observable outcome] will happen or not happen.
Confidence: [X%]

## Worries
The most credible downside or failure mode.

---

## Retrospective
To be completed at review.
```

For a resumed decision, append a new dated thinking-log entry rather than overwriting prior entries. Add genuinely new options to the options section. If the user remains open, summarize the current state and identify the next question to explore.

## 7. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat a bad outcome as proof of a bad process, or a good outcome as proof of a sound process.

## Completion audit and message

Before closing a meaningful decision, check:

- Is the scope appropriate to the real unwind cost?
- Did a hard-to-reverse choice pass the challenge gate or record an explicit override reason?
- Were required stakeholder conversations completed or explicitly deferred with a reason?
- Are user views limited to what the user actually said?
- Is recorded assistant advice explicitly labeled?
- Does the record omit unrelated sensitive information?
- Is the prediction observable, the review date defined, and the next action assigned?

Then summarize:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [DD MMM YYYY]
Review: [DD MMM YYYY or trigger]
Record: [location, if one exists]
```

Use direct language. Challenge weak reasoning with evidence, but do not turn appropriate rigor into endless deliberation. Once readiness gates are met, name the decision and move forward.

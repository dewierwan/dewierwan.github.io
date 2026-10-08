---
name: make-a-decision
description: Match decision rigor to stakes and reversibility, make and record meaningful choices with permission, and review predictions without inventing the user’s views.
---

# Make a decision

Use this workflow to give each decision enough rigor, but no more than it needs. The aim is to make a clear call, record meaningful reasoning only with permission, and learn from results without rewriting history.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices deserve minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user prefers, believes, or decided something they did not actually say.
3. **Separate advice from attribution.** Assistant recommendations belong in conversation and must be labeled as **Assistant analysis**. Add them to a decision record only when the user specifically requests that.
4. **Record only with permission.** “Should we do X?” requests analysis; it does not authorize creating a record. Create or update a record only when the user asks to log, track, open, resume, or commit it, or explicitly agrees to the practice.
5. **Protect privacy and access boundaries.** Before searching or writing shared records, communications, personnel information, customer information, or other sensitive sources, confirm a legitimate purpose and clear authorization. Use the minimum relevant sources and details.
6. **Do not mistake a task for a decision.** If there is no meaningful alternative, say so: “This is an execution task rather than a decision. Let’s plan or do it.”

If a record is visible to other people, confirm that its audience is appropriate before logging sensitive material. For health, relationships, compensation, confidential personnel matters, or similarly private topics, offer a private document or keep the discussion in chat.

## 1. Select the mode

Use the user’s explicit instruction when they provide one. Otherwise, if authorized to access the decision register, search for relevant overlapping records before creating a duplicate.

| Mode | When to use it | Action |
|---|---|---|
| New | No relevant record exists | Frame and classify the decision. |
| Resume | A matching decision remains open | Retrieve it and append new thinking. |
| Commit | An open decision exists and the user is ready to choose | Complete readiness checks, then resolve it. |
| Review | A resolved decision has reached its review date and lacks a final assessment | Compare actuals with the original prediction. |

A resolved decision can mean either answer to a binary question, or simply that a non-binary choice has been made. Do not override a clear instruction such as “start new,” “resume,” “I’ve decided,” or “review.”

For a resumed decision, append information rather than overwriting history. Use the original record as the baseline at review; do not reconstruct old reasoning from memory.

## 2. Frame the decision

Write the question in a form that can be answered. Establish:

- What exactly is being decided?
- Who has decision authority?
- What are the realistic options, including doing nothing when relevant?
- What deadline, trigger, or cost of delay applies?
- What result is desired?
- What happens if no action is taken?

If the problem is open-ended and credible options do not yet exist, generate options before evaluating them. Do not pressure-test a vague problem statement.

## 3. Classify scope

Ask one clarifying question at a time if necessary. Use this test: **What would it cost to unwind this?** Include money, time, trust, operational disruption, opportunity cost, and reputational effects. If the answer cannot be stated quickly or is uncertain, treat the choice as larger than it first appears.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default. |
| Reversible | Moderate stakes and reversible in days or weeks | Compare a few options; use a light record if useful. |
| Hard to reverse | Undoing it has meaningful cost or disruption | Full analysis, challenge gate, and stakeholder check. |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, dissent, and prerequisite conversations. |

If the user calls a decision trivial, test that judgment with the unwind-cost question. If they are stalling on a truly trivial choice, name the cost of delay and recommend a reasonable default.

## 4. Use the appropriate rigor

### Trivial

Choose a reasonable default, give a one-sentence rationale, and move on. Do not create a decision record unless the user asks.

### Reversible

In a short working session:

1. List two or three realistic options.
2. Give each option one meaningful strength, one meaningful weakness, and a rough effort or cost estimate.
3. State a recommendation labeled **Assistant analysis**.
4. Where uncertainty matters, prefer the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before commitment, confirm that the leading option has been pressure-tested in the current work context. A valid pressure test examines assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and major stakeholder objections.

If no relevant pressure test has occurred, stop the commitment flow and say:

> This decision is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Proceed only after the challenge is complete or the user explicitly overrides it with a reason.

Treat the pressure-test result as a decision rule:

- **Green:** No material unresolved objection was found. Continue to commitment after the remaining checks.
- **Amber:** Risks or unknowns remain, but are understood and acceptable, mitigated, or bounded by a test. Continue only if the record names those conditions.
- **Red:** A serious unresolved failure mode, invalid assumption, or better alternative was identified. Do not force commitment. Return to option generation, redesign the leading option, gather a decision-changing fact, or run a bounded test.

After a green or amber result, complete:

1. Options and decision criteria.
2. A pre-mortem: “It is later and this failed. What most likely caused it?”
3. A stakeholder check: who has relevant expertise, bears consequences, or may reveal a constraint?
4. A recommendation, clearly distinguished from the user’s view.

### Direction-setting

Use the hard-to-reverse process plus two gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and represent their strongest case fairly.

The decision is not ready until the required conversation has occurred, unless the user explicitly accepts and records a reason to proceed without it. If rushed, state exactly which consultation, evidence, or dissent is being skipped and why that matters.

## 5. Keep evidence, advice, and user views separate

For each serious option, capture what it enables, what it costs or prevents, the strongest supporting evidence, the strongest objection, key assumptions, and reversal difficulty.

Choose criteria before comparing options. Distinguish non-negotiable requirements from preferences. Use scoring only when it clarifies a real tradeoff rather than disguising judgment.

Maintain these labels:

- **User’s stated view:** Only positions the user has expressed.
- **Assistant analysis:** Recommendations and reasoning from the assistant.
- **Open question:** Material uncertainty not yet resolved.

If the user has not stated a position, write “No position stated yet” or leave that field blank. Never manufacture a lean, confidence percentage, rationale, treatment of dissent, or final choice.

## 6. Commit and record

Before finalizing a meaningful decision, confirm the choice, why it is preferred now, what could change it, next-action owner and date, observable prediction, and the user’s confidence in that prediction.

Use the user’s chosen authorized record system. Suggested fields include status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. Default review periods are one month for reversible choices, three months for hard-to-reverse choices, and six months for direction-setting choices, unless a concrete trigger is better.

For high-stakes decisions, create a reminder in the user’s chosen calendar or task system if authorized. A review-date field alone may be enough for lower-stakes reversible choices.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** [Optional additional option.]

## Thinking log
### [Date]
- New inputs, conversations, data, or events
- How the thinking changed
- User’s stated position today: open / leaning / decided / no position stated yet

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
User’s own reasoning, only when stated by the user.

## What would change my mind
Assumptions or evidence that would justify reversing the choice.

## Prediction
By [date or trigger], [observable outcome] will happen or not happen.
Confidence: [X%]

## Worries
Most credible downside or failure mode.

## Retrospective
To be completed at review.
```

For a new open decision, record only context, options, and actual new inputs. Leave commitment sections blank until the user commits. When resuming, append a dated thinking-log entry rather than replacing earlier reasoning.

## 7. Review outcomes

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare the event with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the evidence, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. A favorable outcome does not prove the process was good; an unfavorable outcome does not prove it was poor.

## Completion message

When the user makes a decision, summarize it clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [DD MMM]
Review: [DD MMM YYYY or trigger]
Record: [location, if one exists]
```

Use direct language and challenge weak reasoning with evidence. Do not let rigor become endless deliberation. Once the appropriate gates are met, name the decision, take the next action, and schedule the learning loop.

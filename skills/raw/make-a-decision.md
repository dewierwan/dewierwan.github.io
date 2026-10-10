---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to apply the right amount of rigor, make a clear call when ready, preserve reasoning for meaningful choices, and learn from outcomes. The goal is not maximum analysis: most decisions should take minutes, while a small number deserve a complete record and later review.

## Core rules

1. **Match rigor to stakes and reversibility.** Spend more time only where reversal is costly or consequences are broad.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may recommend an option in conversation, clearly labeled as assistant analysis. Add it to a record only if the user asks for that.
4. **Record only with permission.** “Should we do X?” asks for analysis, not for a decision record. Create or update a record only when the user asks to log, track, open, or commit it, or explicitly agrees to recording.
5. **Protect privacy and access boundaries.** Before accessing shared communications, personnel information, customer data, or a shared register, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and omit unrelated sensitive personal details.
6. **Do not confuse a task with a decision.** If there is no meaningful alternative, redirect to planning or execution.

If a shared register has an audience beyond the user, confirm that the audience is appropriate before writing. For sensitive matters such as health, relationships, compensation, or confidential personnel issues, offer a private record in the user’s chosen private workspace or keep the discussion in chat.

## 1. Select the mode

Determine whether the work concerns a new or existing decision.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review point and has not yet received a meaningful outcome assessment.

If the user explicitly names the mode, follow that instruction. Otherwise, if authorized to access the decision register, search for overlapping records before creating a duplicate. Search only the authorized register and only for information relevant to the decision.

For a resumed decision, append new information rather than rewriting history. For a review, use the recorded prediction and original reasoning as the baseline rather than reconstructing them from memory.

## 2. Frame the decision

Put the question in a decidable form. Establish:

- What exact choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing where relevant?
- What is the deadline or decision trigger?
- What result is sought?
- What happens if no action is taken?

If the issue is broad and credible options do not yet exist, generate options before evaluating them. If there is only one viable route, say so directly: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time when classification is unclear. Use the cost of unwinding the choice as the main test: consider money, time, trust, operational disruption, opportunity cost, and reputational effects.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default. |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; use a light record if useful. |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, and consult relevant stakeholders. |
| Direction-setting | Shapes strategy, culture, finances, or operations over an extended period | Full analysis, explicit dissent, and named prerequisite conversations. |

If a user calls something trivial, ask what it would cost to unwind. If they cannot state the cost quickly, or the cost is uncertain, treat the choice as at least reversible rather than trivial.

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: continued attention can cost more than an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. For each option, state one major strength, one major weakness, and a rough effort or cost estimate.
3. Recommend an option and name the decisive reason.
4. If uncertainty matters, identify the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

Before committing, pressure-test the leading option. A valid pressure test examines assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and substantial stakeholder objections.

If no relevant pressure test has occurred in the current work context, stop the commitment flow and state:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not bypass the gate merely because the user is in a hurry. Continue only after the pressure test is complete or the user explicitly overrides it with a reason. If the test reveals a serious unresolved failure, return to option generation, redesign the option, gather decision-changing evidence, or run a bounded test.

After the gate is satisfied:

1. Define the options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check stakeholders: who has relevant expertise, bears consequences, or may reveal a constraint?
4. Offer a recommendation labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has occurred, unless the user explicitly accepts and records a reason for proceeding without it. If the work is being rushed, state which consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence in its favor.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies a tradeoff rather than disguising judgment.

Keep these categories distinct:

- **User’s stated view:** Positions the user actually expressed.
- **Assistant analysis:** Recommendation and reasoning supplied by the assistant, identified using the assistant identity active in the current environment.
- **Open question:** Uncertainty not yet resolved.

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

Use the user’s chosen document system, decision register, or private file. A useful record contains status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. Use these review defaults unless the user names a better trigger: one month for reversible choices, three months for hard-to-reverse choices, and six months for direction-setting choices. Add a reminder through the user’s authorized calendar or task system for high-stakes reviews.

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until the user commits. When resuming, append a dated thinking-log entry rather than altering earlier entries.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** [Optional third option.]

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

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat a bad outcome as proof of a bad process, or a good outcome as proof of a sound process.

## Completion message

When a decision is made, summarize it clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [DD MMM]
Review: [DD MMM YYYY or trigger]
Record: [location, if one exists]
```

Use direct language. Challenge weak reasoning with evidence, but do not turn rigor into endless deliberation. Once the appropriate readiness gates are met, name the decision and move forward.

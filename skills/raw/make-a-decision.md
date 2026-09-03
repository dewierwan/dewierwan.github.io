---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make a clear choice with the amount of rigor it deserves. The aim is not to analyze everything deeply. It is to decide quickly when a choice is small, slow down when reversal is costly, preserve the reasoning for important decisions, and learn from the result.

## Core rules

1. **Match rigor to stakes and reversibility.** Most decisions should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user believes, prefers, or decided something they did not actually say.
3. **Separate advice from attribution.** Assistant recommendations belong in conversation and must be labeled as assistant analysis. Include them in a record only if the user specifically asks.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution work. Plan or do the task instead of opening a decision process.
5. **Record only with permission.** “Should we do X?” asks for analysis, not for a record to be created. Create or update a decision record only when the user asks to log, track, open, resume, or commit it, or explicitly agrees to doing so.
6. **Protect privacy and access boundaries.** Before accessing shared communications, personnel information, customer records, or a shared decision register, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and facts.
7. **Do not deliberate indefinitely.** Once the appropriate readiness checks are met, name the decision, assign the next action, and move forward.

If a shared decision register has an audience beyond the decision-maker, confirm that the audience is appropriate before writing. For sensitive topics, including health, relationships, compensation, legal matters, or confidential people issues, offer a private record or keep the discussion in chat. Omit unrelated sensitive personal information even when access is authorized.

## 1. Choose the mode

Determine whether this is a new decision or work on an existing decision.

- **New:** No matching record exists, or the user wants a fresh decision.
- **Resume:** An open decision exists and the user wants to continue thinking.
- **Commit:** An open decision exists and the user is ready to make the call.
- **Review:** A resolved decision has reached its review date and has not yet received a meaningful outcome assessment.

When the user explicitly names a mode, follow it. Otherwise, if authorized to access the selected decision register, search for a substantially overlapping decision before creating a duplicate.

For a resumed decision, retrieve the existing record and append new information instead of overwriting history. For a review, use the original prediction and reasoning as the baseline. Do not recreate them from memory or rewrite them to fit the outcome.

## 2. Frame the decision

Write the decision as a question that can actually be answered. Establish the following before detailed analysis:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing where relevant?
- What deadline, event, or trigger requires a decision?
- What outcome is sought?
- What happens if no action is taken?

If the question is broad and credible options do not yet exist, generate options before evaluating them. Do not pressure-test a vague problem statement.

If only one viable path exists, say so directly:

> This appears to be a task rather than a decision. The next step is to plan or execute it.

Ask one clarifying question at a time when the missing information materially changes the classification or choice.

## 3. Classify scope

Classify the decision by stakes and the practical cost of reversing it.

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not log by default. |
| Reversible | Moderate stakes; can be changed within days or weeks | Compare a few options; use a light record if useful. |
| Hard to reverse | Meaningful cost, disruption, trust loss, or opportunity cost if undone | Full analysis, challenge the leading option, and consult relevant stakeholders. |
| Direction-setting | Shapes strategy, culture, finances, product direction, or operating model for an extended period | Full analysis, explicit dissent, and named prerequisite conversations. |

Use this test if classification is unclear:

> What would it cost to unwind this decision?

Include money, time, operational disruption, trust, legal or contractual exposure, opportunity cost, and reputational effects. If the unwind cost cannot be named quickly, or the uncertainty itself is material, the choice is probably larger than it first appears.

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right rigor

### Trivial

Pick a reasonable default, give a one-sentence rationale, and move on. Do not create a formal record unless the user requests one.

If the user is stalling, name the cost of delay plainly: continued attention may be more expensive than an imperfect choice.

### Reversible

Use a short working session:

1. List two or three realistic options.
2. For each, state one major strength, one major weakness, and a rough effort, time, or cost estimate.
3. Name the decisive tradeoff.
4. Give a recommendation, clearly labeled as assistant analysis unless the user adopts it.
5. If uncertainty is material, choose the smallest reversible test that could change the call.

### Hard to reverse: challenge gate

A hard-to-reverse decision should be pressure-tested before commitment. A valid pressure test examines:

- The leading option’s key assumptions.
- Disconfirming evidence or missing evidence.
- Likely failure modes.
- The strongest alternative.
- Important stakeholder objections or constraints.
- Whether a smaller experiment can reduce uncertainty.

If no relevant pressure test has occurred in the current working context, pause the commitment flow and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not continue merely because someone is in a hurry. Proceed only after the pressure test is complete or the accountable decision-maker explicitly overrides it with a reason.

If the pressure test identifies a serious unresolved failure, do not force a decision. Return to option generation, redesign the option, gather a decision-changing fact, consult a relevant role, or run a bounded test.

After the gate is satisfied:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check stakeholders: who has relevant expertise, bears consequences, controls implementation, or may reveal a constraint?
4. Give a recommendation, labeled as assistant analysis unless the user states the same position in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness checks:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture the strongest opposing case fairly.

The decision is not ready until the required conversation has happened, unless the accountable decision-maker explicitly accepts and records a reason for proceeding without it. If the decision is being rushed, state what consultation, evidence, or dissent is being skipped and why that matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest evidence in its favor.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.
- Who is affected and what they need to know.

Choose decision criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies tradeoffs; do not use a score to disguise judgment or false precision.

Keep these categories distinct in conversation and records:

| Category | What belongs there | Rule |
|---|---|---|
| User’s stated view | Positions, preferences, confidence, and reasoning directly expressed by the user | Quote or accurately paraphrase only what was stated. |
| Assistant analysis | Recommendation, critique, synthesis, and reasoning supplied by the assistant | Label it clearly and do not present it as the user’s view. |
| Open question | Missing evidence, unresolved assumptions, or pending conversations | Keep it visibly unresolved. |

If the user has not expressed a position, write “No position stated yet” or leave the user-position field blank. Never invent a lean, confidence level, rationale, response to dissent, or final choice for them.

## 6. Commit and record

Before finalizing a meaningful decision, confirm:

- What is the decision?
- Which option was chosen?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable result is predicted?
- What is the decision-maker’s confidence in that prediction?

Make the prediction testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Use the user’s chosen decision register, document system, or private file. A useful record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. Suitable review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar, task system, or equivalent reminder for high-stakes reviews.

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until the decision-maker commits. For a resumed decision, append a new dated thinking-log entry rather than rewriting prior entries.

```markdown
## Context
Why this decision exists and why it matters now.

## Options considered
- **Option A:** What it is and its central tradeoff.
- **Option B:** What it is and its central tradeoff.
- **Option C:** [Optional additional option.]

## Thinking log
### [Date]
- New inputs, conversations, data, or events.
- How the thinking changed.
- Decision-maker’s stated position today: open / leaning / decided.

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
The decision-maker’s own reasoning, only when they have stated it.

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

## 7. Review the outcome

At the review point, assess the decision in four parts:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Keep decision quality separate from outcome quality: a sound decision can have a bad result because of uncertainty, and a weak process can occasionally produce a good result.

## 8. Final audit checks

Before sending a recommendation, commitment summary, or record update, check:

- Is this genuinely a decision rather than a task?
- Is the scope classification justified by reversal cost and stakes?
- Has the required pressure test occurred, or was its omission explicitly accepted with a reason?
- For a direction-setting decision, have the required conversations and dissent pass occurred?
- Are facts, the user’s stated view, assistant analysis, and open questions clearly separated?
- Was a record created or updated only with permission?
- Is the record visible only to an appropriate audience?
- Does the record omit irrelevant sensitive information?
- Is the prediction observable and the review date appropriate?
- Is there a concrete next action with an owner and date?

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

Use direct language. Challenge weak reasoning with evidence, but do not turn rigor into endless deliberation. Once the right readiness gates are met, make the call and proceed.

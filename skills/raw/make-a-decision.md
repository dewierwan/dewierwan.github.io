---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to make decisions with the right amount of rigor. The aim is a clear, timely call, not maximum analysis. Record meaningful decisions only with permission, preserve the decision-maker’s actual reasoning, and learn from results.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices deserve minutes, not days.
2. **The decision-maker owns their position.** Never state, record, or imply that they favor, believe, or chose something they have not actually said.
3. **Separate advice from attribution.** Assistant recommendations belong in the conversation and must be labeled as assistant analysis. Add them to a record only if the user requests that.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, this is execution. Plan or do the task instead.
5. **Record only with explicit permission.** “Should we do X?” asks for analysis, not for a permanent record. Create or update a record only when the user asks to log, track, open, update, or commit the decision, or clearly agrees to doing so.
6. **Respect privacy and access boundaries.** Before searching a decision register, shared communications, personnel material, or other records about people, establish a legitimate purpose and clear authorization. Use the minimum relevant sources and details. Exclude unrelated personal, confidential, or sensitive information.

If a record will be visible to others, confirm that the audience is appropriate. For sensitive subjects, such as health, relationships, compensation, or confidential people matters, offer a private record in the user’s chosen private workspace or keep the discussion in chat.

## 1. Select the mode

If the user explicitly says to start, resume, commit, or review a decision, follow that instruction. Otherwise, if authorized, search the available decision register for an overlapping record before creating a duplicate.

| Mode | When to use it | Action |
|---|---|---|
| New | No matching decision exists | Frame and classify the decision |
| Resume | A matching record is still open | Append new inputs and continue analysis |
| Commit | An open decision exists and the user is ready to decide | Complete readiness checks and record the commitment |
| Review | A resolved decision has reached its review date | Compare actual outcomes with the original prediction |

For a resume, append information rather than rewriting the history. For a review, use the original prediction and reasoning as the baseline instead of reconstructing them from memory.

## 2. Frame the question

Write the decision as a concrete, decidable question. Establish:

- What choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing where relevant?
- What deadline, event, or trigger requires a decision?
- What result is desired?
- What happens if no action is taken?

If the issue is broad and credible options do not yet exist, generate options first. Do not pressure-test a vague problem statement. If there is only one viable path, say: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time when classification is unclear. Use the cost of reversal as the primary test: consider money, time, trust, operational disruption, opportunity cost, and reputational effects. If the unwind cost cannot be named quickly, the choice is likely larger than it first appears.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not record by default |
| Reversible | Moderate stakes and reversible in days or weeks | Compare a few options; use a light record if useful |
| Hard to reverse | Meaningful cost, disruption, or loss if undone | Full analysis, challenge the leading option, and consult relevant people |
| Direction-setting | Shapes strategy, operating model, culture, or finances for a long period | Full analysis, explicit dissent, and named prerequisite conversations |

## 4. Apply the appropriate rigor

### Trivial

Choose a reasonable default, state a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: attention spent debating may exceed the cost of an imperfect choice.

### Reversible

Use a short working session:

1. List two or three realistic options.
2. For each, state one major strength, one major weakness, and a rough effort, cost, or time estimate.
3. Recommend an option and identify the decisive reason.
4. If uncertainty matters, choose the smallest reversible test likely to change the call.

### Hard to reverse: challenge gate

Before committing, pressure-test the leading option. A valid challenge examines core assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and important stakeholder objections.

If no relevant pressure test has occurred in the current decision context, stop and say:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Do not bypass this gate merely because the user is in a hurry. Proceed only after the pressure test is complete or the user explicitly overrides it with a reason. If it exposes a serious unresolved problem, return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

After the gate is met:

1. Define options and decision criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check relevant stakeholders: who has expertise, bears consequences, or may reveal a constraint?
4. Give a recommendation, clearly labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has happened, unless the user explicitly accepts and records a reason for proceeding without it. If the decision is being rushed, state what consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture:

- What it enables.
- What it costs, delays, or prevents.
- Strongest supporting evidence.
- Strongest objection.
- Key assumptions.
- Ease and cost of reversal.

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scores only when they clarify tradeoffs rather than hiding judgment.

Keep these categories distinct:

- **Decision-maker’s stated view:** Positions they actually expressed.
- **Assistant analysis:** The assistant’s recommendation and reasoning.
- **Open question:** Important uncertainty not yet resolved.

If the decision-maker has not expressed a view, write “No position stated yet” or leave their position blank. Never invent their lean, confidence, rationale, response to dissent, or final choice.

## 6. Commit and record

Before finalizing, confirm:

- What is the decision?
- Which option was chosen?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable result is predicted?
- What is the decision-maker’s confidence in that prediction?

For meaningful decisions, make the prediction testable:

> By [date or trigger], [observable outcome] will happen or will not happen.  
> Confidence: [percentage].

Use the user’s chosen document system, register, or private file. A useful decision record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome. Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Use a calendar, task system, or equivalent reminder for high-stakes reviews.

For a new open decision, record context, current options, and new inputs. Leave commitment sections blank until a choice is made. When resuming, append a dated thinking entry rather than replacing earlier reasoning.

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
- Decision-maker’s stated position today: open / leaning / decided

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
The decision-maker’s own reasoning, only when they have stated it.

## What would change my mind
Assumptions or evidence that would justify reversing the choice.

## Prediction
By [date], [observable outcome] will happen or will not happen.
Confidence: [X%]

## Worries
The most credible downside or failure mode.

## Retrospective
To be completed at review.
```

## 7. Review the outcome

At the review point, assess four separate questions:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Do not treat a bad outcome as proof of a bad decision process, or a good outcome as proof of sound reasoning.

## Completion message

When a decision is made, summarize it clearly:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences]
Next action: [owner] will [action] by [DD MMM]
Review: [DD MMM or trigger]
Record: [location, if one exists]
```

Use direct language and challenge weak reasoning with evidence. Do not let rigor become endless deliberation: once the appropriate readiness gates are met, name the decision and move forward.

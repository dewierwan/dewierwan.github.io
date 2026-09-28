---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, make a clear call when ready, and, with authorization, record and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to apply enough rigor for the decision at hand, not maximum rigor by default. The aim is to make clear choices, preserve reasoning when it matters, and learn from outcomes without turning every question into a major project.

## Core rules

1. **Match rigor to stakes and reversibility.** Many choices deserve only a few minutes. A small number deserve structured analysis, consultation, a record, and a review.
2. **The user owns their position.** Never state, record, or imply that the user prefers, believes, leans toward, or decided something unless they actually said it.
3. **Separate advice from attribution.** The assistant may recommend an option in chat, labeled **Assistant analysis**. Add it to a record only if the user explicitly asks.
4. **Record only with permission.** “Should we do X?” requests analysis, not a new record. Create or update a record only when the user asks to log, track, open, update, or commit the decision, or has explicitly agreed to that practice.
5. **Use information lawfully and minimally.** Before accessing shared communications, personnel records, customer information, or a decision register, establish a legitimate decision-related purpose and clear authorization. Retrieve only sources needed for that purpose, extract only relevant facts, and do not copy unrelated personal or sensitive information into the analysis or record.
6. **Respect consent, confidentiality, and output boundaries.** Consider whether people reasonably expect their information to be used for this decision. For sensitive topics, confirm that use and sharing are appropriate. Keep the resulting analysis and record visible only to people with a legitimate need to know and authorized access.
7. **Do not confuse a task with a decision.** If there are no meaningful alternatives, this is execution. State that plainly and move to planning or doing the work.
8. **Do not deliberate forever.** Once the appropriate checks are complete, name the decision, set the next action, and move on.

If a record is visible to colleagues, managers, advisors, or other third parties, confirm that this audience is appropriate before writing. For health, relationships, compensation, confidential personnel matters, legal matters, or similarly sensitive subjects, offer a private document or keep the discussion in chat. Do not include diagnoses, private communications, protected characteristics, or personal details unless they are necessary, authorized, and relevant to the decision.

For hiring, performance, or other people-related decisions, focus on role-relevant capabilities, evidence from appropriate assessments, job requirements, and documented constraints. Do not use unrelated personal information. Confirm that any assessment actually distinguishes relevant performance and that the review process is authorized.

## 1. Determine the mode

First identify whether the decision is new, active, ready to commit, or ready to review. If the user explicitly says which mode they want, follow that instruction. Otherwise, search an existing register only if the user has authorized access and the search is necessary to avoid duplicate or incomplete records.

| Mode | Meaning | Action |
|---|---|---|
| New | No relevant record exists, or the user wants a fresh decision | Frame and classify the decision |
| Resume | An existing decision remains open | Retrieve it and append new inputs without rewriting history |
| Commit | An open decision exists and the user is ready to decide | Confirm the call, complete the record, and schedule review |
| Review | A resolved decision has reached its review date and has no completed outcome assessment | Compare actuals with the original prediction |

Use this detection sequence when the user has not specified a mode:

1. Search authorized records for matching titles, descriptions, or decision questions.
2. Treat a matching open record as a possible resume flow. If the user signals a final call, use commit flow instead.
3. Treat a resolved record as review-ready when its review date is due or past and its outcome is blank or marked **Too early**.
4. Trust an explicit user instruction over automated matching.

Do not search broadly through private communications or people records merely to find supporting material. Ask for a relevant source, a summary, or permission to inspect a defined set of sources when necessary.

## 2. Frame the decision

Put the choice in a decidable form before evaluating it. Establish:

- What exactly is being decided?
- Who has decision authority?
- What are the realistic options, including doing nothing where relevant?
- What deadline, trigger, or opportunity window applies?
- What result is desired?
- What happens if no action is taken?
- What evidence is needed, and what sources may legitimately be consulted?

If the question is broad and there are no credible options yet, generate options first. Do not pressure-test a vague problem statement. If there is only one viable path, say: “This appears to be a task rather than a decision. The next step is to plan or execute it.”

## 3. Classify scope

Ask one clarifying question at a time if needed. The most useful test is: **What would it cost to unwind this?** Consider money, time, trust, operational disruption, opportunity cost, and reputation. If the reversal cost is difficult to name quickly, the choice may be bigger than it initially appears.

| Bucket | Meaning | Typical treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not record by default |
| Reversible | Moderate stakes and reversible in days or weeks | Compare a few options; create a light record if useful |
| Hard to reverse | Significant cost, disruption, or lost trust if undone | Full analysis, challenge the leading option, and consult relevant people |
| Direction-setting | Likely to shape strategy, culture, finances, or operating model for a long period | Full analysis, explicit dissent, and required conversations before commitment |

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

If the user calls something trivial but cannot name the undo cost or consequences, challenge the classification. Conversely, do not inflate a low-cost, reversible choice into a strategic exercise.

## 4. Apply the right rigor

### Trivial decisions

Choose a reasonable default, state a one-sentence rationale, and finish. Do not create a record by default. If the user is stalling, name the cost of delay: attention spent debating may cost more than an imperfect choice.

### Reversible decisions

Run a short comparison:

1. List two or three realistic options.
2. For each option, state one major strength, one major weakness, and rough effort or cost.
3. Recommend an option and identify the decisive reason.
4. If uncertainty remains material, choose the smallest reversible test that could change the call.

### Hard-to-reverse decisions: pressure-test gate

Do not commit a hard-to-reverse decision until the leading option has been challenged. A valid pressure test examines:

- Core assumptions and what would disprove them.
- Evidence against the leading option.
- Likely failure modes.
- The strongest alternative.
- Major objections from people with relevant expertise or who will bear material consequences.

If no relevant pressure test has occurred in the current decision context, pause the commitment flow and say:

> This decision is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Proceed only after a completed challenge or an explicit override with a reason. Use the result as a decision rule:

- **Clear or manageable concerns:** Continue with options, a pre-mortem, stakeholder checks, and a recommendation.
- **Material but resolvable concerns:** Continue only after recording the mitigation, test, owner, or evidence needed to resolve them.
- **Serious unresolved concern:** Do not force commitment. Return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

After the gate is satisfied, define options and criteria, run a pre-mortem, check relevant stakeholders, and give a recommendation labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting decisions

Use the hard-to-reverse process plus two further readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation that must happen before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required conversation has happened, unless the user explicitly accepts and records a reason for proceeding without it. If the decision is being rushed, state which consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture what it enables; what it costs, delays, or prevents; strongest supporting evidence; strongest objection; key assumptions; and ease and cost of reversal. Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies tradeoffs rather than disguising judgment.

| Category | What belongs there |
|---|---|
| User’s stated view | Only positions, confidence, and reasons the user actually expressed |
| Assistant analysis | The assistant’s recommendation, evidence, and reasoning |
| Open question | Uncertainty not yet resolved or evidence still needed |

If the user has not stated a position, write “No position stated yet” or leave the user-position field blank. Never invent a lean, confidence percentage, rationale, response to dissent, or final choice for them.

When using information about other people, summarize only decision-relevant evidence. Avoid names and identifying details where roles or anonymized descriptions will do. Do not treat hearsay as fact, and distinguish documented evidence from opinion.

## 6. Record a meaningful decision

Use the user’s chosen document system, decision register, or private file. Use an approved template where one exists. Before writing, confirm the record’s access audience, retention expectations, and whether sensitive details should be omitted or stored privately.

| Field | Example value |
|---|---|
| Status | Open, resolved: yes, or resolved: no |
| Area | Strategy, operations, product, finance, people, or personal |
| Stakes | Low, medium, high, or direction-setting |
| Reversibility | Reversible, hard, or one-way |
| Decision date | Date the user actually made the call |
| Review date | Date or trigger for retrospective |
| Confidence | User’s confidence in the prediction at decision time |
| Outcome | Correct, incorrect, mixed, too early, or not applicable |

For a non-binary question, use a resolved status once the chosen approach is settled. Resolution means the decision has been made; it does not imply that the answer was literally yes or no.

### Open record

For a decision the user wants to continue across sessions:

- Set status to **Open**.
- Record scope, area, reversibility, context, factual inputs, and current options.
- Add a dated thinking-log entry with new inputs and changes in reasoning.
- Leave commitment-only sections blank unless the user has supplied their own content.
- Do not add a user lean if none was stated.

### Committed record

When the user makes the call:

- Set the resolved status appropriate to the decision question.
- Set the decision date to the date the user actually committed.
- Record the user’s confidence in the prediction only if they provide it.
- Set a review date. Useful defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions.
- Clearly label any requested assistant content as **Assistant analysis, not the user’s position**.

Before finalizing, confirm the choice, rationale, reversal conditions, next-action owner and date, observable prediction, and confidence. For high-stakes commitments, create a reminder in an approved calendar or task system only with authorization. Keep reminder titles and descriptions free of unnecessary sensitive information.

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
- User’s stated position today: open / leaning / decided

## Dissent
Relevant objections, their strongest argument, and how they were handled.

## My choice and why
The user’s own reasoning, only when stated by the user.

## What would change my mind
Assumptions or evidence that would justify reversing the choice.

## Prediction
By [date], [observable outcome] will happen or will not happen.
Confidence: [X%]

## Worries
The most credible downside or failure mode.

---

## Retrospective
To be completed at review.
```

When resuming, append a new dated thinking-log entry rather than rewriting history.

## 7. Review the outcome

At the review point, use the original record as the baseline:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare results with the recorded prediction and confidence.
3. **Was the process sound?** Evaluate the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle that can improve a future decision.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. Keep outcome quality separate from decision quality: a sound decision can have a poor outcome because of uncertainty, and a weak process can get lucky.

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

Use direct language. Challenge weak reasoning with evidence, but do not use rigor as a reason to delay indefinitely. After a decision, improve the workflow only through an authorized and transparent process.

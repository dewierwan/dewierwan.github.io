---
name: make-a-decision
description: Match decision-making rigor to stakes and reversibility, then make, record, and review meaningful choices without inventing the user’s views or exposing sensitive information.
---

# Make a decision

Use this workflow to reach a clear decision with an appropriate amount of analysis. The aim is not maximum deliberation: make small choices quickly, apply stronger safeguards to consequential choices, record meaningful decisions only with authorization, and learn from outcomes.

## Core rules

1. **Match rigor to stakes and reversibility.** Most choices should take minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user prefers, believes, is leaning toward, or decided something they did not actually say.
3. **Separate advice from attribution.** The assistant may give a recommendation in chat, clearly labeled **Assistant analysis**. Add it to a record only when the user asks for it there.
4. **Do not confuse a task with a decision.** If there is no meaningful alternative, plan or execute the work instead of opening a decision process.
5. **Record only with permission.** “Should we do X?” requests analysis, not a new record. Create or update a record only when the user asks to log, track, open, resume, or commit it, or has explicitly agreed to an established recording practice.
6. **Protect privacy and access boundaries.** Before searching a shared register or using private communications, personnel information, customer information, or other records, establish a legitimate purpose and clear authorization. Use the minimum relevant sources and facts. Omit unrelated personal or sensitive details.
7. **Do not use rigor as delay.** Once the relevant readiness gates are met, name the decision and proceed.

If a decision record is visible to other people, confirm its audience is appropriate before writing. For sensitive topics, including health, relationships, compensation, confidential personnel matters, or private legal matters, offer a private record or keep the discussion in chat.

## 1. Determine the working mode

If the user explicitly says they want to start, resume, commit, or review a decision, follow that instruction. Otherwise, if authorized, search the chosen decision register for a substantially overlapping record before creating a duplicate.

| Mode | When to use it | Required action |
|---|---|---|
| New | No relevant record exists, or the user requests a fresh decision | Frame and classify it. |
| Resume | A matching record is open and the user wants to continue thinking | Retrieve it and append new information. |
| Commit | An open decision exists and the user is ready to make the call | Confirm readiness, then resolve it. |
| Review | A resolved decision has reached its review date and its outcome is blank or still marked too early | Compare actuals with the original prediction. |

For a resumed decision, append new information rather than rewriting history. For a review, use the original prediction, confidence, assumptions, and stated rationale as the baseline. Do not replace them with hindsight.

## 2. Frame a decidable question

Establish:

- What exact choice is being made?
- Who has final decision authority?
- What are the realistic options, including doing nothing where relevant?
- What is the deadline, trigger, or cost of waiting?
- What result is desired?
- What happens if no action is taken?

If the issue is broad and credible options do not exist yet, generate options before evaluating them. Do not pressure-test a vague problem statement.

If only one viable path exists, say so plainly:

> This appears to be a task rather than a decision. The next step is to plan or execute it.

## 3. Classify the scope

Ask one clarifying question at a time if needed. Classify by consequences and cost of reversal, not by how emotionally difficult the choice feels.

| Bucket | Meaning | Default treatment |
|---|---|---|
| Trivial | Low stakes and reversible within hours | Decide now; do not record by default. |
| Reversible | Moderate stakes and reversible within days or weeks | Compare a few options; use a light record when authorized. |
| Hard to reverse | Meaningful cost, disruption, lost trust, or strategic impact if undone | Full analysis, challenge gate, stakeholder check, and full record when authorized. |
| Direction-setting | Shapes strategy, culture, finances, or operating model for an extended period | Full analysis, explicit dissent, and a named prerequisite consultation. |

Use this test when uncertain:

> What would it cost to unwind this?

Consider money, time, trust, operational disruption, opportunity cost, contractual constraints, and reputational effects. If the unwind cost cannot be stated quickly, or remains highly uncertain, treat the decision as larger rather than smaller.

| Bucket | Typical stakes | Typical reversibility |
|---|---|---|
| Trivial | Low | Easy |
| Reversible | Low or medium | Reversible |
| Hard to reverse | High | Hard |
| Direction-setting | Very high | Difficult or effectively one-way |

## 4. Apply the right level of rigor

### Trivial

Choose a reasonable default, give a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: continued attention may cost more than an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. For each, state one meaningful strength, one meaningful weakness, and a rough effort, time, or cost estimate.
3. Identify the decisive tradeoff.
4. Give a recommendation labeled as Assistant analysis unless the user adopts it in their own words.
5. If uncertainty is material, choose the smallest reversible test likely to change the call.

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test examines its key assumptions, disconfirming evidence, strongest alternative, likely failure modes, stakeholder objections, and relevant reversal conditions.

If no relevant pressure test has been completed in the current work context, stop the commitment flow and state:

> This decision is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Continue only after the pressure test is complete or the user explicitly overrides it with a reason. If it reveals a serious unresolved failure, do not force commitment. Return to option generation, redesign the option, obtain a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and criteria.
2. Run a pre-mortem: “It is later and this failed. What most likely caused it?”
3. Check stakeholders with relevant expertise, consequences, or hidden constraints.
4. Provide a recommendation as Assistant analysis unless the user states their own choice.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees and capture their strongest case fairly.

The decision is not ready until the required consultation has happened, unless the user explicitly accepts and records a reason for proceeding without it. If it is being rushed, name what consultation, evidence, or dissent is being skipped and why it matters.

## 5. Analyze without manufacturing certainty

For each serious option, capture what it enables; what it costs, delays, or prevents; its strongest supporting evidence; its strongest objection; its key assumptions; and the ease and cost of reversal.

Choose criteria before comparing options. Separate non-negotiable requirements from preferences. Use scoring only when it clarifies a real tradeoff rather than disguising judgment as precision.

Keep these categories separate in conversation and records:

| Category | Rule | Example |
|---|---|---|
| User’s stated view | Include only positions actually expressed by the user | “The user stated a preference for Option B.” |
| Assistant analysis | Label assistant advice and reasoning | “Assistant analysis: Option A reduces execution risk.” |
| Open question | Identify uncertainty without treating it as resolved | “Unknown: whether the provider can meet the timeline.” |

If the user has not expressed a position, write “No position stated yet” or leave the user-position field blank. Never invent a lean, confidence level, rationale, response to dissent, or final choice.

## 6. Open, commit, and maintain a record

Use the user’s chosen decision register, document system, or private file. If an organization has an approved practice for recording non-trivial decisions, use it only within the user’s access and authorization boundary.

A record should include at least these fields:

| Field | Purpose | Example value |
|---|---|---|
| Status | Whether the decision remains open or has been resolved | Open; Resolved: Yes; Resolved: No |
| Type or domain | Area affected | Strategy; operations; finance |
| Stakes and reversibility | Rigor and unwind context | High; hard to reverse |
| Decision and review dates | Timing for commitment and learning | [Date] |
| Confidence | User’s confidence in the prediction at decision time | [X%] |
| Outcome | Prediction result, distinct from process quality | Too early; correct; incorrect; mixed; not applicable |

For non-binary questions, use a resolved status once a direction is chosen. Resolution is about whether the call was made, not whether the question has a yes-or-no form.

### Open record

For a decision the user wants to think about across sessions, record the context, options, and factual new inputs. Set its status to open. Leave commitment sections, including the user’s choice, confidence, prediction, and worries, blank unless the user has actually provided them.

### Commit record

Before resolving a meaningful decision, confirm:

- What is the decision and chosen option?
- Why is it preferred now?
- What would change the decision?
- Who owns the next action, and by when?
- What observable result is predicted?
- What is the user’s confidence in that prediction?

Make predictions testable:

> By [date or trigger], [observable outcome] will happen or not happen.  
> Confidence: [percentage].

Set the decision date to when the user actually made the call. Suggested review defaults are one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Adjust when the user identifies a more meaningful trigger.

For hard-to-reverse and direction-setting decisions, create a reminder in the user’s calendar, task system, or other reminder tool when available and authorized. Include the review date, decision question, and permitted link or record location. A record-level review date is usually sufficient for reversible decisions.

Use this body structure:

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

---

## Retrospective
To be completed at review.
```

When resuming an open record, append a new dated thinking-log entry and add newly credible options without deleting earlier history. If the user remains open, summarize the current state and identify what to explore next rather than filling commitment sections.

## 7. Review the outcome

At the review point, assess four separate questions:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle that can improve future decisions.

Update the record’s outcome to correct, incorrect, mixed, too early, or not applicable, and fill the retrospective. Do not collapse a bad outcome into a bad process, or a good outcome into a sound process.

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

Use direct language. Challenge weak reasoning with evidence while preserving the user’s ownership of the decision. Once the appropriate rigor has been applied, make the call and move forward.

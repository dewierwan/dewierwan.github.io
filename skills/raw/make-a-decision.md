---
name: decide
description: Matches decision rigor to stakes and reversibility, records the call with a testable prediction, and reviews it later. Use when asked to help decide, weigh X against Y, or review a past decision.
---

# Make a decision

Use this workflow to apply the right amount of rigor to a decision. Small choices get made quickly. Consequential choices get examined properly, recorded only with permission, and reviewed later without rewriting history.

## Quick version

- Ask what it would cost to unwind the choice. Sort it as trivial, reversible, hard to reverse, or direction-setting.
- If one urgent, reversible choice is bundled with a slower, harder one, split them. Answer the urgent part now and handle the harder part separately.
- For trivial choices, pick a sensible default with a one-sentence reason. For reversible choices, compare two or three options with one strength, one weakness, and rough effort each.
- For hard-to-reverse or direction-setting choices, pressure-test the leading option and check who disagrees before committing.
- Never claim the user leans toward or decided something they did not say. Keep the assistant's recommendation clearly labeled as the assistant's.
- When the user commits, write down a testable prediction, their confidence in it, the next action, and a review date set for when real results will exist. At review, judge the prediction and the process separately.

## 1. Ground rules

1. **Match rigor to stakes and reversibility.** Most decisions deserve minutes, not days.
2. **The user owns their position.** Never state, record, or imply that the user prefers, believes, or decided something they did not actually say. A fabricated lean puts a position the user never held on their own record.
3. **Separate advice from attribution.** Keep the assistant's recommendation distinct from the user's stated view. Include assistant analysis in a record only on request, and label it clearly.
4. **Record only with permission.** "Should we do X?" asks for analysis, not for a record. Create or update a decision record only when the user asks to log, track, open, resume, or commit it, or explicitly agrees.
5. **Do not mistake execution for a decision.** If there is no meaningful alternative, say so and move to planning or doing the work.
6. **Do not deliberate indefinitely.** Once appropriate evidence, challenge, and consultation are complete, make the call and proceed.

Before searching a shared decision register or reading communications, personnel records, or customer information about other people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and details, leave out unrelated or sensitive personal information, and keep outputs within an appropriate access boundary.

Be accurate about who can see the record. Rely on what the user has told you or what you can verify, not on assumptions or outdated notes. Do not tell the user a record is shared or private unless you know it, and if they correct you, update your understanding and stop repeating the old claim.

## 2. Select the mode

Use the user's explicit instruction when they give one. Otherwise, if access is authorized, check the user's chosen decision record for a substantially overlapping decision before creating a duplicate.

- **New:** No matching record exists, or the user asks to start fresh.
- **Resume:** A matching record is open and the user wants to keep thinking.
- **Commit:** An open record exists and the user says they are ready to decide.
- **Review:** A resolved record has reached its review date and has no completed outcome assessment, or is still marked "too early."

Resolution status means whether the decision was made, not whether the outcome was good. For a non-binary question, mark it resolved once a direction has been chosen.

For **Resume**, retrieve the record, append a dated entry with new inputs, how thinking shifted, and where the user stands today, and add any new options. Do not overwrite prior reasoning. If the user wants to keep thinking, summarize the current state and ask what to explore next. If they are ready, move to commitment. For **Review**, use the original prediction, confidence, and stated assumptions as the baseline.

## 3. Frame the decision

Put the question in a decidable form. Establish:

- What choice is being made?
- Who has final decision authority?
- What realistic options exist, including doing nothing?
- What deadline, event, or trigger requires a decision?
- What result is sought?
- What happens if no action is taken?

If the issue is broad and credible options do not yet exist, generate options first. Do not pressure-test a vague problem statement.

If only one viable path exists, say:

> This appears to be a task rather than a decision. The next step is to plan or execute it.

Ask one clarifying question at a time when scope is unclear.

## 4. Classify scope

| Bucket | Meaning | Treatment |
|---|---|---|
| Trivial | Low stakes; reversible within hours | Decide now; do not record by default. |
| Reversible | Moderate stakes; changeable within days or weeks | Compare a few options; use a light record if useful. |
| Hard to reverse | Significant cost, disruption, or loss if undone | Full analysis, challenge gate, and stakeholder check. |
| Direction-setting | Shapes strategy, culture, finances, or operations for an extended period | Full analysis, explicit dissent, and prerequisite conversations. |

When classification is unclear, ask: **What would it cost to unwind this?** Consider money, time, trust, operational disruption, opportunity cost, and reputation. If the unwind cost cannot be named quickly or is highly uncertain, treat the decision as larger. If the user calls a decision trivial but cannot explain how to undo it quickly, reclassify it rather than accepting the label.

**Split bundled decisions.** A request often mixes an urgent, reversible step with a slower, harder choice. Separate them. Answer the urgent step now as a reversible decision, then classify and gate the harder one on its own terms. This prevents urgency from rushing the big choice and prevents the big choice from blocking a simple step.

*Fictional example:* A manager at Tallowbrook Studio asks, "Should I tell the admin team to pause the lease renewal paperwork today, and should we move to a new building?" Pausing the paperwork for a week is reversible and time-sensitive, so it gets a quick answer: yes, pause it, because the renewal deadline is still a month away. Moving buildings is hard to reverse, so it goes through the full challenge gate separately.

## 5. Apply the appropriate rigor

### Trivial

Choose a reasonable default, state a one-sentence rationale, and move on. If the user is stalling, name the cost of delay: attention spent may exceed the cost of an imperfect choice.

### Reversible

In a short working session:

1. List two or three realistic options.
2. For each, state one main strength, one main weakness, and a rough effort or cost.
3. Give a recommendation and the decisive reason.
4. If uncertainty is material, identify the smallest reversible test that could change the call.

| Option | Main strength | Main weakness | Effort or cost |
|---|---|---|---|
| [Option A] | [What it enables] | [Central tradeoff] | [Rough estimate] |

### Hard to reverse: challenge gate

Before commitment, pressure-test the leading option. A valid pressure test covers assumptions, disconfirming evidence, likely failure modes, the strongest alternative, and major stakeholder objections.

If no relevant pressure test has happened in the current decision context, stop the commitment flow and state:

> This is hard to reverse. Pressure-test the leading option before committing. To proceed without that step, explicitly state why the gate is being skipped.

Proceed only after the test is complete or the user explicitly overrides the gate with a reason. Urgency alone is not an override; if urgency is real, check whether a smaller reversible step can be split off instead.

If the pressure test finds a serious unresolved failure, do not force commitment. Return to option generation, redesign the option, gather a decision-changing fact, or run a bounded test.

After the gate is satisfied:

1. Define options and criteria.
2. Run a pre-mortem: "It is later and this failed. What most likely caused it?"
3. Check with people who have relevant expertise, bear consequences, or may reveal constraints.
4. Provide a recommendation labeled as assistant analysis unless the user adopts it in their own words.

### Direction-setting

Use the hard-to-reverse process plus two readiness gates:

1. Name the specific accountable leader, partner, advisor, or stakeholder conversation required before commitment.
2. Ask who disagrees, and capture their strongest case fairly.

The decision is not ready until the prerequisite conversation has occurred, unless the user explicitly accepts and records a reason for proceeding without it. If it is rushed, name what evidence, consultation, or dissent is being skipped and why that matters.

For people-related decisions, use role-relevant capabilities, role alignment, diagnostic evidence, and whether any assessment distinguishes relevant performance. Do not rely on irrelevant personal information or unsupported labels.

## 6. Analyze without inventing certainty

For each serious option, capture what it enables; what it costs, delays, or prevents; its strongest supporting evidence and objection; its key assumptions; and the cost of reversal.

Separate non-negotiable requirements from preferences. Use scores only if they clarify tradeoffs rather than conceal judgment.

Keep these categories separate:

- **User's stated view:** Only what the user actually expressed.
- **Assistant analysis:** The assistant's recommendation and reasoning.
- **Open question:** Material uncertainty not yet resolved.

If the user has not stated a position, write "No position stated yet" or leave the field blank. Never fabricate a lean, confidence level, rationale, response to dissent, or final choice.

## 7. Commit and record

Before finalizing, confirm the choice, rationale, reversal conditions, next action owner and date, observable prediction, and the user's confidence in that prediction.

Use a testable prediction:

> By [date or trigger], [observable outcome] will happen or not happen.
> Confidence: [percentage].

Use the user's chosen register, document, or private file. A useful record includes status, domain, stakes, reversibility, decision date, review date, confidence, and outcome.

For an **open** decision, record context, options, and new inputs, but leave commitment sections blank. For a **commitment**, mark it resolved, record the actual decision date, set confidence, and fill the commitment sections. Do not infer missing user-owned fields.

Suggested default review timing, adjustable: about one month for reversible decisions, three months for hard-to-reverse decisions, and six months for direction-setting decisions. Prefer a meaningful event or trigger if the user names one.

**Check that results will exist by the review date.** Before proposing a date, ask what will actually be observable by then. If the thing being decided will not yet have launched or produced outcomes, move the review to when early outcomes become visible, and frame it as a checkpoint on leading signals rather than a chance to re-decide.

*Fictional example:* Harrowgate Learning commits to starting a mentorship program next term. A default three-month review would land before the first cohort has met more than twice. The review moves to when early retention and participant feedback exist, and its question becomes "Are the early signals on track?" rather than "Should we have launched?"

For hard-to-reverse and direction-setting commitments, make sure a review reminder exists. In a plain chat, give the user a reminder-ready line to add to their own calendar or task list. Use one consistent, unambiguous date format throughout the record.

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
- User's stated position today: open / leaning / decided

## Dissent
Who pushed back, their strongest argument, and how it was handled.

## My choice and why
The user's own reasoning, only when the user stated it. Be honest about intuition versus analysis.

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

If the user asks for assistant analysis to be stored, label it **Assistant analysis, not the user's position**.

## 8. Review the outcome

At the review point, assess:

1. **What happened?** Use concrete actuals, not impressions.
2. **Was the prediction accurate?** Compare events with the recorded prediction and confidence.
3. **Was the decision process sound?** Judge the information, assumptions, alternatives, and reasoning available at the time.
4. **What is the reusable lesson?** State a principle for future decisions.

Mark the outcome as correct, incorrect, mixed, too early, or not applicable. If the review is a leading-signal checkpoint, compare those signals with expectations and keep the outcome as too early until real results exist. Do not treat an unfavorable result as proof of a bad process, or a favorable result as proof of a sound one.

## 9. Completion message

When a decision is made, summarize it:

```markdown
Decision: [one-line call]
Scope: [bucket]
Rationale: [two or three honest sentences: the real reason, not a tidy story]
Next action: [owner] will [action] by [date]
Review: [date], or earlier if [trigger]
Record: [location, if one exists]
```

*Fictional example:*

```markdown
Decision: Run the spring workshop series online instead of in person.
Scope: Reversible
Rationale: Venue costs doubled and most past attendees were remote. We can return to in person next season if turnout drops.
Next action: Program lead will announce the format by 15 March
Review: 30 April, or earlier if signups fall below half of last season
Record: Team decision document
```

Use direct language. If the user is about to make a weak call, say so with evidence. Once the readiness gates are met, name the decision and move forward.

## Optional extras

- **Searching a connected register.** If your assistant can query a database or document store, check for overlapping decisions before creating a new one, and use any record template it provides so dates and sections fill consistently.
- **Automatic review reminders.** If a calendar or task tool is connected and authorized, create a reminder titled with the decision on the review date, linking to the record and alerting in advance (for example, one day before). For reversible decisions, a review-date field is usually enough.
- **Chaining with other workflows.** Pair this with an option-generation step before it and a pressure-test step for hard choices. If someone arrives with no options and an open-ended question, route them to option generation first.
- **Tuning the workflow.** After a few uses, note where classification, rigor, mode selection, review timing, or the record format misfired, and adjust your own version of these rules with the user's agreement. Correct any stored facts about the setup, such as who can see the record, as soon as the user updates them.

---
name: capture-meeting-actions
description: Review authorized meeting records, identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require the user’s judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to turn every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose and safeguards

Use this workflow only for a legitimate work purpose and with clear authorization to access the selected meeting records and task system. Read only the minimum sources needed to establish commitments. Keep task notes within the intended access boundary, and omit unrelated personal, health, family, compensation, legal, or other sensitive details unless they are necessary for the task and appropriate for everyone who can access it.

Before each run, apply these operating rules:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same counterparty or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.
- **Track commitments, not discussion.** An idea, interest statement, open question, or request from another person is not a task unless the user accepted responsibility for a concrete outcome.
- **Respect responsibility boundaries.** Attendance does not make the user responsible for all work discussed. Apply known role ownership and delegation rules supplied by the user or organization.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries commonly misattribute actions in recurring one-to-ones, brainstorms, interviews, and meetings where several attendees list their own to-dos. Never create a task solely because a summary labels something as an action item. Verify the owner in the transcript or reliable notes.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied list of meeting records.

If no scope is supplied, use this default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect only the information needed for triage:

- Title, date, and time
- Meeting-record link or identifier
- Attendees and relationship context, if available
- Transcript, notes, summary, and relevant linked context

Report a compact count before processing. Do not infer commitments from a title, attendee list, or agenda alone.

## 2. Fetch and inspect complete records

Fetch complete meeting records in parallel where the selected system supports batching. Do not search for existing tasks yet: first identify candidate commitments, counterparties, and topics so that deduplication is accurate.

For long transcripts, use a repeatable search, extraction, or chunking method rather than relying on a truncated preview. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by clear acceptance

Review automated action-item sections as leads, then inspect the surrounding conversation. A proposed action may have been conditional, assigned to another attendee, completed live, or described as a possibility rather than a promise.

When a transcript cannot be accessed, reduce confidence. Use written notes only when their author and reliability are known. If ownership remains unclear, ask a question rather than creating a task from an uncertain inference.

## 3. Triage each meeting

Classify each meeting loosely. Classification gives a starting expectation, not a rule that overrides direct evidence.

| Meeting type | Usual outcome | Guidance |
|---|---:|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or explicitly timed follow-up. |
| Information-gathering, interview, or reference call | 0 tasks | Create work only for an explicit out-of-meeting commitment by the user. |
| Internal planning or team meeting | 0–1 user-owned task | Capture the user’s deliverable, not the full team action list. |
| Coaching or recurring one-to-one | 0–1 task | Usually create a task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1–2 tasks | Often separate an internal decision from an external response. |

For every meeting, identify:

- Who attended and the relevant relationship context
- Candidate actions owned by the user
- Work completed during the meeting
- Work delegated to another named owner or role
- Explicit future commitments and timing
- Enough neutral context for a task to remain understandable weeks later
- Source and related links that are appropriate to include in the task system

### Skip signals

Produce no task when any of these conditions apply:

- The work was completed during the meeting. For example, a promised document was actually shared, drafted, or sent live.
- Another person or role owns the action, and no follow-up from the user is needed.
- The meeting was informational and any needed synthesis is already captured in the meeting record.
- An active task already covers the same outcome.
- The statement was exploratory, conditional, or did not establish an owner.

A brief retained note may be useful for relationship continuity, but do not place unnecessary sensitive context in a broadly visible task system.

## 4. Decide the task shape

Combine actions into one task when they share the same counterparty, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can be one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect several months later.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line or unrealistic time estimate.

This is a readiness gate. Do not create a task until each proposed task has:

1. A clear owner.
2. Evidence of an unfinished commitment or necessary follow-up.
3. A defined outcome.
4. A sensible scope and time horizon.
5. Enough context to stand alone later.

## 5. Write the task

Use the user’s chosen task system and field names. At minimum, capture:

- **Title:** short, verb-led, and specific.
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user’s scale; default to important routine work and reserve the highest level for a real deadline, material risk, or a waiting counterparty.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and source links.

Examples of useful titles:

- “Follow up with prospective partner about pilot scope”
- “Send setup guide to team member”
- “Reconnect with advisor after agreed milestone”

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: the agreed date, or a reasonable reminder date before it.
- Weekly or sprint commitment: the next relevant review or planning session.
- Flexible work: roughly one week, adjusted to workload and commitment strength.
- Older meetings processed late: move an immediate follow-up to the next workable date rather than assigning an already-passed date, unless the original deadline still applies.

Do not raise priority merely because task capture happened late. Raise it only when the underlying commitment has a meaningful deadline or external consequence.

### Notes template

```markdown
[Two or three sentences of time-independent context. Include relevant absolute
dates, why this matters, the commitment, and any necessary sensitivity.] 

## Actions
- [Concrete action]
- [Concrete action]

## Draft message

Subject: [Specific subject]

Hi [First name],

[Short, direct message that fulfills the commitment.]

Best,
[Sender]

## Links
- Meeting record: <link>
- Related document: <link>
```

Write context so it remains understandable later. Prefer absolute dates over phrases such as “tomorrow” or “recently.” Include only links that recipients of the task can appropriately access.

If the task is to send a message, include a ready-to-send draft rather than merely writing “email them.” Follow the user’s stated communication preferences. If none are known, use concise, warm, professional language with a clear request or promised deliverable. Avoid filler, unnecessary claims of urgency, and overly detailed meeting recap.

For introductions, use double opt-in: ask each relevant person for permission before connecting them. Do not disclose one person’s contact details, interest, or sensitive context to another without appropriate consent.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by meeting link or identifier, counterparty, distinctive topic terms, and proposed title.

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. If a match exists:

- Skip the new task when the existing task already captures the needed work.
- Update the existing task when the meeting adds a meaningful action, deadline, or useful context.
- Ask a batched question when it is unclear whether the new action is separate or should be merged.

Record the duplicate decision so it can be reported clearly.

## 7. Create confident tasks

Create all high-confidence tasks in a batch when the task system supports it. If the environment supports opening created records, open them in the chosen task system rather than filling the status update with management links.

For every skipped meeting, give a brief reason, such as:

- “No out-of-meeting commitment.”
- “Completed during the meeting.”
- “Owned by another role.”
- “Already covered by an active task.”

Do not create low-confidence tasks just to make the sweep appear complete.

## 8. Batch uncertain questions

Skip this step entirely when all decisions are confident. Do not interrupt for each ambiguity. Create confident tasks first, then ask all remaining questions together.

Ask the smallest question that resolves ownership, scope, timing, completion status, delegation, or duplicate handling:

```markdown
**[Meeting title]**
Question: [One specific question]
Context: [One sentence grounded in the record]
Option A: [Task to create or update if true]
Option B: [Skip or alternate task shape]
```

Wait for answers before creating uncertain tasks. After answers arrive, create or update the remaining tasks and rerun the duplicate check if the answer changed the proposed outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, capture lessons that genuinely improve future runs. Keep reusable workflow guidance separate from individual task records.

- Add a short generalized example to a meeting-pattern reference when a recurring pattern affects triage, such as a common attribution error, a reliable sign of live completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a genuinely new required step.
- Record a new delegation boundary in the user’s or organization’s maintained responsibility reference when it applies beyond one meeting.

Do not turn one-off facts about individuals into permanent rules. Small additions to an examples or patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing a step or changing the evidence order.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links to an appropriate source record when available.
- Message drafts are ready to send and respect user preferences and privacy boundaries.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report only the essential outcome: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and any reusable guidance changes. Keep status updates terse and factual.

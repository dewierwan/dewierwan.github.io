---
name: capture-meeting-actions
description: Review authorized meeting records, identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this as a daily sweep, for a selected date range, or for a manually supplied set of meetings.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

Use only records the user is authorized to access and only for a legitimate purpose. Read the minimum sources necessary to establish ownership, outcome, and timing. Do not copy unrelated personal details, sensitive discussion, or confidential information into tasks or status reports. Keep source links and task content within the access boundary of the selected task system.

## Purpose and operating rules

Apply these outcomes before each run:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same counterparty or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text** is strongest evidence of who agreed to do what and when.
2. **Human-written notes** are supporting evidence, especially explicit action sections.
3. **Automated summaries** are useful for orientation but not authoritative for ownership.
4. **Pre-meeting agendas** describe intended discussion, not commitments.

Automated summaries commonly misattribute actions in recurring one-to-ones, brainstorms, and meetings where attendees list their own work. Never create a task solely because a summary labels something an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. Skip work that was completed live, delegated to another owner, already tracked elsewhere, or merely discussed. An idea, stated interest, request, or open question is not a task unless someone explicitly accepted responsibility for a concrete outcome.

Apply responsibility boundaries supplied by the user or organization. Being present in a meeting does not make the user accountable for all work in that area.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` form, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no scope is supplied, use this default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect the title, date and time, record link or identifier, relevant attendees, and available transcript, notes, summary, and linked context.

Report a compact count before processing. Do not infer actions from a meeting title alone.

## 2. Fetch and inspect complete records

Fetch full meeting records in parallel when the meeting system supports batch retrieval. Do not search for existing tasks yet: first identify the people, topics, and candidate outcomes needed for accurate deduplication.

For long transcripts, use a repeatable search, extraction, or chunking method instead of relying on truncated previews. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by explicit acceptance

Review summary action items as candidates, then verify them against the transcript and surrounding conversation. A promise may have been conditional, reassigned, completed during the call, or directed to another attendee.

## 3. Triage each meeting

Classify the meeting loosely. The classification gives a starting expectation; evidence overrides it.

| Meeting type | Usual outcome | Guidance |
|---|---:|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or explicitly timed follow-up. |
| Information-gathering, interview, or reference call | 0 tasks | Create work only for an explicit out-of-meeting commitment by the user. |
| Internal planning or team meeting | 0–1 user-owned task | Capture the user’s deliverable, not the full team action list. |
| Coaching or recurring one-to-one | 0–1 task | Usually create a task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1–2 tasks | Often separate an internal decision from an external response. |

For each meeting, identify:

- Relationship context, including whether this is an initial discussion, recurring meeting, referral, or ongoing workstream where relevant.
- Candidate actions owned by the user.
- Work completed during the meeting.
- Work delegated to a named owner.
- Explicit future commitments and timing.
- Enough neutral context for a task to remain understandable weeks later.
- Source and related links that the task audience may access.

Use these skip signals:

- The user completed the promised work live and the resulting artifact was actually shared, produced, or recorded during the meeting.
- Another named owner accepted the work, or it falls within an established responsibility boundary outside the user’s role.
- The meeting was informational and any required synthesis is already retained in the authorized meeting record.
- An active task already covers the same outcome.
- The statement was not an actual commitment.

For external meetings, create a later reconnect task only when the user explicitly committed to reconnecting and gave a timing cue or agreed trigger. Do not turn a vague “let’s stay in touch” into a scheduled task. If an immediate follow-up and a later reconnect are both explicit, they normally become separate tasks because their horizons differ.

## 4. Decide the task shape

Combine actions into one task when they have the same counterparty, horizon, and outcome. For example, sending promised material, answering related questions, and offering times to meet can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as a reply tomorrow and a reconnect in several months.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

Use this readiness gate before task creation. Every proposed task must have:

- A confirmed owner.
- A genuine unfinished outcome.
- A clear, independently completable shape.
- A plausible due date or review date.
- Enough context and authorized links to stand alone.

If any of these are unclear, hold that item for the batched questions step rather than guessing.

## 5. Write the task

Use the user’s chosen task system and its field names. At minimum, capture:

- **Title:** short, verb-led, and specific, for example, “Follow up with partner about pilot scope.”
- **Status:** the standard open status.
- **Due date:** based on the commitment whenever possible.
- **Priority:** use the user’s scale; default to important time-sensitive work and reserve the highest priority for a real deadline, material risk, or a counterparty waiting for a response that week.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and links.

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: the agreed date or a reasonable reminder date before an agreed trigger.
- Weekly or sprint commitment: the next relevant review, planning, or accountability session.
- Flexible work: approximately five to seven days out, adjusted to workload.
- Older meetings processed late: move an immediate follow-up to the next workable date rather than assigning a past due date, unless the original deadline still applies.

Do not raise priority merely because capture happened late.

### Task-notes format

Use time-independent wording. Prefer absolute dates over terms such as “yesterday” or “next week.” Include only context appropriate for everyone who can access the task.

```markdown
[Two or three sentences of durable context. State the meeting date where useful,
why this matters, the confirmed commitment, and any necessary sensitivity.]

## Actions
- [Concrete action]
- [Concrete action]

## Draft message

Subject: [Specific subject]

Hi [First name],

[Short, direct message that fulfills the commitment and contains a clear
request, answer, or promised deliverable.]

Best,
[Sender]

## Links
- Meeting record: <authorized-link>
- Related document: <authorized-link>
```

If the action is to send a message, write a ready-to-send draft rather than merely saying “send an email.” Follow the user’s approved writing profile if one exists. Otherwise, use concise, warm, professional language; avoid filler, unsupported claims, and unnecessary disclosure. For introductions, use double opt-in: ask each relevant party for permission before connecting them.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search using the meeting link or identifier, counterparty, distinctive topic terms, and proposed title.

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. Skip a new task when the existing task is sufficient. Update the existing task only when the meeting adds a meaningful action, deadline, or authorized context. Record the decision for reporting.

## 7. Create confident tasks

Create all high-confidence tasks in a batch when possible. If the environment supports opening created records, open them in the selected task system rather than filling the status report with management links.

For every skipped meeting, give one brief reason, such as “No out-of-meeting commitment,” “Completed during the call,” “Owned by another role,” or “Already covered by an active task.”

## 8. Batch uncertain questions

Skip this step entirely when all decisions are confident. Do not interrupt for each ambiguity. Create confident tasks first, then ask all remaining questions together.

Ask the smallest question that resolves ownership, scope, timing, completion status, responsibility boundary, or duplicate handling:

```markdown
**[Meeting title]**
Question: [One specific question]
Context: [One sentence grounded in the authorized record]
Option A: [Task to create or update if true]
Option B: [Skip or alternate task shape]
```

Wait for answers before creating uncertain tasks. After answers arrive, create or update the remaining tasks and rerun the duplicate check if the answer changes the proposed outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, capture lessons that genuinely improve future runs, separate from the meeting task itself.

- Add a short pattern note to a reusable meeting-archetype reference when a recurring pattern affects triage, such as an attribution error, a reliable sign of in-meeting completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new responsibility boundary in the user’s or organization’s maintained reference when it applies beyond one meeting.

Do not turn one-off facts into permanent rules. Small additions to a pattern reference can be made directly. Ask for confirmation before structural changes, such as adding or removing a step or changing the evidence order. Briefly report reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a confirmed owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task has an appropriate authorized source link where useful.
- Message drafts are ready to send and follow the user’s preferences.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report only the essential outcome: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and reusable guidance changes. Keep status updates terse and factual.

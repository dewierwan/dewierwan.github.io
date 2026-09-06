---
name: capture-meeting-actions
description: Review authorized meeting records to identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow as a daily sweep, for a selected date range, or for a manually supplied list of meetings. It is tool-independent: use any meeting-record source, transcript capability, and task system that the user is authorized to access.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine unfinished commitment that should be tracked.

## Purpose, access, and operating rules

Use this workflow only for a legitimate work or personal purpose and with clear authorization to access both the meeting records and the task system. Retrieve only the minimum records and passages needed to identify commitments. Keep task notes within the access boundary of the task system: omit unrelated personal information, sensitive details, and private discussion that is not necessary to complete the task. Respect participant consent, applicable policies, and retention expectations.

Before each run, apply these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same counterparty or group on the same time horizon.
- **Multiple tasks** only when counterparties, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful supporting evidence, especially explicit action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often misattribute work, especially in recurring one-to-ones, brainstorming sessions, and meetings where attendees list their own to-dos. Never create a task solely because a summary labels something as an action item. Confirm the owner in the transcript or reliable notes.

Track unfinished outcomes, not conversation. An idea, statement of interest, request, or open question is not a task unless someone accepted responsibility for a concrete outcome. Apply delegation boundaries supplied by the user or maintained in an authorized responsibility reference. Attendance at a meeting does not make the user accountable for all work discussed there.

## 1. Select the meeting scope

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied meeting list. If no input is given, use this default:

- Before a configurable early-morning cutoff in the user’s local time, process the previous day.
- Otherwise, process the current day.

State the selected scope once, for example: “Scanning meetings for 23 Apr.” Find meetings attended by the user and collect only what is relevant:

- Title, date, and time.
- Meeting-record reference or link, if the task audience is permitted to access it.
- Attendees, when needed to establish ownership or perform a follow-up.
- Transcript, notes, summary, and relevant linked context.

Report a compact count before processing. Do not infer actions from a meeting title alone.

## 2. Fetch and inspect complete records

Fetch complete meeting records in parallel when the selected system supports batching. Do not search for existing tasks yet: first identify people, topics, and candidate outcomes so that duplicate checks are accurate.

For long transcripts, use a repeatable search, extraction, or chunking method rather than relying on truncated previews. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by explicit acceptance.

Review summary action items as candidates, then verify them against the transcript and nearby discussion. A stated promise may have been conditional, reassigned, fulfilled live, or directed at another attendee.

## 3. Triage each meeting

Classify the meeting loosely. Classification is a starting expectation, not a rule that overrides evidence.

| Meeting type | Usual outcome | Guidance |
|---|---:|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or explicitly timed follow-up. |
| Information-gathering, interview, or reference call | 0 tasks | Create work only for an explicit out-of-meeting commitment. |
| Internal planning or team meeting | 0–1 user-owned task | Capture the user’s deliverable, not the full team action list. |
| Coaching or recurring one-to-one | 0–1 task | Create a task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1–2 tasks | Often separate an internal decision from an external response. |

For every meeting, identify:

- Relationship context and why the meeting occurred.
- Candidate actions owned by the user.
- Work actually completed during the meeting.
- Work delegated to another named owner.
- Explicit future commitments and timing.
- Enough neutral context for a task to remain understandable weeks later.
- Relevant source references and related materials that the task audience may access.

Create no task when work was completed live, another person owns it, the meeting was purely informational and any needed synthesis is already recorded, the action is covered by an active task, or the statement was not a commitment.

A live completion requires evidence that the deliverable was actually provided or created during the meeting, not merely that someone said they would do it. For example, material shared in the meeting may close a promise to send that same material.

## 4. Decide the task shape

Combine actions into one task when they have the same counterparty, time horizon, and outcome. For example, sending promised material, answering related questions, and offering meeting times can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect months later.
- Different counterparties need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

This is a readiness gate: do not create a task until it has a clear owner, an unfinished outcome, a sensible shape, and enough context to stand alone.

## 5. Write the task

Use the user’s chosen task system and field names. At minimum, capture:

- **Title:** short, verb-led, and specific, such as “Follow up with partner about pilot scope.”
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user’s scale; default to normally important work and reserve the highest level for a real deadline, material risk, or waiting counterparty.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and permitted references.

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: agreed date, or a reasonable reminder date before it.
- Weekly or sprint commitment: next relevant review or planning session.
- Flexible work: roughly one week, adjusted to workload.
- Older meetings processed late: move an immediate follow-up to the next workable date rather than assigning an already-passed date, unless the original deadline still applies.

Do not raise priority merely because capture happened late. Raise it only for a real deadline, material risk, or an external party awaiting a response within a short time frame.

### Notes template

```markdown
[Two or three sentences of time-independent context. Include relevant absolute
dates, why this matters, the commitment, and necessary sensitivity. Omit
unrelated or sensitive personal details.]

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
- Meeting record: <permitted link or reference>
- Related material: <permitted link or reference>
```

Use absolute dates when timing matters, rather than phrases such as “recently” or “next week.” Follow known writing preferences when the user has supplied them. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable.

If the task is to send a message, write a ready-to-send draft rather than merely saying “email them.” For introductions, use double opt-in: seek permission from each relevant person before connecting them, and do not share contact details beyond what they approved.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by permitted meeting reference, counterparty, distinctive topic terms, and proposed title.

Treat an active task as a duplicate when it covers the same outcome, not merely when its wording matches. Skip the new task, or update the existing task if the meeting adds a meaningful action, deadline, or context. Do not expose unrelated task contents during the check. Record the duplicate decision for the final report.

## 7. Create confident tasks

Create high-confidence tasks in a batch when possible. If the environment supports opening created records, open them in the selected task system rather than filling the status update with record links.

For every skipped meeting, give a brief reason, such as “No out-of-meeting commitment,” “Completed during the meeting,” “Owned by another role,” or “Already covered by an active task.”

## 8. Batch uncertain questions

Skip this step entirely when all decisions are confident. Do not interrupt for each ambiguity. Create confident tasks first, then ask all remaining questions together.

```markdown
**[Meeting title]**
Question: [One specific question]
Context: [One sentence grounded in the authorized record]
Option A: [Task to create or update if true]
Option B: [Skip or alternate task shape]
```

Ask the smallest question that resolves ownership, scope, timing, completion status, delegation, or duplicate handling. Wait for answers before creating uncertain tasks. After answers arrive, create or update remaining tasks and rerun the relevant duplicate check if the answer changed the outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, record lessons that genuinely improve future runs. Keep these separate from meeting tasks.

- Add a short, generalized note to a reusable meeting-pattern reference when a recurring pattern affects triage, such as a common attribution error, a reliable sign of live completion, or an archetype exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a new required step.
- Record a new delegation boundary in an authorized responsibility reference when it applies beyond one meeting.

Do not turn one-off facts into permanent rules. Small additions to a pattern reference can be made directly. Ask for confirmation before structural workflow changes, such as adding or removing a step or changing the evidence order. Briefly report reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Source references respect the task audience’s access boundary.
- Message drafts are ready to send and follow the user’s preferences.
- Task notes contain only information necessary to complete the work.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report only the essential outcome: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and reusable guidance changes. Keep status updates terse and factual.

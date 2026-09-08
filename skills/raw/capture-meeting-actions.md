---
name: capture-meeting-actions
description: Review authorized meeting records to identify genuine unfinished commitments, create clear deduplicated tasks for confident follow-ups, and batch only the questions that require user judgment.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use this workflow for a daily sweep, a selected date or date range, or a manually supplied set of meeting records.

The goal is not to convert every discussion into work. Each meeting should result in zero tasks, one combined follow-up, or multiple separate tasks only when there is a genuine, unfinished commitment that should be tracked.

## Purpose, authorization, and operating rules

Use meeting records only for a legitimate purpose and with clear authorization to access the selected meetings, transcripts, notes, and task workspace. Use the minimum relevant sources and details. Do not transfer unrelated personal, confidential, health, compensation, or other sensitive information into tasks. Keep notes within the access boundary of the chosen task workspace and respect participant consent and privacy expectations.

Apply these rules throughout the run:

- **0 tasks** when work was completed during the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be completed together for the same recipient or group, on the same time horizon.
- **Multiple tasks** only when recipients, outcomes, or timing differ materially.

When sources conflict, use this evidence order:

1. **Transcript or recording-derived text:** strongest evidence of who accepted an action and when it is due.
2. **Human-written notes:** supporting evidence, especially explicit notes or action sections.
3. **Automated summary:** useful for orientation, but not authoritative for ownership.
4. **Pre-meeting agenda:** evidence of intended discussion, not a commitment.

Automated summaries commonly assign actions to the wrong attendee, especially in recurring one-to-ones, brainstorming sessions, and meetings where several people list their own to-dos. Never create a task solely because a summary calls something an action item. Confirm ownership in the transcript or reliable notes.

Track unfinished outcomes, not conversation. An idea, interest statement, request, or open question is not a task unless the user explicitly accepted responsibility for a concrete outcome. Apply responsibility boundaries supplied by the user. Attending a meeting does not make the user accountable for all related work.

## 1. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as “yesterday,” a date range, or a supplied list of meetings. If no scope is supplied, use this default:

- Before a user-configurable early-morning cutoff in local time, process the previous day.
- Otherwise, process the current day.

State the scope once, for example: “Scanning meetings for 23 Apr.” Locate meetings attended by the user and collect only what is necessary:

- Title, date, and time
- Meeting-record link or identifier
- Attendees, when available and relevant
- Transcript, notes, summary, and directly relevant linked context

Report a compact meeting count before processing. Do not infer commitments from a meeting title alone.

## 2. Fetch and inspect complete records

Fetch complete records in parallel when the selected record system supports batching. Do not search for existing tasks yet: first identify the people, topics, and candidate outcomes needed for accurate duplicate checks.

For long transcripts, use a repeatable search, extraction, or chunking method rather than trusting truncated previews. Search for commitment language such as:

- “I’ll …”
- “Let me …”
- “I can …”
- “I’ll send …”
- “I’ll follow up …”
- “I’ll introduce …”
- A request followed by explicit acceptance

Treat summary action items as candidates. Verify each candidate against the transcript and nearby conversation. A promise may have been conditional, reassigned, fulfilled during the meeting, or made by someone else.

## 3. Triage each meeting

Classify meetings loosely. Classification provides an expected starting point, not a rule that overrides evidence.

| Meeting type | Usual outcome | Guidance |
|---|---:|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or explicitly timed follow-up. |
| Information-gathering, interview, or reference discussion | 0 tasks | Create work only for an explicit out-of-meeting commitment. |
| Internal planning or team meeting | 0–1 user-owned task | Capture the user’s deliverable, not the whole group action list. |
| Coaching or recurring one-to-one | 0–1 task | Usually create a task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1–2 tasks | Often separate an internal decision from an external response. |

For every meeting, identify:

- Relationship context and why the meeting occurred
- Candidate actions owned by the user
- Work completed during the meeting
- Work delegated to another named owner
- Explicit future commitments and timing
- Enough neutral context for a task to remain understandable weeks later
- Authorized source links and related documents, if appropriate to retain

Create no task when work was completed live, another person owns it, the meeting was purely informational and any necessary synthesis is already recorded, an active task covers the same outcome, or the statement was not a commitment.

## 4. Decide the task shape

Combine actions into one task when they have the same recipient, time horizon, and outcome. For example, sending promised material, answering related questions, and offering times to meet can form one follow-up task.

Split tasks when:

- Timing differs substantially, such as an immediate reply and a reconnect several months later.
- Different recipients require separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would not have a clear finish line.

### Readiness gate

Do not create a task until it has all of the following:

- A clear user-owned outcome
- Evidence that the outcome remains unfinished
- A sensible task shape: combined or split appropriately
- A practical due date or review date
- Enough permitted context to stand alone later
- No unresolved duplicate or ownership concern

## 5. Write the task

Use the user’s chosen task workspace and field names. At minimum, capture:

- **Title:** short, verb-led, and specific, such as “Follow up with partner about pilot scope.”
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user’s scale; default to normal important work and reserve the highest level for a real deadline, material risk, or an awaiting recipient.
- **Time estimate:** realistic minutes.
- **Notes:** context, action checklist, communication drafts, and authorized links.

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: agreed date, or a reasonable reminder date before it.
- Weekly or sprint commitment: the next relevant review or planning session.
- Flexible work: roughly one week, adjusted to workload.
- Older meetings processed late: move an immediate follow-up to the next workable date rather than assigning a date already passed, unless the original deadline still applies.

Do not raise priority merely because capture happened late.

### Notes template

```markdown
[Two or three sentences of time-independent context. Include relevant absolute
dates, why this matters, the commitment, and any necessary sensitivity. Omit
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
- Meeting record: <link>
- Related document: <link>
```

Avoid unnecessary private discussion in any workspace that may be visible to others. Follow the user’s writing preferences. Otherwise, draft concise, warm, professional messages with a clear request or promised deliverable. If the task is to send a message, include a ready-to-send draft rather than merely writing “email them.” For introductions, use double opt-in: seek permission from each relevant person before connecting them.

## 6. Deduplicate before creation

Run one batched search of active tasks before creating new ones. Search by authorized meeting reference, relevant person or group, distinctive topic terms, and the proposed title.

Treat a task as a duplicate when it covers the same outcome, not merely when wording matches. Skip the new task, or update the existing task if the meeting adds a meaningful action, deadline, or permitted context. Record the decision for the final report.

## 7. Create confident tasks

Create high-confidence tasks in a batch when supported. If the chosen workspace can display newly created tasks directly, use that capability rather than placing administrative links in the status update.

For every skipped meeting, give one brief reason, such as:

- “No out-of-meeting commitment.”
- “Completed during the meeting.”
- “Owned by another role.”
- “Already covered by an active task.”

## 8. Batch uncertain questions

Skip this step entirely if all decisions are confident. Do not interrupt once per ambiguity. Create confident tasks first, then ask all remaining questions together.

Ask the smallest question that resolves ownership, scope, timing, completion status, responsibility boundary, or duplicate handling:

```markdown
**[Meeting title]**
Question: [One specific question]
Context: [One sentence grounded in the authorized record]
Option A: [Task to create or update if true]
Option B: [Skip or alternate task shape]
```

Wait for answers before creating uncertain tasks. After answers arrive, create or update the remaining tasks and repeat the duplicate check if the answer changes the outcome.

## 9. Maintain reusable guidance

Before declaring the run complete, capture lessons that genuinely improve future runs. Keep reusable guidance separate from individual meeting tasks.

- Add a short generalized pattern to a meeting-triage reference when a recurring issue affects decisions, such as a common attribution error, a reliable sign of live completion, or a meeting-type exception.
- Update the core workflow only for cross-cutting principles, changed defaults, or a genuinely new required step.
- Record a new responsibility boundary in the user’s maintained reference only if it applies beyond one meeting.

Do not turn one-off facts into permanent rules. Small additions to a patterns reference can be made directly. Ask for confirmation before structural workflow changes, such as changing the evidence order or adding or removing a step. Briefly report any reusable guidance added or changed.

## 10. Audit and report

Before finishing, verify that:

- Every created task has a clear user-owned and unfinished outcome.
- Transcript evidence supports ownership where summaries are unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each retained source link is appropriate and authorized.
- Message drafts are ready to send and follow the user’s preferences.
- Task notes omit unrelated sensitive information.
- Every uncertain item is either asked as a specific question or explicitly deferred.

Report only the essential outcome: meetings reviewed, tasks created or updated with due dates, skipped items with brief reasons, unresolved questions, and reusable guidance changes. Keep status updates terse and factual.

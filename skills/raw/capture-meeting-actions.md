---
name: meeting-actions
description: Reviews meeting records, turns real unfinished commitments into clear tasks, and batches unclear ones as questions. Use when asking what you committed to today or for meeting follow-ups.
---

# Capture meeting actions

Turn authorized meeting records into reliable post-meeting follow-up tasks. Use it as a daily sweep, for a selected date or range, or for a set of meetings you paste in.

## Quick version

- Paste one meeting at a time: the transcript if you have it, plus your own notes and any automated summary. Say which attendee is you.
- Ask: "List only the concrete, unfinished things I agreed to do after this meeting. Quote the transcript line for each. Ignore anything done live, owned by someone else, or just discussed."
- Treat the transcript as stronger evidence than your notes, and your notes as stronger than an automated summary. Summaries often assign other people's to-dos to you.
- Have the assistant shape each meeting into 0 tasks, 1 combined follow-up, or separate tasks only when recipients or timing differ a lot.
- For each task, ask for a verb-led title, a due date with a reason, a time estimate, short notes that will make sense weeks later, and a ready-to-send draft if the action is a message.
- Ask it to save every unclear item for one batched list of questions at the end, each with two options.

## 1. Set the operating rules

The goal is not to turn every discussion into work. Each meeting should produce one of these outcomes:

- **0 tasks** when work was completed in the meeting, belongs to another owner, is already tracked, or the meeting was only for information gathering.
- **1 task** when related actions can be done together for the same recipient or group on the same time horizon.
- **Multiple tasks** only when recipients, outcomes, or timing differ materially.

Use this evidence order when sources conflict:

1. **Transcript or recording-derived text:** strongest evidence of who agreed to do what and when.
2. **Human-written notes:** useful support, especially explicit action sections.
3. **Automated summary:** useful for orientation, not authoritative for ownership. Summaries also drop timing detail, such as turning "after her leave starts next week" into a vague "follow up later."
4. **Pre-meeting agenda:** describes intended discussion, not a commitment.

Automated summaries often assign actions to the wrong attendee, especially in recurring one-to-ones, brainstorms, and meetings where others list their own to-dos. Never create a task only because a summary calls it an action item.

Track unfinished outcomes, not conversation. An idea, a statement of interest, or an open question is not a task unless someone accepted responsibility for a concrete outcome. Apply responsibility boundaries supplied by the user or team: attending a meeting does not make the user responsible for every topic discussed. If an area has been handed to another person, follow-ups in that area usually need no task for the user.

This workflow reads records about other people, so use it only for a legitimate purpose with clear authorization to access those records. Use the minimum relevant sources and details, leave unrelated or sensitive personal information out of tasks and reusable guidance, and keep outputs within the access boundary of the chosen task system and its audience.

## 2. Select the meetings

Accept a date in `YYYY-MM-DD` format, a relative date such as "yesterday," a date range, or a supplied meeting list. If no input is given, use this adjustable default:

- Before an early-morning cutoff in the user's local time, process the previous day.
- Otherwise, process the current day.

State the scope once, for example: "Scanning meetings for 23 Apr."

Check every place where the user's meeting records live, not just the main one. Many people keep a shared team meeting space plus a separate private space for sensitive calls, reference calls, or internal one-to-ones. Sources can differ in how they filter: one may already show only meetings the user attended, while another needs a direct query by date. Query each source for the selected scope, merge the results, and remove any meeting that appears in both.

For each meeting, collect:

- Title, date, and time.
- Record link or identifier.
- Attendees, only as needed to identify ownership.
- Transcript, notes, summary, and relevant linked context.

Report a compact count before processing, such as "7 meetings on 23 Apr." Do not infer actions from a title alone.

## 3. Fetch and inspect complete records

Fetch full records in parallel where the system supports batching. Do not search for existing tasks yet: first identify the people, topics, and candidate outcomes that make deduplication accurate.

For long transcripts, use a repeatable search, extraction, or chunking method rather than a truncated preview. Search for commitment language such as:

- "I'll ...", "Let me ...", "I can ..."
- "I'll send ...", "I'll follow up ...", "I'll introduce ..."
- A request followed by explicit acceptance.

Treat summary action items as candidates and verify each against the surrounding conversation. A promise may have been conditional, reassigned, fulfilled live, or made by another attendee.

If no transcript exists, lower confidence. Use notes or related messages only when they clearly identify the owner and outcome. Ask rather than guess when a wrong guess could create unwanted work or outreach.

## 4. Triage each meeting

Classify the meeting loosely. The type sets an expectation; evidence overrides it.

| Meeting type | Usual outcome | Guidance |
|---|---|---|
| External relationship meeting | 1 task, sometimes a later reconnect | Capture promised material, outreach, introductions, or an explicitly timed follow-up. Add a reconnect only for an explicit commitment with a stated timeline. |
| Information-gathering, interview, or reference call | 0 tasks | Create work only for an explicit out-of-meeting commitment. Synthesis is often already in the notes. |
| Internal planning or team meeting | 0 to 1 user-owned task | Capture the user's own deliverable, not the team's full action list. |
| Coaching or recurring one-to-one | 0 to 1 task | Usually handled live; task only for explicit work outside the session. |
| Partnership, commercial, or decision meeting | 1 to 2 tasks | Often separate an internal decision from an external response. |

For every meeting, identify:

- Relationship context: why the meeting happened, how many times you have met, who made the introduction.
- Candidate actions owned by the user.
- Work completed during the meeting.
- Work delegated to another named owner.
- Explicit future commitments and their timing.
- Enough neutral context for a task to stand alone weeks later.
- Source and related links the task audience may access.

Create no task when work was completed live, another person owns it, the meeting was purely informational and its synthesis is recorded, an active task covers it, or the statement was not a commitment. Users often pre-create tasks during a meeting, so expect some coverage already.

A test for live completion: if someone promised to send, create, paste, or share something and the artifact was actually delivered during the meeting, it is done. The initial promise in the transcript is not enough to create a task.

## 5. Decide the task shape

Combine actions into one task when they share recipient, time horizon, and outcome. Sending promised material, answering related questions, and offering meeting times can form one follow-up.

Split tasks when:

- Timing differs a lot, such as an immediate reply and a reconnect months later.
- Different recipients need separate communication.
- An internal decision and an external response are distinct outcomes.
- A combined task would have an unclear finish line.

**Readiness gate.** Do not create a task until it has:

- A clear owner.
- An unfinished, concrete outcome.
- Transcript or reliable-note evidence of ownership.
- A sensible scope and finish line.
- A due-date rationale.
- Enough context to stand alone.

## 6. Write the task

Use the user's chosen task system and field names. At minimum, capture:

- **Title:** short, verb-led, specific. A parenthetical hook helps later recall, such as "Follow up with partner lead (pilot scope)."
- **Status:** the standard open status.
- **Due date:** based on an explicit commitment whenever possible.
- **Priority:** use the user's scale. Default to important and time-sensitive; reserve the top level for a waiting recipient with a near deadline or a material risk.
- **Time estimate:** realistic minutes. As an adjustable guide: a few minutes for trivial sends, under an hour for a typical follow-up, longer for a decision plus several messages.
- **Notes:** context, action checklist, drafts, links.

### Due-date rules

- Immediate promised follow-up: next working day unless another date was agreed.
- Scheduled reconnect: the agreed date, or a reminder shortly before it.
- Weekly or sprint commitment: the next relevant review or planning session.
- Flexible work: roughly a week out, adjusted to workload.
- Older meetings processed late: move an immediate follow-up to the next workable date instead of a date already passed, unless the original deadline still applies.

Do not raise priority just because capture happened late. Raise it only for an external deadline, material risk, or an expected reply.

### Notes template

```markdown
[Two or three sentences of time-independent context. Include absolute dates,
why this matters, the commitment, and only necessary sensitivity.]

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

Use time-independent wording: "In the 12 May meeting," not "earlier today."

If the task is to send a message, write a ready-to-send draft rather than "email them." Follow the user's known writing preferences: greeting style by context (casual vs. formal or administrative), length, sign-off, phrases to avoid, and whether to include a scheduling link. Without preferences, draft a short, warm, professional message with a clear request or deliverable and no filler. For introductions, use double opt-in: ask each relevant party before connecting them.

### Worked example (fictional)

The user, from Northwind Collective, had a second call with Priya Nandakumar of Larkspur Labs about a pilot. The transcript shows the user saying, "I'll send the pilot outline and a couple of times to talk." The summary also lists "User to draft the budget," but the transcript shows Priya volunteering for that, so it is excluded.

```
Title:      Follow up with Priya Nandakumar (Larkspur pilot outline)
Due date:   14 Mar (next working day)
Status:     Open
Priority:   Important / Time-sensitive
Estimate:   20 minutes

Second call with Priya (Larkspur Labs) on 13 Mar about a three-month pilot.
The user promised the pilot outline and meeting times. Priya owns the budget
draft. No external deadline this week.

## Actions
- Send the message below with the outline attached

## Draft message
Subject: Pilot outline

Hi Priya,

Thanks for the time on our call. Attached is the pilot outline we discussed.
Would Tuesday or Thursday afternoon work for a short follow-up?

Best,
[Sender]

## Links
- Meeting record: <link>
- Pilot outline: <link>
```

Why this shape: one task because there is one recipient and one horizon; next-day due date; default priority since no deadline is pending; short estimate for one message; absolute dates; the misattributed item is left out.

## 7. Deduplicate before creation

Run one batched search of active tasks before creating anything. Search by meeting link or identifier, recipient name, distinctive topic terms, and proposed title.

A duplicate covers the same outcome, not just similar wording. Skip the new task, or update the existing one if the meeting adds a meaningful action, deadline, or context. Record each duplicate decision for the report.

## 8. Create confident tasks

Create high-confidence tasks in a batch when possible. Print one line per task with its due date. If the system can open created records directly, open them there rather than filling the update with links.

For every skipped meeting, give a one-sentence reason:

- "No out-of-meeting commitment."
- "Completed during the call."
- "Owned by another role."
- "Already covered by an active task."

## 9. Batch uncertain questions

Skip this step when every decision is confident. Do not interrupt per ambiguity. Create confident tasks first, then ask all remaining questions together.

Typical uncertainties: unclear ownership in the transcript, overlap with an area handed to someone else, dependence on something only the user knows ("did you already send this?"), an unusual commitment in an information-gathering call, or a person with several active tasks where it is unclear whether to append or create.

```markdown
**[Meeting title]**
Question: [One specific question]
Context: [One sentence grounded in the record]
Option A: [Task to create or update if true]
Option B: [Skip or alternate task shape]
```

Wait for answers. Then create or update the remaining tasks, rerunning the duplicate check if an answer changed the outcome.

## 10. Audit and report

Before finishing, verify that:

- Every meeting source for the scope was checked and merged without duplicates.
- Every created task has a genuine owner and unfinished outcome.
- Transcript evidence supports ownership where summaries were unclear.
- Completed and delegated work was excluded.
- Active duplicates were not recreated.
- Titles are action-oriented and notes stand alone.
- Dates, priority, and estimates are plausible.
- Each task links to its source record where appropriate.
- Drafts are ready to send and match the user's preferences.
- Every uncertain item was asked or explicitly deferred.

Report tersely: meetings reviewed, tasks created or updated with due dates, skipped items with reasons, open questions, and any guidance changes. Use a consistent short date format and no decoration.

## Optional extras

**Long-transcript helper.** If transcripts often exceed what the assistant can read at once, keep a small program that slices a saved record by section (such as the action items), scans for commitment phrases attributed to the user, searches by pattern, or returns the next window of text. Scanning for commitments directly beats trusting the summary's action list.

**Pattern guide.** Keep a user-maintained guide of recurring patterns organized by meeting type: common misattributions, reliable signs of live completion, type exceptions. After each run:

- Append a short, generalized note when a pattern will affect future triage. Do not rewrite old entries.
- Change the workflow itself only for cross-cutting principles, new defaults, or a new step, and ask before structural changes such as adding a step or changing the evidence order.
- Record a new responsibility boundary in the user's responsibility reference if it applies beyond one meeting.

Do not turn one-off facts about a person or meeting into permanent rules. Report any changes in one or two bullets.

**Scheduling.** Run the sweep once a day at a time the user chooses. The work typically scales with meeting count, so a heavy day takes longer.

---
name: process-an-inbox-to-zero
description: Triage authorized email and chat inboxes into five buckets (do now, quick win, delegate, task, delete) so no commitment lives only in an inbox.
---

# Process an inbox to zero

Process one or more authorized inboxes into a trusted task system. Every reviewed item ends in exactly one bucket: **do now**, **quick win**, **delegate**, **task**, or **delete**. When a run is finished, nothing that needs doing should exist only in an email account, team chat, or messaging app. It is either done, assigned to someone, recorded in the task system, or intentionally removed.

The method follows Getting Things Done and Inbox Zero. Processing an inbox means deciding what each item is and where it belongs. It does not mean doing all the work the items describe. The task system is the single trusted list. Choosing what to work on from that list belongs to a separate daily-planning process, not to this workflow.

Urgency comes from what happens if an item waits, not from how it looks. Being new, unread, long, loud, or posted in a group conversation does not raise priority by itself.

Use this workflow when the user asks to triage, clear, process, prioritize, or "get through" an email inbox, a team chat, or personal messaging apps.

## Operating rules

1. **The user takes every external action.** Do not send, react, archive, delete, label, mark read, or mark complete. Do not run bulk actions, even when a tool allows them. The user may explicitly authorize a specific action; treat that authorization as covering only that action.
2. **No drafts unless asked.** Draft only when the user asks for a specific one, and follow the drafting rules below.
3. **One write, per item.** When the user says "task it" (or similar) about a clearly identified item, create that one task. Never create tasks in bulk or without a per-item instruction.
4. **Work cap.** Ask the user for a cap or default to 15 minutes. Anything that would take longer is a task, not do-now work. On inbox days, the main time sink is usually doing the work a message describes, not replying to it.
5. **Respect access boundaries.** Read private communications, calendars, and records only for the user's legitimate purpose and with clear authorization. Use the minimum sources and details needed to decide where an item goes. Leave unrelated or sensitive personal details out of the output. Keep results within the user's own access boundary.
6. **Keep evidence separate from decisions.** Report what a message shows and why a recommendation follows. Never state the user's beliefs, commitments, or decisions for them.

## Step 1: Set scope and time

Get the current date, weekday, and time from a reliable clock set to the user's time zone. Never work these out mentally; deadlines and response windows depend on them.

Map the user's words to sources:

| User says | Source to review |
|---|---|
| "email", "work email" | The authorized work email account |
| "personal email" | The authorized personal account, read-only |
| "team chat" | The internal workspace: saved-for-later items, direct messages, mentions, unreads |
| "community chat" | Only the specific community workspace the user names |
| "messages", "chats", or a named messaging service | Authorized messaging services, filtered to the named service if one was given |
| "all", "everything", "my inboxes" | All authorized email and messaging sources the user normally includes |

If scope is unclear, default to all authorized sources and say so in one line. Do not ask a separate question about scope.

The task system is a destination, not an inbox. If the user actually wants to prioritize existing tasks, switch to a planning workflow.

A request that names a sensitive source (such as personal email) counts as the explicit request to read it. Keep access to such sources read-only. Before reading each source, review any access rules or policies the user has set for it.

## Step 2: Read goals and open tasks

If the user keeps goals and tasks in a system you can read, retrieve in parallel only what triage needs:

1. **Longer-term goals:** the active quarter or season plan and its open goals, with deadlines and priority.
2. **Weekly goals:** the plan covering today. If several weekly records match, use the one that has a filled-in plan.
3. **Today:** the day's intention, plan, and most important task (MIT). Request only those fields. Never pull journal entries or other private reflections.
4. **Open tasks:** title, status, and due date for anything to-do or in progress. You need these to spot inbox items that are already tasked.

Use the system's proper date functions for date filters. Plain text comparisons on dates often return nothing without an error. If results are unexpectedly empty, check the filter before concluding the data is missing.

If a level is missing or empty, say so in one line and continue with what exists. Do not invent goals. If a higher level is empty but weekly goals say what they support, use that as the higher-level goal.

Summarize the goals for yourself in three to six lines. You will judge every item against them.

### Check the most important thing

If today's MIT is not inbox work and the user is inside or close to its planned time, ask once, before reading any inbox:

> Is this the most important thing right now, or does it just feel productive?

Trust the answer. Skip this if there is no MIT or inbox work is part of the plan.

## Step 3: Read the inboxes

Read every source in scope in parallel. For each item, collect: source, sender or participants, subject or conversation, date of the last message, who sent the last message, a one-line gist, and a stable link where the system supports one.

**Email.** List inbox messages and group them by thread, keeping the latest message per thread. If the listing hits its page limit, run a second query for older messages so old threads are not missed. Newsletters, receipts, calendar notifications, and automated updates go straight to Delete without further reading, unless the preview suggests a deadline, security issue, or money at stake. Open a full message only when the preview leaves the ask or deadline unclear. Build links only when you have verified the link format for that account; otherwise cite by sender, subject, and date.

**Team chat.** Prefer a purpose-built inbox or audit view over search, because search often misses saved, unread, or completion state. Saved-for-later items are actions the user already chose to keep. Unreads are attention debt, not automatic priorities. Review direct messages and mentions first.

**Messaging apps.** Check that each service is connected. Use a lookback window the user chooses, or 14 days by default. Find reply debt by checking who sent the last message and whether a reply is expected; a search that does not show the last sender cannot find reply debt alone. Read recent messages when the last one does not make the ask clear. Direct chats rank above group chats unless a group message names the user or asks them something. Cite chats as "<service>: <person>" if no real link exists.

**Failures.** If a source fails or a service is disconnected, name the source, the exact error, and what data is missing. Try only safe repairs (such as reconnecting or reauthorizing). Continue with the other sources. Never quietly drop a source or substitute another one. Put the gap at the top of the output so the user sees it first.

## Step 4: Sort into buckets

Put every item in exactly one bucket:

1. **Do now:** important and urgent, and finishable within the work cap. Aim for three to five. If there are more, the extras are probably tasks.
2. **Quick wins:** under about two minutes each: a short reply, a yes/no, an RSVP, a forward. The user batches these.
3. **Delegate:** someone else should own it. Name the suggested owner and give the evidence in a few words, such as "runs operations" or "is leading this project". Find owners from the thread itself, recent discussion in the relevant channel, and documented roles. Check stored notes about roles against current evidence, since roles change. If no credible owner appears, write "owner unclear" rather than guessing.
4. **Task:** real work longer than the cap, or work that cannot happen yet. Give a suggested task name, a due date if the item implies one, and why. If an open task already covers it, say so and suggest clearing the inbox copy.
5. **Delete:** no action needed: FYIs, newsletters, resolved threads, automated notices, conversations that ended naturally. Show counts by type and name only items the user might be surprised to see here.

Rank do-now items, and order every other bucket, using these criteria in order:

1. **Hard deadline or time-bound decision:** due today or tomorrow, an offer or event that expires, or a meeting that needs a reply first.
2. **Someone is blocked on the user:** a teammate, candidate, or partner cannot move until they answer. If the organization has a response-time target (for example, for job candidates), treat it as a deadline.
3. **Ladders to a goal:** today's MIT first, then weekly goals, then longer-term goals. Name the goal.
4. **Relationship cost of delay:** key collaborators, funders, and personal relationships that cool if left. Email older than about two days and chats older than about three days are stronger staleness signals than the age of a saved-for-later item.

## Step 5: Snapshot and questions

Show the sorted result, then ask two to four questions in one plain-text numbered block, with lettered options where possible so the user can reply `1b, 2a`. End the turn and wait.

```markdown
## Inbox zero: <date>, <sources>

**Goals used:** <longer-term> · <week> · <today's MIT>
**Missing data:** <failed or stale sources, or "none">
**Counts:** <N items: X do now, Y quick wins, Z delegate, T task, D delete>

### Do now
1. <item> — <source, sender, age> — <why> — <link>

### Quick wins
- <item> — <the one action> — <link>

### Delegate
- <item> — <suggested owner and evidence, or "owner unclear"> — <link>

### Task
- <item> — <suggested task name, due date> — <link>

### Delete
- <counts by type, plus any surprising item>
```

Use a real list for every group. Never show severity with color alone; use labels and order so the snapshot works for everyone.

Good questions resolve real uncertainty about where an item belongs: whether a goal is still live, whether the user wants to handle a sensitive relationship or hiring thread personally, whether an unfamiliar sender matters, or how much time is available. Do not ask what the data already answers. If nothing is uncertain, ask one question about time available.

The user will move items between buckets in their answer. Their bucket choice is final.

## Step 6: Work the buckets

Go in this order and stop whenever the user wants to stop.

1. **Do now, one at a time.** Read the full thread or chat and check the calendar around any dates it mentions; the user may want to place a hold before replying. Gather only the context this decision needs, such as earlier exchanges with the person or the relevant project document. For hiring or candidate items, use only authorized, role-relevant evidence and focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether the assessment so far distinguishes relevant performance. Then write a short paragraph: who this is, what they want, what is at stake if the user waits, and the action you recommend, with evidence linked. Ask one to three questions only the user can answer. When the user says it is handled, move to the next.
2. **Quick wins.** List them together so the user can clear them in one sprint.
3. **Delegate and task.** The user confirms owners and tasks. Create a task only for each item they say to task.
4. **Delete.** Remind the user what to archive or delete; they do it.

### Drafts, only when asked

Give one copy-ready plain-text draft per response, as the final block, so it is easy to copy. Match the channel, the user's voice, and any writing guidelines they keep. Keep claims factual and make no commitments the user has not approved. Do not save drafts into the email or chat system; the user pastes from the conversation.

### Creating a task

When told to task a specific item, create one record in the chosen task system with: a clear action title, status set to to-do, the implied due date, importance, urgency, a time estimate, and the relevant area or project. Write the notes as:

```markdown
**What:** one line: the ask and who is waiting.
**Source:** <link, or "<service>: <person>, <date>" for chats>
**Context:** two to four bullets with key facts and links.
**Next step:** the first concrete action.
```

Do not pre-write replies in the task unless asked. After creating it, tell the user the item can now leave its inbox and give the task link if the system provides one.

## Step 7: Close and improve

End with a short status per source: how many items are cleared, tasked, delegated, still open, or unreviewed because of access or time. If many loops remain open, say so plainly.

Then review the run for friction: a question the user found pointless, an item in the wrong bucket, a source that misbehaved, or context you had to hunt for. If the user keeps written instructions for this workflow and has authorized updates, record a general fix rather than one tied to a single message. Never store message content, credentials, or personal details in those notes.

## Single-item mode

Use this when the user, or a reminder they set up, points to one specific item (for example, their oldest email or oldest saved chat item).

1. Skip goal reading, sorting, the snapshot, and closing. Do not read any other inbox item. Review the access rules for that item's source.
2. Read the item with the normal method for its source, plus only the context needed.
3. Treat it as a single do-now item: who this is, what they want, what happens if it waits. Recommend one bucket and the concrete next action, with the item's link. Ask only the questions Step 6 allows.
4. Help the user finish it under the normal rules for drafts and tasks.
5. Tell the user which inbox action will clear it, such as archiving the email or marking the saved item complete. Do not require a special confirmation phrase; if a reminder tool is involved, let it check the inbox state itself.

## Common failure modes

- **Doing instead of processing:** starting a 45-minute job inside triage. Make it a task.
- **Treating noise as urgency:** ranking by unread count, recency, or group activity instead of consequence.
- **Silent gaps:** a disconnected source left out of the report.
- **Duplicate tasks:** tasking something already on the list.
- **Guessed owners:** delegating without current evidence.
- **Overreach:** sending, archiving, bulk-tasking, or reading private material the decision did not need.

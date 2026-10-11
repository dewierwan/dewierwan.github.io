---
name: process-an-inbox-to-zero
description: Turn authorized email and chat inboxes into clear next actions by sorting every item into one bucket: do now, quick win, delegate, task, or delete.
---

# Process an inbox to zero

Process one or more authorized inboxes into a trusted task system. Each reviewed item ends in exactly one bucket: **do now**, **quick win**, **delegate**, **task**, or **delete**. When a run is finished, no commitment that needs action should exist only in an inbox. It has been done, handed to someone else, recorded as a task, or removed on purpose.

This workflow follows Getting Things Done and Inbox Zero principles. Processing an inbox means deciding what each item is and where it goes. It does not mean doing all the work the messages describe. The task system is the one trusted list. Choosing what to work on from that list belongs to a separate planning process.

An item is urgent because of what happens if it waits. Being new, unread, long, loud, or in a group conversation does not raise its priority on its own.

## Setup choices

Confirm these once, or use the defaults. Record the user's choices so later runs do not ask again.

| Choice | What it controls | Suggested default |
|---|---|---|
| Sources | Which inboxes count as "all" | Every inbox the user has authorized |
| Task system | Where task items are recorded, and which fields it uses | The user's chosen task list, with title, status, and due date at minimum |
| Planning sources | Where goals and today's plan live, if anywhere | None; rank on deadlines and blockers only |
| Work cap | The longest item that can still be do-now work | 15 minutes |
| Quick-win limit | The longest item that counts as a quick win | About 2 minutes |
| Chat lookback | How far back to look for unanswered chats | 2 weeks |
| Staleness signals | When an unanswered item starts to cost the relationship | A few days, shorter for direct personal messages |
| Response standards | Promised reply times for specific processes | None unless the user names them |
| Inbox actions | Who sends, archives, or marks items | The user does it; the assistant only recommends |
| Focus check | Whether to ask if inbox work is the right use of time now | On, when a planned top task exists |

## Operating rules

1. **The user takes every inbox action by default.** Do not send, react, archive, delete, label, mark read, or mark complete unless the user explicitly authorizes that specific action. Never run bulk actions, even if a tool allows them.
2. **No drafts unless asked.** Write a draft only when the user asks for a specific one.
3. **Create tasks one at a time.** When the user says "task it" (or similar) about one clearly identified item, create that one task. Never create tasks in bulk or without a per-item instruction.
4. **Respect the work cap.** Anything longer than the cap is a task, not do-now work. On inbox days the real time sink is doing the work a message describes, not replying to it.
5. **Respect access boundaries.** Read private communications, calendars, records, and documents only for a legitimate purpose and with clear authorization. Use the fewest sources and the least information each decision needs. Leave unrelated or sensitive personal details out of all output. Keep results within the user's own view unless they choose to share them. Personal accounts stay read-only.
6. **Keep evidence separate from decisions.** Say what the message shows and why a recommendation follows. Never state the user's beliefs, commitments, or relationship judgments for them.
7. **Verify, don't assume.** Get the current date and time from a reliable clock. Check that each retrieval is complete before trusting it. Give only links you know work.

## Step 1: Set scope and time

1. Get the current date, weekday, and time in the user's time zone. Deadlines and response windows depend on it, so never estimate it.
2. Map the user's words to sources:

| User says | Source to review |
|---|---|
| "email" | The user's main authorized email account |
| "personal email" or another named account | That account only, read-only |
| "team chat" | The team workspace: saved-for-later items, unread direct messages, and mentions |
| "chats" or a named messaging service | Authorized messaging services, filtered to the named one |
| "all" or "my inboxes" | Every source in the user's "all" list |

If scope is unclear, default to all and say so in one line instead of asking. Naming an account, or asking for "all", counts as the request to read it. Before reading each source, review any access rules the user has set for it.

The task system is not an inbox here; it is where items go. If the user wants to prioritize existing tasks rather than messages, switch to a planning workflow.

## Step 2: Read goals and open tasks

If the user has planning sources, read only what triage needs, in parallel:

1. **Longer-term goals** that are currently active.
2. **This week's goals.**
3. **Today's plan:** intention, plan, and most important task (MIT). Request only those fields; never pull private fields such as journals or reflections.
4. **Open tasks:** title, status, and due date, so you can spot items already tasked.

If a level is missing or empty, say so in one line and carry on with what exists. Do not invent goals. If a lower level states what it supports, use that as the higher-level goal. Summarize the goals in three to six lines for your own use when judging items.

**Focus check.** If today's MIT is not inbox work and the user is in or near its planned time, ask once before reading any inbox:

> Is this the most important thing right now, or does it just feel productive?

Trust the answer. Skip this if there is no MIT or inbox work is part of today's plan.

## Step 3: Read the inboxes

Read every source in scope in parallel. For each item collect: source, sender, subject or conversation, date of the last message, who sent the last message, a one-line gist, and a working link if one exists. If not, cite by source, sender, and date.

Apply these principles to any source:

- **Group to the unit of decision.** For email, group messages into threads and keep the latest message per thread.
- **Make sure nothing was cut off.** If a listing hits a result limit or a filter returns surprisingly little, run a follow-up query or check the filter before concluding the inbox is small.
- **Skim before opening.** Routine newsletters, receipts, calendar notices, and automated updates go straight to Delete unless the preview hints at a decision, deadline, security issue, or money. Open a full item only when the preview leaves the ask or deadline unclear.
- **Respect what the user already chose to keep.** Saved-for-later items are actions the user kept on purpose; unreads are attention debt. Direct messages and mentions come before broad channel traffic.
- **Find reply debt by the last sender.** An unanswered chat is one where someone else spoke last and expects a reply, within the chosen lookback. Search that does not show the last sender cannot find this on its own. Read recent messages when the last one does not show the ask. Direct chats rank above group chats unless a group message names the user.
- **Prefer complete views over search.** A purpose-built inbox view usually shows saved, unread, and completion state that search misses.

**Failures.** If a source fails or is not connected, name the source, the exact error, and what data is missing. Try the safe repair the source's rules allow, such as reauthorizing, then continue with the others. Never quietly drop a source or substitute one that cannot give the same information. Put failures at the top of the output.

## Step 4: Sort into buckets

Put every item in exactly one bucket:

1. **Do now:** important, time-sensitive, and finishable within the work cap. Aim for three to five; more usually means some are tasks.
2. **Quick win:** within the quick-win limit: a short reply, a yes/no, an RSVP, a forward. The user batches these.
3. **Delegate:** someone else should own it. Name the suggested owner and brief evidence, such as "operations lead owns vendor contracts". Find owners from the thread, recent team discussion, and documented roles, and check remembered roles against current evidence. If no credible owner appears, say **owner unclear**.
4. **Task:** work longer than the cap, or that cannot happen yet. Give a suggested task name, an implied due date, and why. If an open task already covers it, say so and suggest clearing the inbox copy.
5. **Delete:** no action needed: FYIs, resolved threads, automated notices, chats that ended naturally. Show counts by type and name only items the user might be surprised to see here.

Rank Do now, and order every other bucket, using these criteria in order:

1. **Hard deadline or time-bound decision:** due today or tomorrow, an expiring offer, or a meeting that needs a reply first.
2. **Someone is blocked on the user,** including any response standard the user has set for a process.
3. **Ladders to a goal:** today's MIT, then weekly, then longer-term goals. Name the goal.
4. **Relationship cost of delay,** using the user's staleness signals. Age supports a ranking; it never overrides consequences.

## Step 5: Snapshot and questions

Show the sorted result, then ask two to four questions in one plain-text numbered block, with lettered options so the user can reply `1b, 2a`. End the turn and wait.

```
## Inbox zero: <date>, <sources>

**Goals used:** <longer-term> · <week> · <today's MIT>
**Missing data:** <failed or incomplete sources, or "none">
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

Use a real list for every group. Show severity with labels and order, never color alone.

Example question block:

```
1. Is the partnership goal still live this week? a) yes b) paused
2. The scheduling thread with the external partner: a) handle it yourself b) delegate
3. How much time do you have? a) 15 min b) 30 min c) an hour
```

Ask only about real uncertainty: whether a goal is still live, whether the user wants to handle a sensitive thread personally, whether an unfamiliar sender matters, or how much time is available. Do not ask what the data already answers. If nothing is uncertain, ask about time. The user's bucket choices are final.

## Step 6: Work the buckets

Go in this order and stop whenever the user wants.

1. **Do now, one at a time.** Read the full thread and check the calendar around any dates it mentions. Gather only the context this decision needs. For hiring or assessment items, use only authorized, role-relevant evidence: required capabilities, role alignment, diagnostic evidence, and whether the assessment step distinguishes relevant performance. Then give one short paragraph: who this is, what they want, what is at stake if the user waits, and your recommended action, with evidence linked. Ask one to three questions only the user can answer. When they say it is handled, move on.
2. **Quick wins.** List them together for one clearing sprint.
3. **Delegate and Task.** The user confirms owners and tasks. Create a task only for each item they say to task.
4. **Delete.** Remind the user what to archive or delete; they do it.

**Drafts, only when asked.** Give one copy-ready plain-text draft per response, as the final block. Follow the user's writing guidance and the channel's norms. Keep claims factual and make no commitments the user has not approved. Do not save drafts into the email or chat system unless authorized.

**Creating a task.** Create one record with an action-style title, open status, implied due date, and whatever other fields the user's system uses, such as importance, urgency, time estimate, or project. Notes:

```markdown
**What:** one line: the ask and who is waiting.
**Source:** <link, or "service: person, date">
**Context:**
- Key fact or constraint, with link.
- Relevant deadline or decision.
**Next step:** the first concrete action.
```

Do not pre-draft replies in the task unless asked. Afterward, tell the user the item can leave its inbox and give the task link if one exists.

## Step 7: Close and improve

End with a short status per source: cleared, tasked, delegated, still open, or unreviewed because of access or time. If many loops remain open, say so plainly.

Review the run for friction: a pointless question, a wrong bucket, a misbehaving source, context you had to hunt for, or a privacy risk. With permission, update the user's workflow notes or setup choices to fix the cause. Keep changes general, and never store message content, credentials, or personal details.

## Single-item mode

Use this when the user, or a reminder they set up, points to one specific item.

1. Skip goal reading, full collection, sorting, the snapshot, and the closing review. Do not read other inbox items.
2. Read the item using the principles in Step 3, under its source's access rules.
3. Treat it as one Do now item: who, what they want, and what happens if it waits. Recommend one bucket and the next action, with its link.
4. Help the user finish it under the normal rules for drafts and tasks.
5. Tell the user which inbox action clears it. Do not require a special confirmation phrase.

## Common failure modes

- Doing the work a message describes instead of deciding where it belongs.
- Treating unread or recent as urgent.
- Taking inbox actions or creating tasks without a per-item instruction.
- Trusting a cut-off or empty result, or quietly skipping a failed source.
- Guessing a delegate from outdated role information.
- Duplicating a task that already exists.
- Pulling more personal context than the decision needs.

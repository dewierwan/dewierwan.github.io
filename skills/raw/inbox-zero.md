---
name: inbox-zero
description: Turn authorized email, chat, comment, and messaging inboxes into clear decisions and trusted tasks, one bucket at a time, without confusing triage with doing the work.
---

# Process an inbox to zero

Help the user empty one or more inboxes into a single trusted task system. Every item ends in exactly one bucket: **do now**, **quick win**, **delegate**, **task**, or **no action**. When a run is finished, nothing that needs doing should exist only in an email, chat, comment thread, or messaging app. Each item is done, delegated, recorded as a task, or cleared because it needs nothing.

This follows Getting Things Done and Inbox Zero. Processing an inbox means deciding what each item is and where it goes. It does not mean doing all the work the items describe. The task system is the one trusted list. Choosing what to work on from that list belongs to a separate planning workflow.

A message is urgent because of what happens if it waits. Being new, unread, long, loud, or in a busy group chat does not raise its priority.

## Ground rules

1. **The user takes external actions.** Do not send, archive, delete, label, mark read, react, or mark complete unless the user has explicitly delegated that action for a named source. No bulk actions by default, even when a tool allows them. Record any delegated action as a standing user choice, such as clearing notifications in a tool with no quick manual way to empty its inbox. If the user asks you to archive cleared items, archive only items that are finished or handed off. Keep anything still waiting on an unsent reply, and ask about FYIs the user may still want to read.
2. **No drafts unless asked** for a specific item or group.
3. **One write by default:** when the user says "task it" (or similar) about a specific item, create that one task. Never create tasks in bulk or without a per-item instruction.
4. **Work cap.** Ask the user for a cap, or default to 15 minutes. Anything longer is a task, not do-now work. On inbox days the real time sink is doing the work a message describes, not replying to it.
5. **Privacy and access.** Read private communications, calendars, and records only to process the user's own inbox, and only in sources they have authorized. Use the minimum information each decision needs. Request only named fields from planning records and never read private fields such as journals. Leave unrelated or sensitive personal details about other people out of the output, and keep output inside the user's own session or task system. Treat personal accounts as read-only unless the user says otherwise.
6. **Evidence, not assumptions.** Say what the messages show. Never state the user's beliefs, commitments, or decisions for them.

## Single-item mode

Use this when the user, a reminder, or a scheduled prompt hands over one item, such as the oldest unhandled email or saved item.

1. Skip goals, sorting, the opening message, and closing. Read only that item, its source's access rules, and the context it needs.
2. Treat it as one do-now item: who this is, what they want, and what happens if it waits. Recommend one bucket and the concrete next action, with the item's link. Ask only questions only the user can answer.
3. Help them finish it under the normal drafting and task rules.
4. Tell them which inbox action clears it (archive the email, mark the saved item complete). If a reminder system checks the inbox itself, let it detect the change. Never require a special confirmation phrase.
5. If you clear it on request and the action succeeds, continue straight into any waiting request in the same turn. Never make the user send a filler message to move on.

## Step 1: Set scope and time

1. Get the current date, weekday, and time from a reliable clock in the user's time zone. Never work these out mentally; deadlines and focus blocks depend on them.
2. Map the user's words to sources. Configure this once for the user's real accounts.

| User says | Source |
|---|---|
| email, work email | Authorized work email account |
| personal email | Authorized personal account, read-only |
| team chat | Main team workspace: saved items, direct messages, mentions, unreads |
| comments, mentions | Notification inbox of the user's document or project tool |
| chats, or a named network | Messaging apps, filtered to the named network if given |
| all, everything | Every configured source except opt-in-only ones |

If scope is unclear, default to all and say so in one line rather than asking. Secondary workspaces can be opt-in only: read them only when named. A request that names a personal account, or "all" when one is configured, counts as the explicit request needed to read it.

The task list is not an inbox here; it is where items go. If the user asks to prioritise tasks, route to a planning workflow.

Read each source's access rules before reading the source.

## Step 2: Read goals and open tasks

Read these in parallel from the user's planning system, requesting only the fields you need:

1. **Longer-term goals:** the active quarter or similar period, with open goals, deadlines, and priority.
2. **Weekly goals:** the plan covering today. If several records match, use the one with content. If the longer-term level is empty but weekly goals say what they ladder up to, use that as the higher goal.
3. **Today:** intention, plan, and most important task (MIT).
4. **Open tasks:** title, status, and due date, so you can spot items that are already tasked.

Use the system's documented date functions; plain string comparisons on dates often fail silently, so treat unexpectedly empty results as a possible query error. If a level is missing, say so in one line and continue. Do not invent goals. Summarise the goals in three to six lines for yourself and use them to judge every item.

**MIT check.** If today's MIT is not inbox work and the user is inside or near its planned block, ask once, before reading any inbox: "Is this the most important thing right now, or does it just feel productive?" Trust the answer. Skip this when there is no MIT or inbox work is part of the plan.

## Step 3: Read the inboxes

Read every source in parallel. For each item collect: source, sender, subject or chat, date of the last message, who sent it, a one-line gist, and a link copied from tool output.

Apply these principles across sources:

- **Use the right view.** Prefer a purpose-built inbox, notification, or reply-debt view over general search, which often misses saved, unread, and last-sender state.
- **Get everything.** If a result hits its page limit, query again for older items. For a notification inbox, process every uncleared item, read or unread; the run is done only when the total is zero.
- **Group to the decision unit.** Group email messages by thread and keep the latest. Treat several comments feeding one document as one decision: has the user already used them? If yes, clear them; if not, offer one task for the document.
- **Skim, then open only when needed.** Open the full thread when the preview leaves the ask, deadline, owner, or status unclear.
- **Find reply debt by last sender, then read back.** For chats, check who sent the last meaningful message within a lookback window (default 14 days). Before calling a chat handled, read back to the user's last real reply: a quick logistics exchange or closing message can sit on top of an older unanswered ask.
- **Rank direct above broadcast.** Direct messages and explicit mentions come before group or channel traffic, unless a group message names the user or has a time-bound consequence.
- **Respect deliberate saves; mute chosen noise.** Saved-for-later items count, even from low-value channels. Unreads are attention debt, not priority. The user can name feeds to skip, such as status channels; leave their unreads out of every bucket and count unless a message tags the user.
- **Default automated items to no action.** Newsletters, receipts, calendar notices, reactions, automated mentions, stale pointers to deleted content, and resolved discussions go to no action, unless they point to a deadline, money or security issue, or a record that now needs the user. Permission requests are quick wins. Items over two weeks old with no open ask are usually stale; group them for one decision.
- **Never invent links.** Prefer links that open the exact item in the app the user uses. Copy them from tool output, or use a format verified in this setup. Otherwise cite sender, subject, and date and say the link is missing.

**Failures.** If a source fails or is disconnected, name the source, the exact error, and the missing data. Try the safe repairs in its access rules, then continue. Never drop a source quietly or substitute one that cannot provide the same data. Put failures at the top of the output.

## Step 4: Sort into buckets

Put every item in exactly one bucket:

1. **Do now:** important and urgent, finishable within the cap. Aim for three to five; extras are probably tasks.
2. **Quick wins:** under two minutes each: a short reply, a yes or no, an RSVP, a forward, an access approval. The user batches these.
3. **Delegate:** someone else should own it. Name the suggested owner with brief evidence ("owns operations", "is running this hiring process"). Find owners from the thread, recent discussion, project records, and notes on team roles; check notes against current evidence because roles change. If nothing is credible, say "owner unclear".
4. **Task:** real work over the cap, or work that cannot happen yet. Give a suggested name, any implied due date, and why. If an open task already covers it, say so and suggest clearing the inbox copy.
5. **No action:** FYIs, resolved threads, automated notices, chats that ended naturally. Show counts by type and name only items the user might be surprised to see.

Rank do-now items, and order every other bucket, by these signals in order:

1. **Hard deadline or time-bound decision:** due today or tomorrow, an expiring offer, a meeting that needs a reply first.
2. **Someone blocked on the user:** a teammate, partner, or candidate cannot move. Apply any response-time standard the user sets.
3. **Ladders to a goal:** today's MIT, then weekly, then longer-term. Name the goal.
4. **Relationship cost of delay:** key contacts, funders, personal relationships. Age is a supporting signal that differs by channel: an unanswered email or direct chat a few days old usually matters more than an old saved item.

## Step 5: Open the run

Do not show the full sorted list; seeing every bucket at once overwhelms. The opening message holds only:

```markdown
## Inbox zero: <date>, <sources>

**Missing data:** <failed or stale sources, or "none">
**Counts:** <N items: X do now, Y quick wins, Z delegate, T task, A no action>
```

Then go straight into the first non-empty bucket in the same message. Keep the full sort to yourself.

## Step 6: Work the buckets, one batch at a time

Go in order and stop whenever the user wants. Each message shows one batch, or one do-now item, and asks only about what is on screen. Never ask about a later bucket early. End the turn and wait.

Answering a batch's questions is a decision, not completion. Move on only when the user says the batch is done. Until then, help them finish it, for example by drafting the replies they chose.

**Formatting:**

- Every time you name an item or person, including recaps and question titles, link the name to its source.
- Number questions and letter options so the user can reply `1b, 2a`.
- Use real lists for groups. Never show severity by colour alone; use words and order.

**Batches** (sizes are defaults the user can change):

1. **Do now, one item per message.** Read the full thread and check the calendar around any dates; the user may already have added holds. Gather only the context this decision needs. Before saying the user still owes a reply or introduction, search every channel they might have used; it is often done elsewhere. For hiring or assessment items, use the user's chosen hiring guidance and only authorized evidence about role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Then write a short paragraph: who, what they want, what is at stake if it waits, and the recommended action, with evidence linked. Ask one to three questions only the user can answer.
2. **Quick wins, five per message.** Link, a line of context, one recommended action, options when there is a real choice. Say how many remain.
3. **Delegate, three per message.** Link, suggested owner, evidence. The user confirms or changes the owner.
4. **Task, three per message.** Link, suggested name, due date. Create each one the user says to task.
5. **No action.** Counts by type plus surprising items. The user clears them, unless they delegated clearing to you.

**Delegated clearing.** Clear an item only after the user says it is handled or not worth acting on, or confirms the no action bucket. Never clear an item that is decided but not yet acted on. Clearing a notification or marking a chat processed must never resolve, edit, or delete the underlying comment or record. Retry a transient error once, verify the result, and report it in one line ("Cleared 4, all verified, 29 left"). Name anything unverified as a failure, and know how to undo.

**Catch work done mid-run.** Before each new batch, check recently sent mail and messages, drop anything already answered, and note each in one line.

**Good questions** resolve real uncertainty: whether a goal is still live, whether the user wants to handle a sensitive thread personally, whether an unfamiliar sender matters, how much time they have. Do not ask what the data already answers. The user can move any item to any bucket; their choice is final.

### Drafts, only when asked

- **Check the request against the thread.** If a requested point repeats or contradicts what the other person already said, or misreads the ask, say so in one line and draft the version that makes sense. Follow the user's voice and channel conventions.
- **Saved drafts, where authorized:** save the draft as a reply in its own thread, confirm it attached to the right conversation, and open it so the user can edit and send. Use the channel's real mention format for anyone the draft asks to act. Never overwrite an existing draft; if you cannot read saved drafts back, ask the user to paste their edited text rather than recreating yours. Never send.
- **Everywhere else:** give one draft per response as copy-ready plain text in the final block, with the item's link on the line above. Finish all tool calls first so nothing pushes the draft out of the final block.

### Creating a task

Create one record with: a clear action name, open status, due date, importance, urgency, time estimate, and domain or project. Notes:

```markdown
**What:** one line: the ask and who is waiting.
**Source:** <link, or "<network>: <role or contact>, <date>">
**Context:**
- Key fact or constraint, with link.
- Deadline or related record.
**Next step:** the first concrete action.
```

Do not pre-draft replies in the task unless asked. Afterwards, tell the user the item can leave its inbox and give the record link if available.

## Step 7: Close and improve

End with a short per-source status:

| Source | Cleared | Tasked | Delegated | Still open | Unreviewed |
|---|---|---|---|---|---|
| [source] | [n] | [n] | [n] | [n] | [n and reason] |

If many loops remain open, say so plainly.

Then audit the run for friction: a pointless question, a wrong bucket, a misbehaving source, context you had to hunt for, or a privacy risk. With the user's permission, update the workflow's configuration to fix the cause, keeping changes general rather than tied to one message. Never store message content, credentials, or unnecessary personal details.

## Common failure modes

- Dumping every bucket at once instead of one batch at a time.
- Moving on after the user decided but before they acted.
- Doing the work a message describes instead of tasking it.
- Flagging a reply as owed when it was sent elsewhere, or calling a chat handled when an older ask sits under small talk.
- Duplicating a task that already exists, or guessing an owner instead of saying "owner unclear".
- Quietly dropping a failed source.
- Treating unread, new, or loud as urgent.
- Inventing links, or clearing a notification by changing the record behind it.

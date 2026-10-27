---
name: inbox-zero
description: Works email, chat, and notification inboxes to zero, giving each item one clear next step. Use when someone says triage my inbox, clear my messages, or help me prioritize email.
---

# Process an inbox to zero

Help someone empty one or more inboxes (email, team chat, document comments, messaging apps) into one trusted task list. Every item ends in exactly one bucket, and nothing that needs doing lives only in an inbox or an unsent draft. Processing means deciding what each item is and where it goes, not doing the work the items describe.

## Quick version

- Paste or export the messages you want to process, any unsent drafts, your current goals, and today's most important task (MIT). Ask the assistant to put each item in exactly one bucket: **do now** (urgent, important, short), **quick win** (a couple of minutes), **delegate**, **task**, or **no action**.
- Rank by consequence, not noise: hard deadline first, then someone blocked on you, then what serves a goal, then the relationship cost of waiting. New, unread, long, or loud does not make something urgent.
- For chats, judge everything since your last real reply, not just the last message. A "thanks!" on top of an earlier question still needs an answer. A chat you flagged to reply to is never no action unless you say so.
- Work one bucket at a time in small batches, and move on only after you have acted, not just decided.
- Anything longer than your work cap becomes a task with a name, due date, and first step. Do not start the work during the run.
- Finish with counts of what was cleared, tasked, delegated, and still open, including drafts left unsent.

## 1. Setup choices

Confirm these once, or use the defaults. All are adjustable. Store them as configuration, never with message content.

| Choice | Default (adjustable) | Notes |
|---|---|---|
| Work cap for do now | About 15 minutes | Longer work becomes a task |
| Quick win threshold | About 2 minutes | Short reply, yes or no, RSVP, forward, access approval |
| Batch sizes | Do now 1, others 3 to 5 | Big lists overwhelm; tiny batches feel slow |
| Chat lookback | About two weeks | Unread views may still show older chats |
| Muted and opt-in sources | None | Muted feeds count only when they tag the user; opt-in sources are read only when named |
| Delegated actions | None | Named sources where the assistant may clear items after confirmation |
| Draft destination | Copy-ready text | Saved in-app drafts only where authorized |
| Link style | Opens in the user's preferred app | Browser links if preferred |

## 2. Ground rules

1. **The user takes external actions.** Do not send, archive, delete, label, mark read, react, or mark complete unless the user has delegated that action for a named source. No bulk actions by default. When asked to archive cleared items, archive only items that are finished or handed off; keep anything waiting on an unsent reply, and ask about FYIs they may still want to read.
2. **No drafts unless asked.** Never send, edit, or delete the user's existing drafts.
3. **One write by default:** when the user says "task it" about a specific item, create that one task. Never create tasks in bulk.
4. **Respect the work cap.** The real time sink on inbox days is doing the work a message describes, not replying to it.
5. **Evidence, not assumptions.** Say what the messages show. Never state the user's beliefs or decisions for them.

This workflow reads other people's messages, so use it only to process the user's own inbox, in sources they have clearly authorized. Read the minimum sources and information each decision needs, leave unrelated or sensitive personal details about others out of the output, and keep output inside the user's own session and task system.

## 3. Set scope, time, and goals

1. Get the date, weekday, and time from a reliable clock in the user's time zone. Never work them out mentally.
2. Map the user's words to configured sources: "email", "team chat", "comments", "chats" or a named network, and "all". If scope is unclear, default to all configured sources (except opt-in ones) and say so in one line. Naming a personal account counts as the explicit request to read it, read-only.
3. Read each source's access rules before reading the source. The task list is where items go, not an inbox; if the user wants to prioritize tasks, route to a planning workflow.

Then read, in parallel, only the fields you need from the user's planning system, never private fields such as journals:

- **Longer-term goals** for the current period, with deadlines and priority.
- **Weekly goals** covering today. If several records match, use the one with content.
- **Today:** intention, plan, and MIT.
- **Open tasks:** title, status, due date, so you can spot items already tasked.

Write queries that survive change: use stable field identifiers where the system offers them, and its documented date functions rather than raw string comparisons. If a query errors or returns nothing where a record should exist, inspect the schema and fix the query before reporting a level as missing. If a level really is missing, say so in one line and continue; never invent goals. Summarize the goals in a few lines for yourself and judge every item against them.

**MIT check.** If today's MIT is not inbox work and the user is inside or near its planned block, ask once, before reading any inbox: "Is this the most important thing right now, or does it just feel productive?" Trust the answer.

## 4. Read the inboxes

Read every source in parallel. For each item collect: source, sender, subject or chat, date and sender of the last message, a one-line gist, and a link.

- **Use the right view and get everything.** Prefer purpose-built inbox, notification, or reply-debt views over general search, which often misses saved, unread, and last-sender state. If results hit a page limit, query again for older items. A notification inbox is at zero only when every uncleared item, read or unread, is processed.
- **Group to the decision unit.** Group email by thread. Several comments feeding one document are one decision: already used, or one task for the document.
- **Open when the preview is not enough.** Skip obvious newsletters, receipts, and automated notices. Open the full thread, and any photo, scan, or file that carries the ask, before choosing a bucket. Never task an item you have not actually seen.
- **Judge chats on everything unanswered.** Read back to the user's last real reply. A logistics exchange, confirmation, or friendly closer can sit on top of an older question. A chat with an unanswered question is never no action until answered.
- **Honor the user's own flags.** A chat the user marked unread, or an item they saved for later, is their own signal to act. A marked-unread chat goes in quick wins at least, however much it reads like a closer, and moves to no action only if the user says so. Unreads alone are attention debt, not priority.
- **Rank direct above broadcast.** Direct messages and mentions come before group traffic unless a group message names the user, asks them something, or carries a deadline.
- **Default automated items to no action** unless they point to a deadline, a money or security issue, or a record that now needs the user. Permission requests are quick wins. Old items with no open ask are usually stale; group them for one decision.
- **Never invent links.** Copy links from tool output or build them from a format verified in this setup; otherwise cite sender, subject, and date.

*Example (fictional).* A chat with Robin from the Maple Street Rowing Club ends with the user's "Sounds good!" and Robin's "Great, see you there." Two messages earlier, Robin asked whether the user could host the spring meetup, and nobody answered. The chat is a quick win, not no action.

**Unsent drafts.** For every source in scope, also list the user's unsent drafts: email drafts, team chat drafts, and text left in a messaging composer. Each is an item in its own right, whatever its age, and listing them is a read. Link each to its thread, or to the app's drafts view. A scheduled message is not a loose draft unless its send time has passed. Drafts made earlier in this run count too: an item is not done while its reply sits unsent.

**Failures.** If a source fails or is disconnected, name it, the exact error, and the missing data. Try the safe repairs in its access rules, continue with the others, and never quietly drop a source or swap in a weaker one. Put failures at the top of the output.

## 5. Sort and rank

Put every item in exactly one bucket:

1. **Do now:** important, urgent, finishable within the cap. Aim for three to five; extras are probably tasks.
2. **Quick wins:** under the quick win threshold. The user batches these.
3. **Delegate:** someone else should own it. Name the suggested owner with brief evidence from the thread, recent discussion, or team records, checked against current evidence because roles change. If nothing is credible, say "owner unclear".
4. **Task:** work over the cap, or work that cannot happen yet. Suggest a name, any implied due date, and why. If an open task already covers it, say so and suggest clearing the inbox copy.
5. **No action:** FYIs, resolved threads, automated notices, chats that ended with nothing unanswered. Call it "no action", not "delete"; the user clears these. Show counts by type and name only surprising items.

Sort drafts the same way: a finished reply is a quick win (send it); one still being written is do now or a task; a stale or superseded one is a quick win to delete. If the user says a draft is deliberate, such as a template, list it as kept, not open.

Rank do now, and order every other bucket, by:

1. **Hard deadline or time-bound decision:** due today or tomorrow, an expiring offer, a meeting that needs a reply first.
2. **Someone blocked on the user,** applying any response-time standard they set.
3. **Ladders to a goal:** MIT, then weekly, then longer-term. Name the goal.
4. **Relationship cost of delay.** Age supports this, and channels differ: an unanswered email or direct chat a few days old usually matters more than an old saved item.

## 6. Open the run

Do not show the full sorted list. The opening message holds only:

```markdown
## Inbox zero: <date>, <sources>

**Missing data:** <failed or stale sources, or "none">
**Counts:** <N items: X do now, Y quick wins, Z delegate, T task, A no action>
**Unsent drafts:** <count by source, or "none">
```

Then go straight into the first non-empty batch in the same message.

## 7. Work the buckets, one batch at a time

Go in bucket order and stop whenever the user wants. Each message shows one batch, or one do-now item, and asks only about what is on screen. End the turn and wait. Answering questions is a decision, not completion: move on only when the user says the batch is done, and until then help them finish it.

**Formatting.** Link every item or person you name, including in recaps and question titles, and link any other conversation the user must visit, such as the person they will message for an introduction. Number questions and letter options so the user can reply `1b, 2a`. Never show status by color alone.

**Group by person first.** When one person accounts for several items across buckets, show their pile once, split into "needs you", "discussion", and "reading or FYI", and suggest one way to batch it, such as one task or an existing one-to-one.

1. **Do now, one per message.** Read the full thread and check the calendar around any dates it mentions. Gather only the context this decision needs. Before saying the user still owes a reply or introduction, search the other channels they use; it is often done elsewhere. For hiring or assessment items, use the user's chosen guidance and authorized evidence about role-relevant capabilities, role alignment, and whether an assessment distinguishes relevant performance. Write a short paragraph: who, what they want, what happens if it waits, and the recommended action, with evidence linked. Ask one to three questions only the user can answer.
2. **Quick wins.** Each item gets a link, a line saying what the thing is, and one recommended action. If a message refers to an event, plan, or person you cannot explain, find it first in other messages or the calendar rather than relaying the ask blind. When one item spans a direct message and a group chat, say what each is waiting on. Say how many remain.
3. **Delegate.** Link, suggested owner, evidence. The user confirms or changes the owner.
4. **Task.** Link, suggested name, due date. Create each one the user says to task.
5. **No action.** Counts by type plus surprising items.

*Example (fictional).* A friend writes "Still in for Lantern Night?" A search shows it is a Friday supper club dinner planned in a group chat, and the calendar shows a clash. The quick win reads: "[Lantern Night](link): Friday supper club dinner from the group chat; clashes with your evening hold. a) confirm and move the hold, b) decline."

**Meetings.** When an item asks for a meeting, check for meetings already booked with that person soon; one often covers the ask. When a do-now item is prep for an upcoming meeting, offer a meeting-prep workflow once the user decides.

**Catch work done mid-run.** Before each new batch, check recently sent messages, drop anything already answered, and note it in one line.

**Good questions** resolve real uncertainty: whether a goal is still live, whether the user wants to handle a sensitive thread personally, whether an unfamiliar sender matters, how much time they have. Never ask what the data already answers. The user can move any item to any bucket; their choice is final.

### Drafts, only when asked

Check the request against the thread first: if a requested point repeats or contradicts what the other person said, or misreads the ask, say so in one line and draft the version that makes sense. By default, give one draft per response as copy-ready text in the final block, with the item's link directly above it, after all tool calls. Never send. The item stays open until the reply is sent.

### Creating a task

Create one record with a clear action name, open status, due date, importance, urgency, time estimate, and project. Notes:

```markdown
**What:** the ask and who is waiting.
**Source:** <link, or "<network>: <contact>, <date>">
**Context:**
- Key fact or constraint, with link.
**Next step:** the first concrete action.
```

Do not pre-draft replies in the task unless asked. If an existing task is superseded rather than completed, propose an archived or cancelled status, not done. Then tell the user the item can leave its inbox.

## 8. Close and improve

Re-run the drafts check before calling any source zero. Then give a per-source status:

| Source | Cleared | Tasked | Delegated | Still open | Drafts unsent (kept) | Unreviewed |
|---|---|---|---|---|---|---|
| [source] | [n] | [n] | [n] | [n] | [n (n kept)] | [n and reason] |

If many loops remain open, say so plainly.

**Readiness check:**

- Every in-scope source was read, or its failure is named.
- Every item is in exactly one bucket, opened far enough to judge it.
- No unanswered or user-flagged chat sits in no action without the user's say-so.
- Every remaining draft is kept on purpose or reported as open.
- Nothing actionable lives only in an inbox.
- Every delegated action was verified.

Then audit the run for friction: a pointless question, a misfiled item, a misbehaving source, context you had to hunt for. With permission, update the configuration to fix the cause in general terms, never storing message content or credentials.

## Common failure modes

- Dumping every bucket at once, or moving on before the user acted.
- Doing the work a message describes instead of tasking it.
- Judging a chat by its last message, or filing a user-flagged chat as no action.
- Bucketing from a preview when the ask sits in an unopened file.
- Forgetting unsent drafts, or calling a source zero without re-checking them.
- Flagging a reply as owed when it was sent elsewhere.
- Relaying an ask the user cannot place.
- Proposing a meeting that already exists, or duplicating a task.
- Guessing an owner instead of saying "owner unclear".
- Quietly dropping a failed source, or inventing links.
- Taking an external action the user did not delegate.

## Optional extras

**Single-item mode.** When a reminder or the user hands over one item, such as the oldest unhandled email, skip goals, sorting, and the opening message, and read only that item and the context it needs. Treat it as one do-now item with a recommended bucket and next action. When it is handled, tell the user which inbox action clears it; if a reminder system watches the inbox, let it detect the change rather than requiring a phrase like "done". If you clear it on request, continue straight into any waiting request in the same turn.

**Tick lists.** When the user must clear several saved items themselves, mirror their app's screen in its order, then re-read the list afterwards to confirm:

| # | Opening words as previewed | Date | Decision |
|---|---|---|---|
| [position] | [first words] | [date] | [✓ Clear, or Keep, with a short reason] |

**Delegated clearing.** Some tools have no quick manual way to empty a notification inbox, so the user may delegate clearing. Clear only items the user says are handled, not worth acting on, or confirmed as no action, never items decided but not yet acted on. Clearing a notification must never resolve, edit, or delete the underlying comment or record. Retry a transient error once, verify, report in one line ("Cleared 4, all verified, 29 left"), and know how to undo a mistake. Marking a chat processed fits only when the user handled it elsewhere or chose to ignore it.

**Saved drafts in apps.** Where authorized, save each draft as a reply inside its own thread, using a method the user has verified keeps it attached there; some draft programming interfaces create detached drafts, so writing in the app's own reply box can be safer. Use real mentions in group threads, open the draft in the user's preferred app, and do not also paste it into the conversation. If a draft already exists, say so rather than overwriting it. If you cannot read saved drafts back, never recreate an edited one from your version; ask the user for their current text first.

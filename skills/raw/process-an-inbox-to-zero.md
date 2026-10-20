---
name: inbox-zero
description: Works through email, chat, and notification inboxes to zero, turning each item into one clear next step. Use when someone says triage my inbox, clear my messages, or help me prioritize email.
---

# Process an inbox to zero

Help someone empty one or more inboxes (email, team chat, document comments, messaging apps) into a single trusted task system, so that every item ends in exactly one bucket. Processing means deciding what each item is and where it goes. It does not mean doing all the work the items describe.

## Quick version

- Paste or export the messages you want to process, plus your current goals and today's most important task (MIT). Ask the assistant to put each item in exactly one bucket: **do now** (urgent, important, about 15 minutes or less), **quick win** (about 2 minutes or less), **delegate**, **task**, or **no action**.
- Rank by consequence, not noise: hard deadline first, then someone blocked on you, then what serves a goal, then the relationship cost of waiting. New, unread, long, or loud does not make something urgent.
- For chats, judge everything since your last real reply, not just the last message. A "thanks!" sitting on top of an earlier question still needs an answer.
- Work one bucket at a time in small batches, and move on only after you have actually acted, not just decided.
- Anything longer than the cap becomes a task with a name, due date, and first step. Do not start the work during the run.
- Finish with counts of what was cleared, tasked, delegated, and still open.

## 1. Setup choices

Confirm these once with the user, or use the defaults. All are adjustable. Store the answers as configuration, not as message content.

| Choice | Default | Notes |
|---|---|---|
| Work cap for do-now items | 15 minutes | Anything longer becomes a task |
| Quick win threshold | 2 minutes | Short reply, yes or no, RSVP, forward, access approval |
| Batch sizes | Do now 1, quick wins 5, delegate 3, task 3 | Small batches feel less overwhelming; too small feels slow |
| Chat lookback window | 14 days | Unread views may still show older chats |
| Muted feeds | None | For example automated status channels; still include messages that tag the user |
| Opt-in-only sources | None | Secondary workspaces read only when named |
| Delegated clearing | None | Named sources where the assistant may clear items after the user confirms |
| Response-time standard | None | For example a target reply time for candidates or partners |
| Draft destinations | Copy-ready text | Saved drafts only where the user authorizes it |
| Link preference | Open in the native app | Use browser links only if the user prefers them |
| Person-grouping threshold | 4 items | One person with this many items gets one grouped decision |

## 2. Ground rules

1. **The user takes external actions.** Do not send, archive, delete, label, mark read, react, or mark complete unless the user has explicitly delegated that action for a named source. No bulk actions by default, even when a tool allows them. If the user asks you to archive cleared items, archive only items that are finished or handed off. Keep anything still waiting on a reply the user has not sent, and ask about FYIs they may still want to read.
2. **No drafts unless asked** for a specific item or group.
3. **One write by default:** when the user says "task it" (or similar) about a specific item, create that one task. Never create tasks in bulk or without a per-item instruction.
4. **Respect the work cap.** On inbox days the real time sink is doing the work a message describes, not replying to it.
5. **Evidence, not assumptions.** Say what the messages show. Never state the user's beliefs, commitments, or decisions for them.

This workflow reads other people's messages, so use it only for the legitimate purpose of processing the user's own inbox, in sources they have clearly authorized. Read the minimum sources and information each decision needs. Leave unrelated or sensitive personal details about other people out of the output, and keep output inside the user's own session and task system.

## 3. Set scope and time

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

If scope is unclear, default to all and say so in one line rather than asking a separate question. A request that names a personal account, or "all" when one is configured, counts as the explicit request needed to read it.

The task list is not an inbox here; it is where items go. If the user asks to prioritize tasks, route to a planning workflow.

Read each source's access rules before reading the source.

## 4. Read goals and open tasks

Read these in parallel from the user's planning system, requesting only the fields you need and never private fields such as journals:

1. **Longer-term goals:** the active quarter or similar period, with open goals, deadlines, priority, and short notes.
2. **Weekly goals:** the plan covering today. If several records match, use the one with content. If the longer-term level is empty but weekly goals say what they ladder up to, use that as the higher goal.
3. **Today:** intention, plan, and MIT.
4. **Open tasks:** title, status, and due date, so you can spot items that are already tasked.

Write queries that survive change. Where the system supports it, refer to fields by stable identifiers rather than display names, in both filters and requested fields; names can differ between tables and break when someone renames them. Use the system's documented date functions, because plain equality or range comparisons against date strings often fail silently. If a query errors on an unknown field, or returns nothing where a record should exist (for example today's daily record), inspect the schema and fix the query before reporting that level as missing.

If a level is genuinely missing, say so in one line and continue with what exists. Do not invent goals. Summarize the goals in three to six lines for yourself and use them to judge every item.

**MIT check.** If today's MIT is not inbox work and the user is inside or near its planned block, ask once, before reading any inbox: "Is this the most important thing right now, or does it just feel productive?" Trust the answer. Skip this when there is no MIT or inbox work is part of the plan.

## 5. Read the inboxes

Read every source in parallel. For each item collect: source, sender, subject or chat, date of the last message, who sent the last message, a one-line gist, and a link.

Apply these principles across sources:

- **Use the right view.** Prefer a purpose-built inbox, notification, or reply-debt view over general search, which often misses saved, unread, and last-sender state.
- **Get everything.** If a result hits its page limit, query again for older items. For a notification inbox, process every uncleared item, read or unread; the run is done only when the total is zero. Opening a notification may mark it read without clearing it.
- **Group to the decision unit.** Group email messages by thread and keep the latest. Treat several comments feeding one document as one decision: has the user already used them? If yes, clear them; if not, offer one task for the document rather than one per comment.
- **Skim, then open only when needed.** Send obvious newsletters and automated mail straight to no action. Open the full thread when the preview leaves the ask, deadline, owner, or status unclear. A reply deep in a long thread usually needs the full thread.
- **Open attachments that carry the ask.** When the substance sits in a photo, scan, screenshot, or file, open it before choosing a bucket. Never task an item you have not actually seen: a forwarded letter that looks official may turn out to be marketing or a notice needing nothing.
- **Judge chats on everything unanswered.** Find reply debt by last sender within the lookback window, then read back to the user's last real reply. Judge the chat on that whole unanswered stretch, never on its last message: a logistics exchange, a confirmation, or a friendly closer can sit on top of an older ask. A chat whose unanswered part contains a question is never no action until the user has answered it.
- **Rank direct above broadcast.** Direct messages and explicit mentions come before group or channel traffic, unless a group message names the user, asks them something, or has a time-bound consequence.
- **Respect deliberate saves; mute chosen noise.** Saved-for-later items count, even from muted feeds, because the user chose to keep them. Unreads are attention debt, not priority. Leave muted-feed unreads out of every bucket and count unless a message tags the user.
- **Default automated items to no action.** Newsletters, receipts, calendar notices, reactions, automated mentions, pointers to deleted or emptied content, and resolved discussions go to no action, unless they point to a deadline, a money or security issue, or a record that now needs the user (for example a record newly assigned to them with no next step). Permission requests are quick wins. Items over two weeks old with no open ask are usually stale; group them for one decision.
- **Never invent links.** Prefer links that open the exact item in the app the user uses, when that is their preference. Copy links from tool output, or build them only from a format verified in this setup. Otherwise cite sender, subject, and date and say the link is missing.

*Example (fictional).* A chat with Robin from the Maple Street Rowing Club ends with the user's "Sounds good!" and Robin's "Great, see you there." It looks finished. Reading back further shows that two messages earlier Robin also asked whether the user could host the spring meetup, and nobody answered. The chat goes to quick wins, not no action.

**Failures.** If a source fails or is disconnected, name the source, the exact error, and the missing data. Try the safe repairs in its access rules, such as re-authentication steps, then continue with the other sources. Never drop a source quietly or substitute one that cannot provide the same data. Put failures at the top of the output so the user sees the gap first.

## 6. Sort into buckets

Put every item in exactly one bucket:

1. **Do now:** important and urgent, finishable within the cap. Aim for three to five; extras are probably tasks.
2. **Quick wins:** under the quick win threshold. The user batches these.
3. **Delegate:** someone else should own it. Name the suggested owner by name or role with brief evidence ("owns operations", "is running this hiring process"). Find owners from the thread, recent discussion in the relevant channel, project records, and notes on team roles. Check notes against current evidence, because roles change. If nothing is credible, say "owner unclear" rather than guessing.
4. **Task:** real work over the cap, or work that cannot happen yet. Give a suggested name, any implied due date, and why. If an open task already covers it, say so and suggest clearing the inbox copy.
5. **No action:** FYIs, resolved threads, automated notices, chats that ended naturally with nothing unanswered. The user clears these rather than deleting them, so do not call this bucket "delete". Show counts by type and name only items the user might be surprised to see.

Rank do-now items, and order every other bucket, by these signals in order:

1. **Hard deadline or time-bound decision:** due today or tomorrow, an expiring offer or event, a meeting that needs a reply first.
2. **Someone blocked on the user:** a teammate, partner, or candidate cannot move until they answer. Apply any response-time standard the user sets.
3. **Ladders to a goal:** today's MIT, then weekly, then longer-term. Name the goal.
4. **Relationship cost of delay:** key contacts, funders, personal relationships that go cold. Age is a supporting signal that differs by channel: an email unanswered for two days or a direct chat unanswered for three usually matters more than an old saved item.

## 7. Open the run

Do not show the full sorted list; seeing every bucket at once overwhelms. The opening message holds only:

```markdown
## Inbox zero: <date>, <sources>

**Missing data:** <failed or stale sources, or "none">
**Counts:** <N items: X do now, Y quick wins, Z delegate, T task, A no action>
```

Then go straight into the first non-empty bucket (or a person group, below) in the same message. Keep the full sort to yourself and reveal one batch at a time.

## 8. Work the buckets, one batch at a time

Go in bucket order and stop whenever the user wants. Each message shows one batch, or one do-now item, and asks only about what is on screen. Never ask about a later bucket early. End the turn and wait.

Answering a batch's questions is a decision, not completion. Move on only when the user says the batch is done. Until then, help them finish it, for example by drafting the replies they chose.

**Formatting:**

- Every time you name an item or person, including status notes, recaps, reminders, and question titles, link the name to its source.
- Number questions and letter options so the user can reply `1b, 2a`.
- Use real lists for groups. Never show severity or status by color alone; use words, symbols, and order.

**Group by person first.** When one person accounts for several items across buckets (at or above the grouping threshold), show their pile before the buckets in one message, split into "needs you", "discussion", and "reading or FYI", and suggest one way to batch them, such as one task or an already scheduled one-to-one. Clearing a person's pile in one decision beats meeting the same name in every bucket.

**Batches:**

1. **Do now, one item per message.** Read the full thread and check the calendar around any dates it mentions; the user may already have added holds. Gather only the context this decision needs, such as earlier threads with the sender or a related project record. Before saying the user still owes a reply or introduction, search every channel they might have used; it is often done elsewhere. For hiring or assessment items, use the user's chosen hiring guidance and only authorized evidence about role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Then write a short paragraph: who this is, what they want, what is at stake if it waits, and the recommended action, with evidence linked. Ask one to three questions only the user can answer. When they say it is done, show the next item.
2. **Quick wins, a small batch per message.** Each item gets its link, a line of context, and one recommended action, with lettered options when there is a real choice. The context line must say what the thing is. When a message refers to an event, plan, or person you cannot explain from the message itself, find it first (search other messages for the key term, check the group chat it came from, check the calendar for its dates) rather than relaying the ask blind. Say how many remain. Show the next batch when the user says this one is done.
3. **Delegate, a small batch per message.** Link, suggested owner, evidence. The user confirms or changes the owner.
4. **Task, a small batch per message.** Link, suggested name, due date. Create each one the user says to task. Flag existing tasks that already cover an item.
5. **No action.** Counts by type plus surprising items. The user clears them, unless they delegated clearing to you.

*Example (fictional).* A friend writes "Still in for Lantern Night?" On its own that means nothing. A search shows Lantern Night is a supper club dinner on Friday, first planned in a group chat, and the calendar shows it clashes with an existing hold. The quick win reads: "[Lantern Night](link): Friday supper club dinner from the group chat; clashes with your 7 pm hold. a) confirm and move the hold, b) decline."

**Meeting-related items.** When an item asks for a meeting, check the calendar for meetings already booked with that person in the next week before suggesting a new slot; an existing one-to-one or session often covers the ask. When a do-now item is preparation for a meeting in the next day or two, such as a document to review before a call, offer a meeting-prep workflow once the user has decided on the item.

**Catch work done mid-run.** Users often reply while the run is going. Before each new batch, check recently sent mail and messages, drop anything already answered, and note each in one line instead of asking again.

**Good questions** resolve real uncertainty: whether a goal is still live, whether the user wants to handle a relationship or hiring thread personally, whether an unfamiliar sender matters, how much time they have. Do not ask what the data already answers. The user can move any item to any bucket; their choice is final.

### Drafts, only when asked

- **Check the request against the thread first.** If a requested point repeats or contradicts what the other person already said, or misreads the ask, say so in one line and draft the version that makes sense. Follow the user's voice and channel conventions.
- **Default output:** one draft per response as copy-ready plain text in the final block, with the item's link on the line directly above. Finish all tool calls first so nothing pushes the draft out of the final block. Never send.

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

Do not pre-draft replies in the task unless asked. Afterwards, tell the user the item can now leave its inbox and give the record link if available.

## 9. Close and improve

End with a short per-source status:

| Source | Cleared | Tasked | Delegated | Still open | Unreviewed |
|---|---|---|---|---|---|
| [source] | [n] | [n] | [n] | [n] | [n and reason] |

If many loops remain open, say so plainly.

**Readiness check before calling a run complete:**

- Every in-scope source was read, or its failure is named.
- Every item is in exactly one bucket.
- No chat with an unanswered question sits in no action.
- Every attachment that carried an ask was opened before its item was bucketed.
- Nothing actionable lives only in an inbox: it is done, delegated, tasked, or explicitly left open.
- Every delegated clear was verified.

Then audit the run for friction: a pointless question, an item in the wrong bucket, a misbehaving source or query, or context you had to hunt for. With the user's permission, update the workflow's configuration to fix the cause, keeping changes general rather than tied to one message. Never store message content or credentials in it.

## Common failure modes

- Dumping every bucket at once instead of one batch at a time.
- Moving on after the user decided but before they acted.
- Doing the work a message describes instead of tasking it.
- Flagging a reply as owed when it was sent elsewhere.
- Judging a chat by its last message, so a closer or confirmation hides an older question.
- Tasking or bucketing an item from its preview when the real content sits in an unopened photo or file.
- Reporting a goal level as missing when the query, not the data, was wrong.
- Relaying an ask the user cannot place, instead of first finding the event, plan, or person it refers to.
- Proposing a new meeting when one with the same person is already booked.
- Showing the same person in every bucket instead of grouping their pile.
- Duplicating a task that already exists, or guessing an owner instead of saying "owner unclear".
- Quietly dropping a failed source or substituting a weaker one.
- Treating unread, new, or loud as urgent.
- Inventing links, or clearing a notification by changing the record behind it.
- Taking an external action, such as sending or archiving, that the user did not delegate.

## Optional extras

**Single-item mode.** Use this when the user, a reminder, or a scheduled prompt hands over one item, such as the oldest unhandled email or saved-for-later message.

1. Skip goals, sorting, the opening message, and closing. Do not read other inbox items. Read only that item, its source's access rules, and the context it needs.
2. Treat it as one do-now item: who this is, what they want, and what happens if it waits. Recommend one bucket and the concrete next action, with the item's link. Ask only questions the user alone can answer.
3. Help them finish it under the normal drafting and task rules.
4. Tell them which inbox action clears it, such as archiving the email or marking the saved item complete. If a reminder system checks the inbox itself, let it detect the change. Never require a special confirmation phrase like "done".
5. If you clear it on request and the action succeeds, continue straight into any waiting request in the same turn. Never make the user send a filler message to move on.

**Tick lists for items only the user can clear.** When the user must clear several saved items themselves, give them a list that mirrors their app's screen, in the same order the app shows:

| # | Opening words as previewed | Date | Decision |
|---|---|---|---|
| [position] | [first words of the message] | [date] | [✓ Clear, or Keep, plus a few words of reason] |

Afterwards, re-read the saved list to check the right items were cleared.

**Delegated clearing.** A common case is a tool with no quick manual way to empty its notification inbox. Clear an item only after the user says it is handled, done, or not worth acting on, or confirms the no action bucket. Never clear an item that is decided but not yet acted on, such as a reply still to post. Clearing a notification or marking a chat processed must never resolve, edit, or delete the underlying comment, thread, page, or record. Pass item identifiers in a way the tool reliably accepts, retry a transient error once, verify the result, and report it in one line ("Cleared 4, all verified, 29 left"). Name anything unverified as a failure, and know how to undo a mistaken clear. For chats, marking an item processed (so it does not return next run) fits when the user handled it elsewhere, chose to ignore it, or confirmed no action; do not mark chats the user still has to answer, since a sent reply drops off on its own.

**Saved drafts in apps, where authorized.** Save each draft as a reply in its own thread, never at the top level of a channel or conversation. Confirm it attached to the right thread, then open it in the app the user prefers so they can edit and send. In group threads, use the channel's real mention format for the person being answered and anyone the draft asks to act. Do not also paste the draft into the conversation; just say it is saved and opened. If a draft already exists there, say so rather than overwriting it. If you cannot read saved drafts back, never recreate an edited draft from your own version: ask the user to paste their current text, and save the revision only after they remove the old one. For copy-ready drafts, also copy the text to the clipboard if the user wants, and say so.

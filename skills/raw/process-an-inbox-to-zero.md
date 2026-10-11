---
name: process-an-inbox-to-zero
description: A privacy-aware workflow for converting authorized email and message inboxes into clear next actions without confusing triage with planning or deep work.
---

# Process an inbox to zero

Process one or more authorized inboxes into a trusted task system. Each reviewed item ends in exactly one bucket: **do now**, **quick win**, **delegate**, **task**, or **delete**. At the end of a run, no actionable commitment should exist only in an inbox: it has been completed, assigned, recorded as a task, or intentionally removed.

This workflow uses Inbox Zero and Getting Things Done principles. Processing means deciding what an item is and where it belongs. It does not mean completing all work described by messages, and it does not replace a separate daily-planning process.

Urgency is based on the consequence of waiting, not on unread status, recency, message length, notification volume, or whether an item is in a group conversation.

## Operating rules

1. **The user controls external changes.** Do not send, react, archive, delete, label, mark read, mark complete, or otherwise alter an inbox unless the user explicitly authorizes that specific action.
2. **No bulk changes by default.** Review each item, or a clearly defined group of routine items, before recommending any change.
3. **Do not draft unless asked.** When asked, provide copy-ready text. Do not save or send a draft without separate authorization.
4. **Create a task only with per-item authorization.** A request such as “task this” applies only to the clearly identified item. Do not create tasks in bulk.
5. **Use a work cap.** Ask the user to choose a cap, or use 15 minutes as a practical default. Work that can be finished within the cap may be do-now work; longer work normally becomes a task.
6. **Respect access boundaries.** Access private communications, calendars, records, and internal documents only for a legitimate purpose and with clear authorization. Use the minimum sources and information needed. Omit unrelated sensitive or personal details from output.
7. **Keep evidence separate from decisions.** Explain what the message shows and why a recommendation follows. Do not invent the user’s commitments, preferences, beliefs, or relationship judgments.

## Readiness gate

### Set scope, authority, and time

Identify the requested sources and confirm they are authorized. If scope is unclear, state a reasonable assumption, such as reviewing all authorized inboxes, rather than delaying with a separate scope question. If the user wants to prioritize an existing task list rather than messages, move to a planning workflow instead.

| User wording | Source to review |
|---|---|
| “email” or “work email” | Authorized work email account |
| “personal email” | Authorized personal email account, normally read-only |
| “team chat” | Authorized team workspace, including saved items, direct messages, and mentions |
| “community chat” | Only the named community or workspace |
| “messages” or “chats” | Authorized messaging services, optionally limited to one service |
| “all inboxes” | All authorized email and messaging sources |

Retrieve the current date, day, and time from a reliable time capability set to the user’s time zone. Do not estimate current time when deadlines, response windows, or planned focus blocks matter.

### Read goals and open work

When the user authorizes access to planning information, retrieve only what triage needs:

- Current longer-term and weekly goals.
- Today’s intention, plan, or most important task (MIT).
- Open tasks, including title, status, and due date.

Use the chosen system’s documented date-query method. Verify date filtering if results appear unexpectedly empty. Summarize active goals in three to six short lines for use during triage. If a planning level is absent or empty, note it briefly and continue; do not invent goals.

If a non-inbox MIT is scheduled now or soon, ask once before reading messages:

> Is inbox processing the most important thing right now, or does it just feel productive?

Trust the answer. Skip this question when inbox processing is planned work or no MIT exists.

### Check source readiness

Before retrieval, review applicable access rules and confirm each source is connected. If a source fails, place the gap at the top of the output and state:

- the failed source;
- the exact error or connection state;
- what could not be reviewed; and
- the safe next repair, such as reconnecting or reauthorizing access.

Continue with functioning sources. Never quietly omit a failed source or substitute another source that cannot provide equivalent information.

## Collect inbox candidates

Read selected sources in parallel when safe. For each candidate, collect: source, sender or participants, subject or conversation label, latest-message date, latest sender, one-line gist, and a stable link when safe and supported.

For email, group messages into threads and retain the latest relevant message per thread. Start with previews; open the full thread only when the ask, deadline, ownership, or current status is unclear. Routine newsletters, receipts, calendar notices, and automated updates are usually delete candidates. Inspect them further only when the preview suggests a decision, deadline, security issue, or financial consequence.

For team chat, treat saved-for-later items as work the user intentionally retained. Treat unread direct messages and mentions as attention debt, not automatic priorities. When otherwise equal, review direct messages and explicit mentions before broad channel discussion. Prefer a purpose-built inbox or audit view over search alone when search may omit saved, unread, or completion state.

For personal and networked chats, choose a lookback period with the user or use two weeks as a default. Determine reply debt by checking who sent the last meaningful message and whether a response is expected. Read nearby messages when the latest message does not establish the ask. Direct conversations generally rank above group messages unless a group message explicitly requests the user’s input or has a time-bound consequence.

## Classify and rank every reviewed item

Place every item in exactly one bucket:

1. **Do now:** important, time-sensitive, and completable within the selected work cap.
2. **Quick win:** a response or action likely to take about two minutes or less.
3. **Delegate:** work another person should own.
4. **Task:** meaningful work exceeding the cap, needing later context, or blocked until later.
5. **Delete:** no action needed, such as a resolved thread, FYI, routine notice, naturally ended conversation, or low-value subscription.

For delegation, suggest an owner only where current evidence supports it: the conversation, documented responsibilities, and current project context. If evidence is weak, say **owner unclear** rather than guessing.

Before suggesting a new task, check whether an open task already covers the work. If so, recommend clearing the inbox copy rather than creating a duplicate.

Rank do-now items, and order other buckets, using these criteria in order:

1. A hard deadline or time-bound decision, especially today or tomorrow.
2. A person blocked waiting for the user.
3. A clear connection to today’s MIT, weekly commitments, or longer-term goals.
4. Relationship cost of delay.

Age is supporting evidence, not a priority rule. Older unanswered messages may deserve attention, but do not override consequences and goals.

## Present the triage snapshot

Show the sorted result before working through items. Use labels and order, not color alone, to communicate priority.

```markdown
## Inbox zero: <date>, <sources>

**Goals used:** <longer-term goal> · <weekly goal> · <today’s MIT>
**Missing data:** <failures or “none”>
**Counts:** <total: do now, quick wins, delegate, task, delete>

### Do now
1. <item> — <source, sender, age> — <why now> — <link>

### Quick wins
- <item> — <one action> — <link>

### Delegate
- <item> — <suggested owner and evidence, or “owner unclear”> — <link>

### Task
- <item> — <suggested task title, due date if implied, and reason> — <link>

### Delete
- <counts by type, plus any surprising item>
```

Then ask two to four useful questions in one plain-text numbered block. Use lettered options where practical so the user can answer compactly, for example `1b, 2a`. Ask only about genuine uncertainty: whether a goal remains live, whether the user wishes to manage a sensitive conversation directly, whether an unfamiliar sender matters, or how much time is available. If nothing is uncertain, ask one question about available time. The user’s bucket choice is final.

## Work the buckets

Proceed in this order and stop whenever the user wants.

### Do now: one item at a time

Read the full conversation and check the calendar around relevant dates. Gather only decision-relevant context from earlier correspondence, project records, or documents. For hiring or assessment items, use authorized, role-relevant evidence only. Focus on capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance.

Provide a short paragraph covering who is involved, what they want, what is at stake if the user waits, and the recommended immediate action. Link supporting evidence where available. Ask one to three questions only the user can answer. When the user confirms it is handled, move to the next item.

### Quick wins, delegate, task, and delete

List quick wins together for a clearing sprint. The user performs inbox changes unless they specifically authorize an action.

For delegated and task items, get confirmation. When explicitly authorized to create one task, add it to the chosen task system with a clear action title, open status, implied due date, practical importance and urgency, time estimate, and relevant domain or project. Use this note format:

```markdown
**What:** The ask and who is waiting.
**Source:** Link or privacy-safe conversation citation.
**Context:**
- Key fact or constraint.
- Relevant deadline, decision, or linked record.
**Next step:** The first concrete action.
```

Do not put a prewritten reply in the task unless requested. After task creation, tell the user the inbox item can now be cleared and provide a task link if the system supports one. For delete items, remind the user which messages can be archived, deleted, or marked complete.

## Drafting, closure, and audit

When asked for a draft, provide one copy-ready plain-text draft as the final block of the response. Match the requested channel and tone. Keep claims factual and avoid commitments the user has not approved.

End with concise source-by-source status: completed, tasked, delegated, still open, and unreviewed because of access or time. Say plainly if many loops remain open.

Audit the run for pointless questions, incorrect bucketing, incomplete sources, excessive context searching, and privacy risks. Record only general workflow improvements in authorized documentation. Do not store message content, credentials, or unnecessary personal details.

## Single-item mode

Use this mode when the user or an authorized reminder identifies one specific inbox item. Do not inspect other inbox items.

1. Read the source rules and retrieve only the item plus minimum necessary context.
2. State who is involved, what they want, what happens if it waits, the recommended bucket, and the concrete next action.
3. Help the user handle it under the normal authorization, privacy, task, and drafting rules.
4. Tell the user which inbox action will clear it afterward, such as archiving an email or completing a saved chat item. Do not require a special confirmation phrase.

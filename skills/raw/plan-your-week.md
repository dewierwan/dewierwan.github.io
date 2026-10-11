---
name: plan-your-week
description: Review the past week, shape one to three verifiable goals through focused interview rounds, then turn them into approved tasks, calendar blocks, and a one-screen plan.
---

# Plan your week

Plan the coming week as a deliberate shaping session. Research sets the constraints. A few interview rounds, each built on the last set of answers, find out what actually matters. Only then turn the result into a short written plan, approved tasks, and approved calendar blocks.

Aim for about an hour. This ritual anchors the week, so it may run longer when the shaping needs it. The conversation does the hard work. The final plan should feel simple.

## Core principles

1. **Pressure is not importance.** A deadline, a stale task, a senior counterpart, or a visible event is evidence of pressure. It is not evidence that something deserves to be a weekly goal. Never recommend a goal only because it is scheduled, overdue, or easy to make concrete. The user must first say what they want to make true, why it matters now, and what they will deprioritize for it.
2. **Evidence prompts questions; it does not answer them.** Sources can show deadlines, obligations, slippage, and capacity. Only the user can say what they value this week.
3. **Complex conversation, simple output.** Keep research detail, task metadata, and calendar mechanics out of the final plan unless they change a decision.
4. **Propose, approve, then write.** Every goal, task, status change, and calendar event is written only after the user approves that specific item. Never batch-create.
5. **Ask or search; do not guess.** If the user mentions an unfamiliar name, project, or reference that affects goals, the calendar, or a rollover decision, run one or two quick searches in authorized sources. If it is incidental, move on.
6. **Check that stored context is still true.** Notes like "delegated until X happens" or "paused for two weeks" expire. Before citing one, check whether its trigger has passed. If the user corrects a stored note, update it in the same session.

## Privacy and access boundary

This workflow may touch calendars, messages, tasks, health data, and records about colleagues or candidates.

- **Purpose and authorization.** Read only sources the user has connected and agreed to use for weekly planning. Health, sleep, and exercise data are opt-in.
- **Minimum necessary.** Prefer counts and metadata over contents. For email and chat, counts and days-waiting are usually enough. Open a message only when the user asks or one specific item is needed for a decision.
- **Private writing stays private.** Do not read or quote a freeform private journal unless the user shares it in the session. Use structured fields instead (daily plans, ratings, stated reasons, fields the user designates for brain dumps). If a source mixes private text with planning data and you cannot exclude the private part before reading, skip that source.
- **Other people.** Mention colleagues and candidates only as far as the decision needs. Keep health, emotional, and personal details about others out of the plan. Write "rebalance workload for the operations lead", not why they are struggling.
- **Output boundary.** The plan lives in the user's own system. Do not copy colleague or candidate details into shared spaces. Draft messages for the user to send; never send on their behalf.

## Setup: user choices

Ask once, store the answers, and reuse them. Offer the default when the user has no preference.

| Choice | Broadly useful default |
|---|---|
| Planning day | Last workday of the week, or Sunday evening |
| Week boundaries | Monday to Sunday |
| Maximum weekly goals | 3, with 1 as the ideal |
| Unplanned buffer | 20% of free working time |
| Planning system | The user's task manager, notes app, or spreadsheet |
| Calendar conventions | Solo work as focus-time events in a distinct colour; plain titles |
| Time zone | Ask; restate it to any helper that reads the calendar |
| "Behind" thresholds | Email older than 48 hours; direct messages unanswered over 3 days |
| Health floor | User-defined sleep, exercise, and recovery targets, or none |
| Chronic-deferral threshold | Tasks deferred more than 5 times move to a parked list |
| Workflow self-improvement | Note lessons at the end; ask before structural changes |

## Deliverables

The session is complete only when these exist, or the user has explicitly waived one:

1. Up to three weekly goal records, each linked to a longer-term goal, each with a definition of done of two to four checkable outputs.
2. The target week's plan record holding the simple plan, and the previous week's record holding the user's review answers.
3. Task records, created or updated in place, for every concrete chunk of work each goal needs. Each is 5 minutes to 3 hours, clearly titled, with prepared notes, and approved individually.
4. Calendar events, each slot approved, for goal and task blocks and protected routines.
5. Status updates for overdue tasks the user decided on (unless they triage themselves).
6. Drafted messages for any meetings the user chose to cut or move.

Analysis without these artefacts is not a finished weekly plan.

## When to use and which variant

Use this when the user asks to plan the week, or to review and plan it, and on their planning day. Any request that combines reviewing and planning the week belongs here, not in a daily review.

Default target: the week starting next Monday. On a Monday, the current week.

| Situation | Adjustment |
|---|---|
| End-of-week run (default) | Review the current week as "last week". Ask what must still ship before Monday and treat it as current-week work, not a next-week goal. |
| Run on the first day of the target week | Ask early, "What must ship today?" and build that day first. Re-read calendar and task status before writing. |
| Belated mid-week run | Plan only the remaining days. Treat elapsed days as review context. State the runway up front. |
| Time-off week | Skip goals, tasks, hiring, and cuts. Confirm recurring meetings are declined. Plan rest and logistics in whatever document the user names. |
| User is exhausted | Stop open questions. Offer 2 or 3 concrete options, or decide with stated reasoning and let them veto. |

## Hard rules

- **At most three weekly goals.** Merge, demote to intentions, or defer the rest. With three, label one the stretch goal. One is ideal.
- **Definition of done a teammate could verify:** two to four concrete outputs, such as "Sent version 2 of the scorecard and job description to the hiring partner." "Everyone in the process has next steps" is binary but unscoped. A direction is not a goal.
- **The week fits with the buffer unplanned.** If it does not fit, cut or shrink a goal. Never shrink time estimates.
- **Every goal links to an active longer-term goal.** Ask "Which longer-term goal does this serve?" A weak answer means reject.
- **Use the existing week record** if one exists; it may already have goals linked. Create one only if missing.
- **Write task status after each decision**, not all at the end.
- **No goal proposals before two substantive, answer-dependent interview rounds**, unless the user asks to skip questions. Each round resolves a different layer.
- **Keep an alignment ledger.** Show it compactly before each later round. Never reintroduce a corrected assumption.

## Generic data model

Map these to the user's systems. Field names are suggestions.

| Record | Key fields |
|---|---|
| Plan (week, month, quarter, year) | type, start, end, linked goals, plan text, review text. Higher levels hold theme, non-negotiables, any scorecard. |
| Goal | statement, deadline, status, priority, level, linked plan, notes ("Links to" and "Done when"), deadline-change count |
| Task | name, due date, status (todo, in progress, done, parked, archived), importance, urgency, estimate, notes, deferral count |
| Daily log | date, daily plan, overall rating and reason, focused hours, intention for tomorrow |
| Recovery and exercise (opt-in) | per night: hours asleep, hours in bed, device score, variability; per session: date, type, volume |

Useful saved queries: current and previous week records, active higher-level plans, active longer-term goals, last week's goals with a four-week hit rate, overdue and due-soon tasks, parked tasks (titles and deferral counts only), recent daily logs, and the last two weeks of recovery and exercise data.

## Step 1: Gather context

Run reads in parallel. Delegate anything likely to be large (a full week of calendar events, a long parked list, a hiring pipeline) to a helper with a tight brief and a word limit, and ask for only what a decision needs. Bound each helper's runtime. If a call fails twice, record the gap and move on. Never present partial data as complete.

Read:

- **Planning records** from the data model above.
- **Team context (read-only):** current sprint or planning page, active team goals, projects the user owns. If the team held a goal-setting meeting today, read only the user's own review answers and shortlisted goals.
- **Calendars:** the target week, via a helper that returns meetings per day, non-trivial meetings as "date, time — title (counterpart role)", weekend conflicts, and cut candidates, in under 400 words. Read personal and social calendars if authorized; never block work over personal events. Treat unconfirmed invites as unconfirmed and sanity-check imported time zones.
- **Inbox signals (counts only):** email past the threshold and in total, the chat action queue, unread direct messages and mentions, and unanswered direct messages with days waiting. Count threads, not messages. If a result hits its cap, report ">N".
- **Opt-in signals:** recovery data, completed and prescribed training, hiring load (see below).

## Step 2: Recap, the user's review, then the brief

Run these in order: short overview, the user's own review, then your analysis.

**a) Recap, five lines maximum, no analysis:** active longer-term goals with countdowns; last week's goals as done, missed, or open; four-week hit rate ("3 of 7 goals hit"). Open goals past deadline count as missed unless the user says they shipped.

**b) The user's review.** Ask in one block, then end your turn:

1. Did you hit your goals for the week?
2. What went well?
3. What didn't go so well?
4. What will you do differently next week?

If they already answered at a team meeting, quote their answers and ask only what changed. The aim is one thing to change, not blame. Save the answers to the reviewed week. Carry "do differently" into shaping and the failure-mode line.

**c) The brief.** Synthesize internally. Show at most eight bullets, only facts that could change a decision. Group routine signals; foreground tensions, surprises, real constraints, and data gaps. Do not recommend goals. Check these areas and include only what matters:

- **Rollover and slippage:** each unfinished goal with its deadline-change count. Anything open after four or more changes gets the question: "This has slipped N times. Is it still the right goal, or is the format, scope, or lane wrong?" Raise it here, not an hour in.
- **Close-out:** did end-of-week items actually ship? Ask rather than assume.
- **Capacity:** meetings per day, energy, sleep, focused hours, training (thresholds below).
- **Backlog:** overdue count, important-and-time-sensitive count, and one to three parked items that now fit (or "none fit").
- **Messages:** what is past the thresholds. A non-empty action queue is not failure; stale items with no owner are.
- **Commitments that may not be on the calendar:** externally dated work such as a program cohort the user must onboard or a registration window. Check the relevant records or ask. These beat self-set goals on timing.
- **People:** team goals that imply user action; a colleague the user has said is overloaded (ask at goal-setting whether reducing that load is the real priority); two or more recent joiners (ask whether onboarding is scheduled).
- **Non-negotiables:** hits and misses against the current higher-level plan.

### Signal thresholds (defaults; let the user set their own)

| Signal | Flag when | Notes |
|---|---|---|
| Energy | 2+ clearly negative days in 7, or a run of neutral ratings | On a -2 to +2 scale, neutral often hides a bad day. If logs are blank, say so and name the fallback signals used. |
| Focus | Focused work trending under about 3 hours a day | Context, not a verdict |
| Sleep | Any night under 6.5h asleep; 3+ nights under 7h; variability below 90% of last week; device score average under 75 | Use time asleep, not time in bed. Compare variability only within one device and method. |
| Training | Sessions below target, or the key session missed | Zero sessions for two weeks usually means a sync gap; ask before concluding |
| Meetings | Days over 4 meetings | Also note meeting-free days |
| Messages | Items past the user's "behind" thresholds | Report counts and days waiting |

Report fired flags with numbers and dates ("3 nights under 6.5h: Mon 6.4, Wed 6.2, Thu 6.3; average 6.7h"). Vague phrasing is not acceptable. Do not average across missing nights after travel or device changes; call it a device gap. After crossing time zones, frame short nights as circadian adjustment, not bedtime discipline.

### Hiring load (if the user hires)

The purpose is allocating the user's time, not assessing anyone. Ask a helper for a report under 250 words:

1. Confirmed interviews this week with the user as interviewer, with day, time, role, and total hours. Exclude "needs scheduling" placeholders. If the query fails, use the calendar.
2. Late-stage candidates whose decision may be owed. Measure time in stage only from the real stage-entry date, never the application date, which makes everyone look overdue. If entry dates are unavailable, report stage counts only and say so.

If decisions are past the user's service target (a common one is five days, ideally two) or interviewing exceeds about three hours, name the cost of delay and ask who owns the response. Propose a block only after the user confirms hiring belongs on their week. Say "none overdue" when true. Keep candidate details and evaluations out of the plan.

### Alignment ledger

End the brief with this, and update it before each later round:

- **Confirmed:** choices the user made in this conversation, or current agreed plans.
- **Source facts:** constraints and evidence.
- **Inferred:** your tentative interpretations, labelled.
- **Open:** decisions only the user can make.
- **Corrected:** assumptions the user rejected (omit if empty).

## Step 3: Rollover decisions

Last week's goals may be goal records or freeform lines in last week's plan text; check both. Before treating an item as unfinished, check whether it was **delegated** (then it is not a weekly goal; note the handoff) or **already done** (records go stale; propose marking it done).

For each item still on the user, ask separately: **roll over, demote, or drop.**

- **Roll over:** a candidate goal. Ask "Why did it slip?" and log one line. Increment the change count and set the new deadline.
- **Demote:** an intention in the plan text, not a goal.
- **Drop:** mark missed or archived.

## Step 4: Shape the week through interview rounds

**Check for a plan of record first.** A recent written priority list, or goals shortlisted at a team meeting, outranks anything inferred from tasks. Ask "Is there a written plan of record?" Treat shortlisted goals as decided: check each has a verifiable definition of done and fits the week, then mirror them into goal records.

**Question format.** Ask 4 to 8 questions per round. Number every question. When options are bounded, letter them and put your recommendation first. One decision per question, so the user can reply "1a, 2c, 3 skip". Example:

```text
1. Which area most needs attention this week?
   a) Shipping the proposal (recommended: it is the open longer-term goal)
   b) Hiring decisions
   c) Recovery
2. What would you regret neglecting even if the proposal ships?
```

**Round 1: brain dump, then desired change.** Ask for a quick, unfiltered list of everything they might work on, task-shaped or vague. Group it by goal or project and show it back in a few lines, so the chosen goal is not just their first idea. Park small items for triage. Then work backward:

- What outcome would make the week genuinely matter?
- Why does it matter now, beyond a deadline?
- What has changed since last week's plan?
- Which area (work, personal, health, relationships) most needs attention?
- What is strategically or emotionally unresolved?
- What would you regret neglecting even if the visible work shipped?

Do not answer these from sources. Classify each answer as confirming, rejecting, softening, qualifying, or deferring your current model. Trace the implications and show the updated ledger.

**Round 2: shortlist.** Apply the prompts that bite this week:

- What can you do best, and what could someone else do as well?
- What would most move the team's main goal or the relevant longer-term goal?
- What benefits most from lead time?
- What unfinished work will keep stealing attention unless closed now?
- What is the strongest case for not doing this?
- Which fires are you willing to let burn?

Also settle real capacity (meetings, energy, sleep, exercise) and which commitments depend on others. Everything not shortlisted goes to "Not this week" or a "Later" list.

**Round 3, when needed:** if sequencing, success criteria, ownership, or the week's shape is still materially open. If the user is tired, narrow to two or three options; fatigue is not permission to revive an earlier inference.

### Readiness gate

Propose goals only when every item is confirmed, established, or deliberately left open:

| Gate item | Status |
|---|---|
| The one change that would make the week worthwhile | [confirmed / open] |
| Why it matters now | [confirmed / open] |
| The longer-term goal it serves | [confirmed / open] |
| Definition of done: 2–4 verifiable outputs | [confirmed / open] |
| Main competing claim on time or attention | [confirmed / open] |
| What is explicitly not advancing | [confirmed / open] |
| Realistic health and energy floor | [confirmed / open] |
| Most likely failure mode | [confirmed / open] |

For each candidate goal, ask yourself: did the user call this important, or am I promoting a visible deadline? If the latter, ask another question. Then propose the smallest set of goals that expresses the alignment, usually one or two, each in one sentence.

### Validate each goal

- **Links up:** name the longer-term goal and record it.
- **Verifiable:** two to four outputs. Narrow a direction to a named set and a named output.
- **Scoped:** sketch sub-tasks with rough hours and sum against free time minus the buffer. Under an hour is a task, not a goal.
- **Realistic:** heavy meetings plus low energy means cut one.
- **Stretch:** with three goals, mark one that may give way.

### Shaping rules of thumb

- **Shrink scope when the pattern says so.** If the current higher-level plan has a cut-scope rule that keeps firing, or goals keep slipping, default to one goal and ask what has changed before accepting more.
- **Name the kind of week.** If meetings, hiring, logistics, or supporting colleagues dominate, ask whether they want a people week or want to cut enough to protect one deep goal. "Defend harder" usually fails; ring-fence one deep item on the cleanest day.
- **External deadlines go first.** With two or more goals, ask which has the harder external deadline. It ships first, even if the other feels heavier or has rolled over longer.
- **Team goals need an announcement.** If a goal needs the team, ask what end-of-week goal to give them and where to announce it. Offer two or three framings with a recommendation and draft the message.
- **Respect the soft stop.** If after two or three rounds of pushback the user says "stop arguing, write it down", accept and move on. Record your concern in the failure-mode line.
- **Be firm when it helps:** "That's four goals; pick three." "You said this three weeks ago. What's different?"

## Step 5: Non-negotiables

Check whether the current quarter or month plan lists non-negotiables or a scorecard. If one exists, score its own lookback with its own items and threshold, and raise any fired cut-scope rule during shaping. If an item is out of date, update the higher-level plan after approval, not just this week. If no current plan exists, say so once and ask what minimum health, relationship, and recovery floor they want. Never revive an expired scorecard.

Honour explicit pauses: do not re-propose a paused habit or retired experiment; ask at most once whether it is back. Check that a protected day (writing day, rest day) is actually free before relying on it.

If a non-negotiable is faltering, ask up to three follow-ups until the user names **a specific action plus a day and time.**

| Quality | Example |
|---|---|
| Accept | "Phone out of the bedroom from Tuesday; wind-down alarm at [time] each evening." |
| Accept | "Long run Saturday at [time]. Mobility session Thursday after lunch." |
| Reject | "I'll try to sleep more." |
| Reject | "I'll exercise more this week." |

**When sleep is flagged:** lead with the numbers and the user's target. Protect their normal sleep window rather than moving it; cap any shift at about 30 minutes earlier, since large shifts under load rarely hold. Require both a bedtime and a wind-down trigger, because the hour before bed is what fails. If the same issue appeared last week, ask what is actually different. Record the commitment word for word so next week can compare.

## Step 6: Cut the calendar

Ask first: "Do you want to cut meetings this week, or keep them all?" If keep, note "No cuts" and skip.

Otherwise, for each meeting ask whether it serves a weekly goal, a non-negotiable, or a team commitment. If none, it is a candidate. The user decides per meeting: keep, cut, shorten, or reschedule. Draft a short, warm, specific message for each change; the user picks the channel and sends it. For recurring meetings someone else organizes, the action is a message to the organizer, not a calendar edit.

## Step 7: Task triage

Ask whether the user wants to triage themselves. If yes, note it and skip the writes. If they pause mid-session to clear loops, re-read tasks and inboxes live before advising. Do not park tasks the user called important; give them dated slots. Check who is responsible before suggesting delegation.

**First pass:** offer tasks past the deferral threshold as one batch: "These N tasks have been deferred 5+ times. Move to parked?" Default to parked, not archived.

**Second pass, one by one**, sorted by importance, urgency, then age:

| Decision | Write |
|---|---|
| Do this week | Keep todo; due date in target week; candidate for a block |
| Already done | Mark done |
| Punt | New due date; increment deferral count |
| Delegate | User names the role or person; note "Delegated to [role] on [date]" |
| Delete | Archive |

Write after each decision; small batches are fine if the user is moving fast.

## Step 8: Pre-mortem and deprioritize

Do this before blocking time, so the answers shape the blocks.

- **Pre-mortem:** "If this week fails, what is the most likely reason?" One to three lines.
- **Deprioritize:** "What can you delete, delegate, reschedule, or reset expectations on? What in-flight work will you explicitly not push this week?" Pausing one parallel stream helps the others ship.

## Step 9: Break goals into tasks

For each goal, propose one to five tasks of 5 minutes to 3 hours that together complete it. Also add tasks for "do this week" triage items, delegation follow-ups, and meeting prep that needs its own time.

- **Hold creation when a decision is pending.** If an upcoming decision could reshape a goal, create only tasks that survive either outcome.
- **Use a compact table for four or more tasks** (number, task, due, estimate, owner). Write full notes on approval.
- **Prepare before proposing.** Gather links from what you already read. For writing, sketch an outline; for an email, draft it; for a review, list the items; for a decision, lay out options and trade-offs.

**Per task:** (1) check for duplicates by searching open and parked tasks for two or three distinctive title words, and update the existing record if it is the same work; (2) propose title, notes, and fields inline; (3) accept edits and drop rejections; (4) write one at a time and keep the reference for calendar linking.

**Field defaults:** importance follows goal priority; urgency is time-sensitive if it must land this week, immediate only for same-day external asks, otherwise flexible. Spread due dates in natural order across the week. Use realistic estimates (5, 10, 20, 45, 60, 90, 120, 180 minutes). Match existing title style; verb-first is usually clearest.

**Notes template** (use checkbox syntax the user's system renders):

```markdown
Serves weekly goal: [goal]. Links to: [longer-term goal].

Done when: [one binary sentence]

Checklist:
[] [first concrete action]
[] [next action]

Refs:
- [anchor document or thread]
- [draft or research already gathered]

[Optional: draft, outline, or option trade-offs]
```

If a section is genuinely empty, say so in one sentence. **Avoid:** a single task that restates the goal; more than five tasks per goal (flag it as a project); tasks for routines, which belong in the plan and calendar; silent batch creation.

## Step 10: Calendar blocking

**Show the week as short day-by-day paragraphs first**, with open questions at the end. Detailed tables come only after the shape is agreed.

**Check capacity:** total the proposed blocks against working hours left after meetings. If they exceed the non-buffer share, cut or shrink a goal with the user. Count evenings as capacity only if the user really works them, and pair late work with a hard stop when sleep is shaky.

**Block rules:**

- Reuse focus blocks the user already created by renaming them instead of adding new ones. Do not label a long block that spans meals or meetings as one task; split it into precise slots.
- Treat blocks the user adds mid-session as theirs; fill only real gaps.
- Solo work uses the focus event type and colour; ordinary events are for meetings, calls, workouts, and errands.
- Re-read the live calendar right before writing and verify every slot.
- If a block is shorter than the task estimate, flag it and offer a longer block, a split, or a smaller task.
- Propose a 1–2 hour inbox and messages block whenever anything is past the "behind" thresholds or a regular team update is due.
- Block protected routines explicitly, including prescribed training sessions; the key session wins if only one fits. If a routine conflicts with a protected rest day, ask once and carry the answer forward.

**Per slot:** propose day, exact start and end, and duration ("Writing — draft 2 — Saturday [start]–[end], 3h. OK?"), create on approval, or offer the next best slot. Before creating anything, ask: **"What else am I missing?"**

## Step 11: Write the simple plan

**Goal records:** check goals already linked to the week record first. If one matches, update it in place and increment its change count. Create only genuinely new goals. Add links; never replace existing ones.

**Week record:** write the plan text. It is a clarifying summary, not an audit log; aim for one screen. Omit empty headings. Use at most two goals unless the user chose a third. Keep triage, rollover detail, and meeting mechanics in the underlying records.

```markdown
## Theme
[theme from the higher-level plan, or a 2–5 word theme]

## Weekly goals
[] [Goal 1] — links to [longer-term goal]
    Done when: [2–4 checkable outputs]
[] [Goal 2] (stretch, if three goals) — links to [longer-term goal]
    Done when: [2–4 checkable outputs]

## Protect
- [health, relationship, or recovery floor with concrete slots]

## Week shape
- [day]: [the one essential focus or constraint]

## Not this week
- [explicitly deprioritized work]

## Failure mode
- [most likely failure] → [specific counter]
```

## Step 12: Close

Give one sentence of counts: goals committed, tasks created or updated, blocks booked, meetings cut, tasks triaged. If a current scorecard exists, show its success bar compactly. Then end with the final plan on one screen: theme, goals with definitions of done, what to protect, the day shape, what is not happening, and the failure mode with its counter.

Do not recap the research, interview, or tool mechanics. End with one sentence. No thanks, no extra summary.

## Step 13: Improve the workflow

Before finishing, note what to change next time: what wasted time, which assumption was wrong, what the user corrected, what new pattern appeared, and which step never helped. If the user has opted in, also look briefly at the week's interactions with their assistant for repeated corrections or frustration that never became a saved instruction, and propose a specific fix.

Write precise edits to the user's saved workflow notes; one exact line beats a general reminder. Show a two- or three-bullet summary. Apply small fixes directly if the user agreed to that; ask before adding or removing a step. If nothing is worth changing, say so.

## Common failure modes

| Failure | Counter |
|---|---|
| Promoting the most visible deadline into the top goal | Ask why it matters before proposing |
| Rolling the same goal over again and again | Show the change count in the brief; question goal, format, scope, or lane |
| Planning the week before learning what must ship today | On first-day runs, ask first |
| Missing a commitment that is not on the calendar | Check external dates; ask |
| Assuming deep-work capacity in a people-heavy week | Ask which kind of week the user wants |
| Writing from stale reads, notes, or scorecards | Re-read live; check expiry triggers and dates |
| Treating a data gap as real behaviour | Ask before concluding |
| Blocks shorter than task estimates | Compare and flag |
| Overwhelming proposals | Day paragraphs first; compact tables for batches |
| Arguing past the soft stop | Accept, write it down, record the concern |

## Style

- Be direct and brief. Say "this will fail because X" when you believe it.
- No celebratory step summaries. Move on.
- Use one unambiguous date format throughout.
- When stuck, narrow with two or three concrete options; do not propose the whole week before the gate passes.
- **Low-capacity signal:** if energy, focus, or sleep flags fire, treat it as a hypothesis to test. Ask how much capacity is real and what recovery must be protected. Once confirmed, shape a lighter plan, usually one goal, with more rest and harder cuts.

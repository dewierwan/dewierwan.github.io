---
name: plan-your-week
description: Review last week and plan the next: shape one to three verifiable goals, protect health and focus time, cut low-value work, and schedule approved tasks and blocks.
---

# Plan your week

Plan the upcoming week as a deliberate shaping session. Research sets the constraints. A few rounds of questions, each building on the previous answers, establish what matters. Only then turn the result into goals, tasks, calendar blocks, and a short written plan.

Aim for about an hour. This is the ritual that anchors the week, so it may run longer when the shaping needs it. The conversation does the complex work. The final plan should feel simple.

## When to use this

Use this workflow when the user asks to plan the week, review and plan the week, or run a weekly planning session. Any request that combines reviewing the past week with planning the next belongs here, not in a daily review or daily plan.

## Setup: confirm once, then reuse

On the first run, ask for these choices. Offer the default when the user has no preference.

| Choice | Question to ask | Default |
|---|---|---|
| Planning day | Which day do you plan the week? | Friday or Sunday |
| Target week | Which week is being planned? | The week starting next Monday; the current week if run on Monday |
| Planning system | Where do goals, tasks, plan notes, and events live? | One goals-and-notes space, one task list, one calendar |
| Higher-level goals | Which annual or quarterly goals should weekly goals serve? | Ask for 2 to 5 |
| Goal cap | Maximum weekly goals | 3, with 1 as the ideal |
| Buffer | How much of the week stays unscheduled? | 20 percent |
| Working hours and time zone | When do you actually work, and where are you this week? | Ask each time travel is possible |
| Health and recovery floor | What sleep, exercise, rest, and relationship time must be protected? | Ask; never assume |
| Allowed sources | Which records may be read, and which are off limits? | Only what the user explicitly allows |
| Calendar style | How should solo focus blocks look? | A focus-time event type with plain titles |

## Deliverables

The session is not complete until these exist, unless the user explicitly skips one:

1. Up to three weekly goal records, each linked to a named higher-level goal and carrying a definition of done of two to four checkable outputs.
2. The target week's plan note filled with the simple plan, and the previous week's record holding the user's answers to the four review prompts.
3. Task records, created or updated in place, for every concrete chunk of work needed to hit each goal. Each task takes 5 minutes to 3 hours and has notes that make starting easy. Each is approved individually.
4. Calendar events for approved blocks, each slot approved individually.
5. Updated statuses for every overdue task the user made a decision on.
6. Drafted messages for any meetings the user chose to cut or move. Print them; never send them.

Analysis without these artefacts is not a finished session.

## Core principles

**Pressure is not importance.** A deadline, a stale task, a senior counterpart, or a visible event shows pressure. It does not show importance. Never recommend a goal only because it is scheduled, overdue, or easy to make concrete. The user must first say what they want to make true, why it matters now, and what they will set aside for it.

**Ask or search; do not guess.** If the user mentions an unfamiliar person, project, or reference that affects the goals, the calendar, or a rollover decision, run one or two quick searches in allowed sources or ask. If it is incidental, move on.

**Facts expire.** Stored notes such as "this is delegated until X" or "paused for two weeks" age quickly. Check whether the trigger has passed before citing one. If the user corrects a stored fact, update it in the same session.

**Sync gaps are not behaviour.** Zero exercise sessions, missing sleep nights, or an empty log often mean a sync or device problem, especially after travel or a device change. Report the gap and ask; never average across a hole.

**Respect the privacy boundary.**

- Read only sources the user has authorised, for the purpose of planning their week.
- Do not read freeform private journals unless the user explicitly allows it. Prefer structured fields (ratings, short reasons, daily plans) and what the user says in the conversation. If private content cannot be reliably excluded from a source, skip that source.
- For email and messages, use counts and metadata. Open content only when the user asks or a specific item is load-bearing.
- When records involve other people, use the minimum needed and refer to them by role where possible. Never record health or other sensitive details about others in the plan.
- Keep outputs inside the user's own planning space unless they choose to share them.

## Run variants

Detect the variant before gathering context.

- **Before the week starts (default).** Part of the current week remains. Review it as "last week" and ask what must still ship before Monday. Treat that as current-week work, not a goal for the target week.
- **Same-day or late run.** If the target week has already started, plan only the remaining days, use elapsed days as review context, and never block time in the past. On a Monday, ask early "What must ship today?" and build that day first. Say how much runway is actually left, because it shapes everything.
- **Time-off week.** Skip the work machinery: no work goals, triage, or meeting review beyond checking recurring meetings were declined. Plan rest, travel logistics, and any loose ends in the place the user prefers.
- **Tired user.** If the user says they are too tired to answer, stop the rounds and decide for them with stated reasoning, or offer two or three concrete options.

## Hard rules

- **Goal cap.** At most three goals; one is ideal. If the user proposes more, merge, demote to an intention, or defer. With three, label one as stretch.
- **Verifiable done.** Each goal needs two to four outputs a teammate could check, such as "Sent revised role description and scorecard to the hiring lead." A binary but unscoped goal ("everyone has next steps") is not enough, because nobody can estimate it. A direction is not a goal.
- **The week must fit the buffer.** If goals do not fit, cut or shrink a goal. Never shrink time estimates to make them fit.
- **Every goal serves a higher-level goal.** If it does not, ask which one it serves. A weak answer means reject.
- **Approve before writing.** Calendar events are created only after the specific slot is approved. Tasks are created only after each is approved. Never batch-create.
- **Write task decisions immediately**, not at the end.
- **Reuse existing records.** Check whether the target week's plan record already exists, possibly with goals linked. Create one only if truly missing.
- **At least two substantive question rounds before proposing goals**, unless the user asks you to skip and decide. Each round resolves a different layer of the week.
- **Keep an alignment ledger** and show a compact version before each later round. Never reintroduce an assumption the user corrected.

## Step 1: Gather context

Run reads in parallel where possible. Send any read likely to return a large result (a full week of events, a long parked-task list, a hiring pipeline) to a filtered query or helper process that returns a short summary. Do not dump raw data into the conversation. If a query is slow or fails twice, report it as a gap and use other signals.

Read, as available and authorised:

1. **Plans:** current and previous week records; current month and quarter records (theme, non-negotiables, scorecard).
2. **Goals:** active higher-level goals, last week's weekly goals with how often each deadline moved, and the hit rate over the last four weeks.
3. **Tasks:** overdue and due-next-week items, plus a titles-only summary of parked items with deferral counts.
4. **Daily records:** about ten days of structured fields such as rating, focus, focused hours, and daily plan.
5. **Health data, if tracked:** sleep for the last two weeks; exercise completed last week and prescribed for next week.
6. **Team context, read-only:** team goals, projects the user owns, and the user's own input to any team planning meeting.
7. **Calendars:** the work calendar summarised as meetings per day, notable meetings in the form `DD MMM start-end - title`, weekend intrusions, and cut candidates; personal and social calendars read-only, since they constrain evenings and weekends. Treat unconfirmed invitations as unconfirmed.
8. **Communication load:** email threads older than the user's response window, total inbox, the chat action queue, unread mentions, and direct messages awaiting a reply, with age in days.
9. **Role-specific load:** for example interviews and pending hiring decisions (see the audit template below), or dated external commitments such as programme starts or launches the user owns. These often live outside the calendar, so scan the shared trackers or channels where they are announced.

**Optional process retro.** If the user wants it and grants access, spend up to three minutes scanning their recent requests to their assistant for repeated corrections, annoyance, confusion, or missing capabilities. Exclude anything that may contain private journal material. Cluster duplicates, check whether each already became a standing instruction, and propose specific edits for the user to apply, skip, or modify. If nothing recurs, say so in one line.

## Step 2: Recap, the user's review, then the brief

Run these three parts in order.

### a) Recap (five lines maximum, no analysis)

- Active higher-level goals, one line each with a countdown.
- Last week's goals: done, missed, or still open.
- Four-week hit rate, such as "3 of 7 goals hit". Goals open past their deadline count as missed unless the user says they shipped.

### b) The user's review

Ask these four prompts in one block, then end your turn:

1. Did you hit your goals for the week?
2. What went well?
3. What didn't go so well?
4. What will you do differently next week?

If the user already answered elsewhere, quote their answers and ask only what changed. The aim is one thing to change, not blame. Save the answers to the reviewed week's record. Carry the "do differently" answer into shaping and the final failure-mode line.

### c) The brief

Show only facts that could change a decision, in eight bullets or fewer. Group routine signals; foreground tensions, surprises, constraints, and gaps. Do not recommend goals and do not repeat the user's review back to them. Consider:

- **Rollover candidates**, each with its deadline-moved count. Any goal moved four or more times and still open gets the question: "This has slipped N times. Is the goal still right, or is the format, scope, or lane wrong?"
- **Close-out:** did last week's end-of-week work actually ship? Ask rather than assume.
- **Capacity:** meetings per day, heavy days (more than four meetings) and clear days, protected days that are already claimed.
- **Energy and health** against the thresholds below, with numbers, not vague phrasing.
- **Backlog:** overdue count, important and time-sensitive count, and one to three parked items that now fit, if any.
- **Communication debt:** email past the response window, stale ownerless items in the action queue, direct messages waiting over three days. Non-zero queues are normal; stale ones are the problem.
- **External and team commitments** the user owns this week or next, which usually beat self-set goals on timing.
- **People load**, only from what the user has shared or from team records they own: a colleague the user has said is overloaded, or several recent joiners. Ask whether supporting them is the real priority.
- **Non-negotiables status** against the current plan, with specific misses.

### Signal thresholds (adjustable defaults)

| Signal | Flag when | Notes |
|---|---|---|
| Sleep | Any night under 6.5 hours asleep, three or more nights under 7, or the recovery metric under 90 percent of the prior week | Use time asleep, not time in bed. Compare metrics only within one device. Ask the user's own target. |
| Energy | Two or more clearly negative days in seven, a run of neutral days if the user uses neutral as a soft negative, or focused work under about 3 hours a day | Ask how the user uses their rating scale. Treat as a hypothesis to test. |
| Goal slippage | Deadline moved four or more times and still open | Ask whether the goal itself is wrong |
| Task deferral | Deferred more than five times | Candidate to park |
| Messages | Email past the response window; direct messages waiting over three days | Behind-ness signal, not failure |

After crossing several time zones, short nights mean the body clock is adjusting, not poor discipline. Frame mitigation as resetting the clock (morning light, morning exercise, steady wake time).

### The alignment ledger

End the brief with this working model:

```markdown
**Confirmed:** <choices the user has made here or in current plans>
**Source facts:** <current constraints and evidence>
**Inferred:** <your tentative reading, labelled as such>
**Open:** <decisions only the user can make>
**Corrected:** <assumptions the user rejected; omit if empty>
```

## Step 3: Rolled-over goals

1. **Find the real source.** If last week's goals were written in the plan note rather than as separate records, use that section.
2. **Check delegation.** If an unfinished goal now belongs to someone else, note the handoff and move on.
3. **Check whether it shipped.** Open statuses are often stale. If daily plans or the review show it finished, propose marking it done.
4. **Decide one goal at a time.** Never batch.

| Decision | Action |
|---|---|
| Roll over | Candidate goal for Step 4. Ask "why did this slip?" and log one line. Increment the deadline-moved counter and set the new deadline. |
| Demote | Not a weekly goal; list it as an intention. |
| Drop | Mark archived or missed. |

## Step 4: Shape the week

### Check for a plan of record first

The user may already have written an ordered action list after a planning event, or shortlisted goals with their team. Ask: "Is there a written plan of record anywhere?" A plan of record outranks inference. Treat team-agreed goals as decided; only check that each has a verifiable definition of done and fits the week.

### Question format

Ask four to eight questions per round. Number every question. When choices are bounded, letter the options and put your recommendation first. One question normally holds one decision.

```markdown
1. Which outcome would make this week worth it?
   a) <recommended option> (recommended: <one-line reason>)
   b) <option>
   c) Something else
2. What are you willing to let slip for it?
```

### Round 1: brain dump, then desired change

Ask for a quick, unfiltered list of everything the user might work on. Group it by goal or project and show it back in a few lines, so the chosen goal is not simply the first idea. Note small items for triage; do not do them now. Then work backwards:

- What outcome would make the week genuinely matter?
- Why does it matter now, beyond having a deadline?
- What has changed since last week's plan?
- Which area (work, health, relationships, personal) most needs attention?
- What is emotionally or strategically unresolved?
- What would you regret neglecting even if the visible work shipped?

Do not answer these from source material. Evidence can prompt a question; it cannot say what the user values. Classify each answer as confirming, rejecting, softening, qualifying, or deferring your model, and show the updated ledger.

### Round 2: shortlist

Apply the prompts that bite this week:

- What can you do best, and what could someone else do as well?
- What would most move the team's main goal or the relevant higher-level goal?
- What would benefit most from lead time?
- What unfinished work will steal attention if not closed now?
- What is the strongest case for not doing this?
- Which fires are you willing to let burn?

Also settle real capacity given meetings, energy, and health, and which commitments depend on others. Everything not shortlisted goes to "Not this week" or a "Later" list.

### Round 3 when needed

Run another round if an important choice about sequencing, success criteria, ownership, or week shape is still open. Fatigue is a reason to narrow options, not permission to revive an earlier inference.

### Readiness gate

Propose goals only when each item is confirmed, established, or deliberately left open:

- The one change that would make the week worthwhile.
- Why it matters now.
- The higher-level goal it serves.
- Two to four verifiable outputs.
- The main competing claim on time.
- What the user is explicitly not advancing.
- The realistic health and energy floor.
- The most likely failure mode.

For each candidate, ask yourself: did the user call this important, or am I promoting a visible deadline? If the latter, ask another question.

### Propose and validate

Propose the smallest set of goals that fits the alignment, usually one or two. Explain each in one sentence. For each:

- **Serves a higher-level goal?** Name it and record it in the goal notes.
- **Verifiable?** Narrow any direction into a named set and named outputs.
- **Scoped?** Sketch sub-tasks with rough hours and sum them against free time after meetings, minus the buffer. Under an hour of work is a task, not a goal.
- **Realistic?** A heavy calendar plus a low-energy signal means cut one.

### Shaping checks

- **Recurring overload means one goal.** If the current plan's cut-scope rule keeps firing, the answer is usually a single goal executed well. Use the current rule only; never import an expired one. Ask what has changed before accepting more scope.
- **People-heavy weeks.** If meetings, interviews, logistics, or supporting others dominate, ask whether this is a people week or whether to cut enough to protect one deep goal. "Defend harder" usually fails. Ring-fence any deep item on the cleanest day.
- **External deadlines first.** With two or more goals, ask which has the harder external deadline. That one ships first, whatever feels heavier.
- **Team goals need a team target.** If a goal needs others, ask what the team should achieve by week's end and where it will be announced. Offer two or three framings with a recommendation, and draft the announcement for the user to send.
- **Soft stop.** If after two or three rounds of pushback the user says "just write it down", accept the plan. Record your concern in the failure-mode line instead of arguing.

## Step 5: Non-negotiables

1. **Check the current higher-level plan.** If it lists non-negotiables, ask whether they still fit. If the user corrects one, update the higher-level plan too, after approval.
2. **Score the current scorecard** if one exists, using its own items, lookback, and threshold. If none exists, say so once and ask what minimum health, relationship, and recovery floor the user wants.
3. **Honour explicit pauses.** Drop habits the user has paused or retired. Ask at most once per session whether they are back.
4. **Verify protected days are free.** Check for events or travel on any rest or focus day, and agree a move or an accepted slip.
5. **Push for concrete mitigations** when something is faltering. Ask up to three follow-ups until the user names an action and a day or time.
   - Good: "Phone out of the bedroom from Tuesday, with a wind-down alarm an hour before my usual bedtime."
   - Not enough: "I'll try to sleep more."

For sleep in particular: lead with the numbers and nights; respect the user's stable sleep window and cap any proposed bedtime shift at about 30 minutes, since bigger shifts usually fail; require both a bedtime and a wind-down trigger; and if the same problem appeared last week, ask what is actually different this time. Record commitments verbatim so the next session can compare.

## Step 6: Cut the calendar

First ask: "Do you want to cut meetings this week, or keep them all?" If keep, note "No cuts this week (chose to keep)" and move on.

Otherwise, for each meeting, ask whether it serves a goal, a non-negotiable, or a team commitment. List those that do not. The user decides each: keep, cut, shorten, or reschedule. If someone else organises a recurring meeting, the change is a message to them, not a calendar edit. Print a short message for each change; the user picks the channel.

```text
Hi <name>, I'm protecting time this week for <goal> and need to <cancel / move / shorten> our <meeting> on <DD MMM>. Could we <async update / next week / shorter slot> instead? Thanks for understanding.
```

## Step 7: Task triage

Ask first whether the user wants to triage alone. If so, note it and skip the writes. If the user pauses to clear tasks or messages themselves, re-read live data when they return.

**First pass: chronic deferrals.** Show tasks deferred more than five times as one batch: "Move these N to parked?" Default to parked, not archived or deferred again. One yes or no, then update in a batch.

**Second pass: one by one,** sorted by importance, urgency, then age. Write each decision immediately.

| Decision | Action |
|---|---|
| Do this week | Keep open with a due date in the target week; candidate for a block |
| Done | Mark done; finished tasks are often left open |
| Defer | Set a future date and increment the deferral counter |
| Delegate | The user names the owner; note "Delegated to <name> on <date>" |
| Delete | Archive |

Do not park tasks the user calls important; give them dated slots. Before proposing delegation, check whether the task can only be done by the user.

## Step 8: Pre-mortem and deprioritise

Do this before calendar blocking, so the answers shape which blocks need the most protection.

- **Pre-mortem:** "If this week fails, what is the most likely reason?" Record one to three lines.
- **Deprioritise:** "What can you delete, delegate, reschedule, or reset expectations on? What in-flight work will you explicitly not push this week?" Pausing one stream often helps others ship.

## Step 9: Break goals into tasks

For each goal, create one to five tasks of 5 minutes to 3 hours that together complete it. Also add tasks for "do this week" triage items, delegation follow-ups, and meeting prep. If a pending decision could reshape a goal, create only tasks that survive either outcome.

**Do the work before proposing.** Gather the links and context the user will need. Draft what you can: outlines, email drafts, review lists, or decision options with tradeoffs.

For four or more tasks, show a compact table first:

| # | Task | Due | Minutes | Owner |
|---|---|---|---|---|
| [1] | [Verb-first title] | [DD MMM] | [estimate] | [user or role] |

**Per-task flow:**

1. **Check for duplicates** among open and parked tasks using two or three distinctive title words. If it is the same work, update that record in place.
2. **Propose** the title, notes, and fields.
3. **The user approves, edits, or rejects.** Rejected means dropped.
4. **Create or update** one at a time and keep the reference for blocking.

**Defaults:** importance follows the goal; urgency is time-sensitive only if it must land this week; spread due dates across the week; use realistic estimates (5, 15, 30, 60, 90, 120, 180 minutes); match the style of existing task titles.

```markdown
Serves weekly goal: <goal>. Ladders to: <higher-level goal>.

**Done when:** <one-sentence binary criterion>

**Checklist:**
[] <first concrete action>
[] <next action>

**Refs:**
- <anchor document or thread>

<optional: draft, outline, or options>
```

Use whatever checkbox syntax the user's system renders. Avoid single tasks that restate a multi-day goal, more than five tasks per goal (that is a project; say so), and task records for routines like exercise, which belong in the plan and calendar.

## Step 10: Calendar blocking

**Show the week as day-by-day paragraphs first,** one short paragraph per day, with open questions at the end. Use tables only after the shape is agreed.

**Check the buffer.** If proposed blocks exceed the agreed share of free hours, cut or shrink a goal rather than squeezing.

**Block:** every task of 45 minutes or more, every task with a hard deadline, and every timed non-negotiable such as training or recovery. If a training plan prescribes sessions, give each a specific slot; the key session wins if only one fits. Count evening work as capacity only if the user really works evenings, and pair late work with a stated stop time when sleep is shaky.

**Propose a message-processing block** of one to two hours whenever communication debt crossed a threshold.

**Size check.** If a block is shorter than its task estimate, flag it and offer a longer block, a split, or a smaller task.

**Reuse the user's placeholders.** Rename generic focus blocks the user already created rather than duplicating them, but split any block that spans meals or meetings into precise work slots.

Ask "What else am I missing?" before creating anything.

**Per-slot flow:**

1. Re-read the live calendar just before writing. Treat changes the user made during the session as a diff and fold them in.
2. Propose one slot: "Draft two - Sat <start>-<end> (3h). OK?"
3. On approval, create it in the confirmed time zone, using the user's focus-block style for solo work and normal events for meetings, calls, and exercise.
4. If rejected, offer the next best slot.

## Step 11: Write the simple plan

**Goal records.** Check goals already linked to the week. Update matching ones in place instead of creating near-duplicates. When linking new goals, add to existing links; never replace them.

**Plan note.** This is the canonical summary, not an audit log. Tasks hold checklists; the calendar holds times. Keep it to one screen and omit empty headings.

```markdown
## Theme
<theme from the higher-level plan, or 2-5 words>

## Weekly goals
[] <Goal 1> - ladders to <higher-level goal>
    Done when: <2-4 checkable outputs>

## Protect
- <health, relationship, or recovery floor with concrete slots>

## Week shape
- <day>: <the one essential focus or constraint>

## Not this week
- <explicitly deprioritised work>

## Failure mode
- <most likely failure> -> <specific counter>
```

Use at most two goals unless the user chose a third, marked stretch.

## Step 12: Close

Give operational counts in one sentence: goals committed, tasks created or updated, blocks booked, meetings cut, tasks triaged. Show the current scorecard's success bar briefly if one exists. End with the final plan on one screen, then one closing sentence. Do not recap research, questions, or tool mechanics.

## Step 13: Improve the workflow

At the end, note what to change next time: what wasted effort, which assumption proved wrong, what the user corrected, and which step fired pointlessly. Make precise edits to the user's stored instructions for this workflow and show a two- or three-bullet summary. Make small fixes directly if allowed; ask before adding or removing steps. If nothing needs changing, say so.

## Hiring audit template

Use this for a short, delegated check when the user hires. Keep candidate data to names, stages, and dates needed for scheduling, and keep it inside the user's planning space.

```text
Audit hiring load for <Mon DD MMM> to <Sun DD MMM>. Under 250 words, names and numbers only, about 3 minutes. If a call fails twice, skip it and note the gap.
1. Confirmed interviews where the user is an interviewer (exclude unscheduled placeholders): day, time, candidate, role, total hours.
2. Late-stage candidates whose next step depends on the user. Flag one as overdue only if a real current-stage entry date exceeds the response target; never use the application creation date. Otherwise report counts per stage and say stage age was not checked.
```

If decisions are overdue or interviews exceed about three hours, name the cost of delay and ask who owns the response. In planning discussions, focus on role-relevant decisions: whether each assessment still distinguishes relevant performance, who is waiting on a decision, and how much interviewer time the week holds.

## Style

- Be direct and terse. Say "this is likely to fail because X" when you believe it.
- Be firm when needed: "That's four goals; pick three." "What's actually different from three weeks ago?"
- Skip end-of-step celebrations. Use one date format, such as `DD MMM`.
- If no higher-level plan exists, ask whether to continue without one or pause for a monthly review. Do not invent a stand-in.

## Common failure modes

| Failure | Counter |
|---|---|
| Promoting the most visible deadline into the goal | Readiness gate; ask what the user wants to make true |
| Planning deep work inside a meeting-heavy week | People-heavy week check; ring-fence one clean day |
| Rolling the same goal over repeatedly | Show the slip count in the brief; ask if the goal is wrong |
| A hidden external commitment appears late | Scan for plans of record and dated commitments early; ask what is missing |
| Treating sync gaps as real behaviour | Report gaps and confirm |
| Stale calendar at write time | Re-read right before creating events |
| Duplicate goals or tasks | Check existing records and update in place |
| Overwhelming proposals | Day-by-day paragraphs, compact tables, one decision per question |
| Arguing past the user's decision | Soft stop; record the concern as the failure mode |
| Reviving paused habits or expired rules | Use only the current plan; honour pauses |
| Reading more personal data than needed | Authorised sources, structured fields first, minimum detail about others |

---
name: wind-down-for-sleep
description: A quiet, repeatable bedtime workflow that lowers stimulation, puts distractions out of reach, prepares the body, and gives a short reply when sleep does not come.
---

# Wind down for sleep

This is an interactive evening workflow. It moves the user from the awake part of the day to sleep. It does three things only: it lowers stimulation, adds reliability, and prepares the body. It does not handle reflection or planning. Those belong to an earlier day-review practice and an earlier next-day planning practice.

Recommended evening order: **day review, then next-day planning, then wind-down.** This workflow comes last.

Target length for the active ritual: about 20 to 30 minutes. Longer rituals tend to get skipped.

## Settings the user chooses

Agree on these once. Reuse them every night until the user changes them. Offer the starting points only as suggestions, and do not assume values the user has not chosen.

| Setting | What to decide | Suggested starting point |
|---|---|---|
| Target sleep time | When the user wants to be asleep | Based on their natural sleep window and wake time |
| Ritual start | When wind-down usually begins | 60 to 90 minutes before target sleep time |
| Review cutoff | The point after which a missed review is skipped | When doing a review would push sleep back |
| Distraction barrier | How the phone or other distracting device goes out of reach | A physical timed box or a charger in another room |
| Default access time | When the device becomes available again | After the first part of the morning routine |
| Early-commitment rule | How far access moves earlier for an early fixed commitment | First commitment minus the time needed to get ready and travel |
| Gate items | The few changes that signal night | A clothing change plus the distraction barrier |
| Allowed device | The one low-stimulation device, if any, used after the gate | None, or one device used only for this workflow |
| Physical prep tasks | Small tasks that set up the morning | Fill water, brush teeth, set out breakfast |
| Settling practice | A short familiar practice | A few minutes of meditation or slow breathing |
| Capture spot | Where stray tasks go for tomorrow | A notes field on tomorrow's record, or paper |

If the user names an earlier bedtime for tonight, work backwards from it. Protect time for physical prep and the settling practice. Do not let planning expand into the remaining window.

## Purpose (re-read every run)

Common failure modes this workflow targets:

- Too much stimulation late in the evening, which leads to scrolling or lying awake.
- Worry about tomorrow. The earlier review (a worry offload) and specific planning mostly handle this.
- An inconsistent routine that gives the body no signal that the day is ending.
- Distraction controls that are easy to bypass. Software limits on the same device are often weak. Physical barriers and blocking tools on separate devices are usually more reliable.

Success signal: the user wakes rested, starts the morning routine without scrolling, and the device stays out of reach until the chosen access time.

Every step must do at least one of these: (a) reduce stimulation, (b) add reliability, or (c) prepare the body. If a step does none of these, remove it during the audit.

Design anchors. Use them to shape the routine, but never explain them at bedtime:

- Writing a specific to-do list before bed has been linked to falling asleep faster. Specificity matters, so planning happens before this workflow, not inside it.
- Scheduled worry time earlier in the evening reduces bedtime anxiety. The review owns the worry offload.
- Dim, warm light late in the evening and little screen light support sleep onset.
- Consistency matters more than contents. Use the same sequence every night.

## Triggers

- **Full ritual:** "wind down", "ready for bed", "going to bed", "time for bed", "help me get to sleep", or similar.
- **Can't-sleep fallback only:** "can't sleep", "still up", "still awake", or similar, after the ritual already ran tonight. Skip every other step and go straight to Step 6.

## Hard rules

- **Gate first.** Do not continue past Step 1 until the user confirms it.
- **Keep the gate minimal.** Include only the gate items the user chose. If the user removes an item, do not add it back later.
- **No distracting-device step after Step 1.** Everything afterward must work offline or with the one allowed device.
- **Never ask about tomorrow.** No outcomes, intentions, wins, or backup one-line plan. If planning was skipped, note it silently and continue. Planning questions raise alertness at the moment the goal is to lower it.
- **Do not reopen reflection or planning.** Do not open a second writing session. Any journal writing belongs to the review, before its questions.
- **Deflect tomorrow-concerns.** Say: "Put a short note in your capture spot. The review will handle it tomorrow. Not tonight."
- **No summary at the end.** Send the close and stop.
- **Stay silent after the close.** If the user says good night, reply with nothing or only "Good night." Never send a follow-up, a placeholder, or a simulated user turn. An unexpected message after bedtime can wake someone up.

## Privacy and data handling

This workflow may touch a personal journal, day records, and calendars. Use only sources the user has explicitly authorized, and only for this purpose.

- **Check status, not content.** Confirm the review finished from a completion signal, such as a rating field or a done marker. Never read, quote, or reconstruct private journal text. An autosaved freeform entry alone does not mean the review finished.
- **Read only what you write to.** When capturing a late task, read only the capture field on tomorrow's record, then append.
- **Calendars are read-only.** Only the tomorrow-morning window is needed.
- **Keep it inside the session.** Do not share or summarize what you saw.

## Step 0: Readiness check

Gather only what is needed to confirm the earlier practices ran and to set the access time. Do not open inboxes, news, or feeds.

If the review and planning ran earlier in the same session, skip all lookups. That state and tomorrow's calendar are already known. Check the current time and continue.

If this workflow runs on its own, gather the following in one batch:

1. Current time, today's date, and tomorrow's date.
2. Whether today's review is complete.
3. Whether tomorrow's plan exists.
4. Tomorrow's first fixed commitment before midday, from every calendar the user approved. Include personal as well as work calendars, since social plans and early activities move the access time too.

Lookup principles:

- **Test presence, not truthiness.** A zero rating is a valid, completed rating.
- **Match dates loosely** and expect more than one record per day. Check each matching record instead of assuming a single one.
- **Degrade quietly.** If a source fails, say so once, compute from what you have plus anything the user mentioned, and leave repair for daytime.

| Review complete? | Time | Action |
|---|---|---|
| Yes | Any | Say "Day reviewed. Starting wind-down." Go to Step 1. |
| No | Before review cutoff | Say "The day review didn't run. Do it now (about 10 minutes)?" If yes, run it and return. If no, mark review skipped and go to Step 1. |
| No | At or after cutoff | Say "Too late to review tonight. We'll pick it up tomorrow." Mark review skipped. Go to Step 1. |

If tomorrow's plan is missing, do not mention it, offer planning, or ask a fallback question.

## Checklist format (Steps 1 and 2)

Use plain bullet lists, not checkboxes. Many interfaces cannot tick boxes, and "tick each one" wording confuses people. Send the whole list in one message and end with "Reply 'done' when all set." Expect one reply. Do not send items one at a time, because that adds turns at bedtime.

## Step 1: Environment and distraction gate

Set the access time:

- Default: the user's chosen access time.
- If tomorrow's first commitment is early enough that the default leaves too little time to get ready and travel, apply the user's early-commitment rule.
- State the time. If it is earlier than usual, give the reason in a few words. If the barrier has a timer, show the duration from now.

```
Before we start:
- [Clothing change, e.g. day clothes off, sleep clothes on]
- [Distraction barrier], timer [duration] (access at [time][, reason if earlier, e.g. travel for an early meeting])

Reply "done" when all set.
```

If the user delays an item ("I'll do it in a sec"), say once: "Do it now. These are the biggest levers. I'll wait." Then wait.

## Step 2: Physical prep (about 5 minutes)

List the user's chosen tasks, grouped by location so they move around less.

```
- [Kitchen task, e.g. fill water bottle for the morning]
- [Bathroom task, e.g. brush teeth]
- [Kitchen task, e.g. set out breakfast in the fridge]

Reply "done" when all set.
```

If a small task surfaces ("out of yoghurt, need to buy tomorrow"), do not solve it. Capture one line so it leaves the user's head:

- Append to tomorrow's capture spot, reading only that field. Preserve existing text exactly. Never overwrite from an earlier cached value.
- Never write into the private journal, and never create a partial review record.
- Then say: "Noted. Captured."

## Step 3: Settling practice

One line naming the practice, for example: "5 min meditation." Give no instructions if the user already knows the practice. Never introduce something new at bedtime. Wait for "done" or similar. Add, remove, or restore this step whenever the user asks.

## Step 4: Close

Say only, adapted to the user's setup:

> [Device] closed. Straight to bed, no detour.
>
> See you tomorrow.

No recap and no "sweet dreams". This is the last message tonight. Move silently to the audit.

## Step 5: Routine audit (silent)

After the close, review the run without sending anything. Do not ask a tired person to diagnose their own ritual. If the user approved direct edits, update the routine. Otherwise, save proposed changes for daytime review. Do not report what changed.

| Signal | Change |
|---|---|
| User misread a prompt or asked what it meant | Rewrite it in plainer words |
| User pushed back on a step | Simplify it, make it optional, or cut it |
| A lookup failed or found the wrong record | Fix the lookup rule |
| An item is skipped without comment | Remove it |
| User stated a preference ("don't ask me X") | Add it as a hard rule |
| The barrier keeps being bypassed | Choose a stronger physical barrier with the user |
| The same worry keeps appearing at bedtime | Move its prevention into the earlier review or planning |

If the run was clean, change nothing. Do not invent improvements. If the user re-engages because they cannot sleep, go to Step 6.

## Step 6: Can't-sleep fallback (stimulus control)

Use only when the user reports being awake after the ritual. Do not rerun the ritual or reopen planning. Say:

> Out of bed. Dim room, something boring (paper reading, nothing on a screen, no problem-solving), about 20 minutes. Back to bed when sleepy. Don't check the time.

This keeps the bed linked with sleep rather than with lying awake. Do not extend the reply. If sleep trouble is frequent or severe, suggest professional support at a daytime moment, not at night.

## Exhaustion rule

If the user is clearly exhausted, they may skip Step 2 or Step 3. Do not skip Step 1, because it is the load-bearing step, unless a health, safety, accessibility, or caregiving need makes it unsuitable.

## Style

- Quiet and short. One question at a time. No preamble.
- No narration ("great, now let's...") and no emojis.
- No sleep science at runtime.
- If the user goes off-script with a work problem, deflect to the capture spot and tomorrow's review.
- Use the user's preferred date and time format.

The best wind-down is quiet, repeatable, and boring enough to become an automatic signal that the day is over.

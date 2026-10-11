---
name: wind-down-for-sleep
description: A quiet, repeatable bedtime workflow that lowers stimulation, secures distractions, prepares the morning offline, and gives a short stimulus-control reply when sleep does not come.
---

# Wind down for sleep

This is an interactive evening workflow. It moves the user from the awake part of the day to sleep. It lowers stimulation, puts distractions out of reach, finishes a few practical tasks, and then ends the conversation. It does not handle reflection or planning. Those belong to an earlier day-review practice and an earlier next-day planning practice.

Recommended evening order: **day review, then next-day planning, then wind-down.** This workflow comes last.

Keep the active ritual short. Most people do well with 15 to 30 minutes. Longer rituals tend to get skipped.

## Settings the user chooses

Agree on these once. Reuse them every night until the user changes them. Do not assume values the user has not chosen. Offer the starting points below only as suggestions.

| Setting | What to decide | Suggested starting point |
|---|---|---|
| Target sleep time | When the user wants to be asleep | Based on their natural sleep window and wake time |
| Ritual start | When wind-down begins | 45 to 90 minutes before target sleep time |
| Review cutoff | The point after which a missed review is skipped | When doing a review would push sleep back |
| Distraction barrier | How the phone or other distracting device is put out of reach | A physical barrier, such as a timed box or a charger in another room |
| Morning access time | When the device becomes available again | After the first part of the morning routine is done |
| Early-commitment rule | How much earlier access moves for an early fixed commitment | Enough time to get ready and travel |
| Environment cues | The light, sound, and clothing changes that signal night | Overhead lights off, dim warm light, sleep clothes |
| Allowed device | The one low-stimulation device, if any, used after the gate | None, or one device used only for this workflow |
| Settling practice | A short familiar practice | A few minutes of meditation, slow breathing, or stretching |
| Capture location | Where stray worries or tasks get written down | A notes field or paper notepad for tomorrow |

If the user names an earlier bedtime for tonight, work backwards from it. Protect the time for physical preparation and the settling practice. Do not let earlier planning spill into this window.

## Why each step exists

Common failure modes this workflow targets:

- Too much stimulation late in the evening, which leads to scrolling or lying awake.
- Worry about tomorrow. The earlier review (a worry offload) and planning (a specific next-day list) mostly handle this.
- An inconsistent routine that gives the body no clear signal that the day is ending.
- Distraction controls that are easy to bypass. Software limits on the same device are often weak. Physical distance or a physical barrier is usually more reliable.

Success signal: the user wakes rested, starts the morning routine without scrolling, and the device stays out of reach until the chosen access time.

Every step must do at least one of these: (a) reduce stimulation, (b) add reliability, or (c) prepare the body or the morning. If a step does none of these, remove it during the audit.

Design anchors. Use these to shape the routine, but do not explain them at bedtime:

- Writing a specific to-do list before bed has been linked to falling asleep faster. Specificity matters, so planning happens before this workflow, not inside it.
- Scheduled worry time earlier in the evening reduces bedtime anxiety. The review owns the worry offload.
- Dim, warm light late in the evening, with bright overhead light off and little screen light, supports sleep onset. That is why the environment check is a gate.
- Consistency matters more than contents. Use the same sequence every night.

## Triggers

- **Full ritual:** "wind down", "ready for bed", "going to bed", "help me get to sleep", or similar.
- **Can't-sleep fallback only:** "can't sleep", "still awake", or similar, after the ritual already ran tonight. Skip every other step.

## Hard rules

- **Environment gate first.** Do not continue past Step 1 until the user confirms it. Do not negotiate it.
- **No distracting-device step after Step 1.** Everything afterward must work offline or with the one allowed device.
- **Never ask about tomorrow.** No priorities, intentions, wins, or backup one-line plan. If planning was skipped, note it silently and continue. Planning questions raise alertness at the moment the goal is to lower it.
- **Do not reopen reflection or planning.** Do not start a new writing session.
- **Deflect worries and tasks.** Say: "Put a short note in your capture spot. The review will handle it tomorrow. Not tonight."
- **No summary at the end.** Send the close message and stop.
- **Stay silent after the close.** If the user says good night, reply with nothing or only "Good night." Never send a follow-up, a placeholder, or a simulated user turn. An unexpected message after bedtime can wake someone up.

## Step 0: Readiness check

Gather only what is needed to confirm the earlier practices ran and to set the morning access time. Do not open messages, inboxes, news, or feeds.

If the review and planning ran earlier in the same session, skip all lookups. That information is already known. Check the current time and continue.

If this workflow runs on its own, gather the following in one batch, using only sources the user has authorized:

1. Current time and tomorrow's date.
2. Whether today's review is complete.
3. Whether tomorrow's plan exists.
4. The first fixed commitment tomorrow morning, from each calendar the user has approved. Read-only.

Data-handling principles:

- **Check status, not content.** Confirm the review is finished from a completion signal, such as a rating or a done marker. Do not read the text of private journal entries. A freeform note saved on its own does not mean the review is finished.
- **Read records carefully.** Treat a valid low value as present, not missing. Allow for loose date matching and more than one record per day.
- **Degrade quietly.** If a source is unavailable, say so once, proceed with what you have, and leave any repair until daytime.

| Review complete? | Time | Action |
|---|---|---|
| Yes | Any | Say "Day reviewed. Starting wind-down." Go to Step 1. |
| No | Before review cutoff | Say "The day review didn't run. Do it now (about 10 minutes)?" If yes, run it and return. If no, mark the review as skipped and go to Step 1. |
| No | At or after review cutoff | Say "Too late to review tonight. We'll pick it up tomorrow." Mark the review as skipped. Go to Step 1. |

If tomorrow's plan is missing, do not mention it and do not offer planning.

## Checklist format (Steps 1 and 3)

Use plain bullet lists, not checkboxes. Many interfaces cannot tick boxes, and "tick each one" wording confuses people. Send the whole list in one message. End with "Reply 'done' when all set." Expect one reply. Do not send items one at a time, because that adds turns at bedtime.

## Step 1: Environment and distraction gate

Set the morning access time:

- Default: the user's chosen access time.
- If tomorrow's first fixed commitment would not leave enough time to get ready and travel, move access earlier using the user's early-commitment rule.
- State the time. If it is earlier than usual, give the reason in a few words. If the barrier uses a timer, show the duration from now.

Template, filled with the user's chosen cues:

```
Before we start:
- [Clothing change, e.g. day clothes off, sleep clothes on]
- [Light change, e.g. overhead lights off, dim warm light on]
- [Optional sound cue, e.g. quiet sleep audio]
- [Distraction barrier], access at [time][, reason if earlier]
- [Allowed device, if any] is the only screen from here

Reply "done" when all set.
```

If the user delays an item ("I'll do the lights in a minute"), say once: "Do it now. This is the biggest lever. I'll wait." Then wait.

## Step 2: Offline morning card (optional, about 3 minutes)

A short handwritten card lets the morning start without the phone. Build the template from the user's real routine once, then reuse it. Example prompt:

> Write your morning card. Template:
> 1. [Hygiene]
> 2. [Medication, if any]
> 3. [Water or breakfast]
> 4. [Movement or health practice]
> 5. [Get ready]
> 6. [Leave or start the first block]
>
> Anything different tomorrow?

Keep it short enough to read at a glance. If the user names a change, say "Write it where it fits." Then ask: "Card done?" Do not write the card for them digitally. The physical act is the commitment. Skip this step if the user already has a reliable offline morning cue.

## Step 3: Physical preparation (about 5 minutes)

List the user's chosen tasks, grouped by location so they move around less. Example:

```
- [Kitchen task, e.g. fill water for the morning, set out breakfast]
- [Bathroom task, e.g. brush teeth, nighttime hygiene]
- [Door task, e.g. lay out clothes, keys, medication]

Reply "done" when all set.
```

If a small task or worry comes up, such as a missing grocery item, do not solve it. Capture one line so it leaves the user's head:

- Write to the user's capture location for tomorrow. If the review was skipped or is incomplete, never create a partial review record. Use the next-day capture spot instead.
- Add to what is already there. Never overwrite or rewrite existing text.

Then say: "Noted. Captured."

## Step 4: Settling practice

One line naming the user's chosen practice, for example: "Five minutes of quiet breathing." Give no instructions unless asked, and never introduce a new or complex practice at bedtime. Wait for "done" or similar. Add, remove, or swap this step whenever the user asks.

## Step 5: Close

Say only, adapted to the user's setup:

> [Device] closed. Straight to bed, no detour.
>
> See you tomorrow.

No recap and no extra pleasantries. This is the last message tonight.

## Can't-sleep fallback (stimulus control)

Use only when the user reports being awake after the ritual. Do not rerun the ritual or reopen planning. Say:

> Out of bed. Dim room, something boring (paper reading, nothing on a screen, no problem-solving), about 20 minutes. Back to bed when sleepy. Don't check the time.

This keeps the bed linked with sleep rather than with lying awake. Do not extend the reply. If sleep trouble is frequent or severe, suggest professional sleep support at a daytime moment, not at night.

## Exhaustion rule

If the user is clearly exhausted, they may skip Step 2, Step 3, or Step 4. Do not skip Step 1 unless a health, safety, accessibility, or caregiving need makes it unsuitable.

## Routine audit

After the close, review the run without sending anything to the user. Do not ask a tired person to diagnose their own routine. If the user has approved direct edits, update the routine. Otherwise, save proposed changes for them to review later.

| Signal | Change |
|---|---|
| User misread a prompt or asked what it meant | Rewrite it in plainer words |
| User pushed back on a step | Simplify it, make it optional, or cut it |
| A lookup failed or returned the wrong record | Fix the lookup rule |
| An item is skipped without comment night after night | Remove it |
| User stated a preference ("don't ask me X") | Add it as a hard rule |
| The distraction barrier keeps being bypassed | Choose a stronger physical barrier with the user |
| The same problem keeps appearing at bedtime | Move its prevention into the earlier review or planning |

If the run was clean, change nothing. Do not invent improvements.

## Style

- Quiet and short. One question at a time. No preamble.
- No narration ("great, now let's..."), no emojis.
- No sleep science at runtime.
- Use the date and time format the user prefers.

The best wind-down is quiet, repeatable, and boring enough to become an automatic signal that the day is over.

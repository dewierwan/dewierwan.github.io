---
name: wind-down-for-sleep
description: A quiet bedtime routine that lowers stimulation, puts distractions out of reach, prepares the morning offline, and gives a short stimulus-control reply when sleep does not come.
---

# Wind down for sleep

This is an interactive, low-stimulation routine that moves the user from the awake day to sleep. It covers the environment, distraction control, a few practical preparations, and a short settling practice. It does not review the day or plan tomorrow. Those belong to separate practices that should happen earlier in the evening.

Recommended evening order: **day review, then next-day planning, then wind-down.** This routine comes last. Keep the active part short, roughly 15 to 30 minutes, so it does not become another task to avoid.

## Setup choices (agree once, then reuse)

Before first use, ask the user to choose the following. Save the answers wherever the user keeps preferences. Suggested defaults are only starting points.

| Choice | What the user decides | Broadly useful default |
|---|---|---|
| Target sleep time | When they want to be asleep, based on their natural sleep window | Start the routine 45 to 90 minutes before it |
| Tonight's override | An earlier in-bed time for one night | Work backwards from the stated time |
| Distraction barrier | How the phone and other tempting devices go out of reach | A physical barrier, such as a timed box or a charger in another room |
| Device return time | When the phone becomes available in the morning | Shortly after the morning routine is done |
| Early-commitment buffer | How much time is needed before an early commitment | Enough for getting ready and travel |
| Environment cues | Light, clothing, sound, or other signals that the day is over | Overhead lights off, dim warm light, quiet familiar audio |
| Morning card | Whether to use a paper card, and what goes on it | A short list of the first few morning actions |
| Prep list | Practical tasks to finish before bed | Water, hygiene, and items needed in the morning |
| Settling practice | One familiar, calm practice | A few minutes of quiet breathing or meditation |
| Record access | Which records, if any, the assistant may check | None; rely on the current conversation |

## Purpose

Common reasons wind-downs fail:

- The user is too stimulated late in the evening, which leads to scrolling or lying awake.
- The user ruminates about tomorrow. An earlier review that offloads worries and a specific plan help with this.
- The routine is inconsistent, so the body gets no clear signal that the day is ending.
- Device limits are easy to bypass in the moment.

Success looks like this: the user wakes rested, starts the morning from the paper card or another offline cue, and the phone stayed out of reach until the chosen return time.

Every step must do at least one of these: **(a) reduce stimulation, (b) add reliability, or (c) prepare the body and morning.** If a step does none of these, remove it during the audit.

## Design principles (shape the routine, never lecture them)

- **Specific planning belongs before bed, not during wind-down.** Writing a concrete plan earlier tends to reduce bedtime worry. Planning during wind-down re-stimulates.
- **Worry belongs earlier.** Scheduled worry time earlier in the evening, a technique from cognitive behavioral therapy for insomnia, lowers anxiety at sleep onset.
- **Light matters.** Dim, warm light in the late evening and less screen light support sleepiness. That is why the environment step comes first and gates everything else.
- **Consistency beats contents.** Running a similar sequence most nights matters more than the exact items in it.
- **Physical barriers beat willpower.** A barrier that takes effort to undo works better than a setting that can be switched off in seconds.

## Triggers

- **Full routine:** "wind down," "ready for bed," "going to bed," "help me get to sleep," or similar.
- **Fallback only:** "can't sleep," "still awake," or similar after the user has tried to sleep. Go straight to the Can't-sleep fallback. Do not restart the routine.

## Hard rules

- **Gate first.** Do not continue past Step 1 until the user confirms it. If a safety, health, accessibility, or caregiving need makes part of the gate unsuitable, adapt that item with the user instead of dropping the gate.
- **Nothing phone-dependent after Step 1.** Later steps must work offline or on one remaining low-stimulation device.
- **Never ask about tomorrow.** No questions about priorities, intentions, outcomes, or wins, and no backup planning question if planning was skipped.
- **Do not reopen reflection or planning.** If the user raises a worry or task, say: "Put a brief note somewhere safe. It can wait until tomorrow."
- **Respect private writing.** Do not read, quote, or reconstruct a private journal. Check completion only through a dedicated status marker or the current conversation. A freeform entry with no completion marker does not mean the review is done.
- **No summary at the end.**
- **After the close message, stop completely.** If the user says good night, reply with nothing or only "Good night." Never create a pretend user turn or a follow-up message. An unexpected message after bedtime can wake the user.

## Step 0: Readiness check (minimal)

Gather only what is needed to check whether the earlier review happened and to set the device return time.

- **If review and planning just ran in the same conversation,** reuse what is already known. Get the current time and continue. Re-checking adds delay when the goal is to slow down.
- **If this routine runs on its own,** check, in one batch and only with the user's authorization: the current date and time, the review and plan completion markers in the user's chosen system, and the start time of tomorrow morning's first fixed commitment across the calendars the user has approved, including personal plans.

Data-access principles:

- Read the smallest fields that answer the question, such as a status marker or an event start time. Do not open event details, messages, feeds, or task lists.
- Match records tolerantly and check every match, because a day can have more than one record.
- Treat an empty but valid value, such as a rating of zero, as present.
- If a source is unavailable, mention it once in one line, use what is available plus anything the user has said, and leave fixing it for another time.

### Decision table

Use a `review_cutoff`: the latest time a short review still fits without delaying sleep. A reasonable default is the start of the user's normal wind-down window.

| Review done? | Time | Action |
|---|---|---|
| Yes | Any | Say "Day closed. Starting wind-down." Go to Step 1. |
| No | Before review_cutoff | Ask once: "The day review didn't happen. Do a short one now?" If yes, run it and return. If no, go to Step 1 and note that the review was skipped. |
| No | At or after review_cutoff | Say "Too late to review tonight. Pick it up tomorrow." Go to Step 1 and note that the review was skipped. |

If planning was missed, say nothing about it. Do not offer it.

## Checklist format (Steps 1 and 3)

Send each checklist as one message of plain bullets, ending with **"Reply 'done' when all set."** Do not use checkbox syntax or "tick each" wording, since many interfaces cannot tick boxes. Do not send items one at a time, because extra turns add stimulation.

## Step 1: Environment and device gate

Set the device return time. Use the user's default unless tomorrow's first commitment is too early for it. In that case, set it to the commitment time minus the user's buffer, and state the reason briefly. If the barrier uses a timer, give the countdown from now.

Template, filled with the user's own cues:

```
Before we start:
- [Change into sleep clothes]
- [Low-light cue, such as overhead lights off and dim warm light on]
- [Optional sound cue, such as quiet familiar audio]
- Phone in [barrier], returns [time]{, reason if earlier than usual}
- [One low-stimulation device] is the only screen from here

Reply "done" when all set.
```

If the user stalls ("I'll do it in a minute"), say once: "Do it now. This is the step that matters most. I'll wait." Then wait.

## Step 2: Offline morning card (optional, a few minutes)

If the user chose this, they handwrite a small card so the morning does not depend on the phone. The physical act is the commitment, so do not write it for them.

> Write your morning card from your usual list: [user's first few morning actions]. Anything different tomorrow?

If they name a change, say: "Add it where it fits." Then ask: "Card done?" Keep the card short enough to read at a glance. This is not planning; only practical exceptions belong here.

## Step 3: Physical preparation (a few minutes)

Send the user's prep list, grouped by location to reduce walking and decisions.

```
- [Task in one room]
- [Task in the same room]
- [Item to set out for the morning]

Reply "done" when all set.
```

If a small to-do comes up, do not solve it. Capture one short line in a designated next-day capture location the user has approved, adding to what is there and never overwriting it. Never write into a private journal. Then say: "Noted. Captured." If no capture location exists, tell the user to jot it on paper.

## Step 4: Settling practice (a few minutes)

Prompt in one line, for example: "Quiet breathing, a few minutes." Use the practice the user already knows; give no instructions and avoid screen-guided content. Wait for "done." If the user asks to drop or change this step, follow the request.

## Step 5: Close

Say only:

> Device closed. Straight to bed, no detour.
>
> See you tomorrow.

This is the final message tonight.

## Silent audit (after close, no user output)

If the workflow can be updated, review the run without messaging the user. Do not ask a tired user to diagnose the routine. Change only what the run showed:

| Signal | Adaptation |
|---|---|
| A prompt was misread or questioned | Rewrite it more plainly or remove it |
| A barrier was bypassed | Choose a stronger barrier with the user later |
| An item was skipped and added nothing | Remove it or make it optional |
| A data check failed or returned nothing | Fix the readiness instructions |
| The user said "don't do X" | Add it as a hard rule |
| The same practical issue keeps appearing at bedtime | Move its prevention into the earlier review or planning |

If the run was clean, change nothing and report nothing.

## Can't-sleep fallback

Do not rerun the routine or reopen reflection or planning. Reply briefly:

> Out of bed. Dim room, a boring screen-free activity, about 20 minutes. Back to bed when sleepy. Don't check the time.

This is stimulus control: the bed stays linked to sleep, not to lying awake. Do not extend the reply. For recurring or severe sleep problems, suggest professional support at a calmer time, not in the middle of the night.

## Data reference (fill in for the user's system)

| Purpose | Location or field | Access |
|---|---|---|
| [Review completion marker, today] | [user's field] | [Read] |
| [Plan completion marker, tomorrow] | [user's field] | [Read] |
| [Next-day capture for late notes] | [user's field] | [Read and append only] |

## Style

- Be quiet. Short prompts, one request at a time, no preamble.
- No narration such as "great, moving on," no emojis, no sleep-science lectures.
- If the user is exhausted, they may skip Steps 2 to 4, but not Step 1.
- Use one consistent, compact date and time format.

---
name: wind-down-for-sleep
description: A quiet, interactive bedtime workflow that lowers stimulation, secures distractions, prepares the morning offline, and handles sleeplessness with brief stimulus control.
---

# Wind down for sleep

This workflow guides a user through the last part of their evening, from awake-day to asleep. It is a physical and reliability routine only. It does not review the day or plan tomorrow. Those belong to separate practices that should run earlier in the evening, in this order:

**day review -> next-day plan -> wind down**

This workflow always runs last. The active routine (Steps 1 to 4) should take about 20 to 30 minutes.

## When to use it

- **Full routine (Steps 0 to 6):** the user says "wind down", "help me wind down", "ready for bed", "going to bed", "time for bed", or something similar.
- **Can't-sleep fallback only:** the user says "can't sleep", "still awake", "still up", or something similar after the routine has already run tonight. Skip everything else and go straight to the fallback.

## Setup choices

Agree on these once with the user and reuse them every night. Change them only when the user asks or when the post-run review shows a clear need.

| Choice | Broadly useful default |
|---|---|
| Target asleep time | The user's natural sleep window; work backwards from it |
| Routine start | About 75 to 90 minutes before the target asleep time |
| Earlier bedtime tonight | If the user states an earlier in-bed time, work backwards from that instead |
| Phone return time | Shortly after the user's normal wake time, leaving room for the first morning steps |
| Distraction barrier | A physical lockbox or a charger in another room; software locks alone are often too easy to bypass |
| Environment cues | Dim warm or red light, overhead lights off, optional blue-blocking glasses, quiet audio |
| Morning card | A short handwritten list of the first morning steps |
| Physical prep list | Water, teeth, simple breakfast prep |
| Settling practice | A brief meditation the user already knows |
| Late-note capture location | A dedicated next-day notes field or a paper note, never a private journal |
| Prep and travel buffer | The time the user needs between phone access and their first fixed commitment |

## Purpose

Common wind-down failure modes this routine targets:

- Too much stimulation late at night, leading to scrolling or lying awake.
- Rumination about tomorrow (reduced by doing the day review and a specific next-day plan earlier).
- An inconsistent routine, so the body gets no signal that the day is ending.
- Phone controls that break down because they are too easy to override.

Success looks like this: the next morning the user wakes well, starts their morning routine without reaching for the phone, and the phone stayed out of reach until the agreed return time.

Every step must do at least one of three things: (a) reduce stimulation, (b) act as a reliability mechanism, or (c) prepare the body or the morning. If a step does none of these, cut it.

### Design basis (keep out of the conversation)

- Writing a specific to-do list at bedtime has been shown to shorten the time it takes to fall asleep, so a specific next-day plan should exist before this routine begins.
- Scheduled worry time earlier in the evening reduces bedtime anxiety, so the day review runs earlier by design.
- Dim, warm light and no bright screens in the last hours before bed support sleepiness, so the environment check comes first and gates progress.
- Consistency matters more than contents. The same short sequence every night beats a perfect routine done occasionally.

Do not lecture on any of this during the routine.

## Hard rules

1. **Nothing phone-dependent after Step 1.** The phone is put away at the end of Step 1. Everything afterwards must work offline or on one agreed low-stimulation device.
2. **Step 1 is a gate.** Do not move on until the user confirms every environment item. Never let it be skipped, except where a health, safety, accessibility, or caregiving need makes an item unsuitable.
3. **Never ask about tomorrow.** No outcomes, intentions, priorities, wins, or fallback planning questions. If the next-day plan was skipped, note it silently and continue. Planning re-stimulates at the moment the goal is to de-stimulate.
4. **Do not reopen reflection or planning.** If the user raises a worry or work problem, say: "Put a short note somewhere safe. The review will handle it tomorrow. Not tonight."
5. **No second writing session.** Any freeform journaling belongs to the earlier review, not here.
6. **No summary at the end.** Deliver the close message and stop.
7. **After the close, stop completely.** If the user says good night, reply with nothing or at most "Good night." Never generate a follow-up message, narration, placeholder, or simulated user turn. An unexpected message after bedtime can wake the user.

## Privacy and data access

If the user keeps their review, plan, or calendar in a digital system, access it only with their clear authorization and only for this purpose.

- Read the minimum: whether the review finished, whether the plan exists, and tomorrow morning's first fixed commitment.
- **Do not read private journal text.** Confirm the review finished from a structured signal such as a rating field, a completion flag, or a saved-result record. A journal entry that exists or autosaved does not by itself prove the review finished.
- Do not read messages, inboxes, news, or feeds. The review already handled them.
- Calendar access is read-only and limited to tomorrow morning. If the user has both a work and a personal calendar, check both, because early personal plans move the phone return time as much as meetings do.
- If a connection fails, say so once in one line, use what the user has mentioned, and offer to fix the connection tomorrow, not tonight.

## Step 0: Readiness check

**If the review and plan ran earlier in this same session,** their status and tomorrow's calendar are already known. Do not re-fetch. Just get the current time and continue.

**If run on its own,** make the minimal reads in one parallel batch: current time and dates, today's review status, tomorrow's plan status, and tomorrow morning's calendar events.

Data-handling principles:

- Use tolerant lookups for date-named records (for example, "contains this date" rather than an exact match), because exact matches can fail silently.
- A single date may have more than one record (for example, one created by planning and one by review). Check all matches before deciding something is missing.
- Test whether a field is present, not whether it is truthy. A rating of 0 is a valid completed rating.

State variables:

- `review_done` = today's structured review signal is present.
- `plan_done` = tomorrow's plan is present. Used only silently.
- `late_cutoff` = about 75 minutes before the target asleep time.

| review_done | Time | Action |
|---|---|---|
| Yes | Any | Say "Day reviewed. Starting wind-down." Go to Step 1. |
| No | Before late_cutoff | Ask once: "The day review didn't run. Do it now (about 10 minutes)?" If yes, run it, then return. If no, go to Step 1 with `review_skipped = true`. |
| No | At or after late_cutoff | Say "Too late to review tonight. We'll pick it up tomorrow." Go to Step 1 with `review_skipped = true`. |

If `plan_done` is false, do not mention it, do not offer planning, and do not ask a substitute question.

If the user has set an earlier bedtime tonight, protect time for physical prep and the settling practice. Do not let upstream planning expand into the remaining window.

## Checklist format (Steps 1 and 3)

Use plain `-` bullets in one message, ending with "Reply 'done' when all set." Do not use checkbox syntax, since many interfaces cannot tick boxes, and do not say "tick each". Do not send items one at a time, because that adds extra turns at bedtime. One message out, one "done" back.

## Step 1: Environment and phone gate

**Phone return time:** use the agreed default. If tomorrow's first fixed commitment leaves less than the user's prep and travel buffer after the default return time, move the return earlier to the first commitment minus that buffer. State the chosen time and the reason. Compute the timer length from the current time.

Template:

```
Before we start:
- Day clothes off, sleepwear on
- Low-light glasses on (if used)
- Overhead lights off, dim warm or red lights on
- Quiet sleep audio playing
- Phone in the lockbox, timer {hours}h {minutes}m (returns at {return time}{, reason if earlier than default})
- From here, only {agreed device} is used

Reply "done" when all set.
```

Example reason line: "returns earlier than usual - travel to an early meeting."

If the user delays an item ("I'll do the lights in a sec"), say once: "Do it now. These are the biggest levers. I'll wait." Then wait.

## Step 2: Offline morning card (about 3 minutes)

The user handwrites a small card so the morning does not depend on the phone. The physical act is the commitment device, so do not create a digital version.

> "Write your morning card. Template:
> 1. Brush teeth
> 2. Medication (if any)
> 3. Drink water
> 4. Exercise or physio
> 5. Shower and dress
> 6. Leave or start first block
>
> Anything to add or change tonight?"

If they name a change, say: "Write it on the card where it fits." Then: "Card done?" Keep the template short enough to fit on the card, and update it when the user's routine changes (for example, dropping a commute step after a move to remote work).

## Step 3: Physical prep (about 5 minutes)

Order tasks by location to save steps (bathroom tasks together, kitchen tasks together).

```
- Fill water bottle for the morning
- Brush teeth
- Prep breakfast

Reply "done" when all set.
```

**Late notes.** If a small to-do surfaces ("out of yoghurt, need to buy some"), do not solve it. Capture one line and move on with "Noted. Captured."

Capture rules:

- Write to the agreed late-note location (default: a next-day notes field or paper).
- If writing into an existing record, re-read its current contents first, preserve them exactly, and append one line. Never overwrite from an earlier cached copy.
- If `review_skipped = true` or the review is incomplete, always use the next-day notes location. Do not create a partial or empty review record.
- Never write into or read a private journal entry.

## Step 4: Brief settling practice

Prompt with one line: "5 minutes of meditation." If the user already knows the practice, give no instructions. Wait for "done" or similar. If the user asks to drop or restore this step, do so.

Alternatives if meditation does not suit: slow breathing, a short body scan, or gentle stretching. Nothing screen-based or new.

## Step 5: Close

Say exactly:

> "Close the device. Straight to bed, no detour.
>
> See you tomorrow."

This is the last user-facing message. No "sweet dreams", no summary.

## Step 6: Silent post-run review

If the assistant can maintain the workflow, do this silently after the close, with no output to the user. Do not ask the tired user to diagnose their own routine.

| Signal in this run | Change |
|---|---|
| User misread a prompt or asked "what do you mean?" | Rewrite the prompt in plainer words |
| User pushed back on a step | Rewrite or cut it |
| A lookup returned nothing or found the wrong record | Fix the lookup instructions |
| An item was skipped without comment, adding nothing | Cut it or make it optional |
| User stated a preference ("don't ask me X") | Add it as a hard rule |
| A worry keeps surfacing at bedtime | Move its prevention into the earlier review or plan |
| The distraction barrier is routinely bypassed | Agree a stronger physical or environmental barrier with the user later |

If the run was clean, change nothing. Do not invent improvements. Do not report changes to the user tonight; they can review them later if they want.

## Can't-sleep fallback

Do not rerun the routine or reopen reflection or planning. Reply briefly:

> "Out of bed. Dim room, boring screen-free activity (paper reading, no problem-solving), about 20 minutes. Back to bed when sleepy. Don't check the time."

This is stimulus control: the bed stays linked with sleep, not with lying awake. Do not extend the reply. For ongoing or severe sleep problems, suggest appropriate medical or sleep-care support at a later, non-bedtime moment.

## Style

- Quiet and short. One prompt at a time, no preamble.
- No narration ("great, now let's..."), no emojis, no coaching tone.
- If the user is exhausted, allow skipping Steps 2 and 3, but not Step 1.
- Use the user's preferred date format.

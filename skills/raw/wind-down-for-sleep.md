---
name: wind-down-for-sleep
description: Guides a short evening routine that lowers stimulation, prepares the body, and handles sleepless nights. Use when someone says "wind down", "ready for bed", or "can't sleep".
---

# Wind down for sleep

This interactive evening workflow moves the user from the awake part of the day to sleep by lowering stimulation, adding reliability, and preparing the body. It runs last in the evening, after any day review and next-day planning, and does neither of those itself.

## Quick version

- Say "wind down" when you are ready to start.
- Do the gate in one go: sleep clothes on, teeth brushed, and your phone or other distracting device out of reach, ideally in another room or a timed box. Set it to come back only when tomorrow morning needs it, based on your first real commitment.
- Then a few minutes of a calming practice you already know, and the screen goes off. That is the last message of the night.
- Go to bed when you feel sleepy, not when the clock says so. Until then, read something on paper in dim light somewhere other than the bed.
- If a worry or task comes up, write one line on paper for tomorrow and leave it. Do not plan tomorrow or reflect on today during this ritual.
- If you are still awake after what feels like about 20 minutes in bed, get up, do something dull in dim light, and return when sleepy.

## 1. Purpose and evening order

Recommended evening order: **day review, then next-day planning, then wind-down.** Reflection belongs to the earlier day-review practice and tomorrow belongs to the earlier planning practice. This workflow comes last.

Target length for the active ritual: short, about 15 to 20 minutes as an adjustable default. Longer rituals tend to get skipped, and every extra message keeps the user looking at a screen.

It targets late stimulation (scrolling, lying awake), worry about tomorrow (mostly handled by the earlier review and specific planning), an inconsistent routine, and distraction controls that are easy to bypass. Physical barriers usually beat software limits on the same device.

Success signal: the user wakes rested, starts the morning without scrolling, and the device stays out of reach until the access time set from tomorrow's commitments. Every step must reduce stimulation, add reliability, or prepare the body; remove any step that does none of these. Re-read this purpose every run.

Design anchors, never explained at bedtime: a specific to-do list written earlier has been linked to falling asleep faster, which is why planning runs before this workflow rather than inside it; scheduled worry time earlier in the evening reduces bedtime anxiety; dim, warm light helps sleep onset; the bed should stay linked with sleep, so sleepiness rather than the clock is the cue to get in; and consistency matters more than contents.

## 2. Standalone mode

You do not need daily records, a calendar, or any other workflow to use this. Tell the assistant tonight's bedtime and your first fixed commitment tomorrow morning, if any, then run Steps 1 and 2 from that alone, and skip Step 0. Use paper as the capture spot.

Chatting with an assistant on a bright screen works against winding down. Use voice if you can, keep the screen dimmed and warm, and let the close be the last thing you read.

## 3. Settings the user chooses

Agree on these once. Reuse them every night until the user changes them. Offer the starting points only as adjustable suggestions, and do not assume values the user has not chosen.

| Setting | What to decide | Suggested starting point |
|---|---|---|
| Target sleep time | When the user wants to be asleep | Based on their natural sleep window and wake time |
| Ritual start | When wind-down usually begins | Enough before target sleep time for the ritual plus some reading |
| Review cutoff | When a missed review is skipped | When a review would push sleep back |
| Distraction barrier | How the device goes out of reach | A timed box or another room |
| Default access time | When the device comes back if nothing early is booked | After the first part of the morning routine |
| Commitment cutoff | How early a commitment must be to move access earlier | Shortly after the default access time plus the commitment buffer |
| Commitment buffer | Time before a commitment to get ready and arrange transport | 45 to 60 minutes |
| Travel buffer | Time before a travel or commute block, which already marks departure | 15 to 20 minutes |
| Gate items | The few changes that signal night, including any essential body prep | A clothing change, teeth, and the distraction barrier |
| Allowed device | The one low-stimulation device, if any, after the gate | None |
| Settling practice | A short familiar practice done after the last message | A few minutes of slow breathing |
| Capture spot | Where stray tasks go for tomorrow | A notes field on tomorrow's record, or paper |

If the user names an earlier bedtime for tonight, work backwards from it. Protect time for the gate and the settling practice. Do not let planning expand into the remaining window.

## 4. Triggers

- **Full ritual:** "wind down", "ready for bed", "going to bed", "time for bed", "help me get to sleep", or similar.
- **Can't-sleep fallback only:** "can't sleep", "still up", "still awake", or similar, after the ritual already ran tonight. Skip every other step and go straight to Step 4.

## 5. Hard rules

- **Gate first.** Do not continue past Step 1 until the user confirms it.
- **Keep the gate minimal.** Include only the gate items the user chose. If the user removes an item or stops a prep task, do not add it back later or move it into a separate step.
- **No distracting-device step after Step 1.** Everything afterward must work offline or with the one allowed device.
- **Never ask about tomorrow, and do not reopen reflection or planning.** No outcomes, intentions, wins, or backup one-line plan. If planning was skipped, note it silently and continue. Planning questions raise alertness at the moment the goal is to lower it. Do not open a second writing session; any journal writing belongs to the review, before its questions.
- **Deflect tomorrow-concerns.** Say: "Put a short note in your capture spot. The review will handle it tomorrow. Not tonight."
- **No summary at the end.** Send the close and stop.
- **Stay silent after the close.** If the user says good night, reply with nothing or only "Good night." Never send a follow-up, a placeholder, or a simulated user turn. An unexpected message after bedtime can wake someone up.

## 6. Step 0: Readiness check

Gather only what is needed to confirm the earlier practices ran and to set the access time. Do not open inboxes, news, or feeds.

If the review and planning ran earlier in the same session, skip all lookups. That state and tomorrow's calendars are already known, so reuse them. Check the current time and continue.

If this workflow runs on its own, gather the following in one batch:

1. Current time, today's date, and tomorrow's date.
2. Whether today's review is complete.
3. Whether tomorrow's plan exists.
4. Tomorrow's morning events (midnight to midday) from every calendar the user approved. Include personal as well as work calendars, since social plans and early activities move the access time too.

| Review complete? | Time | Action |
|---|---|---|
| Yes | Any | Say "Day reviewed. Starting wind-down." Go to Step 1. |
| No | Before review cutoff | Say "The day review didn't run. Do it now (about 10 minutes)?" If yes, run it and return. If no, go to Step 1. |
| No | At or after cutoff | Say "Too late to review tonight. We'll pick it up tomorrow." Go to Step 1. |

If tomorrow's plan is missing, do not mention it, offer planning, or ask a fallback question.

## 7. Checklist format (Step 1)

Use a plain bullet list, not checkboxes. Many interfaces cannot tick boxes, and "tick each one" wording confuses people. Send the whole list in one message and end with "Reply 'done' when all set." Expect one reply. Do not send items one at a time, because that adds turns at bedtime.

## 8. Step 1: Body and distraction gate

This is the only checklist. It combines the night signal, essential body prep, and the device barrier.

Set the access time from tomorrow's calendars every night. There is no fixed time; the device comes back only when the morning needs it.

1. **Use every approved calendar** for tomorrow morning. If the evening's planning already read them, reuse those results as they stood after any blocks planning moved. Never set the time from the work calendar alone. If a source failed, say so once and use what the user has mentioned.
2. **Convert every event time to local time** from its returned zone or offset before comparing. An event that looks late may actually be early.
3. **Find the commitments.** A commitment is a timed event that fixes when the user must be somewhere or with someone: meetings and calls with other attendees the user has not declined, in-person plans, appointments, fixed-time exercise, and travel or commute blocks. These do not count: all-day events, declined or canceled events, sleep blocks, routine blocks, solo work and focus blocks, meals, and out-of-office placeholders.
4. **Take the earliest of:** each commitment's start minus the commitment buffer, and each travel block's start minus the travel buffer.
5. **If no commitment falls before the commitment cutoff,** use the default access time.
6. **If the result is before the user's usual wake time,** keep it and flag it as an early start.
7. **Put the access time, the reason (event and which calendar), and the countdown from now** on the checklist line.

```
Before we start:
- [Clothing change, e.g. day clothes off, sleep clothes on]
- [Body prep item, e.g. teeth brushed]
- [Distraction barrier], timer [duration] (access at [time], [reason, e.g. "for the early call (work)", or "nothing before the cutoff"])

Reply "done" when all set.
```

If the user delays an item ("I'll do the phone in a sec"), say once: "Do it now. These are the biggest levers. I'll wait." Then wait. Once confirmed, go straight to Step 2.

## 9. Small to-dos raised mid-ritual

If a small task surfaces ("library book is due, return it tomorrow"), do not solve it. Capture one line so it leaves the user's head:

- Append to tomorrow's capture spot. Read only that spot first, preserve existing text exactly, and never overwrite from an earlier cached value. Never write into a private journal or a review record.
- Then say: "Noted. Captured." If the gate is already confirmed, put this acknowledgment in the same message as the close rather than sending an extra turn.

## 10. Step 2: Settling practice and close (one message)

As soon as the user confirms the gate, send one final message that names the settling practice, ends screen time, and gives the bed cue. Because it is the last message, the user has no reason to come back to the screen. Adapt the wording to the user's setup:

> [Settling practice, e.g. "A few minutes of slow breathing."] Then screen off.
>
> Go to bed once you feel sleepy. Until then, read something on paper in low light, away from the bed.
>
> Talk tomorrow.

Rules for this message:

- Give no instructions if the user already knows the practice, and never introduce something new at bedtime.
- Do not wait for "done" after the practice. The conversation ends here.
- The cue to get into bed is sleepiness, not the clock. The target sleep time is a goal, not a command to lie down awake.
- No recap and no "sweet dreams".
- If the user asks to drop the practice, cut that line from the close. Restore it whenever they ask.

Then move silently to the audit.

## 11. Step 3: Routine audit (silent)

After the close, review the run without sending anything. Do not ask a tired person to diagnose their own ritual. If the user approved direct edits, update the routine. Otherwise, save proposed changes for daytime review. Do not report what changed.

| Signal | Change |
|---|---|
| User misread a prompt or asked what it meant | Rewrite it in plainer words |
| User pushed back on a step | Simplify it, make it optional, or cut it |
| A lookup failed or found the wrong record | Fix the lookup rule |
| The user corrected the access time | Check which calendar, commitment rule, or time conversion was missed and fix that rule |
| An item is skipped without comment or dropped from the user's evening | Remove it |
| User stated a preference ("don't ask me X") | Add it as a hard rule |
| The user came back to the screen after the close | Fold any remaining step into the close so nothing waits on a reply |
| The barrier keeps being bypassed | Choose a stronger physical barrier with the user |
| The same worry keeps appearing at bedtime | Move its prevention into the earlier review or planning |

How to edit:

- Before editing, decide where the lesson belongs. If the user keeps general guidance on where lessons go, check it first. A reusable rule goes in the routine itself; detailed lookup or setup specifics go in a separate reference note; a one-off incident goes only in the history log, if there is one.
- Edit or merge an existing rule rather than adding a new paragraph. The routine should stay short enough to run quickly.
- Write rules as general principles. Do not add dated incident stories to the routine itself.
- If you want a history, keep a separate one-line-per-entry log of what happened and why a rule changed. Do not load that log during a normal run.
- If the run was clean, change nothing. Do not invent improvements.

If the user re-engages because they cannot sleep, go to Step 4.

## 12. Step 4: Can't-sleep fallback (stimulus control)

Use only when the user reports being awake after the ritual. Do not rerun the ritual or reopen planning. Say:

> Get up for a bit. Low light, something dull like a paper book or folding laundry, nothing on a screen and nothing to solve. Go back to bed once you feel sleepy, and leave the clock alone.

This keeps the bed linked with sleep rather than with lying awake. Do not extend the reply. If sleep trouble is frequent or severe, suggest professional support at a daytime moment, not at night.

## 13. Worked example (invented)

Alex says "wind down" with no records connected. Bedtime is an hour away and nothing is booked early tomorrow, so the phone comes back at Alex's default time after breakfast.

- Assistant: "Before we start: sleep clothes on, teeth brushed, phone in the kitchen drawer until after breakfast (nothing early tomorrow). Reply 'done' when all set."
- Alex: "done. oh, need to call the dentist"
- Assistant: "Write it on the paper by your bed. Not tonight. Ten slow breaths, then screen off. Go to bed once you feel sleepy; until then, read on paper in low light somewhere else. Talk tomorrow."

The assistant sends nothing more, even if Alex replies "good night" (at most, "Good night.").

## 14. Exhaustion rule

If the user is clearly exhausted, they may skip the settling practice. Do not skip Step 1, because it is the load-bearing step, unless a health, safety, accessibility, or caregiving need makes it unsuitable.

## 15. Style

- Quiet and short. One question at a time. No preamble.
- No narration ("great, now let's...") and no emojis.
- No sleep science at runtime.
- If the user goes off-script with a work problem, deflect to the capture spot and tomorrow's review.
- Use the user's preferred date and time format, and keep it consistent across the run.

The best wind-down is quiet, repeatable, and boring enough to become an automatic signal that the day is over.

## Optional extras

### Connected records and calendars

If the workflow connects to a journal, day records, or calendars, use only sources the user has authorized, and only to confirm status and set the access time. Treat calendars as read-only, and keep what you see inside the session.

Lookup principles:

- **Request only the fields you need.** Use an explicit list of fields on every record read, and leave private journal text off that list. Never read, quote, reconstruct, or write into it.
- **Confirm the review from a completion signal.** Use the review's own save confirmation from this session, or a dedicated rating or done marker. A saved free-form entry without that signal does not mean the review finished.
- **Test presence, not truthiness.** A zero rating is a valid, completed rating.
- **Match dates by calendar day** and expect more than one record per day. Exact-match text filters can miss records that exist, so compare dates with a date-aware check at day granularity rather than as text. Use the same lookup method as your other planning and review workflows so they find the same records. Check each matching record instead of assuming a single one.
- **Query calendars in local time.** Give the morning window an explicit local offset, then still convert each returned event to local time before comparing.
- **Degrade quietly.** If a source fails, say so once, compute from what you have plus anything the user mentioned, and leave repair for daytime.

### Invented access-time example

Jordan's example settings, all adjustable: commitment buffer 60 minutes, travel buffer 20 minutes. Times below are relative to Jordan's usual wake time.

- Work calendar: a solo focus block starting half an hour before wake time (does not count) and a team call one hour after wake time (commitment, so access at wake time).
- Personal calendar: "Bus to the climbing gym" returned with a different zone offset, so it first looks like a mid-morning event. Converted to local time, it starts right at wake time. It is a travel block, so access 20 minutes before wake time.

The earliest result is 20 minutes before wake time, which is earlier than usual, so keep it and flag it. The checklist line reads: "Phone in the box, timer [hours until then] (access 20 minutes before your usual wake time, for the gym bus (personal), early start)."

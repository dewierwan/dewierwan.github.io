---
name: recurring-events
description: Sets up the next date of a recurring community event: fresh poster, event page, and invites to opted-in past guests. Use when someone says set up this week's event or post the next one.
---

# Run a recurring community event

Use this when you host a regular event, such as a monthly book swap or game night, and want the assistant to set up the next one: date, fresh poster, event page, and invites, with as few questions as possible.

## Quick version

- Tell the assistant the series name, the rule for when it happens (for example "first Thursday of each month"), the last event number, and any dates that already have an event.
- Ask it to work out the next open date with a real calendar, not in its head.
- Have it reuse last time's description and update only what changed.
- Ask for one fresh poster idea that is clearly different from the last few, written as a single-paragraph image prompt.
- Paste the finished text into your event page yourself, check it as a guest would, and mark yourself as going if that is your habit.
- Invite the usual people, then check the invite count before and after sending.

## Authorization: confirm once, then act

For your own series, standing authorization is the natural default. Confirm it once, in writing, with the series, the usual hosts, who gets invited, and what the assistant may publish and send. After that, each new occurrence should need zero questions. Stop and ask only when something real changes: a new venue, a price, a bigger or different audience, a public listing, or a safety issue.

The invite step reads past guest lists, so use them only to invite people to this series, and only people who agreed to hear about future events, such as past guests who have not opted out. Read only the lists you need, leave out unrelated personal details, keep any names and counts inside the host team, and make opting out easy.

## 1. Work out the date and number

- Compute the next date from the recurrence rule with a calendar or date tool. Weekday and date errors are the most common mistake.
- Check the list of events you already host before picking dates, and skip any date that already has one. A request for "three new ones" means the next three open dates.
- Find the highest existing event number and add one. For several events, use sequential numbers, each with its own poster.
- Check for clashes: a holiday, the venue being closed, or the host being away. A clash does not cancel the event by itself. Go ahead under the standing policy and name the clash in the final report so the host can hand off or cancel.

## 2. Make a fresh poster

Look at the last two or three posters first so you do not repeat them. Keep the series identity steady (the name in the same hand-lettered style, the core activity, a warm and simple look) and change the big idea each time.

Levers worth pulling:

- **Season, weather, light:** first frost, a rainy window, long summer evening light.
- **Viewpoint:** looking up past a teacup, a bird's-eye view of the table, a view from inside a bookshelf.
- **One witty focal object:** a chess knight wearing a party hat, a stack of paperbacks shaped like a lighthouse, a dice cup used as a flowerpot.
- **Local texture:** a familiar street corner, the venue's door, a local landmark.

One clear joke beats a busy scene.

Anti-cliché guardrails to put in the prompt:

- one clear subject and a restrained palette;
- clean, correctly spelled lettering;
- no extra fingers, melted objects, or garbled text;
- no glossy over-rendered finish or generic "epic" lighting.

If the result looks like last time or has obvious generated tells, say so and regenerate once or twice.

Practical rules for the image tool:

- **Write the prompt as one paragraph.** In many chat tools Enter sends the message, so a multi-line prompt gets cut off. If that happens, stop and send the rest as a follow-up.
- **Check before retrying.** Image tools sometimes show an error even though the image finished.
- **Mind your image limit.** Limited plans may allow only a few images per day. When you need several posters, make each prompt strong enough to keep on the first try and send them together in separate fresh chats, so a batch does not use up your retries.

## 3. Build the event page

Reuse the stable parts of the last description and update the rest. Fill fields in this order, because date pickers are often fragile:

1. Title, using the series pattern, such as "Book Swap #N".
2. Date, start and end time. Check the shown date before touching anything else.
3. Location, picking the exact venue, not a similar name.
4. Description.
5. Image. Wait for the upload to finish and check it shows.
6. Co-hosts, if any.
7. Leave visibility, cost, and capacity at the series defaults.

Some platforms publish on a button labeled "Save" or "Done," so know what it does before pressing it. Then check the live page as a guest would: title, date, time, location, description, and image.

If the host wants it (a choice you set once), RSVP as the host: mark yourself as going, leave plus-ones and comments empty, close any follow-up prompts, and confirm the page shows one person going.

## 4. Invite the approved audience

Invite past guests of the series, one past event at a time, including any early unnumbered events. Before pressing "Select all," check whether people are already selected, because pressing it again can clear them. Watch the invite count rise after each group. If it stays flat or drops, stop and look. Send, then confirm the sent state and final count.

## 5. Report

Keep it short: what was created, date and venue, the invite count, any clash from step 1, and the live link as the last line.

## Worked example (invented)

Series: "Second Saturday Board Games," monthly, at a neighborhood café, hosts Priya and Tom, invite list is past guests who have not opted out. The host has asked to be marked as going on each new event.

- Last event was #11 in March. A calendar check gives Saturday 12 April, so this is #12. The hosting list shows no event on that date yet.
- The café closes early that day. Under the standing policy the assistant keeps the usual slot and flags the clash.
- Last two posters were a meeple on a mountain and a rainy window with cards. This time: a bird's-eye view of a game board laid out like a city park, with a single tiny meeple walking a dog. Warm colors, hand-lettered title, nothing else in frame.
- Description carries over unchanged except the date and a new line: "Bring a game you have not played in a year."
- After publishing, the assistant RSVPs as Priya and the page shows "1 going."
- Invites: 11 past sessions, count rises from 0 to 46 with no drops. Sent.

Report: "Board Games #12 is live for Sat 12 April at the café. 46 people invited. Note: the café may close early that day, so you may want to confirm the time with them." Link on the final line.

If Priya later asks for "three more" and #13 already exists for May, the new ones become #14, #15, and #16 on the June, July, and August dates.

## After each run

Keep only reusable lessons, such as platform quirks or a changed template, and update your notes in the same session.

## Optional extras

For assistants that drive a browser or other connected tools:

- **Right account for each site:** the image tool and the event platform may be logged in under different browser profiles or accounts. Route each site to the right one and verify the active account before acting.
- **File handling:** avoid buttons that open a native file dialog the tool cannot control; use the page's file input or the tool's file-chooser support, from a folder the tool can read. If a browser silently blocks a second download, capture the image another way, such as a full-size screenshot of just the image.
- **Verify after every change on screen:** pages shift when extra controls appear, windows resize, or a page is still loading. Take a fresh screenshot before each click after any shift, confirm nothing changed by accident (a style, a date, a selection), and close pickers by clicking empty background rather than trusting close icons or Escape.
- **One thing at a time:** finish and verify an upload before opening another panel. If you script the invite loop, handle one past event per call to stay under time limits, normalize unusual spaces in labels before matching text, wait for each list to load, and read the invite count after each pass.
- **Shared notes:** keep series-specific quirks with this workflow and move general browser lessons into a shared notes file.

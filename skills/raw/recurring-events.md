---
name: recurring-events
description: Publish the next date of a recurring community event, refresh its image and copy, and invite people who opted in. Use when someone says set up this week's event or post the next one.
---

# Run a recurring community event

Use this when you host a regular event, such as a monthly book swap or game night, and want the assistant to set up the next one: date, fresh poster, event page, and invites, with as few questions as possible.

## Quick version

- Tell the assistant the series name, the rule for when it happens (for example "first Thursday of each month"), and the last event number.
- Ask it to work out the next date with a real calendar, not in its head.
- Have it reuse last time's description and update only what changed.
- Ask for one fresh poster idea that is clearly different from the last few.
- Paste the finished text into your event page yourself, check it as a guest would, then invite the usual people.

## Authorization: confirm once, then act

For your own series, standing authorization is the natural default. Confirm it once, in writing, with the series, the usual hosts, who gets invited, and what the assistant may publish and send. After that, each new occurrence should need zero questions. Stop and ask only when something real changes: a new venue, a price, a bigger or different audience, a public listing, or a safety issue. Invite only people who agreed to hear about future events in the series, such as past guests who have not opted out, and make opting out easy.

## 1. Work out the date and number

- Compute the next date from the recurrence rule with a calendar or date tool. Weekday and date errors are the most common mistake.
- Find the highest existing event number and add one.
- Check for clashes: a holiday, the venue being closed, or the host being away. A clash does not cancel the event by itself. Go ahead under the standing policy and name the clash in the final report so the host can hand off or cancel.
- For several events, use consecutive dates and numbers, each with its own poster.

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

**Composer trap:** write the image prompt as one paragraph with no line breaks. In many chat tools, pressing Enter sends the message, so a multi-line prompt gets cut off after the first line. If that happens, stop the generation and send the rest as a follow-up.

Image tools sometimes show an error even though the image finished, so check for a new image before retrying.

## 3. Build the event page

Reuse the stable parts of the last description and update the rest. Fill fields in this order, because date pickers are often fragile:

1. Title, using the series pattern, such as "Book Swap #N".
2. Date, start and end time. Check the shown date before touching anything else.
3. Location, picking the exact venue, not a similar name.
4. Description.
5. Image. Wait for the upload to finish and check it shows.
6. Co-hosts, if any.
7. Leave visibility, cost, and capacity at the series defaults.

Some platforms publish on a button labeled "Save" or "Done," so know what it does before pressing it. Then check the live page as a guest would.

## 4. Invite the approved audience

Invite past guests of the series, one past event at a time. Include early unnumbered events when inviting past guests. Before pressing "Select all," check whether people are already selected, because pressing it again can clear them. Watch the invite count rise after each group. If it stays flat or drops, stop and look. Send, then confirm the sent state and final count.

## 5. Report

Keep it short: what was created, date and venue, the invite count, any clash from step 1, and the live link as the last line.

## Worked example (invented)

Series: "Second Saturday Board Games," monthly, at a neighborhood café, hosts Priya and Tom, invite list is past guests who have not opted out.

- Last event was #11 in March. A calendar check gives Saturday 12 April, so this is #12.
- The café closes early that day. Under the standing policy the assistant keeps the usual slot and flags the clash.
- Last two posters were a meeple on a mountain and a rainy window with cards. This time: a bird's-eye view of a game board laid out like a city park, with a single tiny meeple walking a dog. Warm colors, hand-lettered title, nothing else in frame.
- Description carries over unchanged except the date and a new line: "Bring a game you have not played in a year."
- Invites: 11 past sessions, count rises from 0 to 46 with no drops. Sent.

Report: "Board Games #12 is live for Sat 12 April at the café. 46 people invited. Note: the café may close early that day, so you may want to confirm the time with them." Link on the final line.

## After each run

Keep only reusable lessons, such as platform quirks or a changed template. Never store guest details or quietly widen who gets invited.

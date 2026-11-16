---
name: recurring-events
description: Sets up the next date of a recurring community event: date, poster, event page, invites, and site listing. Use when someone says set up this week's event or post the next few.
---

# Run a recurring community event

Use this when you host a regular event, such as a monthly book swap or game night, and want the assistant to set up the next one: date, fresh poster, event page, invites, and any website listing, with as few questions as possible.

## Quick version

- Tell the assistant the series name, the rule for when it happens (for example "first Thursday of each month"), the last event number, and any dates that already have an event.
- Ask it to work out the next open date with a real calendar, not in its head.
- Have it reuse last time's description and update only what changed.
- Describe your last few posters and ask for one fresh idea that is clearly different, written as a single-paragraph image prompt.
- Paste the finished text into your event page yourself, check it as a guest would, and mark yourself as going if that is your habit.
- Invite the usual people, then check the invite count before and after sending.
- If the series has a website or shared calendar, add the new link there too, and note whether that worked.

## Authorization: confirm once, then act

For your own series, standing authorization is the natural default. Confirm it once, in writing: the series, the usual hosts, who gets invited, and what the assistant may publish and send. After that, each new occurrence should need zero questions. Stop and ask only when something real changes: a new venue, a price, a bigger or different audience, a public listing, or a safety issue.

Standing authorization does not override the assistant's own safety controls. Try the send step first. If a tool blocks it anyway, do not look for a workaround: finish creating every event in the batch, then ask the host once to approve all the sends together.

The invite step reads past guest lists, so use them only to invite people to this series, and only people who agreed to hear about future events. Read only the lists you need, leave out unrelated personal details, keep names and counts inside the host team, and make opting out easy.

## 1. Work out the date and number

- Compute the next date from the recurrence rule with a calendar or date tool. Weekday and date errors are the most common mistake.
- Check the events you already host before picking dates, and skip any date that already has one. "Three new ones" means the next three open dates.
- Take the highest existing event number and add one. For several events, use sequential numbers, each with its own poster.
- Check for clashes: a holiday, the venue being closed, or the host being away. A clash does not cancel the event by itself. Go ahead and name the clash in the final report so the host can hand off or cancel.

## 2. Make a fresh poster

Look at the last two or three posters first so you do not repeat them. If the usual place you keep them is gone, use the images on the most recent event pages instead; viewing them side by side makes repetition easy to spot.

Keep the series identity steady (the name in the same lettering style, the core activity, a warm and simple look) and change the big idea each time, rather than "same style, new scene." Levers worth pulling:

- **Season, weather, light:** first frost, a rainy window, long summer evening light.
- **Viewpoint:** looking up past a teacup, a bird's-eye view of the table.
- **One witty focal object:** a chess knight wearing a party hat, paperbacks stacked like a lighthouse.
- **Local texture:** a familiar street corner, the venue's door, a local landmark.

One clear joke beats a busy scene. Put these guardrails in the prompt: one clear subject, a restrained palette, clean and correctly spelled lettering, no extra fingers or garbled text, no glossy over-rendered finish or generic "epic" lighting. If the result looks like last time or has obvious generated tells, say so and regenerate once or twice. If the tool offers two options, keep the stronger one.

Practical rules for the image tool:

- **Write the prompt as one paragraph.** In many chat tools Enter sends the message, so a multi-line prompt gets cut off. If that happens, send the rest as a follow-up.
- **Check before retrying.** Image tools sometimes show an error even though the image finished.
- **Use an account with enough image capacity.** Limited plans can run out before you can regenerate. For several posters, send each prompt in its own fresh chat at the same time.

## 3. Build the event page

Reuse the stable parts of the last description and update the rest. Fill fields in this order, because date pickers are often fragile:

1. Title, using the series pattern, such as "Book Swap #N".
2. Date, start and end time. Check the shown date before touching anything else.
3. Location, picking the exact venue, not a similar name.
4. Description.
5. Image. Wait for the upload to finish and check it shows before editing anything else.
6. Co-hosts, if any.
7. Visibility, cost, and capacity at the series defaults.

Some platforms publish on a button labeled "Save" or "Done," so know what it does before pressing it. Then check the live page as a guest would: title, date, time, location, description, and image.

If the host wants it (a choice you set once), RSVP as the host: mark going, leave plus-ones and comments empty, close any follow-up prompts, and confirm the page shows one person going.

## 4. Invite the approved audience

Invite past guests of the series one past event at a time, including any early unnumbered events.

- **Pick each past event by its exact name**, not its position in a list. Newly created events join the list and shift the rest.
- **Check the selection before pressing "Select all."** Some platforms pre-select guests, and pressing it again clears them. Skip past events with nobody to select.
- **Watch the invite count** rise after each group by roughly that group's size. If it stays flat or drops, stop and look.

Send, then confirm the final count where the platform records it, which may be a guest management view rather than the invite panel. If guests still show as "sending," reload once before judging. New events invited from the same past events should land on the same count; a mismatch suggests a missed group.

## 5. Update the series website or listing

If the series has its own website, newsletter page, or shared calendar, check how it learns about new events. Many sites show only events listed explicitly, because event links are random and cannot be guessed. Skip this step and new events never appear, and any "next event" link stops at the last one listed.

- Wait until every event in the batch is live, then add all the new links in one update, starting from the latest version if others also edit the site.
- If the site pulls dates, images, and status from the event platform, add only the links.
- If the update fails, say so in the report. The events still exist, so this is a follow-up, not a reason to undo anything.

## 6. Report

Keep it short: what was created, date and venue, the invite count, any clash from step 1, whether the website or listing was updated, and the live link as the last line with nothing after it, so it is easy to copy.

## Worked example (invented)

Series: "Second Saturday Board Games," monthly, at a neighborhood café, hosts Priya and Tom, invite list is past guests who have not opted out. The host likes to be marked as going, and a small website lists each event link.

- Last event was #11 in March. A calendar check gives Saturday 12 April, with no event yet, so this is #12.
- The café closes early that day. The assistant keeps the usual slot and flags the clash.
- Last two posters were a meeple on a mountain and a rainy window with cards. This time: a bird's-eye view of a game board laid out like a city park, with one tiny meeple walking a dog. Warm colors, hand-lettered title, nothing else in frame.
- Description carries over except the date and a new line: "Bring a game you have not played in a year."
- After publishing, the assistant RSVPs as Priya and the page shows "1 going."
- Invites: 11 past sessions, count rises from 0 to 46 with no drops. Sent, and the guest view shows 46 invited after one reload.
- The website now shows #12 as the next event.

Report: "Board Games #12 is live for Sat 12 April at the café. 46 people invited, and the website lists it. Note: the café may close early that day, so you may want to confirm the time." Link on the final line.

If Priya later asks for "three more" and #13 already exists for May, the new ones become #14, #15, and #16 on the June, July, and August dates, added to the website in one update, and all three should show the same invite count.

## After each run

Keep only reusable lessons, such as a platform change or an updated template, and update your notes in the same session. Before editing, check your own rule for where a lesson belongs: in this workflow, in a shared note on general tool mechanics that applies beyond this series, or in a separate lessons file kept for this workflow.

## Optional extras

For assistants that drive a browser or other connected tools:

- **Right account for each site:** the image tool and event platform may use different browser profiles, accounts, or workspaces with different limits. Route each site correctly and verify the active account before acting.
- **Reviewing past posters without a browser:** fetch the last few event pages from your own event list, pull out each poster at a small size, and join them into one strip to review in a single view.
- **Stale text in input boxes:** scripted sending can leave an old prompt in a chat box. Read it before typing; replace it if it was automated, and save it and tell the host if they wrote it. Clear the box when done.
- **File handling:** avoid buttons that open a native file dialog the tool cannot control; use the page's file input or the tool's file-chooser support, from a folder the tool can read. If the browser blocks repeat downloads, capture the image another way, such as a full-size screenshot of just the image, with its tab in front.
- **Verify after every on-screen change:** pages shift when controls appear, windows resize, or content is still loading. Take a fresh screenshot before each click after any shift, confirm nothing changed by accident, close pickers by clicking empty background, and retype if early typing was lost.
- **Scripted invite loop:** handle one past event per call to stay under time limits, group a handful of calls into a batch, normalize unusual spaces before matching labels, wait for each list to load, and read the count after each pass.
- **Website built from a code repository:** keep a small script that adds event links to the site's list. Pull the latest version, run the script once with all new links, calling it by its full path so it works from whatever folder the session happens to be in, commit with a message naming the event numbers, publish, and confirm the events appear.

---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, tall, and target viewports using both real screenshots and programmatic layout checks. Fix every failure and rerun the relevant sweep before reporting the work as完成.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, background, or typography edits: a local change can affect wrapping, height, overflow, alignment, and background visibility at other viewport sizes.

A bounding-box measurement alone is not sufficient. One desktop and one mobile screenshot are not sufficient. Real screenshots and numerical checks catch different failure types, so use both.

## 1. Prepare realistic test states

Run the actual interface in an appropriate test environment. Populate changed surfaces with representative content before capture:

- long paragraphs, formatted text, and long field values;
- representative lists, cards, rows, and validation messages;
- realistic item counts, including content near expected limits;
- loading, empty, and error states when the change can affect them.

Do not validate only a clean or empty state. Sparse content often hides clipping, overlap, unexpected whitespace, and wrapping failures.

## 2. Select the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages, dashboards, or interfaces expected on large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short viewport of about 700 px;
- a tall viewport of about 1400 px or greater.

Include any known target viewport supplied by the requester or product requirements. Explicitly test a very tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, bottom alignment, or similar vertical behavior.

Use a repeatable headless browser automation capability chosen for the project. Capture evidence from the rendered interface, not only from style rules or element measurements.

## 3. Capture and inspect screenshots

Capture screenshots at every relevant viewport and content state. Use full-page screenshots when page length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect each changed component on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design now that the component's role has changed.

Give extra attention to full-bleed, edge-to-edge, or flush changes. Making a component flush on one side can reveal leftover margin or wrapper padding on another side as a visible background strip. Verify every edge, not only the edge directly edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result solely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshot inspection. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is intended to fit the viewport;
- no changed element overlaps neighboring content or escapes its intended container;
- buttons, links, and form fields remain visible, reachable, and usable;
- fixed or sticky UI does not hide required content;
- cards, lists, and controls remain within intended bounds;
- body text retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare the bounding rectangles of relevant elements with adjacent elements and container boundaries.

For prose-heavy pages, flag excessively wide text measures. A useful warning threshold is roughly 80 characters per line; reading-focused designs commonly target about 60–70 characters per line.

## 5. Require both forms of evidence

Measurements can miss visible defects such as exposed background strips, poor visual balance, and unexpected blank regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and all relevant programmatic checks pass.

## 6. Fix failures and retest

If any viewport or realistic state fails:

1. Stop the completion, review, or release process.
2. Identify the layout rule or structural behavior causing the failure.
3. Fix the underlying cause rather than adding a narrow viewport-specific cosmetic patch.
4. Rerun the complete relevant sweep, not only the viewport that exposed the problem.

If a change makes one viewport correct but breaks another, reconsider the diagnosis. The layout model or component constraint is likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights and states, and the checks performed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, state that clearly and do not represent the UI change as complete.

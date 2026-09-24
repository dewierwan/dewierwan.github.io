---
name: test-every-screen-size
description: Verify every UI, layout, and CSS change across representative narrow, wide, short, and tall viewports using real screenshots and programmatic layout checks, then fix and retest failures before reporting the work as complete.
---

# Test every screen size

Use this workflow after **every UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to a one-line spacing or background change: a local edit can alter wrapping, height, overflow, alignment, or exposed backgrounds at other screen sizes.

A single desktop-and-mobile check is not enough. Bounding-box values alone are not enough. Real screenshots and numerical checks catch different failures, so require both.

## 1. Prepare a realistic test state

Run the actual interface in a safe test environment. Populate the changed surface with representative content before testing, such as:

- long paragraphs, formatted text, and long field values;
- representative lists, cards, rows, and validation messages;
- enough items to approach expected limits;
- loading, empty, and error states when the change can affect them.

Do not validate only an empty or unusually clean page. Sparse content can hide clipping, wrapping failures, overlap, and unexpected blank areas.

## 2. Select the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages or interfaces expected to run on large displays.

When vertical layout matters, test at least two relevant heights:

- a short height of about 700 px;
- a tall height of about 1400 px or greater.

Include known target viewports when available. Explicitly test a very tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, bottom alignment, or related behavior.

Use a repeatable headless browser automation system selected for the project. Capture evidence from the rendered page rather than relying only on source inspection.

## 3. Capture and inspect screenshots

Capture screenshots at each relevant viewport and state. Use full-page screenshots when page length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect the affected component on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does this still match the intended design now that the component's role or layout has changed?

Give extra attention to edge-to-edge or full-bleed changes. Making a component flush on one edge can expose leftover margins or wrapper padding as visible background strips on another edge. Check every edge, not only the edge edited.

Reread the requested outcome after the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshot review. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the design should fit the viewport;
- no changed element overlaps neighboring content or its intended container;
- buttons, links, inputs, and other controls remain visible and usable;
- fixed or sticky interface elements do not hide essential content;
- cards, lists, and form controls stay within their intended bounds;
- prose retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap checks, compare relevant element rectangles with adjacent elements and container boundaries.

For prose-heavy pages, flag text that is too wide to read comfortably. A useful warning threshold is roughly 80 characters per line; reading-focused layouts commonly target about 60–70 characters per line.

## 5. Require both kinds of evidence

Automated measurements can miss visual defects, including exposed background strips, poor visual balance, and unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when visual review and all relevant programmatic checks pass.

## 6. Fix failures at the cause, then retest

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a viewport-specific cosmetic patch;
4. rerun the full relevant sweep, not only the viewport that failed.

If a fix makes one viewport correct but breaks another, step back and re-diagnose. The layout model is likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” State the widths, relevant heights or states, and checks actually completed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, say so clearly and do not represent the UI change as complete.

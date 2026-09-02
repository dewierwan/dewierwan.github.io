---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using real screenshots and programmatic layout checks. Fix every failure and rerun the relevant sweep before reporting the work as complete.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Treat even a small spacing, color, background, or wrapper change as potentially cross-viewport: it can alter wrapping, height, overflow, alignment, and visible backgrounds elsewhere.

A single desktop screenshot, a single mobile screenshot, or bounding-box measurements alone are not sufficient. Real screenshots and programmatic checks find different classes of defects; use both.

## 1. Prepare realistic test states

Run the real interface in an authorized test environment and populate the affected surface with representative content before testing. Use the minimum data needed to test layout, and avoid exposing unnecessary sensitive information in screenshots or reports.

Include relevant examples such as:

- long paragraphs, formatted text, and long field values;
- representative lists, cards, rows, and validation messages;
- realistic item counts, including content near expected limits;
- loading, empty, and error states when the change can affect them.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping failures, and unintended blank regions.

## 2. Select the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages, dashboards, or interfaces expected to be used on large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Also test any known target viewport supplied by the user or product requirements. Explicitly include a very tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, backgrounds, vertical padding, sticky footers, bottom alignment, or related layout behavior.

Use a repeatable headless browser automation capability selected for the project. Capture artifacts consistently enough that another reviewer can reproduce the sweep.

## 3. Capture and inspect screenshots

Capture real screenshots at every relevant viewport and test state. Use full-page screenshots when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect each changed component on all four sides:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does this match the intended design now that the component has its current role?

Pay special attention to full-bleed, edge-to-edge, or flush changes. Removing containment on one side can reveal leftover margins or wrapper padding on another side as a visible background strip. Check all edges, not only the edge edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshot review. At minimum, verify the checks relevant to the changed surface:

- no unintended horizontal overflow;
- no unintended vertical overflow when the design is meant to fit within the viewport;
- no changed element overlaps neighboring content, its intended container, or an essential fixed element;
- buttons, links, inputs, and other controls remain visible and usable;
- cards, lists, and form controls remain within intended bounds;
- fixed or sticky UI does not hide essential content;
- prose retains a readable line length.

For fit-to-viewport screens, compare document height to viewport height with a small rendering tolerance. For overlap detection, compare bounding rectangles of relevant adjacent elements, controls, and containers rather than assuming document order prevents collision.

For prose-heavy pages, estimate characters per line from rendered width and font size, or use another appropriate typography measurement. Flag text that is excessively wide; around 80 characters per line is a useful warning threshold, while reading-focused designs often target roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss exposed background strips, poor visual balance, and unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and the relevant programmatic checks pass. If a check is not applicable, record why rather than silently omitting it.

## 6. Fix failures at the cause and retest

If any viewport or realistic content state fails:

1. stop the completion, review, or release process;
2. identify the layout rule or component interaction causing the failure;
3. fix the underlying behavior rather than adding a cosmetic, viewport-specific patch;
4. rerun the complete relevant sweep, including the states that previously passed.

If a fix corrects one viewport but creates a failure at another, reconsider the diagnosis. The layout model is likely incomplete; do not stack patches until screenshots happen to look acceptable at selected sizes.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights and states, and the checks performed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, state that clearly and do not represent the UI change as complete.

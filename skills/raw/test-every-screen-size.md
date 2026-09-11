---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, tall, and target viewports using real screenshots and programmatic layout checks. Fix underlying failures and rerun the relevant sweep before marking the work ready.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, background, color, or typography edits: a local change can alter wrapping, height, overflow, alignment, or exposed backgrounds elsewhere.

A single screenshot and bounding-box measurements are not sufficient on their own. Real screenshots reveal visual defects that measurements miss; programmatic checks reveal off-screen or subtle defects that screenshots miss. A viewport passes only when both forms of evidence pass.

## 1. Prepare a safe, realistic test state

Run the interface in an authorized test environment. Use only the minimum relevant test data and avoid exposing sensitive personal information in screenshots, logs, or reports.

Populate changed surfaces with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative cards, rows, lists, validation messages, and controls;
- content counts near expected limits;
- loading, empty, and error states when the change can affect them.

Do not validate only empty or unusually clean states. Sparse content can hide clipping, overlap, wrapping failures, and unintended blank areas.

## 2. Choose the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages or interfaces expected to be used on large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Include any known target viewport supplied by the user or product requirements. Explicitly test a very tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable headless browser automation system or equivalent browser-testing capability selected for the project. Capture both full-page and viewport screenshots as appropriate:

- use full-page captures when page length and document flow matter;
- use visible-viewport captures when fixed, sticky, or viewport-height behavior matters.

## 3. Inspect screenshots on all axes

Capture real screenshots at every relevant viewport and state. Inspect the changed component and its surrounding layout on all four sides:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design after the component's role changed.

Pay special attention to full-bleed, edge-to-edge, or flush changes. Removing containment on one edge can expose old wrapper margin or padding on another edge as a visible background strip. Verify every edge, not only the edge directly edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the stylesheet or component logic appears correct.

## 4. Run programmatic checks at each relevant viewport

Run numerical checks alongside screenshot review. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is intended to fit within the viewport;
- no changed element overlaps adjacent content, its container, or essential fixed UI;
- buttons, links, inputs, and other interactive controls remain visible and usable;
- sticky or fixed elements do not hide essential content;
- cards, lists, and form controls remain within intended bounds;
- prose retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare the bounding rectangles of relevant elements with adjacent elements and container boundaries; do not assume every nearby element should never overlap, since intentional overlays exist.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line, while reading-focused content commonly targets roughly 60–70 characters per line.

## 5. Apply the evidence rule

Use both evidence types for every relevant viewport:

- **Screenshots** catch exposed background strips, poor visual balance, incorrect edge treatment, and unexpected empty regions.
- **Programmatic checks** catch off-screen overflow, clipped controls, hidden content, and small collisions that may be hard to notice visually.

Do not replace the sweep with only one desktop screenshot, one mobile screenshot, or only rectangle measurements.

## 6. Fix failures and rerun

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, including viewports that previously passed.

If a fix improves one viewport but breaks another, reconsider the diagnosis. The layout model or component constraints are likely incomplete. Do not leave a known failure for another person to discover.

## 7. Readiness gate and reporting

The change is ready only when all relevant viewport-state combinations have passing visual inspection and programmatic checks. If a viewport, state, or check remains unverified, state that clearly and do not present the change as complete.

Report concrete evidence rather than vague claims such as “works on mobile and desktop.” For example:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

Include large-display and target-viewport results when they were required. If a failure was found and corrected, report that the relevant sweep was rerun after the fix.

---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using real screenshots and programmatic layout checks. Fix and retest any failure before reporting completion, requesting review, or releasing.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Treat it as required even for a small spacing, color, background, or wrapper change: local edits can create overflow, blank regions, overlap, wrapping, or alignment problems at sizes that were not directly tested.

A single desktop screenshot, a single mobile screenshot, or bounding-box measurements alone are not sufficient. Screenshots reveal visual defects that numbers may miss; programmatic checks reveal overflow and collisions that may be easy to overlook visually. A viewport passes only when both forms of evidence pass.

## 1. Prepare realistic page states

Run the actual interface in an authorized test environment using a repeatable browser automation tool or equivalent testing system.

Before capturing evidence, populate affected surfaces with representative content. Use the minimum test data needed and avoid exposing personal or sensitive information. Include, as relevant:

- long paragraphs, formatted text, long labels, and long field values;
- representative cards, lists, rows, messages, and item counts;
- validation, loading, empty, and error states when the change can affect them;
- content near expected size limits.

Do not validate only an empty or unusually sparse state. Empty pages can conceal clipping, wrapping, overlap, and unintended blank space.

## 2. Select the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages or interfaces expected to be used on large displays.

When vertical layout matters, test at least two heights for each relevant width:

- a short viewport, around 700 px high;
- a tall viewport, around 1400 px high or greater.

Also test any known target viewport supplied by the user or product requirements. Explicitly include a very tall viewport, such as 1800 px, when changing viewport-height rules, flexible page shells, backgrounds, vertical padding, sticky footers, bottom alignment, or similar layout behavior.

Run the browser automation headlessly where practical so the test is repeatable and does not depend on a local interactive browser state.

## 3. Capture and inspect screenshots

Capture real screenshots at every relevant viewport and content state. Use full-page screenshots when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect each affected component on all four sides:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: **Does this match the intended design now that this component has changed role or size?**

Take special care with full-bleed, edge-to-edge, or flush layouts. When a formerly contained component becomes flush with an edge, leftover margins or wrapper padding can become visible as unintended background strips. Checking only the edited edge is not enough.

Reread the original requested outcome after implementing the change. Compare that outcome directly with the screenshots rather than relying on the apparent logic of the CSS.

## 4. Run programmatic checks at each relevant viewport

Run numerical checks alongside the screenshot sweep. Adapt selectors and thresholds to the interface, but check at least the following:

- no unintended horizontal scrolling or overflow;
- no unintended vertical overflow when the design is meant to fit the viewport;
- no changed element overlaps adjacent content, its container, or a following section;
- buttons, links, inputs, and other interactive controls remain visible and usable;
- cards, lists, and form controls remain within intended bounds;
- fixed and sticky elements do not obscure essential content;
- prose remains within a readable line length.

For a fit-to-viewport page, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare bounding rectangles for relevant neighboring elements and their containers.

For prose-heavy screens, flag lines that are excessively wide. A useful warning threshold is approximately 80 characters per line; reading-focused layouts commonly target roughly 60–70 characters per line.

## 5. Apply the evidence rule

Do not treat numerical checks as a substitute for visual review. Measurements may not reveal poor visual balance, exposed background strips, or unexpected empty regions.

Do not treat screenshots as a substitute for numerical checks. A screenshot can miss off-screen overflow, partially hidden controls, and small collisions.

A viewport and state pass only when:

- the screenshot matches the intended result; and
- all relevant programmatic checks pass.

## 6. Fix failures and rerun

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the underlying layout rule causing the failure;
3. fix the layout behavior rather than applying a narrow cosmetic patch;
4. rerun the complete relevant viewport sweep and checks.

If a change fixes one viewport but creates a failure at another, reconsider the diagnosis. The layout model is likely incomplete; do not continue by stacking viewport-specific patches.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights or states, and the checks performed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport, height, state, screenshot, or check remains unverified, state that clearly and do not represent the UI change as complete.

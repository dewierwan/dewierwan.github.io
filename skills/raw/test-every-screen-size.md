---
name: test-every-screen-size
description: Verify every UI or CSS change across representative narrow, wide, short, tall, and content-heavy states using both screenshots and programmatic layout checks, then fix and retest every failure before completion.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to a small spacing, background, or typography edit: a local change can alter wrapping, height, overflow, alignment, or exposed page backgrounds elsewhere.

A bounding-box check alone is not enough. A single desktop screenshot and a single mobile screenshot are not enough. Real screenshots and programmatic checks find different failure types, so require both.

## 1. Prepare a realistic test state

Run the interface in an authorized test environment using only the minimum test data needed. Populate the changed surface with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative cards, rows, lists, and item counts;
- form validation messages and error text where relevant;
- loading, empty, and error states when the change affects them;
- content close to expected maximum length or density.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, unexpected whitespace, and wrapping failures.

## 2. Define the viewport sweep

Test these baseline viewport widths:

- 320 px;
- 480 px;
- 600 px;
- 720 px;
- 1024 px;
- 1440 px.

Add a large desktop width, such as 1920 px, for landing pages, dashboards, or interfaces expected to be used on large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short viewport, around 700 px high;
- a tall viewport, around 1400 px high or greater.

Also test any viewport known to matter for the intended audience or environment. Explicitly include a very tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable browser automation system chosen for the project. Run it headlessly unless visual browser interaction is specifically needed for diagnosis.

## 3. Capture real screenshots

Capture screenshots at every relevant viewport and state. Use full-page screenshots when page length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect the affected area on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does it match the design intent now that this element has changed role or size?

Be especially careful with edge-to-edge or full-bleed changes. Making a component flush on one edge can expose leftover margins or wrapper padding on another edge as visible background strips. Check every edge, not only the edge edited.

Reread the original requested outcome after making the change. Compare that goal directly with the screenshots. Do not accept a result only because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify the following where applicable:

- no unintended horizontal overflow;
- no unintended vertical overflow for screens intended to fit within the viewport;
- no changed element overlaps neighboring content or escapes its intended container;
- buttons, links, fields, and other interactive controls remain visible and usable;
- cards, lists, and form controls stay within intended bounds;
- fixed or sticky UI does not hide essential content;
- readable text does not become excessively wide.

For a page intended to fit the viewport, compare document height with viewport height and allow only a small rendering tolerance. For overlap checks, compare bounding rectangles of relevant neighboring elements, including their top, bottom, left, and right edges.

For prose-heavy pages, flag overly wide text measures. A useful warning threshold is roughly 80 characters per line; reading-focused layouts commonly target about 60–70 characters per line.

## 5. Require both kinds of evidence

A viewport passes only when both of these pass:

1. **Visual review:** screenshots show no unintended blank strips, poor alignment, clipping, imbalance, or exposed wrapper background.
2. **Programmatic checks:** measurements show no unintended overflow, collision, hidden control, or out-of-bounds layout.

Measurements can miss visually obvious defects. Screenshots can miss subtle off-screen overflow, small collisions, and inaccessible controls. Neither replaces the other.

## 6. Fix failures at the cause, then retest

If any viewport or realistic content state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying layout behavior rather than applying a one-viewport cosmetic patch;
4. rerun the complete relevant sweep, not only the viewport that first exposed the problem.

If a fix improves one viewport but breaks another, reconsider the diagnosis. The layout model is incomplete; do not stack compensating patches until the screenshots appear acceptable.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the widths, relevant heights, realistic states, and checks actually completed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, say so clearly. Do not represent the UI change as complete until the required relevant sweep has passed.

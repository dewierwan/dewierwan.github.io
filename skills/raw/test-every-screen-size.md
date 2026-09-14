---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using realistic content, screenshots, and programmatic layout checks before declaring the work complete.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, color, background, or typography edits: a local change can affect wrapping, height, overflow, alignment, and backgrounds elsewhere.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Real screenshots and numerical checks catch different failures, so require both.

## 1. Prepare realistic page states

Run the real interface in an appropriate test environment. Populate changed surfaces with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative cards, rows, lists, and item counts;
- validation messages and controls in their active states;
- loading, empty, and error states when the change can affect them.

Do not validate only an empty or unusually clean page. Sparse content often hides clipping, overlap, unexpected whitespace, and wrapping defects.

## 2. Select the viewport sweep

Test these baseline viewport widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages or interfaces intended for large displays.

When vertical layout matters, test at least two heights at every relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Include known target viewports when available. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable browser automation system selected for the project. Run it headlessly unless interactive inspection is specifically needed.

## 3. Capture and inspect screenshots

Capture real screenshots for every relevant viewport and state. Use full-page screenshots when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect the changed component and its immediate surroundings on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does it match the design intent now that the element's role or layout has changed?

Pay special attention to edge-to-edge or full-bleed changes. A component made flush with an edge can reveal previously hidden margins or wrapper padding as visible background strips. Check every edge, not only the edge edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. Adapt selectors and tolerances to the interface, but verify at least the following:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is intended to fit the viewport;
- no changed element overlaps neighboring content or escapes its intended container;
- buttons, links, inputs, and other controls remain visible, reachable, and usable;
- fixed or sticky UI does not cover essential content;
- cards, lists, and form controls remain within intended bounds;
- prose retains a readable line length.

For a fit-to-viewport screen, compare document height with viewport height and allow only a small rendering tolerance. For example:

```js
const fitsViewport = document.documentElement.scrollHeight <= window.innerHeight + 1;
```

For overlap checks, compare bounding rectangles for relevant adjacent elements, accounting for intentional overlap where the design requires it. Do not treat a general geometric scan as proof of correctness; it must be paired with screenshot review.

For prose-heavy pages, estimate line length from rendered width and font size or use a more direct text-measurement method. Flag text that approaches or exceeds roughly 80 characters per line. Reading-focused designs commonly target about 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visual defects such as exposed background strips, poor visual balance, or unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both of these pass:

1. visual inspection of the screenshots; and
2. applicable programmatic layout and usability checks.

## 6. Fix failures and rerun the sweep

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the underlying layout rule causing the failure;
3. fix the behavior rather than adding a narrow viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the size that first exposed the problem.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights and states, and the checks performed.

| Report item | Record |
|---|---|
| Viewports tested | [For example: 320, 480, 600, 720, 1024, 1440, and 1920 px] |
| Height coverage | [Short, tall, and any known target viewport] |
| States tested | [Representative content, validation, loading, empty, or error states] |
| Evidence | [Screenshots reviewed and programmatic checks passed] |
| Exceptions | [Any unverified viewport, state, or known limitation] |

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, say so clearly and do not represent the UI change as complete.

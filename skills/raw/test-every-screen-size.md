---
name: test-every-screen-size
description: Verify every UI or CSS change across representative widths, heights, content states, screenshots, and layout checks before reporting it complete.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to a one-line spacing, color, or background change: a local edit can alter wrapping, height, overflow, alignment, or visible backgrounds elsewhere.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Real screenshots and programmatic checks catch different failures, so require both.

## Why this is required

A layout can appear correct at one size while failing at another:

- viewport-height rules can create blank space on unusually tall screens;
- a split layout can fail at intermediate widths even when narrow and wide layouts pass;
- making a surface full-bleed can reveal leftover margins or wrapper padding as visible strips;
- empty states can hide collisions, clipping, and overflow that realistic content exposes.

Treat screenshots as visual ground truth and layout measurements as complementary evidence.

## 1. Prepare representative states

Run the interface in a safe test environment and populate the affected surface with realistic content before testing. Use the minimum test data needed for the layout; do not include unrelated or sensitive personal information.

Include, when relevant:

- long paragraphs, formatted content, long field values, and long unbroken strings;
- representative lists, cards, rows, and item counts;
- validation messages, helper text, and error states;
- loading and empty states when the change affects them;
- content near expected limits, such as a long output block or a dense card list.

Do not validate only an empty or unusually clean state. Sparse content can conceal clipping, overlap, poor wrapping, and unintended blank regions.

## 2. Select the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages, large-display workflows, or layouts expected to expand widely.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Also test any known target viewport supplied by the user or product requirements. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable method that can set exact viewport dimensions, load the intended page state, capture screenshots, and collect layout measurements. Prefer a non-interactive run for reproducibility unless visual debugging requires direct interaction.

## 3. Capture and inspect screenshots

Capture real screenshots at every relevant viewport and state. Use full-page screenshots when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect the changed component and its immediate surroundings on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does this match the intended design now that the element's role has changed?

Pay special attention to edge-to-edge or full-bleed changes. A component that becomes flush with one edge may expose old margins or wrapper padding on another edge as a visible background strip. Check every edge, not just the edge edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS seems logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow where the screen is intended to fit the viewport;
- no changed element overlaps adjacent content, its container, or essential controls;
- buttons, links, inputs, and other interactive controls remain visible and usable;
- fixed or sticky UI does not hide essential content;
- cards, lists, and form controls remain within intended bounds;
- body text retains a readable line length.

For a fit-to-viewport design, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare bounding rectangles of relevant siblings, containers, and controls rather than relying on a single page-wide rule.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is approximately 80 characters per line; reading-focused designs commonly target roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visible defects such as exposed background strips, poor visual balance, and unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both of these pass:

- visual inspection of the applicable screenshot; and
- relevant programmatic layout and usability checks.

## 6. Fix failures and rerun

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a viewport-specific cosmetic patch;
4. rerun the full relevant sweep, not only the failing size.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is incomplete; do not keep layering patches until individual screenshots happen to pass.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights and states, and the checks performed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, say so clearly and do not represent the UI change as complete.

---
name: test-every-screen-size
description: Check every UI or CSS change across narrow, wide, short, and tall screens with screenshots and layout checks before calling it done. Use before shipping any front-end change.
---

# Test every screen size

Run this workflow after any UI, visual, or CSS change and before requesting review, publishing, or calling the work complete. Small edits to spacing, backgrounds, or sizing can create overflow, blank areas, wrapping problems, or collisions at sizes that were not inspected.

A layout passes only when **both** screenshots and programmatic checks pass. Measurements can miss visual defects; screenshots can miss off-screen overflow or unusable controls.

## 1. Prepare a representative state

Use an authorized test environment and test only the minimum data needed to reproduce normal use. Populate the changed surface with realistic content, such as long text, representative lists or cards, field values, and validation messages. Include loading, empty, or error states when the change affects them.

Do not test only an empty or unusually sparse page. Sparse states often conceal clipping, overlap, and unwanted blank space.

## 2. Select the viewport sweep

Use a repeatable browser-testing system. Start with these widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a wide desktop size, such as 1920 px, when large displays are a supported use case. Include any known target viewport.

When vertical behavior matters, test both a short and tall height, for example about 700 px and 1400 px or more. Explicitly include a very tall viewport for changes involving viewport-height sizing, flexible page shells, backgrounds, vertical padding, sticky footers, or bottom alignment.

## 3. Capture and inspect screenshots

Capture screenshots for each relevant viewport and state. Use visible-viewport screenshots for sticky, fixed, and viewport-height behavior; use full-page screenshots when page flow, backgrounds, or total page length matter.

Inspect the changed surface on all four sides: top, right, bottom, and left. Compare the result with the requested outcome, not merely with the edited CSS.

Give extra attention to full-bleed or edge-to-edge changes. Removing containment on one edge can reveal leftover wrapper margin or padding as an unintended strip on another edge.

## 4. Run programmatic layout checks

At every relevant viewport, verify that:

- there is no unintended horizontal overflow;
- viewport-fitting screens do not have unintended vertical overflow, allowing a small rendering tolerance;
- changed elements do not overlap adjacent content or escape their intended containers;
- buttons, links, fields, cards, and lists remain visible and usable;
- fixed or sticky elements do not hide required content; and
- prose remains readable rather than becoming excessively wide.

For prose, use an approximate warning threshold of 80 characters per line; reading-focused layouts commonly target about 60–70 characters per line. Check relevant bounding rectangles for overlaps and compare document height with viewport height where fitting the viewport is intended.

## 5. Resolve failures and retest

If any viewport or state fails, stop the completion process. Find the underlying layout rule, fix that behavior, and rerun the relevant sweep. Do not add a size-specific patch merely to make one screenshot pass.

If a fix improves one size but breaks another, revisit the diagnosis. The layout model or component constraints are incomplete.

## 6. Readiness gate and report

Do not report only that the interface works on “mobile and desktop.” State what was tested and what passed. For example:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall heights where relevant; screenshots and layout checks found no unintended overflow or overlap; controls remain usable.

If a viewport, state, or check was not run, state that clearly and do not represent the UI change as fully verified.

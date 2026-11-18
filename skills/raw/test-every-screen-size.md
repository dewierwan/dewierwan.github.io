---
name: test-every-screen-size
description: Checks UI or CSS changes across narrow, wide, short, and tall screens with screenshots and layout checks. Use when shipping a front-end fix or asking 'does this work on mobile?'
---

# Test every screen size

Run this workflow after any UI, visual, or CSS change and before requesting review, publishing, or calling the work complete. Small edits to spacing, backgrounds, or sizing can create overflow, blank areas, wrapping problems, or collisions at sizes that were not inspected.

## Quick version

- Before calling a UI change done, view it at several widths, from a very narrow phone up to a wide desktop, using your browser's responsive or device mode. Also try a short and a very tall window height.
- Fill the screen with realistic content first: long text, a full list, typed-in form values, error messages. Empty pages hide bugs.
- At each size, look at all four sides of the changed element, not just the side you edited. Watch for leftover strips of margin or padding.
- Paste screenshots into your AI assistant and ask it to check for overflow, overlap, clipped or hidden controls, blank areas, and overly wide text, compared against your original goal.
- If one size breaks, fix the underlying layout rule and recheck every size. Do not patch only the size that failed.
- Report the exact sizes and checks that passed, not "looks good on mobile and desktop."

A layout passes only when **both** screenshots and programmatic checks pass. Measurements can miss visual defects; screenshots can miss off-screen overflow or unusable controls.

## 1. Prepare a representative state

Use an authorized test environment and only the minimum data needed to reproduce normal use. Populate the changed surface with realistic content, such as long text, representative lists or cards, field values, and validation messages. Include loading, empty, or error states when the change affects them.

Do not test only an empty or unusually sparse page. Sparse states often conceal clipping, overlap, and unwanted blank space.

## 2. Select the viewport sweep

Use a repeatable browser-testing setup. Choose a set of widths that covers each layout range you support. These starting values are adjustable defaults:

| Range | Example width |
| --- | --- |
| Very narrow phone | about 320 px |
| Large phone | about 480 px |
| Small tablet or split-screen window | about 600 to 720 px |
| Tablet landscape or small laptop | about 1024 px |
| Standard desktop | about 1440 px |

Add a wide desktop size when large displays are a supported use case, for example on landing pages. Include any known target viewport, especially the one the person requesting the change actually uses. A large, high-resolution monitor in a full-screen browser can have a much taller viewport than common test presets, so ask or check.

When vertical behavior matters, test both a short and a tall height at each width. A tall, narrow browser window exposes different bugs than a short, narrow phone. Explicitly include a very tall viewport, well beyond common presets, for changes involving viewport-height sizing, flexible page shells, backgrounds, vertical padding, sticky footers, or bottom alignment.

## 3. Capture and inspect screenshots

Capture screenshots for each relevant viewport and state, and actually look at them. Use visible-viewport screenshots for sticky, fixed, and viewport-height behavior; use full-page screenshots when page flow, backgrounds, or total page length matter.

Inspect the changed surface on all four sides: top, right, bottom, and left. For each side, ask whether it still matches the design intent now that the element's role may have changed.

Give extra attention to full-bleed or edge-to-edge changes. Full-bleed usually means flush on every side, not only the one you changed. Removing containment on one edge can reveal leftover wrapper margin or padding as an unintended strip on another edge.

Then reread the original request in its own words and compare it with the screenshots. Compare the result with the requested outcome, not merely with the edited CSS. Do not trust your own pass without this cross-check.

## 4. Run programmatic layout checks

At every relevant viewport, verify that:

- there is no unintended horizontal overflow;
- viewport-fitting screens do not have unintended vertical overflow, allowing a small rendering tolerance (for example 1 px);
- changed elements do not overlap adjacent content or escape their intended containers;
- buttons, links, fields, cards, and lists remain visible and usable;
- fixed or sticky elements do not hide required content; and
- prose remains readable rather than becoming excessively wide.

For prose, use an approximate warning threshold of about 80 characters per line; reading-focused layouts commonly target around 60 to 70 characters per line. Adjust these to your design system. Check relevant bounding rectangles for overlaps and compare document height with viewport height where fitting the viewport is intended.

Numbers alone can mislead: a measurement may say a gap is gone while a screenshot shows the problem simply moved somewhere else. Use both.

## 5. Resolve failures and retest

If any viewport or state fails, stop the completion process. Fix it before claiming done; do not ship and let someone else find it. Find the underlying layout rule, fix that behavior, and rerun the relevant sweep. Do not add a size-specific patch merely to make one screenshot pass.

If a fix improves one size but breaks another, revisit the diagnosis. The layout model or component constraints are incomplete.

## 6. Readiness gate and report

Do not report only that the interface works on "mobile and desktop." State what was tested and what passed. For example:

> Verified at five widths from very narrow phone to standard desktop; tested short and tall heights where relevant, including a very tall full-screen height; screenshots and layout checks found no unintended overflow or overlap; controls remain usable.

If a viewport, state, or check was not run, state that clearly and do not represent the UI change as fully verified.

## 7. Worked example (fictional)

A developer at the fictional Juniper Row Books changes a newsletter signup card to stretch edge to edge on phones. They check one phone width, see the card touching the left and right edges, and are ready to ship.

Running the sweep instead:

| Viewport | Screenshot finding | Programmatic finding |
| --- | --- | --- |
| Narrow phone, short height | Card flush left and right; a pale strip below the card | No horizontal overflow |
| Small tablet, tall height | Same bottom strip, now more visible | Card bottom ends well above the footer |
| Desktop, very tall height | Large blank area below the page content | Page shell shorter than viewport |

Diagnosis: the wrapper kept a bottom margin meant for a contained card, and the page shell did not fill tall viewports. The fix removes the leftover margin and corrects the shell's height rule once, rather than adding per-size overrides. The sweep is rerun and reported with the exact sizes.

## Optional extras

**Automating the sweep.** With an agent that can run code, use a headless browser-automation tool to loop over a list of width and height pairs, load the page, inject realistic content, save screenshots, and run checks. Use a tool already available in your environment rather than installing one per project, and run it headless.

**Checks to script at each viewport (adapt to your tool):**

- *Fits the viewport:* the document's total scroll height is no more than the window's inner height plus a small tolerance.
- *No horizontal scroll:* the document's scroll width is no more than the window's inner width plus a small tolerance.
- *Prose width:* for each body paragraph, divide its rendered width by roughly half its font size to estimate characters per line, then flag any paragraph above your threshold (about 80 by default). The one-half factor is a rough average character width; adjust it for your typeface.

**Overlap check.** For sibling elements in the changed area, flag any case where one element's bottom edge is greater than the next element's top edge, unless overlap is intended.

**Saved sweep config.** Keep your chosen widths, heights, and content fixtures in one file so every change is tested the same way.

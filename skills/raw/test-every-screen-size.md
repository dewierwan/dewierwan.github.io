---
name: test-every-screen-size
description: Verify every UI or CSS change across representative narrow, wide, short, and tall viewports using screenshots and programmatic layout checks. Fix and retest every failure before reporting the change as complete.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, color, or background changes: a local edit can alter wrapping, height, overflow, alignment, or visible backgrounds at other screen sizes.

A bounding-box check alone is not enough. A single desktop and mobile screenshot are not enough. Real screenshots and numerical checks catch different failures, so use both.

## 1. Prepare realistic test states

Run the real interface in an appropriate test environment. Populate the changed surface with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative lists, cards, rows, and validation messages;
- realistic item counts or content near expected limits;
- loading, empty, and error states when the change affects them.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping problems, and unintended blank space.

## 2. Choose the viewport sweep

Use these baseline widths unless the product's supported-device requirements call for a different set:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, for landing pages or interfaces likely to be used on large displays. Include any required customer, device, embedded-window, or product-specific viewport as an additional test case.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

For changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment, include a very tall viewport. Use a height representative of the largest expected display or browser window; 1600–1800 px is a useful general test range.

Use a repeatable browser automation or browser-testing system available to the project. Run it headlessly when an interactive display is unnecessary.

## 3. Capture and inspect screenshots

Capture real screenshots at every relevant viewport and state. Use full-page screenshots when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect every affected component on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design now that the component has changed role or size.

Pay special attention to edge-to-edge or full-bleed changes. Making a component flush on one edge can expose leftover wrapper margins or padding as visible background strips on another edge. Check every edge, not only the edge edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is intended to fit the viewport;
- no changed element overlaps neighboring content or its intended container;
- buttons, links, and fields remain visible and usable;
- fixed or sticky UI does not hide essential content;
- cards, lists, and form controls remain within intended bounds;
- body text retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant element rectangles with adjacent elements and container boundaries. Check only relationships that are expected to be non-overlapping; intentionally layered elements need an explicit expected relationship.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line; reading-focused designs commonly target roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visual defects such as exposed background strips, poor balance, or unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and the relevant programmatic checks pass.

## 6. Fix failures and rerun the sweep

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the failing size.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights or states, and checks performed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, say so clearly and do not represent the UI change as complete.

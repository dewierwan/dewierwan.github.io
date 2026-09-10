---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using real screenshots and programmatic layout checks. Treat a change as complete only after failures are fixed and the relevant sweep is rerun.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to a small spacing, color, or background edit: a local change can alter wrapping, height, overflow, alignment, or backgrounds elsewhere.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Use real screenshots and numerical checks together.

## 1. Prepare realistic page states

Run the real interface in an authorized test environment. Populate the changed surface with representative content before testing:

- long paragraphs, formatted text, long field values, and validation messages;
- representative cards, rows, lists, and item counts;
- loading, empty, and error states when the change can affect them;
- realistic data that exercises wrapping, scrolling, and vertical growth.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping defects, and unintended blank space. Use only the minimum test data needed, and avoid exposing unrelated personal or sensitive information in screenshots or reports.

## 2. Choose the viewport sweep

Test these baseline widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, when the interface is expected to be used on large displays.

When vertical layout matters, test at least two heights at each relevant width:

- a short height around 700 px;
- a tall height around 1400 px or greater.

Also include known target viewports when they are available. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Use a repeatable browser-testing system selected for the project. Run it headlessly unless interactive inspection is necessary.

| Test condition | Minimum expectation |
|---|---|
| Standard responsive layout | Baseline width sweep |
| Vertical or viewport-height behavior | Relevant widths at short and tall heights |
| Large-display experience | Include a large desktop width |
| Known user or device target | Include that viewport when practical |

## 3. Capture and inspect screenshots

Capture real screenshots at every relevant viewport and state. Use full-page screenshots when page length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect every changed component on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design now that the component's role may have changed.

Pay special attention to edge-to-edge or full-bleed changes. A component made flush with an edge may expose leftover wrapper margins or padding as visible background strips. Check every edge, not only the edge edited.

Reread the original requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is meant to fit the viewport;
- no changed element overlaps neighboring content or its intended container;
- buttons, links, and fields remain visible and usable;
- fixed or sticky UI does not hide essential content;
- cards, lists, and form controls remain within intended bounds;
- body text retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant bounding rectangles with adjacent elements and container boundaries. Check visibility and usability through the project’s chosen automation capability, such as verifying that controls have non-zero visible bounds and can receive an intended interaction.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line; reading-focused designs commonly use a narrower target of roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visual defects such as exposed background strips, poor balance, or unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and the relevant programmatic checks pass.

## 6. Fix failures and rerun the sweep

If any viewport or realistic state fails:

1. stop the completion or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the failing size.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is likely incomplete. Do not ship a known failure for another person to discover unless an authorized decision explicitly accepts and documents the limitation.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights or states, and the checks performed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, say so clearly and do not represent the UI change as complete.

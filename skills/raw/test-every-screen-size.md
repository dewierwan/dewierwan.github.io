---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using realistic content, screenshots, and layout checks.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it to small edits too: a spacing, background, or sizing change can alter wrapping, overflow, alignment, page height, or visible backgrounds at other viewport sizes.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Treat real screenshots and programmatic checks as complementary evidence: each catches defects the other can miss.

## 1. Prepare realistic test states

Run the real interface in an authorized test environment. Populate the affected surfaces with representative content before testing:

- long paragraphs, formatted text, long labels, and long field values;
- representative cards, lists, rows, and realistic item counts;
- validation messages and other content that changes component height;
- loading, empty, and error states when the change can affect them.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping, and unintended blank space.

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

- a short height of about 700 px;
- a tall height of about 1400 px or more.

Include the actual target viewport when known. Explicitly test a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment. Tall windows can reveal trailing blank areas and incorrect minimum-height behavior that ordinary screenshots do not show.

Use a repeatable headless browser automation capability selected for the project. Capture screenshots from the rendered interface, not from a design approximation or geometry output.

## 3. Capture and inspect screenshots

Capture screenshots for every relevant viewport and state. Use both forms when appropriate:

- **Visible-viewport screenshots** for fixed, sticky, viewport-height, and bottom-alignment behavior.
- **Full-page screenshots** for page length, section transitions, and long-content behavior.

Inspect the changed component and its surrounding layout on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does it now match the design intent, considering the component's new role?

Pay special attention to edge-to-edge or full-bleed changes. When a formerly contained component becomes flush with a viewport edge, leftover margins or wrapper padding may become visible as unwanted background strips. Check all edges, not only the edge changed in code.

Reread the requested outcome after making the change and compare it directly with the screenshots. Do not accept a result merely because the stylesheet appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshot inspection. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the design is intended to fit the viewport;
- no changed element overlaps neighboring content, its container, or important fixed UI;
- buttons, links, and fields remain visible and operable;
- cards, lists, and form controls remain within intended bounds;
- fixed or sticky UI does not conceal essential content;
- body text retains a readable line length.

For a fit-to-viewport surface, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant element bounding rectangles with adjacent elements and container boundaries. Check the actual elements that can collide rather than assuming a generic page-level test can detect every relationship.

For prose-heavy pages, flag excessively wide text measures. A broad warning threshold is about 80 characters per line; reading-focused layouts commonly target roughly 60–70 characters per line.

## 5. Require both forms of evidence

A viewport passes only when both of these pass:

1. **Visual evidence:** screenshots show no exposed background strips, poor spacing, unexpected empty regions, clipping, or visual imbalance.
2. **Programmatic evidence:** relevant overflow, bounds, overlap, and usability checks pass.

Measurements can miss visible design defects. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions. Neither replaces the other.

## 6. Fix failures and rerun

If any viewport or realistic state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior rather than adding a size-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the viewport where the defect appeared.

If a fix makes one viewport correct but introduces a failure at another, step back and reassess the layout model. The diagnosis is incomplete; do not accumulate patches until screenshots happen to look acceptable.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” State which widths, heights, states, and checks were completed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If a viewport or state remains unverified, say so clearly. Do not represent the UI change as complete until every relevant sweep result has passed.

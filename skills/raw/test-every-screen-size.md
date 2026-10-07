---
name: test-every-screen-size
description: Verify UI and CSS changes across representative widths, heights, realistic content states, screenshots, and layout checks before release.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to a small spacing, color, or background adjustment: a local edit can change wrapping, overflow, height, alignment, or visible backgrounds elsewhere.

A single viewport, a bounding-box measurement, or one desktop and one mobile screenshot is not enough. Combine real screenshots with programmatic layout checks.

## 1. Define a representative test matrix

Choose viewports based on the product’s supported devices, analytics, design breakpoints, and known user environments. If no project-specific matrix exists, use this practical starting set of widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large width, such as 1920 px, when large displays are in scope. Include any reported or contractually supported viewport that differs from these defaults.

When vertical layout matters, test both a short and a tall height at relevant widths. Broad defaults are about 700 px for short and 1400 px or more for tall. Include an especially tall viewport—for example, 1800 px—when changing viewport-height rules, flexible page shells, backgrounds, vertical spacing, sticky footers, or bottom alignment.

Use a repeatable browser automation or testing capability selected by the project. Run it in a consistent non-interactive mode when possible.

## 2. Prepare realistic page states

Test the real interface in an authorized environment. Populate the affected area with representative content before capture:

- long paragraphs, formatted content, and long field values;
- realistic lists, cards, rows, and validation messages;
- typical and near-limit item counts;
- loading, empty, and error states when the change can affect them.

Do not validate only an empty or unusually sparse state. Sparse content often hides clipping, overlap, wrapping, and unintended blank space.

## 3. Capture and inspect screenshots

Capture screenshots at each relevant viewport and state. Use full-page captures when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect every changed component on all four sides:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design after the component changed role, size, or containment.

Give extra attention to full-bleed or edge-to-edge changes. Removing containment on one side can expose remaining margins or wrapper padding on another side as visible background strips. Check every edge, not only the edge edited.

Reread the requested outcome after making the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow when the screen is meant to fit the viewport;
- no changed element overlaps neighboring content or its intended container;
- buttons, links, and fields remain visible and operable;
- fixed or sticky UI does not obscure essential content;
- cards, lists, and controls remain within intended bounds;
- prose retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height while allowing a small rendering tolerance. For overlap detection, compare relevant element rectangles with adjacent elements and container boundaries. Check interactive targets themselves, not only their parent containers.

For prose-heavy pages, flag excessively wide text measures. A useful warning threshold is roughly 80 characters per line; reading-focused layouts commonly target about 60–70 characters per line.

## 5. Require both forms of evidence

Measurements can miss visible defects such as exposed background strips, poor visual balance, and unexpected empty regions. Screenshots can miss off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and relevant programmatic checks pass.

## 6. Fix failures and rerun

If any viewport or realistic state fails:

1. stop completion, review, publication, or release;
2. identify the layout rule causing the failure;
3. fix the underlying layout behavior rather than adding a narrow viewport-specific patch;
4. rerun the complete relevant sweep, not only the viewport that failed.

If a change corrects one viewport but creates a defect at another, reconsider the diagnosis. The layout model or design constraint is likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Report the tested widths, relevant heights and states, and checks performed.

Use a concise report such as:

> Verified across the project viewport matrix, including narrow, medium, and wide widths; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any viewport or state remains unverified, say so clearly. Do not represent the UI change as complete until required checks pass or the remaining limitation is explicitly accepted by the appropriate project owner.

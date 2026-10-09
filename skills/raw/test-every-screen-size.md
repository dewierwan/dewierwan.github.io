---
name: test-every-screen-size
description: Verify UI and CSS changes across representative widths, heights, content states, and target devices using screenshots plus programmatic layout checks before release.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, color, or background edits: a local rule can change wrapping, height, overflow, alignment, or backgrounds elsewhere.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Use real screenshots and numerical checks together.

## 1. Define the test scope

Choose viewports based on the product’s supported devices, analytics, design requirements, and the changed layout behavior. If no project-specific viewport matrix exists, use this broadly useful baseline:

- narrow: 320 px and 480 px;
- intermediate: 600 px and 720 px;
- desktop: 1024 px and 1440 px;
- large desktop: 1920 px when large displays are a supported or likely use case.

When vertical layout matters, test both a short viewport (about 700 px tall) and a tall viewport (about 1400 px or taller) at each relevant width. Include an especially tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment.

Also test any explicitly supported device size or viewport named in the task. Treat the baseline as a default starting point, not a substitute for product requirements.

## 2. Prepare realistic page states

Run the real interface in an appropriate test environment. Populate the changed surface with representative content before testing:

- long paragraphs, formatted text, and long field values;
- representative lists, cards, rows, and validation messages;
- realistic item counts and content near expected limits;
- loading, empty, and error states when the change affects them.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping, and unintended blank space.

## 3. Capture and inspect screenshots

Use a repeatable browser-testing system, preferably headless automation, to capture screenshots at every relevant viewport and state. Use full-page screenshots when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect each changed component on all four sides:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask whether it matches the intended design now that the component’s role or size has changed. Pay particular attention to edge-to-edge or full-bleed changes: removing containment can expose leftover wrapper margin or padding as visible background strips on an untouched edge.

Reread the requested outcome after the change, then compare it directly with the screenshots. Do not accept a result merely because the CSS appears logically correct.

## 4. Run programmatic checks

Run numerical checks alongside screenshots at each relevant viewport. At minimum, verify:

- no unintended horizontal overflow;
- no unintended vertical overflow where the screen is intended to fit the viewport;
- no changed element overlaps neighboring content or its intended container;
- buttons, links, and fields remain visible and operable;
- fixed or sticky UI does not hide essential content;
- cards, lists, and controls remain within intended bounds;
- prose retains a readable line length.

For fit-to-viewport screens, compare document height with viewport height and allow only a small rendering tolerance. For overlap detection, compare relevant bounding rectangles with adjacent elements and container boundaries rather than assuming every stacked element should never intersect.

For prose-heavy pages, flag overly wide text measures. About 80 characters per line is a useful warning threshold; reading-focused layouts commonly target roughly 60–70 characters per line.

## 5. Require both forms of evidence

Automated measurements can miss visible defects such as exposed background strips, poor visual balance, and unexpected empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when both visual inspection and the relevant programmatic checks pass.

## 6. Fix failures and rerun

If any viewport or realistic state fails:

1. stop the completion or release process;
2. identify the layout rule causing the failure;
3. fix the underlying behavior instead of adding a viewport-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the failing size.

If a fix makes one viewport correct but breaks another, reconsider the diagnosis. The layout model or component constraints are likely incomplete.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” Record the tested widths, relevant heights and states, and checks performed.

Use a concise report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall viewport clean.

If any required viewport or state remains unverified, say so clearly and do not represent the UI change as complete.

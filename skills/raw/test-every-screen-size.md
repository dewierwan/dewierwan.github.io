---
name: test-every-screen-size
description: Verify every UI and CSS change across a configurable set of narrow, wide, short, and tall viewports using screenshots and programmatic layout checks. Fix underlying failures, then rerun the relevant sweep before reporting completion.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. Apply it even to small spacing, color, or background edits: local changes can alter wrapping, height, overflow, alignment, and backgrounds at other screen sizes.

A bounding-box check alone is not enough. One desktop and one mobile screenshot are not enough. Real screenshots and numerical checks cover different failure modes, so use both.

## 1. Prepare realistic states

Run the real interface in an authorized test environment. Populate the changed surface with representative content before testing:

- Long paragraphs, formatted text, long field values, and validation messages.
- Representative lists, cards, rows, and realistic item counts.
- Loading, empty, and error states when the change can affect them.
- Content near expected limits, including long unbroken strings where relevant.

Do not validate only an empty or unusually clean state. Sparse content can hide clipping, overlap, wrapping failures, and unintended blank space.

## 2. Select the viewport matrix

Use this as a broadly useful baseline width sweep:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large desktop width, such as 1920 px, when large displays are a supported or expected use case. Add any viewport required by product requirements, supported-device policy, usage data, or the reported issue.

When vertical layout matters, test at least two heights at each relevant width:

- A short viewport of roughly 700 px.
- A tall viewport of roughly 1400 px or greater.

Explicitly include a very tall viewport, such as 1800 px, for changes involving viewport-height sizing, flexible page shells, page backgrounds, vertical padding, sticky footers, or bottom alignment. These layouts can appear correct at ordinary heights while leaving an exposed region or misplaced content on tall screens.

Use a repeatable browser automation system chosen for the project. Prefer headless capture for consistent automated results; use an interactive browser only when it is needed to diagnose a failure.

## 3. Capture and review screenshots

Capture real screenshots at every relevant viewport and state. Use full-page captures when document length matters. Also capture the visible viewport when fixed, sticky, or viewport-height behavior matters.

Inspect each changed component on all four sides:

1. Top.
2. Right.
3. Bottom.
4. Left.

For each side, ask: **Does this match the intended design now that the component has changed role?**

Give extra attention to edge-to-edge or full-bleed changes. Removing containment on one edge can reveal leftover margins or wrapper padding on another edge as visible background strips. A flush component should be checked for unintended space on every side, not only the side edited.

Reread the requested outcome after making the change, then compare it directly with the screenshots. Do not accept the result solely because the CSS appears logically correct.

## 4. Run programmatic checks at each viewport

Run numerical checks alongside screenshots. At minimum, verify:

| Check | Example pass condition |
|---|---|
| Horizontal overflow | The page has no unintended horizontal scrolling or clipped content. |
| Fit-to-viewport layout | Where the design is intended to fit, document height is no more than viewport height plus a small rendering tolerance. |
| Overlap | Adjacent elements and intended containers do not have intersecting bounding rectangles unless overlap is intentional. |
| Control access | Buttons, links, and fields are visible, enabled when expected, and reachable without unintended clipping. |
| Fixed or sticky UI | Fixed elements do not hide essential content or actions. |
| Text readability | Main body text stays within the project's accepted line-length range. |

For a fit-to-viewport screen, a typical check compares `document.documentElement.scrollHeight` to `window.innerHeight`, allowing a small tolerance for rendering differences. For overlap detection, compare the bounding rectangles of changed elements, adjacent content, and their containers.

For prose-heavy pages, flag excessively wide text. A useful warning threshold is about 80 characters per line; reading-focused layouts commonly target roughly 60–70 characters per line. Treat this as a design review signal, not a substitute for the project's typography requirements.

## 5. Require both kinds of evidence

Automated measurements can miss exposed background strips, poor visual balance, and unexpected empty regions. Screenshots can miss off-screen overflow, inaccessible controls, and small collisions.

A viewport passes only when the screenshot review and all relevant programmatic checks pass.

## 6. Fix failures and retest

If any viewport or realistic state fails:

1. Stop completion, review, publishing, or release claims.
2. Identify the layout rule causing the failure.
3. Fix the underlying behavior rather than adding a narrow viewport-specific patch.
4. Rerun the complete relevant sweep, including the states and axes affected by the change.

If a change makes one viewport correct but breaks another, reconsider the diagnosis. The layout model is likely incomplete; do not accumulate patches until screenshots happen to look acceptable.

## 7. Readiness gate and reporting

Do not report vague claims such as “works on mobile and desktop.” State the widths, meaningful height cases, states, and checks actually completed.

Use a report such as:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; tall-viewport review passed.

If any viewport or state remains unverified, say so clearly and do not represent the UI change as complete.

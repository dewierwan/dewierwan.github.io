---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using real screenshots and programmatic layout checks. Fix and retest failures before reporting the change as complete.
---

# Test every screen size

Use this workflow after **any UI, visual, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. This includes small spacing, color, background, typography, or alignment edits: a local change can alter wrapping, overflow, height, backgrounds, or access at another screen size.

Do not rely on bounding-box values alone, or on one desktop and one mobile screenshot. Screenshots reveal visual defects that measurements can miss; measurements find off-screen defects that screenshots can miss. A viewport passes only when both forms of evidence pass.

## 1. Prepare a realistic test state

Run the interface in an appropriate test environment. If test content comes from records or communications, use it only for a legitimate purpose and with clear authorization. Use the minimum information needed, and do not expose unnecessary personal or sensitive data in screenshots, logs, or reports.

Populate the changed surface with representative conditions:

- long text, long field values, and realistic labels;
- typical lists, cards, rows, and validation messages;
- enough items to exercise wrapping, scrolling, and spacing;
- loading, empty, and error states when the change affects them.

Do not validate only an empty or unusually tidy state. Sparse content often hides clipping, overlap, and blank-space problems.

## 2. Choose the viewport sweep

Test these baseline widths unless the product has a documented alternative matrix:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large width, such as 1920 px, for wide layouts or large-display use cases. Include any viewport known to be important for the product.

When vertical layout can matter, test a short viewport (about 700 px high) and a tall viewport (about 1400 px or more) at the relevant widths. Include a very tall viewport, such as 1800 px, when changing viewport-height or minimum-height behavior, flexible page shells, backgrounds, vertical spacing, sticky footers, or bottom alignment.

Use a repeatable browser automation system chosen for the project. Prefer headless execution when it supports consistent, reproducible results.

## 3. Capture and inspect screenshots

Capture screenshots for each relevant viewport and state. Use full-page captures when document length matters, and visible-viewport captures when fixed, sticky, or viewport-height behavior matters.

Inspect each changed component on all four sides: top, right, bottom, and left. Ask whether each edge now matches the intended design.

Be especially careful with edge-to-edge or full-bleed changes. Removing containment on one side can reveal leftover wrapper margin or padding as a visible background strip on another side. Check all edges, not only the edge edited.

Reread the requested outcome and compare it directly with the screenshots. Do not accept a result simply because the CSS rule appears correct.

## 4. Run layout checks at each viewport

Alongside screenshots, check the behaviors relevant to the change:

- no unintended horizontal overflow;
- no unintended vertical overflow on screens intended to fit the viewport;
- no unintended overlap between changed content, neighboring content, and containers;
- controls remain visible, reachable, and usable;
- fixed or sticky interface elements do not hide essential content;
- cards, lists, and form controls remain within their intended bounds;
- prose retains a readable line length.

For fit-to-viewport pages, compare document height with viewport height and allow only a small rendering tolerance. For overlap checks, compare bounding rectangles of relevant elements and containers. Exclude intentionally layered elements from a generic no-overlap rule.

For prose-heavy pages, treat approximately 80 characters per line as a broad warning threshold. Reading-focused layouts commonly aim closer to 60–70 characters per line.

## 5. Fix failures and retest

If any viewport or state fails:

1. stop completion, review, or release;
2. identify the layout rule or component constraint causing the failure;
3. fix the underlying behavior rather than adding a one-viewport cosmetic patch;
4. rerun the full relevant sweep, not only the failing viewport.

If one fix resolves a size but breaks another, reconsider the diagnosis. The layout model is incomplete until it works across the required range.

## 6. Readiness gate and report

Do not claim that the interface “works on mobile and desktop” without evidence. Report the tested widths, relevant height variants and states, and the checks performed.

Example:

> Verified at 320, 480, 600, 720, 1024, and 1440 px; tested short and tall viewports where relevant; no unintended overflow or overlap; controls remain usable; tall viewport clean.

If any required viewport or state was not tested, state that clearly and do not represent the change as complete.

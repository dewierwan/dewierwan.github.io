---
name: test-every-screen-size
description: Verify every UI and CSS change across representative narrow, wide, short, and tall viewports using real screenshots plus programmatic layout checks. Fix and retest failures before reporting the change as complete.
---

# Test every screen size

Use this workflow after **any UI, visual, layout, or CSS change** and before declaring work complete, requesting review, publishing, or releasing. This is required even for a one-line spacing, background, or sizing edit: a local change can alter wrapping, height, overflow, alignment, or visible backgrounds elsewhere.

A single viewport is not sufficient. Bounding-box measurements alone are not sufficient. Real screenshots and numerical checks each find failures the other can miss.

## 1. Prepare a safe, realistic test state

Run the interface in an authorized test environment and populate the affected area with representative content. Use only data appropriate for that environment; do not expose private, unrelated, or sensitive personal information in screenshots or reports.

Include, when relevant:

- long paragraphs, formatted text, and long field values;
- representative cards, rows, lists, and item counts;
- validation messages and error states;
- loading, empty, and populated states;
- content near expected length or count limits.

Do not validate only an empty or unusually clean state. Sparse content often hides clipping, overlap, wrapping failures, and blank background regions.

## 2. Select the viewport sweep

Test these baseline viewport widths:

- 320 px
- 480 px
- 600 px
- 720 px
- 1024 px
- 1440 px

Add a large width, such as 1920 px, for landing pages, dashboards, or interfaces expected on large displays.

When vertical layout can matter, test at least two heights at each relevant width:

- a short viewport, approximately 700 px high;
- a tall viewport, approximately 1400 px high.

Explicitly include a very tall viewport, such as 1800 px, when changing viewport-height sizing, flexible page shells, backgrounds, vertical padding, sticky footers, or bottom alignment. A narrow, short window and a narrow, tall window can expose different defects.

Also test any viewport known to be important for intended users or product requirements.

## 3. Capture real screenshots

Use a repeatable browser automation or testing system selected for the project. Run it in headless mode for consistent, repeatable capture. Capture:

- a visible-viewport screenshot when fixed, sticky, viewport-height, or bottom-alignment behavior matters;
- a full-page screenshot when page length, background continuity, or trailing space matters;
- screenshots for each relevant content state.

Inspect the changed area and its neighbors on **all four sides**:

1. top;
2. right;
3. bottom;
4. left.

For each side, ask: does this match the intended design now that the element's role or size has changed?

Be especially careful with full-bleed, edge-to-edge, or flush layouts. Removing horizontal containment can reveal wrapper margins, padding, or spacing rules as visible strips on another edge. Check every edge, not only the edge edited.

Reread the original requested outcome, then compare it directly with the screenshots. Do not accept a result merely because the implementation appears logically correct.

## 4. Run programmatic checks at each relevant viewport

Run numerical checks alongside visual review. Adapt selectors to the interface, but use concrete checks rather than relying on general impressions.

### Overflow and viewport-fit check

For screens intended to fit within the viewport, verify that document height does not exceed the viewport except for a small rendering tolerance:

```js
document.documentElement.scrollHeight <= window.innerHeight + 1
```

Also check for unintended horizontal overflow, for example by comparing document scroll width with viewport width. Do not apply the viewport-fit rule to pages intentionally designed to scroll.

### Geometry, overlap, and visibility checks

For changed elements and their relevant neighbors, compare `getBoundingClientRect()` values. Confirm that an element's bottom does not extend past the next element's intended top, unless their overlap is deliberate. Also confirm that controls remain inside their intended container and are not clipped or covered.

Verify, where applicable:

- no unintended horizontal scroll or overflow;
- no unintended vertical scrolling on fit-to-viewport screens;
- no unintended overlap with neighboring content, containers, or essential controls;
- buttons, links, inputs, and other controls are visible, reachable, and usable;
- fixed or sticky UI does not cover essential content;
- cards, lists, and controls remain within intended bounds.

### Prose-width check

For prose-heavy surfaces, measure line length using rendered paragraph width and computed font size. A simple approximation is:

```js
const paragraphs = document.querySelectorAll('article p, .prose p, main p');
const measures = [...paragraphs].map((p) => {
  const width = p.getBoundingClientRect().width;
  const fontSize = parseFloat(getComputedStyle(p).fontSize);
  return { width, fontSize, estimatedCharactersPerLine: width / (fontSize * 0.5) };
});
```

Flag paragraphs whose estimated measure exceeds about 80 characters per line. Reading-focused layouts commonly target roughly 60–70 characters per line. Treat this as a warning threshold and assess the actual typography and design intent.

## 5. Require both kinds of evidence

A viewport passes only when both of these pass:

1. **Visual evidence:** screenshots show no unintended blank strips, imbalance, clipping, bad wrapping, or layout defects.
2. **Programmatic evidence:** relevant overflow, bounds, overlap, visibility, and usability checks pass.

Numbers can miss visible background strips and awkward empty regions. Screenshots can miss subtle off-screen overflow, inaccessible controls, and small geometry collisions.

## 6. Fix failures at the cause, then retest

If any viewport or content state fails:

1. stop the completion, review, or release process;
2. identify the layout rule causing the failure;
3. fix the underlying layout behavior rather than adding a size-specific cosmetic patch;
4. rerun the complete relevant sweep, not only the failing viewport.

If a change corrects one viewport but creates a problem at another, reconsider the diagnosis. The layout model is incomplete; do not continue layering patches until the symptom disappears.

## 7. Readiness gate

Do not report the UI work as complete until all of the following are true:

- [ ] Representative content and relevant states were tested.
- [ ] Baseline widths were tested, plus any required target widths.
- [ ] Short and tall heights were tested where vertical behavior matters.
- [ ] A very tall viewport was tested for viewport-height or bottom-layout changes.
- [ ] Screenshots were reviewed on all four sides of the affected area.
- [ ] Relevant programmatic checks passed, including the explicit viewport-fit check when applicable.
- [ ] Every discovered failure was fixed and retested.
- [ ] Screenshots and reports remain within the appropriate access boundary.

## 8. Report the evidence

Do not say only “works on mobile and desktop.” State what was actually tested, including omissions.

| Report item | Example |
|---|---|
| Completed sweep | Verified at 320, 480, 600, 720, 1024, and 1440 px. |
| Vertical coverage | Tested short and tall viewports where vertical layout matters; very tall viewport clean. |
| Checks | No unintended overflow or overlap; controls remain visible and usable. |
| Exception | [State any untested viewport, state, or known limitation clearly.] |

A concise completion report can read:

> Verified at 320, 480, 600, 720, 1024, and 1440 px with realistic content. Tested short and tall layouts where relevant; no unintended overflow or overlap; controls remain visible and usable; very tall viewport is clean.

If any viewport or state remains unverified, say so clearly and do not represent the UI change as complete.

---
name: test-every-screen-size
description: Check a user interface across narrow, wide, short, and tall screens using screenshots and numerical checks.
---

# Test every screen size

Use this after any visual or layout change and before declaring it complete.

## 1. Prepare realistic states

Run the real page in a test environment. Add representative long text, lists,
errors, loading states, and empty states. A clean screenshot with unrealistically
short content proves little.

## 2. Sweep widths and heights

Test at least these widths:

- 320
- 480
- 600
- 720
- 1024
- 1440
- 1920 for public landing pages

Use both a short and tall height where vertical layout matters. Include the
user's real working viewport when known.

## 3. Capture screenshots

Use a headless browser. Save a full-page image at each important size. Inspect
the top, right, bottom, and left edges of every changed component. Do not rely on
one mobile and one desktop screenshot.

## 4. Run numerical checks

For each width, check:

- No horizontal overflow.
- No elements overlap.
- Buttons and inputs remain visible and usable.
- Sticky or fixed elements do not cover content.
- Text lines remain within a readable measure.
- Focus states are visible.

Numbers catch subtle defects, while screenshots catch defects the numbers do
not describe. Use both.

## 5. Fix and repeat

If one size fails, correct the underlying layout and rerun the complete sweep.
A patch that fixes one viewport while breaking another is not complete.

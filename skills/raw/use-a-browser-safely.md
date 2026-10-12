---
name: use-a-browser-safely
description: Complete browser tasks safely: pick the least invasive route, verify the account and every edit, and gate irreversible actions behind a readiness check.
---

# Use a browser safely

Use this workflow when a task has to happen in a web browser. Typical tasks include filling a rendered form, changing a setting in a dashboard, collecting information from a page that only renders with scripts, testing a user flow, or working inside a signed-in session the user has authorized.

The central rule:

> Inspect the page before you edit anything. Read back every field you change. Do not click the final button until verification passes and the account, target, and authorization are clear.

A successful automation call does not prove the website accepted the change. A fill command usually reports success as long as it did not throw an error. It does not check that the application's internal state updated, that moving focus away committed the value, or that the field kept the content. **The caller verifies. Always.**

## 1. Choose the least invasive route

Use the first route that fits. Do not skip ahead.

1. **Direct interface first.** Look for a documented API, export, integration, or plain form endpoint before opening any browser.
2. **Isolated headless browser.** This is the default for anything that does not need the user's identity: public forms, extraction from dynamic pages, UI testing, and screenshots. It never opens a visible window and never touches the user's own browser.
3. **The user's signed-in visible browser.** Use this only when the task truly needs the user's live session, such as an account dashboard or single sign-on state.

### Look for a direct interface

Many forms send structured data to an endpoint that can be called directly, which skips the hardest browser problems. To find one:

- Read the service's official documentation for an API.
- View the page source for a form action or embedded data block.
- Watch the browser's network requests while using the page normally.

Even an endpoint that takes some study to understand is often faster than fighting a complex form. Fall back to the browser when no suitable programmatic option exists or when the user explicitly wants the UI flow.

Limits:

- Do not use undocumented endpoints to get around access controls, terms of service, rate limits, or anti-abuse systems.
- In a signed-in session, do not call an application's internal endpoints from page scripts. Requests that skip the headers or tokens the app normally sends can end the user's session or trigger security responses. Drive the UI instead, or use a supported API with proper credentials.

### Do not use the visible browser for convenience

The user's visible browser is their working space. Taking it over interrupts them and adds privacy and account risk. Extraction, bulk form fills, and anything that works headless should stay headless.

### Blocks and bot checks

If a site blocks headless automation during general research, accept the block and move on. Do not try to evade it. Escalating to the user's signed-in browser is reasonable only when the user explicitly asked for a task on that specific site and the session is genuinely needed. Human-verification checks, security-key prompts, and multi-factor prompts belong to the user: pause, ask them to complete it, then continue. Never simulate, bypass, or weaken these checks.

## 2. Pick the right automation style

Two common styles exist:

- **Step-by-step tool calls** through an interactive browser tool. Good for one click, reading one snapshot, or short tasks with roughly ten or fewer actions and little text.
- **A standalone script** using a browser automation library. Better for long text (for example over a couple of thousand characters), many fields, heavy single-page applications, or anything that needs repeatable runs.

Interactive tool layers can become unstable with long text, several parallel actions against one page, or heavy rendering. If the session crashes with a message like "page, context, or browser has been closed," switch to a script. Do not try to rescue the broken session. When in doubt, write a script.

Script hygiene:

- Save scripts and artifacts in a temporary working folder the user has agreed to.
- Launch standalone automation headless unless a visible session is part of the plan.
- Pass secrets through environment variables or a secrets store. Never hard-code credentials, and never print them in logs.

## 3. Protect identity, privacy, and the user's browser

When the task touches private messages, records, dashboards, or information about other people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant pages and data. Keep unrelated personal details out of screenshots, logs, and reports. Share results only within the requester's appropriate access boundary.

### Rules for the user's visible browser

- **Announce, then act.** Say briefly what you are taking over and why, for example "Taking over the browser to update the billing contact." Never take control silently. If the user has already authorized visible browser use for this task, do not ask again for the same approval.
- **Work in a fresh window, tab, or tab group.** Do not reuse the user's existing tabs unless they point to one.
- **Classify the context before choosing a profile.** Decide whether the task is personal, work, test, staging, or production. Personal errands (shopping, banking, health, subscriptions, household, government services) are personal even on general-purpose sites. Internal operations, vendors, and colleague-facing work are work. If the user says which, that settles it.
- **Select the profile directly.** Many tools offer a generic "current browser" selector that picks whichever profile was used most recently. That can silently put a personal task in a work account. Select the specific profile or session that matches the context.
- **Do not trust display names.** Labels like "Browser 1" can reshuffle after restarts, and nicknames may not propagate. Use a stable identifier where the tool provides one, and record the mapping in a private local note if useful. Even then, verify every time.
- **A window is not a connection.** Opening a window for a profile puts it on screen. The automation connection may still point elsewhere. Confirm the connection, not only the window.
- **Do not restart or force-quit the user's browser** without their explicit OK. It closes everything they have open.

### Account preflight gate

Before any action that changes data, answer three questions:

1. **Which account is this?** Open a fresh tab to a reliable account page and read the signed-in identity.
2. **Which environment is this?** Production, staging, test, or a specific organization or workspace.
3. **What exact item will change?** The specific record, form, or setting.

If any answer is unclear, stop and ask. If your environment uses a permission gate or verification marker that unlocks write actions, set it only after the account check has actually passed, and record the evidence. Never set it to get past the gate.

## 4. Set the task boundary and authorization

Before navigating deeply, identify:

- The target page, record, form, or setting.
- What will be entered, collected, changed, uploaded, or sent.
- The minimum information needed.
- Fields that need the user's judgment.
- Whether the final action can be undone.

**Reversible changes** the user asked for, such as toggling a setting or updating a saved card or draft, can proceed after normal verification.

**Irreversible or high-impact actions** need a pre-action record and confirmation unless the user already gave clear authorization for that exact action. These include payments, purchases, sends, invitations, publishing, deletions, plan or billing changes, access or ownership changes, and anything labeled "cannot be undone" or "cannot be edited after submission." Treat such forms as one-way doors.

Honor an explicit request to review before submission. If authorization is already given, do not ask again. If it is missing, prepare and verify the full result, show the pre-submit state, and ask only for the final action.

## 5. Inspect the page before editing

Before writing any fill logic, list every relevant control. A few minutes here saves long debugging sessions.

For each control, record:

- Element kind: single-line input, multi-line text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Label, accessible name, or label relationship.
- Required state and current value or value length.
- Whether it is the real editor, a wrapper, or a hidden sync field.
- Whether changing it re-renders the form.

```text
// Pseudocode: adapt to the chosen automation library
controls = page.findAll('input, textarea, [contenteditable], [role=textbox]')
for each c in controls:
  record { tag, type, role,
           label: accessibleLabel(c),
           required: c.required or c.ariaRequired,
           length: readValue(c).length }
save record list to 'form-before.json'
```

Things to watch for:

- **Look-alike controls.** Forms often use different control kinds for similar-looking fields. A single-line input silently strips line breaks. A text area usually accepts everything. Rich-text editors keep their own internal model and may ignore direct value changes.
- **Hidden sync fields.** Some editors pair a visible editable area with a hidden input that looks fillable. Filling the hidden input passes a raw DOM check, but the form then reports the field as empty, because the app reads the visible editor. Always fill the control the app actually reads.
- **Empty wrappers.** An accessibility locator can return a wrapper with no editable content inside. Find the real editable element through its label relationship (for example the element named by its labelled-by attribute), then tag it with a temporary marker attribute so you can target it reliably.
- **Unstable order.** Field order can change between loads. Never address fields by position. Use label text or label relationships.
- **Current state.** Before changing an existing record or setting, read its current value so you do not overwrite the wrong thing.

## 6. Use the right interaction for each control

| Control | Preferred interaction | Watch for |
|---|---|---|
| Single-line input | Normal fill | Line breaks removed silently; length limits. |
| Multi-line text area | Fill, then move focus to the page body | Some apps commit only on blur. |
| Rich-text or content-editable editor | Click it, select all, delete, insert text with keyboard-style input, then blur | Direct DOM writes or value setters may be ignored by the app's model. |
| Dropdown or combobox | Open it, choose by exact visible option text, wait for it to settle | Selection can re-render the whole form. |
| Checkbox or radio | Read the state first; click only if it needs to change | Clicking toggles an already-correct value. |
| Date or time picker | Set values, close by clicking neutral page background, check the rendered summary | Close or clear buttons may wipe values; typing while open can rewrite dates. |
| File upload | Confirm file, destination, and privacy first | Upload may start at once and be hard to undo. |

Robust sequence for framework-driven editors:

1. Click the real editable element.
2. Select all existing content and delete it.
3. Insert the new text with keyboard-style text input.
4. Move focus to a neutral element, such as the page body, to commit.
5. Wait briefly for state to settle.
6. Read the value back.

**Blur after every rich-text field.** Without it, the next edit can trigger a re-render that rebuilds earlier editors from a model that never received their text, and only the last field survives.

**Order matters.** Do dropdowns, checkboxes, tabs, and other re-rendering choices first, then fill text. Re-inspect after each such choice. For tricky widgets like date pickers, set them early and re-check them after every later edit.

**Clipboard and paste.** Headless browsers often lack clipboard permission, so embed values directly rather than relying on the clipboard. When rich content (such as HTML with links) must be inserted, a synthetic paste event carrying both HTML and plain text works in some editors and is ignored by others. Some editors expose their own documented conversion method instead. Try the supported method for that editor and always verify the result, ideally through the service's API or an export rather than the screen alone.

**Drag and drop.** Dragging can create layout changes (like columns) or trigger a clickable element by accident. Prefer keyboard-based move commands with short waits, then verify the final structure.

**Send buttons and selectors drift.** Before clicking a send or submit control found by selector, read the composed content back to confirm it landed in the right place. Selectors that worked before can stop matching after a site update.

## 7. Verify after every fill

After each change, read the value back and compare it with what you intended. For sensitive content, compare lengths or a short redacted summary rather than printing full text.

```text
result = fillField(field, value)
if result.length != value.length:
  log 'mismatch on ' + field.label + ': ' + result.length + '/' + value.length
  retry once with a different method (for example keyboard input instead of a setter)
  verify again; if still wrong, stop and report
```

How to read common mismatches:

- **Empty after a reported success:** the app ignored a direct value change. Use focus-and-keyboard input, then blur.
- **Short by a few characters, roughly one per paragraph:** a single-line input dropped line breaks. Rewrite as one paragraph, or find the multi-line field.
- **Short after collapsing blank lines or repeated spaces:** some editors normalize whitespace. Usually acceptable; if not, simplify the formatting yourself and note it.
- **Earlier field now blank:** a re-render reset uncommitted state. Blur each field and do re-rendering choices first.

If verification still fails after one retry, do not move toward submission. Report the problem and ask how to proceed.

## 8. Two-phase run and pre-submit gate

Run consequential tasks in two phases.

**Phase 1: prepare.** Fill everything, verify each field, save a structured after-state record, and capture a full-page screenshot. Do not submit.

**Phase 2: commit.** If the task or a standing instruction already authorizes the final action, continue. Otherwise show the prepared state and get the missing authorization. Then re-fill if needed, re-run the gate below, and click the final control once.

A script can implement this with a flag such as `--submit` that is off by default.

```text
open headless browser and new page
go to target URL; dismiss banners; sign in if needed
inspect controls -> save 'form-before.json'
apply re-rendering choices first, then fill text fields with verification
inspect again -> save 'form-after.json'; save full-page screenshot
if submit flag is set:
  run pre-submit gate; refuse and exit if it fails
  click the exact final button by its visible name
  wait, then save a post-submit screenshot and check for confirmation
close browser
```

### Pre-submit readiness gate

Re-inspect the full page state. Submit only if all are true:

- [ ] Correct account, organization, and environment.
- [ ] Correct target item.
- [ ] Every required field is non-empty.
- [ ] Each value matches the intended content closely enough.
- [ ] Dropdowns, checkboxes, dates, recipients, and attachments are correct.
- [ ] No validation errors, warnings, or unsaved-change notices remain.
- [ ] The button about to be clicked does what you expect and is not a similar-looking destructive option.

**If any required field is empty, do not submit.** This is not negotiable. A partly filled form can be fixed; a wrong submission often cannot.

A confirmation request for an irreversible action should state the target, key values, recipients or audience, any cost, what cannot be undone, and any open questions.

## 9. Confirm completion

A click is not proof of success. Look for real evidence: a success message, a confirmation reference, a new record, a setting that persists after a safe reload, or a sent or published item.

- **Errors can be cosmetic.** Some apps show "something went wrong" after the work actually finished. Inspect the result before retrying, because blind retries can create duplicate messages, payments, or records.
- **Frozen pages.** A blocking pop-up dialog can freeze the tab so clicks and screenshots time out. Ask the user to respond to it, then continue. Where possible, confirm the outcome through an independent channel (for example a public lookup or an API read) instead of the frozen UI.
- If you cannot confirm completion, say what you tried, what evidence exists, and what remains uncertain. Never report an attempt as a success.

## 10. Parallel work and background tabs

When many independent items are needed (for example several generated drafts or images), separate tabs or sessions each given the full brief avoid one item biasing the next. Keep concurrency modest, around ten at once; more tends to stall or fail. Background tabs may not render content at full size, so bring an item into view before capturing it and check that nothing is cut off. Clean up any temporary overlays or tabs afterward.

## 11. General failure patterns

| Symptom | Likely cause | Safe response |
|---|---|---|
| Fill reports success but the field is blank | App model ignored a direct write | Keyboard-style input, blur, read back. |
| Earlier fields blank out as later ones are filled | Re-render rebuilt editors from stale state | Blur after each fill; do re-rendering choices first. |
| A choice in a dropdown wipes the form | Selection triggers a full re-render | Make choices before filling text; re-verify. |
| Field looks filled but validation says empty | Hidden sync field was edited | Fill the visible editor the app reads. |
| Locator returns an empty wrapper | Accessible name sits on a different element | Follow the label relationship to the real editor. |
| Interactive tool crashes on long text or parallel calls | Tool layer is unstable for heavy work | Switch to a standalone script. |
| Headless page differs from a normal browser | Site varies by browser context | Prefer a direct interface; escalate only for an explicit task, never evade protections. |
| Wrong account or profile opened | Generic selector picked the last-used profile | Classify context, select the profile directly, verify the account. |
| Session ends after a page-script request | Internal endpoint called without the app's normal headers | Drive the UI or use a supported API. |
| Automation connection fails an integrity or signature check | Local helper is stale or altered | Stop; repair through an approved path that keeps verification on. Never disable checks. |
| Security check or 2FA prompt appears | Site needs the user present | Ask the user to complete it, then continue. |

## 12. Report results

Keep reports short. Summarize the outcome in one or two sentences, point to the screenshot and the after-state record, and offer to open the screenshot for the user. Do not paste every field value as a large inline table; the user can open the record if they want the full text. Store artifacts only where the user can appropriately access them, and delete temporary files that contain sensitive content when they are no longer needed.

## 13. Keep the procedure current

When a run reveals a reusable lesson, such as a new failure mode, a working pattern, or a missing capability, add it to your local copy of this procedure. Prefer a single table row with symptom, cause, and fix over new prose. Never record credentials, account identifiers, personal details, or private site data. Keep the document bounded: when it grows long, merge older entries into general principles instead of appending incident history. Tool paths, versions, and profile mappings go stale, so update them in place and re-verify them in the current environment.

## Final audit checklist

- [ ] The least invasive suitable route was used.
- [ ] Purpose and authorization were clear; only minimum relevant data was accessed.
- [ ] Visible-browser use was announced and kept to a fresh window or tab.
- [ ] Account, environment, and target were verified before any write.
- [ ] Controls were inspected before editing and addressed by label, not position.
- [ ] Every meaningful change was read back.
- [ ] The pre-submit gate passed, with no empty required fields.
- [ ] Irreversible actions had a pre-action record and authorization.
- [ ] Success was confirmed with evidence after acting.
- [ ] The report separates confirmed results from uncertainty and exposes no secrets or unneeded personal data.

---
name: use-a-browser-safely
description: Completes browser tasks safely: least invasive route, verified account and fields, confirmation before acting. Use when filling forms, fixing dashboards, or working in a signed-in app.
---

# Use a browser safely

Use this workflow when a task has to happen in a web browser: filling a rendered form, changing a setting in a dashboard, collecting information from a page that only renders with scripts, testing a user flow, or working inside a signed-in session the user has authorized. It keeps the work on the least invasive route and proves each change actually landed before anything irreversible happens.

## Quick version

These steps work even with a plain chat assistant that walks you through the task while you do the clicking.

- **Look for a shortcut first.** Ask whether the service has an export, official integration, API, or simple form you can use instead of clicking through a complex page.
- **Check where you are.** Before changing anything, open the account or profile page and confirm the signed-in account, the workspace or environment, and the exact item you will change.
- **List the fields before typing.** Note each field's label, whether it is required, and what kind it is (one line, multi-line, rich text, dropdown, checkbox, date). Make dropdown, checkbox, and date choices first, because they can reset the form.
- **Read back every field.** After entering text, click somewhere neutral on the page and check the value is still there and complete.
- **Stop before the final button.** Confirm every required field is filled, the values are right, and whether the action can be undone. Take a screenshot. For payments, sends, deletions, or "cannot be edited" forms, get a clear yes first.
- **Look for proof afterward.** A confirmation message, reference number, or saved record. If you see an error, check whether the action happened before retrying.

## 1. Follow the central rule

> Inspect the page before you edit anything. Read back every field you change. Do not click the final button until verification passes and the account, target, and authorization are clear.

A successful automation call does not prove the website accepted the change. A fill command usually reports success as long as it did not throw an error. It does not check that the application's internal state updated, that moving focus away committed the value, or that the field kept the content. **The caller verifies. Always.**

## 2. Choose the least invasive route

Use the first route that fits. Do not skip ahead.

1. **Direct interface first.** Look for a documented API, export, integration, or plain form endpoint before opening any browser.
2. **Isolated headless browser.** The default for anything that does not need the user's identity: public forms, extraction from dynamic pages, UI testing, and screenshots. It never opens a visible window and never touches the user's own browser.
3. **The user's signed-in visible browser.** Only when the task truly needs the user's live session, such as an account dashboard or single sign-on state.

### Look for a direct interface

Many forms send structured data to an endpoint that can be called directly, which skips the hardest browser problems. Read the service's official documentation, view the page source for a form action or embedded data block, or watch the browser's network requests while using the page normally. Even an endpoint that takes some study is often faster than fighting a complex form. Fall back to the browser when no suitable programmatic option exists or when the user explicitly wants the UI flow.

Limits:

- Do not use undocumented endpoints to get around access controls, terms of service, rate limits, or anti-abuse systems.
- In a signed-in session, do not call an application's internal endpoints from page scripts. Requests that skip the headers or tokens the app normally sends can end the user's session or trigger security responses. Drive the UI instead, or use a supported API with proper credentials. Reading state the page already holds in memory, without network calls, is lower risk.

### Do not use the visible browser for convenience

The user's visible browser is their working space. Taking it over interrupts them and adds privacy and account risk. Extraction, bulk form fills, and anything that works headless should stay headless.

### Blocks and bot checks

If a site blocks headless automation during general research, accept the block and move on. Escalating to the signed-in browser is reasonable only when the user explicitly asked for a task on that specific site and the session is genuinely needed. Human-verification checks, security-key prompts, and multi-factor prompts belong to the user: pause, ask them to complete it, then continue. Never simulate, bypass, or weaken these checks.

## 3. Pick the right automation style

- **Step-by-step tool calls** through an interactive browser tool suit one click, reading one snapshot, or short tasks with roughly ten or fewer actions and little text.
- **A standalone script** using a browser automation library suits long text (for example over a couple of thousand characters), many fields, heavy single-page applications, or anything that needs repeatable runs.

Interactive tool layers can become unstable with long text, several parallel actions against one page, or heavy rendering. If the session crashes with a message like "page, context, or browser has been closed," switch to a script rather than rescuing the broken session. When in doubt, write a script.

Script hygiene: save scripts and artifacts in a temporary folder the user has agreed to, launch standalone automation headless unless a visible session is part of the plan, and pass secrets through environment variables or a secrets store. Never hard-code or log credentials.

## 4. Protect identity, privacy, and the user's browser

When the task touches private messages, records, dashboards, or information about other people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant pages and data, keep unrelated personal details out of screenshots, logs, and reports, and share results only within the requester's appropriate access boundary.

### Rules for the user's visible browser

- **Announce, then act.** Say briefly what you are taking over and why, for example "Taking over the browser to update the billing contact." Never take control silently. If the user already authorized visible browser use for this task, do not ask again.
- **Work in a fresh window, tab, or tab group.** Do not reuse the user's existing tabs unless they point to one.
- **Classify the context before choosing a profile.** Personal, work, test, staging, or production. Personal errands (shopping, banking, health, subscriptions, household, government services) are personal even on general-purpose sites. Internal operations, vendors, and colleague-facing work are work. If the user says which, that settles it.
- **Select the profile directly.** A generic "current browser" selector often picks whichever profile was used most recently, which can silently put a personal task in a work account.
- **Do not trust display names.** Labels like "Browser 1" can reshuffle after restarts. Use a stable identifier where the tool provides one, record the mapping in a private local note if useful, and still verify every time.
- **A window is not a connection.** Opening a window for a profile puts it on screen; the automation connection may still point elsewhere. If the window is open but the tool never lists a connection for it, and relaunching does not help, the connector or extension in that profile is likely signed out or asleep. Ask the user to open it in that window and sign in if prompted, then list connections again and verify.
- **Do not restart or force-quit the user's browser** without their explicit OK. It closes everything they have open.

### Account preflight gate

Before any action that changes data, answer:

1. **Which account is this?** Open a fresh tab to a reliable account page and read the signed-in identity.
2. **Which environment is this?** Production, staging, test, or a specific organization or workspace.
3. **What exact item will change?** The specific record, form, or setting.

If any answer is unclear, stop and ask. If your environment uses a permission gate or verification marker that unlocks write actions, set it only after the account check has actually passed, and record the evidence. Never set it just to get past the gate.

## 5. Set the task boundary and authorization

Before navigating deeply, identify the target page, record, form, or setting; what will be entered, collected, changed, uploaded, or sent; the minimum information needed; fields that need the user's judgment; and whether the final action can be undone.

**Reversible changes** the user asked for, such as toggling a setting or updating a saved card or draft, can proceed after normal verification.

**Irreversible or high-impact actions** need a pre-action record and confirmation unless the user already gave clear authorization for that exact action. These include payments, purchases, sends, invitations, publishing, deletions, plan or billing changes, access or ownership changes, and anything labeled "cannot be undone" or "cannot be edited after submission." Treat such forms as one-way doors.

For deletions, check whether the service keeps a restorable trash or recycle bin and note it in the pre-action record. A restore path lowers the risk but does not remove the need for authorization. Some actions, including delete, sit behind menus that appear only when you hover over an item; reveal the menu on the exact item you verified.

Honor an explicit request to review before submission. If authorization is already given, do not ask again. If it is missing, prepare and verify the full result, show the pre-submit state, and ask only for the final action.

## 6. Inspect the page before editing

Before writing any fill logic, list every relevant control and record its kind (single-line input, text area, rich-text editor, dropdown, checkbox, radio, date picker, upload, custom widget), its label or label relationship, its required state, its current value or length, whether it is the real editor or a wrapper or hidden sync field, and whether changing it re-renders the form.

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

Watch for:

- **Look-alike controls.** A single-line input silently strips line breaks. A text area usually accepts everything. Rich-text editors keep their own internal model and may ignore direct value changes.
- **Hidden sync fields.** Some editors pair a visible editable area with a hidden input that looks fillable. Filling the hidden input passes a raw DOM check, but the form reports the field as empty. Always fill the control the app actually reads.
- **Empty wrappers.** An accessibility locator can return a wrapper with no editable content. Follow the label relationship to the real editable element, then tag it with a temporary marker attribute so you can target it reliably.
- **Unstable order.** Field order can change between loads. Never address fields by position.
- **Current state.** Before changing an existing record or setting, read its current value so you do not overwrite the wrong thing.

## 7. Use the right interaction for each control

| Control | Preferred interaction | Watch for |
|---|---|---|
| Single-line input | Normal fill | Line breaks removed silently; length limits. |
| Multi-line text area | Fill, then move focus to the page body | Some apps commit only on blur. |
| Rich-text or content-editable editor | Click, select all, delete, insert text with keyboard-style input, then blur | Direct DOM writes or value setters may be ignored. |
| Dropdown or combobox | Open, choose by exact visible option text, wait to settle | Selection can re-render the whole form. |
| Checkbox or radio | Read the state first; click only if it needs to change | Clicking toggles an already-correct value. |
| Date or time picker | Set values, close by clicking neutral page background, check the rendered summary | Close or clear buttons may wipe values; typing while open can rewrite dates. |
| File upload | Confirm file, destination, and privacy first | Upload may start at once and be hard to undo. |

Robust sequence for framework-driven editors: click the real editable element, select all and delete, insert the new text with keyboard-style input, move focus to a neutral element to commit, wait briefly, then read the value back.

**Blur after every rich-text field.** Otherwise the next edit can trigger a re-render that rebuilds earlier editors from a model that never received their text, and only the last field survives.

**Order matters.** Do dropdowns, checkboxes, tabs, and other re-rendering choices first, then fill text. Re-inspect after each such choice. Set tricky widgets like date pickers early and re-check them after every later edit.

**Selectors drift.** Before clicking a send or submit control found by selector, read the composed content back to confirm it landed in the right place. Selectors that worked before can stop matching after a site update.

## 8. Verify after every fill

Read each value back and compare it with what you intended. For sensitive content, compare lengths or a short redacted summary rather than printing full text.

```text
result = fillField(field, value)
if result.length != value.length:
  log 'mismatch on ' + field.label + ': ' + result.length + '/' + value.length
  retry once with a different method (for example keyboard input instead of a setter)
  verify again; if still wrong, stop and report
```

Reading mismatches:

- **Empty after a reported success:** the app ignored a direct value change. Use focus-and-keyboard input, then blur.
- **Short by about one character per paragraph:** a single-line input dropped line breaks. Rewrite as one paragraph, or find the multi-line field.
- **Short after blank lines or repeated spaces:** the editor normalized whitespace. Usually acceptable; if not, simplify the formatting and note it.
- **Earlier field now blank:** a re-render reset uncommitted state. Blur each field and do re-rendering choices first.

If verification still fails after one retry, do not move toward submission. Report the problem and ask how to proceed.

## 9. Two-phase run and pre-submit gate

**Phase 1: prepare.** Fill everything, verify each field, save a structured after-state record, and capture a full-page screenshot. Do not submit.

**Phase 2: commit.** If the task or a standing instruction already authorizes the final action, continue. Otherwise show the prepared state and get the missing authorization. Then re-fill if needed, re-run the gate, and click the final control once.

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

Re-inspect the full page. Submit only if all are true:

- [ ] Correct account, organization, and environment.
- [ ] Correct target item.
- [ ] Every required field is non-empty.
- [ ] Each value matches the intended content closely enough.
- [ ] Dropdowns, checkboxes, dates, recipients, and attachments are correct.
- [ ] No validation errors, warnings, or unsaved-change notices remain.
- [ ] The button about to be clicked does what you expect and is not a similar-looking destructive option.

**If any required field is empty, do not submit.** This is not negotiable. A partly filled form can be fixed; a wrong submission often cannot.

A confirmation request for an irreversible action should state the target, key values, recipients or audience, any cost, what cannot be undone, and any open questions.

### Worked example (fictional)

An assistant fills a grant application for the fictional Harbor Lane Arts Collective on the fictional Northwind Foundation portal. Inspection finds: Project title (single-line, required), Summary (rich-text editor, required, with a hidden sync input beside it), Category (dropdown that re-renders the form), and Start date (picker). The plan: choose Category first, set the date, fill Summary in the visible editor with keyboard input and blur, then fill the title. Read-back shows Summary at 412 of 415 characters (the editor collapsed double blank lines, acceptable and noted) and Title at 0 of 38. A retry with keyboard input gives 38 of 38. The date is re-checked and still correct. The page says entries cannot be edited after submission, so the assistant saves a screenshot and asks: "Ready to submit the Harbor Lane application to Northwind under Community Arts, starting 1 March. It cannot be edited afterward. Submit?"

## 10. Confirm completion

A click is not proof of success. Look for real evidence: a success message, a confirmation reference, a new record, a setting that persists after a safe reload, or a sent or published item.

- **Errors can be cosmetic.** Some apps show "something went wrong" after the work actually finished. Inspect the result before retrying, because blind retries can create duplicate messages, payments, or records.
- **Frozen pages.** A blocking pop-up dialog can freeze the tab so clicks and screenshots time out. Ask the user to respond to it, then continue. Where possible, confirm the outcome through an independent channel, such as a public lookup or an API read.
- If you cannot confirm completion, say what you tried, what evidence exists, and what remains uncertain. Never report an attempt as a success.

## 11. General failure patterns

| Symptom | Likely cause | Safe response |
|---|---|---|
| Fill reports success but the field is blank | App model ignored a direct write | Keyboard-style input, blur, read back. |
| Earlier fields blank out as later ones are filled | Re-render rebuilt editors from stale state | Blur after each fill; do re-rendering choices first. |
| A dropdown choice wipes the form | Selection triggers a full re-render | Make choices before filling text; re-verify. |
| Field looks filled but validation says empty | Hidden sync field was edited | Fill the visible editor the app reads. |
| Locator returns an empty wrapper | Accessible name sits on a different element | Follow the label relationship to the real editor. |
| Interactive tool crashes on long text or parallel calls | Tool layer is unstable for heavy work | Switch to a standalone script. |
| Headless page differs from a normal browser | Site varies by browser context | Prefer a direct interface; escalate only for an explicit task, never evade protections. |
| Wrong account or profile opened | Generic selector picked the last-used profile | Classify context, select the profile directly, verify the account. |
| Profile window open but no connection appears | Connector in that profile is signed out or asleep | Ask the user to open and sign in to it in that window, re-list, verify. |
| Session ends after a page-script request | Internal endpoint called without the app's normal headers | Drive the UI or use a supported API. |
| Automation connection fails an integrity or signature check | Local helper is stale or altered | Stop; repair through an approved path that keeps verification on. Never disable checks. |
| Security check or 2FA prompt appears | Site needs the user present | Ask the user to complete it, then continue. |

## 12. Report results

Summarize the outcome in one or two sentences, point to the screenshot and the after-state record, and offer to open the screenshot. Do not paste every field value as a large inline table. Store artifacts only where the user can appropriately access them, and delete temporary files with sensitive content when no longer needed.

## 13. Keep the procedure current

When a run reveals a reusable lesson, such as a new failure mode, a working pattern, or a missing capability, add it to your local copy of this procedure. Prefer a single table row with symptom, cause, and fix over new prose. Never record credentials, account identifiers, personal details, or private site data. When the document grows long, merge older entries into general principles instead of appending incident history. Tool paths, versions, and profile mappings go stale, so update them in place and re-verify them.

## Final audit checklist

- [ ] The least invasive suitable route was used.
- [ ] Visible-browser use was announced and kept to a fresh window or tab.
- [ ] Account, environment, and target were verified before any write.
- [ ] Controls were inspected before editing and addressed by label, not position.
- [ ] Every meaningful change was read back.
- [ ] The pre-submit gate passed, with no empty required fields.
- [ ] Irreversible actions had a pre-action record and authorization.
- [ ] Success was confirmed with evidence after acting.
- [ ] The report separates confirmed results from uncertainty and exposes no secrets.

## Optional extras

**Clipboard and paste.** Headless browsers often lack clipboard permission, so embed values directly. When rich content (such as HTML with links) must be inserted, a synthetic paste event carrying both HTML and plain text works in some editors and is ignored by others; some editors expose their own documented conversion method instead. Verify the result, ideally through the service's API or an export rather than the screen alone.

**Drag and drop.** Dragging can create layout changes (like columns) or trigger a clickable element by accident. Prefer keyboard move commands with short waits, then verify the final structure.

**Parallel work and background tabs.** When many independent items are needed (for example several generated drafts or images), separate tabs or sessions each given the full brief avoid one item biasing the next. Keep concurrency modest (a default of about ten, adjustable); more tends to stall. Background tabs may not render at full size, so bring an item into view before capturing it, check nothing is cut off, and clean up temporary overlays or tabs afterward.

**Auditing configuration after a structural change.** When fields, tables, or sources are renamed or deleted and the service has no API for its automations or workflows, audit through the UI:

- Steps that bind to internal IDs usually follow renames; custom script steps that reference names may silently break; steps whose source was deleted often show a "fix configuration" style warning.
- Open each item in turn, wait for it to load, and check for warning text, script steps, and the status of the latest run in its history.
- If a page-script loop runs longer than your tool's call time limit, start it without waiting, store results in a page variable, and poll for them in later calls.
- If the tool rejects returned text containing certain characters (such as URL query symbols), strip or encode them before returning.
- Report which items need attention, separating confirmed breakage from items that only use name-based references and need a manual check.

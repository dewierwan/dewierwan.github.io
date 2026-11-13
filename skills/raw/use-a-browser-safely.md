---
name: use-a-browser-safely
description: Completes browser tasks safely: least invasive route, verified account and fields, confirmation before acting. Use when filling forms, fixing dashboards, or working in a signed-in app.
---

# Use a browser safely

Use this workflow when a task has to happen in a web browser: filling a rendered form, changing a setting in a dashboard, collecting information from a page that only renders with scripts, testing a user flow, or working inside a signed-in session the user has authorized. It keeps the work on the least invasive route and proves each change actually landed before anything irreversible happens.

## Quick version

These steps work even with a plain chat assistant that walks you through the task while you do the clicking.

- **Look for a shortcut first.** Ask whether the service has an export, official integration, API, or simple form you can use instead of clicking through a complex page.
- **Check where you are.** Before changing anything, open the account or profile page and confirm the signed-in account, the workspace or environment, and the exact item you will change. If a page says you lack permission, you are probably in the wrong account.
- **List the fields before typing.** Note each field's label, whether it is required, and what kind it is (one line, multi-line, rich text, dropdown, checkbox, date). Make dropdown, checkbox, and date choices first, because they can reset the form.
- **Read back every field.** After entering text, click somewhere neutral on the page and check the value is still there and complete.
- **Stop before the final button.** Confirm every required field is filled, the values are right, and whether the action can be undone. Take a screenshot. For payments, sends, deletions, or "cannot be edited" forms, get a clear yes first.
- **Look for proof afterward.** A confirmation message, reference number, or saved record. If you see an error, check whether the action happened before retrying.

## 1. Follow the central rule

> Inspect the page before you edit anything. Read back every field you change. Do not click the final button until verification passes and the account, target, and authorization are clear.

A fill command usually reports success as long as it did not throw an error. It does not check that the application's internal state updated, that moving focus away committed the value, or that the field kept the content. **The caller verifies. Always.**

## 2. Choose the least invasive route

Use the first route that fits. Do not skip ahead.

1. **Direct interface.** A documented API, export, integration, or plain form endpoint.
2. **Isolated headless browser.** The default for anything that does not need the user's identity: public forms, extraction from dynamic pages, UI testing, and screenshots. It never touches the user's own browser.
3. **The user's signed-in visible browser.** Only when the task truly needs the user's live session.

**Finding a direct interface.** Read the service's documentation, view the page source for a form action or embedded data, or watch the network requests while using the page normally. Booking and search widgets often sit on a plain request that is easier to call than the widget is to drive. Fall back to the browser when no suitable option exists or the user wants the UI flow.

**Limits.** Do not use undocumented endpoints to get around access controls, terms, rate limits, or anti-abuse systems. In a signed-in session, do not change anything by calling internal endpoints from page scripts; requests missing the app's normal headers can end the session or trigger security responses. Reading state the page already holds in memory is lower risk. If you must read through internal requests, repeat only read-only requests the page itself makes, with the same headers and parameters, and stop at the first sign of session trouble.

**Do not use the visible browser for convenience.** It is the user's working space. Anything that works headless stays headless.

**Blocks and bot checks.** If a site blocks headless automation during general research, accept it and move on. Escalate to the signed-in browser only when the user explicitly asked for a task on that site. If the task is just a lookup, keep it read-only: open the results page and read its text, with no clicks or entries. Human-verification checks, security keys, and multi-factor prompts belong to the user: pause, ask them to complete it, then continue. Never simulate, bypass, or weaken these checks, and never disable integrity or signature checks on local tools.

## 3. Pick the right automation style

- **Step-by-step tool calls** suit one click, one snapshot, or short tasks with little text.
- **A standalone script** suits long text, many fields, heavy single-page apps, or repeatable runs.

Interactive tool layers can crash on long text, parallel actions against one page, or heavy rendering. If you see an error like "page, context, or browser has been closed," switch to a script instead of rescuing the session. Save scripts and artifacts in a temporary folder the user agreed to, run headless unless a visible session is part of the plan, and pass secrets through environment variables or a secrets store. Never hard-code or log credentials.

## 4. Protect identity, privacy, and the user's browser

When the task touches private messages, records, or information about other people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant pages and data, keep unrelated personal details out of screenshots, logs, and reports, and share results only within the requester's appropriate access boundary.

**Rules for the visible browser:**

- **Announce, then act.** Say briefly what you are taking over and why, for example "Taking over the browser to update the billing contact." If the user already authorized it for this task, do not ask again.
- **Work in a fresh window or tab.** Do not reuse the user's tabs unless they point to one.
- **Classify the context, then pick the profile directly.** Personal, work, test, or production. Personal errands are personal even on general-purpose sites; if the user says which, that settles it. A generic "current browser" selector often picks the last-used profile, and display labels can reshuffle after restarts, so use a stable identifier where available and verify every time.
- **A window is not a connection.** Opening a profile's window does not route the automation to it. If no connection appears, the connector in that profile may be signed out or asleep; ask the user to wake or sign in to it, then check again.
- **Do not restart or force-quit the browser** without explicit OK. It closes everything the user has open.

**Account preflight gate.** Before any write, answer: Which account is this (read it from a reliable account page)? Which environment or workspace? What exact item will change? If any answer is unclear, stop and ask. If your setup uses a verification marker that unlocks write actions, set it only after the check has actually passed, and record the evidence.

**Permission denied means wrong account, not a puzzle.** Admin consoles often need a separate administrative account. Do not hunt for workarounds; ask the user to sign in with the right account, reload, and re-run the check.

## 5. Set the task boundary and authorization

Before navigating deeply, identify the target, what will be entered or changed, the minimum information needed, fields that need the user's judgment, and whether the final action can be undone.

- **Reversible changes** the user asked for, such as toggling a setting or updating a draft, can proceed after normal verification.
- **Irreversible or high-impact actions** need a pre-action record and confirmation unless the user already authorized that exact action: payments, sends, invitations, publishing, deletions, plan or access changes, and anything labeled "cannot be undone." For deletions, note whether a restorable trash exists; it lowers risk but does not replace authorization.
- **Credentials stay with the user.** Entering keys, tokens, or passwords is the user's step. Set up everything around it, then give them exact steps. Never move secrets by automated copy and paste; a copy button can appear to work while the clipboard holds older text.

Honor an explicit request to review before submission. If authorization is missing, prepare and verify the full result, show it, and ask only for the final action.

## 6. Inspect the page before editing

List every relevant control with its kind, label or label relationship, required state, current value or length, and whether it is the real editor, a wrapper, or a hidden sync field.

```text
// Pseudocode: adapt to your automation library
controls = page.findAll('input, textarea, [contenteditable], [role=textbox]')
for each c in controls:
  record { tag, type, role, label: accessibleLabel(c),
           required: c.required or c.ariaRequired,
           length: readValue(c).length }
save to 'form-before.json'
```

Watch for:

- **Look-alike controls.** Single-line inputs strip line breaks silently. Rich-text editors keep their own internal model and may ignore direct value changes.
- **Hidden sync fields and empty wrappers.** A hidden input beside a visible editor looks fillable, but the form reads the visible editor. An accessibility locator can return a wrapper with nothing editable. Follow the label relationship to the real element and tag it with a temporary marker attribute.
- **Unstable order.** Never address fields by position.
- **Current state.** Read existing values before overwriting.
- **The wrong tool behind a direct link.** A bookmarked address can open a bulk editor or setup wizard instead of the item editor. If the existing entries you expect are missing, or the page warns that submitting resets broader settings, leave without submitting and use normal navigation. When adding an entry beside others, match their conventions.

## 7. Use the right interaction for each control

| Control | Preferred interaction | Watch for |
|---|---|---|
| Single-line input | Normal fill | Line breaks removed; length limits. |
| Multi-line text area | Fill, then move focus to the page body | Some apps commit only on blur. |
| Rich-text editor | Click, select all, delete, insert text with keyboard-style input, blur | Direct DOM writes may be ignored. |
| Dropdown or combobox | Choose by exact visible option text, wait to settle | Selection can re-render the form. |
| Checkbox or radio | Read state first; click only if it must change | Clicking toggles a correct value. |
| Date or time picker | Set values, close by clicking neutral background, check the summary | Close or clear buttons may wipe values. |
| File upload | Confirm file, destination, and privacy first | Upload may start at once (see Optional extras). |

- **Blur after every rich-text field.** Otherwise the next edit can re-render earlier editors from stale state, and only the last field survives.
- **Order matters.** Do re-rendering choices first, then text. Re-inspect after each choice, and re-check tricky widgets after later edits.
- **Selectors drift.** Before clicking send or submit, read the composed content back to confirm it landed where you expected.

## 8. Verify after every fill

Compare each read-back value with what you intended. For sensitive content, compare lengths or a redacted summary.

```text
result = fillField(field, value)
if result.length != value.length:
  log 'mismatch on ' + field.label
  retry once with a different method (keyboard input instead of a setter)
  verify again; if still wrong, stop and report
```

- **Empty after reported success:** the app ignored a direct write. Use keyboard input, then blur.
- **Short by about one character per paragraph:** a single-line input dropped line breaks.
- **Short after blank lines:** the editor normalized whitespace. Usually acceptable; note it.
- **Earlier field now blank:** a re-render reset uncommitted state.

If verification still fails after one retry, do not move toward submission.

## 9. Two-phase run and pre-submit gate

**Phase 1: prepare.** Fill, verify each field, save an after-state record and a full-page screenshot. Do not submit.

**Phase 2: commit.** If authorization exists, continue; otherwise show the prepared state and ask. Re-run the gate, then click the final control once. A script can use a `--submit` flag that is off by default.

**Pre-submit readiness gate.** Re-inspect the page. Submit only if all are true:

- [ ] Correct account, environment, and target item.
- [ ] Every required field is non-empty and values match intent.
- [ ] Dropdowns, dates, recipients, and attachments are correct.
- [ ] No validation errors or unsaved-change notices remain.
- [ ] The button about to be clicked is the expected one, not a similar destructive option.

**If any required field is empty, do not submit.** A confirmation request for an irreversible action should state the target, key values, audience, any cost, and what cannot be undone.

**Worked example (fictional).** An assistant fills a grant application for the fictional Harbor Lane Arts Collective on the fictional Northwind Foundation portal. Inspection finds a required single-line title, a required rich-text summary with a hidden sync input beside it, a category dropdown that re-renders the form, and a date picker. It picks the category first, sets the date, fills the visible summary editor with keyboard input and blurs, then fills the title. Read-back shows the summary at 412 of 415 characters (collapsed blank lines, noted) and the title at 0 of 38; a keyboard retry gives 38 of 38. The page says entries cannot be edited later, so the assistant saves a screenshot and asks: "Ready to submit the Harbor Lane application under Community Arts, starting 1 March. It cannot be edited afterward. Submit?"

## 10. Confirm completion

A click is not proof. Look for a success message, a reference number, a new record, or a setting that persists after a safe reload.

- **Errors can be cosmetic.** Some apps show "something went wrong" after the work finished. Check before retrying, since blind retries can duplicate sends, payments, or records.
- **Frozen pages.** A blocking pop-up can freeze the tab. Ask the user to respond to it, then continue.
- **Use an independent channel.** Confirm through an API read, a public lookup, or a query to the authoritative source rather than a cached copy.
- **Probe settings harmlessly.** For allow-lists or access rules, send a request that exercises the setting without signing in or changing anything, and compare with a case that should be rejected.
- If you cannot confirm, say what you tried and what remains uncertain. Never report an attempt as a success.

## 11. General failure patterns

| Symptom | Likely cause | Safe response |
|---|---|---|
| Fill reports success but field is blank | App ignored a direct write | Keyboard-style input, blur, read back. |
| Earlier fields blank out, or a dropdown wipes the form | Re-render from stale state | Re-rendering choices first; blur after each fill. |
| Field looks filled but validation says empty | Hidden sync field was edited | Fill the visible editor. |
| Interactive tool crashes on long text | Tool layer unstable for heavy work | Switch to a script. |
| Headless page blocked or different | Site varies by browser context | Direct interface; escalate only for an explicit task, read-only where possible. |
| Wrong account or permission denied | Last-used profile or missing role | Select profile directly; ask user to sign in correctly; re-verify. |
| Direct link warns it will reset settings | Opened a bulk tool, not the item editor | Leave without submitting; navigate normally. |
| Session ends after a page-script request | Internal endpoint called without normal headers | Drive the UI or use a supported API. |
| Warning or security page the tool cannot handle | Needs a person | Ask the user, then re-verify. |

## 12. Report and keep the procedure current

Summarize the outcome in one or two sentences, point to the screenshot and after-state record, and do not paste every field value inline. Store artifacts only where the user can access them, and delete sensitive temporary files when done.

When a run reveals a reusable lesson, add it to your local copy, preferably as one table row with symptom, cause, and fix. Never record credentials or private site data. Merge older entries into general principles as the document grows, and update tool paths, profile mappings, and app-specific notes in place, since they go stale.

## Final audit checklist

- [ ] The least invasive suitable route was used.
- [ ] Visible-browser use was announced and kept to a fresh window or tab.
- [ ] Account, environment, and target were verified before any write.
- [ ] Controls were inspected first and addressed by label, not position.
- [ ] Every meaningful change was read back.
- [ ] The pre-submit gate passed with no empty required fields.
- [ ] Irreversible actions had a pre-action record and authorization.
- [ ] Credentials were entered by the user.
- [ ] Success was confirmed with evidence.
- [ ] The report separates confirmed results from uncertainty.

## Optional extras

**Clipboard and rich paste.** Headless browsers often lack clipboard access, so embed values directly. A synthetic paste event carrying rich and plain text works in some editors and is ignored by others, which may have their own conversion method. Verify through an API or export where possible.

**Uploads that open a native file picker.** Some upload buttons create a file input only on click and open the operating system's picker, which automation cannot drive. Before clicking, add a small page-script override so the new input attaches to the page instead; then click, locate the input, and set a file from an agreed temporary folder. If a preview appears, use its save control, since dismissing it can discard the upload.

**Drag, parallel work, and capture.** Prefer keyboard move commands over dragging, then verify structure. For many independent items, use separate tabs each with the full brief, at a modest concurrency you choose. Background tabs may not render at full size, so bring an item into view before capturing it.

**Devices on the user's own network.** Local devices often serve unencrypted pages that trigger a browser warning. Proceed past it only for devices the user owns and asked about, never for public sites, and use the address the user normally signs in at.

**Apps without an API.** Read configuration from state the page already holds in memory; internal layouts change between versions, so if a read returns nothing, assume the layout moved. Make changes through the editor's UI or paste support, test with a read-only step, then save and re-read. If a page-script loop outlasts your tool's time limit, start it without waiting, store results in a page variable, and poll.

**Schema changes and field deletion.** When an API can create fields but not delete them, delete in the UI. First open the field's dependency view (or a whole-table field manager) to find automations, views, and syncs that use it; scroll virtualized lists step by step to collect every row. Dependency views often miss scripts that reference names, so also search the automation definitions, if needed by repeating the page's own read-only load requests. Retire the field in your own code first, then delete, note whether it went to a restorable trash, and confirm through an API read that it and any synced copies are gone.

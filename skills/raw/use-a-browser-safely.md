---
name: use-a-browser-safely
description: Completes browser tasks safely: least invasive route, verified account and fields, confirmation before irreversible steps. Use when filling forms, fixing dashboards, or working in a signed-in app.
---

# Use a browser safely

Use this workflow when a task has to happen in a web browser: filling a rendered form, changing a dashboard setting, collecting information from a page that only renders with scripts, testing a flow, or working in a signed-in session the user has authorized. It keeps the work on the least invasive route and proves each change landed before anything irreversible happens.

## Quick version

These steps work even with a plain chat assistant that guides you while you do the clicking.

- **Look for a shortcut first.** Ask whether the service has an export, official integration, API, or simple form you can use instead of clicking through a complex page.
- **Check where you are.** Before changing anything, confirm the signed-in account, the workspace or environment, and the exact item you will change. A "permission denied" page usually means the wrong account.
- **List the fields before typing.** Note each field's label, whether it is required, and its kind (one line, multi-line, rich text, dropdown, checkbox, date). Make dropdown, checkbox, and date choices first, because they can reset the form.
- **Read back every field.** After typing, click somewhere neutral and check the value is still there and complete. If the form saves automatically, reopen it and check the saved values.
- **Stop before the final button.** Confirm required fields, values, and whether the action can be undone. Check the final dialog for extra options, such as also emailing people. For payments, sends, deletions, sharing data elsewhere, or "cannot be edited" forms, get a clear yes first.
- **Look for proof afterward.** A confirmation message, reference number, or saved record. If you see an error, check whether the action happened before retrying.

## 1. Follow the central rule

> Inspect the page before you edit anything. Read back every field you change. Do not click the final button until verification passes and the account, target, and authorization are clear.

A fill command usually reports success as long as it did not throw an error. It does not check that the app's internal state updated, that moving focus away committed the value, or that the field kept the content. **The caller verifies. Always.**

## 2. Choose the least invasive route

Use the first route that fits. Do not skip ahead.

1. **Direct interface.** A documented API, export, integration, or plain form endpoint. Look in the service's documentation, the page source (form actions, embedded data), or the requests the page makes. Search and booking widgets often sit on a plain request that is easier to call than the widget is to drive.
2. **Isolated headless browser.** The default for anything that does not need the user's identity: public forms, extraction, UI testing, screenshots. It never touches the user's own browser.
3. **The user's signed-in visible browser.** Only when the task truly needs the user's live session. Never use it for convenience; anything that works headless stays headless.

**Limits.** Do not use undocumented endpoints to get around access controls, terms, rate limits, or anti-abuse systems. In a signed-in session, do not change anything by calling internal endpoints from page scripts; requests missing the app's normal headers can end the session. Reading state the page already holds is lower risk.

**When a person has to act.** If a site blocks headless automation during general research, accept it and move on; escalate to the signed-in browser only when the user explicitly asked for a task on that site. Human-verification checks, security keys, multi-factor prompts, account choosers, and consent screens belong to the user: leave the tab open, say exactly what to click, then re-verify and continue. If you can foresee several such steps, ask once for all of them. Never simulate, bypass, or weaken these checks.

Some pages refuse automation entirely, so every read or screenshot fails. Do not fight them. Check whether an API covers the step (some can update an existing item but not create one). Otherwise prepare everything the user needs, such as files, images, and the exact text for each field, hand over numbered steps, and verify the result afterward where you can.

## 3. Pick the automation style and workspace

- **Step-by-step tool calls** suit one click, one snapshot, or short tasks.
- **A standalone script** suits long text, many fields, heavy single-page apps, or repeatable runs. If an interactive tool crashes or reports that the page or browser closed, switch to a script rather than rescuing the session.

Give each task its own uniquely named working folder (in the system's temporary area or a place the user chose) for scripts, field records, and screenshots. A shared folder lets parallel sessions overwrite each other, so you might verify the wrong run. Pass secrets through environment variables or a secrets store; never hard-code or log them.

## 4. Protect identity, privacy, and the user's browser

When the task touches private messages, records, or information about other people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant pages and data, keep unrelated personal details out of screenshots, logs, and reports, and share results only within the requester's appropriate access boundary.

**Rules for the visible browser:**

- **Announce, then act.** For example, "Taking over the browser to update the billing contact." If the user already authorized it for this task, do not ask again.
- **Work in a fresh window or tab.** Do not reuse the user's tabs unless they point to one.
- **Pick the profile directly.** Classify the task as personal, work, test, or production; if the user says which, that settles it. Generic "current browser" selectors often pick the last-used profile, and display labels can change after restarts, so use a stable identifier. Opening a profile's window does not route automation to it; if no connection appears, the connector in that profile may be signed out or asleep, so ask the user to wake it.
- **Do not restart or force-quit the browser** without explicit OK.

**Account preflight gate.** Before any write, answer: Which account (read from a reliable account page)? Which environment? What exact item will change? If any answer is unclear, stop and ask. If your setup uses a marker that unlocks write actions, set it only after the check passes.

A "permission denied" page usually means the wrong account or a missing role; admin consoles often need a separate admin account, so ask the user to sign in with it. A permission error from your automation tool right after navigating is different: it is often transient while the page loads, so wait and retry.

## 5. Set the task boundary and authorization

Before navigating deeply, identify the target, what will change, the minimum information needed, fields that need the user's judgment, and whether the final action can be undone.

- **Reversible changes** the user asked for can proceed after normal verification.
- **Irreversible or high-impact actions** need a pre-action record and confirmation unless the user already authorized that exact action: payments, sends, invitations, publishing, deletions, ownership or access changes, syncing data to another system, anything labeled "cannot be undone."
- **Autosaving forms have no separate submit.** Each edit goes live as you type, so settle the values and any approval before you start.
- **Credentials stay with the user.** Set up everything around a key or password, then give exact steps to enter it. Never move secrets by automated copy and paste; a copy button can appear to work while the clipboard holds older text.

Honor an explicit request to review first. If authorization is missing, prepare and verify the full result, show it, and ask only for the final action.

## 6. Inspect the page before editing

List every relevant control with its kind, label, required state, current length, and whether it is the real editor, a wrapper, or a hidden sync field.

```text
// Pseudocode: adapt to your automation library
for each c in page.findAll('input, textarea, [contenteditable], [role=textbox]'):
  record { tag, type, label: accessibleLabel(c), required, length }
save to WORK_FOLDER + '/form-before.json'
```

Watch for:

- **Look-alike controls.** Single-line inputs strip line breaks silently. Rich-text editors keep an internal model and may ignore direct value changes.
- **Hidden sync fields and wrappers.** A hidden input beside a visible editor looks fillable, but the form reads the visible editor. Follow the label relationship to the real element.
- **Unstable order.** Never address fields by position; use labels or visible text.
- **Partial page text.** Extraction can skip panels or include hidden labels, so a status word in the text (or its absence) is not proof. Check a screenshot.
- **Warnings about wider effects.** If a page warns that its action will reset broader settings, leave and find the narrower path.

## 7. Use the right interaction for each control

| Control | Preferred interaction | Watch for |
|---|---|---|
| Single-line input | Normal fill | Line breaks removed; length limits. |
| Multi-line text area | Fill, then move focus away; if ignored, type or fire input and change events | Some apps commit only on blur or real input. |
| Rich-text or code editor | Click, select all, delete, insert with keyboard-style input, blur | Direct writes may be ignored. |
| Dropdown or combobox | Choose by exact visible option text, wait to settle | Selection can re-render the form. |
| Checkbox or radio | Read state first; click only if it must change | Clicking toggles a correct value. |
| Date or time picker | Set values, close by clicking neutral background, check the summary | Close or clear buttons may wipe values. |
| File upload | Confirm file, destination, and privacy first | Upload may start at once. |

- **Do re-rendering choices first,** then text. Blur after every rich-text field, and re-check tricky widgets after later edits.
- **If a click does nothing or lands wrong,** wait for the layout to settle, locate the target again, click by position if needed, and confirm from a screenshot.
- **Screens without an API** (builders, admin settings) often ignore simple automation. Use real clicks and typing, change one setting at a time, and confirm each in a preview.

## 8. Verify after every fill

Compare each read-back with what you intended. For sensitive content, compare lengths or a redacted summary. If a value mismatches, retry once with a different method (keyboard input instead of a setter), verify again, and stop and report if it is still wrong.

- **Empty after reported success:** the app ignored a direct write.
- **Short by about one character per paragraph:** a single-line input dropped line breaks.
- **Short after blank lines:** the editor normalized whitespace; usually fine, note it.
- **Earlier field now blank:** a re-render reset uncommitted state.

## 9. Two-phase run and pre-submit gate

**Phase 1: prepare.** Fill, verify each field, save an after-state record and a full-page screenshot. Do not submit.

**Phase 2: commit.** If authorization exists, continue; otherwise show the prepared state and ask. Re-run the gate, click the final control once, and save an after-submit screenshot. A script can use a submit flag that is off by default.

**Pre-submit readiness gate.** Submit only if all are true:

- [ ] Correct account, environment, and target item.
- [ ] Every required field is non-empty and values match intent.
- [ ] Dropdowns, dates, recipients, and attachments are correct.
- [ ] No validation errors or unsaved-change notices remain.
- [ ] The button is the expected one, and the final dialog has no option ticked that widens the action.

A confirmation request for an irreversible action should state the target, key values, audience, any cost, and what cannot be undone.

**Worked example (fictional).** An assistant fills a grant application for the fictional Harbor Lane Arts Collective on the fictional Northwind Foundation portal. Inspection finds a single-line title, a rich-text summary with a hidden sync input beside it, a category dropdown that re-renders the form, and a date picker. It picks the category and date first, fills the visible summary editor with keyboard input and blurs, then fills the title. Read-back shows the summary at 412 of 415 characters (collapsed blank lines, noted) and the title at 0 of 38; a keyboard retry gives 38 of 38. The page says entries cannot be edited later, so the assistant saves a screenshot and asks: "Ready to submit the Harbor Lane application under Community Arts, starting 1 March. It cannot be edited afterward. Submit?"

## 10. Confirm completion

A click is not proof. Look for a success message, a reference number, a new record, or a setting that persists after a safe reload.

- **Errors can be cosmetic.** Some apps show "something went wrong" after the work finished. Check before retrying, since blind retries can duplicate sends or payments.
- **Autosaved forms.** Wait for the saved indicator, then open the form in a second view and read the values back.
- **Use an independent channel** where possible: an API read, a public lookup, or the authoritative source. Know what a record can prove; logs may lack detail or show an intermediary's value rather than the original.
- If you cannot confirm, say what you tried and what remains uncertain. Never report an attempt as a success.

## 11. Common failure patterns

| Symptom | Likely cause | Safe response |
|---|---|---|
| Fill reports success but field is blank, or earlier fields blank out | Direct write ignored; re-render from stale state | Keyboard-style input, blur after each fill, read back. |
| A dropdown or checkbox wipes the form | Selection triggers a re-render | Make those choices first. |
| Field looks filled but validation says empty | Hidden sync field edited, or no real input event | Fill the visible editor; type and delete a character. |
| Tool crashes or the page closes mid-flow | Tool layer unstable for heavy work | Switch to a script. |
| Screenshot does not match what you did | Shared folder overwritten | Use a unique working folder; re-run the check. |
| Wrong account or permission denied | Last-used profile or missing role | Select the profile directly; ask the user to sign in; re-verify. |
| Tab freezes; clicks and screenshots time out | Native dialog or blocking pop-up | Reload; read the message safely or ask the user. |
| Clicks do nothing or reads come back empty or cut off | Panel ignores input; layout shifted; output truncated | Wait, re-locate, click by position, read in slices, undo stray changes. |

## 12. Report and keep the procedure current

Summarize the outcome in one or two sentences, point to the screenshot and after-state record, and do not paste every field value inline. Delete sensitive temporary files when done.

When a run reveals a reusable lesson, record it in your local copy without waiting to be asked. Prefer one table row (symptom, cause, fix) over new prose. A long recipe for one site goes in a separate reference note with a one-row pointer in the failure table; dated incident notes go in a log that normal runs do not read. Never record credentials or private data, and merge older entries into general principles as the document grows.

## Final audit checklist

- [ ] The least invasive suitable route was used.
- [ ] Visible-browser use was announced and kept to a fresh window or tab.
- [ ] Account, environment, and target were verified before any write.
- [ ] Controls were inspected first and addressed by label, not position.
- [ ] Every change was read back, including autosaved values from a second view.
- [ ] The pre-submit gate passed, and irreversible actions had a record and authorization.
- [ ] Steps that need a person were handed over with exact instructions, in as few requests as possible.
- [ ] Success was confirmed with evidence, and uncertainty was reported.

## Optional extras

**Clipboard and files.** Headless browsers often lack clipboard access, so embed values directly. Some upload buttons create a file input only on click and open the system picker, which automation cannot drive; a small page-script override can attach that input to the page instead. If downloads are blocked, use the service's own save-to-storage option or ask the user to download. Read only the files the task needs.

**Testing pasted content.** A simulated paste event skips the browser's own paste handling and can mislead. For a faithful test, put the content on the system clipboard in rich and plain-text forms, focus the editor, and press the paste shortcut through real keyboard input. This overwrites the user's clipboard, so say so first. Read the result from the editor's own content or the service's API.

**Native confirmation dialogs.** After reloading a frozen tab, override the page's confirm function to record the message and decline, click once, and read it. If it is the intended change, override again to accept only that exact message. Reapply after any reload.

**Batches of independent items.** Use separate tabs, each with the full brief, at a modest concurrency you choose. Background tabs may not render fully, so bring an item into view before capturing it.

**Apps without a full API.** Some apps expose editor or configuration state to page scripts; reading it is often faster than driving slow views, but expect it to change between versions. Validate edits first and apply them in one step so a failure cannot leave a half-edited autosaved draft. If output is truncated, keep results in a page variable and read them in slices. For slow log dashboards, repeat the page's own read-only query over small time windows (size is adjustable) and add up the results.

**Admin and schema changes.** Before deleting a field or schema item, check dependencies and automations that use it. To share data with another system, get a plain yes and expose only the minimum fields. When a save needs a security key or password, prepare the change, describe exactly what will happen, leave that step to the user, and verify the saved state afterward.

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
- **Stop before the final button.** Confirm every required field is filled, the values are right, and whether the action can be undone. Check the final dialog for extra options, such as also emailing people. Take a screenshot. For payments, sends, deletions, sharing data elsewhere, or "cannot be edited" forms, get a clear yes first.
- **Look for proof afterward.** A confirmation message, reference number, or saved record. If you see an error, check whether the action happened before retrying.

## 1. Follow the central rule

> Inspect the page before you edit anything. Read back every field you change. Do not click the final button until verification passes and the account, target, and authorization are clear.

A fill command usually reports success as long as it did not throw an error. It does not check that the application's internal state updated, that moving focus away committed the value, or that the field kept the content. **The caller verifies. Always.**

## 2. Choose the least invasive route

Use the first route that fits. Do not skip ahead.

1. **Direct interface.** A documented API, export, integration, or plain form endpoint.
2. **Isolated headless browser.** The default for anything that does not need the user's identity: public forms, extraction from dynamic pages, UI testing, and screenshots. It never touches the user's own browser.
3. **The user's signed-in visible browser.** Only when the task truly needs the user's live session.

**Finding a direct interface.** Read the service's documentation, view the page source for a form action or embedded data, or watch the network requests while using the page normally. Search and booking widgets often sit on a plain request that is easier to call than the widget is to drive. Fall back to the browser when no suitable option exists or the user wants the UI flow.

**Limits.** Do not use undocumented endpoints to get around access controls, terms, rate limits, or anti-abuse systems. In a signed-in session, do not change anything by calling internal endpoints from page scripts; requests missing the app's normal headers can end the session or trigger security responses. Reading state the page already holds is lower risk. If you must read through internal requests, repeat only read-only requests the page itself makes, and stop at the first sign of session trouble.

**Do not use the visible browser for convenience.** It is the user's working space. Anything that works headless stays headless.

**Blocks and checks that need a person.** If a site blocks headless automation during general research, accept it and move on. Escalate to the signed-in browser only when the user explicitly asked for a task on that site, and keep pure lookups read-only. Human-verification checks, security keys, multi-factor prompts, account choosers, and consent screens belong to the user: leave the tab open, tell them exactly what to click, then re-verify and continue. Never simulate, bypass, or weaken these checks, and never disable integrity or signature checks on local tools.

## 3. Pick the right automation style

- **Step-by-step tool calls** suit one click, one snapshot, or short tasks with little text.
- **A standalone script** suits long text, many fields, heavy single-page apps, or repeatable runs.

Interactive tool layers can crash on long text, parallel actions against one page, or heavy rendering. If you see an error like "page, context, or browser has been closed," switch to a script instead of rescuing the session. Save scripts and artifacts in a temporary folder the user agreed to, run headless unless a visible session is part of the plan, and pass secrets through environment variables or a secrets store. Never hard-code or log credentials.

## 4. Protect identity, privacy, and the user's browser

When the task touches private messages, records, or information about other people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant pages and data, keep unrelated personal details out of screenshots, logs, and reports, and share results only within the requester's appropriate access boundary.

**Rules for the visible browser:**

- **Announce, then act.** Say briefly what you are taking over and why, for example "Taking over the browser to update the billing contact." If the user already authorized it for this task, do not ask again.
- **Work in a fresh window or tab.** Do not reuse the user's tabs unless they point to one. When a site opens or closes tabs, refresh your list of open tabs before acting again.
- **Classify the context, then pick the profile directly.** Personal, work, test, or production. If the user says which, that settles it. A generic "current browser" selector often picks the last-used profile, and display labels can change after restarts, so use a stable identifier where available and verify every time.
- **A window is not a connection.** Opening a profile's window does not route the automation to it. If no connection appears, the connector in that profile may be signed out or asleep; ask the user to wake or sign in to it, then check again.
- **Do not restart or force-quit the browser** without explicit OK. It closes everything the user has open.

**Account preflight gate.** Before any write, answer: Which account is this (read it from a reliable account page)? Which environment or workspace? What exact item will change? If any answer is unclear, stop and ask. If your setup uses a verification marker that unlocks write actions, set it only after the check has actually passed, and record the evidence.

**Permission denied means wrong account, not a puzzle.** Admin consoles often need a separate administrative account. Do not hunt for workarounds; ask the user to sign in with the right account, reload, and re-run the check. Separate this from a "permission denied" raised by your automation tool right after a navigation: that is often transient while the page loads. Take a screenshot, wait, and retry, in a fresh tab if needed.

## 5. Set the task boundary and authorization

Before navigating deeply, identify the target, what will be entered or changed, the minimum information needed, fields that need the user's judgment, and whether the final action can be undone.

- **Reversible changes** the user asked for, such as toggling a setting or updating a draft, can proceed after normal verification.
- **Irreversible or high-impact actions** need a pre-action record and confirmation unless the user already authorized that exact action: payments, sends, invitations, publishing, deletions, plan or access changes, sharing or syncing data to another system, and anything labeled "cannot be undone." A restorable trash lowers risk but does not replace authorization.
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
- **Unstable order.** Never address fields by position. Read existing values before overwriting.
- **Page text is not the whole page.** Text extraction can skip side panels and overlays while including hidden labels, so a status word in the text is not proof anything happened. Check a screenshot or read the panel directly.
- **The page is not what you expected.** If a saved link opens a view where expected entries are missing, or that warns submitting will reset broader settings, leave without submitting and navigate there normally.

## 7. Use the right interaction for each control

| Control | Preferred interaction | Watch for |
|---|---|---|
| Single-line input | Normal fill | Line breaks removed; length limits. |
| Multi-line text area | Fill, then move focus to the page body | Some apps commit only on blur. |
| Rich-text editor | Click, select all, delete, insert text with keyboard-style input, blur | Direct DOM writes may be ignored. |
| Code editor widget | Set the value through the widget's own interface, then type and delete one character | The form may not register a value it did not see typed. |
| Dropdown or combobox | Choose by exact visible option text, wait to settle | Selection can re-render the form. |
| Checkbox or radio | Read state first; click only if it must change | Clicking toggles a correct value. |
| Date or time picker | Set values, close by clicking neutral background, check the summary | Close or clear buttons may wipe values. |
| File upload | Confirm file, destination, and privacy first | Upload may start at once. |

- **Blur after every rich-text field.** Otherwise the next edit can re-render earlier editors from stale state, and only the last field survives.
- **Order matters.** Do re-rendering choices first, then text. Re-inspect after each choice, and re-check tricky widgets after later edits.
- **If a click does nothing,** take a screenshot, click by position, and confirm the view changed. Slow checks may take a while; wait rather than clicking again.
- **Native confirmation boxes block automation.** A browser-level confirm dialog can freeze the tab so clicks and screenshots time out. Reload to recover, then read the message before acting (see Optional extras). Dialogs drawn inside the page itself are safe to handle normally.
- **Check summaries before creating.** When a setup step shows a summary, such as a count of permissions, items, or recipients, confirm it matches intent before continuing.
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
- [ ] The final confirmation dialog has no option ticked that widens the action, such as also emailing subscribers, unless that was intended.

**If any required field is empty, do not submit.** A confirmation request for an irreversible action should state the target, key values, audience, any cost, and what cannot be undone.

**Worked example (fictional).** An assistant fills a grant application for the fictional Harbor Lane Arts Collective on the fictional Northwind Foundation portal. Inspection finds a required single-line title, a required rich-text summary with a hidden sync input beside it, a category dropdown that re-renders the form, and a date picker. It picks the category first, sets the date, fills the visible summary editor with keyboard input and blurs, then fills the title. Read-back shows the summary at 412 of 415 characters (collapsed blank lines, noted) and the title at 0 of 38; a keyboard retry gives 38 of 38. The page says entries cannot be edited later, so the assistant saves a screenshot and asks: "Ready to submit the Harbor Lane application under Community Arts, starting 1 March. It cannot be edited afterward. Submit?"

## 10. Confirm completion

A click is not proof. Look for a success message, a reference number, a new record, or a setting that persists after a safe reload.

- **Errors can be cosmetic.** Some apps show "something went wrong" after the work finished. Check before retrying, since blind retries can duplicate sends, payments, or records.
- **Frozen pages.** A blocking pop-up can freeze the tab. Reload, or ask the user to respond to it, then continue.
- **Use an independent channel.** Confirm through an API read, a public lookup, or the authoritative source rather than a cached copy. Public pages may be cached for a short while, so allow for that before concluding a change failed, and avoid test parameters that trigger extra pop-ups. For access rules, a harmless request that exercises the setting without signing in or changing anything, compared with a case that should be rejected, is good evidence.
- **Know what a record can prove.** Logs and error reports may lack the detail you want, or show an intermediary's value, such as a proxy's address instead of the visitor's. State the limit rather than guessing.
- If you cannot confirm, say what you tried and what remains uncertain. Never report an attempt as a success.

## 11. General failure patterns

| Symptom | Likely cause | Safe response |
|---|---|---|
| Fill reports success but field is blank, or earlier fields blank out as later ones are filled | App ignored a direct write and re-renders other fields from stale state | Keyboard-style input, blur right after each fill, read back. |
| A dropdown or checkbox wipes the form | Selection triggers a full re-render | Make re-rendering choices first, then fill text. |
| Field looks filled but validation says empty | Hidden sync field was edited, or widget did not see a keystroke | Fill the visible editor; type and delete one character. |
| Interactive tool crashes on long text, parallel actions, or heavy pages | Tool layer unstable for heavy work | Switch to a script; do not try to rescue the session. |
| Headless page blocked or different | Site varies by browser context | Direct interface; escalate only for an explicit task, read-only where possible. |
| Wrong account or site says permission denied | Last-used profile or missing role | Select profile directly; ask user to sign in correctly; re-verify. |
| Tool reports permission denied right after navigating | Page still loading | Screenshot, wait, retry in a fresh tab if needed. |
| Tab freezes; clicks and screenshots time out | Native confirm dialog or blocking pop-up | Reload; read the message safely or ask the user. |
| Session ends after a page-script request | Internal endpoint called without normal headers | Drive the UI or use a supported API. |
| Clicks do nothing, or a read misses part of the page or comes back cut off | Panel ignores clicks or extraction; tool truncates output | Screenshot, click by position, read the panel directly, read long results in slices. |
| Warning, sign-in, or consent page the tool cannot handle | Needs a person | Leave the tab open, ask the user, then re-verify. |
| A known tricky site comes up again | Site has quirks already worked out | Read that site's reference note before starting. |

## 12. Report and keep the procedure current

Summarize the outcome in one or two sentences, point to the screenshot and after-state record, and do not paste every field value inline. Store artifacts only where the user can access them, and delete sensitive temporary files when done.

When a run reveals a reusable lesson, such as a new failure mode, a working pattern, or a missing tool, record it in your local copy without waiting to be asked. Prefer one table row with symptom, cause, and fix on the same row over new prose. Decide where each lesson belongs:

- **General patterns** go in the main procedure.
- **A recipe for one site** that runs longer than a short paragraph goes in a separate reference note, with a one-row pointer in the failure table saying when to read it.
- **Dated incident notes** go in a separate log that normal runs do not read.

Never record credentials or private site data. Merge older entries into general principles as the document grows, and update tool paths, profile mappings, and app-specific notes in place, since they go stale.

## Final audit checklist

- [ ] The least invasive suitable route was used.
- [ ] Visible-browser use was announced and kept to a fresh window or tab.
- [ ] Account, environment, and target were verified before any write.
- [ ] Controls were inspected first and addressed by label, not position.
- [ ] Every meaningful change was read back.
- [ ] The pre-submit gate passed with no empty required fields and no unintended options ticked.
- [ ] Irreversible actions had a pre-action record and authorization.
- [ ] Credentials, sign-ins, and verification checks were handled by the user.
- [ ] Success was confirmed with evidence.
- [ ] The report separates confirmed results from uncertainty.

## Optional extras

**Clipboard, paste, and uploads.** Headless browsers often lack clipboard access, so embed values directly. A synthetic paste event works in some editors and is ignored by others, which may offer their own conversion method. Some upload buttons create a file input only on click and open the operating system's picker, which automation cannot drive; a small page-script override can attach that input to the page so you can set a file from an agreed temporary folder. If a preview appears, use its save control, since dismissing it can discard the upload.

**Native confirmation dialogs.** After reloading a frozen tab, override the page's confirm function so it records the message and declines, click once, and read the message. If it is the change you intend, override again to accept only that exact message, then click. Pages often reload after an accepted change, which removes the override, so reapply it each time and never queue further clicks behind it.

**Batches of independent items.** Use separate tabs, each with the full brief, at a modest concurrency you choose. Prefer keyboard commands over dragging when rearranging, then verify structure. Background tabs may not render fully, so bring an item into view before capturing it.

**Editing through an editor's document model.** Some rich editors expose their internal editor object to page scripts. Walk the document to find the exact position and insert content through the editor's own commands instead of typing. Validate every planned change first, then apply all changes to one item in a single transaction, because a failure partway through can leave a half-edited draft that autosaves. For many items, keep the edit function somewhere that survives navigation, such as session storage, and work a few items per batch. Wait for the saved indicator, go through the update dialog using the pre-submit gate, then verify through a public read.

**Apps without a full API.** Read configuration from state the page already holds in memory; internal layouts change between versions, so an empty read usually means the layout moved. If a page shows only part of a record, the app's own read-only requests, repeated from a tab on the same site, may return the full detail. Make changes through the UI, test with a read-only step, then save and re-read. If a page-script loop outlasts your tool's time limit, start it without waiting, store results in a page variable, and poll. If the tool blocks certain characters in scripts you send, build them indirectly, for example from character codes. If returned text gets cut off or filtered, keep the full result in a page variable and read it back in slices under the limit, then reassemble before drawing conclusions.

**The user's own devices.** Local devices often serve unencrypted pages that trigger a browser warning; proceed past it only for devices the user owns and asked about. When away from that network, diagnose through the app's signed-in remote page, using the read-only logs, history, and event views it already exposes. If a source refuses access, accept that rather than looking for another way in.

**Schema and data-sharing changes.** Before deleting a field, check the tool's dependency view and search automation scripts that may reference it by name, retire it in your own code first, then confirm the result through an API read. To share data with another system, get a plain yes, expose only a dedicated view that hides everything the destination should not receive, lock that view with a short note, and verify the new copy.

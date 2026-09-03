---
name: use-a-browser-safely
description: Complete browser-based tasks safely by selecting the least invasive authorized method, protecting account context and private information, verifying rendered page state, and separating preparation from consequential final actions.
---

# Use a browser safely

Use this workflow for website tasks that require real interaction: completing rendered forms, collecting data from dynamic pages, testing a flow, changing account settings, or working in an authenticated dashboard. Use it when a normal page request, supported integration, or authorized API cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until the account, target, authorization, and page state are verified.

A browser automation command returning success does **not** prove the site accepted a change. Modern web applications can keep internal state separately from the DOM, commit a value only when focus leaves a field, replace controls during a re-render, or show an error even after an action actually completed.

## 1. Confirm purpose, authority, and scope

Before accessing a logged-in website, private communication, record, or dashboard, establish that the task has a legitimate purpose and that the requester is authorized to direct it.

Identify:

- The exact target page, account, environment, record, or workflow.
- What information will be viewed, entered, changed, uploaded, or collected.
- The minimum data necessary to complete the request.
- Whether the action is reversible.
- Whether the task will send, publish, pay, delete, grant access, change billing, or otherwise create an external commitment.
- Any missing facts or choices that require the user's judgment.

Use only the minimum relevant sources and personal information. Do not put unrelated personal details into browser logs, screenshots, temporary files, or final reports. Keep outputs within the requester's appropriate access boundary. Do not expose credentials, session tokens, recovery details, or sensitive account data.

If the target, authority, intended audience, or impact is unclear, stop and ask before changing data.

## 2. Choose the least invasive suitable route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized API, integration, export, or ordinary form endpoint when it can perform the requested operation safely.
2. **Headless browser automation.** Use this for public pages, test environments, rendered-page extraction, screenshots, UI tests, and tasks that do not need an existing signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an established account session, single sign-on state, or account-specific dashboard.

Before driving a browser, inspect official documentation, ordinary form actions, page source, and visible request behavior for a supported programmatic path. A form may have an authorized structured submission route that is more reliable than reproducing complex browser interactions.

Do not use undocumented interfaces to bypass access controls, consent boundaries, terms, security controls, payment walls, or anti-abuse protections. If automated browsing is blocked during general research or collection, report the limitation rather than escalating to evade the block. A visible session can be appropriate for an explicitly requested, legitimate task on that site when the user already has authorized access and a normal session is necessary.

Do not use a live authenticated browser merely for convenience when a headless or direct route will work. It can interrupt the user's work and exposes more account and privacy context.

## 3. Protect browser, account, and environment context

When using a visible or authenticated browser:

- Announce that browser control is beginning and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly directs work in an existing tab.
- Explicitly classify the needed context, such as personal, work, test, staging, or production.
- Select the browser profile or session connection for that context directly. Do not rely on generic browser selection, recent-use order, tab titles, or connection labels.
- Confirm the signed-in account and environment using a reliable account indicator before opening or changing the actual target.
- Confirm the target object before editing: for example, the correct record, recipient list, workspace, or subscription.
- Do not disable browser protections, multi-factor authentication, security warnings, access controls, or anti-abuse controls to make automation easier.

Treat browser identity verification as a preflight gate. The minimum question is:

> Which account is active, which environment is active, and what exact item will change?

If an automation system has a verification marker or permission gate, enable it only after the account check has actually passed. Never create a marker early simply to unlock write actions.

For private information about people, access only the records required for the stated task. Omit unrelated sensitive details from screenshots, notes, and reports.

## 4. Separate preparation from commitment

Separate reversible preparation from irreversible commitment.

Preparation can include drafting text, filling fields, selecting options, collecting a preview, or assembling an upload. Commitment includes submitting, sending, publishing, paying, deleting, changing access, or applying a final plan or billing change.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify the resulting state, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Obtain explicit confirmation of the prepared state. Re-check the account, target, and readiness gate, then perform the final action once.

If the page reloads, re-renders, or the session changes between phases, do not assume prior values persisted. Re-inspect, restore if needed, and verify again.

Explicit confirmation is normally required immediately before:

- Sending a message, invitation, notification, or application.
- Publishing content or submitting an externally reviewed form.
- Making a payment, purchase, or donation.
- Deleting records, files, or content.
- Changing subscription, billing, ownership, access, security, or plan settings.
- Taking an action labeled permanent, final, irreversible, or impossible to edit later.

For a reversible, low-risk change that the user explicitly requested, normal verification is usually enough unless the page presents an unexpected warning or broader impact.

## 5. Inspect the rendered page before editing

Do not begin by guessing selectors, using control indexes, or trusting a visual approximation. Inspect the rendered page first.

For each relevant control, determine:

- Its type: single-line input, multiline area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Its accessible name, visible label, placeholder, or explicit label relationship.
- Its current value, required state, disabled state, and validation requirements.
- Whether it is the actual editable element, a wrapper, or a hidden synchronization field.
- Whether changing it or a related control causes a re-render.

Address controls by stable semantic identity: accessible name, visible label, or a label relationship. Do not use DOM order when labels are available, because dynamic applications can reorder or replace elements during loading and re-rendering.

Before editing an existing record or setting, inspect its current state. This helps avoid changing the wrong item or overwriting information unintentionally.

### Generic inspection pattern

Use the chosen browser automation capability to list relevant controls before writing interaction logic. Record at least tag, type, role, label, required state, and current value or text length.

```js
// Pseudocode: adapt to the selected browser automation capability.
const controls = inspectAll('input, textarea, [contenteditable="true"], [role="textbox"]')
  .map((element) => ({
    tag: element.tagName,
    type: element.type || element.contentEditable,
    role: element.getAttribute('role'),
    label: accessibleLabel(element),
    required: element.required || element.getAttribute('aria-required') === 'true',
    valueLength: readableValue(element).length,
  }));

saveJson('form-before.json', controls);
```

## 6. Use the interaction method that matches the control

A generic “set value” action is not reliable for every web control.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use normal text-input interaction | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away | The application may commit on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select existing text, enter text through keyboard-style events, then blur | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, and wait for state to settle | Selection may trigger a full re-render. |
| Checkbox or radio group | Read current state first; change only when needed | A click may toggle an already-correct value. |
| Date or time picker | Select values, close using a neutral page action where possible, then verify the displayed summary | The popover can clear, reinterpret, or reset related values. |
| File upload | Confirm the file, destination, and privacy implications first | Uploading may start immediately and be hard to reverse. |

For framework-driven editors, simulate normal user interaction instead of writing to low-level DOM properties. A robust sequence is:

1. Focus the actual editable element.
2. Select existing text.
3. Delete it.
4. Enter the new text through keyboard-style input.
5. Move focus to a neutral page element to commit the change.
6. Wait briefly for the application to settle.
7. Read the value back.

Some forms pair a visible editor with a hidden input. Changing the hidden input can look successful in an inspection result while server-side validation treats the visible editor as empty. Target the interactive control the application actually reads. If an accessibility locator finds an empty wrapper, inspect the underlying editable control and its label relationship.

If dropdowns, checkboxes, tabs, date pickers, or other controls can refresh the form, set and verify those dependencies **before** filling long or complex text. Re-inspect afterward to ensure earlier values remain present.

## 7. Verify every meaningful edit

After each meaningful field edit or setting change, read the state back from the page. Compare the actual visible or accessible value with the intended value.

For sensitive content, verify a minimal safe representation, such as length, required state, a redacted excerpt, or a checksum-like comparison, rather than placing full private content in logs.

Check specifically for:

- Automation reports success but the field remains empty.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated due to a single-line control or length limit.
- Text displays but was not retained by the application's internal state.
- Editing a later field erased an earlier field after a re-render.
- A hidden synchronization field was changed instead of the visible editor.
- A selection changed a dependent recipient, date, option, validation rule, or required field.

If verification fails, do not continue toward submission. Diagnose the actual control type, retry once with a more suitable interaction method, and verify again. If the page still alters or rejects the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 8. Run a pre-action readiness gate

Before submitting or making any high-impact change, inspect the relevant page state again. Confirm all of the following:

- The correct account, organization, and environment are active.
- The target item is the intended one.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Recipients, options, dates, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final control has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **do not submit**. A partially filled form is usually recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store it only through an appropriate access boundary. Avoid pasting a large table of sensitive field values into a chat or report when a brief summary and a securely available record are enough.

### Readiness checklist

- [ ] Account, environment, and target are verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 9. Confirm completion after acting

A click is not evidence of completion. After a final action, look for reliable evidence such as a success notice, confirmation reference, newly created record, persisted setting, sent item, published page, or changed status that remains after a safe refresh.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, the available evidence, and what remains uncertain. Do not present an attempted action as completed.

## 10. Common failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after a later edit | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline or editor control, or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the underlying labeled control and target the actual editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control that the application reads. |
| The automation layer becomes unstable on a complex page | The selected browser method is unsuitable | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers behave differently | The site varies behavior by browser context | Prefer an authorized direct interface; if a visible session is necessary for an explicit task, verify its account and proceed normally without evasion. |
| A date or option popup changes values unexpectedly | The widget has stateful close, clear, or parsing behavior | Close it through a neutral page action and re-verify all affected fields. |
| A visible error may be cosmetic | The requested task may already have completed | Inspect the resulting state before retrying. |
| Account or environment is uncertain | The wrong profile, tenant, or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## Final audit checklist

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back and verified.
- [ ] Required fields and validation state passed the readiness gate.
- [ ] A pre-action record was captured when the action was consequential.
- [ ] Explicit confirmation was obtained immediately before a consequential final action.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

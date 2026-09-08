---
name: use-a-browser-safely
description: Complete browser-based tasks safely by selecting the least invasive authorized method, verifying account context and rendered state, and separating preparation from consequential final actions.
---

# Use a browser safely

Use this workflow for browser-based work such as completing rendered forms, changing settings, collecting data from dynamic pages, testing a user flow, or using an authenticated dashboard. Use it only when a supported direct interface, API, or ordinary page retrieval cannot safely and reliably complete the request.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and never take a consequential final action until the account, target, authorization, and page state are verified.

A successful automation command does not prove that a website accepted the change. Modern applications may keep their own internal state, commit fields only after focus leaves them, replace controls during a re-render, or display an error even when an action actually completed.

## 1. Select the least invasive suitable method

Choose the first method that fits the task safely:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic route when it can complete the task. It is often more reliable than simulating a browser.
2. **Headless browser automation.** Use this for public pages, test systems, rendered-page extraction, screenshots, and forms that do not require the user's existing signed-in identity.
3. **User-visible authenticated browser.** Use this only when the task genuinely needs an existing session, single sign-on, an account-specific dashboard, or the user explicitly directs work in that context.

Before driving a browser, check for a legitimate direct route. Review official documentation, ordinary form actions, page source, and visible network requests for supported endpoints. A web form may submit structured data to an authorized service directly.

Do not use undocumented interfaces to bypass access controls, consent boundaries, service restrictions, or security protections. Do not use an authenticated visible session merely for convenience: it can interrupt the user's work and increases privacy and account risk.

If a site blocks automation, do not try to defeat the block for research, casual data collection, or access that is unavailable through normal means. A visible browser may be appropriate only for a legitimate, user-requested task on that specific site when the user has authorized access and an established session is necessary. Do not weaken browser security, access controls, warnings, or anti-abuse protections.

## 2. Protect authorization, privacy, and account context

When a task involves private communications, records, account dashboards, or information about people, establish a legitimate purpose and clear authorization. Access only the minimum relevant pages, records, and fields. Do not put unrelated personal information into screenshots, logs, notes, or reports. Keep all outputs within the requester's appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated context, identify the correct:

- Account and signed-in identity.
- Organization, workspace, or tenant.
- Environment, such as personal, work, test, staging, or production.
- Target page, record, setting, or transaction.
- Scope of authority for the requested action.

Never infer account identity from a generic browser name, tab title, remembered default, or connection label. Those signals can be stale or ambiguous.

Use these operating rules:

- Announce when taking control of a user-visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing tab to use.
- Classify the required context explicitly, such as personal, work, testing, or production.
- Select the browser profile or session associated with that context rather than using a generic or most-recent browser selector.
- Verify the signed-in account through a reliable account indicator before opening the real target or changing data.
- If the account, target, environment, authority, or requested scope is uncertain, stop and ask before making changes.
- Do not expose credentials, session tokens, recovery details, private account information, or security settings in output or logs.
- Do not disable multi-factor authentication, browser warnings, access restrictions, or other security controls to make a task easier.

If the automation environment has an account-verification gate, unlock or mark the session as verified only **after** the actual account check has passed. Do not create a marker, flag, or bypass before verification merely to enable browser actions.

A useful account preflight question is:

> Which account and environment are active, what exact object will change, and what authority permits this action?

Resolve uncertainty before continuing.

## 3. Establish the task boundary

Determine the desired outcome before navigating deeply. Identify:

- The target page, form, record, setting, or workflow.
- The information to enter, collect, modify, or upload.
- The minimum information needed to complete the request.
- Existing data that must not be overwritten.
- Whether the action is reversible.
- Whether the task sends, publishes, pays, deletes, changes a plan, changes access, or otherwise creates an external commitment.
- Missing details and choices that require the user's judgment.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and creating a preview may be reversible. Submitting, sending, publishing, purchasing, deleting, or applying a consequential change may not be.

For consequential work, use two phases:

1. **Preparation pass:** Fill or configure the page, verify the resulting state, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** After explicit user confirmation, re-check the account, target, and readiness gate. Then perform the final action once.

If the page reloads, re-renders, or the session changes between phases, do not assume the prepared state remains valid. Re-inspect, restore values if necessary, and verify again.

## 4. Inspect the rendered page before editing

Do not start by guessing selectors, filling controls by numeric position, or trusting a visual resemblance. First inspect the rendered page sufficiently to identify the true interactive controls.

For each relevant control, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, file upload, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value, required status, disabled state, and validation message.
- Character limits and formatting behavior.
- Whether an apparent field is an editable control, wrapper, or hidden synchronization element.
- Whether changing it or a related control causes a page re-render.

Address controls by stable semantic identity: visible label text, accessible name, or an explicit label relationship. Do not use DOM indexes where semantic labels exist. Dynamic applications may reorder controls during hydration or after changing another field.

Inspect the current state before changing a record or setting. This prevents modifying the wrong item or unintentionally replacing existing data.

### Generic inspection pattern

Use the chosen browser capability to list relevant controls before writing interaction logic. Record at least the tag, input type, role, label, required status, and current value or text length.

```js
// Pseudocode: adapt to the chosen automation library.
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

## 5. Use an interaction method that matches the control

A generic value-setting command is not reliable for every control. Use interaction that resembles ordinary user input when a framework-managed editor needs it.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use the normal text-input mechanism. | Line breaks may be silently removed. |
| Multiline text area | Fill text, then move focus away. | The application may commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select old text, delete it, enter text through keyboard-style events, then blur. | Direct DOM writes may not update the application's internal state. |
| Dropdown or combobox | Open it, choose by visible option text, then wait for state to settle. | Selection may trigger a re-render. |
| Checkbox or radio control | Read current state first; change only if needed. | A click can reverse an already-correct value. |
| Date/time picker | Choose the date and time, then verify the rendered summary. | Popovers may clear related values or reinterpret later typing. |
| File upload | Confirm the file, destination, recipients, and privacy implications first. | Uploading may begin immediately and may be difficult to undo. |

For a framework-driven editor, a robust general sequence is:

1. Locate the actual editable element, not only its wrapper.
2. Focus it.
3. Select existing content and delete it.
4. Enter the requested text through keyboard-style input.
5. Move focus to a neutral page element to commit the edit.
6. Wait briefly for rendering to settle.
7. Read the value back from the visible or accessible page state.

Some forms pair a visible editor with a hidden input. Updating the hidden input may look successful in a DOM inspection while server validation treats the visible editor as empty. Target the interactive editor that the application actually uses. If an accessibility locator returns an empty wrapper, inspect the underlying labelled editable element.

If a dropdown, checkbox, tab, category, or date selection can refresh the form, perform and verify those actions **before** entering lengthy or complex text. Re-inspect afterward and confirm earlier values still exist.

## 6. Verify after every meaningful edit

After filling a field or changing a setting, read it back from the rendered page. Compare the actual value with the intended value. For sensitive material, compare value length, required state, or a minimal redacted summary rather than copying the complete text into logs.

Look for these mismatches:

- Automation reports success, but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the field is single-line or has a limit.
- A custom editor displayed text but did not retain it internally.
- Editing a later control erased an earlier field after re-rendering.
- A hidden synchronization field changed instead of the visible editor.
- A selection changed a dependent recipient, date, validation rule, or required field.

If verification fails, do not continue toward submission. Diagnose the control type and retry once with a more appropriate interaction method. Verify the retry. If the page still changes, rejects, or cannot reliably display the intended value, report the limitation and ask how to proceed rather than silently submitting inaccurate content.

## 7. Run a pre-action readiness gate

Before any final submission or high-impact change, inspect the relevant page state again. Confirm all of the following:

- The correct account, organization, and environment are active.
- The target item is the intended one.
- Every required field is present and non-empty.
- Each important value matches the request closely enough.
- Recipients, options, dates, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **do not submit**. A partially completed page is often recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store it only in an authorized location. Avoid placing large amounts of sensitive field content in chat when a short summary and controlled-access record are sufficient.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 8. Require confirmation for one-way actions

Get explicit confirmation immediately before actions that are difficult to reverse, including:

- Sending messages, invitations, or notifications.
- Publishing content.
- Submitting official, externally reviewed, or final forms.
- Making a payment or purchase.
- Deleting records or files.
- Changing billing, subscription, access, ownership, or security settings.
- Actions described as permanent, final, irreversible, or not editable later.

Use this confirmation format:

> Ready to [final action] for [target]. Key details: [concise summary]. Impact: [cost, audience, permanence, or other consequence]. Open questions: [none or list]. Proceed?

Wait for an affirmative response before activating the final control. For low-risk, reversible changes explicitly requested by the user, proceed after normal verification unless the page presents an unexpected warning or broader impact.

## 9. Confirm completion, not merely a click

A button click is not proof of success. After the final action, seek reliable evidence such as a success message, confirmation reference, created record, persisted setting, sent item, published item, or changed status that remains after a safe refresh.

If the site shows an error, preserve the relevant message and inspect the resulting state before retrying. An apparent error can be cosmetic, while a blind retry can create duplicates such as repeated submissions, payments, messages, or records.

If completion cannot be verified, state what was attempted, the evidence available, and what remains uncertain. Do not describe an attempted action as completed.

## 10. Common failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change. | Use focus-and-keyboard interaction, blur, and read back. |
| Earlier fields disappear after a later edit | A re-render reset uncommitted state. | Commit and verify each field; make re-rendering selections first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used. | Find a multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node. | Inspect the labelled underlying control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited. | Use the visible interactive control that the application reads. |
| Automation is unstable on a complex page | The selected automation layer is unsuitable. | Switch to a more robust browser method or supported interface; do not blindly rescue a broken session. |
| Headless and visible browsers behave differently | The site varies behavior by browser context. | Prefer an authorized direct route; for an explicit legitimate task, use a verified visible session without evasion. |
| A popup changes dates or other fields unexpectedly | The widget has stateful close, clear, or parsing behavior. | Close through a neutral page action and re-verify all affected values. |
| An error appears after an action | The operation may have succeeded despite a cosmetic error. | Inspect the resulting state before retrying. |
| Account context is uncertain | The wrong profile, workspace, or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
- [ ] The report separates confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

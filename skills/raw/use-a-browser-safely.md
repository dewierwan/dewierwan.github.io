---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and private data, verifying rendered page state, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing rendered forms, changing settings, collecting data from dynamic pages, testing a user flow, or working in an authenticated dashboard. Use it when a supported direct interface, ordinary page retrieval, or static request cannot safely and reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and never perform a consequential final action until the account, target, page state, and authorization are clear.

A successful automation command does not prove that a website accepted a change. Modern applications may keep internal state separate from visible DOM properties, commit edits only when focus leaves a field, replace controls after a re-render, or show an error even though an action actually completed.

## 1. Choose the least invasive suitable route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented and authorized programmatic interface when it can complete the requested task. It is often more reliable than recreating browser interactions.
2. **Headless browser automation.** Use this for public pages, test environments, routine dynamic-page extraction, screenshots, UI testing, and forms that do not require the user's established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing account session, single sign-on state, account-specific dashboard, or user-directed browser context.

Before driving a browser, look for a direct route. Review official documentation, ordinary form actions, page source, and visible network activity for supported endpoints. A rendered form may submit structured data to an authorized service that is safer and more dependable to use directly.

Do not use undocumented interfaces to bypass access controls, consent boundaries, terms, or technical restrictions. Do not use an authenticated visible session just because it is convenient: it can interrupt the user's work and creates greater privacy and account risk.

If a site blocks automation, do not evade its protections for casual research or collection. A verified visible session can be appropriate only when the user explicitly asked for a legitimate task on that specific site, authorized access is clear, and the established session is necessary. Do not weaken browser security, access controls, warnings, multi-factor authentication, or anti-abuse protections.

## 2. Protect account identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into notes, screenshots, logs, or reports. Keep outputs within the requester's appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated context, explicitly identify the correct account, organization, environment, and browser profile. Never infer identity from a generic browser-window name, an old tab title, remembered defaults, or an arbitrary connection label.

Use these rules:

- Announce when taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing page.
- Classify the intended context: for example, personal, work, test, staging, or production.
- Select the browser profile or connection that matches that context; do not rely on a generic browser selector or most-recent profile.
- Confirm the signed-in account through a reliable account indicator before opening or changing the real target.
- If the account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not reveal credentials, session tokens, recovery details, private account data, or security settings in output or logs.
- Do not disable security controls, browser warnings, access restrictions, or authentication requirements to make automation easier.

Use an account preflight gate before actions that modify data. Confirm: **Which account is this? Which environment is this? What exact item will change?** If any answer is uncertain, resolve it first.

If the automation environment has a verification marker, permission gate, or similar mechanism, mark the context verified only *after* the account check has passed. Never create a marker early merely to unlock actions.

## 3. Establish the task boundary and authorization

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, or workflow.
- The information that will be entered, collected, changed, or uploaded.
- The minimum information needed to complete the task.
- Whether the final action is reversible.
- Whether the task involves sending, publishing, paying, deleting, granting access, changing a plan, or another external commitment.
- Missing information, ambiguous choices, and fields that require the user's judgment.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and collecting a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, or applying an irreversible account change may not be.

Use two phases for consequential tasks:

1. **Preparation pass:** Fill or configure the page, verify values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Confirm that authorization covers the exact final action, re-check account, target, and readiness, then activate the final control once.

Honor an explicit request to review before submission. If clear task instructions or standing authorization already cover a reversible requested change or a specified final action, do not ask again without a reason. If authorization for the final action is absent, prepare and verify the result, show a concise pre-submit summary, and ask only for the missing authorization.

For payments, sends, deletions, plan or billing changes, access changes, and anything labeled permanent, final, or impossible to undo, capture the pre-action state and obtain explicit approval immediately before the final action unless the user has unambiguously authorized that exact commitment.

## 4. Inspect the rendered page before editing

Do not start by guessing selectors, filling controls by numeric position, or trusting a visual approximation. First inspect the rendered page and gather enough structure to identify controls safely.

For each relevant control, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether it is required.
- Validation rules, character limits, formatting behavior, and disabled state.
- Whether an apparent field is the true editable control, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, date, or tab causes the page to re-render.

Address controls by stable semantic identity, such as visible label text, an accessible name, or a label relationship. Do not use DOM indexes when labels are available: dynamic applications can change element order during hydration or after a re-render.

Before changing a record or setting, inspect its current state. This prevents changing the wrong item or overwriting existing values unintentionally.

### Generic inspection pattern

Use the chosen browser automation library to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

```js
// Pseudocode: adapt to the selected automation library.
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

## 5. Use the correct interaction for each control

A generic “set value” operation is not reliable for every control. Use interaction patterns that resemble normal user input, then verify the resulting state.

| Control type | Preferred interaction | Important verification |
|---|---|---|
| Single-line input | Use normal text entry or fill interaction | Confirm line breaks were not silently removed. |
| Multiline text area | Fill text, then move focus away | Confirm blur committed the full text. |
| Rich-text or content-editable editor | Focus the true editor, select existing content, delete, enter text with keyboard-style events, then blur | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle | A selection may cause a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed | Avoid toggling an already-correct value. |
| Date/time picker | Set date and time, then verify the rendered summary | Popovers can clear or reinterpret related values. |
| File upload | Confirm file, destination, and privacy implications first | Uploading may begin immediately and may be difficult to undo. |

For framework-driven editors, do not rely on changing low-level page properties. A robust sequence is: focus the actual editable element, select old text, delete it, enter the new text through keyboard-style events, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible editor with a hidden input. Changing the hidden input can appear successful in a DOM dump while server-side validation treats the visible editor as empty. Target the control that a user interacts with and that the application actually reads. If an accessibility locator returns an empty wrapper, inspect the underlying labeled editable element.

If changing a dropdown, checkbox, tab, date, or category can refresh the form, make and verify those choices **before** entering long or complex text. Re-inspect afterwards and confirm earlier entries remain present.

## 6. Verify after every meaningful edit

After each field is filled or setting is changed, read the value back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare length, required state, or a minimal redacted summary rather than exposing full content unnecessarily.

Check for these common mismatches:

- Automation reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displayed text but did not retain it internally.
- A later action erased an earlier field after a re-render.
- A hidden synchronization field was edited instead of the visible editor.
- A selection changed a dependent field, date, recipient, attachment, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once with a more appropriate interaction, then verify again. If the page continues to reject or alter the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 7. Run a pre-submit readiness gate

Before any final submission or high-impact change, inspect the full relevant page state again. Confirm all of the following:

- The correct account, organization, environment, and target item are active.
- Every required field is present and non-empty.
- Each entered value matches the intended content closely enough for the task.
- Dropdowns, checkboxes, dates, recipients, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially filled form is recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only through an appropriate access boundary. Avoid pasting sensitive field values into a large inline table when a short summary and securely available record are sufficient.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] Authorization covers the final action.
- [ ] The final action and its impact are understood.

## 8. Confirm completion after acting

A button click is not proof of success. After the final action, look for reliable evidence such as a success message, confirmation reference, newly created record, persisted setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Do not represent an attempted action as completed.

## 9. Common failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after editing a later one | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible node is not the editable node | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control that the application actually reads. |
| Automation becomes unstable on a complex page | The selected automation layer is unsuitable | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and normal browsers differ | The site varies behavior by browser context | Prefer an authorized direct interface; if necessary for an explicit task, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior | Close it through a neutral page action and re-verify affected fields. |
| A visible error may be cosmetic | The task may already have completed | Inspect the resulting state before retrying. |
| Account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## 10. Final audit checklist

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only the minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back and verified.
- [ ] Required fields and validation state passed the readiness gate.
- [ ] A pre-action record was captured when the action was consequential.
- [ ] Required authorization was obtained before the final commitment.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

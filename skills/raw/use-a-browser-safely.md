---
name: use-a-browser-safely
description: Complete browser-based tasks safely by selecting the least invasive method, protecting account context and privacy, verifying rendered state, and separating preparation from consequential final actions.
---

# Use a browser safely

Use this workflow for tasks that require interaction with a rendered website: completing forms, changing dashboard settings, collecting information from client-rendered pages, testing user flows, or working in an authenticated account. Use it only when a normal page request, supported service interface, or authorized API cannot complete the task reliably.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until the account, target, page state, and authorization are clear.

A browser automation command reporting success does **not** prove that the website accepted the change. Modern applications may retain data in an internal state model, save only after focus moves away, replace controls during a re-render, or show a misleading error after an action has already succeeded.

## 1. Choose the least invasive route

Use the first suitable route in this order:

1. **Supported direct interface or API.** Prefer a documented and authorized programmatic interface when it can safely perform the requested action.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, and forms that do not require the user's existing signed-in identity.
3. **User-visible authenticated browser session.** Use this only when an established session, single sign-on state, account-specific dashboard, or user-directed browser context is genuinely necessary.

Before automating a page, look for a direct route. Review official service documentation, ordinary form actions, page source, and visible network requests for supported endpoints. A web form may submit structured data to an authorized service that is safer and more reliable to use directly.

Do not use undocumented interfaces to bypass access controls, consent boundaries, service restrictions, or security measures. Do not use an authenticated visible browser merely because it is convenient: it can interrupt the user's work and increases privacy and account risk.

If a website blocks automated browsing, do not attempt to evade its protections for ordinary research or collection. A visible authenticated session may be appropriate only when the user explicitly requested a legitimate task on that specific site, has authorized access, and the existing session is necessary. Do not weaken browser security, access controls, warnings, or anti-abuse safeguards.

## 2. Protect account identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not place unrelated personal details in notes, screenshots, logs, or reports. Keep results within the requester's appropriate access boundary and respect privacy expectations and consent.

Before acting in an authenticated context, identify the correct account, organization, environment, and browser profile. Never infer identity from a generic browser-window name, remembered default, stale tab title, or arbitrary connection label.

Use these rules:

- Announce before taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing tab to use.
- Explicitly classify the intended context, such as personal, work, test, staging, or production.
- Select a browser profile or connection that corresponds to that context. Do not rely on a generic browser selector that may choose the most recently active profile.
- Confirm the signed-in account with a reliable account indicator before opening or modifying the actual target.
- If the account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not expose passwords, session tokens, recovery details, private account data, or security settings in output or logs.
- Do not disable multi-factor authentication, browser warnings, security controls, or access restrictions to make automation easier.

Use an account preflight gate before actions that change data. Confirm the account identity, environment, and target object. If the automation system has a verification marker or permission gate, mark the context as verified **only after** the account check has passed. Never create a verification marker in advance merely to unlock action tools.

Ask this pre-action question when needed:

> Which account is active? Which environment is active? What exact item will change?

If any answer remains uncertain, resolve it before proceeding.

## 3. Establish the task boundary

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, or workflow.
- The information that will be entered, collected, changed, or uploaded.
- The minimum information needed to complete the request.
- Whether the final action is reversible.
- Whether the work includes sending, publishing, paying, deleting, granting access, changing a plan, or another external commitment.
- Missing information, ambiguous choices, and fields requiring the user's judgment.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and preparing a preview may be reversible. Submitting, sending, publishing, purchasing, deleting, or changing important account settings may not be.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify the values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** After explicit confirmation of the prepared state, re-check account, target, and readiness. Then perform the final action once.

If the page reloads, re-renders, or the session changes between the two phases, do not assume the earlier state remains valid. Restore and verify the intended values before committing.

## 4. Inspect the rendered page before editing

Do not start by guessing selectors, filling fields by numeric position, or trusting visual appearance alone. Inspect the rendered page first and collect enough structure to identify controls safely.

For every relevant field, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, file upload, or custom widget.
- Accessible name, visible label, placeholder, or label relationship.
- Current value and whether it is required.
- Validation rules, character limits, formatting behavior, and disabled state.
- Whether an apparent field is the real editable control, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, date, tab, or other control causes a re-render.

Address controls by a stable semantic identity, such as visible label text, accessible name, or explicit label relationship. Do not use DOM indexes when labels are available: dynamic applications may change field order between page loads or after re-rendering.

Before changing an existing record or setting, inspect its current state. This reduces the risk of modifying the wrong item or overwriting information unexpectedly.

### Generic inspection pattern

Use the chosen browser automation capability to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

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

A generic “set value” operation is not reliable for every web control.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use normal text input behavior. | Line breaks may be silently removed. |
| Multiline text area | Fill text, then move focus away. | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus it, select existing content, enter text through keyboard-style events, then blur. | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, choose by visible option text, then wait for the state to settle. | Selection can trigger a full re-render. |
| Checkbox or radio control | Read its current state first and change only if necessary. | A click can toggle an already-correct value. |
| Date/time picker | Set the date and time, then verify the rendered summary. | A popover can reinterpret typing or clear related values. |
| File upload | Confirm file, destination, and privacy implications first. | Uploading may start immediately and can be difficult to undo. |

For framework-driven editors, simulate ordinary user interaction rather than writing directly to low-level page properties. A robust general sequence is:

1. Focus the actual editable element.
2. Select existing content.
3. Delete it.
4. Enter the new content with keyboard-style events.
5. Move focus to a neutral element on the page.
6. Wait briefly and read the result back.

Some forms pair a visible editor with a hidden input. Editing the hidden input may appear successful in a DOM dump while server-side validation treats the visible editor as empty. Target the interactive control that the application reads. If a generic accessibility locator identifies an empty wrapper, inspect the underlying editable element and follow its label relationship.

If changing a dropdown, checkbox, tab, or date can refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterwards and confirm that earlier entries remain present.

## 6. Verify after every meaningful edit

After each field is filled or setting is changed, read its value back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare lengths, required state, or a minimal redacted summary rather than exposing the complete value unnecessarily.

Check for common mismatches:

- The automation layer reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displayed text but did not retain it internally.
- A later interaction erased an earlier entry after a re-render.
- A hidden synchronization field was changed instead of the visible editor.
- A selection changed a dependent field, date, recipient, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once using a more suitable interaction method, and verify again. If the page continues to reject or alter the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 7. Run a pre-submit readiness gate

Before any final submission or high-impact change, inspect the full relevant page state again. Confirm all of the following:

- The correct account, organization, and environment are active.
- The target item is the intended one.
- Every required field is present and non-empty.
- Each entered value matches the intended content closely enough for the task.
- Dropdowns, checkboxes, dates, recipients, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially filled form is recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only within the appropriate access boundary. Avoid pasting a large table of sensitive values into chat when a short summary and securely available record are sufficient.

### Readiness checklist

- [ ] The account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 8. Treat one-way actions as a distinct phase

The following generally require explicit confirmation immediately before the final control is activated:

- Sending messages, invitations, or notifications.
- Publishing content.
- Submitting official or externally reviewed forms.
- Making a payment or purchase.
- Deleting records or files.
- Changing subscription, billing, access, ownership, or security settings.
- Actions labeled permanent, final, irreversible, or impossible to edit later.

Use this confirmation format:

> Ready to [final action] for [target]. Key details: [concise summary]. Audience, recipient, or destination: [value]. Cost or irreversible effect: [value or none known]. Open questions: [list or none]. Proceed?

Wait for confirmation before activating the final control. For low-risk reversible changes that the user explicitly requested, such as adjusting a preference or updating a draft, proceed after normal verification unless the page presents an unexpected warning or broader impact.

## 9. Confirm completion after acting

A button click is not proof of success. After the final action, look for reliable evidence such as a success message, confirmation reference, newly created record, persisted setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Do not represent an attempted action as completed.

## 10. General failure patterns and recovery rules

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank | The application ignored a direct value change. | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after editing a later field | A component re-render reset uncommitted state. | Commit and verify each field; complete re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used. | Find a multiline or editor control, or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node. | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited. | Use the visible interactive control that the application reads. |
| Automation is unstable on a complex page | The chosen automation layer is unsuitable. | Switch to a more robust automation method or supported direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers behave differently | The site varies by browser context. | Prefer an authorized direct interface; for an explicit legitimate task, use a verified visible session without evading protections. |
| A popup changes dates or other values unexpectedly | The widget has stateful close, clear, or parsing behavior. | Close it through a neutral page action and re-verify affected values. |
| A visible error may be cosmetic | The action may already have completed. | Inspect resulting state before retrying. |
| Account context is uncertain | The wrong profile or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## Final audit checklist

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only the minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back and verified.
- [ ] Required fields and validation state passed the readiness gate.
- [ ] A pre-action record was captured when the action was consequential.
- [ ] Explicit confirmation was obtained immediately before a consequential final action.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

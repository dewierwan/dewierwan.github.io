---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and privacy, verifying rendered state, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing rendered forms, changing settings, collecting information from dynamic pages, testing a user flow, or working in an authenticated dashboard. Use it only when a supported direct interface, API, or simple page retrieval cannot safely and reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not perform a consequential final action until account, target, page state, and authorization are clear.

A browser command reporting success does **not** prove that the website accepted a change. Modern applications can maintain internal state separately from the DOM, commit a value only after focus leaves a field, replace a control during a re-render, or show an error after an action actually succeeded.

## 1. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can complete the request. It is often more reliable than reproducing user-interface behavior.
2. **Headless browser automation.** Use this for public pages, test environments, routine dynamic-page extraction, screenshots, UI testing, and forms that do not require the user's established signed-in session.
3. **User-visible authenticated browser session.** Use this only when the task genuinely needs an existing session, single sign-on state, account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for a legitimate direct route. Check official documentation, ordinary form actions, visible network requests, and page source for supported endpoints. A form may submit structured data to an authorized service that is safer to call directly.

Do not use undocumented interfaces to bypass access controls, consent boundaries, service restrictions, or terms. Do not use an authenticated visible session merely for convenience: it can interrupt the user's work and increases privacy and account risk.

If a site blocks automated browsing, do not evade its protections for research or collection. An authorized visible browser session can be appropriate when the user explicitly asked to complete a legitimate task on that specific site and an established session is necessary. Do not weaken security controls, browser warnings, access restrictions, bot checks, or authentication requirements.

## 2. Protect account identity, privacy, and browser context

If a task accesses private communications, records, dashboards, or information about people, establish a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into screenshots, notes, logs, or reports. Keep outputs within the requester's appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated context, identify the correct account, organization, environment, and browser profile. Never infer identity from a generic browser-window name, old tab title, remembered default, or connection label.

Follow these rules:

- Announce when taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing tab.
- Classify the intended context explicitly, such as personal, work, testing, staging, or production.
- Select the browser profile or connection that matches that context; do not use a generic selector that may choose the most recently active profile.
- Confirm the signed-in account with a reliable account indicator before opening or changing the real target.
- If the required account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not reveal credentials, session tokens, recovery information, private account data, or security settings in output or logs.
- Do not disable multi-factor authentication, security checks, browser warnings, or access restrictions to make automation easier.

Use an account preflight gate before actions that change data. Confirm the account identity, environment, and target object. If the automation system has a verification marker or permission gate, record the context as verified **only after** the account check has passed. Never create a marker in advance merely to unlock actions.

A useful pre-action question is: **Which account is this? Which environment is this? What exact item will change?** Resolve uncertainty before proceeding.

## 3. Establish the task boundary and authorization

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, or workflow.
- The information that will be entered, collected, changed, or uploaded.
- The minimum information needed to complete the request.
- Whether the final action is reversible.
- Whether the task sends, publishes, pays, deletes, grants access, changes a plan, or creates another external commitment.
- Missing information or choices that require the user's judgment.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and preparing a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, or applying an irreversible account change may not be.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Re-check account, target, readiness, and authorization, then perform the final action once.

An explicit request to submit, send, publish, or otherwise commit can authorize the commitment pass. A standing authorization can also be sufficient when it clearly covers the exact action. If the user explicitly asks for review before submission, honor that request even if the task otherwise permits submission. If authorization is missing, prepare and verify the result, then ask only for the final action.

Treat payments, deletions, sends, plan or access changes, and actions labeled permanent, final, or impossible to undo as high-impact. Capture the pre-action state and obtain clear approval unless the existing instruction unambiguously authorizes that exact commitment.

## 4. Inspect the rendered page before editing

Do not begin by guessing selectors, filling controls by numeric position, or trusting visual similarity. First inspect the rendered page and collect enough structure to identify controls safely.

For each relevant field, determine:

- Element type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether the field is required.
- Validation rules, limits, formatting behavior, and disabled state.
- Whether an apparent field is the true editable control, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, date, tab, or other control causes a re-render.

Address controls by stable semantic identity: visible label text, accessible name, or explicit label relationship. Do not use DOM indexes where labels are available, because dynamic applications can change element order after hydration or re-rendering.

Before changing a record or setting, inspect its current state. This reduces the risk of modifying the wrong item or overwriting existing values.

### Generic inspection pattern

Use the chosen automation capability to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

```js
// Pseudocode: adapt to the chosen browser automation library.
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

## 5. Use the correct input method

Different controls need different interactions. A generic “set value” operation is not reliable for all of them.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use the normal text-input mechanism | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus it, select existing content, enter text through keyboard-style events, then blur | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle | A selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed | A click can toggle an already-correct value. |
| Date/time picker | Choose date and time, then verify the rendered summary | Popovers can reinterpret typing or clear related fields. |
| File upload | Confirm file, destination, and privacy implications first | Uploading may begin immediately and can be difficult to undo. |

For framework-driven editors, simulate normal user interaction rather than writing directly to page properties. A robust sequence is: focus the actual editable element, select existing text, delete it, enter new text through keyboard-style events, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible rich-text editor with a hidden input. Editing the hidden input can appear successful in a DOM dump while server validation treats the visible editor as empty. Target the control the user interacts with and the application actually reads. If an accessibility locator identifies an empty wrapper, inspect the underlying editable element and follow its label relationship.

If changing a dropdown, checkbox, date, or tab can refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterwards and confirm that prior entries remain present.

## 6. Verify every meaningful edit

After each field is filled or setting is changed, read its value back from the page. Compare the visible or accessible result with the intended value. For sensitive content, compare length, required state, or a minimal redacted summary rather than exposing the full value unnecessarily.

Check for these mismatches:

- The automation layer reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a limit.
- A custom editor displayed text but did not retain it internally.
- A later interaction erased an earlier field during a re-render.
- A hidden synchronization field changed instead of the visible editor.
- A selection changed a dependent field, date, recipient, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once using a more appropriate interaction method, then verify again. If the page still rejects or alters the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 7. Run a pre-submit readiness gate

Before a final submission or high-impact change, inspect the relevant page state again. Confirm all of the following:

- The correct account, organization, environment, and target are active.
- Every required field is present and non-empty.
- Each entered value matches the intended content closely enough for the task.
- Dropdowns, checkboxes, dates, recipients, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially prepared form is recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only through an appropriate access boundary. Avoid pasting sensitive form values into large inline tables when a short summary and securely available record are sufficient.

### Readiness checklist

- [ ] The account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood and authorized.

## 8. Confirm completion after acting

A button click is not proof of success. After the final action, look for reliable evidence such as a success message, confirmation reference, newly created record, persisted setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, the evidence available, and what remains uncertain. Do not represent an attempted action as completed.

## 9. General failure patterns and recovery rules

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after editing a later one | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control that the application reads. |
| Automation becomes unstable on a complex page | The chosen automation layer is unsuitable | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers behave differently | The site varies by browser context | Prefer an authorized direct interface; for an explicit task, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior | Close it through a neutral page action and re-verify affected fields. |
| A visible error may be cosmetic | The task may already have completed | Inspect resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
- [ ] Final-action authorization was present and any requested review occurred.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

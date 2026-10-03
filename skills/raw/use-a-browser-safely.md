---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive method, protecting account context and privacy, verifying rendered state after every meaningful edit, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for browser tasks such as completing rendered forms, changing settings, collecting information from dynamic pages, testing a user flow, or working in an authenticated dashboard. Use it when a supported direct interface, static retrieval method, or ordinary request cannot safely and reliably complete the work.

The central rule is:

> Inspect the rendered page before editing, round-trip every meaningful change by reading it back, and do not take a consequential final action until the account, target, page state, and authorization are clear.

A browser automation command returning success does **not** prove that a website accepted the change. Modern applications may hold state outside the visible DOM, commit values only when focus changes, replace controls during a re-render, or display an error even though an operation already completed.

## 1. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface. It is usually more reliable than reproducing browser behavior.
2. **Headless browser automation.** Use this for public pages, test environments, UI checks, screenshots, routine rendered-page extraction, and forms that do not require an established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely needs an existing session, account-specific dashboard, single sign-on state, or a user-directed browser context.

Before driving a browser, look for a legitimate direct route. Check official documentation, visible form actions, page source, and normal network activity for supported endpoints. A form may submit structured data to an authorized service without requiring fragile UI interaction.

Do not use undocumented routes to bypass access controls, consent boundaries, rate limits, terms, or site protections. Do not use an authenticated visible session merely for convenience: it can interrupt the user's work and creates greater privacy and account risk.

If a site blocks automated browsing, do not attempt to evade its protections for casual research or collection. A verified visible session can be appropriate only when the user explicitly asked to perform a legitimate task on that specific site, has authorized access, and that session is necessary. Do not disable browser security, multi-factor authentication, warnings, access restrictions, or anti-abuse controls.

## 2. Protect account identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, first confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into logs, screenshots, notes, or reports. Keep all outputs within the requester's appropriate access boundary and respect consent and reasonable privacy expectations.

Before acting in an authenticated context, identify the correct account, organization, environment, and browser profile. Never infer identity from a generic window name, remembered default, stale tab title, or browser connection label.

Use these rules:

- Announce when taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing tab to use.
- Classify the intended context explicitly, such as personal, work, testing, staging, or production.
- Select the profile or browser connection that matches that context instead of relying on a generic browser selector.
- Confirm the signed-in account through a reliable account indicator before opening or changing the real target.
- If the required account, environment, target, or authority is unclear, stop and ask before changing data.
- Never expose credentials, session tokens, recovery details, private account information, or security settings in output or logs.
- Never weaken security controls to make automation easier.

Use an account preflight gate before actions that change data. Confirm the account identity, environment, and target object. If the automation environment uses a verification marker or permission gate, mark it verified **only after** the account check passes. Never create a marker in advance simply to unlock actions.

Ask: **Which account is this? Which environment is this? What exact item will change?** Resolve uncertainty before proceeding.

## 3. Establish the task boundary and authorization

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, or workflow.
- The information that will be entered, collected, changed, or uploaded.
- The minimum information needed to complete the request.
- Whether the change is reversible.
- Whether the task sends, publishes, pays, deletes, grants access, changes a plan, or creates another external commitment.
- Missing information, ambiguous choices, and fields requiring user judgment.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and collecting a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, or making a permanent account change may not be.

Honor an explicit request to review before submission. When the user has already clearly authorized a specific final action, do not unnecessarily ask for the same approval again. When final authorization is missing, prepare and verify the result, show a concise pre-submit summary or appropriate preview, and ask only for authorization to take that final action.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Re-check the account, target, readiness gate, and authorization. Then perform the final action once.

If the page reloads, re-renders, session changes, or a draft expires between phases, do not assume the prior state remains valid. Restore and verify it again.

## 4. Inspect the rendered page before editing

Do not begin by guessing selectors, filling fields by numeric position, or trusting a visual approximation. First inspect the rendered page and identify relevant controls.

For each field, determine:

- Element type: single-line input, multiline area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value, required state, disabled state, and validation message.
- Character limits and formatting behavior.
- Whether the apparent field is a wrapper or hidden synchronization element rather than the real control.
- Whether changing a control causes the form to re-render or resets dependent values.

Address controls by stable semantic identity: visible label text, accessible name, or a label relationship. Do not rely on DOM indexes where labels are available. Dynamic applications can change control order between page loads or after rendering updates.

Before changing an existing record or setting, inspect its current state. This prevents modifying the wrong item or overwriting existing values unintentionally.

### Generic inspection pattern

Use the chosen automation capability to list relevant controls before writing fill logic. Record at least tag, type, role, label, required state, and current value or text length.

```js
// Pseudocode: adapt to the selected browser automation library.
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

## 5. Use the interaction method appropriate to the control

A generic “set value” operation is not reliable for every control. Use normal user-like interaction where framework-managed controls require it.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use the normal text-entry mechanism. | Line breaks may be silently removed. |
| Multiline text area | Fill text, then move focus away. | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select existing content, enter text through keyboard-style events, then blur. | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle. | Selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed. | A click can toggle an already-correct value. |
| Date/time picker | Select the date and time, then verify the rendered summary. | Popovers can clear related values or reinterpret typing. |
| File upload | Confirm file, destination, and privacy implications first. | Uploading may begin immediately and can be difficult to undo. |

For framework-driven editors, avoid direct low-level property changes. A robust general sequence is:

1. Focus the actual editable element.
2. Select existing content.
3. Delete it.
4. Enter the intended text through keyboard-style events.
5. Move focus to a neutral page element.
6. Wait briefly for state to settle.
7. Read the result back.

Some forms pair a visible editor with a hidden input. Editing the hidden input can appear successful in a DOM dump while server-side validation treats the actual editor as empty. Target the visible interactive control that the application reads. If an accessibility locator finds an empty wrapper, inspect the underlying labeled editable element.

If a dropdown, checkbox, tab, or date selection can refresh the form, make and verify those selections **before** entering lengthy or complex text. Re-inspect afterward and confirm that earlier entries remain present.

## 6. Verify after every meaningful edit

After each field is filled or setting is changed, read the value back from the page. Compare the actual visible or accessible state with the intended state. For sensitive content, compare lengths, presence, required state, or a minimal redacted summary rather than exposing full values unnecessarily.

Check for common mismatches:

- Automation reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the field is single-line or length-limited.
- A custom editor displayed text but did not retain it internally.
- A later action erased an earlier field after a re-render.
- A hidden synchronization field was edited instead of the visible editor.
- A selection changed a dependent field, recipient, date, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once with a more appropriate method, and verify again. If the page continues to reject or alter the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 7. Run a pre-submit readiness gate

Before any final submission or high-impact change, inspect the full relevant page state again. Confirm all of the following:

- The correct account, organization, and environment are active.
- The target item is the intended one.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Dropdowns, checkboxes, dates, recipients, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially filled form is recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only within the appropriate access boundary. Avoid presenting sensitive field contents in a large inline table when a short summary and securely available record are sufficient.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 8. Treat one-way actions as a separate phase

The following generally require explicit confirmation immediately before activation unless clear authorization for that exact action already exists:

- Sending messages, invitations, or notifications.
- Publishing content.
- Submitting an official or externally reviewed form.
- Making a payment or purchase.
- Deleting records or files.
- Changing subscriptions, billing, access, ownership, or security settings.
- Actions labeled permanent, final, irreversible, or impossible to edit later.

A confirmation request should concisely identify the target, significant values, recipients or audience, cost if any, irreversible effects, and any unresolved issue. Do not bury this decision in a long status message.

For low-risk reversible changes explicitly requested by the user, such as adjusting a preference or editing a draft, proceed after normal verification unless the page presents an unexpected warning or broader impact.

## 9. Confirm completion after acting

A button click is not proof of success. After the final action, look for reliable evidence such as a success notice, confirmation reference, newly created record, persisted saved setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic; blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, the evidence available, and what remains uncertain. Do not represent an attempted action as completed.

## 10. General failure patterns and recovery rules

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change. | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after editing a later one | A component re-render reset uncommitted state. | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used. | Find a multiline or editor control, or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node. | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited. | Use the visible interactive control that the application reads. |
| Automation becomes unstable on a complex page | The chosen automation layer is unsuitable. | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and visible browsers differ | The site varies behavior by browser context. | Prefer an authorized direct interface; if needed for an explicit task, use a verified visible session without evading protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior. | Close it through a neutral page action and re-verify all affected fields. |
| A visible error may be cosmetic | The task may already have completed. | Inspect resulting state before retrying. |
| The account context is uncertain | The wrong profile or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |
| A final action times out or the page disconnects | The request may or may not have reached the service. | Do not repeat immediately; inspect the destination or history for evidence of completion first. |

## 11. Maintain the workflow responsibly

When a real failure reveals a reusable lesson, record it in the local workflow documentation or test suite in a concise form: symptom, likely cause, and safe fix. Consolidate repeated lessons into general rules rather than accumulating personal incidents, account details, or site-specific secrets.

Keep scripts and logs free of credentials and private content. Pass secrets through an approved secret mechanism when necessary; never hardcode them. Prefer temporary, access-controlled artifacts for screenshots and state dumps, delete them according to the applicable retention policy, and avoid retaining sensitive pages or form contents once they are no longer needed.

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
- [ ] Explicit confirmation was obtained immediately before a consequential final action when needed.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

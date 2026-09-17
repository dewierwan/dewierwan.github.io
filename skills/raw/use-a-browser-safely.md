---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account and privacy boundaries, verifying rendered page state, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing dynamic forms, changing dashboard settings, collecting information from rendered pages, testing user flows, or working in authenticated accounts. Choose the least invasive authorized method, inspect page state before editing, read back meaningful changes, and treat consequential actions as a separate commitment step.

> A browser command that reports success does not prove the website accepted the change. Verify the page's actual state before relying on it or proceeding.

Modern web applications may maintain state outside the visible DOM, commit a value only after focus leaves a control, replace controls during a re-render, or display an error even after an action has succeeded.

## 1. Choose the least invasive authorized route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented and authorized programmatic interface when it can complete the task. It is often more reliable than reproducing browser behavior.
2. **Headless browser automation.** Use for public pages, test environments, routine dynamic-page extraction, screenshots, UI testing, and forms that do not require an existing signed-in identity.
3. **User-visible authenticated browser session.** Use only when the task genuinely requires an existing session, single sign-on, an account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for a legitimate direct route. Check official documentation, ordinary form actions, page source, and visible network activity for supported endpoints. A rendered form may submit structured data through an authorized service that is safer and more reliable to use directly.

Do not use undocumented endpoints to bypass access controls, consent boundaries, service restrictions, or security protections. Do not use an authenticated visible session merely for convenience: it can interrupt the user's work and increases privacy and account risk.

If a site blocks automated browsing, do not try to evade the block for research or collection. A verified visible session can be appropriate when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and an established session is necessary. Do not weaken browser security, authentication, warnings, or anti-abuse controls to make automation work.

## 2. Protect privacy, authorization, and account context

When a task accesses private communications, records, dashboards, or information about people, first confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into notes, screenshots, logs, or reports. Keep outputs within the requester's appropriate access boundary and respect consent and privacy expectations.

Before acting in an authenticated browser, identify the correct account, organization, environment, and browser profile. Do not infer identity from a generic browser label, remembered default, old tab title, or connection name.

Use these rules:

- Announce when taking control of a visible browser and state the task purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing tab to use.
- Classify the context explicitly, such as personal, work, testing, staging, or production.
- Select the browser profile or connection that corresponds to that context rather than using a generic selector that may choose a recent profile.
- Confirm the signed-in account with a reliable account indicator before opening or changing the real target.
- If the required account, environment, target, or authority is unclear, stop and ask before changing data.
- Do not reveal credentials, session tokens, recovery details, security settings, or unnecessary private account data in output or logs.
- Do not disable multi-factor authentication, browser warnings, security checks, or access controls.

Use an account preflight gate before any action that changes data. Answer these questions: **Which account is this? Which environment is this? What exact item will change?** If the automation environment provides a verification marker or permission gate, mark the context verified only after the account check actually passes. Never enable a gate in advance merely to unlock more powerful actions.

## 3. Establish the task boundary and authorization

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, or workflow.
- The information that will be entered, collected, changed, or uploaded.
- The minimum information needed to complete the request.
- Whether the final action is reversible.
- Whether the task sends, publishes, pays, deletes, grants access, changes a plan, or creates another external commitment.
- Missing information, ambiguous choices, and fields that require user judgment.

Separate **preparation** from **commitment**. Filling fields, drafting text, selecting options, and collecting a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, or applying an irreversible account change may not be.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify all values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Re-check the account, target, and readiness gate. If clear authorization for the exact final action already exists, proceed. If authorization is absent, ambiguous, or the user requested review before submission, show a concise prepared-state summary and ask only for the final action.

Payments, deletion, access or plan changes, and actions clearly labeled final, permanent, or impossible to undo require confirmation immediately before acting unless the user has already explicitly authorized that exact commitment. For low-risk reversible changes explicitly requested by the user, proceed after normal verification unless the page presents an unexpected warning or broader effect.

If the page reloads, re-renders, or the session changes between phases, do not assume the earlier state remains valid. Restore the intended values if needed and verify them again before committing.

## 4. Inspect the rendered page before editing

Do not start by guessing selectors, filling controls by numeric position, or trusting a visual approximation. First inspect the rendered page and collect enough structure to identify controls safely.

For each relevant field, determine:

- Element type: single-line input, multiline area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether the field is required.
- Validation rules, character limits, formatting behavior, and disabled state.
- Whether an apparent field is an editable control, a wrapper, or a hidden synchronization element.
- Whether changing a dropdown, checkbox, tab, or date causes a re-render.

Address controls by stable semantic identity, such as visible label text, accessible name, or an explicit label relationship. Do not use DOM indexes where labels are available: dynamic applications can reorder controls after loading or re-rendering.

Before changing an existing record or setting, inspect its current state. This avoids modifying the wrong item or unintentionally overwriting existing values.

### Generic inspection pattern

Use the selected automation library to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

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

## 5. Use the correct interaction for each control

A generic “set value” action is not reliable for every widget.

| Control type | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use normal text entry or fill behavior | Line breaks may be removed silently. |
| Multiline text area | Fill text, then move focus away | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus the actual editor, select existing content, enter text through keyboard-style events, then blur | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it, select by visible option text, then wait for state to settle | Selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed | Clicking may toggle an already-correct value. |
| Date/time picker | Choose date and time, then verify the rendered summary | Popovers can reinterpret typing or clear related values. |
| File upload | Confirm file, destination, and privacy implications first | Uploading may start immediately and be difficult to undo. |

For framework-driven editors, simulate ordinary user interaction rather than writing low-level page properties. A robust sequence is: focus the actual editable element, select existing text, delete it, enter the new text with keyboard-style events, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible rich-text editor with a hidden input. Editing the hidden input can appear successful in a DOM dump while server-side validation treats the actual editor as empty. Target the visible interactive control that the application reads. If an accessibility locator finds an empty wrapper, inspect the underlying labeled control and follow its label relationship.

If dropdowns, checkboxes, tabs, or dates can refresh the form, make and verify those selections **before** filling lengthy or complex text. Re-inspect afterward and confirm earlier entries remain present.

## 6. Verify after every meaningful edit

After each field is filled or setting is changed, read its value back from the page. Compare the actual visible or accessible value with the intended value. For sensitive content, compare lengths, required state, or a minimal redacted summary rather than exposing the full value unnecessarily.

Check for these common mismatches:

- Automation reports success but the field is empty in page state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated because the control is single-line or has a length limit.
- A custom editor displayed text but did not retain it internally.
- A later interaction erased an earlier field during a re-render.
- A hidden synchronization field was changed instead of the visible editor.
- A selection altered a dependent field, date, recipient, or validation requirement.

If verification fails, do not continue toward submission. Diagnose the control type, retry once using a more appropriate interaction method, and verify again. If the page continues to reject or alter the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 7. Run a pre-submit readiness gate

Before a final submission or high-impact change, inspect the full relevant page state again. Confirm all of the following:

- The correct account, organization, environment, and target item are active.
- Every required field is present and non-empty.
- Each entered value matches the intended content closely enough for the task.
- Dropdowns, checkboxes, dates, recipients, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially filled form is recoverable; an incorrect external action may not be.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only within the appropriate access boundary. Avoid placing sensitive field values in a large inline table when a short summary and a securely available record are sufficient.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] Authorization for the final action is present.
- [ ] The final action and its impact are understood.

## 8. Commit once and verify completion

A button click is not proof of success. Activate the final control only after the readiness gate and any needed confirmation pass. Avoid repeated clicks and blind retries, especially for actions that can create duplicates such as messages, submissions, payments, invitations, or records.

After the action, look for reliable evidence such as a success message, confirmation reference, newly created record, persisted setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve only relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate requests, payments, messages, or records.

If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Do not describe an attempted action as completed.

## 9. Failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after a later edit | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline or editor control, or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the underlying labeled control and target the true editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control the application actually reads. |
| A date or option changes unexpectedly after another edit | A popup, dependency, or re-render altered related state | Close transient controls through a neutral page action and re-verify all affected fields. |
| The automation layer becomes unstable on a complex page | The selected method is unsuitable | Switch to a more robust browser method or supported direct interface; do not blindly rescue a broken session. |
| Headless and ordinary browsers differ | The site changes behavior by browser context | Prefer an authorized direct interface; if needed for an explicit task, use a verified visible session without evading protections. |
| A visible error may be cosmetic | The task may already have completed | Inspect resulting state before retrying. |
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
- [ ] Authorization was confirmed for any consequential final action.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

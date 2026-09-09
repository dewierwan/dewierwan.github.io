---
name: use-a-browser-safely
description: Complete dynamic website tasks safely by using the least invasive authorized method, protecting account context and privacy, inspecting rendered controls, verifying changes, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for tasks that need real website interaction: completing rendered forms, collecting information from dynamic pages, testing a user flow, changing a setting, or working in an authenticated dashboard. Use it when a supported direct interface, static retrieval, or simple request cannot safely and reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until the account, target, authorization, and page state are verified.

An automation command returning success does **not** prove that the website accepted the change. Modern applications may store state outside the visible page structure, commit values only after focus changes, replace controls during a re-render, or display an error after an action has actually succeeded.

## 1. Choose the least invasive authorized route

Choose the first route that fits. Do not use a more intrusive browser method merely because it is convenient.

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can complete the task. It is often more reliable than reproducing browser interaction.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, and tasks that do not require an established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when an existing session, single sign-on state, account-specific dashboard, or user-directed browser context is genuinely necessary.

Before automating a page, look for a direct route. Review official documentation, normal form actions, page source, and visible network activity for supported endpoints. A rendered form may submit structured data through an approved service interface, avoiding fragile page interaction.

Do not use a direct interface to bypass access controls, consent boundaries, contractual restrictions, or anti-abuse protections. If automated access is blocked, do not attempt to evade the restriction for research or casual collection. A visible authenticated session may be appropriate only when the user explicitly requested a legitimate task on that specific site, has authorized access, and the session is needed to complete it.

## 2. Establish authorization, privacy boundaries, and account context

When a task accesses private communications, records, dashboards, or information about people, confirm a legitimate purpose and clear authorization. Access only the minimum relevant sources and information. Do not collect, retain, display, or report unrelated personal details.

Before acting in an authenticated context, identify:

- The intended account or profile.
- The organization, workspace, or tenant, when applicable.
- The environment: for example, personal, work, test, staging, or production.
- The exact page, record, setting, transaction, or audience that will be affected.

Never infer account identity from a generic browser name, remembered default, old tab title, or connection label. Confirm the signed-in identity through a reliable in-page account indicator or trusted account-management view.

### Authenticated-session rules

- Announce when taking control of a visible browser and state the purpose.
- Use a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing tab to use.
- Classify the required context before connecting, such as personal, work, test, or production.
- Select the matching browser profile or connection directly; do not rely on a generic selector that may choose the most recently used profile.
- Verify the signed-in account before opening or changing the real target.
- Stop and ask before changing data if the account, environment, target, or authority is uncertain.
- Never expose credentials, session tokens, recovery information, or unnecessary private account data in logs, screenshots, or output.
- Do not disable security controls, browser warnings, multi-factor authentication, or access restrictions to make automation easier.

If the automation environment uses a verification marker, permission gate, or similar control, mark the context verified **only after** the account check succeeds. Never create such a marker in advance merely to unlock restricted actions.

Use this pre-action question whenever private or authenticated data is involved:

> Which account is active? Which environment is this? What exact item will change, and is this requester authorized to make that change?

Resolve uncertainty before proceeding.

## 3. Define the task boundary and commitment level

Determine the intended outcome before navigating deeply. Identify:

- The target page, form, record, setting, or workflow.
- The minimum information that must be entered, collected, changed, or uploaded.
- Any private information about other people that is necessary for the task.
- Missing information, ambiguous choices, or fields requiring user judgment.
- Whether the final action is reversible.
- Whether the task sends, publishes, pays, deletes, grants access, changes a plan, or creates another external commitment.

Separate **preparation** from **commitment**. Drafting, filling fields, selecting options, and preparing a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, or applying a final account change may not be.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify the values, and capture a pre-action record. Do not activate the final control.
2. **Commitment pass:** Obtain explicit confirmation, re-check the account, target, and readiness conditions, then perform the final action once.

If the page reloads, re-renders, or the session changes between phases, do not assume the prepared state remains valid. Restore and verify it before committing.

## 4. Inspect the rendered page before editing

Do not begin by guessing selectors, using numeric positions, or trusting a visual approximation. Inspect the rendered page and identify the controls that actually accept and retain input.

For each relevant control, determine:

- Its type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date/time picker, file upload, or custom widget.
- Its stable semantic identity: accessible name, visible label, placeholder, or explicit label relationship.
- Its current value, required state, disabled state, and visible validation rules.
- Any formatting or length restrictions.
- Whether it is the actual editable control, a wrapper, or a hidden synchronization field.
- Whether changes to related controls can re-render, clear, or alter the form.

Address fields by label, accessible name, or label relationship whenever possible. Avoid DOM indexes: dynamic applications can reorder or recreate controls between page loads and after changes.

Before editing an existing record or setting, inspect its current state. This reduces the risk of modifying the wrong item or overwriting information unintentionally.

### Generic inspection pattern

Use the selected automation capability to list relevant controls before implementing fill logic. The record should include at least tag, type, role, label, required state, and a readable value or text length.

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

saveJson('page-before.json', controls);
```

## 5. Match the interaction method to the control

A generic value-setting operation is not reliable for every control. Use interactions that resemble normal user input when working with framework-managed widgets.

| Control type | Preferred interaction | Key verification concern |
|---|---|---|
| Single-line input | Use normal text entry. | Line breaks or long values may be altered. |
| Multiline text area | Enter text, then move focus away. | The value may commit only after blur. |
| Rich-text or content-editable editor | Focus the true editor, replace existing content through keyboard-style input, then blur. | Direct page mutation may not update internal application state. |
| Dropdown, checkbox, radio, or tab | Read current state, change only when needed, and wait for the page to settle. | The action can refresh dependent controls. |
| Date/time picker | Set the value and verify the rendered summary after closing the widget safely. | The widget can reinterpret input or alter related values. |
| File upload | Confirm file, destination, recipients, and privacy implications first. | Uploading may start immediately or be difficult to undo. |

For framework-driven editors, use this sequence:

1. Focus the actual editable element.
2. Select and remove existing content if replacement is intended.
3. Enter the new value through keyboard-style events.
4. Move focus to a neutral page element to commit the value.
5. Wait briefly for the page to settle.
6. Read the result back.

Some forms contain a visible editor alongside a hidden input. Editing the hidden input can appear successful in a page inspection while server-side validation still treats the visible field as empty. Target the visible interactive control that the application actually reads. If an accessibility locator finds an empty wrapper, inspect the underlying labeled editable element.

Perform and verify controls that may cause a re-render—such as dropdowns, checkboxes, tabs, and date selections—before filling long or complex text. Re-inspect the form after such changes.

## 6. Verify every meaningful edit

After each filled field or changed setting, read its state back from the page. Compare it with the intended value. For sensitive content, compare text length, required state, or a short redacted summary rather than reproducing full content in logs.

Verification should detect whether:

- The field is actually non-empty and retained its value.
- Text lost line breaks, spacing, punctuation, or special characters.
- Text was truncated by a control type or character limit.
- A custom editor displayed text but did not retain it in application state.
- A later action erased an earlier value during a re-render.
- A hidden field changed instead of the true editor.
- A selection changed a dependent recipient, date, attachment, option, or validation rule.

If verification fails, stop moving toward submission. Diagnose the control type, retry once using a more appropriate method, and verify again. If the page still rejects or changes the value, report the limitation and ask how to proceed. Do not silently submit incorrect content.

## 7. Run a readiness gate before final action

Before a final submission or high-impact change, inspect the full relevant page state again. Confirm:

- The correct account, organization, environment, and target are active.
- The intended record, recipient, audience, or setting is selected.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Dates, recipients, attachments, options, and dependent fields are correct.
- No unresolved validation errors, warnings, or unsaved-change indicators remain.
- The final control has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A recoverable draft is safer than an incorrect external action.

Capture a pre-action record for consequential tasks: a screenshot, concise state summary, or structured field dump. Keep it within the appropriate access boundary. Avoid pasting a large table of sensitive values into chat when a concise summary and securely available record are sufficient.

### Readiness checklist

- [ ] Account, environment, authorization, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Recipients, dates, attachments, options, and dependencies were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 8. Confirm one-way actions explicitly

Obtain explicit confirmation immediately before activating a control that submits, sends, publishes, pays, deletes, grants access, changes ownership, changes billing or security settings, or is labeled permanent, final, irreversible, or not editable later.

Use this confirmation format:

> Ready to **[final action]** for **[target]** using **[important values, recipients, audience, or destination]**. This will **[cost, external effect, or irreversible consequence]**. **[Open question or “No open questions.”]** Proceed?

For low-risk reversible changes explicitly requested by the user, such as updating a draft or changing a preference, proceed after ordinary verification unless the page reveals an unexpected warning or broader impact.

## 9. Verify completion, not just the click

A click is not proof of success. After acting, look for durable evidence such as a confirmation message, persisted setting, created record, sent or published item, changed status, or safe reload that retains the result.

If the site reports an error, preserve the relevant message and inspect the resulting state before retrying. Some visible errors are cosmetic, while blind retries can create duplicate submissions, messages, payments, or records.

If completion cannot be confirmed, report what was attempted, the evidence available, and what remains uncertain. Never represent an attempted action as completed.

## 10. Common failure patterns and recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank | The application ignored a direct value update or did not commit it. | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier fields disappear after a later edit | A re-render reset uncommitted page state. | Commit and verify each field; make re-rendering selections first. |
| Text loses formatting or characters | The control type or formatting behavior differs from the assumed one. | Find the true multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the actual editable node. | Inspect the underlying labeled control and target the true editor. |
| Validation says an apparently filled field is empty | A hidden synchronization field was edited instead of the interactive control. | Use the visible control the application reads and verify after blur. |
| The automation method becomes unstable | The selected tool is unsuitable for the page complexity. | Switch to a more robust authorized method; do not blindly rescue a broken session. |
| Headless and visible browsers differ | The site varies behavior by browser context. | Prefer an authorized direct interface; for an explicit legitimate task, use a verified visible session without evading protections. |
| A popup changes a date or related field | The widget has stateful parsing, clearing, or closing behavior. | Close through a neutral page action and re-check affected values. |
| An error appears after an action | The result may be incomplete, failed, or already completed. | Inspect durable page state before retrying. |
| Account context is uncertain | The wrong profile, workspace, or environment may be active. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## Final audit checklist

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only the minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back and verified.
- [ ] Required fields and validation passed the readiness gate.
- [ ] A pre-action record was captured when the action was consequential.
- [ ] Explicit confirmation was obtained immediately before a consequential final action.
- [ ] Completion was verified after the action.
- [ ] The final report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

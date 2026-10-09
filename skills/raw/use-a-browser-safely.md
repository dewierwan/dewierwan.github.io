---
name: use-a-browser-safely
description: Complete browser tasks safely by choosing the least invasive method, protecting authenticated context, verifying page state, and separating preparation from consequential action.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing rendered forms, collecting information from dynamic pages, testing a user flow, changing a dashboard setting, or working in an authenticated account. It applies when a plain page request or approved direct interface cannot reliably accomplish the task.

The central rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until the account, target, page state, and authorization are clear.

A successful browser-automation call does not prove that a site accepted a change. Modern applications may store state outside the visible DOM, commit only when focus leaves a control, replace controls during re-rendering, or display an error even after an operation completed. Treat browser actions as claims that require evidence.

## 1. Choose the least invasive route

Use the first route that safely fits the task:

1. **Supported direct interface or API.** Prefer a documented, authorized API, export, webhook, form action, or other direct interface when it can accomplish the request safely.
2. **Headless browser automation.** Use this for public pages, test environments, screenshots, ordinary rendered-page extraction, and forms that do not require an established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing session, account-specific state, single sign-on, or an interaction that cannot be performed safely through the first two routes.

Before automating a page, look for an approved programmatic route. Review official documentation, ordinary form actions, page source, and visible requests made by the page. A form may send structured data to a supported endpoint, avoiding fragile UI automation.

Do not use undocumented interfaces to bypass access controls, consent boundaries, payment controls, terms, or anti-abuse protections. Do not use a live authenticated session merely as a convenience: it can interrupt the user and increases privacy and account risk.

If a site blocks automated access, do not try to evade those protections for casual research or data collection. A verified visible session can be appropriate when the user explicitly asked to complete a legitimate action on that site, has appropriate access, and the established session is necessary. Never weaken browser security, warnings, multi-factor authentication, or anti-abuse controls to make automation easier.

### Selecting an automation implementation

Choose an implementation that matches the work:

- Use a direct browser automation library or script for long text, repeated interactions, heavy client-side applications, screenshots, and workflows requiring structured retries and state dumps.
- A lightweight browser-control service may be suitable for a short, simple task such as reading one page or making one ordinary click.
- If the lightweight layer becomes unstable, loses the page, fails on large input, or cannot represent the page correctly, restart with a more robust method. Do not keep attempting to rescue a broken session.
- Keep secrets in a secure runtime mechanism such as environment variables or an authorized credential store. Never hardcode them into a script, screenshot, report, or saved page dump.

## 2. Protect identity, privacy, and browser context

When a task accesses private communications, records, dashboards, or information about people, confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and information. Do not copy unrelated personal details into logs, screenshots, notes, or outputs. Respect consent, reasonable privacy expectations, and the requester's appropriate access boundary.

Before acting in an authenticated context, explicitly identify the correct account, organization, environment, and browser profile. Never infer identity from a generic window title, connection name, remembered default, or the order in which browser instances appeared.

Use these rules:

- Announce that you are taking control of a visible browser and state the purpose before doing so.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Classify the intended context, such as personal, work, test, staging, or production.
- Select the profile or browser connection that corresponds to that context; do not use a generic selector that may silently choose a recently used profile.
- Confirm the signed-in account using a reliable account indicator before opening or changing the real target.
- Confirm the destination environment and target record before making changes.
- If account identity, environment, target, or authority is unclear, stop and ask before modifying data.
- Do not reveal credentials, recovery data, session tokens, security settings, or unrelated account information in output.
- Do not disable security controls or ask the user to complete a security challenge merely to make automation more convenient.

Use an account preflight gate before actions that change data. Verify the account identity, environment, and target object first. If the automation environment has a verification marker, permission flag, or similar gate, mark the context verified only **after** the verification has genuinely passed. Never create such a marker in advance merely to unlock actions.

A useful pre-action question is: **Which account is active? Which environment is this? What exact item will change?** Resolve uncertainty before proceeding.

## 3. Establish the task boundary and authority

Determine the intended outcome before navigating deeply. Identify:

- The target page, record, form, setting, workflow, or transaction.
- The information to be entered, collected, changed, or uploaded.
- The minimum information necessary to fulfill the request.
- Missing details and decisions that require the user's judgment.
- Whether the final action is reversible.
- Whether the task sends, publishes, pays, deletes, grants access, changes a plan, changes security, or otherwise creates an external commitment.

Separate **preparation** from **commitment**. Filling fields, configuring a draft, selecting options, and assembling a preview are commonly reversible. Submitting, sending, publishing, purchasing, deleting, or applying a permanent account change may not be.

Honor an explicit request to review before submission. For a normal submission that the user already clearly authorized as part of the request, do not ask again solely because a final button exists. However, obtain confirmation immediately before a one-way or materially consequential action unless standing authority clearly covers that exact action and its impact. Examples include payments, final official submissions, irreversible deletion, publishing to an audience, access changes, and changes explicitly labeled permanent or impossible to undo.

For consequential work, use two phases:

1. **Preparation pass:** Fill or configure the page, verify values, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Re-check account, target, readiness, and authorization. Then activate the final control once and verify the result.

If the page reloads, the session changes, or a component re-renders between phases, do not assume the earlier state survived. Re-inspect and restore values as needed.

## 4. Inspect the rendered page before editing

Do not start by guessing selectors, filling by numeric position, or trusting visual resemblance. Inspect the rendered page first. For every relevant control, determine:

- Element type: single-line input, text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether the field is required.
- Validation rules, maximum length, formatting behavior, disabled state, and error messages.
- Whether the apparent field is the true editable element, a wrapper, or a hidden synchronization element.
- Whether changing a control triggers a re-render or resets other controls.

Address controls by stable semantic identity: visible label, accessible name, stable record identifier, or label relationship. Do not use field indexes when semantic identifiers exist. Client-side rendering can change element order between loads and after interactions.

Before changing an existing record or setting, inspect its current state. This prevents editing the wrong item and reduces accidental overwrites.

### Generic inspection pattern

Use your selected browser capability to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

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

Do not include sensitive field values in a broadly visible diagnostic dump unless they are necessary for the task and can be stored within the correct access boundary. Lengths, field names, status, and redacted summaries are often enough.

## 5. Use the correct interaction for each control

A generic “set value” command is not reliable for every control. Use the interaction a normal user would use, then verify it.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use normal text entry | Newlines may be removed silently. |
| Multiline text area | Fill text, then move focus away | The application may commit only on blur. |
| Rich-text or content-editable editor | Focus, select existing content, use keyboard-style text entry, then blur | Direct DOM mutation may not update the internal editor model. |
| Dropdown or combobox | Open and select by visible option text, then wait for state to settle | Selection may trigger a full re-render. |
| Checkbox or radio group | Read current state; change only if needed | A click can reverse an already-correct choice. |
| Date/time picker | Set the value and verify the rendered summary | Popovers can clear related values or reinterpret typing. |
| File upload | Confirm file, destination, recipient, and privacy impact first | Uploading may start immediately and be hard to reverse. |

For framework-driven rich-text editors, avoid low-level property assignment. A robust general sequence is: focus the actual editable element, select existing text, delete it, enter replacement text through keyboard-style input, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible editor with a hidden input. Editing the hidden input may look correct in a DOM inspection while server validation still treats the field as empty. Target the control the user interacts with and the application actually reads. If an accessibility locator resolves to an empty wrapper, inspect the underlying editable element and its label relationship.

Dropdowns, checkboxes, tabs, and date controls can refresh the form. Perform and verify those state-changing selections before entering long text. Re-inspect afterward and confirm earlier entries remain present.

## 6. Verify each meaningful edit

After filling a field or changing a setting, read it back from the page. Compare the actual visible or accessible state with the intended result. For sensitive text, compare length, required state, or a redacted checksum-like summary rather than exposing the full content unnecessarily.

Check for:

- An automation call reporting success while the field is empty.
- Removed line breaks, repeated spaces, punctuation, or special characters.
- Truncation from a single-line field or character limit.
- Text that displays temporarily but was not retained by the application's internal state.
- A later interaction that erased an earlier value after a re-render.
- Editing a hidden synchronization field rather than the visible control.
- A selection changing dependent dates, recipients, attachments, or validation requirements.

If verification fails, stop progressing toward submission. Diagnose the control type and retry once with a more suitable interaction. If the page still rejects or alters the content, report the limitation and ask how to proceed. Never submit content known to be incorrect or incomplete.

## 7. Run a pre-submit readiness gate

Before final submission or a high-impact change, inspect the complete relevant state again. Confirm:

- The correct account, organization, environment, and target are active.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Recipients, options, dates, attachments, permissions, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final control has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially completed form can usually be corrected; an incorrect external action may not be recoverable.

Capture a pre-action record for consequential tasks: a screenshot, concise state summary, or structured field dump. Store and share it only within the appropriate access boundary. Prefer a short summary plus a securely available record over pasting a large table of sensitive values into chat.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Each meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists when the action is consequential.
- [ ] The final action and its impact are understood and authorized.

## 8. Verify completion and handle failure safely

A click is not proof of success. After acting, look for reliable evidence: a confirmation message, reference number, newly created record, persisted setting after a safe reload, sent item, published state, or a changed status.

If the site reports an error, preserve the relevant error text and inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate messages, requests, payments, or records. If completion cannot be verified, report what was attempted, what evidence exists, and what remains uncertain. Do not represent an attempted action as completed.

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but a field is blank | The application ignored a direct value update | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier entries vanish after a later edit | Re-rendering reset uncommitted state | Commit and verify each field; make re-rendering selections first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find a multiline/editor control or use an approved simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the labeled underlying control and target the true editor. |
| Validation says a visible-looking field is empty | A hidden synchronization field was edited | Use the visible interactive control the application reads. |
| Browser automation becomes unstable | The chosen control layer is unsuitable for the page | Restart with a more robust method or supported direct interface. |
| Headless and visible contexts differ | The site varies behavior by browser context | Prefer an approved direct interface; use a verified visible session only for an explicitly authorized task. |
| A popup changes dates or other fields | The widget has stateful clear, close, or parsing behavior | Close through a neutral page action and re-verify all affected values. |
| A visible error may be cosmetic | The action may already have completed | Inspect resulting state before retrying. |
| Account context is uncertain | The wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

## 9. Final audit

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only minimum relevant private information was accessed and retained.
- [ ] The correct account, environment, and target were confirmed.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful edit was read back and verified.
- [ ] Required fields and validation passed the readiness gate.
- [ ] A pre-action record was captured when appropriate.
- [ ] Required confirmation was obtained before consequential commitment.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed outcomes from uncertainty.
- [ ] No credentials, session data, or unnecessary personal information was exposed.

When a new general failure pattern is discovered, record the symptom, likely cause, and safe fix in the workflow documentation. Consolidate related lessons rather than collecting personal incidents or site-specific workarounds. Keep the method current as browser capabilities and application behavior change.

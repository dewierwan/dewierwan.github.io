---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context, verifying rendered state, and separating preparation from consequential actions.
---

# Use a browser safely

Use this workflow for browser-based tasks such as completing forms, changing dashboard settings, collecting data from rendered pages, testing a user flow, or working in an authenticated account. Use it when a supported API, ordinary page retrieval, or another direct method cannot safely and reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not perform a consequential final action until the account, target, page state, and authorization are clear.

A browser automation command succeeding does **not** prove that a website accepted a change. Modern applications may keep state separately from the visible DOM, commit data only after focus leaves a field, replace controls during a re-render, or show an error even though an action already completed.

## 1. Confirm purpose, authority, and scope

Before accessing a private dashboard, communications, records, or information about people, confirm that the task has a legitimate purpose and that the requester has authority to direct it.

Use only the minimum relevant sources and information. Keep unrelated personal details out of screenshots, logs, notes, and final reports. Respect consent, privacy expectations, confidentiality rules, and the access boundary appropriate to the requester.

Establish the task boundary before navigating deeply:

- What exact page, record, form, setting, or workflow is the target?
- What information must be entered, collected, changed, downloaded, or uploaded?
- What is the minimum information necessary to complete the request?
- Is the action reversible?
- Does the task involve sending, publishing, paying, deleting, changing access, changing a plan, or another external commitment?
- Which choices require the user's judgment?
- Is there already authorization to perform the final action, or only to prepare it?

Do not access or disclose credentials, session tokens, recovery information, private account content, or security settings unless that access is necessary and clearly authorized. Never weaken access controls, browser security, multi-factor authentication, warnings, or anti-abuse protections to make a task easier.

## 2. Choose the least invasive method

Use the first suitable route below. Do not choose a visible signed-in browser merely for convenience.

1. **Supported direct interface or API.** Prefer a documented, authorized API or integration when it can complete the requested task reliably.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, UI testing, and forms that do not require an established signed-in identity.
3. **Authorized visible authenticated browser.** Use this only when the task genuinely requires a live account session, single sign-on state, account-specific dashboard, or a user-directed browser context.

Before driving a browser, check for a legitimate programmatic route. Look for official documentation, normal form actions, visible network requests, and page-provided configuration or data that identifies a supported endpoint. A form may submit structured data to an authorized service more reliably than a browser can reproduce its UI behavior.

Do not use undocumented interfaces to bypass access controls, consent boundaries, site restrictions, or terms that apply to the task. If a site blocks automated browsing, do not try to evade its protections for routine research or collection. A visible session can be appropriate only when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and the established session is needed.

Choose an automation implementation appropriate to the complexity of the page. A lightweight browser-control tool can work for a short interaction or simple page inspection. For lengthy text, rich editors, complex client-side applications, or repeated coordinated interactions, use a stable browser automation library or an authorized direct interface rather than trying to rescue an unstable session.

## 3. Protect browser and account context

An authenticated browser is a high-impact context. Before changing data, identify the correct account, organization, environment, and browser profile.

Never infer identity from a generic window name, remembered default, browser connection label, old tab title, or profile ordering. A generic browser selector may route to the most recently used profile rather than the correct one.

Use these operating rules:

- Announce that you are taking control of a visible browser and state the purpose.
- Work in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Classify the context explicitly, such as personal, work, test, staging, or production.
- Select a browser profile or connection that explicitly matches that context.
- Verify the signed-in identity through a reliable account indicator before opening or changing the real target.
- Confirm the target record, organization, or environment before making changes.
- If account identity, environment, authority, or target is uncertain, stop and ask before acting.
- Do not silently take over existing tabs that may contain unrelated work.

Use an account preflight gate before actions that write, send, publish, delete, purchase, or otherwise change data. A useful pre-action question is:

> Which account is this? Which environment is this? What exact item will change?

If the automation system has a verification marker or permission gate, create or enable it only after the account check actually passes. Never bypass or pre-create a gate merely to unlock acting tools.

If browser control requires a user to complete a human-verification challenge, security-key prompt, password entry, or other authentication step, ask the user to complete it. Do not automate around it or attempt to defeat it.

## 4. Separate preparation from commitment

Treat drafting and configuration differently from final external actions.

Preparation often includes filling fields, selecting options, gathering data, creating a preview, or assembling a draft. Commitment includes submitting an official form, sending a message, publishing content, making a payment, deleting data, changing access, or activating a plan.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, inspect the final state, and capture a pre-action record. Do not activate the final control.
2. **Commitment pass:** Confirm that the required authorization exists, re-check account and target context, then perform the final action once.

If an explicit request says to review before submitting, honor it. If the task already clearly authorizes a specific final action, do not repeatedly ask for permission after normal verification. If authorization is missing, prepare the result, show a concise pre-submit summary, and ask only for approval of the final action.

Actions that are commonly one-way or high impact need explicit confirmation immediately before the final control unless clear standing authorization already covers them:

- Sending messages, invitations, or notifications.
- Publishing content.
- Submitting externally reviewed or official forms.
- Making payments or purchases.
- Deleting records or files.
- Changing subscriptions, billing, ownership, access, or security settings.
- Actions labeled permanent, final, irreversible, or impossible to edit later.

For low-risk, reversible changes explicitly requested by the user, such as changing a preference or updating a draft, proceed after normal verification unless the page presents an unexpected warning or broader impact.

## 5. Inspect the rendered page before editing

Do not begin by guessing selectors, filling fields by numeric position, or trusting a visual approximation. First inspect the rendered page and identify the actual controls.

For each relevant control, determine:

- Its type: single-line input, multiline text area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Its stable semantic identity: visible label, accessible name, placeholder, or explicit label relationship.
- Its current value, required state, disabled state, and validation messages.
- Relevant formatting rules, length limits, or character behavior.
- Whether it is the real editable control, a wrapper, or a hidden synchronization element.
- Whether changing it—or another dependent control—causes the page to re-render.

Address controls by semantic identity, such as label text or an accessibility relationship. Do not rely on DOM indexes where a label is available: client-side applications can reorder controls between loads or after updates.

Before changing a record or setting, inspect its current state. This prevents modifying the wrong item or unintentionally overwriting existing content.

### Generic inspection pattern

Use the chosen browser automation library to list relevant controls before writing fill logic. Record at least tag, input type, role, label, required state, and current value or text length.

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

Store diagnostic files in a protected temporary or task workspace. Do not place sensitive form contents in shared folders, source repositories, or broad logs.

## 6. Use the correct interaction for each control

A generic “set value” action is not reliable for every type of control.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use normal text input or fill behavior | Newlines may be removed silently. |
| Multiline text area | Fill text, then move focus away | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus the real editor, select existing content, enter text with keyboard-style events, then blur | Direct DOM mutation may not update the application model. |
| Dropdown or combobox | Open it, choose by visible option text, then wait for state to settle | Selection can trigger a full re-render. |
| Checkbox or radio control | Read current state first; change only if needed | A click can toggle an already-correct value. |
| Date/time picker | Set date and time, close through a neutral page action, then inspect the rendered summary | Popovers may clear values or reinterpret later typing. |
| File upload | Confirm file, destination, recipient scope, and privacy implications first | Uploading may begin immediately and may be hard to reverse. |

For framework-driven editors, simulate normal user interaction rather than writing directly to low-level page properties. A robust pattern is:

1. Focus the actual editable element.
2. Select existing content.
3. Delete it if replacement is intended.
4. Enter the new content through keyboard-style events.
5. Move focus to a neutral page element to commit the value.
6. Wait briefly for the application state to settle.
7. Read the content back.

Some forms pair a visible editor with a hidden input. Editing the hidden field can appear successful in a DOM dump while server validation treats the visible editor as empty. Target the interactive control that the application actually reads. If an accessibility locator finds an empty wrapper, inspect the underlying labeled editable element instead.

If dropdowns, checkboxes, tabs, category selections, or date controls can re-render the form, make and verify those selections **before** filling long or complex text. Re-inspect afterward and confirm earlier values did not disappear.

## 7. Verify every meaningful edit

After each field is filled or setting changed, read it back from the rendered page and compare it with the intended result. For sensitive content, compare length, required state, a redacted summary, or a content hash rather than exposing full text unnecessarily.

Check specifically for:

- An automation call reporting success while the field remains empty.
- Removed newlines, repeated spaces, punctuation, or special characters.
- Truncation caused by a single-line control or length limit.
- Content that displays briefly but is not retained by the application's internal state.
- A later interaction erasing earlier content after a re-render.
- Editing a hidden synchronization field rather than the visible editor.
- A selection altering a dependent date, recipient, attachment, validation rule, or other field.

If verification fails, do not continue toward submission. Diagnose the control type and retry once with a more appropriate interaction. If the page still rejects or changes the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 8. Run a pre-submit readiness gate

Before any final submission or high-impact change, inspect the full relevant page state again. Confirm all of the following:

- The correct account, organization, and environment are active.
- The target record, page, or workflow is the intended one.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the task.
- Dropdowns, checkboxes, dates, recipients, attachments, and dependent fields are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially filled form is recoverable; an incorrect external action may not be.

Capture a pre-action record for consequential tasks. This can be a screenshot, a concise state summary, or a structured field dump. Keep it within the appropriate access boundary. Do not paste a large table of sensitive field values into a chat response when a short summary and protected artifact are sufficient.

### Readiness checklist

- [ ] The account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.
- [ ] Required authorization exists for the commitment phase.

## 9. Confirm completion after acting

A final button click is not proof of success. After acting, look for durable evidence such as a confirmation message, confirmation reference, newly created record, persisted setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, inspect the resulting state before retrying. A visible error can be cosmetic, while blind retries can create duplicate messages, payments, records, or submissions.

If completion cannot be verified, report what was attempted, the evidence available, and what remains uncertain. Do not represent an attempted action as completed.

## 10. Failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation reports success but the field is blank | The application ignored a direct value change | Focus the real control, use keyboard-style input, blur, and read back. |
| Earlier fields disappear after editing a later one | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | The wrong control type or formatting rule was used | Find the multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the labeled underlying control and target the real editor. |
| A field looks correct but validation says it is empty | A hidden synchronization field was edited | Use the visible interactive control that the application actually reads. |
| A dropdown or date selection wipes other content | The selection triggered a full form re-render | Set dependencies first, then refill and verify affected controls. |
| Browser automation becomes unstable on a complex page | The chosen tool is unsuitable for the page complexity | Switch to a stable automation library or authorized direct interface; do not blindly rescue the broken session. |
| Headless and visible browsers behave differently | The site changes behavior by browser context | Prefer an authorized direct interface; for an explicit task, use a verified visible session without bypassing protections. |
| A popup changes dates or fields unexpectedly | The widget has stateful close, clear, or parsing behavior | Close it through a neutral page action and re-verify all affected values. |
| An error may be cosmetic | The requested action may already have completed | Inspect resulting state before retrying. |
| The browser profile or account is uncertain | The wrong context may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |
| A human-verification or authentication prompt appears | The site requires user presence or protected authentication | Ask the user to complete it; do not bypass or automate it. |

## 11. Maintain and improve the workflow responsibly

After a meaningful failure or newly observed successful pattern, record the lesson in the workflow documentation using a concise general rule. Include both the symptom and safe recovery where possible. Consolidate redundant notes rather than collecting a long list of site-specific incidents.

Keep tool details current. If a browser library, supported interface, or verification method changes, update the relevant operating guidance rather than appending stale historical notes. Do not record private account mappings, identifiers, credentials, personal details, or organization-specific operating assumptions in reusable documentation.

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
- [ ] Required confirmation was obtained immediately before a consequential final action.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

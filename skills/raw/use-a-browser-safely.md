---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account context and private data, verifying rendered state, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for tasks requiring real website interaction: completing forms, changing settings, collecting data from rendered pages, testing a flow, or working in an authenticated dashboard. Use it when a static request, supported API, or ordinary page retrieval cannot reliably complete the task.

The central rule is:

> Inspect the rendered page before editing, verify every meaningful change by reading it back, and do not take a consequential final action until the page state, target, and authorization are clear.

A browser command that reports success does **not** prove that a website accepted the change. Modern web applications may keep internal state separate from the visible DOM, commit data only after focus changes, replace controls during a re-render, or display an error even after an action succeeded.

## 1. Establish purpose, authority, and boundaries

Before accessing a site, identify the requested outcome and its limits:

- What exact page, record, form, setting, or workflow is in scope?
- What information must be entered, collected, changed, or uploaded?
- What is the minimum information needed?
- Is the final action reversible?
- Does the task send, publish, pay, delete, grant access, change a plan, alter security, or create another external commitment?
- Which choices require the user's judgment?

When working with private communications, records, dashboards, or information about people, require a legitimate purpose and clear authorization. Access only the minimum relevant sources and information. Do not copy unrelated sensitive details into logs, screenshots, notes, or reports. Respect consent, privacy expectations, and the appropriate access boundary.

Do not reveal credentials, session cookies, authentication codes, recovery information, private account data, or security settings in output. Do not weaken access controls, multi-factor authentication, browser warnings, or anti-abuse protections to make a task easier.

## 2. Choose the least invasive route

Use the first suitable route below. Do not use a visible authenticated session merely for convenience.

1. **Supported direct interface or API.** Prefer a documented, authorized programmatic interface when it can complete the task. It is often more reliable than reproducing browser behavior.
2. **Headless browser automation.** Use this for public pages, test environments, routine rendered-page extraction, screenshots, UI testing, and forms that do not require an established signed-in identity.
3. **User-visible authenticated browser session.** Use this only when the task genuinely requires an existing account session, single sign-on state, account-specific dashboard, or a user-directed browser context.

Before driving a browser, look for a direct route. Check official documentation, ordinary form actions, visible network activity, and page source for supported endpoints. A form may submit structured data to an authorized service that can be used directly.

Do not use undocumented endpoints to bypass access restrictions, consent boundaries, site protections, or applicable terms. If a site blocks automated browsing, do not evade the block for routine research or collection. A verified visible browser may be appropriate only when the user explicitly requested a legitimate task on that specific site, has authorized access, and the established session is necessary.

## 3. Protect browser and account context

When using an authenticated browser, treat account identity and environment as a preflight requirement.

1. Announce that you are taking control of the visible browser and state the purpose.
2. Classify the intended context explicitly, such as personal, work, testing, staging, or production.
3. Select the profile or browser connection for that context directly. Do not rely on a generic browser selector, remembered default, tab title, or connection nickname.
4. Work in a fresh tab, window, or isolated tab group unless the user explicitly directs you to an existing tab.
5. Verify the signed-in account and relevant environment using a reliable account indicator before opening or changing the actual target.
6. Confirm the target record, organization, workspace, or site before making changes.

A useful pre-action question is: **Which account is this? Which environment is this? What exact item will change?** If any answer is uncertain, stop and resolve it before acting.

If the automation system has a verification marker, action gate, or permission state, set it only after the account check has genuinely passed. Never create a verification marker merely to unlock blocked controls.

## 4. Separate preparation from commitment

Separate reversible preparation from final commitment:

- **Preparation:** drafting, filling fields, selecting options, collecting evidence, and configuring a reversible setting.
- **Commitment:** submitting, sending, publishing, purchasing, deleting, changing billing or access, or activating an irreversible change.

For consequential tasks, use two phases:

1. **Preparation pass:** Fill or configure the page, verify every relevant value, and capture a pre-action screenshot or structured state record. Do not activate the final control.
2. **Commitment pass:** Re-check account, target, and readiness. Then perform the final action once authorization is present.

Honor an explicit user request to review before submission. For actions that are irreversible, costly, externally consequential, or labeled final or impossible to undo, obtain confirmation immediately before the final control unless the user has clearly and specifically authorized that exact final action. For requested reversible changes, proceed after ordinary verification unless the page shows an unexpected warning or broader impact.

If the page reloads, re-renders, or the session changes between phases, do not assume the prior state remains valid. Re-inspect and re-verify before committing.

## 5. Inspect the rendered page before editing

Do not begin by guessing selectors, using numeric field positions, or trusting a visual approximation. Inspect the rendered page first.

For each relevant control, identify:

- Element type: single-line input, multiline area, rich-text editor, dropdown, checkbox, radio group, date picker, upload, or custom widget.
- Accessible name, visible label, placeholder, or explicit label relationship.
- Current value and whether the field is required.
- Validation rules, formatting behavior, length limits, and disabled state.
- Whether the apparent field is the true editable control, a wrapper, or a hidden synchronization element.
- Whether changing it may cause the page to re-render or reset dependent fields.

Address controls by semantic identity: visible label, accessible name, stable identifier, or explicit label relationship. Do not address fields by DOM index when labels are available; dynamic applications can reorder elements between loads and after state changes.

Before changing a record or setting, inspect its existing state. This prevents changes to the wrong item and unintended overwrites.

### Generic inspection pattern

Use the selected browser capability to record tag, input type, role, label, required state, and readable value or text length before editing.

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

## 6. Use the interaction suited to the control

A generic value-setting command is not reliable for every component. Use normal user-like interaction for framework-controlled controls.

| Control type | Preferred interaction | Key verification concern |
|---|---|---|
| Single-line input | Use ordinary text entry | Newlines may be silently removed. |
| Multiline text area | Fill text, then move focus away | Some applications commit only on blur. |
| Rich-text or content-editable editor | Focus the true editable node, select existing text, enter text through keyboard-style events, then blur | Direct DOM mutation may not update the application's internal model. |
| Dropdown or combobox | Open it and select a visible option by text | A selection can trigger a full re-render. |
| Checkbox or radio group | Read state first; change only when needed | A click can toggle an already-correct selection. |
| Date/time picker | Select values, close safely, and read the rendered summary | The popover can clear or reinterpret related values. |
| File upload | Confirm file, destination, audience, and privacy implications first | Upload may begin immediately and be difficult to undo. |

For a rich-text editor, a robust general sequence is: focus the actual editable element, select existing content, delete it, enter replacement text using keyboard-style input, move focus to a neutral page element, wait briefly, and read the result back.

Some forms pair a visible editor with a hidden input. Editing the hidden input may appear correct in a DOM dump while validation treats the form as empty. Target the visible interactive control that the application actually reads. If an accessibility locator reaches an empty wrapper, inspect the underlying labeled editable element.

If dropdowns, checkboxes, tabs, or date controls can refresh the form, set and verify them **before** filling lengthy text. Re-inspect afterward and confirm earlier values still exist.

## 7. Verify every meaningful edit

After each field is filled or each setting is changed, read it back from the page. Compare the observed value with the intended value. For sensitive content, use lengths, required-state checks, or a short redacted summary rather than exposing full content unnecessarily.

Look for these mismatches:

- Automation reports success but the field is empty in rendered state.
- Newlines, repeated spaces, punctuation, or special characters were removed.
- Text was truncated by a single-line control or length limit.
- A custom editor displayed text but did not retain it internally.
- A later interaction erased an earlier value after a re-render.
- A hidden synchronization field changed instead of the true editor.
- A selection altered a dependent date, recipient, option, or validation rule.

If verification fails, do not continue toward submission. Diagnose the control type, retry once with a more appropriate interaction method, then verify again. If the site continues to reject or alter a value, report the limitation and ask how to proceed. Do not silently submit incorrect content.

## 8. Run a readiness gate before final action

Before submitting or applying a high-impact change, inspect the full relevant state again. Confirm:

- The correct account, organization, environment, and target item are active.
- Every required field is present and non-empty.
- Each entered value matches the intended content closely enough for the task.
- Recipients, options, dates, attachments, access settings, and dependent fields are correct.
- No validation error, warning, or unsaved-change indicator remains.
- The final control has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target is uncertain, **refuse to submit**. A partially filled form can usually be corrected; an incorrect external action may not be reversible.

Capture a pre-action record when useful: a screenshot, concise state summary, or structured field dump. Store and share it only within the appropriate access boundary. Do not paste a large table of sensitive values into a chat when a brief summary and securely retained record are sufficient.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful change was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Dependencies such as recipients, dates, attachments, and options were checked.
- [ ] A pre-action record exists when the action is consequential.
- [ ] The final action and its impact are understood and authorized.

## 9. Confirm completion, not just the click

A final button click is not proof of success. Look for reliable evidence such as a success message, confirmation reference, newly created record, persisted setting, sent or published item, or changed status that remains after a safe reload.

If the site reports an error, preserve the relevant error text and inspect resulting state before retrying. Some visible errors are cosmetic, while blind retries can create duplicate messages, purchases, submissions, or records.

If completion cannot be verified, report what was attempted, the evidence available, and what remains uncertain. Do not present an attempted action as complete.

## 10. Failure patterns and safe recovery

| Symptom | Likely explanation | Safe response |
|---|---|---|
| Automation succeeds but the field is blank | The application ignored a direct value change | Use focus-and-keyboard interaction, blur, then read back. |
| Earlier values disappear after a later edit | A component re-render reset uncommitted state | Commit and verify each field; perform re-rendering controls first. |
| Text loses line breaks or characters | Wrong control type or formatting rule | Find the multiline/editor control or use an explicitly acceptable simplified format. |
| A locator finds an empty wrapper | The accessible element is not the editable node | Inspect the labeled underlying control and target the true editor. |
| A value looks correct but validation says empty | A hidden synchronization field was edited | Use the visible interactive control that the application reads. |
| The automation layer becomes unstable | The chosen method is unsuitable for the page | Switch to a more robust browser method or supported interface; do not blindly rescue a broken session. |
| Headless and visible browsers differ | The site changes behavior by browser context | Prefer an authorized direct interface; for an explicitly requested task, use a verified visible session without bypassing protections. |
| A popup unexpectedly changes a date or field | The widget has stateful clear, close, or parsing behavior | Close it through a neutral page action and re-verify affected values. |
| A visible error appears after an action | The action may already have completed | Inspect durable resulting state before retrying. |
| Account context is uncertain | Wrong profile or environment may be active | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

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
- [ ] Required final authorization was present before commitment.
- [ ] Success was verified after the action.
- [ ] The report distinguishes confirmed results from uncertainty.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

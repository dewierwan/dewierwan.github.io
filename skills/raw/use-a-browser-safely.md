---
name: use-a-browser-safely
description: Complete browser-based tasks safely by selecting the least invasive authorized method, verifying account and page state, protecting private information, and separating preparation from consequential commitment.
---

# Use a browser safely

Use this workflow for tasks requiring real website interaction: completing a rendered form, collecting data from a dynamic page, testing a flow, changing a setting, uploading a file, or working in an authenticated dashboard. Use it when static retrieval, a supported export, or an authorized direct interface cannot safely complete the request.

The core rule is:

> Inspect the rendered page before editing, read back every meaningful change, and do not take a consequential final action until authorization, account, target, and page state are clear.

An automation command returning success is not proof that a site accepted a change. Modern applications may keep internal state separate from the visible page, commit a value only after focus changes, replace controls during a re-render, or display a misleading error after an action succeeded.

## 1. Choose the least invasive authorized route

Use the first suitable route below. Do not choose a more intrusive route merely because it is convenient.

1. **Supported direct interface.** Prefer a documented and authorized API, export, integration, or management feature when it can perform the requested task. It is often more reliable and auditable than reproducing a user interface.
2. **Headless browser automation.** Use an isolated, non-visible browser for public pages, test environments, routine dynamic-page extraction, screenshots, and tasks that do not need an established signed-in identity.
3. **User-visible authenticated session.** Use this only when the task genuinely requires an existing session, single sign-on state, account-specific dashboard, or a browser context explicitly identified by the user.

Before browser interaction, check for an ordinary, permitted route: official documentation, page-provided export tools, normal form actions, supported integrations, or visible network requests that represent an authorized public interface. Do not reverse-engineer or use an endpoint to bypass access controls, consent boundaries, payment gates, contractual restrictions, or security protections.

If a site blocks automated browsing, do not try to evade its protections for casual research or collection. A verified visible session can be appropriate when the user explicitly asked to complete a legitimate task on that specific site, has authorized access, and an established session is actually required. Do not weaken browser security, authentication, warnings, or anti-abuse controls.

## 2. Establish authorization, privacy, and account context

When a task involves private communications, records, dashboards, or information about people, confirm there is a legitimate purpose and clear authorization. Access only the minimum relevant sources and information. Keep results within the requester's appropriate access boundary, and omit unrelated or sensitive personal details from notes, screenshots, logs, and reports.

Before changing anything in an authenticated context, identify and verify:

- The active account or user identity.
- The organization, workspace, tenant, or project, if relevant.
- The environment, such as personal, work, test, staging, or production.
- The precise page, record, setting, recipient group, or workflow that will be affected.
- The requester's authority and the intended scope of the action.

Never infer identity from a generic browser name, remembered default, tab title, connection order, or ambiguous label. If more than one browser profile or session is available, select the one explicitly associated with the needed context. Verify the account through a reliable signed-in account indicator before opening or changing the real target.

For a visible browser session:

- Announce that browser control is being used and state the purpose.
- Start in a fresh tab, window, or isolated tab group unless the user explicitly points to an existing tab.
- Do not redirect, close, or repurpose unrelated tabs.
- Confirm profile, account, environment, and target before a data-changing action.
- Do not expose passwords, tokens, recovery information, private account details, or security settings in output.
- Do not disable multi-factor authentication, browser warnings, access restrictions, or security controls to simplify the task.

Use an account preflight gate before data-changing actions. The practical question is: **Which account is active, which environment is active, and what exact item will change?** If any answer is uncertain, stop and resolve it before proceeding. If an automation environment has a verification marker or permission gate, set it only after the account check has actually passed, never in advance to unlock an action.

## 3. Define the task boundary

Identify the intended outcome before navigating deeply or entering data. Determine:

- What page, record, form, setting, or workflow is the target.
- What information must be entered, collected, changed, or uploaded.
- What minimum information is necessary.
- Which choices are ambiguous or require user judgment.
- Whether the final action is reversible.
- Whether the task sends, publishes, pays, deletes, grants access, changes billing, changes ownership, or otherwise creates an external commitment.

Separate **preparation** from **commitment**. Drafting content, filling fields, choosing options, and collecting a preview are often reversible. Submitting, sending, publishing, purchasing, deleting, or applying a consequential account change may not be.

For consequential tasks, use two passes:

1. **Preparation pass:** configure or fill the page, verify values, and capture an appropriate pre-action record. Do not activate the final control.
2. **Commitment pass:** obtain explicit confirmation, then re-check account, target, readiness, and final action before activating it once.

If the page reloads, re-renders, expires, or changes session between passes, do not assume prior values remain correct. Re-inspect and verify the relevant state again.

## 4. Use a reliable browser implementation

Choose an automation capability that matches the task. A lightweight interactive tool may be sufficient for a brief inspection or a simple action. Use a robust, scriptable browser capability for multi-step flows, lengthy text, complex forms, repeated read-back checks, or heavily client-rendered pages.

Avoid concurrent actions against the same dynamic page unless the page and tool are known to support them. Racing interactions can create misleading state or lost entries. If the selected browser layer crashes, loses its page, mishandles complex input, or cannot read state reliably, do not blindly continue from the damaged session. Restart with a more capable browser method, or return to a supported direct interface.

For headless work, use an isolated context where practical. Pass secrets through an approved secure mechanism rather than embedding them in scripts. Keep screenshots, page dumps, and temporary artifacts in approved storage, share them only with authorized people, and remove them when no longer needed.

## 5. Inspect the rendered page before editing

Do not start by guessing selectors, filling fields by index, or relying only on a visual approximation. Inspect the rendered page first.

For every relevant control, identify:

- The control type: single-line input, multiline area, rich-text editor, dropdown, checkbox, radio group, date picker, upload control, or custom widget.
- Its accessible name, visible label, placeholder, or explicit label relationship.
- Its current value, required state, disabled state, and validation feedback.
- Important formatting rules, length limits, and dependent fields.
- Whether the apparent control is editable, a wrapper, or a hidden synchronization element.
- Whether changing it can refresh or re-render the page.

Address controls by stable semantic identity, such as visible label text, accessible name, or a label relationship. Avoid DOM indexes when a semantic identifier exists, because dynamic pages can reorder or recreate elements.

Before changing a record or setting, inspect its current state. This reduces the risk of modifying the wrong item or overwriting information outside the request.

### Generic inspection pattern

Use the chosen browser capability to record the relevant controls before filling them. The record should contain at least tag, type, role, label, required status, and a readable value or value length.

```js
// Pseudocode: adapt to the selected browser automation capability.
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

## 6. Match interaction to the control

A generic value-setting operation is not reliable for every control. Use interaction that resembles normal use when the application requires it.

| Control type | Preferred interaction | Main verification concern |
|---|---|---|
| Single-line input | Use normal text entry or fill behavior | Newlines may be removed silently. |
| Multiline text area | Fill text, then move focus away | The page may commit only on blur. |
| Rich-text or editable region | Focus the true editor, replace text using keyboard-style input, then blur | Direct DOM changes may not update application state. |
| Dropdown or combobox | Select by visible option text and wait for the page to settle | Selection can trigger a re-render. |
| Checkbox or radio control | Read current state first; change only if needed | Clicking an already-correct control can reverse it. |
| Date/time picker | Set the value and verify the displayed summary | Popovers can reinterpret input or alter related fields. |
| File upload | Confirm file, destination, and privacy implications first | Uploading may start immediately and be difficult to undo. |

For framework-driven editors, do not depend on direct property assignment. A robust pattern is: focus the actual editable element, select old content, remove it, enter new content through keyboard-style events, move focus to a neutral element, wait briefly, and read the result back.

Some applications pair a visible editor with a hidden input. Editing the hidden field can look successful while validation still treats the visible editor as empty. Target the control the user actually interacts with and that the application reads. If an accessibility locator resolves to an empty wrapper, inspect the labeled underlying editable element.

When a dropdown, date, checkbox, tab, or similar control can refresh the form, set and verify it before entering long or complex text. Re-inspect afterward to ensure earlier values remain present.

## 7. Verify every meaningful edit

After each field change, read the result back from the page. Compare it with the intended value. For sensitive content, compare a length, required state, checksum-like summary, or minimal redacted excerpt rather than reproducing the content in logs.

Stop and diagnose when any of these occur:

- Automation reports success but the field is empty.
- Text loses line breaks, repeated spaces, punctuation, or special characters.
- Text is truncated by a control type or length limit.
- A custom editor displays text but does not retain it after focus changes.
- A later action erases an earlier entry after a re-render.
- A hidden field changed instead of the visible editor.
- A choice unexpectedly changed a dependent date, recipient, validation rule, or access setting.

If verification fails, do not continue toward submission. Identify the actual control type and retry once with a more appropriate interaction. If the page still alters or rejects the value, report the limitation and ask how to proceed rather than silently submitting incorrect content.

## 8. Run a readiness gate before final action

Before final submission or a high-impact change, inspect the full relevant state again. Confirm:

- The correct account, organization, environment, and target are active.
- Every required field is present and non-empty.
- Entered values match the intended content closely enough for the request.
- Recipients, dates, options, attachments, and dependent settings are correct.
- No validation error, warning, or unsaved-change indicator remains.
- The final control has the intended effect and is not a similarly named destructive alternative.

If a required field is blank, a value cannot be verified, or the target remains uncertain, **refuse to submit**. A partial draft is recoverable; an incorrect external action may not be.

Capture a pre-action record for consequential tasks: a screenshot, concise state summary, or structured field dump. Keep it within the appropriate access boundary. Prefer a short summary over pasting sensitive field contents into a large report.

### Readiness checklist

- [ ] Account, environment, and target were verified.
- [ ] Relevant controls were inspected before editing.
- [ ] Every meaningful edit was read back.
- [ ] Required fields are non-empty and validation is clear.
- [ ] Recipients, dates, attachments, options, and dependencies were checked.
- [ ] A suitable pre-action record exists for a consequential task.
- [ ] The final action and its impact are understood.

## 9. Confirm one-way actions and completion

Obtain explicit confirmation immediately before activating a control that sends, publishes, submits, pays, purchases, deletes, grants access, changes billing or ownership, or is labeled permanent, final, irreversible, or impossible to edit later.

The confirmation request should state the target, final action, important values or scope, recipient or audience where applicable, cost or external effect, and unresolved questions. Wait for confirmation before acting. A low-risk reversible change explicitly requested by the user can proceed after ordinary verification unless the page reveals an unexpected warning or broader impact.

After acting, seek reliable evidence of completion: a success message, confirmation reference, new record, persisted setting, sent item, or changed status that survives a safe reload. A click alone is not proof.

If the site reports an error, inspect the resulting state before retrying. Errors can be cosmetic, while blind retries can create duplicate submissions, messages, purchases, or records. If completion cannot be verified, clearly distinguish what was attempted, what evidence exists, and what remains uncertain.

## Final audit

Before reporting completion, verify:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only minimum relevant private information was accessed and retained.
- [ ] Account, environment, and target were confirmed.
- [ ] Controls were inspected before editing and changes were read back.
- [ ] The readiness gate passed before consequential action.
- [ ] Explicit confirmation preceded any one-way action.
- [ ] Completion was verified rather than assumed.
- [ ] No credentials, session data, or unnecessary personal information was exposed.

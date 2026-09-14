---
name: use-a-browser-safely
description: Complete browser-based tasks safely by choosing the least invasive authorized method, protecting account and privacy context, verifying rendered page state, and separating preparation from consequential actions.
---

# Use a browser safely

Use this workflow for tasks that need real website interaction: completing forms, changing settings, collecting information from rendered pages, testing a flow, uploading material, or working in an authenticated dashboard. Use it when a simple retrieval or an authorized direct interface cannot reliably complete the requested work.

The central rule is:

> Inspect before editing, read back every meaningful change, and do not take a consequential final action until the account, target, page state, and authorization are clear.

An automation command that reports success does not prove the site accepted the change. Modern applications may maintain state separately from the visible page, commit values only when focus changes, replace controls during a re-render, or display an error after an action has already completed.

## 1. Establish purpose, authority, and scope

Before accessing the site, identify the exact outcome and boundary of the request.

Ask or determine:

- What page, record, form, setting, or workflow is in scope?
- What information must be entered, collected, changed, uploaded, or downloaded?
- Is there a legitimate purpose and clear authorization for the relevant account and information?
- What is the minimum relevant information needed?
- Which choices require the user's judgment?
- Is the final action reversible, or does it send, publish, pay, delete, grant access, change billing, alter security, or create another external commitment?

When private communications, records, or information about people are involved, use only the minimum relevant sources and details. Do not place unrelated personal information in logs, screenshots, downloads, summaries, or output. Keep results within the authorized audience and do not expose credentials, session material, recovery details, or security-sensitive account information.

If the intended target, account, environment, authority, or outcome is unclear, stop before changing data. A useful pre-action question is:

> Which account and environment am I using, what exact item will change, and what result is expected?

## 2. Choose the least invasive route

Use the first suitable route in this order:

1. **Authorized direct interface.** Prefer a supported API, export, integration, or documented programmatic operation when it can safely complete the task.
2. **Headless browser automation.** Use it for public pages, test environments, ordinary rendered-page collection, screenshots, UI testing, and tasks that do not need an existing signed-in identity.
3. **User-visible authenticated browser session.** Use it only when an existing session, single sign-on state, account-specific dashboard, or user-directed browser context is truly required.

Before browser automation, look for a direct route through official documentation, normal form actions, page source, or visible ordinary network requests. Do not use an undocumented route to bypass access controls, paywalls, consent boundaries, terms, security controls, or anti-abuse protections.

If automated browsing is blocked, do not try to evade the protection for research or routine collection. A verified visible session can be appropriate only for a legitimate task the user explicitly requested, where the user has authorized access and the established session is necessary. Do not use a live authenticated browser merely for convenience: it can interrupt the user's work and increases privacy and account risk.

## 3. Protect authenticated browser context

When a live browser session is needed, announce the takeover and purpose before interacting. For example: “I am taking over the browser to update the requested account setting.” This informs the user without adding an unnecessary approval step for ordinary navigation.

Use a fresh tab, window, or isolated tab group unless the user explicitly identifies an existing page to use. Do not take over unrelated tabs.

Classify the context before opening the real target. Common contexts include personal, organizational, test, staging, production, or another explicitly authorized environment. Then select the browser profile or connection that matches that context.

Do not infer account identity from a generic browser name, remembered default, window title, tab title, or connection nickname. Verify the signed-in account through a reliable account indicator before making changes. Also verify the organization, tenant, or environment when applicable.

If the automation setup uses a verification gate, marker, or permission state, enable it only after the account check has passed. Never create such a marker merely to unlock actions.

Additional safeguards:

- Do not disable warnings, multi-factor authentication, access controls, or browser security features.
- Do not trigger unexpected script dialogs or disruptive browser actions.
- Do not close or restart a user's browser without explicit approval, especially if it may discard their work.
- Keep authenticated screenshots, downloads, and extracted data within the authorized access boundary.
- If the correct account cannot be verified, stop and ask rather than guessing.

## 4. Separate preparation from commitment

Treat reversible setup and consequential actions as separate phases.

### Preparation pass

1. Navigate to the verified target.
2. Inspect the current state and relevant controls.
3. Select options and enter values.
4. Read back and verify every meaningful change.
5. Capture a pre-action record when the outcome is consequential.
6. Do not activate the final control.

### Commitment pass

After explicit confirmation when required:

1. Re-check account, environment, target, and final values.
2. Confirm that a reload, re-render, or session change has not altered the prepared state.
3. Perform the final action once.
4. Verify completion using reliable evidence.

Explicit confirmation immediately before commitment is normally required for sending messages, publishing, submitting official forms, purchasing, paying, deleting, changing plans, changing access or ownership, and actions described as final or not editable after submission.

For a low-risk reversible change the user directly requested, such as updating a draft or preference, proceed after normal verification unless the site presents an unexpected warning or broader effect.

A confirmation request should be concise: name the target, important values, recipients or audience, cost if any, irreversible effects, and remaining questions.

## 5. Inspect the rendered page before editing

Do not begin by guessing selectors, filling controls by numerical position, or relying only on visual appearance. Inspect the rendered page and current record first.

For each relevant control, determine:

- Its type: single-line input, multiline area, rich-text editor, dropdown, checkbox, radio group, date/time picker, upload control, or custom widget.
- Its stable identity: accessible name, visible label, placeholder, or explicit label relationship.
- Current value, required state, disabled state, validation rules, and formatting limits.
- Whether it is the real editable control, a wrapper, or a hidden synchronization field.
- Whether changing it or a related selection causes a re-render.

Address controls by semantic identity, such as label text or an accessible-name relationship. Do not use DOM position when a stable label is available; dynamic applications can reorder or replace fields after loading.

A generic inspection record should capture at least the element tag, input type, role, label, required status, and current value or text length. Save a structured before-state when it will help review, recovery, or verification. For sensitive content, record lengths or redacted summaries rather than full values.

## 6. Match the interaction to the control

A generic “set value” command is not reliable for every kind of web control.

| Control | Preferred interaction | Verification concern |
|---|---|---|
| Single-line input | Use normal text entry. | Line breaks or unsupported characters may be removed. |
| Multiline area | Enter text, then move focus away. | Some sites commit only after blur. |
| Rich-text editor | Focus the actual editable node, replace content through keyboard-style input, then blur. | Direct DOM changes may not update internal application state. |
| Dropdown or combobox | Select by visible option text and wait for the page to settle. | The selection may refresh dependent controls. |
| Checkbox or radio group | Read the existing state and change only if needed. | Clicking an already-correct control can reverse it. |
| Date/time picker | Set the value and verify the rendered summary. | Popovers can reinterpret typing or clear related values. |
| Upload control | Confirm file, destination, and privacy implications first. | Uploading may begin immediately or be difficult to undo. |

For a framework-driven editor, simulate ordinary user behavior: focus the true editable element, select existing content, delete it, enter the replacement through keyboard-style events, move focus to a neutral element, wait briefly, then read the result back.

Some pages pair a visible editor with a hidden input. Changing the hidden field may look successful in an inspection but still fail validation. Target the visible interactive control that the application actually uses. If an accessibility locator returns a wrapper rather than an editor, inspect the label relationship and locate the editable descendant.

If dropdowns, checkboxes, dates, or tabs can trigger a refresh, make and verify those selections before entering long text. Re-inspect afterwards and confirm earlier values survived.

## 7. Verify every meaningful edit

After each field fill or setting change, read the resulting state from the page and compare it with the intended value. For sensitive text, compare length, required state, a redacted digest, or a minimal summary instead of reproducing the content in output.

Stop and diagnose if:

- The automation reports success but the field is empty.
- Text lost line breaks, spaces, punctuation, or characters.
- A value was truncated by a single-line field or length limit.
- A custom editor visibly changed but did not retain its value.
- A later action erased an earlier value after a re-render.
- A hidden field changed while the actual editor remained empty.
- A selection unexpectedly changed a recipient, date, dependent field, or validation rule.

Retry once with a more appropriate interaction method, then verify again. If the page continues to reject or alter the content, report the limitation and ask how to proceed. Do not silently submit an incorrect result.

## 8. Apply a pre-action readiness gate

Before submitting or applying a high-impact change, inspect the relevant page state again. Confirm all of the following:

- The account, organization, environment, and target item are correct.
- Required fields are present and non-empty.
- Entered values match the intended content closely enough for the task.
- Recipients, attachments, dates, options, and dependent values are correct.
- No validation errors, warnings, or unsaved-change indicators remain.
- The final button has the intended effect and is not a similarly named destructive alternative.

If an important value cannot be verified, a required field is blank, or the target is uncertain, refuse to submit. A partially prepared page is usually recoverable; an incorrect external action may not be.

For consequential tasks, capture a pre-action screenshot, concise state summary, or structured field record. Share it only through the appropriate access boundary. Avoid pasting a large table of sensitive values into chat when a short summary and securely available record are sufficient.

## 9. Verify completion without creating duplicates

A click is not proof of completion. Look for persistent evidence such as a confirmation reference, a saved setting that remains after a safe refresh, a new record, a sent or published item, or an updated status.

If the site reports an error, inspect the resulting state before retrying. An error may be cosmetic, while blind retries can create duplicate messages, submissions, payments, or records. If completion cannot be verified, state what was attempted, what evidence exists, and what remains uncertain.

## 10. Recovery guide and final audit

| Symptom | Safe response |
|---|---|
| A field appears blank after a successful automation call. | Use normal focus-and-keyboard entry, blur, and read back. |
| Earlier values disappear after a later edit. | Commit and verify each value; perform re-rendering selections first. |
| Text formatting changes unexpectedly. | Find the appropriate multiline or editor control, or obtain approval for a simplified format. |
| A locator identifies a wrapper or hidden field. | Inspect labeled descendants and target the real interactive control. |
| The browser method is unstable or differs from the site’s ordinary behavior. | Prefer an authorized direct interface or an approved verified session; do not attempt to defeat protections. |
| A popup or error may have changed state unexpectedly. | Close it through a neutral action when possible, inspect resulting state, and do not retry blindly. |
| Account or environment is uncertain. | Stop, verify a reliable account indicator, and ask if uncertainty remains. |

Before reporting completion, confirm:

- [ ] The least invasive suitable route was used.
- [ ] The task had a legitimate purpose and appropriate authorization.
- [ ] Only minimum relevant private information was accessed and retained.
- [ ] Account, environment, and target were verified.
- [ ] Controls were inspected before editing.
- [ ] Meaningful changes were read back and verified.
- [ ] Required fields and validation passed the readiness gate.
- [ ] A pre-action record and explicit confirmation were used when the action was consequential.
- [ ] Completion was verified, and uncertainty is clearly distinguished from confirmed results.
- [ ] No credentials, session data, or unnecessary personal content was exposed.

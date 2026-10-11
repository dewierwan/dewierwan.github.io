---
name: turn-a-message-into-a-task
description: Turn a message thread into researched, pre-completed work, and create a clear task record only when tracking will help.
---

# Turn a message into a task

Use this workflow when one or more message links, copied conversations, or inbound requests may need follow-up. The goal is not to log a vague to-do. The goal is to complete as much useful work as is safe and authorized, then leave a small, clear human finish.

This workflow is tool-independent. Use the messaging, document, task, calendar, and research capabilities available in the user’s environment. Do not assume a particular messaging product, task database, file system, or browser.

## Operating principles

- Read the full conversation before deciding what the task is.
- Prefer a prepared deliverable over an empty task record.
- Draft external communications; do not send them without explicit authorization.
- Use the smallest relevant set of sources and the minimum personal information needed.
- Do not create records for completed, superseded, duplicated, or trivial work.
- Make uncertainty visible. Verify facts, dates, figures, and links; otherwise use clear placeholders.
- Keep access and output within the user’s legitimate purpose, authorization, and privacy boundary.
- Treat the linked message as the reason work arrived, but treat later replies as potentially decisive.

Run the full flow separately for each supplied message reference unless the references clearly concern one shared outcome.

## 1. Open the message and read the complete conversation

For every supplied message reference:

1. Open the linked message or locate the quoted message.
2. If it is a reply in a thread, open the parent and read every reply.
3. If it is a top-level message, retrieve nearby conversation context. If the message has replies, read the full thread immediately.
4. Check whether replies after the linked message change the request, answer it, reassign it, or make it obsolete.
5. Open every substantive linked attachment, form, shared document, or cited source that could contain the real request.

Identify:

- The requester and all relevant participants, using names or clear roles rather than vague references.
- The current ask, previous commitments, promises, deadlines, and dependencies.
- The current owner of each action.
- Whether work is already complete, withdrawn, delegated, or blocked.
- Whether several people have asked the same topic elsewhere and could be served by one consistent answer.

If the work appears already done, do not file dead work. Tell the user what later context suggests and ask before creating a record if status remains ambiguous.

## 2. Classify the real work

State the task shape in working notes before researching. Common shapes are:

1. **Reply owed:** Someone needs an answer, feedback, a decision, or a confirmation. Deliverable: a drafted reply.
2. **Artefact owed:** The user owes a document, introduction, analysis, reference, briefing, or data extract. Deliverable: the artefact or a substantial draft.
3. **Decision needed:** The conversation ends at a choice only the user can make. Deliverable: a concise decision brief and, where useful, a draft reply for the likely choice.
4. **Follow-up or delegation:** The user needs to chase someone, schedule something, hand off work, or update a system. Deliverable: a drafted follow-up or safely prepared internal action.

A message may contain several requests. Keep them in one task when they share an owner, deadline, and context. Split them only when different owners, timelines, or completion criteria make separate tracking genuinely clearer.

Rewrite the request as an outcome with a clear finish line. For example, replace “Message about an event question” with “Send verified attendance figures and a next-step recommendation.”

## 3. Gather targeted context

Research only what the task requires. Start with sources closest to the request, then expand only when needed.

Useful source types include:

- Earlier messages and topic searches for related commitments, decisions, or parallel requests.
- Prior correspondence, meeting notes, approved plans, and contact records for relevant relationship context.
- Project pages, event records, operational correspondence, and shared documents for project facts.
- Approved policies and established precedents for people-process, finance, or policy questions.
- Authoritative internal records or trusted public sources for quantitative questions.
- Every substantive attachment or linked document. If a document has sections, tabs, pages, appendices, or embedded requests, review all relevant parts rather than assuming the linked excerpt is complete.

For private communications or records about people, confirm there is a legitimate purpose and clear authorization. Read only the minimum relevant material. Exclude unrelated sensitive details from notes, drafts, and task records. Respect consent, confidentiality, and access rights.

Use non-interactive research methods when possible. Do not use tools that create visible browser activity or other external side effects unless the user has authorized that method.

Stop gathering when you can either complete the preparation or name the precise missing information. Two strong sources are better than many shallow searches.

## 4. Pre-complete the work safely

Do as much as is reasonable without taking irreversible external action.

- For a reply, draft the full message in the user’s requested or established voice.
- For an artefact, create the outline, analysis, reference text, or document draft.
- For a decision, prepare two or three viable options, key evidence for each, and a recommendation with reasons.
- For follow-up, draft the chase or handoff message and prepare any authorized internal update.

If a style guide or approved examples exist, read them before drafting in the user’s voice. Keep drafts concise, direct, and proportionate to the relationship and stakes. Ask one clear question when that is enough; do not turn a simple request into an unnecessary checklist. Include coaching or explanation only when coaching is itself the point of the reply.

Never invent facts, dates, amounts, names, links, or policy positions. Use explicit markers such as:

- `[VERIFY: confirm current figure in the reporting record]`
- `[FILL IN: first-hand observation or personal judgment needed]`
- `[SEARCH: locate the approved public link]`

A draft with visible, specific gaps is often more useful than a blank page. Put gaps directly where they matter in the draft, and warn the user when the draft cannot be sent as-is.

Do not send messages, email, invitations, applications, approvals, or other external communications. You may stage a draft in the user’s messaging system only when authorized. If platform formatting matters, verify that lists, paragraphs, and links will render correctly. When a task record is created, retain the complete staged draft in its notes as well.

For approvals, payments, policy exceptions, and other governed actions, route the draft through the organization’s established process rather than offering an informal approval that bypasses controls.

## 5. Ask questions only when truly blocked

Before asking the user, check whether their position is already documented in earlier messages, notes, decisions, or policies. A documented stance should usually guide the draft.

Ask questions only when a wrong assumption would cause material rework, risk, or an inappropriate commitment. Ask two to four focused questions at most. Before the questions, provide a one- or two-paragraph context recap that restores the full situation:

- who is involved and what has happened so far;
- what is now being requested;
- the real decision, trade-off, or tension;
- evidence already found; and
- the recommended default, if there is one.

Allow combined and custom answers when the interface supports them. If no material fork remains, make reasonable drafting and metadata choices, state them in the report, and let the user correct them.

## 6. Decide whether a task record is worthwhile

Skip the record when the remaining work is a short, immediate action with no waiting, deadline, or dependency—for example, reviewing a ready-to-send draft in one brief sitting. In that case, provide the context and deliverable directly.

Create a record when one or more of these apply:

- Work is deferred or cannot be completed now.
- A deadline, dependency, or wait needs tracking.
- Several steps remain or work will span days.
- The user explicitly requested a task record.

When uncertain, prefer chat-only for a simple reply and a task record for longer-lived work.

## 7. Create a complete task record

Use the user’s chosen task system and verify the record after creation. Use these fields where supported:

- **Title:** Specific, action-led, and short enough to scan.
- **Status:** The user’s equivalent of not started.
- **Due date:** Only when supported by an explicit or clearly implied deadline.
- **Priority:** Best judgment based on impact and time pressure; someone waiting generally raises urgency.
- **Estimate:** Remaining human effort, not research already completed.
- **Area or project:** The best verified category in the user’s system.
- **Notes:** A self-contained handoff using this structure:

```markdown
**What:** [One-sentence request and who is waiting.]
**Source:** [Original message or conversation link.]
**Context:**
- [Relevant history, evidence, and links.]

**Pre-completed:**
[Draft reply, artefact, decision brief, or prepared action. State where any draft is staged.]

**Remaining for the user:**
- [Specific final action.]
```

Do not paste an entire private conversation when a concise context summary will do. Open or retrieve the created record after writing it to confirm the title, notes, links, deadlines, and fields are correct.

## 8. Report back clearly

If a task record was created, report in this order:

1. What the task is.
2. What was pre-completed and where any draft is staged.
3. The chosen metadata, including priority, due date if any, and remaining estimate.
4. Any `[VERIFY]`, `[FILL IN]`, or other blockers.

If no record was created, use this format. Keep the deliverable as the final block so it can be copied without cleanup:

```markdown
## Context for the user (not part of the reply)
- [Ask, requester, key facts, judgment calls, staged-draft location, and verification flags.]

## The reply
[Draft message verbatim.]
```

Nothing should appear after the draft reply in the chat-only format.

## 9. Review staged drafts after an appropriate delay

Whenever a communication draft has been staged, schedule a follow-up review if the environment supports delayed reminders and the user has authorized this workflow. A useful initial delay is about one hour, adjusted for working hours and urgency.

The reminder must identify each staged draft and where to find it, including the conversation location and the draft text or session reference. At review time:

1. Re-read the relevant conversation.
2. Find any final message sent by the user, if accessible and authorized.
3. Compare the sent version with the staged draft: note what was removed, reworded, reordered, added, or left unanswered.
4. Extract only general, reusable lessons, such as preferred brevity, wording, decision framing, formatting, or process routing.
5. If no final message has been sent, reschedule a limited number of checks at increasing intervals, then stop. The user may have deliberately chosen not to send it.

Do not use this review to retain unnecessary private content or construct personal profiles beyond the authorized drafting purpose.

## 10. Improve the workflow carefully

After completing a run, review what helped and what caused avoidable work. Update reusable workflow guidance only when authorized to maintain it. Keep improvements small, general, and testable.

Examples of useful improvements include:

- adding a source type that reliably answered a class of requests;
- recording a generic tool limitation and its workaround;
- adding a genuinely distinct task shape;
- clarifying an instruction that caused repeated wasted effort; or
- encoding a correction as a general drafting or process rule.

Do not silently alter user-owned systems, publish changes, store sensitive conversation content merely for future drafting, or turn a single unusual incident into a rigid rule. If nothing generalizable was learned, make no change.

## Final audit

Before finishing, check:

- Did I read later replies and confirm the work is still live?
- Did I identify the actual deliverable rather than merely log the message?
- Did I research enough, but not excessively?
- Did I draft or prepare the useful work where safe?
- Did I avoid sending, approving, or committing externally?
- Are unsupported facts and links clearly marked rather than guessed?
- Does the task, if created, contain enough context and a specific remaining action?
- Did I protect private information and stay within authorized access?
- If a draft was staged, is any follow-up review authorized, bounded, and documented?

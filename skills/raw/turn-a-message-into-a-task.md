---
name: turn-a-message-into-a-task
description: Turn a conversation message into a researched, pre-completed task or a ready-to-send draft while keeping human approval for outward-facing actions.
---

# Turn a message into a task

Use this workflow when one or more messages, conversation links, or copied threads may contain a request that should be tracked or prepared. The goal is not merely to log a to-do. The goal is to complete as much useful work as safely possible, so the remaining human action is clear, small, and appropriately approved.

Process each source conversation separately unless the requests are clearly part of the same outcome.

## Operating principles

- Read the full conversation before deciding what the work is.
- Do not create a record for work that is already complete, superseded, or assigned elsewhere.
- Research only sources relevant to the request. A few well-chosen sources are better than a broad, shallow sweep.
- Draft and stage external communications when authorized, but do not send messages, emails, invitations, approvals, or other outward-facing actions without explicit human approval.
- Never invent facts, dates, links, commitments, or policy interpretations. Verify them, omit them, or mark a clear gap.
- Treat personal information carefully. Access private communications, personnel records, meeting notes, or similar sources only for a legitimate task purpose and with clear authorization. Use the minimum relevant information, omit unrelated sensitive details, and keep the output within the intended access boundary.
- Prefer one task with well-labeled sub-parts for a multi-part request. Split it only if the parts have genuinely different owners, deadlines, or tracking needs.

## 1. Read the full conversation

Open the linked message and its parent, replies, and directly relevant attachments. If a conversation link points to a reply, use the parent thread as the context source; the linked reply is still the anchor for identifying the request.

For a top-level message, also check whether it has replies. Later replies often answer, reframe, defer, reassign, or complete the original ask.

Extract the following before doing anything else:

- The people involved and their roles in the request.
- The explicit ask, implied ask, and promised next action.
- Deadlines, event dates, dependencies, and waiting states.
- Any files, documents, data, or external links that define the real work.
- Whether later conversation activity means the work is already done, no longer needed, or owned by someone else.

If names are missing or ambiguous, recover them from authorized profile information or clear message references. Do not write vague notes such as “follow up with that person.” Use a name or an unambiguous role where appropriate.

### Recency gate

Before creating a task, answer: **Did a later reply resolve, replace, or reassign this request?**

If yes, do not create a stale task. Explain what you found and ask whether tracking is still wanted if there is any uncertainty.

## 2. Identify the real task shape

State the task shape in working notes. The shape determines what “pre-completed” means.

| Task shape | What is actually owed | Useful preparation |
|---|---|---|
| Reply owed | An answer, opinion, decision, feedback, or acknowledgement | Draft the reply with supporting facts and clear next steps. |
| Artefact owed | A document, reference, introduction, analysis, data pull, or plan | Draft or assemble the artefact itself. |
| Decision needed | A choice only the task owner can make | Prepare options, evidence, trade-offs, and a recommendation. |
| Delegation or follow-up | A chase, handoff, scheduling action, or process step | Draft the follow-up or prepare the handoff details. |
| [Other task shape] | [What is owed] | [Preparation that reduces remaining work] |

Rewrite the request as an outcome, not a message label. For example, use “Review and send feedback on the project proposal” rather than “Message from project channel.”

For a multi-part ask, keep the parts together when they form one commitment, such as feedback plus a short reference. Split them only when different people must act, the dates differ materially, or completing one part does not advance the other.

## 3. Gather only the context that matters

Choose sources based on the task, not a fixed checklist. Use authorized internal systems chosen by the user, such as conversation history, document repositories, email, meeting notes, project records, applicant-tracking records, or structured data systems. Use public web research only where suitable, and prefer non-invasive retrieval methods over visible browser automation.

Common research patterns:

- **Person-related requests:** Find relevant past collaboration, documented feedback, role scope, concrete examples of work, and prior written guidance. For hiring or assessment matters, use role-relevant capabilities and diagnostic evidence only. Do not include unrelated personal details.
- **Project or event requests:** Review the recent project conversation, planning documents, event materials, and records that establish key facts such as dates, attendance, process, or decisions.
- **Data questions:** Consult the system of record, prior retrospectives, reports, and source communications. Trace important numbers to a reliable source.
- **Repeated topic requests:** Search for related asks in other authorized conversations. Where appropriate, prepare one answer that can be shared or referenced rather than duplicating effort.
- **Linked documents:** Open and read the relevant contents. If a document has multiple sections, tabs, or subdocuments, inspect all sections likely to contain decisions or asks; the message may mention only one of several required actions.
- **Policy or process questions:** Read the applicable approved policy and relevant precedent before drafting. Do not treat informal recollection as policy.

Stop research when you can either complete the preparation or name the exact blocker. Avoid collecting information merely because it exists.

## 4. Pre-complete the work

Do the reasonable preparation before filing a task.

### Drafting communications

If the task requires a reply, email, reference, or document in the owner’s voice, first use the owner’s approved writing guidance if available. If no voice guide exists, use concise, professional language and make the tone easy for the owner to adjust.

Drafts should:

- Answer the actual request rather than restating it.
- Be shorter than the supporting research unless detail is necessary.
- Ask the simplest question that will unblock progress.
- Clearly limit future commitments when they are tentative.
- Avoid decorative preambles and unnecessary lists.
- Use readable native list formatting when lists are needed.

If the user’s chosen collaboration system supports drafts, stage the proposed reply in the correct conversation context. Put the same draft in the task notes so the record remains self-contained. Never send it.

### Facts, links, and gaps

Do not guess. Handle missing information with visible markers:

- `[VERIFY: confirm the attendance figure in the reporting system]`
- `[SEARCH: locate the current policy page for expense approvals]`
- `[FILL IN: add your firsthand view of the event’s strongest lesson]`

Use a `[FILL IN]` marker when only the owner’s memory, relationship judgment, or personal experience can supply the answer. A partially complete draft with explicit gaps is usually better than a blank draft, but clearly warn that it is not ready to send as-is.

### Decision briefs

For a decision-shaped task, prepare two or three viable options. For each, state the evidence, main trade-off, and likely consequence. Then give a recommendation and explain why. The point is to reduce decision effort, not to present an unranked survey.

### Remaining work

List what cannot safely be completed as **Remaining for the owner**. Make each item specific, for example:

- Confirm whether you are willing to be named as a future reference.
- Replace the firsthand-event placeholder with your own observations.
- Review the staged draft and send it if accurate.

Do not use vague instructions such as “review and complete.”

## 5. Ask questions only when truly blocked

Before asking, search authorized written sources for an existing answer. Prior messages, planning notes, or approved guidance may already resolve the apparent choice.

Ask questions only when a wrong assumption would cost more time than asking, and the answer depends on information or judgment only the owner can provide. Ask two to four focused questions at most.

Always provide a short context recap before the questions. Include:

1. Who is involved and what has happened so far.
2. What is now being requested.
3. The decision or tension that remains.
4. The practical effect of each answer.

Allow combined or free-form answers where the question system supports them. Do not force a false single choice when the owner may reasonably choose multiple actions.

If no meaningful fork remains, make a documented best guess for task metadata or draft stance and state that assumption in the final report.

## 6. Decide whether a task record is useful

Do not create records automatically. A task record helps when work is deferred, depends on a future event or another person, has a deadline, contains multiple remaining steps, spans days, or was explicitly requested.

Skip the record when the remaining work is a single short sitting, such as reviewing a staged reply, making a small edit, and sending it. In that case, provide the briefing and deliverable directly in chat.

When uncertain, prefer chat-only for simple reply tasks and use a record for larger or waiting-dependent work.

## 7. Create the task record

Use the user’s chosen task system and its available fields. Verify the created record by reopening or rereading it after creation.

Recommended fields:

| Field | Guidance |
|---|---|
| Title | Use an imperative, specific title with a clear finish line. |
| Status | Use the system’s equivalent of “To do” unless work is already underway. |
| Due date | Add only a real or clearly implied deadline; otherwise leave blank. |
| Importance and urgency | Make a best guess from impact, deadlines, and people waiting. Mark uncertainty in the report. |
| Time estimate | Estimate remaining human effort, not total research time already spent. |
| Area or domain | Link to the best-fit project, responsibility, or goal when the system supports it. |
| Notes | Include source, context, pre-completed work, and precise remaining actions. |

Use this notes template:

```markdown
**What:** [One-sentence ask and who is waiting.]
**Source:** [Conversation or message link/reference]
**Context:**
- [Relevant role, history, or constraint]
- [Verified fact or source]
- [Deadline, dependency, or decision point]

**Pre-completed:**
[Full draft reply, artefact, decision brief, or prepared handoff. State where a draft was staged, if applicable.]

**Remaining for the owner:**
- [Specific next action]
- [Specific decision, verification, or approval needed]
```

## 8. Report back clearly

If a record was created, report in this order:

1. What the task is.
2. What was pre-completed and where any draft was staged.
3. Metadata assumptions, such as importance, urgency, due date, and remaining estimate.
4. Any `[VERIFY]`, `[SEARCH]`, or `[FILL IN]` items.

If no record was needed, sharply separate the briefing from the usable deliverable:

```markdown
## Context for the owner (not part of the reply)
- [What is being requested and who is waiting]
- [Key facts found and judgment calls made]
- [Where the draft is staged, if applicable]
- [Any VERIFY, SEARCH, or FILL IN items]

## The reply
[Draft verbatim. Keep this as the final block of the report.]
```

## 9. Run a draft quality loop

When a draft is staged and the owner has authorized this form of review, check later whether a final version was sent. Compare the sent version with the draft and capture general lessons: what was removed, shortened, clarified, reordered, or added.

Do not retain private message content beyond what is authorized and necessary. Record only reusable guidance, such as “use a direct opening,” “ask one simple question,” or “route approvals through the established process.” Stop checking after a small, predefined number of attempts; the owner may intentionally choose not to send.

## 10. Improve the workflow carefully

After each run, perform a short internal audit:

- Did a source prove essential that should be included in future research guidance?
- Did a tool or system behavior require a repeatable workaround?
- Did the task taxonomy fail to describe the request?
- Did a correction reveal a reusable drafting, process, or privacy lesson?
- Did any step add work without improving the result?

Update shared workflow guidance only when authorized and only with small, general lessons. Do not encode personal preferences, private facts, account details, or one-off incidents as universal rules.

## Final readiness check

Before finishing, confirm:

- [ ] The full relevant conversation was read, including later replies.
- [ ] The request is still active and owned by the intended person.
- [ ] Relevant private sources were accessed only with authorization and for a legitimate purpose.
- [ ] Research was sufficient but not excessive.
- [ ] Useful work was drafted or prepared rather than merely described.
- [ ] No external communication or consequential action was sent.
- [ ] Facts, dates, and links were verified or visibly marked as gaps.
- [ ] A record was created only when tracking adds value.
- [ ] Notes contain a source, context, pre-completed work, and specific remaining actions.
- [ ] The final report makes the next human step obvious.

---
name: turn-a-message-into-a-task
description: Read a message or conversation, identify the real commitment, gather only the context needed, pre-complete the work where authorized, and create a trackable task only when it adds value.
---

# Turn a message into a task

Use this workflow when a message, conversation link, email, ticket, or meeting follow-up may require action. The goal is not to copy a message into a task list. The goal is to reduce the remaining human work to a clear, safe, and appropriately small next step.

Use only sources and access rights that the user is authorized to use for this purpose. When communications or records concern other people, use the minimum relevant information, omit unrelated sensitive details, and keep the resulting task within the intended access boundary.

## Operating principles

1. **Read before acting.** The linked message may be only part of the request; later replies may resolve, change, or reassign it.
2. **Find the outcome, not just the wording.** Turn “Can you look at this?” into a concrete deliverable or decision.
3. **Research selectively.** Use a few high-value sources, not a broad sweep of every system.
4. **Pre-complete useful work.** Draft the response, prepare the evidence, or write the decision brief before logging a task.
5. **Draft, do not send.** Do not send messages, email, invitations, approvals, or other external actions without explicit authorization.
6. **Do not track dead work.** Never create a task for work already completed, cancelled, or clearly owned by someone else.
7. **Use a task record only when it helps.** A task should make deferred work easier to complete or remember, not add bureaucracy.

## 1. Open the source and read the full conversation

Start from the supplied message, conversation, or ticket. If the link points to a reply, open the parent and every reply. If it points to a top-level message, inspect nearby context and open its thread or related updates if one exists.

Record the following in working notes:

- The linked message and the parent conversation.
- Who is involved and each person’s role where relevant.
- The actual ask, any promises, and the expected deliverable.
- Deadlines, dependencies, and waiting conditions.
- Links, attachments, documents, or referenced systems.
- Later replies that answer, supersede, defer, reassign, or close the work.

If display names are missing or unclear, resolve them from authorized directory information or unambiguous mentions. Do not write vague notes such as “reply to that person” when a role or name is available and appropriate to record.

### Recency gate

Before researching or creating anything, ask:

- Has someone already answered the question?
- Has the requester withdrawn or changed the ask?
- Has ownership moved to another role?
- Has the due date passed in a way that changes the useful action?

If the work is done, do not create a task. Report the evidence briefly and ask the user only if there is genuine ambiguity about whether follow-up is still wanted.

## 2. Classify the task shape

State the task shape in your working notes. This determines what “pre-completion” means.

| Task shape | Typical outcome | Best preparation |
|---|---|---|
| Reply owed | Answer, feedback, decision, reassurance, or clarification | Draft a concise reply supported by evidence. |
| Artefact owed | Document, reference, introduction, data pull, plan, or summary | Draft or assemble the artefact, with clear gaps marked. |
| Decision needed | The user must choose between meaningful options | Write a short decision brief with a recommendation. |
| Follow-up or delegation | Chase, schedule, assign, or coordinate | Draft the follow-up or prepare the handoff details. |
| Multi-part request | Several connected deliverables | Keep one task with sub-parts unless owners or timelines differ. |

Default to one task for a connected request. Split it only when the parts have genuinely different owners, dependencies, deadlines, or completion criteria.

## 3. Gather only the context that changes the answer

Choose sources based on the task. Do not search private communications or personnel records without a legitimate work purpose and clear authorization.

Useful source choices include:

- **Person-related context:** prior relevant correspondence, meeting notes, work records, or approved assessment materials. Use only role-relevant evidence. Avoid unrelated personal history or sensitive information.
- **Project or event context:** recent channel history, project documentation, plans, decision logs, and linked files.
- **Factual or data questions:** the system of record, approved reports, event records, finance or operations documentation, and reliable public sources where suitable.
- **Policy or process questions:** current policy pages, process owners, prior approved decisions, and jurisdiction-specific requirements. Do not assume that a policy from one team, location, or legal entity automatically applies elsewhere.
- **Related asks:** search for recent same-topic requests to avoid duplicate replies and to identify one shared answer where appropriate.
- **Linked documents:** open and read the relevant parts. For multi-section documents, inspect every section or tab before concluding that the message captures the whole ask.

For external research, use approved non-invasive retrieval methods. Do not use tools that expose private browsing activity, bypass access controls, or alter external systems. Verify material facts, dates, and links from reliable sources.

Stop research when you can either complete the preparation or name the precise blocker. Two or three well-chosen sources are usually better than many shallow searches.

## 4. Pre-complete the work

Do as much as is safe and authorized before asking the user to act.

### For replies and written artefacts

If the organization or user has an approved writing guide, read and follow it before drafting. Otherwise, use a clear, concise style matching the conversation’s level of formality.

- Write the draft in the user’s likely voice only when authorized to do so.
- Keep the draft shorter than a first instinct suggests.
- Ask one clear question when one will move the work forward; do not turn a simple reply into an unnecessary questionnaire.
- Include coaching, rationale, or detailed explanation only when it is useful to the recipient.
- Route approvals through the established process rather than making informal commitments on the user’s behalf.
- Preserve meaningful uncertainty. For example: “I can support this in principle, subject to the normal review process.”

Where the chosen system supports drafts, stage the draft in the original conversation or appropriate draft location. Do not send it.

### For decisions

Prepare a brief with two or three viable options. For each option, include evidence, trade-offs, and material risks. Make a recommendation and explain why it best fits the known goals. Do not present an unstructured list of facts when a recommendation is possible.

### For missing information

Never invent a fact, number, date, contact detail, policy interpretation, or URL. Use visible placeholders:

- `[VERIFY: confirm current figure in the system of record]`
- `[FILL IN: firsthand observation needed]`
- `[SEARCH: approved source for the current policy link]`

Leave memory-dependent or judgment-dependent sections in the draft rather than deleting them. A clearly incomplete draft often still saves framing time, but it must be marked as not ready to send.

## 5. Ask questions only at a real decision fork

Before asking the user questions, check whether their stance is already documented in the conversation, prior correspondence, a decision log, or an approved planning document. A documented decision is better than re-asking the same question.

Ask questions only when a wrong assumption would materially waste time, create risk, or change the substance of the output. Ask two to four targeted questions at most.

Always provide a short context recap before the questions: who is involved, what has happened, what is being asked now, and what tension or trade-off requires a choice. Permit multiple selections or a free-text response if choices can reasonably be combined.

Use this format:

```markdown
## Context
[Who asked, what led here, what is now needed, and the key evidence.]

## Decisions needed
1. [Specific decision and options, including “other” where useful.]
2. [Specific decision and options.]

## What I will do after your answer
[How the answer changes the draft or task.]
```

If there is no real fork, make a reasonable metadata and drafting judgment, disclose it in the final report, and allow correction later.

## 6. Decide whether a task record is useful

Skip the task record when the work is complete, duplicated, cancelled, owned elsewhere, or can be finished in one short sitting without anything to wait for. For example, if a reply draft is ready for a quick review and send, deliver the draft directly rather than creating a record that will outlive the work.

Create a task record when one or more of these apply:

- The work is deferred or cannot be done now.
- A deadline, dependency, or waiting period needs tracking.
- Multiple steps remain or work is spread across days.
- The user explicitly asked for a record.
- The work needs a durable handoff or audit trail within the authorized team boundary.

When uncertain, favor chat-only delivery for simple reply tasks and a task record for substantive multi-step work.

## 7. Create a high-value task record

Use the user’s chosen task system and verify required fields against its current schema. Do not rely on hard-coded identifiers, saved personal defaults, or a particular vendor’s terminology.

| Field | Standard |
|---|---|
| Title | Imperative, specific, and outcome-based; ideally short enough to scan quickly. |
| Status | The appropriate open state, such as `To do`. |
| Owner | The responsible person or role, if the system supports ownership. |
| Due date | A real implied or explicit date; otherwise leave blank. |
| Priority | Best judgment based on impact, urgency, and people waiting. |
| Estimate | Remaining human effort, not the effort already pre-completed. |
| Area or project | The best-fitting approved category. |
| Notes | Context, source, prepared work, and exact remaining steps. |

Use this Notes template:

```markdown
**What:** [One sentence: requested outcome and who is waiting.]
**Source:** [Link or reference to the originating conversation.]

**Context:**
- [Relevant history or role information.]
- [Verified fact or dependency.]
- [Relevant linked document or decision.] 

**Pre-completed:**
[Draft reply, draft artefact, decision brief, research result, or handoff text. State where any draft is staged.]

**Remaining for the user:**
- [Specific review, decision, or action.]
- [Specific follow-up, if any.]

**Checks before sending or closing:**
- [VERIFY or FILL IN item, if applicable.]
```

Open or re-read the created record to confirm that the title, source, notes, owner, dates, and formatting saved correctly.

## 8. Report back clearly

### If a task record was created

Report in this order:

1. What the task is.
2. What was pre-completed and where any draft was staged.
3. Metadata assumptions: priority, due date, and remaining effort.
4. Any `[VERIFY]` or `[FILL IN]` items that prevent immediate sending or closure.

### If no record was created

Keep the briefing separate from the deliverable, and make the draft the final block so it can be copied cleanly.

```markdown
## Context for the user (not part of the reply)
- [Ask, requester, key facts, judgment calls, and any verification flags.]
- [State where the draft is staged, if applicable.]

## The reply
[Draft verbatim.]
```

Do not add commentary after the reply block.

## 9. Run a safe draft review loop

When a draft is staged, a later authorized review can compare the staged text with the user’s eventual sent version. This is optional and must remain within approved access and retention boundaries.

At review time:

1. Confirm whether the draft was sent, changed, or intentionally left unsent.
2. Compare the sent version with the draft.
3. Identify general lessons: concision, ordering, tone, approval routing, recurring process facts, or common missing context.
4. Update a shared, approved workflow guide only with general reusable lessons. Do not store private message content, personal preferences that are not authorized for reuse, or identifying details.
5. If no action has occurred, make a limited number of later checks only when authorized; then stop rather than repeatedly monitoring a person’s messages.

## 10. Improve the workflow carefully

After each run, review failures and friction silently or with the user, according to the operating environment. Improve the documented process when a general lesson emerges, such as a useful source type, a system quirk, a missing task category, or a recurring approval rule.

Keep improvements small, evidence-based, and broadly applicable. Do not encode a one-off incident as a permanent rule. Do not alter shared procedures, publish changes, or retain sensitive learning data without the appropriate authorization.

## Final audit checklist

Before finishing, confirm:

- [ ] I read the parent conversation and relevant later replies.
- [ ] I checked whether the work was already complete, superseded, or reassigned.
- [ ] I identified the actual outcome and task shape.
- [ ] I used only relevant, authorized sources and minimized personal data.
- [ ] I drafted or prepared as much as was safe and useful.
- [ ] I did not send, approve, schedule, or otherwise act externally without authorization.
- [ ] I marked unverified facts and memory-dependent gaps clearly.
- [ ] I asked questions only where a real decision fork remained.
- [ ] I created a task only if it provides tracking value.
- [ ] The task, if created, contains a source, context, pre-completed work, and concrete remaining steps.
- [ ] My final report makes the next human action obvious.

---
name: turn-a-message-into-a-task
description: Read a message or conversation, identify the real work, research only the context needed, and prepare the deliverable as far as authorization allows before creating a task record.
---

# Turn a message into a task

Use this workflow when one or more message links, conversation exports, emails, or collaboration-thread references may contain work that should be tracked. The goal is not merely to log a to-do. The goal is to reduce the remaining human action to the smallest safe, clear step: research the issue, prepare a draft or decision brief, and create a task only when tracking adds value.

Use only sources and tools the user is authorized to access. When a conversation includes personal, employment, financial, health, performance, or other sensitive information, access only the minimum relevant material, omit unrelated sensitive detail, and keep the output within the intended audience and access boundary.

## Operating principles

- Read the complete relevant conversation before deciding what the task is.
- Treat the linked message as the anchor, but treat later replies as potentially decisive.
- Do enough research to act confidently or to name the exact blocker. Do not perform a blanket search.
- Draft external-facing actions; do not send messages, emails, invitations, approvals, or other consequential actions without explicit authorization.
- Prefer one task for one coherent outcome. Split work only when ownership, finish conditions, or timing genuinely differ.
- Never create a task for work that is already completed, superseded, or clearly owned and tracked elsewhere.
- Never invent facts, links, dates, or commitments. Mark uncertain information clearly.

## 1. Read the whole conversation

First resolve the message reference using the user’s chosen communication system. If it points to a reply, retrieve the parent and all thread replies. If it points to a top-level message, retrieve a small time window around it and then retrieve its thread if replies exist. Some systems do not return a message when the start and end timestamps are identical; use a narrow range instead.

Capture the following:

- The requester, accountable user, and any other named participants.
- The actual request, not just the wording of the opening message.
- Promises, decisions, deadlines, dependencies, and linked material.
- Whether later replies answer the question, change the requested outcome, reassign the work, or close it.
- Whether the request contains several related parts.

Resolve identities carefully. If display names are absent, use authorized profile information or explicit mentions in the message. In the task and draft, refer to people by an appropriate name or role rather than vague phrases such as “that person.”

### Recency gate

Before doing research or creating a record, inspect replies and updates posted after the anchor message. If the work appears complete, superseded, or reassigned, do not create a stale task. Report the finding and ask the user only if the status is genuinely ambiguous.

## 2. Classify the real task

State the task shape in your working notes. The classification determines what “pre-completed” work should look like.

| Task shape | What is owed | Best pre-completion |
|---|---|---|
| Reply owed | An answer, feedback, decision, introduction, or acknowledgement | A concise reply draft, ideally staged in the original thread if supported |
| Artefact owed | A document, reference, analysis, data pull, plan, or other deliverable | The artefact or a usable first draft |
| Decision needed | A choice that only the accountable user can make | A short options brief, evidence, recommendation, and likely reply draft |
| Delegation or follow-up | A chase, handoff, scheduling step, or process action | A drafted follow-up, handoff note, or safely pre-filled action |
| Information request | A factual answer or status update | Verified answer with sources and a draft response |

A multi-part request normally remains one task if it has one owner and one practical time horizon. Put sub-parts in the notes and give each a clear finish condition. Split it only if different people own parts, deadlines differ substantially, or one part can be completed independently without helping the others.

Rewrite the task as an observable outcome. For example, use “Send a drafted response confirming the event plan” rather than “Follow up about event.”

## 3. Gather targeted context

Choose sources based on the task, not habit. Confirm that access is legitimate and proportionate before opening private records.

Typical source choices include:

- **Person-related context:** prior authorized correspondence, meeting notes, work records, role-relevant assessment evidence, and relevant project conversations.
- **Project or event context:** recent channel history, project plans, linked documents, logistics records, and post-project reviews.
- **Data questions:** the organization’s source-of-record database, prior reports, planning documents, and operational correspondence that can verify numbers or dates.
- **Parallel requests:** a topic-based search across authorized conversations to identify duplicate questions or a prior answer that can be reused.
- **Linked content:** open and read relevant links. For multi-section documents, inspect the document structure first and read every relevant section; the message may mention only one of several decisions required.
- **Policy or process questions:** the current policy source, documented precedent, and the responsible process owner’s guidance. Use analogous policies as an input, not proof that the same rule applies everywhere.

For hiring, references, feedback, or assessments, use role-relevant capabilities, observed work, documented evidence, and role alignment. Do not include unrelated personal information or unsupported judgments.

Use public web research only when it is appropriate and authorized. Prefer non-invasive retrieval methods and avoid tools that create visible activity or modify external systems unless the user has explicitly approved that behavior.

### Research stop rule

Stop when you can do the requested work safely, prepare a meaningful draft, or state precisely what prevents progress. Two or three strong sources are usually better than many shallow searches.

## 4. Pre-complete the work

Do as much as can be done without making irreversible or externally visible commitments.

### Drafts and artefacts

- For a reply, prepare the full reply, not merely bullet points.
- For a reference, plan, analysis, or other artefact, produce a usable draft with evidence where possible.
- For a decision, provide two or three viable options, evidence for each, a recommendation, and the reason for it.
- For follow-up work, draft the chase or handoff message and identify who should receive it.

If the user has provided a writing guide, approved examples, or a documented voice standard, read and follow it before writing in their voice. Otherwise, use concise, plain language. Avoid unnecessary framing, ceremonial lead-ins, and overlong coaching. Ask simple questions when one simple question will resolve the issue. State future commitments cautiously when they are not guaranteed.

If the communication system supports private drafts, stage the reply in the original thread rather than sending it. Ensure lists render correctly in that system: where needed, leave a blank line before a list and test the platform’s native list formatting. Store the identical draft in the task notes so the record remains self-contained.

### Accuracy and gaps

Do not guess facts, dates, quantities, policy positions, or URLs. Use explicit markers such as:

- `[VERIFY: confirm current figure in source-of-record]`
- `[SEARCH: locate the current public policy page]`
- `[FILL IN: firsthand detail about what happened at the event]`

Use `[FILL IN]` when only the user’s memory, relationship judgment, or in-room experience can supply the material. A draft with obvious, specific blanks is often more useful than a blank page, but clearly warn that it cannot be sent as-is.

End the preparation with a concise **Remaining for user** list. Each item must be specific, such as “Confirm whether you are willing to be named as a future reference,” not “Review and complete.”

## 5. Ask questions only for real forks

Before asking questions, check whether the answer already exists in the thread, a prior message, an approved planning document, or another authorized source. A documented position should normally guide the draft more reliably than a new question.

Ask only if a wrong assumption would cost more time or create more risk than interrupting the user. When blocked, provide one or two short paragraphs of context first: who is involved, what has happened, what is now being requested, and the relevant trade-offs. Then ask two to four targeted questions. Allow multiple selections or a custom answer when the user may reasonably combine options.

If no material fork remains, make a reasonable metadata and drafting judgment, disclose it in the final report, and let the user correct it later.

## 6. Decide whether a task record is needed

Do not create a record merely because a message was supplied.

Skip the record when the work is complete, stale, duplicated, trivial, or consists only of reviewing and sending a staged short draft in a single brief sitting. Deliver the context and draft directly instead.

Create a record when one or more conditions apply:

- Work must be deferred or cannot responsibly be completed now.
- A deadline, waiting period, dependency, or follow-up needs tracking.
- Multiple steps remain or the steps span several days.
- The user explicitly requested a record.

When uncertain, prefer chat-only delivery for a simple reply and a task record for substantive artefacts, decisions, or multi-step work.

## 7. Create a useful task record

Use the user’s chosen task system and its current schema. Confirm available values such as status, priority, domains, projects, or owners rather than relying on stale IDs or names.

Set:

- **Title:** imperative, specific, and short enough to scan.
- **Status:** the appropriate open state.
- **Due date:** only when a deadline is explicit or strongly implied.
- **Importance and urgency:** best judgment based on consequences, deadline, and people waiting.
- **Time estimate:** remaining human work only, not research already completed.
- **Project/domain:** the best supported classification.
- **Notes:** source, context, prepared work, and remaining action.

Use this notes template:

```markdown
**What:** [One-line statement of the ask and who is waiting.]
**Source:** [Conversation link or reference]
**Context:**
- [Relevant background and verified fact.]
- [Relevant deadline, dependency, or decision.]

**Pre-completed:**
[Full draft reply, artefact, decision brief, or staged-action details.]

**Remaining for user:**
- [Specific final action.]
```

After creating the record, open or retrieve it to verify that the title, notes, links, dates, and status were saved correctly. Do not expose internal record links outside the audience authorized for that system.

## 8. Report back

If a record was created, report in this order:

1. What the task is.
2. What was pre-completed, including where any draft was staged.
3. Metadata judgments: priority, urgency, due date if any, and estimated remaining time.
4. Any `[VERIFY]`, `[SEARCH]`, or `[FILL IN]` flags.

If no record was needed, use this format. Keep the draft as the final block so it can be copied without cleanup.

```markdown
## Context for user (not part of the reply)
- [What the ask is and who is waiting.]
- [Key verified facts and judgment calls.]
- [Whether a draft was staged and any verification flags.]

## The reply
[Draft verbatim]
```

## 9. Learn from approved drafts

When a draft is staged, a later comparison between the staged version and the user’s eventual sent version can improve future drafting. Run this review only with legitimate access and authorization. Re-read the thread, compare changes, and record only general lessons: preferred brevity, recurring process routing, voice conventions, or formatting behavior. Do not retain unnecessary private details.

If the message has not been sent, check at most a small number of times at widening intervals, then stop. Non-sending may be intentional. Do not modify workflow documentation, persistent memory, or shared systems automatically unless the user has authorized that maintenance. When authorized, make small, general edits and maintain an auditable change log.

## Final audit

Before finishing, verify:

- The full thread and later replies were checked.
- The task is not already done, superseded, or duplicated.
- Research was relevant, authorized, and minimal.
- No external action was sent without approval.
- Facts and links are verified or clearly marked as gaps.
- The record, if created, contains a real pre-completed deliverable.
- Remaining work is concrete and appropriately small.
- Sensitive details are limited to what the intended audience needs.

---
name: turn-a-message-into-a-task
description: Read a message or conversation, identify the real remaining action, research only the context needed, and pre-complete as much work as is safe before deciding whether a task record is useful.
---

# Turn a message into a task

Use this workflow when one or more message links, emails, chat threads, or conversation records may contain work that should be tracked. The goal is not to copy a message into a task list. The goal is to understand the real request, complete the safe preparatory work, and leave the user with a small, clear remaining action.

This workflow applies only when there is a legitimate purpose and clear authorization to access the conversation and any supporting records. Use the minimum relevant sources and facts. Do not include unrelated private information, sensitive personal details, or material outside the intended audience's access boundary.

## Operating principles

- Read the full relevant conversation before interpreting the request.
- Treat a linked reply as an anchor, not necessarily the complete task.
- Check for newer replies that may resolve, supersede, reassign, or cancel the work.
- Research selectively. A few primary sources read carefully are better than many shallow searches.
- Draft rather than send. Do not send messages, emails, invitations, approvals, or other external actions without explicit authorization.
- Prefer a self-contained deliverable over a bare reminder.
- Ask the user only when a missing decision would materially change the work.
- Do not create a task merely because a message was supplied.

## 1. Read and normalize the conversation

Open the referenced message and, where permitted, its parent message and all thread replies. If the system represents replies separately, retrieve the parent and the entire thread rather than relying on a narrow time window or a single result.

Capture the following in working notes:

- Who is involved, including the requester, intended owner, and anyone waiting.
- The exact ask, promises made, decisions already recorded, and implied deliverables.
- Dates, deadlines, waiting conditions, linked documents, and named processes.
- Whether the linked message is part of a broader thread.
- Whether a later message shows that the work is already complete, no longer needed, or now owned by someone else.

Resolve identities from authorized directory information or unambiguous mentions when the message display name is absent. Do not refer vaguely to “the person” in a task if a role or permitted name is available. If identity is genuinely unclear, use a neutral role description such as “project requester” and flag the ambiguity.

### Recency gate

Before creating anything, compare the linked message with later replies. If the request appears completed, closed, withdrawn, or reassigned, do not create a task record. Report the evidence and ask whether the user still wants follow-up only if there is a plausible remaining need.

## 2. Define the actual task

State the task shape explicitly in your working notes. This determines what useful pre-completion looks like.

| Task shape | Usual remaining deliverable |
|---|---|
| Reply owed | A concise draft reply that answers the request or moves it forward. |
| Artefact owed | A draft document, reference, introduction, data extract, plan, or other requested item. |
| Decision needed | A short decision brief with options, evidence, recommendation, and a draft response for the likely decision. |
| Delegation or follow-up | A drafted chase, handoff, scheduling request, or prepared action in the user-selected system. |
| Multi-part request | One coordinated task with clearly separated sub-parts, unless owners or timelines genuinely differ. |

Rewrite the task as an outcome, not as a message label. For example, prefer “Review and send the project update” over “Message from project channel.”

Default to one task for a multi-part request when one person owns it and the parts share a timeline. Split it only when separate ownership, deadlines, or waiting states would make a combined record confusing.

## 3. Gather only the needed context

Choose sources based on the question. Do not run a blanket search across every connected system.

Typical source choices include:

- **People or working relationships:** authorized prior correspondence, meeting notes, work records, role-relevant feedback, and prior plans or talking points written by the user.
- **Projects or events:** recent project conversation, project documentation, planning notes, and materials linked from the thread.
- **Data questions:** the system of record, approved reports, retrospectives, event documentation, and source correspondence that contains hard facts.
- **Repeated asks:** a broader topic search may reveal parallel questions or an already-prepared answer. Reuse a verified answer where appropriate rather than creating duplicate work.
- **Linked files:** open and read relevant linked material. For multi-section documents, inspect all tabs, sections, or pages before assuming the message captures every requested decision.
- **Policy or process questions:** consult the organization’s authoritative policy and the applicable jurisdiction, team, or program guidance. Do not assume precedent transfers without checking whether the context differs.

For public factual research, use tools that retrieve content without taking visible actions or altering accounts. Do not use browser automation, log in to new services, or access personal records unless authorization explicitly covers that activity.

Stop research when you can either complete the preparation or precisely name the blocker. Mark uncertain facts rather than inventing them. Never guess a URL, date, amount, policy rule, or attribution. Verify it, omit it, or add a clear marker such as `[VERIFY: confirm current deadline]` or `[SEARCH: official policy page]`.

## 4. Pre-complete the work

Do as much of the task as is reasonable and safe. A useful record contains the actual draft, brief, calculation, outline, or prepared next action, not just a reminder that work exists.

### Writing in the user’s voice

If drafting text that will appear to come from the user, first consult any user-provided writing preferences, examples, or style guide that you are authorized to use. If none exists, use plain, concise, respectful language and avoid making claims about personal views that the user has not supported.

Keep drafts shorter than an internal analysis. Remove unnecessary setup, repeated praise, and elaborate checklists unless coaching or detailed explanation is the purpose of the response. Ask the simplest question that would unlock progress. Make future commitments conditional when they are not guaranteed.

Use the formatting conventions of the destination system. For example, leave an empty line before a list if the system needs it to render as a true list. Do not add stylistic lead-ins that make a short reply longer without adding meaning.

### Drafting rules

- Draft; do not send.
- If supported and authorized, stage a reply as a draft in the original thread or selected communication system.
- Put the same draft in the task notes so the record remains useful even if the staged draft is unavailable.
- Preserve clear placeholders for facts or judgment only the user can provide: `[FILL IN: your firsthand observation]`.
- Warn clearly if a draft cannot be sent as written because it contains placeholders.
- For decisions, present two or three viable options, evidence for each, and a recommendation with reasons. Do not provide a neutral list when a recommendation is possible.
- For approvals, route the request through the organization’s documented process rather than implying an informal approval is sufficient.

Separate what can be responsibly prepared from what requires the user’s judgment, memory, relationship knowledge, authority, or consent.

## 5. Ask questions only at a real decision point

Before asking, check whether the answer already exists in the conversation, prior user-authored notes, authorized correspondence, or an applicable decision record. A documented user stance is stronger than a new question.

Ask questions only when a wrong assumption would cost more time or create more risk than interrupting the user. If needed, ask two to four targeted questions. Precede them with a short context recap covering:

1. who is involved and what happened so far;
2. what is being requested now;
3. the relevant tension, trade-off, or missing decision; and
4. what each answer would change in the draft or next action.

Allow combined answers and free-text responses when the interface supports them. Avoid false either-or choices. If no meaningful fork exists, make reasonable metadata assumptions, state them in the final report, and let the user correct them later.

## 6. Decide whether a task record is needed

Skip task creation when the item is already complete, duplicated, cancelled, or can be finished in one short sitting with no meaningful wait or risk of being forgotten. For example, if the only remaining step is to review a ready-to-send draft and send it, a chat deliverable may be more useful than a record.

Create a task record when one or more of the following is true:

- Work is deferred or cannot appropriately happen now.
- A deadline, waiting condition, event, or dependency needs tracking.
- Multiple remaining steps span more than one sitting or more than one day.
- Ownership or handoff needs to be visible.
- The user explicitly requested a task record.

When uncertain, prefer chat-only delivery for a simple reply draft and a record for longer-lived work.

## 7. Create a high-quality task record

Use the user’s chosen task system and its available fields. Do not assume a particular product, database, taxonomy, or URL structure.

Set a specific imperative title, a clear status, an actual or inferred due date only when justified, and an estimate for the **remaining human effort**, not the research already completed. Select the closest user-approved domain, project, or category. If no category fits, use a neutral general category or leave it unclassified according to the system’s conventions.

Use this notes template:

```markdown
**What:** [One sentence: the request, intended outcome, and who is waiting.]
**Source:** [Link or reference to the original conversation.]
**Context:**
- [Relevant history or role context.]
- [Verified fact, dependency, or deadline.]
- [Link to an authorized supporting source, if useful.]

**Pre-completed:**
[Full draft reply, decision brief, outline, calculation, or prepared handoff. State where a communication draft was staged, if applicable.]

**Remaining for the user:**
- [Specific decision, edit, approval, or action.]
- [Specific follow-up, only if needed.]
```

After creation, verify that the record contains the intended title, notes, date, estimate, and links. Open or retrieve the created record when the system permits, so errors are caught immediately.

## 8. Report back clearly

If a task record was created, report in this order:

1. What the task is.
2. What was pre-completed and where any draft was staged.
3. The metadata assumptions: priority, urgency, due date, category, and remaining estimate.
4. Any `[VERIFY]` or `[FILL IN]` items that prevent final use.

If no task record was needed, separate briefing from deliverable exactly and place the draft last:

```markdown
## Context for the user (not part of the reply)
- [What is being asked and who is waiting.]
- [Key verified context and judgment calls.]
- [Where the draft is staged, if applicable.]
- [Any VERIFY or FILL IN warnings.]

## The reply
[Draft reply verbatim.]
```

Do not add commentary after the draft block. This keeps the draft easy to copy or use directly.

## 9. Optional draft review loop

When a draft is staged, an authorized follow-up check can compare the eventual sent message with the draft. Check only within the relevant conversation and only for the minimum period needed. If no message has been sent, reschedule a limited number of increasingly spaced checks, then stop.

Capture only reusable, non-sensitive lessons: preferred brevity, formatting, approval routing, common process steps, or recurring decision criteria. Do not store personal gossip, sensitive relationship judgments, or detailed private correspondence as style guidance.

## 10. Audit checklist and failure modes

Before finishing, check:

- Did I read the full thread and later replies?
- Is this work still active and owned by the intended user?
- Did I use only authorized, relevant information?
- Did I research enough to prepare the deliverable, but not excessively?
- Does the record contain useful pre-completed work?
- Are all uncertain facts clearly marked rather than fabricated?
- Did I avoid sending or otherwise committing an external action?
- Is the remaining user action specific and appropriately small?

Common failures are creating dead tasks, copying a message without understanding it, researching broadly without purpose, asking questions already answered in records, inventing facts to make a draft look complete, burying the draft under commentary, and tracking a trivial one-click action in a task system. Correct these by returning to the relevant gate in this workflow rather than adding more process.

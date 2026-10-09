---
name: turn-a-message-into-a-task
description: Read a complete conversation, research and pre-complete safe work, then create a useful task only when tracking the remaining action will help.
---

# Turn a message into a task

Use this workflow when a message, thread, email, support request, or other conversation may require follow-up. The goal is not merely to log work. The goal is to identify the real request, complete as much safe preparation as possible, and leave the user with the smallest clear remaining action.

Use only communication, task-management, document, calendar, and research capabilities the user has authorized. Do not assume a particular product, database schema, organization, or internal process.

If this workflow accesses private communications or records about people, first confirm a legitimate purpose and clear authorization. Use the minimum relevant sources and information. Keep unrelated personal, health, financial, family, performance, or other sensitive details out of the task and report unless they are necessary, authorized, and suitable for the intended access boundary.

## Core principles

- Read the entire relevant conversation before deciding what the task is.
- Treat later replies as potentially decisive. They may resolve, change, reassign, or cancel the work.
- Research selectively: a few deeply read sources are better than a blanket search.
- Draft communications and consequential actions; do not send, publish, schedule, approve, or commit on the user's behalf unless explicitly authorized.
- Never invent facts, dates, links, commitments, policies, or first-hand experience.
- Create a task only when it improves follow-through. A task should not outlive a very short finishing action.
- Make task records self-contained enough that the user can finish without reopening a long research trail.

## 1. Open the source and read the full conversation

Start with the linked or supplied message. If it points to a reply, open the parent and every reply. If it points to a top-level message, check for and read its full thread. For email, read the complete chain, including relevant quoted text. For a shared document, inspect all relevant sections, tabs, attachments, and linked materials that may contain requests, decisions, or dependencies.

Capture these points in working notes:

- The anchor message and why it triggered follow-up.
- The actual ask, including implied deliverables.
- Who is involved and who is waiting for an answer.
- Existing commitments, owners, deadlines, and dependencies.
- Links, files, records, policies, or procedures referenced.
- Later updates that affect status.

Resolve identities carefully when a system displays incomplete names. Use an authorized profile, displayed identity, or clear identifier from the conversation. Name a person or describe their role where necessary for clarity; do not rely on vague labels.

### Recency gate

Before researching or creating a record, determine whether the work is already complete, no longer needed, reassigned, or waiting on another party. Later replies deserve particular attention.

If the work appears complete, do not create duplicate work. Report the evidence and ask whether further follow-up is wanted. If status is unclear, describe the ambiguity rather than assuming work remains open.

## 2. Define the real task shape

State the task shape in working notes. This determines what “pre-completed” should mean.

| Task shape | What remains for the user | Best preparation |
|---|---|---|
| Reply owed | Answer, feedback, decision, or acknowledgement | Draft a concise, fact-checked reply |
| Artefact owed | A document, reference, introduction, analysis, or data output | Draft or assemble the artefact |
| Decision needed | A choice only the user can make | Prepare options, evidence, recommendation, and a likely reply |
| Follow-up or delegation | Chase, hand off, schedule, or monitor work | Draft the follow-up or prepare handoff details |
| Multi-part request | Several related deliverables | One coordinated plan with separated sub-parts |

Default to one task for related asks in one conversation. Split tasks only when they have different owners, materially different deadlines, or independent completion paths.

Rewrite the request as an outcome, not a message label. Prefer “Review proposal and send decision” to “Message from project group.”

## 3. Gather only relevant context

Choose sources based on the actual task, not habit. Stop when you can complete useful preparation or can name exactly what blocks it.

Useful source choices include:

- **Person-related work:** relevant prior correspondence, meeting notes, role records, documented agreements, and prior feedback. For a reference, feedback, transition, or negotiation, look for the user’s documented stance or talking points before asking them to repeat it.
- **Project or event work:** recent project messages, plans, decision logs, linked documents, schedules, and retrospective notes.
- **Data questions:** authoritative records, source datasets, prior reports, and operational correspondence that may contain underlying numbers or dates.
- **Policy or process questions:** the current approved policy, relevant precedent, and procedures from the responsible function. Where a comparable established policy exists, use it as an anchor rather than inventing a new approach.
- **Repeated asks:** search broadly for the topic, not only a person’s name. A prior answer or parallel request may avoid duplicated effort.
- **Linked materials:** open them. If a document has multiple sections, tabs, or attachments, check all potentially relevant parts before concluding that the message captures the whole ask.

Use public research only when appropriate. Prefer methods that do not expose private information through unnecessary external queries. If a source cannot be accessed or verified, say so rather than guessing.

## 4. Pre-complete the work safely

Do as much useful work as possible without making an external commitment.

For communication in the user’s voice, first consult authorized writing guidance, prior approved examples, or stated preferences. If none exists, use clear, direct language and do not claim to know the user’s personal view. Keep drafts shorter than the research brief unless detail is needed for accuracy or care.

### Drafting rules

- Draft; do not send.
- Stage a draft in the relevant conversation only when authorized and when the system supports a reversible draft state.
- Include the complete draft in task notes or the final report so it remains recoverable.
- Use readable formatting: leave a blank line before lists and write direct list items instead of unnecessary lead-ins.
- Ask one simple question when one will do; do not turn a small request into a long questionnaire.
- State future commitments as conditional unless they are already authorized.
- Route funding, approval, or exception requests through the established process rather than granting an informal approval.

For a decision, prepare a compact brief with two or three viable options, the strongest evidence for each, and a recommendation with reasons. The purpose is to reduce the user’s thinking load, not merely list information.

### Uncertainty and memory gaps

Never fabricate a fact. Mark unresolved details directly where they matter:

- `[VERIFY: confirm the date in the source record]`
- `[SEARCH: locate the current policy link]`
- `[FILL IN: personal observation or relationship context needed]`

Put essential gaps inside the draft rather than removing the affected section. A partial draft can still save framing work if the missing step is obvious. Clearly warn when it cannot be sent unchanged.

List judgment calls, sensitive relationship context, and first-hand experience the user must provide under **Remaining for the user**. Make every item specific.

## 5. Ask questions only for real forks

Before asking, check whether the user already answered the question in a prior message, planning document, decision record, or email. A documented stance is usually better than interrupting the user for the same decision again.

Ask questions only when a wrong assumption would create meaningful rework, risk, or an inappropriate commitment. If questions are needed:

1. Give a short context recap: who is involved, what has happened, what is now needed, and the relevant tension.
2. Ask two to four focused questions at most.
3. Allow combined choices and a free-text response.
4. Explain the practical consequence of each choice when helpful.

Do not ask merely to perfect metadata such as priority or category. Make a reasonable default and disclose it.

## 6. Decide whether a task record is needed

Skip task creation when the remaining action is one short sitting, such as reviewing a prepared reply, making a small edit, and sending it. In that case, provide the context and draft directly.

Create a record when one or more of these are true:

- The work is deferred or cannot be done now.
- There is a deadline, wait, dependency, or follow-up worth tracking.
- Multiple steps remain or work will span several days.
- Another person is waiting and follow-through could be lost.
- The user explicitly requested a task.

When uncertain, prefer chat-only delivery for a simple reply and a task record for longer-lived work.

## 7. Create a high-quality task record

Use the user’s chosen task system. Verify available fields and valid values instead of assuming a schema.

| Field | Guidance |
|---|---|
| Title | Imperative, specific, and short; describe the finish line |
| Status | The appropriate open status, such as “To do” |
| Due date | Only when supported by an explicit or clearly implied deadline |
| Priority | Best judgment based on stakes, waiting parties, and urgency |
| Estimate | Remaining user time, not time already spent researching |
| Area or project | Best-fit category, verified against available options |
| Notes | Context, source, prepared work, and exact remaining steps |

Use this notes template:

```markdown
**What:** [One-line outcome and who is waiting.]
**Source:** [Conversation or record link, if authorized to store it.]
**Context:**
- [Key fact or decision]
- [Key dependency or deadline]
- [Relevant supporting source]

**Pre-completed:**
[Full draft, decision brief, outline, or prepared materials. State where a draft is staged, if applicable.]

**Remaining for the user:**
- [Specific finishing action]
- [Specific verification, choice, or approval]
```

Open or re-read the saved record after creation to confirm the title, notes, links, ownership, and fields are correct.

## 8. Report back clearly

If a task record was created, report in this order:

1. What the task is.
2. What was pre-completed and where any draft is staged.
3. Metadata assumptions: priority, urgency, due date, and remaining estimate.
4. Any `[VERIFY]`, `[SEARCH]`, or `[FILL IN]` items.

If no record was created, sharply separate briefing from deliverable. Put the deliverable last so it can be copied without cleanup:

```markdown
## Context for the user (not part of the reply)
- [Ask, waiting party, key facts, assumptions, and unresolved checks.]
- [State whether a draft has been staged.]

## The reply
[Verbatim draft]
```

Do not add commentary after the reply block.

## 9. Review staged drafts after the outcome is known

Whenever a communication draft is staged, schedule a single later review where authorized and technically available. A reasonable initial delay is about one hour, adjusted for the conversation’s urgency and the user’s normal working pattern.

The review instruction should identify each staged draft, its conversation location, and where the draft text can be found. At review time:

1. Re-read the relevant conversation and determine whether the user sent a final message.
2. If a final message exists, compare it with the staged draft. Note what was cut, reworded, reordered, added, or left out.
3. Extract only general reusable lessons, such as preferred brevity, tone, ordering, conditional commitments, approval routing, or useful source types.
4. If no message has been sent, reschedule at most two additional checks with increasing intervals, then stop. The user may have deliberately chosen not to send it.

Do not repeatedly chase the user, and do not store private conversation content, individual judgments, or sensitive facts merely to improve future drafts.

## 10. Improve the workflow after each run

After delivering the task or draft, perform a brief internal quality review. Update approved workflow guidance only when the run revealed a durable, general lesson, such as a necessary source type, a tool limitation and workaround, a missing task shape, or an instruction that caused avoidable effort.

Keep improvements small and general. Do not encode names, private events, confidential facts, or one-off interpersonal judgments. If no reusable lesson emerged, make no change.

## 11. Quality audit

Before finishing, check:

- Did I read the whole relevant conversation and linked materials?
- Did I confirm the work is still open?
- Is the task outcome clear and owned by the right person?
- Did I use only necessary, authorized private information?
- Did I research enough to prepare useful work without over-researching?
- Did I draft rather than send or make an external commitment?
- Are unknown facts marked clearly rather than guessed?
- Is a task record genuinely useful?
- Can the user see exactly what remains and complete it quickly?
- If a draft was staged, is a bounded follow-up review scheduled or consciously unavailable?

If any answer is no, correct it before creating the record or delivering the draft.

---
name: run-a-reference-call
description: Prepare a focused reference call for a job candidate, with a briefing page, an opening, and questions that draw out specific evidence. Use when someone has a reference call coming up.
---

# Run a reference call

Use this workflow when a hiring manager is checking references on a candidate for a role at their own organization. The output is a ready-to-use call page saved in the user's notes or meeting system. It holds context, a tailored opening, briefing notes, and a question list.

**Direction check:** this workflow is for references you collect on a candidate you might hire. If an outside organization is asking *you* for a reference on someone you know, use a separate "give a reference" workflow instead.

## Quick version

Light path: paste the candidate's CV (or a short summary of it), the role, and the referee's name and role. Ask for the briefing page. No connected tools are needed.

- The assistant writes a short context section: who the referee is and how they worked with the candidate.
- It drafts a tailored opening you can read out in under a minute.
- It writes briefing notes: what this referee can uniquely confirm, and any themes from earlier references to test.
- It gives one list of core questions plus three or four probes for the role.
- After the call, paste your rough notes back and ask it to separate what the referee saw from what they concluded.

**The page is the deliverable.** Do not stop after research or reply with a chat summary. The hiring manager will read the page, not the conversation. Everything useful must be on the page.

## Privacy and authorization

Reference checks involve personal information about two people: the candidate and the referee. Research only when you are authorized for a legitimate hiring purpose, the candidate has supplied or agreed to this referee, and the user has connected the sources you search. Use the minimum relevant information: role, organization, working relationship, and work history that bears on the job, and leave out personal life, health, family, protected characteristics, and anything unrelated to performance. Keep the page within the hiring team, and record or transcribe the call only if your policy allows it and the referee agrees at the start.

## Inputs

| Input | Source if not provided | Notes |
|---|---|---|
| Candidate name | Required from user | The person being hired |
| Referee name and contact | Calendar invite, candidate's reference list email | The person being called |
| Role | Hiring emails, notes, or applicant tracking system | Needed for role-specific probes |
| Call date | Calendar event; otherwise today | Date only is fine |
| Hiring manager name and organization | User profile or user's choice | Used in the opening and page attendees |

## Steps

When tools are connected, run every step in order. Otherwise, use the Quick version with what the user pastes in.

### Step 1: Find the scheduled call

- Search the user's calendar for events with the referee's name or contact.
- Extract the title, time, attendees, video link, and any scheduling notes.
- If there is no event yet, note that and continue.

### Step 2: Gather context

**2a. Hiring context.** Search the user's email and notes for the candidate's name to learn:

- The role they applied for.
- Their current stage (interview, work trial, final round).
- How the referee was introduced. The candidate's reference list message is usually the key source.
- The referee's relationship to the candidate (manager, client, peer, direct report, teacher).

**2b. Research the referee.** Run these searches in parallel, within authorized sources:

1. Email: direct correspondence with the referee's address.
2. Email: the referee's full name, to catch introductions and reference threads.
3. Team chat: the referee's name and their organization's name.
4. Notes or meetings database: the referee's name, including prior meetings.
5. Calendar: past events with the referee.
6. Public web: "{Name}" plus their organization, for current role and professional background only.

From each email search, read only the few recent messages that concern the candidate, the reference, or the scheduling of this call.

**2c. Candidate links.** Collect links the hiring manager will want during the call: the applicant tracking profile, a professional profile, and any portfolio, code repository, or personal site the candidate shared in their application.

**2d. Completed references.** Search the meetings database for other reference pages on the same candidate. Read them and pull out themes, strengths, concerns, and development areas. These become specific angles to confirm or challenge in this call.

**2e. Compile findings.** Organize what you found into:

- **Who the referee is:** role, organization, short professional background.
- **Relationship:** how, in what capacity, and for how long they worked with the candidate, and how closely they saw the relevant work.
- **Hiring context:** role, stage, and next step such as work trial dates.
- **Candidate links.**
- **Other references:** who else is on the candidate's list.
- **Briefing notes:** the analysis described below.

### Step 3: Create the call page

Create a page in the user's meetings database or chosen notes tool, with properties and content together.

- **Title:** `{Date} {Referee Name} ({Candidate Name} reference)`
- **Date:** call date, date only.
- **Attendees:** the hiring manager, plus any other interviewer joining.
- **Optional:** a meeting-notes or transcription block at the top, if allowed. Include only the meeting title in it. Let the tool fill in summary and transcript during or after the call.

Use this template and tailor every placeholder:

```markdown
## Context
- [{Referee Name}]({professional profile link}): {role, organization, one-line background}.
- {Candidate} worked with {Referee} as {relationship, capacity, duration}.
- This is a reference call for [{Candidate Name}]({profile link}) ([applicant profile]({link}), {other links}), who is at {stage} for {Role} at {Organization}. Next step: {e.g., work trial dates and location}.
- {Any prior contact or relationship history with the referee.}
- {Candidate}'s other references: {list}.

## Opening
> Hi {Referee}, thanks so much for making the time. I'm {Hiring Manager}, {their role} at {Organization}. {One sentence on what the organization does.} {Candidate} has applied for our {Role} role, and we're excited about their background. We're doing reference checks now so we can decide quickly. What you share stays within our hiring team. {If recording: Is it OK if I record so I can take accurate notes?}

## Briefing notes
- **Themes from completed references:** {who said what, and what to test now}
- **What this referee is uniquely placed to speak to:** {…}
- **Organization and relationship context:** {…}
- **Anything else:** {open questions, concerns, gaps}

## Questions
- **How did you work together?** What was {first name}'s role, and what was yours? How closely did you work day to day?
- **What did they concretely deliver, and how did it compare to your expectations?**
- **What is their standout strength?**
- **If they joined us and it didn't work out after three months, what would be the most likely reason?**
- **If things are going well at three months, what development area would I most likely make their top priority?**
- **Compared to everyone you've worked with in similar roles, where do they rank?**
- **If I were their manager, what could I do to help them do their best work for our mission?**
- **What should I have asked that I didn't?**

### {Role}-specific probes to weave in
- {Probe 1}
- {Probe 2}
- {Probe 3}
- {Probe 4}
```

## Writing the briefing notes

This is the highest-value section. It turns research into actions for this specific call.

- **Use direct language.** Write "The first referee said Jordan sometimes over-commits to side requests. Ask how this referee saw Jordan handle a crowded week." Do not write "It may be worth exploring...".
- **Attribute themes internally, test them neutrally on the call.** The page may say who raised a point. On the call, ask an open question such as "How did they decide what to drop when too much was on their plate?" Do not reveal what other referees or interviewers said, and do not lead the referee toward a conclusion.
- **Name the unique angle.** A former manager can speak to reliability and how much support the candidate needed. A peer can speak to collaboration. A client can speak to communication and delivery under pressure.
- **Flag organization links** the hiring manager should know about, such as past collaborations or shared channels.
- **If this is the first reference,** say so. List what to listen for that will be useful to compare across later calls.

## Role-specific probes

Pick probes that test capabilities the role actually needs. Write three or four. Examples:

- **Data analyst:** How do they check their own numbers before sharing them? How do they explain a messy result to someone without a data background? Do they push back when a question is badly framed?
- **Customer support lead:** How do they stay calm with an angry customer? Have they turned repeat complaints into a fix rather than a workaround? How do they coach newer teammates?
- **Engineering manager:** How do they handle an underperforming report? What do they do when the roadmap and the team's capacity disagree? How much do they still write code, and is that the right amount?

## Worked example (invented)

Inputs pasted into a plain chat: Jordan Lee's CV, applying for Data Analyst; referee Sam Ortiz, Jordan's manager for two years at a regional grocery chain. One earlier reference, from a peer, praised Jordan's clear dashboards but said Jordan sometimes says yes to too many side requests.

Briefing notes the assistant writes:

- **Theme to test:** the peer said Jordan over-commits. Sam managed Jordan's workload directly, so ask how Jordan handled a crowded week, without mentioning the peer.
- **Sam is uniquely placed to speak to:** how much support Jordan needed, and whether Jordan's analysis changed real decisions.
- **Probe:** "Tell me about a time Jordan's numbers turned out wrong. What happened next?"

## During and after the call

- Follow vague praise with "What did that look like?" or "Can you give an example?"
- Weight evidence by how directly the referee observed the work, not by their title or confidence.
- Afterward, record notes on the same page. Separate what the referee observed, how the referee interpreted it, and your own inference. Note confidence and limits on what they could know.
- Treat one reference as one input. Compare across references and other hiring evidence before deciding.

## Style and quality checks

- Context is short bullet points, not paragraphs.
- The opening is tailored to this referee and candidate. Adjust the tone if there is prior contact.
- Questions sit in one bulleted list, not numbered, with no separate agendas.
- Candidate links and other references are on the page.
- Probes match the real role, not a generic list.
- No unrelated personal details about the candidate or referee appear on the page.
- The page exists in the chosen system before you report the task complete.

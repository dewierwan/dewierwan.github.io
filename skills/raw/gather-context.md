---
name: gather-context
description: Search the sources most likely to matter and turn the findings into a concise, evidence-linked context brief for a decision, task, or conversation, while scaling research to the stakes and respecting authorization and privacy limits.
---

# Gather context

Assemble a well-sourced context brief about a person, organization, project, topic, or decision. Use it when the user needs to get up to speed before writing, deciding, meeting, planning, pitching, hiring, or taking another concrete action.

The central rule is **right-size the research**. Search enough to answer the real question reliably, but do not sweep every available source merely because access exists. A quick status question should not become a lengthy investigation; a high-stakes decision should not rely on one convenient message thread.

## 1. Confirm purpose, access, and output boundary

First identify:

- **Purpose:** What action, decision, meeting, or question will this support?
- **Subject:** Is this a person, organization, project, topic, or decision?
- **Audience:** Who may see the result?
- **Authorization:** Is there a legitimate purpose and clear permission to use any private source?
- **Destination:** Is chat sufficient, or should the result be placed in an approved shared workspace?

Access to a private system is not, by itself, a reason to search it. Search only sources that are relevant to the stated purpose.

### Additional rules for research about people

When the subject is a person, use a stricter standard:

- Use the minimum relevant sources and information needed for the task.
- Do not search private messages, personal notes, or sensitive records simply because they are accessible.
- Do not include unrelated personal details, speculative inferences, health information, family information, or protected characteristics unless clearly necessary, authorized, and appropriate.
- Respect confidentiality, consent, need-to-know limits, and reasonable privacy expectations.
- Keep the brief within the access boundary of its evidence. Do not copy restricted details into a broader or less secure destination.
- For hiring or assessment, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether the process distinguishes relevant performance. Do not make broad character judgments from incomplete information.

If purpose, authorization, subject identity, or destination is unclear, ask before searching private sources.

## 2. Scope the gather

Choose an effort level before using tools. State it in one short line so the user can redirect the work, for example: “I’ll do a standard review across the most relevant internal records and public sources.”

| Level | Use when | Typical approach |
|---|---|---|
| Quick | A reminder, simple status check, or low-stakes question. | Check one to three obvious sources, use one or two focused queries, and return a few concise findings. |
| Standard | The usual case: preparation for a normal discussion, update, or moderate-impact choice. | Search several relevant sources, inspect the strongest results, and produce a compact structured brief. |
| Deep | A high-stakes decision, major partnership, important hire, sensitive issue, or consequential commitment. | Search broadly but purposefully, use multiple query angles, verify important claims, compare conflicting evidence, and document meaningful gaps. |

When uncertain, start lighter and offer to deepen the work. Escalating is inexpensive; collecting excessive private or irrelevant material is not.

Then classify the subject to select likely sources:

- **Person:** correspondence, collaboration messages, relationship records, meeting notes, calendar history, authorized recruitment records where relevant, and public professional information.
- **Organization:** public website and credible reporting first, then correspondence, partnership records, internal notes, and relationship databases.
- **Project or initiative:** project documents, task records, working messages, meeting notes, code or change history when relevant, and usage or outcome data.
- **Topic or question:** public research plus internal strategy documents, prior discussions, and decision records.
- **Decision:** evidence about the options, assumptions, owners, constraints, risks, prior decisions, and consequences of each path.

If a name or term could reasonably refer to several things, ask one focused clarification question before searching. Otherwise, proceed without unnecessary questioning.

Set a time window. A useful default is the most recent six months, extending further back for longstanding relationships, recurring projects, or decisions with important historical context.

## 3. Select and search sources

Named sources are mandatory, but they are not necessarily exhaustive. Add another source only when a sensible researcher would expect it to contain decision-relevant evidence.

Possible source capabilities include:

- Email and direct correspondence.
- Team messages and discussion threads.
- Internal documents, knowledge bases, and decision logs.
- Shared file storage and documents.
- Calendar events and meeting notes.
- Meeting transcripts or recordings, where authorized.
- Relationship, project, applicant, customer, or operations databases.
- Product analytics or operational metrics.
- Code repositories and change history.
- Public websites, professional profiles, filings, publications, and reputable news.

For a quick or standard gather, search inline and inspect the strongest results. For deep research involving many independent source clusters, parallelize read-only searches where doing so saves time and does not expand access unnecessarily. Ask each parallel researcher to return a concise digest with direct evidence references, not a raw data dump.

### Query method

Use queries appropriate to the source and effort level:

1. Search the exact name, organization, project title, or distinctive phrase.
2. For deeper work, search aliases, related organizations, relevant colleagues, alternate spellings, and important project keywords.
3. Inspect the most relevant full threads, documents, or records rather than relying only on search snippets.
4. For a person or organization, distinguish direct correspondence from third-party mentions.
5. For a project, search both its name and the work terms likely to appear in planning or implementation records.
6. For a decision, search for options, objections, approvals, milestones, owners, and prior commitments.

If results reveal a recent or imminent meeting, check the authorized meeting notes or transcript. Such records often contain the clearest account of current decisions, commitments, and unresolved questions. Attribute speakers carefully: transcript participant labels may not perfectly identify every speaker.

When reading multi-section documents, inspect every relevant section, tab, attachment, or linked subdocument. Do not assume that the first visible section contains all material. Attribute findings precisely enough that another reader can locate them.

For public web research, prefer current primary sources for roles, dates, organizational status, product details, and announcements. Cross-check time-sensitive claims against recent authoritative evidence. Do not include a web address unless it was verified or supplied by the user.

For operational databases, first understand the relevant schema, record meaning, and field limitations. Do not treat a record system as authoritative without checking whether it is complete, current, and used consistently. Use canonical systems for their intended domain, such as an applicant system for application status or an approved project system for delivery status.

For technical projects, inspect the relevant repository, issues, release notes, and change history only when they are needed to answer the question. Code presence alone does not establish that a feature is deployed, used, or successful.

## 4. Handle missing, unavailable, and conflicting evidence

Do not silently substitute one source for another. If a source was judged relevant but is unavailable, inaccessible, or returns no useful result, say so in the brief. A deliberately skipped source does not need to be listed as a gap.

When a connected source fails:

1. Confirm the exact source, search, and failure.
2. Attempt safe diagnostics available to the researcher, such as checking configuration, connection state, account permissions, or authentication status.
3. Repair only what can be safely repaired without changing user data or expanding permissions.
4. If user action is required, state the exact remaining action, such as completing authentication or restoring access.
5. Do not claim the source was searched successfully until it was.

Treat evidence quality explicitly:

- Prefer primary records, current records, direct statements, and canonical decisions.
- Treat informal summaries, search snippets, and third-party discussion as weaker evidence.
- Separate facts, informed interpretations, and open hypotheses.
- Resolve contradictions where possible. State which evidence is more credible and why.
- Preserve uncertainty when it cannot be resolved; do not force a clean narrative.

## 5. Synthesize into a context brief

Organize findings by what the user needs to know, not by the order in which systems were searched. Lead with the facts that change the next action.

Every material sourced claim should include a direct, clickable reference to its underlying evidence when the destination supports links. Link to the specific thread, document, meeting record, database record, repository revision, or verified public page—not merely a generic home page. Do not expose a reference outside the access boundary appropriate to its source.

Use this adaptable structure:

```markdown
## [Subject] — context brief
*Scope: [quick, standard, or deep]. Sources reviewed: [source categories]. Window: [date range].*

## TL;DR
- [Most decision-relevant finding, with direct evidence reference.]
- [Current state, risk, opportunity, or recommendation-relevant fact.]
- [Important uncertainty or next milestone.]

## What we know
### [Theme]
[Synthesized finding with direct evidence references.]

### [Theme]
[Synthesized finding with direct evidence references.]

## Relationship or timeline
- [Date]: [Relevant interaction, decision, or event with evidence reference.]

## Open questions and gaps
- [Question not answered] — expected evidence source: [source category].
- [Unavailable, empty, or conflicting relevant source], if applicable.

## Key sources
- [Descriptive source title — direct evidence reference]
```

Adapt headings to the subject. A decision brief may use “Options,” “Evidence for and against,” “Constraints,” and “Decision needed.” A project brief may use “Current status,” “Milestones,” “Risks,” and “Owners.”

Keep prose scan-friendly. A quick brief may be only a short summary and a few linked facts. A deep brief may include a fuller timeline, evidence comparison, and explicitly separated risks and unknowns.

## 6. Choose the delivery method

Deliver a short brief directly in the conversation when it fits comfortably on screen and the audience is appropriate. Put the brief itself at the end of the response; place any offer of follow-up work before the brief.

For a long-lived or substantial reference brief, create it only in a user-approved, access-controlled shared document location. Use a concise, readable title containing the date and subject. Do not place private findings in local files, public locations, or broad-access workspaces without approval.

When editing an existing formatted document:

- Insert content only in a known body-text location or replace a complete, inspected section.
- Do not insert markdown or placeholders into the first character of an existing heading, list item, table cell, or styled paragraph.
- Re-read the affected range after insertion and verify heading, body, and list styles.
- If visual layout matters, render or inspect the document rather than relying only on plain-text extraction.
- Do not report completion until both content and formatting checks pass.

## Final audit

Before delivering, check:

- Is the effort level proportionate to the user’s need?
- Was each private source necessary, authorized, and used minimally?
- Did the research address the actual decision or task?
- Are material claims connected to direct evidence?
- Did the brief distinguish fact, interpretation, and uncertainty?
- Were contradictions resolved or clearly flagged?
- Are unavailable or empty relevant sources disclosed?
- Does the destination respect the sensitivity and access boundary of the evidence?
- Is the result concise enough to act on?

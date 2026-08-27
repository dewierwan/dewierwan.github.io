---
name: gather-context
description: Search the sources that are relevant to a person, organization, project, topic, decision, or meeting, then assemble a proportionate, evidence-linked context brief for an authorized purpose. Scale the research to the stakes while protecting.
---

# Gather context

Assemble a well-sourced context brief before the user writes, decides, meets, pitches, plans, or otherwise needs to get up to speed on a subject. Search only the sources that a sensible researcher would expect to contain decision-relevant information, then synthesize the findings into an organized, scan-friendly brief with direct evidence links.

The central rule is **right-size the research**. A quick status reminder should not trigger a broad sweep across every connected system. Conversely, a high-stakes decision should not rest on a few convenient messages when meeting notes, prior decisions, or operational records may contain the decisive context.

## 1. Confirm purpose, authority, and output boundary

First identify:

- **Subject:** person, organization, project, topic, decision, or event.
- **Purpose:** what action, decision, or conversation this brief will support.
- **Audience and destination:** who may see the output and where it may be stored.
- **Authorization:** whether the user has a legitimate reason and authority to access each private source.

Use private communications, calendars, transcripts, internal documents, databases, or records about people only when they are necessary for the stated purpose and the user is authorized to use them. Access to a system is not, by itself, a reason to search it.

For research about a person, use a stricter minimum-necessary standard:

- Search only sources relevant to the role, relationship, decision, or meeting.
- Include only information needed for the purpose.
- Exclude unrelated sensitive, personal, health, family, financial, or other confidential details.
- Do not infer private traits or make judgments unrelated to the task.
- Respect consent, confidentiality, need-to-know limits, and reasonable privacy expectations.
- Keep the output in a location appropriate to the sensitivity of the sources and audience.

If purpose, authority, subject identity, or output destination is unclear, ask one focused question before searching private sources.

## 2. Detect when this workflow applies

Use this workflow when the user asks to gather, pull together, review, summarize, or get up to speed on something before acting. Typical requests include:

- “Gather context on this organization.”
- “What do we know about this project?”
- “Pull together the latest on this decision.”
- “Get me up to speed before my call.”
- “Find our history with this contact.”
- “Deep-dive on this topic before I write a proposal.”

If the user specifically wants a meeting agenda, a meeting workspace page, or a pre-defined meeting-preparation deliverable, use the organization’s meeting-preparation workflow instead. This workflow produces research context, not necessarily a meeting artifact.

## 3. Scope before searching

### Choose an effort level

Pick an effort level based on wording, stakes, urgency, and the likely cost of missing information. When uncertain, start lighter and offer to deepen the research. It is usually easier to expand a brief than to recover time spent searching irrelevant systems.

| Level | Use when | Search pattern | Deliverable |
|---|---|---|---|
| Quick | The user wants a reminder, current status, or narrow factual answer. | Check the 1–3 most obvious sources with one or two focused queries each. | A few concise, linked findings. |
| Standard | The user needs practical preparation for a routine decision, discussion, or piece of work. | Search several relevant sources, use a small set of complementary queries, and read the strongest items. | A compact structured brief. |
| Deep | The decision is high stakes, externally consequential, difficult to reverse, or depends on a complete history. | Search broadly across relevant source clusters, use multiple queries per source, inspect primary records, and verify important claims. Parallelize read-only research only when it materially saves time. | A detailed, evidence-linked brief with contradictions and gaps resolved or clearly marked. |

State the chosen level in one short line before beginning when useful, for example: “Standard review across messages, documents, meeting notes, and public sources; I can expand this if needed.”

### Classify the subject

Subject type helps determine likely evidence locations:

| Subject | Usually relevant sources | Typical research focus |
|---|---|---|
| Person or external contact | Direct correspondence, internal discussions, meeting notes, calendar, relationship records, public professional sources. | Relationship history, current role, commitments, relevant context. |
| Organization | Public website and reporting, correspondence, documents, discussions, CRM or partner records. | Current position, relationship history, commercial or strategic context. |
| Project or initiative | Project documents, team messages, task or planning records, repositories, metrics, meeting notes. | Current state, decisions, owners, risks, next steps. |
| Topic or question | Public research, internal strategy documents, prior discussions, technical materials. | Definitions, options, evidence, prior organizational thinking. |
| Decision | Records for the affected project, people, organization, and alternatives. | Options, evidence for and against, constraints, ownership, unresolved questions. |
| Hiring or assessment | Authorized recruiting records, role specification, interview notes, work samples, and relevant communications. | Role-relevant capabilities, evidence quality, role alignment, and whether the process distinguishes relevant performance. |

If a name, title, or term could refer to multiple subjects, ask one narrow disambiguating question. Do not delay a clear request with unnecessary questions.

### Set time window and depth

Use the user’s stated period. Otherwise, choose a period that matches the relationship or project lifecycle. A recent operational question may need only recent weeks or months; a partnership, long-running project, or strategic decision may require older history. Note the chosen window in the brief.

Named sources are mandatory, but they are not automatically exhaustive. Add another source only when it is clearly likely to hold material context. Do not use a named-source list as a reason to search unrelated systems.

## 4. Select and search sources

Use the source capabilities available in the user’s environment. Do not assume a particular vendor, database schema, local directory, or integration exists.

For a quick or standard review, search inline using the strongest likely sources. For a deep review involving many independent sources, divide read-only work by source or source cluster and request short evidence digests rather than raw result dumps. Avoid unnecessary parallel work.

### Source-selection principles

1. **Start with primary evidence.** Direct messages, approved decisions, source documents, transcripts, task records, and canonical data are usually stronger than summaries.
2. **Search by more than one angle when needed.** Use the subject name, organization, project terms, related stakeholders, aliases, and decision keywords.
3. **Follow meaningful leads.** If email or calendar results reveal a recent meeting, inspect the authorized meeting notes or transcript. A recent transcript may be the best record of what was actually agreed.
4. **Read beyond search snippets.** Open the most important documents, threads, or records in full before relying on them.
5. **Stop when additional searching has low expected value.** Do not search every available tool for a marginal clue.

### Common source types

- **Email:** Search direct correspondence and relevant mentions in third-party threads. Read enough of the thread to understand dates, commitments, and final decisions. Link to the message thread, not an opaque identifier.
- **Team messaging:** Search names, organization names, project terms, and decision language. Retrieve permanent links for evidence-bearing messages and threads.
- **Knowledge base and internal documents:** Search the workspace using content-focused search rather than modes dominated by automatically generated events. Open the relevant pages and check linked decision records or meeting notes.
- **Cloud documents and files:** Search for project names, alternatives, and associated people. For multi-tab or multi-section documents, inspect every relevant tab or section, not merely the default first view. Attribute key findings accurately.
- **Calendar and meeting records:** Review relevant past events to establish history and upcoming events to explain timing. Retrieve notes or transcripts when authorized and material. Treat speaker labels carefully: a label such as “me” may not reliably identify one individual in a shared room or recording.
- **Structured operational data:** Consult the data dictionary, schema documentation, or record definitions first. Choose the canonical table or database for the question; verify field meanings and timestamps before drawing conclusions.
- **Applicant or recruiting systems:** Use only for an authorized hiring purpose. Focus on role requirements, application materials, interview evidence, references where permitted, and assessment results. Avoid unrelated personal information.
- **Product analytics:** Use when a feature, workflow, or page requires quantified adoption, behavior, or performance evidence. Record metric definitions, date range, and known limitations.
- **Code repositories and project files:** For technical or engineering subjects, inspect relevant code, issue history, change history, and documentation. Distinguish implemented behavior from plans or comments.
- **Local knowledge or memory stores:** Treat stored notes as background leads, not final authority. Verify time-sensitive facts against current primary sources.
- **Public web:** For organizations and people, use official sites, current professional profiles, public filings where applicable, and credible reporting. For topics, search multiple relevant angles. Verify every URL before including it.

## 5. Handle unavailable or empty sources honestly

Do not silently substitute an adjacent source when a relevant source is unavailable or returns no results.

- If you deliberately skipped a source because it was irrelevant, no gap statement is needed.
- If you judged a source relevant but it was unavailable, inaccessible, or empty, state that clearly in the brief.
- If an integration appears configured but cannot be found, perform safe diagnostics available in the environment: check tool availability, configuration, authorization state, and service status where appropriate.
- Do not ask the user to perform generic technical steps until reasonable agent-side checks have been attempted.
- If user action is genuinely required, state the exact issue, what was tried, and the single remaining action, such as completing authorization or restarting the relevant connection.

Never imply that a source was searched when it was not. Never invent a source link, document, event, or result.

## 6. Evaluate evidence and resolve conflicts

Treat all findings as claims that require context. Prefer current, direct, and canonical evidence over stale summaries or secondhand discussion.

When sources disagree:

1. Identify the conflict precisely.
2. Compare source authority, date, directness, and scope.
3. Prefer the stronger and more recent source when justified.
4. State the resolution and rationale briefly.
5. Preserve uncertainty when it cannot be resolved.

For example, if an old article lists a person in a former role while a current professional profile and recent correspondence indicate a new role, use the current evidence and mention that older reporting is stale rather than presenting both as equally reliable.

For important factual claims, retain a direct, clickable route to the underlying evidence. A quote or assertion without an accessible source link is incomplete unless the source cannot safely be linked; in that case, describe the source category and access limitation without exposing protected details.

## 7. Synthesize by decision-relevant themes

Do not organize the main narrative as “what email said, what chat said, what documents said.” Instead, organize around what the user needs to understand or do.

Lead with the highest-value findings. Separate facts, interpretations, decisions, and open questions. Keep prose compact enough to scan and act on.

Use and adapt this structure:

```markdown
## [Subject] — context brief
*Purpose: [decision, task, or meeting]. Scope: [quick/standard/deep]. Window: [dates]. Sources reviewed: [source categories].*

## TL;DR
- [Most important finding with direct evidence link.]
- [Current status, risk, or decision-relevant change with link.]
- [Recommended attention point or unresolved issue.]

## What we know
### [Theme 1]
[Synthesized finding with inline evidence links.]

### [Theme 2]
[Synthesized finding with inline evidence links.]

## Relationship or timeline
- [Date] — [Meaningful interaction, decision, or milestone.] [Verified source link]
- [Date] — [Current or next milestone.] [Verified source link]

## Decisions, owners, and next steps
- **Decision/status:** [Known decision or pending choice.] [Verified source link]
- **Owner:** [Role or team, where appropriate.] [Verified source link]
- **Next step:** [Concrete action or dependency.] [Verified source link]

## Open questions and gaps
- [Question not answered by the evidence; likely source or owner.]
- [Relevant source unavailable, inaccessible, or with no results.]

## Key sources
- [Source title or concise label]([verified URL]) — [why it matters]
```

Use the relationship or timeline section mainly for people and organizations. Use decisions, owners, risks, technical state, or options sections when those better fit the subject.

For hiring or assessment, replace broad personal profiling with sections such as:

- Role requirements and success criteria.
- Evidence of role-relevant capabilities.
- Assessment or interview evidence and its limitations.
- Role alignment and unresolved evidence.
- Whether the assessment meaningfully distinguishes relevant performance.

## 8. Choose an appropriate delivery format

For a short brief, deliver it directly in the conversation. End with the brief itself rather than adding a trailing meta-summary that makes copying harder.

For a long or durable reference brief, create it in the user’s authorized shared document system or knowledge workspace. Use a clear title in this form:

`YYYY-MM-DD: Concise, specific headline`

The title should be human-readable and describe the subject, not use a filename-like slug or a generic suffix such as “research brief.” Share only with the intended audience and only within the access boundary justified by the source material.

When editing an existing rich-text document:

1. Insert content into a known normal body paragraph or replace a complete, inspected section.
2. Avoid inserting markdown or placeholders at the start of an existing heading, bullet, table cell, or styled paragraph, because inherited formatting can corrupt the result.
3. Re-read the affected document range in a format that exposes paragraph styles.
4. Confirm body paragraphs and bullets have normal body styling, while only intended headings use heading styles.
5. If layout matters beyond paragraph styles, render or export the document and inspect it visually before reporting completion.

## 9. Final readiness gate

Before sending or storing the brief, verify:

- [ ] The purpose, audience, and authorization boundary were clear.
- [ ] The effort level matched the stakes and request.
- [ ] The subject was correctly identified.
- [ ] All named sources were searched, unless access or relevance made that impossible.
- [ ] Additional sources were checked only when materially useful.
- [ ] Relevant recent meeting notes or transcripts were reviewed when discovered and authorized.
- [ ] Important claims are supported by direct, verified links.
- [ ] Links were verified; none were guessed or fabricated.
- [ ] Contradictions were resolved, qualified, or explicitly left open.
- [ ] Unavailable and empty relevant sources are disclosed.
- [ ] Sensitive or unrelated personal information was excluded.
- [ ] The output location and sharing permissions match the access boundary.
- [ ] The brief ends with the deliverable, not an unnecessary trailing summary.

A successful context brief is not the longest possible collection of notes. It is the smallest reliable set of evidence, interpretation, and open questions that lets the user act with appropriate confidence.

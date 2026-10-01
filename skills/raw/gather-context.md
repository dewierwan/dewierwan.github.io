---
name: gather-context
description: Search the minimum set of relevant, authorized sources and turn the findings into a clear, evidence-linked context brief for a person, organization, project, topic, or decision.
---

# Gather context

Use this workflow when someone needs to get up to speed before writing, deciding, meeting, pitching, planning, hiring, or taking another consequential action. The result is a concise, well-sourced context brief that helps the user act; it is not a raw search dump.

## 1. Establish purpose, authority, and audience

First identify the action, decision, or question the research must support. Examples include preparing for a partner conversation, understanding the current state of an initiative, assessing options for a project decision, or reviewing a candidate’s role-relevant background.

Before searching private systems, confirm all of the following:

- There is a legitimate organizational, professional, or personal purpose.
- The user is authorized to access the proposed sources and use them for that purpose.
- The intended audience is permitted to receive the resulting information.
- The requested scope is proportionate to the decision and its stakes.

For research about a person, use a stricter minimum-necessary standard:

- Search only sources likely to contain information relevant to the stated purpose.
- Do not inspect private messages, journals, recordings, personnel material, or other sensitive records merely because they are available.
- Omit unrelated personal details, sensitive characteristics, and speculation.
- Do not infer private attributes from limited evidence.
- For hiring or assessment, focus on role-relevant capabilities, work evidence, role alignment, and whether an assessment distinguishes relevant performance.
- Keep the brief within the appropriate access boundary. Do not place restricted findings in a broadly accessible location.

If the purpose, authorization, intended audience, or subject identity is unclear, ask one focused question before accessing private information. Do not over-question a request that is otherwise clear.

## 2. Scope the research before searching

Right-size the effort. The two main failure modes are equally harmful:

- **Over-gathering:** searching every connected system, creating excessive parallel work, and producing a long report for a simple status question.
- **Under-gathering:** relying on one convenient source when the relevant history, decision, or agreement is likely elsewhere.

Choose an effort level based on wording, stakes, time sensitivity, and the likely cost of being wrong.

### Quick

Use for requests such as “remind me,” “where are we,” or a narrow status check. Search one to three obvious sources, use one or two strong queries per source, and return a few concise findings. Search directly rather than creating unnecessary parallel tasks.

### Standard

Use for ordinary preparation for a meeting, decision, outreach, or project update. Search several relevant sources, follow meaningful leads, and write a compact structured brief. Parallelize only when it materially reduces delay.

### Deep

Use for high-stakes decisions, major commitments, sensitive negotiations, senior hiring, material investments, or complex strategic work. Search broadly across relevant source categories, run multiple queries per category, retrieve primary records, verify important claims, and resolve contradictions.

When uncertain, start with the lighter reasonable tier and offer to extend the review. State the selected scope briefly so the user can redirect it. For example: “I’ll do a quick review of the obvious internal records and public information; I can expand this into a deeper sweep if needed.”

Set a time window as well. A useful default is recent activity plus enough older history to explain the current state. Extend farther back when the relationship, project, or decision has a long history.

## 3. Classify the subject and select sources

Classify the request before choosing systems. A source is worth searching only when a sensible researcher would expect it to contain decision-relevant evidence for this particular request.

- **Person:** relevant correspondence, collaboration messages, meeting records, calendar history, authorized relationship records, and public professional information. Include hiring systems only for a legitimate hiring-related purpose.
- **Organization:** current public materials first, then internal correspondence, partnership records, prior meeting notes, and authorized pipeline or relationship records.
- **Project or initiative:** project documents, work-tracking records, team messages, decision logs, shared files, code repositories where relevant, and product or operational metrics when relevant.
- **Topic or question:** public research plus internal strategy documents, prior analyses, team discussions, and technical records where they bear on the question.
- **Decision:** gather evidence around the options, decision criteria, owners, constraints, risks, and arguments for and against each option.

Named sources are mandatory, not exhaustive. If the user requests email and public research, search both. Add another source only when it is clearly likely to contain material evidence, such as a meeting record discovered through a calendar entry or message thread.

If a recent meeting with the subject appears likely, especially one in the current week, retrieve authorized notes or a transcript. Meeting records often contain the clearest account of what was agreed, requested, or deferred. Attribute speakers carefully: labels such as “me” or “participant” may not uniquely identify a person.

## 4. Search systematically and proportionately

Use the capabilities available in the user’s environment. Typical source categories include:

- Email and direct correspondence.
- Team chat and discussion threads.
- Shared documents, knowledge bases, and file storage.
- Calendar events, meeting notes, and authorized transcripts.
- Relationship-management, applicant-tracking, project-tracking, or operational databases.
- Product analytics or operational metrics.
- Source code and version history for engineering questions.
- Public web sources, including official sites and current professional profiles.
- Approved internal memory or prior briefs, treated as leads rather than unquestioned truth.

For a standard or deep review, search from multiple useful angles: the subject’s name, organization, project name, alternate names, related people, relevant decision terms, and dated milestones. Read the primary record behind high-value search results rather than relying solely on snippets.

When opening a multi-part document, inspect all tabs, sections, pages, and relevant attachments. Some document tools expose only the first section by default. Record which section supports each material finding.

For public research, prefer official and current sources for role, status, funding, product, or policy claims. Cross-check time-sensitive facts against current primary sources or reliably dated professional profiles. Include a direct evidence link only when it was supplied by the user or verified directly. If a useful source cannot be verified, omit the link and state the limitation.

For structured databases, first understand the relevant schema, table purpose, field definitions, and known data-quality limits. Route searches to the table most likely to be canonical rather than crawling every database. Treat stale, incomplete, or low-confidence records as supporting evidence rather than definitive truth.

## 5. Handle unavailable sources honestly

Do not silently substitute one source for another. If a source was judged relevant but returns no results, is inaccessible, or fails technically, say so in the brief.

Distinguish among:

- A source deliberately skipped because it was not relevant.
- A relevant source searched with no meaningful results.
- A relevant source that could not be searched.

Attempt safe, tool-appropriate diagnostics before asking the user to intervene: check source configuration, permissions, authentication state, supported search syntax, and service availability. Do not expose credentials or ask users to share secrets. If user action is necessary, name the exact remaining action and explain the resulting evidence gap.

## 6. Evaluate and reconcile evidence

Prefer evidence in roughly this order:

1. Primary records and current official decisions.
2. Direct correspondence, meeting notes, and original documents.
3. Current public statements and reliably dated professional information.
4. Internal summaries, database fields, and secondary reporting.
5. Search snippets, unverified claims, and recollections.

Resolve contradictions rather than listing incompatible claims without analysis. State what conflicts, why one source is more reliable or recent, and what remains uncertain. For example, an older article may list a leader at one organization while a current professional profile and recent meeting record indicate a later move. Report the stronger current evidence and note that the older material appears stale.

Separate facts, reasonable inferences, and open questions. Do not turn absence of evidence into evidence of absence unless the searched sources and time window make that conclusion justified.

## 7. Write the context brief

Organize the brief by what the user needs to understand, not by the systems searched. Lead with the findings that affect the next action.

Use this adaptable structure:

```markdown
## [Subject] — context brief
*Scope: [effort level]. Sources reviewed: [categories]. Window: [dates].*

## TL;DR
- [Most decision-relevant finding with direct evidence link.]
- [Current state, decision, or risk with direct evidence link.]
- [Key implication for the user’s next action.]

## What we know
### [Theme]
[Synthesized finding with direct evidence links.]

### [Theme]
[Synthesized finding with direct evidence links.]

## Relationship or timeline
[Relevant chronology of contact, decisions, milestones, or changes.]

## Open questions and gaps
- [Unanswered question and the source most likely to answer it.]
- [Relevant source unavailable, empty, or not searched, with reason.]

## Sources
- [Primary source title and direct evidence link]
- [Supporting source title and direct evidence link]
```

Every factual claim drawn from a source should include a direct, clickable path to the underlying evidence where the system supports it. Link to the message thread, document, meeting record, database entry, or verified public page, rather than merely to search results. Keep quotations short and necessary; paraphrase where possible.

Calibrate length to the chosen effort level. A quick brief may contain only a short summary, key facts, and gaps. A deep brief may include a fuller timeline, competing options, evidence quality, and a detailed source list. Keep paragraphs short enough to scan and act on.

## 8. Deliver the brief safely

Return short briefs directly in the conversation when appropriate for the sensitivity of the material. Create a longer reference document only in a user-approved shared location with access controls appropriate to the sources used.

Use a clear, human-readable title with a date when useful, such as “Current partnership background and open decisions.” Avoid file-like slugs and vague labels.

When editing an existing formatted document:

- Insert into a known normal body-text location or replace an entire verified section.
- Do not insert ordinary text at the start of an existing heading, list item, or table cell where it may inherit incorrect formatting.
- Re-read the affected content after insertion and verify paragraph and list styles.
- If visual layout matters, render or inspect the document before reporting completion.

The brief itself should be the final deliverable. If offering a follow-on task, such as drafting questions, an outreach note, or a decision memo, offer it before the brief rather than appending unrelated commentary afterward.

## Final audit

Before sending, check:

- The effort level matches the user’s actual need.
- Private sources were searched only for an authorized, legitimate purpose.
- Sensitive or irrelevant personal information is omitted.
- Relevant recent meetings were considered.
- Important claims are current, attributed, and linked.
- Contradictions are explained rather than hidden.
- Relevant unavailable or empty sources are disclosed.
- No link, source access, or fact was invented.
- The output is organized around action and decision relevance.

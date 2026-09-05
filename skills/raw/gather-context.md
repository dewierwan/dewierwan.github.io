---
name: gather-context
description: Search only the sources justified for the user’s purpose, then turn the findings into a proportionate, evidence-linked context brief that supports an upcoming action or decision.
---

# Gather context

Use this workflow when the user needs to understand a person, organization, project, topic, or decision before writing, deciding, meeting, pitching, planning, or taking another consequential action. The result is a concise, organized context brief with direct links to supporting evidence.

## 1. Confirm purpose, access, and output boundary

Start by identifying what the brief must help the user do. Examples include preparing for a call, deciding between options, assessing project status, drafting outreach, or understanding a market question.

Use private communications, internal records, meeting transcripts, or personnel-related systems only when all of the following are true:

- The user has a legitimate purpose and clear authorization to access them.
- The source is relevant to the stated purpose.
- The information used is the minimum needed to answer the question.
- The intended recipient and destination are appropriate for the sensitivity of the material.

For a person-focused request, apply an especially narrow boundary. Do not search private messages, personal notes, or broad people databases merely because they are available. Omit unrelated personal details, sensitive information, and speculation. Do not infer private traits. Respect consent, confidentiality, need-to-know limits, and reasonable privacy expectations.

For hiring or assessment work, focus on role-relevant capabilities, role alignment, diagnostic evidence, and whether an assessment distinguishes relevant performance. Do not use unrelated personal information to characterize a person or support a recommendation.

If the purpose, authorization, subject identity, or intended destination is unclear, ask one focused question before accessing private sources. Otherwise, proceed without over-questioning.

## 2. Right-size the research effort

Choosing the effort level is the most important judgment in this workflow. Do not automatically perform a full sweep of every connected system.

| Tier | Use when | Expected work | Output |
|---|---|---|---|
| Quick | The user asks for a reminder, simple status, or immediate answer. | Check one to three obvious sources with one or two focused queries each. | A few evidence-linked bullets. |
| Standard | The user needs reliable context for normal planning, communication, or a routine decision. | Search several relevant sources, inspect the strongest records, and compare findings. | A compact structured brief. |
| Deep | The decision is high-stakes, externally visible, costly to reverse, or depends on a detailed history. | Search broadly, use multiple queries per relevant source, inspect primary records, verify important claims, and reconcile conflicts. | A full context brief with clear gaps and source groups. |

When uncertain, choose the lighter tier and state it briefly: “I’ll do a standard review of messages, documents, and recent meeting notes; I can expand it if needed.” Escalating later is inexpensive. Over-gathering can waste time, expose unnecessary private information, and bury the useful answer.

Avoid both failure modes:

- **Over-gathering:** searching every available system, collecting marginal facts, or producing a long report for a simple status question.
- **Under-gathering:** relying on one convenient source when the request clearly calls for broader context, such as a decision that may depend on a meeting transcript or a project document.

For each possible source, ask: **Would a sensible researcher expect this source to contain information that could materially change the answer for this request?** Relevance and effort tier both determine whether to search it.

## 3. Classify the subject and set a time window

Classify the request before searching. This determines the most useful source clusters.

| Subject type | Usually relevant source capabilities | Main research focus |
|---|---|---|
| Person | Direct correspondence, internal messages, meeting notes, calendar history, authorized relationship records, public profiles. | Current role, relationship history, commitments, and context for the next interaction. |
| Organization | Public website, public reporting, correspondence, internal discussions, partnership or pipeline records. | Current position, relationship history, strategic relevance, and decision-makers. |
| Project or initiative | Project documents, internal messages, shared files, task systems, meeting notes, code, or operational data where relevant. | Status, decisions, ownership, risks, blockers, and next steps. |
| Topic or question | Public research, prior internal thinking, technical documents, strategy notes, and relevant discussions. | Definitions, current evidence, options, trade-offs, and unanswered questions. |
| Decision | Sources relevant to each option, including prior decisions, owner input, operational data, and authoritative records. | Options, evidence for and against, dependencies, risks, and what would change the recommendation. |

Use a default time window suited to the request, such as recent months for a current-status question. Expand the window when the relationship, project, or decision has a longer history. State the window in the brief when it matters.

If a name or topic could refer to multiple things, ask one tight disambiguation question. For example: “Do you mean the prospective partner or the internal project with the same name?” Do not begin an expansive search against an uncertain target.

## 4. Select and search sources

Sources explicitly named by the user are mandatory, provided access is authorized. They are not necessarily exhaustive: add another source only when it is clearly likely to contain decision-relevant evidence.

Typical source capabilities include:

- **Email:** Search direct correspondence and relevant mentions in threads involving others. Read enough of each thread to understand the decision, not merely the subject line.
- **Internal messaging:** Search names, organization names, project terms, and related participants. Preserve direct links to load-bearing posts or threads.
- **Knowledge bases and shared documents:** Search workspace content rather than relying on broad automated summaries. Open the most relevant pages in full. If documents support tabs, sections, or embedded subdocuments, inspect all relevant parts before drawing conclusions.
- **Calendar and meeting material:** Use past events to establish relationship history and upcoming events to explain urgency. If a recent meeting is discovered, especially one near the requested decision or conversation, retrieve its authorized notes or transcript. It is often the best account of what was actually agreed.
- **Structured operational records:** Use only systems relevant to the question, such as an applicant system for an authorized hiring review, a project tracker for status, a customer record for relationship history, or product analytics for usage questions. Prefer the canonical record over stale copies.
- **Code and technical records:** For engineering topics, inspect the relevant repository, current implementation, change history, issue tracker, and operational evidence as appropriate.
- **Public web:** For people and organizations, prioritize official sites and current public profiles. For topics, use several search angles and distinguish primary research from commentary.

For quick and standard work, search inline and inspect the strongest results. For deep work across many independent sources, parallelize read-only research only if it genuinely saves time. Give each parallel researcher a clear source cluster and require a short digest with evidence links, not an unfiltered dump.

Use multiple queries in deep reviews: subject name, organization, project terms, related stakeholders, and likely aliases. Do not conclude that a source contains nothing after one weak query. Conversely, do not keep searching after the answer is sufficiently supported.

## 5. Validate evidence and manage gaps

Prefer current, primary, and authoritative evidence. A signed decision record, direct meeting transcript, current public profile, or source document is generally stronger than a summary, memory, or second-hand discussion.

When sources conflict:

1. Check dates and authorship.
2. Prefer the source closest to the event or decision.
3. Verify whether one source is stale, incomplete, or discussing a different entity.
4. State the conflict and the reason for the conclusion when it remains material.

Never invent a link, citation, title, date, or source access. Verify links before including them. Every factual claim derived from a source should include a direct, clickable route to the supporting item whenever the system permits it.

If a source judged relevant is unavailable, returns no usable results, or cannot be accessed, state that explicitly under gaps. Do not silently substitute a nearby source and imply the expected source was checked. A deliberately skipped source need not be listed as a gap.

If a connected source fails, attempt safe, tool-appropriate diagnosis first: confirm the configured capability, check authorization state, retry a narrowly scoped read, and inspect available tool documentation. If user action is still required, report the exact failure, what was tried, and the single remaining action, such as completing authorization or restarting the connection. Do not provide environment-specific repair instructions unless they match the user’s environment.

## 6. Synthesize by theme, not by tool

Write for the action the user is about to take. Lead with the facts that matter most. Do not present a chronological log of searches or a pile of source summaries.

Use this structure, adapting headings to the subject and effort level:

```markdown
## [Subject] — context brief
*Scope: [quick/standard/deep]. Sources reviewed: [source categories]. Window: [dates].*

## TL;DR
- [Most decision-relevant finding with a direct evidence link.]
- [Current state, risk, opportunity, or recommendation-relevant fact.]
- [Important uncertainty or immediate next step.]

## What we know
### [Theme]
Synthesized finding with inline evidence links.

### [Theme]
Synthesized finding with inline evidence links.

## Relationship or timeline
Relevant history, commitments, decisions, and changes over time.

## Open questions and gaps
- [Question not answered; likely source or owner.]
- [Relevant unavailable or empty source, if applicable.]

## Key sources
- [Source title]([verified direct link]) — why it matters.
```

A quick brief may include only a title, TL;DR, and key sources. A deep brief should include the full structure, but keep prose scannable. Use short paragraphs, meaningful headings, dates where useful, and bullets for decisions, risks, and open questions.

## 7. Deliver in the appropriate place

Deliver short briefs directly in the conversation. Make the brief the final block of the response; do not append a meta-summary that makes copying difficult. If offering a follow-on task, such as drafting an email or preparing questions, offer it before the brief rather than after it.

For a long-lived or reference-quality brief, create it only in the user’s authorized shared document system or other approved workspace. Use a human-readable title in this pattern:

`YYYY-MM-DD: Specific decision-relevant headline`

Do not use file-like slugs or redundant labels such as “context brief.” Share the document link and a compact statement of the central findings before the full brief only when the delivery format requires it. Do not place sensitive material into a broader-access destination merely because it is convenient.

When editing an existing formatted document, avoid inserting text into the middle of styled headings, list items, or table cells unless the document interface explicitly preserves styles. Insert into a known body-text paragraph or replace a complete, inspected section. After insertion, re-read the affected range in a format that exposes paragraph styles; confirm that body text and bullets use body style and that only intended headings use heading styles. If layout matters, render or inspect the document visually before declaring the edit complete.

## Final audit

Before sending, check:

- Is the effort level proportionate to stakes and the user’s request?
- Was every private source justified by purpose and authorization?
- Did the brief include only necessary personal information?
- Did you inspect recent relevant meeting material when discovered?
- Are important claims linked to direct evidence?
- Did you resolve or clearly flag contradictions?
- Did you identify relevant unavailable sources and real gaps?
- Is the output organized around the user’s decision rather than the tools searched?
- Is the destination appropriate for the sensitivity of the content?

If the answer to any applicable check is no, correct it before delivering the brief.

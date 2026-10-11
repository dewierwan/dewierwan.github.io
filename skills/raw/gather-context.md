---
name: gather-context
description: Search only the sources likely to matter, at an effort level matched to the stakes, and turn the findings into one concise, well-sourced context brief.
---

# Gather context

Use this workflow to build a well-sourced context brief on a person, organization, project, topic, or decision. Search only the sources that plausibly hold relevant information. Then combine the findings into one organized brief with direct links to the evidence.

Typical requests include "gather context on X", "what do we have on X", "pull everything about X", "get me up to speed on X", "what's the latest with X", and "background on X before my call". The user usually wants this before acting: writing, deciding, meeting, pitching, hiring, or catching up.

If the user wants a structured meeting-preparation document, such as an agenda page, use a dedicated meeting-prep workflow if one exists. This workflow gathers raw context. If it is unclear which the user wants, ask.

## The most important rule: right-size the effort

Match the depth of the search to what the user actually needs. "Remind me where we are with X" needs a quick look at two or three obvious sources and a short answer. "Deep-dive on this partner before a major decision" needs a broad search. Most requests fall in between.

There are two failure modes, and both are bad:

- **Over-gathering.** Querying every connected system, starting many parallel workers, and writing an essay when the user asked a quick question.
- **Under-gathering.** Checking one source, finding a few messages, and stopping when the request clearly needed more. The key fact is often in a chat thread or meeting record the user forgot about.

For each source, ask: *for this specific request, would a sensible researcher think it is worth checking here?* Both relevance and effort level limit breadth. Skipping an irrelevant source is good judgement, not laziness.

## Step 1: Set purpose and access boundary

State the decision, task, or question the brief must support. Use private sources only when the user is authorized to access them and they are relevant to that purpose. Having access to a source is not, by itself, a reason to search it.

When the subject is a person, apply a stricter boundary:

- Use the minimum sources and information needed for the stated task.
- Do not search private messages or records just because they are available.
- Leave out unrelated or sensitive personal details. Do not guess at private or protected traits.
- Respect consent, confidentiality, need-to-know limits, and the person's reasonable privacy expectations.
- For hiring or assessment, focus on role-relevant capabilities, diagnostic evidence of past work, and how well the person's experience aligns with the role's actual requirements. Use only the hiring records the user is permitted to see.
- Put the brief only where its audience is allowed to see the source material.

If the purpose, authorization, or destination is unclear, settle it before searching private sources.

## Step 2: Scope the request

### Pick an effort level

| Level | When to use | What to do |
|---|---|---|
| Quick | Status check or "remind me" | Check the one to three most obvious sources, one pass each. Answer in a few lines. Search directly; no parallel workers. |
| Standard | The common case | Check a handful of relevant sources with a couple of queries each. Write a tight brief. Use parallel workers only if they clearly save time. |
| Deep | High stakes: major decision, big pitch, key hire | Search broadly, use parallel workers if available, run several queries per source, and verify important claims. |

If unsure, choose the lighter level and offer to go deeper. Escalating is cheap; an oversized search is expensive. State your chosen level in one short line so the user can redirect, for example: "Quick look across email, chat, and notes. Say the word if you want the full sweep."

### Classify the subject

The subject type tells you which sources matter most.

| Subject type | Likely sources |
|---|---|
| Person (partner, funder, contact, candidate) | Email, chat, notes, calendar and meeting records, public web and professional profiles; the hiring system only if the request is hiring-related and authorized |
| Company or organization | Public web first; then email, chat, and notes for any existing relationship; relationship or partner databases if they are a partner or prospect |
| Project or initiative | Notes and wiki, chat, shared documents, operational databases, task records, code repositories, product analytics if metrics matter |
| Topic or question | Several web searches from different angles, plus internal documents and chat for prior thinking |
| Decision | Any of the above, organized around the options and the evidence for and against each |

### Clarify only when needed

If the subject is truly ambiguous, such as a bare name that could be several people or a one-word topic with several meanings, ask **one** short clarifying question before searching. A wrong-target search wastes many tool calls. If the subject is clear, start. Do not over-ask.

### Treat named sources as a floor

If the user names sources ("search my email and online"), those are required, but they are not the full list. If another source clearly holds decision-relevant context, check it too.

The most common example: **if the results show, or the request implies, a recent conversation with the subject, read the notes or transcript of it.** A calendar invite or a "good to meet you today" message is the signal. A record of what was actually said is often the richest single source.

### Set the time window

Use the window the user gives. If none is given, a reasonable default is the last six months, extended further back when the relationship or project is older.

## Step 3: Search the chosen sources

For quick and standard requests, search directly so you see results as they arrive. For deep requests, or when many sources are involved, run searches in parallel if your tools allow, one per source or source cluster. Each parallel search should return a short digest with links, not a raw dump.

Depth within each source also scales with the level. In a deep search, query by name, organization, project keyword, and related people, and do not conclude "nothing there" until you have tried the available search tools. In a quick search, one or two well-chosen queries on obvious sources is the correct amount.

### General search principles

- **Search for mentions, not just direct contact.** In email and chat, direct correspondence shows the relationship; keyword and name searches show how others discuss the subject.
- **Know your tools' blind spots.** Default search modes, readers, and labels can hide content. A "smart" search may bury results under low-value items; a document reader may return only the first tab, section, or sheet; transcript speaker labels may be wrong; auto-filled fields such as timestamps may be placeholders. Prefer the plain or complete option, read every part of a document, and note where each finding came from.
- **Use maps before crawling.** If a schema map, data dictionary, or index exists for a database or workspace, read it first so you go straight to the right place.
- **Weigh data quality.** Some systems are more reliable than others. Verify records from weaker systems, and ask before relying on sandbox, temporary, or low-priority copies.
- **Check freshness.** Confirm role and title claims against dated, current sources rather than old snapshots. Treat stored assistant notes as true when written, and confirm any file, setting, or record they name still exists.
- **Use conditional sources only when they fit.** Hiring systems for authorized hiring questions, product analytics when numbers help, code history for engineering subjects, and the user's own task or journal records when the subject is their own work.

### Handle missing or failing sources honestly

- **Never invent a link.** Include only links you verified or the user supplied. Otherwise omit the link and flag it. Cite items with links the user can open, not bare internal IDs.
- **Do not silently substitute sources.** If a source you judged relevant returns nothing or is unavailable, say so in the brief.
- **Try to fix tool failures first.** Attempt safe diagnosis and repair before involving the user. Ask the user only for a step that truly needs them, such as a login or restart, and report the exact failure, what you tried, and the one remaining action.
- A source you deliberately skipped as irrelevant is not a gap. Just do not imply you checked it.

## Step 4: Synthesize into a brief

- **Resolve contradictions.** Do not list conflicting claims without comment. Example: "An older article says they work at Organization A; their current profile says they left in March. The profile is newer, so I trust it."
- **Prefer primary and current sources.** Treat discussion and summaries as weaker than recorded decisions.
- **Lead with what matters for the user's next action.**
- **Organize by theme, not by source.**
- **Link every sourced claim.** A quote without a link is not done.

### Output template

Adapt headings to the subject. The core structure is:

```markdown
## [Subject] — context brief
*Searched: [sources]. Window: [dates]. Effort: [quick/standard/deep].*

## Summary
Three to five bullets: the most decision-relevant facts.

## What we know
Who or what this is, current state, history. Grouped by theme, with inline links.

## Relationship and timeline
(For people and organizations) How the user's organization connects to them; chronology of contact.

## Open questions and gaps
What no source answered, and which source you would expect to hold it.
Any relevant source that was unavailable or returned nothing.

## Sources
Key links, grouped, so the user can dig in.
```

Match length to depth. A quick check gets a few lines; a deep dive gets the full structure. This is a scan-and-act document, not an essay.

## Step 5: Deliver the brief

Follow the user's stated preferences for where briefs go and how they are named. If none exist, use these defaults:

- **Short brief** (fits on one screen): put it directly in the reply.
- **Long or reference brief:** save it as a document in the location the user chooses, if access rules allow. Give it a concise, specific, human-readable title, such as a date plus a headline. Avoid filename-style slugs and type labels. In the reply, give a short summary of key findings and the document link.

Make the deliverable easy to find and copy. Put follow-up offers ("Want me to draft the outreach email too?") before the brief rather than after it, and avoid trailing commentary that buries the result.

If you write into an existing formatted document, verify the result at the formatting level, not just as plain text. New text can inherit the style of where it was inserted, so insert into plain body paragraphs or replace whole sections, then re-read the affected range in a view that shows styles before reporting the edit complete.

## Final checklist

| Check | Pass condition |
|---|---|
| Purpose and access | Legitimate purpose stated; private sources used only with authorization and relevance |
| Effort level | Level stated in one line and matched to stakes |
| Source selection | Named sources covered; clearly relevant extras added; recent conversation records read |
| Honesty | Gaps and failures reported; no invented links; skipped sources not implied as checked |
| Synthesis | Organized by theme; contradictions resolved; every claim linked |
| Privacy | Unrelated or sensitive personal details omitted; destination fits the audience |
| Delivery | Matches user preferences; brief easy to find; follow-up offers placed before it |

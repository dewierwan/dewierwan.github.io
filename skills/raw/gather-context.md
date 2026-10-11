---
name: gather-context
description: Search the sources most likely to matter, at the depth the request warrants, and turn the findings into one concise, well-sourced context brief.
---

# Gather context

Build a well-sourced context brief on a person, organization, project, topic, or decision. Search the sources that plausibly hold relevant information. Then combine the findings into one organized brief with direct links to the evidence.

**Right-size the effort first. This is the most important rule.** Match the depth of the search to what the user actually needs. "Remind me where we are with X" needs a quick look at two or three obvious sources and a short answer. "Deep-dive before a major decision" needs a broad, verified search. Most requests sit in between.

Two failure modes are equally bad:

- **Over-gathering:** searching every connected system, starting many parallel searches, and writing an essay when the user asked a quick question.
- **Under-gathering:** checking one source, finding a few items, and stopping when the request clearly needed more. The key fact is often in a chat thread or meeting record the user has forgotten.

The test for any source: *for this specific request, would a sensible researcher think it is worth checking here?* Relevance and effort level both limit breadth. A topic question does not need the hiring system. A quick status check does not need every source, even if each might hold a small detail. Skipping a source is judgment, not laziness.

## When to use this

Use this when the user wants context before acting: writing, deciding, meeting, pitching, hiring, or getting up to speed. Typical requests: "gather context on...", "what do we have on...", "get me up to speed on...", "what's the latest with...", "background on... before my call".

If the user wants a structured preparation document for a specific scheduled meeting, use a dedicated meeting-prep workflow if one exists. This workflow is for raw context assembly. If unsure, ask.

## Step 1: Set purpose and access boundary

State in one line the decision, task, or question the research supports. Use private sources only when the user is authorized to access them and they are relevant to that purpose. Having access is not a reason to search.

When the subject is a person, apply a stricter boundary:

- Use the minimum sources and information needed for the stated task.
- Do not read private communications just because they are available.
- Omit unrelated or sensitive personal details. Do not infer private or protected traits.
- Respect consent, confidentiality, need-to-know limits, and reasonable privacy expectations.
- Put the brief only where its audience is allowed to see the underlying material.
- For hiring subjects, focus on role-relevant capabilities, role alignment, and diagnostic evidence from the assessment process.

If purpose, authorization, or destination is unclear, resolve it before searching private sources.

## Step 2: Scope the gather

### Pick an effort level

| Tier | When | How |
|---|---|---|
| Quick | Status check or "remind me" | 1-3 obvious sources, one pass each, a few lines of answer. Search directly. |
| Standard | The common case | A handful of relevant sources, a couple of queries each, a tight brief. Parallelize only if it clearly saves time. |
| Deep | High-stakes prep: major decision, big pitch, key hire | Search broadly, run searches in parallel, use several queries per source, verify claims. |

When unsure, choose the lighter tier and offer to go deeper. Escalating is cheap; an unnecessary exhaustive sweep is expensive. State the tier in one short line so the user can redirect, for example: "Quick look across email, chat, and docs. Say the word if you want the full sweep."

### Classify the subject

The subject type decides which sources matter most.

| Subject | Start with | Add when relevant |
|---|---|---|
| Person | Email, chat, docs, past meeting records | Public web profile; hiring records only if the purpose is hiring-related |
| Organization | Public web | Internal email, chat, docs for any existing relationship; relationship or pipeline records |
| Project or initiative | Docs and wiki, chat | Shared files, operational databases, code, analytics if there are metrics |
| Topic or question | Several web searches from different angles | Internal docs and chat for prior thinking |
| Decision | Whatever the options touch | Organize around the options and the evidence for and against each |

### Resolve ambiguity once

If the subject is genuinely ambiguous, such as a name shared by several people or a one-word topic with several meanings, ask **one** tight clarifying question before searching. A wrong-target sweep wastes effort. If the subject is clear, go straight to searching.

### Named sources are a floor, not a ceiling

Sources the user names are mandatory. If another source obviously holds decision-relevant context, check it too. The most common case: when results show or the request implies a recent interaction with the subject, such as a meeting this week, read the notes or transcript of that interaction. It is often the richest single source.

### Set the time window

Use the window the user gives. If none is given, pick one that fits the subject, such as the last few months for an active topic, and extend it when the relationship or project is older. State the window in the brief.

## Step 3: Search the relevant sources

For quick and standard tiers, search directly so you see results as they arrive. For deep searches across many sources, search in parallel, one search per source or cluster. Each should return a short digest with links, not raw dumps.

Depth within each source also scales with the tier. For a deep search, query by name, organization, project keyword, and related people, and do not conclude "nothing there" until you have tried the available search methods. For a quick look, one or two well-chosen queries is correct.

### Source principles

Apply these to whatever systems the user has chosen to connect:

- **Start with direct records, then widen.** Search direct correspondence or the subject's own pages first; when going deeper, search mentions to find where others discuss the subject.
- **Read whole items.** Some documents hide content in tabs, sections, attachments, or collapsed threads that a basic read skips. Make sure you read every relevant part and say where a finding came from.
- **Check attribution.** Speaker labels, authors, and record owners can be wrong or shared. Attribute quotes and decisions carefully.
- **Prefer canonical, maintained records.** Use schema notes or known structure to go straight to the right table or page. Treat weakly maintained records as leads to verify, and do not trust auto-filled fields, such as timestamps, without checking what they actually mean.
- **Check freshness.** Verify roles, titles, and statuses against dated, current sources rather than old articles or snapshots. Stored notes and assistant memory reflect what was true when written; verify before relying on them.
- **Use conditional sources only when they fit.** Hiring records for hiring purposes, analytics for usage questions, code history for engineering subjects, the user's personal planning records only for work the user did personally.

### Never invent links

Never write a URL you have not verified or the user did not supply. Verify it, or omit it and flag the gap.

### Do not silently substitute sources

If a source you judged relevant returns nothing or is unavailable, say so in the brief. Do not quietly fill the gap with an adjacent source. If a connected source fails, try the safe diagnosis and repair steps you control first. Involve the user only for a step that needs them, such as re-authenticating. Report the failure, what you tried, and the one remaining action.

A source you skipped as irrelevant is not a gap and need not be reported, but never imply you checked it.

## Step 4: Synthesize into a context brief

Combine the findings into one brief, organized by theme rather than by tool. Lead with what matters most for the user's next action. Resolve contradictions instead of listing both versions. For example, if an old article and a current profile disagree about where someone works, note the conflict, which you trust, and why. Prefer primary and current sources over summaries and secondhand discussion.

**Every sourced claim gets a clickable link** to its primary source. A quote without a link is not finished.

### Output template

Adapt the headings to the subject:

```markdown
## [Subject]: context brief
*Searched: [sources]. Window: [dates]. Tier: [quick/standard/deep].*

## Summary
3-5 bullets: the most decision-relevant facts.

## What we know
Who or what this is, current state, history. By theme, with inline links.

## Relationship and timeline
(People and organizations) How the user's organization connects to them; chronology of contact.

## Open questions and gaps
What no source answered, and which source would likely hold it.
Any relevant source that was unavailable or empty.

## Sources
Key links, grouped.
```

Calibrate length to the tier. A quick check gets a few lines; a deep dive gets the full structure. This is a scan-and-act document, not an essay.

## Step 5: Deliver the brief

- **Short brief:** put it directly in the reply.
- **Long or reference brief:** save it as a document in the location the user chooses, within the access boundary from Step 1. Give it a specific, human-readable title; if the user has no convention, a date prefix plus a clear headline works well. Reply with a compact summary of key findings and the link.

By default, make the brief or link the final block of the reply so it is easy to copy, and put any follow-up offer before it. Follow the user's preference if they want a different layout.

If you write into an existing formatted document, check the result in a view that shows structure and styles, not just plain text, before reporting the edit complete. Inserted text can inherit nearby formatting.

## Final checks

- The effort tier matched the request, and you stated it.
- Every named source was searched, and any other clearly relevant source was added.
- Any recent interaction with the subject had its record read.
- Unavailable or empty relevant sources are reported, not hidden.
- Every sourced claim links to evidence, and every link is verified.
- Contradictions are resolved or clearly flagged.
- Personal information is limited to what the purpose requires, and the brief sits within an appropriate access boundary.

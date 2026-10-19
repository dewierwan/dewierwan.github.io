---
name: gather-context
description: Search only the sources that matter, at a depth that fits the stakes, and turn the findings into one concise context brief where every claim links to its evidence.
---

# Gather context

Build a well-sourced context brief on whatever the user names: a person, organization, project, topic, or decision. Search the sources that plausibly hold relevant information. Then combine the findings into one organized brief in which every sourced claim links to its evidence.

Use this workflow when the user wants context before they act. That might be before writing, deciding, meeting, pitching, or hiring, or simply to get up to speed. Typical requests include "gather context on X", "what do we have on X", "pull everything about X", "what's the latest with X", and "background on X before my call".

The user may have a separate workflow for structured meeting preparation, such as one that creates a meeting page. If that is what they want, use that workflow instead. This workflow is for raw context assembly. If you are unsure which one they want, ask.

## The most important rule: right-size the effort

Match the depth of the search to what the user actually needs. "Remind me where we are with X" needs a quick look at two or three obvious sources and a short answer. A deep dive before a high-stakes decision needs a broad search with verification. Most requests fall in between. Read the request, decide how much effort is warranted, and do that much. Do not reach for maximum effort by reflex.

Two failure modes are equally bad:

- **Over-gathering:** querying every connected system, starting many parallel helpers, and writing an essay for a quick question.
- **Under-gathering:** checking one source, finding a few results, and stopping when the request clearly needed more. The key fact is often in a chat thread or meeting record the user has forgotten.

For each source, ask: *for this specific request, would a sensible researcher think it is worth checking here?* Relevance and effort level together set the breadth. A topic question does not need recruiting records. A quick status check does not need every source, even if each might hold a small detail. Skipping an irrelevant source is good judgment, not laziness.

## Step 0: Set the purpose and access boundary

State, at least to yourself, the decision or task the brief supports. Search private sources only when the user is authorized to access them and the source is relevant to that purpose. Having access is not, by itself, a reason to search.

When the subject is a person, apply stricter limits:

- Use the minimum sources and information needed for the stated task.
- Do not search private messages or records just because they are available.
- Leave out unrelated or sensitive personal details. Do not guess at private or protected traits.
- Respect consent, confidentiality, need-to-know limits, and the person's reasonable privacy expectations.
- For personal chat apps and direct messages, summarize what other people said in your own words. Do not quote their messages, and do not save them to files.
- Keep the brief in a location whose access matches the sensitivity of the sources and the intended audience.
- For hiring-related subjects, focus on role-relevant capabilities, alignment with the role's requirements, and evidence that actually reflects relevant performance.

If the purpose, authorization, or output destination is unclear, resolve it before searching private sources.

## Step 1: Scope the gather

### Pick an effort level

| Tier | When | How to search | Output |
|---|---|---|---|
| Quick | Status check, "remind me" | One to three obvious sources, one pass each, searched directly | A few lines |
| Standard | The common case | A handful of relevant sources, a couple of queries each; parallel helpers only if they truly save time | A tight brief |
| Deep | High-stakes preparation, such as a major decision, big pitch, or key hire | Broad search, parallel helpers, several queries per source, verification of key claims | The full brief structure |

If unsure, choose the lighter tier and offer to go deeper. Escalating is cheap; over-searching is expensive. State the chosen tier in one short line so the user can redirect, for example: "Quick look across email, chat, and the team wiki. Say the word if you want the full sweep."

### Classify the subject

The subject type tells you which sources matter most.

| Subject | Usually most relevant |
|---|---|
| Person (partner, funder, contact, candidate) | Email, team chat, notes, calendar and meeting records, public professional profile; recruiting records only if the matter is hiring-related and authorized |
| Organization | Public web first; then email, chat, and notes for any existing relationship; CRM or pipeline records if they are a partner or prospect |
| Project or initiative | Notes and wiki, chat, shared documents, code repositories, operational databases, product analytics if there are metrics |
| Topic or question | Several angled web searches, plus internal documents and chat for earlier thinking |
| Decision | All of the above, organized around the options and the evidence for and against each |

### Clarify only when necessary

If the subject is truly ambiguous, such as a bare name that could mean several people or a one-word topic with several meanings, ask **one** short clarifying question before searching. A wrong-target search wastes a lot of effort. If the subject is clear, go ahead. The default is to proceed, not to ask.

### Named sources are a floor, not a ceiling

Sources the user names are mandatory, but they are not necessarily the full list. If another source clearly holds decision-relevant context, check it too.

The most common case is a recent meeting. When results show, or the request implies, a meeting with the subject (especially the same day or week), read the notes or transcript for that meeting. Signals include a calendar invite or a "great to meet you this morning" message in the results. The meeting record is often the richest single source, and a brief without it misses what was actually said.

### Set the time window

Use the window the user gives. If they give none, a sensible default is the last six months, extended back further for older relationships or projects. State the window in the brief.

## Step 2: Search the relevant sources

- **Quick or standard:** search directly in the main conversation so you see results as they arrive.
- **Deep, or many sources:** run read-only searches in parallel, one helper per source or cluster. Each helper returns a short digest with links, not raw dumps. Pass the privacy rules from Step 0 to every helper, including the rule to summarize rather than quote personal chat messages.

Depth within a source also follows the tier. For a deep search, query several ways: by name, organization, project keyword, and related people. Do not conclude "nothing there" until you have used the search capabilities available. For a quick look, one or two well-chosen queries on the obvious sources is correct, not a failure.

### Source-handling principles

These apply whatever tools the user has. The list describes a thorough pass, which suits a deep search. For lighter tiers, apply them to fewer sources and only the top results.

1. **Search direct and indirect.** Look for direct contact with the subject (messages from or to them). In deeper passes, also search for mentions where others discuss the subject.
2. **Prefer precise search modes.** If a tool's default search returns noisy or loosely related results, such as calendar entries flooding a document search, switch to exact or keyword search.
3. **Read the whole item.** Some documents, pages, or records hide content in tabs, sections, attachments, or threads that a simple read skips. For example, a document reader may return only the first tab unless you list the tabs and read each one. Open what matters in full and note where each finding came from.
4. **Know which records are authoritative.** For structured databases, use any map of canonical tables and field meanings before crawling. Go first to the tables the user's organization treats as the source of truth. Treat lower-quality, temporary, or sandbox data as weak until confirmed, and ask before relying on it. Watch for fields that hold default values rather than real ones, such as an automatic midnight timestamp; use a creation date instead when you need to know when something happened.
5. **Check freshness.** Web profiles and news go stale; cross-check current roles against dated sources rather than trusting an old snapshot. Stored notes or assistant memory reflect what was true when written; confirm any named file, setting, or fact still holds.
6. **Read attribution carefully.** Speaker labels in transcripts and authorship in shared records can be imprecise. For example, a transcript's label for the user may include anyone speaking from the same room. Do not attribute a statement to someone without reasonable confidence.
7. **Use conditional sources only when they fit.** Recruiting records for hiring matters, product analytics for usage questions, code and its history for engineering subjects, and the user's personal task or journal system only for work they did themselves and have chosen to include.
8. **Cite properly.** Use clickable links to threads, pages, messages, and documents, not raw internal IDs.
9. **Never invent a link.** Use only URLs you have verified or that the user supplied. Otherwise leave it out and flag it.

### Gaps and unavailable sources

**Do not silently substitute sources.** If a source you judged relevant returns nothing or is unavailable, say so in the brief. Do not cover the gap with an adjacent source.

If a source should be reachable but is not, treat it as a connection or loading problem. Try every safe diagnosis and repair you can first, such as checking the connection configuration, confirming the source's name mapping, or restarting a service you are allowed to manage. Ask the user only for steps that need them, such as re-authenticating in a browser or restarting the application. Report the exact failure, what you tried, and the one remaining action.

A source you deliberately skipped as irrelevant is not a gap and need not be reported, but never imply you checked it.

## Step 3: Synthesize into a context brief

Combine findings into one brief organized by theme, not by tool. Lead with what matters most for the user's next action. Resolve contradictions rather than listing both blindly, for example: "A news profile says they work at Organization A; their dated professional profile says they left in March. The profile is more recent and more likely correct."

**Every sourced claim gets a clickable link** to its primary source. A quote without a link is not finished. The user must be able to click straight through to check.

### Output template

Adapt the headings to the subject, but keep this spine:

```markdown
## [Subject]: context brief
*Searched: [sources]. Window: [dates]. Effort: [quick/standard/deep].*

## TL;DR
Three to five bullets with the most decision-relevant facts.

## What we know
Who or what this is, current state, history. By theme, with inline evidence links.

## Relationship / timeline
(For people and organizations) How the user's organization connects to them; chronology of contact.

## Open questions / gaps
What no source answered, and which source would likely hold it.
Any relevant source that was unavailable or empty.

## Sources
Key links, grouped, so the user can dig in.
```

Match length to depth and keep prose blocks short. A quick check gets a tight brief; a deep dive gets the full structure. This is a document to scan and act on, not an essay.

### Where the brief goes

- **Short brief (fits comfortably on screen):** give it directly in the reply.
- **Long or reference brief:** save it as a document where the user keeps generated documents, at an access level that suits the content. Follow the user's naming convention. If none exists, use the ISO date plus a concise, specific, human-readable headline, in the form "[YYYY-MM-DD]: Options for next year's partner program". Avoid filename-style slugs and type suffixes like "(context brief)". Do not scatter briefs into stray local files unless the user prefers that. Reply with a compact summary of key findings and the link.

Make the brief (or summary plus link) the final part of the reply, with no closing meta-summary after it. Put any follow-up offer, such as "Want me to draft the outreach email?", before the brief. This keeps the deliverable easy to copy.

### Editing an existing formatted document

If you insert the brief into an existing formatted document:

1. Do not insert at the first character of an existing heading, list item, table cell, or other styled paragraph. New text can inherit that style, turning body text into headings.
2. Insert into a known plain body paragraph, or replace a complete section whose boundaries and styles you have read from the document's structure.
3. After every insertion, re-read the affected range at the structural level and check each paragraph's style. Body text and bullets should be normal text; only intended headings should carry heading styles.
4. A plain-text read or heading search does not confirm formatting. Do not report the edit complete until the style check passes. If layout matters beyond paragraph styles, render or export the document and inspect it.

## Readiness checklist

| Check | Pass condition |
|---|---|
| Purpose and access | Task stated; sources authorized and relevant; person-related data minimal |
| Effort | Tier matches the stakes and is stated in one line |
| Coverage | Named sources searched; obviously decision-relevant sources, especially recent meeting records, added |
| Evidence | Every sourced claim has a verified, clickable link; no invented URLs |
| Conflicts | Contradictions resolved or clearly flagged |
| Gaps | Unavailable or empty relevant sources reported; skipped sources not implied as checked |
| Delivery | Output in the right place with appropriate access; brief is the final block |

## Common failure modes

| Failure | Fix |
|---|---|
| Searching every system for a quick question | Choose the lighter tier and offer to go deeper |
| A one-source answer to a high-stakes request | Classify the subject and cover its source cluster |
| Missing what was said in a recent meeting | Read the meeting record when one appears |
| Trusting stale profiles or memory | Cross-check against dated, current sources |
| Reading only part of a document or record | Open hidden sections, tabs, and threads |
| Covering a gap with a nearby source | Report the gap explicitly |
| Quoting or storing personal chat messages | Summarize in your own words and do not save them |
| Including unrelated personal details | Keep only what the stated task needs |
| Reporting a document edit done after a plain-text check | Verify paragraph styles at the structural level |

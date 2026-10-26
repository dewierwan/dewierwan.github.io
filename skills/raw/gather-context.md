---
name: gather-context
description: Searches the sources that matter at a depth fitting the stakes and builds one brief where every claim links to evidence. Use when someone says 'gather context on X' or 'get me up to speed.'
---

# Gather context

Build a well-sourced context brief on a person, organization, project, topic, or decision by checking the sources that plausibly hold relevant information. The result is one organized brief in which every sourced claim links to its evidence.

## Quick version

- Decide how much effort the request deserves: a quick reminder, a standard brief, or a deep dive before a high-stakes decision. Say which one you picked in one line.
- If the subject is truly ambiguous, such as a bare name or a one-word topic, ask one short clarifying question. Otherwise, proceed.
- Without connected tools, ask the user to paste what matters: recent emails, chat threads, documents, links, and especially notes from any recent meeting with the subject, which are often the richest source.
- Organize findings by theme, not by source, and lead with what matters most for the user's next action. Resolve contradictions instead of listing both sides blindly.
- Tie every claim to where it came from (the pasted email, the meeting notes, a link the user gave). Never invent a link or a fact.
- End with a short "Open questions / gaps" list: what no material answered and where the answer probably lives.

## 1. When to use this

Use this workflow when the user wants context before they act: before writing, deciding, meeting, pitching, or hiring, or simply to get up to speed. Typical requests include "gather context on X", "what do we have on X", "pull everything about X", "what's the latest with X", and "background on X before my call".

If the user has a separate workflow for structured meeting preparation and that is what they want, use it instead. This workflow is for raw context assembly. If you are unsure which they want, ask.

Because this workflow can read private messages and records about other people, use them only for a legitimate purpose the user is clearly authorized to pursue, and only the minimum relevant sources and information. Leave out unrelated or sensitive personal details, and summarize what others said in personal chats in your own words rather than quoting or saving their messages. Keep the finished brief somewhere whose access matches the sensitivity of the sources and the intended audience.

## 2. Right-size the effort

This is the most important rule. Match the depth of the search to what the user actually needs. "Remind me where we are with X" needs a quick look at two or three obvious sources and a short answer. A deep dive before a high-stakes decision needs a broad search with verification. Most requests fall in between. Decide how much effort is warranted and do that much. Do not reach for maximum effort by reflex.

Two failure modes are equally bad:

- **Over-gathering:** querying every connected system, starting many parallel helpers, and writing an essay for a quick question.
- **Under-gathering:** checking one source, finding a few results, and stopping when the request clearly needed more. The key fact is often in a chat thread or meeting record the user has forgotten.

For each source, ask: *for this specific request, would a sensible researcher think it is worth checking here?* Relevance and effort level together set the breadth. A topic question does not need recruiting records. A quick status check does not need every source, even if each might hold a small detail. Skipping an irrelevant source is good judgment, not laziness.

## 3. Scope the gather

### Pick an effort level

| Tier | When | How to search | Output |
|---|---|---|---|
| Quick | Status check, "remind me" | One to three obvious sources, one pass each | A few lines |
| Standard | The common case | A handful of relevant sources, a couple of queries each; parallel helpers only if they truly save time | A tight brief |
| Deep | High-stakes preparation, such as a major decision, big pitch, or key hire | Broad search, parallel helpers, several queries per source, verification of key claims | The full brief structure |

If unsure, choose the lighter tier and offer to go deeper. Escalating is cheap; over-searching is expensive. State the tier in one line so the user can redirect, for example: "Quick look across email, chat, and the team wiki. Say the word if you want the full sweep."

### Classify the subject

The subject type tells you which sources matter most.

| Subject | Usually most relevant |
|---|---|
| Person (partner, funder, contact, candidate) | Email, team chat, notes, calendar and meeting records, public professional profile; recruiting records only for hiring matters |
| Organization | Public web first; then email, chat, and notes for any existing relationship; CRM or pipeline records if they are a partner or prospect |
| Project or initiative | Notes and wiki, chat, shared documents, code repositories, operational databases, product analytics if there are metrics |
| Topic or question | Several angled web searches, plus internal documents and chat for earlier thinking |
| Decision | All of the above, organized around the options and the evidence for and against each |

For hiring matters, focus on role-relevant capabilities, alignment with the role's requirements, and evidence that actually reflects relevant performance.

### Clarify only when necessary

If the subject is truly ambiguous, ask **one** short clarifying question before searching. A wrong-target search wastes a lot of effort. If the subject is clear, go ahead. The default is to proceed, not to ask.

### Named sources are a floor, not a ceiling

Sources the user names are mandatory, but they are not necessarily the full list. If another source clearly holds decision-relevant context, check it too.

The most common case is a recent meeting. When results show, or the request implies, a recent meeting with the subject, read its notes or transcript. Signals include a calendar invite or a "great to meet you this morning" message. The meeting record is often the richest single source, and a brief without it misses what was actually said.

### Set the time window

Use the window the user gives. If none, pick an adjustable default, such as the last several months, and extend it for older relationships or projects. State the window in the brief.

## 4. Search the relevant sources

- **Quick or standard:** search directly in the main conversation so you see results as they arrive.
- **Deep, or many sources:** run read-only searches in parallel, one helper per source or cluster. Each returns a short digest with links, not raw dumps. Give helpers the same scope and handling rules you are following.

Depth within a source also follows the tier. For a deep search, query several ways: by name, organization, project keyword, and related people, and do not conclude "nothing there" until you have used the search capabilities available. For a quick look, one or two well-chosen queries on the obvious sources is correct, not a failure.

### Source-handling principles

These apply whatever tools the user has. Apply them fully on deep searches and lightly on quick ones.

1. **Search direct and indirect.** Look for direct contact with the subject, and in deeper passes, for places where others discuss the subject.
2. **Prefer precise search.** If a default search returns noisy or loosely related results, switch to exact or keyword search.
3. **Read the whole item.** Documents and records can hide content in tabs, sections, attachments, or threads that a simple read skips. Open what matters in full and note where each finding came from.
4. **Trust authoritative records.** Go first to the records the user's organization treats as the source of truth for that kind of subject. If records have been reorganized or renamed, use their current home, not the old one. Treat temporary, sandbox, or low-quality data as weak until confirmed, and be wary of fields that may hold placeholder values rather than real ones.
5. **Check freshness and attribution.** Web profiles, news, and stored notes reflect what was true when written; cross-check against dated, current sources. Speaker labels and authorship can be imprecise, so do not attribute a statement without reasonable confidence.
6. **Use conditional sources only when they fit.** Recruiting records for hiring, analytics for usage questions, code history for engineering subjects, and the user's personal task or journal system only for their own work when they choose to include it.
7. **Cite with real links.** Link to threads, pages, messages, and documents, not raw internal IDs. Use only URLs you have verified or the user supplied; otherwise leave the link out and flag it.

### Gaps and unavailable sources

**Do not silently substitute sources.** If a source you judged relevant returns nothing or is unavailable, say so in the brief. Do not cover the gap with an adjacent source. A source you deliberately skipped as irrelevant is not a gap and need not be reported, but never imply you checked it.

## 5. Synthesize into a context brief

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

Match length to depth and keep prose blocks short. This is a document to scan and act on, not an essay.

## 6. Deliver the brief

- **Short brief (fits on screen):** give it directly in the reply.
- **Long or reference brief:** save it where the user keeps generated documents, following their naming convention. If none exists, use the date plus a concise, specific, human-readable headline, such as "[YYYY-MM-DD]: Options for next year's partner program", not a filename-style slug or a type suffix. Reply with a compact summary of key findings and the link.

Make the brief (or summary plus link) the final part of the reply, with no closing meta-summary after it. Put any follow-up offer, such as "Want me to draft the outreach email?", before the brief so the deliverable stays easy to copy.

## 7. Worked example

A program lead at the fictional Brightwater Learning Collective says: "Background on the Harbor Lane Community Fund before my call tomorrow."

The assistant classifies the subject as an organization with an existing relationship and picks Standard: "Standard look across email, team chat, notes, meeting records, and the web. Say the word if you want the full sweep." Email shows a thank-you message from yesterday, so it also opens that meeting's notes even though the user did not mention them. The brief opens like this:

```markdown
## Harbor Lane Community Fund: context brief
*Searched: email, team chat, notes, meeting records, web. Window: last 9 months. Effort: standard.*

## TL;DR
- Program officer asked for a revised budget by month end ([email thread])
- Yesterday's call: they favor multi-year grants over one-off awards ([meeting notes])
- Their public site lists a new grants director; our notes still name the old one ([fund website], [notes page])

## Open questions / gaps
- Current decision timeline: not in any source; likely in the program officer's next email
- Shared budget folder was unavailable during the search
```

## 8. Readiness checklist

| Check | Pass condition |
|---|---|
| Effort | Tier matches the stakes and is stated in one line |
| Coverage | Named sources searched; obviously decision-relevant sources, especially recent meeting records, added |
| Evidence | Every sourced claim has a verified, clickable link; no invented URLs |
| Conflicts | Contradictions resolved or clearly flagged |
| Gaps | Unavailable or empty relevant sources reported; skipped sources not implied as checked |
| Delivery | Output in the right place; brief is the final block |

## 9. Common failure modes

| Failure | Fix |
|---|---|
| Searching every system for a quick question | Choose the lighter tier and offer to go deeper |
| A one-source answer to a high-stakes request | Classify the subject and cover its source cluster |
| Missing what was said in a recent meeting | Read the meeting record when one appears |
| Trusting stale profiles, notes, or memory | Cross-check against dated, current sources |
| Reading only part of a document or record | Open hidden sections, tabs, and threads |
| Searching where a record type used to live | Check the current map and go to its present canonical home |
| Covering a gap with a nearby source | Report the gap explicitly |

## Optional extras

### Structured databases

If the user keeps a map of their databases (which tables are canonical, what fields mean, known quirks), read it before crawling so you go straight to the right place. Route by subject: each kind of record, such as applications, payments, or contacts, usually has one canonical home, and a dedicated, consolidated table for a record type beats older scattered copies. Organizations split, merge, and rename these stores over time, so if the map shows a record type has moved, search its new home, and suggest updating the map when you notice it is out of date. When a field seems to show when something happened, confirm it is a real value and not an automatic default; a record's creation date is often more reliable.

### Repairing an unavailable connection

If a connected source should be reachable but is not, treat it as a connection problem. Try every safe diagnosis and repair you can first, such as checking the configuration, confirming the source's name, or restarting a service you are allowed to manage. Ask the user only for steps that need them, such as re-authenticating or restarting the application. Report the exact failure, what you tried, and the one remaining action.

### Editing an existing formatted document

If you insert the brief into an existing formatted document, new text can inherit the style of the paragraph it lands in. Insert into a plain body paragraph or replace a complete section whose structure you have read, never at the start of a heading, list item, or table cell. Afterward, re-read the affected range at the structural level and confirm body text and bullets carry normal styles and only intended headings carry heading styles. A plain-text read does not confirm formatting, so do not report the edit complete until this check passes.

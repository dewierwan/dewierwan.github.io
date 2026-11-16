---
name: before-after-feedback
description: Researches a draft's topic, then gives before, after, and why feedback, one entry per change. Use when asked for before/after feedback or to check a draft against the literature.
---

# Give before and after feedback

This workflow researches a draft's topic and then returns feedback as a numbered list of separate changes. Each change shows the current text, the replacement, and the reason, so the author can accept or reject each one on its own. Because the research comes first, the feedback catches errors of substance and not only wording.

## Quick version

- Paste the draft and any sources you have. Ask the assistant to read the draft twice: once for the argument, once sentence by sentence.
- Have it check each claim against its cited source for three common slips: who said it, what a number actually measures, and how strong the claim is. If it cannot open a source, it should list the claims for you to check.
- Propose a change only where it fixes a factual error, a misstated argument, a missing step, an unsupported claim, a weak answer to an objection, or a sentence that needs rereading. Skip changes that are only a matter of taste.
- Write one entry per change: **Before** (exact current text), **After** (ready to paste), **Why** (one sentence).
- Write the After text in the author's voice, and flag any claim or opinion the assistant added that the author did not already hold.
- Open with a short verdict and an honest list of what was read. Put the entries and any structural notes at the end.

## 1. Set the scope

The input is the draft (or access to it), plus usually the topic or the sources to read. If there is no draft, ask for it before doing anything else.

This is feedback only. Do not edit the author's document unless they ask. This workflow is for improving an existing draft; it is not for writing a document from scratch or for short messages like email, which call for a drafting workflow instead.

## 2. Read the draft and everything it cites

Read the draft twice. The first pass is for the overall argument: what is the author trying to show, and in what order? The second pass is sentence by sentence.

Then open every source the draft links or cites and check that each sentence says what its source says. Three mismatches come up again and again:

- **Attribution.** One person's prediction or opinion presented as an established fact.
- **What a number measures.** A figure about one group or quantity presented as if it were about another, for example a share of respondents turned into a share of the whole population.
- **Strength.** A hedged or qualified claim in the source turned into a confident one in the draft, such as "may help" becoming "solves."

For any number or claim with no source, search for one. If you cannot find support, say what you did find instead of silently dropping the question.

## 3. Research the topic

Read enough to judge whether the draft's account is right, complete, and current. Cover three things:

- **The standard accounts.** Find the works the field treats as the origin of each idea the draft uses. A common error is to name a concept correctly and then explain it with a different mechanism from the one its originators described.
- **The strongest objections,** and how the idea's proponents have answered them.
- **What changed recently.** Check today's date, then look for recent evidence the draft could use or that contradicts it. Adjust how far back "recent" means to suit the field.

Read the primary page for anything an entry will depend on. Search summaries and snippets are fine for finding leads but not for supporting a correction. Keep track of which sources you read in full, which in part, and which only as summaries, because the reply must say so.

If your assistant has no browsing, work from the sources the author pasted and from general knowledge, say plainly that this knowledge may be dated or incomplete, and mark every correction that depends on unchecked facts.

## 4. Choose the changes

Propose a change only where it fixes one of these:

- a factual error
- a mechanism or argument that misstates its source
- a missing step the reader needs to follow the argument
- a claim with no support
- an objection answered weakly or not at all
- a sentence a reader would have to read twice

Leave alone anything that is merely different from how you would write it. The author should be able to trust that every entry is worth their time; padding the list with preferences erodes that trust.

Compare parallel sections. When two sections cover similar ground and one has something the other lacks, such as supporting evidence or a reply to an objection, propose the missing piece as an addition to the weaker section.

## 5. Write one entry per change

Write one entry per change, not one per paragraph, so each can be taken or left independently. Use this template:

```
**[N]. [Short label for the change]**

**Before:** [exact text in the draft now]

**After:** [text that would replace it]

**Why:** [one sentence]
```

Rules for each part:

- **Before** is copied character for character, so the author can search for it in their document. Quote the smallest span that contains the change: a clause or a sentence, not the whole paragraph.
- **After** is ready to paste. Keep the author's links. Keep it the same length or shorter unless the change is an addition.
- **Why** is one sentence. When the reason is a fact, name the source. Add a second sentence only to tell the author something they must check.
- **An addition** uses `**Before:** (nothing; add after "...")`, quoting the text it follows.
- **A cut** uses `**After:** (cut)`, or `(cut, or add a source)` when the problem is an unsupported claim.
- **Two changes in the same sentence** become a single entry that gives the final sentence and both reasons. Two separate entries would hand the author two conflicting versions of one sentence.

Number entries continuously in the order the text appears, grouped under the draft's own section headings.

Invented example, from a draft essay about shorter work weeks that cites a fictional report by the Halden Work Institute:

**4. Share of firms, not size of gain**

**Before:** productivity rose 40% in the Halden pilot

**After:** 40% of firms in the Halden pilot reported higher productivity

**Why:** The Halden report gives the share of firms reporting any gain, not the size of the gain.

**5. Answer the coverage objection**

**Before:** (nothing; add after "most staff preferred the new schedule.")

**After:** Firms that needed daily customer coverage handled it by staggering days off across teams.

**Why:** The report's own limitations section raises coverage as the main objection, and the draft does not address it. This adds a point you did not make; check you agree.

## 6. Write the After text in the author's voice

The author will publish this under their own name, so the After text must sound like them. If they have a style guide, voice notes, or earlier writing, read it before writing any After text. Otherwise, match the draft's own sentence length, vocabulary, and tone.

Never put a belief or argument in the author's mouth. When an After adds a claim, rebuttal, or judgment that is yours and not already theirs, say so in the Why and ask them to confirm they agree.

Every link in an After must be one the author supplied or one you actually opened during this review. Never construct or recall a link from memory.

## 7. Order the reply

1. **Verdict.** One or two sentences: what works, and the two or three changes that matter most, by number.
2. **What you read.** What you read in full, what you read in part or only as a summary, and what you could not open, with links. Never imply you read everything on a topic.
3. **The entries.**
4. **Structural changes.** A short list of points that do not fit a before and after shape, such as reordering sections or making two parallel sections follow the same order. Omit this when there are none.

The entries and structural changes come last so the author can copy them in one block.

## 8. Check before sending

- Is every Before an exact match for the draft?
- Does every After read correctly when dropped into the surrounding text, including grammar at both edges?
- Does any After rely on a fact you saw only in a search summary? Check it at the source or flag it in the Why.
- Did any entry add an opinion the author did not state, without flagging it?
- Does every entry fix one of the listed problem types, rather than a style preference?

## Optional extras

- **Connected document tools.** If your assistant can read the author's document directly, use read-only access and still deliver feedback as a list. Leave comments or suggested edits in the document only if the author asks.
- **Reading log.** For long reviews, keep a simple log while researching so the "What you read" section is accurate:

| Source | How read | Used for |
| --- | --- | --- |
| [Report or article title] | [Full / partial / summary only / could not open] | [Entry numbers it supports] |

- **Large drafts.** For very long documents, review one section at a time but keep entry numbering continuous across sections, and run the parallel-section comparison once all sections are done.
- **Adjustable defaults.** The one-sentence Why, the "same length or shorter" rule for After text, and how far back to look for recent evidence are sensible defaults. Change them to suit the author and the field.

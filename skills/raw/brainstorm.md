---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a small ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not to make a long list of ideas. The goal is to identify meaningfully different paths, show the tradeoffs honestly, and leave the user with a small set of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources available in the current environment, review the minimum material needed to understand the decision.

If the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Constraints, commitments, budgets, or deadlines
- Stakeholder concerns, responsibilities, and approval boundaries
- Evidence about what has already been tried

Use targeted retrieval only when it could materially change the options. When reviewing private communications or records, have a legitimate purpose and clear authorization; use only relevant information, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

Do not search broadly by default. If important context is unavailable, state the assumption or ask a focused question rather than inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- What the user is actually deciding
- Important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should distinguish the options

The user’s wording may describe a symptom or an assumed solution rather than the actual decision. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited delivery window?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious and low-stakes, or when the user explicitly requests an immediate first pass. A wrong frame creates polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless there are genuinely fewer meaningful paths. Each option must be a fundamentally different approach, not merely a different intensity level of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes process, incentives, scope, ownership, or the framing of the problem
- At least one surprising but plausible option, such as delaying, partnering, reducing scope, observing longer, or doing nothing

Do not be contrarian merely to seem creative. A wait-or-do-nothing option is useful only when timing, learning, risk reduction, or avoiding distraction has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

- **What:** One or two sentences describing the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limitations.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option appear stronger by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, evidence strength, and stakeholder burden. Use domain-specific criteria where they matter more.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are useful for comparison, but state clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, goals, and constraints—not why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may:

- Choose an option
- Ask for more detail on one option
- Correct the framing or constraints
- Request additional options
- Combine options into a hybrid

If the user proposes a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than adding complexity. Do not begin implementation simply because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity according to consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, significant staffing decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that captures the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, implementation tasks, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before responding, verify that:

- The framing reflects the real decision rather than only the initial wording.
- The options are genuinely distinct.
- At least one plausible non-default path was considered.
- Strengths and weaknesses are candid and concrete.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than the assistant’s preferences.
- The output does not expose unnecessary private, sensitive, or unrelated information.

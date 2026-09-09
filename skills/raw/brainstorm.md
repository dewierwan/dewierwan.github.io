---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a small ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas. It is to surface meaningfully different paths, make tradeoffs clear, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources that are available in the current environment, review the sources that are most likely to change the recommendation.

When accessing private communications, internal records, or information about people, do so only for a legitimate purpose and with clear authorization. Use the minimum relevant sources and details. Do not expose unrelated personal information, sensitive details, or material outside the intended access boundary.

If the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Constraints, commitments, budgets, or deadlines
- Stakeholder concerns and ownership boundaries
- Evidence about what has already been tried

Do not search broadly by default. Use targeted retrieval only when it could materially change the option set. If important context is unavailable, state the assumption or ask a focused question rather than inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- Important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The user’s wording may describe a symptom or a proposed solution rather than the underlying decision. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip the pause only when the framing is obvious, low-stakes, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not merely a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes process, incentives, scope, timing, or the problem framing
- At least one surprising option, such as delaying, partnering, reducing scope, or doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, or avoided distraction has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

- **What:** One or two sentences explaining the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages or failure risks.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option appear better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose evaluation criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, and stakeholder burden. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but state clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may choose an option, request more detail, reject the framing, ask for additional options, or combine approaches.

If the user proposes a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge or pre-mortem before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that names the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After the decision is recorded, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The options are genuinely distinct.
- The framing reflects the actual decision rather than just the initial wording.
- Relevant context was used appropriately and within authorized access boundaries.
- Weaknesses are candid and effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than default assistant preferences.
- The response ends with a clear invitation for the user to choose, revise, compare, or combine options.

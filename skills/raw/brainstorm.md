---
name: brainstorm
description: Generate distinct options for a decision or problem, assess their tradeoffs honestly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs credible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long idea list: surface genuinely different paths, make tradeoffs clear, and preserve a small set of meaningful choices.

## 1. Gather relevant context

Start with the information supplied in the request. If the user refers to documents, discussion records, prior decisions, research, or other materials available in the current environment, review the minimum relevant material first.

When the question is not self-contained, retrieve a small number of high-value sources that could materially change the decision, such as:

- Earlier decisions and their rationale
- Constraints, commitments, deadlines, and dependencies
- Relevant stakeholder concerns and ownership boundaries
- Evidence about what has already been attempted

Use targeted retrieval rather than broad searching. Access private communications or records only for a legitimate purpose, with clear authorization, and only within the user’s appropriate access boundary. Include only information relevant to the decision; omit unrelated sensitive or personal details.

If important context is unavailable, state the assumption or ask a focused question. Do not invent facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that identifies:

- What decision the user is actually making
- Important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging options

The stated request may describe a symptom or favored solution rather than the underlying decision. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the framing is obvious and low-stakes, or when the user explicitly requests an immediate first pass. A wrong framing produces irrelevant options.

## 3. Generate distinct options

Generate five to seven options unless fewer genuinely different paths exist. Each option must represent a fundamentally different approach, not merely a different level of effort. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes process, incentives, scope, timing, or the problem framing
- At least one surprising but credible path, such as delaying, partnering, reducing scope, or deliberately doing nothing

Do not be contrarian merely to appear creative. A no-action option is useful only if observation, timing, avoided distraction, or preserving resources has real value.

Give each option a short, memorable label. For every option, provide:

| Element | What to include |
|---|---|
| **What** | One or two sentences explaining the approach. |
| **Strengths** | One or two concrete advantages. |
| **Weaknesses** | One or two concrete disadvantages, risks, or limitations. |
| **Effort** | Low, Medium, or High. |

Use specific tradeoffs. Do not soften serious drawbacks or make a preferred option look better by evaluating alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, operational burden, and stakeholder impact. Add domain-specific criteria when they matter more than these defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are informative, but state clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not why it is generally attractive.
4. Name the key assumption most likely to change the ranking, when one exists.

Do not force a single winner unless the user explicitly requests one. The purpose is to support a decision, not to make it on the user’s behalf.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may select an option, request more detail, correct the framing, ask for different options, or propose a hybrid.

If the user proposes a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

After the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. This applies to major strategic bets, public commitments, long-term obligations, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that defines the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than only the first proposed solution.
- The options are genuinely distinct.
- The conventional and surprising paths are both considered where relevant.
- Weaknesses and effort estimates are candid and plausible.
- Recommendations follow the user’s stated criteria rather than unstated assistant preferences.
- Any retrieved information was authorized, necessary, and kept within the appropriate privacy boundary.

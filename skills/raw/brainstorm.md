---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas; it is a set of meaningfully different paths with clear tradeoffs and a small number of credible recommendations.

## 1. Gather relevant context

Start with the information supplied in the request. If the user references documents, discussion records, prior decisions, research, or other sources that the current environment can legitimately access, review the minimum material needed to understand the decision.

When the question is not self-contained, retrieve only a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Constraints, commitments, budget limits, deadlines, or ownership boundaries
- Evidence of what has already been tried
- Relevant stakeholder needs or operating risks

Use targeted retrieval only when it could materially change the options. If reviewing private communications or records about people, do so only for a legitimate purpose with clear authorization; use the minimum relevant information, omit unrelated sensitive details, and keep the output within the appropriate access boundary. If needed context is unavailable, state the assumption or ask a focused question rather than inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- What decision the user is actually making
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The stated request may be a symptom or proposed solution rather than the underlying decision. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the framing is obvious, low-consequence, or the user explicitly asks for an immediate first pass. Poor framing produces irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless there are genuinely fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes process, incentives, scope, timing, or the problem framing
- At least one surprising but plausible option, such as delaying, partnering, narrowing scope, or doing nothing

Do not be contrarian merely to appear creative. A “do nothing” option is useful only when waiting, observing, or avoiding distraction is a real strategic choice.

Give every option a concise, memorable label. For each option, provide:

| Field | What to include |
|---|---|
| **What** | One or two sentences explaining the approach. |
| **Strengths** | One or two concrete advantages. |
| **Weaknesses** | One or two concrete disadvantages, risks, or limitations. |
| **Effort** | Low, Medium, or High. |

Use specific tradeoffs. Do not soften serious drawbacks or make preferred options look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, evidence strength, and stakeholder burden. Add domain-specific criteria when they matter more.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but clearly say why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may choose an option, request more detail, correct the framing, ask for additional options, or combine approaches.

If they propose a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than merely adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record with the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before responding, verify that:

- The framing reflects the real decision rather than only the user’s proposed solution.
- Options are genuinely distinct and include the obvious path where appropriate.
- At least one option explores a different framing, scope, timing, or level of commitment.
- Weaknesses are candid and effort labels are plausible.
- Recommendations follow the stated criteria and user context rather than default preferences.
- Any retrieved private information was necessary, authorized, minimized, and handled within the proper access boundary.

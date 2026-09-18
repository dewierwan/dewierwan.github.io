---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a small ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The aim is not a long list of ideas; it is a small set of meaningfully different paths, honest tradeoffs, and clear next choices.

## 1. Gather relevant context

Begin with the information the user provided. Review any documents, discussion records, research, or prior decisions that are available and relevant.

Only access private communications, records, or personal information when there is a legitimate purpose and clear authorization. Use the minimum sources and details needed for the decision. Do not include unrelated sensitive information in the output, and keep the response within the user’s access boundary.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Prior decisions and their rationale
- Constraints, commitments, deadlines, budgets, or ownership boundaries
- Evidence about earlier attempts and their results
- Relevant stakeholder needs or risks

Do not search broadly by default. If key context is unavailable, state an assumption or ask a focused question instead of inventing facts.

## 2. Frame the decision

Write a short framing of the decision, usually two to four sentences. State:

- What the user is actually deciding
- The important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should determine the choice

The user’s initial wording may describe a symptom or a proposed solution rather than the underlying decision. For example, “Should we add this feature?” may really mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly requests an immediate first pass.

**Readiness gate:** Do not generate detailed recommendations if the decision, key constraint, or success criterion remains unclear. Ask the smallest question that resolves the uncertainty.

## 3. Generate distinct options

Generate five to seven options unless fewer genuinely meaningful paths exist. Each option must be a fundamentally different approach, not a different level of investment in the same approach. Merge near-duplicates.

Where relevant, include:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes scope, timing, process, incentives, or the problem framing
- At least one surprising but credible path, such as delaying, partnering, removing scope, observing longer, or doing nothing

Do not be contrarian merely to sound creative. A “do nothing” option is useful only when waiting, avoiding distraction, or gathering evidence has real value.

Give each option a short, memorable label that makes its approach clear. For every option, provide:

| Element | What to include |
|---|---|
| **What** | One or two sentences describing the approach. |
| **Strengths** | One or two concrete advantages. |
| **Weaknesses** | One or two concrete drawbacks, risks, or limitations. |
| **Effort** | Low, Medium, or High, as a rough implementation burden. |

Use specific tradeoffs. Do not soften serious weaknesses, and do not make a preferred option appear stronger by describing alternatives unfairly.

## 4. Evaluate and recommend

Select criteria that fit the decision. Common criteria include likely impact, effort, cost, speed, risk, reversibility, strategic fit, quality, and stakeholder burden. Add domain-specific criteria where needed.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they teach something useful, but clearly explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not why it is generally attractive.
4. State the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve genuine choice.

## 5. Stop for a decision

After presenting the options and recommendations, wait for the user. They may:

- Select an option
- Ask for more detail on an option
- Correct the framing or constraints
- Request additional options
- Propose a hybrid approach

If the user proposes a hybrid, test whether its parts are compatible and whether it resolves a real tradeoff rather than merely adding complexity.

Do not begin implementation simply because one option appears promising.

## 6. Hand off with appropriate rigor

After the user chooses a path, match the next activity to the decision’s consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record covering the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choice:** After recording the decision, move to planning and execution: requirements, milestones, tasks, dependencies, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending, verify:

- The framing reflects the actual decision rather than only the initial wording.
- The options are genuinely distinct.
- The option set includes both credible defaults and at least one meaningfully different path.
- Strengths and weaknesses are concrete and candid.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than unstated assistant preferences.
- Any retrieved private context was necessary, authorized, minimized, and handled within appropriate privacy boundaries.

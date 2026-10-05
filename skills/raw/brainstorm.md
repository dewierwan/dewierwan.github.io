---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas. It is to identify genuinely different paths, make tradeoffs visible, and leave the user with a small set of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they link documents, discussion records, prior decisions, research, or other accessible sources, review only the sources relevant to the decision.

When the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Existing commitments, deadlines, budgets, or technical constraints
- Stakeholder concerns, decision ownership, and approval boundaries
- Evidence about what has already been tried

Use private communications or records only for a legitimate purpose with clear authorization. Use the minimum necessary information, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

Do not search broadly by default. If important information is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- What decision is actually being made
- Important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging options

The user may describe a symptom or a preferred solution rather than the real decision. For example, “Should we add a feature?” may actually mean, “How should we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip the pause only when the decision is obvious and low-stakes, or when the user explicitly requests an immediate first pass. Incorrect framing creates polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision genuinely has fewer meaningful paths. Each option must represent a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes the process, incentives, scope, or framing
- At least one surprising option, such as delaying, partnering, reducing scope, or deliberately doing nothing

Do not be contrarian merely to seem creative. A “do nothing” option is useful only when observation, timing, or avoiding distraction has real value.

Give every option a short, memorable label. For each option, provide:

- **What:** One or two sentences explaining the approach
- **Strengths:** One or two concrete advantages
- **Weaknesses:** One or two concrete disadvantages or failure risks
- **Effort:** Low, Medium, or High

Use specific tradeoffs. Do not soften serious drawbacks or make a preferred option look better by describing alternatives unfairly.

### Option template

| Option | What | Strengths | Weaknesses | Effort |
|---|---|---|---|---|
| [Short label] | [One- or two-sentence approach] | [Concrete advantages] | [Concrete drawbacks or risks] | [Low / Medium / High] |

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, and stakeholder burden. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when instructive, but state clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may select an option, ask for more detail, correct the framing, request additional options, or propose a hybrid.

If they propose a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once a path is selected, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge or pre-mortem before commitment. Use this for major strategic bets, public commitments, long-term obligations, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record: the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The options are genuinely distinct.
- The framing captures the actual decision rather than only the stated symptom.
- Constraints and assumptions are explicit.
- Weaknesses are candid and proportionate.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than unstated assistant preferences.
- Any use of internal or personal context was necessary, authorized, and appropriately minimized.

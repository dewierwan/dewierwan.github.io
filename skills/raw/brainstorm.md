---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a small ranked set while preserving the user’s final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not an unfiltered idea list: it is a set of meaningfully different paths, clear tradeoffs, and a short list of credible choices.

## 1. Gather relevant context

Start with the information the user provides. If they link or reference documents, discussion records, prior decisions, research, or other material that is available in the current environment, review the sources that are directly relevant.

When the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Constraints, commitments, budgets, deadlines, or dependencies
- Concerns from relevant stakeholders and ownership boundaries
- Evidence about attempts already made and their results

Use only sources that the user is authorized to access and share for this purpose. Review the minimum necessary information; omit unrelated personal or sensitive details from the response. Do not search broadly by default. If a key fact is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that identifies:

- What the user is actually deciding
- The important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging options

The stated request may describe a symptom or a preferred solution rather than the underlying decision. For example, “Should we add a feature?” may actually mean, “How can we reduce a recurring user problem within a limited delivery window?”

Ask the user to confirm or correct the framing before generating a substantial option set. You may skip this pause when the decision is obvious and low-stakes, or when the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision truly has fewer meaningful paths. Each option must represent a fundamentally different approach, not merely a different level of investment in the same approach. Merge near-duplicates.

Where relevant, include:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes the process, incentives, scope, or framing of the problem
- At least one surprising but plausible option, such as delaying, partnering, narrowing scope, observing longer, or doing nothing

Do not be contrarian merely to seem creative. A “do nothing” option is useful only when waiting, learning, timing, or avoiding distraction has genuine value.

Give each option a short, memorable label that communicates its core approach. For every option, provide:

- **What:** One or two sentences explaining the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limits.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a favored option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Select criteria that fit the decision. Common criteria include likely impact, effort, cost, speed, risk, reversibility, strategic fit, operational burden, and stakeholder effects. Add domain-specific criteria where they matter more than generic ones.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but state plainly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not merely why it is attractive in general.
4. Name the key assumption most likely to change the ranking, if there is one.

Do not force a single winner unless the user explicitly asks for one. Preserve genuine choice when multiple paths remain viable.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may:

- Select an option
- Request more detail on an option
- Correct the framing or constraints
- Ask for additional options
- Combine elements of multiple options

If the user proposes a hybrid, check whether its components are compatible and whether the combination resolves a real tradeoff rather than simply adding complexity. Do not start implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record: the choice, accountable owner, rationale, assumptions, constraints, and review point.
- **Build-oriented choice:** After recording the decision, move to planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, challenge consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the real decision rather than only the requested solution.
- The options are genuinely distinct.
- The conventional option and a plausible alternative framing have both been considered where relevant.
- Weaknesses are candid and concrete.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than unstated assistant preferences.
- Any retrieved context was used with legitimate purpose, appropriate authorization, and minimal disclosure.

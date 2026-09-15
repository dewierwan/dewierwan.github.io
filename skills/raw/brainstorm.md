---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when a user needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not to produce a long idea list; it is to identify meaningfully different paths, explain their tradeoffs honestly, and leave the user with two or three credible choices.

## 1. Gather relevant context

Start with the information the user provided. If they reference documents, discussions, prior decisions, research, or records that are available in the current environment, review the minimum relevant material first.

When accessing internal or personal communications, records, or documents about people, do so only for a legitimate decision-related purpose and with clear authorization. Use only relevant sources, omit unrelated sensitive details, and keep the output within the user’s appropriate access boundary.

If the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, deadlines, and ownership boundaries
- Evidence about what has already been tried
- Relevant stakeholder needs or operational risks

Do not search broadly by default. Use targeted retrieval only when it could materially change the options. If important information is unavailable, state an assumption or ask a focused question rather than inventing context.

## 2. Frame the decision

Write a two-to-four sentence framing that states:

- What the user is actually deciding
- The important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should determine the choice

The user’s wording may describe a symptom or a proposed solution rather than the underlying decision. For example, “Should we add a feature?” may really mean, “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the framing is obvious, low-stakes, or the user explicitly asks for an immediate first pass.

### Framing template

> **Decision:** [What must be chosen or resolved?]
>
> **Constraints:** [Budget, timing, capabilities, commitments, risk limits, or other non-negotiables.]
>
> **Success criteria:** [What outcomes matter most, and how will options be judged?]
>
> **Key uncertainty:** [The assumption most likely to affect the choice, if known.]

## 3. Generate distinct options

Generate five to seven options unless the decision naturally has fewer meaningful paths. An option must be a fundamentally different approach, not merely a different intensity level of the same idea. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes process, incentives, scope, timing, or the framing of the problem
- At least one surprising but credible option, such as delaying, partnering, reducing scope, running an experiment, or deliberately doing nothing

Do not be contrarian merely to appear creative. A “do nothing” option is useful only when waiting, observation, timing, or avoiding distraction has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

| Element | Include |
|---|---|
| **What** | One or two sentences describing the approach and its mechanism. |
| **Strengths** | One or two concrete advantages tied to the decision criteria. |
| **Weaknesses** | One or two concrete disadvantages, constraints, or failure risks. Do not soften serious drawbacks. |
| **Effort** | Low, Medium, or High, using a rough estimate of work, coordination, and time. |

## 4. Evaluate and recommend

Choose evaluation criteria that fit the decision. Common criteria include expected impact, effort, cost, speed, risk, reversibility, strategic fit, evidence quality, and stakeholder burden. Add domain-specific criteria when they matter more than these defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when instructive, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this user’s specific goals, constraints, and context—not merely why it is generally attractive.
4. State the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice.

### Recommendation template

| Rank | Option | Why it fits | Watch condition |
|---|---|---|---|
| 1 | [Option label] | [Situation-specific reason.] | [Assumption or trigger that could change the choice.] |

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may:

- Select an option
- Ask for more detail on a specific option
- Correct the framing or constraints
- Request additional options
- Combine options into a hybrid

For a hybrid, test whether its components are compatible and whether it resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record that identifies the choice, decision owner, rationale, assumptions, and review point.
- **Build-oriented choice:** After the decision is recorded, move to planning and execution: requirements, milestones, tasks, ownership, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Readiness gates

Do not finalize recommendations until these conditions are met:

- The decision, constraints, and success criteria are clear enough to distinguish options.
- The options are genuinely different rather than cosmetic variations.
- At least one option challenges the default framing when that could be valuable.
- Weaknesses are candid and comparable across options.
- Recommendations follow the user’s criteria rather than the assistant’s preferences.

If these conditions are not met, ask one or two focused questions or provide a clearly labeled provisional first pass.

## Quality audit and common failure modes

Before sending, check for the following:

- **Idea-list failure:** Many suggestions are listed without decisions or tradeoffs. Remedy: consolidate into distinct approaches and evaluate each.
- **False variety:** Options differ only in scale or wording. Remedy: merge them and seek a different mechanism, timing, scope, or ownership model.
- **Premature solutioning:** The options answer the stated request but not the underlying decision. Remedy: return to the framing.
- **Biased evaluation:** A preferred option receives richer strengths while alternatives receive vague criticism. Remedy: apply the same level of specificity to every option.
- **Unfounded certainty:** Missing context is treated as fact. Remedy: state assumptions and identify what would change the ranking.
- **Forced commitment:** One winner is declared when meaningful tradeoffs remain. Remedy: recommend a ranked set unless the user asks for a single choice.
- **Premature execution:** Planning begins before the user selects a path. Remedy: stop after recommendations and wait for direction.

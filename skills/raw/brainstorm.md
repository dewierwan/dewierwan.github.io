---
name: brainstorm
description: Generate genuinely distinct options for a decision, weigh their tradeoffs honestly, and recommend a short ranked set. Use when someone asks for options, alternatives, or ways they could approach something.
---

# Brainstorm options

Use this workflow when someone needs credible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas. It is to surface genuinely different paths, show their tradeoffs clearly, and leave the user with a small set of meaningful choices.

## 1. Gather relevant context

Begin with the information the user supplied. If they provide links, documents, discussion records, prior decisions, research, or other accessible materials, review only the sources relevant to the decision.

If the question is not self-contained, retrieve a small number of high-value sources that may materially change the options, such as:

- Earlier decisions and the reasons behind them
- Existing commitments, deadlines, budget limits, or technical constraints
- Evidence about what has already been tried
- Relevant stakeholder needs, ownership boundaries, or approval requirements

Use private communications or records only for a legitimate purpose and with clear authorization. Use the minimum relevant information, omit unrelated personal or sensitive details, and keep the output within the appropriate access boundary.

Do not search broadly by default. If key information is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- What the user is actually deciding
- Important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should distinguish options

The stated request may describe a symptom or a preferred solution rather than the underlying choice. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited budget and timeline?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly requests an immediate first pass. A wrong framing produces irrelevant options.

## 3. Generate distinct options

Generate five to seven options unless there are genuinely fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes the process, incentives, scope, or framing
- At least one surprising but credible path, such as delaying, partnering, narrowing scope, observing longer, or doing nothing

Do not be contrarian merely to appear creative. A “do nothing” option is useful only when waiting, learning, timing, or avoiding distraction has real value.

Give every option a short, memorable label that makes its approach clear. For each option, provide:

- **What:** One or two sentences describing the approach
- **Strengths:** One or two concrete advantages
- **Weaknesses:** One or two concrete disadvantages, constraints, or failure risks
- **Effort:** Low, Medium, or High

Be candid. Do not soften serious drawbacks or describe alternatives unfairly to favor a preferred option.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include expected impact, cost, effort, speed, risk, reversibility, strategic fit, confidence in evidence, and burden on affected people. Add domain-specific criteria when they matter more.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are instructive, but clearly explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, state in one sentence why it fits this situation, constraints, and goals—not merely why it is attractive in general.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the options and recommendations, wait for the user. They may:

- Choose an option
- Request more detail on one option
- Correct the framing or constraints
- Ask for additional options
- Propose a hybrid approach

For a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or hard-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term obligations, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that states the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move to planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The decision framing reflects the real choice rather than only the requested solution
- The options are genuinely distinct
- The obvious option and a credible alternative framing were considered
- Weaknesses and effort labels are plausible and candid
- Recommendations follow the user’s stated criteria and constraints
- Uncertainty, missing evidence, and assumptions are visible
- The output does not make an implementation commitment before the user chooses

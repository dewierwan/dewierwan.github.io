---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs honestly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when a user needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not to produce a long idea list. It is to surface genuinely different paths, make their tradeoffs clear, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources that are available in the current environment, review the relevant material first.

When accessing private communications, records, or information about people, do so only for a legitimate purpose and with clear authorization. Use the minimum sources and details needed for the decision. Do not expose unrelated personal, confidential, or sensitive information in the output; keep findings within the appropriate access boundary.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, deadlines, and ownership boundaries
- Stakeholder concerns or operational dependencies
- Evidence about what has already been tried

Do not search broadly by default. If important context is unavailable, state the assumption or ask a focused question rather than inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- Important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging options

The user’s wording may describe a symptom or a proposed solution rather than the real decision. For example, “Should we add a feature?” may actually mean, “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same idea. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes process, incentives, scope, or the framing of the problem
- At least one surprising but credible option, such as delaying, partnering, narrowing scope, or intentionally doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, avoided cost, or reduced distraction has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

- **What:** One or two sentences explaining the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages or failure risks.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, stakeholder burden, and evidence strength. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not merely why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may:

- Choose an option
- Request more detail on a specific option
- Reject or revise the framing
- Ask for additional options
- Combine approaches into a hybrid

If the user proposes a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that states the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than only the user’s first proposed solution.
- Options are genuinely distinct and not variations in scale.
- At least one credible non-default path was considered.
- Weaknesses are candid, concrete, and proportionate.
- Effort labels are plausible.
- Recommendations follow the stated criteria and constraints rather than default assistant preferences.
- Any retrieved private context was authorized, minimized, and represented without unnecessary personal or sensitive detail.

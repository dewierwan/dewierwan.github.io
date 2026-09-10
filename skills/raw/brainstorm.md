---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when a user needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas; it is to surface genuinely different paths, make tradeoffs clear, and leave the user with a small set of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources accessible in the current environment, review them when they are likely to affect the answer.

When accessing non-public communications or records, confirm there is a legitimate purpose and clear authorization. Use only the minimum relevant sources and information, omit unrelated or sensitive personal details, and keep the output within the appropriate access boundary.

If the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, budgets, or deadlines
- Stakeholder concerns, responsibilities, and approval boundaries
- Evidence about what has already been tried

Do not search broadly by default. Use targeted retrieval only when it could materially change the options. If important context is unavailable, state an assumption or ask a focused question instead of inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The user’s wording may describe a symptom or a preferred solution rather than the real decision. For example, “Should we add a feature?” may really mean, “How should we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip the pause only when the framing is obvious, the choice is low-stakes, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes the process, incentives, scope, or problem framing
- At least one surprising option, such as delaying, partnering, removing scope, or doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, or avoided distraction has genuine value.

Give every option a short, memorable label that communicates its core approach. For each, provide:

| Element | Include |
|---|---|
| What | One or two sentences explaining the approach. |
| Strengths | One or two concrete advantages. |
| Weaknesses | One or two concrete disadvantages, constraints, or failure risks. |
| Effort | Low, Medium, or High. |

Use specific tradeoffs. Do not soften serious drawbacks or make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, and stakeholder burden. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not why it is generally attractive.
4. Name the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may choose an option, request more detail, reject the framing, ask for new options, or combine approaches.

If the user proposes a hybrid, test whether the components are compatible and whether combining them resolves a real tradeoff rather than adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record: define the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After the decision is recorded, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Avoid skipping the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than only the stated symptom or solution.
- The options are genuinely distinct and not variations in scale.
- At least one option challenges the default framing when that could be useful.
- Strengths and weaknesses are candid, concrete, and comparably detailed.
- Effort labels are plausible.
- Recommendations follow the user’s criteria and constraints rather than unstated assistant preferences.
- Sensitive or private context, if used, was authorized, minimized, and not exposed unnecessarily.

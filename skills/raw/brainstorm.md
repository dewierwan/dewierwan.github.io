---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a small ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas; it is a set of meaningfully different paths, clear tradeoffs, and two or three credible choices to consider.

## 1. Gather relevant context

Start with the information provided in the request. Review any documents, discussion records, prior decisions, research, or links that are available within the current environment and relevant to the decision.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the answer, such as:

- Earlier decisions and their rationale
- Constraints, commitments, budget limits, deadlines, or dependencies
- Stakeholder concerns, ownership boundaries, and decision authority
- Evidence about what has already been tried and what happened

Use targeted retrieval rather than broad searching. If reviewing private communications or records about people, do so only for a legitimate purpose with clear authorization. Use the minimum relevant sources and details, omit unrelated sensitive information, and keep the output within the appropriate access boundary.

If material information is unavailable, state the assumption or ask a focused question. Do not invent context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that identifies:

- What decision is actually being made
- Important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should be used to compare options

The stated request may describe a symptom or a proposed solution rather than the underlying decision. For example, “Should we add a feature?” may really mean “How should we reduce a recurring user problem within a limited budget and timeline?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly asks for an immediate first pass. A wrong framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must represent a fundamentally different approach, not merely a different intensity level of the same approach. Merge near-duplicates.

Where relevant, include:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes scope, process, incentives, timing, or the framing of the problem
- At least one surprising but credible path, such as delaying, partnering, reducing scope, observing longer, or doing nothing

Do not be contrarian merely to appear creative. A “do nothing” option is useful only when waiting, learning, preserving focus, or avoiding a bad commitment has real value.

Give each option a short, memorable label that makes the approach clear. For every option, provide:

| Element | Include |
|---|---|
| What | One or two sentences describing the approach. |
| Strengths | One or two concrete advantages. |
| Weaknesses | One or two concrete disadvantages, risks, or limitations. |
| Effort | Low, Medium, or High. |

Use concrete tradeoffs. Do not soften serious weaknesses, and do not make a preferred option appear stronger by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, stakeholder burden, and confidence in the evidence. Add domain-specific criteria where needed.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are informative, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not merely why it is attractive in general.
4. Name the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless explicitly asked. Preserve meaningful choice when more than one option is viable.

## 5. Stop for a decision

After presenting the options and recommendations, wait for the user. They may:

- Select an option
- Ask for more detail on one option
- Correct the framing or constraints
- Request additional options
- Propose a hybrid approach

If the user proposes a hybrid, check whether the components are compatible and whether combining them resolves a real tradeoff rather than adding unnecessary complexity.

Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once a path is selected, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that captures the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, implementation tasks, owners, and validation measures.

A useful sequence is: brainstorm options, challenge consequential choices, make the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The options are genuinely distinct rather than variations of one approach.
- The framing reflects the actual decision, not just the first proposed solution.
- The obvious option is included when relevant.
- At least one non-obvious but credible alternative was considered.
- Weaknesses are candid and specific.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria and constraints rather than default preferences.
- The response does not expose unnecessary private, sensitive, or unrelated information.

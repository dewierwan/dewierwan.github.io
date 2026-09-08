---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and present a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas; it is a set of meaningfully different paths, clear tradeoffs, and two or three credible choices.

## 1. Gather relevant context

Start with information the user has provided. Review linked documents, discussion records, prior decisions, research, or other sources only if you have legitimate access and they are relevant to the decision.

When the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Current constraints, commitments, budgets, or deadlines
- Stakeholder concerns, decision ownership, and access boundaries
- Evidence from previous attempts or experiments

Use targeted retrieval rather than broad searching. If records include personal or sensitive information, use only the minimum relevant information, omit unrelated details, and respect consent, confidentiality, and the user’s authorized access level. If key context is unavailable, state the assumption or ask a focused question; do not invent facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- The decision the user is actually making
- Important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging options

The stated request may describe a symptom or a preferred solution rather than the underlying choice. For example, “Should we add a feature?” may really mean, “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip the pause only when the framing is obvious and low-stakes, or when the user explicitly requests an immediate first pass. A wrong frame produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision genuinely has fewer meaningful paths. Options must represent fundamentally different approaches, not different intensity levels of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes process, incentives, scope, ownership, or the framing of the problem
- At least one surprising but plausible option, such as delaying, partnering, narrowing scope, or deliberately doing nothing

Do not be contrarian just to seem creative. A “do nothing” option is useful only when observation, timing, avoided distraction, or preservation of resources is a real strategic choice.

Give each option a short, memorable label that makes its approach clear. For every option, provide:

- **What:** One or two sentences describing the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limits.
- **Effort:** Low, Medium, or High.

Use specific and comparable tradeoffs. Do not soften serious drawbacks or make a preferred option look better by evaluating alternatives unfairly.

### Option template

| Option | What | Strengths | Weaknesses | Effort |
|---|---|---|---|---|
| [Short, clear label] | [One or two sentence approach.] | [Concrete benefits.] | [Concrete risks or costs.] | [Low / Medium / High] |

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic alignment, operational burden, and stakeholder impact. Add domain-specific criteria when they matter more than generic defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are informative, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not merely why it is attractive in general.
4. State the key assumption most likely to change the ranking, if there is one.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

### Recommendation format

| Rank | Option | Why it fits | Key condition or assumption |
|---|---|---|---|
| 1 | [Option label] | [Situation-specific reason.] | [What could change the ranking.] |

## 5. Stop for a decision

After presenting the options and recommendations, wait for the user. They may:

- Choose an option
- Request more detail on one option
- Correct the framing or constraints
- Ask for additional options
- Combine options into a hybrid

If the user proposes a hybrid, test whether its components are compatible and whether the combination resolves a real tradeoff rather than adding complexity and cost.

Do not start implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user chooses a path, select the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing decisions, or choices with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record that states the choice, decision owner, rationale, assumptions, and a review point.
- **Build-oriented choice:** After the decision is recorded, move to planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision, not just the first solution mentioned.
- Options are genuinely distinct and not degree variations.
- At least one conventional option and one non-obvious but plausible option are considered where relevant.
- Strengths and weaknesses are candid, concrete, and comparably described.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than the assistant’s default preferences.
- Any retrieved context was authorized, relevant, and handled within appropriate privacy and access boundaries.
- The response ends with a clear invitation for the user to choose, refine, reject, or combine options.

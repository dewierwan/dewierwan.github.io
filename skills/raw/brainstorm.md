---
name: brainstorm
description: Generate distinct options for a decision or problem, assess their tradeoffs honestly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long idea list: surface genuinely different paths, state their tradeoffs plainly, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they refer to documents, discussion threads, prior decisions, research, or other records available in the current environment, review only the sources needed to understand the decision.

When accessing non-public communications or records, do so only for a legitimate purpose with clear authorization. Use the minimum relevant information, omit unrelated personal or sensitive details, and keep the response within the appropriate access boundary.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Constraints, commitments, deadlines, or available resources
- Relevant stakeholder concerns and decision ownership
- Evidence about prior attempts, results, or risks

Do not search broadly by default. If a material fact is unavailable, state the assumption or ask a focused question instead of inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- What the user is actually deciding
- Important constraints and non-negotiables
- What a good outcome looks like and the criteria for judging it

The stated request may describe a symptom or preferred solution rather than the underlying decision. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Options must be fundamentally different approaches, not different intensity levels of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes process, incentives, scope, timing, or problem framing
- At least one surprising but plausible path, such as delaying, partnering, reducing scope, or doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, or avoided distraction has real value.

Give each option a short, memorable label that communicates its core approach. Use this format:

| Option | What | Strengths | Weaknesses | Effort |
|---|---|---|---|---|
| [Short label] | [One or two sentences describing the approach.] | [One or two concrete advantages.] | [One or two concrete disadvantages or failure risks.] | [Low / Medium / High] |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, evidence strength, and stakeholder burden. Add domain-specific criteria where needed.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are instructive, but clearly state why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not merely why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may:

- Pick an option
- Ask for more detail on a specific option
- Correct the framing or challenge the options
- Request additional alternatives
- Combine options into a hybrid

If the user proposes a hybrid, check whether its components are compatible and whether the combination resolves a real tradeoff rather than merely adding complexity. Do not start implementation simply because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that captures the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move to planning and execution: requirements, milestones, tasks, ownership, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before responding, verify that:

- The framing reflects the actual decision rather than only the requested solution.
- The options are truly distinct and not variations in degree.
- The set includes the conventional path and a meaningfully different alternative where appropriate.
- Strengths and weaknesses are concrete, balanced, and candid.
- Effort labels are plausible for the user’s context.
- Recommendations follow the stated criteria and constraints rather than default assistant preferences.
- The response does not expose unnecessary private, sensitive, or unrelated information.

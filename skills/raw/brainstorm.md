---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas. It is to identify meaningfully different paths, make tradeoffs visible, and leave the user with a few credible choices.

## 1. Gather relevant context

Start with the information the user provided. If they reference documents, discussion threads, research, prior decisions, or other accessible sources, review only the sources needed to understand the decision.

When the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Constraints, commitments, deadlines, budget limits, or technical boundaries
- What has already been tried and what happened
- Stakeholder needs, ownership boundaries, and approval requirements
- Evidence about expected outcomes or risks

Use targeted retrieval rather than broad searching. If reviewing private communications or records, do so only for a legitimate purpose with clear authorization. Use the minimum relevant information, omit unrelated or sensitive personal details, and keep the output within the appropriate access boundary.

If material information is unavailable, state the assumption or ask a focused question. Do not invent context.

## 2. Frame the decision

Before generating a substantial option set, write a short framing of two to four sentences that states:

- What the user is actually deciding
- Important constraints and non-negotiables
- What a good outcome looks like
- The criteria that should determine the choice

The initial wording may describe a symptom or preferred solution rather than the underlying decision. For example, “Should we add a feature?” may actually mean “How can we reduce a recurring user problem within a limited budget and timeline?”

Ask the user to confirm or correct the framing before continuing. Skip this pause only when the decision is obvious and low-stakes, or when the user explicitly requests an immediate first pass. Incorrect framing produces irrelevant options.

## 3. Generate distinct options

Generate five to seven options unless the situation naturally has fewer meaningful paths. Each option must represent a fundamentally different approach, not a different amount of the same activity. Merge near-duplicates.

Where relevant, include:

- The obvious or conventional approach
- A lower-effort, incremental approach
- A more ambitious approach
- An approach that changes scope, process, incentives, timing, or ownership
- At least one surprising but plausible option, such as delaying, partnering, narrowing the problem, removing scope, or intentionally doing nothing

Do not be contrarian merely to seem creative. A “do nothing” option is useful only when waiting, observing, or avoiding distraction is a genuine strategic choice.

Give each option a short, memorable label that makes its approach clear. For each option, provide:

- **What:** One or two sentences describing the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limitations.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not soften serious weaknesses, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, stakeholder burden, operational complexity, and confidence in the evidence. Add domain-specific criteria when they matter more.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are instructive, but clearly explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, give one sentence explaining why it fits this situation, its constraints, and its goals—not merely why it is generally attractive.
4. Name the key assumption most likely to change the ranking, if there is one.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice when multiple paths are viable.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may:

- Select an option
- Ask for more detail on an option
- Correct the framing or constraints
- Request additional options
- Combine compatible options into a hybrid

If the user proposes a hybrid, test whether its components are compatible and whether the combination resolves a real tradeoff rather than adding unnecessary complexity.

Do not begin implementation just because an option appears promising.

## 6. Hand off with appropriate rigor

Once the user selects a path, choose the next activity according to consequence and reversibility:

- **High-consequence or hard-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record with the choice, owner, rationale, assumptions, boundaries, and review point.
- **Build-oriented choices:** After the decision is recorded, move to planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before responding, verify that:

- The framing describes the actual decision rather than only the requested solution.
- The options are genuinely distinct.
- The obvious option and a plausible non-obvious option are represented when relevant.
- Strengths and weaknesses are concrete and candid.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than unstated assistant preferences.
- The response does not prematurely turn a choice into an implementation plan.
- Any use of sensitive or private context was authorized, minimal, and relevant to the decision.

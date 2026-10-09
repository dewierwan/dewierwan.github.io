---
name: brainstorm
description: Generate distinct options for a decision, assess their tradeoffs honestly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs credible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas; it is a small set of genuinely different paths with candid tradeoffs and a clear basis for choosing.

## 1. Gather relevant context

Start with the information provided in the request. If the user links documents, prior decisions, research, discussion records, or other materials that are available in the current environment, review the minimum sources needed to understand the decision.

When the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Previous decisions and their rationale
- Existing commitments, deadlines, budgets, and technical constraints
- Evidence about attempts already made and their results
- Relevant stakeholder needs, ownership boundaries, or risks

Access private communications or records only for a legitimate purpose and with clear authorization. Use only relevant information, omit unrelated sensitive details, and keep the output within the appropriate access boundary.

Do not search broadly by default. If essential context is unavailable, state the assumption or ask a focused question instead of inventing facts.

## 2. Frame the decision

Before generating a substantial option set, write a short framing of two to four sentences that states:

- What decision is actually being made
- The key constraints and non-negotiables
- What a good outcome looks like
- The criteria that should determine the choice

The stated question may describe a symptom or a proposed solution rather than the real decision. For example, “Should we add this feature?” may actually mean “What is the lowest-risk way to reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before continuing. Skip this pause only when the decision is obvious and low-stakes, or when the user explicitly requests an immediate first pass. Bad framing creates polished but irrelevant options.

## 3. Generate distinct options

Generate five to seven options unless the decision naturally contains fewer meaningful paths. Each option must be a fundamentally different approach, not a variation in scale or intensity. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes scope, incentives, process, timing, or framing
- At least one surprising but plausible option, such as delaying, partnering, reducing scope, or deliberately doing nothing

Do not be contrarian merely to seem creative. A “do nothing” option is useful only when waiting, observing, or avoiding distraction is a real strategic choice.

Give each option a brief, memorable label that communicates its core idea. For every option, provide:

- **What:** One or two sentences explaining the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limits.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not hide serious drawbacks or make a preferred option look better by evaluating alternatives unfairly.

## 4. Evaluate and recommend

Select criteria that fit the decision. Common criteria include likely impact, effort, cost, speed, reversibility, strategic fit, risk, stakeholder burden, and confidence in the evidence. Add domain-specific criteria when they matter more.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but clearly explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not merely why it is generally attractive.
4. State the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user asks for one. Preserve real choices when the evidence does not justify false certainty.

## 5. Stop for a decision

After presenting the options and recommendations, wait for the user. They may:

- Pick an option
- Ask for more detail on one option
- Correct the framing or constraints
- Request additional options
- Propose a hybrid approach

For a hybrid, check whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity. Do not begin implementation merely because an option seems promising.

## 6. Hand off with appropriate rigor

Once a path is selected, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge or pre-mortem before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record with the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choice:** After recording the decision, create an execution plan covering requirements, milestones, tasks, dependencies, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than a superficial request.
- Options are meaningfully distinct.
- The obvious option and at least one non-obvious option were considered where relevant.
- Strengths and weaknesses are concrete and candid.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria and constraints.
- Any retrieved private information was necessary, authorized, minimized, and handled within the proper access boundary.

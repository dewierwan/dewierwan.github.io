---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs credible approaches to a decision, problem, or opportunity but is not ready to commit. The aim is not a long list of ideas. It is to identify meaningfully different paths, make their tradeoffs visible, and preserve a small number of real choices.

## 1. Gather relevant context

Start with the information provided in the request. If the user refers to documents, discussion records, prior decisions, research, or other accessible sources, review only the sources that are likely to affect the decision.

When accessing private communications, records, or information about people, do so only for a legitimate purpose with clear authorization. Use the minimum relevant sources and details, omit unrelated sensitive information, respect consent and expected privacy, and keep the output within the user’s authorized access boundary.

If the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Constraints, commitments, deadlines, and budget limits
- Evidence about what has already been tried
- Stakeholder needs, ownership boundaries, and implementation dependencies

Do not search broadly by default. Use targeted retrieval only when it could materially change the option set or recommendation. If necessary context is unavailable, state the assumption or ask a focused question rather than inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, covering:

- The decision the user is actually making
- Important constraints and non-negotiables
- What a good outcome looks like
- The criteria by which options should be judged

The stated request may describe a symptom or a preferred solution rather than the underlying decision. For example, “Should we add a feature?” may actually mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the decision is obvious and low-stakes, or when the user explicitly requests an immediate first pass. Incorrect framing leads to polished but irrelevant options.

## 3. Generate a distinct option set

Generate five to seven options unless the situation genuinely has fewer meaningful paths. Each option must represent a fundamentally different approach, not merely a different intensity of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes scope, process, incentives, timing, or the problem framing
- At least one surprising but credible option, such as delaying, partnering, reducing scope, testing an assumption, or doing nothing

Do not be contrarian for its own sake. A “do nothing” option is useful only when observation, timing, or avoiding distraction is a meaningful strategic choice.

Give each option a short, memorable label that communicates its core approach. For every option, provide:

- **What:** One or two sentences describing the approach
- **Strengths:** One or two concrete advantages
- **Weaknesses:** One or two concrete drawbacks, risks, or likely failure modes
- **Effort:** Low, Medium, or High

Use specific tradeoffs. Do not soften serious weaknesses, and do not make a preferred option appear stronger by treating alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, operational burden, and stakeholder impact. Add domain-specific criteria where they matter more than generic ones.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are instructive, but state clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not merely why it is attractive in general.
4. State the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. The result should leave the user with meaningful choice.

## 5. Stop for a decision

After presenting the options and recommendations, wait for the user. They may:

- Select an option
- Ask for more detail on one option
- Correct the framing or constraints
- Request additional options
- Propose a hybrid approach

If the user proposes a hybrid, check whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity.

Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once a path is selected, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or risk review before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record with the choice, owner, rationale, assumptions, constraints, and review point.
- **Build-oriented choices:** After recording the decision, move into planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The decision framing reflects the underlying choice rather than only the user’s initial wording.
- Options are genuinely distinct and not minor variations.
- At least one non-obvious path was considered where appropriate.
- Strengths and weaknesses are concrete and candid.
- Effort labels are plausible.
- Recommendations follow the user’s criteria and constraints rather than default preferences.
- The response does not expose unnecessary private, personal, or sensitive information.

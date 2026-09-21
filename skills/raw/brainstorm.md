---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when a user needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long idea list; it is a small set of genuinely different paths, clear tradeoffs, and recommendations that preserve meaningful choice.

## 1. Gather relevant context

Start with the information supplied in the request. Review linked documents, prior decisions, research, discussion records, or other materials only when they are relevant and you have a legitimate purpose and clear authorization to access them.

Before accessing private communications, personnel records, customer information, or other sensitive material, confirm:

- **Purpose:** The information is necessary to help with the stated decision, not merely available.
- **Authorization:** The user is entitled to access and use the source for this purpose, and any required consent or notice has been obtained.
- **Minimum necessary scope:** Retrieve only the smallest set of sources, date ranges, people, and details likely to affect the decision.
- **Sensitive-data handling:** Avoid collecting or repeating unrelated personal, health, financial, demographic, security, or confidential details. Use generalized or aggregated observations where possible.
- **Output boundary:** Share conclusions only with the intended audience and at the same or a narrower access level than the underlying material. Do not expose source excerpts, identities, or sensitive details unless necessary and authorized.

When the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Constraints, commitments, deadlines, and available resources
- Stakeholder concerns, decision ownership, and affected groups
- Evidence about attempts already made and their results

Use targeted retrieval rather than broad searching. If consent, authorization, or the intended use is unclear, ask a focused question or proceed only from non-sensitive information the user has provided. If important context is unavailable, state the assumption rather than inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision is actually being made
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The stated request may describe a symptom or proposed solution rather than the underlying decision. For example, “Should we add a feature?” may really mean, “How should we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, low-consequence, or the user explicitly requests an immediate first pass. A mistaken framing produces irrelevant options.

## 3. Generate a distinct option set

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not merely a different intensity level of the same idea. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes process, incentives, scope, timing, or the problem framing
- At least one surprising but credible option, such as delaying, partnering, reducing scope, observing longer, or doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when waiting, observation, timing, or avoided distraction has real value.

Give each option a short, memorable label that makes its core approach clear. For every option, provide:

| Element | Include |
|---|---|
| What | One or two sentences explaining the approach. |
| Strengths | One or two concrete advantages. |
| Weaknesses | One or two concrete disadvantages, risks, or limitations. |
| Effort | Low, Medium, or High. |

Use specific tradeoffs. Do not soften serious drawbacks or make a preferred option appear stronger by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose criteria that fit the decision. Common criteria include expected impact, effort, cost, risk, speed, reversibility, strategic fit, operational burden, and stakeholder effects. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when instructive, but clearly explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not merely why it is generally attractive.
4. Name the assumption most likely to change the ranking, if one exists.
5. If evidence depends on sensitive or incomplete information, state that limitation without revealing unnecessary details, and identify what authorized evidence would reduce uncertainty.

Do not force a single winner unless the user explicitly requests one. If evidence is weak, say what would need to be learned before choosing.

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may:

- Choose an option
- Request more detail on an option
- Correct the framing or constraints
- Ask for additional options
- Propose a hybrid approach

For a hybrid, test whether its components are compatible and whether it resolves a real tradeoff rather than adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once a path is selected, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term obligations, major staffing decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that names the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After recording the decision, move to planning and execution: requirements, milestones, tasks, dependencies, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing reflects the actual decision rather than only the initial wording.
- Options are genuinely distinct and include plausible alternatives, not artificial variety.
- Strengths and weaknesses are candid, concrete, and applied consistently.
- Effort labels are plausible for the available resources and timeline.
- Recommendations follow the user’s stated criteria rather than default preferences.
- Uncertain assumptions, missing evidence, and access limitations are clearly identified.
- Any private or sensitive information used was necessary for the stated purpose, accessed with clear authorization and any required consent, minimized to relevant details, and presented only within the appropriate output-access boundary.

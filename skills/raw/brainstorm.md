---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a small ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The aim is not a long list of ideas; it is a set of meaningfully different paths, clear tradeoffs, and a small number of credible choices.

## 1. Gather relevant context

Start with the information supplied in the request. If the requester provides links, documents, discussion records, prior decisions, research, or other materials that you are authorized to access, review the minimum relevant material first.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the recommendation, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, deadlines, and budgets
- Stakeholder responsibilities and concerns
- Evidence about prior attempts, outcomes, or risks

Use targeted retrieval, not broad searching. Access private communications or records only for a legitimate purpose and with clear authorization. Include only information relevant to the decision; omit unrelated personal or sensitive details. If important context is unavailable, state the assumption or ask a focused question rather than inventing facts.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the requester is actually making
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The initial wording may name a symptom or preferred solution rather than the real choice. For example, “Should we add a feature?” may actually mean “How can we reduce a recurring user problem within a limited budget?”

Ask the requester to confirm or correct the framing before generating a substantial option set. You may skip the pause when the framing is obvious, low-stakes, or the requester explicitly asks for an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not merely a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes process, incentives, scope, timing, or the problem framing
- At least one surprising option, such as delaying, partnering, reducing scope, observing longer, or doing nothing

Do not be contrarian merely to appear creative. A “do nothing” option is useful only when waiting, learning, or avoiding distraction is a real strategic choice.

Give every option a short, memorable label that communicates its core approach. Use this format:

| Option | What | Strengths | Weaknesses | Effort |
|---|---|---|---|---|
| **[Clear option label]** | [One or two sentences describing the approach.] | [One or two concrete advantages.] | [One or two candid disadvantages or failure risks.] | Low / Medium / High |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose evaluation criteria that fit the decision. Common criteria include likely impact, cost, effort, speed, risk, reversibility, strategic fit, operational burden, and stakeholder impact. Add domain-specific criteria when they matter more than these defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they teach something useful, but clearly state why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, its constraints, and its goals—not why it is generally attractive.
4. State the assumption most likely to change the ranking, if there is one.

Do not force a single winner unless the requester explicitly asks for one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting the options and recommendations, wait for the requester. They may select an option, ask for detail, correct the framing, request additional options, or combine approaches.

If they propose a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with appropriate rigor

Once a path is selected, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record with the choice, decision owner, rationale, assumptions, boundaries, and review point.
- **Build-oriented choice:** After recording the decision, move to planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the challenge step when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The framing addresses the actual decision rather than only the stated symptom.
- Options are genuinely distinct and not minor variants.
- At least one conventional and one meaningfully different path were considered when appropriate.
- Strengths and weaknesses are concrete, balanced, and candid.
- Effort labels are plausible for the requester’s context.
- Recommendations follow the stated criteria rather than unstated assistant preferences.
- Any retrieved private context was authorized, minimal, relevant, and kept within the appropriate access boundary.

---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs credible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long list of ideas; it is a small set of meaningfully different paths, with clear tradeoffs and a next step chosen at the right level of rigor.

## 1. Gather relevant context

Start with the information provided. If the user references documents, discussion threads, prior decisions, research, or other records that you are authorized to access, review only the sources needed to understand the decision.

When the question is not self-contained, retrieve a small number of high-value sources, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, deadlines, and dependencies
- Relevant stakeholder concerns and ownership boundaries
- Evidence about attempts already made

Use targeted retrieval only when it could materially change the options. Access private communications or records only for a legitimate purpose, with clear authorization, and use the minimum relevant information. Do not include unrelated personal or sensitive details in the output.

If important context is unavailable, state the assumption or ask a focused question. Do not invent constraints, evidence, or consensus.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What the user is actually deciding
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The initial question may describe a symptom or a proposed solution rather than the real decision. For example, “Should we add a feature?” may actually mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip the pause only when the framing is obvious, the choice is low-stakes, or the user explicitly requests an immediate first pass. A wrong frame produces polished but irrelevant options.

## 3. Generate distinct options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not merely a different level of investment in the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional path
- A lower-effort or incremental path
- A more ambitious path
- A path that changes process, incentives, scope, ownership, or the problem framing
- At least one surprising option, such as delaying, partnering, reducing scope, observing longer, or doing nothing

Do not be contrarian just to appear creative. “Do nothing” is useful only when waiting, learning, timing, or avoided distraction has real value.

Give each option a short, memorable label that communicates its core approach. For every option, provide:

- **What:** One or two sentences explaining the approach.
- **Strengths:** One or two concrete advantages.
- **Weaknesses:** One or two concrete disadvantages, risks, or limitations.
- **Effort:** Low, Medium, or High.

Use specific tradeoffs. Do not hide serious drawbacks or make a preferred option look better by describing alternatives unfairly.

### Option format

| Option | What | Strengths | Weaknesses | Effort |
|---|---|---|---|---|
| **[Short label]** | [Describe the distinct approach.] | [Concrete benefits.] | [Concrete drawbacks or risks.] | [Low / Medium / High] |

## 4. Evaluate and recommend

Choose evaluation criteria that fit the decision. Common criteria include likely impact, effort, cost, speed, risk, reversibility, strategic fit, stakeholder burden, and quality of evidence. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they clarify the decision, but say plainly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this situation, constraints, and goals—not merely why it is attractive in general.
4. Name the assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice.

### Recommendation format

| Rank | Recommendation | Why it fits | Condition that could change the ranking |
|---|---|---|---|
| 1 | **[Option label]** | [Situation-specific reason.] | [Key assumption or new evidence.] |

## 5. Stop for a decision

After presenting the recommendations, wait for the user. They may:

- Choose an option
- Ask for more detail on one option
- Correct the framing or constraints
- Request additional options
- Combine options into a hybrid

If the user proposes a hybrid, test whether its components are compatible and whether it resolves a real tradeoff rather than simply adding scope and complexity.

Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once a path is selected, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term agreements, major staffing decisions, or choices with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record that states the choice, decision owner, rationale, assumptions, expected downside, and review point.
- **Build-oriented choice:** After the decision is recorded, move into planning and execution: requirements, milestones, tasks, ownership, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify that:

- The decision framing reflects the real choice rather than only the requested solution.
- Options are genuinely distinct and not variations in intensity.
- The obvious path and a credible alternative framing have both been considered where relevant.
- Weaknesses are candid, concrete, and proportionate.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria and constraints rather than default preferences.
- Any retrieved private context was authorized, minimal, and kept within the appropriate access boundary.
- The response ends with a clear choice point rather than unrequested implementation.

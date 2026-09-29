---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set without forcing a final choice. Use this workflow when a user asks to brainstorm approaches, explore possible.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not to create a long list of ideas; it is to surface genuinely different paths, make tradeoffs clear, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources that are available in the current environment, review the relevant material first.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the recommendation, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, deadlines, or budgets
- Stakeholder concerns, responsibilities, and approval boundaries
- Evidence about what has already been tried
- Comparable outcomes, customer feedback, or operational data

Use targeted retrieval rather than broad searching. Where sources contain personal or confidential information, access them only with a legitimate purpose and clear authorization. Use the minimum relevant information, omit unrelated sensitive details, and keep the response within the appropriate access boundary.

If important context is unavailable, either state the assumption being made or ask a focused question. Do not invent missing facts.

## 2. Frame the decision before ideating

Write a short framing of the decision, usually two to four sentences. It should identify:

- What the user is actually deciding
- The key constraints and non-negotiables
- What a good outcome looks like
- The criteria by which options should be compared

The user's first wording may describe a symptom or a proposed solution rather than the underlying decision. For example, “Should we add a feature?” may actually mean, “How should we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before producing a substantial option set. Skip this pause only when the framing is obvious, the choice is low-stakes, or the user explicitly requests an immediate first pass. A wrong framing produces polished but irrelevant options.

### Framing template

> **Decision:** [What must be chosen or resolved?]
>
> **Constraints:** [Budget, time, risk, dependencies, permissions, or other limits]
>
> **A good outcome:** [What success looks like]
>
> **Evaluation criteria:** [For example: impact, speed, cost, reversibility, risk, strategic fit]

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional approach
- A lower-effort or incremental approach
- A more ambitious approach
- An approach that changes the process, incentives, scope, ownership, or problem framing
- At least one surprising option, such as delaying, partnering, removing scope, running an experiment, or deliberately doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when waiting, observing, preserving capacity, or avoiding a premature commitment has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

| Element | Include |
|---|---|
| **What** | One or two sentences explaining the approach. |
| **Strengths** | One or two concrete advantages. |
| **Weaknesses** | One or two concrete disadvantages, risks, or limitations. |
| **Effort** | Low, Medium, or High; use a rough estimate of work, coordination, and time. |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option appear stronger by describing alternatives unfairly.

### Option format

#### [Short option label]

- **What:** [Describe the approach.]
- **Strengths:** [Concrete benefits.]
- **Weaknesses:** [Concrete costs, risks, or limitations.]
- **Effort:** [Low / Medium / High]

## 4. Evaluate and recommend

Select evaluation criteria that fit the decision. Common criteria include likely impact, effort, cost, speed, risk, reversibility, strategic fit, stakeholder burden, and learning value. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible when they are instructive, but state clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this user's specific situation, constraints, and goals—not merely why it is generally attractive.
4. Name the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice when several options are credible.

### Recommendation format

1. **[Option label]** — Best fit because [specific connection to the user's constraints and goals].
2. **[Option label]** — Strong alternative because [specific tradeoff it handles better].
3. **[Option label]** — Best if [condition or priority changes].

**Not recommended now:** [Option label], because [dealbreaker weakness].

**Ranking-changing assumption:** [The fact, estimate, or priority that would alter the recommendation].

## 5. Stop for a decision

After presenting recommendations, wait for the user's response. They may:

- Select an option
- Request more detail on an option
- Correct the framing or constraints
- Ask for additional or different options
- Propose a hybrid approach

If the user proposes a hybrid, check whether its components are compatible and whether combining them resolves a real tradeoff rather than simply adding complexity.

Do not begin implementation merely because an option appears promising. Move into execution only after the user selects or explicitly authorizes a path.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choice:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing choices, or decisions with broad organizational effects.
- **Reversible choice:** Create a right-sized decision record that states the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choice:** After the decision is recorded, move into planning and execution: requirements, milestones, tasks, dependencies, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Quality checks

Before sending the response, verify:

- The framing reflects the actual decision rather than only the user's initial phrasing.
- Any contextual retrieval was necessary, authorized, and limited to relevant information.
- The options are genuinely distinct rather than variations in scale.
- The obvious option and at least one meaningfully different option are represented where appropriate.
- Strengths and weaknesses are concrete, balanced, and candid.
- Effort labels reflect both execution work and coordination burden.
- Eliminations are tied to stated constraints rather than hidden preferences.
- Recommendations are tailored to the user's criteria.
- The response preserves the user's decision authority and does not begin implementation prematurely.

---
name: brainstorm
description: Generate genuinely distinct options for a decision or problem, assess their tradeoffs candidly, and recommend a short ranked set while preserving the user’s final choice.
---

# Brainstorm options

Use this workflow when a user needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not a long idea list: surface genuinely different paths, make their tradeoffs clear, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with the information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources that the current environment can access, review the relevant material first.

Only access private communications, records, or documents when there is a legitimate purpose, clear authorization, and an appropriate access boundary. Use the minimum relevant sources and information. Do not include unrelated personal, confidential, or sensitive details in the output.

If the question is not self-contained, retrieve a small number of high-value sources that could materially change the options, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, ownership boundaries, or deadlines
- Evidence about what has already been tried
- Relevant stakeholder needs or operational dependencies

Do not search broadly by default. Use targeted retrieval. If important information is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- Important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The user’s wording may describe a symptom or a preferred solution rather than the underlying decision. For example, “Should we add a feature?” may really mean “How can we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, low-consequence, or the user explicitly requests an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must represent a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, when relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes process, incentives, scope, timing, or the problem framing
- At least one surprising option, such as delaying, partnering, removing scope, or deliberately doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, avoided distraction, or preserving resources has genuine value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

| Element | Include |
|---|---|
| **What** | One or two sentences explaining the approach. |
| **Strengths** | One or two concrete advantages. |
| **Weaknesses** | One or two concrete disadvantages, risks, or limitations. |
| **Effort** | Low, Medium, or High; use a rough, context-appropriate estimate. |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option appear stronger by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose evaluation criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, evidence strength, and stakeholder burden. Add domain-specific criteria when they matter more than these defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but clearly explain why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits this user’s situation, constraints, and goals—not merely why it is attractive in general.
4. Name the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly asks for one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may:

- Choose an option
- Request more detail on a specific option
- Correct the framing or constraints
- Ask for additional options
- Combine options into a hybrid

If the user proposes a hybrid, test whether its components are compatible and whether the combination resolves a real tradeoff rather than simply adding complexity.

Do not begin implementation merely because an option appears promising. Move into execution only after the user selects or explicitly authorizes a path.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence, reversibility, and implementation needs:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, major staffing choices, or decisions with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that identifies the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After the decision is recorded, move into planning and execution: requirements, milestones, tasks, ownership, and validation measures.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Do not skip the pressure test when the cost of being wrong is high.

## Response template

Use the following structure for a typical response:

```markdown
## Decision framing
[Two to four sentences describing the actual decision, constraints, and success criteria.]

## Options

### [Memorable option label]
- **What:** [Approach.]
- **Strengths:** [Concrete advantages.]
- **Weaknesses:** [Concrete disadvantages or risks.]
- **Effort:** [Low / Medium / High]

### [Memorable option label]
- **What:** [Approach.]
- **Strengths:** [Concrete advantages.]
- **Weaknesses:** [Concrete disadvantages or risks.]
- **Effort:** [Low / Medium / High]

## Assessment
- **Not recommended:** [Any option with a dealbreaker, and why.]
- **1. [Recommended option]:** [Why it fits this situation.]
- **2. [Recommended option]:** [Why it fits this situation.]
- **3. [Recommended option, if useful]:** [Why it fits this situation.]
- **Ranking could change if:** [Key assumption or missing evidence.]

## Next step
[Ask the user to choose, request detail, revise the framing, or propose a hybrid.]
```

## Quality checks

Before sending, verify that:

- The framing reflects the actual decision rather than only the first solution proposed.
- The options are truly distinct and not minor variants of one another.
- The option set includes the obvious path and, where useful, a genuinely different or surprising path.
- Strengths and weaknesses are concrete and candid.
- Effort labels are plausible for the stated context.
- Recommendations follow the user’s criteria and constraints rather than default assistant preferences.
- The response does not expose unnecessary private, sensitive, or irrelevant information.
- The response ends by returning control to the user rather than prematurely starting implementation.

---
name: brainstorm
description: Generate distinct options for a decision or problem, assess their tradeoffs honestly, and recommend a short ranked set without forcing a final choice.
---

# Brainstorm options

Use this workflow when someone needs possible approaches to a decision, problem, or opportunity but is not ready to commit. The goal is not to produce a long idea list; it is to surface genuinely different paths, make their tradeoffs clear, and leave the user with a small number of credible choices.

## 1. Gather relevant context

Start with information the user supplied. If they reference documents, discussion threads, prior decisions, research, or other sources available in the current environment, review the sources that are necessary to understand the decision.

When accessing private communications or records, do so only for a legitimate purpose and with clear authorization. Use the minimum relevant sources and details, omit unrelated sensitive information, and keep the output within the appropriate access boundary.

If the question is not self-contained, retrieve a small number of high-value sources of context, such as:

- Earlier decisions and their rationale
- Existing constraints, commitments, or deadlines
- Stakeholder concerns, responsibilities, and approval boundaries
- Evidence about what has already been tried

Do not search broadly by default. Use targeted retrieval only when it could materially change the options. If important information is unavailable, state the assumption or ask a focused question rather than inventing context.

## 2. Frame the decision before ideating

Write a short framing, usually two to four sentences, that states:

- What decision the user is actually making
- The important constraints and non-negotiables
- What a good outcome looks like and how options should be judged

The user’s wording may describe a symptom or a proposed solution rather than the underlying decision. For example, “Should we add a feature?” may really mean, “How should we reduce a recurring user problem within a limited budget?”

Ask the user to confirm or correct the framing before generating a substantial option set. Skip this pause only when the framing is obvious, the decision is low-stakes, or the user explicitly asks for an immediate first pass. Incorrect framing produces polished but irrelevant options.

## 3. Generate a distinct set of options

Generate five to seven options unless the decision naturally has fewer meaningful paths. Each option must be a fundamentally different approach, not a different intensity level of the same approach. Merge near-duplicates.

Include, where relevant:

- The obvious or conventional option
- A lower-effort or incremental option
- A more ambitious option
- An option that changes the process, incentives, scope, ownership, or problem framing
- At least one surprising option, such as delaying, partnering, reducing scope, or doing nothing

Do not be contrarian merely to appear creative. “Do nothing” is useful only when observation, timing, or avoiding distraction has real value.

Give every option a short, memorable label that communicates its core approach. For each option, provide:

| Element | What to include |
|---|---|
| **What** | One or two sentences explaining the approach. |
| **Strengths** | One or two concrete advantages. |
| **Weaknesses** | One or two concrete disadvantages or failure risks. |
| **Effort** | Low, Medium, or High. |

Use specific tradeoffs. Do not soften serious drawbacks, and do not make a preferred option look better by describing alternatives unfairly.

## 4. Evaluate and recommend

Choose evaluation criteria that fit the decision. Common criteria include likely impact, effort, cost, risk, speed, reversibility, strategic fit, and stakeholder burden. Add domain-specific criteria when they matter more than the defaults.

Then:

1. Identify options with dealbreaker weaknesses under the stated constraints. Keep them visible if they are instructive, but say clearly why they are not recommended.
2. Rank the strongest two or three options.
3. For each recommendation, explain in one sentence why it fits the user’s specific situation, constraints, and goals—not merely why it is generally attractive.
4. Name the key assumption most likely to change the ranking, if one exists.

Do not force a single winner unless the user explicitly requests one. Preserve meaningful choice.

## 5. Stop for a decision

After presenting recommendations, wait for the user. They may choose an option, request more detail, reject the framing, ask for additional options, or combine approaches.

If the user proposes a hybrid, test whether its components are compatible and whether combining them resolves a real tradeoff rather than adding complexity. Do not begin implementation merely because an option appears promising.

## 6. Hand off with the right level of rigor

Once the user selects a path, choose the next activity based on consequence and reversibility:

- **High-consequence or difficult-to-reverse choices:** Run a structured challenge, pre-mortem, or pressure test before commitment. Use this for major strategic bets, public commitments, long-term contracts, major role decisions, or choices with broad organizational effects.
- **Reversible choices:** Create a right-sized decision record that defines the choice, owner, rationale, assumptions, and review point.
- **Build-oriented choices:** After the decision is recorded, move into planning and execution: requirements, milestones, implementation tasks, and validation.

A useful sequence is: brainstorm options, pressure-test consequential choices, make and record the decision, then plan or build. Avoid skipping the pressure test when the cost of being wrong is high.

## Output template

```markdown
### Decision framing
[Two to four sentences describing the actual decision, constraints, and success criteria.]

### Options

#### [Short option label]
- **What:** [Approach.]
- **Strengths:** [Concrete advantages.]
- **Weaknesses:** [Concrete disadvantages or risks.]
- **Effort:** [Low / Medium / High]

[Repeat for each distinct option.]

### Evaluation
- **Not recommended:** [Option and dealbreaker, if applicable.]
- **1. [Recommended option]:** [Why it fits this situation.]
- **2. [Recommended option]:** [Why it fits this situation.]
- **3. [Recommended option]:** [Why it fits this situation, if useful.]
- **Ranking-changing assumption:** [Assumption most likely to alter the recommendation.]

### Next step
[Ask the user to choose, request detail, revise the framing, or propose a hybrid.]
```

## Quality checks

Before sending, verify that:

- The decision framing reflects the actual choice rather than only the stated symptom or preferred solution.
- Options are genuinely distinct rather than variations in scale or effort.
- The obvious option and a meaningfully different or surprising option are represented when relevant.
- Weaknesses are candid, concrete, and proportionate.
- Effort labels are plausible.
- Recommendations follow the user’s stated criteria rather than the assistant’s default preferences.
- Any retrieved private context was authorized, necessary, minimally used, and not exposed beyond the intended audience.

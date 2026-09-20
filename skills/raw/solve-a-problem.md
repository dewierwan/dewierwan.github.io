---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through option selection, implementation, verification, and handoff, with an analysis-only stopping point when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem whose solution is not already clear. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, complete Step 6, present the proposal, and stop pending a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's proposed solution. Work backward from a request to build something:

- Who has the problem, and what are they trying to achieve?
- What happens today?
- What workaround or alternative exists?
- How frequent, costly, urgent, or blocking is the problem?
- What observable outcome would make the situation better?

Write a concise problem statement and descriptive requirements. State the outcome and constraints rather than assuming a particular implementation. If the requested solution does not fit the problem, say so directly.

Ask only for information that cannot be found in available context, documentation, code, or authorized records. When accessing communications or records about people, confirm a legitimate purpose and clear authorization; use the minimum relevant sources and information, omit unrelated sensitive details, and keep findings within the appropriate access boundary.

## 2. Confirm priority and decision readiness

Assess severity, frequency, affected users, opportunity cost, and alternatives. Treat **do nothing**, **deprioritize**, and **improve the current workaround** as genuine options.

Separate decisions by reversibility:

- **Reversible decisions:** Small choices that are easy to change. Make a reasonable choice and proceed.
- **Hard-to-reverse decisions:** Persistent data changes, public interfaces, long-lived settings, migrations, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation.

Use this workflow when the direction is sufficiently committed. If the real task is still to explore possibilities, challenge assumptions, or select a strategic direction, do that decision work first. Do not allow implementation momentum to create an unapproved long-term commitment.

### Readiness gate: proceed to research

Proceed only when the following are true:

- The problem and intended outcome are understandable.
- The responsible decision-maker and relevant constraints are known.
- Priority is sufficient relative to other work, or the user explicitly requests exploration.
- Any hard-to-reverse decision is either out of scope or explicitly awaiting a decision.

If a condition is not met, state the missing decision or information and request it rather than designing prematurely.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before creating a new abstraction.

Identify compatibility requirements, deployment and release practices, security expectations, supported environments, ownership boundaries, monitoring, and maintenance capacity. Follow existing system conventions unless there is a clear reason not to.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. For example:

- Must preserve existing authentication, permissions, and data behavior.
- Must fit the available delivery and maintenance capacity.
- Should avoid unnecessary dependencies and persistent settings.
- Must have a clear test and verification method.
- Should be removable or reversible if it does not work.

These criteria govern both option generation and selection. Without them, the first plausible solution may win by accident.

## 5. Generate varied approaches

Generate meaningfully different approaches rather than small variations of one design. Consider:

1. Do nothing, defer, or improve the workaround.
2. A non-code solution: instructions, process changes, templates, training, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated technical solution.
5. Build, buy, or integrate with an existing service.

For ambiguous or high-impact problems, create a broader candidate set before narrowing; use roughly ten candidates when deliberate exploration is needed. Keep each option brief: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that differ by runtime conditions.
- Validate inputs and fail clearly for invalid states. Do not silently turn programming errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where practical.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Avoid quick fixes placed outside the appropriate design boundary.

## 6. Evaluate and recommend

Compare viable options against the criteria. Make one clear recommendation; do not merely list possibilities. Explain why it is preferred, the tradeoffs accepted, and any decision that remains open.

Use this proposal format:

```markdown
# DD MMM YYYY: Solve — [topic]

## Problem
[Who needs what outcome, current state, impact, and constraints.]

## Evaluation criteria
- [Criterion]

## Options
### 1. [Option name]
[What it is, benefits, costs, risks, and fit against criteria.]

## Recommendation
[Chosen option, rationale, tradeoffs, and required decision or approval.]

## Risks and open questions
- [Risk, irreversible consequence, dependency, or unresolved question]
```

Keep each approach to one or two short paragraphs. Store the proposal in the user's chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a date-prefixed title in `DD MMM YYYY` format.

### Recommendation gate

Before presenting a recommendation, check that:

- At least one non-build or defer option was considered.
- Options were evaluated against stated criteria, not intuition alone.
- The recommendation does not hide a hard-to-reverse commitment.
- Important assumptions, risks, and unverified claims are explicit.
- The proposal identifies the person or role that must make any remaining decision.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Put it where appropriate reviewers can inspect, edit, and approve it. Include scope, ordered steps, affected components, dependencies, migration or rollback strategy, test strategy, deployment steps, and ownership of follow-up work.

Use this plan format:

```markdown
# DD MMM YYYY: Solve — [topic] plan

## Scope and non-goals
[What is included and explicitly excluded.]

## Implementation steps
1. [Step, affected component, and expected result.]

## Safety and rollout
[Migration, compatibility, rollback, release, and monitoring approach.]

## Verification
- [Automated check]
- [Manual or operational check]

## Completion criteria
- [Observable condition required to call the work complete.]
```

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual or operational verification. Test expected behavior, failure behavior, and relevant compatibility boundaries.

### Implementation completion gate

Do not claim completion until:

- The implementation meets the agreed evaluation criteria or documented exceptions are approved.
- Relevant checks have run and their results are recorded.
- Migration, rollback, release, and monitoring needs have been addressed where applicable.
- Known gaps, failed checks, and unverified assumptions are disclosed.

Commit, publish, or deploy changes only according to the user's repository and release practices.

## 8. Hand off

Report the outcome in this format:

```markdown
## Outcome
[What changed and the user outcome enabled.]

## Verification
- [Check performed]: [result]

## Limitations and risks
- [Known limitation, deferred work, or monitoring concern]

## Required follow-up
- [User action, rollout step, owner, or date]

## References
- [Proposal, plan, change set, or operational record]
```

Keep the handoff focused on outcomes and operationally useful facts. Do not imply that untested behavior is verified, and do not bury important limitations in temporary implementation detail.

---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, recommendation, implementation, verification, and handoff. The workflow supports analysis-only work when requested and requires explicit,.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, automation, or operational problem whose solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to “build X,” work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including existing workarounds?
- How frequent, costly, urgent, or blocking is it?
- What outcome would materially improve the situation?
- What constraints matter: time, budget, reliability, privacy, compatibility, or ownership?

Write a concise problem statement and descriptive requirements. Describe desired outcomes and constraints, not an assumed implementation. If the proposed solution does not fit the problem, say so directly.

Ask only for information that cannot be found in authorized project context, documentation, code, or records. When examining communications or records about people, use them only for a legitimate purpose with clear authorization; inspect the minimum relevant sources, omit unrelated sensitive details, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and the cost of delay. Include **do nothing**, **defer**, or **improve the current workaround** as real options when appropriate.

Distinguish between:

- **Reversible decisions:** Small, easy-to-change choices. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, long-lived settings, migrations, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record rationale when the decision has lasting consequences.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before spending substantial effort on design or implementation.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before inventing a new mechanism.

Identify constraints such as compatibility requirements, deployment practices, supported environments, ownership boundaries, monitoring, security expectations, and privacy requirements. Use existing conventions unless there is a strong, documented reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve existing authentication, access controls, and data behavior.
- Must fit available delivery time and maintenance capacity.
- Should avoid new dependencies, public interfaces, or persistent configuration.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide option generation and selection. Without them, the first plausible solution can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change: instructions, a process adjustment, a template, training, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For an ambiguous or high-impact problem, generate a broader set of candidates before narrowing. Keep each option concise: what it is, which requirement it addresses, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate inputs and states strictly; fail visibly for invalid states rather than silently producing plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, persistent data, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Place changes in the appropriate design boundary; do not use a quick fix that creates hidden long-term complexity.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Keep the proposal direct. Store it in the user's chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear date-prefixed title, such as `10 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and ownership of follow-up actions. Keep the plan in a location where relevant reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, access control, privacy, and failure behavior.

Do not claim success based only on implementation. State what was actually tested, what passed or failed, and what remains unverified. Commit, publish, or deploy only according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.

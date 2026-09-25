---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, recommendation, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, or automation problem whose solution is not already obvious. Do not use it for a small fix, a routine task with a known implementation, or a request that only needs a direct factual answer.

By default, work from understanding through implementation and handoff. If the user asks for analysis only, stop after the recommendation and wait for a decision.

When reviewing private communications, records, or data about people, first confirm a legitimate purpose and clear authorization. Use only the minimum relevant sources and information, omit unrelated sensitive details, respect consent and privacy expectations, and keep findings within the appropriate access boundary.

## 1. Understand the problem

Start with the underlying problem, not the user’s first proposed solution. If they ask to “build X,” work backward:

- Who experiences the problem, and in what role or context?
- What are they trying to accomplish?
- What happens today?
- What workarounds exist?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the situation meaningfully better?

Write a concise problem statement and descriptive requirements. Describe desired outcomes, constraints, and evidence of success rather than assuming an implementation. If the proposed solution appears mismatched to the problem, say so directly and explain why.

Ask only for information that cannot reasonably be found in the available documentation, project context, authorized records, or system behavior.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, maintenance cost, and available alternatives. Include **do nothing**, **deprioritize**, or **improve the current workaround** as real options when the issue is rare, low-cost, or already adequately handled.

Distinguish between decisions that are easy to reverse and commitments that are expensive to undo:

- **Reversible decisions:** small, isolated choices that can be changed cheaply. Use reasonable judgment, choose, and move forward.
- **Hard-to-reverse decisions:** public interfaces, persistent data changes, long-lived settings, migrations, security boundaries, external contracts, vendor commitments, or changes with broad compatibility effects. Pause and obtain an explicit decision before implementation. Record the rationale when useful.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in substantial design or implementation.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns, reusable components, and existing platform capabilities before inventing something new.

Understand relevant constraints, including compatibility expectations, deployment practices, ownership boundaries, security requirements, supported environments, monitoring, and maintenance capacity. Follow existing conventions unless there is a clear reason not to.

When research involves personal or confidential information, summarize only what is necessary to solve the stated problem. Do not expose private details merely because they were available.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve existing authentication, authorization, and data behavior.
- Must fit the available delivery time and maintenance capacity.
- Should avoid new dependencies, persistent settings, or external commitments.
- Must have a clear verification method.
- Must be removable or reversible if it fails.
- Must respect privacy, access controls, and applicable policy.

These criteria guide option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, training, or a capability already available in an existing platform.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For especially ambiguous problems, generate a wider candidate set before narrowing. Keep each option concise: what it is, what it solves, its main costs, and its key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that behave differently depending on runtime conditions.
- Validate inputs and states strictly. Fail visibly for invalid internal states rather than silently producing plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, public interfaces, and data structures as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where practical.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Avoid quick fixes that bypass the appropriate design boundary.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep proposals direct and short. Store durable proposals in the user’s chosen shared documentation system when review, editing, or a decision record is needed; otherwise provide the proposal in the current workspace. Use a clear date-prefixed title, such as `25 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, data or migration effects, rollback strategy, test strategy, deployment steps, and follow-up ownership.

Implement the approved solution using the project’s conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, privacy, security, and failure behavior.

Do not claim success based only on implementation. State what was actually tested, what passed or failed, and what remains unverified. Commit, publish, or deploy only according to the user’s repository, review, and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- The verification performed and its results.
- Known limitations, risks, and deferred work.
- Any required user action, rollout step, or monitoring.
- Links or references to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.

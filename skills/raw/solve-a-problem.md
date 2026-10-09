---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only mode.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, operational, integration, or automation problem whose solution is not already obvious. Do not use it for a small fix or routine task with a known implementation.

By default, work from understanding through implementation. If the user requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's proposed solution. If they ask to “build X,” work backward:

- Who experiences the problem, and in what role or context?
- What are they trying to accomplish?
- What happens today, including workarounds?
- How frequent, costly, urgent, or blocking is it?
- What outcome would make the situation meaningfully better?

Write a concise problem statement and descriptive requirements. Describe desired outcomes and constraints, not an assumed implementation. If the proposed solution does not fit the problem, say so directly.

Ask only for information that cannot reasonably be found in authorized context, documentation, code, or records. When using communications or records about people, have a legitimate purpose and clear authorization; use only the minimum relevant material, omit unrelated sensitive details, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, and available alternatives. Include “do nothing,” “deprioritize,” or “improve the workaround” as real options when appropriate.

Distinguish decisions by reversibility:

- **Reversible decisions:** Small, easy-to-change choices. Use reasonable judgment, choose, and proceed.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, long-lived settings, migrations, external contracts, security boundaries, or vendor commitments. Pause and obtain an explicit decision before implementation. Record the decision and rationale when useful.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Find established patterns and reusable components before inventing new ones.

Understand compatibility needs, deployment practices, security expectations, supported environments, ownership boundaries, monitoring, and maintenance capacity. Follow existing conventions unless there is a strong, documented reason to change them.

## 4. Define evaluation criteria

Define lightweight, explicit criteria before generating solutions. For example:

- Must preserve existing authentication, authorization, and data behavior.
- Must fit the available time and maintenance capacity.
- Should avoid new dependencies, persistent settings, or public interfaces.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide both option generation and selection. Without them, the first plausible idea may win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small, targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For especially ambiguous problems, generate a wider candidate set before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-dependent special cases.
- Validate strictly and fail fast for invalid states. Do not silently convert programming errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Place changes in the appropriate design boundary; avoid quick fixes that create hidden coupling.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep proposals direct and short. Store them in the user’s chosen shared documentation system when durable review or collaboration is needed; otherwise use the current workspace. Use a clear, date-prefixed title such as `DD MMM YYYY: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership. Keep the plan where reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm results against the evaluation criteria, including compatibility, authorization, privacy, and failure behavior.

Do not claim success based only on implementation. State what was tested and what remains unverified. Commit, publish, or deploy changes only according to the user’s repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and its results.
- Known limitations, risks, and deferred work.
- Required user action, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Avoid burying the reader in temporary implementation notes.

---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem whose solution is not already obvious. Do not use it for a small fix, a routine task with a known implementation, or work that should first be resolved as a strategic decision.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to build a particular thing, work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, and what workarounds exist?
- How frequent, costly, urgent, or blocking is it?
- What outcome would materially improve the situation?
- What constraints, compatibility needs, deadlines, or access boundaries apply?

Write a concise problem statement and descriptive requirements. Describe outcomes and constraints rather than assuming an implementation. If the proposed solution appears mismatched to the problem, say so directly.

Ask only for information that cannot be found in authorized project context, documentation, code, or records. When reviewing communications or records about people, use them only for a legitimate authorized purpose, inspect the minimum relevant sources, and omit unrelated or sensitive personal details from outputs.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Include **do nothing**, **deprioritize**, or **improve the current workaround** as genuine options when appropriate.

Distinguish between:

- **Reversible decisions:** Small, easy-to-change choices. Make a reasonable choice and proceed.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, long-lived settings, migrations, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation and record the rationale when useful.

If priority or direction is unclear, present the tradeoff and ask the accountable decision-maker to choose before substantial design or implementation work.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Find established patterns and reusable components before inventing new ones.

Identify compatibility requirements, deployment practices, supported environments, ownership boundaries, security expectations, and monitoring needs. Use existing conventions unless there is a clear reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve current authentication, permissions, and data behavior.
- Must fit available delivery time and maintenance capacity.
- Should avoid new dependencies and long-lived configuration.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide generation and selection. Without them, the first plausible idea may win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For ambiguous problems, generate a wider candidate set before narrowing. For each option, state what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that vary by runtime condition.
- Validate strictly and fail fast for invalid states. Do not hide programmer errors by returning plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Avoid quick fixes that bypass the appropriate design boundary.

## 6. Evaluate and recommend

Compare viable options against the evaluation criteria. Present a concise proposal containing:

- Problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Keep the proposal direct. Store it in the user's approved shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear date-prefixed title, such as `17 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership. Put the plan where appropriate reviewers can edit and approve it.

Implement the approved solution using project conventions and authorized access. Run relevant automated tests, static checks, and focused manual verification. Confirm results against the evaluation criteria, including compatibility and failure behavior.

Do not claim success based only on implementation. State what was tested, the observed results, and what remains unverified. Commit, publish, or deploy only according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Do not include personal, confidential, or access-restricted information beyond the audience's authorized boundary.

---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, while allowing analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem whose solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start from the underlying problem, not the user's proposed solution. If the request is to “build X,” work backward:

- Who is affected, and what are they trying to accomplish?
- What happens today?
- What workarounds exist?
- How frequent, costly, urgent, or blocking is the issue?
- What outcome would materially improve the situation?

Write a concise problem statement and descriptive requirements. Describe the required outcome and constraints, not an assumed implementation. If the proposed solution does not fit the problem, say so directly.

Ask only for information that cannot be found in authorized project context, documentation, code, or records. When reviewing private communications or records about people, confirm a legitimate purpose and clear authorization; use only the minimum relevant material, omit unrelated sensitive details, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, available alternatives, opportunity cost, and maintenance cost. “Do nothing,” “deprioritize,” or “improve the workaround” are valid options when the issue is rare, low-impact, or adequately addressed already.

Distinguish between decision types:

- **Reversible decisions:** Small choices that are cheap to change. Make a reasonable choice and proceed.
- **Hard-to-reverse decisions:** Public interfaces, persistent data changes, migrations, long-lived configuration, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the commitment matters.

A useful sequence is: explore possibilities, test the preferred direction, make the commitment, then solve and implement. If direction or priority is unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in detailed design.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before creating new ones.

Identify compatibility requirements, deployment practices, privacy and security expectations, supported environments, ownership boundaries, and monitoring needs. Use established system conventions unless there is a strong reason to change them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating solutions. For example:

- Must preserve existing authentication, authorization, and data behavior.
- Must fit the available delivery time and maintenance capacity.
- Should avoid new dependencies and long-lived configuration where practical.
- Must have a clear verification method.
- Must be reversible or removable if it fails.

These criteria guide solution generation and selection. Without them, the first plausible idea may win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the existing workaround.
2. A non-code solution, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For an ambiguous or high-impact problem, generate a broader candidate set before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases whose behavior changes with runtime conditions.
- Validate inputs and fail clearly for invalid states. Do not silently turn programmer errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is a stated requirement.
- Put changes at the correct design boundary; avoid quick fixes that bypass the system’s structure.

## 6. Evaluate and recommend

Compare viable options against the criteria from Step 4. Present a concise proposal containing:

- The problem statement.
- Evaluation criteria.
- Viable options and their tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep the proposal direct. Store it in the user’s chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear, date-prefixed title such as `30 Sep 2026: Solve — topic`.

**Readiness gate:** Do not implement until the problem, recommendation, scope, decision owner, and any hard-to-reverse commitments are clear. If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, dependencies, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership. Keep the plan where appropriate reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, authorization, privacy, and failure behavior.

Use this audit before declaring completion:

- The implemented behavior matches the approved problem statement.
- Tests cover the main path and meaningful failure cases.
- Invalid inputs and internal faults fail visibly rather than producing misleading output.
- Rollback, migration, and operational effects are understood where relevant.
- Documentation, monitoring, and access controls are updated when needed.

Do not claim success based only on implementation. State what was tested and what remains unverified. Commit, publish, or deploy changes only according to the user’s repository and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and its results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- Links or references to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail. Common failure modes are solving the requested implementation rather than the real problem, skipping explicit evaluation criteria, treating a permanent commitment as a minor choice, silently masking defects, and declaring completion without meaningful verification.

---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem whose solution is not already obvious. Do not use it for a small fix or a routine task with a known implementation.

By default, work from understanding through implementation. If the user asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the user's first proposed solution. If they ask to build something, work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today, including workarounds?
- How often does it occur, how costly or blocking is it, and who is affected?
- What outcome would make the situation meaningfully better?

Write a concise problem statement and descriptive requirements. Describe the desired outcome, constraints, and success conditions rather than assuming an implementation. If the proposed solution does not fit the problem, say so clearly.

Ask only for information that cannot be found in the available context, documentation, code, or authorized records. When reviewing communications, operational records, or information about people, use them only for a legitimate purpose with clear authorization. Use the minimum relevant sources and details, omit unrelated sensitive information, and keep findings within the appropriate access boundary.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, and available alternatives. Treat “do nothing,” “deprioritize,” or “improve the current workaround” as real options when the issue is rare, low-cost, or adequately handled.

Distinguish reversible decisions from hard-to-reverse commitments:

- **Reversible decisions:** Small choices that are easy to change. Use reasonable judgment, decide, and move forward.
- **Hard-to-reverse decisions:** Persistent data changes, public interfaces, long-lived settings, migrations, external contracts, security boundaries, or vendor commitments. Pause and obtain an explicit decision before implementation. Record the decision and rationale when the commitment warrants it.

If priority or direction is unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in substantial design or implementation.

## 3. Research the current context

Read relevant project instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns and reusable components before creating new ones.

Understand compatibility requirements, deployment practices, security expectations, supported environments, ownership boundaries, operational constraints, and monitoring. Follow existing conventions unless there is a strong, documented reason to change them.

## 4. Define evaluation criteria

Define lightweight, explicit criteria before generating solutions. For example:

- Must preserve existing authentication, authorization, and data behavior.
- Must fit the available delivery time and maintenance capacity.
- Should avoid new dependencies, persistent settings, and public surface area.
- Must have a clear verification method.
- Should be removable or reversible if it fails.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of the same design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code change, such as clearer instructions, a process adjustment, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For ambiguous problems, generate a wider set of candidates before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that behave differently by runtime condition.
- Use strict validation and fail fast for invalid states. Do not silently convert programmer errors into plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Place changes in the appropriate design boundary; avoid expedient patches that create lasting complexity.

## 6. Evaluate and recommend

Compare viable options against the evaluation criteria. Present a concise proposal containing:

- Problem statement and current impact.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, hard-to-reverse consequences, and open decisions.

Keep proposals direct and brief. Store them in the user's chosen shared documentation system when durable review or collaboration is needed; otherwise provide them in the current workspace. Use a clear date-prefixed title, such as `12 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and ownership of follow-up actions. Keep the plan where relevant reviewers can edit and approve it.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm the result against the evaluation criteria, including compatibility, security, privacy, and failure behavior.

Do not claim success based only on implementation. State what was tested, the results, and what remains unverified. Commit, publish, or deploy changes only according to the user's repository, review, and release practices.

## 8. Hand off

Report:

- What changed and the user outcome it enables.
- Verification performed and its results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful details. Do not bury the reader in temporary implementation notes.

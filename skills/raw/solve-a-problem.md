---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff, with an analysis-only stopping point when requested.
---

# Solve a problem

Use this workflow for a non-trivial product, technical, process, integration, automation, or operational problem whose solution is not already clear. Do not use it for a small fix or a routine task with a known implementation path.

By default, work from understanding through implementation and handoff. If the user requests analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start from the underlying problem, not the user's proposed solution. If they ask to “build X,” work backward:

- Who experiences the problem, and what are they trying to accomplish?
- What happens today?
- What workarounds exist?
- How frequent, costly, urgent, or blocking is the issue?
- What outcome would materially improve the situation?

Write a concise problem statement and descriptive requirements. State desired outcomes, constraints, and success conditions without prematurely assuming an implementation. If the proposed solution does not address the underlying problem, say so clearly.

Ask only for information that cannot be found in authorized, relevant project context. When consulting private records or communications, have a legitimate purpose and clear authorization, use the minimum relevant material, and exclude unrelated or sensitive personal details.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, alternatives, and maintenance burden. Treat “do nothing,” “deprioritize,” or “improve the current workaround” as valid options when appropriate.

Separate decisions by reversibility:

- **Reversible decisions:** Small choices that are cheap to change. Use reasonable judgment and proceed.
- **Hard-to-reverse decisions:** Persistent data changes, public interfaces, long-lived settings, migrations, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the rationale when the decision will matter later.

If priority or direction is unclear, present the tradeoff and obtain a decision before investing heavily in design or implementation.

## 3. Research the current context

Review relevant instructions, architecture notes, repository guidance, service documentation, existing code, tests, operational procedures, and prior attempts. Look for established patterns, reusable components, and constraints before designing something new.

Identify compatibility requirements, deployment practices, security expectations, supported environments, ownership boundaries, monitoring, and rollback limits. Follow existing conventions unless there is a clear reason not to.

## 4. Define evaluation criteria

Set explicit, lightweight criteria before generating options. For example:

- Must preserve existing authentication, privacy, and data behavior.
- Must fit available time and maintenance capacity.
- Should avoid unnecessary dependencies or durable configuration.
- Must have a clear verification method.
- Should be removable or reversible if it performs poorly.

These criteria guide both option generation and selection. Without them, the first plausible idea can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the workaround.
2. A non-code solution: clearer guidance, a process change, a template, or an existing platform capability.
3. A small targeted technical change.
4. A larger integrated solution.
5. Build, buy, or integrate with an existing service.

For ambiguous problems, generate a broader candidate set before narrowing. Keep each option short: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over special cases that vary with runtime conditions.
- Validate strictly and fail fast for invalid states. Do not hide programmer errors by returning plausible but incorrect results.
- Prefer established conventions over new abstractions, and new abstractions over long-lived configuration.
- Treat new fields, settings, and public interfaces as ongoing maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and existing infrastructure where possible.
- Design for deterministic, isolated tests.
- Prioritize correctness over performance unless performance is an explicit requirement.
- Make clean changes in the appropriate design boundary; avoid quick fixes that create future debt.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal with:

- Problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, and open decisions.

Keep the proposal direct. Store it in the user's chosen shared documentation system when durable review or collaboration is needed; otherwise provide it in the current workspace. Use a clear date-prefixed title, such as `29 Sep 2026: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, migration or rollback strategy, test strategy, deployment steps, and follow-up ownership.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Check results against the evaluation criteria, including compatibility, privacy, security, and failure behavior.

Do not claim success based solely on implementation. State what was tested, what passed, and what remains unverified. Commit, publish, or deploy only according to the user's repository and release practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and results.
- Known limitations, risks, and deferred work.
- Required user action, rollout steps, or monitoring.
- References to the proposal, plan, and change set when applicable.

Keep the handoff focused on outcomes and operationally useful detail rather than temporary implementation notes.

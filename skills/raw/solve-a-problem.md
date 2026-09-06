---
name: solve-a-problem
description: Take a non-trivial product, technical, process, or automation problem from diagnosis through options, implementation, verification, and handoff. The workflow supports analysis-only work when requested.
---

# Solve a problem

Use this workflow for a non-trivial build, integration, automation, process, or operational problem where the appropriate solution is not already clear. Do not use it for a small fix or routine task with a known implementation.

By default, work from understanding through implementation. If the requester asks for analysis only, stop after the recommendation and wait for a decision.

## 1. Understand the problem

Start with the underlying problem, not the proposed solution. If someone asks to “build X,” work backward:

- Who experiences the problem, and in what role or situation?
- What are they trying to accomplish?
- How does the work happen today?
- What workarounds, failures, delays, or risks exist?
- How frequent, costly, urgent, or blocking is it?
- What outcome would meaningfully improve the situation?

Write a concise problem statement and descriptive requirements. State desired outcomes and constraints rather than assuming a particular implementation. If the proposed solution does not appear to solve the underlying problem, say so directly and explain why.

Ask only for information that cannot reasonably be found in authorized project context, documentation, code, or relevant records. When accessing records about people, use them only for a legitimate, authorized purpose; review the minimum relevant material; and omit unrelated or sensitive personal details.

## 2. Assess whether to solve it now

Assess severity, frequency, affected users, opportunity cost, available alternatives, and maintenance burden. Treat “do nothing,” “deprioritize,” or “improve the current workaround” as valid options when the problem is rare, low-impact, or adequately handled already.

Distinguish between reversible choices and hard-to-reverse commitments:

- **Reversible choices:** Small, easy-to-change decisions. Use reasonable judgment, choose a path, and proceed.
- **Hard-to-reverse commitments:** Public interfaces, persistent data changes, migrations, long-lived settings, security boundaries, external contracts, or vendor commitments. Pause for an explicit decision before implementation. Record the decision, alternatives, and rationale when the impact warrants it.

If direction or priority remains unclear, present the tradeoff and ask the responsible decision-maker to choose before investing in extensive design or implementation.

## 3. Research the current context

Read relevant project guidance, architecture notes, repository instructions, service documentation, existing code, tests, operating procedures, and prior attempts. Look for established patterns and reusable components before creating a new approach.

Identify relevant constraints, including compatibility, supported environments, security expectations, ownership boundaries, deployment practices, observability, and operational support. Follow existing conventions unless there is a clear, documented reason to depart from them.

## 4. Define evaluation criteria

Define explicit, lightweight criteria before generating options. For example:

| Criterion | Example expectation |
|---|---|
| Compatibility | Must preserve current authentication and existing data behavior. |
| Delivery | Must fit the available time and maintenance capacity. |
| Complexity | Should avoid unnecessary dependencies, settings, and special cases. |
| Verification | Must have a clear test and validation method. |
| Reversibility | Should be removable or recoverable if it does not work. |

These criteria guide both option generation and selection. Without them, the first plausible solution can win by accident.

## 5. Generate varied approaches

Generate genuinely different approaches, not minor variations of one design. Consider:

1. Do nothing, defer, or improve the current workaround.
2. A non-code solution, such as clearer instructions, a process change, a template, or an existing platform capability.
3. A small, targeted technical change.
4. A larger integrated solution.
5. Building internally, purchasing a service, or integrating an existing service.

For an ambiguous problem, generate a wider candidate set before narrowing. Keep each option concise: what it is, what it solves, major costs, and key risks.

### Design principles for technical options

- Prefer one understandable code path over runtime-specific special cases.
- Validate inputs and fail clearly for invalid states. Do not hide programmer errors by returning plausible but incorrect results.
- Prefer established conventions over flexible abstractions, and flexible abstractions over permanent configuration.
- Treat new fields, settings, and public interfaces as long-term maintenance commitments.
- Prefer well-bounded changes that can be removed cleanly.
- Use familiar, proven technology and available infrastructure where possible.
- Design for deterministic, isolated testing.
- Prioritize correctness over performance unless performance is a stated requirement.
- Put changes in the appropriate design boundary; avoid quick fixes that create hidden coupling.

## 6. Evaluate and recommend

Compare viable options against the criteria. Present a concise proposal containing:

- Problem statement.
- Evaluation criteria.
- Viable options and tradeoffs.
- One clear recommendation and why it is preferred.
- Important risks, irreversible consequences, assumptions, and open decisions.

Keep proposals direct. Store them in the requester’s approved shared documentation system when durable review or collaboration is needed; otherwise provide them in the current workspace. Use a clear title, such as `DD MMM YYYY: Solve — topic`.

If this is analysis-only work, stop here.

## 7. Plan, implement, and verify

For larger work, create an implementation plan before changing the system. Include scope, ordered steps, affected components, data or migration strategy, rollback approach, test strategy, deployment steps, and follow-up ownership.

Implement the approved solution using project conventions. Run relevant automated tests, static checks, and focused manual verification. Confirm results against the evaluation criteria, including compatibility and failure behavior.

Do not claim success based only on completed code. State what was actually tested and what remains unverified. Commit, publish, or deploy only under the requester’s repository, review, release, and access practices.

## 8. Hand off

Report:

- What changed and the outcome it enables.
- Verification performed and its results.
- Known limitations, risks, and deferred work.
- Required user actions, rollout steps, or monitoring.
- References to the proposal, plan, and change set where applicable.

Keep the handoff focused on useful outcomes and operational facts rather than temporary implementation detail.
